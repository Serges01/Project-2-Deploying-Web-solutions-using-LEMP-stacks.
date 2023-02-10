
# Deploying-Web-solutions-using-LEMP-stacks.

In this project you will implement a web solutions deployment using LEMP stacks.

Basically a stack is just a way of keeping things in order one over the other. 

Therefore a technology stack keeps them together or it is a combination of several technologies stacked together in order to build an application. 

They are acronymns for individual technologies used together for a specific technology product. some examples are:

LAMP (Linux, Apache, MySQL, PHP or Python, or Perl).

LEMP (Linux, Nginx, MySQL, PHP or Python, or Perl).

MERN (MongoDB, ExpressJS, ReactJS, NodeJS).

MEAN (MongoDB, ExpressJS, AngularJS, NodeJS.


## Step 0 Preparing Prerequisites

In order to complete this project you will need an AWS account and a virtual server with Ubuntu Server OS.


After creating your AWS account, log in to reach the console home as seen below.

<img width="1000" alt="image" src="https://user-images.githubusercontent.com/38444929/218208486-52bc90f7-f675-4655-9254-3916a73c215c.png">


Click on the EC2 service in order to create an instance.

 <img width="1000" alt="image" src="https://user-images.githubusercontent.com/38444929/218211151-8bdb052f-cf7c-4576-9829-8fe696d77900.png">
 
 I have already created some instances. So to create one click on launch instance.
 
 <img width="1000" alt="image" src="https://user-images.githubusercontent.com/38444929/218212100-6a7d89d2-1645-41e1-8db0-9c1e3c2df1d5.png">

 Give a name to your server.
 
 <img width="1000" alt="image" src="https://user-images.githubusercontent.com/38444929/218212562-f36d67cd-7ce6-4dd4-99a5-5458d9cff900.png">

 
Launch a new "EC2" instance of t2.micro family with Ubuntu Server 22.04 LTS(HVM) 64 bit

<img width="1000" alt="image" src="https://user-images.githubusercontent.com/38444929/218214012-ff8b9b8b-8326-4630-a9ed-59c3da67dd9a.png">

You can use a key pair to securely connect to your instance. Ensure that you have access to the selected key pair before you launch the instance. 

<img width="1000" alt="image" src="https://user-images.githubusercontent.com/38444929/218214213-8d381383-4c03-4d12-81dc-b036ac7a330a.png">


Click on Create new key pair then click on Create key pair.

<img width="1000" alt="image" src="https://user-images.githubusercontent.com/38444929/218214309-cedaf497-5197-4d13-a53f-b747b484ab68.png">

Configure Security Group; A security group acts as a virtual firewall for your EC2 instances to control incoming and outgoing traffic. Inbound rules control the incoming traffic to your instance, and outbound rules control the outgoing traffic from your instance. When you launch an instance, you can specify one or more security groups. 

<img width="1000" alt="image" src="https://user-images.githubusercontent.com/38444929/218214646-08a06838-8009-49f4-8713-f42d21680c28.png">

Click on create security group.

Under the Network settings, select existing security group.

<img width="1000" alt="image" src="https://user-images.githubusercontent.com/38444929/218214837-9e770dc6-4d3a-4562-8e4b-3cfb05905c31.png">

Click on security groups to select the security groups to select the security group created.

<img width="1000" alt="image" src="https://user-images.githubusercontent.com/38444929/218216984-df5bae1c-d088-42a8-b7ba-295f7ed245ea.png">

Then click on launch instance.

<img width="1000" alt="image" src="https://user-images.githubusercontent.com/38444929/218217359-ac1864fe-462e-45bb-92fe-887a2871717b.png">

Click on instance to see if the new created one is running.

<img width="1000" alt="image" src="https://user-images.githubusercontent.com/38444929/218218300-2e5e91b5-d626-452d-b8f5-fb8527a69bec.png">

Click on the running instance in order to see the instance details.

<img width="1000" alt="image" src="https://user-images.githubusercontent.com/38444929/218218655-50454612-1aca-4538-a597-276249ccba3f.png">


Next is to connect my instance to an SSH Client by clicking on connect.

<img width="1000" alt="image" src="https://user-images.githubusercontent.com/38444929/218218840-a598ec01-b83e-4b8e-9d1c-ae89acae0892.png">

Connecting to EC2 terminal

Using the terminal on MAC/Linux

•	The terminal is already installed by default. You just need to open it up.

•	You do not need to convert to a .ppk file. Just use the same key as downloaded from AWS.

•	Change directory into the location where your PEM file is. Most likely will be in the Downloads folder

```
cd ~/Downloads
```

•	Change premissions for the private key file (.pem), otherwise you can get an error "Bad permissions"

```
sudo chmod 0400 <private-key-name>.pem

```

•	Connect to the instance by running

```
ssh -i <private-key-name>.pem ubuntu@<Public-IP-address>
```
<img width="500" alt="image" src="https://user-images.githubusercontent.com/38444929/218220656-481573ce-5f79-4f07-85f6-8d799fc38ecc.png">

Answer yes to carry on

<img width="454" alt="image" src="https://user-images.githubusercontent.com/38444929/218220802-f0b934d7-5a71-4204-a7a5-3484c9533cfc.png">

Congratulations! You have just created your very first Linux Server in the Cloud and our set up looks like this now: (You are the client)

<img width="454" alt="image" src="https://user-images.githubusercontent.com/38444929/218220899-ad818a3e-949d-4153-87c8-059e05b374a8.png">








