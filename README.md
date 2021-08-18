# Red-Serverless

## Requriements
* [AWS cli](https://aws.amazon.com/cli/)
* [Serverless Framework](https://www.serverless.com/)

## Prerequisites
* Setup a internet facing Cobalt Strike teamserver with port 443 open

## Serverless Deploy
* Deploy the AWS serverless infrastructure \
`sls deploy --teamserver "<domain name/IP>"`

```
$ sls deploy --teamserver "<domain name/IP>"

Serverless: Packaging service...
Serverless: Excluding development dependencies...
Serverless: Uploading CloudFormation file to S3...
Serverless: Uploading artifacts...
Serverless: Uploading service red-serverless.zip file to S3 (1.05 KB)...
Serverless: Validating template...
Serverless: Updating Stack...
Serverless: Checking Stack update progress...
..............
Serverless: Stack update finished...
Service Information
service: red-serverless
stage: api
region: us-east-1
stack: red-serverless-api
resources: 11
api keys:
  None
endpoints:
  ANY - https://1234567890.execute-api.us-east-1.amazonaws.com/api/{all+}
functions:
  redirector: red-serverless-api-redirector
layers:
  None
Serverless: Removing old service artifacts from S3...
Serverless: Deprecation warning: Detected unrecognized CLI options: "--teamserver".
            Starting with the next major, Serverless Framework will report them with a thrown error
            More Info: https://www.serverless.com/framework/docs/deprecations/#UNSUPPORTED_CLI_OPTIONS
```
