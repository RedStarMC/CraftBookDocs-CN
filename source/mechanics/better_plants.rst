=============
更好的植物 Better Plants
=============

**更好的植物（Better Plants）** 机制是一系列旨在增强游戏中植物交互方式的功能。目的是创造一个更自然、更具互动性的环境。

蕨类种植 Fern Farming
============

蕨类种植允许玩家种植蕨类植物。小型蕨类经过一段时间后会长成大型蕨类，然后大型蕨类的顶部方块可以被破坏以掉落另一个小型蕨类。一旦大型蕨类被破坏，其位置会重新放置一个小型蕨类。

.. image:: /images/better_plants/fern_farming.png
    :align: center

配置 Configuration
=============

.. csv-table::
  :header: 节点, 说明, 默认值
  :widths: 15, 30, 10

  ``fern-farming``,"允许通过破坏大型蕨类上半部分来种植蕨类（同时小型蕨类也能生长）。","true"
  ``fast-random-ticks``,"使用一种减少随机数生成的方式，仅对每个区块生成一次随机数，而不是每个区块内分别生成。","true"