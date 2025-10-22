# Badge

## Badge/BadgeCardAttributeTipsWindow.lua.lua
**Functions:**
- BadgeCardAttributeTipsWindow.ReInitData
- BadgeCardAttributeTipsWindow.OnInit
- BadgeCardAttributeTipsWindow.UpdateInfo
- BadgeCardAttributeTipsWindow.InitBtn
- BadgeCardAttributeTipsWindow.OnClose
**Requires:**
- CardAttribute_CardAttributeTipsWindowByName
**Snippet:**
```lua
require("CardAttribute_CardAttributeTipsWindowByName")
local BadgeCardAttributeTipsWindow = {}
local uis, contentPane, info

function BadgeCardAttributeTipsWindow.ReInitData()
end

function BadgeCardAttributeTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BadgeCardAttributeTipsWindow.package, WinResConfig.BadgeCardAttributeTipsWindow.comName, function(com)
    contentPane = com
```

---

## Badge/BadgeCardInfoWindow.lua.lua
**Functions:**
- BadgeCardInfoWindow.ReInitData
- BadgeCardInfoWindow.OnInit
- BadgeCardInfoWindow.GetData
- BadgeCardInfoWindow.ShowAttribute
- BadgeCardInfoWindow.ShowAddAttribute
- list.itemRenderer
- list.itemRenderer
- list.itemRenderer
- list.itemRenderer
- list.itemRenderer
- detailItemlist.itemRenderer
- BadgeCardInfoWindow.InitUI
- tablist.itemRenderer
- BadgeCardInfoWindow.GetSkillInfo
- BadgeCardInfoWindow.UpdateInfo
- uis.Main.SpclSkillTipsList.itemRenderer
- list.itemRenderer
- BadgeCardInfoWindow.ShowSkillDes
- list.itemRenderer
- BadgeCardInfoWindow.InitBtn
- BadgeCardInfoWindow.OnClose
**Requires:**
- CardAttribute_BadgeCardInfoWindowByName
**Snippet:**
```lua
require("CardAttribute_BadgeCardInfoWindowByName")
local BadgeCardInfoWindow = {}
local uis, contentPane, cardInfo, skillInfo, displayDetailMode

function BadgeCardInfoWindow.ReInitData()
end

function BadgeCardInfoWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BadgeCardInfoWindow.package, WinResConfig.BadgeCardInfoWindow.comName, function(com)
    contentPane = com
```

---

## Badge/BadgeData.lua.lua
**Functions:**
- BadgeData.InitScreeningData
- BadgeData.IsScreen
- BadgeData.InitSortData
- BadgeData.DeleteOneSuitId
- BadgeData.DeleteOneMainAttribute
- BadgeData.DeleteOneViceAttribute
- BadgeData.UpdateTakeoffOrWearInfo
- BadgeData.GetAttribute
- BadgeData.GetBadgeByPart
- BadgeData.GetBadgePartName
- BadgeData.GetBadgeAttributeName
- BadgeData.GetAttributeNameByInfo
- BadgeData.GetMainAttribute
- BadgeData.GetSuitCountBySuitId
- BadgeData.GetDefaultScreeningResult
- BadgeData.SortByStar
- BadgeData.SortByLevel
**Snippet:**
```lua
BadgeData = {}
BADGE_SORT_TYPE_ENUM = {STAR = 0, LEVEL = 1}

function BadgeData.InitScreeningData()
  BadgeData.SuitId = {}
  BadgeData.StarNum = {}
  BadgeData.MainAttribute = {}
  BadgeData.ViceAttribute = {}
end

```

---

## Badge/BadgeDecomposeWindow.lua.lua
**Functions:**
- BadgeDecomposeWindow.ReInitData
- BadgeDecomposeWindow.OnInit
- BadgeDecomposeWindow.UpdateInfo
- BadgeDecomposeWindow.GetClearNew
- BadgeDecomposeWindow.GetListMinLen
- BadgeDecomposeWindow.PartListItem
- BadgeDecomposeWindow.InitDecomposeData
- BadgeDecomposeWindow.GetDecomposeItem
- BadgeDecomposeWindow.GetBadgeExp
- BadgeDecomposeWindow.ShowNum
- list.itemRenderer
- BadgeDecomposeWindow.StopAnim
- BadgeDecomposeWindow.InitText
- BadgeDecomposeWindow.ShowSortBtnName
- BadgeDecomposeWindow.InitBtn
- BadgeDecomposeWindow.IsSatrMax
- BadgeDecomposeWindow.GetSelectUid
- BadgeDecomposeWindow.UpdateItemList
- BadgeDecomposeWindow.HandleMessage
- BadgeDecomposeWindow.OnClose
**Requires:**
- Badge_BadgeDecomposeWindowByName
**Snippet:**
```lua
require("Badge_BadgeDecomposeWindowByName")
local BadgeDecomposeWindow = {}
local uis, contentPane, jumpTb
local isPlayAnim = true
local curPartData, allSelect, selectItem, animTime, lastItemIndex, lastUid, backUpdate, reverseSort, itemExpSort, expPre
local ITEM_STATE_ENUM = {
  NONE = 0,
  SELECT_LOOK = 1,
  LOOK = 2,
  SELECT = 3
```

---

## Badge/BadgeExchangeWindow.lua.lua
**Functions:**
- BadgeExchangeWindow.ReInitData
- BadgeExchangeWindow.OnInit
- BadgeExchangeWindow.ShowCard
- BadgeExchangeWindow.UpdateInfo
- BadgeExchangeWindow.ShowHead
- BadgeExchangeWindow.InitBtn
- BadgeExchangeWindow.CloseWindow
- BadgeExchangeWindow.OnClose
**Requires:**
- Badge_ExchangeWindowByName
**Snippet:**
```lua
require("Badge_ExchangeWindowByName")
local BadgeExchangeWindow = {}
local uis, contentPane, target

function BadgeExchangeWindow.ReInitData()
end

function BadgeExchangeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BadgeExchangeWindow.package, WinResConfig.BadgeExchangeWindow.comName, function(com)
    contentPane = com
```

---

## Badge/BadgeFilterSortWindow.lua.lua
**Functions:**
- BadgeFilterSortWindow.ReInitData
- BadgeFilterSortWindow.OnInit
- BadgeFilterSortWindow.UpdateInfo
- starList.itemRenderer
- attributeList.itemRenderer
- BadgeFilterSortWindow.Remove
- BadgeFilterSortWindow.InitBtn
- BadgeFilterSortWindow.CloseWindow
- BadgeFilterSortWindow.OnClose
**Requires:**
- Badge_FilterSortWindowByName
**Snippet:**
```lua
require("Badge_FilterSortWindowByName")
local BadgeFilterSortWindow = {}
local uis, contentPane

function BadgeFilterSortWindow.ReInitData()
end

function BadgeFilterSortWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BadgeFilterSortWindow.package, WinResConfig.BadgeFilterSortWindow.comName, function(com)
    contentPane = com
```

---

## Badge/BadgeGetTipsWindow.lua.lua
**Functions:**
- BadgeGetTipsWindow.ReInitData
- BadgeGetTipsWindow.OnInit
- BadgeGetTipsWindow.UpdateInfo
- uis.Main.WordList.itemRenderer
- BadgeGetTipsWindow.InitBtn
- BadgeGetTipsWindow.OnClose
**Requires:**
- Message_BadgeGetTipsWindowByName
**Snippet:**
```lua
require("Message_BadgeGetTipsWindowByName")
local BadgeGetTipsWindow = {}
local uis, contentPane, badgeConfig

function BadgeGetTipsWindow.ReInitData()
end

function BadgeGetTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BadgeGetTipsWindow.package, WinResConfig.BadgeGetTipsWindow.comName, function(com)
    contentPane = com
```

---

## Badge/BadgeGetTips_BadgeGetTipsByName.lua.lua
**Functions:**
- GetBadgeGetTips_BadgeGetTipsUis
**Requires:**
- CommonResource_BackGroundByName
- BadgeGetTips_LightByName
- BadgeGetTips_BadgePicByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("BadgeGetTips_LightByName")
require("BadgeGetTips_BadgePicByName")

function GetBadgeGetTips_BadgeGetTipsUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Light = GetBadgeGetTips_LightUis(ui:GetChild("Light"))
  uis.BadgePic = GetBadgeGetTips_BadgePicUis(ui:GetChild("BadgePic"))
  uis.ElementList = ui:GetChild("ElementList")
```

---

## Badge/BadgeGetTips_BadgeGetTipsWindowByName.lua.lua
**Functions:**
- GetBadgeGetTips_BadgeGetTipsWindowUis
**Requires:**
- BadgeGetTips_BadgeGetTipsByName
**Snippet:**
```lua
require("BadgeGetTips_BadgeGetTipsByName")

function GetBadgeGetTips_BadgeGetTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetBadgeGetTips_BadgeGetTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeGetTips_BadgePicByName.lua.lua
**Functions:**
- GetBadgeGetTips_BadgePicUis
**Snippet:**
```lua
function GetBadgeGetTips_BadgePicUis(ui)
  local uis = {}
  
  uis.BadgeLoader = ui:GetChild("BadgeLoader")
  uis.BadgeHolder = ui:GetChild("BadgeHolder")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeGetTips_LightByName.lua.lua
**Functions:**
- GetBadgeGetTips_LightUis
**Snippet:**
```lua
function GetBadgeGetTips_LightUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeInfoTipsWindow.lua.lua
**Functions:**
- BadgeInfoTipsWindow.ReInitData
- BadgeInfoTipsWindow.OnInit
- BadgeInfoTipsWindow.UpdateInfo
- viceList.itemRenderer
- suitList.itemRenderer
- BadgeInfoTipsWindow.GetGoToData
- BadgeInfoTipsWindow.StageIsUnlock
- BadgeInfoTipsWindow.ShowAllGoTo
- uis.Main.Way.GetStripList.itemRenderer
- BadgeInfoTipsWindow.ShowGoTo
- uis.Main.Way.GetStripList.itemRenderer
- BadgeInfoTipsWindow.CloseWindow
- BadgeInfoTipsWindow.InitBtn
- BadgeInfoTipsWindow.OnClose
**Requires:**
- Message_BadgeInfoTipsWindowByName
**Snippet:**
```lua
require("Message_BadgeInfoTipsWindowByName")
local BadgeInfoTipsWindow = {}
local uis, contentPane, badgeData, badgeInfo, wayData, jumpData, notShowWay

function BadgeInfoTipsWindow.ReInitData()
end

function BadgeInfoTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BadgeInfoTipsWindow.package, WinResConfig.BadgeInfoTipsWindow.comName, function(com)
    contentPane = com
```

---

## Badge/BadgeLevelUpTipsWindow.lua.lua
**Functions:**
- BadgeLevelUpTipsWindow.ReInitData
- BadgeLevelUpTipsWindow.OnInit
- BadgeLevelUpTipsWindow.UpdateInfo
- BadgeLevelUpTipsWindow.CloseWindow
- BadgeLevelUpTipsWindow.InitBtn
- BadgeLevelUpTipsWindow.OnClose
**Requires:**
- Badge_LevelUpTipsWindowByName
**Snippet:**
```lua
require("Badge_LevelUpTipsWindowByName")
local BadgeLevelUpTipsWindow = {}
local uis, contentPane, info

function BadgeLevelUpTipsWindow.ReInitData()
end

function BadgeLevelUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BadgeLevelUpTipsWindow.package, WinResConfig.BadgeLevelUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## Badge/BadgeMgr.lua.lua
**Functions:**
- BadgeMgr.CheckSuit
- BadgeMgr.ShowBadgeTextInfo
- info2.AttributeList.itemRenderer
- list.itemRenderer
- suitList.itemRenderer
- info3.InfoList.itemRenderer
- BadgeMgr.ShowBadgeItem
- BadgeMgr.ShowPartInfo
- BadgeMgr.ShowStar
- BadgeMgr.ShowLevel
- BadgeMgr.ShowHead
- BadgeMgr.OpenBadgeDecompose
- BadgeMgr.Init
**Snippet:**
```lua
BadgeMgr = {}
BadgeMgr.mainAttributeCtr = {
  [1] = 0,
  [2] = 1,
  [3] = 2,
  [7] = 3,
  [8] = 4,
  [9] = 5,
  [11] = 6,
  [12] = 7,
```

---

## Badge/BadgeOverviewWindow.lua.lua
**Functions:**
- BadgeOverviewWindow.ReInitData
- BadgeOverviewWindow.OnInit
- BadgeOverviewWindow.UpdateCardList
- cardList.itemRenderer
- BadgeOverviewWindow.StopAnim
- BadgeOverviewWindow.UpdateInfo
- topList.itemRenderer
- BadgeOverviewWindow.ShowCard
- list.itemRenderer
- BadgeOverviewWindow.ShowTeam
- list.itemRenderer
- BadgeOverviewWindow.GetChoiceListData
- BadgeOverviewWindow.ShowBadgeInfo
- attributeList.itemRenderer
- effectList.itemRenderer
- BadgeOverviewWindow.ShowBadgeAttribute
- attributeList.itemRenderer
- BadgeOverviewWindow.ShowBadgeSuit
- suitList.itemRenderer
- BadgeOverviewWindow.ShowCardWarnMask
- BadgeOverviewWindow.CheckHave
- BadgeOverviewWindow.InitBtn
- BadgeOverviewWindow.AutoWear
- BadgeOverviewWindow.UpdateAutoWearState
- BadgeOverviewWindow.InitHomePartData
- BadgeOverviewWindow.FindMaxLvPart
- BadgeOverviewWindow.GetSuitPart
- BadgeOverviewWindow.GetSuitPartByWear
- BadgeOverviewWindow.OnClose
- BadgeOverviewWindow.HandleMessage
**Requires:**
- BadgeOverview_BadgeOverviewWindowByName
**Snippet:**
```lua
require("BadgeOverview_BadgeOverviewWindowByName")
local BadgeOverviewWindow = {}
local uis, contentPane, cardId, choiceData, cardListData, maskTexture, homePartData, animTime

function BadgeOverviewWindow.ReInitData()
end

function BadgeOverviewWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BadgeOverviewWindow.package, WinResConfig.BadgeOverviewWindow.comName, function(com)
    contentPane = com
```

---

## Badge/BadgeOverview_AllWearBtnByName.lua.lua
**Functions:**
- GetBadgeOverview_AllWearBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetBadgeOverview_AllWearBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_Attribute1ByName.lua.lua
**Functions:**
- GetBadgeOverview_Attribute1Uis
**Requires:**
- BadgeOverview_Attribute2ByName
**Snippet:**
```lua
require("BadgeOverview_Attribute2ByName")

function GetBadgeOverview_Attribute1Uis(ui)
  local uis = {}
  uis.Attribute2 = GetBadgeOverview_Attribute2Uis(ui:GetChild("Attribute2"))
  uis.AttributeList = ui:GetChild("AttributeList")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_Attribute2ByName.lua.lua
**Functions:**
- GetBadgeOverview_Attribute2Uis
**Snippet:**
```lua
function GetBadgeOverview_Attribute2Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_Attribute3ByName.lua.lua
**Functions:**
- GetBadgeOverview_Attribute3Uis
**Requires:**
- BadgeOverview_LevelUpNumberByName
**Snippet:**
```lua
require("BadgeOverview_LevelUpNumberByName")

function GetBadgeOverview_Attribute3Uis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.LevelUpNumber = GetBadgeOverview_LevelUpNumberUis(ui:GetChild("LevelUpNumber"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
```

---

## Badge/BadgeOverview_AttributeByName.lua.lua
**Functions:**
- GetBadgeOverview_AttributeUis
**Requires:**
- BadgeOverview_Attribute1ByName
**Snippet:**
```lua
require("BadgeOverview_Attribute1ByName")

function GetBadgeOverview_AttributeUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.Attribute1 = GetBadgeOverview_Attribute1Uis(ui:GetChild("Attribute1"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TypeTxt = ui:GetChild("TypeTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Badge/BadgeOverview_AttributeRegionByName.lua.lua
**Functions:**
- GetBadgeOverview_AttributeRegionUis
**Snippet:**
```lua
function GetBadgeOverview_AttributeRegionUis(ui)
  local uis = {}
  
  uis.BadgeList = ui:GetChild("BadgeList")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_BadgeOverviewByName.lua.lua
**Functions:**
- GetBadgeOverview_BadgeOverviewUis
**Requires:**
- CommonResource_BackGroundByName
- BadgeOverview_LeftTabRegionByName
- BadgeOverview_TopTabRegionByName
- BadgeOverview_AttributeRegionByName
- BadgeOverview_EffectRegionByName
- BadgeOverview_CardEmptyByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("BadgeOverview_LeftTabRegionByName")
require("BadgeOverview_TopTabRegionByName")
require("BadgeOverview_AttributeRegionByName")
require("BadgeOverview_EffectRegionByName")
require("BadgeOverview_CardEmptyByName")

function GetBadgeOverview_BadgeOverviewUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
```

---

## Badge/BadgeOverview_BadgeOverviewWindowByName.lua.lua
**Functions:**
- GetBadgeOverview_BadgeOverviewWindowUis
**Requires:**
- BadgeOverview_BadgeOverviewByName
**Snippet:**
```lua
require("BadgeOverview_BadgeOverviewByName")

function GetBadgeOverview_BadgeOverviewWindowUis(ui)
  local uis = {}
  uis.Main = GetBadgeOverview_BadgeOverviewUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_BgAniByName.lua.lua
**Functions:**
- GetBadgeOverview_BgAniUis
**Snippet:**
```lua
function GetBadgeOverview_BgAniUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_CardBreachByName.lua.lua
**Functions:**
- GetBadgeOverview_CardBreachUis
**Snippet:**
```lua
function GetBadgeOverview_CardBreachUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_CardEmptyByName.lua.lua
**Functions:**
- GetBadgeOverview_CardEmptyUis
**Snippet:**
```lua
function GetBadgeOverview_CardEmptyUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_CardMark1ByName.lua.lua
**Functions:**
- GetBadgeOverview_CardMark1Uis
**Snippet:**
```lua
function GetBadgeOverview_CardMark1Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_CardMark2ByName.lua.lua
**Functions:**
- GetBadgeOverview_CardMark2Uis
**Snippet:**
```lua
function GetBadgeOverview_CardMark2Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_CardMark3ByName.lua.lua
**Functions:**
- GetBadgeOverview_CardMark3Uis
**Snippet:**
```lua
function GetBadgeOverview_CardMark3Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_CardOccupationByName.lua.lua
**Functions:**
- GetBadgeOverview_CardOccupationUis
**Snippet:**
```lua
function GetBadgeOverview_CardOccupationUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_Effect1ByName.lua.lua
**Functions:**
- GetBadgeOverview_Effect1Uis
**Snippet:**
```lua
function GetBadgeOverview_Effect1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_EffectByName.lua.lua
**Functions:**
- GetBadgeOverview_EffectUis
**Requires:**
- BadgeOverview_WearStateByName
**Snippet:**
```lua
require("BadgeOverview_WearStateByName")

function GetBadgeOverview_EffectUis(ui)
  local uis = {}
  uis.WearState = GetBadgeOverview_WearStateUis(ui:GetChild("WearState"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.EffectList = ui:GetChild("EffectList")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_EffectRegionByName.lua.lua
**Functions:**
- GetBadgeOverview_EffectRegionUis
**Snippet:**
```lua
function GetBadgeOverview_EffectRegionUis(ui)
  local uis = {}
  
  uis.BadgeList = ui:GetChild("BadgeList")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_GoWearBtnByName.lua.lua
**Functions:**
- GetBadgeOverview_GoWearBtnUis
**Snippet:**
```lua
function GetBadgeOverview_GoWearBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_HeadFrameBgByName.lua.lua
**Functions:**
- GetBadgeOverview_HeadFrameBgUis
**Snippet:**
```lua
function GetBadgeOverview_HeadFrameBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_HeadFrameBtnByName.lua.lua
**Functions:**
- GetBadgeOverview_HeadFrameBtnUis
**Requires:**
- BadgeOverview_HeadFrameByName
**Snippet:**
```lua
require("BadgeOverview_HeadFrameByName")

function GetBadgeOverview_HeadFrameBtnUis(ui)
  local uis = {}
  uis.HeadFrame = GetBadgeOverview_HeadFrameUis(ui:GetChild("HeadFrame"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_HeadFrameByName.lua.lua
**Functions:**
- GetBadgeOverview_HeadFrameUis
**Requires:**
- BadgeOverview_CardOccupationByName
- BadgeOverview_HeadFrameBgByName
- BadgeOverview_CardBreachByName
- BadgeOverview_CardMark1ByName
- BadgeOverview_CardMark2ByName
- BadgeOverview_CardMark3ByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("BadgeOverview_CardOccupationByName")
require("BadgeOverview_HeadFrameBgByName")
require("BadgeOverview_CardBreachByName")
require("BadgeOverview_CardMark1ByName")
require("BadgeOverview_CardMark2ByName")
require("BadgeOverview_CardMark3ByName")
require("CommonResource_RedDotByName")

function GetBadgeOverview_HeadFrameUis(ui)
  local uis = {}
```

---

## Badge/BadgeOverview_LeftTabRegionByName.lua.lua
**Functions:**
- GetBadgeOverview_LeftTabRegionUis
**Snippet:**
```lua
function GetBadgeOverview_LeftTabRegionUis(ui)
  local uis = {}
  
  uis.OccupationList = ui:GetChild("OccupationList")
  uis.TeamList = ui:GetChild("TeamList")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_LevelUpNumberByName.lua.lua
**Functions:**
- GetBadgeOverview_LevelUpNumberUis
**Snippet:**
```lua
function GetBadgeOverview_LevelUpNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_Mark1ByName.lua.lua
**Functions:**
- GetBadgeOverview_Mark1Uis
**Snippet:**
```lua
function GetBadgeOverview_Mark1Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_Mark2ByName.lua.lua
**Functions:**
- GetBadgeOverview_Mark2Uis
**Snippet:**
```lua
function GetBadgeOverview_Mark2Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_Mark3ByName.lua.lua
**Functions:**
- GetBadgeOverview_Mark3Uis
**Snippet:**
```lua
function GetBadgeOverview_Mark3Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_OccupationBtnByName.lua.lua
**Functions:**
- GetBadgeOverview_OccupationBtnUis
**Requires:**
- BadgeOverview_BgAniByName
**Snippet:**
```lua
require("BadgeOverview_BgAniByName")

function GetBadgeOverview_OccupationBtnUis(ui)
  local uis = {}
  uis.BgAni = GetBadgeOverview_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Badge/BadgeOverview_RecommendWearBtnByName.lua.lua
**Functions:**
- GetBadgeOverview_RecommendWearBtnUis
**Snippet:**
```lua
function GetBadgeOverview_RecommendWearBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_StateBtnByName.lua.lua
**Functions:**
- GetBadgeOverview_StateBtnUis
**Snippet:**
```lua
function GetBadgeOverview_StateBtnUis(ui)
  local uis = {}
  
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_TeamBtnByName.lua.lua
**Functions:**
- GetBadgeOverview_TeamBtnUis
**Requires:**
- BadgeOverview_BgAniByName
**Snippet:**
```lua
require("BadgeOverview_BgAniByName")

function GetBadgeOverview_TeamBtnUis(ui)
  local uis = {}
  uis.BgAni = GetBadgeOverview_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_TopTabBtnBgByName.lua.lua
**Functions:**
- GetBadgeOverview_TopTabBtnBgUis
**Snippet:**
```lua
function GetBadgeOverview_TopTabBtnBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_TopTabBtnByName.lua.lua
**Functions:**
- GetBadgeOverview_TopTabBtnUis
**Requires:**
- BadgeOverview_TopTabBtnBgByName
**Snippet:**
```lua
require("BadgeOverview_TopTabBtnBgByName")

function GetBadgeOverview_TopTabBtnUis(ui)
  local uis = {}
  uis.MaterialTabBtnBg = GetBadgeOverview_TopTabBtnBgUis(ui:GetChild("MaterialTabBtnBg"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_TopTabRegionByName.lua.lua
**Functions:**
- GetBadgeOverview_TopTabRegionUis
**Snippet:**
```lua
function GetBadgeOverview_TopTabRegionUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeOverview_WearStateByName.lua.lua
**Functions:**
- GetBadgeOverview_WearStateUis
**Requires:**
- BadgeOverview_Mark1ByName
- BadgeOverview_Mark2ByName
- BadgeOverview_Mark3ByName
**Snippet:**
```lua
require("BadgeOverview_Mark1ByName")
require("BadgeOverview_Mark2ByName")
require("BadgeOverview_Mark3ByName")

function GetBadgeOverview_WearStateUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.Mark1 = GetBadgeOverview_Mark1Uis(ui:GetChild("Mark1"))
  uis.Mark2 = GetBadgeOverview_Mark2Uis(ui:GetChild("Mark2"))
  uis.Mark3 = GetBadgeOverview_Mark3Uis(ui:GetChild("Mark3"))
```

---

## Badge/BadgePrimaryAttributeWindow.lua.lua
**Functions:**
- BadgePrimaryAttributeWindow.ReInitData
- BadgePrimaryAttributeWindow.OnInit
- BadgePrimaryAttributeWindow.UpdateInfo
- tips.ContentList.itemRenderer
- BadgePrimaryAttributeWindow.GetSelecteId
- BadgePrimaryAttributeWindow.InitBtn
- BadgePrimaryAttributeWindow.CloseWindow
- BadgePrimaryAttributeWindow.OnClose
**Requires:**
- Badge_PrimaryAttributeWindowByName
**Snippet:**
```lua
require("Badge_PrimaryAttributeWindowByName")
local BadgePrimaryAttributeWindow = {}
local uis, contentPane, selecteId

function BadgePrimaryAttributeWindow.ReInitData()
end

function BadgePrimaryAttributeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BadgePrimaryAttributeWindow.package, WinResConfig.BadgePrimaryAttributeWindow.comName, function(com)
    contentPane = com
```

---

## Badge/BadgeRecommendWindow.lua.lua
**Functions:**
- BadgeRecommendWindow.ReInitData
- BadgeRecommendWindow.OnInit
- BadgeRecommendWindow.UpdateInfo
- tips.BadgeShow.ShowList.itemRenderer
- wordList.itemRenderer
- pageList.itemRenderer
- tips.AttributeShow.Attribute1.TypeList.itemRenderer
- wordList.itemRenderer
- tips.AttributeShow.Attribute2.TypeList.itemRenderer
- BadgeRecommendWindow.SetPageShow
- BadgeRecommendWindow.GetBadgeCountByPart
- BadgeRecommendWindow.CloseWindow
- BadgeRecommendWindow.InitBtn
- BadgeRecommendWindow.OnClose
**Requires:**
- BadgeRecommend_RecommendWindowByName
**Snippet:**
```lua
require("BadgeRecommend_RecommendWindowByName")
local BadgeRecommendWindow = {}
local uis, contentPane, cardId

function BadgeRecommendWindow.ReInitData()
end

function BadgeRecommendWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BadgeRecommendWindow.package, WinResConfig.BadgeRecommendWindow.comName, function(com)
    contentPane = com
```

---

## Badge/BadgeRecommend_AllWearBtnByName.lua.lua
**Functions:**
- GetBadgeRecommend_AllWearBtnUis
**Snippet:**
```lua
function GetBadgeRecommend_AllWearBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeRecommend_Attribute1ByName.lua.lua
**Functions:**
- GetBadgeRecommend_Attribute1Uis
**Snippet:**
```lua
function GetBadgeRecommend_Attribute1Uis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.TypeList = ui:GetChild("TypeList")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeRecommend_Attribute1TypeByName.lua.lua
**Functions:**
- GetBadgeRecommend_Attribute1TypeUis
**Snippet:**
```lua
function GetBadgeRecommend_Attribute1TypeUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeRecommend_Attribute1TypeWordByName.lua.lua
**Functions:**
- GetBadgeRecommend_Attribute1TypeWordUis
**Snippet:**
```lua
function GetBadgeRecommend_Attribute1TypeWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeRecommend_Attribute2ByName.lua.lua
**Functions:**
- GetBadgeRecommend_Attribute2Uis
**Snippet:**
```lua
function GetBadgeRecommend_Attribute2Uis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.TypeList = ui:GetChild("TypeList")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeRecommend_Attribute2TypeWordByName.lua.lua
**Functions:**
- GetBadgeRecommend_Attribute2TypeWordUis
**Snippet:**
```lua
function GetBadgeRecommend_Attribute2TypeWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeRecommend_AttributeShowByName.lua.lua
**Functions:**
- GetBadgeRecommend_AttributeShowUis
**Requires:**
- BadgeRecommend_Attribute1ByName
- BadgeRecommend_Attribute2ByName
**Snippet:**
```lua
require("BadgeRecommend_Attribute1ByName")
require("BadgeRecommend_Attribute2ByName")

function GetBadgeRecommend_AttributeShowUis(ui)
  local uis = {}
  uis.Attribute1 = GetBadgeRecommend_Attribute1Uis(ui:GetChild("Attribute1"))
  uis.Attribute2 = GetBadgeRecommend_Attribute2Uis(ui:GetChild("Attribute2"))
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeRecommend_BadgeShowByName.lua.lua
**Functions:**
- GetBadgeRecommend_BadgeShowUis
**Requires:**
- BadgeRecommend_BadgeShowIcon1ByName
- BadgeRecommend_BadgeShowIcon2ByName
**Snippet:**
```lua
require("BadgeRecommend_BadgeShowIcon1ByName")
require("BadgeRecommend_BadgeShowIcon2ByName")

function GetBadgeRecommend_BadgeShowUis(ui)
  local uis = {}
  uis.BadgeIcon = GetBadgeRecommend_BadgeShowIcon1Uis(ui:GetChild("BadgeIcon"))
  uis.BadgeIcon1 = GetBadgeRecommend_BadgeShowIcon2Uis(ui:GetChild("BadgeIcon1"))
  uis.BadgeIcon2 = GetBadgeRecommend_BadgeShowIcon2Uis(ui:GetChild("BadgeIcon2"))
  uis.BadgeIcon3 = GetBadgeRecommend_BadgeShowIcon2Uis(ui:GetChild("BadgeIcon3"))
  uis.AllWearBtn = ui:GetChild("AllWearBtn")
```

---

## Badge/BadgeRecommend_BadgeShowIcon1ByName.lua.lua
**Functions:**
- GetBadgeRecommend_BadgeShowIcon1Uis
**Snippet:**
```lua
function GetBadgeRecommend_BadgeShowIcon1Uis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeRecommend_BadgeShowIcon2ByName.lua.lua
**Functions:**
- GetBadgeRecommend_BadgeShowIcon2Uis
**Snippet:**
```lua
function GetBadgeRecommend_BadgeShowIcon2Uis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeRecommend_BadgeShowListByName.lua.lua
**Functions:**
- GetBadgeRecommend_BadgeShowListUis
**Snippet:**
```lua
function GetBadgeRecommend_BadgeShowListUis(ui)
  local uis = {}
  
  uis.ShowList = ui:GetChild("ShowList")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeRecommend_BadgeShowWordByName.lua.lua
**Functions:**
- GetBadgeRecommend_BadgeShowWordUis
**Snippet:**
```lua
function GetBadgeRecommend_BadgeShowWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeRecommend_Mark1ByName.lua.lua
**Functions:**
- GetBadgeRecommend_Mark1Uis
**Snippet:**
```lua
function GetBadgeRecommend_Mark1Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeRecommend_Mark2ByName.lua.lua
**Functions:**
- GetBadgeRecommend_Mark2Uis
**Snippet:**
```lua
function GetBadgeRecommend_Mark2Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeRecommend_Mark3ByName.lua.lua
**Functions:**
- GetBadgeRecommend_Mark3Uis
**Snippet:**
```lua
function GetBadgeRecommend_Mark3Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeRecommend_PageByName.lua.lua
**Functions:**
- GetBadgeRecommend_PageUis
**Snippet:**
```lua
function GetBadgeRecommend_PageUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeRecommend_RecommendByName.lua.lua
**Functions:**
- GetBadgeRecommend_RecommendUis
**Requires:**
- CommonResource_PopupBgByName
- BadgeRecommend_RecommendTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("BadgeRecommend_RecommendTipsByName")

function GetBadgeRecommend_RecommendUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.RecommendTips = GetBadgeRecommend_RecommendTipsUis(ui:GetChild("RecommendTips"))
  uis.root = ui
```

---

## Badge/BadgeRecommend_RecommendTipsByName.lua.lua
**Functions:**
- GetBadgeRecommend_RecommendTipsUis
**Requires:**
- BadgeRecommend_TitleByName
- BadgeRecommend_BadgeShowListByName
- BadgeRecommend_AttributeShowByName
**Snippet:**
```lua
require("BadgeRecommend_TitleByName")
require("BadgeRecommend_BadgeShowListByName")
require("BadgeRecommend_AttributeShowByName")

function GetBadgeRecommend_RecommendTipsUis(ui)
  local uis = {}
  uis.Title = GetBadgeRecommend_TitleUis(ui:GetChild("Title"))
  uis.BadgeShow = GetBadgeRecommend_BadgeShowListUis(ui:GetChild("BadgeShow"))
  uis.AttributeShow = GetBadgeRecommend_AttributeShowUis(ui:GetChild("AttributeShow"))
  uis.PageNumberList = ui:GetChild("PageNumberList")
```

---

## Badge/BadgeRecommend_RecommendWindowByName.lua.lua
**Functions:**
- GetBadgeRecommend_RecommendWindowUis
**Requires:**
- BadgeRecommend_RecommendByName
**Snippet:**
```lua
require("BadgeRecommend_RecommendByName")

function GetBadgeRecommend_RecommendWindowUis(ui)
  local uis = {}
  uis.Main = GetBadgeRecommend_RecommendUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeRecommend_TitleByName.lua.lua
**Functions:**
- GetBadgeRecommend_TitleUis
**Requires:**
- BadgeRecommend_WearStateByName
**Snippet:**
```lua
require("BadgeRecommend_WearStateByName")

function GetBadgeRecommend_TitleUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.StarList = ui:GetChild("StarList")
  uis.WearState = GetBadgeRecommend_WearStateUis(ui:GetChild("WearState"))
  uis.root = ui
  return uis
end
```

---

## Badge/BadgeRecommend_WearStateByName.lua.lua
**Functions:**
- GetBadgeRecommend_WearStateUis
**Requires:**
- BadgeRecommend_Mark1ByName
- BadgeRecommend_Mark2ByName
- BadgeRecommend_Mark3ByName
**Snippet:**
```lua
require("BadgeRecommend_Mark1ByName")
require("BadgeRecommend_Mark2ByName")
require("BadgeRecommend_Mark3ByName")

function GetBadgeRecommend_WearStateUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.Mark1 = GetBadgeRecommend_Mark1Uis(ui:GetChild("Mark1"))
  uis.Mark2 = GetBadgeRecommend_Mark2Uis(ui:GetChild("Mark2"))
  uis.Mark3 = GetBadgeRecommend_Mark3Uis(ui:GetChild("Mark3"))
```

---

## Badge/BadgeScreenWindow.lua.lua
**Functions:**
- BadgeScreenWindow.ReInitData
- BadgeScreenWindow.OnInit
- BadgeScreenWindow.UpdateInfo
- BadgeScreenWindow.UpdateSuitList
- suitList.itemRenderer
- BadgeScreenWindow.UpdateStarList
- starList.itemRenderer
- BadgeScreenWindow.UpdateMainAttributeList
- mainAttributeList.itemRenderer
- BadgeScreenWindow.UpdateViceAttributeList
- viceAttributeList.itemRenderer
- BadgeScreenWindow.UpdateResult
- BadgeScreenWindow.InitBtn
- BadgeScreenWindow.CloseWindow
- BadgeScreenWindow.HandleMessage
- BadgeScreenWindow.OnClose
**Requires:**
- Badge_BadgeScreenWindowByName
**Snippet:**
```lua
require("Badge_BadgeScreenWindowByName")
local BadgeScreenWindow = {}
local uis, contentPane, screen, suitList, starList, mainAttributeList, viceAttributeList

function BadgeScreenWindow.ReInitData()
end

function BadgeScreenWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BadgeScreenWindow.package, WinResConfig.BadgeScreenWindow.comName, function(com)
    contentPane = com
```

---

## Badge/BadgeScriptList.lua.lua
**Requires:**
- BadgeData
- BadgeService
- BadgeMgr
**Snippet:**
```lua
local require = require
require("BadgeData")
require("BadgeService")
require("BadgeMgr")
```

---

## Badge/BadgeSecondaryAttributeWindow.lua.lua
**Functions:**
- BadgeSecondaryAttributeWindow.ReInitData
- BadgeSecondaryAttributeWindow.OnInit
- BadgeSecondaryAttributeWindow.UpdateInfo
- tips.ContentList.itemRenderer
- BadgeSecondaryAttributeWindow.GetSelecteId
- BadgeSecondaryAttributeWindow.CloseWindow
- BadgeSecondaryAttributeWindow.InitBtn
- BadgeSecondaryAttributeWindow.OnClose
**Requires:**
- Badge_SecondaryAttributeWindowByName
**Snippet:**
```lua
require("Badge_SecondaryAttributeWindowByName")
local BadgeSecondaryAttributeWindow = {}
local uis, contentPane, selecteId

function BadgeSecondaryAttributeWindow.ReInitData()
end

function BadgeSecondaryAttributeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BadgeSecondaryAttributeWindow.package, WinResConfig.BadgeSecondaryAttributeWindow.comName, function(com)
    contentPane = com
```

---

## Badge/BadgeService.lua.lua
**Functions:**
- BadgeService.Init
- BadgeService.DecomposeBadgeReq
- BadgeService.DecomposeBadgeRsp
- BadgeService.SetBadgeLockStateReq
- BadgeService.SetBadgeLockStateRsp
- BadgeService.TakeoffBadgeReq
- BadgeService.TakeoffBadgeRsp
- BadgeService.WearBadgeReq
- BadgeService.WearBadgeRsp
- BadgeService.LevelupBadgeReq
- BadgeService.LevelupBadgeRsp
- BadgeService.ClearBadgeNewTagReq
- BadgeService.ClearBadgeNewTagRsp
- BadgeService.SwitchBadgeReq
- BadgeService.SwitchBadgeRsp
**Snippet:**
```lua
BadgeService = {}

function BadgeService.Init()
  Net.AddListener(Proto.MsgName.TakeoffBadgeRsp, BadgeService.TakeoffBadgeRsp)
  Net.AddListener(Proto.MsgName.LevelupBadgeRsp, BadgeService.LevelupBadgeRsp)
  Net.AddListener(Proto.MsgName.WearBadgeRsp, BadgeService.WearBadgeRsp)
  Net.AddListener(Proto.MsgName.DecomposeBadgeRsp, BadgeService.DecomposeBadgeRsp)
  Net.AddListener(Proto.MsgName.SetBadgeLockStateRsp, BadgeService.SetBadgeLockStateRsp)
  Net.AddListener(Proto.MsgName.ClearBadgeNewTagRsp, BadgeService.ClearBadgeNewTagRsp)
  Net.AddListener(Proto.MsgName.SwitchBadgeRsp, BadgeService.SwitchBadgeRsp)
```

---

## Badge/BadgeSuitScreenWindow.lua.lua
**Functions:**
- BadgeSuitScreenWindow.ReInitData
- BadgeSuitScreenWindow.OnInit
- BadgeSuitScreenWindow.GetAllSuits
- BadgeSuitScreenWindow.UpdateInfo
- tips.ContentList.itemRenderer
- BadgeSuitScreenWindow.GetSelecteId
- BadgeSuitScreenWindow.CloseWindow
- BadgeSuitScreenWindow.InitBtn
- BadgeSuitScreenWindow.OnClose
**Requires:**
- Badge_SuitScreenWindowByName
**Snippet:**
```lua
require("Badge_SuitScreenWindowByName")
local BadgeSuitScreenWindow = {}
local uis, contentPane, selecteId

function BadgeSuitScreenWindow.ReInitData()
end

function BadgeSuitScreenWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BadgeSuitScreenWindow.package, WinResConfig.BadgeSuitScreenWindow.comName, function(com)
    contentPane = com
```

---

## Badge/BadgeUnknownTipsWindow.lua.lua
**Functions:**
- BadgeUnknownTipsWindow.ReInitData
- BadgeUnknownTipsWindow.OnInit
- BadgeUnknownTipsWindow.UpdateInfo
- suitList.itemRenderer
- BadgeUnknownTipsWindow.GetGoToData
- BadgeUnknownTipsWindow.StageIsUnlock
- BadgeUnknownTipsWindow.ShowAllGoTo
- uis.Main.Way.GetStripList.itemRenderer
- BadgeUnknownTipsWindow.ShowGoTo
- uis.Main.Way.GetStripList.itemRenderer
- BadgeUnknownTipsWindow.CloseWindow
- BadgeUnknownTipsWindow.InitBtn
- BadgeUnknownTipsWindow.OnClose
**Requires:**
- Message_BadgeUnknownTipsWindowByName
**Snippet:**
```lua
require("Message_BadgeUnknownTipsWindowByName")
local BadgeUnknownTipsWindow = {}
local uis, contentPane, badgeData, wayData, jumpData

function BadgeUnknownTipsWindow.ReInitData()
end

function BadgeUnknownTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BadgeUnknownTipsWindow.package, WinResConfig.BadgeUnknownTipsWindow.comName, function(com)
    contentPane = com
```

---

## Badge/BadgeWindow.lua.lua
**Functions:**
- BadgeWindow.ReInitData
- BadgeWindow.OnInit
- BadgeWindow.InitRedDot
- BadgeWindow.InitFixedData
- BadgeWindow.UpdateInfo
- BadgeWindow.LoadPartEffect
- BadgeWindow.SetSpineEffectAnimation
- BadgeWindow.GetPartBtn
- BadgeWindow.IintCard
- list.itemRenderer
- BadgeWindow.ShowCardWarnMask
- BadgeWindow.CheckHave
- BadgeWindow.InitHomePartData
- BadgeWindow.CardItemClick
- BadgeWindow.InitPartInfo
- BadgeWindow.WearBadge
- BadgeWindow.TakeoffBadge
- BadgeWindow.ReverseData
- BadgeWindow.ShowSortBtnName
- BadgeWindow.ChangePage
- BadgeWindow.GetClearNew
- BadgeWindow.ShowDetailsInfo
- BadgeWindow.PartListItem
- BadgeWindow.PlayChangeEffect
- BadgeWindow.PlayWearEffect
- BadgeWindow.UpdateCurPart
- BadgeWindow.ShowAttribute
- attList.itemRenderer
- BadgeWindow.StopAnim
- BadgeWindow.GetWearBadgeIdByType
- BadgeWindow.InitLvUp
- BadgeWindow.OpenLevelTips
- BadgeWindow.ShowLvUpItem
- tips.BadgeList.itemRenderer
- BadgeWindow.UpdateCostGold
- BadgeWindow.ShowAddLvUpTips
- wordList.itemRenderer
- BadgeWindow.PlayAddItemExpAnim
- BadgeWindow.SetTempLv
- BadgeWindow.ShowExpBarAnim
- BadgeWindow.GetTatalMaxExp
- BadgeWindow.GetLevelUpItem
- BadgeWindow.LevelUpUpdate
- BadgeWindow.GetGesture
- BadgeWindow.StopTween
- BadgeWindow.UpdateItemList
- BadgeWindow.SetTouchable
- BadgeWindow.Back
- BadgeWindow.InitCurrencyReturn
- BadgeWindow.InitBtn
- BadgeWindow.UpdateAutoWearState
- BadgeWindow.GetSuitPart
- BadgeWindow.GetSuitPartByWear
- BadgeWindow.AutoWear
- BadgeWindow.HandleMessage
- BadgeWindow.OnShown
- BadgeWindow.OnClose
**Requires:**
- Badge_BadgeWindowByName
- Badge_PartsByName
**Snippet:**
```lua
require("Badge_BadgeWindowByName")
require("Badge_PartsByName")
local BadgeWindow = {}
local uis, contentPane, jumpTb, curTypePartData, selectBadgeData, isPlayAnim, timeIndex, playAnim, homePartData, showFirstUid, wearBadgeList, cardId, lvUpItem, spendItemData, costLvMoney, longSpeed, tempLv, tempExp, maxLv, upDataId, curMaxLvExp, tatalMaxExp, tweener, lvTween, addAttr, upAttr, totalMoney, mainAddRoot, lvUpItemCost, costMoneyTxt, costGoldRoot, costMoney, curBadgeInfo, upInfoTips, animTime, reverseSort, tempSortUid, badgeEffEct, partBtn, partInfoRoot, maskTexture, lastEffUid, changeEffect
local starColor = {
  [1] = {
    r = 73,
    g = 191,
    b = 96,
    a = 0,
```

---

## Badge/Badge_AllChoiceBtnByName.lua.lua
**Functions:**
- GetBadge_AllChoiceBtnUis
**Snippet:**
```lua
function GetBadge_AllChoiceBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_AllWearBtnByName.lua.lua
**Functions:**
- GetBadge_AllWearBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetBadge_AllWearBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_BadgeByName.lua.lua
**Functions:**
- GetBadge_BadgeUis
**Requires:**
- CommonResource_BackGroundByName
- Badge_CardShowByName
- Badge_EmptyEffectByName
- Badge_HomePageByName
- Badge_BadgeDetailsLevelUpByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Badge_CardShowByName")
require("Badge_EmptyEffectByName")
require("Badge_HomePageByName")
require("Badge_BadgeDetailsLevelUpByName")
require("CommonResource_CurrencyReturnByName")

function GetBadge_BadgeUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
```

---

## Badge/Badge_BadgeDecomposeAniByName.lua.lua
**Functions:**
- GetBadge_BadgeDecomposeAniUis
**Snippet:**
```lua
function GetBadge_BadgeDecomposeAniUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_BadgeDecomposeBtnByName.lua.lua
**Functions:**
- GetBadge_BadgeDecomposeBtnUis
**Requires:**
- Badge_HeadShow1ByName
- Badge_IconLockByName
**Snippet:**
```lua
require("Badge_HeadShow1ByName")
require("Badge_IconLockByName")

function GetBadge_BadgeDecomposeBtnUis(ui)
  local uis = {}
  uis.IconLoader = ui:GetChild("IconLoader")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.StarList = ui:GetChild("StarList")
  uis.HeadShow = GetBadge_HeadShow1Uis(ui:GetChild("HeadShow"))
  uis.IconLock = GetBadge_IconLockUis(ui:GetChild("IconLock"))
```

---

## Badge/Badge_BadgeDecomposeByName.lua.lua
**Functions:**
- GetBadge_BadgeDecomposeUis
**Requires:**
- CommonResource_BackGroundByName
- Badge_DecomposeInfoByName
- Badge_DecomposeListByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Badge_DecomposeInfoByName")
require("Badge_DecomposeListByName")
require("CommonResource_CurrencyReturnByName")

function GetBadge_BadgeDecomposeUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.DecomposeInfo = GetBadge_DecomposeInfoUis(ui:GetChild("DecomposeInfo"))
  uis.DecomposeList = GetBadge_DecomposeListUis(ui:GetChild("DecomposeList"))
```

---

## Badge/Badge_BadgeDecomposeWindowByName.lua.lua
**Functions:**
- GetBadge_BadgeDecomposeWindowUis
**Requires:**
- Badge_BadgeDecomposeByName
**Snippet:**
```lua
require("Badge_BadgeDecomposeByName")

function GetBadge_BadgeDecomposeWindowUis(ui)
  local uis = {}
  uis.Main = GetBadge_BadgeDecomposeUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_BadgeDetailsByName.lua.lua
**Functions:**
- GetBadge_BadgeDetailsUis
**Requires:**
- Badge_ContrastTipsByName
- Badge_DetailsInfoByName
- Badge_WearBadgeContainerByName
**Snippet:**
```lua
require("Badge_ContrastTipsByName")
require("Badge_DetailsInfoByName")
require("Badge_WearBadgeContainerByName")

function GetBadge_BadgeDetailsUis(ui)
  local uis = {}
  uis.ContrastTips = GetBadge_ContrastTipsUis(ui:GetChild("ContrastTips"))
  uis.DetailsInfo = GetBadge_DetailsInfoUis(ui:GetChild("DetailsInfo"))
  uis.WearBadgeContainer = GetBadge_WearBadgeContainerUis(ui:GetChild("WearBadgeContainer"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## Badge/Badge_BadgeDetailsLevelUpByName.lua.lua
**Functions:**
- GetBadge_BadgeDetailsLevelUpUis
**Requires:**
- Badge_PartsInfoByName
- Badge_BadgeDetailsByName
- Badge_BadgeLevelUpByName
**Snippet:**
```lua
require("Badge_PartsInfoByName")
require("Badge_BadgeDetailsByName")
require("Badge_BadgeLevelUpByName")

function GetBadge_BadgeDetailsLevelUpUis(ui)
  local uis = {}
  uis.PartsInfo = GetBadge_PartsInfoUis(ui:GetChild("PartsInfo"))
  uis.BadgeDetails = GetBadge_BadgeDetailsUis(ui:GetChild("BadgeDetails"))
  uis.BadgeLevelUp = GetBadge_BadgeLevelUpUis(ui:GetChild("BadgeLevelUp"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## Badge/Badge_BadgeLevelUpByName.lua.lua
**Functions:**
- GetBadge_BadgeLevelUpUis
**Requires:**
- Badge_LevelUpInfoByName
- Badge_LevelUpListByName
**Snippet:**
```lua
require("Badge_LevelUpInfoByName")
require("Badge_LevelUpListByName")

function GetBadge_BadgeLevelUpUis(ui)
  local uis = {}
  uis.LevelUpInfo = GetBadge_LevelUpInfoUis(ui:GetChild("LevelUpInfo"))
  uis.LevelUpList = GetBadge_LevelUpListUis(ui:GetChild("LevelUpList"))
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_BadgeReplaceIconBtnByName.lua.lua
**Functions:**
- GetBadge_BadgeReplaceIconBtnUis
**Requires:**
- Badge_HeadShow1ByName
- Badge_IconLockByName
**Snippet:**
```lua
require("Badge_HeadShow1ByName")
require("Badge_IconLockByName")

function GetBadge_BadgeReplaceIconBtnUis(ui)
  local uis = {}
  uis.IconLoader = ui:GetChild("IconLoader")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.StarList = ui:GetChild("StarList")
  uis.HeadShow = GetBadge_HeadShow1Uis(ui:GetChild("HeadShow"))
  uis.IconLock = GetBadge_IconLockUis(ui:GetChild("IconLock"))
```

---

## Badge/Badge_BadgeScreen1ByName.lua.lua
**Functions:**
- GetBadge_BadgeScreen1Uis
**Snippet:**
```lua
function GetBadge_BadgeScreen1Uis(ui)
  local uis = {}
  
  uis.ScreenList = ui:GetChild("ScreenList")
  uis.ResettingBtn = ui:GetChild("ResettingBtn")
  uis.ScreenSureBtn = ui:GetChild("ScreenSureBtn")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_BadgeScreen2ByName.lua.lua
**Functions:**
- GetBadge_BadgeScreen2Uis
**Requires:**
- Badge_BadgeScreen1ByName
**Snippet:**
```lua
require("Badge_BadgeScreen1ByName")

function GetBadge_BadgeScreen2Uis(ui)
  local uis = {}
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.BadgeScreen1 = GetBadge_BadgeScreen1Uis(ui:GetChild("BadgeScreen1"))
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_BadgeScreenWindowByName.lua.lua
**Functions:**
- GetBadge_BadgeScreenWindowUis
**Requires:**
- Badge_BadgeScreen2ByName
**Snippet:**
```lua
require("Badge_BadgeScreen2ByName")

function GetBadge_BadgeScreenWindowUis(ui)
  local uis = {}
  uis.Main = GetBadge_BadgeScreen2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_BadgeWindowByName.lua.lua
**Functions:**
- GetBadge_BadgeWindowUis
**Requires:**
- Badge_BadgeByName
**Snippet:**
```lua
require("Badge_BadgeByName")

function GetBadge_BadgeWindowUis(ui)
  local uis = {}
  uis.Main = GetBadge_BadgeUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_CardBreachByName.lua.lua
**Functions:**
- GetBadge_CardBreachUis
**Snippet:**
```lua
function GetBadge_CardBreachUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_CardShowByName.lua.lua
**Functions:**
- GetBadge_CardShowUis
**Snippet:**
```lua
function GetBadge_CardShowUis(ui)
  local uis = {}
  
  uis.CardShowLoader = ui:GetChild("CardShowLoader")
  uis.CardShowHolder = ui:GetChild("CardShowHolder")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ChoiceBtnByName.lua.lua
**Functions:**
- GetBadge_ChoiceBtnUis
**Snippet:**
```lua
function GetBadge_ChoiceBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ChoiceSortBtnByName.lua.lua
**Functions:**
- GetBadge_ChoiceSortBtnUis
**Snippet:**
```lua
function GetBadge_ChoiceSortBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ChoiceSortByName.lua.lua
**Functions:**
- GetBadge_ChoiceSortUis
**Snippet:**
```lua
function GetBadge_ChoiceSortUis(ui)
  local uis = {}
  
  uis.ChoiceSortBtn = ui:GetChild("ChoiceSortBtn")
  uis.SortBtn = ui:GetChild("SortBtn")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ClearBtnByName.lua.lua
**Functions:**
- GetBadge_ClearBtnUis
**Snippet:**
```lua
function GetBadge_ClearBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ContrastBtnByName.lua.lua
**Functions:**
- GetBadge_ContrastBtnUis
**Snippet:**
```lua
function GetBadge_ContrastBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ContrastTipsByName.lua.lua
**Functions:**
- GetBadge_ContrastTipsUis
**Requires:**
- Badge_DetailsInfo1ByName
- Badge_DetailsInfo2ByName
- Badge_DetailsInfo3ByName
- Badge_ContrastUserByName
**Snippet:**
```lua
require("Badge_DetailsInfo1ByName")
require("Badge_DetailsInfo2ByName")
require("Badge_DetailsInfo3ByName")
require("Badge_ContrastUserByName")

function GetBadge_ContrastTipsUis(ui)
  local uis = {}
  uis.DetailsInfo1 = GetBadge_DetailsInfo1Uis(ui:GetChild("DetailsInfo1"))
  uis.DetailsInfo2 = GetBadge_DetailsInfo2Uis(ui:GetChild("DetailsInfo2"))
  uis.DetailsInfo3 = GetBadge_DetailsInfo3Uis(ui:GetChild("DetailsInfo3"))
```

---

## Badge/Badge_ContrastUserByName.lua.lua
**Functions:**
- GetBadge_ContrastUserUis
**Requires:**
- Badge_HeadShowByName
**Snippet:**
```lua
require("Badge_HeadShowByName")

function GetBadge_ContrastUserUis(ui)
  local uis = {}
  uis.HeadShow = GetBadge_HeadShowUis(ui:GetChild("HeadShow"))
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_Decompose1BtnByName.lua.lua
**Functions:**
- GetBadge_Decompose1BtnUis
**Snippet:**
```lua
function GetBadge_Decompose1BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_DecomposeBtnByName.lua.lua
**Functions:**
- GetBadge_DecomposeBtnUis
**Snippet:**
```lua
function GetBadge_DecomposeBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_DecomposeInfoByName.lua.lua
**Functions:**
- GetBadge_DecomposeInfoUis
**Requires:**
- Badge_DetailsInfo1ByName
- Badge_DetailsInfo2ByName
- Badge_DetailsInfo3ByName
**Snippet:**
```lua
require("Badge_DetailsInfo1ByName")
require("Badge_DetailsInfo2ByName")
require("Badge_DetailsInfo3ByName")

function GetBadge_DecomposeInfoUis(ui)
  local uis = {}
  uis.DetailsInfo1 = GetBadge_DetailsInfo1Uis(ui:GetChild("DetailsInfo1"))
  uis.DetailsInfo2 = GetBadge_DetailsInfo2Uis(ui:GetChild("DetailsInfo2"))
  uis.DetailsInfo3 = GetBadge_DetailsInfo3Uis(ui:GetChild("DetailsInfo3"))
  uis.WordTxt = ui:GetChild("WordTxt")
```

---

## Badge/Badge_DecomposeListByName.lua.lua
**Functions:**
- GetBadge_DecomposeListUis
**Requires:**
- Badge_DecomposeTabRegionByName
- Badge_ChoiceSortByName
- Badge_DecomposeResultByName
**Snippet:**
```lua
require("Badge_DecomposeTabRegionByName")
require("Badge_ChoiceSortByName")
require("Badge_DecomposeResultByName")

function GetBadge_DecomposeListUis(ui)
  local uis = {}
  uis.DecomposeTabRegion = GetBadge_DecomposeTabRegionUis(ui:GetChild("DecomposeTabRegion"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.ChoiceNumberTxt = ui:GetChild("ChoiceNumberTxt")
  uis.ChoiceBtn = ui:GetChild("ChoiceBtn")
```

---

## Badge/Badge_DecomposeResultByName.lua.lua
**Functions:**
- GetBadge_DecomposeResultUis
**Snippet:**
```lua
function GetBadge_DecomposeResultUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_DecomposeSrueBtnByName.lua.lua
**Functions:**
- GetBadge_DecomposeSrueBtnUis
**Snippet:**
```lua
function GetBadge_DecomposeSrueBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_DecomposeTabRegionByName.lua.lua
**Functions:**
- GetBadge_DecomposeTabRegionUis
**Snippet:**
```lua
function GetBadge_DecomposeTabRegionUis(ui)
  local uis = {}
  
  uis.Tab1Btn = ui:GetChild("Tab1Btn")
  uis.Tab2Btn = ui:GetChild("Tab2Btn")
  uis.Tab3Btn = ui:GetChild("Tab3Btn")
  uis.Tab4Btn = ui:GetChild("Tab4Btn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Badge/Badge_DetailsInfo1ByName.lua.lua
**Functions:**
- GetBadge_DetailsInfo1Uis
**Requires:**
- Badge_LockByName
**Snippet:**
```lua
require("Badge_LockByName")

function GetBadge_DetailsInfo1Uis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.PartsTxt = ui:GetChild("PartsTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.Lock = GetBadge_LockUis(ui:GetChild("Lock"))
  uis.root = ui
  return uis
```

---

## Badge/Badge_DetailsInfo2ByName.lua.lua
**Functions:**
- GetBadge_DetailsInfo2Uis
**Requires:**
- Badge_DetailsInfo2_1ByName
**Snippet:**
```lua
require("Badge_DetailsInfo2_1ByName")

function GetBadge_DetailsInfo2Uis(ui)
  local uis = {}
  uis.DetailsInfo2_1 = GetBadge_DetailsInfo2_1Uis(ui:GetChild("DetailsInfo2_1"))
  uis.WordList = ui:GetChild("WordList")
  uis.AttributeList = ui:GetChild("AttributeList")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_DetailsInfo2_1ByName.lua.lua
**Functions:**
- GetBadge_DetailsInfo2_1Uis
**Snippet:**
```lua
function GetBadge_DetailsInfo2_1Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Badge/Badge_DetailsInfo2_2ByName.lua.lua
**Functions:**
- GetBadge_DetailsInfo2_2Uis
**Requires:**
- Badge_NewByName
- Badge_LevelUpNumberByName
**Snippet:**
```lua
require("Badge_NewByName")
require("Badge_LevelUpNumberByName")

function GetBadge_DetailsInfo2_2Uis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.New = GetBadge_NewUis(ui:GetChild("New"))
  uis.LevelUpNumber = GetBadge_LevelUpNumberUis(ui:GetChild("LevelUpNumber"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## Badge/Badge_DetailsInfo3ByName.lua.lua
**Functions:**
- GetBadge_DetailsInfo3Uis
**Snippet:**
```lua
function GetBadge_DetailsInfo3Uis(ui)
  local uis = {}
  
  uis.InfoList = ui:GetChild("InfoList")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_DetailsInfo3_1ByName.lua.lua
**Functions:**
- GetBadge_DetailsInfo3_1Uis
**Snippet:**
```lua
function GetBadge_DetailsInfo3_1Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SuitList = ui:GetChild("SuitList")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_DetailsInfo3_2ByName.lua.lua
**Functions:**
- GetBadge_DetailsInfo3_2Uis
**Snippet:**
```lua
function GetBadge_DetailsInfo3_2Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_DetailsInfo3_3ByName.lua.lua
**Functions:**
- GetBadge_DetailsInfo3_3Uis
**Snippet:**
```lua
function GetBadge_DetailsInfo3_3Uis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.AllSuitList = ui:GetChild("AllSuitList")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_DetailsInfoByName.lua.lua
**Functions:**
- GetBadge_DetailsInfoUis
**Requires:**
- Badge_DetailsInfo1ByName
- Badge_DetailsInfo2ByName
- Badge_DetailsInfo3ByName
**Snippet:**
```lua
require("Badge_DetailsInfo1ByName")
require("Badge_DetailsInfo2ByName")
require("Badge_DetailsInfo3ByName")

function GetBadge_DetailsInfoUis(ui)
  local uis = {}
  uis.DetailsInfo1 = GetBadge_DetailsInfo1Uis(ui:GetChild("DetailsInfo1"))
  uis.ContrastBtn = ui:GetChild("ContrastBtn")
  uis.DetailsInfo2 = GetBadge_DetailsInfo2Uis(ui:GetChild("DetailsInfo2"))
  uis.DetailsInfo3 = GetBadge_DetailsInfo3Uis(ui:GetChild("DetailsInfo3"))
```

---

## Badge/Badge_DownBtnByName.lua.lua
**Functions:**
- GetBadge_DownBtnUis
**Snippet:**
```lua
function GetBadge_DownBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_EmptyEffectByName.lua.lua
**Functions:**
- GetBadge_EmptyEffectUis
**Snippet:**
```lua
function GetBadge_EmptyEffectUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_EmptyTouchBtnByName.lua.lua
**Functions:**
- GetBadge_EmptyTouchBtnUis
**Snippet:**
```lua
function GetBadge_EmptyTouchBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ExchangeByName.lua.lua
**Functions:**
- GetBadge_ExchangeUis
**Requires:**
- CommonResource_PopupBgByName
- Badge_ExchangeTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Badge_ExchangeTipsByName")

function GetBadge_ExchangeUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.PrimaryAttributeTips = GetBadge_ExchangeTipsUis(ui:GetChild("PrimaryAttributeTips"))
  uis.root = ui
  return uis
```

---

## Badge/Badge_ExchangeCardSuitBgByName.lua.lua
**Functions:**
- GetBadge_ExchangeCardSuitBgUis
**Snippet:**
```lua
function GetBadge_ExchangeCardSuitBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ExchangeCardSuitByName.lua.lua
**Functions:**
- GetBadge_ExchangeCardSuitUis
**Requires:**
- Badge_ExchangeCardSuitBgByName
- Badge_ExchangeIconByName
**Snippet:**
```lua
require("Badge_ExchangeCardSuitBgByName")
require("Badge_ExchangeIconByName")

function GetBadge_ExchangeCardSuitUis(ui)
  local uis = {}
  uis.CardBg = GetBadge_ExchangeCardSuitBgUis(ui:GetChild("CardBg"))
  uis.Icon1 = GetBadge_ExchangeIconUis(ui:GetChild("Icon1"))
  uis.Icon2 = GetBadge_ExchangeIconUis(ui:GetChild("Icon2"))
  uis.Icon3 = GetBadge_ExchangeIconUis(ui:GetChild("Icon3"))
  uis.root = ui
```

---

## Badge/Badge_ExchangeChoice1BtnByName.lua.lua
**Functions:**
- GetBadge_ExchangeChoice1BtnUis
**Snippet:**
```lua
function GetBadge_ExchangeChoice1BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ExchangeChoice2BtnByName.lua.lua
**Functions:**
- GetBadge_ExchangeChoice2BtnUis
**Snippet:**
```lua
function GetBadge_ExchangeChoice2BtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ExchangeChoiceRegionByName.lua.lua
**Functions:**
- GetBadge_ExchangeChoiceRegionUis
**Snippet:**
```lua
function GetBadge_ExchangeChoiceRegionUis(ui)
  local uis = {}
  
  uis.AllBtn = ui:GetChild("AllBtn")
  uis.Position1Btn = ui:GetChild("Position1Btn")
  uis.Position2Btn = ui:GetChild("Position2Btn")
  uis.Position3Btn = ui:GetChild("Position3Btn")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ExchangeClearBtnByName.lua.lua
**Functions:**
- GetBadge_ExchangeClearBtnUis
**Snippet:**
```lua
function GetBadge_ExchangeClearBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ExchangeCloseBtnByName.lua.lua
**Functions:**
- GetBadge_ExchangeCloseBtnUis
**Snippet:**
```lua
function GetBadge_ExchangeCloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ExchangeIconByName.lua.lua
**Functions:**
- GetBadge_ExchangeIconUis
**Requires:**
- Badge_IconLockByName
**Snippet:**
```lua
require("Badge_IconLockByName")

function GetBadge_ExchangeIconUis(ui)
  local uis = {}
  uis.IconLoader = ui:GetChild("IconLoader")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.StarList = ui:GetChild("StarList")
  uis.IconLock = GetBadge_IconLockUis(ui:GetChild("IconLock"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## Badge/Badge_ExchangeSureBtnByName.lua.lua
**Functions:**
- GetBadge_ExchangeSureBtnUis
**Snippet:**
```lua
function GetBadge_ExchangeSureBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ExchangeTipsByName.lua.lua
**Functions:**
- GetBadge_ExchangeTipsUis
**Requires:**
- Badge_ExchangeCardSuitByName
- Badge_ExchangeChoiceRegionByName
**Snippet:**
```lua
require("Badge_ExchangeCardSuitByName")
require("Badge_ExchangeChoiceRegionByName")

function GetBadge_ExchangeTipsUis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.Card1 = GetBadge_ExchangeCardSuitUis(ui:GetChild("Card1"))
  uis.Card2 = GetBadge_ExchangeCardSuitUis(ui:GetChild("Card2"))
  uis.ChoiceRegion = GetBadge_ExchangeChoiceRegionUis(ui:GetChild("ChoiceRegion"))
  uis.WordTxt = ui:GetChild("WordTxt")
```

---

## Badge/Badge_ExchangeWindowByName.lua.lua
**Functions:**
- GetBadge_ExchangeWindowUis
**Requires:**
- Badge_ExchangeByName
**Snippet:**
```lua
require("Badge_ExchangeByName")

function GetBadge_ExchangeWindowUis(ui)
  local uis = {}
  uis.Main = GetBadge_ExchangeUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ExpAddProgressBarByName.lua.lua
**Functions:**
- GetBadge_ExpAddProgressBarUis
**Requires:**
- Badge_ExpAddProgressFillByName
**Snippet:**
```lua
require("Badge_ExpAddProgressFillByName")

function GetBadge_ExpAddProgressBarUis(ui)
  local uis = {}
  uis.bar = GetBadge_ExpAddProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ExpAddProgressFillByName.lua.lua
**Functions:**
- GetBadge_ExpAddProgressFillUis
**Snippet:**
```lua
function GetBadge_ExpAddProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ExpProgressBarByName.lua.lua
**Functions:**
- GetBadge_ExpProgressBarUis
**Requires:**
- Badge_ExpProgressFillByName
**Snippet:**
```lua
require("Badge_ExpProgressFillByName")

function GetBadge_ExpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetBadge_ExpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ExpProgressFillByName.lua.lua
**Functions:**
- GetBadge_ExpProgressFillUis
**Snippet:**
```lua
function GetBadge_ExpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_FilterSortByName.lua.lua
**Functions:**
- GetBadge_FilterSortUis
**Requires:**
- CommonResource_PopupBgByName
- Badge_FilterSortTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Badge_FilterSortTipsByName")

function GetBadge_FilterSortUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.FilterSortTips = GetBadge_FilterSortTipsUis(ui:GetChild("FilterSortTips"))
  uis.root = ui
  return uis
```

---

## Badge/Badge_FilterSortChoice1BtnByName.lua.lua
**Functions:**
- GetBadge_FilterSortChoice1BtnUis
**Snippet:**
```lua
function GetBadge_FilterSortChoice1BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_FilterSortChoice2BtnByName.lua.lua
**Functions:**
- GetBadge_FilterSortChoice2BtnUis
**Snippet:**
```lua
function GetBadge_FilterSortChoice2BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.OrderTxt = ui:GetChild("OrderTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_FilterSortTipsByName.lua.lua
**Functions:**
- GetBadge_FilterSortTipsUis
**Snippet:**
```lua
function GetBadge_FilterSortTipsUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.ContentList = ui:GetChild("ContentList")
  uis.ClearBtn = ui:GetChild("ClearBtn")
  uis.SureBtn = ui:GetChild("SureBtn")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.root = ui
  return uis
```

---

## Badge/Badge_FilterSortTipsRegion1ByName.lua.lua
**Functions:**
- GetBadge_FilterSortTipsRegion1Uis
**Requires:**
- Badge_FilterSortTitle1ByName
**Snippet:**
```lua
require("Badge_FilterSortTitle1ByName")

function GetBadge_FilterSortTipsRegion1Uis(ui)
  local uis = {}
  uis.FilterSortTitle = GetBadge_FilterSortTitle1Uis(ui:GetChild("FilterSortTitle"))
  uis.ChoiceList = ui:GetChild("ChoiceList")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_FilterSortTipsRegion2ByName.lua.lua
**Functions:**
- GetBadge_FilterSortTipsRegion2Uis
**Requires:**
- Badge_FilterSortTitle2ByName
**Snippet:**
```lua
require("Badge_FilterSortTitle2ByName")

function GetBadge_FilterSortTipsRegion2Uis(ui)
  local uis = {}
  uis.FilterSortTitle = GetBadge_FilterSortTitle2Uis(ui:GetChild("FilterSortTitle"))
  uis.ChoiceList = ui:GetChild("ChoiceList")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_FilterSortTitle1ByName.lua.lua
**Functions:**
- GetBadge_FilterSortTitle1Uis
**Snippet:**
```lua
function GetBadge_FilterSortTitle1Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_FilterSortTitle2ByName.lua.lua
**Functions:**
- GetBadge_FilterSortTitle2Uis
**Snippet:**
```lua
function GetBadge_FilterSortTitle2Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_FilterSortWindowByName.lua.lua
**Functions:**
- GetBadge_FilterSortWindowUis
**Requires:**
- Badge_FilterSortByName
**Snippet:**
```lua
require("Badge_FilterSortByName")

function GetBadge_FilterSortWindowUis(ui)
  local uis = {}
  uis.Main = GetBadge_FilterSortUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_HeadFrameBgByName.lua.lua
**Functions:**
- GetBadge_HeadFrameBgUis
**Snippet:**
```lua
function GetBadge_HeadFrameBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_HeadFrameBtnByName.lua.lua
**Functions:**
- GetBadge_HeadFrameBtnUis
**Requires:**
- Badge_HeadFrameByName
**Snippet:**
```lua
require("Badge_HeadFrameByName")

function GetBadge_HeadFrameBtnUis(ui)
  local uis = {}
  uis.HeadFrame = GetBadge_HeadFrameUis(ui:GetChild("HeadFrame"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_HeadFrameByName.lua.lua
**Functions:**
- GetBadge_HeadFrameUis
**Requires:**
- Badge_OccupationByName
- Badge_HeadFrameBgByName
- Badge_CardBreachByName
- Badge_Mark1ByName
- Badge_Mark2ByName
- Badge_Mark3ByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("Badge_OccupationByName")
require("Badge_HeadFrameBgByName")
require("Badge_CardBreachByName")
require("Badge_Mark1ByName")
require("Badge_Mark2ByName")
require("Badge_Mark3ByName")
require("CommonResource_RedDotByName")

function GetBadge_HeadFrameUis(ui)
  local uis = {}
```

---

## Badge/Badge_HeadShow1BgByName.lua.lua
**Functions:**
- GetBadge_HeadShow1BgUis
**Snippet:**
```lua
function GetBadge_HeadShow1BgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_HeadShow1ByName.lua.lua
**Functions:**
- GetBadge_HeadShow1Uis
**Requires:**
- Badge_HeadShow1BgByName
**Snippet:**
```lua
require("Badge_HeadShow1BgByName")

function GetBadge_HeadShow1Uis(ui)
  local uis = {}
  uis.HeadShowBg = GetBadge_HeadShow1BgUis(ui:GetChild("HeadShowBg"))
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_HeadShowBgByName.lua.lua
**Functions:**
- GetBadge_HeadShowBgUis
**Snippet:**
```lua
function GetBadge_HeadShowBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_HeadShowByName.lua.lua
**Functions:**
- GetBadge_HeadShowUis
**Requires:**
- Badge_HeadShowBgByName
**Snippet:**
```lua
require("Badge_HeadShowBgByName")

function GetBadge_HeadShowUis(ui)
  local uis = {}
  uis.HeadShowBg = GetBadge_HeadShowBgUis(ui:GetChild("HeadShowBg"))
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_HomePageByName.lua.lua
**Functions:**
- GetBadge_HomePageUis
**Snippet:**
```lua
function GetBadge_HomePageUis(ui)
  local uis = {}
  
  uis.CardList = ui:GetChild("CardList")
  uis.DecomposeBtn = ui:GetChild("DecomposeBtn")
  uis.OverviewBtn = ui:GetChild("OverviewBtn")
  uis.AllWearBtn = ui:GetChild("AllWearBtn")
  uis.RecommendWearBtn = ui:GetChild("RecommendWearBtn")
  uis.root = ui
  return uis
```

---

## Badge/Badge_IconLockByName.lua.lua
**Functions:**
- GetBadge_IconLockUis
**Snippet:**
```lua
function GetBadge_IconLockUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_LevelAttribute1ByName.lua.lua
**Functions:**
- GetBadge_LevelAttribute1Uis
**Snippet:**
```lua
function GetBadge_LevelAttribute1Uis(ui)
  local uis = {}
  
  uis.Level1Txt = ui:GetChild("Level1Txt")
  uis.Level2Txt = ui:GetChild("Level2Txt")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_LevelAttribute2ByName.lua.lua
**Functions:**
- GetBadge_LevelAttribute2Uis
**Snippet:**
```lua
function GetBadge_LevelAttribute2Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Badge/Badge_LevelAttribute3ByName.lua.lua
**Functions:**
- GetBadge_LevelAttribute3Uis
**Requires:**
- Badge_NewByName
- Badge_LevelUpNumberByName
**Snippet:**
```lua
require("Badge_NewByName")
require("Badge_LevelUpNumberByName")

function GetBadge_LevelAttribute3Uis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.New = GetBadge_NewUis(ui:GetChild("New"))
```

---

## Badge/Badge_LevelUpInfo1ByName.lua.lua
**Functions:**
- GetBadge_LevelUpInfo1Uis
**Snippet:**
```lua
function GetBadge_LevelUpInfo1Uis(ui)
  local uis = {}
  
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.ExpTxt = ui:GetChild("ExpTxt")
  uis.ExpAddProgressBar = ui:GetChild("ExpAddProgressBar")
  uis.ExpProgressBar = ui:GetChild("ExpProgressBar")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Badge/Badge_LevelUpInfoByName.lua.lua
**Functions:**
- GetBadge_LevelUpInfoUis
**Requires:**
- Badge_LevelUpInfo1ByName
- Badge_DetailsInfo1ByName
- Badge_DetailsInfo3ByName
- Badge_DetailsInfo2ByName
**Snippet:**
```lua
require("Badge_LevelUpInfo1ByName")
require("Badge_DetailsInfo1ByName")
require("Badge_DetailsInfo3ByName")
require("Badge_DetailsInfo2ByName")

function GetBadge_LevelUpInfoUis(ui)
  local uis = {}
  uis.LevelUpInfo1 = GetBadge_LevelUpInfo1Uis(ui:GetChild("LevelUpInfo1"))
  uis.DetailsInfo1 = GetBadge_DetailsInfo1Uis(ui:GetChild("DetailsInfo1"))
  uis.DetailsInfo3 = GetBadge_DetailsInfo3Uis(ui:GetChild("DetailsInfo3"))
```

---

## Badge/Badge_LevelUpItemBtnByName.lua.lua
**Functions:**
- GetBadge_LevelUpItemBtnUis
**Snippet:**
```lua
function GetBadge_LevelUpItemBtnUis(ui)
  local uis = {}
  
  uis.IconLoader = ui:GetChild("IconLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Badge/Badge_LevelUpItemByName.lua.lua
**Functions:**
- GetBadge_LevelUpItemUis
**Snippet:**
```lua
function GetBadge_LevelUpItemUis(ui)
  local uis = {}
  
  uis.LevelUpItemBtn = ui:GetChild("LevelUpItemBtn")
  uis.LevelUpItemReduceBtn = ui:GetChild("LevelUpItemReduceBtn")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_LevelUpItemReduceBtnByName.lua.lua
**Functions:**
- GetBadge_LevelUpItemReduceBtnUis
**Snippet:**
```lua
function GetBadge_LevelUpItemReduceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_LevelUpItemWordByName.lua.lua
**Functions:**
- GetBadge_LevelUpItemWordUis
**Snippet:**
```lua
function GetBadge_LevelUpItemWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_LevelUpListByName.lua.lua
**Functions:**
- GetBadge_LevelUpListUis
**Requires:**
- Badge_LevelUpItemWordByName
- CommonResource_AssetsTipsByName
- Badge_UpGoldSpendByName
- Badge_LevelUpMaxByName
**Snippet:**
```lua
require("Badge_LevelUpItemWordByName")
require("CommonResource_AssetsTipsByName")
require("Badge_UpGoldSpendByName")
require("Badge_LevelUpMaxByName")

function GetBadge_LevelUpListUis(ui)
  local uis = {}
  uis.BadgeList = ui:GetChild("BadgeList")
  uis.Word = GetBadge_LevelUpItemWordUis(ui:GetChild("Word"))
  uis.AssetsTips = GetCommonResource_AssetsTipsUis(ui:GetChild("AssetsTips"))
```

---

## Badge/Badge_LevelUpMaxByName.lua.lua
**Functions:**
- GetBadge_LevelUpMaxUis
**Snippet:**
```lua
function GetBadge_LevelUpMaxUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_LevelUpNumberByName.lua.lua
**Functions:**
- GetBadge_LevelUpNumberUis
**Snippet:**
```lua
function GetBadge_LevelUpNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_LevelUpTipsAni1ByName.lua.lua
**Functions:**
- GetBadge_LevelUpTipsAni1Uis
**Snippet:**
```lua
function GetBadge_LevelUpTipsAni1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_LevelUpTipsAni2ByName.lua.lua
**Functions:**
- GetBadge_LevelUpTipsAni2Uis
**Snippet:**
```lua
function GetBadge_LevelUpTipsAni2Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_LevelUpTipsByName.lua.lua
**Functions:**
- GetBadge_LevelUpTipsUis
**Requires:**
- CommonResource_PopupBgByName
- Badge_LevelUpTipsContentByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Badge_LevelUpTipsContentByName")

function GetBadge_LevelUpTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.LevelUpTipsContent = GetBadge_LevelUpTipsContentUis(ui:GetChild("LevelUpTipsContent"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.root = ui
  return uis
```

---

## Badge/Badge_LevelUpTipsContentByName.lua.lua
**Functions:**
- GetBadge_LevelUpTipsContentUis
**Requires:**
- Badge_LevelUpTipsAni1ByName
- Badge_LevelUpTipsAni2ByName
- Badge_LevelAttribute1ByName
**Snippet:**
```lua
require("Badge_LevelUpTipsAni1ByName")
require("Badge_LevelUpTipsAni2ByName")
require("Badge_LevelAttribute1ByName")

function GetBadge_LevelUpTipsContentUis(ui)
  local uis = {}
  uis.TipsAni1 = GetBadge_LevelUpTipsAni1Uis(ui:GetChild("TipsAni1"))
  uis.TipsAni2 = GetBadge_LevelUpTipsAni2Uis(ui:GetChild("TipsAni2"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.LevelAttribute1 = GetBadge_LevelAttribute1Uis(ui:GetChild("LevelAttribute1"))
```

---

## Badge/Badge_LevelUpTipsWindowByName.lua.lua
**Functions:**
- GetBadge_LevelUpTipsWindowUis
**Requires:**
- Badge_LevelUpTipsByName
**Snippet:**
```lua
require("Badge_LevelUpTipsByName")

function GetBadge_LevelUpTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetBadge_LevelUpTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_LevelUpWordByName.lua.lua
**Functions:**
- GetBadge_LevelUpWordUis
**Snippet:**
```lua
function GetBadge_LevelUpWordUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_LeveUpBtnByName.lua.lua
**Functions:**
- GetBadge_LeveUpBtnUis
**Snippet:**
```lua
function GetBadge_LeveUpBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_LockByName.lua.lua
**Functions:**
- GetBadge_LockUis
**Snippet:**
```lua
function GetBadge_LockUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_Mark1ByName.lua.lua
**Functions:**
- GetBadge_Mark1Uis
**Snippet:**
```lua
function GetBadge_Mark1Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_Mark2ByName.lua.lua
**Functions:**
- GetBadge_Mark2Uis
**Snippet:**
```lua
function GetBadge_Mark2Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_Mark3ByName.lua.lua
**Functions:**
- GetBadge_Mark3Uis
**Snippet:**
```lua
function GetBadge_Mark3Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_NewByName.lua.lua
**Functions:**
- GetBadge_NewUis
**Snippet:**
```lua
function GetBadge_NewUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_OccupationByName.lua.lua
**Functions:**
- GetBadge_OccupationUis
**Snippet:**
```lua
function GetBadge_OccupationUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_OverviewBtnByName.lua.lua
**Functions:**
- GetBadge_OverviewBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetBadge_OverviewBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_PartsByName.lua.lua
**Functions:**
- GetBadge_PartsUis
**Requires:**
- Badge_PartsLevelByName
**Snippet:**
```lua
require("Badge_PartsLevelByName")

function GetBadge_PartsUis(ui)
  local uis = {}
  uis.IconLoader = ui:GetChild("IconLoader")
  uis.Level = GetBadge_PartsLevelUis(ui:GetChild("Level"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.EffectHolder1 = ui:GetChild("EffectHolder1")
  uis.TouchBtn = ui:GetChild("TouchBtn")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Badge/Badge_PartsCardAttributeByName.lua.lua
**Functions:**
- GetBadge_PartsCardAttributeUis
**Snippet:**
```lua
function GetBadge_PartsCardAttributeUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_PartsCardBgByName.lua.lua
**Functions:**
- GetBadge_PartsCardBgUis
**Snippet:**
```lua
function GetBadge_PartsCardBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_PartsCardByName.lua.lua
**Functions:**
- GetBadge_PartsCardUis
**Requires:**
- Badge_PartsCardBgByName
**Snippet:**
```lua
require("Badge_PartsCardBgByName")

function GetBadge_PartsCardUis(ui)
  local uis = {}
  uis.AttributeList = ui:GetChild("AttributeList")
  uis.PartsCardBg = GetBadge_PartsCardBgUis(ui:GetChild("PartsCardBg"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_PartsInfoByName.lua.lua
**Functions:**
- GetBadge_PartsInfoUis
**Requires:**
- Badge_PartsCardByName
**Snippet:**
```lua
require("Badge_PartsCardByName")

function GetBadge_PartsInfoUis(ui)
  local uis = {}
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.StarList = ui:GetChild("StarList")
  uis.PartsCard = GetBadge_PartsCardUis(ui:GetChild("PartsCard"))
  uis.RecommendWearBtn = ui:GetChild("RecommendWearBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## Badge/Badge_PartsInfoStarByName.lua.lua
**Functions:**
- GetBadge_PartsInfoStarUis
**Snippet:**
```lua
function GetBadge_PartsInfoStarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_PartsLevelByName.lua.lua
**Functions:**
- GetBadge_PartsLevelUis
**Snippet:**
```lua
function GetBadge_PartsLevelUis(ui)
  local uis = {}
  
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_PrimaryAttributeByName.lua.lua
**Functions:**
- GetBadge_PrimaryAttributeUis
**Requires:**
- CommonResource_PopupBgByName
- Badge_PrimaryAttributeTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Badge_PrimaryAttributeTipsByName")

function GetBadge_PrimaryAttributeUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.PrimaryAttributeTips = GetBadge_PrimaryAttributeTipsUis(ui:GetChild("PrimaryAttributeTips"))
  uis.root = ui
  return uis
```

---

## Badge/Badge_PrimaryAttributeChoiceBtnByName.lua.lua
**Functions:**
- GetBadge_PrimaryAttributeChoiceBtnUis
**Snippet:**
```lua
function GetBadge_PrimaryAttributeChoiceBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_PrimaryAttributeTipsByName.lua.lua
**Functions:**
- GetBadge_PrimaryAttributeTipsUis
**Snippet:**
```lua
function GetBadge_PrimaryAttributeTipsUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.ContentList = ui:GetChild("ContentList")
  uis.ClearBtn = ui:GetChild("ClearBtn")
  uis.SureBtn = ui:GetChild("SureBtn")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.root = ui
  return uis
```

---

## Badge/Badge_PrimaryAttributeWindowByName.lua.lua
**Functions:**
- GetBadge_PrimaryAttributeWindowUis
**Requires:**
- Badge_PrimaryAttributeByName
**Snippet:**
```lua
require("Badge_PrimaryAttributeByName")

function GetBadge_PrimaryAttributeWindowUis(ui)
  local uis = {}
  uis.Main = GetBadge_PrimaryAttributeUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_RecommendWear1BtnByName.lua.lua
**Functions:**
- GetBadge_RecommendWear1BtnUis
**Snippet:**
```lua
function GetBadge_RecommendWear1BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_RecommendWearBtnByName.lua.lua
**Functions:**
- GetBadge_RecommendWearBtnUis
**Snippet:**
```lua
function GetBadge_RecommendWearBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ResettingBtnByName.lua.lua
**Functions:**
- GetBadge_ResettingBtnUis
**Snippet:**
```lua
function GetBadge_ResettingBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_RewardItemByName.lua.lua
**Functions:**
- GetBadge_RewardItemUis
**Snippet:**
```lua
function GetBadge_RewardItemUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_RewardItemReduceByName.lua.lua
**Functions:**
- GetBadge_RewardItemReduceUis
**Requires:**
- Badge_RewardItemByName
**Snippet:**
```lua
require("Badge_RewardItemByName")

function GetBadge_RewardItemReduceUis(ui)
  local uis = {}
  uis.RewardItem = GetBadge_RewardItemUis(ui:GetChild("RewardItem"))
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ScreenSureBtnByName.lua.lua
**Functions:**
- GetBadge_ScreenSureBtnUis
**Snippet:**
```lua
function GetBadge_ScreenSureBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ScreenTitle1BtnByName.lua.lua
**Functions:**
- GetBadge_ScreenTitle1BtnUis
**Snippet:**
```lua
function GetBadge_ScreenTitle1BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ScreenTitle2BtnByName.lua.lua
**Functions:**
- GetBadge_ScreenTitle2BtnUis
**Snippet:**
```lua
function GetBadge_ScreenTitle2BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ScreenTitleByName.lua.lua
**Functions:**
- GetBadge_ScreenTitleUis
**Snippet:**
```lua
function GetBadge_ScreenTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ScreenTitleStrip1BtnByName.lua.lua
**Functions:**
- GetBadge_ScreenTitleStrip1BtnUis
**Snippet:**
```lua
function GetBadge_ScreenTitleStrip1BtnUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ScreenTitleStrip3BtnByName.lua.lua
**Functions:**
- GetBadge_ScreenTitleStrip3BtnUis
**Snippet:**
```lua
function GetBadge_ScreenTitleStrip3BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ScreenTitleStrip4BtnByName.lua.lua
**Functions:**
- GetBadge_ScreenTitleStrip4BtnUis
**Snippet:**
```lua
function GetBadge_ScreenTitleStrip4BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ScreenTitleTips1ByName.lua.lua
**Functions:**
- GetBadge_ScreenTitleTips1Uis
**Requires:**
- Badge_ScreenTitleByName
**Snippet:**
```lua
require("Badge_ScreenTitleByName")

function GetBadge_ScreenTitleTips1Uis(ui)
  local uis = {}
  uis.ScreenTitle = GetBadge_ScreenTitleUis(ui:GetChild("ScreenTitle"))
  uis.ScreenTitleBtn = ui:GetChild("ScreenTitleBtn")
  uis.TipsList = ui:GetChild("TipsList")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ScreenTitleTips2ByName.lua.lua
**Functions:**
- GetBadge_ScreenTitleTips2Uis
**Requires:**
- Badge_ScreenTitleByName
**Snippet:**
```lua
require("Badge_ScreenTitleByName")

function GetBadge_ScreenTitleTips2Uis(ui)
  local uis = {}
  uis.ScreenTitle = GetBadge_ScreenTitleUis(ui:GetChild("ScreenTitle"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ScreenTitleTips3ByName.lua.lua
**Functions:**
- GetBadge_ScreenTitleTips3Uis
**Requires:**
- Badge_ScreenTitleByName
**Snippet:**
```lua
require("Badge_ScreenTitleByName")

function GetBadge_ScreenTitleTips3Uis(ui)
  local uis = {}
  uis.ScreenTitle = GetBadge_ScreenTitleUis(ui:GetChild("ScreenTitle"))
  uis.ScreenTitleBtn = ui:GetChild("ScreenTitleBtn")
  uis.TipsList = ui:GetChild("TipsList")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_ScreenTitleTips4ByName.lua.lua
**Functions:**
- GetBadge_ScreenTitleTips4Uis
**Requires:**
- Badge_ScreenTitleByName
**Snippet:**
```lua
require("Badge_ScreenTitleByName")

function GetBadge_ScreenTitleTips4Uis(ui)
  local uis = {}
  uis.ScreenTitle = GetBadge_ScreenTitleUis(ui:GetChild("ScreenTitle"))
  uis.ScreenTitleBtn = ui:GetChild("ScreenTitleBtn")
  uis.TipsList = ui:GetChild("TipsList")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_SecondaryAttributeByName.lua.lua
**Functions:**
- GetBadge_SecondaryAttributeUis
**Requires:**
- CommonResource_PopupBgByName
- Badge_SecondaryAttributeTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Badge_SecondaryAttributeTipsByName")

function GetBadge_SecondaryAttributeUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.PrimaryAttributeTips = GetBadge_SecondaryAttributeTipsUis(ui:GetChild("PrimaryAttributeTips"))
  uis.root = ui
  return uis
```

---

## Badge/Badge_SecondaryAttributeChoiceBtnByName.lua.lua
**Functions:**
- GetBadge_SecondaryAttributeChoiceBtnUis
**Snippet:**
```lua
function GetBadge_SecondaryAttributeChoiceBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_SecondaryAttributeTipsByName.lua.lua
**Functions:**
- GetBadge_SecondaryAttributeTipsUis
**Snippet:**
```lua
function GetBadge_SecondaryAttributeTipsUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.ContentList = ui:GetChild("ContentList")
  uis.ClearBtn = ui:GetChild("ClearBtn")
  uis.SureBtn = ui:GetChild("SureBtn")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
```

---

## Badge/Badge_SecondaryAttributeWindowByName.lua.lua
**Functions:**
- GetBadge_SecondaryAttributeWindowUis
**Requires:**
- Badge_SecondaryAttributeByName
**Snippet:**
```lua
require("Badge_SecondaryAttributeByName")

function GetBadge_SecondaryAttributeWindowUis(ui)
  local uis = {}
  uis.Main = GetBadge_SecondaryAttributeUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_SortBtnByName.lua.lua
**Functions:**
- GetBadge_SortBtnUis
**Snippet:**
```lua
function GetBadge_SortBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_StarByName.lua.lua
**Functions:**
- GetBadge_StarUis
**Snippet:**
```lua
function GetBadge_StarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_SuitChoiceBtnByName.lua.lua
**Functions:**
- GetBadge_SuitChoiceBtnUis
**Snippet:**
```lua
function GetBadge_SuitChoiceBtnUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_SuitScreenByName.lua.lua
**Functions:**
- GetBadge_SuitScreenUis
**Requires:**
- CommonResource_PopupBgByName
- Badge_SuitTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Badge_SuitTipsByName")

function GetBadge_SuitScreenUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.SuitTips = GetBadge_SuitTipsUis(ui:GetChild("SuitTips"))
  uis.root = ui
  return uis
```

---

## Badge/Badge_SuitScreenWindowByName.lua.lua
**Functions:**
- GetBadge_SuitScreenWindowUis
**Requires:**
- Badge_SuitScreenByName
**Snippet:**
```lua
require("Badge_SuitScreenByName")

function GetBadge_SuitScreenWindowUis(ui)
  local uis = {}
  uis.Main = GetBadge_SuitScreenUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_SuitTipsByName.lua.lua
**Functions:**
- GetBadge_SuitTipsUis
**Snippet:**
```lua
function GetBadge_SuitTipsUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.ContentList = ui:GetChild("ContentList")
  uis.ClearBtn = ui:GetChild("ClearBtn")
  uis.SureBtn = ui:GetChild("SureBtn")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.root = ui
  return uis
```

---

## Badge/Badge_SuitTipsClearBtnByName.lua.lua
**Functions:**
- GetBadge_SuitTipsClearBtnUis
**Snippet:**
```lua
function GetBadge_SuitTipsClearBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_SuitTipsCloseBtnByName.lua.lua
**Functions:**
- GetBadge_SuitTipsCloseBtnUis
**Snippet:**
```lua
function GetBadge_SuitTipsCloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_SuitTipsSureBtnByName.lua.lua
**Functions:**
- GetBadge_SuitTipsSureBtnUis
**Snippet:**
```lua
function GetBadge_SuitTipsSureBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_TabBtnBgByName.lua.lua
**Functions:**
- GetBadge_TabBtnBgUis
**Snippet:**
```lua
function GetBadge_TabBtnBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_TabBtnByName.lua.lua
**Functions:**
- GetBadge_TabBtnUis
**Requires:**
- Badge_TabBtnBgByName
**Snippet:**
```lua
require("Badge_TabBtnBgByName")

function GetBadge_TabBtnUis(ui)
  local uis = {}
  uis.TabBtnBg = GetBadge_TabBtnBgUis(ui:GetChild("TabBtnBg"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_TabRegionByName.lua.lua
**Functions:**
- GetBadge_TabRegionUis
**Snippet:**
```lua
function GetBadge_TabRegionUis(ui)
  local uis = {}
  
  uis.Tab1Btn = ui:GetChild("Tab1Btn")
  uis.Tab2Btn = ui:GetChild("Tab2Btn")
  uis.Tab3Btn = ui:GetChild("Tab3Btn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_UpBtnByName.lua.lua
**Functions:**
- GetBadge_UpBtnUis
**Snippet:**
```lua
function GetBadge_UpBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_UpGoldSpendByName.lua.lua
**Functions:**
- GetBadge_UpGoldSpendUis
**Snippet:**
```lua
function GetBadge_UpGoldSpendUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Badge/Badge_WearBadgeContainerByName.lua.lua
**Functions:**
- GetBadge_WearBadgeContainerUis
**Requires:**
- Badge_TabRegionByName
- Badge_ChoiceSortByName
**Snippet:**
```lua
require("Badge_TabRegionByName")
require("Badge_ChoiceSortByName")

function GetBadge_WearBadgeContainerUis(ui)
  local uis = {}
  uis.TabRegion = GetBadge_TabRegionUis(ui:GetChild("TabRegion"))
  uis.BadgeList = ui:GetChild("BadgeList")
  uis.ChoiceBtn = ui:GetChild("ChoiceBtn")
  uis.ChoiceSort = GetBadge_ChoiceSortUis(ui:GetChild("ChoiceSort"))
  uis.root = ui
```

---

## Badge/BagData.lua.lua
**Functions:**
- BagData.GetSelectType
- BagData.SetSelectType
- BagData.GetItemByType
- BagData.GetCardSort
- BagData.SortBadge
**Snippet:**
```lua
BagData = {selectType = nil}

function BagData.GetSelectType()
  if BagData.selectType == nil then
    BagData.selectType = BAG_TYPE.ALL
  end
  return BagData.selectType
end

function BagData.SetSelectType(selectType)
```

---

## Badge/BagMgr.lua.lua
**Snippet:**
```lua
BagMgr = {}
```

---

## Badge/BagScriptList.lua.lua
**Requires:**
- BagMgr
- BagData
- BagService
**Snippet:**
```lua
local require = require
require("BagMgr")
require("BagData")
require("BagService")
```

---

## Badge/BagService.lua.lua
**Functions:**
- BagService.Init
- BagService.SaleItemReq
- BagService.DealSaleItemRsp
- BagService.UseItemReq
- BagService.DealUseItemRsp
**Snippet:**
```lua
BagService = {}

function BagService.Init()
  Net.AddListener(Proto.MsgName.SaleItemRsp, BagService.DealSaleItemRsp)
  Net.AddListener(Proto.MsgName.UseItemRsp, BagService.DealUseItemRsp)
end

function BagService.SaleItemReq(itemUid, itemCount, rspCallBack)
  local msg = {}
  msg.itemUid = itemUid
```

---

## Badge/BagWindow.lua.lua
**Functions:**
- BagWindow.ReInitData
- BagWindow.OnInit
- BagWindow.UpdateBackground
- BagWindow.InitList
- BagWindow.UpdateInfo
- BagWindow.UpdateFuncUnlock
- BagWindow.UpdateTextDisplay
- BagWindow.InitBtn
- BagWindow.UpdateItemList
- BagWindow.ShowBadgeNum
- BagWindow.RefreshItem
- BagWindow.StopAnim
- BagWindow.TouchItem
- BagWindow.CheckItemTime
- BagWindow.OnShown
- BagWindow.OnHide
- BagWindow.OnClose
- BagWindow.HandleMessage
**Requires:**
- Bag_BagWindowByName
**Snippet:**
```lua
require("Bag_BagWindowByName")
local BagWindow = {}
local uis, contentPane, itemInfoList, itemList, jumpTb
local timeIndex = 0
local isPlayAnim, animTime

function BagWindow.ReInitData()
end

function BagWindow.OnInit(bridgeObj)
```

---

## Badge/Bag_BadgeDecomposeBtnByName.lua.lua
**Functions:**
- GetBag_BadgeDecomposeBtnUis
**Snippet:**
```lua
function GetBag_BadgeDecomposeBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## Badge/Bag_BadgeGoBtnByName.lua.lua
**Functions:**
- GetBag_BadgeGoBtnUis
**Snippet:**
```lua
function GetBag_BadgeGoBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## Badge/Bag_BadgeMemoryByName.lua.lua
**Functions:**
- GetBag_BadgeMemoryUis
**Snippet:**
```lua
function GetBag_BadgeMemoryUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Badge/Bag_BagByName.lua.lua
**Functions:**
- GetBag_BagUis
**Requires:**
- CommonResource_BackGroundByName
- Bag_TabRegionByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Bag_TabRegionByName")
require("CommonResource_CurrencyReturnByName")

function GetBag_BagUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.TabRegion = GetBag_TabRegionUis(ui:GetChild("TabRegion"))
  uis.BadgeDecomposeBtn = ui:GetChild("BadgeDecomposeBtn")
```

---

## Badge/Bag_BagWindowByName.lua.lua
**Functions:**
- GetBag_BagWindowUis
**Requires:**
- Bag_BagByName
**Snippet:**
```lua
require("Bag_BagByName")

function GetBag_BagWindowUis(ui)
  local uis = {}
  uis.Main = GetBag_BagUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Badge/Bag_ExploreDevelopBtnByName.lua.lua
**Functions:**
- GetBag_ExploreDevelopBtnUis
**Snippet:**
```lua
function GetBag_ExploreDevelopBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## Badge/Bag_ItemAniByName.lua.lua
**Functions:**
- GetBag_ItemAniUis
**Requires:**
- CommonResource_ItemFrameByName
**Snippet:**
```lua
require("CommonResource_ItemFrameByName")

function GetBag_ItemAniUis(ui)
  local uis = {}
  uis.ItemFrame = GetCommonResource_ItemFrameUis(ui:GetChild("ItemFrame"))
  uis.root = ui
  return uis
end
```

---

## Badge/Bag_TabBtnBgByName.lua.lua
**Functions:**
- GetBag_TabBtnBgUis
**Snippet:**
```lua
function GetBag_TabBtnBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Badge/Bag_TabBtnByName.lua.lua
**Functions:**
- GetBag_TabBtnUis
**Requires:**
- Bag_TabBtnBgByName
- Bag_BadgeMemoryByName
**Snippet:**
```lua
require("Bag_TabBtnBgByName")
require("Bag_BadgeMemoryByName")

function GetBag_TabBtnUis(ui)
  local uis = {}
  uis.TabBtnBg = GetBag_TabBtnBgUis(ui:GetChild("TabBtnBg"))
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.BadgeMemory = GetBag_BadgeMemoryUis(ui:GetChild("BadgeMemory"))
  uis.buttonCtr = ui:GetController("button")
```

---

## Badge/Bag_TabRegionByName.lua.lua
**Functions:**
- GetBag_TabRegionUis
**Snippet:**
```lua
function GetBag_TabRegionUis(ui)
  local uis = {}
  
  uis.Tab1Btn = ui:GetChild("Tab1Btn")
  uis.Tab2Btn = ui:GetChild("Tab2Btn")
  uis.Tab3Btn = ui:GetChild("Tab3Btn")
  uis.Tab4Btn = ui:GetChild("Tab4Btn")
  uis.Tab5Btn = ui:GetChild("Tab5Btn")
  uis.Tab6Btn = ui:GetChild("Tab6Btn")
  uis.c1Ctr = ui:GetController("c1")
```

---
