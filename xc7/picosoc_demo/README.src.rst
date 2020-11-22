``picosoc`` - `picorv32 <https://github.com/cliffordwolf/picorv32>`__ based SoC
===============================================================================

The design targets the `Basys3 board <https://store.digilentinc.com/basys-3-artix-7-fpga-trainer-board-recommended-for-introductory-users/>`__.

.. include:: ../setup.rst

Building the examples
---------------------

.. build_examples_include_begin_label

To build the picosoc example, run the following commands:

.. code:: bash
        :name: xc7-picosoc

        pushd xc7/picosoc_demo && make && popd

