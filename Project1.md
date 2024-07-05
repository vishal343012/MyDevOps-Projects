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
















