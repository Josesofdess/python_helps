данные **API/Constructors/Document** делались с тестированием на Документы.

```python
@client.on(events.NewMessage(func=lambda e: e.document))
async def ss(event):
	print("2", event.media.document)
	print("3", event.media.document.id)
	print("4", event.media.document.access_hash)
	print("5", event.media.document.file_reference)
	print("6", event.media.document.date)
	print("7", event.media.document.date.tzinfo)
	print("8", event.media.document.mime_type)
	print("9", event.media.document.size)
	print("10", event.media.document.dc_id)```
