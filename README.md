# Net OS - Laravel Convert Case Middleware

1. `composer require net-os/laravel-convert-case-middleware`
2. Add the middleware to the appropriate group in `App\Http\Kernel.php`. For example

```
protected $middlewareGroups = [
    'api' => [
        'throttle:60,1',
        'bindings',
        \NetOS\LaravelConvertCaseMiddleware\ConvertRequestToSnakeCase::class,
        \NetOS\LaravelConvertCaseMiddleware\ConvertResponseToCamelCase::class,
    ],
];
```
