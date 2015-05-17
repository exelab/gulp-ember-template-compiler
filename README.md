# gulp-ember-template-compiler

Gulp Plugin that compiles templates for Ember 1.12+
An adapted version of this [plugin](https://github.com/Geodesigner/gulp-ember-template-compiler).

### Installation

```bash
npm install n-fuse/gulp-ember-template-compiler#1.13.0-beta.1
```

where 1.13.0-beta.1 is the Ember version to be used.

### Usage

```JavaScript
var rename = require('gulp-ember-template-compiler');

gulp.task('templates', function() {
  return gulp.src('app/**/*.hbs')
    .pipe(compiler())
    .pipe(rename(function(path) {
      path.extname = '.hbs.js'
    }))
    .pipe(gulp.dest('app'));
});
```

#### Import a Compiled Template

```JavaScript
import tmp from './my-tmpl.hbs'
```

### License

[MIT license](LICENSE.txt)
