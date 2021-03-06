# Offline

> To make web apps work offline use **Cache Manifest**

## Manifest file

- **CACHE MANIFEST** - Files listed under this header will be cached after they are downloaded for the first time.
- **NETWORK** - Files listed under this header require a connection to the server, and will *never* be cached.
- **FALLBACK** - Files listed under this header specifies fallback pages if a page is inaccessible.


### Example

```
CACHE MANIFEST:
/theme.css
/logo.gif
/main.js

NETWORK:
login.js

FALLBACK:
/html/ offline.html   # would serve offline.html as a fallback
```

## Overriding cache

> Once an application is cached, it remains cached until one of the following happens:

- The user clears the browser's cache
- The manifest file is modified
- The application cache is programmatically updated

