=============
弹跳方块 Bounce Blocks
=============

**弹跳方块（Bounce Blocks）** 机制引入了特殊的方块，当玩家在其上跳跃或行走时会被弹射出去。

建造方法
============

弹跳方块由两部分组成：一个来自配置允许列表的方块，以及一个直接放置在该方块下方的告示牌。

告示牌的第二行必须匹配以下告示牌类型之一，以决定弹跳方块的触发方式，第三行可选配置弹跳速度。

告示牌类型 Sign Types
----------

* ``[Jump]`` —— 当玩家在上方方块上跳跃时触发的弹跳方块告示牌。
* ``[Launch]`` —— 当玩家走上上方方块时触发的弹跳方块告示牌。

弹跳速度 Bounce Velocity
---------------

默认情况下，弹跳方块会将玩家以 0.5 的垂直速度弹起，但可以通过在告示牌第三行指定不同的值来更改。

例如，要指定 1.0 的垂直速度，第三行只需写上 ``1.0``。

但不仅仅只有向上的速度选项。你还可以通过提供多个以逗号分隔的值来同时指定“向前”和“侧向”速度。

例如，要以 0.5 的速度向前推进玩家，同时以 1 的速度向上弹起，第三行应写上 ``0.5,1,0``。

虽然这看起来像 X、Y、Z 坐标，但它实际上是相对于玩家自身的。因此，X 指向前，Y 指向上，Z 指向侧向。这意味着无论玩家从哪个方向过来，他们都会被向前弹射。

绝对速度 Absolute Velocities
~~~~~~~~~~~~~~~~~~~

如果你希望弹跳方块始终向某个固定方向弹射，例如用于跑酷课程或某个单一目的地的系统，你可以在第三行开头添加 ``!``。这会将弹跳方块切换为使用实际游戏坐标，而不是相对于玩家移动方向。

例如，要以 1.0 的速度将玩家向上和向 Z 轴负方向弹射，第三行应写上 ``!0,1,-1``。

配置 Configuration
=============

.. csv-table::
  :header: 节点, 说明, 默认值
  :widths: 15, 30, 10

  ``blocks``,"可用作弹跳方块的方块列表。","[minecraft:black_terracotta, minecraft:blue_terracotta, minecraft:brown_terracotta, minecraft:cyan_terracotta, minecraft:gray_terracotta, minecraft:green_terracotta, minecraft:light_blue_terracotta, minecraft:light_gray_terracotta, minecraft:lime_terracotta, minecraft:magenta_terracotta, minecraft:orange_terracotta, minecraft:pink_terracotta, minecraft:purple_terracotta, minecraft:red_terracotta, minecraft:terracotta, minecraft:white_terracotta, minecraft:yellow_terracotta]"
  ``sensitivity``,"触发方块所需移动灵敏度。","0.1"

权限 Permissions
===========

.. csv-table::
  :header: 权限节点 Permission Node, 效果 Effect
  :widths: 20, 30

  ``craftbook.bounceblocks.create``,"允许创建弹跳方块告示牌"
  ``craftbook.bounceblocks.use``,"允许使用弹跳方块"