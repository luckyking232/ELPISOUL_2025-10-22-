# Activty

## Activty/ActivityDungeonData.lua.lua
**Functions:**
- ActivityDungeonData.ClearData
- ActivityDungeonData.SaveShowId
- ActivityDungeonData.GetShowId
- ActivityDungeonData.SaveActivityInfo
- ActivityDungeonData.SaveActivityData
- ActivityDungeonData.SetActivityInfo
- ActivityDungeonData.GetActivityInfo
- ActivityDungeonData.GetActivityStageByShowId
- ActivityDungeonData.GetActivityDataByShowId
- ActivityDungeonData.UpdateCreamCount
- ActivityDungeonData.UpdateSignInfo
- ActivityDungeonData.UpdateBoughtItem
- ActivityDungeonData.UpdateOneTask
- ActivityDungeonData.GetActivityData
- ActivityDungeonData.GetAllActivityStage
**Snippet:**
```lua
ActivityDungeonData = {}
local activityConfig = {}
local activityStage = {}
local curShowId

function ActivityDungeonData.ClearData()
  activityConfig = {}
  activityStage = {}
  curShowId = nil
end
```

---

## Activty/ActivityDungeonMgr.lua.lua
**Functions:**
- ActivityDungeonMgr.OpenWindow
- ActivityDungeonMgr.OpenActivityPlotWindow
- ActivityDungeonMgr.GetUnlockPlotId
- ActivityDungeonMgr.GetCurDay
- ActivityDungeonMgr.SaveDay
- ActivityDungeonMgr.MergeItemNum
- ActivityDungeonMgr.CheckActivityEnd
- ActivityDungeonMgr.GetConfigDataByShowId
- ActivityDungeonMgr.GetActivityPlotStoryId
**Snippet:**
```lua
ActivityDungeonMgr = {}

function ActivityDungeonMgr.OpenWindow(showId)
  ActivityDungeonData.SaveShowId(showId)
  local data = ActivityDungeonData.GetActivityData()
  if data then
    if 1 == data.show_id then
      OpenWindow(WinResConfig.ActivityDungeonWindow.name)
    elseif 2 == data.show_id then
      OpenWindow(WinResConfig.Activity2DungeonWindow.name)
```

---

## Activty/ActivityDungeonScriptList.lua.lua
**Requires:**
- ActivityDungeonMgr
- ActivityDungeonService
- ActivityDungeonData
**Snippet:**
```lua
local require = require
require("ActivityDungeonMgr")
require("ActivityDungeonService")
require("ActivityDungeonData")
```

---

## Activty/ActivityDungeonService.lua.lua
**Functions:**
- ActivityDungeonService.Init
- ActivityDungeonService.GetActivityAllReq
- ActivityDungeonService.GetActivityAllRsp
- ActivityDungeonService.ActivityStageSignInReq
- ActivityDungeonService.ActivityStageSignInRsp
- ActivityDungeonService.ActivityStageShopBuyReq
- ActivityDungeonService.ActivityStageShopBuyRsp
- ActivityDungeonService.ActivityStageTaskRewardReq
- ActivityDungeonService.ActivityStageTaskRewardRsp
**Snippet:**
```lua
ActivityDungeonService = {}

function ActivityDungeonService.Init()
  Net.AddListener(Proto.MsgName.GetActivityAllRsp, ActivityDungeonService.GetActivityAllRsp)
  Net.AddListener(Proto.MsgName.ActivityStageSignInRsp, ActivityDungeonService.ActivityStageSignInRsp)
  Net.AddListener(Proto.MsgName.ActivityStageShopBuyRsp, ActivityDungeonService.ActivityStageShopBuyRsp)
  Net.AddListener(Proto.MsgName.ActivityStageTaskRewardRsp, ActivityDungeonService.ActivityStageTaskRewardRsp)
end

function ActivityDungeonService.GetActivityAllReq(rspCallBack)
```

---

## Activty/ActivityDungeonWindow.lua.lua
**Functions:**
- ActivityDungeonWindow.ReInitData
- ActivityDungeonWindow.OnInit
- ActivityDungeonWindow.LoadBg
- ActivityDungeonWindow.InitRedDot
- ActivityDungeonWindow.UpdateInfo
- ActivityDungeonWindow.InitBtnTxt
- ActivityDungeonWindow.InitBtn
- ActivityDungeonWindow.OnShown
- ActivityDungeonWindow.OnClose
- ActivityDungeonWindow.HandleMessage
**Requires:**
- ActivityDungeon1_ActivityDungeonWindowByName
**Snippet:**
```lua
require("ActivityDungeon1_ActivityDungeonWindowByName")
local ActivityDungeonWindow = {}
local uis, contentPane, jumpTb, configData, activityInfo, effect
local InitMiniGameInfo = function()
  local data = ActivityDungeonData.GetActivityData()
  if data.id == 70440001 then
    ld("Activity1_MiniGame")
    Activity1_MiniGameService.MiniGameInfoReq(function()
      RedDotMgr.AddNode({
        windowName = WinResConfig.ActivityDungeonWindow.name,
```

---

## Activty/ActivityMaterialWindow.lua.lua
**Functions:**
- ActivityMaterialWindow.ReInitData
- ActivityMaterialWindow.OnInit
- ActivityMaterialWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- ActivityMaterialWindow.GetChapter
- ActivityMaterialWindow.GetMaxCount
- ActivityMaterialWindow.InitBtn
- ActivityMaterialWindow.CloseWindow
- ActivityMaterialWindow.OnShown
- ActivityMaterialWindow.OnClose
**Requires:**
- ActivityDungeon1_MaterialWindowByName
**Snippet:**
```lua
require("ActivityDungeon1_MaterialWindowByName")
local ActivityMaterialWindow = {}
local uis, contentPane, activityInfo, maxCount, posX

function ActivityMaterialWindow.ReInitData()
end

function ActivityMaterialWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ActivityMaterialWindow.package, WinResConfig.ActivityMaterialWindow.comName, function(com)
    contentPane = com
```

---

## Activty/ActivityMiniGameCountdownWindow.lua.lua
**Functions:**
- ActivityMiniGameCountdownWindow.ReInitData
- ActivityMiniGameCountdownWindow.OnInit
- ActivityMiniGameCountdownWindow.UpdateInfo
- ActivityMiniGameCountdownWindow.InitBtn
- ActivityMiniGameCountdownWindow.OnClose
- ActivityMiniGameCountdownWindow.HandleMessage
**Requires:**
- ActivityDungeon1_MiniStart_CountdownWindowByName
**Snippet:**
```lua
require("ActivityDungeon1_MiniStart_CountdownWindowByName")
local ActivityMiniGameCountdownWindow = {}
local uis, contentPane

function ActivityMiniGameCountdownWindow.ReInitData()
end

function ActivityMiniGameCountdownWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ActivityMiniGameCountdownWindow.package, WinResConfig.ActivityMiniGameCountdownWindow.comName, function(com)
    contentPane = com
```

---

## Activty/ActivityMiniGameEndTipsWindow.lua.lua
**Functions:**
- ActivityMiniGameEndTipsWindow.ReInitData
- ActivityMiniGameEndTipsWindow.OnInit
- ActivityMiniGameEndTipsWindow.UpdateInfo
- ActivityMiniGameEndTipsWindow.InitBtn
- ActivityMiniGameEndTipsWindow.OnClose
**Requires:**
- ActivityDungeon1_MiniStart_EndTipsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1_MiniStart_EndTipsWindowByName")
local ActivityMiniGameEndTipsWindow = {}
local uis, contentPane, callback

function ActivityMiniGameEndTipsWindow.ReInitData()
end

function ActivityMiniGameEndTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ActivityMiniGameEndTipsWindow.package, WinResConfig.ActivityMiniGameEndTipsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/ActivityMiniGameMainWindow.lua.lua
**Functions:**
- ActivityMiniGameMainWindow.ReInitData
- ActivityMiniGameMainWindow.OnInit
- ActivityMiniGameMainWindow.UpdateInfo
- ActivityMiniGameMainWindow.InitBtn
- ActivityMiniGameMainWindow.OnClose
- ActivityMiniGameMainWindow.HandleMessage
**Requires:**
- ActivityDungeon1_MiniGameWindowByName
**Snippet:**
```lua
require("ActivityDungeon1_MiniGameWindowByName")
local ActivityMiniGameMainWindow = {}
local uis, contentPane
ld("Activity1_MiniGame")
local RefreshPanelInfo = function()
  local totalScoreTxt = T(20484)
  local dailyScoreTxt = T(20485)
  local info = Activity1_MiniGameData.GetMiniGameInfo()
  local conf = ActivityDungeonData.GetActivityData()
  local str = conf.game_day_reward[1]
```

---

## Activty/ActivityMiniGameRecordWindow.lua.lua
**Functions:**
- ActivityMiniGameRecordWindow.ReInitData
- ActivityMiniGameRecordWindow.OnInit
- ActivityMiniGameRecordWindow.UpdateInfo
- list.itemRenderer
- itemlist.itemRenderer
- ActivityMiniGameRecordWindow.InitBtn
- ActivityMiniGameRecordWindow.OnClose
**Requires:**
- ActivityDungeon1_MiniIntegralWindowByName
**Snippet:**
```lua
require("ActivityDungeon1_MiniIntegralWindowByName")
local ActivityMiniGameRecordWindow = {}
local uis, contentPane
local FLOWER_URL_LOOKUP = {
  [1] = "ui://ActivityDungeon1/Flower_1001",
  [2] = "ui://ActivityDungeon1/Flower_1002",
  [3] = "ui://ActivityDungeon1/Flower_1003"
}

function ActivityMiniGameRecordWindow.ReInitData()
```

---

## Activty/ActivityMiniGameSubmitWindow.lua.lua
**Functions:**
- ActivityMiniGameSubmitWindow.ReInitData
- ActivityMiniGameSubmitWindow.OnInit
- ActivityMiniGameSubmitWindow.UpdateInfo
- itemlist.itemRenderer
- ActivityMiniGameSubmitWindow.InitBtn
- submitCallback
- ActivityMiniGameSubmitWindow.OnClose
**Requires:**
- ActivityDungeon1_MiniStart_EndRewardWindowByName
**Snippet:**
```lua
require("ActivityDungeon1_MiniStart_EndRewardWindowByName")
local ActivityMiniGameSubmitWindow = {}
local uis, contentPane, submitlist

function ActivityMiniGameSubmitWindow.ReInitData()
end

function ActivityMiniGameSubmitWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ActivityMiniGameSubmitWindow.package, WinResConfig.ActivityMiniGameSubmitWindow.comName, function(com)
    contentPane = com
```

---

## Activty/ActivityMiniGameTaskWindow.lua.lua
**Functions:**
- RefreshRewardList
- list.itemRenderer
- itemlist.itemRenderer
- ActivityMiniGameTaskWindow.ReInitData
- ActivityMiniGameTaskWindow.OnInit
- ActivityMiniGameTaskWindow.UpdateInfo
- ActivityMiniGameTaskWindow.InitBtn
- ActivityMiniGameTaskWindow.OnClose
**Requires:**
- ActivityDungeon1_MiniTaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1_MiniTaskWindowByName")
local ActivityMiniGameTaskWindow = {}
local uis, contentPane

local function RefreshRewardList()
  local info = Activity1_MiniGameData.GetMiniGameInfo()
  local minigame_tasks = info.taskList
  local list = uis.Main.TipsList
  list:SetVirtual()
  
```

---

## Activty/ActivityMiniGameWindow.lua.lua
**Functions:**
- ActivityMiniGameWindow.ReInitData
- ActivityMiniGameWindow.OnInit
- ActivityMiniGameWindow.UpdateInfo
- ActivityMiniGameWindow.InitBtn
- ActivityMiniGameWindow.OnClose
- ActivityMiniGameWindow.HandleMessage
**Requires:**
- ActivityDungeon1_MiniGameStartWindowByName
**Snippet:**
```lua
require("ActivityDungeon1_MiniGameStartWindowByName")
local ActivityMiniGameWindow = {}
local uis, contentPane, submitlist
local controller = Activity1_MiniGameController
local pause, skeletonAnimations, effects
local FLOWER_URL_LOOKUP = {
  [1] = "Assets/Art/Models/UI_spine/prefab/MiniGame/MiniGame001/MiniGame001_flower_001.prefab",
  [2] = "Assets/Art/Models/UI_spine/prefab/MiniGame/MiniGame001/MiniGame001_flower_003.prefab",
  [3] = "Assets/Art/Models/UI_spine/prefab/MiniGame/MiniGame001/MiniGame001_flower_002.prefab"
}
```

---

## Activty/ActivityOpenWindow.lua.lua
**Functions:**
- ActivityOpenWindow.ReInitData
- ActivityOpenWindow.OnInit
- ActivityOpenWindow.UpdateInfo
- ActivityOpenWindow.InitBtn
- ActivityOpenWindow.OnClose
**Requires:**
- Abyss_ActivityOpenWindowByName
**Snippet:**
```lua
require("Abyss_ActivityOpenWindowByName")
local ActivityOpenWindow = {}
local uis, contentPane

function ActivityOpenWindow.ReInitData()
end

function ActivityOpenWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ActivityOpenWindow.package, WinResConfig.ActivityOpenWindow.comName, function(com)
    contentPane = com
```

---

## Activty/ActivityPassportLevelUpTipsWindow.lua.lua
**Functions:**
- ActivityPassportLevelUpTipsWindow.ReInitData
- ActivityPassportLevelUpTipsWindow.OnInit
- ActivityPassportLevelUpTipsWindow.UpdateInfo
- ActivityPassportLevelUpTipsWindow.InitBtn
- ActivityPassportLevelUpTipsWindow.OnClose
**Requires:**
- ActivityDungeon1_PassportUp_LevelUpTipsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1_PassportUp_LevelUpTipsWindowByName")
local ActivityPassportLevelUpTipsWindow = {}
local uis, contentPane, lv

function ActivityPassportLevelUpTipsWindow.ReInitData()
end

function ActivityPassportLevelUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ActivityPassportLevelUpTipsWindow.package, WinResConfig.ActivityPassportLevelUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/ActivityPassportWindow.lua.lua
**Functions:**
- ActivityPassportWindow.ReInitData
- ActivityPassportWindow.OnInit
- ActivityPassportWindow.UpdateTextDisplay
- ActivityPassportWindow.InitPassport
- uis.Main.TabRegion.TabList.itemRenderer
- ActivityPassportWindow.InitEffect
- ActivityPassportWindow.InitLv
- ActivityPassportWindow.ShowLevelUp
- ActivityPassportWindow.SaveLevel
- ActivityPassportWindow.GetRewardByLv
- ActivityPassportWindow.GetRewardNum
- ActivityPassportWindow.IsGetAllReward
- ActivityPassportWindow.ShowReward
- ActivityPassportWindow.GetUpdateLv
- ActivityPassportWindow.RefreshListReward
- ActivityPassportWindow.CheckItemTime
- ActivityPassportWindow.ShowQuitTips
- ActivityPassportWindow.RefreshUI
- ActivityPassportWindow.GetExpMxp
- ActivityPassportWindow.SetLevelInfo
- ActivityPassportWindow.InitList
- list.itemRenderer
- ActivityPassportWindow.SetListPos
- ActivityPassportWindow.RefreshReward
- ActivityPassportWindow.ShowGetEffect
- ActivityPassportWindow.RewardItemClick
- ActivityPassportWindow.IsReward
- ActivityPassportWindow.RefreshRewardFirst
- ActivityPassportWindow.RefreshRewardEnd
- ActivityPassportWindow.ShowState
- ActivityPassportWindow.RefreshRewardShow
- ActivityPassportWindow.RefreshRewardState
- ActivityPassportWindow.PassportActivate
- ActivityPassportWindow.CloseWindow
- ActivityPassportWindow.InitBtn
- ActivityPassportWindow.ShowExpBarAnim
- ActivityPassportWindow.InitTask
- list.itemRenderer
- ActivityPassportWindow.InitClothes
- clothes.BuyReward.RewardList.itemRenderer
- ActivityPassportWindow.SetLastLv
- ActivityPassportWindow.PlayFirstRewardEffect
- ActivityPassportWindow.PlayEndRewardEffect
- ActivityPassportWindow.HandleMessage
- ActivityPassportWindow.OnShown
- ActivityPassportWindow.OnClose
**Requires:**
- ActivityDungeon1_PassportWindowByName
**Snippet:**
```lua
require("ActivityDungeon1_PassportWindowByName")
local ActivityPassportWindow = {}
local uis, contentPane, passInfo, lvMax, modelType, expMax, rewardData, rewardType, rewardLv, listPage, passLv, jumpTb, isShowAllGet, passPortConfig, lvTween, lastLv, waitMessageId, newPassPort, animTween

function ActivityPassportWindow.ReInitData()
end

function ActivityPassportWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ActivityPassportWindow.package, WinResConfig.ActivityPassportWindow.comName, function(com)
    contentPane = com
```

---

## Activty/ActivityPlotCGWindow.lua.lua
**Functions:**
- ActivityPlotCGWindow.ReInitData
- ActivityPlotCGWindow.OnInit
- ActivityPlotCGWindow.UpdateInfo
- list.itemRenderer
- ActivityPlotCGWindow.GetActivityData
- ActivityPlotCGWindow.InitBtn
- ActivityPlotCGWindow.OnClose
**Requires:**
- AbyssActivityPlot_ActivityCGWindowByName
**Snippet:**
```lua
require("AbyssActivityPlot_ActivityCGWindowByName")
local ActivityPlotCGWindow = {}
local uis, contentPane

function ActivityPlotCGWindow.ReInitData()
end

function ActivityPlotCGWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ActivityPlotCGWindow.package, WinResConfig.ActivityPlotCGWindow.comName, function(com)
    contentPane = com
```

---

## Activty/ActivityPlotData.lua.lua
**Functions:**
- ActivityPlotData.SaveActivityData
- ActivityPlotData.GetActivityInfo
- ActivityPlotData.UpdateLockList
- ActivityPlotData.UpdateShop
**Snippet:**
```lua
ActivityPlotData = {}
local info

function ActivityPlotData.SaveActivityData(msg)
  info = msg
end

function ActivityPlotData.GetActivityInfo()
  return info
end
```

---

## Activty/ActivityPlotScriptList.lua.lua
**Requires:**
- ActivityPlotService
- ActivityPlotData
**Snippet:**
```lua
local require = require
require("ActivityPlotService")
require("ActivityPlotData")
```

---

## Activty/ActivityPlotService.lua.lua
**Functions:**
- ActivityPlotService.Init
- ActivityPlotService.GetActivityReviewInfoReq
- ActivityPlotService.GetActivityReviewInfoRsp
- ActivityPlotService.ActivityReviewUnlockReq
- ActivityPlotService.ActivityReviewUnlockRsp
- ActivityPlotService.ActivityReviewShopBuyReq
- ActivityPlotService.ActivityReviewShopBuyRsp
**Snippet:**
```lua
ActivityPlotService = {}

function ActivityPlotService.Init()
  Net.AddListener(Proto.MsgName.GetActivityReviewInfoRsp, ActivityPlotService.GetActivityReviewInfoRsp)
  Net.AddListener(Proto.MsgName.ActivityReviewShopBuyRsp, ActivityPlotService.ActivityReviewShopBuyRsp)
  Net.AddListener(Proto.MsgName.ActivityReviewUnlockRsp, ActivityPlotService.ActivityReviewUnlockRsp)
end

function ActivityPlotService.GetActivityReviewInfoReq(rspCallBack)
  local msg = {}
```

---

## Activty/ActivityPlotShopWindow.lua.lua
**Functions:**
- ActivityPlotShopWindow.ReInitData
- ActivityPlotShopWindow.OnInit
- ActivityPlotShopWindow.GetActivityData
- ActivityPlotShopWindow.UpdateInfo
- uis.Main.ItemList.itemRenderer
- ActivityPlotShopWindow.ShowItem
- list.itemRenderer
- ActivityPlotShopWindow.ShowOneReward
- list.itemRenderer
- ActivityPlotShopWindow.GetShopGrid
- ActivityPlotShopWindow.InitBtn
- ActivityPlotShopWindow.OnClose
- ActivityPlotShopWindow.HandleMessage
**Requires:**
- AbyssActivityPlot_ActivityPlotShopWindowByName
**Snippet:**
```lua
require("AbyssActivityPlot_ActivityPlotShopWindowByName")
local ActivityPlotShopWindow = {}
local uis, contentPane, jumpTb, tempAssetsTips, activityInfo

function ActivityPlotShopWindow.ReInitData()
end

function ActivityPlotShopWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ActivityPlotShopWindow.package, WinResConfig.ActivityPlotShopWindow.comName, function(com)
    contentPane = com
```

---

## Activty/ActivityPlotWindow.lua.lua
**Functions:**
- ActivityPlotWindow.ReInitData
- ActivityPlotWindow.OnInit
- ActivityPlotWindow.UpdateInfo
- list.itemRenderer
- ActivityPlotWindow.InitBtn
- ActivityPlotWindow.CloseWindow
- ActivityPlotWindow.OnClose
**Requires:**
- ActivityDungeon1_PlotWindowByName
**Snippet:**
```lua
require("ActivityDungeon1_PlotWindowByName")
local ActivityPlotWindow = {}
local uis, contentPane, configData

function ActivityPlotWindow.ReInitData()
end

function ActivityPlotWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ActivityPlotWindow.package, WinResConfig.ActivityPlotWindow.comName, function(com)
    contentPane = com
```

---

## Activty/ActivityReturnData.lua.lua
**Snippet:**
```lua
local activInfo
local SetActivityInfo = function(data)
  activInfo = data
end
local GetActivityInfo = function()
  return activInfo
end
local UpdateSignInfo = function(signDay, loginReward)
  if not activInfo then
    return
```

---

## Activty/ActivityReturnMgr.lua.lua
**Snippet:**
```lua
local getD_H = function(timestamp)
  local localTimestamp = timestamp + LoginData.timezoneOffset
  local day = math.floor(localTimestamp / 86400)
  local mod = localTimestamp % 86400
  local hour = mod / 3600 % 24
  return day, hour
end
local GetMultiDroppedEntries = function()
  local activInfo = ActivityReturnData.GetActivityInfo()
  if not activInfo then
```

---

## Activty/ActivityReturnScriptList.lua.lua
**Requires:**
- ActivityReturnData
- ActivityReturnService
- ActivityReturnMgr
**Snippet:**
```lua
ActivityReturnData = require("ActivityReturnData")
ActivityReturnService = require("ActivityReturnService")
ActivityReturnMgr = require("ActivityReturnMgr")
```

---

## Activty/ActivityReturnService.lua.lua
**Snippet:**
```lua
local GetAllActivitiesReq = function(rspCallback)
  Net.Send(Proto.MsgName.GetActivityAllReq, nil, rspCallback)
end
local GetAllActivitiesRsp = function(msg)
  local data = msg.returnProAct
  if type(data) == "table" and _G.next(data) then
    ActivityReturnData.SetActivityInfo(data)
  else
    ActivityReturnData.SetActivityInfo(nil)
  end
```

---

## Activty/ActivityReviewPlotWindow.lua.lua
**Functions:**
- ActivityReviewPlotWindow.ReInitData
- ActivityReviewPlotWindow.OnInit
- ActivityReviewPlotWindow.UpdateInfo
- list.itemRenderer
- ActivityReviewPlotWindow.AssetsTipsList
- ActivityReviewPlotWindow.GetActivityData
- ActivityReviewPlotWindow.InitBtn
- ActivityReviewPlotWindow.OnClose
**Requires:**
- AbyssActivityPlot_ActivityPlotWindowByName
**Snippet:**
```lua
require("AbyssActivityPlot_ActivityPlotWindowByName")
local ActivityReviewPlotWindow = {}
local uis, contentPane, jumpTb, activityNum

function ActivityReviewPlotWindow.ReInitData()
end

function ActivityReviewPlotWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ActivityReviewPlotWindow.package, WinResConfig.ActivityReviewPlotWindow.comName, function(com)
    contentPane = com
```

---

## Activty/ActivityShopWindow.lua.lua
**Functions:**
- ActivityShopWindow.ReInitData
- ActivityShopWindow.OnInit
- ActivityShopWindow.UpdateInfo
- uis.Main.ItemList.itemRenderer
- ActivityShopWindow.ShowItem
- list.itemRenderer
- ActivityShopWindow.ShowOneReward
- list.itemRenderer
- ActivityShopWindow.GetShopGrid
- ActivityShopWindow.InitBtn
- ActivityShopWindow.CloseWindow
- ActivityShopWindow.OnClose
- ActivityShopWindow.HandleMessage
**Requires:**
- ActivityDungeon1_ShopWindowByName
**Snippet:**
```lua
require("ActivityDungeon1_ShopWindowByName")
local ActivityShopWindow = {}
local uis, contentPane, activityInfo, tempAssetsTips

function ActivityShopWindow.ReInitData()
end

function ActivityShopWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ActivityShopWindow.package, WinResConfig.ActivityShopWindow.comName, function(com)
    contentPane = com
```

---

## Activty/ActivitySignWindow.lua.lua
**Functions:**
- ActivitySignWindow.ReInitData
- ActivitySignWindow.OnInit
- ActivitySignWindow.UpdateInfo
- list.RewardList.itemRenderer
- ActivitySignWindow.ShowAllItemFrame
- ActivitySignWindow.GetRewardData
- ActivitySignWindow.InitBtn
- ActivitySignWindow.CloseWindow
- ActivitySignWindow.OnClose
**Requires:**
- ActivityDungeon1_SignWindowByName
**Snippet:**
```lua
require("ActivityDungeon1_SignWindowByName")
local ActivitySignWindow = {}
local uis, contentPane, activityInfo

function ActivitySignWindow.ReInitData()
end

function ActivitySignWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ActivitySignWindow.package, WinResConfig.ActivitySignWindow.comName, function(com)
    contentPane = com
```

---

## Activty/ActivityTaskWindow.lua.lua
**Functions:**
- ActivityTaskWindow.ReInitData
- ActivityTaskWindow.OnInit
- ActivityTaskWindow.UpdateInfo
- list.itemRenderer
- rewardList.itemRenderer
- ActivityTaskWindow.GetRewardNum
- ActivityTaskWindow.ShowAllItemFrame
- ActivityTaskWindow.SortTask
- ActivityTaskWindow.InitBtn
- ActivityTaskWindow.CloseWindow
- ActivityTaskWindow.OnShown
- ActivityTaskWindow.OnClose
**Requires:**
- ActivityDungeon1_TaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1_TaskWindowByName")
local ActivityTaskWindow = {}
local uis, contentPane

function ActivityTaskWindow.ReInitData()
end

function ActivityTaskWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ActivityTaskWindow.package, WinResConfig.ActivityTaskWindow.comName, function(com)
    contentPane = com
```

---
