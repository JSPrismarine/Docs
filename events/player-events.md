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

Fired when a player moves.

### playerToggleFlight

Fired when a player toggles fly.

### playerToggleSprint

Fired when a player toggles sprint.

### playerToggleOperator

Fired when a player add or removes their operator status.

### playerSetGamemode

Fired when a player changes their gamemode.

## Examples

### Prevent any player from flying

```typescript
this.api.getEventManager()
    .on("playerToggleFlight", (event: PlayerToggleFlightEvent) => {
        event.preventDefault();
    });
```

