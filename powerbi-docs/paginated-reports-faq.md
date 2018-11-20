---
title: 'Отчеты с разбивкой на страницы в Power BI (предварительная версия): вопросы и ответы'
description: В этой статье содержатся ответы на часто задаваемые вопросы об отчетах с разбивкой на страницы. Это отчеты с широкой поддержкой форматирования и идеальной попиксельной оптимизацией для печати или создания PDF.
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: report-builder
ms.topic: overview
ms.date: 11/05/2018
ms.author: maggies
ms.openlocfilehash: 0ddf95563c52af135ac7ae4fe71aeddcd2ce7313
ms.sourcegitcommit: b23fdcc0ceff5acd2e4d52b15b310068236cf8c7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "51268925"
---
# <a name="paginated-reports-in-power-bi-faq-preview"></a>Отчеты с разбивкой на страницы в Power BI (предварительная версия): вопросы и ответы

В этой статье содержатся ответы на часто задаваемые вопросы об отчетах с разбивкой на страницы. Это отчеты с широкой поддержкой форматирования и идеальной попиксельной оптимизацией для печати или создания PDF. Под термином "с разбивкой на страницы" подразумевается то, что формат отчетов подбирается с учетом отображения на нескольких страницах. Отчеты с разбивкой на страницы создаются на основе технологии RDL (языка определения отчетов), используемой в SQL Server Reporting Services. 

В этой статье содержатся ответы на многие распространенные вопросы, которые возникают у пользователей об отчетах с разбивкой на страницы в Power BI Premium, и о специальном средстве для создания отчетов с разбивкой на страницы, которое называется "построитель отчетов". Для публикации отчета в службе нужна лицензия Power BI Pro. Вы можете публиковать и совместно использовать отчеты с разбивкой на страницы в своей рабочей области или в рабочей области приложений, если эта рабочая область находится в емкости Power BI Premium. 

## <a name="administration"></a>Администрирование

### <a name="what-size-premium-capacity-do-i-need-for-paginated-reports"></a>Какой размер емкости Premium требуется для отчетов с разбивкой на страницы?

Рабочая нагрузка "Отчеты с разбивкой на страницы" доступна для номеров SKU P1–P3 в режиме общедоступной предварительной версии.  Вы также можете использовать ее в сценариях тестирования и разработки в номерах SKU A4–A6.

### <a name="what-is-the-maximum-memory-threshold-i-can-put-for-paginated-reports-in-my-capacity"></a>Какое максимальное пороговое значение памяти я могу указать в моей емкости для отчетов с разбивкой на страницы?

В настоящее время вы можете зарезервировать для этой рабочей нагрузки только 50 % памяти. 

### <a name="how-does-user-access-work-for-paginated-reports"></a>Как работает доступ пользователей к отчетам с разбивкой на страницы?

Доступ пользователей к отчетам с разбивкой на страницы организован так же, как к любому содержимому в службе Power BI. 

### <a name="how-do-i-turn-onoff-my-paginated-reports-workload"></a>Как мне включить или выключить рабочую нагрузку "Отчеты с разбивкой на страницы"?

Рабочую нагрузку "Отчеты с разбивкой на страницы" может включить и (или) выключить администратор емкости на странице портала администрирования емкости.  

### <a name="how-can-i-monitor-usage-of-paginated-reports-in-my-tenant"></a>Как мне отслеживать использование отчетов с разбивкой на страницы в клиенте?

В журналах аудита Office 365 сохраняется подробная информация об использовании отчетов этого типа во время следующих событий: 

- просмотр отчета Power BI;
- удаление отчета Power BI;
- создание отчета Power BI;
- Скачанный отчет Power BI

Для отчетов с разбивкой на страницы поле ReportType имеет значение PaginatedReport, чтобы отличать их от обычных отчетов Power BI.

Также журналы аудита предоставляют для отчетов с разбиением на страницы данные о следующих событиях:

- привязка набора данных Power BI к шлюзу;
- обнаружение источника данных Power BI;
- TakeOverDatasource

### <a name="can-i-monitor-this-workload-through-the-premium-capacity-monitoring-app"></a>Могу ли я отслеживать эту рабочую нагрузку через приложение мониторинга емкости Premium?

Эта возможность пока недоступна. Мониторинг скоро будет доступен в режиме общедоступной предварительной версии на новой вкладке в существующих отчетах, и будет содержать те же важные данные, что и для наборов данных Power BI.

### <a name="do-i-need-a-pro-license-to-create-and-publish-paginated-reports"></a>Нужна ли лицензия Pro, чтобы создавать и публиковать отчеты с разбивкой на страницы?

Да. Вы не сможете отправить отчеты в рабочую область, не имея лицензии Pro. Вы можете свободно скачать и опробовать построитель отчетов без лицензии Pro, но созданные отчеты с разбивкой на страницы не удастся опубликовать. 

### <a name="what-if-i-have-a-paginated-report-in-a-workspace-and-the-paginated-report-workload-is-turned-off"></a>Что произойдет, если в моей рабочей области есть отчет с разбивкой на страницы, но рабочая нагрузка "Отчеты с разбивкой на страницы" в ней отключена?

Вы получите сообщение об ошибке и не сможете просмотреть такой отчет, пока не включите эту рабочую нагрузку. Но вы можете спокойно удалить этот отчет из рабочей области.

### <a name="what-is-the-default-memory-for-each-of-the-premium-skus-supported-for-paginated-reports"></a>Какой объем памяти по умолчанию поддерживается для отчетов с разбивкой на страницы для каждого номера SKU уровня Premium?

Объем памяти по умолчанию для отчетов с разбивкой на страницы для номеров SKU уровня Premium составляет:

- **P1/A4**: по умолчанию 20 %; не менее 10 %;
- **P2/A5**: по умолчанию 10 %; не менее 5 %;
- **P3/A6**: по умолчанию 5 %; не менее 2,5 %;

## <a name="general"></a>Общий

### <a name="when-should-i-use-a-paginated-report-vs-a-power-bi-report"></a>В каких случаях отчет с разбивкой на страницы больше подходит, чем отчет Power BI?

Отчеты с разбивкой на страницы подходят в тех случаях, когда важны широкая поддержка форматирования и идеальная попиксельная оптимизация для печати или создания PDF.  Например, отчет с разбивкой на страницы будет правильным выбором для создания отчета о результатах финансовой деятельности организации.  

Отчеты Power BI оптимизированы для исследования данных и интерактивных возможностей.  В формате отчета Power BI лучше создавать, например, отчет о продажах с возможностью выборки данных по конкретным регионам, отраслям и клиентам и с мгновенным отображением соответствующих подытогов.

### <a name="the-documentation-says-report-builder-is-the-preferred-authoring-tool-can-i-create-paginated-reports-in-sql-server-data-tools-for-power-bi"></a>В документации сказано, что построитель отчетов является основным средством разработки. Но могу ли я создавать отчеты с разбивкой на страницы в SQL Server Data Tools для Power BI?

Да, но служба Power BI позволяет передать за раз только один элемент, поэтому она пока не поддерживает многие распространенные сценарии разработки в SQL Server Data Tools (SSDT). Полный [список неподдерживаемых функций](#what-paginated-report-features-in-ssrs-arent-yet-supported-in-power-bi) размещен далее в этой статье с вопросами и ответами.  

### <a name="what-versions-of-report-builder-do-you-support"></a>Какие версии построителя отчетов поддерживаются?

Для создания отчетов и их публикации в службе Power BI следует всегда использовать последнюю версию построителя отчетов для SQL Server 2016. Установите [построитель отчетов из Центра загрузки Майкрософт](https://www.microsoft.com/download/details.aspx?id=53613).

### <a name="how-do-i-move-existing-reports-i-have-saved-in-sql-server-reporting-services-to-power-bi"></a>Как переместить в Power BI существующие отчеты, сохраненные в SQL Server Reporting Services (SSRS)?

Скачайте нужный отчет с сервера, а затем передайте его в Power BI через портал.  В настоящее время средство миграции отсутствует, но мы намерены создать его, когда завершится стадия общедоступной предварительной версии и будет достигнуто достаточное равенство функций между этими продуктами.

### <a name="can-i-open-reports-and-publish-directly-to-the-service"></a>Могу ли я открывать и публиковать отчеты непосредственно в службе?

Сейчас это невозможно. Через некоторое время мы добавим возможность открывать и публиковать отчеты непосредственно в службе из построителя отчетов, как это возможно сейчас в Power BI Desktop.

### <a name="what-paginated-report-features-in-ssrs-arent-yet-supported-in-power-bi"></a>Какие функции SSRS для отчетов с разбивкой на страницы пока не поддерживаются в Power BI?

Сейчас отчеты с разбивкой на страницы не поддерживают следующие элементы:

- общие источники данных;
- Общие наборы данных
- вложенные отчеты;
- действия сквозного перехода и детализации;
- связанные отчеты;
- Закладки
- слои карт Bing;
- пользовательские шрифты;
- скрытые параметры.

Переключение и интерактивная сортировка пока не действуют в рабочей среде, но будут добавлены в ближайшее время.    

Вы получите сообщение об ошибке при попытке отправить файл с функцией, которая пока не поддерживается в службе Power BI, за исключением функций переключения и (или) сортировки.

### <a name="what-data-sources-do-you-support-currently-for-paginated-reports"></a>Какие источники данных поддерживаются сейчас для отчетов с разбивкой на страницы?

Мы поддерживаем Базу данных SQL Azure, и табличные модели SQL Server и SQL Server Analysis Services (SSAS) через локальный шлюз. Сейчас не поддерживаются многомерные модели SSAS.

Если доступ к SSAS осуществляется через шлюз, для нормальной работы пользователь, чьи учетные данные сохранены, должен иметь повышенные права в службах SSAS.

### <a name="what-authentication-methods-do-you-support"></a>Какие методы проверки подлинности поддерживаются?

Сейчас необходимо сохранять на портале или шлюзе имя пользователя и пароль для доступа к источнику данных.  Позже в предварительную версию будут добавлены дополнительные методы проверки подлинности, например поддержка безопасности на уровне строк.

### <a name="can-i-use-a-power-bi-dataset-as-a-data-source-for-my-paginated-report"></a>Могу ли я использовать набор данных Power BI в качестве источника данных для отчета с разбивкой на страницы?

Пока нет, но такая поддержка будет добавлена в ближайшее время.

### <a name="can-i-use-stored-procedures-through-the-gateway"></a>Могу ли я использовать хранимые процедуры через шлюз?

Вы можете использовать хранимую процедуру через шлюз, но только если она не использует параметры.

### <a name="what-export-formats-are-available-for-my-report-in-the-power-bi-service"></a>Какие форматы экспорта доступны для отчетов в службе Power BI?

Вы можете экспортировать отчеты в Microsoft Excel, Microsoft Word, Microsoft PowerPoint, PDF, CSV, XML и MHTML.

### <a name="can-i-print-paginated-reports"></a>Могу ли я распечатать отчет с разбивкой на страницы?

Сейчас распечатать для печати можно только экспортировать файл в формат PDF. Прямая печать из режима просмотра отчета с разбивкой на страницы будет скоро добавлена. 

### <a name="are-e-mail-subscriptions-available-yet-for-paginated-reports"></a>Доступна ли подписка по электронной почте на отчеты с разбивкой на страницы?

Нет, подписка по электронной почте будет добавлена позднее.

### <a name="what-features-from-ssrs-will-you-be-supporting-in-the-power-bi-service"></a>Какие функции из служб SSRS будут поддерживаться в службе Power BI?

В перспективе мы намерены обеспечить почти полное равенство функций между этими двумя продуктами.  Некоторые особенности работы SSRS и Power BI делают бессмысленными попытки миграции некоторых шаблонов, используемых в SSRS, например, Power BI использует другие модели разрешений. Но все решения по этому поводу мы будем принимать только с учетом обратной связи от клиентов и партнеров.

### <a name="can-i-run-custom-code-in-my-report"></a>Могу ли я запускать в отчете пользовательский код?

Да, мы поддерживаем возможность запуска пользовательского кода в отчетах, как и в службе SSRS.

### <a name="does-this-mean-ssrs-is-going-away"></a>Означает ли это, что SSRS скоро прекратит работу?

Конечно, нет.  Это новое предложение позволяет клиентам использовать отчеты с разбивкой на страницы в облачной системе.  

### <a name="can-i-use-power-bi-embedded-to-embed-my-paginated-reports-into-an-app-im-hosting"></a>Могу ли я с помощью Power BI Embedded внедрить отчеты с разбивкой на страницы в размещаемое приложение?

Мы планируем реализовать поддержку этого сценария в существующих интерфейсах API Power BI, но пока не определили для него график внедрения.

### <a name="can-i-drill-through-from-a-power-bi-report-to-a-paginated-report"></a>Могу ли я переходить из отчета Power BI в отчет с разбивкой на страницы для просмотра подробных сведений?

Пока нет, но мы точно реализуем поддержку такого сценария.

### <a name="can-i-share-my-paginated-report-content-through-a-power-bi-app"></a>Могу ли я использовать содержимое из отчета с разбивкой на страницы в приложении Power BI?

Сейчас вы можете предоставлять общий доступ к конкретным отчетам с разбивкой на страницы другим пользователям с помощью действия управления доступом на портале. Мы пока не поддерживаем совместное использование в приложении, но намерены реализовать такую поддержку в ближайшее время. Кроме того, на панели инструментов будет создана кнопка для предоставления общего доступа.

### <a name="will-other-report-specific-features-in-power-bi-like-pinning-to-report-tiles-to-dashboards-work-with-paginated-reports"></a>Будут ли работать для отчетов с разбивкой на страницы другие функции отчетов в Power BI, например закрепление плиток на панелях мониторинга?

Мы планируем обеспечить для отчетов максимально возможную поддержку всех основных сценариев работы службы.  В идеале должно быть так, чтобы пользователь воспринимал эти отчеты так же, как и другие элементы в списке отчетов на портале, несмотря на использование другого средства для их создания. Пользователю не важно, как создан отчет, ему лишь нужно выполнить свою задачу.  Хорошим примером равенства функций можно считать запланированную поддержку комментариев. Эта функция будет работать немного по-разному для отчетов разных типов, но вы сможете использовать комментарии для обоих типов.

### <a name="are-you-planning-to-create-a-new-authoring-tool-for-paginated-reports-in-the-power-bi-service--we-cant-do-everything-we-need-to-with-report-builder-today"></a>Планируется ли создать новое средство для разработки отчетов с разбивкой на страницы в службе Power BI?  Сейчас построитель отчетов не позволяет нам выполнить все, что нужно.

Мы пока еще продолжаем анализ разных вариантов и инструментов, но в любом случае реализуем поддержку таких функций, как управление жизненным циклом приложений, пользовательские расширения и многих других, даже если они существуют только в одном из средств разработки для SSRS. 

### <a name="is-a-migration-tool-planned-so-ssrs-customers-can-move-their-existing-reports-and-assets-to-power-bi"></a>Есть ли планы создать средство миграции, чтобы пользователи SSRS могли переносить существующие отчеты и ресурсы в Power BI?

Да, но к этому мы перейдем только после того, как завершим создание базового набора функций в службе Power BI.

### <a name="will-i-ever-be-able-to-create-both-paginated-reports-and-power-bi-reports-in-a-single-authoring-tool"></a>Будет ли у меня когда-либо возможность создавать отчеты с разбивкой на страницы и обычные отчеты Power BI в едином средстве разработки?

В настоящее время у нас нет планов создать единое средство разработки, но мы рассматриваем возможность распространять разные средства разработки в едином наборе BI, чтобы уйти от использования разных наименований и разных интерфейсов скачивания для этих средств.

### <a name="is-there-a-report-viewer-control-for-paginated-reports-in-the-power-bi-service"></a>Существует ли элемент управления для просмотра отчетов с разбивкой на страницы в службе Power BI?

Нет, в настоящее время не существует элементов управления для просмотра отчетов.

### <a name="can-you-search-for-paginated-reports-from-the-new-home-experience-in-the-power-bi-service"></a>Можно ли найти отчет с разбивкой на страницы через новый интерфейс главной страницы в службе Power BI?

Нет, вы пока не можете выполнять поиск отчетов с разбиением на главной странице.  Но вы будете их видеть в других разделах нового интерфейса главной страницы.

## <a name="next-steps"></a>Дальнейшие действия

- [Установка построителя отчетов из Центра загрузки Майкрософт](https://www.microsoft.com/download/details.aspx?id=53613)
- [Руководство по созданию отчета с разбивкой на страницы](paginated-reports-quickstart-aw.md)