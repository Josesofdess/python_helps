**чаты в четырех типах:**

приватный чат (между двумя пользователями) - **is_private**
групповой чат (обычные группы) - **is_group**
группы ужина
канал - **is_channel**

когда вы получаете сообщение от telegram с telethon, у вас есть три флага:

- **is_private**
- **is_group**
- **is_channel**


значение флагов:

- если **is_private = 1, is_group = 0, is_channel = 0** чат - это приватный чат
- если **is_private = 0, is_group = 1, is_channel = 0** чат - является нормальной группой
- если **is_private = 0, is_group = 1, is_channel = 1** чат - является группой ужина
- если **is_private = 0, is_group = 0, is_channel = 1** чат - является каналом

____
