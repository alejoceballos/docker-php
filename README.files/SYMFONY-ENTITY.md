[<< Previous: Symfony Views](SYMFONY-VIEW.md)

---

# Symfony: Entities (WIP)

## ORM: Object Relational Mapping

TBD

## Database configuration

TBD: .env

## Doctrine

TBD

### The Anemic Domain Model: Entity

TBD
```shell script
bin/console make:entity
```
TBD

### Database Migration

```shell script
bin/console make:migration
```
```shell script
bin/console doctrine:migrations:migrate
```

### The Unit of Work handler: Entity Manager

```php
$this->getDoctrine->getManager()
```
#### Persist & Flush

---

[Next: Symfony Services >>](SYMFONY-SERVICE.md)
