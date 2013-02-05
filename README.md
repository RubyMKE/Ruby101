# Ruby101 Installfest

`DON'T PANIC`

Installation of Ruby and other tools is not as hard as it used to be, but things still occasionally go wrong. We will have volunteers around to help if something does go awry. Just raise your hand or find one of us.


# The Long Version (Recommended)
The [RailsBridge](http://workshops.railsbridge.org/) team has created a fantastic set of installation documentation along with tests to ensure everything is configured correctly.

`HOLD UP. READ THIS. IT JUST MAY SAVE YOUR LIFE...`

As you go through each section of the installation please read the _entire_ step through its end and _then_ execute the step. There are sublties about the installation process that if done out of order will get you caught up. All in, the installation takes people 30 to 45 minutes and most of that is donwloading softare.  Good luck!

`Okay. Now you can click away...`

[RailsBridge Install Fest Instructions](http://ruby201.herokuapp.com/installfest/)


If you want to be sure that, before you leave, everything you need for Ruby and Rails development is installed correctly, follow the RailsBridge instructions. If you don't plan to work with Rails, are short on time, or just want to see the basic steps, look below to Installation For The Impatient


# While You Wait
A few parts of the installation can take a fair amount of time. While waiting, one thing you could do is get started learning Ruby.
## A First Look At Ruby
[TryRuby.org](http://tryruby.org) - Interactive Ruby Tutorial on the web, in a style very representative of the Ruby community. Welcome!

----

###A Quick Detour

While checking out TryRuby, be sure to click that link in the bottom left to find the *best programming book ever written* which just happens to be about Ruby: [Why's (Poignant) Guide To Ruby](http://mislav.uniqpath.com/poignant-guide)

----



# Installation For The Impatient

## What are we installing?
* [Homebrew](http://mxcl.github.com/homebrew/) (OS X) - Package management
* [Git](http://git-scm.com/) - Version control and getting packages
* [RVM](https://rvm.beginrescueend.com/) (except Windows) - Installing and managing Ruby versions
* [Ruby-1.9.3](http://www.ruby-lang.org/)
* [Rails 3.2](http://rubyonrails.org/)
* [Bundler](http://gembundler.com/) - Managing gem dependencies (optional)
* A text editor, if you don't already have a favorite.

NOTE: A dollar sign `$` in the instructions below is meant to indicate a command line prompt. This means the instruction is indented to be entered on the command line. You should type everything in the box *except* the $ into the command line prompt

## Rails
On OS X and Windows the fastest way to install everything on our list is to use the [RailsInstaller](http://railsinstaller.org/).

Once the OS-specific installation steps below are performed, rails installation is the same on all platforms: `$ gem install rails`

## OS X
* Compiler - Hopefully you have this already
  * [XCode](http://developer.apple.com/downloads) - Search for "Command Line Tools for XCode"
  * [gcc-installer](https://github.com/kennethreitz/osx-gcc-installer) - Can also be used
* Homebrew: `$ ruby -e "$(curl -fossil raw.github.com/mxcl/homebrew/go)"`
* Git:  `$ brew install git`
* RVM:  `$ curl -L get.rvm.io | bash -s stable && source ~/.bash_profile`
* Ruby: `$ rvm install 1.9.3 # May need --with-gcc=clang`
* Set default: `$ rvm use 1.9.3 --default`
* Bundler: `$ gem install bundler`

## Linux
*Note:* Ruby and gems are poorly served by almost all official distribution packaging, so most Rubyist avoid them. Instead, the environment is very similar to OS X.

* Git: `$ apt-get install git-core`
* RVM: `$ curl -L get.rvm.io | bash -s stable && source ~/.bashrc`
* Ruby: `$ rvm install 1.9.3`
* Set default: `$ rvm use 1.9.3 --default`
* Bundler: `$ gem install bundler`


# Windows Note
Ruby and Rails development on Windows is totally possible, but will be fraught with occasional compatibility issues. Some gems require native compiled extensions which is sometimes problematic on Windows. Windows can provide a fine experience, but this is your warning that it may not always be as easy.

# Text Editors
If you don't have a favorite text editor, there are many choices. Rubyist do tend to use a text editor over an IDE, but we have those available as well.

* [Sublime Text2](http://www.sublimetext.com/2) - Cross-platform (windows/mac/linux) and a tool that makes coding lovely.
* [Redcar](http://redcareditor.com/) - Written in Ruby, cross-platform.
* [RubyMine](http://www.jetbrains.com/ruby/) - IDE, cross-platform
* [Notepad++](http://notepad-plus-plus.org/) - Windows

If you really want to invest time in learning a powerful text editor, [vim](http://www.vim.org/) is arguably the most popular among Rubyist, while [emacs](http://www.gnu.org/software/emacs/) is arguably the most powerful. Both take real dedication to master and pay handsome rewards for doing so.


# Common Installation Problems
If you run into an issue while following the installfest instructions, check the [Solutions to Common Problems](https://github.com/RubyMKE/Ruby101/blob/master/solutions-to-common-install-problems.md) where we are cataloging issues found as well as solutions. (Feel free fork and add your problem, if its not already there.)

# Next Steps

## Ruby Exercises
[Learn Ruby The Hard Way](http://ruby.learncodethehardway.org/book/) is a great set of small exercises for quickly getting up to speed with Ruby. Work through the end of Lesson 33, but feel free to further if you wish.

## Command Line Exercises
During the InstallFest we noticed that some people were a little uncomfortable at the command line. This is a pretty common issue, with a common solution: practice. The same as author as the Ruby book above wrote [Learn Command Line The Hard Way](http://cli.learncodethehardway.org/book/) which is a great intro to the basics of using the command line to get work done. It is highly recommended that you be at least comfortable at the command line, as much of the Ruby world's tools are command line tools.
