## Running playstrategy-bot
After activating the virtual environment created in the installation steps (the `source` line for Linux and Macs or the `activate` script for Windows), run
```
python3 playstrategy-bot.py
```
The working directory for the engine execution will be the playstrategy-bot directory. If your engine requires files located elsewhere, make sure they are specified by absolute path or copy the files to an appropriate location inside the playstrategy-bot directory.

To output more information (including your engine's thinking output and debugging information), the `-v` option can be passed to playstrategy-bot:
```
python3 playstrategy-bot.py -v
```

If you want to disable automatic logging:
```
python3 playstrategy-bot.py --disable_auto_logging
```

If you want to record the output to a log file, add the `-l` or `--logfile` along with a file name:
```
python3 playstrategy-bot.py --logfile log.txt
```

If you want to specify a different config file, add the `--config` along with a file name:
```
python3 playstrategy-bot.py --config config2.yml
```

### Running as a service
- Here's an example systemd service definition:
```ini
[Unit]
Description=playstrategy-bot
After=network-online.target
Wants=network-online.target

[Service]
Environment="PYTHONUNBUFFERED=1"
ExecStart=/usr/bin/python3 /home/thibault/playstrategy-bot/playstrategy-bot.py
WorkingDirectory=/home/thibault/playstrategy-bot/
User=thibault
Group=thibault
Restart=always

[Install]
WantedBy=multi-user.target
```

## Quitting
- Press `CTRL+C`.
- It may take some time to quit.

**Previous step**: [Configure playstrategy-bot](https://github.com/Mind-Sports-Games/playstrategy-bot/wiki/Configure-playstrategy-bot)