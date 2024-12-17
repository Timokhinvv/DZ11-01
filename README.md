# DZ11-01
# Домашнее задание к занятию «Базы данных, их типы»

### Инструкция по выполнению домашнего задания

1. Сделайте fork [репозитория c шаблоном решения](https://github.com/netology-code/sys-pattern-homework) к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/gitlab-hw или https://github.com/имя-вашего-репозитория/8-03-hw).
2. Выполните клонирование этого репозитория к себе на ПК с помощью команды `git clone`.
3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
   - впишите вверху название занятия и ваши фамилию и имя;
   - в каждом задании добавьте решение в требуемом виде: текст/код/скриншоты/ссылка;
   - для корректного добавления скриншотов воспользуйтесь инструкцией [«Как вставить скриншот в шаблон с решением»](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md);
   - при оформлении используйте возможности языка разметки md. Коротко об этом можно посмотреть в [инструкции по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md).
4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`).
5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
6. Любые вопросы задавайте в чате учебной группы и/или в разделе «Вопросы по заданию» в личном кабинете.

Желаем успехов в выполнении домашнего задания.

---

### Задание 1. СУБД

### Кейс
Крупная строительная компания, которая также занимается проектированием и девелопментом, решила создать 
правильную архитектуру для работы с данными. Ниже представлены задачи, которые необходимо решить для
каждой предметной области. 

Какие типы СУБД, на ваш взгляд, лучше всего подойдут для решения этих задач и почему? 
 
1.1. Бюджетирование проектов с дальнейшим формированием финансовых аналитических отчётов и прогнозирования рисков.
СУБД должна гарантировать целостность и чёткую структуру данных.

Для этой задачи подойдут СУБД, поддерживающие работу с финансовыми данными и обеспечивающие целостность данных. Я рекомендую использовать реляционную СУБД, PostgreSQL или MySQL, которые предоставляют строгую структуру данных и обеспечивают высокую безопасность. Реляционная СУБД также позволяет выполнить сложные запросы и аналитику, необходимые для финансовых отчётов.

1.1.* Хеширование стало занимать длительно время, какое API можно использовать для ускорения работы? 


Для ускорения хеширования можно использовать API, такие как Apache, которые поддерживают распределённое хеширование и обеспечивают высокую производительность. Alternatively, можно использовать API, такие как Redis или Memcached.


1.2. Под каждый девелоперский проект создаётся отдельный лендинг, и все данные по лидам стекаются в CRM к 
маркетологам и менеджерам по продажам. Какой тип СУБД лучше использовать для лендингов и для CRM? 
СУБД должны быть гибкими и быстрыми.

Для этой задачи подойдут СУБД, поддерживающие работу с данными, которые постоянно появляются и изменяются. Я рекомендую использовать NoSQL СУБД, которые предоставляют гибкую структуру данных и обеспечивают высокую скорость записи и чтения.

1.2.* Можно ли эту задачу закрыть одной СУБД? И если да, то какой именно СУБД и какой реализацией?

Да, можно закрыть эту задачу одной СУБД. NoSQL СУБД, могут поддерживать оба типа данных (лиды и CRM) и обеспечивать гибкую структуру данных.


1.3. Отдел контроля качества решил создать базу по корпоративным нормам и правилам, обучающему материалу 
и так далее, сформированную согласно структуре компании. СУБД должна иметь простую и понятную структуру.

Для этой задачи подойдут СУБД, поддерживающие работу с структурированными данными. Я рекомендую использовать реляционную СУБД, PostgreSQL или MySQL, которые предоставляют строгую структуру данных и обеспечивают высокую безопасность.


1.3.* Можно ли под эту задачу использовать уже существующую СУБД из задач выше и если да, то как лучше это 
реализовать?

Да, можно под эту задачу использовать реляционную СУБД, PostgreSQL или MySQL. Для реализации можно использовать уже существующую базу данных и добавить в неё новую таблицу для хранения корпоративных норм и правил.


1.4. Департамент логистики нуждается в решении задач по быстрому формированию маршрутов доставки материалов 
по объектам и распределению курьеров по маршрутам с доставкой документов. СУБД должна уметь быстро работать
со связями.

Для этой задачи подойдут СУБД, поддерживающие работу с графами и обеспечивающие быструю обработку связей. Я рекомендую использовать графовую СУБД, Amazon Neptune, которые предоставляют гибкую структуру данных и обеспечивают высокую скорость обработки связей.


1.4.* Можно ли к этой СУБД подключить отдел закупок или для них лучше сформировать свою СУБД в связке с СУБД 
логистов?

Да, можно подключить отдел закупок к графовой СУБД, Amazon Neptune. Для реализации можно использовать API. 


1.5.* Можно ли все перечисленные выше задачи решить, используя одну СУБД? Если да, то какую именно?



*Приведите ответ в свободной форме.*

---

### Задание 2. Транзакции

2.1. Пользователь пополняет баланс счёта телефона, распишите пошагово, какие действия должны произойти для того, чтобы 
транзакция завершилась успешно. Ориентируйтесь на шесть действий.

1. Войдите в систему. Пользователь вводит свои учетные данные (логин и пароль) для входа в систему.

2. Найдите счет. Система ищет учетную запись пользователя и выводит информацию о счете.

3. Проверьте доступные балансы. Система проверяет доступные балансы на счете пользователя и определяет, достаточно ли средств для пополнения.

4. Обновите баланс. Если средств достаточно, система обновляет баланс на счете пользователя.

5. Отразите транзакцию. Система отражает транзакцию в базе данных и генерирует соответствующую запись о транзакции.

6. Обратите внимание пользователя. Система уведомляет пользователя об успешном завершении транзакции.


2.1.* Какие действия должны произойти, если пополнение счёта телефона происходило бы через автоплатёж?

Пользователь авторизует автоплатёж, указав свои учетные данные и данные карты.
Система проверяет доступные балансы на счете пользователя и определяет, достаточно ли средств для пополнения.
Если средств достаточно, система обновляет баланс на счете пользователя и отражает транзакцию в базе данных.
Система также обрабатывает автоплатёж, удерживая соответствующую сумму с карты пользователя.
Система уведомляет пользователя об успешном завершении транзакции.
Система также может отправить подтверждение о пополнении баланса на электронную почту или смс пользователя.


*Приведите ответ в свободной форме.*

---

### Задание 3. SQL vs NoSQL

3.1. Напишите пять преимуществ SQL-систем по отношению к NoSQL. 

1. Строгая структура данных.
2. Поддержка ACID-комплиансности.
3. Предоставление поддержки транзакций.
4. Поддержка сложных запросов.
5. Высокая скорость выполнения запросов.



3.1.* Какие, на ваш взгляд, преимущества у NewSQL систем перед SQL и NoSQL.

*Приведите ответ в свободной форме.*

---

### Задание 4. Кластеры

Необходимо производить большое количество вычислений при работе с огромным количеством данных, под эту задачу 
выделено 1000 машин. 

На основе какого критерия будете выбирать тип СУБД и какая модель *распределённых вычислений* 
здесь справится лучше всего и почему?

*Приведите ответ в свободной форме.*


Рекомендую выбирать тип СУБД, который имеет следующие характеристики:

Распределённая база данных: способность распределять данные по нескольким машинам для повышения производительности и доступности.
Шардирование: способность разделить данные на несколько участков (шардов) для повышения производительности и доступности.
Распределённые вычисления: способность распределять вычисления по нескольким машинам для повышения производительности и доступности.

---

Задания,помеченные звёздочкой, — дополнительные, то есть не обязательные к выполнению, и никак не повлияют на получение вами зачёта по этому домашнему заданию. Вы можете их выполнить, если хотите глубже разобраться в материале.
