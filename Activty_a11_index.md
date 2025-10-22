# Activty/a11

## Activty/a11/ActivityDungeon1011_ActivityDungeonByName.lua.lua
**Functions:**
- GetActivityDungeon1011_ActivityDungeonUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1011_MainTitleByName
- ActivityDungeon1011_ReviewWordByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1011_MainTitleByName")
require("ActivityDungeon1011_ReviewWordByName")
require("CommonResource_CurrencyReturnByName")

function GetActivityDungeon1011_ActivityDungeonUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.MainTitle = GetActivityDungeon1011_MainTitleUis(ui:GetChild("MainTitle"))
  uis.PlotBtn = ui:GetChild("PlotBtn")
```

---

## Activty/a11/ActivityDungeon1011_ActivityDungeonWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1011_ActivityDungeonWindowUis
**Requires:**
- ActivityDungeon1011_ActivityDungeonByName
**Snippet:**
```lua
require("ActivityDungeon1011_ActivityDungeonByName")

function GetActivityDungeon1011_ActivityDungeonWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1011_ActivityDungeonUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_AddBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_AddBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_AddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_BossBattleByName.lua.lua
**Functions:**
- GetActivityDungeon1011_BossBattleUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1011_BossBattle_InfoByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1011_BossBattle_InfoByName")

function GetActivityDungeon1011_BossBattleUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.Info = GetActivityDungeon1011_BossBattle_InfoUis(ui:GetChild("Info"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a11/ActivityDungeon1011_BossBattleWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1011_BossBattleWindowUis
**Requires:**
- ActivityDungeon1011_BossBattleByName
**Snippet:**
```lua
require("ActivityDungeon1011_BossBattleByName")

function GetActivityDungeon1011_BossBattleWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1011_BossBattleUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_BossBattle_Info1ByName.lua.lua
**Functions:**
- GetActivityDungeon1011_BossBattle_Info1Uis
**Snippet:**
```lua
function GetActivityDungeon1011_BossBattle_Info1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_BossBattle_InfoByName.lua.lua
**Functions:**
- GetActivityDungeon1011_BossBattle_InfoUis
**Requires:**
- ActivityDungeon1011_BossBattle_Info1ByName
**Snippet:**
```lua
require("ActivityDungeon1011_BossBattle_Info1ByName")

function GetActivityDungeon1011_BossBattle_InfoUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = GetActivityDungeon1011_BossBattle_Info1Uis(ui:GetChild("WordTxt"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_BossBattle_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1011_BossBattle_TipsAniUis
**Requires:**
- ActivityDungeon1011_BossBattle_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1011_BossBattle_TipsByName")

function GetActivityDungeon1011_BossBattle_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1011_BossBattle_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_BossBattle_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1011_BossBattle_TipsUis
**Requires:**
- ActivityDungeon1011_BossBattle_TipsRewardByName
**Snippet:**
```lua
require("ActivityDungeon1011_BossBattle_TipsRewardByName")

function GetActivityDungeon1011_BossBattle_TipsUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1011_BossBattle_TipsRewardUis(ui:GetChild("Reward"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.NumberWordTxt = ui:GetChild("NumberWordTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a11/ActivityDungeon1011_BossBattle_TipsRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1011_BossBattle_TipsRewardUis
**Snippet:**
```lua
function GetActivityDungeon1011_BossBattle_TipsRewardUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_BossBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_BossBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_BossBtnUis(ui)
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

## Activty/a11/ActivityDungeon1011_BuyLevelBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_BuyLevelBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_BuyLevelBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_BuyLevelDes1ByName.lua.lua
**Functions:**
- GetActivityDungeon1011_BuyLevelDes1Uis
**Requires:**
- ActivityDungeon1011_NumberStripByName
- ActivityDungeon1011_BuyPriceNumberByName
**Snippet:**
```lua
require("ActivityDungeon1011_NumberStripByName")
require("ActivityDungeon1011_BuyPriceNumberByName")

function GetActivityDungeon1011_BuyLevelDes1Uis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.NumberStrip = GetActivityDungeon1011_NumberStripUis(ui:GetChild("NumberStrip"))
  uis.BuyPriceNumber = GetActivityDungeon1011_BuyPriceNumberUis(ui:GetChild("BuyPriceNumber"))
```

---

## Activty/a11/ActivityDungeon1011_BuyLevelDes2ByName.lua.lua
**Functions:**
- GetActivityDungeon1011_BuyLevelDes2Uis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1011_BuyLevelDes1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1011_BuyLevelDes1ByName")

function GetActivityDungeon1011_BuyLevelDes2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.BuyLevelDes1 = GetActivityDungeon1011_BuyLevelDes1Uis(ui:GetChild("BuyLevelDes1"))
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.root = ui
```

---

## Activty/a11/ActivityDungeon1011_BuyLevelDesWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1011_BuyLevelDesWindowUis
**Requires:**
- ActivityDungeon1011_BuyLevelDes2ByName
**Snippet:**
```lua
require("ActivityDungeon1011_BuyLevelDes2ByName")

function GetActivityDungeon1011_BuyLevelDesWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1011_BuyLevelDes2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_BuyLevelItemByName.lua.lua
**Functions:**
- GetActivityDungeon1011_BuyLevelItemUis
**Requires:**
- ActivityDungeon1011_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1011_PassReward_AllFrame_EByName")

function GetActivityDungeon1011_BuyLevelItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1011_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_BuyPriceNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1011_BuyPriceNumberUis
**Snippet:**
```lua
function GetActivityDungeon1011_BuyPriceNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_ChallengeByName.lua.lua
**Functions:**
- GetActivityDungeon1011_ChallengeUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1011_MapListByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1011_MapListByName")

function GetActivityDungeon1011_ChallengeUis(ui)
  local uis = {}
  uis.BgList = ui:GetChild("BgList")
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Map = GetActivityDungeon1011_MapListUis(ui:GetChild("Map"))
  uis.ShopBtn = ui:GetChild("ShopBtn")
  uis.ChapterList = ui:GetChild("ChapterList")
```

---

## Activty/a11/ActivityDungeon1011_ChallengeChapterBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_ChallengeChapterBtnUis
**Requires:**
- ActivityDungeon1011_NormalPointLockByName
**Snippet:**
```lua
require("ActivityDungeon1011_NormalPointLockByName")

function GetActivityDungeon1011_ChallengeChapterBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Lock = GetActivityDungeon1011_NormalPointLockUis(ui:GetChild("Lock"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Activty/a11/ActivityDungeon1011_ChallengeShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_ChallengeShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_ChallengeShopBtnUis(ui)
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

## Activty/a11/ActivityDungeon1011_ChallengeWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1011_ChallengeWindowUis
**Requires:**
- ActivityDungeon1011_ChallengeByName
**Snippet:**
```lua
require("ActivityDungeon1011_ChallengeByName")

function GetActivityDungeon1011_ChallengeWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1011_ChallengeUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MainTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MainTitleUis
**Snippet:**
```lua
function GetActivityDungeon1011_MainTitleUis(ui)
  local uis = {}
  
  uis.Time1Txt = ui:GetChild("Time1Txt")
  uis.Time2Txt = ui:GetChild("Time2Txt")
  uis.reviewCtr = ui:GetController("review")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MapBottom_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MapBottom_1Uis
**Snippet:**
```lua
function GetActivityDungeon1011_MapBottom_1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MapBottom_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MapBottom_2Uis
**Snippet:**
```lua
function GetActivityDungeon1011_MapBottom_2Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MapListByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MapListUis
**Snippet:**
```lua
function GetActivityDungeon1011_MapListUis(ui)
  local uis = {}
  
  uis.MapList = ui:GetChild("MapList")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Map_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Map_1Uis
**Snippet:**
```lua
function GetActivityDungeon1011_Map_1Uis(ui)
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

## Activty/a11/ActivityDungeon1011_Map_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Map_2Uis
**Snippet:**
```lua
function GetActivityDungeon1011_Map_2Uis(ui)
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

## Activty/a11/ActivityDungeon1011_MaterialBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MaterialBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1011_MaterialBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
```

---

## Activty/a11/ActivityDungeon1011_MaterialByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MaterialUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1011_Material_BattleNumberByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1011_Material_BattleNumberByName")

function GetActivityDungeon1011_MaterialUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.BattleNumber = GetActivityDungeon1011_Material_BattleNumberUis(ui:GetChild("BattleNumber"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a11/ActivityDungeon1011_MaterialWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MaterialWindowUis
**Requires:**
- ActivityDungeon1011_MaterialByName
**Snippet:**
```lua
require("ActivityDungeon1011_MaterialByName")

function GetActivityDungeon1011_MaterialWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1011_MaterialUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Material_BattleAniByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Material_BattleAniUis
**Requires:**
- ActivityDungeon1011_Material_BattleByName
**Snippet:**
```lua
require("ActivityDungeon1011_Material_BattleByName")

function GetActivityDungeon1011_Material_BattleAniUis(ui)
  local uis = {}
  uis.Battle = GetActivityDungeon1011_Material_BattleUis(ui:GetChild("Battle"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Material_BattleByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Material_BattleUis
**Snippet:**
```lua
function GetActivityDungeon1011_Material_BattleUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Material_BattleNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Material_BattleNumberUis
**Snippet:**
```lua
function GetActivityDungeon1011_Material_BattleNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MaxBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MaxBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_MaxBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MinBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MinBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_MinBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniExplainByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniExplainUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1011_MiniExplain_TipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1011_MiniExplain_TipsByName")

function GetActivityDungeon1011_MiniExplainUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Tips = GetActivityDungeon1011_MiniExplain_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
```

---

## Activty/a11/ActivityDungeon1011_MiniExplainWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniExplainWindowUis
**Requires:**
- ActivityDungeon1011_MiniExplainByName
**Snippet:**
```lua
require("ActivityDungeon1011_MiniExplainByName")

function GetActivityDungeon1011_MiniExplainWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1011_MiniExplainUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniExplain_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniExplain_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniExplain_TipsUis(ui)
  local uis = {}
  
  uis.ContentList = ui:GetChild("ContentList")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniExplain_TipsCloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniExplain_TipsCloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniExplain_TipsCloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniExplain_TipsContentByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniExplain_TipsContentUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniExplain_TipsContentUis(ui)
  local uis = {}
  
  uis.WordList = ui:GetChild("WordList")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniExplain_TipsContentWordByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniExplain_TipsContentWordUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniExplain_TipsContentWordUis(ui)
  local uis = {}
  
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniExplain_TipsWordByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniExplain_TipsWordUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniExplain_TipsWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniGameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniGameBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1011_MiniGameBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniGameByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniGameUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1011_MiniMain_TopByName
- ActivityDungeon1011_MiniMain_BottonByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1011_MiniMain_TopByName")
require("ActivityDungeon1011_MiniMain_BottonByName")

function GetActivityDungeon1011_MiniGameUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Top = GetActivityDungeon1011_MiniMain_TopUis(ui:GetChild("Top"))
  uis.Botton = GetActivityDungeon1011_MiniMain_BottonUis(ui:GetChild("Botton"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a11/ActivityDungeon1011_MiniGameChoiceByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniGameChoiceUis
**Requires:**
- CommonResource_BackGroundByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")

function GetActivityDungeon1011_MiniGameChoiceUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.StartBtn = ui:GetChild("StartBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
  return uis
```

---

## Activty/a11/ActivityDungeon1011_MiniGameChoiceWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniGameChoiceWindowUis
**Requires:**
- ActivityDungeon1011_MiniGameChoiceByName
**Snippet:**
```lua
require("ActivityDungeon1011_MiniGameChoiceByName")

function GetActivityDungeon1011_MiniGameChoiceWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1011_MiniGameChoiceUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniGameChoice_MapByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniGameChoice_MapUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniGameChoice_MapUis(ui)
  local uis = {}
  
  uis.DotList = ui:GetChild("DotList")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniGameChoice_MapDotByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniGameChoice_MapDotUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniGameChoice_MapDotUis(ui)
  local uis = {}
  
  uis.Dot1Btn = ui:GetChild("Dot1Btn")
  uis.Dot2Btn = ui:GetChild("Dot2Btn")
  uis.Dot3Btn = ui:GetChild("Dot3Btn")
  uis.Dot4Btn = ui:GetChild("Dot4Btn")
  uis.Dot5Btn = ui:GetChild("Dot5Btn")
  uis.Dot6Btn = ui:GetChild("Dot6Btn")
  uis.Dot7Btn = ui:GetChild("Dot7Btn")
```

---

## Activty/a11/ActivityDungeon1011_MiniGameChoice_StartBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniGameChoice_StartBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniGameChoice_StartBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniGameChoice_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniGameChoice_TipsAniUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniGameChoice_TipsAniUis(ui)
  local uis = {}
  
  uis.TipsBtn = ui:GetChild("TipsBtn")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniGameChoice_TipsBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniGameChoice_TipsBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniGameChoice_TipsBtnUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniGameStartByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniGameStartUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1011_MiniStart_BoxRegionByName
- ActivityDungeon1011_MiniStart_HandRegionByName
- ActivityDungeon1011_MiniStart_LaunchByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1011_MiniStart_BoxRegionByName")
require("ActivityDungeon1011_MiniStart_HandRegionByName")
require("ActivityDungeon1011_MiniStart_LaunchByName")

function GetActivityDungeon1011_MiniGameStartUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BoxRegion = GetActivityDungeon1011_MiniStart_BoxRegionUis(ui:GetChild("BoxRegion"))
  uis.HandRegion = GetActivityDungeon1011_MiniStart_HandRegionUis(ui:GetChild("HandRegion"))
```

---

## Activty/a11/ActivityDungeon1011_MiniGameStartWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniGameStartWindowUis
**Requires:**
- ActivityDungeon1011_MiniGameStartByName
**Snippet:**
```lua
require("ActivityDungeon1011_MiniGameStartByName")

function GetActivityDungeon1011_MiniGameStartWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1011_MiniGameStartUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniGameWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniGameWindowUis
**Requires:**
- ActivityDungeon1011_MiniGameByName
**Snippet:**
```lua
require("ActivityDungeon1011_MiniGameByName")

function GetActivityDungeon1011_MiniGameWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1011_MiniGameUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniMain_BottonByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniMain_BottonUis
**Requires:**
- ActivityDungeon1011_MiniMain_TodayTaskByName
**Snippet:**
```lua
require("ActivityDungeon1011_MiniMain_TodayTaskByName")

function GetActivityDungeon1011_MiniMain_BottonUis(ui)
  local uis = {}
  uis.TaskBtn = ui:GetChild("TaskBtn")
  uis.TodayTask = GetActivityDungeon1011_MiniMain_TodayTaskUis(ui:GetChild("TodayTask"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniMain_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniMain_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniMain_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniMain_StartBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniMain_StartBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniMain_StartBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniMain_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniMain_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1011_MiniMain_TaskBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniMain_TodayTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniMain_TodayTaskUis
**Requires:**
- ActivityDungeon1011_PassReward_AllFrame_EByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("ActivityDungeon1011_PassReward_AllFrame_EByName")
require("CommonResource_RedDotByName")

function GetActivityDungeon1011_MiniMain_TodayTaskUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1011_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a11/ActivityDungeon1011_MiniMain_TopByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniMain_TopUis
**Requires:**
- ActivityDungeon1011_MiniMain_IntegralByName
**Snippet:**
```lua
require("ActivityDungeon1011_MiniMain_IntegralByName")

function GetActivityDungeon1011_MiniMain_TopUis(ui)
  local uis = {}
  uis.Integral = GetActivityDungeon1011_MiniMain_IntegralUis(ui:GetChild("Integral"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniStart_BeadByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniStart_BeadUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniStart_BeadUis(ui)
  local uis = {}
  
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.c1Ctr = ui:GetController("c1")
  uis.effectCtr = ui:GetController("effect")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniStart_BeadRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniStart_BeadRegionUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniStart_BeadRegionUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniStart_BoxRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniStart_BoxRegionUis
**Requires:**
- ActivityDungeon1011_MiniStart_BeadRegionByName
- ActivityDungeon1011_MiniStart_BoxShadeByName
**Snippet:**
```lua
require("ActivityDungeon1011_MiniStart_BeadRegionByName")
require("ActivityDungeon1011_MiniStart_BoxShadeByName")

function GetActivityDungeon1011_MiniStart_BoxRegionUis(ui)
  local uis = {}
  uis.BeadRegion = GetActivityDungeon1011_MiniStart_BeadRegionUis(ui:GetChild("BeadRegion"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.BoxShade = GetActivityDungeon1011_MiniStart_BoxShadeUis(ui:GetChild("BoxShade"))
  uis.root = ui
  return uis
```

---

## Activty/a11/ActivityDungeon1011_MiniStart_BoxShadeByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniStart_BoxShadeUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniStart_BoxShadeUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniStart_CloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniStart_CloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniStart_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniStart_DirectionBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniStart_DirectionBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniStart_DirectionBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniStart_EndAgainBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniStart_EndAgainBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniStart_EndAgainBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniStart_EndCloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniStart_EndCloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniStart_EndCloseBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniStart_EndFailByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniStart_EndFailUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniStart_EndFailUis(ui)
  local uis = {}
  
  uis.NumberWordTxt = ui:GetChild("NumberWordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniStart_EndRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniStart_EndRewardUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1011_MiniStart_EndFailByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1011_MiniStart_EndFailByName")

function GetActivityDungeon1011_MiniStart_EndRewardUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EndFail = GetActivityDungeon1011_MiniStart_EndFailUis(ui:GetChild("EndFail"))
  uis.AgainBtn = ui:GetChild("AgainBtn")
```

---

## Activty/a11/ActivityDungeon1011_MiniStart_EndRewardWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniStart_EndRewardWindowUis
**Requires:**
- ActivityDungeon1011_MiniStart_EndRewardByName
**Snippet:**
```lua
require("ActivityDungeon1011_MiniStart_EndRewardByName")

function GetActivityDungeon1011_MiniStart_EndRewardWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1011_MiniStart_EndRewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniStart_ExchangeBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniStart_ExchangeBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniStart_ExchangeBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniStart_HandRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniStart_HandRegionUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniStart_HandRegionUis(ui)
  local uis = {}
  
  uis.LeftBtn = ui:GetChild("LeftBtn")
  uis.RightBtn = ui:GetChild("RightBtn")
  uis.ShootBtn = ui:GetChild("ShootBtn")
  uis.ExchangeBtn = ui:GetChild("ExchangeBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Activty/a11/ActivityDungeon1011_MiniStart_ItemByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniStart_ItemUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniStart_ItemUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniStart_LaunchByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniStart_LaunchUis
**Requires:**
- ActivityDungeon1011_MiniStart_BeadByName
**Snippet:**
```lua
require("ActivityDungeon1011_MiniStart_BeadByName")

function GetActivityDungeon1011_MiniStart_LaunchUis(ui)
  local uis = {}
  uis.ArrowImage = ui:GetChild("ArrowImage")
  uis.Bead1 = GetActivityDungeon1011_MiniStart_BeadUis(ui:GetChild("Bead1"))
  uis.Bead2 = GetActivityDungeon1011_MiniStart_BeadUis(ui:GetChild("Bead2"))
  uis.SwitchBtn = ui:GetChild("SwitchBtn")
  uis.ItemList = ui:GetChild("ItemList")
  uis.NumberTxt = ui:GetChild("NumberTxt")
```

---

## Activty/a11/ActivityDungeon1011_MiniStart_ShootBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniStart_ShootBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniStart_ShootBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniStart_SwitchBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniStart_SwitchBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniStart_SwitchBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniTaskUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1011_MiniTask_IntegralByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1011_MiniTask_IntegralByName")

function GetActivityDungeon1011_MiniTaskUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Integral = GetActivityDungeon1011_MiniTask_IntegralUis(ui:GetChild("Integral"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a11/ActivityDungeon1011_MiniTaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniTaskWindowUis
**Requires:**
- ActivityDungeon1011_MiniTaskByName
**Snippet:**
```lua
require("ActivityDungeon1011_MiniTaskByName")

function GetActivityDungeon1011_MiniTaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1011_MiniTaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniTask_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniTask_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniTask_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniTask_RewardItemByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniTask_RewardItemUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniTask_RewardItemUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniTask_RewardItemGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniTask_RewardItemGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniTask_RewardItemGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniTask_TipsAniUis
**Requires:**
- ActivityDungeon1011_MiniTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1011_MiniTask_TipsByName")

function GetActivityDungeon1011_MiniTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1011_MiniTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_MiniTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1011_MiniTask_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1011_MiniTask_TipsUis(ui)
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

## Activty/a11/ActivityDungeon1011_NormalBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_NormalBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_NormalBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_NormalPoint1BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_NormalPoint1BtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_NormalPoint1BtnUis(ui)
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

## Activty/a11/ActivityDungeon1011_NormalPoint2BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_NormalPoint2BtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_NormalPoint2BtnUis(ui)
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

## Activty/a11/ActivityDungeon1011_NormalPointLockByName.lua.lua
**Functions:**
- GetActivityDungeon1011_NormalPointLockUis
**Snippet:**
```lua
function GetActivityDungeon1011_NormalPointLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_NumberStripByName.lua.lua
**Functions:**
- GetActivityDungeon1011_NumberStripUis
**Snippet:**
```lua
function GetActivityDungeon1011_NumberStripUis(ui)
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

## Activty/a11/ActivityDungeon1011_PassBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1011_PassBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_PassClothes_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassClothes_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_PassClothes_BuyBtnUis(ui)
  local uis = {}
  
  uis.PriceTxt = ui:GetChild("PriceTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_PassClothes_BuyRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassClothes_BuyRewardUis
**Snippet:**
```lua
function GetActivityDungeon1011_PassClothes_BuyRewardUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_PassClothes_CardQBByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassClothes_CardQBUis
**Snippet:**
```lua
function GetActivityDungeon1011_PassClothes_CardQBUis(ui)
  local uis = {}
  
  uis.QBHolder = ui:GetChild("QBHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_PassClothes_ClothseRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassClothes_ClothseRegionUis
**Requires:**
- ActivityDungeon1011_PassClothes_WordByName
- ActivityDungeon1011_PassClothes_CardQBByName
- ActivityDungeon1011_PassClothes_BuyRewardByName
**Snippet:**
```lua
require("ActivityDungeon1011_PassClothes_WordByName")
require("ActivityDungeon1011_PassClothes_CardQBByName")
require("ActivityDungeon1011_PassClothes_BuyRewardByName")

function GetActivityDungeon1011_PassClothes_ClothseRegionUis(ui)
  local uis = {}
  uis.Word = GetActivityDungeon1011_PassClothes_WordUis(ui:GetChild("Word"))
  uis.CardQB = GetActivityDungeon1011_PassClothes_CardQBUis(ui:GetChild("CardQB"))
  uis.BuyReward = GetActivityDungeon1011_PassClothes_BuyRewardUis(ui:GetChild("BuyReward"))
  uis.BuyBtn = ui:GetChild("BuyBtn")
```

---

## Activty/a11/ActivityDungeon1011_PassClothes_NameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassClothes_NameBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_PassClothes_NameBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_PassClothes_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassClothes_WordUis
**Snippet:**
```lua
function GetActivityDungeon1011_PassClothes_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_PassportByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassportUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1011_PassReward_RewardRegionByName
- ActivityDungeon1011_PassTask_TaskRegionByName
- ActivityDungeon1011_PassClothes_ClothseRegionByName
- ActivityDungeon1011_Passport_LevelByName
- ActivityDungeon1011_Sign_TimeByName
- ActivityDungeon1011_Passport_TabRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1011_PassReward_RewardRegionByName")
require("ActivityDungeon1011_PassTask_TaskRegionByName")
require("ActivityDungeon1011_PassClothes_ClothseRegionByName")
require("ActivityDungeon1011_Passport_LevelByName")
require("ActivityDungeon1011_Sign_TimeByName")
require("ActivityDungeon1011_Passport_TabRegionByName")

function GetActivityDungeon1011_PassportUis(ui)
  local uis = {}
```

---

## Activty/a11/ActivityDungeon1011_PassportUp_LevelUpBgByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassportUp_LevelUpBgUis
**Snippet:**
```lua
function GetActivityDungeon1011_PassportUp_LevelUpBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_PassportUp_LevelUpTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassportUp_LevelUpTipsUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1011_PassportUp_LevelUpBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1011_PassportUp_LevelUpBgByName")

function GetActivityDungeon1011_PassportUp_LevelUpTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.LevelUpBg = GetActivityDungeon1011_PassportUp_LevelUpBgUis(ui:GetChild("LevelUpBg"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
```

---

## Activty/a11/ActivityDungeon1011_PassportUp_LevelUpTipsWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassportUp_LevelUpTipsWindowUis
**Requires:**
- ActivityDungeon1011_PassportUp_LevelUpTipsByName
**Snippet:**
```lua
require("ActivityDungeon1011_PassportUp_LevelUpTipsByName")

function GetActivityDungeon1011_PassportUp_LevelUpTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1011_PassportUp_LevelUpTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_PassportWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassportWindowUis
**Requires:**
- ActivityDungeon1011_PassportByName
**Snippet:**
```lua
require("ActivityDungeon1011_PassportByName")

function GetActivityDungeon1011_PassportWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1011_PassportUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Passport_AllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Passport_AllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_Passport_AllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Passport_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Passport_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_Passport_BuyBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Passport_ExpProgressBarByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Passport_ExpProgressBarUis
**Requires:**
- ActivityDungeon1011_Passport_ExpProgressFillByName
**Snippet:**
```lua
require("ActivityDungeon1011_Passport_ExpProgressFillByName")

function GetActivityDungeon1011_Passport_ExpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetActivityDungeon1011_Passport_ExpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Passport_ExpProgressFillByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Passport_ExpProgressFillUis
**Snippet:**
```lua
function GetActivityDungeon1011_Passport_ExpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Passport_LevelByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Passport_LevelUis
**Snippet:**
```lua
function GetActivityDungeon1011_Passport_LevelUis(ui)
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

## Activty/a11/ActivityDungeon1011_Passport_TabBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Passport_TabBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1011_Passport_TabBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## Activty/a11/ActivityDungeon1011_Passport_TabRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Passport_TabRegionUis
**Snippet:**
```lua
function GetActivityDungeon1011_Passport_TabRegionUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_PassReward_AllFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassReward_AllFrame_EUis
**Requires:**
- ActivityDungeon1011_PassReward_ItemFrame_EByName
- ActivityDungeon1011_PassReward_CardFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1011_PassReward_ItemFrame_EByName")
require("ActivityDungeon1011_PassReward_CardFrame_EByName")

function GetActivityDungeon1011_PassReward_AllFrame_EUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1011_PassReward_ItemFrame_EUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1011_PassReward_CardFrame_EUis(ui:GetChild("CardFrame"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## Activty/a11/ActivityDungeon1011_PassReward_AllFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassReward_AllFrame_MUis
**Requires:**
- ActivityDungeon1011_PassReward_ItemFrame_MByName
- ActivityDungeon1011_PassReward_CardFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1011_PassReward_ItemFrame_MByName")
require("ActivityDungeon1011_PassReward_CardFrame_MByName")

function GetActivityDungeon1011_PassReward_AllFrame_MUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1011_PassReward_ItemFrame_MUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1011_PassReward_CardFrame_MUis(ui:GetChild("CardFrame"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a11/ActivityDungeon1011_PassReward_CardFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassReward_CardFrame_EUis
**Requires:**
- ActivityDungeon1011_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1011_PassReward_ItemCardPicByName")

function GetActivityDungeon1011_PassReward_CardFrame_EUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1011_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a11/ActivityDungeon1011_PassReward_CardFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassReward_CardFrame_MUis
**Requires:**
- ActivityDungeon1011_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1011_PassReward_ItemCardPicByName")

function GetActivityDungeon1011_PassReward_CardFrame_MUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1011_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a11/ActivityDungeon1011_PassReward_EndTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassReward_EndTwoUis
**Requires:**
- ActivityDungeon1011_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1011_PassReward_AllFrame_EByName")

function GetActivityDungeon1011_PassReward_EndTwoUis(ui)
  local uis = {}
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.Item1 = GetActivityDungeon1011_PassReward_AllFrame_EUis(ui:GetChild("Item1"))
  uis.Item2 = GetActivityDungeon1011_PassReward_AllFrame_EUis(ui:GetChild("Item2"))
  uis.root = ui
```

---

## Activty/a11/ActivityDungeon1011_PassReward_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassReward_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1011_PassReward_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_PassReward_ItemFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassReward_ItemFrame_EUis
**Snippet:**
```lua
function GetActivityDungeon1011_PassReward_ItemFrame_EUis(ui)
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

## Activty/a11/ActivityDungeon1011_PassReward_ItemFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassReward_ItemFrame_MUis
**Snippet:**
```lua
function GetActivityDungeon1011_PassReward_ItemFrame_MUis(ui)
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

## Activty/a11/ActivityDungeon1011_PassReward_LevelTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassReward_LevelTitleUis
**Snippet:**
```lua
function GetActivityDungeon1011_PassReward_LevelTitleUis(ui)
  local uis = {}
  
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_PassReward_MiddleRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassReward_MiddleRegionUis
**Snippet:**
```lua
function GetActivityDungeon1011_PassReward_MiddleRegionUis(ui)
  local uis = {}
  
  uis.MiddleList = ui:GetChild("MiddleList")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_PassReward_MidTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassReward_MidTwoUis
**Requires:**
- ActivityDungeon1011_PassReward_MidTwoItemByName
- ActivityDungeon1011_PassReward_LevelTitleByName
**Snippet:**
```lua
require("ActivityDungeon1011_PassReward_MidTwoItemByName")
require("ActivityDungeon1011_PassReward_LevelTitleByName")

function GetActivityDungeon1011_PassReward_MidTwoUis(ui)
  local uis = {}
  uis.Reward1 = GetActivityDungeon1011_PassReward_MidTwoItemUis(ui:GetChild("Reward1"))
  uis.Reward2 = GetActivityDungeon1011_PassReward_MidTwoItemUis(ui:GetChild("Reward2"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Title = GetActivityDungeon1011_PassReward_LevelTitleUis(ui:GetChild("Title"))
```

---

## Activty/a11/ActivityDungeon1011_PassReward_MidTwoItemByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassReward_MidTwoItemUis
**Requires:**
- ActivityDungeon1011_PassReward_AllFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1011_PassReward_AllFrame_MByName")

function GetActivityDungeon1011_PassReward_MidTwoItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1011_PassReward_AllFrame_MUis(ui:GetChild("Item"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_PassReward_PicByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassReward_PicUis
**Snippet:**
```lua
function GetActivityDungeon1011_PassReward_PicUis(ui)
  local uis = {}
  
  uis.BuyTxt = ui:GetChild("BuyTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_PassReward_RewardRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassReward_RewardRegionUis
**Requires:**
- ActivityDungeon1011_PassReward_MiddleRegionByName
- ActivityDungeon1011_PassReward_StartTwoByName
- ActivityDungeon1011_PassReward_EndTwoByName
**Snippet:**
```lua
require("ActivityDungeon1011_PassReward_MiddleRegionByName")
require("ActivityDungeon1011_PassReward_StartTwoByName")
require("ActivityDungeon1011_PassReward_EndTwoByName")

function GetActivityDungeon1011_PassReward_RewardRegionUis(ui)
  local uis = {}
  uis.MiddleList = GetActivityDungeon1011_PassReward_MiddleRegionUis(ui:GetChild("MiddleList"))
  uis.StartTwo = GetActivityDungeon1011_PassReward_StartTwoUis(ui:GetChild("StartTwo"))
  uis.EndTwo = GetActivityDungeon1011_PassReward_EndTwoUis(ui:GetChild("EndTwo"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a11/ActivityDungeon1011_PassReward_StartTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassReward_StartTwoUis
**Requires:**
- ActivityDungeon1011_PassReward_PicByName
**Snippet:**
```lua
require("ActivityDungeon1011_PassReward_PicByName")

function GetActivityDungeon1011_PassReward_StartTwoUis(ui)
  local uis = {}
  uis.Pic = GetActivityDungeon1011_PassReward_PicUis(ui:GetChild("Pic"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_PassTask_TaskRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassTask_TaskRegionUis
**Requires:**
- ActivityDungeon1011_TaskMaxByName
**Snippet:**
```lua
require("ActivityDungeon1011_TaskMaxByName")

function GetActivityDungeon1011_PassTask_TaskRegionUis(ui)
  local uis = {}
  uis.TipsList = ui:GetChild("TipsList")
  uis.Max = GetActivityDungeon1011_TaskMaxUis(ui:GetChild("Max"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_PassTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassTask_TipsAniUis
**Requires:**
- ActivityDungeon1011_PassTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1011_PassTask_TipsByName")

function GetActivityDungeon1011_PassTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1011_PassTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_PassTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassTask_TipsUis
**Requires:**
- ActivityDungeon1011_PassTask_TipsIntegralByName
**Snippet:**
```lua
require("ActivityDungeon1011_PassTask_TipsIntegralByName")

function GetActivityDungeon1011_PassTask_TipsUis(ui)
  local uis = {}
  uis.ProgressTxt = ui:GetChild("ProgressTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Integral = GetActivityDungeon1011_PassTask_TipsIntegralUis(ui:GetChild("Integral"))
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a11/ActivityDungeon1011_PassTask_TipsIntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PassTask_TipsIntegralUis
**Snippet:**
```lua
function GetActivityDungeon1011_PassTask_TipsIntegralUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_PlotBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PlotBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_PlotBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_PlotByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PlotUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1011_Plot_WordByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1011_Plot_WordByName")

function GetActivityDungeon1011_PlotUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Word = GetActivityDungeon1011_Plot_WordUis(ui:GetChild("Word"))
  uis.PlotList = ui:GetChild("PlotList")
  uis.ProspectBtn = ui:GetChild("ProspectBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a11/ActivityDungeon1011_PlotWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1011_PlotWindowUis
**Requires:**
- ActivityDungeon1011_PlotByName
**Snippet:**
```lua
require("ActivityDungeon1011_PlotByName")

function GetActivityDungeon1011_PlotWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1011_PlotUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Plot_ProspectBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Plot_ProspectBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_Plot_ProspectBtnUis(ui)
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

## Activty/a11/ActivityDungeon1011_Plot_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Plot_TipsAniUis
**Requires:**
- ActivityDungeon1011_Plot_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1011_Plot_TipsByName")

function GetActivityDungeon1011_Plot_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1011_Plot_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Plot_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Plot_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1011_Plot_TipsUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Plot_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Plot_WordUis
**Snippet:**
```lua
function GetActivityDungeon1011_Plot_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_ReduceBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_ReduceBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_ReduceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_ReviewWordByName.lua.lua
**Functions:**
- GetActivityDungeon1011_ReviewWordUis
**Snippet:**
```lua
function GetActivityDungeon1011_ReviewWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_ShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_ShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_ShopBtnUis(ui)
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

## Activty/a11/ActivityDungeon1011_ShopByName.lua.lua
**Functions:**
- GetActivityDungeon1011_ShopUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1011_Shop_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1011_Shop_TimeByName")

function GetActivityDungeon1011_ShopUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Time = GetActivityDungeon1011_Shop_TimeUis(ui:GetChild("Time"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a11/ActivityDungeon1011_ShopWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1011_ShopWindowUis
**Requires:**
- ActivityDungeon1011_ShopByName
**Snippet:**
```lua
require("ActivityDungeon1011_ShopByName")

function GetActivityDungeon1011_ShopWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1011_ShopUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Shop_CardHeadBgByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Shop_CardHeadBgUis
**Snippet:**
```lua
function GetActivityDungeon1011_Shop_CardHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Shop_ItemAniByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Shop_ItemAniUis
**Requires:**
- ActivityDungeon1011_Shop_ItemByName
**Snippet:**
```lua
require("ActivityDungeon1011_Shop_ItemByName")

function GetActivityDungeon1011_Shop_ItemAniUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1011_Shop_ItemUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Shop_ItemBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Shop_ItemBtnUis
**Requires:**
- ActivityDungeon1011_Shop_CardHeadBgByName
- ActivityDungeon1011_Shop_ItemNumberByName
- ActivityDungeon1011_Shop_UseMarkByName
**Snippet:**
```lua
require("ActivityDungeon1011_Shop_CardHeadBgByName")
require("ActivityDungeon1011_Shop_ItemNumberByName")
require("ActivityDungeon1011_Shop_UseMarkByName")

function GetActivityDungeon1011_Shop_ItemBtnUis(ui)
  local uis = {}
  uis.CardHeadBg = GetActivityDungeon1011_Shop_CardHeadBgUis(ui:GetChild("CardHeadBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.ItemNumber = GetActivityDungeon1011_Shop_ItemNumberUis(ui:GetChild("ItemNumber"))
```

---

## Activty/a11/ActivityDungeon1011_Shop_ItemByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Shop_ItemUis
**Requires:**
- ActivityDungeon1011_Shop_SellOutByName
**Snippet:**
```lua
require("ActivityDungeon1011_Shop_SellOutByName")

function GetActivityDungeon1011_Shop_ItemUis(ui)
  local uis = {}
  uis.ItemBtn = ui:GetChild("ItemBtn")
  uis.SellOut = GetActivityDungeon1011_Shop_SellOutUis(ui:GetChild("SellOut"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Shop_ItemNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Shop_ItemNumberUis
**Snippet:**
```lua
function GetActivityDungeon1011_Shop_ItemNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Shop_ItemRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Shop_ItemRegionUis
**Requires:**
- ActivityDungeon1011_Shop_TitleByName
**Snippet:**
```lua
require("ActivityDungeon1011_Shop_TitleByName")

function GetActivityDungeon1011_Shop_ItemRegionUis(ui)
  local uis = {}
  uis.ShopTitle = GetActivityDungeon1011_Shop_TitleUis(ui:GetChild("ShopTitle"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Shop_SellOutByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Shop_SellOutUis
**Snippet:**
```lua
function GetActivityDungeon1011_Shop_SellOutUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Shop_StarByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Shop_StarUis
**Snippet:**
```lua
function GetActivityDungeon1011_Shop_StarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Shop_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Shop_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1011_Shop_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Shop_TitleByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Shop_TitleUis
**Snippet:**
```lua
function GetActivityDungeon1011_Shop_TitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Shop_UseMarkByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Shop_UseMarkUis
**Snippet:**
```lua
function GetActivityDungeon1011_Shop_UseMarkUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_SignBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_SignBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1011_SignBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_SignByName.lua.lua
**Functions:**
- GetActivityDungeon1011_SignUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1011_Sign_RewardListByName
- ActivityDungeon1011_Sign_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1011_Sign_RewardListByName")
require("ActivityDungeon1011_Sign_TimeByName")

function GetActivityDungeon1011_SignUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.RewardList = GetActivityDungeon1011_Sign_RewardListUis(ui:GetChild("RewardList"))
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.Time = GetActivityDungeon1011_Sign_TimeUis(ui:GetChild("Time"))
```

---

## Activty/a11/ActivityDungeon1011_SignWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1011_SignWindowUis
**Requires:**
- ActivityDungeon1011_SignByName
**Snippet:**
```lua
require("ActivityDungeon1011_SignByName")

function GetActivityDungeon1011_SignWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1011_SignUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Sign_AllFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Sign_AllFrameUis
**Requires:**
- ActivityDungeon1011_Sign_ItemFrameByName
- ActivityDungeon1011_Sign_CardFrameByName
**Snippet:**
```lua
require("ActivityDungeon1011_Sign_ItemFrameByName")
require("ActivityDungeon1011_Sign_CardFrameByName")

function GetActivityDungeon1011_Sign_AllFrameUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1011_Sign_ItemFrameUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1011_Sign_CardFrameUis(ui:GetChild("CardFrame"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a11/ActivityDungeon1011_Sign_CardFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Sign_CardFrameUis
**Requires:**
- ActivityDungeon1011_Sign_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1011_Sign_ItemCardPicByName")

function GetActivityDungeon1011_Sign_CardFrameUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1011_Sign_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a11/ActivityDungeon1011_Sign_GetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Sign_GetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_Sign_GetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Sign_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Sign_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1011_Sign_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Sign_ItemFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Sign_ItemFrameUis
**Snippet:**
```lua
function GetActivityDungeon1011_Sign_ItemFrameUis(ui)
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

## Activty/a11/ActivityDungeon1011_Sign_RewardAniByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Sign_RewardAniUis
**Requires:**
- ActivityDungeon1011_Sign_RewardByName
**Snippet:**
```lua
require("ActivityDungeon1011_Sign_RewardByName")

function GetActivityDungeon1011_Sign_RewardAniUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1011_Sign_RewardUis(ui:GetChild("Reward"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Sign_RewardByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Sign_RewardUis
**Requires:**
- ActivityDungeon1011_Sign_AllFrameByName
**Snippet:**
```lua
require("ActivityDungeon1011_Sign_AllFrameByName")

function GetActivityDungeon1011_Sign_RewardUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1011_Sign_AllFrameUis(ui:GetChild("Item"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Sign_RewardListByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Sign_RewardListUis
**Snippet:**
```lua
function GetActivityDungeon1011_Sign_RewardListUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_Sign_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1011_Sign_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1011_Sign_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_TaskAllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_TaskAllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_TaskAllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1011_TaskBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_TaskByName.lua.lua
**Functions:**
- GetActivityDungeon1011_TaskUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1011_TaskTitleByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1011_TaskTitleByName")

function GetActivityDungeon1011_TaskUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TaskTitle = GetActivityDungeon1011_TaskTitleUis(ui:GetChild("TaskTitle"))
  uis.TaskTipsList = ui:GetChild("TaskTipsList")
  uis.AllGetBtn = ui:GetChild("AllGetBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a11/ActivityDungeon1011_TaskGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1011_TaskGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1011_TaskGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_TaskMaxByName.lua.lua
**Functions:**
- GetActivityDungeon1011_TaskMaxUis
**Snippet:**
```lua
function GetActivityDungeon1011_TaskMaxUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_TaskProgressByName.lua.lua
**Functions:**
- GetActivityDungeon1011_TaskProgressUis
**Snippet:**
```lua
function GetActivityDungeon1011_TaskProgressUis(ui)
  local uis = {}
  
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_TaskTipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1011_TaskTipsAniUis
**Requires:**
- ActivityDungeon1011_TaskTipsByName
**Snippet:**
```lua
require("ActivityDungeon1011_TaskTipsByName")

function GetActivityDungeon1011_TaskTipsAniUis(ui)
  local uis = {}
  uis.TaskTips = GetActivityDungeon1011_TaskTipsUis(ui:GetChild("TaskTips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_TaskTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1011_TaskTipsUis
**Requires:**
- ActivityDungeon1011_TaskProgressByName
**Snippet:**
```lua
require("ActivityDungeon1011_TaskProgressByName")

function GetActivityDungeon1011_TaskTipsUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.RewardList = ui:GetChild("RewardList")
  uis.TaskProgress = GetActivityDungeon1011_TaskProgressUis(ui:GetChild("TaskProgress"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a11/ActivityDungeon1011_TaskTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1011_TaskTitleUis
**Snippet:**
```lua
function GetActivityDungeon1011_TaskTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a11/ActivityDungeon1011_TaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1011_TaskWindowUis
**Requires:**
- ActivityDungeon1011_TaskByName
**Snippet:**
```lua
require("ActivityDungeon1011_TaskByName")

function GetActivityDungeon1011_TaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1011_TaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---
