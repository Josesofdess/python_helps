

**event.original_update**


**[Для Приватных Чатов (ЛС)](https://github.com/Josesofdess/python_helps/blob/main/telethon/event.original_update.md#%D0%B4%D0%BB%D1%8F-%D0%BF%D1%80%D0%B8%D0%B2%D0%B0%D1%82%D0%BD%D1%8B%D1%85-%D1%87%D0%B0%D1%82%D0%BE%D0%B2-%D0%BB%D1%81)** 
Ссылки на данные методы.
- **https://core.telegram.org/constructor/message** 
- **https://core.telegram.org/constructor/updateNewMessage**

- **https://tl.telethon.dev/constructors/message.html**
- **https://tl.telethon.dev/constructors/update_new_message.html**

**[Для Групповых Чатов (Канал)](https://github.com/Josesofdess/python_helps/blob/main/telethon/event.original_update.md#%D0%B4%D0%BB%D1%8F-%D0%BF%D1%80%D0%B8%D0%B2%D0%B0%D1%82%D0%BD%D1%8B%D1%85-%D1%87%D0%B0%D1%82%D0%BE%D0%B2-%D0%BB%D1%81)**
Ссылки на данные методы.
- **https://core.telegram.org/constructor/message** 
- **https://core.telegram.org/constructor/updateNewChannelMessage**

- **https://tl.telethon.dev/constructors/message.html**
- **https://tl.telethon.dev/constructors/update_new_channel_message.html**

# Для Приватных Чатов (ЛС)
```python
from telethon import events
@client.on(events.NewMessage)
async def ss(event):
	#print("00 ", event.stringify())
	print("0 ", event.original_update)
	print("1 ", event.original_update.pts) #Новое количество действий в окне сообщения
	print("2 ", event.original_update.pts_count) #Количество сгенерированных событий
	print("3 ", event.original_update.message.id) #	ID сообщения
	print("4 ", event.original_update.message.to_id) # ID чата, в который было отправлено сообщение
	print("5 ", event.original_update.message.to_id.user_id) # ID чата, в который было отправлено сообщение
	print("6 ", event.original_update.message.date)# Дата сообщения
	print("7 ", event.original_update.message.date.tzinfo)# timezone
	print("8 ", event.original_update.message.message) # текст сообщения
	print("9 ", event.original_update.message.out)  # Является ли сообщение исходящим
	print("10 ", event.original_update.message.mentioned)  # Упоминались ли мы в сообщении
	print("11 ", event.original_update.message.media_unread)  # Есть ли в этом сообщении непрочитанные упоминания
	print("12 ", event.original_update.message.silent)  # Если true, сообщение является беззвучным, уведомления запускаться не должны.
	print("13 ", event.original_update.message.post)  # Это сообщение канала
	print("14 ", event.original_update.message.from_scheduled)  # Является ли это запланированной публикацией
	print("15 ", event.original_update.message.legacy)  # 	Это устаревшее сообщение: его нужно переписать с новым слоем.
	print("16 ", event.original_update.message.edit_hide)  # Должно ли сообщение отображаться как неизмененное для пользователя, даже если присутствует дата редактирования
	print("17 ", event.original_update.message.from_id)  # ID отправителя сообщения
	print("18 ", event.original_update.message.fwd_from)  # Информация о перенаправленных сообщениях
	print("19 ", event.original_update.message.via_bot_id)  # ID встроенного бота, создавшего сообщение
	print("20 ", event.original_update.message.reply_to_msg_id) #ID сообщения, на которое это сообщение отвечает
	print("21 ", event.original_update.message.media)  # Вложение media
	print("22 ", event.original_update.message.reply_markup)  #Разметка ответа (боты / встроенные клавиатуры)
	print("23 ", event.original_update.message.entities)  #"Сущности" сообщения для стилизованного текста #https://core.telegram.org/api/entities
	print("24 ", event.original_update.message.views)  #Количество просмотров сообщений на канале
	print("25 ", event.original_update.message.edit_date)  #Дата последнего редактирования этого сообщения
	print("26 ", event.original_update.message.post_author)  #Имя автора сообщения для сообщений на канале (с включенными подписями)
	print("27 ", event.original_update.message.grouped_id)  #Несколько мультимедийных сообщений, отправленных с использованием messages.sendMultiMedia с одним и тем же сгруппированным идентификатором, указывают на альбом
	print("28 ", event.original_update.message.restriction_reason)  # Содержит причину, по которой доступ к этому сообщению должен быть ограничен.
```

# Для Групповых Чатов (Канал)
```python
from telethon import event
@client.on(events.NewMessage)
async def ss(event):
	#print("00 ", event.stringify())
	print("0 ", event.original_update)
	print("1 ", event.original_update.pts) #Новое количество действий в окне сообщения
	print("2 ", event.original_update.pts_count) #Количество сгенерированных событий
	print("3 ", event.original_update.message.id) #	ID сообщения
	print("4 ", event.original_update.message.to_id) # ID Канала, в который было отправлено сообщение
	print("5 ", event.original_update.message.to_id.channel_id) # ID Канала, в который было отправлено сообщение
	print("6 ", event.original_update.message.date)# Дата сообщения
	print("7 ", event.original_update.message.date.tzinfo)# timezone
	print("8 ", event.original_update.message.message) # текст сообщения
	print("9 ", event.original_update.message.out)  # Является ли сообщение исходящим
	print("10 ", event.original_update.message.mentioned)  # Упоминались ли мы в сообщении
	print("11 ", event.original_update.message.media_unread)  # Есть ли в этом сообщении непрочитанные упоминания
	print("12 ", event.original_update.message.silent)  # Если true, сообщение является беззвучным, уведомления запускаться не должны.
	print("13 ", event.original_update.message.post)  # Это сообщение канала
	print("14 ", event.original_update.message.from_scheduled)  # Является ли это запланированной публикацией
	print("15 ", event.original_update.message.legacy)  # 	Это устаревшее сообщение: его нужно переписать с новым слоем.
	print("16 ", event.original_update.message.edit_hide)  # Должно ли сообщение отображаться как неизмененное для пользователя, даже если присутствует дата редактирования
	print("17 ", event.original_update.message.from_id)  # ID отправителя сообщения
	print("18 ", event.original_update.message.fwd_from)  # Информация о перенаправленных сообщениях
	print("19 ", event.original_update.message.via_bot_id)  # ID встроенного бота, создавшего сообщение
	print("20 ", event.original_update.message.reply_to_msg_id) #ID сообщения, на которое это сообщение отвечает
	print("21 ", event.original_update.message.media)  # Вложение media
	print("22 ", event.original_update.message.reply_markup)  #Разметка ответа (боты / встроенные клавиатуры)
	print("23 ", event.original_update.message.entities)  #"Сущности" сообщения для стилизованного текста #https://core.telegram.org/api/entities
	print("24 ", event.original_update.message.views)  #Количество просмотров сообщений на канале
	print("25 ", event.original_update.message.edit_date)  #Дата последнего редактирования этого сообщения
	print("26 ", event.original_update.message.post_author)  #Имя автора сообщения для сообщений на канале (с включенными подписями)
	print("27 ", event.original_update.message.grouped_id)  #Несколько мультимедийных сообщений, отправленных с использованием messages.sendMultiMedia с одним и тем же сгруппированным идентификатором, указывают на альбом
	print("28 ", event.original_update.message.restriction_reason)  # Содержит причину, по которой доступ к этому сообщению должен быть ограничен```

