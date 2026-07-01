========================
矿车物理控制 Minecart Physics Control
========================

**矿车物理控制（Minecart Physics Control）** 机制允许你控制矿车物理的各个精细方面。

空车减速 Empty Slowdown
==============

在 Minecraft 原版中，空矿车比载人矿车减速更快。这可以通过 ``slow-when-empty`` 配置选项禁用。

下落速度 Fall Speed
==========

``vertical-fall-speed`` 和 ``horizontal-fall-speed`` 选项允许配置下落矿车的垂直和水平速度。

这可以用于创建下落速度远快于前进速度的矿车，或下落更慢以获得更长滞空时间的矿车。一个常见的用途是创建矿车过山车。

使用 ``-1`` 作为速度值可以禁用此功能并恢复为 Minecraft 默认值。

.. note::

  垂直和水平速度都必须设置（不能为 ``-1``）此功能才能生效。

最大速度 Max Speed
=========

``max-speed`` 选项允许配置矿车可以达到的最大速度。

使用 ``-1`` 作为速度值可以禁用此功能并恢复为 Minecraft 默认值 0.4。

.. note::

  矿车在高速过弯时可能会变得不稳定。

脱轨速度 Off Rail Speed
==============

``off-rail-speed`` 选项允许调整矿车在非铁轨方块上行驶时的速度。

使用 ``-1`` 作为速度值可以禁用此功能并恢复为矿车默认值。

配置 Configuration
=============

.. csv-table::
  :header: 节点, 说明, 默认值
  :widths: 15, 30, 10

  ``slow-when-empty``,"矿车是否应在空载时减速更快","true"
  ``vertical-fall-speed``,"设置矿车的垂直下落速度","-1.0"
  ``horizontal-fall-speed``,"设置矿车的水平下落速度","-1.0"
  ``max-speed``,"设置矿车的最大速度修正值。Minecraft 正常速度为 0.4","-1.0"
  ``off-rail-speed``,"设置矿车的脱轨速度修正值","-1.0"