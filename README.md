# Powershell Cookbook

[![AppVeyor Build status](https://ci.appveyor.com/api/projects/status/ej1qiur29xbuc2eq/branch/master?svg=true)](https://ci.appveyor.com/project/ChefWindowsCookbooks/powershell/branch/master) [![Cookbook Version](https://img.shields.io/cookbook/v/powershell.svg)](https://supermarket.chef.io/cookbooks/powershell)

Installs and configures PowerShell 2.0, 3.0, 4.0 or 5.0.

## Requirements

### Platforms

Not every version of Windows supports every version of Powershell. The following table illustrates Powershell support across the Windows family. **Included** means that the base installation of the operating system includes the indicated version of Powershell.

Windows Version                     | PowerShell 2.0 | PowerShell 3.0 | PowerShell 4.0 | PowerShell 5.0
----------------------------------- | -------------- | -------------- | -------------- | --------------
Windows Server 2008 R2              | Included       | Supported      | Supported      | Supported
Windows Server 2012 / Windows 8     | Included       | Included       | Supported      | Supported
Windows Server 2012R2 / Windows 8.1 | Included       | Not Available  | Included       | Supported

### Chef

- Chef 13+

### Cookbooks

- windows 3.0+

PowerShell also requires the appropriate version of the Microsoft .NET Framework to be installed, if the operating system does not ship with that version. The following community cookbooks are used to install the correct version of the .NET Framework:

- ms_dotnet

## Resources

### `powershell_module`

#### Deprecated

The `powershell_module` has been removed from this cookbook as it was non-functional for most needs and has been replaced with built in resources in chef:

- [powershell_package_source](https://docs.chef.io/resource_powershell_package_source.html)
- [powershell_package](https://docs.chef.io/resource_powershell_package.html)

## Usage

**Note**: The installation may require a restart of the node being configured before PowerShell can be used.

### default

The default recipe contains no resources and will do nothing if included on a run_list.

### powershell2

Include the `powershell2` recipe in a run list, to ensure PowerShell 2.0 is installed. If the platform is not supported, a warning will be logged.

### powershell3

Include the `powershell3` recipe in a run list, to install PowerShell 3.0 is installed on applicable platforms. If the platform is not supported, a warning will be logged.

### powershell4

Include the `powershell4` recipe in a run list, to install PowerShell 4.0 is installed on applicable platforms. If the platform is not supported, a warning will be logged.

### powershell5

Include the `powershell5` recipe in a run list, to install PowerShell 5.0 is installed on applicable platforms. If the platform is not supported, a warning will be logged.

## References

- Installing [Windows Management Framework 2.0](http://support.microsoft.com/kb/968929)
- Installing [Windows Management Framework 3.0](http://www.microsoft.com/en-us/download/details.aspx?id=34595)
- Installing [Windows Management Framework 4.0](http://www.microsoft.com/en-us/download/details.aspx?id=40855)
- Installing [Windows Management Framework 5.0](https://www.microsoft.com/en-us/download/details.aspx?id=50395)

## License & Authors

- Author:: Seth Chisamore ([schisamo@chef.io](mailto:schisamo@chef.io))
- Author:: Julian Dunn ([jdunn@chef.io](mailto:jdunn@chef.io))

```text
Copyright:: 2011-2016, Chef Software, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
