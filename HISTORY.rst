History
-------

0.4.3 (2022-11-19)
==================

* Add typing hints: contribution from @bh2smith
* Add CI workflow

0.4.2 (2022-10-31)
==================

* Transition release to make mypy happy

0.4.0 (2022-10-31)
==================

* Rename py-cid to py-multiformats-cid (@pinnaculum)
* remove crazy version range limits for dependencies which cause major headaches
  for downstream projects with multiple confluent indirect dependencies on this library

0.2.1 (2018-10-20)
==================

* Fix edge cases with multibase and multihash decoding
* Added hypothesis tests while verifying CIDs

0.1.5 (2018-10-12)
==================

* Handle the case where an incorrect base58 encoded value is provided to `make_cid`


0.1.0 (2017-09-05)
==================

* First release on PyPI.
