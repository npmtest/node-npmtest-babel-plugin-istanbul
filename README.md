# npmtest-babel-plugin-istanbul

#### basic test coverage for  [babel-plugin-istanbul (v4.1.1)](https://github.com/istanbuljs/babel-plugin-istanbul#readme)  [![npm package](https://img.shields.io/npm/v/npmtest-babel-plugin-istanbul.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-babel-plugin-istanbul) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-babel-plugin-istanbul.svg)](https://travis-ci.org/npmtest/node-npmtest-babel-plugin-istanbul)

#### A babel plugin that adds istanbul instrumentation to ES6 code

[![NPM](https://nodei.co/npm/babel-plugin-istanbul.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/babel-plugin-istanbul)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-babel-plugin-istanbul/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-babel-plugin-istanbul/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-babel-plugin-istanbul/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-babel-plugin-istanbul/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-babel-plugin-istanbul/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-babel-plugin-istanbul/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-babel-plugin-istanbul/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-babel-plugin-istanbul/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-babel-plugin-istanbul/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-babel-plugin-istanbul/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-babel-plugin-istanbul/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-babel-plugin-istanbul/build/test-report.html](https://npmtest.github.io/node-npmtest-babel-plugin-istanbul/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-babel-plugin-istanbul/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-babel-plugin-istanbul/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-babel-plugin-istanbul/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-babel-plugin-istanbul/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-babel-plugin-istanbul/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-babel-plugin-istanbul/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-babel-plugin-istanbul/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-babel-plugin-istanbul/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "babel-plugin-istanbul",
    "version": "4.1.1",
    "author": "Thai Pangsakulyanont @dtinth",
    "license": "BSD-3-Clause",
    "description": "A babel plugin that adds istanbul instrumentation to ES6 code",
    "main": "lib/index.js",
    "files": [
        "lib"
    ],
    "dependencies": {
        "find-up": "^2.1.0",
        "istanbul-lib-instrument": "^1.6.2",
        "test-exclude": "^4.0.3"
    },
    "devDependencies": {
        "babel-cli": "^6.18.0",
        "babel-core": "^6.21.0",
        "babel-preset-es2015": "^6.18.0",
        "chai": "^3.5.0",
        "coveralls": "^2.11.16",
        "cross-env": "^3.1.4",
        "mocha": "^3.2.0",
        "nyc": "^10.0.0",
        "pmock": "^0.2.3",
        "standard": "^8.6.0",
        "standard-version": "^4.0.0"
    },
    "scripts": {
        "coverage": "nyc report --reporter=text-lcov | coveralls",
        "release": "babel src --out-dir lib",
        "pretest": "standard && npm run release",
        "test": "cross-env NODE_ENV=test nyc --reporter=lcov --reporter=text mocha test/*.js",
        "prepublish": "npm test && npm run release",
        "version": "standard-version"
    },
    "standard": {
        "ignore": [
            "fixtures/has-inline-source-map.js"
        ]
    },
    "repository": {
        "type": "git",
        "url": "git+https://github.com/istanbuljs/babel-plugin-istanbul.git"
    },
    "keywords": [
        "istanbul",
        "babel",
        "plugin",
        "instrumentation"
    ],
    "nyc": {
        "include": [
            "src/*.js",
            "fixtures/should-cover.js"
        ],
        "require": [
            "babel-core/register"
        ],
        "sourceMap": false,
        "instrument": false
    },
    "bugs": {
        "url": "https://github.com/istanbuljs/babel-plugin-istanbul/issues"
    },
    "homepage": "https://github.com/istanbuljs/babel-plugin-istanbul#readme",
    "greenkeeper": {
        "ignore": [
            "find-up",
            "cross-env"
        ]
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
