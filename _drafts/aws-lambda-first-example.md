---
layout: post
title: AWS Lambda. My First Function
date: 2018-02-28 23:44:00 +0200
description: # description (optional)
img: aws-lambda/lambdaAWS.jpg # Add image post (optional)
tags: [cloud, aws lambda, serveless, Node js]
---



Hi everyone!!

In my [previous post]({{site.baseurl}}/aws-lambda-what-is/) I told you about what is AWS Lambda and how to use it.
In this post, my propouse is to explain you how to create a Lambda Function and its main concepts.

### Step 1. Create the function.
On your console, you can choose __Lambda__ in the section of __Compute__ or you can search it in the search bar. When click on Lambda you can view this page,if you don't have any lambda function.

![First time in lambda]({{site.baseurl}}/assets/img/aws-lambda/FuncionamientoAWSLambda.png)

Otherwise, you wath this other if you have some lambda function.

![I have functions]({{site.baseurl}}/assets/img/aws-lambda/FuncionamientoAWSLambda.png)

Now, we click on __*Create function*__ and open a new page, where we can select 3 options.

* Author from scratch. In this section, we create our function on a blank method.
* Blueprints. This are examples that you can choose to know how works.
* Serverless Application Repository. In this section, you can search some apps published by developers, companies,...

![Options to select]({{site.baseurl}}/assets/img/aws-lambda/FuncionamientoAWSLambda.png)

In this case, select the option *Author from scratch* and fill the form like this:

![Fill the form]({{site.baseurl}}/assets/img/aws-lambda/FuncionamientoAWSLambda.png)

Now, We create our firts lambda.

### Step 2. Code the function
In this section we can see some blocks about how to configure our lambda function. But in our case, we only use the *Function code* section. Here is where we code our function

![Image function code]({{site.baseurl}}/assets/img/aws-lambda/FuncionamientoAWSLambda.png)

To work with lambda, we need to implement the *handler* function, that AWS Lambda can invoke when the service executes our code. The syntax of this function is compose by 4 parts:
* Event. AWS Lambda uses this parameter to pass the data to the handler.
* Context. Provide the runtime information of the Lambda function that is executing.
* Callback. Returns the information to the caller.
* handler. This is AWS Lambda's name invoke to execute the function.

In our example, only print the value of the event and the context.

```node
exports.handler = (event, context, callback) => {
    console.log('this is the event: ' + event);
    console.log('this is the context: ' + context);
    callback(null, 'Hello from Lambda');
};
```
And finally *save* it.

### Step 3. Test our function

In this step, we test the function manually and watch the result.
To test it, in the *Configure test events* and select *Create new Test event*, enter an *Event name* and save.

When we create the test, select the __Test__ button and watch the result like this:

![Result test function]({{site.baseurl}}/assets/img/aws-lambda/FuncionamientoAWSLambda.png)

The result of our function is divide in three parts:
* Execution result. Indicates execution's state and the output, context's value.
* Summary. Information about the execution.
* Log output. Show the logs that the function generate.

With this example, we learn how to create a function and test it and we have know the main components that affect in the function.

In the next post, we are going to create a function that interactue with other resources like DynamoDB and AWS Gateway. 
