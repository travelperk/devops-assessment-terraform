# DevOps assessment terraform

This is the template you can use to do the Terraform part of the [devops assessment][1]. Like the other repo,
please clone it and don't mention TravelPerk on name to avoid someone copies of your solution.

## What is expected

We should be able to request the application using the DNS of an external load
balancer on port 80. (443 not needed).

These are the services you have access to:

 * Full ECS permissions
 * Full EC2 permissions
 * Full LoadBalancer (ELB/ELBv2) permissions
 * Full VPC permissions
 * Read-only access to IAM role 'ecsTaskExecutionRole'


## Notes

 * You don't have access to S3, so use a local state file
 * Right now only 2 replicas are accepted due to service limits. Don't try to
   deploy more.
 * Keep in mind that Fargate needs to reach outside the VPC to download the
   containers from ECR. A `CannotPullContainerError` is not only a permission
   error. There are two ways to achieve this, all seem fine to us.
 * There is a role called `ecsTaskExecutionRole` available to be used as
   execution role of the tasks.
 * Maybe is a good idea to try to deploy manually in AWS and then use
   `terraform import` to define resources here.
 * Don't prepare CI/CD workflow for this project.

[1]: https://github.com/travelperk/devops-assessment
