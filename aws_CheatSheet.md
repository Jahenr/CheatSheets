

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
		
	
