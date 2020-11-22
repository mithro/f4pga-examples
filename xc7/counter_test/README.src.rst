``counter`` - simple 4-bit counter driving LEDs
===============================================

The design targets the `Basys3 board <https://store.digilentinc.com/basys-3-artix-7-fpga-trainer-board-recommended-for-introductory-users/>`__ and the `Arty board <https://store.digilentinc.com/arty-a7-artix-7-fpga-development-board-for-makers-and-hobbyists/>`__.


.. include:: ../setup.rst

Building the examples
---------------------

.. build_examples_include_begin_label

To build the counter example, run any or all of the following commands:

.. code:: bash
        :name: xc7-counter

        pushd xc7/counter_test && make clean && TARGET="arty_50" make && popd
        pushd xc7/counter_test && make clean && TARGET="arty_100" make && popd
        pushd xc7/counter_test && make clean && TARGET="basys3" make && popd
