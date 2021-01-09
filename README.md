<p align="center">
</p>

# Remediations for PCI DSS 3.2.1 and AWS Foundational Security Best Practices (FBSP) using AWS Config and Custom AWS Systems Manager Automation Documents

1. **aws-configremediations-pci**
* Provides custom AWS Systems Manager automation documents and AWS Config Remediations for AWS Foundational Security Best Practices (FSBP). Fully auotomated with CloudFormation (including pre-reqs). Installs in approx 3-4 mins.

2. **aws-configremediations-fsbp**
* Provides custom AWS Systems Manager automation documents and AWS Config Remediations for PCI DSS 3.2.1. Fully auotomated with CloudFormation (including pre-reqs). Installs in approx 3-4 mins.

3. **aws-confpackwithremediations-pci**
* Provides custom AWS Systems Manager automation documents and AWS Config Remediations for PCI DSS 3.2.1 packaged as custom AWS Config Conformance Packs. 

4. **aws-devsecops-conformancepack-pci**
* Provides a DevSecOps pipeline for implementing automated remediations for PCI DSS 3.2.1 using custom AWS Config Conformance Packs with custom AWS Systems Manager automation documents.
* **<https://aws.amazon.com/blogs/mt/devsecops-auto-healing-pci-dss-3-2-1-violations-aws-using-custom-aws-config-conformance-packs-aws-systems-manager-aws-codepipeline/>**



## COVERAGE

The repository provides remediations for the following PCI checks:
* [PCI.AutoScaling.1] Auto scaling groups associated with a load balancer should use health checks
* [PCI.CloudTrail.1] CloudTrail logs should be encrypted at rest using AWS KMS CMK
* [PCI.CloudTrail.2] CloudTrail should be enabled
* [PCI.CloudTrail.3] CloudTrail log file validation should be enabled
* [PCI.CloudTrail.4] CloudTrail trails should be integrated with CloudWatch Logs
* [PCI.CodeBuild.2] CodeBuild project environment variables should not contain clear text credentials
* [PCI.CW.1] A log metric filter and alarm should exist for usage of the "root" user
* [PCI.Config.1] AWS Config should be enabled
* [PCI.EC2.1] Amazon EBS snapshots should not be publicly restorable
* [PCI.EC2.2] VPC default security group should prohibit inbound and outbound traffic
* [PCI.EC2.3] Unused EC2 security groups should be removed
* [PCI.EC2.4] Unused EC2 EIPs should be removed
* [PCI EC2.5] Security groups should not allow ingress from 0.0.0.0/0 to port 22 
* [PCI.EC2.6] Ensure VPC flow logging is enabled in all VPCs
* [PCI.IAM.1] IAM root user access key should not exist
* [PCI.IAM.2] IAM users should not have IAM policies attached
* [PCI.IAM.3] IAM policies should not allow full * administrative privileges
* [PCI.KMS.1] Customer master key (CMK) rotation should be enabled
* [PCI.Lambda.1] Lambda functions should prohibit public access
* [PCI.Lambda.2] Lambda functions should be in a VPC
* [PCI.RDS.1] RDS snapshots should prohibit public access
* [PCI.RDS.2] RDS DB Instances should prohibit public access
* [PCI.Redshift.1] Amazon Redshift clusters should prohibit public access
* [PCI.S3.1] S3 buckets should prohibit public write access
* [PCI.S3.2] S3 buckets should prohibit public read access
* [PCI.S3.3] S3 buckets should have cross-region replication enabled
* [PCI.S3.4] S3 buckets should have server-side encryption enabled
* [PCI.SSM.1] Amazon EC2 instances managed by Systems Manager should have a patch compliance status of COMPLIANT after a patch installation

The repository provides remediations for the following FSBP checks:
* [EC2.3] Attached EBS volumes should be encrypted at-rest
* [GuardDuty.1] GuardDuty should be enabled
* [IAM.3] IAM users' access keys should be rotated every 90 days or less
* [Lambda.1] Lambda functions should prohibit public access by other accounts
* [Lambda.2] Lambda functions should use latest runtimes
* [RDS.3] RDS DB instances should have encryption at-rest enabled
* [SSM.1] EC2 instances should be managed by AWS Systems Manager
* [AutoScaling.1] Auto Scaling groups associated with a load balancer should use load balancer health checks
* [CloudTrail.1] CloudTrail should be enabled and configured with at least one multi-Region trail
* [CloudTrail.2] CloudTrail should have encryption at-rest enabled
* [CodeBuild.2] CodeBuild project environment variables should not contain clear text credentials
* [Config.1] AWS Config should be enabled
* [EC2.1] Amazon EBS snapshots should not be public, determined by the ability to be restorable by anyone
* [EC2.2] The VPC default security group should not allow inbound and outbound traffic
* [IAM.1] IAM policies should not allow full * administrative privileges
* [IAM.2] IAM users should not have IAM policies attached
* [IAM.4] IAM root user access key should not exist
* [IAM.7] Password policies for IAM users should have strong configurations
* [S3.1] S3 Block Public Access setting should be enabled
* [S3.2] S3 buckets should prohibit public read access
* [S3.3] S3 buckets should prohibit public write access
* [S3.4] S3 buckets should have server-side encryption enabled
* [RDS.1] RDS snapshots should be private
* [RDS.2] RDS DB instances should prohibit public access, determined by the PubliclyAccessible configuration
* [SSM.2] Amazon EC2 instances managed by Systems Manager should have a patch compliance status of COMPLIANT after a patch installation 



## Author

Kanishk Mahajan; kmmahaj@amazon.com
