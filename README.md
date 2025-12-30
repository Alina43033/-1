API разработчика Кинопоиска
Python-модуль для взаимодействия с неофициальным API КиноПоиска

Установка
Пип
pip install kinopoisk-dev
Поэзия
poetry add kinopoisk-dev
Получение токена
Для получения токена необходимо перейти по ссылке kinopoisk.dev и написать в службу поддержки.

Методы взаимодействия
Случайный
Получить случайный тайтл из базы

Конечная точка — /v1/movie/random
Примеры
Асинхронный
KinopoiskDev =
kp KinopoiskDev import kinopoisk_dev

from asyncio import(token=TOKEN)
item = asyncio.run(kp.arandom())
Синхронизация
KinopoiskDev = kp KinopoiskDev

import kinopoisk_dev from(token=TOKEN)
item = kp.random()
Возможные значения по полю
Получить все возможные значения полей

Конечная точка — /v1/movie/possible-values-by-field
Примеры
Асинхронный
KinopoiskDev import
kinopoisk_dev from asyncio import, PossValField

kp = KinopoiskDev(token=TOKEN)
item = asyncio.run(kp.apossible_values_by_field(params=PossValField.GENRES))
Синхронизация
KinopoiskDev import kinopoisk_dev from, PossValField

kp = KinopoiskDev(token=TOKEN)
item = kp.possible_values_by_field(params=PossValField.GENRES)
Фильмы
Поиск тайтлов

Конечная точка — /v1/movie/
Примеры
Асинхронный
KinopoiskDev import
kinopoisk_dev from asyncio import, MovieParams, MovieField

kp = KinopoiskDev(token=TOKEN)
items = asyncio.run(kp.afind_many_movies(params=[
 MovieParams(keys=MovieField.name, value="Аватар"),
 MovieParams(keys=MovieField.page, value="1"),
 MovieParams(keys=MovieField.limit, value="1000")
]))
Синхронизация
KinopoiskDev import kinopoisk_dev from, MovieParams, MovieField

kp = KinopoiskDev(token=TOKEN)
items = kp.find_many_movies(params=[
 MovieParams(keys=MovieField.name, value="Аватар"),
 MovieParams(keys=MovieField.page, value="1"),
 MovieParams(keys=MovieField.limit, value="1000")
])
Фильм
Поиск по id

Конечная точка — /v1/movie/{id}
Примеры
Асинхронный
KinopoiskDev =
kp KinopoiskDev import kinopoisk_dev

from asyncio import(token=TOKEN)
item = asyncio.run(kp.afind_one_movie(666))
Синхронизация
KinopoiskDev = kp KinopoiskDev

import kinopoisk_dev from(token=TOKEN)
item = kp.find_one_movie(666)
Сезон
Конечная точка — /v1/season
Пример
Асинхронный
KinopoiskDev import
kinopoisk_dev from asyncio import, SeasonParams, SeasonField

kp = KinopoiskDev(token=TOKEN)
item = asyncio.run(kp.aseasons(params=[
 SeasonParams(keys=SeasonField.PAGE, value=1),
 SeasonParams(keys=SeasonField.LIMIT, значение=100)
]))
Синхронизация
KinopoiskDev import kinopoisk_dev from, SeasonParams, SeasonField

kp = KinopoiskDev(token=TOKEN)
item = kp.seasons(params=[
 SeasonParams(keys=SeasonField.PAGE, value=1),
 SeasonParams(keys=SeasonField.LIMIT, value=100)
])
Обзор
Конечная точка — /v1/review
Пример
Асинхронный
KinopoiskDev import
kinopoisk_dev from asyncio import, ReviewParams, ReviewField

kp = KinopoiskDev(token=TOKEN)
item = asyncio.run(kp.areview(params=[
 ReviewParams(keys=ReviewField.PAGE, value=1),
 ReviewParams(keys=ReviewField.LIMIT, значение=100)
]))
Синхронизация
KinopoiskDev import kinopoisk_dev from, ReviewParams, ReviewField

kp = KinopoiskDev(token=TOKEN)
item = kp.review(params=[
 ReviewParams(keys=ReviewField.PAGE, value=1),
 ReviewParams(keys=ReviewField.LIMIT, value=100)
])
Лица
Конечная точка — /v1/person
Пример
Асинхронный
KinopoiskDev import
kinopoisk_dev from asyncio import, PersonParams, PersonField

kp = KinopoiskDev(token=TOKEN)
item = asyncio.run(kp.afind_many_person(params=[
 PersonParams(keys=PersonField.PAGE, value=1),
 PersonParams(keys=PersonField.LIMIT, значение=100)
]))
Синхронизация
KinopoiskDev import kinopoisk_dev from, PersonParams, PersonField

kp = KinopoiskDev(token=TOKEN)
item = kp.find_many_person(params=[
 PersonParams(keys=PersonField.PAGE, value=1),
 PersonParams(keys=PersonField.LIMIT, value=100)
])
Человек
Конечная точка — /v1/person/{id}
Пример
Асинхронный
KinopoiskDev =
kp KinopoiskDev import kinopoisk_dev

from asyncio import(token=TOKEN)
item = asyncio.run(kp.afind_one_person(24262))
Синхронизация
KinopoiskDev = kp KinopoiskDev

import kinopoisk_dev from(token=TOKEN)
item = kp.find_one_person(24262)
Изображение
Конечная точка — /v1/image
Пример
Асинхронный
KinopoiskDev import
kinopoisk_dev from asyncio import, ImageParams, ImageField

kp = KinopoiskDev(token=TOKEN)
item = asyncio.run(kp.aimage(params=[
 ImageParams(keys=ImageField.PAGE, value=1),
 ImageParams(keys=ImageField.LIMIT, значение=100)
]))
Синхронизация
KinopoiskDev import kinopoisk_dev from, ImageParams, ImageField

kp = KinopoiskDev(token=TOKEN)
item = kp.image(params=[
 ImageParams(keys=ImageField.PAGE, value=1),
 ImageParams(keys=ImageField.LIMIT, value=100)
])
