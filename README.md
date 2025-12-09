# Проект по курсу «Цифровая архивация современности»

В этом репозитории собрана [коллекция сайтов](https://drive.google.com/drive/folders/1qPiALfm-brgv8m8pdS4npaDrIcVmK-SS?usp=sharing) на лингвистическую тематику. Сайты архивировались с помощью [wpull](https://github.com/ArchiveTeam/wpull) и оценивались с помощью ресурса [ArchiveReady](https://archiveready.com/), результаты были проанализированы с помощью сервиса [Replay Webpage](https://replayweb.page/) и утилиты [metawarc](https://github.com/datacoon/metawarc). В репозитории представлен подробный анализ архивации каждого из перечисленных сайтов.

## Описание коллекции

Коллекция состоит из полезных "сборников" со справочной лингвистической информацией о языках мира: типологические концепты, универсалии и рары, языковые карты, письменности мира. Для архивации были выбраны следующие сайты:

 1. [Rara & Universals Archive](https://typo.uni-konstanz.de/rara/rara-intro/)
 2. [Lingvarium project](http://lingvarium.org/index.shtml)
 3. [The WALS](https://wals.info/chapter)
 4. [Omniglot](https://www.omniglot.com/conscripts/natlangs.htm)

Более подробное описание каждого из ресурсов доступно в соответствующих README-документах.

## Методы

При сборе и обработке коллекции применялись следующие инструменты:

 1. Библиотека **wpull**, запущенная через скрипт для массового обкачивания ряда сайтов, с настроенными параметрами: расширения необходимых файлов, уровень рекурсивного скачивания и др.
 2. Пакет **metawarc**, позволяющий анализировать результат архивирования и создавать вспомогательные файлы: базы данных с составом архива, статистика, ошибки и т.д.
 4. Сайт **ArchiveReady**, высчитывающий рейтинг архивируемости сайта и выдающий сводку возможных трудностей по отдельным показателям
 5. Сайт **Replay Webpage**, позволяющий загрузить файл с архивом и проверить успешность скачивания

## Содержание репозитория

Файлы для каждого сайта помещены в одноимённую папку. Для каждого сайта доступны README с подробным описанием страницы и результата архивации, а также следующие файлы:

1. Изображения с сайтов ArchiveReady и Replay Webpage (в формате png)
2. **meta.jsonl** – метаданные архива, собранные с помощью **metawarc**
3. **metadata_errors.txt** – ошибки, возникшие в ходе сбора метаданных
4. **metawarc.db** – база данных, составленная автоматически на основе метаданных

## Контакты

Проект выполнен [Елизаветой Копыловой](https://github.com/kopyloveta).

## Условия использования

<p xmlns:cc="http://creativecommons.org/ns#" >Данная работа может свободно распространяться по лицензиии <a href="http://creativecommons.org/publicdomain/zero/1.0?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC0 1.0 Universal<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/zero.svg?ref=chooser-v1"></a></p>
