# get-youtube-id

Parse a youtube url returning the video ID.

## Installation

```
npm install get-youtube-id
```

## Example

``` js
var getYouTubeID = require('get-youtube-id');

var id = getYouTubeID("http://www.youtube.com/watch?v=9bZkp7q19f0");
console.log(id); // "9bZkp7q19f0"


// Or, if you're using ES6 syntax:
import getYouTubeID from 'get-youtube-id';
```

## Fuzzy matching

By default `getYouTubeID` will make a last-ditch effort to look for anything that resembles
an 11-character id. If you want it to be more strict you can turn this off with an options
argument.

```js
var getYouTubeID = require('get-youtube-id');

var id = getYouTubeID("youtube abcdefghijk", {fuzzy: false});
console.log(id); // null
```

# License

MIT
