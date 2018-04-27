---
description: 'FAQ: https://aws.amazon.com/cloudformation/faqs/'
---

# AWS CloudFormation

Provides a common language for you to describe and provision all the infrastructure resources in your cloud environment. CloudFormation allows you to use a simple text file to model and provision, in an automated and secure manner, all the resources needed for your applications across all regions and accounts. This file serves as the single source of truth for your cloud environment.

* Available at **no additional charge**, and you pay only for the AWS resources needed to run your applications.
* Template Sections
  * Format Version \(optional\) - The template format version can change independently of the API and WSDL versions.
  * Description \(optional\) - A text string that describes the template. This section must always follow the template format version section.
  * Metadata \(optional\) - Objects that provide additional information about the template.
  * Parameters \(optional\) - Values to pass to your template at runtime \(when you create or update a stack\).
  * Mappings \(optional\) - A mapping of keys and associated values that you can use to specify conditional parameter values, similar to a lookup table.
  * Conditions \(optional\) - Conditions that control whether certain resources are created or whether certain resource properties are assigned a value during stack creation or update.
  * Transform \(optional\) - For serverless applications, specifies the version of the AWS Serverless Application Model \(AWS SAM\) to use. The model defines the syntax that you can use and how it is processed.
  * Resources \(required\) - Specifies the stack resources and their properties, such as an Amazon Elastic Compute Cloud instance or an Amazon Simple Storage Service bucket.
  * Outputs \(optional\) - Describes the values that are returned whenever you view your stack's properties. For example, you can declare an output for an S3 bucket name and then call the aws cloudformation describe-stacks AWS CLI command to view the name.

