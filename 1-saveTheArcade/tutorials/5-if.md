# If

### @explicitHints 1

### @activities true

## First Activity

### Making decisions

Some problems involve performing actions over and over, but other actions are not necessarily repeated consistently.  An ``||logic:if||`` block can simplify code by determining when it is appropriate to perform a certain action.

An ``||logic:if||`` block is another type of **compound statement block**.  It uses a **condition** to determine whether to run its code.  If the condition is true, then the code inside the ``||logic:if||`` block will run.

#### ~ tutorialhint

A **condition** can be true or false.  **Condition blocks** have a distinct pointed shape to indicate that they fit where a condition is expected, as in an ``||logic:if||`` block.

### Agent detect

The ``||agent:agent detect||`` block can determine whether there is a solid block next to the agent.

Try using an ``||logic:if||`` block and an ``||agent:agent detect||`` block to make the ``||agent:agent destroy||`` only solid blocks.

Be sure to specify the correct direction in the ``||agent:agent detect||`` block. Also, the ``||loops:repeat||`` block is already set to run the correct number of times.

#### ~ tutorialhint

If there is a block, then ``||agent:agent detect||`` returns a value of **true**.  Items that the agent can walk through (such as torches, buttons, and levers) cause ``||agent:agent detect||`` to return a value of **false**.

### Review

Some problems can be simplified by using an ``||logic:if||`` block to run certain sections of code based on a condition.

Code with a condition can determine whether a specific section of code will run, which eliminates the need for manually addressing every single scenario.

#### ~ tutorialhint

```blocks
player.onChat("run", function () {
    for (let index = 0; index < 4; index++) {
        if (agent.detect(AgentDetection.Block, RIGHT)) {
            agent.destroy(RIGHT)
        }
        agent.move(FORWARD, 1)
    }
})
```

```template
player.onChat("run", function () {
    for (let index = 0; index < 4; index++) {
        agent.destroy(RIGHT)
        agent.move(FORWARD, 1)
    }
})
```

```ghost
player.onChat("run", function () {
    for (let index = 0; index < 4; index++) {
        if (agent.detect(AgentDetection.Block, FORWARD)) {
            agent.destroy(FORWARD)
            agent.move(FORWARD, 1)
            agent.interact(FORWARD)
            agent.setItem(REDSTONE_BLOCK, 1, 1)
            agent.place(FORWARD)
            agent.turn(LEFT_TURN)
        }
    }
})
```
