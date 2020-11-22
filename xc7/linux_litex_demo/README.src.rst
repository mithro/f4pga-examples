``linux_litex`` - `LiteX <https://github.com/enjoy-digital/litex>`__ based system with Linux capable `VexRiscv core <https://github.com/SpinalHDL/VexRiscv>`__
==============================================================================================================================================================

The design includes `DDR <https://github.com/enjoy-digital/litedram>`__ and `Ethernet <https://github.com/enjoy-digital/liteeth>`__ controllers. The design targets the `Arty board <https://store.digilentinc.com/arty-a7-artix-7-fpga-development-board-for-makers-and-hobbyists/>`__.

The Linux images for the ``linux_litex`` example can be built following the `linux on litex vexriscv <https://github.com/litex-hub/linux-on-litex-vexriscv>`__ instructions.
The ``linux_litex`` example is already provided with working Linux images.


.. include:: ../setup.rst

Building the examples
---------------------

.. build_examples_include_begin_label

Before building any example, set the installation directory to match what you set it to earlier,

To build the litex example, run the following commands:

.. code:: bash
        :name: xc7-litex

        wget https://raw.githubusercontent.com/enjoy-digital/litex/master/litex_setup.py
        chmod +x litex_setup.py
        ./litex_setup.py init
        ./litex_setup.py install
        wget https://static.dev.sifive.com/dev-tools/riscv64-unknown-elf-gcc-8.1.0-2019.01.0-x86_64-linux-ubuntu14.tar.gz
        tar -xf riscv64-unknown-elf-gcc-8.1.0-2019.01.0-x86_64-linux-ubuntu14.tar.gz
        export PATH=$PATH:$PWD/riscv64-unknown-elf-gcc-8.1.0-2019.01.0-x86_64-linux-ubuntu14/bin/
        pushd litex/litex/boards/targets && ./arty.py --toolchain symbiflow --cpu-type vexriscv --build && popd

To build the linux-litex-demo example, run the following commands:

.. code:: bash
        :name: xc7-linux

        pushd xc7/linux_litex_demo && make && popd
        pushd xc7/linux_litex_demo && TARGET="arty_100" make && popd

.. build_examples_include_end_label
