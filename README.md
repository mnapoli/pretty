[![](https://hc4rcprbe1.execute-api.eu-west-1.amazonaws.com/dev?name=mnapoli/pretty)](https://prettyci.com/)

**A single CLI command with sane defaults to simplify CodeSniffer and PHP-CS-Fixer.**

---

[PHP CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer) and [PHP-CS-Fixer](https://github.com/FriendsOfPHP/PHP-CS-Fixer) are powerful but using them is not simple. It is not always obvious which tool a project uses and whether there is a configuration file to use or whether you need to provide options to the CLI command.

Now it's easy, simply run:

```
pretty
```

*Pretty* will detect the configuration file that exist in the current directory and will run the correct tool. If no configuration file exist, *Pretty* will run PHP CodeSniffer with PSR-2 by default.

If errors are found, simply run:

```
pretty fix
```

Again, *Pretty* will run the appropriate tool (`php-cs-fixer` or `phpcbf`) to fix as many errors as possible in your code.

## Installation

If you have already [set up a global install of Composer](http://akrabat.com/php/global-installation-of-php-tools-with-composer/) just run:

```
composer global require mnapoli/pretty
```

*Pretty* comes with no dependencies so it should not bring any conflict in Composer.

You can also install it as a local dependency of your project with `composer require mnapoli/pretty`. In that case you can start the tool with `vendor/bin/pretty`.

You will be able to update to new versions by running:

```
composer global update mnapoli/pretty
```

## Usage

Running an analysis is as simple as running:

```
pretty
```

This command will not change any code. To fix errors reported by this command, simply run:

```
pretty fix
```

In case you are running the analyses in CI you might want to run:

```
pretty ci
```

This will disable the caching option of PHP-CS-Fixer or CodeSniffer (because the cache will not be kept in CI).

## Hosted continuous integration

If you are using `pretty` in your daily development workflow you may be interested in [PrettyCI.com](https://prettyci.com/), the SaaS version of `pretty`.
