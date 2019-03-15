---
title: TableControl-элемент (формат) | Документация Майкрософт
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 1550b068-dfbc-4ae0-9aa1-72c9a680ec59
caps.latest.revision: 15
ms.openlocfilehash: dd48e82452e83f93e2e005c9db53bbc51d8b2eb4
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2019
ms.locfileid: "56858920"
---
# <a name="tablecontrol-element-format"></a><span data-ttu-id="65441-102">Элемент TableControl (формат)</span><span class="sxs-lookup"><span data-stu-id="65441-102">TableControl Element (Format)</span></span>

<span data-ttu-id="65441-103">Определяет формат таблицы для представления.</span><span class="sxs-lookup"><span data-stu-id="65441-103">Defines a table format for a view.</span></span>

<span data-ttu-id="65441-104">TableControl-элемент элемента (формат) элемент ViewDefinitions (формат) представления (формат)</span><span class="sxs-lookup"><span data-stu-id="65441-104">ViewDefinitions Element (Format) View Element (Format) TableControl Element (Format)</span></span>

## <a name="syntax"></a><span data-ttu-id="65441-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65441-105">Syntax</span></span>

```xml
<TableControl>
  <AutoSize/>
  <HideTableHeaders/>
  <TableHeaders>...</TableHeaders>
  <TableRowEntries>...</TableRowEntries>
</TableControl>

```

## <a name="attributes-and-elements"></a><span data-ttu-id="65441-106">Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="65441-106">Attributes and Elements</span></span>

<span data-ttu-id="65441-107">Ниже описаны атрибуты, дочерние элементы и родительский элемент `TableControl` элемент.</span><span class="sxs-lookup"><span data-stu-id="65441-107">The following sections describe attributes, child elements, and parent element of the `TableControl` element.</span></span> <span data-ttu-id="65441-108">Необходимо указать строки таблицы.</span><span class="sxs-lookup"><span data-stu-id="65441-108">You must specify the rows of the table.</span></span> <span data-ttu-id="65441-109">Все дочерние элементы являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="65441-109">All other child elements are optional.</span></span>

### <a name="attributes"></a><span data-ttu-id="65441-110">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="65441-110">Attributes</span></span>

<span data-ttu-id="65441-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="65441-111">None.</span></span>

### <a name="child-elements"></a><span data-ttu-id="65441-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="65441-112">Child Elements</span></span>

|<span data-ttu-id="65441-113">Элемент</span><span class="sxs-lookup"><span data-stu-id="65441-113">Element</span></span>|<span data-ttu-id="65441-114">Описание</span><span class="sxs-lookup"><span data-stu-id="65441-114">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="65441-115">AutoSize-элемент для TableControl (формат)</span><span class="sxs-lookup"><span data-stu-id="65441-115">AutoSize Element for TableControl (Format)</span></span>](./autosize-element-for-tablecontrol-format.md)|<span data-ttu-id="65441-116">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="65441-116">Optional element.</span></span><br /><br /> <span data-ttu-id="65441-117">Указывает ли размер столбца и количество столбцов изменить в зависимости от объема данных.</span><span class="sxs-lookup"><span data-stu-id="65441-117">Specifies whether the column size and the number of columns are adjusted based on the size of the data.</span></span>|
|[<span data-ttu-id="65441-118">Элемент HideTableHeaders для TableControl (формат)</span><span class="sxs-lookup"><span data-stu-id="65441-118">HideTableHeaders Element for TableControl (Format)</span></span>](./hidetableheaders-element-format.md)|<span data-ttu-id="65441-119">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="65441-119">Optional element.</span></span><br /><br /> <span data-ttu-id="65441-120">Указывает, отображается ли заголовок таблицы.</span><span class="sxs-lookup"><span data-stu-id="65441-120">Indicates whether the header of the table is not displayed.</span></span>|
|[<span data-ttu-id="65441-121">Элемент TableHeaders для TableControl (формат)</span><span class="sxs-lookup"><span data-stu-id="65441-121">TableHeaders Element for TableControl (Format)</span></span>](./tableheaders-element-format.md)|<span data-ttu-id="65441-122">Обязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="65441-122">Required element.</span></span><br /><br /> <span data-ttu-id="65441-123">Определяет, метки, значения ширины и выравнивания данных для столбцов представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="65441-123">Defines the labels, the widths, and the alignment of the data for the columns of the table view.</span></span>|
|[<span data-ttu-id="65441-124">Элемент TableRowEntries для TableCotrol (формат)</span><span class="sxs-lookup"><span data-stu-id="65441-124">TableRowEntries Element for TableCotrol (Format)</span></span>](./tablerowentries-element-for-tablecontrol-format.md)|<span data-ttu-id="65441-125">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="65441-125">Optional element.</span></span><br /><br /> <span data-ttu-id="65441-126">Предоставляет определения представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="65441-126">Provides the definitions of the table view.</span></span>|

### <a name="parent-elements"></a><span data-ttu-id="65441-127">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="65441-127">Parent Elements</span></span>

|<span data-ttu-id="65441-128">Элемент</span><span class="sxs-lookup"><span data-stu-id="65441-128">Element</span></span>|<span data-ttu-id="65441-129">Описание</span><span class="sxs-lookup"><span data-stu-id="65441-129">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="65441-130">Элемент представления (формат)</span><span class="sxs-lookup"><span data-stu-id="65441-130">View Element (Format)</span></span>](./view-element-format.md)|<span data-ttu-id="65441-131">Определяет представление, которое используется для отображения элементов из одного или нескольких объектов.</span><span class="sxs-lookup"><span data-stu-id="65441-131">Defines a view that is used to display the members of one or more objects.</span></span>|

## <a name="remarks"></a><span data-ttu-id="65441-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="65441-132">Remarks</span></span>

<span data-ttu-id="65441-133">Дополнительные сведения о компонентах в табличное представление, см. в разделе [Создание представления таблицы](./creating-a-table-view.md).</span><span class="sxs-lookup"><span data-stu-id="65441-133">For more information about the components of a table view, see [Creating a Table View](./creating-a-table-view.md).</span></span>

## <a name="example"></a><span data-ttu-id="65441-134">Пример</span><span class="sxs-lookup"><span data-stu-id="65441-134">Example</span></span>

<span data-ttu-id="65441-135">В этом примере показано `TableControl` элемент, который используется для отображения свойств [System.Serviceprocess.Servicecontroller](/dotnet/api/System.ServiceProcess.ServiceController) объекта.</span><span class="sxs-lookup"><span data-stu-id="65441-135">This example shows a `TableControl` element that is used to display the properties of the [System.Serviceprocess.Servicecontroller](/dotnet/api/System.ServiceProcess.ServiceController) object.</span></span>

```xml
<View>
  <Name>service</Name>
  <ViewSelectedBy>
    <TypeName>System.ServiceProcess.ServiceController</TypeName>
  </ViewSelectedBy>
  <TableControl>
    <TableHeaders>...</TableHeaders>
    <TableRowEntries>...</TableRowEntries>
  </TableControl>
</View>

```

## <a name="see-also"></a><span data-ttu-id="65441-136">См. также</span><span class="sxs-lookup"><span data-stu-id="65441-136">See Also</span></span>

[<span data-ttu-id="65441-137">Создание представления таблицы</span><span class="sxs-lookup"><span data-stu-id="65441-137">Creating a Table View</span></span>](./creating-a-table-view.md)

[<span data-ttu-id="65441-138">Элемент представления (формат)</span><span class="sxs-lookup"><span data-stu-id="65441-138">View Element (Format)</span></span>](./view-element-format.md)

[<span data-ttu-id="65441-139">AutoSize-элемент для TableControl (формат)</span><span class="sxs-lookup"><span data-stu-id="65441-139">AutoSize Element for TableControl (Format)</span></span>](./autosize-element-for-tablecontrol-format.md)

[<span data-ttu-id="65441-140">Элемент HideTableHeaders (формат)</span><span class="sxs-lookup"><span data-stu-id="65441-140">HideTableHeaders Element (Format)</span></span>](./hidetableheaders-element-format.md)

[<span data-ttu-id="65441-141">Элемент TableHeaders (формат)</span><span class="sxs-lookup"><span data-stu-id="65441-141">TableHeaders Element (Format)</span></span>](./tableheaders-element-format.md)

[<span data-ttu-id="65441-142">Элемент TableRowEntries (формат)</span><span class="sxs-lookup"><span data-stu-id="65441-142">TableRowEntries Element (Format)</span></span>](./tablerowentries-element-for-tablecontrol-format.md)

[<span data-ttu-id="65441-143">Запись файла форматирования PowerShell</span><span class="sxs-lookup"><span data-stu-id="65441-143">Writing a PowerShell Formatting File</span></span>](./writing-a-powershell-formatting-file.md)