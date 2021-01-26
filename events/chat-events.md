# Chat Events

## Events

### chat

Fired when a new chat is sent.

## Examples

### Prevent any chat with capital letters

```typescript
this.api.getEventManager()
    .on("chat", (event: ChatEvent) => {
        const message = event.getChat().getMessage();

        if (!/[A-Z]/.test(message)) return;

        this.api.getLogger().info("Messages can not have capital letters!");
        event.preventDefault();
    });
```

