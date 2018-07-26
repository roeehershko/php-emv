# PHP EMV

A collection of EMV tools and utilities for PHP 5.3+

**This is a fork of Massimo Lombardo's [project][ORIGIN]**

## Installation

The recommended way to install PHP EMV is through [Composer][COMPOSER]:

```json
{
    "require": {
        "billpocket/php-emv": "@stable"
    }
}
```

```bash
$ composer install
```

## Basic Usage

For parse from string (codec by HEX):

```php
{
    use \EMV\Codec;
    
    $codecObj = new Codec();
    
    $codecObj->unserialize($hexTLV); //this returns an array
    
}
```



[COMPOSER]: https://getcomposer.org/
[PACKAGIST_VERSION]: https://packagist.org/packages/unwiredbrain/php-emv

## Testing

PHP EMV comes with a full-fledged test suite. To run it, install [PHPUnit][PHPUNIT] via [Composer][COMPOSER]:

```bash
$ composer install --dev
$ php vendor/bin/phpunit
```

[PHPUNIT]: http://phpunit.de/
[COMPOSER]: https://getcomposer.org/

## Contributing

Here are a few basic rules so that nobody gets grumpy:

* every pull request MUST follow the [basic coding standars][PSR1], the [coding style guide][PSR2] and, where applicable, the [improved autoloding][PSR4] recommendations by the [PHP-FIG][PHPFIG].
* the unit tests MUST be written or updated
* the test suite MUST succeed entirely
* the documentation MUST be written or updated
* commit messages MUST [make sense][COMMITS]
* the pull request branch MUST be [rebased][REBASING] against the latest `master` branch
* useless commits MUST be [squashed][SQUASHING]

[PSR1]: http://www.php-fig.org/psr/psr-1
[PSR2]: http://www.php-fig.org/psr/psr-2
[PSR4]: http://www.php-fig.org/psr/psr-4
[PHPFIG]: http://www.php-fig.org/
[COMMITS]: http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html
[REBASING]: http://git-scm.com/book/en/Git-Branching-Rebasing
[SQUASHING]: http://gitready.com/advanced/2009/02/10/squashing-commits-with-rebase.html
[ORIGIN]: https://github.com/unwiredbrain/php-emv

## Credits

* [Massimo Lombardo][CREDITS_ML], original author
* [Open source community][CREDITS_OSC]

[CREDITS_ML]: https://github.com/unwiredbrain
[CREDITS_OSC]: https://github.com/unwiredbrain/emv-utils/graphs/contributors

## License

PHP EMV is released under the MIT license. See the bundled `LICENSE` file for details.
