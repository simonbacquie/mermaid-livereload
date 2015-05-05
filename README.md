# mermaid-livereload

Simple premade template for creating flowcharts in plain text, that get rendered in a browser by [Mermaid](http://knsv.github.io/mermaid/flowchart.html). Packaged as a Sinatra app with Guard and guard-livereload, so that your browser will auto-reload every time you save a change to your flowchart.

## Requirements

Ruby, and Bundler.

## Usage

    bundle install
    bundle exec rackup
    
..to install dependencies, and start the Sinatra app. Leave that running, then in another terminal:

    bundle exec guard start
    
Your flowcharts go in the public folder. Try out the included flowchart.html to get started.

On file save, you should see some feedback in your Guard console letting you know that a refresh was sent to the browser.
