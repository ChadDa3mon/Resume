---
tags:
  - Ansible
---
This project was led by me by developed by our core Ansible team as the necessary skills were a bit above my level. 

# Problem
As an MSSP we interface with a very wide variety of devices from dozens of different vendors. When using tools like Ansible Tower this means someone has to be familiar with every plugin for every vendor if they want to create automations. 

It also means the output given back to a user is different for each vendor. 

Imagine this: You support 5 different firewall vendors and you want to write automations that work for all of them. For example, you need to review the routing table, or network interfaces. 

With the default way of handling things in Ansible, you would have to write 5 different playbooks and then figure out how to parse the output from 5 different vendors. It was a nightmare to handle automations at scale. 

# Solution
I developed a common framework where our Ansible team had to simply write an adapter for each vendor. This adapter ensured the query was the same, regardless of the vendor you were working with (Checkpoint or Cisco) and the output was consistant. 

With this new framework, our internal users and automation developers can simply specify the *Device ID* in their query and our framework handles the rest. 

Now, you can just say "Get the routes for Device123" and not have to worry if Device123 is a Checkpoint, Cisco, Palo Alto etc. You will also get back a normalized output that you can parse. 

# Result
This made it substantially easier for our automation developers to write playbooks in Ansible that support multiple vendors. 

New automations in Ansible can easily be written in a few days instead of weeks. 