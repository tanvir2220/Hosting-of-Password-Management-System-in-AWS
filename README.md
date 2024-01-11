<h1>Hosting of Password Management System in AWS</h1>


<h2>Overview</h2>
The project involves creation of Passbolt, a self-hosted password manager, to securely store and manage complex passwords in AWS cloud
<br />

<h2>Environments Used </h2>

- <b>Amazon Web Services</b>
- <b>Ubuntu 22.04.3 LTS</b>
- <b>Passbolt Community Edition AMI</b>


<h2>To-Do</h2>

To successfully complete the project, we need to perform following tasks:

1.	Create Free AWS Account
2.	Deployment of Passbolt to AWS
3.	Create an EC2 Key Pair 
4.	Buy a Domain Name (Very Cheap) for IP Address EC2 Instance
5.	Configuration of nginx Server on Ubuntu for SSL Connection
6.	Download Passbolt Extension in the Web Browser (Chrome/Firefox)
7.	Testing of Newly Created Password Manager
8.	Deletion of EC2 Instance in AWS to Avoid Further Cost



<h2>Program Walk-Through</h2>

1.	Create Free AWS Account: First of all, I created free AWS Subscription. Make sure you delete the EC2 instances that has all of our resources in it otherwise it will eat up our subscription cost. Here's the link: https://aws.amazon.com/free
   
2.	Deployment of Passbolt to AWS: In this step, I went to https://www.passbolt.com/pricing/pro and selected Community Edition. Then I selected AWS from "Deploy on your favorite cloud provider" section.

<p align="center">
<img src="https://i.ibb.co/DrkcgRD/24.jpg" height="80%" width="80%" alt="Hosting of Password Management System in AWS"/>
<br />
<br />

<p align="center">
<img src="https://i.ibb.co/YDk8JNr/2.jpg" height="80%" width="80%" alt="Hosting of Password Management System in AWS"/>
<br />
<br />
  
<p align="center">
<img src="https://i.ibb.co/XLb6jGC/3.jpg" height="80%" width="80%" alt="Hosting of Password Management System in AWS"/>
<br />
<br />
  
<p align="center">
<img src="https://i.ibb.co/4VZNT5n/4.jpg" height="80%" width="80%" alt="Hosting of Password Management System in AWS"/>
<br />
<br />

4.	Allow all in NIC Network Security Group in Azure: In this step, I will allow all incoming connection in NIC Network Security Group in Microsofot Azure. The purpose of this is to make is completely vulnerable, acting like a honeypot.

<p align="center">
<img src="https://i.ibb.co/TBD7zNt/1.jpg" height="80%" width="80%" alt="Hosting of Password Management System in AWS"/>
<br />
<br />

4.	Create Log Analytics Workspace: Now I will create a Log Analytics Workspace. The purpose of this is to ingest logs from the virtual machine to Log Analytics Workspace. I will then create custom log that contains geographic information.

<p align="center">
<img src="https://i.ibb.co/zmdqtbL/2.jpg" height="80%" width="80%" alt="Create Honeypots to Observe LIVE Cyber Attacks and Convert Source IP to Geolocation"/>
<br />
<br />

5.	Enable gathering VM logs in Microsoft Defender for Cloud: Next i will go to "Defender Plans" and "Data Collection" in Microsoft Defender for Cloud and do the following:

<p align="center">
<img src="https://i.ibb.co/wK7hbPg/3.jpg" height="80%" width="80%" alt="Create Honeypots to Observe LIVE Cyber Attacks and Convert Source IP to Geolocation"/>
<br />
<br />

<p align="center">
<img src="https://i.ibb.co/XY9Ktrv/4.jpg" height="80%" width="80%" alt="Create Honeypots to Observe LIVE Cyber Attacks and Convert Source IP to Geolocation"/>
<br />
<br />

6.	Connect Log Analytics to VM: Then connect Log Analytics to Virtual Machine which I created earlier.

<p align="center">
<img src="https://i.ibb.co/SyMr0pW/6.jpg" height="80%" width="80%" alt="Create Honeypots to Observe LIVE Cyber Attacks and Convert Source IP to Geolocation"/>
<br />
<br />

7.	Setup Microsoft Sentinel

<p align="center">
<img src="https://i.ibb.co/9T6XyDT/5.jpg" height="80%" width="80%" alt="Create Honeypots to Observe LIVE Cyber Attacks and Convert Source IP to Geolocation"/>
<br />
<br />

8.	Log into VM with Remote Desktop

<p align="center">
<img src="https://i.ibb.co/rfzqnyJ/7.jpg" height="80%" width="80%" alt="Create Honeypots to Observe LIVE Cyber Attacks and Convert Source IP to Geolocation"/>
<br />
<br />

9.	Observe Event Viewer Logs in VM

<p align="center">
<img src="https://i.ibb.co/K2JrGYw/9.jpg" height="80%" width="80%" alt="Create Honeypots to Observe LIVE Cyber Attacks and Convert Source IP to Geolocation"/>
<br />
<br />

10.	Turn off Windows Firewall on VM: Then I turned off Windows Firewall in the Virtual Machine.

11.	Download PowerShell Script: Now download the PowerShell script from the link https://github.com/joshmadakor1/Sentinel-Lab/blob/main/Custom_Security_Log_Exporter.ps1. Run the script from VM's Windows PowerShell ISE.

<p align="center">
<img src="https://i.ibb.co/7SWwC4y/11.jpg" height="80%" width="80%" alt="Create Honeypots to Observe LIVE Cyber Attacks and Convert Source IP to Geolocation"/>
<br />
<br />

12.	Get Geolocation.io API Key: However, before running the script in the previous step, we must get our own API key from https://ipgeolocation.io/

13.	Run Script To get Geo Data from attackers: As soon as someone tries to login to honeypot, the log will be saved in C:\ProgramData directory. Itried to login with incorrect password and here's the saved log:

<p align="center">
<img src="https://i.ibb.co/JrNpC4m/12.jpg" height="80%" width="80%" alt="Create Honeypots to Observe LIVE Cyber Attacks and Convert Source IP to Geolocation"/>
<br />
<br />

14.	Create custom log in Log Analytics Workspace to bring in our custom log

<p align="center">
<img src="https://i.ibb.co/fxd1GyD/15.jpg" height="80%" width="80%" alt="Create Honeypots to Observe LIVE Cyber Attacks and Convert Source IP to Geolocation"/>
<br />
<br />

15.	Create custom fields/extract fields from raw custom log data

<p align="center">
<img src="https://i.ibb.co/Z19S808/16.jpg" height="80%" width="80%" alt="Create Honeypots to Observe LIVE Cyber Attacks and Convert Source IP to Geolocation"/>
<br />
<br />

<p align="center">
<img src="https://i.ibb.co/6WKDpVC/23.jpg" height="80%" width="80%" alt="Create Honeypots to Observe LIVE Cyber Attacks and Convert Source IP to Geolocation"/>
<br />
<br />

<p align="center">
<img src="https://i.ibb.co/JxxHvfm/24.jpg" height="80%" width="80%" alt="Create Honeypots to Observe LIVE Cyber Attacks and Convert Source IP to Geolocation"/>
<br />
<br />

16.	Testing Extracts: I tested the extract with following code:

Sentinel Map Query

FAILED_RDP_WITH_GEO_CL | summarize event_count=count() by sourcehost_CF, latitude_CF, longitude_CF, country_CF, label_CF, destinationhost_CF
| where destinationhost_CF != "samplehost"
| where sourcehost_CF != ""

<p align="center">
<img src="https://i.ibb.co/1XzrMYH/25.jpg" height="80%" width="80%" alt="Create Honeypots to Observe LIVE Cyber Attacks and Convert Source IP to Geolocation"/>
<br />
<br />

<p align="center">
<img src="https://i.ibb.co/P1Qv23Y/21.jpg" height="80%" width="80%" alt="Create Honeypots to Observe LIVE Cyber Attacks and Convert Source IP to Geolocation"/>
<br />
<br />
   
17.	Setup map in sentinel with Latitude and Longitude (or country)

<p align="center">
<img src="https://i.ibb.co/CH3t5Zm/20.jpg" height="80%" width="80%" alt="Create Honeypots to Observe LIVE Cyber Attacks and Convert Source IP to Geolocation"/>
<br />
<br />

<p align="center">
<img src="https://i.ibb.co/YtNWSL8/22.jpg" height="80%" width="80%" alt="Create Honeypots to Observe LIVE Cyber Attacks and Convert Source IP to Geolocation"/>
<br />
<br />
