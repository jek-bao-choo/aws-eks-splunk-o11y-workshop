# 17 Steps

##  Step 1
Go to AWS Event Engine at https://dashboard.eventengine.run/login 

![Event Engine](eventengine.png "Event Engine")

Please get the Event Hash from your workshop instructor.

```bash
9bc4-1064967d54-cd
```

## Step 2

Sign in (to AWS EKS environment) via Email OTP

![Sign In Option](sign-in-option.png "Sign In Option")

## Step 3

Select AWS Console
![Credentials](credentials.png "Credentials")

## Step 4

Remember to only use "us-west-2" as your region
![EKS Region](eks-region.png "EKS Region")

## Step 5

Select EC2 from Management Console and select Instances (running). You should see a EC2 instance called SplunkWorkshop-box
![EC2 Splunk](ec2-splunk.png "EC2 Splunk")

## Step 6

Now select SplunkWorkshop instance and select connect
![Connect EC2](connect-ec2.png "Connect EC2")

## Step 7

Click Connect
![EC2 Instance Connect](ec2-instance-connect.png "EC2 Instance Connect")

## Step 8

Verify that you see the terminal.

![Browser Terminal](browser-terminal.png "Browser Terminal")

## Step 9

Verify EKS cluster. Select EC2 Instance Connect tab and click connect. This will open an SSH session to the EC2 instance. Once the instance is opened check the running EKS cluster. You should see a cluster named
```bash
eksctl get cluster --region us-west-2
```

## Step 10

Update Kubectl
```bash
aws eks --region us-west-2 update-kubeconfig --name eksworkshop-eksctl
```

## Step 11

Test Kubectl
```bash
kubectl get nodes
```
If we see our 2 nodes, we know we have authenticated correctly

## Step 12

Install Helm 3
```bash
curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3
```

---

```bash
chmod 700 get_helm.sh
```

---

```bash
./get_helm.sh
```

## Step 13

Get Workshop content from Splunk Observability repo

```bash
wget https://github.com/signalfx/observability-workshop/archive/refs/heads/master.zip
```

---

```bash
unzip master.zip
```

---

```bash
mv observability-workshop-master workshop
```

# ***Congratulations***
You have completed your AWS EKS cluster setup with the resources for Splunk O11y workshop. Let us get started with the workshop by accessing Splunk O11y portal. 

## Step 14

Access your Splunk O11y portal by going to your email account. We have triggered an invite. 

![Email Invite](email-invite.png "email invite")

## Step 15

Once signed in to Splunk O11y portal, expand the side nav. 

![Expand Sidenav](expand-side-nav.png "expand side nav")

## Step 16

Select Settings

![Settings](settings.png "settings")

## Step 17

Select Access Tokens

![Access Token](access-token.png "access token")


Show token 
![Show Token](show-token.png "show token")


# ***Hooray!***
You have achieved a great deal. These are what you have achieved:
- Signed in to AWS EKS
- Downloaded the workshop resources
- Signed in to Splunk Observability 

---

## Next steps
Take a 10 minutes break; you earned it! 

After the break, let us see the value of Splunk Observability with the following hands-on activity
![Splunk Workshop Content](splunk-workshop-content.png "splunk workshop content")

### Get started with the next steps after your break: go to https://signalfx.github.io/observability-workshop/v3.14/otel/k3s/
