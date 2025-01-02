---
title: Lambda Web Adapter
nav_order: 2
parent: CCCBuilder Backend
---

# Lambda Web Adapter

Initially, the backend was actually separated into three Lambda functions, all written in Python. We wanted to implement respose streaming so that the frontend could display articulations or requirements as the backend fetched them, which made the interface more responsive. However, at the time of writing, AWS currently does not support streaming responses from Lambda functions written in Python. 

To solve this issue, we decided to use the Lambda Web Adapter. By packaging a web application into a Docker container with some specific confirguration, a single Lambda function using the web adapter can run the entire web application when invoked. We opted to use FastAPI because there were several examples on GitHub that used it. 