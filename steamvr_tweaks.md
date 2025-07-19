To disable tracker power on to startup SteamVR edit file:

C:\Program Files (x86)\Steam\config\steamvr.vrsettings

Add the following JSON key:
```json
{
   "power" : {
      "autoLaunchSteamVROnButtonPress" : false
   }
}
```

---

To enable Lightouse tracking on Quest Headset (providing you attached a tracker to the headset)

in C:\Program Files (x86)\Steam\config\steamvr.vrsettings

```json
{
   "steamvr" : {
      "requireHmd": false,
      "activateMultipleDrivers" : true
   },
   "TrackingOverrides" : {
      "/devices/lighthouse/LHR-E13F79E8" : "/user/head"
   },
}
```
You then want VRChat to ignore a specific tracker so it's not prompted in the FBT stuff (nor does it prompt said FBT stuff when you're just using a single tracker with Index controller for example).

Just add to the startup options `--ignore-trackers=LHR-E13F79E8`

---

To enable pairing control for dongle and thus control what is paired with what dongle

```json
{
   "dashboard" : {
      "allowInHeadsetControllerPairing" : true
   },
}
```
