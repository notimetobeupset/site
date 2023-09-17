# Изученные темы по проектированию систем

## Rate Limiter
Источники: Тема подробно рассмотрена в текстовом формате в первой части книги "System Design - An insider's guide (volume 1)" авторства Alex Xu.

Видео - https://www.youtube.com/watch?v=FU4WlwfS3G0
### Контрольные вопросы
В разработке

## Consistent Hashing
Источники: Тема подробно рассмотрена в текстовом формате в первой части книги "System Design - An insider's guide (volume 1)" авторства Alex Xu.
### Контрольные вопросы
В разработке

## DESIGNING A UNIQUE ID GENERATOR IN DISTRIBUTED SYSTEMS

Источники: Тема подробно рассмотрена в текстовом формате в первой части книги "System Design - An insider's guide (volume 1)" авторства Alex Xu.

### Контрольные вопросы
1. Какие четыре основных подхода вы можете назвать для решения данной проблемы?
1. Какие недостатки у UUID?
1. В чем отличие подходов "Ticket Server" и "Twitter Snowflake"?
1. Каков предел количества уникальных ID, которые алгоритм "Twitter Snowflake" может сгенерировать в миллисекунду?
1. Что означает "bit tuning" в контексте алгоритма "Twitter Snowflake"?
1. В какой ситуации "Twitter Snowflake" перестает генерировать ID и начинает ожидать определенного события?


## Designing a Location-Based Service (also known as Proximity service)

Источники: Тема подробно рассмотрена в текстовом формате во второй части книги "System Design - An insider's guide (volume 2)" авторства Alex Xu.

Видео -  https://www.youtube.com/watch?v=M4lR_Va97cQ

### Контрольные вопросы
1. Перечислите два основных подхода к алгоритмам индексирования геоданных, а также укажите названия четырех основных алгоритмов.
1. Почему традиционная SQL база данных не подходит для геораспределенного поиска?
1. В чем заключается разница между алгоритмами geohash и quadtree? В каких случаях лучше использовать алгоритм quadtree?

## Nearby Friends (Geospatial Search Service)

Источники: Тема подробно рассмотрена в текстовом формате во второй части книги "System Design - An insider's guide (volume 2)" авторства Alex Xu.

### Контрольные вопросы
1. Кто является publisher, а кто subscriber, в предложенной архитектуре с использованием redis pub/sub? 
1. В предложенной архитектуре какое количество каналов и инстансов redis потредуется, как происхожит scale up/down?
1. Для чего используется location cache?

## S3-like Object Storage

Источники: Тема подробно рассмотрена в текстовом формате во второй части книги "System Design - An insider's guide (volume 2)" авторства Alex Xu.

### Контрольные вопросы
1. В каком сервисе генерируется UUID для сохраняемого объекта?
1. Почему bucket name должен быть уникальным в рамках всего сервиса?
1. Как добавить в систему новый API вызов, который позволяет обновить кусок данных внутри уже хранимого объекта?
1. Как переносить данные, если мы добавили/удалили датацентр или сервер в ДЦ?
1. Что делать, если из-за потери связанности между датацентрами возникли два разных объекта с одинаковым именем?


## Design a Key-Value Store

Источники: Тема подробно рассмотрена в текстовом формате в первой части книги "System Design - An insider's guide (volume 1)" авторства Alex Xu.

Видео: CAP Theorem - https://www.youtube.com/watch?v=BHqjEjzAicA, Distributed Cache - https://www.youtube.com/watch?v=iuqZvajTOyA&t=865s

### Контрольные вопросы
1. В чем разница между eventual consistency и weak consistency?
1. Что происходит при удалении узла из hashing ring и как это влияет на кворум чтения данных?
1. Когда узел становится доступным для чтения/записи при переносе данных внутри hashing ring?
1. Как работает SSTable?
1. В чем различия между Cassandra и MongoDB? 


## Design Youtube

Источники: Тема подробно рассмотрена в текстовом формате в первой части книги "System Design - An insider's guide (volume 1)" авторства Alex Xu.

### Контрольные вопросы
1. Какие изменения произойдут в схеме загрузки при добавлении функции Live Streaming? 
1. Каким образом контент загружается на CDN? 
1. Имеет ли смысл использовать P2P CDN? 

## Design a Notification System

Источники: Тема подробно рассмотрена в текстовом формате в первой части книги "System Design - An insider's guide (volume 1)" авторства Alex Xu.

Видео по теме https://www.youtube.com/watch?v=bBTPZ9NdSk8


### Контрольные вопросы
1. Что можно предпринять, если оборвалась связь с 3rd party провайдером, через которого мы публикуем сообщения (APNS, FCM)?
1. Как защитить пользователя от большого количества нотификаций, если в нашей инфраструктуре появился компонент, который взломали спамеры и начали публикацию сообщений? 
1. Scalability системы: где мы должны использовать масштабируемые инстансы?


## Design Google Drive

Источники: Тема подробно рассмотрена в текстовом формате в первой части книги "System Design - An insider's guide (volume 1)" авторства Alex Xu.

### Контрольные вопросы
В разработке


## Design Inter Planetary File System 

Источники:  
- Офф. сайт https://docs.ipfs.tech/concepts/
- Paper - Design and Evaluation of IPFS: A Storage Layer for the Decentralized Web ( [https://arxiv.org/abs/2208.05877](https://arxiv.org/abs/2208.05877))
- Доклады https://github.com/ipfs/camp/  https://github.com/ipfs/ipfs-camp-2022

Видео запись: https://youtu.be/VZikTwkd_04
### Контрольные вопросы
В разработке