---
tags:
  - Python
  - Selenium
  - ServiceNow
---

Another example of just how powerful Selenium can be. 

# Problem
We had a large customer of ours who wanted us to manually create tickets in their ServiceNow instance every time a security incident was raised in our system for them. Basically manually cloning the details of the security incident from our system into their system. 

While normally we'd just build an integration between the two instances, they refused that solution and insisted our staff log into their ServiceNow to manually do the work. 

Not only was this a massive time sink for us (happening several times a day) but it also opened us up to the risk of cross-contamination, where someone accidentally copies the details from the wrong customer into this instance. 

# Solution
A custom python app that their team could run from their laptops. 
- Upon running the application they would be prompted to enter the security incident number. 
- The application would then retrieve the details of that security incident and verify it was for the proper customer, thus eliminating the risk of cross-contamination. 
- It then launched a new browser via Selenium and prompted them to enter their login information for the customer's ServiceNow instance. 
- Once logged into the customer's instance, the automation would automatically create the incident and fill in all of the details from our system. 

# Result
This was a big success. A task that normally took 10 to 15 minutes and had a moderate chance of human error now takes 2 to 3 minutes and virtually eliminates our risk exposure. 