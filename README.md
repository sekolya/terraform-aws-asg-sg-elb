# terraform-aws-asg-elb

### Requirements
### please use terraform 0.14.7 or above
### Please copy paste below code
```
module "wordpress" {
  app_name         = "wordpress"
  source           = "../aws-asg-elb"
  aws_region       = "us-east-1"
  desired_capacity = 1
  max_size         = 1
  min_size         = 1
  key_name         = "developer-key"
  key_location     = "~/.ssh/id.rsa.pub"
  ssh_cidr_blocks = [
    "127.0.0.0/32",
    "0.0.0.0/0"
  ]

}
```

### Please run 

```
terraform init
terraform apply
```