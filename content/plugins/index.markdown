---
title: Plugins
template: page.html
---

Everything in InContext, even the build process itself, is a plugin, and plugins themselves can provide plugin interfaces (but that's getting carried away). There are a number of different plugin types that are important to know about:

- Handlers
- Commands
- Context Functions
- Filters

# Introduction

Plugins are simply Python modules that live in the `plugins` directory in the InContext source tree. InContext supports two different mechanisms for loading plugins: using [decorators](#decorators), and using a [plugin initializer](#plugin-initializer).

## Decorators

## Plugin Initializer

# Context Functions

Context functions are extensions to the Jinja 2 templating engine which can expose rich functionality to your templates.

For example, the following context function adds the method `now()` to Jinja 2.

```python
@incontext.context_function(name="now")
def now():
    return datetime.datetime.utcnow().replace(tzinfo=pytz.utc)
```

This can be used as follows:

```
<p>Rendered at {{ now() }}.</p>
```
