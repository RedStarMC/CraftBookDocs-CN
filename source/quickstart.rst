===========
快速开始
===========

启用机制
==================

CraftBook 的所有功能默认都是禁用的。这是为了让服主能够根据自身需求定制 CraftBook 的功能。

CraftBook 的功能被划分成多个模块，称为**机制（Mechanics）**。

你可以在 ``config.yml`` 文件中（参见 :doc:`config`）或通过游戏内命令启用或禁用机制。

首先，你应该决定实际想要启用哪些机制。请查看 :doc:`mechanics/index` 了解每种机制的信息。

通过配置文件
---------------------

* 用你喜欢的文本编辑器打开 ``plugins/CraftBook/config.yml`` 文件。
* 在配置的 ``mechanics`` 部分，将你想要启用的项目设置为 ``true``。
* 重启服务器或运行 ``/cb reload``。**（不要**使用 ``/reload`` 命令。`点击此处了解原因。 <https://madelinemiller.dev/blog/problem-with-reload/>`_）

通过命令
-------------

* 运行 ``/cb mech list`` 查看可用机制列表。
* 点击 ``[Enable]`` 或 ``[Disable]`` 按钮来启用或禁用机制。
* 你也可以直接使用 ``/cb mech enable 机制名称`` 或 ``/cb mech disable 机制名称`` 来启用或禁用机制。

.. note::

  由于 Spigot/Paper 平台的限制，在服务器运行时启用带有命令的机制后，命令补全功能需要重启服务器才能正常显示。

配置机制
==================

许多机制可以进一步配置。有关具体配置选项的更多信息，请查看该机制的专属页面，详见 :doc:`这里 <mechanics/index>`。

要配置这些机制，请找到 ``CraftBook/mechanics`` 文件夹。在该文件夹中，你会找到每个机制的配置文件。

使用机制
==================

由于每种机制的使用方式不同，最佳参考是该机制的专属页面，详见 :doc:`这里 <mechanics/index>`。