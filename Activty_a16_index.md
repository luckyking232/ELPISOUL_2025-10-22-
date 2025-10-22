# Activty/a16

## Activty/a16/ActivityDungeon1016_ActivityDungeonByName.lua.lua
**Functions:**
- GetActivityDungeon1016_ActivityDungeonUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1016_MainTitleByName
- ActivityDungeon1016_ReviewWordByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1016_MainTitleByName")
require("ActivityDungeon1016_ReviewWordByName")
require("CommonResource_CurrencyReturnByName")

function GetActivityDungeon1016_ActivityDungeonUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.MainTitle = GetActivityDungeon1016_MainTitleUis(ui:GetChild("MainTitle"))
  uis.PlotBtn = ui:GetChild("PlotBtn")
```

---

## Activty/a16/ActivityDungeon1016_ActivityDungeonWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1016_ActivityDungeonWindowUis
**Requires:**
- ActivityDungeon1016_ActivityDungeonByName
**Snippet:**
```lua
require("ActivityDungeon1016_ActivityDungeonByName")

function GetActivityDungeon1016_ActivityDungeonWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1016_ActivityDungeonUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_AddBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_AddBtnUis
**Snippet:**
```lua
function GetActivityDungeon1016_AddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_BossBattleByName.lua.lua
**Functions:**
- GetActivityDungeon1016_BossBattleUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1016_BossBattle_InfoByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1016_BossBattle_InfoByName")

function GetActivityDungeon1016_BossBattleUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.Info = GetActivityDungeon1016_BossBattle_InfoUis(ui:GetChild("Info"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a16/ActivityDungeon1016_BossBattleWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1016_BossBattleWindowUis
**Requires:**
- ActivityDungeon1016_BossBattleByName
**Snippet:**
```lua
require("ActivityDungeon1016_BossBattleByName")

function GetActivityDungeon1016_BossBattleWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1016_BossBattleUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_BossBattle_Info1ByName.lua.lua
**Functions:**
- GetActivityDungeon1016_BossBattle_Info1Uis
**Snippet:**
```lua
function GetActivityDungeon1016_BossBattle_Info1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_BossBattle_InfoByName.lua.lua
**Functions:**
- GetActivityDungeon1016_BossBattle_InfoUis
**Requires:**
- ActivityDungeon1016_BossBattle_Info1ByName
**Snippet:**
```lua
require("ActivityDungeon1016_BossBattle_Info1ByName")

function GetActivityDungeon1016_BossBattle_InfoUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = GetActivityDungeon1016_BossBattle_Info1Uis(ui:GetChild("WordTxt"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_BossBattle_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1016_BossBattle_TipsAniUis
**Requires:**
- ActivityDungeon1016_BossBattle_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1016_BossBattle_TipsByName")

function GetActivityDungeon1016_BossBattle_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1016_BossBattle_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_BossBattle_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1016_BossBattle_TipsUis
**Requires:**
- ActivityDungeon1016_BossBattle_TipsRewardByName
**Snippet:**
```lua
require("ActivityDungeon1016_BossBattle_TipsRewardByName")

function GetActivityDungeon1016_BossBattle_TipsUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1016_BossBattle_TipsRewardUis(ui:GetChild("Reward"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.NumberWordTxt = ui:GetChild("NumberWordTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a16/ActivityDungeon1016_BossBattle_TipsRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1016_BossBattle_TipsRewardUis
**Snippet:**
```lua
function GetActivityDungeon1016_BossBattle_TipsRewardUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_BossBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_BossBtnUis
**Snippet:**
```lua
function GetActivityDungeon1016_BossBtnUis(ui)
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

## Activty/a16/ActivityDungeon1016_BuyLevelBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_BuyLevelBtnUis
**Snippet:**
```lua
function GetActivityDungeon1016_BuyLevelBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_BuyLevelDes1ByName.lua.lua
**Functions:**
- GetActivityDungeon1016_BuyLevelDes1Uis
**Requires:**
- ActivityDungeon1016_NumberStripByName
- ActivityDungeon1016_BuyPriceNumberByName
**Snippet:**
```lua
require("ActivityDungeon1016_NumberStripByName")
require("ActivityDungeon1016_BuyPriceNumberByName")

function GetActivityDungeon1016_BuyLevelDes1Uis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.NumberStrip = GetActivityDungeon1016_NumberStripUis(ui:GetChild("NumberStrip"))
  uis.BuyPriceNumber = GetActivityDungeon1016_BuyPriceNumberUis(ui:GetChild("BuyPriceNumber"))
```

---

## Activty/a16/ActivityDungeon1016_BuyLevelDes2ByName.lua.lua
**Functions:**
- GetActivityDungeon1016_BuyLevelDes2Uis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1016_BuyLevelDes1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1016_BuyLevelDes1ByName")

function GetActivityDungeon1016_BuyLevelDes2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.BuyLevelDes1 = GetActivityDungeon1016_BuyLevelDes1Uis(ui:GetChild("BuyLevelDes1"))
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.root = ui
```

---

## Activty/a16/ActivityDungeon1016_BuyLevelDesWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1016_BuyLevelDesWindowUis
**Requires:**
- ActivityDungeon1016_BuyLevelDes2ByName
**Snippet:**
```lua
require("ActivityDungeon1016_BuyLevelDes2ByName")

function GetActivityDungeon1016_BuyLevelDesWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1016_BuyLevelDes2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_BuyLevelItemByName.lua.lua
**Functions:**
- GetActivityDungeon1016_BuyLevelItemUis
**Requires:**
- ActivityDungeon1016_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1016_PassReward_AllFrame_EByName")

function GetActivityDungeon1016_BuyLevelItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1016_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_BuyPriceNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1016_BuyPriceNumberUis
**Snippet:**
```lua
function GetActivityDungeon1016_BuyPriceNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_ChallengeByName.lua.lua
**Functions:**
- GetActivityDungeon1016_ChallengeUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1016_MapListByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1016_MapListByName")

function GetActivityDungeon1016_ChallengeUis(ui)
  local uis = {}
  uis.BgList = ui:GetChild("BgList")
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Map = GetActivityDungeon1016_MapListUis(ui:GetChild("Map"))
  uis.ShopBtn = ui:GetChild("ShopBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a16/ActivityDungeon1016_ChallengeChapterBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_ChallengeChapterBtnUis
**Requires:**
- ActivityDungeon1016_NormalPointLockByName
**Snippet:**
```lua
require("ActivityDungeon1016_NormalPointLockByName")

function GetActivityDungeon1016_ChallengeChapterBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Lock = GetActivityDungeon1016_NormalPointLockUis(ui:GetChild("Lock"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Activty/a16/ActivityDungeon1016_ChallengeShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_ChallengeShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1016_ChallengeShopBtnUis(ui)
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

## Activty/a16/ActivityDungeon1016_ChallengeWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1016_ChallengeWindowUis
**Requires:**
- ActivityDungeon1016_ChallengeByName
**Snippet:**
```lua
require("ActivityDungeon1016_ChallengeByName")

function GetActivityDungeon1016_ChallengeWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1016_ChallengeUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MainTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MainTitleUis
**Snippet:**
```lua
function GetActivityDungeon1016_MainTitleUis(ui)
  local uis = {}
  
  uis.Time1Txt = ui:GetChild("Time1Txt")
  uis.Time2Txt = ui:GetChild("Time2Txt")
  uis.reviewCtr = ui:GetController("review")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MapBottom_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MapBottom_1Uis
**Snippet:**
```lua
function GetActivityDungeon1016_MapBottom_1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MapBottom_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MapBottom_2Uis
**Snippet:**
```lua
function GetActivityDungeon1016_MapBottom_2Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MapListByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MapListUis
**Snippet:**
```lua
function GetActivityDungeon1016_MapListUis(ui)
  local uis = {}
  
  uis.MapList = ui:GetChild("MapList")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Map_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Map_1Uis
**Snippet:**
```lua
function GetActivityDungeon1016_Map_1Uis(ui)
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

## Activty/a16/ActivityDungeon1016_Map_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Map_2Uis
**Snippet:**
```lua
function GetActivityDungeon1016_Map_2Uis(ui)
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

## Activty/a16/ActivityDungeon1016_MaterialBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MaterialBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1016_MaterialBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
```

---

## Activty/a16/ActivityDungeon1016_MaterialByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MaterialUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1016_Material_BattleNumberByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1016_Material_BattleNumberByName")

function GetActivityDungeon1016_MaterialUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.BattleNumber = GetActivityDungeon1016_Material_BattleNumberUis(ui:GetChild("BattleNumber"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a16/ActivityDungeon1016_MaterialWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MaterialWindowUis
**Requires:**
- ActivityDungeon1016_MaterialByName
**Snippet:**
```lua
require("ActivityDungeon1016_MaterialByName")

function GetActivityDungeon1016_MaterialWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1016_MaterialUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Material_BattleAniByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Material_BattleAniUis
**Requires:**
- ActivityDungeon1016_Material_BattleByName
**Snippet:**
```lua
require("ActivityDungeon1016_Material_BattleByName")

function GetActivityDungeon1016_Material_BattleAniUis(ui)
  local uis = {}
  uis.Battle = GetActivityDungeon1016_Material_BattleUis(ui:GetChild("Battle"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Material_BattleByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Material_BattleUis
**Snippet:**
```lua
function GetActivityDungeon1016_Material_BattleUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Material_BattleNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Material_BattleNumberUis
**Snippet:**
```lua
function GetActivityDungeon1016_Material_BattleNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MaxBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MaxBtnUis
**Snippet:**
```lua
function GetActivityDungeon1016_MaxBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MinBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MinBtnUis
**Snippet:**
```lua
function GetActivityDungeon1016_MinBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniGameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniGameBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1016_MiniGameBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniGameByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniGameUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1016_MiniMain_TopByName
- ActivityDungeon1016_MiniMain_BottonByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1016_MiniMain_TopByName")
require("ActivityDungeon1016_MiniMain_BottonByName")

function GetActivityDungeon1016_MiniGameUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Top = GetActivityDungeon1016_MiniMain_TopUis(ui:GetChild("Top"))
  uis.Botton = GetActivityDungeon1016_MiniMain_BottonUis(ui:GetChild("Botton"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a16/ActivityDungeon1016_MiniGameStartByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniGameStartUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1016_MiniStart_OperateRegionByName
- ActivityDungeon1016_MiniStart_IntegralByName
- ActivityDungeon1016_MiniStart_Tips1ByName
- ActivityDungeon1016_MiniStart_Tips2ByName
- ActivityDungeon1016_MiniStart_PreviewByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1016_MiniStart_OperateRegionByName")
require("ActivityDungeon1016_MiniStart_IntegralByName")
require("ActivityDungeon1016_MiniStart_Tips1ByName")
require("ActivityDungeon1016_MiniStart_Tips2ByName")
require("ActivityDungeon1016_MiniStart_PreviewByName")

function GetActivityDungeon1016_MiniGameStartUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
```

---

## Activty/a16/ActivityDungeon1016_MiniGameStartWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniGameStartWindowUis
**Requires:**
- ActivityDungeon1016_MiniGameStartByName
**Snippet:**
```lua
require("ActivityDungeon1016_MiniGameStartByName")

function GetActivityDungeon1016_MiniGameStartWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1016_MiniGameStartUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniGameWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniGameWindowUis
**Requires:**
- ActivityDungeon1016_MiniGameByName
**Snippet:**
```lua
require("ActivityDungeon1016_MiniGameByName")

function GetActivityDungeon1016_MiniGameWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1016_MiniGameUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniMain_BottonByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniMain_BottonUis
**Requires:**
- ActivityDungeon1016_MiniMain_TodayTaskByName
**Snippet:**
```lua
require("ActivityDungeon1016_MiniMain_TodayTaskByName")

function GetActivityDungeon1016_MiniMain_BottonUis(ui)
  local uis = {}
  uis.TaskBtn = ui:GetChild("TaskBtn")
  uis.TodayTask = GetActivityDungeon1016_MiniMain_TodayTaskUis(ui:GetChild("TodayTask"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniMain_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniMain_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1016_MiniMain_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniMain_RecordBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniMain_RecordBtnUis
**Snippet:**
```lua
function GetActivityDungeon1016_MiniMain_RecordBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniMain_StartBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniMain_StartBtnUis
**Snippet:**
```lua
function GetActivityDungeon1016_MiniMain_StartBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniMain_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniMain_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1016_MiniMain_TaskBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniMain_TodayTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniMain_TodayTaskUis
**Requires:**
- ActivityDungeon1016_PassReward_AllFrame_EByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("ActivityDungeon1016_PassReward_AllFrame_EByName")
require("CommonResource_RedDotByName")

function GetActivityDungeon1016_MiniMain_TodayTaskUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1016_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a16/ActivityDungeon1016_MiniMain_TopByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniMain_TopUis
**Requires:**
- ActivityDungeon1016_MiniMain_IntegralByName
**Snippet:**
```lua
require("ActivityDungeon1016_MiniMain_IntegralByName")

function GetActivityDungeon1016_MiniMain_TopUis(ui)
  local uis = {}
  uis.Integral = GetActivityDungeon1016_MiniMain_IntegralUis(ui:GetChild("Integral"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniStart_Block01ByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniStart_Block01Uis
**Requires:**
- ActivityDungeon1016_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1016_MiniStart_BlockByName")

function GetActivityDungeon1016_MiniStart_Block01Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.root = ui
  return uis
```

---

## Activty/a16/ActivityDungeon1016_MiniStart_Block02ByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniStart_Block02Uis
**Requires:**
- ActivityDungeon1016_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1016_MiniStart_BlockByName")

function GetActivityDungeon1016_MiniStart_Block02Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.root = ui
  return uis
```

---

## Activty/a16/ActivityDungeon1016_MiniStart_Block03ByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniStart_Block03Uis
**Requires:**
- ActivityDungeon1016_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1016_MiniStart_BlockByName")

function GetActivityDungeon1016_MiniStart_Block03Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.B5 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B5"))
  uis.root = ui
```

---

## Activty/a16/ActivityDungeon1016_MiniStart_Block04ByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniStart_Block04Uis
**Requires:**
- ActivityDungeon1016_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1016_MiniStart_BlockByName")

function GetActivityDungeon1016_MiniStart_Block04Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.root = ui
  return uis
```

---

## Activty/a16/ActivityDungeon1016_MiniStart_Block05ByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniStart_Block05Uis
**Requires:**
- ActivityDungeon1016_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1016_MiniStart_BlockByName")

function GetActivityDungeon1016_MiniStart_Block05Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniStart_Block06ByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniStart_Block06Uis
**Requires:**
- ActivityDungeon1016_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1016_MiniStart_BlockByName")

function GetActivityDungeon1016_MiniStart_Block06Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.root = ui
  return uis
```

---

## Activty/a16/ActivityDungeon1016_MiniStart_Block07ByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniStart_Block07Uis
**Requires:**
- ActivityDungeon1016_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1016_MiniStart_BlockByName")

function GetActivityDungeon1016_MiniStart_Block07Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.B5 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B5"))
  uis.B6 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B6"))
```

---

## Activty/a16/ActivityDungeon1016_MiniStart_Block08ByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniStart_Block08Uis
**Requires:**
- ActivityDungeon1016_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1016_MiniStart_BlockByName")

function GetActivityDungeon1016_MiniStart_Block08Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.B5 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B5"))
  uis.root = ui
```

---

## Activty/a16/ActivityDungeon1016_MiniStart_Block09ByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniStart_Block09Uis
**Requires:**
- ActivityDungeon1016_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1016_MiniStart_BlockByName")

function GetActivityDungeon1016_MiniStart_Block09Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.root = ui
  return uis
```

---

## Activty/a16/ActivityDungeon1016_MiniStart_Block10ByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniStart_Block10Uis
**Requires:**
- ActivityDungeon1016_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1016_MiniStart_BlockByName")

function GetActivityDungeon1016_MiniStart_Block10Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniStart_Block11ByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniStart_Block11Uis
**Requires:**
- ActivityDungeon1016_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1016_MiniStart_BlockByName")

function GetActivityDungeon1016_MiniStart_Block11Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniStart_Block12ByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniStart_Block12Uis
**Requires:**
- ActivityDungeon1016_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1016_MiniStart_BlockByName")

function GetActivityDungeon1016_MiniStart_Block12Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniStart_Block13ByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniStart_Block13Uis
**Requires:**
- ActivityDungeon1016_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1016_MiniStart_BlockByName")

function GetActivityDungeon1016_MiniStart_Block13Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.B5 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B5"))
  uis.B6 = GetActivityDungeon1016_MiniStart_BlockUis(ui:GetChild("B6"))
```

---

## Activty/a16/ActivityDungeon1016_MiniStart_BlockByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniStart_BlockUis
**Snippet:**
```lua
function GetActivityDungeon1016_MiniStart_BlockUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniStart_CloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniStart_CloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1016_MiniStart_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniStart_EndAgainBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniStart_EndAgainBtnUis
**Snippet:**
```lua
function GetActivityDungeon1016_MiniStart_EndAgainBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniStart_EndCloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniStart_EndCloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1016_MiniStart_EndCloseBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniStart_EndRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniStart_EndRewardUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetActivityDungeon1016_MiniStart_EndRewardUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.AgainBtn = ui:GetChild("AgainBtn")
  uis.CloseBtn = ui:GetChild("CloseBtn")
```

---

## Activty/a16/ActivityDungeon1016_MiniStart_EndRewardWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniStart_EndRewardWindowUis
**Requires:**
- ActivityDungeon1016_MiniStart_EndRewardByName
**Snippet:**
```lua
require("ActivityDungeon1016_MiniStart_EndRewardByName")

function GetActivityDungeon1016_MiniStart_EndRewardWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1016_MiniStart_EndRewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniStart_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniStart_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1016_MiniStart_IntegralUis(ui)
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

## Activty/a16/ActivityDungeon1016_MiniStart_OperateRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniStart_OperateRegionUis
**Snippet:**
```lua
function GetActivityDungeon1016_MiniStart_OperateRegionUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniStart_PreviewByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniStart_PreviewUis
**Snippet:**
```lua
function GetActivityDungeon1016_MiniStart_PreviewUis(ui)
  local uis = {}
  
  uis.Preview1Loader = ui:GetChild("Preview1Loader")
  uis.Preview2Loader = ui:GetChild("Preview2Loader")
  uis.Preview3Loader = ui:GetChild("Preview3Loader")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniStart_PreviewItemByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniStart_PreviewItemUis
**Snippet:**
```lua
function GetActivityDungeon1016_MiniStart_PreviewItemUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniStart_Tips1ByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniStart_Tips1Uis
**Requires:**
- ActivityDungeon1016_MiniStart_Tips1numberByName
**Snippet:**
```lua
require("ActivityDungeon1016_MiniStart_Tips1numberByName")

function GetActivityDungeon1016_MiniStart_Tips1Uis(ui)
  local uis = {}
  uis.NumberTxt = GetActivityDungeon1016_MiniStart_Tips1numberUis(ui:GetChild("NumberTxt"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniStart_Tips1numberByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniStart_Tips1numberUis
**Snippet:**
```lua
function GetActivityDungeon1016_MiniStart_Tips1numberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniStart_Tips2ByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniStart_Tips2Uis
**Snippet:**
```lua
function GetActivityDungeon1016_MiniStart_Tips2Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniTaskUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1016_MiniTask_IntegralByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1016_MiniTask_IntegralByName")

function GetActivityDungeon1016_MiniTaskUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Integral = GetActivityDungeon1016_MiniTask_IntegralUis(ui:GetChild("Integral"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a16/ActivityDungeon1016_MiniTaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniTaskWindowUis
**Requires:**
- ActivityDungeon1016_MiniTaskByName
**Snippet:**
```lua
require("ActivityDungeon1016_MiniTaskByName")

function GetActivityDungeon1016_MiniTaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1016_MiniTaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniTask_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniTask_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1016_MiniTask_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniTask_RewardItemByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniTask_RewardItemUis
**Snippet:**
```lua
function GetActivityDungeon1016_MiniTask_RewardItemUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniTask_RewardItemGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniTask_RewardItemGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1016_MiniTask_RewardItemGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniTask_TipsAniUis
**Requires:**
- ActivityDungeon1016_MiniTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1016_MiniTask_TipsByName")

function GetActivityDungeon1016_MiniTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1016_MiniTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_MiniTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1016_MiniTask_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1016_MiniTask_TipsUis(ui)
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

## Activty/a16/ActivityDungeon1016_NormalBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_NormalBtnUis
**Snippet:**
```lua
function GetActivityDungeon1016_NormalBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_NormalPoint1BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_NormalPoint1BtnUis
**Snippet:**
```lua
function GetActivityDungeon1016_NormalPoint1BtnUis(ui)
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

## Activty/a16/ActivityDungeon1016_NormalPoint2BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_NormalPoint2BtnUis
**Snippet:**
```lua
function GetActivityDungeon1016_NormalPoint2BtnUis(ui)
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

## Activty/a16/ActivityDungeon1016_NormalPointLockByName.lua.lua
**Functions:**
- GetActivityDungeon1016_NormalPointLockUis
**Snippet:**
```lua
function GetActivityDungeon1016_NormalPointLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_NumberStripByName.lua.lua
**Functions:**
- GetActivityDungeon1016_NumberStripUis
**Snippet:**
```lua
function GetActivityDungeon1016_NumberStripUis(ui)
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

## Activty/a16/ActivityDungeon1016_PassBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1016_PassBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_PassClothes_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassClothes_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1016_PassClothes_BuyBtnUis(ui)
  local uis = {}
  
  uis.PriceTxt = ui:GetChild("PriceTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_PassClothes_BuyRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassClothes_BuyRewardUis
**Snippet:**
```lua
function GetActivityDungeon1016_PassClothes_BuyRewardUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_PassClothes_CardQBByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassClothes_CardQBUis
**Snippet:**
```lua
function GetActivityDungeon1016_PassClothes_CardQBUis(ui)
  local uis = {}
  
  uis.QBHolder = ui:GetChild("QBHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_PassClothes_ClothseRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassClothes_ClothseRegionUis
**Requires:**
- ActivityDungeon1016_PassClothes_WordByName
- ActivityDungeon1016_PassClothes_CardQBByName
- ActivityDungeon1016_PassClothes_BuyRewardByName
**Snippet:**
```lua
require("ActivityDungeon1016_PassClothes_WordByName")
require("ActivityDungeon1016_PassClothes_CardQBByName")
require("ActivityDungeon1016_PassClothes_BuyRewardByName")

function GetActivityDungeon1016_PassClothes_ClothseRegionUis(ui)
  local uis = {}
  uis.Word = GetActivityDungeon1016_PassClothes_WordUis(ui:GetChild("Word"))
  uis.CardQB = GetActivityDungeon1016_PassClothes_CardQBUis(ui:GetChild("CardQB"))
  uis.BuyReward = GetActivityDungeon1016_PassClothes_BuyRewardUis(ui:GetChild("BuyReward"))
  uis.BuyBtn = ui:GetChild("BuyBtn")
```

---

## Activty/a16/ActivityDungeon1016_PassClothes_NameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassClothes_NameBtnUis
**Snippet:**
```lua
function GetActivityDungeon1016_PassClothes_NameBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_PassClothes_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassClothes_WordUis
**Snippet:**
```lua
function GetActivityDungeon1016_PassClothes_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_PassportByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassportUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1016_PassReward_RewardRegionByName
- ActivityDungeon1016_PassTask_TaskRegionByName
- ActivityDungeon1016_PassClothes_ClothseRegionByName
- ActivityDungeon1016_Passport_LevelByName
- ActivityDungeon1016_Sign_TimeByName
- ActivityDungeon1016_Passport_TabRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1016_PassReward_RewardRegionByName")
require("ActivityDungeon1016_PassTask_TaskRegionByName")
require("ActivityDungeon1016_PassClothes_ClothseRegionByName")
require("ActivityDungeon1016_Passport_LevelByName")
require("ActivityDungeon1016_Sign_TimeByName")
require("ActivityDungeon1016_Passport_TabRegionByName")

function GetActivityDungeon1016_PassportUis(ui)
  local uis = {}
```

---

## Activty/a16/ActivityDungeon1016_PassportUp_LevelUpBgByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassportUp_LevelUpBgUis
**Snippet:**
```lua
function GetActivityDungeon1016_PassportUp_LevelUpBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_PassportUp_LevelUpTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassportUp_LevelUpTipsUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1016_PassportUp_LevelUpBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1016_PassportUp_LevelUpBgByName")

function GetActivityDungeon1016_PassportUp_LevelUpTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.LevelUpBg = GetActivityDungeon1016_PassportUp_LevelUpBgUis(ui:GetChild("LevelUpBg"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
```

---

## Activty/a16/ActivityDungeon1016_PassportUp_LevelUpTipsWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassportUp_LevelUpTipsWindowUis
**Requires:**
- ActivityDungeon1016_PassportUp_LevelUpTipsByName
**Snippet:**
```lua
require("ActivityDungeon1016_PassportUp_LevelUpTipsByName")

function GetActivityDungeon1016_PassportUp_LevelUpTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1016_PassportUp_LevelUpTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_PassportWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassportWindowUis
**Requires:**
- ActivityDungeon1016_PassportByName
**Snippet:**
```lua
require("ActivityDungeon1016_PassportByName")

function GetActivityDungeon1016_PassportWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1016_PassportUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Passport_AllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Passport_AllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1016_Passport_AllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Passport_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Passport_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1016_Passport_BuyBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Passport_ExpProgressBarByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Passport_ExpProgressBarUis
**Requires:**
- ActivityDungeon1016_Passport_ExpProgressFillByName
**Snippet:**
```lua
require("ActivityDungeon1016_Passport_ExpProgressFillByName")

function GetActivityDungeon1016_Passport_ExpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetActivityDungeon1016_Passport_ExpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Passport_ExpProgressFillByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Passport_ExpProgressFillUis
**Snippet:**
```lua
function GetActivityDungeon1016_Passport_ExpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Passport_LevelByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Passport_LevelUis
**Snippet:**
```lua
function GetActivityDungeon1016_Passport_LevelUis(ui)
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

## Activty/a16/ActivityDungeon1016_Passport_TabBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Passport_TabBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1016_Passport_TabBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## Activty/a16/ActivityDungeon1016_Passport_TabRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Passport_TabRegionUis
**Snippet:**
```lua
function GetActivityDungeon1016_Passport_TabRegionUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_PassReward_AllFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassReward_AllFrame_EUis
**Requires:**
- ActivityDungeon1016_PassReward_ItemFrame_EByName
- ActivityDungeon1016_PassReward_CardFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1016_PassReward_ItemFrame_EByName")
require("ActivityDungeon1016_PassReward_CardFrame_EByName")

function GetActivityDungeon1016_PassReward_AllFrame_EUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1016_PassReward_ItemFrame_EUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1016_PassReward_CardFrame_EUis(ui:GetChild("CardFrame"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## Activty/a16/ActivityDungeon1016_PassReward_AllFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassReward_AllFrame_MUis
**Requires:**
- ActivityDungeon1016_PassReward_ItemFrame_MByName
- ActivityDungeon1016_PassReward_CardFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1016_PassReward_ItemFrame_MByName")
require("ActivityDungeon1016_PassReward_CardFrame_MByName")

function GetActivityDungeon1016_PassReward_AllFrame_MUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1016_PassReward_ItemFrame_MUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1016_PassReward_CardFrame_MUis(ui:GetChild("CardFrame"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a16/ActivityDungeon1016_PassReward_CardFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassReward_CardFrame_EUis
**Requires:**
- ActivityDungeon1016_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1016_PassReward_ItemCardPicByName")

function GetActivityDungeon1016_PassReward_CardFrame_EUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1016_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a16/ActivityDungeon1016_PassReward_CardFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassReward_CardFrame_MUis
**Requires:**
- ActivityDungeon1016_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1016_PassReward_ItemCardPicByName")

function GetActivityDungeon1016_PassReward_CardFrame_MUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1016_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a16/ActivityDungeon1016_PassReward_EndTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassReward_EndTwoUis
**Requires:**
- ActivityDungeon1016_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1016_PassReward_AllFrame_EByName")

function GetActivityDungeon1016_PassReward_EndTwoUis(ui)
  local uis = {}
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.Item1 = GetActivityDungeon1016_PassReward_AllFrame_EUis(ui:GetChild("Item1"))
  uis.Item2 = GetActivityDungeon1016_PassReward_AllFrame_EUis(ui:GetChild("Item2"))
  uis.root = ui
```

---

## Activty/a16/ActivityDungeon1016_PassReward_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassReward_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1016_PassReward_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_PassReward_ItemFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassReward_ItemFrame_EUis
**Snippet:**
```lua
function GetActivityDungeon1016_PassReward_ItemFrame_EUis(ui)
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

## Activty/a16/ActivityDungeon1016_PassReward_ItemFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassReward_ItemFrame_MUis
**Snippet:**
```lua
function GetActivityDungeon1016_PassReward_ItemFrame_MUis(ui)
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

## Activty/a16/ActivityDungeon1016_PassReward_LevelTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassReward_LevelTitleUis
**Snippet:**
```lua
function GetActivityDungeon1016_PassReward_LevelTitleUis(ui)
  local uis = {}
  
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_PassReward_MiddleRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassReward_MiddleRegionUis
**Snippet:**
```lua
function GetActivityDungeon1016_PassReward_MiddleRegionUis(ui)
  local uis = {}
  
  uis.MiddleList = ui:GetChild("MiddleList")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_PassReward_MidTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassReward_MidTwoUis
**Requires:**
- ActivityDungeon1016_PassReward_MidTwoItemByName
- ActivityDungeon1016_PassReward_LevelTitleByName
**Snippet:**
```lua
require("ActivityDungeon1016_PassReward_MidTwoItemByName")
require("ActivityDungeon1016_PassReward_LevelTitleByName")

function GetActivityDungeon1016_PassReward_MidTwoUis(ui)
  local uis = {}
  uis.Reward1 = GetActivityDungeon1016_PassReward_MidTwoItemUis(ui:GetChild("Reward1"))
  uis.Reward2 = GetActivityDungeon1016_PassReward_MidTwoItemUis(ui:GetChild("Reward2"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Title = GetActivityDungeon1016_PassReward_LevelTitleUis(ui:GetChild("Title"))
```

---

## Activty/a16/ActivityDungeon1016_PassReward_MidTwoItemByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassReward_MidTwoItemUis
**Requires:**
- ActivityDungeon1016_PassReward_AllFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1016_PassReward_AllFrame_MByName")

function GetActivityDungeon1016_PassReward_MidTwoItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1016_PassReward_AllFrame_MUis(ui:GetChild("Item"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_PassReward_PicByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassReward_PicUis
**Snippet:**
```lua
function GetActivityDungeon1016_PassReward_PicUis(ui)
  local uis = {}
  
  uis.BuyTxt = ui:GetChild("BuyTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_PassReward_RewardRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassReward_RewardRegionUis
**Requires:**
- ActivityDungeon1016_PassReward_MiddleRegionByName
- ActivityDungeon1016_PassReward_StartTwoByName
- ActivityDungeon1016_PassReward_EndTwoByName
**Snippet:**
```lua
require("ActivityDungeon1016_PassReward_MiddleRegionByName")
require("ActivityDungeon1016_PassReward_StartTwoByName")
require("ActivityDungeon1016_PassReward_EndTwoByName")

function GetActivityDungeon1016_PassReward_RewardRegionUis(ui)
  local uis = {}
  uis.MiddleList = GetActivityDungeon1016_PassReward_MiddleRegionUis(ui:GetChild("MiddleList"))
  uis.StartTwo = GetActivityDungeon1016_PassReward_StartTwoUis(ui:GetChild("StartTwo"))
  uis.EndTwo = GetActivityDungeon1016_PassReward_EndTwoUis(ui:GetChild("EndTwo"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a16/ActivityDungeon1016_PassReward_StartTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassReward_StartTwoUis
**Requires:**
- ActivityDungeon1016_PassReward_PicByName
**Snippet:**
```lua
require("ActivityDungeon1016_PassReward_PicByName")

function GetActivityDungeon1016_PassReward_StartTwoUis(ui)
  local uis = {}
  uis.Pic = GetActivityDungeon1016_PassReward_PicUis(ui:GetChild("Pic"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_PassTask_TaskRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassTask_TaskRegionUis
**Requires:**
- ActivityDungeon1016_TaskMaxByName
**Snippet:**
```lua
require("ActivityDungeon1016_TaskMaxByName")

function GetActivityDungeon1016_PassTask_TaskRegionUis(ui)
  local uis = {}
  uis.TipsList = ui:GetChild("TipsList")
  uis.Max = GetActivityDungeon1016_TaskMaxUis(ui:GetChild("Max"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_PassTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassTask_TipsAniUis
**Requires:**
- ActivityDungeon1016_PassTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1016_PassTask_TipsByName")

function GetActivityDungeon1016_PassTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1016_PassTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_PassTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassTask_TipsUis
**Requires:**
- ActivityDungeon1016_PassTask_TipsIntegralByName
**Snippet:**
```lua
require("ActivityDungeon1016_PassTask_TipsIntegralByName")

function GetActivityDungeon1016_PassTask_TipsUis(ui)
  local uis = {}
  uis.ProgressTxt = ui:GetChild("ProgressTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Integral = GetActivityDungeon1016_PassTask_TipsIntegralUis(ui:GetChild("Integral"))
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a16/ActivityDungeon1016_PassTask_TipsIntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PassTask_TipsIntegralUis
**Snippet:**
```lua
function GetActivityDungeon1016_PassTask_TipsIntegralUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_PlotBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PlotBtnUis
**Snippet:**
```lua
function GetActivityDungeon1016_PlotBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_PlotByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PlotUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1016_Plot_WordByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1016_Plot_WordByName")

function GetActivityDungeon1016_PlotUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Word = GetActivityDungeon1016_Plot_WordUis(ui:GetChild("Word"))
  uis.PlotList = ui:GetChild("PlotList")
  uis.ProspectBtn = ui:GetChild("ProspectBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a16/ActivityDungeon1016_PlotWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1016_PlotWindowUis
**Requires:**
- ActivityDungeon1016_PlotByName
**Snippet:**
```lua
require("ActivityDungeon1016_PlotByName")

function GetActivityDungeon1016_PlotWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1016_PlotUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Plot_ProspectBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Plot_ProspectBtnUis
**Snippet:**
```lua
function GetActivityDungeon1016_Plot_ProspectBtnUis(ui)
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

## Activty/a16/ActivityDungeon1016_Plot_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Plot_TipsAniUis
**Requires:**
- ActivityDungeon1016_Plot_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1016_Plot_TipsByName")

function GetActivityDungeon1016_Plot_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1016_Plot_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Plot_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Plot_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1016_Plot_TipsUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Plot_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Plot_WordUis
**Snippet:**
```lua
function GetActivityDungeon1016_Plot_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_ReduceBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_ReduceBtnUis
**Snippet:**
```lua
function GetActivityDungeon1016_ReduceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_ReviewWordByName.lua.lua
**Functions:**
- GetActivityDungeon1016_ReviewWordUis
**Snippet:**
```lua
function GetActivityDungeon1016_ReviewWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_ShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_ShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1016_ShopBtnUis(ui)
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

## Activty/a16/ActivityDungeon1016_ShopByName.lua.lua
**Functions:**
- GetActivityDungeon1016_ShopUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1016_Shop_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1016_Shop_TimeByName")

function GetActivityDungeon1016_ShopUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Time = GetActivityDungeon1016_Shop_TimeUis(ui:GetChild("Time"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a16/ActivityDungeon1016_ShopWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1016_ShopWindowUis
**Requires:**
- ActivityDungeon1016_ShopByName
**Snippet:**
```lua
require("ActivityDungeon1016_ShopByName")

function GetActivityDungeon1016_ShopWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1016_ShopUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Shop_CardHeadBgByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Shop_CardHeadBgUis
**Snippet:**
```lua
function GetActivityDungeon1016_Shop_CardHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Shop_ItemAniByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Shop_ItemAniUis
**Requires:**
- ActivityDungeon1016_Shop_ItemByName
**Snippet:**
```lua
require("ActivityDungeon1016_Shop_ItemByName")

function GetActivityDungeon1016_Shop_ItemAniUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1016_Shop_ItemUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Shop_ItemBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Shop_ItemBtnUis
**Requires:**
- ActivityDungeon1016_Shop_CardHeadBgByName
- ActivityDungeon1016_Shop_ItemNumberByName
- ActivityDungeon1016_Shop_UseMarkByName
**Snippet:**
```lua
require("ActivityDungeon1016_Shop_CardHeadBgByName")
require("ActivityDungeon1016_Shop_ItemNumberByName")
require("ActivityDungeon1016_Shop_UseMarkByName")

function GetActivityDungeon1016_Shop_ItemBtnUis(ui)
  local uis = {}
  uis.CardHeadBg = GetActivityDungeon1016_Shop_CardHeadBgUis(ui:GetChild("CardHeadBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.ItemNumber = GetActivityDungeon1016_Shop_ItemNumberUis(ui:GetChild("ItemNumber"))
```

---

## Activty/a16/ActivityDungeon1016_Shop_ItemByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Shop_ItemUis
**Requires:**
- ActivityDungeon1016_Shop_SellOutByName
**Snippet:**
```lua
require("ActivityDungeon1016_Shop_SellOutByName")

function GetActivityDungeon1016_Shop_ItemUis(ui)
  local uis = {}
  uis.ItemBtn = ui:GetChild("ItemBtn")
  uis.SellOut = GetActivityDungeon1016_Shop_SellOutUis(ui:GetChild("SellOut"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Shop_ItemNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Shop_ItemNumberUis
**Snippet:**
```lua
function GetActivityDungeon1016_Shop_ItemNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Shop_ItemRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Shop_ItemRegionUis
**Requires:**
- ActivityDungeon1016_Shop_TitleByName
**Snippet:**
```lua
require("ActivityDungeon1016_Shop_TitleByName")

function GetActivityDungeon1016_Shop_ItemRegionUis(ui)
  local uis = {}
  uis.ShopTitle = GetActivityDungeon1016_Shop_TitleUis(ui:GetChild("ShopTitle"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Shop_SellOutByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Shop_SellOutUis
**Snippet:**
```lua
function GetActivityDungeon1016_Shop_SellOutUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Shop_StarByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Shop_StarUis
**Snippet:**
```lua
function GetActivityDungeon1016_Shop_StarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Shop_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Shop_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1016_Shop_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Shop_TitleByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Shop_TitleUis
**Snippet:**
```lua
function GetActivityDungeon1016_Shop_TitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Shop_UseMarkByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Shop_UseMarkUis
**Snippet:**
```lua
function GetActivityDungeon1016_Shop_UseMarkUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_SignBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_SignBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1016_SignBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_SignByName.lua.lua
**Functions:**
- GetActivityDungeon1016_SignUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1016_Sign_RewardListByName
- ActivityDungeon1016_Sign_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1016_Sign_RewardListByName")
require("ActivityDungeon1016_Sign_TimeByName")

function GetActivityDungeon1016_SignUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.RewardList = GetActivityDungeon1016_Sign_RewardListUis(ui:GetChild("RewardList"))
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.Time = GetActivityDungeon1016_Sign_TimeUis(ui:GetChild("Time"))
```

---

## Activty/a16/ActivityDungeon1016_SignWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1016_SignWindowUis
**Requires:**
- ActivityDungeon1016_SignByName
**Snippet:**
```lua
require("ActivityDungeon1016_SignByName")

function GetActivityDungeon1016_SignWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1016_SignUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Sign_AllFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Sign_AllFrameUis
**Requires:**
- ActivityDungeon1016_Sign_ItemFrameByName
- ActivityDungeon1016_Sign_CardFrameByName
**Snippet:**
```lua
require("ActivityDungeon1016_Sign_ItemFrameByName")
require("ActivityDungeon1016_Sign_CardFrameByName")

function GetActivityDungeon1016_Sign_AllFrameUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1016_Sign_ItemFrameUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1016_Sign_CardFrameUis(ui:GetChild("CardFrame"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a16/ActivityDungeon1016_Sign_CardFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Sign_CardFrameUis
**Requires:**
- ActivityDungeon1016_Sign_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1016_Sign_ItemCardPicByName")

function GetActivityDungeon1016_Sign_CardFrameUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1016_Sign_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a16/ActivityDungeon1016_Sign_GetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Sign_GetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1016_Sign_GetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Sign_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Sign_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1016_Sign_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Sign_ItemFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Sign_ItemFrameUis
**Snippet:**
```lua
function GetActivityDungeon1016_Sign_ItemFrameUis(ui)
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

## Activty/a16/ActivityDungeon1016_Sign_RewardAniByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Sign_RewardAniUis
**Requires:**
- ActivityDungeon1016_Sign_RewardByName
**Snippet:**
```lua
require("ActivityDungeon1016_Sign_RewardByName")

function GetActivityDungeon1016_Sign_RewardAniUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1016_Sign_RewardUis(ui:GetChild("Reward"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Sign_RewardByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Sign_RewardUis
**Requires:**
- ActivityDungeon1016_Sign_AllFrameByName
**Snippet:**
```lua
require("ActivityDungeon1016_Sign_AllFrameByName")

function GetActivityDungeon1016_Sign_RewardUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1016_Sign_AllFrameUis(ui:GetChild("Item"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Sign_RewardListByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Sign_RewardListUis
**Snippet:**
```lua
function GetActivityDungeon1016_Sign_RewardListUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_Sign_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1016_Sign_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1016_Sign_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_TaskAllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_TaskAllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1016_TaskAllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1016_TaskBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_TaskByName.lua.lua
**Functions:**
- GetActivityDungeon1016_TaskUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1016_TaskTitleByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1016_TaskTitleByName")

function GetActivityDungeon1016_TaskUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TaskTitle = GetActivityDungeon1016_TaskTitleUis(ui:GetChild("TaskTitle"))
  uis.TaskTipsList = ui:GetChild("TaskTipsList")
  uis.AllGetBtn = ui:GetChild("AllGetBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a16/ActivityDungeon1016_TaskGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1016_TaskGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1016_TaskGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_TaskMaxByName.lua.lua
**Functions:**
- GetActivityDungeon1016_TaskMaxUis
**Snippet:**
```lua
function GetActivityDungeon1016_TaskMaxUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_TaskProgressByName.lua.lua
**Functions:**
- GetActivityDungeon1016_TaskProgressUis
**Snippet:**
```lua
function GetActivityDungeon1016_TaskProgressUis(ui)
  local uis = {}
  
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_TaskTipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1016_TaskTipsAniUis
**Requires:**
- ActivityDungeon1016_TaskTipsByName
**Snippet:**
```lua
require("ActivityDungeon1016_TaskTipsByName")

function GetActivityDungeon1016_TaskTipsAniUis(ui)
  local uis = {}
  uis.TaskTips = GetActivityDungeon1016_TaskTipsUis(ui:GetChild("TaskTips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_TaskTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1016_TaskTipsUis
**Requires:**
- ActivityDungeon1016_TaskProgressByName
**Snippet:**
```lua
require("ActivityDungeon1016_TaskProgressByName")

function GetActivityDungeon1016_TaskTipsUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.RewardList = ui:GetChild("RewardList")
  uis.TaskProgress = GetActivityDungeon1016_TaskProgressUis(ui:GetChild("TaskProgress"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a16/ActivityDungeon1016_TaskTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1016_TaskTitleUis
**Snippet:**
```lua
function GetActivityDungeon1016_TaskTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a16/ActivityDungeon1016_TaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1016_TaskWindowUis
**Requires:**
- ActivityDungeon1016_TaskByName
**Snippet:**
```lua
require("ActivityDungeon1016_TaskByName")

function GetActivityDungeon1016_TaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1016_TaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---
