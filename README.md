<h1>Configuring AAA for Device Access Control</h1>


<h2>Description</h2>
In this lab, I learned to configure AAA for device access control. The AAA (authentication, authorization, and accounting) feature allows you to verify the identity of, grant access to, and track the actions of users managing the router. The Cisco router supports RADIUS (Remote Access Dial-In User Service) or TACACS+ (Terminal Access Controller Access Control device Plus) protocols.
<br />



<h2>Environments Used </h2>

- <b>Ubuntu 20.04.2 LTS</b> 
- <b>PuTTY SSH Client</b>

<h2>Program walk-through:</h2>

<p align="center">
From the left sidebar click PuTTY SSH Client and proceed to put in the IP address, port number, click Telnet and then click open: <br/>
<img src="https://i.postimg.cc/65W26rkj/Screen-Shot-2022-08-26-at-5-26-10-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />
  
  
  
<br />
In the R3 terminal execute the following commands:   <br/>
1. en <br/>
2. conf t <br/>
3. hostname R3 <br/>
4. aaa new-model <br/>
5. tacacs-server host 192.168.1.3 <br/>
6. tacacs-server key cisco <br/>
7. username admin password ucertify <br/>
8. aaa authentication login CCIE group tacacs+ local <br/>
9. line vty 0 4 <br/>
10. login authentication CCIE <br/>
11. end <br/>
<img src="https://i.postimg.cc/Y0M6HhKJ/Screen-Shot-2022-08-26-at-5-45-02-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />
  
  
  
  
<br />
Open a new window from PuTTY SSH Client and enter in the IP address, port number, click Telnet and then click open  <br/>
<img src="https://i.postimg.cc/fRt01xSV/Screen-Shot-2022-08-26-at-5-46-33-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />




<br />
In the R4 terminal window execute the following commands  <br/>
1. en <br/>
2. telnet 192.168.1.1 <br/>
after this type in the username and password 
<img src="https://i.postimg.cc/L8tmqXry/Screen-Shot-2022-08-26-at-5-49-37-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />













  
  
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
