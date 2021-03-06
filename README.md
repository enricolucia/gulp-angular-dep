# gulp-angular-dep [![Code Climate](https://codeclimate.com/github/enricolucia/gulp-angular-dep/badges/gpa.svg)](https://codeclimate.com/github/enricolucia/gulp-angular-dep) [![npm version](https://badge.fury.io/js/gulp-angular-dep.svg)](http://badge.fury.io/js/gulp-angular-dep)
> Configurable dynamic install angular Bower dependencies.

# DEPRECATED
Use instead gulp-framework-dep: [npm] or [github]
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
       //exclude files from stream
       exclude: ['arg1','arg2','arg3', .....]
 })
    .pipe(gulp.dest('path/'))
});
```

[github]:https://github.com/enricolucia/gulp-framework-dep
[npm]:https://www.npmjs.com/package/gulp-framework-dep


## Changelog

#####0.0.1
- initial release

#####0.0.4
- updated README.md on npm

#####0.0.5
- updated README.md and index.js typo
