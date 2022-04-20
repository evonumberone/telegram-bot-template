# Шаблон для Telegram Bot (aiogram)
***

### *ПЕРЕД НАЧАЛОМ*
- *Перед началом создайте файл config.py в директории с ботом и вставьте туда токен бота из @BotFather*
#### Файл config.py:
```python
TOKEN = 'YOUR TOKEN'
```
#### Файл main.py:
```python
import config
import logging
from aiogram import Bot, Dispatcher, executor, types


# Логирование
logging.basicConfig(level=logging.INFO)

# Инициализация бота
bot = Bot(token=config.TOKEN)
dp = Dispatcher(bot)


# Обработчик сообщений
@dp.message_handler()
async def name(message: types.Message):
    await message.answer('message')



# start long-pooling
if __name__ == '__main__':
    executor.start_polling(dp, skip_updates=True)
```
