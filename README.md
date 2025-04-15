# Backend для AB Dashboard

Этот репозиторий содержит бэкенд часть для [AB Dashboard](https://github.com/Yodzhik/ab-dashboard) - веб-панели управления, построенной на React.


## 📦 Установка

1. Клонируйте репозиторий:
```bash
git clone https://github.com/Yodzhik/backend-for-ab-dashboard.git
```

2. Установите зависимости:
```bash
npm install
```

## 🛠️ Запуск

Запустите сервер:
```bash
npm start
```

## 📡 API Endpoints

```
GET     /sites                Получить список сайтов
GET     /sites/[id]           Получить сайт по ID
GET     /tests                Получить список тестов
GET     /tests/[id]           Получить тест по ID
```

## 📊 Типы данных

```typescript
enum Type {
  CLASSIC = "CLASSIC",
  SERVER_SIDE = "SERVER_SIDE",
  MVT = "MVT"
}

enum Status {
  DRAFT = "DRAFT",
  ONLINE = "ONLINE",
  PAUSED = "PAUSED",
  STOPPED = "STOPPED",
}

interface Site {
  id: number;
  url: string;
}

interface Test {
  id: number;
  name: string;
  type: Type;
  status: Status;
  siteId: number;
}
```

## 🔗 Связанные репозитории

- [Фронтенд часть](https://github.com/Yodzhik/ab-dashboard)
