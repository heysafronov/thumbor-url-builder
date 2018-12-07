# Thumbor URL builder
Thumbor client for JavaScript.

## Install

```
// install

npm i thumbor-js-url-builder
```

## Declare in JS

```js
// declare in JS

import Thumbor from 'thumbor'
const thumbor = new Thumbor('my_key', https://mysite.com/thumbs)
```

## Generate your URL

```js
// generate your url

 const thumborize = thumbor
   .filter('format(webp)')
   .setImagePath('https://myimageurl.com/img.jpg')
   .resize(200, 300)
   .buildUrl()
```