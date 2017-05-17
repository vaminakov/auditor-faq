# Небольшой FAQ по АС "Ревизор" и процедурам блокировки в целом:
***
Если у вас имеются вопросы/проблемы с АС "Ревизор" и вы не нашли ответы в данном FAQ, обратитесь в группу "Я люблю АС "Ревизор" в [Telegram](https://t.me/i_love_auditor)
***
**Вопрос:** Каким образом ресурс, добавленный в реестр n часов/дней/лет назад попал в выгрузку только сейчас:

**Ответ:** Все очень просто. Реестр не является выгрузкой. Операторы обязаны блокировать только то, что в выгрузке. Сутки на блокировку даются именно с момента появления в выгрузке.
***
**Вопрос:** Через какое время после появления в выгрузке Ревизор начинает проверять сайты?

**Ответ:** Через сутки по всему реестру, через час для записей 398-ФЗ (экстремизм).
***
**Вопрос:** По каким IP-адресам ходит Ревизор?

**Ответ:** Ревизор берет IP-адреса явно указанные в реестре, а также из DNS для domain/url.
***
**Вопрос:** Если у сайта 5/10/20 IP-адресов, сколько будет выявлено нарушений?

**Ответ:** Например, у сайта 10 IP-адресов в реестре, и 10 (других) в DNS. Ревизор проверит все 20. Если ко всем не получит доступ, нарушения нет. Если получит доступ к одному из 20, будет зафиксировано одно нарушение. Если получит доступ ко всем 20, будет зафиксировано одно нарушение.
***
**Вопрос:** Какими DNS пользуется Ревизор?

**Ответ:** Строго теми, которые выдает оператор связи по DHCP. В случае, если у оператора нет своих DNS-серверов, а также в служебных целях (не для проверок) используется сервер 8.8.8.8.
***
**Вопрос:** Подозреваю, что коробка лукавит/система сбоит. Как быть?

**Ответ:** Пишите дамп трафика, обращайтесь к [@vvl_rulez](https://t.me/vvl_rulez)
***
**Вопрос:** Как записать дамп Ревизора?

**Ответ:** tcpdump -i <iface> -G 1800 -w /storage/hd1/dumps/<some_name>_%d-%m-%Y_%H-%M-%I.pcap - пишет дампами по пол-часа (параметр -G - ротация по времени в секундах) в имени файла указываются параметры strftime.
***
**Вопрос:** Как обмануть коробку? Не хочу исполнять закон, хочу избежать штрафов.

**Ответ:** Коробка не так тупа, как кажется. Проще грамотно настроить систему фильтрации (в теме вам помогут). В случае, если будет выявлена подобная попытка - сотрудники Роскомнадзора со всем пристрастием объяснят вам вашу неправоту.
***
**Вопрос:** Зачем вообще нужны программные Агенты? Не хочу его ставить, он не сертифицирован.

**Ответ:** Ваше право (получите аппаратный). В рамках действующего законодательства нет требований к сертификации программного Агента, поэтому он и не сертифицирован.
