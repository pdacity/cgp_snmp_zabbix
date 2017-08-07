# cgp_snmp_zabbix

Zabbix SNMP template for CommuniGate server

Настройка Communigate:

Установки -> Услуги -> SNMP -> Приемник

Необходимо добавить порт для SNMP (по умолчанию 161) и задать адреса с которых будут приниматься  SNMP запросы

Установки -> Услуги -> SNMP

Задать пароль (SNMP community) для доступа и версию SNMP протокола.



Шаблон


Добавление узла

Необходимо задать SNMP community в макросах  {$SNMP_COMMUNITY} = youcommunity (пароль  SNMP в терминах CGP) 


