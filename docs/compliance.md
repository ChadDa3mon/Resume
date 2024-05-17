---
tags:
  - Python
  - Gradio
---
This project showcased a popular web-based interface for Python called Gradio. 

# Problem
Our compliance team has to manually create tasks for our firewall engineers to ensure around 200 firewalls are audited every 90 days. This was a very manual task and heavily prone to human error. 

# Solution
I developed a python app with a web based front end. This allowed them to simply upload a report from ServiceNow (Excel) and the automation took care of the rest. 

It would first look for devices that haven't been audited in more than 90 days. For each device it found, it would then
- Verify there are no known outages for that device
- Create a ticket and fill in the relevant details
- Assign the ticket to the appropriate team for execution

# Result
A monthly task that took a team over 8 hours now takes around 20 minutes. 