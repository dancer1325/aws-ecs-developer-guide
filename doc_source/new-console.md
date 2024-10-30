# New Amazon ECS console<a name="new-console"></a>

* allows
  * deploy containerized applications,
  * configure 
    * load balancing,
    * networking,
  * monitoring,
  * new workflows -- for the -- effective
    * operations
    * troubleshooting 

* new console

## Configuration which is not available in the new console<a name="classic-console-use-cases"></a>

* classic console vs new console
  * less functionalities

### First run wizard<a name="classic-console-first-run"></a>

* see [Getting started with Amazon ECS](getting-started.md)

### Clusters<a name="classic-console-clusters"></a>

* cluster parameters / -- can be configured via -- AWS CLI
  + **Spot Instances**
    + requirements
      + EC2 launch type
    + uses
      + cluster Auto Scaling group
  + **Creating a new VPC | cluster creation**
    + if you create a cluster -> MUST use existing VPCs & subnets 
* [create AWS cluster -- via -- AWS CLI](https://docs.aws.amazon.com/cli/latest/reference/ecs/create-cluster.html)

### Task definitions<a name="classic-console-task-def"></a>

* ways to configure
  * JSON editor | new console
    * see [Creating a task definition using the console](create-task-definition.md)
  * AWS CLI
    * see [register\-task\-definition](https://docs.aws.amazon.com/cli/latest/reference/ecs/register-task-definition.html) 
* task definition parameters / can be configured
  + **Docker labels**
  + **AWS App Mesh integration**
  + **FireLens customization**
  + **Elastic inference**
  + **Task placement constraints**
  + **Update a service with the new task definition revision**
  + **Network modes**
    + NOT supported
      + **host**
      + **none**
  + **Container parameters** 
    + NOT supported
      + **Startup and dependency ordering**
      + **Individual container log configuration** Monitoring and logging has replaced this option
      + **Timeouts, ulimits, and network settings**
* ONLY CloudWatch log driver -- is -- supported

### Tasks<a name="classic-console-tasks"></a>

* ways to configure scheduled tasks
  * EventBridge console
    * see [Scheduled tasks](scheduled_tasks.md)
  * AWS CLI

### Services<a name="classic-console-services"></a>

* ways to deploy a service
  * AWS CLI
    * see [how to create a service](https://docs.aws.amazon.com/cli/latest/reference/ecs/create-service.html)
  * AWS CloudFormation
    * see [AWS::ECS::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-service.html)
* common actions | service
  * **Service Discovery**
    * ONLY view your Service Discovery configuration
  * **Step scaling policies for service auto scaling**
  * **Tracking policy with a custom metric** 
  * **Update Service**
    * NOT possible to update the 
      * `awsvpc` network configuration
      * health check grace period

### Container instances<a name="classic-console-instances"></a>

* AWS CLI enables,
  * about custom metadata
    * -- for -- your container instance
      * view
      * edit
    * except to, **Instance attributes** 
* see
  * [Adding an attribute using the classic console](task-placement-constraints.md#add-attribute)
  * [Filtering by attribute using the console](task-placement-constraints.md#filter-attribute)

## List view enhancements<a name="display-enhancements"></a>

* list views 
  * -- for --
    * your resources 
      * cluster,
      * services,
      * task definitions
    * items
      * networking,
      * container instances,
      * deployments
  * are displayed | table / you can adjust
    + number of items / page
    + fields / are visible
    + if it's applicable -> 
      + line wrap option
      + timestamp format
        + default is the absolute time | local format
        + available options
          + Absolute time | ISO format
          + Relative time