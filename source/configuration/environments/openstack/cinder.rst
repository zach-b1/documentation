======
Cinder
======

iSCSI support
=============

.. code-block:: yaml
   :caption: environments/kolla/configuration.yml

   enable_cinder_backend_iscsi: yes
   enable_cinder_backend_lvm: no

.. code-block:: ini
   :caption: inventory/hosts

   [iscsid:children]
   compute
   storage
   ironic-conductor

   [multipathd:children]
   compute
   storage

   [tgtd:children]
   storage
