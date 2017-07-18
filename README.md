<p align="center">
  <a href="https://github.com/tunnckoCore/charlike">
    <img height="250" width="250" src="./logo.png">
  </a>
</p>

# charlike-cli [![NPM version](https://img.shields.io/npm/v/charlike-cli.svg?style=flat)](https://www.npmjs.com/package/charlike-cli) [![NPM monthly downloads](https://img.shields.io/npm/dm/charlike-cli.svg?style=flat)](https://npmjs.org/package/charlike-cli) [![npm total downloads][downloads-img]][downloads-url]

> Command line interface for the [charlike][] project scaffolder.

[![code climate][codeclimate-img]][codeclimate-url] 
[![standard code style][standard-img]][standard-url] 
[![linux build status][travis-img]][travis-url] 
[![windows build][appveyor-img]][appveyor-url] 
[![code coverage][codecov-img]][codecov-url] 
[![dependency status][david-img]][david-url]

## Table of Contents
- [Install](#install)
- [Usage](#usage)
- [Related](#related)
- [Contributing](#contributing)
- [Building docs](#building-docs)
- [Running tests](#running-tests)
- [Author](#author)
- [Logo](#logo)
- [License](#license)

## Install
Install with [npm](https://www.npmjs.com/)

```
$ npm install charlike-cli --global
```

or install using [yarn](https://yarnpkg.com)

```
$ yarn global add charlike-cli
```

## Usage
> Just type `charlike --help` to see more. All of flags are optional
and are directly passed to the [charlike][] API.

```
  Usage
    $ charlike <name> <description> [flags]

  Common Flags
    --help            Show this output
    --version         Show version

  Flags
    --owner, -O       Project github owner - username or organization
    --name, -N        Name of the project, same as to pass first param
    --desc, -D        Project description, same as to pass second param
    --repo, -R        Repository pattern like username/projectName
    --engine, -E      Engine to be used, j140 by default
    --locals, -L      Context to pass to template files (support dot notation)
    --templates, -T   Path to templates folder
    --cwd, -C         Folder to be used as current working dir

  Examples
    $ charlike my-awesome-project 'some cool description'
    $ charlike minibase-data 'we are awesome' --owner node-minibase
    $ charlike -D 'abc description here' -N beta-trans -O gulpjs

  Issues: http://github.com/tunnckoCore/charlike
```

**Notes:**

- The `name` and `description` positional params are required if not flags instead are given
- The `engine` is that you want to use in the template files, but is also required to install some [jstransformer][] for it. For example if you want to use [handlebars][] in the templates, install [jstransformer-handlebars][]
- The `locals` support dot notation, so `--locals.foo.bar.baz 123` will set `foo.bar.baz` in your templates to have `123` value.
- If `owner` is not passed, it tries to use [git-user-name][] from current working directory

## Related
- [always-done](https://www.npmjs.com/package/always-done): Handle completion and errors with elegance! Support for streams, callbacks, promises, child processes, async/await and sync functions. A drop-in replacement… [more](https://github.com/hybridables/always-done#readme) | [homepage](https://github.com/hybridables/always-done#readme "Handle completion and errors with elegance! Support for streams, callbacks, promises, child processes, async/await and sync functions. A drop-in replacement for [async-done][] - pass 100% of its tests plus more")
- [minibase](https://www.npmjs.com/package/minibase): Minimalist alternative for Base. Build complex APIs with small units called plugins. Works well with most of the already existing… [more](https://github.com/node-minibase/minibase#readme) | [homepage](https://github.com/node-minibase/minibase#readme "Minimalist alternative for Base. Build complex APIs with small units called plugins. Works well with most of the already existing [base][] plugins.")
- [try-catch-core](https://www.npmjs.com/package/try-catch-core): Low-level package to handle completion and errors of sync or asynchronous functions, using [once][] and [dezalgo][] libs. Useful for and… [more](https://github.com/hybridables/try-catch-core#readme) | [homepage](https://github.com/hybridables/try-catch-core#readme "Low-level package to handle completion and errors of sync or asynchronous functions, using [once][] and [dezalgo][] libs. Useful for and used in higher-level libs such as [always-done][] to handle completion of anything.")

## Contributing
Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](https://github.com/tunnckoCore/charlike-cli/issues/new).  
Please read the [contributing guidelines](CONTRIBUTING.md) for advice on opening issues, pull requests, and coding standards.  
If you need some help and can spent some cash, feel free to [contact me at CodeMentor.io](https://www.codementor.io/tunnckocore?utm_source=github&utm_medium=button&utm_term=tunnckocore&utm_campaign=github) too.

**In short:** If you want to contribute to that project, please follow these things

1. Please DO NOT edit [README.md](README.md), [CHANGELOG.md](CHANGELOG.md) and [.verb.md](.verb.md) files. See ["Building docs"](#building-docs) section.
2. Ensure anything is okey by installing the dependencies and run the tests. See ["Running tests"](#running-tests) section.
3. Always use `npm run commit` to commit changes instead of `git commit`, because it is interactive and user-friendly. It uses [commitizen][] behind the scenes, which follows Conventional Changelog idealogy.
4. Do NOT bump the version in package.json. For that we use `npm run release`, which is [standard-version][] and follows Conventional Changelog idealogy.

Thanks a lot! :)

## Building docs
Documentation and that readme is generated using [verb-generate-readme][], which is a [verb][] generator, so you need to install both of them and then run `verb` command like that

```
$ npm install verbose/verb#dev verb-generate-readme --global && verb
```

_Please don't edit the README directly. Any changes to the readme must be made in [.verb.md](.verb.md)._

## Running tests
Clone repository and run the following in that cloned directory

```
$ npm install && npm test
```

## Author
**Charlike Mike Reagent**

+ [github/tunnckoCore](https://github.com/tunnckoCore)
+ [twitter/tunnckoCore](https://twitter.com/tunnckoCore)
+ [codementor/tunnckoCore](https://codementor.io/tunnckoCore)

## Logo
The logo is [Monster Icon](http://thenounproject.com/term/moster/63928/) by [Christian Mohr](http://www.thenounproject.com/mom-digital). Released under the [CC BY 3.0](http://creativecommons.org/licenses/by/3.0/us/) license.

## License
Copyright © 2016-2017, [Charlike Mike Reagent](http://i.am.charlike.online). MIT

***

_This file was generated by [verb-generate-readme](https://github.com/verbose/verb-generate-readme), v0.6.0, on July 18, 2017._  
_Project scaffolded using [charlike][] cli._

[always-done]: https://github.com/hybridables/always-done
[async-done]: https://github.com/gulpjs/async-done
[base]: https://github.com/node-base/base
[charlike]: https://github.com/tunnckoCore/charlike
[commitizen]: https://github.com/commitizen/cz-cli
[dezalgo]: https://github.com/npm/dezalgo
[git-user-name]: https://github.com/jonschlinkert/git-user-name
[handlebars]: http://www.handlebarsjs.com/
[jstransformer]: https://github.com/jstransformers/jstransformer
[once]: https://github.com/isaacs/once
[standard-version]: https://github.com/conventional-changelog/standard-version
[verb-generate-readme]: https://github.com/verbose/verb-generate-readme
[verb]: https://github.com/verbose/verb

[downloads-url]: https://www.npmjs.com/package/charlike-cli
[downloads-img]: https://img.shields.io/npm/dt/charlike-cli.svg

[codeclimate-url]: https://codeclimate.com/github/tunnckoCore/charlike-cli
[codeclimate-img]: https://img.shields.io/codeclimate/github/tunnckoCore/charlike-cli.svg

[travis-url]: https://travis-ci.org/tunnckoCore/charlike-cli
[travis-img]: https://img.shields.io/travis/tunnckoCore/charlike-cli/master.svg?label=linux

[appveyor-url]: https://ci.appveyor.com/project/tunnckoCore/charlike-cli
[appveyor-img]: https://img.shields.io/appveyor/ci/tunnckoCore/charlike-cli/master.svg?label=windows

[codecov-url]: https://codecov.io/gh/tunnckoCore/charlike-cli
[codecov-img]: https://img.shields.io/codecov/c/github/tunnckoCore/charlike-cli/master.svg?label=codecov

[david-url]: https://david-dm.org/tunnckoCore/charlike-cli
[david-img]: https://img.shields.io/david/tunnckoCore/charlike-cli.svg

[standard-url]: https://github.com/feross/standard
[standard-img]: https://img.shields.io/badge/code%20style-standard-brightgreen.svg

[jstransformer-handlebars]: https://github.com/jstransformers/jstransformer-handlebars