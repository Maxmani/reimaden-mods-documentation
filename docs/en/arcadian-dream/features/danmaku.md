# Danmaku

## Introduction

Danmaku (弾幕, "barrage", lit. "bullet curtain"), also known as Bullet Hell, is a sub-genre of shoot 'em up video games featuring complex patterns of dozens to hundreds of enemy bullets. The Touhou Project games are a well-known example of this genre.

In the context of Arcadian Dream, danmaku is a system that allows you to create bullet patterns and use them in combat. Naturally, there are also enemies that use danmaku against you. In a sense, danmaku is this mod's equivalent of magic.

## Getting Started

To begin creating your own danmaku, you will need a few materials. The main source of these materials are the various enemies in the mod.

!!! note

    Which material does what can be modified using tags.


Icon | Material | Description
-----|----------|------------
<img alt="Power Item" width="16" src="https://raw.githubusercontent.com/Maxmani/arcadian-dream/HEAD/src/main/resources/assets/arcadiandream/textures/item/power_item.png"/> | Power Item | Used to increase the power of bullets.
<img alt="Big Power Item" width="16" src="https://raw.githubusercontent.com/Maxmani/arcadian-dream/HEAD/src/main/resources/assets/arcadiandream/textures/item/big_power_item.png"/> | Big Power Item | Used to increase the amount of bullets in a single shot. Also used to create the initial Shot item.
<img alt="Point Item" width="16" src="https://raw.githubusercontent.com/Maxmani/arcadian-dream/HEAD/src/main/resources/assets/arcadiandream/textures/item/point_item.png"/> | Point Item | Used to increase the speed of bullets.
<img alt="Max Point Item" width="16" src="https://raw.githubusercontent.com/Maxmani/arcadian-dream/HEAD/src/main/resources/assets/arcadiandream/textures/item/max_point_item.png"/> | Max Point Item | Has no use currently.
<img alt="Star Item" width="16" src="https://raw.githubusercontent.com/Maxmani/arcadian-dream/HEAD/src/main/resources/assets/arcadiandream/textures/item/star_item.png"/> | Star Item | Used to increase the duration of bullets. Also used to create Bullet Cores.
<img alt="Faith Item" width="16" src="https://raw.githubusercontent.com/Maxmani/arcadian-dream/HEAD/src/main/resources/assets/arcadiandream/textures/item/faith_item.png"/> | Faith Item | Used to repair Shot items.
<img alt="Time Orb" width="16" src="https://raw.githubusercontent.com/Maxmani/arcadian-dream/HEAD/src/main/resources/assets/arcadiandream/textures/item/time_orb.png"/> | Time Orb | Permanently halves the cooldown of a shot.
<img alt="Enchanted Ice" width="16" src="https://raw.githubusercontent.com/Maxmani/arcadian-dream/HEAD/src/main/resources/assets/arcadiandream/textures/item/enchanted_ice.png"/> | Enchanted Ice | Makes a shot apply freezing on hit.

The first step is to create a Bullet Core. Each bullet type has an equivalent Bullet Core. These can be crafted using Star Items in a regular crafting table.

!!! note

    Each bullet type has its own base and max stats.

Icon | Bullet Type | Notes
-----|-------------|-----------
![Circle](../../../assets/images/circle_shot.png) | Circle |
![Bubble](../../../assets/images/bubble_shot.png) | Bubble | Has a quite large hitbox.
![Amulet](../../../assets/images/amulet_shot.png) | Amulet | Deals more damage to undead mobs.
![Star](../../../assets/images/star_shot.png) | Star | Ignores armor.
![Kunai](../../../assets/images/kunai_shot.png) | Kunai | Pierces through enemies.
![Pellet](../../../assets/images/pellet_shot.png) | Pellet | Has high max density.

To turn a core into a usable Shot, you will need a Danmaku Crafting Table.

## Danmaku Crafting Table

The Danmaku Crafting Table is a block that allows you to create, repair and modify Shot items.

![Danmaku Crafting Table](../../../assets/images/danmaku_crafting_table.png)

1. Core
2. Shot
3. Modifier
4. Repair
5. Pattern
6. Color
7. Result

Placing a core in the core slot and a Big Power Item in the modifier slot will result in a Shot item. From there you can place it in the shot slot to repair it using Faith Items in a repair slot or modifying it using other materials and slots.

<figure markdown>
  ![Danmaku Crafting Example](../../../assets/images/danmaku_crafting_example1.png){width="326"}
  <figcaption>An example of crafting a shot.</figcaption>
</figure>

<figure markdown>
  ![Danmaku Crafting Example](../../../assets/images/danmaku_crafting_example2.png){width="326"}
  <figcaption>An example of modifying and repairing a shot.</figcaption>
</figure>

## Using Danmaku

After getting your hands on a Shot, you can use it like any other throwable projectile. Keep in mind that the shot's density affects the durability. Shots cannot break, only become unusable until repaired.

There is also a cooldown between shots. Modifying a shot in any way will increase the cooldown, up to a maximum based on the bullet type.

Bullets deal their own type of damage, so they are not affected by things like Projectile Protection. There is a new enchantment called Danmaku Protection that can be applied to armor to reduce the damage taken from bullets.

## Patterns

By default, shots come with the "spread" pattern. This pattern will fire a single bullet in the direction you are looking. If there are multiple bullets in a single shot, they will have divergence applied to them based on the density.

More patterns can be found around the Minecraft world in the form of templates. Once found, a Pattern Template can be crafted into a Bullet Pattern item, which can then be placed in the pattern slot of a Danmaku Crafting Table.

Pattern items can be duplicated using an existing pattern, some materials and a shot.

Icon | Pattern | Location
-----|---------|---------
<img alt="Spread Pattern" width="16" src="https://raw.githubusercontent.com/Maxmani/arcadian-dream/HEAD/src/main/resources/assets/arcadiandream/textures/item/spread_pattern.png"/> | Spread | Shipwreck
<img alt="Ray Pattern" width="16" src="https://raw.githubusercontent.com/Maxmani/arcadian-dream/HEAD/src/main/resources/assets/arcadiandream/textures/item/ray_pattern.png"/> | Ray | Pillager Outpost
<img alt="Ring Pattern" width="16" src="https://raw.githubusercontent.com/Maxmani/arcadian-dream/HEAD/src/main/resources/assets/arcadiandream/textures/item/ring_pattern.png"/> | Ring | Nether Fortress & Abandoned Shrine
<img alt="Arc Pattern" width="16" src="https://raw.githubusercontent.com/Maxmani/arcadian-dream/HEAD/src/main/resources/assets/arcadiandream/textures/item/arc_pattern.png"/> | Arc | Ancient City
<img alt="Double Pattern" width="16" src="https://raw.githubusercontent.com/Maxmani/arcadian-dream/HEAD/src/main/resources/assets/arcadiandream/textures/item/double_pattern.png"/> | Double | Mineshaft
<img alt="Triple Pattern" width="16" src="https://raw.githubusercontent.com/Maxmani/arcadian-dream/HEAD/src/main/resources/assets/arcadiandream/textures/item/triple_pattern.png"/> | Triple | Stronghold

## Cancelling Bullets and Extends

Icon | Item
-----|-----
<img alt="Bomb Item" width="16" src="https://raw.githubusercontent.com/Maxmani/arcadian-dream/HEAD/src/main/resources/assets/arcadiandream/textures/item/bomb_item.png"/> | Bomb Item
<img alt="Extend Item" width="16" src="https://raw.githubusercontent.com/Maxmani/arcadian-dream/HEAD/src/main/resources/assets/arcadiandream/textures/item/extend_item.png"/> | Extend Item
<img alt="Life Fragment" width="16" src="https://raw.githubusercontent.com/Maxmani/arcadian-dream/HEAD/src/main/resources/assets/arcadiandream/textures/item/life_fragment.png"/> | Life Fragment

Bullets that are not your own can be cancelled using a Bomb Item. This removes all nearby bullets and gives you some Star Items in return. Bombs are quite uncommon, so use them wisely.

There is also the Extend Item, which acts as an equipable Totem of Undying. It will cancel bullets similar to a Bomb, but won't give you any Star Items. It also grants temporary invulnerability. It is a rare drop from certain mobs.

Extends can be turned into Life Fragments and vice versa.
