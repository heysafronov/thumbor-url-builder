# Thumbor URL builder
Thumbor client for JavaScript.

## Install

```
npm i thumbor-js-url-builder
```

## Declare in JS

```js
// declare in JS

import Thumbor from 'thumbor-js-url-builder'
const thumbor = new Thumbor('my_key', 'https://my-site.com/thumbs')
```

## Generate your URL

```js
// generate your url

 const thumborize = thumbor
   .filter('format(webp)')
   .setImagePath('https://my-image-url.com/img.jpg')
   .resize(600, 400)
   .buildUrl()
```

## `Example`

```js
// .env

thumborKey="gr4mf3t3gsg4g3g3d3d"
thumborUrl="https://my-site.com/thumbs"

// thumborize.js 

import Thumbor from 'thumbor-js-url-builder'
const thumbor = new Thumbor(process.env.thumborKey, process.env.thumborUrl)

const thumborize = (type = 'jpeg', url, num = 1, width = 600, height = 400) => {
  return thumbor
    .filter(`format(${type})`)
    .setImagePath(url)
    .resize(width * num, height * num)
    .buildUrl()
}

export default thumborize
```