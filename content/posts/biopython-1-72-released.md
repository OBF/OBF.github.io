---
author: peterc
category:
  - biopython
  - blogroll
  - code
  - development
  - obf-projects
cover:
  alt: biopython_2017_banner_white_bg
  image: /wp-content/uploads/2017/07/biopython_2017_banner_white_bg.png
date: "2018-06-27T19:06:41+00:00"
guid: https://news.open-bio.org/?p=1975
tag:
  - biopython
  - code
  - community
  - news
  - obf
  - obf-projects
  - open-source
  - release
  - releases
title: Biopython 1.72 released
url: /2018/06/27/biopython-1-72-released/

---
Dear Biopythoneers,

I'm writing this in Portland at the [GCC BOSC 2018 conference](https://gccbosc2018.sched.com/), where I will present the Biopython Project Update 2018 talk tomorrow. Yesterday during my airport layover in Iceland, I published the Biopython 1.72 release to our website and PyPI:

[https://biopython.org/wiki/Download](https://biopython.org/wiki/Download) [https://pypi.python.org/pypi/biopython/1.72](https://pypi.python.org/pypi/biopython/1.72)

This release of Biopython supports Python 2.7, 3.4, 3.5 and 3.6. It has also been tested on PyPy2.7 v6.0.0 and PyPy3.5 v6.0.0.

Internal changes to Bio.SeqIO have sped up the SeqRecord .format method and SeqIO.write (especially when used in a for loop).

The MAF alignment indexing in Bio.AlignIO.MafIO has been updated to use inclusive end co-ordinates to better handle searches at end points. This will require you to rebuild any existing MAF index files.

In this release more of our code is now explicitly available under either our original "Biopython License Agreement", or the very similar but more commonly used "3-Clause BSD License". See the LICENSE.rst file for more details.

The Entrez module now supports the NCBI API key. Also you can now set a custom directory for DTD and XSD files. This allows Entrez to be used in environments like AWS Lambda, which restricts write access to specific directories. Improved support for parsing NCBI Entrez XML files that use XSD schemas.

Internal changes to our C code mean that NumPy is no longer required at compile time - only at run time (and only for those modules which use NumPy).

Seq, UnknownSeq, MutableSeq and derived classes now support integer multiplication methods, matching native Python string methods.

A translate method has been added to Bio.SeqFeature that will extract a feature and translate it using the codon\_start and transl\_table qualifiers of the feature if they are present.

Bio.SearchIO is no longer considered experimental, and so it does not raise warnings anymore when imported.

A new pairwise sequence aligner is available in Bio.Align, as an alternative to the existing pairwise sequence aligner in Bio.pairwise2.

Many thanks to the Biopython developers and community for making this release possible, especially the following contributors:

- Benjamin Vaisvil (first contribution)
- Blaise Li
- Chad Parmet
- Chris Rands
- Connor T. Skennerton
- Francesco Gastaldello
- Michiel de Hoon
- Pamela Russell (first contribution)
- Peter Cock
- Spencer Bliven
- Wibowo 'Bow' Arindrarto

Thank you all.

Peter

P.S. You can follow [@Biopython on Twitter](https://twitter.com/Biopython)

--

Checksums for interest/public record:

```
$ shasum -a 256 biopython-1.72*

abc14a111ed89332c902d239f516cc9ab84ab4458b577c61208dc4c20b74dc83
biopython-1.72-cp27-cp27m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl

3e8c85d4a3295be598a9e9616adeed8a4f81bd0452326aaea7bf81cca468f7c1
biopython-1.72-cp27-cp27m-manylinux1_i686.whl

f1b4abd90d0c84ab2c5dab704da1d397cf75ee41f72619a1802479c3768ac347
biopython-1.72-cp27-cp27m-manylinux1_x86_64.whl

b426a2d858414bed0c25fca155fdf27485347ce6f69805db65b8b36ec00a0f41
biopython-1.72-cp27-cp27mu-manylinux1_i686.whl

71762c193ffc9a1b936dfaa2d456fb172856f0952090483ee4a84635a1aa6fe3
biopython-1.72-cp27-cp27mu-manylinux1_x86_64.whl

57a449709df7a47980360ecbd2f195effc56e9b0253fa0e74fb00b10b44778e0
biopython-1.72-cp27-cp27m-win32.whl

3d3deb59c3f5d04d41aec443db4e89dbbdd0bb7749078f91e797935849c8db48
biopython-1.72-cp27-cp27m-win_amd64.whl

b76241a55a1ba832c2768733fb113eef1fdfa1d738aa1f84fcdd4ba0b6432394
biopython-1.72-cp34-cp34m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl

ad2c72c289561d51f6f7a9ae977e9cd54cd48b575b946421f82ede1ac24198cb
biopython-1.72-cp34-cp34m-manylinux1_i686.whl

3a199d469465c4f3c4c238f688d07b9bce4f504be73dead6cdf5d36a47728fcd
biopython-1.72-cp34-cp34m-manylinux1_x86_64.whl

16a99e2462ee5acb6962f3a1d344336db58d7b87acf9d5023beb3efe6ebb47a8
biopython-1.72-cp34-cp34m-win32.whl

defd163110d698ea534e470995c68c519bd56e4e23043ae9dd8b646f2a803e5b
biopython-1.72-cp34-cp34m-win_amd64.whl

5882ba8fb87cbbe36d9e5d87c9b8f3139d503fe7da1023b472760a8122e579e6
biopython-1.72-cp35-cp35m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl

99faabef8c563bf5a9ed80ea677a5fd9edab5c06405a08fe44fb0f5bd4f6af38
biopython-1.72-cp35-cp35m-manylinux1_i686.whl

539a475c263b68cd1ae3624648090bf1a5d853ec967d450e4cb991e63f72cb05
biopython-1.72-cp35-cp35m-manylinux1_x86_64.whl

874a3c30bf7287e003e3668b55bd73a243edb85f4249826cff54b6fe3740483a
biopython-1.72-cp35-cp35m-win32.whl

db3517d654c2ca81c57b2e4e5340650b55055eb3985e5732c5ec668cf70143f1
biopython-1.72-cp35-cp35m-win_amd64.whl

2fbfe0f2d7b731b638c41466987cf00e36e08502b3db2b2d72beb9cbb79097e3
biopython-1.72-cp36-cp36m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl

6d8e56e46cccc38fb8ac026e70f700528f0d5e6f264d03f9c348fb81dd7e65b6
biopython-1.72-cp36-cp36m-manylinux1_i686.whl

6d27eb0fda18f2f70661bcd498f2aa0148ce56953aac094c35d8a12fb8261482
biopython-1.72-cp36-cp36m-manylinux1_x86_64.whl

d3c7ba7b0ffb3dd5132093d4fb21782daccc0e41358e5887676c455e1ae841c9
biopython-1.72-cp36-cp36m-win32.whl

5e0b830ff270b16abf1f050a8bf4732c9f2da29d27fdd2be9aeab76b6d087919
biopython-1.72-cp36-cp36m-win_amd64.whl

ab6b492443adb90c66267b3d24d602ae69a93c68f4b9f135ba01cb06d36ce5a2
biopython-1.72.tar.gz

08e1d6b43d974efc3578a5e8eebe6c118b03feea21b96d964c7e461c5cf53c18
biopython-1.72.zip
```

```
$ md5sum biopython-1.72*

661d50514eaa8151192b2127f52a8f5e
biopython-1.72-cp27-cp27m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl

a66e12a83c44ee50f01888129658eba0  biopython-1.72-cp27-cp27m-manylinux1_i686.whl

d7eb8003d855b3b425e2d7b5062d390a
biopython-1.72-cp27-cp27m-manylinux1_x86_64.whl

13b4e63a2a4c97e3fefa5360425f5199  biopython-1.72-cp27-cp27mu-manylinux1_i686.whl

a5a418d1c4b6a2e58ccb73bafdc60a3e
biopython-1.72-cp27-cp27mu-manylinux1_x86_64.whl

e6ca44a18b5fc65e7ca4267f877fd9cc  biopython-1.72-cp27-cp27m-win32.whl

4978d56508b002591e7b6c931c5d54f4  biopython-1.72-cp27-cp27m-win_amd64.whl

eed950f7b23a3c42682f3f635a135e57
biopython-1.72-cp34-cp34m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl

50e8fc0e63ca3ad524ea8c5d237ed6b1  biopython-1.72-cp34-cp34m-manylinux1_i686.whl

d20e9cfa98ee8991b7008f64a44f6130
biopython-1.72-cp34-cp34m-manylinux1_x86_64.whl

1ea11554a42996491c847ae0cf36de97  biopython-1.72-cp34-cp34m-win32.whl

848d5d53c3a6c60d9e94528e6cc35087  biopython-1.72-cp34-cp34m-win_amd64.whl

bde20eb5d6abdaa6479113dc96690603
biopython-1.72-cp35-cp35m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl

75b83b673997dbae8a8fe1a6fa15d3e3  biopython-1.72-cp35-cp35m-manylinux1_i686.whl

b883f5439353885224789b9e25107661
biopython-1.72-cp35-cp35m-manylinux1_x86_64.whl

d76442d3fc18de8953936a6c5ef5a79f  biopython-1.72-cp35-cp35m-win32.whl

f043fa59e3fbd5d505599474aaed74b5  biopython-1.72-cp35-cp35m-win_amd64.whl

dab6b61605938b75eef18fa9cae944da
biopython-1.72-cp36-cp36m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl

49fd975593798f0d7a293ebe327f800e  biopython-1.72-cp36-cp36m-manylinux1_i686.whl

8259fbf571b15dc05f0405b5e99394ce
biopython-1.72-cp36-cp36m-manylinux1_x86_64.whl

4e0d4de83b89d632a5dad9ee417306f2  biopython-1.72-cp36-cp36m-win32.whl

acdf4e57da4fc90bf7c52c76c2bf4182  biopython-1.72-cp36-cp36m-win_amd64.whl

418fecc41f75353fde30de73586900ac  biopython-1.72.tar.gz

e1db4737caf6bd2f7443f7e3c986ebbb  biopython-1.72.zip
```
