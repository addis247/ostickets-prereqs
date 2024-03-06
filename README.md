<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Enable internet information services (IIS)
- Install web platform installer
- Install MySQL and set up the username and password
- Install C++ redistributable
- Configure permissions and install OSticket 

<h2>Installation Steps</h2>
<p>
Begin by accessing portal.azure.com and establishing a resource group. Upon completion, proceed to create a Virtual Machine running Windows 10, configured with 4 virtual CPUs.
</p>
<p align="center">
<img src="https://i.imgur.com/IAQwOJX.png" height="60%" width="60%" />
</p>
<p align="center">
<img src="https://i.imgur.com/huiTMpp.png" height="60%" width="60%" />
</p>

<p>
Once the Virtual Machine setup is complete, utilize the public IP address to establish a remote desktop connection. Within the control menu, navigate to the "uninstall a program" option and select "turn windows features on and off".
<p>
Enable necessary features within Windows, specifically under World Wide Web Services and Internet Information Services (IIS), including CGI and Common HTTP Features.
<p>
<p>
  
</p>
<p align="center">
<img src="https://i.imgur.com/72GXbfW.png" height="40%" width="40%" />
</p>
<p>
Confirm the installation of IIS by accessing the web browser and searching for 127.0.0.1.
</p>
<p align="center">
<img src="https://i.imgur.com/0ej018Y.png" height="60%" width="60%" />
</p>
<p>
Install the PHP Manager for IIS and the Rewrite Module.
</p>
<p align="center">
<img src="https://i.imgur.com/wa9XJqG.png" height="60%" width="60%" />
</p>

</p>
<p align="center">
<img src="https://i.imgur.com/G8kT9O7.png" height="60%" width="60%" />
</p>
<p>Download and install PHP 7.3.8, extracting its contents into the designated directory (C:\PHP).
</p>
<p align="center">
<img src="https://i.imgur.com/emVJjwM.png" height="60%" width="60%" />
</p>
<p>
Install VC_redist.x86.exe.


</p>
<p align="center">
<img src="https://i.imgur.com/szePMjd.png" height="60%" width="60%" />
</p>
<p>
Download and install MySQL 5.5.62, opting for a Typical Setup and configuring a new root password when prompted by the Configuration Wizard.
</p>
<p align="center">
<img src="https://i.imgur.com/oBXmDrQ.png" height="60%" width="60%" />
</p>

</p>
<p align="center">
<img src="https://i.imgur.com/hlOM7ha.png" height="60%" width="60%" />
</p>
<p>Open IIS as an Administrator, register PHP within IIS, and specify the path for the PHP executable file.
</p>
<p align="center">
<img src="https://i.imgur.com/tV3F8Rr.png" height="60%" width="60%" />
</p>
</p>
<p align="center">
<img src="https://i.imgur.com/hgzzhRi.png" height="60%" width="60%" />
</p>
<p>
Reload IIS and proceed to install osTicket v1.15.8. Extract the 'upload' folder to c:\inetpub\wwwroot, renaming it to 'osTicket'.
</p>
<p align="center">
<img src="https://i.imgur.com/G1bFu8j.png" height="60%" width="60%" />
</p>
<p align="center">
<img src="https://i.imgur.com/ExlF4dE.png" height="60%" width="60%" />
</p>
<p>
Reload IIS once more, navigate to 'sites -> Default -> osTicket', and click 'Browse *.80' to access the osTicket installer page.
</p>
<p align="center">
<img src="https://i.imgur.com/ywcaFsZ.png" height="60%" width="60%" />
</p>
<p>
Enable necessary PHP extensions such as php_imap.dll, php_intl.dll, and php_opcache.dll within IIS.

Rename 'ost-sampleconfig.php' to 'ost-config.php' within the osTicket folder, adjust file permissions accordingly, and continue with the setup process in the browser.
</p>
<p align="center">
<img src="https://i.imgur.com/MPFC0rL.png" height="60%" width="60%" />
</p>
<p align="center">
<img src="https://i.imgur.com/Qsz2nIC.png" height="60%" width="60%" />
</p>

</p>
<p align="center">
<img src="https://i.imgur.com/r3xORfL.png" height="60%" width="60%" />
</p>
<p>
<p align="center">
<img src="https://i.imgur.com/4bMoDkS.png" height="40%" width="40%" />
</p>

<p align="center">
<img src="https://i.imgur.com/R1jXSso.png" height="60%" width="60%" />
</p>
<p>
Download and install HeidiSQL. Create a new database named 'osTicket' within HeidiSQL.
</p>
<p align="center">
<img src="https://i.imgur.com/R6Tk5an.png" height="60%" width="60%" />
</p>
<p>
Return to the browser for the osTicket page, complete the MySQL database information, and proceed with the installation process.
</p>
<p align="center">
<img src="https://i.imgur.com/T552pjD.png" height="60%" width="60%" />
</p>
Finalize the installation by providing the required MySQL Database, Username, and Password information, then click 'Install Now!'
  
<p>
Once the installation is complete, a confirmation page will be displayed.
</p>
<p align="center">
<img src="https://i.imgur.com/siezGtX.png" height="60%" width="60%" />
</p>
<p>
Conclude the process by deleting the setup folder, restoring file permissions in 'ost-config.php' to 'Read', and accessing the help desk login page at http://localhost/osTicket/scp/login.php. Confirm successful loading of the login page.
</p>
<p align="center">
<img src="https://i.imgur.com/swLbMQA.png" height="40%" width="40%" />
</p>
<p>
Thanks
</>
