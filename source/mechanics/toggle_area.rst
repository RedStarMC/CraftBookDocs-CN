===========
切换区域 Toggle Area
===========

**切换区域（Toggle Area）** 机制允许你创建任意大小的区域，并通过右键点击告示牌、使用红石或使用命令来切换其召唤/收回状态。

建造方法
============

世界中的切换区域以一个告示牌为参照，引用一个或两个已通过命令保存的区域。

基础切换区域告示牌可按以下行设置：

1. 命名空间（空白则使用个人命名空间）
2. ``[ToggleArea]``
3. 区域名称
4. 关闭时显示的另一区域名称（留空则替换为空气）

译注：命名空间见"https://craftbook.enginehub.org/en/5.0.0/mechanics/variables/"

保存的区域与其保存时的位置固有绑定。无论切换区域告示牌创建在何处，它都将在保存时的位置进行切换。
译注：就像worldedit的//copy和//paste一样

如果配置允许，红石可用于通过告示牌切换区域开关。否则，可以右键点击告示牌进行切换。

自动保存区域 Auto-saving areas
-----------------

如果你希望切换区域在每次切换时保留对其所做的修改，可以改用 ``[ToggleAreaSave]`` 告示牌。其行为与普通切换区域告示牌相同，但每次切换时会重新保存该区域。

切换命令 Toggle command
--------------

对于复杂情况，CraftBook 提供了 ``/area toggle`` 命令。该命令允许提供游戏内坐标（从控制台运行时可选提供世界）来切换切换区域告示牌。

例如，以下命令将切换位于名为 ``world`` 的世界中坐标 X:0, Y:0, Z:0 处的告示牌：

``/area toggle -w world 0,0,0``

命名空间 Namespaces
==========

切换区域在保存和引用区域时使用命名空间概念。默认情况下，所有命令和告示牌都使用玩家自己的个人命名空间。

个人命名空间 Personal namespaces
-------------------

个人命名空间是特殊的，因为它们只能由拥有该空间的玩家使用。它们内部以玩家的 UUID 保存，当未指定命名空间时，所有命令和告示牌会自动使用。

在告示牌上，它们会以斜体显示为 ``~[名称]``，以表示这是个人命名空间而非自定义命名空间。

个人命名空间是服务器管理员用例之外推荐使用的方式，因为它们也遵守 ``max-per-user`` 配置选项。同时，它也是一种简单的方法，可以防止玩家编辑其他人的切换区域。

自定义命名空间 Custom namespaces
-----------------

如果你希望多人共享同一个命名空间，可以使用自定义命名空间。在命令中通过提供 ``-n`` 标志使用，在告示牌上则在第一行输入。

例如，保存到自定义命名空间可使用以下命令：

``/area save -n some_text area_name``

这会将名为 ``area_name`` 的切换区域保存到命名空间 ``some_text`` 中。然后在告示牌上，第一行输入 ``some_text``，第三行输入 ``area_name`` 即可使用。

区域管理 Area Management
===============

保存 Saving
------

区域使用 WorldEdit 选区（selection）和 ``/area save [名称]`` 命令创建。

一旦你创建了选区，只需运行该命令即可将其保存到玩家的命名空间。你可以使用 ``-n`` 标志指定自定义命名空间。

列表 Listing
-------

使用 ``/area list`` 命令可以获取当前已保存区域的列表。

默认使用个人命名空间，但你可以使用 ``-n`` 标志指定自定义命名空间。你也可以使用 ``-a`` 标志跨所有命名空间搜索。

删除 Deleting
--------

要删除区域，可使用 ``/area delete`` 命令；要删除命名空间内的所有区域，可使用 ``/area delete-all`` 命令。

默认使用个人命名空间，但你可以使用 ``-n`` 标志指定自定义命名空间。

配置 Configuration
=============

.. csv-table::
  :header: 节点, 说明, 默认值
  :widths: 15, 30, 10

  ``allow-redstone``,"允许切换区域通过红石切换。","true"
  ``max-size``,"设置切换区域可包含的最大方块数量。","5000"
  ``max-per-user``,"设置单个个人命名空间中最多可保存的切换区域数量。","30"

权限 Permissions
===========

.. csv-table::
  :header: 权限节点 Permission Node, 效果 Effect
  :widths: 20, 30

  ``craftbook.togglearea.create``,"允许创建切换区域告示牌"
  ``craftbook.togglearea.create.save``,"允许创建切换区域自动保存告示牌"
  ``craftbook.togglearea.use``,"允许使用切换区域告示牌"
  ``craftbook.togglearea.save``,"允许使用 ``/area save`` 命令"
  ``craftbook.togglearea.save.[namespace]``,"允许在指定命名空间中保存"
  ``craftbook.togglearea.save.self``,"允许在玩家自己的命名空间中保存"
  ``craftbook.togglearea.bypass-area-limit``,"允许绕过最大区域数量限制"
  ``craftbook.togglearea.list``,"允许使用 ``/area list`` 命令"
  ``craftbook.togglearea.list.[namespace]``,"允许列出指定命名空间中的区域"
  ``craftbook.togglearea.list.all``,"允许跨所有命名空间列出区域"
  ``craftbook.togglearea.list.self``,"允许列出玩家自己的命名空间中的区域"
  ``craftbook.togglearea.toggle-command``,"允许使用 ``/area toggle`` 命令"
  ``craftbook.togglearea.delete``,"允许使用 ``/area delete`` 命令"
  ``craftbook.togglearea.delete.[namespace]``,"允许删除指定命名空间中的区域"
  ``craftbook.togglearea.delete.self``,"允许删除玩家自己命名空间中的区域"
  ``craftbook.togglearea.delete.[namespace].all``,"允许删除指定命名空间中的所有区域"
  ``craftbook.togglearea.delete.self.all``,"允许删除玩家自己命名空间中的所有区域"


命令 Commands
========

.. contents::
    :local:

.. note::

    用 ``[ ]`` 括起来的参数为可选，用 ``< >`` 括起来的为必需。

ToggleArea
~~~~~~~~~~
.. raw:: html

    <span id="command-/area"></span>

.. topic:: ``/area``（或 ``/togglearea``）
    :class: command-topic

.. csv-table::
  :widths: 8, 15

        **用法 Usage**,"``/area <delete-all|save|toggle|list|delete>``"
        **描述 Description**,"CraftBook 切换区域命令"

.. raw:: html

    <span id="command-/area-delete-all"></span>

.. topic:: ``/area delete-all``
    :class: command-topic

.. csv-table::
  :widths: 8, 15

        **用法 Usage**,"``/area delete-all <piston.argument.namespace...>``"
          ``<piston.argument.namespace...>``,"命名空间"
        **描述 Description**,"删除命名空间中的所有区域。"
        **权限 Permissions**,"``craftbook.togglearea.delete``"

.. raw:: html

    <span id="command-/area-save"></span>

.. topic:: ``/area save``
    :class: command-topic

.. csv-table::
  :widths: 8, 15

        **用法 Usage**,"``/area save [-be] [-n <piston.argument.namespace>] <piston.argument.name>``"
          ``[-e]``,"保存实体"
          ``[-n <piston.argument.namespace>]``,"命名空间"
          ``<piston.argument.name>``,"区域名称"
          ``[-b]``,"保存生物群系"
        **描述 Description**,"保存选中的区域"
        **权限 Permissions**,"``craftbook.togglearea.save``"

.. raw:: html

    <span id="command-/area-toggle"></span>

.. topic:: ``/area toggle``
    :class: command-topic

.. csv-table::
  :widths: 8, 15

        **用法 Usage**,"``/area toggle [-s] [-w <piston.argument.world>] <piston.argument.position>``"
          ``[-w <piston.argument.world>]``,"世界"
          ``<piston.argument.position>``,"坐标位置"
        **描述 Description**,"切换指定位置处的区域告示牌。"
        **权限 Permissions**,"``craftbook.togglearea.toggle-command``"
          ``[-s]``,"静默输出"

.. raw:: html

    <span id="command-/area-list"></span>

.. topic:: ``/area list``
    :class: command-topic

.. csv-table::
  :widths: 8, 15

        **用法 Usage**,"``/area list [-a] [-n <piston.argument.namespace>] [-p <piston.argument.page>]``"
          ``[-n <piston.argument.namespace>]``,"命名空间"
          ``[-p <piston.argument.page>]``,"页码"
          ``[-a]``,"列出所有命名空间中的区域"
        **描述 Description**,"列出指定命名空间中的区域，或列出所有区域。"
        **权限 Permissions**,"``craftbook.togglearea.list``"

.. raw:: html

    <span id="command-/area-delete"></span>

.. topic:: ``/area delete``
    :class: command-topic

.. csv-table::
  :widths: 8, 15

        **用法 Usage**,"``/area delete [-n <piston.argument.namespace>] <piston.argument.name>``"
          ``[-n <piston.argument.namespace>]``,"命名空间"
          ``<piston.argument.name>``,"区域名称"
        **描述 Description**,"删除指定命名空间中的区域。"
        **权限 Permissions**,"``craftbook.togglearea.delete``"