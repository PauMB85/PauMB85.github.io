---
layout: post
title: AWS Lambda. Go to serveless
date: 2017-12-13 23:44:00 +0200
description: # description (optional)
img:  # Add image post (optional)
tags: [cloud,aws lambda, serveless]
---

Hi everyone!!

In this post, I talk about __AWS Lambda__, where AWS wants to convert a core of API Serveless.
I'm going to write a serie of post of this topic, 
1. The firts post I will talk about what is it.
2. In the second post I show you how to delevop my firts AWS Lambda and how to deploy it.
3. And the last post I develop a CRUD operation with DynamoDB and I tell you about good practise to develope it.

But... What is AWs Lambda??

AWS Lambda is a cloud services where you can upload your code and this is executed when there is a event. The main objective of AWS is offers you a back-end without
provisioning or managing any server. This service run your code on high-available compute
infraestructure and autoscales automatically.

![How works AWS Lambda]({{site.baseurl}}/assets/img/aws-lambda/FuncionamientoAWSLambda.png)

You can develop a Lambda function in some programming lenguajes like *Node.js, Python, Java or C#*

Its main advantatges to use AWS Lamda are:

* Custom back-end services. The user only need to develop software and they can forget about the servers.
* Automated managed. The user don't need to update or keeping servers.
* Fault tolerance. AWS Lambda offers a high-disponibility to user's services. All the services always are avialible.
* Automatic scale. AWS Lambda can autoscale in function the request, with this method always is aviabla and the customers can used his services in any time.


Now you must thinking... what are its uses??
There are a lot of kind uses like:
1. Data processing in real time.
2. Stream processing in real time.
3. Extract, transform and load.
4. Movil, web or IoT back-end.

![Movil Back-end]({{site.baseurl}}/assets/img/aws-lambda/arquitecturaMovilAWSLAmbda.png)