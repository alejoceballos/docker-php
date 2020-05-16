[<< Previous: Symfony Services](SYMFONY-SERVICE.md)

---

# Symfony: Routes (WIP)

## Annotations

In previous versions of Symfony, the way to declare a route to a controller would be to define it in 
`config/routes.yaml`.
```smartyconfig
default:
    path: /my/route/path
    controller: App\Controller\SomeController::someMethod
```
Now it can be achieved using the annotation `@Route` within the method comment.

#### Path

TBD

```php
@Route("/my/route/path")
```

i18n paths:
```php
@Route({
    "en": "/my/route/path",
    "pt-br": "/meu/caminho/de/rota",
    "es-ar": "/mi/camino/de/ruta"
})
```

#### Parameters

TBD

```php
@Route("/my/route/path/{parameter}")
```

Optional:

```php
@Route("/my/route/path/{parameter?}")
```

#### Name

Used to name a controller redirection, for example:
```php
@Route("...", name="my_route_name")
```
```php
    .
    .
    .
    return $this->redirectToRoute('my_route_name');
    .
    .
    .
```

#### Requirements

Constrains the parameter value passed as argument.

```php
@Route("...", name="...", requirements={"parameter"="RegEx"})
```

Example, only number: 
```php
@Route("/my/route/path/{parameter}", name="whatever", requirements={"parameter"="\d+"})
```
Will accept 
```
/my/route/path/123
```
But will reject 
```
/my/route/path/onetwothree
```

If the parameter doesn't match the regular expression a `ResourceNotFoundHttpException` will trigger a 
`NotFoundHttpException` that consequently will trigger an `HTTP 404` response.

### A complete example

```php
@Route(
    "/my/route/path/{param1}/{param2}/{param3}",
    defaults={
        "param3"="whatsoever"
    },
    requirements={
        "param1"="whatever|whenever",
        "param2"="\d+"
    }
)
```

QUESTION: `defaults` can only be applied to the last parameters?

---

[Next: TBD >>](SYMFONY-ROUTE.md)
