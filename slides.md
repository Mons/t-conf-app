class: first
layout:false

.absolute.left10.right30.top8[

# Подходы к построению приложений на Tarantool

## Владимир Перепелица
## Mail.ru Cloud Solutions
]

---

class: first
layout:false

.absolute.left10.right30.top8[

# Подходы к построению приложений на Tarantool

## Mons Anderson
## Mail.ru Cloud Solutions
]

???

# Вступление: чем мы занимаемся


---
layout:true
.footer[
   .mcslogo.absolute.top00.bottom00[
      ![](style/mcs.svg)
   ]
   .absolute.left20.top0[
      [mons.github.io/t-conf-app](https://mons.github.io/t-conf-app)
   ]
]

---

# Чем мы занимаемся?

???

# Делаем приложения на Tarantool в Mail.ru

---

# Чем мы занимаемся?

* Делаем приложения на Tarantool в Mail.ru

???

# 6 лет

---

# Чем мы занимаемся?

* Делаем приложения на Tarantool в Mail.ru

* 6 лет

???

# Облако Mail.ru

---

# Чем мы занимаемся?

* Делаем приложения на Tarantool в Mail.ru

* 6 лет

* Облако Mail.ru

???

# Mail.ru Cloud Solutions

---

# Чем мы занимаемся?

* Делаем приложения на Tarantool в Mail.ru

* 6 лет

* Облако Mail.ru

* Mail.ru Cloud Solutions

???

# От 1.4 до 1.10+

---

# Чем мы занимаемся?

* Делаем приложения на Tarantool в Mail.ru

* 6 лет

* Облако Mail.ru

* Mail.ru Cloud Solutions

* От 1.4 до 1.10+

???

# 💩

---

# Чем мы занимаемся?

* Делаем приложения на Tarantool в Mail.ru

* 6 лет

* Облако Mail.ru

* Mail.ru Cloud Solutions

* От 1.4 до 1.10+

* Наелись 💩

???

# Что мы сделали

---

# Что мы сделали на базе Tarantool?

???

# Key-value с экспайром (мемкэш)

---

# Что мы сделали на базе Tarantool?

* Key-value с экспирацией

???

# Кеширующие прокси к SQL


---

# Что мы сделали на базе Tarantool?

* Key-value с экспирацией

* Кеширующие прокси к SQL

???

# Очереди

---

# Что мы сделали на базе Tarantool?

* Key-value с экспирацией

* Кеширующие прокси к SQL

* Очереди

???

# Очень разные очереди

---

# Что мы сделали на базе Tarantool?

* Key-value с экспирацией

* Кеширующие прокси к SQL

* Очереди

* Очень разные очереди

???

# Шардированные кластера

---

# Что мы сделали на базе Tarantool?

* Key-value с экспирацией

* Кеширующие прокси к SQL

* Очереди

* Очень разные очереди

* Шардированные кластера

???

# Мультимастер кластер

---

# Что мы сделали на базе Tarantool?

* Key-value с экспирацией

* Кеширующие прокси к SQL

* Очереди

* Очень разные очереди

* Шардированные кластера

* Мультимастер кластер

???

# 3 биллинга

---

# Что мы сделали на базе Tarantool?

* Key-value с экспирацией

* Кеширующие прокси к SQL

* Очереди

* Очень разные очереди

* Шардированные кластера

* Мультимастер кластер

* Биллинги

???

# Рейт-лимитер

---

# Что мы сделали на базе Tarantool?

* Key-value с экспирацией

* Кеширующие прокси к SQL

* Очереди

* Очень разные очереди

* Шардированные кластера

* Мультимастер кластер

* Биллинги

* Рейт-лимитер

???

# Сложно поверить — как реляционную БД

---

# Что мы сделали на базе Tarantool?

* Key-value с экспирацией

* Кеширующие прокси к SQL

* Очереди

* Очень разные очереди

* Шардированные кластера

* Мультимастер кластер

* Биллинги

* Рейт-лимитер

* Просто использовали как реляционную базу данных :)

???

# Документация говорит: тарантул — БД

---

# tarantool.io/doc:

* Tarantool — база данных

???

# А ещё — сервер приложений

---

# tarantool.io/doc:

* Tarantool — база данных

* _Tarantool — сервер приложений_

???

# И как его готовить?

---

# tarantool.io/doc:

* Tarantool — база данных

* _Tarantool — сервер приложений_

.center[
# как?
]

???

# Что нужно для эксплуатации?

---

# Эксплуатация приложения

???

# Доставка кода

---

# Эксплуатация приложения

* Доставка кода

???

# Обновление

---

# Эксплуатация приложения

* Доставка кода

* Обновление

???

# Конфигурация

---

# Эксплуатация приложения

* Доставка кода

* Обновление

* Конфигурация

???

# Обратная совместимость

---

# Эксплуатация приложения

* Доставка кода

* Обновление

* Конфигурация

* Обратная совместимость

???

# Наше стандартное решение

---

# Наше стандартное приложение (снаружи)

???

# Определённый layout
# (like LSB)

---

# Наше стандартное приложение (снаружи)

* Базируется на baselayout

???

# Общение только по iproto
# (msgpack)

---

# Наше стандартное приложение (снаружи)

* Базируется на baselayout

* Общение с тарантулом — по iproto

???

# В тарантул ходим из nginx

---

# Наше стандартное приложение (снаружи)

* Базируется на baselayout

* Общение с тарантулом — по iproto

* Nginx → Tarantool

???

# а также из различных демонов

---

# Наше стандартное приложение (снаружи)

* Базируется на baselayout

* Общение с тарантулом — по iproto

* Nginx → Tarantool

* (Perl/Go/&hellip;) → Tarantool

???

# Tarantool → Tarantool (net.box)

---

# Наше стандартное приложение (снаружи)

* Базируется на baselayout

* Общение с тарантулом — по iproto

* Nginx → Tarantool

* (Perl/Go/&hellip;) → Tarantool

* &hellip; → Tarantool (Balancer) → Tarantool (Sharder) → Tarantool → &hellip;

???

# Даже есть универсальная прокси

---

# Наше стандартное приложение (снаружи)

* Базируется на baselayout

* Общение с тарантулом — по iproto

* Nginx → Tarantool

* (Perl/Go/&hellip;) → Tarantool

* &hellip; → Tarantool (Balancer) → Tarantool (Sharder) → Tarantool → &hellip;

* Универсальная прокси: moonlibs/apex

???

# А что внутри?

---

# Наше стандартное приложение (внутри)

???

# Только iproto CALL

---

# Наше стандартное приложение (внутри)

* Только CALL

???

# API wrapper

---

# Наше стандартное приложение (внутри)

* Только CALL

* Точка входа — API wrapper

???

# Перехват ошибок во враппере
# (pcall/xpcall)

---

# Наше стандартное приложение (внутри)

* Только CALL

* Точка входа — API wrapper

* Перехват ошибок

???

# Асинхрон — контекст

---

# Наше стандартное приложение (внутри)

* Только CALL

* Точка входа — API wrapper

* Перехват ошибок

* Объект контекста (moonlibs/ctx)

???

# request-id (ctx)
# tracing

---

# Наше стандартное приложение (внутри)

* Только CALL

* Точка входа — API wrapper

* Перехват ошибок

* Объект контекста (moonlibs/ctx)

* Проброс или генерация request-id (tracing)

???

# Логгирование + req-id

---

# Наше стандартное приложение (внутри)

* Только CALL

* Точка входа — API wrapper

* Перехват ошибок

* Объект контекста (moonlibs/ctx)

* Проброс или генерация request-id (tracing)

* Логгирование

???

# "HTTP"-стиль

---

# Наше стандартное приложение (внутри)

* Только CALL

* Точка входа — API wrapper

* Перехват ошибок

* Объект контекста (moonlibs/ctx)

* Проброс или генерация request-id (tracing)

* Логгирование

* "HTTP" стиль возврата

```lua
return box.tuple.new{ 200, {...} }
return box.tuple.new{ 500, {...} }
```

???

# Что насчёт шардинга?

---

# Шардинг?

???

# Свой

--

* Свой

--

* v1

--

* v2

--

* v3

--

* &hellip;

???

# иногда vshard

--

* tarantool/vshard

???

# >> baselayout

---

# Baselayout

???

# Унифицированный подход
* разработка
* продакшн

---

# Baselayout

* Унифицированный подход к запуску
   - nodetach
   - tarantoolctl (local)
   - init.d
   - systemd

???

# Зависимости

---

# Baselayout

* Унифицированный подход к запуску
   - nodetach
   - tarantoolctl (local)
   - init.d
   - systemd

* Установка зависимостей (sandbox)

???

# Сборка RPM

---

# Baselayout

* Унифицированный подход к запуску
   - nodetach
   - tarantoolctl (local)
   - init.d
   - systemd

* Установка зависимостей (sandbox)

* Сборка пакетов

???

# Как к этому пришли?
# Подход 1.5

---

# Подход "1.5"

> /etc/tarantool/instances.enabled/myapp.lua:

```nohighlight
box.cfg{
   ...
}

dofile "/usr/share/myapp/init.lua"
```

???

## счастливые люди – не видели 1.5
<br/>

# Проблемы
## Нет контроля за `box.cfg`
## конфиг приложения?

---

# Подход "1.5"

> /etc/tarantool/instances.enabled/myapp.lua:

```nohighlight
box.cfg{
   ...
}

dofile "/usr/share/myapp/init.lua"
```

* Нет контроля за `box.cfg` со стороны приложения
* Где хранить конфиг приложения?

???

# Подход 1.6
# приложение в /etc

---

# Подход "1.6"

> /etc/tarantool/instances.enabled/myapp.lua:

```nohighlight
myapp...

box.cfg{
   ...
}

myapp...
```

???

# Проблемы:
## Код в etc
## Доставка кода пакетом?
## Где хранить конфиг приложения?

---

# Подход "1.6"

> /etc/tarantool/instances.enabled/myapp.lua:

```nohighlight
myapp...

box.cfg{
   ...
}

myapp...
```

* Код в etc

* Доставка кода пакетом?

* Где хранить конфиг приложения?

???

# baselayout:
## приложение в /usr/share

---

# Подход baselayout: application

```nohighight
/usr/share/myapp/
├── `init.lua`
├── app
│   ├── myapp
│   │   ├── api
│   │   │   └── ...
│   │   └── db
│   │       ├── scheme.lua
│   │       └── triggers.lua
│   └── myapp.lua
└── libs
    ├── lib64
    │   ├── lua
    │   │   └── 5.1
    │   │       └── ...
```

???

# baselayout:
## конфиги в /etc

---

# Baselayout: config

```nohighlight
/etc/tarantool/
└── instances.available
    ├── myapp_01.lua -> /usr/share/myapp/init.lua
    ├── myapp_02.lua -> /usr/share/myapp/init.lua
    └── example.lua

/etc/myapp/
└── conf.lua
```

???

# Baselayout: начинка
## init.lua

---

# Baselayout: init.lua

???

# Резолвинг окружения (nodetach, ctl, ...)

---

# Baselayout: init.lua

* Резолвинг окружения (nodetach, ctl, ...)

???

# Определение имени инстанса

---

# Baselayout: init.lua

* Резолвинг окружения (nodetach, ctl, ...)

* Определение имени инстанса

???

# Поиск конфига (/etc или ./etc)

---

# Baselayout: init.lua

* Резолвинг окружения (nodetach, ctl, ...)

* Определение имени инстанса

* Поиск конфига (/etc или ./etc)

???

# package.path: локальные либы
# sandbox

---

# Baselayout: init.lua

* Резолвинг окружения (nodetach, ctl, ...)

* Определение имени инстанса

* Поиск конфига (/etc или ./etc)

* Установка `package.path` и `package.cpath`

???

# обязательные модули
## config
## package.reload
## kit

---

# Baselayout: init.lua

* Резолвинг окружения (nodetach, ctl, ...)

* Определение имени инстанса

* Поиск конфига (/etc или ./etc)

* Установка `package.path` и `package.cpath`

* Подключение обязательного набора модулей

   - config
   - package.reload
   - kit

???

# config: задумывалось

---

# config: задумывалось

* Загрузка конфига из /etc

.width90.margin-auto[
> /etc/myapp/conf.lua:

```nohighlight
box = {
   background = true,
   work_dir   = "/var/lib/tarantool/myapp",
   ...
}
app = {
   param = "value",
}
```
]


* Вызов `box.cfg` с параметрами из секции `box`

* Метод для получения параметров из Lua: `config.get`

???

# а на самом деле получилось

---

# config: получилось

???

# Загрузка конфига из /etc

---

# config: получилось

* Загрузка конфига из /etc

???

# Загрузка конфига из etcd, если указано

---

# config: получилось

* Загрузка конфига из /etc

* Загрузка конфига из etcd, если указано

* Мерж конфигов

???

# Валидация параметров под версию


---

# config: получилось

* Загрузка конфига из /etc

* Загрузка конфига из etcd, если указано

* Мерж конфигов

* Валидация параметров

???

# запуск или релоад

---

# config: получилось

* Загрузка конфига из /etc

* Загрузка конфига из etcd, если указано

* Мерж конфигов

* Валидация параметров

* Определение фазы (запуск или релоад)

???

# роль: мастер/реплика
# список реплик

---

# config: получилось

* Загрузка конфига из /etc

* Загрузка конфига из etcd, если указано

* Мерж конфигов

* Валидация параметров

* Определение фазы (запуск или релоад)

* Определение списка реплик и роли (ro/rw)

???

# Воркэраунды эксплуатационных проблем

---

# config: получилось

* Загрузка конфига из /etc

* Загрузка конфига из etcd, если указано

* Мерж конфигов

* Валидация параметров

* Определение фазы (запуск или релоад)

* Определение списка реплик и роли (ro/rw)

* Воркэраунды эксплуатационных проблем

???

# пример проблемы
# рестарт мастера
# работают мастер + реплика

---

# Проблема рестарта мастера

.width70.margin-auto[
```nohighlight
           
           
M..........
           
           
           

R..........
           
           

──────────────────────────────────────────────────>
                                                  t
```
]

???

# мастер рестартится
# стартует
# загружает снапшот

---

# Проблема рестарта мастера

.width70.margin-auto[
```nohighlight
           мастер упал
           ▼
M..........X.cfg/rw...
              
              
              

R.....................
                      
                      

──────────────────────────────────────────────────>
                                                  t
```
]

???

# это долго

---

# Проблема рестарта мастера

.width70.margin-auto[
```nohighlight
           мастер упал
           ▼
M..........X.cfg/rw...............up
              └─────────┬─────────┘
                    загрузка
                   ~ 5Gb/min

R...................................
                        
                        

──────────────────────────────────────────────────>
                                                  t
```
]

???

# админ или автоматика
# переключат мастер


---

# Проблема рестарта мастера

.width70.margin-auto[
```nohighlight
           мастер упал
           ▼
M..........X.cfg/rw...............up
              └─────────┬─────────┘
                    загрузка
                   ~ 5Gb/min

R.......................M...........
                        ▲
                        админ переключил

──────────────────────────────────────────────────>
                                                  t
```
]

???

# загрузка продолжилась
# rw
# 2 мастера

---

# Проблема рестарта мастера

.width70.margin-auto.not[
```nohighlight
           мастер упал               второй мастер
           ▼                         ▼
M..........X.cfg/rw.............up/rw`.`
              └─────────┬─────────┘
                    загрузка
                   ~ 5Gb/min

R.......................M............`.`
                        ▲
                        админ переключил

──────────────────────────────────────────────────>
                                                  t
```
]

???

# конфиг:
# заворкэраундим

---

# config. воркэраунды эксплуатационных проблем

* Рестарт мастера
   - Запуск `box.cfg{ ..., readonly=true }`
   - Перечитывание конфига
   - Вызов `box.cfg{ readonly=false }` (если требуется)

???

# Рестарт репликации при релоаде

---

# config. воркэраунды эксплуатационных проблем

* Рестарт мастера
   - Запуск `box.cfg{ ..., readonly=true }`
   - Перечитывание конфига
   - Вызов `box.cfg{ readonly=false }` (если требуется)

* Рестарт репликации при релоаде
   - Валидация списка реплик при релоаде
   - Сверка текущего значения с конфигом

???

# Проблемы запуска мультимастера
# default: RO

---

# config. воркэраунды эксплуатационных проблем

* Рестарт мастера
   - Запуск `box.cfg{ ..., readonly=true }`
   - Перечитывание конфига
   - Вызов `box.cfg{ readonly=false }` (если требуется)

* Рестарт репликации при релоаде
   - Валидация списка реплик при релоаде
   - Сверка текущего значение с конфигом

* Проблемы запуска мультимастера
   - Запуск без параметра по умолчанию в readonly

???

# мутант

---
class: image-full

![](style/aeromunculus-crop.jpg)

???

# Перезагрузка кода

---

# Перезагрузка кода: `package.reload`

```lua
...
require 'package.reload'
...
```

* Запоминает загруженные пакеты

* При повторной загрузке очищает `package.loaded`

* Считает перезагрузки

* Имеет интерфейс для регистрации коллбэка на релоад

* Перезагрузка командой `package.reload()`<br>(вместо `dofile "/path/to/init.lua"`)

```lua
tarantool> package.reload()
```

???

# обратная совместимость

---

# Обратная совместимость

???

# обновитесь

---

# Обратная совместимость

.absolute.width40.left30.right30[
![](style/update.webp)
]

???

# нельзя просто так...

---

# Обратная совместимость

```nohighlight
> box.info
---
- version: 1.6.9-93-g54ff183
  status: running
  uptime: 26347645
  vclock:
  - 300196557
  - 1038271887
  - 742025077
  - 441487729
  - 1215367990
  - 1388988834
  - 1563133725
  - 6539473305
  - 1122655197
...
```

???

# сервер пожил.
# аптайм под год

---

# Обратная совместимость

```nohighlight
> box.info
---
- version: `1.6.9`-93-g54ff183
  status: running
  uptime: 26347645    `<----- 304 дня`
  vclock:
  - 300196557
  - 1038271887
  - 742025077
  - 441487729
  - 1215367990
  - 1388988834
  - 1563133725
  - 6539473305
  - 1122655197
...
```

???

# цепочка версий

---

# Обратная совместимость

.center[
# 1.6 → 1.7 → 1.9 → 1.10 → 1.10.2 → 1.10.3 → 2.0 → 2.1
]

???

# правильный символ

---

# Обратная совместимость

.center[
# 1.6 💩 1.7 💩 1.9 💩 1.10 💩 1.10.2 💩 1.10.3 💩 2.0 💩 2.1
]

???

# box.info

---

# Обратная совместимость

.center[
# 1.6 → 1.7 → 1.9 → 1.10 → 1.10.2 → 1.10.3 → 2.0 → 2.1
]

* `box.info.server.ro` vs `box.info.ro`

* `box.info.server.*`: `lsn`, `id`, `uuid`

* `wait_lsn`

* `schema_version`

* &hellip;

???

# kit: обобщённый интерфейс

---

# kit: обобщённый интерфейс

```lua
require 'kit'
```

```nohighlight
tarantool> kit.node()
---
- id: 1
  uuid: 1457a4ce-0001-0001-0000-000000000000
  lsn: 8120720
  ro: false
  rw: true
  hostname: my.hostname.com
...
```


???

# функции из новых версий

---

# kit: обратная совместимость

* `kit.wait_lsn(node_id, lsn [,timeout])`

* `table.new`, `table.clear`

* `box.NULL` without box.cfg

* `kit.schema_version`

???

# как сделано

---

# kit: устройство

```nohighlight
├── kit.lua
└── kit
    ├── 1
    │   ├── 10.lua
    │   ├── 5
    │   │   ├── fiber.lua
    │   │   └── init.lua
    │   ├── 6
    │   │   └── 0.lua
    │   ├── 6+.lua
    │   ├── 6.lua
    │   ├── 7.lua
    │   └── 9.lua
    ├── 1.lua
    └── loc.lua
```

???

# порядок загрузки

---

# kit: устройство

## 1.10.2-203-g0b7078a

* kit/1.lua

* kit/1/10.lua

* kit/1/10/2.lua

* kit/1/10/2-203-g0b7078a.lua

???

# что ещё мы используем?

---

# Что ещё?

* moonlibs/tarantoolapp — генератор шаблона приложения

* igorcoding/spacer (v1) — декларативное описание спейсов

* igorcoding/spacer (v2) — + мигратор схемы

* tarantool/moonwalker — обход спейса

* moonlibs/xqueue — модуль для очередей

* moonlibs/apex — универсальная прокси

???

# Как попробовать?

---

# Как попробовать?

.absolute.left25.right25.top30[
## https://github.com/moonlibs/tarantoolapp
## https://github.com/moonlibs/baselayout
## https://github.com/moonlibs/config
]

---

# Как попробовать?


.absolute.left15.right15.top30[
```nohighlight
$ luarocks install tarantoolapp

$ tarantoolapp create --template=universal myapp
```
]

---
class:first
layout:false

.absolute.left10.right30.top8[

# Вопросы?

#### https://github.com/tarantool<br>https://github.com/moonlibs

## Mons Anderson
## Mail.ru Cloud Solutions
]

.absolute.bottom1.left20.color-white[
[mons.github.io/t-conf-app](https://mons.github.io/t-conf-app)
]
