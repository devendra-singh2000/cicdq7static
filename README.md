# Docker image using Jenkins and deploy on AWS ECS
---
## Requirements
| Name  | Version |
| ------ | ------ |
| Jenkins | >=2.3 |
| JDK | >=11.0 |
| Terraform | >=4.0 |
| AWS | >=4.0 |
| Ubuntu | >=20.04 |
| Git | >= 2.25 |
##  Infrastructure Setup 
| Number | Name |
| ------ | ------|
| 1 | VPC |
| 1 | Public subnets |
| 1 | Load Balancer |

## Set up a build pipeline with Jenkins and Amazon ECS
- We’ll be using a sample Java application, available on GitHub. The repository contains a simple Dockerfile that uses a openjdk base image and runs our application: 
- This Dockerfile is used by the build pipeline to create a new Docker image. The built image will then be used to start a new service on an ECS cluster. 
## Providers
AWS


## Modules
| Name | Description |
| ------ | ------ |
| vpc | To create VPC for our infrastructure |
| elb | For load balancer|
| sg | Security groups |
| subnet | For creating subnet |

##   Resources 
| Name | Type |
|------|------|
| [aws_vpc](https://registry.terraform.io/providers/hashicorp/random/latest/docs/resources/string) | resource |
| [aws_lb](https://registry.terraform.io/providers/hashicorp/random/latest/docs/resources/string) | resource |
| [aws_security_group](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/security_group) | resource |
| [aws_ecs_cluster](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/mq_broker) | resource |
| [aws_subnet](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/mq_broker) | resource |
| [aws_iam_role](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/mq_broker) | data source |
| [aws_ecs_task_definition](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/mq_broker) | resource |
| [aws_ecs_service](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/mq_broker) | resource |
| [aws_internet_gateway](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/mq_broker) | resource |
| [aws_route_table](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/mq_broker) | resource |


