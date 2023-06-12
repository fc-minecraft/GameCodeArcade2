# Sequencing

### @explicitHints 1

### @activities true

## First Activity

### Placing blocks

The agent is capable of placing Minecraft blocks, but doing so is a multi-step process.  Before the agent can place a Minecraft block, the agent needs to have a block in its inventory.

The first step is to use ``||agent:agent set block or item||`` to put a block in the agent's inventory.

#### ~ tutorialhint

The agent places blocks from its first inventory slot by default, so use ``||agent:agent set block or item||`` to set a block in slot **1** of the agent's inventory.

### Searching by block name

The drop-down menu in ``||agent:agent set block or item||`` is rather large, so finding a specific Minecraft block can be challenging.

In the drop-down menu, search for **redstone** to quickly find **Block of Redstone**.

#### ~ tutorialhint

```blocks
player.onChat("place", function () {
    agent.setItem(REDSTONE_BLOCK, 1, 1)
})
```

### Consecutive statements

The second step, after putting a block in the agent's inventory, is to make the ``||agent:agent place||`` the block.

Drag an ``||agent:agent place||`` block from the ``||agent:AGENT||`` category and attach it to the bottom of ``||agent:agent set block or item||``.  Then run the **place** ``||player:chat command||``.

#### ~ tutorialhint

Event blocks can hold multiple statement blocks so that multiple actions can run in sequence.

### Review

The agent can perform multiple actions in a row in the order that they appear in the event block.

**Statement blocks** are shaped so that they can be placed one after the other to form a sequence of actions.

#### ~ tutorialhint

```blocks
player.onChat("place", function () {
    agent.setItem(REDSTONE_BLOCK, 1, 1)
    agent.place(FORWARD)
})
```

```template
player.onChat("place", function () {
    agent.setItem(GRASS, 1, 1)
})
```

```ghost
player.onChat("run", function () {
    agent.interact(FORWARD)
    agent.move(FORWARD, 1)
    agent.destroy(FORWARD)
    agent.turn(LEFT_TURN)
    agent.setItem(REDSTONE_BLOCK, 1, 1)
    agent.place(FORWARD)
})
```
