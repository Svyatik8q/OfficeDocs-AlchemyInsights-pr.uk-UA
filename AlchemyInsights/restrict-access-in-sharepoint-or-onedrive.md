---
title: Обмеження доступу в SharePoint або OneDrive
ms.author: mikeplum
author: MikePlumleyMSFT
ms.date: 8/7/2018
ms.audience: ITPro
ms.topic: article
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Priority
ms.assetid: af1b936b-0475-497b-a6d3-e671aef7b717
ms.openlocfilehash: b6be074ed5f7e83f8196ca3fe90252673896569f
ms.sourcegitcommit: d6ea5e9458a2b8ceaab3ac4bd483e1130b9a398a
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 01/15/2019
ms.locfileid: "28319486"
---
# <a name="restrict-access-in-sharepoint-or-onedrive"></a>Обмеження доступу в SharePoint або OneDrive

У SharePoint і OneDrive Вам обмежити доступ до пунктам, як файли, папки та списки надавши права доступу лише для особи або групи осіб, які ви хочете мати доступ. За промовчанням дозволи в SharePoint успадковано від вище вгору в ієрархії. Так файл успадковують його дозволи з папки, які успадковують його дозволи з бібліотеки, які успадковують його дозволи від сайту.
  
Ви можете поділитися на вищому рівні (таких як шляхом обміну всього сайту) і потім розбити спадкування, якщо ви не хочете ділитися всі предмети на сайті. Однак, не рекомендується це тому, що це робить підтримання дозволи більш складною і заплутаною в майбутньому. Ось те, що ви могли б зробити замість цього:
  
- Якщо, наприклад, ви хочете поділитися весь вміст папки, за винятком одного файлу в ньому, перемістити цей файл до нового розташування, які не є спільним.
    
- Якщо у вас є два вкладені папки в папці, і ви хочете, щоб поділитися один вкладену папку з групи A та B і дозволити тільки Група A доступ до другого підпапку, поділитися батьківську папку з групи A та додати Група B першу вкладену папку.
    
[Закрити спільний доступ до файлу або папки](https://go.microsoft.com/fwlink/?linkid=2008861)
  
