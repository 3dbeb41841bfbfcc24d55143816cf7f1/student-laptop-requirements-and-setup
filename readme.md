<!--
This file is auto-generated from a 'template.md'
file using the 'md-process' script.
Therefore *DO NOT* edit this file directly!
Instead edit the template file and then run 'md-process'.
-->

# Student Laptop Requirements and Setup

## Table of Contents

* [Laptop Machine](#laptop-machine)
  * [Versions of Mac OS(X)](#versions-of-mac-osx)
* [Administrater Rights](#administrater-rights)
* [Login and Shell](#login-and-shell)
* [BASH Configuration](#bash-configuration)
  * [.bash_profile](#bashprofile)
  * [.bashrc](#bashrc)
  * [Why Two Configuration Files?](#why-two-configuration-files?)
* [Other Useful Hacks](#other-useful-hacks)

## Laptop Machine

We highly recommend a MacBook, MacBook Pro, or MacBook Air with at least 4GB of memory (8GB is even better) and 100GB of free storage space.

We also recommend being on a recent version of MacOSX (a version released in the last 12 months) because many of the 3rd party and open source software that we will be installing and using requires a recent version of MacOSX.

### Versions of Mac OS(X)

* Mac OS X 10.0 – code name "Cheetah", released in 2001
* Mac OS X 10.1 – code name "Puma", released in 2001
* Mac OS X 10.2 – also marketed as "Jaguar", released in 2002
* Mac OS X Panther – version 10.3, released in 2003
* Mac OS X Tiger – version 10.4, released in 2005
* Mac OS X Leopard – version 10.5, released in 2007
* Mac OS X Snow Leopard – version 10.6, released in 2009
* Mac OS X Lion – version 10.7, released in 2011
* OS X Mountain Lion – version 10.8, released in 2012
* OS X Mavericks – version 10.9, released in 2013
* OS X Yosemite – version 10.10, released in 2014
* OS X El Capitan – version 10.11, released in 2015
* Mac OS Sierra – version 10.12, released in 2016


You can check your Mac Laptop via the desktop "Apple" menu:

![About This Mac](images/about-this-mac.png)

The overview tab will show you the version of MacOSX you are running as well as your display, processor, and the amount of main memory (RAM) installed in your laptop.

![About This Mac - Overview](images/about-this-mac-overview.png)

The storage tab will show you how much available storage you have. We will be installing a _lot_ of software over the 12 week class so you will need approximately 100GB of available storage space.

![About This Mac - Storage](images/about-this-mac-storage.png)

## Administrater Rights

You will need to have _administrative_ rights on your laptop. You can check this by going to _System Preferences_ => _Users and Groups_ and selecting your account on the left side of the dialog. The option _Allow user to administer this computer_ should be checked:

![](images/current-user-admin.png)

## Login and Shell

We will be using the _Terminal_ a lot in this class to install software, create directories, manage GIT repositories, and perform other tasks. The _Terminal_ will launch your default _shell_ which should be the _BASH_ shell.

To check your default shell, open the _Terminal_ app (you can use Spotlight) and at the prompt type:

```bash
echo $SHELL
```

And you should get the following response:

```bash
/bin/bash
```

## BASH Configuration

We will be using two files to configure our BASH Shell: .bash_profile and .bashrc.

Below are examples of these files.

### .bash_profile

```bash
echo "Hello from .bash_profile"

export PATH=/usr/local/bin:$PATH

alias path='echo -e ${PATH//:/\\n}'

[[ -r ~/.bashrc ]] && . ~/.bashrc
```

### .bashrc

```bash
echo "Hello from .bashrc"
```

### Why Two Configuration Files?

You can put configuration settings in either `.bash_profile` or `.bashrc`. The only difference between these two files is that:

* `.bash_profile` is executed when you login.
* `.bashrc` is used for non login shells (i.e. shells that are launched to run a script or a background process).

Since we often put settings in `.bashrc` that we also want to be set in a login session, we source the `.bashrc` file from the `.bash_profile` file.

## Other Useful Hacks

* Add OneTab Chrome Plugin
* Setup a nice bash prompt
  - Liquid Prompt
* Setup some Git aliases for the _longer_ Git commands (via ~/.gitconfig), for example:

```
[alias]
  g  = log --graph --all --branches --decorate --pretty=format:'[%C(auto)%h%Creset][%C(cyan)%an %ar%Creset]%C(auto)%d%Creset %s %C(auto)%Creset'
  ls = log --stat --all --decorate
```
