VSA 10 Deployment Methods:

1. Automatic | Network Discovery and Deployment
	1. This method is especially suitable for mass deployment as several systems can be selected and the deployment initiated simultaneously for all of them.
	2. All the agents deployed are preconfigured with the policies you want.
2. Manual | MSI Installer 

## How to use Discovery and Deployment
1. Navigate to **Discovery & Deployment** in VSA 10. 
2. Select **Add** at the top to get started.
3. Add a probe by selecting an existing Windows agent already installed.
4. Run a probe discovery.
5. Select the discovered systems you want to deploy the agents to.
6. Deploy the agent on those systems. Please note: You can select the group you want to be assigned and also pre-configure them with the settings copied from an already deployed system.
7. Once the deployment has started you can see the progress.
8. Deployment has been successful.

## MSI Installer

This is another simple method for deploying the VSA 10 Agent.  The MSI has the Agent Group's unique token ID embedded within it that automatically associates the machine to the group.

While downloading an MSI, VSA 10 asks for the Organization, Site, and Agent Group of the required installer, so as to provide a customized file for those specifications.

This download link eliminates the need to attach a whole Installer file to an e-mail. You can simply share the MSI download link with partners via email, who then can deploy the Agent onto their systems with ease.


## Additional Features: Tags & Scopes

**Tags** are similar to labels that allow you to target machines across Organizations, Sites, and Groups.
Systems > Tags > New


**Scopes** are a logical combination of Groups, Tags, System Types, Descriptions, Custom Fields, or a combination of all. Scopes can be leveraged to run automation and reporting, as well as to apply patch management or antivirus policies.
Systems > Scopes > Create Scope
