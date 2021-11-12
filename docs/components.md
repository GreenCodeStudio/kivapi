# Components
Components are parts of webpage, that can be managed by user.

Components can be found in Components directory in your project and also inside installed packages (./Packages/{vendor}/{package name/Components}).

## How to create component
To create component make new directory inside ./Components. Name of this directory will be name of component. In this directory create Controller.php file. Sample file is below. Keep in ming [namespaces](projectStructure.md#Namespaces)

```php
<?php

namespace Demo\Components\Layout;

use Core\ComponentManager\ComponentController;
use Core\ComponentManager\ComponentManager;

class Controller extends ComponentController
{
    public function __construct($params)
    {
        $this->params = $params;
    }

    public static function DefinedParameters()
    {
        return [
            'pageTitle' => (object)['type' => 'string'],
        ];
    }

    public function loadView()
    {
        include __DIR__.'/View.php';
    }
    public static function type()
    {
        return "layout";
    }
}

```

Next create View.php file, contains HTML of your component.