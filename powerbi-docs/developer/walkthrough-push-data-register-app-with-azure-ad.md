---
title: Регистрация приложения в Azure AD
description: Пошаговое руководство — принудительная отправка данных в набор данных — регистрация приложения в Azure AD
author: markingmyname
ms.author: maghan
manager: kfile
ms.reviewer: madia
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: conceptual
ms.date: 02/05/2019
ms.openlocfilehash: a3154a7b74d196f3c0aa2969e7c25bf56000a662
ms.sourcegitcommit: 0abcbc7898463adfa6e50b348747256c4b94e360
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2019
ms.locfileid: "55762037"
---
# <a name="step-1-register-an-app-with-azure-ad"></a>Шаг 1. Регистрация приложения в Azure AD

Эта статья является частью пошагового руководства по [принудительной отправке данных в набор данных](walkthrough-push-data.md).

Первым шагом процесса принудительной отправки данных в набор данных Power BI является регистрация приложения в Azure AD. Эта процедура необходима для последующего получения **идентификатора клиента** , определяющего ваше приложение в Azure AD. Без **идентификатора клиента**Azure AD не сможет проверить подлинность приложения.

> **ПРИМЕЧАНИЕ**. Прежде чем зарегистрировать приложение для Power BI, вам нужно [зарегистрироваться в Power BI](create-an-azure-active-directory-tenant.md).

Ниже приведены действия по регистрации приложения в Azure AD.

## <a name="register-an-app-in-azure-ad"></a>Регистрация приложения в Azure AD

1. Перейдите по адресу dev.powerbi.com/apps.
2. Выберите команду **Войти с использованием существующей учетной записи**и войдите в учетную запись Power BI.
3. В поле **Имя приложения** введите имя (например, "Пример приложения по отправке данных").
4. В поле **Тип приложения**выберите **Собственное приложение**.
5. В поле **URL-адрес перенаправления** укажите URL-адрес, например **https://login.live.com/oauth20_desktop.srf**. В случае **собственного клиентского приложения**URI перенаправления позволяет **Azure AD** получить дополнительную информацию о конкретном приложении, для которого будет выполнена проверка подлинности. Стандартным URI для клиентского приложения является https://login.live.com/oauth20_desktop.srf.
6. Для параметра **Choose APIs to access** (Выбор API для доступа) выберите значение **Read and Write All Datasets** (Чтение и запись всех наборов данных). Перечень всех разрешений для приложений Power BI см. в статье [Разрешения Power BI](power-bi-permissions.md).
7. Щелкните **Зарегистрировать приложение**и сохраните созданный **идентификатор клиента** . **Идентификатор клиента** определяет приложение в Azure AD.

Страница **Регистрация приложения Power BI** должна выглядеть следующим образом.

![Регистрация приложения](media/walkthrough-push-data-register-app-with-azure-ad/powerbi-developer-sample-register-app.png)

Следующим шагом является получение [токена доступа для проверки подлинности](walkthrough-push-data-get-token.md).

[Дальнейшие действия >](walkthrough-push-data-get-token.md)

## <a name="next-steps"></a>Дальнейшие действия

[Регистрация бесплатной учетной записи Power BI с пользовательским клиентом каталога Azure Active Directory](create-an-azure-active-directory-tenant.md)  
[Получение токена доступа для проверки подлинности](walkthrough-push-data-get-token.md)  
[Пошаговое руководство. Принудительная отправка данных в набор данных](walkthrough-push-data.md)  
[Регистрация приложения для внедрения содержимого Power BI](register-app.md)  
[Обзор интерфейса REST API Power BI](overview-of-power-bi-rest-api.md)  

Появились дополнительные вопросы? [Попробуйте задать вопрос в сообществе Power BI.](http://community.powerbi.com/)