
# Single instance of EC2

## Prerequisites

### create credentials and config files in .aws folder
https://registry.terraform.io/providers/hashicorp/aws/latest/docs#shared-credentials-file

Be aware that Terraform won't take region from the `config` file

It takes only credentials from `credentials` file

### double check `ami` identifiers (e.g.: they can be different for other regions)

&nbsp;

## Start

### run:
```
terraform init
```

### set profile in main.tf:
```
provider "aws" {
    profile = "<profile_name>"
}
```
or set environmental variable:
```
AWS_PROFILE=<profile_name>
```

Windows Powershell:
```
$env:AWS_PROFILE = '<profile_name>'
```

MacOS / Linux:
```
export AWS_PROFILE=<profile_name>
```
