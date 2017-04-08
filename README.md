# api documentation for  [mqtt (v2.6.0)](https://github.com/mqttjs/MQTT.js#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-mqtt.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-mqtt) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-mqtt.svg)](https://travis-ci.org/npmdoc/node-npmdoc-mqtt)
#### A library for the MQTT protocol

[![NPM](https://nodei.co/npm/mqtt.png?downloads=true)](https://www.npmjs.com/package/mqtt)

[![apidoc](https://npmdoc.github.io/node-npmdoc-mqtt/build/screenCapture.buildNpmdoc.browser.%252Fhome%252Ftravis%252Fbuild%252Fnpmdoc%252Fnode-npmdoc-mqtt%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-mqtt/build/apidoc.html)

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
            "name": "Adam Rudd",
            "email": "adamvrr@gmail.com"
        },
        {
            "name": "Matteo Collina",
            "email": "matteo.collina@gmail.com",
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
        "readable-stream": "^2.2.3",
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
        "snazzy": "^6.0.0",
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
        "shasum": "381fcf76c2110f0b5d32967862fe6347a255f36d",
        "tarball": "https://registry.npmjs.org/mqtt/-/mqtt-2.6.0.tgz"
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
    "gitHead": "f55a8e90ae2a03650597f4352652de1266fd24ec",
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
            "name": "adamvr",
            "email": "adam.rudd@uqconnect.edu.au"
        },
        {
            "name": "matteo.collina",
            "email": "hello@matteocollina.com"
        }
    ],
    "name": "mqtt",
    "optionalDependencies": {},
    "pre-commit": [
        "test"
    ],
    "readme": "ERROR: No README data found!",
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
    "version": "2.6.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module mqtt](#apidoc.module.mqtt)
1.  [function <span class="apidocSignatureSpan">mqtt.</span>Client (streamBuilder, options)](#apidoc.element.mqtt.Client)
1.  [function <span class="apidocSignatureSpan">mqtt.</span>MqttClient (streamBuilder, options)](#apidoc.element.mqtt.MqttClient)
1.  [function <span class="apidocSignatureSpan">mqtt.</span>Store ()](#apidoc.element.mqtt.Store)
1.  [function <span class="apidocSignatureSpan">mqtt.</span>connect (brokerUrl, opts)](#apidoc.element.mqtt.connect)
1.  object <span class="apidocSignatureSpan">mqtt.</span>MqttClient.prototype
1.  object <span class="apidocSignatureSpan">mqtt.</span>Store.prototype
1.  object <span class="apidocSignatureSpan">mqtt.</span>validations

#### [module mqtt.MqttClient](#apidoc.module.mqtt.MqttClient)
1.  [function <span class="apidocSignatureSpan">mqtt.</span>MqttClient (streamBuilder, options)](#apidoc.element.mqtt.MqttClient.MqttClient)
1.  [function <span class="apidocSignatureSpan">mqtt.MqttClient.</span>super_ ()](#apidoc.element.mqtt.MqttClient.super_)

#### [module mqtt.MqttClient.prototype](#apidoc.module.mqtt.MqttClient.prototype)
1.  [function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_checkDisconnecting (callback)](#apidoc.element.mqtt.MqttClient.prototype._checkDisconnecting)
1.  [function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_checkPing ()](#apidoc.element.mqtt.MqttClient.prototype._checkPing)
1.  [function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_cleanUp (forced, done)](#apidoc.element.mqtt.MqttClient.prototype._cleanUp)
1.  [function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_clearReconnect ()](#apidoc.element.mqtt.MqttClient.prototype._clearReconnect)
1.  [function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_handleAck (packet)](#apidoc.element.mqtt.MqttClient.prototype._handleAck)
1.  [function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_handleConnack (packet)](#apidoc.element.mqtt.MqttClient.prototype._handleConnack)
1.  [function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_handlePacket (packet, done)](#apidoc.element.mqtt.MqttClient.prototype._handlePacket)
1.  [function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_handlePingresp ()](#apidoc.element.mqtt.MqttClient.prototype._handlePingresp)
1.  [function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_handlePublish (packet, done)](#apidoc.element.mqtt.MqttClient.prototype._handlePublish)
1.  [function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_handlePubrel (packet, callback)](#apidoc.element.mqtt.MqttClient.prototype._handlePubrel)
1.  [function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_nextId ()](#apidoc.element.mqtt.MqttClient.prototype._nextId)
1.  [function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_reconnect ()](#apidoc.element.mqtt.MqttClient.prototype._reconnect)
1.  [function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_sendPacket (packet, cb)](#apidoc.element.mqtt.MqttClient.prototype._sendPacket)
1.  [function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_setupPingTimer ()](#apidoc.element.mqtt.MqttClient.prototype._setupPingTimer)
1.  [function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_setupReconnect ()](#apidoc.element.mqtt.MqttClient.prototype._setupReconnect)
1.  [function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_setupStream ()](#apidoc.element.mqtt.MqttClient.prototype._setupStream)
1.  [function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_shiftPingInterval ()](#apidoc.element.mqtt.MqttClient.prototype._shiftPingInterval)
1.  [function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>end (force, cb)](#apidoc.element.mqtt.MqttClient.prototype.end)
1.  [function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>getLastMessageId ()](#apidoc.element.mqtt.MqttClient.prototype.getLastMessageId)
1.  [function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>handleMessage (packet, callback)](#apidoc.element.mqtt.MqttClient.prototype.handleMessage)
1.  [function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>publish (topic, message, opts, callback)](#apidoc.element.mqtt.MqttClient.prototype.publish)
1.  [function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>subscribe ()](#apidoc.element.mqtt.MqttClient.prototype.subscribe)
1.  [function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>unsubscribe (topic, callback)](#apidoc.element.mqtt.MqttClient.prototype.unsubscribe)

#### [module mqtt.Store](#apidoc.module.mqtt.Store)
1.  [function <span class="apidocSignatureSpan">mqtt.</span>Store ()](#apidoc.element.mqtt.Store.Store)

#### [module mqtt.Store.prototype](#apidoc.module.mqtt.Store.prototype)
1.  [function <span class="apidocSignatureSpan">mqtt.Store.prototype.</span>close (cb)](#apidoc.element.mqtt.Store.prototype.close)
1.  [function <span class="apidocSignatureSpan">mqtt.Store.prototype.</span>createStream ()](#apidoc.element.mqtt.Store.prototype.createStream)
1.  [function <span class="apidocSignatureSpan">mqtt.Store.prototype.</span>del (packet, cb)](#apidoc.element.mqtt.Store.prototype.del)
1.  [function <span class="apidocSignatureSpan">mqtt.Store.prototype.</span>get (packet, cb)](#apidoc.element.mqtt.Store.prototype.get)
1.  [function <span class="apidocSignatureSpan">mqtt.Store.prototype.</span>put (packet, cb)](#apidoc.element.mqtt.Store.prototype.put)

#### [module mqtt.connect](#apidoc.module.mqtt.connect)
1.  [function <span class="apidocSignatureSpan">mqtt.</span>connect (brokerUrl, opts)](#apidoc.element.mqtt.connect.connect)
1.  [function <span class="apidocSignatureSpan">mqtt.connect.</span>MqttClient (streamBuilder, options)](#apidoc.element.mqtt.connect.MqttClient)

#### [module mqtt.validations](#apidoc.module.mqtt.validations)
1.  [function <span class="apidocSignatureSpan">mqtt.validations.</span>validateTopics (topics)](#apidoc.element.mqtt.validations.validateTopics)



# <a name="apidoc.module.mqtt"></a>[module mqtt](#apidoc.module.mqtt)

#### <a name="apidoc.element.mqtt.Client"></a>[function <span class="apidocSignatureSpan">mqtt.</span>Client (streamBuilder, options)](#apidoc.element.mqtt.Client)
- description and source-code
```javascript
function MqttClient(streamBuilder, options) {
  var k
  var that = this

  if (!(this instanceof MqttClient)) {
    return new MqttClient(streamBuilder, options)
  }

  this.options = options || {}

  // Defaults
  for (k in defaultConnectOptions) {
    if (typeof this.options[k] === 'undefined') {
      this.options[k] = defaultConnectOptions[k]
    } else {
      this.options[k] = options[k]
    }
  }

  this.options.clientId = this.options.clientId || defaultId()

  this.streamBuilder = streamBuilder

  // Inflight message storages
  this.outgoingStore = this.options.outgoingStore || new Store()
  this.incomingStore = this.options.incomingStore || new Store()

  // Should QoS zero messages be queued when the connection is broken?
  this.queueQoSZero = this.options.queueQoSZero === undefined ? true : this.options.queueQoSZero

  // map of subscribed topics to support reconnection
  this._resubscribeTopics = {}

  // Ping timer, setup in _setupPingTimer
  this.pingTimer = null
  // Is the client connected?
  this.connected = false
  // Are we disconnecting?
  this.disconnecting = false
  // Packet queue
  this.queue = []
  // connack timer
  this.connackTimer = null
  // Reconnect timer
  this.reconnectTimer = null
  // MessageIDs starting with 1
  this.nextId = Math.floor(Math.random() * 65535)

  // Inflight callbacks
  this.outgoing = {}

  // Mark connected on connect
  this.on('connect', function () {
    if (this.disconnected) {
      return
    }

    this.connected = true
    var outStore = null
    outStore = this.outgoingStore.createStream()

    // Control of stored messages
    outStore.once('readable', function () {
      function storeDeliver () {
        var packet = outStore.read(1)
        var cb

        if (!packet) {
          return
        }

        // Avoid unnecesary stream read operations when disconnected
        if (!that.disconnecting && !that.reconnectTimer && that.options.reconnectPeriod > 0) {
          outStore.read(0)
          cb = that.outgoing[packet.messageId]
          that.outgoing[packet.messageId] = function (err, status) {
            // Ensure that the original callback passed in to publish gets invoked
            if (cb) {
              cb(err, status)
            }

            storeDeliver()
          }
          that._sendPacket(packet)
        } else if (outStore.destroy) {
          outStore.destroy()
        }
      }
      storeDeliver()
    })
    .on('error', this.emit.bind(this, 'error'))
  })

  // Mark disconnected on stream close
  this.on('close', function () {
    this.connected = false
    clearTimeout(this.connackTimer)
  })

  // Setup ping timer
  this.on('connect', this._setupPingTimer)

  // Send queued packets
  this.on('connect', function () {
    var queue = this.queue

    function deliver () {
      var entry = queue.shift()
      var packet = null

      if (!entry) {
        return
      }

      packet = entry.packet

      that._sendPacket(
        packet,
        function (err) {
          if (entry.cb) {
            entry.cb(err)
          }
          deliver()
        }
      )
    }

    deliver()
  })

  // resubscribe
  this.on('reconnect', function () {
    if (this.options.clean && Object.keys(this._resubscribeTopics).length > 0) {
      this.subscribe(this._resubscribeTopics)
    }
  })

  // Clear ping timer
  this.on('close', function () {
    if (that.pingTimer !== null) {
      that.pingTimer.clear()
      that.pingTimer = null
    }
  })

  // Setup reconnect timer on disconnect
  this.on('close', this._setupReconnect)

  events.EventEmitter.call(this)

  this._setupStream()
}
```
- example usage
```shell
...
at every connect.

For all MQTT-related options, see the [Client](#client)
constructor.

-------------------------------------------------------
<a name="client"></a>
### mqtt.Client(streamBuilder, options)

The 'Client' class wraps a client connection to an
MQTT broker over an arbitrary transport method (TCP, TLS,
WebSocket, ecc).

'Client' automatically handles the following:
...
```

#### <a name="apidoc.element.mqtt.MqttClient"></a>[function <span class="apidocSignatureSpan">mqtt.</span>MqttClient (streamBuilder, options)](#apidoc.element.mqtt.MqttClient)
- description and source-code
```javascript
function MqttClient(streamBuilder, options) {
  var k
  var that = this

  if (!(this instanceof MqttClient)) {
    return new MqttClient(streamBuilder, options)
  }

  this.options = options || {}

  // Defaults
  for (k in defaultConnectOptions) {
    if (typeof this.options[k] === 'undefined') {
      this.options[k] = defaultConnectOptions[k]
    } else {
      this.options[k] = options[k]
    }
  }

  this.options.clientId = this.options.clientId || defaultId()

  this.streamBuilder = streamBuilder

  // Inflight message storages
  this.outgoingStore = this.options.outgoingStore || new Store()
  this.incomingStore = this.options.incomingStore || new Store()

  // Should QoS zero messages be queued when the connection is broken?
  this.queueQoSZero = this.options.queueQoSZero === undefined ? true : this.options.queueQoSZero

  // map of subscribed topics to support reconnection
  this._resubscribeTopics = {}

  // Ping timer, setup in _setupPingTimer
  this.pingTimer = null
  // Is the client connected?
  this.connected = false
  // Are we disconnecting?
  this.disconnecting = false
  // Packet queue
  this.queue = []
  // connack timer
  this.connackTimer = null
  // Reconnect timer
  this.reconnectTimer = null
  // MessageIDs starting with 1
  this.nextId = Math.floor(Math.random() * 65535)

  // Inflight callbacks
  this.outgoing = {}

  // Mark connected on connect
  this.on('connect', function () {
    if (this.disconnected) {
      return
    }

    this.connected = true
    var outStore = null
    outStore = this.outgoingStore.createStream()

    // Control of stored messages
    outStore.once('readable', function () {
      function storeDeliver () {
        var packet = outStore.read(1)
        var cb

        if (!packet) {
          return
        }

        // Avoid unnecesary stream read operations when disconnected
        if (!that.disconnecting && !that.reconnectTimer && that.options.reconnectPeriod > 0) {
          outStore.read(0)
          cb = that.outgoing[packet.messageId]
          that.outgoing[packet.messageId] = function (err, status) {
            // Ensure that the original callback passed in to publish gets invoked
            if (cb) {
              cb(err, status)
            }

            storeDeliver()
          }
          that._sendPacket(packet)
        } else if (outStore.destroy) {
          outStore.destroy()
        }
      }
      storeDeliver()
    })
    .on('error', this.emit.bind(this, 'error'))
  })

  // Mark disconnected on stream close
  this.on('close', function () {
    this.connected = false
    clearTimeout(this.connackTimer)
  })

  // Setup ping timer
  this.on('connect', this._setupPingTimer)

  // Send queued packets
  this.on('connect', function () {
    var queue = this.queue

    function deliver () {
      var entry = queue.shift()
      var packet = null

      if (!entry) {
        return
      }

      packet = entry.packet

      that._sendPacket(
        packet,
        function (err) {
          if (entry.cb) {
            entry.cb(err)
          }
          deliver()
        }
      )
    }

    deliver()
  })

  // resubscribe
  this.on('reconnect', function () {
    if (this.options.clean && Object.keys(this._resubscribeTopics).length > 0) {
      this.subscribe(this._resubscribeTopics)
    }
  })

  // Clear ping timer
  this.on('close', function () {
    if (that.pingTimer !== null) {
      that.pingTimer.clear()
      that.pingTimer = null
    }
  })

  // Setup reconnect timer on disconnect
  this.on('close', this._setupReconnect)

  events.EventEmitter.call(this)

  this._setupStream()
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mqtt.Store"></a>[function <span class="apidocSignatureSpan">mqtt.</span>Store ()](#apidoc.element.mqtt.Store)
- description and source-code
```javascript
function Store() {
  if (!(this instanceof Store)) {
    return new Store()
  }

  this._inflights = {}
}
```
- example usage
```shell
...
<a name="reconnecting"></a>
### mqtt.Client#reconnecting

Boolean : set to 'true' if the client is trying to reconnect to the server. 'false' otherwise.

-------------------------------------------------------
<a name="store"></a>
### mqtt.Store()

In-memory implementation of the message store.

Another implementaion is
[mqtt-level-store](http://npm.im/mqtt-level-store) which uses
[Level-browserify](http://npm.im/level-browserify) to store the inflight
data, making it usable both in Node and the Browser.
...
```

#### <a name="apidoc.element.mqtt.connect"></a>[function <span class="apidocSignatureSpan">mqtt.</span>connect (brokerUrl, opts)](#apidoc.element.mqtt.connect)
- description and source-code
```javascript
function connect(brokerUrl, opts) {
  if ((typeof brokerUrl === 'object') && !opts) {
    opts = brokerUrl
    brokerUrl = null
  }

  opts = opts || {}

  if (brokerUrl) {
    var parsed = url.parse(brokerUrl, true)
    if (parsed.port != null) {
      parsed.port = Number(parsed.port)
    }

    opts = xtend(parsed, opts)

    if (opts.protocol === null) {
      throw new Error('Missing protocol')
    }
    opts.protocol = opts.protocol.replace(/:$/, '')
  }

  // merge in the auth options if supplied
  parseAuthOptions(opts)

  // support clientId passed in the query string of the url
  if (opts.query && typeof opts.query.clientId === 'string') {
    opts.clientId = opts.query.clientId
  }

  if (opts.cert && opts.key) {
    if (opts.protocol) {
      if (['mqtts', 'wss'].indexOf(opts.protocol) === -1) {
<span class="apidocCodeCommentSpan">        /*
         * jshint and eslint
         * complains that break from default cannot be reached after throw
         * it is a foced exit from a control structure
         * maybe add a check after switch to see if it went through default
         * and then throw the error
        */
</span>        /* jshint -W027 */
        /* eslint no-unreachable:1 */
        switch (opts.protocol) {
          case 'mqtt':
            opts.protocol = 'mqtts'
            break
          case 'ws':
            opts.protocol = 'wss'
            break
          default:
            throw new Error('Unknown protocol for secure connection: "' + opts.protocol + '"!')
            break
        }
        /* eslint no-unreachable:0 */
        /* jshint +W027 */
      }
    } else {
      // don't know what protocol he want to use, mqtts or wss
      throw new Error('Missing secure protocol key')
    }
  }

  if (!protocols[opts.protocol]) {
    var isSecure = ['mqtts', 'wss'].indexOf(opts.protocol) !== -1
    opts.protocol = [
      'mqtt',
      'mqtts',
      'ws',
      'wss'
    ].filter(function (key, index) {
      if (isSecure && index % 2 === 0) {
        // Skip insecure protocols when requesting a secure one.
        return false
      }
      return (typeof protocols[key] === 'function')
    })[0]
  }

  if (opts.clean === false && !opts.clientId) {
    throw new Error('Missing clientId for unclean clients')
  }

  function wrapper (client) {
    if (opts.servers) {
      if (!client._reconnectCount || client._reconnectCount === opts.servers.length) {
        client._reconnectCount = 0
      }

      opts.host = opts.servers[client._reconnectCount].host
      opts.port = opts.servers[client._reconnectCount].port
      opts.hostname = opts.host

      client._reconnectCount++
    }

    return protocols[opts.protocol](client, opts)
  }

  return new MqttClient(wrapper, opts)
}
```
- example usage
```shell
...
<a name="example"></a>
## Example

For the sake of simplicity, let's put the subscriber and the publisher in the same file:

'''js
var mqtt = require('mqtt')
var client  = mqtt.connect('mqtt://test.mosquitto.org')

client.on('connect', function () {
  client.subscribe('presence')
  client.publish('presence', 'Hello mqtt')
})

client.on('message', function (topic, message) {
...
```



# <a name="apidoc.module.mqtt.MqttClient"></a>[module mqtt.MqttClient](#apidoc.module.mqtt.MqttClient)

#### <a name="apidoc.element.mqtt.MqttClient.MqttClient"></a>[function <span class="apidocSignatureSpan">mqtt.</span>MqttClient (streamBuilder, options)](#apidoc.element.mqtt.MqttClient.MqttClient)
- description and source-code
```javascript
function MqttClient(streamBuilder, options) {
  var k
  var that = this

  if (!(this instanceof MqttClient)) {
    return new MqttClient(streamBuilder, options)
  }

  this.options = options || {}

  // Defaults
  for (k in defaultConnectOptions) {
    if (typeof this.options[k] === 'undefined') {
      this.options[k] = defaultConnectOptions[k]
    } else {
      this.options[k] = options[k]
    }
  }

  this.options.clientId = this.options.clientId || defaultId()

  this.streamBuilder = streamBuilder

  // Inflight message storages
  this.outgoingStore = this.options.outgoingStore || new Store()
  this.incomingStore = this.options.incomingStore || new Store()

  // Should QoS zero messages be queued when the connection is broken?
  this.queueQoSZero = this.options.queueQoSZero === undefined ? true : this.options.queueQoSZero

  // map of subscribed topics to support reconnection
  this._resubscribeTopics = {}

  // Ping timer, setup in _setupPingTimer
  this.pingTimer = null
  // Is the client connected?
  this.connected = false
  // Are we disconnecting?
  this.disconnecting = false
  // Packet queue
  this.queue = []
  // connack timer
  this.connackTimer = null
  // Reconnect timer
  this.reconnectTimer = null
  // MessageIDs starting with 1
  this.nextId = Math.floor(Math.random() * 65535)

  // Inflight callbacks
  this.outgoing = {}

  // Mark connected on connect
  this.on('connect', function () {
    if (this.disconnected) {
      return
    }

    this.connected = true
    var outStore = null
    outStore = this.outgoingStore.createStream()

    // Control of stored messages
    outStore.once('readable', function () {
      function storeDeliver () {
        var packet = outStore.read(1)
        var cb

        if (!packet) {
          return
        }

        // Avoid unnecesary stream read operations when disconnected
        if (!that.disconnecting && !that.reconnectTimer && that.options.reconnectPeriod > 0) {
          outStore.read(0)
          cb = that.outgoing[packet.messageId]
          that.outgoing[packet.messageId] = function (err, status) {
            // Ensure that the original callback passed in to publish gets invoked
            if (cb) {
              cb(err, status)
            }

            storeDeliver()
          }
          that._sendPacket(packet)
        } else if (outStore.destroy) {
          outStore.destroy()
        }
      }
      storeDeliver()
    })
    .on('error', this.emit.bind(this, 'error'))
  })

  // Mark disconnected on stream close
  this.on('close', function () {
    this.connected = false
    clearTimeout(this.connackTimer)
  })

  // Setup ping timer
  this.on('connect', this._setupPingTimer)

  // Send queued packets
  this.on('connect', function () {
    var queue = this.queue

    function deliver () {
      var entry = queue.shift()
      var packet = null

      if (!entry) {
        return
      }

      packet = entry.packet

      that._sendPacket(
        packet,
        function (err) {
          if (entry.cb) {
            entry.cb(err)
          }
          deliver()
        }
      )
    }

    deliver()
  })

  // resubscribe
  this.on('reconnect', function () {
    if (this.options.clean && Object.keys(this._resubscribeTopics).length > 0) {
      this.subscribe(this._resubscribeTopics)
    }
  })

  // Clear ping timer
  this.on('close', function () {
    if (that.pingTimer !== null) {
      that.pingTimer.clear()
      that.pingTimer = null
    }
  })

  // Setup reconnect timer on disconnect
  this.on('close', this._setupReconnect)

  events.EventEmitter.call(this)

  this._setupStream()
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mqtt.MqttClient.super_"></a>[function <span class="apidocSignatureSpan">mqtt.MqttClient.</span>super_ ()](#apidoc.element.mqtt.MqttClient.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mqtt.MqttClient.prototype"></a>[module mqtt.MqttClient.prototype](#apidoc.module.mqtt.MqttClient.prototype)

#### <a name="apidoc.element.mqtt.MqttClient.prototype._checkDisconnecting"></a>[function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_checkDisconnecting (callback)](#apidoc.element.mqtt.MqttClient.prototype._checkDisconnecting)
- description and source-code
```javascript
_checkDisconnecting = function (callback) {
  if (this.disconnecting) {
    if (callback) {
      callback(new Error('client disconnecting'))
    } else {
      this.emit('error', new Error('client disconnecting'))
    }
  }
  return this.disconnecting
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mqtt.MqttClient.prototype._checkPing"></a>[function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_checkPing ()](#apidoc.element.mqtt.MqttClient.prototype._checkPing)
- description and source-code
```javascript
_checkPing = function () {
  if (this.pingResp) {
    this.pingResp = false
    this._sendPacket({ cmd: 'pingreq' })
  } else {
    // do a forced cleanup since socket will be in bad shape
    this._cleanUp(true)
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mqtt.MqttClient.prototype._cleanUp"></a>[function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_cleanUp (forced, done)](#apidoc.element.mqtt.MqttClient.prototype._cleanUp)
- description and source-code
```javascript
_cleanUp = function (forced, done) {
  if (done) {
    this.stream.on('close', done)
  }

  if (forced) {
    this.stream.destroy()
  } else {
    this._sendPacket(
      { cmd: 'disconnect' },
      setImmediate.bind(
        null,
        this.stream.end.bind(this.stream)
      )
    )
  }

  if (!this.disconnecting) {
    this._clearReconnect()
    this._setupReconnect()
  }

  if (this.pingTimer !== null) {
    this.pingTimer.clear()
    this.pingTimer = null
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mqtt.MqttClient.prototype._clearReconnect"></a>[function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_clearReconnect ()](#apidoc.element.mqtt.MqttClient.prototype._clearReconnect)
- description and source-code
```javascript
_clearReconnect = function () {
  if (this.reconnectTimer) {
    clearInterval(this.reconnectTimer)
    this.reconnectTimer = null
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mqtt.MqttClient.prototype._handleAck"></a>[function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_handleAck (packet)](#apidoc.element.mqtt.MqttClient.prototype._handleAck)
- description and source-code
```javascript
_handleAck = function (packet) {
<span class="apidocCodeCommentSpan">  /* eslint no-fallthrough: "off" */
</span>  var mid = packet.messageId
  var type = packet.cmd
  var response = null
  var cb = this.outgoing[mid]
  var that = this

  if (!cb) {
    // Server sent an ack in error, ignore it.
    return
  }

  // Process
  switch (type) {
    case 'pubcomp':
      // same thing as puback for QoS 2
    case 'puback':
      // Callback - we're done
      delete this.outgoing[mid]
      this.outgoingStore.del(packet, cb)
      break
    case 'pubrec':
      response = {
        cmd: 'pubrel',
        qos: 2,
        messageId: mid
      }

      this._sendPacket(response)
      break
    case 'suback':
      delete this.outgoing[mid]
      cb(null, packet)
      break
    case 'unsuback':
      delete this.outgoing[mid]
      cb(null)
      break
    default:
      that.emit('error', new Error('unrecognized packet type'))
  }

  if (this.disconnecting &&
      Object.keys(this.outgoing).length === 0) {
    this.emit('outgoingEmpty')
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mqtt.MqttClient.prototype._handleConnack"></a>[function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_handleConnack (packet)](#apidoc.element.mqtt.MqttClient.prototype._handleConnack)
- description and source-code
```javascript
_handleConnack = function (packet) {
  var rc = packet.returnCode
  var errors = [
    '',
    'Unacceptable protocol version',
    'Identifier rejected',
    'Server unavailable',
    'Bad username or password',
    'Not authorized'
  ]

  clearTimeout(this.connackTimer)

  if (rc === 0) {
    this.reconnecting = false
    this.emit('connect', packet)
  } else if (rc > 0) {
    this.emit('error', new Error('Connection refused: ' + errors[rc]))
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mqtt.MqttClient.prototype._handlePacket"></a>[function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_handlePacket (packet, done)](#apidoc.element.mqtt.MqttClient.prototype._handlePacket)
- description and source-code
```javascript
_handlePacket = function (packet, done) {
  this.emit('packetreceive', packet)

  switch (packet.cmd) {
    case 'publish':
      this._handlePublish(packet, done)
      break
    case 'puback':
    case 'pubrec':
    case 'pubcomp':
    case 'suback':
    case 'unsuback':
      this._handleAck(packet)
      done()
      break
    case 'pubrel':
      this._handlePubrel(packet, done)
      break
    case 'connack':
      this._handleConnack(packet)
      done()
      break
    case 'pingresp':
      this._handlePingresp(packet)
      done()
      break
    default:
      // do nothing
      // maybe we should do an error handling
      // or just log it
      break
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mqtt.MqttClient.prototype._handlePingresp"></a>[function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_handlePingresp ()](#apidoc.element.mqtt.MqttClient.prototype._handlePingresp)
- description and source-code
```javascript
_handlePingresp = function () {
  this.pingResp = true
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mqtt.MqttClient.prototype._handlePublish"></a>[function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_handlePublish (packet, done)](#apidoc.element.mqtt.MqttClient.prototype._handlePublish)
- description and source-code
```javascript
_handlePublish = function (packet, done) {
  var topic = packet.topic.toString()
  var message = packet.payload
  var qos = packet.qos
  var mid = packet.messageId
  var that = this

  switch (qos) {
    case 2:
      this.incomingStore.put(packet, function () {
        that._sendPacket({cmd: 'pubrec', messageId: mid}, done)
      })
      break
    case 1:
      // do not wait sending a puback
      // no callback passed
      this._sendPacket({
        cmd: 'puback',
        messageId: mid
      })
<span class="apidocCodeCommentSpan">      /* falls through */
</span>    case 0:
      // emit the message event for both qos 1 and 0
      this.emit('message', topic, message, packet)
      this.handleMessage(packet, done)
      break
    default:
      // do nothing
      // log or throw an error about unknown qos
      break
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mqtt.MqttClient.prototype._handlePubrel"></a>[function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_handlePubrel (packet, callback)](#apidoc.element.mqtt.MqttClient.prototype._handlePubrel)
- description and source-code
```javascript
_handlePubrel = function (packet, callback) {
  var mid = packet.messageId
  var that = this

  that.incomingStore.get(packet, function (err, pub) {
    if (err) {
      return that.emit('error', err)
    }

    if (pub.cmd !== 'pubrel') {
      that.emit('message', pub.topic, pub.payload, pub)
      that.incomingStore.put(packet)
    }

    that._sendPacket({cmd: 'pubcomp', messageId: mid}, callback)
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mqtt.MqttClient.prototype._nextId"></a>[function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_nextId ()](#apidoc.element.mqtt.MqttClient.prototype._nextId)
- description and source-code
```javascript
_nextId = function () {
  var id = this.nextId++
  // Ensure 16 bit unsigned int:
  if (id === 65535) {
    this.nextId = 1
  }
  return id
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mqtt.MqttClient.prototype._reconnect"></a>[function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_reconnect ()](#apidoc.element.mqtt.MqttClient.prototype._reconnect)
- description and source-code
```javascript
_reconnect = function () {
  this.emit('reconnect')
  this._setupStream()
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mqtt.MqttClient.prototype._sendPacket"></a>[function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_sendPacket (packet, cb)](#apidoc.element.mqtt.MqttClient.prototype._sendPacket)
- description and source-code
```javascript
_sendPacket = function (packet, cb) {
  if (!this.connected) {
    if (packet.qos > 0 || packet.cmd !== 'publish' || this.queueQoSZero) {
      this.queue.push({ packet: packet, cb: cb })
    } else if (cb) {
      cb(new Error('No connection to broker'))
    }

    return
  }

  // When sending a packet, reschedule the ping timer
  this._shiftPingInterval()

  if (packet.cmd !== 'publish') {
    sendPacket(this, packet, cb)
    return
  }

  switch (packet.qos) {
    case 2:
    case 1:
      storeAndSend(this, packet, cb)
      break
<span class="apidocCodeCommentSpan">    /**
     * no need of case here since it will be caught by default
     * and jshint comply that before default it must be a break
     * anyway it will result in -1 evaluation
     */
</span>    case 0:
      /* falls through */
    default:
      sendPacket(this, packet, cb)
      break
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mqtt.MqttClient.prototype._setupPingTimer"></a>[function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_setupPingTimer ()](#apidoc.element.mqtt.MqttClient.prototype._setupPingTimer)
- description and source-code
```javascript
_setupPingTimer = function () {
  var that = this

  if (!this.pingTimer && this.options.keepalive) {
    this.pingResp = true
    this.pingTimer = reInterval(function () {
      that._checkPing()
    }, this.options.keepalive * 1000)
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mqtt.MqttClient.prototype._setupReconnect"></a>[function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_setupReconnect ()](#apidoc.element.mqtt.MqttClient.prototype._setupReconnect)
- description and source-code
```javascript
_setupReconnect = function () {
  var that = this

  if (!that.disconnecting && !that.reconnectTimer && (that.options.reconnectPeriod > 0)) {
    if (!this.reconnecting) {
      this.emit('offline')
      this.reconnecting = true
    }
    that.reconnectTimer = setInterval(function () {
      that._reconnect()
    }, that.options.reconnectPeriod)
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mqtt.MqttClient.prototype._setupStream"></a>[function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_setupStream ()](#apidoc.element.mqtt.MqttClient.prototype._setupStream)
- description and source-code
```javascript
_setupStream = function () {
  var connectPacket
  var that = this
  var writable = new Writable()
  var parser = mqttPacket.parser(this.options)
  var completeParse = null
  var packets = []

  this._clearReconnect()

  this.stream = this.streamBuilder(this)

  parser.on('packet', function (packet) {
    packets.push(packet)
  })

  function process () {
    var packet = packets.shift()
    var done = completeParse

    if (packet) {
      that._handlePacket(packet, process)
    } else {
      completeParse = null
      done()
    }
  }

  writable._write = function (buf, enc, done) {
    completeParse = done
    parser.parse(buf)
    process()
  }

  this.stream.pipe(writable)

  // Suppress connection errors
  this.stream.on('error', nop)

  // Echo stream close
  eos(this.stream, this.emit.bind(this, 'close'))

  // Send a connect packet
  connectPacket = Object.create(this.options)
  connectPacket.cmd = 'connect'
  // avoid message queue
  sendPacket(this, connectPacket)

  // Echo connection errors
  parser.on('error', this.emit.bind(this, 'error'))

  // many drain listeners are needed for qos 1 callbacks if the connection is intermittent
  this.stream.setMaxListeners(1000)

  clearTimeout(this.connackTimer)
  this.connackTimer = setTimeout(function () {
    that._cleanUp(true)
  }, this.options.connectTimeout)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mqtt.MqttClient.prototype._shiftPingInterval"></a>[function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>_shiftPingInterval ()](#apidoc.element.mqtt.MqttClient.prototype._shiftPingInterval)
- description and source-code
```javascript
_shiftPingInterval = function () {
  if (this.pingTimer && this.options.keepalive && this.options.reschedulePings) {
    this.pingTimer.reschedule(this.options.keepalive * 1000)
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mqtt.MqttClient.prototype.end"></a>[function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>end (force, cb)](#apidoc.element.mqtt.MqttClient.prototype.end)
- description and source-code
```javascript
end = function (force, cb) {
  var that = this

  if (typeof force === 'function') {
    cb = force
    force = false
  }

  function closeStores () {
    that.disconnected = true
    that.incomingStore.close(function () {
      that.outgoingStore.close(cb)
    })
  }

  function finish () {
    // defer closesStores of an I/O cycle,
    // just to make sure things are
    // ok for websockets
    that._cleanUp(force, setImmediate.bind(null, closeStores))
  }

  if (this.disconnecting) {
    return this
  }

  this._clearReconnect()

  this.disconnecting = true

  if (!force && Object.keys(this.outgoing).length > 0) {
    // wait 10ms, just to be sure we received all of it
    this.once('outgoingEmpty', setTimeout.bind(null, finish, 10))
  } else {
    finish()
  }

  return this
}
```
- example usage
```shell
...
  client.subscribe('presence')
  client.publish('presence', 'Hello mqtt')
})

client.on('message', function (topic, message) {
  // message is Buffer
  console.log(message.toString())
  client.end()
})
'''

output:
'''
Hello mqtt
'''
...
```

#### <a name="apidoc.element.mqtt.MqttClient.prototype.getLastMessageId"></a>[function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>getLastMessageId ()](#apidoc.element.mqtt.MqttClient.prototype.getLastMessageId)
- description and source-code
```javascript
getLastMessageId = function () {
  return (this.nextId === 1) ? 65535 : (this.nextId - 1)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mqtt.MqttClient.prototype.handleMessage"></a>[function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>handleMessage (packet, callback)](#apidoc.element.mqtt.MqttClient.prototype.handleMessage)
- description and source-code
```javascript
handleMessage = function (packet, callback) {
  callback()
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mqtt.MqttClient.prototype.publish"></a>[function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>publish (topic, message, opts, callback)](#apidoc.element.mqtt.MqttClient.prototype.publish)
- description and source-code
```javascript
publish = function (topic, message, opts, callback) {
  var packet

  // .publish(topic, payload, cb);
  if (typeof opts === 'function') {
    callback = opts
    opts = null
  }

  // Default opts
  if (!opts) {
    opts = {qos: 0, retain: false}
  }

  if (this._checkDisconnecting(callback)) {
    return this
  }

  packet = {
    cmd: 'publish',
    topic: topic,
    payload: message,
    qos: opts.qos,
    retain: opts.retain,
    messageId: this._nextId()
  }

  switch (opts.qos) {
    case 1:
    case 2:

      // Add to callbacks
      this.outgoing[packet.messageId] = callback || nop
      this._sendPacket(packet)
      break
    default:
      this._sendPacket(packet, callback)
      break
  }

  return this
}
```
- example usage
```shell
...

'''js
var mqtt = require('mqtt')
var client  = mqtt.connect('mqtt://test.mosquitto.org')

client.on('connect', function () {
  client.subscribe('presence')
  client.publish('presence', 'Hello mqtt')
})

client.on('message', function (topic, message) {
  // message is Buffer
  console.log(message.toString())
  client.end()
})
...
```

#### <a name="apidoc.element.mqtt.MqttClient.prototype.subscribe"></a>[function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>subscribe ()](#apidoc.element.mqtt.MqttClient.prototype.subscribe)
- description and source-code
```javascript
subscribe = function () {
  var packet
  var args = Array.prototype.slice.call(arguments)
  var subs = []
  var obj = args.shift()
  var callback = args.pop() || nop
  var opts = args.pop()
  var invalidTopic
  var that = this

  if (typeof obj === 'string') {
    obj = [obj]
  }

  if (typeof callback !== 'function') {
    opts = callback
    callback = nop
  }

  invalidTopic = validations.validateTopics(obj)
  if (invalidTopic !== null) {
    setImmediate(callback, new Error('Invalid topic ' + invalidTopic))
    return this
  }

  if (this._checkDisconnecting(callback)) {
    return this
  }

  if (!opts) {
    opts = { qos: 0 }
  }

  if (Array.isArray(obj)) {
    obj.forEach(function (topic) {
      subs.push({
        topic: topic,
        qos: opts.qos
      })
    })
  } else {
    Object
      .keys(obj)
      .forEach(function (k) {
        subs.push({
          topic: k,
          qos: obj[k]
        })
      })
  }

  packet = {
    cmd: 'subscribe',
    subscriptions: subs,
    qos: 1,
    retain: false,
    dup: false,
    messageId: this._nextId()
  }

  // subscriptions to resubscribe to in case of disconnect
  subs.forEach(function (sub) {
    that._resubscribeTopics[sub.topic] = sub.qos
  })

  this.outgoing[packet.messageId] = function (err, packet) {
    if (!err) {
      var granted = packet.granted
      for (var i = 0; i < granted.length; i += 1) {
        subs[i].qos = granted[i]
      }
    }

    callback(err, subs)
  }

  this._sendPacket(packet)

  return this
}
```
- example usage
```shell
...
For the sake of simplicity, let's put the subscriber and the publisher in the same file:

'''js
var mqtt = require('mqtt')
var client  = mqtt.connect('mqtt://test.mosquitto.org')

client.on('connect', function () {
client.subscribe('presence')
client.publish('presence', 'Hello mqtt')
})

client.on('message', function (topic, message) {
// message is Buffer
console.log(message.toString())
client.end()
...
```

#### <a name="apidoc.element.mqtt.MqttClient.prototype.unsubscribe"></a>[function <span class="apidocSignatureSpan">mqtt.MqttClient.prototype.</span>unsubscribe (topic, callback)](#apidoc.element.mqtt.MqttClient.prototype.unsubscribe)
- description and source-code
```javascript
unsubscribe = function (topic, callback) {
  var packet = {
    cmd: 'unsubscribe',
    qos: 1,
    messageId: this._nextId()
  }
  var that = this

  callback = callback || nop

  if (this._checkDisconnecting(callback)) {
    return this
  }

  if (typeof topic === 'string') {
    packet.unsubscriptions = [topic]
  } else if (typeof topic === 'object' && topic.length) {
    packet.unsubscriptions = topic
  }

  packet.unsubscriptions.forEach(function (topic) {
    delete that._resubscribeTopics[topic]
  })

  this.outgoing[packet.messageId] = callback

  this._sendPacket(packet)

  return this
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mqtt.Store"></a>[module mqtt.Store](#apidoc.module.mqtt.Store)

#### <a name="apidoc.element.mqtt.Store.Store"></a>[function <span class="apidocSignatureSpan">mqtt.</span>Store ()](#apidoc.element.mqtt.Store.Store)
- description and source-code
```javascript
function Store() {
  if (!(this instanceof Store)) {
    return new Store()
  }

  this._inflights = {}
}
```
- example usage
```shell
...
<a name="reconnecting"></a>
### mqtt.Client#reconnecting

Boolean : set to 'true' if the client is trying to reconnect to the server. 'false' otherwise.

-------------------------------------------------------
<a name="store"></a>
### mqtt.Store()

In-memory implementation of the message store.

Another implementaion is
[mqtt-level-store](http://npm.im/mqtt-level-store) which uses
[Level-browserify](http://npm.im/level-browserify) to store the inflight
data, making it usable both in Node and the Browser.
...
```



# <a name="apidoc.module.mqtt.Store.prototype"></a>[module mqtt.Store.prototype](#apidoc.module.mqtt.Store.prototype)

#### <a name="apidoc.element.mqtt.Store.prototype.close"></a>[function <span class="apidocSignatureSpan">mqtt.Store.prototype.</span>close (cb)](#apidoc.element.mqtt.Store.prototype.close)
- description and source-code
```javascript
close = function (cb) {
  this._inflights = null
  if (cb) {
    cb()
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mqtt.Store.prototype.createStream"></a>[function <span class="apidocSignatureSpan">mqtt.Store.prototype.</span>createStream ()](#apidoc.element.mqtt.Store.prototype.createStream)
- description and source-code
```javascript
createStream = function () {
  var stream = new Readable(streamsOpts)
  var inflights = this._inflights
  var ids = Object.keys(this._inflights)
  var destroyed = false
  var i = 0

  stream._read = function () {
    if (!destroyed && i < ids.length) {
      this.push(inflights[ids[i++]])
    } else {
      this.push(null)
    }
  }

  stream.destroy = function () {
    if (destroyed) {
      return
    }

    var self = this

    destroyed = true

    process.nextTick(function () {
      self.emit('close')
    })
  }

  return stream
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mqtt.Store.prototype.del"></a>[function <span class="apidocSignatureSpan">mqtt.Store.prototype.</span>del (packet, cb)](#apidoc.element.mqtt.Store.prototype.del)
- description and source-code
```javascript
del = function (packet, cb) {
  packet = this._inflights[packet.messageId]
  if (packet) {
    delete this._inflights[packet.messageId]
    cb(null, packet)
  } else if (cb) {
    cb(new Error('missing packet'))
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mqtt.Store.prototype.get"></a>[function <span class="apidocSignatureSpan">mqtt.Store.prototype.</span>get (packet, cb)](#apidoc.element.mqtt.Store.prototype.get)
- description and source-code
```javascript
get = function (packet, cb) {
  packet = this._inflights[packet.messageId]
  if (packet) {
    cb(null, packet)
  } else if (cb) {
    cb(new Error('missing packet'))
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mqtt.Store.prototype.put"></a>[function <span class="apidocSignatureSpan">mqtt.Store.prototype.</span>put (packet, cb)](#apidoc.element.mqtt.Store.prototype.put)
- description and source-code
```javascript
put = function (packet, cb) {
  this._inflights[packet.messageId] = packet

  if (cb) {
    cb()
  }

  return this
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mqtt.connect"></a>[module mqtt.connect](#apidoc.module.mqtt.connect)

#### <a name="apidoc.element.mqtt.connect.connect"></a>[function <span class="apidocSignatureSpan">mqtt.</span>connect (brokerUrl, opts)](#apidoc.element.mqtt.connect.connect)
- description and source-code
```javascript
function connect(brokerUrl, opts) {
  if ((typeof brokerUrl === 'object') && !opts) {
    opts = brokerUrl
    brokerUrl = null
  }

  opts = opts || {}

  if (brokerUrl) {
    var parsed = url.parse(brokerUrl, true)
    if (parsed.port != null) {
      parsed.port = Number(parsed.port)
    }

    opts = xtend(parsed, opts)

    if (opts.protocol === null) {
      throw new Error('Missing protocol')
    }
    opts.protocol = opts.protocol.replace(/:$/, '')
  }

  // merge in the auth options if supplied
  parseAuthOptions(opts)

  // support clientId passed in the query string of the url
  if (opts.query && typeof opts.query.clientId === 'string') {
    opts.clientId = opts.query.clientId
  }

  if (opts.cert && opts.key) {
    if (opts.protocol) {
      if (['mqtts', 'wss'].indexOf(opts.protocol) === -1) {
<span class="apidocCodeCommentSpan">        /*
         * jshint and eslint
         * complains that break from default cannot be reached after throw
         * it is a foced exit from a control structure
         * maybe add a check after switch to see if it went through default
         * and then throw the error
        */
</span>        /* jshint -W027 */
        /* eslint no-unreachable:1 */
        switch (opts.protocol) {
          case 'mqtt':
            opts.protocol = 'mqtts'
            break
          case 'ws':
            opts.protocol = 'wss'
            break
          default:
            throw new Error('Unknown protocol for secure connection: "' + opts.protocol + '"!')
            break
        }
        /* eslint no-unreachable:0 */
        /* jshint +W027 */
      }
    } else {
      // don't know what protocol he want to use, mqtts or wss
      throw new Error('Missing secure protocol key')
    }
  }

  if (!protocols[opts.protocol]) {
    var isSecure = ['mqtts', 'wss'].indexOf(opts.protocol) !== -1
    opts.protocol = [
      'mqtt',
      'mqtts',
      'ws',
      'wss'
    ].filter(function (key, index) {
      if (isSecure && index % 2 === 0) {
        // Skip insecure protocols when requesting a secure one.
        return false
      }
      return (typeof protocols[key] === 'function')
    })[0]
  }

  if (opts.clean === false && !opts.clientId) {
    throw new Error('Missing clientId for unclean clients')
  }

  function wrapper (client) {
    if (opts.servers) {
      if (!client._reconnectCount || client._reconnectCount === opts.servers.length) {
        client._reconnectCount = 0
      }

      opts.host = opts.servers[client._reconnectCount].host
      opts.port = opts.servers[client._reconnectCount].port
      opts.hostname = opts.host

      client._reconnectCount++
    }

    return protocols[opts.protocol](client, opts)
  }

  return new MqttClient(wrapper, opts)
}
```
- example usage
```shell
...
<a name="example"></a>
## Example

For the sake of simplicity, let's put the subscriber and the publisher in the same file:

'''js
var mqtt = require('mqtt')
var client  = mqtt.connect('mqtt://test.mosquitto.org')

client.on('connect', function () {
  client.subscribe('presence')
  client.publish('presence', 'Hello mqtt')
})

client.on('message', function (topic, message) {
...
```

#### <a name="apidoc.element.mqtt.connect.MqttClient"></a>[function <span class="apidocSignatureSpan">mqtt.connect.</span>MqttClient (streamBuilder, options)](#apidoc.element.mqtt.connect.MqttClient)
- description and source-code
```javascript
function MqttClient(streamBuilder, options) {
  var k
  var that = this

  if (!(this instanceof MqttClient)) {
    return new MqttClient(streamBuilder, options)
  }

  this.options = options || {}

  // Defaults
  for (k in defaultConnectOptions) {
    if (typeof this.options[k] === 'undefined') {
      this.options[k] = defaultConnectOptions[k]
    } else {
      this.options[k] = options[k]
    }
  }

  this.options.clientId = this.options.clientId || defaultId()

  this.streamBuilder = streamBuilder

  // Inflight message storages
  this.outgoingStore = this.options.outgoingStore || new Store()
  this.incomingStore = this.options.incomingStore || new Store()

  // Should QoS zero messages be queued when the connection is broken?
  this.queueQoSZero = this.options.queueQoSZero === undefined ? true : this.options.queueQoSZero

  // map of subscribed topics to support reconnection
  this._resubscribeTopics = {}

  // Ping timer, setup in _setupPingTimer
  this.pingTimer = null
  // Is the client connected?
  this.connected = false
  // Are we disconnecting?
  this.disconnecting = false
  // Packet queue
  this.queue = []
  // connack timer
  this.connackTimer = null
  // Reconnect timer
  this.reconnectTimer = null
  // MessageIDs starting with 1
  this.nextId = Math.floor(Math.random() * 65535)

  // Inflight callbacks
  this.outgoing = {}

  // Mark connected on connect
  this.on('connect', function () {
    if (this.disconnected) {
      return
    }

    this.connected = true
    var outStore = null
    outStore = this.outgoingStore.createStream()

    // Control of stored messages
    outStore.once('readable', function () {
      function storeDeliver () {
        var packet = outStore.read(1)
        var cb

        if (!packet) {
          return
        }

        // Avoid unnecesary stream read operations when disconnected
        if (!that.disconnecting && !that.reconnectTimer && that.options.reconnectPeriod > 0) {
          outStore.read(0)
          cb = that.outgoing[packet.messageId]
          that.outgoing[packet.messageId] = function (err, status) {
            // Ensure that the original callback passed in to publish gets invoked
            if (cb) {
              cb(err, status)
            }

            storeDeliver()
          }
          that._sendPacket(packet)
        } else if (outStore.destroy) {
          outStore.destroy()
        }
      }
      storeDeliver()
    })
    .on('error', this.emit.bind(this, 'error'))
  })

  // Mark disconnected on stream close
  this.on('close', function () {
    this.connected = false
    clearTimeout(this.connackTimer)
  })

  // Setup ping timer
  this.on('connect', this._setupPingTimer)

  // Send queued packets
  this.on('connect', function () {
    var queue = this.queue

    function deliver () {
      var entry = queue.shift()
      var packet = null

      if (!entry) {
        return
      }

      packet = entry.packet

      that._sendPacket(
        packet,
        function (err) {
          if (entry.cb) {
            entry.cb(err)
          }
          deliver()
        }
      )
    }

    deliver()
  })

  // resubscribe
  this.on('reconnect', function () {
    if (this.options.clean && Object.keys(this._resubscribeTopics).length > 0) {
      this.subscribe(this._resubscribeTopics)
    }
  })

  // Clear ping timer
  this.on('close', function () {
    if (that.pingTimer !== null) {
      that.pingTimer.clear()
      that.pingTimer = null
    }
  })

  // Setup reconnect timer on disconnect
  this.on('close', this._setupReconnect)

  events.EventEmitter.call(this)

  this._setupStream()
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mqtt.validations"></a>[module mqtt.validations](#apidoc.module.mqtt.validations)

#### <a name="apidoc.element.mqtt.validations.validateTopics"></a>[function <span class="apidocSignatureSpan">mqtt.validations.</span>validateTopics (topics)](#apidoc.element.mqtt.validations.validateTopics)
- description and source-code
```javascript
function validateTopics(topics) {
  if (topics.length === 0) {
    return 'empty_topic_list'
  }
  for (var i = 0; i < topics.length; i++) {
    if (!validateTopic(topics[i])) {
      return topics[i]
    }
  }
  return null
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
