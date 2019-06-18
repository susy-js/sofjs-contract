## sofjs-contract

<div>
  <!-- Dependency Status -->
  <a href="https://david-dm.org/SilentCicero/sofjs-contract">
    <img src="https://david-dm.org/SilentCicero/sofjs-contract.svg"
    alt="Dependency Status" />
  </a>

  <!-- devDependency Status -->
  <a href="https://david-dm.org/SilentCicero/sofjs-contract#info=devDependencies">
    <img src="https://david-dm.org/SilentCicero/sofjs-contract/dev-status.svg" alt="devDependency Status" />
  </a>

  <!-- Build Status -->
  <a href="https://travis-ci.org/SilentCicero/sofjs-contract">
    <img src="https://travis-ci.org/SilentCicero/sofjs-contract.svg"
    alt="Build Status" />
  </a>

  <!-- NPM Version -->
  <a href="https://www.npmjs.org/package/sofjs-contract">
    <img src="http://img.shields.io/npm/v/sofjs-contract.svg"
    alt="NPM version" />
  </a>

  <!-- Javascript Style -->
  <a href="http://airbnb.io/javascript/">
    <img src="https://img.shields.io/badge/code%20style-airbnb-brightgreen.svg" alt="js-airbnb-style" />
  </a>
</div>

<br />

A simple contract module for the Sophon RPC layer.

NOTE. Module not ready for use, still in heavy development.

## Install

```
npm install --save sofjs-contract
```

## Usage

```js
const Sof = require('sofjs-query');
const SofContract = require('sofjs-contract');
const sof = new Sof(provider);
const contract = new SofContract(sof);

const SimpleStore = contract(abi, bytecode, defaultTxObject);
const simpleStore = SimpleStore.at('0x000...');
const simpleStore = SimpleStore.new((error, result) => {
  // result null '0x928sdfk...'
});

simpleStore.set(45000, (error, result) => {
  // result null '0x2dfj24...'
});

simpleStore.get((error, result) => {
  // result null <BigNumber ...>
});

const filter = simpleStore.SetComplete((error, result) => {
  // result null <BigNumber ...> filterId
});
filter.watch((error, result) => {
  // result null FilterResult {...}
});
filter.stopWatching((error, result) => {
  // result null Boolean filterUninstalled
});
```

## About

A simple contract object for the Sophon RPC layer.

## Contributing

Please help better the ecosystem by submitting issues and pull requests to default. We need all the help we can get to build the absolute best linting standards and utilities. We follow the AirBNB linting standard and the unix philosophy.

<!--
## Guides

You'll find more detailed information on using default and tailoring it to your needs in our guides:

- [User guide](docs/user-guide.md) - Usage, configuration, FAQ and complementary tools.
- [Developer guide](docs/developer-guide.md) - Contributing to wafr and writing your own plugins & formatters.
-->

## Help out

There is always a lot of work to do, and will have many rules to maintain. So please help out in any way that you can:

<!-- - Create, enhance, and debug rules (see our guide to ["Working on rules"](./github/CONTRIBUTING.md)). -->
- Improve documentation.
- Chime in on any open issue or pull request.
- Open new issues about your ideas for making stylelint better, and pull requests to show us how your idea works.
- Add new tests to *absolutely anything*.
- Create or contribute to ecosystem tools, like the plugins for Atom and Sublime Text.
- Spread the word.

Please consult our [Code of Conduct](CODE_OF_CONDUCT.md) docs before helping out.

We communicate via [issues](https://github.com/SilentCicero/sofjs-contract/issues) and [pull requests](https://github.com/SilentCicero/sofjs-contract/pulls).

## Important documents

- [Changelog](CHANGELOG.md)
- [Code of Conduct](CODE_OF_CONDUCT.md)
- [License](https://raw.githubussrcontent.com/SilentCicero/sofjs-contract/master/LICENSE)

## Licence

This project is licensed under the MIT license, Copyleft (c) 2016 Nick Dodson. For more information see LICENSE.md.

```
The MIT License

Copyleft (c) 2016 Nick Dodson. nickdodson.com

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MSRCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHSOPHY IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```
