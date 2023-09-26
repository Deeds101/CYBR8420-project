## Use and Misuse Case Diagrams and Reflection

# Part 1

**[Password Management Use/Misuse Analysis](https://github.com/Deeds101/CYBR8420-project/blob/main/Use-Misuses%20Case%20Diagrams/Final%20Diagrams/Password%20Management%20-%20Use%20and%20Misuse%20Case%20Diagram.PNG):**
 ![image](https://github.com/Deeds101/CYBR8420-project/assets/87542247/e8547fa6-b1e0-41a5-9d3b-fbdea9a0370b)

 SUMMARY: This abuse case analysis focused on the processes, controls, and threats that may impact the ITFLOW (software) from a password management perspective. As demonstrated within the diagram the data analyst (user) would most likely leverage the password management functions of the software for logging on to the system, changing passwords, and setting up new accounts. Review of system documentation and issue remediation documentation available through the [ITFLOW github page](https://github.com/itflow-org/itflow) it was determined that controls were in place to address a number of attack methods that may be carried out by a disgruntled employee. Despite these controls, it's important to consider that management of user access capabilities by an authorized System Admin internal to each organization leveraging this software to ensure internal information and capabilities are appropriately restricted to only active, authorized personnel.

  
**[Database Security Use/Misuse](https://github.com/Deeds101/CYBR8420-project/blob/main/Use-Misuses%20Case%20Diagrams/Final%20Diagrams/SQL%20Injection.drawio.png):**
![image](https://github.com/Deeds101/CYBR8420-project/assets/87542247/2a989453-0485-4e2b-88cf-5140a9a84ed9)

SUMMARY: Database attacks are so hot right now. According to past issues, SQL injection was an attack that IT Flow was vulnerable to, which was corrected. IT Flow also encrypts dataflow and APIs, whcih protects against generic theft of data. Currently, an attacker could compromise an inactive account and use to gain access to the system. An account purge would be an effective means of mitigating this attack. Removing old, inactive, or termed employee accounts would be an important event to factor in.


**[Email Tracker](https://github.com/Deeds101/CYBR8420-project/blob/main/Use-Misuses%20Case%20Diagrams/Final%20Diagrams/use%20misuse%20case%20(email%20tracking).png):**
![image](https://github.com/Deeds101/CYBR8420-project/assets/107895832/724632b6-9074-4889-9f35-33e10278712b)


SUMMARY: In reviewing the forum for ITFlow, there was a ticket created for them to address an issue where an email was sent into the IT Helpdesk for a company and it continually created new tickets within the ITFlow dashboard. This could potentially cause problems if the emails were automatically routed to the folder to create a ticket, and since the parser runs with a cronjob, it could easily overload the dashboard, and eventually the IT Helpdesk workers. According to the forum, this issue was fixed with a code push 5 days ago.

**[Role-Based-Access-Control](https://github.com/Deeds101/CYBR8420-project/blob/main/Use-Misuses%20Case%20Diagrams/Final%20Diagrams/RBAC_Final.PNG):**
![image](https://github.com/Deeds101/CYBR8420-project/assets/107895832/55611867-6c4f-476c-a120-e4db54dff2cc)


SUMMARY: I was searching the forums for features that were going to be implemented or bugs that needed squashing. I read over a couple of cases that intersected with a need for a Role-based access control system. One of the bugs that I read on the forums, as well as being pointed out by my project team, is that a Security Researcher discovered that the code is vulnerable with an SQL injection on the client page, this got fixed. There was also an IDOR vulnerability with the fact that people could visit vital site pages if they had a valid URL, This got put in the release milestone 1.0.

**[Billing](https://github.com/Deeds101/CYBR8420-project/blob/main/Use-Misuses%20Case%20Diagrams/Final%20Diagrams/Use-Misuse%20Case%20Billing.png):**

![image](https://github.com/Deeds101/CYBR8420-project/assets/143226996/3b168fc1-ce4d-4a61-aa3e-32145dee706e)

SUMMARY: One of the core components of the ITFlow software is the Sales and Billing portion. At the heart of this component is the billing functionality which allows you to create and track invoices then send out requests for payment. My goal with my Use-Misuse case diagram was to document potential ways the Billing feature could be exploited. Since the tool consists of mostly internal components, I used the lens of a rogue employee as the attack actor. From this viewpoint, I documented potential attacks that could be done to the Billing system and various features or designs which would help mitigate against the rogue employee. Through a robust backup, auditing, and role framework, a majority of the attacks that I foresaw could be prevented. 

**[MFA](https://github.com/Deeds101/CYBR8420-project/blob/main/Use-Misuses%20Case%20Diagrams/Final%20Diagrams/MFA%20Final%20Case.PNG):**

![image](https://github.com/Deeds101/CYBR8420-project/assets/104231228/5e79db77-72d9-4df8-b5e1-ef8ed8ee027d)

SUMMARY: One of the bigger possible flaws of ITFlow, and as it is seen being voiced on the forums for the OSS, is the lack of a forced MFA or second level verification for IT users of this platform. With no second level login security, there arises multiple possible security exploits as well as possible simple hashing cracks to get into an account of the backend of the system. There is an option to opt into the MFA but without the force, it leaves the vulnerability of "it only takes one" to allow an attacker to breach the system and attain possible high value and private information. If, in our system environment of a hospital, private patient info is easily accessible, the amount of money ransomware attackers will hold it for is much more than your average attack. And with MFA being able to be an opt in feature, it sounds like a possible thought thrown on the backburner of a security vulnerability waiting to happen. The simplest way to resolve this would be to just force an MFA upon login and have that MFA feature have a decent encryption.

**Project Board: [ITFLOW Use-Misuse Projects](https://github.com/users/Deeds101/projects/3/views/1)**

**Individual Contributions:**
Each individual wrote the summary for their respective diagram.

- Adam McAlpine (Atmcalpine): Developed Password Management Diagram, provided feedback on team-mate diagrams, aided in the development of the markdown document, and actively engaged in team discussions.
- Kendra Herrmann (kdherrm88): Developed Email Tracker Diagram as well as provide feedback on teammate's diagrams. Assisted the team with markdown documentation and attended team meetings and engaged in discussion.
- Ryan Thompson (DoomDragoon): Developed Diagram for database security. Provided and received feedback on issues and discussions. Scheduled additional team meetings to facilitate engaging collaboration and development of diagrams and markdown document review. Ensured deadline was met and all requirements were completed to the best of our understanding.
- Joseph Diedrichsen (Deeds101): Developed RBAC diagram as well as provided feedback on this week's project milestone. Reviewed the codebase to see if there were any more bugs that stood out. Attended team meetings as well as participated in and made a discussion board for further collaboration.
- Corey Mekelburg (Cojajomaco) - Developed Billing Diagram, provided feedback on teammate's diagrams, engaged in discussions, and assisted with markdown documentation. Absent for team meeting due to a vacation taking place during the scheduled time.
- Brevin Wagner (bdog711998): Developed MFA Diagram, provided feedback and colaboration on teammate's and selfs diagrams, attended avilable team meetings and took and gave constructive feedback and assistance from everyone.

**Reflection:**
- This project was easier to coordinate as each team member was able to take a misuse case and develop diagrams on their own time.  During this time, periodic team updates were held to discuss the progress of these diagrams as well as any questions or concerns.  During this process issues were experienced in relation to the use of the project boards for which there were some technical issues largely involved with access capabilities for moving projects along to the different phases (e.g., in-progress, done, etc.).  These issues were largely mitigated by having the Team Lead who had access move projects to the different phases as they progressed.  An additional issue experienced was properly understanding the level of detail and in-depth analysis expected from this assignment.  A discussion with the professor did assist in gaining a better level of understanding of what was expected, but the team from that 15 minutes was not a sufficient amount of time to address all the necessary diagrams and questions involved with this assignment.  To address future system issues, the team will largely have to wait to see what the future projects will involve; however, if there are questions/issues experienced we will work to either email the professor with these questions or ensure they are addressed during the team check-in times.  In addition, if the time to meet with the professor is not considered sufficient we will attempt to schedule a secondary meeting to ensure all questions/concerns can be addressed in a timely manner. There were also issues for our team with the timing of the assignment being released. Since our team meets on Tuesdays, generally when the assignment is given on a Monday this is not an issue but when the assignment comes out later in the week, we are unable to start it as a team until our next meeting time since our team is comprised of people who have full-time jobs and are involved in other activities outside of graduate school work. In the future, this could be alleviated via a secondary meeting, but as mentioned, our team is comprised of people who have full-time jobs and are involved in other activities outside of graduate school work and that will make a secondary meeting difficult. It could be helpful to have all of the necessary requirements/assignments due for the week released on the same day to allow enough time for all teams to meet these requirements. 

# Part 2
**Overarching Summary to Use/Misuse Analyses**

Setting up a VM to host IT Flow was not that difficult, it would have been helpful if an in-depth explanation for the process was more fleshed out regarding the public.pem and private.key with OpenSSH.  Configuing ITFlow was not that difficult either, again it would have been more helpful to have a thourough explanation of the of the process. In the documentation of ITFlow, the creators have helpful links that redirect to forums and websites. It would be beneficial to include these in the installation page, to facilitate a smooth installation process. One the more colorful interactions we found was regarding an SQL injection attack. This is a common attack that should be fairly easy to mitigate with input validation. This calls into question what kind of protection the software has against other database attacks. The softwares most valuabel asset will be its database, which could potentially hold thousands of records regarding customer information. Role based access would mitagte this, which is currently being developed, as well as effective backups in the event of the database being held for ransom. Over-privledged accounts is also another common way for hackers to gain entry, which can be mitigated with a GRC system that calcualtes risk based on how privledged an account becomes. This is standard practice with ERP systems, such as SAP, that deal with billing and invoicing and the same should be expected with IT Flow.
