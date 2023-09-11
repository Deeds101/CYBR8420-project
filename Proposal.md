## CYBR8420-project

## Project Team Name: Channel Four News Team
### **Channel Four News Team : https://github.com/Deeds101/CYBR8420-project.git**


# Team: 
- Ryan Thompson - Team Lead
- Joseph Diedrichsen - Technical Analyst
- Kendra Herrmann - Scribe/Documentation
- Corey Mekelburg - Reviewer/QA
- Adam Mcalpine - Project Manager
- Brevin Wagner - Technical Analyst

## **Project: [IT Flow](https://github.com/itflow-org/itflow)**

**Operational Environment:** Managed Service Providers (MSPs) are widely used by small to medium sized businesses. While these businesses are often times of targets of cyber attacks, MSPs allow attackers to exploit a single vulnerability that can have expansive affects on multiple businesses.  As a result, ITFlow will need to ensure a secure connection can be established for the secure handling of confidential information.  This may be accomplished by allowing the software to be downloaded onto the client's internal network or operated externally via a website. Regardless, ITFlow will need to ensure adequate converage to ensure client passwords and data is properly secured while ensuring consistent availability to users. 

# **Diagram of Software System**
<img width="560" alt="image" src="https://github.com/Deeds101/CYBR8420-project/assets/87542247/818b8055-7ce7-4fb5-b9e1-4c08f86e6bcb">



**Threats Percieved by Users:**
* Inadequate backup and recovery capabilities
* Loss of documentation
* Lack of vulnerability and patch Management
* Ransomware
* Lack of Availability
* Unauthorized Access

**List of Security Features:**
* Account Logins
* Role-based access control
* Password Encryption (AES)
* Security Alerts
* FIDO2 WebAuthn Support for passwordless authwntiation, Fingerprint, USB hardware key authorization (In Progress)
* MFA (In Progress)

**Motivations:**  MSP software is vital to hundreds of small and medium sized companies in order to help them manage a varied client base that contains a myriad of hardware, software, and policies. ITFlow is a software that aims to compile company passwords, documentation, and financing information all in one portal to make MSP management more accessible. This kind of software is of vital importance to an MSP and is one of their most targeted assets by threat actors. In addition to the software being a target and source of risk for an MSP, MSPs themselves are a watering hole for attackers and adversaries since they hold the "keys to the kingdom" of many other targets. If an MSP is compromised, it can be assumed that each of their clients will be compromised, as well. Unfortunately, not every MSP is able afford security-rich software such as ITGlue to help them maintain or improve their security posture. ITFlow is an open-source solution for smaller, growing businesses to assist them in managing and securing their clients. Our team member, Corey Mekelburg, works at an MSP professionally and has a good understanding of how they work and what kind of security they need. We hope this will be an excellant contribution to Quality Assurance of the open source project.

# **Security** 


**Open Source Project Description**
ITFlow is a software that consolidates common MSP needs into one system; including IT Documentation, ticketing, and billing. ITFlow is self-hosted and includes the ability to be accessed via a web browser. Currently, ITFLow is in Beta and has had 13 contributors to help build the project out in PHP, CSS, and JavaScript. Edits have been committed to GitHub for this project within the last week (week of 9-8-2023). Documentation for ITFlow can be found on it's public GitHub, referenced above. 

**Licensing Agreements:**
ITFlow is distributed "as is" under the GPL License, WITHOUT WARRANTY OF ANY KIND.  This is a free, copyleft license that allows users to modify and reuse the software without any restrictions.  The only condition is that all modifications must be made freely available to other users.

**Contributor Agreement:**
Contributors are to fork the repo and create a pull request.  While making contributions, individuals are to follow the code of standards (https://docs.itflow.org/code_standards).  A discussion is to be held with the other contributors if larger changes/new features are expected to be implemented.

**Process for making contributions:**
If a security issue is discovered, it is to be reported to [report it](https://github.com/itflow-org/itflow/security/advisories/new)  Expect to receive an initial acknowledgement within 72 hours.

**Security History:** This open-source project has a robust reporting feature that will make it easy to notify the owners that there is a security incident.

ITFlow has had two separate security advisories that the public is allowed to see.
March 5, 2023: Persistent XSS 

Impact:
ITFlow (Beta commits prior to 75da31d) is affected by persistent XSS vulnerabilities.
An authenticated application user could execute arbitrary web scripts or HTML in the browser context of other application users by injecting a crafted payload.

May 12, 2023: Authenticated users can craft a POST request to delete any file on the webserver

Impact:
- Loss of availability
- Catastrophic consequences if the webserver administrator is lazy and has www-data in the sudoers file
- https://demo.itflow.org/ could potentially be taken down along with any other websites in the web directory
- Security breach in division of account roles (for example, the Expenses page and expenses-related functions should not be available to technicians)


**Reflection:**
The main point of contention amongst our team was finding a scheduled time to work on the project. We have a diverse background of students working on this project - parents, full-time employees, coaches, and hobbyists. This diversity provides for an enriching experience, however, it also required more effort to be put into the planning phase of our project. It should be a testament to our teamwork that we were able to successfully find a timeslot for us to work together in a continued fashion. It is to be expected that scheduling may become an issue again in the future, as plans change, but we as a group have decided that we will need to be lenient and flexible in order to reach our deadlines. Our software, ITFlow, had a projected date of July 2023 for a 1.0 release, they are shooting for a stable release soon. This will effect how we approach our security evaluation. There will be flaws, but the focus will be on whether or not the software has fulfilled basic security needs.


