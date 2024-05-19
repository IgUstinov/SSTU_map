# SSTU_map
Интерактивная карта Саратовского Государственного Технического Университета имени Ю.А. Гагарина. Способствует изучению местности вуза, а также последующего закрепления знаний посредством интерактивного тестирования

# Установка

1-й способ - скачать архив denwer, распаковать 
Запустить denwer зайдя в распакованный файл (denwer - Run.exe), подождать запуска 
В браузере открыть карту http://localhost/map 

______________________________________________
2-й способ (Страницы и БД отдельно) 
Если у вас имеется denwer:
Необходимо скачать карту и положить её в home-localhost-www
Базу данных необходимо скачать. Открыть localhost/tools/phpmyadmin нажать импорт и выбрать базу данных для загрузки
В самом проекте в файле test_new.php нужно заменить:
В строчках 54 и 529 - имя пользователя (который есть в вашем phpmyadmin. Должен иметь абсолютно все права)
В строчках 55 и 530 - пароль к этому пользователю

После включения denwer
Чтобы открыть карту нужно прописать http://localhost/map
Для проверки, что база данных работает, нужно на странице http://localhost/map/test_new.php нажать "Показать таблицу"
Если она после нажатия показывается, то всё работает успешно
Если нет, то возможные ошибки:
Старая версия php 
Тогда необходимо заменить во всех методах, где используется "mysqli" на "mysql" (С помощью CTRL+R можно сделать замену во всём файле)

Также в строчках 61, 65, 72, 536, 540, 542 
необходимо либо поменять аргументы в методах местами, либо удалить из аргументов переменную $checkconnect
