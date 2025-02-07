In VSA 10, you can use a configuration hierarchy to organize your machines into different Organizations, Sites, and Agent Groups to streamline agent deployment.

In order to do so, Organizations and their associated Sites and Agent Groups will need to be created first.

These can be created in: **Server Admin > Configuration**.

## Organizations and Sites

Organizations are top level objects that are generally associated with customers or your company.

Sites can be created within an organization, and are used for things like different departments or geographical locations.

Agents, however, should be used for things like physical location or OS type.


## Agent Groups

Agent groups are created in the same area as Organizations and Sites. This is a tertiary group. A custom MSI can be downloaded from the group, which has a special token that automatically associates a machine with that group. 

To download the MSI, select Server Admin > Configuration > Organization > Site > Agent Group, then the Downloads tab.