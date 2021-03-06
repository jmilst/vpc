---

copyright:
  years: 2018, 2020
lastupdated: "2020-02-05"

keywords: vpc, limitations, restrictions

subcollection: vpc


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}


# Limitations and restrictions
{: #limitations}

Limitations might change as capabilities are added, so feel free to check back from time to time.
{:shortdesc}

## Limits
The following table displays current VPC resource limits. Unlike quotas, these limits can't be adjusted. For information about quotas, see [Quotas](/docs/vpc?topic=vpc-quotas).

|Resource|Limit| 
|--------|-----|
| VPCs with classic access | 1 per region|
| Public Gateways | 1 per zone per VPC |
| Secondary volumes per instance, attached when creating an instance |  4 secondary volumes |
| Secondary volumes per instance, for existing instances with fewer than 4 cores | 4 secondary volumes |
| Secondary volumes per instance, for existing instances with 4 cores or more | Up to 12 secondary volumes |
{: caption="Table 1. Limits for VPC resources" caption-side="top"}

## General restrictions
{: #general-restrictions}

The following features are not supported, including all properties associated with these features:
* Shares

* The following concepts are not supported:
  * IPV6
  * Multiple IP addresses on the same network interface

* Virtual server instance name change: If you update the name of a virtual server, the name change may not appear consistently in different areas of the {{site.data.keyword.cloud}} console. For example, the virtual server name change might not be reflected in the {{site.data.keyword.cloud_notm}} console, or on the billing invoice, yet it appears correctly in the user's list of running instances.

* POWER-based instances are not supported in the Washington DC region.

## Virtual private cloud restrictions
{: #virtual-private-cloud-restrictions}

* An {{site.data.keyword.vpc_short}} cannot be peered with other VPCs. While it is possible to connect VPCs with either VPN Gateways or Floating IPs, there is no automatic route advertisement between the two VPCs. Static routes must be used in each VPC to enable layer 3 connectivity between the two VPCs. For more information about how you can achieve VPC-to-VPC connectivity, see [API example: Connecting two VPCs using VPN](/docs/vpc?topic=vpc-using-vpn#vpn-example).

## Network restrictions
{: #network-restrictions}

* Multi-zone regions: 
  * A security group can be configured in a single zone only. 
  * A security group can’t reference another security group in a different zone in the same region.

* Bring your own subnet:
  * Address prefixes must be within one of the "private" address ranges defined in RFC1918.
  * Address prefixes can't be configured in the IBM Cloud console.

* Multiple Virtual Network Interface Controllers: Only one Virtual Network Interface Controller is allowed for each virtual server instance. Currently, only the primary Virtual Network Interface Controller (VNIC) Ethernet 0 (eth0) works for a virtual server.

* VPN: A VPN gateway serves only subnets that are in the zone in which the VPN is created. For more information, see [Using VPN](/docs/vpc?topic=vpc-using-vpn#vpn-limitations).

## Compute restrictions
{: #compute-restrictions}

* The following images are not supported on the POWER architecture:
  * Red Hat Enterprise Linux 
  * Windows
* Every x86-based profile has a network performance value of 2 Gbps per vCPU, with a cap of 80 Gbps.
* Every POWER-based profile has a network performance value of 3 Gbps per vCPU, with a cap of 100 Gbps.
* Each x86-based network interface has a network performance cap of 16 Gbps. <!-- You might need to attach multiple network interfaces to your virtual server instance to optimize network performance. -->
* Each POWER-based network interface has a network performance cap of 25 Gbps.
* Start/Stop actions are not registered under virtual server instance activity in the UI.
* Activity Tracker logs (request logs and resource lifecycle event logs) are not available.
* Updating the profile of a created instance is not supported.
* Live migration is not supported.

## Storage restrictions
{: #storage-restrictions}

* Customer-managed encryption for secondary volumes is not supported.

## API considerations
{: #api-considerations}

* For API limitations and considerations, see [API application migration considerations](/docs/vpc?topic=vpc-api-integration-migration). 

