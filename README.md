# [RU] Шаблон для Telegram Bot (aiogram)
# [EN] Template for Telegram Bot (aiogram)
***
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
