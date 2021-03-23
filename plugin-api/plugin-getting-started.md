---
description: JSPrismarine plugin-development quick-start guide
---

# Getting Started

## Generating boiler-plate plugin using create-prismarine-plugin

Start by executing the following command which will guide you through a step-by-step process

```text
$ npx @jsprismarine/create-prismarine-plugin
```

{% hint style="info" %}
You can contribute to create-prismarine-plugin by visting [https://github.com/JSPrismarine/create-prismarine-plugin](https://github.com/JSPrismarine/create-prismarine-plugin)
{% endhint %}

## Navigating the project structure

{% tabs %}
{% tab title="index.ts" %}
```typescript
import type { PluginApi } from '@jsprismarine/prismarine';

export default class PluginBase {
    api: PluginApi;

    constructor(api: PluginApi) {
        this.api = api;
    }

    public async onEnable() { }
    public async onDisable() { }
}
```
{% endtab %}

{% tab title="package.json" %}
```javascript
{
    ...
    "prismarine": {
        "apiVersion": "${apiVersion}",
        "displayName": "${displayName}"
    },
    ...
}
```
{% endtab %}
{% endtabs %}

