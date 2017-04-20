# npmdoc-flux

#### api documentation for  [flux (v3.1.2)](http://facebook.github.io/flux/)  [![npm package](https://img.shields.io/npm/v/npmdoc-flux.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-flux) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-flux.svg)](https://travis-ci.org/npmdoc/node-npmdoc-flux)

#### An application architecture based on a unidirectional data flow

[![NPM](https://nodei.co/npm/flux.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/flux)

- [https://npmdoc.github.io/node-npmdoc-flux/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-flux/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-flux/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-flux/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-flux/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-flux/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "flux",
    "version": "3.1.2",
    "description": "An application architecture based on a unidirectional data flow",
    "keywords": [
        "flux",
        "react",
        "facebook",
        "dispatcher"
    ],
    "homepage": "http://facebook.github.io/flux/",
    "bugs": "https://github.com/facebook/flux/issues",
    "files": [
        "LICENSE",
        "PATENTS",
        "README.md",
        "index.js",
        "lib",
        "utils.js",
        "dist"
    ],
    "main": "index.js",
    "scripts": {
        "build": "gulp build",
        "prepublish": "gulp publish",
        "test": "NODE_ENV=test jest"
    },
    "repository": {
        "type": "git",
        "url": "https://github.com/facebook/flux"
    },
    "author": "Facebook",
    "contributors": [
        "Jing Chen <jingc@fb.com>",
        "Bill Fisher <fisherwebdev@gmail.com>",
        "Paul O'Shannessy <paul@oshannessy.com>",
        "Kyle Davis <kyldvs@gmail.com>"
    ],
    "license": "BSD-3-Clause",
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
    "dependencies": {
        "fbemitter": "^2.0.0",
        "fbjs": "^0.8.0"
    },
    "peerDependencies": {
        "react": "^15.0.2"
    },
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
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
