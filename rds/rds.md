* Parameter group
* Auto scaling
* Automated snapshot are automatically deleted after max 35 days
* Manual snapshot can be retained indefinitely, be default 365 days if created from console
* RDS MySql can shard the date across multi db instances
* Automated backup is a storage volume snapshot of entire DB instance every 24 hours. It also capture trans log every 5 mins and save in S3
* Multi-AZ ensures there are instances running in multi AZ for HA
* SQS FIFO queue can be used to queue writes so write operations are not lost, but it is not for performance
* When MYSQL in question, replace it with Aurora always is a correct choice