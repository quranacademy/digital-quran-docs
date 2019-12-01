---
description: >-
  Here are provided some examples of files parsing code for the most common
  usecases
---

# Code examples

## Get translations in &lt;surah, ayah \[, word\], text&gt; format

The most common way to use a translation is to get it in csv-like format, i.e. like `<surah, ayah, text>` \(or `<surah, ayah, word, text>` for word-by-word translations\) format. To do so, one can easily read a **JSON** translation file:

{% tabs %}
{% tab title="Python" %}
```python
import json

# Read the json translation-file
with open(path_to_json_file, "r") as translation_file:
    translation = json.load(translation_file)

# Loop over surahs-ayahs-words
for surah in translation["content"]["surahs"]:
    for ayah in surah["ayahs"]:
        print(surah["number"], ayah["number"], ayah["text"]) # Put your code here
        # For a word-by-word translation add one more loop:
        #for word in ayah["words"]:
        #    print(surah["number"], ayah["number"], word["number"], word["text"])

```
{% endtab %}

{% tab title="PHP" %}
```php
<?php
// Read the json translation-file
$translation_file = file_get_contents($path_to_json_file);
$translation = json_decode($translation_file, true);

// Loop over surahs-ayahs-words
foreach ($translation['content']['surahs'] as $surah) {
  foreach ($surah['ayahs'] as $ayah) {
    echo $surah['number'], $ayah['number'], $ayah['text']; // Put your code here
    // For a word-by-word translation add one more loop:
    //foreach ($ayah['words'] as $word) {
    //  echo $surah['number'], $ayah['number'], $word['number'], $word['text'];
    //}      
  }
}
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
// Read the json translation-file
const translation = require(path_to_json_file);

// Loop over surahs-ayahs-words
for (surah of translation.content.surahs) {
    for (ayah of surah.ayahs) {
        console.log(surah.number, ayah.number, ayah.text); // Put your code here
        // For a word-by-word translation add one more loop:
        //foreach (word of ayah.words) {
        //  console.log(surah.number, ayah.number, word.number, word.text);
        //}  
    }
}
```
{% endtab %}
{% endtabs %}

You can do the same, using **XML** formatting. 

{% hint style="info" %}
JavaScript is an exception since one of the most popular ways to read xml in node.js is transforming xml to json. So, for JavaScript users, it is recommended to stick with json format.
{% endhint %}

{% tabs %}
{% tab title="Python" %}
```python
from xml.etree import ElementTree as ET

# Read the XML translation-file
translation = ET.parse(path_to_xml_file).getroot()

# Loop over surahs-ayahs-words
for surah in translation.findall("content/surahs/surah"):
    for ayah in surah.findall("ayahs/ayah"):
        print(surah.attrib["number"], ayah.attrib["number"], ayah.text) # Put your code here
        # For a word-by-word translation add one more loop:
        #for word in ayah.findall("words/word"):
        #    print(surah.attrib["number"], ayah.attrib["number"], word.attrib["number"], word.text)
        
```
{% endtab %}

{% tab title="PHP" %}
```php

```
{% endtab %}
{% endtabs %}

## Get meta information

Here are some examples how one can read meta-data from the files

{% tabs %}
{% tab title="Python" %}
```python
# Choose the language: en - for English, and native - for native
language = "en"

# Get the name of the translation
translation_json["meta"]["name"][language]
translation_xml.find(f"meta/name/{language}").text

# Get authors names
[author["name"][language] for author in translation_json["meta"]["authors"]]
[name.text for name in translation_xml.findall(f"meta/authors/author/name/{language}")]

# Get surah names. Change `names` to `nameTrnaliterated` for transliterated names
[surah["name"] for surah in translation_json["content"]["surahs"]]
[name.text for name in translation_xml.findall("content/surahs/surah/name")]

```
{% endtab %}

{% tab title="PHP" %}
```php
// Choose the language: en - for English, and native - for native
$language = "en"

// Get the name of the translation
$translation_json["meta"]["name"][$language]

// Get authors names
$get_author_name = function($author, $lang=$language) {
    return $autor["name"][$lang];
};
array_map($get_author_name, $translation_json["meta"]["authors"]);

// Get surah names. Change `names` to `nameTrnaliterated` for transliterated names
$get_surah_name = function($surah) {
    return $surah["name"];
};
array_map($get_surah_name, $translation_json["content"]["surahs"]);

```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
// Choose the language: en - for English, and native - for native
const language = "en";

// Get the name of the translation
translation.meta.name[language]

// Get authors names
translation.meta.authors.map(author => author.name[language])

// Get surah names. Change `names` to `nameTrnaliterated` for transliterated names
translation.content.surahs.map(surah => surah.name)

```
{% endtab %}
{% endtabs %}

