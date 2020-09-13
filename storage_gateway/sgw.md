https://aws.amazon.com/storagegateway/faqs/

## What is AWS Storage Gateway?

A hybrid cloud storage service that gives you on-premises access to virtually unlimited cloud storage.

## 3 types of storage interfaces

The File Gateway enables you to store and retrieve objects in Amazon S3 using file protocols such as Network File System (NFS) and Server Message Block (SMB). Objects written through File Gateway can be directly accessed in S3.

The Volume Gateway provides block storage to your on-premises applications using iSCSI connectivity. Data on the volumes is stored in Amazon S3 and you can take point in time copies of volumes which are stored in AWS as Amazon EBS snapshots. You can also take copies of volumes and manage their retention using AWS Backup. You can restore EBS snapshots to a Volume Gateway volume or an EBS volume.

The Tape Gateway provides your backup application with an iSCSI virtual tape library (VTL) interface, consisting of a virtual media changer, virtual tape drives, and virtual tapes. Virtual tapes are stored in Amazon S3 and can be archived to Amazon S3 Glacier or Amazon S3 Glacier Deep Archive.

## Storage Gateway appliance

On-premises, you can deploy a virtual machine containing the Storage Gateway software on VMware ESXi, Microsoft Hyper-V, or Linux KVM, or you can deploy Storage Gateway as a hardware appliance. You can also deploy the Storage Gateway VM in VMware Cloud on AWS, or as an AMI in Amazon EC2.

## Volumn Gateway

### Cached mode
your primary data is written to S3, while retaining your frequently accessed data locally in a cache for low-latency access.

### Stored mode
Your primary data is stored locally and your entire dataset is available for low-latency access while asynchronously backed up to AWS.


## Misc
Gateway-Cached and File Gateway volumes retain a copy of frequently accessed data subsets locally. Cached volumes offer a substantial cost savings on primary storage and minimize the need to scale your storage on-premises. Note that AWS recently changed the naming. You should know both forms for the exam.