This is primarily the pre-deployment section, which preps you for the Deployment Specialist track.

There is a three tier hierarchy:
- Account: The entire estate
- Site: Customers, generally. The middle management level.
- Device: The actual device itself. ESXi hosts, servers/workstations, and even SNMP equipment are supported.

Devices can be organized at the account OR site level in two ways:
- Device filters: Identifies devices based on specific criteria, which is dynamic. These can be customized, but there many predefined filters available.
- Device groups: Collections of devices that filters are not granular enough for, but are static and need to be added to manually in the web portal.

DRMM is based on an agent that runs on devices, excluding SNMP and ESXi hosts. It can:
- 