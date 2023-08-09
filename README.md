I am creating a native docker image with the following command.

Docker Image: spring-boot:build-image -P native


Then I run my application with docker run. Then I am getting the following error.


2023-08-08T17:55:58.544Z  WARN 1 --- [           main] o.s.c.support.GenericApplicationContext  : Exception encountered during context initialization - cancelling refresh attempt: org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'binderClientFactoryCustomizer': Unexpected exception during bean creation
2023-08-08T17:55:58.544Z  WARN 1 --- [           main] w.s.c.ServletWebServerApplicationContext : Exception encountered during context initialization - cancelling refresh attempt: org.springframework.context.ApplicationContextException: Failed to start bean 'inputBindingLifecycle'
2023-08-08T17:55:58.544Z  INFO 1 --- [           main] o.s.i.endpoint.EventDrivenConsumer       : Removing {logging-channel-adapter:_org.springframework.integration.errorLogger} as a subscriber to the 'errorChannel' channel
2023-08-08T17:55:58.544Z  INFO 1 --- [           main] o.s.i.channel.PublishSubscribeChannel    : Channel 'application.errorChannel' has 0 subscriber(s).
2023-08-08T17:55:58.544Z  INFO 1 --- [           main] o.s.i.endpoint.EventDrivenConsumer       : stopped bean '_org.springframework.integration.errorLogger'
2023-08-08T17:55:58.546Z  INFO 1 --- [           main] o.apache.catalina.core.StandardService   : Stopping service [Tomcat]
2023-08-08T17:55:58.583Z ERROR 1 --- [           main] o.s.b.d.LoggingFailureAnalysisReporter   :

***************************
APPLICATION FAILED TO START
***************************

Description:

A component required a bean named 'outerContext' that could not be found.


Action:

Consider defining a bean named 'outerContext' in your configuration.