## laravel-livewire-rappasoft-datatable-example
A dynamic Laravel Livewire component for data tables.

![Dark Mode](https://imgur.com/QoEdC7n.png)

![Full Table](https://i.imgur.com/2kfibjR.png)

### [Bootstrap 4 Demo](https://tables.laravel-boilerplate.com/bootstrap-4) | [Bootstrap 5 Demo](https://tables.laravel-boilerplate.com/bootstrap-5) | [Tailwind Demo](https://tables.laravel-boilerplate.com/tailwind) | [Demo Repository](https://github.com/rappasoft/laravel-livewire-tables-demo)

## Installation

You can install the package via composer:

``` bash
composer require rappasoft/laravel-livewire-tables
```

## Documentation and Usage Instructions

See the [documentation](https://rappasoft.com/docs/laravel-livewire-tables) for detailed installation and usage instructions.

## Basic Example

```php
<?php

namespace App\Http\Livewire\Admin\User;

use App\Domains\Auth\Models\User;
use Illuminate\Database\Eloquent\Builder;
use Rappasoft\LaravelLivewireTables\DataTableComponent;
use Rappasoft\LaravelLivewireTables\Views\Column;

class UsersTable extends DataTableComponent
{

    public function columns(): array
    {
        return [
            Column::make('Name')
                ->sortable()
                ->searchable(),
            Column::make('E-mail', 'email')
                ->sortable()
                ->searchable(),
            Column::make('Verified', 'email_verified_at')
                ->sortable(),
        ];
    }

    public function query(): Builder
    {
        return User::query();
    }
}
```

### [See advanced example](https://rappasoft.com/docs/laravel-livewire-tables/v1/usage/advanced-example-table)

## To-do/Roadmap

- [x] Bootstrap 4 Template
- [x] Bootstrap 5 Template
- [x] Sorting By Relationships
- [x] User Column Selection
- [x] Drag & Drop (beta)
- [x] Column Search
- [x] Greater Configurability
- [ ] Collection/Query Support
- [ ] Test Suite (WIP)


