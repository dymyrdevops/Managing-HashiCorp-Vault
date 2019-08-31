Install azurecli before execute all steps:
https://github.com/MicrosoftDocs/azure-docs-cli/blob/master/docs-ref-conceptual/install-azure-cli-apt.md

Expected output:
===============


![Output](https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcR7LJd7o_xjL5TNeyG2ZUMxndldjWcoHoWxMvBd3PfsUCg_KoYt)

az login
az account list --query "[].{name:name, subscriptionId:id, tenantId:tenantId}"
az account set --subscription="${SUBSCRIPTION_ID}"
az ad sp create-for-rbac --role="Contributor" --scopes="/subscriptions/${SUBSCRIPTION_ID}"

Collect all output and update vars.tfvars
========================================

ARM_SUBSCRIPTION_ID=your_subscription_id
ARM_CLIENT_ID=your_appId
ARM_CLIENT_SECRET=your_password
ARM_TENANT_ID=your_tenant_id

Sample vars.tfvars

arm_client_id = "c0003591-4hh2-4d27-9101-027jj49e495c"

arm_client_secret = "d96f36-ae40-4ad3-a4e8-3c000f4bb82e"

arm_tenant_id = "5c0d5e1b-4699-4b7c-9676-68e02b1a69"

arm_subscription_id = "cc0d65c7-cf49-752d-8cd9-7oc93059f9g4"

ssh_key_pub = "~/.ssh/id_rsa.pub"

mysql_password = "Km@123456"

aks_prefix = "vault"

#kubernetes_client_id = ""

#kubernetes_client_secret = ""

#vault_domain = "dymyr.com"
