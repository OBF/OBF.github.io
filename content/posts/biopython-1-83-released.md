---
author: peterc
category:
  - biopython
  - code
  - development
  - obf-projects
cover:
  alt: Biopython logo
  image: /wp-content/uploads/2023/09/biopython_logo_s.png
date: "2024-01-10T13:46:10+00:00"
guid: https://www.open-bio.org/?p=7593
tag:
  - biopython
  - bosc
  - open-source
title: Biopython 1.83 released
url: /2024/01/10/biopython-1-83-released/

---
Dear Biopythoneers,

Our first release of 2024 is now out, sooner than planned as this is purely to revert the removal of the `.strand`, `.ref`, and `.ref_db` attributes of the `SeqFeature` which was done in Biopython 1.82 without a deprecation period. They are again aliases for `.location.strand` etc, but now trigger deprecation warnings. See our [deprecation policy](https://biopython.org/wiki/Deprecation_policy). We apologize for any inconvenience, and thank you to those reporting this.

This release of Biopython supports Python 3.8, 3.9, 3.10, 3.11 and 3.12. It has also been tested on PyPy3.9 v7.3.13. Python 3.8 is approaching end of life, our support for it is now deprecated.

Biopython 1.83 source releases are available from our [website](https://biopython.org/wiki/Download) and [PyPI](https://pypi.python.org/pypi/biopython/1.83), which also has pre-compiled wheels for the major platforms. We would expect the release to be on conda-forge shortly too.

Happy New Year!
