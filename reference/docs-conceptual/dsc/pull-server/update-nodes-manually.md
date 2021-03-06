---
ms.date: 06/12/2017
keywords: dsc,powershell,конфигурация,установка
title: Обновление узлов на опрашиваемом сервере
ms.openlocfilehash: fa59a2f6574db2dbc96621be4326f1d5a55e5de9
ms.sourcegitcommit: 30ccbbb32915b551c4cd4c91ef1df96b5b7514c4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2020
ms.locfileid: "80500662"
---
# <a name="update-nodes-from-a-pull-server"></a>Обновление узлов на опрашиваемом сервере

В следующих разделах предполагается, что вы уже настроили опрашиваемый сервер. Если вы не настроили опрашиваемый сервер, можно воспользоваться следующими руководствами.

- [Настройка опрашиваемого SMB-сервера DSC](pullServerSmb.md)
- [Настройка опрашиваемого HTTP-сервера DSC](pullServer.md)

Для каждого целевого узла можно настроить скачивание конфигураций, ресурсов и даже отчет о состоянии. В этой статье показано, как передать ресурсы, чтобы они были доступны для загрузки, и настроить клиенты, чтобы ресурсы загружались автоматически. Когда Узел получает назначенную конфигурацию с помощью команды **получить** или **отправить** (v5), он автоматически загружает любые ресурсы, требуемые конфигурацией, из расположения, указанного в LCM.

## <a name="using-the-update-dscconfiguration-cmdlet"></a>Использование командлета Update-DSCConfiguration

Начиная с PowerShell 5.0, командлет [Update-DSCConfiguration](/powershell/module/psdesiredstateconfiguration/update-dscconfiguration) принуждает узел обновлять свою конфигурацию с опрашиваемого сервера, настроенного в LCM.

```powershell
Update-DSCConfiguration -ComputerName "Server01"
```

## <a name="using-invoke-cimmethod"></a>Использование Invoke-CimMethod

В PowerShell 4.0 вы по прежнему можете вручную заставить клиента — получателя данных обновить свою конфигурацию, используя [Invoke-CIMMethod](/powershell/module/cimcmdlets/invoke-cimmethod). В следующем примере создается сеанс CIM с указанными учетными данными, который вызывает соответствующий метод CIM и удаляет сеанс.

```powershell
$cimSession = New-CimSession -ComputerName "Server01" -Credential $(Get-Credential)
Invoke-CimMethod -CimSession $cimSession -Namespace 'root/microsoft/windows/desiredstateconfiguration' -Class 'MSFT_DscLocalConfigurationManager' -MethodName 'PerformRequiredConfigurationChecks' -Arguments @{ 'Flags' = [uint32]1 } -Verbose
$cimSession | Remove-CimSession
```

## <a name="see-also"></a>См. также:

[PerformRequiredConfigurationChecks](../reference/mof-classes/msft-dsclocalconfigurationmanager-performrequiredconfigurationchecks.md)
