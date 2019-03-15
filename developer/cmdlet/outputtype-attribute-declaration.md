---
title: Объявление атрибута OutputType | Документация Майкрософт
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: a97a98ee-ffc0-42f0-a9a6-b0717b39c798
caps.latest.revision: 5
ms.openlocfilehash: 7aa6fa407e509a31c4066c4f73ae01b02b2f338c
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2019
ms.locfileid: "56853720"
---
# <a name="outputtype-attribute-declaration"></a><span data-ttu-id="4b3f2-102">Объявление атрибута для типа выходных данных</span><span class="sxs-lookup"><span data-stu-id="4b3f2-102">OutputType Attribute Declaration</span></span>

<span data-ttu-id="4b3f2-103">`OutputType` Атрибут определяет типы .NET Framework, возвращаемые командлета, функции или сценарии.</span><span class="sxs-lookup"><span data-stu-id="4b3f2-103">The `OutputType` attribute identifies the .NET Framework types returned by a cmdlet, function, or script.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b3f2-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b3f2-104">Syntax</span></span>

```csharp
[OutputType(params string[] type)]
[OutputType(params Type[] type)]
[OutputType(params string[] type, Named Parameters...)]
[OutputType(params Type[] type, Named Parameters...)]
```

#### <a name="parameters"></a><span data-ttu-id="4b3f2-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b3f2-105">Parameters</span></span>

<span data-ttu-id="4b3f2-106">Тип (`string[]` или `Type[]`) требуется.</span><span class="sxs-lookup"><span data-stu-id="4b3f2-106">Type (`string[]` or `Type[]`) Required.</span></span> <span data-ttu-id="4b3f2-107">Указывает типы, возвращаемые функции командлета или сценария.</span><span class="sxs-lookup"><span data-stu-id="4b3f2-107">Specifies the types returned by the cmdlet function, or script.</span></span>

<span data-ttu-id="4b3f2-108">ParameterSetName (string[]) необязательно.</span><span class="sxs-lookup"><span data-stu-id="4b3f2-108">ParameterSetName (string[]) Optional.</span></span> <span data-ttu-id="4b3f2-109">Указывает наборы параметров, возвращающих типы, заданные в `type` параметра.</span><span class="sxs-lookup"><span data-stu-id="4b3f2-109">Specifies the parameter sets that return the types specified in the `type` parameter.</span></span>

<span data-ttu-id="4b3f2-110">providerCmdlet необязательно.</span><span class="sxs-lookup"><span data-stu-id="4b3f2-110">providerCmdlet Optional.</span></span> <span data-ttu-id="4b3f2-111">Указывает командлет поставщика, который возвращает типы, заданные в `type` параметра.</span><span class="sxs-lookup"><span data-stu-id="4b3f2-111">Specifies the provider cmdlet that returns the types specified in the `type` parameter.</span></span>

## <a name="see-also"></a><span data-ttu-id="4b3f2-112">См. также</span><span class="sxs-lookup"><span data-stu-id="4b3f2-112">See Also</span></span>

[<span data-ttu-id="4b3f2-113">Запись командлета Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="4b3f2-113">Writing a Windows PowerShell Cmdlet</span></span>](./writing-a-windows-powershell-cmdlet.md)