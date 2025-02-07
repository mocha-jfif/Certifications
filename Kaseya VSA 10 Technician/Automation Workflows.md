## VSA 10 Automation
In VSA 9, automation is performed by Agent Procedures. 

Agent Procedures are scripts that are built on Kaseya's proprietary language, which executes on agents to perform specific tasks.

These tasks can vary, from enabling Bitlocker to activating a Windows license, or even installing an application.

VSA 10 offers the option to build automated workflows, which will be triggered when a certain event occurs from your monitored systems and that triggers a notification, allowing you to remedy some issues automatically. 

In VSA 10, automation has been structured into three sections:

- Scripts
	- Standalone scripts written in Powershell, Bash, or VBScript that are executed on a device ad hoc.
- Tasks
	- A series of scripts
	- Can be scheduled or run ad hoc.
- Workflows
	- Has the ability to run on a schedule, or be triggered by a notification.
	- Create conditions and checks to run various processes 

## Creating a Workflow

1. Navigate to: **VSA 10 WebApp -> Automation -> Workflows -> Create Workflow**
2. Give the Workflow a name, activate it, set a maximum execution time, and then click on the button **Next** button.
3. On the next page, you will have the option to select a trigger type (Notification). 
4. In the example below, a **High CPU Usage** notification will be triggering the workflow when it exceeds preset limits.
5. Once a **Trigge**r is selected, this is how it is displayed as part of the Workflow schema
6. Once a trigger is selected, you will see the option to add a step in the chain of actions. Click on the **New Step** button to proceed.
7. A drop-down list will show up presenting available actions for the selected trigger.
8. You can make use of Condition steps to execute different actions based on the outcome of your logical statements.

