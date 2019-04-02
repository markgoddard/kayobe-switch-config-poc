=========================================
Kayobe Switch Config Mk2 Proof of Concept
=========================================

Try it out:

.. code-block:: console

   ansible-playbook -i inventory play.yml

Switch configuration is generated from Jinja templates ``switch-config.yml.j2``
and ``switch-config-interfaces.yml.j2``. The templates consume a model of the
switch connectivity in host_vars/<host>. In this example there are two hosts -
``sw0`` and ``sw1``. Because the hosts to which the switches are connected are
usually in the Kayobe inventory, we can use our knowledge about them to
determine how their ports should be setup.

One of the nice things about this approach is that it requires no changes to
Kayobe.
