# Getting Started

In this chapter we will get Middleman and the underlying environment set up. 

Middleman is a Ruby gem and as such needs Ruby to be installed on your operation system.

The current stable version as of writing is `2.3.1`.

## Installing Ruby

Below are my best efforts at trying to install Ruby the best way on each major platform. If you

### Linux

### Mac

### Windows

## Using Codio

If you've not set up a development environment before, or installed a programming language, it can be pretty daunting.

But you are in luck. Nowadays you do tinker through your browser using platforms such as [Codio](https://codio.com). 

Although geared up for educational institutes the Codio platform offers a great way to spin up Linux development environments and access them through your browser.

I seriously recommend using Codio. I use it on my Chromebook.

To use Codio, sign up for Codio (using the free tier) and log in to the user dashboard.

Once you have done that:

1. Create a new project using the prominent blue button
2. Choose "Ruby+Rails" as your starting point
3. Add a project title choice of your choosing
4. Press create

This will spin up a free development environment for you to use.

Take a few minutes to play with your IDE environment.

To get started open up a terminal using `Tools > Terminal` or by pressing `Shift+Alt+T`. Once you have a terminal open, you should be ready to get going with the rest of this book. Where Codio does things slightly differently I will indicate throughout the book.

> Codio isn't the only web browser IDE environment. However, it is the only one I've found that has good performance, unlimited public projects, simple enough IDE experience. I am sure others are equally good, but I either encountered them when they had flaws or they just didn't fit me. Examples include: Koding, Nitrous ...

## Installing Middleman

Let's get Middleman installed.

Like other Ruby gems it is a single line to install.

Fire open a terminal and run:

```bash
gem install middleman
```

if you are using Mac OS X you may have to install some additional command-line tools. This is the xcode toolset. You can install this using the following command:

```
xcode-select --install
```

> If you get any errors using Codio, like permissions issues, try using ```sudo``` in front of  the gem install command. Normally you wouldn't want Middleman installed using sudo, but the codio platform occasionally requires it.

## Middleman init

## Our first website