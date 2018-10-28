# PersonalHotspot.spoon

A [Hammerspoon](http://www.hammerspoon.org) to connect, disconnect, or toggle connection to/from a personal hotspot. Optionally kills/opens a list of apps on connect/disconnect respectively.

Example configuration (using [SpoonInstall.spoon](http://www.hammerspoon.org/Spoons/SpoonInstall.html)):
```lua
spoon.SpoonInstall:andUse(
  "PersonalHotspot",
  {
    config = {
      hotspotName = "John Appleseed’s iPhone",
      appsToKill = {
        "Arq",
        "Arq Agent",
        "Dropbox"
      }
    },
    hotkeys = {
      toggle = { {"cmd", "option", "ctrl"} , "h"}
    }
  }
)
 ```

If `hotspotName` isn't set, the first personal hotspot in the Wi-Fi menu will be selected, and `hotspotName` will be set to the name of that hotspot.
