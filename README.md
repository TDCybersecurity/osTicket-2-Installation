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

![](RackMultipart20240527-1-gnqdxa_html_9873744417c50fa6.png)

| Php-7.3.8-nts-Win32-VC15-x86 | HeidiSQL\_12.3.0.6589 | mysql-5.5.62-win32.msi | osTicket-v1.15.8.zip |
| --- | --- | --- | --- |
| PHPManagerForIIS.V1.5.0.msi | Rewrite\_amd64\_en\_US.smi | VC\_redist.x86.ext |
 |

Ideally, you want to have both screens side by side.

![](RackMultipart20240527-1-gnqdxa_html_32735f9d16250266.png)

**Configure IIS Internet Information Services**

Go to Windows Right click the Start menu, and click run, type control in

![](RackMultipart20240527-1-gnqdxa_html_45da475d0a3fe539.png)

Select **Programs**\> **Turn Windows features on or off**\> Select the following features

 Internet Information Services and then expand, expand World Wide Web Services

Expand Application Development Features

 CGI and then collapse Application Development Features

Expand Common HTTP Features (select all)

 Default Document  Directory Browsing  HTTP Errors

 HTTP Redirection  Static Content  WebDAV Publishing

Now click **OK** and wait for **Windows completed the requested changes.** Click on **Close**

![](RackMultipart20240527-1-gnqdxa_html_acc795fa125d2fe1.png)

Confirm the installation of **IIS**, go to a VM browser and type 127.0.0.1 to observe the page.

![](RackMultipart20240527-1-gnqdxa_html_8b8d8a39913b21d7.png)

**PHP Manager for IIS**, download and install.

Go to installation files and **Download**\> This file type might be dangerous \> Download anyway

Go to File Explorer, observe the downloaded file. ![](RackMultipart20240527-1-gnqdxa_html_f891bc79b2b4127b.png)

Double-click the file and follow the Setup Wizard

Next \>  I Agree \> Next \> Close \> ****** Repair PHP Manager for IIS**\> Finish \> Close

**Rewrite Module**, download and install.

Go to installation files and **Download**\> This file type might be dangerous \> Download anyway

Go to File Explorer, observe the downloaded file.

![](RackMultipart20240527-1-gnqdxa_html_dedac01a49dc2664.png)

Double-click the file and follow the Setup Wizard

Install \> Finish \> Close

**Create a directory C:\PHP**

Go to File Explorer \> enter C: \>New \> Folder \>PHP

![](RackMultipart20240527-1-gnqdxa_html_51b0ebb46e175f74.png)

**php-7.3.8-nts-Win32-VC15-x86.zip**

Go to installation files and **Download**\> This file type might be dangerous \> Download anyway

Go to File Explorer, observe the downloaded file.

![](RackMultipart20240527-1-gnqdxa_html_81aec343c6122caa.png)

Right-click \> Extract All…\> Extract into the PHP Folder select Browse…This PC \> Windows(C:) \>

PHP \> **Select Folder** then click **Extract**

![](RackMultipart20240527-1-gnqdxa_html_5cdce8131f0e6bf.png)

**VC-redist.x86.exe**

Go to installation files and **Download**\> This file type might be dangerous \> Download anyway

Go to File Explorer, observe the downloaded file.

![](RackMultipart20240527-1-gnqdxa_html_eb183c748c96ca6c.png)

Double-click on download \>  I agree to the license terms and conditions \> Install \> Close

![](RackMultipart20240527-1-gnqdxa_html_85e363423323b0ba.png)

**Mysql-5.5.62-win32.msi**

Go to installation files and **Download**\> This file type might be dangerous \> Download anyway

Go to File Explorer, observe the downloaded file.

![](RackMultipart20240527-1-gnqdxa_html_774c7844dd57b93e.png)

Next \>  I accept the terms in the License Agreement \> Next \> Typical \> Install \>

 Launch the MySQL Instance Configuration Wizard \> Finish \> Next \> Standard Configuration\>

Next \> Install As Windows Service Next \> New **root** password: **Password1**| Confirm: **Password1**

Next \> Execute \> Processing configuration…\> Finish

![](RackMultipart20240527-1-gnqdxa_html_52a0f32e68319a89.png) ![](RackMultipart20240527-1-gnqdxa_html_578c052b974e557f.png)

**Open IIS as an Administrator**

Click on **Microsoft Start**, enter **IIS** and **Run as administrator.**

![](RackMultipart20240527-1-gnqdxa_html_5b3ef7d6c2c353f5.png)

Observe previous downloads URL Rewrite and PHP Manager \> Click on **PHP Manager**

![](RackMultipart20240527-1-gnqdxa_html_581dcd8bebfc455d.png)

![](RackMultipart20240527-1-gnqdxa_html_227cb23f303c5e73.png)

Click on **Register new PHP version**\> Browse…\> PHP \> php-cgi \> Open\> OK

![](RackMultipart20240527-1-gnqdxa_html_3b7454cd196720e.png)

Click on **vm-osTicketC**(vm-osTicketC) and click on **Restart**

![](RackMultipart20240527-1-gnqdxa_html_c4f450d615b90638.png)

**Install osTicket**

Go to installation files and **Download**\> This file type might be dangerous \> Download anyway

Go to **File Explorer**, observe the downloaded file. Open another **File Explorer** placing them side by side.

![](RackMultipart20240527-1-gnqdxa_html_648a3445749766ec.png)

Double-click osTicket on green arrow page, so that you can drag and drop the upload folder.

On the other window, go to This PC \> Windows (C:) \> inetpub \> wwwroot \> iisstart

![](RackMultipart20240527-1-gnqdxa_html_e4fc8e70a85ab747.png)

![](RackMultipart20240527-1-gnqdxa_html_6e074a48e1f3281f.png)

Rename **upfold** folder to **osTicket**![](RackMultipart20240527-1-gnqdxa_html_423ec240ba1a2a7e.png)

Open **IIS** and **Restart** the server

![](RackMultipart20240527-1-gnqdxa_html_1a99d1d6199eebc4.png)

Vm-osTicketC \> Sites \> Default Web Site \>osTicket \> Browse \*.80 (http)

![](RackMultipart20240527-1-gnqdxa_html_46dfc8dd297cdbc7.png)

**osTicket Installer** appears \> Observe some features are not enabled
# **X.**

![](RackMultipart20240527-1-gnqdxa_html_a6e2153c657e68e7.png)

Go back to IIS \> Default Web Site \> osTicket \> Double-click on PHP Manager

Click Enable or Disable an extension \> Enable

PHP IMAP Extension | Intl Extension | APCu Extension | Zend OP cache Extension & refresh

![](RackMultipart20240527-1-gnqdxa_html_e9c5b57b11271c76.png)

**Rename ost-config.php**

Go to File Explorer \> This PC \> C: Drive \> wwwroot \> and open osTicket

Double-include \> find **ost-sampleconfig.php** and delete out sample

File is not named **ost-config.php**

![](RackMultipart20240527-1-gnqdxa_html_a05038432c98277b.png)

**Assign Permission on ost-config.php**

Right-click on the file \> Properties \> Security \> Advanced \>

![](RackMultipart20240527-1-gnqdxa_html_f1d0ba25ac67a683.png)

Click on **Remove all inherited permissions from this object**.

Click Add \> Open **Select a principal**\> Enter the object name to select **everyone**

Check Names \> OK \>

 Full control  Modify  Read & execute  Read  Write Check all and **OK**

![](RackMultipart20240527-1-gnqdxa_html_e86e4c90495c9abd.png)

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

![](RackMultipart20240527-1-gnqdxa_html_4be4bae99811d011.png)

![](RackMultipart20240527-1-gnqdxa_html_57f6df1dad433e0e.png)

 I accept the agreement \> Next \> Next \> Next \> Install \>  Launch FeidiSQL \> Finish \> **Donate Feature** Skip \>Donate.

Create a new connection

Click + New

![](RackMultipart20240527-1-gnqdxa_html_780b2245a629b076.png)

Select Unnamed \> Create new \> Database \> Name osTicket \> OK

![](RackMultipart20240527-1-gnqdxa_html_c18f6595d9a55d1f.png)

Go back to osTicket and enter the following:

| **MySQL Table Prefix**| **MySQL Hostname**| **MySQL Database**| **MySQL Username**| **MySQL Password**|
| --- | --- | --- | --- | --- |
| ost\_ | Localhost | osTicket | Root | Password1 |

Click on **Install Now**

![](RackMultipart20240527-1-gnqdxa_html_14053e9c7ca7054d.png)

**Delete: C:\\inetpub\wwwroot\osTicket\setup**

Go to inetpub\> wwwroot \> osTicket \> setup Right-click and Delete

Set Permissions to: **Read only**

Go to include\>ost-config.php \> Right-click Properties \> Security \> Advanced \> Everyone\> Edit so that  Read & execute  Read are selected \> OK \> Apply \> OK

![](RackMultipart20240527-1-gnqdxa_html_eabf3a662075af85.png)

Confirm osTicket Admin login: [http://localhost/osTicket/scp/login.php](http://localhost/osTicket/scp/login.php)

Confirm End User login: [http://localhost/osTicket/](http://localhost/osTicket/)

![](RackMultipart20240527-1-gnqdxa_html_673c8136fdd1ae87.png)

![](RackMultipart20240527-1-gnqdxa_html_1e2f03c92d08c9d8.png)
