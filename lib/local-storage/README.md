local-storage
=============

This is a very simple polyfill that implements the core methods of localStorage
when the native API is either unavailable or not working correctly (e.g., safari in private mode):

```
localStorage.setItem( key, value )
localStorage.getItem( key )
localStorage.removeItem( key )
localStorage.clear()
localStorage.length
```

Just require and call this once into the page (prior to any calls to these methods) and
it will either create or augment the `window.localStorage` object as necessary.

```
var localStoragePolyfill = require( 'react-test-env-setup/lib/local-storage' )();
```