## Markdown Overview (Playground)

Diese Seite ist ein reines **Feature-Muster**. Inhalt muss keinen Sinn ergeben — Ziel ist: alles rendert.

## Inhaltsverzeichnis (manuell)

- [Text](#text)
- [Listen](#listen)
- [Zitate](#zitate)
- [Code](#code)
- [Links](#links)
- [Bilder](#bilder)
- [Tabellen](#tabellen)
- [HTML](#html)
- [Fußnoten](#fußnoten)

## Text

Normaler Text, **fett**, _kursiv_, ~~durchgestrichen~~, `inline code`.

Hard line break folgt hier.  
Und hier geht’s weiter in der nächsten Zeile.

## Listen

- Bullet 1
- Bullet 2
  - nested bullet A
  - nested bullet B

1. Nummer 1
2. Nummer 2
   1. Unterpunkt 2.1
   2. Unterpunkt 2.2

Task List:

- [x] erledigt
- [ ] offen
- [ ] noch offen

## Zitate

> Ein Quote.
>
> > Ein verschachteltes Quote.
>
> Zurück zur ersten Ebene.

## Code

Inline: `php artisan route:list --except-vendor`

Fenced (bash):

```bash
php -v
php artisan --version
php artisan route:list --except-vendor --method=GET
```

Fenced (php):

```php
<?php

declare(strict_types=1);

use Illuminate\Support\Str;

$slug = Str::slug('Hello Playground!');
echo $slug;
```

## Links

- Relativ: [Getting Started](../introduction/getting-started.md)
- In Datei: [Style Guide](../reference/style-guide.md)
- Extern: `https://laravel.com/docs`

## Bilder

Ein Bild-Platzhalter (falls dein Renderer Bilder rendert):

![Placeholder](https://via.placeholder.com/1200x400.png?text=Docs+Playground)

## Tabellen

| Spalte A | Spalte B | Spalte C |
| --- | --- | --- |
| 1 | 2 | 3 |
| `code` | **bold** | _italic_ |
| Zeile mit langem Text | wrap wrap wrap | Ende |

## HTML

<details>
  <summary>Toggle (HTML details/summary)</summary>

  <p>Dieser Block testet HTML innerhalb von Markdown.</p>
  <ul>
    <li>Ein Punkt</li>
    <li>Noch ein Punkt</li>
  </ul>
</details>

## Fußnoten

Ein Satz mit Fußnote.[^1] Noch ein Satz mit zweiter Fußnote.[^2]

[^1]: Fußnote 1: kompletter Testtext.
[^2]: Fußnote 2: nochmal Testtext.

