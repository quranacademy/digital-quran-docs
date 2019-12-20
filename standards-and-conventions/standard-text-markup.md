---
description: >-
  Quranic Text Markup Language is the standard markup language for Quranic texts
  like translations, tafsirs.
---

# Quranic Text Markup Language \(QTML\)

**VERSION 0.1**

{% hint style="info" %}
The standard is currently under the development. Versions 0.x will be used for versioning untill the first stable standard released with version **1**. After the first stable version, versions will be in single integer format, i.e. 2, 3, 4, etc. 
{% endhint %}

Quran related texts like translations and tafsirs have a very specific and complicated structure. Without a detailed markup, it is difficult to render these texts in proper and convenient way. Wouldn't it be nice to render all Quran references in a tafsir as a link or a tooltip? Prettify quotations, footnotes, headers, etc.? Besides prettier rendering, some elements, like Arabic words inside not-Arabic, might be rendered incorrectly without the proper handling. 

QTML was created to address all these problems. Basically it is a special XML format for Quranic/Islamic content. You can think of it like HTML for the web: having common markup standards allows developers to create better products for the users. Why don't we do the same for Quranic content?

{% hint style="info" %}
**NOTE**: Developers don't have to worry about parsing QTML. Along with QTML, compiling scripts on different programming languages will be provided \(**TODO**\), so developers can focus on their product instead of parsing QTML. For example, using provided compiler, one can easily translate QTML text to HTML with custom styles, classes, etc. 
{% endhint %}

## General standards

* Text in QTML format is a valid XML using only specific elements \(tags\) and attributes described in this standard \(see [the elements of QTML](standard-text-markup.md#the-elements-of-qtml)\)
* The root element is `<qtml>`
* There are two type of elements: block elements and inline elements:
  * Each text paragraph \(i.e. content block starting from a new line\) is wrapped by one of block elements \(see below\)
  * An element _**can not**_ contain a block element and _**can**_ ****contain any number of inline elements
* A footnotes block element, if presented, is the last block element
* QTML text encoded by UTF-8

## The elements and tags of QTML

### Block elements

Block elements mark content blocks starting from a new line such as: text paragraph, Quran citation, quotation, reference, footnote, etc. Each block element is described in details bellow.

#### Paragraph block \(&lt;p&gt;\)

Similar to HTML, the &lt;p&gt; tag defines a paragraph. It is used if none of the other block elements is eligible.

Each paragraph is in a separate `<p>` block. There is no line breaks inside a block.

_**Example:**_

```markup
 <p>This is some text in a paragraph.</p>
 <p>This is some text in a paragraph.</p>
```

#### Quran block \(&lt;quran&gt;\)

The Quran block is used to mark up a citation of the Quran ayah inside the text. This block includes only complete ayah citations:

* For short inline Quran citations `<inline-quran>` element is used
* For multi-ayah citation multiple `<quran>` blocks used: each ayah in a separate block

_**Attributes:**_ **`surah, ayah`**  The attributes provide the beginning and the ending ayah coordinates correspondingly. Where an ayah coordinate is a number of surah and ayah separated by a colon. For example, `4:3` is the coordinate of the 3rd ayah of the 4th surah.

_**Example:**_

```markup
<quran surah="30" ayah="21">
    <arabic>وَمِنْ آيَاتِهِ أَنْ خَلَقَ لَكُم مِّنْ أَنفُسِكُمْ أَزْوَاجًا لِّتَسْكُنُوا إِلَيْهَا وَجَعَلَ بَيْنَكُم مَّوَدَّةً وَرَحْمَةً إِنَّ فِي ذَلِكَ لَآيَاتٍ لِّقَوْمٍ يَتَفَكَّرُونَ</arabic>
    <translation>Среди Его знамений — то, что Он сотворил из вас самих жён для вас, чтобы вы находили в них успокоение, и установил между вами любовь и милосердие</translation>
</quran>
```

#### Footnotes block \(&lt;footnotes&gt;, &lt;footnote-content&gt;, &lt;footnote&gt;\)

In order to separate a footnote from the text, a footnote is split into two parts: 

* `<footnote>` - marks the position of the footnote inside the paragraph
* `<footnote-content>` - contains the text of the footnote

These two elements are linked by the `id` attribute. The value of the `id` attribute is also the subscript text \(usually a number\) inside the paragraph. 

While `<footnote>` elements are placed inside the paragraph, all the corresponding `<footnote-content>` elements are placed in a `<footnotes>` block at the end, i.e. it is always the last block element.

_**Example:**_ 

{% tabs %}
{% tab title="QTML" %}
```markup
<p>Ние ти дадохме<footnote id="1"/> ал-Каусар.<footnote id="2"/></p>

<footnotes>
    <footnote-content id="1">
        о, Мухаммад реката
    </footnote-content>
    <footnote-content id="2">
        “Каусар” е името на реката на изобилието, дарена на Мухаммед, мир нему, същевременно означава “голямо изобилие”. В тази сура се повелява да се прави жертвоприношение и се дава отговор на съдружаващите, които обиждали Пророка, наричайки го “Лишения” (“Ал-абтар”), защото нямал мъжка рожба.
    </footnote-content>
</footnotes>
```
{% endtab %}

{% tab title="Markdown" %}
```
Ние ти дадохме[^1] ал-Каусар.[^2]

[^1]: о, Мухаммад реката
[^2]: “Каусар” е името на реката на изобилието, дарена на Мухаммед, мир нему, същевременно означава “голямо изобилие”. В тази сура се повелява да се прави жертвоприношение и се дава отговор на съдружаващите, които обиждали Пророка, наричайки го “Лишения” (“Ал-абтар”), защото нямал мъжка рожба.
```
{% endtab %}
{% endtabs %}

#### Quote \(&lt;quote&gt;\)

Marks up a quotation or a citation from a source. Used for citations of a hadith or a scholar's quote. Optionaly, a source of the citation can be provided by the `source` attribute.

_**Attributes:**_ **`source`** \(optional\)

_**Example:**_

```markup
<p>Mujahid, Sa`id bin Jubayr and Ad-Dahhak said:</p>
<quote>
This  is  the  useful  kind  of  mud  which  sticks  to itself.
</quote>

<p>Ibn Abbas <radu/> and Ikrimah said:</p>
<quote>It is sticky and useful.</quote>

<p>Qatadah said:</p>
<quote source="The source name">It is that which sticks to the hand.</quote>
```

### Inline elements

The following elements are used inline, i.e. inside a block element.

#### Text formatting \(&lt;b&gt;, &lt;i&gt;, &lt;u&gt;\)

Tags are used to format a text between the start-tag and the end-tag to bold \(`<b>`\), italic \(`<i>`\), and underlines \(`<u>`\).

{% hint style="warning" %}
Similar to HTML, this tags should be avoided as mush as possible since QTML-elements are for semantics rather than styling. The main reason of these elements support is to enable marking words emphysised by the author in the way the most close to the original text \(i.e. author's choise\).
{% endhint %}

_**Example:**_ **TODO**

#### Arabic text \(&lt;arabic&gt;\)

This elements marks up Arabic text inside a text of the other language. For example, it is common to for non-Arabic \(or translated\) tafsirs to mix Arabic text with the native language. Mixing a left-to-right text with a right-to-left might often leads to an incorrect rendering of the text. That is why this tag is important to use in such cases.

_**Example:**_ 

```text
Original: Ибн Джарир и ат-Тирмизи добавили: «( الصَّمَدُ ) Самодостаточный - значит, ...
QTML: Ибн Джарир и ат-Тирмизи добавили: «(<arabic>الصَّمَدُ</arabic>) Самодостаточный - значит, ...
```

#### Inline Quran citation \(&lt;quran-inline&gt;\)

Self-closing tag. Marks up inline Quran citations, i.e. the citation is not separated from the text of the paragraph. Such elements are used in case of paticial ayah citation. For exmaple, sub-words of an ayah often used in tafsirs:

> ... Слово Аллаха: \(مَثْنَى وَثُلَاثَ وَرُبَاعَ\) И двух, и трех, и четырех – т.е. женитесь на других женщинах кроме них, если хотите на двух, на трёх и даже на четырёх.... \([Russin translation of Ibn Kathir, 4:3](https://en.quranacademy.org/quran/4:3)\)

{% hint style="warning" %}
For full ayah citation, `<quran>` block element is be used.
{% endhint %}

 _**Attributes:**_ **`from, till`**  The attributes provide the starting and the ending word coordinates correspondingly. Where a word coordinate is a number of surah, ayah, and word separated by a colon. For example, `4:3:5` is the coordinate of the 5th word in the 3rd ayah of the 4th surah.

_**Example:**_

```markup
... Слово Аллаха: <inline-quran from="4:3:13" to="4:3:15"/> И двух, и трех, и четырех – т.е. женитесь на других женщинах кроме них, если хотите на двух, на трёх и даже на четырёх...
```

#### Comment \(&lt;inline-comment&gt;\)

Marks a short inline comment made by the author in a translation. 

Such comments often can be found in a translation inside round \(`(`\) or squared \(`[`\) brackets. Some translations use both round and squared brackets to differentiate the meaning of comments. For example, `(` for words which are implicitly implied in the original Arabic text and `[` for clarifying text. To keep that information in the digital format, a `brackets` attribute is used.

Some translation also provide long inline comments in doubled squared brackets \(`[[`\). In that case, the long text semantically closer to a footnote, so should be marked up as a footnote \(see &lt;footnote&gt; + footnotes block\).

_**Attributes:**_ **`brackets=round|square`**

_**Example:**_ 

```markup
Original: Который научил (людей) (письму) пером [письменной тростью],
QTML: Который научил <inline-comment brackets="round">людей</inline-comment> <inline-comment brackets="round">письму</inline-comment> пером <inline-comment brackets="square">письменной тростью</inline-comment>,
```

#### Footnote \(&lt;footnote&gt;\)

Self-closing tag. Defines the position of the corresponding footnote content \(see `<footnotes>` block element\).

_**Attributes:**_ **`id`** id of the corresponding `<footnote-content>` element. 

_**Example:**_ See `<footnotes>` block element

#### Honorifics

> An **honorific** is a title that conveys esteem, courtesy, or respect for position or rank when used in addressing or referring to a person \([Wikipedia](https://en.wikipedia.org/wiki/Honorific)\).

Here are some examples of Islamic honorifics: _Subhanahu Wa Ta'ala, RadiAllahu_ \`_anhu,_ etc. Each honorific has its own [empty element with self-closing tag](https://www.w3schools.com/xml/xml_elements.asp). Here is the list of available honorifics and their tags:

| Tag | Applied to | Arabic | Transliteration | English |
| :--- | :--- | :--- | :--- | :--- |
| `<awj/>` | Allah | عزّ وجلّ‎ | Azza wa Jall | Mighty and the Majestic |
| `<swt/>` | Allah | سبحانه وتعالىٰ | Subhanahu wa Taʿālā | Glorified and Exalted be He |
| `<jal/>` | Allah | جل جلاله | Jalla Jalāluhu | The Most Exalted |
| `<sas/>` | Muhammad | صَلّى اللهُ عليهِ وسلّم | Ṣallallāhu ′alayhi wa sallam | May Allah send blessings and peace upon him |
| `<as/>` | Angels and prophets | عليه السلام | Alayhi s-salam | Peace be upon him |
| `<radu/>` | Companions of Muhammad | رضي الله عنه | Radiyallahu ′anhu | May Allah be pleased with him |
| `<rada/>` | Companions of Muhammad | رضي الله عنها | Radiyallahu ′anha | May Allah be pleased with her |
| `<radum/>` | Companions of Muhammad | رضي الله عنهم | Radiyallahu ′anhum | May Allah be pleased with them |
| `<raduma/>` | Companions of Muhammad | رضي الله عنهما | Radiyallahu ′anhuma | May Allah be pleased with them both |
| `<rahimahu/>` | Scholars | رحمه الله | Rahimullah | May Allah's mercy be upon him |
| `<rahimahum/>` | Scholars | رحمهم الله | Rahimullah | May Allah's mercy be upon them |
| `<rahimahuma/>` | Scholars | رحمهما الله | Rahimumallah | May Allah's mercy be upon them two |





