#!/usr/bin/env bash
# Gracefully reloads Gunicorn.

ps aux | grep gunicorn | awk '{ print $2 }' | xargs kill -HUP
