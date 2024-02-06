# AzureFunction

This is a template for an Azure Function in F# using NET 8.

## prerequisits for azure functions 

### VS Code

```pwsh
code --install-extension Ionide.Ionide-fsharp
code --install-extension ms-azuretools.vscode-azurefunctions
code --install-extension Azurite.azurite
```

### Azure function tooling 

[how to install](https://learn.microsoft.com/en-us/azure/azure-functions/functions-run-local?tabs=linux%2Cisolated-process%2Cnode-v4%2Cpython-v2%2Chttp-trigger%2Ccontainer-apps&pivots=programming-language-csharp#install-the-azure-functions-core-tools)

```bash
sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/microsoft-ubuntu-$(lsb_release -cs)-prod $(lsb_release -cs) main" > /etc/apt/sources.list.d/dotnetdev.list'

sudo apt-get update
sudo apt-get install azure-functions-core-tools-4
```

### Azurite 
Install Azurite for local debugging

```bash
npm install -g azurite
```


### Dotnet Templates 

```pwsh
dotnet new install Microsoft.Azure.WebJobs.ItemTemplates
```

this will provide yo|u with item templates like 



```pwsh
dotnet new install Microsoft.Azure.WebJobs.ProjectTemplates
```

this will provide you with project templates like 

```pwsh
dotnet new func --language "F#" --name "<THENAME>"
```

# how to run

change to src folder and run with console

```pwsh
func start
```

or use VS Code, VS or Rider and hit F5