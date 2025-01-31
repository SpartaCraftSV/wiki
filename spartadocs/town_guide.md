---
layout: default
title: Town
nav_order: 5
description: "Town Guide"
permalink: town-guide
---

# Create a town
{: .fs-9 }

<img src="/assets/images/town.jpeg" alt="town-image"/>

{: .mt-5 }
{: .caution }
Towns automatically get deleted after 60 days of inactivity if no single resident has joined the server in that period of time.

## The essentials

1. Find a town to join. You may either request invitation or join an open town. Once invited, type `/accept` or click the prompt in chat. You can join open towns via `/t join [town]`.

2. Creating a town costs 64 gold ingots. Once you earned the required amount of gold, go to the location where you want the town to be. 
Then, type `/t new [name]` and accept the prompt. It will create a town with a single chunk.

3. Basic commands for towns:
- `/t spawn` teleports you to town's spawn.
- `/t invite [player]` invites players to your town.
- `/t leave` allows you to leave town. It must not be owned by you.

4. Claiming more land costs gold. One chunk costs 25 gold ingots. Stand in unclaimed chunk and type `/t claim`. Be sure you deposited the required amount in town bank via `/t deposit [amount]`.

5. Your town can join a nation via `/n join [name]` (or be invited as well). You can only join nations whose capital's homeblock is within 3000 blocks of your town's homeblock. The nation must either be open as seen on `/n [nation]`, or your town has to be invited. Accept the invite using `/t invite accept [nation]`.

{: .tip }
Avoid giving your residents a pre-made house and too much free gear. Let your residents grow and develop with your town. This improves resident retention.

## Town permissions

Town permissions manage what residents have access to interact with inside a town. There are 4 permission types:

- Build: Place blocks inside the town.
- Destroy: Destroy blocks inside the town.
- Switch: Interact with chests, furnaces, levers, hoppers, droppers, and blocks with similar nature.
- Item: Interact with water, lava, buckets, lighters, bone meal, ender pearls, bottles, and items of similar nature.

All town permissions are disabled by default, as a mayor you can grant permissions by giving ranks with `/t rank add [player] [rank]` or by selling individual plots to residents with `/plot fs [price]`. It's also possible to change permissions specifically for allies and outsiders. For example, `/t set perm ally build on` would allow residents of allied nations to build inside the town. You can interact this way with individual chunks (called plots), too. More on that later.

##  Plots

Plots are used to manage land inside the town. Plots can be sold to residents, have different properties and different permissions. Individual plots have the exact same size as town claims and Minecraft chunks which can be conveniently displayed with the chunk debug screen toggled with `F3+G`.

A mayor can add land to a town by claiming nearby wilderness for a cost of 25 gold `/t claim`. Read more about claiming [here]. A mayor or other high-ranking town members can change permissions of individual plots and sell plots to residents. Residents can buy plots in their own town, but can't add new land to a town. This can cause confusion, especially since “plots” and “claims” are sometimes used interchangeably within the community.

Plots are useful since they allow towns to be divided for different purposes and town residents. A newly claimed chunk has the default plot settings/permissions and is only accessible by the mayor and residents with appropriate town ranks. A mayor or plot owner can put the plot up for sale by standing in the plot and running command `/plot fs [price]`. This allows town residents to buy it. To buy a plot, stand inside it and run command `/plot claim`. Buying a plot gives you full permissions to that 16x16 plot of land. Run `/plot unclaim` to remove yourself from the plot.

{: .tip }
Remember that a resident is an asset to your town and it can often make sense to give plots away for free. Residents are likely to leave if they don't find anywhere to build. Make it easy for new residents to find plots for sale.

### Plot types

Once you have access to a plot you may alter it in several ways. The first thing is to select what type of plot it is. Different types of plots have different types of properties. A plot can not have multiple types set at the same time. Set plot type with command `/plot set [type]`.

| Plot type    | Description       | 
|:-------------|:------------------|
| Default      | The default plot type. Useful for personal builds, such as homes or other forms of town bases.  |
| Shop         | Required in order to create shops. |
| Arena        | Enables PvP inside the plot.   |
| Farm         | Allows nation residents to harvest farms inside the plot, but not break any other types of blocks. It's also possible to damage mobs in farm plots.      |
| Embassy      | This allows any player to buy the plot, regardless of what town they may belong to. Owning an embassy and changing plot type will still make you the owner. This is useful when creating shops in different towns, expanding your markets abroad. |
| Inn          | Allows other than plot owner to use beds inside the plot. |

### Plot permissions

It's possible to alter individual plot permissions. Plot permissions override global town permissions and work very similar to town permissions. Run `/plot set [build/destroy/switch/itemuse]`. Please see town permission section for explanation of what each permission type covers.

It's also possible to toggle certain behaviors inside the plot. Run `/plot toggle [explosion/fire/mobs/pvp]`.

### Plot commands summary

|Command	|Description|
|:-------------|:------------------|
|/plot fs price	|Set plot for sale|
|/plot claim	|Buy available plot|
|/plot unclaim	|Remove yourself from plot|
|/plot set type	|Set type of plot|
|/plot set perm [build/destroy/switch/itemuse]	|Settings for plot|
|/plot toggle [explosion/fire/mobs/pvp]	|Toggle specific values for plot|

## Town ranks

Mayors can give ranks to residents with `/t rank add [player] [rank]`.

- ***Councillor*** gives the player full access to town plots regardless of ownership, access to most town commands excluding `/t unclaim`, `/t set mayor <player>`, `/t delete`, etc. This rank should only be given to the most trusted citizens as it could be detrimental to your town. They can kick everyone except the mayor and other councillors, withdraw gold from the town bank and edit town/plot's permissions.

- ***Settlers*** can claim chunks for the town with `/t claim`.

- ***Recruiters*** are able to invite other players with `/t add [player]`.

- ***Sherif*** might add users to the town outlaw list with `/t outlaw add [player]`.

- ***Treasurers*** are allowed to use `/t withdraw [amount]` to withdraw gold from the town bank.

## Town commands

|Command	|Description|
|:-------------|:------------------|
|/t [town]	|View information on specific town|
|/t invite [player]	|Invite player to town|
|/t here	|Shows information on town at current location|
|/t list	|List of all towns|
|/t leave	|Leave town|
|/t new [name]	|Create a new town|
|/t add [player]	|Add resident to town|
|/t kick [player]	|Kick resident from town|
|/t spawn	|Teleport to town spawn|
|/t claim	|Claim chunk|
|/t withdraw [amount]	|Withdraw gold from town bank|
|/t deposit [amount]	|Deposit gold to town bank|
|/t rank [add/remove][player] [rank]	|Add/remove a town rank|
|/t set [board/mayor/homeblock/perm]	|Settings for town|
|/t toggle [explosion/fire/mobs/pvp]	|Toggle specific values for town|

[here]: /claiming-land