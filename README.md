# coolMsgroom
Yet another MsgRoom server. Thanks to [@nolanwhy](https://github.com/nolanwhy) for some references.
# This isn't finished yet!!

## Startup
```sh
git clone https://github.com/RixInGithub/coolMsgroom.git
cd coolMsgroom
pip3 install -r requirements.txt
python3 main.py
```
## `config.ini`
When you try to run `main.py`, you'll see a warn like this:
```
NOTE: config.ini file nonexistent. Continuing with hard-coded presets...
```
To avoid this, simply create a `config.ini` file in the project root (if ran through "Startup" without rename, `coolMsgroom/`).
### Docs
|Key|Hard-coded val|Type|Meaning|
|:-:|:-:|:-:|:-|
|`name`|`coolMsgroom`|String|Title used for Flask import name, etc.|
|`supportBotArg`|`1`|Number 0-1 (invalid nums are `0`)|Support `bot` argument in `auth` event|
|`chatUI`|`1`|Number 0-1 (invalid nums are `0`)|Enable experimental UI. Note the UI is different from MsgRoom's original UI. If `0`, will send value of config variable `httpRet`|
|`httpRet`|`Welcome to coolMsgroom's homepage!\nLooks like the chat UI had been disabled... :(`|String (use `\n` to replace for a newline)|If `chatUI` is `0`, coolMsgroom will send this variable's value as MIME type `text/text` if requested through HTTP. Else, return the chat UI.|
||||
## coolMsgroom docs
So far, I've digged up a lot of Msgroom API docs. All of these features are used in `coolMsgroom` unless a otherwise stated
