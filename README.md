# laravel-reference

Learn Laravel for PHP on MacOS :)

## Requirements

- Homebrew

## Installation (MacOS)

- Install composer | https://getcomposer.org/doc/00-intro.md

```
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === 'e0012edf3e80b6978849f5eff0d4b4e4c79ff1609dd1e613307e16318854d24ae64f26d17af3ef0bf7cfb710ca74755a') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
```

- Move `composer.phar` in to `/usr/local/bin/composer` to install globally:

```
mv composer.phar /usr/local/bin/composer
```

- Verify composer global

```
composer
```

- Install node.js | https://nodejs.org/en/download/

- Verify node.js

```
node -v
npm -v
```

- Install PHP

```
brew install php@7.x
```

> Specify PHP version to be installed. (brew install php@7.4)

- Install Laravel | https://laravel.com/docs/7.x/installation#installing-laravel

```
composer global require laravel/installer
```

> Issues:
>
> 1. `zsh: command not found: laravel`
>    ZSH won't expand the ~ on PATH. Try this instead:
>    `export PATH="$HOME/.composer/vendor/bin:$PATH"`

- Verify Laravel

```
laravel
```

- Install Laravel instance

```
laravel new <project_name>
```

## Project Setup

Install modules

```php
composer install
```

Create `.env` from `.env.example`

Run application

```php
php artisan serve
```

Generate a key

```php
php artisan key:generate
```

Navigate to: `http://127.0.0.1:8000/`
