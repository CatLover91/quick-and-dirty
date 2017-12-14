# Learn how to build an API

Sometimes you just want to run your own API from a vps. If you are looking to re-route requests to hide API keys, or just want something online that outputs json, this is how you do it. This readme shows you how to do it quick.

## What you need

1. A vps: Your code needs to run somewhere. I like [linode](https://www.linode.com/) but [digital ocean](https://www.digitalocean.com/) and [vultr](https://www.vultr.com/) are great too.
2. Nodejs: The absolute fastest way to get an api server up. Make sure to install node in the way [your operating system recommends](https://nodejs.org/en/download/package-manager/).

that is literally it

## Set up your project

1. Make a directory in your user account's home directory where you will keep all of the code.
2. `cd mydirectoryname` to change scopes to the project root and then `npm init` to initialize a node project. Just hit enter on the questions npm init asks if you don't care about answering them.
3. Download [app.js](./app.js) template into the folder or make a new file and type it out (it's pretty short).
4. Run `npm install express` in the directory to install express as a dependencies.
5. Run `node app.js` to start the server

You now have a simple server running at http://192.your.ip.1:8080

## Learn how the API works

In `app.js`, a simple express server is defined. Express is used because it is easy to learn and well supported, but you can change this out later if you wish.

Within the express definition, there are a couple settings defined:


First we include our server library for us to use, and then define the instance that we are customizing.
```js
var express = require('express');
var app = express();
```

Then we define a path that represents one of our API endpoints
```js
app.get('/', function(req, res) {
  res.json({ aKey: 'This is the value of aKey' });
});
```
This creates a response that returns the json object `{ aKey: 'This is the value of aKey' }` when the root URL is queried.

Finally we tell our server to start listening at a port, in this case the common 8080. The server is still initialized before this point, but this line initializes the servers capability to accept connections. Remember when using the api that the port comes before the path but after the host. I.E.- if you have a `get` describing `/my-path`, the url would be http://192.my.ip.1:8080/my-path.
```js
app.listen(8080, function(){
  console.log("Example app listening at 8080");
});
```
When you see the console log without any debug stuff consoled out, then you know you are in the clear.

## customize the API

### Change what is output

All you have to do is change what happens in the function within the `app.get`. Flex your javascript knowhow and make something fun. Add extra get's for more paths to handle.

### Make it run in production mode

When you run the application, use the command `NODE_ENV=production node app.js`. This makes node run more stably, but makes it harder to debug due to included caching.

### Make it run in the background

Install [Forever.js](https://github.com/foreverjs/forever). Read the docs on the github, it is easy to use.

### Install nginx

Nginx does so much for you that it is insane. It's easier to use than Apache, super quick, and one of my favorite libraries of all time. Make sure to install it [as is described by your OS](https://www.nginx.com/resources/admin-guide/installing-nginx-open-source/#prebuilt).

Things you can do with it:
* You probably want a domain name for your server, nginx lets you [connect it to your webserver](http://nginx.org/en/docs/http/server_names.html).
* Everything should use HTTPS. Use [certbot](https://certbot.eff.org/) with nginx to easily configure LetsEncrypt-based SSL after installing nginx.
* Use nginx as a reverse proxy: nginx is way more powerful and stable than node when it comes to handling requests. You can use nginx to sit in front of node so that your tiny express server isn't baraged by large amounts of requests. This also obfuscates your port so you don't have that tacky `:8080` at the end of your api URL. [Here is a great tutorial on how to do this](https://medium.com/@utkarsh_verma/configure-nginx-as-a-web-server-and-reverse-proxy-for-nodejs-application-on-aws-ubuntu-16-04-server-872922e21d38).

## That's it

Enjoy.
