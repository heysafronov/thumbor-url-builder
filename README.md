# Thumbor URL builder
Thumbor client for JavaScript.

## Install

```
npm i thumbor-js-url-builder
```

## Declare in JS

```js
// declare in JS

import Thumbor from 'thumbor'
const thumbor = new Thumbor('my_key', 'https://my-site.com/thumbs')
```

## Generate your URL

```js
// generate your url

 const thumborize = thumbor
   .filter('format(webp)')
   .setImagePath('https://my-image-url.com/img.jpg')
   .resize(200, 300)
   .buildUrl()
```

## `**Example**`