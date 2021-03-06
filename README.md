WDIO Cucumber Framework Adapter
===============================

[![Build Status](https://circleci.com/gh/lgandecki/wdio-cucumber2-framework.svg?style=svg)](https://circleci.com/gh/lgandecki/wdio-cucumber2-framework) [![Code Climate](https://codeclimate.com/github/lgandecki/wdio-cucumber2-framework/badges/gpa.svg)](https://codeclimate.com/github/lgandecki/wdio-cucumber2-framework) [![Test Coverage](https://codeclimate.com/github/lgandecki/wdio-cucumber2-framework/badges/coverage.svg)](https://codeclimate.com/github/lgandecki/wdio-cucumber2-framework/coverage)

***

> A WebdriverIO plugin. Adapter for CucumberJS 2 testing framework.

This is based off the wdio-cucumber-framework, rewrote to work with the second version of CucumberJS.

## Installation

The easiest way is to keep `wdio-cucumber2-framework` as a devDependency in your `package.json`.

```json
{
  "devDependencies": {
    "wdio-cucumber2-framework": "~0.0.1"
  }
}
```

You can simple do it by:

```bash
npm install wdio-cucumber2-framework --save-dev
```

Instructions on how to install `WebdriverIO` can be found [here.](http://webdriver.io/guide/getstarted/install.html)


## Configuration

Following code shows the default wdio test runner configuration...

```js
// wdio.conf.js
module.exports = {
  // ...
  framework: 'cucumber2'
  cucumberOpts: {
    timeout: 10000
  }
  // ...
};
```

## `cucumberOpts` Options

### backtrace
Show full backtrace for errors.

Type: `Boolean`<br>
Default: `false`

### compiler
Require files with the given EXTENSION after requiring MODULE.

Type: `String[]`<br>
Default: `*[]*`<br>
Example: `['js:babel-core/register']`

### failFast
Abort the run on first failure.

Type: `Boolean`<br>
Default: `false`

### name
Only execute the scenarios with name matching the expression (repeatable).

Type: `REGEXP[]`<br>
Default: `[]`

### snippets
Hide step definition snippets for pending steps.

Type: `Boolean`<br>
Default: `true`

### source
Hide source uris.

Type: `Boolean`<br>
Default: `true`

### profile
Specify the profile to use.

Type: `String[]`<br>
Default: `[]`

### require
Require files/dir before executing features. If you apply a path don't use globbing as it is not supported by Cucumber. Instead just reference the directory where you step definitions are located (e.g. `/path/to/definitions` instead of `/path/to/definitions/*`).

Type: `String[]`<br>
Default: `[]`

### snippetSyntax
Specify a custom snippet syntax.

Type: `String`<br>
Default: `undefined`

### strict
Fail if there are any undefined or pending steps

Type: `Boolean`<br>
Default: `false`

### tags
Only execute the features or scenarios with tags matching the expression. Note that untagged
features will still spawn a Selenium session (see issue [webdriverio/webdriverio#1247](https://github.com/webdriverio/webdriverio/issues/1247)).
The recommended way to specify a subset of feature files is to use [suites](http://webdriver.io/guide/testrunner/organizesuite.html#Group-Test-Specs).
Using `['@t1,@t2']` will run scenarios tagged with `@t1` OR `@t2` whilst `['@t1', '@t2']` will run those with `@t1` AND `@t2`.

Type: `String[]`<br>
Default: `[]`

### timeout
Timeout in milliseconds for step definitions.

Type: `Number`<br>
Default: `30000`

### ignoreUndefinedDefinitions
**Please note that this is a wdio-cucumber-framework specifc option and not recognized by cucumber-js itself**
Treat undefined definitions as warnings.

Type: `Boolean`<br>
Default: `false`

### failAmbiguousDefinitions
**Please note that this is a wdio-cucumber2-framework specifc option and not recognized by cucumber-js itself**
Treat ambiguous definitions as errors.

Type: `Boolean`<br>
Default: `false`

## Development

All commands can be found in the package.json. The most important are:

Watch changes:

```sh
$ npm run watch
```

Run tests:

```sh
$ npm test

# run test with coverage report:
$ npm run test:cover
```

Build package:

```sh
$ npm build
```

----

For more information on WebdriverIO see the [homepage](http://webdriver.io).
