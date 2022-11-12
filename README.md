# ELB with stickiness Example

The example launches a web server, installs nginx, creates an ELB for instance. It also creates security groups for the ELB and EC2 instance.


To run, configure your AWS provider as described in https://www.terraform.io/docs/providers/aws/index.html


This example assumes you have created a Key Pair use:
https://console.aws.amazon.com/ec2/v2/home 


region=ap-south-1 #KeyPairs:sort=keyName to create a key if you do not have one.

Run this example using commands :

```
terraform init
```

```
terraform plan
```

```
terraform apply -var 'key_name=YOUR_KEY_NAME'
```

Alternatively to using `-var` with each command, the `terraform.template.tfvars` file can be copied to `terraform.tfvars` and updated.

Wait a couple of minutes for the EC2 userdata to install nginx, and then type the ELB DNS Name from outputs in your browser and see the nginx welcome page.

At last if you want to delete the resources to avoid unnecessary charges , you should use:

```
terraform destroy
```

**NOTE** : YOU WILL GET ELB DNS NAME FROM THE AWS CONSOLE UNDER SERVICE ELB 
