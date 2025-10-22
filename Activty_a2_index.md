# Activty/a2

## Activty/a2/ActivityDungeon1002_ActivityDungeonByName.lua.lua
**Functions:**
- GetActivityDungeon1002_ActivityDungeonUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1002_MainTitleByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1002_MainTitleByName")
require("CommonResource_CurrencyReturnByName")

function GetActivityDungeon1002_ActivityDungeonUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.MainTitle = GetActivityDungeon1002_MainTitleUis(ui:GetChild("MainTitle"))
  uis.PlotBtn = ui:GetChild("PlotBtn")
  uis.TaskBtn = ui:GetChild("TaskBtn")
```

---

## Activty/a2/ActivityDungeon1002_ActivityDungeonWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1002_ActivityDungeonWindowUis
**Requires:**
- ActivityDungeon1002_ActivityDungeonByName
**Snippet:**
```lua
require("ActivityDungeon1002_ActivityDungeonByName")

function GetActivityDungeon1002_ActivityDungeonWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1002_ActivityDungeonUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_AddBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_AddBtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_AddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_BossBattleByName.lua.lua
**Functions:**
- GetActivityDungeon1002_BossBattleUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1002_BossBattle_InfoByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1002_BossBattle_InfoByName")

function GetActivityDungeon1002_BossBattleUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.Info = GetActivityDungeon1002_BossBattle_InfoUis(ui:GetChild("Info"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a2/ActivityDungeon1002_BossBattleWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1002_BossBattleWindowUis
**Requires:**
- ActivityDungeon1002_BossBattleByName
**Snippet:**
```lua
require("ActivityDungeon1002_BossBattleByName")

function GetActivityDungeon1002_BossBattleWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1002_BossBattleUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_BossBattle_Info1ByName.lua.lua
**Functions:**
- GetActivityDungeon1002_BossBattle_Info1Uis
**Snippet:**
```lua
function GetActivityDungeon1002_BossBattle_Info1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_BossBattle_InfoByName.lua.lua
**Functions:**
- GetActivityDungeon1002_BossBattle_InfoUis
**Requires:**
- ActivityDungeon1002_BossBattle_Info1ByName
**Snippet:**
```lua
require("ActivityDungeon1002_BossBattle_Info1ByName")

function GetActivityDungeon1002_BossBattle_InfoUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = GetActivityDungeon1002_BossBattle_Info1Uis(ui:GetChild("WordTxt"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_BossBattle_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1002_BossBattle_TipsAniUis
**Requires:**
- ActivityDungeon1002_BossBattle_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1002_BossBattle_TipsByName")

function GetActivityDungeon1002_BossBattle_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1002_BossBattle_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_BossBattle_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1002_BossBattle_TipsUis
**Requires:**
- ActivityDungeon1002_BossBattle_TipsRewardByName
**Snippet:**
```lua
require("ActivityDungeon1002_BossBattle_TipsRewardByName")

function GetActivityDungeon1002_BossBattle_TipsUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1002_BossBattle_TipsRewardUis(ui:GetChild("Reward"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.NumberWordTxt = ui:GetChild("NumberWordTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a2/ActivityDungeon1002_BossBattle_TipsRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1002_BossBattle_TipsRewardUis
**Snippet:**
```lua
function GetActivityDungeon1002_BossBattle_TipsRewardUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_BossBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_BossBtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_BossBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
```

---

## Activty/a2/ActivityDungeon1002_BuyLevelBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_BuyLevelBtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_BuyLevelBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_BuyLevelDes1ByName.lua.lua
**Functions:**
- GetActivityDungeon1002_BuyLevelDes1Uis
**Requires:**
- ActivityDungeon1002_NumberStripByName
- ActivityDungeon1002_BuyPriceNumberByName
**Snippet:**
```lua
require("ActivityDungeon1002_NumberStripByName")
require("ActivityDungeon1002_BuyPriceNumberByName")

function GetActivityDungeon1002_BuyLevelDes1Uis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.NumberStrip = GetActivityDungeon1002_NumberStripUis(ui:GetChild("NumberStrip"))
  uis.BuyPriceNumber = GetActivityDungeon1002_BuyPriceNumberUis(ui:GetChild("BuyPriceNumber"))
```

---

## Activty/a2/ActivityDungeon1002_BuyLevelDes2ByName.lua.lua
**Functions:**
- GetActivityDungeon1002_BuyLevelDes2Uis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1002_BuyLevelDes1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1002_BuyLevelDes1ByName")

function GetActivityDungeon1002_BuyLevelDes2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.BuyLevelDes1 = GetActivityDungeon1002_BuyLevelDes1Uis(ui:GetChild("BuyLevelDes1"))
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.root = ui
```

---

## Activty/a2/ActivityDungeon1002_BuyLevelDesWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1002_BuyLevelDesWindowUis
**Requires:**
- ActivityDungeon1002_BuyLevelDes2ByName
**Snippet:**
```lua
require("ActivityDungeon1002_BuyLevelDes2ByName")

function GetActivityDungeon1002_BuyLevelDesWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1002_BuyLevelDes2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_BuyLevelItemByName.lua.lua
**Functions:**
- GetActivityDungeon1002_BuyLevelItemUis
**Requires:**
- ActivityDungeon1002_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1002_PassReward_AllFrame_EByName")

function GetActivityDungeon1002_BuyLevelItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1002_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_BuyPriceNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1002_BuyPriceNumberUis
**Snippet:**
```lua
function GetActivityDungeon1002_BuyPriceNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_ChallengeByName.lua.lua
**Functions:**
- GetActivityDungeon1002_ChallengeUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1002_MapListByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1002_MapListByName")

function GetActivityDungeon1002_ChallengeUis(ui)
  local uis = {}
  uis.BgList = ui:GetChild("BgList")
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Map = GetActivityDungeon1002_MapListUis(ui:GetChild("Map"))
  uis.ShopBtn = ui:GetChild("ShopBtn")
  uis.ChapterList = ui:GetChild("ChapterList")
```

---

## Activty/a2/ActivityDungeon1002_ChallengeChapterBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_ChallengeChapterBtnUis
**Requires:**
- ActivityDungeon1002_NormalPointLockByName
**Snippet:**
```lua
require("ActivityDungeon1002_NormalPointLockByName")

function GetActivityDungeon1002_ChallengeChapterBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Lock = GetActivityDungeon1002_NormalPointLockUis(ui:GetChild("Lock"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Activty/a2/ActivityDungeon1002_ChallengeShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_ChallengeShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_ChallengeShopBtnUis(ui)
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

## Activty/a2/ActivityDungeon1002_ChallengeWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1002_ChallengeWindowUis
**Requires:**
- ActivityDungeon1002_ChallengeByName
**Snippet:**
```lua
require("ActivityDungeon1002_ChallengeByName")

function GetActivityDungeon1002_ChallengeWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1002_ChallengeUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MainTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MainTitleUis
**Snippet:**
```lua
function GetActivityDungeon1002_MainTitleUis(ui)
  local uis = {}
  
  uis.Time1Txt = ui:GetChild("Time1Txt")
  uis.Time2Txt = ui:GetChild("Time2Txt")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MapBottom_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MapBottom_1Uis
**Snippet:**
```lua
function GetActivityDungeon1002_MapBottom_1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MapBottom_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MapBottom_2Uis
**Snippet:**
```lua
function GetActivityDungeon1002_MapBottom_2Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MapBottom_3ByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MapBottom_3Uis
**Snippet:**
```lua
function GetActivityDungeon1002_MapBottom_3Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MapListByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MapListUis
**Snippet:**
```lua
function GetActivityDungeon1002_MapListUis(ui)
  local uis = {}
  
  uis.MapList = ui:GetChild("MapList")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Map_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Map_1Uis
**Snippet:**
```lua
function GetActivityDungeon1002_Map_1Uis(ui)
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

## Activty/a2/ActivityDungeon1002_Map_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Map_2Uis
**Snippet:**
```lua
function GetActivityDungeon1002_Map_2Uis(ui)
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

## Activty/a2/ActivityDungeon1002_Map_3ByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Map_3Uis
**Snippet:**
```lua
function GetActivityDungeon1002_Map_3Uis(ui)
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

## Activty/a2/ActivityDungeon1002_MaterialBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MaterialBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1002_MaterialBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
```

---

## Activty/a2/ActivityDungeon1002_MaterialByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MaterialUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1002_Material_BattleNumberByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1002_Material_BattleNumberByName")

function GetActivityDungeon1002_MaterialUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.BattleNumber = GetActivityDungeon1002_Material_BattleNumberUis(ui:GetChild("BattleNumber"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a2/ActivityDungeon1002_MaterialWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MaterialWindowUis
**Requires:**
- ActivityDungeon1002_MaterialByName
**Snippet:**
```lua
require("ActivityDungeon1002_MaterialByName")

function GetActivityDungeon1002_MaterialWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1002_MaterialUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Material_BattleAniByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Material_BattleAniUis
**Requires:**
- ActivityDungeon1002_Material_BattleByName
**Snippet:**
```lua
require("ActivityDungeon1002_Material_BattleByName")

function GetActivityDungeon1002_Material_BattleAniUis(ui)
  local uis = {}
  uis.Battle = GetActivityDungeon1002_Material_BattleUis(ui:GetChild("Battle"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Material_BattleByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Material_BattleUis
**Snippet:**
```lua
function GetActivityDungeon1002_Material_BattleUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Material_BattleNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Material_BattleNumberUis
**Snippet:**
```lua
function GetActivityDungeon1002_Material_BattleNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MaxBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MaxBtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_MaxBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MinBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MinBtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_MinBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MiniGameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniGameBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1002_MiniGameBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MiniGameByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniGameUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1002_MiniMain_TopByName
- ActivityDungeon1002_MiniMain_BottonByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1002_MiniMain_TopByName")
require("ActivityDungeon1002_MiniMain_BottonByName")

function GetActivityDungeon1002_MiniGameUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Top = GetActivityDungeon1002_MiniMain_TopUis(ui:GetChild("Top"))
  uis.Botton = GetActivityDungeon1002_MiniMain_BottonUis(ui:GetChild("Botton"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a2/ActivityDungeon1002_MiniGameStartByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniGameStartUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1002_MiniStart_MidRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1002_MiniStart_MidRegionByName")

function GetActivityDungeon1002_MiniGameStartUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.MidRegion = GetActivityDungeon1002_MiniStart_MidRegionUis(ui:GetChild("MidRegion"))
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.root = ui
  return uis
```

---

## Activty/a2/ActivityDungeon1002_MiniGameStartWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniGameStartWindowUis
**Requires:**
- ActivityDungeon1002_MiniGameStartByName
**Snippet:**
```lua
require("ActivityDungeon1002_MiniGameStartByName")

function GetActivityDungeon1002_MiniGameStartWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1002_MiniGameStartUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MiniGameWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniGameWindowUis
**Requires:**
- ActivityDungeon1002_MiniGameByName
**Snippet:**
```lua
require("ActivityDungeon1002_MiniGameByName")

function GetActivityDungeon1002_MiniGameWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1002_MiniGameUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MiniIntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniIntegralUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetActivityDungeon1002_MiniIntegralUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
  return uis
```

---

## Activty/a2/ActivityDungeon1002_MiniIntegralWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniIntegralWindowUis
**Requires:**
- ActivityDungeon1002_MiniIntegralByName
**Snippet:**
```lua
require("ActivityDungeon1002_MiniIntegralByName")

function GetActivityDungeon1002_MiniIntegralWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1002_MiniIntegralUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MiniIntegral_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniIntegral_TipsAniUis
**Requires:**
- ActivityDungeon1002_MiniIntegral_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1002_MiniIntegral_TipsByName")

function GetActivityDungeon1002_MiniIntegral_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1002_MiniIntegral_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MiniIntegral_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniIntegral_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1002_MiniIntegral_TipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MiniMain_BottonByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniMain_BottonUis
**Requires:**
- ActivityDungeon1002_MiniMain_TodayTaskByName
**Snippet:**
```lua
require("ActivityDungeon1002_MiniMain_TodayTaskByName")

function GetActivityDungeon1002_MiniMain_BottonUis(ui)
  local uis = {}
  uis.TaskBtn = ui:GetChild("TaskBtn")
  uis.RecordBtn = ui:GetChild("RecordBtn")
  uis.TodayTask = GetActivityDungeon1002_MiniMain_TodayTaskUis(ui:GetChild("TodayTask"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MiniMain_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniMain_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1002_MiniMain_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MiniMain_RecordBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniMain_RecordBtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_MiniMain_RecordBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MiniMain_StartBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniMain_StartBtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_MiniMain_StartBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MiniMain_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniMain_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1002_MiniMain_TaskBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MiniMain_TodayTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniMain_TodayTaskUis
**Requires:**
- ActivityDungeon1002_PassReward_AllFrame_EByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("ActivityDungeon1002_PassReward_AllFrame_EByName")
require("CommonResource_RedDotByName")

function GetActivityDungeon1002_MiniMain_TodayTaskUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1002_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a2/ActivityDungeon1002_MiniMain_TopByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniMain_TopUis
**Requires:**
- ActivityDungeon1002_MiniMain_IntegralByName
**Snippet:**
```lua
require("ActivityDungeon1002_MiniMain_IntegralByName")

function GetActivityDungeon1002_MiniMain_TopUis(ui)
  local uis = {}
  uis.Integral = GetActivityDungeon1002_MiniMain_IntegralUis(ui:GetChild("Integral"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MiniStart_CloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniStart_CloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_MiniStart_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MiniStart_EndAgainBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniStart_EndAgainBtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_MiniStart_EndAgainBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MiniStart_EndCloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniStart_EndCloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_MiniStart_EndCloseBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MiniStart_EndRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniStart_EndRewardUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetActivityDungeon1002_MiniStart_EndRewardUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.AgainBtn = ui:GetChild("AgainBtn")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.EffectHolder = ui:GetChild("EffectHolder")
```

---

## Activty/a2/ActivityDungeon1002_MiniStart_EndRewardWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniStart_EndRewardWindowUis
**Requires:**
- ActivityDungeon1002_MiniStart_EndRewardByName
**Snippet:**
```lua
require("ActivityDungeon1002_MiniStart_EndRewardByName")

function GetActivityDungeon1002_MiniStart_EndRewardWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1002_MiniStart_EndRewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MiniStart_MidLatticeAniByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniStart_MidLatticeAniUis
**Requires:**
- ActivityDungeon1002_MiniStart_MidLatticeByName
**Snippet:**
```lua
require("ActivityDungeon1002_MiniStart_MidLatticeByName")

function GetActivityDungeon1002_MiniStart_MidLatticeAniUis(ui)
  local uis = {}
  uis.Lattice = GetActivityDungeon1002_MiniStart_MidLatticeUis(ui:GetChild("Lattice"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MiniStart_MidLatticeByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniStart_MidLatticeUis
**Requires:**
- ActivityDungeon1002_MiniStart_MidLatticeLineRegionByName
**Snippet:**
```lua
require("ActivityDungeon1002_MiniStart_MidLatticeLineRegionByName")

function GetActivityDungeon1002_MiniStart_MidLatticeUis(ui)
  local uis = {}
  uis.Line = GetActivityDungeon1002_MiniStart_MidLatticeLineRegionUis(ui:GetChild("Line"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a2/ActivityDungeon1002_MiniStart_MidLatticeLineByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniStart_MidLatticeLineUis
**Snippet:**
```lua
function GetActivityDungeon1002_MiniStart_MidLatticeLineUis(ui)
  local uis = {}
  
  uis.AddImage = ui:GetChild("AddImage")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MiniStart_MidLatticeLineRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniStart_MidLatticeLineRegionUis
**Requires:**
- ActivityDungeon1002_MiniStart_MidLatticeLineByName
**Snippet:**
```lua
require("ActivityDungeon1002_MiniStart_MidLatticeLineByName")

function GetActivityDungeon1002_MiniStart_MidLatticeLineRegionUis(ui)
  local uis = {}
  uis.Line1 = GetActivityDungeon1002_MiniStart_MidLatticeLineUis(ui:GetChild("Line1"))
  uis.Line2 = GetActivityDungeon1002_MiniStart_MidLatticeLineUis(ui:GetChild("Line2"))
  uis.Line3 = GetActivityDungeon1002_MiniStart_MidLatticeLineUis(ui:GetChild("Line3"))
  uis.Line4 = GetActivityDungeon1002_MiniStart_MidLatticeLineUis(ui:GetChild("Line4"))
  uis.Line5 = GetActivityDungeon1002_MiniStart_MidLatticeLineUis(ui:GetChild("Line5"))
  uis.Line6 = GetActivityDungeon1002_MiniStart_MidLatticeLineUis(ui:GetChild("Line6"))
```

---

## Activty/a2/ActivityDungeon1002_MiniStart_MidRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniStart_MidRegionUis
**Requires:**
- ActivityDungeon1002_MiniStart_MidLatticeAniByName
**Snippet:**
```lua
require("ActivityDungeon1002_MiniStart_MidLatticeAniByName")

function GetActivityDungeon1002_MiniStart_MidRegionUis(ui)
  local uis = {}
  uis.Lattice1 = GetActivityDungeon1002_MiniStart_MidLatticeAniUis(ui:GetChild("Lattice1"))
  uis.Lattice2 = GetActivityDungeon1002_MiniStart_MidLatticeAniUis(ui:GetChild("Lattice2"))
  uis.Lattice3 = GetActivityDungeon1002_MiniStart_MidLatticeAniUis(ui:GetChild("Lattice3"))
  uis.Lattice4 = GetActivityDungeon1002_MiniStart_MidLatticeAniUis(ui:GetChild("Lattice4"))
  uis.Lattice5 = GetActivityDungeon1002_MiniStart_MidLatticeAniUis(ui:GetChild("Lattice5"))
  uis.Lattice6 = GetActivityDungeon1002_MiniStart_MidLatticeAniUis(ui:GetChild("Lattice6"))
```

---

## Activty/a2/ActivityDungeon1002_MiniTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniTaskUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1002_MiniTask_IntegralByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1002_MiniTask_IntegralByName")

function GetActivityDungeon1002_MiniTaskUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Integral = GetActivityDungeon1002_MiniTask_IntegralUis(ui:GetChild("Integral"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a2/ActivityDungeon1002_MiniTaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniTaskWindowUis
**Requires:**
- ActivityDungeon1002_MiniTaskByName
**Snippet:**
```lua
require("ActivityDungeon1002_MiniTaskByName")

function GetActivityDungeon1002_MiniTaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1002_MiniTaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MiniTask_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniTask_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1002_MiniTask_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MiniTask_RewardItemByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniTask_RewardItemUis
**Snippet:**
```lua
function GetActivityDungeon1002_MiniTask_RewardItemUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MiniTask_RewardItemGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniTask_RewardItemGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_MiniTask_RewardItemGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MiniTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniTask_TipsAniUis
**Requires:**
- ActivityDungeon1002_MiniTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1002_MiniTask_TipsByName")

function GetActivityDungeon1002_MiniTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1002_MiniTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_MiniTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1002_MiniTask_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1002_MiniTask_TipsUis(ui)
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

## Activty/a2/ActivityDungeon1002_NormalBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_NormalBtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_NormalBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_NormalPoint1BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_NormalPoint1BtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_NormalPoint1BtnUis(ui)
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

## Activty/a2/ActivityDungeon1002_NormalPoint2BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_NormalPoint2BtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_NormalPoint2BtnUis(ui)
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

## Activty/a2/ActivityDungeon1002_NormalPointBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_NormalPointBtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_NormalPointBtnUis(ui)
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

## Activty/a2/ActivityDungeon1002_NormalPointLockByName.lua.lua
**Functions:**
- GetActivityDungeon1002_NormalPointLockUis
**Snippet:**
```lua
function GetActivityDungeon1002_NormalPointLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_NumberStripByName.lua.lua
**Functions:**
- GetActivityDungeon1002_NumberStripUis
**Snippet:**
```lua
function GetActivityDungeon1002_NumberStripUis(ui)
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

## Activty/a2/ActivityDungeon1002_PassBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1002_PassBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_PassClothes_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassClothes_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_PassClothes_BuyBtnUis(ui)
  local uis = {}
  
  uis.PriceTxt = ui:GetChild("PriceTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_PassClothes_BuyRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassClothes_BuyRewardUis
**Snippet:**
```lua
function GetActivityDungeon1002_PassClothes_BuyRewardUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_PassClothes_CardQBByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassClothes_CardQBUis
**Snippet:**
```lua
function GetActivityDungeon1002_PassClothes_CardQBUis(ui)
  local uis = {}
  
  uis.QBHolder = ui:GetChild("QBHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_PassClothes_ClothseRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassClothes_ClothseRegionUis
**Requires:**
- ActivityDungeon1002_PassClothes_WordByName
- ActivityDungeon1002_PassClothes_CardQBByName
- ActivityDungeon1002_PassClothes_BuyRewardByName
**Snippet:**
```lua
require("ActivityDungeon1002_PassClothes_WordByName")
require("ActivityDungeon1002_PassClothes_CardQBByName")
require("ActivityDungeon1002_PassClothes_BuyRewardByName")

function GetActivityDungeon1002_PassClothes_ClothseRegionUis(ui)
  local uis = {}
  uis.Word = GetActivityDungeon1002_PassClothes_WordUis(ui:GetChild("Word"))
  uis.CardQB = GetActivityDungeon1002_PassClothes_CardQBUis(ui:GetChild("CardQB"))
  uis.BuyReward = GetActivityDungeon1002_PassClothes_BuyRewardUis(ui:GetChild("BuyReward"))
  uis.BuyBtn = ui:GetChild("BuyBtn")
```

---

## Activty/a2/ActivityDungeon1002_PassClothes_NameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassClothes_NameBtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_PassClothes_NameBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_PassClothes_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassClothes_WordUis
**Snippet:**
```lua
function GetActivityDungeon1002_PassClothes_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_PassportByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassportUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1002_PassReward_RewardRegionByName
- ActivityDungeon1002_PassTask_TaskRegionByName
- ActivityDungeon1002_PassClothes_ClothseRegionByName
- ActivityDungeon1002_Passport_LevelByName
- ActivityDungeon1002_Sign_TimeByName
- ActivityDungeon1002_Passport_TabRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1002_PassReward_RewardRegionByName")
require("ActivityDungeon1002_PassTask_TaskRegionByName")
require("ActivityDungeon1002_PassClothes_ClothseRegionByName")
require("ActivityDungeon1002_Passport_LevelByName")
require("ActivityDungeon1002_Sign_TimeByName")
require("ActivityDungeon1002_Passport_TabRegionByName")

function GetActivityDungeon1002_PassportUis(ui)
  local uis = {}
```

---

## Activty/a2/ActivityDungeon1002_PassportUp_LevelUpBgByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassportUp_LevelUpBgUis
**Snippet:**
```lua
function GetActivityDungeon1002_PassportUp_LevelUpBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_PassportUp_LevelUpTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassportUp_LevelUpTipsUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1002_PassportUp_LevelUpBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1002_PassportUp_LevelUpBgByName")

function GetActivityDungeon1002_PassportUp_LevelUpTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.LevelUpBg = GetActivityDungeon1002_PassportUp_LevelUpBgUis(ui:GetChild("LevelUpBg"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
```

---

## Activty/a2/ActivityDungeon1002_PassportUp_LevelUpTipsWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassportUp_LevelUpTipsWindowUis
**Requires:**
- ActivityDungeon1002_PassportUp_LevelUpTipsByName
**Snippet:**
```lua
require("ActivityDungeon1002_PassportUp_LevelUpTipsByName")

function GetActivityDungeon1002_PassportUp_LevelUpTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1002_PassportUp_LevelUpTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_PassportWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassportWindowUis
**Requires:**
- ActivityDungeon1002_PassportByName
**Snippet:**
```lua
require("ActivityDungeon1002_PassportByName")

function GetActivityDungeon1002_PassportWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1002_PassportUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Passport_AllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Passport_AllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_Passport_AllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Passport_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Passport_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_Passport_BuyBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Passport_ExpProgressBarByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Passport_ExpProgressBarUis
**Requires:**
- ActivityDungeon1002_Passport_ExpProgressFillByName
**Snippet:**
```lua
require("ActivityDungeon1002_Passport_ExpProgressFillByName")

function GetActivityDungeon1002_Passport_ExpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetActivityDungeon1002_Passport_ExpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Passport_ExpProgressFillByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Passport_ExpProgressFillUis
**Snippet:**
```lua
function GetActivityDungeon1002_Passport_ExpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Passport_LevelByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Passport_LevelUis
**Snippet:**
```lua
function GetActivityDungeon1002_Passport_LevelUis(ui)
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

## Activty/a2/ActivityDungeon1002_Passport_TabBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Passport_TabBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1002_Passport_TabBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## Activty/a2/ActivityDungeon1002_Passport_TabRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Passport_TabRegionUis
**Snippet:**
```lua
function GetActivityDungeon1002_Passport_TabRegionUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_PassReward_AllFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassReward_AllFrame_EUis
**Requires:**
- ActivityDungeon1002_PassReward_ItemFrame_EByName
- ActivityDungeon1002_PassReward_CardFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1002_PassReward_ItemFrame_EByName")
require("ActivityDungeon1002_PassReward_CardFrame_EByName")

function GetActivityDungeon1002_PassReward_AllFrame_EUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1002_PassReward_ItemFrame_EUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1002_PassReward_CardFrame_EUis(ui:GetChild("CardFrame"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## Activty/a2/ActivityDungeon1002_PassReward_AllFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassReward_AllFrame_MUis
**Requires:**
- ActivityDungeon1002_PassReward_ItemFrame_MByName
- ActivityDungeon1002_PassReward_CardFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1002_PassReward_ItemFrame_MByName")
require("ActivityDungeon1002_PassReward_CardFrame_MByName")

function GetActivityDungeon1002_PassReward_AllFrame_MUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1002_PassReward_ItemFrame_MUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1002_PassReward_CardFrame_MUis(ui:GetChild("CardFrame"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a2/ActivityDungeon1002_PassReward_CardFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassReward_CardFrame_EUis
**Requires:**
- ActivityDungeon1002_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1002_PassReward_ItemCardPicByName")

function GetActivityDungeon1002_PassReward_CardFrame_EUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1002_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a2/ActivityDungeon1002_PassReward_CardFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassReward_CardFrame_MUis
**Requires:**
- ActivityDungeon1002_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1002_PassReward_ItemCardPicByName")

function GetActivityDungeon1002_PassReward_CardFrame_MUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1002_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a2/ActivityDungeon1002_PassReward_EndTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassReward_EndTwoUis
**Requires:**
- ActivityDungeon1002_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1002_PassReward_AllFrame_EByName")

function GetActivityDungeon1002_PassReward_EndTwoUis(ui)
  local uis = {}
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.Item1 = GetActivityDungeon1002_PassReward_AllFrame_EUis(ui:GetChild("Item1"))
  uis.Item2 = GetActivityDungeon1002_PassReward_AllFrame_EUis(ui:GetChild("Item2"))
  uis.root = ui
```

---

## Activty/a2/ActivityDungeon1002_PassReward_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassReward_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1002_PassReward_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_PassReward_ItemFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassReward_ItemFrame_EUis
**Snippet:**
```lua
function GetActivityDungeon1002_PassReward_ItemFrame_EUis(ui)
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

## Activty/a2/ActivityDungeon1002_PassReward_ItemFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassReward_ItemFrame_MUis
**Snippet:**
```lua
function GetActivityDungeon1002_PassReward_ItemFrame_MUis(ui)
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

## Activty/a2/ActivityDungeon1002_PassReward_LevelTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassReward_LevelTitleUis
**Snippet:**
```lua
function GetActivityDungeon1002_PassReward_LevelTitleUis(ui)
  local uis = {}
  
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_PassReward_MiddleRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassReward_MiddleRegionUis
**Snippet:**
```lua
function GetActivityDungeon1002_PassReward_MiddleRegionUis(ui)
  local uis = {}
  
  uis.MiddleList = ui:GetChild("MiddleList")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_PassReward_MidTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassReward_MidTwoUis
**Requires:**
- ActivityDungeon1002_PassReward_MidTwoItemByName
- ActivityDungeon1002_PassReward_LevelTitleByName
**Snippet:**
```lua
require("ActivityDungeon1002_PassReward_MidTwoItemByName")
require("ActivityDungeon1002_PassReward_LevelTitleByName")

function GetActivityDungeon1002_PassReward_MidTwoUis(ui)
  local uis = {}
  uis.Reward1 = GetActivityDungeon1002_PassReward_MidTwoItemUis(ui:GetChild("Reward1"))
  uis.Reward2 = GetActivityDungeon1002_PassReward_MidTwoItemUis(ui:GetChild("Reward2"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Title = GetActivityDungeon1002_PassReward_LevelTitleUis(ui:GetChild("Title"))
```

---

## Activty/a2/ActivityDungeon1002_PassReward_MidTwoItemByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassReward_MidTwoItemUis
**Requires:**
- ActivityDungeon1002_PassReward_AllFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1002_PassReward_AllFrame_MByName")

function GetActivityDungeon1002_PassReward_MidTwoItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1002_PassReward_AllFrame_MUis(ui:GetChild("Item"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_PassReward_PicByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassReward_PicUis
**Snippet:**
```lua
function GetActivityDungeon1002_PassReward_PicUis(ui)
  local uis = {}
  
  uis.BuyTxt = ui:GetChild("BuyTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_PassReward_RewardRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassReward_RewardRegionUis
**Requires:**
- ActivityDungeon1002_PassReward_MiddleRegionByName
- ActivityDungeon1002_PassReward_StartTwoByName
- ActivityDungeon1002_PassReward_EndTwoByName
**Snippet:**
```lua
require("ActivityDungeon1002_PassReward_MiddleRegionByName")
require("ActivityDungeon1002_PassReward_StartTwoByName")
require("ActivityDungeon1002_PassReward_EndTwoByName")

function GetActivityDungeon1002_PassReward_RewardRegionUis(ui)
  local uis = {}
  uis.MiddleList = GetActivityDungeon1002_PassReward_MiddleRegionUis(ui:GetChild("MiddleList"))
  uis.StartTwo = GetActivityDungeon1002_PassReward_StartTwoUis(ui:GetChild("StartTwo"))
  uis.EndTwo = GetActivityDungeon1002_PassReward_EndTwoUis(ui:GetChild("EndTwo"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a2/ActivityDungeon1002_PassReward_StartTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassReward_StartTwoUis
**Requires:**
- ActivityDungeon1002_PassReward_PicByName
**Snippet:**
```lua
require("ActivityDungeon1002_PassReward_PicByName")

function GetActivityDungeon1002_PassReward_StartTwoUis(ui)
  local uis = {}
  uis.Pic = GetActivityDungeon1002_PassReward_PicUis(ui:GetChild("Pic"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_PassTask_TaskRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassTask_TaskRegionUis
**Requires:**
- ActivityDungeon1002_TaskMaxByName
**Snippet:**
```lua
require("ActivityDungeon1002_TaskMaxByName")

function GetActivityDungeon1002_PassTask_TaskRegionUis(ui)
  local uis = {}
  uis.TipsList = ui:GetChild("TipsList")
  uis.Max = GetActivityDungeon1002_TaskMaxUis(ui:GetChild("Max"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_PassTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassTask_TipsAniUis
**Requires:**
- ActivityDungeon1002_PassTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1002_PassTask_TipsByName")

function GetActivityDungeon1002_PassTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1002_PassTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_PassTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassTask_TipsUis
**Requires:**
- ActivityDungeon1002_PassTask_TipsIntegralByName
**Snippet:**
```lua
require("ActivityDungeon1002_PassTask_TipsIntegralByName")

function GetActivityDungeon1002_PassTask_TipsUis(ui)
  local uis = {}
  uis.ProgressTxt = ui:GetChild("ProgressTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Integral = GetActivityDungeon1002_PassTask_TipsIntegralUis(ui:GetChild("Integral"))
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a2/ActivityDungeon1002_PassTask_TipsIntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PassTask_TipsIntegralUis
**Snippet:**
```lua
function GetActivityDungeon1002_PassTask_TipsIntegralUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_PlotBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PlotBtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_PlotBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_PlotByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PlotUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1002_Plot_WordByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1002_Plot_WordByName")

function GetActivityDungeon1002_PlotUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Word = GetActivityDungeon1002_Plot_WordUis(ui:GetChild("Word"))
  uis.PlotList = ui:GetChild("PlotList")
  uis.ProspectBtn = ui:GetChild("ProspectBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a2/ActivityDungeon1002_PlotWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1002_PlotWindowUis
**Requires:**
- ActivityDungeon1002_PlotByName
**Snippet:**
```lua
require("ActivityDungeon1002_PlotByName")

function GetActivityDungeon1002_PlotWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1002_PlotUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Plot_ProspectBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Plot_ProspectBtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_Plot_ProspectBtnUis(ui)
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

## Activty/a2/ActivityDungeon1002_Plot_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Plot_TipsAniUis
**Requires:**
- ActivityDungeon1002_Plot_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1002_Plot_TipsByName")

function GetActivityDungeon1002_Plot_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1002_Plot_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Plot_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Plot_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1002_Plot_TipsUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Plot_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Plot_WordUis
**Snippet:**
```lua
function GetActivityDungeon1002_Plot_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_ReduceBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_ReduceBtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_ReduceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_ShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_ShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_ShopBtnUis(ui)
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

## Activty/a2/ActivityDungeon1002_ShopByName.lua.lua
**Functions:**
- GetActivityDungeon1002_ShopUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1002_Shop_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1002_Shop_TimeByName")

function GetActivityDungeon1002_ShopUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Time = GetActivityDungeon1002_Shop_TimeUis(ui:GetChild("Time"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a2/ActivityDungeon1002_ShopWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1002_ShopWindowUis
**Requires:**
- ActivityDungeon1002_ShopByName
**Snippet:**
```lua
require("ActivityDungeon1002_ShopByName")

function GetActivityDungeon1002_ShopWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1002_ShopUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Shop_CardHeadBgByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Shop_CardHeadBgUis
**Snippet:**
```lua
function GetActivityDungeon1002_Shop_CardHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Shop_ItemAniByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Shop_ItemAniUis
**Requires:**
- ActivityDungeon1002_Shop_ItemByName
**Snippet:**
```lua
require("ActivityDungeon1002_Shop_ItemByName")

function GetActivityDungeon1002_Shop_ItemAniUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1002_Shop_ItemUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Shop_ItemBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Shop_ItemBtnUis
**Requires:**
- ActivityDungeon1002_Shop_CardHeadBgByName
- ActivityDungeon1002_Shop_ItemNumberByName
- ActivityDungeon1002_Shop_UseMarkByName
**Snippet:**
```lua
require("ActivityDungeon1002_Shop_CardHeadBgByName")
require("ActivityDungeon1002_Shop_ItemNumberByName")
require("ActivityDungeon1002_Shop_UseMarkByName")

function GetActivityDungeon1002_Shop_ItemBtnUis(ui)
  local uis = {}
  uis.CardHeadBg = GetActivityDungeon1002_Shop_CardHeadBgUis(ui:GetChild("CardHeadBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.ItemNumber = GetActivityDungeon1002_Shop_ItemNumberUis(ui:GetChild("ItemNumber"))
```

---

## Activty/a2/ActivityDungeon1002_Shop_ItemByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Shop_ItemUis
**Requires:**
- ActivityDungeon1002_Shop_SellOutByName
**Snippet:**
```lua
require("ActivityDungeon1002_Shop_SellOutByName")

function GetActivityDungeon1002_Shop_ItemUis(ui)
  local uis = {}
  uis.ItemBtn = ui:GetChild("ItemBtn")
  uis.SellOut = GetActivityDungeon1002_Shop_SellOutUis(ui:GetChild("SellOut"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Shop_ItemNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Shop_ItemNumberUis
**Snippet:**
```lua
function GetActivityDungeon1002_Shop_ItemNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Shop_ItemRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Shop_ItemRegionUis
**Requires:**
- ActivityDungeon1002_Shop_TitleByName
**Snippet:**
```lua
require("ActivityDungeon1002_Shop_TitleByName")

function GetActivityDungeon1002_Shop_ItemRegionUis(ui)
  local uis = {}
  uis.ShopTitle = GetActivityDungeon1002_Shop_TitleUis(ui:GetChild("ShopTitle"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Shop_SellOutByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Shop_SellOutUis
**Snippet:**
```lua
function GetActivityDungeon1002_Shop_SellOutUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Shop_StarByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Shop_StarUis
**Snippet:**
```lua
function GetActivityDungeon1002_Shop_StarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Shop_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Shop_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1002_Shop_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Shop_TitleByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Shop_TitleUis
**Snippet:**
```lua
function GetActivityDungeon1002_Shop_TitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Shop_UseMarkByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Shop_UseMarkUis
**Snippet:**
```lua
function GetActivityDungeon1002_Shop_UseMarkUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_SignBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_SignBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1002_SignBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_SignByName.lua.lua
**Functions:**
- GetActivityDungeon1002_SignUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1002_Sign_RewardListByName
- ActivityDungeon1002_Sign_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1002_Sign_RewardListByName")
require("ActivityDungeon1002_Sign_TimeByName")

function GetActivityDungeon1002_SignUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.RewardList = GetActivityDungeon1002_Sign_RewardListUis(ui:GetChild("RewardList"))
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.Time = GetActivityDungeon1002_Sign_TimeUis(ui:GetChild("Time"))
```

---

## Activty/a2/ActivityDungeon1002_SignWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1002_SignWindowUis
**Requires:**
- ActivityDungeon1002_SignByName
**Snippet:**
```lua
require("ActivityDungeon1002_SignByName")

function GetActivityDungeon1002_SignWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1002_SignUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Sign_AllFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Sign_AllFrameUis
**Requires:**
- ActivityDungeon1002_Sign_ItemFrameByName
- ActivityDungeon1002_Sign_CardFrameByName
**Snippet:**
```lua
require("ActivityDungeon1002_Sign_ItemFrameByName")
require("ActivityDungeon1002_Sign_CardFrameByName")

function GetActivityDungeon1002_Sign_AllFrameUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1002_Sign_ItemFrameUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1002_Sign_CardFrameUis(ui:GetChild("CardFrame"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a2/ActivityDungeon1002_Sign_CardFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Sign_CardFrameUis
**Requires:**
- ActivityDungeon1002_Sign_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1002_Sign_ItemCardPicByName")

function GetActivityDungeon1002_Sign_CardFrameUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1002_Sign_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a2/ActivityDungeon1002_Sign_GetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Sign_GetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_Sign_GetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Sign_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Sign_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1002_Sign_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Sign_ItemFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Sign_ItemFrameUis
**Snippet:**
```lua
function GetActivityDungeon1002_Sign_ItemFrameUis(ui)
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

## Activty/a2/ActivityDungeon1002_Sign_RewardAniByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Sign_RewardAniUis
**Requires:**
- ActivityDungeon1002_Sign_RewardByName
**Snippet:**
```lua
require("ActivityDungeon1002_Sign_RewardByName")

function GetActivityDungeon1002_Sign_RewardAniUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1002_Sign_RewardUis(ui:GetChild("Reward"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Sign_RewardByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Sign_RewardUis
**Requires:**
- ActivityDungeon1002_Sign_AllFrameByName
**Snippet:**
```lua
require("ActivityDungeon1002_Sign_AllFrameByName")

function GetActivityDungeon1002_Sign_RewardUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1002_Sign_AllFrameUis(ui:GetChild("Item"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Sign_RewardListByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Sign_RewardListUis
**Snippet:**
```lua
function GetActivityDungeon1002_Sign_RewardListUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_Sign_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1002_Sign_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1002_Sign_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_TaskAllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_TaskAllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_TaskAllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1002_TaskBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_TaskByName.lua.lua
**Functions:**
- GetActivityDungeon1002_TaskUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1002_TaskTitleByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1002_TaskTitleByName")

function GetActivityDungeon1002_TaskUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TaskTitle = GetActivityDungeon1002_TaskTitleUis(ui:GetChild("TaskTitle"))
  uis.TaskTipsList = ui:GetChild("TaskTipsList")
  uis.AllGetBtn = ui:GetChild("AllGetBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a2/ActivityDungeon1002_TaskGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1002_TaskGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1002_TaskGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_TaskMaxByName.lua.lua
**Functions:**
- GetActivityDungeon1002_TaskMaxUis
**Snippet:**
```lua
function GetActivityDungeon1002_TaskMaxUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_TaskProgressByName.lua.lua
**Functions:**
- GetActivityDungeon1002_TaskProgressUis
**Snippet:**
```lua
function GetActivityDungeon1002_TaskProgressUis(ui)
  local uis = {}
  
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_TaskTipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1002_TaskTipsAniUis
**Requires:**
- ActivityDungeon1002_TaskTipsByName
**Snippet:**
```lua
require("ActivityDungeon1002_TaskTipsByName")

function GetActivityDungeon1002_TaskTipsAniUis(ui)
  local uis = {}
  uis.TaskTips = GetActivityDungeon1002_TaskTipsUis(ui:GetChild("TaskTips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_TaskTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1002_TaskTipsUis
**Requires:**
- ActivityDungeon1002_TaskProgressByName
**Snippet:**
```lua
require("ActivityDungeon1002_TaskProgressByName")

function GetActivityDungeon1002_TaskTipsUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.RewardList = ui:GetChild("RewardList")
  uis.TaskProgress = GetActivityDungeon1002_TaskProgressUis(ui:GetChild("TaskProgress"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a2/ActivityDungeon1002_TaskTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1002_TaskTitleUis
**Snippet:**
```lua
function GetActivityDungeon1002_TaskTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a2/ActivityDungeon1002_TaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1002_TaskWindowUis
**Requires:**
- ActivityDungeon1002_TaskByName
**Snippet:**
```lua
require("ActivityDungeon1002_TaskByName")

function GetActivityDungeon1002_TaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1002_TaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---
