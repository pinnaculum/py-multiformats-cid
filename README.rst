
CID (Content IDentifier)
------------------------


.. image:: https://img.shields.io/pypi/v/py-multiformats-cid.svg
        :target: https://pypi.python.org/pypi/py-multiformats-cid

.. image:: https://img.shields.io/travis/pinnaculum/py-multiformats-cid.svg?branch=master
        :target: https://travis-ci.org/pinnaculum/py-multiformats-cid?branch=master

.. image:: https://codecov.io/gh/pinnaculum/py-multiformats-cid/branch/master/graph/badge.svg
        :target: https://codecov.io/gh/pinnaculum/py-multiformats-cid


What is CID ?
=============

`CID <https://github.com/multiformats/cid>`_ is a format for referencing content in distributed information systems,
like `IPFS <https://ipfs.io>`_.
It leverages `content addressing <https://en.wikipedia.org/wiki/Content-addressable_storage>`_,
`cryptographic hashing <https://simple.wikipedia.org/wiki/Cryptographic_hash_function>`_, and
`self-describing formats <https://github.com/multiformats/multiformats>`_.

It is the core identifier used by `IPFS <https://ipfs.io>`_ and `IPLD <https://ipld.io>`_.

CID is a self-describing content-addressed identifier.

It uses cryptographic hashes to achieve content addressing.

It uses several `multiformats <https://github.com/multiformats/multiformats>`_ to achieve flexible self-description,
namely `multihash <https://github.com/multiformats/multihash>`_ for hashes,
`multicodec <https://github.com/multiformats/multicodec>`_ for data content
types, and `multibase <https://github.com/multiformats/multibase>`_ to encode the CID itself into strings.

Sample Usage
============

.. code-block:: python

    >>> from multiformats_cid import make_cid
    >>> make_cid('QmaozNR7DZHQK1ZcU9p7QdrshMvXqWK6gpu5rmrkPdT3L4')
    CIDv0(version=0, codec=dag-pb, multihash=b"\x12 \xb9M'\xb9\x93M>\x08\xa5.R\xd7\xda}\xab\xfa\xc4\x84..")

    >>> cid = make_cid('QmaozNR7DZHQK1ZcU9p7QdrshMvXqWK6gpu5rmrkPdT3L4')
    >>> print(cid.version, cid.codec, cid.multihash)

    >>> print(cid.encode())
    QmaozNR7DZHQK1ZcU9p7QdrshMvXqWK6gpu5rmrkPdT3L4

    >>> str(cid)
    'QmaozNR7DZHQK1ZcU9p7QdrshMvXqWK6gpu5rmrkPdT3L4'


Installation
============

Stable release
~~~~~~~~~~~~~~

To install CID, run this command in your terminal:

.. code-block:: console

    $ pip install py-multiformats-cid

This is the preferred method to install CID, as it will always install the most recent stable release.

If you don't have `pip`_ installed, this `Python installation guide`_ can guide
you through the process.

.. _pip: https://pip.pypa.io
.. _Python installation guide: http://docs.python-guide.org/en/latest/starting/installation/

From sources
~~~~~~~~~~~~

The sources for CID can be downloaded from the `Github repo`_.

You can either clone the public repository:

.. code-block:: console

    $ git clone https://github.com/pinnaculum/py-multiformats-cid

Or download the `tarball`_:

.. code-block:: console

    $ curl  -OL https://github.com/pinnaculum/py-multiformats-cid/tarball/master

Once you have a copy of the source, you can install it with:

.. code-block:: console

    $ python setup.py install


.. _Github repo: https://github.com/pinnaculum/py-multiformats-cid
.. _tarball: https://github.com/pinnaculum/py-multiformats-cid/tarball/master

Other info
==========

* Free software: MIT license
* Documentation: https://py-multiformats-cid.readthedocs.io.
* Python versions: 3.7, 3.8, 3.9, 3.10
