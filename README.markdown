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

0. You need a Google API key in order to run this application.  Go to https://developers.google.com/+/api/ to sign up for your key
1. Clone this repo with your favorite Git client
2. Follow steps on the Heroku Node.js page: http://devcenter.heroku.com/articles/node-js. Below is a summary
2.1 heroku create --stack cedar
2.2 git push heroku master
2.2.1 You will see Heroku deploy that app.  The last line will be the URL of the deployed app
2.3 heroku ps
2.3.1 This will verify that the app is running
3. Run the command: heroku config:add NODE_ENV=production
4. Run the command: heroku config:add GOOGLE_API_KEY=[api key]
5. Open your web browser
