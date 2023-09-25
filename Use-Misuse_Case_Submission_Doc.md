Assignment Two - Use and Misuse Cases
/home/doom/Downloads/SQL Injection.drawio.png

## Use and Misuse Case Diagrams and Reflection
**[Password Management Use/Misuse Analysis](https://github.com/Deeds101/CYBR8420-project/blob/main/Use-Misuses%20Case%20Diagrams/Final%20Diagrams/Password%20Management%20-%20Use%20and%20Misuse%20Case%20Diagram.PNG):**
 ![image](https://github.com/Deeds101/CYBR8420-project/assets/87542247/e8547fa6-b1e0-41a5-9d3b-fbdea9a0370b)

 SUMMARY: This abuse case analysis focused on the processes, controls, and threats that may impact the ITFLOW (software) from a password management perspective. As demonstrated within the diagram the data analyst (user) would most likely leverage the password management functions of the software for logging on to the system, changing passwords, and setting up new accounts. Review of system documentation and issue remediation documentation available through the ITFLOW github page it was determined that controls were in place to address a number of attack methods that may be carried out by a disgruntled employees. Despite these controls, it's important to consider that management of user access capabilities by an authorized System Admin internal to each organization leveraging this software to ensure internal information and capabilities are appopriately restricted to only active, authorized personnel.

**[SQL Injection Use/Misuse Analysis](https://github.com/Deeds101/CYBR8420-project/blob/main/Use-Misuses%20Case%20Diagrams/Final%20Diagrams/SQL%20Injection.drawio.png):**
![image](https://github.com/Deeds101/CYBR8420-project/assets/87542247/2a989453-0485-4e2b-88cf-5140a9a84ed9)


-Email Tracker: Kendra Herrmann\
<img width="560" alt="image" src="https://github.com/Deeds101/CYBR8420-project/blob/main/Use-Misuses%20Case%20Diagrams/Final%20Diagrams/use%20misuse%20case%20(email%20tracking).png">
In reviewing the forum for ITFlow, there was a ticket created for them to address an issue where an email was sent into the IT Helpdesk for a company and it continually created new tickets within the ITFlow dashboard. This could potentially cause problems if the emails were automatically routed to the folder to create a ticket, and since the parser runs with a cronjob, it could easily overload the dashboard, and eventually the IT Helpdesk workers. According to the forum, this issue was fixed with a code push 5 days ago.
