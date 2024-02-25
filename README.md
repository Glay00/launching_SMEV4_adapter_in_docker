# Задание 2: Запуск СМЭВ 4 адаптера в Docker

## p.s Файл с выполненным заданием слишком большой, поэтому необходимо скачать [архив с Google drive](https://drive.google.com/file/d/1AAZtdpHQciFF_jFhGqm5-9Drn-Gtk-qf/view?usp=sharing) (см. примечание).

### 1. Ознакомиться с документацией Агента ПОДД (СМЭВ 4 Адаптер)

- Ознакомился с документацией;
- Создал тестовую организацию ЛК УВ;
- Создал ИС в тестовой среде ЛК УВ;
- Сформировал сертификаты для дальнейшего подключения;
- Ознакомился с инструкцией для развёртывания в docker.

### 2. Разверуть  образ docker контейнера для Агента ПОДД


- Развернул docker-image (локально).
![2024-02-25 19 52 01](https://github.com/Glay00/second_task_to-increase/assets/96641789/1736e73a-483e-4747-83a1-0ca7503a6360)

- Настроил конфигрурационный файл application.yml.
![Снимок экрана 2024-02-25 в 13 43 27](https://github.com/Glay00/second_task_to-increase/assets/96641789/8d367bea-733d-495a-99c3-610096ea0a75)

- Запустил контейнер-докер (локально).
<img width="1384" alt="Снимок экрана 2024-02-25 в 15 25 52" src="https://github.com/Glay00/second_task_to-increase/assets/96641789/031bb391-aaed-4c59-bb5b-fb9b956f3f53">

### 3. Получить лог-файл Агента ПОДД

- см. файл ```log-20240225-114110.txt```

### 4. Описать схему обмена сведениями в СМЭВ 4

СМЭВ 4 - это система, предназначенная для обмена сведениями между организациями или органами власти в рамках сеансов
обмена.

![Vvodnaya-Risunok1](https://github.com/Glay00/second_task_to-increase/assets/96641789/7fb39cc8-ae98-4fc8-8cdc-766deae4ef22)

#### В роли участников взаимодействия можно выделить следующих:

- Поставщики данных
- Потребители данных

---

Потребители данных могут получать сведения из других ИС путём отправки регламентированных запросов или пользуясь
подпиской
на изменение сведений.

---

Поставщики данных ПОДД СМЭВ осуществляют подключение к ПОДД СМЭВ, размещая актуальные данные, а также регистрируют
регламентированные завросы для получения данных Потребирелем.

Все запросы и ответы направляются в ПОДД СМЭВ от имени организаций
и подписываются электронными подмисями органов власти (ЭП-ОВ).

### 5. Описать отличие СМЭВ 4 от СМЭВ 3

В настоящее время существуют две версии СМЭВ — v3 и v4.

СМЭВ 3, разработанная в 2009 году, на момент своего запуска привнесла революцию в систему государственного
взаимодействия.
Однако со временем стали появляться новые требования и возможности, необходимые для её совершенствования, что привело к
созданию более современной версии — СМЭВ 4.

---

#### Основные отличия СМЭВ4 и СМЭВ 3:

- поддержка технологии RESTful API;
- создание гибких и маштабируемых приложений с использованием HTTP-протокола;
- использование новых технологий и стндартов, обеспечивающие безопасное электронное взаимодействие.
- современный интерфейс для пользователя + расширенный функционал для граждан

---

#### Технические характеристики отличия (СМЭВ 4 от СМЭВ 3):

- версия протокола: В СМЭВ 3 используется протокол SOAP 1.1, а в СМЭВ 4 — SOAP 1.2. Это обеспечивает более надежную и
  безопасную передачу данных между системами.
- система шифрования: СМЭВ 4 поддерживает более современные алгоритмы шифрования, такие как ГОСТ Р 34.10-2012 и ГОСТ Р
  34.11-2012. Это обеспечивает высокую безопасность данных при передаче.
- режим работы: В СМЭВ 3 используется синхронный режим работы, когда ответ на запрос возвращается непосредственно после
  выполнения запроса. В СМЭВ 4 также присутствует возможность асинхронного режима работы, когда ответ на запрос может
  быть получен позже.
- возможность передачи вложений: СМЭВ 4 позволяет передавать вложения в виде файлов с использованием протокола MTOM, что
  обеспечивает более эффективную и экономичную передачу больших объемов данных.
- работа с реестрами: В СМЭВ 4 добавлена возможность работы с реестрами для хранения и получения информации. Это
  обеспечивает удобство и гибкость при работе с данными.

---

#### Формат данных в СМЭВ3:

- используется XML формат для передачи данных. XML позволяет описывать структуру и содержание данных с помощью тегов и
  атрибутов.

#### Формат данных в СМЭВ4:

- используется более современный формат данных — JSON. JSON обеспечивает более компактное представление данных, что
  позволяет снизить объем трафика и увеличить скорость передачи.

---

### Примечание:

- Для запуска необходимо разархивировать скачанный [файл](https://drive.google.com/file/d/1AAZtdpHQciFF_jFhGqm5-9Drn-Gtk-qf/view?usp=sharing),
  а также в корне проекта разархивировать certs.zip и keys.zip.

---
## #TODO FOR ME:

- поработать с CryptoPro чтобы лучше ориентироваться в особенностях при работе с ключами и сертификатам (научиться администрировать).
