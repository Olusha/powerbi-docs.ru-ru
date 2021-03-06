---
title: Что такое Microsoft Power BI Premium?
description: Решение Power BI Premium предоставляет выделенную емкость для вашей организации или команды, обеспечивая более стабильную производительность при работе большими объемами данных. При этом вам не нужно приобретать лицензии для каждого пользователя.
author: minewiskan
ms.author: owend
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: conceptual
ms.date: 03/12/2019
ms.custom: seodec18
LocalizationGroup: Premium
ms.openlocfilehash: f327cb95c10756f079778d20e62cba4871b95c02
ms.sourcegitcommit: ac63b08a4085de35e1968fa90f2f49ea001b50c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2019
ms.locfileid: "57964946"
---
# <a name="what-is-microsoft-power-bi-premium"></a>Что такое Microsoft Power BI Premium?

> [!NOTE]
> Сейчас эта статья перерабатывается для описания новых функций, предоставления более подробных сведений и повышения удобочитаемости. Актуальные сведения см. в статье [Развертывание емкостей Power BI Premium и управление ими](whitepaper-powerbi-premium-deployment.md).

Power BI Premium предоставляет выделенные ресурсы для выполнения службы Power BI для вашей организации. Это решение обеспечивает более стабильную производительность при работе с большими объемами данных. Power BI Premium также обеспечивает широкое распространение содержимого без необходимости приобретать лицензии Pro для каждого пользователя, использующего содержимое.  

## <a name="premium-capacity-and-shared-capacity"></a>Общая емкость и емкость Premium

Воспользуйтесь преимуществами Power BI Premium, назначив для рабочих областей *емкость Premium*. Емкость Premium — это выделенный ресурс вашей организации. Рабочие области, не назначенные емкости Premium, находятся в *общей емкости*. В общей емкости рабочие нагрузки выполняются на вычислительных ресурсах, совместно используемых другими пользователями.

На рисунке ниже показана связь между емкостью Premium и общей емкостью: в качестве примера используется организация Contoso.

![Иллюстрация Power BI Premium](media/service-premium/premium-chart.png)

| С областями | Описание |
| --- | --- |
| **(1)** Элементы с емкостью Premium | <ul><li>Для доступа к рабочим областям приложения (в качестве участников или администраторов) и публикации приложений требуется лицензия Power BI Pro.<li>Для совместного использования приложения требуется лицензия Pro, однако для работы с приложением лицензия не требуется.<li>Все получатели панели мониторинга, независимо от назначенной им лицензии, могут настраивать оповещения об изменении данных.<li>Интерфейсы REST API для внедрения используют учетную запись службы с лицензией Pro, а не учетную запись пользователя.</ul> |
| **(2)** Моя рабочая область в общей емкости | <ul><li>Для общего доступа и использования приложения требуется лицензия Pro.</ul> |
| **(3)** Рабочие области приложений в общей емкости | <ul><li>Для использования любого приложения требуется лицензия Pro.</ul>|
| | |

В общей емкости Power BI включает дополнительные ограничения для отдельных пользователей, чтобы обеспечить высокое качество работы для всех пользователей. По умолчанию ваша рабочая область находится в общей емкости, включающей личную область *Моя рабочая область* и рабочие области приложений.

В таблице ниже приводится краткий перечень различий между общей емкостью и емкостью Premium.

|  | Общая емкость | Емкость Power BI Premium |
| --- | --- | --- |
| **Частота обновления** |8 раз в день |48 раз в день |
| Изоляция с помощью выделенного оборудования |![Недоступно](media/service-premium/not-available.png) |![](media/service-premium/available.png) |
| Распространение на предприятии для *всех пользователей* | | |
| Приложения и совместное использование |![Недоступно](media/service-premium/not-available.png) |![](media/service-premium/available.png) |
| Внедренные API и элементы управления |![Недоступно](media/service-premium/not-available.png) |![](media/service-premium/available.png)<sup>[1](#fnt1)</sup> |
| Локальная публикация отчетов Power BI |![Недоступно](media/service-premium/not-available.png) |![](media/service-premium/available.png) |
| | | |

<a name="fnt1">1</a> После выпуска общедоступной версии Power BI Premium улучшения будут расширены.



### <a name="premium-capacity-nodes"></a>Узлы емкости Premium

Power BI Premium предоставляется в виде узлов с разной емкостью виртуальных ядер. Дополнительные сведения о конкретных номерах SKU предложений и затратах см. на странице [расценок на Power BI](https://powerbi.microsoft.com/pricing/). Кроме того, доступен [калькулятор затрат](https://powerbi.microsoft.com/calculator/). Сведения о планирования емкости для внедренной аналитики см. в [техническом документе по планированию развертывания Power BI Enterprise](https://aka.ms/pbienterprisedeploy). Подведем итоги.

* Узлы P можно использовать для внедренных развертываний или развертываний служб.

* Узлы EM можно использовать только для внедренных развертываний. Для узлов EM не поддерживаются расширенные возможности, такие как предоставление общего доступа к приложению пользователям, у которых нет лицензии Power BI Pro.

| Узел емкости | Число виртуальных ядер<br/>*(Серверная часть и интерфейс)*  | Виртуальные ядра сервера <sup>[1](#fn1)</sup> | Виртуальные ядра интерфейса <sup>[2](#fn2)</sup> | Ограничения для подключений DirectQuery и активных подключений | Максимальное количество одновременных обновлений |
| --- | --- | --- | --- | --- | --- |
| EM1 (ежемесячная подписка) |1 виртуальное ядро |0,5 виртуальных ядер, 2,5 ГБ ОЗУ |0,5 виртуальных ядра |3,75 в секунду |  1 |
| EM2 (ежемесячная подписка) |2 виртуальных ядра |1 виртуальное ядро, 5 ГБ ОЗУ |1 виртуальное ядро |7,5 в секунду |  2 |
| EM3 (ежемесячная подписка) |4 виртуальных ядра |2 виртуальных ядра, 10 ГБ ОЗУ |2 виртуальных ядра | 15 | 3 |
| P1 |8 виртуальных ядер |4 виртуальных ядра, 25 ГБ ОЗУ |4 виртуальных ядра |30 в секунду | 6 |
| P2 |16 виртуальных ядер |8 виртуальных ядер, 50 ГБ ОЗУ |8 виртуальных ядер |60 в секунду | 12 |
| P3 |32 виртуальных ядра |16 виртуальных ядер, 100 ГБ ОЗУ |16 виртуальных ядер |120 в секунду | 24 |
| | | | | | |

<a name="fn1">1.</a> Виртуальные ядра интерфейса отвечают за работу веб-службы, например панель мониторинга и отчеты, управление правами доступа, планирование, интерфейсы API, передачу и скачивание, а также все взаимодействие с пользователем. 

<a name="fn2">2.</a> Виртуальные ядра сервера выполняют трудоемкие задачи: обработку запросов, управление кэшем, выполнение серверов R Server, обновление данных, обработку запросов на естественном языке, обслуживание веб-каналов в реальном времени, а также отрисовку отчетов и изображений на стороне сервера. Для внутренних ядер также резервируется определенный объем памяти. Наличие достаточного объема памяти становится особенно важным при работе с большими моделями данных или с большим числом активных наборов данных.

## <a name="workloads-in-premium-capacity"></a>Рабочие нагрузки в емкости Premium

По умолчанию емкости Power BI Premium и Power BI Embedded поддерживают только рабочие нагрузки, связанные с выполнением запросов Power BI в облаке. Версия Premium также поддерживает дополнительные рабочие нагрузки для **ИИ**, **потоков данных** и **отчетов с разбивкой на страницы**. Прежде чем эти рабочие нагрузки смогут использовать ресурсы емкости, их нужно включить на портале администрирования Power BI или с помощью REST API для Power BI. Каждая рабочая нагрузка имеет параметры по умолчанию для поддержки максимального объема памяти, который может использовать каждая рабочая нагрузка. Но вы можете настроить другие параметры потребления памяти, чтобы определить, как рабочие нагрузки влияют друг на друга и как они потребляют ресурсы емкости. Дополнительные сведения см. в статье [Настройка рабочих нагрузок](service-admin-premium-workloads.md).

## <a name="power-bi-report-server"></a>Сервер отчетов Power BI

Power BI Premium также включает возможность локального запуска сервера отчетов Power BI в организации. Дополнительные сведения см. в разделе [Приступая к работе с сервером отчетов Power BI](report-server/get-started.md).

## <a name="next-steps"></a>Дальнейшие действия

[Развертывание емкостей Power BI Premium и управление ими](whitepaper-powerbi-premium-deployment.md)   
[Как купить Power BI Premium](service-admin-premium-purchase.md)   
[Вопросы и ответы по Power BI Premium](service-premium-faq.md)   



Появились дополнительные вопросы? [Попробуйте задать вопрос в сообществе Power BI.](https://community.powerbi.com/)
