---
title: Відновлення видаленої вузлів
ms.author: kaarins
author: kaarins
manager: scotv
ms.date: 5/1/2018
ms.audience: Admin
ms.topic: article
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Priority
ms.collection: Adm_O365
ms.custom: Adm_O365
ms.assetid: cf7521c3-97b4-465a-97eb-6c0a41338a30
ms.openlocfilehash: b3c72033dfcc093dd0c2837d2866c6a78d64449c
ms.sourcegitcommit: d6ea5e9458a2b8ceaab3ac4bd483e1130b9a398a
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 01/15/2019
ms.locfileid: "28319209"
---
# <a name="restore-a-deleted-site-collection"></a><span data-ttu-id="c418d-102">Відновлення видаленої вузлів</span><span class="sxs-lookup"><span data-stu-id="c418d-102">Restore a deleted site collection</span></span>

<span data-ttu-id="c418d-p101">Коли адміністратор видаляє класичний вузлів, вона перебуває у колекції сайтів кошика, де вона зберігається на 93 днів, перш ніж вона видаляється остаточно. Щоб відновити колекції сайтів:</span><span class="sxs-lookup"><span data-stu-id="c418d-p101">When an admin deletes a classic site collection, it's placed in the site collection Recycle Bin, where it's kept for 93 days before it's permanently deleted. To restore the site collection:</span></span>
  
1. <span data-ttu-id="c418d-105">Класичний центру адміністрування SharePoint клацніть **«Кошик»** на стрічці.</span><span class="sxs-lookup"><span data-stu-id="c418d-105">In the classic SharePoint admin center, click **Recycle Bin** on the ribbon.</span></span> 
    
2. <span data-ttu-id="c418d-106">Установіть прапорець поруч із колекції сайтів, для відновлення.</span><span class="sxs-lookup"><span data-stu-id="c418d-106">Select the check box next to the site collection you want to restore.</span></span>
    
3. <span data-ttu-id="c418d-107">Натисніть кнопку **відновити видалені елементи**.</span><span class="sxs-lookup"><span data-stu-id="c418d-107">Click **Restore Deleted Items**.</span></span>
    
<span data-ttu-id="c418d-p102">Щоб відновити видалене повідомлення сайту, можна використовувати нові SharePoint admin центр попереднього перегляду. В іншому випадку ви повинні використовувати PowerShell. Щоб відновити сайт, що належить до групи Office 365, потрібно буде відновити група Exchange центру адміністрування. Групи можуть бути відновлені протягом 30 днів після того, як вони ви видалили.</span><span class="sxs-lookup"><span data-stu-id="c418d-p102">To restore a deleted communication site, you can use the new SharePoint admin center preview. Otherwise, you need to use PowerShell. To restore a site that belongs to an Office 365 group, you need to restore the group in the Exchange admin center. Groups can be restored for 30 days after they're deleted.</span></span>
  
