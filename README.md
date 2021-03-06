# gulp-livescript
> Distributed via

[![NPM version](https://badge.fury.io/js/gulp-livescript.png)](http://badge.fury.io/js/gulp-livescript)

> Compile LiveScript to JavaScript for Gulp

[![Build Status](https://secure.travis-ci.org/tomchentw/gulp-livescript.png)](http://travis-ci.org/tomchentw/gulp-livescript) [![Code Climate](https://codeclimate.com/github/tomchentw/gulp-livescript.png)](https://codeclimate.com/github/tomchentw/gulp-livescript) [![Dependency Status](https://gemnasium.com/tomchentw/gulp-livescript.png)](https://gemnasium.com/tomchentw/gulp-livescript)

## Information

<table>
<tr> 
<td>Package</td><td>gulp-livescript</td>
</tr>
<tr>
<td>Description</td>
<td>Compile LiveScript to JavaScript for Gulp</td>
</tr>
<tr>
<td>Node Version</td>
<td>>= 0.9</td>
</tr>
<tr>
<td>Gulp Version</td>
<td>>= 3.5.0</td>
</tr>
</table>


## Usage

```javascript
var gulpLiveScript = require('gulp-livescript');

gulp.task('ls', function() {
  gulp.src('./src/*.ls')
    .pipe(gulpLiveScript({bare: true}).on('error', gutil.log))
    .pipe(gulp.dest('./public/'));
});

```

### Error Handling

`gulp-livescript` will emit an error for cases such as invalid LiveScript syntax. If uncaught, the error will crash gulp.

You will need to attach a listener (i.e. .on('error')) for the error event emitted by gulp-livescript. Since .on(...) returns this, you can compact it as inline code (See [Usage](https://github.com/tomchentw/gulp-livescript/blob/master/README.md#Usage)).

### Options

The options object supports the same options as the standard LiveScript compiler.


## Contributing

[![devDependency Status](https://david-dm.org/tomchentw/gulp-livescript/dev-status.png?branch=master)](https://david-dm.org/tomchentw/gulp-livescript#info=devDependencies)

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## Credits

* [`gulp-coffee` by @wearefractal](https://github.com/wearefractal/gulp-coffee)
