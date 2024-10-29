# What is Amazon Elastic Container Service?<a name="Welcome"></a>

* Amazon ECS
  * FULLY managed container orchestration service / 
    * helps you easily about containerized applications 
      * deploy,
      * manage,
      * scale
    * -> 
      * built-in AWS configuration & operational best practices 
        * Reason: 🧠 it's fully managed 🧠
      * 👀NO need to manage control plane, nodes, or add\-ons 👀
    * regional service
  * integrations
    * with
      * AWS tools &
        * _Example:_ Amazon ECR
      * TP tools
        * _Example:_ Docker
    * benefits
      * focus on building the applications
        * NOT the environment
  * key features
    + serverless option -- via -- AWS Fargate
      + AWS Fargate 
        + allows
          + forgetting (== NO need to) manage servers,
          + handle capacity planning,
            + _Example:_ -- based on -- your 
              + resource needs,
              + isolation policies,
              + availability requirements 
          + isolate container workloads -- for -- security
    + external instance option / ECS Anywhere
      + ECS Anywhere
        + allows
          + managing your on-premises container workloads -- via --
            + Amazon ECS console
            + AWS CLI 
    + Amazon EC2 option
      + EC2 
        + allows
          + managing your EC2 instances -- via --
            + Amazon ECS console
            + AWS CLI
    + -- Integration with -- AWS IAM
      + allows
        + assign granular permissions / EACH of your containers
        + high level of isolation | building your applications
    + AWS managed container orchestration
    + CI/CD
      + common process | microservice architectures / -- based on -- Docker containers
      + typical actions 
        + Monitors changes | source code repository
        + Builds a new Docker image -- from -- that source
        + Pushes the image | image repository (_Example:_ Amazon ECR or Docker Hub)
        + Updates your Amazon ECS services -- to use the -- new image | your application
    + -- support for -- service discovery
      + use cases
        + distributed systems & SOA architectures
      + allows
        + your microservice components -- are automatically -- discovered | they're created & terminated | given infrastructure
    + -- support for -- sending your container instance log information -- to -> CloudWatch Logs
      + allows
        + monitoring better the logs from your container instances
        + preventing your container logs / take up disk space -- on -- your container instances
  * [AWS Containers Roadmap](https://github.com/aws/containers-roadmap)

## Launch types<a name="launch-types"></a>

* models to run your containers
  + Fargate launch type
    + 👀== serverless pay-as-you-go option 👀
      + == host your containers | Fargate (serverless infrastructure) / -- is managed by -- Amazon ECS
    + allows
      + running containers / WITHOUT needing to manage your infrastructure
    + use cases
      + workloads /
        + large / need optimization -- for -- low overhead 
        + Small / have occasional burst
        + Tiny workloads
        + Batch workloads
    + requirements
      + AWS Regions / Amazon ECS -- supports -- AWS Fargate
  + EC2 launch type
    + == configure & deploy EC2 instances | your cluster / run your containers
    + use cases
      + workloads /
        + require consistently high CPU core & memory usage
        + large workloads / need optimization -- for -- price
      + applications / -- need to access -- persistent storage
      + you MUST directly manage your infrastructure

## Access Amazon ECS<a name="welcome-interfaces"></a>

* available interfaces / allows creating, access, and manage your Amazon ECS resources
  + **AWS Management Console**
  + **AWS CLI**
    + [AWS Command Line Interface](https://aws.amazon.com/cli/)
  + **AWS SDKs**
    + see [AWS SDKs](http://aws.amazon.com/tools/#SDKs)
  + **AWS Copilot**
    + := open\-source tool /
      + audience
        + developers
      + allows
        + about containerized applications | Amazon ECS
          + build
          + release,
          + operate 
    + see [AWS Copilot](https://github.com/aws/copilot-cli)
  + **Amazon ECS CLI**
    + == CLI /
      + allows
        + running your applications | Amazon ECS & AWS Fargate -- via -- Docker Compose file format
        + quickly
          + provisioning resources,
          + push and pull images -- via -- Amazon ECR
        + monitor running applications | Amazon ECS or Fargate
        + 👀test containers / are running locally -- along with -- containers | Cloud 👀
    + see [Amazon ECS CLI](https://github.com/aws/amazon-ecs-cli)
  + **AWS CDK**
    + := open\-source software development framework /
      + allows
        + -- via -- familiar programming languages
          + model your cloud application resources
          + provision your cloud application resources
      + provisions your resources -- via -- AWS CloudFormation / manner
        + safe
        + repeatable 
    + see [Getting started with Amazon ECS using the AWS CDK](tutorial-ecs-web-server-cdk.md)

## Pricing<a name="welcome-pricing"></a>

* -- depends on --
  * [used launch type](#launch-typesa-namelaunch-typesa) -- to -- host your containerized workloads
* if you use Amazon ECS | AWS Outposts -> pricing model == pricing model / using Amazon EC2 directly 
* see [Amazon ECS Pricing](https://aws.amazon.com/ecs/pricing)
* [Savings Plans User Guide](https://docs.aws.amazon.com/savingsplans/latest/userguide/)
* check your bills
  * [AWS Billing and Cost Management console](https://console.aws.amazon.com/billing/)
  * [AWS Account Billing](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/)
* [contact AWS Support](https://aws.amazon.com/contact-us/)
* see [AWS Trusted Advisor](https://aws.amazon.com/premiumsupport/trustedadvisor/)
  * help you to optimize | your AWS environment 
    * costs,
    * security,
    * performance