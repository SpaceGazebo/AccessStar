AccessStar
==========

AccessStar is an Access Control List, Role-Based, Group-Based, Permission-Based, Context-Based permissions management system. This project was created from scratch using Entrust as a reference.

Installation
==========

Set Up
==========

Usage
==========

###### User has role:

```php
if (Access::role('Moderator')->granted())
{
    [...]
}
```

###### User has a rank:

If you like numbered ranks

```php
if (Access::rank(3)->granted())
{
    [...]
}
```


