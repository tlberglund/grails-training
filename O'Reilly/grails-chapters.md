# Mastering Grails 101

## Intro

Meet your instructors and learn the planned outline of the course.

## Grails: What and Why

Grails is a request-based, convention-over-configuration framework that uses the Groovy language for development. Learn where and how these ideas emerged in the past several years of web framework development, and why our choice of abstractions matters in a framework.

## An Introduction to Groovy

Groovy is a dynamic language of the JVM designed to interoperate well with Java code and to be easy for Java developers to learn. It emphasizes essence over ceremony, attempting to remove the boilerplate so common to Java.

## Groovy Hello, World

We begin by looking at some important features of Groovy syntax that differentiate it from Java.

## Groovy Strings

We look at two interesting features of Groovy strings: string interpolation and multi-line heredoc strings.

## Groovy Collections

Groovy provides a literal syntax for declaring lists and maps, and enhances list and map types with a concise syntax for reading and writing these data structures.

## Groovy Closures

We look at closures, a compelling feature of Groovy that allows us to declare code blocks that we can pass as parameters to methods as parameters.

## Groovy Beans

Groovy provides a concise property syntax that avoids the usual Java boilerplate setters and getters. When constructing new objects, we can use the default map constructor for an even more concise way to initialize Groovy bean properties.

## Groovy Metaprogramming

Grails relies heavily on Groovy's metaprogramming capabilities, so we take a quick look at them here. We look at how reflection works in Groovy, what the methodMissing() method is, and how to add methods to any class at runtime.

## Installing Grails

We briefly review the steps involved in installing Grails, then create a new Grails application and examine its directory structure. We also explore the implications of Grails being a full-stack framework.

## Creating Domain Classes

Grails uses Hibernate for database persistence, but hides much of Hibernate's complexity from the user. Here we begin our look at GORM, the Grails Object-Relational Mapping layer, by creating a domain class and configuring it with some constraints.

## Generating Scaffolding

Having created a simple domain model, we now use Grails' scaffolding feature to create a fully-functional CRUD user interface.

## Configuring Grails

Grails uses the in-memory H2 database by default. We will reconfigure Grails to use MySQL alternatively, and along the way we'll explore the Grails configuration file format, Grails run-time environments, and Grails dependency management.

## Domain Class Relationships

Now that our application has a simple user interface and durable database persistence, we can enrich the domain model to include two classes with a one-to-many relationship between them. In the process, we learn how to work with statically generated scaffolding when the domain is rapidly changing.

## Groovy Server Pages

Grails provides an integrated template system in the form of Groovy Server Pages, or GSPs. We'll look at where GSPs go in a Grails project, how views, layouts, and templates work together, and how controller actions delegate to GSPs to stream markup to the client.

## A Closer Look at Controllers

We have been using controllers in the form of scaffolding and in our discussion of GSPs, but we now turn our attention to controllers as a first-class citizen of a Grails app. We will create a controller action to perform a new kind of processing on our domain, and even override the default Grails URL mapping to match a URL scheme of our own design.

## Wrapping Up

We wrap up our introduction to Grails, looking back on the Groovy language, the principles behind Grails as a framework, Grails support for domain modeling, HTML views, and controller logic.
