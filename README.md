# IONDV. IS-registry

IONDV. IS-registry - is a web application based on [IONDV. Framework](https://iondv.com). It is used as a registry to account, store, and present the data on the 
availability of information systems
(informatization, types of support, costs of creation and maintenance, level of protection, etc.) necessary for the conduct of the activities of organizations.
A key entity is an information system that contains information about the nature and links to objects, detailed information about the accounting object.

The main advantage of using the system is the analysis of the current state and the availability of information systems.
The app is free for everyone but available only in Russian. 

## Описание  

**IONDV. IS-registry** - это программное решение на основе [IONDV. Framework](https://iondv.com), реализованное для организации учета, хранения и отображения данных об информационных системах 
(информатизация, виды обеспечения, затраты на создание и сопровождение, уровень защиты и др.) необходимых для ведения деятельности организации, в том числе и для собственных продуктов организации. 
Ключевой сущностью является Информационная система, которая содержит в себе информацию описательного характера и ссылки на объекты, содержащие подробную информацию об объекте учета. 

Главное преимущество использования системы - анализ текущего состояния и предоставлении информации о наличии информационных систем.

### Демо

Демо доступ в систему для ознакомления, без регистрации: https://is-registy-ru.iondv.com

Учетная запись для [бек-офиса](https://is-registy-ru.iondv.com/registry): пользователь **demo**, пароль **ion-demo**. 

### Дополнительные преимущества:
 
* Открытый исходный код всех компонентов Системы - https://github.com/iondv/is-registy-ru;
* Открытое программное обеспечение используемое для СУБД и серверных ОС (работет под linux и windows);
* Возможна любая адаптация и модернизация системы, в том числе структур данных без программирования в [визуальном редакторе](https://studio.iondv.com).
* Запуск собственной версии в течении нескольких минут - см. [Как получить](#как-получить)

### Модули

Основу реестра данных составляет [модуль Регистри](https://github.com/iondv/registry). 
Также используются: 

* [Административный модуль](https://github.com/iondv/ionadmin) - позволяет управлять пользователями и ролями для доступа к системе и другими функциями, неоходимыми администартору, 
* [модуль Дашборда](https://github.com/iondv/dashboard) - отображение контрольной панели, с указанием наглядной информации в виде графиков о степени нагрузки системы,
* [модуль Аналитики](https://github.com/iondv/report) - построение аналитических отчетов на основе данных, заведенных в системе.  

## Как получить?  

### Git

Быстрый старт с использованием репозитория IONDV. IS-registry на GitHub — [подробная инструкция](https://github.com/iondv/framework/blob/master/docs/ru/readme.md#быстрый-старт-с-использованием-репозитория).  

1. Установите системное окружение и глобальные зависимости.
2. Клонируйте ядро, модуль и приложение.
3. Соберите и разверните приложение.
4. Запустите.

Или установка и запуск в одну строку под Linux с использованием установщика [iondv-app](https://github.com/iondv/iondv-app) (требуется локально node.js, MongoDB и Git):
```
curl -L -s https://github.com/iondv/iondv-app/archive/master.zip > iondv-app.zip &&\
  unzip -p iondv-app.zip iondv-app-master/iondv-app > iondv-app &&\
  bash iondv-app -q -i -m localhost:27017 is-registry-ru
```
Где вместо `localhost:27017` нужно указать адрес MongoDb. После запуска открыть ссылку 'http://localhost:8888', учетная запись бек офиса **demo**, пароль **ion-demo**.

### Docker

Запуск приложения с использованием докер контейнера - [подробная инструкция](https://hub.docker.com/r/iondv/is-registry-ru).

1. Запустите СУБД mongodb: `docker run --name mongodb -v mongodb_data:/data/db -p 27017:27017 -d mongo`
2. Запустите IONDV. IS-registry `docker run -d -p 80:8888 --link mongodb iondv/is-registry-ru`.
3. Откройте ссылку `http://localhost` в браузере через минуту (время требуется для инициализации данных). Для бек офиса логин: **demo**, пароль: **ion-demo** 

## Ссылки

Для дополнительной информации смотрите следующие ресурсы:

* [IONDV. Framework](https://iondv.com/) 
* [Facebook](https://www.facebook.com/iondv/)

--------------------------------------------------------------------------  


#### [Licence](/LICENSE) &ensp; [Contact us](https://iondv.com/contacts) &ensp; [Stack Overflow](https://stackoverflow.com/questions/tagged/iondv) &ensp; [FAQs](/faqs.md)          
<div><img src="https://mc.iondv.com/watch/github/docs/is-registry-ru" style="position:absolute; left:-9999px;" height=1 width=1 alt="iondv metrics"></div>


--------------------------------------------------------------------------  

Copyright (c) 2018 **LLC "ION DV".**  
All rights reserved.
