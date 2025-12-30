=============
Bounce Blocks
=============

The **Bounce Blocks** mechanic introduces special blocks that propel players when they either jump or walk on them.

Construction
============

Bounce Blocks consist of two parts. A block from configured list of allowed bounce blocks, and a sign placed directly below it.

The second line of the sign must match one of the below sign types to determine how the bounce block will activate, with the third line optionally configuring the bounce velocity.

Sign Types
----------

* ``[Jump]`` - A bounce block sign that activates when a player jumps on the block above it.
* ``[Launch]`` - A bounce block sign that activates when a player walks onto the block above it.

Bounce Velocity
---------------

By default, bounce blocks will propel players with a vertical velocity of 0.5, however this can be altered by specifying a different value on the third line of the sign.

For example, to specify a vertical velocity of 1.0, the third line would simply state ``1.0``.

Upwards velocities aren't the only option however. You can also specify both "forward" and "sideways" velocities by providing multiple values separated by commas.

For example, to propel a player forwards with a velocity of 0.5 and upwards with a velocity of 1, the third line would state ``0.5,1,0``.

While this looks like an X,Y,Z coordinate, it's actually relative to the player itself. So X refers to forwards, Y refers to upwards, and Z refers to sideways. This means that no matter what direction the player comes from, they will still be propelled forwards.

Absolute Velocities
~~~~~~~~~~~~~~~~~~~

If you would like a bounce block to always propel in a certain direction, such as for a parkour course or some other system with one single destination, you can add a ``!`` to the start of the third line. This swaps the bounce blocks to use actual game coordinates, rather than relative to the player's movement direction.

For example, to launch the player with a velocity of 1.0 both upwards and towards the negative Z direction, the third line would state ``!0,1,-1``.

Configuration
=============

.. csv-table::
  :header: Node, Comment, Default
  :widths: 15, 30, 10

  ``blocks``,"A list of blocks that can be used as bounce blocks.","[minecraft:black_terracotta, minecraft:blue_terracotta, minecraft:brown_terracotta, minecraft:cyan_terracotta, minecraft:gray_terracotta, minecraft:green_terracotta, minecraft:light_blue_terracotta, minecraft:light_gray_terracotta, minecraft:lime_terracotta, minecraft:magenta_terracotta, minecraft:orange_terracotta, minecraft:pink_terracotta, minecraft:purple_terracotta, minecraft:red_terracotta, minecraft:terracotta, minecraft:white_terracotta, minecraft:yellow_terracotta]"
  ``sensitivity``,"The sensitivity of movement required to activate the block.","0.1"

Permissions
===========

.. csv-table::
  :header: Permission Node, Effect
  :widths: 20, 30

  ``craftbook.bounceblocks.create``,"Allows the creation of Bounce Blocks signs"
  ``craftbook.bounceblocks.use``,"Allows for the usage of Bounce Blocks"
