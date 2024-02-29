# Starter Template for HTML/CSS/JS Development
Starter template.
***

## Structure
`/src/` - folder for source code

`/build/` - the final project will be assembled here

`/gulp/` - folder with tasks for [gulp](http://gulpjs.com/)
***

## Structure of src
`/fonts/` - fonts -> copied to `build/css/fonts`

`/img/` - images -> copied to `build/img`

`/img/icons/` - sprite is generated from all images in the folder -> sprite is saved in `build/img`, styles and mixins for sprites are saved in `/scss/lib/_sprite.sass`

`/img/svg/` - SVG font is generated from all images in the folder -> font is saved in `build/css/fonts`

`/js/` - JavaScript code

`/lib/` - all bower dependencies are stored here

`/partials/` - HTML templates, can be included using comments, [details here](https://www.npmjs.com/package/gulp-include)

`/scss/` - SCSS, [SCSS documentation](http://sass-lang.com/)
***

## Installation
+   Install [Ruby](https://www.ruby-lang.org/ru/downloads/)
+   Install gem dependencies [sass](http://sass-scss.ru/install/) and [scss-lint](https://github.com/brigade/scss-lint)

		$ gem install sass
		$ gem install scss_lint

+   Install [node.js](https://github.com/creationix/nvm)
+   Install bower and gulp globally
+   Download the repository and install npm i bower dependencies, executing the following commands in the project folder

		$ bower install
		$ npm install

+   Build the project and run gulp

		$ gulp build
		$ gulp

***

## Gulp Tasks

Gulp-cli tasks are described here [gulp cli doc](https://github.com/gulpjs/gulp/blob/master/docs/CLI.md)

Task Name      | Command to Run      | Description
------------- | -------------------- | -----
**copy**      | `gulp copy`          | Copy files from `src` to `build`
**html**      | `gulp html`          | Compile `html` files
**svgFont**   | `gulp svgFont`       | Generate an icon font from SVG images
**js**        | `gulp js`            | Compile, and minify `js` files
**jsLint**    | `gulp jsLint`        | Linting of `js` code
**sass**      | `gulp sass`          | Compile and minify `scss` and `sass`
**scssLint**  | `gulp scssLint`      | Linting of `scss` code
**server**    | `gulp server`        | Start the server
**sprite**    | `gulp sprite`        | Generate sprites from the `src/icons` folder, and generate styles and mixins for them in `/scss/lib/_sprite.sass`
**clean**     | `gulp clean`         | Clean the `build` folder
**default**   | `gulp`               | Run watchers for all files and recompile on changes
**build**     | `gulp build`         | Run all tasks for a complete project build
