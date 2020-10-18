

**[Для Приватных Чатов (ЛС)](https://github.com/Josesofdess/python_helps/new/main/telethon#%D0%B4%D0%BB%D1%8F-%D0%BF%D1%80%D0%B8%D0%B2%D0%B0%D1%82%D0%BD%D1%8B%D1%85-%D1%87%D0%B0%D1%82%D0%BE%D0%B2-%D0%BB%D1%81)**

**[Для Групповых Чатов (Канал)](https://github.com/Josesofdess/python_helps/new/main/telethon#%D0%B4%D0%BB%D1%8F-%D0%B3%D1%80%D1%83%D0%BF%D0%BF%D0%BE%D0%B2%D1%8B%D1%85-%D1%87%D0%B0%D1%82%D0%BE%D0%B2-%D0%BA%D0%B0%D0%BD%D0%B0%D0%BB)**

**Ссылки на данные методы.**

- https://tl.telethon.dev/constructors/photo.html
- https://tl.telethon.dev/constructors/photo_stripped_size.html
- https://tl.telethon.dev/types/photo_size.html
- https://tl.telethon.dev/constructors/message_media_photo.html
- https://tl.telethon.dev/constructors/message.html
- https://tl.telethon.dev/constructors/update_new_message.html
- https://core.telegram.org/constructor/photo
- https://core.telegram.org/constructor/photoStrippedSize
- https://core.telegram.org/constructor/photoSize
- https://core.telegram.org/constructor/messageMediaPhoto
- https://core.telegram.org/constructor/message
- https://core.telegram.org/constructor/updateNewMessage



# Для Приватных Чатов (ЛС)
```python
@client.on(events.NewMessage)
async def ss(event):
	#print("00 ", event.stringify())
	print("0 ", event.original_update)
	print("1 ", event.original_update.pts) #Новое количество действий в окне сообщения
	print("2 ", event.original_update.pts_count) #Количество сгенерированных событий
	print("3 ", event.original_update.message.id) #	ID сообщения
	print("4 ", event.original_update.message.to_id) # ID Канала, в который было отправлено сообщение
	print("5 ", event.original_update.message.to_id.user_id) # ID Канала, в который было отправлено сообщение
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

	# https://tl.telethon.dev/constructors/photo.html
	# https://core.telegram.org/constructor/photo
	print("21 ", event.original_update.message.media)
	print("22 ", event.original_update.message.media.photo)
	print("23 ", event.original_update.message.media.photo.id) # ID
	print("24 ", event.original_update.message.media.photo.access_hash) # Хеш доступа
	print("25 ", event.original_update.message.media.photo.file_reference)  # ссылка на файл
	print("26 ", event.original_update.message.media.photo.date)  # Дата загрузки
	print("27 ", event.original_update.message.media.photo.date.tzinfo)  # Дата загрузки

	#https://tl.telethon.dev/constructors/photo_stripped_size.html
	#https://core.telegram.org/constructor/photoStrippedSize
	print("28 ", event.original_update.message.media.photo.sizes[0])  # Вложение media
	print("29 ", event.original_update.message.media.photo.sizes[0].type)
	print("30 ", event.original_update.message.media.photo.sizes[0].bytes)# Вложение media

	#https://tl.telethon.dev/types/photo_size.html
	#https://core.telegram.org/constructor/photoSize
	print("31 ", event.original_update.message.media.photo.sizes[1])
	print("32 ", event.original_update.message.media.photo.sizes[1].type) #Тип эскиза
	print("33 ", event.original_update.message.media.photo.sizes[1].location) # Расположение файла
	print("34 ", event.original_update.message.media.photo.sizes[1].location.volume_id) # Вложение media
	print("35 ", event.original_update.message.media.photo.sizes[1].location.local_id) # Вложение media
	print("36 ", event.original_update.message.media.photo.sizes[1].w) # Ширина изображения
	print("37 ", event.original_update.message.media.photo.sizes[1].h) # Высота изображения
	print("38 ", event.original_update.message.media.photo.sizes[1].size) # Размер файла

	# https://tl.telethon.dev/types/photo_size.html
	# https://core.telegram.org/constructor/photoSize
	print("39 ", event.original_update.message.media.photo.sizes[2])
	print("40 ", event.original_update.message.media.photo.sizes[2].type) #Тип эскиза
	print("41 ", event.original_update.message.media.photo.sizes[2].location) # Расположение файла
	print("42 ", event.original_update.message.media.photo.sizes[2].location.volume_id) # Вложение media
	print("43 ", event.original_update.message.media.photo.sizes[2].location.local_id) # Вложение media
	print("44 ", event.original_update.message.media.photo.sizes[2].w) # Ширина изображения
	print("45 ", event.original_update.message.media.photo.sizes[2].h) # Высота изображения
	print("46 ", event.original_update.message.media.photo.sizes[2].size) # Размер файла

	# https://tl.telethon.dev/types/photo_size.html
	# https://core.telegram.org/constructor/photoSize
	print("47 ", event.original_update.message.media.photo.sizes[3])
	print("48 ", event.original_update.message.media.photo.sizes[3].type) #Тип эскиза
	print("49 ", event.original_update.message.media.photo.sizes[3].location) # Расположение файла
	print("50 ", event.original_update.message.media.photo.sizes[3].location.volume_id)  # Вложение media
	print("51 ", event.original_update.message.media.photo.sizes[3].location.local_id)  # Вложение media
	print("52 ", event.original_update.message.media.photo.sizes[3].w) # Ширина изображения
	print("53 ", event.original_update.message.media.photo.sizes[3].h) # Высота изображения
	print("54 ", event.original_update.message.media.photo.sizes[3].size)  # Вложение media

	# https://tl.telethon.dev/constructors/photo.html
	# https://core.telegram.org/constructor/photo
	print("55 ", event.original_update.message.media.photo.dc_id)  # DC ID для загрузки
	print("56 ", event.original_update.message.media.photo.has_stickers)  # Вложение media
	print("57 ", event.original_update.message.media.photo.video_sizes)  # Вложение media

	#https://tl.telethon.dev/constructors/message_media_photo.html
	#https://core.telegram.org/constructor/messageMediaPhoto
	print("58 ", event.original_update.message.media.ttl_seconds) # Время жить в секундах самоуничтожающегося фото

	print("59 ", event.original_update.message.reply_markup)  #Разметка ответа (боты / встроенные клавиатуры)
	print("60 ", event.original_update.message.entities)  #"Сущности" сообщения для стилизованного текста #https://core.telegram.org/api/entities
	print("61 ", event.original_update.message.views)  #Количество просмотров сообщений на канале
	print("62 ", event.original_update.message.edit_date)  #Дата последнего редактирования этого сообщения
	print("63 ", event.original_update.message.post_author)  #Имя автора сообщения для сообщений на канале (с включенными подписями)
	print("64 ", event.original_update.message.grouped_id)  #Несколько мультимедийных сообщений, отправленных с использованием messages.sendMultiMedia с одним и тем же сгруппированным идентификатором, указывают на альбом
	print("65 ", event.original_update.message.restriction_reason)  # Содержит причину, по которой доступ к этому сообщению должен быть ограничен.
  ```


# Для Групповых Чатов (Канал)
```python
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

	# https://tl.telethon.dev/constructors/photo.html
	# https://core.telegram.org/constructor/photo
	print("21 ", event.original_update.message.media)
	print("22 ", event.original_update.message.media.photo)
	print("23 ", event.original_update.message.media.photo.id) # ID
	print("24 ", event.original_update.message.media.photo.access_hash) # Хеш доступа
	print("25 ", event.original_update.message.media.photo.file_reference)  # ссылка на файл
	print("26 ", event.original_update.message.media.photo.date)  # Дата загрузки
	print("27 ", event.original_update.message.media.photo.date.tzinfo)  # Дата загрузки

	#https://tl.telethon.dev/constructors/photo_stripped_size.html
	#https://core.telegram.org/constructor/photoStrippedSize
	print("28 ", event.original_update.message.media.photo.sizes[0])  # Вложение media
	print("29 ", event.original_update.message.media.photo.sizes[0].type)
	print("30 ", event.original_update.message.media.photo.sizes[0].bytes)# Вложение media

	#https://tl.telethon.dev/types/photo_size.html
	#https://core.telegram.org/constructor/photoSize
	print("31 ", event.original_update.message.media.photo.sizes[1])
	print("32 ", event.original_update.message.media.photo.sizes[1].type) #Тип эскиза
	print("33 ", event.original_update.message.media.photo.sizes[1].location) # Расположение файла
	print("34 ", event.original_update.message.media.photo.sizes[1].location.volume_id) # Вложение media
	print("35 ", event.original_update.message.media.photo.sizes[1].location.local_id) # Вложение media
	print("36 ", event.original_update.message.media.photo.sizes[1].w) # Ширина изображения
	print("37 ", event.original_update.message.media.photo.sizes[1].h) # Высота изображения
	print("38 ", event.original_update.message.media.photo.sizes[1].size) # Размер файла

	# https://tl.telethon.dev/types/photo_size.html
	# https://core.telegram.org/constructor/photoSize
	print("39 ", event.original_update.message.media.photo.sizes[2])
	print("40 ", event.original_update.message.media.photo.sizes[2].type) #Тип эскиза
	print("41 ", event.original_update.message.media.photo.sizes[2].location) # Расположение файла
	print("42 ", event.original_update.message.media.photo.sizes[2].location.volume_id) # Вложение media
	print("43 ", event.original_update.message.media.photo.sizes[2].location.local_id) # Вложение media
	print("44 ", event.original_update.message.media.photo.sizes[2].w) # Ширина изображения
	print("45 ", event.original_update.message.media.photo.sizes[2].h) # Высота изображения
	print("46 ", event.original_update.message.media.photo.sizes[2].size) # Размер файла

	# https://tl.telethon.dev/types/photo_size.html
	# https://core.telegram.org/constructor/photoSize
	print("47 ", event.original_update.message.media.photo.sizes[3])
	print("48 ", event.original_update.message.media.photo.sizes[3].type) #Тип эскиза
	print("49 ", event.original_update.message.media.photo.sizes[3].location) # Расположение файла
	print("50 ", event.original_update.message.media.photo.sizes[3].location.volume_id)  # Вложение media
	print("51 ", event.original_update.message.media.photo.sizes[3].location.local_id)  # Вложение media
	print("52 ", event.original_update.message.media.photo.sizes[3].w) # Ширина изображения
	print("53 ", event.original_update.message.media.photo.sizes[3].h) # Высота изображения
	print("54 ", event.original_update.message.media.photo.sizes[3].size)  # Вложение media

	# https://tl.telethon.dev/constructors/photo.html
	# https://core.telegram.org/constructor/photo
	print("55 ", event.original_update.message.media.photo.dc_id)  # DC ID для загрузки
	print("56 ", event.original_update.message.media.photo.has_stickers)  # Вложение media
	print("57 ", event.original_update.message.media.photo.video_sizes)  # Вложение media

	#https://tl.telethon.dev/constructors/message_media_photo.html
	#https://core.telegram.org/constructor/messageMediaPhoto
	print("58 ", event.original_update.message.media.ttl_seconds) # Время жить в секундах самоуничтожающегося фото

	print("59 ", event.original_update.message.reply_markup)  #Разметка ответа (боты / встроенные клавиатуры)
	print("60 ", event.original_update.message.entities)  #"Сущности" сообщения для стилизованного текста #https://core.telegram.org/api/entities
	print("61 ", event.original_update.message.views)  #Количество просмотров сообщений на канале
	print("62 ", event.original_update.message.edit_date)  #Дата последнего редактирования этого сообщения
	print("63 ", event.original_update.message.post_author)  #Имя автора сообщения для сообщений на канале (с включенными подписями)
	print("64 ", event.original_update.message.grouped_id)  #Несколько мультимедийных сообщений, отправленных с использованием messages.sendMultiMedia с одним и тем же сгруппированным идентификатором, указывают на альбом
	print("65 ", event.original_update.message.restriction_reason)  # Содержит причину, по которой доступ к этому сообщению должен быть ограничен.```
```
