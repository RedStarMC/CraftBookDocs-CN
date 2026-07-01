================
空船消失 Boat Empty Decay
================

**空船消失（Boat Empty Decay）** 机制会使船在无人乘坐达到可配置的时间后消失。

.. note::

  此机制**不会**掉落船物品。如果你希望船在下船时自动分解，请改用 :doc:`船下船移除 boat_exit_remover` 机制。

配置 Configuration
=============

.. csv-table::
  :header: 节点, 说明, 默认值
  :widths: 15, 30, 10

  ``decay-delay``,"船在消失前等待的时间（刻）。","200"