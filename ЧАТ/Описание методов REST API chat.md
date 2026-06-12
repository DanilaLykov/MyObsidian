

СТРУКТУРА БАЗЫ ДАННЫХ

  
chats
- id
- created
- entity_id
- status (1,0)

messages
- id
- author_uid 
- text
- created
- chat_id
- status   // 1 - , 2, 3

chat_members
- id
- chat_id
- uid

  

# Панель администратора

  
- Пермишн "administer_chat" (может подключиться к любому чату)

- Страница /admin/content/ae_chat  (доступна только по пермишну)

- Вывести страницу со списком чатов

  

  

##########################################

# Чат с поддержкой

  

Хранится в базе с adv_id объявления 0.  Пользователи с правом chat_support могут просматривать все чаты с поддержкой. Пользователь с соотв. правом может подключиться к любому чату, нажав на кнопку "подключиться". то помимо отправки сообщения от него, он должен добавиться в список членов чата.

  
- страница admin/content/ae_chat_support#open 
- страница admin/content/ae_chat_support#my
- страница admin/content/ae_chat_support#closed  
  выводятся все чаты по поддержке, отсортированными по дате последнего сообщения
- На странице со списком чатов нужно добавить кнопку (Написать в поддержку)
- метод для подключения к чату join_chat

  

###########################################



  
##########################################

# API методы

## get_messages

Возвращает 10 последних сообщений ранее last_message_id, в случае если last_message_id не указан, то возвращает последние

Параметры:

```
- chat_id
- last_message_id
```

Ответ:

```json
{
	"error": "Текст ошибки",
	"result": 
		"messages": [
			{
				"id": 45,
				"author_uid": 5,
				"text": "sdfdsf sdfsdfsdfsdf",
				"created": "15.03.2023",
				"chat_id": 59,
				"status": 1,
				"adv": {
					"id": 45,
					"title": "Шестерня ведущая",
					"img": "[Http://adress_img](Http://adress_img)",
					"author": {
						"uid": 423,
						"name": "Сергей",
						"avatar": "http://sdfsdsdfsdf.jpg",
						"avatar_bgcolor": "#980987",
						"avatar_letter": "C",
						"last_online": "2024-05-12 22:34"
					}  
				}
			},
			{
				"id": 45,
				"author_uid": 5,
				"text": "sdfdsf sdfsdfsdfsdf",
				"created": "15.03.2023",
				"chat_id": 59,
				"status": 1,
				"adv": {
					"id": 45,
					"title": "Шестерня ведущая",
					"img": "[Http://adress_img](Http://adress_img)",
					"author": {
						"uid": 423,
						"name": "Сергей",
						"avatar": "http://sdfsdsdfsdf.jpg",
						"avatar_bgcolor": "#980987",
						"avatar_letter": "C",
						"last_online": "2024-05-12 22:34"
					}  
				}
			},
		]
}
```

## get_chats

Возвращает все действующие чаты пользователя 

Параметры:

```
- uid // не обязательный, по умолчанию current_user
- status // не обязательный, по умолчанию = -1 (чаты со всеми статусами)
- adv // не обязательны, по умолчанию -1 (чаты по всем объявлениям)
- my // не обязательный, по умолчанию true
- count_members // не обязательный, по умолчанию = -1 (любое к-во участников) 
```

Возвращает:

``` json
{
	"error": "Текст ошибки",
	"result": [
		{
			"id": 34,
			"created": "2024-02-12 21:30", 
			"adv_id": 45,
			"status": 1,
			"can_join": True,
			"last_message": "Текст последнего сообщения",
			"last_message_date": "2024-02-12 21:30", 
			"last_message_status": 1,
			"members": [
					{
						 "uid": 423,
						 "current_user": true,
						 "name": "Сергей",
						 "avatar": "http://sdfsdsdfsdf.jpg",
						 "avatar_bgcolor": "#980987",
						 "avatar_letter": "C"
					},
					{
						 "uid": 424,
						 "current_user": false,
						 "name": "Сергей",
						 "avatar": "http://sdfsdsdfsdf.jpg",
						 "avatar_bgcolor": "#980987",
						 "avatar_letter": "C"
				   }
			],
			"adv": {
				"id": 45,
				"title": "werwer ererwerer ewrewrew",
				"img": "http://adress_img.jpg",
				"author": {
					"uid": 423,
					"name": "Сергей",
					"avatar": "http://sdfsdsdfsdf.jpg",
					"avatar_bgcolor": "#980987",
					"avatar_letter": "C",
					"last_online": "2024-05-12 22:34"
				}  
			}
		},
		{
			"id": 34,
			"created": "2024-02-12 21:30", 
			"adv_id": 45,
			"status": 1,
			"can_join": True,
			"last_message": "Текст последнего сообщения",
			"last_message_date": "2024-02-12 21:30", 
			"last_message_status": 1,
			"members": [
					{
						 "uid": 423,
						 "current_user": true,
						 "name": "Сергей",
						 "avatar": "http://sdfsdsdfsdf.jpg",
						 "avatar_bgcolor": "#980987",
						 "avatar_letter": "C"
					},
					{
						 "uid": 424,
						 "current_user": false,
						 "name": "Сергей",
						 "avatar": "http://sdfsdsdfsdf.jpg",
						 "avatar_bgcolor": "#980987",
						 "avatar_letter": "C"
				   }
			],
			"adv": {
				"id": 45,
				"title": "werwer ererwerer ewrewrew",
				"img": "Http://adress_img.jpg",
				"author": {
					"uid": 423,
					"name": "Сергей",
					"avatar": "http://sdfsdsdfsdf.jpg",
					"avatar_bgcolor": "#980987",
					"avatar_letter": "C",
					"last_online": "2024-05-12 22:34"
				}  
			}
		}
	]
}
```

## get_chat

Возвращает чат по его id 

Параметры:

```
- chat_id
```

Возвращает:

```json
{
	"error": "Текст ошибки",
	"result": {
		"id": 34,
		"created": "2024-02-12 21:30", 
		"adv_id": 45,
		"status": 1,
		"can_join": True,
		"last_message": "Текст последнего сообщения",
		"last_message_date": "2024-02-12 21:30", 
		"last_message_status": 1,
		"members": [
			{
				 "uid": 423,
				 "current_user": true,
				 "name": "Сергей",
				 "avatar": "http://sdfsdsdfsdf.jpg",
				 "avatar_bgcolor": "#980987",
				 "avatar_letter": "C"
			},
			{
				 "uid": 424,
				 "current_user": false,
				 "name": "Сергей",
				 "avatar": "http://sdfsdsdfsdf.jpg",
				 "avatar_bgcolor": "#980987",
				 "avatar_letter": "C"
		   }
		],
		"adv": {
			"id": 45,
			"title": "werwer ererwerer ewrewrew",
			"img": "Http://adress_img.jpg",
			"author": {
				"uid": 423,
				"name": "Сергей",
				"avatar": "http://sdfsdsdfsdf.jpg",
				"avatar_bgcolor": "#980987",
				"avatar_letter": "C",
				"last_online": "2024-05-12 22:34"
			}  
		}
	}
}

```

## get_messenger_status

Возвращает информацию о статусе мессенджера для пользователя (сейчас нужно только для возвращения количества непрочитанных сообщений для бэйджа мессенджера)

Возвращает:

``` json
{
	"error": "Текст ошибки",
	"result": {
		"uid": 34,
		"new_messages": 1
	}          
}
```

## post_chat

Создает новый чат по объявлению, минимум из 2-х пользователей (автор объявления, и отправитель запроса).

Параметры:

```
- entity_id // может быть равен support, что обозначает чат с поддержкой
- uids // масив uid для дополнительных пользователей, не обязательно
```

Возвращает:

{

"error": "Текст ошибки",
"result": {

     "chat": {

          "id": 34,

         "created": "13.05.2023",

         "adv_id": 45,

          "status": 1, 

         "members": [

               {

                 "uid": 423,

                 "current_user": true,

                 "name": "Сергей",

                 "avatar": "[http://sdfsdsdfsdf](http://sdfsdsdfsdf)",

                 "avatar_bgcolor": "#980987",

                 "avatar_letter": "C"

               },

               {

                 "uid": 424,

                 "current_user": false,

                 "name": "Сергей",

                 "avatar": "[http://sdfsdsdfsdf](http://sdfsdsdfsdf)",

                 "avatar_bgcolor": "#980987",

                 "avatar_letter": "C"

               }

          ]

          "adv": {

                  "id": 45,

                  "title": "werwer ererwerer ewrewrew",

                  "img": "[Http://adress_img](Http://adress_img)",

                  "author": {

                             "uid": 423,

                             "name": "Сергей",

                             "avatar": "[http://sdfsdsdfsdf](http://sdfsdsdfsdf)",

                        "avatar_bgcolor": "#980987",

                        "avatar_letter": "C"

                            }  

                 }

            }

     }

}

  

  

  

  

## post_message  !!!!!  УСТАРЕВШИЙ, не работает

метод отправляет сообщение 

  

[http://chat.algusdev.ru/ae_chat_api/post_message](http://chat.algusdev.ru/ae_chat_api/post_message)

  

параметры: 

- author_uid

- text

- chat_id

  

возвращает:

{

"error": "Текст ошибки",

"result": {

           "id": 34,

           "author_uid": 15,

           "text": "yarykarky",

           "created": "2024-02-12 21:30",

           "chat_id": 5,

           "status": 1

  "adv": {

                  "id": 45,

                  "title": "werwer ererwerer ewrewrew",

                  "img": "[Http://adress_img](Http://adress_img)",

                  "author": {

                             "uid": 423,

                             "name": "Сергей",

                             "avatar": "[http://sdfsdsdfsdf](http://sdfsdsdfsdf)",

                        "avatar_bgcolor": "#980987",

                        "avatar_letter": "C"

                            }  

                 }

          }

}

  

  

## get_user

  

Возвращает информацию по пользователю

  

[http://chat.algusdev.ru/ae_chat_api/get_user](http://chat.algusdev.ru/ae_chat_api/get_user)

  

параметры:

- uid

  

возвращает:

  

{

"error": "Текст ошибки",

"result": {

           "uid": 34,

           "name": "Алексей" 

           "avatar": [https://agaga](https://agaga)

           "avatar_bgcolor": #12341

           "avatar_letter": "S"

           "last_online": 27.05.2023

          }

}

  

  

## get_users  

  

Возвращает информацию по пользователю

  

[http://chat.algusdev.ru/ae_chat_api/get_users](http://chat.algusdev.ru/ae_chat_api/get_users)

  

параметры:

- uids - массив [45, 34, 65]

  

возвращает:

  

{

"error": "Текст ошибки",

"result": {

           "uid": 34,

           "name": "Алексей" 

           "avatar": [https://agaga](https://agaga)

           "avatar_bgcolor": #12341

           "avatar_letter": "S"

           "last_online": 27.05.2023

          },

          {

           "uid": 34,

           "name": "Алексей" 

           "avatar": [https://agaga](https://agaga)

           "avatar_bgcolor": #12341

           "avatar_letter": "S"

           "last_online": 27.05.2023

          },

          {

           "uid": 34,

           "name": "Алексей" 

           "avatar": [https://agaga](https://agaga)

           "avatar_bgcolor": #12341

           "avatar_letter": "S"

           "last_online": 27.05.2023

          }

}

  

## join_chat

  

Добавляет текущего пользователя в указанный чат.

  

Параметры:

  

- chat_id

  

Возвращает объект чата

  

{

"error": "Текст ошибки",

"result": {

     "chat": {

          "id": 34,

         "created": "13.05.2023",

         "adv_id": 45,

          "status": 1, 

          "can_join": True,

          "last_message": "Текст последнего сообщения",

          "last_message_date": "2024-02-12 21:30", 

          "last_message_status": 1,

         "members": [

               {

                 "uid": 423,

                 "current_user": true,

                 "name": "Сергей",

                 "avatar": "[http://sdfsdsdfsdf](http://sdfsdsdfsdf)",

                 "avatar_bgcolor": "#980987",

                 "avatar_letter": "C"

               },

               {

                 "uid": 424,

                 "current_user": false,

                 "name": "Сергей",

                 "avatar": "[http://sdfsdsdfsdf](http://sdfsdsdfsdf)",

                 "avatar_bgcolor": "#980987",

                 "avatar_letter": "C"

               }

          ]

          "adv": {

                  "id": 45,

                  "title": "werwer ererwerer ewrewrew",

                  "img": "[Http://adress_img](Http://adress_img)",

                  "author": {

                             "uid": 423,

                             "name": "Сергей",

                             "avatar": "[http://sdfsdsdfsdf](http://sdfsdsdfsdf)",

                        "avatar_bgcolor": "#980987",

                        "avatar_letter": "C"

                            }  

                 }

            }

     }

}

  

  

  

  

  

#################################################

# План работ

- Создаем  таблицы по структуре

- на примитивном уровне реализуем окно просмотра чата пользователем (?chat_id=5&uid=5), где его собственные сообщения выделены

- сделать форму добавления сообщения с полями (chat_id, uid, text) она должна рассылать в сокеты и сохранять в базу данных 

  

  

- описываем методы API

- создаем ресурсы методов на пирмитивном уровне

- залить на хостинг, в т.ч. базу, чтобы можно было проверить работу методов (настройка вебсокетов необязательно)

-поизучать ajax jquery

  

  

- создать тип материала unit_technic добавить несколько полей (картинку)

- создать страницу со списком объявлений (views)

- создаем модуль ae_adv_messenger

- создаем страницу конфигурации (форма) 

    - Тип материала объявления   (строка, в которой нужно указать, какой тип материала считаь объявлением)

- на сохранение формы делаем валидацию - проверка наличия такого типа материала (можно не делать)

  сохраняем кнфигурацию.

- перенести все таблицы кроме users в drupal

- изучить rest api  в drupal  и начать делать методы, /adv_msg_api/[название метода]  

- с помощью hook_preprocess_node вывести кнопку "Начать чат" на странице и на тизере объявления

- все авторизованным пользователям подключить скрипт js (с помощью hook preprocess 4 способ [https://drupal.ru/docs/chastye-voprosy/dobavit-kastomnyy-js-kod-na-sayt-razlichnye-metriki-i-dr](https://drupal.ru/docs/chastye-voprosy/dobavit-kastomnyy-js-kod-na-sayt-razlichnye-metriki-i-dr))

  

- Довести описание API до идеала (дописать метод отправки)

- Реализовать API в полном соответствии

- Проверить аутентификацию по Кукам

  

  

  

  

 Дизайнеру:

- В кокшке со списком чатов добавить сверху кнопку "Написать в поддержку"

- В окошке со списком чатов показать пример чата с поддержкой ()

- Иконка для чата с поддержкой

- Название чата сверху, пользователь с аватаркой, последним сообщением

- На карточке чата имена участников с датой активности списком

- оформить кнопку "подключиться"

  

  

Верстальщику:

- Напсать скрипт, который выводит закладки, и выводит содержимое для страниц

---- страница admin/content/ae_chat_support#open 

---- страница admin/content/ae_chat_support#my

---- страница admin/content/ae_chat_support#closed  

  

  

  

  

МНЕ

- JS-Скрипт, для вставки на сайт 

-  API с методами создания всех сущносттей и получения

- Придумать авторизацию

  

  

Доработки от 28.06.2023

- Если пользователь не авторизован, то кнопка должна открывать модальное окно со ссылкой на вход/рег-ю. Если пользователь авторизован, но не имеет  прав на чат, то не выводим кнопку.

- Зарегать по ползователю из каждой роли, и составить список этих пользователей, паролей

-

  

  

  

  

  

Модальное окно:

- Заголовок: "Авторизуйетсь чтобы написать сообщение"

- Текст: 

Присать сообщения по объявлениям могут только авторизованные пользователи. Войдите под своей учетной записью, либо зарегистрируйтесь.

- Кнопка: ВОЙТИ

- ссылка: зарегистрироваться