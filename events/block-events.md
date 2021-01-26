# Block Events

## Events

### blockRegister

Fired when a new block is registered.

## Examples

### Prevent block from being registered

```typescript
this.api.getEventManager()
    .on("blockRegister", (event: BlockRegisterEvent) => {
        const block = event.getBlock() as Block;
        if (block.getName() !== "minecraft:stone") return;

        this.api.getLogger().info("minecraft:stone isn't permitted");
        event.preventDefault();
    });
```

