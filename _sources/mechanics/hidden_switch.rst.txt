=============
隐藏开关 Hidden Switch
=============

**隐藏开关（Hidden Switch）** 机制允许创建隐蔽的开关，使用隐藏在墙壁后面的拉杆或按钮。右键点击墙壁时，隐藏的拉杆或按钮会被切换。

建造方法
============

隐藏开关由三部分组成：

- 一个供玩家右键点击以切换开关的方块
- 切换方块上的墙壁告示牌，第二行为 ``[X]``
- 告示牌下方的拉杆或按钮

.. image:: /images/hidden_switch/hidden_switch.png
    :align: center
    :height: 300px

任意面 Any Face
--------

如果启用了 ``allow-any-face`` 选项，切换方块的任何面都可以通过右键点击来触发开关。如果禁用，则只有告示牌所在面的相对面可以触发。

访问限制 Access Restrictions
-------------------

权限组 Permission Groups
~~~~~~~~~~~~~~~~~

如果在告示牌的第三行写入了权限组名称，只有该组的成员才能使用此开关。

配置 Configuration
=============

.. csv-table::
  :header: 节点, 说明, 默认值
  :widths: 15, 30, 10

  ``allow-any-face``,"允许从方块的任何面激活隐藏开关。","true"

权限 Permissions
===========

.. csv-table::
  :header: 权限节点 Permission Node, 效果 Effect
  :widths: 20, 30

  ``craftbook.hiddenswitch.create``,"允许创建隐藏开关告示牌"
  ``craftbook.hiddenswitch.use``,"允许使用隐藏开关机制"