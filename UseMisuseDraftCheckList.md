# Assignment Part 1

## Here is what your team will need to accomplish. Build a markdown report that describes the following:

[] Identify five to six (depending on team size) essential interactions of your open-source software (system-of-interest) with its environment of operation. You will most likely identify these interactions based on the enabling systems or other systems in your systems engineering view (previous assignment). Ideally, the interactions would be spread across your software's different external interactors (humans or systems). Once different external interactors have been identified, the interactions can focus on the most critical features used by the external interactor.\
[] Develop use-cases diagrams of the five interactions. The use-cases should be about features supported by your software (system of interest). Keep these diagrams simple and avoid introducing complexity early.\ 
 - You may use the following sample file to have quick access to shapes for a use case diagram in https://app.diagrams.netLinks to an external site. 
 - Use Case Sample.drawio Download Use Case Sample.drawio 
 - For each use case, derive security requirements using misuse case analysis. 
 - The misusers should be contextualized in your environment of operation and relevant to the interactions identified above. Use names for misusers that help the reader understand their motives, resources, attack of choice, and the available access to the system to carry out their attack.
 - Here is a sample file to have quick access to shapes for a use/misuse case diagram in https://app.diagrams.netLinks to an external site.:
 - Use-Misuse Case Sample.drawio Download Use-Misuse Case Sample.drawio  
 - Iterate between use and misuse cases to elaborate additional security functions. This step is important to derive quality security requirements. Embed the final diagram in your report.
 - Diagraming Advice: Use proper notation as discussed in class materials. Use cases should focus on software features. Go back and forth between use case and misuse case analysis until specific functional security requirements that are implemented by the software can be identified. For misuse cases, prioritize mitigations that are implemented in the OSS project, instead of the environment. Make sure use cases address all misuse cases. Arrange the diagram appropriately to reduce clutter.
 - Assess the alignment of security requirements derived from misuse case analysis with advertised features of the open-source software. Review OSS project documentation and codebase to support your observations. Provide a summary of your findings.\

[] *Show your internal project task assignments and collaborations to finish this task in a Github Project Board.*\
[] Provide a link to this board.\ 

**Project Board: [ITFLOW Use-Misuse Projects](https://github.com/users/Deeds101/projects/3)**

[] Include a summary of your individual contributions.\

**Individual Contributions:**
- Adam McAlpine: Developed Password Management Diagram, provided feedback on team-mate diagrams, aided in the development of the markdown document, and actively engaged in team discussions.
- Kendra Herrmann: Developed Email Tracker Diagram as well as provided feedback on teammate's diagrams. Assisted the team with markdown documentation and attended team meetings and engaged in discussion.
- 
[] Include a reflection of your teamwork for this assignment. What issues occurred? How did you resolve them? What did you plan to change moving forward?

**Reflection:**
[] This project was easier to coordinate as each team member was able to take a misuse case and develop diagrams on their own time.  During this time, periodic team updates were held to discuss the progress of these diagrams as well as any questions or concerns.  Durring this process issues were experiences in relation to the use of the project boards for which there were some technical issues largely involved with access capabilities for moving projects along to the different phases (e.g., in-progress, done, etc.).  This issues were largely mitigates by having the Team Lead who had access move projects to the different phases as the progressed.  An additional issue experienced, was properly understanding the level of detail and indepth analysis expected from this assignment.  A discussion with the professor did assist in gaining a better level of understanding of what was expected, but the team from that 15 mins was not a sufficient amount of time to address all the necessary diagrams and questions involved with this assignment.  To address future system issues, the team will largely have to wait to see what the future projects will involve; however, if there are questions/issues experiences we will work to either email the professor with these questions or ensure they are addressed during the team checkin times.  In addition, if time to meet with the professor is not considered sufficient we will attempt to schedule a secondary meeting to ensure all questions/concerns can be addressed in a timely manner.

# Assignment Part 2

## Continue to develop your markdown report further with the following:

[] Review OSS project documentation for security-related configuration and installation issues. Summarize your observations.
 - The purpose of this task is to review security-related documentation of the project and find ways to improve it. Open source projects are always looking for contributors for their documentation. It may also allow you to get to know the open source community and procedures to contribute.

**[Password Management Use/Misuse Analysis](https://github.com/Deeds101/CYBR8420-project/blob/main/Use-Misuses%20Case%20Diagrams/Final%20Diagrams/Password%20Management%20-%20Use%20and%20Misuse%20Case%20Diagram.PNG):**
 ![image](https://github.com/Deeds101/CYBR8420-project/assets/87542247/e8547fa6-b1e0-41a5-9d3b-fbdea9a0370b)

 SUMMARY: This abuse case analysis focused on the processes, controls, and threats that may impact the ITFLOW (software) from a password management perspective. As demonstrated within the diagram the data analyst (user) would most likely leverage the password management functions of the software for logging on to the system, changing passwords, and setting up new accounts. Review of system documentation and issue remediation documentation available through the ITFLOW github page it was determined that controls were in place to address a number of attack methods that may be carried out by a disgruntled employees. Despite these controls, it's important to consider that management of user access capabilities by an authorized System Admin internal to each organization leveraging this software to ensure internal information and capabilities are appopriately restricted to only active, authorized personnel.


**[SQL Injection Use/Misuse Analysis](https://github.com/Deeds101/CYBR8420-project/blob/main/Use-Misuses%20Case%20Diagrams/Final%20Diagrams/SQL%20Injection.drawio.png):**
![image](https://github.com/Deeds101/CYBR8420-project/assets/87542247/2a989453-0485-4e2b-88cf-5140a9a84ed9)

