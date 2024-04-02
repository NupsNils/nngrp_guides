# Font
"NNGRP.SIZE" - Bsp. "NNGRP.24"

# NNGRP Button
<img src="https://raw.githubusercontent.com/NupsNils/nngrp_guides/main/ui_elements/imgs/nngrp_button.png">

```LUA
:SetMsg(text) // Ändert den Text des Buttons
:SetCol(color) // Ändert die Farbe des Buttons
:SetUp(text, font, color, func) Bsp. :SetUp("TEST", "NNGRP.24", Color(255, 0, 0), function() print("TEST") end)
```
## Bsp. wie im Bild
```LUA
self.Element = self.Frame:Add("NNGRP.Button")
self.Element:SetSize(w * .5, h * .1)
self.Element:SetPos(w * .25, h * .45)
self.Element:SetUp("ORANGE BUTTON", "NNGRP.30", Color(200, 100, 0), function()
    // FUNKTION
end)
```

# NNGRP Close Button
<img src="https://raw.githubusercontent.com/NupsNils/nngrp_guides/main/ui_elements/imgs/nngrp_closebutton.png">
### Größe ist automatisch angepasst, kann aber verändert werden

```LUA
:SetUp(func) Bsp. :SetUp(function() print("TEST") end)
```
## Bsp. wie im Bild
```LUA
self.Element = self.Frame:Add("NNGRP.CloseButton")
self.Element:SetUp(function()
    // FUNKTION
    frame:Close()
end)
```

# NNGRP Frame
## Mit :SetBGImg(false)
<img src="https://raw.githubusercontent.com/NupsNils/nngrp_guides/main/ui_elements/imgs/nngrp_frame_false.png" style="width: 300px; height: 250px">

## Mit :SetBGImg("LINK ZUM MATERIAL")
<img src="https://raw.githubusercontent.com/NupsNils/nngrp_guides/main/ui_elements/imgs/nngrp_frame_true.png" style="width: 300px; height: 250px">

```LUA
:SetBGImg(bgimg) // Link zum Material z.B. "nng/img4" (Materials Ordner bei Addons)
:SetFrameInfo(header, info) // Header = Titel, Info = Beschreibung
```
## Bsp. wie im Bild
```LUA
self.Frame = vgui.Create("NNGRP.Frame")
self.Frame:SetPos((ScrW() - w) / 2, (ScrH() - h) / 2)
self.Frame:SetSize(w, h)
self.Frame:SetFrameInfo("BSP. Servername", "BSP. Waffenkiste")
self.Frame:SetBGImg(false)
```
