# AWS-CloudFormation

CloudFormation allows us to provision infrastructure as code. To test CloudFormation, using a template we are going to create a stack from which an S3 bucket will be deployed. Then, we'll refresh the stack by adding another S3 bucket, and finally we'll delete it.

![Diagram](https://static.platzi.com/media/articlases/Images/Screenshot%20at%202022-06-03%2015-03-58.png)

```json
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description": "this template does XXXX",
  "Metadata": {},
  "Parameters": {},
  "Mappings": {},
  "Conditions": {},
  "Transform": {},
  "Resources": {},
  "Outputs": {}
}

- **AWSTemplateFormatVersion**: This parameter is optional. Here, we specify the template version.
- **Description**: A text string describing the template. It should come after AWSTemplateFormatVersion.
- **Metadata**: Objects that provide additional information about the template.
- **Parameters**: Values that we will pass to the template when it is executed, either during stack creation or update.
- **Mappings**: Allows us to map a set of values to a specific key. For example, to set values based on a region, we can create a mapping that uses the region name as the key and contains the values we want to specify for each region.
- **Conditions**: Controls whether resources are created or values are assigned to those resources based on a condition. For example, we can assign different values for production or testing environments.
- **Transform**: Specifies the macros that AWS CloudFormation uses to process the template.
- **Resources**: This is where you declare the resources to include in the stack. For example, EC2 instances or S3 buckets.
- **Outputs**: Declares output values that can be used in other stacks.
