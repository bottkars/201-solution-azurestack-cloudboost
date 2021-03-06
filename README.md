# 201-solution-azurestack-cloudboost

This Template Deploys and Configures DEL|EMC Cloudboost Virtual Edition onto Azurestack

Prework and Requirements:
  -  Have Custom Script for Linux extensions Available on AzureStackHub
  -  Upload CloudBoost root and lvm VHD for Azure* to Blob in Subscription



AZ CLI Deployment Example:

```azurecli-interactive
az group create --name CloudBoost_from_cli --location local
```

```azurecli-interactive
az deployment group validate  \
--template-uri https://raw.githubusercontent.com/bottkars/201-solution-azurestack-cloudboost/master/azuredeploy.json \
--parameters https://raw.githubusercontent.com/bottkars/201-solution-azurestack-cloudboost/master/azuredeploy.parameters.json \
--resource-group CloudBoost_from_cli
```

```azurecli-interactive
az deployment group create  \
--template-uri https://raw.githubusercontent.com/bottkars/201-solution-azurestack-cloudboost/master/azuredeploy.json \
--parameters https://raw.githubusercontent.com/bottkars/201-solution-azurestack-cloudboost/master/azuredeploy.parameters.json \
--resource-group CloudBoost_from_cli
```

delete

```azurecli-interactive
az group delete --name CloudBoost_from_cli  -y
```
