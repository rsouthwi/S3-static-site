# s3-static-site
This is for  [a domain that I own](http://www.ronsouthwick.com).  
I'm using an AWS S3 bucket to serve this static website.

![](images/regal_ant.gif)

### Deployment
This site is deployed via [Terraform](https://www.terraform.io/).  

1. create the file `terraform.tfvars` at the root including values for `aws_region` and `bucket_name`
2. `terraform init` – downloads provider and module files
3. `terraform plan` – validates and creates a plan
4. `terraform apply` – implements the plan
  (note: sometimes the first time this command is run, it results in the following message:
  `Error putting S3 policy: AccessDenied: Access Denied`  so run `terraform apply` twice ¯\_(ツ)_/¯ )
5. `terraform destroy` – throws it all away