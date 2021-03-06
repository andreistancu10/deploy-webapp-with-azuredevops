# deploy-webapp-with-azuredevops
Demo Deploy ASP.NET webapplication using Azure DevOps and Terraform for provisioning Azure infrastructure

The following image will walk you through all the steps explained in this project
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

1. Navigate to Pipelines –> Pipelines -> New Pipeline -> Other Git repo -> ![image](https://user-images.githubusercontent.com/44494776/152773337-91562bc4-63ef-4be0-97f3-93c9799f6cc5.png)


2. Create tasks for continous integration. This pipeline has tasks to compile .Net Core project. The dotnet tasks in the pipeline will restore dependencies build, test and publish the build output into a zip file (package) which can be deployed to a web application

![image](https://user-images.githubusercontent.com/44494776/152773044-ee7278da-9ca9-43c3-a450-afa70ed61024.png)

3. In addition to the application build, I need to publish terraform files to build artifacts so that it will be available in CD pipeline. So we have added Copy files task to copy Terraform file to Artifacts directory.


![image](https://user-images.githubusercontent.com/44494776/152774371-d5d2c0bd-3c82-4336-b8a6-21b527a74192.png)



STEP 3:  Deploy application and azure resources with Terraform using Azure CD pipeline

Navigate to Pipelines -> Releases -> Create Release

1. Create a new release using artifact from STEP 2

![image](https://user-images.githubusercontent.com/44494776/152809927-e9aa8b96-5a4e-47d0-8c52-5adf856e816c.png)

2. Create tasks for CD pipeline:

![image](https://user-images.githubusercontent.com/44494776/152810199-c7450963-e897-4f9a-ac1f-096bed27bbcb.png)




