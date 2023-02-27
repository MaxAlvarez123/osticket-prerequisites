<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- [Have PHP Manager Installed](https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view)
- [Have Rewrite Module Installed](https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view)
- [Have PHP 7.3.8 installed and unzip into a folder name PHP](https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view)
- [Have C++ x86 installed](https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view)
- [Have MySQL 5.562 installed](https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view)

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/VOM0Zm4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 1

- In order for PHP Manager to be installed you'll first have to enable CGI within ISS. 
This feature allows your computer to serve a website which is what osTicket runs on.

- To test out and see if you enable CGI correctly you can use the following IP Address 127.0.0.1 and if it shows the defualt ISS website
its turned on correctly. 

- How to find CGI: Control panel -> Programs -> Turn Window Features on or off -> Internet Information Services -> World Wide Web 
-> Application Development Features -> CGI.
</p>
<br />

<p>
<img src="https://i.imgur.com/kiiTmfE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/lAXcTOq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/qVJ1fNy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/CZeJ1Ar.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step2

After having downlaoded all of the necessary application in the "List of Prerequisites" you will now register PHP within IIS.

This is done by opening IIS as a administrator.

Opening PHP manager and then selecting the PHP folder which has all of the unzipped contents from before.

</p>

<br />

<p>
<img src="https://i.imgur.com/oTUNaOI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 3

- Next you'll will use the following link to dowload [osTicket.](https://drive.google.com/file/d/1VeVXKlzHDRjeaVUL99ptq7qYbrbXdFxJ/view)

- You will then unzip the folder into c:\inetpub\wwwroot.

- Next, withing c:\inetpub\wwwroot you will rename the "upload" file name to "osTicket". 


</p>
<br />

<br />

<p>
<img src="https://i.imgur.com/NLqZttp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 4

- Within IIS Go to Sites -> Default -> osTicket and on the right click on "Browse *:80”

- It will take you to the osTicket intallation page and there are still some red X's beside some extenstions which means we
need to enable them in order for us to use all of the features.
</p>
<br />

<br />

<p>
<img src="https://i.imgur.com/ZrwebpA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/fcbqJum.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 5

- Back to IIS go to sites -> Default -> osTicket.

- Double click on PHP Manager.

- Click "Enable or Disable an extenstion" and enable the following extension.
    - php_imapdll
    
    - php_intl.dll
    
    - php_opcache.dll
    
- Once enabled go back to the osTicket installation page, refresh the site and see the changes. 

</p>
<br />

<br />

<p>
<img src="https://i.imgur.com/PcTNeZu.pngv" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/qJUNLOj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/zSACpTO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 6

- Next we will rename the ost-sampleconfig.php file to ost-config.php which can be found from C:\inetpub\wwwroot\osTicket\include\ost-config.php

- Next within ost-config.php we will assign new permissions within this file.
    
    - Disable Inheritance -> Remove All
    
    - New Permission -> Everyone -> All
 
- Finally, go back to the osTicket installation page and hit continue and set up osTicket the way you want it. 
</p>
<br />
