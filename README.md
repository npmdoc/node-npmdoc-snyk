# npmdoc-snyk

#### basic api documentation for  [snyk (v1.29.0)](https://github.com/Snyk/snyk#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-snyk.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-snyk) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-snyk.svg)](https://travis-ci.org/npmdoc/node-npmdoc-snyk)

#### snyk library and cli utility

[![NPM](https://nodei.co/npm/snyk.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/snyk)

- [https://npmdoc.github.io/node-npmdoc-snyk/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-snyk/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-snyk/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-snyk/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-snyk/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-snyk/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Remy Sharp"
    },
    "bin": {
        "snyk": "./cli/index.js"
    },
    "bugs": {
        "url": "https://github.com/Snyk/snyk/issues"
    },
    "dependencies": {
        "abbrev": "^1.0.7",
        "ansi-escapes": "^1.3.0",
        "chalk": "^1.1.1",
        "configstore": "^1.2.0",
        "debug": "^2.2.0",
        "es6-promise": "^3.0.2",
        "hasbin": "^1.2.3",
        "inquirer": "1.0.3",
        "open": "^0.0.5",
        "os-name": "^1.0.3",
        "request": "^2.74.0",
        "semver": "^5.1.0",
        "snyk-config": "1.0.1",
        "snyk-module": "1.8.1",
        "snyk-policy": "1.7.1",
        "snyk-recursive-readdir": "^2.0.0",
        "snyk-resolve": "1.0.0",
        "snyk-resolve-deps": "1.7.0",
        "snyk-tree": "^1.0.0",
        "snyk-try-require": "^1.2.0",
        "tempfile": "^1.1.1",
        "then-fs": "^2.0.0",
        "undefsafe": "0.0.3",
        "update-notifier": "^0.5.0",
        "url": "^0.11.0",
        "uuid": "^3.0.1"
    },
    "description": "snyk library and cli utility",
    "devDependencies": {
        "babel-cli": "^6.7.7",
        "babel-polyfill": "^6.7.4",
        "babel-preset-es2015": "^6.6.0",
        "babel-preset-stage-3": "^6.5.0",
        "jscs": "^2.0.0",
        "lodash": "^3.10.1",
        "lodash-cli": "^3.10.1",
        "proxyquire": "^1.7.4",
        "restify": "^4.1.1",
        "semantic-release": "^4.3.5",
        "sinon": "^1.17.2",
        "tap": "^5.7.1",
        "tap-only": "0.0.5",
        "tape": "^4.0.0"
    },
    "directories": {
        "test": "test"
    },
    "dist": {
        "shasum": "20be4eaddc9641ca004fb24368dc33d6f82d17dc",
        "tarball": "https://registry.npmjs.org/snyk/-/snyk-1.29.0.tgz"
    },
    "gitHead": "d984cb845b9439109e0d9769cd70b97176b412b8",
    "homepage": "https://github.com/Snyk/snyk#readme",
    "keywords": [
        "security",
        "snyk"
    ],
    "license": "Apache-2.0",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "snyk-admin"
        }
    ],
    "name": "snyk",
    "nyc": {
        "exclude": [
            "dist",
            "test",
            "test{,-*}.js",
            "**/*.test.js",
            "**/__tests__/**"
        ]
    },
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/Snyk/snyk.git"
    },
    "scripts": {
        "build": "mkdir dist; lodash -p -o ./dist/lodash-min.js include=cloneDeep,extend,defaults,forEach,flatten,flattenDeep,merge,unique",
        "check-tests": "! grep 'test\\.only' test/*.test.js -n",
        "coverage": "tap --cov --coverage-report=lcov test/*.test.js",
        "lint": "jscs 'find ./cli -name '*.js'' -v && jscs 'find ./lib -name '*.js'' -v",
        "semantic-release": "semantic-release pre && npm publish && semantic-release post",
        "snyk-auth": "node cli auth $SNYK_API_KEY",
        "snyk-auth-windows": "node cli auth %SNYK_API_KEY%",
        "tap": "COVERALLS_REPO_TOKEN=0 tap --timeout=180 --cov --coverage-report=text-summary test/*.test.js",
        "tap:babel": "COVERALLS_REPO_TOKEN=0 tap --nyc-arg=--require --nyc-arg=babel-polyfill --timeout=180 --cov --coverage-report=text-summary test/*.test.js",
        "test": "npm run test-common && npm run tap",
        "test-common": "npm run check-tests && npm run lint && node cli/index.js test",
        "test:babel": "npm run test-common && babel test/*.js -d . && npm run tap:babel",
        "travis-coverage": "node_modules/tap/node_modules/.bin/nyc report --reporter=text-lcov | node_modules/tap/node_modules/.bin/coveralls",
        "windows-build": "mkdir dist & lodash -p -o ./dist/lodash-min.js include=cloneDeep,extend,defaults,forEach,flatten,flattenDeep,merge,unique",
        "windows-tests": "tap -R spec test/*.test.js --timeout=120"
    },
    "snyk": true,
    "version": "1.29.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
