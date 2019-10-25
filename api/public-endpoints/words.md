# Words

## List words of a specific surah

### URL

```text
/words
```

### Parameters

| Name | Type | Description | Required | Default |
| :--- | :--- | :--- | :--- | :--- |
| surah_number | integer | The number of a surah. | Yes | None |
| include_arabic_text | boolean | Add text in arabic? | No | false |
| language | string | The code of a language. | No | None |
| start_ayah_number | integer | The number of the start ayah (if you want to get words of a range of ayahs). | No | None |
| end_ayah_number | integer | The number of the end ayah (if you want to get words of a range of ayahs). | No | None |

Example:

```json
{
    "surah_number": 1,
    "include_arabic_text": true,
    "language": "ru"
}
```

### Response

```json
{
    "data": [
        {
            "surah_number": 1,
            "number": 1,
            "words": [
                {
                    "position": 1,
                    "arabic_text": "بِسْمِ",
                    "translation": "С именем"
                },
                {
                    "position": 2,
                    "arabic_text": "ٱللَّهِ",
                    "translation": "Аллаха,"
                },
                {
                    "position": 3,
                    "arabic_text": "ٱلرَّحْمَٰنِ",
                    "translation": "Милостивого,"
                },
                {
                    "position": 4,
                    "arabic_text": "ٱلرَّحِيمِ",
                    "translation": "Милосердного!"
                }
            ]
        },
        {
            "surah_number": 1,
            "number": 2,
            "words": [
                {
                    "position": 1,
                    "arabic_text": "ٱلْحَمْدُ",
                    "translation": "Хвала"
                },
                {
                    "position": 2,
                    "arabic_text": "لِلَّهِ",
                    "translation": "Аллаху,"
                },
                {
                    "position": 3,
                    "arabic_text": "رَبِّ",
                    "translation": "Господу"
                },
                {
                    "position": 4,
                    "arabic_text": "ٱلْعَٰلَمِينَ",
                    "translation": "миров,"
                }
            ]
        }
    ]
}
```
