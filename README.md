<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
In this project we will cover the prerequisites and step-by-step installation of osTicket, an open-source help desk ticketing system used for managing and tracking customer support requests.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 11</b> (24H2)

<h2>Steps Included</h2>

- STEP 1 - Enable Internet Information Services (IIS) w/ CGI, then install PHP Manager, Rewrite Module, and extract PHP 7.3.8 to C:\PHP.
- STEP 2 - Install dependencies including the C++ Redistributable and MySQL 5.5.62, and Setup Login Credentials.
- STEP 3 - Set up osTicket in IIS by placing the "upload" folder in C:\inetpub\wwwroot, renaming it to "osTicket", enabling required PHP extensions, and configuring permissions.
- STEP 4 - Use a browser to complete the osTicket setup, create the database with HeidiSQL, and finalize installation with the provided MySQL credentials.

<h2>Installation Steps</h2>

To setup osTicket, we first need to enable Internet Information Services (IIS) with the CGI feature, which allows PHP to work with IIS, using the "Turn Windows features on or off" utility. After enabling IIS, install PHP Manager for IIS and the URL Rewrite Module to manage PHP settings and URL routing. Next extract PHP 7.3.8 into the C:\PHP directory so that IIS can use it to process PHP scripts for osTicket.
</p>
<img width="1540" height="829" alt="osTck Project 1" src="https://github.com/user-attachments/assets/c8d7d6d5-c190-4e17-b458-116974c4eab8" />
</p>
<br />

To support PHP and MySQL functionality, we must install the Microsoft Visual C++ distributable x86 as it’s required by PHP and MySQL to run properly. Download the MySQL Installer. During installation, there will be a prompt directing us to create login credentials. These credentials are essential for creating and connecting the osTicket database during the web-based setup.
</p>
<img width="726" height="442" alt="osTick Project 2" src="https://github.com/user-attachments/assets/5d0f28cf-d042-45f5-bebd-e9945a8df5aa" />
<p>
<br />

To set up osTicket in IIS, we unzip the osTicket-v1.15.8.zip file and move the "upload" folder into C:\inetpub\wwwroot, then rename the folder to "osTicket". Next up open IIS, browse to the osTicket site, and use PHP Manager to enable required extensions like php_imap.dll, php_intl.dll, and php_opcache.dll. Finally, rename the configuration file to ost-config.php, adjust its permissions by disabling inheritance and granting Everyone full access so osTicket can complete the setup.
</p>
<img width="1712" height="861" alt="osTick Project 3" src="https://github.com/user-attachments/assets/60225f89-8128-4560-976e-fbef8afbc331" />
</p>
<br />
Open a web browser and go to http://localhost/osTicket to launch the osTicket setup page. There we will enter basic HelpDesk details. Now we will open HeidiSQL, connect using the MySQL login credentials, & create a new database called osTicket. Return to the browser to complete the installation by entering the database name and credentials, then click “Install Now” to finalize the setup.
</p>
<img width="1325" height="815" alt="osTick Project 4" src="https://github.com/user-attachments/assets/a3b12291-a017-4ede-a813-a5775b513c20" />
</p>
</p>
<h2>Final Thoughts</h2>
This project provided me practical experience in deploying and configuring an open-source ticketing system while strengthening my skills in server administration and web application setup. It also highlighted the importance of scalable support solutions in managing real-world IT service requests.
