**A single command to run PHP code formatters like CodeSniffer or PHP-CS-Fixer.**

---

[PHP CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer) and [PHP-CS-Fixer](https://github.com/FriendsOfPHP/PHP-CS-Fixer) are powerful but using them is not simple. It is not always obvious which tool a project uses and whether there is a configuration file to use or whether you need to provide options to the CLI command.

Now it's easy, simply run:

```
pretty
```

*Pretty* will detect the configuration file that exist in the current directory and will run the correct tool.

If no configuration file exist, *Pretty* will run PHP-CS-Fixer with PSR-2 by default.

## Installation

If you have already [set up a global install of Composer](http://akrabat.com/php/global-installation-of-php-tools-with-composer/) just run:

```
composer global require mnapoli/pretty
```

*Pretty* comes with no dependencies so it should not bring any conflict in Composer.

You can also install it as a local dependency of your project with `composer require mnapoli/pretty`. In that case you can start the tool with `vendor/bin/pretty`.
