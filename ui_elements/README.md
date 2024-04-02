__#INFO__


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
<img src="https://raw.githubusercontent.com/NupsNils/nngrp_guides/main/ui_elements/imgs/nngrp_frame_false.png">

## Mit :SetBGImg("LINK ZUM MATERIAL")
<img src="https://raw.githubusercontent.com/NupsNils/nngrp_guides/main/ui_elements/imgs/nngrp_frame_true.png">

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

# NNGRP ListView
<img src="https://raw.githubusercontent.com/NupsNils/nngrp_guides/main/ui_elements/imgs/nngrp_listview.png">

```LUA
:AddColumnWithCustomStyle(...) // Fügt einen Column hinzu Bsp. AddColumnWithCustomStyle("Test")
:SetColumnFont(font) // Ändert die Font der Columns Bsp. SetColumnFont("NNGRP.50")
:AddLineWithCustomStyle(...) // Fügt eine Line hinzu Bsp. AddLineWithCustomStyle("Test")
:SetLineFont(font) // Ändert die Font der Line Bsp. SetColumnFont("NNGRP.50")
```
## Bsp. wie im Bild
```LUA
self.Element = self.Frame:Add("NNGRP.ListView")
self.Element:SetSize(w * .4, h * .4)
self.Element:Center()
self.Element:SetHeaderHeight(self.Frame:GetTall() * .035)
self.Element:SetDataHeight(self.Frame:GetTall() * .03)
self.Element:SetMultiSelect(false)
self.Element:SetText("")
self.Element:AddColumnWithCustomStyle("Test")
function self.Element:Paint(w,h)
    draw.RoundedBox(0, 0, 0, w, h, Color(25,25,25))
end

for k, v in pairs({"Test1","Test2","Test3","Test4","Test5"}) do
    local line = self.Element:AddLineWithCustomStyle(v)
        
    if v == "Test2" then
        line:SetTextColor(Color(150, 0, 0))
    end
end
```

# NNGRP Scrollpanel
<img src="https://raw.githubusercontent.com/NupsNils/nngrp_guides/main/ui_elements/imgs/nngrp_scrollpanel.png">

## Bsp. wie im Bild
```LUA
self.Element = self.Frame:Add("NNGRP.ScrollPanel")
self.Element:SetSize(w * .4, h * .4)
self.Element:Center()

for i = 0, 20 do
    self.TestButton = self.Element:Add("NNGRP.Button")
    self.TestButton:Dock(TOP)
    self.TestButton:SetUp("Button " .. i, "NNGRP.20", Color(20, 100, 20), function()
        // FUNKTION
    end)
end
```

# NNGRP TextEntry
<img src="https://raw.githubusercontent.com/NupsNils/nngrp_guides/main/ui_elements/imgs/nngrp_textentry.png">

## Bsp. wie im Bild
```LUA
self.Element = self.Frame:Add("NNGRP.TextEntry")
self.Element:SetSize(w * .4, h * .1)
self.Element:Center()
```
