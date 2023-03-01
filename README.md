# AWS Lambda Java Calculator
Sample Java project on AWS Lambda 

### SAM CLI - Project Build
```bash
sam build
```

### SAM CLI - Local Testing
```bash
sam local invoke -e events/test.json
```

### SAM CLI - Local Debugging
```bash
sam local invoke -e events/test.json -d 5005
```

_Note: (IntelliJ) Run -> Debug... -> Remote JVM Debug_

### SAM CLI - Lambda Deployment
```bash
sam deploy --stack-name java-calculator --guided
```

### SAM CLI - Log Monitoring
```bash
sam logs --stack-name java-calculator --tail
```

### AWS CLI - Lambda Invocation
```bash
aws lambda invoke --function-name java-calculator --payload file://events/test.json --cli-binary-format raw-in-base64-out /tmp/java-calculator.out
```

### SAM CLI - Delete Deployment
```bash
sam delete
```

### Ref
https://docs.aws.amazon.com/lambda/latest/dg/lambda-java.html