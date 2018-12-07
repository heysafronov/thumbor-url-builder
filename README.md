# Thumbor URL builder
Thumbor client for JavaScript.

## Usage

```$xslt
# install

npm i thumbor-js-url-builder
```

```
# declare thumbor-js-url-builder in JS

import Thumbor from 'thumbor'
const thumbor = new Thumbor('my_key', https://mysite.com/thumbs)

# generate your url

 const thumborize = thumbor
   .filter(format(webp)')
   .setImagePath('https://myimageurl.com/img.jpg')
   .resize(200, 300)
   .buildUrl()
```