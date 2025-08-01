- Routine maintenance can be easily established through jobs and components.
	- Component: package containing a script, and may include file attachments.
	- Job: the mechanism used to deploy and run one or more components
- Two types of jobs:
	- Quick job: Run one component immediately. Can be run against one or more individually selected devices or sites, and runs under the system user context only.
	- Scheduled job: Run multiple components at a specific point in time, and can be recurring or triggered when devices are first onboarded. It can be targeted against devices, sites, filters, or groups, and can be set to run as the logged-in user.
- The web portal signals the targeted devices that a job needs to be run, then the agent downloads and executes the components.
- ComStore applications are divided into categories:
	- Applications: Installers, typically.
	- Scripts
	- Integrations and Extensions
	- Device monitors
- Only application and script components can be run within jobs.
- You can create your own jobs, and share/collaborate with others globally with the community forum.
- Users can run their own components if they are assigned as user tasks; this can be automatic remediations users can do themselves with one click so they don't need to open a ticket, like restarting a print spooler or clearing disk space. It will show in the agent browser under the tasks tab. Admin privileges are not required.