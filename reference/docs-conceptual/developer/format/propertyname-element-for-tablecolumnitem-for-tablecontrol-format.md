---
title: Элемент PropertyName для Таблеколумнитем для Таблеконтрол (Format) | Документация Майкрософт
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: fb26d72c-2f77-4801-badf-0537ccc55e31
caps.latest.revision: 10
ms.openlocfilehash: 6e86b6a0874b385703121802bc8108a0410442cd
ms.sourcegitcommit: 52a67bcd9d7bf3e8600ea4302d1fa8970ff9c998
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/15/2019
ms.locfileid: "72362253"
---
# <a name="propertyname-element-for-tablecolumnitem-for-tablecontrol-format"></a><span data-ttu-id="68bad-102">Элемент PropertyName для элемента TableColumnItem для элемента TableControl (формат)</span><span class="sxs-lookup"><span data-stu-id="68bad-102">PropertyName Element for TableColumnItem for TableControl (Format)</span></span>

<span data-ttu-id="68bad-103">Указывает свойство, значение которого отображается в столбце строки.</span><span class="sxs-lookup"><span data-stu-id="68bad-103">Specifies the property whose value is displayed in the column of the row.</span></span>

<span data-ttu-id="68bad-104">Элемент конфигурации (Format) Виевдефинитионс элемент (формат) элемент представления (Format) Таблеконтрол элемент (Format) Таблеровентриес элемент (Format) Таблеровентри элемент (Format) Таблеколумнитемс элемент (Format) Таблеколумнитем элемент (Format) Элемент PropertyName для Таблеколумнитем (Format)</span><span class="sxs-lookup"><span data-stu-id="68bad-104">Configuration Element (Format) ViewDefinitions Element (Format) View Element (Format) TableControl Element (Format) TableRowEntries Element (Format) TableRowEntry Element (Format) TableColumnItems Element (Format) TableColumnItem Element (Format) PropertyName Element for TableColumnItem (Format)</span></span>

## <a name="syntax"></a><span data-ttu-id="68bad-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68bad-105">Syntax</span></span>

```xml
<PropertyName>.NetTypeProperty</PropertyName>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="68bad-106">Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="68bad-106">Attributes and Elements</span></span>

<span data-ttu-id="68bad-107">В следующих разделах описываются атрибуты, дочерние элементы и родительский элемент элемента `PropertyName`.</span><span class="sxs-lookup"><span data-stu-id="68bad-107">The following sections describe attributes, child elements, and parent element of the `PropertyName` element.</span></span>

### <a name="attributes"></a><span data-ttu-id="68bad-108">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="68bad-108">Attributes</span></span>

<span data-ttu-id="68bad-109">Нет.</span><span class="sxs-lookup"><span data-stu-id="68bad-109">None.</span></span>

### <a name="child-elements"></a><span data-ttu-id="68bad-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="68bad-110">Child Elements</span></span>

<span data-ttu-id="68bad-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="68bad-111">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="68bad-112">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="68bad-112">Parent Elements</span></span>

|<span data-ttu-id="68bad-113">Элемент</span><span class="sxs-lookup"><span data-stu-id="68bad-113">Element</span></span>|<span data-ttu-id="68bad-114">Описание</span><span class="sxs-lookup"><span data-stu-id="68bad-114">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="68bad-115">Элемент Таблеколумнитем (Format)</span><span class="sxs-lookup"><span data-stu-id="68bad-115">TableColumnItem Element (Format)</span></span>](./tablecolumnitem-element-for-tablecolumnitems-for-tablecontrol-format.md)|<span data-ttu-id="68bad-116">Определяет свойство или скрипт, значение которого отображается в столбце строки.</span><span class="sxs-lookup"><span data-stu-id="68bad-116">Defines the property or script whose value is displayed in the column of the row.</span></span>|

## <a name="text-value"></a><span data-ttu-id="68bad-117">Текстовое значение</span><span class="sxs-lookup"><span data-stu-id="68bad-117">Text Value</span></span>

<span data-ttu-id="68bad-118">Укажите имя свойства, значение которого отображается.</span><span class="sxs-lookup"><span data-stu-id="68bad-118">Specify the name of the property whose value is displayed.</span></span>

## <a name="remarks"></a><span data-ttu-id="68bad-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="68bad-119">Remarks</span></span>

<span data-ttu-id="68bad-120">Дополнительные сведения о компонентах табличного представления см. в разделе [Создание табличного представления](./creating-a-table-view.md).</span><span class="sxs-lookup"><span data-stu-id="68bad-120">For more information about the components of a table view, see [Creating a Table View](./creating-a-table-view.md).</span></span>

## <a name="example"></a><span data-ttu-id="68bad-121">Пример</span><span class="sxs-lookup"><span data-stu-id="68bad-121">Example</span></span>

<span data-ttu-id="68bad-122">В этом примере показан элемент `TableColumnItem`, указывающий свойство `Status` объекта [System. Diagnostics. Process](/dotnet/api/System.Diagnostics.Process) .</span><span class="sxs-lookup"><span data-stu-id="68bad-122">This example shows a `TableColumnItem` element that specifies the `Status` property of the [System.Diagnostics.Process](/dotnet/api/System.Diagnostics.Process) object.</span></span>

```xml
<TableColumnItem>
   <Alignment>Centered</Alignment>
  <PropertyName>Status</PropertyName>
</TableColumnItem>

```

## <a name="see-also"></a><span data-ttu-id="68bad-123">См. также:</span><span class="sxs-lookup"><span data-stu-id="68bad-123">See Also</span></span>

[<span data-ttu-id="68bad-124">Создание табличного представления</span><span class="sxs-lookup"><span data-stu-id="68bad-124">Creating a Table View</span></span>](./creating-a-table-view.md)

[<span data-ttu-id="68bad-125">Элемент Таблеколумнитем (Format)</span><span class="sxs-lookup"><span data-stu-id="68bad-125">TableColumnItem Element (Format)</span></span>](./tablecolumnitem-element-for-tablecolumnitems-for-tablecontrol-format.md)

[<span data-ttu-id="68bad-126">Написание файла форматирования PowerShell</span><span class="sxs-lookup"><span data-stu-id="68bad-126">Writing a PowerShell Formatting File</span></span>](./writing-a-powershell-formatting-file.md)