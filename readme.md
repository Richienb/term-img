# term-img [![Build Status](https://travis-ci.org/sindresorhus/term-img.svg?branch=master)](https://travis-ci.org/sindresorhus/term-img)

> Display images in iTerm

You probably want the higher-level [terminal-image](https://github.com/sindresorhus/terminal-image) module for displaying your images.

![](screenshot.jpg)

Even [animated gifs](https://github.com/vdemedes/gifi)!

*Currently only supported on [iTerm >=3](https://www.iterm2.com/downloads.html).*


## Install

```
$ npm install term-img
```


## Usage

```js
const termImg = require('term-img');

function fallback() {
	// Return something else when not supported
}

console.log(termImg('unicorn.jpg', {fallback}));
```


## API

### termImg(image, [options])

Get the image as a `string` that you can log manually.

#### image

Type: `string | Buffer`

Filepath to an image or an image as a buffer.

#### options

##### width
##### height

Type: `'auto' | string | number`

The width and height are given as a number followed by a unit, or the word `'auto'`.

- `N`: N character cells.
- `Npx`: N pixels.
- `N%`: N percent of the session's width or height.
- `auto`: The image's inherent size will be used to determine an appropriate dimension.

##### preserveAspectRatio

Type: `boolean`<br>
Default: `true`

##### fallback

Type: `Function`<br>
Default: `() => throw new UnsupportedTerminalError()`

Enables you to do something else when the terminal doesn't support images.


## Related

- [term-img-cli](https://github.com/sindresorhus/term-img-cli) - CLI for this module


## License

MIT © [Sindre Sorhus](https://sindresorhus.com)
