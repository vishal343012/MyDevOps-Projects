𝐃𝐞𝐩𝐥𝐨𝐲 𝐀𝐒𝐏 .𝐍𝐄𝐓 𝐂𝐨𝐫𝐞 𝐖𝐞𝐛𝐬𝐢𝐭𝐞 𝐭𝐨 𝐀𝐳𝐮𝐫𝐞 𝐕𝐌 -𝐈𝐈𝐒- 𝐀𝐳𝐮𝐫𝐞 𝐏𝐢𝐩𝐞𝐥𝐢𝐧𝐞𝐬
Deploying an ASP.NET Core website to an Azure VM using IIS and Azure Pipelines involves several steps. Here is a full guide to help you through the process:

**Step 1: Set Up Your Azure VM**
Create an Azure VM:

**Go to the Azure Portal**.
Click on Create a resource > Virtual Machine.
Follow the prompts to configure your VM (choose a Windows Server image).
**Set Up IIS on the Azure VM**:

**Connect to your VM via Remote Desktop**.
Open Server Manager, go to Manage > Add Roles and Features.
Select Web Server (IIS) and proceed through the installation.

Install .NET Core Hosting Bundle:
**Step 2: Prepare Your ASP.NET Core Project**
Create a new project in visual studio and push that project in azure dev repository.

**Step 3: Set Up Azure Pipelines**
1.	Create a New Pipeline:
o	Go to your Azure DevOps project.
o	Click on Pipelines > New pipeline.
o	Select your repository (e.g., GitHub, Azure Repos).

Create a Pipeline and build the Jobs
![image](https://github.com/vishal343012/MyDevOps-Projects/assets/119778329/b937e7fe-0be9-4f52-947a-4d21e9f444b2)

**Step 4: Deploy to IIS on Azure VM**
Set Up Deployment Group on Azure DevOps:

In Azure DevOps, go to Pipelines > Deployment groups > New Deployment Group.
Follow the instructions to install the Azure Pipelines agent on your Azure VM.
<img width="736" alt="image" src="https://github.com/vishal343012/MyDevOps-Projects/assets/119778329/7efc3de3-e0d0-4213-99d0-b8ff2def230e">


**Create a Release Pipeline:
**
Go to Pipelines > Releases > New pipeline.
Select the build artifact created from your build pipeline.
Add a stage and configure it to use the deployment group targeting your Azure VM.
Deploy to IIS:

Add the following tasks to your release stage:

Create release Pipeline and select IIS template
<img width="595" alt="image" src="https://github.com/vishal343012/MyDevOps-Projects/assets/119778329/064416f1-481f-4f51-a77c-46351801ad0b">

**Now we will go to virtual machine open the PowerShell as an administrator and paste the scripts and connect from azure pipeline**
<img width="488" alt="image" src="https://github.com/vishal343012/MyDevOps-Projects/assets/119778329/65645ba0-cea6-4777-8fb6-9976264c8a43">

**Now we will select the deployment task and choose the deployment group from drop down which we have created – My websites
Now we will create a new release**

****View the release and deploy it in deploy section we have to chnage in yaml file we ned to add  -task:  
- task: PublishBuildArtifacts@1****

- <img width="301" alt="image" src="https://github.com/vishal343012/MyDevOps-Projects/assets/119778329/a19ed552-11c6-46b4-b2ef-a01ffeb62bfd">

**Now copy the Public IP of virtual machine and check from browser**

<img width="308" alt="image" src="https://github.com/vishal343012/MyDevOps-Projects/assets/119778329/bdb9b9bc-e49a-4a4b-bc68-303e26f1bf9f">
















