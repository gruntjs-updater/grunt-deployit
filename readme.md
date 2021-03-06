# grunt-deployit [![Build Status](https://travis-ci.org/quintana-dev/grunt-deployit.svg)](https://travis-ci.org/quintana-dev/grunt-deployit) [![Dependency Status](https://david-dm.org/quintana-dev/grunt-deployit.svg)](https://david-dm.org/quintana-dev/grunt-deployit)

> Deploy your files easily.

## Getting Started
This plugin requires Grunt `~0.4.5`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
$ npm install grunt-deployit --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-deployit');
```

## The "deployit" task

### Overview
In your project's Gruntfile, add a section named `deployit` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  deployit: {
    options: {
      host: 'localhost',
      port: '22',
      username: 'guest'
    },
    files: {
      src: './dist',
      dest: '/home/guest/deploy'
    }
  }
});
```

### Options
Server options.

#### options.host
Type: `String`
Default value: `localhost`

Server host address.

#### options.port
Type: `String`
Default value: `22`

Server port.

#### options.username
Type: `String`
Default value: `guest`

Server user name.

#### options.password
Type: `String` (optional)

Server user password.

**Note:** If password is not provided (by default), prompt will request for your password.

### Files
Deployment settings.

#### files.src
Type: `String`

Local directory to deploy.

**Note:** `Src` option supports [glob patterns](https://github.com/isaacs/node-glob).

#### files.dest
Type: `String`

Remote directory to deploy.

### Usage Examples

#### Options
Using glob pattern.

```js
grunt.initConfig({
  deployit: {
    server: {
      host: 'my.remote.server.com',
      port: '22',
      username: 'guest'
    },
    deploy: {
      src: './dist/{,*/}*.js',
      dest: '/home/guest/deploy'
    }
  }
});
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

## Release History
Date | Version | Description
--- | --- | ---
2015-10-12 | v0.1.0 | Work in progress, not yet officially released.

## License
MIT license

© 2015 [José Luis Quintana](http://quintana.io)
