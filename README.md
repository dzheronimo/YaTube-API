# О чем проект

API социальной сети **yatube***


# Как запустить проект:

1. Клонировать репозиторий и перейти в него в командной строке:
```
git clone https://github.com/dzheronimo/YaTube-API.git**
```
```
cd YaTube-API
```

2. Cоздать и активировать виртуальное окружение:
```
python3 -m venv env
```
```
source env/bin/activate
```

3. Установить зависимости из файла requirements.txt:
```
python3 -m pip install --upgrade pip
```
```
pip install -r requirements.txt
```
4. Выполнить миграции:
```
python3 manage.py migrate
```
5. Запустить проект:
```
python3 manage.py runserver
```

## Примеры запросов

1. GET /api/v1/posts/ - Получаем все существующие посты, выдача поделена пагинацией
```
{
  "count": 123,
  "next": "http://api.example.org/accounts/?offset=400&limit=100",
  "previous": "http://api.example.org/accounts/?offset=200&limit=100",
  "results": [
    {
      "id": 0,
      "author": "string",
      "text": "string",
      "pub_date": "2021-10-14T20:41:29.648Z",
      "image": "string",
      "group": 0
    }
  ]
}
```

2. POST /api/v1/posts/ - Создаем пост
```
{
  "text": "string",
  "image": "string",
  "group": 0
}
```
