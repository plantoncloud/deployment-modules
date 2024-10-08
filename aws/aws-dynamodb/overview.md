# Overview

The AWS DynamoDB API resource provides a consistent and streamlined interface for deploying and managing DynamoDB tables within our cloud infrastructure. By abstracting the complexities of AWS DynamoDB configurations, this resource allows you to define your database requirements effortlessly while ensuring consistency and compliance across different environments.

## Why We Created This API Resource

Deploying DynamoDB tables can be intricate due to the numerous configuration options and best practices that need to be considered. To simplify this process and promote a standardized approach, we developed this API resource. It enables you to:

- **Easily Configure Tables**: Define table names, keys, billing modes, and other essential settings without dealing with low-level AWS details.
- **Maintain Consistency**: Ensure that all DynamoDB tables across various environments adhere to our organization's standards and policies.
- **Enhance Productivity**: Reduce the time and effort required to deploy and manage DynamoDB tables, allowing you to focus on application development.

## Key Features

### Environment Integration

- **Environment Info**: Integrates with our environment management system to deploy tables within specific environments seamlessly.
- **Stack Job Settings**: Supports custom stack job settings for infrastructure-as-code deployments.

### AWS Credential Management

- **AWS Credential ID**: Utilizes specified AWS credentials to ensure secure and authorized deployments.

### Customizable Table Specifications

- **Table Name**: Option to provide a custom table name or generate one based on the context.
- **Billing Mode**: Choose between `PROVISIONED` and `PAY_PER_REQUEST` billing modes.
- **Key Attributes**: Define the hash (partition) key and optional range (sort) key, including their data types.

### Advanced Configurations

- **Streams**: Enable DynamoDB Streams and specify the `stream_view_type` to control what data is captured.
- **Server-Side Encryption**: Configure encryption at rest using AWS-managed keys or custom KMS keys.
- **Point-in-Time Recovery**: Enable point-in-time recovery for data protection against accidental writes or deletes.
- **Time to Live (TTL)**: Set up TTL configurations to automatically remove expired items from the table.
- **Auto Scaling**: Define auto-scaling policies for read and write capacities based on target utilization metrics.

### Indexes Support

- **Global Secondary Indexes (GSIs)**: Create GSIs with specific key schemas, projection types, and provisioned capacities.
- **Local Secondary Indexes (LSIs)**: Define LSIs at table creation for additional query flexibility using alternative sort keys.

### Data Import Capability

- **S3 Data Import**: Import data from Amazon S3 into a new table, supporting various input formats (`CSV`, `DYNAMODB_JSON`, `ION`) and compression types (`GZIP`, `ZSTD`, `NONE`).
- **Input Format Options**: Customize CSV import options, including delimiters and header definitions.

### Global Tables Configuration

- **Replication**: Configure DynamoDB Global Tables V2 for multi-region replication by specifying replica regions.

## Benefits

- **Simplified Deployment**: Reduce the complexity involved in setting up DynamoDB tables with a user-friendly API.
- **Consistency**: Ensure all tables comply with organizational standards for security, performance, and scalability.
- **Scalability**: Leverage auto-scaling features to handle varying workloads efficiently.
- **Security**: Integrate with AWS KMS for encryption and manage credentials securely.
- **Flexibility**: Customize tables extensively to meet specific application requirements without compromising on best practices.
