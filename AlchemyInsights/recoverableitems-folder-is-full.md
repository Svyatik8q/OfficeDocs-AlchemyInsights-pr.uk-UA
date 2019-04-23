---
title: Сповнена 1336 RecoverableItems папки
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 11/5/2018
ms.audience: ITPro
ms.topic: article
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
ms.custom: 1336
ms.assetid: a3a923e8-fece-4a26-b8b6-00970d75275e
ms.openlocfilehash: 14d46980caf7dac90e73c34482a3aee34382fa1f
ms.sourcegitcommit: 1a4b8fa9e38a95ca811085af516edb81caf2018c
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/13/2019
ms.locfileid: "31859017"
---
# <a name="the-recoverable-items-folder-is-full"></a><span data-ttu-id="2a978-102">Папки «Відновлювані» заповнено</span><span class="sxs-lookup"><span data-stu-id="2a978-102">The Recoverable Items folder is full</span></span>

<span data-ttu-id="2a978-103">Для поштових скриньок Exchange Online у службі Office 365 максимальний зберігання для папки «Відновлювані» становить 30 ГБ.</span><span class="sxs-lookup"><span data-stu-id="2a978-103">For Exchange Online mailboxes in Office 365, the default storage limit for the Recoverable Items folder is 30 GB.</span></span> <span data-ttu-id="2a978-104">Граничний розмір сховища для папки «Відновлювані» автоматично збільшується на 100 ГБ, якщо поштова скринька розміщена на судове утримання, пошук необхідної утримання, чи призначено політику збереження до Office 365.</span><span class="sxs-lookup"><span data-stu-id="2a978-104">The storage limit for the Recoverable Items folder is automatically increased to 100 GB if the mailbox is placed on Litigation Hold, eDiscovery hold, or is assigned to an Office 365 retention policy.</span></span>

<span data-ttu-id="2a978-105">Коли папки «Відновлювані» досягає граничний розмір сховища, поштової скриньки функціональність порушені таким чином:</span><span class="sxs-lookup"><span data-stu-id="2a978-105">When the Recoverable Items folder reaches the storage limit, mailbox functionality is affected in the following ways:</span></span>

- <span data-ttu-id="2a978-106">Користувач не може видаляти з поштової скриньки.</span><span class="sxs-lookup"><span data-stu-id="2a978-106">The user can't delete items from the mailbox.</span></span>

- <span data-ttu-id="2a978-107">Помічник із керованих папок не вдалося видалити елементи на основі тег збереження або настройки для керованих папок.</span><span class="sxs-lookup"><span data-stu-id="2a978-107">The Managed Folder Assistant can't delete items based on retention tag or managed folder settings.</span></span>

- <span data-ttu-id="2a978-108">Для поштових скриньок, які мають одну функцію відновлення елемента включений, або поміщаються на утримання процес запису копію сторінки захист не може підтримувати версій елементів відредагований користувачем.</span><span class="sxs-lookup"><span data-stu-id="2a978-108">For mailboxes that have Single Item Recovery enabled or are placed on hold, the copy-on-write page protection process can't maintain versions of items edited by the user.</span></span>

- <span data-ttu-id="2a978-109">Для поштових скриньок, які мають журналюванням аудиту поштової скриньки не записи в журналі аудиту поштової скриньки можуть бути збережені у аудитів вкладеної папки в папці Відновлювані елементи».</span><span class="sxs-lookup"><span data-stu-id="2a978-109">For mailboxes that have mailbox audit logging enabled, no mailbox audit log entries can be saved in the Audits subfolder in the Recoverable Items folder.</span></span>

<span data-ttu-id="2a978-110">Для поштових скриньок, які не утримуються, адміністратори можуть використовувати на `Search-Mailbox -SearchDumpsterOnly -DeleteContent` команду в Exchange Online PowerShell видалити елементи в папці Відновлювані елементи».</span><span class="sxs-lookup"><span data-stu-id="2a978-110">For mailboxes that aren't on hold, admins can use the `Search-Mailbox -SearchDumpsterOnly -DeleteContent` command in Exchange Online PowerShell to delete items in the Recoverable Items folder.</span></span> <span data-ttu-id="2a978-111">Докладніше Перегляньте такі розділи:</span><span class="sxs-lookup"><span data-stu-id="2a978-111">For more information, see the following topics:</span></span> 

- [<span data-ttu-id="2a978-112">Пошук і видалення повідомлень</span><span class="sxs-lookup"><span data-stu-id="2a978-112">Search for and delete messages</span></span>](https://docs.microsoft.com/office365/securitycompliance/search-for-and-delete-messagesadmin-help)

- [<span data-ttu-id="2a978-113">Search-Mailbox</span><span class="sxs-lookup"><span data-stu-id="2a978-113">Search-Mailbox</span></span>](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Search-Mailbox)

<span data-ttu-id="2a978-114">Для поштових скриньок, які знаходяться на утриманні адміністратори повинні видалити утримання, перш ніж вони можуть видалені елементи з папки «Відновлювані».</span><span class="sxs-lookup"><span data-stu-id="2a978-114">For mailboxes that are on hold, admins have to remove the hold before they can deleted items from the Recoverable Items folder.</span></span> <span data-ttu-id="2a978-115">Докладніше перегляньте [видалення елементів у відновлювані папку хмарних поштових скриньок на утримуйте](https://docs.microsoft.com/office365/securitycompliance/delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold).</span><span class="sxs-lookup"><span data-stu-id="2a978-115">For more information, see [Delete items in the Recoverable Items folder of cloud-based mailboxes on hold](https://docs.microsoft.com/office365/securitycompliance/delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold).</span></span>

<span data-ttu-id="2a978-116">Щоб запобігти папки «Відновлювані» стає повний, адміністратори можуть збільшити зберігання Відновлювані папку для поштових скриньок на провести і настроїти політику збереження поштової скриньки, який переміщує елементи з папки «Відновлювані» до архіву користувача Поштова скринька.</span><span class="sxs-lookup"><span data-stu-id="2a978-116">To help prevent the Recoverable Items folder from becoming full, admins can increase the storage limit of the Recoverable Items folder for mailboxes on hold and set up a mailbox retention policy that moves items from the Recoverable Items folder to the user's archive mailbox.</span></span> <span data-ttu-id="2a978-117">Переглянути [збільшити Відновлювані квоти поштових скриньок на утримуйте](https://docs.microsoft.com/office365/securitycompliance/increase-the-recoverable-quota-for-mailboxes-on-hold).</span><span class="sxs-lookup"><span data-stu-id="2a978-117">See [Increase the Recoverable Items quota for mailboxes on hold](https://docs.microsoft.com/office365/securitycompliance/increase-the-recoverable-quota-for-mailboxes-on-hold).</span></span>