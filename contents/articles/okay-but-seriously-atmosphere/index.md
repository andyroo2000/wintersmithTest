---
title: Okay, but seriously... Atmosphere
author: andrew
date: 2013-11-26
template: article.jade
---

Please forgive the enthusiasm of a newcomer, but I've recently begun poking around and having fun with Meteor.js. While trolling StackOverflow questions tagged 'Meteor' I noticed several people gushing about the wonders of [Atmosphere](https://atmosphere.meteor.com). Since I was still trying to understand the basics of the framework, I figured I should try and work with vanilla Meteor.js until I felt the need to step outside the included packages.

### It started with Bootstrap

It might have taken me longer to see the light, but I decided that I was going to use Bootstrap for my test app, but things were not working as expected... At the time of writing, when you type `meteor add bootstrap` you will be using Bootstrap 2. As I like to be living in the future, this did not work for me.

I could have just put a link to the CDN in my .html file or dropped the Bootstrap 3 files into my project, but I started thinking that I would check the Atmosphere thing everyone was talking about. Sure enough, adding the latest version of Bootstrap was as simple as typing `mrt add bootstrap-3`.

### Default login is meh...

Similarly when I didn't feel like styling the default login screen, I could have uninstalled "accounts-ui" and installed "accounts-ui-unstyled" although that doesn't really give you much control over the styling and I didn't really feel like recreating the login process just to have fine-grained CSS control over the login elements for a test-app.

Again comes Atmosphere to the rescue... There's a package called [accounts-ui-bootstrap](https://atmosphere.meteor.com/package/accounts-ui-bootstrap-3) which instantly makes the login dialog fit in much better with the default Bootstrap aesthetic.

### Need for speed

The list of packages on Atmosphere is impressive for such a young framework and I can't wait to see how the Meteor.js community develops. Already, Meteor.js seems like a good choice for rapidly building modern web-apps with JavaScript on the client and server. Me-te-or... Me-te-or!!!

### The goods

Okay, now that I've hyped it up, here is my first simple Meteor.js app... It's... [drum roll]... a... To-do list. I'm still getting my sea-legs with this whole Meteor.js thing, but I can tell that it's going to be a fun framework to play with.

And here it is... [MyAwesomeApp.js](http://andyroo2000-todo-list.meteor.com/)
