---
title: Пример кода RunSpace09 | Документация Майкрософт
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 136e451f-767b-42e0-bd6f-6486693abd5e
caps.latest.revision: 6
ms.openlocfilehash: 122a40dea93d874a7c131774e3d1abb148bcd4fc
ms.sourcegitcommit: 52a67bcd9d7bf3e8600ea4302d1fa8970ff9c998
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/15/2019
ms.locfileid: "72360133"
---
# <a name="runspace09-code-sample"></a><span data-ttu-id="bef42-102">Примеры кода RunSpace09</span><span class="sxs-lookup"><span data-stu-id="bef42-102">RunSpace09 Code Sample</span></span>

<span data-ttu-id="bef42-103">Ниже приведен исходный код для примера Runspace09, описанного в разделе [Создание консольного приложения, которое вызывает конвейер асинхронно](https://msdn.microsoft.com/en-us/198c1c94-2a06-457e-93ce-c0d910618e47).</span><span class="sxs-lookup"><span data-stu-id="bef42-103">Here is the source code for the Runspace09 sample described in [Creating a Console Application That Invokes a Pipeline Asynchronously](https://msdn.microsoft.com/en-us/198c1c94-2a06-457e-93ce-c0d910618e47).</span></span> <span data-ttu-id="bef42-104">Этот пример приложения создает и открывает пространство выполнения, создает и асинхронно вызывает конвейер, а затем использует события конвейера для асинхронной обработки скрипта.</span><span class="sxs-lookup"><span data-stu-id="bef42-104">This sample application creates and opens a runspace, creates and asynchronously invokes a pipeline, and then uses pipeline events to process the script asynchronously.</span></span> <span data-ttu-id="bef42-105">Скрипт, выполняемый этим приложением, создает целые числа от 1 до 10 в 0,5-секундном интервале (500 мс).</span><span class="sxs-lookup"><span data-stu-id="bef42-105">The script that is run by this application creates the integers 1 through 10 in 0.5-second intervals (500 ms).</span></span>

## <a name="code-sample"></a><span data-ttu-id="bef42-106">Пример кода</span><span class="sxs-lookup"><span data-stu-id="bef42-106">Code Sample</span></span>

[!code-csharp[Runspace09.cs](../../../../powershell-sdk-samples/SDK-2.0/csharp/Runspace09/Runspace09.cs#L11-L113 "Runspace09.cs")]

## <a name="see-also"></a><span data-ttu-id="bef42-107">См. также:</span><span class="sxs-lookup"><span data-stu-id="bef42-107">See Also</span></span>

[<span data-ttu-id="bef42-108">Пакет SDK для Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="bef42-108">Windows PowerShell SDK</span></span>](../windows-powershell-reference.md)