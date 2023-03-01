# AWS Lambda Java Calculator
Sample Java project on AWS Lambda 

### SAM CLI - Project Build
`sam build`

### SAM CLI - Local Testing
`sam local invoke -e events/test.json`

### SAM CLI - Local Debugging
`sam local invoke -e events/test.json -d 5005`

_Note: (IntelliJ) Run -> Debug... -> Remote JVM Debug_

### SAM CLI - Lambda Deployment
`sam deploy --stack-name java-calculator --guided`

### SAM CLI - Log Monitoring
`sam logs --stack-name java-calculator --tail`

### AWS CLI - Lambda Invocation
`aws lambda invoke --function-name java-calculator --payload file://events/test.json --cli-binary-format raw-in-base64-out /tmp/java-calculator.out`

### SAM CLI - Delete Deployment
`sam delete`

### Ref
https://docs.aws.amazon.com/lambda/latest/dg/lambda-java.html