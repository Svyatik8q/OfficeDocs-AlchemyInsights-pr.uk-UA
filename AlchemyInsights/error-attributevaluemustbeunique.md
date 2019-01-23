---
title: Помилка AttributeValueMustBeUnique
ms.author: pebaum
author: pebaum
manager: mnirkhe
ms.date: 3/20/2018
ms.audience: Admin
ms.topic: article
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Priority
ms.collection: Adm_O365
ms.custom: Adm_O365
ms.assetid: bf8ac830-6f0c-4616-827d-987616700e59
ms.openlocfilehash: 7a97d1a5ff352b55833bd457e3220a56130d7e7e
ms.sourcegitcommit: d6ea5e9458a2b8ceaab3ac4bd483e1130b9a398a
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 01/15/2019
ms.locfileid: "28319373"
---
# <a name="error-attributevaluemustbeunique"></a>Помилка: AttributeValueMustBeUnique

Найпоширеніша причина AttributeValueMustBeUnique помилка в два об'єкти з різними SourceAnchor (immutableId) мають однакове значення для атрибутів ProxyAddresses та/або UserPrincipalName. Виправити помилки AttributeValueMustBeUnique:
  
1. Визначити дубльованого proxyAddresses, userPrincipalName або інші значення атрибута, яке викликає появу помилки. Також визначити, які об'єкти два (або більше) беруть участь в конфлікті. У доповіді породжених Azure оголошення підключення здоров'я для синхронізації може допомогти визначити два об'єкти.
    
2. Визначити, які об'єкти повинні продовжувати, які дублюються виконання і які об'єкти.
    
3. Видаліть дубльовані значення з об'єкта, який не може мати значення. Зверніть увагу, що ви повинні зробити зміни в каталог, де об'єкт був здобутий з. У деяких випадках може знадобитися видалити один з об'єктів в конфлікті.
    
4. Після внесення змін в приміщенні на оголошення, дайте Azure оголошення підключення синхронізувати зміни помилок отримати фіксовані.
    
