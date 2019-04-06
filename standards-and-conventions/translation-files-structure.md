---
description: Here you can find standards related to translation files
---

# Translation files structure

All translations available in two formats: XML and JSON in UTF-8 encoding. Data in a file is split into two parts: 1\) meta-data, like authors, licence, etc. -- called `meta` in files, 2\) translation itself -- called `content` in files.

## Meta-data \(meta\)

 Meta-data \(`meta` in files\) provides information about the translation, like authors, contacts, license, etc. All information is provided in, at least, two languages: language of the translation and English. Meta-data section has the following structure:

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

`about` section provides description of the translation. It is like a text in the first few pages of a book.

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

This sections contains only one value -- riwaya \(transmission\) on which the translation is based, i.e. Hafs, Warsh, Qaloon, etc. By default it is assumed that the translation in based on Hafs riwaya.

### lastVersionSources

This sections provides links to the sources where the latest version of the translation can be found. For example, some authors have their own web-sites where they update their translation. However our project keeps track of updates, so you can just simply sync with Digital Quran.

### copyrights

The section provides information about copyrights, like license, right-holder and special conditions of the license.

| PROPERTY | EXAMPLE | DESCRIPTION |
| :--- | :--- | :--- |
| license | Creative Commons Attribution 4.0 International License \([http://creativecommons.org/licenses/by/4.0/](http://creativecommons.org/licenses/by/4.0/)\) | License of the translation |
| specialConditions |  | Spectial conditions of the license **\(optional\)**. |
| rightholder | Abu Adel | Rightholder of the translation |

### issueContacts

List of persons and/or organizations that should be contacted in case if a error or a typo is found, or there is suggestion about a translation, etc. The sections consists of object of the following structure:

| PROPERTY | EXAMPLE | DESCRIPTION |
| :--- | :--- | :--- |
| name | Abu Adel | Name of person or organization |
| type | email | Type of the contact: email, phone, etc. |
| value | example@example.com | The contact itself |

### File changes info: firstGeneratedAt, lastGeneratedAt, textUpdatedAt

For easier keep track of changes in the translation, three date-time fields are provided.

| PROPERTY | EXAMPLE | DESCRIPTION |
| :--- | :--- | :--- |
| firstGeneratedAt |  | Date-time of the first release of the translation **in Digital Quran** |
| lastGeneratedAt |  | Date-time of the last release of the translation **in Digital Quran**. i.e. the last time the file was changed for any reasons: authors info, license info, translation text, etc.  |
| textUpdatedAt |  | Date-time of the release where text of the translation was changed. i.e. the last time when only translation was modified. This field is important to separate updates of meta-data from updates from text of the translation was edited.  |

## Translation itself \(content\)

TODO:

