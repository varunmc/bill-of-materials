# bill-of-materials
_Declaration of all external Maven artifacts used by the platform_

A "Bill of Materials" defines the versions of all third-party artifacts that can be used by a project. For more information, read [Importing Dependencies](https://maven.apache.org/guides/introduction/introduction-to-dependency-mechanism.html#Importing_Dependencies).

It serves as a central location to set versions to dependencies that can then be used by all child projects. This is done by using the ```xml <scope>import</scope>``` in a [parent](https://github.com/varunmc/parent) POM's ```xml <dependencyManagement/>``` section.

## Getting Started
The AWS CloudFormation template _stack.yml_ will create an AWS CodePipeline with an AWS CodeBuild phase. The build will execute `buildspec.yml` which will execute `mvn deploy` and publish the artifact to the internal Maven repository.

## Links
* [Stack](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stack/detail?stackId=arn:aws:cloudformation:us-east-1:497513737772:stack%2FBillOfMaterials%2F4741fed0-92db-11e7-b09f-50d5cd1ea8d2)
* [Build Pipeline](https://console.aws.amazon.com/codepipeline/home?region=us-east-1#/view/BillOfMaterials)
* [Maven Builder](https://console.aws.amazon.com/codebuild/home?region=us-east-1#/projects/BillOfMaterials/view)
* [Artifacts](https://s3.console.aws.amazon.com/s3/buckets/maven.varun.mc/mc/varun/bill-of-materials/?region=us-east-1&tab=overview)
