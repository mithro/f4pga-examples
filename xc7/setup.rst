
Clone this repository
---------------------
If you have not already done so, clone this repository and `cd` into it:

.. code:: bash

   sudo apt install git
   git clone https://github.com/SymbiFlow/symbiflow-examples.git && cd symbiflow-examples



Setting up the toolchain
------------------------

Choose the installation directory (see the `README <../README.rst>`_ one level up for details):


.. code:: bash

    export INSTALL_DIR=~/opt/symbiflow   # or somewhere else you choose

.. toolchain_include_begin_label

.. code:: bash
        :name: xc7-setup-toolchain

        bash conda_installer.sh -b -p $INSTALL_DIR/xc7/conda
        source "$INSTALL_DIR/xc7/conda/etc/profile.d/conda.sh"
        conda env create -f xc7/environment.yml
        conda activate xc7
        wget -qO- https://storage.googleapis.com/symbiflow-arch-defs/artifacts/prod/foss-fpga-tools/symbiflow-arch-defs/continuous/install/66/20200914-111752/symbiflow-arch-defs-install-05d68df0.tar.xz | tar -xJ --one-top-level=$INSTALL_DIR/xc7/install
        conda deactivate

.. toolchain_include_end_label
