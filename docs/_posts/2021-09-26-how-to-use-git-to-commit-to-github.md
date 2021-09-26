---
layout = post
title = Using Git to Commit Files to Github
date = 2021-09-26 15:47:23 +0800
categories: git
---



# Using Git to Commit Files to Github

@Linux Mint 20.2

Git 2.25.1



***

## Install Git

### Install Git on Linux using package manager

+ Debian / Ubuntu

``` bash
# apt-get update

# apt-get install git
```

+ Arch Linux

``` bash
# pacman -S git
```

+ Fedora

Up to Fedora 21:

``` bash
# yum install git
```

Fedora 22 and later:

``` bash
# dnf install git
```

 + Alpine

``` bash
$ apk add git
```



### Build from Source

You can find tarballs on [kernel.org](https://www.kernel.org/pub/software/scm/git/).

// TODO finish this part  



### Install Git via Git

``` bash
git clone https://github.com/git/git
```



### Downloads for macOS / Windows

+ Download for macOS: [here](https://git-scm.com/download/mac)

+ Download for Windows: [here](https://git-scm.com/download/win)

## Check Git Version

``` bash
$ git --version
```

If installed correctly, you should see the following: (versions may be different)

``` 
git version 2.25.1
```



## Add Remote Repository

``` bash
git remote add [shortname] [url]
```



## Generate and Add SSH key

### Generate SSH key

``` bash
$ ssh-keygen -t rsa -C "email@example.com"
```

"email@example.com" is the email you register for Github.

When the terminal asks you to enter file directory, pass phrase, you can enter your personalized configuration or just directly press Enter for three times.

### Add SSH key to your Github

1. If SSH key is generated successfully, you can find it under **~/.ssh/id_rsa.pub**. 

2. Copy key.

3. Go to **Github** -> **Account** -> **Settings** -> **SSH and GPG keys**.

4. Click **New SSH key**.

5. Enter a title for SSH keys, and paste key.

6. Click **Add SSH Key**



To verify you have done it successfully, enter the following in terminal:

``` bash
$ ssh -T git@github.com
```

Enter **yes** when asked "are you sure you want to continue connecting?".



## Use Git to Commit

### Clone a repository to your computer

Change to working directory:

``` bash
$ cd dir
```

Clone your repository:

```bash
$ git clone https://github.com/username/repo
```



### Modify your repository locally

For example, add a README doc:

``` bash
$ echo "Hello world!" >> README.md
```



### Commit

You can check your repository status, like which file has been changed:

``` bash
$ git status
```

Add all files:

``` bash
$ git add .
```

Or you can add some files you want to add:ssh -T git@github.com

``` bash
$ git add README.md
```

Commit and and add message:

``` bash
$ git commit -m "Commit message"
```



### Push

```bash
$ git remote set-url origin git@github.com:username/repo.git
```

``` bash
$ git remote add origin git@github.com:username/repo.git
```

 ``` bash
 $ git push -u origin master
 ```







