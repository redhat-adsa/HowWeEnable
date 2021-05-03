# Enterprise Architecture Standards Deep Dive into 

## Source Code Management Strategy

All modern tools and platforms today start with code. Even if we are infrastructure administrators or deploying applications (COTS or custom) we need to use a single source of truth for storing the code/configurations and making them available for others to collaborate into. The industry standard for everyone is GIT which was created by Linus Torvalds to help manage contributions to the Linux kernel in April of 2005.

The biggest recommendation we can make is solidify a strategy around a centrally used git (github, gitlab, bitbucket etc)and help create a culture of collaboration. Once this is in place you will want to have standards around branching patterns.

Branching patterns are a religious discussion to some, however there is an excellent resource available for this is on [MartinFowler.com](https://martinfowler.com/articles/branching-patterns.html)

`Note:` COTS is commercial off the shelf software, usually not open source and notoriously difficult to maintain.
