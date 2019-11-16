---
description: 'Here you can find conventions about naming terms, fields, attributes, etc.'
---

# Naming convention

## Arabic / Quranic terms

For naming Arabic / Quranic terms transliteration of singular form is used. A transliteration must not contain non-ASCII symbols \(like ā\) and apostrophe\(like in Qur'an\). A plural form must be formed from singular form + "s", instead of transliteration of plural form in Arabic. For example, we use "surahs" \(surah + s\) instead of "suwar" \(transliteration from Arabic for plural form\). Here is a list of most common terms and their names in Digital Quran:

| Singular | Plural | Details |
| :--- | :--- | :--- |
| Quran |  |  |
| Surah | Surahs | A chapter of the Quran |
| Ayah | Ayahs | A verse of a chapter |
| Riwaya |  | Transmission of the Quran |

## Naming

* Identifiers use only ASCII letters and digits and the first symbol must be a letter. 
* **lowerCamelCase** is used for naming elements, objects, attributes, etc.
* Names of logical \(true/false\) fields start with "is" prefix, like "isAlive".
* Array fields, i.e. fields accepting many values are in plural form, like "authors". In JSON format, a value of such a fields is an array \(mostly array of objects\). In XML format, such an element contains many elements with the same name, but in singular form. Here is an example of an array field:

{% tabs %}
{% tab title="JSON" %}
{% code title="JSON" %}
```javascript
contacts: [
    {
        "type": "email",
        "value": "example.com"
    },
    {
        "type": "phone",
        "value": "+123456789"
    }
]
```
{% endcode %}
{% endtab %}

{% tab title="XML" %}
{% code title="XML" %}
```markup
<contacts>
    <contact>
        <type>email</type>
        <value>example.com</value>
    </contact>
    <contact>
        <type>phone</type>
        <value>+123456789</value>
    </contact>
</contacts>
```
{% endcode %}
{% endtab %}
{% endtabs %}

* In XML files using an element is preferred over an attribute. With the exception of a few elements, there are no attributes in XML documents. Instead, nested elements are used. 

