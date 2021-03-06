## Week 16 Homework Submission File: Penetration Testing 1

#### Step 1: Google Dorking


- Using Google, can you identify who the Chief Executive Officer of Altoro Mutual is:
  - ["Karl Fitzgerald, Chairman and Chief Executive Officer"](http://demo.testfire.net/index.jsp?content=pr/20060720.htm)

- How can this information be helpful to an attacker:
  - This information can be useful when doing reconassaince and to determine a deeper search on a high-seated person of a company and might link somethings that are related to the company to levarage attacks and other information.


#### Step 2: DNS and Domain Discovery

Enter the IP address for `demo.testfire.net` into Domain Dossier and answer the following questions based on the results:

  1. Where is the company located:
    - 9725 Datapoint Drive, Suite 100, San Antonio, TX 78229 US

  2. What is the NetRange IP address:
    - 65.61.137.64 - 65.61.137.127

  3. What is the company they use to store their infrastructure:
    - Rackspace Backbone Engineering

  4. What is the IP address of the DNS server:
    - 65.61.137.117

#### Step 3: Shodan

- What open ports and running services did Shodan find:
  - 80 (http): Apache Tomcat/Coyote JSP Engine 1.1
  - 443 (https): Apache Tomcat/Coyote JSP engine1.1 

#### Step 4: Recon-ng

Is Altoro Mutual vulnerable to XSS:
  - Yes
  ![AltoroMutualXSSED](images/AltoroMutualXSSED.png)

### Step 5: Zenmap

Your client has asked that you help identify any vulnerabilities with their file-sharing server. Using the Metasploitable machine to act as your client's server, complete the following:

- using ```nmap -sV -sC -oN /root/Desktop/nmapscan.txt 192.168.0.10``` to run nmap against the Metasploit VM outputs the vulnerabilities [nmapscan.txt](images/nmapscan.txt)

- Once you have identified this vulnerability, answer the following questions for your client:
  1. What is the vulnerability:
    - ftp-anon
  2. Why is it dangerous:
    - This vulnerability creates an access to the machine that bypasses the login password.
  3. What mitigation strategies can you recommendations for the client to protect their server:
    - Disable anonymous log access with the FTP server.