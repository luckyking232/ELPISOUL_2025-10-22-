# Abyss

## Abyss/AbyssActivityPlot_ActivityCGByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityCGUis
**Requires:**
- CommonResource_PopupBgByName
- AbyssActivityPlot_ActivityCG_TipsRegionByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("AbyssActivityPlot_ActivityCG_TipsRegionByName")

function GetAbyssActivityPlot_ActivityCGUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.TipsRegion = GetAbyssActivityPlot_ActivityCG_TipsRegionUis(ui:GetChild("TipsRegion"))
  uis.root = ui
  return uis
```

---

## Abyss/AbyssActivityPlot_ActivityCGWindowByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityCGWindowUis
**Requires:**
- AbyssActivityPlot_ActivityCGByName
**Snippet:**
```lua
require("AbyssActivityPlot_ActivityCGByName")

function GetAbyssActivityPlot_ActivityCGWindowUis(ui)
  local uis = {}
  uis.Main = GetAbyssActivityPlot_ActivityCGUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityCG_CloseBtnByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityCG_CloseBtnUis
**Snippet:**
```lua
function GetAbyssActivityPlot_ActivityCG_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityCG_TipsAniByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityCG_TipsAniUis
**Snippet:**
```lua
function GetAbyssActivityPlot_ActivityCG_TipsAniUis(ui)
  local uis = {}
  
  uis.CGIconBtn = ui:GetChild("CGIconBtn")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityCG_TipsBtnByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityCG_TipsBtnUis
**Snippet:**
```lua
function GetAbyssActivityPlot_ActivityCG_TipsBtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.FlagCtr = ui:GetController("Flag")
  uis.root = ui
  return uis
```

---

## Abyss/AbyssActivityPlot_ActivityCG_TipsRegionByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityCG_TipsRegionUis
**Requires:**
- AbyssActivityPlot_ActivityCG_TitleByName
**Snippet:**
```lua
require("AbyssActivityPlot_ActivityCG_TitleByName")

function GetAbyssActivityPlot_ActivityCG_TipsRegionUis(ui)
  local uis = {}
  uis.Title = GetAbyssActivityPlot_ActivityCG_TitleUis(ui:GetChild("Title"))
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.TipsList = ui:GetChild("TipsList")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityCG_TitleByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityCG_TitleUis
**Snippet:**
```lua
function GetAbyssActivityPlot_ActivityCG_TitleUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityGameByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityGameUis
**Requires:**
- CommonResource_PopupBgByName
- AbyssActivityPlot_ActivityGame_TipsRegionByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("AbyssActivityPlot_ActivityGame_TipsRegionByName")

function GetAbyssActivityPlot_ActivityGameUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.TipsRegion = GetAbyssActivityPlot_ActivityGame_TipsRegionUis(ui:GetChild("TipsRegion"))
  uis.root = ui
  return uis
```

---

## Abyss/AbyssActivityPlot_ActivityGameWindowByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityGameWindowUis
**Requires:**
- AbyssActivityPlot_ActivityGameByName
**Snippet:**
```lua
require("AbyssActivityPlot_ActivityGameByName")

function GetAbyssActivityPlot_ActivityGameWindowUis(ui)
  local uis = {}
  uis.Main = GetAbyssActivityPlot_ActivityGameUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityGame_CloseBtnByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityGame_CloseBtnUis
**Snippet:**
```lua
function GetAbyssActivityPlot_ActivityGame_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityGame_EntryBtnByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityGame_EntryBtnUis
**Snippet:**
```lua
function GetAbyssActivityPlot_ActivityGame_EntryBtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityGame_LockByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityGame_LockUis
**Snippet:**
```lua
function GetAbyssActivityPlot_ActivityGame_LockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityGame_TipsAniByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityGame_TipsAniUis
**Requires:**
- AbyssActivityPlot_ActivityGame_TipsByName
**Snippet:**
```lua
require("AbyssActivityPlot_ActivityGame_TipsByName")

function GetAbyssActivityPlot_ActivityGame_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetAbyssActivityPlot_ActivityGame_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityGame_TipsByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityGame_TipsUis
**Requires:**
- AbyssActivityPlot_ActivityGame_LockByName
**Snippet:**
```lua
require("AbyssActivityPlot_ActivityGame_LockByName")

function GetAbyssActivityPlot_ActivityGame_TipsUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.EntryList = ui:GetChild("EntryList")
  uis.Lock = GetAbyssActivityPlot_ActivityGame_LockUis(ui:GetChild("Lock"))
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
```

---

## Abyss/AbyssActivityPlot_ActivityGame_TipsRegionByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityGame_TipsRegionUis
**Requires:**
- AbyssActivityPlot_ActivityGame_TitleByName
**Snippet:**
```lua
require("AbyssActivityPlot_ActivityGame_TitleByName")

function GetAbyssActivityPlot_ActivityGame_TipsRegionUis(ui)
  local uis = {}
  uis.Title = GetAbyssActivityPlot_ActivityGame_TitleUis(ui:GetChild("Title"))
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.TipsList = ui:GetChild("TipsList")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityGame_TitleByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityGame_TitleUis
**Snippet:**
```lua
function GetAbyssActivityPlot_ActivityGame_TitleUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityPlotAssets1ByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityPlotAssets1Uis
**Snippet:**
```lua
function GetAbyssActivityPlot_ActivityPlotAssets1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityPlotAssetsByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityPlotAssetsUis
**Snippet:**
```lua
function GetAbyssActivityPlot_ActivityPlotAssetsUis(ui)
  local uis = {}
  
  uis.IconLoader = ui:GetChild("IconLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityPlotByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityPlotUis
**Requires:**
- CommonResource_BackGroundByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("CommonResource_CurrencyReturnByName")

function GetAbyssActivityPlot_ActivityPlotUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.ShopBtn = ui:GetChild("ShopBtn")
  uis.CGBtn = ui:GetChild("CGBtn")
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
```

---

## Abyss/AbyssActivityPlot_ActivityPlotCGBtnByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityPlotCGBtnUis
**Snippet:**
```lua
function GetAbyssActivityPlot_ActivityPlotCGBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityPlotGameBtnByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityPlotGameBtnUis
**Snippet:**
```lua
function GetAbyssActivityPlot_ActivityPlotGameBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityPlotLockByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityPlotLockUis
**Snippet:**
```lua
function GetAbyssActivityPlot_ActivityPlotLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityPlotShopBtnByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityPlotShopBtnUis
**Snippet:**
```lua
function GetAbyssActivityPlot_ActivityPlotShopBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityPlotShopByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityPlotShopUis
**Requires:**
- CommonResource_BackGroundByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("CommonResource_CurrencyReturnByName")

function GetAbyssActivityPlot_ActivityPlotShopUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.ItemList = ui:GetChild("ItemList")
  uis.CurrencyReturn = GetCommonResource_CurrencyReturnUis(ui:GetChild("CurrencyReturn"))
  uis.root = ui
```

---

## Abyss/AbyssActivityPlot_ActivityPlotShopWindowByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityPlotShopWindowUis
**Requires:**
- AbyssActivityPlot_ActivityPlotShopByName
**Snippet:**
```lua
require("AbyssActivityPlot_ActivityPlotShopByName")

function GetAbyssActivityPlot_ActivityPlotShopWindowUis(ui)
  local uis = {}
  uis.Main = GetAbyssActivityPlot_ActivityPlotShopUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityPlotShop_CardHeadBgByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityPlotShop_CardHeadBgUis
**Snippet:**
```lua
function GetAbyssActivityPlot_ActivityPlotShop_CardHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityPlotShop_ItemAniByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityPlotShop_ItemAniUis
**Requires:**
- AbyssActivityPlot_ActivityPlotShop_ItemByName
**Snippet:**
```lua
require("AbyssActivityPlot_ActivityPlotShop_ItemByName")

function GetAbyssActivityPlot_ActivityPlotShop_ItemAniUis(ui)
  local uis = {}
  uis.Item = GetAbyssActivityPlot_ActivityPlotShop_ItemUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityPlotShop_ItemBtnByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityPlotShop_ItemBtnUis
**Requires:**
- AbyssActivityPlot_ActivityPlotShop_CardHeadBgByName
- AbyssActivityPlot_ActivityPlotShop_ItemNumberByName
- AbyssActivityPlot_ActivityPlotShop_UseMarkByName
**Snippet:**
```lua
require("AbyssActivityPlot_ActivityPlotShop_CardHeadBgByName")
require("AbyssActivityPlot_ActivityPlotShop_ItemNumberByName")
require("AbyssActivityPlot_ActivityPlotShop_UseMarkByName")

function GetAbyssActivityPlot_ActivityPlotShop_ItemBtnUis(ui)
  local uis = {}
  uis.CardHeadBg = GetAbyssActivityPlot_ActivityPlotShop_CardHeadBgUis(ui:GetChild("CardHeadBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.ItemNumber = GetAbyssActivityPlot_ActivityPlotShop_ItemNumberUis(ui:GetChild("ItemNumber"))
```

---

## Abyss/AbyssActivityPlot_ActivityPlotShop_ItemByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityPlotShop_ItemUis
**Requires:**
- AbyssActivityPlot_ActivityPlotShop_SellOutByName
**Snippet:**
```lua
require("AbyssActivityPlot_ActivityPlotShop_SellOutByName")

function GetAbyssActivityPlot_ActivityPlotShop_ItemUis(ui)
  local uis = {}
  uis.ItemBtn = ui:GetChild("ItemBtn")
  uis.SellOut = GetAbyssActivityPlot_ActivityPlotShop_SellOutUis(ui:GetChild("SellOut"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityPlotShop_ItemNumberByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityPlotShop_ItemNumberUis
**Snippet:**
```lua
function GetAbyssActivityPlot_ActivityPlotShop_ItemNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityPlotShop_ItemRegionByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityPlotShop_ItemRegionUis
**Requires:**
- AbyssActivityPlot_ActivityPlotShop_TitleByName
**Snippet:**
```lua
require("AbyssActivityPlot_ActivityPlotShop_TitleByName")

function GetAbyssActivityPlot_ActivityPlotShop_ItemRegionUis(ui)
  local uis = {}
  uis.ShopTitle = GetAbyssActivityPlot_ActivityPlotShop_TitleUis(ui:GetChild("ShopTitle"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityPlotShop_SellOutByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityPlotShop_SellOutUis
**Snippet:**
```lua
function GetAbyssActivityPlot_ActivityPlotShop_SellOutUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityPlotShop_StarByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityPlotShop_StarUis
**Snippet:**
```lua
function GetAbyssActivityPlot_ActivityPlotShop_StarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityPlotShop_TitleByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityPlotShop_TitleUis
**Snippet:**
```lua
function GetAbyssActivityPlot_ActivityPlotShop_TitleUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityPlotShop_UseMarkByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityPlotShop_UseMarkUis
**Snippet:**
```lua
function GetAbyssActivityPlot_ActivityPlotShop_UseMarkUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityPlotTimeByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityPlotTimeUis
**Snippet:**
```lua
function GetAbyssActivityPlot_ActivityPlotTimeUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityPlotTips1ByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityPlotTips1Uis
**Snippet:**
```lua
function GetAbyssActivityPlot_ActivityPlotTips1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityPlot_ActivityPlotTipsBtnByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityPlotTipsBtnUis
**Requires:**
- AbyssActivityPlot_ActivityPlotTips1ByName
- AbyssActivityPlot_ActivityPlotTipsByName
**Snippet:**
```lua
require("AbyssActivityPlot_ActivityPlotTips1ByName")
require("AbyssActivityPlot_ActivityPlotTipsByName")

function GetAbyssActivityPlot_ActivityPlotTipsBtnUis(ui)
  local uis = {}
  uis.Tips1 = GetAbyssActivityPlot_ActivityPlotTips1Uis(ui:GetChild("Tips1"))
  uis.Tips = GetAbyssActivityPlot_ActivityPlotTipsUis(ui:GetChild("Tips"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Abyss/AbyssActivityPlot_ActivityPlotTipsByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityPlotTipsUis
**Requires:**
- AbyssActivityPlot_ActivityPlotTimeByName
- AbyssActivityPlot_ActivityPlotLockByName
**Snippet:**
```lua
require("AbyssActivityPlot_ActivityPlotTimeByName")
require("AbyssActivityPlot_ActivityPlotLockByName")

function GetAbyssActivityPlot_ActivityPlotTipsUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.Time = GetAbyssActivityPlot_ActivityPlotTimeUis(ui:GetChild("Time"))
  uis.Lock = GetAbyssActivityPlot_ActivityPlotLockUis(ui:GetChild("Lock"))
  uis.lcokCtr = ui:GetController("lcok")
  uis.newCtr = ui:GetController("new")
```

---

## Abyss/AbyssActivityPlot_ActivityPlotWindowByName.lua.lua
**Functions:**
- GetAbyssActivityPlot_ActivityPlotWindowUis
**Requires:**
- AbyssActivityPlot_ActivityPlotByName
**Snippet:**
```lua
require("AbyssActivityPlot_ActivityPlotByName")

function GetAbyssActivityPlot_ActivityPlotWindowUis(ui)
  local uis = {}
  uis.Main = GetAbyssActivityPlot_ActivityPlotUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssActivityWindow.lua.lua
**Functions:**
- list.itemRenderer
- RefreshBuildingPanel
- RefreshTreasurePanel
- rewardlist.itemRenderer
- progresslist.itemRenderer
- statelist.itemRenderer
- AbyssActivityWindow.ReInitData
- AbyssActivityWindow.OnInit
- AbyssActivityWindow.UpdateInfo
- tablist.itemRenderer
- titlelist.itemRenderer
- AbyssActivityWindow.InitBtn
- AbyssActivityWindow.OnShown
- AbyssActivityWindow.OnClose
**Requires:**
- Abyss_ActivityWindowByName
**Snippet:**
```lua
require("Abyss_ActivityWindowByName")
local AbyssActivityWindow = {}
local uis, contentPane, pages, selectedPage, eventsBuffer, selectedEntry, selectedTabIndex, selectedPageIndex, selectedSubtabIndex, showFromHide, timer, wait
local GetRegionName = function(regionId)
  local regionConf = TableData.GetConfig(regionId, "BaseManorMapSub")
  local regionName = type(regionConf.name) == "function" and regionConf.name() or regionId
  return regionName
end
local StartTimer = function(updateFunc)
  if timer then
```

---

## Abyss/AbyssBattleEventHandleWindow.lua.lua
**Functions:**
- AbyssBattleEventHandleWindow.ReInitData
- AbyssBattleEventHandleWindow.OnInit
- AbyssBattleEventHandleWindow.UpdateInfo
- btnlist.itemRenderer
- wordlist.itemRenderer
- AbyssBattleEventHandleWindow.InitBtn
- AbyssBattleEventHandleWindow.OnClose
**Requires:**
- Abyss_MobWindowByName
**Snippet:**
```lua
require("Abyss_MobWindowByName")
local AbyssBattleEventHandleWindow = {}
local uis, contentPane, grid, eventInfo
local BTN_TITLE_FUNC = {
  [1] = {
    ui_ctrl_index = 0,
    title = T(20361),
    callback = function()
      AbyssExploreMgr.Dispatch(AbyssExploreMsgEnum.TRIGGER_BATTLE, grid, eventInfo)
      local stageId = tonumber(eventInfo.param)
```

---

## Abyss/AbyssBigMapWindow.lua.lua
**Functions:**
- AbyssBigMapWindow.ReInitData
- AbyssBigMapWindow.OnInit
- AbyssBigMapWindow.UpdateInfo
- AbyssBigMapWindow.InitBtn
- AbyssBigMapWindow.OnClose
- AbyssBigMapWindow.HandleMessage
**Requires:**
- Abyss_BigMapWindowByName
**Snippet:**
```lua
require("Abyss_BigMapWindowByName")
local AbyssBigMapWindow = {}
local uis, contentPane, initWidth, initHeight
local extendScale, minExtendScale, maxExtendScale, sensitivity = 0, 0, 0.3, 0.01
local mapCache, playerflag, eventflags, FOWHolder, minimapFOWMask
local pathpoints = {}
local pathRenderer, tempHolder, tweenId
local UpdatePathpoints = function(points)
  for _ = 1, #pathpoints do
    table.remove(pathpoints)
```

---

## Abyss/AbyssButtonTipsWindow.lua.lua
**Functions:**
- AbyssButtonTipsWindow.ReInitData
- AbyssButtonTipsWindow.OnInit
- AbyssButtonTipsWindow.UpdateInfo
- AbyssButtonTipsWindow.InitBtn
- AbyssButtonTipsWindow.OnClose
**Requires:**
- AbyssFunctionOpen_AbyssButtonTipsWindowByName
**Snippet:**
```lua
require("AbyssFunctionOpen_AbyssButtonTipsWindowByName")
local AbyssButtonTipsWindow = {}
local uis, contentPane, canOpaque, openId

function AbyssButtonTipsWindow.ReInitData()
end

function AbyssButtonTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.AbyssButtonTipsWindow.package, WinResConfig.AbyssButtonTipsWindow.comName, function(com)
    contentPane = com
```

---

## Abyss/AbyssEventList.lua.lua
**Snippet:**
```lua
local eventsBuffer
local version = 0
local busy = false
local visible = true
local clickEffectPath, getEventControllerIndexFunc
local EventHandleItemRenderer = function(i, item)
  local child = item:GetChild("EventTips")
  child.alpha = 0
  if i < #eventsBuffer - 1 then
    LeanTween.delayedCall((i + 1) * 0.08, function()
```

---

## Abyss/AbyssExploreCamCtrl.lua.lua
**Snippet:**
```lua
local camCache, mapcamCache
local GetCameraInst = function()
  return camCache
end
local GetMapcamInst = function()
  return mapcamCache
end
local Follow = function(position, lerp)
  if not mapcamCache then
    return
```

---

## Abyss/AbyssExploreChrCtrl.lua.lua
**Snippet:**
```lua
local CHR_go, CHR_Root, CHR_Spine, fashionIdCache, cachedCardId
local busy = false
local motion, lastmotion = false, false
local movespeed = 4
local move_anim_speed = 1
local waypoints, waypointsIndex, track
local epsilon = 0.001
local pointsmemory, __event_lock, gridTargetEff, pathRenderers, footprints, footprint_count, footprint_elapse, footprint_interval
local footprint_lookup = {
  [0] = "Assets/Art/Map/Prefab/footprint_common.prefab",
```

---

## Abyss/AbyssExploreConst.lua.lua
**Snippet:**
```lua
AbyssExploreEventID = {
  POSITIVE = 1,
  BRANCH = 2,
  DAILY_RANDOM = 3,
  BUILDING = 4,
  BUILDING_RANDOM = 5,
  OBSTACLE = 6,
  ILLUSTRATIONS_BGM = 7,
  ILLUSTRATIONS_MONSTER = 8,
  DAILY_RANDOM_NEWBIE = 9,
```

---

## Abyss/AbyssExploreData.lua.lua
**Snippet:**
```lua
local branchEvents, completedBranchEvents, allEvents, activities, focusevents, manorInfo, featureSchedules, plotValueRecoverTimestamp, actionValueRecoverTimestamp
local InsertBranchEvent = function(eventInfo)
  if not table.keyof(branchEvents, eventInfo.eventId, "eventId") and not eventInfo.suspend then
    table.insert(branchEvents, eventInfo)
  end
end
local InsertCompletedBranchEvent = function(eventInfo)
  table.insert(completedBranchEvents, eventInfo)
end
local DeleteBranchEvent = function(eventInfo)
```

---

## Abyss/AbyssExploreEventHandler.lua.lua
**Snippet:**
```lua
local CheckAndHandle = function(eventInfo, handleCallback)
  if AbyssExploreMgr.EventIsHandleable(eventInfo, false) and handleCallback then
    handleCallback()
  end
end
local OnTriggerBattle = function(grid, eventInfo, stageId)
  local type = eventInfo.type
  if type == AbyssExploreEventID.POSITIVE or type == AbyssExploreEventID.DAILY_RANDOM or type == AbyssExploreEventID.DAILY_RANDOM_NEWBIE then
    if AbyssExploreMgr.RegionIsCleared(1) then
      CheckAndHandle(eventInfo, function()
```

---

## Abyss/AbyssExploreFastWindow.lua.lua
**Functions:**
- AbyssExploreFastWindow.ReInitData
- AbyssExploreFastWindow.OnInit
- AbyssExploreFastWindow.SaveChoiceInfo
- AbyssExploreFastWindow.UpdateInfo
- AbyssExploreFastWindow.ShopItemRenderer
- AbyssExploreFastWindow.UpdateList
- tips.Item2List.itemRenderer
- AbyssExploreFastWindow.GetNum
- AbyssExploreFastWindow.SetNum
- AbyssExploreFastWindow.GetGesture
- AbyssExploreFastWindow.GetGridId
- AbyssExploreFastWindow.InitBtn
- AbyssExploreFastWindow.OnClose
**Requires:**
- Abyss_ExploreFastWindowByName
**Snippet:**
```lua
require("Abyss_ExploreFastWindowByName")
local AbyssExploreFastWindow = {}
local uis, contentPane, goods, choiceInfo, priceInfo, priceConf, numMax, allSellPrice, canSell
local transPlay = {}
local transItem = {}

function AbyssExploreFastWindow.ReInitData()
end

function AbyssExploreFastWindow.OnInit(bridgeObj)
```

---

## Abyss/AbyssExploreFramingOperation.lua.lua
**Functions:**
- afterDelayCallback
- afterDelayCallback
- destroyedCallback
- destroyedCallback
**Snippet:**
```lua
local operation_pool, operation_sequence, tweeners
OP_TYPE = {
  EVENT_CREATE = 1,
  EVENT_DELETE = 2,
  EVENT_TRIGGER = 4,
  ILLUSTRATION_GET = 8,
  REGION_UNLOCK_TIPS = 16,
  FUNC_UNLOCK = 32,
  CINEMATICS = 64,
  DELAY_CALLBACK = 128
```

---

## Abyss/AbyssExploreLocalTestSupport.lua.lua
**Functions:**
- BattleMgr.SendBattleOverMsg
- FormationMgr.SendBattleReq
**Snippet:**
```lua
if Application.platform ~= RuntimePlatform.WindowsEditor and Application.platform ~= RuntimePlatform.OSXEditor then
  return
end
local CloseBattle_LocalTest = function(msg, rspCallback)
  local extData = msg.battleData.initData.extData
  if type(extData) == "table" then
    local storyId = extData.curStoryId
    local eventInfo = extData.eventInfo
    eventInfo.storyRecords = eventInfo.storyRecords or {}
    table.insert(eventInfo.storyRecords, storyId)
```

---

## Abyss/AbyssExploreMapCtrl.lua.lua
**Functions:**
- renderer.OnSliceLoaded
**Snippet:**
```lua
local mapViewCache, mapLogicCache, groups, snapshot
local ignoreObstacle = false
local enableSearchPath = true
local mapResMgr, pathRenderers, sceneItemVisibleFunc, globalScale
local LoadMapData = function(mapId)
  local path
  if mapId >= EXPLORE_MAP_ID.ACTIVITY_1 then
    path = "Assets/Data/ExploreMapData/activity_map_data@" .. tostring(mapId) .. ".bytes"
  elseif mapId >= EXPLORE_MAP_ID.GUILD_WAR_1 then
    path = "Assets/Data/ExploreMapData/guildwar_map_data@" .. tostring(mapId) .. ".bytes"
```

---

## Abyss/AbyssExploreMapflag.lua.lua
**Snippet:**
```lua
local reuseables = {}
local init = function(self, gobj, parent, mapObj, ratiox, ratioy, maprect)
  self.gobj = gobj
  self.mapObj = mapObj
  self.maprect = maprect
  self:setpos(ratiox or 0, ratioy or 0)
  self:setparent(parent)
  local flag_obj = gobj:GetChild("n8")
  if flag_obj then
    flag_obj.pivot = Vector2(0.5, 1)
```

---

## Abyss/AbyssExploreMgr.lua.lua
**Functions:**
- inst.args.ondestroyed
- _filter_env.callback
- fov.visibleCallback
- fov.getRadiusCallback
- fov.getPositionCallback
- Init
- InitAsync
- Release
**Snippet:**
```lua
local cameraFollow = true
local cameraFollowLerpVal = 1
local listeners, Init, InitAsync, Release
local unpack = unpack or table.unpack
local open_time_regions
local initialized, enabled, gesturable, pause = false, true, -1, 0
local delayMotion
local EXCLAM_PHASE = {
  START = 1,
  BEFORE_ANIM = 2,
```

---

## Abyss/AbyssExploreMinimapUtils.lua.lua
**Snippet:**
```lua
local WorldPositionToMapRatio = function(position)
  local referSize = AbyssExploreSettings.Map.size
  local referPosition = AbyssExploreSettings.Map.origin
  local diffx = position.x - referPosition.x
  local diffy = position.y - referPosition.y
  local x = diffx / referSize.x
  local y = diffy / referSize.y
  return x, y
end
local DEFAULT_RECT = {
```

---

## Abyss/AbyssExploreResUtils.lua.lua
**Snippet:**
```lua
local shadowScale = Vector3(0.620000005, 0.317743778, 0.620000005)
local OnSpineLoaded = function(go)
  local goTrans = go.transform
  SkeletonAnimationUtil.SetShaderEffectEnable(go, false, true, false, true)
  LuaUtil.SetOutLineColor(go, 0, 79, 149, 179, 255)
  local helper = go:GetComponent(typeof(MaterialPropertyHelper))
  helper:ChangeFloatValue("_OcclusionAlpha", 1, -1)
  helper:ChangeFloatValue("_OcclusionColorBlend", 0.64, -1)
  helper:ChangeColorValue("_OcclusionColor", Color(0.37254901960784315, 0.6509803921568628, 0.6431372549019608, 1), -1)
  helper:ChangeFloatValue("_XTilt", 0, -1)
```

---

## Abyss/AbyssExploreScriptList.lua.lua
**Requires:**
- AbyssExploreConst
- AbyssExploreMgr
- AbyssExploreChrCtrl
- AbyssExploreMapCtrl
- AbyssExploreCamCtrl
- AbyssExploreData
- AbyssExploreService
- AbyssExploreEventHandler
- AbyssExploreStoryUtils
- AbyssExploreMapflag
- AbyssExploreMinimapUtils
- AbyssExploreFramingOperation
- AbyssEventList
- AbyssExploreResUtils
**Snippet:**
```lua
require("AbyssExploreConst")
AbyssExploreMgr = require("AbyssExploreMgr")
AbyssExploreChrCtrl = require("AbyssExploreChrCtrl")
AbyssExploreMapCtrl = require("AbyssExploreMapCtrl")
AbyssExploreCamCtrl = require("AbyssExploreCamCtrl")
AbyssExploreData = require("AbyssExploreData")
AbyssExploreService = require("AbyssExploreService")
AbyssExploreEventHandler = require("AbyssExploreEventHandler")
AbyssExploreStoryUtils = require("AbyssExploreStoryUtils")
AbyssExploreMapflag = require("AbyssExploreMapflag")
```

---

## Abyss/AbyssExploreService.lua.lua
**Snippet:**
```lua
local eventsBuffer
local clear = function(arr)
  local count = #arr
  for i = 1, count do
    table.remove(arr)
  end
end
local setPlotNodeInfo = function(eventInfo)
  local step, numNodes = 0, 0
  local plotNodeId = eventInfo.plotNodeId
```

---

## Abyss/AbyssExploreStoryUtils.lua.lua
**Functions:**
- mergedlist.itemRenderer
- list.itemRenderer
- list.itemRenderer
- list.itemRenderer
- onyield
- optionList.itemRenderer
**Snippet:**
```lua
local INVALID_STORY_ID = -1
local StoryCoroutine = function(storyId)
  local story_id = tonumber(storyId or INVALID_STORY_ID)
  while type(story_id) == "number" and story_id > 0 do
    local storyData = TableData.GetConfig(story_id, "BaseStorySimple") or nil
    story_id = coroutine.yield(storyData)
  end
end
local PlayChildrenTransition = function(list, transition, specialIndex, callback, delay, reverse)
  delay = type(delay) == "number" and delay or 0
```

---

## Abyss/AbyssFunctionOpenWindow.lua.lua
**Functions:**
- AbyssFunctionOpenWindow.ReInitData
- AbyssFunctionOpenWindow.OnInit
- AbyssFunctionOpenWindow.UpdateInfo
- AbyssFunctionOpenWindow.InitBtn
- AbyssFunctionOpenWindow.OnClose
**Requires:**
- AbyssFunctionOpen_FunctionOpenWindowByName
**Snippet:**
```lua
require("AbyssFunctionOpen_FunctionOpenWindowByName")
local AbyssFunctionOpenWindow = {}
local uis, contentPane, functionId, onCloseCallback, busy, endPosition
local duration = 1.2
local TweenOutAndClose = function()
  if busy then
    return
  end
  busy = true
  local elapse = 0
```

---

## Abyss/AbyssFunctionOpen_AbyssButtonTipsByName.lua.lua
**Functions:**
- GetAbyssFunctionOpen_AbyssButtonTipsUis
**Requires:**
- CommonResource_AbyssTipsWordByName
**Snippet:**
```lua
require("CommonResource_AbyssTipsWordByName")

function GetAbyssFunctionOpen_AbyssButtonTipsUis(ui)
  local uis = {}
  uis.AbyssTipsBtn = ui:GetChild("AbyssTipsBtn")
  uis.AbyssTipsWord = GetCommonResource_AbyssTipsWordUis(ui:GetChild("AbyssTipsWord"))
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssFunctionOpen_AbyssButtonTipsWindowByName.lua.lua
**Functions:**
- GetAbyssFunctionOpen_AbyssButtonTipsWindowUis
**Requires:**
- AbyssFunctionOpen_AbyssButtonTipsByName
**Snippet:**
```lua
require("AbyssFunctionOpen_AbyssButtonTipsByName")

function GetAbyssFunctionOpen_AbyssButtonTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetAbyssFunctionOpen_AbyssButtonTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssFunctionOpen_AbyssTips1BgByName.lua.lua
**Functions:**
- GetAbyssFunctionOpen_AbyssTips1BgUis
**Snippet:**
```lua
function GetAbyssFunctionOpen_AbyssTips1BgUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssFunctionOpen_AbyssTips1ByName.lua.lua
**Functions:**
- GetAbyssFunctionOpen_AbyssTips1Uis
**Requires:**
- AbyssFunctionOpen_AbyssTips1BgByName
- AbyssFunctionOpen_TipsInfo1ByName
- AbyssFunctionOpen_TipsSignByName
**Snippet:**
```lua
require("AbyssFunctionOpen_AbyssTips1BgByName")
require("AbyssFunctionOpen_TipsInfo1ByName")
require("AbyssFunctionOpen_TipsSignByName")

function GetAbyssFunctionOpen_AbyssTips1Uis(ui)
  local uis = {}
  uis.AbyssTips1Bg = GetAbyssFunctionOpen_AbyssTips1BgUis(ui:GetChild("AbyssTips1Bg"))
  uis.TipsCloseBtn = ui:GetChild("TipsCloseBtn")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TipsInfoList = ui:GetChild("TipsInfoList")
```

---

## Abyss/AbyssFunctionOpen_AbyssTips2ByName.lua.lua
**Functions:**
- GetAbyssFunctionOpen_AbyssTips2Uis
**Requires:**
- CommonResource_PopupBgByName
- AbyssFunctionOpen_AbyssTips1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("AbyssFunctionOpen_AbyssTips1ByName")

function GetAbyssFunctionOpen_AbyssTips2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.AbyssTips1 = GetAbyssFunctionOpen_AbyssTips1Uis(ui:GetChild("AbyssTips1"))
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssFunctionOpen_AbyssTipsWindowByName.lua.lua
**Functions:**
- GetAbyssFunctionOpen_AbyssTipsWindowUis
**Requires:**
- AbyssFunctionOpen_AbyssTips2ByName
**Snippet:**
```lua
require("AbyssFunctionOpen_AbyssTips2ByName")

function GetAbyssFunctionOpen_AbyssTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetAbyssFunctionOpen_AbyssTips2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssFunctionOpen_FunctionOpen1ByName.lua.lua
**Functions:**
- GetAbyssFunctionOpen_FunctionOpen1Uis
**Snippet:**
```lua
function GetAbyssFunctionOpen_FunctionOpen1Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssFunctionOpen_FunctionOpen2ByName.lua.lua
**Functions:**
- GetAbyssFunctionOpen_FunctionOpen2Uis
**Requires:**
- AbyssFunctionOpen_PopupBgByName
- AbyssFunctionOpen_FunctionOpen1ByName
- AbyssFunctionOpen_FunctionOpenIconByName
**Snippet:**
```lua
require("AbyssFunctionOpen_PopupBgByName")
require("AbyssFunctionOpen_FunctionOpen1ByName")
require("AbyssFunctionOpen_FunctionOpenIconByName")

function GetAbyssFunctionOpen_FunctionOpen2Uis(ui)
  local uis = {}
  uis.PopupBg = GetAbyssFunctionOpen_PopupBgUis(ui:GetChild("PopupBg"))
  uis.FunctionOpen1 = GetAbyssFunctionOpen_FunctionOpen1Uis(ui:GetChild("FunctionOpen1"))
  uis.Pic = GetAbyssFunctionOpen_FunctionOpenIconUis(ui:GetChild("Pic"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
```

---

## Abyss/AbyssFunctionOpen_FunctionOpenIconByName.lua.lua
**Functions:**
- GetAbyssFunctionOpen_FunctionOpenIconUis
**Snippet:**
```lua
function GetAbyssFunctionOpen_FunctionOpenIconUis(ui)
  local uis = {}
  
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssFunctionOpen_FunctionOpenWindowByName.lua.lua
**Functions:**
- GetAbyssFunctionOpen_FunctionOpenWindowUis
**Requires:**
- AbyssFunctionOpen_FunctionOpen2ByName
**Snippet:**
```lua
require("AbyssFunctionOpen_FunctionOpen2ByName")

function GetAbyssFunctionOpen_FunctionOpenWindowUis(ui)
  local uis = {}
  uis.Main = GetAbyssFunctionOpen_FunctionOpen2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssFunctionOpen_PopupBgByName.lua.lua
**Functions:**
- GetAbyssFunctionOpen_PopupBgUis
**Snippet:**
```lua
function GetAbyssFunctionOpen_PopupBgUis(ui)
  local uis = {}
  
  uis.BlurLoader = ui:GetChild("BlurLoader")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssFunctionOpen_TipsCloseBtnByName.lua.lua
**Functions:**
- GetAbyssFunctionOpen_TipsCloseBtnUis
**Snippet:**
```lua
function GetAbyssFunctionOpen_TipsCloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssFunctionOpen_TipsGoToBtnByName.lua.lua
**Functions:**
- GetAbyssFunctionOpen_TipsGoToBtnUis
**Snippet:**
```lua
function GetAbyssFunctionOpen_TipsGoToBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssFunctionOpen_TipsInfo1ByName.lua.lua
**Functions:**
- GetAbyssFunctionOpen_TipsInfo1Uis
**Snippet:**
```lua
function GetAbyssFunctionOpen_TipsInfo1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssFunctionOpen_TipsInfoByName.lua.lua
**Functions:**
- GetAbyssFunctionOpen_TipsInfoUis
**Snippet:**
```lua
function GetAbyssFunctionOpen_TipsInfoUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssFunctionOpen_TipsLeftBtnByName.lua.lua
**Functions:**
- GetAbyssFunctionOpen_TipsLeftBtnUis
**Snippet:**
```lua
function GetAbyssFunctionOpen_TipsLeftBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssFunctionOpen_TipsRightBtnByName.lua.lua
**Functions:**
- GetAbyssFunctionOpen_TipsRightBtnUis
**Snippet:**
```lua
function GetAbyssFunctionOpen_TipsRightBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssFunctionOpen_TipsSignByName.lua.lua
**Functions:**
- GetAbyssFunctionOpen_TipsSignUis
**Snippet:**
```lua
function GetAbyssFunctionOpen_TipsSignUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssFunctionOpen_TipsSwitchByName.lua.lua
**Functions:**
- GetAbyssFunctionOpen_TipsSwitchUis
**Snippet:**
```lua
function GetAbyssFunctionOpen_TipsSwitchUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssRegionOpenWindow.lua.lua
**Functions:**
- AbyssRegionOpenWindow.ReInitData
- AbyssRegionOpenWindow.OnInit
- AbyssRegionOpenWindow.UpdateInfo
- AbyssRegionOpenWindow.InitBtn
- AbyssRegionOpenWindow.OnClose
**Requires:**
- Abyss_ActivityOpenWindowByName
**Snippet:**
```lua
require("Abyss_ActivityOpenWindowByName")
local AbyssRegionOpenWindow = {}
local uis, contentPane, unlockedRegionId

function AbyssRegionOpenWindow.ReInitData()
end

function AbyssRegionOpenWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.AbyssRegionOpenWindow.package, WinResConfig.AbyssRegionOpenWindow.comName, function(com)
    contentPane = com
```

---

## Abyss/AbyssRewardWindow.lua.lua
**Functions:**
- AbyssRewardWindow.ReInitData
- AbyssRewardWindow.OnInit
- AbyssRewardWindow.UpdateInfo
- wordlist.itemRenderer
- itemlist.itemRenderer
- AbyssRewardWindow.InitBtn
- AbyssRewardWindow.OnClose
**Requires:**
- AbyssReward_AbyssRewardWindowByName
**Snippet:**
```lua
require("AbyssReward_AbyssRewardWindowByName")
local AbyssRewardWindow = {}
local uis, contentPane

function AbyssRewardWindow.ReInitData()
end

function AbyssRewardWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.AbyssRewardWindow.package, WinResConfig.AbyssRewardWindow.comName, function(com)
    contentPane = com
```

---

## Abyss/AbyssReward_AbyssRewardByName.lua.lua
**Functions:**
- GetAbyssReward_AbyssRewardUis
**Requires:**
- CommonResource_PopupBgByName
- AbyssReward_RewardTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("AbyssReward_RewardTipsByName")

function GetAbyssReward_AbyssRewardUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.RewardTips = GetAbyssReward_RewardTipsUis(ui:GetChild("RewardTips"))
  uis.root = ui
  return uis
```

---

## Abyss/AbyssReward_AbyssRewardWindowByName.lua.lua
**Functions:**
- GetAbyssReward_AbyssRewardWindowUis
**Requires:**
- AbyssReward_AbyssRewardByName
**Snippet:**
```lua
require("AbyssReward_AbyssRewardByName")

function GetAbyssReward_AbyssRewardWindowUis(ui)
  local uis = {}
  uis.Main = GetAbyssReward_AbyssRewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssReward_CompleteByName.lua.lua
**Functions:**
- GetAbyssReward_CompleteUis
**Snippet:**
```lua
function GetAbyssReward_CompleteUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssReward_LockByName.lua.lua
**Functions:**
- GetAbyssReward_LockUis
**Snippet:**
```lua
function GetAbyssReward_LockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssReward_RewardTipsByName.lua.lua
**Functions:**
- GetAbyssReward_RewardTipsUis
**Requires:**
- AbyssReward_LockByName
- AbyssReward_CompleteByName
**Snippet:**
```lua
require("AbyssReward_LockByName")
require("AbyssReward_CompleteByName")

function GetAbyssReward_RewardTipsUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.RewardTxt = ui:GetChild("RewardTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.Lock = GetAbyssReward_LockUis(ui:GetChild("Lock"))
  uis.GetBtn = ui:GetChild("GetBtn")
```

---

## Abyss/AbyssReward_WordByName.lua.lua
**Functions:**
- GetAbyssReward_WordUis
**Snippet:**
```lua
function GetAbyssReward_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/AbyssShopWindow.lua.lua
**Functions:**
- AbyssShopWindow.ReInitData
- AbyssShopWindow.OnInit
- itemlist.itemProvider
- itemlist.itemRenderer
- list.itemRenderer
- itemlist.itemRenderer
- selllist.itemRenderer
- pricelist.itemRenderer
- tablist.itemRenderer
- msg_box_sureBtnParam.touchCallback
- shop.LeftTab.LeftTabList.itemRenderer
- AbyssShopWindow.UpdateInfo
- AbyssShopWindow.InitBtn
- AbyssShopWindow.OnShown
- AbyssShopWindow.OnHide
- AbyssShopWindow.OnClose
- AbyssShopWindow.HandleMessage
**Requires:**
- Abyss_ShopWindowByName
- Abyss_ShopEnterAniByName
**Snippet:**
```lua
require("Abyss_ShopWindowByName")
require("Abyss_ShopEnterAniByName")
local AbyssShopWindow = {}
local uis, contentPane
local ShopType = {
  AbyssPeriodicShop = 3,
  AbyssNormalShop = 4,
  AbyssBourse = 999,
  AbyssSeal = 5,
  AbyssExtend = 6
```

---

## Abyss/AbyssTipsWindow.lua.lua
**Functions:**
- AbyssTipsWindow.ReInitData
- AbyssTipsWindow.OnInit
- AbyssTipsWindow.UpdateInfo
- AbyssTipsWindow.ShowInfo
- AbyssTipsWindow.ChangeInfo
- tips.TipsInfoList.itemRenderer
- tips.TipsSwitchList.itemRenderer
- AbyssTipsWindow.CloseWindow
- AbyssTipsWindow.InitBtn
- AbyssTipsWindow.OnClose
**Requires:**
- AbyssFunctionOpen_AbyssTipsWindowByName
**Snippet:**
```lua
require("AbyssFunctionOpen_AbyssTipsWindowByName")
local AbyssTipsWindow = {}
local uis, contentPane, isAbyss, openId, rookieFinished
local sortTb = {}
local pageIndex

function AbyssTipsWindow.ReInitData()
end

function AbyssTipsWindow.OnInit(bridgeObj)
```

---

## Abyss/AbyssWindow.lua.lua
**Functions:**
- stateList.itemRenderer
- list.itemProvider
- list.itemRenderer
- AbyssWindow.ReInitData
- AbyssWindow.OnInit
- AbyssWindow.UpdateInfo
- AbyssWindow.InitBtn
- AbyssWindow.OnShown
- AbyssWindow.OnHide
- AbyssWindow.OnClose
- AbyssWindow.HandleMessage
**Requires:**
- Abyss_AbyssWindowByName
- Abyss_CardTaskByName
**Snippet:**
```lua
require("Abyss_AbyssWindowByName")
require("Abyss_CardTaskByName")
local AbyssWindow = {}
local uis, contentPane, branchesCache, activitiesCache, focusCache, minimap, fowMask, mapflags, playerflag, flagscale, cursors, cursorRoot, eventOverlapsCollection, softMask, eventTipsRoot, eventsBuffer, tipsVersion
local enablePopupEventTips, eventTipsVisible = false, true
local unlockedFunctions
local FuncList = {
  [FEATURE_ENUM.ABYSS_FUNC_INDEX] = {
    id = FEATURE_ENUM.ABYSS_FUNC_INDEX,
    sort = 1,
```

---

## Abyss/Abyss_AbyssByName.lua.lua
**Functions:**
- GetAbyss_AbyssUis
**Requires:**
- CommonResource_BackGroundByName
- Abyss_PlayerInfoByName
- Abyss_SmallMapRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Abyss_PlayerInfoByName")
require("Abyss_SmallMapRegionByName")

function GetAbyss_AbyssUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.PlayerInfo = GetAbyss_PlayerInfoUis(ui:GetChild("PlayerInfo"))
  uis.ExplainBtn = ui:GetChild("ExplainBtn")
  uis.CardSwitchBtn = ui:GetChild("CardSwitchBtn")
```

---

## Abyss/Abyss_AbyssWindowByName.lua.lua
**Functions:**
- GetAbyss_AbyssWindowUis
**Requires:**
- Abyss_AbyssByName
**Snippet:**
```lua
require("Abyss_AbyssByName")

function GetAbyss_AbyssWindowUis(ui)
  local uis = {}
  uis.Main = GetAbyss_AbyssUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ActionValueByName.lua.lua
**Functions:**
- GetAbyss_ActionValueUis
**Snippet:**
```lua
function GetAbyss_ActionValueUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ActionValueTipsByName.lua.lua
**Functions:**
- GetAbyss_ActionValueTipsUis
**Snippet:**
```lua
function GetAbyss_ActionValueTipsUis(ui)
  local uis = {}
  
  uis.AllTimeTxt = ui:GetChild("AllTimeTxt")
  uis.NextTimeTxt = ui:GetChild("NextTimeTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ActivityBtnByName.lua.lua
**Functions:**
- GetAbyss_ActivityBtnUis
**Requires:**
- CommonResource_AbyssSign2ByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_AbyssSign2ByName")
require("CommonResource_RedDotByName")

function GetAbyss_ActivityBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.AbyssSign = GetCommonResource_AbyssSign2Uis(ui:GetChild("AbyssSign"))
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
```

---

## Abyss/Abyss_ActivityByName.lua.lua
**Functions:**
- GetAbyss_ActivityUis
**Requires:**
- CommonResource_PopupBgByName
- Abyss_ActivityTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Abyss_ActivityTipsByName")

function GetAbyss_ActivityUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.ActivityTips = GetAbyss_ActivityTipsUis(ui:GetChild("ActivityTips"))
  uis.root = ui
  return uis
```

---

## Abyss/Abyss_ActivityCloseBtnByName.lua.lua
**Functions:**
- GetAbyss_ActivityCloseBtnUis
**Snippet:**
```lua
function GetAbyss_ActivityCloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ActivityOpen1ByName.lua.lua
**Functions:**
- GetAbyss_ActivityOpen1Uis
**Snippet:**
```lua
function GetAbyss_ActivityOpen1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ActivityOpen2ByName.lua.lua
**Functions:**
- GetAbyss_ActivityOpen2Uis
**Requires:**
- CommonResource_PopupBgByName
- Abyss_ActivityOpenBgByName
- Abyss_ActivityOpen1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Abyss_ActivityOpenBgByName")
require("Abyss_ActivityOpen1ByName")

function GetAbyss_ActivityOpen2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.ActivityOpenBg = GetAbyss_ActivityOpenBgUis(ui:GetChild("ActivityOpenBg"))
  uis.Currency1 = GetAbyss_ActivityOpen1Uis(ui:GetChild("Currency1"))
```

---

## Abyss/Abyss_ActivityOpenBgByName.lua.lua
**Functions:**
- GetAbyss_ActivityOpenBgUis
**Snippet:**
```lua
function GetAbyss_ActivityOpenBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ActivityOpenWindowByName.lua.lua
**Functions:**
- GetAbyss_ActivityOpenWindowUis
**Requires:**
- Abyss_ActivityOpen2ByName
**Snippet:**
```lua
require("Abyss_ActivityOpen2ByName")

function GetAbyss_ActivityOpenWindowUis(ui)
  local uis = {}
  uis.Main = GetAbyss_ActivityOpen2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ActivityTabBgByName.lua.lua
**Functions:**
- GetAbyss_ActivityTabBgUis
**Snippet:**
```lua
function GetAbyss_ActivityTabBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ActivityTabBtnByName.lua.lua
**Functions:**
- GetAbyss_ActivityTabBtnUis
**Requires:**
- Abyss_ActivityTabBgByName
- CommonResource_RedDotByName
- CommonResource_AbyssSign1ByName
- CommonResource_AbyssSign4ByName
**Snippet:**
```lua
require("Abyss_ActivityTabBgByName")
require("CommonResource_RedDotByName")
require("CommonResource_AbyssSign1ByName")
require("CommonResource_AbyssSign4ByName")

function GetAbyss_ActivityTabBtnUis(ui)
  local uis = {}
  uis.ActivityTabBg = GetAbyss_ActivityTabBgUis(ui:GetChild("ActivityTabBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
```

---

## Abyss/Abyss_ActivityTipsByName.lua.lua
**Functions:**
- GetAbyss_ActivityTipsUis
**Requires:**
- Abyss_BossRegionByName
- Abyss_ExpeditionRegionByName
- Abyss_BuildRegionByName
- Abyss_BoxRegionByName
- Abyss_RogueRegionByName
- Abyss_SuperRegionByName
- Abyss_ExploreRegionByName
- Abyss_ExploreDungeonRegionByName
**Snippet:**
```lua
require("Abyss_BossRegionByName")
require("Abyss_ExpeditionRegionByName")
require("Abyss_BuildRegionByName")
require("Abyss_BoxRegionByName")
require("Abyss_RogueRegionByName")
require("Abyss_SuperRegionByName")
require("Abyss_ExploreRegionByName")
require("Abyss_ExploreDungeonRegionByName")

function GetAbyss_ActivityTipsUis(ui)
```

---

## Abyss/Abyss_ActivityTitleBtnByName.lua.lua
**Functions:**
- GetAbyss_ActivityTitleBtnUis
**Snippet:**
```lua
function GetAbyss_ActivityTitleBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ActivityWindowByName.lua.lua
**Functions:**
- GetAbyss_ActivityWindowUis
**Requires:**
- Abyss_ActivityByName
**Snippet:**
```lua
require("Abyss_ActivityByName")

function GetAbyss_ActivityWindowUis(ui)
  local uis = {}
  uis.Main = GetAbyss_ActivityUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_AllEventByName.lua.lua
**Functions:**
- GetAbyss_AllEventUis
**Requires:**
- Abyss_EventChoiceByName
**Snippet:**
```lua
require("Abyss_EventChoiceByName")

function GetAbyss_AllEventUis(ui)
  local uis = {}
  uis.EventChoice = GetAbyss_EventChoiceUis(ui:GetChild("EventChoice"))
  uis.PlayerBtn = ui:GetChild("PlayerBtn")
  uis.GuideboardBtn = ui:GetChild("GuideboardBtn")
  uis.ItemBtn = ui:GetChild("ItemBtn")
  uis.PlotBtn = ui:GetChild("PlotBtn")
  uis.BuildingBtn = ui:GetChild("BuildingBtn")
```

---

## Abyss/Abyss_AllPutBtnByName.lua.lua
**Functions:**
- GetAbyss_AllPutBtnUis
**Snippet:**
```lua
function GetAbyss_AllPutBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_Area1ByName.lua.lua
**Functions:**
- GetAbyss_Area1Uis
**Requires:**
- Abyss_AreaTitleByName
**Snippet:**
```lua
require("Abyss_AreaTitleByName")

function GetAbyss_Area1Uis(ui)
  local uis = {}
  uis.AreaTitle = GetAbyss_AreaTitleUis(ui:GetChild("AreaTitle"))
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_Area2ByName.lua.lua
**Functions:**
- GetAbyss_Area2Uis
**Requires:**
- Abyss_AreaTitleByName
**Snippet:**
```lua
require("Abyss_AreaTitleByName")

function GetAbyss_Area2Uis(ui)
  local uis = {}
  uis.AreaTitle = GetAbyss_AreaTitleUis(ui:GetChild("AreaTitle"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_Area3ByName.lua.lua
**Functions:**
- GetAbyss_Area3Uis
**Requires:**
- Abyss_AreaTitleByName
**Snippet:**
```lua
require("Abyss_AreaTitleByName")

function GetAbyss_Area3Uis(ui)
  local uis = {}
  uis.AreaTitle = GetAbyss_AreaTitleUis(ui:GetChild("AreaTitle"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_Area4ByName.lua.lua
**Functions:**
- GetAbyss_Area4Uis
**Requires:**
- Abyss_AreaTitleByName
**Snippet:**
```lua
require("Abyss_AreaTitleByName")

function GetAbyss_Area4Uis(ui)
  local uis = {}
  uis.AreaTitle = GetAbyss_AreaTitleUis(ui:GetChild("AreaTitle"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_Area5ByName.lua.lua
**Functions:**
- GetAbyss_Area5Uis
**Requires:**
- Abyss_AreaTitleByName
**Snippet:**
```lua
require("Abyss_AreaTitleByName")

function GetAbyss_Area5Uis(ui)
  local uis = {}
  uis.AreaTitle = GetAbyss_AreaTitleUis(ui:GetChild("AreaTitle"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_Area6ByName.lua.lua
**Functions:**
- GetAbyss_Area6Uis
**Requires:**
- Abyss_AreaTitleByName
**Snippet:**
```lua
require("Abyss_AreaTitleByName")

function GetAbyss_Area6Uis(ui)
  local uis = {}
  uis.AreaTitle = GetAbyss_AreaTitleUis(ui:GetChild("AreaTitle"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_Area7ByName.lua.lua
**Functions:**
- GetAbyss_Area7Uis
**Requires:**
- Abyss_AreaTitleByName
**Snippet:**
```lua
require("Abyss_AreaTitleByName")

function GetAbyss_Area7Uis(ui)
  local uis = {}
  uis.AreaTitle = GetAbyss_AreaTitleUis(ui:GetChild("AreaTitle"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_Area8ByName.lua.lua
**Functions:**
- GetAbyss_Area8Uis
**Requires:**
- Abyss_AreaTitleByName
**Snippet:**
```lua
require("Abyss_AreaTitleByName")

function GetAbyss_Area8Uis(ui)
  local uis = {}
  uis.AreaTitle = GetAbyss_AreaTitleUis(ui:GetChild("AreaTitle"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_AreaTitleByName.lua.lua
**Functions:**
- GetAbyss_AreaTitleUis
**Snippet:**
```lua
function GetAbyss_AreaTitleUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ArrowByName.lua.lua
**Functions:**
- GetAbyss_ArrowUis
**Snippet:**
```lua
function GetAbyss_ArrowUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BadgeBtnByName.lua.lua
**Functions:**
- GetAbyss_BadgeBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetAbyss_BadgeBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
```

---

## Abyss/Abyss_BatteryProgressBarByName.lua.lua
**Functions:**
- GetAbyss_BatteryProgressBarUis
**Requires:**
- Abyss_BatteryProgressFillByName
**Snippet:**
```lua
require("Abyss_BatteryProgressFillByName")

function GetAbyss_BatteryProgressBarUis(ui)
  local uis = {}
  uis.bar = GetAbyss_BatteryProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BatteryProgressFillByName.lua.lua
**Functions:**
- GetAbyss_BatteryProgressFillUis
**Snippet:**
```lua
function GetAbyss_BatteryProgressFillUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BigMapByName.lua.lua
**Functions:**
- GetAbyss_BigMapUis
**Requires:**
- CommonResource_BackGroundByName
- Abyss_BigMapPicDragByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Abyss_BigMapPicDragByName")

function GetAbyss_BigMapUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BigMapPicDrag = GetAbyss_BigMapPicDragUis(ui:GetChild("BigMapPicDrag"))
  uis.MapCloseBtn = ui:GetChild("MapCloseBtn")
  uis.BigMapResetBtn = ui:GetChild("BigMapResetBtn")
  uis.root = ui
```

---

## Abyss/Abyss_BigMapEventPicByName.lua.lua
**Functions:**
- GetAbyss_BigMapEventPicUis
**Snippet:**
```lua
function GetAbyss_BigMapEventPicUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BigMapPic1ByName.lua.lua
**Functions:**
- GetAbyss_BigMapPic1Uis
**Snippet:**
```lua
function GetAbyss_BigMapPic1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BigMapPicByName.lua.lua
**Functions:**
- GetAbyss_BigMapPicUis
**Requires:**
- Abyss_BigMapPic1ByName
**Snippet:**
```lua
require("Abyss_BigMapPic1ByName")

function GetAbyss_BigMapPicUis(ui)
  local uis = {}
  uis.BigMapPic1 = GetAbyss_BigMapPic1Uis(ui:GetChild("BigMapPic1"))
  uis.FogHolder = ui:GetChild("FogHolder")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BigMapPicDragByName.lua.lua
**Functions:**
- GetAbyss_BigMapPicDragUis
**Requires:**
- Abyss_BigMapPicByName
- Abyss_Area1ByName
- Abyss_Area2ByName
- Abyss_Area3ByName
- Abyss_Area4ByName
- Abyss_Area5ByName
- Abyss_Area6ByName
- Abyss_Area7ByName
- Abyss_Area8ByName
- Abyss_BigMapEventPicByName
**Snippet:**
```lua
require("Abyss_BigMapPicByName")
require("Abyss_Area1ByName")
require("Abyss_Area2ByName")
require("Abyss_Area3ByName")
require("Abyss_Area4ByName")
require("Abyss_Area5ByName")
require("Abyss_Area6ByName")
require("Abyss_Area7ByName")
require("Abyss_Area8ByName")
require("Abyss_BigMapEventPicByName")
```

---

## Abyss/Abyss_BigMapResetBtnByName.lua.lua
**Functions:**
- GetAbyss_BigMapResetBtnUis
**Snippet:**
```lua
function GetAbyss_BigMapResetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BigMapWindowByName.lua.lua
**Functions:**
- GetAbyss_BigMapWindowUis
**Requires:**
- Abyss_BigMapByName
**Snippet:**
```lua
require("Abyss_BigMapByName")

function GetAbyss_BigMapWindowUis(ui)
  local uis = {}
  uis.Main = GetAbyss_BigMapUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BossBattleBtnByName.lua.lua
**Functions:**
- GetAbyss_BossBattleBtnUis
**Snippet:**
```lua
function GetAbyss_BossBattleBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BossRegionByName.lua.lua
**Functions:**
- GetAbyss_BossRegionUis
**Requires:**
- Abyss_BossTopInfoByName
- Abyss_BossTipsTitleByName
**Snippet:**
```lua
require("Abyss_BossTopInfoByName")
require("Abyss_BossTipsTitleByName")

function GetAbyss_BossRegionUis(ui)
  local uis = {}
  uis.BossTopInfo = GetAbyss_BossTopInfoUis(ui:GetChild("BossTopInfo"))
  uis.Title = GetAbyss_BossTipsTitleUis(ui:GetChild("Title"))
  uis.TabList = ui:GetChild("TabList")
  uis.TipsList = ui:GetChild("TipsList")
  uis.root = ui
```

---

## Abyss/Abyss_BossTipsAniByName.lua.lua
**Functions:**
- GetAbyss_BossTipsAniUis
**Requires:**
- Abyss_BossTipsByName
**Snippet:**
```lua
require("Abyss_BossTipsByName")

function GetAbyss_BossTipsAniUis(ui)
  local uis = {}
  uis.BossTips = GetAbyss_BossTipsUis(ui:GetChild("BossTips"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BossTipsByName.lua.lua
**Functions:**
- GetAbyss_BossTipsUis
**Requires:**
- Abyss_BossTipsDifficultyByName
- Abyss_BossTipsLock1ByName
- Abyss_BossTipsSpendByName
**Snippet:**
```lua
require("Abyss_BossTipsDifficultyByName")
require("Abyss_BossTipsLock1ByName")
require("Abyss_BossTipsSpendByName")

function GetAbyss_BossTipsUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.RewardList = ui:GetChild("RewardList")
  uis.Difficulty = GetAbyss_BossTipsDifficultyUis(ui:GetChild("Difficulty"))
```

---

## Abyss/Abyss_BossTipsDifficultyByName.lua.lua
**Functions:**
- GetAbyss_BossTipsDifficultyUis
**Snippet:**
```lua
function GetAbyss_BossTipsDifficultyUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BossTipsGoBtnByName.lua.lua
**Functions:**
- GetAbyss_BossTipsGoBtnUis
**Snippet:**
```lua
function GetAbyss_BossTipsGoBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BossTipsLock1ByName.lua.lua
**Functions:**
- GetAbyss_BossTipsLock1Uis
**Snippet:**
```lua
function GetAbyss_BossTipsLock1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BossTipsLockByName.lua.lua
**Functions:**
- GetAbyss_BossTipsLockUis
**Snippet:**
```lua
function GetAbyss_BossTipsLockUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BossTipsReward1ByName.lua.lua
**Functions:**
- GetAbyss_BossTipsReward1Uis
**Snippet:**
```lua
function GetAbyss_BossTipsReward1Uis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BossTipsSpendByName.lua.lua
**Functions:**
- GetAbyss_BossTipsSpendUis
**Snippet:**
```lua
function GetAbyss_BossTipsSpendUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BossTipsTitleByName.lua.lua
**Functions:**
- GetAbyss_BossTipsTitleUis
**Requires:**
- Abyss_BossTipsLockByName
**Snippet:**
```lua
require("Abyss_BossTipsLockByName")

function GetAbyss_BossTipsTitleUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Lock = GetAbyss_BossTipsLockUis(ui:GetChild("Lock"))
  uis.BoBtn = ui:GetChild("BoBtn")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Abyss/Abyss_BossTopInfo2_2BtnByName.lua.lua
**Functions:**
- GetAbyss_BossTopInfo2_2BtnUis
**Snippet:**
```lua
function GetAbyss_BossTopInfo2_2BtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BossTopInfoByName.lua.lua
**Functions:**
- GetAbyss_BossTopInfoUis
**Snippet:**
```lua
function GetAbyss_BossTopInfoUis(ui)
  local uis = {}
  
  uis.Info2Btn = ui:GetChild("Info2Btn")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BoxRegionByName.lua.lua
**Functions:**
- GetAbyss_BoxRegionUis
**Requires:**
- Abyss_BoxTopInfoByName
**Snippet:**
```lua
require("Abyss_BoxTopInfoByName")

function GetAbyss_BoxRegionUis(ui)
  local uis = {}
  uis.BoxTopInfo = GetAbyss_BoxTopInfoUis(ui:GetChild("BoxTopInfo"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BoxTabBgByName.lua.lua
**Functions:**
- GetAbyss_BoxTabBgUis
**Snippet:**
```lua
function GetAbyss_BoxTabBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BoxTabBtnByName.lua.lua
**Functions:**
- GetAbyss_BoxTabBtnUis
**Requires:**
- Abyss_BoxTabBgByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("Abyss_BoxTabBgByName")
require("CommonResource_RedDotByName")

function GetAbyss_BoxTabBtnUis(ui)
  local uis = {}
  uis.ActivityTabBg = GetAbyss_BoxTabBgUis(ui:GetChild("ActivityTabBg"))
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Abyss/Abyss_BoxTipsAniByName.lua.lua
**Functions:**
- GetAbyss_BoxTipsAniUis
**Requires:**
- Abyss_BoxTipsByName
**Snippet:**
```lua
require("Abyss_BoxTipsByName")

function GetAbyss_BoxTipsAniUis(ui)
  local uis = {}
  uis.BoxTips = GetAbyss_BoxTipsUis(ui:GetChild("BoxTips"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BoxTipsByName.lua.lua
**Functions:**
- GetAbyss_BoxTipsUis
**Requires:**
- Abyss_BoxTipsResetByName
- Abyss_BoxTipsInfo1ByName
- Abyss_BoxTipsInfo2ByName
- Abyss_BoxTipsInfo3ByName
- Abyss_BoxTipsLockByName
**Snippet:**
```lua
require("Abyss_BoxTipsResetByName")
require("Abyss_BoxTipsInfo1ByName")
require("Abyss_BoxTipsInfo2ByName")
require("Abyss_BoxTipsInfo3ByName")
require("Abyss_BoxTipsLockByName")

function GetAbyss_BoxTipsUis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
```

---

## Abyss/Abyss_BoxTipsGoBtnByName.lua.lua
**Functions:**
- GetAbyss_BoxTipsGoBtnUis
**Snippet:**
```lua
function GetAbyss_BoxTipsGoBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BoxTipsInfo1ByName.lua.lua
**Functions:**
- GetAbyss_BoxTipsInfo1Uis
**Snippet:**
```lua
function GetAbyss_BoxTipsInfo1Uis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BoxTipsInfo2ByName.lua.lua
**Functions:**
- GetAbyss_BoxTipsInfo2Uis
**Snippet:**
```lua
function GetAbyss_BoxTipsInfo2Uis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BoxTipsInfo3BgByName.lua.lua
**Functions:**
- GetAbyss_BoxTipsInfo3BgUis
**Snippet:**
```lua
function GetAbyss_BoxTipsInfo3BgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BoxTipsInfo3ByName.lua.lua
**Functions:**
- GetAbyss_BoxTipsInfo3Uis
**Requires:**
- Abyss_BoxTipsInfo3BgByName
**Snippet:**
```lua
require("Abyss_BoxTipsInfo3BgByName")

function GetAbyss_BoxTipsInfo3Uis(ui)
  local uis = {}
  uis.BoxTipsInfo3Bg = GetAbyss_BoxTipsInfo3BgUis(ui:GetChild("BoxTipsInfo3Bg"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BoxTipsLockByName.lua.lua
**Functions:**
- GetAbyss_BoxTipsLockUis
**Snippet:**
```lua
function GetAbyss_BoxTipsLockUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BoxTipsResetByName.lua.lua
**Functions:**
- GetAbyss_BoxTipsResetUis
**Snippet:**
```lua
function GetAbyss_BoxTipsResetUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BoxTopInfo1ByName.lua.lua
**Functions:**
- GetAbyss_BoxTopInfo1Uis
**Snippet:**
```lua
function GetAbyss_BoxTopInfo1Uis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BoxTopInfoByName.lua.lua
**Functions:**
- GetAbyss_BoxTopInfoUis
**Requires:**
- Abyss_BoxTopInfo1ByName
**Snippet:**
```lua
require("Abyss_BoxTopInfo1ByName")

function GetAbyss_BoxTopInfoUis(ui)
  local uis = {}
  uis.BuildTopInfo1 = GetAbyss_BoxTopInfo1Uis(ui:GetChild("BuildTopInfo1"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BuildingBtnByName.lua.lua
**Functions:**
- GetAbyss_BuildingBtnUis
**Snippet:**
```lua
function GetAbyss_BuildingBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BuildRegionByName.lua.lua
**Functions:**
- GetAbyss_BuildRegionUis
**Requires:**
- Abyss_BuildTopInfoByName
- Abyss_BuildTipsEndByName
- Abyss_BuildTipsLockByName
**Snippet:**
```lua
require("Abyss_BuildTopInfoByName")
require("Abyss_BuildTipsEndByName")
require("Abyss_BuildTipsLockByName")

function GetAbyss_BuildRegionUis(ui)
  local uis = {}
  uis.BuildTopInfo = GetAbyss_BuildTopInfoUis(ui:GetChild("BuildTopInfo"))
  uis.ProgressList = ui:GetChild("ProgressList")
  uis.GoBtn = ui:GetChild("GoBtn")
  uis.RewardBtn = ui:GetChild("RewardBtn")
```

---

## Abyss/Abyss_BuildTipsAniByName.lua.lua
**Functions:**
- GetAbyss_BuildTipsAniUis
**Requires:**
- Abyss_BuildTipsByName
**Snippet:**
```lua
require("Abyss_BuildTipsByName")

function GetAbyss_BuildTipsAniUis(ui)
  local uis = {}
  uis.BuildTips = GetAbyss_BuildTipsUis(ui:GetChild("BuildTips"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BuildTipsByName.lua.lua
**Functions:**
- GetAbyss_BuildTipsUis
**Requires:**
- Abyss_Super_ProgressLockByName
**Snippet:**
```lua
require("Abyss_Super_ProgressLockByName")

function GetAbyss_BuildTipsUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Lock = GetAbyss_Super_ProgressLockUis(ui:GetChild("Lock"))
  uis.IconList = ui:GetChild("IconList")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Abyss/Abyss_BuildTipsEndByName.lua.lua
**Functions:**
- GetAbyss_BuildTipsEndUis
**Snippet:**
```lua
function GetAbyss_BuildTipsEndUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BuildTipsGoBtnByName.lua.lua
**Functions:**
- GetAbyss_BuildTipsGoBtnUis
**Snippet:**
```lua
function GetAbyss_BuildTipsGoBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BuildTipsLockByName.lua.lua
**Functions:**
- GetAbyss_BuildTipsLockUis
**Snippet:**
```lua
function GetAbyss_BuildTipsLockUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BuildTipsOpenByName.lua.lua
**Functions:**
- GetAbyss_BuildTipsOpenUis
**Snippet:**
```lua
function GetAbyss_BuildTipsOpenUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BuildTipsProgressByName.lua.lua
**Functions:**
- GetAbyss_BuildTipsProgressUis
**Snippet:**
```lua
function GetAbyss_BuildTipsProgressUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.IconList = ui:GetChild("IconList")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BuildTipsProgressIconByName.lua.lua
**Functions:**
- GetAbyss_BuildTipsProgressIconUis
**Snippet:**
```lua
function GetAbyss_BuildTipsProgressIconUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BuildTipsRewardBtnByName.lua.lua
**Functions:**
- GetAbyss_BuildTipsRewardBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetAbyss_BuildTipsRewardBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BuildTipsState1ByName.lua.lua
**Functions:**
- GetAbyss_BuildTipsState1Uis
**Snippet:**
```lua
function GetAbyss_BuildTipsState1Uis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BuildTipsState2ByName.lua.lua
**Functions:**
- GetAbyss_BuildTipsState2Uis
**Snippet:**
```lua
function GetAbyss_BuildTipsState2Uis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BuildTipsState3ByName.lua.lua
**Functions:**
- GetAbyss_BuildTipsState3Uis
**Snippet:**
```lua
function GetAbyss_BuildTipsState3Uis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BuildTopInfo1ByName.lua.lua
**Functions:**
- GetAbyss_BuildTopInfo1Uis
**Snippet:**
```lua
function GetAbyss_BuildTopInfo1Uis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_BuildTopInfoByName.lua.lua
**Functions:**
- GetAbyss_BuildTopInfoUis
**Snippet:**
```lua
function GetAbyss_BuildTopInfoUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardHeadPicByName.lua.lua
**Functions:**
- GetAbyss_CardHeadPicUis
**Snippet:**
```lua
function GetAbyss_CardHeadPicUis(ui)
  local uis = {}
  
  uis.CardLoader = ui:GetChild("CardLoader")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardPlotBtnByName.lua.lua
**Functions:**
- GetAbyss_CardPlotBtnUis
**Snippet:**
```lua
function GetAbyss_CardPlotBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
```

---

## Abyss/Abyss_CardPlotDetailsByName.lua.lua
**Functions:**
- GetAbyss_CardPlotDetailsUis
**Requires:**
- Abyss_DetailsTipsTitleAniByName
**Snippet:**
```lua
require("Abyss_DetailsTipsTitleAniByName")

function GetAbyss_CardPlotDetailsUis(ui)
  local uis = {}
  uis.TipsList = ui:GetChild("TipsList")
  uis.DetailsTipsTitleAni = GetAbyss_DetailsTipsTitleAniUis(ui:GetChild("DetailsTipsTitleAni"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardPlotDetailsWindowByName.lua.lua
**Functions:**
- GetAbyss_CardPlotDetailsWindowUis
**Requires:**
- Abyss_CardPlotDetailsByName
**Snippet:**
```lua
require("Abyss_CardPlotDetailsByName")

function GetAbyss_CardPlotDetailsWindowUis(ui)
  local uis = {}
  uis.Main = GetAbyss_CardPlotDetailsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardPlotListByName.lua.lua
**Functions:**
- GetAbyss_CardPlotListUis
**Requires:**
- CommonResource_BackGroundByName
- Abyss_CardPlotListRegionByName
- Abyss_CardPlotDetailsByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Abyss_CardPlotListRegionByName")
require("Abyss_CardPlotDetailsByName")
require("CommonResource_CurrencyReturnByName")

function GetAbyss_CardPlotListUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.CardPlotListRegion = GetAbyss_CardPlotListRegionUis(ui:GetChild("CardPlotListRegion"))
  uis.CardPlotDetails = GetAbyss_CardPlotDetailsUis(ui:GetChild("CardPlotDetails"))
```

---

## Abyss/Abyss_CardPlotListRegionByName.lua.lua
**Functions:**
- GetAbyss_CardPlotListRegionUis
**Snippet:**
```lua
function GetAbyss_CardPlotListRegionUis(ui)
  local uis = {}
  
  uis.TypeList = ui:GetChild("TypeList")
  uis.CardAList = ui:GetChild("CardAList")
  uis.CardBList = ui:GetChild("CardBList")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Abyss/Abyss_CardPlotListTips1ByName.lua.lua
**Functions:**
- GetAbyss_CardPlotListTips1Uis
**Requires:**
- Abyss_CardPlotListTipsHeadByName
**Snippet:**
```lua
require("Abyss_CardPlotListTipsHeadByName")

function GetAbyss_CardPlotListTips1Uis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.Head = GetAbyss_CardPlotListTipsHeadUis(ui:GetChild("Head"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Abyss/Abyss_CardPlotListTipsAni1ByName.lua.lua
**Functions:**
- GetAbyss_CardPlotListTipsAni1Uis
**Requires:**
- Abyss_CardPlotListTips1ByName
**Snippet:**
```lua
require("Abyss_CardPlotListTips1ByName")

function GetAbyss_CardPlotListTipsAni1Uis(ui)
  local uis = {}
  uis.CardPlotListTips = GetAbyss_CardPlotListTips1Uis(ui:GetChild("CardPlotListTips"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardPlotListTipsAniByName.lua.lua
**Functions:**
- GetAbyss_CardPlotListTipsAniUis
**Requires:**
- Abyss_CardPlotListTipsByName
**Snippet:**
```lua
require("Abyss_CardPlotListTipsByName")

function GetAbyss_CardPlotListTipsAniUis(ui)
  local uis = {}
  uis.CardPlotListTips = GetAbyss_CardPlotListTipsUis(ui:GetChild("CardPlotListTips"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardPlotListTipsByName.lua.lua
**Functions:**
- GetAbyss_CardPlotListTipsUis
**Requires:**
- Abyss_CardPlotListTipsHeadByName
- Abyss_CardPlotProgressByName
**Snippet:**
```lua
require("Abyss_CardPlotListTipsHeadByName")
require("Abyss_CardPlotProgressByName")

function GetAbyss_CardPlotListTipsUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.PicHolder = ui:GetChild("PicHolder")
  uis.Head = GetAbyss_CardPlotListTipsHeadUis(ui:GetChild("Head"))
  uis.Progress = GetAbyss_CardPlotProgressUis(ui:GetChild("Progress"))
  uis.ScheduleList = ui:GetChild("ScheduleList")
```

---

## Abyss/Abyss_CardPlotListTipsHeadBgByName.lua.lua
**Functions:**
- GetAbyss_CardPlotListTipsHeadBgUis
**Snippet:**
```lua
function GetAbyss_CardPlotListTipsHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardPlotListTipsHeadByName.lua.lua
**Functions:**
- GetAbyss_CardPlotListTipsHeadUis
**Requires:**
- Abyss_CardPlotListTipsHeadBgByName
**Snippet:**
```lua
require("Abyss_CardPlotListTipsHeadBgByName")

function GetAbyss_CardPlotListTipsHeadUis(ui)
  local uis = {}
  uis.HeadBg = GetAbyss_CardPlotListTipsHeadBgUis(ui:GetChild("HeadBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardPlotListTipsOpenBtnByName.lua.lua
**Functions:**
- GetAbyss_CardPlotListTipsOpenBtnUis
**Snippet:**
```lua
function GetAbyss_CardPlotListTipsOpenBtnUis(ui)
  local uis = {}
  
  uis.ChapterTxt = ui:GetChild("ChapterTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardPlotListTipstypeByName.lua.lua
**Functions:**
- GetAbyss_CardPlotListTipstypeUis
**Snippet:**
```lua
function GetAbyss_CardPlotListTipstypeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardPlotListTitleByName.lua.lua
**Functions:**
- GetAbyss_CardPlotListTitleUis
**Requires:**
- Abyss_CardPlotListTitleName1ByName
- Abyss_CardPlotListTitleName2ByName
- Abyss_CardPlotListTitleName4ByName
**Snippet:**
```lua
require("Abyss_CardPlotListTitleName1ByName")
require("Abyss_CardPlotListTitleName2ByName")
require("Abyss_CardPlotListTitleName4ByName")

function GetAbyss_CardPlotListTitleUis(ui)
  local uis = {}
  uis.Title = GetAbyss_CardPlotListTitleName1Uis(ui:GetChild("Title"))
  uis.Name = GetAbyss_CardPlotListTitleName2Uis(ui:GetChild("Name"))
  uis.CardName = GetAbyss_CardPlotListTitleName4Uis(ui:GetChild("CardName"))
  uis.ChapterList = ui:GetChild("ChapterList")
```

---

## Abyss/Abyss_CardPlotListTitleName1ByName.lua.lua
**Functions:**
- GetAbyss_CardPlotListTitleName1Uis
**Snippet:**
```lua
function GetAbyss_CardPlotListTitleName1Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardPlotListTitleName2ByName.lua.lua
**Functions:**
- GetAbyss_CardPlotListTitleName2Uis
**Snippet:**
```lua
function GetAbyss_CardPlotListTitleName2Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardPlotListTitleName3BtnByName.lua.lua
**Functions:**
- GetAbyss_CardPlotListTitleName3BtnUis
**Snippet:**
```lua
function GetAbyss_CardPlotListTitleName3BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardPlotListTitleName4ByName.lua.lua
**Functions:**
- GetAbyss_CardPlotListTitleName4Uis
**Snippet:**
```lua
function GetAbyss_CardPlotListTitleName4Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardPlotListWindowByName.lua.lua
**Functions:**
- GetAbyss_CardPlotListWindowUis
**Requires:**
- Abyss_CardPlotListByName
**Snippet:**
```lua
require("Abyss_CardPlotListByName")

function GetAbyss_CardPlotListWindowUis(ui)
  local uis = {}
  uis.Main = GetAbyss_CardPlotListUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardPlotMainAssetsExplainByName.lua.lua
**Functions:**
- GetAbyss_CardPlotMainAssetsExplainUis
**Snippet:**
```lua
function GetAbyss_CardPlotMainAssetsExplainUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardPlotMainAssetsTipsByName.lua.lua
**Functions:**
- GetAbyss_CardPlotMainAssetsTipsUis
**Requires:**
- Abyss_CardPlotMainAssetsExplainByName
**Snippet:**
```lua
require("Abyss_CardPlotMainAssetsExplainByName")

function GetAbyss_CardPlotMainAssetsTipsUis(ui)
  local uis = {}
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.Explain = GetAbyss_CardPlotMainAssetsExplainUis(ui:GetChild("Explain"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## Abyss/Abyss_CardPlotMainByName.lua.lua
**Functions:**
- GetAbyss_CardPlotMainUis
**Requires:**
- CommonResource_BackGroundByName
- Abyss_CardPlotMainAssetsTipsByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Abyss_CardPlotMainAssetsTipsByName")
require("CommonResource_CurrencyReturnByName")

function GetAbyss_CardPlotMainUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.AssetsTips = GetAbyss_CardPlotMainAssetsTipsUis(ui:GetChild("AssetsTips"))
  uis.Entry1Btn = ui:GetChild("Entry1Btn")
  uis.Entry2Btn = ui:GetChild("Entry2Btn")
```

---

## Abyss/Abyss_CardPlotMainEntry1BtnByName.lua.lua
**Functions:**
- GetAbyss_CardPlotMainEntry1BtnUis
**Snippet:**
```lua
function GetAbyss_CardPlotMainEntry1BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardPlotMainEntry2BtnByName.lua.lua
**Functions:**
- GetAbyss_CardPlotMainEntry2BtnUis
**Snippet:**
```lua
function GetAbyss_CardPlotMainEntry2BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardPlotMainWindowByName.lua.lua
**Functions:**
- GetAbyss_CardPlotMainWindowUis
**Requires:**
- Abyss_CardPlotMainByName
**Snippet:**
```lua
require("Abyss_CardPlotMainByName")

function GetAbyss_CardPlotMainWindowUis(ui)
  local uis = {}
  uis.Main = GetAbyss_CardPlotMainUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardPlotProgressByName.lua.lua
**Functions:**
- GetAbyss_CardPlotProgressUis
**Snippet:**
```lua
function GetAbyss_CardPlotProgressUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardPlotScheduleByName.lua.lua
**Functions:**
- GetAbyss_CardPlotScheduleUis
**Snippet:**
```lua
function GetAbyss_CardPlotScheduleUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardPlotStartByName.lua.lua
**Functions:**
- GetAbyss_CardPlotStartUis
**Requires:**
- CommonResource_PopupBgByName
- Abyss_CardTitleShowByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Abyss_CardTitleShowByName")

function GetAbyss_CardPlotStartUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.CardTitleShow = GetAbyss_CardTitleShowUis(ui:GetChild("CardTitleShow"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.root = ui
  return uis
```

---

## Abyss/Abyss_CardPlotStartWindowByName.lua.lua
**Functions:**
- GetAbyss_CardPlotStartWindowUis
**Requires:**
- Abyss_CardPlotStartByName
**Snippet:**
```lua
require("Abyss_CardPlotStartByName")

function GetAbyss_CardPlotStartWindowUis(ui)
  local uis = {}
  uis.Main = GetAbyss_CardPlotStartUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardPlotTalkByName.lua.lua
**Functions:**
- GetAbyss_CardPlotTalkUis
**Requires:**
- CommonResource_BackGroundByName
- Abyss_CardPlotTalkLeftByName
- Abyss_WeatherByName
- Abyss_TalkTipsByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Abyss_CardPlotTalkLeftByName")
require("Abyss_WeatherByName")
require("Abyss_TalkTipsByName")

function GetAbyss_CardPlotTalkUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TabRegion = GetAbyss_CardPlotTalkLeftUis(ui:GetChild("TabRegion"))
  uis.Weather = GetAbyss_WeatherUis(ui:GetChild("Weather"))
```

---

## Abyss/Abyss_CardPlotTalkLeftByName.lua.lua
**Functions:**
- GetAbyss_CardPlotTalkLeftUis
**Snippet:**
```lua
function GetAbyss_CardPlotTalkLeftUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardPlotTalkLeftSignByName.lua.lua
**Functions:**
- GetAbyss_CardPlotTalkLeftSignUis
**Snippet:**
```lua
function GetAbyss_CardPlotTalkLeftSignUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardPlotTalkLeftTabBtnByName.lua.lua
**Functions:**
- GetAbyss_CardPlotTalkLeftTabBtnUis
**Requires:**
- Abyss_CardPlotTalkLeftSignByName
**Snippet:**
```lua
require("Abyss_CardPlotTalkLeftSignByName")

function GetAbyss_CardPlotTalkLeftTabBtnUis(ui)
  local uis = {}
  uis.Sign = GetAbyss_CardPlotTalkLeftSignUis(ui:GetChild("Sign"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Abyss/Abyss_CardPlotTalkWindowByName.lua.lua
**Functions:**
- GetAbyss_CardPlotTalkWindowUis
**Requires:**
- Abyss_CardPlotTalkByName
**Snippet:**
```lua
require("Abyss_CardPlotTalkByName")

function GetAbyss_CardPlotTalkWindowUis(ui)
  local uis = {}
  uis.Main = GetAbyss_CardPlotTalkUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardPlotTalk_HideBtnByName.lua.lua
**Functions:**
- GetAbyss_CardPlotTalk_HideBtnUis
**Snippet:**
```lua
function GetAbyss_CardPlotTalk_HideBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardPlotTalk_HideByName.lua.lua
**Functions:**
- GetAbyss_CardPlotTalk_HideUis
**Snippet:**
```lua
function GetAbyss_CardPlotTalk_HideUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardSwitchBtnByName.lua.lua
**Functions:**
- GetAbyss_CardSwitchBtnUis
**Snippet:**
```lua
function GetAbyss_CardSwitchBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardTaskByName.lua.lua
**Functions:**
- GetAbyss_CardTaskUis
**Requires:**
- Abyss_CardTaskTimeByName
**Snippet:**
```lua
require("Abyss_CardTaskTimeByName")

function GetAbyss_CardTaskUis(ui)
  local uis = {}
  uis.Time = GetAbyss_CardTaskTimeUis(ui:GetChild("Time"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TaskDirectionBtn = ui:GetChild("TaskDirectionBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Abyss/Abyss_CardTaskTimeByName.lua.lua
**Functions:**
- GetAbyss_CardTaskTimeUis
**Snippet:**
```lua
function GetAbyss_CardTaskTimeUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CardTitleShowByName.lua.lua
**Functions:**
- GetAbyss_CardTitleShowUis
**Snippet:**
```lua
function GetAbyss_CardTitleShowUis(ui)
  local uis = {}
  
  uis.TitleLoader = ui:GetChild("TitleLoader")
  uis.TitleHolder = ui:GetChild("TitleHolder")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CollectionAniByName.lua.lua
**Functions:**
- GetAbyss_CollectionAniUis
**Snippet:**
```lua
function GetAbyss_CollectionAniUis(ui)
  local uis = {}
  
  uis.CollectionBtn = ui:GetChild("CollectionBtn")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CollectionBtnByName.lua.lua
**Functions:**
- GetAbyss_CollectionBtnUis
**Snippet:**
```lua
function GetAbyss_CollectionBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.SellStateCtr = ui:GetController("SellState")
  uis.TypeCtr = ui:GetController("Type")
  uis.root = ui
```

---

## Abyss/Abyss_CycleCommodity1ByName.lua.lua
**Functions:**
- GetAbyss_CycleCommodity1Uis
**Requires:**
- Abyss_SellOutByName
- Abyss_ItemLockByName
- CommonResource_RedDotByName
- Abyss_NewByName
- Abyss_CycleCommodityTimeByName
**Snippet:**
```lua
require("Abyss_SellOutByName")
require("Abyss_ItemLockByName")
require("CommonResource_RedDotByName")
require("Abyss_NewByName")
require("Abyss_CycleCommodityTimeByName")

function GetAbyss_CycleCommodity1Uis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
```

---

## Abyss/Abyss_CycleCommodity1GetBtnByName.lua.lua
**Functions:**
- GetAbyss_CycleCommodity1GetBtnUis
**Snippet:**
```lua
function GetAbyss_CycleCommodity1GetBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CycleCommodity2ByName.lua.lua
**Functions:**
- GetAbyss_CycleCommodity2Uis
**Requires:**
- Abyss_SellOutByName
- Abyss_ItemLockByName
- Abyss_NewByName
- Abyss_CycleCommodityTimeByName
**Snippet:**
```lua
require("Abyss_SellOutByName")
require("Abyss_ItemLockByName")
require("Abyss_NewByName")
require("Abyss_CycleCommodityTimeByName")

function GetAbyss_CycleCommodity2Uis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.SurplusTxt = ui:GetChild("SurplusTxt")
```

---

## Abyss/Abyss_CycleCommodity3ByName.lua.lua
**Functions:**
- GetAbyss_CycleCommodity3Uis
**Requires:**
- Abyss_SellOutByName
- Abyss_ItemLockByName
- Abyss_NewByName
- Abyss_CycleCommodityTimeByName
**Snippet:**
```lua
require("Abyss_SellOutByName")
require("Abyss_ItemLockByName")
require("Abyss_NewByName")
require("Abyss_CycleCommodityTimeByName")

function GetAbyss_CycleCommodity3Uis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.SurplusTxt = ui:GetChild("SurplusTxt")
```

---

## Abyss/Abyss_CycleCommodity4ByName.lua.lua
**Functions:**
- GetAbyss_CycleCommodity4Uis
**Requires:**
- Abyss_SellOutByName
- Abyss_ItemLockByName
- Abyss_NewByName
- Abyss_CycleCommodityTimeByName
- Abyss_CycleCommodity4UseMarkByName
**Snippet:**
```lua
require("Abyss_SellOutByName")
require("Abyss_ItemLockByName")
require("Abyss_NewByName")
require("Abyss_CycleCommodityTimeByName")
require("Abyss_CycleCommodity4UseMarkByName")

function GetAbyss_CycleCommodity4Uis(ui)
  local uis = {}
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
```

---

## Abyss/Abyss_CycleCommodity4UseMarkByName.lua.lua
**Functions:**
- GetAbyss_CycleCommodity4UseMarkUis
**Snippet:**
```lua
function GetAbyss_CycleCommodity4UseMarkUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CycleCommodityAni1ByName.lua.lua
**Functions:**
- GetAbyss_CycleCommodityAni1Uis
**Requires:**
- Abyss_CycleCommodity1ByName
**Snippet:**
```lua
require("Abyss_CycleCommodity1ByName")

function GetAbyss_CycleCommodityAni1Uis(ui)
  local uis = {}
  uis.Item = GetAbyss_CycleCommodity1Uis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CycleCommodityAni2ByName.lua.lua
**Functions:**
- GetAbyss_CycleCommodityAni2Uis
**Requires:**
- Abyss_CycleCommodity2ByName
**Snippet:**
```lua
require("Abyss_CycleCommodity2ByName")

function GetAbyss_CycleCommodityAni2Uis(ui)
  local uis = {}
  uis.Item = GetAbyss_CycleCommodity2Uis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CycleCommodityAni3ByName.lua.lua
**Functions:**
- GetAbyss_CycleCommodityAni3Uis
**Requires:**
- Abyss_CycleCommodity3ByName
**Snippet:**
```lua
require("Abyss_CycleCommodity3ByName")

function GetAbyss_CycleCommodityAni3Uis(ui)
  local uis = {}
  uis.Item = GetAbyss_CycleCommodity3Uis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CycleCommodityAni4ByName.lua.lua
**Functions:**
- GetAbyss_CycleCommodityAni4Uis
**Requires:**
- Abyss_CycleCommodity4ByName
**Snippet:**
```lua
require("Abyss_CycleCommodity4ByName")

function GetAbyss_CycleCommodityAni4Uis(ui)
  local uis = {}
  uis.Item = GetAbyss_CycleCommodity4Uis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CycleCommodityTimeByName.lua.lua
**Functions:**
- GetAbyss_CycleCommodityTimeUis
**Snippet:**
```lua
function GetAbyss_CycleCommodityTimeUis(ui)
  local uis = {}
  
  uis.TimeHolder = ui:GetChild("TimeHolder")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_CycleShopByName.lua.lua
**Functions:**
- GetAbyss_CycleShopUis
**Snippet:**
```lua
function GetAbyss_CycleShopUis(ui)
  local uis = {}
  
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_DailyTaskBtnByName.lua.lua
**Functions:**
- GetAbyss_DailyTaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetAbyss_DailyTaskBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_DayByName.lua.lua
**Functions:**
- GetAbyss_DayUis
**Snippet:**
```lua
function GetAbyss_DayUis(ui)
  local uis = {}
  
  uis.Day1Txt = ui:GetChild("Day1Txt")
  uis.Day2Txt = ui:GetChild("Day2Txt")
  uis.UnitTxt = ui:GetChild("UnitTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_DeleteBtnByName.lua.lua
**Functions:**
- GetAbyss_DeleteBtnUis
**Snippet:**
```lua
function GetAbyss_DeleteBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_DetailsTipsAniByName.lua.lua
**Functions:**
- GetAbyss_DetailsTipsAniUis
**Requires:**
- Abyss_DetailsTipsByName
**Snippet:**
```lua
require("Abyss_DetailsTipsByName")

function GetAbyss_DetailsTipsAniUis(ui)
  local uis = {}
  uis.DetailsTips = GetAbyss_DetailsTipsUis(ui:GetChild("DetailsTips"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_DetailsTipsByName.lua.lua
**Functions:**
- GetAbyss_DetailsTipsUis
**Requires:**
- Abyss_CardPlotProgressByName
**Snippet:**
```lua
require("Abyss_CardPlotProgressByName")

function GetAbyss_DetailsTipsUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.Progress = GetAbyss_CardPlotProgressUis(ui:GetChild("Progress"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Abyss/Abyss_DetailsTipsLineAniByName.lua.lua
**Functions:**
- GetAbyss_DetailsTipsLineAniUis
**Requires:**
- Abyss_DetailsTipsLineByName
**Snippet:**
```lua
require("Abyss_DetailsTipsLineByName")

function GetAbyss_DetailsTipsLineAniUis(ui)
  local uis = {}
  uis.DetailsTipsLine = GetAbyss_DetailsTipsLineUis(ui:GetChild("DetailsTipsLine"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_DetailsTipsLineByName.lua.lua
**Functions:**
- GetAbyss_DetailsTipsLineUis
**Snippet:**
```lua
function GetAbyss_DetailsTipsLineUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_DetailsTipsTitleAniByName.lua.lua
**Functions:**
- GetAbyss_DetailsTipsTitleAniUis
**Requires:**
- Abyss_DetailsTipsTitleByName
**Snippet:**
```lua
require("Abyss_DetailsTipsTitleByName")

function GetAbyss_DetailsTipsTitleAniUis(ui)
  local uis = {}
  uis.DetailsTipsTitle = GetAbyss_DetailsTipsTitleUis(ui:GetChild("DetailsTipsTitle"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_DetailsTipsTitleByName.lua.lua
**Functions:**
- GetAbyss_DetailsTipsTitleUis
**Requires:**
- Abyss_CardPlotListTipsHeadByName
- Abyss_CardPlotProgressByName
**Snippet:**
```lua
require("Abyss_CardPlotListTipsHeadByName")
require("Abyss_CardPlotProgressByName")

function GetAbyss_DetailsTipsTitleUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.PicHolder = ui:GetChild("PicHolder")
  uis.Head = GetAbyss_CardPlotListTipsHeadUis(ui:GetChild("Head"))
  uis.Progress = GetAbyss_CardPlotProgressUis(ui:GetChild("Progress"))
  uis.ScheduleList = ui:GetChild("ScheduleList")
```

---

## Abyss/Abyss_EventChoiceByName.lua.lua
**Functions:**
- GetAbyss_EventChoiceUis
**Snippet:**
```lua
function GetAbyss_EventChoiceUis(ui)
  local uis = {}
  
  uis.EventTabBtn = ui:GetChild("EventTabBtn")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_EventSpendByName.lua.lua
**Functions:**
- GetAbyss_EventSpendUis
**Snippet:**
```lua
function GetAbyss_EventSpendUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_EventTabBtnByName.lua.lua
**Functions:**
- GetAbyss_EventTabBtnUis
**Snippet:**
```lua
function GetAbyss_EventTabBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_EventTipsAniByName.lua.lua
**Functions:**
- GetAbyss_EventTipsAniUis
**Requires:**
- Abyss_EventTipsByName
**Snippet:**
```lua
require("Abyss_EventTipsByName")

function GetAbyss_EventTipsAniUis(ui)
  local uis = {}
  uis.EventTips = GetAbyss_EventTipsUis(ui:GetChild("EventTips"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_EventTipsByName.lua.lua
**Functions:**
- GetAbyss_EventTipsUis
**Requires:**
- Abyss_EventSpendByName
**Snippet:**
```lua
require("Abyss_EventSpendByName")

function GetAbyss_EventTipsUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EventSpend = GetAbyss_EventSpendUis(ui:GetChild("EventSpend"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## Abyss/Abyss_EventTipsListByName.lua.lua
**Functions:**
- GetAbyss_EventTipsListUis
**Snippet:**
```lua
function GetAbyss_EventTipsListUis(ui)
  local uis = {}
  
  uis.EventTipsList = ui:GetChild("EventTipsList")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExclamatoryByName.lua.lua
**Functions:**
- GetAbyss_ExclamatoryUis
**Snippet:**
```lua
function GetAbyss_ExclamatoryUis(ui)
  local uis = {}
  
  uis.EffectLoader = ui:GetChild("EffectLoader")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExpeditionBtnByName.lua.lua
**Functions:**
- GetAbyss_ExpeditionBtnUis
**Snippet:**
```lua
function GetAbyss_ExpeditionBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExpeditionCompleteByName.lua.lua
**Functions:**
- GetAbyss_ExpeditionCompleteUis
**Snippet:**
```lua
function GetAbyss_ExpeditionCompleteUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExpeditionGoBtnByName.lua.lua
**Functions:**
- GetAbyss_ExpeditionGoBtnUis
**Snippet:**
```lua
function GetAbyss_ExpeditionGoBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExpeditionLayerByName.lua.lua
**Functions:**
- GetAbyss_ExpeditionLayerUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetAbyss_ExpeditionLayerUis(ui)
  local uis = {}
  uis.Name3Txt = ui:GetChild("Name3Txt")
  uis.Name1Txt = ui:GetChild("Name1Txt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.root = ui
  return uis
```

---

## Abyss/Abyss_ExpeditionLockByName.lua.lua
**Functions:**
- GetAbyss_ExpeditionLockUis
**Snippet:**
```lua
function GetAbyss_ExpeditionLockUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExpeditionRegionByName.lua.lua
**Functions:**
- GetAbyss_ExpeditionRegionUis
**Requires:**
- Abyss_ExpeditionLayerByName
- Abyss_ExpeditionCompleteByName
- Abyss_ExpeditionLockByName
- Abyss_ExpeditionTimeByName
**Snippet:**
```lua
require("Abyss_ExpeditionLayerByName")
require("Abyss_ExpeditionCompleteByName")
require("Abyss_ExpeditionLockByName")
require("Abyss_ExpeditionTimeByName")

function GetAbyss_ExpeditionRegionUis(ui)
  local uis = {}
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.ExpeditionLayer = GetAbyss_ExpeditionLayerUis(ui:GetChild("ExpeditionLayer"))
```

---

## Abyss/Abyss_ExpeditionReward1ByName.lua.lua
**Functions:**
- GetAbyss_ExpeditionReward1Uis
**Requires:**
- Abyss_ExpeditionRewardTotalByName
**Snippet:**
```lua
require("Abyss_ExpeditionRewardTotalByName")

function GetAbyss_ExpeditionReward1Uis(ui)
  local uis = {}
  uis.Total = GetAbyss_ExpeditionRewardTotalUis(ui:GetChild("Total"))
  uis.RewardList = ui:GetChild("RewardList")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExpeditionReward2ByName.lua.lua
**Functions:**
- GetAbyss_ExpeditionReward2Uis
**Requires:**
- CommonResource_PopupBgByName
- Abyss_ExpeditionReward1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Abyss_ExpeditionReward1ByName")

function GetAbyss_ExpeditionReward2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.ExpeditionReward1 = GetAbyss_ExpeditionReward1Uis(ui:GetChild("ExpeditionReward1"))
  uis.root = ui
  return uis
```

---

## Abyss/Abyss_ExpeditionRewardFrameByName.lua.lua
**Functions:**
- GetAbyss_ExpeditionRewardFrameUis
**Snippet:**
```lua
function GetAbyss_ExpeditionRewardFrameUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExpeditionRewardItemAniByName.lua.lua
**Functions:**
- GetAbyss_ExpeditionRewardItemAniUis
**Requires:**
- Abyss_ExpeditionRewardItemByName
**Snippet:**
```lua
require("Abyss_ExpeditionRewardItemByName")

function GetAbyss_ExpeditionRewardItemAniUis(ui)
  local uis = {}
  uis.Item = GetAbyss_ExpeditionRewardItemUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExpeditionRewardItemByName.lua.lua
**Functions:**
- GetAbyss_ExpeditionRewardItemUis
**Requires:**
- Abyss_ExpeditionRewardFrameByName
**Snippet:**
```lua
require("Abyss_ExpeditionRewardFrameByName")

function GetAbyss_ExpeditionRewardItemUis(ui)
  local uis = {}
  uis.StarNumberTxt = ui:GetChild("StarNumberTxt")
  uis.GetTxt = ui:GetChild("GetTxt")
  uis.Item = GetAbyss_ExpeditionRewardFrameUis(ui:GetChild("Item"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Abyss/Abyss_ExpeditionRewardTotalByName.lua.lua
**Functions:**
- GetAbyss_ExpeditionRewardTotalUis
**Snippet:**
```lua
function GetAbyss_ExpeditionRewardTotalUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExpeditionRewardWindowByName.lua.lua
**Functions:**
- GetAbyss_ExpeditionRewardWindowUis
**Requires:**
- Abyss_ExpeditionReward2ByName
**Snippet:**
```lua
require("Abyss_ExpeditionReward2ByName")

function GetAbyss_ExpeditionRewardWindowUis(ui)
  local uis = {}
  uis.Main = GetAbyss_ExpeditionReward2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExpeditionTimeByName.lua.lua
**Functions:**
- GetAbyss_ExpeditionTimeUis
**Snippet:**
```lua
function GetAbyss_ExpeditionTimeUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExplainBtnByName.lua.lua
**Functions:**
- GetAbyss_ExplainBtnUis
**Snippet:**
```lua
function GetAbyss_ExplainBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExploreDungeonProgressBarByName.lua.lua
**Functions:**
- GetAbyss_ExploreDungeonProgressBarUis
**Requires:**
- Abyss_ExploreDungeonProgressFillByName
**Snippet:**
```lua
require("Abyss_ExploreDungeonProgressFillByName")

function GetAbyss_ExploreDungeonProgressBarUis(ui)
  local uis = {}
  uis.bar = GetAbyss_ExploreDungeonProgressFillUis(ui:GetChild("bar"))
  uis.ScaleHolder = ui:GetChild("ScaleHolder")
  uis.ScaleLoader = ui:GetChild("ScaleLoader")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExploreDungeonProgressByName.lua.lua
**Functions:**
- GetAbyss_ExploreDungeonProgressUis
**Snippet:**
```lua
function GetAbyss_ExploreDungeonProgressUis(ui)
  local uis = {}
  
  uis.ExploreDungeonProgressBar = ui:GetChild("ExploreDungeonProgressBar")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExploreDungeonProgressFillByName.lua.lua
**Functions:**
- GetAbyss_ExploreDungeonProgressFillUis
**Snippet:**
```lua
function GetAbyss_ExploreDungeonProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExploreDungeonRegionByName.lua.lua
**Functions:**
- GetAbyss_ExploreDungeonRegionUis
**Requires:**
- Abyss_ExploreDungeonProgressByName
- Abyss_BuildTipsLockByName
**Snippet:**
```lua
require("Abyss_ExploreDungeonProgressByName")
require("Abyss_BuildTipsLockByName")

function GetAbyss_ExploreDungeonRegionUis(ui)
  local uis = {}
  uis.Progress = GetAbyss_ExploreDungeonProgressUis(ui:GetChild("Progress"))
  uis.GoBtn = ui:GetChild("GoBtn")
  uis.Lock = GetAbyss_BuildTipsLockUis(ui:GetChild("Lock"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Abyss/Abyss_ExploreExpProgressBarByName.lua.lua
**Functions:**
- GetAbyss_ExploreExpProgressBarUis
**Requires:**
- Abyss_ExploreExpProgressFillByName
**Snippet:**
```lua
require("Abyss_ExploreExpProgressFillByName")

function GetAbyss_ExploreExpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetAbyss_ExploreExpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExploreExpProgressFillByName.lua.lua
**Functions:**
- GetAbyss_ExploreExpProgressFillUis
**Snippet:**
```lua
function GetAbyss_ExploreExpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExploreFastAddBtnByName.lua.lua
**Functions:**
- GetAbyss_ExploreFastAddBtnUis
**Snippet:**
```lua
function GetAbyss_ExploreFastAddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExploreFastBuyBtnByName.lua.lua
**Functions:**
- GetAbyss_ExploreFastBuyBtnUis
**Snippet:**
```lua
function GetAbyss_ExploreFastBuyBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExploreFastByName.lua.lua
**Functions:**
- GetAbyss_ExploreFastUis
**Requires:**
- CommonResource_PopupBgByName
- Abyss_ExploreFastTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Abyss_ExploreFastTipsByName")

function GetAbyss_ExploreFastUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Tips = GetAbyss_ExploreFastTipsUis(ui:GetChild("Tips"))
  uis.AssetsList = ui:GetChild("AssetsList")
  uis.root = ui
```

---

## Abyss/Abyss_ExploreFastCloseBtnByName.lua.lua
**Functions:**
- GetAbyss_ExploreFastCloseBtnUis
**Snippet:**
```lua
function GetAbyss_ExploreFastCloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExploreFastItem1ByName.lua.lua
**Functions:**
- GetAbyss_ExploreFastItem1Uis
**Requires:**
- Abyss_ExploreFastSpend1ByName
- Abyss_ExploreFastNumberStripByName
**Snippet:**
```lua
require("Abyss_ExploreFastSpend1ByName")
require("Abyss_ExploreFastNumberStripByName")

function GetAbyss_ExploreFastItem1Uis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Spend = GetAbyss_ExploreFastSpend1Uis(ui:GetChild("Spend"))
  uis.NumberStrip = GetAbyss_ExploreFastNumberStripUis(ui:GetChild("NumberStrip"))
```

---

## Abyss/Abyss_ExploreFastItem2AniByName.lua.lua
**Functions:**
- GetAbyss_ExploreFastItem2AniUis
**Requires:**
- Abyss_ExploreFastItem2ByName
**Snippet:**
```lua
require("Abyss_ExploreFastItem2ByName")

function GetAbyss_ExploreFastItem2AniUis(ui)
  local uis = {}
  uis.Item = GetAbyss_ExploreFastItem2Uis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExploreFastItem2ByName.lua.lua
**Functions:**
- GetAbyss_ExploreFastItem2Uis
**Snippet:**
```lua
function GetAbyss_ExploreFastItem2Uis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExploreFastItemChoiceBtnByName.lua.lua
**Functions:**
- GetAbyss_ExploreFastItemChoiceBtnUis
**Snippet:**
```lua
function GetAbyss_ExploreFastItemChoiceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExploreFastNumberStripByName.lua.lua
**Functions:**
- GetAbyss_ExploreFastNumberStripUis
**Snippet:**
```lua
function GetAbyss_ExploreFastNumberStripUis(ui)
  local uis = {}
  
  uis.ChoiceNumberTxt = ui:GetChild("ChoiceNumberTxt")
  uis.ReduceBtn = ui:GetChild("ReduceBtn")
  uis.AddBtn = ui:GetChild("AddBtn")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExploreFastReduceBtnByName.lua.lua
**Functions:**
- GetAbyss_ExploreFastReduceBtnUis
**Snippet:**
```lua
function GetAbyss_ExploreFastReduceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExploreFastSpend1ByName.lua.lua
**Functions:**
- GetAbyss_ExploreFastSpend1Uis
**Snippet:**
```lua
function GetAbyss_ExploreFastSpend1Uis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExploreFastSpend2ByName.lua.lua
**Functions:**
- GetAbyss_ExploreFastSpend2Uis
**Snippet:**
```lua
function GetAbyss_ExploreFastSpend2Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExploreFastTipsByName.lua.lua
**Functions:**
- GetAbyss_ExploreFastTipsUis
**Requires:**
- Abyss_ExploreFastSpend2ByName
**Snippet:**
```lua
require("Abyss_ExploreFastSpend2ByName")

function GetAbyss_ExploreFastTipsUis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.BuyBtn = ui:GetChild("BuyBtn")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.Item1List = ui:GetChild("Item1List")
  uis.Item2List = ui:GetChild("Item2List")
  uis.Spend = GetAbyss_ExploreFastSpend2Uis(ui:GetChild("Spend"))
```

---

## Abyss/Abyss_ExploreFastWindowByName.lua.lua
**Functions:**
- GetAbyss_ExploreFastWindowUis
**Requires:**
- Abyss_ExploreFastByName
**Snippet:**
```lua
require("Abyss_ExploreFastByName")

function GetAbyss_ExploreFastWindowUis(ui)
  local uis = {}
  uis.Main = GetAbyss_ExploreFastUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExploreLevelByName.lua.lua
**Functions:**
- GetAbyss_ExploreLevelUis
**Snippet:**
```lua
function GetAbyss_ExploreLevelUis(ui)
  local uis = {}
  
  uis.ExpProgressBar = ui:GetChild("ExpProgressBar")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.ExpTxt = ui:GetChild("ExpTxt")
  uis.ExpMaxTxt = ui:GetChild("ExpMaxTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Abyss/Abyss_ExploreRegionByName.lua.lua
**Functions:**
- GetAbyss_ExploreRegionUis
**Requires:**
- Abyss_ExploreLevelByName
- Abyss_BuildTipsLockByName
**Snippet:**
```lua
require("Abyss_ExploreLevelByName")
require("Abyss_BuildTipsLockByName")

function GetAbyss_ExploreRegionUis(ui)
  local uis = {}
  uis.ExploreLevel = GetAbyss_ExploreLevelUis(ui:GetChild("ExploreLevel"))
  uis.StateList = ui:GetChild("StateList")
  uis.GoBtn = ui:GetChild("GoBtn")
  uis.Lock = GetAbyss_BuildTipsLockUis(ui:GetChild("Lock"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## Abyss/Abyss_ExploreShopByName.lua.lua
**Functions:**
- GetAbyss_ExploreShopUis
**Requires:**
- Abyss_ExploreShop_LeftTabByName
- Abyss_ExploreShop_ItemRegionByName
**Snippet:**
```lua
require("Abyss_ExploreShop_LeftTabByName")
require("Abyss_ExploreShop_ItemRegionByName")

function GetAbyss_ExploreShopUis(ui)
  local uis = {}
  uis.LeftTab = GetAbyss_ExploreShop_LeftTabUis(ui:GetChild("LeftTab"))
  uis.ItemRegion = GetAbyss_ExploreShop_ItemRegionUis(ui:GetChild("ItemRegion"))
  uis.QuickBtn = ui:GetChild("QuickBtn")
  uis.root = ui
  return uis
```

---

## Abyss/Abyss_ExploreShop_ItemAniByName.lua.lua
**Functions:**
- GetAbyss_ExploreShop_ItemAniUis
**Requires:**
- Abyss_ExploreShop_ItemByName
**Snippet:**
```lua
require("Abyss_ExploreShop_ItemByName")

function GetAbyss_ExploreShop_ItemAniUis(ui)
  local uis = {}
  uis.Item = GetAbyss_ExploreShop_ItemUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExploreShop_ItemByName.lua.lua
**Functions:**
- GetAbyss_ExploreShop_ItemUis
**Requires:**
- Abyss_SellOutByName
- Abyss_ItemLockByName
- Abyss_NewByName
- Abyss_CycleCommodityTimeByName
- Abyss_CycleCommodity4UseMarkByName
**Snippet:**
```lua
require("Abyss_SellOutByName")
require("Abyss_ItemLockByName")
require("Abyss_NewByName")
require("Abyss_CycleCommodityTimeByName")
require("Abyss_CycleCommodity4UseMarkByName")

function GetAbyss_ExploreShop_ItemUis(ui)
  local uis = {}
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
```

---

## Abyss/Abyss_ExploreShop_ItemRegionByName.lua.lua
**Functions:**
- GetAbyss_ExploreShop_ItemRegionUis
**Snippet:**
```lua
function GetAbyss_ExploreShop_ItemRegionUis(ui)
  local uis = {}
  
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExploreShop_LeftBtnByName.lua.lua
**Functions:**
- GetAbyss_ExploreShop_LeftBtnUis
**Requires:**
- Abyss_ExploreShop_LeftTabTimeByName
- CommonResource_RedDotByName
- Abyss_ExploreShop_NewByName
**Snippet:**
```lua
require("Abyss_ExploreShop_LeftTabTimeByName")
require("CommonResource_RedDotByName")
require("Abyss_ExploreShop_NewByName")

function GetAbyss_ExploreShop_LeftBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.Time = GetAbyss_ExploreShop_LeftTabTimeUis(ui:GetChild("Time"))
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
```

---

## Abyss/Abyss_ExploreShop_LeftTabByName.lua.lua
**Functions:**
- GetAbyss_ExploreShop_LeftTabUis
**Snippet:**
```lua
function GetAbyss_ExploreShop_LeftTabUis(ui)
  local uis = {}
  
  uis.LeftTabList = ui:GetChild("LeftTabList")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExploreShop_LeftTabTimeByName.lua.lua
**Functions:**
- GetAbyss_ExploreShop_LeftTabTimeUis
**Snippet:**
```lua
function GetAbyss_ExploreShop_LeftTabTimeUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExploreShop_NewByName.lua.lua
**Functions:**
- GetAbyss_ExploreShop_NewUis
**Snippet:**
```lua
function GetAbyss_ExploreShop_NewUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExploreShop_QuickBtnByName.lua.lua
**Functions:**
- GetAbyss_ExploreShop_QuickBtnUis
**Snippet:**
```lua
function GetAbyss_ExploreShop_QuickBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ExploreStateByName.lua.lua
**Functions:**
- GetAbyss_ExploreStateUis
**Snippet:**
```lua
function GetAbyss_ExploreStateUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NothingTxt = ui:GetChild("NothingTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Abyss/Abyss_FixedShopByName.lua.lua
**Functions:**
- GetAbyss_FixedShopUis
**Snippet:**
```lua
function GetAbyss_FixedShopUis(ui)
  local uis = {}
  
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_FunctionOpenBtnByName.lua.lua
**Functions:**
- GetAbyss_FunctionOpenBtnUis
**Snippet:**
```lua
function GetAbyss_FunctionOpenBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_GuideboardBtnByName.lua.lua
**Functions:**
- GetAbyss_GuideboardBtnUis
**Snippet:**
```lua
function GetAbyss_GuideboardBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_GuideBoardByName.lua.lua
**Functions:**
- GetAbyss_GuideBoardUis
**Requires:**
- CommonResource_PopupBgByName
- Abyss_GuideBoardTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Abyss_GuideBoardTipsByName")

function GetAbyss_GuideBoardUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.GuideBoardTips = GetAbyss_GuideBoardTipsUis(ui:GetChild("GuideBoardTips"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_GuideBoardTipsBtnByName.lua.lua
**Functions:**
- GetAbyss_GuideBoardTipsBtnUis
**Snippet:**
```lua
function GetAbyss_GuideBoardTipsBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_GuideBoardTipsByName.lua.lua
**Functions:**
- GetAbyss_GuideBoardTipsUis
**Snippet:**
```lua
function GetAbyss_GuideBoardTipsUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.SureBtn = ui:GetChild("SureBtn")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_GuideBoardWindowByName.lua.lua
**Functions:**
- GetAbyss_GuideBoardWindowUis
**Requires:**
- Abyss_GuideBoardByName
**Snippet:**
```lua
require("Abyss_GuideBoardByName")

function GetAbyss_GuideBoardWindowUis(ui)
  local uis = {}
  uis.Main = GetAbyss_GuideBoardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_GuideBoardWordByName.lua.lua
**Functions:**
- GetAbyss_GuideBoardWordUis
**Snippet:**
```lua
function GetAbyss_GuideBoardWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_HandBookEventByName.lua.lua
**Functions:**
- GetAbyss_HandBookEventUis
**Requires:**
- Abyss_MonsterBookByName
- Abyss_MusicBookByName
- Abyss_HandBookEventCollectByName
**Snippet:**
```lua
require("Abyss_MonsterBookByName")
require("Abyss_MusicBookByName")
require("Abyss_HandBookEventCollectByName")

function GetAbyss_HandBookEventUis(ui)
  local uis = {}
  uis.MonsterBook = GetAbyss_MonsterBookUis(ui:GetChild("MonsterBook"))
  uis.MusicBook = GetAbyss_MusicBookUis(ui:GetChild("MusicBook"))
  uis.Collect = GetAbyss_HandBookEventCollectUis(ui:GetChild("Collect"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
```

---

## Abyss/Abyss_HandBookEventCollectByName.lua.lua
**Functions:**
- GetAbyss_HandBookEventCollectUis
**Snippet:**
```lua
function GetAbyss_HandBookEventCollectUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_HandBookEventWindowByName.lua.lua
**Functions:**
- GetAbyss_HandBookEventWindowUis
**Requires:**
- Abyss_HandBookEventByName
**Snippet:**
```lua
require("Abyss_HandBookEventByName")

function GetAbyss_HandBookEventWindowUis(ui)
  local uis = {}
  uis.Main = GetAbyss_HandBookEventUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ItemBtnByName.lua.lua
**Functions:**
- GetAbyss_ItemBtnUis
**Snippet:**
```lua
function GetAbyss_ItemBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ItemLockByName.lua.lua
**Functions:**
- GetAbyss_ItemLockUis
**Snippet:**
```lua
function GetAbyss_ItemLockUis(ui)
  local uis = {}
  
  uis.ConditionTxt = ui:GetChild("ConditionTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_LeftBtnByName.lua.lua
**Functions:**
- GetAbyss_LeftBtnUis
**Snippet:**
```lua
function GetAbyss_LeftBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_LeftTabByName.lua.lua
**Functions:**
- GetAbyss_LeftTabUis
**Snippet:**
```lua
function GetAbyss_LeftTabUis(ui)
  local uis = {}
  
  uis.ProgressTxt = ui:GetChild("ProgressTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.LeftTabList = ui:GetChild("LeftTabList")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MapBuildExploreByName.lua.lua
**Functions:**
- GetAbyss_MapBuildExploreUis
**Snippet:**
```lua
function GetAbyss_MapBuildExploreUis(ui)
  local uis = {}
  
  uis.StateList = ui:GetChild("StateList")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MapBuildExploreStateByName.lua.lua
**Functions:**
- GetAbyss_MapBuildExploreStateUis
**Snippet:**
```lua
function GetAbyss_MapBuildExploreStateUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MapBuildLockByName.lua.lua
**Functions:**
- GetAbyss_MapBuildLockUis
**Snippet:**
```lua
function GetAbyss_MapBuildLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MapBuildSignByName.lua.lua
**Functions:**
- GetAbyss_MapBuildSignUis
**Requires:**
- Abyss_MapBuildTimeByName
- Abyss_MapBuildLockByName
- Abyss_MapBuildWordByName
- Abyss_MapBuildExploreByName
**Snippet:**
```lua
require("Abyss_MapBuildTimeByName")
require("Abyss_MapBuildLockByName")
require("Abyss_MapBuildWordByName")
require("Abyss_MapBuildExploreByName")

function GetAbyss_MapBuildSignUis(ui)
  local uis = {}
  uis.MapBuildTime = GetAbyss_MapBuildTimeUis(ui:GetChild("MapBuildTime"))
  uis.MapBuildLock = GetAbyss_MapBuildLockUis(ui:GetChild("MapBuildLock"))
  uis.MapBuildWord = GetAbyss_MapBuildWordUis(ui:GetChild("MapBuildWord"))
```

---

## Abyss/Abyss_MapBuildTimeByName.lua.lua
**Functions:**
- GetAbyss_MapBuildTimeUis
**Snippet:**
```lua
function GetAbyss_MapBuildTimeUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MapBuildWordByName.lua.lua
**Functions:**
- GetAbyss_MapBuildWordUis
**Snippet:**
```lua
function GetAbyss_MapBuildWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MapCloseBtnByName.lua.lua
**Functions:**
- GetAbyss_MapCloseBtnUis
**Snippet:**
```lua
function GetAbyss_MapCloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MapOverlapByName.lua.lua
**Functions:**
- GetAbyss_MapOverlapUis
**Snippet:**
```lua
function GetAbyss_MapOverlapUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MaterialSellByName.lua.lua
**Functions:**
- GetAbyss_MaterialSellUis
**Requires:**
- Abyss_SellContainerByName
- Abyss_NothingByName
**Snippet:**
```lua
require("Abyss_SellContainerByName")
require("Abyss_NothingByName")

function GetAbyss_MaterialSellUis(ui)
  local uis = {}
  uis.TabList = ui:GetChild("TabList")
  uis.ItemList = ui:GetChild("ItemList")
  uis.MaterialSell = GetAbyss_SellContainerUis(ui:GetChild("MaterialSell"))
  uis.AllPutBtn = ui:GetChild("AllPutBtn")
  uis.Nothing = GetAbyss_NothingUis(ui:GetChild("Nothing"))
```

---

## Abyss/Abyss_MaterialTabBtnBgByName.lua.lua
**Functions:**
- GetAbyss_MaterialTabBtnBgUis
**Snippet:**
```lua
function GetAbyss_MaterialTabBtnBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MaterialTabBtnByName.lua.lua
**Functions:**
- GetAbyss_MaterialTabBtnUis
**Requires:**
- Abyss_MaterialTabBtnBgByName
**Snippet:**
```lua
require("Abyss_MaterialTabBtnBgByName")

function GetAbyss_MaterialTabBtnUis(ui)
  local uis = {}
  uis.MaterialTabBtnBg = GetAbyss_MaterialTabBtnBgUis(ui:GetChild("MaterialTabBtnBg"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MemberBtnByName.lua.lua
**Functions:**
- GetAbyss_MemberBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetAbyss_MemberBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MobByName.lua.lua
**Functions:**
- GetAbyss_MobUis
**Requires:**
- CommonResource_PopupBgByName
- Abyss_MobTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Abyss_MobTipsByName")

function GetAbyss_MobUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.MobTips = GetAbyss_MobTipsUis(ui:GetChild("MobTips"))
  uis.root = ui
  return uis
```

---

## Abyss/Abyss_MobTipsBtnByName.lua.lua
**Functions:**
- GetAbyss_MobTipsBtnUis
**Snippet:**
```lua
function GetAbyss_MobTipsBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MobTipsByName.lua.lua
**Functions:**
- GetAbyss_MobTipsUis
**Snippet:**
```lua
function GetAbyss_MobTipsUis(ui)
  local uis = {}
  
  uis.WordList = ui:GetChild("WordList")
  uis.BtnList = ui:GetChild("BtnList")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MobTipsWordByName.lua.lua
**Functions:**
- GetAbyss_MobTipsWordUis
**Snippet:**
```lua
function GetAbyss_MobTipsWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MobWindowByName.lua.lua
**Functions:**
- GetAbyss_MobWindowUis
**Requires:**
- Abyss_MobByName
**Snippet:**
```lua
require("Abyss_MobByName")

function GetAbyss_MobWindowUis(ui)
  local uis = {}
  uis.Main = GetAbyss_MobUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MonsterBookByName.lua.lua
**Functions:**
- GetAbyss_MonsterBookUis
**Requires:**
- Abyss_MonsterShowByName
- Abyss_MonsterTitleByName
**Snippet:**
```lua
require("Abyss_MonsterShowByName")
require("Abyss_MonsterTitleByName")

function GetAbyss_MonsterBookUis(ui)
  local uis = {}
  uis.Show = GetAbyss_MonsterShowUis(ui:GetChild("Show"))
  uis.Title = GetAbyss_MonsterTitleUis(ui:GetChild("Title"))
  uis.MonsterNameTxt = ui:GetChild("MonsterNameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
```

---

## Abyss/Abyss_MonsterShowByName.lua.lua
**Functions:**
- GetAbyss_MonsterShowUis
**Snippet:**
```lua
function GetAbyss_MonsterShowUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.PicHolder = ui:GetChild("PicHolder")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MonsterTitleByName.lua.lua
**Functions:**
- GetAbyss_MonsterTitleUis
**Snippet:**
```lua
function GetAbyss_MonsterTitleUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MoveChoiceAniByName.lua.lua
**Functions:**
- GetAbyss_MoveChoiceAniUis
**Snippet:**
```lua
function GetAbyss_MoveChoiceAniUis(ui)
  local uis = {}
  
  uis.ChoiceBtn = ui:GetChild("ChoiceBtn")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MoveChoiceBtnByName.lua.lua
**Functions:**
- GetAbyss_MoveChoiceBtnUis
**Snippet:**
```lua
function GetAbyss_MoveChoiceBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.BattleTxt = ui:GetChild("BattleTxt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.ItemTxt = ui:GetChild("ItemTxt")
  uis.ItemWordTxt = ui:GetChild("ItemWordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Abyss/Abyss_MoveCloseBtnByName.lua.lua
**Functions:**
- GetAbyss_MoveCloseBtnUis
**Snippet:**
```lua
function GetAbyss_MoveCloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MoveEndBtnByName.lua.lua
**Functions:**
- GetAbyss_MoveEndBtnUis
**Snippet:**
```lua
function GetAbyss_MoveEndBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MoveEventTipsByName.lua.lua
**Functions:**
- GetAbyss_MoveEventTipsUis
**Snippet:**
```lua
function GetAbyss_MoveEventTipsUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.ModuleList = ui:GetChild("ModuleList")
  uis.NextStepBtn = ui:GetChild("NextStepBtn")
  uis.ChoiceList = ui:GetChild("ChoiceList")
  uis.EndChoiceBtn = ui:GetChild("EndChoiceBtn")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
```

---

## Abyss/Abyss_MoveEventTipsWindowByName.lua.lua
**Functions:**
- GetAbyss_MoveEventTipsWindowUis
**Requires:**
- CommonResource_PopupBgByName
- Lottery_AssetsTipsGroupByName
- Abyss_MoveEventTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Lottery_AssetsTipsGroupByName")
require("Abyss_MoveEventTipsByName")

function GetAbyss_MoveEventTipsWindowUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.AssetsTipsGroup = GetLottery_AssetsTipsGroupUis(ui:GetChild("AssetsTipsGroup"))
  uis.Main = GetAbyss_MoveEventTipsUis(ui:GetChild("Main"))
  uis.CloseBtn = ui:GetChild("CloseBtn")
```

---

## Abyss/Abyss_MoveLeftWordByName.lua.lua
**Functions:**
- GetAbyss_MoveLeftWordUis
**Snippet:**
```lua
function GetAbyss_MoveLeftWordUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MoveNextStepBtnByName.lua.lua
**Functions:**
- GetAbyss_MoveNextStepBtnUis
**Snippet:**
```lua
function GetAbyss_MoveNextStepBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MovePlotBtnByName.lua.lua
**Functions:**
- GetAbyss_MovePlotBtnUis
**Snippet:**
```lua
function GetAbyss_MovePlotBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MoveRewardByName.lua.lua
**Functions:**
- GetAbyss_MoveRewardUis
**Snippet:**
```lua
function GetAbyss_MoveRewardUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MoveRewardGroupByName.lua.lua
**Functions:**
- GetAbyss_MoveRewardGroupUis
**Snippet:**
```lua
function GetAbyss_MoveRewardGroupUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MoveRightWordByName.lua.lua
**Functions:**
- GetAbyss_MoveRightWordUis
**Snippet:**
```lua
function GetAbyss_MoveRightWordUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MoveSkipBtnByName.lua.lua
**Functions:**
- GetAbyss_MoveSkipBtnUis
**Snippet:**
```lua
function GetAbyss_MoveSkipBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MoveWordByName.lua.lua
**Functions:**
- GetAbyss_MoveWordUis
**Snippet:**
```lua
function GetAbyss_MoveWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MusicBookByName.lua.lua
**Functions:**
- GetAbyss_MusicBookUis
**Requires:**
- Abyss_MusicShowByName
- Abyss_MusicTitleByName
**Snippet:**
```lua
require("Abyss_MusicShowByName")
require("Abyss_MusicTitleByName")

function GetAbyss_MusicBookUis(ui)
  local uis = {}
  uis.Show = GetAbyss_MusicShowUis(ui:GetChild("Show"))
  uis.Title = GetAbyss_MusicTitleUis(ui:GetChild("Title"))
  uis.MusicNameTxt = ui:GetChild("MusicNameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
```

---

## Abyss/Abyss_MusicShowByName.lua.lua
**Functions:**
- GetAbyss_MusicShowUis
**Snippet:**
```lua
function GetAbyss_MusicShowUis(ui)
  local uis = {}
  
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_MusicTitleByName.lua.lua
**Functions:**
- GetAbyss_MusicTitleUis
**Snippet:**
```lua
function GetAbyss_MusicTitleUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_NewByName.lua.lua
**Functions:**
- GetAbyss_NewUis
**Snippet:**
```lua
function GetAbyss_NewUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_NothingByName.lua.lua
**Functions:**
- GetAbyss_NothingUis
**Snippet:**
```lua
function GetAbyss_NothingUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_NoviceMoveTipsByName.lua.lua
**Functions:**
- GetAbyss_NoviceMoveTipsUis
**Snippet:**
```lua
function GetAbyss_NoviceMoveTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_PlayerBtnByName.lua.lua
**Functions:**
- GetAbyss_PlayerBtnUis
**Snippet:**
```lua
function GetAbyss_PlayerBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_PlayerInfoByName.lua.lua
**Functions:**
- GetAbyss_PlayerInfoUis
**Requires:**
- Abyss_DayByName
**Snippet:**
```lua
require("Abyss_DayByName")

function GetAbyss_PlayerInfoUis(ui)
  local uis = {}
  uis.Day = GetAbyss_DayUis(ui:GetChild("Day"))
  uis.BatteryProgressBar = ui:GetChild("BatteryProgressBar")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.IdNumberTxt = ui:GetChild("IdNumberTxt")
  uis.PlayerNameTxt = ui:GetChild("PlayerNameTxt")
  uis.root = ui
```

---

## Abyss/Abyss_PlotBtnByName.lua.lua
**Functions:**
- GetAbyss_PlotBtnUis
**Snippet:**
```lua
function GetAbyss_PlotBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_PositionBtnByName.lua.lua
**Functions:**
- GetAbyss_PositionBtnUis
**Snippet:**
```lua
function GetAbyss_PositionBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_QBHeadBtnByName.lua.lua
**Functions:**
- GetAbyss_QBHeadBtnUis
**Requires:**
- Abyss_CardHeadPicByName
**Snippet:**
```lua
require("Abyss_CardHeadPicByName")

function GetAbyss_QBHeadBtnUis(ui)
  local uis = {}
  uis.CardHeadPic = GetAbyss_CardHeadPicUis(ui:GetChild("CardHeadPic"))
  uis.CardNameTxt = ui:GetChild("CardNameTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## Abyss/Abyss_QBHeadByName.lua.lua
**Functions:**
- GetAbyss_QBHeadUis
**Snippet:**
```lua
function GetAbyss_QBHeadUis(ui)
  local uis = {}
  
  uis.CardHeadBtn = ui:GetChild("CardHeadBtn")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_QBSwitchByName.lua.lua
**Functions:**
- GetAbyss_QBSwitchUis
**Snippet:**
```lua
function GetAbyss_QBSwitchUis(ui)
  local uis = {}
  
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.HeadList = ui:GetChild("HeadList")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_QBSwitchWindowByName.lua.lua
**Functions:**
- GetAbyss_QBSwitchWindowUis
**Requires:**
- Abyss_QBSwitchByName
**Snippet:**
```lua
require("Abyss_QBSwitchByName")

function GetAbyss_QBSwitchWindowUis(ui)
  local uis = {}
  uis.Main = GetAbyss_QBSwitchUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_RandomChoiceAniByName.lua.lua
**Functions:**
- GetAbyss_RandomChoiceAniUis
**Snippet:**
```lua
function GetAbyss_RandomChoiceAniUis(ui)
  local uis = {}
  
  uis.ChoiceBtn = ui:GetChild("ChoiceBtn")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_RandomChoiceBtnByName.lua.lua
**Functions:**
- GetAbyss_RandomChoiceBtnUis
**Snippet:**
```lua
function GetAbyss_RandomChoiceBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.BattleTxt = ui:GetChild("BattleTxt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.ItemTxt = ui:GetChild("ItemTxt")
  uis.ItemWordTxt = ui:GetChild("ItemWordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Abyss/Abyss_RandomEndBtnByName.lua.lua
**Functions:**
- GetAbyss_RandomEndBtnUis
**Snippet:**
```lua
function GetAbyss_RandomEndBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_RandomNextStepBtnByName.lua.lua
**Functions:**
- GetAbyss_RandomNextStepBtnUis
**Snippet:**
```lua
function GetAbyss_RandomNextStepBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_RandomTipsByName.lua.lua
**Functions:**
- GetAbyss_RandomTipsUis
**Snippet:**
```lua
function GetAbyss_RandomTipsUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TalkList = ui:GetChild("TalkList")
  uis.ChoiceList = ui:GetChild("ChoiceList")
  uis.EndChoiceBtn = ui:GetChild("EndChoiceBtn")
  uis.NextStepBtn = ui:GetChild("NextStepBtn")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Abyss/Abyss_RandomTipsWindowByName.lua.lua
**Functions:**
- GetAbyss_RandomTipsWindowUis
**Requires:**
- CommonResource_PopupBgByName
- Lottery_AssetsTipsGroupByName
- Abyss_RandomTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Lottery_AssetsTipsGroupByName")
require("Abyss_RandomTipsByName")

function GetAbyss_RandomTipsWindowUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.AssetsTipsGroup = GetLottery_AssetsTipsGroupUis(ui:GetChild("AssetsTipsGroup"))
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.Main = GetAbyss_RandomTipsUis(ui:GetChild("Main"))
```

---

## Abyss/Abyss_ReturnBtnByName.lua.lua
**Functions:**
- GetAbyss_ReturnBtnUis
**Snippet:**
```lua
function GetAbyss_ReturnBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_RogueLetterBtnByName.lua.lua
**Functions:**
- GetAbyss_RogueLetterBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetAbyss_RogueLetterBtnUis(ui)
  local uis = {}
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## Abyss/Abyss_RogueRegionByName.lua.lua
**Functions:**
- GetAbyss_RogueRegionUis
**Requires:**
- Abyss_RogueScoreByName
- Abyss_BuildTipsLockByName
**Snippet:**
```lua
require("Abyss_RogueScoreByName")
require("Abyss_BuildTipsLockByName")

function GetAbyss_RogueRegionUis(ui)
  local uis = {}
  uis.Score = GetAbyss_RogueScoreUis(ui:GetChild("Score"))
  uis.ScoreRewardBtn = ui:GetChild("ScoreRewardBtn")
  uis.RogueLetterBtn = ui:GetChild("RogueLetterBtn")
  uis.GoBtn = ui:GetChild("GoBtn")
  uis.Lock = GetAbyss_BuildTipsLockUis(ui:GetChild("Lock"))
```

---

## Abyss/Abyss_RogueRewardExpandByName.lua.lua
**Functions:**
- GetAbyss_RogueRewardExpandUis
**Snippet:**
```lua
function GetAbyss_RogueRewardExpandUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_RogueScoreByName.lua.lua
**Functions:**
- GetAbyss_RogueScoreUis
**Snippet:**
```lua
function GetAbyss_RogueScoreUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_RogueScoreRewardBtnByName.lua.lua
**Functions:**
- GetAbyss_RogueScoreRewardBtnUis
**Requires:**
- Abyss_RogueRewardExpandByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("Abyss_RogueRewardExpandByName")
require("CommonResource_RedDotByName")

function GetAbyss_RogueScoreRewardBtnUis(ui)
  local uis = {}
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.RewardExpand = GetAbyss_RogueRewardExpandUis(ui:GetChild("RewardExpand"))
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
```

---

## Abyss/Abyss_SellBtnByName.lua.lua
**Functions:**
- GetAbyss_SellBtnUis
**Snippet:**
```lua
function GetAbyss_SellBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_SellContainerByName.lua.lua
**Functions:**
- GetAbyss_SellContainerUis
**Requires:**
- Abyss_SellTitleByName
- Abyss_TotalPriceStripByName
- Abyss_NothingByName
**Snippet:**
```lua
require("Abyss_SellTitleByName")
require("Abyss_TotalPriceStripByName")
require("Abyss_NothingByName")

function GetAbyss_SellContainerUis(ui)
  local uis = {}
  uis.SellTitle = GetAbyss_SellTitleUis(ui:GetChild("SellTitle"))
  uis.TotalPriceStrip = GetAbyss_TotalPriceStripUis(ui:GetChild("TotalPriceStrip"))
  uis.SellBtn = ui:GetChild("SellBtn")
  uis.DeleteBtn = ui:GetChild("DeleteBtn")
```

---

## Abyss/Abyss_SellItemBtnAniByName.lua.lua
**Functions:**
- GetAbyss_SellItemBtnAniUis
**Snippet:**
```lua
function GetAbyss_SellItemBtnAniUis(ui)
  local uis = {}
  
  uis.SellItemBtn = ui:GetChild("SellItemBtn")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_SellItemBtnByName.lua.lua
**Functions:**
- GetAbyss_SellItemBtnUis
**Snippet:**
```lua
function GetAbyss_SellItemBtnUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_SellOutByName.lua.lua
**Functions:**
- GetAbyss_SellOutUis
**Snippet:**
```lua
function GetAbyss_SellOutUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_SellTitleByName.lua.lua
**Functions:**
- GetAbyss_SellTitleUis
**Snippet:**
```lua
function GetAbyss_SellTitleUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ShopBtnByName.lua.lua
**Functions:**
- GetAbyss_ShopBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetAbyss_ShopBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
```

---

## Abyss/Abyss_ShopByName.lua.lua
**Functions:**
- GetAbyss_ShopUis
**Requires:**
- CommonResource_BackGroundByName
- Abyss_CycleShopByName
- Abyss_FixedShopByName
- Abyss_MaterialSellByName
- Abyss_ExploreShopByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Abyss_CycleShopByName")
require("Abyss_FixedShopByName")
require("Abyss_MaterialSellByName")
require("Abyss_ExploreShopByName")
require("CommonResource_CurrencyReturnByName")

function GetAbyss_ShopUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
```

---

## Abyss/Abyss_ShopEnterAniByName.lua.lua
**Functions:**
- GetAbyss_ShopEnterAniUis
**Snippet:**
```lua
function GetAbyss_ShopEnterAniUis(ui)
  local uis = {}
  
  uis.ShopEnterBtn = ui:GetChild("ShopEnterBtn")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_ShopEnterBtnByName.lua.lua
**Functions:**
- GetAbyss_ShopEnterBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetAbyss_ShopEnterBtnUis(ui)
  local uis = {}
  uis.TimeHolder = ui:GetChild("TimeHolder")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Abyss/Abyss_ShopWindowByName.lua.lua
**Functions:**
- GetAbyss_ShopWindowUis
**Requires:**
- Abyss_ShopByName
**Snippet:**
```lua
require("Abyss_ShopByName")

function GetAbyss_ShopWindowUis(ui)
  local uis = {}
  uis.Main = GetAbyss_ShopUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_SmallMapByName.lua.lua
**Functions:**
- GetAbyss_SmallMapUis
**Requires:**
- Abyss_SmallMapPicByName
**Snippet:**
```lua
require("Abyss_SmallMapPicByName")

function GetAbyss_SmallMapUis(ui)
  local uis = {}
  uis.SmallMapPic = GetAbyss_SmallMapPicUis(ui:GetChild("SmallMapPic"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_SmallMapPicByName.lua.lua
**Functions:**
- GetAbyss_SmallMapPicUis
**Snippet:**
```lua
function GetAbyss_SmallMapPicUis(ui)
  local uis = {}
  
  uis.MapHolder = ui:GetChild("MapHolder")
  uis.MapLoader = ui:GetChild("MapLoader")
  uis.ShadeHolder = ui:GetChild("ShadeHolder")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_SmallMapRegionByName.lua.lua
**Functions:**
- GetAbyss_SmallMapRegionUis
**Requires:**
- Abyss_SmallMapByName
- Abyss_ActionValueByName
- Abyss_ActionValueTipsByName
**Snippet:**
```lua
require("Abyss_SmallMapByName")
require("Abyss_ActionValueByName")
require("Abyss_ActionValueTipsByName")

function GetAbyss_SmallMapRegionUis(ui)
  local uis = {}
  uis.SmallMap = GetAbyss_SmallMapUis(ui:GetChild("SmallMap"))
  uis.ActionValue = GetAbyss_ActionValueUis(ui:GetChild("ActionValue"))
  uis.ActionValueTips = GetAbyss_ActionValueTipsUis(ui:GetChild("ActionValueTips"))
  uis.CloseTipsBtn = ui:GetChild("CloseTipsBtn")
```

---

## Abyss/Abyss_StoryBtnByName.lua.lua
**Functions:**
- GetAbyss_StoryBtnUis
**Requires:**
- Abyss_NewByName
**Snippet:**
```lua
require("Abyss_NewByName")

function GetAbyss_StoryBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetAbyss_NewUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
```

---

## Abyss/Abyss_SuperRegionByName.lua.lua
**Functions:**
- GetAbyss_SuperRegionUis
**Requires:**
- Abyss_Super_TimeByName
- Abyss_BuildTipsEndByName
- Abyss_BuildTipsLockByName
**Snippet:**
```lua
require("Abyss_Super_TimeByName")
require("Abyss_BuildTipsEndByName")
require("Abyss_BuildTipsLockByName")

function GetAbyss_SuperRegionUis(ui)
  local uis = {}
  uis.Time = GetAbyss_Super_TimeUis(ui:GetChild("Time"))
  uis.RewardBtn = ui:GetChild("RewardBtn")
  uis.ProgressList = ui:GetChild("ProgressList")
  uis.GoBtn = ui:GetChild("GoBtn")
```

---

## Abyss/Abyss_Super_ProgressByName.lua.lua
**Functions:**
- GetAbyss_Super_ProgressUis
**Requires:**
- Abyss_Super_ProgressStarByName
- Abyss_Super_ProgressLockByName
**Snippet:**
```lua
require("Abyss_Super_ProgressStarByName")
require("Abyss_Super_ProgressLockByName")

function GetAbyss_Super_ProgressUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Star = GetAbyss_Super_ProgressStarUis(ui:GetChild("Star"))
  uis.Lock = GetAbyss_Super_ProgressLockUis(ui:GetChild("Lock"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## Abyss/Abyss_Super_ProgressLockByName.lua.lua
**Functions:**
- GetAbyss_Super_ProgressLockUis
**Snippet:**
```lua
function GetAbyss_Super_ProgressLockUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_Super_ProgressStarByName.lua.lua
**Functions:**
- GetAbyss_Super_ProgressStarUis
**Snippet:**
```lua
function GetAbyss_Super_ProgressStarUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_Super_RewardBtnByName.lua.lua
**Functions:**
- GetAbyss_Super_RewardBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetAbyss_Super_RewardBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_Super_TimeByName.lua.lua
**Functions:**
- GetAbyss_Super_TimeUis
**Snippet:**
```lua
function GetAbyss_Super_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TabBtnByName.lua.lua
**Functions:**
- GetAbyss_TabBtnUis
**Requires:**
- CommonResource_AbyssSign3ByName
**Snippet:**
```lua
require("CommonResource_AbyssSign3ByName")

function GetAbyss_TabBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.AbyssSign = GetCommonResource_AbyssSign3Uis(ui:GetChild("AbyssSign"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Abyss/Abyss_TabRegionByName.lua.lua
**Functions:**
- GetAbyss_TabRegionUis
**Snippet:**
```lua
function GetAbyss_TabRegionUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TalkAutoBtnByName.lua.lua
**Functions:**
- GetAbyss_TalkAutoBtnUis
**Snippet:**
```lua
function GetAbyss_TalkAutoBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TalkChoiceBtnAniByName.lua.lua
**Functions:**
- GetAbyss_TalkChoiceBtnAniUis
**Snippet:**
```lua
function GetAbyss_TalkChoiceBtnAniUis(ui)
  local uis = {}
  
  uis.TalkChoiceBtn = ui:GetChild("TalkChoiceBtn")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TalkChoiceBtnByName.lua.lua
**Functions:**
- GetAbyss_TalkChoiceBtnUis
**Snippet:**
```lua
function GetAbyss_TalkChoiceBtnUis(ui)
  local uis = {}
  
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TalkEndChoiceBtnAniByName.lua.lua
**Functions:**
- GetAbyss_TalkEndChoiceBtnAniUis
**Snippet:**
```lua
function GetAbyss_TalkEndChoiceBtnAniUis(ui)
  local uis = {}
  
  uis.TalkEndChoiceBtn = ui:GetChild("TalkEndChoiceBtn")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TalkEndChoiceBtnByName.lua.lua
**Functions:**
- GetAbyss_TalkEndChoiceBtnUis
**Snippet:**
```lua
function GetAbyss_TalkEndChoiceBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TalkHead1ByName.lua.lua
**Functions:**
- GetAbyss_TalkHead1Uis
**Requires:**
- Abyss_TalkHeadBgByName
**Snippet:**
```lua
require("Abyss_TalkHeadBgByName")

function GetAbyss_TalkHead1Uis(ui)
  local uis = {}
  uis.HeadBg = GetAbyss_TalkHeadBgUis(ui:GetChild("HeadBg"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TalkHeadBgByName.lua.lua
**Functions:**
- GetAbyss_TalkHeadBgUis
**Snippet:**
```lua
function GetAbyss_TalkHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TalkHeadByName.lua.lua
**Functions:**
- GetAbyss_TalkHeadUis
**Requires:**
- Abyss_TalkHeadBgByName
**Snippet:**
```lua
require("Abyss_TalkHeadBgByName")

function GetAbyss_TalkHeadUis(ui)
  local uis = {}
  uis.HeadBg = GetAbyss_TalkHeadBgUis(ui:GetChild("HeadBg"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TalkLeftAniByName.lua.lua
**Functions:**
- GetAbyss_TalkLeftAniUis
**Requires:**
- Abyss_TalkLeftByName
**Snippet:**
```lua
require("Abyss_TalkLeftByName")

function GetAbyss_TalkLeftAniUis(ui)
  local uis = {}
  uis.Talk = GetAbyss_TalkLeftUis(ui:GetChild("Talk"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TalkLeftByName.lua.lua
**Functions:**
- GetAbyss_TalkLeftUis
**Requires:**
- Abyss_TalkHeadByName
**Snippet:**
```lua
require("Abyss_TalkHeadByName")

function GetAbyss_TalkLeftUis(ui)
  local uis = {}
  uis.Head = GetAbyss_TalkHeadUis(ui:GetChild("Head"))
  uis.WordList = ui:GetChild("WordList")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TalkLeftWordByName.lua.lua
**Functions:**
- GetAbyss_TalkLeftWordUis
**Snippet:**
```lua
function GetAbyss_TalkLeftWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TalkLineByName.lua.lua
**Functions:**
- GetAbyss_TalkLineUis
**Snippet:**
```lua
function GetAbyss_TalkLineUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TalkNextStepBtnByName.lua.lua
**Functions:**
- GetAbyss_TalkNextStepBtnUis
**Snippet:**
```lua
function GetAbyss_TalkNextStepBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TalkProgressByName.lua.lua
**Functions:**
- GetAbyss_TalkProgressUis
**Snippet:**
```lua
function GetAbyss_TalkProgressUis(ui)
  local uis = {}
  
  uis.Progress1Txt = ui:GetChild("Progress1Txt")
  uis.Progress2Txt = ui:GetChild("Progress2Txt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TalkRightAniByName.lua.lua
**Functions:**
- GetAbyss_TalkRightAniUis
**Requires:**
- Abyss_TalkRightByName
**Snippet:**
```lua
require("Abyss_TalkRightByName")

function GetAbyss_TalkRightAniUis(ui)
  local uis = {}
  uis.Talk = GetAbyss_TalkRightUis(ui:GetChild("Talk"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TalkRightByName.lua.lua
**Functions:**
- GetAbyss_TalkRightUis
**Requires:**
- Abyss_TalkHead1ByName
**Snippet:**
```lua
require("Abyss_TalkHead1ByName")

function GetAbyss_TalkRightUis(ui)
  local uis = {}
  uis.Head = GetAbyss_TalkHead1Uis(ui:GetChild("Head"))
  uis.WordList = ui:GetChild("WordList")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TalkRightWordByName.lua.lua
**Functions:**
- GetAbyss_TalkRightWordUis
**Snippet:**
```lua
function GetAbyss_TalkRightWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TalkSkipBtnByName.lua.lua
**Functions:**
- GetAbyss_TalkSkipBtnUis
**Snippet:**
```lua
function GetAbyss_TalkSkipBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TalkSummaryByName.lua.lua
**Functions:**
- GetAbyss_TalkSummaryUis
**Snippet:**
```lua
function GetAbyss_TalkSummaryUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TalkTipsByName.lua.lua
**Functions:**
- GetAbyss_TalkTipsUis
**Requires:**
- Abyss_CardTitleShowByName
- Abyss_TalkProgressByName
- Abyss_TalkSummaryByName
- Abyss_CardPlotTalk_HideByName
**Snippet:**
```lua
require("Abyss_CardTitleShowByName")
require("Abyss_TalkProgressByName")
require("Abyss_TalkSummaryByName")
require("Abyss_CardPlotTalk_HideByName")

function GetAbyss_TalkTipsUis(ui)
  local uis = {}
  uis.CardTitleShow = GetAbyss_CardTitleShowUis(ui:GetChild("CardTitleShow"))
  uis.TalkProgress = GetAbyss_TalkProgressUis(ui:GetChild("TalkProgress"))
  uis.TalkSummary = GetAbyss_TalkSummaryUis(ui:GetChild("TalkSummary"))
```

---

## Abyss/Abyss_TalkWordAniByName.lua.lua
**Functions:**
- GetAbyss_TalkWordAniUis
**Requires:**
- Abyss_TalkWordByName
**Snippet:**
```lua
require("Abyss_TalkWordByName")

function GetAbyss_TalkWordAniUis(ui)
  local uis = {}
  uis.TalkWord = GetAbyss_TalkWordUis(ui:GetChild("TalkWord"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TalkWordBattleAniByName.lua.lua
**Functions:**
- GetAbyss_TalkWordBattleAniUis
**Requires:**
- Abyss_TalkWordBattleByName
**Snippet:**
```lua
require("Abyss_TalkWordBattleByName")

function GetAbyss_TalkWordBattleAniUis(ui)
  local uis = {}
  uis.TalkWordBattle = GetAbyss_TalkWordBattleUis(ui:GetChild("TalkWordBattle"))
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TalkWordBattleByName.lua.lua
**Functions:**
- GetAbyss_TalkWordBattleUis
**Snippet:**
```lua
function GetAbyss_TalkWordBattleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TalkWordByName.lua.lua
**Functions:**
- GetAbyss_TalkWordUis
**Snippet:**
```lua
function GetAbyss_TalkWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TalkWordChoiceByName.lua.lua
**Functions:**
- GetAbyss_TalkWordChoiceUis
**Snippet:**
```lua
function GetAbyss_TalkWordChoiceUis(ui)
  local uis = {}
  
  uis.ChoiceList = ui:GetChild("ChoiceList")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TalkWordRewardByName.lua.lua
**Functions:**
- GetAbyss_TalkWordRewardUis
**Snippet:**
```lua
function GetAbyss_TalkWordRewardUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TaskDirectionBtnByName.lua.lua
**Functions:**
- GetAbyss_TaskDirectionBtnUis
**Requires:**
- Abyss_ArrowByName
**Snippet:**
```lua
require("Abyss_ArrowByName")

function GetAbyss_TaskDirectionBtnUis(ui)
  local uis = {}
  uis.Arrow = GetAbyss_ArrowUis(ui:GetChild("Arrow"))
  uis.DistanceTxt = ui:GetChild("DistanceTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Abyss/Abyss_TipsTypeBgByName.lua.lua
**Functions:**
- GetAbyss_TipsTypeBgUis
**Snippet:**
```lua
function GetAbyss_TipsTypeBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TipsTypeBtnByName.lua.lua
**Functions:**
- GetAbyss_TipsTypeBtnUis
**Snippet:**
```lua
function GetAbyss_TipsTypeBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TotalPriceByName.lua.lua
**Functions:**
- GetAbyss_TotalPriceUis
**Snippet:**
```lua
function GetAbyss_TotalPriceUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_TotalPriceStripByName.lua.lua
**Functions:**
- GetAbyss_TotalPriceStripUis
**Snippet:**
```lua
function GetAbyss_TotalPriceStripUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PriceList = ui:GetChild("PriceList")
  uis.root = ui
  return uis
end
```

---

## Abyss/Abyss_WeatherByName.lua.lua
**Functions:**
- GetAbyss_WeatherUis
**Snippet:**
```lua
function GetAbyss_WeatherUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.PlaceTxt = ui:GetChild("PlaceTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---
