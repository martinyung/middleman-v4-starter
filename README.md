# Middleman V4 Starter
Middleman V4 has updated the [asset pipeline](https://middlemanapp.com/advanced/external-pipeline/) and thus making alot of ruby gems not working.

Here's a simple starter for activating sprockets and integrating jquery, susy and bootstrap using bower

**This starter includes:**
* [Livereload](http://livereload.com): Automatically refresh your browser whenever you edit your files.
* [Slim](http://slim-lang.com): A lightweight templating engine.
* [Bower](http://bower.io): A package manager for the web.
* [Sass](http://sass-lang.com): Syntactically Awesome Style Sheets
* [Bootstrap-sass](https://github.com/twbs/bootstrap-sass): Powerful frontend framework
* [Susy](http://susy.oddbird.net): Lighter grid layout design
* [Jquery](https://jquery.com/): Fast, small, and feature-rich JavaScript library.
* [Fontawesome](http://fontawesome.io/): The iconic font and CSS toolkit.

## Installation

```
git clone https://github.com/martinyung/middleman-v4-starter.git [your_app_name]
```

```
gem install bundler
```

Finally, do a ```bundle install``` to install the required gems

## Description

Here's the configuration needed when upgrading to middleman v4.

in /Gemfile add:

```
gem 'middleman-sprockets', '~> 4.1.0'
```

Activate sprockets and include bower_components path in asset pipeline

in /config.rb, add:

```
activate :sprockets
sprockets.append_path File.join root.to_s, "bower_components"
```

Import the require files in site.css and site.js

Example:

in /source/stylesheets/site.css.sass

```
@import 'bootstrap-sass/assets/stylesheets/bootstrap'
```

in /source/javascripts/site.js

```
//= require jquery/dist/jquery.min.js
```

And that's it, you are good to go!

