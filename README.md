# docker-mediawiki

## Установка docker
Устанавливаем docker, используя [официальную инструкцию](https://docs.docker.com/engine/install/)

# Установка mediawiki с дополнительными плагинами
В файле `mediawiki/Dockerfile` описаны плагины, которые будут добавлены к официальному образу.

# LDAP
На текущий момент (конец 2022г.) есть проблемы в работе некоторых плагинов для ldap. Необходимо установить mediawiki:1.38.5 и PluggableAuth с ветки REL1_37.
Настройка ldap описана в файле `ldap.json`
