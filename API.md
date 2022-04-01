# API Reference

**Classes**

Name|Description
----|-----------
[DockerImageName](#retbrown-cdk-ecr-deployment-dockerimagename)|*No description*
[ECRDeployment](#retbrown-cdk-ecr-deployment-ecrdeployment)|*No description*
[S3ArchiveName](#retbrown-cdk-ecr-deployment-s3archivename)|*No description*


**Structs**

Name|Description
----|-----------
[ECRDeploymentProps](#retbrown-cdk-ecr-deployment-ecrdeploymentprops)|*No description*


**Interfaces**

Name|Description
----|-----------
[IImageName](#retbrown-cdk-ecr-deployment-iimagename)|*No description*



## class DockerImageName  <a id="retbrown-cdk-ecr-deployment-dockerimagename"></a>



__Implements__: [IImageName](#retbrown-cdk-ecr-deployment-iimagename)

### Initializer




```ts
new DockerImageName(name: string, creds?: string)
```

* **name** (<code>string</code>)  *No description*
* **creds** (<code>string</code>)  *No description*



### Properties


Name | Type | Description 
-----|------|-------------
**uri** | <code>string</code> | The uri of the docker image.
**creds**? | <code>string</code> | __*Optional*__



## class ECRDeployment  <a id="retbrown-cdk-ecr-deployment-ecrdeployment"></a>



__Implements__: [IConstruct](#constructs-iconstruct), [IConstruct](#aws-cdk-core-iconstruct), [IConstruct](#constructs-iconstruct), [IDependable](#aws-cdk-core-idependable)
__Extends__: [Construct](#aws-cdk-core-construct)

### Initializer




```ts
new ECRDeployment(scope: Construct, id: string, props: ECRDeploymentProps)
```

* **scope** (<code>[Construct](#constructs-construct)</code>)  *No description*
* **id** (<code>string</code>)  *No description*
* **props** (<code>[ECRDeploymentProps](#retbrown-cdk-ecr-deployment-ecrdeploymentprops)</code>)  *No description*
  * **dest** (<code>[IImageName](#retbrown-cdk-ecr-deployment-iimagename)</code>)  The destination of the docker image. 
  * **src** (<code>[IImageName](#retbrown-cdk-ecr-deployment-iimagename)</code>)  The source of the docker image. 
  * **environment** (<code>Map<string, string></code>)  The environment variable to set. __*Optional*__
  * **memoryLimit** (<code>number</code>)  The amount of memory (in MiB) to allocate to the AWS Lambda function which replicates the files from the CDK bucket to the destination bucket. __*Default*__: 512
  * **role** (<code>[IRole](#aws-cdk-aws-iam-irole)</code>)  Execution role associated with this function. __*Default*__: A role is automatically created
  * **vpc** (<code>[IVpc](#aws-cdk-aws-ec2-ivpc)</code>)  The VPC network to place the deployment lambda handler in. __*Default*__: None
  * **vpcSubnets** (<code>[SubnetSelection](#aws-cdk-aws-ec2-subnetselection)</code>)  Where in the VPC to place the deployment lambda handler. __*Default*__: the Vpc default strategy if not specified




## class S3ArchiveName  <a id="retbrown-cdk-ecr-deployment-s3archivename"></a>



__Implements__: [IImageName](#retbrown-cdk-ecr-deployment-iimagename)

### Initializer




```ts
new S3ArchiveName(p: string, ref?: string, creds?: string)
```

* **p** (<code>string</code>)  *No description*
* **ref** (<code>string</code>)  *No description*
* **creds** (<code>string</code>)  *No description*



### Properties


Name | Type | Description 
-----|------|-------------
**uri** | <code>string</code> | The uri of the docker image.
**creds**? | <code>string</code> | __*Optional*__



## struct ECRDeploymentProps  <a id="retbrown-cdk-ecr-deployment-ecrdeploymentprops"></a>






Name | Type | Description 
-----|------|-------------
**dest** | <code>[IImageName](#retbrown-cdk-ecr-deployment-iimagename)</code> | The destination of the docker image.
**src** | <code>[IImageName](#retbrown-cdk-ecr-deployment-iimagename)</code> | The source of the docker image.
**environment**? | <code>Map<string, string></code> | The environment variable to set.<br/>__*Optional*__
**memoryLimit**? | <code>number</code> | The amount of memory (in MiB) to allocate to the AWS Lambda function which replicates the files from the CDK bucket to the destination bucket.<br/>__*Default*__: 512
**role**? | <code>[IRole](#aws-cdk-aws-iam-irole)</code> | Execution role associated with this function.<br/>__*Default*__: A role is automatically created
**vpc**? | <code>[IVpc](#aws-cdk-aws-ec2-ivpc)</code> | The VPC network to place the deployment lambda handler in.<br/>__*Default*__: None
**vpcSubnets**? | <code>[SubnetSelection](#aws-cdk-aws-ec2-subnetselection)</code> | Where in the VPC to place the deployment lambda handler.<br/>__*Default*__: the Vpc default strategy if not specified



## interface IImageName  <a id="retbrown-cdk-ecr-deployment-iimagename"></a>

__Implemented by__: [DockerImageName](#retbrown-cdk-ecr-deployment-dockerimagename), [S3ArchiveName](#retbrown-cdk-ecr-deployment-s3archivename)



### Properties


Name | Type | Description 
-----|------|-------------
**uri** | <code>string</code> | The uri of the docker image.
**creds**? | <code>string</code> | The credentials of the docker image.<br/>__*Optional*__



