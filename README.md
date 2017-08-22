# EN

# Zabbix SNMP Template for CommuniGate

> Version 1.2 - (20170822)

> for Zabbix 3.x (Zabbix 2.x was not tested)

> zabbix-agent must be installed on the monitored node

> some of the less critical metrics are not included in the template



### Communigate settings:

Установки -> Услуги -> SNMP -> Приемник

Необходимо задать порт для SNMP (по умолчанию 161) и задать адреса с которых будут приниматься  SNMP запросы

Установки -> Услуги -> SNMP

Set the password (SNMP community) for access and the SNMP protocol version


### Template
* The template receives and processes the built-in CommuniGate metrics (Наблюдение -> Статистика)

* The template does not contain all metrics (will be added later)

### Graphs

* CGP Auth - external authentication, including errors
* CGP IMAP - the IMAP protocol usage
* CGP Session - users sessions (HTTPU)
* CGP SMTP - SMTP protocol usage
* CGP TCP Traffic - total TCP traffic for node

![Host](https://github.com/pdacity/cgp_snmp_zabbix/blob/master/CGP_sessions.png)

![Host](https://github.com/pdacity/cgp_snmp_zabbix/blob/master/CGP_SMTP.png)

### Adding node

* On each node add a template "Template CGP SNMP"

* Set the macros {$SNMP_COMMUNITY} = youcommunity 



# RU

# Zabbix SNMP Template for CommuniGate

> версия 1.2 - (20170822)

> для Zabbix 3.x (Zabbix 2.x не тестировалось)

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

* На каждом узле добавьте шаблон "Template CGP SNMP"

* Необходимо задать SNMP community в макросах  {$SNMP_COMMUNITY} = youcommunity (пароль  SNMP в терминах CGP) 

