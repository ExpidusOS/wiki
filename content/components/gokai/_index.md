---
title: Gokai
---

# Gokai

Gokai is the main runtime and framework utilized in all applications and compositors for ExpidusOS. It utilizes the embedded Flutter Engine to run multiple engines on different display outputs or window views. The core design is inspired by Android's API by having a context (`Gokai::Context`) which exposes functionality via services (`Gokai::Service`). Each service gets their own service channel (`Gokai::ServiceChannel`) which allows for each service to communicate with the engine instances that call for the service. However, not every service in Gokai exposes functionality through a service channel.
