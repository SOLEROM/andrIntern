# gapp install log

```
angler:/ # cat /sdcard/open_gapps_log.txt                                                                                                   
# Begin Open GApps Install Log
------------------------------------------------------------------
            ROM Android version | 8.1.0
                   ROM Build ID | aosp_angler-eng 8.1.0 OPM7.181205.001 eng.root.20200416.203240 test-keys
          ROM Version increment | eng.root.20200416.203240
                ROM SDK version | 27
        ROM/Recovery modversion | OmniROM-6.0.1-20190519-angler-HOMEMADE
                Device Recovery | TWRP 3.3.1-0-f5955b1c
                    Device Name | angler
                   Device Model | AOSP on angler
                    Device Type | phone
                     Device CPU | arm64-v8a,armeabi-v7a,armeabi
          Device A/B-partitions | false
             Installer Platform | arm
                   ROM Platform | arm64
           Display Density Used | 560
                   Install Type | Clean[Data Wiped]
             Smart ART Pre-ODEX | false
Google Camera already installed | Clean
              VRMode Compatible | false
       Google Camera Compatible | true
      New Camera API Compatible | true[whitelist]
          Google Pixel Features | false
          Current GApps Version | 20200415
     Current Open GApps Package | pico
       Installing GApps Zipfile | /sdcard/open_gapps-arm64-8.1-pico-20200415-UNOFFICIAL.zip
       Installing GApps Version | 20200415
          Installing GApps Type | pico
                    Config Type | 
             Using gapps-config | Not Used
      Remove Stock/AOSP Browser | false[NO_Chrome]
       Remove Stock/AOSP Camera | false[NO_CameraGoogle]
       Remove Stock/AOSP Dialer | false[NO_DialerGoogle]
        Remove Stock/AOSP Email | false[NO_Gmail]
      Remove Stock/AOSP Gallery | false[NO_Photos]
     Remove Stock/AOSP Launcher | false[NO_GoogleNow/PixelLauncher]
      Remove Stock/AOSP MMS App | false[NO_Messenger]
     Remove Stock/AOSP Pico TTS | false[default]
         Ignore Google Contacts | false
           Ignore Google Dialer | true[NoRemove]
         Ignore Google Keyboard | false
Ignore Google Package Installer | false[PackageInstallerGoogle]
          Ignore Google NFC Tag | false
          Ignore Google WebView | false
         Total System Size (KB) | 3144432
         Used System Space (KB) | 1045848
        Current Free Space (KB) | 2082200
   Post Install Free Space (KB) | 2064888   << See Calculations Below
------------------------------------------------------------------
# End Open GApps Install Log


# Begin GApps Size Calculations
------------------------------------------------------------------
  TYPE  |         DESCRIPTION        |      SIZE |   TOTAL
        |         Current Free Space |   2082200 | 2082200
 Remove |             Existing GApps | +  129976 | 2212176
 Remove |             Obsolete Files | +       0 | 2212176
 Remove |           extservicesstock | +       0 | 2212176
 Remove |             extsharedstock | +       0 | 2212176
 Remove |      packageinstallerstock | +       0 | 2212176
 Remove |                  provision | +       0 | 2212176
Install |                       Core | -  104692 | 2107484
Install |                    calsync | -    2868 | 2104616
Install |            dialerframework | -      32 | 2104584
Install |                  googletts | -   24776 | 2079808
Install |     packageinstallergoogle | -    5704 | 2074104
        |               Buffer Space | -    9216 | 2064888
------------------------------------------------------------------
                        Post Install Free Space | 2064888
------------------------------------------------------------------

# End GApps Size Calculations

# Begin User's gapps-config

# End User's gapps-config

```


# after install

```
angler:/ # ls /system/priv-app/                                                                                                             
BackupRestoreConfirmation ContactsProvider        GmsCoreSetupPrebuilt     Launcher3            ProxyHandler        Tag               
BlockedNumberProvider     CtsShimPrivPrebuilt     GoogleBackupTransport    ManagedProvisioning  Settings            TeleService       
CalendarProvider          DefaultContainerService GoogleExtServices        MediaProvider        SettingsProvider    Telecom           
CallLogBackup             Dialer                  GoogleFeedback           MmsService           SetupWizard         TelephonyProvider 
CarrierConfig             DocumentsUI             GoogleOneTimeInitializer MtpDocumentsProvider SharedStorageBackup VpnDialogs        
CarrierSetup              DownloadProvider        GooglePackageInstaller   MusicFX              Shell               WallpaperCropper  
CellBroadcastReceiver     EmergencyInfo           GooglePartnerSetup       OneTimeInitializer   StatementService    twrpapp           
ConfigUpdater             ExternalStorageProvider GoogleServicesFramework  Phonesky             StorageManager      
Contacts                  FusedLocation           InputDevices             PrebuiltGmsCorePix   SystemUI 
```
