# l200_hc_templ


# Deployment of a Windows VM, configure windows featurtes like IIS, .Net framework etc., download application deployment packages using DSC

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2F201-vm-win-iis-app-ssl%2Fazuredeploy.json" target="_blank">
<img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/201-vm-win-iis-app-ssl/images/deploytoazure.png"/>
</a>
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2F201-vm-win-iis-app-ssl%2Fazuredeploy.json" target="_blank">
<img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/201-vm-win-iis-app-ssl/images/visualizebutton.png"/>
</a>

To deploy this template using the scripts from the root of this repo: 
```PowerShell

.\Deploy-AzureResourceGroup.ps1 -StorageAccountName '<artifacts storage account name>' -ResourceGroupName '<Resource guroup name>' -ResourceGroupLocation '<RG location>' -TemplateFile .\azuredeploy.json -TemplateParametersFile .\azuredeploy.parameters.json -ArtifactStagingDirectory '.' -DSCSourceFolder '.\dsc' -UploadArtifacts
```

The following resources are deployed as part of the solution

#### A VNet with a single subnet 
The VNet and the subnet IP prefixes are defined in the variables section i.e. appVnetPrefix & appVnetSubnet1Prefix respectively. Set these two accrodingly.

#### NSG to define the security rules
It defines the rules for http, https and rdp acces to the VM. The NSG is assigned to the subnet

#### A NIC, a Public IP and a VM with Windows Server 2012 R2

#### A Storage account for the VM as well as for the artifacts

## Deployment steps

You can click the "deploy to Azure" button at the beginning of this document or follow the instructions for command line deployment using the scripts in the root of this repo.
