# vkui-connect-promise

Пакет для интеграции VK Apps-приложений с официальными клиентами VK для iOS, Android и Web с шиной событий на промисах.

Подробнее о промисах можно почитать тут:
- https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise 🇬🇧/🇷🇺
- http://learn.javascript.ru/promise 🇷🇺


## Подключение
```js
import connect from '@vkontakte/vkui-connect-promise';
```

## Пример использования
Теперь нет необходимости отдельно подписываться на обработку событий, а можно работать с событиями VK Connect как с нативными промисами, например так:
```js
// Отправляет событие клиенту
connect.send('VKWebAppInit', {})
  .then(data => handleResponse(data))
  .catch(error => handleError(error));
```