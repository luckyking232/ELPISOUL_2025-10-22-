# Activty/a19

## Activty/a19/ActivityDungeon1019_ActivityDungeonByName.lua.lua
**Functions:**
- GetActivityDungeon1019_ActivityDungeonUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1019_MainTitleByName
- ActivityDungeon1019_ReviewWordByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1019_MainTitleByName")
require("ActivityDungeon1019_ReviewWordByName")
require("CommonResource_CurrencyReturnByName")

function GetActivityDungeon1019_ActivityDungeonUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.MainTitle = GetActivityDungeon1019_MainTitleUis(ui:GetChild("MainTitle"))
  uis.PlotBtn = ui:GetChild("PlotBtn")
```

---

## Activty/a19/ActivityDungeon1019_ActivityDungeonWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1019_ActivityDungeonWindowUis
**Requires:**
- ActivityDungeon1019_ActivityDungeonByName
**Snippet:**
```lua
require("ActivityDungeon1019_ActivityDungeonByName")

function GetActivityDungeon1019_ActivityDungeonWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1019_ActivityDungeonUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_AddBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_AddBtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_AddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_BossBattleByName.lua.lua
**Functions:**
- GetActivityDungeon1019_BossBattleUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1019_BossBattle_InfoByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1019_BossBattle_InfoByName")

function GetActivityDungeon1019_BossBattleUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.Info = GetActivityDungeon1019_BossBattle_InfoUis(ui:GetChild("Info"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a19/ActivityDungeon1019_BossBattleWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1019_BossBattleWindowUis
**Requires:**
- ActivityDungeon1019_BossBattleByName
**Snippet:**
```lua
require("ActivityDungeon1019_BossBattleByName")

function GetActivityDungeon1019_BossBattleWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1019_BossBattleUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_BossBattle_Info1ByName.lua.lua
**Functions:**
- GetActivityDungeon1019_BossBattle_Info1Uis
**Snippet:**
```lua
function GetActivityDungeon1019_BossBattle_Info1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_BossBattle_InfoByName.lua.lua
**Functions:**
- GetActivityDungeon1019_BossBattle_InfoUis
**Requires:**
- ActivityDungeon1019_BossBattle_Info1ByName
**Snippet:**
```lua
require("ActivityDungeon1019_BossBattle_Info1ByName")

function GetActivityDungeon1019_BossBattle_InfoUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = GetActivityDungeon1019_BossBattle_Info1Uis(ui:GetChild("WordTxt"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_BossBattle_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1019_BossBattle_TipsAniUis
**Requires:**
- ActivityDungeon1019_BossBattle_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1019_BossBattle_TipsByName")

function GetActivityDungeon1019_BossBattle_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1019_BossBattle_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_BossBattle_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1019_BossBattle_TipsUis
**Requires:**
- ActivityDungeon1019_BossBattle_TipsRewardByName
**Snippet:**
```lua
require("ActivityDungeon1019_BossBattle_TipsRewardByName")

function GetActivityDungeon1019_BossBattle_TipsUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1019_BossBattle_TipsRewardUis(ui:GetChild("Reward"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.NumberWordTxt = ui:GetChild("NumberWordTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a19/ActivityDungeon1019_BossBattle_TipsRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1019_BossBattle_TipsRewardUis
**Snippet:**
```lua
function GetActivityDungeon1019_BossBattle_TipsRewardUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_BossBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_BossBtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_BossBtnUis(ui)
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

## Activty/a19/ActivityDungeon1019_BuyLevelBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_BuyLevelBtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_BuyLevelBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_BuyLevelDes1ByName.lua.lua
**Functions:**
- GetActivityDungeon1019_BuyLevelDes1Uis
**Requires:**
- ActivityDungeon1019_NumberStripByName
- ActivityDungeon1019_BuyPriceNumberByName
**Snippet:**
```lua
require("ActivityDungeon1019_NumberStripByName")
require("ActivityDungeon1019_BuyPriceNumberByName")

function GetActivityDungeon1019_BuyLevelDes1Uis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.NumberStrip = GetActivityDungeon1019_NumberStripUis(ui:GetChild("NumberStrip"))
  uis.BuyPriceNumber = GetActivityDungeon1019_BuyPriceNumberUis(ui:GetChild("BuyPriceNumber"))
```

---

## Activty/a19/ActivityDungeon1019_BuyLevelDes2ByName.lua.lua
**Functions:**
- GetActivityDungeon1019_BuyLevelDes2Uis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1019_BuyLevelDes1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1019_BuyLevelDes1ByName")

function GetActivityDungeon1019_BuyLevelDes2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.BuyLevelDes1 = GetActivityDungeon1019_BuyLevelDes1Uis(ui:GetChild("BuyLevelDes1"))
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.root = ui
```

---

## Activty/a19/ActivityDungeon1019_BuyLevelDesWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1019_BuyLevelDesWindowUis
**Requires:**
- ActivityDungeon1019_BuyLevelDes2ByName
**Snippet:**
```lua
require("ActivityDungeon1019_BuyLevelDes2ByName")

function GetActivityDungeon1019_BuyLevelDesWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1019_BuyLevelDes2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_BuyLevelItemByName.lua.lua
**Functions:**
- GetActivityDungeon1019_BuyLevelItemUis
**Requires:**
- ActivityDungeon1019_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1019_PassReward_AllFrame_EByName")

function GetActivityDungeon1019_BuyLevelItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1019_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_BuyPriceNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1019_BuyPriceNumberUis
**Snippet:**
```lua
function GetActivityDungeon1019_BuyPriceNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_ChallengeByName.lua.lua
**Functions:**
- GetActivityDungeon1019_ChallengeUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1019_MapListByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1019_MapListByName")

function GetActivityDungeon1019_ChallengeUis(ui)
  local uis = {}
  uis.BgList = ui:GetChild("BgList")
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Map = GetActivityDungeon1019_MapListUis(ui:GetChild("Map"))
  uis.ShopBtn = ui:GetChild("ShopBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a19/ActivityDungeon1019_ChallengeChapterBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_ChallengeChapterBtnUis
**Requires:**
- ActivityDungeon1019_NormalPointLockByName
**Snippet:**
```lua
require("ActivityDungeon1019_NormalPointLockByName")

function GetActivityDungeon1019_ChallengeChapterBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Lock = GetActivityDungeon1019_NormalPointLockUis(ui:GetChild("Lock"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Activty/a19/ActivityDungeon1019_ChallengeShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_ChallengeShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_ChallengeShopBtnUis(ui)
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

## Activty/a19/ActivityDungeon1019_ChallengeWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1019_ChallengeWindowUis
**Requires:**
- ActivityDungeon1019_ChallengeByName
**Snippet:**
```lua
require("ActivityDungeon1019_ChallengeByName")

function GetActivityDungeon1019_ChallengeWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1019_ChallengeUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MainTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MainTitleUis
**Snippet:**
```lua
function GetActivityDungeon1019_MainTitleUis(ui)
  local uis = {}
  
  uis.Time1Txt = ui:GetChild("Time1Txt")
  uis.Time2Txt = ui:GetChild("Time2Txt")
  uis.reviewCtr = ui:GetController("review")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MapBottom_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MapBottom_1Uis
**Snippet:**
```lua
function GetActivityDungeon1019_MapBottom_1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MapBottom_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MapBottom_2Uis
**Snippet:**
```lua
function GetActivityDungeon1019_MapBottom_2Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MapListByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MapListUis
**Snippet:**
```lua
function GetActivityDungeon1019_MapListUis(ui)
  local uis = {}
  
  uis.MapList = ui:GetChild("MapList")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Map_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Map_1Uis
**Snippet:**
```lua
function GetActivityDungeon1019_Map_1Uis(ui)
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

## Activty/a19/ActivityDungeon1019_Map_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Map_2Uis
**Snippet:**
```lua
function GetActivityDungeon1019_Map_2Uis(ui)
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

## Activty/a19/ActivityDungeon1019_MaterialBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MaterialBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1019_MaterialBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
```

---

## Activty/a19/ActivityDungeon1019_MaterialByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MaterialUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1019_Material_BattleNumberByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1019_Material_BattleNumberByName")

function GetActivityDungeon1019_MaterialUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.BattleNumber = GetActivityDungeon1019_Material_BattleNumberUis(ui:GetChild("BattleNumber"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a19/ActivityDungeon1019_MaterialWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MaterialWindowUis
**Requires:**
- ActivityDungeon1019_MaterialByName
**Snippet:**
```lua
require("ActivityDungeon1019_MaterialByName")

function GetActivityDungeon1019_MaterialWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1019_MaterialUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Material_BattleAniByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Material_BattleAniUis
**Requires:**
- ActivityDungeon1019_Material_BattleByName
**Snippet:**
```lua
require("ActivityDungeon1019_Material_BattleByName")

function GetActivityDungeon1019_Material_BattleAniUis(ui)
  local uis = {}
  uis.Battle = GetActivityDungeon1019_Material_BattleUis(ui:GetChild("Battle"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Material_BattleByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Material_BattleUis
**Snippet:**
```lua
function GetActivityDungeon1019_Material_BattleUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Material_BattleNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Material_BattleNumberUis
**Snippet:**
```lua
function GetActivityDungeon1019_Material_BattleNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MaxBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MaxBtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_MaxBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MinBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MinBtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_MinBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniGameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniGameBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1019_MiniGameBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniGameByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniGameUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1019_MiniMain_TopByName
- ActivityDungeon1019_MiniMain_BottonByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1019_MiniMain_TopByName")
require("ActivityDungeon1019_MiniMain_BottonByName")

function GetActivityDungeon1019_MiniGameUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Top = GetActivityDungeon1019_MiniMain_TopUis(ui:GetChild("Top"))
  uis.Botton = GetActivityDungeon1019_MiniMain_BottonUis(ui:GetChild("Botton"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a19/ActivityDungeon1019_MiniGameStartByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniGameStartUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1019_MiniStart_OperateRegionByName
- ActivityDungeon1019_MiniStart_IntegralByName
- ActivityDungeon1019_MiniStart_HpByName
- ActivityDungeon1019_MiniStart_OperateTipsByName
- ActivityDungeon1019_MiniStart_WordTipsByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1019_MiniStart_OperateRegionByName")
require("ActivityDungeon1019_MiniStart_IntegralByName")
require("ActivityDungeon1019_MiniStart_HpByName")
require("ActivityDungeon1019_MiniStart_OperateTipsByName")
require("ActivityDungeon1019_MiniStart_WordTipsByName")

function GetActivityDungeon1019_MiniGameStartUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
```

---

## Activty/a19/ActivityDungeon1019_MiniGameStartWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniGameStartWindowUis
**Requires:**
- ActivityDungeon1019_MiniGameStartByName
**Snippet:**
```lua
require("ActivityDungeon1019_MiniGameStartByName")

function GetActivityDungeon1019_MiniGameStartWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1019_MiniGameStartUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniGameWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniGameWindowUis
**Requires:**
- ActivityDungeon1019_MiniGameByName
**Snippet:**
```lua
require("ActivityDungeon1019_MiniGameByName")

function GetActivityDungeon1019_MiniGameWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1019_MiniGameUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniMain_BottonByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniMain_BottonUis
**Requires:**
- ActivityDungeon1019_MiniMain_TodayTaskByName
**Snippet:**
```lua
require("ActivityDungeon1019_MiniMain_TodayTaskByName")

function GetActivityDungeon1019_MiniMain_BottonUis(ui)
  local uis = {}
  uis.TaskBtn = ui:GetChild("TaskBtn")
  uis.TodayTask = GetActivityDungeon1019_MiniMain_TodayTaskUis(ui:GetChild("TodayTask"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniMain_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniMain_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniMain_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniMain_RecordBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniMain_RecordBtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniMain_RecordBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniMain_StartBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniMain_StartBtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniMain_StartBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniMain_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniMain_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1019_MiniMain_TaskBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniMain_TodayTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniMain_TodayTaskUis
**Requires:**
- ActivityDungeon1019_PassReward_AllFrame_EByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("ActivityDungeon1019_PassReward_AllFrame_EByName")
require("CommonResource_RedDotByName")

function GetActivityDungeon1019_MiniMain_TodayTaskUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1019_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a19/ActivityDungeon1019_MiniMain_TopByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniMain_TopUis
**Requires:**
- ActivityDungeon1019_MiniMain_IntegralByName
**Snippet:**
```lua
require("ActivityDungeon1019_MiniMain_IntegralByName")

function GetActivityDungeon1019_MiniMain_TopUis(ui)
  local uis = {}
  uis.Integral = GetActivityDungeon1019_MiniMain_IntegralUis(ui:GetChild("Integral"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniStart_BlockByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_BlockUis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniStart_BlockUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniStart_CloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_CloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniStart_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniStart_Cloud01ByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_Cloud01Uis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniStart_Cloud01Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniStart_Cloud02ByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_Cloud02Uis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniStart_Cloud02Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniStart_Cloud03ByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_Cloud03Uis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniStart_Cloud03Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniStart_Cloud04ByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_Cloud04Uis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniStart_Cloud04Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniStart_Cloud05ByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_Cloud05Uis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniStart_Cloud05Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniStart_Cloud06ByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_Cloud06Uis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniStart_Cloud06Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniStart_Cloud07ByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_Cloud07Uis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniStart_Cloud07Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniStart_Cloud08ByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_Cloud08Uis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniStart_Cloud08Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniStart_Cloud09ByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_Cloud09Uis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniStart_Cloud09Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniStart_EndAgainBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_EndAgainBtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniStart_EndAgainBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniStart_EndCloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_EndCloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniStart_EndCloseBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniStart_EndRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_EndRewardUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetActivityDungeon1019_MiniStart_EndRewardUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.AgainBtn = ui:GetChild("AgainBtn")
  uis.CloseBtn = ui:GetChild("CloseBtn")
```

---

## Activty/a19/ActivityDungeon1019_MiniStart_EndRewardWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_EndRewardWindowUis
**Requires:**
- ActivityDungeon1019_MiniStart_EndRewardByName
**Snippet:**
```lua
require("ActivityDungeon1019_MiniStart_EndRewardByName")

function GetActivityDungeon1019_MiniStart_EndRewardWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1019_MiniStart_EndRewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniStart_GuGuByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_GuGuUis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniStart_GuGuUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniStart_HpByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_HpUis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniStart_HpUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniStart_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniStart_IntegralUis(ui)
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

## Activty/a19/ActivityDungeon1019_MiniStart_Map01ByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_Map01Uis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniStart_Map01Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniStart_Map02ByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_Map02Uis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniStart_Map02Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniStart_Map03ByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_Map03Uis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniStart_Map03Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniStart_Map04ByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_Map04Uis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniStart_Map04Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniStart_Map05ByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_Map05Uis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniStart_Map05Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniStart_OperateRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_OperateRegionUis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniStart_OperateRegionUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniStart_OperateTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_OperateTipsUis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniStart_OperateTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniStart_TouchBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_TouchBtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniStart_TouchBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniStart_WordTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniStart_WordTipsUis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniStart_WordTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniTaskUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1019_MiniTask_IntegralByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1019_MiniTask_IntegralByName")

function GetActivityDungeon1019_MiniTaskUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Integral = GetActivityDungeon1019_MiniTask_IntegralUis(ui:GetChild("Integral"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a19/ActivityDungeon1019_MiniTaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniTaskWindowUis
**Requires:**
- ActivityDungeon1019_MiniTaskByName
**Snippet:**
```lua
require("ActivityDungeon1019_MiniTaskByName")

function GetActivityDungeon1019_MiniTaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1019_MiniTaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniTask_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniTask_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniTask_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniTask_RewardItemByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniTask_RewardItemUis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniTask_RewardItemUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniTask_RewardItemGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniTask_RewardItemGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniTask_RewardItemGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniTask_TipsAniUis
**Requires:**
- ActivityDungeon1019_MiniTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1019_MiniTask_TipsByName")

function GetActivityDungeon1019_MiniTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1019_MiniTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_MiniTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1019_MiniTask_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1019_MiniTask_TipsUis(ui)
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

## Activty/a19/ActivityDungeon1019_NormalBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_NormalBtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_NormalBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_NormalPoint1BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_NormalPoint1BtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_NormalPoint1BtnUis(ui)
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

## Activty/a19/ActivityDungeon1019_NormalPoint2BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_NormalPoint2BtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_NormalPoint2BtnUis(ui)
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

## Activty/a19/ActivityDungeon1019_NormalPointLockByName.lua.lua
**Functions:**
- GetActivityDungeon1019_NormalPointLockUis
**Snippet:**
```lua
function GetActivityDungeon1019_NormalPointLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_NumberStripByName.lua.lua
**Functions:**
- GetActivityDungeon1019_NumberStripUis
**Snippet:**
```lua
function GetActivityDungeon1019_NumberStripUis(ui)
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

## Activty/a19/ActivityDungeon1019_PassBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1019_PassBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_PassClothes_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassClothes_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_PassClothes_BuyBtnUis(ui)
  local uis = {}
  
  uis.PriceTxt = ui:GetChild("PriceTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_PassClothes_BuyRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassClothes_BuyRewardUis
**Snippet:**
```lua
function GetActivityDungeon1019_PassClothes_BuyRewardUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_PassClothes_CardQBByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassClothes_CardQBUis
**Snippet:**
```lua
function GetActivityDungeon1019_PassClothes_CardQBUis(ui)
  local uis = {}
  
  uis.QBHolder = ui:GetChild("QBHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_PassClothes_ClothseRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassClothes_ClothseRegionUis
**Requires:**
- ActivityDungeon1019_PassClothes_WordByName
- ActivityDungeon1019_PassClothes_CardQBByName
- ActivityDungeon1019_PassClothes_BuyRewardByName
**Snippet:**
```lua
require("ActivityDungeon1019_PassClothes_WordByName")
require("ActivityDungeon1019_PassClothes_CardQBByName")
require("ActivityDungeon1019_PassClothes_BuyRewardByName")

function GetActivityDungeon1019_PassClothes_ClothseRegionUis(ui)
  local uis = {}
  uis.Word = GetActivityDungeon1019_PassClothes_WordUis(ui:GetChild("Word"))
  uis.CardQB = GetActivityDungeon1019_PassClothes_CardQBUis(ui:GetChild("CardQB"))
  uis.BuyReward = GetActivityDungeon1019_PassClothes_BuyRewardUis(ui:GetChild("BuyReward"))
  uis.BuyBtn = ui:GetChild("BuyBtn")
```

---

## Activty/a19/ActivityDungeon1019_PassClothes_NameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassClothes_NameBtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_PassClothes_NameBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_PassClothes_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassClothes_WordUis
**Snippet:**
```lua
function GetActivityDungeon1019_PassClothes_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_PassportByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassportUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1019_PassReward_RewardRegionByName
- ActivityDungeon1019_PassTask_TaskRegionByName
- ActivityDungeon1019_PassClothes_ClothseRegionByName
- ActivityDungeon1019_Passport_LevelByName
- ActivityDungeon1019_Sign_TimeByName
- ActivityDungeon1019_Passport_TabRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1019_PassReward_RewardRegionByName")
require("ActivityDungeon1019_PassTask_TaskRegionByName")
require("ActivityDungeon1019_PassClothes_ClothseRegionByName")
require("ActivityDungeon1019_Passport_LevelByName")
require("ActivityDungeon1019_Sign_TimeByName")
require("ActivityDungeon1019_Passport_TabRegionByName")

function GetActivityDungeon1019_PassportUis(ui)
  local uis = {}
```

---

## Activty/a19/ActivityDungeon1019_PassportUp_LevelUpBgByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassportUp_LevelUpBgUis
**Snippet:**
```lua
function GetActivityDungeon1019_PassportUp_LevelUpBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_PassportUp_LevelUpTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassportUp_LevelUpTipsUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1019_PassportUp_LevelUpBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1019_PassportUp_LevelUpBgByName")

function GetActivityDungeon1019_PassportUp_LevelUpTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.LevelUpBg = GetActivityDungeon1019_PassportUp_LevelUpBgUis(ui:GetChild("LevelUpBg"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
```

---

## Activty/a19/ActivityDungeon1019_PassportUp_LevelUpTipsWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassportUp_LevelUpTipsWindowUis
**Requires:**
- ActivityDungeon1019_PassportUp_LevelUpTipsByName
**Snippet:**
```lua
require("ActivityDungeon1019_PassportUp_LevelUpTipsByName")

function GetActivityDungeon1019_PassportUp_LevelUpTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1019_PassportUp_LevelUpTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_PassportWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassportWindowUis
**Requires:**
- ActivityDungeon1019_PassportByName
**Snippet:**
```lua
require("ActivityDungeon1019_PassportByName")

function GetActivityDungeon1019_PassportWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1019_PassportUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Passport_AllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Passport_AllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_Passport_AllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Passport_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Passport_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_Passport_BuyBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Passport_ExpProgressBarByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Passport_ExpProgressBarUis
**Requires:**
- ActivityDungeon1019_Passport_ExpProgressFillByName
**Snippet:**
```lua
require("ActivityDungeon1019_Passport_ExpProgressFillByName")

function GetActivityDungeon1019_Passport_ExpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetActivityDungeon1019_Passport_ExpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Passport_ExpProgressFillByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Passport_ExpProgressFillUis
**Snippet:**
```lua
function GetActivityDungeon1019_Passport_ExpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Passport_LevelByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Passport_LevelUis
**Snippet:**
```lua
function GetActivityDungeon1019_Passport_LevelUis(ui)
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

## Activty/a19/ActivityDungeon1019_Passport_TabBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Passport_TabBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1019_Passport_TabBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## Activty/a19/ActivityDungeon1019_Passport_TabRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Passport_TabRegionUis
**Snippet:**
```lua
function GetActivityDungeon1019_Passport_TabRegionUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_PassReward_AllFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassReward_AllFrame_EUis
**Requires:**
- ActivityDungeon1019_PassReward_ItemFrame_EByName
- ActivityDungeon1019_PassReward_CardFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1019_PassReward_ItemFrame_EByName")
require("ActivityDungeon1019_PassReward_CardFrame_EByName")

function GetActivityDungeon1019_PassReward_AllFrame_EUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1019_PassReward_ItemFrame_EUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1019_PassReward_CardFrame_EUis(ui:GetChild("CardFrame"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## Activty/a19/ActivityDungeon1019_PassReward_AllFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassReward_AllFrame_MUis
**Requires:**
- ActivityDungeon1019_PassReward_ItemFrame_MByName
- ActivityDungeon1019_PassReward_CardFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1019_PassReward_ItemFrame_MByName")
require("ActivityDungeon1019_PassReward_CardFrame_MByName")

function GetActivityDungeon1019_PassReward_AllFrame_MUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1019_PassReward_ItemFrame_MUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1019_PassReward_CardFrame_MUis(ui:GetChild("CardFrame"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a19/ActivityDungeon1019_PassReward_CardFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassReward_CardFrame_EUis
**Requires:**
- ActivityDungeon1019_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1019_PassReward_ItemCardPicByName")

function GetActivityDungeon1019_PassReward_CardFrame_EUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1019_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a19/ActivityDungeon1019_PassReward_CardFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassReward_CardFrame_MUis
**Requires:**
- ActivityDungeon1019_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1019_PassReward_ItemCardPicByName")

function GetActivityDungeon1019_PassReward_CardFrame_MUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1019_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a19/ActivityDungeon1019_PassReward_EndTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassReward_EndTwoUis
**Requires:**
- ActivityDungeon1019_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1019_PassReward_AllFrame_EByName")

function GetActivityDungeon1019_PassReward_EndTwoUis(ui)
  local uis = {}
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.Item1 = GetActivityDungeon1019_PassReward_AllFrame_EUis(ui:GetChild("Item1"))
  uis.Item2 = GetActivityDungeon1019_PassReward_AllFrame_EUis(ui:GetChild("Item2"))
  uis.root = ui
```

---

## Activty/a19/ActivityDungeon1019_PassReward_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassReward_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1019_PassReward_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_PassReward_ItemFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassReward_ItemFrame_EUis
**Snippet:**
```lua
function GetActivityDungeon1019_PassReward_ItemFrame_EUis(ui)
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

## Activty/a19/ActivityDungeon1019_PassReward_ItemFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassReward_ItemFrame_MUis
**Snippet:**
```lua
function GetActivityDungeon1019_PassReward_ItemFrame_MUis(ui)
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

## Activty/a19/ActivityDungeon1019_PassReward_LevelTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassReward_LevelTitleUis
**Snippet:**
```lua
function GetActivityDungeon1019_PassReward_LevelTitleUis(ui)
  local uis = {}
  
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_PassReward_MiddleRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassReward_MiddleRegionUis
**Snippet:**
```lua
function GetActivityDungeon1019_PassReward_MiddleRegionUis(ui)
  local uis = {}
  
  uis.MiddleList = ui:GetChild("MiddleList")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_PassReward_MidTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassReward_MidTwoUis
**Requires:**
- ActivityDungeon1019_PassReward_MidTwoItemByName
- ActivityDungeon1019_PassReward_LevelTitleByName
**Snippet:**
```lua
require("ActivityDungeon1019_PassReward_MidTwoItemByName")
require("ActivityDungeon1019_PassReward_LevelTitleByName")

function GetActivityDungeon1019_PassReward_MidTwoUis(ui)
  local uis = {}
  uis.Reward1 = GetActivityDungeon1019_PassReward_MidTwoItemUis(ui:GetChild("Reward1"))
  uis.Reward2 = GetActivityDungeon1019_PassReward_MidTwoItemUis(ui:GetChild("Reward2"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Title = GetActivityDungeon1019_PassReward_LevelTitleUis(ui:GetChild("Title"))
```

---

## Activty/a19/ActivityDungeon1019_PassReward_MidTwoItemByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassReward_MidTwoItemUis
**Requires:**
- ActivityDungeon1019_PassReward_AllFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1019_PassReward_AllFrame_MByName")

function GetActivityDungeon1019_PassReward_MidTwoItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1019_PassReward_AllFrame_MUis(ui:GetChild("Item"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_PassReward_PicByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassReward_PicUis
**Snippet:**
```lua
function GetActivityDungeon1019_PassReward_PicUis(ui)
  local uis = {}
  
  uis.BuyTxt = ui:GetChild("BuyTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_PassReward_RewardRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassReward_RewardRegionUis
**Requires:**
- ActivityDungeon1019_PassReward_MiddleRegionByName
- ActivityDungeon1019_PassReward_StartTwoByName
- ActivityDungeon1019_PassReward_EndTwoByName
**Snippet:**
```lua
require("ActivityDungeon1019_PassReward_MiddleRegionByName")
require("ActivityDungeon1019_PassReward_StartTwoByName")
require("ActivityDungeon1019_PassReward_EndTwoByName")

function GetActivityDungeon1019_PassReward_RewardRegionUis(ui)
  local uis = {}
  uis.MiddleList = GetActivityDungeon1019_PassReward_MiddleRegionUis(ui:GetChild("MiddleList"))
  uis.StartTwo = GetActivityDungeon1019_PassReward_StartTwoUis(ui:GetChild("StartTwo"))
  uis.EndTwo = GetActivityDungeon1019_PassReward_EndTwoUis(ui:GetChild("EndTwo"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a19/ActivityDungeon1019_PassReward_StartTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassReward_StartTwoUis
**Requires:**
- ActivityDungeon1019_PassReward_PicByName
**Snippet:**
```lua
require("ActivityDungeon1019_PassReward_PicByName")

function GetActivityDungeon1019_PassReward_StartTwoUis(ui)
  local uis = {}
  uis.Pic = GetActivityDungeon1019_PassReward_PicUis(ui:GetChild("Pic"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_PassTask_TaskRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassTask_TaskRegionUis
**Requires:**
- ActivityDungeon1019_TaskMaxByName
**Snippet:**
```lua
require("ActivityDungeon1019_TaskMaxByName")

function GetActivityDungeon1019_PassTask_TaskRegionUis(ui)
  local uis = {}
  uis.TipsList = ui:GetChild("TipsList")
  uis.Max = GetActivityDungeon1019_TaskMaxUis(ui:GetChild("Max"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_PassTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassTask_TipsAniUis
**Requires:**
- ActivityDungeon1019_PassTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1019_PassTask_TipsByName")

function GetActivityDungeon1019_PassTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1019_PassTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_PassTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassTask_TipsUis
**Requires:**
- ActivityDungeon1019_PassTask_TipsIntegralByName
**Snippet:**
```lua
require("ActivityDungeon1019_PassTask_TipsIntegralByName")

function GetActivityDungeon1019_PassTask_TipsUis(ui)
  local uis = {}
  uis.ProgressTxt = ui:GetChild("ProgressTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Integral = GetActivityDungeon1019_PassTask_TipsIntegralUis(ui:GetChild("Integral"))
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a19/ActivityDungeon1019_PassTask_TipsIntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PassTask_TipsIntegralUis
**Snippet:**
```lua
function GetActivityDungeon1019_PassTask_TipsIntegralUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_PlotBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PlotBtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_PlotBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_PlotByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PlotUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1019_Plot_WordByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1019_Plot_WordByName")

function GetActivityDungeon1019_PlotUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Word = GetActivityDungeon1019_Plot_WordUis(ui:GetChild("Word"))
  uis.PlotList = ui:GetChild("PlotList")
  uis.ProspectBtn = ui:GetChild("ProspectBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a19/ActivityDungeon1019_PlotWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1019_PlotWindowUis
**Requires:**
- ActivityDungeon1019_PlotByName
**Snippet:**
```lua
require("ActivityDungeon1019_PlotByName")

function GetActivityDungeon1019_PlotWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1019_PlotUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Plot_ProspectBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Plot_ProspectBtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_Plot_ProspectBtnUis(ui)
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

## Activty/a19/ActivityDungeon1019_Plot_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Plot_TipsAniUis
**Requires:**
- ActivityDungeon1019_Plot_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1019_Plot_TipsByName")

function GetActivityDungeon1019_Plot_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1019_Plot_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Plot_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Plot_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1019_Plot_TipsUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Plot_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Plot_WordUis
**Snippet:**
```lua
function GetActivityDungeon1019_Plot_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_ReduceBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_ReduceBtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_ReduceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_ReviewWordByName.lua.lua
**Functions:**
- GetActivityDungeon1019_ReviewWordUis
**Snippet:**
```lua
function GetActivityDungeon1019_ReviewWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_ShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_ShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_ShopBtnUis(ui)
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

## Activty/a19/ActivityDungeon1019_ShopByName.lua.lua
**Functions:**
- GetActivityDungeon1019_ShopUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1019_Shop_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1019_Shop_TimeByName")

function GetActivityDungeon1019_ShopUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Time = GetActivityDungeon1019_Shop_TimeUis(ui:GetChild("Time"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a19/ActivityDungeon1019_ShopWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1019_ShopWindowUis
**Requires:**
- ActivityDungeon1019_ShopByName
**Snippet:**
```lua
require("ActivityDungeon1019_ShopByName")

function GetActivityDungeon1019_ShopWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1019_ShopUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Shop_CardHeadBgByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Shop_CardHeadBgUis
**Snippet:**
```lua
function GetActivityDungeon1019_Shop_CardHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Shop_ItemAniByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Shop_ItemAniUis
**Requires:**
- ActivityDungeon1019_Shop_ItemByName
**Snippet:**
```lua
require("ActivityDungeon1019_Shop_ItemByName")

function GetActivityDungeon1019_Shop_ItemAniUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1019_Shop_ItemUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Shop_ItemBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Shop_ItemBtnUis
**Requires:**
- ActivityDungeon1019_Shop_CardHeadBgByName
- ActivityDungeon1019_Shop_ItemNumberByName
- ActivityDungeon1019_Shop_UseMarkByName
**Snippet:**
```lua
require("ActivityDungeon1019_Shop_CardHeadBgByName")
require("ActivityDungeon1019_Shop_ItemNumberByName")
require("ActivityDungeon1019_Shop_UseMarkByName")

function GetActivityDungeon1019_Shop_ItemBtnUis(ui)
  local uis = {}
  uis.CardHeadBg = GetActivityDungeon1019_Shop_CardHeadBgUis(ui:GetChild("CardHeadBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.ItemNumber = GetActivityDungeon1019_Shop_ItemNumberUis(ui:GetChild("ItemNumber"))
```

---

## Activty/a19/ActivityDungeon1019_Shop_ItemByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Shop_ItemUis
**Requires:**
- ActivityDungeon1019_Shop_SellOutByName
**Snippet:**
```lua
require("ActivityDungeon1019_Shop_SellOutByName")

function GetActivityDungeon1019_Shop_ItemUis(ui)
  local uis = {}
  uis.ItemBtn = ui:GetChild("ItemBtn")
  uis.SellOut = GetActivityDungeon1019_Shop_SellOutUis(ui:GetChild("SellOut"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Shop_ItemNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Shop_ItemNumberUis
**Snippet:**
```lua
function GetActivityDungeon1019_Shop_ItemNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Shop_ItemRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Shop_ItemRegionUis
**Requires:**
- ActivityDungeon1019_Shop_TitleByName
**Snippet:**
```lua
require("ActivityDungeon1019_Shop_TitleByName")

function GetActivityDungeon1019_Shop_ItemRegionUis(ui)
  local uis = {}
  uis.ShopTitle = GetActivityDungeon1019_Shop_TitleUis(ui:GetChild("ShopTitle"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Shop_SellOutByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Shop_SellOutUis
**Snippet:**
```lua
function GetActivityDungeon1019_Shop_SellOutUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Shop_StarByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Shop_StarUis
**Snippet:**
```lua
function GetActivityDungeon1019_Shop_StarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Shop_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Shop_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1019_Shop_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Shop_TitleByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Shop_TitleUis
**Snippet:**
```lua
function GetActivityDungeon1019_Shop_TitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Shop_UseMarkByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Shop_UseMarkUis
**Snippet:**
```lua
function GetActivityDungeon1019_Shop_UseMarkUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_SignBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_SignBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1019_SignBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_SignByName.lua.lua
**Functions:**
- GetActivityDungeon1019_SignUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1019_Sign_RewardListByName
- ActivityDungeon1019_Sign_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1019_Sign_RewardListByName")
require("ActivityDungeon1019_Sign_TimeByName")

function GetActivityDungeon1019_SignUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.RewardList = GetActivityDungeon1019_Sign_RewardListUis(ui:GetChild("RewardList"))
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.Time = GetActivityDungeon1019_Sign_TimeUis(ui:GetChild("Time"))
```

---

## Activty/a19/ActivityDungeon1019_SignWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1019_SignWindowUis
**Requires:**
- ActivityDungeon1019_SignByName
**Snippet:**
```lua
require("ActivityDungeon1019_SignByName")

function GetActivityDungeon1019_SignWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1019_SignUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Sign_AllFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Sign_AllFrameUis
**Requires:**
- ActivityDungeon1019_Sign_ItemFrameByName
- ActivityDungeon1019_Sign_CardFrameByName
**Snippet:**
```lua
require("ActivityDungeon1019_Sign_ItemFrameByName")
require("ActivityDungeon1019_Sign_CardFrameByName")

function GetActivityDungeon1019_Sign_AllFrameUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1019_Sign_ItemFrameUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1019_Sign_CardFrameUis(ui:GetChild("CardFrame"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a19/ActivityDungeon1019_Sign_CardFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Sign_CardFrameUis
**Requires:**
- ActivityDungeon1019_Sign_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1019_Sign_ItemCardPicByName")

function GetActivityDungeon1019_Sign_CardFrameUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1019_Sign_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a19/ActivityDungeon1019_Sign_GetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Sign_GetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_Sign_GetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Sign_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Sign_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1019_Sign_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Sign_ItemFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Sign_ItemFrameUis
**Snippet:**
```lua
function GetActivityDungeon1019_Sign_ItemFrameUis(ui)
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

## Activty/a19/ActivityDungeon1019_Sign_RewardAniByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Sign_RewardAniUis
**Requires:**
- ActivityDungeon1019_Sign_RewardByName
**Snippet:**
```lua
require("ActivityDungeon1019_Sign_RewardByName")

function GetActivityDungeon1019_Sign_RewardAniUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1019_Sign_RewardUis(ui:GetChild("Reward"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Sign_RewardByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Sign_RewardUis
**Requires:**
- ActivityDungeon1019_Sign_AllFrameByName
**Snippet:**
```lua
require("ActivityDungeon1019_Sign_AllFrameByName")

function GetActivityDungeon1019_Sign_RewardUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1019_Sign_AllFrameUis(ui:GetChild("Item"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Sign_RewardListByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Sign_RewardListUis
**Snippet:**
```lua
function GetActivityDungeon1019_Sign_RewardListUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_Sign_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1019_Sign_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1019_Sign_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_TaskAllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_TaskAllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_TaskAllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1019_TaskBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_TaskByName.lua.lua
**Functions:**
- GetActivityDungeon1019_TaskUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1019_TaskTitleByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1019_TaskTitleByName")

function GetActivityDungeon1019_TaskUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TaskTitle = GetActivityDungeon1019_TaskTitleUis(ui:GetChild("TaskTitle"))
  uis.TaskTipsList = ui:GetChild("TaskTipsList")
  uis.AllGetBtn = ui:GetChild("AllGetBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a19/ActivityDungeon1019_TaskGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1019_TaskGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1019_TaskGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_TaskMaxByName.lua.lua
**Functions:**
- GetActivityDungeon1019_TaskMaxUis
**Snippet:**
```lua
function GetActivityDungeon1019_TaskMaxUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_TaskProgressByName.lua.lua
**Functions:**
- GetActivityDungeon1019_TaskProgressUis
**Snippet:**
```lua
function GetActivityDungeon1019_TaskProgressUis(ui)
  local uis = {}
  
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_TaskTipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1019_TaskTipsAniUis
**Requires:**
- ActivityDungeon1019_TaskTipsByName
**Snippet:**
```lua
require("ActivityDungeon1019_TaskTipsByName")

function GetActivityDungeon1019_TaskTipsAniUis(ui)
  local uis = {}
  uis.TaskTips = GetActivityDungeon1019_TaskTipsUis(ui:GetChild("TaskTips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_TaskTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1019_TaskTipsUis
**Requires:**
- ActivityDungeon1019_TaskProgressByName
**Snippet:**
```lua
require("ActivityDungeon1019_TaskProgressByName")

function GetActivityDungeon1019_TaskTipsUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.RewardList = ui:GetChild("RewardList")
  uis.TaskProgress = GetActivityDungeon1019_TaskProgressUis(ui:GetChild("TaskProgress"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a19/ActivityDungeon1019_TaskTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1019_TaskTitleUis
**Snippet:**
```lua
function GetActivityDungeon1019_TaskTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a19/ActivityDungeon1019_TaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1019_TaskWindowUis
**Requires:**
- ActivityDungeon1019_TaskByName
**Snippet:**
```lua
require("ActivityDungeon1019_TaskByName")

function GetActivityDungeon1019_TaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1019_TaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---
