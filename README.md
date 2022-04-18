# graphql-springboot-book-demo

### Getting started with Spring Boot
This is a tutorial I am spinning up and following to create a GraphQL Server in Java.  It requires some Spring Boot and Java knowledge and the focus of this project is how to easily and quickly developing a GraphQL server in Java.

### GraphQL in 3 minutes
GraphQL is a query language to retrieve data from a server. It is an alternative to REST, SOAP or gRPC in some way.
Schema files are not JSON (even though it looks deliberately similar), but is a GraphQL query.

This project focuses on how to implement a GraphQL server in Java.

### GraphQL Java Overview
GraphQL Java is the Java (server) implementation for GraphQL. The are several repositories in the GraphQL Java Github org. The most important one is the GraphQL Java Engine which is the basis for everything else.

GraphQL Java Engine itself is only concerned with executing queries. It doesn't deal with any HTTP or JSON related topics. For these aspects, we will use the GraphQL Java Spring Boot adapter which takes care of exposing our API via Spring Boot over HTTP.

The main steps of creating a GraphQL Java server are:
 * Defining a GraphQL Schema.
 * Deciding on how the actual data for a query is fetched.

### Static Types in GraphQL
One very important property of GraphQL is that it is statically typed: the server knows exactly the shape of every object you can query and any client can actually "introspect" the server and ask for the so called "schema". The schema describes what queries are possible and what fields you can get back. 

(Note: when we refer to schema here, we always refer to a "GraphQL Schema", which is not related to other schemas like "JSON Schema" or "Database Schema")

### Create a Spring Boot app
The easiest way to create a Spring Boot app is to use the "Spring Initializr" at https://start.spring.io/.

Select:
 * Gradle Project
 * Java
 * Spring Boot 2.1.x

For the project metadata we use:
 * Group: com.graphql-java.tutorial
 * Artifact: book-details
 * As dependency, we just select Web.

A click on Generate Project will give you a ready to use Spring Boot app. All subsequently mentioned files and paths will be relative to this generated project.
