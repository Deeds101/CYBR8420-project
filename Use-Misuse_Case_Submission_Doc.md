## Use and Misuse Case Diagrams and Reflection
**Overarching Summary to Use/Misuse Analyses**
- TBD

**[Password Management Use/Misuse Analysis](https://github.com/Deeds101/CYBR8420-project/blob/main/Use-Misuses%20Case%20Diagrams/Final%20Diagrams/Password%20Management%20-%20Use%20and%20Misuse%20Case%20Diagram.PNG):**
 ![image](https://github.com/Deeds101/CYBR8420-project/assets/87542247/e8547fa6-b1e0-41a5-9d3b-fbdea9a0370b)

 SUMMARY: This abuse case analysis focused on the processes, controls, and threats that may impact the ITFLOW (software) from a password management perspective. As demonstrated within the diagram the data analyst (user) would most likely leverage the password management functions of the software for logging on to the system, changing passwords, and setting up new accounts. Review of system documentation and issue remediation documentation available through the [ITFLOW github page](https://github.com/itflow-org/itflow) it was determined that controls were in place to address a number of attack methods that may be carried out by a disgruntled employee. Despite these controls, it's important to consider that management of user access capabilities by an authorized System Admin internal to each organization leveraging this software to ensure internal information and capabilities are appropriately restricted to only active, authorized personnel.

  
**[SQL Injection Use/Misuse Analysis](https://github.com/Deeds101/CYBR8420-project/blob/main/Use-Misuses%20Case%20Diagrams/Final%20Diagrams/SQL%20Injection.drawio.png):**
![image](https://github.com/Deeds101/CYBR8420-project/assets/87542247/2a989453-0485-4e2b-88cf-5140a9a84ed9)


**[Email Tracker](https://github.com/Deeds101/CYBR8420-project/blob/main/Use-Misuses%20Case%20Diagrams/Final%20Diagrams/use%20misuse%20case%20(email%20tracking).png):**
![image](https://github.com/Deeds101/CYBR8420-project/blob/main/Use-Misuses%20Case%20Diagrams/Final%20Diagrams/use%20misuse%20case%20(email%20tracking).png)

SUMMARY: In reviewing the forum for ITFlow, there was a ticket created for them to address an issue where an email was sent into the IT Helpdesk for a company and it continually created new tickets within the ITFlow dashboard. This could potentially cause problems if the emails were automatically routed to the folder to create a ticket, and since the parser runs with a cronjob, it could easily overload the dashboard, and eventually the IT Helpdesk workers. According to the forum, this issue was fixed with a code push 5 days ago.

**Project Board: [ITFLOW Use-Misuse Projects](https://github.com/users/Deeds101/projects/3/views/1)**

**Individual Contributions:**
- Adam McAlpine (Atmcalpine): Developed Password Management Diagram, provided feedback on team-mate diagrams, aided in the development of the markdown document, and actively engaged in team discussions.
- Kendra Herrmann (kdherrm88): Developed Email Tracker Diagram as well as provide feedback on teammate's diagrams. Assisted the team with markdown documentation and attended team meetings and engaged in discussion.

**Reflection:**
- This project was easier to coordinate as each team member was able to take a misuse case and develop diagrams on their own time.  During this time, periodic team updates were held to discuss the progress of these diagrams as well as any questions or concerns.  During this process issues were experienced in relation to the use of the project boards for which there were some technical issues largely involved with access capabilities for moving projects along to the different phases (e.g., in-progress, done, etc.).  These issues were largely mitigated by having the Team Lead who had access move projects to the different phases as they progressed.  An additional issue experienced was properly understanding the level of detail and in-depth analysis expected from this assignment.  A discussion with the professor did assist in gaining a better level of understanding of what was expected, but the team from that 15 minutes was not a sufficient amount of time to address all the necessary diagrams and questions involved with this assignment.  To address future system issues, the team will largely have to wait to see what the future projects will involve; however, if there are questions/issues experienced we will work to either email the professor with these questions or ensure they are addressed during the team check-in times.  In addition, if the time to meet with the professor is not considered sufficient we will attempt to schedule a secondary meeting to ensure all questions/concerns can be addressed in a timely manner.
