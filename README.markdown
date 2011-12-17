# Google Reader RSS Feed for Google+'d Items

This tool is to fill a specific need to reproduce the Google Reader RSS feed functionality
so it can be used with publishing tools like dlvr.it which was broken when Google switched
to the G+ method of sharing.

This tool is a fork of https://github.com/frosas/google-plus-user-feed which is a node.js
based application to create a RSS feed of all your public G+ posts

## Changes made

I created another URL path that will just return items that are posted by Google Reader.
The one nice thing with with the G+ json result is that it has a lot of meta data to
include the provider who posted the item to your G+ feed.  The new url is
http://<server:port>/googlereader/<G+ profile id>

## Install instructions

These instructions are how to deploy to Heroku

1. Clone this repo with your favorite Git client
2. Follow the steps on the Heroku Node.js page: http://devcenter.heroku.com/articles/node-js
3. ...
