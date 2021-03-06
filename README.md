# [Basis](https://packagist.org/packages/silverstripe-australia/ba-sis)

[![Build Status](https://travis-ci.org/silverstripe-australia/silverstripe-ba-sis.svg?branch=master)](https://travis-ci.org/silverstripe-australia/silverstripe-ba-sis)

Ba-SIS. **SilverStripe Australia** Standard Implementation Set. AKA, Basis.

The recommended module compilation for a base SilverStripe project, which provides the most common, and what we consider to be the most fundamental components when building an intuitive and flexible platform for both users and developers alike.

These module dependencies will be updated over time, so please keep an eye out for future releases!

## Travis Debugging

https://github.com/silverstripe-labs/silverstripe-travis-support#troubleshooting

To replicate the travis behaviour, you can do the following locally..

* export TRAVIS_REPO_SLUG=ba-sis
* export TRAVIS_BRANCH=master
* export TRAVIS_COMMIT=68ff4f59c16f65850e03d65cf0c60935e09c0b3a
* export CORE_RELEASE=3.2
* export DB=MYSQL
* git clone git@github.com:silverstripe-australia/silverstripe-ba-sis.git ba-sis
* cd ba-sis
* git checkout $TRAVIS_COMMIT
* git clone git://github.com/silverstripe-labs/silverstripe-travis-support.git ../travis-support
* php ../travis-support/travis_setup.php --source \`pwd\` --target ../travis
* cd ../travis
* vendor/bin/phpunit framework/tests
* vendor/bin/phpunit framework/admin/tests
* vendor/bin/phpunit cms/tests
* cd ..
* sudo rm -rf ba-sis
* sudo rm -rf travis-support
* sudo rm -rf travis
* unset TRAVIS_REPO_SLUG
* unset TRAVIS_BRANCH
* unset TRAVIS_COMMIT
* unset CORE_RELEASE
* unset DB
