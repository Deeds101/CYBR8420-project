## Part 1: Assurance Cases
### 1.1 Assurance Case 1: Login Credential Security
**Assurance Case:**   ITFlow sufficiently secures credentials from unauthorized use.

![image](https://github.com/Deeds101/CYBR8420-project/assets/87542247/2e814cbc-baf8-405f-b38b-2b719ed1c3ef)


### 1.2 Assurance Case 2: Database Security
**Assurance Case:**  The ITFlow database meets security expectations. 

![Draft1Assurance Claim Diagram](https://github.com/Deeds101/CYBR8420-project/assets/107895832/360918f7-5919-4917-8480-41f63288f59b)


### 1.3 Assurance Case 3: Multi-Factor Authentication
**Assurance Case:** IT Flow effectively utilizes MFA security requirements.
![image](https://github.com/Deeds101/CYBR8420-project/blob/main/AssuranceClaimDiagrams/MFA%20Assurance%20Case.PNG)


### 1.4 Assurance Case 4: Data Transmission Security
**Assurance Case:**   ITFlow has sufficient data transit security.

![image](https://github.com/Deeds101/CYBR8420-project/assets/143226996/fea03910-406c-4515-a947-8dd00f883b80)


### 1.5 Assurance Case 5: Role-Based Access Control
**Assurance Case:**   ITFlow provides secure access to roles in the environment.

![image](https://github.com/Deeds101/CYBR8420-project/blob/main/AssuranceClaimDiagrams/RBAC%20Assurance%20Claim.png)


### 1.6 Assurance Case 6: Workflow Automation and Documentation Security
**Assurance Case:**  ITFlow provides appropriate secure tracking of documentation and workflows.

![image](https://github.com/Deeds101/CYBR8420-project/assets/87542247/e6707633-dfd3-47cd-b66e-264c3eee36d5)






## Part 2: Evidence Alignment Observations
### 2.1 Assurance Case 1: Login Credential Security
#### *2.1.1 Available Evidence*
***E4 - Manual review of password-related source code*** \
In the [password rotation documentation](https://github.com/itflow-org/itflow/blob/5b49d35f1a0241060c0f83ee696aa53df2f3c782/report_password_rotation.php#L4) it was validated that ITFlow will lock out user accounts where the passwords had not been changed within the last 90 days. In addition, a report of these accounts is also made available to users with elevated access privileges for review/escalation purposes. As such, this control was considered to be sufficient to ensure passwords were being periodically changed to minimize the risk of brute force attacks.<br><br>
***E6 - ITFlow Code Base (HTML Purifier)*** \
Review of the ITFlow Code base determined the [HTML Purifier plugin]( itflow/README.md at 537f18efd263a2ad5bf2518100288e8f336ff57e · itflow-org/itflow (github.com)) is used to scrub login input for potential buffer overflow attempts. Review of the setup of this [plugin](http://htmlpurifier.org) determined that ITFlow was sufficiently minimizing the risk of a successful stack overflow attack.<br><br>
***E7 - Review of logging configuration report*** \
Review of the [login configuration documentation](https://github.com/itflow-org/itflow/blob/5b49d35f1a0241060c0f83ee696aa53df2f3c782/login.php) determined that 
ITFlow only required the following for a user to successfully log in:
- Users are required to log in from a HTTPS address for enhanced security.
- Users are required to enter a valid MFA key.
- User must not have had multiple failed login attempts (e.g., >=15) from a single IP address.
- User must be attempting to log in from an IP address associated with a previously successful login attempt.  If not, an email is to be sent to the user's designated email address notifying them of the unusual login attempt.

Based on consideration of these requirements and detection methods being used, it was determined that ITFlow sufficiently monitors user accounts for abnormalities in order to reduce the risk of unauthorized access attempts<br><br>
#### *2.1.2 Insufficient Evidence*
***E2 - Manual review of source code*** \
In the [log settings documentation](https://github.com/itflow-org/itflow/blob/cd006d0625d638880fe3d6e1c4210eb14e504dbd/logs.php#L17) ITFlow logs IP addresses associated with each login attempt. This information is retained within an Audit Log document within the database. This information is then reviewed in future login attempts as part of the [login settings documentation](https://github.com/itflow-org/itflow/blob/cd006d0625d638880fe3d6e1c4210eb14e504dbd/login.php#L3) where if fifteen or more failed login attempts are identified, then the corresponding IP address is automatically locked out by the system. Based on this information and the results of the manual review of the source code, it was believed that while this control would likely block some brute-force attacks, it could easily be bypassed by periodically changing IP addresses. Further, if a threat actor just wanted to lock out the system, they could identify the IP information being used by the organization leveraging the system and repeatedly block access to the organization via a bot. As such, this control was not considered sufficient.
<br><br>
***E3 - ITFlow Password Policy*** \
This evidence is unavailable, and we believe it needs to be completed for ITFlow to ensure more complex passwords are being leveraged by users to reduce the risk of successful brute-force attacks.
<br><br>

### 2.2 Assurance Case 2: Database Security
#### *2.2.1 Available Evidence*
***E1 - Software is kept up to date*** \
IT Flow has built database updates and version logs into the documentation. A mechanism to maintain current versions exists. Maintaining the updates will be up to the user, but IT Flow facilitates an easy way for the user to do this.

***E3 - Documentation indicates IT Flow uses HTML Purifier*** \
In researching the code for IT FLow, it was found the software uses HTML Purifier, a PHP plugin, to sanitize HTML input. HTML Purifier allows developers to create whitelists, or more complex policies as needed. HTML Purifier is quite extensive, it looks to protect against inserting malicious schemas into an SQL database as well.

***E5 - Assurance Case on Login Credential Security*** \
User access to the database is password-protected. The security of passwords and accounts is extensively detailed in the login Credential Assurance Case.

#### *2.2.2 Insufficent Evidence*

***E2 - User input is escaped*** \
While the software uses HTML purifier to sanitize html input, no indication was found that the software escapes all input to normalize text. Normalizing text helps prevent malicious SQL queries from being executed as code.

***E4 - IT Flow follows AES as a standard*** \
IT FLow most likely uses some kind of encryption to protect the database, and other functions, no evidence was found that points to a specific type of encryption. It would be recommended to follow the AES modern encryption standards.
<br><br>

### 2.3 Assurance Case 3: Multi-Factor Authentication
#### *2.3.1 Available Evidence*
***E1 - Login Information Assurance Case Diagram*** \
The encryption for login and MFA is further described in the assurance diagram. Within that diagram, it goes into detail on the encryption that ITFlow implements for its login system and credentials.

***E3 - Review of ITFlow forum update*** \
Initially, ITFlow did not have a function or option available to force MFA for Admin users or any users at login. There was an option to opt into it which left exploitable vulnerabilities if a simple password was hashed or cracked. After reviewing a forum update further on the need to force the implementation, developers did end up saying that they were going to change that option to become available and progress on the workings of enforcing MFA for Admin accounts. [Force MFA Request](https://forum.itflow.org/d/304-feature-request-force-mfa)

***E4 - ITFlow MFA code implementation update*** \
After another forum update, the ITFlow Admins updated their code to move in the right direction when it comes to forcing MFA and requiring it to be set up and not bypassed whatsoever.
- [commit 1](https://github.com/itflow-org/itflow/commit/2a142f1c426ce1ee9016dee21b1d61fcf1aa33e1)
- [commit 2](https://github.com/itflow-org/itflow/commit/17c8a9ab0ccbb5f03fbb550b6b01251769a84197)
- [commit 3](https://github.com/itflow-org/itflow/commit/747b7de143b0f9addba620072af4bcd90a5f8089)

#### *2.3.2 Insufficient Evidence*
***E2 - ITFlow MFA Policy*** \ 
While there were multiple minor mentions and thoughts from the developers regarding the implementation of a strict policy for a specific list of requirements MFA must meet in order to decrease risk factors, there was never a set-in-stone policy put in place. 
<br><br>

### 2.4 Assurance Case 4: Data Transmission Security
#### *2.2.1 Available Evidence*
***E1 - ITFlow send function code review*** \
As far as I can tell, ITFlow uses the "PHPMailer" library to send emails which uses opportunistic TLS to encrypt data. This could leave the application vulnerable if an attacker is in the network already. This would be sufficiently secure for most environments with mitigating controls. 

***E2 - Manual encryption function code review*** \
Encryption is done through various means. Mailing uses "PHPMailer SMTPSecure" for TLS encryption. Mail encryption supports SSL and TLS, leaving the choice of security to the user (I'd love to see SSL deprecated and only support TLS 1.2 or higher). Other forms of encryption utilize standard HTTPS encryption protocols including OpenSSL. Login information is enforced via HTTPS.  

***E3 - Login Information Assurance Case Diagram*** \
Reference diagram contained in this document. 

***E4 - ITFlow Key generation function*** \
The key generation function in https://github.com/itflow-org/itflow/blob/master/api_key_add_modal.php calls "randomString(156)" in line 2. This has sufficient complexity (156 characters sanitized for HTML).

***E5 - Database Assurance Case Diagram*** \
Reference diagram contained in this document. 

***E6 - ITFlow audit log*** \
ITFlow documents sensitive security events through robust audit log entries in its code. This is peppered throughout various security functions. 

***E7 - ITFlow code changelog*** \
https://github.com/itflow-org/itflow/commits/master

***E8 - Manual code review of randomization function*** \
Randomization uses a documented PHP function called "random_bytes" (https://www.php.net/manual/en/function.random-bytes.php) to generate a randomized string. The "randomString" function then trims the string to create URL safe keys. This function is sufficiently secure. 

***E9 - Manual PKI code review*** \
Overview of PKI implementation appears to follow X.509 standards.

#### *2.2.2 Insufficent Evidence*

***None found***
<br><br>


### 2.5 Assurance Case 5: Role-Based Access Control

***E1 - Database Assurance Case*** \
See 1.2/2.2 Assurance Case 2


***E2: Roles set by Admins*** \
In the ITFlow demo site, you can create user accounts if you are logged in as an administrator. 

***E3 - Manual testing in the demo environment*** \
I went into the demo site to test for IDOR and SSRF vulnerabilities and could not escalate my privileges on that site. I started by creating a new client logging into the client page and inspecting the element on a browser to see if there were any vulnerabilities in the webpage that I could exploit. Then I put the webpage in a burpsuite environment to see if I could see anything while crawling the page. I was not able to find anything. 


***E4 - Resolved by devs*** \
This issue was resolved by the devs of ITFlow. 

You can see the issue here: https://github.com/itflow-org/itflow/issues/673

***E5 - MFA Assurance Case*** \
See 1.3/2.3 Assurance Case 3

***E6 - ITFlow Codebase*** \
According to the ITFlow codebase in GitHub, input is sanitized every time a new request for a login comes through or the website is refreshed. 
<br><br>

### 2.6 Assurance Case 6: Workflow Automation and Documentation Security
***E1 - Assurance Case on MFA*** \
ITFlow does not enforce MFA by default on *user* accounts but allows it to be used to help secure login functions. ITFlow is implementing a force for MFA on any Admin account. For further information on ITFlow's use of MFA, see 1.3/2.3 Assurance Case 3.

***E2 - Assurance Case on Login Credential Security*** \
See 1.1/2.1 Assurance Case 1

***E3 - Assurance Case on MFA*** \
See 1.3/2.3 Assurance Case 3

***E4 - Assurance Case on Login Credential Security*** \
See 1.1/2.1 Assurance Case 1

<br><br>


## Project Board Link: [Assurance Case Project Board](https://github.com/users/Deeds101/projects/4/views/1)

## Teamwork Reflection

For this week's assignment, our team worked well together. We were able to have regularly scheduled meetings as well as add other meetings to accommodate the time necessary to plan out what was needed. One thing we did add this week to allow for more time for review of the diagrams of others was to ask that all diagrams be loaded into GitHub by Friday. This gave all team members the time to review and add comments where necessary and gave time for those with comments on their diagrams to change those diagrams to better align with the evidence and comments given. 

The team did have some challenges defining the appropriate top-level claims that were applicable related to ITFlow. These challenges were largely addressed through additional meetings with team members to discuss and ensure alignment on what these top-level claims are and how they should be worded.


