## What has changed?

1. Terminology has changed: Agent Procedures are now known as the Automation Workflows in VSA 10.
2. A dedicated scripting language is no longer required in VSA 10.
3. Translation of PowerShell commands is no longer required in VSA 10.
4. Scripting can now function as Batch files, PowerShell files, VBScript files, and BASH files (for Mac and Linux).

## Converting VSA 9 Procedures

Converting agent procedures can be done in 2 ways:
1. Using the upgrade wizard
	1. The wizard enables partners to move selected agent procedures to workflows during the upgrade process.
2. Export VSA 9 Agent Procedures
	1. This option allows for current VSA 9 agent procedures to be exported from the user interface to VSA 10 in an XML format.

### Requirements Prior to Upgrading using the Wizard
1. Unique link for VSA 10 instance required (this will be supplied at the time of upgrade)
2. Create a Personal Access Token (PAT)
3. Have VSA 9 connection details at hand

## Agent Procedure Translation Tool
The translation tool can be leveraged to convert VSA 9 Agent Procedures to VSA 10 Automation Workflows.

Head to your VSA 9 instance and navigate to **Agent Procedures > Schedule/Create.**
1. Select the agent procedure you wish to export.
2. Right-click on the selected procedure.
3. Select **Export Procedure**.

_Please note: A folder and its contents (procedures) can also be selected for export. Rather than selecting a single procedure, select a folder for export._

Select the location where the files should be saved. The file will be saved in an XML format.
Select **Save**.

Once the agent procedures have been exported, the files can now be imported into your VSA 10 platform.

Navigate to **Automation > Workflows** and select **Import VSA 9 Agent Procedures**.
n VSA 10:

1. In the **Automation / Workflows** tab, a new button is introduced called **Import VSA 9 Agent Procedure**. 
    1. When importing any Agent Procedure XML file, the translator tool will parse the file content and present the Agent Procedures to be imported in a list where you can select and continue. 
    2. There will also be information about the current compatibility score 1- 5 for each Agent Procedure where 5 is the highest. This information gives an overview and understanding of what specific Agent Procedures features currently are available in Workflow Actions & Conditions.

Select the file or folder that has been exported from your VSA 9 instance. Select **Open**.
If a folder is being imported into your VSA 10 instance, the agent procedures will be listed separately for selection.

Select the relevant procedures you wish to import and select **Continue** to finalize the import.
Any selected Agent Procedure within the imported XML file will generate a Workflow to be reviewed. 

1. The tool can be used to evaluate the currently supported Actions & Conditions translated from the Agent Procedures. 
2. The tool will also show any Action or Condition not yet supported by coloring it red and rendering the Workflow inactive, unable to be activated. The Workflow can however be edited or modified.

Confirmation of successful completion will appear.

