==================
可读书架 Readable Bookshelf
==================

**可读书架（Readable Bookshelf）** 机制使书架在右键点击时可“阅读”。
每次右键点击，从 books 文件中读取的文本行会打印到玩家的聊天栏中，就像他们从书架上的书中读到的一样。

.. image:: /images/readable_bookshelf/reading.png
    :align: center

自定义文本行 Customizing the lines
=====================

CraftBook 下载附带的 books.txt 文件中提供了一组默认的语录。该文件位于 CraftBook 文件夹中。

你可以添加新行、删除行，或完全替换整个文件。每行文本代表一本“书”。你可以根据需要设置任意数量的行。

可能用途 Possible Uses
-------------

可读书架机制的一个常见用途是在服务器中注入“背景故事”。例如，讲述游戏内过去的事件或历史。

配置 Configuration
=============

.. csv-table::
  :header: 节点, 说明, 默认值
  :widths: 15, 30, 10

  ``allow-sneaking``,"允许在潜行时阅读。","false"
  ``allow-holding-block``,"允许玩家手持方块时使用书架。","false"


权限 Permissions
===========

+----------------------------------+--------------------------------------+
|  权限节点 Permission Node        |  效果 Effect                         |
+==================================+======================================+
|  craftbook.readablebookshelf.use |  允许使用可读书架。                   |
+----------------------------------+--------------------------------------+