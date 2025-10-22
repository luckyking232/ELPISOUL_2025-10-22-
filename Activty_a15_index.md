# Activty/a15

## Activty/a15/ActivityDungeon1015_ActivityDungeonByName.lua.lua
**Functions:**
- GetActivityDungeon1015_ActivityDungeonUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1015_MainTitleByName
- ActivityDungeon1015_ReviewWordByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1015_MainTitleByName")
require("ActivityDungeon1015_ReviewWordByName")
require("CommonResource_CurrencyReturnByName")

function GetActivityDungeon1015_ActivityDungeonUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.MainTitle = GetActivityDungeon1015_MainTitleUis(ui:GetChild("MainTitle"))
  uis.PlotBtn = ui:GetChild("PlotBtn")
```

---

## Activty/a15/ActivityDungeon1015_ActivityDungeonWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1015_ActivityDungeonWindowUis
**Requires:**
- ActivityDungeon1015_ActivityDungeonByName
**Snippet:**
```lua
require("ActivityDungeon1015_ActivityDungeonByName")

function GetActivityDungeon1015_ActivityDungeonWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1015_ActivityDungeonUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_AddBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_AddBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_AddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_BossBattleByName.lua.lua
**Functions:**
- GetActivityDungeon1015_BossBattleUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1015_BossBattle_InfoByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1015_BossBattle_InfoByName")

function GetActivityDungeon1015_BossBattleUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.Info = GetActivityDungeon1015_BossBattle_InfoUis(ui:GetChild("Info"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a15/ActivityDungeon1015_BossBattleWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1015_BossBattleWindowUis
**Requires:**
- ActivityDungeon1015_BossBattleByName
**Snippet:**
```lua
require("ActivityDungeon1015_BossBattleByName")

function GetActivityDungeon1015_BossBattleWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1015_BossBattleUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_BossBattle_Info1ByName.lua.lua
**Functions:**
- GetActivityDungeon1015_BossBattle_Info1Uis
**Snippet:**
```lua
function GetActivityDungeon1015_BossBattle_Info1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_BossBattle_InfoByName.lua.lua
**Functions:**
- GetActivityDungeon1015_BossBattle_InfoUis
**Requires:**
- ActivityDungeon1015_BossBattle_Info1ByName
**Snippet:**
```lua
require("ActivityDungeon1015_BossBattle_Info1ByName")

function GetActivityDungeon1015_BossBattle_InfoUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = GetActivityDungeon1015_BossBattle_Info1Uis(ui:GetChild("WordTxt"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_BossBattle_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1015_BossBattle_TipsAniUis
**Requires:**
- ActivityDungeon1015_BossBattle_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1015_BossBattle_TipsByName")

function GetActivityDungeon1015_BossBattle_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1015_BossBattle_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_BossBattle_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1015_BossBattle_TipsUis
**Requires:**
- ActivityDungeon1015_BossBattle_TipsRewardByName
**Snippet:**
```lua
require("ActivityDungeon1015_BossBattle_TipsRewardByName")

function GetActivityDungeon1015_BossBattle_TipsUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1015_BossBattle_TipsRewardUis(ui:GetChild("Reward"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.NumberWordTxt = ui:GetChild("NumberWordTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a15/ActivityDungeon1015_BossBattle_TipsRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1015_BossBattle_TipsRewardUis
**Snippet:**
```lua
function GetActivityDungeon1015_BossBattle_TipsRewardUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_BossBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_BossBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_BossBtnUis(ui)
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

## Activty/a15/ActivityDungeon1015_BuyLevelBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_BuyLevelBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_BuyLevelBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_BuyLevelDes1ByName.lua.lua
**Functions:**
- GetActivityDungeon1015_BuyLevelDes1Uis
**Requires:**
- ActivityDungeon1015_NumberStripByName
- ActivityDungeon1015_BuyPriceNumberByName
**Snippet:**
```lua
require("ActivityDungeon1015_NumberStripByName")
require("ActivityDungeon1015_BuyPriceNumberByName")

function GetActivityDungeon1015_BuyLevelDes1Uis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.NumberStrip = GetActivityDungeon1015_NumberStripUis(ui:GetChild("NumberStrip"))
  uis.BuyPriceNumber = GetActivityDungeon1015_BuyPriceNumberUis(ui:GetChild("BuyPriceNumber"))
```

---

## Activty/a15/ActivityDungeon1015_BuyLevelDes2ByName.lua.lua
**Functions:**
- GetActivityDungeon1015_BuyLevelDes2Uis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1015_BuyLevelDes1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1015_BuyLevelDes1ByName")

function GetActivityDungeon1015_BuyLevelDes2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.BuyLevelDes1 = GetActivityDungeon1015_BuyLevelDes1Uis(ui:GetChild("BuyLevelDes1"))
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.root = ui
```

---

## Activty/a15/ActivityDungeon1015_BuyLevelDesWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1015_BuyLevelDesWindowUis
**Requires:**
- ActivityDungeon1015_BuyLevelDes2ByName
**Snippet:**
```lua
require("ActivityDungeon1015_BuyLevelDes2ByName")

function GetActivityDungeon1015_BuyLevelDesWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1015_BuyLevelDes2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_BuyLevelItemByName.lua.lua
**Functions:**
- GetActivityDungeon1015_BuyLevelItemUis
**Requires:**
- ActivityDungeon1015_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1015_PassReward_AllFrame_EByName")

function GetActivityDungeon1015_BuyLevelItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1015_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_BuyPriceNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1015_BuyPriceNumberUis
**Snippet:**
```lua
function GetActivityDungeon1015_BuyPriceNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_ChallengeByName.lua.lua
**Functions:**
- GetActivityDungeon1015_ChallengeUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1015_MapListByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1015_MapListByName")

function GetActivityDungeon1015_ChallengeUis(ui)
  local uis = {}
  uis.BgList = ui:GetChild("BgList")
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Map = GetActivityDungeon1015_MapListUis(ui:GetChild("Map"))
  uis.ShopBtn = ui:GetChild("ShopBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a15/ActivityDungeon1015_ChallengeChapterBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_ChallengeChapterBtnUis
**Requires:**
- ActivityDungeon1015_NormalPointLockByName
**Snippet:**
```lua
require("ActivityDungeon1015_NormalPointLockByName")

function GetActivityDungeon1015_ChallengeChapterBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Lock = GetActivityDungeon1015_NormalPointLockUis(ui:GetChild("Lock"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Activty/a15/ActivityDungeon1015_ChallengeShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_ChallengeShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_ChallengeShopBtnUis(ui)
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

## Activty/a15/ActivityDungeon1015_ChallengeWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1015_ChallengeWindowUis
**Requires:**
- ActivityDungeon1015_ChallengeByName
**Snippet:**
```lua
require("ActivityDungeon1015_ChallengeByName")

function GetActivityDungeon1015_ChallengeWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1015_ChallengeUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MainTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MainTitleUis
**Snippet:**
```lua
function GetActivityDungeon1015_MainTitleUis(ui)
  local uis = {}
  
  uis.Time1Txt = ui:GetChild("Time1Txt")
  uis.Time2Txt = ui:GetChild("Time2Txt")
  uis.reviewCtr = ui:GetController("review")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MapBottom_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MapBottom_1Uis
**Snippet:**
```lua
function GetActivityDungeon1015_MapBottom_1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MapBottom_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MapBottom_2Uis
**Snippet:**
```lua
function GetActivityDungeon1015_MapBottom_2Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MapListByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MapListUis
**Snippet:**
```lua
function GetActivityDungeon1015_MapListUis(ui)
  local uis = {}
  
  uis.MapList = ui:GetChild("MapList")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Map_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Map_1Uis
**Snippet:**
```lua
function GetActivityDungeon1015_Map_1Uis(ui)
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

## Activty/a15/ActivityDungeon1015_Map_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Map_2Uis
**Snippet:**
```lua
function GetActivityDungeon1015_Map_2Uis(ui)
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

## Activty/a15/ActivityDungeon1015_MaterialBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MaterialBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1015_MaterialBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
```

---

## Activty/a15/ActivityDungeon1015_MaterialByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MaterialUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1015_Material_BattleNumberByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1015_Material_BattleNumberByName")

function GetActivityDungeon1015_MaterialUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.BattleNumber = GetActivityDungeon1015_Material_BattleNumberUis(ui:GetChild("BattleNumber"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a15/ActivityDungeon1015_MaterialWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MaterialWindowUis
**Requires:**
- ActivityDungeon1015_MaterialByName
**Snippet:**
```lua
require("ActivityDungeon1015_MaterialByName")

function GetActivityDungeon1015_MaterialWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1015_MaterialUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Material_BattleAniByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Material_BattleAniUis
**Requires:**
- ActivityDungeon1015_Material_BattleByName
**Snippet:**
```lua
require("ActivityDungeon1015_Material_BattleByName")

function GetActivityDungeon1015_Material_BattleAniUis(ui)
  local uis = {}
  uis.Battle = GetActivityDungeon1015_Material_BattleUis(ui:GetChild("Battle"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Material_BattleByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Material_BattleUis
**Snippet:**
```lua
function GetActivityDungeon1015_Material_BattleUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Material_BattleNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Material_BattleNumberUis
**Snippet:**
```lua
function GetActivityDungeon1015_Material_BattleNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MaxBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MaxBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_MaxBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MinBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MinBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_MinBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniGameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniGameBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1015_MiniGameBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniGameByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniGameUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1015_MiniMain_TopByName
- ActivityDungeon1015_MiniMain_BottonByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1015_MiniMain_TopByName")
require("ActivityDungeon1015_MiniMain_BottonByName")

function GetActivityDungeon1015_MiniGameUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Top = GetActivityDungeon1015_MiniMain_TopUis(ui:GetChild("Top"))
  uis.Botton = GetActivityDungeon1015_MiniMain_BottonUis(ui:GetChild("Botton"))
  uis.StartBtn = ui:GetChild("StartBtn")
```

---

## Activty/a15/ActivityDungeon1015_MiniGameStartByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniGameStartUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1015_MiniStart_OperateRegionByName
- ActivityDungeon1015_MiniStart_IntegralByName
- ActivityDungeon1015_MiniStart_DirectionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1015_MiniStart_OperateRegionByName")
require("ActivityDungeon1015_MiniStart_IntegralByName")
require("ActivityDungeon1015_MiniStart_DirectionByName")

function GetActivityDungeon1015_MiniGameStartUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.OperateRegion = GetActivityDungeon1015_MiniStart_OperateRegionUis(ui:GetChild("OperateRegion"))
  uis.Integral = GetActivityDungeon1015_MiniStart_IntegralUis(ui:GetChild("Integral"))
```

---

## Activty/a15/ActivityDungeon1015_MiniGameStartWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniGameStartWindowUis
**Requires:**
- ActivityDungeon1015_MiniGameStartByName
**Snippet:**
```lua
require("ActivityDungeon1015_MiniGameStartByName")

function GetActivityDungeon1015_MiniGameStartWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1015_MiniGameStartUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniGameWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniGameWindowUis
**Requires:**
- ActivityDungeon1015_MiniGameByName
**Snippet:**
```lua
require("ActivityDungeon1015_MiniGameByName")

function GetActivityDungeon1015_MiniGameWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1015_MiniGameUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniMain_BottonByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniMain_BottonUis
**Requires:**
- ActivityDungeon1015_MiniMain_TodayTaskByName
**Snippet:**
```lua
require("ActivityDungeon1015_MiniMain_TodayTaskByName")

function GetActivityDungeon1015_MiniMain_BottonUis(ui)
  local uis = {}
  uis.TaskBtn = ui:GetChild("TaskBtn")
  uis.TodayTask = GetActivityDungeon1015_MiniMain_TodayTaskUis(ui:GetChild("TodayTask"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniMain_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniMain_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1015_MiniMain_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniMain_OperateBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniMain_OperateBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_MiniMain_OperateBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniMain_RecordBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniMain_RecordBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_MiniMain_RecordBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniMain_StartBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniMain_StartBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_MiniMain_StartBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniMain_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniMain_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1015_MiniMain_TaskBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniMain_TodayTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniMain_TodayTaskUis
**Requires:**
- ActivityDungeon1015_PassReward_AllFrame_EByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("ActivityDungeon1015_PassReward_AllFrame_EByName")
require("CommonResource_RedDotByName")

function GetActivityDungeon1015_MiniMain_TodayTaskUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1015_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a15/ActivityDungeon1015_MiniMain_TopByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniMain_TopUis
**Requires:**
- ActivityDungeon1015_MiniMain_IntegralByName
**Snippet:**
```lua
require("ActivityDungeon1015_MiniMain_IntegralByName")

function GetActivityDungeon1015_MiniMain_TopUis(ui)
  local uis = {}
  uis.Integral = GetActivityDungeon1015_MiniMain_IntegralUis(ui:GetChild("Integral"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniSetByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniSetUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1015_MiniSet_TipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1015_MiniSet_TipsByName")

function GetActivityDungeon1015_MiniSetUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Tips = GetActivityDungeon1015_MiniSet_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
```

---

## Activty/a15/ActivityDungeon1015_MiniSetWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniSetWindowUis
**Requires:**
- ActivityDungeon1015_MiniSetByName
**Snippet:**
```lua
require("ActivityDungeon1015_MiniSetByName")

function GetActivityDungeon1015_MiniSetWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1015_MiniSetUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniSet_ChoiceBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniSet_ChoiceBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_MiniSet_ChoiceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniSet_CloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniSet_CloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_MiniSet_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniSet_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniSet_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1015_MiniSet_TipsUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.ChoiceBtn = ui:GetChild("ChoiceBtn")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniStart_CloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniStart_CloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_MiniStart_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniStart_DirectionByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniStart_DirectionUis
**Snippet:**
```lua
function GetActivityDungeon1015_MiniStart_DirectionUis(ui)
  local uis = {}
  
  uis.LeftBtn = ui:GetChild("LeftBtn")
  uis.RightBtn = ui:GetChild("RightBtn")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniStart_EndAgainBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniStart_EndAgainBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_MiniStart_EndAgainBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniStart_EndCloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniStart_EndCloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_MiniStart_EndCloseBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniStart_EndRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniStart_EndRewardUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetActivityDungeon1015_MiniStart_EndRewardUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.AgainBtn = ui:GetChild("AgainBtn")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.EffectHolder = ui:GetChild("EffectHolder")
```

---

## Activty/a15/ActivityDungeon1015_MiniStart_EndRewardWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniStart_EndRewardWindowUis
**Requires:**
- ActivityDungeon1015_MiniStart_EndRewardByName
**Snippet:**
```lua
require("ActivityDungeon1015_MiniStart_EndRewardByName")

function GetActivityDungeon1015_MiniStart_EndRewardWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1015_MiniStart_EndRewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniStart_GuGuByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniStart_GuGuUis
**Snippet:**
```lua
function GetActivityDungeon1015_MiniStart_GuGuUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Effect3Holder = ui:GetChild("Effect3Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniStart_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniStart_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1015_MiniStart_IntegralUis(ui)
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

## Activty/a15/ActivityDungeon1015_MiniStart_ItemByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniStart_ItemUis
**Snippet:**
```lua
function GetActivityDungeon1015_MiniStart_ItemUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniStart_JumpBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniStart_JumpBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_MiniStart_JumpBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniStart_LeftBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniStart_LeftBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_MiniStart_LeftBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniStart_OperateRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniStart_OperateRegionUis
**Snippet:**
```lua
function GetActivityDungeon1015_MiniStart_OperateRegionUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniStart_RightBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniStart_RightBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_MiniStart_RightBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniTaskUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1015_MiniTask_IntegralByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1015_MiniTask_IntegralByName")

function GetActivityDungeon1015_MiniTaskUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Integral = GetActivityDungeon1015_MiniTask_IntegralUis(ui:GetChild("Integral"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a15/ActivityDungeon1015_MiniTaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniTaskWindowUis
**Requires:**
- ActivityDungeon1015_MiniTaskByName
**Snippet:**
```lua
require("ActivityDungeon1015_MiniTaskByName")

function GetActivityDungeon1015_MiniTaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1015_MiniTaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniTask_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniTask_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1015_MiniTask_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniTask_RewardItemByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniTask_RewardItemUis
**Snippet:**
```lua
function GetActivityDungeon1015_MiniTask_RewardItemUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniTask_RewardItemGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniTask_RewardItemGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_MiniTask_RewardItemGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniTask_TipsAniUis
**Requires:**
- ActivityDungeon1015_MiniTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1015_MiniTask_TipsByName")

function GetActivityDungeon1015_MiniTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1015_MiniTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniTask_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1015_MiniTask_TipsUis(ui)
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

## Activty/a15/ActivityDungeon1015_MiniTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniTipsUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1015_MiniTips_RegionByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1015_MiniTips_RegionByName")

function GetActivityDungeon1015_MiniTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Tips = GetActivityDungeon1015_MiniTips_RegionUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
```

---

## Activty/a15/ActivityDungeon1015_MiniTipsWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniTipsWindowUis
**Requires:**
- ActivityDungeon1015_MiniTipsByName
**Snippet:**
```lua
require("ActivityDungeon1015_MiniTipsByName")

function GetActivityDungeon1015_MiniTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1015_MiniTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniTips_CloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniTips_CloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_MiniTips_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_MiniTips_RegionByName.lua.lua
**Functions:**
- GetActivityDungeon1015_MiniTips_RegionUis
**Snippet:**
```lua
function GetActivityDungeon1015_MiniTips_RegionUis(ui)
  local uis = {}
  
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_NormalBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_NormalBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_NormalBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_NormalPoint1BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_NormalPoint1BtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_NormalPoint1BtnUis(ui)
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

## Activty/a15/ActivityDungeon1015_NormalPoint2BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_NormalPoint2BtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_NormalPoint2BtnUis(ui)
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

## Activty/a15/ActivityDungeon1015_NormalPointLockByName.lua.lua
**Functions:**
- GetActivityDungeon1015_NormalPointLockUis
**Snippet:**
```lua
function GetActivityDungeon1015_NormalPointLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_NumberStripByName.lua.lua
**Functions:**
- GetActivityDungeon1015_NumberStripUis
**Snippet:**
```lua
function GetActivityDungeon1015_NumberStripUis(ui)
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

## Activty/a15/ActivityDungeon1015_PassBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1015_PassBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_PassClothes_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassClothes_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_PassClothes_BuyBtnUis(ui)
  local uis = {}
  
  uis.PriceTxt = ui:GetChild("PriceTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_PassClothes_BuyRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassClothes_BuyRewardUis
**Snippet:**
```lua
function GetActivityDungeon1015_PassClothes_BuyRewardUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_PassClothes_CardQBByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassClothes_CardQBUis
**Snippet:**
```lua
function GetActivityDungeon1015_PassClothes_CardQBUis(ui)
  local uis = {}
  
  uis.QBHolder = ui:GetChild("QBHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_PassClothes_ClothseRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassClothes_ClothseRegionUis
**Requires:**
- ActivityDungeon1015_PassClothes_WordByName
- ActivityDungeon1015_PassClothes_CardQBByName
- ActivityDungeon1015_PassClothes_BuyRewardByName
**Snippet:**
```lua
require("ActivityDungeon1015_PassClothes_WordByName")
require("ActivityDungeon1015_PassClothes_CardQBByName")
require("ActivityDungeon1015_PassClothes_BuyRewardByName")

function GetActivityDungeon1015_PassClothes_ClothseRegionUis(ui)
  local uis = {}
  uis.Word = GetActivityDungeon1015_PassClothes_WordUis(ui:GetChild("Word"))
  uis.CardQB = GetActivityDungeon1015_PassClothes_CardQBUis(ui:GetChild("CardQB"))
  uis.BuyReward = GetActivityDungeon1015_PassClothes_BuyRewardUis(ui:GetChild("BuyReward"))
  uis.BuyBtn = ui:GetChild("BuyBtn")
```

---

## Activty/a15/ActivityDungeon1015_PassClothes_NameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassClothes_NameBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_PassClothes_NameBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_PassClothes_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassClothes_WordUis
**Snippet:**
```lua
function GetActivityDungeon1015_PassClothes_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_PassportByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassportUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1015_PassReward_RewardRegionByName
- ActivityDungeon1015_PassTask_TaskRegionByName
- ActivityDungeon1015_PassClothes_ClothseRegionByName
- ActivityDungeon1015_Passport_LevelByName
- ActivityDungeon1015_Sign_TimeByName
- ActivityDungeon1015_Passport_TabRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1015_PassReward_RewardRegionByName")
require("ActivityDungeon1015_PassTask_TaskRegionByName")
require("ActivityDungeon1015_PassClothes_ClothseRegionByName")
require("ActivityDungeon1015_Passport_LevelByName")
require("ActivityDungeon1015_Sign_TimeByName")
require("ActivityDungeon1015_Passport_TabRegionByName")

function GetActivityDungeon1015_PassportUis(ui)
  local uis = {}
```

---

## Activty/a15/ActivityDungeon1015_PassportUp_LevelUpBgByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassportUp_LevelUpBgUis
**Snippet:**
```lua
function GetActivityDungeon1015_PassportUp_LevelUpBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_PassportUp_LevelUpTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassportUp_LevelUpTipsUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1015_PassportUp_LevelUpBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1015_PassportUp_LevelUpBgByName")

function GetActivityDungeon1015_PassportUp_LevelUpTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.LevelUpBg = GetActivityDungeon1015_PassportUp_LevelUpBgUis(ui:GetChild("LevelUpBg"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
```

---

## Activty/a15/ActivityDungeon1015_PassportUp_LevelUpTipsWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassportUp_LevelUpTipsWindowUis
**Requires:**
- ActivityDungeon1015_PassportUp_LevelUpTipsByName
**Snippet:**
```lua
require("ActivityDungeon1015_PassportUp_LevelUpTipsByName")

function GetActivityDungeon1015_PassportUp_LevelUpTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1015_PassportUp_LevelUpTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_PassportWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassportWindowUis
**Requires:**
- ActivityDungeon1015_PassportByName
**Snippet:**
```lua
require("ActivityDungeon1015_PassportByName")

function GetActivityDungeon1015_PassportWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1015_PassportUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Passport_AllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Passport_AllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_Passport_AllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Passport_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Passport_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_Passport_BuyBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Passport_ExpProgressBarByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Passport_ExpProgressBarUis
**Requires:**
- ActivityDungeon1015_Passport_ExpProgressFillByName
**Snippet:**
```lua
require("ActivityDungeon1015_Passport_ExpProgressFillByName")

function GetActivityDungeon1015_Passport_ExpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetActivityDungeon1015_Passport_ExpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Passport_ExpProgressFillByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Passport_ExpProgressFillUis
**Snippet:**
```lua
function GetActivityDungeon1015_Passport_ExpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Passport_LevelByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Passport_LevelUis
**Snippet:**
```lua
function GetActivityDungeon1015_Passport_LevelUis(ui)
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

## Activty/a15/ActivityDungeon1015_Passport_TabBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Passport_TabBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1015_Passport_TabBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## Activty/a15/ActivityDungeon1015_Passport_TabRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Passport_TabRegionUis
**Snippet:**
```lua
function GetActivityDungeon1015_Passport_TabRegionUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_PassReward_AllFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassReward_AllFrame_EUis
**Requires:**
- ActivityDungeon1015_PassReward_ItemFrame_EByName
- ActivityDungeon1015_PassReward_CardFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1015_PassReward_ItemFrame_EByName")
require("ActivityDungeon1015_PassReward_CardFrame_EByName")

function GetActivityDungeon1015_PassReward_AllFrame_EUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1015_PassReward_ItemFrame_EUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1015_PassReward_CardFrame_EUis(ui:GetChild("CardFrame"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## Activty/a15/ActivityDungeon1015_PassReward_AllFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassReward_AllFrame_MUis
**Requires:**
- ActivityDungeon1015_PassReward_ItemFrame_MByName
- ActivityDungeon1015_PassReward_CardFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1015_PassReward_ItemFrame_MByName")
require("ActivityDungeon1015_PassReward_CardFrame_MByName")

function GetActivityDungeon1015_PassReward_AllFrame_MUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1015_PassReward_ItemFrame_MUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1015_PassReward_CardFrame_MUis(ui:GetChild("CardFrame"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a15/ActivityDungeon1015_PassReward_CardFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassReward_CardFrame_EUis
**Requires:**
- ActivityDungeon1015_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1015_PassReward_ItemCardPicByName")

function GetActivityDungeon1015_PassReward_CardFrame_EUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1015_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a15/ActivityDungeon1015_PassReward_CardFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassReward_CardFrame_MUis
**Requires:**
- ActivityDungeon1015_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1015_PassReward_ItemCardPicByName")

function GetActivityDungeon1015_PassReward_CardFrame_MUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1015_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a15/ActivityDungeon1015_PassReward_EndTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassReward_EndTwoUis
**Requires:**
- ActivityDungeon1015_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1015_PassReward_AllFrame_EByName")

function GetActivityDungeon1015_PassReward_EndTwoUis(ui)
  local uis = {}
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.Item1 = GetActivityDungeon1015_PassReward_AllFrame_EUis(ui:GetChild("Item1"))
  uis.Item2 = GetActivityDungeon1015_PassReward_AllFrame_EUis(ui:GetChild("Item2"))
  uis.root = ui
```

---

## Activty/a15/ActivityDungeon1015_PassReward_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassReward_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1015_PassReward_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_PassReward_ItemFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassReward_ItemFrame_EUis
**Snippet:**
```lua
function GetActivityDungeon1015_PassReward_ItemFrame_EUis(ui)
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

## Activty/a15/ActivityDungeon1015_PassReward_ItemFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassReward_ItemFrame_MUis
**Snippet:**
```lua
function GetActivityDungeon1015_PassReward_ItemFrame_MUis(ui)
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

## Activty/a15/ActivityDungeon1015_PassReward_LevelTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassReward_LevelTitleUis
**Snippet:**
```lua
function GetActivityDungeon1015_PassReward_LevelTitleUis(ui)
  local uis = {}
  
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_PassReward_MiddleRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassReward_MiddleRegionUis
**Snippet:**
```lua
function GetActivityDungeon1015_PassReward_MiddleRegionUis(ui)
  local uis = {}
  
  uis.MiddleList = ui:GetChild("MiddleList")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_PassReward_MidTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassReward_MidTwoUis
**Requires:**
- ActivityDungeon1015_PassReward_MidTwoItemByName
- ActivityDungeon1015_PassReward_LevelTitleByName
**Snippet:**
```lua
require("ActivityDungeon1015_PassReward_MidTwoItemByName")
require("ActivityDungeon1015_PassReward_LevelTitleByName")

function GetActivityDungeon1015_PassReward_MidTwoUis(ui)
  local uis = {}
  uis.Reward1 = GetActivityDungeon1015_PassReward_MidTwoItemUis(ui:GetChild("Reward1"))
  uis.Reward2 = GetActivityDungeon1015_PassReward_MidTwoItemUis(ui:GetChild("Reward2"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Title = GetActivityDungeon1015_PassReward_LevelTitleUis(ui:GetChild("Title"))
```

---

## Activty/a15/ActivityDungeon1015_PassReward_MidTwoItemByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassReward_MidTwoItemUis
**Requires:**
- ActivityDungeon1015_PassReward_AllFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1015_PassReward_AllFrame_MByName")

function GetActivityDungeon1015_PassReward_MidTwoItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1015_PassReward_AllFrame_MUis(ui:GetChild("Item"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_PassReward_PicByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassReward_PicUis
**Snippet:**
```lua
function GetActivityDungeon1015_PassReward_PicUis(ui)
  local uis = {}
  
  uis.BuyTxt = ui:GetChild("BuyTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_PassReward_RewardRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassReward_RewardRegionUis
**Requires:**
- ActivityDungeon1015_PassReward_MiddleRegionByName
- ActivityDungeon1015_PassReward_StartTwoByName
- ActivityDungeon1015_PassReward_EndTwoByName
**Snippet:**
```lua
require("ActivityDungeon1015_PassReward_MiddleRegionByName")
require("ActivityDungeon1015_PassReward_StartTwoByName")
require("ActivityDungeon1015_PassReward_EndTwoByName")

function GetActivityDungeon1015_PassReward_RewardRegionUis(ui)
  local uis = {}
  uis.MiddleList = GetActivityDungeon1015_PassReward_MiddleRegionUis(ui:GetChild("MiddleList"))
  uis.StartTwo = GetActivityDungeon1015_PassReward_StartTwoUis(ui:GetChild("StartTwo"))
  uis.EndTwo = GetActivityDungeon1015_PassReward_EndTwoUis(ui:GetChild("EndTwo"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a15/ActivityDungeon1015_PassReward_StartTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassReward_StartTwoUis
**Requires:**
- ActivityDungeon1015_PassReward_PicByName
**Snippet:**
```lua
require("ActivityDungeon1015_PassReward_PicByName")

function GetActivityDungeon1015_PassReward_StartTwoUis(ui)
  local uis = {}
  uis.Pic = GetActivityDungeon1015_PassReward_PicUis(ui:GetChild("Pic"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_PassTask_TaskRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassTask_TaskRegionUis
**Requires:**
- ActivityDungeon1015_TaskMaxByName
**Snippet:**
```lua
require("ActivityDungeon1015_TaskMaxByName")

function GetActivityDungeon1015_PassTask_TaskRegionUis(ui)
  local uis = {}
  uis.TipsList = ui:GetChild("TipsList")
  uis.Max = GetActivityDungeon1015_TaskMaxUis(ui:GetChild("Max"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_PassTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassTask_TipsAniUis
**Requires:**
- ActivityDungeon1015_PassTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1015_PassTask_TipsByName")

function GetActivityDungeon1015_PassTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1015_PassTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_PassTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassTask_TipsUis
**Requires:**
- ActivityDungeon1015_PassTask_TipsIntegralByName
**Snippet:**
```lua
require("ActivityDungeon1015_PassTask_TipsIntegralByName")

function GetActivityDungeon1015_PassTask_TipsUis(ui)
  local uis = {}
  uis.ProgressTxt = ui:GetChild("ProgressTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Integral = GetActivityDungeon1015_PassTask_TipsIntegralUis(ui:GetChild("Integral"))
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a15/ActivityDungeon1015_PassTask_TipsIntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PassTask_TipsIntegralUis
**Snippet:**
```lua
function GetActivityDungeon1015_PassTask_TipsIntegralUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_PlotBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PlotBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_PlotBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_PlotByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PlotUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1015_Plot_WordByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1015_Plot_WordByName")

function GetActivityDungeon1015_PlotUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Word = GetActivityDungeon1015_Plot_WordUis(ui:GetChild("Word"))
  uis.PlotList = ui:GetChild("PlotList")
  uis.ProspectBtn = ui:GetChild("ProspectBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a15/ActivityDungeon1015_PlotWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1015_PlotWindowUis
**Requires:**
- ActivityDungeon1015_PlotByName
**Snippet:**
```lua
require("ActivityDungeon1015_PlotByName")

function GetActivityDungeon1015_PlotWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1015_PlotUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Plot_ProspectBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Plot_ProspectBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_Plot_ProspectBtnUis(ui)
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

## Activty/a15/ActivityDungeon1015_Plot_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Plot_TipsAniUis
**Requires:**
- ActivityDungeon1015_Plot_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1015_Plot_TipsByName")

function GetActivityDungeon1015_Plot_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1015_Plot_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Plot_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Plot_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1015_Plot_TipsUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Plot_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Plot_WordUis
**Snippet:**
```lua
function GetActivityDungeon1015_Plot_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_ReduceBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_ReduceBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_ReduceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_ReviewWordByName.lua.lua
**Functions:**
- GetActivityDungeon1015_ReviewWordUis
**Snippet:**
```lua
function GetActivityDungeon1015_ReviewWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_ShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_ShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_ShopBtnUis(ui)
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

## Activty/a15/ActivityDungeon1015_ShopByName.lua.lua
**Functions:**
- GetActivityDungeon1015_ShopUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1015_Shop_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1015_Shop_TimeByName")

function GetActivityDungeon1015_ShopUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Time = GetActivityDungeon1015_Shop_TimeUis(ui:GetChild("Time"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a15/ActivityDungeon1015_ShopWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1015_ShopWindowUis
**Requires:**
- ActivityDungeon1015_ShopByName
**Snippet:**
```lua
require("ActivityDungeon1015_ShopByName")

function GetActivityDungeon1015_ShopWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1015_ShopUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Shop_CardHeadBgByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Shop_CardHeadBgUis
**Snippet:**
```lua
function GetActivityDungeon1015_Shop_CardHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Shop_ItemAniByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Shop_ItemAniUis
**Requires:**
- ActivityDungeon1015_Shop_ItemByName
**Snippet:**
```lua
require("ActivityDungeon1015_Shop_ItemByName")

function GetActivityDungeon1015_Shop_ItemAniUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1015_Shop_ItemUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Shop_ItemBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Shop_ItemBtnUis
**Requires:**
- ActivityDungeon1015_Shop_CardHeadBgByName
- ActivityDungeon1015_Shop_ItemNumberByName
- ActivityDungeon1015_Shop_UseMarkByName
**Snippet:**
```lua
require("ActivityDungeon1015_Shop_CardHeadBgByName")
require("ActivityDungeon1015_Shop_ItemNumberByName")
require("ActivityDungeon1015_Shop_UseMarkByName")

function GetActivityDungeon1015_Shop_ItemBtnUis(ui)
  local uis = {}
  uis.CardHeadBg = GetActivityDungeon1015_Shop_CardHeadBgUis(ui:GetChild("CardHeadBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.ItemNumber = GetActivityDungeon1015_Shop_ItemNumberUis(ui:GetChild("ItemNumber"))
```

---

## Activty/a15/ActivityDungeon1015_Shop_ItemByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Shop_ItemUis
**Requires:**
- ActivityDungeon1015_Shop_SellOutByName
**Snippet:**
```lua
require("ActivityDungeon1015_Shop_SellOutByName")

function GetActivityDungeon1015_Shop_ItemUis(ui)
  local uis = {}
  uis.ItemBtn = ui:GetChild("ItemBtn")
  uis.SellOut = GetActivityDungeon1015_Shop_SellOutUis(ui:GetChild("SellOut"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Shop_ItemNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Shop_ItemNumberUis
**Snippet:**
```lua
function GetActivityDungeon1015_Shop_ItemNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Shop_ItemRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Shop_ItemRegionUis
**Requires:**
- ActivityDungeon1015_Shop_TitleByName
**Snippet:**
```lua
require("ActivityDungeon1015_Shop_TitleByName")

function GetActivityDungeon1015_Shop_ItemRegionUis(ui)
  local uis = {}
  uis.ShopTitle = GetActivityDungeon1015_Shop_TitleUis(ui:GetChild("ShopTitle"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Shop_SellOutByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Shop_SellOutUis
**Snippet:**
```lua
function GetActivityDungeon1015_Shop_SellOutUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Shop_StarByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Shop_StarUis
**Snippet:**
```lua
function GetActivityDungeon1015_Shop_StarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Shop_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Shop_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1015_Shop_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Shop_TitleByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Shop_TitleUis
**Snippet:**
```lua
function GetActivityDungeon1015_Shop_TitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Shop_UseMarkByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Shop_UseMarkUis
**Snippet:**
```lua
function GetActivityDungeon1015_Shop_UseMarkUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_SignBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_SignBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1015_SignBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_SignByName.lua.lua
**Functions:**
- GetActivityDungeon1015_SignUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1015_Sign_RewardListByName
- ActivityDungeon1015_Sign_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1015_Sign_RewardListByName")
require("ActivityDungeon1015_Sign_TimeByName")

function GetActivityDungeon1015_SignUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.RewardList = GetActivityDungeon1015_Sign_RewardListUis(ui:GetChild("RewardList"))
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.Time = GetActivityDungeon1015_Sign_TimeUis(ui:GetChild("Time"))
```

---

## Activty/a15/ActivityDungeon1015_SignWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1015_SignWindowUis
**Requires:**
- ActivityDungeon1015_SignByName
**Snippet:**
```lua
require("ActivityDungeon1015_SignByName")

function GetActivityDungeon1015_SignWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1015_SignUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Sign_AllFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Sign_AllFrameUis
**Requires:**
- ActivityDungeon1015_Sign_ItemFrameByName
- ActivityDungeon1015_Sign_CardFrameByName
**Snippet:**
```lua
require("ActivityDungeon1015_Sign_ItemFrameByName")
require("ActivityDungeon1015_Sign_CardFrameByName")

function GetActivityDungeon1015_Sign_AllFrameUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1015_Sign_ItemFrameUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1015_Sign_CardFrameUis(ui:GetChild("CardFrame"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a15/ActivityDungeon1015_Sign_CardFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Sign_CardFrameUis
**Requires:**
- ActivityDungeon1015_Sign_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1015_Sign_ItemCardPicByName")

function GetActivityDungeon1015_Sign_CardFrameUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1015_Sign_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a15/ActivityDungeon1015_Sign_GetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Sign_GetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_Sign_GetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Sign_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Sign_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1015_Sign_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Sign_ItemFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Sign_ItemFrameUis
**Snippet:**
```lua
function GetActivityDungeon1015_Sign_ItemFrameUis(ui)
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

## Activty/a15/ActivityDungeon1015_Sign_RewardAniByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Sign_RewardAniUis
**Requires:**
- ActivityDungeon1015_Sign_RewardByName
**Snippet:**
```lua
require("ActivityDungeon1015_Sign_RewardByName")

function GetActivityDungeon1015_Sign_RewardAniUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1015_Sign_RewardUis(ui:GetChild("Reward"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Sign_RewardByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Sign_RewardUis
**Requires:**
- ActivityDungeon1015_Sign_AllFrameByName
**Snippet:**
```lua
require("ActivityDungeon1015_Sign_AllFrameByName")

function GetActivityDungeon1015_Sign_RewardUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1015_Sign_AllFrameUis(ui:GetChild("Item"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Sign_RewardListByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Sign_RewardListUis
**Snippet:**
```lua
function GetActivityDungeon1015_Sign_RewardListUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_Sign_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1015_Sign_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1015_Sign_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_TaskAllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_TaskAllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_TaskAllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1015_TaskBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_TaskByName.lua.lua
**Functions:**
- GetActivityDungeon1015_TaskUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1015_TaskTitleByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1015_TaskTitleByName")

function GetActivityDungeon1015_TaskUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TaskTitle = GetActivityDungeon1015_TaskTitleUis(ui:GetChild("TaskTitle"))
  uis.TaskTipsList = ui:GetChild("TaskTipsList")
  uis.AllGetBtn = ui:GetChild("AllGetBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a15/ActivityDungeon1015_TaskGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1015_TaskGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1015_TaskGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_TaskMaxByName.lua.lua
**Functions:**
- GetActivityDungeon1015_TaskMaxUis
**Snippet:**
```lua
function GetActivityDungeon1015_TaskMaxUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_TaskProgressByName.lua.lua
**Functions:**
- GetActivityDungeon1015_TaskProgressUis
**Snippet:**
```lua
function GetActivityDungeon1015_TaskProgressUis(ui)
  local uis = {}
  
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_TaskTipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1015_TaskTipsAniUis
**Requires:**
- ActivityDungeon1015_TaskTipsByName
**Snippet:**
```lua
require("ActivityDungeon1015_TaskTipsByName")

function GetActivityDungeon1015_TaskTipsAniUis(ui)
  local uis = {}
  uis.TaskTips = GetActivityDungeon1015_TaskTipsUis(ui:GetChild("TaskTips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_TaskTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1015_TaskTipsUis
**Requires:**
- ActivityDungeon1015_TaskProgressByName
**Snippet:**
```lua
require("ActivityDungeon1015_TaskProgressByName")

function GetActivityDungeon1015_TaskTipsUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.RewardList = ui:GetChild("RewardList")
  uis.TaskProgress = GetActivityDungeon1015_TaskProgressUis(ui:GetChild("TaskProgress"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a15/ActivityDungeon1015_TaskTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1015_TaskTitleUis
**Snippet:**
```lua
function GetActivityDungeon1015_TaskTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a15/ActivityDungeon1015_TaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1015_TaskWindowUis
**Requires:**
- ActivityDungeon1015_TaskByName
**Snippet:**
```lua
require("ActivityDungeon1015_TaskByName")

function GetActivityDungeon1015_TaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1015_TaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---
