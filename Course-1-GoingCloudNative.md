# module 1 :
## What is a region in AWS?

Regions are sperate locations around the world where there are several clusters of data centers.

Diffrent regions have diffrent prices, latencies, transer speeds and diffrent updates of applications.

## What is an availability Zone in an AWS region?

it's a cluster of data centers.

Availability zones are connected by high-speed fiber networks; so no difference with speed between different zones.

you can put your application on different availability zones but will be treated as one, to provide high-availability and backup.

---

 #module 2 :
## Compute
compute are services used to run your applications on.
### LightSail:
It's a simple service that has a bunch of pre-built services for quick setup.

### Amazon EC2:
It's a resizable compute service on the cloud for application to run on.
It's a virtual server called `EC2 instance`.
---
# module 3:
## VPC:
`"Virtual private Cloud"` used to isolate your application from other applications on AWS.

It's a frame where your application lives in which you control the permission that goes in and out.

you need to setup {subnets, routing tables, internet Gateways **IGW** }

you can make your VPC available across multiple availability zones which will bet treated as one; in this way you can run your application on multiple EC2 on different availability zones and connect them to Elastic Load Balancing **ELB** to help distribute traffic on different availability zones, if one availability zone became unavailable your application will still run.

## Storage:

storage in AWS has 2 types :

- **Object-level** :

	- Data saved as a big object

	- changing data changes the entire file

- **Block level**: changing data changes part of the file or the data

	- Data saved as blocks

	- Changin data changes the related block only

### EBS:
**Elastic Block Storage** connects to one EC2 only.
### S3:
**Simple Storage Service** uses buckets to hold objects of data
bucket's name is unique like DNS and you access it through HTTP or HTTPs
### EFS:
**Elastic File System** used to link multiple EC2 instances and other services to one EBS.