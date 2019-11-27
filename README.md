# Laravel + Bootstrap

I got tired of setting up a Laravel project so I created a boilerplate that I clone everytime I need to create a [Laravel](https://laravel.com/) with [Bootstrap](https://getbootstrap.com/) project.

## Contents

This project includes the following:

-   [Laravel](https://laravel.com/) version 6.x
-   [Bootsrap](https://getbootstrap.com/) version 4.3.x
-   Uses [Laravel Homestead](https://laravel.com/docs/6.x/homestead)!!!
-   [Browsersync](https://www.browsersync.io/) (lazy people's F5 &mdash; like me, hehe)
-   Pre-configured `webpack.mix.js` (+ versioning and Browsersync)

That's all. Nothing fancy.

## Clone/ get a copy

```
git clone https://github.com/earvinpiamonte/laraboots.git
```

## Install packages and update

First, change your directory to `laraboots` &mdash; the one you just cloned.

```
cd laraboots
```

Then, execute the following commands:

```bash
composer update
```

```bash
php vendor/bin/homestead make
```

Don't forget!

Please update `map` value under `sites:` to the following on `Homestead.yaml`:

eg.

```bash
sites:
    - map: laraboots.local
      to: /home/vagrant/code/public
```

This is important.

```bash
vagrant up
```

```bash
vagrant reload --provision
```

## Connect via SSH

```bash
vagrant ssh
```

## Compiling assets

While connected via SSH, change the directory to `~/code/` and install Node modules:

```bash
cd code/
```

```bash
npm install
```

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

First, update the `MIX_SENTRY_DSN_PUBLIC` file on your `.env` file, matching the assigned hostname on the `- map` of your `Homestead.yaml`.

eg. from `Homestead.yaml`

```yaml
sites:
    - map: laraboots.local
      to: /home/vagrant/code/public
```

Therefore, your `MIX_SENTRY_DSN_PUBLIC` should be set to `http://laraboots.local`.

After setting up the `MIX_SENTRY_DSN_PUBLIC` correctly, run the following (still connected via SSH):

```
npm run serve
```

Open your browser and enter `http://laraboots.local:3000`. The files are now on watch. Take note of the port!

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
