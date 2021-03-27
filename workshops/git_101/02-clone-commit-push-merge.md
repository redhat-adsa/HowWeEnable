# Clone Commit Push Merge

## Forking

Most public repositories don't let everyone push to them so you will need to fork the repository to your own namespace in your git server before you can clone it.

Here are links to the most common git systems and how to clone from them:

[Azure Devops](https://docs.microsoft.com/en-us/azure/devops/repos/git/forks?view=azure-devops&tabs=visual-studio)

[Bitbucket](https://support.atlassian.com/bitbucket-cloud/docs/fork-a-repository/)

[Gitlab](https://docs.gitlab.com/ee/user/project/repository/forking_workflow.html)

[Github](https://docs.github.com/en/github/getting-started-with-github/fork-a-repo)

## Cloning a repository

Cloning is making a local copy of code in a local copy of the remote repository. Most of the time you will be cloning someone elses repository so you can use it or make a change and then push in for a request to have it merged into the upstream codebase. Remember unless you have access to the upstream repository you will need to either request access or fork the code to push into it.

For this exercise fork this repository using the github instructions above then clone it (depending on if you created a PAT(public access token) or a SSH key follow the correct instruction below:

### SSH Clone

```shell
git clone git@github.com:yourgithubname/HowWeEnable.git
```

### HTTP Clone

```shell
git clone https://<pat>@github.com/yourgithubusername/HowWeEnable.git
```

`NOTE:` Replace `<pat>` with the toekn you ceated in the earlier excercise.

Output:

```shell
Cloning into 'HowWeEnable'...
remote: Enumerating objects: 283, done.
remote: Counting objects: 100% (283/283), done.
remote: Compressing objects: 100% (173/173), done.
remote: Total 283 (delta 77), reused 276 (delta 74), pack-reused 0
Receiving objects: 100% (283/283), 81.03 KiB | 1.72 MiB/s, done.
Resolving deltas: 100% (77/77), done.
cd HowWeEnable
tree
.
├── LICENSE
├── README.md
└── workshops
    └── how_we_enable
        ├── 01-Getting_Started.md
        ├── 02-Logistics.md
        ├── 03-Strategy.md
        └── 04-Practice_Scenarios.md
```
