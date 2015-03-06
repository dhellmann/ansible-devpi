devpi
=====

Deploy a devpi server (https://pypi.python.org/pypi/devpi) for caching
downloads from the Python Package Index and configures pip to use it
and store wheels in a local wheelhouse.

Installs monit and configures it to keep devpi running.

Requirements
------------

The role uses virtualenv does not install it because different
developers may want to have it installed from different sources. In
*most* cases, it should be installed from source, but some people
still like to use the system package.

Role Variables
--------------

* devpi_virtualenv

  The full path to the virtualenv that should be created for
  installing devpi. Defaults to ~/.virtualenvs/devpi.

* devpi_port

  The port number on which the devpi server should listen. Defaults to
  3141. Always listens on localhost.

* devpi_wheelhouse

  The directory used for pip's wheelhouse cache. Defaults to
  ~/.pip/wheelhouse.

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - devpi

License
-------

BSD

Author Information
------------------

Doug Hellmann
