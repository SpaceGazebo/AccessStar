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

//  User is a Moderator
if (Access::role('Moderator')->granted())

// User is a Moderator and/or a Poster
if (Access::role('Moderator','Poster')->granted())

// User is a Moderator and/or a Poster
if (Access::role('Moderator','Poster','')->granted())

// User is one of the following:
if (Access::role('Oracle','Orator','Orchard','Orchestra','Organ','Orphan')->granted())

// You can also do
if (Access::isAdmin()) //shortcut for Access::role('Admin')->granted()

// If you really needed to:
if (Access::isOracleOrOratorOrOrchardOrOrchestraOrOrganOrOrphan()) // using space-age if statements to sort out "Or Orator" from "Or Or ator"

// Check if the user has the permissions 'post' in only one specific context
if (Access::context($board)->perm('post')->granted())

// Check if the user has the permissions 'post' in any context
if (Access::perm('post')->granted())

// Check if the user has the permissions 'post' in at least one of these contexts
if (Access::context($board1, $board2, $board3)->perm('post')->granted())
```

###### User has a rank:

If you like numbered ranks

```php
if (Access::rank(3)->granted())
{
    [...]
}
```


