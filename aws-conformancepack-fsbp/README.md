<p align="center">
</p>

# Automated, Real Time and Continuous Remediations for FSBP Benchmarks using AWS Config

These templates provide real time, continuous and automated remediations for each of the FSBP benchmarks by providing a fully automated  integration with AWS Config Remediation and AWS Systems Manager automation documents. They leverage the format of AWS Config Conformance Packs


Template 1 first provisions AWS Systems Manager Automation Documents as well as all the required pre-reqs. Template 2 then leverages the SSM documents within AWS Config Remediation Rules in the format of Conformance Packs.


## How it Works

1. Leverages the format of AWS Conformance Templates
2. Leverages AWS Config Managed Rules to provide automated and continuous detection and recording of FSBP Benchmarks - native built-in support from AWS for providing secure compliance baselines
3. Provides NEW AWS Systems Manager Automation Documents for automated remediation for AWS Config FSBP Benchmark findings
4. Provides NEW integration of AWS Config Remediations with AWS Systems Manager Automation Documents to provide continuous and real time remediations of AWS Config FSBP Benchmark findings


## DEMO

Watch a [demo](https://awscisautoreme.com/overview.html) here to see how this solution works end to end for CIS Benchmarks

## COVERAGE

The [Coverage Matrix](https://github.com/kmmahaj/config/blob/master/aws-auto-remediate-fsbp-securityhub/coverage/AWS%20SecurityHub%20Benchmarks-Coverage-v1.xlsx) provides the current coverage of this solution wrt the FSBP Benchmarks
 
## Solution Design

![Solution Design](https://github.com/kmmahaj/config/blob/master/aws-conformancepack-pci/images/arch-diagram1.png)


## How To Install

1. **Template 1 of 2:** aws-fsbp-confpack-ssmautomation.yml
* Provisions AWS Systems Manager automation documents. These documents are used to provide automated remediations within the provisioned AWS Config Rule.
* Provisions with fully built-in pre-reqs. No input parameters required. Simply install on the CloudFormation console (or CLI). Installs in approx 3-4 mins.

2. **Template 2 of 2:** aws-fsbp-conformancepack.yml
* Provisions AWS Config Rules in the format of a Conformance Template with built-in remediation. No input parameters. Simply install on the CloudFormation console (or CLI). Installs in approx 3-4 mins.
* Leverages the output from the previous template specifically the AWS Systems Manager Automation documents


## Author

Kanishk Mahajan; kmmahaj@amazon.com
