# Laravel + Bootstrap

I got tired of setting up a Laravel project so I created a boilerplate that I clone everytime I need to create a [Laravel](https://laravel.com/) with [Bootstrap](https://getbootstrap.com/) project.

It's just basically a Laravel project. I just added Bootstrap via [npm](https://www.npmjs.com). WTF, don't judge.

## Contents

This project includes the following:

-   [Laravel](https://laravel.com/) version 6.0.x
-   [Bootsrap](https://getbootstrap.com/) version 4.3.x
-   [Browsersync](https://www.browsersync.io/) (lazy people's F5 &mdash; like me, hehe)
-   Pre-configured `.htaccess` on root directory
-   Pre-configured `webpack.mix.js` (+ versioning and Browsersync)
-   Automatically creates `.env` file and generates `APP_KEY` based on `.env.example` &mdash; (so don't delete this file)

That's all. Nothing fancy.

## Clone/ get a copy

```
git clone https://github.com/earvinpiamonte/laravel-bootstrap.git
```

## Install packages and update

First, change your directory to `laravel-bootstrap` &mdash; the one you just cloned.

```
cd laravel-bootstrap
```

Then, do composer update.

```
composer update
```

After that, do install Node.js modules.

```
npm install
```

## Compiling assets

Get the most out of Larvel by using their [Mix](https://laravel.com/docs/6.0/mix) that runs on top of [Webpack](https://webpack.js.org/). Pretty cool.

Run all Mix tasks

```
npm run dev
```

Run all Mix tasks and minify output

```
npm run prod
```

WANT TO AUTOMATICALLY RELOAD THE BROWSER WHEN YOU MAKE CHANGES ON THE SOURCE CODE?

Say no more fam. [Browsersync](https://www.browsersync.io/) is here.

First, update the `APP_URL` and `APP_PACKAGE` on your `.env` file. That's on line number 5 and 6.

You can change the `APP_URL` and `APP_PACKAGE` to your preference, depends on your setup. Please just check it out. It's a cool feature. Believe me.

After setting up the `APP_URL` and `APP_PACKAGE`, run:

```
npm run watch
```

The cool part here is when you modify a script or PHP file, watch as the browser instantly refreshes the page to reflect your changes.

I'm actually tired of typing things here so just go ahead and go to [Laravel Mix's](https://laravel.com/docs/6.0/mix) documentation.

## Contact

Found any issue or have some recommendation? Email me at [earvin.piamonte@gmail.com](mailto:earvin.piamonte@gmail.com).

Also, check out my [website](https://earvinpiamonte.com). It's built using React, Gatsby as the static site generator and deployed on Netlify.

### CTRL/CMD + F me:

GitHub - https://github.com/earvinpiamonte

GitHub Gist - https://gist.github.com/earvinpiamonte

CodePen - https://codepen.io/earvinpiamonte

Twitter - https://twitter.com/earvinpiamonte

LinkedIn - https://www.linkedin.com/in/earvinpiamonte

Website & Résumé - https://www.earvinpiamonte.com
