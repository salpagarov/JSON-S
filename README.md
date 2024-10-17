# JSONS

Спецификация JSON допускает перезапись ключей. Это дает нам возможность сначала вписать мета-данные ключей – комментарии, формат, что угодно! – перед самими данными. Таким образом, мы находим способ расширить формат, сохраняя совместимость.

## Пример 1

~~~json
{
    "user": "Пользователи",
    "user": [
        {
            "name" : "Имя пользователя",
            "password" : "Пароль",
            "groups" : "Группы пользователя",
            "name" : "root",
            "password" : "p@ssw0rd",
            "groups" : [
                "system", "security", "staff"
            ]
        }
    ],
    "group": "Группы",
    "group": [
        "system", "security", "staff"
    ]
}
~~~

## Пример 2

~~~json
{
    "user": "Пользователи",
    "group": "Группы",
    "user" : {
            "name" : "Имя пользователя",
            "password" : "Пароль",
            "groups" : "Группы пользователя"
    }
    "user": [
        {
            "name" : "root",
            "password" : "p@ssw0rd",
            "groups" : [
                "system", "security", "staff"
            ]
        }
    ]
    "group": [
        "system", "security", "staff"
    ]
}
~~~
