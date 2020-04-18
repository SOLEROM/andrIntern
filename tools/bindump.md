# bindump


* If the Binder debug functionality is enabled through the Linux debugfs filesystem ( /sys/kernel/debug/binder )
* you can figure out who's connected to what
* bindump use simple derivative of the (service check) command
* obtains a handle to the system service of choice
* then inspects its own entry in the /sys/kernel/debug/binder/proc directory
* Each process using binder has a pseudo-file containing various statistics,
* the NODE entries contained therein reveal the PIDs connected on the other end

### example1:

```
# Inquire about wallpaper service
shell@htc_m8wl:/ $ /data/local/tmp/bindump wallpaper
Service: wallpaper node ref: 2034
User: PID 1377
com.htc.launcher
User: PID 1194
com.android.systemui
Owner: PID 1008
system_server
User: PID
368
/system/bin/servicemanager



# Who owns the batterypropreg service?
shell@htc_m8wl:/ $ /data/local/tmp/bindump owner batterypropreg
Service: batterypropreg node ref: 105785
Owner: PID 8153
/sbin/healthd

```



