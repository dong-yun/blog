---

layout: post 
title: "AWS Lambda for Serverless Java Developers: What’s in It for You?" 
date: 2016-09-03 11:26:00 +0900
categories: agile
tags:
- AWS
- Lamda

---

-	원문 : [AWS Lambda for Serverless Java Developers: What’s in It for You?](https://www.javacodegeeks.com/2016/08/aws-lambda-serverless-java-developers-whats.html)


How can serverless computing help your production infrastructure?
------------

serverless computing architecture는 server 쪽 주요 컴포넌트에 포커스가 맞춰진 이래 최근 몇년간 주목을 받아고 있다.
이 architecture 는 조금 다른 접근을 하고 있다.
이 기사는 serverless 로 가는 것이 무엇인지 설명하고 어떻게 당신의 application 에 도움이 될지 이해하는데 도움을 주려한다.


The Cloud’s New Clothes
------------

serverless computing 의 컨셉은 코드 배포에 대해 이야기 한다. server 가 아니라.
이 이야기는 당신의 app 실행과 전체에 대해 server 를 비릴 수 있다고 의미하기 때문에, 처음에는 좀 혼란스러울 수 있다.
하지만 상상하는 그런 일은 일어나지 않는다.
servers 를 구매/관리/증가 하는 부분은 cloud 가 VM 상으로 제공한다.
그래서, 여전히 server 는 필요하다, 하지만 이 새로운 모델은 당신이 책임으로 부터 자유롭게 한다.
다른 말로 하자면, server 에 배포하거나 software 를 install 하는 것에 번거로움이 없다는 얘기다.
기본적으로, cloud service 와 computer 를 관리하는 것만 하면 된다.

![Serverless Architecture Diagram. Source: Amazon](http://www.javacodegeeks.com/wp-content/uploads/2016/08/Serverless-Architecture-Diagram.png)

Enter AWS Lambda
------------

This model was first introduced by Amazon, as AWS Lambda in 2014. 
The company was the first to offer the serverless service, as part of the Amazon Web Services suite.
AWS Lambda is based on an event-driven platform, triggered by events such as signups, updates and so on. 
When an event happens, it will call the relevant functions that in turn, will run the code. All this, while managing and computing the resources required to run and using only them.
In other words, the basic workflow stays the same: write code, upload it to a server for it to run, and remove the concerns about response time, operations and so on.
AWS Lambda is sometimes referred to as Function as a Service (FaaS), 
 since the events trigger the relevant functions needed to proceed the requests, allowing us to run our functions without the hassle behind it.
Along with FaaS, the serverless architecture is also known as Backend as a Service (BaaS), 
 that removes a significant part of the database administration overhead, and provide authorization for different users and levels.
Tim Wagner, General Manager of AWS Lambda shared a diagram that illustrates the components and their connections: 
 a Lambda function as the compute resource (“backend”) and a mobile app that connects directly to it, 
 plus Amazon API Gateway to provide an HTTP endpoint for a static Amazon S3-hosted website:

Taking Care of Your Code
--------------
AWS Lambda’s main goal is allowing developers to build smaller, on-demand and event-responsive applications in a simple way. It works for you and manages the “compute fleet” that balance memory, CPU, network, apply security patches, monitor health and any other resources and actions needed.
A nice way to look at it is as an outsourcing service. Not only it “relocates the IT”, it can even help you reduce operational costs, since you can remove infrastructure costs and even cut down on the amount of team members needed to maintain the servers.
Speaking of costs, you only pay for what you use, based on the number of requests for your functions and the time your code executes. And it’s important to state that the free tier includes 1M free requests per month and and up to 3.2 million seconds of compute time per month.
The calculation of each request is counted from when it starts executing as a response to an event or invoke call. And that also includes tests from the console.
According to Amazon, AWS Lambda is the platform for many application scenarios. But of course, there’s a catch, this statement is only relevant to the languages supported by AWS Lambda: Node.js, Java, and Python.
On the bright side, building AWS Lambda functions with Java can be done with the tools you already know, Maven or Gradle, and the build process remains pretty much the same.

Show Me the Code
--------------
Invoking an AWS Lambda function is pretty easy after a basic setup and you can view the full explanation here.
It includes defining POJOs that represent the input and output JSON, specifying an interface that represents our microservice and annotate it with the name of the Lambda function to invoke when it’s called.
The next step will be using the LambdaInvokerFactory to create an implementation of this interface. This will allow us to make calls to the service that’s running on Lambda. Then we can simply invoke our service using this proxy object, like… counting cats:

```
CountCatsInput input = new CountCatsInput();
input.setBucketName("pictures-of-cats");
input.setKey("three-cute-cats");
 
int cats = catService.countCats(input).getCount();
``` 


Before You Start…
---------------
Of course, nothing is perfect and the option to focus mainly on code comes with a few drawbacks. Since it’s still a pretty new technology, it’s easy finding a list of issues that the users are not quite happy about, such as:
Control – You’re “handing away” your servers in hope your cloud host will handle them the best way possible. But you might experience major issues that you’ll have to sit back and wait for them to work out, and that may even include downtime and unhappy customers.
Locked-In – Speaking of handing everything to your cloud host, using AWS Lambda means you have to use AWS. It might not be an issue right now, but it will become one if you ever think about moving to Google or simply using your own servers.
Flexibility – You won’t be able to login to compute instances, or customize the operating system or language runtime.
Security – Using a 3rd party also means using his security. We’re not saying AWS is not secure, but you’re passing on this responsibility completely to a 3rd party which can be less than ideal. .
Monitoring – With AWS Lambda you can monitor and debug your system only with the in-house tool, CloudWatch. While you can still create custom alarms, view request rates and error rates – it’s a pretty basic tool, and it might not help you understand the root cause of your problems.
And that’s just a small (but important) part of the downsides this architecture has. It’s also important to point out that if you already have an application and you would like to migrate it to a serverless architecture, you might find yourself writing it from scratch. So you might have to think it over or simply backlog it to the next new app you’re planning on working on.

Final Thoughts
------------

Amazon 이 AWS에서 serverless를 먼저 시작했고 이제는 Microsoft, Google, IBM 등과 규모가 작은 회사 혹은 startup 회사에서도 하고 있다.
내기를 하자면 serverless 는 미래이다. cloud computing 진화의 다음단계 이다.
우리 스스로보다 cloud 와 provider 에게 신뢰를 줄 수 있다.
지금은, 쓰고있는 cloud 나 on-premise server (사내 서버) 에 있는 것이 낫다.
이건 여전히 새로운 기술이고 아직 Amazon, Google 에서도 좀 충돌이 있으며 좀 더 다듬어야 한다.
아직 걸음마 단계일 수 있다. 하지만, 좋던 싫던 이 방향으로 향하고 있다. 
