---
title: 'Exercise 01 - Installation Instructions'
author: kleinen
layout: page
---


(These are detailled instructions for the installation part of the [Info 3 Startup Lab](../lab-01-startup) ).
## Note on Eclipse, 06/Oct/2014
[startup bug on Mavericks](https://imi-bachelor.htw-berlin.de/studium/labore/hinweise//#c36938)

## Which Computer to use?

As most of your colleagues in the former semesters completely ignored the new [iMacs in our Web Technology lab](https://imi-bachelor.htw-berlin.de/studium/labore/web-technology/) and rather unfolded tiny notebooks in front of the 27'' screens (which unfortunatley even cannot be used as an external monitor), I expect that you will also mainly use your personal computers for working on the exercises. If doing so, you need to make sure to have a set of software available.

If you become more proficient with standard tools like the command line and git, you will find it easier to switch between different computers and end up using the Macs at some point, anyway.


## Text Editor
You need a good basic text editor. Wordpad, Word etc. are no options, as they add format information to the text. Eclipse is also not the best option, as it is rather heavyweight.
Here are some suggestions:

  * [Komodo Edit](https://www.activestate.com/komodo-edit) (free)
  * I use [Sublime Text 2](https://www.sublimetext.com/2 ) which is not free, but can be evaluated for free.
  * [vi](https://en.wikipedia.org/wiki/Vi) or vim - free, available everywhere, somewhat steeper learning curve - I recommend that you learn at least some basic vi commands as vi is available on all remote unix boxes you might happen to log in with ssh.

If you work on multiple platforms, you should choose one that is available on all of them.

## Git & GitHub

* [Git](https://git-scm.com/) is the state-of-the-art Source Code Management Tool. Install the command line client for your platform, and maybe also a GUI Client, [which can all be found here](https://git-scm.com/download/).
* Sign up on [GitHub](https://github.com/) if you haven't already done so. See also
[Setting up Git](https://help.github.com/articles/set-up-git) from GitHub for a comprehensive documentation.
* For other projects, you might want to use the HTW [Projekteserver](https://studi.f4.htw-berlin.de/www/) which offers you private repositorys, or any other service offering
central repositories. Github also offers free private repositories for students.
* Github translates markdown files automatically to HTML - That's how the README.md files you see in most repositories work. Read through the [Markdown](https://help.github.com/articles/markdown-basics) and maybe also the [GitHub Flavored Markdown](https://help.github.com/articles/github-flavored-markdown) documentation.

## Command Line
As a software developer, you need to know the basics of the command line - preferably in linux flavor!

You should at least be able to navigate the file system, look at directories, files and their contents, and start commands, at least your text editor, directly from there (which saves you the time of finding first your text editor and then the file again from some dreadful file open dialog).

See [Learning the Shell](https://linuxcommand.org/learning_the_shell.php) for an intro
and [Tobi's Cheat Sheet](https://pragtob.github.io/rails-beginner-cheatsheet/) for the absolute basics including Windows specials -

### Windows
As I said, preferably linux style. That is, if you're working on Windows, rather learn the linux commands first and then adapt to the Windows equivalents. Or, better yet, install [Cygwin](https://www.cygwin.com/) which gives you a shell with all the linux commands on windows. You might also get away with just using git bash which comes with the windows git installation.

I have installed Cygwin and added the cygwin bin directory to the Windows path, which makes all linux commands from cygwin available in a windows "cmd" window - no need to remember that it would be dir instead of ls anymore!

### The Path

Speaking of that, you should understand the [PATH](https://www.linfo.org/path_env_var.html) - basically a list of directories the shell (the program that reads your commands in the command line) searches for the command.

Also, be aware that if you use Windows, programs like git, graphical git clients, cygwin and cmd have different opinions on where your 'home directory' is.


## UML Drawing Tool

I will accept hand-drawn UML Diagrams for the Lab Reports! I even recommend drawing them by hand, as it gives you more time thinking about your design versus fighting the idiosyncrasies of a particular UML tool which will be out of date or for some other reason unusable next time you need one. And, as redrawing them is more work if you do them by hand, you might end up with simpler diagrams focussing on the most important aspects than if you have a tool.

Nevertheless, your colleagues from the previous semesters preferred UML tools. Well, go ahead and find one, if you must.

## git

[Git](https://git-scm.com/) is the state-of-the-art Source Code Management Tool. Install the command line client for your platform, and maybe also a GUI Client, [which can all be found here](https://git-scm.com/download/).

## Ruby and Ruby on Rails Installation

Installing Ruby and Ruby on Rails has proven to be not as straightforward as one might wish for. I'll give you some hints here; but as I hardly saw the same issue twice there's no much point in trying to collect every possible issue here. On Linux and MacOS, I recommend using RVM.

A lot of issues come from the fact that you'll need a C compiler on your machine.

### Ruby in the Labs:

#### MacOs:

Als  User Pfad der gems in ~/.bash_profile setzen und ein neues Terminal öffnen:

    export GEM_HOME=$HOME/data
    export GEM_PATH=$HOME/data/path
    export GEM_SPEC_CACHE=$HOME/data/spec
    export PATH=$PATH:$HOME/data/bin

Als User Rails installieren:

    $ gem update
    $ gem install rails


### Versions

I usually try to work with the latest versions - the ruby and especially the rails world is evolving quickly. As of today (Oct 5th, 2014) this would be Ruby 2.1.3 and Rails 4.1. - so try to install these versions.
The Windows Ruby Installer usually gives you an older version - use it at your own risk - but Ruby 2.0.0 should be ok.

### Local Installation on your machine
The programming examples will be in Ruby, and at the end of the semester we will dip into the Ruby on Rails Web Development framework and have a look at how Enterprise Application Patterns and agile best practices are incorporated there. As Ruby installation tends to be a pain on Windows, better start now.
For MacOs and Linux, I recommend using rvm (ruby version manager) - all [options are explained and linked from the ruby download page](https://www.ruby-lang.org/en/downloads/).

I will be using the newest versions of ruby and rails in my examples - that is, ruby 2.0 and rails 4.0 as of now. You should be able to get away with ruby 1.8.7 and rails 3.2 for everything we're going to do, but avoiding understanding and navigating around the subtle differences may be worth the effort of getting rid of ruby 1.8.7 on your mac. Honestly.

After installing Ruby, install rails with

    gem install rails

-- see [Rails installation](https://guides.rubyonrails.org/getting_started.html#installing-rails) for further information.

You should then be able to run

    rails new my-first-app
    cd my-first-app
    rails server

in your shell and see a success page if you open [https://localhost:3000](https://localhost:3000) in your browser.

The tricky part about installing rails is, that you need c development tools on your machine. Yes, that means you **need** to install XCode on your Mac. And jump some hoops on Windows. This is because many of the additional packages (called gems in the ruby world) have to be compiled on your machine during installation.

***

## If that works, you're all set!

If not, at least try googling the particular issues you encounter during installation or get help from your peers. [Stackoverflow](https://stackoverflow.com/) is also a great resource. Also, taking the advice that you should understand the path, be able to navigate your files from the command line and be able to look into files is a great help during trouble shooting.

I've also set up an [Q&A Forum in Moodle](https://moodle.htw-berlin.de/mod/forum/view.php?id=27971) - if you get stuck or encounter serious problems please post a question there! Also, if you encounter a problem and find a solution it would be great if you documented it there, as your peers will probably stumble upon similar things (Just post a question and anser it yourself!).

## Do I really need to do all this? If I don't need to turn anything in...

There is nothing to turn in for this e-Learning session or lab. If you get seriously stuck with something, we will try to resolve things next week, 18-Oct-2013 in the Lab. Typically, that will be with Rails on Windows.

I won't, however, be particularly patient with your questions if I find that you start the first UML lab by researching an UML drawing tool for an hour, installing ruby instead of getting your head around the ruby syntax, and spend the rails lab with downloading XCode instead of creating your first web app, or in general seem to be unable to find and look at a file from the command line.

We will also use most of the tools (except ruby and rails) next week for practicing git. So get started!
