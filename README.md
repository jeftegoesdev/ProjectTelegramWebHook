## What is this project

It is a small / simple project that shows how to use telegram bot api, the example was used as the basis https://github.com/TelegramBots/Telegram.Bot.Examples

## Project Type WebAPI

.NET 5.0

Telegram.Bot 15.7.1

## Utils

ngrok

## How to run this project

1. Change the appsettings files, the BotToken attribute, by the token generated by the telegram <MY_TOKEN_HERE>
2. Execute dotnet run to run this project
3. Download and execute this command ngrok.exe http -host-header=localhost 5000 
4. Get the https url, generated by ngrok and test if webhook work
5. Contract telegram with webhook using the first command below

## Some useful commands

Contract webhook with telegram
>https://api.telegram.org/bot<MY_TOKEN_HERE>/setWebhook?url=MY_LINK/Api/Update

Return some information about the bot
>https://api.telegram.org/bot<MY_TOKEN_HERE>/getMe

Get all informations about contract with webhook
>https://api.telegram.org/bot<MY_TOKEN_HERE>/getWebhookInfo

Delete contract between webhook and telegram
>https://api.telegram.org/bot<MY_TOKEN_HERE>/deleteWebhook

Retrieves all messages in the telegram pool
>https://api.telegram.org/bot<MY_TOKEN_HERE>/getUpdates

Remove chat message of TELEGRAM, but dont clear pool messages
>https://api.telegram.org/bot<MY_TOKEN_HERE>/deleteMessage?chat_id=697809357&message_id=63

Retrieves all messages in the telegram pool, if the offser parameter is informed, with the message_id of the pool, it excludes the previous one
>https://api.telegram.org/bot<MY_TOKEN_HERE>/getUpdates?offset=697809357