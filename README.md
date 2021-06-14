# Godot-Admob-android-ios
## IOS
download ios [admob sdk](https://drive.google.com/file/d/1xPNys1MWJDaGt-plIXAGVVpB6dsP-pVE/view?usp=sharing).
Add in ios/plugins/lib/ folder.

```
var admob
```
```
if Engine.has_singleton("AdMobSD"):
  print("AdMobSD was detedted")
  admob = Engine.get_singleton("AdMobSD")
  var instance_id = get_instance_id()
  var isReal = true
  admob.init(isReal, instance_id)
  loadInterstitial()
else:
  print("AdMobSD was not detedted")
```

```
func loadInterstitial():
  if admob != null:
    admob.loadInterstitial(adInterstitialId)
    print("ADMOB LOADED")
```
```
func _on_showInterstitial():
  if admob != null:
    admob.showInterstitial()
```
```
func _on_loadwith_showInterstitial():
  if admob != null:
    admob.loadWithShowInterstitial()
```
