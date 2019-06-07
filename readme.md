# MicroProfile generated Application

## Introduction

MicroProfile Starter has generated this MicroProfile application for you.

The generation of the executable jar file can be performed by issuing the following command

    mvn clean package

This will create an executable jar file **DemoAPI.jar** within the _target_ maven folder. This can be started by executing the following command

    java -jar target/DemoAPI.jar

To launch the test page, open your browser at the following URL

    http://localhost:8181/DemoAPI/index.html

## Specification examples

By default, there is always the creation of a JAX-RS application class to define the path on which the JAX-RS endpoints are available.

Also, a simple Hello world endpoint is created, have a look at the class **HelloController**.

More information on MicroProfile can be found [here](https://microprofile.io/)










### JWT Auth

Using the OpenId Connect JWT token to pass authentication and authorization information to the JAX-RS endpoint. Specification [here](https://microprofile.io/project/eclipse/microprofile-rest-client)

Have a look at the **JWTClient** class within the test directory which calls the protected endpoint on the server from a Java Main method.
The **ProtectedController** contains the protected endpoint since it contains the _@RolesAllowed_ annotation on the JAX-RS endpoint method.

In order to call the protected endpoint, a separate program (see _JWTClient_) is used to simulate as much as possible a real world situation. A JAX-RS client implementation is used for this purpose to match the selected MicroProfile implementation, with an arbitrary version.
However, any method to send a REST request with an appropriate header will work of course. Please feel free to change this code to your needs.







