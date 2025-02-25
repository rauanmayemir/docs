# Table of Contents [v2.*]

* [Documentation for v1.0](https://github.com/spiral/docs/tree/master)

* Getting Started
    * [About Framework](about/spiral.md)
    * [Installation](about/install.md)
    * [Versioning](about/semver.md)
    * [Contributing](about/contributing.md)
    * [LICENSE](license.md)
* Basics
    * [Workers and Application Lifecycle](basic/workers.md)
    * [Application Structure](basic/structure.md)
    * [Default Configuration](basic/configuration.md)
    * [Console Commands](basic/commands.md)
* Framework
    * Design Approach
    * [Application Server](framework/application-server.md)
    * Kernel, Environment
    * [Container and Factories](framework/container.md)
    * [Bootloaders](framework/bootloaders.md)
    * [Singletons](framework/singletons.md)
    * [Config Objects](framework/config.md)
    * [IoC scopes](framework/scopes.md)
    * [Auto Wiring](framework/auto-wiring.md)
    * [Static Memory](framework/memory.md)
    * [Finalizers](framework/finalizers.md)
* Cookbook
    * Quick Start
    * Scaffolding
    * [Prototyping](cookbook/prototype.md)
    * Database Scaffolding
    * MVC Application
    * [Website Scraper](cookbook/scraper.md)
    * [Custom PSR-15 Handlers](cookbook/psr-15.md)
    * [Integrate Golang service to PHP](cookbook/golang-library.md)
    * Write an Extension       
    * [Custom Dispatcher](cookbook/custom-dispatcher.md)
    * Testing Application
* Components
    * Files and Directories
    * Code Generation
    * [Data Encryption](component/encrypter.md)
    * Validation
    * [Pagination](component/pagination.md)
    * RBAC Authorization
    * [Static Analysis Tools](component/tokenizer.md)
    * [Prometheus Metrics](component/metrics.md)
* Console
    * [Installation and Configuration](console/configuration.md)
    * [User Commands](console/commands.md)
* HTTP
    * [Installation and Configuration](http/configuration.md)
    * [Request Lifecycle](http/lifecycle.md)
    * [Request and Response](http/request-response.md)
    * [Routing](http/routing.md)
    * [Error Pages](http/errors.md)
    * [Middleware](http/middleware.md)
    * [Golang Middleware](http/golang.md)
    * [Cookies](http/cookies.md)
    * Session
    * CSRF protection
* Request/Filter Objects
    * Installation and Configuration
    * Filter Entity
    * Nested Filters
    * Error Mapping
* Queue and Jobs
    * [Installation and Configuration](queue/configuration.md)
    * [Console Commands](queue/commands.md)
    * [Running Jobs](queue/jobs.md)
    * [Standalone Usage](queue/standalone.md)
* GRPC
    * Installation and Configuration
    * Generating Service Code
    * Passing Metadata and Errors
    * Golang Services
    * GPRC client code
* Views
    * Installation and Configuration
    * View object
    * [Plain PHP templates](views/native.md)
    * [Twig templates](views/twig.md)
* Stempler templates
    * Installation and Configuration
    * Basic Usage
    * Inheritance
    * Components and Props
    * Directives
    * [AST Modifications](stempler/visitors.md)
* Internalization
    * Installation and Configuration
    * Import and Export
    * Translate Views
    * Say Trait
* DBAL
    * Installation and Configuration
    * Databases and Drivers
    * Database Isolation
    * Query Builders
    * [Transactions](database/transactions.md)
    * [Schema Introspection](database/introspection.md)
    * [Schema Declaration](database/declaration.md)
    * [Migrations](database/migrations.md)
    * [Errata](database/errata.md)
* Cycle DataMapper ORM
    * [Installation and Configuration](cycle/configuration.md)
    * [Transactions](cycle/transactions.md)
    * [Full Documentation](cycle/documentation.md)
    * [Console Commands](cycle/commands.md)
 * WebSocket Broadcasting
    * Installation and Configuration
    * JavaScript Client
    * Topics and Authorization
    * Standalone Usage
* Debug and Profiling
    * [Dumping Variables](debug/dumps.md)
    * RoadRunner Gotchas
    * Logging
    * [Handling Exceptions](debug/exceptions.md)
    * XDebug
* Extensions
    * [Code Style](extension/code-style.md)
    * [Dotenv](extension/dotenv.md)   
    * [Monolog](extension/monolog.md)
