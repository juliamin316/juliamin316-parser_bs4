# juliamin316-parser_bs4 
Этот проект представляет собой парсер продуктов с веб-страницы, написанный на Python. Код собирает информацию о товарах, включая артикул (SKU), название, ссылку и цену, и сохраняет её в CSV-файл. Код парсит все товары одной категории с сайта магазина строительных материалов https://glavsnab.net/. В качестве примера код реализован на разделе "Садовая техника". 
# Структура проекта
1. main.py: Основной файл для запуска парсера.
2. model.py: Содержит dataclass для сохранения информации.
3. otvet.csv: Файл, в который сохраняются результаты парсинга.
# Требования 
Для запуска проекта вам понадобится Python версии 3.8 и выше, а также следующие библиотеки: requests, beautifulsoup4 
# Как использовать
1. Склонируйте репозиторий или скачайте исходный код.
2. Установите необходимые библиотеки
3. Убедитесь, что файл model.py находится в той же папке, что и основной скрипт main.py.
4. (Опционально) В файле main.py измените значение параметра url на нужный вам URL, а также задайте максимальное количество товаров для парсинга (max_item). (можно оставить все как есть и код спарсит раздел садовой техники, данный шаг нежен, если надо спарсить другой раздел сайта)
5. Запустите скрипт
6. После завершения работы программы откройте файл otvet.csv, чтобы увидеть результаты.
# Настройка параметров 
1. В параметре url указывается адрес страницы, с которой будет происходить парсинг, например: 
url="https://glavsnab.net/tovary-dlya-dachi-i-sada/tekhnika-dlya-sada.html?limit=100
2. Параметр max_item задаёт максимальное число товаров, которые будут обработаны, например:
max_item=653
# Структура CSV-файла
Файл otvet.csv содержит следующие колонки:
1. sku: Артикул товара.
2. name: Название товара.
3. link: Ссылка на страницу товара.
4. price: Цена товара (если она отсутствует, указывается "По запросу").
