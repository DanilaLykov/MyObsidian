
WebSocket-сервер организован посредством библиотеки PHP Ratchet. 

## На сервер

### send_message -  Отправка сообщения в чат

```json
{
	'type': 'send_message',
	'data': {
        'content': 'Текст сообщения',
        'chat_id': 45
	}
}
```
### typing_message - Набор текста

```json
{
    'type': 'typing_message',
    'data': {
         'chat_id': 19
    }
}
```
### stop_typing_message - Прекратил набор текста

```json
{
    'type': 'stop_typing_message',
    'data': {
         'chat_id': 19
    }
}
```
### read_message - Сообщение прочитано

```json
{
    'type': 'read_message',
    'data': {
         'chat_id': 24,
         'message_id': 234  
    }

}
```


## На фронт

### send_message - Отправка сообщений

```json
{
    'type': 'send_message',
    'data': {
		 'message_id': 220,
		 'text': 'hellomir',
		 'author_uid': 1,
		 'created': '2023-07-17 15:47:30',
		 'chat_id': 215,
		 'status': 1
     }
}
```

### typing_message - Пользователь набирает сообщение

```json
{
	'type': 'typing_message',
	'data': {
		 'chat_id': 19,
		 'uid': 18
	}    
}
```

### stop_typing_message - Пользователь преестал набирать сообщение

```json
{
	'type': 'stop_typing_message',
	'data': {
		 'chat_id': 19,
		 'uid': 18
	}    
}
```

### read_message - Сообщение прочитано

```json
{
	'type': 'read_message',
	 'data': {
		 'message_id': 456,
		 'chat_id': 24
	}
}
```

### online_user - Пользователь появился онлайн

```json
{
	 'type': 'online_user'
	 'data': {
		 'uid': 45,
	 }
}
```

### offline_user - Пользователь отсоединился

``` json
{
	 'type': 'offline_user'
	 'data': {
		 'uid': 45,
		 'last_online': "2023-07-17 15:47:30"
	 }
}
```

### error - Сообщение об ошибке на сервере

```json
{
	'type': 'error'
	'data': {
		 'error_msg': 'Error',
		 'error_code': 400
	}
}
```

### unread_chats  - Изменилось количество непрочитанных чатов

Отправляется, когда появляется новый непрочитанный чат, либо наоборот прочитывается чат этим же пользователем. 

```json
{
    'type': 'unread_chats',
     'data': {
         'count_unread_chats': 4
    }
}
```
  
### delivered_message - Сообщение доставлено

Сообщает о том, что некоторое сообщение было доставлено аппоненту. Отправляется в случаях когда собеседнику было отправлено по вебсокету сообщение, либо собеседник открыл чат и увидел все сообщения.

```json
{
	'type': 'delivered_message',
	 'data': {
		 'message_id': 456,
		 'chat_id': 24
	}
}
```
