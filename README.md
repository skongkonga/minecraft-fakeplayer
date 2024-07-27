# FakePlayer

[简体中文](README_zh.md)

This is a plugin inspired by Carpet Mod which allows you to spawn fake players to keep chunk loading.

## Supported Versions

Only supports [Paper](https://papermc.io) and [Purpur](http://purpurmc.org)

Required JAVA 21+

+ supports `1.20`, `1.20.2`, `1.20.3`, `1.20.4`, `1.20.5`, `1.20.6`
+ supports `1.21`

## Requirement plugins:

- [CommandAPI](https://commandapi.jorel.dev)

## Features

1. You can spawn some fake players that look like real to the server.
2. Most commands can work on them such as `/ban`, `/kick`, `/pay`
3. You can open their backpack and put your stuff into it.
4. You can have them perform actions like moving, jumping, attacking, and eating. What's better? You can make it periodical!
5. Let your imagination run wild, have them do more things.

## Commands

| Command       | Function                                 | Permission                   | Note                                                               |
|---------------|------------------------------------------|------------------------------|--------------------------------------------------------------------|
| /fp spawn     | Spawn fake player                        | fakeplayer.command.spawn     |                                                                    |
| /fp kill      | Kill fake player                         | fakeplayer.command.kill      |                                                                    |
| /fp killall   | Kill all fake players on the server      | OP                           |                                                                    |
| /fp select    | Select fake player                       | fakeplayer.command.select    | Appears only when player spawned more then 1 fake players          |
| /fp selection | View selected fake player                | fakeplayer.command.selection | Appears only when player spawned more then 1 fake players          |
| /fp list      | View summoned fake players               | fakeplayer.command.list      |                                                                    |
| /fp distance  | View distance to fake player             | fakeplayer.command.distance  |                                                                    |
| /fp drop      | Drop held item                           | fakeplayer.command.drop      |                                                                    |
| /fp dropstack | Drop entire stack held item              | fakeplayer.command.dropstack |                                                                    |
| /fp dropinv   | Drop all items in inventory              | fakeplayer.command.dropinv   |                                                                    |
| /fp skin      | Copy player skin                         | fakeplayer.command.skin      | 60 seconds cooldown if copy from a offline player                  | 
| /fp invsee    | View fake player inventory               | fakeplayer.command.invsee    | Right-clicking on fake players has the same effect                 |
| /fp sleep     | Sleep in bed                             | fakeplayer.command.sleep     |                                                                    |
| /fp wakeup    | Wake up from bed                         | fakeplayer.command.wakeup    |                                                                    |
| /fp status    | View player status                       | fakeplayer.command.status    |                                                                    |
| /fp respawn   | Respawn dead fake player                 | fakeplayer.command.respawn   | Appears only when server config does not kick on fake player death |
| /fp tp        | Teleport to fake player                  | fakeplayer.command.tp        |                                                                    |
| /fp tphere    | Teleport fake player to self             | fakeplayer.command.tphere    |                                                                    |
| /fp tps       | Swap positions with fake player          | fakeplayer.command.tps       |                                                                    |
| /fp set       | Change fake player configuration         | fakeplayer.command.set       |                                                                    |
| /fp config    | Change default fake player configuration | fakeplayer.command.config    |                                                                    |
| /fp expme     | Absorb fake player experience            | fakeplayer.command.expme     |                                                                    |
| /fp attack    | Attack                                   | fakeplayer.command.attack    |                                                                    |
| /fp mine      | Mine                                     | fakeplayer.command.mine      |                                                                    |
| /fp use       | Use/Interact/Place                       | fakeplayer.command.use       |                                                                    |
| /fp jump      | Jump                                     | fakeplayer.command.jump      |                                                                    |
| /fp turn      | Turn around                              | fakeplayer.command.turn      |                                                                    |
| /fp look      | Look at specified location               | fakeplayer.command.look      |                                                                    |
| /fp move      | Move                                     | fakeplayer.command.mvoe      |                                                                    |
| /fp ride      | Ride                                     | fakeplayer.command.ride      |                                                                    |
| /fp sneak     | Sneak                                    | fakeplayer.command.sneak     |                                                                    |
| /fp swap      | Swap main and off-hand items             | fakeplayer.command.swap      |                                                                    |
| /fp hold      | Hold corresponding hotbar item           | fakeplayer.command.hold      |                                                                    |
| /fp cmd       | Execute command                          | fakeplayer.command.cmd       |                                                                    |
| /fp reload    | Reload config file                       | OP                           |                                                                    |

_In addition, fake players are recognized by any command, such as `kick`, `tp`, `ban`, etc._

## Permissions

In fact, each command has its permission. But you still can use the following permission packs.

### Basic Command Group Permissions

`fakeplayer.spawn` includes the following permissions:

- fakeplayer.command.spawn - Create fake player
- fakeplayer.command.kill - Kill fake player
- fakeplayer.command.list - List fake players
- fakeplayer.command.distance - View distance
- fakeplayer.command.select - Select fake player
- fakeplayer.command.selection - View selected fake player
- fakeplayer.command.drop - Drop an item
- fakeplayer.command.dropstack - Drop entire stack of items
- fakeplayer.command.dropinv - Drop all inventory items
- fakeplayer.command.skin - Copy skin
- fakeplayer.command.invsee - View inventory
- fakeplayer.command.status - View status
- fakeplayer.command.respawn - Respawn fake player
- fakeplayer.command.config - Set default settings
- fakeplayer.command.set - Set fake player settings

### Teleportation Group Permissions

`fakeplayer.tp` includes the following permissions:

- fakeplayer.command.tp
- fakeplayer.command.tphere
- fakeplayer.command.tps

### Action Control Permissions

`fakeplayer.action` includes the following permissions:

- fakeplayer.command.attack - Attack
- fakeplayer.command.mine - Mine
- fakeplayer.command.use - Use
- fakeplayer.command.jump - Jump
- fakeplayer.command.sneak - Sneak
- fakeplayer.command.look - Look
- fakeplayer.command.turn - Turn
- fakeplayer.command.move - Move
- fakeplayer.command.ride - Ride
- fakeplayer.command.swap - Swap main and off-hand items
- fakeplayer.command.sleep - Sleep
- fakeplayer.command.wakeup - Wake up
- fakeplayer.command.hold - Switch hotbar
- fakeplayer.config.replenish - Auto-replenish
- fakeplayer.config.replenish.chest - Can replenish from nearby chests when auto-replenishing

If your server does not restrict various player commands, you can use this directly.
`fakeplayer.basic` includes all secure permissions, except for `/fp cmd` commands.

## Interaction

+ Right-clicking on a fake player allows you to view their inventory.

## Player Personalized Configuration

This is the personalized configuration of each player's created fake player. After modifying the configuration, the next time a fake player is created, it will take effect.

Command examples:

+ `/fp config list` - View all personalized configurations
+ `/fp config set collidable false` - Set personalized configuration

| Configuration Item | Note                                                                                                                                |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| collidable         | Whether collision box is enabled                                                                                                    |
| invulnerable       | Whether invincible mode is enabled                                                                                                  |
| look_at_entity     | Automatically look at nearby attackable entities (including players), can be combined with `attack` to automatically fight monsters |
| pickup_items       | Whether to pick up items                                                                                                            |
| skin               | Whether to use your skin                                                                                                            |
| replenish          | Whether to auto-replenish                                                                                                           |


# FAQs (Important - Must Read)

## Fake players do not attract aggression

By default, fake players are in invincible mode. Players need to manually turn off invincible mode with `/fp config set invulnerable false` to attract aggression. After turning it off, they will
receive hunger and health effects. You may need to use `res` or beacon to ensure the fake player's `hunger` and `health`.

## Fake players automatically log out after a while

This may be because plugins like `AutheMe` detect that fake players have not logged in for a long time. You can include the login command in the configuration file's `self-commands` to prevent the
plugin from kicking out players for being idle:

```yaml
# Note: You should use a complex password, or AuthMe may reject it
self-commands:
  - '/register abc123! abc123!'
  - '/login abc123!'
