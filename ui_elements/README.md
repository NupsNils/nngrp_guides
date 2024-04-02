# Font
"NNGRP.SIZE" - Bsp. "NNGRP.24"

# NNGRP Button
<img src="https://raw.githubusercontent.com/NupsNils/nngrp_guides/main/ui_elements/imgs/nngrp_button.png">
```lua
:SetMsg(text) // Ändert den Text des Buttons
:SetCol(color) // Ändert die Farbe des Buttons
:SetUp(text, font, color, func) Bsp. :SetUp("TEST", "NNGRP.24", Color(255, 0, 0), function() print("TEST") end
```
## Bsp. wie im Bild
```lua
self.Element = self.Frame:Add("NNGRP.Button")
self.Element:SetSize(w * .5, h * .1)
self.Element:SetPos(w * .25, h * .45)
self.Element:SetUp("ORANGE BUTTON", "NNGRP.30", Color(200, 100, 0), function()
    // FUNKTION
end)
```
