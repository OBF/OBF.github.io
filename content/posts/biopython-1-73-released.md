---
author: peterc
category:
  - biopython
  - blogroll
  - code
  - community
  - development
  - obf-projects
cover:
  alt: biopython_2017_banner_white_bg
  image: /wp-content/uploads/2017/07/biopython_2017_banner_white_bg.png
date: "2018-12-18T16:58:41+00:00"
guid: https://news.open-bio.org/?p=2112
tag:
  - biopython
  - obf-projects
  - release
  - releases
title: Biopython 1.73 released
url: /2018/12/18/biopython-1-73-released/

---
Dear Biopythoneers,

Biopython 1.73 has been released and is available from our [website](https://biopython.org/wiki/Download) and [PyPI](https://pypi.python.org/pypi/biopython/1.73).

This release of Biopython supports Python 2.7, 3.4, 3.5 and 3.6. It has also been tested on PyPy2.7 v6.0.0 and PyPy3.5 v6.0.0.

As in recent releases, more of our code is now explicitly available under either our original " _Biopython License Agreement"_, or the very similar but more commonly used _"3-Clause BSD License"_.  See the [LICENSE.rst](https://github.com/biopython/biopython/blob/master/LICENSE.rst) file for more details.

The dictionary-like indexing in `Bio.SeqIO` and `Bio.SearchIO` will now explicitly preserve record order to match a behaviour change in the Python standard dict object. This means looping over the index will load the records in the on-disk order, which will be much faster (previously it would be effectively at random, based on the key hash sorting).

The "grant" matrix in Bio.SubsMat.MatrixInfo has been replaced as our original values taken from Gerhard Vogt's old webpages at EMBL Heidelberg were discovered to be in error. The new values have been transformed following Vogt's approach, taking the global maximum 215 minus the similarity scores from the original paper Grantham (1974), to give a distance measure.

Double-quote characters in GenBank feature qualifier values in `Bio.SeqIO` are now escaped as per the NCBI standard. Improperly escaped values trigger a warning on parsing.

There is a new command line wrapper for the BWA-MEM sequence mapper.

The string-based FASTA parsers in `Bio.SeqIO.FastaIO` have been optimised, which also speeds up parsing FASTA files using `Bio.SeqIO.parse()`.

Additionally, a number of small bugs and typos have been fixed with further additions to the test suite, and there has been further work to follow the Python PEP8, PEP257 and best practice standard coding style.

Many thanks to the Biopython developers and community for making this release possible, especially the following contributors:

- Alona Levy-Jurgenson (first contribution)
- Ariel Aptekmann
- Brandon Invergo
- Catherine Lesuisse
- Chris Rands
- Darcy Mason (first contribution)
- Devang Thakkar (first contribution)
- Ivan Antonov (first contribution)
- Jeremy LaBarage (first contribution)
- Juraj Szász (first contribution)
- Kai Blin
- Konstantin Vdovkin (first contribution)
- Manuel Nuno Melo (first contribution)
- Maximilian Greil
- Nick Negretti (first contribution)
- Peter Cock
- Rona Costello (first contribution)
- Spencer Bliven
- Wibowo 'Bow' Arindrarto
- Yi Hsiao (first contribution)

For reference, checksums:

 `$ md5sum biopython-1.73*
9bab1776b3f63cb2a81715e78abfb6e0  biopython-1.73-cp27-cp27m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
a531f656ecae854adf1fc6021735c2a9  biopython-1.73-cp27-cp27m-manylinux1_i686.whl
27f5179f2493408d33e5322690f1bb7a  biopython-1.73-cp27-cp27m-manylinux1_x86_64.whl
41fdb1f257cdcd030a468e7339a6c6ab  biopython-1.73-cp27-cp27mu-manylinux1_i686.whl
bf23d2daae5c72c2d84058bce3acd7a2  biopython-1.73-cp27-cp27mu-manylinux1_x86_64.whl
d3cab98752b83cef121b7a1e8b81853c  biopython-1.73-cp27-cp27m-win32.whl
178be72d7b294a2a15c92630bbee2a81  biopython-1.73-cp27-cp27m-win_amd64.whl
32fc6184cbf21faca0776251570b2c58  biopython-1.73-cp34-cp34m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
5c78b8210de0b511c208facf7325c7e6  biopython-1.73-cp34-cp34m-manylinux1_i686.whl
ae414b4666900567579cc92df4223521  biopython-1.73-cp34-cp34m-manylinux1_x86_64.whl
1b0d7ba1b4c097b318213431d9b6b99e  biopython-1.73-cp34-cp34m-win32.whl
04a91b6ea826596b0c8b643b743d176f  biopython-1.73-cp34-cp34m-win_amd64.whl
a8ecaa7bf30fd912536881228e754664  biopython-1.73-cp35-cp35m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
0676a634a73e049903a4bc36e3b60fc3  biopython-1.73-cp35-cp35m-manylinux1_i686.whl
6d4ebb6131a611a71816b0208747de55  biopython-1.73-cp35-cp35m-manylinux1_x86_64.whl
65165d6551e43bdc18e0912935f9c7fd  biopython-1.73-cp35-cp35m-win32.whl
24c6352a143ea28c47bff5da754f0af9  biopython-1.73-cp35-cp35m-win_amd64.whl
d11a2c7ba85a9927815fb9b6dfd9a0ac  biopython-1.73-cp36-cp36m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
8898e77221359b4d4280e42a53bfbc52  biopython-1.73-cp36-cp36m-manylinux1_i686.whl
fb8a38c943a9e80492ddb657e9d330a5  biopython-1.73-cp36-cp36m-manylinux1_x86_64.whl
1f49d1a5b492639008dd674b83a8bcb7  biopython-1.73-cp36-cp36m-win32.whl
f0dde83e1a7c27a107e6aeb253f29f08  biopython-1.73-cp36-cp36m-win_amd64.whl
e082d026d3bb894838e389f159a8362b  biopython-1.73-cp37-cp37m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
0db98f888700a7e119f39f136687c3d1  biopython-1.73-cp37-cp37m-manylinux1_i686.whl
c92184fad3be8c8ba3cc3e8816603dc5  biopython-1.73-cp37-cp37m-manylinux1_x86_64.whl
58c58f52d514bd9a86df01da1db0d804  biopython-1.73-cp37-cp37m-win32.whl
e32acd6a4a2c703ee5ff34cd62f83124  biopython-1.73-cp37-cp37m-win_amd64.whl
d1d2e6154c2c89d6bb0e77f4a3578686  biopython-1.73.tar.gz
478d71daf63e9b57775fbd5aaa8f48f1  biopython-1.73.zip`  `$ sha256sum biopython-1.73*
c43a47ad3397336aa7af5a0bb5ebec91aa2ae328b71421e550cf7e7f80d00f69  biopython-1.73-cp27-cp27m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
0302d5be80850fbaa93789ab516d189c9400755901cfe566a324e8fea10ed39b  biopython-1.73-cp27-cp27m-manylinux1_i686.whl
e5b5666724cab7983aebeb593e52dd276ff9fdabb3669d57db8b5ea303a097a5  biopython-1.73-cp27-cp27m-manylinux1_x86_64.whl
21723d79a1d15e99c823b440dd37176259dffa686e2a015919ad255d89238491  biopython-1.73-cp27-cp27mu-manylinux1_i686.whl
85d53b91406aacfef673fb3cf24873d978654fa49d52b5ab4d9c3b0d06b003d6  biopython-1.73-cp27-cp27mu-manylinux1_x86_64.whl
c5beb53e2d5a5a573baaaa449a32d3adfb3d03bd7752adbcb20a62d6e8041e03  biopython-1.73-cp27-cp27m-win32.whl
add575d5b81eec95381a53ca8c042e9de9e506b24734ec773690247d997eaa69  biopython-1.73-cp27-cp27m-win_amd64.whl
59610b1639a7d9c1f36a5398e748c044c21f4285230fa79fcea2cafe835f9366  biopython-1.73-cp34-cp34m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
1c4b55412c12b246b948c3bbb30e60a7b075da9770449371a731ac9987849381  biopython-1.73-cp34-cp34m-manylinux1_i686.whl
aed261f47f72d63292fdf4c81197fdbc150094a34e10176647a932c83e179db9  biopython-1.73-cp34-cp34m-manylinux1_x86_64.whl
3cc401c15a85829eb6ae01babb02fbe7828548709b4dcb6d5149e94d5173ed7c  biopython-1.73-cp34-cp34m-win32.whl
f49558bea021cc5243e50efb38d545842153cde276e14879d6d63222065c683d  biopython-1.73-cp34-cp34m-win_amd64.whl
a149ea816f21ef72e1b4e6f538b13141584bdc531f864c5f1eb8b8feed71ba06  biopython-1.73-cp35-cp35m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
e7a03ae81b5507b3a668f81a58351c065fa6d8a0b77f772e183eb284c1cc4619  biopython-1.73-cp35-cp35m-manylinux1_i686.whl
fce8051b05d62d7d0ff7af0999f6874bd9af17f0613e6c8664ac20c93215345a  biopython-1.73-cp35-cp35m-manylinux1_x86_64.whl
99e6f78317c68b27a8b406c5595364005d43fee67f3b8ae20c3332588999442f  biopython-1.73-cp35-cp35m-win32.whl
839882c1929476538f9872e7fe6617c6fbcd65989483254817effbc388feead1  biopython-1.73-cp35-cp35m-win_amd64.whl
164b9958d1714f318015900f2689fcc08859f76b11484e8f91f1f29acb4b7465  biopython-1.73-cp36-cp36m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
d120346e2eed46beaf1d0771826a18cee7c3155cc8c0dafc6ffffc74ac49e8fc  biopython-1.73-cp36-cp36m-manylinux1_i686.whl
92c0940c5c2a76b559538a4eb1fc0277d3e960209c537d5b74632fa87a51a810  biopython-1.73-cp36-cp36m-manylinux1_x86_64.whl
5542f847a860b90e742a1be8a9807aa57accacd2bccfb07b3f6511f85201af19  biopython-1.73-cp36-cp36m-win32.whl
ef69ed6acf7bee26c530e40a768d060f46eef228d06aa2ea89439d3c54759bd8  biopython-1.73-cp36-cp36m-win_amd64.whl
cfb44ba6cdfb1dbfc05b7e46f26286b37d35b2bb847868c9088e9b67060fd7be  biopython-1.73-cp37-cp37m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
ede4e4335828a780dc2096fd0443c45efb3f8fcac741e544454997b978ad3cf3  biopython-1.73-cp37-cp37m-manylinux1_i686.whl
26f8ae8ddf06c85dab12f5aaff538593c7cec69102bb4ad968b3eb40a0477bf8  biopython-1.73-cp37-cp37m-manylinux1_x86_64.whl
93d79520586b48a2a77bec3a0623871b656c45dbb83c9b6834540f0a7232478e  biopython-1.73-cp37-cp37m-win32.whl
0fa9346c8ec144da12a556861090cfe5fbb6ecd89418d6358047b90def48e032  biopython-1.73-cp37-cp37m-win_amd64.whl
70c5cc27dc61c23d18bb33b6d38d70edc4b926033aea3b7434737c731c94a5e0  biopython-1.73.tar.gz
ade6ebfd01d58e7937a53f16e2d87e17509ec8335fe2573f39bdb7495e7e3d2b  biopython-1.73.zip`
