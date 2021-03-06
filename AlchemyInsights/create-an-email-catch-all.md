---
title: Створення повідомлення електронної пошти "спіймати все"
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
- "9001524"
- "3732"
ms.openlocfilehash: 262d2c6a7181d94094f3d840c4ba3ebd07000cf4
ms.sourcegitcommit: c6692ce0fa1358ec3529e59ca0ecdfdea4cdc759
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 09/14/2020
ms.locfileid: "47713007"
---
# <a name="create-an-email-catch-all"></a>Створення повідомлення електронної пошти "спіймати все"

Використання спіймати все сильно не рекомендується. Щоб відправник не міг отримувати повідомлення про те, що його не можна було доставити, то краще надати відправнику відомості про те, що вони можуть виконувати дії. Ви також можете обмежити відповідну поштову скриньку, щоб зловити раніше дійсні адреси електронної пошти. 

Усі поштові скриньки можуть отримувати багато спаму, а потім заповнювати їх, якщо вони не будуть ретельно контролюватися. (Є обмеження на отримання.) 

Якщо ви вирішите продовжити, виконайте наведені нижче дії.

1. Створення динамічної групи розсилки & містять "Усі типи одержувачів".

2. Створюйте спеціальні поштові скриньки, щоб спіймати повідомлення електронної пошти, наприклад catchall@domain.com.

3. Для певного домену настройте тип домену на "InternalRelay". Якщо ви згодом видалите всі елементи "спіймати все", переконайтеся, що домен повернутися до авторитетного значення.

4. Створення правила транспортування поштової потоки таким, як описано нижче.

    - Якщо відправник – "поза організацією"
    - Переспрямування повідомлення до Catchall@domain.com
    - За винятком випадків, коли одержувач входить до складу allusers@domain.com (група розсилки містить всі учасники)
    - Перевірка того, що нові поштові скриньки додаються до динамічної групи розсилки
