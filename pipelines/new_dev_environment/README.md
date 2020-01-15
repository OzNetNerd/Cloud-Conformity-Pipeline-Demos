# New Dev Environment
## CloudFormation

The template creates a new dev environment (VPC, internet gateway, security group, EC2 instance, etc).

## Pipeline

The pipeline consists of the following stages:

1. Using `awscli`, ensures the CloudFormation template is valid
2. Using [Pipeline Scanner](https://github.com/OzNetNerd/Cloud-Conformity-Pipeline-Scanner), ensures the CloudFormation template is secure

If the second stage fails, the insecure findings will be made available through the `findings.json` artifact.

If you'd like the pipeline to succeed, set the `CC_RISK_LEVEL` variable to `EXTREME`. 