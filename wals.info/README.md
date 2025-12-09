# WALS

[The World Atlas of Language Structures](https://wals.info/chapter) (WALS) – это база данных различных свойств языков (фонологических, грамматических, лексических), собранная на основе описательных материалов большой командой авторов. На странице Chapters представлен список глав по категориям и авторам. Также на сайте представлены языковые карты с представленностью тех или иных явлений в разных языках мира.

## ArchiveReady

![](/wals.info/ArchiveReady.png)

У [данного сайта](https://archiveready.com/check?url=https%3A%2F%2Fwals.info%2Fchapter) достаточно высокий рейтинг архивируемости: он обладает максимальным показателем целостности (Cohesion), остальные показатели также довольно высоки. Наиболее низко оценено соответствие стандартам (Standards Compliance). Из отмеченных проблем: есть некорректные RSS, HTML и CSS-файлы, низкая скорость отклика сайта, недоступны HTTP-заголовки, есть Java-script вставки.

## Replay Webpage

В данном случае дизайн сайта был сохранен практически полностью, все разделы в шапке сайта сохранены. Однако не хватает самой важной части: база, которая подгружалась в разделах с главами, недоступна, что лишает архива его главной составляющей.

![](/wals.info/ReplayWebpage1.png)

![](/wals.info/ReplayWebpage2.png)

## metawarc

`metawarc analyze wals.info.warc.gz`

| mimes                  | files |      size |      share |
|------------------------|------:|----------:|-----------:|
| application/xml        |    13 |  14540323 |   92.9964  |
| application/javascript |     1 |    685719 |    4.3857  |
| text/css               |     1 |    289902 |    1.85414 |
| text/html              |     8 |     81417 |    0.520724|
| image/png              |     3 |     20506 |    0.131152|
| image/gif              |     1 |      9131 |    0.0583997|
| text/javascript        |     1 |      6756 |    0.0432098|
| image/x-icon           |     1 |      1401 |    0.00896046|
| text/plain             |     1 |       198 |    0.00126636|
| #total                 |    30 |  15635353 |  100       |
	
БОльшую часть архива занимают xml - это sitemap-файлы со ссылками на некоторые объекты и последней датой обновления.
	 
`metawarc metadata --output meta.jsonl wals.info.warc.gz`

Файлы с метаданными доступны в meta.jsonl. Там перечислены некоторые характеристики нескольких встретившихся png-изображений. Ошибки при извлечении метаданных записаны в файле metadata_errors.txt.
 
`metawarc index wals.info.warc.gz`
 
Эта команда индексирует архив и создаёт базу данных, по которой можно производить дополнительный анализ.

`metawarc stats -m mimes`

| mime                           |     size | count |
|--------------------------------|---------:|------:|
| application/javascript         |   685719 |     1 |
| application/xml; charset=UTF-8 | 14540323 |    13 |
| image/gif                      |     9131 |     1 |
| image/png                      |    20506 |     3 |
| image/x-icon                   |     1401 |     1 |
| text/css                       |   289902 |     1 |
| text/html                      |      326 |     1 |
| text/html; charset=UTF-8       |     8515 |     1 |
| text/html; charset=utf-8       |    72576 |     6 |
| text/javascript; charset=UTF-8 |     6756 |     1 |
| text/plain; charset=UTF-8      |      198 |     1 |

Таблица практически дублирует информацию команды analyze выше.
