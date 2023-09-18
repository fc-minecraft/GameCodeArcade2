# Controlling the agent

### @explicitHints 1

### @activities true

## First Activity

### Sequencing

Multiple actions within an ``||player:on chat command||`` can be used to make the agent do different things in sequence. The agent has several different capabilities, which can be customized via the drop-down menu.

We already have an ``||player:on chat command||`` named **interact** with an ``||agent:agent move||`` block inside, but we also need the agent to interact with the lever. 

#### ~ tutorialhint

Press **next** to continue tutorial

### Agent interact

The ``||agent:agent interact||`` block from the ``||agent:AGENT||`` category makes the agent interact with mechanisms like levers, buttons, doors, gates, and more.

From the ``||agent:AGENT||`` category drag an ``||agent:agent interact||`` block underneath the ``||agent:agent move||`` block inside the **interact** ``||player:on chat command||``

#### ~ tutorialhint

```blocks
player.onChat("interact", function () {
    agent.move(FORWARD, 1)
    agent.interact(FORWARD)
})
```

### Review

Press the green Play button to load this new chat command into your agent. Send the command **interact** in the Minecraft chat to run the code in the **interact** ``||player:chat command||``.

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
