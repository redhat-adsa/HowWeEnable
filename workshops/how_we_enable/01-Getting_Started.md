# Getting Started

## How To Use

The first thing we need to do before anything else is get a full understanding of tools, developers, architectures, security and best practices. In order to do this we have created a checklist to simplify the process. ***Use this as a conversation starter NOT as a survey!***

As this is open source please feel free to put in a PR to add to this list.

---

## MVS Thought Provoking Topics

Rate organization's skill maturity on a scale of 1-5:

| Minimum Viable Skill | 1 | 2 | 3 | 4 | 5 |
|----------------------|---|---|---|---|---|
| **Automation** | Automation is rarely used or misunderstood by most IT teams | Automation is used by at least one vertical (sec/devs/ops) to perform at least a few day-to-day tasks | Automation is used in a few verticals using disperate tools, and at least some automations are used in production | Automation is used widely across the organization, but no standards/structure exists for automation across the organization | Automation is used across all IT teams in a standardized way and is shared and managed through APIs |
| **Cloud Native Development** | CND is not understood or used by any teams | CND has been explored conceptually by at least one team, but never used in production | CND is used by at least one team as a preferred framework in production | CND is widely used, but without organizational consensus on standards, platforms, or tooling | CND is widely used across the organization, backed by standards for all developers and golden roads to production through automation |
| **Collaboration** | Pathological+ | | Beurocratic+ | | Generative+ |
| **Containerization** | Containers are not understood or used by any teams | Containers have been explored conceptually by at least one team, but never implemented in production | Containers are used by at least one team as their preferred hosting framework in production | Containers are widely used, but orchestration of containers is not formalized across the organization, automation/tooling is lacking, the orchestrator is not named "Kubernetes", or Kubernetes is used but not understood by teams | Containers are widely used and orchestrated in a well-defined and understood way using Kubernetes, with developer and operations tooling/automations eliminating nearly all toil from the application lifecycle |
| **Networking** | Networks are completely black-box to all but a few people, requests for network resources take weeks/months | Networks are understood by at least one non-networking team, but requests for resources still take a long time | Networks are understood by at least a few teams, and some automation has started to happen, but it's only available to a few people so requests take days | Networks are somewhat automated, with a few common resources/requests being completely automated | Network architecture is standardized, generally known by all IT teams, and day-to-day tasks are completely automated including maintaining/creating certificates, DNS, firewalls, and load balancers, with teams provisioning these resources in seconds through self-service automation |
| **Security** | Security is seen as a waste of resources | Security is considered by at least one team, with audits happening yearly/quarterly | Security audits happen with regularity and at least some automation is in place for performing day-to-day tasks | Security automation is widely used for scanning infrastructure and source code and security is a primary concern for large/critical projects from the start, but most security still happens after implementation | Security expectations are well defined and a primary concern of all employees from the start with robust and thorough security automation baked-in to all levels of infrastructure and source code being scanned on every commit for vulerabilities |
| **Testing** | Testing is not used or misunderstood | Testing is frequently used by at least one team | Testing is adopted by a few teams using TDD and tests execute on each commit | Testing through TDD is widely used with some standards, and other forms of tests have started to arise, but are generally not adopted | Testing is standardized and has moved beyond TDD to include contract testing, integration testing, and other patterns |

> _+ see [Westrum Organizational Culture](https://cloud.google.com/architecture/devops/devops-culture-westrum-organizational-culture)_


| Architecture           | Details (Get specifics and link to possible workshop ideas) |
|------------------------|-------------------------------------------------------------|
| API Standards          |                                                             |
| Coding Standards       |                                                             |
| CI/CD Standards        |                                                             |
| Data Standards         |                                                             |
| Developer Experience   |                                                             |
| Hybrid Cloud           |                                                             |
| Source Code Management |                                                             |

| Languages and Frameworks | Details (Get specifics and link to possible workshop ideas) |
|--------------------------|-------------------------------------------------------------|
| Angular                  |                                                             |
| Golang                   |                                                             |
| Java                     |                                                             |
| Julia                    |                                                             |
| Node                     |                                                             |
| .NET                     |                                                             |
| Perl                     |                                                             |
| PHP                      |                                                             |
| Perl                     |                                                             |
| Python                   |                                                             |
| R                        |                                                             |
| React                    |                                                             |
| Spring                   |                                                             |

| Security           | Details (Get specifics and link to possible workshop ideas) |
|--------------------|-------------------------------------------------------------|
| API Security       |                                                             |
| Artifactory        |                                                             |
| Code Analysis      |                                                             |
| Container Security |                                                             |
| Secrets Management |                                                             |
