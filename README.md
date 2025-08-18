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


