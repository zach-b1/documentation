======
Common
======

.. list-table::
   :widths: 10 90
   :align: left

   * - **Name**
     - ``osism.common``
   * - **Repository**
     - https://github.com/osism/ansible-common
   * - **Documentation**
     - ---

Microcode installation
======================

The parameter ``install_microcode_package_common`` can be used to install
the packages ``intel-microcode`` and ``amd64-microcode``.

.. code-block:: yaml
   :caption: environments/configuration.yml

   ##########################
   # common

   install_microcode_package_common: yes

Hardware clock synchronisation
==============================

If a node cannot access the hardware clock, it is possible to deactivate hardware clock synchronisation.

.. code-block:: yaml
   :caption: environments/manager/host_vars/<hostname>.yml

   ##########################
   # common

   systohc_common: false
