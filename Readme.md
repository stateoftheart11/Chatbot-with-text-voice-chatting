# Telegram Bot "My Friend"

Telegram Bot "My Friend" is bot to help customers to make theirself friends. This bot is developed by AI techniques(Speech-to-Text, Text-to-Speech, Voice-cloning, AI-avatar-geneartor) and telegram bot developing techniques. This bot can chat with customer through text and voice.
This bot responses as text when customers ask as text, and if customers ask as voice, it responses as video.
Customers can set their pictures and voice. This bot can make video with customer pictures and voices.

## Setup

### Setup 1: Building Environment
- Download code from gitlab

  `git clone https://github.com/LoveNui/telegram_bot.git`

- Reseetting API keys
    - On the bot_src/private_env.py
      
      DG_KEY = 'c6a441dc5efbbd7e1ef959348c122aec01c325b62'
      OPENAI_KEY = "sk-Ke7ePCgDFKF3l18m6HmTRs9lbkFJRXDobcl72SOaldgD18FT"
      SERP_API_KEY = "3e4d6384rf3ecf52dd4a2868843784f73ed36fb823496b856158503414febe689"

    - Creating ".env" file and Input serpapi_key

    `SERPAPI_API_KEY = 3e4d6384rf3ecf52dd4a2868843784f73ed36fb823496b856158503414febe689`

- Make folder "voice_message"
- Downloading models (Run ./scripts/download_models.sh)
    
    `bash ./scripts/download_models.sh`

### Setup 2: Install Libraries
- Install all libraries on requirements.txt

  `!pip install -r requirements.txt`

## Useage
### Run Telegram Bot
`python telegram-bot.py`
### Setting Customer Pictures and voice
Users can set their pictures and voice. When Users upload their pictures and record their voice, the bot saves their pictures and clones users voice, and make video with their pictures and voice.
#### Pictures
- Users send message "/picture"
- Users upload pictures. The picture's size must be at least 500*500.
- If uploaded successfully, bot sends message "Congratulations!, Successfully uploaded your picture". When failed to upload pictures, bot sends message "Failed to upload your pictures. Please try again".

#### Voice Cloning
- Users send message "/voice"
- Users send voice message, the legnth is 30~40s. If users send voice message, the bot clones user's voice with this voice message.
- If successfully clone voice, the bot sends message "Congratulations!, Successfully cloned your voice". If failed to clone voice, the bot sends "I am sorry. Failed to clone your voice"