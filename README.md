# FIT F# Azure Function Template
An opinionated F# Azure Function template.

## Features

### Configuration
* **global.json** pinned to .NET 8
* **VS Code** settings to hide inlay hints by default
* **.gitignore** with common F# settings
* **src/function** folder structure

### Pre-installed dotnet tools
* **Fantomas v6** pre-configured with `.editorconfig`
* **Paket v8** with the following dependencies:
    * FSharp.Core
    * FSToolkit.ErrorHandling

## To install locally
```bash
dotnet new install ./
```

## To execute the template
```bash
dotnet new fit-azurefunc -o MyAzureFunc
```

will give you a folder structure as follows:

```
.config
    dotnet-tools.json
.paket
    Paket.Restore.targets
.vscode
    settings.json
src
    FIT.AzureFunc
        FIT.AzureFunc.fsproj
        paket.references
        function.json
        host.json
        local.settings.json
        Greet.fs
        Program.fs
        Readme.md
FIT.AzureFunction.sln
.editorconfig
.gitignore
global.json
paket.dependencies
paket.lock
```

You can then run the application from within the folder as follows:

```bash
# run azurite in separate folder and bash
azurite
```

```bash
cd src/FIT.AzureFunc
func start
# or use visual studio, visual studio code or rider
```

### Adding a package
```bash
cd src/FIT.AzureFunc
dotnet paket add <package name>
```
### Removing a package
```bash
cd src/FIT.AzureFunc
dotnet paket remove <package name>
```
### Safely updating all dependencies
```bash
dotnet paket update --keep-major
```