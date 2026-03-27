## Laravel Snippets (Playground)

Diese Seite enthält **Beispielcode im Stil der Laravel-Dokumentation** (Routes, Controller, Validation, Eloquent, Queues).
Inhaltlich muss es nicht “passen” — es geht um Rendering von Codeblöcken und Syntax.

## Routing (web)

```php
<?php

use Illuminate\Support\Facades\Route;

Route::get('/health', function () {
    return 'ok';
});

Route::middleware(['web'])->group(function () {
    Route::get('/users/{user}', function (string $user) {
        return "user={$user}";
    })->where('user', '[0-9]+');
});
```

## Controller (minimal)

```php
<?php

namespace App\Http\Controllers;

use Illuminate\Http\Request;

final class PlaygroundController
{
    public function __invoke(Request $request): array
    {
        return [
            'ok' => true,
            'input' => $request->all(),
        ];
    }
}
```

## Validation (Form Request style)

```php
<?php

use Illuminate\Http\Request;
use Illuminate\Support\Facades\Validator;

$validator = Validator::make(
    ['email' => 'taylor@laravel.com', 'name' => 'X'],
    ['email' => ['required', 'email'], 'name' => ['required', 'string', 'min:2']]
);

if ($validator->fails()) {
    $errors = $validator->errors()->toArray();
}
```

## Eloquent (query samples)

```php
<?php

use App\Models\User;

$users = User::query()
    ->where('active', true)
    ->orderByDesc('created_at')
    ->take(10)
    ->get(['id', 'name', 'email']);

$count = User::query()->whereNotNull('email_verified_at')->count();
```

## Events & Listeners (shape demo)

```php
<?php

namespace App\Events;

final class SomethingHappened
{
    public function __construct(public string $message)
    {
    }
}
```

## Queue / Job (shape demo)

```php
<?php

namespace App\Jobs;

use Illuminate\Bus\Queueable;
use Illuminate\Contracts\Queue\ShouldQueue;
use Illuminate\Foundation\Bus\Dispatchable;

final class ProcessPlayground implements ShouldQueue
{
    use Dispatchable, Queueable;

    public function __construct(public int $id)
    {
    }

    public function handle(): void
    {
        // intentionally empty (playground)
    }
}
```

## Blade (template snippet)

```blade
@if ($user)
    <h1>Hello, {{ $user->name }}</h1>
@else
    <h1>Hello, guest</h1>
@endif
```

