
## Network ACL

Is stateless




## Route propagation

Allows a virtual private gateway to automatically propagate routes to the route tables. This means that you don't need to manually enter VPN routes to your route tables. 

It needs to enabled.

## Misc

* There is no route connecting your VPC back to the on premise data center.
* AD connector cannot change password from AWS SSO
* Direct connect need redundent connection for HA
* VPC advertise IP prefixes not VGW
* BGP ASN
* VGW can setup VPN from different region
* Security groups blick traffic by default
* NAT gateway in public subnet
* PrivateLink (VPC endpoints) is to provide access to specific resource to multi VPCs, while VPC peering enable all resource to be accessiable across VPCs https://docs.aws.amazon.com/vpc/latest/userguide/vpc-endpoints.html
* Ephemeral ports has to be allows in SG and NACL for ssh to work
* S3 proxy is used to access S3 from outside VPC and not go through internet
* ENI's MAC address is fixed
* Once a VPC is set to Dedicated hosting, it can be changed back to default hosting via the CLI, SDK or API. Note that this will not change hosting settings for existing instances, only future ones. Existing instances can be changed via CLI, SDK or API but need to be in a stopped state to do so
* VPC Flow Logs can be created at the VPC, subnet, and network interface levels.
* The purpose of an "Egress-Only Internet Gateway" is to allow IPv6 based traffic within a VPC to access the Internet, whilst denying any Internet based resources the possibility of initiating a connection back into the VPC.



## VPC pearing
* VPC peering doesn't have to be same region
* Transitive routing is not supported, e.g. using another VPC's NAT gateway is not supported

## Direct Connection (DX)
* Public virtual interface, private virtual interface
* VPN has to use public vertual interface
* It is defined as part of the AWS VPN configuration process. Direct Connect could be a carrier, but is not a VPN its self.

## VPN
* Each VPN tunnel has two endpoints
* ECMP (Equal Cost Multi Path) can be used to carry trffic on both VPN endpoints.
* DX + VPN = hige performance + secure IPSEC
* Hardware VPN is lower cost than software VPN
* DNS Hostname should be enabled so EC2s lauched in the VPC has publis DNS name.
* Secondary CIDR range can be added to VPC, route table will automatedly updated to allow this CIDR communicate internally within VPC
* There are a number of ways to set up a VPN. AWS have a standard solution that makes use of a VPC with; a private subnet, Hardware VPN Access, a VPG, and an on-premise Customer Gateway.

## NAT
* NAT gateway should be placed in publish subnet, it can be in private subnet, but internect connection won't work
* You need to make sure routing table is route traffic correctly to NAT
* NAT cannot work with IPv6, use Egress-only Internet Gateway instead

## Subnet
* Each subnet reserves first 4 and last 1 IP



https://docs.aws.amazon.com/whitepapers/latest/aws-vpc-connectivity-options/welcome.html