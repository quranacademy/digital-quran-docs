---
description: >-
  Here are examples of translation files to give a better understanding of the
  structure
---

# Translation files: examples

Here you can find examples of [by-ayah translation](translation-files-examples.md#by-ayah-translation-example) and [word-by-word translation](translation-files-examples.md#word-by-word-translation-example) of both JSON and XML formats.

{% hint style="warning" %}
**NOTE.** Information in examples is not reliable! Please, do not treat it as real information. Mostly it is made up to just give you an idea of how values look like. 
{% endhint %}

## By-ayah translation example

{% tabs %}
{% tab title="JSON" %}
{% code title="By-ayah translation exmaple" %}
```javascript
{
    "translation": {
        "meta": {
            "name": {
                "ru": "Эльмир Кулиев",
                "en": "Elmir Kuliyev"
            },
            "language": {
                "name": "Russian",
                "iso1": "ru",
                "iso3": "rus",
                "direction": "ltr"
            },
            "about": {
                "ru": "В 2002 году вышел перевод смыслов Эльмира Кулиева. Этот перевод отличается от остальных современных переводов тем, что Кулиев не имеет необходимого профессионального образования, и не является маститым учёным арабистом и востоковедом, а также и богословом. Тем не менее обсуждение перевода проводилось совместно с известными саудовскими корановедами и под руководством заведующего отделом Комплекса по изданию Корана в Саудовской Аравии Али Насиром аль-Факихи Как и Порохова, Кулиев, будучи сам мусульманином, сделал попытку взглянуть на текст исходя из традиции толкования ранних комментаторов. Перевод был одобрен и учёными и мусульманским духовенством. Светские учёные отмечают, как достоинства перевода, выразившиеся в попытке сделать точное соответствие арабского текста русскому, так и недостатки проявившиеся в замене исходных слов и речевых оборотов своими синонимами и фразами, что превращало перевод в пересказ.",
                "en": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
            },
            "authors": [
                {
                    "name": {
                        "ru": "Эльмир Кулиев",
                        "en": "Elmir Kuliev",
                    },
                    "bio": {
                        "ru": "Эльмир Кулиев — азербайджанский светский ученый-религиовед, автор перевода Священного Корана на русский язык, специалист в области мусульманского богословия, истории и культуры исламского региона. Автор книг «Пророчества о приближении конца света», «На пути к Корану», «Коран и глобализация», «Сладость веры», соавтор книг «Уроки благословенного месяца», «Исламоведение» (пособие для преподавателей), «Корановедение» (пособие для вузов). В последние годы Эльмир Кулиев занимается исследовательской и преподавательской деятельностью в своем родном городе, участвует в международных конференциях и выступает с лекциями в разных странах, ведет персональный сайт www.guliyev.org и страницу в социальной сети Facebook www.facebook.com/guliyev.org.",
                        "en": "Elmir Guliyev is an Azerbaijani secular religious scholar, author of the translation of the Holy Quran into Russian, an expert in Muslim theology, history and culture of the Islamic region. Author of the books “Prophecies about the end of the world”, “Towards the Qur'an”, “The Quran and Globalization”, “Sweetness of Faith”, co-author of the books “Lessons of the blessed month”, “Islamic studies” (teacher’s manual), “Koran studies” (manual for universities). In recent years, Elmir Guliyev is engaged in research and teaching activities in his hometown, participates in international conferences and lectures in different countries, maintains a personal website www.guliyev.org and a page on the social network Facebook www.facebook.com/guliyev.org."
                    },
                    "contacts": [
                        {
                            "type": "email",
                            "value": "kuliev@mail.ru"
                        },
                        {
                            "type": "website",
                            "value": "www.guliyev.org"
                        },
                        {
                            "type": "facebook",
                            "value": "www.facebook.com/guliyev"
                        }
                    ],
                    "isAlive": "true"
                }
            ],
            "riwaya": "Hafs",
            "copyrights": {
                "license": "Creative Commons Attribution 4.0 International License (http://creativecommons.org/licenses/by/4.0/)",
                "rightholder": "Elmir Kuliev"
            },
            "issueContacts": {
                "contact": [
                    {
                        "name": "Elmir Kuliev",
                        "type": "email",
                        "value": "kuliev@mail.ru"
                    },
                    {
                        "name": "Quran Academy Support",
                        "type": "email",
                        "value": "digitalquran@quranacademy.org"
                    }
                ]
            },
            "firstGeneratedAt": "2019-04-05 06:01:53",
            "lastGeneratedAt": "2019-04-05 06:01:53",
            "textUpdatedAt": "2018-11-13 05:44:32"
        },
        "content": {
            "surahs": [
                {
                    "number": 1,
                    "name": "Открывающая Коран",
                    "nameTransliterated": "Аль-Фатиха",
                    "ayahs": [
                        {
                            "number": 1,
                            "text": "С именем Аллаха Милостивого, Милосердного!"
                        },
                        {
                            "number": 2,
                            "text": "(Вся) хвала – (лишь одному) Аллаху, Господу миров [Господу всех творений],"
                        }
                    ]
                }
            ]
        }
    }
}
```
{% endcode %}
{% endtab %}

{% tab title="XML" %}
```markup
<?xml version="1.0" encoding="utf-8"?>
<translation>
    <meta>
        <name>
            <ru>Эльмир Кулиев</ru>
            <en>Elmir Kuliyev</en>
        </name>
        <language>
            <name>Russian</name>
            <iso1>ru</iso1>
            <iso3>rus</iso3>
            <direction>ltr</direction>
        </language>
        <about>
            <ru>В 2002 году вышел перевод смыслов Эльмира Кулиева. Этот перевод отличается от остальных современных переводов тем, что Кулиев не имеет необходимого профессионального образования, и не является маститым учёным арабистом и востоковедом, а также и богословом. Тем не менее обсуждение перевода проводилось совместно с известными саудовскими корановедами и под руководством заведующего отделом Комплекса по изданию Корана в Саудовской Аравии Али Насиром аль-Факихи Как и Порохова, Кулиев, будучи сам мусульманином, сделал попытку взглянуть на текст исходя из традиции толкования ранних комментаторов. Перевод был одобрен и учёными и мусульманским духовенством. Светские учёные отмечают, как достоинства перевода, выразившиеся в попытке сделать точное соответствие арабского текста русскому, так и недостатки проявившиеся в замене исходных слов и речевых оборотов своими синонимами и фразами, что превращало перевод в пересказ.</ru>
            <en>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</en>
        </about>
        <authors>
            <author>
                <name>
                    <ru>Эльмир Кулиев</ru>
                    <en>Elmir Kuliev</en>
                </name>
                <bio>
                    <ru>Эльмир Кулиев — азербайджанский светский ученый-религиовед, автор перевода Священного Корана на русский язык, специалист в области мусульманского богословия, истории и культуры исламского региона. Автор книг «Пророчества о приближении конца света», «На пути к Корану», «Коран и глобализация», «Сладость веры», соавтор книг «Уроки благословенного месяца», «Исламоведение» (пособие для преподавателей), «Корановедение» (пособие для вузов). В последние годы Эльмир Кулиев занимается исследовательской и преподавательской деятельностью в своем родном городе, участвует в международных конференциях и выступает с лекциями в разных странах, ведет персональный сайт www.guliyev.org и страницу в социальной сети Facebook www.facebook.com/guliyev.org.</ru>
                    <en>Elmir Guliyev is an Azerbaijani secular religious scholar, author of the translation of the Holy Quran into Russian, an expert in Muslim theology, history and culture of the Islamic region. Author of the books “Prophecies about the end of the world”, “Towards the Qur'an”, “The Quran and Globalization”, “Sweetness of Faith”, co-author of the books “Lessons of the blessed month”, “Islamic studies” (teacher’s manual), “Koran studies” (manual for universities). In recent years, Elmir Guliyev is engaged in research and teaching activities in his hometown, participates in international conferences and lectures in different countries, maintains a personal website www.guliyev.org and a page on the social network Facebook www.facebook.com/guliyev.org.</en>
                </bio>
                <contacts>
                    <contact>
                        <type>email</type>
                        <value>kuliev@mail.ru</value>
                    </contact>
                    <contact>
                        <type>website</type>
                        <value>www.guliyev.org</value>
                    </contact>
                    <contact>
                        <type>facebook</type>
                        <value>www.facebook.com/guliyev</value>
                    </contact>
                </contacts>
                <isAlive>true</isAlive>
            </author>
        </authors>
        <riwaya>Hafs</riwaya>
        <copyrights>
            <license>Creative Commons Attribution 4.0 International License (http://creativecommons.org/licenses/by/4.0/)</license>
            <rightholder>Elmir Kuliev</rightholder>
        </copyrights>
        <issueContacts>
            <contact>
                <contact>
                    <name>Elmir Kuliev</name>
                    <type>email</type>
                    <value>kuliev@mail.ru</value>
                </contact>
                <contact>
                    <name>Quran Academy Support</name>
                    <type>email</type>
                    <value>digitalquran@quranacademy.org</value>
                </contact>
            </contact>
        </issueContacts>
        <firstGeneratedAt>2019-04-05 06:01:53</firstGeneratedAt>
        <lastGeneratedAt>2019-04-05 06:01:53</lastGeneratedAt>
        <textUpdatedAt>2018-11-13 05:44:32</textUpdatedAt>
    </meta>
    <content>
        <surahs>
            <surah number="1" ayahCount="7">
                <name>Открывающая Коран</name>
                <nameTransliterated>Аль-Фатиха</nameTransliterated>
                <ayahs>
                    <ayah number="1">Во имя Аллаха, Милостивого, Милосердного!</ayah>
                    <ayah number="2">Хвала Аллаху, Господу миров,</ayah>
                    <ayah number="3">Милостивому, Милосердному,</ayah>
                    <ayah number="4">Властелину Дня воздаяния!</ayah>
                    <ayah number="5">Тебе одному мы поклоняемся и Тебя одного молим о помощи.</ayah>
                    <ayah number="6">Веди нас прямым путем,</ayah>
                    <ayah number="7">путем тех, кого Ты облагодетельствовал, не тех, на кого пал гнев, и не заблудших.</ayah>
                </ayahs>
            </surah>
        </surahs>
    </content>
</translation>
```
{% endtab %}
{% endtabs %}



## Word-by-word translation example

{% tabs %}
{% tab title="JSON" %}
{% code title="word-by-word translation exmaple" %}
```javascript
{
    "translation": {
        "meta": {
            "name": {
                "ru": "Абу Адель",
                "en": "Abu Adel"
            },
            "language": {
                "name": "Russian",
                "iso1": "ru",
                "iso3": "rus",
                "direction": "ltr"
            },
            "about": {
                "ru": "В ноябре 2008 года вышел в свет перевод-тафсир, основой для написания которого послужил «ат-Тафсир аль-муяссар» (Облегчённое толкование) составленный группой преподавателей толкования Корана под руководством Абдуллаха ибн Абд аль-Мухсина. В нём также использованы толкования аш-Шаукани, Ибн аль-Усеймина, Абу Бакра аль-Джазаири, аль-Багави, Ибн аль-Джаузи и других исламских богословов. Перевод, выполненный Абу Аделем, представляет собой совмещение перевода с толкованием."
                "en": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
            },
            "authors": [
                {
                    "name": {
                        "ru": "Абу Адель",
                        "en": "Abu Adel",
                    },
                    "bio": {
                        "ru": "Родился и живёт в Татарстане. До Ислама работал переводчиком с английского.Принял Ислам в 1998 году и начал изучать Коран и арабский язык.Ещё до принятия Ислама дважды прочитал перевод Крачковского. Известен по книге \"Курс арабского языка. Вводная, первая и вторая части\". (400 страниц)Автор брошюр: \"Истина и смысл жизни\", \"Аллах Велик!\", \"Я люблю Аллаха\", \"Жизнь в Вечности\".Личное: женат, имеет пятеро детей.",
                        "en": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
                    },
                    "contacts": [
                        {
                            "type": "email",
                            "value": "abuadel@example.com"
                        }
                    ],
                    "isAlive": "true"
                }
            ],
            "riwaya": "Hafs",
            "copyrights": {
                "license": "Creative Commons Attribution 4.0 International License (http://creativecommons.org/licenses/by/4.0/)",
                "rightholder": "Abu Adel"
            },
            "issueContacts": {
                "contact": [
                    {
                        "name": "Quran Academy Support",
                        "type": "email",
                        "value": "digitalquran@quranacademy.org"
                    }
                ]
            },
            "firstGeneratedAt": "2019-04-05 06:01:53",
            "lastGeneratedAt": "2019-04-05 06:01:53",
            "textUpdatedAt": "2018-11-13 05:44:32"
        },
        "content": {
            "surahs": [
                {
                    "number": 1,
                    "name": "Открывающая Коран",
                    "nameTransliterated": "Аль-Фатиха",
                    "ayahs": [
                        {
                            "number": 1,
                            "words": [
                                {
                                    "number": 1,
                                    "text": "С именем"
                                },
                                {
                                    "number": 2,
                                    "text": "Аллаха,"
                                },
                                {
                                    "number": 3,
                                    "text": "Милостивого,"
                                },
                                {
                                    "number": 4,
                                    "text": "Милосердного!"
                                }
                            ]
                        },
                        {
                            "number": 2,
                            "words": [
                                {
                                    "number": 1,
                                    "text": "Хвала"
                                }
                                {
                                    "number": 2,
                                    "text": "Аллаху,"
                                }
                                {
                                    "number": 3,
                                    "text": "Господу"
                                }
                                {
                                    "number": 4,
                                    "text": "миров,"
                                }
                            ]
                        },
                        {
                            "number": 3,
                            "words": [
                                {
                                    "number": 1,
                                    "text": "Милостивому,"
                                }
                                {
                                    "number": 2,
                                    "text": "Милосердному,"
                                }
                            ]
                        },
                        {
                            "number": 4,
                            "words": [
                                {
                                    "number": 1,
                                    "text": "Владыке"
                                }
                                {
                                    "number": 2,
                                    "text": "Дня"
                                }
                                {
                                    "number": 3,
                                    "text": "Воздаяния!"
                                }
                            ]
                        },
                        {
                            "number": 5,
                            "words": [
                                {
                                    "number": 1,
                                    "text": "(Только) Тебе"
                                }
                                {
                                    "number": 2,
                                    "text": "мы поклоняемся"
                                }
                                {
                                    "number": 3,
                                    "text": "и (только) у Тебя"
                                }
                                {
                                    "number": 4,
                                    "text": "просим помощи!"
                                }
                            ]
                        },
                        {
                            "number": 6,
                            "words": [
                                {
                                    "number": 1,
                                    "text": "Веди нас"
                                }
                                {
                                    "number": 2,
                                    "text": "Путём"
                                }
                                {
                                    "number": 3,
                                    "text": "Прямым,"
                                }
                            ]
                        },
                        {
                            "number": 7,
                            "words": [
                                {
                                    "number": 1,
                                    "text": "Путём"
                                }
                                {
                                    "number": 2,
                                    "text": "тех"
                                }
                                {
                                    "number": 3,
                                    "text": "(Ты) благом одарил"
                                }
                                {
                                    "number": 4,
                                    "text": "которых (досл. на них)"
                                }
                                {
                                    "number": 5,
                                    "text": "(но) не (путём)"
                                }
                                {
                                    "number": 6,
                                    "text": "(тех, которые) под гневом (Твоим),"
                                }
                                {
                                    "number": 7,
                                    "text": "на них"
                                }
                                {
                                    "number": 8,
                                    "text": "и не (путём)"
                                }
                                {
                                    "number": 9,
                                    "text": "заблудших."
                                }
                            ]
                        }
                    ]
                }
            ]
        }
    }
}
```
{% endcode %}
{% endtab %}

{% tab title="XML" %}
{% code title="word-by-word translation exmaple" %}
```markup
<?xml version="1.0" encoding="utf-8"?>
<translation>
    <meta>
        <name>
            <ru>Абу Адель</ru>
            <en>Abu Adel</en>
        </name>
        <language>
            <name>Russian</name>
            <iso1>ru</iso1>
            <iso3>rus</iso3>
            <direction>ltr</direction>
        </language>
        <about>
            <ru>В ноябре 2008 года вышел в свет перевод-тафсир, основой для написания которого послужил «ат-Тафсир аль-муяссар» (Облегчённое толкование) составленный группой преподавателей толкования Корана под руководством Абдуллаха ибн Абд аль-Мухсина. В нём также использованы толкования аш-Шаукани, Ибн аль-Усеймина, Абу Бакра аль-Джазаири, аль-Багави, Ибн аль-Джаузи и других исламских богословов. Перевод, выполненный Абу Аделем, представляет собой совмещение перевода с толкованием.</ru>
            <en>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</en>
        </about>
        <authors>
            <author>
                <name>
                    <ru>Абу Адель</ru>
                    <en>Abu Adel</en>
                </name>
                <bio>
                    <ru>Родился и живёт в Татарстане. До Ислама работал переводчиком с английского.Принял Ислам в 1998 году и начал изучать Коран и арабский язык.Ещё до принятия Ислама дважды прочитал перевод Крачковского. Известен по книге "Курс арабского языка. Вводная, первая и вторая части". (400 страниц)Автор брошюр: "Истина и смысл жизни", "Аллах Велик!", "Я люблю Аллаха", "Жизнь в Вечности".Личное: женат, имеет пятеро детей.</ru>
                    <en>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</en>
                </bio>
                <contacts>
                    <contact>
                        <type>email</type>
                        <value>abuadel@example.com</value>
                    </contact>
                </contacts>
                <isAlive>true</isAlive>
            </author>
        </authors>
        <riwaya>Hafs</riwaya>
        <copyrights>
            <license>Creative Commons Attribution 4.0 International License (http://creativecommons.org/licenses/by/4.0/)</license>
            <rightholder>Abu Adel</rightholder>
        </copyrights>
        <issueContacts>
            <contact>
                <contact>
                    <name>Quran Academy Support</name>
                    <type>email</type>
                    <value>digitalquran@quranacademy.org</value>
                </contact>
            </contact>
        </issueContacts>
        <firstGeneratedAt>2019-04-05 06:01:53</firstGeneratedAt>
        <lastGeneratedAt>2019-04-05 06:01:53</lastGeneratedAt>
        <textUpdatedAt>2018-11-13 05:44:32</textUpdatedAt>
    </meta>
    <content>
        <surahs>
            <surah number="1" ayahCount="7">
                <name>Открывающая Коран</name>
                <nameTransliterated>Аль-Фатиха</nameTransliterated>
                <ayahs>
                    <ayah number="1">
                        <words>
                            <word number="1">С именем</word>
                            <word number="2">Аллаха,</word>
                            <word number="3">Милостивого,</word>
                            <word number="4">Милосердного!</word>
                        </words>
                    </ayah>
                    <ayah number="2">
                        <words>
                            <word number="1">Хвала</word>
                            <word number="2">Аллаху,</word>
                            <word number="3">Господу</word>
                            <word number="4">миров,</word>
                        </words>
                    </ayah>
                    <ayah number="3">
                        <words>
                            <word number="1">Милостивому,</word>
                            <word number="2">Милосердному,</word>
                        </words>
                    </ayah>
                    <ayah number="4">
                        <words>
                            <word number="1">Владыке</word>
                            <word number="2">Дня</word>
                            <word number="3">Воздаяния!</word>
                        </words>
                    </ayah>
                    <ayah number="5">
                        <words>
                            <word number="1">(Только) Тебе</word>
                            <word number="2">мы поклоняемся</word>
                            <word number="3">и (только) у Тебя</word>
                            <word number="4">просим помощи!</word>
                        </words>
                    </ayah>
                    <ayah number="6">
                        <words>
                            <word number="1">Веди нас</word>
                            <word number="2">Путём</word>
                            <word number="3">Прямым,</word>
                        </words>
                    </ayah>
                    <ayah number="7">
                        <words>
                            <word number="1">Путём</word>
                            <word number="2">тех</word>
                            <word number="3">(Ты) благом одарил</word>
                            <word number="4">которых (досл. на них)</word>
                            <word number="5">(но) не (путём)</word>
                            <word number="6">(тех, которые) под гневом (Твоим),</word>
                            <word number="7">на них</word>
                            <word number="8">и не (путём)</word>
                            <word number="9">заблудших.</word>
                        </words>
                    </ayah>
                </ayahs>
            </surah>
        </surahs>
    </content>
</translation>
```
{% endcode %}
{% endtab %}
{% endtabs %}



