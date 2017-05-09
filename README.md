ErrBot Docker
=============

This repository provides a Docker image to run the [ErrBot](http://errbot.io) chat bot.

Volumes
-------

All files related to ErrBot are stored under `/err`, which is the home directory of the user `err`.
It is adviced to mount at least `/err/data` as volume to persist the configuration and state of your plugins. To provide an own
`config.py` mount `/err/config.py` as volume as well.

```
docker run -v /tmp/err-data:/err/data -e "ERR_USERNAME=err@example.org" -e "ERR_PASSWORD=test1234" freakybytes/errbot
```

Environment Variables
---------------------

| Parameter | Description | Default |
|-----------|-------------|---------|
| `ERR_BACKEND` | Backend used by Err. | `XMPP` |
| `ERR_DATA_DIR` | Data directory | `/err/data` |
| `ERR_LOG_LEVEL` | Python log level. `debug`, `info`, `warning`, `error`, `fatal`, `critical` | `info` |
| `ERR_USERNAME` | Err identity username | Empty |
| `ERR_PASSWORD` | Err identity password | Empty |
| `ERR_TOKEN` | Err identity token for HipChat, Slack, Telegram, etc. | Empty |
| `ERR_ENDPOINT` | Endpoint of a selfhosted HipChat instance | `https://api.hipchat.com` |
| `ERR_ADMINS` | Comma separated list of usernames with admin priviledges | Empty |
| `ERR_CHATROOMS` | Comma separated list of chatrooms to join on startup | Empty |
