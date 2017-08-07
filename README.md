# Zabbix SNMP Template for CommuniGate

> версия 1.1 - (20170807)

> для Zabbix 3.x

> zabbix-agent должен быть установлен на наблюдаемом узле

> успешно используется в системе c 500000+ почтовых ящиков

> часть малокритичных метрик не включена в шаблон. Будет исправлено во 2 версии



### Настройка Communigate:

Установки -> Услуги -> SNMP -> Приемник

Необходимо задать порт для SNMP (по умолчанию 161) и задать адреса с которых будут приниматься  SNMP запросы

Установки -> Услуги -> SNMP

Задать пароль (SNMP community) для доступа и версию SNMP протокола.


### Шаблон
* Шаблон получает и обрабатывает встроенные метрики CommuniGate (Наблюдение -> Статистика)

* Шаблон содержит не все метрики (будет добавлено позже)

### Графики

* CGP Auth - график внешних аутентификаций, включая ошибочные
* CGP IMAP - график использование  IMAP протокола
* CGP Session - график пользовательских сессий (HTTPU)
* CGP SMTP - график использования  SMTP протокола
* CGP TCP Traffic - график общего TCP тафика узла

![Host](https://github.com/pdacity/cgp_snmp_zabbix/blob/master/CGP_sessions.png)

![Host](https://github.com/pdacity/cgp_snmp_zabbix/blob/master/CGP_SMTP.png)

### Добавление узла

* На каждом узде добавьте шаблон "Template CGP SNMP"

* Необходимо задать SNMP community в макросах  {$SNMP_COMMUNITY} = youcommunity (пароль  SNMP в терминах CGP) 

