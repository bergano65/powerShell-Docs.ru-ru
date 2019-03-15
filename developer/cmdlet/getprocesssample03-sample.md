---
title: Пример GetProcessSample03 | Документация Майкрософт
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: fc9d80ee-6ebd-48cd-a7ea-53cb2b442a22
caps.latest.revision: 6
ms.openlocfilehash: ec5a8c284dd3fa772261099281aba1fb68c49118
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2019
ms.locfileid: "56856480"
---
# <a name="getprocesssample03-sample"></a><span data-ttu-id="409aa-102">Пример командлета GetProcessSample03</span><span class="sxs-lookup"><span data-stu-id="409aa-102">GetProcessSample03 Sample</span></span>

<span data-ttu-id="409aa-103">В этом примере показано, как выполнить командлет, который извлекает процессы на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="409aa-103">This sample shows how to implement a cmdlet that retrieves the processes on the local computer.</span></span> <span data-ttu-id="409aa-104">Он предоставляет `Name` параметр, который может принять объект из конвейера или значения из свойства объекта, имя свойства совпадает с именем параметра.</span><span class="sxs-lookup"><span data-stu-id="409aa-104">It provides a `Name` parameter that can accept an object from the pipeline or a value from a property of an object whose property name is the same as the parameter name.</span></span> <span data-ttu-id="409aa-105">Этот командлет представляет упрощенную версию `Get-Process` командлет, предоставляемые Windows PowerShell 2.0.</span><span class="sxs-lookup"><span data-stu-id="409aa-105">This cmdlet is a simplified version of the `Get-Process` cmdlet provided by Windows PowerShell 2.0.</span></span>

## <a name="how-to-build-the-sample-using-visual-studio"></a><span data-ttu-id="409aa-106">Способы создания образца с использованием Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="409aa-106">How to build the sample using Visual Studio.</span></span>

1. <span data-ttu-id="409aa-107">С помощью Windows PowerShell 2.0 установлен пакет SDK перейдите к папке GetProcessSample03.</span><span class="sxs-lookup"><span data-stu-id="409aa-107">With the Windows PowerShell 2.0 SDK installed, navigate to the GetProcessSample03 folder.</span></span> <span data-ttu-id="409aa-108">Расположение по умолчанию — C:\Program Files (x86) \Microsoft SDKs\Windows\v7.0\Samples\sysmgmt\WindowsPowerShell\csharp\GetProcessSample03.</span><span class="sxs-lookup"><span data-stu-id="409aa-108">The default location is C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0\Samples\sysmgmt\WindowsPowerShell\csharp\GetProcessSample03.</span></span>

2. <span data-ttu-id="409aa-109">Дважды щелкните значок файла решения (SLN).</span><span class="sxs-lookup"><span data-stu-id="409aa-109">Double-click the icon for the solution (.sln) file.</span></span> <span data-ttu-id="409aa-110">Откроется пример проекта в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="409aa-110">This opens the sample project in Visual Studio.</span></span>

3. <span data-ttu-id="409aa-111">В **построения** меню, выберите **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="409aa-111">In the **Build** menu, select **Build Solution**.</span></span>

    <span data-ttu-id="409aa-112">Библиотеки для образца будет располагаться в папках \bin или \bin\debug по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="409aa-112">The library for the sample will be built in the default \bin or \bin\debug folders.</span></span>

### <a name="how-to-run-the-sample"></a><span data-ttu-id="409aa-113">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="409aa-113">How to run the sample</span></span>

1. <span data-ttu-id="409aa-114">Создайте следующую папку модуля:</span><span class="sxs-lookup"><span data-stu-id="409aa-114">Create the following module folder:</span></span>

    `[user]/documents/windowspowershell/modules/GetProcessSample03`

2. <span data-ttu-id="409aa-115">Скопируйте сборку образца в папке модуля.</span><span class="sxs-lookup"><span data-stu-id="409aa-115">Copy the sample assembly to the module folder.</span></span>

3. <span data-ttu-id="409aa-116">Запустите Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="409aa-116">Start Windows PowerShell.</span></span>

4. <span data-ttu-id="409aa-117">Выполните следующую команду, чтобы загрузить сборку в Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="409aa-117">Run the following command to load the assembly into Windows PowerShell:</span></span>

    `Import-module getprossessample03`

5. <span data-ttu-id="409aa-118">Выполните следующую команду, чтобы запустить командлет:</span><span class="sxs-lookup"><span data-stu-id="409aa-118">Run the following command to run the cmdlet:</span></span>

    `get-proc`

## <a name="requirements"></a><span data-ttu-id="409aa-119">Требования</span><span class="sxs-lookup"><span data-stu-id="409aa-119">Requirements</span></span>

<span data-ttu-id="409aa-120">В этом примере требуется Windows PowerShell 2.0.</span><span class="sxs-lookup"><span data-stu-id="409aa-120">This sample requires Windows PowerShell 2.0.</span></span>

## <a name="demonstrates"></a><span data-ttu-id="409aa-121">Демонстрация</span><span class="sxs-lookup"><span data-stu-id="409aa-121">Demonstrates</span></span>

<span data-ttu-id="409aa-122">В этом примере демонстрируется следующее.</span><span class="sxs-lookup"><span data-stu-id="409aa-122">This sample demonstrates the following.</span></span>

- <span data-ttu-id="409aa-123">Объявление класса командлет, используя атрибут командлета.</span><span class="sxs-lookup"><span data-stu-id="409aa-123">Declaring a cmdlet class using the Cmdlet attribute.</span></span>

- <span data-ttu-id="409aa-124">Объявление параметра командлета, с помощью параметра атрибута.</span><span class="sxs-lookup"><span data-stu-id="409aa-124">Declaring a cmdlet parameter using the Parameter attribute.</span></span>

- <span data-ttu-id="409aa-125">Задают позицию задаваемого параметра.</span><span class="sxs-lookup"><span data-stu-id="409aa-125">Specifying the position of the parameter.</span></span>

- <span data-ttu-id="409aa-126">Указание, что он принимает входные данные из конвейера.</span><span class="sxs-lookup"><span data-stu-id="409aa-126">Specifying that the parameter takes input from the pipeline.</span></span> <span data-ttu-id="409aa-127">Входные данные могут быть взяты из объекта или значение из свойства объекта, имя свойства совпадает с именем параметра.</span><span class="sxs-lookup"><span data-stu-id="409aa-127">The input can be taken from an object or a value from a property of an object whose property name is the same as the parameter name.</span></span>

- <span data-ttu-id="409aa-128">Объявление атрибута проверки для входного параметра.</span><span class="sxs-lookup"><span data-stu-id="409aa-128">Declaring a validation attribute for the parameter input.</span></span>

## <a name="example"></a><span data-ttu-id="409aa-129">Пример</span><span class="sxs-lookup"><span data-stu-id="409aa-129">Example</span></span>

<span data-ttu-id="409aa-130">В этом образце показана реализация командлет Get-Proc, который включает в себя `Name` параметр, который принимает входные данные из конвейера.</span><span class="sxs-lookup"><span data-stu-id="409aa-130">This sample shows an implementation of the Get-Proc cmdlet that includes a `Name` parameter that accepts input from the pipeline.</span></span>

```csharp
namespace Microsoft.Samples.PowerShell.Commands
{
  using System;
  using System.Diagnostics;
  using System.Management.Automation;           // Windows PowerShell namespace
  #region GetProcCommand

  /// <summary>
  /// This class implements the get-proc cmdlet.
  /// </summary>
  [Cmdlet(VerbsCommon.Get, "Proc")]
  public class GetProcCommand : Cmdlet
  {
    #region Parameters

    /// <summary>
    /// The names of the processes retrieved by the cmdlet.
    /// </summary>
    private string[] processNames;

    /// <summary>
    /// Gets or sets the names of the
    /// process that the cmdlet will retrieve.
    /// </summary>
    [Parameter(
               Position = 0,
               ValueFromPipeline = true,
               ValueFromPipelineByPropertyName = true)]
    [ValidateNotNullOrEmpty]
    public string[] Name
    {
      get { return this.processNames; }
      set { this.processNames = value; }
    }

    #endregion Parameters

    #region Cmdlet Overrides

    /// <summary>
    /// The ProcessRecord method calls the Process.GetProcesses
    /// method to retrieve the processes specified by the Name
    /// parameter. Then, the WriteObject method writes the
    /// associated processes to the pipeline.
    /// </summary>
    protected override void ProcessRecord()
    {
      // If no process names are passed to the cmdlet, get all
      // processes.
      if (this.processNames == null)
      {
        WriteObject(Process.GetProcesses(), true);
      }
      else
      {
        // If process names are passed to the cmdlet, get and write
        // the associated processes.
        foreach (string name in this.processNames)
        {
          WriteObject(Process.GetProcessesByName(name), true);
        }
      } // End if (processNames ...)
    } // End ProcessRecord.

    #endregion Overrides
  } // End GetProcCommand.
  #endregion GetProcCommand
}
```

## <a name="see-also"></a><span data-ttu-id="409aa-131">См. также</span><span class="sxs-lookup"><span data-stu-id="409aa-131">See Also</span></span>

[<span data-ttu-id="409aa-132">Запись командлета Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="409aa-132">Writing a Windows PowerShell Cmdlet</span></span>](./writing-a-windows-powershell-cmdlet.md)