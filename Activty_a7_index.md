# Activty/a7

## Activty/a7/ActivityDungeon1007_ActivityDungeonByName.lua.lua
**Functions:**
- GetActivityDungeon1007_ActivityDungeonUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1007_MainTitleByName
- ActivityDungeon1007_ReviewWordByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1007_MainTitleByName")
require("ActivityDungeon1007_ReviewWordByName")
require("CommonResource_CurrencyReturnByName")

function GetActivityDungeon1007_ActivityDungeonUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.MainTitle = GetActivityDungeon1007_MainTitleUis(ui:GetChild("MainTitle"))
  uis.PlotBtn = ui:GetChild("PlotBtn")
```

---

## Activty/a7/ActivityDungeon1007_ActivityDungeonWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1007_ActivityDungeonWindowUis
**Requires:**
- ActivityDungeon1007_ActivityDungeonByName
**Snippet:**
```lua
require("ActivityDungeon1007_ActivityDungeonByName")

function GetActivityDungeon1007_ActivityDungeonWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1007_ActivityDungeonUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_AddBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_AddBtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_AddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_BossBattleByName.lua.lua
**Functions:**
- GetActivityDungeon1007_BossBattleUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1007_BossBattle_InfoByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1007_BossBattle_InfoByName")

function GetActivityDungeon1007_BossBattleUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.Info = GetActivityDungeon1007_BossBattle_InfoUis(ui:GetChild("Info"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a7/ActivityDungeon1007_BossBattleWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1007_BossBattleWindowUis
**Requires:**
- ActivityDungeon1007_BossBattleByName
**Snippet:**
```lua
require("ActivityDungeon1007_BossBattleByName")

function GetActivityDungeon1007_BossBattleWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1007_BossBattleUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_BossBattle_Info1ByName.lua.lua
**Functions:**
- GetActivityDungeon1007_BossBattle_Info1Uis
**Snippet:**
```lua
function GetActivityDungeon1007_BossBattle_Info1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_BossBattle_InfoByName.lua.lua
**Functions:**
- GetActivityDungeon1007_BossBattle_InfoUis
**Requires:**
- ActivityDungeon1007_BossBattle_Info1ByName
**Snippet:**
```lua
require("ActivityDungeon1007_BossBattle_Info1ByName")

function GetActivityDungeon1007_BossBattle_InfoUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = GetActivityDungeon1007_BossBattle_Info1Uis(ui:GetChild("WordTxt"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_BossBattle_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1007_BossBattle_TipsAniUis
**Requires:**
- ActivityDungeon1007_BossBattle_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1007_BossBattle_TipsByName")

function GetActivityDungeon1007_BossBattle_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1007_BossBattle_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_BossBattle_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1007_BossBattle_TipsUis
**Requires:**
- ActivityDungeon1007_BossBattle_TipsRewardByName
**Snippet:**
```lua
require("ActivityDungeon1007_BossBattle_TipsRewardByName")

function GetActivityDungeon1007_BossBattle_TipsUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1007_BossBattle_TipsRewardUis(ui:GetChild("Reward"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.NumberWordTxt = ui:GetChild("NumberWordTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a7/ActivityDungeon1007_BossBattle_TipsRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1007_BossBattle_TipsRewardUis
**Snippet:**
```lua
function GetActivityDungeon1007_BossBattle_TipsRewardUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_BossBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_BossBtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_BossBtnUis(ui)
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

## Activty/a7/ActivityDungeon1007_BuyLevelBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_BuyLevelBtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_BuyLevelBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_BuyLevelDes1ByName.lua.lua
**Functions:**
- GetActivityDungeon1007_BuyLevelDes1Uis
**Requires:**
- ActivityDungeon1007_NumberStripByName
- ActivityDungeon1007_BuyPriceNumberByName
**Snippet:**
```lua
require("ActivityDungeon1007_NumberStripByName")
require("ActivityDungeon1007_BuyPriceNumberByName")

function GetActivityDungeon1007_BuyLevelDes1Uis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.NumberStrip = GetActivityDungeon1007_NumberStripUis(ui:GetChild("NumberStrip"))
  uis.BuyPriceNumber = GetActivityDungeon1007_BuyPriceNumberUis(ui:GetChild("BuyPriceNumber"))
```

---

## Activty/a7/ActivityDungeon1007_BuyLevelDes2ByName.lua.lua
**Functions:**
- GetActivityDungeon1007_BuyLevelDes2Uis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1007_BuyLevelDes1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1007_BuyLevelDes1ByName")

function GetActivityDungeon1007_BuyLevelDes2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.BuyLevelDes1 = GetActivityDungeon1007_BuyLevelDes1Uis(ui:GetChild("BuyLevelDes1"))
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.root = ui
```

---

## Activty/a7/ActivityDungeon1007_BuyLevelDesWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1007_BuyLevelDesWindowUis
**Requires:**
- ActivityDungeon1007_BuyLevelDes2ByName
**Snippet:**
```lua
require("ActivityDungeon1007_BuyLevelDes2ByName")

function GetActivityDungeon1007_BuyLevelDesWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1007_BuyLevelDes2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_BuyLevelItemByName.lua.lua
**Functions:**
- GetActivityDungeon1007_BuyLevelItemUis
**Requires:**
- ActivityDungeon1007_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1007_PassReward_AllFrame_EByName")

function GetActivityDungeon1007_BuyLevelItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1007_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_BuyPriceNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1007_BuyPriceNumberUis
**Snippet:**
```lua
function GetActivityDungeon1007_BuyPriceNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_ChallengeByName.lua.lua
**Functions:**
- GetActivityDungeon1007_ChallengeUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1007_MapListByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1007_MapListByName")

function GetActivityDungeon1007_ChallengeUis(ui)
  local uis = {}
  uis.BgList = ui:GetChild("BgList")
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Map = GetActivityDungeon1007_MapListUis(ui:GetChild("Map"))
  uis.ShopBtn = ui:GetChild("ShopBtn")
  uis.ChapterList = ui:GetChild("ChapterList")
```

---

## Activty/a7/ActivityDungeon1007_ChallengeChapterBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_ChallengeChapterBtnUis
**Requires:**
- ActivityDungeon1007_NormalPointLockByName
**Snippet:**
```lua
require("ActivityDungeon1007_NormalPointLockByName")

function GetActivityDungeon1007_ChallengeChapterBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Lock = GetActivityDungeon1007_NormalPointLockUis(ui:GetChild("Lock"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Activty/a7/ActivityDungeon1007_ChallengeShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_ChallengeShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_ChallengeShopBtnUis(ui)
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

## Activty/a7/ActivityDungeon1007_ChallengeWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1007_ChallengeWindowUis
**Requires:**
- ActivityDungeon1007_ChallengeByName
**Snippet:**
```lua
require("ActivityDungeon1007_ChallengeByName")

function GetActivityDungeon1007_ChallengeWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1007_ChallengeUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MainTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MainTitleUis
**Snippet:**
```lua
function GetActivityDungeon1007_MainTitleUis(ui)
  local uis = {}
  
  uis.Time1Txt = ui:GetChild("Time1Txt")
  uis.Time2Txt = ui:GetChild("Time2Txt")
  uis.reviewCtr = ui:GetController("review")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MapBottom_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MapBottom_1Uis
**Snippet:**
```lua
function GetActivityDungeon1007_MapBottom_1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MapBottom_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MapBottom_2Uis
**Snippet:**
```lua
function GetActivityDungeon1007_MapBottom_2Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MapListByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MapListUis
**Snippet:**
```lua
function GetActivityDungeon1007_MapListUis(ui)
  local uis = {}
  
  uis.MapList = ui:GetChild("MapList")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Map_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Map_1Uis
**Snippet:**
```lua
function GetActivityDungeon1007_Map_1Uis(ui)
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

## Activty/a7/ActivityDungeon1007_Map_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Map_2Uis
**Snippet:**
```lua
function GetActivityDungeon1007_Map_2Uis(ui)
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

## Activty/a7/ActivityDungeon1007_MaterialBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MaterialBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1007_MaterialBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
```

---

## Activty/a7/ActivityDungeon1007_MaterialByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MaterialUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1007_Material_BattleNumberByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1007_Material_BattleNumberByName")

function GetActivityDungeon1007_MaterialUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.BattleNumber = GetActivityDungeon1007_Material_BattleNumberUis(ui:GetChild("BattleNumber"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a7/ActivityDungeon1007_MaterialWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MaterialWindowUis
**Requires:**
- ActivityDungeon1007_MaterialByName
**Snippet:**
```lua
require("ActivityDungeon1007_MaterialByName")

function GetActivityDungeon1007_MaterialWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1007_MaterialUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Material_BattleAniByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Material_BattleAniUis
**Requires:**
- ActivityDungeon1007_Material_BattleByName
**Snippet:**
```lua
require("ActivityDungeon1007_Material_BattleByName")

function GetActivityDungeon1007_Material_BattleAniUis(ui)
  local uis = {}
  uis.Battle = GetActivityDungeon1007_Material_BattleUis(ui:GetChild("Battle"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Material_BattleByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Material_BattleUis
**Snippet:**
```lua
function GetActivityDungeon1007_Material_BattleUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Material_BattleNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Material_BattleNumberUis
**Snippet:**
```lua
function GetActivityDungeon1007_Material_BattleNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MaxBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MaxBtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_MaxBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MinBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MinBtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_MinBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniExplainByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniExplainUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1007_MiniExplain_TipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1007_MiniExplain_TipsByName")

function GetActivityDungeon1007_MiniExplainUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Tips = GetActivityDungeon1007_MiniExplain_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
```

---

## Activty/a7/ActivityDungeon1007_MiniExplainWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniExplainWindowUis
**Requires:**
- ActivityDungeon1007_MiniExplainByName
**Snippet:**
```lua
require("ActivityDungeon1007_MiniExplainByName")

function GetActivityDungeon1007_MiniExplainWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1007_MiniExplainUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniExplain_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniExplain_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1007_MiniExplain_TipsUis(ui)
  local uis = {}
  
  uis.Word1List = ui:GetChild("Word1List")
  uis.Word2List = ui:GetChild("Word2List")
  uis.Word3List = ui:GetChild("Word3List")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniExplain_TipsCloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniExplain_TipsCloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_MiniExplain_TipsCloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniExplain_TipsWordByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniExplain_TipsWordUis
**Snippet:**
```lua
function GetActivityDungeon1007_MiniExplain_TipsWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniGameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniGameBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1007_MiniGameBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniGameByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniGameUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1007_MiniMain_TopByName
- ActivityDungeon1007_MiniMain_BottonByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1007_MiniMain_TopByName")
require("ActivityDungeon1007_MiniMain_BottonByName")

function GetActivityDungeon1007_MiniGameUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Top = GetActivityDungeon1007_MiniMain_TopUis(ui:GetChild("Top"))
  uis.Botton = GetActivityDungeon1007_MiniMain_BottonUis(ui:GetChild("Botton"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a7/ActivityDungeon1007_MiniGameStartByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniGameStartUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1007_MiniStart_OperateRegionByName
- ActivityDungeon1007_MiniStart_IntegralByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1007_MiniStart_OperateRegionByName")
require("ActivityDungeon1007_MiniStart_IntegralByName")

function GetActivityDungeon1007_MiniGameStartUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.OperateRegion = GetActivityDungeon1007_MiniStart_OperateRegionUis(ui:GetChild("OperateRegion"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
```

---

## Activty/a7/ActivityDungeon1007_MiniGameStartWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniGameStartWindowUis
**Requires:**
- ActivityDungeon1007_MiniGameStartByName
**Snippet:**
```lua
require("ActivityDungeon1007_MiniGameStartByName")

function GetActivityDungeon1007_MiniGameStartWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1007_MiniGameStartUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniGameWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniGameWindowUis
**Requires:**
- ActivityDungeon1007_MiniGameByName
**Snippet:**
```lua
require("ActivityDungeon1007_MiniGameByName")

function GetActivityDungeon1007_MiniGameWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1007_MiniGameUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniIntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniIntegralUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetActivityDungeon1007_MiniIntegralUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
  return uis
```

---

## Activty/a7/ActivityDungeon1007_MiniIntegralWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniIntegralWindowUis
**Requires:**
- ActivityDungeon1007_MiniIntegralByName
**Snippet:**
```lua
require("ActivityDungeon1007_MiniIntegralByName")

function GetActivityDungeon1007_MiniIntegralWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1007_MiniIntegralUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniIntegral_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniIntegral_TipsAniUis
**Requires:**
- ActivityDungeon1007_MiniIntegral_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1007_MiniIntegral_TipsByName")

function GetActivityDungeon1007_MiniIntegral_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1007_MiniIntegral_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniIntegral_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniIntegral_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1007_MiniIntegral_TipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniMain_BottonByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniMain_BottonUis
**Requires:**
- ActivityDungeon1007_MiniMain_TodayTaskByName
**Snippet:**
```lua
require("ActivityDungeon1007_MiniMain_TodayTaskByName")

function GetActivityDungeon1007_MiniMain_BottonUis(ui)
  local uis = {}
  uis.TaskBtn = ui:GetChild("TaskBtn")
  uis.RecordBtn = ui:GetChild("RecordBtn")
  uis.TodayTask = GetActivityDungeon1007_MiniMain_TodayTaskUis(ui:GetChild("TodayTask"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniMain_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniMain_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1007_MiniMain_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniMain_RecordBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniMain_RecordBtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_MiniMain_RecordBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniMain_StartBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniMain_StartBtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_MiniMain_StartBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniMain_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniMain_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1007_MiniMain_TaskBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniMain_TodayTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniMain_TodayTaskUis
**Requires:**
- ActivityDungeon1007_PassReward_AllFrame_EByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("ActivityDungeon1007_PassReward_AllFrame_EByName")
require("CommonResource_RedDotByName")

function GetActivityDungeon1007_MiniMain_TodayTaskUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1007_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a7/ActivityDungeon1007_MiniMain_TopByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniMain_TopUis
**Requires:**
- ActivityDungeon1007_MiniMain_IntegralByName
**Snippet:**
```lua
require("ActivityDungeon1007_MiniMain_IntegralByName")

function GetActivityDungeon1007_MiniMain_TopUis(ui)
  local uis = {}
  uis.Integral = GetActivityDungeon1007_MiniMain_IntegralUis(ui:GetChild("Integral"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniOperationByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniOperationUis
**Snippet:**
```lua
function GetActivityDungeon1007_MiniOperationUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniOperationWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniOperationWindowUis
**Requires:**
- ActivityDungeon1007_MiniOperationByName
**Snippet:**
```lua
require("ActivityDungeon1007_MiniOperationByName")

function GetActivityDungeon1007_MiniOperationWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1007_MiniOperationUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniStart_CloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniStart_CloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_MiniStart_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniStart_Column1ByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniStart_Column1Uis
**Snippet:**
```lua
function GetActivityDungeon1007_MiniStart_Column1Uis(ui)
  local uis = {}
  
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Effect3Holder = ui:GetChild("Effect3Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniStart_Column2ByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniStart_Column2Uis
**Snippet:**
```lua
function GetActivityDungeon1007_MiniStart_Column2Uis(ui)
  local uis = {}
  
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Effect3Holder = ui:GetChild("Effect3Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniStart_Column3ByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniStart_Column3Uis
**Snippet:**
```lua
function GetActivityDungeon1007_MiniStart_Column3Uis(ui)
  local uis = {}
  
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Effect3Holder = ui:GetChild("Effect3Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniStart_EndAgainBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniStart_EndAgainBtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_MiniStart_EndAgainBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniStart_EndCloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniStart_EndCloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_MiniStart_EndCloseBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniStart_EndRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniStart_EndRewardUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetActivityDungeon1007_MiniStart_EndRewardUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.AgainBtn = ui:GetChild("AgainBtn")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.root = ui
```

---

## Activty/a7/ActivityDungeon1007_MiniStart_EndRewardWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniStart_EndRewardWindowUis
**Requires:**
- ActivityDungeon1007_MiniStart_EndRewardByName
**Snippet:**
```lua
require("ActivityDungeon1007_MiniStart_EndRewardByName")

function GetActivityDungeon1007_MiniStart_EndRewardWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1007_MiniStart_EndRewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniStart_GuGuByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniStart_GuGuUis
**Snippet:**
```lua
function GetActivityDungeon1007_MiniStart_GuGuUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniStart_InfoByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniStart_InfoUis
**Snippet:**
```lua
function GetActivityDungeon1007_MiniStart_InfoUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniStart_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniStart_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1007_MiniStart_IntegralUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniStart_ItemAniByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniStart_ItemAniUis
**Requires:**
- ActivityDungeon1007_MiniStart_ItemByName
**Snippet:**
```lua
require("ActivityDungeon1007_MiniStart_ItemByName")

function GetActivityDungeon1007_MiniStart_ItemAniUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1007_MiniStart_ItemUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniStart_ItemByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniStart_ItemUis
**Snippet:**
```lua
function GetActivityDungeon1007_MiniStart_ItemUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniStart_OperateRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniStart_OperateRegionUis
**Snippet:**
```lua
function GetActivityDungeon1007_MiniStart_OperateRegionUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniStart_Vine1ByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniStart_Vine1Uis
**Snippet:**
```lua
function GetActivityDungeon1007_MiniStart_Vine1Uis(ui)
  local uis = {}
  
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Effect3Holder = ui:GetChild("Effect3Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniStart_Vine2ByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniStart_Vine2Uis
**Snippet:**
```lua
function GetActivityDungeon1007_MiniStart_Vine2Uis(ui)
  local uis = {}
  
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Effect3Holder = ui:GetChild("Effect3Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniStart_Vine3ByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniStart_Vine3Uis
**Snippet:**
```lua
function GetActivityDungeon1007_MiniStart_Vine3Uis(ui)
  local uis = {}
  
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Effect3Holder = ui:GetChild("Effect3Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniTaskUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1007_MiniTask_IntegralByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1007_MiniTask_IntegralByName")

function GetActivityDungeon1007_MiniTaskUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Integral = GetActivityDungeon1007_MiniTask_IntegralUis(ui:GetChild("Integral"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a7/ActivityDungeon1007_MiniTaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniTaskWindowUis
**Requires:**
- ActivityDungeon1007_MiniTaskByName
**Snippet:**
```lua
require("ActivityDungeon1007_MiniTaskByName")

function GetActivityDungeon1007_MiniTaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1007_MiniTaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniTask_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniTask_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1007_MiniTask_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniTask_RewardItemByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniTask_RewardItemUis
**Snippet:**
```lua
function GetActivityDungeon1007_MiniTask_RewardItemUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniTask_RewardItemGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniTask_RewardItemGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_MiniTask_RewardItemGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniTask_TipsAniUis
**Requires:**
- ActivityDungeon1007_MiniTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1007_MiniTask_TipsByName")

function GetActivityDungeon1007_MiniTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1007_MiniTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_MiniTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1007_MiniTask_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1007_MiniTask_TipsUis(ui)
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

## Activty/a7/ActivityDungeon1007_NormalBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_NormalBtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_NormalBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_NormalPoint1BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_NormalPoint1BtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_NormalPoint1BtnUis(ui)
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

## Activty/a7/ActivityDungeon1007_NormalPointBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_NormalPointBtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_NormalPointBtnUis(ui)
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

## Activty/a7/ActivityDungeon1007_NormalPointLockByName.lua.lua
**Functions:**
- GetActivityDungeon1007_NormalPointLockUis
**Snippet:**
```lua
function GetActivityDungeon1007_NormalPointLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_NumberStripByName.lua.lua
**Functions:**
- GetActivityDungeon1007_NumberStripUis
**Snippet:**
```lua
function GetActivityDungeon1007_NumberStripUis(ui)
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

## Activty/a7/ActivityDungeon1007_PassBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1007_PassBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_PassClothes_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassClothes_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_PassClothes_BuyBtnUis(ui)
  local uis = {}
  
  uis.PriceTxt = ui:GetChild("PriceTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_PassClothes_BuyRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassClothes_BuyRewardUis
**Snippet:**
```lua
function GetActivityDungeon1007_PassClothes_BuyRewardUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_PassClothes_CardQBByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassClothes_CardQBUis
**Snippet:**
```lua
function GetActivityDungeon1007_PassClothes_CardQBUis(ui)
  local uis = {}
  
  uis.QBHolder = ui:GetChild("QBHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_PassClothes_ClothseRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassClothes_ClothseRegionUis
**Requires:**
- ActivityDungeon1007_PassClothes_WordByName
- ActivityDungeon1007_PassClothes_CardQBByName
- ActivityDungeon1007_PassClothes_BuyRewardByName
**Snippet:**
```lua
require("ActivityDungeon1007_PassClothes_WordByName")
require("ActivityDungeon1007_PassClothes_CardQBByName")
require("ActivityDungeon1007_PassClothes_BuyRewardByName")

function GetActivityDungeon1007_PassClothes_ClothseRegionUis(ui)
  local uis = {}
  uis.Word = GetActivityDungeon1007_PassClothes_WordUis(ui:GetChild("Word"))
  uis.CardQB = GetActivityDungeon1007_PassClothes_CardQBUis(ui:GetChild("CardQB"))
  uis.BuyReward = GetActivityDungeon1007_PassClothes_BuyRewardUis(ui:GetChild("BuyReward"))
  uis.BuyBtn = ui:GetChild("BuyBtn")
```

---

## Activty/a7/ActivityDungeon1007_PassClothes_NameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassClothes_NameBtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_PassClothes_NameBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_PassClothes_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassClothes_WordUis
**Snippet:**
```lua
function GetActivityDungeon1007_PassClothes_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_PassportByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassportUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1007_PassReward_RewardRegionByName
- ActivityDungeon1007_PassTask_TaskRegionByName
- ActivityDungeon1007_PassClothes_ClothseRegionByName
- ActivityDungeon1007_Passport_LevelByName
- ActivityDungeon1007_Sign_TimeByName
- ActivityDungeon1007_Passport_TabRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1007_PassReward_RewardRegionByName")
require("ActivityDungeon1007_PassTask_TaskRegionByName")
require("ActivityDungeon1007_PassClothes_ClothseRegionByName")
require("ActivityDungeon1007_Passport_LevelByName")
require("ActivityDungeon1007_Sign_TimeByName")
require("ActivityDungeon1007_Passport_TabRegionByName")

function GetActivityDungeon1007_PassportUis(ui)
  local uis = {}
```

---

## Activty/a7/ActivityDungeon1007_PassportUp_LevelUpBgByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassportUp_LevelUpBgUis
**Snippet:**
```lua
function GetActivityDungeon1007_PassportUp_LevelUpBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_PassportUp_LevelUpTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassportUp_LevelUpTipsUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1007_PassportUp_LevelUpBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1007_PassportUp_LevelUpBgByName")

function GetActivityDungeon1007_PassportUp_LevelUpTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.LevelUpBg = GetActivityDungeon1007_PassportUp_LevelUpBgUis(ui:GetChild("LevelUpBg"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
```

---

## Activty/a7/ActivityDungeon1007_PassportUp_LevelUpTipsWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassportUp_LevelUpTipsWindowUis
**Requires:**
- ActivityDungeon1007_PassportUp_LevelUpTipsByName
**Snippet:**
```lua
require("ActivityDungeon1007_PassportUp_LevelUpTipsByName")

function GetActivityDungeon1007_PassportUp_LevelUpTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1007_PassportUp_LevelUpTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_PassportWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassportWindowUis
**Requires:**
- ActivityDungeon1007_PassportByName
**Snippet:**
```lua
require("ActivityDungeon1007_PassportByName")

function GetActivityDungeon1007_PassportWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1007_PassportUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Passport_AllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Passport_AllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_Passport_AllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Passport_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Passport_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_Passport_BuyBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Passport_ExpProgressBarByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Passport_ExpProgressBarUis
**Requires:**
- ActivityDungeon1007_Passport_ExpProgressFillByName
**Snippet:**
```lua
require("ActivityDungeon1007_Passport_ExpProgressFillByName")

function GetActivityDungeon1007_Passport_ExpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetActivityDungeon1007_Passport_ExpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Passport_ExpProgressFillByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Passport_ExpProgressFillUis
**Snippet:**
```lua
function GetActivityDungeon1007_Passport_ExpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Passport_LevelByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Passport_LevelUis
**Snippet:**
```lua
function GetActivityDungeon1007_Passport_LevelUis(ui)
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

## Activty/a7/ActivityDungeon1007_Passport_TabBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Passport_TabBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1007_Passport_TabBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## Activty/a7/ActivityDungeon1007_Passport_TabRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Passport_TabRegionUis
**Snippet:**
```lua
function GetActivityDungeon1007_Passport_TabRegionUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_PassReward_AllFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassReward_AllFrame_EUis
**Requires:**
- ActivityDungeon1007_PassReward_ItemFrame_EByName
- ActivityDungeon1007_PassReward_CardFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1007_PassReward_ItemFrame_EByName")
require("ActivityDungeon1007_PassReward_CardFrame_EByName")

function GetActivityDungeon1007_PassReward_AllFrame_EUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1007_PassReward_ItemFrame_EUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1007_PassReward_CardFrame_EUis(ui:GetChild("CardFrame"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## Activty/a7/ActivityDungeon1007_PassReward_AllFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassReward_AllFrame_MUis
**Requires:**
- ActivityDungeon1007_PassReward_ItemFrame_MByName
- ActivityDungeon1007_PassReward_CardFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1007_PassReward_ItemFrame_MByName")
require("ActivityDungeon1007_PassReward_CardFrame_MByName")

function GetActivityDungeon1007_PassReward_AllFrame_MUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1007_PassReward_ItemFrame_MUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1007_PassReward_CardFrame_MUis(ui:GetChild("CardFrame"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a7/ActivityDungeon1007_PassReward_CardFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassReward_CardFrame_EUis
**Requires:**
- ActivityDungeon1007_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1007_PassReward_ItemCardPicByName")

function GetActivityDungeon1007_PassReward_CardFrame_EUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1007_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a7/ActivityDungeon1007_PassReward_CardFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassReward_CardFrame_MUis
**Requires:**
- ActivityDungeon1007_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1007_PassReward_ItemCardPicByName")

function GetActivityDungeon1007_PassReward_CardFrame_MUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1007_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a7/ActivityDungeon1007_PassReward_EndTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassReward_EndTwoUis
**Requires:**
- ActivityDungeon1007_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1007_PassReward_AllFrame_EByName")

function GetActivityDungeon1007_PassReward_EndTwoUis(ui)
  local uis = {}
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.Item1 = GetActivityDungeon1007_PassReward_AllFrame_EUis(ui:GetChild("Item1"))
  uis.Item2 = GetActivityDungeon1007_PassReward_AllFrame_EUis(ui:GetChild("Item2"))
  uis.root = ui
```

---

## Activty/a7/ActivityDungeon1007_PassReward_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassReward_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1007_PassReward_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_PassReward_ItemFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassReward_ItemFrame_EUis
**Snippet:**
```lua
function GetActivityDungeon1007_PassReward_ItemFrame_EUis(ui)
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

## Activty/a7/ActivityDungeon1007_PassReward_ItemFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassReward_ItemFrame_MUis
**Snippet:**
```lua
function GetActivityDungeon1007_PassReward_ItemFrame_MUis(ui)
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

## Activty/a7/ActivityDungeon1007_PassReward_LevelTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassReward_LevelTitleUis
**Snippet:**
```lua
function GetActivityDungeon1007_PassReward_LevelTitleUis(ui)
  local uis = {}
  
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_PassReward_MiddleRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassReward_MiddleRegionUis
**Snippet:**
```lua
function GetActivityDungeon1007_PassReward_MiddleRegionUis(ui)
  local uis = {}
  
  uis.MiddleList = ui:GetChild("MiddleList")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_PassReward_MidTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassReward_MidTwoUis
**Requires:**
- ActivityDungeon1007_PassReward_MidTwoItemByName
- ActivityDungeon1007_PassReward_LevelTitleByName
**Snippet:**
```lua
require("ActivityDungeon1007_PassReward_MidTwoItemByName")
require("ActivityDungeon1007_PassReward_LevelTitleByName")

function GetActivityDungeon1007_PassReward_MidTwoUis(ui)
  local uis = {}
  uis.Reward1 = GetActivityDungeon1007_PassReward_MidTwoItemUis(ui:GetChild("Reward1"))
  uis.Reward2 = GetActivityDungeon1007_PassReward_MidTwoItemUis(ui:GetChild("Reward2"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Title = GetActivityDungeon1007_PassReward_LevelTitleUis(ui:GetChild("Title"))
```

---

## Activty/a7/ActivityDungeon1007_PassReward_MidTwoItemByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassReward_MidTwoItemUis
**Requires:**
- ActivityDungeon1007_PassReward_AllFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1007_PassReward_AllFrame_MByName")

function GetActivityDungeon1007_PassReward_MidTwoItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1007_PassReward_AllFrame_MUis(ui:GetChild("Item"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_PassReward_PicByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassReward_PicUis
**Snippet:**
```lua
function GetActivityDungeon1007_PassReward_PicUis(ui)
  local uis = {}
  
  uis.BuyTxt = ui:GetChild("BuyTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_PassReward_RewardRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassReward_RewardRegionUis
**Requires:**
- ActivityDungeon1007_PassReward_MiddleRegionByName
- ActivityDungeon1007_PassReward_StartTwoByName
- ActivityDungeon1007_PassReward_EndTwoByName
**Snippet:**
```lua
require("ActivityDungeon1007_PassReward_MiddleRegionByName")
require("ActivityDungeon1007_PassReward_StartTwoByName")
require("ActivityDungeon1007_PassReward_EndTwoByName")

function GetActivityDungeon1007_PassReward_RewardRegionUis(ui)
  local uis = {}
  uis.MiddleList = GetActivityDungeon1007_PassReward_MiddleRegionUis(ui:GetChild("MiddleList"))
  uis.StartTwo = GetActivityDungeon1007_PassReward_StartTwoUis(ui:GetChild("StartTwo"))
  uis.EndTwo = GetActivityDungeon1007_PassReward_EndTwoUis(ui:GetChild("EndTwo"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a7/ActivityDungeon1007_PassReward_StartTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassReward_StartTwoUis
**Requires:**
- ActivityDungeon1007_PassReward_PicByName
**Snippet:**
```lua
require("ActivityDungeon1007_PassReward_PicByName")

function GetActivityDungeon1007_PassReward_StartTwoUis(ui)
  local uis = {}
  uis.Pic = GetActivityDungeon1007_PassReward_PicUis(ui:GetChild("Pic"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_PassTask_TaskRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassTask_TaskRegionUis
**Requires:**
- ActivityDungeon1007_TaskMaxByName
**Snippet:**
```lua
require("ActivityDungeon1007_TaskMaxByName")

function GetActivityDungeon1007_PassTask_TaskRegionUis(ui)
  local uis = {}
  uis.TipsList = ui:GetChild("TipsList")
  uis.Max = GetActivityDungeon1007_TaskMaxUis(ui:GetChild("Max"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_PassTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassTask_TipsAniUis
**Requires:**
- ActivityDungeon1007_PassTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1007_PassTask_TipsByName")

function GetActivityDungeon1007_PassTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1007_PassTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_PassTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassTask_TipsUis
**Requires:**
- ActivityDungeon1007_PassTask_TipsIntegralByName
**Snippet:**
```lua
require("ActivityDungeon1007_PassTask_TipsIntegralByName")

function GetActivityDungeon1007_PassTask_TipsUis(ui)
  local uis = {}
  uis.ProgressTxt = ui:GetChild("ProgressTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Integral = GetActivityDungeon1007_PassTask_TipsIntegralUis(ui:GetChild("Integral"))
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a7/ActivityDungeon1007_PassTask_TipsIntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PassTask_TipsIntegralUis
**Snippet:**
```lua
function GetActivityDungeon1007_PassTask_TipsIntegralUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_PlotBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PlotBtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_PlotBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_PlotByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PlotUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1007_Plot_WordByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1007_Plot_WordByName")

function GetActivityDungeon1007_PlotUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Word = GetActivityDungeon1007_Plot_WordUis(ui:GetChild("Word"))
  uis.PlotList = ui:GetChild("PlotList")
  uis.ProspectBtn = ui:GetChild("ProspectBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a7/ActivityDungeon1007_PlotWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1007_PlotWindowUis
**Requires:**
- ActivityDungeon1007_PlotByName
**Snippet:**
```lua
require("ActivityDungeon1007_PlotByName")

function GetActivityDungeon1007_PlotWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1007_PlotUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Plot_ProspectBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Plot_ProspectBtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_Plot_ProspectBtnUis(ui)
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

## Activty/a7/ActivityDungeon1007_Plot_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Plot_TipsAniUis
**Requires:**
- ActivityDungeon1007_Plot_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1007_Plot_TipsByName")

function GetActivityDungeon1007_Plot_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1007_Plot_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Plot_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Plot_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1007_Plot_TipsUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Plot_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Plot_WordUis
**Snippet:**
```lua
function GetActivityDungeon1007_Plot_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_ReduceBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_ReduceBtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_ReduceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_ReviewWordByName.lua.lua
**Functions:**
- GetActivityDungeon1007_ReviewWordUis
**Snippet:**
```lua
function GetActivityDungeon1007_ReviewWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_ShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_ShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_ShopBtnUis(ui)
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

## Activty/a7/ActivityDungeon1007_ShopByName.lua.lua
**Functions:**
- GetActivityDungeon1007_ShopUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1007_Shop_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1007_Shop_TimeByName")

function GetActivityDungeon1007_ShopUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Time = GetActivityDungeon1007_Shop_TimeUis(ui:GetChild("Time"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a7/ActivityDungeon1007_ShopWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1007_ShopWindowUis
**Requires:**
- ActivityDungeon1007_ShopByName
**Snippet:**
```lua
require("ActivityDungeon1007_ShopByName")

function GetActivityDungeon1007_ShopWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1007_ShopUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Shop_CardHeadBgByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Shop_CardHeadBgUis
**Snippet:**
```lua
function GetActivityDungeon1007_Shop_CardHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Shop_ItemAniByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Shop_ItemAniUis
**Requires:**
- ActivityDungeon1007_Shop_ItemByName
**Snippet:**
```lua
require("ActivityDungeon1007_Shop_ItemByName")

function GetActivityDungeon1007_Shop_ItemAniUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1007_Shop_ItemUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Shop_ItemBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Shop_ItemBtnUis
**Requires:**
- ActivityDungeon1007_Shop_CardHeadBgByName
- ActivityDungeon1007_Shop_ItemNumberByName
- ActivityDungeon1007_Shop_UseMarkByName
**Snippet:**
```lua
require("ActivityDungeon1007_Shop_CardHeadBgByName")
require("ActivityDungeon1007_Shop_ItemNumberByName")
require("ActivityDungeon1007_Shop_UseMarkByName")

function GetActivityDungeon1007_Shop_ItemBtnUis(ui)
  local uis = {}
  uis.CardHeadBg = GetActivityDungeon1007_Shop_CardHeadBgUis(ui:GetChild("CardHeadBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.ItemNumber = GetActivityDungeon1007_Shop_ItemNumberUis(ui:GetChild("ItemNumber"))
```

---

## Activty/a7/ActivityDungeon1007_Shop_ItemByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Shop_ItemUis
**Requires:**
- ActivityDungeon1007_Shop_SellOutByName
**Snippet:**
```lua
require("ActivityDungeon1007_Shop_SellOutByName")

function GetActivityDungeon1007_Shop_ItemUis(ui)
  local uis = {}
  uis.ItemBtn = ui:GetChild("ItemBtn")
  uis.SellOut = GetActivityDungeon1007_Shop_SellOutUis(ui:GetChild("SellOut"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Shop_ItemNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Shop_ItemNumberUis
**Snippet:**
```lua
function GetActivityDungeon1007_Shop_ItemNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Shop_ItemRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Shop_ItemRegionUis
**Requires:**
- ActivityDungeon1007_Shop_TitleByName
**Snippet:**
```lua
require("ActivityDungeon1007_Shop_TitleByName")

function GetActivityDungeon1007_Shop_ItemRegionUis(ui)
  local uis = {}
  uis.ShopTitle = GetActivityDungeon1007_Shop_TitleUis(ui:GetChild("ShopTitle"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Shop_SellOutByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Shop_SellOutUis
**Snippet:**
```lua
function GetActivityDungeon1007_Shop_SellOutUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Shop_StarByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Shop_StarUis
**Snippet:**
```lua
function GetActivityDungeon1007_Shop_StarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Shop_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Shop_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1007_Shop_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Shop_TitleByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Shop_TitleUis
**Snippet:**
```lua
function GetActivityDungeon1007_Shop_TitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Shop_UseMarkByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Shop_UseMarkUis
**Snippet:**
```lua
function GetActivityDungeon1007_Shop_UseMarkUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_SignBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_SignBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1007_SignBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_SignByName.lua.lua
**Functions:**
- GetActivityDungeon1007_SignUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1007_Sign_RewardListByName
- ActivityDungeon1007_Sign_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1007_Sign_RewardListByName")
require("ActivityDungeon1007_Sign_TimeByName")

function GetActivityDungeon1007_SignUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.RewardList = GetActivityDungeon1007_Sign_RewardListUis(ui:GetChild("RewardList"))
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.Time = GetActivityDungeon1007_Sign_TimeUis(ui:GetChild("Time"))
```

---

## Activty/a7/ActivityDungeon1007_SignWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1007_SignWindowUis
**Requires:**
- ActivityDungeon1007_SignByName
**Snippet:**
```lua
require("ActivityDungeon1007_SignByName")

function GetActivityDungeon1007_SignWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1007_SignUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Sign_AllFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Sign_AllFrameUis
**Requires:**
- ActivityDungeon1007_Sign_ItemFrameByName
- ActivityDungeon1007_Sign_CardFrameByName
**Snippet:**
```lua
require("ActivityDungeon1007_Sign_ItemFrameByName")
require("ActivityDungeon1007_Sign_CardFrameByName")

function GetActivityDungeon1007_Sign_AllFrameUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1007_Sign_ItemFrameUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1007_Sign_CardFrameUis(ui:GetChild("CardFrame"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a7/ActivityDungeon1007_Sign_CardFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Sign_CardFrameUis
**Requires:**
- ActivityDungeon1007_Sign_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1007_Sign_ItemCardPicByName")

function GetActivityDungeon1007_Sign_CardFrameUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1007_Sign_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a7/ActivityDungeon1007_Sign_GetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Sign_GetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_Sign_GetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Sign_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Sign_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1007_Sign_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Sign_ItemFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Sign_ItemFrameUis
**Snippet:**
```lua
function GetActivityDungeon1007_Sign_ItemFrameUis(ui)
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

## Activty/a7/ActivityDungeon1007_Sign_RewardAniByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Sign_RewardAniUis
**Requires:**
- ActivityDungeon1007_Sign_RewardByName
**Snippet:**
```lua
require("ActivityDungeon1007_Sign_RewardByName")

function GetActivityDungeon1007_Sign_RewardAniUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1007_Sign_RewardUis(ui:GetChild("Reward"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Sign_RewardByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Sign_RewardUis
**Requires:**
- ActivityDungeon1007_Sign_AllFrameByName
**Snippet:**
```lua
require("ActivityDungeon1007_Sign_AllFrameByName")

function GetActivityDungeon1007_Sign_RewardUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1007_Sign_AllFrameUis(ui:GetChild("Item"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Sign_RewardListByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Sign_RewardListUis
**Snippet:**
```lua
function GetActivityDungeon1007_Sign_RewardListUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_Sign_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1007_Sign_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1007_Sign_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_TaskAllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_TaskAllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_TaskAllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1007_TaskBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_TaskByName.lua.lua
**Functions:**
- GetActivityDungeon1007_TaskUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1007_TaskTitleByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1007_TaskTitleByName")

function GetActivityDungeon1007_TaskUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TaskTitle = GetActivityDungeon1007_TaskTitleUis(ui:GetChild("TaskTitle"))
  uis.TaskTipsList = ui:GetChild("TaskTipsList")
  uis.AllGetBtn = ui:GetChild("AllGetBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a7/ActivityDungeon1007_TaskGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1007_TaskGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1007_TaskGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_TaskMaxByName.lua.lua
**Functions:**
- GetActivityDungeon1007_TaskMaxUis
**Snippet:**
```lua
function GetActivityDungeon1007_TaskMaxUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_TaskProgressByName.lua.lua
**Functions:**
- GetActivityDungeon1007_TaskProgressUis
**Snippet:**
```lua
function GetActivityDungeon1007_TaskProgressUis(ui)
  local uis = {}
  
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_TaskTipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1007_TaskTipsAniUis
**Requires:**
- ActivityDungeon1007_TaskTipsByName
**Snippet:**
```lua
require("ActivityDungeon1007_TaskTipsByName")

function GetActivityDungeon1007_TaskTipsAniUis(ui)
  local uis = {}
  uis.TaskTips = GetActivityDungeon1007_TaskTipsUis(ui:GetChild("TaskTips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_TaskTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1007_TaskTipsUis
**Requires:**
- ActivityDungeon1007_TaskProgressByName
**Snippet:**
```lua
require("ActivityDungeon1007_TaskProgressByName")

function GetActivityDungeon1007_TaskTipsUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.RewardList = ui:GetChild("RewardList")
  uis.TaskProgress = GetActivityDungeon1007_TaskProgressUis(ui:GetChild("TaskProgress"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a7/ActivityDungeon1007_TaskTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1007_TaskTitleUis
**Snippet:**
```lua
function GetActivityDungeon1007_TaskTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a7/ActivityDungeon1007_TaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1007_TaskWindowUis
**Requires:**
- ActivityDungeon1007_TaskByName
**Snippet:**
```lua
require("ActivityDungeon1007_TaskByName")

function GetActivityDungeon1007_TaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1007_TaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---
