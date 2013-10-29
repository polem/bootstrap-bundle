[BraincraftedBootstrapBundle](http://bootstrap.braincrafted.com)
=================

By [Florian Eckerstorfer](http://florianeckerstorfer.com)

[![Build Status](https://secure.travis-ci.org/braincrafted/bootstrap-bundle.png)](http://travis-ci.org/braincrafted/bootstrap-bundle)

## BraincraftedBootstrapBundle 2.0 is in an early development phase


About
-----

BraincraftedBootstrapBundle is [Bootstrap, from Twitter](http://twitter.github.com/bootstrap/) encapsulated in a [Symfony2](http://symfony.com) bundle.

This bundle is highly opiniated by how I use Twitter Bootstrap and Symfony.


Installation
------------

First you need to add `braincrafted/bootstrap-bundle` to `composer.json`:

    {
       "require": {
            "braincrafted/bootstrap-bundle": "dev-master"
        }
    }

Please note that `dev-master` points to the latest release. If you want to use the latest development version please use `dev-develop`. Of course you can also use an explicit version number, e.g., `2.0.*`.

You also have to add `BraincraftedBootstrapBundle` to your `AppKernel.php`:

    // app/AppKernel.php
    ...
    class AppKernel extends Kernel
    {
        ...
        public function registerBundles()
        {
            $bundles = array(
                ...
                new Braincrafted\Bundle\BootstrapBundle\BraincraftedBootstrapBundle()
            );
            ...

            return $bundles;
        }
        ...
    }


Download Assets
---------------

This bundle does no longer contain the asset files from Twitter Bootstrap (images, stylesheets and JavaScripts). The best way to include those assets is to add Twitter Bootstrap to your `composer.json`:

    {
       "require": {
            "twbs/bootstrap": "3.0.*"
        }
    }

You can find a detailed description in the documentation.


More Information
----------------

Check out the [documentation](http://bootstrap.braincrafted.com) to find out how you can use BraincraftedBootstrapBundle in your Symfony2 project.


Compatibility
-------------

- **BraincraftedBootstrapBundle v1.3.***
    - Twitter Bootstrap v2.3.*
    - jQuery v1.9.*
    - Symfony 2.2.*
- **BraincraftedBootstrapBundle v1.4.***
    - Twitter Bootstrap v2.3.*
    - jQuery v1.9.*
    - Symfony 2.2.*
- **BraincraftedBootstrapBundle v2.0**
    - Bootstrap v3.0.*
    - jQuery v1.10.*
    - Symfony v2.3.*


Changelog
---------

## Version 2.0.0

- Updated to Bootstrap v3.0.0
- Updated to jQuery v1.10.2
- Remove `include_responsive` option because Bootstrap 3.0.0 no longer has a not responsive version
- Added `boostrap_money` form type that uses Bootstraps prepend or append style to display the currency
- `percent` form type uses Bootstraps append style to display the percent sign
- Changed namespace back to `Braincrafted\Bundle\BootstrapBundle`
- Support for custom `variables.less`

### Version 1.4.0

- Changed namespace to `Braincrafted\Bundle\BootstrapBundle`
- Automatically configure Twig
- Automatically configure KnpMenuBundle
- Automatically configure KnpPaginatorBundle
- Automatically configure Assetic
- Improved layout of error messages in compound fields
- Improved code style (usage of PHP_CodeSniffer and PHPMD)
- Support for `data-prototype` option in collection fields
- Helper and template for flash messages

License
-------

- The bundle is licensed under the [MIT License](http://opensource.org/licenses/MIT)
- The CSS and Javascript from the Twitter Bootstrap are licensed under the [Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0)
