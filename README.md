Trying to see if it’s possible to work on an InDesign document on Git, with several branches (or contributors) doing different things on the same document. Then trying to merge the edits.

The INDD file format is binary, but the IDML file format is a (special) ZIP containing XML files.

**Process to work:**

1. Pull.
2. Run zip.sh to turn the document folder into a working IDML file.
3. Open the IDML, work in it.
4. Save.
5. Run unzip.sh to turn the IDML file into a commitable folder again.
6. Push.

(Both SH scripts are very raw.)

**Results**

* Modifications on the same page are almost impossible to merge.
* Any other modifications, even on different pages (and so recorded on different files), are not easy to merge because shared files keep changing and specific files keep being renamed. A lot of XML manual editing would be required, so it’s not interesting.

**Conclusion**

Unless it’s possible to make a custom script to handle merging IDMLs, InDesign documents are really not ready to be worked through Git! More testing later.
