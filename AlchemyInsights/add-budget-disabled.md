---
title: Чому кнопка "Додати бюджет" для мене вимкнуто?
ms.author: pebaum
author: pebaum
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
ms.collection: Adm_O365
ms.custom:
- "9003547"
- "6464"
ms.openlocfilehash: 18edad73f617ba180cb08576ee6e5fa8faf07128
ms.sourcegitcommit: 9a7b85eae0bb775bc2498a83d8f5fedb72a6451e
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/27/2020
ms.locfileid: "48807674"
---
# <a name="why-is-the-add-budget-button-disabled-for-me"></a>Чому кнопка "Додати бюджет" для мене вимкнуто?

Щоб створити бюджет, знадобиться один із таких дозволів:

- Група «керування», «Передплата», «області груп ресурсів»
- Учасник керування витратами
- Власник
- Внесок
- Лише для корпоративного клієнта: «реєстрація», «відділ», «області облікових записів»
- Адміністратор реєстрації (установлення бюджету на область реєстрації)
- Адміністратор відділу (Настроювання бюджету в області департаменту)
- Власник облікового запису (Настроювання бюджету в області облікових записів)
- Лише сучасна угода клієнта: обліковий запис рахунку, профіль виставлення рахунків, області "рахунок-фактура"
- Створення "Блакитний"

**Я створив бюджет, коли моя вартість поточного місяця вже пройшла через бюджет. Чому я не отримав оповіщення?**  
Якщо ви вже перевищили певний поріг витрат, коли ви створюєте бюджет, у якому оповіщення не буде пожежа. Після запуску нового циклу, якщо ви порушують поріг, то оповіщення буде пожежа.

**Коли слід очікувати отримати оповіщення після того, як ви перевищуєте один із моїх визначених порогів сповіщень про бюджет?**  
Бюджети обчислюються кожні 4 години. Для використання даних, які можна використовувати для досягнення системи бюджетів, потрібно не менше 8 годин. Якщо врахувати це, оповіщення може тривати до 12 годин, щоб вогонь після перевищення порогу.

**Чому кнопка "Дата початку" вимкнута, коли я вибюю час скидання місяця або місяця виставлення рахунків?**  
Бюджети відповідають поточному календарному місяцю або поточному рахунку (у випадку, коли вибрано "місяць виставлення рахунків"). Тому ми попередньо заповните це значення.

**Чому граф моїх витрат не відображається в досвіді створення бюджету?**  
Нам потрібно мінімум 2 місяці вартості даних, перш ніж ми зможемо надати графік, щоб допомогти вам у створенні бюджету.

**Чому я не можу встановити бюджет із передплатою, яку я щойно створив?**  
Після створення передплатою, дані мають 24-48 годин для обробки, перш ніж встановлювати бюджет.

**Ресурси бюджетної API**

- " [БЮДЖЕТИ API" V1](https://docs.microsoft.com/rest/api/consumption/budgets?WT.mc_id=Portal-Microsoft_Azure_Support): надає операції для створення та оновлення бюджетів. Використовуючи API для бюджетів, ви можете встановити граничне значення бюджету та настроїти кілька оповіщень на пожежу під час наближення цього порогу. Оповіщення можуть ініціювати електронну пошту або групу дій Azure, щоб виконувати автоматизацію. Примітка. фільтрування для цього API не вирівнюється за допомогою фільтрування та вимірів API запитів.
- [БЮДЖЕТИ API V2](https://github.com/Azure/azure-rest-api-specs/blob/master/specification/cost-management/resource-manager/Microsoft.CostManagement/preview/2019-04-01-preview/examples/CreateOrUpdateBudget.json): створення бюджетів за допомогою більшої вартості фільтруючих можливостей, ніж V1. Фільтрування Вирівнює за договором, який використовується в нашому запиті та розмірах API. Це рекомендований API для бюджетів, щоб використовувати рух вперед.
- [Розміри](https://docs.microsoft.com/rest/api/cost-management/dimensions?WT.mc_id=Portal-Microsoft_Azure_Support): надає операції, щоб отримати підтримувані розміри для використання в різних областях. Використовуючи API "виміри", можна отримати список вимірів, які можна використовувати як входи для створення запитів за допомогою API запитів.
- [Запит](https://docs.microsoft.com/rest/api/cost-management/query?WT.mc_id=Portal-Microsoft_Azure_Support): надає операції, щоб отримати Сукупні витрати та дані про використання на основі запиту, який ви надаєте. За допомогою API запитів можна вказати бажаний фільтрування, сортування та групування на всіх доступних розмірах (які доступні з API "виміри").

**Прогнозовані витрати**

**Чому не відображаються прогнози для витрат у аналізі витрат?**  
Існує кілька причин, через які проекцію прогнозу може бути відсутнє для вас у аналізі витрат, деякі з них мають такий вигляд:

1. Якщо вартість даних становить менше 10 днів, діаграму прогнозу не завантажиться. Модель вимагає принаймні 10 днів після нещодавньої вартості даних для точних прогнозів
2. Якщо виділено історичні дати, діаграму не буде видно. Виберіть проміжок часу, у якому майбутні дати для діаграми прогнозного відображення
3. Якщо ваш обліковий запис має кілька валют, на діаграмі прогнозу буде лише вартість проекту "Усі витрати в доларах США"

**Чому прогноз зміниться під час внесення змін до ресурсів?**  
Модель прогнозу вимагає кілька днів, щоб враховувати зміни в обліковому записі, а також не вносити негайні прогнози на основі змін у ресурсах  
Для більших кроків збільшення або зменшення кількості ресурсів модель займе трохи більше часу, щоб ці зміни були в обліковому записі для аномалій

**Чому мій прогноз збільшиться після того, як ви робите покупку або придбання ринку?**  
Модель прогнозу враховує ваші фактичні витрати та не враховує використання та придбання окремо. Для одноразової покупки модель зменшить прогнози через 10 днів, щоб враховувати різке збільшення витрат.

**Я хочу переглянути прогнози для окремого виміру (наприклад. Метр**  
Зараз прогноз підтримує загальні прогнози на витрати, а не для окремих лічильників. Таким чином, коли "згруповано за" виміром, прогнози міститимуться в загальній складності всіх одиниць виміру.

**Рекомендовані документи**

- [Що таке Лазурне керування витратами?](https://docs.microsoft.com/azure/cost-management/overview-cost-mgt?WT.mc_id=Portal-Microsoft_Azure_Support)
- [Практичні поради з керування витратами в "Блакитний"](https://docs.microsoft.com/azure/cost-management/cost-mgt-best-practices?WT.mc_id=Portal-Microsoft_Azure_Support)
- [Аналізувати витрати та витрати](https://docs.microsoft.com/azure/cost-management/quick-acm-cost-analysis?WT.mc_id=Portal-Microsoft_Azure_Support)
- [Огляд та аналіз витрат за допомогою аналізу витрат](https://docs.microsoft.com/azure/cost-management/quick-acm-cost-analysis?WT.mc_id=Portal-Microsoft_Azure_Support)
- [Керування витратами на Лазурне: ціноутворення](https://azure.microsoft.com/services/cost-management/#pricing)
- [Перевірка витрат у аналізі витрат](https://docs.microsoft.com/azure/cost-management-billing/costs/quick-acm-cost-analysis?WT.mc_id=Portal-Microsoft_Azure_Support#review-costs-in-cost-analysis)
- [Навчальне відео: створення бюджету на порталі «Лазурний»](https://www.youtube.com/watch?v=ExIVG_Gr45A&t=4s)
- [Попередні вимоги для перегляду та настроювання бюджетів](https://docs.microsoft.com/azure/cost-management-billing/costs/tutorial-acm-create-budgets?WT.mc_id=Portal-Microsoft_Azure_Support#prerequisites)
- [Створення та керування бюджетами](https://docs.microsoft.com/azure/cost-management-billing/costs/tutorial-acm-create-budgets?WT.mc_id=Portal-Microsoft_Azure_Support#create-a-budget-in-the-azure-portal)
- [Настроювання автоматизації за допомогою ІНТЕРФЕЙСУ "Azure груп дій і бюджетів"](https://docs.microsoft.com/azure/cost-management/tutorial-acm-create-budgets?WT.mc_id=Portal-Microsoft_Azure_Support#trigger-an-action-group)
- [Використання сповіщень про витрати для відстеження використання та витрачання коштів](https://docs.microsoft.com/azure/cost-management/cost-mgt-alerts-monitor-usage-spending?WT.mc_id=Portal-Microsoft_Azure_Support)
- [Практичні поради з керування витратами](https://docs.microsoft.com/azure/cost-management/cost-mgt-best-practices?WT.mc_id=Portal-Microsoft_Azure_Support)  

**Навчальне відео**

- [Створення бюджету на порталі «Лазурний»](https://go.microsoft.com/fwlink/?linkid=2146761)
- [Керування витратами за допомогою API бюджетів і груп дій](https://go.microsoft.com/fwlink/?linkid=2147038)