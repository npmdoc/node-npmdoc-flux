# api documentation for  [flux (v3.1.2)](http://facebook.github.io/flux/)  [![npm package](https://img.shields.io/npm/v/npmdoc-flux.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-flux) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-flux.svg)](https://travis-ci.org/npmdoc/node-npmdoc-flux)
#### An application architecture based on a unidirectional data flow

[![NPM](https://nodei.co/npm/flux.png?downloads=true)](https://www.npmjs.com/package/flux)

[![apidoc](https://npmdoc.github.io/node-npmdoc-flux/build/screenCapture.buildNpmdoc.browser.%252Fhome%252Ftravis%252Fbuild%252Fnpmdoc%252Fnode-npmdoc-flux%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-flux/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-flux/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-flux/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Facebook"
    },
    "bugs": {
        "url": "https://github.com/facebook/flux/issues"
    },
    "contributors": [
        {
            "name": "Jing Chen",
            "email": "jingc@fb.com"
        },
        {
            "name": "Bill Fisher",
            "email": "fisherwebdev@gmail.com"
        },
        {
            "name": "Paul O'Shannessy",
            "email": "paul@oshannessy.com"
        },
        {
            "name": "Kyle Davis",
            "email": "kyldvs@gmail.com"
        }
    ],
    "dependencies": {
        "fbemitter": "^2.0.0",
        "fbjs": "^0.8.0"
    },
    "description": "An application architecture based on a unidirectional data flow",
    "devDependencies": {
        "babel-core": "^5.8.22",
        "babel-loader": "^5.3.2",
        "del": "^2.2.0",
        "fbjs-scripts": "^0.5.0",
        "gulp": "^3.9.0",
        "gulp-babel": "^5.1.0",
        "gulp-flatten": "^0.2.0",
        "gulp-header": "1.8.2",
        "gulp-rename": "^1.2.2",
        "gulp-util": "^3.0.6",
        "immutable": "^3.7.4",
        "jest": "^15.1.1",
        "object-assign": "^4.0.1",
        "react": "^15.0.2",
        "react-addons-test-utils": "^15.0.1",
        "react-dom": "^15.0.1",
        "run-sequence": "^1.1.0",
        "vinyl-source-stream": "^1.0.0",
        "webpack": "^1.11.0",
        "webpack-stream": "^3.1.0"
    },
    "directories": {},
    "dist": {
        "shasum": "8c170addf95b8cb2febb3ddd640aa3e24505762f",
        "tarball": "https://registry.npmjs.org/flux/-/flux-3.1.2.tgz"
    },
    "files": [
        "LICENSE",
        "PATENTS",
        "README.md",
        "index.js",
        "lib",
        "utils.js",
        "dist"
    ],
    "gitHead": "a6dfedde64ea4c8190da8ddcf4486f28ca39a2d3",
    "homepage": "http://facebook.github.io/flux/",
    "jest": {
        "modulePathIgnorePatterns": [
            "/lib/",
            "/node_modules/"
        ],
        "preprocessorIgnorePatterns": [
            "/node_modules/"
        ],
        "rootDir": "./",
        "scriptPreprocessor": "scripts/jest/preprocessor.js",
        "setupFiles": [
            "scripts/jest/environment.js"
        ],
        "testPathDirs": [
            "<rootDir>/src"
        ]
    },
    "keywords": [
        "flux",
        "react",
        "facebook",
        "dispatcher"
    ],
    "license": "BSD-3-Clause",
    "main": "index.js",
    "maintainers": [
        {
            "name": "fisherwebdev",
            "email": "fisherwebdev@gmail.com"
        },
        {
            "name": "fb",
            "email": "opensource+npm@fb.com"
        },
        {
            "name": "kyldvs",
            "email": "kyldvs@gmail.com"
        }
    ],
    "name": "flux",
    "optionalDependencies": {},
    "peerDependencies": {
        "react": "^15.0.2"
    },
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/facebook/flux.git"
    },
    "scripts": {
        "build": "gulp build",
        "prepublish": "gulp publish",
        "test": "NODE_ENV=test jest"
    },
    "version": "3.1.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module flux](#apidoc.module.flux)
1.  [function <span class="apidocSignatureSpan">flux.</span>Dispatcher ()](#apidoc.element.flux.Dispatcher)
1.  [function <span class="apidocSignatureSpan">flux.</span>FluxContainerSubscriptions ()](#apidoc.element.flux.FluxContainerSubscriptions)
1.  [function <span class="apidocSignatureSpan">flux.</span>FluxReduceStore (dispatcher)](#apidoc.element.flux.FluxReduceStore)
1.  [function <span class="apidocSignatureSpan">flux.</span>FluxStore (dispatcher)](#apidoc.element.flux.FluxStore)
1.  [function <span class="apidocSignatureSpan">flux.</span>FluxStoreGroup (stores, callback)](#apidoc.element.flux.FluxStoreGroup)
1.  object <span class="apidocSignatureSpan">flux.</span>Dispatcher.prototype
1.  object <span class="apidocSignatureSpan">flux.</span>FluxContainer
1.  object <span class="apidocSignatureSpan">flux.</span>FluxContainerSubscriptions.prototype
1.  object <span class="apidocSignatureSpan">flux.</span>FluxReduceStore.prototype
1.  object <span class="apidocSignatureSpan">flux.</span>FluxStore.prototype
1.  object <span class="apidocSignatureSpan">flux.</span>FluxStoreGroup.prototype
1.  object <span class="apidocSignatureSpan">flux.</span>utils

#### [module flux.Dispatcher](#apidoc.module.flux.Dispatcher)
1.  [function <span class="apidocSignatureSpan">flux.</span>Dispatcher ()](#apidoc.element.flux.Dispatcher.Dispatcher)

#### [module flux.Dispatcher.prototype](#apidoc.module.flux.Dispatcher.prototype)
1.  [function <span class="apidocSignatureSpan">flux.Dispatcher.prototype.</span>_invokeCallback (id)](#apidoc.element.flux.Dispatcher.prototype._invokeCallback)
1.  [function <span class="apidocSignatureSpan">flux.Dispatcher.prototype.</span>_startDispatching (payload)](#apidoc.element.flux.Dispatcher.prototype._startDispatching)
1.  [function <span class="apidocSignatureSpan">flux.Dispatcher.prototype.</span>_stopDispatching ()](#apidoc.element.flux.Dispatcher.prototype._stopDispatching)
1.  [function <span class="apidocSignatureSpan">flux.Dispatcher.prototype.</span>dispatch (payload)](#apidoc.element.flux.Dispatcher.prototype.dispatch)
1.  [function <span class="apidocSignatureSpan">flux.Dispatcher.prototype.</span>isDispatching ()](#apidoc.element.flux.Dispatcher.prototype.isDispatching)
1.  [function <span class="apidocSignatureSpan">flux.Dispatcher.prototype.</span>register (callback)](#apidoc.element.flux.Dispatcher.prototype.register)
1.  [function <span class="apidocSignatureSpan">flux.Dispatcher.prototype.</span>unregister (id)](#apidoc.element.flux.Dispatcher.prototype.unregister)
1.  [function <span class="apidocSignatureSpan">flux.Dispatcher.prototype.</span>waitFor (ids)](#apidoc.element.flux.Dispatcher.prototype.waitFor)

#### [module flux.FluxContainer](#apidoc.module.flux.FluxContainer)
1.  [function <span class="apidocSignatureSpan">flux.FluxContainer.</span>create (Base, options)](#apidoc.element.flux.FluxContainer.create)
1.  [function <span class="apidocSignatureSpan">flux.FluxContainer.</span>createFunctional (viewFn, _getStores, _calculateState, options)](#apidoc.element.flux.FluxContainer.createFunctional)

#### [module flux.FluxContainerSubscriptions](#apidoc.module.flux.FluxContainerSubscriptions)
1.  [function <span class="apidocSignatureSpan">flux.</span>FluxContainerSubscriptions ()](#apidoc.element.flux.FluxContainerSubscriptions.FluxContainerSubscriptions)

#### [module flux.FluxContainerSubscriptions.prototype](#apidoc.module.flux.FluxContainerSubscriptions.prototype)
1.  [function <span class="apidocSignatureSpan">flux.FluxContainerSubscriptions.prototype.</span>_resetCallbacks ()](#apidoc.element.flux.FluxContainerSubscriptions.prototype._resetCallbacks)
1.  [function <span class="apidocSignatureSpan">flux.FluxContainerSubscriptions.prototype.</span>_resetStoreGroup ()](#apidoc.element.flux.FluxContainerSubscriptions.prototype._resetStoreGroup)
1.  [function <span class="apidocSignatureSpan">flux.FluxContainerSubscriptions.prototype.</span>_resetTokens ()](#apidoc.element.flux.FluxContainerSubscriptions.prototype._resetTokens)
1.  [function <span class="apidocSignatureSpan">flux.FluxContainerSubscriptions.prototype.</span>addListener (fn)](#apidoc.element.flux.FluxContainerSubscriptions.prototype.addListener)
1.  [function <span class="apidocSignatureSpan">flux.FluxContainerSubscriptions.prototype.</span>reset ()](#apidoc.element.flux.FluxContainerSubscriptions.prototype.reset)
1.  [function <span class="apidocSignatureSpan">flux.FluxContainerSubscriptions.prototype.</span>setStores (stores)](#apidoc.element.flux.FluxContainerSubscriptions.prototype.setStores)

#### [module flux.FluxReduceStore](#apidoc.module.flux.FluxReduceStore)
1.  [function <span class="apidocSignatureSpan">flux.</span>FluxReduceStore (dispatcher)](#apidoc.element.flux.FluxReduceStore.FluxReduceStore)

#### [module flux.FluxReduceStore.prototype](#apidoc.module.flux.FluxReduceStore.prototype)
1.  [function <span class="apidocSignatureSpan">flux.FluxReduceStore.prototype.</span>__invokeOnDispatch (action)](#apidoc.element.flux.FluxReduceStore.prototype.__invokeOnDispatch)
1.  [function <span class="apidocSignatureSpan">flux.FluxReduceStore.prototype.</span>areEqual (one, two)](#apidoc.element.flux.FluxReduceStore.prototype.areEqual)
1.  [function <span class="apidocSignatureSpan">flux.FluxReduceStore.prototype.</span>getInitialState ()](#apidoc.element.flux.FluxReduceStore.prototype.getInitialState)
1.  [function <span class="apidocSignatureSpan">flux.FluxReduceStore.prototype.</span>getState ()](#apidoc.element.flux.FluxReduceStore.prototype.getState)
1.  [function <span class="apidocSignatureSpan">flux.FluxReduceStore.prototype.</span>reduce (state, action)](#apidoc.element.flux.FluxReduceStore.prototype.reduce)

#### [module flux.FluxStore](#apidoc.module.flux.FluxStore)
1.  [function <span class="apidocSignatureSpan">flux.</span>FluxStore (dispatcher)](#apidoc.element.flux.FluxStore.FluxStore)

#### [module flux.FluxStore.prototype](#apidoc.module.flux.FluxStore.prototype)
1.  [function <span class="apidocSignatureSpan">flux.FluxStore.prototype.</span>__emitChange ()](#apidoc.element.flux.FluxStore.prototype.__emitChange)
1.  [function <span class="apidocSignatureSpan">flux.FluxStore.prototype.</span>__invokeOnDispatch (payload)](#apidoc.element.flux.FluxStore.prototype.__invokeOnDispatch)
1.  [function <span class="apidocSignatureSpan">flux.FluxStore.prototype.</span>__onDispatch (payload)](#apidoc.element.flux.FluxStore.prototype.__onDispatch)
1.  [function <span class="apidocSignatureSpan">flux.FluxStore.prototype.</span>addListener (callback)](#apidoc.element.flux.FluxStore.prototype.addListener)
1.  [function <span class="apidocSignatureSpan">flux.FluxStore.prototype.</span>getDispatchToken ()](#apidoc.element.flux.FluxStore.prototype.getDispatchToken)
1.  [function <span class="apidocSignatureSpan">flux.FluxStore.prototype.</span>getDispatcher ()](#apidoc.element.flux.FluxStore.prototype.getDispatcher)
1.  [function <span class="apidocSignatureSpan">flux.FluxStore.prototype.</span>hasChanged ()](#apidoc.element.flux.FluxStore.prototype.hasChanged)

#### [module flux.FluxStoreGroup](#apidoc.module.flux.FluxStoreGroup)
1.  [function <span class="apidocSignatureSpan">flux.</span>FluxStoreGroup (stores, callback)](#apidoc.element.flux.FluxStoreGroup.FluxStoreGroup)

#### [module flux.FluxStoreGroup.prototype](#apidoc.module.flux.FluxStoreGroup.prototype)
1.  [function <span class="apidocSignatureSpan">flux.FluxStoreGroup.prototype.</span>release ()](#apidoc.element.flux.FluxStoreGroup.prototype.release)

#### [module flux.utils](#apidoc.module.flux.utils)
1.  [function <span class="apidocSignatureSpan">flux.utils.</span>Mixin (stores)](#apidoc.element.flux.utils.Mixin)
1.  [function <span class="apidocSignatureSpan">flux.utils.</span>ReduceStore (dispatcher)](#apidoc.element.flux.utils.ReduceStore)
1.  [function <span class="apidocSignatureSpan">flux.utils.</span>Store (dispatcher)](#apidoc.element.flux.utils.Store)
1.  object <span class="apidocSignatureSpan">flux.utils.</span>Container



# <a name="apidoc.module.flux"></a>[module flux](#apidoc.module.flux)

#### <a name="apidoc.element.flux.Dispatcher"></a>[function <span class="apidocSignatureSpan">flux.</span>Dispatcher ()](#apidoc.element.flux.Dispatcher)
- description and source-code
```javascript
function Dispatcher() {
  _classCallCheck(this, Dispatcher);

  this._callbacks = {};
  this._isDispatching = false;
  this._isHandled = {};
  this._isPending = {};
  this._lastID = 1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.flux.FluxContainerSubscriptions"></a>[function <span class="apidocSignatureSpan">flux.</span>FluxContainerSubscriptions ()](#apidoc.element.flux.FluxContainerSubscriptions)
- description and source-code
```javascript
function FluxContainerSubscriptions() {
  _classCallCheck(this, FluxContainerSubscriptions);

  this._callbacks = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.flux.FluxReduceStore"></a>[function <span class="apidocSignatureSpan">flux.</span>FluxReduceStore (dispatcher)](#apidoc.element.flux.FluxReduceStore)
- description and source-code
```javascript
function FluxReduceStore(dispatcher) {
  _classCallCheck(this, FluxReduceStore);

  _FluxStore.call(this, dispatcher);
  this._state = this.getInitialState();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.flux.FluxStore"></a>[function <span class="apidocSignatureSpan">flux.</span>FluxStore (dispatcher)](#apidoc.element.flux.FluxStore)
- description and source-code
```javascript
function FluxStore(dispatcher) {
  var _this = this;

  _classCallCheck(this, FluxStore);

  this.__className = this.constructor.name;

  this.__changed = false;
  this.__changeEvent = 'change';
  this.__dispatcher = dispatcher;
  this.__emitter = new EventEmitter();
  this._dispatchToken = dispatcher.register(function (payload) {
    _this.__invokeOnDispatch(payload);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.flux.FluxStoreGroup"></a>[function <span class="apidocSignatureSpan">flux.</span>FluxStoreGroup (stores, callback)](#apidoc.element.flux.FluxStoreGroup)
- description and source-code
```javascript
function FluxStoreGroup(stores, callback) {
  var _this = this;

  _classCallCheck(this, FluxStoreGroup);

  this._dispatcher = _getUniformDispatcher(stores);

  // Precompute store tokens.
  var storeTokens = stores.map(function (store) {
    return store.getDispatchToken();
  });

  // Register with the dispatcher.
  this._dispatchToken = this._dispatcher.register(function (payload) {
    _this._dispatcher.waitFor(storeTokens);
    callback();
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.flux.Dispatcher"></a>[module flux.Dispatcher](#apidoc.module.flux.Dispatcher)

#### <a name="apidoc.element.flux.Dispatcher.Dispatcher"></a>[function <span class="apidocSignatureSpan">flux.</span>Dispatcher ()](#apidoc.element.flux.Dispatcher.Dispatcher)
- description and source-code
```javascript
function Dispatcher() {
  _classCallCheck(this, Dispatcher);

  this._callbacks = {};
  this._isDispatching = false;
  this._isHandled = {};
  this._isPending = {};
  this._lastID = 1;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.flux.Dispatcher.prototype"></a>[module flux.Dispatcher.prototype](#apidoc.module.flux.Dispatcher.prototype)

#### <a name="apidoc.element.flux.Dispatcher.prototype._invokeCallback"></a>[function <span class="apidocSignatureSpan">flux.Dispatcher.prototype.</span>_invokeCallback (id)](#apidoc.element.flux.Dispatcher.prototype._invokeCallback)
- description and source-code
```javascript
function _invokeCallback(id) {
  this._isPending[id] = true;
  this._callbacks[id](this._pendingPayload);
  this._isHandled[id] = true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.flux.Dispatcher.prototype._startDispatching"></a>[function <span class="apidocSignatureSpan">flux.Dispatcher.prototype.</span>_startDispatching (payload)](#apidoc.element.flux.Dispatcher.prototype._startDispatching)
- description and source-code
```javascript
function _startDispatching(payload) {
  for (var id in this._callbacks) {
    this._isPending[id] = false;
    this._isHandled[id] = false;
  }
  this._pendingPayload = payload;
  this._isDispatching = true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.flux.Dispatcher.prototype._stopDispatching"></a>[function <span class="apidocSignatureSpan">flux.Dispatcher.prototype.</span>_stopDispatching ()](#apidoc.element.flux.Dispatcher.prototype._stopDispatching)
- description and source-code
```javascript
function _stopDispatching() {
  delete this._pendingPayload;
  this._isDispatching = false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.flux.Dispatcher.prototype.dispatch"></a>[function <span class="apidocSignatureSpan">flux.Dispatcher.prototype.</span>dispatch (payload)](#apidoc.element.flux.Dispatcher.prototype.dispatch)
- description and source-code
```javascript
function dispatch(payload) {
  !!this._isDispatching ? process.env.NODE_ENV !== 'production' ? invariant(false, 'Dispatch.dispatch(...): Cannot dispatch in the
 middle of a dispatch.') : invariant(false) : undefined;
  this._startDispatching(payload);
  try {
    for (var id in this._callbacks) {
      if (this._isPending[id]) {
        continue;
      }
      this._invokeCallback(id);
    }
  } finally {
    this._stopDispatching();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.flux.Dispatcher.prototype.isDispatching"></a>[function <span class="apidocSignatureSpan">flux.Dispatcher.prototype.</span>isDispatching ()](#apidoc.element.flux.Dispatcher.prototype.isDispatching)
- description and source-code
```javascript
function isDispatching() {
  return this._isDispatching;
}
```
- example usage
```shell
...
};

/**
 * Returns whether the store has changed during the most recent dispatch.
 */

FluxStore.prototype.hasChanged = function hasChanged() {
  !this.__dispatcher.isDispatching() ? process.env.NODE_ENV !== 'production' ? invariant(false, '%s.hasChanged(): Must be invoked
 while dispatching.', this.__className) : invariant(false) : undefined;
  return this.__changed;
};

FluxStore.prototype.__emitChange = function __emitChange() {
  !this.__dispatcher.isDispatching() ? process.env.NODE_ENV !== 'production' ? invariant(false, '%s.__emitChange(): Must be invoked
 while dispatching.', this.__className) : invariant(false) : undefined;
  this.__changed = true;
};
...
```

#### <a name="apidoc.element.flux.Dispatcher.prototype.register"></a>[function <span class="apidocSignatureSpan">flux.Dispatcher.prototype.</span>register (callback)](#apidoc.element.flux.Dispatcher.prototype.register)
- description and source-code
```javascript
function register(callback) {
  var id = _prefix + this._lastID++;
  this._callbacks[id] = callback;
  return id;
}
```
- example usage
```shell
...

  this.__className = this.constructor.name;

  this.__changed = false;
  this.__changeEvent = 'change';
  this.__dispatcher = dispatcher;
  this.__emitter = new EventEmitter();
  this._dispatchToken = dispatcher.register(function (payload) {
    _this.__invokeOnDispatch(payload);
  });
}

FluxStore.prototype.addListener = function addListener(callback) {
  return this.__emitter.addListener(this.__changeEvent, callback);
};
...
```

#### <a name="apidoc.element.flux.Dispatcher.prototype.unregister"></a>[function <span class="apidocSignatureSpan">flux.Dispatcher.prototype.</span>unregister (id)](#apidoc.element.flux.Dispatcher.prototype.unregister)
- description and source-code
```javascript
function unregister(id) {
  !this._callbacks[id] ? process.env.NODE_ENV !== 'production' ? invariant(false, 'Dispatcher.unregister(...): '%s' does not map
 to a registered callback.', id) : invariant(false) : undefined;
  delete this._callbacks[id];
}
```
- example usage
```shell
...
  this._dispatchToken = this._dispatcher.register(function (payload) {
    _this._dispatcher.waitFor(storeTokens);
    callback();
  });
}

FluxStoreGroup.prototype.release = function release() {
  this._dispatcher.unregister(this._dispatchToken);
};

return FluxStoreGroup;
})();

function _getUniformDispatcher(stores) {
!(stores && stores.length) ? process.env.NODE_ENV !== 'production' ? invariant(false, 'Must provide at least one store to FluxStoreGroup
') : invariant(false) : undefined;
...
```

#### <a name="apidoc.element.flux.Dispatcher.prototype.waitFor"></a>[function <span class="apidocSignatureSpan">flux.Dispatcher.prototype.</span>waitFor (ids)](#apidoc.element.flux.Dispatcher.prototype.waitFor)
- description and source-code
```javascript
function waitFor(ids) {
  !this._isDispatching ? process.env.NODE_ENV !== 'production' ? invariant(false, 'Dispatcher.waitFor(...): Must be invoked while
 dispatching.') : invariant(false) : undefined;
  for (var ii = 0; ii < ids.length; ii++) {
    var id = ids[ii];
    if (this._isPending[id]) {
      !this._isHandled[id] ? process.env.NODE_ENV !== 'production' ? invariant(false, 'Dispatcher.waitFor(...): Circular dependency
 detected while ' + 'waiting for '%s'.', id) : invariant(false) : undefined;
      continue;
    }
    !this._callbacks[id] ? process.env.NODE_ENV !== 'production' ? invariant(false, 'Dispatcher.waitFor(...): '%s' does not map
to a registered callback.', id) : invariant(false) : undefined;
    this._invokeCallback(id);
  }
}
```
- example usage
```shell
...
  // Precompute store tokens.
  var storeTokens = stores.map(function (store) {
    return store.getDispatchToken();
  });

  // Register with the dispatcher.
  this._dispatchToken = this._dispatcher.register(function (payload) {
    _this._dispatcher.waitFor(storeTokens);
    callback();
  });
}

FluxStoreGroup.prototype.release = function release() {
  this._dispatcher.unregister(this._dispatchToken);
};
...
```



# <a name="apidoc.module.flux.FluxContainer"></a>[module flux.FluxContainer](#apidoc.module.flux.FluxContainer)

#### <a name="apidoc.element.flux.FluxContainer.create"></a>[function <span class="apidocSignatureSpan">flux.FluxContainer.</span>create (Base, options)](#apidoc.element.flux.FluxContainer.create)
- description and source-code
```javascript
function create(Base, options) {
  enforceInterface(Base);

  // Construct the options using default, override with user values as necessary.
  var realOptions = _extends({}, DEFAULT_OPTIONS, options || {});

  var getState = function (state, maybeProps, maybeContext) {
    var props = realOptions.withProps ? maybeProps : undefined;
    var context = realOptions.withContext ? maybeContext : undefined;
    return Base.calculateState(state, props, context);
  };

  var getStores = function (maybeProps, maybeContext) {
    var props = realOptions.withProps ? maybeProps : undefined;
    var context = realOptions.withContext ? maybeContext : undefined;
    return Base.getStores(props, context);
  };

  // Build the container class.

  var ContainerClass = (function (_Base) {
    _inherits(ContainerClass, _Base);

    function ContainerClass(props, context) {
      var _this = this;

      _classCallCheck(this, ContainerClass);

      _Base.call(this, props, context);
      this._fluxContainerSubscriptions = new FluxContainerSubscriptions();
      this._fluxContainerSubscriptions.setStores(getStores(props));
      this._fluxContainerSubscriptions.addListener(function () {
        _this.setState(function (prevState, currentProps) {
          return getState(prevState, currentProps, context);
        });
      });
      var calculatedState = getState(undefined, props, context);
      this.state = _extends({}, this.state || {}, calculatedState);
    }

    // Make sure we override shouldComponentUpdate only if the pure option is
    // specified. We can't override this above because we don't want to override
    // the default behavior on accident. Super works weird with react ES6 classes.

    ContainerClass.prototype.componentWillReceiveProps = function componentWillReceiveProps(nextProps, nextContext) {
      if (_Base.prototype.componentWillReceiveProps) {
        _Base.prototype.componentWillReceiveProps.call(this, nextProps, nextContext);
      }

      if (realOptions.withProps || realOptions.withContext) {
        // Update both stores and state.
        this._fluxContainerSubscriptions.setStores(getStores(nextProps, nextContext));
        this.setState(function (prevState) {
          return getState(prevState, nextProps, nextContext);
        });
      }
    };

    ContainerClass.prototype.componentWillUnmount = function componentWillUnmount() {
      if (_Base.prototype.componentWillUnmount) {
        _Base.prototype.componentWillUnmount.call(this);
      }

      this._fluxContainerSubscriptions.reset();
    };

    return ContainerClass;
  })(Base);

  var container = realOptions.pure ? createPureComponent(ContainerClass) : ContainerClass;

  // Update the name of the container before returning
  var componentName = Base.displayName || Base.name;
  container.displayName = 'FluxContainer(' + componentName + ')';
  return container;
}
```
- example usage
```shell
...

'use strict';

var _extends = Object.assign || function (target) { for (var i = 1; i < arguments.length; i++) { var source = arguments[i]; for (
var key in source) { if (Object.prototype.hasOwnProperty.call(source, key)) { target[key] = source[key]; } } } return target; };

function _classCallCheck(instance, Constructor) { if (!(instance instanceof Constructor)) { throw new TypeError('Cannot call a class
 as a function'); } }

function _inherits(subClass, superClass) { if (typeof superClass !== 'function' && superClass !== null) { throw new TypeError('Super
 expression must either be null or a function, not ' + typeof superClass); } subClass.prototype = Object.create(superClass && superClass
.prototype, { constructor: { value: subClass, enumerable: false, writable: true, configurable: true } }); if (superClass) Object
.setPrototypeOf ? Object.setPrototypeOf(subClass, superClass) : subClass.__proto__ = superClass; }

var FluxContainerSubscriptions = require('./FluxContainerSubscriptions');
var React = require('react');

var invariant = require('fbjs/lib/invariant');
var shallowEqual = require('fbjs/lib/shallowEqual');
...
```

#### <a name="apidoc.element.flux.FluxContainer.createFunctional"></a>[function <span class="apidocSignatureSpan">flux.FluxContainer.</span>createFunctional (viewFn, _getStores, _calculateState, options)](#apidoc.element.flux.FluxContainer.createFunctional)
- description and source-code
```javascript
function createFunctional(viewFn, _getStores, _calculateState, options) {
  var FunctionalContainer = (function (_Component) {
    _inherits(FunctionalContainer, _Component);

    function FunctionalContainer() {
      _classCallCheck(this, FunctionalContainer);

      _Component.apply(this, arguments);
    }

    // Update the name of the component before creating the container.

    FunctionalContainer.getStores = function getStores(props, context) {
      return _getStores(props, context);
    };

    FunctionalContainer.calculateState = function calculateState(prevState, props, context) {
      return _calculateState(prevState, props, context);
    };

    FunctionalContainer.prototype.render = function render() {
      return viewFn(this.state);
    };

    return FunctionalContainer;
  })(Component);

  var viewFnName = viewFn.displayName || viewFn.name || 'FunctionalContainer';
  FunctionalContainer.displayName = viewFnName;
  return create(FunctionalContainer, options);
}
```
- example usage
```shell
...
 *
 *   function calculateState() {
 *     return {
 *       value: FooStore.getState();
 *     };
 *   }
 *
 *   module.exports = FluxContainer.createFunctional(
 *     FooView,
 *     getStores,
 *     calculateState,
 *   );
 *
 */
function createFunctional(viewFn, _getStores, _calculateState, options) {
...
```



# <a name="apidoc.module.flux.FluxContainerSubscriptions"></a>[module flux.FluxContainerSubscriptions](#apidoc.module.flux.FluxContainerSubscriptions)

#### <a name="apidoc.element.flux.FluxContainerSubscriptions.FluxContainerSubscriptions"></a>[function <span class="apidocSignatureSpan">flux.</span>FluxContainerSubscriptions ()](#apidoc.element.flux.FluxContainerSubscriptions.FluxContainerSubscriptions)
- description and source-code
```javascript
function FluxContainerSubscriptions() {
  _classCallCheck(this, FluxContainerSubscriptions);

  this._callbacks = [];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.flux.FluxContainerSubscriptions.prototype"></a>[module flux.FluxContainerSubscriptions.prototype](#apidoc.module.flux.FluxContainerSubscriptions.prototype)

#### <a name="apidoc.element.flux.FluxContainerSubscriptions.prototype._resetCallbacks"></a>[function <span class="apidocSignatureSpan">flux.FluxContainerSubscriptions.prototype.</span>_resetCallbacks ()](#apidoc.element.flux.FluxContainerSubscriptions.prototype._resetCallbacks)
- description and source-code
```javascript
function _resetCallbacks() {
  this._callbacks = [];
}
```
- example usage
```shell
...
FluxContainerSubscriptions.prototype.addListener = function addListener(fn) {
  this._callbacks.push(fn);
};

FluxContainerSubscriptions.prototype.reset = function reset() {
  this._resetTokens();
  this._resetStoreGroup();
  this._resetCallbacks();
};

FluxContainerSubscriptions.prototype._resetTokens = function _resetTokens() {
  if (this._tokens) {
    this._tokens.forEach(function (token) {
      return token.remove();
    });
...
```

#### <a name="apidoc.element.flux.FluxContainerSubscriptions.prototype._resetStoreGroup"></a>[function <span class="apidocSignatureSpan">flux.FluxContainerSubscriptions.prototype.</span>_resetStoreGroup ()](#apidoc.element.flux.FluxContainerSubscriptions.prototype._resetStoreGroup)
- description and source-code
```javascript
function _resetStoreGroup() {
  if (this._storeGroup) {
    this._storeGroup.release();
    this._storeGroup = null;
  }
}
```
- example usage
```shell
...
this._callbacks = [];
  }

  FluxContainerSubscriptions.prototype.setStores = function setStores(stores) {
var _this = this;

this._resetTokens();
this._resetStoreGroup();

var changed = false;
var changedStores = [];

if (process.env.NODE_ENV !== 'production') {
  // Keep track of the stores that changed for debugging purposes only
  this._tokens = stores.map(function (store) {
...
```

#### <a name="apidoc.element.flux.FluxContainerSubscriptions.prototype._resetTokens"></a>[function <span class="apidocSignatureSpan">flux.FluxContainerSubscriptions.prototype.</span>_resetTokens ()](#apidoc.element.flux.FluxContainerSubscriptions.prototype._resetTokens)
- description and source-code
```javascript
function _resetTokens() {
  if (this._tokens) {
    this._tokens.forEach(function (token) {
      return token.remove();
    });
    this._tokens = null;
  }
}
```
- example usage
```shell
...

this._callbacks = [];
  }

  FluxContainerSubscriptions.prototype.setStores = function setStores(stores) {
var _this = this;

this._resetTokens();
this._resetStoreGroup();

var changed = false;
var changedStores = [];

if (process.env.NODE_ENV !== 'production') {
  // Keep track of the stores that changed for debugging purposes only
...
```

#### <a name="apidoc.element.flux.FluxContainerSubscriptions.prototype.addListener"></a>[function <span class="apidocSignatureSpan">flux.FluxContainerSubscriptions.prototype.</span>addListener (fn)](#apidoc.element.flux.FluxContainerSubscriptions.prototype.addListener)
- description and source-code
```javascript
function addListener(fn) {
  this._callbacks.push(fn);
}
```
- example usage
```shell
...
  var _this = this;

  _classCallCheck(this, ContainerClass);

  _Base.call(this, props, context);
  this._fluxContainerSubscriptions = new FluxContainerSubscriptions();
  this._fluxContainerSubscriptions.setStores(getStores(props));
  this._fluxContainerSubscriptions.addListener(function () {
    _this.setState(function (prevState, currentProps) {
      return getState(prevState, currentProps, context);
    });
  });
  var calculatedState = getState(undefined, props, context);
  this.state = _extends({}, this.state || {}, calculatedState);
}
...
```

#### <a name="apidoc.element.flux.FluxContainerSubscriptions.prototype.reset"></a>[function <span class="apidocSignatureSpan">flux.FluxContainerSubscriptions.prototype.</span>reset ()](#apidoc.element.flux.FluxContainerSubscriptions.prototype.reset)
- description and source-code
```javascript
function reset() {
  this._resetTokens();
  this._resetStoreGroup();
  this._resetCallbacks();
}
```
- example usage
```shell
...
  };

  ContainerClass.prototype.componentWillUnmount = function componentWillUnmount() {
    if (_Base.prototype.componentWillUnmount) {
      _Base.prototype.componentWillUnmount.call(this);
    }

    this._fluxContainerSubscriptions.reset();
  };

  return ContainerClass;
})(Base);

var container = realOptions.pure ? createPureComponent(ContainerClass) : ContainerClass;
...
```

#### <a name="apidoc.element.flux.FluxContainerSubscriptions.prototype.setStores"></a>[function <span class="apidocSignatureSpan">flux.FluxContainerSubscriptions.prototype.</span>setStores (stores)](#apidoc.element.flux.FluxContainerSubscriptions.prototype.setStores)
- description and source-code
```javascript
function setStores(stores) {
  var _this = this;

  this._resetTokens();
  this._resetStoreGroup();

  var changed = false;
  var changedStores = [];

  if (process.env.NODE_ENV !== 'production') {
    // Keep track of the stores that changed for debugging purposes only
    this._tokens = stores.map(function (store) {
      return store.addListener(function () {
        changed = true;
        changedStores.push(store);
      });
    });
  } else {
    (function () {
      var setChanged = function () {
        changed = true;
      };
      _this._tokens = stores.map(function (store) {
        return store.addListener(setChanged);
      });
    })();
  }

  var callCallbacks = function () {
    if (changed) {
      _this._callbacks.forEach(function (fn) {
        return fn();
      });
      changed = false;
      if (process.env.NODE_ENV !== 'production') {
        // Uncomment this to print the stores that changed.
        // console.log(changedStores);
        changedStores = [];
      }
    }
  };
  this._storeGroup = new FluxStoreGroup(stores, callCallbacks);
}
```
- example usage
```shell
...
    function ContainerClass(props, context) {
var _this = this;

_classCallCheck(this, ContainerClass);

_Base.call(this, props, context);
this._fluxContainerSubscriptions = new FluxContainerSubscriptions();
this._fluxContainerSubscriptions.setStores(getStores(props));
this._fluxContainerSubscriptions.addListener(function () {
  _this.setState(function (prevState, currentProps) {
    return getState(prevState, currentProps, context);
  });
});
var calculatedState = getState(undefined, props, context);
this.state = _extends({}, this.state || {}, calculatedState);
...
```



# <a name="apidoc.module.flux.FluxReduceStore"></a>[module flux.FluxReduceStore](#apidoc.module.flux.FluxReduceStore)

#### <a name="apidoc.element.flux.FluxReduceStore.FluxReduceStore"></a>[function <span class="apidocSignatureSpan">flux.</span>FluxReduceStore (dispatcher)](#apidoc.element.flux.FluxReduceStore.FluxReduceStore)
- description and source-code
```javascript
function FluxReduceStore(dispatcher) {
  _classCallCheck(this, FluxReduceStore);

  _FluxStore.call(this, dispatcher);
  this._state = this.getInitialState();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.flux.FluxReduceStore.prototype"></a>[module flux.FluxReduceStore.prototype](#apidoc.module.flux.FluxReduceStore.prototype)

#### <a name="apidoc.element.flux.FluxReduceStore.prototype.__invokeOnDispatch"></a>[function <span class="apidocSignatureSpan">flux.FluxReduceStore.prototype.</span>__invokeOnDispatch (action)](#apidoc.element.flux.FluxReduceStore.prototype.__invokeOnDispatch)
- description and source-code
```javascript
function __invokeOnDispatch(action) {
  this.__changed = false;

  // Reduce the stream of incoming actions to state, update when necessary.
  var startingState = this._state;
  var endingState = this.reduce(startingState, action);

  // This means your ending state should never be undefined.
  !(endingState !== undefined) ? process.env.NODE_ENV !== 'production' ? invariant(false, '%s returned undefined from reduce(...),
did you forget to return ' + 'state in the default case? (use null if this was intentional)', this.constructor.name) : invariant
(false) : undefined;

  if (!this.areEqual(startingState, endingState)) {
    this._state = endingState;

    // '__emitChange()' sets 'this.__changed' to true and then the actual
    // change will be fired from the emitter at the end of the dispatch, this
    // is required in order to support methods like 'hasChanged()'
    this.__emitChange();
  }

  if (this.__changed) {
    this.__emitter.emit(this.__changeEvent);
  }
}
```
- example usage
```shell
...
  this.__className = this.constructor.name;

  this.__changed = false;
  this.__changeEvent = 'change';
  this.__dispatcher = dispatcher;
  this.__emitter = new EventEmitter();
  this._dispatchToken = dispatcher.register(function (payload) {
    _this.__invokeOnDispatch(payload);
  });
}

FluxStore.prototype.addListener = function addListener(callback) {
  return this.__emitter.addListener(this.__changeEvent, callback);
};
...
```

#### <a name="apidoc.element.flux.FluxReduceStore.prototype.areEqual"></a>[function <span class="apidocSignatureSpan">flux.FluxReduceStore.prototype.</span>areEqual (one, two)](#apidoc.element.flux.FluxReduceStore.prototype.areEqual)
- description and source-code
```javascript
function areEqual(one, two) {
  return one === two;
}
```
- example usage
```shell
...
// Reduce the stream of incoming actions to state, update when necessary.
var startingState = this._state;
var endingState = this.reduce(startingState, action);

// This means your ending state should never be undefined.
!(endingState !== undefined) ? process.env.NODE_ENV !== 'production' ? invariant(false, '%s returned undefined from reduce(...),
did you forget to return ' + 'state in the default case? (use null if this was intentional)', this.constructor.name) : invariant
(false) : undefined;

if (!this.areEqual(startingState, endingState)) {
  this._state = endingState;

  // '__emitChange()' sets 'this.__changed' to true and then the actual
  // change will be fired from the emitter at the end of the dispatch, this
  // is required in order to support methods like 'hasChanged()'
  this.__emitChange();
}
...
```

#### <a name="apidoc.element.flux.FluxReduceStore.prototype.getInitialState"></a>[function <span class="apidocSignatureSpan">flux.FluxReduceStore.prototype.</span>getInitialState ()](#apidoc.element.flux.FluxReduceStore.prototype.getInitialState)
- description and source-code
```javascript
function getInitialState() {
  return abstractMethod('FluxReduceStore', 'getInitialState');
}
```
- example usage
```shell
...
var FluxReduceStore = (function (_FluxStore) {
_inherits(FluxReduceStore, _FluxStore);

function FluxReduceStore(dispatcher) {
  _classCallCheck(this, FluxReduceStore);

  _FluxStore.call(this, dispatcher);
  this._state = this.getInitialState();
}

/**
 * Getter that exposes the entire state of this store. If your state is not
 * immutable you should override this and not expose _state directly.
 */
...
```

#### <a name="apidoc.element.flux.FluxReduceStore.prototype.getState"></a>[function <span class="apidocSignatureSpan">flux.FluxReduceStore.prototype.</span>getState ()](#apidoc.element.flux.FluxReduceStore.prototype.getState)
- description and source-code
```javascript
function getState() {
  return this._state;
}
```
- example usage
```shell
...
*   class FooContainer extends Component {
*     static getStores() {
*       return [FooStore];
*     }
*
*     static calculateState() {
*       return {
*         foo: FooStore.getState(),
*       };
*     }
*
*     render() {
*       return <FooView {...this.state} />;
*     }
*   }
...
```

#### <a name="apidoc.element.flux.FluxReduceStore.prototype.reduce"></a>[function <span class="apidocSignatureSpan">flux.FluxReduceStore.prototype.</span>reduce (state, action)](#apidoc.element.flux.FluxReduceStore.prototype.reduce)
- description and source-code
```javascript
function reduce(state, action) {
  return abstractMethod('FluxReduceStore', 'reduce');
}
```
- example usage
```shell
...
  };

  FluxReduceStore.prototype.__invokeOnDispatch = function __invokeOnDispatch(action) {
this.__changed = false;

// Reduce the stream of incoming actions to state, update when necessary.
var startingState = this._state;
var endingState = this.reduce(startingState, action);

// This means your ending state should never be undefined.
!(endingState !== undefined) ? process.env.NODE_ENV !== 'production' ? invariant(false, '%s returned undefined from reduce(...),
did you forget to return ' + 'state in the default case? (use null if this was intentional)', this.constructor.name) : invariant
(false) : undefined;

if (!this.areEqual(startingState, endingState)) {
  this._state = endingState;
...
```



# <a name="apidoc.module.flux.FluxStore"></a>[module flux.FluxStore](#apidoc.module.flux.FluxStore)

#### <a name="apidoc.element.flux.FluxStore.FluxStore"></a>[function <span class="apidocSignatureSpan">flux.</span>FluxStore (dispatcher)](#apidoc.element.flux.FluxStore.FluxStore)
- description and source-code
```javascript
function FluxStore(dispatcher) {
  var _this = this;

  _classCallCheck(this, FluxStore);

  this.__className = this.constructor.name;

  this.__changed = false;
  this.__changeEvent = 'change';
  this.__dispatcher = dispatcher;
  this.__emitter = new EventEmitter();
  this._dispatchToken = dispatcher.register(function (payload) {
    _this.__invokeOnDispatch(payload);
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.flux.FluxStore.prototype"></a>[module flux.FluxStore.prototype](#apidoc.module.flux.FluxStore.prototype)

#### <a name="apidoc.element.flux.FluxStore.prototype.__emitChange"></a>[function <span class="apidocSignatureSpan">flux.FluxStore.prototype.</span>__emitChange ()](#apidoc.element.flux.FluxStore.prototype.__emitChange)
- description and source-code
```javascript
function __emitChange() {
  !this.__dispatcher.isDispatching() ? process.env.NODE_ENV !== 'production' ? invariant(false, '%s.__emitChange(): Must be invoked
 while dispatching.', this.__className) : invariant(false) : undefined;
  this.__changed = true;
}
```
- example usage
```shell
...

  if (!this.areEqual(startingState, endingState)) {
    this._state = endingState;

    // '__emitChange()' sets 'this.__changed' to true and then the actual
    // change will be fired from the emitter at the end of the dispatch, this
    // is required in order to support methods like 'hasChanged()'
    this.__emitChange();
  }

  if (this.__changed) {
    this.__emitter.emit(this.__changeEvent);
  }
};
...
```

#### <a name="apidoc.element.flux.FluxStore.prototype.__invokeOnDispatch"></a>[function <span class="apidocSignatureSpan">flux.FluxStore.prototype.</span>__invokeOnDispatch (payload)](#apidoc.element.flux.FluxStore.prototype.__invokeOnDispatch)
- description and source-code
```javascript
function __invokeOnDispatch(payload) {
  this.__changed = false;
  this.__onDispatch(payload);
  if (this.__changed) {
    this.__emitter.emit(this.__changeEvent);
  }
}
```
- example usage
```shell
...
  this.__className = this.constructor.name;

  this.__changed = false;
  this.__changeEvent = 'change';
  this.__dispatcher = dispatcher;
  this.__emitter = new EventEmitter();
  this._dispatchToken = dispatcher.register(function (payload) {
    _this.__invokeOnDispatch(payload);
  });
}

FluxStore.prototype.addListener = function addListener(callback) {
  return this.__emitter.addListener(this.__changeEvent, callback);
};
...
```

#### <a name="apidoc.element.flux.FluxStore.prototype.__onDispatch"></a>[function <span class="apidocSignatureSpan">flux.FluxStore.prototype.</span>__onDispatch (payload)](#apidoc.element.flux.FluxStore.prototype.__onDispatch)
- description and source-code
```javascript
function __onDispatch(payload) {
  !false ? process.env.NODE_ENV !== 'production' ? invariant(false, '%s has not overridden FluxStore.__onDispatch(), which is required
', this.__className) : invariant(false) : undefined;
}
```
- example usage
```shell
...
 * This method encapsulates all logic for invoking __onDispatch. It should
 * be used for things like catching changes and emitting them after the
 * subclass has handled a payload.
 */

FluxStore.prototype.__invokeOnDispatch = function __invokeOnDispatch(payload) {
  this.__changed = false;
  this.__onDispatch(payload);
  if (this.__changed) {
    this.__emitter.emit(this.__changeEvent);
  }
};

/**
 * The callback that will be registered with the dispatcher during
...
```

#### <a name="apidoc.element.flux.FluxStore.prototype.addListener"></a>[function <span class="apidocSignatureSpan">flux.FluxStore.prototype.</span>addListener (callback)](#apidoc.element.flux.FluxStore.prototype.addListener)
- description and source-code
```javascript
function addListener(callback) {
  return this.__emitter.addListener(this.__changeEvent, callback);
}
```
- example usage
```shell
...
  var _this = this;

  _classCallCheck(this, ContainerClass);

  _Base.call(this, props, context);
  this._fluxContainerSubscriptions = new FluxContainerSubscriptions();
  this._fluxContainerSubscriptions.setStores(getStores(props));
  this._fluxContainerSubscriptions.addListener(function () {
    _this.setState(function (prevState, currentProps) {
      return getState(prevState, currentProps, context);
    });
  });
  var calculatedState = getState(undefined, props, context);
  this.state = _extends({}, this.state || {}, calculatedState);
}
...
```

#### <a name="apidoc.element.flux.FluxStore.prototype.getDispatchToken"></a>[function <span class="apidocSignatureSpan">flux.FluxStore.prototype.</span>getDispatchToken ()](#apidoc.element.flux.FluxStore.prototype.getDispatchToken)
- description and source-code
```javascript
function getDispatchToken() {
  return this._dispatchToken;
}
```
- example usage
```shell
...

_classCallCheck(this, FluxStoreGroup);

this._dispatcher = _getUniformDispatcher(stores);

// Precompute store tokens.
var storeTokens = stores.map(function (store) {
  return store.getDispatchToken();
});

// Register with the dispatcher.
this._dispatchToken = this._dispatcher.register(function (payload) {
  _this._dispatcher.waitFor(storeTokens);
  callback();
});
...
```

#### <a name="apidoc.element.flux.FluxStore.prototype.getDispatcher"></a>[function <span class="apidocSignatureSpan">flux.FluxStore.prototype.</span>getDispatcher ()](#apidoc.element.flux.FluxStore.prototype.getDispatcher)
- description and source-code
```javascript
function getDispatcher() {
  return this.__dispatcher;
}
```
- example usage
```shell
...
  };

  return FluxStoreGroup;
})();

function _getUniformDispatcher(stores) {
  !(stores && stores.length) ? process.env.NODE_ENV !== 'production' ? invariant(false, 'Must provide at least one store to FluxStoreGroup
') : invariant(false) : undefined;
  var dispatcher = stores[0].getDispatcher();
  if (process.env.NODE_ENV !== 'production') {
    for (var _iterator = stores, _isArray = Array.isArray(_iterator), _i = 0, _iterator = _isArray ? _iterator : _iterator[Symbol
.iterator]();;) {
var _ref;

if (_isArray) {
  if (_i >= _iterator.length) break;
  _ref = _iterator[_i++];
...
```

#### <a name="apidoc.element.flux.FluxStore.prototype.hasChanged"></a>[function <span class="apidocSignatureSpan">flux.FluxStore.prototype.</span>hasChanged ()](#apidoc.element.flux.FluxStore.prototype.hasChanged)
- description and source-code
```javascript
function hasChanged() {
  !this.__dispatcher.isDispatching() ? process.env.NODE_ENV !== 'production' ? invariant(false, '%s.hasChanged(): Must be invoked
 while dispatching.', this.__className) : invariant(false) : undefined;
  return this.__changed;
}
```
- example usage
```shell
...
};

/**
 * Returns whether the store has changed during the most recent dispatch.
 */

FluxStore.prototype.hasChanged = function hasChanged() {
  !this.__dispatcher.isDispatching() ? process.env.NODE_ENV !== 'production' ? invariant(false, '%s.hasChanged(): Must be invoked
 while dispatching.', this.__className) : invariant(false) : undefined;
  return this.__changed;
};

FluxStore.prototype.__emitChange = function __emitChange() {
  !this.__dispatcher.isDispatching() ? process.env.NODE_ENV !== 'production' ? invariant(false, '%s.__emitChange(): Must be invoked
 while dispatching.', this.__className) : invariant(false) : undefined;
  this.__changed = true;
};
...
```



# <a name="apidoc.module.flux.FluxStoreGroup"></a>[module flux.FluxStoreGroup](#apidoc.module.flux.FluxStoreGroup)

#### <a name="apidoc.element.flux.FluxStoreGroup.FluxStoreGroup"></a>[function <span class="apidocSignatureSpan">flux.</span>FluxStoreGroup (stores, callback)](#apidoc.element.flux.FluxStoreGroup.FluxStoreGroup)
- description and source-code
```javascript
function FluxStoreGroup(stores, callback) {
  var _this = this;

  _classCallCheck(this, FluxStoreGroup);

  this._dispatcher = _getUniformDispatcher(stores);

  // Precompute store tokens.
  var storeTokens = stores.map(function (store) {
    return store.getDispatchToken();
  });

  // Register with the dispatcher.
  this._dispatchToken = this._dispatcher.register(function (payload) {
    _this._dispatcher.waitFor(storeTokens);
    callback();
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.flux.FluxStoreGroup.prototype"></a>[module flux.FluxStoreGroup.prototype](#apidoc.module.flux.FluxStoreGroup.prototype)

#### <a name="apidoc.element.flux.FluxStoreGroup.prototype.release"></a>[function <span class="apidocSignatureSpan">flux.FluxStoreGroup.prototype.</span>release ()](#apidoc.element.flux.FluxStoreGroup.prototype.release)
- description and source-code
```javascript
function release() {
  this._dispatcher.unregister(this._dispatchToken);
}
```
- example usage
```shell
...
    });
    this._tokens = null;
  }
};

FluxContainerSubscriptions.prototype._resetStoreGroup = function _resetStoreGroup() {
  if (this._storeGroup) {
    this._storeGroup.release();
    this._storeGroup = null;
  }
};

FluxContainerSubscriptions.prototype._resetCallbacks = function _resetCallbacks() {
  this._callbacks = [];
};
...
```



# <a name="apidoc.module.flux.utils"></a>[module flux.utils](#apidoc.module.flux.utils)

#### <a name="apidoc.element.flux.utils.Mixin"></a>[function <span class="apidocSignatureSpan">flux.utils.</span>Mixin (stores)](#apidoc.element.flux.utils.Mixin)
- description and source-code
```javascript
function FluxMixinLegacy(stores) {
  var options = arguments.length <= 1 || arguments[1] === undefined ? { withProps: false } : arguments[1];

  stores = stores.filter(function (store) {
    return !!store;
  });

  return {
    getInitialState: function () {
      enforceInterface(this);
      return options.withProps ? this.constructor.calculateState(null, this.props) : this.constructor.calculateState(null, undefined
);
    },

    componentWillMount: function () {
      var _this = this;

      // This tracks when any store has changed and we may need to update.
      var changed = false;
      var setChanged = function () {
        changed = true;
      };

      // This adds subscriptions to stores. When a store changes all we do is
      // set changed to true.
      this._fluxMixinSubscriptions = stores.map(function (store) {
        return store.addListener(setChanged);
      });

      // This callback is called after the dispatch of the relevant stores. If
      // any have reported a change we update the state, then reset changed.
      var callback = function () {
        if (changed) {
          _this.setState(function (prevState) {
            return options.withProps ? _this.constructor.calculateState(prevState, _this.props) : _this.constructor.calculateState
(prevState, undefined);
          });
        }
        changed = false;
      };
      this._fluxMixinStoreGroup = new FluxStoreGroup(stores, callback);
    },

    componentWillUnmount: function () {
      this._fluxMixinStoreGroup.release();
      for (var _iterator = this._fluxMixinSubscriptions, _isArray = Array.isArray(_iterator), _i = 0, _iterator = _isArray ? _iterator
 : _iterator[Symbol.iterator]();;) {
        var _ref;

        if (_isArray) {
          if (_i >= _iterator.length) break;
          _ref = _iterator[_i++];
        } else {
          _i = _iterator.next();
          if (_i.done) break;
          _ref = _i.value;
        }

        var subscription = _ref;

        subscription.remove();
      }
      this._fluxMixinSubscriptions = [];
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.flux.utils.ReduceStore"></a>[function <span class="apidocSignatureSpan">flux.utils.</span>ReduceStore (dispatcher)](#apidoc.element.flux.utils.ReduceStore)
- description and source-code
```javascript
function FluxReduceStore(dispatcher) {
  _classCallCheck(this, FluxReduceStore);

  _FluxStore.call(this, dispatcher);
  this._state = this.getInitialState();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.flux.utils.Store"></a>[function <span class="apidocSignatureSpan">flux.utils.</span>Store (dispatcher)](#apidoc.element.flux.utils.Store)
- description and source-code
```javascript
function FluxStore(dispatcher) {
  var _this = this;

  _classCallCheck(this, FluxStore);

  this.__className = this.constructor.name;

  this.__changed = false;
  this.__changeEvent = 'change';
  this.__dispatcher = dispatcher;
  this.__emitter = new EventEmitter();
  this._dispatchToken = dispatcher.register(function (payload) {
    _this.__invokeOnDispatch(payload);
  });
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
