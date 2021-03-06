---
title: Настройка параметров прокси-сервера для локального шлюза данных
description: Сведения о настройке параметров прокси-сервера для локального шлюза данных.
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-gateways
ms.topic: conceptual
ms.date: 11/21/2017
ms.author: mblythe
LocalizationGroup: Gateways
ms.openlocfilehash: 2122ce9bd6eb850a51a06188ca1c10faf78f4bb1
ms.sourcegitcommit: ac63b08a4085de35e1968fa90f2f49ea001b50c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2019
ms.locfileid: "57964670"
---
# <a name="configuring-proxy-settings-for-the-on-premises-data-gateway"></a>Настройка параметров прокси-сервера для локального шлюза данных
Рабочие среды могут требовать, чтобы доступ в Интернет осуществлялся через прокси-сервер. Это может помешать локальному шлюзу данных подключаться к службе.

## <a name="does-your-network-use-a-proxy"></a>Используется ли прокси-сервер в вашей сети?
В приведенной ниже публикации на сайте superuser.com описано, как попытаться определить наличие прокси-сервера в сети.

[Как узнать, какой прокси-сервер используется? (SuperUser.com)](https://superuser.com/questions/346372/how-do-i-know-what-proxy-server-im-using)

## <a name="configuration-file-location-and-default-configuration"></a>Расположение файла конфигурации и конфигурация по умолчанию
Сведения о прокси-сервере настраиваются в файле конфигурации платформы .NET. Расположение и имена файлов зависят от используемого шлюза.

### <a name="on-premises-data-gateway"></a>Локальный шлюз данных
Локальный шлюз данных использует два основных файла конфигурации.

**Конфигурация**

Первый предназначен для экранов конфигурации, используемых непосредственно для настройки шлюза. Если возникают проблемы при настройке шлюза, обратитесь именно к этому файлу.

    C:\Program Files\On-premises data gateway\enterprisegatewayconfigurator.exe.config

**Служба Windows**

Второй служит для фактической службы Windows, которая взаимодействует со службой Power BI и обрабатывает запросы.

    C:\Program Files\On-premises data gateway\Microsoft.PowerBI.EnterpriseGateway.exe.config

## <a name="configuring-proxy-settings"></a>Настройка параметров прокси-сервера
По умолчанию для прокси-сервера используется следующая конфигурация:

```
<system.net>
    <defaultProxy useDefaultCredentials="true" />
</system.net>
```


В конфигурации по умолчанию применяется аутентификация Windows. Если прокси-сервер использует другую форму проверки подлинности, необходимо изменить параметры. Если вы не уверены, что именно следует сделать, обратитесь к администратору сети. Не рекомендуем использовать обычную проверку подлинности прокси. При попытке ее выполнения могут возникнуть ошибки, которые приведут к неправильной настройке шлюза. Чтобы устранить ошибку, выберите более надежный механизм проверки подлинности прокси.

Помимо использования учетных данных по умолчанию, можно добавить элемент <proxy>, чтобы более детально определить параметры прокси-сервера. Например, можно указать, что локальный шлюз данных всегда должен использовать прокси-сервер даже для локальных ресурсов, присвоив параметру bypassonlocal значение false. Это может помочь при устранении неполадок, если нужно отслеживать все запросы по протоколу HTTPS от локального шлюза данных в файлах журнала прокси-сервера. В соответствии с приведенным ниже образцом конфигурации все запросы должны передаваться через определенный прокси-сервер с IP-адресом 192.168.1.10.

```
<system.net>
    <defaultProxy useDefaultCredentials="true">
        <proxy  
            autoDetect="false"  
            proxyaddress="http://192.168.1.10:3128"  
            bypassonlocal="false"  
            usesystemdefault="true"
        />  
    </defaultProxy>
</system.net>
```

Кроме того, для подключения шлюза к облачным источникам данных через прокси-сервер обновите следующий файл: *C:\Program Files\On-premises data gateway\Microsoft.Mashup.Container.NetFX45.exe*. В файле разверните раздел `<configurations>`, чтобы включить указанное ниже содержимое, а также обновите атрибут `proxyaddress`, добавив сведения о прокси-сервере. Следующий пример будет перенаправлять все запросы облака через определенный прокси-сервер с IP-адресом 192.168.1.10.

```
<configuration>
<system.net>
    <defaultProxy useDefaultCredentials="true" enabled="true">
    <proxy proxyaddress=""http://192.168.1.10:3128" bypassonlocal="true" />
    </defaultProxy>
</system.net>
</configuration>
```

Дополнительные сведения о настройке элементов прокси-сервера в файлах конфигурации .NET см. в статье об [элементе defaultProxy (параметры сети)](https://msdn.microsoft.com/library/kd3cf2ex.aspx).

## <a name="changing-the-gateway-service-account-to-a-domain-user"></a>Смена учетной записи службы шлюза на пользователя домена
Если при настройке параметров прокси-сервера вы указали учетные данные по умолчанию, как описано выше, могут возникнуть проблемы с проверкой подлинности. Это связано с тем, что учетная запись службы по умолчанию представляет собой идентификатор безопасности службы, а не прошедшего проверку подлинности пользователя домена. Чтобы настроить правильную проверку подлинности на прокси-сервере, вы можете сменить учетную запись службы шлюза.

> [!NOTE]
> Чтобы избежать необходимости сбрасывать пароли, рекомендуется использовать управляемую учетную запись службы. Узнайте, как создать [управляемую учетную запись службы](https://technet.microsoft.com/library/dd548356.aspx) в Active Directory.
> 
> 

### <a name="change-the-on-premises-data-gateway-service-account"></a>Изменение учетной записи службы локального шлюза данных
1. Сведения о том, как изменить учетную запись службы Windows для **локального шлюза данных**.

    По умолчанию в качестве учетной записи для этой службы используется *NT SERVICE\PBIEgwService*. Ее рекомендуется заменить учетной записью пользователя домена Active Directory. Кроме того, чтобы избежать необходимости менять пароль, можно воспользоваться управляемой учетной записью службы.

    Учетная запись меняется на вкладке **Вход** в свойствах службы Windows.
2. Перезапустите **службу локального шлюза данных**.

    Выполните следующую команду в окне командной строки администратора.

        net stop PBIEgwService

        net start PBIEgwService
3. Запустите **средство настройки локального шлюза данных**. Вы можете нажать кнопку пуска Windows и выполнить поиск по запросу *локальный шлюз данных*.
4. Войдите в Power BI.
5. Восстановите шлюз с помощью ключа восстановления.

    В результате новая учетная запись службы сможет расшифровать учетные данные, сохраненные для источников данных.

> [!NOTE]
> Если вы изменяете учетную запись службы непосредственно на панели управления службами, записи ACL не обновляются автоматически. Необходимо убедиться, что новая учетная запись службы предоставляет доступ к файлам и папке установки. Папка установки локального шлюза данных находится здесь: C:\Program Files\On-premises data gateway. 
> 

## <a name="next-steps"></a>Дальнейшие действия
[Локальный шлюз данных (персональный режим)](service-gateway-personal-mode.md)
[Сведения о брандмауэре](service-gateway-onprem-tshoot.md#firewall-or-proxy)  
Появились дополнительные вопросы? [Ответы на них см. в сообществе Power BI.](http://community.powerbi.com/)

