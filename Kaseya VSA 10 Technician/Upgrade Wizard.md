## Organizational Structure Mapping
In VSA 10, the concept of an Organization is similar to VSA 9. However, in VSA 10, the organizational hierarchy is a **three-tiered model** consisting of:

- **Organizations**
- **Sites**, and
- **Groups**.

_Please note: All three levels must exist to host **Agents** and **Devices**._

1. Organizations are top-level containers.
2. Underneath Organizations are Sites. Sites are middle-level containers.
3. Underneath Sites are Groups. Groups are lower-level containers and here managed devices like Agents and Network devices are physically located.

Organizations ---> Organizations
Sub-Organizations ---> Sites
- VSA 9 sub-organizations map to VSA 10 sites with the following conditions:
	- If a VSA 9 sub-org does not explicitly contain any child Machine Group(s), it will be created in VSA 10 as an empty site.
Machine Groups ---> Groups
- VSA 9 machine groups map to VSA 10 groups with the following conditions:
	- If a VSA 9 machine group does not contain any agents or assets, it will be created in VSA 10 as an empty group
	- VSA 9 agents and assets contained within a VSA 9 machine group will be moved to the corresponding VSA 10 group
	- In VSA 9, if the direct parent of a machine group is an organization, a new VSA 10 site will need to be created as the middle-level container, and then the VSA 9 machine group will be created as a VSA 10 group under the new VSA 10 site.

## Agent Upgrade

Once the VSA 9 Organizational structure has been upgraded, new Agent records will be created in VSA 10 within their associated Organizational structure. 

The upgrade process will attempt to deploy Agents automatically, but some Agents will require manual installation.

When a VSA 10 Agent is installed manually for a VSA 9 Agent that was included in the upgrade process, the VSA 10 platform will attempt to automatically reconcile the newly registering VSA 10 Agent with an existing Agent record that was created during the upgrade.

When the Upgrade is being performed, the following will be for various operating systems:
1. Windows:
	1. Existing VSA 9 Agents will automatically deploy a VSA 10 Agent.
2. macOS:
	1. Existing VSA 9 Agents will automatically prepare each device with specific information about the upgrade. 
	2. Next, the VSA 10 Agents will need to be installed manually. 
	3. When the Agent is deployed, based on the local system information from the VSA 9 Agent, the VSA 10 Agent will register itself with the proper VSA 10 Agent record.
3. Linux:
	1. Existing VSA 9 Agents will automatically prepare each device with specific information about the upgrade. 
	2. Next, the VSA 10 Agents will need to be installed manually. 
	3. When the Agent is deployed, based on the local system information from the VSA 9 Agent, the VSA 10 Agent will register itself with the proper VSA 10 Agent record.

## Organization and Agent Data Upgrade
The following VSA 9 data will be recreated in VSA 10 and aligned with its associated object record

##### Organization
Custom Fields ---> Upgraded to VSA 10 Organization Custom Fields
Managed Variables ---> Upgraded to VSA 10 Organization Custom Fields
- These will be aligned with the relevant VSA 10 Organization, site, or group

##### Agent
Custom Fields ---> Upgraded to VSA 10 Organization Custom Fields
Notes ---> Upgraded to VSA 10 Agent Notes


## Network and Device Upgrade
In VSA 10, the concept of a Network is the same as in VSA 9. 

It requires an existing Agent that resides within the given network subnet to be assigned as a ‘probe’ machine for the purpose of performing important local network functions such as a **Discovery Scan**.

**VSA 9 devices that are not promoted to Assets will not be upgraded.**

##### Discovery Scans

Once a network has been upgraded to VSA 10, Discovery Scans will automatically occur every six hours. 

**_Please note: A scan can also be triggered manually._**

##### Differences Between VSA 9 and VSA 10 Network Functionality

Scan Inclusions:
1. VSA 10 Networks allow for Scan Inclusions only; **no exclusions**. Inclusions are defined in CIDR notation. The upgrade process will attempt to upgrade VSA 9 network inclusions, but some individual scan ranges may not be upgraded. Please be sure to check your VSA 10 network scan inclusions once the upgrade is complete.

Enrolled Devices:
1. In VSA 10, the equivalent of a VSA 9 Asset is referred to as an **Enrolled Device**. VSA 10 will display all discovered devices but only those with Agents deployed or those who have been enrolled will be able to be managed using the available functionality for each. _Example: if you wish to remote control into a VSA 9 network device with the built-in SSH functionality or monitor a network device using SNMP, the device must first be enrolled._

## User Account Upgrades

User accounts can be selected for the upgrade from VSA 9 to VSA 10. However, passwords will not be upgraded. 

Instead, a secure invite will be sent to the email address found in VSA 9 for each user account selected to be upgraded. If there is no email address for a given user account, you can provide one during the upgrade process.

_Please note: In order to upgrade a user account, an email address is required. A user account will not be upgraded without an email address._

## User Permission Hierarchy

In VSA 10, feature permissions and access controls are managed using **Teams**. 

A VSA 10 Team is a container for user accounts. All VSA 10 user accounts must belong to a Team (and can only belong to one).

_Please note: You can assign a Team for each user, or optionally assign users to a Team in bulk._

A team has the following characteristics:
1. Controls permissions for feature functions.
	1. i.e., I can view Patch Management, but I am unable to make any changes to it.
2. Controls access for devices a user can view.
	1. i.e., I am unable to view any Sites, Groups, or Devices from the All IT Shop

There is a preconfigured **Administrators** Team. Users assigned to this Team have full privileges and access to all systems.

