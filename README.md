# npmdoc-mqtt

#### basic api documentation for  [mqtt (v2.6.2)](https://github.com/mqttjs/MQTT.js#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-mqtt.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-mqtt) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-mqtt.svg)](https://travis-ci.org/npmdoc/node-npmdoc-mqtt)

#### A library for the MQTT protocol

[![NPM](https://nodei.co/npm/mqtt.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/mqtt)

- [https://npmdoc.github.io/node-npmdoc-mqtt/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-mqtt/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-mqtt/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-mqtt/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-mqtt/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-mqtt/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bin": {
        "mqtt_pub": "./bin/pub.js",
        "mqtt_sub": "./bin/sub.js",
        "mqtt": "./mqtt.js"
    },
    "browser": {
        "./mqtt.js": "./lib/connect/index.js",
        "fs": false,
        "tls": false,
        "net": false
    },
    "bugs": {
        "url": "https://github.com/mqttjs/MQTT.js/issues"
    },
    "contributors": [
        {
            "name": "Adam Rudd"
        },
        {
            "name": "Matteo Collina",
            "url": "https://github.com/mcollina"
        }
    ],
    "dependencies": {
        "commist": "^1.0.0",
        "concat-stream": "^1.6.0",
        "end-of-stream": "^1.1.0",
        "help-me": "^1.0.1",
        "inherits": "^2.0.3",
        "minimist": "^1.2.0",
        "mqtt-packet": "^5.2.1",
        "pump": "^1.0.2",
        "readable-stream": "^2.2.9",
        "reinterval": "^1.1.0",
        "split2": "^2.1.1",
        "websocket-stream": "^4.0.0",
        "xtend": "^4.0.1"
    },
    "description": "A library for the MQTT protocol",
    "devDependencies": {
        "browserify": "^14.1.0",
        "codecov": "^2.0.0",
        "istanbul": "^0.4.5",
        "mkdirp": "^0.5.1",
        "mocha": "^3.2.0",
        "mqtt-connection": "^3.0.0",
        "nsp": "^2.6.2",
        "pre-commit": "^1.2.2",
        "rimraf": "^2.6.1",
        "should": "*",
        "sinon": "~1.17.7",
        "snazzy": "^7.0.0",
        "standard": "^10.0.0",
        "through2": "^2.0.3",
        "tslint": "^4.5.1",
        "tslint-config-standard": "^4.0.0",
        "typescript": "^2.2.1",
        "uglify": "^0.1.5",
        "uglify-js": "^2.7.5",
        "ws": "^2.0.0",
        "zuul": "^3.11.1",
        "zuul-ngrok": "^4.0.0"
    },
    "directories": {},
    "dist": {
        "shasum": "9dc5fc853dd4a049c859e24c6754b42f18ce8774",
        "tarball": "https://registry.npmjs.org/mqtt/-/mqtt-2.6.2.tgz"
    },
    "engines": {
        "node": ">=4.0.0"
    },
    "files": [
        "dist/",
        "CONTRIBUTING.md",
        "doc",
        "lib",
        "bin",
        "examples",
        "test",
        "types",
        "mqtt.js"
    ],
    "gitHead": "e6bd5bc3ba6257c174d72b51374c1d8792d7b338",
    "homepage": "https://github.com/mqttjs/MQTT.js#readme",
    "keywords": [
        "mqtt",
        "publish/subscribe",
        "publish",
        "subscribe"
    ],
    "license": "MIT",
    "main": "mqtt.js",
    "maintainers": [
        {
            "name": "adamvr"
        },
        {
            "name": "matteo.collina"
        }
    ],
    "name": "mqtt",
    "optionalDependencies": {},
    "pre-commit": [
        "test"
    ],
    "repository": {
        "type": "git",
        "url": "git://github.com/mqttjs/MQTT.js.git"
    },
    "scripts": {
        "browser-build": "rimraf dist/ && mkdirp dist/ && browserify mqtt.js -s mqtt > dist/mqtt.js && uglifyjs --screw-ie8 < dist/mqtt.js > dist/mqtt.min.js",
        "browser-test": "zuul --server test/browser/server.js --local --open test/browser/test.js",
        "ci": "npm run tslint && npm run test && codecov",
        "prepublish": "nsp check && npm run browser-build",
        "pretest": "standard | snazzy",
        "sauce-test": "zuul --server test/browser/server.js --tunnel ngrok -- test/browser/test.js",
        "test": "istanbul cover ./node_modules/mocha/bin/_mocha --report lcovonly -- --bail",
        "tslint": "tslint types/**/*.d.ts"
    },
    "standard": {
        "env": [
            "mocha"
        ]
    },
    "types": "types/index.d.ts",
    "version": "2.6.2"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
