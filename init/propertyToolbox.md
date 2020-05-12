# propertyToolbox

* access through getprop/setprop,
* property listener in the watchprops command
* api at: system/core/include/cutils/properties.h
* Framework level access to system properties is carried out through android.os.SystemProperty 
  * which accesses the properties via JNI calls to the API calls.

