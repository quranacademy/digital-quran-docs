---
description: Here you can find standards related to translation files
---

# Translation files: description

All translations available in two formats: XML and JSON in UTF-8 encoding. Data in a file is split into two parts: 1\) meta-data, like authors, license, etc. -- called `meta` in files, 2\) translation itself -- called `content` in files.

{% hint style="info" %}
Translations are of two types: by-ayah and word-by-word. The structure of both types is mostly the same. The only difference is in the`ayah` object in the`content` part. See [Translation itself \(content\)](translation-files-structure.md#translation-itself-content) section below for the details.
{% endhint %}

{% hint style="danger" %}
Some by-ayah translations and most of the word-by-word translations have joined translations, i.e. when two \(or more\) words translated as one. See [Russian word-by-word translation of 90:14 at Quran Academy](https://ru.quranacademy.org/quran/90) for an example. Check [Translation texts](translation-texts.md) for more details.
{% endhint %}

## Meta-data \(meta\)

{% hint style="warning" %}
**NOTE.** Information in examples is not reliable! Please, do not treat it as real information. Mostly it is made up to just give you an idea of how values look like.
{% endhint %}

Meta-data \(`meta` in files\) provides information about the translation, like authors, contacts, licenses, etc. All information is provided in, at least, two languages: the language of the translation and English. Meta-data section has the following structure:

### language

The `language` section provides some details about the language.

| PROPERTY | EXAMPLE | DESCRIPTION |
| :--- | :--- | :--- |
| name | Russian | ISO language name |
| iso1 | ru | ISO 639-1 two-letter code of the language of translation. **Does not exist for some languages.** |
| iso3 | rur | ISO 639-3 three-letter code of the language of translation. |
| direction | ltr | "rtl" for a Rigth-To-Left language and "ltr" for a Left-To-Right language |

### name

Provides names of the translation in different languages.

| PROPERTY | EXAMPLE | DESCRIPTION |
| :--- | :--- | :--- |
| en | Translation of meanings of the Quran | Name of the translation in English |
| iso1/iso3 code of the native language | Перевод смыслов Корана. | Name of the translation in the native language |

### about

`about` section provides a description of the translation. It is like a text in the first few pages of a book.

| PROPERTY | EXAMPLE | DESCRIPTION |
| :--- | :--- | :--- |
| en | In November 2008, the translation-tafsir was published, the basis for which was written... | Description of the translation in English |
| iso1/iso3 code of the native language | В ноябре 2008 года вышел в свет перевод-тафсир, основой для написания которого... | Description of the translation in the native language |

### authors

This section provides detailed information about each author of the translation.

| PROPERTY | SUB-PROPERTY | EXAMPLE | DESCRIPTION |
| :--- | :--- | :--- | :--- |
| isAlive |  | false | Is the author alive? |
| name |  |  | Name of the author |
|  | en | Abu Adel | in English |
|  | iso1/iso3 code of the native language | Абу Адель | in the native language |
| bio |  |  | Some information about the author |
|  | en | Before Islam, he worked as an English translator. Accepted Islam in 1998 and began to study the Quran and Arabic... | in English |
|  | iso1/iso3 code of the native language | До Ислама работал переводчиком с английского. Принял Ислам в 1998 году и начал изучать Коран и арабский язык... | in the native language |
| contacts |  |  | Contacts of the author **\(optional\)** |
|  | type | email | Type of the contact, i.e. email, phone, etc. |
|  | value | example@example.com | The contact itself |

### reviewer / approver / dataPreparer

These three sections

* `reviewer` -- the person reviewed before publication
* `approver` -- the person responsible for publication
* `dataPreparer` -- the person responsible for converting the translation in digital format

are optional sections with the same content:

| PROPERTY | EXAMPLE | DESCRIPTION |
| :--- | :--- | :--- |
| name | Abu Adel | Name of the translation in English |
| email | example@example.com | Name of the translation in the native language |

### riwaya

This section contains only one value -- riwaya \(transmission\) on which the translation is based, i.e. Hafs, Warsh, Qaloon, etc. By default, it is assumed that the translation in based on Hafs riwaya. More information about riwaya, qira'at, and the difference between them can be found [here](https://en.wikipedia.org/wiki/Qira%27at).

### lastVersionSources

This section provides links to the sources where the latest version of the translation can be found. For example, some authors have websites where they update their translation. However our project keeps track of updates, so you can just simply sync with Digital Quran.

### copyrights

The section provides information about copyrights, like license, right-holder and special conditions of the license. Please read more about licenses here [Common Creatives](https://creativecommons.org/).

| PROPERTY | EXAMPLE | DESCRIPTION |
| :--- | :--- | :--- |
| license | Creative Commons Attribution 4.0 International License \([http://creativecommons.org/licenses/by/4.0/](http://creativecommons.org/licenses/by/4.0/)\) | License of the translation |
| specialConditions |  | Spectial conditions of the license **\(optional\)**. |
| rightholder | Abu Adel | Rightholder of the translation |

### issueContacts

List of persons and/or organizations that should be contacted in case of an error or a typo is found, or there is a suggestion about a translation, etc. The section consists of objects of the following structure:

| PROPERTY | EXAMPLE | DESCRIPTION |
| :--- | :--- | :--- |
| name | Abu Adel | Name of person or organization |
| type | email | Type of the contact: email, phone, etc. |
| value | example@example.com | The contact itself |

### File changes info: firstGeneratedAt, lastGeneratedAt, textUpdatedAt

For easier keep track of changes in the translation, three date-time fields are provided. Date-time values are provided in `YYYY-MM-DD HH:MM:SS` format.

| PROPERTY | EXAMPLE | DESCRIPTION |
| :--- | :--- | :--- |
| firstGeneratedAt | 2018-04-06 16:33:47 | Date-time of the first release of the translation **in Digital Quran** |
| lastGeneratedAt | 2019-04-06 16:33:47 | Date-time of the last release of the translation **in Digital Quran**. i.e. the last time the file was changed for any reasons: authors info, license info, translation text, etc.  |
| textUpdatedAt | 2018-04-06 16:33:47 | Date-time of the release where text of the translation was changed. i.e. the last time when **only translation** was modified. This field is important to separate updates of meta-data from updates from text of the translation was edited.  |

## Translation itself \(content\)

The text of the translation is placed in the `content` section. For both translation types \(by-ayah and word-by-word\) it has mostly the same structure described below.

{% hint style="warning" %}
Some translations can be incomplete. For that reason, we provide a number for each surah, ayah, and word. Use them instead of index.
{% endhint %}

### **surahs**

| PROPERTY | EXAMPLE | DESCRIPTION |
| :--- | :--- | :--- |
| number | 2 | The number of the surah, integer from 1 to 114 |
| ayahCount | 286 | Total number of ayahs in the surah |
| name | Корова | Translated \(to the language of the translation\) name of the surah. By default translated names are taken from Quran Academy. But it can be different, if the author wanted their own translation to be used. |
| nameTransliterated | Аль-Бакара | Transliterated \(to the language of the translation\) name of the surah. As for the translated name, by default values are taken from Quran Academy, but on demand of the author, it can be different. |
| ayahs |  | A list of ayahs of the surah. **Has a different structure in by-ayah and word-by-word translations** |

### ayahs

{% hint style="danger" %}
Some by-ayah translations and most of the word-by-word translations have merged translations, i.e. when two \(or more\) words translated as one. See [Russian word-by-word translation of 90:14 at Quran Academy](https://ru.quranacademy.org/quran/90) for an example. Check [Translation texts](translation-texts.md#merged-translations) for more details.
{% endhint %}

{% hint style="danger" %}
There are some differences in formatting translation text in JSON and XML. Although they are minor, it is important to know about them. See the [Translation texts](translation-texts.md#translation-comments-and-footnotes) section below for details.
{% endhint %}

{% tabs %}
{% tab title="BY-AYAH" %}
| PROPERTY | EXAMPLE | DESCRIPTION |
| :--- | :--- | :--- |
| number | 1 | Number of the ayah |
| text | Алиф лам мим. | Translation of the ayah |
{% endtab %}

{% tab title="WORD-BY-WORD" %}
| PROPERTY | SUB-PROPERTY | EXAMPLE | DESCRIPTION |
| :--- | :--- | :--- | :--- |
| number |  | 2 | Number of the ayah |
| words |  |  | A list of words of the ayah |
|  | number | 1 | Number of the word |
|  | text | Это | Translation of the word |
{% endtab %}
{% endtabs %}



