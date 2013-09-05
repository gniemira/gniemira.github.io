---
layout: post
title:  "How to Get Around Precompile Issues on Heroku"
date:   2013-08-31
---

Rails SASS and Heroku don't always play nicely. When compiling, Heroku may try to connect to the DB for some reason, which causes Heroku to puke on your asset precompilation. If you must use SASS and you must use Heroku, but you don't want to manually compile the assets, there's a nice little workaround.

From your command prompt, enter the following:

```
heroku labs:enable user-env-compile
```

This will enable a Heroku labs plug in that does away with all this BS and does the asset precompile stuff like normal.
