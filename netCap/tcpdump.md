# tcpdump to log packets

```
adb push ~/Downloads/tcpdump /sdcard/
adb shell
su root
mv /sdcard/tcpdump /data/local/
cd /data/local/
chmod +x tcpdump


./tcpdump -vv -i any -s 0 -w /sdcard/dump.pcap
CTRL+C after you've captured enough packets.
exit
exit
adb pull /sdcard/dump.pcap ~/Downloads/

```
