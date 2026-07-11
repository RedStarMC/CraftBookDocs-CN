==================
撞船伤害 Boat Impact Damage
==================

**撞船伤害（Boat Impact Damage）** 机制使船在碰撞时对其他实体造成伤害。碰撞时，实体会被推向船的方向并受到伤害。

.. note::

  由于 Minecraft 的限制，伤害和击退效果无法根据船的速度进行调整。

配置 Configuration
=============

.. csv-table::
  :header: 节点, 说明, 默认值
  :widths: 15, 30, 10

  ``remove-other-boats``,"允许船在碰撞时移除其他船只。","false"