# Activty/a4

## Activty/a4/ActivityDungeon1004_ActivityDungeonByName.lua.lua
**Functions:**
- GetActivityDungeon1004_ActivityDungeonUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1004_MainTitleByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1004_MainTitleByName")
require("CommonResource_CurrencyReturnByName")

function GetActivityDungeon1004_ActivityDungeonUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.MainTitle = GetActivityDungeon1004_MainTitleUis(ui:GetChild("MainTitle"))
  uis.MiniGame1Btn = ui:GetChild("MiniGame1Btn")
  uis.MiniGameBtn = ui:GetChild("MiniGameBtn")
```

---

## Activty/a4/ActivityDungeon1004_ActivityDungeonWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1004_ActivityDungeonWindowUis
**Requires:**
- ActivityDungeon1004_ActivityDungeonByName
**Snippet:**
```lua
require("ActivityDungeon1004_ActivityDungeonByName")

function GetActivityDungeon1004_ActivityDungeonWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1004_ActivityDungeonUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_AddBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_AddBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_AddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_BossBattleByName.lua.lua
**Functions:**
- GetActivityDungeon1004_BossBattleUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1004_BossBattle_InfoByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1004_BossBattle_InfoByName")

function GetActivityDungeon1004_BossBattleUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.Info = GetActivityDungeon1004_BossBattle_InfoUis(ui:GetChild("Info"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a4/ActivityDungeon1004_BossBattleWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1004_BossBattleWindowUis
**Requires:**
- ActivityDungeon1004_BossBattleByName
**Snippet:**
```lua
require("ActivityDungeon1004_BossBattleByName")

function GetActivityDungeon1004_BossBattleWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1004_BossBattleUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_BossBattle_Info1ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_BossBattle_Info1Uis
**Snippet:**
```lua
function GetActivityDungeon1004_BossBattle_Info1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_BossBattle_InfoByName.lua.lua
**Functions:**
- GetActivityDungeon1004_BossBattle_InfoUis
**Requires:**
- ActivityDungeon1004_BossBattle_Info1ByName
**Snippet:**
```lua
require("ActivityDungeon1004_BossBattle_Info1ByName")

function GetActivityDungeon1004_BossBattle_InfoUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = GetActivityDungeon1004_BossBattle_Info1Uis(ui:GetChild("WordTxt"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_BossBattle_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1004_BossBattle_TipsAniUis
**Requires:**
- ActivityDungeon1004_BossBattle_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1004_BossBattle_TipsByName")

function GetActivityDungeon1004_BossBattle_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1004_BossBattle_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_BossBattle_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1004_BossBattle_TipsUis
**Requires:**
- ActivityDungeon1004_BossBattle_TipsRewardByName
**Snippet:**
```lua
require("ActivityDungeon1004_BossBattle_TipsRewardByName")

function GetActivityDungeon1004_BossBattle_TipsUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1004_BossBattle_TipsRewardUis(ui:GetChild("Reward"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.NumberWordTxt = ui:GetChild("NumberWordTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a4/ActivityDungeon1004_BossBattle_TipsRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1004_BossBattle_TipsRewardUis
**Snippet:**
```lua
function GetActivityDungeon1004_BossBattle_TipsRewardUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_BossBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_BossBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1004_BossBtnUis(ui)
  local uis = {}
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.newCtr = ui:GetController("new")
```

---

## Activty/a4/ActivityDungeon1004_BuyLevelBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_BuyLevelBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_BuyLevelBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_BuyLevelDes1ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_BuyLevelDes1Uis
**Requires:**
- ActivityDungeon1004_NumberStripByName
- ActivityDungeon1004_BuyPriceNumberByName
**Snippet:**
```lua
require("ActivityDungeon1004_NumberStripByName")
require("ActivityDungeon1004_BuyPriceNumberByName")

function GetActivityDungeon1004_BuyLevelDes1Uis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.NumberStrip = GetActivityDungeon1004_NumberStripUis(ui:GetChild("NumberStrip"))
  uis.BuyPriceNumber = GetActivityDungeon1004_BuyPriceNumberUis(ui:GetChild("BuyPriceNumber"))
```

---

## Activty/a4/ActivityDungeon1004_BuyLevelDes2ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_BuyLevelDes2Uis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1004_BuyLevelDes1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1004_BuyLevelDes1ByName")

function GetActivityDungeon1004_BuyLevelDes2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.BuyLevelDes1 = GetActivityDungeon1004_BuyLevelDes1Uis(ui:GetChild("BuyLevelDes1"))
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.root = ui
```

---

## Activty/a4/ActivityDungeon1004_BuyLevelDesWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1004_BuyLevelDesWindowUis
**Requires:**
- ActivityDungeon1004_BuyLevelDes2ByName
**Snippet:**
```lua
require("ActivityDungeon1004_BuyLevelDes2ByName")

function GetActivityDungeon1004_BuyLevelDesWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1004_BuyLevelDes2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_BuyLevelItemByName.lua.lua
**Functions:**
- GetActivityDungeon1004_BuyLevelItemUis
**Requires:**
- ActivityDungeon1004_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1004_PassReward_AllFrame_EByName")

function GetActivityDungeon1004_BuyLevelItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1004_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_BuyPriceNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1004_BuyPriceNumberUis
**Snippet:**
```lua
function GetActivityDungeon1004_BuyPriceNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_ChallengeByName.lua.lua
**Functions:**
- GetActivityDungeon1004_ChallengeUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1004_MapListByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1004_MapListByName")

function GetActivityDungeon1004_ChallengeUis(ui)
  local uis = {}
  uis.BgList = ui:GetChild("BgList")
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Map = GetActivityDungeon1004_MapListUis(ui:GetChild("Map"))
  uis.ShopBtn = ui:GetChild("ShopBtn")
  uis.ChapterList = ui:GetChild("ChapterList")
```

---

## Activty/a4/ActivityDungeon1004_ChallengeChapterBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_ChallengeChapterBtnUis
**Requires:**
- ActivityDungeon1004_NormalPointLockByName
**Snippet:**
```lua
require("ActivityDungeon1004_NormalPointLockByName")

function GetActivityDungeon1004_ChallengeChapterBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Lock = GetActivityDungeon1004_NormalPointLockUis(ui:GetChild("Lock"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Activty/a4/ActivityDungeon1004_ChallengeShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_ChallengeShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_ChallengeShopBtnUis(ui)
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

## Activty/a4/ActivityDungeon1004_ChallengeWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1004_ChallengeWindowUis
**Requires:**
- ActivityDungeon1004_ChallengeByName
**Snippet:**
```lua
require("ActivityDungeon1004_ChallengeByName")

function GetActivityDungeon1004_ChallengeWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1004_ChallengeUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MainBuildSignByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MainBuildSignUis
**Snippet:**
```lua
function GetActivityDungeon1004_MainBuildSignUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MainSeasonsByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MainSeasonsUis
**Snippet:**
```lua
function GetActivityDungeon1004_MainSeasonsUis(ui)
  local uis = {}
  
  uis.BackGroundHolder = ui:GetChild("BackGroundHolder")
  uis.BackGround1Holder = ui:GetChild("BackGround1Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MainSeasonsWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MainSeasonsWindowUis
**Requires:**
- ActivityDungeon1004_MainSeasonsByName
**Snippet:**
```lua
require("ActivityDungeon1004_MainSeasonsByName")

function GetActivityDungeon1004_MainSeasonsWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1004_MainSeasonsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MainTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MainTitleUis
**Snippet:**
```lua
function GetActivityDungeon1004_MainTitleUis(ui)
  local uis = {}
  
  uis.Time1Txt = ui:GetChild("Time1Txt")
  uis.Time2Txt = ui:GetChild("Time2Txt")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MapBottom_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MapBottom_1Uis
**Snippet:**
```lua
function GetActivityDungeon1004_MapBottom_1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MapBottom_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MapBottom_2Uis
**Snippet:**
```lua
function GetActivityDungeon1004_MapBottom_2Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MapBottom_3ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MapBottom_3Uis
**Snippet:**
```lua
function GetActivityDungeon1004_MapBottom_3Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MapBottom_4ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MapBottom_4Uis
**Snippet:**
```lua
function GetActivityDungeon1004_MapBottom_4Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MapListByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MapListUis
**Snippet:**
```lua
function GetActivityDungeon1004_MapListUis(ui)
  local uis = {}
  
  uis.MapList = ui:GetChild("MapList")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Map_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Map_1Uis
**Snippet:**
```lua
function GetActivityDungeon1004_Map_1Uis(ui)
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

## Activty/a4/ActivityDungeon1004_Map_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Map_2Uis
**Snippet:**
```lua
function GetActivityDungeon1004_Map_2Uis(ui)
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

## Activty/a4/ActivityDungeon1004_Map_3ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Map_3Uis
**Snippet:**
```lua
function GetActivityDungeon1004_Map_3Uis(ui)
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

## Activty/a4/ActivityDungeon1004_Map_4ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Map_4Uis
**Snippet:**
```lua
function GetActivityDungeon1004_Map_4Uis(ui)
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

## Activty/a4/ActivityDungeon1004_MaterialBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MaterialBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1004_MaterialBtnUis(ui)
  local uis = {}
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
```

---

## Activty/a4/ActivityDungeon1004_MaterialByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MaterialUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1004_Material_BattleNumberByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1004_Material_BattleNumberByName")

function GetActivityDungeon1004_MaterialUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.BattleNumber = GetActivityDungeon1004_Material_BattleNumberUis(ui:GetChild("BattleNumber"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a4/ActivityDungeon1004_MaterialWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MaterialWindowUis
**Requires:**
- ActivityDungeon1004_MaterialByName
**Snippet:**
```lua
require("ActivityDungeon1004_MaterialByName")

function GetActivityDungeon1004_MaterialWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1004_MaterialUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Material_BattleAniByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Material_BattleAniUis
**Requires:**
- ActivityDungeon1004_Material_BattleByName
**Snippet:**
```lua
require("ActivityDungeon1004_Material_BattleByName")

function GetActivityDungeon1004_Material_BattleAniUis(ui)
  local uis = {}
  uis.Battle = GetActivityDungeon1004_Material_BattleUis(ui:GetChild("Battle"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Material_BattleByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Material_BattleUis
**Snippet:**
```lua
function GetActivityDungeon1004_Material_BattleUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Material_BattleNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Material_BattleNumberUis
**Snippet:**
```lua
function GetActivityDungeon1004_Material_BattleNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MaxBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MaxBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_MaxBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MinBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MinBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_MinBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniBook2ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniBook2Uis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1004_MiniBook2_NumberByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1004_MiniBook2_NumberByName")

function GetActivityDungeon1004_MiniBook2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.Number = GetActivityDungeon1004_MiniBook2_NumberUis(ui:GetChild("Number"))
  uis.TipsList = ui:GetChild("TipsList")
```

---

## Activty/a4/ActivityDungeon1004_MiniBook2WindowByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniBook2WindowUis
**Requires:**
- ActivityDungeon1004_MiniBook2ByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniBook2ByName")

function GetActivityDungeon1004_MiniBook2WindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1004_MiniBook2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniBook2_GetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniBook2_GetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniBook2_GetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniBook2_NumberByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniBook2_NumberUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniBook2_NumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniBook2_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniBook2_TipsAniUis
**Requires:**
- ActivityDungeon1004_MiniBook2_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniBook2_TipsByName")

function GetActivityDungeon1004_MiniBook2_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1004_MiniBook2_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniBook2_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniBook2_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniBook2_TipsUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
```

---

## Activty/a4/ActivityDungeon1004_MiniGame1BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniGame1BtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1004_MiniGame1BtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniGame2ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniGame2Uis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1004_MiniMain2_TopByName
- ActivityDungeon1004_MiniMain2_BottonByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1004_MiniMain2_TopByName")
require("ActivityDungeon1004_MiniMain2_BottonByName")

function GetActivityDungeon1004_MiniGame2Uis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Top = GetActivityDungeon1004_MiniMain2_TopUis(ui:GetChild("Top"))
  uis.Botton = GetActivityDungeon1004_MiniMain2_BottonUis(ui:GetChild("Botton"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a4/ActivityDungeon1004_MiniGame2WindowByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniGame2WindowUis
**Requires:**
- ActivityDungeon1004_MiniGame2ByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniGame2ByName")

function GetActivityDungeon1004_MiniGame2WindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1004_MiniGame2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniGameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniGameBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1004_MiniGameBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniGameByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniGameUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1004_MiniMain_TopByName
- ActivityDungeon1004_MiniMain_BottonByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1004_MiniMain_TopByName")
require("ActivityDungeon1004_MiniMain_BottonByName")

function GetActivityDungeon1004_MiniGameUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Top = GetActivityDungeon1004_MiniMain_TopUis(ui:GetChild("Top"))
  uis.Botton = GetActivityDungeon1004_MiniMain_BottonUis(ui:GetChild("Botton"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a4/ActivityDungeon1004_MiniGameStart2ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniGameStart2Uis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1004_MiniStart2_TopRegionByName
- ActivityDungeon1004_MiniStart2_StageRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1004_MiniStart2_TopRegionByName")
require("ActivityDungeon1004_MiniStart2_StageRegionByName")

function GetActivityDungeon1004_MiniGameStart2Uis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TopRegion = GetActivityDungeon1004_MiniStart2_TopRegionUis(ui:GetChild("TopRegion"))
  uis.StageRegion = GetActivityDungeon1004_MiniStart2_StageRegionUis(ui:GetChild("StageRegion"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
```

---

## Activty/a4/ActivityDungeon1004_MiniGameStart2WindowByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniGameStart2WindowUis
**Requires:**
- ActivityDungeon1004_MiniGameStart2ByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniGameStart2ByName")

function GetActivityDungeon1004_MiniGameStart2WindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1004_MiniGameStart2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniGameStartByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniGameStartUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1004_MiniStart_IntegralByName
- ActivityDungeon1004_MiniStart_ConditionByName
- ActivityDungeon1004_MiniStart_LatticeRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1004_MiniStart_IntegralByName")
require("ActivityDungeon1004_MiniStart_ConditionByName")
require("ActivityDungeon1004_MiniStart_LatticeRegionByName")

function GetActivityDungeon1004_MiniGameStartUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Integral = GetActivityDungeon1004_MiniStart_IntegralUis(ui:GetChild("Integral"))
  uis.Condition = GetActivityDungeon1004_MiniStart_ConditionUis(ui:GetChild("Condition"))
```

---

## Activty/a4/ActivityDungeon1004_MiniGameStartWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniGameStartWindowUis
**Requires:**
- ActivityDungeon1004_MiniGameStartByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniGameStartByName")

function GetActivityDungeon1004_MiniGameStartWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1004_MiniGameStartUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniGameWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniGameWindowUis
**Requires:**
- ActivityDungeon1004_MiniGameByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniGameByName")

function GetActivityDungeon1004_MiniGameWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1004_MiniGameUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniIntegral2ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniIntegral2Uis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetActivityDungeon1004_MiniIntegral2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
  return uis
```

---

## Activty/a4/ActivityDungeon1004_MiniIntegral2WindowByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniIntegral2WindowUis
**Requires:**
- ActivityDungeon1004_MiniIntegral2ByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniIntegral2ByName")

function GetActivityDungeon1004_MiniIntegral2WindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1004_MiniIntegral2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniIntegral2_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniIntegral2_TipsAniUis
**Requires:**
- ActivityDungeon1004_MiniIntegral2_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniIntegral2_TipsByName")

function GetActivityDungeon1004_MiniIntegral2_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1004_MiniIntegral2_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniIntegral2_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniIntegral2_TipsUis
**Requires:**
- ActivityDungeon1004_MiniIntegral2_TipsFirstByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniIntegral2_TipsFirstByName")

function GetActivityDungeon1004_MiniIntegral2_TipsUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.First = GetActivityDungeon1004_MiniIntegral2_TipsFirstUis(ui:GetChild("First"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a4/ActivityDungeon1004_MiniIntegral2_TipsFirstByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniIntegral2_TipsFirstUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniIntegral2_TipsFirstUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniIntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniIntegralUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetActivityDungeon1004_MiniIntegralUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
  return uis
```

---

## Activty/a4/ActivityDungeon1004_MiniIntegralWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniIntegralWindowUis
**Requires:**
- ActivityDungeon1004_MiniIntegralByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniIntegralByName")

function GetActivityDungeon1004_MiniIntegralWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1004_MiniIntegralUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniIntegral_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniIntegral_TipsAniUis
**Requires:**
- ActivityDungeon1004_MiniIntegral_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniIntegral_TipsByName")

function GetActivityDungeon1004_MiniIntegral_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1004_MiniIntegral_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniIntegral_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniIntegral_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniIntegral_TipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniMain2_BookBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniMain2_BookBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniMain2_BookBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniMain2_BottonByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniMain2_BottonUis
**Requires:**
- ActivityDungeon1004_MiniMain2_TodayTaskByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniMain2_TodayTaskByName")

function GetActivityDungeon1004_MiniMain2_BottonUis(ui)
  local uis = {}
  uis.TaskBtn = ui:GetChild("TaskBtn")
  uis.RecordBtn = ui:GetChild("RecordBtn")
  uis.TodayTask = GetActivityDungeon1004_MiniMain2_TodayTaskUis(ui:GetChild("TodayTask"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniMain2_RecordBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniMain2_RecordBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniMain2_RecordBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniMain2_StartBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniMain2_StartBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniMain2_StartBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniMain2_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniMain2_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1004_MiniMain2_TaskBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniMain2_TodayTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniMain2_TodayTaskUis
**Requires:**
- ActivityDungeon1004_PassReward_AllFrame_EByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("ActivityDungeon1004_PassReward_AllFrame_EByName")
require("CommonResource_RedDotByName")

function GetActivityDungeon1004_MiniMain2_TodayTaskUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1004_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a4/ActivityDungeon1004_MiniMain2_TopByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniMain2_TopUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniMain2_TopUis(ui)
  local uis = {}
  
  uis.BookBtn = ui:GetChild("BookBtn")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniMain_BottonByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniMain_BottonUis
**Requires:**
- ActivityDungeon1004_MiniMain_TodayTaskByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniMain_TodayTaskByName")

function GetActivityDungeon1004_MiniMain_BottonUis(ui)
  local uis = {}
  uis.TaskBtn = ui:GetChild("TaskBtn")
  uis.RecordBtn = ui:GetChild("RecordBtn")
  uis.TodayTask = GetActivityDungeon1004_MiniMain_TodayTaskUis(ui:GetChild("TodayTask"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniMain_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniMain_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniMain_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniMain_RecordBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniMain_RecordBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniMain_RecordBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniMain_StartBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniMain_StartBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniMain_StartBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniMain_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniMain_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1004_MiniMain_TaskBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniMain_TodayTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniMain_TodayTaskUis
**Requires:**
- ActivityDungeon1004_PassReward_AllFrame_EByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("ActivityDungeon1004_PassReward_AllFrame_EByName")
require("CommonResource_RedDotByName")

function GetActivityDungeon1004_MiniMain_TodayTaskUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1004_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a4/ActivityDungeon1004_MiniMain_TopByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniMain_TopUis
**Requires:**
- ActivityDungeon1004_MiniMain_IntegralByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniMain_IntegralByName")

function GetActivityDungeon1004_MiniMain_TopUis(ui)
  local uis = {}
  uis.Integral = GetActivityDungeon1004_MiniMain_IntegralUis(ui:GetChild("Integral"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart2_BookBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart2_BookBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart2_BookBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart2_CloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart2_CloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart2_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart2_End1ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart2_End1Uis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart2_End1Uis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart2_End1WindowByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart2_End1WindowUis
**Requires:**
- ActivityDungeon1004_MiniStart2_End1ByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniStart2_End1ByName")

function GetActivityDungeon1004_MiniStart2_End1WindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1004_MiniStart2_End1Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart2_End2ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart2_End2Uis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart2_End2Uis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
```

---

## Activty/a4/ActivityDungeon1004_MiniStart2_End2WindowByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart2_End2WindowUis
**Requires:**
- ActivityDungeon1004_MiniStart2_End2ByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniStart2_End2ByName")

function GetActivityDungeon1004_MiniStart2_End2WindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1004_MiniStart2_End2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart2_HarvestByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart2_HarvestUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart2_HarvestUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart2_HarvestProgressBarByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart2_HarvestProgressBarUis
**Requires:**
- ActivityDungeon1004_MiniStart2_HarvestProgressFillByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniStart2_HarvestProgressFillByName")

function GetActivityDungeon1004_MiniStart2_HarvestProgressBarUis(ui)
  local uis = {}
  uis.bar = GetActivityDungeon1004_MiniStart2_HarvestProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart2_HarvestProgressFillByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart2_HarvestProgressFillUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart2_HarvestProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart2_NumberByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart2_NumberUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart2_NumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart2_NumberProgressBarByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart2_NumberProgressBarUis
**Requires:**
- ActivityDungeon1004_MiniStart2_NumberProgressFillByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniStart2_NumberProgressFillByName")

function GetActivityDungeon1004_MiniStart2_NumberProgressBarUis(ui)
  local uis = {}
  uis.bar = GetActivityDungeon1004_MiniStart2_NumberProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart2_NumberProgressFillByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart2_NumberProgressFillUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart2_NumberProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart2_Stage1BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart2_Stage1BtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart2_Stage1BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart2_Stage2BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart2_Stage2BtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart2_Stage2BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart2_Stage3BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart2_Stage3BtnUis
**Requires:**
- ActivityDungeon1004_MiniStart2_Stage3EffectByName
- ActivityDungeon1004_MiniStart2_Stage3WordByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniStart2_Stage3EffectByName")
require("ActivityDungeon1004_MiniStart2_Stage3WordByName")

function GetActivityDungeon1004_MiniStart2_Stage3BtnUis(ui)
  local uis = {}
  uis.Effect = GetActivityDungeon1004_MiniStart2_Stage3EffectUis(ui:GetChild("Effect"))
  uis.Word = GetActivityDungeon1004_MiniStart2_Stage3WordUis(ui:GetChild("Word"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## Activty/a4/ActivityDungeon1004_MiniStart2_Stage3EffectByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart2_Stage3EffectUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart2_Stage3EffectUis(ui)
  local uis = {}
  
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Effect3Holder = ui:GetChild("Effect3Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart2_Stage3WordByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart2_Stage3WordUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart2_Stage3WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart2_StageRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart2_StageRegionUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart2_StageRegionUis(ui)
  local uis = {}
  
  uis.Stage1Btn = ui:GetChild("Stage1Btn")
  uis.Stage2Btn = ui:GetChild("Stage2Btn")
  uis.Stage3Btn = ui:GetChild("Stage3Btn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart2_TopRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart2_TopRegionUis
**Requires:**
- ActivityDungeon1004_MiniStart2_HarvestByName
- ActivityDungeon1004_MiniStart2_NumberByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniStart2_HarvestByName")
require("ActivityDungeon1004_MiniStart2_NumberByName")

function GetActivityDungeon1004_MiniStart2_TopRegionUis(ui)
  local uis = {}
  uis.HarvestProgressBar = ui:GetChild("HarvestProgressBar")
  uis.NumberProgressBar = ui:GetChild("NumberProgressBar")
  uis.Harvest = GetActivityDungeon1004_MiniStart2_HarvestUis(ui:GetChild("Harvest"))
  uis.Number = GetActivityDungeon1004_MiniStart2_NumberUis(ui:GetChild("Number"))
  uis.BookBtn = ui:GetChild("BookBtn")
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_CloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_CloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_Condition1ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_Condition1Uis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart_Condition1Uis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_Condition2ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_Condition2Uis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart_Condition2Uis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_ConditionByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_ConditionUis
**Requires:**
- ActivityDungeon1004_MiniStart_Condition2ByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniStart_Condition2ByName")

function GetActivityDungeon1004_MiniStart_ConditionUis(ui)
  local uis = {}
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.Condition1List = ui:GetChild("Condition1List")
  uis.Condition2 = GetActivityDungeon1004_MiniStart_Condition2Uis(ui:GetChild("Condition2"))
  uis.root = ui
  return uis
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_EndAgainBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_EndAgainBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart_EndAgainBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_EndCloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_EndCloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart_EndCloseBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_EndFailByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_EndFailUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart_EndFailUis(ui)
  local uis = {}
  
  uis.NumberWordTxt = ui:GetChild("NumberWordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_EndItemByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_EndItemUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart_EndItemUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_EndRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_EndRewardUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1004_MiniStart_EndFailByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1004_MiniStart_EndFailByName")

function GetActivityDungeon1004_MiniStart_EndRewardUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.NumberWordTxt = ui:GetChild("NumberWordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.EndFail = GetActivityDungeon1004_MiniStart_EndFailUis(ui:GetChild("EndFail"))
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_EndRewardWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_EndRewardWindowUis
**Requires:**
- ActivityDungeon1004_MiniStart_EndRewardByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniStart_EndRewardByName")

function GetActivityDungeon1004_MiniStart_EndRewardWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1004_MiniStart_EndRewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart_IntegralUis(ui)
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

## Activty/a4/ActivityDungeon1004_MiniStart_Item01ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_Item01Uis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart_Item01Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_Item02ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_Item02Uis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart_Item02Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_Item03ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_Item03Uis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart_Item03Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_Item04ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_Item04Uis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart_Item04Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_Item05ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_Item05Uis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart_Item05Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_Item06ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_Item06Uis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart_Item06Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_Item07ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_Item07Uis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart_Item07Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_Item08ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_Item08Uis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart_Item08Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_LatticeByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_LatticeUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart_LatticeUis(ui)
  local uis = {}
  
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Effect3Holder = ui:GetChild("Effect3Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_LatticeEffectByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_LatticeEffectUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart_LatticeEffectUis(ui)
  local uis = {}
  
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Effect3Holder = ui:GetChild("Effect3Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_LatticeExchangeByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_LatticeExchangeUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart_LatticeExchangeUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_LatticeRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_LatticeRegionUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart_LatticeRegionUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_LatticeTipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_LatticeTipsAniUis
**Requires:**
- ActivityDungeon1004_MiniStart_LatticeTipsByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniStart_LatticeTipsByName")

function GetActivityDungeon1004_MiniStart_LatticeTipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1004_MiniStart_LatticeTipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_LatticeTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_LatticeTipsUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart_LatticeTipsUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_WinByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_WinUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart_WinUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_WinTargetByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_WinTargetUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniStart_WinTargetUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_WinTargetWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_WinTargetWindowUis
**Requires:**
- ActivityDungeon1004_MiniStart_WinTargetByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniStart_WinTargetByName")

function GetActivityDungeon1004_MiniStart_WinTargetWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1004_MiniStart_WinTargetUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniStart_WinWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniStart_WinWindowUis
**Requires:**
- ActivityDungeon1004_MiniStart_WinByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniStart_WinByName")

function GetActivityDungeon1004_MiniStart_WinWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1004_MiniStart_WinUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniTask2ByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniTask2Uis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1004_MiniTask2_IntegralByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1004_MiniTask2_IntegralByName")

function GetActivityDungeon1004_MiniTask2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Integral = GetActivityDungeon1004_MiniTask2_IntegralUis(ui:GetChild("Integral"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a4/ActivityDungeon1004_MiniTask2WindowByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniTask2WindowUis
**Requires:**
- ActivityDungeon1004_MiniTask2ByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniTask2ByName")

function GetActivityDungeon1004_MiniTask2WindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1004_MiniTask2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniTask2_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniTask2_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniTask2_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniTask2_RewardItemByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniTask2_RewardItemUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniTask2_RewardItemUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniTask2_RewardItemGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniTask2_RewardItemGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniTask2_RewardItemGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniTask2_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniTask2_TipsAniUis
**Requires:**
- ActivityDungeon1004_MiniTask2_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniTask2_TipsByName")

function GetActivityDungeon1004_MiniTask2_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1004_MiniTask2_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniTask2_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniTask2_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniTask2_TipsUis(ui)
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

## Activty/a4/ActivityDungeon1004_MiniTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniTaskUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1004_MiniTask_IntegralByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1004_MiniTask_IntegralByName")

function GetActivityDungeon1004_MiniTaskUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Integral = GetActivityDungeon1004_MiniTask_IntegralUis(ui:GetChild("Integral"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a4/ActivityDungeon1004_MiniTaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniTaskWindowUis
**Requires:**
- ActivityDungeon1004_MiniTaskByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniTaskByName")

function GetActivityDungeon1004_MiniTaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1004_MiniTaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniTask_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniTask_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniTask_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniTask_RewardItemByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniTask_RewardItemUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniTask_RewardItemUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniTask_RewardItemGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniTask_RewardItemGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniTask_RewardItemGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniTask_TipsAniUis
**Requires:**
- ActivityDungeon1004_MiniTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniTask_TipsByName")

function GetActivityDungeon1004_MiniTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1004_MiniTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_MiniTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1004_MiniTask_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1004_MiniTask_TipsUis(ui)
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

## Activty/a4/ActivityDungeon1004_NormalBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_NormalBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_NormalBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_NormalPoint1BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_NormalPoint1BtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_NormalPoint1BtnUis(ui)
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

## Activty/a4/ActivityDungeon1004_NormalPoint2BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_NormalPoint2BtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_NormalPoint2BtnUis(ui)
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

## Activty/a4/ActivityDungeon1004_NormalPoint3BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_NormalPoint3BtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_NormalPoint3BtnUis(ui)
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

## Activty/a4/ActivityDungeon1004_NormalPointBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_NormalPointBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_NormalPointBtnUis(ui)
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

## Activty/a4/ActivityDungeon1004_NormalPointLockByName.lua.lua
**Functions:**
- GetActivityDungeon1004_NormalPointLockUis
**Snippet:**
```lua
function GetActivityDungeon1004_NormalPointLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_NumberStripByName.lua.lua
**Functions:**
- GetActivityDungeon1004_NumberStripUis
**Snippet:**
```lua
function GetActivityDungeon1004_NumberStripUis(ui)
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

## Activty/a4/ActivityDungeon1004_PassBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1004_PassBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_PassClothes_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassClothes_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_PassClothes_BuyBtnUis(ui)
  local uis = {}
  
  uis.PriceTxt = ui:GetChild("PriceTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_PassClothes_BuyRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassClothes_BuyRewardUis
**Snippet:**
```lua
function GetActivityDungeon1004_PassClothes_BuyRewardUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_PassClothes_CardQBByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassClothes_CardQBUis
**Snippet:**
```lua
function GetActivityDungeon1004_PassClothes_CardQBUis(ui)
  local uis = {}
  
  uis.QBHolder = ui:GetChild("QBHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_PassClothes_ClothseRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassClothes_ClothseRegionUis
**Requires:**
- ActivityDungeon1004_PassClothes_WordByName
- ActivityDungeon1004_PassClothes_CardQBByName
- ActivityDungeon1004_PassClothes_BuyRewardByName
**Snippet:**
```lua
require("ActivityDungeon1004_PassClothes_WordByName")
require("ActivityDungeon1004_PassClothes_CardQBByName")
require("ActivityDungeon1004_PassClothes_BuyRewardByName")

function GetActivityDungeon1004_PassClothes_ClothseRegionUis(ui)
  local uis = {}
  uis.Word = GetActivityDungeon1004_PassClothes_WordUis(ui:GetChild("Word"))
  uis.CardQB = GetActivityDungeon1004_PassClothes_CardQBUis(ui:GetChild("CardQB"))
  uis.BuyReward = GetActivityDungeon1004_PassClothes_BuyRewardUis(ui:GetChild("BuyReward"))
  uis.BuyBtn = ui:GetChild("BuyBtn")
```

---

## Activty/a4/ActivityDungeon1004_PassClothes_NameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassClothes_NameBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_PassClothes_NameBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_PassClothes_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassClothes_WordUis
**Snippet:**
```lua
function GetActivityDungeon1004_PassClothes_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_PassportByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassportUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1004_PassReward_RewardRegionByName
- ActivityDungeon1004_PassTask_TaskRegionByName
- ActivityDungeon1004_PassClothes_ClothseRegionByName
- ActivityDungeon1004_Passport_LevelByName
- ActivityDungeon1004_Sign_TimeByName
- ActivityDungeon1004_Passport_TabRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1004_PassReward_RewardRegionByName")
require("ActivityDungeon1004_PassTask_TaskRegionByName")
require("ActivityDungeon1004_PassClothes_ClothseRegionByName")
require("ActivityDungeon1004_Passport_LevelByName")
require("ActivityDungeon1004_Sign_TimeByName")
require("ActivityDungeon1004_Passport_TabRegionByName")

function GetActivityDungeon1004_PassportUis(ui)
  local uis = {}
```

---

## Activty/a4/ActivityDungeon1004_PassportUp_LevelUpBgByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassportUp_LevelUpBgUis
**Snippet:**
```lua
function GetActivityDungeon1004_PassportUp_LevelUpBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_PassportUp_LevelUpTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassportUp_LevelUpTipsUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1004_PassportUp_LevelUpBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1004_PassportUp_LevelUpBgByName")

function GetActivityDungeon1004_PassportUp_LevelUpTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.LevelUpBg = GetActivityDungeon1004_PassportUp_LevelUpBgUis(ui:GetChild("LevelUpBg"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
```

---

## Activty/a4/ActivityDungeon1004_PassportUp_LevelUpTipsWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassportUp_LevelUpTipsWindowUis
**Requires:**
- ActivityDungeon1004_PassportUp_LevelUpTipsByName
**Snippet:**
```lua
require("ActivityDungeon1004_PassportUp_LevelUpTipsByName")

function GetActivityDungeon1004_PassportUp_LevelUpTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1004_PassportUp_LevelUpTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_PassportWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassportWindowUis
**Requires:**
- ActivityDungeon1004_PassportByName
**Snippet:**
```lua
require("ActivityDungeon1004_PassportByName")

function GetActivityDungeon1004_PassportWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1004_PassportUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Passport_AllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Passport_AllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_Passport_AllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Passport_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Passport_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_Passport_BuyBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Passport_ExpProgressBarByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Passport_ExpProgressBarUis
**Requires:**
- ActivityDungeon1004_Passport_ExpProgressFillByName
**Snippet:**
```lua
require("ActivityDungeon1004_Passport_ExpProgressFillByName")

function GetActivityDungeon1004_Passport_ExpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetActivityDungeon1004_Passport_ExpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Passport_ExpProgressFillByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Passport_ExpProgressFillUis
**Snippet:**
```lua
function GetActivityDungeon1004_Passport_ExpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Passport_LevelByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Passport_LevelUis
**Snippet:**
```lua
function GetActivityDungeon1004_Passport_LevelUis(ui)
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

## Activty/a4/ActivityDungeon1004_Passport_TabBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Passport_TabBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1004_Passport_TabBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## Activty/a4/ActivityDungeon1004_Passport_TabRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Passport_TabRegionUis
**Snippet:**
```lua
function GetActivityDungeon1004_Passport_TabRegionUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_PassReward_AllFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassReward_AllFrame_EUis
**Requires:**
- ActivityDungeon1004_PassReward_ItemFrame_EByName
- ActivityDungeon1004_PassReward_CardFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1004_PassReward_ItemFrame_EByName")
require("ActivityDungeon1004_PassReward_CardFrame_EByName")

function GetActivityDungeon1004_PassReward_AllFrame_EUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1004_PassReward_ItemFrame_EUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1004_PassReward_CardFrame_EUis(ui:GetChild("CardFrame"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## Activty/a4/ActivityDungeon1004_PassReward_AllFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassReward_AllFrame_MUis
**Requires:**
- ActivityDungeon1004_PassReward_ItemFrame_MByName
- ActivityDungeon1004_PassReward_CardFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1004_PassReward_ItemFrame_MByName")
require("ActivityDungeon1004_PassReward_CardFrame_MByName")

function GetActivityDungeon1004_PassReward_AllFrame_MUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1004_PassReward_ItemFrame_MUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1004_PassReward_CardFrame_MUis(ui:GetChild("CardFrame"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a4/ActivityDungeon1004_PassReward_CardFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassReward_CardFrame_EUis
**Requires:**
- ActivityDungeon1004_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1004_PassReward_ItemCardPicByName")

function GetActivityDungeon1004_PassReward_CardFrame_EUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1004_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a4/ActivityDungeon1004_PassReward_CardFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassReward_CardFrame_MUis
**Requires:**
- ActivityDungeon1004_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1004_PassReward_ItemCardPicByName")

function GetActivityDungeon1004_PassReward_CardFrame_MUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1004_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a4/ActivityDungeon1004_PassReward_EndTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassReward_EndTwoUis
**Requires:**
- ActivityDungeon1004_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1004_PassReward_AllFrame_EByName")

function GetActivityDungeon1004_PassReward_EndTwoUis(ui)
  local uis = {}
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.Item1 = GetActivityDungeon1004_PassReward_AllFrame_EUis(ui:GetChild("Item1"))
  uis.Item2 = GetActivityDungeon1004_PassReward_AllFrame_EUis(ui:GetChild("Item2"))
  uis.root = ui
```

---

## Activty/a4/ActivityDungeon1004_PassReward_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassReward_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1004_PassReward_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_PassReward_ItemFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassReward_ItemFrame_EUis
**Snippet:**
```lua
function GetActivityDungeon1004_PassReward_ItemFrame_EUis(ui)
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

## Activty/a4/ActivityDungeon1004_PassReward_ItemFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassReward_ItemFrame_MUis
**Snippet:**
```lua
function GetActivityDungeon1004_PassReward_ItemFrame_MUis(ui)
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

## Activty/a4/ActivityDungeon1004_PassReward_LevelTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassReward_LevelTitleUis
**Snippet:**
```lua
function GetActivityDungeon1004_PassReward_LevelTitleUis(ui)
  local uis = {}
  
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_PassReward_MiddleRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassReward_MiddleRegionUis
**Snippet:**
```lua
function GetActivityDungeon1004_PassReward_MiddleRegionUis(ui)
  local uis = {}
  
  uis.MiddleList = ui:GetChild("MiddleList")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_PassReward_MidTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassReward_MidTwoUis
**Requires:**
- ActivityDungeon1004_PassReward_MidTwoItemByName
- ActivityDungeon1004_PassReward_LevelTitleByName
**Snippet:**
```lua
require("ActivityDungeon1004_PassReward_MidTwoItemByName")
require("ActivityDungeon1004_PassReward_LevelTitleByName")

function GetActivityDungeon1004_PassReward_MidTwoUis(ui)
  local uis = {}
  uis.Reward1 = GetActivityDungeon1004_PassReward_MidTwoItemUis(ui:GetChild("Reward1"))
  uis.Reward2 = GetActivityDungeon1004_PassReward_MidTwoItemUis(ui:GetChild("Reward2"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Title = GetActivityDungeon1004_PassReward_LevelTitleUis(ui:GetChild("Title"))
```

---

## Activty/a4/ActivityDungeon1004_PassReward_MidTwoItemByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassReward_MidTwoItemUis
**Requires:**
- ActivityDungeon1004_PassReward_AllFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1004_PassReward_AllFrame_MByName")

function GetActivityDungeon1004_PassReward_MidTwoItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1004_PassReward_AllFrame_MUis(ui:GetChild("Item"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_PassReward_PicByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassReward_PicUis
**Snippet:**
```lua
function GetActivityDungeon1004_PassReward_PicUis(ui)
  local uis = {}
  
  uis.BuyTxt = ui:GetChild("BuyTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_PassReward_RewardRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassReward_RewardRegionUis
**Requires:**
- ActivityDungeon1004_PassReward_MiddleRegionByName
- ActivityDungeon1004_PassReward_StartTwoByName
- ActivityDungeon1004_PassReward_EndTwoByName
**Snippet:**
```lua
require("ActivityDungeon1004_PassReward_MiddleRegionByName")
require("ActivityDungeon1004_PassReward_StartTwoByName")
require("ActivityDungeon1004_PassReward_EndTwoByName")

function GetActivityDungeon1004_PassReward_RewardRegionUis(ui)
  local uis = {}
  uis.MiddleList = GetActivityDungeon1004_PassReward_MiddleRegionUis(ui:GetChild("MiddleList"))
  uis.StartTwo = GetActivityDungeon1004_PassReward_StartTwoUis(ui:GetChild("StartTwo"))
  uis.EndTwo = GetActivityDungeon1004_PassReward_EndTwoUis(ui:GetChild("EndTwo"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a4/ActivityDungeon1004_PassReward_StartTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassReward_StartTwoUis
**Requires:**
- ActivityDungeon1004_PassReward_PicByName
**Snippet:**
```lua
require("ActivityDungeon1004_PassReward_PicByName")

function GetActivityDungeon1004_PassReward_StartTwoUis(ui)
  local uis = {}
  uis.Pic = GetActivityDungeon1004_PassReward_PicUis(ui:GetChild("Pic"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_PassTask_TaskRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassTask_TaskRegionUis
**Requires:**
- ActivityDungeon1004_TaskMaxByName
**Snippet:**
```lua
require("ActivityDungeon1004_TaskMaxByName")

function GetActivityDungeon1004_PassTask_TaskRegionUis(ui)
  local uis = {}
  uis.TipsList = ui:GetChild("TipsList")
  uis.Max = GetActivityDungeon1004_TaskMaxUis(ui:GetChild("Max"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_PassTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassTask_TipsAniUis
**Requires:**
- ActivityDungeon1004_PassTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1004_PassTask_TipsByName")

function GetActivityDungeon1004_PassTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1004_PassTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_PassTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassTask_TipsUis
**Requires:**
- ActivityDungeon1004_PassTask_TipsIntegralByName
**Snippet:**
```lua
require("ActivityDungeon1004_PassTask_TipsIntegralByName")

function GetActivityDungeon1004_PassTask_TipsUis(ui)
  local uis = {}
  uis.ProgressTxt = ui:GetChild("ProgressTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Integral = GetActivityDungeon1004_PassTask_TipsIntegralUis(ui:GetChild("Integral"))
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a4/ActivityDungeon1004_PassTask_TipsIntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PassTask_TipsIntegralUis
**Snippet:**
```lua
function GetActivityDungeon1004_PassTask_TipsIntegralUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_PlotBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PlotBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_PlotBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_PlotByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PlotUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1004_Plot_WordByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1004_Plot_WordByName")

function GetActivityDungeon1004_PlotUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Word = GetActivityDungeon1004_Plot_WordUis(ui:GetChild("Word"))
  uis.PlotList = ui:GetChild("PlotList")
  uis.ProspectBtn = ui:GetChild("ProspectBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a4/ActivityDungeon1004_PlotWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1004_PlotWindowUis
**Requires:**
- ActivityDungeon1004_PlotByName
**Snippet:**
```lua
require("ActivityDungeon1004_PlotByName")

function GetActivityDungeon1004_PlotWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1004_PlotUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Plot_ProspectBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Plot_ProspectBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_Plot_ProspectBtnUis(ui)
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

## Activty/a4/ActivityDungeon1004_Plot_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Plot_TipsAniUis
**Requires:**
- ActivityDungeon1004_Plot_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1004_Plot_TipsByName")

function GetActivityDungeon1004_Plot_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1004_Plot_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Plot_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Plot_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1004_Plot_TipsUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Plot_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Plot_WordUis
**Snippet:**
```lua
function GetActivityDungeon1004_Plot_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_ReduceBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_ReduceBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_ReduceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_ShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_ShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_ShopBtnUis(ui)
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

## Activty/a4/ActivityDungeon1004_ShopByName.lua.lua
**Functions:**
- GetActivityDungeon1004_ShopUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1004_Shop_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1004_Shop_TimeByName")

function GetActivityDungeon1004_ShopUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Time = GetActivityDungeon1004_Shop_TimeUis(ui:GetChild("Time"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a4/ActivityDungeon1004_ShopWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1004_ShopWindowUis
**Requires:**
- ActivityDungeon1004_ShopByName
**Snippet:**
```lua
require("ActivityDungeon1004_ShopByName")

function GetActivityDungeon1004_ShopWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1004_ShopUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Shop_CardHeadBgByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Shop_CardHeadBgUis
**Snippet:**
```lua
function GetActivityDungeon1004_Shop_CardHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Shop_ItemAniByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Shop_ItemAniUis
**Requires:**
- ActivityDungeon1004_Shop_ItemByName
**Snippet:**
```lua
require("ActivityDungeon1004_Shop_ItemByName")

function GetActivityDungeon1004_Shop_ItemAniUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1004_Shop_ItemUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Shop_ItemBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Shop_ItemBtnUis
**Requires:**
- ActivityDungeon1004_Shop_CardHeadBgByName
- ActivityDungeon1004_Shop_ItemNumberByName
- ActivityDungeon1004_Shop_UseMarkByName
**Snippet:**
```lua
require("ActivityDungeon1004_Shop_CardHeadBgByName")
require("ActivityDungeon1004_Shop_ItemNumberByName")
require("ActivityDungeon1004_Shop_UseMarkByName")

function GetActivityDungeon1004_Shop_ItemBtnUis(ui)
  local uis = {}
  uis.CardHeadBg = GetActivityDungeon1004_Shop_CardHeadBgUis(ui:GetChild("CardHeadBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.ItemNumber = GetActivityDungeon1004_Shop_ItemNumberUis(ui:GetChild("ItemNumber"))
```

---

## Activty/a4/ActivityDungeon1004_Shop_ItemByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Shop_ItemUis
**Requires:**
- ActivityDungeon1004_Shop_SellOutByName
**Snippet:**
```lua
require("ActivityDungeon1004_Shop_SellOutByName")

function GetActivityDungeon1004_Shop_ItemUis(ui)
  local uis = {}
  uis.ItemBtn = ui:GetChild("ItemBtn")
  uis.SellOut = GetActivityDungeon1004_Shop_SellOutUis(ui:GetChild("SellOut"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Shop_ItemNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Shop_ItemNumberUis
**Snippet:**
```lua
function GetActivityDungeon1004_Shop_ItemNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Shop_ItemRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Shop_ItemRegionUis
**Requires:**
- ActivityDungeon1004_Shop_TitleByName
**Snippet:**
```lua
require("ActivityDungeon1004_Shop_TitleByName")

function GetActivityDungeon1004_Shop_ItemRegionUis(ui)
  local uis = {}
  uis.ShopTitle = GetActivityDungeon1004_Shop_TitleUis(ui:GetChild("ShopTitle"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Shop_SellOutByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Shop_SellOutUis
**Snippet:**
```lua
function GetActivityDungeon1004_Shop_SellOutUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Shop_StarByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Shop_StarUis
**Snippet:**
```lua
function GetActivityDungeon1004_Shop_StarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Shop_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Shop_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1004_Shop_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Shop_TitleByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Shop_TitleUis
**Snippet:**
```lua
function GetActivityDungeon1004_Shop_TitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Shop_UseMarkByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Shop_UseMarkUis
**Snippet:**
```lua
function GetActivityDungeon1004_Shop_UseMarkUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_SignBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_SignBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1004_SignBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_SignByName.lua.lua
**Functions:**
- GetActivityDungeon1004_SignUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1004_Sign_RewardListByName
- ActivityDungeon1004_Sign_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1004_Sign_RewardListByName")
require("ActivityDungeon1004_Sign_TimeByName")

function GetActivityDungeon1004_SignUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.RewardList = GetActivityDungeon1004_Sign_RewardListUis(ui:GetChild("RewardList"))
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.Time = GetActivityDungeon1004_Sign_TimeUis(ui:GetChild("Time"))
```

---

## Activty/a4/ActivityDungeon1004_SignWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1004_SignWindowUis
**Requires:**
- ActivityDungeon1004_SignByName
**Snippet:**
```lua
require("ActivityDungeon1004_SignByName")

function GetActivityDungeon1004_SignWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1004_SignUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Sign_AllFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Sign_AllFrameUis
**Requires:**
- ActivityDungeon1004_Sign_ItemFrameByName
- ActivityDungeon1004_Sign_CardFrameByName
**Snippet:**
```lua
require("ActivityDungeon1004_Sign_ItemFrameByName")
require("ActivityDungeon1004_Sign_CardFrameByName")

function GetActivityDungeon1004_Sign_AllFrameUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1004_Sign_ItemFrameUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1004_Sign_CardFrameUis(ui:GetChild("CardFrame"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a4/ActivityDungeon1004_Sign_CardFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Sign_CardFrameUis
**Requires:**
- ActivityDungeon1004_Sign_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1004_Sign_ItemCardPicByName")

function GetActivityDungeon1004_Sign_CardFrameUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1004_Sign_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a4/ActivityDungeon1004_Sign_GetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Sign_GetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_Sign_GetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Sign_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Sign_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1004_Sign_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Sign_ItemFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Sign_ItemFrameUis
**Snippet:**
```lua
function GetActivityDungeon1004_Sign_ItemFrameUis(ui)
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

## Activty/a4/ActivityDungeon1004_Sign_RewardAniByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Sign_RewardAniUis
**Requires:**
- ActivityDungeon1004_Sign_RewardByName
**Snippet:**
```lua
require("ActivityDungeon1004_Sign_RewardByName")

function GetActivityDungeon1004_Sign_RewardAniUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1004_Sign_RewardUis(ui:GetChild("Reward"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Sign_RewardByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Sign_RewardUis
**Requires:**
- ActivityDungeon1004_Sign_AllFrameByName
**Snippet:**
```lua
require("ActivityDungeon1004_Sign_AllFrameByName")

function GetActivityDungeon1004_Sign_RewardUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1004_Sign_AllFrameUis(ui:GetChild("Item"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Sign_RewardListByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Sign_RewardListUis
**Snippet:**
```lua
function GetActivityDungeon1004_Sign_RewardListUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_Sign_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1004_Sign_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1004_Sign_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_TaskAllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_TaskAllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_TaskAllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1004_TaskBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_TaskByName.lua.lua
**Functions:**
- GetActivityDungeon1004_TaskUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1004_TaskTitleByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1004_TaskTitleByName")

function GetActivityDungeon1004_TaskUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TaskTitle = GetActivityDungeon1004_TaskTitleUis(ui:GetChild("TaskTitle"))
  uis.TaskTipsList = ui:GetChild("TaskTipsList")
  uis.AllGetBtn = ui:GetChild("AllGetBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a4/ActivityDungeon1004_TaskGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1004_TaskGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1004_TaskGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_TaskMaxByName.lua.lua
**Functions:**
- GetActivityDungeon1004_TaskMaxUis
**Snippet:**
```lua
function GetActivityDungeon1004_TaskMaxUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_TaskProgressByName.lua.lua
**Functions:**
- GetActivityDungeon1004_TaskProgressUis
**Snippet:**
```lua
function GetActivityDungeon1004_TaskProgressUis(ui)
  local uis = {}
  
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_TaskTipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1004_TaskTipsAniUis
**Requires:**
- ActivityDungeon1004_TaskTipsByName
**Snippet:**
```lua
require("ActivityDungeon1004_TaskTipsByName")

function GetActivityDungeon1004_TaskTipsAniUis(ui)
  local uis = {}
  uis.TaskTips = GetActivityDungeon1004_TaskTipsUis(ui:GetChild("TaskTips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_TaskTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1004_TaskTipsUis
**Requires:**
- ActivityDungeon1004_TaskProgressByName
**Snippet:**
```lua
require("ActivityDungeon1004_TaskProgressByName")

function GetActivityDungeon1004_TaskTipsUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.RewardList = ui:GetChild("RewardList")
  uis.TaskProgress = GetActivityDungeon1004_TaskProgressUis(ui:GetChild("TaskProgress"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a4/ActivityDungeon1004_TaskTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1004_TaskTitleUis
**Snippet:**
```lua
function GetActivityDungeon1004_TaskTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a4/ActivityDungeon1004_TaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1004_TaskWindowUis
**Requires:**
- ActivityDungeon1004_TaskByName
**Snippet:**
```lua
require("ActivityDungeon1004_TaskByName")

function GetActivityDungeon1004_TaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1004_TaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---
