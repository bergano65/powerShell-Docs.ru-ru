---
ms.date: 07/10/2019
keywords: jea,powershell,безопасность
title: Конфигурации сеансов JEA
ms.openlocfilehash: 650d0d11ef13605847d0822249e29e3491180629
ms.sourcegitcommit: debd2b38fb8070a7357bf1a4bf9cc736f3702f31
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2019
ms.locfileid: "70017735"
---
# <a name="jea-session-configurations"></a>Конфигурации сеансов JEA

Конечная точка JEA регистрируется в системе путем создания и регистрации файла конфигурации сеанса PowerShell. Конфигурации сеансов определяют, кто может использовать конечную точку JEA и к каким ролям будет предоставлен доступ. Они также определяют глобальные параметры, которые применяются ко всем пользователям в сеансе JEA.

## <a name="create-a-session-configuration-file"></a>Создание файла конфигурации сеанса

Чтобы зарегистрировать конечную точку JEA, следует указать способ ее настройки. Существует множество факторов, которые следует учитывать. Ниже приведены наиболее важные из них.

- Кто имеет доступ к конечной точке JEA?
- Какие роли им назначены
- Какое удостоверение JEA использует на самом деле
- Имя конечной точки JEA

Все они определяются в файле конфигурации сеанса PowerShell, который представляет собой файл данных PowerShell с расширением `.pssc`. Файл конфигурации сеанса можно открыть в любом текстовом редакторе.

Выполните следующую команду, чтобы создать пустой шаблон файла конфигурации.

```powershell
New-PSSessionConfigurationFile -SessionType RestrictedRemoteServer -Path .\MyJEAEndpoint.pssc
```

> [!TIP]
> По умолчанию файл шаблона включает только основные параметры конфигурации. Чтобы включить в создаваемый PSSC-файл все применимые настройки, используйте параметр `-Full`.

Поле `-SessionType RestrictedRemoteServer` указывает, что конфигурация сеанса будет использоваться JEA для безопасного управления. Настроенные таким образом сеансы работают в режиме **NoLanguage** и содержат только следующие команды (и псевдонимы) по умолчанию:

- Clear-Host (cls, clear)
- Exit-PSSession (exsn, exit)
- Get-Command (gcm)
- Get-FormatData
- Get-Help
- Measure-Object (measure)
- Out-Default
- Select-Object (select)

Поставщики PowerShell недоступны, как и внешние программы (исполняемые файлы, скрипты).

Дополнительные сведения о режимах языка см. в разделе [about_Language_modes](/powershell/module/microsoft.powershell.core/about/about_language_modes).

### <a name="choose-the-jea-identity"></a>Выбор удостоверения JEA

Для выполнения команд подключенных пользователей JEA требуется удостоверение (учетная запись).
Определить используемое JEA удостоверение можно в файле конфигурации сеанса.

#### <a name="local-virtual-account"></a>Локальная виртуальная учетная запись

Если роли, поддерживаемые этой конечной точкой JEA, используются для управления локальным компьютером, а для успешного выполнения команд достаточно учетной записи локального администратора, следует настроить в JEA использование локальной виртуальной учетной записи.
Виртуальные учетные записи — это временные записи, уникальные для определенного пользователя, срок действия которых ограничен длительностью его сеанса PowerShell. На рядовом сервере или рабочей станции виртуальные учетные записи принадлежат к группе **Администраторы** локального компьютера. На контроллере домена Active Directory виртуальные учетные записи принадлежат к группе **Администраторы домена** домена.

```powershell
# Setting the session to use a virtual account
RunAsVirtualAccount = $true
```

Если ролям, определенным в конфигурации сеанса, не требуются полные права администратора, можно указать группы безопасности, к которым будет принадлежать виртуальная учетная запись. На рядовом сервере или рабочей станции указанные группы безопасности должны быть локальными, а не из домена.

Если указаны группы безопасности, виртуальная учетная запись не будет принадлежать к группе локальных администраторов или администраторов домена.

```powershell
# Setting the session to use a virtual account that only belongs to the NetworkOperator and NetworkAuditor local groups
RunAsVirtualAccount = $true
RunAsVirtualAccountGroups = 'NetworkOperator', 'NetworkAuditor'
```

> [!NOTE]
> Виртуальные учетные записи временно получают право на вход качестве службы в политике безопасности на локальном сервере. Если одной из указанных групп VirtualAccountGroup уже предоставлено это право в политике, отдельная виртуальная учетная запись больше не добавляется и удаляется из политики. Это может быть полезно в таких сценариях, как контроллеры домена, где ведется детальный аудит изменений в политике безопасности контроллера домена. Эта возможность доступна только в Windows Server 2016 с накопительным пакетом обновления за ноябрь 2018 года или более поздней версии и Windows Server 2019 с накопительным пакетом обновления за январь 2019 года или более поздней версии.

#### <a name="group-managed-service-account"></a>Групповая управляемая учетная запись службы

Если пользователям JEA нужен доступ к таким сетевым ресурсам, как другие компьютеры или веб-службы, наиболее подходящим удостоверением является групповая управляемая учетная запись службы (gMSA). Эти учетные записи предоставляют удостоверение домена, которое можно использовать для проверки подлинности при доступе к ресурсам на любом компьютере в домене. Права, предоставляемые GMSA, определяются ресурсами, к которым вы обращаетесь. Вы не получите права администратора на компьютерах или в службах автоматически, пока администратор компьютера или службы явно не предоставит их учетной записи GMSA.

```powershell
# Configure JEA sessions to use the GMSA in the local computer's domain
# with the sAMAccountName of 'MyJEAGMSA'
GroupManagedServiceAccount = 'Domain\MyJEAGMSA'
```

GMSA следует использовать только в том случае, когда это необходимо:

- Сложно отследить связь действий с пользователями при использовании GMSA. Каждый пользователь использует одно и то же удостоверение запуска от имени. Для сопоставления отдельных пользователей с действиями потребуется обратиться к записям сеансов и журналам PowerShell.

- GMSA может иметь доступ к различным ресурсам сети, обращаться к которым подключающемуся пользователю не требуется. Всегда старайтесь ограничить действующие разрешения в рамках сеанса JEA и следуйте принципу предоставления минимальных прав.

> [!NOTE]
> Групповые управляемые учетные записи доступны только в PowerShell 5.1 или более поздней версии на компьютерах, присоединенных к домену.

Дополнительные сведения об обеспечении безопасности сеансов JEA см. в статье [Вопросы безопасности](security-considerations.md).

### <a name="session-transcripts"></a>Записи сеансов

Рекомендуется настроить на конечной точке JEA автоматическую запись сеансов пользователей. Записи сеансов PowerShell содержат сведения о подключающемся пользователе, назначенном ему удостоверении запуска от имени и выполняемых им командах. Их удобно использовать для аудита группы, когда необходимо знать, кто именно внес определенное изменение в систему.

Чтобы настроить автоматическую запись в файле конфигурации сеанса, укажите путь к папке, где должны храниться записи.

```powershell
TranscriptDirectory = 'C:\ProgramData\JEAConfiguration\Transcripts'
```

Записи помещаются в папку с учетной записью **Local System**, которой требуются права на чтение и запись в каталоге. У стандартных пользователей не должно быть доступа к этой папке. Ограничьте число администраторов безопасности, которые имеют доступ для аудита записей.

### <a name="user-drive"></a>Диск пользователя

Если подключающимся пользователям требуется скопировать файлы с конечной точки JEA или на нее для выполнения команды, можно включить диск пользователя в файле конфигурации сеанса. Диск пользователя — это **PSDrive**, сопоставленный с уникальной папкой каждого подключающегося пользователя. Эта папка служит для копирования файлов из системы и в нее без назначения пользователям прав доступа ко всей файловой системе или предоставления поставщика FileSystem. Содержимое диска пользователя сохраняется между сеансами на случай, если сетевое подключение будет прервано.

```powershell
MountUserDrive = $true
```

По умолчанию этот диск позволяет хранить до 50 МБ данных на пользователя. Вы можете ограничить объем данных, доступных пользователю, с помощью поля *UserDriveMaximumSize*.

```powershell
# Enables the user drive with a per-user limit of 500MB (524288000 bytes)
MountUserDrive = $true
UserDriveMaximumSize = 524288000
```

Если хранить данные на диске пользователя не требуется, можно настроить в системе запланированное задание, автоматически очищающее папку каждую ночь.

> [!NOTE]
> Диск пользователя доступен только в PowerShell 5.1 или более поздней версии.

Дополнительные сведения о накопителях PSDrive см. в разделе [Управление дисками PowerShell](/powershell/scripting/samples/managing-windows-powershell-drives).

### <a name="role-definitions"></a>Определения ролей

Определения ролей в файле конфигурации сеанса определяют сопоставление **пользователей** с **ролями**. Все пользователи или группы, включенные в это поле, получают разрешение на конечную точку JEA после ее регистрации.
Пользователя или группу можно включить в качестве ключа в хэш-таблицу только один раз, однако им можно назначить несколько ролей. Имя возможности роли должно соответствовать имени файла возможности роли без расширения `.psrc`.

```powershell
RoleDefinitions = @{
    'CONTOSO\JEA_DNS_ADMINS'    = @{ RoleCapabilities = 'DnsAdmin', 'DnsOperator', 'DnsAuditor' }
    'CONTOSO\JEA_DNS_OPERATORS' = @{ RoleCapabilities = 'DnsOperator', 'DnsAuditor' }
    'CONTOSO\JEA_DNS_AUDITORS'  = @{ RoleCapabilities = 'DnsAuditor' }
}
```

Если пользователи принадлежат к нескольким группам в определении роли, они получат доступ к ролям в каждой из них. Если две роли предоставляют доступ к одним и тем же командлетам, пользователю назначается наиболее нестрогий набор параметров.

При указании локальных пользователей и группы в поле определения роли перед обратной косой чертой обязательно укажите имя компьютера (не **localhost** и не подстановочный знак). Чтобы проверить имя компьютера, проверьте имя переменной `$env:COMPUTERNAME`.

```powershell
RoleDefinitions = @{
    'MyComputerName\MyLocalGroup' = @{ RoleCapabilities = 'DnsAuditor' }
}
```

### <a name="role-capability-search-order"></a>Порядок поиска возможностей ролей

Как показано в приведенном выше примере, ссылка на возможности ролей осуществляется по базовому имени файла возможностей ролей. Базовое имя файла — имя файла без расширения. Если несколько возможностей ролей доступны в системе с одинаковым именем, PowerShell использует неявный порядок поиска для выбора действующего файла возможностей ролей. При этом JEA **не** предоставляет доступ всем файлам возможностей ролей с одинаковым именем.

JEA использует переменную `$env:PSModulePath` среды, чтобы определить искомые пути для файлов возможностей роли. В пределах каждого из этих путей JEA будет искать допустимые модули PowerShell, которые содержат вложенную папку RoleCapabilities. Как и при импорте модулей JEA использует возможности роли, доступные в Windows, а не пользовательские возможности роли с тем же именем.

При всех других конфликтах имен приоритет определяется порядком, в котором Windows перечисляет файлы в каталоге (не обязательно в алфавитном порядке). Первый найденный файл возможности роли, соответствующий указанному имени, будет использоваться для подключающегося пользователя. Так как поиск возможностей ролей не имеет детерминированного порядка, **настоятельно рекомендуется** использовать уникальные имена файлов возможностей ролей.

### <a name="conditional-access-rules"></a>Правила условного доступа

Все пользователи и группы, включенные в поле **RoleDefinitions**, автоматически получают доступ к конечным точкам JEA. Правила условного доступа позволяют уточнить такой доступ и потребовать от пользователей принадлежности к дополнительным группам безопасности, не оказывающим влияния на роли, которым они назначены. Это может быть полезно, если требуется интегрировать решение управления привилегированным доступом "JIT", проверку подлинности смарт-карт или другое решение многофакторной проверки подлинности с помощью JEA.

Правила условного доступа определяются в поле RequiredGroups файла конфигурации сеанса.
Там можно задать хэш-таблицу (при необходимости вложенной), которая использует ключи "And" и "Or" для создания правил. Ниже представлены примеры использования этого поля.

```powershell
# Example 1: Connecting users must belong to a security group called "elevated-jea"
RequiredGroups = @{ And = 'elevated-jea' }

# Example 2: Connecting users must have signed on with 2 factor authentication or a smart card
# The 2 factor authentication group name is "2FA-logon" and the smart card group name is "smartcard-logon"
RequiredGroups = @{ Or = '2FA-logon', 'smartcard-logon' }

# Example 3: Connecting users must elevate into "elevated-jea" with their JIT system and have logged on with 2FA or a smart card
RequiredGroups = @{ And = 'elevated-jea', @{ Or = '2FA-logon', 'smartcard-logon' }}
```

> [!NOTE]
> Правила условного доступа доступны только в PowerShell 5.1 или более поздней версии.

### <a name="other-properties"></a>Другие свойства

Файлы конфигурации сеанса позволяют выполнять те же операции, что и файл возможностей ролей, за исключением предоставления подключающимся пользователям доступа к другим командам. Если вы хотите разрешить всем пользователям доступ к определенным командлетам, функциям или поставщикам, это можно сделать прямо в файле конфигурации сеанса.
Чтобы вывести полный список поддерживаемых свойств в файле конфигурации сеанса, запустите `Get-Help New-PSSessionConfigurationFile -Full`.

## <a name="testing-a-session-configuration-file"></a>Проверка файла конфигурации сеанса

Конфигурацию сеанса можно проверить с помощью командлета [Test-PSSessionConfigurationFile](/powershell/module/microsoft.powershell.core/test-pssessionconfigurationfile). Рекомендуется проверить файл конфигурации сеанса, если вы вручную редактировали `.pssc`-файл. Тестирование гарантирует, что используется правильный синтаксис. Если файл конфигурации сеанса не пройдет проверку, он не регистрируется в системе.

## <a name="sample-session-configuration-file"></a>Пример файла конфигурации сеанса

Ниже приведен пример, показывающий, как создать и проверить конфигурацию сеанса для JEA. Для удобства использования и чтения определения роли создаются и хранятся в переменной `$roles`. Это не является обязательным.

```powershell
$roles = @{
    'CONTOSO\JEA_DNS_ADMINS'    = @{ RoleCapabilities = 'DnsAdmin', 'DnsOperator', 'DnsAuditor' }
    'CONTOSO\JEA_DNS_OPERATORS' = @{ RoleCapabilities = 'DnsOperator', 'DnsAuditor' }
    'CONTOSO\JEA_DNS_AUDITORS'  = @{ RoleCapabilities = 'DnsAuditor' }
}

New-PSSessionConfigurationFile -SessionType RestrictedRemoteServer -Path .\JEAConfig.pssc -RunAsVirtualAccount -TranscriptDirectory 'C:\ProgramData\JEAConfiguration\Transcripts' -RoleDefinitions $roles -RequiredGroups @{ Or = '2FA-logon', 'smartcard-logon' }
Test-PSSessionConfigurationFile -Path .\JEAConfig.pssc # should yield True
```

## <a name="updating-session-configuration-files"></a>Изменение файлов конфигурации сеанса

Чтобы изменить свойства конфигурации сеанса JEA, включая сопоставление пользователей с ролями, следует [отменить регистрацию](register-jea.md#unregistering-jea-configurations). Затем [перерегистрируйте](register-jea.md) конфигурацию сеанса JEA, используя измененный файл конфигурации сеанса.

## <a name="next-steps"></a>Дальнейшие действия

- [Регистрация конфигурации JEA](register-jea.md)
- [Создание ролей JEA](role-capabilities.md)
