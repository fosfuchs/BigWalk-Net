# BigWalk Net

Мод для Big Walk: свой хост по IP + панель подключения в игре. Без лобби, без Steam-сети, сервер можно держать headless в Docker.

## Установка клиента
    Linux:    ./install.sh                
    Windows:  install.bat                 
    удалить:  uninstall.sh / uninstall.bat

В игре - панель слева сверху: IP сервера + порт -> «Подключиться». Скрыть/вернуть - «Скрыть панель» / кнопка BW.

## Установка сервера (Docker)
    ./server.sh install --copy-from "$HOME/.local/share/Steam/steamapps/common/Big Walk"
    ./server.sh up
    ./server.sh status

настройки сервера server.conf: GAME_DIR PORT PLAYER WORLD PASSWORD MEM -> после правки ./server.sh restart.

    ./server.sh world-list | world-delete ИМЯ | world-delete --all | reset | uninstall

**Я не проверял, но по поведению если вы сами захостите мир и подключитесь напрямую, то тоже самое будет, ненадо будет даже пак с сервером качать**


## ОГРАНИЧЕНИЯ
- net_join.txt на клиенте не создавать - это сугубо мое, а вырезать не хочу.
- клиент хоста ограничен по фпсу(60) дабы сильно не нагружать.

## Для чего это все?
Я хз друг попросил я сделал, сам мод на публику, врдуг ктото еще хочет
