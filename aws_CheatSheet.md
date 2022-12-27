	#Config
		#Create profiles
			aws configure --profile profilename
		
		#Specify AWS region
			aws configure region (region-name)

	#API Gateway
		#List API Gateway IDs and Names
			aws apigateway get-rest-apis |jq -r '.items[]| .id+" "+.name'
		
		#List API Gateway keys
			aws apigateway get-api-keys |jq -r '.items[]| .id+" "+.name'
		
		#List API Gateway domain names
			aws apigateway get-domain-names | jq -r '.items[]| .domainName+" "+.regionalDomainName'
	
	#Amplify
		#List Amplify apps and source repository
			aws amplify list-apps | jq -r '.apps[] | .name+" "+.defaultDomain'

	#CloudFront
		#To get a list of the CloudFront distributions 
			aws cloudfront list-distributions
	
	#CloudWatch
		#Provide information about the alarm named "myalarm"
			aws cloudwatch describe-alarms --alarm-names "myalarm"

	#DynamoDB
		#List DynamoDB tables
			aws dynamodb list-tables
				
				#To limit page size
					aws dynamodb list-tables \
    						--page-size 1
				#To limit the number of items returned
					aws dynamodb list-tables \
    						--max-items 2
	#EBS
		#Complete a Snapshot
			aws ebs complete-snapshot (snapshot-id)
		
	#EC2
		#List Instance ID, Type and Name
			aws ec2 describe-instances
		#Create a key pair 
			aws ec2 create-key-pair --key-name MyKeyPair --query 'KeyMaterial' --output text > MyKeyPair.pem
				#Options include.
				--key-name = Your key name
				--query = A JMESPath query to use in filtering the response data
				--output = The formatting style for command output. (json | text | table)
	#IAM
		#To create the IAM group
			aws iam create-group --group-name

	#Amazon S3
		#Create a bucket
			aws s3 mb <target> [--options]
				
				#Create a bucket in specified region
					aws s3 mb bucket_name --region region_name
	#Amazon SNS
		#Get the list of subscribed sns
			aws sns list-subscriptions
		#Get the list of topics
			aws sns list-topics
		#Create a topic with the specified name
			aws sns create-topic --name my-topic
		#Subscribe to a topic
			aws sns subscribe --topic-arn arn:aws:sns:us-west-2:123456789012:my-topic --protocol email --notification-endpoint saanvi@example.com
				#Options include.
				--topic-arn = The ARN of the topic you want to subscribe to
				--protocol = The protocol that you want to use
				--notification-endpoint = The endpoint that you want to receive notifications
		#Publish to a topic and sends the message "Hello World!" to all subscribers of the specified topic
			aws sns publish --topic-arn arn:aws:sns:us-west-2:123456789012:my-topic --message "Hello World!"
		#Unsubscribe from a topic
			aws sns unsubscribe --subscription-arn arn:aws:sns:us-west-2:123456789012:my-topic:1328f057-de93-4c15-512e-8bb22EXAMPLE
		#Delete a topic
			aws sns delete-topic --topic-arn arn:aws:sns:us-west-2:123456789012:my-topic
		
	#Amazon AWS
		#Create alias for frequently-used commands
			$ whoami = sts get-caller-identity
