---
description: by Phottor
---

# Mining mechanics

## **Mining mechanics in Settlers IV**&#x20;

![Coordinate system on a hexagonal map, such as the ones used by the game.](../.gitbook/assets/hexagonal_map_sample.png)

Geologists never place two signs onto adjacent tiles, unless two of them happen to be working on adjacent tiles at the same time. Usually, they leave at least one free tiles in every direction, sometimes more.

Internally, each resource deposit has a fill state between 1 and 15. This exactly corresponds to the amount of resources that can be extracted from that tile. If a resources is extracted, the fill state is reduced by one. A sign with one visible icon signifies a tile with a fill state of 1 up to 5, a sign with two icons signifies a fill state of 6 up to 10, and a sign with three icons signifies a fill state of 11 up to 15.

On random maps, all resource desposits found on mountains always have the exact same shape and size, unless it is on a mirror axis, is overwritten by another deposit during generation, or is generated at the edge of the mountain with parts of it ending up outside of mountain terrain. The orientation of the overall shape also slightly differs depending on which quadrant the deposit is in if it is a mirrored map. On HGXX all tiles that have a resource start with a fill state of 15. On MGXX and LGXX a random variance is applied, but overall, the average should not deviate too much. This also means that players should not pay too much attention to the amount of signs placed by geologists.

{% tabs %}
{% tab title="Gold" %}
![Gold](../.gitbook/assets/gold_spot.png)
{% endtab %}

![Coal](https://media.discordapp.net/attachments/576807103256068102/850486127903375410/unknown.png)
{% tab title="Coal" %}
![Coal](../.gitbook/assets/coal_spot.png)
{% endtab %}

![Iron](https://media.discordapp.net/attachments/576807103256068102/850486164652818432/unknown.png)
{% tab title="Iron" %}
![Iron](../.gitbook/assets/iron_spot.png)
{% endtab %}

![Stone](https://media.discordapp.net/attachments/576807103256068102/850486195997638656/unknown.png)
{% tab title="Stone" %}
![Stone](../.gitbook/assets/stone_spot.png)
{% endtab %}

![Sulfur](https://media.discordapp.net/attachments/576807103256068102/850486232282955836/unknown.png)
{% tab title="Sulfur" %}
![Sulfur](../.gitbook/assets/sulfur_spot.png)
{% endtab %}
{% endtabs %}
A mine can extract resources from it's hotspot and four additional tiles in each direction, for 64 tiles in total. This means that on a Metzel map, a single mine can extract 64\*15=960 resources over it's lifetime. However, as efficiency drops sharply towards the end, a massive amount of food would be required to extract the last few resources. Mines can also extract resources from tiles outside the player's borders.

![Working Area](../.gitbook/assets/mine_working_area.png)

For each piece of a miner's favorite food, the miner will make 10 attempts to extract resources. He will also make 10 attempts "for free" after the mine is built. For each attempt, the mine will randomly pick one of the 64 tiles it it's working area. If the tile is empty, has the wrong resource, is covered with snow, or not a mountain tile at all, the miner will fail to extract a resource. If a tile with the correct resource is found, the fill state comes into play. If it is >= 4, a resource will be extracted. If it is less, the chance of success is 25%\*fill state.&#x20;

This means that the initial efficiency of a mine on 2-icon-signs is exactly equal to a mine on 3-icon-signs. But the former will lose efficiency much sooner than the latter.

The efficiency bar only show the success quota for the last 15 mining attempts. This means that even a mine on a small deposit can temporarily show 100% efficiency, while a mine that is starting to lose efficiency can temporarily drop to 0% if the miner had particular good or bad luck.

For a gold deposit, there are 19 tiles where a mine can fully encompass it. For iron, stone or sulphur mines, there are 11 such tiles. Coal deposits only have a single tile where the mine can perfectly cover the entire deposit. The image bewow illustrates this, along with a rough estimate on the efficiency loss if the placement is off.

![Mine placement](../.gitbook/assets/mineplacement.jpg)

\
