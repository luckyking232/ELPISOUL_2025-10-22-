# Activty/a18

## Activty/a18/ActivityDungeon1018_ActivityDungeonByName.lua.lua
**Functions:**
- GetActivityDungeon1018_ActivityDungeonUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1018_MainTitleByName
- ActivityDungeon1018_ReviewWordByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1018_MainTitleByName")
require("ActivityDungeon1018_ReviewWordByName")
require("CommonResource_CurrencyReturnByName")

function GetActivityDungeon1018_ActivityDungeonUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.MainTitle = GetActivityDungeon1018_MainTitleUis(ui:GetChild("MainTitle"))
  uis.PlotBtn = ui:GetChild("PlotBtn")
```

---

## Activty/a18/ActivityDungeon1018_ActivityDungeonWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1018_ActivityDungeonWindowUis
**Requires:**
- ActivityDungeon1018_ActivityDungeonByName
**Snippet:**
```lua
require("ActivityDungeon1018_ActivityDungeonByName")

function GetActivityDungeon1018_ActivityDungeonWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1018_ActivityDungeonUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_AddBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_AddBtnUis
**Snippet:**
```lua
function GetActivityDungeon1018_AddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_BossBattleByName.lua.lua
**Functions:**
- GetActivityDungeon1018_BossBattleUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1018_BossBattle_InfoByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1018_BossBattle_InfoByName")

function GetActivityDungeon1018_BossBattleUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.Info = GetActivityDungeon1018_BossBattle_InfoUis(ui:GetChild("Info"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a18/ActivityDungeon1018_BossBattleWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1018_BossBattleWindowUis
**Requires:**
- ActivityDungeon1018_BossBattleByName
**Snippet:**
```lua
require("ActivityDungeon1018_BossBattleByName")

function GetActivityDungeon1018_BossBattleWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1018_BossBattleUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_BossBattle_Info1ByName.lua.lua
**Functions:**
- GetActivityDungeon1018_BossBattle_Info1Uis
**Snippet:**
```lua
function GetActivityDungeon1018_BossBattle_Info1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_BossBattle_InfoByName.lua.lua
**Functions:**
- GetActivityDungeon1018_BossBattle_InfoUis
**Requires:**
- ActivityDungeon1018_BossBattle_Info1ByName
**Snippet:**
```lua
require("ActivityDungeon1018_BossBattle_Info1ByName")

function GetActivityDungeon1018_BossBattle_InfoUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = GetActivityDungeon1018_BossBattle_Info1Uis(ui:GetChild("WordTxt"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_BossBattle_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1018_BossBattle_TipsAniUis
**Requires:**
- ActivityDungeon1018_BossBattle_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1018_BossBattle_TipsByName")

function GetActivityDungeon1018_BossBattle_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1018_BossBattle_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_BossBattle_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1018_BossBattle_TipsUis
**Requires:**
- ActivityDungeon1018_BossBattle_TipsRewardByName
**Snippet:**
```lua
require("ActivityDungeon1018_BossBattle_TipsRewardByName")

function GetActivityDungeon1018_BossBattle_TipsUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1018_BossBattle_TipsRewardUis(ui:GetChild("Reward"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.NumberWordTxt = ui:GetChild("NumberWordTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a18/ActivityDungeon1018_BossBattle_TipsRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1018_BossBattle_TipsRewardUis
**Snippet:**
```lua
function GetActivityDungeon1018_BossBattle_TipsRewardUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_BossBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_BossBtnUis
**Snippet:**
```lua
function GetActivityDungeon1018_BossBtnUis(ui)
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

## Activty/a18/ActivityDungeon1018_BuyLevelBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_BuyLevelBtnUis
**Snippet:**
```lua
function GetActivityDungeon1018_BuyLevelBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_BuyLevelDes1ByName.lua.lua
**Functions:**
- GetActivityDungeon1018_BuyLevelDes1Uis
**Requires:**
- ActivityDungeon1018_NumberStripByName
- ActivityDungeon1018_BuyPriceNumberByName
**Snippet:**
```lua
require("ActivityDungeon1018_NumberStripByName")
require("ActivityDungeon1018_BuyPriceNumberByName")

function GetActivityDungeon1018_BuyLevelDes1Uis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.NumberStrip = GetActivityDungeon1018_NumberStripUis(ui:GetChild("NumberStrip"))
  uis.BuyPriceNumber = GetActivityDungeon1018_BuyPriceNumberUis(ui:GetChild("BuyPriceNumber"))
```

---

## Activty/a18/ActivityDungeon1018_BuyLevelDes2ByName.lua.lua
**Functions:**
- GetActivityDungeon1018_BuyLevelDes2Uis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1018_BuyLevelDes1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1018_BuyLevelDes1ByName")

function GetActivityDungeon1018_BuyLevelDes2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.BuyLevelDes1 = GetActivityDungeon1018_BuyLevelDes1Uis(ui:GetChild("BuyLevelDes1"))
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.root = ui
```

---

## Activty/a18/ActivityDungeon1018_BuyLevelDesWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1018_BuyLevelDesWindowUis
**Requires:**
- ActivityDungeon1018_BuyLevelDes2ByName
**Snippet:**
```lua
require("ActivityDungeon1018_BuyLevelDes2ByName")

function GetActivityDungeon1018_BuyLevelDesWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1018_BuyLevelDes2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_BuyLevelItemByName.lua.lua
**Functions:**
- GetActivityDungeon1018_BuyLevelItemUis
**Requires:**
- ActivityDungeon1018_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1018_PassReward_AllFrame_EByName")

function GetActivityDungeon1018_BuyLevelItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1018_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_BuyPriceNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1018_BuyPriceNumberUis
**Snippet:**
```lua
function GetActivityDungeon1018_BuyPriceNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_ChallengeByName.lua.lua
**Functions:**
- GetActivityDungeon1018_ChallengeUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1018_MapListByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1018_MapListByName")

function GetActivityDungeon1018_ChallengeUis(ui)
  local uis = {}
  uis.BgList = ui:GetChild("BgList")
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Map = GetActivityDungeon1018_MapListUis(ui:GetChild("Map"))
  uis.ShopBtn = ui:GetChild("ShopBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a18/ActivityDungeon1018_ChallengeChapterBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_ChallengeChapterBtnUis
**Requires:**
- ActivityDungeon1018_NormalPointLockByName
**Snippet:**
```lua
require("ActivityDungeon1018_NormalPointLockByName")

function GetActivityDungeon1018_ChallengeChapterBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Lock = GetActivityDungeon1018_NormalPointLockUis(ui:GetChild("Lock"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Activty/a18/ActivityDungeon1018_ChallengeShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_ChallengeShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1018_ChallengeShopBtnUis(ui)
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

## Activty/a18/ActivityDungeon1018_ChallengeWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1018_ChallengeWindowUis
**Requires:**
- ActivityDungeon1018_ChallengeByName
**Snippet:**
```lua
require("ActivityDungeon1018_ChallengeByName")

function GetActivityDungeon1018_ChallengeWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1018_ChallengeUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MainTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MainTitleUis
**Snippet:**
```lua
function GetActivityDungeon1018_MainTitleUis(ui)
  local uis = {}
  
  uis.Time1Txt = ui:GetChild("Time1Txt")
  uis.Time2Txt = ui:GetChild("Time2Txt")
  uis.reviewCtr = ui:GetController("review")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MapBottom_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MapBottom_1Uis
**Snippet:**
```lua
function GetActivityDungeon1018_MapBottom_1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MapBottom_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MapBottom_2Uis
**Snippet:**
```lua
function GetActivityDungeon1018_MapBottom_2Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MapListByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MapListUis
**Snippet:**
```lua
function GetActivityDungeon1018_MapListUis(ui)
  local uis = {}
  
  uis.MapList = ui:GetChild("MapList")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Map_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Map_1Uis
**Snippet:**
```lua
function GetActivityDungeon1018_Map_1Uis(ui)
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

## Activty/a18/ActivityDungeon1018_Map_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Map_2Uis
**Snippet:**
```lua
function GetActivityDungeon1018_Map_2Uis(ui)
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

## Activty/a18/ActivityDungeon1018_MaterialBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MaterialBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1018_MaterialBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
```

---

## Activty/a18/ActivityDungeon1018_MaterialByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MaterialUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1018_Material_BattleNumberByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1018_Material_BattleNumberByName")

function GetActivityDungeon1018_MaterialUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.BattleNumber = GetActivityDungeon1018_Material_BattleNumberUis(ui:GetChild("BattleNumber"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a18/ActivityDungeon1018_MaterialWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MaterialWindowUis
**Requires:**
- ActivityDungeon1018_MaterialByName
**Snippet:**
```lua
require("ActivityDungeon1018_MaterialByName")

function GetActivityDungeon1018_MaterialWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1018_MaterialUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Material_BattleAniByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Material_BattleAniUis
**Requires:**
- ActivityDungeon1018_Material_BattleByName
**Snippet:**
```lua
require("ActivityDungeon1018_Material_BattleByName")

function GetActivityDungeon1018_Material_BattleAniUis(ui)
  local uis = {}
  uis.Battle = GetActivityDungeon1018_Material_BattleUis(ui:GetChild("Battle"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Material_BattleByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Material_BattleUis
**Snippet:**
```lua
function GetActivityDungeon1018_Material_BattleUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Material_BattleNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Material_BattleNumberUis
**Snippet:**
```lua
function GetActivityDungeon1018_Material_BattleNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MaxBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MaxBtnUis
**Snippet:**
```lua
function GetActivityDungeon1018_MaxBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MinBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MinBtnUis
**Snippet:**
```lua
function GetActivityDungeon1018_MinBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MiniGameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniGameBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1018_MiniGameBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MiniGameByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniGameUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1018_MiniMain_TopByName
- ActivityDungeon1018_MiniMain_BottonByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1018_MiniMain_TopByName")
require("ActivityDungeon1018_MiniMain_BottonByName")

function GetActivityDungeon1018_MiniGameUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Top = GetActivityDungeon1018_MiniMain_TopUis(ui:GetChild("Top"))
  uis.Botton = GetActivityDungeon1018_MiniMain_BottonUis(ui:GetChild("Botton"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a18/ActivityDungeon1018_MiniGameStartByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniGameStartUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1018_MiniStart_OperateRegionByName
- ActivityDungeon1018_MiniStart_IntegralByName
- ActivityDungeon1018_MiniStart_LeftByName
- ActivityDungeon1018_MiniStart_RightByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1018_MiniStart_OperateRegionByName")
require("ActivityDungeon1018_MiniStart_IntegralByName")
require("ActivityDungeon1018_MiniStart_LeftByName")
require("ActivityDungeon1018_MiniStart_RightByName")

function GetActivityDungeon1018_MiniGameStartUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.OperateRegion = GetActivityDungeon1018_MiniStart_OperateRegionUis(ui:GetChild("OperateRegion"))
```

---

## Activty/a18/ActivityDungeon1018_MiniGameStartWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniGameStartWindowUis
**Requires:**
- ActivityDungeon1018_MiniGameStartByName
**Snippet:**
```lua
require("ActivityDungeon1018_MiniGameStartByName")

function GetActivityDungeon1018_MiniGameStartWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1018_MiniGameStartUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MiniGameWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniGameWindowUis
**Requires:**
- ActivityDungeon1018_MiniGameByName
**Snippet:**
```lua
require("ActivityDungeon1018_MiniGameByName")

function GetActivityDungeon1018_MiniGameWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1018_MiniGameUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MiniMain_BottonByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniMain_BottonUis
**Requires:**
- ActivityDungeon1018_MiniMain_TodayTaskByName
**Snippet:**
```lua
require("ActivityDungeon1018_MiniMain_TodayTaskByName")

function GetActivityDungeon1018_MiniMain_BottonUis(ui)
  local uis = {}
  uis.TaskBtn = ui:GetChild("TaskBtn")
  uis.TodayTask = GetActivityDungeon1018_MiniMain_TodayTaskUis(ui:GetChild("TodayTask"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MiniMain_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniMain_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1018_MiniMain_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MiniMain_RecordBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniMain_RecordBtnUis
**Snippet:**
```lua
function GetActivityDungeon1018_MiniMain_RecordBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MiniMain_StartBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniMain_StartBtnUis
**Snippet:**
```lua
function GetActivityDungeon1018_MiniMain_StartBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MiniMain_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniMain_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1018_MiniMain_TaskBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MiniMain_TodayTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniMain_TodayTaskUis
**Requires:**
- ActivityDungeon1018_PassReward_AllFrame_EByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("ActivityDungeon1018_PassReward_AllFrame_EByName")
require("CommonResource_RedDotByName")

function GetActivityDungeon1018_MiniMain_TodayTaskUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1018_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a18/ActivityDungeon1018_MiniMain_TopByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniMain_TopUis
**Requires:**
- ActivityDungeon1018_MiniMain_IntegralByName
**Snippet:**
```lua
require("ActivityDungeon1018_MiniMain_IntegralByName")

function GetActivityDungeon1018_MiniMain_TopUis(ui)
  local uis = {}
  uis.Integral = GetActivityDungeon1018_MiniMain_IntegralUis(ui:GetChild("Integral"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MiniStart_BlockByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniStart_BlockUis
**Snippet:**
```lua
function GetActivityDungeon1018_MiniStart_BlockUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MiniStart_CloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniStart_CloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1018_MiniStart_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MiniStart_DragBlockByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniStart_DragBlockUis
**Requires:**
- ActivityDungeon1018_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1018_MiniStart_BlockByName")

function GetActivityDungeon1018_MiniStart_DragBlockUis(ui)
  local uis = {}
  uis.Block1 = GetActivityDungeon1018_MiniStart_BlockUis(ui:GetChild("Block1"))
  uis.Block2 = GetActivityDungeon1018_MiniStart_BlockUis(ui:GetChild("Block2"))
  uis.Block3 = GetActivityDungeon1018_MiniStart_BlockUis(ui:GetChild("Block3"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a18/ActivityDungeon1018_MiniStart_EndAgainBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniStart_EndAgainBtnUis
**Snippet:**
```lua
function GetActivityDungeon1018_MiniStart_EndAgainBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MiniStart_EndCloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniStart_EndCloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1018_MiniStart_EndCloseBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MiniStart_EndRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniStart_EndRewardUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetActivityDungeon1018_MiniStart_EndRewardUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.AgainBtn = ui:GetChild("AgainBtn")
  uis.CloseBtn = ui:GetChild("CloseBtn")
```

---

## Activty/a18/ActivityDungeon1018_MiniStart_EndRewardWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniStart_EndRewardWindowUis
**Requires:**
- ActivityDungeon1018_MiniStart_EndRewardByName
**Snippet:**
```lua
require("ActivityDungeon1018_MiniStart_EndRewardByName")

function GetActivityDungeon1018_MiniStart_EndRewardWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1018_MiniStart_EndRewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MiniStart_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniStart_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1018_MiniStart_IntegralUis(ui)
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

## Activty/a18/ActivityDungeon1018_MiniStart_LeftByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniStart_LeftUis
**Requires:**
- ActivityDungeon1018_MiniStart_DragBlockByName
**Snippet:**
```lua
require("ActivityDungeon1018_MiniStart_DragBlockByName")

function GetActivityDungeon1018_MiniStart_LeftUis(ui)
  local uis = {}
  uis.LeftProgressBar = ui:GetChild("LeftProgressBar")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.DragBlock = GetActivityDungeon1018_MiniStart_DragBlockUis(ui:GetChild("DragBlock"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Activty/a18/ActivityDungeon1018_MiniStart_LeftProgressBarByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniStart_LeftProgressBarUis
**Snippet:**
```lua
function GetActivityDungeon1018_MiniStart_LeftProgressBarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MiniStart_OperateRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniStart_OperateRegionUis
**Snippet:**
```lua
function GetActivityDungeon1018_MiniStart_OperateRegionUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MiniStart_RightByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniStart_RightUis
**Requires:**
- ActivityDungeon1018_MiniStart_DragBlockByName
**Snippet:**
```lua
require("ActivityDungeon1018_MiniStart_DragBlockByName")

function GetActivityDungeon1018_MiniStart_RightUis(ui)
  local uis = {}
  uis.DragBlock = GetActivityDungeon1018_MiniStart_DragBlockUis(ui:GetChild("DragBlock"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MiniTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniTaskUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1018_MiniTask_IntegralByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1018_MiniTask_IntegralByName")

function GetActivityDungeon1018_MiniTaskUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Integral = GetActivityDungeon1018_MiniTask_IntegralUis(ui:GetChild("Integral"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a18/ActivityDungeon1018_MiniTaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniTaskWindowUis
**Requires:**
- ActivityDungeon1018_MiniTaskByName
**Snippet:**
```lua
require("ActivityDungeon1018_MiniTaskByName")

function GetActivityDungeon1018_MiniTaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1018_MiniTaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MiniTask_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniTask_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1018_MiniTask_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MiniTask_RewardItemByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniTask_RewardItemUis
**Snippet:**
```lua
function GetActivityDungeon1018_MiniTask_RewardItemUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MiniTask_RewardItemGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniTask_RewardItemGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1018_MiniTask_RewardItemGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MiniTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniTask_TipsAniUis
**Requires:**
- ActivityDungeon1018_MiniTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1018_MiniTask_TipsByName")

function GetActivityDungeon1018_MiniTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1018_MiniTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_MiniTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1018_MiniTask_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1018_MiniTask_TipsUis(ui)
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

## Activty/a18/ActivityDungeon1018_NormalBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_NormalBtnUis
**Snippet:**
```lua
function GetActivityDungeon1018_NormalBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_NormalPoint1BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_NormalPoint1BtnUis
**Snippet:**
```lua
function GetActivityDungeon1018_NormalPoint1BtnUis(ui)
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

## Activty/a18/ActivityDungeon1018_NormalPoint2BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_NormalPoint2BtnUis
**Snippet:**
```lua
function GetActivityDungeon1018_NormalPoint2BtnUis(ui)
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

## Activty/a18/ActivityDungeon1018_NormalPointLockByName.lua.lua
**Functions:**
- GetActivityDungeon1018_NormalPointLockUis
**Snippet:**
```lua
function GetActivityDungeon1018_NormalPointLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_NumberStripByName.lua.lua
**Functions:**
- GetActivityDungeon1018_NumberStripUis
**Snippet:**
```lua
function GetActivityDungeon1018_NumberStripUis(ui)
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

## Activty/a18/ActivityDungeon1018_PassBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1018_PassBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_PassClothes_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassClothes_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1018_PassClothes_BuyBtnUis(ui)
  local uis = {}
  
  uis.PriceTxt = ui:GetChild("PriceTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_PassClothes_BuyRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassClothes_BuyRewardUis
**Snippet:**
```lua
function GetActivityDungeon1018_PassClothes_BuyRewardUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_PassClothes_CardQBByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassClothes_CardQBUis
**Snippet:**
```lua
function GetActivityDungeon1018_PassClothes_CardQBUis(ui)
  local uis = {}
  
  uis.QBHolder = ui:GetChild("QBHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_PassClothes_ClothseRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassClothes_ClothseRegionUis
**Requires:**
- ActivityDungeon1018_PassClothes_WordByName
- ActivityDungeon1018_PassClothes_CardQBByName
- ActivityDungeon1018_PassClothes_BuyRewardByName
**Snippet:**
```lua
require("ActivityDungeon1018_PassClothes_WordByName")
require("ActivityDungeon1018_PassClothes_CardQBByName")
require("ActivityDungeon1018_PassClothes_BuyRewardByName")

function GetActivityDungeon1018_PassClothes_ClothseRegionUis(ui)
  local uis = {}
  uis.Word = GetActivityDungeon1018_PassClothes_WordUis(ui:GetChild("Word"))
  uis.CardQB = GetActivityDungeon1018_PassClothes_CardQBUis(ui:GetChild("CardQB"))
  uis.BuyReward = GetActivityDungeon1018_PassClothes_BuyRewardUis(ui:GetChild("BuyReward"))
  uis.BuyBtn = ui:GetChild("BuyBtn")
```

---

## Activty/a18/ActivityDungeon1018_PassClothes_NameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassClothes_NameBtnUis
**Snippet:**
```lua
function GetActivityDungeon1018_PassClothes_NameBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_PassClothes_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassClothes_WordUis
**Snippet:**
```lua
function GetActivityDungeon1018_PassClothes_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_PassportByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassportUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1018_PassReward_RewardRegionByName
- ActivityDungeon1018_PassTask_TaskRegionByName
- ActivityDungeon1018_PassClothes_ClothseRegionByName
- ActivityDungeon1018_Passport_LevelByName
- ActivityDungeon1018_Sign_TimeByName
- ActivityDungeon1018_Passport_TabRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1018_PassReward_RewardRegionByName")
require("ActivityDungeon1018_PassTask_TaskRegionByName")
require("ActivityDungeon1018_PassClothes_ClothseRegionByName")
require("ActivityDungeon1018_Passport_LevelByName")
require("ActivityDungeon1018_Sign_TimeByName")
require("ActivityDungeon1018_Passport_TabRegionByName")

function GetActivityDungeon1018_PassportUis(ui)
  local uis = {}
```

---

## Activty/a18/ActivityDungeon1018_PassportUp_LevelUpBgByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassportUp_LevelUpBgUis
**Snippet:**
```lua
function GetActivityDungeon1018_PassportUp_LevelUpBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_PassportUp_LevelUpTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassportUp_LevelUpTipsUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1018_PassportUp_LevelUpBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1018_PassportUp_LevelUpBgByName")

function GetActivityDungeon1018_PassportUp_LevelUpTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.LevelUpBg = GetActivityDungeon1018_PassportUp_LevelUpBgUis(ui:GetChild("LevelUpBg"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
```

---

## Activty/a18/ActivityDungeon1018_PassportUp_LevelUpTipsWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassportUp_LevelUpTipsWindowUis
**Requires:**
- ActivityDungeon1018_PassportUp_LevelUpTipsByName
**Snippet:**
```lua
require("ActivityDungeon1018_PassportUp_LevelUpTipsByName")

function GetActivityDungeon1018_PassportUp_LevelUpTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1018_PassportUp_LevelUpTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_PassportWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassportWindowUis
**Requires:**
- ActivityDungeon1018_PassportByName
**Snippet:**
```lua
require("ActivityDungeon1018_PassportByName")

function GetActivityDungeon1018_PassportWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1018_PassportUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Passport_AllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Passport_AllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1018_Passport_AllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Passport_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Passport_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1018_Passport_BuyBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Passport_ExpProgressBarByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Passport_ExpProgressBarUis
**Requires:**
- ActivityDungeon1018_Passport_ExpProgressFillByName
**Snippet:**
```lua
require("ActivityDungeon1018_Passport_ExpProgressFillByName")

function GetActivityDungeon1018_Passport_ExpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetActivityDungeon1018_Passport_ExpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Passport_ExpProgressFillByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Passport_ExpProgressFillUis
**Snippet:**
```lua
function GetActivityDungeon1018_Passport_ExpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Passport_LevelByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Passport_LevelUis
**Snippet:**
```lua
function GetActivityDungeon1018_Passport_LevelUis(ui)
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

## Activty/a18/ActivityDungeon1018_Passport_TabBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Passport_TabBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1018_Passport_TabBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## Activty/a18/ActivityDungeon1018_Passport_TabRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Passport_TabRegionUis
**Snippet:**
```lua
function GetActivityDungeon1018_Passport_TabRegionUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_PassReward_AllFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassReward_AllFrame_EUis
**Requires:**
- ActivityDungeon1018_PassReward_ItemFrame_EByName
- ActivityDungeon1018_PassReward_CardFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1018_PassReward_ItemFrame_EByName")
require("ActivityDungeon1018_PassReward_CardFrame_EByName")

function GetActivityDungeon1018_PassReward_AllFrame_EUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1018_PassReward_ItemFrame_EUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1018_PassReward_CardFrame_EUis(ui:GetChild("CardFrame"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## Activty/a18/ActivityDungeon1018_PassReward_AllFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassReward_AllFrame_MUis
**Requires:**
- ActivityDungeon1018_PassReward_ItemFrame_MByName
- ActivityDungeon1018_PassReward_CardFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1018_PassReward_ItemFrame_MByName")
require("ActivityDungeon1018_PassReward_CardFrame_MByName")

function GetActivityDungeon1018_PassReward_AllFrame_MUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1018_PassReward_ItemFrame_MUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1018_PassReward_CardFrame_MUis(ui:GetChild("CardFrame"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a18/ActivityDungeon1018_PassReward_CardFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassReward_CardFrame_EUis
**Requires:**
- ActivityDungeon1018_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1018_PassReward_ItemCardPicByName")

function GetActivityDungeon1018_PassReward_CardFrame_EUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1018_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a18/ActivityDungeon1018_PassReward_CardFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassReward_CardFrame_MUis
**Requires:**
- ActivityDungeon1018_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1018_PassReward_ItemCardPicByName")

function GetActivityDungeon1018_PassReward_CardFrame_MUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1018_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a18/ActivityDungeon1018_PassReward_EndTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassReward_EndTwoUis
**Requires:**
- ActivityDungeon1018_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1018_PassReward_AllFrame_EByName")

function GetActivityDungeon1018_PassReward_EndTwoUis(ui)
  local uis = {}
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.Item1 = GetActivityDungeon1018_PassReward_AllFrame_EUis(ui:GetChild("Item1"))
  uis.Item2 = GetActivityDungeon1018_PassReward_AllFrame_EUis(ui:GetChild("Item2"))
  uis.root = ui
```

---

## Activty/a18/ActivityDungeon1018_PassReward_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassReward_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1018_PassReward_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_PassReward_ItemFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassReward_ItemFrame_EUis
**Snippet:**
```lua
function GetActivityDungeon1018_PassReward_ItemFrame_EUis(ui)
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

## Activty/a18/ActivityDungeon1018_PassReward_ItemFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassReward_ItemFrame_MUis
**Snippet:**
```lua
function GetActivityDungeon1018_PassReward_ItemFrame_MUis(ui)
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

## Activty/a18/ActivityDungeon1018_PassReward_LevelTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassReward_LevelTitleUis
**Snippet:**
```lua
function GetActivityDungeon1018_PassReward_LevelTitleUis(ui)
  local uis = {}
  
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_PassReward_MiddleRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassReward_MiddleRegionUis
**Snippet:**
```lua
function GetActivityDungeon1018_PassReward_MiddleRegionUis(ui)
  local uis = {}
  
  uis.MiddleList = ui:GetChild("MiddleList")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_PassReward_MidTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassReward_MidTwoUis
**Requires:**
- ActivityDungeon1018_PassReward_MidTwoItemByName
- ActivityDungeon1018_PassReward_LevelTitleByName
**Snippet:**
```lua
require("ActivityDungeon1018_PassReward_MidTwoItemByName")
require("ActivityDungeon1018_PassReward_LevelTitleByName")

function GetActivityDungeon1018_PassReward_MidTwoUis(ui)
  local uis = {}
  uis.Reward1 = GetActivityDungeon1018_PassReward_MidTwoItemUis(ui:GetChild("Reward1"))
  uis.Reward2 = GetActivityDungeon1018_PassReward_MidTwoItemUis(ui:GetChild("Reward2"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Title = GetActivityDungeon1018_PassReward_LevelTitleUis(ui:GetChild("Title"))
```

---

## Activty/a18/ActivityDungeon1018_PassReward_MidTwoItemByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassReward_MidTwoItemUis
**Requires:**
- ActivityDungeon1018_PassReward_AllFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1018_PassReward_AllFrame_MByName")

function GetActivityDungeon1018_PassReward_MidTwoItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1018_PassReward_AllFrame_MUis(ui:GetChild("Item"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_PassReward_PicByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassReward_PicUis
**Snippet:**
```lua
function GetActivityDungeon1018_PassReward_PicUis(ui)
  local uis = {}
  
  uis.BuyTxt = ui:GetChild("BuyTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_PassReward_RewardRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassReward_RewardRegionUis
**Requires:**
- ActivityDungeon1018_PassReward_MiddleRegionByName
- ActivityDungeon1018_PassReward_StartTwoByName
- ActivityDungeon1018_PassReward_EndTwoByName
**Snippet:**
```lua
require("ActivityDungeon1018_PassReward_MiddleRegionByName")
require("ActivityDungeon1018_PassReward_StartTwoByName")
require("ActivityDungeon1018_PassReward_EndTwoByName")

function GetActivityDungeon1018_PassReward_RewardRegionUis(ui)
  local uis = {}
  uis.MiddleList = GetActivityDungeon1018_PassReward_MiddleRegionUis(ui:GetChild("MiddleList"))
  uis.StartTwo = GetActivityDungeon1018_PassReward_StartTwoUis(ui:GetChild("StartTwo"))
  uis.EndTwo = GetActivityDungeon1018_PassReward_EndTwoUis(ui:GetChild("EndTwo"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a18/ActivityDungeon1018_PassReward_StartTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassReward_StartTwoUis
**Requires:**
- ActivityDungeon1018_PassReward_PicByName
**Snippet:**
```lua
require("ActivityDungeon1018_PassReward_PicByName")

function GetActivityDungeon1018_PassReward_StartTwoUis(ui)
  local uis = {}
  uis.Pic = GetActivityDungeon1018_PassReward_PicUis(ui:GetChild("Pic"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_PassTask_TaskRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassTask_TaskRegionUis
**Requires:**
- ActivityDungeon1018_TaskMaxByName
**Snippet:**
```lua
require("ActivityDungeon1018_TaskMaxByName")

function GetActivityDungeon1018_PassTask_TaskRegionUis(ui)
  local uis = {}
  uis.TipsList = ui:GetChild("TipsList")
  uis.Max = GetActivityDungeon1018_TaskMaxUis(ui:GetChild("Max"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_PassTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassTask_TipsAniUis
**Requires:**
- ActivityDungeon1018_PassTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1018_PassTask_TipsByName")

function GetActivityDungeon1018_PassTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1018_PassTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_PassTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassTask_TipsUis
**Requires:**
- ActivityDungeon1018_PassTask_TipsIntegralByName
**Snippet:**
```lua
require("ActivityDungeon1018_PassTask_TipsIntegralByName")

function GetActivityDungeon1018_PassTask_TipsUis(ui)
  local uis = {}
  uis.ProgressTxt = ui:GetChild("ProgressTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Integral = GetActivityDungeon1018_PassTask_TipsIntegralUis(ui:GetChild("Integral"))
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a18/ActivityDungeon1018_PassTask_TipsIntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PassTask_TipsIntegralUis
**Snippet:**
```lua
function GetActivityDungeon1018_PassTask_TipsIntegralUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_PlotBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PlotBtnUis
**Snippet:**
```lua
function GetActivityDungeon1018_PlotBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_PlotByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PlotUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1018_Plot_WordByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1018_Plot_WordByName")

function GetActivityDungeon1018_PlotUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Word = GetActivityDungeon1018_Plot_WordUis(ui:GetChild("Word"))
  uis.PlotList = ui:GetChild("PlotList")
  uis.ProspectBtn = ui:GetChild("ProspectBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a18/ActivityDungeon1018_PlotWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1018_PlotWindowUis
**Requires:**
- ActivityDungeon1018_PlotByName
**Snippet:**
```lua
require("ActivityDungeon1018_PlotByName")

function GetActivityDungeon1018_PlotWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1018_PlotUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Plot_ProspectBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Plot_ProspectBtnUis
**Snippet:**
```lua
function GetActivityDungeon1018_Plot_ProspectBtnUis(ui)
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

## Activty/a18/ActivityDungeon1018_Plot_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Plot_TipsAniUis
**Requires:**
- ActivityDungeon1018_Plot_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1018_Plot_TipsByName")

function GetActivityDungeon1018_Plot_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1018_Plot_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Plot_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Plot_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1018_Plot_TipsUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Plot_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Plot_WordUis
**Snippet:**
```lua
function GetActivityDungeon1018_Plot_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_ReduceBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_ReduceBtnUis
**Snippet:**
```lua
function GetActivityDungeon1018_ReduceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_ReviewWordByName.lua.lua
**Functions:**
- GetActivityDungeon1018_ReviewWordUis
**Snippet:**
```lua
function GetActivityDungeon1018_ReviewWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_ShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_ShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1018_ShopBtnUis(ui)
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

## Activty/a18/ActivityDungeon1018_ShopByName.lua.lua
**Functions:**
- GetActivityDungeon1018_ShopUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1018_Shop_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1018_Shop_TimeByName")

function GetActivityDungeon1018_ShopUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Time = GetActivityDungeon1018_Shop_TimeUis(ui:GetChild("Time"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a18/ActivityDungeon1018_ShopWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1018_ShopWindowUis
**Requires:**
- ActivityDungeon1018_ShopByName
**Snippet:**
```lua
require("ActivityDungeon1018_ShopByName")

function GetActivityDungeon1018_ShopWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1018_ShopUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Shop_CardHeadBgByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Shop_CardHeadBgUis
**Snippet:**
```lua
function GetActivityDungeon1018_Shop_CardHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Shop_ItemAniByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Shop_ItemAniUis
**Requires:**
- ActivityDungeon1018_Shop_ItemByName
**Snippet:**
```lua
require("ActivityDungeon1018_Shop_ItemByName")

function GetActivityDungeon1018_Shop_ItemAniUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1018_Shop_ItemUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Shop_ItemBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Shop_ItemBtnUis
**Requires:**
- ActivityDungeon1018_Shop_CardHeadBgByName
- ActivityDungeon1018_Shop_ItemNumberByName
- ActivityDungeon1018_Shop_UseMarkByName
**Snippet:**
```lua
require("ActivityDungeon1018_Shop_CardHeadBgByName")
require("ActivityDungeon1018_Shop_ItemNumberByName")
require("ActivityDungeon1018_Shop_UseMarkByName")

function GetActivityDungeon1018_Shop_ItemBtnUis(ui)
  local uis = {}
  uis.CardHeadBg = GetActivityDungeon1018_Shop_CardHeadBgUis(ui:GetChild("CardHeadBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.ItemNumber = GetActivityDungeon1018_Shop_ItemNumberUis(ui:GetChild("ItemNumber"))
```

---

## Activty/a18/ActivityDungeon1018_Shop_ItemByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Shop_ItemUis
**Requires:**
- ActivityDungeon1018_Shop_SellOutByName
**Snippet:**
```lua
require("ActivityDungeon1018_Shop_SellOutByName")

function GetActivityDungeon1018_Shop_ItemUis(ui)
  local uis = {}
  uis.ItemBtn = ui:GetChild("ItemBtn")
  uis.SellOut = GetActivityDungeon1018_Shop_SellOutUis(ui:GetChild("SellOut"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Shop_ItemNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Shop_ItemNumberUis
**Snippet:**
```lua
function GetActivityDungeon1018_Shop_ItemNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Shop_ItemRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Shop_ItemRegionUis
**Requires:**
- ActivityDungeon1018_Shop_TitleByName
**Snippet:**
```lua
require("ActivityDungeon1018_Shop_TitleByName")

function GetActivityDungeon1018_Shop_ItemRegionUis(ui)
  local uis = {}
  uis.ShopTitle = GetActivityDungeon1018_Shop_TitleUis(ui:GetChild("ShopTitle"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Shop_SellOutByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Shop_SellOutUis
**Snippet:**
```lua
function GetActivityDungeon1018_Shop_SellOutUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Shop_StarByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Shop_StarUis
**Snippet:**
```lua
function GetActivityDungeon1018_Shop_StarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Shop_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Shop_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1018_Shop_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Shop_TitleByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Shop_TitleUis
**Snippet:**
```lua
function GetActivityDungeon1018_Shop_TitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Shop_UseMarkByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Shop_UseMarkUis
**Snippet:**
```lua
function GetActivityDungeon1018_Shop_UseMarkUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_SignBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_SignBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1018_SignBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_SignByName.lua.lua
**Functions:**
- GetActivityDungeon1018_SignUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1018_Sign_RewardListByName
- ActivityDungeon1018_Sign_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1018_Sign_RewardListByName")
require("ActivityDungeon1018_Sign_TimeByName")

function GetActivityDungeon1018_SignUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.RewardList = GetActivityDungeon1018_Sign_RewardListUis(ui:GetChild("RewardList"))
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.Time = GetActivityDungeon1018_Sign_TimeUis(ui:GetChild("Time"))
```

---

## Activty/a18/ActivityDungeon1018_SignWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1018_SignWindowUis
**Requires:**
- ActivityDungeon1018_SignByName
**Snippet:**
```lua
require("ActivityDungeon1018_SignByName")

function GetActivityDungeon1018_SignWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1018_SignUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Sign_AllFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Sign_AllFrameUis
**Requires:**
- ActivityDungeon1018_Sign_ItemFrameByName
- ActivityDungeon1018_Sign_CardFrameByName
**Snippet:**
```lua
require("ActivityDungeon1018_Sign_ItemFrameByName")
require("ActivityDungeon1018_Sign_CardFrameByName")

function GetActivityDungeon1018_Sign_AllFrameUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1018_Sign_ItemFrameUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1018_Sign_CardFrameUis(ui:GetChild("CardFrame"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a18/ActivityDungeon1018_Sign_CardFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Sign_CardFrameUis
**Requires:**
- ActivityDungeon1018_Sign_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1018_Sign_ItemCardPicByName")

function GetActivityDungeon1018_Sign_CardFrameUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1018_Sign_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a18/ActivityDungeon1018_Sign_GetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Sign_GetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1018_Sign_GetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Sign_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Sign_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1018_Sign_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Sign_ItemFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Sign_ItemFrameUis
**Snippet:**
```lua
function GetActivityDungeon1018_Sign_ItemFrameUis(ui)
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

## Activty/a18/ActivityDungeon1018_Sign_RewardAniByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Sign_RewardAniUis
**Requires:**
- ActivityDungeon1018_Sign_RewardByName
**Snippet:**
```lua
require("ActivityDungeon1018_Sign_RewardByName")

function GetActivityDungeon1018_Sign_RewardAniUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1018_Sign_RewardUis(ui:GetChild("Reward"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Sign_RewardByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Sign_RewardUis
**Requires:**
- ActivityDungeon1018_Sign_AllFrameByName
**Snippet:**
```lua
require("ActivityDungeon1018_Sign_AllFrameByName")

function GetActivityDungeon1018_Sign_RewardUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1018_Sign_AllFrameUis(ui:GetChild("Item"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Sign_RewardListByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Sign_RewardListUis
**Snippet:**
```lua
function GetActivityDungeon1018_Sign_RewardListUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_Sign_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1018_Sign_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1018_Sign_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_TaskAllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_TaskAllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1018_TaskAllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1018_TaskBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_TaskByName.lua.lua
**Functions:**
- GetActivityDungeon1018_TaskUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1018_TaskTitleByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1018_TaskTitleByName")

function GetActivityDungeon1018_TaskUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TaskTitle = GetActivityDungeon1018_TaskTitleUis(ui:GetChild("TaskTitle"))
  uis.TaskTipsList = ui:GetChild("TaskTipsList")
  uis.AllGetBtn = ui:GetChild("AllGetBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a18/ActivityDungeon1018_TaskGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1018_TaskGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1018_TaskGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_TaskMaxByName.lua.lua
**Functions:**
- GetActivityDungeon1018_TaskMaxUis
**Snippet:**
```lua
function GetActivityDungeon1018_TaskMaxUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_TaskProgressByName.lua.lua
**Functions:**
- GetActivityDungeon1018_TaskProgressUis
**Snippet:**
```lua
function GetActivityDungeon1018_TaskProgressUis(ui)
  local uis = {}
  
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_TaskTipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1018_TaskTipsAniUis
**Requires:**
- ActivityDungeon1018_TaskTipsByName
**Snippet:**
```lua
require("ActivityDungeon1018_TaskTipsByName")

function GetActivityDungeon1018_TaskTipsAniUis(ui)
  local uis = {}
  uis.TaskTips = GetActivityDungeon1018_TaskTipsUis(ui:GetChild("TaskTips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_TaskTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1018_TaskTipsUis
**Requires:**
- ActivityDungeon1018_TaskProgressByName
**Snippet:**
```lua
require("ActivityDungeon1018_TaskProgressByName")

function GetActivityDungeon1018_TaskTipsUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.RewardList = ui:GetChild("RewardList")
  uis.TaskProgress = GetActivityDungeon1018_TaskProgressUis(ui:GetChild("TaskProgress"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a18/ActivityDungeon1018_TaskTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1018_TaskTitleUis
**Snippet:**
```lua
function GetActivityDungeon1018_TaskTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a18/ActivityDungeon1018_TaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1018_TaskWindowUis
**Requires:**
- ActivityDungeon1018_TaskByName
**Snippet:**
```lua
require("ActivityDungeon1018_TaskByName")

function GetActivityDungeon1018_TaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1018_TaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---
