# Chat Events

## Events

### chat

Fired when a new chat is sent.

## Examples

### Prevent any chat message with capital letters

```typescript
this.api.getEventManager()
    .on("chat", async (event: ChatEvent) => {
        const message = event.getChat().getMessage();
        const sender = event.getChat().getSender();

        if (!/[A-Z]/.test(message)) return;

        await sender.sendMessage("Messages can not have capital letters!");
        event.preventDefault();
    });
```

