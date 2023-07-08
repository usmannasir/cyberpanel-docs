# **1.1 Installing CyberPanel**

## Requirements for Installation.

To install CyberPanel, the following requirements must be met.

- Server with fresh install of **Centos 7**.x (Not recommended for new installs), **Centos 8.x, Ubuntu 18.04, Ubuntu 20.04, AlmaLinux 8, Ubuntu 22.04**

- **Python 3.x**

- **1024MB RAM, or higher**

- **10GB Disk Space**

## **Cyberpanel** with **Cyberpanel Ent**

CyberPanel is 100% identical in both versions. The only difference is which web server is running in the back-end.

1. **Cyberpanel** normallycomes with OpenLiteSpeed and it is completely free for an unlimited number of domains (You can host unlimited domains) and work processes.
2. **Cyberpanel Enterprise** comes with LiteSpeed Web Server Enterprise and it is free for one domain and if you want for multiple domains you can get different plans according to your needs on the [Pricing page](https://cyberpanel.net/litespeed-enterprise/). The Cyberpanel License includes the price of the Litespeed Enterprise license.

To learn more about **Open Litespeed** and **Litespeed Enterprise** please check this comprehensive [comparison](https://www.litespeedtech.com/products/litespeed-web-server/editions).

Let's move towards the installation.

## **Installing CyberPanel**
The installation of the cyberpanel is very simple and easy, just follow the instructions accordingly.

- **Step 1** : **Connect to server via SSH client.** ( **Putty** , **Bitvise SSH client** , etc)
 First login to your server through SSH client as a Root user (Sudo will not work). You can get the Login detail from your web host.
- **Step 2** : **Update server Packages.**
 Update your server OS first (Because it updated overall services because it provides much better compatibility)
 Run this command
 For Ubuntu:
sudo apt update && sudo apt upgrade -y
 For CentOS/Alma/Rocky:
sudo yum **check-update**
sudo yum **update**
- **Step 3** : **Run the Installation Script.**
 Execute the provided command to initiate the automated installation script. This script will guide you through several decisions regarding the LiteSpeed version and additional add-ons you wish to install.

sh \<(curl https://cyberpanel.net/install.sh || wget -O - https://cyberpanel.net/install.sh)


For some reason, If you are not login as root user, Then use this below Script

sudo su - -c "sh \<(curl https://cyberpanel.net/install.sh || wget -O - https://cyberpanel.net/install.sh)"

- **Step 4** : **Select the version of LiteSpeed that you would like to use.**
 As mentioned above in the **Cyberpanel** with **Cyberpanel Ent** Select which version of Litespeed You want to Install. If you select Litespeed Enterprise, Please first ensure that you have got the license key. You can visit the [Pricing page](https://cyberpanel.net/litespeed-enterprise/) to get the required plan.

 ![](RackMultipart20230708-1-uput1w_html_5c35f0d1cd5eb1a2.png)
 If you selected LiteSpeed Enterprise, you will see the following prompt. Enter your serial number

If you do not have any license, you can also use trial license (if server has not used trial license before), type TRIAL

Please input your serial number for LiteSpeed WebServer Enterprise:

- **Step 5** : **Select Services and Packages.**
 You will encounter a sequence of prompts offering various options and add-ons for selection.
 - **Full Service (default Y):**
 ![](RackMultipart20230708-1-uput1w_html_1c1b24df530b05c.png)
[**PowerDNS**](https://www.powerdns.com/) **-**  **an open-source DNS server**
[**Postfix**](http://www.postfix.org/) **-**  **open-source mail transfer agent**
[**Pure-FTPd**](https://www.pureftpd.org/project/pure-ftpd/) **-**  **open-source FTP server**

-**Remote MySQL (default N):**
Allow for your Database to be installed on a remote server
 ![](RackMultipart20230708-1-uput1w_html_3646cb2cf884f904.png)
 - **CyberPanel Version (default Latest Version):**
You can choose to install a previous version of CyberPanel, or press Enter to install the latest version.
 ![](RackMultipart20230708-1-uput1w_html_351e25520126970c.png)
 - **Password (default "1234567"):**
Using the default password is **not advisable**. It is recommended to set a **strong** password of your own by choosing 's' or generate a **random** password by selecting 'r'. After the installation, you will see the password prompt displayed on the screen.
 ![](RackMultipart20230708-1-uput1w_html_f96eda6589da964c.png)
 - **Memcached (default Y):**

![](RackMultipart20230708-1-uput1w_html_5227d7e80ac95506.png)

Distributed memory object caching system

- **Redis (default Y):**

![](RackMultipart20230708-1-uput1w_html_dd04fdc0b0a7f47.png)

In-memory data structure store, used as a database, cache, and message broke

- **Watchdog (default Yes)**:

![](RackMultipart20230708-1-uput1w_html_77980c7e441aec9c.png)

Kernel watchdog is used to monitor if a system is running. It is supposed to automatically reboot hanged systems due to unrecoverable software errors

- **Step 6: Installation Processing**

The installation process will initiate automatically and is expected to complete within 5-10 minutes, depending on your server's speed.

- **Step 7: Finalize Installation**

Upon completion of the installation process, you will encounter a screen displaying important information regarding your configuration. It is recommended to select and securely copy this information to a safe location for future reference.