# systemServerTreads

* Dalvik's thread objects may be named when created
* using prctl system call - highly useful API - allows the renaming of threads and processes at the kernel level.
* The name is then visible through the /proc filesystem in the status proc entry


```
> cd /proc/XXX/task 
> for t in *; do echo Thread $t `grep Name: $t/status`; done



```
