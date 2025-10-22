# Activty/a17

## Activty/a17/ActivityDungeon1017Battle_BattleEndByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_BattleEndUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1017Battle_BattleEnd_InfoByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1017Battle_BattleEnd_InfoByName")

function GetActivityDungeon1017Battle_BattleEndUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.Info1 = GetActivityDungeon1017Battle_BattleEnd_InfoUis(ui:GetChild("Info1"))
  uis.Info2 = GetActivityDungeon1017Battle_BattleEnd_InfoUis(ui:GetChild("Info2"))
  uis.EndBtn = ui:GetChild("EndBtn")
```

---

## Activty/a17/ActivityDungeon1017Battle_BattleEndWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_BattleEndWindowUis
**Requires:**
- ActivityDungeon1017Battle_BattleEndByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_BattleEndByName")

function GetActivityDungeon1017Battle_BattleEndWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1017Battle_BattleEndUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_BattleEnd_InfoByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_BattleEnd_InfoUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_BattleEnd_InfoUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_BattleEnd_SureBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_BattleEnd_SureBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_BattleEnd_SureBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_BattleExitByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_BattleExitUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetActivityDungeon1017Battle_BattleExitUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.CancelBtn = ui:GetChild("CancelBtn")
  uis.ExitBtn = ui:GetChild("ExitBtn")
  uis.root = ui
```

---

## Activty/a17/ActivityDungeon1017Battle_BattleExitWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_BattleExitWindowUis
**Requires:**
- ActivityDungeon1017Battle_BattleExitByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_BattleExitByName")

function GetActivityDungeon1017Battle_BattleExitWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1017Battle_BattleExitUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_BattlePauseByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_BattlePauseUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetActivityDungeon1017Battle_BattlePauseUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.root = ui
  return uis
```

---

## Activty/a17/ActivityDungeon1017Battle_BattlePauseWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_BattlePauseWindowUis
**Requires:**
- ActivityDungeon1017Battle_BattlePauseByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_BattlePauseByName")

function GetActivityDungeon1017Battle_BattlePauseWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1017Battle_BattlePauseUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_BattleStartBgByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_BattleStartBgUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_BattleStartBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_BattleStartByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_BattleStartUis
**Requires:**
- ActivityDungeon1017Battle_BattleStartBgByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_BattleStartBgByName")

function GetActivityDungeon1017Battle_BattleStartUis(ui)
  local uis = {}
  uis.BattleStartBg = GetActivityDungeon1017Battle_BattleStartBgUis(ui:GetChild("BattleStartBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_BattleStartWaveBgByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_BattleStartWaveBgUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_BattleStartWaveBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_BattleTopByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_BattleTopUis
**Requires:**
- ActivityDungeon1017Battle_NumberByName
- ActivityDungeon1017Battle_ExpByName
- ActivityDungeon1017Battle_TimeByName
- ActivityDungeon1017Battle_ProgressByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_NumberByName")
require("ActivityDungeon1017Battle_ExpByName")
require("ActivityDungeon1017Battle_TimeByName")
require("ActivityDungeon1017Battle_ProgressByName")

function GetActivityDungeon1017Battle_BattleTopUis(ui)
  local uis = {}
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.PauseBtn = ui:GetChild("PauseBtn")
  uis.SpeedBtn = ui:GetChild("SpeedBtn")
```

---

## Activty/a17/ActivityDungeon1017Battle_BattleUIByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_BattleUIUis
**Requires:**
- ActivityDungeon1017Battle_BattleTopByName
- ActivityDungeon1017Battle_BottomByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_BattleTopByName")
require("ActivityDungeon1017Battle_BottomByName")

function GetActivityDungeon1017Battle_BattleUIUis(ui)
  local uis = {}
  uis.Top = GetActivityDungeon1017Battle_BattleTopUis(ui:GetChild("Top"))
  uis.Bottom = GetActivityDungeon1017Battle_BottomUis(ui:GetChild("Bottom"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_BattleUIWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_BattleUIWindowUis
**Requires:**
- ActivityDungeon1017Battle_BattleUIByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_BattleUIByName")

function GetActivityDungeon1017Battle_BattleUIWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1017Battle_BattleUIUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_BottomByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_BottomUis
**Requires:**
- ActivityDungeon1017Battle_DPSInfoSwitchByName
- ActivityDungeon1017Battle_BuildHPByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_DPSInfoSwitchByName")
require("ActivityDungeon1017Battle_BuildHPByName")

function GetActivityDungeon1017Battle_BottomUis(ui)
  local uis = {}
  uis.DPSInfoSwitch = GetActivityDungeon1017Battle_DPSInfoSwitchUis(ui:GetChild("DPSInfoSwitch"))
  uis.BuildHP = GetActivityDungeon1017Battle_BuildHPUis(ui:GetChild("BuildHP"))
  uis.CardList = ui:GetChild("CardList")
  uis.root = ui
  return uis
```

---

## Activty/a17/ActivityDungeon1017Battle_BuildHPByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_BuildHPUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_BuildHPUis(ui)
  local uis = {}
  
  uis.BuildHPProgressBar = ui:GetChild("BuildHPProgressBar")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.HPTxt = ui:GetChild("HPTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_BuildHPProgressBarByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_BuildHPProgressBarUis
**Requires:**
- ActivityDungeon1017Battle_BuildHPProgressFillByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_BuildHPProgressFillByName")

function GetActivityDungeon1017Battle_BuildHPProgressBarUis(ui)
  local uis = {}
  uis.bar = GetActivityDungeon1017Battle_BuildHPProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_BuildHPProgressFillByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_BuildHPProgressFillUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_BuildHPProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_Card_HeadBgByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_Card_HeadBgUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_Card_HeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_Card_HeadByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_Card_HeadUis
**Requires:**
- ActivityDungeon1017Battle_Card_HeadBgByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_Card_HeadBgByName")

function GetActivityDungeon1017Battle_Card_HeadUis(ui)
  local uis = {}
  uis.Bg = GetActivityDungeon1017Battle_Card_HeadBgUis(ui:GetChild("Bg"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.SkillList = ui:GetChild("SkillList")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a17/ActivityDungeon1017Battle_Card_HeadProgressBarByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_Card_HeadProgressBarUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_Card_HeadProgressBarUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_Card_HeadSkillByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_Card_HeadSkillUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_Card_HeadSkillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_CritHitNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_CritHitNumberUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_CritHitNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_CritHitNumberTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_CritHitNumberTipsUis
**Requires:**
- ActivityDungeon1017Battle_CritHitNumberByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_CritHitNumberByName")

function GetActivityDungeon1017Battle_CritHitNumberTipsUis(ui)
  local uis = {}
  uis.CritHitNumber = GetActivityDungeon1017Battle_CritHitNumberUis(ui:GetChild("CritHitNumber"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_DPS1ByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_DPS1Uis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_DPS1Uis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.DPSProgressBar = ui:GetChild("DPSProgressBar")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_DPS1ProgressBarByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_DPS1ProgressBarUis
**Requires:**
- ActivityDungeon1017Battle_DPS1ProgressFillByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_DPS1ProgressFillByName")

function GetActivityDungeon1017Battle_DPS1ProgressBarUis(ui)
  local uis = {}
  uis.bar = GetActivityDungeon1017Battle_DPS1ProgressFillUis(ui:GetChild("bar"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_DPS1ProgressFillByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_DPS1ProgressFillUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_DPS1ProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_DPS1RegionByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_DPS1RegionUis
**Requires:**
- ActivityDungeon1017Battle_DPS1ByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_DPS1ByName")

function GetActivityDungeon1017Battle_DPS1RegionUis(ui)
  local uis = {}
  uis.Card1 = GetActivityDungeon1017Battle_DPS1Uis(ui:GetChild("Card1"))
  uis.Card2 = GetActivityDungeon1017Battle_DPS1Uis(ui:GetChild("Card2"))
  uis.Card3 = GetActivityDungeon1017Battle_DPS1Uis(ui:GetChild("Card3"))
  uis.Card4 = GetActivityDungeon1017Battle_DPS1Uis(ui:GetChild("Card4"))
  uis.Card5 = GetActivityDungeon1017Battle_DPS1Uis(ui:GetChild("Card5"))
  uis.root = ui
```

---

## Activty/a17/ActivityDungeon1017Battle_DPSInfoSwitchByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_DPSInfoSwitchUis
**Requires:**
- ActivityDungeon1017Battle_DPS1RegionByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_DPS1RegionByName")

function GetActivityDungeon1017Battle_DPSInfoSwitchUis(ui)
  local uis = {}
  uis.DPS1 = GetActivityDungeon1017Battle_DPS1RegionUis(ui:GetChild("DPS1"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_ExpByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_ExpUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_ExpUis(ui)
  local uis = {}
  
  uis.ExpProgressBar = ui:GetChild("ExpProgressBar")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.ExpTxt = ui:GetChild("ExpTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_ExpProgressBarByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_ExpProgressBarUis
**Requires:**
- ActivityDungeon1017Battle_ExpProgressFillByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_ExpProgressFillByName")

function GetActivityDungeon1017Battle_ExpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetActivityDungeon1017Battle_ExpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_ExpProgressFillByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_ExpProgressFillUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_ExpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_GreenHpNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_GreenHpNumberUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_GreenHpNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_GreenHpNumberTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_GreenHpNumberTipsUis
**Requires:**
- ActivityDungeon1017Battle_GreenHpNumberByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_GreenHpNumberByName")

function GetActivityDungeon1017Battle_GreenHpNumberTipsUis(ui)
  local uis = {}
  uis.GreenHpNumber = GetActivityDungeon1017Battle_GreenHpNumberUis(ui:GetChild("GreenHpNumber"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_NormalHitNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_NormalHitNumberUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_NormalHitNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_NormalHitNumberTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_NormalHitNumberTipsUis
**Requires:**
- ActivityDungeon1017Battle_NormalHitNumberByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_NormalHitNumberByName")

function GetActivityDungeon1017Battle_NormalHitNumberTipsUis(ui)
  local uis = {}
  uis.NormalHitNumber = GetActivityDungeon1017Battle_NormalHitNumberUis(ui:GetChild("NormalHitNumber"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_NumberByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_NumberUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_NumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_PauseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_PauseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_PauseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_ProgressByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_ProgressUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_ProgressUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_ReturnBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_ReturnBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_ReturnBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_SkillChoiceByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_SkillChoiceUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1017Battle_SkillChoice_TimeByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1017Battle_SkillChoice_TimeByName")

function GetActivityDungeon1017Battle_SkillChoiceUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.Time = GetActivityDungeon1017Battle_SkillChoice_TimeUis(ui:GetChild("Time"))
  uis.root = ui
  return uis
```

---

## Activty/a17/ActivityDungeon1017Battle_SkillChoiceWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_SkillChoiceWindowUis
**Requires:**
- ActivityDungeon1017Battle_SkillChoiceByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_SkillChoiceByName")

function GetActivityDungeon1017Battle_SkillChoiceWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1017Battle_SkillChoiceUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_SkillChoice_CardBgByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_SkillChoice_CardBgUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_SkillChoice_CardBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_SkillChoice_CardByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_SkillChoice_CardUis
**Requires:**
- ActivityDungeon1017Battle_SkillChoice_CardBgByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_SkillChoice_CardBgByName")

function GetActivityDungeon1017Battle_SkillChoice_CardUis(ui)
  local uis = {}
  uis.PartsCardBg = GetActivityDungeon1017Battle_SkillChoice_CardBgUis(ui:GetChild("PartsCardBg"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_SkillChoice_SureBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_SkillChoice_SureBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_SkillChoice_SureBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_SkillChoice_Time1ProgressBarByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_SkillChoice_Time1ProgressBarUis
**Requires:**
- ActivityDungeon1017Battle_SkillChoice_Time1ProgressFillByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_SkillChoice_Time1ProgressFillByName")

function GetActivityDungeon1017Battle_SkillChoice_Time1ProgressBarUis(ui)
  local uis = {}
  uis.bar = GetActivityDungeon1017Battle_SkillChoice_Time1ProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_SkillChoice_Time1ProgressFillByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_SkillChoice_Time1ProgressFillUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_SkillChoice_Time1ProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_SkillChoice_Time2ProgressBarByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_SkillChoice_Time2ProgressBarUis
**Requires:**
- ActivityDungeon1017Battle_SkillChoice_Time2ProgressFillByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_SkillChoice_Time2ProgressFillByName")

function GetActivityDungeon1017Battle_SkillChoice_Time2ProgressBarUis(ui)
  local uis = {}
  uis.bar = GetActivityDungeon1017Battle_SkillChoice_Time2ProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_SkillChoice_Time2ProgressFillByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_SkillChoice_Time2ProgressFillUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_SkillChoice_Time2ProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_SkillChoice_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_SkillChoice_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_SkillChoice_TimeUis(ui)
  local uis = {}
  
  uis.Time1ProgressBar = ui:GetChild("Time1ProgressBar")
  uis.Time2ProgressBar = ui:GetChild("Time2ProgressBar")
  uis.SureBtn = ui:GetChild("SureBtn")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_SkillChoice_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_SkillChoice_TipsAniUis
**Requires:**
- ActivityDungeon1017Battle_SkillChoice_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_SkillChoice_TipsByName")

function GetActivityDungeon1017Battle_SkillChoice_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1017Battle_SkillChoice_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_SkillChoice_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_SkillChoice_TipsUis
**Requires:**
- ActivityDungeon1017Battle_SkillChoice_CardByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_SkillChoice_CardByName")

function GetActivityDungeon1017Battle_SkillChoice_TipsUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.Card = GetActivityDungeon1017Battle_SkillChoice_CardUis(ui:GetChild("Card"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## Activty/a17/ActivityDungeon1017Battle_SkillChoice_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_SkillChoice_WordUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_SkillChoice_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_SpeedBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_SpeedBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_SpeedBtnUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017Battle_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1017Battle_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1017Battle_TimeUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_ActivityDungeonByName.lua.lua
**Functions:**
- GetActivityDungeon1017_ActivityDungeonUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1017_MainTitleByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1017_MainTitleByName")
require("CommonResource_CurrencyReturnByName")

function GetActivityDungeon1017_ActivityDungeonUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.MainTitle = GetActivityDungeon1017_MainTitleUis(ui:GetChild("MainTitle"))
  uis.MiniGame1Btn = ui:GetChild("MiniGame1Btn")
  uis.MiniGameBtn = ui:GetChild("MiniGameBtn")
```

---

## Activty/a17/ActivityDungeon1017_ActivityDungeonWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1017_ActivityDungeonWindowUis
**Requires:**
- ActivityDungeon1017_ActivityDungeonByName
**Snippet:**
```lua
require("ActivityDungeon1017_ActivityDungeonByName")

function GetActivityDungeon1017_ActivityDungeonWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1017_ActivityDungeonUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_AddBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_AddBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_AddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_BossBattleByName.lua.lua
**Functions:**
- GetActivityDungeon1017_BossBattleUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1017_BossBattle_InfoByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1017_BossBattle_InfoByName")

function GetActivityDungeon1017_BossBattleUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.Info = GetActivityDungeon1017_BossBattle_InfoUis(ui:GetChild("Info"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a17/ActivityDungeon1017_BossBattleWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1017_BossBattleWindowUis
**Requires:**
- ActivityDungeon1017_BossBattleByName
**Snippet:**
```lua
require("ActivityDungeon1017_BossBattleByName")

function GetActivityDungeon1017_BossBattleWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1017_BossBattleUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_BossBattle_Info1ByName.lua.lua
**Functions:**
- GetActivityDungeon1017_BossBattle_Info1Uis
**Snippet:**
```lua
function GetActivityDungeon1017_BossBattle_Info1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_BossBattle_InfoByName.lua.lua
**Functions:**
- GetActivityDungeon1017_BossBattle_InfoUis
**Requires:**
- ActivityDungeon1017_BossBattle_Info1ByName
**Snippet:**
```lua
require("ActivityDungeon1017_BossBattle_Info1ByName")

function GetActivityDungeon1017_BossBattle_InfoUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = GetActivityDungeon1017_BossBattle_Info1Uis(ui:GetChild("WordTxt"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_BossBattle_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1017_BossBattle_TipsAniUis
**Requires:**
- ActivityDungeon1017_BossBattle_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1017_BossBattle_TipsByName")

function GetActivityDungeon1017_BossBattle_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1017_BossBattle_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_BossBattle_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1017_BossBattle_TipsUis
**Requires:**
- ActivityDungeon1017_BossBattle_TipsRewardByName
**Snippet:**
```lua
require("ActivityDungeon1017_BossBattle_TipsRewardByName")

function GetActivityDungeon1017_BossBattle_TipsUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1017_BossBattle_TipsRewardUis(ui:GetChild("Reward"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.NumberWordTxt = ui:GetChild("NumberWordTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a17/ActivityDungeon1017_BossBattle_TipsRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1017_BossBattle_TipsRewardUis
**Snippet:**
```lua
function GetActivityDungeon1017_BossBattle_TipsRewardUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_BossBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_BossBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1017_BossBtnUis(ui)
  local uis = {}
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.newCtr = ui:GetController("new")
```

---

## Activty/a17/ActivityDungeon1017_Box1BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Box1BtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_Box1BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Box2BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Box2BtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_Box2BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_BuyLevelBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_BuyLevelBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_BuyLevelBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_BuyLevelDes1ByName.lua.lua
**Functions:**
- GetActivityDungeon1017_BuyLevelDes1Uis
**Requires:**
- ActivityDungeon1017_NumberStripByName
- ActivityDungeon1017_BuyPriceNumberByName
**Snippet:**
```lua
require("ActivityDungeon1017_NumberStripByName")
require("ActivityDungeon1017_BuyPriceNumberByName")

function GetActivityDungeon1017_BuyLevelDes1Uis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.NumberStrip = GetActivityDungeon1017_NumberStripUis(ui:GetChild("NumberStrip"))
  uis.BuyPriceNumber = GetActivityDungeon1017_BuyPriceNumberUis(ui:GetChild("BuyPriceNumber"))
```

---

## Activty/a17/ActivityDungeon1017_BuyLevelDes2ByName.lua.lua
**Functions:**
- GetActivityDungeon1017_BuyLevelDes2Uis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1017_BuyLevelDes1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1017_BuyLevelDes1ByName")

function GetActivityDungeon1017_BuyLevelDes2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.BuyLevelDes1 = GetActivityDungeon1017_BuyLevelDes1Uis(ui:GetChild("BuyLevelDes1"))
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.root = ui
```

---

## Activty/a17/ActivityDungeon1017_BuyLevelDesWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1017_BuyLevelDesWindowUis
**Requires:**
- ActivityDungeon1017_BuyLevelDes2ByName
**Snippet:**
```lua
require("ActivityDungeon1017_BuyLevelDes2ByName")

function GetActivityDungeon1017_BuyLevelDesWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1017_BuyLevelDes2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_BuyLevelItemByName.lua.lua
**Functions:**
- GetActivityDungeon1017_BuyLevelItemUis
**Requires:**
- ActivityDungeon1017_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1017_PassReward_AllFrame_EByName")

function GetActivityDungeon1017_BuyLevelItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1017_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_BuyPriceNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1017_BuyPriceNumberUis
**Snippet:**
```lua
function GetActivityDungeon1017_BuyPriceNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_ChallengeByName.lua.lua
**Functions:**
- GetActivityDungeon1017_ChallengeUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1017_MapListByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1017_MapListByName")

function GetActivityDungeon1017_ChallengeUis(ui)
  local uis = {}
  uis.BgList = ui:GetChild("BgList")
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Map = GetActivityDungeon1017_MapListUis(ui:GetChild("Map"))
  uis.ShopBtn = ui:GetChild("ShopBtn")
  uis.ChapterList = ui:GetChild("ChapterList")
```

---

## Activty/a17/ActivityDungeon1017_ChallengeChapterBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_ChallengeChapterBtnUis
**Requires:**
- ActivityDungeon1017_NormalPointLockByName
**Snippet:**
```lua
require("ActivityDungeon1017_NormalPointLockByName")

function GetActivityDungeon1017_ChallengeChapterBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Lock = GetActivityDungeon1017_NormalPointLockUis(ui:GetChild("Lock"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Activty/a17/ActivityDungeon1017_ChallengeShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_ChallengeShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_ChallengeShopBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_ChallengeWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1017_ChallengeWindowUis
**Requires:**
- ActivityDungeon1017_ChallengeByName
**Snippet:**
```lua
require("ActivityDungeon1017_ChallengeByName")

function GetActivityDungeon1017_ChallengeWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1017_ChallengeUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_EventTipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1017_EventTipsAniUis
**Requires:**
- ActivityDungeon1017_EventTipsByName
**Snippet:**
```lua
require("ActivityDungeon1017_EventTipsByName")

function GetActivityDungeon1017_EventTipsAniUis(ui)
  local uis = {}
  uis.EventTips = GetActivityDungeon1017_EventTipsUis(ui:GetChild("EventTips"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_EventTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1017_EventTipsUis
**Snippet:**
```lua
function GetActivityDungeon1017_EventTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_EventTipsListByName.lua.lua
**Functions:**
- GetActivityDungeon1017_EventTipsListUis
**Snippet:**
```lua
function GetActivityDungeon1017_EventTipsListUis(ui)
  local uis = {}
  
  uis.EventTipsList = ui:GetChild("EventTipsList")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MainBuildSignByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MainBuildSignUis
**Snippet:**
```lua
function GetActivityDungeon1017_MainBuildSignUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MainSeasonsByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MainSeasonsUis
**Snippet:**
```lua
function GetActivityDungeon1017_MainSeasonsUis(ui)
  local uis = {}
  
  uis.BackGroundHolder = ui:GetChild("BackGroundHolder")
  uis.BackGround1Holder = ui:GetChild("BackGround1Holder")
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MainSeasonsWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MainSeasonsWindowUis
**Requires:**
- ActivityDungeon1017_MainSeasonsByName
**Snippet:**
```lua
require("ActivityDungeon1017_MainSeasonsByName")

function GetActivityDungeon1017_MainSeasonsWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1017_MainSeasonsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MainTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MainTitleUis
**Snippet:**
```lua
function GetActivityDungeon1017_MainTitleUis(ui)
  local uis = {}
  
  uis.Time1Txt = ui:GetChild("Time1Txt")
  uis.Time2Txt = ui:GetChild("Time2Txt")
  uis.reviewCtr = ui:GetController("review")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MapBottom_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MapBottom_1Uis
**Snippet:**
```lua
function GetActivityDungeon1017_MapBottom_1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MapBottom_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MapBottom_2Uis
**Snippet:**
```lua
function GetActivityDungeon1017_MapBottom_2Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MapBottom_3ByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MapBottom_3Uis
**Snippet:**
```lua
function GetActivityDungeon1017_MapBottom_3Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MapBottom_4ByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MapBottom_4Uis
**Snippet:**
```lua
function GetActivityDungeon1017_MapBottom_4Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MapListByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MapListUis
**Snippet:**
```lua
function GetActivityDungeon1017_MapListUis(ui)
  local uis = {}
  
  uis.MapList = ui:GetChild("MapList")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Map_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Map_1Uis
**Snippet:**
```lua
function GetActivityDungeon1017_Map_1Uis(ui)
  local uis = {}
  
  uis.Point1Btn = ui:GetChild("Point1Btn")
  uis.Point2Btn = ui:GetChild("Point2Btn")
  uis.Point3Btn = ui:GetChild("Point3Btn")
  uis.Point4Btn = ui:GetChild("Point4Btn")
  uis.Point5Btn = ui:GetChild("Point5Btn")
  uis.Point6Btn = ui:GetChild("Point6Btn")
  uis.Point7Btn = ui:GetChild("Point7Btn")
```

---

## Activty/a17/ActivityDungeon1017_Map_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Map_2Uis
**Snippet:**
```lua
function GetActivityDungeon1017_Map_2Uis(ui)
  local uis = {}
  
  uis.Point1Btn = ui:GetChild("Point1Btn")
  uis.Point2Btn = ui:GetChild("Point2Btn")
  uis.Point3Btn = ui:GetChild("Point3Btn")
  uis.Point4Btn = ui:GetChild("Point4Btn")
  uis.Point5Btn = ui:GetChild("Point5Btn")
  uis.Point6Btn = ui:GetChild("Point6Btn")
  uis.Point7Btn = ui:GetChild("Point7Btn")
```

---

## Activty/a17/ActivityDungeon1017_Map_3ByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Map_3Uis
**Snippet:**
```lua
function GetActivityDungeon1017_Map_3Uis(ui)
  local uis = {}
  
  uis.Point1Btn = ui:GetChild("Point1Btn")
  uis.Point2Btn = ui:GetChild("Point2Btn")
  uis.Point3Btn = ui:GetChild("Point3Btn")
  uis.Point4Btn = ui:GetChild("Point4Btn")
  uis.Point5Btn = ui:GetChild("Point5Btn")
  uis.Point6Btn = ui:GetChild("Point6Btn")
  uis.Point7Btn = ui:GetChild("Point7Btn")
```

---

## Activty/a17/ActivityDungeon1017_Map_4ByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Map_4Uis
**Snippet:**
```lua
function GetActivityDungeon1017_Map_4Uis(ui)
  local uis = {}
  
  uis.Point1Btn = ui:GetChild("Point1Btn")
  uis.Point2Btn = ui:GetChild("Point2Btn")
  uis.Point3Btn = ui:GetChild("Point3Btn")
  uis.Point4Btn = ui:GetChild("Point4Btn")
  uis.Point5Btn = ui:GetChild("Point5Btn")
  uis.Point6Btn = ui:GetChild("Point6Btn")
  uis.Point7Btn = ui:GetChild("Point7Btn")
```

---

## Activty/a17/ActivityDungeon1017_MaterialBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MaterialBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1017_MaterialBtnUis(ui)
  local uis = {}
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
```

---

## Activty/a17/ActivityDungeon1017_MaterialByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MaterialUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1017_Material_BattleNumberByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1017_Material_BattleNumberByName")

function GetActivityDungeon1017_MaterialUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.BattleNumber = GetActivityDungeon1017_Material_BattleNumberUis(ui:GetChild("BattleNumber"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a17/ActivityDungeon1017_MaterialWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MaterialWindowUis
**Requires:**
- ActivityDungeon1017_MaterialByName
**Snippet:**
```lua
require("ActivityDungeon1017_MaterialByName")

function GetActivityDungeon1017_MaterialWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1017_MaterialUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Material_BattleAniByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Material_BattleAniUis
**Requires:**
- ActivityDungeon1017_Material_BattleByName
**Snippet:**
```lua
require("ActivityDungeon1017_Material_BattleByName")

function GetActivityDungeon1017_Material_BattleAniUis(ui)
  local uis = {}
  uis.Battle = GetActivityDungeon1017_Material_BattleUis(ui:GetChild("Battle"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Material_BattleByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Material_BattleUis
**Snippet:**
```lua
function GetActivityDungeon1017_Material_BattleUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Material_BattleNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Material_BattleNumberUis
**Snippet:**
```lua
function GetActivityDungeon1017_Material_BattleNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MaxBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MaxBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_MaxBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MinBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MinBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_MinBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniGame1BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniGame1BtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1017_MiniGame1BtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniGame2ByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniGame2Uis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1017_MiniMain2_TopByName
- ActivityDungeon1017_MiniMain2_BottonByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1017_MiniMain2_TopByName")
require("ActivityDungeon1017_MiniMain2_BottonByName")

function GetActivityDungeon1017_MiniGame2Uis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Top = GetActivityDungeon1017_MiniMain2_TopUis(ui:GetChild("Top"))
  uis.Botton = GetActivityDungeon1017_MiniMain2_BottonUis(ui:GetChild("Botton"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a17/ActivityDungeon1017_MiniGame2WindowByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniGame2WindowUis
**Requires:**
- ActivityDungeon1017_MiniGame2ByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniGame2ByName")

function GetActivityDungeon1017_MiniGame2WindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1017_MiniGame2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniGameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniGameBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1017_MiniGameBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniGameByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniGameUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1017_MiniMain_TopByName
- ActivityDungeon1017_MiniMain_BottonByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1017_MiniMain_TopByName")
require("ActivityDungeon1017_MiniMain_BottonByName")

function GetActivityDungeon1017_MiniGameUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Top = GetActivityDungeon1017_MiniMain_TopUis(ui:GetChild("Top"))
  uis.Botton = GetActivityDungeon1017_MiniMain_BottonUis(ui:GetChild("Botton"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a17/ActivityDungeon1017_MiniGameChoice2ByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniGameChoice2Uis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1017_MiniGameChoice2_CardRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1017_MiniGameChoice2_CardRegionByName")

function GetActivityDungeon1017_MiniGameChoice2Uis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.CardRegion = GetActivityDungeon1017_MiniGameChoice2_CardRegionUis(ui:GetChild("CardRegion"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a17/ActivityDungeon1017_MiniGameChoice2WindowByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniGameChoice2WindowUis
**Requires:**
- ActivityDungeon1017_MiniGameChoice2ByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniGameChoice2ByName")

function GetActivityDungeon1017_MiniGameChoice2WindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1017_MiniGameChoice2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniGameChoice2_CardHeadBgByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniGameChoice2_CardHeadBgUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniGameChoice2_CardHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniGameChoice2_CardHeadByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniGameChoice2_CardHeadUis
**Requires:**
- ActivityDungeon1017_MiniGameChoice2_CardHeadBgByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniGameChoice2_CardHeadBgByName")

function GetActivityDungeon1017_MiniGameChoice2_CardHeadUis(ui)
  local uis = {}
  uis.Bg = GetActivityDungeon1017_MiniGameChoice2_CardHeadBgUis(ui:GetChild("Bg"))
  uis.c1Ctr = ui:GetController("c1")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniGameChoice2_CardInfo1ByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniGameChoice2_CardInfo1Uis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniGameChoice2_CardInfo1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.InfoList = ui:GetChild("InfoList")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniGameChoice2_CardInfo2ByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniGameChoice2_CardInfo2Uis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniGameChoice2_CardInfo2Uis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniGameChoice2_CardInfoByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniGameChoice2_CardInfoUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniGameChoice2_CardInfoUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.InfoList = ui:GetChild("InfoList")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniGameChoice2_CardInfoLockByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniGameChoice2_CardInfoLockUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniGameChoice2_CardInfoLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniGameChoice2_CardRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniGameChoice2_CardRegionUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniGameChoice2_CardRegionUis(ui)
  local uis = {}
  
  uis.HeadList = ui:GetChild("HeadList")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniGameChoice2_CloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniGameChoice2_CloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniGameChoice2_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniGameChoice2_InfoRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniGameChoice2_InfoRegionUis
**Requires:**
- ActivityDungeon1017_MiniGameChoice2_CardInfoLockByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniGameChoice2_CardInfoLockByName")

function GetActivityDungeon1017_MiniGameChoice2_InfoRegionUis(ui)
  local uis = {}
  uis.InfoList = ui:GetChild("InfoList")
  uis.Lock = GetActivityDungeon1017_MiniGameChoice2_CardInfoLockUis(ui:GetChild("Lock"))
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniGameChoice2_InfoSkillByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniGameChoice2_InfoSkillUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1017_MiniGameChoice2_InfoRegionByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1017_MiniGameChoice2_InfoRegionByName")

function GetActivityDungeon1017_MiniGameChoice2_InfoSkillUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Info = GetActivityDungeon1017_MiniGameChoice2_InfoRegionUis(ui:GetChild("Info"))
  uis.root = ui
  return uis
```

---

## Activty/a17/ActivityDungeon1017_MiniGameChoice2_InfoSkillWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniGameChoice2_InfoSkillWindowUis
**Requires:**
- ActivityDungeon1017_MiniGameChoice2_InfoSkillByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniGameChoice2_InfoSkillByName")

function GetActivityDungeon1017_MiniGameChoice2_InfoSkillWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1017_MiniGameChoice2_InfoSkillUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniGameChoice_LockByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniGameChoice_LockUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniGameChoice_LockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniGameChoice_MapByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniGameChoice_MapUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniGameChoice_MapUis(ui)
  local uis = {}
  
  uis.Tips1Btn = ui:GetChild("Tips1Btn")
  uis.Tips3Btn = ui:GetChild("Tips3Btn")
  uis.Tips5Btn = ui:GetChild("Tips5Btn")
  uis.Tips7Btn = ui:GetChild("Tips7Btn")
  uis.Tips9Btn = ui:GetChild("Tips9Btn")
  uis.Tips11Btn = ui:GetChild("Tips11Btn")
  uis.Tips13Btn = ui:GetChild("Tips13Btn")
```

---

## Activty/a17/ActivityDungeon1017_MiniGameChoice_Tips1BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniGameChoice_Tips1BtnUis
**Requires:**
- ActivityDungeon1017_MiniGameChoice_LockByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniGameChoice_LockByName")

function GetActivityDungeon1017_MiniGameChoice_Tips1BtnUis(ui)
  local uis = {}
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.Time = GetActivityDungeon1017_MiniGameChoice_LockUis(ui:GetChild("Time"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## Activty/a17/ActivityDungeon1017_MiniGameChoice_Tips2BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniGameChoice_Tips2BtnUis
**Requires:**
- ActivityDungeon1017_MiniGameChoice_LockByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniGameChoice_LockByName")

function GetActivityDungeon1017_MiniGameChoice_Tips2BtnUis(ui)
  local uis = {}
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.Time = GetActivityDungeon1017_MiniGameChoice_LockUis(ui:GetChild("Time"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## Activty/a17/ActivityDungeon1017_MiniGameChoice_Tips3BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniGameChoice_Tips3BtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniGameChoice_Tips3BtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniGameStartByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniGameStartUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1017_MiniStart_MapRegionByName
- ActivityDungeon1017_MiniStart_IntegralByName
- ActivityDungeon1017_MiniStart_InfoByName
- ActivityDungeon1017_MiniStart_JoystickByName
- ActivityDungeon1017_MiniStart_EffectTipsByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1017_MiniStart_MapRegionByName")
require("ActivityDungeon1017_MiniStart_IntegralByName")
require("ActivityDungeon1017_MiniStart_InfoByName")
require("ActivityDungeon1017_MiniStart_JoystickByName")
require("ActivityDungeon1017_MiniStart_EffectTipsByName")

function GetActivityDungeon1017_MiniGameStartUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
```

---

## Activty/a17/ActivityDungeon1017_MiniGameStartWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniGameStartWindowUis
**Requires:**
- ActivityDungeon1017_MiniGameStartByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniGameStartByName")

function GetActivityDungeon1017_MiniGameStartWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1017_MiniGameStartUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniGameWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniGameWindowUis
**Requires:**
- ActivityDungeon1017_MiniGameByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniGameByName")

function GetActivityDungeon1017_MiniGameWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1017_MiniGameUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniMain2_BottonByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniMain2_BottonUis
**Requires:**
- ActivityDungeon1017_MiniMain2_TodayTaskByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniMain2_TodayTaskByName")

function GetActivityDungeon1017_MiniMain2_BottonUis(ui)
  local uis = {}
  uis.TaskBtn = ui:GetChild("TaskBtn")
  uis.TodayTask = GetActivityDungeon1017_MiniMain2_TodayTaskUis(ui:GetChild("TodayTask"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniMain2_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniMain2_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniMain2_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniMain2_StartBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniMain2_StartBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniMain2_StartBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniMain2_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniMain2_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1017_MiniMain2_TaskBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniMain2_TodayTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniMain2_TodayTaskUis
**Requires:**
- ActivityDungeon1017_PassReward_AllFrame_EByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("ActivityDungeon1017_PassReward_AllFrame_EByName")
require("CommonResource_RedDotByName")

function GetActivityDungeon1017_MiniMain2_TodayTaskUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1017_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a17/ActivityDungeon1017_MiniMain2_TopByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniMain2_TopUis
**Requires:**
- ActivityDungeon1017_MiniMain2_IntegralByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniMain2_IntegralByName")

function GetActivityDungeon1017_MiniMain2_TopUis(ui)
  local uis = {}
  uis.Integral = GetActivityDungeon1017_MiniMain2_IntegralUis(ui:GetChild("Integral"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniMain_BottonByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniMain_BottonUis
**Requires:**
- ActivityDungeon1017_MiniMain_TodayTaskByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniMain_TodayTaskByName")

function GetActivityDungeon1017_MiniMain_BottonUis(ui)
  local uis = {}
  uis.TaskBtn = ui:GetChild("TaskBtn")
  uis.TodayTask = GetActivityDungeon1017_MiniMain_TodayTaskUis(ui:GetChild("TodayTask"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniMain_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniMain_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniMain_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniMain_ReturnBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniMain_ReturnBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniMain_ReturnBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniMain_SetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniMain_SetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniMain_SetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniMain_StartBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniMain_StartBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniMain_StartBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniMain_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniMain_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1017_MiniMain_TaskBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniMain_TodayTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniMain_TodayTaskUis
**Requires:**
- ActivityDungeon1017_PassReward_AllFrame_EByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("ActivityDungeon1017_PassReward_AllFrame_EByName")
require("CommonResource_RedDotByName")

function GetActivityDungeon1017_MiniMain_TodayTaskUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1017_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a17/ActivityDungeon1017_MiniMain_TopByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniMain_TopUis
**Requires:**
- ActivityDungeon1017_MiniMain_IntegralByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniMain_IntegralByName")

function GetActivityDungeon1017_MiniMain_TopUis(ui)
  local uis = {}
  uis.Integral = GetActivityDungeon1017_MiniMain_IntegralUis(ui:GetChild("Integral"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniOperateChoiceByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniOperateChoiceUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetActivityDungeon1017_MiniOperateChoiceUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.TipsList = ui:GetChild("TipsList")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.root = ui
  return uis
```

---

## Activty/a17/ActivityDungeon1017_MiniOperateChoiceWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniOperateChoiceWindowUis
**Requires:**
- ActivityDungeon1017_MiniOperateChoiceByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniOperateChoiceByName")

function GetActivityDungeon1017_MiniOperateChoiceWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1017_MiniOperateChoiceUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniOperateChoice_CloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniOperateChoice_CloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniOperateChoice_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniOperateChoice_TipsBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniOperateChoice_TipsBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniOperateChoice_TipsBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.joystickCtr = ui:GetController("joystick")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniStart_ArrowDownByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniStart_ArrowDownUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniStart_ArrowDownUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniStart_ArrowLeftByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniStart_ArrowLeftUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniStart_ArrowLeftUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniStart_ArrowRightByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniStart_ArrowRightUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniStart_ArrowRightUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniStart_ArrowUpByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniStart_ArrowUpUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniStart_ArrowUpUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniStart_EffectTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniStart_EffectTipsUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniStart_EffectTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniStart_EndAgainBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniStart_EndAgainBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniStart_EndAgainBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniStart_EndCloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniStart_EndCloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniStart_EndCloseBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniStart_EndRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniStart_EndRewardUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetActivityDungeon1017_MiniStart_EndRewardUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.AgainBtn = ui:GetChild("AgainBtn")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.EffectHolder = ui:GetChild("EffectHolder")
```

---

## Activty/a17/ActivityDungeon1017_MiniStart_EndRewardWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniStart_EndRewardWindowUis
**Requires:**
- ActivityDungeon1017_MiniStart_EndRewardByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniStart_EndRewardByName")

function GetActivityDungeon1017_MiniStart_EndRewardWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1017_MiniStart_EndRewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniStart_InfoByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniStart_InfoUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniStart_InfoUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniStart_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniStart_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniStart_IntegralUis(ui)
  local uis = {}
  
  uis.NumberWordTxt = ui:GetChild("NumberWordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.NumberWord1Txt = ui:GetChild("NumberWord1Txt")
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniStart_ItemAniByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniStart_ItemAniUis
**Requires:**
- ActivityDungeon1017_MiniStart_ItemByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniStart_ItemByName")

function GetActivityDungeon1017_MiniStart_ItemAniUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1017_MiniStart_ItemUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniStart_ItemByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniStart_ItemUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniStart_ItemUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.itemCtr = ui:GetController("item")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniStart_JoystickByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniStart_JoystickUis
**Requires:**
- ActivityDungeon1017_MiniStart_ArrowUpByName
- ActivityDungeon1017_MiniStart_ArrowDownByName
- ActivityDungeon1017_MiniStart_ArrowLeftByName
- ActivityDungeon1017_MiniStart_ArrowRightByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniStart_ArrowUpByName")
require("ActivityDungeon1017_MiniStart_ArrowDownByName")
require("ActivityDungeon1017_MiniStart_ArrowLeftByName")
require("ActivityDungeon1017_MiniStart_ArrowRightByName")

function GetActivityDungeon1017_MiniStart_JoystickUis(ui)
  local uis = {}
  uis.Up = GetActivityDungeon1017_MiniStart_ArrowUpUis(ui:GetChild("Up"))
  uis.Down = GetActivityDungeon1017_MiniStart_ArrowDownUis(ui:GetChild("Down"))
  uis.Left = GetActivityDungeon1017_MiniStart_ArrowLeftUis(ui:GetChild("Left"))
```

---

## Activty/a17/ActivityDungeon1017_MiniStart_MapRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniStart_MapRegionUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniStart_MapRegionUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniStart_PlayerByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniStart_PlayerUis
**Requires:**
- ActivityDungeon1017_MiniStart_PlayerDotByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniStart_PlayerDotByName")

function GetActivityDungeon1017_MiniStart_PlayerUis(ui)
  local uis = {}
  uis.Dot = GetActivityDungeon1017_MiniStart_PlayerDotUis(ui:GetChild("Dot"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniStart_PlayerDotByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniStart_PlayerDotUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniStart_PlayerDotUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniTask2ByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniTask2Uis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1017_MiniTask2_IntegralByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1017_MiniTask2_IntegralByName")

function GetActivityDungeon1017_MiniTask2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Integral = GetActivityDungeon1017_MiniTask2_IntegralUis(ui:GetChild("Integral"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a17/ActivityDungeon1017_MiniTask2WindowByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniTask2WindowUis
**Requires:**
- ActivityDungeon1017_MiniTask2ByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniTask2ByName")

function GetActivityDungeon1017_MiniTask2WindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1017_MiniTask2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniTask2_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniTask2_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniTask2_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniTask2_RewardItemGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniTask2_RewardItemGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniTask2_RewardItemGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniTask2_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniTask2_TipsAniUis
**Requires:**
- ActivityDungeon1017_MiniTask2_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniTask2_TipsByName")

function GetActivityDungeon1017_MiniTask2_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1017_MiniTask2_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniTask2_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniTask2_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniTask2_TipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.ItemList = ui:GetChild("ItemList")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a17/ActivityDungeon1017_MiniTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniTaskUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1017_MiniTask_IntegralByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1017_MiniTask_IntegralByName")

function GetActivityDungeon1017_MiniTaskUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Integral = GetActivityDungeon1017_MiniTask_IntegralUis(ui:GetChild("Integral"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a17/ActivityDungeon1017_MiniTaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniTaskWindowUis
**Requires:**
- ActivityDungeon1017_MiniTaskByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniTaskByName")

function GetActivityDungeon1017_MiniTaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1017_MiniTaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniTask_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniTask_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniTask_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniTask_RewardItemGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniTask_RewardItemGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniTask_RewardItemGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniTask_TipsAniUis
**Requires:**
- ActivityDungeon1017_MiniTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniTask_TipsByName")

function GetActivityDungeon1017_MiniTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1017_MiniTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_MiniTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1017_MiniTask_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1017_MiniTask_TipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.ItemList = ui:GetChild("ItemList")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a17/ActivityDungeon1017_NormalBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_NormalBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_NormalBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_NormalPoint1BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_NormalPoint1BtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_NormalPoint1BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_NormalPoint2BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_NormalPoint2BtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_NormalPoint2BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_NormalPoint3BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_NormalPoint3BtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_NormalPoint3BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_NormalPoint4BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_NormalPoint4BtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_NormalPoint4BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_NormalPointLockByName.lua.lua
**Functions:**
- GetActivityDungeon1017_NormalPointLockUis
**Snippet:**
```lua
function GetActivityDungeon1017_NormalPointLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_NumberStripByName.lua.lua
**Functions:**
- GetActivityDungeon1017_NumberStripUis
**Snippet:**
```lua
function GetActivityDungeon1017_NumberStripUis(ui)
  local uis = {}
  
  uis.ChoiceNumberTxt = ui:GetChild("ChoiceNumberTxt")
  uis.ReduceBtn = ui:GetChild("ReduceBtn")
  uis.AddBtn = ui:GetChild("AddBtn")
  uis.MinBtn = ui:GetChild("MinBtn")
  uis.MaxBtn = ui:GetChild("MaxBtn")
  uis.root = ui
  return uis
```

---

## Activty/a17/ActivityDungeon1017_PassBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1017_PassBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_PassClothes_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassClothes_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_PassClothes_BuyBtnUis(ui)
  local uis = {}
  
  uis.PriceTxt = ui:GetChild("PriceTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_PassClothes_BuyRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassClothes_BuyRewardUis
**Snippet:**
```lua
function GetActivityDungeon1017_PassClothes_BuyRewardUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.RewardList = ui:GetChild("RewardList")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_PassClothes_CardQBByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassClothes_CardQBUis
**Snippet:**
```lua
function GetActivityDungeon1017_PassClothes_CardQBUis(ui)
  local uis = {}
  
  uis.QBHolder = ui:GetChild("QBHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_PassClothes_ClothseRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassClothes_ClothseRegionUis
**Requires:**
- ActivityDungeon1017_PassClothes_WordByName
- ActivityDungeon1017_PassClothes_CardQBByName
- ActivityDungeon1017_PassClothes_BuyRewardByName
**Snippet:**
```lua
require("ActivityDungeon1017_PassClothes_WordByName")
require("ActivityDungeon1017_PassClothes_CardQBByName")
require("ActivityDungeon1017_PassClothes_BuyRewardByName")

function GetActivityDungeon1017_PassClothes_ClothseRegionUis(ui)
  local uis = {}
  uis.Word = GetActivityDungeon1017_PassClothes_WordUis(ui:GetChild("Word"))
  uis.CardQB = GetActivityDungeon1017_PassClothes_CardQBUis(ui:GetChild("CardQB"))
  uis.BuyReward = GetActivityDungeon1017_PassClothes_BuyRewardUis(ui:GetChild("BuyReward"))
  uis.BuyBtn = ui:GetChild("BuyBtn")
```

---

## Activty/a17/ActivityDungeon1017_PassClothes_NameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassClothes_NameBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_PassClothes_NameBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_PassClothes_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassClothes_WordUis
**Snippet:**
```lua
function GetActivityDungeon1017_PassClothes_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_PassportByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassportUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1017_PassReward_RewardRegionByName
- ActivityDungeon1017_PassTask_TaskRegionByName
- ActivityDungeon1017_PassClothes_ClothseRegionByName
- ActivityDungeon1017_Passport_LevelByName
- ActivityDungeon1017_Sign_TimeByName
- ActivityDungeon1017_Passport_TabRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1017_PassReward_RewardRegionByName")
require("ActivityDungeon1017_PassTask_TaskRegionByName")
require("ActivityDungeon1017_PassClothes_ClothseRegionByName")
require("ActivityDungeon1017_Passport_LevelByName")
require("ActivityDungeon1017_Sign_TimeByName")
require("ActivityDungeon1017_Passport_TabRegionByName")

function GetActivityDungeon1017_PassportUis(ui)
  local uis = {}
```

---

## Activty/a17/ActivityDungeon1017_PassportUp_LevelUpBgByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassportUp_LevelUpBgUis
**Snippet:**
```lua
function GetActivityDungeon1017_PassportUp_LevelUpBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_PassportUp_LevelUpTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassportUp_LevelUpTipsUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1017_PassportUp_LevelUpBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1017_PassportUp_LevelUpBgByName")

function GetActivityDungeon1017_PassportUp_LevelUpTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.LevelUpBg = GetActivityDungeon1017_PassportUp_LevelUpBgUis(ui:GetChild("LevelUpBg"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
```

---

## Activty/a17/ActivityDungeon1017_PassportUp_LevelUpTipsWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassportUp_LevelUpTipsWindowUis
**Requires:**
- ActivityDungeon1017_PassportUp_LevelUpTipsByName
**Snippet:**
```lua
require("ActivityDungeon1017_PassportUp_LevelUpTipsByName")

function GetActivityDungeon1017_PassportUp_LevelUpTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1017_PassportUp_LevelUpTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_PassportWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassportWindowUis
**Requires:**
- ActivityDungeon1017_PassportByName
**Snippet:**
```lua
require("ActivityDungeon1017_PassportByName")

function GetActivityDungeon1017_PassportWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1017_PassportUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Passport_AllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Passport_AllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_Passport_AllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Passport_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Passport_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_Passport_BuyBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Passport_ExpProgressBarByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Passport_ExpProgressBarUis
**Requires:**
- ActivityDungeon1017_Passport_ExpProgressFillByName
**Snippet:**
```lua
require("ActivityDungeon1017_Passport_ExpProgressFillByName")

function GetActivityDungeon1017_Passport_ExpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetActivityDungeon1017_Passport_ExpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Passport_ExpProgressFillByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Passport_ExpProgressFillUis
**Snippet:**
```lua
function GetActivityDungeon1017_Passport_ExpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Passport_LevelByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Passport_LevelUis
**Snippet:**
```lua
function GetActivityDungeon1017_Passport_LevelUis(ui)
  local uis = {}
  
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.ExpNumberTxt = ui:GetChild("ExpNumberTxt")
  uis.ExpProgressBar = ui:GetChild("ExpProgressBar")
  uis.LevelBuyBtn = ui:GetChild("LevelBuyBtn")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Passport_TabBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Passport_TabBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1017_Passport_TabBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## Activty/a17/ActivityDungeon1017_Passport_TabRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Passport_TabRegionUis
**Snippet:**
```lua
function GetActivityDungeon1017_Passport_TabRegionUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_PassReward_AllFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassReward_AllFrame_EUis
**Requires:**
- ActivityDungeon1017_PassReward_ItemFrame_EByName
- ActivityDungeon1017_PassReward_CardFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1017_PassReward_ItemFrame_EByName")
require("ActivityDungeon1017_PassReward_CardFrame_EByName")

function GetActivityDungeon1017_PassReward_AllFrame_EUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1017_PassReward_ItemFrame_EUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1017_PassReward_CardFrame_EUis(ui:GetChild("CardFrame"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## Activty/a17/ActivityDungeon1017_PassReward_AllFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassReward_AllFrame_MUis
**Requires:**
- ActivityDungeon1017_PassReward_ItemFrame_MByName
- ActivityDungeon1017_PassReward_CardFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1017_PassReward_ItemFrame_MByName")
require("ActivityDungeon1017_PassReward_CardFrame_MByName")

function GetActivityDungeon1017_PassReward_AllFrame_MUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1017_PassReward_ItemFrame_MUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1017_PassReward_CardFrame_MUis(ui:GetChild("CardFrame"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a17/ActivityDungeon1017_PassReward_CardFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassReward_CardFrame_EUis
**Requires:**
- ActivityDungeon1017_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1017_PassReward_ItemCardPicByName")

function GetActivityDungeon1017_PassReward_CardFrame_EUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1017_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a17/ActivityDungeon1017_PassReward_CardFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassReward_CardFrame_MUis
**Requires:**
- ActivityDungeon1017_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1017_PassReward_ItemCardPicByName")

function GetActivityDungeon1017_PassReward_CardFrame_MUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1017_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a17/ActivityDungeon1017_PassReward_EndTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassReward_EndTwoUis
**Requires:**
- ActivityDungeon1017_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1017_PassReward_AllFrame_EByName")

function GetActivityDungeon1017_PassReward_EndTwoUis(ui)
  local uis = {}
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.Item1 = GetActivityDungeon1017_PassReward_AllFrame_EUis(ui:GetChild("Item1"))
  uis.Item2 = GetActivityDungeon1017_PassReward_AllFrame_EUis(ui:GetChild("Item2"))
  uis.root = ui
```

---

## Activty/a17/ActivityDungeon1017_PassReward_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassReward_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1017_PassReward_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_PassReward_ItemFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassReward_ItemFrame_EUis
**Snippet:**
```lua
function GetActivityDungeon1017_PassReward_ItemFrame_EUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a17/ActivityDungeon1017_PassReward_ItemFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassReward_ItemFrame_MUis
**Snippet:**
```lua
function GetActivityDungeon1017_PassReward_ItemFrame_MUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a17/ActivityDungeon1017_PassReward_LevelTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassReward_LevelTitleUis
**Snippet:**
```lua
function GetActivityDungeon1017_PassReward_LevelTitleUis(ui)
  local uis = {}
  
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_PassReward_MiddleRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassReward_MiddleRegionUis
**Snippet:**
```lua
function GetActivityDungeon1017_PassReward_MiddleRegionUis(ui)
  local uis = {}
  
  uis.MiddleList = ui:GetChild("MiddleList")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_PassReward_MidTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassReward_MidTwoUis
**Requires:**
- ActivityDungeon1017_PassReward_MidTwoItemByName
- ActivityDungeon1017_PassReward_LevelTitleByName
**Snippet:**
```lua
require("ActivityDungeon1017_PassReward_MidTwoItemByName")
require("ActivityDungeon1017_PassReward_LevelTitleByName")

function GetActivityDungeon1017_PassReward_MidTwoUis(ui)
  local uis = {}
  uis.Reward1 = GetActivityDungeon1017_PassReward_MidTwoItemUis(ui:GetChild("Reward1"))
  uis.Reward2 = GetActivityDungeon1017_PassReward_MidTwoItemUis(ui:GetChild("Reward2"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Title = GetActivityDungeon1017_PassReward_LevelTitleUis(ui:GetChild("Title"))
```

---

## Activty/a17/ActivityDungeon1017_PassReward_MidTwoItemByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassReward_MidTwoItemUis
**Requires:**
- ActivityDungeon1017_PassReward_AllFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1017_PassReward_AllFrame_MByName")

function GetActivityDungeon1017_PassReward_MidTwoItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1017_PassReward_AllFrame_MUis(ui:GetChild("Item"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_PassReward_PicByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassReward_PicUis
**Snippet:**
```lua
function GetActivityDungeon1017_PassReward_PicUis(ui)
  local uis = {}
  
  uis.BuyTxt = ui:GetChild("BuyTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_PassReward_RewardRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassReward_RewardRegionUis
**Requires:**
- ActivityDungeon1017_PassReward_MiddleRegionByName
- ActivityDungeon1017_PassReward_StartTwoByName
- ActivityDungeon1017_PassReward_EndTwoByName
**Snippet:**
```lua
require("ActivityDungeon1017_PassReward_MiddleRegionByName")
require("ActivityDungeon1017_PassReward_StartTwoByName")
require("ActivityDungeon1017_PassReward_EndTwoByName")

function GetActivityDungeon1017_PassReward_RewardRegionUis(ui)
  local uis = {}
  uis.MiddleList = GetActivityDungeon1017_PassReward_MiddleRegionUis(ui:GetChild("MiddleList"))
  uis.StartTwo = GetActivityDungeon1017_PassReward_StartTwoUis(ui:GetChild("StartTwo"))
  uis.EndTwo = GetActivityDungeon1017_PassReward_EndTwoUis(ui:GetChild("EndTwo"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a17/ActivityDungeon1017_PassReward_StartTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassReward_StartTwoUis
**Requires:**
- ActivityDungeon1017_PassReward_PicByName
**Snippet:**
```lua
require("ActivityDungeon1017_PassReward_PicByName")

function GetActivityDungeon1017_PassReward_StartTwoUis(ui)
  local uis = {}
  uis.Pic = GetActivityDungeon1017_PassReward_PicUis(ui:GetChild("Pic"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_PassTask_TaskRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassTask_TaskRegionUis
**Requires:**
- ActivityDungeon1017_TaskMaxByName
**Snippet:**
```lua
require("ActivityDungeon1017_TaskMaxByName")

function GetActivityDungeon1017_PassTask_TaskRegionUis(ui)
  local uis = {}
  uis.TipsList = ui:GetChild("TipsList")
  uis.Max = GetActivityDungeon1017_TaskMaxUis(ui:GetChild("Max"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_PassTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassTask_TipsAniUis
**Requires:**
- ActivityDungeon1017_PassTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1017_PassTask_TipsByName")

function GetActivityDungeon1017_PassTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1017_PassTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_PassTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassTask_TipsUis
**Requires:**
- ActivityDungeon1017_PassTask_TipsIntegralByName
**Snippet:**
```lua
require("ActivityDungeon1017_PassTask_TipsIntegralByName")

function GetActivityDungeon1017_PassTask_TipsUis(ui)
  local uis = {}
  uis.ProgressTxt = ui:GetChild("ProgressTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Integral = GetActivityDungeon1017_PassTask_TipsIntegralUis(ui:GetChild("Integral"))
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a17/ActivityDungeon1017_PassTask_TipsIntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PassTask_TipsIntegralUis
**Snippet:**
```lua
function GetActivityDungeon1017_PassTask_TipsIntegralUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_PlotBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PlotBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_PlotBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_PlotByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PlotUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1017_Plot_WordByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1017_Plot_WordByName")

function GetActivityDungeon1017_PlotUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Word = GetActivityDungeon1017_Plot_WordUis(ui:GetChild("Word"))
  uis.PlotList = ui:GetChild("PlotList")
  uis.ProspectBtn = ui:GetChild("ProspectBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a17/ActivityDungeon1017_PlotWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1017_PlotWindowUis
**Requires:**
- ActivityDungeon1017_PlotByName
**Snippet:**
```lua
require("ActivityDungeon1017_PlotByName")

function GetActivityDungeon1017_PlotWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1017_PlotUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Plot_ProspectBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Plot_ProspectBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_Plot_ProspectBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Plot_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Plot_TipsAniUis
**Requires:**
- ActivityDungeon1017_Plot_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1017_Plot_TipsByName")

function GetActivityDungeon1017_Plot_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1017_Plot_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Plot_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Plot_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1017_Plot_TipsUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Plot_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Plot_WordUis
**Snippet:**
```lua
function GetActivityDungeon1017_Plot_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_ReduceBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_ReduceBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_ReduceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_ReviewWordByName.lua.lua
**Functions:**
- GetActivityDungeon1017_ReviewWordUis
**Snippet:**
```lua
function GetActivityDungeon1017_ReviewWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_ShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_ShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_ShopBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_ShopByName.lua.lua
**Functions:**
- GetActivityDungeon1017_ShopUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1017_Shop_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1017_Shop_TimeByName")

function GetActivityDungeon1017_ShopUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Time = GetActivityDungeon1017_Shop_TimeUis(ui:GetChild("Time"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a17/ActivityDungeon1017_ShopWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1017_ShopWindowUis
**Requires:**
- ActivityDungeon1017_ShopByName
**Snippet:**
```lua
require("ActivityDungeon1017_ShopByName")

function GetActivityDungeon1017_ShopWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1017_ShopUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Shop_CardHeadBgByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Shop_CardHeadBgUis
**Snippet:**
```lua
function GetActivityDungeon1017_Shop_CardHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Shop_ItemAniByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Shop_ItemAniUis
**Requires:**
- ActivityDungeon1017_Shop_ItemByName
**Snippet:**
```lua
require("ActivityDungeon1017_Shop_ItemByName")

function GetActivityDungeon1017_Shop_ItemAniUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1017_Shop_ItemUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Shop_ItemBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Shop_ItemBtnUis
**Requires:**
- ActivityDungeon1017_Shop_CardHeadBgByName
- ActivityDungeon1017_Shop_ItemNumberByName
- ActivityDungeon1017_Shop_UseMarkByName
**Snippet:**
```lua
require("ActivityDungeon1017_Shop_CardHeadBgByName")
require("ActivityDungeon1017_Shop_ItemNumberByName")
require("ActivityDungeon1017_Shop_UseMarkByName")

function GetActivityDungeon1017_Shop_ItemBtnUis(ui)
  local uis = {}
  uis.CardHeadBg = GetActivityDungeon1017_Shop_CardHeadBgUis(ui:GetChild("CardHeadBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.ItemNumber = GetActivityDungeon1017_Shop_ItemNumberUis(ui:GetChild("ItemNumber"))
```

---

## Activty/a17/ActivityDungeon1017_Shop_ItemByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Shop_ItemUis
**Requires:**
- ActivityDungeon1017_Shop_SellOutByName
**Snippet:**
```lua
require("ActivityDungeon1017_Shop_SellOutByName")

function GetActivityDungeon1017_Shop_ItemUis(ui)
  local uis = {}
  uis.ItemBtn = ui:GetChild("ItemBtn")
  uis.SellOut = GetActivityDungeon1017_Shop_SellOutUis(ui:GetChild("SellOut"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Shop_ItemNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Shop_ItemNumberUis
**Snippet:**
```lua
function GetActivityDungeon1017_Shop_ItemNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Shop_ItemRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Shop_ItemRegionUis
**Requires:**
- ActivityDungeon1017_Shop_TitleByName
**Snippet:**
```lua
require("ActivityDungeon1017_Shop_TitleByName")

function GetActivityDungeon1017_Shop_ItemRegionUis(ui)
  local uis = {}
  uis.ShopTitle = GetActivityDungeon1017_Shop_TitleUis(ui:GetChild("ShopTitle"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Shop_SellOutByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Shop_SellOutUis
**Snippet:**
```lua
function GetActivityDungeon1017_Shop_SellOutUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Shop_StarByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Shop_StarUis
**Snippet:**
```lua
function GetActivityDungeon1017_Shop_StarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Shop_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Shop_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1017_Shop_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Shop_TitleByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Shop_TitleUis
**Snippet:**
```lua
function GetActivityDungeon1017_Shop_TitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Shop_UseMarkByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Shop_UseMarkUis
**Snippet:**
```lua
function GetActivityDungeon1017_Shop_UseMarkUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_SignBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_SignBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1017_SignBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_SignByName.lua.lua
**Functions:**
- GetActivityDungeon1017_SignUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1017_Sign_RewardListByName
- ActivityDungeon1017_Sign_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1017_Sign_RewardListByName")
require("ActivityDungeon1017_Sign_TimeByName")

function GetActivityDungeon1017_SignUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.RewardList = GetActivityDungeon1017_Sign_RewardListUis(ui:GetChild("RewardList"))
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.Time = GetActivityDungeon1017_Sign_TimeUis(ui:GetChild("Time"))
```

---

## Activty/a17/ActivityDungeon1017_SignWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1017_SignWindowUis
**Requires:**
- ActivityDungeon1017_SignByName
**Snippet:**
```lua
require("ActivityDungeon1017_SignByName")

function GetActivityDungeon1017_SignWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1017_SignUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Sign_AllFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Sign_AllFrameUis
**Requires:**
- ActivityDungeon1017_Sign_ItemFrameByName
- ActivityDungeon1017_Sign_CardFrameByName
**Snippet:**
```lua
require("ActivityDungeon1017_Sign_ItemFrameByName")
require("ActivityDungeon1017_Sign_CardFrameByName")

function GetActivityDungeon1017_Sign_AllFrameUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1017_Sign_ItemFrameUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1017_Sign_CardFrameUis(ui:GetChild("CardFrame"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a17/ActivityDungeon1017_Sign_CardFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Sign_CardFrameUis
**Requires:**
- ActivityDungeon1017_Sign_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1017_Sign_ItemCardPicByName")

function GetActivityDungeon1017_Sign_CardFrameUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1017_Sign_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a17/ActivityDungeon1017_Sign_GetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Sign_GetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_Sign_GetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Sign_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Sign_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1017_Sign_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Sign_ItemFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Sign_ItemFrameUis
**Snippet:**
```lua
function GetActivityDungeon1017_Sign_ItemFrameUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a17/ActivityDungeon1017_Sign_RewardAniByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Sign_RewardAniUis
**Requires:**
- ActivityDungeon1017_Sign_RewardByName
**Snippet:**
```lua
require("ActivityDungeon1017_Sign_RewardByName")

function GetActivityDungeon1017_Sign_RewardAniUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1017_Sign_RewardUis(ui:GetChild("Reward"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Sign_RewardByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Sign_RewardUis
**Requires:**
- ActivityDungeon1017_Sign_AllFrameByName
**Snippet:**
```lua
require("ActivityDungeon1017_Sign_AllFrameByName")

function GetActivityDungeon1017_Sign_RewardUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1017_Sign_AllFrameUis(ui:GetChild("Item"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Sign_RewardListByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Sign_RewardListUis
**Snippet:**
```lua
function GetActivityDungeon1017_Sign_RewardListUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_Sign_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1017_Sign_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1017_Sign_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_TaskAllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_TaskAllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_TaskAllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1017_TaskBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_TaskByName.lua.lua
**Functions:**
- GetActivityDungeon1017_TaskUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1017_TaskTitleByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1017_TaskTitleByName")

function GetActivityDungeon1017_TaskUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TaskTitle = GetActivityDungeon1017_TaskTitleUis(ui:GetChild("TaskTitle"))
  uis.TaskTipsList = ui:GetChild("TaskTipsList")
  uis.AllGetBtn = ui:GetChild("AllGetBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a17/ActivityDungeon1017_TaskGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_TaskGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1017_TaskGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_TaskMaxByName.lua.lua
**Functions:**
- GetActivityDungeon1017_TaskMaxUis
**Snippet:**
```lua
function GetActivityDungeon1017_TaskMaxUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_TaskProgressByName.lua.lua
**Functions:**
- GetActivityDungeon1017_TaskProgressUis
**Snippet:**
```lua
function GetActivityDungeon1017_TaskProgressUis(ui)
  local uis = {}
  
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_TaskTipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1017_TaskTipsAniUis
**Requires:**
- ActivityDungeon1017_TaskTipsByName
**Snippet:**
```lua
require("ActivityDungeon1017_TaskTipsByName")

function GetActivityDungeon1017_TaskTipsAniUis(ui)
  local uis = {}
  uis.TaskTips = GetActivityDungeon1017_TaskTipsUis(ui:GetChild("TaskTips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_TaskTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1017_TaskTipsUis
**Requires:**
- ActivityDungeon1017_TaskProgressByName
**Snippet:**
```lua
require("ActivityDungeon1017_TaskProgressByName")

function GetActivityDungeon1017_TaskTipsUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.RewardList = ui:GetChild("RewardList")
  uis.TaskProgress = GetActivityDungeon1017_TaskProgressUis(ui:GetChild("TaskProgress"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a17/ActivityDungeon1017_TaskTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1017_TaskTitleUis
**Snippet:**
```lua
function GetActivityDungeon1017_TaskTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_TaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1017_TaskWindowUis
**Requires:**
- ActivityDungeon1017_TaskByName
**Snippet:**
```lua
require("ActivityDungeon1017_TaskByName")

function GetActivityDungeon1017_TaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1017_TaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_TreasureArrowByName.lua.lua
**Functions:**
- GetActivityDungeon1017_TreasureArrowUis
**Snippet:**
```lua
function GetActivityDungeon1017_TreasureArrowUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a17/ActivityDungeon1017_TreasureBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1017_TreasureBtnUis
**Requires:**
- ActivityDungeon1017_TreasureArrowByName
**Snippet:**
```lua
require("ActivityDungeon1017_TreasureArrowByName")

function GetActivityDungeon1017_TreasureBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Arrow = GetActivityDungeon1017_TreasureArrowUis(ui:GetChild("Arrow"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---
