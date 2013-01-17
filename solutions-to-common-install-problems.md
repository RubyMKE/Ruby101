# Installfest - Solutions to Common Problems

During the installfest for 101, we ran into a couple of common issues. This page attempts to catallog the problems and, if possible, provide a solution.


## RVM isn't working on Ubuntu
Many people on Ubuntu got to the point, around [Step 4](http://docs.railsbridge.org/installfest/ubuntu), in the installfest where you run: `type rvm |head -1`

The expected output is: `rvm is a function`

Instead, many people see: `rvm is hashed`

This is because the terminal application on Ubuntu 12.04 and later does not start the shell as a 'login shell'. To fix this, go to the Terminal, then up in the menu choose Edit -> Profile Preferences. From here, select the 'Title and Command' tab, then select the checkbox next to 'Run command as a login shell'. After this, restart your terminal and the above `type rvm` command should work as expected.


## Rails 4.0 Deprecation Warning During Heroku db:migrate
Some people got deprecation warnings when they run `heroku run rake db:migrate`. This is to let you know that once Rails 4 comes out, this method won't work. However, for this course we'll be working strictly on Rails 3, so this problem can be safely ignored.

To silence the issues, open the file `conf/environment/production.rb` and add the following (near the top, between the `do` and `end`):

`ActiveSupport::Deprecation.silenced = true`


## Javascript problems on Windows 8
TBD

## OS X Ruby Compilation Problems
TBD
