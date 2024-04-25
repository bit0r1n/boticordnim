<p align="center">
    <img src="https://cdn.bitor.in/botiheh.png" width="560">
</p>

<p align="center">
    Utility for interaction with Boticord API on Nim
</p>

[API Reference](https://bit0r1n.github.io/boticordnim)

## Installation

Enter this command to install package
```
nimble install https://github.com/bit0r1n/boticordnim
```

## Examples

Get info from some resources

```nim
import boticordnim/[bots, users, servers]
import asyncdispatch, strformat

let
  botId = "974297735559806986"
  bot = waitFor getBot(botId) # or getBot(id = botId)
  
  serverId = "992158889116180502"
  server = waitFor getServer(serverId)
  
  userId = "267729391172321290"
  user = waitFor getUser(userId)

echo fmt"Name of {botId} resource (bots): {bot.name}"
echo fmt"Name of {serverId} resource (servers): {server.name}"
echo fmt"Name of {userId} resource (users): {user.username}"
```

Other examples are located in [examples folder](/examples)