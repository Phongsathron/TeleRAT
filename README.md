# TeleRAT
Project Computer Programing 
# How TeleRAT Work
```
 _____________                       _______________                       _______________
| BOT(Client) | ==================> |     Server    | ==================> |   Telegram    |
|   Ubuntu    |                     | Ubuntu On AWS |                     |    Message    | 
|_____________| <================== |_______________| <================== |_______________|

Bot communicate with Server        handle with command that recieve from
using Reverse TCP concept          Telegram massege 
with 1s refresh rate               Waiting for connection from BOT
                                   then send the command to execute


```

# Telegram Commands
```
 _________
< TeleRAT >
 ---------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||

/help - List of commands.
/shell - Exec shell commands with timeout.
/cp - Copy file/folder.
/mv - Move file/folder.
/rm - Remove file/folder.
/mkdir - Make directory.
/timeout - Set timeout for shell.
/mvbot - Move bot to custom location.
/getfile - Download file from bot.
/BOOM! - DESTROY ITSELF!
```

# Setting up self-signed certificates

for connecting to Telegram API. You need to generate `public key` and `private key` for use HTTPS connection for POST request and setup webhook. use `openssl` command to generate the key in PEM encoded

```
openssl req -newkey rsa:2048 -sha256 -nodes -keyout private.pem -x509 -days 365 -out public.pem
```