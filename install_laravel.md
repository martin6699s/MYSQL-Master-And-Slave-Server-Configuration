
➜  ~ git:(master) ✗ php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
➜  Master-Slave git:(master) ✗ php composer-setup.php
➜  Master-Slave git:(master) ✗ php -r "unlink('composer-setup.php');"
➜  Master-Slave git:(master) ✗ php composer.phar
➜  Master-Slave git:(master) ✗ vim composer.json
```
{
    "name": "laravel/laravel",
    "description": "The Laravel Framework.",
    "keywords": ["framework", "laravel"],
    "license": "MIT",
    "type": "project",
    "require": {
        "php": ">=5.5.9",
        "laravel/framework": "5.1.*"
    },
    "config": {
        "preferred-install": "dist"
    },
    "repositories": {
        "packagist": {
            "type": "composer",
            "url": "https://packagist.phpcomposer.com"
        }
    }
}
```

➜  Master-Slave git:(master) ✗ composer install

➜  Master-Slave git:(master) ✗ composer create-project laravel/laravel datainstead "5.1.*"
Installing laravel/laravel (v5.1.33)
  - Installing laravel/laravel (v5.1.33) Downloading: 100%
Created project in datainstead
> php -r "copy('.env.example', '.env');"
Loading composer repositories with package information
Updating dependencies (including require-dev)
Package operations: 59 installs, 0 updates, 0 removals
  - Installing vlucas/phpdotenv (v1.1.1) Loading from cache
  - Installing symfony/var-dumper (v2.7.25) Loading from cache
  - Installing symfony/translation (v2.7.25) Loading from cache
  - Installing symfony/routing (v2.7.25) Loading from cache
  - Installing symfony/process (v2.7.25) Loading from cache
  - Installing psr/log (1.0.2) Loading from cache
  - Installing symfony/debug (v2.7.25) Loading from cache
  - Installing symfony/polyfill-mbstring (v1.3.0) Loading from cache
  - Installing symfony/http-foundation (v2.7.25) Loading from cache
  - Installing symfony/event-dispatcher (v2.8.18) Loading from cache
  - Installing symfony/http-kernel (v2.7.25) Loading from cache
  - Installing symfony/finder (v2.7.25) Loading from cache
  - Installing symfony/dom-crawler (v2.7.25) Loading from cache
  - Installing symfony/css-selector (v2.8.18) Loading from cache
  - Installing symfony/console (v2.7.25) Loading from cache
  - Installing swiftmailer/swiftmailer (v5.4.6) Loading from cache
  - Installing jakub-onderka/php-console-color (0.1) Loading from cache
  - Installing jakub-onderka/php-console-highlighter (v0.3.2) Loading from cache
  - Installing dnoegel/php-xdg-base-dir (0.1) Loading from cache
  - Installing nikic/php-parser (v2.1.1) Loading from cache
  - Installing psy/psysh (v0.7.2) Loading from cache
  - Installing paragonie/random_compat (v1.4.2) Loading from cache
  - Installing nesbot/carbon (1.22.1) Loading from cache
  - Installing mtdowling/cron-expression (v1.2.0) Loading from cache
  - Installing monolog/monolog (1.22.1) Loading from cache
  - Installing league/flysystem (1.0.37) Loading from cache
  - Installing symfony/polyfill-util (v1.3.0) Loading from cache
  - Installing symfony/polyfill-php56 (v1.3.0) Loading from cache
  - Installing jeremeamia/superclosure (2.3.0) Loading from cache
  - Installing doctrine/inflector (v1.1.0) Loading from cache
  - Installing danielstjules/stringy (1.10.0) Loading from cache
  - Installing classpreloader/classpreloader (3.1.0) Loading from cache
  - Installing laravel/framework (v5.1.46) Downloading: 100%
  - Installing fzaninotto/faker (v1.6.0) Loading from cache
  - Installing hamcrest/hamcrest-php (v1.2.2) Loading from cache
  - Installing mockery/mockery (0.9.9) Loading from cache
  - Installing symfony/yaml (v3.2.6) Loading from cache
  - Installing sebastian/version (1.0.6) Downloading: 100%
  - Installing sebastian/global-state (1.1.1) Loading from cache
  - Installing sebastian/recursion-context (1.0.5) Downloading: 100%
  - Installing sebastian/exporter (1.2.2) Downloading: 100%
  - Installing sebastian/environment (1.3.8) Downloading: 100%
  - Installing sebastian/diff (1.4.1) Loading from cache
  - Installing sebastian/comparator (1.2.4) Loading from cache
  - Installing doctrine/instantiator (1.0.5) Loading from cache
  - Installing phpunit/php-text-template (1.2.1) Loading from cache
  - Installing phpunit/phpunit-mock-objects (2.3.8) Downloading: 100%
  - Installing phpunit/php-timer (1.0.9) Loading from cache
  - Installing phpunit/php-file-iterator (1.4.2) Loading from cache
  - Installing phpunit/php-token-stream (1.4.11) Loading from cache
  - Installing phpunit/php-code-coverage (2.2.4) Downloading: 100%
  - Installing webmozart/assert (1.2.0) Loading from cache
  - Installing phpdocumentor/reflection-common (1.0) Loading from cache
  - Installing phpdocumentor/type-resolver (0.2.1) Loading from cache
  - Installing phpdocumentor/reflection-docblock (3.1.1) Loading from cache
  - Installing phpspec/prophecy (v1.7.0) Loading from cache
  - Installing phpunit/phpunit (4.8.35) Downloading: 100%
  - Installing phpspec/php-diff (v1.0.2) Downloading: 100%
  - Installing phpspec/phpspec (2.5.5) Downloading: 100%
symfony/var-dumper suggests installing ext-symfony_debug ()
symfony/translation suggests installing symfony/config ()
symfony/routing suggests installing doctrine/annotations (For using the annotation loader)
symfony/routing suggests installing symfony/config (For using the all-in-one router or any loader)
symfony/routing suggests installing symfony/expression-language (For using expression matching)
symfony/event-dispatcher suggests installing symfony/dependency-injection ()
symfony/http-kernel suggests installing symfony/browser-kit ()
symfony/http-kernel suggests installing symfony/class-loader ()
symfony/http-kernel suggests installing symfony/config ()
symfony/http-kernel suggests installing symfony/dependency-injection ()
psy/psysh suggests installing ext-pdo-sqlite (The doc command requires SQLite to work.)
paragonie/random_compat suggests installing ext-libsodium (Provides a modern crypto API that can be used to generate random bytes.)
monolog/monolog suggests installing aws/aws-sdk-php (Allow sending log messages to AWS services like DynamoDB)
monolog/monolog suggests installing doctrine/couchdb (Allow sending log messages to a CouchDB server)
monolog/monolog suggests installing ext-amqp (Allow sending log messages to an AMQP server (1.0+ required))
monolog/monolog suggests installing ext-mongo (Allow sending log messages to a MongoDB server)
monolog/monolog suggests installing graylog2/gelf-php (Allow sending log messages to a GrayLog2 server)
monolog/monolog suggests installing mongodb/mongodb (Allow sending log messages to a MongoDB server via PHP Driver)
monolog/monolog suggests installing php-amqplib/php-amqplib (Allow sending log messages to an AMQP server using php-amqplib)
monolog/monolog suggests installing php-console/php-console (Allow sending log messages to Google Chrome)
monolog/monolog suggests installing rollbar/rollbar (Allow sending log messages to Rollbar)
monolog/monolog suggests installing ruflin/elastica (Allow sending log messages to an Elastic Search server)
monolog/monolog suggests installing sentry/sentry (Allow sending log messages to a Sentry server)
league/flysystem suggests installing league/flysystem-aws-s3-v2 (Allows you to use S3 storage with AWS SDK v2)
league/flysystem suggests installing league/flysystem-aws-s3-v3 (Allows you to use S3 storage with AWS SDK v3)
league/flysystem suggests installing league/flysystem-azure (Allows you to use Windows Azure Blob storage)
league/flysystem suggests installing league/flysystem-cached-adapter (Flysystem adapter decorator for metadata caching)
league/flysystem suggests installing league/flysystem-copy (Allows you to use Copy.com storage)
league/flysystem suggests installing league/flysystem-dropbox (Allows you to use Dropbox storage)
league/flysystem suggests installing league/flysystem-eventable-filesystem (Allows you to use EventableFilesystem)
league/flysystem suggests installing league/flysystem-rackspace (Allows you to use Rackspace Cloud Files)
league/flysystem suggests installing league/flysystem-sftp (Allows you to use SFTP server storage via phpseclib)
league/flysystem suggests installing league/flysystem-webdav (Allows you to use WebDAV storage)
league/flysystem suggests installing league/flysystem-ziparchive (Allows you to use ZipArchive adapter)
laravel/framework suggests installing aws/aws-sdk-php (Required to use the SQS queue driver and SES mail driver (~3.0).)
laravel/framework suggests installing doctrine/dbal (Required to rename columns and drop SQLite columns (~2.4).)
laravel/framework suggests installing guzzlehttp/guzzle (Required to use the Mailgun and Mandrill mail drivers and the ping methods on schedules (~5.3|~6.0).)
laravel/framework suggests installing iron-io/iron_mq (Required to use the iron queue driver (~2.0).)
laravel/framework suggests installing league/flysystem-aws-s3-v3 (Required to use the Flysystem S3 driver (~1.0).)
laravel/framework suggests installing league/flysystem-rackspace (Required to use the Flysystem Rackspace driver (~1.0).)
laravel/framework suggests installing pda/pheanstalk (Required to use the beanstalk queue driver (~3.0).)
laravel/framework suggests installing predis/predis (Required to use the redis cache and queue drivers (~1.0).)
laravel/framework suggests installing pusher/pusher-php-server (Required to use the Pusher broadcast driver (~2.0).)
laravel/framework suggests installing symfony/psr-http-message-bridge (Required to psr7 bridging features (0.2.*).)
sebastian/global-state suggests installing ext-uopz (*)
phpunit/php-code-coverage suggests installing ext-xdebug (>=2.2.1)
phpunit/phpunit suggests installing phpunit/php-invoker (~1.1)
phpspec/phpspec suggests installing phpspec/nyan-formatters (~1.0 – Adds Nyan formatters)
Writing lock file
Generating autoload files
> Illuminate\Foundation\ComposerScripts::postUpdate
> php artisan optimize
Generating optimized class loader
> php artisan key:generate
Application key [eQtWYPWP5ug2v6xLnkYocJDLeHJKvzzP] set successfully.

➜  datainstead git:(master) ✗ sudo chmod -R 775 ./storage
