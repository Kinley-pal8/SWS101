# CAP 2: Bug Bounty Program

## Introduction

Imagine being an expert penetrator of numerous web-based applications, you have been contracted to offer service to RUB in that as a university, it has developed several web applications that ought to be examined for vulnerabilities before release on the internet. Since the last unit focuses on the common vulnerabilities found in web applications, the assignment is set up to ask you to analyze the websites located at 10. 3. 21. 141:8000, 10. 3. 21. 141:8008, 10. 3. 21. 141:8090, and www. hackthissite. In addition, there are other websites that are restricted only to the active users and learners within the GCBS college network. The goal that you have to achieve is to describe and analyze such Web applications and give a list of known Web application vulnerabilities, including the one that are listed in the hackers’ Top 10 most critical Web application security risks. In order to perform this task, you must ensure that every feature and component in the applications has been tested and tried to the maximum, leaving no room for find any security vulnerabilities. When you are through with your testing you will need to present a report outlining all the vulnerabilities you found and as importantly the process that you followed to find these bugs and the manner you carried out the testing that is following standard bug bounty report to enable the university to fix these problems before they release the applications to the public. 

## Instructions

Ensure that you are connected to the GCBS college's network, as the servers hosting the web applications are not accessible from the internet or public networks like Bmobile or TashiCell. The only website available on the internet is www.hackthissite.org.
The URLs of the web applications you need to test are:
- 10.3.21.141:8000
- 10.3.21.141:8008
- 10.3.21.141:8090
- www.hackthissite.org

Note: Each of the URLs listed above represents a different web application, and therefore, they may have different attack vectors and vulnerabilities.
If the IP address changes during the course of the assignment, the new IP address will be announced in the Google Space Chat, and this document will be updated accordingly.
Your task is similar to the web vulnerability practicals you completed in the SWS101 course on TryHackMe. You are expected to gain access to these servers and identify vulnerabilities by thoroughly testing the web applications.
Follow the OWASP Top 10 web application security risks as a guideline to identify common vulnerabilities, but do not limit your testing to these risks alone. Explore all parts and functionalities of the web applications to uncover any potential security flaws.
Once you have completed your testing, prepare a comprehensive bug bounty report detailing all the vulnerabilities you have discovered in each of the web applications. Follow industry-standard practices for bug bounty reporting to ensure that the information you provide is clear, concise, and actionable for the university to address the identified issues.

Remember, the goal of this assignment is to simulate a real-world bug bounty scenario, where you need to rigorously test the web applications and report any vulnerabilities before they are deployed on the internet, ensuring the security and integrity of the systems.

# Executive Summary



## Approach

### Methodology
The assessment followed a structured and thorough testing methodology, which included the following steps:

- Reconnaissance: Gathered information about the target websites, including technologies used, entry points, and potential attack surface areas.
- Mapping: Created a detailed map of the applications' functionality, user roles, and data flows to understand potential risks better.
- Automated Scanning: Utilized industry-standard tools like Burp Suite and OWASP ZAP to perform automated vulnerability scans, identifying potential issues for further investigation.
- Manual Testing: Conducted manual testing techniques, such as input fuzzing, parameter tampering, and business logic testing, to uncover vulnerabilities that may have been missed by automated scanners.
- Exploitation and Validation: Attempted to safely exploit identified vulnerabilities in a controlled environment, capturing evidence and analyzing the potential    impact.
- Reporting: Documented the findings, including vulnerability descriptions, severity ratings, and recommended remediation steps, in a comprehensive report.

The assessment was carried out by an experienced bug bounty hunter, following industry-standard practices and guidelines, including the OWASP Top 10 web application security risks.
 
### Scope 

The activity carried out is a simple internal penetration test of the server at IP 10. 3. 21. on College Network, we are simulating a malicious insider who has no credentials. The specific objectives included: 

 - Revealing open live servers addresses/ports that a target server is hosting. 
 - Deciding on the appropriate visages of the services that directly interact with customers. 
 - Exploitation of vulnerabilities by mapping and scanning operations 
 - To gaining access and raising privileges are some of the attempts. 
 - The attacker connected to many Wi-Fi connection points within the College Campus, and the exposure of the ports/service varied across the segments. 

In the rules of engagement, explicitly outlawed were any acts resulting in Denial-of-Service (DoS) or data destruction. Scans and attacks were narrowed to the specific server 10. 3. 21.


### Tools

1. Burp Suite:
- Comprehensive suite of tools for web application security testing
- Proxy to intercept and modify HTTP/HTTPS traffic
- Scanner to automatically scan for vulnerabilities
- Intruder for automated attacks and payload-based testing
- Other modules for decoding, collaboration, and manual testing

2. OWASP ZAP:
- Free and open-source web application security scanner
- Proxy for traffic interception and modification
- Automated vulnerability scanning
- Fuzzing for sending malformed data
- Active and passive scanning techniques
- Website crawling and mapping capabilities


## Conclusion and Remediation Summary

To address the vulnerabilities, the following measures should be taken to reduce the impact of Cross-Site
Scripting (XSS) attack: Ensure that input validation is properly implemented to minimize chances of SQL
injection attack. Moreover, the authorization mechanisms need to be audited and enhanced with regard
to the enforcement of the principle of least privilege and input validation with a view to avoiding some
Elevation of Privilege. To mitigate Cross-Site Request Forgery it is recommended to use anti-CSRF tokens
and to demand re-authentication for crucial actions. Also, the measures which help in overcoming Path
Traversal vulnerabilities include input validation, the limitation of changed value to an allowed set of
paths and never exposing sensitive files. Finally, updating software regularly, provisioning and availing
secure coding training to the developers, incorporating regular security audit, incorporating secure coding
standards in logging and monitoring services, and preparing an incident handling plan are essential for
holding a strong security posture. Addressing these vulnerabilities, using proper coding standards, best
practices and integration of security measures need to be done to improve the security posture of the
assessed systems.









