# Controlling the agent

### @explicitHints 1

### @activities true

## First Activity

### Chat commands

The ``||player:on chat command||`` event block runs its code when a specific message is sent via the Minecraft chat window. Try to make the ``||agent:agent move forward||`` one block by sending the message **move** in chat.
Press the green play button to run your code. Then press **T** (or tap the Chat icon) to open the Minecraft chat window and type **move** in chat.

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
