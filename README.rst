elb checker
-----------

Example of a classical packaging capability for python.

* Use -e to install the project in dev mode::

    $ pip install -e .
    
or::

    $ python setup.py develop

* Using __main__.py allow you to call your app with::

    $ python -m elbchecker

* Using pbr allows

    - Set distribution version from git commits (latest tag).
    - No need to repeat requirements.txt in setup.py
    - No need to repeat project description which will be taken from readme.rst
    - Generate Changelog from git log automatically.
    - Generate AUTHOR from git automatically.
    - Simplify lookup for packages.

... etc, see https://docs.openstack.org/pbr/latest/

* Usage of conditional dependencies with <extra> with setuptools, see setup.cfg.
* Use EntryPoint named Console script to declare cli script.

How to release:
---------------

1. Tag your git repository as you see fit::

    $ git tag -a <x.y.z>

2. Generate source or binary distribution::

    $ python setup.py [ sdist | bdist | ... ]
