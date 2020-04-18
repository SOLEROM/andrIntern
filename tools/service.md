# service


* Android provides the service command line utility as a simple interface for the service manager
* (service list) you can display all registered services, as well as their published interfaces
* (service check) see if a given service can be contacted.

## example1


## example2
* The true power lies in its ability to call the services themselves.
* use (service call)  and specifying the service name and method number
* methods are assigned numbers in order of their appearance in the service's .aidl file
* supports two types of arguments: i32, which are integer values,and s16, which are used for unicode strings
* Each interface has a corresponding .aidl file in the AOSP, wherein its methods and their arguments are clearly defined


```
phone 2 s16 "foo"
s16 "555-1234"		Place a call to the specified

statusbar 1		expandNotificationsPanel()
statusbar 9		expandSettingsPanel()
statusbar 2		collapsePanels()

dream 1			Screensaver (if configured)

power 11		Returns 0 if screen is off, else 1

```


