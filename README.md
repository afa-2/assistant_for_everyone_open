# assistant_for_everyone_open
Python3 скрипт, реализованный в exe файл, который локально на компьютере запускает ТГ бота, привязанного к ассистенту в openAI.
Принцип работы: при отправке сообщения ТГ боту, этот скрипт берет это сообщение, отправляет ассистенту в openAi, получает ответ, возвращает ответ в ТГ пользователю, который написал сообщение.

Путь к настройкам: main/_internal/config_files_and_secret_inf/config.json

Пример настройки (файл config.json):
{
  "telegram_token": "11111:1111111111111111",
  
  "users": {
    "684416659": {
      "name": "Afa",
      "open_ai_key": "sk-111111111111111111",
      "assistant_id": "asst_11111111111111111111111"
    },

    "11111111": {
      "name": "Name",
      "open_ai_key": "111111111111111",
      "assistant_id": "asst_ggggggggggggggggg"
    }
  }
}

telegram_token - токен ТГ бота, созданного через botfathr
users - список юзеров, которым разрешено пользоваться ботом
"684416659": {
      "name": "Afa",
      "open_ai_key": "sk-111111111111111111",
      "assistant_id": "asst_11111111111111111111111"
    },
    
684416659 - id юзера в ТГ (можно выяснить через бота @getmyid)
open_ai_key - ключ openAI, который будет использоваться для отправи запросов в openAi. Какждому пользователю можно приявязть отдельный ключ.
assistant_id - id ассисетнта, созданного также в openai
