==========
更多铁轨 More Rails
==========

**更多铁轨（More Rails）** 机制通过使用其他方块来增加新的铁轨类型。

4岔铁道 4-Way Intersections
===================

4岔铁道功能允许使用压力板创建矿车岔道。当矿车驶过压力板时，会获得持续的加速效果，使其不会停下来。

垂直铁轨 Vertical Rails
==============

垂直铁轨功能允许使用梯子或藤蔓创建垂直向上的矿车轨道。当矿车撞上这些方块时，会向上行驶。

配置 Configuration
=============

.. csv-table::
  :header: 节点, 说明, 默认值
  :widths: 15, 30, 10

  ``pressure-plate-intersection``,"允许使用压力板作为铁轨交叉口。","true"
  ``ladder-vertical-rail``,"允许使用梯子和藤蔓作为垂直铁轨。","true"
  ``ladder-vertical-rail-velocity``,"设置垂直铁轨上矿车的速度。","0.1"