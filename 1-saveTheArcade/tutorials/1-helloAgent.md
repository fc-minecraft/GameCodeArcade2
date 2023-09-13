# Hello, Agent.

### @explicitHints 1

### @activities true

## First Activity

### Events

The ``||loops:on start||`` block is an **event block**.  An event block runs its code when a certain event occurs.

For the ``||loops:on start||`` block, pressing the Play button is the event that triggers this event block.

#### ~ tutorialhint

The shape of an **event block** allows other code blocks to fit inside it.

### Statements

The ``||player:say||`` block is a **statement block**.  A statement block performs an action.

The text in the ``||player:say||`` block says "Hello, Agent." Press the Play button to run the code and display the text in chat.

#### ~ tutorialhint

The shape of a **statement block** allows it to fit inside an event block.

### Review

With the ``||player:say||`` block inside the ``||loops:on start||`` block, pressing the Play button sends a message in the Minecraft chat.

#### ~ tutorialhint

```blocks
player.say("Hello, Agent.")
```

```template
player.say("Hello, Agent.")
```
