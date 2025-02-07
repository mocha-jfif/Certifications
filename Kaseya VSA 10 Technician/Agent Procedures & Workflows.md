## VSA 9 Agent Procedures

What's changed?

1. Terminology has changed. Agent Procedures are now known as the Automation in VSA 10.
2. A dedicated scripting language is no longer required in VSA 10.
3. Translation of PowerShell commands is no longer required in VSA 10.
4. Scripting can now function as Batch, Powershell, VBScript files, and BASH.

## Workflow Actions
The Workflow action **Get Device Value** will help you query for various device values as variables to be used within the Workflow Conditions.

In a workflow, you may want to test if a condition is met on the targeted device. It can be a service or process running, a registry key exists if a specific file exists, or if a user is currently logged on to the device. 

The workflow action **Get Device Value** will help you query for various device values as variables to be used within the workflow conditions.

## Available Device Values

- Services + Applications
	- Is Process Running: Evaluates if one or multiple processes are running as a Boolean value.
		- Yes if one named or list of named processes are running.
		-  No if one named or any in a list of named processes are not running.
	- Service Running: Evaluates if one or a list of named Services are running as a Boolean value.
		- Yes if one named or list of named services are running.
		- No if one named or any in a list of named services are not running.
- Users
	- Is user logged on: Evaluates if a user is logged on to the device console session as a Boolean value. Leave empty (blank) for any user or specify one or multiple usernames as a Boolean value.
		- Returns **Yes** if any (blank) or specific named user currently are logged in to the console session.
		- Returns **No** if any (blank), one specific named user or a list of multiple named users currently are not logged in to the console session.
	- Is user active: Evaluates if a user currently is active on the device console session as a Boolean value. Leave empty for any user or specify one or multiple usernames.
		- Returns **Yes** is if any (blank) or one named user currently is active in the console session.
		- Returns **No** if any (blank), one specific named user, or a list of multiple named users currently are inactive in the console session.
- File System
	- File exists: Evaluate if a file exists as a Boolean value.
		- Yes if exists
		- No if it does not
	- File timestamp: Returns the latest update as a Date value from a specified file.
		- Returns the file timestamp as a Date value.
		- Fail if the specified file does not exist.
	- File contains: evaluate if a file contains a specified string as a Boolean value.
		- Returns yes if the file exists and the string matches
		- Returns no if the specified file doesn't exist or the string does not match
	- File version: Returns the latest update as a Date value from a specified file
		- Fail if the specified file does not exist
	- File Size: Returns the file size for a specified file as a Number value
		- Fail if the specified file does not exist
- General
	- Constant value: Create constant values by String, Date, or Number.
	- Get CPU architecture: Returns the CPU architecture as a String value.

