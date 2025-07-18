Auvik:

  

Generally, most alerts that are here do come into the support queue; however, some are very repetitive, so it may be worth watching weekly for the next few weeks to gauge consistency and severity.  
  
AWN:

  

One of our largest alert generators; daily monitoring is required.  
  

  

Cron Daemon:

  

Mostly alerting to changes in metadata and transactions. No actionable items within the last three weeks; loosely monitor here onward.

  

Dark Web Monitoring:

  

These are generated weekly across our clients. For at least the next few weeks, I'll take a look at this reports weekly to see if any action items should be taken, or if a ticket needs generated but there wasn't one. We have few clean bill of health emails come through, so I'd like that number to go up during my tenure.

  

DB Alerts (SQL2019 for ZAV):

  

Very few alerts (only 1 within the last month). It generally is quiet, and the only alert reported that an optimization job failed, which is not exactly actionable. Because of the low volume, this alert can be disregarded until one comes in (does not require frequent check-ins. HOWEVER, the SQL2019 server should be checked weekly for storage volume. I will likely create a recurring ticket for this task just to ensure that our runaway query problem is under control.

  

Datto Backup (BCDR):

  

Currently, the amount of alerts generated on a daily basis is at a very high volume. Currently, CDHE seems to be having issues with the hardware of their appliance. Our cloud solutions are generally not noisy and do not require extreme care. Modifications are being made to CDHE's backup environment, so we should see the noise decrease overtime. However, its important, at least until the changes are made and backups are rectified, to monitor these daily and compile general issues for Kaseya support when applicable. Our configurations are correct to our knowledge, otherwise. These are being forwarded to Centralized Services when tickets are generated for the foreseeable future, until a game plan is made to get their backups working appropriately.

  

Graphus:

  

These are mostly daily insight emails for each of our clients, which is actually useful to see the security stance of the organizations we monitor. This helps determine if one of our clients is being targeted by malicious actors, and how well Graphus is preventing and mitigating the behavior. It may be worth reviewing daily for the next week or so, then reviews can be consolidated to a weekly basis per client. This way, I can track a trend of their email security stance.

  

MS365:

  

At this point in time, all of these alerts are for Leanin' Tree specifically. They are all synchronization errors between the DC and AAD, mostly due to duplicate user accounts. This may be worth bringing to Tony's attention to reduce noise, but there is no critical issue to monitor here. When these come in, especially at this volume (once a day) I would say its safe to bring up with the POC to attempt to control the noise.

  

myITProcess:

  

No real alerts are being generated here at this current point in time, and requires no monitoring. 

  

ProofPoint:

  

ProofPoint alerts are about the same as Graphus in terms of their use, especially since they can be previewed and what have you. We also get active directory reports, which are helpful if they're changed. I think this could be reviewed daily and move to weekly as I get a trend going of the stance.

  

QuickPass:

  

After looking at these, I want to see if I can get them silenced. They don't seem to be of much benefit, and are only alerting on very few machines at once. I want to check into these errors, and hopefully reduce them.

  

SunQuest:

  

Not much in my purview from what it seems; I don't think there is much action I need or can take on these. I'll be ignoring them until a support instance with this vendor comes up.

  

  

Synology:

  

This is primarily for DPP. I think it would be worth looking into this. 9 times out of 10 its an alert that some of their firmware is out-of-date, which could become an issue for them the longer the updates sit. However, it is their one and only file share, so I understand the concern of taking it out of production for updates. We may be able to plan something, or they may switch to a different solution later.  

  

Spanning/Unitrends:

  

This is something I'd like to check daily for the next few weeks. I think its important to make sure that our backups are working correctly, even before I grab metrics for the scoreboard. I also want to troubleshoot backup issues as they come up, rather than waiting to discover them when I grab metrics.

  

  

VSAx:

  

There is a lot of noise here, and some less than relevant alerts. I'd like to go in and make adjustments to what alerts are warned, which are tickets, and which are just informational. In order to do that, I need to monitor this daily for the next few weeks, just to make sure I get an accurate idea of what alerts we can silence. Others might need to be actual tickets.

  

Misc Alerts:

  

RingCentral doesn't come in often, but when it does, I'll be checking them. Egnyte is the same way, assuming I have permission to access to appropriate Egnyte and RingCentral tenants.

  

EasyDMARC will become a larger part of the CS life in the near future, so I will be taking a gander at these weekly reports each Monday after the scoreboard.

  

Sucuri is nice to check to make sure a client's security stance is up to par. It serves a purpose to  

  

Ruckus occasionally sends update notices.  

  

vPenTest notifies us when tests are running and their status.  

  

UPS notifications are important and checked on a regular basis; I'd recommend creating inbox rules to ensure they're marked as important.  

  

05/20/2025 01:13 PM (last action 05/20/2025 08:06 PM)

note

time

attachment

edit

delete

2 Replies

KI

Khalid Ibrahim:
This looks good! Regarding Dark Web ID, there is an active integration with AT that automatically cr

This looks good! Regarding Dark Web ID, there is an active integration with AT that automatically creates a ticket whenever a compromised account is detected. This ensures that any potential threats are reviewed and addressed promptly. For Graphus, “Email 911” notifications are sent to the Managed Services email address whenever a user reports an email as phishing. These alerts are investigated, and if confirmed as malicious, we proceed to block the email—and if necessary, the associated domain—in Proofpoint at the global level to prevent future phishing attempts across all clients. I agree on disabling the Quickpass notifications for now, as we are not currently taking action on them. These alerts primarily relate to local account password rotations. We can revisit and re-enable the notifications in the future if we decide to utilize Quickpass’s privilege elevation feature on client workstations.