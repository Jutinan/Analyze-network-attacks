# Analyze-network-attacks
## Activity Overview
In this activity, you will consider a scenario involving a customer of the company that you work for who experiences a security issue when accessing the company’s website. You will  identify the likely cause of the service interruption. Then, you will explain how the attack occurred and the negative impact it had on the website. 

In this course, you have learned about several common network attacks. You have learned their names, how they are carried out, and the characteristics of each attack from the perspective of the target. Understanding how attacks impact a network will help you troubleshoot issues on your organization’s network. It will also help you take steps to mitigate damage and protect a network from future attacks.

Be sure to complete this activity before moving on. The next course item will provide you with a completed exemplar to compare to your own work. 
## Scenario
Review the following scenario. Then complete the step-by-step instructions.

You work as a security analyst for a travel agency that advertises sales and promotions on the company’s website. The employees of the company regularly access the company’s sales webpage to search for vacation packages their customers might like. 

One afternoon, you receive an automated alert from your monitoring system indicating a problem with the web server. You attempt to visit the company’s website, but you receive a connection timeout error message in your browser.

You use a packet sniffer to capture data packets in transit to and from the web server. You notice a large number of TCP SYN requests coming from an unfamiliar IP address. The web server appears to be overwhelmed by the volume of incoming traffic and is losing its ability to respond to the abnormally large number of SYN requests. You suspect the server is under attack by a malicious actor. 

You take the server offline temporarily so that the machine can recover and return to a normal operating status. You also configure the company’s firewall to block the IP address that was sending the abnormal number of SYN requests. You know that your IP blocking solution won’t last long, as an attacker can spoof other IP addresses to get around this block. You need to alert your manager about this problem quickly and discuss the next steps to stop this attacker and prevent this problem from happening again. You will need to be prepared to tell your boss about the type of attack you discovered and how it was affecting the web server and employees.

# Activity: Wireshark TCP/HTTP log [https://docs.google.com/spreadsheets/d/1v8V2NO8yh6kCqNUuKsQOh7zRTGta_B2_pmCDzDeyDlE/edit?usp=sharing]

# Cybersecurity Incident Report
## Section 1: Identify the type of attack that may have caused this network interruption: 
From the table of Wireshark TCP/HTTP, the `203.0.113.0` is the only attacker IP address that using SYN flood attack, which is one of DoS attack to the company IP address `192.0.2.1` caused the web server stops respoding and website's connection timeout error message.

## Section 2: Explain how the attack is causing the website to malfunction:
The attacker simulates a TCP connection and flood a server with SYN packets and overwhelms the server connection that using three-way handshake. This attack called SYN flood attack which is one of DoS (Denial of Service) attacks.
The log indicate that the web server has become overwhelmed and is unable to process the visitors' SYN requests. The server is unable to open a new connection to new visitors who receive a connection timeout message. 
