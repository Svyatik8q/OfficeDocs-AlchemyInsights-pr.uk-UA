---
title: Відкрити за допомогою провідника не працює
ms.author: toresing
author: tomresing
manager: scotv
ms.date: 12/10/2018
ms.audience: Admin
ms.topic: article
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Priority
ms.collection: Adm_O365
ms.custom: Adm_O365
ms.assetid: b8f07022-69fe-4112-a2f6-d3a6cedb966c
ms.openlocfilehash: b55fc7bd5670e655334ef7be368b245c8899633a
ms.sourcegitcommit: d6ea5e9458a2b8ceaab3ac4bd483e1130b9a398a
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 01/15/2019
ms.locfileid: "28318696"
---
# <a name="open-with-explorer-isnt-working"></a>Відкрити за допомогою провідника не працює

Якщо **Відкрити у провіднику** або **Перегляд у Файловому провіднику** не працює переконайтеся, WebClient служби **запущений** , виконавши наведені нижче дії. Наприклад, може тривати багато часу, щоб відкрити бібліотеки SharePoint або OneDrive, коли службу не запущено. 
  
1. У полі пошуку Windows, тип запустити, виберіть запустити застосунок робочого стола, введіть Services. msc і виберіть **Enter**.
    
2. Прокрутіть вниз до служби WebClient і перегляньте стовпець **стан** . Якщо стан служби WebClient ще не **запущено**, двічі клацніть служби, натисніть кнопку **Пуск**і натисніть кнопку **ОК**. Підключити послугу, якщо це необхідно, вибираючи або **вручну** або **автоматично** в полі **Тип запуску** . 
    
> [!NOTE]
> Для виправлення неполадок відкриття у Файловому провіднику, переглянути [відкриті у провіднику](https://go.microsoft.com/fwlink/?linkid=871665). Дослідіть синхронізації як краща альтернатива: [SharePoint синхронізації файлів з новим клієнтом синхронізації OneDrive](https://go.microsoft.com/fwlink/?linkid=871666). 
  
