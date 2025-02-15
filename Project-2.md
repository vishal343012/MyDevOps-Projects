 **𝐒𝐞𝐚𝐦𝐥𝐞𝐬𝐬𝐥𝐲 𝐃𝐞𝐩𝐥𝐨𝐲 𝐀𝐩𝐩𝐥𝐢𝐜𝐚𝐭𝐢𝐨𝐧𝐬 𝐨𝐧 𝐆𝐨𝐨𝐠𝐥𝐞 𝐀𝐩𝐩 𝐄𝐧𝐠𝐢𝐧𝐞 𝐰𝐢𝐭𝐡 𝐉𝐞𝐧𝐤𝐢𝐧𝐬 𝐌𝐚𝐬𝐭𝐞𝐫-𝐒𝐥𝐚𝐯𝐞 𝐏𝐢𝐩𝐞𝐥𝐢𝐧𝐞**


![Animation](https://github.com/vishal343012/MyDevOps-Projects/assets/119778329/54c965e3-dbee-4333-96f4-a6b82ea55349)






Prerequisites
**Jenkins Server**: 

Ensure you have Jenkins installed and running.

**Google Cloud Account**: 
You need a Google Cloud account with App Engine enabled.

**Google Cloud SDK**: 
Install the Google Cloud SDK on your Jenkins nodes.

**Source Code Repository**: 
Your application code should be in a repository like GitHub,


****Step 1: Setting Up Jenkins Master-Slave Architecture**
**1.1 Install Jenkins

1.2 Configure Jenkins Master

**Create a New Node**:
Go to Manage Jenkins > Manage Nodes and Clouds > New Node.

**Enter the node name and select Permanent Agent**.
Configure the node with the required details (remote root directory, labels, etc.).
Launch Agent: Use the Launch agent via Java Web Start option, or configure the agent to connect using SSH.

**Step 2: **Configure Google Cloud SDK on Jenkins Nodes**

******sudo apt-get update && sudo apt-get install -y apt-transport-https ca-certificates gnupg
echo "deb [signed-by=/usr/share/keyrings/cloud.google.gpg] http://packages.cloud.google.com/apt cloud-sdk main" | sudo tee -a /etc/apt/sources.list.d/google-cloud-sdk.list
sudo apt-get install -y google-cloud-****__sdk******

****Authenticate with Google Cloud**:
**

gcloud auth login
gcloud config set project YOUR_PROJECT_ID



****Step 3: Create Jenkins Pipeline for Deployment**

**3.1 Install Required Plugins

Google OAuth Credentials: For Google authentication.
Google Kubernetes Engine: For deploying to GKE (if using Kubernetes).

****3.2 Configure Credentials**
**Add Google Cloud Credentials:
Go to Manage Jenkins > Manage Credentials.
Add a new Google Service Account from private key and upload the JSON key file from your Google Cloud service account.

****3.3 Create a Pipeline Job**
**New Item: Go to New Item, enter a name, select Pipeline, and click OK.
**Pipeline Definition: In the pipeline configuration, define your pipeline script. Here’s an example:
**
![image](https://github.com/vishal343012/MyDevOps-Projects/assets/119778329/a87dce46-05fd-404a-bf67-58e0d9b8508e)


**Step 4: Run the Pipeline
**
