# Rules for AWS IoT<a name="iot-rules"></a>

Rules give your devices the ability to interact with AWS services\. Rules are analyzed and actions are performed based on the MQTT topic stream\. You can use rules to support tasks like these:
+ Augment or filter data received from a device\.
+ Write data received from a device to an Amazon DynamoDB database\.
+ Save a file to Amazon S3\.
+ Send a push notification to all users using Amazon SNS\.
+ Publish data to an Amazon SQS queue\.
+ Invoke a Lambda function to extract data\.
+ Process messages from a large number of devices using Amazon Kinesis\.
+ Process messages from a large number of devices using Amazon Kinesis Firehose\.
+ Send data to the Amazon Elasticsearch Service\.
+ Capture a CloudWatch metric\. 
+ Change a CloudWatch alarm\.
+ Send the data from an MQTT message to Amazon Machine Learning to make predictions based on an Amazon ML model\. 
+ Send a message to a Salesforce IoT Input Stream\.
+ Send message data to an AWS IoT Analytics channel\.
+ Start execution of a Step Functions state machine\.
+ Send message data to an AWS IoT Events input\.
+ Send message data an asset property in AWS IoT SiteWise\.
+ Send message data to a web application or service\.

Your rules can use MQTT messages that pass through the publish/subscribe [Message Broker for AWS IoT](iot-message-broker.md) or, using the [Basic Ingest](iot-basic-ingest.md) feature, you can securely send device data to the AWS services listed above without incurring [messaging costs](https://aws.amazon.com/iot-core/pricing/)\. \(The [Basic Ingest](iot-basic-ingest.md) feature optimizes data flow by removing the publish/subscribe message broker from the ingestion path, so it is more cost effective while keeping the security and data processing features of AWS IoT\.\)

Before AWS IoT can perform these actions, you must grant it permission to access your AWS resources on your behalf\. When the actions are performed, you incur the standard charges for the AWS services you use\.

## Troubleshooting a Rule<a name="iot-troubleshoot-rule"></a>

If you are having an issue with your rules, you should enable CloudWatch Logs\. By analyzing your logs, you can determine whether the issue is authorization or whether, for example, a WHERE clause condition did not match\. For more information, see [Setting Up CloudWatchLogs](https://docs.aws.amazon.com/iot/latest/developerguide/cloud-watch-logs.html)\.
