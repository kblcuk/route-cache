[![Build Status](https://travis-ci.org/bradoyler/route-cache.svg?branch=master)](https://travis-ci.org/bradoyler/route-cache)

# Route-Cache
Simple middleware for Express route caching with a given TTL (in seconds)

Make your routes do this ->![dodging](http://gifs.gifbin.com/1234778873_Muhammad_Ali_dodging_punches.gif)

## Why?
- makes hard-working routes super-fast, under heavy-load
- easy to use and fork for your needs
- works with gzip compression

## Install
```sh
npm install route-cache
```

## Test
```sh
npm test
```

## How to use
```javascript

var routeCache = require('route-cache');

// cache route for 20 seconds
app.get('/index', routeCache.cacheSeconds(20), function(req, res){
	// do your dirty work here...
	console.log('you will only see this every 20 seconds.');
	res.send('this response will be cached');
});


```

## Future plans / todos
- client-side Cache-Control
- support for distributed caches (redis or memcache)

------
The MIT License (MIT)

Copyright (c) 2014 Brad Oyler

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
