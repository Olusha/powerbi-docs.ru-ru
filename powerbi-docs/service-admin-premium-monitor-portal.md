---
title: Мониторинг емкостей Power BI Premium с помощью портала администрирования
description: Используйте портал администрирования Power BI для мониторинга емкостей Premium.
author: minewiskan
ms.author: owend
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: conceptual
ms.date: 02/05/2019
LocalizationGroup: Premium
ms.openlocfilehash: 59097c07719e4bb8db188e8a86db377076aea7a9
ms.sourcegitcommit: 54d44deb6e03e518ad6378656c769b06f2a0b6dc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/07/2019
ms.locfileid: "55794118"
---
# <a name="monitor-capacities-in-the-admin-portal"></a>Мониторинг емкостей на портале администрирования

В этой статье описывается, как быстро получить представление об эффективности использования емкости в области "Параметры емкости" на портале администрирования.  Для получения наиболее полных метрик емкости лучше использовать приложение [Power BI Premium Capacity Metrics](service-admin-premium-monitor-capacity.md).

## <a name="capacity-metrics"></a>Метрики емкости

В области **Параметры емкости** на портале администрирования имеется четыре датчика, которые указывают нагрузку и ресурсы, использованные вашей емкостью за последние семь дней. Эти четыре элемента работают в почасовом временном окне, что указывает, сколько часов за последние семь дней соответствующая метрика была выше 80 %. Эта метрика указывает на потенциальное снижение производительности для пользователей.

![Использование в течение 7 дней](media/service-admin-premium-monitor-capacity/usage-in-days.png)

| **Метрика** | **Описание** |
| --- | --- |
| ЦП |Число раз, когда загрузка ЦП превысила 80 %. |
| Пробуксовка памяти |Нехватка памяти в ядрах серверной части. В частности, это метрика показывает, сколько раз наборы данных вытесняются из памяти из-за нехватки памяти в результате использования нескольких наборов данных. |
| Использование памяти |Средний уровень использования памяти в гигабайтах (ГБ). |
| Прямых запросов в секунду | Число раз, когда количество прямых запросов и активных подключений превысило 80 % от максимального. <br>  Общее количество запросов DirectQuery и активных запросов на подключение в секунду ограничено. Ограничения составляют до 30 запросов в секунду для P1, 60 запросов в секунду для P2 и 120 запросов в секунду для P3.  При учете указанного выше ограничения число прямых запросов и активных запросов на подключение складывается. Например, при наличии 15 прямых запросов и 15 запросов на динамическое подключение в секунду будет достигнут лимит регулирования.<br> Это в равной степени относится как к локальным, так и к облачным подключениям. |
|  |  |

Метрики отражают использование за последнюю неделю.  Чтобы изучить метрики более подробно, можно щелкнуть одну из плиток сводки.  В результате открываются подробные диаграммы для каждой из метрик, связанных с емкостью Premium. На следующей диаграмме показаны подробные метрики ЦП.

![Подробная диаграмма по загрузке ЦП](media/service-admin-premium-monitor-capacity/premium-usage-detailed-chart-cpu.png)

На диаграммах представлены сводные данные за последнюю неделю, которые обновляются каждый час. Это позволяет определить, когда произошли те или иные события, связанные с производительностью емкости Premium.

Базовые данные любой из метрик можно также экспортировать в CSV-файл.  Он будет содержать подробные сведения за каждый день последней недели с трехминутным интервалом.

## <a name="next-steps"></a>Дальнейшие действия

Теперь, когда вы понимаете, как выполнять мониторинг емкостей Power BI Premium, узнайте больше об их оптимизации.

> [!div class="nextstepaction"]
> [Использование и оптимизация ресурсов емкости Power BI Premium](service-premium-understand-how-it-works.md)
