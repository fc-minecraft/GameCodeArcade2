# If

### @explicitHints 1

### @activities true

## First Activity

### Making decisions

Some problems involve performing actions over and over, but other actions are not necessarily repeated consistently.  An ``||logic:if||`` block can simplify code by determining when it is appropriate to perform a certain action.
An ``||logic:if||`` block is another type of **compound statement block**.  It uses a **condition** to determine whether to run its code.  If the condition is true, then the code inside the ``||logic:if||`` block will run.

#### ~ tutorialhint

A **condition** can be true or false.  **Condition blocks** have a distinct pointed shape to indicate that they fit where a condition is expected.

### Agent detect

Try using an ``||logic:if||`` block and an ``||agent:agent detect||`` block to make the ``||agent:agent destroy||`` only solid blocks.
From the ``||logic:LOGIC||`` category drag an ``||logic:if||`` block inside the ``||loops:repeat||`` block.
From the ``||agent:AGENT||`` category drag an ``||agent:agent detect||`` block and place it where it fits inside the ``||logic:if||`` block.

#### ~ tutorialhint

```blocks
player.onChat("fix", function () {
    for (let index = 0; index < 12; index++) {
        if (agent.detect(AgentDetection.Block, FORWARD)) {
        }
        agent.move(FORWARD, 1)
    }
})
```
### Determining the condition

The ``||agent:agent detect||`` block can determine whether there is a solid block next to the agent.

Be sure to specify the correct direction in the ``||agent:agent detect||`` block. Also, the ``||loops:repeat||`` block is already set to run the correct number of times.

#### ~ tutorialhint

If there is a block, then ``||agent:agent detect||`` returns a value of **true**.  Items that the agent can walk through (such as torches, buttons, and levers) cause ``||agent:agent detect||`` to return a value of **false**.

### If true...

If the agent does ``||agent:agent detect||``  a block to the right, we want the agent to ``||agent:agent destroy||``  the block. Inside the ``||logic:if||`` block, add ``||agent:agent destroy||`` **right**.
Whether or not the agent **detects** a block to destroy, when it is complete, we need it to move forward. Let's add an ``||agent:agent move||`` **forward** after the ``||logic:if||`` block.

#### ~ tutorialhint

```blocks
player.onChat("fix", function () {
    for (let index = 0; index < 12; index++) {
        if (agent.detect(AgentDetection.Block, RIGHT)) {
            agent.destroy(RIGHT)
        }
        agent.move(FORWARD, 1)
    }
})
```

### Review

Some problems can be simplified by using an ``||logic:if||`` block to run certain sections of code based on a condition.

Code with a condition can determine whether a specific section of code will run, which eliminates the need for manually coding every single step.

#### ~ tutorialhint

```blocks
player.onChat("fix", function () {
    for (let index = 0; index < 12; index++) {
        if (agent.detect(AgentDetection.Block, RIGHT)) {
            agent.destroy(RIGHT)
        }
        agent.move(FORWARD, 1)
    }
})
```

```template
player.onChat("fix", function () {
    for (let index = 0; index < 12; index++) {
    }
})
```

```ghost
player.onChat("run", function () {
    for (let index = 0; index < 12; index++) {
        if (agent.detect(AgentDetection.Block, FORWARD)) {
            agent.destroy(FORWARD)
            agent.move(FORWARD, 1)
        }
    }
})
```
