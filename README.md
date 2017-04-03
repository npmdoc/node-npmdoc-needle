# api documentation for  [needle (v1.6.0)](https://github.com/tomas/needle#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-needle.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-needle) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-needle.svg)](https://travis-ci.org/npmdoc/node-npmdoc-needle)
#### The leanest and most handsome HTTP client in the Nodelands.

[![NPM](https://nodei.co/npm/needle.png?downloads=true)](https://www.npmjs.com/package/needle)

[![apidoc](https://npmdoc.github.io/node-npmdoc-needle/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-needle_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-needle/build..beta..travis-ci.org/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-needle/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-needle/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Tomás Pollak",
        "email": "tomas@forkhq.com"
    },
    "bin": {
        "needle": "./bin/needle"
    },
    "bugs": {
        "url": "https://github.com/tomas/needle/issues"
    },
    "dependencies": {
        "debug": "^2.1.2",
        "iconv-lite": "^0.4.4"
    },
    "description": "The leanest and most handsome HTTP client in the Nodelands.",
    "devDependencies": {
        "JSONStream": "",
        "jschardet": "",
        "mocha": "",
        "q": "",
        "should": "",
        "sinon": "",
        "xml2js": ""
    },
    "directories": {
        "lib": "./lib"
    },
    "dist": {
        "shasum": "f52a5858972121618e002f8e6384cadac22d624f",
        "tarball": "https://registry.npmjs.org/needle/-/needle-1.6.0.tgz"
    },
    "engines": {
        "node": ">= 0.10.x"
    },
    "gitHead": "f801ef68c707639d7fffbd5e147cc6abcd6fbeca",
    "homepage": "https://github.com/tomas/needle#readme",
    "keywords": [
        "http",
        "https",
        "simple",
        "request",
        "client",
        "multipart",
        "upload",
        "proxy",
        "deflate",
        "timeout",
        "charset",
        "iconv",
        "cookie",
        "redirect"
    ],
    "license": "MIT",
    "main": "./lib/needle",
    "maintainers": [
        {
            "name": "tomas",
            "email": "tomas@forkhq.com"
        }
    ],
    "name": "needle",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/tomas/needle.git"
    },
    "scripts": {
        "test": "mocha test"
    },
    "tags": [
        "http",
        "https",
        "simple",
        "request",
        "client",
        "multipart",
        "upload",
        "proxy",
        "deflate",
        "timeout",
        "charset",
        "iconv",
        "cookie",
        "redirect"
    ],
    "version": "1.6.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module needle](#apidoc.module.needle)
1.  [function <span class="apidocSignatureSpan">needle.</span>defaults (obj)](#apidoc.element.needle.defaults)
1.  [function <span class="apidocSignatureSpan">needle.</span>delete (uri, data, options, callback)](#apidoc.element.needle.delete)
1.  [function <span class="apidocSignatureSpan">needle.</span>get (uri, options, callback)](#apidoc.element.needle.get)
1.  [function <span class="apidocSignatureSpan">needle.</span>head (uri, options, callback)](#apidoc.element.needle.head)
1.  [function <span class="apidocSignatureSpan">needle.</span>patch (uri, data, options, callback)](#apidoc.element.needle.patch)
1.  [function <span class="apidocSignatureSpan">needle.</span>post (uri, data, options, callback)](#apidoc.element.needle.post)
1.  [function <span class="apidocSignatureSpan">needle.</span>put (uri, data, options, callback)](#apidoc.element.needle.put)
1.  [function <span class="apidocSignatureSpan">needle.</span>request (method, uri, data, opts, callback)](#apidoc.element.needle.request)
1.  object <span class="apidocSignatureSpan">needle.</span>auth
1.  object <span class="apidocSignatureSpan">needle.</span>cookies
1.  object <span class="apidocSignatureSpan">needle.</span>multipart
1.  object <span class="apidocSignatureSpan">needle.</span>querystring
1.  string <span class="apidocSignatureSpan">needle.</span>version

#### [module needle.auth](#apidoc.module.needle.auth)
1.  [function <span class="apidocSignatureSpan">needle.auth.</span>basic (user, pass)](#apidoc.element.needle.auth.basic)
1.  [function <span class="apidocSignatureSpan">needle.auth.</span>digest (header, user, pass, method, path)](#apidoc.element.needle.auth.digest)
1.  [function <span class="apidocSignatureSpan">needle.auth.</span>header (header, credentials, opts)](#apidoc.element.needle.auth.header)

#### [module needle.cookies](#apidoc.module.needle.cookies)
1.  [function <span class="apidocSignatureSpan">needle.cookies.</span>read (header)](#apidoc.element.needle.cookies.read)
1.  [function <span class="apidocSignatureSpan">needle.cookies.</span>write (obj)](#apidoc.element.needle.cookies.write)

#### [module needle.multipart](#apidoc.module.needle.multipart)
1.  [function <span class="apidocSignatureSpan">needle.multipart.</span>build (data, boundary, callback)](#apidoc.element.needle.multipart.build)

#### [module needle.querystring](#apidoc.module.needle.querystring)
1.  [function <span class="apidocSignatureSpan">needle.querystring.</span>build (obj, prefix)](#apidoc.element.needle.querystring.build)



# <a name="apidoc.module.needle"></a>[module needle](#apidoc.module.needle)

#### <a name="apidoc.element.needle.defaults"></a>[function <span class="apidocSignatureSpan">needle.</span>defaults (obj)](#apidoc.element.needle.defaults)
- description and source-code
```javascript
defaults = function (obj) {
  for (var key in obj) {
    var target_key = aliased.options[key] || key;

    if (defaults.hasOwnProperty(target_key) && typeof obj[key] != 'undefined') {
      if (target_key != 'parse_response' && target_key != 'proxy') {
        // ensure type matches the original, except for proxy/parse_response that can be null/bool or string
        var valid_type = defaults[target_key].constructor.name;

        if (obj[key].constructor.name != valid_type)
          throw new TypeError('Invalid type for ' + key + ', should be ' + valid_type);
      }
      defaults[target_key] = obj[key];
    }
  }

  return defaults;
}
```
- example usage
```shell
...

Overriding Defaults
-------------------

Yes sir, we have it. Needle includes a 'defaults()' method, that lets you override some of the defaults for all future requests.
Like this:

'''js
needle.defaults({
  open_timeout: 60000,
  user_agent: 'MyApp/1.2.3',
  parse_response: false });
'''

This will override Needle's default user agent and 10-second timeout, and disable response parsing, so you don't need to pass those
 options in every other request.
...
```

#### <a name="apidoc.element.needle.delete"></a>[function <span class="apidocSignatureSpan">needle.</span>delete (uri, data, options, callback)](#apidoc.element.needle.delete)
- description and source-code
```javascript
delete = function (uri, data, options, callback) {
  return new Needle(method, uri, data, options, callback).start();
}
```
- example usage
```shell
...
});
'''

### needle.patch(url, data[, options][, callback])

Same behaviour as PUT.

### needle.delete(url, data[, options][, callback])

'''js
var options = {
  username: 'fidelio',
  password: 'x'
}
...
```

#### <a name="apidoc.element.needle.get"></a>[function <span class="apidocSignatureSpan">needle.</span>get (uri, options, callback)](#apidoc.element.needle.get)
- description and source-code
```javascript
get = function (uri, options, callback) {
  return new Needle(method, uri, null, options, callback).start();
}
```
- example usage
```shell
...
[![NPM](https://nodei.co/npm/needle.png)](https://nodei.co/npm/needle/)

The leanest and most handsome HTTP client in the Nodelands.

'''js
var needle = require('needle');

needle.get('http://www.google.com', function(error, response) {
  if (!error && response.statusCode == 200)
    console.log(response.body);
});
'''

Callbacks not floating your boat? Needle got your back.
...
```

#### <a name="apidoc.element.needle.head"></a>[function <span class="apidocSignatureSpan">needle.</span>head (uri, options, callback)](#apidoc.element.needle.head)
- description and source-code
```javascript
head = function (uri, options, callback) {
  return new Needle(method, uri, null, options, callback).start();
}
```
- example usage
```shell
...
'''

API
---

All of Needle's request methods return a Readable stream, and both 'options' and 'callback' are optional. If passed, the callback
 will return three arguments: 'error', 'response' and 'body', which is basically an alias for 'response.body'.

### needle.head(url[, options][, callback])

'''js
var options = {
  open_timeout: 5000 // if we don't get our response headers in 5 seconds, boom.
}

needle.head('https://my.backend.server.com', function(err, resp) {
...
```

#### <a name="apidoc.element.needle.patch"></a>[function <span class="apidocSignatureSpan">needle.</span>patch (uri, data, options, callback)](#apidoc.element.needle.patch)
- description and source-code
```javascript
patch = function (uri, data, options, callback) {
  return new Needle(method, uri, data, options, callback).start();
}
```
- example usage
```shell
...
}

needle.put('https://api.app.com/v2', nested, function(err, resp) {
  console.log('Got ' + resp.bytes + ' bytes.') // another nice treat from this handsome fella.
});
'''

### needle.patch(url, data[, options][, callback])

Same behaviour as PUT.

### needle.delete(url, data[, options][, callback])

'''js
var options = {
...
```

#### <a name="apidoc.element.needle.post"></a>[function <span class="apidocSignatureSpan">needle.</span>post (uri, data, options, callback)](#apidoc.element.needle.post)
- description and source-code
```javascript
post = function (uri, data, options, callback) {
  return new Needle(method, uri, data, options, callback).start();
}
```
- example usage
```shell
...
'''js
var data = {
  file: '/home/johnlennon/walrus.png',
  content_type: 'image/png'
};

needle
  .post('https://my.server.com/foo', data, { multipart: true })
  .on('readable', function() { /* eat your chunks */ })
  .on('done', function() {
    console.log('Ready-o, friend-o.');
  })
'''

With only one real dependency, Needle supports:
...
```

#### <a name="apidoc.element.needle.put"></a>[function <span class="apidocSignatureSpan">needle.</span>put (uri, data, options, callback)](#apidoc.element.needle.put)
- description and source-code
```javascript
put = function (uri, data, options, callback) {
  return new Needle(method, uri, data, options, callback).start();
}
```
- example usage
```shell
...
}

needle.post('https://my.app.com/endpoint', 'foo=bar', options, function(err, resp) {
// you can pass params as a string or as an object.
});
'''

### needle.put(url, data[, options][, callback])

'''js
var nested = {
params: {
  are: {
    also: 'supported'
  }
...
```

#### <a name="apidoc.element.needle.request"></a>[function <span class="apidocSignatureSpan">needle.</span>request (method, uri, data, opts, callback)](#apidoc.element.needle.request)
- description and source-code
```javascript
request = function (method, uri, data, opts, callback) {
  return new Needle(method, uri, data, opts, callback).start();
}
```
- example usage
```shell
...
}

needle.delete('https://api.app.com/messages/123', null, options, function(err, resp) {
// in this case, data may be null, but you need to explicity pass it.
});
'''

### needle.request(method, url, data[, options][, callback])

Generic request. This not only allows for flexibility, but also lets you perform a GET request with data, in which case will be
appended to the request as a query string, unless you pass a 'json: true' option (read below).

'''js
var params = {
q    : 'a very smart query',
page : 2
...
```



# <a name="apidoc.module.needle.auth"></a>[module needle.auth](#apidoc.module.needle.auth)

#### <a name="apidoc.element.needle.auth.basic"></a>[function <span class="apidocSignatureSpan">needle.auth.</span>basic (user, pass)](#apidoc.element.needle.auth.basic)
- description and source-code
```javascript
function basic(user, pass) {
  var str  = typeof pass == 'undefined' ? user : [user, pass].join(':');
  return 'Basic ' + new Buffer(str).toString('base64');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.needle.auth.digest"></a>[function <span class="apidocSignatureSpan">needle.auth.</span>digest (header, user, pass, method, path)](#apidoc.element.needle.auth.digest)
- description and source-code
```javascript
digest = function (header, user, pass, method, path) {

  var nc        = 1,
      cnonce    = null,
      challenge = digest.parse_header(header);

  var ha1  = md5(user + ':' + challenge.realm + ':' + pass),
      ha2  = md5(method.toUpperCase() + ':' + path),
      resp = [ha1, challenge.nonce];

  if (typeof challenge.qop === 'string') {
    cnonce = md5(Math.random().toString(36)).substr(0, 8);
    nc     = digest.update_nc(nc);
    resp   = resp.concat(nc, cnonce);
  }

  resp = resp.concat(challenge.qop, ha2);

  var params = {
    uri      : path,
    realm    : challenge.realm,
    nonce    : challenge.nonce,
    username : user,
    response : md5(resp.join(':'))
  }

  if (challenge.qop) {
    params.qop = challenge.qop;
  }

  if (challenge.opaque) {
    params.opaque = challenge.opaque;
  }

  if (cnonce) {
    params.nc = nc;
    params.cnonce = cnonce;
  }

  header = []
  for (var k in params)
    header.push(k + '="' + params[k] + '"')

  return 'Digest ' + header.join(', ');
}
```
- example usage
```shell
...
  }
}

////////////////////
// basic

function md5(string) {
  return createHash('md5').update(string).digest('hex');
}

function basic(user, pass) {
  var str  = typeof pass == 'undefined' ? user : [user, pass].join(':');
  return 'Basic ' + new Buffer(str).toString('base64');
}
...
```

#### <a name="apidoc.element.needle.auth.header"></a>[function <span class="apidocSignatureSpan">needle.auth.</span>header (header, credentials, opts)](#apidoc.element.needle.auth.header)
- description and source-code
```javascript
function get_header(header, credentials, opts) {
  var type = header.split(' ')[0],
      user = credentials[0],
      pass = credentials[1];

  if (type == 'Digest') {
    return digest.generate(header, user, pass, opts.method, opts.path);
  } else if (type == 'Basic') {
    return basic(user, pass);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.needle.cookies"></a>[module needle.cookies](#apidoc.module.needle.cookies)

#### <a name="apidoc.element.needle.cookies.read"></a>[function <span class="apidocSignatureSpan">needle.cookies.</span>read (header)](#apidoc.element.needle.cookies.read)
- description and source-code
```javascript
function parseSetCookieHeader(header) {
  if (!header) return {};
  header = (header instanceof Array) ? header : [header];

  return header.reduce(function(res, str) {
    var cookie = parseSetCookieString(str);
    if (cookie) res[cookie.name] = cookie.value;
    return res;
  }, {});
}
```
- example usage
```shell
...
rejectUnauthorized : true  // verify SSL certificate
}

var stream = needle.get('https://backend.server.com/everything.html', options);

// read the chunks from the 'readable' event, so the stream gets consumed.
stream.on('readable', function() {
while (data = this.read()) {
  console.log(data.toString());
}
})

stream.on('done', function(err) {
// if our request had an error, our 'done' event will tell us.
if (!err) console.log('Great success!');
...
```

#### <a name="apidoc.element.needle.cookies.write"></a>[function <span class="apidocSignatureSpan">needle.cookies.</span>write (obj)](#apidoc.element.needle.cookies.write)
- description and source-code
```javascript
function writeCookieString(obj) {
  return Object.keys(obj).reduce(function(str, name) {
    var encodedName  = encodeCookieComponent(name);
    var encodedValue = encodeCookieComponent(obj[name]);
    str += (str ? '; ' : '') + encodedName + '=' + encodedValue;
    return str;
  }, '');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.needle.multipart"></a>[module needle.multipart](#apidoc.module.needle.multipart)

#### <a name="apidoc.element.needle.multipart.build"></a>[function <span class="apidocSignatureSpan">needle.multipart.</span>build (data, boundary, callback)](#apidoc.element.needle.multipart.build)
- description and source-code
```javascript
build = function (data, boundary, callback) {

  if (typeof data != 'object' || typeof data.pipe == 'function')
    return callback(new Error('Multipart builder expects data as key/val object.'));

  var body   = '',
      object = flatten(data),
      count  = Object.keys(object).length;

  if (count === 0)
    return callback(new Error('Empty multipart body. Invalid data.'))

  function done(err, section) {
    if (err) return callback(err);
    if (section) body += section;
    --count || callback(null, body + '--' + boundary + '--');
  };

  for (var key in object) {

    var value = object[key];
    if (value === null || typeof value == 'undefined') {
      done();
    } else {
      var part = (value.buffer || value.file || value.content_type) ? value : {value: value};
      generate_part(key, part, boundary, done);
    }
  }

}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.needle.querystring"></a>[module needle.querystring](#apidoc.module.needle.querystring)

#### <a name="apidoc.element.needle.querystring.build"></a>[function <span class="apidocSignatureSpan">needle.querystring.</span>build (obj, prefix)](#apidoc.element.needle.querystring.build)
- description and source-code
```javascript
function stringify(obj, prefix) {
  if (prefix && (obj === null || typeof obj == 'undefined')) {
    return prefix + '=';
  } else if (toString.call(obj) == '[object Array]') {
    return stringifyArray(obj, prefix);
  } else if (toString.call(obj) == '[object Object]') {
    return stringifyObject(obj, prefix);
  } else if (toString.call(obj) == '[object Date]') {
    return obj.toISOString();
  } else if (prefix) { // string inside array or hash
    return prefix + '=' + encodeURIComponent(String(obj));
  } else if (String(obj).indexOf('=') !== -1) { // string with equal sign
    return String(obj);
  } else {
    throw new TypeError('Cannot build a querystring out of: ' + obj);
  }
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
