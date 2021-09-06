
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

**Compute Optimized**
