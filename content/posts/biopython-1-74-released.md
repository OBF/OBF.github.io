---
author: peterc
category:
  - biopython
  - blogroll
  - code
  - community
  - development
  - documentation
  - obf-projects
cover:
  alt: biopython
  image: /wp-content/uploads/2019/02/biopython.png
date: "2019-07-16T19:39:56+00:00"
guid: https://www.open-bio.org/?p=3776
tag:
  - biopython
  - obf-projects
  - release
  - releases
title: Biopython 1.74 released
url: /2019/07/16/biopython-1-74-released/

---
Dear Biopythoneers,

Biopython 1.74 has been released and is available from our [website](https://biopython.org/wiki/Download) and [PyPI](https://pypi.python.org/pypi/biopython/1.74).

This release of Biopython supports Python 2.7, 3.4, 3.5, 3.6 and 3.7. However, it will be the last release to support Python 3.4 which is now at end-of-life. It has also been tested on PyPy2.7 v6.0.0 and PyPy3.5 v6.0.0.

(Please note we will be dropping support for Python 2.7 in early 2020.)

Over half our code is now explicitly available under either our original "Biopython License Agreement", or the very similar but more commonly used "3-Clause BSD License". See the `LICENSE.rst` file for more details.

Our core sequence objects ( `Seq`, `UnknownSeq`, and `MutableSeq`) now have a string-like `.join()` method.

The NCBI now allows longer accessions in the GenBank file LOCUS line, meaning the fields may not always follow the historical column based positions. We no longer give a warning when parsing these. We now allow writing such files (although with a warning as support for reading them is not yet widespread).

Support for the `mysqlclient` package, a fork of MySQLdb, has been added.

We now capture the IDcode field from PDB Header records.

`Bio.pairwise2`'s pretty-print output from `format_alignment` has been optimized for local alignments: If they do not consist of the whole sequences, only the aligned section of the sequences are shown, together with the start positions of the sequences (in 1-based notation). Alignments of lists will now also be prettily printed.

`Bio.SearchIO` now supports parsing the text output of the HHsuite protein sequence search tool. The format name is `hhsuite2-text` and `hhsuite3-text`, for versions 2 and 3 of HHsuite, respectively.

`Bio.SearchIO` HSP objects has a new attribute called `output_index`. This attribute is meant for capturing the order by which the HSP were output in the parsed file and is set with a default value of -1 for all HSP objects. It is also used for sorting the output of `QueryResult.hsps`.

`Bio.SeqIO.AbiIO` has been updated to preserve bytes value when parsing. The goal of this change is make the parser more robust by being able to extract string-values that are not utf-8-encoded. This affects all tag values, except for ID and description values, where they need to be extracted as strings to conform to the `SeqRecord` interface. In this case, the parser will attempt to decode using `utf-8` and fall back to the system encoding if that fails. This change affects Python 3 only.

`Bio.motifs.mast` has been updated to parse XML output files from MAST over the plain-text output file. The goal of this change is to parse a more structured data source with minimal loss of functionality upon future MAST releases. Class structure remains the same plus an additional attribute `Record.strand_handling` required for diagram parsing.

`Bio.Entrez` now automatically retries HTTP requests on failure. The maximum number of tries and the sleep between them can be configured by changing `Bio.Entrez.max_tries` and `Bio.Entrez.sleep_between_tries`. (The defaults are 3 tries and 15 seconds, respectively.)

All tests using the older print-and-compare approach have been replaced by unit tests following Python's standard testing framework.

On the documentation side, all the public modules, classes, methods and functions now have docstrings (built in help strings). In addition to displaying the [Biopython API documentation via epydoc](https://biopython.org/DIST/docs/api/), we now also have the [Biopython API documentation via Sphinx](https://biopython.org/docs/1.74/api/) (which we hope to make the default in future). Furthermore, the PDF version of the _Biopython Tutorial and Cookbook_ now uses syntax coloring for code snippets.

Additionally, a number of small bugs and typos have been fixed with further additions to the test suite, and there has been further work to follow the Python PEP8, PEP257 and best practice standard coding style.

Many thanks to the Biopython developers and community for making this release possible, especially the following contributors:

- Andrey Raspopov (first contribution)
- Antony Lee
- Benjamin Rowell (first contribution)
- Bernhard Thiel
- Brandon Invergo
- Catherine Lesuisse
- Chris Rands
- Deepak Khatri (first contribution)
- Gert Hulselmans
- Jared Andrews
- Jens Thomas (first contribution)
- Konstantin Vdovkin
- Lenna Peterson
- Mark Amery
- Markus Piotrowski
- Micky Yun Chan (first contribution)
- Nick Negretti
- Peter Cock
- Peter Kerpedjiev
- Ralf Stephan
- Rob Miller
- Sergio Valqui
- Victor Lin
- Wibowo 'Bow' Arindrarto
- Zheng Ruan

For reference, checksums:

```
$ md5sum biopython-1.74*
 808a8cc83ef7ae8328de47112a9619c9  biopython-1.74-cp27-cp27m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
 bc71b115d62fa0505b05dcb8d51ebbb3  biopython-1.74-cp27-cp27m-manylinux1_i686.whl
 eb9b68d29187208688f3763d7f9b4443  biopython-1.74-cp27-cp27m-manylinux1_x86_64.whl
 e060e2971cb64488392690f2b49a894a  biopython-1.74-cp27-cp27mu-manylinux1_i686.whl
 69e2b9aea866248dcb250b0d4749347c  biopython-1.74-cp27-cp27mu-manylinux1_x86_64.whl
 301964b516d9a1af29db36c45e97857c  biopython-1.74-cp27-cp27m-win32.whl
 72549961e56ba7c00ddf5aa4d4a2c4b7  biopython-1.74-cp27-cp27m-win_amd64.whl
 7545b99fe59e820b3e5343463df9bf61  biopython-1.74-cp34-cp34m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
 a18c82789358cd3a6cf854750bbf9216  biopython-1.74-cp34-cp34m-manylinux1_i686.whl
 33f5c75fe0fd63bba49afb19077a6067  biopython-1.74-cp34-cp34m-manylinux1_x86_64.whl
 2d42a3e23b976a4a7db837b9d2782df1  biopython-1.74-cp34-cp34m-win32.whl
 9a74dbfa0c81848ce107ad3c169ce1d3  biopython-1.74-cp34-cp34m-win_amd64.whl
 6fc5cce9f94e5cac1aa4b57774e8626b  biopython-1.74-cp35-cp35m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
 7c8e4473a474c05e39d70d8106dbd641  biopython-1.74-cp35-cp35m-manylinux1_i686.whl
 dc9710022e6409590fc99bc82309cd8d  biopython-1.74-cp35-cp35m-manylinux1_x86_64.whl
 fe2623ea21ca2e9f057eae333d0ae386  biopython-1.74-cp35-cp35m-win32.whl
 b4b59bbf517e42c8e1abfbe7af2a6893  biopython-1.74-cp35-cp35m-win_amd64.whl
 a28eaf891cd04af42ea6391477c968d8  biopython-1.74-cp36-cp36m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
 74761f292187cfc06166107230d94dcd  biopython-1.74-cp36-cp36m-manylinux1_i686.whl
 62e7696d4597d7b7ff8bbf157191c284  biopython-1.74-cp36-cp36m-manylinux1_x86_64.whl
 419f489831ec20aa1e11384d2991676c  biopython-1.74-cp36-cp36m-win32.whl
 743a888661c48b66d41de2e6c04890d5  biopython-1.74-cp36-cp36m-win_amd64.whl
 025d4a914ad515b0181bdb0f8b1e8a2e  biopython-1.74-cp37-cp37m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
 db5ee8837a887188bcef09f57b5bf12f  biopython-1.74-cp37-cp37m-manylinux1_i686.whl
 f7602a46d3e2e3302f99437739652727  biopython-1.74-cp37-cp37m-manylinux1_x86_64.whl
 20075d6abfbdb011460829f624de0832  biopython-1.74-cp37-cp37m-win32.whl
 ffdd7986cb63dedf8daa4fb78140bbac  biopython-1.74-cp37-cp37m-win_amd64.whl
 cead2bfe9e7be45267eba00635f68d5c  biopython-1.74.tar.gz
 ff21159f333f433f3fa5a01a791cf717  biopython-1.74.zip
```

```
$ sha256sum biopython-1.74*
 6182f8c17c81aa40987b018e6241719137e463f5bb263c423db6180d118d3a03  biopython-1.74-cp27-cp27m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
 7103f3dd3cef9f6ae52c0c3275ecb65121f3935b90d25c5e149ce62f684fbaf2  biopython-1.74-cp27-cp27m-manylinux1_i686.whl
 bb302ad68a133ed3ae26efa0a0c82a0905c8b9b85a70fa6626611a882a65ec61  biopython-1.74-cp27-cp27m-manylinux1_x86_64.whl
 77145b88a74c89f752db2ed11f64737161cc337c9e520e3853c945bd1d9866e6  biopython-1.74-cp27-cp27mu-manylinux1_i686.whl
 022909d10bbdfbc70eba6ea1c06ff573444e26e40ef0899025fb269898604b16  biopython-1.74-cp27-cp27mu-manylinux1_x86_64.whl
 540f9df15e11f091e2d92959b891d2001bb59660ca806d51ca30d76dab60d39e  biopython-1.74-cp27-cp27m-win32.whl
 36c35d93d16c9270303bfc755d2364171a1aaebd75f3bfa97179712a3ac09e2d  biopython-1.74-cp27-cp27m-win_amd64.whl
 d6a310fab78e11dba51b55a2b194a79128d202584127e17952f7f64b52da83e2  biopython-1.74-cp34-cp34m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
 d3bf43ea45859bec05e8496c39dbd614c75520a832da20d826fdbd7e83105414  biopython-1.74-cp34-cp34m-manylinux1_i686.whl
 8b7a3edd0dcc9eae3020849ad6110c721399f2c8dd71e54317dcc50035f9ebf9  biopython-1.74-cp34-cp34m-manylinux1_x86_64.whl
 32c50dd9450ac780d640baa212ecde22fcc98dc0de472b40296968df2385c824  biopython-1.74-cp34-cp34m-win32.whl
 015b79eea59bb5ccf7abef2ab17a813540c5c1969a8def2148fe3d529ff405a3  biopython-1.74-cp34-cp34m-win_amd64.whl
 1324bd2f6ea1dbad748085875d4c206f08748bb7848355f365d31fcd771dfa75  biopython-1.74-cp35-cp35m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
 6d9a39f295d97ed953a48c1cde635b35205ed25034015238776dbd2a8afbb2a7  biopython-1.74-cp35-cp35m-manylinux1_i686.whl
 273c524550aaad3284edbdacecdf66cfd880dac580a5f6c5f80a9925a70144fb  biopython-1.74-cp35-cp35m-manylinux1_x86_64.whl
 e6cc6e725a5fb628d41ed675bb74aa5eb03763e1ccd3111d0f73f739c7263ab4  biopython-1.74-cp35-cp35m-win32.whl
 aa07bcf7def1c270c1fc1bab25f72a34f1ba24ab0a2d680f0a8466b39a2a7660  biopython-1.74-cp35-cp35m-win_amd64.whl
 efee2f77cef1b65a76fe27af83c05774329b481c2da71d0580fcbcf92d6e9988  biopython-1.74-cp36-cp36m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
 f50ee861a67e96488d21bc210ea72250df8cb7578351366f52c3904b841b5fbe  biopython-1.74-cp36-cp36m-manylinux1_i686.whl
 fa8ed2c3fec5dc45f9b750bd5da386f82cddb7944b456bfd0472106050efa397  biopython-1.74-cp36-cp36m-manylinux1_x86_64.whl
 7c32c37b20843e1d22e76c889f1733097e27996d1ec0fe54d84e5f737c9ff65e  biopython-1.74-cp36-cp36m-win32.whl
 046510af3cbaaf822e7451f0772e3e3f327916edbfd1f34798e6b8cbf60e8aa3  biopython-1.74-cp36-cp36m-win_amd64.whl
 67144db2defb3b49d505c7c4c676ca80b3451a0764f507b930b86031b7ebde5c  biopython-1.74-cp37-cp37m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
 b8cdfaf2963b7ef24497aa82e60bfc86267989f32a49b4edd4a67aba75202834  biopython-1.74-cp37-cp37m-manylinux1_i686.whl
 a117596b366e2226e2bf0adaf87f32cda495357c398b1b2ca2ada9f54c386718  biopython-1.74-cp37-cp37m-manylinux1_x86_64.whl
 3a802aba32b64aee9c3b92d8b5d50aa3d0a95c8188b69a78a2cbc292578dae08  biopython-1.74-cp37-cp37m-win32.whl
 ca627475233f698ede17b5adb169ed10b44ab4dc3a48d71069d7ab0086bdbc1c  biopython-1.74-cp37-cp37m-win_amd64.whl
 25152c1be2c9205bf80901fc49adf2c2efff49f0dddbcf6e6b2ce31dfa6590c0  biopython-1.74.tar.gz
 546dd36c5ba18696d6b4673d8f68c01bd27b016f2e3fdefb5ff848f646a91ba4  biopython-1.74.zip
```
