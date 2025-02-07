VSA 10’s Network Monitoring gives you total visibility across your network. With automatic discovery and diagramming, managing the network becomes simple, intuitive, and efficient.

## Creating a Network
Creating a Network is simple. 
1. Navigate to: Networks > Manage > Create Network.
2. Probe & Custom Subnets. Here, the User can choose the Probe machine. In addition, the User can define Custom  Subnets to be scanned by the Probe to discover devices for the network. This is important to ensure that the scanning process happens in a timely matter by not scanning irrelevant portions of the network. 
3. Notifications. In addition, the User can also configure basic Notifications for when new devices are added to the network and also in the absence of devices.

## Network Topology Maps: Functionality
A comprehensive view of the network is essential – and a network topology map can provide this!

By visualizing the network’s devices, their interconnections, location, and interdependencies, administrators can monitor network devices, proactively identify failures/bottlenecks, and ensure better disaster recovery and business continuity.

You can also perform basic troubleshooting of devices directly from the topology map i.e rebooting a device.

Once the network is created and the associated devices are discovered, the **Network Topology Map** is generated.

The **Topology Map** screen also presents some summary information on the network at the bottom of the screen. 

Also, at any point in time, the original network discovery settings that were entered while creating the **Network** can be edited by clicking on the **Edit** icon on the bottom right corner of the **Topology Map** screen.

On hovering over the **Probe** (or any device), summary information about the device will be displayed:

- Is it online or offline?
- If online, how long has it been online?
- How many alerts are associated with this device?

On clicking on the **Probe** (or any network device), a right panel opens up with details of the machine.

On this right panel, by clicking on **See System Details**, a new tab will open up with the complete **Probe** machine information on the **Systems** screen.

On right-clicking any **Device** on the network, the system generates options to:

| **Edit**   | Rename/change the Device Type                                                                                                                                                                                                       |
| ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Enroll** | Enroll as a Managed Network Device                                                                                                                                                                                                  |
| **Move**   | Shift the Device to another part of the Network                                                                                                                                                                                     |
| **Hide**   | Eliminate the visibility of Devices that are no longer relevant.  <br>  <br>Devices on the Topology Map can be hidden - either individually or as whole clusters. A user can later **Show** (or un-hide) previously hidden devices. |
When the User clicks on the three dots in the right panel of each **Cluster/Device**, the system generates options to: 

- Edit (Device only)
- Enroll / Un-enroll (Device only)
- Open SSH terminal - if the device has SSH support (Device only)
- Rename (Device and Cluster)
- Add a custom device (Cluster only)
    - The User can add a Device manually to a Cluster using this option (in cases such as  Discovery not picking up a device or if the User does not want a scan to occur and so on). 
    - If the User knows its MAC address, the Device can be added manually. During the next scan, if this manually added custom device is discovered, the system will auto-reconcile i.e. there will be no duplicates.  
    - _Please note: To ensure that the Custom Device is reconciled during the next scan, make sure to **Edit** it and add the MAC address._

On enrolling a Device, the User has the option to enable an **Offline Notification** setting for that Device. 

The Device does not need to have SNMP enabled in order to support this offline notification setting, as it is based on a Ping test.

_Please note: It is recommended that the Offline Notification be enabled for the Probe. If this setting is not enabled and the Probe goes offline, Users will receive a surge of offline notifications for each of the devices mapped to the Probe._

If a certain Device Type is not recognized, it classifies the same as an **Unknown** Device and groups all **Unknowns** together. 

For each Unknown Device, the user can manually define the Device Type with ease, by right-clicking on the Device and choosing the **Edit** option. 

 The user can try and identify the Device Type of an Unknown Device using its IP address and MAC address displayed in the Topology Map. 

Once an Unknown Device is classified into a known Device Type by the user, it gets automatically added to the respective Cluster.

There is also an option to classify a Device as a **Custom** Device Type. 

Once a user does so, the device will have its own Cluster. It will not be grouped with other Custom devices (if any). That is, each Custom Device Type will have its own individual Cluster.

## Network Topology Maps: Nesting Devices

The Network Topology Map also offers the capability to perform **nesting of devices** as per user preferences. 

VSA 10 provides users with the capability to **Cluster / Group** the nodes on the Network Topology Map in the way that makes the most business sense to them. In other words, VSA 10 empowers each user with _perspective-based visibility_.

VSA 10 supports SNMP monitoring through the configuration of SNMP Profiles, which is a centralized configuration of SNMP-related variables and alerts.