# terraform-examples

A collection of Terraform examples for learning Infrastructure as Code (IaC) on AWS. This repository demonstrates common patterns such as basic resources, parameterized configurations with variables, and reusable modules.

## Prerequisites

- [Terraform](https://developer.hashicorp.com/terraform/downloads) installed (v1.0+)
- An [AWS account](https://aws.amazon.com/) with configured credentials
- The [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html) installed and configured (`aws configure`)

## Getting Started

Clone the repository and navigate into it:

```bash
git clone https://github.com/jaezeu/terraform-examples.git
cd terraform-examples
```

Each example is self-contained. To run one, change into its directory and use the standard Terraform workflow:

```bash
cd terraform-examples/<example-directory>

terraform init      # Initialize providers and modules
terraform plan      # Preview the changes
terraform apply     # Create the resources
terraform destroy   # Tear down the resources when done
```

## Repository Structure

- **`main.tf`** — A basic root example that provisions an S3 bucket.
- **`terraform-examples/`** — A collection of more focused examples:

| Example | Description |
| --- | --- |
| `custom-module-example` | Consuming a locally-defined custom module. |
| `dynamodb-parameterized-example` | Creating a DynamoDB table driven by input variables. |
| `ec2-key-multi-env-module-example` | An EC2 + key pair setup across multiple environments using modules. |
| `ec2-module-example` | Provisioning EC2 instances via a module. |
| `public-vpc-module-example` | Building a public VPC using a module. |
| `s3-parameterized-example` | Creating an S3 bucket driven by input variables. |

## Notes

- Applying these examples may create billable AWS resources. Remember to run `terraform destroy` to avoid unexpected charges.
- Update variable values (such as bucket names and regions) to match your own AWS environment before applying.

## License

This project is provided as-is for educational purposes.
