# DevOps assessment terraform

This is the template you can use to do the Terraform part of the [devops assessment][1].
Notice the following:

 * You don't have access to S3, so use a local state file
 * There are some data types defined to help you start
 * If you have time to prepare CI/CD workflow for this project, do it. But don't get crazy about it

These are the services you have access to:

 * Full ECS permissions
 * Full EC2 permissions
 * Full LoadBalancer (ELB/ELBv2) permissions
 * Full VPC permissions
 * Read-only access to IAM role 'ecsTaskExecutionRole'


[1]: https://github.com/travelperk/devops-assessment
