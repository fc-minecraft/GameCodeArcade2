# Controlling the agent

### @explicitHints 1

### @activities true

## First Activity

### Agent interact

Multiple chat commands with meaningful names can be used to make the agent do different things.

The agent has several different capabilities, which can be performed in different directions via the drop-down menu.

Open the ``||player:PLAYER||`` category and drag a new ``||player:chat command||`` block into the workspace.  This command will be used to make the ``||agent:agent interact||`` with a lever, so renaming it to **interact** would be a good idea.

The ``||agent:agent interact||`` block from the ``||agent:AGENT||`` category makes the ``||agent:agent interact||`` with levers.

Try to make the ``||agent:agent interact||`` with a lever by adding a statement block to the **interact** ``||player:chat command||``.

Send the appropriate commands in chat to move the agent next to the lever and then interact with it.

#### ~ tutorialhint

```blocks
player.onChat("interact", function () {
    agent.move(FORWARD, 1)
    agent.interact(FORWARD)
})
```

```template
player.onChat("interact", function () {
    agent.move(FORWARD, 1)
})
```
