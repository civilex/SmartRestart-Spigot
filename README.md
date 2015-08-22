SmartRestart-Spigot
===================

What does it do?
----------------
Allows to set limits for a server restart. Currently based on memory usage, tick time (tick below 12 for instance) and scheduled (every 24 hours).

### Base Configuration

```
# Valid time suffixes are:
# - d: day
# - h: hour
# - m: minute
# - s: seconds
# - ms: milli seconds
# You can use 3d4h23m10s19ms as a time value in all time configuration values.
>
#Prevents the server from restarting in this time period. Scheduled is not affected by this.
Restart-Timeout: 30m
>
# shorthand notations:
# k - 1000
# c - 100
# m - 1000000
Max-Log-Size: 10k
# Enables restart on memory limit.
Memory-Limit-Enabled: true
# Set the memory limit for a restart.
Memory-Limit: 90%
# Enables restart on time.
Scheduled-Restart-Enabled: true
#This forces a restart every X hours.
Restart-Force-Hours: 24h
# Enables restart on tick below a certain level.
Tick-Restart-Enabled: true
# Restart if tick falls below:
Restart-On-Tick-Below: 12
```
