# contentful-management.js

Javascript client for [Contentful's](https://www.contentful.com) Content Management API:

- [Documentation](https://www.contentful.com/developers/documentation/content-management-api)

## Install

In node, using [npm](http://npmjs.org):

``` sh
npm install contentful-management
```

Note: The next minor version release of `dist/contentful.min.js` will
be much smaller. Please use a package manager to keep your JS
dependencies up to date and get the newest version right when it's
ready!

## Usage

``` js
var contentful = require('contentful-management');

var client = contentful.createClient({
  // A valid access token for your user
  accessToken: 'b4c0n73n7fu1',

  // Enable or disable SSL. Enabled by default.
  secure: true
});

var log = console.log.bind(console); // wat

// Get Space
client.getSpace('foobar').then(log, log);

// Get all Entries
client.getSpace('foobar').then(function(space) {
  return space.getEntries();
}).then(log, log);
```

For now, please check out the
[Content Management API documentation](https://www.contentful.com/developers/documentation/content-management-api)
to learn how the API and the JavaScript client work.

## License

MIT
