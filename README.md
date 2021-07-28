# Proof of Concept - AWS Config Custom Rule with Auto Remediation

Automatically Remediate EC2 Instance Ports Accessible to the Internet with AWS Config and AWS System Manager.

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