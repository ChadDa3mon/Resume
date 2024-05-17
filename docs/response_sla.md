---
tags:
  - Python
  - Slack Bot
  - ServiceNow
  - Kafka
---

# Problem
We have a 60 minute response SLA for customer updates in our portal, meaning we have to respond to their request within 60 minutes. 

We had no easy way of notifying people when these updates came in or what the update was. 

# Solution
I built a Slack Bot in python that runs in our OpenShift cluster (Kubernetes). Along with an Event Driven Automation utilizing Kafka and triggers in ServiceNow. 

This ensures that people get instant and meaningful notifications as soon as the update comes in. The slack notification contains all of the details they need to quickly respond, along with a link to the ticket itself so they can easily load things. 

# Result
Substantial improvement to our response times and overall staff morale. This slack bot is now sending over 500 messages per day to various users and channels and has received tremendous feedback. 