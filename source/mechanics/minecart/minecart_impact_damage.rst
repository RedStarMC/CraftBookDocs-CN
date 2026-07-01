======================
矿车撞击伤害 Minecart Impact Damage
======================

**矿车撞击伤害（Minecart Impact Damage）** 机制使矿车在碰撞时对其他实体造成伤害。碰撞时，实体会被推向矿车方向并受到伤害。

配置 Configuration
=============

.. csv-table::
  :header: 节点, 说明, 默认值
  :widths: 15, 30, 10

  ``remove-other-minecarts``,"允许矿车在撞击时移除其他矿车。","false"
  ``allow-empty-carts``,"允许空矿车造成撞击伤害。","false"
  ``damage-players``,"允许矿车对玩家造成伤害并致死。","true"