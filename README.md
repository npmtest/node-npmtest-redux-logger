# npmtest-redux-logger

#### test coverage for  [redux-logger (v3.0.1)](https://github.com/theaqua/redux-logger#readme)  [![npm package](https://img.shields.io/npm/v/npmtest-redux-logger.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-redux-logger) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-redux-logger.svg)](https://travis-ci.org/npmtest/node-npmtest-redux-logger)

#### Logger for Redux

[![NPM](https://nodei.co/npm/redux-logger.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/redux-logger)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-redux-logger/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-redux-logger/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-redux-logger/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-redux-logger/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-redux-logger/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-redux-logger/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-redux-logger/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-redux-logger/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-redux-logger/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-redux-logger/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-redux-logger/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-redux-logger/build/test-report.html](https://npmtest.github.io/node-npmtest-redux-logger/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-redux-logger/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-redux-logger/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-redux-logger/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-redux-logger/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-redux-logger/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-redux-logger/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-redux-logger/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-redux-logger/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Eugene Rodionov",
        "url": "https://github.com/theaqua"
    },
    "bugs": {
        "url": "https://github.com/theaqua/redux-logger/issues"
    },
    "dependencies": {
        "deep-diff": "0.3.4"
    },
    "description": "Logger for Redux",
    "devDependencies": {
        "@dtrussia/eslint-config-dtrussia": "2.2.1",
        "babel-cli": "^6.24.0",
        "babel-core": "^6.24.0",
        "babel-eslint": "7.1.1",
        "babel-loader": "^6.4.1",
        "babel-plugin-add-module-exports": "0.2.1",
        "babel-plugin-transform-es2015-modules-umd": "6.24.0",
        "babel-plugin-transform-inline-environment-variables": "6.8.0",
        "babel-preset-es2015": "^6.24.0",
        "babel-preset-react": "^6.23.0",
        "babel-preset-stage-0": "^6.22.0",
        "chai": "3.5.0",
        "codecov": "1.0.1",
        "eslint": "3.10.2",
        "eslint-plugin-react": "6.7.1",
        "http-server": "0.9.0",
        "husky": "^0.13.2",
        "mocha": "3.1.2",
        "nyc": "9.0.1",
        "open-url": "2.0.2",
        "redux": "^3.6.0",
        "rimraf": "^2.6.1",
        "sinon": "^1.17.7",
        "webpack": "1.13.3"
    },
    "directories": {},
    "dist": {
        "shasum": "ae8ae4c3c55ed3dd7aa31509f0856c5d3751057a",
        "tarball": "https://registry.npmjs.org/redux-logger/-/redux-logger-3.0.1.tgz"
    },
    "files": [
        "dist",
        "lib",
        "src"
    ],
    "gitHead": "9ec10bb21ea2b1ba19f0c4aae44b228247c64bad",
    "homepage": "https://github.com/theaqua/redux-logger#readme",
    "keywords": [
        "redux",
        "logger",
        "redux-logger",
        "middleware"
    ],
    "license": "MIT",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "evgenyrodionov"
        },
        {
            "name": "toxic"
        }
    ],
    "name": "redux-logger",
    "nyc": {
        "exclude": [
            "node_modules",
            "spec",
            "example",
            "lib",
            "dist",
            "webpack.*.js"
        ]
    },
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/theaqua/redux-logger.git"
    },
    "scripts": {
        "build": "npm run build:lib && npm run build:umd && npm run build:umd:min",
        "build:lib": "$(npm bin)/babel src --out-dir lib",
        "build:umd": "LIBRARY_NAME=reduxLogger NODE_ENV=development $(npm bin)/webpack src/index.js dist/index.js --config webpack.build.js",
        "build:umd:min": "LIBRARY_NAME=reduxLogger NODE_ENV=production $(npm bin)/webpack -p src/index.js dist/index.min.js --config webpack.build.js",
        "clean": "$(npm bin)/rimraf dist lib",
        "coverage": "nyc report",
        "coverage:html": "nyc report --reporter=html && (http-server -p 8077 ./coverage & open-url http://localhost:8077/)",
        "coverage:production": "nyc report --reporter=text-lcov > coverage.lcov && codecov",
        "lint": "$(npm bin)/eslint src",
        "precommit": "npm run test",
        "prepublish": "npm run clean && npm run test:production && npm run build",
        "spec": "NODE_PATH=src nyc --all --silent --require babel-core/register mocha --plugins transform-inline-environment-variables --recursive spec/*.spec.js",
        "spec:watch": "NODE_ENV=development npm run spec -- --watch",
        "test": "NODE_ENV=development npm run lint && npm run spec",
        "test:production": "NODE_ENV=production npm run lint && npm run spec"
    },
    "version": "3.0.1"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
