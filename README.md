# AWS-VPC-Peering-project
AWS project showing VPC peering between two VPCs with public/private subnet.

This project desmosntrates how to connect two AWS VPCs using VPC Peering ,NAT Gateways, Route Tables, EC2 ,Internet Gateway.
It includes both Public and Private subnet in each VPC.

#Artitecture Overview

*VPC 1 (MY test VPC) 

CIDR:10.0.0.0/18
- public subnet:10.0.0.0/22
- private subnet:10.0.4.0/22
- NAT Gateway and Internet Gateway attached

  *VPC 2 (My prod VPC)
  
  CIDR:10.1.0.0/16
  - public subnet:10.1.0.0./20
  - private subnet:10.1.16.0/20
  - NAT gateway and Internet gateway attached
 
#setup steps

1. Create two VPCs with **non-overlapping CIDR blocks**
2. Create two VPCs with **non-overlapping CIDR blocks**
3. Attach Internet Gateways to public subnets
4. Create and attach NAT Gateways for private subnets
5. Create a *VPC Peering connection* between both VPCs
6. Update route tables to route traffic between VPCs
7. Launch EC2 instances and test using `ping`  

#Testing

From your EC2 in one VPC:
ping(Ip address of one VPC tp other VPC) 

Here is the diagram also,

