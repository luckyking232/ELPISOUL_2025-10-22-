# Activty/a20

## Activty/a20/ActivityDungeon1020_ActivityDungeonByName.lua.lua
**Functions:**
- GetActivityDungeon1020_ActivityDungeonUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1020_MainTitleByName
- ActivityDungeon1020_ReviewWordByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1020_MainTitleByName")
require("ActivityDungeon1020_ReviewWordByName")
require("CommonResource_CurrencyReturnByName")

function GetActivityDungeon1020_ActivityDungeonUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.MainTitle = GetActivityDungeon1020_MainTitleUis(ui:GetChild("MainTitle"))
  uis.PlotBtn = ui:GetChild("PlotBtn")
```

---

## Activty/a20/ActivityDungeon1020_ActivityDungeonWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1020_ActivityDungeonWindowUis
**Requires:**
- ActivityDungeon1020_ActivityDungeonByName
**Snippet:**
```lua
require("ActivityDungeon1020_ActivityDungeonByName")

function GetActivityDungeon1020_ActivityDungeonWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1020_ActivityDungeonUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_AddBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_AddBtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_AddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_BossBattleByName.lua.lua
**Functions:**
- GetActivityDungeon1020_BossBattleUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1020_BossBattle_InfoByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1020_BossBattle_InfoByName")

function GetActivityDungeon1020_BossBattleUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.Info = GetActivityDungeon1020_BossBattle_InfoUis(ui:GetChild("Info"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a20/ActivityDungeon1020_BossBattleWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1020_BossBattleWindowUis
**Requires:**
- ActivityDungeon1020_BossBattleByName
**Snippet:**
```lua
require("ActivityDungeon1020_BossBattleByName")

function GetActivityDungeon1020_BossBattleWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1020_BossBattleUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_BossBattle_Info1ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_BossBattle_Info1Uis
**Snippet:**
```lua
function GetActivityDungeon1020_BossBattle_Info1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_BossBattle_InfoByName.lua.lua
**Functions:**
- GetActivityDungeon1020_BossBattle_InfoUis
**Requires:**
- ActivityDungeon1020_BossBattle_Info1ByName
**Snippet:**
```lua
require("ActivityDungeon1020_BossBattle_Info1ByName")

function GetActivityDungeon1020_BossBattle_InfoUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = GetActivityDungeon1020_BossBattle_Info1Uis(ui:GetChild("WordTxt"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_BossBattle_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1020_BossBattle_TipsAniUis
**Requires:**
- ActivityDungeon1020_BossBattle_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1020_BossBattle_TipsByName")

function GetActivityDungeon1020_BossBattle_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1020_BossBattle_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_BossBattle_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1020_BossBattle_TipsUis
**Requires:**
- ActivityDungeon1020_BossBattle_TipsRewardByName
**Snippet:**
```lua
require("ActivityDungeon1020_BossBattle_TipsRewardByName")

function GetActivityDungeon1020_BossBattle_TipsUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1020_BossBattle_TipsRewardUis(ui:GetChild("Reward"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.NumberWordTxt = ui:GetChild("NumberWordTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a20/ActivityDungeon1020_BossBattle_TipsRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1020_BossBattle_TipsRewardUis
**Snippet:**
```lua
function GetActivityDungeon1020_BossBattle_TipsRewardUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_BossBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_BossBtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_BossBtnUis(ui)
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

## Activty/a20/ActivityDungeon1020_BuyLevelBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_BuyLevelBtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_BuyLevelBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_BuyLevelDes1ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_BuyLevelDes1Uis
**Requires:**
- ActivityDungeon1020_NumberStripByName
- ActivityDungeon1020_BuyPriceNumberByName
**Snippet:**
```lua
require("ActivityDungeon1020_NumberStripByName")
require("ActivityDungeon1020_BuyPriceNumberByName")

function GetActivityDungeon1020_BuyLevelDes1Uis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.NumberStrip = GetActivityDungeon1020_NumberStripUis(ui:GetChild("NumberStrip"))
  uis.BuyPriceNumber = GetActivityDungeon1020_BuyPriceNumberUis(ui:GetChild("BuyPriceNumber"))
```

---

## Activty/a20/ActivityDungeon1020_BuyLevelDes2ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_BuyLevelDes2Uis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1020_BuyLevelDes1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1020_BuyLevelDes1ByName")

function GetActivityDungeon1020_BuyLevelDes2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.BuyLevelDes1 = GetActivityDungeon1020_BuyLevelDes1Uis(ui:GetChild("BuyLevelDes1"))
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.root = ui
```

---

## Activty/a20/ActivityDungeon1020_BuyLevelDesWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1020_BuyLevelDesWindowUis
**Requires:**
- ActivityDungeon1020_BuyLevelDes2ByName
**Snippet:**
```lua
require("ActivityDungeon1020_BuyLevelDes2ByName")

function GetActivityDungeon1020_BuyLevelDesWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1020_BuyLevelDes2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_BuyLevelItemByName.lua.lua
**Functions:**
- GetActivityDungeon1020_BuyLevelItemUis
**Requires:**
- ActivityDungeon1020_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1020_PassReward_AllFrame_EByName")

function GetActivityDungeon1020_BuyLevelItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1020_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_BuyPriceNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1020_BuyPriceNumberUis
**Snippet:**
```lua
function GetActivityDungeon1020_BuyPriceNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_ChallengeByName.lua.lua
**Functions:**
- GetActivityDungeon1020_ChallengeUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1020_MapListByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1020_MapListByName")

function GetActivityDungeon1020_ChallengeUis(ui)
  local uis = {}
  uis.BgList = ui:GetChild("BgList")
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Map = GetActivityDungeon1020_MapListUis(ui:GetChild("Map"))
  uis.ShopBtn = ui:GetChild("ShopBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a20/ActivityDungeon1020_ChallengeChapterBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_ChallengeChapterBtnUis
**Requires:**
- ActivityDungeon1020_NormalPointLockByName
**Snippet:**
```lua
require("ActivityDungeon1020_NormalPointLockByName")

function GetActivityDungeon1020_ChallengeChapterBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Lock = GetActivityDungeon1020_NormalPointLockUis(ui:GetChild("Lock"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Activty/a20/ActivityDungeon1020_ChallengeShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_ChallengeShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_ChallengeShopBtnUis(ui)
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

## Activty/a20/ActivityDungeon1020_ChallengeWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1020_ChallengeWindowUis
**Requires:**
- ActivityDungeon1020_ChallengeByName
**Snippet:**
```lua
require("ActivityDungeon1020_ChallengeByName")

function GetActivityDungeon1020_ChallengeWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1020_ChallengeUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MainTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MainTitleUis
**Snippet:**
```lua
function GetActivityDungeon1020_MainTitleUis(ui)
  local uis = {}
  
  uis.Time1Txt = ui:GetChild("Time1Txt")
  uis.Time2Txt = ui:GetChild("Time2Txt")
  uis.reviewCtr = ui:GetController("review")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MapBottom_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MapBottom_1Uis
**Snippet:**
```lua
function GetActivityDungeon1020_MapBottom_1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MapBottom_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MapBottom_2Uis
**Snippet:**
```lua
function GetActivityDungeon1020_MapBottom_2Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MapListByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MapListUis
**Snippet:**
```lua
function GetActivityDungeon1020_MapListUis(ui)
  local uis = {}
  
  uis.MapList = ui:GetChild("MapList")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Map_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Map_1Uis
**Snippet:**
```lua
function GetActivityDungeon1020_Map_1Uis(ui)
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

## Activty/a20/ActivityDungeon1020_Map_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Map_2Uis
**Snippet:**
```lua
function GetActivityDungeon1020_Map_2Uis(ui)
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

## Activty/a20/ActivityDungeon1020_MaterialBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MaterialBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1020_MaterialBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
```

---

## Activty/a20/ActivityDungeon1020_MaterialByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MaterialUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1020_Material_BattleNumberByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1020_Material_BattleNumberByName")

function GetActivityDungeon1020_MaterialUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.BattleNumber = GetActivityDungeon1020_Material_BattleNumberUis(ui:GetChild("BattleNumber"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a20/ActivityDungeon1020_MaterialWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MaterialWindowUis
**Requires:**
- ActivityDungeon1020_MaterialByName
**Snippet:**
```lua
require("ActivityDungeon1020_MaterialByName")

function GetActivityDungeon1020_MaterialWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1020_MaterialUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Material_BattleAniByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Material_BattleAniUis
**Requires:**
- ActivityDungeon1020_Material_BattleByName
**Snippet:**
```lua
require("ActivityDungeon1020_Material_BattleByName")

function GetActivityDungeon1020_Material_BattleAniUis(ui)
  local uis = {}
  uis.Battle = GetActivityDungeon1020_Material_BattleUis(ui:GetChild("Battle"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Material_BattleByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Material_BattleUis
**Snippet:**
```lua
function GetActivityDungeon1020_Material_BattleUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Material_BattleNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Material_BattleNumberUis
**Snippet:**
```lua
function GetActivityDungeon1020_Material_BattleNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MaxBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MaxBtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_MaxBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MinBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MinBtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_MinBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniGameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniGameBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1020_MiniGameBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniGameByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniGameUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1020_MiniMain_TopByName
- ActivityDungeon1020_MiniMain_BottonByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1020_MiniMain_TopByName")
require("ActivityDungeon1020_MiniMain_BottonByName")

function GetActivityDungeon1020_MiniGameUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Top = GetActivityDungeon1020_MiniMain_TopUis(ui:GetChild("Top"))
  uis.Botton = GetActivityDungeon1020_MiniMain_BottonUis(ui:GetChild("Botton"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a20/ActivityDungeon1020_MiniGameStartByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniGameStartUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1020_MiniStart_OperateRegionByName
- ActivityDungeon1020_MiniStart_IntegralByName
- ActivityDungeon1020_MiniStart_PreviewByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1020_MiniStart_OperateRegionByName")
require("ActivityDungeon1020_MiniStart_IntegralByName")
require("ActivityDungeon1020_MiniStart_PreviewByName")

function GetActivityDungeon1020_MiniGameStartUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.OperateRegion = GetActivityDungeon1020_MiniStart_OperateRegionUis(ui:GetChild("OperateRegion"))
  uis.Integral = GetActivityDungeon1020_MiniStart_IntegralUis(ui:GetChild("Integral"))
```

---

## Activty/a20/ActivityDungeon1020_MiniGameStartWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniGameStartWindowUis
**Requires:**
- ActivityDungeon1020_MiniGameStartByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniGameStartByName")

function GetActivityDungeon1020_MiniGameStartWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1020_MiniGameStartUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniGameWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniGameWindowUis
**Requires:**
- ActivityDungeon1020_MiniGameByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniGameByName")

function GetActivityDungeon1020_MiniGameWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1020_MiniGameUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniMain_BottonByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniMain_BottonUis
**Requires:**
- ActivityDungeon1020_MiniMain_TodayTaskByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniMain_TodayTaskByName")

function GetActivityDungeon1020_MiniMain_BottonUis(ui)
  local uis = {}
  uis.TaskBtn = ui:GetChild("TaskBtn")
  uis.TodayTask = GetActivityDungeon1020_MiniMain_TodayTaskUis(ui:GetChild("TodayTask"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniMain_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniMain_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1020_MiniMain_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniMain_RecordBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniMain_RecordBtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_MiniMain_RecordBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniMain_StartBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniMain_StartBtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_MiniMain_StartBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniMain_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniMain_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1020_MiniMain_TaskBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniMain_TodayTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniMain_TodayTaskUis
**Requires:**
- ActivityDungeon1020_PassReward_AllFrame_EByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("ActivityDungeon1020_PassReward_AllFrame_EByName")
require("CommonResource_RedDotByName")

function GetActivityDungeon1020_MiniMain_TodayTaskUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1020_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a20/ActivityDungeon1020_MiniMain_TopByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniMain_TopUis
**Requires:**
- ActivityDungeon1020_MiniMain_IntegralByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniMain_IntegralByName")

function GetActivityDungeon1020_MiniMain_TopUis(ui)
  local uis = {}
  uis.Integral = GetActivityDungeon1020_MiniMain_IntegralUis(ui:GetChild("Integral"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block01ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block01Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block01Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.root = ui
  return uis
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block02ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block02Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block02Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.root = ui
  return uis
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block03ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block03Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block03Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.root = ui
  return uis
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block04ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block04Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block04Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.root = ui
  return uis
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block05ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block05Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block05Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.root = ui
  return uis
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block06ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block06Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block06Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.B5 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B5"))
  uis.root = ui
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block07ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block07Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block07Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.B5 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B5"))
  uis.root = ui
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block08ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block08Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block08Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.B5 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B5"))
  uis.root = ui
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block09ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block09Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block09Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.B5 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B5"))
  uis.root = ui
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block10ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block10Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block10Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.root = ui
  return uis
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block11ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block11Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block11Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.root = ui
  return uis
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block12ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block12Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block12Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.root = ui
  return uis
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block13ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block13Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block13Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.root = ui
  return uis
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block14ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block14Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block14Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.root = ui
  return uis
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block15ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block15Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block15Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.root = ui
  return uis
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block16ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block16Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block16Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.root = ui
  return uis
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block17ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block17Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block17Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.root = ui
  return uis
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block18ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block18Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block18Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block19ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block19Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block19Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block20ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block20Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block20Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block21ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block21Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block21Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block22ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block22Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block22Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.root = ui
  return uis
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block23ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block23Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block23Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.root = ui
  return uis
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block24ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block24Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block24Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.root = ui
  return uis
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block25ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block25Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block25Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.root = ui
  return uis
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block26ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block26Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block26Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.B5 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B5"))
  uis.root = ui
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block27ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block27Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block27Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.B5 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B5"))
  uis.root = ui
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block28ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block28Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block28Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.root = ui
  return uis
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block29ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block29Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block29Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.root = ui
  return uis
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block30ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block30Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block30Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block31ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block31Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block31Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block32ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block32Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block32Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block33ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block33Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block33Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block34ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block34Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block34Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block35ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block35Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block35Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.B5 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B5"))
  uis.B6 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B6"))
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_Block36ByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_Block36Uis
**Requires:**
- ActivityDungeon1020_MiniStart_BlockByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_BlockByName")

function GetActivityDungeon1020_MiniStart_Block36Uis(ui)
  local uis = {}
  uis.B1 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B1"))
  uis.B2 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B2"))
  uis.B3 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B3"))
  uis.B4 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B4"))
  uis.B5 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B5"))
  uis.B6 = GetActivityDungeon1020_MiniStart_BlockUis(ui:GetChild("B6"))
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_BlockByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_BlockUis
**Snippet:**
```lua
function GetActivityDungeon1020_MiniStart_BlockUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.numberCtr = ui:GetController("number")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_CloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_CloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_MiniStart_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_EndAgainBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_EndAgainBtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_MiniStart_EndAgainBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_EndCloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_EndCloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_MiniStart_EndCloseBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_EndRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_EndRewardUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1020_MiniStart_WinByName
- ActivityDungeon1020_MiniStart_FailByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1020_MiniStart_WinByName")
require("ActivityDungeon1020_MiniStart_FailByName")

function GetActivityDungeon1020_MiniStart_EndRewardUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.Win = GetActivityDungeon1020_MiniStart_WinUis(ui:GetChild("Win"))
  uis.Fail = GetActivityDungeon1020_MiniStart_FailUis(ui:GetChild("Fail"))
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_EndRewardWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_EndRewardWindowUis
**Requires:**
- ActivityDungeon1020_MiniStart_EndRewardByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_EndRewardByName")

function GetActivityDungeon1020_MiniStart_EndRewardWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1020_MiniStart_EndRewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_FailByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_FailUis
**Snippet:**
```lua
function GetActivityDungeon1020_MiniStart_FailUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_GuGuByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_GuGuUis
**Requires:**
- ActivityDungeon1020_MiniStart_GuGuNumberByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_GuGuNumberByName")

function GetActivityDungeon1020_MiniStart_GuGuUis(ui)
  local uis = {}
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.Left = GetActivityDungeon1020_MiniStart_GuGuNumberUis(ui:GetChild("Left"))
  uis.Right = GetActivityDungeon1020_MiniStart_GuGuNumberUis(ui:GetChild("Right"))
  uis.numberCtr = ui:GetController("number")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_GuGuNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_GuGuNumberUis
**Snippet:**
```lua
function GetActivityDungeon1020_MiniStart_GuGuNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_GuGuPositionByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_GuGuPositionUis
**Snippet:**
```lua
function GetActivityDungeon1020_MiniStart_GuGuPositionUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_InitialPositionByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_InitialPositionUis
**Snippet:**
```lua
function GetActivityDungeon1020_MiniStart_InitialPositionUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1020_MiniStart_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_OperateRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_OperateRegionUis
**Requires:**
- ActivityDungeon1020_MiniStart_InitialPositionByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_InitialPositionByName")

function GetActivityDungeon1020_MiniStart_OperateRegionUis(ui)
  local uis = {}
  uis.P01 = GetActivityDungeon1020_MiniStart_InitialPositionUis(ui:GetChild("P01"))
  uis.P02 = GetActivityDungeon1020_MiniStart_InitialPositionUis(ui:GetChild("P02"))
  uis.P03 = GetActivityDungeon1020_MiniStart_InitialPositionUis(ui:GetChild("P03"))
  uis.P04 = GetActivityDungeon1020_MiniStart_InitialPositionUis(ui:GetChild("P04"))
  uis.P05 = GetActivityDungeon1020_MiniStart_InitialPositionUis(ui:GetChild("P05"))
  uis.P06 = GetActivityDungeon1020_MiniStart_InitialPositionUis(ui:GetChild("P06"))
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_PreviewByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_PreviewUis
**Snippet:**
```lua
function GetActivityDungeon1020_MiniStart_PreviewUis(ui)
  local uis = {}
  
  uis.Preview1Loader = ui:GetChild("Preview1Loader")
  uis.Preview2Loader = ui:GetChild("Preview2Loader")
  uis.Preview3Loader = ui:GetChild("Preview3Loader")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_PreviewItemByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_PreviewItemUis
**Snippet:**
```lua
function GetActivityDungeon1020_MiniStart_PreviewItemUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_SwitchBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_SwitchBtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_MiniStart_SwitchBtnUis(ui)
  local uis = {}
  
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniStart_WinByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniStart_WinUis
**Snippet:**
```lua
function GetActivityDungeon1020_MiniStart_WinUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniTaskUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1020_MiniTask_IntegralByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1020_MiniTask_IntegralByName")

function GetActivityDungeon1020_MiniTaskUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Integral = GetActivityDungeon1020_MiniTask_IntegralUis(ui:GetChild("Integral"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a20/ActivityDungeon1020_MiniTaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniTaskWindowUis
**Requires:**
- ActivityDungeon1020_MiniTaskByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniTaskByName")

function GetActivityDungeon1020_MiniTaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1020_MiniTaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniTask_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniTask_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1020_MiniTask_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniTask_RewardItemByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniTask_RewardItemUis
**Snippet:**
```lua
function GetActivityDungeon1020_MiniTask_RewardItemUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniTask_RewardItemGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniTask_RewardItemGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_MiniTask_RewardItemGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniTask_TipsAniUis
**Requires:**
- ActivityDungeon1020_MiniTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniTask_TipsByName")

function GetActivityDungeon1020_MiniTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1020_MiniTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_MiniTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1020_MiniTask_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1020_MiniTask_TipsUis(ui)
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

## Activty/a20/ActivityDungeon1020_NormalBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_NormalBtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_NormalBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_NormalPoint1BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_NormalPoint1BtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_NormalPoint1BtnUis(ui)
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

## Activty/a20/ActivityDungeon1020_NormalPoint2BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_NormalPoint2BtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_NormalPoint2BtnUis(ui)
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

## Activty/a20/ActivityDungeon1020_NormalPointLockByName.lua.lua
**Functions:**
- GetActivityDungeon1020_NormalPointLockUis
**Snippet:**
```lua
function GetActivityDungeon1020_NormalPointLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_NumberStripByName.lua.lua
**Functions:**
- GetActivityDungeon1020_NumberStripUis
**Snippet:**
```lua
function GetActivityDungeon1020_NumberStripUis(ui)
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

## Activty/a20/ActivityDungeon1020_PassBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1020_PassBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_PassClothes_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassClothes_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_PassClothes_BuyBtnUis(ui)
  local uis = {}
  
  uis.PriceTxt = ui:GetChild("PriceTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_PassClothes_BuyRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassClothes_BuyRewardUis
**Snippet:**
```lua
function GetActivityDungeon1020_PassClothes_BuyRewardUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_PassClothes_CardQBByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassClothes_CardQBUis
**Snippet:**
```lua
function GetActivityDungeon1020_PassClothes_CardQBUis(ui)
  local uis = {}
  
  uis.QBHolder = ui:GetChild("QBHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_PassClothes_ClothseRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassClothes_ClothseRegionUis
**Requires:**
- ActivityDungeon1020_PassClothes_WordByName
- ActivityDungeon1020_PassClothes_CardQBByName
- ActivityDungeon1020_PassClothes_BuyRewardByName
**Snippet:**
```lua
require("ActivityDungeon1020_PassClothes_WordByName")
require("ActivityDungeon1020_PassClothes_CardQBByName")
require("ActivityDungeon1020_PassClothes_BuyRewardByName")

function GetActivityDungeon1020_PassClothes_ClothseRegionUis(ui)
  local uis = {}
  uis.Word = GetActivityDungeon1020_PassClothes_WordUis(ui:GetChild("Word"))
  uis.CardQB = GetActivityDungeon1020_PassClothes_CardQBUis(ui:GetChild("CardQB"))
  uis.BuyReward = GetActivityDungeon1020_PassClothes_BuyRewardUis(ui:GetChild("BuyReward"))
  uis.BuyBtn = ui:GetChild("BuyBtn")
```

---

## Activty/a20/ActivityDungeon1020_PassClothes_NameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassClothes_NameBtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_PassClothes_NameBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_PassClothes_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassClothes_WordUis
**Snippet:**
```lua
function GetActivityDungeon1020_PassClothes_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_PassportByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassportUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1020_PassReward_RewardRegionByName
- ActivityDungeon1020_PassTask_TaskRegionByName
- ActivityDungeon1020_PassClothes_ClothseRegionByName
- ActivityDungeon1020_Passport_LevelByName
- ActivityDungeon1020_Sign_TimeByName
- ActivityDungeon1020_Passport_TabRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1020_PassReward_RewardRegionByName")
require("ActivityDungeon1020_PassTask_TaskRegionByName")
require("ActivityDungeon1020_PassClothes_ClothseRegionByName")
require("ActivityDungeon1020_Passport_LevelByName")
require("ActivityDungeon1020_Sign_TimeByName")
require("ActivityDungeon1020_Passport_TabRegionByName")

function GetActivityDungeon1020_PassportUis(ui)
  local uis = {}
```

---

## Activty/a20/ActivityDungeon1020_PassportUp_LevelUpBgByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassportUp_LevelUpBgUis
**Snippet:**
```lua
function GetActivityDungeon1020_PassportUp_LevelUpBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_PassportUp_LevelUpTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassportUp_LevelUpTipsUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1020_PassportUp_LevelUpBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1020_PassportUp_LevelUpBgByName")

function GetActivityDungeon1020_PassportUp_LevelUpTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.LevelUpBg = GetActivityDungeon1020_PassportUp_LevelUpBgUis(ui:GetChild("LevelUpBg"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
```

---

## Activty/a20/ActivityDungeon1020_PassportUp_LevelUpTipsWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassportUp_LevelUpTipsWindowUis
**Requires:**
- ActivityDungeon1020_PassportUp_LevelUpTipsByName
**Snippet:**
```lua
require("ActivityDungeon1020_PassportUp_LevelUpTipsByName")

function GetActivityDungeon1020_PassportUp_LevelUpTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1020_PassportUp_LevelUpTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_PassportWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassportWindowUis
**Requires:**
- ActivityDungeon1020_PassportByName
**Snippet:**
```lua
require("ActivityDungeon1020_PassportByName")

function GetActivityDungeon1020_PassportWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1020_PassportUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Passport_AllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Passport_AllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_Passport_AllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Passport_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Passport_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_Passport_BuyBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Passport_ExpProgressBarByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Passport_ExpProgressBarUis
**Requires:**
- ActivityDungeon1020_Passport_ExpProgressFillByName
**Snippet:**
```lua
require("ActivityDungeon1020_Passport_ExpProgressFillByName")

function GetActivityDungeon1020_Passport_ExpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetActivityDungeon1020_Passport_ExpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Passport_ExpProgressFillByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Passport_ExpProgressFillUis
**Snippet:**
```lua
function GetActivityDungeon1020_Passport_ExpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Passport_LevelByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Passport_LevelUis
**Snippet:**
```lua
function GetActivityDungeon1020_Passport_LevelUis(ui)
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

## Activty/a20/ActivityDungeon1020_Passport_TabBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Passport_TabBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1020_Passport_TabBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## Activty/a20/ActivityDungeon1020_Passport_TabRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Passport_TabRegionUis
**Snippet:**
```lua
function GetActivityDungeon1020_Passport_TabRegionUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_PassReward_AllFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassReward_AllFrame_EUis
**Requires:**
- ActivityDungeon1020_PassReward_ItemFrame_EByName
- ActivityDungeon1020_PassReward_CardFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1020_PassReward_ItemFrame_EByName")
require("ActivityDungeon1020_PassReward_CardFrame_EByName")

function GetActivityDungeon1020_PassReward_AllFrame_EUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1020_PassReward_ItemFrame_EUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1020_PassReward_CardFrame_EUis(ui:GetChild("CardFrame"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## Activty/a20/ActivityDungeon1020_PassReward_AllFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassReward_AllFrame_MUis
**Requires:**
- ActivityDungeon1020_PassReward_ItemFrame_MByName
- ActivityDungeon1020_PassReward_CardFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1020_PassReward_ItemFrame_MByName")
require("ActivityDungeon1020_PassReward_CardFrame_MByName")

function GetActivityDungeon1020_PassReward_AllFrame_MUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1020_PassReward_ItemFrame_MUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1020_PassReward_CardFrame_MUis(ui:GetChild("CardFrame"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a20/ActivityDungeon1020_PassReward_CardFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassReward_CardFrame_EUis
**Requires:**
- ActivityDungeon1020_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1020_PassReward_ItemCardPicByName")

function GetActivityDungeon1020_PassReward_CardFrame_EUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1020_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a20/ActivityDungeon1020_PassReward_CardFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassReward_CardFrame_MUis
**Requires:**
- ActivityDungeon1020_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1020_PassReward_ItemCardPicByName")

function GetActivityDungeon1020_PassReward_CardFrame_MUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1020_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a20/ActivityDungeon1020_PassReward_EndTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassReward_EndTwoUis
**Requires:**
- ActivityDungeon1020_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1020_PassReward_AllFrame_EByName")

function GetActivityDungeon1020_PassReward_EndTwoUis(ui)
  local uis = {}
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.Item1 = GetActivityDungeon1020_PassReward_AllFrame_EUis(ui:GetChild("Item1"))
  uis.Item2 = GetActivityDungeon1020_PassReward_AllFrame_EUis(ui:GetChild("Item2"))
  uis.root = ui
```

---

## Activty/a20/ActivityDungeon1020_PassReward_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassReward_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1020_PassReward_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_PassReward_ItemFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassReward_ItemFrame_EUis
**Snippet:**
```lua
function GetActivityDungeon1020_PassReward_ItemFrame_EUis(ui)
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

## Activty/a20/ActivityDungeon1020_PassReward_ItemFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassReward_ItemFrame_MUis
**Snippet:**
```lua
function GetActivityDungeon1020_PassReward_ItemFrame_MUis(ui)
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

## Activty/a20/ActivityDungeon1020_PassReward_LevelTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassReward_LevelTitleUis
**Snippet:**
```lua
function GetActivityDungeon1020_PassReward_LevelTitleUis(ui)
  local uis = {}
  
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_PassReward_MiddleRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassReward_MiddleRegionUis
**Snippet:**
```lua
function GetActivityDungeon1020_PassReward_MiddleRegionUis(ui)
  local uis = {}
  
  uis.MiddleList = ui:GetChild("MiddleList")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_PassReward_MidTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassReward_MidTwoUis
**Requires:**
- ActivityDungeon1020_PassReward_MidTwoItemByName
- ActivityDungeon1020_PassReward_LevelTitleByName
**Snippet:**
```lua
require("ActivityDungeon1020_PassReward_MidTwoItemByName")
require("ActivityDungeon1020_PassReward_LevelTitleByName")

function GetActivityDungeon1020_PassReward_MidTwoUis(ui)
  local uis = {}
  uis.Reward1 = GetActivityDungeon1020_PassReward_MidTwoItemUis(ui:GetChild("Reward1"))
  uis.Reward2 = GetActivityDungeon1020_PassReward_MidTwoItemUis(ui:GetChild("Reward2"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Title = GetActivityDungeon1020_PassReward_LevelTitleUis(ui:GetChild("Title"))
```

---

## Activty/a20/ActivityDungeon1020_PassReward_MidTwoItemByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassReward_MidTwoItemUis
**Requires:**
- ActivityDungeon1020_PassReward_AllFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1020_PassReward_AllFrame_MByName")

function GetActivityDungeon1020_PassReward_MidTwoItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1020_PassReward_AllFrame_MUis(ui:GetChild("Item"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_PassReward_PicByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassReward_PicUis
**Snippet:**
```lua
function GetActivityDungeon1020_PassReward_PicUis(ui)
  local uis = {}
  
  uis.BuyTxt = ui:GetChild("BuyTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_PassReward_RewardRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassReward_RewardRegionUis
**Requires:**
- ActivityDungeon1020_PassReward_MiddleRegionByName
- ActivityDungeon1020_PassReward_StartTwoByName
- ActivityDungeon1020_PassReward_EndTwoByName
**Snippet:**
```lua
require("ActivityDungeon1020_PassReward_MiddleRegionByName")
require("ActivityDungeon1020_PassReward_StartTwoByName")
require("ActivityDungeon1020_PassReward_EndTwoByName")

function GetActivityDungeon1020_PassReward_RewardRegionUis(ui)
  local uis = {}
  uis.MiddleList = GetActivityDungeon1020_PassReward_MiddleRegionUis(ui:GetChild("MiddleList"))
  uis.StartTwo = GetActivityDungeon1020_PassReward_StartTwoUis(ui:GetChild("StartTwo"))
  uis.EndTwo = GetActivityDungeon1020_PassReward_EndTwoUis(ui:GetChild("EndTwo"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a20/ActivityDungeon1020_PassReward_StartTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassReward_StartTwoUis
**Requires:**
- ActivityDungeon1020_PassReward_PicByName
**Snippet:**
```lua
require("ActivityDungeon1020_PassReward_PicByName")

function GetActivityDungeon1020_PassReward_StartTwoUis(ui)
  local uis = {}
  uis.Pic = GetActivityDungeon1020_PassReward_PicUis(ui:GetChild("Pic"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_PassTask_TaskRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassTask_TaskRegionUis
**Requires:**
- ActivityDungeon1020_TaskMaxByName
**Snippet:**
```lua
require("ActivityDungeon1020_TaskMaxByName")

function GetActivityDungeon1020_PassTask_TaskRegionUis(ui)
  local uis = {}
  uis.TipsList = ui:GetChild("TipsList")
  uis.Max = GetActivityDungeon1020_TaskMaxUis(ui:GetChild("Max"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_PassTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassTask_TipsAniUis
**Requires:**
- ActivityDungeon1020_PassTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1020_PassTask_TipsByName")

function GetActivityDungeon1020_PassTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1020_PassTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_PassTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassTask_TipsUis
**Requires:**
- ActivityDungeon1020_PassTask_TipsIntegralByName
**Snippet:**
```lua
require("ActivityDungeon1020_PassTask_TipsIntegralByName")

function GetActivityDungeon1020_PassTask_TipsUis(ui)
  local uis = {}
  uis.ProgressTxt = ui:GetChild("ProgressTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Integral = GetActivityDungeon1020_PassTask_TipsIntegralUis(ui:GetChild("Integral"))
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a20/ActivityDungeon1020_PassTask_TipsIntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PassTask_TipsIntegralUis
**Snippet:**
```lua
function GetActivityDungeon1020_PassTask_TipsIntegralUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_PlotBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PlotBtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_PlotBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_PlotByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PlotUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1020_Plot_WordByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1020_Plot_WordByName")

function GetActivityDungeon1020_PlotUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Word = GetActivityDungeon1020_Plot_WordUis(ui:GetChild("Word"))
  uis.PlotList = ui:GetChild("PlotList")
  uis.ProspectBtn = ui:GetChild("ProspectBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a20/ActivityDungeon1020_PlotWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1020_PlotWindowUis
**Requires:**
- ActivityDungeon1020_PlotByName
**Snippet:**
```lua
require("ActivityDungeon1020_PlotByName")

function GetActivityDungeon1020_PlotWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1020_PlotUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Plot_ProspectBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Plot_ProspectBtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_Plot_ProspectBtnUis(ui)
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

## Activty/a20/ActivityDungeon1020_Plot_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Plot_TipsAniUis
**Requires:**
- ActivityDungeon1020_Plot_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1020_Plot_TipsByName")

function GetActivityDungeon1020_Plot_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1020_Plot_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Plot_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Plot_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1020_Plot_TipsUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Plot_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Plot_WordUis
**Snippet:**
```lua
function GetActivityDungeon1020_Plot_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_ReduceBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_ReduceBtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_ReduceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_ReviewWordByName.lua.lua
**Functions:**
- GetActivityDungeon1020_ReviewWordUis
**Snippet:**
```lua
function GetActivityDungeon1020_ReviewWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_ShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_ShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_ShopBtnUis(ui)
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

## Activty/a20/ActivityDungeon1020_ShopByName.lua.lua
**Functions:**
- GetActivityDungeon1020_ShopUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1020_Shop_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1020_Shop_TimeByName")

function GetActivityDungeon1020_ShopUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Time = GetActivityDungeon1020_Shop_TimeUis(ui:GetChild("Time"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a20/ActivityDungeon1020_ShopWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1020_ShopWindowUis
**Requires:**
- ActivityDungeon1020_ShopByName
**Snippet:**
```lua
require("ActivityDungeon1020_ShopByName")

function GetActivityDungeon1020_ShopWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1020_ShopUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Shop_CardHeadBgByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Shop_CardHeadBgUis
**Snippet:**
```lua
function GetActivityDungeon1020_Shop_CardHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Shop_ItemAniByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Shop_ItemAniUis
**Requires:**
- ActivityDungeon1020_Shop_ItemByName
**Snippet:**
```lua
require("ActivityDungeon1020_Shop_ItemByName")

function GetActivityDungeon1020_Shop_ItemAniUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1020_Shop_ItemUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Shop_ItemBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Shop_ItemBtnUis
**Requires:**
- ActivityDungeon1020_Shop_CardHeadBgByName
- ActivityDungeon1020_Shop_ItemNumberByName
- ActivityDungeon1020_Shop_UseMarkByName
**Snippet:**
```lua
require("ActivityDungeon1020_Shop_CardHeadBgByName")
require("ActivityDungeon1020_Shop_ItemNumberByName")
require("ActivityDungeon1020_Shop_UseMarkByName")

function GetActivityDungeon1020_Shop_ItemBtnUis(ui)
  local uis = {}
  uis.CardHeadBg = GetActivityDungeon1020_Shop_CardHeadBgUis(ui:GetChild("CardHeadBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.ItemNumber = GetActivityDungeon1020_Shop_ItemNumberUis(ui:GetChild("ItemNumber"))
```

---

## Activty/a20/ActivityDungeon1020_Shop_ItemByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Shop_ItemUis
**Requires:**
- ActivityDungeon1020_Shop_SellOutByName
**Snippet:**
```lua
require("ActivityDungeon1020_Shop_SellOutByName")

function GetActivityDungeon1020_Shop_ItemUis(ui)
  local uis = {}
  uis.ItemBtn = ui:GetChild("ItemBtn")
  uis.SellOut = GetActivityDungeon1020_Shop_SellOutUis(ui:GetChild("SellOut"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Shop_ItemNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Shop_ItemNumberUis
**Snippet:**
```lua
function GetActivityDungeon1020_Shop_ItemNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Shop_ItemRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Shop_ItemRegionUis
**Requires:**
- ActivityDungeon1020_Shop_TitleByName
**Snippet:**
```lua
require("ActivityDungeon1020_Shop_TitleByName")

function GetActivityDungeon1020_Shop_ItemRegionUis(ui)
  local uis = {}
  uis.ShopTitle = GetActivityDungeon1020_Shop_TitleUis(ui:GetChild("ShopTitle"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Shop_SellOutByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Shop_SellOutUis
**Snippet:**
```lua
function GetActivityDungeon1020_Shop_SellOutUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Shop_StarByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Shop_StarUis
**Snippet:**
```lua
function GetActivityDungeon1020_Shop_StarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Shop_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Shop_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1020_Shop_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Shop_TitleByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Shop_TitleUis
**Snippet:**
```lua
function GetActivityDungeon1020_Shop_TitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Shop_UseMarkByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Shop_UseMarkUis
**Snippet:**
```lua
function GetActivityDungeon1020_Shop_UseMarkUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_SignBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_SignBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1020_SignBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_SignByName.lua.lua
**Functions:**
- GetActivityDungeon1020_SignUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1020_Sign_RewardListByName
- ActivityDungeon1020_Sign_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1020_Sign_RewardListByName")
require("ActivityDungeon1020_Sign_TimeByName")

function GetActivityDungeon1020_SignUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.RewardList = GetActivityDungeon1020_Sign_RewardListUis(ui:GetChild("RewardList"))
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.Time = GetActivityDungeon1020_Sign_TimeUis(ui:GetChild("Time"))
```

---

## Activty/a20/ActivityDungeon1020_SignWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1020_SignWindowUis
**Requires:**
- ActivityDungeon1020_SignByName
**Snippet:**
```lua
require("ActivityDungeon1020_SignByName")

function GetActivityDungeon1020_SignWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1020_SignUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Sign_AllFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Sign_AllFrameUis
**Requires:**
- ActivityDungeon1020_Sign_ItemFrameByName
- ActivityDungeon1020_Sign_CardFrameByName
**Snippet:**
```lua
require("ActivityDungeon1020_Sign_ItemFrameByName")
require("ActivityDungeon1020_Sign_CardFrameByName")

function GetActivityDungeon1020_Sign_AllFrameUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1020_Sign_ItemFrameUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1020_Sign_CardFrameUis(ui:GetChild("CardFrame"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a20/ActivityDungeon1020_Sign_CardFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Sign_CardFrameUis
**Requires:**
- ActivityDungeon1020_Sign_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1020_Sign_ItemCardPicByName")

function GetActivityDungeon1020_Sign_CardFrameUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1020_Sign_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a20/ActivityDungeon1020_Sign_GetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Sign_GetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_Sign_GetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Sign_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Sign_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1020_Sign_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Sign_ItemFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Sign_ItemFrameUis
**Snippet:**
```lua
function GetActivityDungeon1020_Sign_ItemFrameUis(ui)
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

## Activty/a20/ActivityDungeon1020_Sign_RewardAniByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Sign_RewardAniUis
**Requires:**
- ActivityDungeon1020_Sign_RewardByName
**Snippet:**
```lua
require("ActivityDungeon1020_Sign_RewardByName")

function GetActivityDungeon1020_Sign_RewardAniUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1020_Sign_RewardUis(ui:GetChild("Reward"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Sign_RewardByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Sign_RewardUis
**Requires:**
- ActivityDungeon1020_Sign_AllFrameByName
**Snippet:**
```lua
require("ActivityDungeon1020_Sign_AllFrameByName")

function GetActivityDungeon1020_Sign_RewardUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1020_Sign_AllFrameUis(ui:GetChild("Item"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Sign_RewardListByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Sign_RewardListUis
**Snippet:**
```lua
function GetActivityDungeon1020_Sign_RewardListUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_Sign_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1020_Sign_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1020_Sign_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_TaskAllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_TaskAllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_TaskAllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1020_TaskBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_TaskByName.lua.lua
**Functions:**
- GetActivityDungeon1020_TaskUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1020_TaskTitleByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1020_TaskTitleByName")

function GetActivityDungeon1020_TaskUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TaskTitle = GetActivityDungeon1020_TaskTitleUis(ui:GetChild("TaskTitle"))
  uis.TaskTipsList = ui:GetChild("TaskTipsList")
  uis.AllGetBtn = ui:GetChild("AllGetBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a20/ActivityDungeon1020_TaskGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1020_TaskGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1020_TaskGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_TaskMaxByName.lua.lua
**Functions:**
- GetActivityDungeon1020_TaskMaxUis
**Snippet:**
```lua
function GetActivityDungeon1020_TaskMaxUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_TaskProgressByName.lua.lua
**Functions:**
- GetActivityDungeon1020_TaskProgressUis
**Snippet:**
```lua
function GetActivityDungeon1020_TaskProgressUis(ui)
  local uis = {}
  
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_TaskTipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1020_TaskTipsAniUis
**Requires:**
- ActivityDungeon1020_TaskTipsByName
**Snippet:**
```lua
require("ActivityDungeon1020_TaskTipsByName")

function GetActivityDungeon1020_TaskTipsAniUis(ui)
  local uis = {}
  uis.TaskTips = GetActivityDungeon1020_TaskTipsUis(ui:GetChild("TaskTips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_TaskTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1020_TaskTipsUis
**Requires:**
- ActivityDungeon1020_TaskProgressByName
**Snippet:**
```lua
require("ActivityDungeon1020_TaskProgressByName")

function GetActivityDungeon1020_TaskTipsUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.RewardList = ui:GetChild("RewardList")
  uis.TaskProgress = GetActivityDungeon1020_TaskProgressUis(ui:GetChild("TaskProgress"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a20/ActivityDungeon1020_TaskTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1020_TaskTitleUis
**Snippet:**
```lua
function GetActivityDungeon1020_TaskTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a20/ActivityDungeon1020_TaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1020_TaskWindowUis
**Requires:**
- ActivityDungeon1020_TaskByName
**Snippet:**
```lua
require("ActivityDungeon1020_TaskByName")

function GetActivityDungeon1020_TaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1020_TaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---
