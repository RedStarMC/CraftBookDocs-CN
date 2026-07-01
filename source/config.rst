=============
配置
=============

CraftBook 有多个配置文件，因此本页将重点介绍主配置文件，而不是每个单独机制的配置文件。
要配置机制，请参阅 :doc:`mechanics/index`。

配置文件
===================

在安装了 CraftBook 并运行服务器后，你会在 **plugins/CraftBook** 文件夹中找到主配置文件：

* ``config.yml``

设置
========

.. note::
     以下仅列出 ``config.yml`` 中的设置。更多设置请参见各机制专属页面 :doc:`这里 <mechanics/index>`

.. csv-table::
  :header: 节点, 说明, 默认值
  :widths: 15, 30, 10

  ``mechanics``,"启用的机制列表及其是否启用",""
  ``st-think-ticks``,"警告！更改此值可能导致所有 ST 机制表现异常，除非你清楚自己在做什么，否则不要修改！","2"
  ``safe-destruction``,"使许多机制需要足够的方块才能运作，例如闸门、桥梁和门。","true"
  ``no-op-permissions``,"如果开启，OP 默认不会拥有所有权限。","false"
  ``indirect-redstone``,"允许不直接朝向机械装置的红石触发该装置。","false"
  ``obey-worldguard-flags``,"在执行 CraftBook 操作时是否检查 WorldGuard 标志。","true"
  ``obey-plugin-protections``,"是否服从其他插件取消 CraftBook 操作的尝试。","true"
  ``sign-click-timeout``,"玩家与 CraftBook 告示牌交互的冷却时间（毫秒）。","500"
  ``debug-mode``,"启用调试模式，会在控制台输出额外的调试信息。","false"
  ``debug-mode-file-logging``,"将调试模式的所有输出记录到文件中。该文件在每次启动（以及每次 /cb reload）时重置。","false"
  ``debug-flags``,"调试模式启用时，开启特定类型的调试输出。","[]"
  ``show-permission-messages``,"当玩家没有权限执行某操作时，显示提示信息。","true"