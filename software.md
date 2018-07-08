---
layout: page
title: Software Installation
sidebar_link: true
permalink: /software-installation/
---

## Bare Metal - Dev Machine

### System Requirements

* Ubuntu

#### Basic packages

For the smooth functioning of the steps that follows its better to have the following tools installed.


```sh
sudo apt-get --ignore-missing install build-essential git-core curl openssl libssl-dev libcurl4-openssl-dev zlib1g zlib1g-dev libreadline6-dev libyaml-dev libsqlite3-dev libsqlite3-0 sqlite3 libxml2-dev libxslt1-dev libffi-dev software-properties-common libgdm-dev libncurses5-dev automake autoconf libtool bison
```

### Ruby

#### Ruby Version Manager

A version manager is a software that helps us manage multiple versions of a tool in our system. It ensures
that libraries/code of one version doesn't conflict or create issues with another version. When we install a
software through `apt-get` it installs single version that is getting set for that user in that machine.

Ruby releases a new version every year and following a one year release cycle, it also release a patch for
security vulnerabilities as soon as its made known. In most likely when you work as a professional ruby programmer you will be working on multiple versions of ruby at the same time.

In the ruby ecosystem there are two popular version managers called RVM and rbenv. The tool I personally use and recommend is RVM (Ruby Version manager).

Refer: [https://rvm.io](https://rvm.io)

#### Setup

```sh
gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB

curl -sSL https://get.rvm.io | bash -s stable
```

If you see an error that says curl doesn't exist then run the bellow command:

```sh
sudo apt-get install curl
```

*Note:* Do not install RVM or ruby as a root user. Its recommended because we don't want
the applications we are building to have root permission. Giving root permission to an application could lead to serious security issues in future.

If you find any issues with RVM after successful install then checkout rvm gnome-shell post install instructions [http://rvm.io/integration/gnome-terminal](http://rvm.io/integration/gnome-terminal)

#### Install latest Ruby

Its always recommended to work in the latest version of any tool before you build your new
application. As the chances are that you won't be able to upgrade once you start writing business critical code.

```
rvm install 2.5.1
```

### NodeJS

Node JS is not a requirement for ruby programs, but its is a requirement for Rails. Rails being known as a swiss army knife of web development, can't be called so unless it lets us work with the frontend HTML and JS as easy as writing backend code or managing the database.

Rails makes uses logs of tools from the JS world to achieve this, thus its now important to have Node JS installed in the system as well.

NodeJS has something similar to RVM called NVM (Node version manager). Installing NVM in our dev machines will allow us to better manage our node js applications.

Refer: [https://github.com/creationix/nvm](https://github.com/creationix/nvm)

#### Setup

```sh
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash
```


### Rails

Only step now is to install rails gem (libraries in ruby ecosystem are referred to as gem.) Gems in ruby are installed using the command gem.

```
gem install rails
```

#### Make a new rails app

```
rails new test-app
cd test-app
bundle install
bundle exec rails s
```

Once the above steps are done go visit the url. `https://localhost:3000`, if you see a web page then your rails app is online. 🎉

### Text Editor

During this workshop we will be using the text-editor vscode. But if you have one that you are already good with then feel free to use that.

Refer: [https://code.visualstudio.com/docs/setup/linux](https://code.visualstudio.com/docs/setup/linux)

### Database (If your workshop covers databases as well)

#### SQLite 3

If you followed the first set of steps you have already installed SQLite3


### How to know if the software is installed right?

One of the steps that most people do is to check the version number. Only if the tool is installed
can it tell us the version number 🤓.

```
rvm -v
ruby -v
nvm -v
node -v
rails -v
```

*All the software recommended in this workshop are free and open source*
