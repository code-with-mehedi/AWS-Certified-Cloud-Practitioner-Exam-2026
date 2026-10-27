# Practice questions: 10. Networking & Content Delivery

[Study guide: 10. Networking & Content Delivery](../README.md#10--networking--content-delivery) · [All topics](README.md) · [Next: 11. Security, Identity & Compliance](11-security-identity-compliance.md)

> [!NOTE]
> Read the question and decide on your answer, then click an option to see whether it is right or wrong and why. A round marker (◯) means pick one answer. A square marker (☐) means pick every answer the question asks for, so click each option you think is correct.

### Question 1

A company wants to explicitly block traffic from one malicious IP address at the subnet level. Which feature should it use?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Security group</summary>

❌ **Incorrect.** Security groups support allow rules only, so they cannot explicitly deny an IP address.

</details>

<details><summary>◯ <b>B.</b> AWS Shield Standard</summary>

❌ **Incorrect.** Shield Standard provides automatic DDoS protection but cannot be used to block one IP address at the subnet.

</details>

<details><summary>◯ <b>C.</b> IAM policy</summary>

❌ **Incorrect.** IAM policies control permissions for AWS API actions, and network traffic is outside their scope.

</details>

<details><summary>◯ <b>D.</b> Network ACL (NACL)</summary>

✅ **Correct.** NACLs work at the subnet level and support explicit deny rules, so they can block a specific IP range.

</details>

Study: [10.2 Security Groups vs. Network ACLs (NACLs)](../README.md#102-security-groups-vs-network-acls-nacls)

### Question 2

A company serves images and videos from an S3 bucket to users around the world and wants to cache the content close to them to reduce latency. Which service should it use?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> AWS Global Accelerator</summary>

❌ **Incorrect.** Global Accelerator improves routing over the AWS global network with static IP addresses, but it does not cache content.

</details>

<details><summary>◯ <b>B.</b> Amazon CloudFront</summary>

✅ **Correct.** CloudFront is a content delivery network that caches content at edge locations close to users.

</details>

<details><summary>◯ <b>C.</b> Amazon Route 53</summary>

❌ **Incorrect.** Route 53 is a DNS service that routes users to endpoints without caching any content.

</details>

<details><summary>◯ <b>D.</b> AWS Direct Connect</summary>

❌ **Incorrect.** Direct Connect is a private link between a data center and AWS and cannot act as a global content cache.

</details>

Study: [10.5 Content Delivery & DNS: CloudFront & Route 53](../README.md#105-content-delivery--dns-cloudfront--route-53)

### Question 3

Instances in a private subnet must download operating system patches from the internet but must not be reachable from the internet. What should the company use?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> A NAT gateway in a public subnet</summary>

✅ **Correct.** A NAT gateway lets private instances start outbound connections while blocking unsolicited inbound traffic from the internet.

</details>

<details><summary>◯ <b>B.</b> An internet gateway route in the private subnet</summary>

❌ **Incorrect.** Adding a route to an internet gateway would make the subnet public and reachable from the internet.

</details>

<details><summary>◯ <b>C.</b> A VPC peering connection</summary>

❌ **Incorrect.** Peering connects two VPCs privately and gives private instances no outbound internet access.

</details>

<details><summary>◯ <b>D.</b> AWS Direct Connect</summary>

❌ **Incorrect.** Direct Connect links an on-premises network to AWS. It is not used for outbound internet access from a private subnet.

</details>

Study: [10.1 Amazon Virtual Private Cloud (VPC), Subnets & Gateways](../README.md#101-amazon-virtual-private-cloud-vpc-subnets--gateways)

### Question 4

Which TWO statements about connecting VPCs and networks are correct?

*☐ Choose TWO.*

<details><summary>☐ <b>A.</b> VPC peering is non-transitive</summary>

✅ **Correct.** If VPC A peers with VPC B and VPC B peers with VPC C, VPC A still cannot reach VPC C through VPC B.

</details>

<details><summary>☐ <b>B.</b> AWS Transit Gateway acts as a central hub that connects many VPCs and on-premises networks</summary>

✅ **Correct.** It supports transitive routing and simplifies large networks.

</details>

<details><summary>☐ <b>C.</b> VPC peering supports transitive routing</summary>

❌ **Incorrect.** Peering is non-transitive, so each pair of VPCs needs its own connection.

</details>

<details><summary>☐ <b>D.</b> AWS Direct Connect traffic travels over the public internet</summary>

❌ **Incorrect.** Direct Connect is a dedicated private connection that bypasses the public internet.

</details>

<details><summary>☐ <b>E.</b> A NAT gateway lets hosts on the internet start connections to private instances</summary>

❌ **Incorrect.** A NAT gateway allows only outbound connections initiated from the private subnet.

</details>

Study: [10.3 Hybrid Connectivity: Direct Connect, VPN & Transit Gateway](../README.md#103-hybrid-connectivity-direct-connect-vpn--transit-gateway)

### Question 5

A company needs a dedicated private physical connection from its data center to AWS that does not travel over the public internet. Which service should it use?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> AWS Site-to-Site VPN</summary>

❌ **Incorrect.** A VPN creates encrypted tunnels over the public internet, so it is not a dedicated physical link.

</details>

<details><summary>◯ <b>B.</b> AWS Direct Connect</summary>

✅ **Correct.** Direct Connect provides a dedicated private network connection with consistent throughput.

</details>

<details><summary>◯ <b>C.</b> Amazon CloudFront</summary>

❌ **Incorrect.** CloudFront is a content delivery network. It does not connect data centers to AWS.

</details>

<details><summary>◯ <b>D.</b> AWS Global Accelerator</summary>

❌ **Incorrect.** Global Accelerator routes user traffic over the AWS global network and gives a data center no connection to AWS.

</details>

Study: [10.3 Hybrid Connectivity: Direct Connect, VPN & Transit Gateway](../README.md#103-hybrid-connectivity-direct-connect-vpn--transit-gateway)

[Study guide: 10. Networking & Content Delivery](../README.md#10--networking--content-delivery) · [All topics](README.md) · [Next: 11. Security, Identity & Compliance](11-security-identity-compliance.md)

*Original exam-style practice questions written for this study guide. They are not actual AWS exam questions, and this project is not affiliated with or endorsed by AWS.*
