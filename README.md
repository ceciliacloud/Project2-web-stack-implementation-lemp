# web-stack-implementation-lemp

Hello and welcome to the Web stack **implementation using LEMP stack** project. In this project, we will be using the **LEMP** stack! You may be wondering, _what is LEMP_?

- `L` stands for **Linux** Operating system
- `E` stands for **Nginx** web server (pronounced as engine-x, hence the `E` in the acronym)
- `M` stands for **MySQL** database 
- `P` stands for **PHP** scripting language.

**Linux** is an operating system that manages the underlying hardware on your PC. It is an open-source software that is used worldwide. It is flexible and easy to configure.

**Nginx** is ...

**MySQL** is ...

**PHP** is ...


Let's get started! 

# LINUX
## Setting up your virtual environment on AWS

In order to complete this project, it is necessary to set up a virtual environment using AWS. In case you are not familiar with AWS, don't worry! It is user-friendly. I will guide you along the way!

Amazon Web Services (AWS) is the leading Cloud Service Provider in the world. AWS offers a wide variety of databases and services for different types of applications. This allows users to choose the right tool for the job while receiving the best cost and performance.

Fortunately, AWS offers a Free Tier for newly registered account users. This enables users to try out some AWS services free of charge within certain usage limits. For this project, we will utilize the EC2 (Elastic Compute Cloud) service, which is covered by the Free Tier!

Let's begin by setting up a virtual environment. First, create a free account on AWS. Once you have created your account, [login](https://aws.amazon.com/) as the IAM user, using your credentials.

![](./images/login.png)

Once you have signed-in to your AWS account, navigate to the top-right of the screen and select your preferred region (this should be the closest region to your physical location).
￼
![](./images/selectregion.png)

After you have selected your region, navigate to the search bar and type in EC2. Select the EC2 service that appears.

![](./images/selectec2.png)

Next, click on "Launch Instances".
￼
![](./images/launchinstance.png)

Now we are going to configure our EC2 instance! Select the Ubuntu Server 20.04 LTS (HVM) as the Amazon Machine Image (AMI).

![](./images/AMI.png)
￼
Then, select "t2.micro" as the instance type. Once you have made the selection, click "Review and Launch".

![](./images/instancetype.png)

When you reach the "Review and Launch" page, click the "Launch" at the bottom-right of the page.

![](./images/XXX.png)

Next, you should see a window appear. Create a key pair and then select "Download". Don't lose it! You will need this file in order to connect into your server from your local PC. After you downloaded the key pair, check the box for the acknowledgement, and then click on "Launch Instances".

![](./images/keypair.png)

Great job! You've launched an EC2 instance! You can view your new instance by clicking the "View Instances" button at the bottom-right of your screen. 
_Note: it may take a moment to initialize, so please be patient_!

![](./images/XXX.png)



# Connecting to your EC2 from your local PC

**PLEASE NOTE**
**Anchor tags < >** will be used to indicate contents what must be replaced with your unique values. For example, if you have a file named "keypair123.pem" you must enter this information within the corresponding anchor tag: **< private-key-name >**

Now let's connect to our instance!

Begin by opening Terminal. Once you have opened Terminal, use the `cd` command to change into the directory that your key pair is located. This is usually the `~/Downloads` directory. If you are having difficulty finding it, you can use the `ls` command to list the contents of your current directory.

Once you have located the key pair, use the command below to activate the key pair file (.pem). This command will also change permissions (otherwise you may get the error “Bad Permissions”):

`$ sudo chmod 0400 <private-key-name>.pem`

When prompted, type the password for your local PC and press Enter on your keyboard.

Next, go back to the AWS console for a moment, and navigate to your running EC2 instance. Copy the Public IP address, as shown in the image below:

![](./images/XXX.png)

Now that you've copied the Public IP address, go back to Terminal. Connect to the EC2 instance by using the command below:

`ssh -i <Your-private-key.pem> ubuntu@<EC2-Public-IP-address>`

Next, you will be asked if you want to continue connecting. Type `Yes` and press Enter on your keyboard.

![](./images/XXX.png)

To verify that you are connected, you should see your IP address on the top-right of the screen. Nice job! You have successfully connected to your Linux server in the Cloud environment.

![](./images/XXX.png)


# Nginx Web Server
## Installing Nginx on your virtual environment






# MySQL
## Installing MySQL on your virtual environment






# PHP
## Installing PHP on your virtual environment






# Configuring Nginx to use the PHP Processor







# Testing PHP with Nginx






# Retrieving data from MySQL database with PHP


