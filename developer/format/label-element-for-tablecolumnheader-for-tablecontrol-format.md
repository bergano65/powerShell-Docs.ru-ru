---
title: Метка элемента для TableColumnHeader для TableControl (формат) | Документация Майкрософт
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 7196f039-2f6a-41fd-b252-5b1623ebb9f9
caps.latest.revision: 11
ms.openlocfilehash: 59dfd40b95d5088a711eb89cf101eb31a4b159f5
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2019
ms.locfileid: "56856090"
---
# <a name="label-element-for-tablecolumnheader-for-tablecontrol-format"></a><span data-ttu-id="716a2-102">Элемент Label для элемента TableColumnHeader для элемента TableControl (формат)</span><span class="sxs-lookup"><span data-stu-id="716a2-102">Label Element for TableColumnHeader for TableControl (Format)</span></span>

<span data-ttu-id="716a2-103">Определяет метку, которая отображается в верхней части столбца.</span><span class="sxs-lookup"><span data-stu-id="716a2-103">Defines the label that is displayed at the top of a column.</span></span> <span data-ttu-id="716a2-104">Этот элемент используется при определении представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="716a2-104">This element is used when defining a table view.</span></span>

<span data-ttu-id="716a2-105">Элемент (формат) элемент ViewDefinitions (формат) представление элемент (формат) TableControl-элемент (формат) TableHeaders элемент конфигурации для элемента TableColumnHeader TableControl (формат) для TableHeaders для метки элемента TableControl (формат) TableColumnHeader для TablControl (формат)</span><span class="sxs-lookup"><span data-stu-id="716a2-105">Configuration Element (Format) ViewDefinitions Element (Format) View Element (Format) TableControl Element (Format) TableHeaders Element for TableControl (Format) TableColumnHeader Element for TableHeaders for TableControl (Format) Label Element  for TableColumnHeader for TablControl (Format)</span></span>

## <a name="syntax"></a><span data-ttu-id="716a2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="716a2-106">Syntax</span></span>

```xml
<Label>DisplayedLabel</Label>

```

## <a name="attributes-and-elements"></a><span data-ttu-id="716a2-107">Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="716a2-107">Attributes and Elements</span></span>

<span data-ttu-id="716a2-108">В следующих разделах атрибуты, дочерние элементы и родительский элемент `Label` элемент.</span><span class="sxs-lookup"><span data-stu-id="716a2-108">The following sections describe the attributes, child elements, and the parent element of the `Label` element.</span></span> <span data-ttu-id="716a2-109">Для каждого столбца можно использовать только одну метку.</span><span class="sxs-lookup"><span data-stu-id="716a2-109">Only one label is allowed for each column.</span></span>

### <a name="attributes"></a><span data-ttu-id="716a2-110">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="716a2-110">Attributes</span></span>

<span data-ttu-id="716a2-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="716a2-111">None.</span></span>

### <a name="child-elements"></a><span data-ttu-id="716a2-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="716a2-112">Child Elements</span></span>

<span data-ttu-id="716a2-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="716a2-113">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="716a2-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="716a2-114">Parent Elements</span></span>

|<span data-ttu-id="716a2-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="716a2-115">Element</span></span>|<span data-ttu-id="716a2-116">Описание</span><span class="sxs-lookup"><span data-stu-id="716a2-116">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="716a2-117">Элемент TableColumnHeader для TableHeaders для TableControl (формат)</span><span class="sxs-lookup"><span data-stu-id="716a2-117">TableColumnHeader Element for TableHeaders for TableControl  (Format)</span></span>](./tablecolumnheader-element-format.md)|<span data-ttu-id="716a2-118">Определяет метку, ширину и выравнивания данных для столбца таблицы.</span><span class="sxs-lookup"><span data-stu-id="716a2-118">Defines a label, the width, and the alignment of the data for a column of the table.</span></span>|

## <a name="text-value"></a><span data-ttu-id="716a2-119">Текстовое значение</span><span class="sxs-lookup"><span data-stu-id="716a2-119">Text Value</span></span>

<span data-ttu-id="716a2-120">Укажите текст, отображаемый в верхней части столбца таблицы.</span><span class="sxs-lookup"><span data-stu-id="716a2-120">Specify the text that is displayed at the top of the column of the table.</span></span> <span data-ttu-id="716a2-121">Существуют не запрещенные знаки для метки столбца.</span><span class="sxs-lookup"><span data-stu-id="716a2-121">There are no restricted characters for the column label.</span></span>

## <a name="remarks"></a><span data-ttu-id="716a2-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="716a2-122">Remarks</span></span>

<span data-ttu-id="716a2-123">Если метка не указана, используется имя свойства, значение которого отображается в строках.</span><span class="sxs-lookup"><span data-stu-id="716a2-123">If no label is specified, the name of the property whose value is displayed in the rows is used.</span></span>

<span data-ttu-id="716a2-124">Дополнительные сведения о компонентах в табличное представление, см. в разделе [Создание представления таблицы](./creating-a-table-view.md).</span><span class="sxs-lookup"><span data-stu-id="716a2-124">For more information about the components of a table view, see [Creating a Table View](./creating-a-table-view.md).</span></span>

## <a name="example"></a><span data-ttu-id="716a2-125">Пример</span><span class="sxs-lookup"><span data-stu-id="716a2-125">Example</span></span>

<span data-ttu-id="716a2-126">В этом примере показано `TableColumnHeader` элемент, метка которого является «Столбец 1».</span><span class="sxs-lookup"><span data-stu-id="716a2-126">This example shows a `TableColumnHeader` element whose label is "Column 1".</span></span>

```xml
<TableColumnHeader>
  <Label>Column 1</Label)
  <Width>16</Width>
  <Alignment>Left</Alignment>
</TableColumnHeader>
```

## <a name="see-also"></a><span data-ttu-id="716a2-127">См. также</span><span class="sxs-lookup"><span data-stu-id="716a2-127">See Also</span></span>

[<span data-ttu-id="716a2-128">Создание представления таблицы</span><span class="sxs-lookup"><span data-stu-id="716a2-128">Creating a Table View</span></span>](./creating-a-table-view.md)

[<span data-ttu-id="716a2-129">Элемент TableColumnHeader (формат)</span><span class="sxs-lookup"><span data-stu-id="716a2-129">TableColumnHeader Element (Format)</span></span>](./tablecolumnheader-element-format.md)

[<span data-ttu-id="716a2-130">Запись файла форматирования PowerShell</span><span class="sxs-lookup"><span data-stu-id="716a2-130">Writing a PowerShell Formatting File</span></span>](./writing-a-powershell-formatting-file.md)