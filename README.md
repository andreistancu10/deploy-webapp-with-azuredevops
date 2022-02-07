# deploy-webapp-with-azuredevops
Demo Deploy ASP.NET webapplication using Azure DevOps and Terraform for provisioning Azure infrastructure
![image](https://user-images.githubusercontent.com/44494776/152757898-08b0c943-6a9e-4197-899c-b1e1bc456e12.png)


STEP 1: Prepare Azure DevOps

Sign into Azure DevOps
Select organisation that you have created above
Select New Project
Enter new project name & description

From marketplace add azuredevops extenstions: Terraform and Replace tokens
https://marketplace.visualstudio.com/search?term=terraform&target=AzureDevOps&category=All%20categories&sortBy=Relevance

![image](https://user-images.githubusercontent.com/44494776/152760184-b0b57b98-d4e3-40d6-83ce-5946d2625ef2.png)



Step 2: Build webapplication using Azure CI Pipeline
