# AWS-S3-Cross-Region-Replication
Project Description

Your organization want you to make a real-time copy of the object in bucket A into bucket B and they need you to make sure that this bucket are not in the same region. In order to help you out your team lead requires you to use S3 replication to solve this issue. The reason behind this is to have something to depend on in case the object in bucket A get deleted, having bucket B serve as backup and also making bucket B serve as secondary bucket in the incident of failover. This are just few of the reason your organization requires you to use S3 replication in resolving this issue.

Steps

Head to Amazon AWS Console and go to S3

When in S3 create two buckets, in two different regions, the main one and the one to be replicated

While setting up make sure to Enable Bucket Versioning
![1](https://github.com/lexbytez/AWS-S3-Cross-Region-Replication/assets/128375535/00fc530a-4724-4764-8f9b-29ef5adb556a)
![2](https://github.com/lexbytez/AWS-S3-Cross-Region-Replication/assets/128375535/719fc440-a587-4699-9dbc-b65ca4fd0ac9)
![3](https://github.com/lexbytez/AWS-S3-Cross-Region-Replication/assets/128375535/3ea59d2a-9cab-4491-a95d-daebc5b90ce9)
![4](https://github.com/lexbytez/AWS-S3-Cross-Region-Replication/assets/128375535/aa63e976-36fe-411e-817c-aec117ba4502)
Now we have our two buckets created namely main-chak and replic-chak

We head into management settings under main-chak and create a replication rule

We choose the destination bucket

We choose IAM roles to be used(either create a new one or use existing role)
Save the settings
![1](https://github.com/lexbytez/AWS-S3-Cross-Region-Replication/assets/128375535/2d39a4c5-c9ea-4606-a959-3604cf3c51af)
![2](https://github.com/lexbytez/AWS-S3-Cross-Region-Replication/assets/128375535/9e2e95fa-21db-4942-a0f2-43ed4a77a701)
![3](https://github.com/lexbytez/AWS-S3-Cross-Region-Replication/assets/128375535/fb9ca4c5-0b4b-4578-82e2-44325cf0ea4c)
![4](https://github.com/lexbytez/AWS-S3-Cross-Region-Replication/assets/128375535/ce2dc65b-9048-416d-aba8-c1dc16e82c51)

