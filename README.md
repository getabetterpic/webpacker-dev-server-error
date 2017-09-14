# README

* Ruby version => 2.4.0

* System dependencies => Yarn

## Steps to reproduce

1. Run `bundle install` and `yarn install` to install dependencies.
1. Start server in one terminal: `rails s`
1. Go to [localhost:3000/hello_world](http://localhost:3000/hello_world)
1. Open dev tools. Should see the webpacker hello world message in console.
1. While leaving the rails server running, in another terminal start the webpack dev server: `./bin/webpack-dev-server`
1. Refresh the page. Should still see the webpacker hello world message in console.
1. Stop the webpack dev server.
1. Refresh the page again. Now browser complains about not being able to find the application pack.

## Problem

After starting the webpack dev server then quitting, webpack no longer serves the correct packs automatically.

## Expected behaviour

The background webpack service should continue serving the correct packs after quitting the webpack dev server.
