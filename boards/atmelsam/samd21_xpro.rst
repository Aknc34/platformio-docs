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

.. _board_atmelsam_samd21_xpro:

Atmel SAMD21-XPRO
=================

.. contents::

Hardware
--------

Platform :ref:`platform_atmelsam`: Atmel | SMART offers Flash- based ARM products based on the ARM Cortex-M0+, Cortex-M3 and Cortex-M4 architectures, ranging from 8KB to 2MB of Flash including a rich peripheral and feature mix.

.. list-table::

  * - **Microcontroller**
    - SAMD21J18A
  * - **Frequency**
    - 48MHz
  * - **Flash**
    - 256KB
  * - **RAM**
    - 32KB
  * - **Vendor**
    - `Atmel <https://www.microchip.com/en-us/development-tool/atsamd21-xpro?utm_source=platformio.org&utm_medium=docs>`__


Configuration
-------------

Please use ``samd21_xpro`` ID for :ref:`projectconf_env_board` option in :ref:`projectconf`:

.. code-block:: ini

  [env:samd21_xpro]
  platform = atmelsam
  board = samd21_xpro

You can override default Atmel SAMD21-XPRO settings per build environment using
``board_***`` option, where ``***`` is a JSON object path from
board manifest `samd21_xpro.json <https://github.com/platformio/platform-atmelsam/blob/master/boards/samd21_xpro.json>`_. For example,
``board_build.mcu``, ``board_build.f_cpu``, etc.

.. code-block:: ini

  [env:samd21_xpro]
  platform = atmelsam
  board = samd21_xpro

  ; change microcontroller
  board_build.mcu = samd21j18a

  ; change MCU frequency
  board_build.f_cpu = 48000000L


Uploading
---------
Atmel SAMD21-XPRO supports the following uploading protocols:

* ``atmel-ice``
* ``blackmagic``
* ``cmsis-dap``
* ``jlink``

Default protocol is ``cmsis-dap``

You can change upload protocol using :ref:`projectconf_upload_protocol` option:

.. code-block:: ini

  [env:samd21_xpro]
  platform = atmelsam
  board = samd21_xpro

  upload_protocol = cmsis-dap

Debugging
---------

:ref:`piodebug` - "1-click" solution for debugging with a zero configuration.

.. warning::
    You will need to install debug tool drivers depending on your system.
    Please click on compatible debug tool below for the further
    instructions and configuration information.

You can switch between debugging :ref:`debugging_tools` using
:ref:`projectconf_debug_tool` option in :ref:`projectconf`.

Atmel SAMD21-XPRO has on-board debug probe and **IS READY** for debugging. You don't need to use/buy external debug probe.

.. list-table::
  :header-rows:  1

  * - Compatible Tools
    - On-board
    - Default
  * - :ref:`debugging_tool_atmel-ice`
    - 
    - 
  * - :ref:`debugging_tool_blackmagic`
    - 
    - 
  * - :ref:`debugging_tool_cmsis-dap`
    - Yes
    - Yes
  * - :ref:`debugging_tool_jlink`
    - 
    - 

Frameworks
----------
.. list-table::
    :header-rows:  1

    * - Name
      - Description

    * - :ref:`framework_zephyr`
      - The Zephyr Project is a scalable real-time operating system (RTOS) supporting multiple hardware architectures, optimized for resource constrained devices, and built with safety and security in mind