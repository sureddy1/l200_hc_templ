# l200_hc_templ


# Deployment of a Windows VM, configure windows featurtes like IIS, .Net framework etc., download application deployment packages using DSC

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fsureddy1%2Fl200_hc_templ%2Fmaster%2Fazuredeploy.json" target="_blank">
<img src="https://raw.githubusercontent.com/sureddy1/l200_hc_templ/master/images/deploytoazure.png"/>
</a>

To deploy this template using the scripts from the root of this repo: 
```PowerShell

.\Deploy-AzureResourceGroup.ps1 -StorageAccountName '<artifacts storage account name>' -ResourceGroupName '<Resource guroup name>' -ResourceGroupLocation '<RG location>' -TemplateFile .\azuredeploy.json -TemplateParametersFile .\azuredeploy.parameters.json -ArtifactStagingDirectory '.' -DSCSourceFolder '.\dsc' -UploadArtifacts
```

## Deployment steps

You can click the "deploy to Azure" button at the beginning of this document or follow the instructions for command line deployment using the scripts in the root of this repo.
