[Main Page](../README.md)

# Reading Notes 16

# Serverless Functions

## What is Serverless Computing? (through Pros and Cons Section)

[Source](https://www.ibm.com/cloud/learn/serverless)

Serverless - "A cloud computing execution model"

- provides required computing resources to run an app on demand or in response to a specific event

- scales the computing resources in response to demand whether it be up or down for increased or decreased demand

Uses the cloud provider for all backend cloud infrastructure and operations tasks. This allows more time for developers to focus on the front-end code and logic

The servers are "invisible" to customers, they do not see, manage, or interact with them.

In 2014, Amazon Web Services introduced serverless with AWS Lambda.

Other cloud service providers include:

- Microsoft Azure (Azure Functions)

- Google Cloud (Google Cloud Functions)

- IBM Cloud (IBM Cloud Code Engine)

Pros and Cons of Serverless:

Pros:

- Developers have more time to focus on writing code

- Customers only pay for execution, from when the request is made to when the execution finishes

- Any language or framework can be used

- simplifies DevOps cycles

- parallel processing is faster and more cost effective than other compute forms

Cons:

Some applications will have technical and business trade offs to consider

- Stable or predictable workloads

- Cold starts

- Monitoring and debugging

- Vendow lock-in

---