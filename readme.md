# [gulp](https://github.com/wearefractal/gulp)-template [![Build Status](https://secure.travis-ci.org/sindresorhus/gulp-template.png?branch=master)](http://travis-ci.org/sindresorhus/gulp-template)

> Compile [Lodash templates](http://lodash.com/docs#template)

*Lodash is like Underscore, but faster and better.*


## Install

Install with [npm](https://npmjs.org/package/gulp-template)

```
npm install --save-dev gulp-template
```


## Example

src/greeting.html

```erb
<h1>Hello <%= name %></h1>
```

gulpfile.js

```js
var gulp = require('gulp');
var template = require('gulp-template');

gulp.task('default', function () {
	gulp.src('src/greeting.html')
		.pipe(template({name: 'Sindre'}))
		.pipe(gulp.dest('dist/greeting.html'));
});
```

dist/greeting.html

```html
<h1>Hello Sindre</h1>
```


## API

See the [Lodash._template docs](http://lodash.com/docs#template).


### template(data, options)


#### data

Type: `Object`

The data object used to populate the text.


#### options

Type: `Object`

[Lodash._template options](http://lodash.com/docs#template).


## License

MIT © [Sindre Sorhus](http://sindresorhus.com)
