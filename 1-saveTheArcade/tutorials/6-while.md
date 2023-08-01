# While

### @explicitHints 1

### @activities true

## First Activity

### Conditional looping

For some problems involving a loop, a ``||loops:repeat block||`` is not appropriate because counting the number of times to repeat is infeasible.

A ``||loops:while||`` block is another type of loop that uses a condition to determine whether it should repeatedly loop through its code.

#### ~ tutorialhint

A ``||loops:while||`` block runs its code while the condition is true.  After running the code inside, the ``||loops:while||`` block checks the condition once more to determine whether to run its code again.  The ``||loops:while||`` loop terminates when the condition is false.

### Agent inspect

The ``||agent:agent inspect||`` block is a value block.  **Value blocks** have a distinct rounded shape and provide a piece of information, which is called a **value**.  The information returned by ``||agent:agent inspect||`` is whatever Minecraft block is next to the agent.

Value blocks fit in the rounded bubbles of other code blocks where a value is expected, such as the drop-down menu in ``||agent:agent set block or item||``.

#### ~ tutorialhint

The placement of ``||agent:agent inspect||`` in ``||agent:agent set block or item||`` puts whatever block is to the agent's right in the agent's inventory.

### Comparing values

The ``||logic:LOGIC||`` category has a condition block that allows for the ``||logic:comparison||`` of two values.  With the **equal sign (=)** selected, the ``||logic:comparison||`` block returns true if the two values are the same.

Try to use a ``||logic:comparison||`` block to make a condition for the ``||loops:while||`` block.  The agent needs to continue its task ``||loops:while||`` ``||agent:agent detect||`` **down** is equal to **cobblestone**.

#### ~ tutorialhint

Use a ``||blocks:block value||`` from the ``||blocks:BLOCKS||`` category to complete the comparison.

### Review

A ``||loops:while||`` block uses a condition to determine whether it should continue to loop through its code.

``||loops:While||`` loops are useful when the number of times to repeat is unclear but a condition for repeating is apparent.

``||logic:Comparison||`` blocks can compare two values to create a condition.

#### ~ tutorialhint

```blocks
player.onChat("copy", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) == COBBLESTONE) {
        agent.move(FORWARD, 1)
        agent.setItem(agent.inspect(AgentInspection.Block, RIGHT), 1, 1)
        agent.place(LEFT)
    }
})
```

```template
player.onChat("copy", function () {
    while (false) {
        agent.move(FORWARD, 1)
        agent.setItem(agent.inspect(AgentInspection.Block, RIGHT), 1, 1)
        agent.place(LEFT)
    }
})
```

```ghost
player.onChat("run", function () {
    while (agent.inspect(AgentInspection.Block, FORWARD) == GRASS) {
        agent.interact(FORWARD)
        agent.setItem(REDSTONE_BLOCK, 1, 1)
        agent.place(FORWARD)
        agent.turn(LEFT_TURN)
    }
    for (let index = 0; index < 4; index++) {
        if (agent.detect(AgentDetection.Block, FORWARD)) {
            agent.destroy(RIGHT)
            agent.move(FORWARD, 1)
        }
    }
})
```
