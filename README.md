# Alexa Guitar Ace

An Alexa Skill that helps you tune and plays chords on your guitar

## Setup

### Lambda
1. Go to the [AWS Management Console / Lamda](https://console.aws.amazon.com/lambda/)
2. Create Lambda function
3. Go to "Configure triggers"
4. Select "Alexa Skills Kit"
5. Go to "Configure function"
6. Use these settings:
 - Name: alexa-guitar-ace
 - Runtime: Node.js 4.3
 - Handler: index.Handler
 - Role: Choose an existing Role
 - Existing role: lambda_basic_execution
7. Proceed to review and then click "Create function"
8. Take note of the Lambda function ARN

### Alexa
1. Go to [Alexa Skills Kit Developer Console](https://developer.amazon.com/edw/home.html#/skills/list)
2. Click "Add a New Skill"
3. On Skill Information step, use these settings:
 - Name: Guitar Ace
 - Invocation Name: guitar ace
4. On Interaction Model step, use values from /speechAssets directory in this repository
5. On Configuration step, specify "AWS Lambda ARN" as Service Endpoint Type, Choose "North America" as the geographical region, and enter the Lambda ARN
6. Click "Save"

## Deploy

Run `npm run deploy-lambda`

## Usage Examples
- "Alexa, ask guitar ace to help me tune my guitar."
- "Alexa, ask guitar ace to play C7."