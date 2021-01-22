---
title: Виправлення неполадок користувача
ms.author: v-smandalika
author: v-smandalika
manager: dansimp
ms.date: 01/15/2021
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Priority
ms.collection: Adm_O365
ms.custom:
- "7813"
- "9004358"
ms.openlocfilehash: d9964e50bdea0c41ac14ab3783b579034b5f2c8c
ms.sourcegitcommit: 6d02eb533fd74199af6b20f714b3720991da2c4a
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 01/18/2021
ms.locfileid: "49901342"
---
# <a name="announcements"></a>Оголошення

Дотримуйтеся вказівок Google, щоб перевірити, чи впливають ваші програми на тестування. Рекомендації Google доступні в програмі https://docs.microsoft.com/azure/active-directory/external-identities/google-federation#deprecation-of-webview-sign-in-support .

Переконайтеся, що ви використовуєте веб-перегляд системи або системний браузер під час входу користувачів зі службою споживчого облікового запису Google. Щоб отримати докладніші відомості, перегляньте [проблеми з входом у програму лише за допомогою браузера Chrome](https://docs.microsoft.com/office365/troubleshoot/miscellaneous/chrome-behavior-affects-applications).


**Не вдається створити нового користувача в папці "мій Лазурний РЕКЛАМНИЙ"**

Щоб усунути проблему не в стані створення нового користувача в Azure AD, виконайте наведені нижче дії.

1. Переконайтеся, що ви надали дозвіл на створення нового стандартного користувача. Створити новий стандартний користувач може лише Глобальний адміністратор або роль адміністратора користувача в Лазурому Active Directory (AD). Якщо ви не в одній із цих ролей, попросіть адміністратора додати вас до однієї з цих ролей або створити новий обліковий запис користувача.
2. Переконайтеся, що ім'я користувача перебуває в домені, який перевіряється в Лазурному ОГОЛОШЕННІ. Якщо у вас немає жодного перевіреного настроюваного імені домену в Лазурному ОГОЛОШЕННІ, ви можете скористатися вашим початковим доменом Azure AD, що завершується *. onmicrosoft.com.
3. Переконайтеся, що ім'я користувача перебуває в домені, який не є федеративним для Azure AD від локального РЕКЛАМНОГО користувача. Користувачі не можуть додавати до хмари з іменами доменів, які є федеративними в локальних.
4. Переконайтеся, що інший користувач або контакт уже має ім'я користувача, яке потрібно призначити новому користувачу. Імена користувачів мають бути унікальними в межах Лазурого AD.
5. Переглядайте [блакитні ролі та адміністратори](https://ms.portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/RolesAndAdministrators) в лазурому оголошенні.
6. Перегляньте [імена доменів](https://ms.portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Domains) для свого AZURE AD.
7. Перегляньте [журнали аудиту](https://ms.portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Audit) , щоб переглянути докладні відомості про нещодавно створений або видалений користувач, який виконав дію та коли.
8. Щоб отримати докладні відомості про додавання нових користувачів, перегляньте статтю [використання порталу "Лазурний" для створення нового користувача в Лазур](https://docs.microsoft.com/azure/active-directory/fundamentals/add-users-azure-active-directory) .
9. Щоб отримати докладніші відомості про дозволи на роль адміністратора в Azure AD, ознайомтеся зі своїми [ролями адміністрування AZURE AD](https://docs.microsoft.com/azure/active-directory/roles/permissions-reference).
10. Щоб отримати докладні відомості про створення користувача за допомогою служби Azure AD PowerShell, ознайомтеся [з веб-програмою AZURE AD PowerShell, щоб створити новий користувач](https://docs.microsoft.com/powershell/module/azuread/new-azureaduser).

**Проблема з самообслуговуванням Реєстрація**

Щоб виправити неполадки, які стосуються самостійної реєстрації, виконайте наведені нижче дії.

1. Щоб використовувати реєстрацію в програмах самообслуговування, спочатку активуйте службу самообслуговування для свого клієнта. 
2. Щоб активувати програму, щоб підтримати самообслуговування, додайте його до свого потоку користувачів. Наступного разу, коли ви перейдете на сторінку входу для цієї програми, відобразиться опція **_немає облікового запису? Створіть один!_* _. Після цього розпочнеться процес реєстрації самостійної служби.
3. Щоб отримати відомості про те, як використовувати самослужбу, щоб заповнити організацію в лазурому, перегляньте статтю [Self-Service Sign Up For AZURE AD](https://docs.microsoft.com/azure/active-directory/enterprise-users/directory-self-service-signup).
4. Якщо ви пов'язуєте потік користувача з одним або кількома програмами, користувачі, які відвідуватимуть цю програму, зможуть зареєструватися та отримати гостьовий обліковий запис за допомогою параметрів, настроєних у потоці користувача. Щоб отримати докладні відомості про реєстрацію та отримання гостьового облікового запису, користувачі можуть бачити, як можна [зареєструватися для користувачів із самообслуговуванням](https://docs.microsoft.com/azure/active-directory/external-identities/self-service-sign-up-user-flow).

_ *Проблема з запрошенням зовнішнього користувача**

Щоб усунути проблеми, пов'язані з запрошенням зовнішнього користувача, виконайте такі дії:

Переконайтеся, що ви надсилаєте запрошення користувача на адресу електронної пошти, яка відповідає назві, у якому користувач підписує з ним. Якщо надіслати запрошення на адресу електронної пошти проксі-сервера користувача, користувач не зможе його викупити. Для отримання додаткових [відомостей див.](https://docs.microsoft.com/azure/active-directory/external-identities/)

**Не вдається призначити ліцензії користувачу**

Щоб виправити неполадки, які стосуються призначення ліцензій для користувача, виконайте наведені нижче дії.

1. Щоб керувати ліцензіями користувачів, переконайтеся, що ви використовуєте обліковий запис, використовуючи один із обов'язкових ролей адміністратора: Глобальний адміністратор, адміністратор ліцензії або адміністратор користувачів. Ви можете перевірити роль користувача на вкладці " **роль каталогу** " на клинку користувача.
2. Якщо ви використовуєте непотрібний портал та призначення ліцензії, клацніть сповіщення у верхньому правому куті. Це відкриває лезо з відомостями про те, що пішло не так. У більшості випадків це достатньо для того, щоб розібратися та вирішити цю проблему.
3. Перш ніж ліцензію можна призначити користувачу, переконайтеся, що властивість розташування для **використання** настроєно для користувача. Переконайтеся, що користувач має цей набір властивостей, переглянувши вкладку **профіль** на клинку користувача.
4. Переконайтеся, що для продукту, який ви намагаєтеся призначити, достатньо доступних ліцензій. Ви можете побачити кількість доступних ліцензій на порталі Azure, у "Лазурний", " [>" ліцензії "> всі продукти](https://ms.portal.azure.com/#blade/Microsoft_AAD_IAM/LicensesMenuBlade/Products)".
5. Можливо, у користувача уже є інша ліцензія, чиї служби конфліктують з новими ліцензіями, які ви намагаєтеся призначити. Наприклад, якщо користувач має службу Exchange Online (план 1), ви не зможете призначити ліцензію за допомогою служби Exchange Online (план 2). Вимкніть одну з служб, щоб дозволити нову призначення ліцензії. Якщо ви використовуєте командлети "Лазурний портал" або "PowerShell", на сторінці " **відомості про проблему** " перелічено певні служби, які призводять до конфлікту.
6. Якщо ви намагаєтеся видалити ліцензію, а це не вдається, можливо, користувач може мати інші ліцензії з службами, які залежать від служб, які ви намагаєтеся видалити. Якщо використовуються командлети "Лазурний портал" або "PowerShell", у повідомленні про помилку буде наведено певні служби, які мають залежності.
7. Якщо ви хочете дізнатися, чому для користувача було додано або видалено ліцензію (наприклад, хто ще в організації може внести зміни), перевірте журнали аудиту. Установлення фільтра для **дій ліцензії** для відображення всіх змін, включно з "актором", що їх виконав.
8. Якщо ви користуєтеся службою Exchange Online, деякі користувачі в клієнті можуть неправильно настроєні за допомогою тієї самої адреси проксі-сервера. У таких випадках можна побачити загальні повідомлення про помилку, коли не вдається виконати операцію ліцензії. У [цій статті](https://docs.microsoft.com/exchange/troubleshoot/administration/proxy-address-being-used) наведено докладні відомості про цю проблему, зокрема відомості про [те, як підключитися до служби Exchange Online за допомогою віддаленого PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell). Щоб визначити, які користувачі в клієнті містять таку саму адресу проксі-сервера, виконайте цей командлет Exchange Online:

Запустити

Get-Recipient | де {$ _. EmailAddresses-Match <user principal name> } | Ім'я для fL, тип Rereienttype, EmailAddresses




