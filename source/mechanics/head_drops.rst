==========
头颅掉落 Head Drops
==========

**头颅掉落（Head Drops）** 机制允许玩家或生物在被击杀时，以可配置的概率掉落其头颅。

视频指南：https://www.youtube.com/watch?v=Lv74hI7mVGA

使用方法
=====

使用时，只需击杀一个受支持的生物或玩家即可。掉落概率可配置，抢夺（Looting）附魔的影响也可配置。

默认情况下，玩家和生物都会掉落头颅，但这也是可配置的。

为了限制头颅刷取，可以在配置中要求必须由玩家击杀该实体。

高级配置
======================

按实体类型单独设置掉率
--------------------------

如果你想精细控制每种生物的掉率，可以使用 drop-rates 部分。对于此处列出的任何实体，将使用该值替代全局掉率。抢夺附魔仍然照常生效。

.. code-block:: yaml

    drop-rates:
      pig: 0.5
      cow: 0.1

自定义生物头颅 / 额外生物头颅
--------------------------------

在配置中可以覆盖或添加皮肤。这对于运行模组服务器并希望为模组生物添加支持，或使用资源包并希望覆盖皮肤以更好适配的情况非常有用。

此选项需要来自 Mojang 的签名皮肤纹理 blob——这是在 Profile 查询端点的 "value" 部分之后的那段奇怪文本。

要获取某玩家的此值，请找到其 UUID 并移除 '-' 字符。然后访问 URL
"https://sessionserver.mojang.com/session/minecraft/profile/UUID"，将 UUID 替换为实际 UUID。在那里你可以看到其皮肤数据。

例如，档案 "MHF_Enderman" 的 URL 为 https://sessionserver.mojang.com/session/minecraft/profile/40ffb37212f64678b3f22176bf56dd4b。

以此为例，custom-skins 部分应填写如下：

.. code-block:: yaml

    custom-skins:
      enderman: "ewogICJ0aW1lc3RhbXAiIDogMTYwNDU3ODQyNjM0NywKICAicHJvZmlsZUlkIiA6ICI0MGZmYjM3MjEyZjY0Njc4YjNmMjIxNzZiZjU2ZGQ0YiIsCiAgInByb2ZpbGVOYW1lIiA6ICJNSEZfRW5kZXJtYW4iLAogICJ0ZXh0dXJlcyIgOiB7CiAgICAiU0tJTiIgOiB7CiAgICAgICJ1cmwiIDogImh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvMWIwOWEzNzUyNTEwZTkxNGIwYmRjOTA5NmIzOTJiYjM1OWY3YThlOGE5NTY2YTAyZTdmNjZmYWZmOGQ2Zjg5ZSIKICAgIH0KICB9Cn0="

配置
=============

.. csv-table::
  :header: 节点, 说明, 默认值
  :widths: 15, 30, 10

  ``drop-mob-heads``,"是否让生物在被击杀时掉落头颅。","true"
  ``drop-player-heads``,"是否让玩家在被击杀时掉落头颅。","true"
  ``require-player-killer``,"仅当被玩家击杀时才掉落头颅。（可配合权限使用）","true"
  ``override-natural-head-drops``,"覆盖原版头颅掉落，使原版头颅掉落使用 CraftBook 提供的概率（例如，凋灵骷髅头颅）。","false"
  ``drop-rate``,"0~1 之间的值，表示全局掉率。可按实体类型覆盖。","0.05"
  ``looting-rate-modifier``,"每级抢夺附魔增加的概率。例如，基础概率 0.05（5%），抢夺修正 0.05（5%），抢夺 III 时总概率为 0.20（20%）。","0.05"
  ``show-name-right-click``,"启用后，右键点击已放置的头颅会显示其所有者名称。","true"
  ``drop-rates``,"不同生物的自定义掉率列表",""
  ``custom-skins``,"不同生物的自定义皮肤列表",""


权限 Permissions
===========

+-----------------------------+--------------------------------------------------------------------+
|  权限节点 Permission Node   |  效果 Effect                                                       |
+=============================+====================================================================+
|  craftbook.headdrops.drops  |  允许玩家获得头颅掉落物。                                          |
+-----------------------------+--------------------------------------------------------------------+

命令 Commands
========
.. contents::
    :local:

.. note::

    用 ``[ ]`` 括起来的参数为可选，用 ``< >`` 括起来的为必需。

HeadDrops
~~~~~~~~~
.. raw:: html

    <span id="command-/headdrops"></span>

.. topic:: ``/headdrops``
    :class: command-topic

.. csv-table::
  :widths: 8, 15

        **用法 Usage**,"``/headdrops <give>``"
        **描述 Description**,"CraftBook 头颅掉落命令"

.. raw:: html

    <span id="command-/headdrops-give"></span>

.. topic:: ``/headdrops give``
    :class: command-topic

.. csv-table::
  :widths: 8, 15

        **用法 Usage**,"``/headdrops give [-s] <piston.argument.Entity Type> [-p <piston.argument.otherPlayer>] [-a <piston.argument.amount>]``"
          ``[-a <piston.argument.amount>]``,"给予数量"
        **描述 Description**,"给予玩家头颅掉落物品。"
        **权限 Permissions**,"``craftbook.headdrops.give``"
          ``<piston.argument.Entity Type>``,"要生成头颅的实体类型"
          ``[-p <piston.argument.otherPlayer>]``,"目标玩家"
          ``[-s]``,"静默输出"