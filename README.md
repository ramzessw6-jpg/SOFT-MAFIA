# SOFT-MAFIA
MAFIA OYINI RASMIY BOTI
import os
import telebot

TOKEN = os.getenv("BOT_TOKEN")
bot = telebot.TeleBot(TOKEN)

@bot.message_handler(commands=["start"])
def start(message):
    bot.reply_to(
        message,
        "🎭 BAKU MAFIA BOT\n\n"
        "Mafiya o‘yiniga xush kelibsiz!\n"
        "O‘yinni boshlash uchun guruhga qo‘shing."
    )

bot.infinity_polling(