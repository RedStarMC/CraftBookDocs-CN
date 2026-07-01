=================
发射器配方 Dispenser Recipes
=================

**发射器配方（Dispenser Recipes）** 机制为发射器内部添加了配方，在发射时执行特定任务。

配方 Recipes
=======

加农炮 Cannon
------

**加农炮（Cannon）** 配方会以相当大的力量从发射器中发射出一块点燃的 TNT。

.. image:: /images/dispenser/cannon_recipe.png
    :align: center

风扇 Fan
---

**风扇（Fan）** 配方会推开发射器前方 5 格范围内的所有实体。

.. image:: /images/dispenser/fan_recipe.png
    :align: center

吸尘器 Vacuum
------

**吸尘器（Vacuum）** 配方会吸入发射器前方 5 格范围内的所有实体。

.. image:: /images/dispenser/vacuum_recipe.png
    :align: center

火矢 Fire Arrows
-----------

**火矢（Fire Arrows）** 配方会从发射器中射出燃烧的箭矢。

.. image:: /images/dispenser/fire_arrow_recipe.png
    :align: center

雪球发射器 Snow Shooter
------------

**雪球发射器（Snow Shooter）** 配方会从发射器中射出雪球。

.. image:: /images/dispenser/snow_shooter_recipe.png
    :align: center

经验瓶发射器 XP Shooter
----------

**经验瓶发射器（XP Shooter）** 配方会从发射器中射出经验瓶。

.. image:: /images/dispenser/xp_shooter_recipe.png
    :align: center

配置 Configuration
=============

.. csv-table::
  :header: 节点, 说明, 默认值
  :widths: 15, 30, 10

  ``cannon-enable``,"启用加农炮发射器配方。","true"
  ``fan-enable``,"启用风扇发射器配方。","true"
  ``vacuum-enable``,"启用真空吸尘器发射器配方。","true"
  ``fire-arrows-enable``,"启用火矢发射器配方。","true"
  ``snow-shooter-enable``,"启用雪球发射器配方。","true"
  ``xp-shooter-enable``,"启用经验瓶发射器配方。","true"