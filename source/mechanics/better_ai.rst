=========
更好的 AI Better AI
=========

**更好的 AI（Better AI）** 机制为增强实体 AI 提供了众多选项。

增强视野 Enhanced Vision
===============

**增强视野（Enhanced Vision）** 功能改变了生物看到玩家的条件。当为某实体启用时，以下额外目标规则生效：

* 只有在冲刺时才能透过墙壁看到你
* 在低光照条件下潜行会减少视野范围

暴击弓 Critical Bow
=============

**暴击弓（Critical Bow）** 功能使生物有一定几率用弓造成暴击伤害。暴击伤害表现为点燃目标。

攻击被动生物 Attack Passive
===============

**攻击被动生物（Attack Passive）** 功能允许生物攻击被动实体，如猪或羊。

逃离武器 Flee from Weapons
=================

**逃离武器（Flee from Weapons）** 功能使动物在玩家手持剑靠近时逃离。

体型差异 Size Variance
=============

**体型差异（Size Variance）** 功能使动物在生成时体型有微小的差异，变异性可配置。这为动物生成增加了一些自然变化，使它们在体型上看起来略有不同，而不是完全一样。

繁殖变异性 Breeding Variability
--------------------

如果在配置中启用，动物可以选择根据父母的体型继承体型。它们的基础体型将是父母双方体型的平均值，并在其上添加可配置的变异性以考虑突变。这允许选择性繁殖特定体型的动物，从而随着时间的推移培育出非常小或非常大的动物。

配置 Configuration
=============

.. csv-table::
  :header: 节点, 说明, 默认值
  :widths: 15, 30, 10

  ``enhanced-vision-enabled``,"启用增强视野 AI 机制的实体列表。","[minecraft:zombie, minecraft:drowned, minecraft:husk, minecraft:zombified_piglin]"
  ``critical-bow-enabled``,"启用暴击弓 AI 机制的实体列表。","[minecraft:skeleton]"
  ``attack-passive-enabled``,"启用攻击被动生物 AI 机制的实体列表。","[minecraft:zombie, minecraft:drowned, minecraft:husk]"
  ``attack-passive-ignore-hostile-mounts``,"敌对生物是否忽略被敌对实体骑乘的被动实体。","true"
  ``flee-from-weapons``,"启用逃离武器 AI 机制的实体列表。","[minecraft:chicken, minecraft:pig, minecraft:cow, minecraft:mooshroom, minecraft:sheep]"
  ``size-variance``,"启用体型差异 AI 机制的实体列表。","[minecraft:chicken, minecraft:pig, minecraft:cow, minecraft:mooshroom, minecraft:sheep]"
  ``size-variance-allow-breeding``,"体型差异是否也适用于实体繁殖时。","true"
  ``size-variance-variability``,"应用于实体的默认体型变异范围。","0.2"
  ``size-variance-breeding-variability``,"繁殖时应用于后代体型的变异范围。","0.1"