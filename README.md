<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system, osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Enable Internet Information Services (IIS) w/ CGI, then install PHP Manager, Rewrite Module, and extract PHP 7.3.8 to C:\PHP
- Install dependencies including the C++ Redistributable and MySQL 5.5.62, and Setup Login Credentials
- Set up osTicket in IIS by placing the "upload" folder in C:\inetpub\wwwroot, renaming it to "osTicket", enabling required PHP extensions, and configuring permissions
- Use a browser to complete the osTicket setup, create the database with HeidiSQL, and finalize installation with the provided MySQL credentials

<h2>Installation Steps</h2>

To setup osTicket, you first need to enable Internet Information Services (IIS) with the CGI feature, which allows PHP to work with IIS, using the "Turn Windows features on or off" utility. After enabling IIS, install PHP Manager for IIS and the URL Rewrite Module to manage PHP settings and URL routing. Finally, extract PHP 7.3.8 into the C:\PHP directory so that IIS can use it to process PHP scripts for osTicket.
</p>
<br />
<img width="1540" height="829" alt="osTck Project 1" src="https://github.com/user-attachments/assets/c8d7d6d5-c190-4e17-b458-116974c4eab8" />
</p>
<br />

To support PHP and MySQL functionality, install the  Microsoft Visual C++ distributable x86 as it’s required by PHP and MySQL to run properly. Download the MySQL Installer. During installation, you’ll be prompted to create login credentials. These credentials are essential for creating and connecting the osTicket database during the web-based setup.
</p>
<br />
<img width="726" height="442" alt="osTick Project 2" src="https://github.com/user-attachments/assets/5d0f28cf-d042-45f5-bebd-e9945a8df5aa" />
<p>
<br />

To set up osTicket in IIS, unzip your osTicket-v1.15.8.zip file and move the "upload" folder into C:\inetpub\wwwroot, then rename the folder to "osTicket". Open IIS, browse to the osTicket site, and use PHP Manager to enable required extensions like php_imap.dll, php_intl.dll, and php_opcache.dll. Finally, rename the configuration file to ost-config.php, adjust its permissions by disabling inheritance and granting Everyone full access so osTicket can complete the setup.
</p>
<br />
<img width="1712" height="861" alt="osTick Project 3" src="https://github.com/user-attachments/assets/60225f89-8128-4560-976e-fbef8afbc331" />
</p>
<br />
Open a web browser and go to http://localhost/osTicket to launch the osTicket setup page, where you’ll enter basic helpdesk details. Then, open HeidiSQL, connect using the MySQL login credentials, and create a new database called osTicket. Return to the browser to complete the installation by entering the database name and credentials, then click “Install Now” to finalize the setup.
</p>
<br />
<img width="1325" height="815" alt="osTick Project 4" src="https://github.com/user-attachments/assets/a3b12291-a017-4ede-a813-a5775b513c20" />

