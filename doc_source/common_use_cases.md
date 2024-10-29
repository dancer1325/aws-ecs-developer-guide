# Common use cases in Amazon ECS<a name="common_use_cases"></a>

* common use cases
  * Microservices
  * Websites
  * Video rendering services
  * Machine learning
* \+ AWS Batch
  * use cases
    * farm out tasks -- across -- your containers

## Additional resources<a name="additional-resources"></a>

* more use cases
  * create a consistent build and deployment experience
  * manage and scale batch & Extract-Transform-Load \(ETL\) workloads
  * build sophisticated application architectures | microservices model
  * see [Container Use Cases](http://aws.amazon.com/containers/)

* _Examples:_ 
  * [Deploying Microservices with Amazon ECS, AWS CloudFormation, and an Application Load Balancer](https://github.com/awslabs/ecs-refarch-cloudformation)
  * about CI/CD
    + [ECS Reference Architecture: Continuous Deployment](https://github.com/awslabs/ecs-refarch-continuous-deployment)
    + [Continuous Delivery Pipeline for Amazon ECS Using Jenkins, GitHub, and Amazon ECR](https://github.com/awslabs/aws-cicd-docker-containers)

* check
  * [Managing Secrets for Amazon ECS Applications Using Parameter Store and IAM Roles for Tasks](http://aws.amazon.com/blogs/compute/managing-secrets-for-amazon-ecs-applications-using-parameter-store-and-iam-roles-for-tasks/)
    * goal
      * how to integrate the [Amazon ECS' functionality IAM roles for tasks](task-iam-roles.md) -- with the -- AWS Systems Manager Parameter Store
  * about making your services discoverable:
    + [Run Containerized Microservices with Amazon ECS Container Service and Application Load Balancer](http://aws.amazon.com/blogs/compute/microservice-delivery-with-amazon-ecs-and-application-load-balancers/)
      + goal
        + how to use the Elastic Load Balancing Application Load Balancers features
          + dynamic port mapping
          + path\-based routing
    + [Amazon Elastic Container Service \- Reference Architecture: Service Discovery](https://github.com/awslabs/ecs-refarch-service-discovery/)
    + [Metrics and traces collection from Amazon ECS using AWS Distro for OpenTelemetry with dynamic service discovery](http://aws.amazon.com/blogs/containers/metrics-and-traces-collection-from-amazon-ecs-using-aws-distro-for-opentelemetry-with-dynamic-service-discovery/)
      + goal
        + employ 1! instance of an ADOT Collector / 
          + collect X\-Ray traces & Prometheus metrics -- from -- Amazon ECS services / dynamically discovered -- via -- AWS Cloud Map