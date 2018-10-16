# networktoolbox
This is an exercise to show you how to use different aws network resources. 


You are the Network Engineer of a company

You designed and operate the Data Center Network of this company. 

You have heard that your company started to use AWS while ago and today your boss invited you to a meeting because Cloud engineers need help to interconnect and secure workloads in AWS.

This is your first contact with AWS Networking.


Scenario 1: Patch update
Cloud Engineer: I don’t have access to  internet from private instances. I need to update my OS

Solution: NAT Gateway
  You can use a network address translation (NAT) gateway to enable instances in a private subnet to connect to the internet or other AWS services, but prevent the internet from initiating a connection with those instances. 


Scenario 2: I need access to On-premises resources
Cloud Engineer: The new app requires access to our internal systems. By the way, can we do the same from a VPC at sa-east-1? We just acquired a new company.
  Note: Your company has a Data-Center in Ireland with all IT systems. This is a usual request: Connect Apps from VPC to On-prem resources or migrate workloads from on-prem Data Center to cloud .

Solution: VPN (or Direct Connect we will see that later)
  By default, instances that you launch into an Amazon VPC can't communicate with your own (remote) network. You can enable access to your remote network from your VPC by attaching a virtual private gateway to the VPC, creating a custom route table, updating your security group rules, and creating an AWS managed VPN connection. 
  

Scenario 3: I need talk to another VPC
Cloud Engineer: Net Guy! I need to consume some APIs from a VPC at sa-east-1. Is that possible?

Solution: VPC Peering
  A VPC peering connection is a networking connection between two VPCs that enables you to route traffic between them privately. Instances in either VPC can communicate with each other as if they are within the same network. You can create a VPC peering connection between your own VPCs, with a VPC in another AWS account, or with a VPC in a different AWS Region. 


Scenario 4: IP Overlapping
Cloud Engineer: Net Guy!  Remember that VPC peering? Can you do it again to one of our customers? They are using the same subnet of ours. But, that works right?

Solution: Privatelink


Scenario 5: More bandwidth, less latency
Cloud Engineer: We are planning a lot of new stuff with AWS: Data Backups, server migrations ,new Apps. Can you help us achieve
more  Bandwidth, througput and lower latency with AWS?  ewr

Solution: We can do that with a Direct Connect.  Not only we gonna get these benefits but optimize costs.

Scenario 6: EC2 bandwidth
Cloud Engineer: Why can’t I get more bandwidth between my servers?

Solution: Enhanced Network Adapter



