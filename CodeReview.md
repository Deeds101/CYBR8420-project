
# Code review
	We chose to do an automated review because none of 
	are group members are exceptionally good at coding and/or 
	identifying vulnerabilities in raw code. Before even begining, 
	our team knew this would be a challenge. Thus, auotmated review to address this challenge.
	The code review software we used is called Synk. It integrates well with GitHub and
	is easy to use and import multiple open source projects.
	In additionj it is exceptionally good at analysis.
	Not only does it identify potential vulnerabilites, it
	performs a fix analysis based on the discoverya and resolution of
	other open source projects it has scanned on github.

### File Analysis: post/*location.php*

The file has a potential SQL injection vulnerabiilty.
Lines 28-47 is a check to see if a file is attached for uploading directly into
the query *mysqli_query.* This could give bad actors direct access to the database.

**[CWE-89](https://cwe.mitre.org/data/definitions/89.html)**
**[CEW-23](https://cwe.mitre.org/data/definitions/23.html)**

### File Analysis: plugins/PHPMailer/src/*POP3.php*

The file has a potential privacy leak.
Password data flows directly into an echo statement at line 396. 
Transit (API) and sotrage(server) should both be encrypted.

**[CWE-532](https://cwe.mitre.org/data/definitions/532.html)**
