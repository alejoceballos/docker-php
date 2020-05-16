[<< Previous: Symfony Project](SYMFONY-PROJECT.md)

---

# Symfony: Controllers (WIP)

### Responses
```php
return $this->render(template, parameters)
```
```php
return $this->json(keyParameterizedArray)
```
```php
return new Response(text)
```

### URL REST parameters
For the URL:
```
http://localhost:8080/default/some_parameter_value
```
Grab `some_parameter_value` in the controller:
```php/
.
.
.
/**
 * @Route("/default/{param}", name="default")
 */
public function index($param)
{
    return new Response($param);
}
.
.
.
```

### Redirection
```php
return $this->redirect('http://anotherUrl.whatever.com')
```

Imagine that some controller method has the following annotation:
```
 @Route("/anotherRoute", name="namedAnotherRoute")]
```
To easily redirect to that route from another controller method:
```php
return $this->redirectToRoute('namedAnotherRoute')
```
`redirectToRoute` does not accept parameters!

### Flash messages

Reference:
- https://symfony.com/doc/current/controller.html#flash-messages

Flash messages are string data that can be stored in the session that are kept until a response is sent.

> By design, flash messages are meant to be used exactly once: they vanish from the session automatically as soon as you 
> retrieve them. This feature makes "flash" messages particularly great for storing user notifications.

This:
```php
$this->addFlash('notice', 'Your changes were saved!');
```
Is the same as
```php
$request->getSession()->getFlashBag()->add('notice', 'Your changes were saved!');
```
---

[Next: Symfony Views >>](SYMFONY-VIEW.md)
