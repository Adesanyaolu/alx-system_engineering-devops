# Postmortem Report
## Issue Summary
The merchants' support portal broke down and refuse to load. The issue started at about 9 am (CAT) on a Wednesday, 10/08/2022. The issue was resolved around noon (CAT). This resulted in most users not being able to log into their profiles to attend to their chargeback claims within this period. The root cause was an overload on one of the profiles that were leading to a timeout while the page was loading. This profile has over 100 emails in its profile.

## Timeline
The downtime started at about 9:16 am (CAT) One of the account managers notified the team around 10 am (CAT) The downtime lasted for about 2 hours. The team swung into action by passing the complaint to the lead software engineer. Merchant report to have gained back access to the portal around 12 pm (CAT).

## Root Cause
The issue was caused by a customer I profiled at the end of the working hours on the previous day. The customer had multiple emails registered on the profile. Sending reports to these emails simultaneously caused the timeout while the portal was loading.

## Resolution and Actions Taken
Took the lead engineer about 2hrs to discover the root of the problem (didn't know how he did that). I guess he found out through the backend.

The multiple emails of the customer were compressed into one group mail.

This resolved the issue and the portal got back to working effectively.

PS: I use to think postmortem is only a medical term, never knew it could be used in the tech world. If you are like me, now you know.
