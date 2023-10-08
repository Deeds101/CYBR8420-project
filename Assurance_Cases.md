## Part 1: Assurance Cases
### 1.1 Assurance Case 1: Login Credential Security
**Assurance Case:**   ITFlow sufficiently secures credentials from unauthorized use.

![image](https://github.com/Deeds101/CYBR8420-project/assets/87542247/0c083090-ce4a-4ea6-a55d-c0cb8d0b114b)


### 1.2 Assurance Case 2: Database Security
**Assurance Case:**  The ITFlow database meets security expectations. 

![image](https://github.com/Deeds101/CYBR8420-project/assets/87542247/69a22b1f-3f05-4537-a0b7-17b344b992c7)

### 1.3 Assurance Case 3: Multi-Factor Authentication
**Assurance Case:**

### 1.4 Assurance Case 4: Data Transmission Security
**Assurance Case:**   ITFlow has sufficient data transit security.

![image](https://github.com/Deeds101/CYBR8420-project/assets/143226996/0381581f-4a5e-4967-a238-d48ae2cd5a1e)
Reflection: My diagram went through many different shifts. Orginally, I had wanted to focus on just the billing functions within ITFlow. However, upon further review it appeared that my diagram would incorporate most of everyone's top-level claims as a sub-claim, so it felt as if my diagram did not impose a question of significant value which was not already being answered. From there, I created a version of the data transmission diagram which focused on each transmission vector as a rebuttal (mailing, web browsing, database transactions). I worked on this diagram for some time before realizing that my rebuttals resulted in the same evidence. I decided to condense my diagram further into what it is now. I realized along the way that I was not directly analyzing security functions for the software, rather, I was analyzing individual components and then trying to force security into them. I think addressing the main security functions that each component uses ended up being key to understanding the assignment. 

### 1.5 Assurance Case 5: Role-Based Access Control
**Assurance Case:**   ITFlow provides secure access to roles in the environment.

![image](https://github.com/Deeds101/CYBR8420-project/assets/87542247/3eb9fef9-806a-41b6-9bc7-5da46efa13d9)

### 1.6 Assurance Case 6: Workflow Automation and Documentation Security
**Assurance Case:**  ITFlow provides appropriate secure tracking of documentation and workflows.

![image](https://github.com/Deeds101/CYBR8420-project/assets/87542247/38c4c268-b823-4a82-a6fc-8c401c0f16de)

## Part 2: Evidence Alignment Observations
### 2.1 Assurance Case 1
#### *2.1.1 Available Evidence*
***E3 - Manual review of password related source code*** \
In the [password rotation documentation](https://github.com/itflow-org/itflow/blob/5b49d35f1a0241060c0f83ee696aa53df2f3c782/report_password_rotation.php#L4) it was validated that ITFlow will lock out user accounts where the passwords had not been changed within the last 90 days.  In addition, a report of these accounts is also made available to users with elevated access privileges for review/escalation purposes. As such, this control was considered to be sufficient to ensure passwords were being periodically changed to minimize the risk of brute force attacks.<br><br>
***E4 - Pentration test results*** \
***E5 - Review of logging configuration report*** \
Review of the [login configuration documentation](https://github.com/itflow-org/itflow/blob/5b49d35f1a0241060c0f83ee696aa53df2f3c782/login.php) determined that 
ITFlow only required the following for a user to successfully login:
- Users are required to login from a HTTPS address for enhanced security.
- Users are required to enter a valid MFA key.
- User must not have had multipe failed login attempts (e.g., >=15) from a single IP address.
- User must be attempting to login from an IP address associated with a previously successful login attempt.  If not, an email is to be sent to the users designated email address notifying them of the unusual login attempt. \
Based on consideration for these requirements and detection methods being used, it was determined that ITFlow sufficiently monitors user accounts for abnormalities in order to reduce the risk of unauthorized access attempts.<br><br>
#### *2.1.2 Insufficient Evidence*
***E1 - Manual review of source code*** \
In the [log settings documentation](https://github.com/itflow-org/itflow/blob/cd006d0625d638880fe3d6e1c4210eb14e504dbd/logs.php#L17) ITFlow logs IP addresses associated with each login attempt.  This information is retained within an Audit Log document within the database.  This information is then reviewed in future login attempts as part of the [login settings documentation](https://github.com/itflow-org/itflow/blob/cd006d0625d638880fe3d6e1c4210eb14e504dbd/login.php#L3) where if fifteen or more failed login attempts are identified, then the corresponding IP address is automatically locked out by the system.  Based on this information and the results of the manual review of the source code, it was believed that while this control will likely block some brute force attacks, it could easily be bypassed by periodically changing IP addresses.  Further, if a threat actor just wanted to lockout the system, they could identify the IP information being using by the organization leveraging the system and repeatedly block access to the organization via a bot.  As such, this control was not considered sufficient.<br><br>
***E2 - ITFlow Password Policy*** \
This evidence is unavailable, an we believe it needs to be completed for ITFlow to ensure more complex passwords are being leveraged by users to reduce the risk of successful brute force attacks.<br><br>

## Project Board Link: [Assurance Case Project Board](https://github.com/users/Deeds101/projects/4/views/1)

## Teamwork Reflection


