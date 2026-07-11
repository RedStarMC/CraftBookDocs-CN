==============
更好的活塞 Better Pistons
==============

**更好的活塞（BetterPistons）** 机制允许活塞实现更多功能。

目前有 4 种活塞机制：

* 压碎（Crush）
* 弹射（Bounce）
* 超级粘性（SuperSticky）
* 超级推动（SuperPush）

可以在配置中设置黑名单，以阻止特定方块与每种活塞机制交互。

使用多个功能 Using Multiple
==============

可以在同一活塞上放置多个告示牌来组合使用多种活塞机制。这些告示牌也可以堆叠在一起。

活塞类型 Piston Types
============

压碎 Crush
-----

**压碎（Crush）** 机制会破坏活塞头所推入的方块。

需要在活塞上附着告示牌，第二行为 ``[Crush]``。当活塞被充能时，活塞伸入的方块将被摧毁。

此机制还可以选择配置为对碰撞到的生物和玩家造成伤害。

弹射 Bounce
------

**弹射（Bounce）** 机制将方块和实体沿活塞方向弹射出去。

需要在活塞上附着告示牌，第二行为 ``[Bounce]``，第三行可选填弹射速度。

.. note::
    由于 Minecraft 的限制，速度超过 10 将无法生效。

超级粘性 SuperSticky
-----------

**超级粘性（SuperSticky）** 机制允许拉取距离超过 1 格的方块。

需要在活塞上附着告示牌，第二行为 ``[SuperSticky]``。

第三行表示拉取方块的最大距离以及移动的格数，以冒号分隔。

例如，要将 10 格外的方块移动 1 格，请输入 ``10:1``。

如果最后一行是 ``AIR``，则获得将空气当作实体方块拉取的能力。

超级推动 SuperPush
---------

**超级推动（SuperPush）** 机制也允许活塞推动空气。

需要在活塞上附着告示牌，第二行为 ``[SuperPush]``。

第三行表示拉取方块的最大距离以及移动的格数，以冒号分隔。

例如，要将 10 格外的方块移动 1 格，请输入 ``10:1``。

权限 Permissions
===========

+---------------------------------------------+-----------------------------------------------------+
|  权限节点 Permission Node                   |  效果 Effect                                        |
+=============================================+=====================================================+
|  craftbook.betterpistons.bounce.create      |  允许创建“弹射”类更好的活塞。                        |
+---------------------------------------------+-----------------------------------------------------+
|  craftbook.betterpistons.crush.create       |  允许创建“压碎”类更好的活塞。                        |
+---------------------------------------------+-----------------------------------------------------+
|  craftbook.betterpistons.supersticky.create |  允许创建“超级粘性”类更好的活塞。                    |
+---------------------------------------------+-----------------------------------------------------+
|  craftbook.betterpistons.superpush.create   |  允许创建“超级推动”类更好的活塞。                    |
+---------------------------------------------+-----------------------------------------------------+

配置 Configuration
=============

.. csv-table::
  :header: 节点, 说明, 默认值
  :widths: 15, 30, 10

  ``enable-crush``,"启用压碎机制。","true"
  ``crush-kills-mobs``,"使压碎不仅能破坏方块，还能杀死生物（包括玩家）。","false"
  ``crush-block-blacklist``,"压碎活塞无法破坏的方块列表。","[minecraft:obsidian, minecraft:bedrock, minecraft:nether_portal, minecraft:end_portal, minecraft:end_portal_frame, minecraft:end_gateway]"
  ``enable-super-sticky``,"启用超级粘性机制。","true"
  ``enable-super-push``,"启用超级推动机制。","true"
  ``movement-blacklist``,"与移动相关的更好活塞无法交互的方块列表。","[minecraft:obsidian, minecraft:bedrock, minecraft:nether_portal, minecraft:end_portal, minecraft:end_portal_frame, minecraft:end_gateway]"
  ``enable-bounce``,"启用弹射机制。","true"
  ``bounce-blacklist``,"弹射活塞无法弹射的方块列表。","[minecraft:obsidian, minecraft:bedrock, minecraft:nether_portal, minecraft:end_portal, minecraft:end_portal_frame, minecraft:end_gateway]"
  ``max-distance``,"更好的活塞可以与方块交互的最大距离。","12"
  ``bounce-max-velocity``,"弹射活塞可使用的最大速度。","5.0"