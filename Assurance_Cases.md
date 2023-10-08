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

![image](https://github.com/Deeds101/CYBR8420-project/assets/87542247/c4751163-68ce-4451-b5c2-257ee3465453)

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
***E4 - Pentration test results*** \
#### *2.1.2 Insufficient Evidence*
***E1 - Manual review of source code*** \
In the [log settings documentation](https://github.com/itflow-org/itflow/blob/cd006d0625d638880fe3d6e1c4210eb14e504dbd/logs.php#L17), ITFlow logs IP addresses associated with each login attempt.  This information is retained within an Audit Log document within the database.  This information is then reviewed in future login attempts as part of the [login settings documentation](https://github.com/itflow-org/itflow/blob/cd006d0625d638880fe3d6e1c4210eb14e504dbd/login.php#L3) where if fifteen or more failed login attempts are identified, then the corresponding IP address is automatically locked out by the system.  Based on this information and the results of the manual review of the source code, it was believed that while this control will likely block some brute force attacks, it could easily be bypassed by periodically changing IP addresses.  Further, if a threat actor just wanted to lockout the system, they could identify the IP information being using by the organization leveraging the system and repeatedly block access to the organization via a bot.  As such, this control was not considered sufficient.<br><br>
***E2 - ITFlow Password Policy*** \
***E5 - Review of logging configuration report*** \

## Project Board Link: [Assurance Case Project Board](https://github.com/users/Deeds101/projects/4/views/1)

## Teamwork Reflection


