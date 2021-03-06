---
title: Усунення несправностей із програмою Microsoft Defender для Office 365 (АТФ)
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 04/21/2020
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
ms.collection: Admin_O365
ms.custom: 3100021
ms.openlocfilehash: cf54d5b3b854587202ff1b575889b9602228dd06
ms.sourcegitcommit: 4caf5e6c2fee2903ccaf92cfc9006eb580faa7ba
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/29/2020
ms.locfileid: "48801428"
---
# <a name="troubleshoot-issues-with-office-365-atp"></a>Виправлення неполадок із АТФ Office 365

- **Зверніть увагу на затримку з доставкою повідомлення електронної пошти** ? Скористайтеся параметром динамічної доставки для політик вкладень у службі АТФ. Після цього ви уникнете затримки доставки повідомлень електронної пошти під час захисту одержувачів від зловмисних файлів.
- **Ви хочете повідомити про помилкові спрацьовувань або помилкових негативів** ? Скористайтеся цим посиланням, щоб надіслати файл для аналізу. [https://microsoft.com/wdsi/filesubmission](https://microsoft.com/wdsi/filesubmission)
- **Чи знаєте ви, що ви можете ввімкнути захист зв'язків із безпечними посиланнями для електронної пошти, надісланих між користувачами в організації** ? Виконайте наведені нижче кроки.
    1. Перейдіть на сторінку https://protection.office.com та ввійдіть.
    2. Перехід до **політики керування загрозою** "  >  **Policy**  >  **безпечні посилання** ".
    3. У розділі **політики, які стосуються певних одержувачів** , редагування (або додавання) політики.
    4. Виберіть пункт **використовувати безпечні посилання на повідомлення, надіслані в організації** .
    5. Збережіть свою політику та дозвольте приблизно 30 хвилин для змін, які потрібно працювати в центрі обробки даних.
- Щоб отримати додаткову довідку з АТФ, перегляньте статтю [Microsoft Defender для Office 365](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp).