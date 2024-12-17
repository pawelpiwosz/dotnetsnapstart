# .NET Lambda SAM Application

This project is a .NET Lambda function application that uses AWS SAM for deployment. The function is designed to update a counter stored in DynamoDB for every request received through API Gateway. 

## Project Structure

```
dotnet-lambda-sam-app
├── src
│   ├── DotnetLambdaFunction
│   │   ├── Function.cs
│   │   ├── FunctionHandler.cs
│   │   ├── aws-lambda-tools-defaults.json
│   │   ├── DotnetLambdaFunction.csproj
│   │   └── Startup.cs
├── template.yaml
└── README.md
```

## Setup Instructions

1. **Prerequisites**
   - .NET SDK (version 6.0 or later)
   - AWS CLI configured with appropriate permissions
   - AWS SAM CLI

2. **Clone the Repository**
   ```bash
   git clone <repository-url>
   cd dotnet-lambda-sam-app
   ```

3. **Build the Project**
   Navigate to the `src/DotnetLambdaFunction` directory and run:
   ```bash
   dotnet build
   ```

4. **Deploy the Application**
   Use the SAM CLI to deploy the application:
   ```bash
   sam deploy --guided
   ```

5. **Test the API**
   After deployment, you can test the API using tools like Postman or curl. The endpoint will be provided in the output of the deployment command.

## Usage

Send a request to the API Gateway endpoint to increment the counter in DynamoDB. Each request will update the counter value.

## Cold Start and SnapStart Testing

This project is set up to test the cold start performance of the Lambda function and to evaluate the benefits of AWS Lambda SnapStart for Java functions.

## License

This project is licensed under the MIT License. See the LICENSE file for details.