# generator-raadhuis [![Build Status](https://secure.travis-ci.org/raadhuis/generator-raadhuis.png?branch=master)](https://travis-ci.org/raadhuis/generator-raadhuis)

## Features

* CSS Autoprefixing
* Built-in preview server with LiveReload
* Automagically compile CoffeeScript & Sass
* Automagically lint your scripts
* Automagically wire up your Bower components with [grunt-wiredep](#third-party-dependencies).
* Awesome Image Optimization (via OptiPNG, pngquant, jpegtran and gifsicle)
* Mocha Unit Testing with PhantomJS
* Leaner Modernizr builds (Optional)

For more information on what `generator-webapp` can do for you, take a look at the [Grunt tasks](https://github.com/yeoman/generator-webapp/blob/master/app/templates/_package.json) used in our `package.json`.

## Getting Started

### What is Yeoman?

Not every new computer comes with a Yeoman pre-installed. He lives in the [npm](https://npmjs.org) package repository. You only have to ask for him once, then he packs up and moves into your hard drive. *Make sure you clean up, he likes new and shiny things.*

```bash
sudo npm install -g yo
```
If you'd like to get to know Yeoman better and meet some of his friends, [Grunt](http://gruntjs.com) and [Bower](http://bower.io), check out the complete [Getting Started Guide](https://github.com/yeoman/yeoman/wiki/Getting-Started).

### Using Yeoman RAADHUIS generator 

To install generator-raadhuis from npm, run:

```bash
sudo npm install -g generator-raadhuis
```

Finally, initiate the generator:

```bash
yo raadhuis
```

Beginning the development process by just type:
```bash
grunt serve
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

## License

[BSD license](http://opensource.org/licenses/bsd-license.php)

