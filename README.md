<p align="center">
    <a href="https://github.com/pyrogram/pyrogram">
        <img src="https://raw.githubusercontent.com/pyrogram/artwork/master/artwork/pyrogram-logo.png" alt="Pyrogram" width="128">
    </a>
    <br>
    <b>Telegram MTProto API Framework for Python</b>
    <br>
    <a href="https://pyrogram.org">
        Homepage
    </a>
    •
    <a href="https://docs.pyrogram.org">
        Documentation
    </a>
    •
    <a href="https://docs.pyrogram.org/releases">
        Releases
    </a>
    •
    <a href="https://t.me/pyrogram">
        News
    </a>
</p>

## Pyrogram

> [!NOTE]
> The project is no longer maintained or supported. Thanks for appreciating it.

> Elegant, modern and asynchronous Telegram MTProto API framework in Python for users and bots

``` python
from pyrogram import Client, filters

app = Client("my_account")


@app.on_message(filters.private)
async def hello(client, message):
    await message.reply("Hello from Pyrogram!")


app.run()
```

**Pyrogram** is a modern, elegant and asynchronous [MTProto API](https://docs.pyrogram.org/topics/mtproto-vs-botapi)
framework. It enables you to easily interact with the main Telegram API through a user account (custom client) or a bot
identity (bot API alternative) using Python.

### Key Features

- **Ready**: Install Pyrogram with pip and start building your applications right away.
- **Easy**: Makes the Telegram API simple and intuitive, while still allowing advanced usages.
- **Elegant**: Low-level details are abstracted and re-presented in a more convenient way.
- **Fast**: Boosted up by [TgCrypto](https://github.com/pyrogram/tgcrypto), a high-performance cryptography library written in C.  
- **Type-hinted**: Types and methods are all type-hinted, enabling excellent editor support.
- **Async**: Fully asynchronous (also usable synchronously if wanted, for convenience).
- **Powerful**: Full access to Telegram's API to execute any official client action and more.

## Patches in this Fork

This fork maintains compatibility for modern Telegram infrastructure and current Python versions:

- **64-bit Telegram IDs**: Updated channel, supergroup, and user ID ranges (`MIN_CHANNEL_ID` and `MAX_USER_ID`) in `pyrogram.utils` to support channels created above `-1002000000000` without triggering `ValueError: Peer id invalid`.
- **Python 3.12+ Event Loop Compatibility**: Updated event loop acquisition across `Client`, `Dispatcher`, `Session`, `TCP`, `sync`, and `download_media` to gracefully handle environments without an active running loop or where implicit event loop creation is deprecated.

### Installing

Install directly from this repository:

```bash
pip3 install git+https://github.com/itswill00/pyrogram.git
```

### Resources

- Check out the docs at https://docs.pyrogram.org to learn more about Pyrogram, get started right
away and discover more in-depth material for building your client applications.
- Join the official channel at https://t.me/pyrogram and stay tuned for news, updates and announcements.
