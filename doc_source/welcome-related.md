# Related services<a name="welcome-related"></a>

* AWS services / -- used along -- Amazon ECS
  * **AWS Identity and Access Management**
    * uses | Amazon ECS
      * control access | 
        * container instance level -- via -- IAM roles
        * task level -- via -- IAM task roles
      * see [Identity and Access Management for Amazon Elastic Container Service](security-iam.md) 

  * **Amazon EC2 Auto Scaling**
    * \+ Fargate task | service
      * to scale -- in response to a -- # of metrics
    * \+ EC2 task
      * to scale the container instances | your cluster
    * see [Service auto scaling](service-auto-scaling.md)

  * **Elastic Load Balancing**
    * uses
      * achieve greater levels of fault tolerance | your applications
      * provide the amount of load\-balancing capacity / -- required to -- distribute application traffic
      * create an endpoint / balances traffic -- across -- services | cluster
    * see [Service load balancing](service-load-balancing.md)

  * **Amazon Elastic Container Registry**
    * repositories & images / hosted
      * == resource\-based permissions using IAM / specific users or tasks -- can -- access 
    * see the *[Amazon Elastic Container Registry User Guide](https://docs.aws.amazon.com/AmazonECR/latest/userguide/)*

  * **AWS CloudFormation**  
    * uses
      * define -- as -- entities | AWS CloudFormation script
        * clusters,
        * task definitions,
        * services 
    * see [AWS CloudFormation Template Reference](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/)\