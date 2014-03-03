---
title: What's So Great About Gulp?
author: andrew
date: 2014-02-22
template: article.jade
---


If you have been keeping up with the latest tools in web-development, you've probably heard that [gulp.js](http://gulpjs.com) is poised to take the throne from [Grunt.js](http://gruntjs.com) as the world's favorite automated task-runner.

While some complain about the onslaught of new tools that basically do the same things as tools that seem to be working okay, I have to say that gulp is worth looking into.

#### Wait, what does it do?

Okay, maybe you aren't using Grunt.js right now, and you aren't really sure what exactly these task-runners do.

In short, you specify a bunch of things that you want to happen to a bunch of files and the task-runner makes it happen in the background without you having to think about it again. The types of things I use them for include:

- convert **jade** files to **html** and **minified html**
- convert **stylus** files to **CSS** and **minified CSS**
- apply the incredible **autoprefixer** plugin to the compiled **CSS**
- convert **javascript** files to **uglified javascript**
- run **jshint** on **javascript** files on **save**

#### What does gulp do better than Grunt?

The first thing is subjective, but for me, it's much easier to use. Rather than specifying configuration in an object in a Grunt.js file, you use Node.js streams and simply pipe the data through various plugins. Each of these plugins performs only one task and they can be chained together in any way that you can imagine. Especially, if you have any Node.js experience, piping data will seem much more intuitive than setting configuration objects in Grunt.

The second thing is not so subjective. It's significantly faster than Grunt. In many cases, it is orders of magnitute faster.

##### Here is why:

Let's say that you want to perform 7 different transformations on a file before writing another file. With Grunt, each plugin will write to a temporary file that the next plugin will process. Hitting the file system for each transformation is expensive.

Now let's say that you want to perform the same tasks using gulp. Now we're using Node.js streams, so the data is kept in RAM as it's passed from one plugin to the next until it finally writes to the output file.

I've personally seen a large-scale app's build time go from 3.5 seconds using Grunt to less than one second by switching the build processes to gulp.js.

#### How do I get started?

Head on over to [gulpjs.com](http://gulpjs.com) and check out the examples. It's pretty easy to get started. Just for kicks, I made a project template and my first gulp file, so this could give you some ideas, as well:

[my gulp file](https://github.com/andyroo2000/JadeProjectStarter/blob/master/gulpfile.js)
