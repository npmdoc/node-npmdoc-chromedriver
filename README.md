# api documentation for  [chromedriver (v2.28.0)](https://github.com/giggio/node-chromedriver)  [![npm package](https://img.shields.io/npm/v/npmdoc-chromedriver.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-chromedriver) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-chromedriver.svg)](https://travis-ci.org/npmdoc/node-npmdoc-chromedriver)
#### ChromeDriver for Selenium

[![NPM](https://nodei.co/npm/chromedriver.png?downloads=true)](https://www.npmjs.com/package/chromedriver)

[![apidoc](https://npmdoc.github.io/node-npmdoc-chromedriver/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-chromedriver_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-chromedriver/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-chromedriver/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-chromedriver/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Giovanni Bassi",
        "email": "giggio@giggio.net",
        "url": "http://www.lambda3.com.br"
    },
    "bin": {
        "chromedriver": "./bin/chromedriver"
    },
    "bugs": {
        "url": "https://github.com/giggio/node-chromedriver/issues"
    },
    "dependencies": {
        "adm-zip": "^0.4.7",
        "kew": "^0.7.0",
        "mkdirp": "^0.5.1",
        "rimraf": "^2.5.4"
    },
    "description": "ChromeDriver for Selenium",
    "devDependencies": {},
    "directories": {},
    "dist": {
        "shasum": "ea0c383621dd27db340c612b85fe39414c16ec79",
        "tarball": "https://registry.npmjs.org/chromedriver/-/chromedriver-2.28.0.tgz"
    },
    "gitHead": "4d1f06f2908f69f044f81bd241d5d4d8e26f2461",
    "homepage": "https://github.com/giggio/node-chromedriver",
    "keywords": [
        "chromedriver",
        "selenium"
    ],
    "licenses": [
        {
            "type": "Apache 2.0",
            "url": "http://www.apache.org/licenses/LICENSE-2.0.html"
        }
    ],
    "main": "lib/chromedriver",
    "maintainers": [
        {
            "name": "giggio",
            "email": "giggio@giggio.net"
        }
    ],
    "name": "chromedriver",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/giggio/node-chromedriver.git"
    },
    "scripts": {
        "install": "node install.js"
    },
    "version": "2.28.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module chromedriver](#apidoc.module.chromedriver)
1.  [function <span class="apidocSignatureSpan">chromedriver.</span>start (args)](#apidoc.element.chromedriver.start)
1.  [function <span class="apidocSignatureSpan">chromedriver.</span>stop ()](#apidoc.element.chromedriver.stop)
1.  string <span class="apidocSignatureSpan">chromedriver.</span>path
1.  string <span class="apidocSignatureSpan">chromedriver.</span>version



# <a name="apidoc.module.chromedriver"></a>[module chromedriver](#apidoc.module.chromedriver)

#### <a name="apidoc.element.chromedriver.start"></a>[function <span class="apidocSignatureSpan">chromedriver.</span>start (args)](#apidoc.element.chromedriver.start)
- description and source-code
```javascript
start = function (args) {
  exports.defaultInstance = require('child_process').execFile(exports.path, args);
  return exports.defaultInstance;
}
```
- example usage
```shell
...

'''javascript
var chromedriver = require('chromedriver');

args = [
	// optional arguments
];
chromedriver.start(args);
// run your tests
chromedriver.stop();

'''
Note: if your tests are ran asynchronously, chromedriver.stop() will have to be
executed as a callback at the end of your tests
...
```

#### <a name="apidoc.element.chromedriver.stop"></a>[function <span class="apidocSignatureSpan">chromedriver.</span>stop ()](#apidoc.element.chromedriver.stop)
- description and source-code
```javascript
stop = function () {
  if (exports.defaultInstance != null){
    exports.defaultInstance.kill();
  }
}
```
- example usage
```shell
...
var chromedriver = require('chromedriver');

args = [
	// optional arguments
];
chromedriver.start(args);
// run your tests
chromedriver.stop();

'''
Note: if your tests are ran asynchronously, chromedriver.stop() will have to be
executed as a callback at the end of your tests

Versioning
----------
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
