импорт  asyncio
из  случайного случайного  импорта 

с  телемарафона  импортируйте  TelegramClient
телемарафон  от.events  импорт  нового сообщения

APP_ID = 1252636
API_HASH = '4037e9f957f6f17d461b0c288ffa50f1'

СЕРДЦЕ  =  '🤍'
= ЦВЕТНЫЕ СЕРДЦА ['💗', '💓', '💖', '💘', '❤️', '💞']
= MAGIC_PHRASES ['магия']
EDIT_DELAY = 0.01

PARADE_MAP = "'
00000000000
00111011100
01111111110
01111111110
00111111100
00011111000
00001110000
00000100000
'''

TelegramClient = клиент ('tg-аккаунт', APP_ID, API_HASH)


генерация_parade_colored  def():
    вывод  = "
    PARADE_MAP  в  c  для:
        '0' ==  c , если:
            вывод  +=  СЕРДЦЕ
        '1' ==  c  elif:
            выбор  +=  вывод (COLORED_HEARTS)
        ещё:
            вывод  += c
    возвращает  вывод


process_love_words  def  асинхронный (событие: новое сообщение.Событие):
    клиент  ожидает.edit_message(event.peer_id.user_id, event.message.id , "я")
    ожидание  асинхронного режима.сон (1)
    ожидание клиента .edit_message(event.peer_id.user_id, event.message.id , "я люблю")
    ожидание  асинхронного режима.сон (1)
    клиент  ожидает.edit_message(event.peer_id.user_id, event.message.id , "я люблю тебя")
    ожидание  асинхронного режима.сон (1)
    клиент  ожидает.edit_message(event.peer_id.user_id, event.message.id , "я люблю тебя вечно")
    ожидание  асинхронного режима.сон (1)
    клиент  ожидает.edit_message(event.peer_id.user_id, event.message.id , "я люблю тебя вечно")


process_build_place  def  асинхронный (событие: новое сообщение.Событие):
    вывод  = "
    диапазон  в  i  для (8):
        вывод  +=  '\n'
        диапазон  в  дж  для (11):
            вывод  +=  СЕРДЦЕ
            клиент  ожидает.edit_message(event.peer_id.user_id, event.message.id , выходной)
            asyncio await.sleep(EDIT_DELAY / 2)


process_colored_parade  def  асинхронный (событие: новое сообщение.Событие):
    диапазон  в  i  для (50):
        generate_parade_colored = text()
        клиент  ожидает.edit_message(event.peer_id.user_id, event.message.id , текст)

        ожидание  асинхронного режима.sleep(EDIT_DELAY)


@client.on(новое сообщение (исходящее = True))
handle_message   определяет асинхронность (событие: новое сообщение.Событие):
    событие , если.сообщение.сообщение  в  MAGIC_PHRASES:
        process_build_place  ожидает (событие)
        ожидание  process_colored_parade (событие)
        process_love_words  ожидает (событие)


'__main__' == __name__ если:
    print('[*] Подключиться к клиенту ...')
    client.start()
    client.run_until_disconnectedrun_until_disconnected()
   
