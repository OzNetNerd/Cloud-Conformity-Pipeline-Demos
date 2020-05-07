# New Dev Environment
## CloudFormation

The template creates a new dev environment (VPC, internet gateway, security group, EC2 instance, etc).

## Pipeline

The pipeline uses this [Pipeline Scanner](https://github.com/OzNetNerd/Cloud-Conformity-Pipeline-Scanner) to ensure the CloudFormation template is secure

If scanner finds any issues, the pipeline fails. The insecure configurations will then be made available through the `findings.json` artifact.

If you'd like the pipeline to succeed, set the `CC_RISK_LEVEL` variable to `EXTREME`. 