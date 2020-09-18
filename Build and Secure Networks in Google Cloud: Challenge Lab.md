**Task 1:**


gcloud compute firewall-rules delete open-access


**Task 2:**


gcloud compute instances start bastion


**Task 3:**


gcloud compute firewall-rules create ssh-ingress --allow=3Dtcp:22 --source-=
ranges 35.235.240.0/20 --target-tags ssh-ingress --network acme-vpc



gcloud compute instances add-tags bastion --tags=3Dssh-ingress --zone=3Dus-=
central1-b


**Task 4:**


gcloud compute firewall-rules create http-ingress --allow=3Dtcp:80 --source=
-ranges 0.0.0.0/0 --target-tags http-ingress --network acme-vpc



gcloud compute instances add-tags juice-shop --tags=3Dhttp-ingress --zone=
=3Dus-central1-b


**Task 5:**


gcloud compute firewall-rules create internal-ssh-ingress --allow=3Dtcp:22 =
--source-ranges 192.168.10.0/24 --target-tags internal-ssh-ingress --networ=
k acme-vpc



gcloud compute instances add-tags juice-shop --tags=3Dinternal-ssh-ingress =
--zone=3Dus-central1-b




**Task 6:**



1.

**In the Compute Engine instances page, click the SSH button for the bastio=
n host. Once connected, SSH to** **juice-shop****.**

ssh [IP address of juice-shop]

![](https://lh6.googleusercontent.com/JvqJWBWd1kDjuGXhRTQi2MiLd3ia1jv78lNd=
7bQIuXFQGCFgBM4HJBXQ8HEBqVDocPvbaH88RmBVUbEgDQkMlRz7Xy9HZezIoaz82lzM3zcWPl2=
MgIUspeJAUU6LZgq3dql8_hUE) ![](https://lh5.googleusercontent.com/Zz1Hq-9AMM=
8U6B6JOHsqvcLCqZY5J-lk0PW5v_agqThtjGpzByfMVb2Wjdad1AuA-Mo7bLc1RJbs8Wfrdj-wj=
nj6uQ0PqDgMm7baGzlPLfZx4Lj2cjOvbXOzfwIuKsUfuPxi0BII)
