# Controlling the agent

### @explicitHints 1

### @activities true

## First Activity

### Chat commands

The ``||player:on chat command||`` event block runs its code when a specific message is sent via the Minecraft chat window.

Try to make the ``||agent:agent move forward||`` one block by sending the message **move** in chat.

#### ~ tutorialhint

Close the Code Builder window and then press **T** (or tap the Chat icon) to open the Minecraft chat window.

### Agent destroy

The agent can do more than just move.  The agent can also destroy blocks.

Open the ``||agent:AGENT||`` category and drag an ``||agent:agent destroy||`` block into the ``||player:on chat command||`` block named **destroy**.

Try to have the agent destroy a block in its path.

#### ~ tutorialhint

Send the command **destroy** in the Minecraft chat to run the code in the **destroy** ``||player:chat command||``.

### Agent interact

Open the ``||player:PLAYER||`` category and drag a new ``||player:chat command||`` block into the workspace.  This command will be used to make the ``||agent:agent interact||`` with a lever, so renaming it to **interact** would be a good idea.

Try to make the ``||agent:agent interact||`` with a lever by adding a statement block to the **interact** ``||player:chat command||``.

#### ~ tutorialhint

The ``||agent:agent interact||`` block from the ``||agent:AGENT||`` category makes the ``||agent:agent interact||`` with levers.

Send the appropriate commands in chat to move the agent next to the lever and interact with it.

### Review

Multiple chat commands with meaningful names can be used to make the agent do different things.

The agent has several different capabilities, which can be performed in different directions via the drop-down menu.

#### ~ tutorialhint

```blocks
player.onChat("interact", function () {
    agent.interact(FORWARD)
})
player.onChat("destroy", function () {
    agent.destroy(FORWARD)
})
player.onChat("move", function () {
    agent.move(FORWARD, 1)
})
```

```template
player.onChat("destroy", function () {
	
})
player.onChat("move", function () {
    agent.move(FORWARD, 1)
})
```
