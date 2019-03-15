---
title: Способы тестирования обновляемой справки | Документация Майкрософт
ms.custom: ''
ms.date: 09/12/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 3e064048-2b94-4365-bdb7-f1ee7c0a7fd7
caps.latest.revision: 6
ms.openlocfilehash: cecc6c26ccaece06462ddd74b53534137fcf3037
ms.sourcegitcommit: 5990f04b8042ef2d8e571bec6d5b051e64c9921c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/12/2019
ms.locfileid: "57794269"
---
# <a name="how-to-test-updatable-help"></a><span data-ttu-id="95784-102">Как проверить обновляемую справку</span><span class="sxs-lookup"><span data-stu-id="95784-102">How to Test Updatable Help</span></span>

<span data-ttu-id="95784-103">В этом разделе описаны подходы к тестированию обновляемую справку для модуля.</span><span class="sxs-lookup"><span data-stu-id="95784-103">This topic describes approaches to testing Updatable Help for a module.</span></span>

## <a name="using-verbose-to-detect-errors"></a><span data-ttu-id="95784-104">С помощью подробного для обнаружения ошибок</span><span class="sxs-lookup"><span data-stu-id="95784-104">Using Verbose to Detect Errors</span></span>

<span data-ttu-id="95784-105">После отправки XML-файл HelpInfo и CAB-файлы для вашего модуля, проверить файлы, запустив [Update-Help](/powershell/module/Microsoft.PowerShell.Core/Update-Help) с **Verbose** параметра.</span><span class="sxs-lookup"><span data-stu-id="95784-105">After uploading the HelpInfo XML file and CAB files for your module, test the files by running an [Update-Help](/powershell/module/Microsoft.PowerShell.Core/Update-Help) command with the **Verbose** parameter.</span></span> <span data-ttu-id="95784-106">**Verbose** параметр направляет `Update-Help` сообщить о важных этапов его действия, от чтения **HelpInfoUri** ключа в манифесте модуля к проверке типов файлов в распакованную CAB-файл и поместить файлы в каталоге модуля для конкретного языка.</span><span class="sxs-lookup"><span data-stu-id="95784-106">The **Verbose** parameter directs `Update-Help` to report the critical steps in its actions, from reading the **HelpInfoUri** key in the module manifest to validating the file types in the unpacked CAB file and placing the files in the language-specific module directory.</span></span>

<span data-ttu-id="95784-107">При разрешении все подробные сообщения, запустите `Update-Help` с **Отладка** параметра.</span><span class="sxs-lookup"><span data-stu-id="95784-107">When all verbose messages are resolved, run an `Update-Help` command with the **Debug** parameter.</span></span> <span data-ttu-id="95784-108">Этот параметр определяет всех оставшихся проблем с обновляемых файлов справки.</span><span class="sxs-lookup"><span data-stu-id="95784-108">This parameter should detect any remaining problems with the Updatable Help files.</span></span>