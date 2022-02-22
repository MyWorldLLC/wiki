---
title: Scripting
has_children: true
---
# Introducing Chipmunk: MyWorld's Scripting Language
Chipmunk is a fast, powerful, dynamically typed
scripting language designed to be easy to learn
and intuitive to use for both new programmers and
industry veterans alike. It has modules, classes,
powerful trait-based inheritance and polymorphism,
and is competitive in speed with other
industry-standard languages.

Chipmunk is hosted in a dedicated
[GitHub repository](https://github.com/MyWorldLLC/Chipmunk),
and a good set of examples of the language's syntax and
capabilities is the official
[language test scripts](https://github.com/MyWorldLLC/Chipmunk/tree/master/Lang/src/test/resources/chipmunk).

## Attaching Scripts - Lifecycle & Permissions
Scripts are run in MyWorld by attaching them to entities.
Any entity can have scripts attached, including your avatar,
and scripts can be run on either the client or the server.
Some of the library modules that MyWorld exposes to scripts
are only available on the client, and some are only available
on the server. When an entity loads, its scripts are immediately
run. Depending on the code contained in each script, it may either
run and terminate shortly afterwards, or it may register event
listeners to remain permanently "running" until it stops itself,
de-registers event listeners, or its entity is removed from the
world.

All scripts must declare an entrypoint method named `main()` in
a module named `main`:
```chipmunk
module main

def main(){
    # ... implement main here ...
}

```
Scripts that should not terminate when `main()` exits must register
event listeners before `main()` exits.

MyWorld's permission system is not yet functional, but once it is
assume that serverside scripts generally run with the permissions
of the entity they are attached to and that clientside scripts run
with the permissions of the user whose avatar they are attached to.


> Note that client-side scripts run on *every*
client that is in range of the entity, and they run with the
permissions of the user who is logged in on that client - so
a script may be able to do some things but not other things
depending on which user's client it is running on.