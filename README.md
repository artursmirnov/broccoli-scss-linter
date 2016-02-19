# broccoli-scss-linter

> Broccoli plugin for validate .scss files.

> This is a fork of [broccoli-scss-lint](https://github.com/a-tarasyuk/broccoli-scss-lint) that applies latest Broccoli changes and mutes logging for better integration.

### Dependencies

1. [Ruby](http://www.ruby-lang.org/en/downloads/) (Ruby 1.9.3+)
2. [scss-lint](https://github.com/causes/scss-lint#installation)

### Installation
```shell
npm install broccoli-scss-linter
```

### Options

#### config
Type: `String`
Default: `''`

Specify a configuration file to use

####bundleExec
Type: `Boolean`
Default: `false`

#### format
Type: `String` | `Array`
Default: `Default`

Output format (xml, config). If value of this option equals xml, option 'reportFile' cannot be empty. Also you can set format as array (['xml', 'default'], ['config', 'default'], ['config', 'default', 'xml']) in order to see errors in console and save result in xml file.

#### reportFile
Type: `String`
Default: `''`

File where will be saved report

#### verbose
Type: `Boolean`
Deafult: `false`

Enable progress output

### Examples
1.
```js
var scssLint = require('broccoli-scss-lint');

// Validate with custom config
files = scssLint(tree, {
  config: '.config.yml'
});

```

2.
```js
var scssLint = require('broccoli-scss-lint');

// Save xml report
files = scssLint(tree, {
  format: 'xml',
  reportFile: 'scss-lint-report.xml'
});
```
