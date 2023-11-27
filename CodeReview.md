
# Code review
	We chose to do an automated review because none of 
	our group members are exceptionally good at coding and/or 
	identifying vulnerabilities in raw code. Before even beginning, 
	our team knew this would be a challenge. Thus, automated review to address this challenge.
	The code review software we used is called Synk. It integrates well with GitHub and
	is easy to use and import multiple open-source projects.
	In addition, it is exceptionally good at analysis.
	Not only does it identify potential vulnerabilities, but it also
	performs a fix analysis based on the discovery and resolution of
	other open source projects it has scanned on Git Hub.

### File Analysis: post/*location.php*

The file has a potential SQL injection vulnerabiilty.
Lines 28-47 is a check to see if a file is attached for uploading directly into
the query *mysqli_query.* This could give bad actors direct access to the database.

**[CWE-89](https://cwe.mitre.org/data/definitions/89.html)** \
**[CWE-23](https://cwe.mitre.org/data/definitions/23.html)**

### File Analysis: plugins/PHPMailer/src/*POP3.php*

The file has a potential privacy leak.
Password data flows directly into an echo statement at line 396. 
Transit (API) and sotrage(server) should both be encrypted.

**[CWE-532](https://cwe.mitre.org/data/definitions/532.html)**

### File Analysis: Functions.php*

The file is missing the HttpOnly and Secure attributes for setcookie (set to false by default) in two separate places – lines 319 and 321.
This flag should be set to true to protect the created cookie from any possible malicious code creation/usage, or possible Man-in-the-Middle attacks from the client side.

**[CWE-1004](https://cwe.mitre.org/data/definitions/1004.html)** \
**[CWE-614](https://cwe.mitre.org/data/definitions/614.html)**

### File Analysis: portal/login_reset.php*

This file has potential SQL Injection and Cross-Site Scripting vulnerabilities. The SQL Injection vulnerability is caused by a failure to sanitize input from HTTP parameter flows into a mysqli query in lines 56, 67, 91, 115, 126, 149-150, and 208.
The Cross-Site Scripting vulnerability is also caused by the failure to sanitize input from HTTP parameter flows into an echo statement where it is used to render an HTML page which is then returned to the user in lines 223-224.

**[CWE-89](https://cwe.mitre.org/data/definitions/89.html)** \
**[CWE-79](https://cwe.mitre.org/data/definitions/79.html)**
