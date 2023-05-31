# s3-static-site
This is for  [a domain that I own](http://www.ronsouthwick.com).  
I'm using an AWS S3 bucket to serve this static website.

![](images/regal_ant.gif)

### Deployment
This site is deployed via [Terraform](https://www.terraform.io/).  

1. create the file `terraform.tfvars` at the root including values for `aws_region` and `bucket_name`
2. `terraform init` – downloads provider and module files
3. `terraform plan` – validate and create a plan
4. `terraform apply` – implement the plan (note: some times this command needs to be run twice ¯\_(ツ)_/¯ )
5. `terraform destroy` – throws it all away