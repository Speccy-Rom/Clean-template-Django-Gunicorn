* 23.11.2020 R.Spiridonov aka Speccy-Rom

### Разработал чистый шаблон Django проекта, с которым можно быстро начать разработку. В шаблон входит конфиг Systemd, nginx, gunicorn.

* Установка представляет собой просто указание Python интерпретатора и названия домена, запустите:

./install.sh

* В конфиге Django заполните настройки базы данных (src/config/settings.py).
* Посмотреть статус gunicorn демона:

sudo systemctl status gunicorn

* Логи gunicorn'а лежат в gunicorn/access.log и gunicorn/error.log.
* После изменения systemd конфига надо перечитать его и затем перезапустить юнит:

sudo systemctl daemon-reload
sudo systemctl restart gunicorn

#####Пользуйтесь.....