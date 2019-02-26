# Microservice Sample project using MSF4J framework

MSF4J - Microservices Framework for Java is a WSO2 framework for developing microservices. It is compatible with other spring based jars
and work together.


## Dependency

```
<dependency>
	<groupId>org.wso2.msf4j</groupId>
	<artifactId>msf4j-spring</artifactId>
	<version>2.0.0</version>
</dependency>
```

## Overview

The sample microservice is a Account Inquiry service which will take account number as input and fetch the account details from MySql database and send the response to client.

![Image of Workflow](https://github.com/praveen9800/microservice-sample-msf4j/blob/master/accountinquiry_msf4j.png)


## Configuring MSF4J through Spring

### 1. Changing HTTP port

```
@Configuration
public class TransportConfiguration {

    @Bean
    public HTTPTransportConfig http(){
         return new HTTPTransportConfig(8090);
     }

}
```
