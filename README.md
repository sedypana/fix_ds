<h1 align="center">Fix_Bat (обход блокировки Discord'а и Youtube'а)</h1>

> [!NOTE]  
> Данный репозиторий - **некоммерческая** копия [оригинального репозитория](https://github.com/bol-van/zapret).

## Преимущества
- [x] Быстрый и удобный обход блокировки Youtube and Discord
- [x] Без вирусных программ
- [x] Возможность использовать одновременно все запрещенные программы, запустив только 1 .bat файл

## Структура репозитория
[](https://avatars.dzeninfra.ru/get-zen_doc/271828/pub_670e1e869f99bb0f3f64d3cc_678e53f871feae4844541b60/scale_1200)
## Guides
### Windows
> [!IMPORTANT]  
> Если всё еще не скачан, то скачайте последний [релиз](https://github.com/Flowseal/zapret-discord-youtube/releases), разархивируйте в отдельную папку.

Запустите **от имени администратора** то, что вам нужно:
- **`discord.bat`** - запустить обход дискорда.
- **`general.bat`** - запустить обход дискорда и ютуба.
  * Если обход не работает, пробуйте по порядку **`general (ALT ..).bat`** (также можете проверить стратегию на **МГТС**)
###
- **`service_install.bat`** - установить на автозапуск (в сервисы) любую стратегию из этого репозитория (стратегия **НЕ** должна начинаться со слова `service`)
###
- **`service_goodbye_discord.bat`** - запустить, если вы используете **СЕРВИС goodbyedpi**, и хотите, чтобы zapret обходил **только discord**.
  * **ВНИМАНИЕ**: Запускать ПОСЛЕ создания сервиса goodbyedpi. Первый раз goodbyedpi может вылететь - просто перезапустите устройство!
###
- **`service_remove.bat`** - остановить и удалить сервисы выше

## Решение проблем

- Проверьте, запускаете ли вы файлы от **ИМЕНИ АДМИНИСТРАТОРА**
- Не запускаются bat файлы? Попробуйте найти ответ здесь: https://github.com/Flowseal/zapret-discord-youtube/issues/522
- <p style="text-align: left;">
    <img src="https://cdn-icons-png.flaticon.com/16/3670/3670147.png" alt="discord" style="vertical-align: middle;"/>
    Не работает <strong>Youtube</strong>? Попробуйте найти ответ здесь - 
    <a href="https://github.com/Flowseal/zapret-discord-youtube/discussions/251">Обсуждение YouTube</a>
  </p>
- <p style="text-align: left;">
    <img src="https://cdn-icons-png.flaticon.com/16/906/906361.png" alt="discord" style="vertical-align: middle;"/>
    Не работает <strong>Discord</strong>? Попробуйте найти ответ здесь - 
    <a href="https://github.com/Flowseal/zapret-discord-youtube/discussions/252">Обсуждение Discord</a>
  </p>
##
- Не работает вместе с **VPN**? Отключите функцию **TUN** (Tunneling) в настройках VPN.
- Не работает **`service_goodbye_discord`**? Удостовертесь, что сервис goodbyedpi запущен и имеет название GoodbyeDPI. После снова запустите `service_goodbye_discord.bat` и перезапустите устройство.
- Попробуйте обновить бинарники с оригинального репозитория.

### Остановка и удаление обхода
Для этого запустите **`service_remove.bat`**.
- Если WinDivert так и не удалился, узнайте его название с помощью команды `driverquery | find "Divert"` в cmd, а затем удалите данными командами (заместо WinDivert введите название, которые вы узнали):
```
sc stop WinDivert
sc delete WinDivert
```

### Добавление дополнительных адресов заблокированных сайтов 
- Список можно дополнить используя `list-general.txt` (для файлов `general`) и в список `list-discord` (для файлов `discord`).
> [!IMPORTANT]  
> После добавления сервис нужно перезапустить.
