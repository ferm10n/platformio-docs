..  Copyright (c) 2014-present PlatformIO <contact@platformio.org>
    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at
       http://www.apache.org/licenses/LICENSE-2.0
    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

.. _board_nxplpc_oc_mbuino:

mBuino
======

.. contents::

Hardware
--------

Platform :ref:`platform_nxplpc`: The NXP LPC is a family of 32-bit microcontroller integrated circuits by NXP Semiconductors. The LPC chips are grouped into related series that are based around the same 32-bit ARM processor core, such as the Cortex-M4F, Cortex-M3, Cortex-M0+, or Cortex-M0. Internally, each microcontroller consists of the processor core, static RAM memory, flash memory, debugging interface, and various peripherals.

.. list-table::

  * - **Microcontroller**
    - LPC11U24
  * - **Frequency**
    - 50MHz
  * - **Flash**
    - 32KB
  * - **RAM**
    - 10KB
  * - **Vendor**
    - `GHI Electronics <https://developer.mbed.org/platforms/mBuino/?utm_source=platformio.org&utm_medium=docs>`__


Configuration
-------------

Please use ``oc_mbuino`` ID for :ref:`projectconf_env_board` option in :ref:`projectconf`:

.. code-block:: ini

  [env:oc_mbuino]
  platform = nxplpc
  board = oc_mbuino

You can override default mBuino settings per build environment using
``board_***`` option, where ``***`` is a JSON object path from
board manifest `oc_mbuino.json <https://github.com/platformio/platform-nxplpc/blob/master/boards/oc_mbuino.json>`_. For example,
``board_build.mcu``, ``board_build.f_cpu``, etc.

.. code-block:: ini

  [env:oc_mbuino]
  platform = nxplpc
  board = oc_mbuino

  ; change microcontroller
  board_build.mcu = lpc11u24

  ; change MCU frequency
  board_build.f_cpu = 50000000L

Debugging
---------
:ref:`piodebug` currently does not support mBuino board.

Frameworks
----------
.. list-table::
    :header-rows:  1

    * - Name
      - Description

    * - :ref:`framework_mbed`
      - Arm Mbed OS is a platform operating system designed for the internet of things