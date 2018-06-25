# Express
 1. Создание папки с текущей датой и временем с помощью командной строки, установка линтера:
mkdir $(date +%Y%m%d_%H%M%S) && cd $_ && yarn init -y
bash < (curl -s https://kodaktor.ru/g/eslint_exec)
atom .

 2. Установка зависимостей:
yarn add express pug	axios	
yarn add --dev nodemon

 3. Добавление скрипта в package.json:
 "scripts": {
    "start": "nodemon"
  }
  
 4.Создание папки src и файла index.js с нужным содержанием
 
 5.Создание папки views и файла list.pug с шаблоном
 
 6. Импорт метода get из зависимости axios:
const { get } = require('axios');
const URL = 'https://kodaktor.ru/j/users';

и создание асинхронного обработчика маршрута users:
.get(/users/, async r => { 
      const { data: { users: items } } = await get(URL);
      r.res.render('list', {title: 'Login list', items});
   })
   
 7. Результат работы прослушивания порта 4321  в браузере:
 ![alt text](https://github.com/nastyandreeva/Express/blob/master/express.PNG)
