# Развертывание мониторинг стека на astra linux 
### Простой способ
запускаем `bash script.sh` . Скрипт распаковывает и устанавливает grafana, prometheus, nodeexporter. Устанавливает сервисы-демоны из каталога `services`. 

*установка происходит с конфигурацией для мониторинга в рамках локалхоста!*

### Добавляем дашборды в графану
Из каталога `grafana-dashboards`. 

Если добавляем в каталог что-то своё запускаем команду `sed -i '0,/"id": .*/{s/"id": .*/"id": null,/}' grafana-dashboards/*.json` для подмены `id` импортированного дашборда на `null`.

