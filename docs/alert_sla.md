---
tags:
  - Slack Bot
  - Python
---
This project was a simple integration with my slack bot. 

## Problem
A team was committed to a 90 minute response SLA for certain alerts that came into their SIEM. Due to the volume of alerts they were often missing these key alerts and had an SLA compliance of around 75%. 

This SLA had financial penalties involved, so they came to me to ask for help alerting them if one of these alerts had been sitting for more than 50% of the SLA without assignment. 

## Solution
I implemented a python micro-service that runs in our OpenShift (Kubernetes) platform and checks the status of all alerts every 2 minutes. If a given alert had not been touched for more than 45 minutes it sent a slack notification to their team channel. 

## Results
Almost overnight, SLA compliance went from 74% to 96%. 