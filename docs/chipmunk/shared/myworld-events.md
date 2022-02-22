---
title: myworld.events
parent: Shared Modules
nav_order: 2
---
# Overview
This module exposes the low-level API for scripts to manage event
registrations. Scripts that should remain running after `main()`
exits must register one or more event handlers, and will remain
active until they de-register all handlers or until the `exit()`
method is called.

> Note: currently the event classes are not exposed to scripts. This
> API will need some more work before it's ready for use, and it's
> probable that the classes will be replaced with event type 
> id strings.

## Methods
* `register(eventType, handler, method)` - registers an event handler
  * `eventType` - class, the type of event to listen for
  * `handler` - the object containing the handler method to be called
  * `method` - string, the name of the method to call with the event.
     method must accept exactly 1 parameter, which is the event object.
  

* `unregister(eventType, handler, method)` - unregisters a previously 
   registered event handler
  * `eventType` - class, the previously registered event type
  * `handler` - the previously registered handler object
  * `method` - the previously registered handler method name