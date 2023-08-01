# Controlling the agent

### @explicitHints 1

### @activities true

## First Activity

### Chat commands

The ``||player:on chat command||`` event block runs its code when a specific message is sent via the Minecraft chat window.

Try to make the ``||agent:agent move forward||`` one block by sending the message **move** in chat.

Close the Code Builder window and then press **T** (or tap the Chat icon) to open the Minecraft chat window.

#### ~ tutorialhint

```blocks
player.onChat("move", function () {
    agent.move(FORWARD, 1)
})
```

```template
player.onChat("move", function () {
    agent.move(FORWARD, 1)
})
```
