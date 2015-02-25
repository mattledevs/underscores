Ready? Set. Go!
---------------

This is a powerhouse combo of the popularized Underscores for its lightweight Wordpress theme approach plus Gulp as the task runner neatly put together by @MattLePhoto.

Enjoy, tweak, springboard, change the world. 

Underscores Docs
---------------

![Travis CI Build Status](https://travis-ci.org/Automattic/_s.svg?branch=master)

_s
===

Hi. I'm a starter theme called `_s`, or `underscores`, if you like. I'm a theme meant for hacking so don't use me as a Parent Theme. Instead try turning me into the next, most awesome, WordPress theme out there. That's what I'm here for.

My ultra-minimal CSS might make me look like theme tartare but that means less stuff to get in your way when you're designing your awesome theme. Here are some of the other more interesting things you'll find here:

* A just right amount of lean, well-commented, modern, HTML5 templates.
* A helpful 404 template.
* A sample custom header implementation in `inc/custom-header.php` that can be activated by uncommenting one line in `functions.php` and adding the code snippet found in the comments of `inc/custom-header.php` to your `header.php` template.
* Custom template tags in `inc/template-tags.php` that keep your templates clean and neat and prevent code duplication.
* Some small tweaks in `inc/extras.php` that can improve your theming experience.
* A script at `js/navigation.js` that makes your menu a toggled dropdown on small screens (like your phone), ready for CSS artistry. It's enqueued in `functions.php`.
* 2 sample CSS layouts in `layouts/` for a sidebar on either side of your content.
* Smartly organized starter CSS in `style.css` that will help you to quickly get your design off the ground.
* Licensed under GPLv2 or later. :) Use it to make something cool.

Getting started
===

If you want to keep it simple, head over to http://underscores.me and generate your `_s` based theme from there. You just input the name of the theme you want to create, click the "Generate" button, and you get your ready-to-awesomize starter theme.

If you want to set things up manually, download `_s` from GitHub. The first thing you want to do is copy the `_s` directory and change the name to something else (like, say, `megatherium`), and then you'll need to do a five-step find and replace on the name in all the templates.

1. Search for `'_s'` (inside single quotations) to capture the text domain.
2. Search for `_s_` to capture all the function names.
3. Search for `Text Domain: _s` in style.css.
4. Search for <code>&nbsp;_s</code> (with a space before it) to capture DocBlocks.
5. Search for `_s-` to capture prefixed handles.

OR

* Search for: `'_s'` and replace with: `'megatherium'`
* Search for: `_s_` and replace with: `megatherium_`
* Search for: `Text Domain: _s` and replace with: `Text Domain: megatherium` in style.css.
* Search for: <code>&nbsp;_s</code> and replace with: <code>&nbsp;Megatherium</code>
* Search for: `_s-` and replace with: `megatherium-`

Then, update the stylesheet header in `style.css` and the links in `footer.php` with your own information. Next, update or delete this readme.

Install Packages with Bower
---------------
With Bower you can manage all your packages in one place and source control their versions. This step is optional. 

### Install Bower

Bower Site - http://bower.io/

#### 1. Install bower globally:

```sh
$ npm install -g bower
```

#### 2. Install bower dependencies in your project folder:

```sh
$ bower init
```

#### 3. Install any package you want:

```sh
$ bower install bootstrap-sass-official --save  
$ bower install fontawesome --save
```



Setting up Gulp
---------------
Underscores uses the task runner Gulp to compile everything nicely and neatly. Everything is configured to play nice with Underscores. Follow these command lines to get up and running with Gulp. 

### Install Gulp

Gulp Site - http://gulpjs.com/

#### 1. Install gulp globally:

```sh
$ npm install --global gulp
```

#### 2. Install gulp dependencies in your project:

```sh
$ npm install --save-dev gulp
```

#### 3. Download and install required node packages:

```sh
$ npm install gulp-bower gulp-sass gulp-autoprefixer gulp-minify-css gulp-jshint gulp-concat gulp-uglify gulp-imagemin gulp-notify gulp-rename gulp-livereload gulp-cache del --save-dev
```

#### 4. Run gulp:

```sh
$ gulp
```

Here are a few notable tasks you can run form this setup. To view the entire list, please view the package.json file. 

Tasks with Gulp
===

To gain the full benefits of Flint's Gulp setup, please see the following example commands: 

**Compiling and optimizing tasks:**

| Command   |      Task(s)      |
|----------|:-------------:|
| `styles` | Compile all *.scss* files in src/sass directory |
| `scripts` |    Compile all vendor and plugin *.js* files   |
| `images` |    Optimize images within the src/images directory   |
| **`default`** |    Run `styles`, `scripts`, and `images` simultaneously   |

**Automated tasks:**

| Command   |      Task(s)      |
|----------|:-------------:|
| `watch` |  Run Watch for *.scss*, *.js*, and *.html* () |
| `sync` |    Run Browser-Sync    |
