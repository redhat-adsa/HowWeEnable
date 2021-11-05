# Getting Started with GIT

## Introduction to Git Presentation

[PDF](into_to_Git_slides.pdf)

[ODP](into_to_Git_slides.odp)

## Install GIT

### Installing on Linux

If you want to install the basic Git tools on Linux via a binary installer, you can generally do so through the package management tool that comes with your distribution. If you’re on Fedora (or any closely-related RPM-based distribution, such as RHEL or CentOS), you can use dnf or yum:

```shell
sudo dnf install git-all
```

If you’re on a Debian-based distribution, such as Ubuntu, use apt:

```shell
sudo apt install git-all
```

### Installing on macOS

If using a Mac with OSX, from version 10.9 onward, Git is preinstalled up to Big Sur (Latest OS release at this time) and can be verified by running the following:

```shell
git --version
```

For other operating systems, follow latest documentation on [git-scm.com](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

## Create your first project

To create your first local project you will need to create a directory and run the init command with the name of the default branch as `main` otherwise it will default to `master`.

```shell
mkdir project-name
cd project-name
git init --initial-branch=main
```

## Git Config

The git config command is used to get and set repository or global level options. Let's set some options for the repository you just created so that when you do a push it knows who made the changes. `NOTE:` If this is a shared machine ([vscodeserver](https://github.com/cdr/code-server) etc) remove the `--global` and it will only add this to the local repository.

```shell
git config --global user.name "john doe"
git config --global user.email "john.doe@example.com"
```

### Set main as global default

Extra credit so you don't have to set initial branch every time you create a new repository.

```shell
git config --global init.defaultBranch main
```

### Show all settings

```shell
git config --list
```

Output:

```shell
user.name=John Doe
user.email=johndoe@example.com
color.status=auto
color.branch=auto
color.interactive=auto
color.diff=auto
```

## Authentication

Most repositories are disabling username and password as an auth mechanism for security reason so you will either need to set up a personal access token if using https authentication, or set up an ssh key and add it to your git server. Below are links to the most common git servers and how to do this:

### SSH

1. Generate an 4096 bit rsa key with a comment to make sure you know what it is for later.

    ```shell
    ssh-keygen -t rsa -b 4096 -C "sshkeyforgit"
    cat ~/.ssh/id_rsa.pub
    ```

    `NOTE:` Never share your private key. It is the one without the `.pub` extension.

2. Add the key to the git server:

[Azure Devops](https://docs.microsoft.com/en-us/azure/devops/repos/git/use-ssh-keys-to-authenticate?view=azure-devops)

[Bitbucket](https://confluence.atlassian.com/bitbucketserver/ssh-user-keys-for-personal-use-776639793.html) `NOTE` You can skip xclip and just cat ~/.ssh/id_rsa.pub

[Gitlab](https://docs.gitlab.com/ee/ssh/)

[Github](https://docs.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account)

### Personal Access Tokens

[Azure DevOps](https://docs.microsoft.com/en-us/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate?view=azure-devops&tabs=preview-page)

[Bitbucket](https://confluence.atlassian.com/bitbucketserver/personal-access-tokens-939515499.html)

[Gitlab](https://docs.gitlab.com/ee/user/profile/personal_access_tokens.html)

[Github](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token)

---

[Next Clone, Commit, Merge](02-clone-commit-push-merge.md)
