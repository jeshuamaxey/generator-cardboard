# Generator Cardboard [![Build Status](https://secure.travis-ci.org/jeshuamaxey/generator-cardboard.svg?branch=master)](http://travis-ci.org/jeshuamaxey/generator-cardboard)

[Yeoman](http://yeoman.io) generator that scaffolds out a web app complete with a virtual reality environment built with [THREE.js](http://threejs.org) which is [Google Cardboard](http://g.co/cardboard) compatible.

An example of what is generated out of the box can be found at [http://jeshua.co/labs/demos/generator-cardboard/](http://jeshua.co/labs/demos/generator-cardboard/).

![](http://i.imgur.com/ojYuQtb.png)

## Features

* CSS Autoprefixing
* Built-in preview server with LiveReload
* Automagically compile Sass
* Automagically lint your scripts
* Automagically wire up your Bower components with [grunt-wiredep](#third-party-dependencies).
* Awesome Image Optimization (via OptiPNG, pngquant, jpegtran and gifsicle)
* Mocha Unit Testing with PhantomJS
* Bootstrap for Sass (Optional)
* Leaner Modernizr builds (Optional)

## Getting Started

- Install: `npm install -g generator-cardboard`
- Run: `yo cardboard`
- Run `grunt` for building and `grunt serve` for preview. `--allow-remote` option for remote access.

#### Directory Structure

Below is an incomplete listing of the generated directory structure. The `vr/` directory is what is generated when the single empty scene VR environment is chosen, the source for which can be found [here](http://vr.chromeexperiments.com/).

```
├── app                   # contains all publicly accessible files 
│   ├── css               # site css
│   │   └── main.css
│   ├── js                # site javascript
│   │   ├── main.js
│   │   └── util.js
│   ├── vr                # contains the files for your VR application
│   │   ├── js
│   │   │   └── third-party
│   │   │       └── threejs
│   │   │           ├── DeviceOrientationControls.js
│   │   │           ├── OrbitControls.js
│   │   │           ├── StereoEffect.js
│   │   │           └── three.js
│   │   ├── textures
│   │   │   └── patterns
│   │   │       └── checker.png
│   └── index.html        # site landing page
├── test                  # tests
│   ├── spec
│   │   └── test.js
│   └── index.html
└── Gruntfile.js          # defines build tasks
```

#### Third-Party Dependencies

*(HTML/CSS/JS/Images/etc)*

Third-party dependencies are managed with [grunt-wiredep](https://github.com/stephenplusplus/grunt-wiredep). Add new dependencies using **Bower** and then run the **Grunt** task to load them:

```sh
$ bower install --save jquery
$ grunt wiredep
```

This works if the package author has followed the [Bower spec](https://github.com/bower/bower.json-spec). If the files are not automatically added to your source code, check with the package's repo for support and/or file an issue with them to have it updated.

To manually add dependencies, `bower install --save depName` to get the files, then add a `script` or `style` tag to your `index.html` or another appropriate place.

The components are installed in the root of the project at `/bower_components`. To reference them from index.html, use `src="bower_components"` or `src="/bower_components"`. Treat the `bower_components` directory as if it was a sibling to `index.html`.

*Testing Note*: a project checked into source control and later checked out needs to have `bower install` run from the `test` folder as well as from the project root.

## Options

* `--skip-install`

  Skips the automatic execution of `bower` and `npm` after scaffolding has finished.

* `--test-framework=<framework>`

  Defaults to `mocha`. Can be switched for another supported testing framework like `jasmine`.


## Contribute

See the [contributing docs](https://github.com/jeshuamaxey/generator-cardboard/blob/master/contributing.md).

## License

[BSD license](http://opensource.org/licenses/bsd-license.php)
