# 12 Steps

## Recommendation
You are recommended to use Firefox browser because you could easily copy and paste.

##  Step 1
Go to AWS Event Engine at https://dashboard.eventengine.run/login 

![Event Engine](eventengine.png "Event Engine")

Please get the Event Hash from your workshop instructor.

## Step 2

Sign in (to AWS EKS environment) via Email OTP

![Sign In Option](signoption.png "Sign In Option")

## Step 3

Select AWS Console
![Credentials](credentials.png "Credentials")

## Step 4

Remeber to only use "ap-southeast-1" as your region
![EKS Region](eks-region.png "EKS Region")

## Step 5

Select EC2 from Management Console and select Instances (running). You should see a EC2 instance called SplunkWorkshop-box
![EC2 Splunk](ec2-splunk.png "EC2 Splunk")

## Step 6

Now select SplunkWorkshop instance and select connect
![Connect EC2](connect-ec2.png "Connect EC2")

## Step 7

Remeber to only use "ap-southeast-1" as your region
![EKS Region](eks-region.png "EKS Region")

## Step 8

Verify EKS cluster¶
Select EC2 Instance Connect tab and click connect. This will open an SSH session to the EC2 instance. Once the instance is opened check the running EKS cluster. You should see a cluster named
```bash
eksctl get cluster --region ap-southeast-1
```

## Step 9

Update Kubectl
```bash
aws eks --region ap-southeast-1 update-kubeconfig --name eksworkshop-eksctl
```

## Step 10

Test Kubectl
```bash
kubectl get nodes
```
If we see our 2 nodes, we know we have authenticated correctly

## Step 11

Install Helm 3
```bash
curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3
```

---

```bash
chmod 700 get_helm.sh
./get_helm.sh
```

## Step 12

```bash
wget https://github.com/splunk/imt-workshop/archive/refs/heads/master.zip
```

---

```bash
unzip master.zip
```

---

```bash
mv imt-workshop-master workshop
```

## Congratulations
You have setup your AWS EKS cluster with the resources required for Splunk O11y workshop. Let us get started with the workshop at https://signalfx.github.io/observability-workshop/ 