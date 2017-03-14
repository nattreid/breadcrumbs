# Drobečková navigace pro Nette Framework

## Nastavení v **config.neon**
Zaregistrujte továrnu

```neon
services:
    - NAttreid\Breadcrumbs\IBreadcrumbFactory
```

## Použití
```php
/** @var \NAttreid\Breadcrumbs\IBreadcrumbFactory @inject */
public $breadcrumbFactory;

protected function createComponentBreadcrumbs() {
    $control = $this->breadcrumbFactory->create();
    $control->addLink('name', 'Link:action');
    return $control;
}
```