# Full-Stack Notes

## Contents

I. <a name="top">Core Technologies</a>

1. [Java](#java)
2. [Maven](#maven)
3. [SQL](#sql)
4. [HTML & CSS](#html-css)
5. [JavaScript](#javascript)
6. [XML](#xml)
7. [Servlets](#servlets)
8. [AWS](#aws)
9. [Typescript](#typescript)
10. [DevOps](#devops)
11. [Hibernate](#hibernate)
12. [Spring](#spring)
13. [Web Services](#web-services)
14. [Microservices](#microservices)
15. [Docker](#docker)
16. [Kubernetes](#kubernetes)

II. Appendix

1. Command Line
2. Git
3. IDEs
4. Architecture and Design
5. Test Driven Design
6. Agile
7. Thymeleaf
8. GoogleMapsApi
9. Authentication & Authorization
10. Connecting it all
11. Logging
12. Learning from tutorials
13. Reading Stack Overflow answers
14. Clean Coding
15. Markdown
16. Cryptography

## <a name="java">Java</a>
&nbsp;[[top]](#top)

Java is a programming language and computing platform first released by Sun Microsystems in 1995. It is advertised as being fast, secure, and reliable. [Source](https://java.com/en/download/faq/whatis_java.xml).

Official documentation: https://docs.oracle.com/en/java/

### Java Basics

#### Packages

There can be at most one package statement per Java source file. It must be the first statement in the file.

#### Variables

Instance variables and static variables receive a default value if not explicitly initialized. So, primitives get a value equivalent to 0. Boolean default is false. Local variables must be initialized.

##### Local Variables

A local variable (a.k.a. automatic variable) means a variable declared in a method. They do not have accessibility. They are only accessible from the block in which they are declared. You must initialize them explicitly.

You cannot specify visibility of local variables. They are always only accessible within the block in which they are declared.

### Object-Oriented Concepts

### Data Types

#### Arrays

An array of length zero is a valid object.

#### Floats

Precision is lost when float or double are converted into type int.

### Operators and Decision Constructs

`instanceof` : tests whether object is instance of specified type. Returns true or false.

### Constructors

Calls to a super class's constructor must be placed as the first statement in the constructor.

If you do not write a constructor for a class, the compiler will automatically create one for it. This is the default constructor and it takes no arguments.

### Working with Methods

### Working with Inheritance

Members of a class declared private are not inherited by subclasses. Only members of a class declared protected or public are inherited by sublclasses declared in packages outside of the one where they were declared. Constructors and static initializers are not members and therefore are not inherited.

##### Overriding

An overriding method must have the same parameters as the base class method. Private methods are not inherited. Final methods cannot be overridden.

##### Overloading

### Handling Exceptions

You can declare anything that is a Throwable or subclass of Throwable in the throws clause.

Finally is always executed.

#### System.exit()

Calling `System.exit` causes the JVM to exit.

### Lamda Expressions

#### Functional interface

A functional interface is an interface with one, and exactly one, abstract method. Because it contains only one abstract method, its name may be omitted when implemented with a lambda expression. It may have other default or static methods.

### Working with Java API

### String class

#### StringBuilder

There is no `reverse ()` method for StringBuilder. You must use either `StringBuffer` or `StringBuilder` for that.

#### Date-Time API

The Date-Time API uses the calendar system defined in ISO-8601 as default calendar. Most of the actual date related classes in the Date-Time API (e.g. LocalDate, LocalTime, and LocalDateTime) are immutable.

### Garbage Collection

### Java APIs

#### Java Database Connectivity (JDBC)

## <a name="maven">Maven</a>
&nbsp;[[top]](#top)

Apache Maven is a software management and comprehension tool based on the concept of a project object model (POM). It began as an attempt to simplify Java build processes and has the primary goal of allowing a developer to comprehend the complete state of a development effort in the shortest period of time.

### Dependencies

A dependency is an artifact that Maven will include as part of the build. It is analogous to including the .jar files in your class path for an Eclipse build.

### Repositories

A Maven respository is the directory where all project .jars, library .jars, and plugins are stored. The maven local repository is a folder on your machine that gets created when you run any maven command for the first time.

Official Maven site: https://maven.apache.org/index.html

## SQL
&nbsp;[[top]](#top)

Structured Query Language is a domain-specific language used in programming for designing and managing data held in a relational database management system (RDBMS). It is particularly useful for handling structured data.

### Normalization

Normalization means organizing data in the database to eliminate redundancy and inconsistent dependencies. There are six normal forms, though a typical organization may only use the first three.

1. Atomic/Granular - divide up each attribute until it cannot be divided anymore. Create a Primary Key and identify each set of related data with the prinary key. (1NF)
2. Start with 1NF. Every non-key attribute is dependent on the primary key as a whole. No partial dependencies. I.e., if there is a composite key, each non-key attribute must rely on the entire composite key, not just some of it. (2NF)
3. Must be in 2NF. Every non-key attribute is not dependent on any non-key attribute. "

In other words, these three can be said as:
_"The key, the whole key, and nothing but the key, so help me Codd."_

### SQL Sublanguages

  * DML: data manipulation language (SELECT, INSERT, UPDATE, DELETE)
  * DQL: data query language (SELECT)
  * DDL: data definiion language (CREATE, ALTER, TRUNCATE, DROP)
  * TCL: transaction control languages

Postgresql official documentation: https://www.postgresql.org/docs/

## <a name="html-css">HTML & CSS</a>
&nbsp;[[top]](#top)

Hypertext Markup Language (HTML) is the standard markup language for documents designed to be displayed in a web browser. It describes the structure of a web page semantically and originally included cues for a documents appearance.

Cascading Style Sheets (CSS) are used for describing the presentation of a document written in a markup language like HTML. It is designed to separate the concerns of presentation from content, and it contains formatting information like layout, colors, and typography.

HTML and CSS form the cornerstone technologies of the World Wide Web, alongside scripting languages like Javascript.

HTML official documentation (English): https://developer.mozilla.org/en-US/docs/Web/HTML
CSS official documentation (English): https://developer.mozilla.org/en-US/docs/Web/CSS

## Javascript
&nbsp;[[top]](#top)

 Javascript or ECMAScript (ES6) is a scripting language that lets you implement complex features on web pages. It is the third layer on the layer cake of standard web technologies, along with HTML and CSS. It is high-level with dynamic typing, prototype-based object-orientation and first-class functions. It was created by Brendan Eich to add dynamic behavior to th Netscape Navigator browser in 1995.

 Official documentation: https://developer.mozilla.org/en-US/docs/Web/JavaScript

## XML
&nbsp;[[top]](#top)

Extensible Markup Language (XML) is a markup language that defines a set of rules for encoding documents in a format that is both human- and machine-readable. The specifications for XML are defined by the World Wide Web Consortium's XML 1.0. It is used for storing and transporting data.

### XML vs. HTML

XMl is for storing and transporting data. HTML is used for displaying data.

### Defining tags

All tags are defined in the Document Type Declaration (DTD) or the XML Schema Definition (XSD).

### XSD

The XML Schema Definition (XSD) specifies how to formally describe elements in an XML document.

### Being well-formed, being valid.

XML is well-formed when it is syntatically correct. I.e., all tags are properly closed, etc. It can be well-formed but not valid. The XSD or a Document Type Declaration (DTD) can validate an XML document.

### JAX and JAXP

JAX is the Java XML API, while JAXP is the API for XML processing. JAXP gives us two APIs for processing information inside an XML document, DOM and SAX.

###

Official documentation: https://www.w3.org/XML/

## Servlets
&nbsp;[[top]](#top)

A _servlet_ is a _Java_programming_ language class used for extending the capabilities of servers that host applications accessed by the request-response programming model, most commonly an HTTP request.

Tutorial at [Oracle](https://docs.oracle.com/javaee/5/tutorial/doc/bnafe.html)

### Tomcat

The Apache Tomcat software is an open source implementation of the Java Servlet and JavaServer Pages (JSP). It acts as a web and servlet container and can be a standalone container.

Tomcat provides a "pure Java" HTTP web server environment and is responsible for managing the lifecylce of servlets, mapping URLs to servlets, and ensuring that the URL requester has correct access rights.

### Servers and Servlets

A server is a program which manages access to a resource or service in a network.

A _servlet_ is a Java class that acts as a middle layer between a client request and an application on the server. Servlets read data explicitly sent by clients and implicitly sent in the form such as cookies. They process data and generate results by invoking a web service or directly computing the response.

#### Creating Servlets

Servlets are created by the `javax.servlet` and `javax.servlet.http` packages.

#### Servlet Hierarchy

Servlet(interface) --> GenericServlet(AbstractClass) --> HttpServlet(AbstractClass) --> myCustomServlet (you should make a class for this).

The central interface in the Servlet API is `javax.servlet.Servlet`. Every servlet class implements this interface, whether directly or indirectly.

The `GenericServlet` abstract class implements the Servlet interface. It provides all methods except for the service() method.

The _HTTP_SERVLET_, `javax.http.HTTPServlet` is an HTTP capable servlet. It is an abstract class and extends GenericServlet, providing support for the HTTP protocol. It adds a new service() method with the method signature `service(HttpServletRequest, HttpServletResponse)`. It has is a corresponding method for every HTTP method. I.e.: `doGet()`, `doHead()`, `doPost()`, `doDelete()`, `doPut()`, `doOptions()`, `doTrace()`.

The `doGet()` and `doPost` are the most commonly overridden abstract classes. A typical way of overriding the HTTPServlet `doGet()` method might look like:

```java
protected void doGet(HttpServletRequest req, HttpServletResponse res) throws IOException, ServletException {}
```

#### Lifecycle of a Servlet


The lifecycle of a Servlet is `init()`, `service()`, and `destroy()`.

##### `init()`

The method `init()` is called exactly once at container start and instantiantiates the servlet (when load-on-startup is a non-negative integer). If load-on-startup is a negative integer, the `init()` method will be called upon being requested for the first time.

##### `service()`

The `service()` method handles servlet logic. It parses the HTTP requeset and determines applicable methods to be called. The `service()` method is called as many times as needed during the lifecycle of a servlet.

##### `destroy()`

The servlet method `destroy()` closes database connections and does other cleanup activities. It is called exactly once in the servlet lifecycle, either when the web container is terminating or when there is a fatal error within the servlet.

#### Deployment Descriptor

The _deployment_descriptor_ is a configuration file named `web.xml` and which lives in the `WEB-INF` folder.

##### Registering a Servlet in the Deployment Descriptor

To register a servlet, wrap `<servlet-name>`, `<servlet-class>` and `<load-on-startup>` inside of `servlet`.

You must also wrap the `<servlet-name>` and `<url-pattern>` inside of `<servlet-mapping>`.

#### Common Servlet Methods

##### Reacting to incoming HTTP requests

A servlet will react to an incoming HTTP request by sending a direct message, forwarding it, or redirecting it. To write a direct message back to the browser declare a variable named `out` as an object of the `Printwriter` class and set its value to `response.getWired()`. That command is:

```java
PrintWriter out = response.getWired();
```

Then you can send content by calling the `println()` method of the `out` object:
```java
out.println("Hello World");
```

##### Reading Form Data with Servlets

 1. `getParameter()` : gets the value of a form parameter.
 2. `getParameterValues()` : returns values of all parameters with given name if parameter appears more than once.
 3. `getParameterNames()` : returns

##### Returning current session

The `getSession()` method will return current session associated with request or, if none is present it will create one.

##### Getting and setting object inside a session

```java

/* set method */
HttpSession ses = req.getSession();
ses.setAttribute("foo", obj);

/* get method */
HttpSession ses = req.getSession();
ses.getAttribute("bar", obj)
```



http://tomcat.apache.org/


## AWS
&nbsp;[[top]](#top)

Amazon Web Services (AWS) is a subsidiary of Amazon that provide on demand cloud computing platforms and APIs.

Official site:  https://aws.amazon.com/

## <a name="typescript">Typescript</a>
&nbsp;[[top]](#top)

Typescript is an open-source language which builds on JavaScript by adding static type definitions. Types provide a way to describe the shape of an object, provide better documentation and allow your code to be validated better. Typescript was developed and maintained by Microsoft.

Typescript is a strict syntatical superset of JavaScript. Anythis you can do in JavaScript you can do in TypeScript. It is transpiled into JavaScript before it can be read by modenr browsers.

### Typescript Datatypes

* string
* number
* boolean
* array
* any (acts like `let`)
* void
* null
* tuple (stores values of different types)
* enum

### Access modifiers
1. Public
2. Private
3. Protected

### Decorators

Decorators are a special kind of declaration that be attached to a class declaration, method, accessor, property or parameter. They are functions called at declaration (and look a lot like annotations).

### Modules

Modules refer to small units of independent code. A class becomes a module by using the keyword `export` and it can be imported by another file.

#### Making Parameters Optional

A parameter can be made optional by putting the `?` symbol after it. All other parameters to the right of this must also be optional.

### Get & Set

The keywords `get` and `set` allow a method to be used like a variable.

### Inheritance

Interfaces can be inherited by using the `implements` keyword. Another class can be inherited with the `extends` keyword, but only a single class can be inherited.

#### Install

`npm install -g typescript`

#### Transpiling at the Terminal

Run `tsc foo.ts` where 'foo' is the file name and `.ts` is the TypeScript file extension.

Official site: https://www.typescriptlang.org/

## DevOps
&nbsp;[[top]](#top)

DevOps is an organization set of practices that works to automate and integrate activities between software development and IT teams, so they can build, test and release software faster and more reliably.

## <a name="hibernate">Hibernate</a>
&nbsp;[[top]](#top)

Hibernate ORM, or simply _Hibernate_, is an object-relational mapping tool for Java. It provides a framework for mapping a domain model to a relational database by generating SQL calls. This relieves developers from manual handling and object conversion of the result set.

### Object Relational Mapping (ORM)

Object Relational Mapping (ORM) frameworks help provide the following:

* An API for basic CRUD operations.
* An API to create simple and complex queries that target application classes as opposed to database tables.
* A way to specify metadata, (e.g. a column to be created will be a foreign key and not null).
* Optimizations such as dirty checking and lazy associations fetching.

### Benefits of ORMs

* Shields developers from messy SQL statements.
* Improve performance
* Portable (i.e. database independent)
* Additional security

### Mapping

Hibernate uses configuration files (XML) or annotations for mapping.

#### Dirty Checking

Hibernate automatically will update a database when we modify the state of an object inside of a transaction.

### Core interfaces/classes

#### Configuration

These gather information from hibernate.cfg.xml to create a session factory

#### Session Factory

A SessionFactory object is created from the Configuration class after gathering information from hibernate.cfg.xml. Thus it contains all configurations needed to operate Hibernate. It lets a Session object be instatiated and stores information on making connections to the database. Once configured it is immutable.

#### Transaction interface

A transaction object lets you access transaction functionality by abstracting JDBC operations. Transactions in Hibernate are ACID (atomic, consistent, isolated, durable).

#### Query Interface

#### Criteria Interface

#### Methods

* `save`, `insert`: result in an sql insert.
* `delete` : an SQL delete
* `update`, `merge`: an sql update
* `get`, `load`: select statements

### Common JPA annotations in Hibernate

* `@Entity`:
* `@Table`:
* `@Id`:
* `@Column`:

Others include: `@GeneratedValue`, `@OneToOne`, `@ManyToMany`, `@ManyToMany`, `OneToMany`, `ManyToOne`, `@JoinTable`, `@JoinColumn`.

### Java Persistnece API

The Java Persistence API (JPA) provides a POJO persistence model for object-relational mapping. Hibernate implements the Java Persistence API for its annotation functionality.

### States of Persistence

A class can exist in one of three states of persistence:
1. Transient: a new instance with no assocation to the Session or representation in the database.
2. Persistent: is associated with Session and has representation in database.
3. Detached: Session associates with persistent of object is closed.

### Caching

Caching is a mechanism to enhance system performance by creating a memory buffer between an application and database. Hibernate uses L1 caching by default, which is done on a per-session bases. L2 is an optional strategy done at the SessionFactory level whereby objects can be seen by all sessions using the same L2 cache configuration.

#### Implementing L2 cacheing

Select caching provider based on concurrency strategy (EHCache)

### Transaction

A transaction is accessing or changing information in a database.

### Transaction Properties

A transaction must be
  - (A)tomic: transaction executes completely, or not at all.
  - (C)onsistent: the underlying data store is consistent.
  - (I)solated: transaction executes without interference from other processes.
  - (D)urable: the data is not lost if the system crashes.

#### Transaction Isolation Levels

A number of scenarios can arise during concurrent data access. These include dirty reads, unrepeatable reads, phantom reads, and serialization anomolies. Isolation levels are a solution to common issues like lost updates, dirty reads, unrepeatable reads, and phantom reads.

Transaction levels table:

| Read Problems | Dirty | Unrepeatable  | Phantom | Serialization |
| ------------- | ----- | ------------- | ------- | ------ |
| Read Uncommitted | x | x | x | x |
| Read Committed   | - | x | x | x |
| Repeatable Read   | - | - | x | x |
| Serializable  | - | - | - | - | x |

(if marked 'x', problem can happen)

### Caching


Official site: https://hibernate.org/orm/

## Spring
&nbsp;[[top]](#top)

The Spring Framework is an application framework and inversion of control container for Java. It is an open-source platform originally written by [Rod Johnson](https://en.wikipedia.org/wiki/Rod_Johnson_(programmer)) and includes several modules for a range of services.

Spring official site: https://spring.io/

### Annotations
#### Stereotypes
Stereotypes are markers for any class that fulfills a role in an application. Examples might include `@Controller`, `@Repository`, and `@Service`.

### Template Engines & Viewing Technologies
A Spring MVC application separate concerns, so switching from one viewing technology to another simply involves updating configuration. Render different views by defining a _ViewResolver_ for each view technology. View names can then be returned from @Controller mapping methods.

Viewing technologies include Java Server Pages (JSP), Thymeleaf, Groovy, FreeMarker, and Jade.

#### Java Server Pages
A popular view technology that is supported by Spring out-of-the-box. To render JSP files, one common type of bean is the _ViewResolver_:

```java
@EnableWebMvc
@Configuration
public class ApplicationConfiguration implements WebMvcConfigurer {
    @Bean
    public ViewResolver jspViewResolver() {
        InternalResourceViewResolver bean = new InternalResourceViewResolver();
        bean.setPrefix("/WEB-INF/views/");
        bean.setSuffix(".jsp");
        return bean;
    }
}
```

#### Thymeleaf
This Java template engine processes HTML, XML, text, and Javascript or CSS files. It is unique in that templates can be used as prototypes, meaning they can be viewed as static files.

##### Dependencies

Integrate Thymeleaf into Spring by adding the _thymelead-spring4_ dependencies:

```java
<dependency>
    <groupId>org.thymeleaf</groupId>
    <artifactId>thymeleaf</artifactId>
    <version>3.0.7.RELEASE</version>
</dependency>
<dependency>
    <groupId>org.thymeleaf</groupId>
    <artifactId>thymeleaf-spring4</artifactId>
    <version>3.0.7.RELEASE</version>
</dependency>
```

##### Configuration

Add required configuration beans _SpringTemplateEngine_ and _TemplateResolver_. The latter specifies location and type of view files:

```java
@Configuration
@EnableWebMvc
public class ThymeleafConfiguration {

    @Bean
    public SpringTemplateEngine templateEngine() {
        SpringTemplateEngine templateEngine = new SpringTemplateEngine();
        templateEngine.setTemplateResolver(thymeleafTemplateResolver());
        return templateEngine;
    }

    @Bean
    public SpringResourceTemplateResolver thymeleafTemplateResolver() {
        SpringResourceTemplateResolver templateResolver
          = new SpringResourceTemplateResolver();
        templateResolver.setPrefix("/WEB-INF/views/");
        templateResolver.setSuffix(".html");
        templateResolver.setTemplateMode("HTML5");
        return templateResolver;
    }
}
```

It is important to add a view resolver bean of type _ThymeleafViewResolver_


## <a name="web-services">Web Services</a>

A web service is any piece of software that makes itself available over the internet via a standard protocol. They must be discoverable and not tied to an OS.

### Service Oriented Architecture (SOA)
&nbsp;[[top]](#top)

Service-Oriented Architecture (SOA) is a technique for building business applications using loosely-coupled services. These act like black boxes and can be orchestrated to achieve a given functionality.

### Characteristics of SOA

* Reusable
* Autonomous
* Loosely-coupled
* Location-independent
* Standards-based
* Platform-independent

### Services

A service is software that makes itself available.

## Microservices
&nbsp;[[top]](#top)

## Docker
&nbsp;[[top]](#top)

## Kubernetes
&nbsp;[[top]](#top)

II - Appendix

## Architecture and Design

### Object-oriented principles
Four pillars and Grady Booch's major/minor elements.

#### Major & Minor Elements
