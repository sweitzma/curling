# Curling
Scripts/utilities to run on on a raspberry pi to add some controlled
and regular traffic into my network.

### Setup
Set up a symlink into the `$PATH` via
```
ln -s $PATH_TO_REPO/curling /usr/bin/curling
```

For now we'll do the most basic version of running this, we'll configure cron
to run it every minute and log to the home directory. We can do this via
```
crontab -e
```
and then adding the line
```
* * * * * curling > ~/curling.log
```

Down the line we may want to use `systemd` and `rsyslog` to handle logging and wrap
this all in a more proper service.
