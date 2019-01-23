---
title: Усунення несправностей із зарахування iOS пристроїв у Microsoft Intune
ms.author: pebaum
author: pebaum
manager: mnirkhe
ms.date: 10/24/2018
ms.audience: ITPro
ms.topic: article
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Priority
ms.assetid: d717bcc9-1cc1-44f6-b5e6-c1bc059c1973
ms.openlocfilehash: 663ff9b101494be781095ca550a4ed3deedca175
ms.sourcegitcommit: d6ea5e9458a2b8ceaab3ac4bd483e1130b9a398a
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 01/15/2019
ms.locfileid: "28319877"
---
# <a name="troubleshoot-issues-with-enrolling-ios-devices-in-microsoft-intune"></a>Усунення несправностей із зарахування iOS пристроїв у Microsoft Intune

Огляд ресурсів, перераховані нижче, щоб вирішити проблему, ваш тепер. 
  
Деякі поширені повідомлення про помилки та резолюції кроки:
  
- **Пристрій обмеження досягнуто** Користувач має додаткові пристрої вступив ніж пристрою обмеження. Перегляньте ці документи до [зняття пристрою](https://docs.microsoft.com/en-us/intune/devices-wipe) або [Змінити обмеження на пристрій](https://docs.microsoft.com/en-us/intune/enrollment-restrictions-set#set-device-limit-restrictions).
    
- **Це послуга не підтримується. Немає реєстрації політика:** Apple підштовхнути служби сповіщень (APNS) повинен бути налаштований або знову. Огляд [цей документ](https://docs.microsoft.com/en-us/intune/apple-mdm-push-certificate-get) для отримання інструкцій про те, як це зробити. 
    
- **Користувача ліцензії типу неприпустиме або ім'я користувача не розпізнано:** Користувач повинен призначити Intune або EMS ліцензії. Перегляньте ці документи до призначите ліцензію через: [блакитні порталу](https://docs.microsoft.com/en-us/azure/active-directory/license-users-groups)або [Офісу Центру адміністрування](https://docs.microsoft.com/en-us/intune/licenses-assign) .
    
Додаткові ресурси, щоб допомогти вирішити вашу проблему:
  
1. Використовувати [Intune виправлення неполадок портал](https://devicemanagement.microsoft.com/#blade/Microsoft_Intune_DeviceSettings/TroubleshootBlade) діагностувати та усунути поширені зарахування невдач. Огляд [цей документ](https://docs.microsoft.com/en-us/intune/help-desk-operators) для більш докладної інформації. 
    
2. Перегляньте ці документи список поширених помилок, які заважають заявки на участь та постанов до кожного: [усунення несправностей керівництво](https://support.microsoft.com/en-us/help/4039809/troubleshooting-ios-device-enrollment-in-intune) та [усунення несправностей doc](https://docs.microsoft.com/en-us/intune-classic/troubleshoot/troubleshoot-device-enrollment-in-intune).
    
3. [Дізнайтеся, як записатися iOS пристроїв у Microsoft Intune](https://docs.microsoft.com/en-us/intune/ios-enroll).
    
