---
title: Помилки застосунку
ms.author: v-aiyengar
author: AshaIyengar21
manager: dansimp
ms.date: 01/25/2021
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
ms.collection: Adm_O365
ms.custom:
- "9004342"
- "7841"
ms.openlocfilehash: 2ef90b54ce222a06740e05891fabe87b6565cb14
ms.sourcegitcommit: ba3118b7ad5e02756d0e5c2113245090f54370af
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 01/25/2021
ms.locfileid: "49984654"
---
# <a name="application-errors"></a>Помилки застосунку

Шукаєте відомості про **коди помилок Aadsts** , які повертаються в службі маркерів безпеки «Лазурний» ("AZURE AD")? Ознайомтеся з [автентифікацією Azure AD автентифікації та кодами помилок авторизації](https://docs.microsoft.com/azure/active-directory/develop/reference-aadsts-error-codes) , щоб знаходити описи помилок AADSTS, виправлення та деякі запропоновані способи вирішення.

Помилки авторизації можуть бути результатом кількох різних проблем, більшість з яких створює помилку 401 або 403. Наприклад, наведені нижче дії можуть призвести до помилок авторизації:

- Неправильні [потоки на придбання маркерів доступу](https://docs.microsoft.com/azure/active-directory/develop/reference-aadsts-error-codes) 
- Погано налаштовані [області дозволів](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-scopes) 
- Відсутність [згоди](https://docs.microsoft.com/azure/active-directory/develop/active-directory-devhowto-multi-tenant-overview#understanding-user-and-admin-consent)

Щоб вирішити поширені помилки авторизації, виконайте наведені нижче дії, які найбільше відповідають отриманій помилці. Може застосовуватися кілька.

**401 несанкціоноване повідомлення про помилку: чи є ваш маркер дійсним?**

Переконайтеся, що ваша програма представляє припустимий маркер доступу до Microsoft Graph як частину запиту. Ця помилка часто свідчить про те, що маркер доступу може бути відсутнє в заголовку запиту автентифікації HTTP або що цей маркер недійсний або минув. Ми настійно рекомендуємо використовувати [бібліотеку автентифікації Microsoft (MSAL)](https://docs.microsoft.com/azure/active-directory/develop/msal-overview) для придбання маркерів Access. Крім того, ця помилка може виникати, якщо ви намагаєтеся використовувати маркер, наданий для особистого облікового запису Microsoft, щоб отримати доступ до API, який підтримує тільки робочі або шкільні облікові записи (організаційні облікові записи).

**403 Заборонене повідомлення про помилку: ви вибрали потрібний набір дозволів?**

Переконайтеся, що ви запросили відповідного набору дозволів на основі API Microsoft Graph для програми. Рекомендовані найменше привілейовані дозволи надаються в усіх розділах посилань на програмний засіб Microsoft Graph API. Крім того, ці дозволи мають бути надані користувачу або адміністратору. Надання дозволів зазвичай відбувається через сторінку згоди або шляхом надання дозволів на відповідний рахунок для реєстрації програми Azure Portal. У розділі " **настройки** " для програми виберіть **потрібні дозволи**, а потім натисніть кнопку **надати дозволи**.

- [Дозволи Microsoft Graph](https://docs.microsoft.com/graph/permissions-reference) 
- [Розуміння дозволів і згоди на Azure AD](https://docs.microsoft.com/azure/active-directory/develop/v2-permissions-and-consent) 

**403 Заборонене повідомлення про помилку: чи має ваша програма придбати маркер, щоб відповідати вибраним дозволами?**

Переконайтеся, що запитаний тип дозволів або надано відповідає типу маркера доступу, який набуває програма. Можливо, вам потрібно буде запитувати та надати дозволи на використання, але використовувати делеговані коди потоку інтерактивних кодів, а не маркери потоку клієнтських облікових даних, а також запити та надання делегованих дозволів, але за допомогою маркерів передавання облікових даних клієнта замість делегованих маркерів потоків коду.

- [Отримання доступу від імені користувачів і делегованих дозволів](https://docs.microsoft.com/graph/auth_v2_user) 
- [Azure AD v 2.0-OAuth 2,0 код авторизації](https://docs.microsoft.com/azure/active-directory/develop/v2-oauth2-auth-code-flow) 
- [Отримання доступу без користувача (служби демона) і дозволів на використання](https://docs.microsoft.com/graph/auth_v2_service) 
- [Azure AD v 2.0-OAuth 2,0 клієнтських облікових даних](https://docs.microsoft.com/azure/active-directory/develop/v2-oauth2-client-creds-grant-flow) 

**403 Заборонене повідомлення про помилку: скидання пароля**

Наразі немає дозволів на надання дозволу на використання програми, які дають змогу скинути паролі користувачів. Ці API підтримуються лише за допомогою інтерактивного делегованого коду, який має підписаний адміністратор.

- [Дозволи Microsoft Graph](https://docs.microsoft.com/graph/permissions-reference)

**403 Заборонене: чи користувач має доступ, і вони мають ліцензію?**

Для делегованих потоків коду, Microsoft Graph оцінює, чи дозволено запит на основі дозволів, наданих програмі, а також дозволів, які користувач, який увійшов у систему. Зазвичай ця помилка вказує на те, що користувач не достатньо Привілейований, щоб виконати запит або користувач не ліцензовано для доступу до даних. Лише користувачі, які мають потрібні дозволи або ліцензії, можуть зробити запит успішно.

**403 Заборонене: ви вибрали правильне API ресурсів?**

Служби API, як-от Microsoft Graph, перевірте, чи відповідає він (аудиторія) в маркер отриманого доступу, значення, яке він очікує для себе, і якщо ні, це призводить до помилки 403. Поширена помилка, що виникає в результаті цієї помилки, намагається використовувати маркер, придбаний для роботи з API Azure AD Graph, API для Outlook або SharePoint або OneDrive, щоб викликати Microsoft Graph (або навпаки). Переконайтеся, що ресурс (або область) – це придбання маркера для відповідності API, у якому програма телефонує.

**400 неправильний запит або 403 Заборонене: чи відповідає користувач політиці умовного доступу своєї організації (CA)?**

Використовуючи політику CA організації, користувач, який має доступ до ресурсів Microsoft Graph за допомогою програми, може бути оскаржено, щоб отримати додаткові відомості, відсутні в маркер доступу, який ви отримали спочатку. У цьому випадку програма отримує 400 з помилкою *interaction_required* під час придбання маркера доступу або 403 з *insufficient_claims* помилка під час виклику Microsoft Graph. В обох випадках відповідь на повідомлення про помилку містить додаткові відомості, які можуть бути представлені в кінцевій точці авторизації, щоб кинути виклик користувачу для додаткової інформації (наприклад, багатофакторної автентифікації або реєстрації пристрою).

- [Оброблення викликів умовного доступу за допомогою MSAL ](https://docs.microsoft.com/azure/active-directory/develop/msal-handling-exceptions#conditional-access-and-claims-challenges)
- [Посібник розробника для умовного доступу до служби "Azure Active Directory"](https://docs.microsoft.com/azure/active-directory/develop/conditional-access-dev-guide)
