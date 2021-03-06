---
title: Подключение к Smartsheet с помощью Power BI
description: Smartsheet для Power BI
author: SarinaJoan
manager: kfile
ms.reviewer: maggiesMSFT
ms.service: powerbi
ms.subservice: powerbi-template-apps
ms.topic: conceptual
ms.date: 10/16/2017
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: 55d61e89b1fb01de472d967a312b25340d482951
ms.sourcegitcommit: 750f0bfab02af24c8c72e6e9bbdd876e4a7399de
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/04/2019
ms.locfileid: "54008474"
---
# <a name="connect-to-smartsheet-with-power-bi"></a>Подключение к Smartsheet с помощью Power BI
Smartsheet — это удобная платформа для совместной работы и обмена файлами. Пакет содержимого Smartsheet для Power BI включает панель мониторинга, отчеты и набор данных с обзором вашей учетной записи Smartsheet. Вы можете также использовать [Power BI Desktop](desktop-connect-to-data.md) для подключения напрямую к отдельным листам в учетной записи. 

Подключитесь к [пакету содержимого Smartsheet](https://app.powerbi.com/groups/me/getdata/services/smartsheet) для Power BI.

>[!NOTE]
>Для подключения и загрузки пакета содержимого для Power BI рекомендуется использовать учетную запись администратора Smartsheet, так как она обеспечивает доступ к дополнительным возможностям.

## <a name="how-to-connect"></a>Способы подключения
1. Нажмите кнопку **Получить данные** в нижней части левой панели навигации.
   
   ![](media/service-connect-to-smartsheet/pbi_getdata.png)
2. В поле **Службы** выберите **Получить**.
   
   ![](media/service-connect-to-smartsheet/pbi_getservices.png) 
3. Выберите **Smartsheet \> Получить**.
   
   ![](media/service-connect-to-smartsheet/smartsheet.png)
4. В качестве метода проверки подлинности выберите **oAuth2 \> Войти**.
   
   При появлении запроса введите учетные данные Smartsheet и пройдите проверку подлинности.
   
   ![](media/service-connect-to-smartsheet/creds.png)
   
   ![](media/service-connect-to-smartsheet/creds2.png)
5. После импорта данных в Power BI в области навигации слева появятся новая панель мониторинга, отчеты и набора данных. Новые элементы будут отмечены желтой звездочкой (\*). Выберите Smartsheet.
   
   ![](media/service-connect-to-smartsheet/dashboard.png)

**Дальнейшие действия**

* Попробуйте [задать вопрос в поле "Вопросы и ответы"](consumer/end-user-q-and-a.md) в верхней части информационной панели.
* [Измените плитки](service-dashboard-edit-tile.md) на информационной панели.
* [Выберите плитку](consumer/end-user-tiles.md), чтобы открыть соответствующий отчет.
* Хотя набор данных будет обновляться ежедневно по расписанию, вы можете изменить график обновлений или попытаться выполнять обновления по запросу с помощью кнопки **Обновить сейчас**

## <a name="whats-included"></a>Содержимое
Пакет содержимого Smartsheet для Power BI содержит общие сведения о вашей учетной записи Smartsheet, например число рабочих областей, отчеты и листы, в которые вносятся изменения, и т. д. Пользователи с правами администратора смогут также видеть некоторые сведения о пользователях в системе, например создателей верхних листов.  

Вы можете использовать соединитель Smartsheet в [Power BI Desktop](desktop-connect-to-data.md) для подключения напрямую к отдельным листам в учетной записи.  

## <a name="next-steps"></a>Дальнейшие действия:

[Что такое Power BI?](power-bi-overview.md)

[Получение данных для Power BI](service-get-data.md)