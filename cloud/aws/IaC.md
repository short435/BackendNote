# Infrastructure as Code (IaC)

Cloud service always change fast beacuse of the new technology comes. For me the most important tool for Devops should be the Infrastructure as Code(IaC) tools.

## What's IaC Tools?

- Version control for the Cloud infra.
- Automatically test the correctness of the cloud infra.
- Get same infra on different environment.(Dev/Stage/Prod)


## Objective

For here, we would compare between different IaC tools for AWS service. In order to choose one in the different stiuations.


## AWS CloudFormation

Original IaC tool for the AWS which release in 2011. 

- Robust resource state management.
- Showing what's going to happen before you deploy the infra.
- Offer json and yml for the format.
- 


## AWS Serverless Application Model SAM

Superset of the CloudFormation. 

- More suitable for AWS Lambda or event-driven computing.

## AWS CDK

Latest IaC tool for the AWS which release in 2019. Able to use programming language to build the whole infrasturcute for AWS.(Python/Java/C#/TypeScript)

- You cloud take CDK as a high level language when comparing to the Cloudformation.
  - CloudForamtion -> assembly language
  - CDK -> Python/C#/JS any other high level language
- By adopting the CDK, you still get all the state management and inherent benefits (and downsides) of CloudFormation
- Consturcts
  - Re-use in different project.

==Additionaly, there are CDK for Terraform==

## Terraform

Introdcted in 2014 for targeting on AWS services. 

- Complex management scenarios and compliance across multiple clouds.
  - AWS/Azure/Google


## Comparison

### CloudFormation vs Terraform

| CloudFormation    | Terraform |
| -------- | ------- |
| Interacts with the infrastructure itself  | Interacts with AWS API    |
|struggled with these inconsistent states|resolve inconsistencies and refresh a correct state of the infrastructure|
|only for the subset of resources|importing unmanaged resources|
|AWS only|Hybrid cloud|


### CDK vs CloudFormation

CDK let user easier to get into the world of the cloud. CDK was built based on the CloudFormation.


