## setup


```python
import boto3

# Set up client
client = boto3.client('service_name', region_name='your_region')

# Set up resource
resource = boto3.resource('service_name', region_name='your_region')
```

## Common operations

#### S3 Operations

```python
import boto3

# Initialize the S3 client
s3 = boto3.client('s3')

# List buckets
response = s3.list_buckets()
buckets = [bucket['Name'] for bucket in response['Buckets']]

# Create bucket
s3.create_bucket(Bucket='bucket_name')

# Delete bucket
s3.delete_bucket(Bucket='bucket_name')

# Upload file to bucket
with open('file.txt', 'rb') as file:
    s3.upload_fileobj(file, 'bucket_name', 'file.txt')

# Download file from bucket
with open('downloaded_file.txt', 'wb') as file:
    s3.download_fileobj('bucket_name', 'file.txt', file)

# List objects in bucket
response = s3.list_objects_v2(Bucket='bucket_name')
objects = [obj['Key'] for obj in response['Contents']]

# Delete object from bucket
s3.delete_object(Bucket='bucket_name', Key='file.txt')

# Copy object within bucket
s3.copy_object(Bucket='bucket_name', CopySource='bucket_name/file.txt', Key='file_copy.txt')

# Get presigned URL for object
url = s3.generate_presigned_url('get_object', Params={'Bucket': 'bucket_name', 'Key': 'file.txt'}, ExpiresIn=3600)
print(url)

```

#### EC2 Operations

```python
# List instances
instances = [instance.id for instance in resource.instances.all()]

# Start instance
instance_id = 'your_instance_id'
instance = resource.Instance(instance_id)
instance.start()

# Stop instance
instance.stop()

# Terminate instance
instance.terminate()
```

#### Lambda Operations

```python
# List functions
functions = [func['FunctionName'] for func in client.list_functions()['Functions']]

# Invoke function
response = client.invoke(FunctionName='function_name', InvocationType='RequestResponse', Payload='{}')

# Create function
response = client.create_function(
    FunctionName='function_name',
    Runtime='python3.8',
    Role='arn:aws:iam::123456789012:role/service-role/role_name',
    Handler='filename.handler_name',
    Code={
        'S3Bucket': 'bucket_name',
        'S3Key': 'object_key'
    }
)

# Delete function
client.delete_function(FunctionName='function_name')
```

#### SQS Operations

```python
# List queues
queues = [queue.url for queue in client.list_queues()['QueueUrls']]

# Send message
client.send_message(QueueUrl='queue_url', MessageBody='message_body')

# Receive message
response = client.receive_message(QueueUrl='queue_url')
message = response['Messages'][0]

# Delete message
client.delete_message(QueueUrl='queue_url', ReceiptHandle=message['ReceiptHandle'])
```

#### DynamoDB Operations

```python
# List tables
tables = [table.name for table in client.list_tables()['TableNames']]

# Create table
client.create_table(
    TableName='table_name',
    KeySchema=[
        {'AttributeName': 'primary_key', 'KeyType': 'HASH'},
        # Add more key schemas if needed
    ],
    AttributeDefinitions=[
        {'AttributeName': 'primary_key', 'AttributeType': 'S'},
        # Add more attribute definitions if needed
    ],
    ProvisionedThroughput={
        'ReadCapacityUnits': 5,
        'WriteCapacityUnits': 5
    }
)

# Put item
client.put_item(
    TableName='table_name',
    Item={
        'primary_key': {'S': 'value'},
        # Add more item attributes as needed
    }
)

# Get item
response = client.get_item(TableName='table_name', Key={'primary_key': {'S': 'value'}})
item = response['Item']

# Delete item
client.delete_item(TableName='table_name', Key={'primary_key': {'S': 'value'}})
```

#### SNS Operations

```python
# List topics
topics = [topic['TopicArn'] for topic in client.list_topics()['Topics']]

# Create topic
topic_arn = client.create_topic(Name='topic_name')['TopicArn']

# Publish message
client.publish(TopicArn=topic_arn, Message='message_body')

# Subscribe to topic
subscription_arn = client.subscribe(
    TopicArn=topic_arn,
    Protocol='email',
    Endpoint='email@example.com'
)['SubscriptionArn']

# Unsubscribe from topic
client.unsubscribe(SubscriptionArn=subscription_arn)
```

#### IAM Operations

```python
# List users
users = [user.name for user in client.list_users()['Users']]

# Create user
client.create_user(UserName='user_name')

# Delete user
client.delete_user(UserName='user_name')

# List roles
roles = [role['RoleName'] for role in client.list_roles()['Roles']]

# Create role
client.create_role(
    RoleName='role_name',
    AssumeRolePolicyDocument='{"Version": "2012-10-17", "Statement": [{...}]}'
)

# Delete role
client.delete_role(RoleName='role_name')
```

