# Statesman meme generator

[![Built with Grunt](https://cdn.gruntjs.com/builtwith.png)](http://gruntjs.com/)

The Statesman's meme generator is a lightly-modified fork of the [Vox meme generator](https://github.com/voxmedia/meme). It has been modified to work without Ruby (except Compass, which is required to run the build process).

Assets are now built using Grunt, which transpiles the SASS files and concatenates/minifies the JavaScript. We modified the app this way to make it more easily deployable on our internal infrastructure.

To assist in development, the default Grunt task also:
  * launches a local server at `http://localhost:8000/`
  * starts `grunt-contrib-watch` to watch `index.html` and the .js files in `/source`
  * Livereload is enabled if you are running the [browser extenstions](http://livereload.com/extensions/)]].

![screenshot](readme.png)

## Deploying

Statesman images, fonts, etc. are currently in the app so you'll need to follow the steps below to customize the app for your use:

1. Edit the settings file at `source/javascripts/settings.js`.
2. Add any fonts you'll need at `source/stylesheets/_fonts.scss`.
3. `npm install`
4. `gem install compass`
5. Run `grunt`

A local server should open at `http://localhost:8000/` where you can use the tool locally.

We run the project through [GitHub pages](https://pages.github.com/) to allow access to the newsroom. We deploy this with `git push origin master:gh-pages`.

See the original repo at https://github.com/voxmedia/meme for additional info.
