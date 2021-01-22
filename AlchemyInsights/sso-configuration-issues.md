---
title: Проблеми з конфігурацією єдиного входу
ms.author: v-smandalika
author: v-smandalika
manager: dansimp
ms.date: 01/17/2021
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Priority
ms.collection: Adm_O365
ms.custom:
- "7760"
- "9004346"
ms.openlocfilehash: 5ab56ec1eda10ea059e600e8933ce85bb143b76e
ms.sourcegitcommit: 6d02eb533fd74199af6b20f714b3720991da2c4a
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 01/18/2021
ms.locfileid: "49901345"
---
# <a name="sso-configuration-issues"></a>Проблеми з конфігурацією єдиного входу

1. Виконайте [QuickStart: Настройте властивості для посібника із програми,](https://docs.microsoft.com/azure/active-directory/manage-apps/add-application-portal-configure) щоб настроїти програму.
2. Залежно від вибраного [параметра "єдиний вхід](https://docs.microsoft.com/azure/active-directory/manage-apps/sso-options) ", дотримуйтеся відповідних вказівок нижче: a. Щоб настроїти **локальну програму** на **основі ЄДИНОГО входу (SSO)**, у програмі "єдиний вхід" можна переглянути [Локальні програми для локальних програм із проксі-сервером](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy-configure-single-sign-on-on-premises-apps).
    b. Щоб настроїти **хмарну програму** для **єдиного входу на основі пароля**, перегляньте статтю [настроїти єдиний вхід у пароль](https://docs.microsoft.com/azure/active-directory/manage-apps/configure-password-single-sign-on-non-gallery-applications).
    c. Щоб настроїти **локальну програму** для єдиного входу за **допомогою проксі-сервера програми**, перегляньте статтю " [склепіння паролів" для єдиного входу з проксі-сервером застосунку](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy-configure-single-sign-on-password-vaulting).
3. **Виправлення неполадок із проксі-сервером програми**: ми радимо почати роботу з відповідними питаннями, щоб визначити, чи правильно настроєно сполучні лінії проксі-сервера програми [налагодження](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy-debug-connectors) . Якщо ви все ще не змогли підключитися до програми, виконайте вказівки з виправлення неполадок у [вирішенні проблем програми налагодження проксі-](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy-debug-apps)застосунку. Ви можете [визначити проблеми з CORORS](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy-understand-cors-issues#understand-and-identify-cors-issues) , виконавши наведені нижче дії з налагодження браузера: a. Запустіть браузер і перейдіть до веб-програми.
    b. Натисніть клавішу **F12** , щоб відкрити консоль налагодження.
    c. Виконайте спроби відтворити транзакцію та переглянути Консольне повідомлення. Під час порушення функції "Джерело" створюється помилка в консолі.
    d. Деякі проблеми із входом не можна усунути, наприклад термін дії маркера доступу, коли програма переспрямовує до login.microsoftonline.com для автентифікації. У результаті закінчення терміну дії маркера доступу в полі "виклик" не вдасться виконати виклики. Спосіб вирішення цього сценарію – подовжити термін дії маркера доступу, щоб запобігти його появі під час сеансу користувача. Щоб отримати докладні відомості про те, як це зробити, ознайомтеся [з Настроювана маркером користувача в платформі Microsoft Identity](https://docs.microsoft.com/azure/active-directory/develop/active-directory-configurable-token-lifetimes).
4. **Виправлення неполадок** із службою єдиного входу в SAML: ми радимо перевіряти проблеми, які потрібно виконати, щоб знайти вирішення проблем, на [основі яких настроєно єдиний вхід](https://docs.microsoft.com/azure/active-directory/manage-apps/application-sign-in-problem-federated-sso-gallery) .
5. **Виправлення помилок на основі паролів**: ми рекомендуємо перевіряти [Виправлення неполадок на основі єдиного входу в "Лазурний](https://docs.microsoft.com/azure/active-directory/manage-apps/troubleshoot-password-based-sso) ", щоб знайти вирішення проблем, з якими ви найчастіше стикаємося.
6. **Помилка конфігурації**: щоб виправити помилки конфігурації, радимо перевірити такі статті: a. [Проблеми з входом на веб-програми "єдиний вхід на основі" для входу](https://docs.microsoft.com/azure/active-directory/manage-apps/application-sign-in-problem-federated-sso-gallery) в службу "b". [Облікові дані заповнюються, але розширення не надсилають їх на](https://docs.microsoft.com/azure/active-directory/manage-apps/troubleshoot-password-based-sso#credentials-are-filled-in-but-the-extension-does-not-submit-them) c. [Облікові дані заповнюються та надсилаються, але ця сторінка вказує на те, що облікові дані неправильні](https://docs.microsoft.com/azure/active-directory/manage-apps/troubleshoot-password-based-sso) d. [На сторінці програми відображається повідомлення про помилку після того, як користувач підписує](https://docs.microsoft.com/azure/active-directory/manage-apps/application-sign-in-problem-application-error)
7. У **мене виникли проблеми з підключенням безшовного ЄДИНОГО входу в Локальні програми**: щоб вирішити проблеми, пов'язані з інтеграцією БЕЗШОВНОГО входу в Локальні програми, радимо перевірити такі статті: a. [Настроювання компонента "єдиний вхід у програму" для проксі-сервера програми](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy-config-sso-how-to) b. " [Єдиний вхід" для локальних програм із проксі-застосунком програми](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy-configure-single-sign-on-on-premises-apps) c. [Розуміння та вирішення проблем із проксі-сервером служби "Azure Active Directory](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy-understand-cors-issues#solutions-for-application-proxy-cors-issues) " d. [Усунення несправностей у конфігурації делегування для протоколу Kerberos для проксі-сервера програми](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy-back-end-kerberos-constrained-delegation-how-to)
8. **Мені потрібно виправити претензії або подовжити термін дії маркера. Мені потрібно змінити тривалість сеансу**: для цього радимо перевірити такі статті: a. [Настроювання тверджень SAML, надісланих до програми](https://docs.microsoft.com/azure/active-directory/develop/active-directory-claims-mapping) b. [Робота з претензіями – з урахуванням застосунків](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy-configure-for-claims-aware-applications) c. Настроювання [життя маркера в програмі Microsoft Identity для платформи](https://docs.microsoft.com/azure/active-directory/develop/active-directory-configurable-token-lifetimes) d. [Настроювання Керування сеансами автентифікації за допомогою умовного доступу](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-conditional-access-session-lifetime) e. [Параметри файлів cookie для доступу до локальних програм](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy-configure-cookie-settings)
9. **Мені потрібна допомога в управлінні доступом користувачів і гостей (B2B)**, щоб отримати докладні відомості про керування доступом користувачів і гостей, радимо перевірити такі статті: a. [Керування доступом до програм](https://docs.microsoft.com/azure/active-directory/manage-apps/what-is-access-management) b. [Керування призначенням користувача для програми в надбудові "Azure Active Directory](https://docs.microsoft.com/azure/active-directory/manage-apps/assign-user-or-group-access-portal) c". [Настроювання програм SaaS для співпраці з B2B](https://docs.microsoft.com/azure/active-directory/external-identities/configure-saas-apps) d. [Надайте КОРИСТУВАЧАМ B2B доступ до своїх локальних програм у лазурі](https://docs.microsoft.com/azure/active-directory/external-identities/configure-saas-apps) . [Надання доступу до хмарних ресурсів для локальних облікових записів партнерів із використанням співпраці в Azure AD B2B](https://docs.microsoft.com/azure/active-directory/external-identities/hybrid-on-premises-to-cloud)
10. **Я хочу налаштувати мої програми**: щоб отримати докладні відомості про настроювання програм, радимо перевірити такі статті: a. [Настроювання спеціальних доменів за допомогою проксі-сервера програми Azure AD](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy-configure-custom-domain) . [Настроювання настроюваної домашньої сторінки для опублікованих програм](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy-configure-custom-home-page) c. [Програми узагальнення](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy-wildcard)
11. У **мене виникли проблеми з міграцією програми AD FS до Azure**: щоб усунути проблеми, які виникають під час перенесення програми з AD FS до Azure, радимо перевірити такі статті: a. [Під час перенесення автентифікації застосунку з служб Федерації Active Directory до Azure Active Directory](https://docs.microsoft.com/azure/active-directory/manage-apps/migrate-adfs-apps-to-azure) b. [Ресурси для перенесення програм до служби Azure Active Directory](https://docs.microsoft.com/azure/active-directory/manage-apps/migration-resources)
