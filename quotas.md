---

copyright:
  years: 2018, 2020
lastupdated: "2020-02-05"

keywords: quotas, vpc, resources, limits

subcollection: vpc


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:download: .download}

# Quotas
{: #quotas}

This document covers quotas for {{site.data.keyword.vpc_full}} and the resources available within it. 
{:shortdesc}

To increase a quota for a particular resource, [contact support](/docs/get-support?topic=get-support-getting-customer-support). 
{:note}

## VPCs
{: #vpc-quotas}

|   Resource     | Quota |
| ------- | ------ |
| Virtual private clouds | 5 per region|    
| Subnets | 15 per VPC |  
| Address prefixes | 15 per VPC |  
{: caption="Table 1. Quotas for the VPC service" caption-side="top"}

## Virtual server instances
{: #vsi-quotas}

|   Resource     | Quota | 
| ------- | ------ | 
| vCPU |  200 per region  |   
| RAM | 800 GB per region |   
| Network interfaces | 5 per instance |   
| Floating IP addresses | 5 per zone |   
| SSH keys | 200 per account |   
| GPUs (POWER only) | 16 |   
{: caption="Table 2. Quotas for virtual server instances" caption-side="top"}


## Security groups
{: #security-group-quotas}

|Resource|Quota| 
|--------|-----| 
|Security groups|25 per VPC|  
|Rules|25 per security group|   
|Remote rules|5 per security group|  
|Network interfaces|5 per security group|    
{: caption="Table 3. Quotas for security groups" caption-side="top"}

## Access control lists
{: #acl-quotas}

|Resource|Quota|
|--------|-----| 
|ACLs| 25 per VPC |  
|Ingress rules|25 per ACL |  
|Egress rules |25 per ACL |  
{: caption="Table 4. Quotas for access control lists" caption-side="top"}

## Block storage volumes
{: #block-storage-quotas}

|Resource|Quota| 
|--------|-----| 
| Boot and secondary volumes | 750 total volumes per account in a region |  
{: caption="Table 5. Quotas for block storage volumes" caption-side="top"}

## VPNs
{: #vpn-quotas}

|Resource|Quota| 
|--------|-----| 
| VPN gateways| 9 per region, 3 per zone |  
| VPN connections | 10 per VPN gateway |  
| IKE policies | 20 per region |  
| IPSec policies | 20 per region |  
| Peer subnets | 50 across all connections of a VPN gateway, 15 per indvidual VPN connection |  
| Local subnets | 50 across all connections of a VPN gateway, 15 per indvidual VPN connection |  
{: caption="Table 6. Quotas for the VPN service" caption-side="top"}

## Load balancers
{: #load-balancer-quotas}


|Resource|Quota| 
|--------|-----|
| Load balancers | 20 per account |  
| Listeners | 10 per load balancer |  
| Pools | 10 per load balancer |  
| Members | 50 per pool | 
{: caption="Table 7. Quotas for load balancers" caption-side="top"}

