# api documentation for  [grunt-jsbeautifier (v0.2.13)](https://github.com/vkadam/grunt-jsbeautifier)  [![npm package](https://img.shields.io/npm/v/npmdoc-grunt-jsbeautifier.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-grunt-jsbeautifier) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-grunt-jsbeautifier.svg)](https://travis-ci.org/npmdoc/node-npmdoc-grunt-jsbeautifier)
#### jsbeautifier.org for grunt

[![NPM](https://nodei.co/npm/grunt-jsbeautifier.png?downloads=true)](https://www.npmjs.com/package/grunt-jsbeautifier)

[![apidoc](https://npmdoc.github.io/node-npmdoc-grunt-jsbeautifier/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-grunt-jsbeautifier_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-grunt-jsbeautifier/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-grunt-jsbeautifier/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-grunt-jsbeautifier/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Vishal Kadam",
        "email": "vishal.4kadam@gmail.com"
    },
    "bugs": {
        "url": "https://github.com/vkadam/grunt-jsbeautifier/issues"
    },
    "dependencies": {
        "async": "^2.0.0-rc.3",
        "grunt": ">=0.4.1",
        "js-beautify": ">=1.4.2",
        "lodash": ">=2.4.1",
        "rc": ">=0.5.5",
        "semver": ">=4.3.1",
        "underscore.string": ">=2.3.3"
    },
    "description": "jsbeautifier.org for grunt",
    "devDependencies": {
        "chai": "^1.9.2",
        "chai-fs": "^0.1.0",
        "grunt-contrib-clean": "^1.0.0",
        "grunt-contrib-copy": "^1.0.0",
        "grunt-contrib-jshint": "^1.0.0",
        "grunt-contrib-nodeunit": "^1.0.0",
        "grunt-dev-update": "^2.0.0",
        "grunt-mocha-test": "^0.12.1",
        "load-grunt-tasks": "^3.0.0",
        "mocha": ">1.20.0",
        "ncp": "^2.0.0"
    },
    "directories": {},
    "dist": {
        "shasum": "f3d41738fcb5f9984ef296d5beebc40489105642",
        "tarball": "https://registry.npmjs.org/grunt-jsbeautifier/-/grunt-jsbeautifier-0.2.13.tgz"
    },
    "engines": {
        "node": ">=0.8"
    },
    "gitHead": "681edeffbc76313bda2f6df0768e8bd529dc8d02",
    "homepage": "https://github.com/vkadam/grunt-jsbeautifier",
    "keywords": [
        "gruntplugin",
        "beautify",
        "beautifier",
        "jsbeautifier",
        "code-quality",
        "javascript beautify",
        "html beautify",
        "css beautify",
        "json beautify"
    ],
    "licenses": [
        {
            "type": "MIT",
            "url": "https://github.com/vkadam/grunt-jsbeautifier/blob/master/LICENSE-MIT"
        }
    ],
    "maintainers": [
        {
            "name": "vkadam",
            "email": "vishal.4kadam@gmail.com"
        }
    ],
    "name": "grunt-jsbeautifier",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/vkadam/grunt-jsbeautifier.git"
    },
    "scripts": {
        "test": "grunt test -v"
    },
    "version": "0.2.13"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module grunt-jsbeautifier](#apidoc.module.grunt-jsbeautifier)
1.  [function <span class="apidocSignatureSpan">grunt-jsbeautifier.</span>jsbeautifier (task)](#apidoc.element.grunt-jsbeautifier.jsbeautifier)
1.  object <span class="apidocSignatureSpan">grunt-jsbeautifier.</span>jsbeautifier.prototype

#### [module grunt-jsbeautifier.jsbeautifier](#apidoc.module.grunt-jsbeautifier.jsbeautifier)
1.  [function <span class="apidocSignatureSpan">grunt-jsbeautifier.</span>jsbeautifier (task)](#apidoc.element.grunt-jsbeautifier.jsbeautifier.jsbeautifier)
1.  [function <span class="apidocSignatureSpan">grunt-jsbeautifier.jsbeautifier.</span>registerWithGrunt (grunt)](#apidoc.element.grunt-jsbeautifier.jsbeautifier.registerWithGrunt)
1.  object <span class="apidocSignatureSpan">grunt-jsbeautifier.jsbeautifier.</span>DEFAULT_OPTIONS

#### [module grunt-jsbeautifier.jsbeautifier.prototype](#apidoc.module.grunt-jsbeautifier.jsbeautifier.prototype)
1.  [function <span class="apidocSignatureSpan">grunt-jsbeautifier.jsbeautifier.prototype.</span>run ()](#apidoc.element.grunt-jsbeautifier.jsbeautifier.prototype.run)



# <a name="apidoc.module.grunt-jsbeautifier"></a>[module grunt-jsbeautifier](#apidoc.module.grunt-jsbeautifier)

#### <a name="apidoc.element.grunt-jsbeautifier.jsbeautifier"></a>[function <span class="apidocSignatureSpan">grunt-jsbeautifier.</span>jsbeautifier (task)](#apidoc.element.grunt-jsbeautifier.jsbeautifier)
- description and source-code
```javascript
jsbeautifier = function (task) {
    // Store reference to original task
    this.task = task;
    var args = {};

    task.args.forEach(function(item, index) {
        if (index % 2 === 0) {
            args[item] = task.args[index + 1];
        }
    });
    this.args = args;

    // Merge task options with defaults
    this.options = task.options(JsBeautifierTask.DEFAULT_OPTIONS);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.grunt-jsbeautifier.jsbeautifier"></a>[module grunt-jsbeautifier.jsbeautifier](#apidoc.module.grunt-jsbeautifier.jsbeautifier)

#### <a name="apidoc.element.grunt-jsbeautifier.jsbeautifier.jsbeautifier"></a>[function <span class="apidocSignatureSpan">grunt-jsbeautifier.</span>jsbeautifier (task)](#apidoc.element.grunt-jsbeautifier.jsbeautifier.jsbeautifier)
- description and source-code
```javascript
jsbeautifier = function (task) {
    // Store reference to original task
    this.task = task;
    var args = {};

    task.args.forEach(function(item, index) {
        if (index % 2 === 0) {
            args[item] = task.args[index + 1];
        }
    });
    this.args = args;

    // Merge task options with defaults
    this.options = task.options(JsBeautifierTask.DEFAULT_OPTIONS);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grunt-jsbeautifier.jsbeautifier.registerWithGrunt"></a>[function <span class="apidocSignatureSpan">grunt-jsbeautifier.jsbeautifier.</span>registerWithGrunt (grunt)](#apidoc.element.grunt-jsbeautifier.jsbeautifier.registerWithGrunt)
- description and source-code
```javascript
registerWithGrunt = function (grunt) {
    grunt.registerMultiTask("jsbeautifier", "jsbeautifier.org for grunt", function() {
        var task = new JsBeautifierTask(this);
        task.run();
    });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.grunt-jsbeautifier.jsbeautifier.prototype"></a>[module grunt-jsbeautifier.jsbeautifier.prototype](#apidoc.module.grunt-jsbeautifier.jsbeautifier.prototype)

#### <a name="apidoc.element.grunt-jsbeautifier.jsbeautifier.prototype.run"></a>[function <span class="apidocSignatureSpan">grunt-jsbeautifier.jsbeautifier.prototype.</span>run ()](#apidoc.element.grunt-jsbeautifier.jsbeautifier.prototype.run)
- description and source-code
```javascript
run = function () {
    var options = this.options,
        args = this.args;

    var fileCount = 0,
        changedFileCount = 0,
        unVerifiedFiles = [];

    function verifyActionHandler(src) {
        unVerifiedFiles.push(src);
    }

    function verifyAndWriteActionHandler(src, result) {
        grunt.verbose.writeln(options.dest + src);
        grunt.file.write(options.dest + src, result);
        changedFileCount++;
    }

    function convertCamelCaseToUnderScore(config) {
        var underscoreKey;
        _.forEach([config.js, config.css, config.html], function(conf) {
            _.forEach(conf, function(value, key) {
                underscoreKey = stringUtils.underscored(key);
                if ("fileTypes" !== key && key !== underscoreKey) {
                    conf[underscoreKey] = value;
                    delete conf[key];
                }
            });
        });
    }

    function getConfig() {
        var config,
            rcFile = require("rc")("jsbeautifier", {});

        if (options.config || !_.isEqual(rcFile, {})) {
            var baseConfig = options.config ? grunt.file.readJSON(path.resolve(options.config)) : rcFile;
            config = {
                js: {},
                css: {},
                html: {}
            };
            if (!baseConfig.js && !baseConfig.css && !baseConfig.html) {
                _.extend(config.js, baseConfig);
                _.extend(config.css, baseConfig);
                _.extend(config.html, baseConfig);
            }
            _.extend(config.js, baseConfig.js);
            _.extend(config.css, baseConfig.css);
            _.extend(config.html, baseConfig.html);
            _.extend(config.js, options.js);
            _.extend(config.css, options.css);
            _.extend(config.html, options.html);
        } else {
            config = options;
        }
        config.js.fileTypes = _.union(config.js.fileTypes, [".js", ".json", '.es6']);
        config.css.fileTypes = _.union(config.css.fileTypes, [".css"]);
        config.html.fileTypes = _.union(config.html.fileTypes, [".html"]);

        grunt.verbose.writeln("Beautify config before converting camelcase to underscore: " + JSON.stringify(config));

        convertCamelCaseToUnderScore(config);

        grunt.verbose.writeln("Using beautify config: " + JSON.stringify(config));
        return config;
    }

    var sourceFiles = this.task.files,
        done = this.task.async();
    if ((sourceFiles && sourceFiles.length > 0) || !_.isEmpty(args.file)) {
        if (!_.isEmpty(options.dest)) {
            grunt.verbose.writeln("All beautified files will be stored under \"" + options.dest + "\" folder");
            if (!stringUtils.endsWith(options.dest, "/")) {
                options.dest += "/";
            }
        }

        grunt.verbose.writeln("Using mode=\"" + options.mode + "\"...");
        var actionHandler = "VERIFY_ONLY" === options.mode ? verifyActionHandler : verifyAndWriteActionHandler,
            config = getConfig();

<span class="apidocCodeCommentSpan">        /** Add new line for js file unless specified as false */
</span>        addJsNewLine = config.js.end_with_newline !== false;

        jsBeautifyVersion(options.jsBeautifyVersion, function(error) {
            if (error) {
                grunt.fail.fatal("Unable to update js-beautify version to " + options.jsBeautifyVersion + " due to \n" + error);
                return done(error);
            }
            var q = async.queue(function(src, callback) {
                if (grunt.file.isDir(src)) {
                    callback();
                    return;
                }

                beautify(src, config, actionHandler);
                fileCount++;
                callback();
            }, 10);

            q.drain = function() {
                if (unVerifiedFiles.length) {
                    grunt.fail.warn("The following files are not beautified:\n" + unVerifiedFiles.join("\n").cyan + "\n");
                }
                grunt.log.write("Beautified " + fileCount.toString().cyan + " files, changed " + changedFileCount.toString().cyan ...
```
- example usage
```shell
...
 * Static method for registering an instance of the task with Grunt.
 *
 * @param {*} grunt
 */
JsBeautifierTask.registerWithGrunt = function(grunt) {
grunt.registerMultiTask("jsbeautifier", "jsbeautifier.org for grunt", function() {
    var task = new JsBeautifierTask(this);
    task.run();
});
};

function getFileType(file, config) {
var fileType = null,
    fileMapping = {
        "js": config.js.fileTypes,
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
