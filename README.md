
# Pa11y HTML Reporter

## This repository is now deprecated.

The reporter has been merged into [pa11y/reporters](https://github.com/pa11y/pa11y/tree/master/lib/reporters).

An HTML reporter for [Pa11y 5.0](https://github.com/pa11y/pa11y).

[![NPM version][shield-npm]][info-npm]
[![Build status][shield-build]][info-build]
[![LGPL-3.0 licensed][shield-license]][info-license]


## Table Of Contents

- [Requirements](#requirements)
- [Usage](#usage)
  - [Command-Line](#command-line)
  - [JavaScript](#javascript)
- [Contributing](#contributing)
- [License](#license)


## Requirements

Pa11y HTML Reporter is compatible with Pa11y 5.0. It will not work with older versions of Pa11y.


## Usage

### Command-Line

Install Pa11y and Pa11y HTML Reporter with [npm](https://www.npmjs.com/) (locally or globally is fine):

```sh
npm install -g pa11y pa11y-reporter-html
```

Run Pa11y using the HTML reporter:

```sh
pa11y --reporter html http://example.com
```

Run Pa11y and save HTML file of report:

```sh
pa11y --reporter html http://example.com > report.html
```

### JavaScript

Assuming you've installed both Pa11y and Pa11y HTML Reporter:

```js
const html = require('pa11y-reporter-html');
const pa11y = require('pa11y');

pa11y('http://example.com').then(async results => {
    // Returns a string with the results formatted as HTML
    const htmlResults = await html.results(results);
    console.log(htmlResults);
});
```


## Contributing

There are many ways to contribute to Pa11y HTML Reporter, we cover these in the [contributing guide](CONTRIBUTING.md) for this repo.

If you're ready to contribute some code, clone this repo locally and commit your code on a new branch.

Please write unit tests for your code, and check that everything works by running the following before opening a <abbr title="pull request">PR</abbr>:

```sh
make ci
```

You can also run verifications and tests individually:

```sh
make verify              # Verify all of the code (ESLint)
make test                # Run all tests
make test-unit           # Run the unit tests
make test-unit-coverage  # Run the unit tests with coverage
```


## License

Pa11y HTML Reporter is licensed under the [Lesser General Public License (LGPL-3.0)][info-license].<br/>
Copyright &copy; 2017, Team Pa11y


[info-license]: LICENSE
[info-npm]: https://www.npmjs.com/package/pa11y
[info-build]: https://travis-ci.org/pa11y/pa11y
[shield-license]: https://img.shields.io/badge/license-LGPL%203.0-blue.svg
[shield-npm]: https://img.shields.io/npm/v/pa11y-reporter-html.svg
[shield-build]: https://img.shields.io/travis/pa11y/pa11y-reporter-html/master.svg
