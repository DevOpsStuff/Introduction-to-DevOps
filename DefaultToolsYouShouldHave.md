# Default Tools You should have for Infra guy.

Always have the habit of reducing the usage of `Mouse`. 

# Visual Code Editior

An Awesome Editor which supports many langauages with extension. Vim is also better, when you dont want GUI.
- [Download](https://code.visualstudio.com/)

# A Silver Searcher

A Silver Searcher is a fast search tool, when you are working on a large codebase. shortly called as `ag`. There is also similar tool called `ack`.

[Silver Searcher Github Page](https://github.com/ggreer/the_silver_searcher)

## Installation

### macOS

    brew install the_silver_searcher

or

    port install the_silver_searcher
    
### Linux

* Ubuntu >= 13.10 (Saucy) or Debian >= 8 (Jessie)

        apt-get install silversearcher-ag
* Fedora 21 and lower

        yum install the_silver_searcher
* Fedora 22+

        dnf install the_silver_searcher
* RHEL7+

        yum install epel-release.noarch the_silver_searcher
* Centos

        yum install the_silver_searcher

# Bash-completion

Auto complete tool for command line. 

- [Github](https://github.com/scop/bash-completion)
- [Setup and Usage](https://sourabhbajaj.com/mac-setup/BashCompletion/)

## Installation:

### macOS

    brew install bash-completion
    
# Hub

Now, everyone is familiar with git command, but still for somethings like creating a repo in Github, we have too visit the github and do some UI stuff. A Hub is an 
Extesion for github, you can do most of the things via command line instead of visiting the github.

## Installation

* Mac OS
 
    brew install hub

## Usage
   
   ```
   # clone your own project
hub clone dotfiles

# clone another project
hub clone github/hub

# fast-forward all local branches to match the latest state on the remote
cd myproject
hub sync

# list latest open issues in the current repository
hub issue --limit 10

# open the current project's issues page
hub browse -- issues

# open another project's wiki
hub browse rbenv/ruby-build wiki

# share log output via Gist
hub gist create --copy build.log
```

And a lot more examples you can find from this [link](https://hub.github.com/)

# [Docker](https://github.com/DevOpsStuff/Containerization)

No Need any explanation for this, by this time if you haven't heard about this term `Docker`. You are still living in 80's world.

# Shellcheck

ShellCheck is a static analysis tool that shows warnings and suggestions concerning bad code in bash/sh shell scripts. 
It can be used in several ways: from the web by pasting your shell script in an online editor (Ace – a standalone code editor written in JavaScript) in https://www.shellcheck.net 
(it is always synchronized to the latest git commit, and is the simplest way to give ShellCheck a go) for instant feedback.

## Installation

* macOS

      brew install shellcheck

# jq

Most of the admin's favourite tool who works with JSON. you can combine with `CURL` command. There is a similar command line tool in python for this

`curl http://example/api/v1/name | python -mjson`

(And more to go..)
