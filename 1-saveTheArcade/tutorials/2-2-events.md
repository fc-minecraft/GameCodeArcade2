# Controlling the agent

### @explicitHints 1

### @activities true

## Первое задание

### Разрушение агента

Открой категорию "АГЕНТ" и перетащи блок "агент разрушить" в блок "при команде в чате" с названием **разрушить**.

Попробуй заставить агента разрушить блок на его пути. Отправь команду **разрушить** в чат Minecraft, чтобы запустить код в блоке "при команде в чате" с названием **разрушить**.


#### ~ tutorialhint


```blocks
player.onChat("destroy", function () {
    agent.destroy(FORWARD)
})
```

```template
player.onChat("destroy", function () {
	
})
```
