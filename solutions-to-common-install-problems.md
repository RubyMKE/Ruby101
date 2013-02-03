# Installfest - Solutions to Common Problems

During the installfest for 101, we ran into a couple of common issues. This page attempts to catallog the problems and, if possible, provide a solution.


## RVM isn't working on Ubuntu
Many people on Ubuntu got to the point, around [Step 4](http://docs.railsbridge.org/installfest/ubuntu), in the installfest where you run: `type rvm |head -1`

The expected output is: `rvm is a function`

Instead, many people see: `rvm is hashed`

This is because the terminal application on Ubuntu 12.04 and later does not start the shell as a 'login shell'. To fix this, go to the Terminal, then up in the menu choose Edit -> Profile Preferences. From here, select the 'Title and Command' tab, then select the checkbox next to 'Run command as a login shell'. After this, restart your terminal and the above `type rvm` command should work as expected.


## Rails 4.0 Deprecation Warning During Heroku db:migrate
When running `heroku run rake db:migrate`, you may see an error message like the following:
```
DEPRECATION WARNING: You have Rails 2.3-style plugins in vendor/plugins! Support for these plugins will be removed in
Rails 4.0. Move them out and bundle them in your Gemfile, or fold them in to your app as lib/myplugin/* and config
/initializers/myplugin.rb. See the release notes for more on this: 
http://weblog.rubyonrails.org/2012/1/4/rails-3-2-0-rc2-has-been-released.
(called from <top (required)> at /app/Rakefile:7)
```

This is to let you know that once Rails 4 comes out, plugins in the vendor/plugins directory will not work. However, for this course we will not be using any plugins or worrying about Rails 4, so this problem can be safely ignored.



To silence the issues, open the file `conf/environments/production.rb` and add the following (near the top, between the `do` and `end`):

`ActiveSupport::Deprecation.silenced = true`

Note: This doesn't actually work ;)
Todo: Figure this out


## Javascript problems on Windows 8
TBD

## OS X Ruby Compilation Problems
TBD
