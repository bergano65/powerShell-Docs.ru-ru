---
title: Пример кода AccessDbProviderSample06 | Документация Майкрософт
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: baab6a56-c199-48d7-a03e-a904b1bb1baa
caps.latest.revision: 7
ms.openlocfilehash: 7f75a3a3d2ab89696bb34ec2fdf7ba7a5ce0f9b1
ms.sourcegitcommit: debd2b38fb8070a7357bf1a4bf9cc736f3702f31
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2019
ms.locfileid: "74416236"
---
# <a name="accessdbprovidersample06-code-sample"></a>Пример кода AccessDbProviderSample06

В следующем коде показана реализация поставщика содержимого Windows PowerShell, описанного в статье [Создание поставщика содержимого Windows PowerShell](./creating-a-windows-powershell-content-provider.md). Этот поставщик позволяет пользователю управлять содержимым элементов в хранилище данных.

> [!NOTE]
> C# Исходный файл (AccessDBSampleProvider06.cs) для этого поставщика можно скачать с помощью пакета средств разработки программного обеспечения Microsoft Windows для компонентов среды выполнения Windows Vista и Microsoft .NET Framework 3,0. Инструкции по загрузке см. в статье [Установка Windows PowerShell и Загрузка пакета SDK для Windows PowerShell](/powershell/scripting/developer/installing-the-windows-powershell-sdk).
>
> Скачанные исходные файлы доступны в **\<примеров PowerShell >** Directory.
>
> Дополнительные сведения о других реализациях поставщиков Windows PowerShell см. в разделе [Разработка поставщика Windows PowerShell](./designing-your-windows-powershell-provider.md).

## <a name="code-sample"></a>Образец кода

[!code-csharp[AccessDBProviderSample06.cs](../../../../powershell-sdk-samples/SDK-2.0/csharp/AccessDBProviderSample06/AccessDBProviderSample06.cs#L11-L2399 "AccessDBProviderSample06.cs")]

## <a name="see-also"></a>См. также:

[Руководством программиста Windows PowerShell](./windows-powershell-programmer-s-guide.md)

[Пакет SDK для Windows PowerShell](../windows-powershell-reference.md)
