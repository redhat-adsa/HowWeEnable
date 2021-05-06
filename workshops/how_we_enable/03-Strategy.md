# Enterprise Architecture Standards Deep Dive

## APIs

Application Programming Interfaces are the defacto standard for how applications talk to each other. Making these be secure, reusable and cataloging them so they are accessible to your customers is a standard practice for digital transformation.

_Note:_ "Customers" can be internal or external customers.

## Automation

"Covid-19 has made automation a boardroom imperative.” - Forrester Research 2020
Automating all services and making them consumable via APIs is the standard way of doing this in today's IT. Most people start with a command line tool, and build it into a pipeline or pass around cookbooks or playbooks, which is a great way to start, however someone needs to know where these are. A common practice is using a centralized tool like Ansible Tower to make all of these playbooks self service by exposing them as APIs.

## Cloud Native Development

All new application development should follow Cloud Native Standards:

| Standard                | Description                                                      |
|-------------------------|------------------------------------------------------------------|
| **Codebase**            | One codebase tracked in revision control, many deploys           |
| **Dependencies**        | Explicitly declare and isolate dependencies                      |
| **Config**              | Store config in the environment                                  |
| **Backing services**    | Treat backing services as attached resources                     |
| **Build, release, run** | Strictly separate build and run stages                           |
| **Processes**           | Execute the app as one or more stateless processes               |
| **Port binding**        | Export services via port binding                                 |
| **Concurrency**         | Scale out via the process model                                  |
| **Disposability**       | Maximize robustness with fast startup and graceful shutdown      |
| **Dev/prod parity**     | Keep development, staging, and production as similar as possible |
| **Logs**                | Treat logs as event streams                                      |
| **Admin processes**     | Run admin/management tasks as one-off processes                  |

_Source:_ [12factor.net](https://www.12factor.net)

## CI/CD

Continuous integration and continuous delivery/deployment is the defacto standard for delivering applications in a cloud native way.  Having a standardized pipeline that everyone uses to build, test, operate, measure, monitor, secure and deploy applications at the enterprise level helps everyone to follow the same standards for quality application delivery.

## Monitoring/Observability

Much like CI/CD, having consistent cross functional standards for logging (preferably as streams) monitoring, tracing and utilization is a best practice to have.

## Security

Security can be made easier for developers when you solidify a standard for them to use and implement into their CI/CD pipelines. This includes but is not limited to the implementation of static code analysis as well as running code analysis tools. It is also a best practice to use a trusted source for libraries that is regularly scanned (ie not pulling libraries directly from the internet pypi, npm etc).
.

## Source Code Management Strategy

All modern tools and platforms today start with code. Even if we are infrastructure administrators or deploying applications (COTS or custom) we need to use a single source of truth for storing the code/configurations and making them available for others to collaborate into. The industry standard for everyone is GIT which was created by Linus Torvalds to help manage contributions to the Linux kernel in April of 2005.

The biggest recommendation we can make is solidify a strategy around a centrally used git (github, gitlab, bitbucket etc)and help create a culture of collaboration. Once this is in place you will want to have standards around branching patterns.

Branching patterns are a religious discussion to some, however there is an excellent resource available for this is on [MartinFowler.com](https://martinfowler.com/articles/branching-patterns.html)

`Note:` COTS is commercial off the shelf software, usually not open source and notoriously difficult to maintain.

## Testing and Test Driven Development

When you build your applications around tests and mocking you ensure that any changes to the application will be validated and ensures that future enhancements you do not break the application in the future.  One of the best guides on this is here:

[Thoughtworks TDD Blog](https://www.thoughtworks.com/insights/blog/test-driven-development-best-thing-has-happened-software-design)
