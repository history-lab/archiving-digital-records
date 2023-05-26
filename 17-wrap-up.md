---
marp: true
theme: gaia
class:
  - invert
paginate: true
---
<!-- _class: lead -->
# Wrap-up
---
# Local Install
1. Instal Visual Studio Code
     * it's what we've been using in codespaces
     * [macOS](https://code.visualstudio.com/docs/setup/mac)
     * [windows](https://code.visualstudio.com/docs/setup/windows)

2. poppler-utils 
    * reach out to Ben
    * right path dependent on OS and what you have installed
---
# Possible Next Steps
* Start working on your project
* Read the books - Doing Digital History, Hermeneutica
* Consider Python Programming
     * [Python Tutorials for Digital Humanities](https://www.youtube.com/@python-programming)
     * [The Right Mindset](https://norvig.com/21-days.html)
* Check out the [Programming Historian](https://programminghistorian.org/)
---
<!-- _class: lead -->
# Follow-ups
---
# OCRing a scanned PDF
1. install additional software in codespace:
```
sudo apt-get update
sudo apt-get install ocrmypdf tesseract-ocr-all poppler-utils imagemagick
```
2. get a scanned pdf (no text)
https://www.pfu.ricoh.com/global/scanners/downloads/v5/sv600_m_normal.pdf

3. run ocrmypdf:
```
ocrmypdf sv600_m_normal.pdf ocred.pdf
```
---
# NER
* [Code example](https://colab.research.google.com/github/NukeAce/HNG-named-entity-recognition/blob/master/Named_entity_recognition_using_spacy_model.ipynb#scrollTo=4zSSlTgxLAwK)
---
# Adding metadata


