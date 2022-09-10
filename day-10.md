# Day 10 of #100daysofcloud

### Time for AWS Serverless compute. It is all about Lambda this time around for my AWS SAA-C03 certification.

- I learned serverless compute is all about transferring the hassle of installing, managing, and patching underlying instances software to the service provider. This makes the software engineers/developers focus on what they do best, building solutions, writing code, and business logic.
- I learned there are 3 major parts to AWS lambda - the input, the function, and the output
  - The function is simply your code. It is an instance of your lambda.
  - The computing power is based on the memory spec. (min is 128MB, max is 10,240MB) which in turn affects the CPU, network, and disk I/O operations.
  - Other needs (permissions, env. variables, etc) can be specified in the function
  - Java, Go, Nodejs, PowerShell, C#, Python and Ruby are natively supported runtimes. Custom runtime can be used for other programming languages
  - The input is simply invoking the function via a trigger based on a specified event/service call, HTTP endpoint, or direct invocation.
  - Invoking the function can be through AWS management console, CLI, SDK, AWS toolkits, function URL (HTTP endpoint), AWS service, or resource
  - The output is the final stage of a lambda function. It is the result of your function call to a downstream resource, an API call to other AWS services, and so on.
  - Lambda function activities can be monitored and measured via CloudWatch. It is possible to write custom logging and monitoring codes in the function. The most important logging metrics are invocation, performance and concurrency metrics.
- I learned the cost is based on what you use. This can be a number of requests to function, amount of computing power, or duration of running the code (rounded up to 1ms)
- Function timeout determines how long a function should run before termination (min time is 3 seconds, max time is 15 minutes)
- I learned that concurrency of lambda function means how many instances of your function can run to serve more than one event/request at the same time. There are two possible options - reserved and provisioned concurrency
- Reserved concurrency helps to cap the number of concurrent instances of your functions. this is useful to prevent resources from mostly being used by a single function in the entire region. This is free to use
- Provisioned concurrency helps solve the problem of cold-starting/delay of function when it is initialised for the first time. provisioned concurrency solves this problem by already initialising the function and getting it warmed
- There are three methods to invoke service API
  - Synchronous (push-based) model - useful when your application needs to wait for a response
  - Asynchronous (event-based) model - useful for long-running tasks that do not need to wait for a response
  - Stream (poll-based) model - useful to process messages from a stream or queue.

#aws #cloudcomputing #cloud #publiccloud #hyperscaler #terraform #iac #linux #learninpublic
