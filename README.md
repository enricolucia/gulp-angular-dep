# gulp-angular-dep
> Configurable dynamic install angular Bower dependencies.

## Usage

First, install `gulp-angular-dep` as a development dependency:

```shell
npm install --save gulp-angular-dep
```

Then, add it to your `gulpfile.js`:

```javascript
var gulp = require('gulp');
var angularDep = require('gulp-angular-dep');

gulp.task('default', function() {
  return angularDep()
    .pipe(gulp.dest('lib/'))
});
```

This defaults to the directory configured in `./.bowerrc` or to `./bower_components` when no `.bowerrc` could be found.


You can also pass a config Object with all these optional parameters to gulp-angular-dep:

```javascript
var gulp = require('gulp');
var angularDep = require('gulp-angular-dep');

gulp.task('default', function() {
  return angularDep({
      //path to .bowerrc
       cwd: './',
       //bower folders where to pick files
       directory: './bower_components',
       //pick minified version from bower folders
       minified: true,
       //esclude files from stream
       esclude: ['arg1','arg2','arg3', .....]
 })
    .pipe(gulp.dest('path/'))
});
```




## Changelog

#####0.0.1
- initial release
