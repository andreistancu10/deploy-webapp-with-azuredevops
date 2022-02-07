# deploy-webapp-with-azuredevops
Demo Deploy ASP.NET webapplication using Azure DevOps and Terraform for provisioning Azure infrastructure
![image](https://user-images.githubusercontent.com/44494776/152757898-08b0c943-6a9e-4197-899c-b1e1bc456e12.png)


STEP 1: Prepare Azure DevOps

The first setup to setting up Azure DevOps is to create an organisation

1. Sign into Azure DevOps
2. Select New Organisation
3. Enter your preferred Azure DevOps organisation name & hosting location (In this lab, I will be using thomasthorntoncloud organisation)
4. Once you have created your organisation, you can sign into your organisation anything using https://dev.azure.com/{yourorganization
5. Once an organisation has been setup, next is to create an Azure DevOps project

6. Sign into Azure DevOps
7. Select organisation that you have created above
8. Select New Project
9. Enter new project name & description
10. From marketplace add azuredevops extenstions: Terraform and Replace tokens
https://marketplace.visualstudio.com/search?term=terraform&target=AzureDevOps&category=All%20categories&sortBy=Relevance




![image](https://user-images.githubusercontent.com/44494776/152761027-956d9205-8de8-4605-82cb-f0cab0474360.png)




Step 2: Build webapplication using Azure CI Pipeline
