
# EC2

- EC2 stands for **Elastic Compute Cloud**.
- EC2 intance is a **virtual server ( virtual machine )** which is used for running applications on the Amazon Web Services (AWS).
- It provides **scalable computing capacity**
    -   based on your requirements you can **scale up** or **scale down** the RAM, hard disk, external drive etc.
- **Any number** of EC2 intances(VM,VS) can be created with defined **security, networking and storage.**
    - per region **20 intances** can be created with **2 I/O intance**(more intance can also be possible).
- Billing is done **pay as you use**(per min or per sec).
- Two storage options are present
    - **EBS [ Elastic Block Store ]** (external storage )
    - **Instance Store** (internal storage )
- For AWS **root volume** (where your OS is intalled) we can make use these IS or EBS.
- Pre configured templates are already present **( Amazon Machine Image [AMI])**
![Elastic Compute Cloud](https://user-images.githubusercontent.com/62538952/132107446-27cd7dc0-5484-408a-b71e-fc1e7019e38d.gif)

# Types of EC2

- [**General Purpose**](https://github.com/Venkatesh0610/EC2#General-Purpose)
- [**Compute Optimized**](https://github.com/Venkatesh0610/EC2#Compute-Optimized)
- [**Previous Generation**](https://github.com/Venkatesh0610/EC2#Previous-Generation)
- [**Memory Optimized**](https://github.com/Venkatesh0610/EC2#Memory-Optimized)
- [**Storage Optimized**](https://github.com/Venkatesh0610/EC2#Storage-Optimized)
- [**Accelrated Computing**](https://github.com/Venkatesh0610/EC2#Accelerated-Computing)
- [**High Memory**](https://github.com/Venkatesh0610/EC2#High-Memory)

# General Purpose

When we require a balanced/average compute,memory,networking used fro variety of workload in that case we choose GPI

GPI consists of three Series :

- A (A1)
- M (M4,M5,M5a,M5ad,M5d)
- T (T2,T3,T3a)

**Note:** In GPI the instance size varies from nano,small,medium,large.

**A Series**

When we required scale out(increase the instance anytimw) of our workload
we select A series GPI.

Basically used for :

Small web servers, containerize micro Services,caching fleets (at a time many EC2 can run).

**M Series**

Whenever we have a high workload and the instance has to perform high in that cases we basically use M series GPI.

In M series we have M4,M5,M5a,M5ad,M5d instance.

**M4:**

- It features a custom intel xeon v3 haswell processor
- VCPU : 2 to 40, RAM : 8 to 160 GB, Storage : EBS only

**M5,5a,5ad,5d :**

- when we require balanced compute, memory and networking for our workload,
- VCPU : 2 to 96, RAM : 8 to 384 GB, Storage : EBS & NVMe SDD.

**T Series**

It provides a baseline level of CPU performance with **burst** when it reaches to higher level.

In T series we have T2(**free tier**),T3,T3a instance.

**T2,T3,T3a :**
- VCPU : 2 to 8, RAM : 0.5 to 32 GB, Storage : EBS only

![GPI](https://user-images.githubusercontent.com/62538952/132138324-b100296a-292d-4042-b581-3840e8083dc3.png)

# Compute Optimized

When we need high performance by doing parallel, batch processing in that case we use COI.

Less cost effective as compared to MOI(M Series).

GPI consists of only one Series :

- C Series (C4,C5,C5n).

**C4**

Optimized for compute intensive workload with high performance at a low cost.

VCPU: 2 to 36, RAM: 3.75 to 60 GB, Storage: **EBS Only**, network Bandwidth : 10 Gbps

used at : web servers,video encoding etc.

**C5,C5n**

It is same as C4 but with more effective and upgradable hypervisor( Nitro System ).

VCPU: 2 to 72, RAM: 4 to 196 GB, Storage: **EBS & NVMe**, network Bandwidth : 25 Gbps

used at : web servers,video encoding etc.

- C5 supports maximum of 25 EBS volume.
- It use AWS Nitro System ( Hypervisor ).

![COI](https://user-images.githubusercontent.com/62538952/132389026-6cf79eac-a3c9-4bfe-b109-0672284eb2c1.png)


# Memory Optimize

It is use when we have to deliver fast performamce for that workloads which process large datasets in memory.

Basically in simple terms when we have to process big databases data.

MOI consists of three series:
- R Series(R4,R5,R5a,R5ad,R5d)
- X Series(X1,X1e)
- Z Series(Z1d)

![MOI](https://user-images.githubusercontent.com/62538952/132390618-112da604-8ecf-47f3-8ce4-f64a346587cb.png)

# How to create an EC2 Instance

In this section you will be going to understand how you can create an EC2 instance in AWS.

For creating an EC2 instance we need to follow the below steps:

- [Sign-in to AWS](https://github.com/Venkatesh0610/EC2#Sign-in-to-AWS)
- [Search for EC2 instance](https://github.com/Venkatesh0610/EC2#Search-for-EC2-instance)
- [Create your first EC2 Instance](https://github.com/Venkatesh0610/EC2#Create-your-first-EC2-Instance)

# Sign-in to AWS

In this step you need to sign-in to your AWS root user account.

**Note:** If you didn't yet created the free tier account then create it first and then login.
[**AWS free tier**](https://aws.amazon.com/free/)

Once you are logged in into the AWS account you will be able to see the dashboard as shown below.

![aws dashboard](https://user-images.githubusercontent.com/62538952/132393104-cb858e25-6ec8-449f-81a9-c91b094b2c7d.PNG)

# Search for EC2 instance

Now its time to search for EC2 instance from the search bar and open it.

![image](https://user-images.githubusercontent.com/62538952/132393341-7f318476-5220-45a7-9fbe-86d2bb4f4c11.png)

And the EC2 dashboard is as shown below:

![image](https://user-images.githubusercontent.com/62538952/132393761-41f3e860-99d8-4ead-99e1-7ee805e8615a.png)

# Create your first EC2 Instance

Now for creating an EC2 instance in AWS you need to click on **Instances** option and then for launching your first instance click on **Launch instances** button which is present in the top right corner.

![image](https://user-images.githubusercontent.com/62538952/132562307-95e34faa-7ec9-4542-a709-7fc2d58c3975.png)

After click on Launch instances it will redirect to a new page where we need to select the type of the instance which we need to create.

We will be going to create a LINUX instance which is a free eligible instance in AWS, for selecting the LINUX instace you simply needs to click on **Select** button.

![image](https://user-images.githubusercontent.com/62538952/132563326-04f94cff-2944-4fde-8c06-d96dc534ff78.png)

Now from here we need to go with the default configured instance setting by simply clicking on **Next. Configure Instance Details**

Here we will be going to select a **t2 micro** General Purpose Instace which is a free tier eligible instance in AWS and we already discussed about [General Purpose](https://github.com/Venkatesh0610/EC2#General-Purpose) and its series in details above in this present repository.

![image](https://user-images.githubusercontent.com/62538952/132564419-4f7eff8f-63cd-4564-94a1-4ff78ce6aa38.png)

In the next step we have an user data script section under **Advance Details** by using which also we can install the required depedencies for our instance(Which we will be going to see later in this repository).

![image](https://user-images.githubusercontent.com/62538952/132566457-ab929811-3e4e-4d0f-8d89-0c66fcf419ec.png)

Under Add Storage section go with the default storage and click on **Add Tags**


![image](https://user-images.githubusercontent.com/62538952/132566935-4c5a7842-54af-481c-889e-03b602fcc1b5.png)

Then simply click on Add another tag option and give any name in key section and click on next

![image](https://user-images.githubusercontent.com/62538952/132567586-6101344a-957f-4bf9-8ce8-11c74e980ca3.png)

Now its time to review all the default setting before launching the instance, here in this step simply click on **Review and Launch** button.


![image](https://user-images.githubusercontent.com/62538952/132567841-ead19ba8-ef4d-4233-a0b0-5167835096c4.png)

Finally now in above step all the settings will be visible for you and once you click on **Launch** button you LIINUX EC2 instance will be created, but before that make sure you create a new key pair with any name and **don't forget to download the key pair**, then finally click on Launch Instances.

![image](https://user-images.githubusercontent.com/62538952/132568114-b389f2c5-50c4-4617-8bab-47c93f40f91e.png)

![image](https://user-images.githubusercontent.com/62538952/132569463-069f2b92-f1e3-4932-b09c-ad62a746b348.png)

Once the instance is created you will able to see something as shown below, from here simply click on the **id or launch instances**

![image](https://user-images.githubusercontent.com/62538952/132569379-9fc2eb2d-ab5d-48cd-86ef-2436a495f9c5.png)

After few minutes the instance which you created will be in running state as shown below

![image](https://user-images.githubusercontent.com/62538952/132569831-4204f3ff-e7a2-45d5-83cb-1d982198b033.png)

Steps to be followed:

![20210909_004905](https://user-images.githubusercontent.com/62538952/132571843-cc71554c-a24c-48eb-a894-d3ab97656ca4.gif)


# How to connect our instance using putty

As we already done with creating our EC2 instance in AWS now here we will be connecting our server using putty.

So before moving forward we need to install the below softwares:

- [Putty](https://www.putty.org/)
- [Puttygen](https://www.puttygen.com/)

**Note :** This steps is only for windows user.

Follow the below steps to setup the server.

- Open Puttygen and load the keypair
- Open Putty and connect the server.

**Open Puttygen and load the key pair**

From the search bar open the Puttygen and load the key pair which we already downloaded while creating the LINUX instance and the save the private key for further use.

**Open Putty and connect the server**

Now open putty from search bar and click on **Auth** which will be present under **SHH**
and then browse the private key which we saved in the previous step.

And then click on **Session** and provide the IP address which will be avialable under the instance in AWS,once the adress is added a terminal will open where you need to write **ec2-user** which will connect your server.

Follow the below reference for better understanding the steps.

![20210909_233031](https://user-images.githubusercontent.com/62538952/132738681-62d0d983-cb41-481b-95e6-7e13560370f9.gif)


# How to connect with windows server
