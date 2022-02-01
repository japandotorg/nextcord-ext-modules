# nextcord/ext/space

![discord](https://img.shields.io/discord/772708529744248842?color=red&label=discord&style=flat-square)
![pythonVersion](https://img.shields.io/pypi/pyversions/nextcord-ext-space)
![implementation](https://img.shields.io/pypi/implementation/nextcord-ext-space)
![format](https://img.shields.io/pypi/format/nextcord-ext-space)
![status](https://img.shields.io/pypi/status/nextcord-ext-space)
![version](https://img.shields.io/pypi/v/nextcord-ext-space)
![license](https://img.shields.io/github/license/japandotorg/nextcord-ext-space)

An event logger for [nextcord](https://github.com/nextcord/nextcord).

## Install
```sh
$ python3.8 -m pip install -U nextcord-ext-space
```

## Extras

### [`databases`](https://github.com/encode/databases) package

You may want to manually install [`databases`](https://github.com/encode/databases) with the correct drivers installed.

## Examples

```py
import logging

from nextcord.ext.space import Astronaut, EventFlags, Configuration
from nextcord.ext.space.recorders.databases import DatabaseRecorder

logging.basicConfig(filename='myBotLog.log', filemode='w', level=logging.DEBUG)

config = Configuration(
    events=EventFlags.guilds()
    recorder=DatabaseRecorder('url/to/my/database')
)

client = Astronaut(config=config)

client.run('TOKEN')
```