# osTicket-Installation-2
<h2>Installation of Prerequisites and osTicket</h2>

Go to portal.azure.com and click on Home \> Locate vm-osTicketC \> note Public IP 40.84.7.95 and Private IP 10.0.0.4
![osTicket C 1](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/e64ba1d6-df5c-4363-8c89-43cc765d14c0)

At **Windows Start Menu** Search bar enter **Remote Desktop Connection** and sign in with Public IP 40.84.7.95
![osTicket C 2](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/63d1b835-2566-407e-9d41-3c7c653e3bcc)
![osTicket C 3](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/b8aea56e-720d-4c47-8fed-1216e2764242)

In the VM choose **NO** for all **Privacy Settings for your device** and click **Accept****\>Continue\> **** Start without your data ****.**
**This is a lab VM \*\*No need to bring over data as if you are setting up the device for everyday use \>** Click Finish.
Copy and then paste the Installation Files into the VM URL so that download and install them.
![osTicket C 4](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/c4380ff0-4732-4979-a0bd-2e09e4be9f51)

| Php-7.3.8-nts-Win32-VC15-x86 | HeidiSQL\_12.3.0.6589 | mysql-5.5.62-win32.msi | osTicket-v1.15.8.zip |
| --- | --- | --- | --- |
| PHPManagerForIIS.V1.5.0.msi | Rewrite\_amd64\_en\_US.smi | VC\_redist.x86.ext |
 |

Ideally, you want to have both screens side by side.
![osTicket C5](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/b19494c5-b9e7-4961-a4d7-1db258238eaf)
**Configure IIS Internet Information Services**
Go to Windows Right click the Start menu, and click run, type control in

![osTicket C 6](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/606dbf42-dfa9-4ca8-a0b9-cfe5d522a01c)

Select **Programs**\> **Turn Windows features on or off**\> Select the following features
 Internet Information Services and then expand, expand World Wide Web Services
Expand Application Development Features
 CGI and then collapse Application Development Features
Expand Common HTTP Features (select all)
 Default Document  Directory Browsing  HTTP Errors
 HTTP Redirection  Static Content  WebDAV Publishing
Now click **OK** and wait for **Windows completed the requested changes.** Click on **Close**
![osTicket C Click on Close](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/c8ee363d-fcaf-4af1-8669-31fbe45cf4c9)

Confirm the installation of **IIS**, go to a VM browser and type 127.0.0.1 to observe the page.
![osTicket C 7](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/26179fd5-37eb-4898-ab06-72a639a71362)

**PHP Manager for IIS**, download and install.
Go to installation files and **Download**\> This file type might be dangerous \> Download anyway
Go to File Explorer, observe the downloaded file. 
![osTicket C 10](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/cb63416a-3c1f-4bdf-8f3a-da68b9d39e16)

Double-click the file and follow the Setup Wizard
Next \>  I Agree \> Next \> Close \> ****** Repair PHP Manager for IIS**\> Finish \> Close

**Rewrite Module**, download and install.
Go to installation files and **Download**\> This file type might be dangerous \> Download anyway
Go to File Explorer, observe the downloaded file.
![osTicket C 9](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/ed11b671-a6a7-4f0b-adf7-e413ee0620cd)

Double-click the file and follow the Setup Wizard
Install \> Finish \> Close

**Create a directory C:\PHP**

Go to File Explorer \> enter C: \>New \> Folder \>PHP

![osTicket C 11](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/d1a8c340-385d-4511-a6c1-b875356f4742)

**php-7.3.8-nts-Win32-VC15-x86.zip**

Go to installation files and **Download**\> This file type might be dangerous \> Download anyway

Go to File Explorer, observe the downloaded file.

![osTicket C 12](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/a4804fe8-24d5-4b23-92a5-996942d104e1)

Right-click \> Extract All…\> Extract into the PHP Folder select Browse…This PC \> Windows(C:) \>
PHP \> **Select Folder** then click **Extract**
![osTicket C 13](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/ff34a2de-5b02-43d7-a38d-70fe00387887)


**VC-redist.x86.exe**
Go to installation files and **Download**\> This file type might be dangerous \> Download anyway
Go to File Explorer, observe the downloaded file.
![osTicket C 14](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/fecd4234-24d8-459b-8636-5f402a75f8d9)









Double-click on download \>  I agree to the license terms and conditions \> Install \> Close
![osTicket C 15](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/3637abd3-6411-4298-abbd-2303e5ea6c3f)


**Mysql-5.5.62-win32.msi**
Go to installation files and **Download**\> This file type might be dangerous \> Download anyway
Go to File Explorer, observe the downloaded file.
![osTicket C 16](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/7d9e0b68-b765-4d6f-88af-4376682111a0)


Next \>  I accept the terms in the License Agreement \> Next \> Typical \> Install \>
 Launch the MySQL Instance Configuration Wizard \> Finish \> Next \> Standard Configuration\>
Next \> Install As Windows Service Next \> New **root** password: **Password1**| Confirm: **Password1**
Next \> Execute \> Processing configuration…\> Finish

![osTicket C 17](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/697408f4-58ce-4ee1-84de-1ae71279c8e7)![osTicket C 18](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/b081d63d-2ba0-4aae-bfb8-57591894ee91)

**Open IIS as an Administrator**

Click on **Microsoft Start**, enter **IIS** and **Run as administrator.**
![osTicket C 19](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/3460aa06-3e67-4764-bfec-5dcdd186cc2b)


Observe previous downloads URL Rewrite and PHP Manager \> Click on **PHP Manager**
![osTicket C 20](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/70fae9f6-52b0-4167-9b86-9e0af6d11f40)
![osTicket C 21](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/2fbeef7b-debe-4e79-9f3c-53d007910e8a)










Click on **Register new PHP version**\> Browse…\> PHP \> php-cgi \> Open\> OK




Click on **vm-osTicketC**(vm-osTicketC) and click on **Restart**



**Install osTicket**
Go to installation files and **Download**\> This file type might be dangerous \> Download anyway
Go to **File Explorer**, observe the downloaded file. Open another **File Explorer** placing them side by side.
![osTicket C 24](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/3af4a372-99d0-4e7f-9a6f-c285e35f5504)


Double-click osTicket on green arrow page, so that you can drag and drop the upload folder.
On the other window, go to This PC \> Windows (C:) \> inetpub \> wwwroot \> iisstart
![osTicket C 25](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/92bf91fa-b814-4101-af3f-efa47202a4a8)
![osTicket C 26](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/c18b6844-6673-4012-a460-a7588d36c039)

Rename **upfold** folder to **osTicket**
![osTicket C 27](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/45744c58-1cec-4710-a42c-17c56fa4f417)

Open **IIS** and **Restart** the server
![osTicket C 28](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/e4b4f2d6-7f06-4958-9e37-e7cad18c6090)


vm-osTicketC \> Sites \> Default Web Site \>osTicket \> Browse \*.80 (http)
![osTicket C 29](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/46a88a5d-8ea2-439b-97a7-005af7a83dfa)


**osTicket Installer** appears \> Observe some features are not enabled # **X.**
![osTicket C 31](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/2ceae063-7c56-445d-bb41-bb28ad2fc0ad)












![osTicket C 30](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/88004c7a-a9a9-462e-bb26-8325aa66a475)


Go back to IIS \> Default Web Site \> osTicket \> Double-click on PHP Manager
Click Enable or Disable an extension \> Enable
PHP IMAP Extension | Intl Extension | APCu Extension | Zend OP cache Extension & refresh
![osTicket C 32](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/f899734b-e684-4613-a48f-e8000a1f7093)



**Rename ost-config.php**

Go to File Explorer \> This PC \> C: Drive \> wwwroot \> and open osTicket
Double-include \> find **ost-sampleconfig.php** and delete out sample
File is not named **ost-config.php**
![osTicket C 33](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/c9229f79-f802-4049-ab26-cff42bddfdbb)


**Assign Permission on ost-config.php**

Right-click on the file \> Properties \> Security \> Advanced \>
![osTicket C 34](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/cf01f7d4-3c04-4591-869b-77b9737206ee)


Click on **Remove all inherited permissions from this object**.

Click Add \> Open **Select a principal**\> Enter the object name to select **everyone**

Check Names \> OK \>

 Full control  Modify  Read & execute  Read  Write Check all and **OK**
![osTicket C 35](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/c4f1816c-cfbd-4859-a8eb-a754f4bcc85c)



Click Apply \> OK \> OK

**Set up osTicket in the browser**

Go to osTicket \> Continue

Helpdesk Name: **TD Help Desk** Default Email: [td@helper.com](mailto:td@helper.com)

Admin User

First: **Terry** Last: **Davis** Email: [**td@gmail.com**](mailto:td@gmail.com)

Username: **Terry** Password: **Password1**

**Install HeidiSQL**
Go to installation files and **Download**\> This file type might be dangerous \> Download anyway
Go to File Explorer, observe the downloaded file.
![osTicket C 37](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/c54c9086-0772-4b73-85d9-42f93ff6673f)


 I accept the agreement \> Next \> Next \> Next \> Install \>  Launch FeidiSQL \> Finish \> **Donate Feature** Skip \>Donate.


Create a new connection
Click + New
![osTicket C 38](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/f3276974-ece4-40da-9709-1aad41a17a45)


Select Unnamed \> Create new \> Database \> Name osTicket \> OK
![osTicket C 39](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/622707f8-76de-4fc1-ae13-9ab67fbe7496)



Go back to osTicket and enter the following:

| **MySQL Table Prefix**| **MySQL Hostname**| **MySQL Database**| **MySQL Username**| **MySQL Password**|
| --- | --- | --- | --- | --- |
| ost\_ | Localhost | osTicket | Root | Password1 |

Click on **Install Now**
![osTicket C 40](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/3b80e98c-3be0-4dbc-8d8a-d8d2ff6e3f84)



**Delete: C:\\inetpub\wwwroot\osTicket\setup**

Go to inetpub\> wwwroot \> osTicket \> setup Right-click and Delete

Set Permissions to: **Read only**

Go to include\>ost-config.php \> Right-click Properties \> Security \> Advanced \> Everyone\> Edit so that  Read & execute  Read are selected \> OK \> Apply \> OK
![osTicket C 41](https://github.com/TDCybersecurity/osTicket-Installation-2/assets/142702123/782a323f-c390-47d9-84da-854501b09520)



Confirm osTicket Admin login: [http://localhost/osTicket/scp/login.php](http://localhost/osTicket/scp/login.php)

Confirm End User login: [http://localhost/osTicket/](http://localhost/osTicket/)



![](RackMultipart20240527-1-gnqdxa_html_1e2f03c92d08c9d8.png)
