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

3.	Create an EC2 Key Pair: In this step, I created a key-pair in EC2 instance. The purpose of EC2 key pair is to securely connect Amazon Elastic Compute Cloud. The key pair consists of a public key and private key which are used to secure and authenticate my access to the instance. For providing my public key, I went to Ubuntu terminal and typed ssh-keygen. 

<p align="center">
<img src="https://i.ibb.co/pZ0MdRP/5.jpg" height="80%" width="80%" alt="Hosting of Password Management System in AWS"/>
<br />
<br />

<p align="center">
<img src="https://i.ibb.co/NSZHyGM/6.jpg" height="80%" width="80%" alt="Hosting of Password Management System in AWS"/>
<br />
<br />

<p align="center">
<img src="https://i.ibb.co/9crNG4r/8.jpg" height="80%" width="80%" alt="Hosting of Password Management System in AWS"/>
<br />
<br />

<p align="center">
<img src="https://i.ibb.co/FBzHgD8/9.jpg" height="80%" width="80%" alt="Hosting of Password Management System in AWS"/>
<br />
<br />

4.	Buy a Domain Name (Very Cheap) for IP Address EC2 Instance: Passbolt is successfully installed. Now it is the time for configuration. When I clicked on "Get Started", I could see that SSL is not configured. I must configure SSL otherwise password will be sent in clear text. To configur SSL, I need a Domain Name to associate it with IP address. I bought the Domain Name "passbolt.click" from NameCheap.


<p align="center">
<img src="https://i.ibb.co/CtN9Q0N/10.jpg" height="80%" width="80%" alt="Hosting of Password Management System in AWS"/>
<br />
<br />

<p align="center">
<img src="https://i.ibb.co/SJZWhTh/11.jpg" height="80%" width="80%" alt="Hosting of Password Management System in AWS"/>
<br />
<br />

<p align="center">
<img src="https://i.ibb.co/NYsvBsp/14.jpg" height="80%" width="80%" alt="Hosting of Password Management System in AWS"/>
<br />
<br />

5.	Configuration of nginx Server on Ubuntu for SSL Connection: To do so, I must connect to our ec2 instance from our ubuntu via SSH. I took the IP address (54.252.193.206) from EC2 instance and typed command “ssh admin@54.252.193.206”. I was then connected to Passbolt via SSH. To open the configuration file of nginx, I typed “sudo nano /etc/nginx/sites-enabled/nginx-passbolt.conf”  and put server name : “passbolt.click” . Then I saved the configuration file and started proceeding with nginx server configuration. Once configured, the https version of the domain (https://passbolt.click) was available. Then I completed the remaining configuration from the website.

<p align="center">
<img src="https://i.ibb.co/zm1bXHd/18.jpg" height="80%" width="80%" alt="Hosting of Password Management System in AWS"/>
<br />
<br />

6.	Download Passbolt Extension in the Web Browser (Chrome/Firefox):

<p align="center">
<img src="https://i.ibb.co/VQmY9nd/19.jpg" height="80%" width="80%" alt="Hosting of Password Management System in AWS"/>
<br />
<br />

<p align="center">
<img src="https://i.ibb.co/s943DGY/20.jpg" height="80%" width="80%" alt="Hosting of Password Management System in AWS"/>
<br />
<br />

<p align="center">
<img src="https://i.ibb.co/sJBRjbJ/21.jpg" height="80%" width="80%" alt="Hosting of Password Management System in AWS"/>
<br />
<br />

7.	Testing of Newly Created Password Manager

<p align="center">
<img src="https://i.ibb.co/TwM2dgm/22.jpg" height="80%" width="80%" alt="Hosting of Password Management System in AWS"/>
<br />
<br />

8.	Deletion of EC2 Instance in AWS to Avoid Further Cost

<p align="center">
<img src="https://i.ibb.co/FWVxVCG/23.jpg" height="80%" width="80%" alt="Hosting of Password Management System in AWS"/>
<br />
<br />
