====================
空矿车消失 Minecart Empty Decay
====================

**空矿车消失（Minecart Empty Decay）** 机制会使矿车在无人乘坐达到可配置的时间后消失。

.. note::

  此机制**不会**掉落矿车物品。如果你希望矿车在下车时自动分解，请改用 :doc:`矿车下船移除 minecart_exit_remover` 机制。

配置 Configuration
=============

.. csv-table::
  :header: 节点, 说明, 默认值
  :widths: 15, 30, 10

  ``decay-delay``,"矿车在消失前等待的时间（刻）。","200"