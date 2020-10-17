данные **API/Constructors/DocumentAttributeVideo** делались с тестированием на видео.

```python
@client.on(events.NewMessage(func=lambda e: e.document))
async def ss(event):
	print("1 ", event.media.document.stringify())
	print("2 ", event.media.document.attributes[0])
	print("3 ",event.media.document.attributes[0].duration)
	print("4 ", event.media.document.attributes[0].w)
	print("5 ", event.media.document.attributes[0].h)
	print("6 ", event.media.document.attributes[0].round_message)
	print("7 ", event.media.document.attributes[0].supports_streaming)
	print("8 ", event.media.document.attributes[1])
	print("9 ", event.media.document.attributes[1].file_name)
	print("10 ", event.media.document.thumbs[0])
	print("11 ", event.media.document.thumbs[0].type)
	print("12 ", event.media.document.thumbs[0].bytes)
	print("13 ", event.media.document.thumbs[1])
	print("14 ", event.media.document.thumbs[1].type)
	print("15 ", event.media.document.thumbs[1].location)
	print("16 ", event.media.document.thumbs[1].location.volume_id)
	print("17 ", event.media.document.thumbs[1].location.local_id)
	print("18 ", event.media.document.thumbs[1].w)
	print("19 ", event.media.document.thumbs[1].h)
	print("20 ", event.media.document.thumbs[1].size)```
