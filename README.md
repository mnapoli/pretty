# My Awesome Project

A single command to run PHP code formatters like CodeSniffer or PHP-CS-Fixer.

## Why?

[PHP CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer) and [PHP-CS-Fixer](https://github.com/FriendsOfPHP/PHP-CS-Fixer) are powerful but using them is not simple. It is not always obvious which tool a project uses and whether there is a configuration file to use or whether you need to provide options to the CLI command.

Now it's easy, simply run:

```
pretty
```

*Pretty* will detect the configuration file that exist in the current directory and will run the correct tool.

If no configuration file exist, *Pretty* will run PHP-CS-Fixer with PSR-2 by default.

## Installation

TODO
