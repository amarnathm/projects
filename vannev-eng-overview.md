

# Vannev Engineering Overview

*Amarnath Mukherjee*  
October 13, 2011

Vannev provides a collection of services. The platform is flexible. Each service is implemented in its own pool of servers. A pool exposes a subdomain, and may have its own pools at the backend, e.g., for search, background jobs, and caching.

There is a shared caching server that provides consident data for feeds to the different services. For example, feeds provide "updates" when a user shares a trail with another, or adds an item to a shared trail.

The update is essentially a publish-subscribe subsystem.

Sharing allows for fine grained access control to each record. Implementing it at an Internet scale is its own business problem.

Login includes login-with-facebook, implementing OAuth-2 in Java.

Search is implemented on top of Solr. Shared search and permission controls require special handling. So also, providing relevant snippets for trails.

The database schema generation is check-pointed. This helps multiple developers, as well as the QA and Production machines, to update to the latest schema in a determininstic, error free way.

Recent client side javascript uses jQuery. There is also a whole bunch of legacy javascript/ajax.

The platform is similar to Google Apps, Yahoo, and other larger websites. Machines in a pool can be brought down and restarted, transparently to users. That's why, the controller framework does not implement session beans -- there is no state cached in any server instance that is not also available to other server instances. There is caching, but they are also backed to a persistent data store.

The server platform is Java. The database is MySQL. Development platform can be Windows or Linux. Deployment is on Ubuntu.

Because of the nature of the business problem, there is often a need to execute a number of SQL statements at once -- so considerable amount of SQL is pushed into MySQL stored procedures. The tradeoff was between database independence and efficiency. We chose efficiency. In the event we need to move to a different database, the stored procedures (and potentially, the Java Dao classes calling them) will need to be ported.

As is standard, a request comes to the presentation-layer, goes through the business-layer, then the data-layer, and then back up the chain. Static code is organized as hierarchical modules (Eclipse projects) to manage dependencies. 

We use a number of open source libraries. While they are too many to list, there are the usual suspects -- logging, file-upload, xml-parsing, json-parser, etc.

For output, we used to use JSPs, and still do. However, these days, there is almost no Java code in a JSP -- they are all encapsulated in either custom tags, or via a special <s:property name="foo" /> tag similar to Struts-2. This makes it easier to refactor the code, as well as in debugging. 

Much of the code is needed by more than one service, so is part of the platform. Examples include Search, Database-Schema-Checkpointing, and Contolled Sharing. The different services extend relevant classes and provide their own customizations, if  necessary.

Build for the various services is managed with Ant. Customizations are provided for development, QA, and production environments. Customizations include, among other things, concatenating javascript files for performance (in QA and production), compressing output files (QA and production), providing different urls and other data for the various services, etc.



Copyright Amarnath Mukherjee, 2011.