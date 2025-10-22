# Activty/a13

## Activty/a13/ActivityDungeon1013_ActivityDungeonByName.lua.lua
**Functions:**
- GetActivityDungeon1013_ActivityDungeonUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1013_MainTitleByName
- ActivityDungeon1013_ReviewWordByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1013_MainTitleByName")
require("ActivityDungeon1013_ReviewWordByName")
require("CommonResource_CurrencyReturnByName")

function GetActivityDungeon1013_ActivityDungeonUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.MainTitle = GetActivityDungeon1013_MainTitleUis(ui:GetChild("MainTitle"))
  uis.MiniGame1Btn = ui:GetChild("MiniGame1Btn")
```

---

## Activty/a13/ActivityDungeon1013_ActivityDungeonWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1013_ActivityDungeonWindowUis
**Requires:**
- ActivityDungeon1013_ActivityDungeonByName
**Snippet:**
```lua
require("ActivityDungeon1013_ActivityDungeonByName")

function GetActivityDungeon1013_ActivityDungeonWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1013_ActivityDungeonUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_AddBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_AddBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_AddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_BossBattleByName.lua.lua
**Functions:**
- GetActivityDungeon1013_BossBattleUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1013_BossBattle_InfoByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1013_BossBattle_InfoByName")

function GetActivityDungeon1013_BossBattleUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.Info = GetActivityDungeon1013_BossBattle_InfoUis(ui:GetChild("Info"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a13/ActivityDungeon1013_BossBattleWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1013_BossBattleWindowUis
**Requires:**
- ActivityDungeon1013_BossBattleByName
**Snippet:**
```lua
require("ActivityDungeon1013_BossBattleByName")

function GetActivityDungeon1013_BossBattleWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1013_BossBattleUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_BossBattle_Info1ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_BossBattle_Info1Uis
**Snippet:**
```lua
function GetActivityDungeon1013_BossBattle_Info1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_BossBattle_InfoByName.lua.lua
**Functions:**
- GetActivityDungeon1013_BossBattle_InfoUis
**Requires:**
- ActivityDungeon1013_BossBattle_Info1ByName
**Snippet:**
```lua
require("ActivityDungeon1013_BossBattle_Info1ByName")

function GetActivityDungeon1013_BossBattle_InfoUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = GetActivityDungeon1013_BossBattle_Info1Uis(ui:GetChild("WordTxt"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_BossBattle_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1013_BossBattle_TipsAniUis
**Requires:**
- ActivityDungeon1013_BossBattle_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1013_BossBattle_TipsByName")

function GetActivityDungeon1013_BossBattle_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1013_BossBattle_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_BossBattle_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1013_BossBattle_TipsUis
**Requires:**
- ActivityDungeon1013_BossBattle_TipsRewardByName
**Snippet:**
```lua
require("ActivityDungeon1013_BossBattle_TipsRewardByName")

function GetActivityDungeon1013_BossBattle_TipsUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1013_BossBattle_TipsRewardUis(ui:GetChild("Reward"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.NumberWordTxt = ui:GetChild("NumberWordTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a13/ActivityDungeon1013_BossBattle_TipsRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1013_BossBattle_TipsRewardUis
**Snippet:**
```lua
function GetActivityDungeon1013_BossBattle_TipsRewardUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_BossBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_BossBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1013_BossBtnUis(ui)
  local uis = {}
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.newCtr = ui:GetController("new")
```

---

## Activty/a13/ActivityDungeon1013_BuyLevelBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_BuyLevelBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_BuyLevelBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_BuyLevelDes1ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_BuyLevelDes1Uis
**Requires:**
- ActivityDungeon1013_NumberStripByName
- ActivityDungeon1013_BuyPriceNumberByName
**Snippet:**
```lua
require("ActivityDungeon1013_NumberStripByName")
require("ActivityDungeon1013_BuyPriceNumberByName")

function GetActivityDungeon1013_BuyLevelDes1Uis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.NumberStrip = GetActivityDungeon1013_NumberStripUis(ui:GetChild("NumberStrip"))
  uis.BuyPriceNumber = GetActivityDungeon1013_BuyPriceNumberUis(ui:GetChild("BuyPriceNumber"))
```

---

## Activty/a13/ActivityDungeon1013_BuyLevelDes2ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_BuyLevelDes2Uis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1013_BuyLevelDes1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1013_BuyLevelDes1ByName")

function GetActivityDungeon1013_BuyLevelDes2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.BuyLevelDes1 = GetActivityDungeon1013_BuyLevelDes1Uis(ui:GetChild("BuyLevelDes1"))
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.root = ui
```

---

## Activty/a13/ActivityDungeon1013_BuyLevelDesWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1013_BuyLevelDesWindowUis
**Requires:**
- ActivityDungeon1013_BuyLevelDes2ByName
**Snippet:**
```lua
require("ActivityDungeon1013_BuyLevelDes2ByName")

function GetActivityDungeon1013_BuyLevelDesWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1013_BuyLevelDes2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_BuyLevelItemByName.lua.lua
**Functions:**
- GetActivityDungeon1013_BuyLevelItemUis
**Requires:**
- ActivityDungeon1013_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1013_PassReward_AllFrame_EByName")

function GetActivityDungeon1013_BuyLevelItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1013_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_BuyPriceNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1013_BuyPriceNumberUis
**Snippet:**
```lua
function GetActivityDungeon1013_BuyPriceNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_ChallengeByName.lua.lua
**Functions:**
- GetActivityDungeon1013_ChallengeUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1013_MapListByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1013_MapListByName")

function GetActivityDungeon1013_ChallengeUis(ui)
  local uis = {}
  uis.BgList = ui:GetChild("BgList")
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Map = GetActivityDungeon1013_MapListUis(ui:GetChild("Map"))
  uis.ShopBtn = ui:GetChild("ShopBtn")
  uis.ChapterList = ui:GetChild("ChapterList")
```

---

## Activty/a13/ActivityDungeon1013_ChallengeChapterBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_ChallengeChapterBtnUis
**Requires:**
- ActivityDungeon1013_NormalPointLockByName
**Snippet:**
```lua
require("ActivityDungeon1013_NormalPointLockByName")

function GetActivityDungeon1013_ChallengeChapterBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Lock = GetActivityDungeon1013_NormalPointLockUis(ui:GetChild("Lock"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Activty/a13/ActivityDungeon1013_ChallengeShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_ChallengeShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_ChallengeShopBtnUis(ui)
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

## Activty/a13/ActivityDungeon1013_ChallengeWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1013_ChallengeWindowUis
**Requires:**
- ActivityDungeon1013_ChallengeByName
**Snippet:**
```lua
require("ActivityDungeon1013_ChallengeByName")

function GetActivityDungeon1013_ChallengeWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1013_ChallengeUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_EventTipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1013_EventTipsAniUis
**Requires:**
- ActivityDungeon1013_EventTipsByName
**Snippet:**
```lua
require("ActivityDungeon1013_EventTipsByName")

function GetActivityDungeon1013_EventTipsAniUis(ui)
  local uis = {}
  uis.EventTips = GetActivityDungeon1013_EventTipsUis(ui:GetChild("EventTips"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_EventTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1013_EventTipsUis
**Snippet:**
```lua
function GetActivityDungeon1013_EventTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_EventTipsListByName.lua.lua
**Functions:**
- GetActivityDungeon1013_EventTipsListUis
**Snippet:**
```lua
function GetActivityDungeon1013_EventTipsListUis(ui)
  local uis = {}
  
  uis.EventTipsList = ui:GetChild("EventTipsList")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MainBuildSignByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MainBuildSignUis
**Snippet:**
```lua
function GetActivityDungeon1013_MainBuildSignUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MainCoverByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MainCoverUis
**Snippet:**
```lua
function GetActivityDungeon1013_MainCoverUis(ui)
  local uis = {}
  
  uis.BackGroundHolder = ui:GetChild("BackGroundHolder")
  uis.BackGround1Holder = ui:GetChild("BackGround1Holder")
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MainCoverWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MainCoverWindowUis
**Requires:**
- ActivityDungeon1013_MainCoverByName
**Snippet:**
```lua
require("ActivityDungeon1013_MainCoverByName")

function GetActivityDungeon1013_MainCoverWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1013_MainCoverUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MainTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MainTitleUis
**Snippet:**
```lua
function GetActivityDungeon1013_MainTitleUis(ui)
  local uis = {}
  
  uis.Time1Txt = ui:GetChild("Time1Txt")
  uis.Time2Txt = ui:GetChild("Time2Txt")
  uis.reviewCtr = ui:GetController("review")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MapBottom_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MapBottom_1Uis
**Snippet:**
```lua
function GetActivityDungeon1013_MapBottom_1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MapBottom_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MapBottom_2Uis
**Snippet:**
```lua
function GetActivityDungeon1013_MapBottom_2Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MapBottom_3ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MapBottom_3Uis
**Snippet:**
```lua
function GetActivityDungeon1013_MapBottom_3Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MapBottom_4ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MapBottom_4Uis
**Snippet:**
```lua
function GetActivityDungeon1013_MapBottom_4Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MapListByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MapListUis
**Snippet:**
```lua
function GetActivityDungeon1013_MapListUis(ui)
  local uis = {}
  
  uis.MapList = ui:GetChild("MapList")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Map_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Map_1Uis
**Snippet:**
```lua
function GetActivityDungeon1013_Map_1Uis(ui)
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

## Activty/a13/ActivityDungeon1013_Map_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Map_2Uis
**Snippet:**
```lua
function GetActivityDungeon1013_Map_2Uis(ui)
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

## Activty/a13/ActivityDungeon1013_Map_3ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Map_3Uis
**Snippet:**
```lua
function GetActivityDungeon1013_Map_3Uis(ui)
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

## Activty/a13/ActivityDungeon1013_Map_4ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Map_4Uis
**Snippet:**
```lua
function GetActivityDungeon1013_Map_4Uis(ui)
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

## Activty/a13/ActivityDungeon1013_MaterialBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MaterialBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1013_MaterialBtnUis(ui)
  local uis = {}
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
```

---

## Activty/a13/ActivityDungeon1013_MaterialByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MaterialUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1013_Material_BattleNumberByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1013_Material_BattleNumberByName")

function GetActivityDungeon1013_MaterialUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.BattleNumber = GetActivityDungeon1013_Material_BattleNumberUis(ui:GetChild("BattleNumber"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a13/ActivityDungeon1013_MaterialWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MaterialWindowUis
**Requires:**
- ActivityDungeon1013_MaterialByName
**Snippet:**
```lua
require("ActivityDungeon1013_MaterialByName")

function GetActivityDungeon1013_MaterialWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1013_MaterialUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Material_BattleAniByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Material_BattleAniUis
**Requires:**
- ActivityDungeon1013_Material_BattleByName
**Snippet:**
```lua
require("ActivityDungeon1013_Material_BattleByName")

function GetActivityDungeon1013_Material_BattleAniUis(ui)
  local uis = {}
  uis.Battle = GetActivityDungeon1013_Material_BattleUis(ui:GetChild("Battle"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Material_BattleByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Material_BattleUis
**Snippet:**
```lua
function GetActivityDungeon1013_Material_BattleUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Material_BattleNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Material_BattleNumberUis
**Snippet:**
```lua
function GetActivityDungeon1013_Material_BattleNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MaxBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MaxBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_MaxBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MinBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MinBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_MinBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniExplain2ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniExplain2Uis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1013_MiniExplain2_TipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1013_MiniExplain2_TipsByName")

function GetActivityDungeon1013_MiniExplain2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Tips = GetActivityDungeon1013_MiniExplain2_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
```

---

## Activty/a13/ActivityDungeon1013_MiniExplain2WindowByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniExplain2WindowUis
**Requires:**
- ActivityDungeon1013_MiniExplain2ByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniExplain2ByName")

function GetActivityDungeon1013_MiniExplain2WindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1013_MiniExplain2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniExplain2_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniExplain2_TipsUis
**Requires:**
- ActivityDungeon1013_MiniExplain2_TipsContentWordByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniExplain2_TipsContentWordByName")

function GetActivityDungeon1013_MiniExplain2_TipsUis(ui)
  local uis = {}
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.Word1 = GetActivityDungeon1013_MiniExplain2_TipsContentWordUis(ui:GetChild("Word1"))
  uis.Word2 = GetActivityDungeon1013_MiniExplain2_TipsContentWordUis(ui:GetChild("Word2"))
  uis.Word3 = GetActivityDungeon1013_MiniExplain2_TipsContentWordUis(ui:GetChild("Word3"))
  uis.root = ui
  return uis
```

---

## Activty/a13/ActivityDungeon1013_MiniExplain2_TipsCloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniExplain2_TipsCloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniExplain2_TipsCloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniExplain2_TipsContentWordByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniExplain2_TipsContentWordUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniExplain2_TipsContentWordUis(ui)
  local uis = {}
  
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.WordList = ui:GetChild("WordList")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniExplain2_TipsWordByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniExplain2_TipsWordUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniExplain2_TipsWordUis(ui)
  local uis = {}
  
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniGame1BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniGame1BtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1013_MiniGame1BtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniGame2ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniGame2Uis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1013_MiniMain2_TopByName
- ActivityDungeon1013_MiniMain2_BottonByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1013_MiniMain2_TopByName")
require("ActivityDungeon1013_MiniMain2_BottonByName")

function GetActivityDungeon1013_MiniGame2Uis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Top = GetActivityDungeon1013_MiniMain2_TopUis(ui:GetChild("Top"))
  uis.Botton = GetActivityDungeon1013_MiniMain2_BottonUis(ui:GetChild("Botton"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a13/ActivityDungeon1013_MiniGame2WindowByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniGame2WindowUis
**Requires:**
- ActivityDungeon1013_MiniGame2ByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniGame2ByName")

function GetActivityDungeon1013_MiniGame2WindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1013_MiniGame2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniGameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniGameBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1013_MiniGameBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniGameByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniGameUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1013_MiniMain_TopByName
- ActivityDungeon1013_MiniMain_BottonByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1013_MiniMain_TopByName")
require("ActivityDungeon1013_MiniMain_BottonByName")

function GetActivityDungeon1013_MiniGameUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Top = GetActivityDungeon1013_MiniMain_TopUis(ui:GetChild("Top"))
  uis.Botton = GetActivityDungeon1013_MiniMain_BottonUis(ui:GetChild("Botton"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a13/ActivityDungeon1013_MiniGameStart2ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniGameStart2Uis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1013_MiniStart2_IntegralByName
- ActivityDungeon1013_MiniStart2_OperateRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1013_MiniStart2_IntegralByName")
require("ActivityDungeon1013_MiniStart2_OperateRegionByName")

function GetActivityDungeon1013_MiniGameStart2Uis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Integral = GetActivityDungeon1013_MiniStart2_IntegralUis(ui:GetChild("Integral"))
  uis.OperateRegion = GetActivityDungeon1013_MiniStart2_OperateRegionUis(ui:GetChild("OperateRegion"))
  uis.WithdrawBtn = ui:GetChild("WithdrawBtn")
```

---

## Activty/a13/ActivityDungeon1013_MiniGameStart2WindowByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniGameStart2WindowUis
**Requires:**
- ActivityDungeon1013_MiniGameStart2ByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniGameStart2ByName")

function GetActivityDungeon1013_MiniGameStart2WindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1013_MiniGameStart2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniGameStartByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniGameStartUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1013_MiniStart_HandRegionByName
- ActivityDungeon1013_MiniStart_BoxByName
- ActivityDungeon1013_MiniStart_LaunchByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1013_MiniStart_HandRegionByName")
require("ActivityDungeon1013_MiniStart_BoxByName")
require("ActivityDungeon1013_MiniStart_LaunchByName")

function GetActivityDungeon1013_MiniGameStartUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.HandRegion = GetActivityDungeon1013_MiniStart_HandRegionUis(ui:GetChild("HandRegion"))
  uis.Box = GetActivityDungeon1013_MiniStart_BoxUis(ui:GetChild("Box"))
```

---

## Activty/a13/ActivityDungeon1013_MiniGameStartWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniGameStartWindowUis
**Requires:**
- ActivityDungeon1013_MiniGameStartByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniGameStartByName")

function GetActivityDungeon1013_MiniGameStartWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1013_MiniGameStartUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniGameWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniGameWindowUis
**Requires:**
- ActivityDungeon1013_MiniGameByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniGameByName")

function GetActivityDungeon1013_MiniGameWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1013_MiniGameUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniMain2_BottonByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniMain2_BottonUis
**Requires:**
- ActivityDungeon1013_MiniMain2_TodayTaskByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniMain2_TodayTaskByName")

function GetActivityDungeon1013_MiniMain2_BottonUis(ui)
  local uis = {}
  uis.TaskBtn = ui:GetChild("TaskBtn")
  uis.TodayTask = GetActivityDungeon1013_MiniMain2_TodayTaskUis(ui:GetChild("TodayTask"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniMain2_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniMain2_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniMain2_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniMain2_StartBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniMain2_StartBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniMain2_StartBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniMain2_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniMain2_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1013_MiniMain2_TaskBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniMain2_TodayTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniMain2_TodayTaskUis
**Requires:**
- ActivityDungeon1013_PassReward_AllFrame_EByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("ActivityDungeon1013_PassReward_AllFrame_EByName")
require("CommonResource_RedDotByName")

function GetActivityDungeon1013_MiniMain2_TodayTaskUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1013_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a13/ActivityDungeon1013_MiniMain2_TopByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniMain2_TopUis
**Requires:**
- ActivityDungeon1013_MiniMain2_IntegralByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniMain2_IntegralByName")

function GetActivityDungeon1013_MiniMain2_TopUis(ui)
  local uis = {}
  uis.Integral = GetActivityDungeon1013_MiniMain2_IntegralUis(ui:GetChild("Integral"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniMain_BottonByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniMain_BottonUis
**Requires:**
- ActivityDungeon1013_MiniMain_TodayTaskByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniMain_TodayTaskByName")

function GetActivityDungeon1013_MiniMain_BottonUis(ui)
  local uis = {}
  uis.TaskBtn = ui:GetChild("TaskBtn")
  uis.RecordBtn = ui:GetChild("RecordBtn")
  uis.TodayTask = GetActivityDungeon1013_MiniMain_TodayTaskUis(ui:GetChild("TodayTask"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniMain_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniMain_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniMain_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniMain_RecordBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniMain_RecordBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniMain_RecordBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniMain_StartBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniMain_StartBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniMain_StartBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniMain_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniMain_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1013_MiniMain_TaskBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniMain_TodayTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniMain_TodayTaskUis
**Requires:**
- ActivityDungeon1013_PassReward_AllFrame_EByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("ActivityDungeon1013_PassReward_AllFrame_EByName")
require("CommonResource_RedDotByName")

function GetActivityDungeon1013_MiniMain_TodayTaskUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1013_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a13/ActivityDungeon1013_MiniMain_TopByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniMain_TopUis
**Requires:**
- ActivityDungeon1013_MiniMain_IntegralByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniMain_IntegralByName")

function GetActivityDungeon1013_MiniMain_TopUis(ui)
  local uis = {}
  uis.Integral = GetActivityDungeon1013_MiniMain_IntegralUis(ui:GetChild("Integral"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniRankByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniRankUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetActivityDungeon1013_MiniRankUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.TipsList = ui:GetChild("TipsList")
  uis.IntegralList = ui:GetChild("IntegralList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a13/ActivityDungeon1013_MiniRankWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniRankWindowUis
**Requires:**
- ActivityDungeon1013_MiniRankByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniRankByName")

function GetActivityDungeon1013_MiniRankWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1013_MiniRankUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniRank_Integral1ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniRank_Integral1Uis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniRank_Integral1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniRank_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniRank_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniRank_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniRank_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniRank_TipsAniUis
**Requires:**
- ActivityDungeon1013_MiniRank_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniRank_TipsByName")

function GetActivityDungeon1013_MiniRank_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1013_MiniRank_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniRank_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniRank_TipsUis
**Requires:**
- CommonResource_HeadByName
**Snippet:**
```lua
require("CommonResource_HeadByName")

function GetActivityDungeon1013_MiniRank_TipsUis(ui)
  local uis = {}
  uis.RankTxt = ui:GetChild("RankTxt")
  uis.Head = GetCommonResource_HeadUis(ui:GetChild("Head"))
  uis.GuildTxt = ui:GetChild("GuildTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.LengthTxt = ui:GetChild("LengthTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a13/ActivityDungeon1013_MiniStart2_AgainBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart2_AgainBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart2_AgainBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart2_CloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart2_CloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart2_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart2_EndAgainBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart2_EndAgainBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart2_EndAgainBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart2_EndCloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart2_EndCloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart2_EndCloseBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart2_EndRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart2_EndRewardUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetActivityDungeon1013_MiniStart2_EndRewardUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.AgainBtn = ui:GetChild("AgainBtn")
  uis.CloseBtn = ui:GetChild("CloseBtn")
```

---

## Activty/a13/ActivityDungeon1013_MiniStart2_EndRewardWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart2_EndRewardWindowUis
**Requires:**
- ActivityDungeon1013_MiniStart2_EndRewardByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniStart2_EndRewardByName")

function GetActivityDungeon1013_MiniStart2_EndRewardWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1013_MiniStart2_EndRewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart2_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart2_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart2_IntegralUis(ui)
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

## Activty/a13/ActivityDungeon1013_MiniStart2_Move00ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart2_Move00Uis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart2_Move00Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart2_Move01ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart2_Move01Uis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart2_Move01Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart2_Move02ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart2_Move02Uis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart2_Move02Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart2_Move03ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart2_Move03Uis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart2_Move03Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart2_Move04ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart2_Move04Uis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart2_Move04Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart2_Move05ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart2_Move05Uis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart2_Move05Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart2_Move06ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart2_Move06Uis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart2_Move06Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart2_Move07ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart2_Move07Uis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart2_Move07Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart2_Move08ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart2_Move08Uis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart2_Move08Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart2_Move09ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart2_Move09Uis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart2_Move09Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart2_Move10ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart2_Move10Uis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart2_Move10Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart2_OperateRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart2_OperateRegionUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart2_OperateRegionUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart2_PauseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart2_PauseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart2_PauseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart2_WithdrawBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart2_WithdrawBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart2_WithdrawBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart_BoxByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart_BoxUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart_BoxUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart_CloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart_CloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart_DirectionBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart_DirectionBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart_DirectionBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart_EndAgainBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart_EndAgainBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart_EndAgainBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart_EndCloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart_EndCloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart_EndCloseBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart_EndRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart_EndRewardUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetActivityDungeon1013_MiniStart_EndRewardUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.AgainBtn = ui:GetChild("AgainBtn")
  uis.CloseBtn = ui:GetChild("CloseBtn")
```

---

## Activty/a13/ActivityDungeon1013_MiniStart_EndRewardWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart_EndRewardWindowUis
**Requires:**
- ActivityDungeon1013_MiniStart_EndRewardByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniStart_EndRewardByName")

function GetActivityDungeon1013_MiniStart_EndRewardWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1013_MiniStart_EndRewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart_ExchangeBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart_ExchangeBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart_ExchangeBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart_HandRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart_HandRegionUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart_HandRegionUis(ui)
  local uis = {}
  
  uis.ExchangeBtn = ui:GetChild("ExchangeBtn")
  uis.LeftBtn = ui:GetChild("LeftBtn")
  uis.RightBtn = ui:GetChild("RightBtn")
  uis.ShootBtn = ui:GetChild("ShootBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Activty/a13/ActivityDungeon1013_MiniStart_ItemByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart_ItemUis
**Requires:**
- ActivityDungeon1013_MiniStart_ItemNumberByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniStart_ItemNumberByName")

function GetActivityDungeon1013_MiniStart_ItemUis(ui)
  local uis = {}
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.ItemNumber = GetActivityDungeon1013_MiniStart_ItemNumberUis(ui:GetChild("ItemNumber"))
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Activty/a13/ActivityDungeon1013_MiniStart_ItemNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart_ItemNumberUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart_ItemNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart_LaunchBallByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart_LaunchBallUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart_LaunchBallUis(ui)
  local uis = {}
  
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart_LaunchByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart_LaunchUis
**Requires:**
- ActivityDungeon1013_MiniStart_LaunchInfoByName
- ActivityDungeon1013_MiniStart_LaunchBallByName
- ActivityDungeon1013_MiniStart_LaunchStaffByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniStart_LaunchInfoByName")
require("ActivityDungeon1013_MiniStart_LaunchBallByName")
require("ActivityDungeon1013_MiniStart_LaunchStaffByName")

function GetActivityDungeon1013_MiniStart_LaunchUis(ui)
  local uis = {}
  uis.Info1 = GetActivityDungeon1013_MiniStart_LaunchInfoUis(ui:GetChild("Info1"))
  uis.Info2 = GetActivityDungeon1013_MiniStart_LaunchInfoUis(ui:GetChild("Info2"))
  uis.Ball = GetActivityDungeon1013_MiniStart_LaunchBallUis(ui:GetChild("Ball"))
  uis.Staff = GetActivityDungeon1013_MiniStart_LaunchStaffUis(ui:GetChild("Staff"))
```

---

## Activty/a13/ActivityDungeon1013_MiniStart_LaunchInfoByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart_LaunchInfoUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart_LaunchInfoUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart_LaunchStaffByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart_LaunchStaffUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart_LaunchStaffUis(ui)
  local uis = {}
  
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniStart_ShootBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniStart_ShootBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniStart_ShootBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniTask2ByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniTask2Uis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1013_MiniTask2_IntegralByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1013_MiniTask2_IntegralByName")

function GetActivityDungeon1013_MiniTask2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Integral = GetActivityDungeon1013_MiniTask2_IntegralUis(ui:GetChild("Integral"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a13/ActivityDungeon1013_MiniTask2WindowByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniTask2WindowUis
**Requires:**
- ActivityDungeon1013_MiniTask2ByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniTask2ByName")

function GetActivityDungeon1013_MiniTask2WindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1013_MiniTask2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniTask2_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniTask2_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniTask2_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniTask2_RewardItemByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniTask2_RewardItemUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniTask2_RewardItemUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniTask2_RewardItemGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniTask2_RewardItemGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniTask2_RewardItemGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniTask2_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniTask2_TipsAniUis
**Requires:**
- ActivityDungeon1013_MiniTask2_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniTask2_TipsByName")

function GetActivityDungeon1013_MiniTask2_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1013_MiniTask2_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniTask2_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniTask2_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniTask2_TipsUis(ui)
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

## Activty/a13/ActivityDungeon1013_MiniTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniTaskUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1013_MiniTask_IntegralByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1013_MiniTask_IntegralByName")

function GetActivityDungeon1013_MiniTaskUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Integral = GetActivityDungeon1013_MiniTask_IntegralUis(ui:GetChild("Integral"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a13/ActivityDungeon1013_MiniTaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniTaskWindowUis
**Requires:**
- ActivityDungeon1013_MiniTaskByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniTaskByName")

function GetActivityDungeon1013_MiniTaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1013_MiniTaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniTask_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniTask_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniTask_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniTask_RewardItemByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniTask_RewardItemUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniTask_RewardItemUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniTask_RewardItemGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniTask_RewardItemGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniTask_RewardItemGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniTask_TipsAniUis
**Requires:**
- ActivityDungeon1013_MiniTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniTask_TipsByName")

function GetActivityDungeon1013_MiniTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1013_MiniTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniTask_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniTask_TipsUis(ui)
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

## Activty/a13/ActivityDungeon1013_MiniTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniTipsUis
**Snippet:**
```lua
function GetActivityDungeon1013_MiniTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_MiniTipsWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1013_MiniTipsWindowUis
**Requires:**
- ActivityDungeon1013_MiniTipsByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniTipsByName")

function GetActivityDungeon1013_MiniTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1013_MiniTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_NormalBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_NormalBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_NormalBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_NormalPoint1BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_NormalPoint1BtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_NormalPoint1BtnUis(ui)
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

## Activty/a13/ActivityDungeon1013_NormalPoint2BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_NormalPoint2BtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_NormalPoint2BtnUis(ui)
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

## Activty/a13/ActivityDungeon1013_NormalPoint3BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_NormalPoint3BtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_NormalPoint3BtnUis(ui)
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

## Activty/a13/ActivityDungeon1013_NormalPoint4BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_NormalPoint4BtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_NormalPoint4BtnUis(ui)
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

## Activty/a13/ActivityDungeon1013_NormalPointLockByName.lua.lua
**Functions:**
- GetActivityDungeon1013_NormalPointLockUis
**Snippet:**
```lua
function GetActivityDungeon1013_NormalPointLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_NumberStripByName.lua.lua
**Functions:**
- GetActivityDungeon1013_NumberStripUis
**Snippet:**
```lua
function GetActivityDungeon1013_NumberStripUis(ui)
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

## Activty/a13/ActivityDungeon1013_PassBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1013_PassBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_PassClothes_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassClothes_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_PassClothes_BuyBtnUis(ui)
  local uis = {}
  
  uis.PriceTxt = ui:GetChild("PriceTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_PassClothes_BuyRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassClothes_BuyRewardUis
**Snippet:**
```lua
function GetActivityDungeon1013_PassClothes_BuyRewardUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_PassClothes_CardQBByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassClothes_CardQBUis
**Snippet:**
```lua
function GetActivityDungeon1013_PassClothes_CardQBUis(ui)
  local uis = {}
  
  uis.QBHolder = ui:GetChild("QBHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_PassClothes_ClothseRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassClothes_ClothseRegionUis
**Requires:**
- ActivityDungeon1013_PassClothes_WordByName
- ActivityDungeon1013_PassClothes_CardQBByName
- ActivityDungeon1013_PassClothes_BuyRewardByName
**Snippet:**
```lua
require("ActivityDungeon1013_PassClothes_WordByName")
require("ActivityDungeon1013_PassClothes_CardQBByName")
require("ActivityDungeon1013_PassClothes_BuyRewardByName")

function GetActivityDungeon1013_PassClothes_ClothseRegionUis(ui)
  local uis = {}
  uis.Word = GetActivityDungeon1013_PassClothes_WordUis(ui:GetChild("Word"))
  uis.CardQB = GetActivityDungeon1013_PassClothes_CardQBUis(ui:GetChild("CardQB"))
  uis.BuyReward = GetActivityDungeon1013_PassClothes_BuyRewardUis(ui:GetChild("BuyReward"))
  uis.BuyBtn = ui:GetChild("BuyBtn")
```

---

## Activty/a13/ActivityDungeon1013_PassClothes_NameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassClothes_NameBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_PassClothes_NameBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_PassClothes_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassClothes_WordUis
**Snippet:**
```lua
function GetActivityDungeon1013_PassClothes_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_PassportByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassportUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1013_PassReward_RewardRegionByName
- ActivityDungeon1013_PassTask_TaskRegionByName
- ActivityDungeon1013_PassClothes_ClothseRegionByName
- ActivityDungeon1013_Passport_LevelByName
- ActivityDungeon1013_Sign_TimeByName
- ActivityDungeon1013_Passport_TabRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1013_PassReward_RewardRegionByName")
require("ActivityDungeon1013_PassTask_TaskRegionByName")
require("ActivityDungeon1013_PassClothes_ClothseRegionByName")
require("ActivityDungeon1013_Passport_LevelByName")
require("ActivityDungeon1013_Sign_TimeByName")
require("ActivityDungeon1013_Passport_TabRegionByName")

function GetActivityDungeon1013_PassportUis(ui)
  local uis = {}
```

---

## Activty/a13/ActivityDungeon1013_PassportUp_LevelUpBgByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassportUp_LevelUpBgUis
**Snippet:**
```lua
function GetActivityDungeon1013_PassportUp_LevelUpBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_PassportUp_LevelUpTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassportUp_LevelUpTipsUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1013_PassportUp_LevelUpBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1013_PassportUp_LevelUpBgByName")

function GetActivityDungeon1013_PassportUp_LevelUpTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.LevelUpBg = GetActivityDungeon1013_PassportUp_LevelUpBgUis(ui:GetChild("LevelUpBg"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
```

---

## Activty/a13/ActivityDungeon1013_PassportUp_LevelUpTipsWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassportUp_LevelUpTipsWindowUis
**Requires:**
- ActivityDungeon1013_PassportUp_LevelUpTipsByName
**Snippet:**
```lua
require("ActivityDungeon1013_PassportUp_LevelUpTipsByName")

function GetActivityDungeon1013_PassportUp_LevelUpTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1013_PassportUp_LevelUpTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_PassportWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassportWindowUis
**Requires:**
- ActivityDungeon1013_PassportByName
**Snippet:**
```lua
require("ActivityDungeon1013_PassportByName")

function GetActivityDungeon1013_PassportWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1013_PassportUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Passport_AllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Passport_AllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_Passport_AllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Passport_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Passport_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_Passport_BuyBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Passport_ExpProgressBarByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Passport_ExpProgressBarUis
**Requires:**
- ActivityDungeon1013_Passport_ExpProgressFillByName
**Snippet:**
```lua
require("ActivityDungeon1013_Passport_ExpProgressFillByName")

function GetActivityDungeon1013_Passport_ExpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetActivityDungeon1013_Passport_ExpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Passport_ExpProgressFillByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Passport_ExpProgressFillUis
**Snippet:**
```lua
function GetActivityDungeon1013_Passport_ExpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Passport_LevelByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Passport_LevelUis
**Snippet:**
```lua
function GetActivityDungeon1013_Passport_LevelUis(ui)
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

## Activty/a13/ActivityDungeon1013_Passport_TabBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Passport_TabBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1013_Passport_TabBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## Activty/a13/ActivityDungeon1013_Passport_TabRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Passport_TabRegionUis
**Snippet:**
```lua
function GetActivityDungeon1013_Passport_TabRegionUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_PassReward_AllFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassReward_AllFrame_EUis
**Requires:**
- ActivityDungeon1013_PassReward_ItemFrame_EByName
- ActivityDungeon1013_PassReward_CardFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1013_PassReward_ItemFrame_EByName")
require("ActivityDungeon1013_PassReward_CardFrame_EByName")

function GetActivityDungeon1013_PassReward_AllFrame_EUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1013_PassReward_ItemFrame_EUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1013_PassReward_CardFrame_EUis(ui:GetChild("CardFrame"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## Activty/a13/ActivityDungeon1013_PassReward_AllFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassReward_AllFrame_MUis
**Requires:**
- ActivityDungeon1013_PassReward_ItemFrame_MByName
- ActivityDungeon1013_PassReward_CardFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1013_PassReward_ItemFrame_MByName")
require("ActivityDungeon1013_PassReward_CardFrame_MByName")

function GetActivityDungeon1013_PassReward_AllFrame_MUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1013_PassReward_ItemFrame_MUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1013_PassReward_CardFrame_MUis(ui:GetChild("CardFrame"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a13/ActivityDungeon1013_PassReward_CardFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassReward_CardFrame_EUis
**Requires:**
- ActivityDungeon1013_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1013_PassReward_ItemCardPicByName")

function GetActivityDungeon1013_PassReward_CardFrame_EUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1013_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a13/ActivityDungeon1013_PassReward_CardFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassReward_CardFrame_MUis
**Requires:**
- ActivityDungeon1013_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1013_PassReward_ItemCardPicByName")

function GetActivityDungeon1013_PassReward_CardFrame_MUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1013_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a13/ActivityDungeon1013_PassReward_EndTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassReward_EndTwoUis
**Requires:**
- ActivityDungeon1013_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1013_PassReward_AllFrame_EByName")

function GetActivityDungeon1013_PassReward_EndTwoUis(ui)
  local uis = {}
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.Item1 = GetActivityDungeon1013_PassReward_AllFrame_EUis(ui:GetChild("Item1"))
  uis.Item2 = GetActivityDungeon1013_PassReward_AllFrame_EUis(ui:GetChild("Item2"))
  uis.root = ui
```

---

## Activty/a13/ActivityDungeon1013_PassReward_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassReward_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1013_PassReward_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_PassReward_ItemFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassReward_ItemFrame_EUis
**Snippet:**
```lua
function GetActivityDungeon1013_PassReward_ItemFrame_EUis(ui)
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

## Activty/a13/ActivityDungeon1013_PassReward_ItemFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassReward_ItemFrame_MUis
**Snippet:**
```lua
function GetActivityDungeon1013_PassReward_ItemFrame_MUis(ui)
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

## Activty/a13/ActivityDungeon1013_PassReward_LevelTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassReward_LevelTitleUis
**Snippet:**
```lua
function GetActivityDungeon1013_PassReward_LevelTitleUis(ui)
  local uis = {}
  
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_PassReward_MiddleRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassReward_MiddleRegionUis
**Snippet:**
```lua
function GetActivityDungeon1013_PassReward_MiddleRegionUis(ui)
  local uis = {}
  
  uis.MiddleList = ui:GetChild("MiddleList")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_PassReward_MidTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassReward_MidTwoUis
**Requires:**
- ActivityDungeon1013_PassReward_MidTwoItemByName
- ActivityDungeon1013_PassReward_LevelTitleByName
**Snippet:**
```lua
require("ActivityDungeon1013_PassReward_MidTwoItemByName")
require("ActivityDungeon1013_PassReward_LevelTitleByName")

function GetActivityDungeon1013_PassReward_MidTwoUis(ui)
  local uis = {}
  uis.Reward1 = GetActivityDungeon1013_PassReward_MidTwoItemUis(ui:GetChild("Reward1"))
  uis.Reward2 = GetActivityDungeon1013_PassReward_MidTwoItemUis(ui:GetChild("Reward2"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Title = GetActivityDungeon1013_PassReward_LevelTitleUis(ui:GetChild("Title"))
```

---

## Activty/a13/ActivityDungeon1013_PassReward_MidTwoItemByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassReward_MidTwoItemUis
**Requires:**
- ActivityDungeon1013_PassReward_AllFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1013_PassReward_AllFrame_MByName")

function GetActivityDungeon1013_PassReward_MidTwoItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1013_PassReward_AllFrame_MUis(ui:GetChild("Item"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_PassReward_PicByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassReward_PicUis
**Snippet:**
```lua
function GetActivityDungeon1013_PassReward_PicUis(ui)
  local uis = {}
  
  uis.BuyTxt = ui:GetChild("BuyTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_PassReward_RewardRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassReward_RewardRegionUis
**Requires:**
- ActivityDungeon1013_PassReward_MiddleRegionByName
- ActivityDungeon1013_PassReward_StartTwoByName
- ActivityDungeon1013_PassReward_EndTwoByName
**Snippet:**
```lua
require("ActivityDungeon1013_PassReward_MiddleRegionByName")
require("ActivityDungeon1013_PassReward_StartTwoByName")
require("ActivityDungeon1013_PassReward_EndTwoByName")

function GetActivityDungeon1013_PassReward_RewardRegionUis(ui)
  local uis = {}
  uis.MiddleList = GetActivityDungeon1013_PassReward_MiddleRegionUis(ui:GetChild("MiddleList"))
  uis.StartTwo = GetActivityDungeon1013_PassReward_StartTwoUis(ui:GetChild("StartTwo"))
  uis.EndTwo = GetActivityDungeon1013_PassReward_EndTwoUis(ui:GetChild("EndTwo"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a13/ActivityDungeon1013_PassReward_StartTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassReward_StartTwoUis
**Requires:**
- ActivityDungeon1013_PassReward_PicByName
**Snippet:**
```lua
require("ActivityDungeon1013_PassReward_PicByName")

function GetActivityDungeon1013_PassReward_StartTwoUis(ui)
  local uis = {}
  uis.Pic = GetActivityDungeon1013_PassReward_PicUis(ui:GetChild("Pic"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_PassTask_TaskRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassTask_TaskRegionUis
**Requires:**
- ActivityDungeon1013_TaskMaxByName
**Snippet:**
```lua
require("ActivityDungeon1013_TaskMaxByName")

function GetActivityDungeon1013_PassTask_TaskRegionUis(ui)
  local uis = {}
  uis.TipsList = ui:GetChild("TipsList")
  uis.Max = GetActivityDungeon1013_TaskMaxUis(ui:GetChild("Max"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_PassTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassTask_TipsAniUis
**Requires:**
- ActivityDungeon1013_PassTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1013_PassTask_TipsByName")

function GetActivityDungeon1013_PassTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1013_PassTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_PassTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassTask_TipsUis
**Requires:**
- ActivityDungeon1013_PassTask_TipsIntegralByName
**Snippet:**
```lua
require("ActivityDungeon1013_PassTask_TipsIntegralByName")

function GetActivityDungeon1013_PassTask_TipsUis(ui)
  local uis = {}
  uis.ProgressTxt = ui:GetChild("ProgressTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Integral = GetActivityDungeon1013_PassTask_TipsIntegralUis(ui:GetChild("Integral"))
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a13/ActivityDungeon1013_PassTask_TipsIntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PassTask_TipsIntegralUis
**Snippet:**
```lua
function GetActivityDungeon1013_PassTask_TipsIntegralUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_PlotBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PlotBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_PlotBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_PlotByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PlotUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1013_Plot_WordByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1013_Plot_WordByName")

function GetActivityDungeon1013_PlotUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Word = GetActivityDungeon1013_Plot_WordUis(ui:GetChild("Word"))
  uis.PlotList = ui:GetChild("PlotList")
  uis.ProspectBtn = ui:GetChild("ProspectBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a13/ActivityDungeon1013_PlotWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1013_PlotWindowUis
**Requires:**
- ActivityDungeon1013_PlotByName
**Snippet:**
```lua
require("ActivityDungeon1013_PlotByName")

function GetActivityDungeon1013_PlotWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1013_PlotUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Plot_ProspectBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Plot_ProspectBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_Plot_ProspectBtnUis(ui)
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

## Activty/a13/ActivityDungeon1013_Plot_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Plot_TipsAniUis
**Requires:**
- ActivityDungeon1013_Plot_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1013_Plot_TipsByName")

function GetActivityDungeon1013_Plot_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1013_Plot_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Plot_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Plot_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1013_Plot_TipsUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Plot_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Plot_WordUis
**Snippet:**
```lua
function GetActivityDungeon1013_Plot_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_ReduceBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_ReduceBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_ReduceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_ReviewWordByName.lua.lua
**Functions:**
- GetActivityDungeon1013_ReviewWordUis
**Snippet:**
```lua
function GetActivityDungeon1013_ReviewWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_ShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_ShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_ShopBtnUis(ui)
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

## Activty/a13/ActivityDungeon1013_ShopByName.lua.lua
**Functions:**
- GetActivityDungeon1013_ShopUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1013_Shop_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1013_Shop_TimeByName")

function GetActivityDungeon1013_ShopUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Time = GetActivityDungeon1013_Shop_TimeUis(ui:GetChild("Time"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a13/ActivityDungeon1013_ShopWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1013_ShopWindowUis
**Requires:**
- ActivityDungeon1013_ShopByName
**Snippet:**
```lua
require("ActivityDungeon1013_ShopByName")

function GetActivityDungeon1013_ShopWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1013_ShopUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Shop_CardHeadBgByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Shop_CardHeadBgUis
**Snippet:**
```lua
function GetActivityDungeon1013_Shop_CardHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Shop_ItemAniByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Shop_ItemAniUis
**Requires:**
- ActivityDungeon1013_Shop_ItemByName
**Snippet:**
```lua
require("ActivityDungeon1013_Shop_ItemByName")

function GetActivityDungeon1013_Shop_ItemAniUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1013_Shop_ItemUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Shop_ItemBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Shop_ItemBtnUis
**Requires:**
- ActivityDungeon1013_Shop_CardHeadBgByName
- ActivityDungeon1013_Shop_ItemNumberByName
- ActivityDungeon1013_Shop_UseMarkByName
**Snippet:**
```lua
require("ActivityDungeon1013_Shop_CardHeadBgByName")
require("ActivityDungeon1013_Shop_ItemNumberByName")
require("ActivityDungeon1013_Shop_UseMarkByName")

function GetActivityDungeon1013_Shop_ItemBtnUis(ui)
  local uis = {}
  uis.CardHeadBg = GetActivityDungeon1013_Shop_CardHeadBgUis(ui:GetChild("CardHeadBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.ItemNumber = GetActivityDungeon1013_Shop_ItemNumberUis(ui:GetChild("ItemNumber"))
```

---

## Activty/a13/ActivityDungeon1013_Shop_ItemByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Shop_ItemUis
**Requires:**
- ActivityDungeon1013_Shop_SellOutByName
**Snippet:**
```lua
require("ActivityDungeon1013_Shop_SellOutByName")

function GetActivityDungeon1013_Shop_ItemUis(ui)
  local uis = {}
  uis.ItemBtn = ui:GetChild("ItemBtn")
  uis.SellOut = GetActivityDungeon1013_Shop_SellOutUis(ui:GetChild("SellOut"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Shop_ItemNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Shop_ItemNumberUis
**Snippet:**
```lua
function GetActivityDungeon1013_Shop_ItemNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Shop_ItemRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Shop_ItemRegionUis
**Requires:**
- ActivityDungeon1013_Shop_TitleByName
**Snippet:**
```lua
require("ActivityDungeon1013_Shop_TitleByName")

function GetActivityDungeon1013_Shop_ItemRegionUis(ui)
  local uis = {}
  uis.ShopTitle = GetActivityDungeon1013_Shop_TitleUis(ui:GetChild("ShopTitle"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Shop_SellOutByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Shop_SellOutUis
**Snippet:**
```lua
function GetActivityDungeon1013_Shop_SellOutUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Shop_StarByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Shop_StarUis
**Snippet:**
```lua
function GetActivityDungeon1013_Shop_StarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Shop_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Shop_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1013_Shop_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Shop_TitleByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Shop_TitleUis
**Snippet:**
```lua
function GetActivityDungeon1013_Shop_TitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Shop_UseMarkByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Shop_UseMarkUis
**Snippet:**
```lua
function GetActivityDungeon1013_Shop_UseMarkUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_SignBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_SignBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1013_SignBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_SignByName.lua.lua
**Functions:**
- GetActivityDungeon1013_SignUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1013_Sign_RewardListByName
- ActivityDungeon1013_Sign_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1013_Sign_RewardListByName")
require("ActivityDungeon1013_Sign_TimeByName")

function GetActivityDungeon1013_SignUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.RewardList = GetActivityDungeon1013_Sign_RewardListUis(ui:GetChild("RewardList"))
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.Time = GetActivityDungeon1013_Sign_TimeUis(ui:GetChild("Time"))
```

---

## Activty/a13/ActivityDungeon1013_SignWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1013_SignWindowUis
**Requires:**
- ActivityDungeon1013_SignByName
**Snippet:**
```lua
require("ActivityDungeon1013_SignByName")

function GetActivityDungeon1013_SignWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1013_SignUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Sign_AllFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Sign_AllFrameUis
**Requires:**
- ActivityDungeon1013_Sign_ItemFrameByName
- ActivityDungeon1013_Sign_CardFrameByName
**Snippet:**
```lua
require("ActivityDungeon1013_Sign_ItemFrameByName")
require("ActivityDungeon1013_Sign_CardFrameByName")

function GetActivityDungeon1013_Sign_AllFrameUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1013_Sign_ItemFrameUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1013_Sign_CardFrameUis(ui:GetChild("CardFrame"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a13/ActivityDungeon1013_Sign_CardFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Sign_CardFrameUis
**Requires:**
- ActivityDungeon1013_Sign_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1013_Sign_ItemCardPicByName")

function GetActivityDungeon1013_Sign_CardFrameUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1013_Sign_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a13/ActivityDungeon1013_Sign_GetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Sign_GetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_Sign_GetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Sign_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Sign_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1013_Sign_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Sign_ItemFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Sign_ItemFrameUis
**Snippet:**
```lua
function GetActivityDungeon1013_Sign_ItemFrameUis(ui)
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

## Activty/a13/ActivityDungeon1013_Sign_RewardAniByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Sign_RewardAniUis
**Requires:**
- ActivityDungeon1013_Sign_RewardByName
**Snippet:**
```lua
require("ActivityDungeon1013_Sign_RewardByName")

function GetActivityDungeon1013_Sign_RewardAniUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1013_Sign_RewardUis(ui:GetChild("Reward"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Sign_RewardByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Sign_RewardUis
**Requires:**
- ActivityDungeon1013_Sign_AllFrameByName
**Snippet:**
```lua
require("ActivityDungeon1013_Sign_AllFrameByName")

function GetActivityDungeon1013_Sign_RewardUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1013_Sign_AllFrameUis(ui:GetChild("Item"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Sign_RewardListByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Sign_RewardListUis
**Snippet:**
```lua
function GetActivityDungeon1013_Sign_RewardListUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_Sign_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1013_Sign_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1013_Sign_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_TaskAllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_TaskAllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_TaskAllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1013_TaskBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_TaskByName.lua.lua
**Functions:**
- GetActivityDungeon1013_TaskUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1013_TaskTitleByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1013_TaskTitleByName")

function GetActivityDungeon1013_TaskUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TaskTitle = GetActivityDungeon1013_TaskTitleUis(ui:GetChild("TaskTitle"))
  uis.TaskTipsList = ui:GetChild("TaskTipsList")
  uis.AllGetBtn = ui:GetChild("AllGetBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a13/ActivityDungeon1013_TaskGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_TaskGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_TaskGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_TaskMaxByName.lua.lua
**Functions:**
- GetActivityDungeon1013_TaskMaxUis
**Snippet:**
```lua
function GetActivityDungeon1013_TaskMaxUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_TaskProgressByName.lua.lua
**Functions:**
- GetActivityDungeon1013_TaskProgressUis
**Snippet:**
```lua
function GetActivityDungeon1013_TaskProgressUis(ui)
  local uis = {}
  
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_TaskTipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1013_TaskTipsAniUis
**Requires:**
- ActivityDungeon1013_TaskTipsByName
**Snippet:**
```lua
require("ActivityDungeon1013_TaskTipsByName")

function GetActivityDungeon1013_TaskTipsAniUis(ui)
  local uis = {}
  uis.TaskTips = GetActivityDungeon1013_TaskTipsUis(ui:GetChild("TaskTips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_TaskTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1013_TaskTipsUis
**Requires:**
- ActivityDungeon1013_TaskProgressByName
**Snippet:**
```lua
require("ActivityDungeon1013_TaskProgressByName")

function GetActivityDungeon1013_TaskTipsUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.RewardList = ui:GetChild("RewardList")
  uis.TaskProgress = GetActivityDungeon1013_TaskProgressUis(ui:GetChild("TaskProgress"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a13/ActivityDungeon1013_TaskTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1013_TaskTitleUis
**Snippet:**
```lua
function GetActivityDungeon1013_TaskTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_TaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1013_TaskWindowUis
**Requires:**
- ActivityDungeon1013_TaskByName
**Snippet:**
```lua
require("ActivityDungeon1013_TaskByName")

function GetActivityDungeon1013_TaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1013_TaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a13/ActivityDungeon1013_TouchScreenBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1013_TouchScreenBtnUis
**Snippet:**
```lua
function GetActivityDungeon1013_TouchScreenBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---
