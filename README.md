---
ms.openlocfilehash: 6e36e6599e36218ce2a925dceda7aa0ee6811057
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2019
ms.locfileid: "58142229"
---
# <a name="microsoft-open-source-code-of-conduct"></a><span data-ttu-id="a2024-101">Правила поведения: использование открытого исходного кода Майкрософт</span><span class="sxs-lookup"><span data-stu-id="a2024-101">Microsoft Open Source Code of Conduct</span></span>

<span data-ttu-id="a2024-102">Этот проект основывается на [правилах использования открытого исходного кода Майкрософт](https://opensource.microsoft.com/codeofconduct/).</span><span class="sxs-lookup"><span data-stu-id="a2024-102">This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).</span></span>
<span data-ttu-id="a2024-103">Дополнительные сведения см. в [вопросах и ответах о правилах поведения](https://opensource.microsoft.com/codeofconduct/faq/) или обратитесь по адресу [opencode@microsoft.com](mailto:opencode@microsoft.com) с любыми дополнительными вопросами или комментариями.</span><span class="sxs-lookup"><span data-stu-id="a2024-103">For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.</span></span>

<span data-ttu-id="a2024-104">[![Состояние сборки](https://ci.appveyor.com/api/projects/status/onshefxnc4g4pv87/branch/staging?svg=true)](https://ci.appveyor.com/project/PowerShell/powershell-docs/branch/staging)</span><span class="sxs-lookup"><span data-stu-id="a2024-104">[![Build status](https://ci.appveyor.com/api/projects/status/onshefxnc4g4pv87/branch/staging?svg=true)](https://ci.appveyor.com/project/PowerShell/powershell-docs/branch/staging)</span></span>

## <a name="powershell-documentation"></a><span data-ttu-id="a2024-105">Документация по PowerShell</span><span class="sxs-lookup"><span data-stu-id="a2024-105">PowerShell Documentation</span></span>

<span data-ttu-id="a2024-106">Добро пожаловать в репозиторий PowerShell-Docs, в котором находится официальная документация по PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a2024-106">Welcome to the PowerShell-Docs repository, housing the official PowerShell documentation.</span></span>

## <a name="repository-structure"></a><span data-ttu-id="a2024-107">Структура репозитория</span><span class="sxs-lookup"><span data-stu-id="a2024-107">Repository Structure</span></span>

<span data-ttu-id="a2024-108">Каждая из перечисленных ниже папок верхнего уровня содержит набор документации, которая опубликована на сайте [документации Майкрософт](https://docs.microsoft.com/powershell).</span><span class="sxs-lookup"><span data-stu-id="a2024-108">Each of the following top-level folders in this repo contain a DocSet that is published to [Microsoft Docs](https://docs.microsoft.com/powershell).</span></span>

- <span data-ttu-id="a2024-109">[/developer/](https://docs.microsoft.com/powershell/developer/) — папка для будущей документации по пакету SDK PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a2024-109">[/developer/](https://docs.microsoft.com/powershell/developer/) is the future home of the PowerShell SDK documentation</span></span>
  - <span data-ttu-id="a2024-110">Сейчас мы переносим это содержимое с сайта MSDN.</span><span class="sxs-lookup"><span data-stu-id="a2024-110">We are in the process of migrating this content from MSDN</span></span>
- <span data-ttu-id="a2024-111">[/dsc/](https://docs.microsoft.com/powershell/dsc/) — для функции настройки требуемого состояния.</span><span class="sxs-lookup"><span data-stu-id="a2024-111">[/dsc/](https://docs.microsoft.com/powershell/dsc/) is for the Desired State Configuration feature</span></span>
- <span data-ttu-id="a2024-112">[/gallery/](https://docs.microsoft.com/powershell/gallery) — для [коллекции PowerShell](https://www.powershellgallery.com/);</span><span class="sxs-lookup"><span data-stu-id="a2024-112">[/gallery/](https://docs.microsoft.com/powershell/gallery) is for the [PowerShell Gallery](https://www.powershellgallery.com/)</span></span>
- <span data-ttu-id="a2024-113">[/jea/](https://docs.microsoft.com/powershell/jea/) — для функции Just Enough Administration (JEA);</span><span class="sxs-lookup"><span data-stu-id="a2024-113">[/jea/](https://docs.microsoft.com/powershell/jea/) is for the Just Enough Administration feature</span></span>
- <span data-ttu-id="a2024-114">[/reference/](https://docs.microsoft.com/powershell/scripting/) — для концептуальных статей по PowerShell и справочной документации по модулям для версий 3.0, 4.0, 5.0, 5.1 и 6.0.</span><span class="sxs-lookup"><span data-stu-id="a2024-114">[/reference/](https://docs.microsoft.com/powershell/scripting/) is for PowerShell conceptual topics and module reference across versions 3.0, 4.0, 5.0, 5.1, and 6.0</span></span>
  - <span data-ttu-id="a2024-115">Это содержимое также служит источником справочных сведений, выводимых с помощью командлета `Get-Help`.</span><span class="sxs-lookup"><span data-stu-id="a2024-115">This content is also the source of help content retrieved by the `Get-Help` cmdlet</span></span>
- <span data-ttu-id="a2024-116">[/wmf](https://docs.microsoft.com/powershell/wmf/readme) — содержит заметки о платформе Windows Management Framework (пакет, используемый для распространения новых версий PowerShell в предыдущих версиях Windows).</span><span class="sxs-lookup"><span data-stu-id="a2024-116">[/wmf](https://docs.microsoft.com/powershell/wmf/readme) contains release notes for the Windows Management Framework, the package used to distribute new versions of PowerShell to previous versions of Windows.</span></span>

## <a name="contributing"></a><span data-ttu-id="a2024-117">Публикация</span><span class="sxs-lookup"><span data-stu-id="a2024-117">Contributing</span></span>

<span data-ttu-id="a2024-118">Мы активно объединяем публикации в этом репозитории с помощью [запроса на включение внесенных изменений](https://help.github.com/articles/using-pull-requests/) в *промежуточной* ветви.</span><span class="sxs-lookup"><span data-stu-id="a2024-118">We actively merge contributions into this repository via [pull request](https://help.github.com/articles/using-pull-requests/) into the *staging* branch.</span></span>
<span data-ttu-id="a2024-119">Примечание. Для того, чтобы сообщество свободно использовало ваши публикации, перед отправкой запроса на включение внесенных изменений необходимо [подписать соглашение Contribution License Agreement](https://cla.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="a2024-119">Please note that before you submit a pull request you must [sign a Contribution License Agreement](https://cla.microsoft.com/) to ensure that the community is free to use your submissions.</span></span>

<span data-ttu-id="a2024-120">Дополнительные сведения о публикации можно прочесть в [руководстве по публикациям](CONTRIBUTING.md).</span><span class="sxs-lookup"><span data-stu-id="a2024-120">For more information on contributing, read our [contributor's guide](CONTRIBUTING.md).</span></span>
<span data-ttu-id="a2024-121">Руководство по публикациям содержит подробные сведения об участии в составлении документации и рекомендуемых инструментах, а также требования к стилю и форматированию.</span><span class="sxs-lookup"><span data-stu-id="a2024-121">The contributor's guide contains detail information about how to contribute documentation, suggested tools, and style and formatting requirements.</span></span>
<span data-ttu-id="a2024-122">Используйте шаблоны "Проблема" и "Запрос на включение внесенных изменений", чтобы обеспечить согласованность документации по разным версиям.</span><span class="sxs-lookup"><span data-stu-id="a2024-122">Please use the Issue and Pull Request templates to help keep documentation consistent across versions.</span></span>

## <a name="licenses"></a><span data-ttu-id="a2024-123">Лицензии</span><span class="sxs-lookup"><span data-stu-id="a2024-123">Licenses</span></span>

<span data-ttu-id="a2024-124">Существует два файла лицензии для этого проекта.</span><span class="sxs-lookup"><span data-stu-id="a2024-124">There are two license files for this project.</span></span>
<span data-ttu-id="a2024-125">Лицензия MIT применяется к коду, содержащемуся в этом репозитории.</span><span class="sxs-lookup"><span data-stu-id="a2024-125">The MIT License applies to the code contained in this repo.</span></span>
<span data-ttu-id="a2024-126">Лицензия Creative Commons применяется к документации.</span><span class="sxs-lookup"><span data-stu-id="a2024-126">The Creative Commons license applies to the documentation.</span></span>