# grunt-rem-plus

> px change to rem

## Getting Started
This plugin requires Grunt `~0.4.5`

Dependencies rem-core[rem-core](https://www.npmjs.com/package/rem-core).
If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-rem-plus --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-rem-plus');
```

## The "rem_plus" task

### Overview
In your project's Gruntfile, add a section named `rem_plus` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  rem_plus: {
    options: {
      dist: {
          src: ['./demo.css'],
          dest: './dist/aio.css'
      }
      // Task-specific options go here.
    },
    your_target: {
      // Target-specific file lists and/or options go here.
    },
  },
});
```

### Options

#### options.separator
Type: `String`
Default value: `',  '`

A string value that is used to do something with whatever.

#### options.punctuation
Type: `String`
Default value: `'.'`

A string value that is used to do something else with whatever else.

### Usage Examples

#### Default Options
In this example, the default options are used to do something with whatever. So if the `testing` file has the content `Testing` and the `123` file had the content `1 2 3`, the generated result would be `Testing, 1 2 3.`

```js
grunt.initConfig({
  rem_plus: {
    options: {},
    files: {
      'dest/default_options': ['src/testing', 'src/123'],
    },
  },
});
```

#### Custom Options
In this example, custom options are used to do something else with whatever else. So if the `testing` file has the content `Testing` and the `123` file had the content `1 2 3`, the generated result in this case would be `Testing: 1 2 3 !!!`

```js
grunt.initConfig({
  rem_plus: {
    options: {
      separator: ': ',
      punctuation: ' !!!',
      rem: 18,
      min: 3,
      dpr: 2,
      fontSize2Rem: false, // default: true 
      exclude: [
        'background', 'background-size'
      ]
    },
    files: {
      'dest/default_options': ['src/testing', 'src/123'],
    },
  },
});
```

### Web bowser runtime js
taobao [flexible.js](https://github.com/amfe/lib-flexible)

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

## Release History
_(Nothing yet)_
