---
title: Обійти лобі
ms.author: pebaum
author: pebaum
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
ms.collection: Adm_O365
ms.custom:
- "2673"
- "9000740"
ms.openlocfilehash: 311af365a94b788182bb6870bca3f67b2ad802d0
ms.sourcegitcommit: 932981641dd8e973e28dfe346bbdf9c923111b13
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 12/27/2019
ms.locfileid: "40889103"
---
# <a name="control-lobby-settings-and-level-of-participation-in-teams"></a><span data-ttu-id="4333d-102">Контроль параметрів лобі та рівень участі в teams</span><span class="sxs-lookup"><span data-stu-id="4333d-102">Control lobby settings and level of participation in Teams</span></span>

<span data-ttu-id="4333d-103">Якщо ви хочете дозволити всім, включаючи комутованих, зовнішніх і анонімних користувачів, щоб **обійти фойє**, використовуйте PowerShell для виконання цього завдання.</span><span class="sxs-lookup"><span data-stu-id="4333d-103">If you'd like to allow everyone, including Dial-in, external, and anonymous users, to **bypass the lobby**, use PowerShell to accomplish this task.</span></span> <span data-ttu-id="4333d-104">Нижче наведено приклад змінення політики глобального наради для вашої організації.</span><span class="sxs-lookup"><span data-stu-id="4333d-104">Here's an example of modifying the global meeting policy for your organization.</span></span>

`Set-CsTeamsMeetingPolicy -Identity Global -AutoAdmittedUsers "Everyone" -AllowPSTNUsersToBypassLobby $True`

<span data-ttu-id="4333d-105">Цю команду в даний час вимагає використання Skype для бізнесу PowerShell модуль.</span><span class="sxs-lookup"><span data-stu-id="4333d-105">This cmdlet currently requires the use of Skype for Business PowerShell module.</span></span> <span data-ttu-id="4333d-106">Щоб отримати налаштування для використання цього командлета, перегляньте [керування політиками за допомогою PowerShell](https://docs.microsoft.com/microsoftteams/teams-powershell-overview#managing-policies-via-powershell).</span><span class="sxs-lookup"><span data-stu-id="4333d-106">To get set up to use this cmdlet, check out [Managing policies via PowerShell](https://docs.microsoft.com/microsoftteams/teams-powershell-overview#managing-policies-via-powershell).</span></span>

<span data-ttu-id="4333d-107">Після настроювання політики потрібно застосувати його до користувачів; або, якщо ви змінили глобальну політику, вона буде автоматично застосовуватися до користувачів.</span><span class="sxs-lookup"><span data-stu-id="4333d-107">Once you’ve set up a policy, you need to apply it to users; or, if you modified the Global policy, it will automatically apply to users.</span></span> <span data-ttu-id="4333d-108">Для будь-яких змін у політиці потрібно зачекати принаймні **4 години до 24 годин** , щоб правила набрали сили.</span><span class="sxs-lookup"><span data-stu-id="4333d-108">For any policy change, you need to wait at least **4 hours up to 24 hours** for the policies to take effect.</span></span> 

<span data-ttu-id="4333d-109">Обов'язково перегляньте документацію нижче, перш ніж вносити ці зміни, щоб точно зрозуміти, що це дозволяє.</span><span class="sxs-lookup"><span data-stu-id="4333d-109">Be sure to review the documentation below before making these changes to understand exactly what this allows.</span></span>


## <a name="understanding-teams-meeting-lobby-policy-controls"></a><span data-ttu-id="4333d-110">Знайомство з командами переговорних елементів керування політикою</span><span class="sxs-lookup"><span data-stu-id="4333d-110">Understanding Teams meeting lobby policy controls</span></span>

<span data-ttu-id="4333d-111">Ці настройки керують тим, що учасники зустрічі чекають у вестибюлі, перш ніж вони будуть допущені до зустрічі і рівень участі, який вони можуть отримати на нараді.</span><span class="sxs-lookup"><span data-stu-id="4333d-111">These settings control which meeting participants wait in the lobby before they are admitted to the meeting and the level of participation they are allowed in a meeting.</span></span> <span data-ttu-id="4333d-112">PowerShell можна використовувати для оновлення зустрічі параметри політики, які ще не реалізовано (з написом "скоро") у команди центру адміністрування.</span><span class="sxs-lookup"><span data-stu-id="4333d-112">You can use PowerShell to update meeting policy settings that haven't yet been implemented (labeled "coming soon") in the Teams admin center.</span></span> <span data-ttu-id="4333d-113">Нижче наведено приклад командлета PowerShell, який дозволяє всім користувачам обходити фойє.</span><span class="sxs-lookup"><span data-stu-id="4333d-113">See below for an example PowerShell cmdlet that allows all users to bypass the lobby.</span></span>

- <span data-ttu-id="4333d-114">[Автоматично визнати](https://docs.microsoft.com/microsoftteams/meeting-policies-in-teams#automatically-admit-people) , що люди в політиці для Організатора, що контролює, чи є люди приєднатися до наради безпосередньо або чекати у фойє, поки вони не будуть допущені автентифікованим користувачем.</span><span class="sxs-lookup"><span data-stu-id="4333d-114">[Automatically admit people](https://docs.microsoft.com/microsoftteams/meeting-policies-in-teams#automatically-admit-people) is a per-organizer policy that controls whether people join a meeting directly or wait in the lobby until they are admitted by an authenticated user.</span></span>

- <span data-ttu-id="4333d-115">[Дозволити анонімним людям розпочати нараду](https://docs.microsoft.com/microsoftteams/meeting-policies-in-teams#allow-anonymous-people-to-start-a-meeting) – це політика Організатора, яка керує тим, чи можуть користувачі анонімних користувачів, ВКЛЮЧНО з B2B та федеративними користувачами, приєднатися до наради користувача без автентифікованого користувача з організації.</span><span class="sxs-lookup"><span data-stu-id="4333d-115">[Allow anonymous people to start a meeting](https://docs.microsoft.com/microsoftteams/meeting-policies-in-teams#allow-anonymous-people-to-start-a-meeting) is a per-organizer policy that controls whether anonymous people, including B2B and federated users, can join the user's meeting without an authenticated user from the organization in attendance.</span></span>

- <span data-ttu-id="4333d-116">[Дозволити комутованого користувачів, щоб обійти фойє](https://docs.microsoft.com/microsoftteams/meeting-policies-in-teams#allow-dial-in-users-to-bypass-the-lobby-coming-soon) (**скоро**) є для Організатора політики, яка контролює, чи люди, які підключаються по телефону приєднатися до наради безпосередньо або чекати в холі, незалежно від того, **автоматично визнати, люди** налаштування.</span><span class="sxs-lookup"><span data-stu-id="4333d-116">[Allow dial-in users to bypass the lobby](https://docs.microsoft.com/microsoftteams/meeting-policies-in-teams#allow-dial-in-users-to-bypass-the-lobby-coming-soon) (**coming soon**) is a per-organizer policy that controls whether people who dial in by phone join the meeting directly or wait in the lobby regardless of the **Automatically admit people** setting.</span></span>

- <span data-ttu-id="4333d-117">[Дозволити організаторам змінювати параметри фойє](https://docs.microsoft.com/microsoftteams/meeting-policies-in-teams#allow-organizers-to-override-lobby-settings-coming-soon) (**скоро**)-це політика Організатора, яка керує тим, чи може Організатор наради перевизначити параметри фойє, які встановлюються адміністратором у **автоматичному режимі, допускають** користувачів і **дозволяють користувачам телефонувати до фойє** під час планування нової наради.</span><span class="sxs-lookup"><span data-stu-id="4333d-117">[Allow organizers to override lobby settings](https://docs.microsoft.com/microsoftteams/meeting-policies-in-teams#allow-organizers-to-override-lobby-settings-coming-soon) (**coming soon**) is a per-organizer policy that controls whether the meeting organizer can override the lobby settings that an admin set in **Automatically admit people** and **Allow dial-in users to bypass the lobby** when they schedule a new meeting.</span></span>

<span data-ttu-id="4333d-118">**Примітка:** Для повного огляду політики зборів Microsoft teams прочитайте [команди керування політикою нарад](https://docs.microsoft.com/microsoftteams/meeting-policies-in-teams) .</span><span class="sxs-lookup"><span data-stu-id="4333d-118">**Note:** Read [Manage meeting policies in Teams](https://docs.microsoft.com/microsoftteams/meeting-policies-in-teams) for a complete overview of Microsoft Teams meeting policies.</span></span>