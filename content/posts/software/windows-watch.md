Title: Watch on Windows?
Date: 2019-07-10 12:00pm
Category: Software
Tags: watch, windows, automation
Summary: Using watchexec as an alterative to watch.

In a previous post I mentioned using [http server](/python-http-server.html) as a quick way to test my changes in my Pelican Blog.

This has been a nice and simple solution as I only have to run one command: `make html` to re-generate the files to be served.

However I recently found out by someone about the `watch` command, which is a built-in command in Linux to run any arbitrary command at regular intervals.

This is awesome to hear about because rather then manually running `make html` every time I make a change to test it on the server, I can just have the `watch` command watch my files to automatically re-generate!

Another cool feature that Linux has, but for every other OS there is [watchexec](https://github.com/watchexec/watchexec), a simple, standalone tool that watches a path and runs a command whenever it detects modifications. Exactly what I need!

I installed it following the [Windows intallation](https://github.com/watchexec/watchexec#Windows) by [using scoop](https://scoop.sh/)

Then for this Pelican Blog, in the main folder:
```
 watchexec -i output make html
 ```

 Then I create a python http server to run it on, and now any time I change my files they will be automatically regenerated.