# VideoURLRecognizer

Recognize video service URL or code for embeding, and receive title, ebmed, description and preview in json format...

Implemented via:
* Symfony
* Twig
* PHPUnit

## Requirements
* PHP7.1 or above
* Composer

## Installation
1. `git clone https://github.com/someApprentice/filehosting.git`
1. `composer install`

### Adding a custom services
You may add a custom service by implementing following interfaces:

1. CheckerInterface

You also have to make checkURL(...) and checkEmbed(...) methods return an array like ['hosting' => "NAME_OF_HOSTING", 'type' => "URL"] or ['hosting' => "NAME_OF_HOSTING", 'type' => "embed"] in dependency of the method 

2. AbstractFactory
3. ParserInterface
4. AbstractResult

Tag your new Checker(s) in a `config/services.yaml` file or with a method `set(string $key, CheckerInterface  $checker)` in wherever you pleased

## Tests
Just simple run `'vendor/bin/phpunit'` in your console
