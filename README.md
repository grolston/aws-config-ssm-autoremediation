# Proof of Concept - AWS Config Custom Rule with Auto Remediation

Automatically Remediate EC2 instance ports accessible to the internet (0.0.0.0/0) with AWS Config and AWS System Manager.

## Overview

The project is closely based on the AWS Blog Post *[How to auto-remediate internet accessible ports with AWS Config and AWS System Manager](https://aws.amazon.com/blogs/security/how-to-auto-remediate-internet-accessible-ports-with-aws-config-and-aws-system-manager/)* by Amal AlQhtani. The project simplifies the deployment by giving it a one-click deployment solution. The deployed solution creates:

1. Custom AWS Config rule backed by lambda
2. SSM Automation Document leveraging aws:executeScript with python
3. AWS Config Automated Remedation configuration (ties AWS Config compliance to automated response from SSM Automation document)

For more information review the blog post [How to auto-remediate internet accessible ports with AWS Config and AWS System Manager](https://aws.amazon.com/blogs/security/how-to-auto-remediate-internet-accessible-ports-with-aws-config-and-aws-system-manager/)

> Note: At this time there is no deviation from the implementation created by Amal AlQhtani. Current work will be in factoring privileges and applying security best practices to the cloudformation.

## Prerequisites

The following prerequisites will need to be met to launch solution in your account.

1. Ensure the AWS Config Record configured in specified region
2. Minimum of AWS Config recording EC2 resources in specified region


## Deployment

1. Open your web browser and login to your AWS Account.
2. Click this button to launch stack.
3. Fill out parameters

> **Note:** If you want to open the link as a new tab use `ctrl+click` when clicking the *launch Stack* button below...or do the two-finger click and select `open new tab`

[![Launch Stack](https://cdn.rawgit.com/buildkite/cloudformation-launch-stack-button-svg/master/launch-stack.svg)](https://console.aws.amazon.com/cloudformation/home#/stacks/new?templateURL=https://rolston-cloud-library.s3.amazonaws.com/grolston-aws/aws-config-ssm-autoremediation/main.yml)