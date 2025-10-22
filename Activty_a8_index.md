# Activty/a8

## Activty/a8/ActivityDungeon1008_ActivityDungeonByName.lua.lua
**Functions:**
- GetActivityDungeon1008_ActivityDungeonUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1008_MainTitleByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1008_MainTitleByName")
require("CommonResource_CurrencyReturnByName")

function GetActivityDungeon1008_ActivityDungeonUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.MainTitle = GetActivityDungeon1008_MainTitleUis(ui:GetChild("MainTitle"))
  uis.MiniGame1Btn = ui:GetChild("MiniGame1Btn")
  uis.MiniGameBtn = ui:GetChild("MiniGameBtn")
```

---

## Activty/a8/ActivityDungeon1008_ActivityDungeonWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1008_ActivityDungeonWindowUis
**Requires:**
- ActivityDungeon1008_ActivityDungeonByName
**Snippet:**
```lua
require("ActivityDungeon1008_ActivityDungeonByName")

function GetActivityDungeon1008_ActivityDungeonWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1008_ActivityDungeonUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_AddBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_AddBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_AddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_BossBattleByName.lua.lua
**Functions:**
- GetActivityDungeon1008_BossBattleUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1008_BossBattle_InfoByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1008_BossBattle_InfoByName")

function GetActivityDungeon1008_BossBattleUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.Info = GetActivityDungeon1008_BossBattle_InfoUis(ui:GetChild("Info"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a8/ActivityDungeon1008_BossBattleWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1008_BossBattleWindowUis
**Requires:**
- ActivityDungeon1008_BossBattleByName
**Snippet:**
```lua
require("ActivityDungeon1008_BossBattleByName")

function GetActivityDungeon1008_BossBattleWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1008_BossBattleUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_BossBattle_Info1ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_BossBattle_Info1Uis
**Snippet:**
```lua
function GetActivityDungeon1008_BossBattle_Info1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_BossBattle_InfoByName.lua.lua
**Functions:**
- GetActivityDungeon1008_BossBattle_InfoUis
**Requires:**
- ActivityDungeon1008_BossBattle_Info1ByName
**Snippet:**
```lua
require("ActivityDungeon1008_BossBattle_Info1ByName")

function GetActivityDungeon1008_BossBattle_InfoUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = GetActivityDungeon1008_BossBattle_Info1Uis(ui:GetChild("WordTxt"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_BossBattle_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1008_BossBattle_TipsAniUis
**Requires:**
- ActivityDungeon1008_BossBattle_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1008_BossBattle_TipsByName")

function GetActivityDungeon1008_BossBattle_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1008_BossBattle_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_BossBattle_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1008_BossBattle_TipsUis
**Requires:**
- ActivityDungeon1008_BossBattle_TipsRewardByName
**Snippet:**
```lua
require("ActivityDungeon1008_BossBattle_TipsRewardByName")

function GetActivityDungeon1008_BossBattle_TipsUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1008_BossBattle_TipsRewardUis(ui:GetChild("Reward"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.NumberWordTxt = ui:GetChild("NumberWordTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a8/ActivityDungeon1008_BossBattle_TipsRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1008_BossBattle_TipsRewardUis
**Snippet:**
```lua
function GetActivityDungeon1008_BossBattle_TipsRewardUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_BossBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_BossBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1008_BossBtnUis(ui)
  local uis = {}
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.newCtr = ui:GetController("new")
```

---

## Activty/a8/ActivityDungeon1008_BoxBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_BoxBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_BoxBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_BuyLevelBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_BuyLevelBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_BuyLevelBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_BuyLevelDes1ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_BuyLevelDes1Uis
**Requires:**
- ActivityDungeon1008_NumberStripByName
- ActivityDungeon1008_BuyPriceNumberByName
**Snippet:**
```lua
require("ActivityDungeon1008_NumberStripByName")
require("ActivityDungeon1008_BuyPriceNumberByName")

function GetActivityDungeon1008_BuyLevelDes1Uis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.NumberStrip = GetActivityDungeon1008_NumberStripUis(ui:GetChild("NumberStrip"))
  uis.BuyPriceNumber = GetActivityDungeon1008_BuyPriceNumberUis(ui:GetChild("BuyPriceNumber"))
```

---

## Activty/a8/ActivityDungeon1008_BuyLevelDes2ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_BuyLevelDes2Uis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1008_BuyLevelDes1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1008_BuyLevelDes1ByName")

function GetActivityDungeon1008_BuyLevelDes2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.BuyLevelDes1 = GetActivityDungeon1008_BuyLevelDes1Uis(ui:GetChild("BuyLevelDes1"))
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.root = ui
```

---

## Activty/a8/ActivityDungeon1008_BuyLevelDesWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1008_BuyLevelDesWindowUis
**Requires:**
- ActivityDungeon1008_BuyLevelDes2ByName
**Snippet:**
```lua
require("ActivityDungeon1008_BuyLevelDes2ByName")

function GetActivityDungeon1008_BuyLevelDesWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1008_BuyLevelDes2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_BuyLevelItemByName.lua.lua
**Functions:**
- GetActivityDungeon1008_BuyLevelItemUis
**Requires:**
- ActivityDungeon1008_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1008_PassReward_AllFrame_EByName")

function GetActivityDungeon1008_BuyLevelItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1008_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_BuyPriceNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1008_BuyPriceNumberUis
**Snippet:**
```lua
function GetActivityDungeon1008_BuyPriceNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_ChallengeByName.lua.lua
**Functions:**
- GetActivityDungeon1008_ChallengeUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1008_MapListByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1008_MapListByName")

function GetActivityDungeon1008_ChallengeUis(ui)
  local uis = {}
  uis.BgList = ui:GetChild("BgList")
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Map = GetActivityDungeon1008_MapListUis(ui:GetChild("Map"))
  uis.ShopBtn = ui:GetChild("ShopBtn")
  uis.ChapterList = ui:GetChild("ChapterList")
```

---

## Activty/a8/ActivityDungeon1008_ChallengeChapterBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_ChallengeChapterBtnUis
**Requires:**
- ActivityDungeon1008_NormalPointLockByName
**Snippet:**
```lua
require("ActivityDungeon1008_NormalPointLockByName")

function GetActivityDungeon1008_ChallengeChapterBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Lock = GetActivityDungeon1008_NormalPointLockUis(ui:GetChild("Lock"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Activty/a8/ActivityDungeon1008_ChallengeShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_ChallengeShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_ChallengeShopBtnUis(ui)
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

## Activty/a8/ActivityDungeon1008_ChallengeWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1008_ChallengeWindowUis
**Requires:**
- ActivityDungeon1008_ChallengeByName
**Snippet:**
```lua
require("ActivityDungeon1008_ChallengeByName")

function GetActivityDungeon1008_ChallengeWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1008_ChallengeUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_EventTipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1008_EventTipsAniUis
**Requires:**
- ActivityDungeon1008_EventTipsByName
**Snippet:**
```lua
require("ActivityDungeon1008_EventTipsByName")

function GetActivityDungeon1008_EventTipsAniUis(ui)
  local uis = {}
  uis.EventTips = GetActivityDungeon1008_EventTipsUis(ui:GetChild("EventTips"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_EventTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1008_EventTipsUis
**Snippet:**
```lua
function GetActivityDungeon1008_EventTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_EventTipsListByName.lua.lua
**Functions:**
- GetActivityDungeon1008_EventTipsListUis
**Snippet:**
```lua
function GetActivityDungeon1008_EventTipsListUis(ui)
  local uis = {}
  
  uis.EventTipsList = ui:GetChild("EventTipsList")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MainBuildSignByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MainBuildSignUis
**Snippet:**
```lua
function GetActivityDungeon1008_MainBuildSignUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MainSeasonsByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MainSeasonsUis
**Snippet:**
```lua
function GetActivityDungeon1008_MainSeasonsUis(ui)
  local uis = {}
  
  uis.BackGroundHolder = ui:GetChild("BackGroundHolder")
  uis.BackGround1Holder = ui:GetChild("BackGround1Holder")
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MainSeasonsWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MainSeasonsWindowUis
**Requires:**
- ActivityDungeon1008_MainSeasonsByName
**Snippet:**
```lua
require("ActivityDungeon1008_MainSeasonsByName")

function GetActivityDungeon1008_MainSeasonsWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1008_MainSeasonsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MainTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MainTitleUis
**Snippet:**
```lua
function GetActivityDungeon1008_MainTitleUis(ui)
  local uis = {}
  
  uis.Time1Txt = ui:GetChild("Time1Txt")
  uis.Time2Txt = ui:GetChild("Time2Txt")
  uis.reviewCtr = ui:GetController("review")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MapBottom_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MapBottom_1Uis
**Snippet:**
```lua
function GetActivityDungeon1008_MapBottom_1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MapBottom_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MapBottom_2Uis
**Snippet:**
```lua
function GetActivityDungeon1008_MapBottom_2Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MapBottom_3ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MapBottom_3Uis
**Snippet:**
```lua
function GetActivityDungeon1008_MapBottom_3Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MapBottom_4ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MapBottom_4Uis
**Snippet:**
```lua
function GetActivityDungeon1008_MapBottom_4Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MapListByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MapListUis
**Snippet:**
```lua
function GetActivityDungeon1008_MapListUis(ui)
  local uis = {}
  
  uis.MapList = ui:GetChild("MapList")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Map_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Map_1Uis
**Snippet:**
```lua
function GetActivityDungeon1008_Map_1Uis(ui)
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

## Activty/a8/ActivityDungeon1008_Map_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Map_2Uis
**Snippet:**
```lua
function GetActivityDungeon1008_Map_2Uis(ui)
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

## Activty/a8/ActivityDungeon1008_Map_3ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Map_3Uis
**Snippet:**
```lua
function GetActivityDungeon1008_Map_3Uis(ui)
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

## Activty/a8/ActivityDungeon1008_Map_4ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Map_4Uis
**Snippet:**
```lua
function GetActivityDungeon1008_Map_4Uis(ui)
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

## Activty/a8/ActivityDungeon1008_MaterialBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MaterialBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1008_MaterialBtnUis(ui)
  local uis = {}
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
```

---

## Activty/a8/ActivityDungeon1008_MaterialByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MaterialUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1008_Material_BattleNumberByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1008_Material_BattleNumberByName")

function GetActivityDungeon1008_MaterialUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.BattleNumber = GetActivityDungeon1008_Material_BattleNumberUis(ui:GetChild("BattleNumber"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a8/ActivityDungeon1008_MaterialWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MaterialWindowUis
**Requires:**
- ActivityDungeon1008_MaterialByName
**Snippet:**
```lua
require("ActivityDungeon1008_MaterialByName")

function GetActivityDungeon1008_MaterialWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1008_MaterialUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Material_BattleAniByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Material_BattleAniUis
**Requires:**
- ActivityDungeon1008_Material_BattleByName
**Snippet:**
```lua
require("ActivityDungeon1008_Material_BattleByName")

function GetActivityDungeon1008_Material_BattleAniUis(ui)
  local uis = {}
  uis.Battle = GetActivityDungeon1008_Material_BattleUis(ui:GetChild("Battle"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Material_BattleByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Material_BattleUis
**Snippet:**
```lua
function GetActivityDungeon1008_Material_BattleUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Material_BattleNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Material_BattleNumberUis
**Snippet:**
```lua
function GetActivityDungeon1008_Material_BattleNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MaxBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MaxBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_MaxBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MinBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MinBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_MinBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniGame1BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniGame1BtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1008_MiniGame1BtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniGame2ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniGame2Uis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1008_MiniMain2_TopByName
- ActivityDungeon1008_MiniMain2_BottonByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1008_MiniMain2_TopByName")
require("ActivityDungeon1008_MiniMain2_BottonByName")

function GetActivityDungeon1008_MiniGame2Uis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Top = GetActivityDungeon1008_MiniMain2_TopUis(ui:GetChild("Top"))
  uis.Botton = GetActivityDungeon1008_MiniMain2_BottonUis(ui:GetChild("Botton"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a8/ActivityDungeon1008_MiniGame2WindowByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniGame2WindowUis
**Requires:**
- ActivityDungeon1008_MiniGame2ByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniGame2ByName")

function GetActivityDungeon1008_MiniGame2WindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1008_MiniGame2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniGameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniGameBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1008_MiniGameBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniGameByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniGameUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1008_MiniMain_TopByName
- ActivityDungeon1008_MiniMain_BottonByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1008_MiniMain_TopByName")
require("ActivityDungeon1008_MiniMain_BottonByName")

function GetActivityDungeon1008_MiniGameUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Top = GetActivityDungeon1008_MiniMain_TopUis(ui:GetChild("Top"))
  uis.Botton = GetActivityDungeon1008_MiniMain_BottonUis(ui:GetChild("Botton"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a8/ActivityDungeon1008_MiniGameChoiceByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniGameChoiceUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetActivityDungeon1008_MiniGameChoiceUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.StartBtn = ui:GetChild("StartBtn")
  uis.OperateBtn = ui:GetChild("OperateBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a8/ActivityDungeon1008_MiniGameChoiceWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniGameChoiceWindowUis
**Requires:**
- ActivityDungeon1008_MiniGameChoiceByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniGameChoiceByName")

function GetActivityDungeon1008_MiniGameChoiceWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1008_MiniGameChoiceUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniGameChoice_OperateBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniGameChoice_OperateBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniGameChoice_OperateBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniGameChoice_StartBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniGameChoice_StartBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniGameChoice_StartBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniGameChoice_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniGameChoice_TipsAniUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniGameChoice_TipsAniUis(ui)
  local uis = {}
  
  uis.TipsBtn = ui:GetChild("TipsBtn")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniGameChoice_TipsBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniGameChoice_TipsBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniGameChoice_TipsBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.mapCtr = ui:GetController("map")
  uis.root = ui
  return uis
```

---

## Activty/a8/ActivityDungeon1008_MiniGameStart2ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniGameStart2Uis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1008_MiniStart2_MapRegionByName
- ActivityDungeon1008_MiniStart2_IntegralByName
- ActivityDungeon1008_MiniStart_Joystick1ByName
- ActivityDungeon1008_MiniStart_Joystick3ByName
- ActivityDungeon1008_MiniStart_Joystick2ByName
- ActivityDungeon1008_MiniStart2_TipsWordByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1008_MiniStart2_MapRegionByName")
require("ActivityDungeon1008_MiniStart2_IntegralByName")
require("ActivityDungeon1008_MiniStart_Joystick1ByName")
require("ActivityDungeon1008_MiniStart_Joystick3ByName")
require("ActivityDungeon1008_MiniStart_Joystick2ByName")
require("ActivityDungeon1008_MiniStart2_TipsWordByName")

function GetActivityDungeon1008_MiniGameStart2Uis(ui)
  local uis = {}
```

---

## Activty/a8/ActivityDungeon1008_MiniGameStart2WindowByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniGameStart2WindowUis
**Requires:**
- ActivityDungeon1008_MiniGameStart2ByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniGameStart2ByName")

function GetActivityDungeon1008_MiniGameStart2WindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1008_MiniGameStart2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniGameStartByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniGameStartUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1008_MiniStart_MapRegionByName
- ActivityDungeon1008_MiniStart_IntegralByName
- ActivityDungeon1008_MiniStart_Info1ByName
- ActivityDungeon1008_MiniStart_Info2ByName
- ActivityDungeon1008_MiniStart_Joystick1ByName
- ActivityDungeon1008_MiniStart_Joystick3ByName
- ActivityDungeon1008_MiniStart_Joystick2ByName
- ActivityDungeon1008_MiniStart_EffectTipsAniByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1008_MiniStart_MapRegionByName")
require("ActivityDungeon1008_MiniStart_IntegralByName")
require("ActivityDungeon1008_MiniStart_Info1ByName")
require("ActivityDungeon1008_MiniStart_Info2ByName")
require("ActivityDungeon1008_MiniStart_Joystick1ByName")
require("ActivityDungeon1008_MiniStart_Joystick3ByName")
require("ActivityDungeon1008_MiniStart_Joystick2ByName")
require("ActivityDungeon1008_MiniStart_EffectTipsAniByName")

```

---

## Activty/a8/ActivityDungeon1008_MiniGameStartWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniGameStartWindowUis
**Requires:**
- ActivityDungeon1008_MiniGameStartByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniGameStartByName")

function GetActivityDungeon1008_MiniGameStartWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1008_MiniGameStartUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniGameWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniGameWindowUis
**Requires:**
- ActivityDungeon1008_MiniGameByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniGameByName")

function GetActivityDungeon1008_MiniGameWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1008_MiniGameUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniGame_Map01ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniGame_Map01Uis
**Requires:**
- ActivityDungeon1008_MiniStart_GateByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniStart_GateByName")

function GetActivityDungeon1008_MiniGame_Map01Uis(ui)
  local uis = {}
  uis.Gate = GetActivityDungeon1008_MiniStart_GateUis(ui:GetChild("Gate"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniGame_Map02ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniGame_Map02Uis
**Requires:**
- ActivityDungeon1008_MiniStart_GateByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniStart_GateByName")

function GetActivityDungeon1008_MiniGame_Map02Uis(ui)
  local uis = {}
  uis.Gate = GetActivityDungeon1008_MiniStart_GateUis(ui:GetChild("Gate"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniGame_Map03ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniGame_Map03Uis
**Requires:**
- ActivityDungeon1008_MiniStart_GateByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniStart_GateByName")

function GetActivityDungeon1008_MiniGame_Map03Uis(ui)
  local uis = {}
  uis.Gate = GetActivityDungeon1008_MiniStart_GateUis(ui:GetChild("Gate"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniGame_Map04ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniGame_Map04Uis
**Requires:**
- ActivityDungeon1008_MiniStart_GateByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniStart_GateByName")

function GetActivityDungeon1008_MiniGame_Map04Uis(ui)
  local uis = {}
  uis.Gate = GetActivityDungeon1008_MiniStart_GateUis(ui:GetChild("Gate"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniGame_Map05ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniGame_Map05Uis
**Requires:**
- ActivityDungeon1008_MiniStart_GateByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniStart_GateByName")

function GetActivityDungeon1008_MiniGame_Map05Uis(ui)
  local uis = {}
  uis.Gate = GetActivityDungeon1008_MiniStart_GateUis(ui:GetChild("Gate"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniGame_Map06ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniGame_Map06Uis
**Requires:**
- ActivityDungeon1008_MiniStart_GateByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniStart_GateByName")

function GetActivityDungeon1008_MiniGame_Map06Uis(ui)
  local uis = {}
  uis.Gate = GetActivityDungeon1008_MiniStart_GateUis(ui:GetChild("Gate"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniGame_Map07ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniGame_Map07Uis
**Requires:**
- ActivityDungeon1008_MiniStart_GateByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniStart_GateByName")

function GetActivityDungeon1008_MiniGame_Map07Uis(ui)
  local uis = {}
  uis.Gate = GetActivityDungeon1008_MiniStart_GateUis(ui:GetChild("Gate"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniGame_Map08ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniGame_Map08Uis
**Requires:**
- ActivityDungeon1008_MiniStart_GateByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniStart_GateByName")

function GetActivityDungeon1008_MiniGame_Map08Uis(ui)
  local uis = {}
  uis.Gate = GetActivityDungeon1008_MiniStart_GateUis(ui:GetChild("Gate"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniIntegral2ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniIntegral2Uis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetActivityDungeon1008_MiniIntegral2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
  return uis
```

---

## Activty/a8/ActivityDungeon1008_MiniIntegral2WindowByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniIntegral2WindowUis
**Requires:**
- ActivityDungeon1008_MiniIntegral2ByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniIntegral2ByName")

function GetActivityDungeon1008_MiniIntegral2WindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1008_MiniIntegral2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniIntegral2_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniIntegral2_TipsAniUis
**Requires:**
- ActivityDungeon1008_MiniIntegral2_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniIntegral2_TipsByName")

function GetActivityDungeon1008_MiniIntegral2_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1008_MiniIntegral2_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniIntegral2_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniIntegral2_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniIntegral2_TipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniIntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniIntegralUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetActivityDungeon1008_MiniIntegralUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
  return uis
```

---

## Activty/a8/ActivityDungeon1008_MiniIntegralWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniIntegralWindowUis
**Requires:**
- ActivityDungeon1008_MiniIntegralByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniIntegralByName")

function GetActivityDungeon1008_MiniIntegralWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1008_MiniIntegralUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniIntegral_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniIntegral_TipsAniUis
**Requires:**
- ActivityDungeon1008_MiniIntegral_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniIntegral_TipsByName")

function GetActivityDungeon1008_MiniIntegral_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1008_MiniIntegral_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniIntegral_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniIntegral_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniIntegral_TipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniMain2_BottonByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniMain2_BottonUis
**Requires:**
- ActivityDungeon1008_MiniMain2_TodayTaskByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniMain2_TodayTaskByName")

function GetActivityDungeon1008_MiniMain2_BottonUis(ui)
  local uis = {}
  uis.TaskBtn = ui:GetChild("TaskBtn")
  uis.RecordBtn = ui:GetChild("RecordBtn")
  uis.TodayTask = GetActivityDungeon1008_MiniMain2_TodayTaskUis(ui:GetChild("TodayTask"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniMain2_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniMain2_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniMain2_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniMain2_RecordBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniMain2_RecordBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniMain2_RecordBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniMain2_StartBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniMain2_StartBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniMain2_StartBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniMain2_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniMain2_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1008_MiniMain2_TaskBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniMain2_TodayTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniMain2_TodayTaskUis
**Requires:**
- ActivityDungeon1008_PassReward_AllFrame_EByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("ActivityDungeon1008_PassReward_AllFrame_EByName")
require("CommonResource_RedDotByName")

function GetActivityDungeon1008_MiniMain2_TodayTaskUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1008_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a8/ActivityDungeon1008_MiniMain2_TopByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniMain2_TopUis
**Requires:**
- ActivityDungeon1008_MiniMain2_IntegralByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniMain2_IntegralByName")

function GetActivityDungeon1008_MiniMain2_TopUis(ui)
  local uis = {}
  uis.Integral = GetActivityDungeon1008_MiniMain2_IntegralUis(ui:GetChild("Integral"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniMain_BottonByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniMain_BottonUis
**Requires:**
- ActivityDungeon1008_MiniMain_TodayTaskByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniMain_TodayTaskByName")

function GetActivityDungeon1008_MiniMain_BottonUis(ui)
  local uis = {}
  uis.TaskBtn = ui:GetChild("TaskBtn")
  uis.RecordBtn = ui:GetChild("RecordBtn")
  uis.TodayTask = GetActivityDungeon1008_MiniMain_TodayTaskUis(ui:GetChild("TodayTask"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniMain_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniMain_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniMain_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniMain_RecordBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniMain_RecordBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniMain_RecordBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniMain_StartBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniMain_StartBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniMain_StartBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniMain_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniMain_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1008_MiniMain_TaskBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniMain_TodayTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniMain_TodayTaskUis
**Requires:**
- ActivityDungeon1008_PassReward_AllFrame_EByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("ActivityDungeon1008_PassReward_AllFrame_EByName")
require("CommonResource_RedDotByName")

function GetActivityDungeon1008_MiniMain_TodayTaskUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1008_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a8/ActivityDungeon1008_MiniMain_TopByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniMain_TopUis
**Requires:**
- ActivityDungeon1008_MiniMain_IntegralByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniMain_IntegralByName")

function GetActivityDungeon1008_MiniMain_TopUis(ui)
  local uis = {}
  uis.Integral = GetActivityDungeon1008_MiniMain_IntegralUis(ui:GetChild("Integral"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniOperateChoiceByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniOperateChoiceUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetActivityDungeon1008_MiniOperateChoiceUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.TipsList = ui:GetChild("TipsList")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.root = ui
  return uis
```

---

## Activty/a8/ActivityDungeon1008_MiniOperateChoiceWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniOperateChoiceWindowUis
**Requires:**
- ActivityDungeon1008_MiniOperateChoiceByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniOperateChoiceByName")

function GetActivityDungeon1008_MiniOperateChoiceWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1008_MiniOperateChoiceUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniOperateChoice_CloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniOperateChoice_CloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniOperateChoice_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniOperateChoice_TipsBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniOperateChoice_TipsBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniOperateChoice_TipsBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.joystickCtr = ui:GetController("joystick")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart2_EndAgainBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart2_EndAgainBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart2_EndAgainBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart2_EndCloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart2_EndCloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart2_EndCloseBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart2_EndRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart2_EndRewardUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetActivityDungeon1008_MiniStart2_EndRewardUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.AgainBtn = ui:GetChild("AgainBtn")
  uis.CloseBtn = ui:GetChild("CloseBtn")
```

---

## Activty/a8/ActivityDungeon1008_MiniStart2_EndRewardWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart2_EndRewardWindowUis
**Requires:**
- ActivityDungeon1008_MiniStart2_EndRewardByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniStart2_EndRewardByName")

function GetActivityDungeon1008_MiniStart2_EndRewardWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1008_MiniStart2_EndRewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart2_Gu01ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart2_Gu01Uis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart2_Gu01Uis(ui)
  local uis = {}
  
  uis.ExtraImage = ui:GetChild("ExtraImage")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart2_Gu02ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart2_Gu02Uis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart2_Gu02Uis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart2_Gu03ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart2_Gu03Uis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart2_Gu03Uis(ui)
  local uis = {}
  
  uis.ExtraImage = ui:GetChild("ExtraImage")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart2_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart2_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart2_IntegralUis(ui)
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

## Activty/a8/ActivityDungeon1008_MiniStart2_Item01ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart2_Item01Uis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart2_Item01Uis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart2_Item02ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart2_Item02Uis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart2_Item02Uis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart2_Item03ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart2_Item03Uis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart2_Item03Uis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart2_Item04ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart2_Item04Uis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart2_Item04Uis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart2_Item05ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart2_Item05Uis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart2_Item05Uis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart2_Item06ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart2_Item06Uis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart2_Item06Uis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart2_MapLatticeByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart2_MapLatticeUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart2_MapLatticeUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart2_MapRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart2_MapRegionUis
**Requires:**
- ActivityDungeon1008_MiniStart2_MapLatticeByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniStart2_MapLatticeByName")

function GetActivityDungeon1008_MiniStart2_MapRegionUis(ui)
  local uis = {}
  uis.MapLattice = GetActivityDungeon1008_MiniStart2_MapLatticeUis(ui:GetChild("MapLattice"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart2_TipsWordByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart2_TipsWordUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart2_TipsWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart_ArrowDownByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart_ArrowDownUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart_ArrowDownUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart_ArrowLeftByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart_ArrowLeftUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart_ArrowLeftUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart_ArrowRightByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart_ArrowRightUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart_ArrowRightUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart_ArrowUpByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart_ArrowUpUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart_ArrowUpUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart_CloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart_CloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart_EffectTipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart_EffectTipsAniUis
**Requires:**
- ActivityDungeon1008_MiniStart_EffectTipsByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniStart_EffectTipsByName")

function GetActivityDungeon1008_MiniStart_EffectTipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1008_MiniStart_EffectTipsUis(ui:GetChild("Tips"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart_EffectTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart_EffectTipsUis
**Requires:**
- ActivityDungeon1008_MiniStart_ItemByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniStart_ItemByName")

function GetActivityDungeon1008_MiniStart_EffectTipsUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1008_MiniStart_ItemUis(ui:GetChild("Item"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart_EndAgainBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart_EndAgainBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart_EndAgainBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart_EndCloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart_EndCloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart_EndCloseBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart_EndFailByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart_EndFailUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart_EndFailUis(ui)
  local uis = {}
  
  uis.NumberWordTxt = ui:GetChild("NumberWordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart_EndRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart_EndRewardUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1008_MiniStart_EndFailByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1008_MiniStart_EndFailByName")

function GetActivityDungeon1008_MiniStart_EndRewardUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.NumberWordTxt = ui:GetChild("NumberWordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
```

---

## Activty/a8/ActivityDungeon1008_MiniStart_EndRewardWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart_EndRewardWindowUis
**Requires:**
- ActivityDungeon1008_MiniStart_EndRewardByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniStart_EndRewardByName")

function GetActivityDungeon1008_MiniStart_EndRewardWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1008_MiniStart_EndRewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart_GateByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart_GateUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart_GateUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart_GuideAniByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart_GuideAniUis
**Requires:**
- ActivityDungeon1008_MiniStart_GuideByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniStart_GuideByName")

function GetActivityDungeon1008_MiniStart_GuideAniUis(ui)
  local uis = {}
  uis.Guide = GetActivityDungeon1008_MiniStart_GuideUis(ui:GetChild("Guide"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart_GuideByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart_GuideUis
**Requires:**
- ActivityDungeon1008_MiniStart_ItemByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniStart_ItemByName")

function GetActivityDungeon1008_MiniStart_GuideUis(ui)
  local uis = {}
  uis.ArrowImage = ui:GetChild("ArrowImage")
  uis.Item = GetActivityDungeon1008_MiniStart_ItemUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart_Info1ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart_Info1Uis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart_Info1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart_Info2ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart_Info2Uis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart_Info2Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart_IntegralUis(ui)
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

## Activty/a8/ActivityDungeon1008_MiniStart_ItemAniByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart_ItemAniUis
**Requires:**
- ActivityDungeon1008_MiniStart_ItemByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniStart_ItemByName")

function GetActivityDungeon1008_MiniStart_ItemAniUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1008_MiniStart_ItemUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart_ItemByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart_ItemUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart_ItemUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.itemCtr = ui:GetController("item")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart_Joystick1ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart_Joystick1Uis
**Requires:**
- ActivityDungeon1008_MiniStart_ArrowUpByName
- ActivityDungeon1008_MiniStart_ArrowDownByName
- ActivityDungeon1008_MiniStart_ArrowLeftByName
- ActivityDungeon1008_MiniStart_ArrowRightByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniStart_ArrowUpByName")
require("ActivityDungeon1008_MiniStart_ArrowDownByName")
require("ActivityDungeon1008_MiniStart_ArrowLeftByName")
require("ActivityDungeon1008_MiniStart_ArrowRightByName")

function GetActivityDungeon1008_MiniStart_Joystick1Uis(ui)
  local uis = {}
  uis.Up = GetActivityDungeon1008_MiniStart_ArrowUpUis(ui:GetChild("Up"))
  uis.Down = GetActivityDungeon1008_MiniStart_ArrowDownUis(ui:GetChild("Down"))
  uis.Left = GetActivityDungeon1008_MiniStart_ArrowLeftUis(ui:GetChild("Left"))
```

---

## Activty/a8/ActivityDungeon1008_MiniStart_Joystick2ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart_Joystick2Uis
**Requires:**
- ActivityDungeon1008_MiniStart_ArrowUpByName
- ActivityDungeon1008_MiniStart_ArrowDownByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniStart_ArrowUpByName")
require("ActivityDungeon1008_MiniStart_ArrowDownByName")

function GetActivityDungeon1008_MiniStart_Joystick2Uis(ui)
  local uis = {}
  uis.Up = GetActivityDungeon1008_MiniStart_ArrowUpUis(ui:GetChild("Up"))
  uis.Down = GetActivityDungeon1008_MiniStart_ArrowDownUis(ui:GetChild("Down"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart_Joystick3ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart_Joystick3Uis
**Requires:**
- ActivityDungeon1008_MiniStart_ArrowLeftByName
- ActivityDungeon1008_MiniStart_ArrowRightByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniStart_ArrowLeftByName")
require("ActivityDungeon1008_MiniStart_ArrowRightByName")

function GetActivityDungeon1008_MiniStart_Joystick3Uis(ui)
  local uis = {}
  uis.Left = GetActivityDungeon1008_MiniStart_ArrowLeftUis(ui:GetChild("Left"))
  uis.Right = GetActivityDungeon1008_MiniStart_ArrowRightUis(ui:GetChild("Right"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart_MapRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart_MapRegionUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart_MapRegionUis(ui)
  local uis = {}
  
  uis.MapHolder = ui:GetChild("MapHolder")
  uis.GuideHolder = ui:GetChild("GuideHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart_PlayerByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart_PlayerUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart_PlayerUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniStart_SetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniStart_SetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniStart_SetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniTask2ByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniTask2Uis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1008_MiniTask2_IntegralByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1008_MiniTask2_IntegralByName")

function GetActivityDungeon1008_MiniTask2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Integral = GetActivityDungeon1008_MiniTask2_IntegralUis(ui:GetChild("Integral"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a8/ActivityDungeon1008_MiniTask2WindowByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniTask2WindowUis
**Requires:**
- ActivityDungeon1008_MiniTask2ByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniTask2ByName")

function GetActivityDungeon1008_MiniTask2WindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1008_MiniTask2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniTask2_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniTask2_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniTask2_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniTask2_RewardItemByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniTask2_RewardItemUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniTask2_RewardItemUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniTask2_RewardItemGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniTask2_RewardItemGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniTask2_RewardItemGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniTask2_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniTask2_TipsAniUis
**Requires:**
- ActivityDungeon1008_MiniTask2_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniTask2_TipsByName")

function GetActivityDungeon1008_MiniTask2_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1008_MiniTask2_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniTask2_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniTask2_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniTask2_TipsUis(ui)
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

## Activty/a8/ActivityDungeon1008_MiniTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniTaskUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1008_MiniTask_IntegralByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1008_MiniTask_IntegralByName")

function GetActivityDungeon1008_MiniTaskUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Integral = GetActivityDungeon1008_MiniTask_IntegralUis(ui:GetChild("Integral"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a8/ActivityDungeon1008_MiniTaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniTaskWindowUis
**Requires:**
- ActivityDungeon1008_MiniTaskByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniTaskByName")

function GetActivityDungeon1008_MiniTaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1008_MiniTaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniTask_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniTask_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniTask_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniTask_RewardItemByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniTask_RewardItemUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniTask_RewardItemUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniTask_RewardItemGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniTask_RewardItemGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniTask_RewardItemGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniTask_TipsAniUis
**Requires:**
- ActivityDungeon1008_MiniTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniTask_TipsByName")

function GetActivityDungeon1008_MiniTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1008_MiniTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_MiniTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1008_MiniTask_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1008_MiniTask_TipsUis(ui)
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

## Activty/a8/ActivityDungeon1008_NormalBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_NormalBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_NormalBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_NormalPoint1BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_NormalPoint1BtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_NormalPoint1BtnUis(ui)
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

## Activty/a8/ActivityDungeon1008_NormalPoint2BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_NormalPoint2BtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_NormalPoint2BtnUis(ui)
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

## Activty/a8/ActivityDungeon1008_NormalPoint3BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_NormalPoint3BtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_NormalPoint3BtnUis(ui)
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

## Activty/a8/ActivityDungeon1008_NormalPointBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_NormalPointBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_NormalPointBtnUis(ui)
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

## Activty/a8/ActivityDungeon1008_NormalPointLockByName.lua.lua
**Functions:**
- GetActivityDungeon1008_NormalPointLockUis
**Snippet:**
```lua
function GetActivityDungeon1008_NormalPointLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_NumberStripByName.lua.lua
**Functions:**
- GetActivityDungeon1008_NumberStripUis
**Snippet:**
```lua
function GetActivityDungeon1008_NumberStripUis(ui)
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

## Activty/a8/ActivityDungeon1008_PassBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1008_PassBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_PassClothes_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassClothes_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_PassClothes_BuyBtnUis(ui)
  local uis = {}
  
  uis.PriceTxt = ui:GetChild("PriceTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_PassClothes_BuyRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassClothes_BuyRewardUis
**Snippet:**
```lua
function GetActivityDungeon1008_PassClothes_BuyRewardUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_PassClothes_CardQBByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassClothes_CardQBUis
**Snippet:**
```lua
function GetActivityDungeon1008_PassClothes_CardQBUis(ui)
  local uis = {}
  
  uis.QBHolder = ui:GetChild("QBHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_PassClothes_ClothseRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassClothes_ClothseRegionUis
**Requires:**
- ActivityDungeon1008_PassClothes_WordByName
- ActivityDungeon1008_PassClothes_CardQBByName
- ActivityDungeon1008_PassClothes_BuyRewardByName
**Snippet:**
```lua
require("ActivityDungeon1008_PassClothes_WordByName")
require("ActivityDungeon1008_PassClothes_CardQBByName")
require("ActivityDungeon1008_PassClothes_BuyRewardByName")

function GetActivityDungeon1008_PassClothes_ClothseRegionUis(ui)
  local uis = {}
  uis.Word = GetActivityDungeon1008_PassClothes_WordUis(ui:GetChild("Word"))
  uis.CardQB = GetActivityDungeon1008_PassClothes_CardQBUis(ui:GetChild("CardQB"))
  uis.BuyReward = GetActivityDungeon1008_PassClothes_BuyRewardUis(ui:GetChild("BuyReward"))
  uis.BuyBtn = ui:GetChild("BuyBtn")
```

---

## Activty/a8/ActivityDungeon1008_PassClothes_NameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassClothes_NameBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_PassClothes_NameBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_PassClothes_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassClothes_WordUis
**Snippet:**
```lua
function GetActivityDungeon1008_PassClothes_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_PassportByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassportUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1008_PassReward_RewardRegionByName
- ActivityDungeon1008_PassTask_TaskRegionByName
- ActivityDungeon1008_PassClothes_ClothseRegionByName
- ActivityDungeon1008_Passport_LevelByName
- ActivityDungeon1008_Sign_TimeByName
- ActivityDungeon1008_Passport_TabRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1008_PassReward_RewardRegionByName")
require("ActivityDungeon1008_PassTask_TaskRegionByName")
require("ActivityDungeon1008_PassClothes_ClothseRegionByName")
require("ActivityDungeon1008_Passport_LevelByName")
require("ActivityDungeon1008_Sign_TimeByName")
require("ActivityDungeon1008_Passport_TabRegionByName")

function GetActivityDungeon1008_PassportUis(ui)
  local uis = {}
```

---

## Activty/a8/ActivityDungeon1008_PassportUp_LevelUpBgByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassportUp_LevelUpBgUis
**Snippet:**
```lua
function GetActivityDungeon1008_PassportUp_LevelUpBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_PassportUp_LevelUpTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassportUp_LevelUpTipsUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1008_PassportUp_LevelUpBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1008_PassportUp_LevelUpBgByName")

function GetActivityDungeon1008_PassportUp_LevelUpTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.LevelUpBg = GetActivityDungeon1008_PassportUp_LevelUpBgUis(ui:GetChild("LevelUpBg"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
```

---

## Activty/a8/ActivityDungeon1008_PassportUp_LevelUpTipsWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassportUp_LevelUpTipsWindowUis
**Requires:**
- ActivityDungeon1008_PassportUp_LevelUpTipsByName
**Snippet:**
```lua
require("ActivityDungeon1008_PassportUp_LevelUpTipsByName")

function GetActivityDungeon1008_PassportUp_LevelUpTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1008_PassportUp_LevelUpTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_PassportWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassportWindowUis
**Requires:**
- ActivityDungeon1008_PassportByName
**Snippet:**
```lua
require("ActivityDungeon1008_PassportByName")

function GetActivityDungeon1008_PassportWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1008_PassportUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Passport_AllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Passport_AllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_Passport_AllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Passport_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Passport_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_Passport_BuyBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Passport_ExpProgressBarByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Passport_ExpProgressBarUis
**Requires:**
- ActivityDungeon1008_Passport_ExpProgressFillByName
**Snippet:**
```lua
require("ActivityDungeon1008_Passport_ExpProgressFillByName")

function GetActivityDungeon1008_Passport_ExpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetActivityDungeon1008_Passport_ExpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Passport_ExpProgressFillByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Passport_ExpProgressFillUis
**Snippet:**
```lua
function GetActivityDungeon1008_Passport_ExpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Passport_LevelByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Passport_LevelUis
**Snippet:**
```lua
function GetActivityDungeon1008_Passport_LevelUis(ui)
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

## Activty/a8/ActivityDungeon1008_Passport_TabBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Passport_TabBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1008_Passport_TabBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## Activty/a8/ActivityDungeon1008_Passport_TabRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Passport_TabRegionUis
**Snippet:**
```lua
function GetActivityDungeon1008_Passport_TabRegionUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_PassReward_AllFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassReward_AllFrame_EUis
**Requires:**
- ActivityDungeon1008_PassReward_ItemFrame_EByName
- ActivityDungeon1008_PassReward_CardFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1008_PassReward_ItemFrame_EByName")
require("ActivityDungeon1008_PassReward_CardFrame_EByName")

function GetActivityDungeon1008_PassReward_AllFrame_EUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1008_PassReward_ItemFrame_EUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1008_PassReward_CardFrame_EUis(ui:GetChild("CardFrame"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## Activty/a8/ActivityDungeon1008_PassReward_AllFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassReward_AllFrame_MUis
**Requires:**
- ActivityDungeon1008_PassReward_ItemFrame_MByName
- ActivityDungeon1008_PassReward_CardFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1008_PassReward_ItemFrame_MByName")
require("ActivityDungeon1008_PassReward_CardFrame_MByName")

function GetActivityDungeon1008_PassReward_AllFrame_MUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1008_PassReward_ItemFrame_MUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1008_PassReward_CardFrame_MUis(ui:GetChild("CardFrame"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a8/ActivityDungeon1008_PassReward_CardFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassReward_CardFrame_EUis
**Requires:**
- ActivityDungeon1008_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1008_PassReward_ItemCardPicByName")

function GetActivityDungeon1008_PassReward_CardFrame_EUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1008_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a8/ActivityDungeon1008_PassReward_CardFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassReward_CardFrame_MUis
**Requires:**
- ActivityDungeon1008_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1008_PassReward_ItemCardPicByName")

function GetActivityDungeon1008_PassReward_CardFrame_MUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1008_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a8/ActivityDungeon1008_PassReward_EndTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassReward_EndTwoUis
**Requires:**
- ActivityDungeon1008_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1008_PassReward_AllFrame_EByName")

function GetActivityDungeon1008_PassReward_EndTwoUis(ui)
  local uis = {}
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.Item1 = GetActivityDungeon1008_PassReward_AllFrame_EUis(ui:GetChild("Item1"))
  uis.Item2 = GetActivityDungeon1008_PassReward_AllFrame_EUis(ui:GetChild("Item2"))
  uis.root = ui
```

---

## Activty/a8/ActivityDungeon1008_PassReward_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassReward_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1008_PassReward_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_PassReward_ItemFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassReward_ItemFrame_EUis
**Snippet:**
```lua
function GetActivityDungeon1008_PassReward_ItemFrame_EUis(ui)
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

## Activty/a8/ActivityDungeon1008_PassReward_ItemFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassReward_ItemFrame_MUis
**Snippet:**
```lua
function GetActivityDungeon1008_PassReward_ItemFrame_MUis(ui)
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

## Activty/a8/ActivityDungeon1008_PassReward_LevelTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassReward_LevelTitleUis
**Snippet:**
```lua
function GetActivityDungeon1008_PassReward_LevelTitleUis(ui)
  local uis = {}
  
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_PassReward_MiddleRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassReward_MiddleRegionUis
**Snippet:**
```lua
function GetActivityDungeon1008_PassReward_MiddleRegionUis(ui)
  local uis = {}
  
  uis.MiddleList = ui:GetChild("MiddleList")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_PassReward_MidTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassReward_MidTwoUis
**Requires:**
- ActivityDungeon1008_PassReward_MidTwoItemByName
- ActivityDungeon1008_PassReward_LevelTitleByName
**Snippet:**
```lua
require("ActivityDungeon1008_PassReward_MidTwoItemByName")
require("ActivityDungeon1008_PassReward_LevelTitleByName")

function GetActivityDungeon1008_PassReward_MidTwoUis(ui)
  local uis = {}
  uis.Reward1 = GetActivityDungeon1008_PassReward_MidTwoItemUis(ui:GetChild("Reward1"))
  uis.Reward2 = GetActivityDungeon1008_PassReward_MidTwoItemUis(ui:GetChild("Reward2"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Title = GetActivityDungeon1008_PassReward_LevelTitleUis(ui:GetChild("Title"))
```

---

## Activty/a8/ActivityDungeon1008_PassReward_MidTwoItemByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassReward_MidTwoItemUis
**Requires:**
- ActivityDungeon1008_PassReward_AllFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1008_PassReward_AllFrame_MByName")

function GetActivityDungeon1008_PassReward_MidTwoItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1008_PassReward_AllFrame_MUis(ui:GetChild("Item"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_PassReward_PicByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassReward_PicUis
**Snippet:**
```lua
function GetActivityDungeon1008_PassReward_PicUis(ui)
  local uis = {}
  
  uis.BuyTxt = ui:GetChild("BuyTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_PassReward_RewardRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassReward_RewardRegionUis
**Requires:**
- ActivityDungeon1008_PassReward_MiddleRegionByName
- ActivityDungeon1008_PassReward_StartTwoByName
- ActivityDungeon1008_PassReward_EndTwoByName
**Snippet:**
```lua
require("ActivityDungeon1008_PassReward_MiddleRegionByName")
require("ActivityDungeon1008_PassReward_StartTwoByName")
require("ActivityDungeon1008_PassReward_EndTwoByName")

function GetActivityDungeon1008_PassReward_RewardRegionUis(ui)
  local uis = {}
  uis.MiddleList = GetActivityDungeon1008_PassReward_MiddleRegionUis(ui:GetChild("MiddleList"))
  uis.StartTwo = GetActivityDungeon1008_PassReward_StartTwoUis(ui:GetChild("StartTwo"))
  uis.EndTwo = GetActivityDungeon1008_PassReward_EndTwoUis(ui:GetChild("EndTwo"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a8/ActivityDungeon1008_PassReward_StartTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassReward_StartTwoUis
**Requires:**
- ActivityDungeon1008_PassReward_PicByName
**Snippet:**
```lua
require("ActivityDungeon1008_PassReward_PicByName")

function GetActivityDungeon1008_PassReward_StartTwoUis(ui)
  local uis = {}
  uis.Pic = GetActivityDungeon1008_PassReward_PicUis(ui:GetChild("Pic"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_PassTask_TaskRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassTask_TaskRegionUis
**Requires:**
- ActivityDungeon1008_TaskMaxByName
**Snippet:**
```lua
require("ActivityDungeon1008_TaskMaxByName")

function GetActivityDungeon1008_PassTask_TaskRegionUis(ui)
  local uis = {}
  uis.TipsList = ui:GetChild("TipsList")
  uis.Max = GetActivityDungeon1008_TaskMaxUis(ui:GetChild("Max"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_PassTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassTask_TipsAniUis
**Requires:**
- ActivityDungeon1008_PassTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1008_PassTask_TipsByName")

function GetActivityDungeon1008_PassTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1008_PassTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_PassTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassTask_TipsUis
**Requires:**
- ActivityDungeon1008_PassTask_TipsIntegralByName
**Snippet:**
```lua
require("ActivityDungeon1008_PassTask_TipsIntegralByName")

function GetActivityDungeon1008_PassTask_TipsUis(ui)
  local uis = {}
  uis.ProgressTxt = ui:GetChild("ProgressTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Integral = GetActivityDungeon1008_PassTask_TipsIntegralUis(ui:GetChild("Integral"))
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a8/ActivityDungeon1008_PassTask_TipsIntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PassTask_TipsIntegralUis
**Snippet:**
```lua
function GetActivityDungeon1008_PassTask_TipsIntegralUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_PlotBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PlotBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_PlotBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_PlotByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PlotUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1008_Plot_WordByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1008_Plot_WordByName")

function GetActivityDungeon1008_PlotUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Word = GetActivityDungeon1008_Plot_WordUis(ui:GetChild("Word"))
  uis.PlotList = ui:GetChild("PlotList")
  uis.ProspectBtn = ui:GetChild("ProspectBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a8/ActivityDungeon1008_PlotWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1008_PlotWindowUis
**Requires:**
- ActivityDungeon1008_PlotByName
**Snippet:**
```lua
require("ActivityDungeon1008_PlotByName")

function GetActivityDungeon1008_PlotWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1008_PlotUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Plot_ProspectBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Plot_ProspectBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_Plot_ProspectBtnUis(ui)
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

## Activty/a8/ActivityDungeon1008_Plot_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Plot_TipsAniUis
**Requires:**
- ActivityDungeon1008_Plot_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1008_Plot_TipsByName")

function GetActivityDungeon1008_Plot_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1008_Plot_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Plot_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Plot_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1008_Plot_TipsUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Plot_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Plot_WordUis
**Snippet:**
```lua
function GetActivityDungeon1008_Plot_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_ReduceBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_ReduceBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_ReduceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_ReviewWordByName.lua.lua
**Functions:**
- GetActivityDungeon1008_ReviewWordUis
**Snippet:**
```lua
function GetActivityDungeon1008_ReviewWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_ShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_ShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_ShopBtnUis(ui)
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

## Activty/a8/ActivityDungeon1008_ShopByName.lua.lua
**Functions:**
- GetActivityDungeon1008_ShopUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1008_Shop_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1008_Shop_TimeByName")

function GetActivityDungeon1008_ShopUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Time = GetActivityDungeon1008_Shop_TimeUis(ui:GetChild("Time"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a8/ActivityDungeon1008_ShopWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1008_ShopWindowUis
**Requires:**
- ActivityDungeon1008_ShopByName
**Snippet:**
```lua
require("ActivityDungeon1008_ShopByName")

function GetActivityDungeon1008_ShopWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1008_ShopUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Shop_CardHeadBgByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Shop_CardHeadBgUis
**Snippet:**
```lua
function GetActivityDungeon1008_Shop_CardHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Shop_ItemAniByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Shop_ItemAniUis
**Requires:**
- ActivityDungeon1008_Shop_ItemByName
**Snippet:**
```lua
require("ActivityDungeon1008_Shop_ItemByName")

function GetActivityDungeon1008_Shop_ItemAniUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1008_Shop_ItemUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Shop_ItemBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Shop_ItemBtnUis
**Requires:**
- ActivityDungeon1008_Shop_CardHeadBgByName
- ActivityDungeon1008_Shop_ItemNumberByName
- ActivityDungeon1008_Shop_UseMarkByName
**Snippet:**
```lua
require("ActivityDungeon1008_Shop_CardHeadBgByName")
require("ActivityDungeon1008_Shop_ItemNumberByName")
require("ActivityDungeon1008_Shop_UseMarkByName")

function GetActivityDungeon1008_Shop_ItemBtnUis(ui)
  local uis = {}
  uis.CardHeadBg = GetActivityDungeon1008_Shop_CardHeadBgUis(ui:GetChild("CardHeadBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.ItemNumber = GetActivityDungeon1008_Shop_ItemNumberUis(ui:GetChild("ItemNumber"))
```

---

## Activty/a8/ActivityDungeon1008_Shop_ItemByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Shop_ItemUis
**Requires:**
- ActivityDungeon1008_Shop_SellOutByName
**Snippet:**
```lua
require("ActivityDungeon1008_Shop_SellOutByName")

function GetActivityDungeon1008_Shop_ItemUis(ui)
  local uis = {}
  uis.ItemBtn = ui:GetChild("ItemBtn")
  uis.SellOut = GetActivityDungeon1008_Shop_SellOutUis(ui:GetChild("SellOut"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Shop_ItemNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Shop_ItemNumberUis
**Snippet:**
```lua
function GetActivityDungeon1008_Shop_ItemNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Shop_ItemRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Shop_ItemRegionUis
**Requires:**
- ActivityDungeon1008_Shop_TitleByName
**Snippet:**
```lua
require("ActivityDungeon1008_Shop_TitleByName")

function GetActivityDungeon1008_Shop_ItemRegionUis(ui)
  local uis = {}
  uis.ShopTitle = GetActivityDungeon1008_Shop_TitleUis(ui:GetChild("ShopTitle"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Shop_SellOutByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Shop_SellOutUis
**Snippet:**
```lua
function GetActivityDungeon1008_Shop_SellOutUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Shop_StarByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Shop_StarUis
**Snippet:**
```lua
function GetActivityDungeon1008_Shop_StarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Shop_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Shop_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1008_Shop_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Shop_TitleByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Shop_TitleUis
**Snippet:**
```lua
function GetActivityDungeon1008_Shop_TitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Shop_UseMarkByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Shop_UseMarkUis
**Snippet:**
```lua
function GetActivityDungeon1008_Shop_UseMarkUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_SignBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_SignBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1008_SignBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_SignByName.lua.lua
**Functions:**
- GetActivityDungeon1008_SignUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1008_Sign_RewardListByName
- ActivityDungeon1008_Sign_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1008_Sign_RewardListByName")
require("ActivityDungeon1008_Sign_TimeByName")

function GetActivityDungeon1008_SignUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.RewardList = GetActivityDungeon1008_Sign_RewardListUis(ui:GetChild("RewardList"))
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.Time = GetActivityDungeon1008_Sign_TimeUis(ui:GetChild("Time"))
```

---

## Activty/a8/ActivityDungeon1008_SignWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1008_SignWindowUis
**Requires:**
- ActivityDungeon1008_SignByName
**Snippet:**
```lua
require("ActivityDungeon1008_SignByName")

function GetActivityDungeon1008_SignWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1008_SignUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Sign_AllFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Sign_AllFrameUis
**Requires:**
- ActivityDungeon1008_Sign_ItemFrameByName
- ActivityDungeon1008_Sign_CardFrameByName
**Snippet:**
```lua
require("ActivityDungeon1008_Sign_ItemFrameByName")
require("ActivityDungeon1008_Sign_CardFrameByName")

function GetActivityDungeon1008_Sign_AllFrameUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1008_Sign_ItemFrameUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1008_Sign_CardFrameUis(ui:GetChild("CardFrame"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a8/ActivityDungeon1008_Sign_CardFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Sign_CardFrameUis
**Requires:**
- ActivityDungeon1008_Sign_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1008_Sign_ItemCardPicByName")

function GetActivityDungeon1008_Sign_CardFrameUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1008_Sign_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a8/ActivityDungeon1008_Sign_GetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Sign_GetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_Sign_GetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Sign_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Sign_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1008_Sign_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Sign_ItemFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Sign_ItemFrameUis
**Snippet:**
```lua
function GetActivityDungeon1008_Sign_ItemFrameUis(ui)
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

## Activty/a8/ActivityDungeon1008_Sign_RewardAniByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Sign_RewardAniUis
**Requires:**
- ActivityDungeon1008_Sign_RewardByName
**Snippet:**
```lua
require("ActivityDungeon1008_Sign_RewardByName")

function GetActivityDungeon1008_Sign_RewardAniUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1008_Sign_RewardUis(ui:GetChild("Reward"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Sign_RewardByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Sign_RewardUis
**Requires:**
- ActivityDungeon1008_Sign_AllFrameByName
**Snippet:**
```lua
require("ActivityDungeon1008_Sign_AllFrameByName")

function GetActivityDungeon1008_Sign_RewardUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1008_Sign_AllFrameUis(ui:GetChild("Item"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Sign_RewardListByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Sign_RewardListUis
**Snippet:**
```lua
function GetActivityDungeon1008_Sign_RewardListUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_Sign_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1008_Sign_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1008_Sign_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_TaskAllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_TaskAllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_TaskAllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1008_TaskBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_TaskByName.lua.lua
**Functions:**
- GetActivityDungeon1008_TaskUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1008_TaskTitleByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1008_TaskTitleByName")

function GetActivityDungeon1008_TaskUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TaskTitle = GetActivityDungeon1008_TaskTitleUis(ui:GetChild("TaskTitle"))
  uis.TaskTipsList = ui:GetChild("TaskTipsList")
  uis.AllGetBtn = ui:GetChild("AllGetBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a8/ActivityDungeon1008_TaskGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1008_TaskGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1008_TaskGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_TaskMaxByName.lua.lua
**Functions:**
- GetActivityDungeon1008_TaskMaxUis
**Snippet:**
```lua
function GetActivityDungeon1008_TaskMaxUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_TaskProgressByName.lua.lua
**Functions:**
- GetActivityDungeon1008_TaskProgressUis
**Snippet:**
```lua
function GetActivityDungeon1008_TaskProgressUis(ui)
  local uis = {}
  
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_TaskTipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1008_TaskTipsAniUis
**Requires:**
- ActivityDungeon1008_TaskTipsByName
**Snippet:**
```lua
require("ActivityDungeon1008_TaskTipsByName")

function GetActivityDungeon1008_TaskTipsAniUis(ui)
  local uis = {}
  uis.TaskTips = GetActivityDungeon1008_TaskTipsUis(ui:GetChild("TaskTips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_TaskTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1008_TaskTipsUis
**Requires:**
- ActivityDungeon1008_TaskProgressByName
**Snippet:**
```lua
require("ActivityDungeon1008_TaskProgressByName")

function GetActivityDungeon1008_TaskTipsUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.RewardList = ui:GetChild("RewardList")
  uis.TaskProgress = GetActivityDungeon1008_TaskProgressUis(ui:GetChild("TaskProgress"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a8/ActivityDungeon1008_TaskTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1008_TaskTitleUis
**Snippet:**
```lua
function GetActivityDungeon1008_TaskTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a8/ActivityDungeon1008_TaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1008_TaskWindowUis
**Requires:**
- ActivityDungeon1008_TaskByName
**Snippet:**
```lua
require("ActivityDungeon1008_TaskByName")

function GetActivityDungeon1008_TaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1008_TaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---
