# Security Policy

## Supported Versions

Use this section to tell people about which versions of your project are
currently being supported with security updates.

| Version | Supported          |
| ------- | ------------------ |
| 5.1.x   | :white_check_mark: |
| 5.0.x   | :x:                |
| 4.0.x   | :white_check_mark: |
| < 4.0   | :x:                |

## Reporting a Vulnerability

Use this section to tell people how to report a vulnerability.

Tell them where to go, how often they can expect to get an update on a
reported vulnerability, what to expect if the vulnerability is accepted or
declined, etc.

# Copyright 2010 by Peter Cock.  All rights reserved.

# This code is part of the Biopython distribution and governed by its

# license.  Please see the LICENSE file that should have been included

# as part of this package.


"""Testing online code in Bio.SCOP module."""


import unittest


from Bio import SCOP


import requires_internet


requires_internet.check()



class ScopSearch(unittest.TestCase):

    """SCOP search tests."""


    def test_search(self):

        """Test search."""

        handle = SCOP.search("1JOY")



if __name__ == "__main__":

    runner = unittest.TextTestRunner(verbosity=2)

    unittest.main(testRunner=runner)

