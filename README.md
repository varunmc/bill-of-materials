# bill-of-materials
_Declaration of all external Maven artifacts used by the platform_

A "Bill Of Materials" (BOM) is a POM defining the default version of dependencies that could be used by a project. The project would then import the BOM, thereby making available all declared dependencies. For more information, read [Importing Dependencies](https://maven.apache.org/guides/introduction/introduction-to-dependency-mechanism.html#Importing_Dependencies).

This BOM is imported into the [parent](https://github.com/varunmc/parent).

## Getting Started
The [AWS CodeFormation](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stack/detail?stackId=arn:aws:cloudformation:us-east-1:497513737772:stack%2FBillOfMaterials%2F4741fed0-92db-11e7-b09f-50d5cd1ea8d2) template _stack.yml_ will create an [AWS CodePipeline](https://console.aws.amazon.com/codepipeline/home?region=us-east-1#/view/BillOfMaterials) with an [AWS CodeBuild](https://console.aws.amazon.com/codebuild/home?region=us-east-1#/projects/BillOfMaterials/view) builder as defined in _buildspec.yml_. The continuous build pipeline will package and publish the artifact to [AWS S3](https://s3.console.aws.amazon.com/s3/buckets/maven.varun.mc/mc/varun/bill-of-materials/?region=us-east-1&tab=overview).
