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
![1](https://github.com/lexbytez/AWS-S3-Cross-Region-Replication/assets/128375535/2ff7d2d6-ba49-4c88-b8d0-234d97ef8704)
![2](https://github.com/lexbytez/AWS-S3-Cross-Region-Replication/assets/128375535/73342520-ff82-483c-b95e-2576b5f2bd6c)
![3](https://github.com/lexbytez/AWS-S3-Cross-Region-Replication/assets/128375535/3ddedba0-8747-4dd4-8df8-b574b453d1fc)
Next

Head into the main bucket and upload our file(chak-test.txt)

we wait few minutes and check the destination bucket to make sure same file has been replicated into it
![1](https://github.com/lexbytez/AWS-S3-Cross-Region-Replication/assets/128375535/b7adc11e-8683-4454-96e4-659aaf6db055)
![2](https://github.com/lexbytez/AWS-S3-Cross-Region-Replication/assets/128375535/5233e301-9588-42f2-b5ec-33f4b3d2a931)
