---
tags:
  - Python
  - Gradio
---

This was something built to help out a coworker. It is a python application with a GUI (Gradio) that she runs locally from her laptop. 

# Problem
Once or twice a week she had to update multiple drop down entries in ServiceNow which was a very time consuming task. Due to the setup of our ServiceNow instance, this had to be done by someone with administrative privileges so we couldn't really offload this to other teams. 

# Solution
The data came to her in a spreadsheet with dozens of columns and hundreds of rows in various tabs. I built a python application with a GUI where she could simply upload that spreadsheet and the application would then query ServiceNow to see what needed to change. 

It then presented the proposed edits to her for review, and if she was happy with things it would automatically make all of the changes in ServiceNow. 

# Result
A process which used to consume 5 to 8 hours of her week, each and every week, now takes around 30 to 40 minutes. 