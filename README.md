# cult [![NPM version](https://badge.fury.io/js/cult.svg)](http://badge.fury.io/js/cult)

> cult monitors gulpfile changes and reloads gulp

_Works on OS X, Linux and Windows._

```bash
$ npm install -g cult
```

```bash
$ cult <task> <othertask> # will call gulp <task> <othertask>
```

### For `gulpfile` split across multiple files

If your `gulpfile` is split across multiple files, use [node-touch](https://github.com/isaacs/node-touch) and add something similar to this to your `watch` task to reload on any gulp file changes:

```javascript
gulp.watch(['gulp/**'], function() { touch('gulpfile.coffee') }
```

## History

* 2.x.x Since gulp 3.7, there's no need anymore to add --require, cult now will symply monitor gulpfile (until this feature is added to gulp :)
* 1.x.x Monitors gulpfile changes and adds `--require` depending on gulpfile extension

## License

MIT
