# bill-of-materials
_Declaration of all external Maven artifacts used by the platform_

A "Bill of Materials" defines the versions of all third-party artifacts used by the platform. For more information, read [Importing Dependencies](https://maven.apache.org/guides/introduction/introduction-to-dependency-mechanism.html#Importing_Dependencies).

## Getting Started
The AWS CloudFormation template _stack.yml_ will create an AWS CodePipeline with an AWS CodeBuild phase. The build will execute `mvn deploy` which will publish the artifact to the internal Maven repository.
