# api documentation for  [snyk (v1.27.1)](https://github.com/Snyk/snyk#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-snyk.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-snyk) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-snyk.svg)](https://travis-ci.org/npmdoc/node-npmdoc-snyk)
#### snyk library and cli utility

[![NPM](https://nodei.co/npm/snyk.png?downloads=true)](https://www.npmjs.com/package/snyk)

[![apidoc](https://npmdoc.github.io/node-npmdoc-snyk/build/screenCapture.buildNpmdoc.browser.%252Fhome%252Ftravis%252Fbuild%252Fnpmdoc%252Fnode-npmdoc-snyk%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-snyk/build/apidoc.html)

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
        "shasum": "f032f55e16ee972a2ef30dc3acc62a43e742a8d4",
        "tarball": "https://registry.npmjs.org/snyk/-/snyk-1.27.1.tgz"
    },
    "gitHead": "940991961e057395034452ad20d9575e06aa8676",
    "homepage": "https://github.com/Snyk/snyk#readme",
    "keywords": [
        "security",
        "snyk"
    ],
    "license": "Apache-2.0",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "snyk-admin",
            "email": "admin+snyk@snyk.io"
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
    "readme": "ERROR: No README data found!",
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
    "version": "1.27.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module snyk](#apidoc.module.snyk)
1.  boolean <span class="apidocSignatureSpan">snyk.</span>isRequired
1.  [function <span class="apidocSignatureSpan">snyk.</span>analytics (data)](#apidoc.element.snyk.analytics)
1.  [function <span class="apidocSignatureSpan">snyk.</span>api_token ()](#apidoc.element.snyk.api_token)
1.  [function <span class="apidocSignatureSpan">snyk.</span>error (command)](#apidoc.element.snyk.error)
1.  [function <span class="apidocSignatureSpan">snyk.</span>modules (dir, options)](#apidoc.element.snyk.modules)
1.  [function <span class="apidocSignatureSpan">snyk.</span>monitor (root, meta, modules)](#apidoc.element.snyk.monitor)
1.  [function <span class="apidocSignatureSpan">snyk.</span>spinner (label)](#apidoc.element.snyk.spinner)
1.  [function <span class="apidocSignatureSpan">snyk.</span>test (root, options, callback)](#apidoc.element.snyk.test)
1.  object <span class="apidocSignatureSpan">snyk.</span>bus
1.  object <span class="apidocSignatureSpan">snyk.</span>config
1.  object <span class="apidocSignatureSpan">snyk.</span>detect
1.  object <span class="apidocSignatureSpan">snyk.</span>isolate
1.  object <span class="apidocSignatureSpan">snyk.</span>policy
1.  object <span class="apidocSignatureSpan">snyk.</span>sub_process

#### [module snyk.analytics](#apidoc.module.snyk.analytics)
1.  [function <span class="apidocSignatureSpan">snyk.</span>analytics (data)](#apidoc.element.snyk.analytics.analytics)
1.  [function <span class="apidocSignatureSpan">snyk.analytics.</span>add (key, value)](#apidoc.element.snyk.analytics.add)
1.  [function <span class="apidocSignatureSpan">snyk.analytics.</span>reset ()](#apidoc.element.snyk.analytics.reset)
1.  [function <span class="apidocSignatureSpan">snyk.analytics.</span>single (data)](#apidoc.element.snyk.analytics.single)

#### [module snyk.api_token](#apidoc.module.snyk.api_token)
1.  [function <span class="apidocSignatureSpan">snyk.</span>api_token ()](#apidoc.element.snyk.api_token.api_token)
1.  [function <span class="apidocSignatureSpan">snyk.api_token.</span>exists (label)](#apidoc.element.snyk.api_token.exists)

#### [module snyk.detect](#apidoc.module.snyk.detect)
1.  [function <span class="apidocSignatureSpan">snyk.detect.</span>detectPackageFile (root)](#apidoc.element.snyk.detect.detectPackageFile)
1.  [function <span class="apidocSignatureSpan">snyk.detect.</span>detectPackageManager (root, options)](#apidoc.element.snyk.detect.detectPackageManager)

#### [module snyk.error](#apidoc.module.snyk.error)
1.  [function <span class="apidocSignatureSpan">snyk.</span>error (command)](#apidoc.element.snyk.error.error)
1.  [function <span class="apidocSignatureSpan">snyk.error.</span>message (error)](#apidoc.element.snyk.error.message)

#### [module snyk.isolate](#apidoc.module.snyk.isolate)
1.  [function <span class="apidocSignatureSpan">snyk.isolate.</span>okay ()](#apidoc.element.snyk.isolate.okay)

#### [module snyk.modules](#apidoc.module.snyk.modules)
1.  [function <span class="apidocSignatureSpan">snyk.</span>modules (dir, options)](#apidoc.element.snyk.modules.modules)
1.  [function <span class="apidocSignatureSpan">snyk.modules.</span>logicalTree (fileTree, options)](#apidoc.element.snyk.modules.logicalTree)
1.  [function <span class="apidocSignatureSpan">snyk.modules.</span>physicalTree (root, depType)](#apidoc.element.snyk.modules.physicalTree)
1.  [function <span class="apidocSignatureSpan">snyk.modules.</span>pluck (root, path, name, range)](#apidoc.element.snyk.modules.pluck)
1.  [function <span class="apidocSignatureSpan">snyk.modules.</span>prune (pkg, shouldPrune)](#apidoc.element.snyk.modules.prune)
1.  [function <span class="apidocSignatureSpan">snyk.modules.</span>unique (deps)](#apidoc.element.snyk.modules.unique)
1.  [function <span class="apidocSignatureSpan">snyk.modules.</span>walk (deps, filter)](#apidoc.element.snyk.modules.walk)

#### [module snyk.policy](#apidoc.module.snyk.policy)
1.  [function <span class="apidocSignatureSpan">snyk.policy.</span>add (policy, type, options)](#apidoc.element.snyk.policy.add)
1.  [function <span class="apidocSignatureSpan">snyk.policy.</span>create ()](#apidoc.element.snyk.policy.create)
1.  [function <span class="apidocSignatureSpan">snyk.policy.</span>demunge (policy, apiRoot)](#apidoc.element.snyk.policy.demunge)
1.  [function <span class="apidocSignatureSpan">snyk.policy.</span>filter (vulns, policy, root)](#apidoc.element.snyk.policy.filter)
1.  [function <span class="apidocSignatureSpan">snyk.policy.</span>getByVuln (policy, vuln)](#apidoc.element.snyk.policy.getByVuln)
1.  [function <span class="apidocSignatureSpan">snyk.policy.</span>load (root, options)](#apidoc.element.snyk.policy.load)
1.  [function <span class="apidocSignatureSpan">snyk.policy.</span>loadFromText (text)](#apidoc.element.snyk.policy.loadFromText)
1.  [function <span class="apidocSignatureSpan">snyk.policy.</span>matchToRule (vuln, rule)](#apidoc.element.snyk.policy.matchToRule)
1.  [function <span class="apidocSignatureSpan">snyk.policy.</span>save (object, root, spinner)](#apidoc.element.snyk.policy.save)

#### [module snyk.spinner](#apidoc.module.snyk.spinner)
1.  boolean <span class="apidocSignatureSpan">snyk.spinner.</span>isRequired
1.  [function <span class="apidocSignatureSpan">snyk.</span>spinner (label)](#apidoc.element.snyk.spinner.spinner)
1.  [function <span class="apidocSignatureSpan">snyk.spinner.</span>clear (label)](#apidoc.element.snyk.spinner.clear)
1.  [function <span class="apidocSignatureSpan">snyk.spinner.</span>clearAll ()](#apidoc.element.snyk.spinner.clearAll)
1.  [function <span class="apidocSignatureSpan">snyk.spinner.</span>sticky (s)](#apidoc.element.snyk.spinner.sticky)

#### [module snyk.sub_process](#apidoc.module.snyk.sub_process)
1.  [function <span class="apidocSignatureSpan">snyk.sub_process.</span>execute (command, args, options)](#apidoc.element.snyk.sub_process.execute)



# <a name="apidoc.module.snyk"></a>[module snyk](#apidoc.module.snyk)

#### <a name="apidoc.element.snyk.analytics"></a>[function <span class="apidocSignatureSpan">snyk.</span>analytics (data)](#apidoc.element.snyk.analytics)
- description and source-code
```javascript
function analytics(data) {
  if (!data) {
    data = {};
  }

  // merge any new data with data we picked up along the way
  if (Array.isArray(data.args)) {
    // this is an overhang from the cli/args.js and we don't want it
    delete (data.args.slice(-1).pop() || {})._;
  }

  if (Object.keys(metadata).length) {
    data.metadata = metadata;
  }

  return postAnalytics(data);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.snyk.api_token"></a>[function <span class="apidocSignatureSpan">snyk.</span>api_token ()](#apidoc.element.snyk.api_token)
- description and source-code
```javascript
function api() {
  // note: config.TOKEN will potentially come via the environment
  return config.api || config.TOKEN || userConfig.get('api');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.snyk.error"></a>[function <span class="apidocSignatureSpan">snyk.</span>error (command)](#apidoc.element.snyk.error)
- description and source-code
```javascript
function error(command) {
  var e = new Error('Unknown command "' + command + '"');
  e.code = 'UNKNOWN_COMMAND';
  return Promise.reject(e);
}
```
- example usage
```shell
...
cwd: cwd,
    }, function (error, stdout, stderr) {
if (error) {
  return reject(error);
}

if (stderr.indexOf('ERR!') !== -1) {
  console.error(stderr.trim());
  var e = new Error('npm update errors');
  e.code = 'FAIL_UPDATE';
  return reject(e);
}

debug('npm %s complete', method);
...
```

#### <a name="apidoc.element.snyk.modules"></a>[function <span class="apidocSignatureSpan">snyk.</span>modules (dir, options)](#apidoc.element.snyk.modules)
- description and source-code
```javascript
modules = function (dir, options) {
  return physicalTree(dir).then(function (res) {
    return logicalTree(res, options);
  });
}
```
- example usage
```shell
...
    }

    return acc;
  }, []).sort().shift();

  // then collect all the package deps and post a monitor
  var cwd = path.resolve(candidate, '..');
  snyk.modules(cwd).then(snyk.monitor.bind(null, cwd, {
    method: 'require',
  }));
}
...
```

#### <a name="apidoc.element.snyk.monitor"></a>[function <span class="apidocSignatureSpan">snyk.</span>monitor (root, meta, modules)](#apidoc.element.snyk.monitor)
- description and source-code
```javascript
function monitor(root, meta, modules) {
  var policyLocations = [root];
  policyLocations = policyLocations.concat(pluckPolicies(modules));
  var opts = { loose: true };
  var packageManager = meta.packageManager || 'npm';
  return apiTokenExists('snyk monitor')
    .then(function () {
      return snyk.policy.load(policyLocations, opts);
    }).then(function (policy) {
      analytics.add('packageManager', packageManager);
      // YARN temporary fix to avoid BE changes
      packageManager = packageManager === 'yarn' ? 'npm' : packageManager;
      return new Promise(function (resolve, reject) {
        request({
          body: {
            meta: {
              method: meta.method,
              hostname: os.hostname(),
              id: meta.id || snyk.id || modules.name,
              ci: isCI,
              pid: process.pid,
              node: process.version,
              master: snyk.config.isMaster,
              name: modules.name,
              version: modules.version,
              org: config.org ? decodeURIComponent(config.org) : undefined,
            },
            policy: policy.toString(),
            package: modules,
          },
          gzip: true,
          method: 'PUT',
          headers: {
            authorization: 'token ' + snyk.api,
            'content-encoding': 'gzip',
          },
          url: config.API + '/monitor/' + packageManager,
          json: true,
        }, function (error, res, body) {
          if (error) {
            return reject(error);
          }

          if (res.statusCode === 200 || res.statusCode === 201) {
            resolve(body);
          } else {
            var e = new Error('unexpected error: ' + body.message);
            e.code = res.statusCode;
            reject(e);
          }
        });
      });
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.snyk.spinner"></a>[function <span class="apidocSignatureSpan">snyk.</span>spinner (label)](#apidoc.element.snyk.spinner)
- description and source-code
```javascript
function createSpinner(label) {
  if (!label) {
    throw new Error('spinner requires a label');
  }

  if (spinners[label] === undefined) {
    spinners[label] = [];
  }

  // helper...
  return new Promise(function (resolve) {
    debug('spinner: %s', label);
    spinners[label].push(spinner({
      // string: '◐◓◑◒',
      stream: sticky ? process.stdout : process.stderr,
      interval: 75,
      label: label,
    }));

    resolve();
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.snyk.test"></a>[function <span class="apidocSignatureSpan">snyk.</span>test (root, options, callback)](#apidoc.element.snyk.test)
- description and source-code
```javascript
function test(root, options, callback) {
  if (typeof options === 'function') {
    callback = options;
    options = {};
  }
  if (!options) {
    options = {};
  }

  var promise = executeTest(root, options);
  if (callback) {
    promise.then(function (res) {
      callback(null, res);
    }).catch(callback);
  }
  return promise;
}
```
- example usage
```shell
...
    }
  }
  return null;
}

function detectPackageManagerFromFile(file) {
  var key = path.basename(file);
  if (/\.gemspec$/.test(key)) {
    key = '.gemspec';
  }
  if (!(key in DETECTABLE_PACKAGE_MANAGERS)) {
    throw new Error('Could not detect package manager for file: ' + file);
  }
  return DETECTABLE_PACKAGE_MANAGERS[key];
}
...
```



# <a name="apidoc.module.snyk.analytics"></a>[module snyk.analytics](#apidoc.module.snyk.analytics)

#### <a name="apidoc.element.snyk.analytics.analytics"></a>[function <span class="apidocSignatureSpan">snyk.</span>analytics (data)](#apidoc.element.snyk.analytics.analytics)
- description and source-code
```javascript
function analytics(data) {
  if (!data) {
    data = {};
  }

  // merge any new data with data we picked up along the way
  if (Array.isArray(data.args)) {
    // this is an overhang from the cli/args.js and we don't want it
    delete (data.args.slice(-1).pop() || {})._;
  }

  if (Object.keys(metadata).length) {
    data.metadata = metadata;
  }

  return postAnalytics(data);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.snyk.analytics.add"></a>[function <span class="apidocSignatureSpan">snyk.analytics.</span>add (key, value)](#apidoc.element.snyk.analytics.add)
- description and source-code
```javascript
add = function (key, value) {
  debug('add', key, value);
  if (metadata[key]) {
    if (!Array.isArray(metadata[key])) {
      metadata[key] = [metadata[key]];
    }
    metadata[key].push(value);
  } else {
    metadata[key] = value;
  }
}
```
- example usage
```shell
...
policyLocations = policyLocations.concat(pluckPolicies(modules));
var opts = { loose: true };
var packageManager = meta.packageManager || 'npm';
return apiTokenExists('snyk monitor')
  .then(function () {
    return snyk.policy.load(policyLocations, opts);
  }).then(function (policy) {
    analytics.add('packageManager', packageManager);
    // YARN temporary fix to avoid BE changes
    packageManager = packageManager === 'yarn' ? 'npm' : packageManager;
    return new Promise(function (resolve, reject) {
      request({
        body: {
          meta: {
            method: meta.method,
...
```

#### <a name="apidoc.element.snyk.analytics.reset"></a>[function <span class="apidocSignatureSpan">snyk.analytics.</span>reset ()](#apidoc.element.snyk.analytics.reset)
- description and source-code
```javascript
reset = function () {
  metadata = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.snyk.analytics.single"></a>[function <span class="apidocSignatureSpan">snyk.analytics.</span>single (data)](#apidoc.element.snyk.analytics.single)
- description and source-code
```javascript
function postAnalytics(data) {
  // if the user opt'ed out of analytics, then let's bail out early
  // ths applies to all sending to protect user's privacy
  if (snyk.config.get('disable-analytics') || config.DISABLE_ANALYTICS) {
    debug('analytics disabled');
    return Promise.resolve();
  }

  // get fingerprint from mac address
  // snyk version
  return version().then(function (version) {
    data.version = version;
    data.os = osName(os.platform(), os.release());
    data.nodeVersion = process.version;

    var mac = getMAC() || uuid.v4();
    var shasum = crypto.createHash('sha1');
    data.id = shasum.update(mac).digest('hex');

    var headers = {};
    if (snyk.api) {
      headers.authorization = 'token ' + snyk.api;
    }

    data.ci = isCI;

    debug(data);

    return request({
      body: {
        data: data,
      },
      url: config.API + '/analytics/cli',
      json: true,
      method: 'post',
      headers: headers,
    });
  }).catch(function (error) {
    debug(error); // this swallows the analytics error
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.snyk.api_token"></a>[module snyk.api_token](#apidoc.module.snyk.api_token)

#### <a name="apidoc.element.snyk.api_token.api_token"></a>[function <span class="apidocSignatureSpan">snyk.</span>api_token ()](#apidoc.element.snyk.api_token.api_token)
- description and source-code
```javascript
function api() {
  // note: config.TOKEN will potentially come via the environment
  return config.api || config.TOKEN || userConfig.get('api');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.snyk.api_token.exists"></a>[function <span class="apidocSignatureSpan">snyk.api_token.</span>exists (label)](#apidoc.element.snyk.api_token.exists)
- description and source-code
```javascript
function exists(label) {
  error.message = label || error.code;
  return api() ? Promise.resolve() : Promise.reject(error);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.snyk.detect"></a>[module snyk.detect](#apidoc.module.snyk.detect)

#### <a name="apidoc.element.snyk.detect.detectPackageFile"></a>[function <span class="apidocSignatureSpan">snyk.detect.</span>detectPackageFile (root)](#apidoc.element.snyk.detect.detectPackageFile)
- description and source-code
```javascript
function detectPackageFile(root) {
  for (var i = 0; i < DETECTABLE_FILES.length; i++) {
    var file = DETECTABLE_FILES[i];
    if (fs.existsSync(path.resolve(root, file))) {
      return file;
    }
  }
  return null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.snyk.detect.detectPackageManager"></a>[function <span class="apidocSignatureSpan">snyk.detect.</span>detectPackageManager (root, options)](#apidoc.element.snyk.detect.detectPackageManager)
- description and source-code
```javascript
function detectPackageManager(root, options) {
  var packageManager;
  if (isCodeTest(root)) {
    if (localFileSuppliedButNotFound(root, options.file)) {
      throw new Error('File not found: ' + options.file);
    }
    var file = options.file || detectPackageFile(root) || 'package.json';
    packageManager = detectPackageManagerFromFile(file);
  } else {
    var registry = options.registry || 'npm';
    packageManager = detectPackageManagerFromRegistry(registry);
  }
  return packageManager;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.snyk.error"></a>[module snyk.error](#apidoc.module.snyk.error)

#### <a name="apidoc.element.snyk.error.error"></a>[function <span class="apidocSignatureSpan">snyk.</span>error (command)](#apidoc.element.snyk.error.error)
- description and source-code
```javascript
function error(command) {
  var e = new Error('Unknown command "' + command + '"');
  e.code = 'UNKNOWN_COMMAND';
  return Promise.reject(e);
}
```
- example usage
```shell
...
cwd: cwd,
    }, function (error, stdout, stderr) {
if (error) {
  return reject(error);
}

if (stderr.indexOf('ERR!') !== -1) {
  console.error(stderr.trim());
  var e = new Error('npm update errors');
  e.code = 'FAIL_UPDATE';
  return reject(e);
}

debug('npm %s complete', method);
...
```

#### <a name="apidoc.element.snyk.error.message"></a>[function <span class="apidocSignatureSpan">snyk.error.</span>message (error)](#apidoc.element.snyk.error.message)
- description and source-code
```javascript
message = function (error) {
  var message = error; // defaults to a string (which is super unlikely)
  if (error instanceof Error) {
    if (error.code === 'VULNS') {
      return error.message;
    }

    // try to lookup the error string based either on the error code OR
    // the actual error.message (which can be "Unauthorized" for instance),
    // otherwise send the error message back
    message = codes[error.code || error.message] ||
              errors[error.code || error.message];
    if (message) {
      message = message.replace(/(%s)/g, error.message).trim();
      message = chalk.bold.red(message);
    } else if (error.code) { // means it's a code error
      message = 'An unknown error occurred. Please include the trace below ' +
                'when reporting to Snyk:\n\n' + error.stack;
    } else { // should be one of ours
      message = error.message;
    }
  }

  return message;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.snyk.isolate"></a>[module snyk.isolate](#apidoc.module.snyk.isolate)

#### <a name="apidoc.element.snyk.isolate.okay"></a>[function <span class="apidocSignatureSpan">snyk.isolate.</span>okay ()](#apidoc.element.snyk.isolate.okay)
- description and source-code
```javascript
okay = function () {
  return true;
}
```
- example usage
```shell
...
  snyk.bus.emit('after:module', module);
}

function registerExtension(ext) {
  var old = oldHandlers[ext] || oldHandlers['.js'] || require.extensions['.js'];

  require.extensions[ext] = function (m, filename) {
    if (snyk.isolate.okay(filename)) {
      loader(m, filename, old);
    }
  };
}


function hookExtensions(_exts) {
...
```



# <a name="apidoc.module.snyk.modules"></a>[module snyk.modules](#apidoc.module.snyk.modules)

#### <a name="apidoc.element.snyk.modules.modules"></a>[function <span class="apidocSignatureSpan">snyk.</span>modules (dir, options)](#apidoc.element.snyk.modules.modules)
- description and source-code
```javascript
modules = function (dir, options) {
  return physicalTree(dir).then(function (res) {
    return logicalTree(res, options);
  });
}
```
- example usage
```shell
...
    }

    return acc;
  }, []).sort().shift();

  // then collect all the package deps and post a monitor
  var cwd = path.resolve(candidate, '..');
  snyk.modules(cwd).then(snyk.monitor.bind(null, cwd, {
    method: 'require',
  }));
}
...
```

#### <a name="apidoc.element.snyk.modules.logicalTree"></a>[function <span class="apidocSignatureSpan">snyk.modules.</span>logicalTree (fileTree, options)](#apidoc.element.snyk.modules.logicalTree)
- description and source-code
```javascript
function logicalTree(fileTree, options) {
  if (!options) {
    options = {};
  }

  problems = [];
  var logicalRoot = copy(fileTree, fileTree.__from, true);
  logicalRoot.dependencies = walkDeps(fileTree, fileTree);

  var removedPaths = [];

  if (!options.dev) {
    // do a shallow pass on the deps and strip out dev deps
    Object.keys(fileTree.dependencies).forEach(function (name) {
      var dep = fileTree.dependencies[name];
      // if we're not interested in devDeps, then strip them out
      if (dep.depType === depTypes.DEV) {
        // since dev deps are only ever on the root, we know we can remove it
        // directly from the logicalRoot.dependencies
        removedPaths.push(dep.__from);
        delete logicalRoot.dependencies[dep.name];
        return;
      }
    });
  }

  logicalRoot.numFileDependencies = 0;

  walk(fileTree.dependencies, function (dep) {
    logicalRoot.numFileDependencies++;
    if (!dep.__used) {
      var deppath = dep.__from.slice(0, -1).toString();
      var removed = removedPaths.filter(function (path) {
        return deppath.indexOf(path) === 0;
      }).length;

      if (removed) {
        return false; // this was from a dev dep, so let's lose it
      }

      var leaf = copy(dep);

      var issue = format('%s: %s@%s (from %s) > %s', ext, leaf.name,
        leaf.version, leaf.dep, path.relative('.', leaf.__filename));
      leaf.problems = [issue];
      problems.push(issue);
      leaf.extraneous = true;
      leaf.depType = depTypes.EXTRANEOUS;
      leaf.dependencies = walkDeps(fileTree, dep);
      walk(leaf.dependencies, function (dep) {
        dep.extraneous = true;
        dep.depType = depTypes.EXTRANEOUS;
      });
      insertLeaf(logicalRoot, leaf, dep.__from);
    }
  });

  logicalRoot.numDependencies = Object.keys(
    unique(logicalRoot).dependencies
  ).length;

  logicalRoot.pluck = pluck.bind(null, fileTree);
  logicalRoot.unique = unique.bind(null, logicalRoot);
  logicalRoot.problems = problems.slice(0);

  return logicalRoot;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.snyk.modules.physicalTree"></a>[function <span class="apidocSignatureSpan">snyk.modules.</span>physicalTree (root, depType)](#apidoc.element.snyk.modules.physicalTree)
- description and source-code
```javascript
function loadModules(root, depType) {
  tryRequire.cache.reset(); // reset the package cache on re-run
  return loadModulesInternal(root, depType || null).then(function (tree) {
    // ensure there's no missing packages our known root deps
    var missing = [];
    if (tree.__dependencies) {
      Object.keys(tree.__dependencies).forEach(function (name) {
        if (!tree.dependencies[name]) {
          missing.push(resolve(name, root).then(function (dir) {
            return loadModulesInternal(dir, depTypes.PROD, {
              __from: [tree.name + '@' + tree.version, name],
            });
          }).catch(function (e) {
            if (e.code === 'NO_PACKAGE_FOUND') {
              return false;
            }
          }));
        }
      });
    }

    if (missing.length) {
      return Promise.all(missing).then(function (packages) {
        packages.filter(Boolean).forEach(function (pkg) {
          pkg.dep = tree.__dependencies[pkg.name];
          tree.dependencies[pkg.name] = pkg;
        });
        return tree;
      });
    }

    return tree;
  });

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.snyk.modules.pluck"></a>[function <span class="apidocSignatureSpan">snyk.modules.</span>pluck (root, path, name, range)](#apidoc.element.snyk.modules.pluck)
- description and source-code
```javascript
function pluck(root, path, name, range) {
  if (range === 'latest') {
    range = '*';
  }

  // Cycle through the tree path via the root tree object **ala node require**.
  // note that we don't need the first item in the path (which is the root
  // package name).
  var from = path.slice(0);
  var rootPath = moduleToObject(from.shift(), parseOptions).name;

  // if the root of the virtual tree doesn't even match our path, bail out
  if (rootPath !== root.name) {
    return false;
  }

  // do a check to see if the last item in the path is actually the package
  // we're looking for, and if it's not, push it on
  if (from.length !== 0 &&
      moduleToObject(from.slice(-1).pop(), parseOptions).name === name) {
    from.pop();
  }

  // then we always put the target package on the end of the chain
  // to ensure it's in exactly the right format to be used in 'getMatch'
  from.push(name + '@' + range);

  debug('using forward search %s@%s in %s', from.join(' > '));

  var match = false;
  var leaf = root;
  var realPath = [];

  while (from.length) {
    var pkg = moduleToObject(from[0], parseOptions);
    var test = getMatch(leaf, pkg.name, pkg.version);

    if (test) {
      from.shift();
      realPath.push(leaf);
      leaf = test;
    } else {
      leaf = realPath.pop();
      if (!leaf) {
        return false;
      }
    }
  }

  return leaf.name === name ? leaf : false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.snyk.modules.prune"></a>[function <span class="apidocSignatureSpan">snyk.modules.</span>prune (pkg, shouldPrune)](#apidoc.element.snyk.modules.prune)
- description and source-code
```javascript
function prune(pkg, shouldPrune) {
  var remove = shouldPrune(pkg);
  if (!remove) {
    pkg.dependencies = {};
  }

  var deps = Object.keys(pkg.dependencies || {});

  if (deps.length) {
    remove = deps.filter(function (name) {
      if (prune(pkg.dependencies[name], shouldPrune)) {
        delete pkg.dependencies[name];
        return false;
      }
      return true;
    }).length;
    remove = remove === 0;
  }

  return remove;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.snyk.modules.unique"></a>[function <span class="apidocSignatureSpan">snyk.modules.</span>unique (deps)](#apidoc.element.snyk.modules.unique)
- description and source-code
```javascript
function unique(deps) {
  var res = copy(deps);
  res.dependencies = {};

  walk(deps, function (dep) {
    var shallowCopy = copy(dep);
    res.dependencies[dep.name + '@' + dep.version] = shallowCopy;
  });

  return res;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.snyk.modules.walk"></a>[function <span class="apidocSignatureSpan">snyk.modules.</span>walk (deps, filter)](#apidoc.element.snyk.modules.walk)
- description and source-code
```javascript
function walk(deps, filter) {
  if (!deps) {
    return [];
  }

  if (deps.dependencies) {
    deps = deps.dependencies;
  }

  Object.keys(deps).forEach(function (name) {
    var res = filter(deps[name], name, deps);
    if (!res && deps[name] && deps[name].dep) {
      walk(deps[name].dependencies, filter);
    }
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.snyk.policy"></a>[module snyk.policy](#apidoc.module.snyk.policy)

#### <a name="apidoc.element.snyk.policy.add"></a>[function <span class="apidocSignatureSpan">snyk.policy.</span>add (policy, type, options)](#apidoc.element.snyk.policy.add)
- description and source-code
```javascript
function add(policy, type, options) {
  if (type !== 'ignore' && type !== 'patch') {
    throw new Error('policy.add: unknown type "' + type + '" to add to');
  }

  if (!options || !options.id || !options.path) {
    throw new Error('policy.add: required option props { id, path }');
  }

  var id = options.id;
  var path = options.path;
  var data = Object.keys(options).reduce(function (acc, curr) {
    if (curr === 'id' || curr === 'path') {
      return acc;
    }

    acc[curr] = options[curr];
    return acc;
  }, {});

  if (!policy[type][id]) {
    policy[type][id] = [];
  }

<span class="apidocCodeCommentSpan">  /* istanbul ignore if */
</span>  if (policy[type][id][path]) {
    debug('policy.add: path already exists', policy[type][id][path]);
  }

  var rule = {};
  rule[path] = data;

  policy[type][id].push(rule);

  return policy;
}
```
- example usage
```shell
...
policyLocations = policyLocations.concat(pluckPolicies(modules));
var opts = { loose: true };
var packageManager = meta.packageManager || 'npm';
return apiTokenExists('snyk monitor')
  .then(function () {
    return snyk.policy.load(policyLocations, opts);
  }).then(function (policy) {
    analytics.add('packageManager', packageManager);
    // YARN temporary fix to avoid BE changes
    packageManager = packageManager === 'yarn' ? 'npm' : packageManager;
    return new Promise(function (resolve, reject) {
      request({
        body: {
          meta: {
            method: meta.method,
...
```

#### <a name="apidoc.element.snyk.policy.create"></a>[function <span class="apidocSignatureSpan">snyk.policy.</span>create ()](#apidoc.element.snyk.policy.create)
- description and source-code
```javascript
function create() {
  return loadFromText('');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.snyk.policy.demunge"></a>[function <span class="apidocSignatureSpan">snyk.policy.</span>demunge (policy, apiRoot)](#apidoc.element.snyk.policy.demunge)
- description and source-code
```javascript
function demunge(policy, apiRoot) {
  if (!apiRoot) {
    apiRoot = '';
  }

  var res = ['ignore', 'patch'].reduce(function (acc, type) {
    acc[type] = policy[type] ? Object.keys(policy[type]).map(function (id) {
      var paths = policy[type][id].map(function (pathObj) {
        var path = Object.keys(pathObj).pop();
        var res = {
          path: path,
        };
        if (type === 'ignore') {
          res.reason = pathObj[path].reason;
          res.expires = new Date(pathObj[path].expires);
        }

        return res;
      });
      return {
        id: id,
        url: apiRoot + '/vuln/' + id,
        paths: paths,
      };
    }) : [];
    return acc;
  }, {});

  res.version = policy.version;

  return res;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.snyk.policy.filter"></a>[function <span class="apidocSignatureSpan">snyk.policy.</span>filter (vulns, policy, root)](#apidoc.element.snyk.policy.filter)
- description and source-code
```javascript
function filter(vulns, policy, root) {
  if (!root) {
    root = process.cwd();
  }

  if (vulns.ok) {
    return vulns;
  }

  var filtered = {
    ignore: [],
    patch: [],
  };

  // strip the ignored modules from the results
  vulns.vulnerabilities = ignore(
    policy.ignore,
    vulns.vulnerabilities,
    filtered.ignore
  );

  vulns.vulnerabilities = patch(
    policy.patch,
    vulns.vulnerabilities,
    root,
    policy.skipVerifyPatch ? true : false,
    filtered.patch
  );

  if (policy.suggest) {
    vulns.vulnerabilities = notes(
      policy.suggest,
      vulns.vulnerabilities,
      root
    );
  }

  // if there's no vulns after the ignore process, let's reset the 'ok'
  // state and remove the vulns entirely.
  if (vulns.vulnerabilities.length === 0) {
    vulns.ok = true;
    vulns.vulnerabilities = [];
  }

  vulns.filtered = filtered;

  debug('> has threshold? %s', policy.failThreshold);

  if (policy.failThreshold && vulns.ok === false) {
    // check what's left and switch the failure flag if there's anything
    // under our threshold
    var levels = {
      high: 3,
      medium: 2,
      low: 1,
    };
    var level = levels[policy.failThreshold];
    vulns.ok = true;
    vulns.vulnerabilities.some(function (vuln) {
      if (levels[vuln.severity] >= level) {
        vulns.ok = false;
        return true; // breaks
      }
    });
  }

  return vulns;
}
```
- example usage
```shell
...
  'bamboo.buildKey',
  'PHPCI',
  'GOCD_SERVER_HOST',
  'BUILDKITE',
  'TF_BUILD',
];

module.exports = !!Object.keys(process.env).filter(function (env) {
  return ciEnvs.indexOf(env) !== -1;
}).length;
...
```

#### <a name="apidoc.element.snyk.policy.getByVuln"></a>[function <span class="apidocSignatureSpan">snyk.policy.</span>getByVuln (policy, vuln)](#apidoc.element.snyk.policy.getByVuln)
- description and source-code
```javascript
function getByVuln(policy, vuln) {
  var found = null;

  if (!policy || !vuln) {
    return found;
  }

  ['ignore', 'patch'].forEach(function (key) {
    Object.keys(policy[key] || []).forEach(function (p) {
      if (p === vuln.id) {
        policy[key][p].forEach(function (rule) {
          if (matchToRule(vuln, rule)) {
            found = {
              type: key,
              id: vuln.id,
              rule: vuln.from,
            };
            var rootRule = Object.keys(rule).pop();
            Object.keys(rule[rootRule]).forEach(function (key) {
              found[key] = rule[rootRule][key];
            });
          }
        });
      }
    });
  });

  return found;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.snyk.policy.load"></a>[function <span class="apidocSignatureSpan">snyk.policy.</span>load (root, options)](#apidoc.element.snyk.policy.load)
- description and source-code
```javascript
function load(root, options) {
  if (!Array.isArray(root) && typeof root !== 'string') {
    options = root;
    root = null;
  }

  if (!root) {
    root = process.cwd();
  }

  if (!options) {
    options = {};
  }

  var ignorePolicy = !!options['ignore-policy'];

  var filename = '';
  if (Array.isArray(root)) {
    // we do a bit of a dance to get the first item in the array, and
    // use it as our filename
    filename = root[0];
  } else {
    if (root.indexOf('.snyk') === -1) {
      root = path.resolve(root, '.snyk');
    }
    filename = root;
  }

  if (filename.indexOf('.snyk') === -1) {
    filename = path.resolve(filename, '.snyk');
  }

  var promise = new Promise(function (resolve) {
    if (ignorePolicy) {
      return resolve(parse.import());
    }

    if (!ignorePolicy && Array.isArray(root)) {
      return resolve(mergePolicies(root, options).then(function (res) {
        debug('final policy:');
        debug(JSON.stringify(res, '', 2));
        return res;
      }));
    }

    resolve(fs.readFile(filename, 'utf8').then(parse.import));
  });

  var promises = [
    promise,
    fs.stat(filename).catch(function () {
      return {};
    }),
  ];

  return Promise.all(promises).catch(function (error) {
    if (options.loose && error.code === 'ENOENT') {
      debug('ENOENT on file, but running loose');
      return [parse.import(), {}];
    }

    throw error;
  }).then(function (res) {
    var policy = res[0];

    policy.__modified = res[1].mtime;
    policy.__created = res[1].birthtime || res[1].ctime;

    if (options.loose && !policy.__modified) {
      policy.__filename = null;
    } else {
      policy.__filename = path.relative(process.cwd(), filename);
    }

    return policy;
  }).then(attachMethods);
}
```
- example usage
```shell
...
function monitor(root, meta, modules) {
var policyLocations = [root];
policyLocations = policyLocations.concat(pluckPolicies(modules));
var opts = { loose: true };
var packageManager = meta.packageManager || 'npm';
return apiTokenExists('snyk monitor')
  .then(function () {
    return snyk.policy.load(policyLocations, opts);
  }).then(function (policy) {
    analytics.add('packageManager', packageManager);
    // YARN temporary fix to avoid BE changes
    packageManager = packageManager === 'yarn' ? 'npm' : packageManager;
    return new Promise(function (resolve, reject) {
      request({
        body: {
...
```

#### <a name="apidoc.element.snyk.policy.loadFromText"></a>[function <span class="apidocSignatureSpan">snyk.policy.</span>loadFromText (text)](#apidoc.element.snyk.policy.loadFromText)
- description and source-code
```javascript
function loadFromText(text) {
  return new Promise(function (resolve) {
    var policy = parse.import(text);
    var now = Date.now();

    policy.__filename = '';
    policy.__modified = now;
    policy.__created = now;

    resolve(policy);
  }).then(attachMethods);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.snyk.policy.matchToRule"></a>[function <span class="apidocSignatureSpan">snyk.policy.</span>matchToRule (vuln, rule)](#apidoc.element.snyk.policy.matchToRule)
- description and source-code
```javascript
function matchToRule(vuln, rule) {
  return Object.keys(rule).some(function (path) {
    return matchToSingleRule(vuln, path);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.snyk.policy.save"></a>[function <span class="apidocSignatureSpan">snyk.policy.</span>save (object, root, spinner)](#apidoc.element.snyk.policy.save)
- description and source-code
```javascript
function save(object, root, spinner) {
  var filename = root ?
    path.resolve(root, '.snyk') :
    defaultFilename();

  var lbl = 'Saving .snyk policy file...';

  if (!spinner) {
    spinner = function (res) {
      return Promise.resolve(res);
    };
    spinner.clear = spinner;
  }

  return spinner(lbl).then(function () {
    return parse.export(object);
  }).then(function (yaml) {
    return fs.writeFile(filename, yaml);
  }).then(spinner.clear(lbl));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.snyk.spinner"></a>[module snyk.spinner](#apidoc.module.snyk.spinner)

#### <a name="apidoc.element.snyk.spinner.spinner"></a>[function <span class="apidocSignatureSpan">snyk.</span>spinner (label)](#apidoc.element.snyk.spinner.spinner)
- description and source-code
```javascript
function createSpinner(label) {
  if (!label) {
    throw new Error('spinner requires a label');
  }

  if (spinners[label] === undefined) {
    spinners[label] = [];
  }

  // helper...
  return new Promise(function (resolve) {
    debug('spinner: %s', label);
    spinners[label].push(spinner({
      // string: '◐◓◑◒',
      stream: sticky ? process.stdout : process.stderr,
      interval: 75,
      label: label,
    }));

    resolve();
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.snyk.spinner.clear"></a>[function <span class="apidocSignatureSpan">snyk.spinner.</span>clear (label)](#apidoc.element.snyk.spinner.clear)
- description and source-code
```javascript
clear = function (label) {
  if (spinners[label] === undefined) {
    throw new Error('unknown spinner label: ' + label);
  }

  return function (res) {
    debug('clearing %s (%s)', label, spinners[label].length);
    if (spinners[label].length) {
      var s = spinners[label].pop();
      if (s) {
        s.clear();
      }
    }
    return res;
  };
}
```
- example usage
```shell
...
  }

  return function (res) {
    debug('clearing %s (%s)', label, spinners[label].length);
    if (spinners[label].length) {
      var s = spinners[label].pop();
      if (s) {
        s.clear();
      }
    }
    return res;
  };
};

createSpinner.clearAll = function () {
...
```

#### <a name="apidoc.element.snyk.spinner.clearAll"></a>[function <span class="apidocSignatureSpan">snyk.spinner.</span>clearAll ()](#apidoc.element.snyk.spinner.clearAll)
- description and source-code
```javascript
clearAll = function () {
  Object.keys(spinners).map(function (lbl) {
    createSpinner.clear(lbl)();
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.snyk.spinner.sticky"></a>[function <span class="apidocSignatureSpan">snyk.spinner.</span>sticky (s)](#apidoc.element.snyk.spinner.sticky)
- description and source-code
```javascript
sticky = function (s) {
  sticky = s === undefined ? true : s;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.snyk.sub_process"></a>[module snyk.sub_process](#apidoc.module.snyk.sub_process)

#### <a name="apidoc.element.snyk.sub_process.execute"></a>[function <span class="apidocSignatureSpan">snyk.sub_process.</span>execute (command, args, options)](#apidoc.element.snyk.sub_process.execute)
- description and source-code
```javascript
execute = function (command, args, options) {
  var spawnOptions = { shell: true };
  if (options && options.cwd) {
    spawnOptions.cwd = options.cwd;
  }

  return new Promise(function (resolve, reject) {
    var stdout = '';
    var stderr = '';

    var proc = childProcess.spawn(command, args, spawnOptions);
    proc.stdout.on('data', function (data) { stdout = stdout + data; });
    proc.stderr.on('data', function (data) { stderr = stderr + data; });

    proc.on('close', function (code) {
      if (code !== 0) {
        return reject(stdout || stderr);
      }
      resolve({ stdout: stdout, stderr: stderr });
    });
  });
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
