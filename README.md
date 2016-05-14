isomorphic-spotify
============
API library for the Spotify REST API.

Install
---
Install it with npm: `npm install isomorphic-spotify`

API
---
The following will return promises with response object being json

```javascript
lookup: function({ type: 'artist OR album OR track', id: 'Spotify ID Hash' })
```

```javascript
search: function({ type: 'artist OR album OR track', query: 'My search query', limit: 20 })
```

```javascript
get: function(query) -- See http://developer.spotify.com/en/metadata-api/overview/
```

These won't return a promise.  Setting a oauth token will make all subsequent api calls with token.
```javascript
setOAuth: function(token) 
```

```javascript
getOAuth: function() 
```



Example
-------
```javascript
var spotify = require('isomorphic-spotify');

spotify.search({ type: 'track', query: 'dancing in the moonlight' })
    .then(function(data) {
        // ... do something with data
    })
    .catch(function(err){
        // ... handle error
    });
```
