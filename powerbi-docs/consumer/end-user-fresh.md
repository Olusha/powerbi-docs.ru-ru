---
title: Как Power BI гарантирует, что ваше содержимое находится в актуальном состоянии
description: Узнайте, как Power BI гарантирует, что вы работаете с последней версией данных, отчетов, панели мониторинга и приложения.
author: mihart
manager: kvivek
ms.service: powerbi
ms.custom: ''
ms.subservice: powerbi-service
ms.topic: overview
ms.date: 02/08/2019
ms.author: mihart
LocalizationGroup: Get started
ms.openlocfilehash: 5ab305777306d8ee12edf2756404efeffa52e44b
ms.sourcegitcommit: 88ac51106ec7d0ead8c2a1550a11afae0d502bb9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2019
ms.locfileid: "56086662"
---
# <a name="your-content-is-up-to-date"></a>Содержимое актуально
Как *потребитель* вы можете взаимодействовать с содержимым, которое создается *разработчиками* и предоставляется вам при помощи общего доступа. Может возникнуть вопрос, актуально ли такое содержимое, или может потребоваться узнать, когда последний раз оно обновлялось. Знание того, что вы работаете с самыми новыми версиями содержимого, придает уверенность.  
 
![Панель мониторинга Power BI](media/end-user-consumer/power-bi-service.png)


Часто для принятия правильных решений крайне важно располагать актуальными данными. Что можно сделать, чтобы убедиться, что вы используете последние материалы? Во многих случаях вам вообще не нужно ничего делать. Приложения, которыми поделились с вами, автоматически обновляются по расписанию, заданному разработчиком. То же касается панелей мониторинга и отчетов, которые вам были предоставлены: разработчик либо вручную, либо с помощью расписания автоматического обновления гарантирует, что содержимое будет актуальным.  

Если у вас есть вопросы относительно актуальности данных, обратитесь к разработчику.

## <a name="how-to-locate-the-name-of-the-designer"></a>Как найти имя разработчика

### <a name="apps"></a>Приложения

На экране приложения показано имя разработчика, а также дата создания приложения.  

1. В левой области навигации выберите **Приложения**.

    ![Панель навигации слева](media/end-user-fresh/power-bi-nav-apps.png)

    Для каждого приложения вы увидите имя и дату создания. 

2. Наведите на приложение, чтобы также вывести имя разработчика. 

    ![Два приложения, одно выбрано](media/end-user-fresh/power-bi-app.png)


### <a name="shared-with-me"></a>Мне предоставлен доступ
Экран **Мне предоставлен доступ** показывает имя владельца содержимого, а также даты, когда содержимое было вам предоставлено.

![Снимок экрана "Мне предоставлен доступ": дата изменения и владелец](media/end-user-fresh/power-bi-shared-new.png) 


## <a name="how-to-look-up-the-last-refresh-date"></a>Как найти дату последнего обновления
Вы можете найти дату последнего обновления для большей части содержимого. 

### <a name="dashboard-tiles"></a>Плитки панели мониторинга
Для плиток панели мониторинга откройте плитку в режиме фокусировки, чтобы увидеть метку времени последнего обновления.

1. На плитке панели мониторинга щелкните многоточие (…) и выберите пункт **Открыть в режиме фокусировки**.

    ![Меню, которое отображается после выбора многоточия](media/end-user-fresh/power-bi-focus.png)

2. В правом верхнем углу появится дата последнего обновления. Если вы не видите его, разверните окно браузера, чтобы сделать его шире. 

    ![Ширина браузера, показывающего последнее обновление](media/end-user-fresh/power-bi-last-refresh2.png)

### <a name="from-dashboards-and-reports"></a>Через панели мониторинга и отчеты
Другой способ поиска даты последнего обновления — с помощью **просмотра связанных элементов**.  **Просмотр связанных элементов** доступен в верхнем меню Power BI.

![Выберите "Просмотр связанных элементов" в меню](media/end-user-fresh/power-bi-view-related.png)

В панели **Связанное содержимое** отображаются сведения о времени последнего обновления для базового набора данных панели мониторинга или отчета.

![Панель мониторинга Power BI](media/end-user-fresh/power-bi-last-refresh.png)

## <a name="what-happens-if-an-app-is-deleted-by-the-designer"></a>Что произойдет, если разработчик удалит приложение

Если разработчик удаляет приложения, панели мониторинга и отчеты, связанные с этим приложением, также автоматически удаляются из рабочей области Power BI. Они станут недоступны, и приложение перестанет отображаться в области навигации.


## <a name="subscribe-to-see-changes"></a>Подпишитесь на изменения
Другой способ оставаться в курсе — подписаться на отчет или панель мониторинга. Вместо того, чтобы войти и открыть отчет или панель мониторинга, вы указываете Power BI отправлять моментальные снимки по заданному расписанию.  Дополнительные сведения см. в разделе [Подписка на панели мониторинга и отчеты](end-user-subscribe.md).

## <a name="set-data-alerts"></a>Настройка оповещений о данных
Хотите получать уведомления при изменении данных, вышедших за предельное значение? [Создайте предупреждение данных](end-user-alerts.md).  Оставаться в курсе будет легко с помощью предупреждений данных. Используя их, вы указываете Power BI отправить вам сообщение электронной почты, если значение в отчете превышает определенный порог.  Например, если объем запасов на складе стал ниже 25 единиц или продажи превышают цели.  

## <a name="next-steps"></a>Дальнейшие действия
[Создание предупреждения данных](end-user-alerts.md)    
[Подписка на панели мониторинга и отчеты](end-user-subscribe.md)    
[Просмотр связанного содержимого](end-user-related.md)    