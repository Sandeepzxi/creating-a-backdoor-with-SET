# creating-a-backdoor-with-SET
creating a backdoor with SET - Ethical Hacking Techniques course

# AIM:
To Create a backdoor with Social Engineering Toolkit (SET)

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode


### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

### Architecture Diagram

```
+----------------+        +------------------------+        +----------------------+
| Attacker's PC  | -----> | SET (Credential        | -----> | Fake Login Page      |
| (Kali Linux)   |        | Harvester via Apache)  |        | (Hosted by SET)      |
+----------------+        +------------------------+        +----------------------+
       |                                                             |
       |                                                             v
       |   1. Configure SET with phishing site (e.g., Gmail clone)   |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Victim's Browser     |
       | <------------------------------------------------| Clicks Phishing Link|
       |                                                 +----------------------+
       |                                                             |
       |                                                             v
       |     2. Victim Enters Credentials → Sent to SET/Attacker    |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Credentials Captured |
       |                                                 | in Apache log/SET DB |
       |                                                 +----------------------+

```

## EXECUTION STEPS AND ITS OUTPUT:
Social Engineering attacks are the various cons used by the hackers to trick people into providing sensitive data to the attackers.

**Steps to Use SET for Phishing (Credential Harvester Attack Method)**

**1. Open terminal:**
```bash
sudo setoolkit
```
<img width="686" height="762" alt="image" src="https://github.com/user-attachments/assets/3e4eea63-d5e4-48d4-8153-0c67d3de70f0" />

**2. Navigate:**
```bash
1) Social-Engineering Attacks  
2) Website Attack Vectors  
3) Credential Harvester Attack Method  
```
<img width="756" height="652" alt="image" src="https://github.com/user-attachments/assets/7f60f4c4-453f-4f44-a2c3-e10288b3cc6e" />

<img width="1781" height="473" alt="image" src="https://github.com/user-attachments/assets/ac2fb3ed-459f-4682-b71e-0544835e86d9" />
<img width="621" height="299" alt="image" src="https://github.com/user-attachments/assets/9612d778-d139-4577-9167-3f68b84c8b70" />



**3. Enter your IP address as the attacker server.**
**4. Choose:**
```bash
2) Site Cloner
```
<img width="767" height="355" alt="image" src="https://github.com/user-attachments/assets/4c0f11cc-13da-46af-9fe2-932f26475ce8" />

**5. Enter the URL of the legitimate site ```(e.g., https://accounts.google.com)```**
<img width="1014" height="334" alt="image" src="https://github.com/user-attachments/assets/c1de7cc4-7b43-4062-9e5b-2aefd90a0a62" />


**6. Send the generated link to the victim.**
<img width="793" height="223" alt="image" src="https://github.com/user-attachments/assets/424dbdd3-cb72-4473-ae44-193d7980802a" />


**7. Once the victim logs in → their credentials are stored in:**
```bash
/var/www/html/
```
<img width="1229" height="606" alt="image" src="https://github.com/user-attachments/assets/dc5103db-2e9a-40a3-9238-7a47f99ae84e" />



## RESULT:
The Social Engineering Toolkit (SET) is used to create backdoor is  examined successfully
