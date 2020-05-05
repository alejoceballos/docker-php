# Symfony Bundles

- [Symfony Maker](SYMFONY-BUNDLES.md#symfony-maker);
- [Doctrine](SYMFONY-BUNDLES.md#doctrine)

## Symfony Maker

References:
- https://symfony.com/doc/current/bundles/SymfonyMakerBundle/index.html

A bundle that allows automatic creation of controllers, forms, routes and more.

Once in the container shell:
```shell script
composer require symfony/maker-bundle --dev
```
```
Using version ^1.15 for symfony/maker-bundle
./composer.json has been updated
Loading composer repositories with package information
Updating dependencies (including require-dev)
Restricting packages listed in "symfony/symfony" to "5.0.*"

Prefetching 3 packages 🎶 💨
  - Downloading (100%)

Package operations: 3 installs, 0 updates, 0 removals
  - Installing nikic/php-parser (v4.4.0): Loading from cache
  - Installing doctrine/inflector (1.3.1): Loading from cache
  - Installing symfony/maker-bundle (v1.15.1): Loading from cache
Writing lock file
Generating autoload files
21 packages you are using are looking for funding.
Use the `composer fund` command to find out more!
Symfony operations: 1 recipe (dec4b58fa62ebad8cfd1f08a87b8d8c1)
  - Configuring symfony/maker-bundle (>=1.0): From github.com/symfony/recipes:master
Executing script cache:clear [OK]
Executing script assets:install public [OK]

Some files may have been created or updated to configure your new packages.
Please review, edit and commit them: these files are yours.
```

## Doctrine

A bundle that allows Object Relational Mapping for PHP.

Once in the container shell:
```shell script
composer require doctrine/annotations
```
```
Using version ^1.10 for doctrine/annotations
./composer.json has been updated
Loading composer repositories with package information
Updating dependencies (including require-dev)
Restricting packages listed in "symfony/symfony" to "5.0.*"

Prefetching 2 packages 🎶 💨
  - Downloading (100%)

Package operations: 2 installs, 0 updates, 0 removals
  - Installing doctrine/lexer (1.2.0): Loading from cache
  - Installing doctrine/annotations (1.10.2): Loading from cache
Writing lock file
Generating autoload files
21 packages you are using are looking for funding.
Use the `composer fund` command to find out more!
Symfony operations: 1 recipe (942e95b4a265effefbbbad11b719986b)
  - Configuring doctrine/annotations (>=1.0): From github.com/symfony/recipes:master
Executing script cache:clear [OK]
Executing script assets:install public [OK]

Some files may have been created or updated to configure your new packages.
Please review, edit and commit them: these files are yours.
```
