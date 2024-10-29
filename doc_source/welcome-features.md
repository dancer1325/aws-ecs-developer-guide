# Amazon ECS components<a name="welcome-features"></a>

## Clusters<a name="welcome-clusters"></a>

* := logical grouping of tasks or services
  * uses
    * isolate your applications
      * -> != underlying infrastructure
  * 👀if your tasks are run | Fargate -> your cluster resources -- are ALSO managed by -- Fargate 👀 

## Containers and images<a name="welcome-containers-images"></a>

* 👀if you want to deploy applications | Amazon ECS -> requirements 👀
  * your application components -- must be configured to -- run | *containers* 
* container
  * := standardized unit of software development /
    * holds everything / your software application -- requires to -- run
      * everything == relevant code + runtime + system tools + system libraries
  * -- created from a -- *image*
* *image*
  * := read-only template 
    * typically built -- from a -- Dockerfile
* Dockerfile
  * == plaintext file / specifies
    * ALL components / included | container
  * once they're built -> these images are stored | container *registry*
    * where they can be downloaded from
    * see [Creating a container image for use on Amazon ECS](create-container-image.md)

![\[Diagram showing Docker image creation and registration within an Amazon ECS environment.\]](http://docs.aws.amazon.com/AmazonECS/latest/developerguide/images/overview-containers.png)

## Task definitions<a name="welcome-task-definitions"></a>

* *task definition*
  * := text file /
    * -- describes -- [1,10] containers / -- form -- your application
      * == 👀 blueprint for your application 👀 
      * parameters 
        * / can be specified
          * for the OS
          * containers to use
          * ports to open -- for your -- application
          * data volumes -- to use with the -- containers | task
        * -- depend on the -- needs of your specific application
    * JSON format
  * uses
    * run tasks
    * create services
  * recommendations
    * 👀span your application -- across -- MULTIPLE task definitions 👀
      * -- via --
        * combining related containers | their own task definitions / EACH -- represents -- 1! component 
  * requirements
    * cluster MUST be
      * up
      * running


## Tasks<a name="welcome-task-sched"></a>

* *task*
  * == instantiation of a task definition | a cluster
  * steps
    * create a task definition -- for -- your application | Amazon ECS
    * specify the # of tasks / run | your cluster
  * ways to run a task
    * as standalone task
    * as part of a service

## Services<a name="welcome-service"></a>

* Amazon ECS *service*
  * uses
    * run & maintain 👀your desired 👀 number of tasks simultaneously | Amazon ECS cluster
      * maintain == if any of your tasks fail or stop -> Amazon ECS service scheduler launches another instance / -- based on -- your task definition

## Container agent<a name="welcome-agent"></a>

* *container agent*
  * runs | EACH container instance | Amazon ECS cluster
  * -- sends information to -- Amazon ECS,  about the 
    * current running tasks
    * resource utilization of your containers
  * -- based on -- request from Amazon ECS,
    * starts tasks
    * stops tasks
  * see [Amazon ECS container agent](ECS_agent.md)

![\[Diagram showing container agent tasks within an Amazon ECS environment.\]](http://docs.aws.amazon.com/AmazonECS/latest/developerguide/images/overview-containeragent-fargate.png)

## Fargate architecture overview<a name="welcome-architecture"></a>

* Amazon ECS is a Regional service
* Amazon ECS clusters can be created | NEW or EXISTING VPC
+ _Example:_ architecture of an Amazon ECS environment / runs | AWS Fargate

![\[Diagram showing architecture of an Amazon ECS environment using the Fargate launch type.\]](http://docs.aws.amazon.com/AmazonECS/latest/developerguide/images/overview-fargate.png)