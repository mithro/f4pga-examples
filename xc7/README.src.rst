SymbiFlow Toolchain Examples for Xilinx 7 Series
================================================

#. ``counter`` - simple 4-bit counter driving LEDs. The design targets the `Basys3 board <https://store.digilentinc.com/basys-3-artix-7-fpga-trainer-board-recommended-for-introductory-users/>`__ and the `Arty board <https://store.digilentinc.com/arty-a7-artix-7-fpga-development-board-for-makers-and-hobbyists/>`__.

#. ``picosoc`` - `picorv32 <https://github.com/cliffordwolf/picorv32>`__ based SoC. The design targets the `Basys3 board <https://store.digilentinc.com/basys-3-artix-7-fpga-trainer-board-recommended-for-introductory-users/>`__.

#. ``linux_litex`` - `LiteX <https://github.com/enjoy-digital/litex>`__ based system with Linux capable `VexRiscv core <https://github.com/SpinalHDL/VexRiscv>`__. The design includes `DDR <https://github.com/enjoy-digital/litedram>`__ and `Ethernet <https://github.com/enjoy-digital/liteeth>`__ controllers. The design targets the `Arty board <https://store.digilentinc.com/arty-a7-artix-7-fpga-development-board-for-makers-and-hobbyists/>`__.

The Linux images for the ``linux_litex`` example can be built following the `linux on litex vexriscv <https://github.com/litex-hub/linux-on-litex-vexriscv>`__ instructions.
The ``linux_litex`` example is already provided with working Linux images.


.. include:: setup.rst

.. include:: counter/README.rst
   :start-after:.. build_examples_include_begin_label

.. include:: picosoc/README.rst
   :start-after:.. build_examples_include_begin_label

.. include:: linux_litex/README.rst
   :start-after:.. build_examples_include_begin_label
