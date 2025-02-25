# HTTP - Installation and Configuration
The web application bundle (`spiral/app`) ships with pre-configured http component. You will need a number of extensions
to enable it in alternative builds.

## Installation
To install the extension:

```bash
$ composer require spiral/http spiral/router spiral/nyholm-bridge
```

Extension can be activated by adding two bootloaders:

```php
class App extends Kernel
{
    /*
     * List of components and extensions to be automatically registered
     * within system container on application start.
     */
    protected const LOAD = [
        // ...

        // Fast PSR-7 implementation
        \Spiral\Nyholm\Bootloader\NyholmBootloader::class,

        // HTTP core
        Spiral\Bootloader\Http\HttpBootloader::class,

        // PSR-15 handler      
        Spiral\Bootloader\Http\RouterBootloader::class,

        // ...
    ];
}
```

> See how to use custom PSR-15 handler [here](/cookbook/psr-15.md).

Make sure to configure [routing](/http/routing.md).

## Configuration
The HTTP extension can be configured via `app/config/http.php` file:

```php
<?php

declare(strict_types=1);

return [
    // default base path
    'basePath'   => '/',
    
    // default headers
    'headers'    => [
        'Content-Type' => 'text/html; charset=UTF-8'
    ],

    // application level middleware
    'middleware' => [
        // middleware class name
    ],
];
```

> The default configuration will be used if such file does not exists.

You can register middleware during the bootload phase via `HttpBootloader`:

```php
namespace App\Bootloader;

use Spiral\Boot\Bootloader\Bootloader;
use Spiral\Bootloader\Http\HttpBootloader;
use Spiral\Http\Middleware\JsonPayloadMiddleware;

class AppBootloader extends Bootloader
{
    public function boot(HttpBootloader $http): void
    {
        // parse json payloads
        $http->addMiddleware(JsonPayloadMiddleware::class);
    }
}
```

## Middleware
HTTP extension include multiple middleware you might want to activate in your project:

Bootloader | Middleware
--- | ---
Spiral\Bootloader\Http\ErrorHandlerBootloader | Hide exceptions in non debug mode and render HTTP error pages.
Spiral\Bootloader\Http\JsonPayloadParserBootloader | Parse body of `application/json` requests.
Spiral\Bootloader\Http\PaginationBootloader | Use request query parameters to automatically configure paginator(s).
Spiral\Bootloader\Http\DiactorosBootloader | Use Zend/Diactoros as PSR-7 implementation (legacy).
