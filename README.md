# Fixi.js Cheat Sheet

## HTML Attributes (6)

| Attribute     | Description                                  |
|---------------|----------------------------------------------|
| `fx-action`   | URL to send the request to (required)        |
| `fx-method`   | HTTP method (`GET`, `POST`, etc.), default `GET` |
| `fx-trigger`  | Event that triggers the request, default based on element type (`click`, `submit`, `change`) |
| `fx-target`   | CSS selector for element to update           |
| `fx-swap`     | How to inject content (`innerHTML`, `outerHTML`, etc.) |
| `fx-ignore`   | Skip processing for element and its children |

## Events (9)

| Event         | Description                                        |
|---------------|----------------------------------------------------|
| `fx:init`     | Before element is initialized                      |
| `fx:inited`   | After element is initialized (non-bubbling)        |
| `fx:process`  | Manually initialize fixi-powered elements          |
| `fx:config`   | Configure request before sending                   |
| `fx:before`   | Just before request is sent                        |
| `fx:after`    | After response is received, before DOM swap        |
| `fx:error`    | If fetch fails due to a network error              |
| `fx:finally`  | After request ends, whether success or failure     |
| `fx:swapped`  | After swap and view transition complete            |

## Properties (2)

| Property         | Description                                      |
|------------------|--------------------------------------------------|
| `evt.detail.cfg` | Request config object used by all fetch events   |
| `cfg.swap`       | Can be set to a custom DOM swap function         |

---

# Surreal.js Cheat Sheet

## Core Selectors

| Function | Description                                               |
|----------|-----------------------------------------------------------|
| `me()`   | Selects a single element (context-aware, smart `this`)    |
| `any()`  | Selects multiple elements (always returns an array)       |

## DOM Functions

| Function        | Description                                    |
|-----------------|------------------------------------------------|
| `classAdd()`    | Add class(es)                                  |
| `classRemove()` | Remove class(es)                               |
| `classToggle()` | Toggle class(es)                               |
| `styles()`      | Apply inline styles                            |
| `attribute()`   | Get/set/remove attributes                      |
| `remove()`      | Remove element(s) from the DOM                 |
| `createElement()` | Shortcut for `document.createElement()`      |

## Event Handling

| Function     | Description                              |
|--------------|------------------------------------------|
| `on()`       | Add event listener                       |
| `off()`      | Remove specific listener                 |
| `offAll()`   | Remove all listeners                     |
| `send()`     | Dispatch an event                        |
| `disable()`  | Disable interaction (click/key/submit)   |
| `enable()`   | Re-enable interaction                    |

## Utilities

| Function     | Description                                        |
|--------------|----------------------------------------------------|
| `run()`      | Run function on one or more elements               |
| `sleep(ms)`  | Waits for specified time (async)                   |
| `tick()`     | Waits 1 animation frame                            |
| `halt(ev)`   | Stops propagation and prevents default             |
| `rAF()`      | Runs function in requestAnimationFrame             |
| `rIC()`      | Runs function during idle time                     |
| `onloadAdd()`| Add callback for DOM ready                         |

## Animations

| Function     | Description                        |
|--------------|------------------------------------|
| `fadeOut()`  | Fade out and remove (or keep)      |
| `fadeIn()`   | Fade in from hidden                |

## Plugin Support

| Feature         | Description                                 |
|------------------|---------------------------------------------|
| `plugins.push(fn)` | Add custom methods to elements globally  |
