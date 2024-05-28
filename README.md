## Learn Terraform - Terraform Conditions
Follow along with this [Hashicorp tutorial](https://developer.hashicorp.com/terraform/tutorials/configuration-language/custom-conditions).

## Goal
* Use custom condition blocks
  * if they fail -> custom error messages produced

## Prerequisites
* Terraform [v1.2+](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli) installed locally
* AWS account with [associated credentials](https://registry.terraform.io/providers/hashicorp/aws/latest/docs#authentication-and-configuration)
  * via
    * add in the 'provider' block
    * environment variables
      * 'AWS_ACCESS_KEY_ID'
      * 'AWS_SECRET_ACCESS_KEY'
      * 'AWS_REGION'
    * credential files
      * `aws config` & pass the 'AWS_ACCESS_KEY_ID' & 'AWS_SECRET_ACCESS_KEY'


## How to run?
* `terraform init`
* `terraform plan`
  * if some resource lifecycle precondition fails -> NOT checked the plan
* `terraform apply`
  * if some resource lifecycle precondition fails -> NOT DONE the apply
  * `terraform appy -var aws_region=us-west-1`
    * pass another variable rather than default one
* `terraform destroy`

## Notes
* 'modules/'
  * local module
* 'terraform.tfvars'
  * file name / detected automatically to provide input variables