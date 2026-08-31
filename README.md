# Week-3-Cybersecurity---Password-cracking
<h1>PENETRATION TESTING REPORT</h1>
<h3>PASSWORD CRACKING PHASE</h3>

|  Pentester Name 	    |  MICHELLE CHEMUTAI                                            	|
|---              	    |---	                                                            |
|  Program / Batch    	|   B082-Networkwalks                                           	|
|   Date          	    |  August 2026                                                  	|
|   Modules completed 	| W3 – Password Cracking (John the Ripper + Networkwalks Tools)  	|
|  Client / Target    	|   Authorized lab PDF (My Locked PDF1.pdf)	                      |
|   Permission secured?	| Yes (Educational lab)                                       	  |
|  Phases covered 	    |   Password Hash Extraction & Dictionary Attack                  |

<h2><u>1. Liability Disclaimer</u></h2>
I performed these activities only on the authorized lab files provided by Networkwalks. All materials are for education and research purposes only. Unauthorized password cracking is illegal.

<h2><u>2. Introduction</u></h2>
This report covers Week 3 practicals on password cracking. I used two different approaches to recover the password of a protected PDF file:

1. John the Ripper (via Johnny GUI)
2. Networkwalks Hash Calculator + Dictionary Attack Lab

Both methods successfully recovered the same password and captured the flag.

<h2><u>3. Tools Used</u></h2>

|   Tool                        	      |  Purpose                                	|
|---	                                  |---                                      	|
|  John the Ripper (Jumbo 1.9.0)      	| Open-source password cracker            	|
|   Johnny (GUI)	                      |   Graphical interface for John the Ripper	|
|   OnlineHashCrack	                    |   Extract PDF password hash             	|
|   Networkwalks Hash Calculator      	| Extract crackable PDF hash               	|
|   Networkwalks Password Cracker     	|  Dictionary attack against PDF hash     	|
|  Wordlist (JTR_default_password.txt) 	|  3556 common passwords                  	|

<h2><u>4. Activities Performed</u></h2>
Part 1: John the Ripper + Johnny

 1. Downloaded John the Ripper Jumbo from openwall.com
 2. Installed and configured Johnny GUI, pointing it to john.exe
 3. Uploaded the locked PDF to OnlineHashCrack and extracted the hash
 4. Loaded the hash into Johnny and started a dictionary attack
 5. Password successfully cracked: good-luck
 6. Opened the PDF with the recovered password
 7. Flag captured: nw{cybersecurity_flag_captured_2608}

    <u>Part 2: Networkwalks Tools</u>
 1. Uploaded the same locked PDF to Networkwalks Hash Calculator
 2. Extracted the identical $pdf$ hash
 3. Pasted the hash into the Networkwalks Password Cracker (Dictionary Attack Lab)
 4. Ran the attack using the built-in list, then uploaded JTR_default_password.txt (3556 words)
 5. Password successfully cracked: good-luck
 6. Opened the PDF and captured the same flag:
    nw{cybersecurity_flag_captured_2608}

<h2><u></u>5. Risk Analysis / Impact</h2>/u></h2>
|  # 	|  Finding                            |   Observation       	|  Potential Impact 	                    | Risk Level|
|---	|---	                                |---	                  |---                                     	|---      	|
|   1	|   Weak password used	              | simple dictionary word| Easily cracked with common wordlists  	| High    	|
|   2	|password protection can be bypassed	| attack succeeded  	  |  Sensitive documents revealed 	        | Medium  	|

<h2><u></u>6. Recommendations</h2>u></h2>

 1. Never use simple dictionary words or short passwords for important files.
 2. Use strong, unique passwords (minimum 12–16 characters with mixed case, numbers, and symbols).
 3. Prefer modern encryption methods and stronger PDF protection where possible.
 4. Consider using password managers to generate and store strong passwords.
 4. Regularly audit password strength in organizational documents.
 5. Educate users about the risks of weak passwords.

<h2><u>7. Conclusion</u></h2>
In Week 3 I successfully performed password cracking using two different methods:

John the Ripper (industry-standard tool via Johnny GUI)
Networkwalks own Hash Calculator + Dictionary Attack tool

Both approaches recovered the password good-luck from the protected PDF and allowed me to capture the flag nw{cybersecurity_flag_captured_2608}.
This practical clearly demonstrated how weak passwords can be quickly recovered using dictionary attacks, highlighting the importance of strong password policies.
