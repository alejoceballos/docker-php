[<< Previous: Symfony Controllers](SYMFONY-CONTROLLER.md)

---

# Symfony: The View (WIP)

## Twig

TBD: explain what twig is

### Inheritance and blocks

Twig can allow some sort of "inheritance" by defining a basic template um specific named blocks that can be substituted 
by the templates that inherits from it, for example:
```twig
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>{% block title %}Welcome!{% endblock %}</title>
        {% block stylesheets %}{% endblock %}
    </head>
    <body>
        {% block body %}{% endblock %}
        {% block javascripts %}{% endblock %}
    </body>
</html>
```
This master template defines four blocks, _title_, _stylesheets_, _body_, and _javascripts_.

The inheriting template extends from the previous one below (called `base.html.twig`) and makes use of some of its 
blocks, _title_ and _body_:
```twig
{% extends 'base.html.twig' %}

{% block title %}Hello DefaultController!{% endblock %}

{% block body %}
<style>
    .example-wrapper { margin: 1em auto; max-width: 800px; width: 95%; font: 18px/1.5 sans-serif; }
    .example-wrapper code { background: #F5F5F5; padding: 2px 6px; }
</style>

<div class="example-wrapper">
    <h1>Hello {{ controller_name }}! ✅</h1>

    This friendly message is coming from:
    <ul>
        <li>Your controller at <code><a href="{{ '/var/www/my-project/src/Controller/DefaultController.php'|file_link(0) }}">src/Controller/DefaultController.php</a></code></li>
        <li>Your template at <code><a href="{{ '/var/www/my-project/templates/default/index.html.twig'|file_link(0) }}">templates/default/index.html.twig</a></code></li>
    </ul>
</div>
{% endblock %}
```
The base path for templates is `src/templates`, that's why there is no need to reference the parent's path location in 
the child template.

### Parameters and literals

In the previous template, note the parameter `controller_name` under double braces. The template engine will replace 
this parameter by the value passed by the controller:
```php
$this->render(
    'default/index.html.twig', 
    [ 'controller_name' => 'DefaultController' ]
);
```

The same double braces may be used to render literals or literals and variables concatenations.

### Code blocks

Use braces and percent to insert logic in the template:
```twig
{% for value in list %}
    . . .
{% endfor %}
```
```twig
loop.index
```
and
```twig
loop.index0
```

---

[Next: Symfony Entities >>](SYMFONY-ENTITY.md)
