---
marp: true
theme: gaia
---
<!-- _class: lead -->
# Intro to PDF/A
---
# What is PDF/A?
* PDF version for archiving and long-term preservation
* ISO standard
* Full replacement for paper
---
# Why PDF/A?
## goal: long-term reproducibility
* view regardless of SW/HW changes
* no file conversions required at later date
* make documents future proof
## $\rightarrow$ document must be self-contained
* PDF/A is a subset of PDF
---
# PDF/A forbids certain PDF features
* JavaScript and executable file launches
* Audio and video content
* Encryption
* External content references
* Certain forms of compression
* Certain PDF forms
---
# PDF/A requires certain optional PDF features
* Standards based metadata
* All fonts must be embedded and without IP concerns
* Colorspces must be specified in a device independent manner
---
# PDF/A versions
| version | published | ISO number | PDF version |
|---------|:---------:|------------|:-----------:|
| PDF/A-1 | 2005      | ISO 19005-1| 1.4         |
| PDF/A-2 | 2008      | ISO 19005-2| 1.7         |
| PDF/A-3 | 2012      | ISO 19005-3| 1.7         |
| PDF/A-4 | 2020      | ISO 19005-4| 2.0         |

* older versions are not obsolete!
    * PDF/A viewer must be backwards compatible
---
# Generating PDF/A documents
---
# Validating PDF/A documents
* checking to see if a document conforms to PDF/A
    * version and conformance level checks
* [veraPDF](https://verapdf.org/home/) 
    * open source
    * funded by European Commission, industry supported
* Adobe Acrobat Pro (paid version)
* review metadata
---
# References
* [Library of Congress: PDF/A](https://www.loc.gov/preservation/digital/formats/fdd/fdd000318.shtml)
* [PDF/A in a Nutshell](https://pdfa.org/resource/pdfa-in-a-nutshell-2-0/)
* 

