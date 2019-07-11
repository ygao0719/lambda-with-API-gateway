# Lambda with API gateway
A user should be able to find the first repeated word in a sentence by visiting a URL.
That URL should use API Gateway to call a Lambda function that finds the first repeated word in a sentence.

##  link to API Gateway
https://8fkj332yb5.execute-api.us-west-2.amazonaws.com/beta?string=
- Type in a string after =, then you will get the first duplicated word in that string.

## Issues
1. First I had java run time issue. I used Java 12 in my intellij but Lambda is using Java 8.
So I have to downgrade my intellij to Java 8. Also in the build.gradle tell gradle to use Java 8.(Thanks 
to my instructor).
2. In the AWS API gateway, when you set up Integration Request, Content-Type has to be application/json. I thought we were 
passing the string as input, so I use application/string which is not working. 