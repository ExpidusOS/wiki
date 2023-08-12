---
title: Gokai
---

# Gokai

Gokai is the main runtime and framework utilized in all applications and compositors for ExpidusOS. It utilizes the embedded Flutter Engine to run multiple engines on different display outputs or window views. The core design is inspired by Android's API by having a context (`Gokai::Context`) which exposes functionality via services (`Gokai::Service`). Each service gets their own service channel (`Gokai::ServiceChannel`) which allows for each service to communicate with the engine instances that call for the service. However, not every service in Gokai exposes functionality through a service channel.

## Environmental Variables

| Name                                                              | Description                               | Accepted Values                                                |
|-------------------------------------------------------------------|-------------------------------------------|----------------------------------------------------------------|
| `GOKAI_CONTEXT_DISPLAY_BACKEND`<a href="#note-1"><sub>1</sub></a> | Changes the display backend.              | `try-auto`, `x11`<a href="#note-2"><sub>2</sub></a>, `wayland` |
| `GOKAI_CONTEXT_MODE`                                              | Changes the context mode to run Gokai in. | `client`, `compositor`                                         |
| `GOKAI_LOGGER`                                                    | Changes the logging method.               | Linux: `syslog`, `systemd`, `default`                          |

<p><a href="#note-1"><sub id="note-1">1</sub></a> Works only with Linux.</p>

<p><a href="#note-2"><sub id="note-2">2</sub></a> Works only when <code>GOKAI_CONTEXT_MODE</code> is set to <code>client</code>.</p>
