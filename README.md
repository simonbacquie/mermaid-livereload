# mermaid-livereload

Simple premade template for creating flowcharts in plain text, that get rendered in a browser by [Mermaid](http://knsv.github.io/mermaid/flowchart.html). Packaged as a Sinatra app with Guard and guard-livereload, so that your browser will auto-reload every time you save a change to your flowchart.

## Requirements

Ruby, and Bundler.

## Usage

    bundle install
    bundle exec rackup
    
..to install dependencies, and start the Sinatra app. Leave that running, then in another terminal:

    bundle exec guard start
    
Your flowcharts go in the public folder. Try out the included flowchart.html to get started:

    http://localhost:9292/flowchart.html

On file save, you should see some feedback in your Guard console letting you know that a refresh was sent to the browser.

## FAQ

#### Why did this have to have a Sinatra app?
LiveReload.js doesn't like files that are opened straight from the filesystem with file://, so Sinatra serving them up is so that the URL can be "localhost". If you don't want to run a Sinatra app, you can use a LiveReload browser plugin instead of LiveReload.js, but it's not as nice.

#### Why did you use Guard and not Grunt?
Because I work more with Ruby these days.
