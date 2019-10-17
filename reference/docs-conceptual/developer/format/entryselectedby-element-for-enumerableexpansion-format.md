---
title: Элемент Ентриселектедби для Енумерабликспансион (Format) | Документация Майкрософт
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 3af6aff8-4c2d-4f08-9bb1-e1f3ed3e583e
caps.latest.revision: 11
ms.openlocfilehash: 6a371bdbb85d07730c32931a4a79ee40856ce298
ms.sourcegitcommit: 52a67bcd9d7bf3e8600ea4302d1fa8970ff9c998
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/15/2019
ms.locfileid: "72368803"
---
# <a name="entryselectedby-element-for-enumerableexpansion-format"></a><span data-ttu-id="e5d32-102">Элемент EntrySelectedBy для элемента EnumerableExpansion (формат)</span><span class="sxs-lookup"><span data-stu-id="e5d32-102">EntrySelectedBy Element for EnumerableExpansion (Format)</span></span>

<span data-ttu-id="e5d32-103">Определяет типы .NET, которые используют это определение, или условие, которое должно существовать, чтобы использовать это определение.</span><span class="sxs-lookup"><span data-stu-id="e5d32-103">Defines the .NET types that use this definition or the condition that must exist for this definition to be used.</span></span>

<span data-ttu-id="e5d32-104">Элемент конфигурации (Format) Дефаултсеттингс элемент (Format) Енумерабликспансионс элемент (Format) Енумерабликспансион элемент (Format) Ентриселектедби для Енумерабликспансион (Format)</span><span class="sxs-lookup"><span data-stu-id="e5d32-104">Configuration Element (Format) DefaultSettings Element (Format) EnumerableExpansions Element (Format) EnumerableExpansion Element (Format) EntrySelectedBy Element for EnumerableExpansion (Format)</span></span>

## <a name="syntax"></a><span data-ttu-id="e5d32-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5d32-105">Syntax</span></span>

```xml
<EntrySelectedBy>
  <TypeName>Nameof.NetType</TypeName>
  <SelectionSetName>NameofSelectionSet</SelectionSetName>
  <SelectionCondition>...</SelectionCondition>
</EntrySelectedBy>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="e5d32-106">Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="e5d32-106">Attributes and Elements</span></span>

<span data-ttu-id="e5d32-107">В следующих разделах описываются атрибуты, дочерние элементы и родительский элемент элемента `EntrySelectedBy`.</span><span class="sxs-lookup"><span data-stu-id="e5d32-107">The following sections describe attributes, child elements, and the parent element of the `EntrySelectedBy` element.</span></span>

### <a name="attributes"></a><span data-ttu-id="e5d32-108">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e5d32-108">Attributes</span></span>

<span data-ttu-id="e5d32-109">Нет.</span><span class="sxs-lookup"><span data-stu-id="e5d32-109">None.</span></span>

### <a name="child-elements"></a><span data-ttu-id="e5d32-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e5d32-110">Child Elements</span></span>

|<span data-ttu-id="e5d32-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="e5d32-111">Element</span></span>|<span data-ttu-id="e5d32-112">Описание</span><span class="sxs-lookup"><span data-stu-id="e5d32-112">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="e5d32-113">Элемент Селектионкондитион для Ентриселектедби для Енумерабликспансион (Format)</span><span class="sxs-lookup"><span data-stu-id="e5d32-113">SelectionCondition Element for EntrySelectedBy for EnumerableExpansion (Format)</span></span>](./selectioncondition-element-for-entryselectedby-for-enumerableexpansion-format.md)|<span data-ttu-id="e5d32-114">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="e5d32-114">Optional element.</span></span><br /><br /> <span data-ttu-id="e5d32-115">Определяет условие, которое должно существовать для расширения объектов коллекции этого определения.</span><span class="sxs-lookup"><span data-stu-id="e5d32-115">Defines the condition that must exist to expand the collection objects of this definition.</span></span>|
|[<span data-ttu-id="e5d32-116">Элемент Селектионсетнаме для Ентриселектедби для Енумерабликспансион (Format)</span><span class="sxs-lookup"><span data-stu-id="e5d32-116">SelectionSetName Element for EntrySelectedBy for EnumerableExpansion (Format)</span></span>](./selectionsetname-element-for-entryselectedby-for-enumerableexpansion-format.md)|<span data-ttu-id="e5d32-117">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="e5d32-117">Optional element.</span></span><br /><br /> <span data-ttu-id="e5d32-118">Задает набор типов .NET, использующих это определение того, как разворачиваются объекты коллекции.</span><span class="sxs-lookup"><span data-stu-id="e5d32-118">Specifies a set of .NET types that use this definition of how collection objects are expanded.</span></span>|
|[<span data-ttu-id="e5d32-119">Элемент TypeName для Ентриселектедби для Енумерабликспансион (Format)</span><span class="sxs-lookup"><span data-stu-id="e5d32-119">TypeName Element for EntrySelectedBy for EnumerableExpansion (Format)</span></span>](./typename-element-for-entryselectedby-for-enumerableexpansion-format.md)|<span data-ttu-id="e5d32-120">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="e5d32-120">Optional element.</span></span><br /><br /> <span data-ttu-id="e5d32-121">Указывает тип .NET, использующий это определение того, как разворачиваются объекты коллекции.</span><span class="sxs-lookup"><span data-stu-id="e5d32-121">Specifies a .NET type that uses this definition of how collection objects are expanded.</span></span>|

### <a name="parent-elements"></a><span data-ttu-id="e5d32-122">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="e5d32-122">Parent Elements</span></span>

|<span data-ttu-id="e5d32-123">Элемент</span><span class="sxs-lookup"><span data-stu-id="e5d32-123">Element</span></span>|<span data-ttu-id="e5d32-124">Описание</span><span class="sxs-lookup"><span data-stu-id="e5d32-124">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="e5d32-125">Элемент Енумерабликспансион (Format)</span><span class="sxs-lookup"><span data-stu-id="e5d32-125">EnumerableExpansion Element (Format)</span></span>](./enumerableexpansion-element-format.md)|<span data-ttu-id="e5d32-126">Определяет, каким способом развертываются определенные объекты коллекции .NET, когда они отображаются в представлении.</span><span class="sxs-lookup"><span data-stu-id="e5d32-126">Defines how specific .NET collection objects are expanded when they are displayed in a view.</span></span>|

## <a name="remarks"></a><span data-ttu-id="e5d32-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="e5d32-127">Remarks</span></span>

<span data-ttu-id="e5d32-128">Необходимо указать по крайней мере один тип, набор выбора или условие выбора для записи определения.</span><span class="sxs-lookup"><span data-stu-id="e5d32-128">You must specify at least one type, selection set, or selection condition for a definition entry.</span></span> <span data-ttu-id="e5d32-129">Максимальное количество дочерних элементов, которое можно использовать, не ограничено.</span><span class="sxs-lookup"><span data-stu-id="e5d32-129">There is no maximum limit to the number of child elements that you can use.</span></span>

<span data-ttu-id="e5d32-130">Условия выбора используются для определения условия, которое должно существовать, чтобы использовать определение, например, если объект имеет определенное свойство или значение конкретного свойства или скрипта равно `true`.</span><span class="sxs-lookup"><span data-stu-id="e5d32-130">Selection conditions are used to define a condition that must exist for the definition to be used, such as when an object has a specific property or that a specific property value or script evaluates to `true`.</span></span> <span data-ttu-id="e5d32-131">Дополнительные сведения об условиях выбора см. в разделе [Определение условий для отображения данных](./defining-conditions-for-displaying-data.md).</span><span class="sxs-lookup"><span data-stu-id="e5d32-131">For more information about selection conditions, see [Defining Conditions for Displaying Data](./defining-conditions-for-displaying-data.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e5d32-132">См. также:</span><span class="sxs-lookup"><span data-stu-id="e5d32-132">See Also</span></span>

[<span data-ttu-id="e5d32-133">Определение условий для отображения данных</span><span class="sxs-lookup"><span data-stu-id="e5d32-133">Defining Conditions for Displaying Data</span></span>](./defining-conditions-for-displaying-data.md)

[<span data-ttu-id="e5d32-134">Элемент Енумерабликспансион (Format)</span><span class="sxs-lookup"><span data-stu-id="e5d32-134">EnumerableExpansion Element (Format)</span></span>](./enumerableexpansion-element-format.md)

[<span data-ttu-id="e5d32-135">Элемент Селектионкондитион для Ентриселектедби для Енумерабликспансион (Format)</span><span class="sxs-lookup"><span data-stu-id="e5d32-135">SelectionCondition Element for EntrySelectedBy for EnumerableExpansion (Format)</span></span>](./selectioncondition-element-for-entryselectedby-for-enumerableexpansion-format.md)

[<span data-ttu-id="e5d32-136">Элемент Селектионсетнаме для Ентриселектедби для Енумерабликспансион (Format)</span><span class="sxs-lookup"><span data-stu-id="e5d32-136">SelectionSetName Element for EntrySelectedBy for EnumerableExpansion (Format)</span></span>](./selectionsetname-element-for-entryselectedby-for-enumerableexpansion-format.md)

[<span data-ttu-id="e5d32-137">Элемент TypeName для Ентриселектедби для Енумерабликспансион (Format)</span><span class="sxs-lookup"><span data-stu-id="e5d32-137">TypeName Element for EntrySelectedBy for EnumerableExpansion (Format)</span></span>](./typename-element-for-entryselectedby-for-enumerableexpansion-format.md)

[<span data-ttu-id="e5d32-138">Написание файла форматирования PowerShell</span><span class="sxs-lookup"><span data-stu-id="e5d32-138">Writing a PowerShell Formatting File</span></span>](./writing-a-powershell-formatting-file.md)