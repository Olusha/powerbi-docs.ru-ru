---
title: Часто задаваемые вопросы о Power BI Embedded
description: Просмотрите список часто задаваемых вопросов о Power BI Embedded и ознакомьтесь с ответами.
author: markingmyname
ms.author: maghan
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: conceptual
ms.date: 02/05/2019
ms.openlocfilehash: abc45f3c32ee5db81f71295268db85bfce23aafd
ms.sourcegitcommit: 39bc75597b99bc9e8d0a444c38eb02452520e22b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/25/2019
ms.locfileid: "58430445"
---
# <a name="frequently-asked-questions-about-power-bi-embedded"></a>Часто задаваемые вопросы о Power BI Embedded

* Если у вас возникли другие вопросы, [задайте их участникам сообщества Power BI](http://community.powerbi.com/).
* Проблема до сих пор не устранена? Посетите [страницу поддержки по Power BI](https://powerbi.microsoft.com/support/).

## <a name="general"></a>Общие

### <a name="what-is-power-bi-embedded"></a>Что такое Power BI Embedded?

[Microsoft Power BI Embedded (PBIE)](azure-pbie-what-is-power-bi-embedded.md) позволяет разработчикам приложений внедрять впечатляющие, полностью интерактивные отчеты в приложения, не тратя время и деньги на создание собственных визуализаций данных и элементов управления с нуля.

### <a name="who-is-the-target-audience-for-power-bi-embedded"></a>Какова целевая аудитория службы Power BI Embedded?

Разработчики и компании, которые создают собственные приложения, называются независимыми поставщиками программного обеспечения.

### <a name="how-is-power-bi-embedded-different-from-power-bi-the-service"></a>Чем Power BI Embedded отличается от службы Power BI?

Служба Power BI Embedded предназначена для независимых поставщиков ПО и разработчиков, которые создают приложения и хотят внедрять в них визуальные элементы, чтобы помочь клиентам решать свои задачи, не создавая средства аналитики с нуля. [Встроенная аналитика](embedding.md) позволяет бизнес-пользователям получать доступ к бизнес-данным и выполнять запросы на формирование аналитических сведений на основе этих данных в приложении.

Power BI представляет собой решение программного обеспечения как услуги для аналитики, которое предоставляет организациям единое представление их критически важных бизнес-данных.

### <a name="what-is-the-difference-between-power-bi-premium-and-power-bi-embedded"></a>В чем разница между Power BI Premium и Power BI Embedded?

Power BI Premium — это комплексное решение бизнес-аналитики для предприятий, которое обеспечивает единое представление данных организации, сведений о партнерах, клиентах и поставщиках. Power BI Premium помогает организациям в принятии решений. Power BI Premium — это продукт SaaS, с помощью которого пользователи могут работать с содержимым через портал Power BI, мобильное приложение и приложения, разработанные в компании.

Служба Power BI Embedded предназначена для независимых поставщиков ПО и разработчиков, которые создают приложения и хотят внедрить в них визуальные элементы. Power BI Embedded помогает клиентам принимать решения. Так как эта служба создана для разработчиков приложений, пользователи этих приложений, как в организации, так и за ее пределами, могут работать с содержимым, хранящимся в емкости Power BI Embedded. К емкости Power BI Embedded невозможно предоставить общий доступ, опубликовав в Интернете или на SharePoint одним щелчком, и для него не поддерживаются отчеты SSRS.

### <a name="what-is-the-microsoft-recommendation-for-when-a-customer-should-buy-power-bi-premium-vs-power-bi-embedded"></a>В каких случаях корпорация Майкрософт рекомендует покупать Power BI Premium, а в каких — Power BI Embedded?

Корпорация Майкрософт рекомендует организациям покупать корпоративное облачное решение для самостоятельной бизнес-аналитики Power BI Premium, а независимым поставщикам ПО — облачное решение Power BI Embedded со встроенными компонентами аналитики. Тем не менее, клиенты не ограничены в выборе продукта.

Возможно, в некоторых случаях независимым поставщикам ПО (как правило, крупным) потребуется номер SKU P, чтобы получить дополнительные возможности предварительно упакованной службы Power BI для своей организации и внедрить их в приложения. Некоторые предприятия могут решить использовать номера SKU A в Azure, если они собираются только создавать бизнес-приложения и внедрять в них средства аналитики, но при этом они не заинтересованы использовать предварительно упакованную службу Power BI.

### <a name="how-many-embed-tokens-can-i-create"></a>Сколько можно создать токенов внедрения?

Токены внедрения с лицензиями PRO предназначены для тестирования при разработке, поэтому количество таких токенов, создаваемых главной учетной записью или [субъектом-службой](embed-service-principal.md) Power BI, ограничено. Необходимо [приобрести емкость](#technical) для возможности внедрения в рабочей среде. В этом случае приобретения емкости количество создаваемых токенов внедрения не ограничено. Выберите [Доступные компоненты](https://docs.microsoft.com/rest/api/power-bi/availablefeatures), чтобы проверить данные по использованию Embedded, выраженные в процентах от общей емкости.

## <a name="technical"></a>Технические вопросы

### <a name="what-is-the-difference-between-the-a-skus-in-azure-and-the-em-skus-in-office-365"></a>В чем разница между номерами SKU A в Azure и SKU EM в Office 365?

PowerBI.com — это корпоративное решение, которое содержит множество возможностей, таких как совместная работа пользователей, подписки по электронной почте и т. д., в рамках предложения "программное обеспечение как услуга" (SaaS).

Power BI Embedded — это набор интерфейсов API, позволяющих разработчикам создавать внедряемые решения для аналитики, в рамках предложения PaaS (платформа как услуга). В сценариях встроенной аналитики независимые поставщики ПО и разработчики могут использовать PowerBI.com, чтобы управлять содержимым решения встроенной аналитики и настройками на уровне клиента.

Ниже приведен неполный список различий между функциями, используемыми в решениях.

| Избранное | Power BI Embedded | Емкость Power BI Premium | Емкость Power BI Premium |
|----------------------------------------------------------------------------------|-------------------|---------------------------|---------------------------|
|   | (Номера SKU A) | (Номера SKU EM) | (Номера SKU P) |
| Внедрение артефактов из рабочих областей приложения Power BI | Емкость Azure | Емкость Office 365 | Емкость Office 365 |
| Использование отчетов Power BI во внедренном приложении | Да | Да | Да |
| Использование отчетов Power BI в SharePoint | Нет | Да | Да |
| Использование отчетов Power BI в Dynamics | Нет | Да | Да |
| Использование отчетов Power BI в Teams (за исключением мобильного приложения) | Нет | Да | Да |
| Доступ к содержимому с бесплатной лицензией Power BI на Powerbi.com и в Power BI Mobile | Нет | Нет | Да |
| Доступ к содержимому с бесплатной лицензией Power BI в приложениях MS Office | Нет | Да | Да |

### <a name="power-bi-now-offers-three-skus-for-embedding-a-skus-em-skus-and-p-skus-which-one-should-i-purchase-for-my-scenario"></a>Сейчас в Power BI предлагается три типа номеров SKU для внедрения: SKU A, SKU EM и SKU P. Какой из них следует приобрести в моем случае?

|  |SKU A (Power BI Embedded)  |SKU EM (Power BI Premium)  |SKU P (Power BI Premium)  |
|---------|---------|---------|---------|
|Купить  |Портал Azure |Office |Office |
|Варианты использования | Внедрение содержимого в собственное приложение | <li> Внедрение содержимого в собственное приложение <br><br><br> <li> Внедрение содержимого в приложения MS Office: <br> - [SharePoint](https://powerbi.microsoft.com/blog/integrate-power-bi-reports-in-sharepoint-online/) <br> - [Teams (за исключением мобильного приложения)](https://powerbi.microsoft.com/blog/power-bi-teams-up-with-microsoft-teams/) <br> - [Dynamics 365](https://docs.microsoft.com/dynamics365/customer-engagement/basics/add-edit-power-bi-visualizations-dashboard) | <li> Внедрение содержимого в собственное приложение <br><br><br> <li> Внедрение содержимого в приложения MS Office: <br> - [SharePoint](https://powerbi.microsoft.com/blog/integrate-power-bi-reports-in-sharepoint-online/) <br> - [Teams (за исключением мобильного приложения)](https://powerbi.microsoft.com/blog/power-bi-teams-up-with-microsoft-teams/) <br> - [Dynamics 365](https://docs.microsoft.com/dynamics365/customer-engagement/basics/add-edit-power-bi-visualizations-dashboard) <br><br><br> <li> Предоставление общего доступа к содержимому пользователям Power BI через [службу Power BI](https://powerbi.microsoft.com/)  |
|Выставление счетов |Каждый час |Ежемесячно |Ежемесячно |
|Обязательство  |Никаких обязательств |Ежегодно  |Ежемесячно или ежегодно |
|Отличия |Полная гибкость — масштабируемость, приостановление и возобновление использования ресурсов на портале Azure или с помощью API  |Можно использовать для внедрения содержимого в SharePoint Online и Microsoft Teams (за исключением мобильного приложения) |Объединение возможности внедрения в приложение и использования службы Power BI в одной емкости |

### <a name="what-are-the-prerequisites-to-create-a-pbie-capacity-in-azure"></a>Что необходимо для создания емкости PBIE в Azure?

* Необходимо войти в каталог организации (учетные записи MSA не поддерживаются).
* Необходим клиент Power BI. Как минимум один пользователь в вашем каталоге должен зарегистрироваться в Power BI. 
* Необходимо иметь подписку Azure в каталоге организации.

### <a name="how-can-i-monitor-power-bi-embedded-capacity-consumption"></a>Как отслеживать использование емкости Power BI Embedded?

* На [портале администрирования Power BI](../service-admin-portal.md#power-bi-embedded).

* Загрузка [приложения метрик](https://review.docs.microsoft.com/power-bi/service-admin-premium-monitor-capacity) в Power BI.

* С помощью [Журнала диагностики Azure](azure-pbie-diag-logs.md).

### <a name="can-my-capacity-scale-automatically-to-adjust-to-the-consumption-of-my-app"></a>Может ли емкость автоматически масштабироваться в соответствии с использованием приложения?

Автоматическое масштабирование сейчас не поддерживается, но все интерфейсы API доступны для масштабирования.

### <a name="why-creatingscalingresuming-a-capacity-results-in-putting-the-capacity-into-a-suspended-state"></a>Почему создание, масштабирование и возобновление емкости приводит к переводу емкости в приостановленное состояние?

Подготовка емкости (при масштабировании, возобновлении, создании) может завершиться сбоем. Вызывающий объект вызова подготовки должен проверять состояние подготовки емкости с помощью API получения сведений: [Емкость -> Получить сведения](https://docs.microsoft.com/rest/api/power-bi-embedded/capacities/getdetails).

### <a name="can-i-only-create-power-bi-embedded-capacities-in-a-specific-region"></a>Я могу создавать емкости Power BI Embedded только в определенном регионе?

С функцией [Поддержка нескольких регионов (предварительная версия)](embedded-multi-geo.md) вы можете приобрести [емкость Power BI Embedded](azure-pbie-create-capacity.md) в регионе, где не расположен ваш домашний клиент Power BI

### <a name="how-can-i-find-what-is-my-pbi-tenant-region"></a>Как узнать свой регион клиента PBI?

Чтобы узнать регион клиента PBI, можно использовать портал PBI.

[https://app.powerbi.com/](https://app.powerbi.com/) > ? > О Power BI

![О Power BI](media/embedded-faq/about-01.png)
![Регион клиента](media/embedded-faq/tenant-location-01.png)

### <a name="what-is-supported-by-the-cloud-solution-provider-csp-channel"></a>Какие возможности поддерживаются каналом поставщиков облачных решений (CSP)?

* Вы можете создать PBIE для вашего клиента с типом подписки CSP.
* Пользователь с партнерской учетной записью может войти в клиент заказчика и приобрести для него PBIE, указав пользователя клиента в качестве администратора емкости Power BI.

### <a name="why-do-i-get-an-unsupported-account-message"></a>Почему я получаю сообщение о неподдерживаемой учетной записи?

Регистрация в Power BI подразумевает использование корпоративной учетной записи. Регистрация в Power BI с помощью учетной записи Майкрософт не поддерживается.

### <a name="can-i-use-apis-to-create--manage-azure-capacities"></a>Можно ли использовать API для создания емкостей Azure и управления ими?

Да, существуют командлеты PowerShell и API-интерфейсы Azure Resource Manager (ARM), которые можно использовать для создания ресурсов PBIE и управления ими.

* REST API — https://docs.microsoft.com/rest/api/power-bi-embedded/
* Командлеты PowerShell — https://docs.microsoft.com/powershell/module/azurerm.powerbiembedded/

### <a name="what-is-the-pbi-embedded-dedicated-capacity-role-in-a-pbi-embedded-solution"></a>Что такое роль выделенной емкости PBI Embedded в решении PBI Embedded?

Чтобы [перенести решение в рабочую среду](embed-sample-for-customers.md#move-to-production), необходимо назначить содержимое Power BI (рабочую область приложения, которую вы используете в приложении) емкости Power BI Embedded (SKU А).

### <a name="what-are-the-azure-regions-pbi-embedded-is-available"></a>В каких регионах Azure доступен компонент PBI Embedded?

[PAM](https://ecosystemmanager.azurewebsites.net/home) (EcoManager) — см. раздел "Менеджер по наличию продуктов"

Доступные регионы (16 — те же регионы, что и для Power BI)

* США (6) — восточная часть США, восточная часть США 2, центрально-северная часть США, центрально-южная часть США, западная часть США, западная часть США 2
* Европа (2) — северная Европа, западная Европа
* Азиатско-Тихоокеанский регион (2) — юго-восточная Азия, восточная Азия
* Бразилия (1) — южная часть Бразилии
* Япония (1) — восточная Япония
* Австралия (1) — юго-восточная часть Австралии
* Индия (1) — западная Индия
* Канада (1) — центральная Канада
* Великобритания (1) — южная часть Соединенного Королевства

### <a name="what-is-the-authentication-model-for-power-bi-embedded"></a>Какая модель аутентификации используется в Power BI Embedded?

В Power BI Embedded по-прежнему используется Azure AD для аутентификации главного пользователя (назначенный пользователь с лицензией Power BI Pro) или [субъект-служба](embed-service-principal.md) при проверке подлинности приложения в Power BI.  

Проверку подлинности и авторизацию пользователей приложения реализует независимый поставщик ПО. Он может реализовать собственную модель проверки подлинности для своих приложений.

Если у вас уже есть клиент Azure AD, вы можете использовать существующий каталог или создать новый клиент Azure AD, чтобы обеспечить безопасность содержимого приложения.

Чтобы получить токен Azure AD, можно использовать одну из [библиотек проверки подлинности Azure Active Directory](https://docs.microsoft.com/azure/active-directory/develop/active-directory-authentication-libraries). Клиентские библиотеки доступны для различных платформ.

### <a name="my-application-already-uses-aad-for-user-authentication-how-can-we-use-this-identity-when-authenticating-to-power-bi-in-a-user-owns-data-scenario"></a>Мое приложение уже использует AAD для проверки подлинности пользователей. Как можно использовать это удостоверение при проверке подлинности в Power BI в сценарии "Данные, принадлежащие пользователю"?

Это стандартный поток OAuth от имени (<https://docs.microsoft.com/azure/active-directory/develop/web-api>). Приложение нужно настроить на запрос разрешений на использование службы Power BI (с обязательным областями). Получив маркер пользователя для приложения, просто вызовите для AcquireTokenAsync API ADAL с помощью маркера доступа и укажите URL-адрес ресурса Power BI как идентификатор ресурса. Как это сделать, см. в. следующем фрагменте кода:

```csharp
var context = new AD.AuthenticationContext(authorityUrl);
var userAssertion = new AD.UserAssertion(userAccessToken);
var clientAssertion = new AD.ClientAssertionCertificate(MyAppId, MyAppCertificate)
var authenticationResult = await context.AcquireTokenAsync(resourceId, clientAssertion, userAssertion);
```

### <a name="how-is-power-bi-embedded-different-from-other-azure-services"></a>Чем Power BI Embedded отличается от других служб Azure?

Чтобы приобрести Power BI Embedded в Azure, у независимого поставщика ПО или разработчика должна быть учетная запись Power BI. Регион развертывания Power BI Embedded определяет учетную запись Power BI. Управляйте ресурсом Power BI Embedded в Azure для следующих действий:

* увеличение или уменьшение масштаба;
* добавление администраторов емкости;
* приостановление и возобновление работы службы.

Используйте PowerBI.com, чтобы назначать рабочие области и отменять их назначение для емкости Power BI Embedded.

### <a name="what-deploy-regions-are-supported"></a>Какие регионы развертывания поддерживаются?

Восточная часть США 2, восточная Япония, Западная Европа, западная Индия, западная часть США, западная часть США 2, северная Европа, центрально-северная часть США, центральная Канада, юго-восточная Австралия, Юго-Восточная Азия, центрально-южная часть США, южная Бразилия и южная часть Соединенного Королевства.

### <a name="what-type-of-content-pack-data-can-be-embedded"></a>Какой тип данных пакета содержимого можно внедрять?

**Панели мониторинга** и **плитки**, сформированные из наборов данных в пакете содержимого, *невозможно* внедрить, а полученные аналогичным образом **отчеты** — *можно*.

### <a name="what-is-the-difference-between-using-rls-vs-javascript-filters"></a>Какая разница между использованием RLS и фильтров JavaScript?

Часто возникают путаницы в выборе RLS и фильтров JavaScript, так как один из методов — контроль того, что может увидеть конкретный пользователь, а другой — оптимизация представления пользователя.

При использовании RLS разработчик независимого поставщика программного обеспечения управляет фильтрацией данных в процессе создания модели и поколения токенов внедрения. Конечный пользователь видит только то, на что независимый поставщик программного обеспечения предоставляет доступ. В этом случае пользователь может выбрать меньшее, чем то, что фильтровалось, но не сможет обойти конфигурацию RLS и увидеть больше, чем разрешено.

При осуществляемой пользователем фильтрации (JavaScript) независимый поставщик может решить, что будет видеть конечный пользователь в исходном представлении, но он не может контролировать изменения, которые конечный пользователь может применить к самому представлению. Несмотря на то что фильтрация данных может произойти в серверной части, клиентский код JavaScript активирует ее, и поэтому конечный пользователь может изменить фильтрацию, что может быть небезопасно.

Для дополнительной информации см. раздел [Сравнение использования RLS и фильтров JavaScript](embedded-row-level-security.md#using-rls-vs-javascript-filters).

### <a name="how-do-i-manage-permissions-for-service-principals-with-power-bi"></a>Как управлять разрешениями для субъектов-служб в Power BI?

После активации [субъекта-службы](embed-service-principal.md) для использования с Power BI разрешения приложения в Active Directory перестают действовать. В дальнейшем управление разрешениями приложения осуществляется на портале администрирования Power BI.

Субъекты-службы наследуют разрешения для всех параметров клиента Power BI от своей группы безопасности. Чтобы дополнительно ограничить разрешения, создайте для субъектов-служб отдельную группу безопасности и добавьте ее в список "За исключением отдельных групп безопасности" для тех параметров Power BI, которые должны быть включены.

Это важно, когда вы добавляете субъект-службу в качестве **администратора** в новую рабочую область. Эту задачу можно выполнить с помощью [интерфейсов API](https://docs.microsoft.com/rest/api/power-bi/groups/addgroupuser) или службы Power BI.

### <a name="when-to-use-an-application-id-vs-a-service-principal-object-id"></a>Когда следует использовать идентификатор приложения, а когда — идентификатор объекта субъекта-службы?

**[Идентификатор приложения](embed-sample-for-customers.md#application-id)** используется для создания маркера доступа при передаче этого идентификатора для проверки подлинности.

При выполнении операций с субъектом-службой или внесении изменений в него, например добавлении субъекта-службы в качестве администратора в рабочую область, на него необходимо ссылаться по **[идентификатору объекта субъекта-службы](embed-service-principal.md#how-to-get-the-service-principal-object-id)**.

### <a name="can-you-manage-an-on-premises-data-gateway-with-service-principal"></a>Можно ли управлять локальным шлюзом данных с помощью субъекта-службы?

С помощью [субъекта-службы](embed-service-principal.md) нельзя управлять локальным шлюзом данных, как с помощью главной учетной записи.

Используя главную учетную запись, можно установить шлюз данных, добавить в него пользователей, подключиться к источникам данных и выполнять другие задачи администрирования.

С помощью субъекта-службы можно настроить [безопасность на уровне строк (RLS)](embedded-row-level-security.md#on-premises-data-gateway-with-service-principal-preview), используя в качестве источника данных активное подключение к локальным службам SQL Server Analysis Services (SSAS). Это позволит управлять пользователями и их доступом к данным в службах SSAS при интеграции с **Power BI Embedded** посредством субъекта-службы.

### <a name="can-you-sign-into-the-power-bi-service-with-service-principal"></a>Можно ли входить в службу Power BI с помощью субъекта-службы?

Нет, входить в службу Power BI с помощью субъекта-службы нельзя.

Кроме того, нельзя использовать содержимое во внешних приложениях (внедренных по модели SaaS). Для этого требуется создать токен внедрения.

### <a name="what-are-the-best-practices-to-improve-performance"></a>Рекомендации по повышению производительности

[Производительность Power BI Embedded](embedded-performance-best-practices.md)

## <a name="licensing"></a>Лицензирование

### <a name="how-do-i-purchase-power-bi-embedded"></a>Как приобрести Power BI Embedded?

Служба Power BI Embedded доступна в Azure.

### <a name="what-happens-if-i-already-purchased-power-bi-premium-and-now-i-want-some-of-the-benefits-of-power-bi-embedded-in-azure"></a>Что если решение Power BI Premium уже приобретено и я хочу воспользоваться некоторыми преимуществами Power BI Embedded в Azure?

Клиенты будут продолжать оплачивать все существующие покупки Power BI Premium до завершения срока текущего соглашения. По истечении срока клиенты смогут перенести покупки Power BI Premium, если будет такая необходимость на тот момент.

### <a name="do-i-still-have-to-buy-power-bi-premium-to-get-access-to-power-bi-embedded"></a>Требуется ли приобрести Power BI Premium, чтобы получить доступ к Power BI Embedded?

Нет. Power BI Embedded включает в себя емкость Azure, которая требуется для развертывания и распространения решений для клиентов.

### <a name="whats-the-purchase-commitment-for-power-bi-embedded"></a>Какие существуют обязательства по приобретению Power BI Embedded?

Пользователи могут изменять способ использования на почасовой основе. Для службы Power BI Embedded нет ежегодного или ежемесячного обязательства.

### <a name="how-does-the-usage-of-power-bi-embedded-show-up-on-my-bill"></a>Как плата за использование Power BI Embedded отражается в счете?

Плата за использование Power BI Embedded предусматривает прогнозируемую почасовую тарификацию с учетом типа развернутых узлов. Если ресурс активен, вам будет выставляться счет за него, даже если ресурс не используется. Чтобы прекратить выставление счетов, необходимо приостановить работу ресурса.

### <a name="who-needs-a-power-bi-pro-license-for-power-bi-embedded-and-why"></a>Кому требуется лицензия Power BI Pro для Power BI Embedded и почему?

Любому разработчику, который должен использовать REST API, нужна лицензия Power BI Pro или [субъект-служба](embed-service-principal.md). Любой аналитик, которому необходимо добавлять отчеты в рабочую область Power BI, может использовать лицензию Power BI Pro или субъект-службу. Администратор, который управляет клиентом Power BI и емкостью, должен иметь лицензию Power BI Pro.

Так как Power BI Embedded позволяет использовать портал Power BI для управления внедренным содержимым и его проверки, лицензия Power BI Pro требуется для проверки подлинности приложения на сайте PowerBI.com и получения доступа к отчетам в соответствующих репозиториях.

Однако для [создания или изменения внедренных отчетов](https://github.com/Microsoft/PowerBI-JavaScript/wiki/Create-Report-in-Embed-View) внутри собственного приложения конечному пользователю не требуется лицензия Pro, так как ему вообще необязательно быть пользователем Power BI.

### <a name="can-i-get-started-for-free"></a>Можно ли начать работу бесплатно?

Да, вы можете использовать [деньги на счете в Azure](https://azure.microsoft.com/free/) для Power BI Embedded.

### <a name="can-i-get-a-trial-experience-for-power-bi-embedded-in-azure"></a>Можно ли получить пробную версию Power BI Embedded в Azure?

Так как Power BI Embedded является частью Azure, вы можете приобрести эту службу за [200 $, полученных при регистрации в Azure](https://azure.microsoft.com/free/).

### <a name="is-power-bi-embedded-available-for-national-clouds-us-government-germany-china"></a>Доступна ли службы Power BI Embedded в национальных облаках (для государственных организаций США, Германии и Китая)?

Power BI Embedded также доступна в [национальных облаках](embed-sample-for-customers-national-clouds.md).

### <a name="is-power-bi-embedded-available-for-non-profits-and-educational"></a>Будет ли Power BI Embedded доступна для некоммерческих и образовательных организаций?

Некоммерческие и образовательные организации смогут приобрести подписку Azure. Для клиентов такой категории нет специальных цен в Azure.

## <a name="power-bi-workspace-collection"></a>Коллекция рабочих областей Power BI

### <a name="what-is-power-bi-workspace-collection"></a>Что такое коллекция рабочих областей Power BI?

**Коллекция рабочих областей Power BI** (**Power BI Embedded** версии 1) — это решение на основе ресурса Azure **Коллекция рабочих областей Power BI**. Это решение позволяет создавать приложения **Power BI Embedded** для предоставления клиентам содержимого Power BI, размещенного в решении **Коллекция рабочих областей Power BI** с помощью специальных интерфейсов API и ключей рабочей области для проверки подлинности приложения в Power BI.

### <a name="can-i-migrate-from-power-bi-workspace-collection-to-power-bi-embedded"></a>Можно ли перенести содержимое из коллекции рабочих областей Power BI в Power BI Embedded?

1. Средство миграции позволяет клонировать содержимое из **коллекции рабочих областей Power BI** в Power BI — https://docs.microsoft.com/power-bi/developer/migrate-from-powerbi-embedded#content-migration.

2. Для начала примените POC-приложение **Power BI Embedded**, которое использует содержимое Power BI.

3. Когда вы будете готовы перейти в рабочую среду, приобретите выделенную емкость **Power BI Embedded** и назначьте ей определенное содержимое (рабочую область) Power BI.

    > [!Note]
    > Вы можете продолжать работу с **коллекцией рабочих областей Power BI** параллельно с созданием решения **Power BI Embedded**. Когда вы будете полностью готовы, перенесите данные клиента в новое решение **Power BI Embedded** и прекратите использовать решение **Коллекция рабочих областей Power BI**.

Дополнительные сведения см. в статье [о переносе содержимого из коллекции рабочих областей Power BI в Power BI Embedded](https://docs.microsoft.com/power-bi/developer/migrate-from-powerbi-embedded).

### <a name="is-power-bi-workspace-collection-on-a-path-to-be-deprecated"></a>Правда ли, что коллекция рабочих областей Power BI скоро будет считаться нерекомендуемой?

Да, это так, но клиенты могут продолжать работу с решением **Коллекция рабочих областей Power BI**, пока оно не станет нерекомендуемым. Клиенты также могут создавать коллекции рабочих областей и приложения **Power BI Embedded**, использующие решения на основе **коллекции рабочих областей Power BI**.

Однако это также означает, что новые функции уже не добавляются в **коллекцию рабочих областей Power BI**, и мы рекомендуем всем пользователям запланировать миграцию решений на платформу **Power BI Embedded**.

### <a name="when-is-power-bi-workspace-collection-support-discontinued"></a>Когда будет прекращена поддержка коллекции рабочих областей Power BI?

Клиенты, которые используют решения на основе **коллекций рабочих областей Power BI**, могут продолжать работу с ними до конца июня 2018 года или до конца текущего соглашения на поддержку.

### <a name="in-what-regions-can-pbi-workspace-collection-be-created"></a>В каких регионах можно создать коллекцию рабочих областей Power BI?

Это решение доступно в следующих регионах: восточная часть США 2, восточная Япония, Западная Европа, западная Индия, западная часть США, северная Европа, центрально-северная часть США, центральная Канада, юго-восточная Австралия, Юго-Восточная Азия, центрально-южная часть США, южная Бразилия и южная часть Соединенного Королевства.

### <a name="why-should-i-migrate-from-pbi-workspace-collection-to-power-bi-embedded"></a>Зачем мне переносить содержимое из коллекции рабочих областей Power BI в Power BI Embedded?

В решение **Power BI Embedded** добавлены новые функции и возможности, которые недоступны в **коллекции рабочих областей Power BI**.

Вот лишь некоторые из них:

* Поддержка всех источников данных Power BI, а не только двух стандартных источников для **коллекции рабочих областей Power BI**. 
* Новые функции, такие как вопросы и ответы, обновление, закладки, внедрение информационных панелей и плиток, а также пользовательские меню поддерживаются только в решении **Power BI Embedded**.
* модель выставления счетов по емкости.

## <a name="embedding-setup-tool"></a>Средство настройки внедрения

### <a name="what-is-the-embedding-setup-tool"></a>Что такое средство настройки внедрения?

[Средство настройки внедрения](https://aka.ms/embedsetup) позволяет быстро приступить к работе и скачать образец приложения, чтобы начать внедрение в Power BI.

### <a name="which-solution-should-i-choose"></a>Какое решение выбрать?

* [Внедрение для клиентов](embedding.md#embedding-for-your-customers) позволяет внедрять панели мониторинга и отчеты для пользователей, у которых нет учетной записи Power BI. Запустите решение [Внедрение для клиентов](https://aka.ms/embedsetup/AppOwnsData).
* [Внедрение для организации](embedding.md#embedding-for-your-organization) позволяет расширить возможности службы Power BI. Запустите решение [Внедрение для организации](https://aka.ms/embedsetup/UserOwnsData).

### <a name="ive-downloaded-the-sample-app-which-solution-do-i-choose"></a>Образец приложения скачан. Какое решение выбрать?

Если вы работаете с решением **Внедрение для клиентов**, сохраните и распакуйте файл *PowerBI-Developer-Samples.zip*. Затем откройте папку *PowerBI-Developer-Samples-master\App Owns Data* и запустите файл *PowerBIEmbedded_AppOwnsData.sln*.

Если вы работаете с решением **Внедрение для организации**, сохраните и распакуйте файл *PowerBI-Developer-Samples.zip*. Затем откройте папку *PowerBI-Developer-Samples-master\User Owns Data\integrate-report-web-app* и запустите файл *pbi-saas-embed-report.sln*.

### <a name="how-can-i-edit-my-registered-application"></a>Как изменить зарегистрированное приложение?

Узнать, как изменять зарегистрированные в Azure AD приложения, можно в [руководстве по обновлению приложения в Azure Active Directory](https://docs.microsoft.com/azure/active-directory/develop/quickstart-v1-update-azure-ad-app).

### <a name="how-can-i-edit-my-power-bi-user-profile-or-data"></a>Как изменить профиль пользователя или данные Power BI?

Узнать, как изменить данные Power BI, можно [здесь](https://docs.microsoft.com/power-bi/service-basic-concepts).

Дополнительные сведения: [Устранение неполадок внедренного приложения](embedded-troubleshoot.md).

Появились дополнительные вопросы? [Ответы на них см. в сообществе Power BI.](http://community.powerbi.com/)