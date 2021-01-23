Development
===========

Setting up environment
----------------------

This assumes ``git`` and ``Python`` 3.5 or above are already installed on your system (see :doc:`INSTALL`).

1. Fork the `repository source code <https://github.com/MikeSmithEU/csvlike.git>`_ from github to your own account.

2. Clone the repository from github to your local development environment (replace ``[YOURUSERNAME]`` with your
   github username)::

      git clone https://github.com/[YOURUSERNAME]/csvlike.git
      cd csvlike

3. Create and activate a local environment::

      python3 -m pip install venv
      python3 -m venv
      source bin/activate

4. Install the package, this will also install all requirements. This does an "editable" install, i.e.
   it creates a symbolic link to the source code::

      make dev

5. You now have a local development environment where you can commit and push to your own forked repository. It is recommended to run the tests to check your local copy passes all unit tests::

      make test

.. warning::

   The development version of csvlike is only available in your current `venv` environment. Make sure to run ``source bin/activate`` to activate your local `venv` before using csvlike.


Building the documentation
--------------------------

First install the dependencies for building the documentation (sphinx, etc.) using::

      make setupdocs

This only needs to be done once.

Then to build the documentation locally::

      make docs

The documentation will be created in /docs/build/html/

