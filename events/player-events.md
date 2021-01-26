# Player Events

## Events

### playerConnect

Fired when a player connects to the server.

### playerDisconnect

Fired when a player disconnects from the server.

### playerSpawn

Fired when a player spawns into the world.

### playerDespawn

Fired when a player despawns from the world.

### playerMove

Fired when a player moves in the server.

### playerToggleFlight

Fired when a player starts to fly.

### playerToggleSprint

Fired when a player starts to sprint.

### playerToggleOperator

Fired when a player add or removes there operator status.

### playerSetGamemode

Fired when a player changes there gamemode.

## Examples

### Prevent any chat with capital letters

```typescript
this.api.getEventManager()
    .on("playerToggleFlight", (event: PlayerToggleFlightEvent) => {
        event.preventDefault();
    });
```

