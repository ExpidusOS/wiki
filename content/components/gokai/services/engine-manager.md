---
title: Engine Manager
description: Information on Gokai's Engine Manager service.
---

# Engine Manager

The engine management service in Gokai is one of the most vital services in Gokai.
It provides methods for controlling, looking up, and destroying instances of the Flutter Engine.
Each engine is assigned a UUID string to identify each instance.

## Service Channel

As the engine manager service is vital to Gokai, it exposes some of its functionality
through a service channel. The service channel name is `Gokai::Service::EngineManager`
and each method is encoded to be compatible with Flutter's JSON Method Channel.

### Methods

#### `String getEngineId()`

This method returns the UUID assigned to the engine which called it.

#### `List<String> getIds()`

This method returns all ID's of every engine instance which are created and running.

#### `GokaiFlutterEngineViewType getViewType(String id)`

Returns the view type (`window` or `display`) of a particular engine instance.

#### `String getViewName(String id)`

Returns the name of the view assigned to a particular engine instance.
