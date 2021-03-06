## Hifone

[![StyleCI](https://styleci.io/repos/60775510/shield)](https://styleci.io/repos/60775510/)
[![Build Status](https://img.shields.io/travis/Hifone/Hifone/master.svg?style=flat-square)](https://travis-ci.org/Hifone/Hifone)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE)

![Screenshot](https://camo.githubusercontent.com/d0e2887410b6c68b84707412b9235950c58cefa1/687474703a2f2f363438322e636f6d2f6869666f6e65322e706e67)

Hifone is a free, open-source, self-hosted forum software based on the Laravel PHP Framework.

## Features

This package is currently in (very-)alpha stage, so all of the following features may or may not work yet. However, feel free to post issues and features requests [here](https://github.com/Hifone/Hifone/issues) . We will try to fix and improve the package as fast as we can based on your help!

* Fast and simple
* Beautiful and responsive
* Roles & Permissions
* Markdown & Emoj
* Image upload
* Avatars
* Notifications
* RSS Feeds
* Localization: language files, time zone and UTF-8 support

## Requirements

There are a few things that you will need to have set up in order to run Gitamin:

- A web server: **Nginx**, **Apache** (with mod_rewrite), or **Lighttpd**
- **PHP 5.6.4+** with the following extensions: mbstring, pdo_mysql
- **MySQL** or **PostgreSQL**
- **Composer**

## Installation

By default Hifone comes with a .env.example file. You'll need to rename this file to just .env regardless of what environment you're working on.

If you're using SQLite then your .env file should not contain a DB_HOST key. You'll also need to touch ./database/hifone.sqlite and give it the required permissions.

Directories within the `storage` and the `bootstrap/cache` directories should be writable by your web server or Hifone will not run. 


### Step 1: Shell

```shell
git clone https://github.com/Hifone/Hifone
cd Hifone

cp .env.example .env
vi .env  # write database settings

composer install --no-dev -o

php artisan hifone:install

chmod -R 777 storage
chmod -R 777 bootstrap/cache
```

### Step 2: Browser

Now go to http://your_site_domain/ and have fun!


## Development

These extra dependencies are required to develop Hifone:

- Node.js
- Bower
- Gulp

```shell
npm install
bower install
gulp
```

If you're making a lot of changes, you'll find that running `gulp watch` will really help you out!

## Demo

[Hifone website](http://hifone.com/).

## License

Hifone is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT)
