# Zabbix SNMP Template for CommuniGate

> для Zabbix 3.x

> zabbix-agent должен быть установлен на наблюдаемом узле

> успешно используется в системе +500к почтовых ящиков



### Настройка Communigate:

Установки -> Услуги -> SNMP -> Приемник

Необходимо задать порт для SNMP (по умолчанию 161) и задать адреса с которых будут приниматься  SNMP запросы

Установки -> Услуги -> SNMP

Задать пароль (SNMP community) для доступа и версию SNMP протокола.



### Шаблон

щаблон содержит не все метрики (будет добавлено позже)

### Добавление узла

Необходимо задать SNMP community в макросах  {$SNMP_COMMUNITY} = youcommunity (пароль  SNMP в терминах CGP) 

