# Deploy infrastructure for Example application

This configuration deploys infrastructure for an example application
* load balancer
* security group
* EC2 instances

## Notes
* `provider`
  * NOT specified because they are inherit from root module
* custom conditions added
  * resource preconditions to the lifecycle
  * datasource postcondition to the lifecycle
