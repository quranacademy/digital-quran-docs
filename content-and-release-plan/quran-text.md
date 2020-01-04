---
description: (under review)
---

# Quran text

This repository contains Quran as UTF-8 encoded plain text files, following the best Unicode practices as possible \(no more font specific hacks, no re purposing of totally unrelated code points and so one\), plus some tools to convert it into other document formats.

Some of the symbols used in this text were introduced in Unicode 6.1, so old applications or applications that haven’t been updated to Unicode 6.1 or newer might have issues displaying this text.

**The text have not been formally reviewed, yet, so it may contain some errors. If you find any please, please report it.**

Currently the text is best viewed using [Amiri Quran](http://www.amirifont.org) font, as it has all the needed symbols and layout rules.

### Variations from Tanzil's Text

* Add ayah numbers and End of Ayah \(U+06DD\) mark \(note that most fonts do not properly join the two\).
* Use regular Hamzah \(U+0621\) instead of Tatweel & Hamzah Above combination \(U+0640 & U+0654\).
* Use U+06CC \(Farsi Yeh\) for all Yaa' positions, instead of U+064A \(Arabic Yeh\) for starting and middle, and U+0649 \(Alef Maksura\) for final and isolated.
* Use open Tanween \(U+08F0, U+08F1, U+08F2\) in ikhfaa' and idghaam cases, instead of regular Tanween \(U+064B, U+064C, U+064D\).
* Don't use Tanween before U+06E2 \(Small High Meem\) \(i.e., in iqlaab cases\).
* Use U+06E1 \(Small High Dotless Head Of Khah\) instead of U+0652 \(Sukun\).
* Use U+06E4 \(Small High Madda\) instead of U+0653 \(Maddah Above\).
* No spaces before pause marks.
* Variation in the use and location of spaces \(some removed; some added\).
* Variation in the use and location of pause marks \(some removed; some added; as they are, in the end, simply indicators\).

