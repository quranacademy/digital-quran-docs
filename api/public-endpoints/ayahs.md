# Ayahs

## List ayahs of a specific surah

### URL

```text
GET /ayahs
```

### Parameters

| Name | Type | Description | Required | Default |
| :--- | :--- | :--- | :--- | :--- |
| surah\_number | integer | The number of a surah. | Yes | None |
| include\_arabic\_text | boolean | Add text in arabic? | No | false |
| translations | string\[\] | Codes of translations. | No | None |
| start\_ayah\_number | integer | The number of the start ayah \(if you want to get a range of ayahs\). | No | None |
| end\_ayah\_number | integer | The number of the end ayah \(if you want to get a range of ayahs\). | No | None |

Example:

```javascript
{
    "surah_number": 1,
    "include_arabic_text": true,
    "translations": ["en-saheeh-international", "ru-abu-adel"]
}
```

### Response

```javascript
{
    "data": [
        {
            "surah_number": 1,
            "number": 1,
            "juz_number": 1,
            "hizb_number": 1,
            "rub_number": 1,
            "sajdah": false,
            "word_count": 4,
            "arabic_text": "بِسْمِ اللَّهِ الرَّحْمَٰنِ الرَّحِيمِ",
            "translations": {
                "en-saheeh-international": "In the name of Allah, the Entirely Merciful, the Especially Merciful.",
                "ru-abu-adel": "С именем Аллаха Милостивого, Милосердного!"
            }
        },
        {
            "surah_number": 1,
            "number": 2,
            "juz_number": 1,
            "hizb_number": 1,
            "rub_number": 1,
            "sajdah": false,
            "word_count": 4,
            "arabic_text": "الْحَمْدُ لِلَّهِ رَبِّ الْعَالَمِينَ",
            "translations": {
                "en-saheeh-international": "(All) praise is (due) to Allah, Lord of the worlds -",
                "ru-abu-adel": "(Вся) хвала – (лишь одному) Аллаху, Господу миров [Господу всех творений],\n"
            }
        }
    ]
}
```

