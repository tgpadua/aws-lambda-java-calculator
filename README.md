# AWS Lambda Java Calculator
Sample Java project on AWS Lambda 

### local test
sam local invoke -e events/test.json

### local debug 
sam local invoke -e events/test.json -d 5005

_Note: (IntelliJ) Run -> Debug... -> Remote JVM Debug_

### deploy on AWS
sam deploy --stack-name java-calculator --guided

### monitoring logs
sam logs --stack-name java-calculator --tail

### invoke lambda api
aws lambda invoke --function-name java-calculator --payload file://events/test.json --cli-binary-format raw-in-base64-out /dev/stdout

### cleanup
sam delete

### Ref
https://docs.aws.amazon.com/lambda/latest/dg/lambda-java.html