# EF

## EF/EffectUtil.lua.lua
**Functions:**
- EffectUtil.GetFullPath
- EffectUtil.GetEffectDuration
- EffectUtil.SetAutoDestroyCallback
- EffectUtil.SetEffectSpeed
- EffectUtil.PlayTimeLine
- EffectUtil.PlayTimeLineByName
- EffectUtil.StopTimeLine
- EffectUtil.Overturn
- EffectUtil.GetCurAnimatorName
**Snippet:**
```lua
local EffectUtil = {}
local cachedEffectPath = {}

function EffectUtil.GetFullPath(path)
  if path then
    if nil == cachedEffectPath[path] then
      cachedEffectPath[path] = RES_PATH_PREFIX.EFFECT .. path
    end
    return cachedEffectPath[path]
  end
```

---

## EF/EnergyData.lua.lua
**Snippet:**
```lua
EnergyData = {info = nil}
```

---

## EF/EnergyObtain_CleanBtnByName.lua.lua
**Functions:**
- GetEnergyObtain_CleanBtnUis
**Snippet:**
```lua
function GetEnergyObtain_CleanBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/EnergyObtain_EnergyByName.lua.lua
**Functions:**
- GetEnergyObtain_EnergyUis
**Requires:**
- CommonResource_BackGroundByName
- EnergyObtain_EnergyItemByName
- EnergyObtain_EnergyMunberByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("EnergyObtain_EnergyItemByName")
require("EnergyObtain_EnergyMunberByName")
require("CommonResource_CurrencyReturnByName")

function GetEnergyObtain_EnergyUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.UseBtn = ui:GetChild("UseBtn")
  uis.EnergyBuy = GetEnergyObtain_EnergyItemUis(ui:GetChild("EnergyBuy"))
```

---

## EF/EnergyObtain_EnergyItemBtnByName.lua.lua
**Functions:**
- GetEnergyObtain_EnergyItemBtnUis
**Requires:**
- EnergyObtain_SurplusDayByName
**Snippet:**
```lua
require("EnergyObtain_SurplusDayByName")

function GetEnergyObtain_EnergyItemBtnUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.SurplusDay = GetEnergyObtain_SurplusDayUis(ui:GetChild("SurplusDay"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.LimitTxt = ui:GetChild("LimitTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## EF/EnergyObtain_EnergyItemByName.lua.lua
**Functions:**
- GetEnergyObtain_EnergyItemUis
**Snippet:**
```lua
function GetEnergyObtain_EnergyItemUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.EnergyItemBtn = ui:GetChild("EnergyItemBtn")
  uis.CleanBtn = ui:GetChild("CleanBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/EnergyObtain_EnergyMunberByName.lua.lua
**Functions:**
- GetEnergyObtain_EnergyMunberUis
**Requires:**
- EnergyObtain_RecoveryTimeByName
**Snippet:**
```lua
require("EnergyObtain_RecoveryTimeByName")

function GetEnergyObtain_EnergyMunberUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.RecoveryTime1 = GetEnergyObtain_RecoveryTimeUis(ui:GetChild("RecoveryTime1"))
  uis.RecoveryTime2 = GetEnergyObtain_RecoveryTimeUis(ui:GetChild("RecoveryTime2"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## EF/EnergyObtain_EnergyWindowByName.lua.lua
**Functions:**
- GetEnergyObtain_EnergyWindowUis
**Requires:**
- EnergyObtain_EnergyByName
**Snippet:**
```lua
require("EnergyObtain_EnergyByName")

function GetEnergyObtain_EnergyWindowUis(ui)
  local uis = {}
  uis.Main = GetEnergyObtain_EnergyUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/EnergyObtain_RecoveryTimeByName.lua.lua
**Functions:**
- GetEnergyObtain_RecoveryTimeUis
**Snippet:**
```lua
function GetEnergyObtain_RecoveryTimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/EnergyObtain_SurplusDayByName.lua.lua
**Functions:**
- GetEnergyObtain_SurplusDayUis
**Snippet:**
```lua
function GetEnergyObtain_SurplusDayUis(ui)
  local uis = {}
  
  uis.DayTxt = ui:GetChild("DayTxt")
  uis.root = ui
  return uis
end
```

---

## EF/EnergyObtain_UseBtnByName.lua.lua
**Functions:**
- GetEnergyObtain_UseBtnUis
**Snippet:**
```lua
function GetEnergyObtain_UseBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/EnergyScriptList.lua.lua
**Requires:**
- EnergyData
- EnergyService
**Snippet:**
```lua
local require = require
require("EnergyData")
require("EnergyService")
```

---

## EF/EnergyService.lua.lua
**Functions:**
- EnergyService.Init
- EnergyService.GetEnergyRecoverInfoReq
- EnergyService.GetEnergyRecoverInfoRsp
- EnergyService.BuyCountResourceReq
- EnergyService.BuyCountResourceRsp
- EnergyService.ExchangeEnergyReq
- EnergyService.ExchangeEnergyRsp
**Snippet:**
```lua
EnergyService = {}

function EnergyService.Init()
  Net.AddListener(Proto.MsgName.GetEnergyRecoverInfoRsp, EnergyService.GetEnergyRecoverInfoRsp)
  Net.AddListener(Proto.MsgName.BuyCountResourceRsp, EnergyService.BuyCountResourceRsp)
  Net.AddListener(Proto.MsgName.ExchangeEnergyRsp, EnergyService.ExchangeEnergyRsp)
end

function EnergyService.GetEnergyRecoverInfoReq()
  local msg = {}
```

---

## EF/EnergyWindow.lua.lua
**Functions:**
- EnergyWindow.OnInit
- EnergyWindow.GetEnergyMax
- EnergyWindow.GetCostIds
- EnergyWindow.InitBgPrefab
- EnergyWindow.StopTween
- EnergyWindow.SetEnergyAlpha
- EnergyWindow.Split
- EnergyWindow.GetIdByPos
- EnergyWindow.GetItemCountByExpire
- EnergyWindow.ShowItem
- EnergyWindow.InitUI
- EnergyWindow.UpdateTime
- EnergyWindow.SetLongPressGesture
- EnergyWindow.FormatTime
- EnergyWindow.InitTime
- EnergyWindow.RefreshUI
- EnergyWindow.IsPitchOn
- EnergyWindow.AddItemClick
- EnergyWindow.GetOneCostNum
- EnergyWindow.GetEffectNum
- EnergyWindow.CleanItemClick
- EnergyWindow.ShowDay
- EnergyWindow.ShowEffect
- EnergyWindow.GetAllEnergy
- EnergyWindow.InitBtn
- EnergyWindow.SetAlpha
- EnergyWindow.HandleMessage
- EnergyWindow.OnClose
**Requires:**
- EnergyObtain_EnergyWindowByName
**Snippet:**
```lua
require("EnergyObtain_EnergyWindowByName")
local EnergyWindow = {}
local uis, contentPane, bgPrefab, middle_press, red_screen, line, press, spine, itemNum, cost, reward, getEnergy
local costId = {}
local itemUid = {}
local costData, curIndex
local energyNum = {}
local maskImage, downTime, energyMax, longPressStop, isMax, tween, itemEffect, jumpTb

function EnergyWindow.OnInit(bridgeObj)
```

---

## EF/EnterClampUtil.lua.lua
**Functions:**
- EnterClampUtil.WhetherToEnter
- EnterClampUtil.Init
- EnterClampUtil.CheckUnlockInfoFromServer
- EnterClampUtil.RemoveNeedGetInfoList
- EnterClampUtil.CheckBackHome
- EnterClampUtil.CheckNewFeature
- EnterClampUtil.UpdateEntranceState
- EnterClampUtil.TestBadgeCondition
- EnterClampUtil.Clear
**Snippet:**
```lua
local EnterClampUtil = {
  needGetFromServer = {}
}
local lastLv = 0

function EnterClampUtil.WhetherToEnter(id, floatTips, level)
  if nil == level and ActorData.GetFeatureIsUnlock(id) then
    return true
  end
  local data = TableData.GetConfig(id, "BaseFeature")
```

---

## EF/ErrorCode.lua.lua
**Functions:**
- ErrorCode.DealError
**Snippet:**
```lua
local ErrorCode = {}

function ErrorCode.DealError(errorCode)
  local RET_CODE = ProtoEnum.RET_CODE
  if errorCode == RET_CODE.RC_TOKEN_INVALID or errorCode == RET_CODE.RC_TOKEN_EXPIRE or errorCode == RET_CODE.RC_TOKEN_NOT_AUTHED or errorCode == RET_CODE.RC_TOKEN_ILLEGAL then
    LoginMgr.ConnectSDKAuth()
  end
end

return ErrorCode
```

---

## EF/EventHelper.lua.lua
**Functions:**
- EventHelper.innerAddListener
- EventHelper.AddListener
- EventHelper.AddOnceListener
- EventHelper.Dispatch
- EventHelper.CSCallLuaDispatch
- EventHelper.removeFromCS
- EventHelper.innerRemoveListener
- EventHelper.RemoveListener
- EventHelper.RemoveOnceListener
**Requires:**
- Handler
**Snippet:**
```lua
require("Handler")
local csEventDis = CS.EventDispatcher.Singleton
local EventHelper = {}
local eventTable = GetNewHandler()
local onceEventTable = GetNewHandler()

function EventHelper.innerAddListener(eventid, func, tableobj, once)
  if once then
    csEventDis:AddLuaListenerOnce(eventid)
    onceEventTable:AddHandle(eventid, func, tableobj)
```

---

## EF/EventID.lua.lua
**Snippet:**
```lua
local csEventID = CS.EventID
EventID = {DoQuset = 6000100}
setmetatable(EventID, {
  __index = function(t, k)
    local value = csEventID[k]
    if nil ~= value then
      t[k] = value
      return value
    end
  end
```

---

## EF/EventPopWindow.lua.lua
**Functions:**
- EventPopWindow.ReInitData
- EventPopWindow.OnInit
- EventPopWindow.UpdateInfo
- EventPopWindow.InitBtn
- EventPopWindow.OnHide
- EventPopWindow.OnClose
- EventPopWindow.HandleMessage
**Requires:**
- Abyss_EventPopWindowByName
**Snippet:**
```lua
require("Abyss_EventPopWindowByName")
local EventPopWindow = {}
local uis, contentPane, argsTbl, eventGoCache, eventInfo, ensureCallback

function EventPopWindow.ReInitData()
end

function EventPopWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.EventPopWindow.package, WinResConfig.EventPopWindow.comName, function(com)
    contentPane = com
```

---

## EF/ExpeditionBattleBuffLookWindow.lua.lua
**Functions:**
- ExpeditionBattleBuffLookWindow.ReInitData
- ExpeditionBattleBuffLookWindow.OnInit
- ExpeditionBattleBuffLookWindow.UpdateInfo
- list.itemRenderer
- wordList.itemRenderer
- ExpeditionBattleBuffLookWindow.InitBtn
- ExpeditionBattleBuffLookWindow.OnClose
**Requires:**
- Expedition_BattleBuffLookWindowByName
**Snippet:**
```lua
require("Expedition_BattleBuffLookWindowByName")
local ExpeditionBattleBuffLookWindow = {}
local uis, contentPane
local trans_intvl = 0.04

function ExpeditionBattleBuffLookWindow.ReInitData()
end

function ExpeditionBattleBuffLookWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ExpeditionBattleBuffLookWindow.package, WinResConfig.ExpeditionBattleBuffLookWindow.comName, function(com)
```

---

## EF/ExpeditionBattleChoiceWindow.lua.lua
**Functions:**
- RefreshLevelSelectedPanel
- maplist.itemRenderer
- EnterLevelSelected
- ExpeditionBattleChoiceWindow.ReInitData
- ExpeditionBattleChoiceWindow.OnInit
- ExpeditionBattleChoiceWindow.UpdateInfo
- ExpeditionBattleChoiceWindow.InitBtn
- ExpeditionBattleChoiceWindow.OnClose
**Requires:**
- Expedition_BattleChoiceWindowByName
**Snippet:**
```lua
require("Expedition_BattleChoiceWindowByName")
local ExpeditionBattleChoiceWindow = {}
local uis, contentPane, bgEffect, bgTree_gameObject, bgTree_animator, bgTree_timeline, tree_children, playing, selectedChapterIndex
local stageEntrance_eff_boss = "Assets/Art/Effects/Prefab/UI_prefab/Expedition/FX_ui_expedition_icon_boss.prefab"
local stageEntrance_eff_normal = "Assets/Art/Effects/Prefab/UI_prefab/Expedition/FX_ui_expedition_icon_normal.prefab"
local stageEntrance_eff_complete = "Assets/Art/Effects/Prefab/UI_prefab/Expedition/FX_ui_expedition_icon_end.prefab"
local EnterLevelSelected, RefreshLevelSelectedPanel

function RefreshLevelSelectedPanel(expedData, chapterIndex, play_animation)
  local animator = bgTree_animator
```

---

## EF/ExpeditionBattleReviewWindow.lua.lua
**Functions:**
- detaillist.itemRenderer
- headlist.itemRenderer
- RefreshRecords
- ExpeditionBattleReviewWindow.ReInitData
- ExpeditionBattleReviewWindow.OnInit
- ExpeditionBattleReviewWindow.UpdateInfo
- ExpeditionBattleReviewWindow.InitBtn
- ExpeditionBattleReviewWindow.OnClose
**Requires:**
- Expedition_BattleReviewWindowByName
**Snippet:**
```lua
require("Expedition_BattleReviewWindowByName")
local ExpeditionBattleReviewWindow = {}
local uis, contentPane, selectedChapterIndex, RefreshRecords
local Seconds2TimeStr = function(seconds)
  local minutes = math.floor(seconds / 60)
  seconds = math.floor(seconds % 60)
  return string.format("%02d:%02d", minutes, seconds)
end
local Frames2TimeStr = function(frames)
  local seconds = frames / BATTLE_CONFIG_ENUM.FIXED_FPS
```

---

## EF/ExpeditionBattleStageWindow.lua.lua
**Functions:**
- RefreshBuffPagePanel
- RefreshBuffChoicePanel
- list.itemRenderer
- RefreshStagePanel
- maplist.itemRenderer
- dotlist.itemRenderer
- EnterStagePanel
- ReverseTransition
- RefreshBuffEnsurePanel
- list.itemRenderer
- wordList.itemRenderer
- RefreshBuffRecordPanel
- list.itemRenderer
- wordList.itemRenderer
- RefreshPanelState
- ExpeditionBattleStageWindow.ReInitData
- ExpeditionBattleStageWindow.OnInit
- ExpeditionBattleStageWindow.UpdateInfo
- ExpeditionBattleStageWindow.InitBtn
- ExpeditionBattleStageWindow.OnShown
- ExpeditionBattleStageWindow.OnClose
- ExpeditionBattleStageWindow.HandleMessage
**Requires:**
- Expedition_BattleStageWindowByName
**Snippet:**
```lua
require("Expedition_BattleStageWindowByName")
local ExpeditionBattleStageWindow = {}
local uis, contentPane
local maxBuffNum = 4
local trans_intvl = 0.04
local bgEffect, bgTimeline, bgTree_Go, bgTree_animator, tree_Objs, RefreshStagePanel, EnterStagePanel, ReverseTransition, RefreshPanelState, RefreshBuffEnsurePanel, RefreshBuffRecordPanel, RefreshBuffPagePanel, RefreshBuffChoicePanel, buffComponents, buffClickEffects, originPos, tweenTimer
local transitions = {
  [1] = "fang",
  [2] = "jin",
  [3] = "tu",
```

---

## EF/ExpeditionBuffTipsWindow.lua.lua
**Functions:**
- ExpeditionBuffTipsWindow.ReInitData
- ExpeditionBuffTipsWindow.OnInit
- ExpeditionBuffTipsWindow.UpdateInfo
- ExpeditionBuffTipsWindow.InitBtn
- ExpeditionBuffTipsWindow.OnClose
**Requires:**
- Expedition_BuffTipsWindowByName
**Snippet:**
```lua
require("Expedition_BuffTipsWindowByName")
local ExpeditionBuffTipsWindow = {}
local uis, contentPane

function ExpeditionBuffTipsWindow.ReInitData()
end

function ExpeditionBuffTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ExpeditionBuffTipsWindow.package, WinResConfig.ExpeditionBuffTipsWindow.comName, function(com)
    contentPane = com
```

---

## EF/ExpeditionData.lua.lua
**Snippet:**
```lua
local expedData, curStageInfo, gotRewards, stageBattleRecords
local SetCurStageInfo = function(curStage)
  curStageInfo = curStageInfo or {}
  curStageInfo.id = curStage
  local stageConf = TableData.GetConfig(curStage, "BaseStage")
  if stageConf then
    curStageInfo.monsterGroup = stageConf.monster_group_list
  end
end
local SetRewardsInfo = function(rewards)
```

---

## EF/ExpeditionEndWindow.lua.lua
**Functions:**
- list.itemRenderer
- ExpeditionEndWindow.ReInitData
- ExpeditionEndWindow.OnInit
- ExpeditionEndWindow.UpdateInfo
- ExpeditionEndWindow.InitBtn
- ExpeditionEndWindow.OnClose
**Requires:**
- Expedition_ExpeditionEndWindowByName
**Snippet:**
```lua
require("Expedition_ExpeditionEndWindowByName")
local ExpeditionEndWindow = {}
local uis, contentPane
local DISPLAY_TYPE = {DEFAULT = 0, DETAILED = 1}
local curDisplayType, stateSnapshot
local RefreshSummeryPanel = function(displayType, playTrans)
  local numPerRow = 8
  local lists = {
    [1] = uis.Main.Card1List,
    [2] = uis.Main.Card2List,
```

---

## EF/ExpeditionGiveUpWindow.lua.lua
**Functions:**
- ExpeditionGiveUpWindow.ReInitData
- ExpeditionGiveUpWindow.OnInit
- ExpeditionGiveUpWindow.UpdateInfo
- ExpeditionGiveUpWindow.InitBtn
- ExpeditionGiveUpWindow.OnClose
**Requires:**
- Expedition_GiveUpWindowByName
**Snippet:**
```lua
require("Expedition_GiveUpWindowByName")
local ExpeditionGiveUpWindow = {}
local uis, contentPane

function ExpeditionGiveUpWindow.ReInitData()
end

function ExpeditionGiveUpWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ExpeditionGiveUpWindow.package, WinResConfig.ExpeditionGiveUpWindow.comName, function(com)
    contentPane = com
```

---

## EF/ExpeditionMgr.lua.lua
**Snippet:**
```lua
local GetClearedNumStages = function()
  local expedData = ExpeditionData.GetData()
  local curStage = expedData.curStage
  local chapters = expedData.chapters
  local records = expedData.records
  local stageOffset, stageCount = 0, 0
  for i, v in ipairs(chapters) do
    local chapterConf = TableData.GetConfig(v.chapterId, "BaseChapter")
    local stages = chapterConf.stages
    if -1 == curStage then
```

---

## EF/ExpeditionRewardWindow.lua.lua
**Functions:**
- rewradlist.itemRenderer
- itemlist.itemRenderer
- ExpeditionRewardWindow.ReInitData
- ExpeditionRewardWindow.OnInit
- ExpeditionRewardWindow.UpdateInfo
- ExpeditionRewardWindow.InitBtn
- ExpeditionRewardWindow.OnClose
- ExpeditionRewardWindow.HandleMessage
**Requires:**
- Expedition_RewardWindowByName
**Snippet:**
```lua
require("Expedition_RewardWindowByName")
local ExpeditionRewardWindow = {}
local uis, contentPane
local locked_eff = "Assets/Art/Effects/Prefab/UI_prefab/Expedition/FX_ui_expedition_geticon_get.prefab"
local unlocked_eff = "Assets/Art/Effects/Prefab/UI_prefab/Expedition/FX_ui_expedition_geticon_unget.prefab"
local RefreshRewardsInfo = function()
  local expedData = ExpeditionData.GetData()
  local gotRewards = ExpeditionData.GetRewardsInfo()
  local numStars = expedData.highPassStar
  local rewradlist = uis.Main.RewardList
```

---

## EF/ExpeditionScriptList.lua.lua
**Requires:**
- ExpeditionMgr
- ExpeditionData
- ExpeditionService
**Snippet:**
```lua
local require = require
ExpeditionMgr = require("ExpeditionMgr")
ExpeditionData = require("ExpeditionData")
ExpeditionService = require("ExpeditionService")
ExpeditionService.Init()
```

---

## EF/ExpeditionService.lua.lua
**Snippet:**
```lua
local GetExpeditionInfoReq = function(rspCallback)
  Net.Send(Proto.MsgName.GetExpeditionInfoReq, nil, rspCallback)
end
local GetExpeditionInfoRsp = function(msg)
  local data_refresh = false
  local curData = ExpeditionData.GetData()
  if curData then
    local curNextRefreshTimestamp = curData.nextRefreshStamp
    if curNextRefreshTimestamp ~= msg.nextRefreshStamp then
      data_refresh = true
```

---

## EF/ExpeditionStageWindow.lua.lua
**Functions:**
- ExpeditionStageWindow.ReInitData
- ExpeditionStageWindow.OnInit
- ExpeditionStageWindow.UpdateInfo
- goallist.itemRenderer
- ExpeditionStageWindow.InitBtn
- ExpeditionStageWindow.OnClose
**Requires:**
- Expedition_ArrangeWindowByName
**Snippet:**
```lua
require("Expedition_ArrangeWindowByName")
local ExpeditionStageWindow = {}
local uis, contentPane, buffId, stageId, stageIndex

function ExpeditionStageWindow.ReInitData()
end

local jumpTb

function ExpeditionStageWindow.OnInit(bridgeObj)
```

---

## EF/ExpeditionWindow.lua.lua
**Functions:**
- ExpeditionWindow.ReInitData
- ExpeditionWindow.OnInit
- ExpeditionWindow.InitWithData
- ExpeditionWindow.UpdateInfo
- ExpeditionWindow.InitBtn
- ExpeditionWindow.OnShown
- ExpeditionWindow.OnHide
- ExpeditionWindow.OnClose
- ExpeditionWindow.HandleMessage
**Requires:**
- Expedition_ExpeditionWindowByName
**Snippet:**
```lua
require("Expedition_ExpeditionWindowByName")
local ExpeditionWindow = {}
local uis, contentPane
local bg_fx_path = "Assets/Art/Effects/Prefab/UI_prefab/Bosschallenge/FX_ui_Bosschallenge_opbg.prefab"
local LoadBgEffect = function(holder)
  local o = ResourceManager.Instantiate(bg_fx_path)
  holder.pivot = Vector2(0.5, 0.5)
  UIUtil.SetObjectToUI(o, holder, 10000)
  o.transform.localPosition = Vector3.zero
end
```

---

## EF/Expedition_ArrangeByName.lua.lua
**Functions:**
- GetExpedition_ArrangeUis
**Requires:**
- CommonResource_BackGroundByName
- Expedition_ArrangeLevelByName
- Expedition_ArrangeTips1ByName
- Expedition_ArrangeTips2ByName
- Expedition_ArrangeTips3ByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Expedition_ArrangeLevelByName")
require("Expedition_ArrangeTips1ByName")
require("Expedition_ArrangeTips2ByName")
require("Expedition_ArrangeTips3ByName")
require("CommonResource_CurrencyReturnByName")

function GetExpedition_ArrangeUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
```

---

## EF/Expedition_ArrangeLevelByName.lua.lua
**Functions:**
- GetExpedition_ArrangeLevelUis
**Snippet:**
```lua
function GetExpedition_ArrangeLevelUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_ArrangeStartBtnByName.lua.lua
**Functions:**
- GetExpedition_ArrangeStartBtnUis
**Snippet:**
```lua
function GetExpedition_ArrangeStartBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_ArrangeTips1ByName.lua.lua
**Functions:**
- GetExpedition_ArrangeTips1Uis
**Snippet:**
```lua
function GetExpedition_ArrangeTips1Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_ArrangeTips2ByName.lua.lua
**Functions:**
- GetExpedition_ArrangeTips2Uis
**Requires:**
- Expedition_ArrangeTips2_1ByName
**Snippet:**
```lua
require("Expedition_ArrangeTips2_1ByName")

function GetExpedition_ArrangeTips2Uis(ui)
  local uis = {}
  uis.Title = GetExpedition_ArrangeTips2_1Uis(ui:GetChild("Title"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_ArrangeTips2_1ByName.lua.lua
**Functions:**
- GetExpedition_ArrangeTips2_1Uis
**Snippet:**
```lua
function GetExpedition_ArrangeTips2_1Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_ArrangeTips2_2ByName.lua.lua
**Functions:**
- GetExpedition_ArrangeTips2_2Uis
**Snippet:**
```lua
function GetExpedition_ArrangeTips2_2Uis(ui)
  local uis = {}
  
  uis.WordTxtTxt = ui:GetChild("WordTxtTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_ArrangeTips3ByName.lua.lua
**Functions:**
- GetExpedition_ArrangeTips3Uis
**Snippet:**
```lua
function GetExpedition_ArrangeTips3Uis(ui)
  local uis = {}
  
  uis.WaveTxt = ui:GetChild("WaveTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.CardList = ui:GetChild("CardList")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_ArrangeTips3_1ByName.lua.lua
**Functions:**
- GetExpedition_ArrangeTips3_1Uis
**Requires:**
- Expedition_ReviewTips2_2BgByName
**Snippet:**
```lua
require("Expedition_ReviewTips2_2BgByName")

function GetExpedition_ArrangeTips3_1Uis(ui)
  local uis = {}
  uis.HeadBg = GetExpedition_ReviewTips2_2BgUis(ui:GetChild("HeadBg"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_ArrangeWindowByName.lua.lua
**Functions:**
- GetExpedition_ArrangeWindowUis
**Requires:**
- Expedition_ArrangeByName
**Snippet:**
```lua
require("Expedition_ArrangeByName")

function GetExpedition_ArrangeWindowUis(ui)
  local uis = {}
  uis.Main = GetExpedition_ArrangeUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_BattleChoiceBuffBtnByName.lua.lua
**Functions:**
- GetExpedition_BattleChoiceBuffBtnUis
**Snippet:**
```lua
function GetExpedition_BattleChoiceBuffBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_BattleChoiceByName.lua.lua
**Functions:**
- GetExpedition_BattleChoiceUis
**Requires:**
- CommonResource_BackGroundByName
- Expedition_ChoiceTabRegionByName
- Expedition_BattleChoiceTitleByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Expedition_ChoiceTabRegionByName")
require("Expedition_BattleChoiceTitleByName")
require("CommonResource_CurrencyReturnByName")

function GetExpedition_BattleChoiceUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.MapList = ui:GetChild("MapList")
  uis.RewardBtn = ui:GetChild("RewardBtn")
```

---

## EF/Expedition_BattleChoiceTitleByName.lua.lua
**Functions:**
- GetExpedition_BattleChoiceTitleUis
**Snippet:**
```lua
function GetExpedition_BattleChoiceTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.BuffBtn = ui:GetChild("BuffBtn")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_BattleChoiceWindowByName.lua.lua
**Functions:**
- GetExpedition_BattleChoiceWindowUis
**Requires:**
- Expedition_BattleChoiceByName
**Snippet:**
```lua
require("Expedition_BattleChoiceByName")

function GetExpedition_BattleChoiceWindowUis(ui)
  local uis = {}
  uis.Main = GetExpedition_BattleChoiceUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_BattleReviewByName.lua.lua
**Functions:**
- GetExpedition_BattleReviewUis
**Requires:**
- CommonResource_BackGroundByName
- Expedition_ReviewTabRegionByName
- Expedition_ReviewTitleByName
- Expedition_ReviewProgressByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Expedition_ReviewTabRegionByName")
require("Expedition_ReviewTitleByName")
require("Expedition_ReviewProgressByName")
require("CommonResource_CurrencyReturnByName")

function GetExpedition_BattleReviewUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.ReviewTabRegion = GetExpedition_ReviewTabRegionUis(ui:GetChild("ReviewTabRegion"))
```

---

## EF/Expedition_BattleReviewWindowByName.lua.lua
**Functions:**
- GetExpedition_BattleReviewWindowUis
**Requires:**
- Expedition_BattleReviewByName
**Snippet:**
```lua
require("Expedition_BattleReviewByName")

function GetExpedition_BattleReviewWindowUis(ui)
  local uis = {}
  uis.Main = GetExpedition_BattleReviewUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_BuffTipsBgByName.lua.lua
**Functions:**
- GetExpedition_BuffTipsBgUis
**Snippet:**
```lua
function GetExpedition_BuffTipsBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_BuffTipsByName.lua.lua
**Functions:**
- GetExpedition_BuffTipsUis
**Requires:**
- CommonResource_PopupBgByName
- Expedition_BuffTipsBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Expedition_BuffTipsBgByName")

function GetExpedition_BuffTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.BuffTipsBg = GetExpedition_BuffTipsBgUis(ui:GetChild("BuffTipsBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
```

---

## EF/Expedition_BuffTipsWindowByName.lua.lua
**Functions:**
- GetExpedition_BuffTipsWindowUis
**Requires:**
- Expedition_BuffTipsByName
**Snippet:**
```lua
require("Expedition_BuffTipsByName")

function GetExpedition_BuffTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetExpedition_BuffTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_ChoiceTabBtnByName.lua.lua
**Functions:**
- GetExpedition_ChoiceTabBtnUis
**Requires:**
- Expedition_ChoiceTabLockByName
**Snippet:**
```lua
require("Expedition_ChoiceTabLockByName")

function GetExpedition_ChoiceTabBtnUis(ui)
  local uis = {}
  uis.n9 = GetExpedition_ChoiceTabLockUis(ui:GetChild("n9"))
  uis.NumbetTxt = ui:GetChild("NumbetTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## EF/Expedition_ChoiceTabLockByName.lua.lua
**Functions:**
- GetExpedition_ChoiceTabLockUis
**Snippet:**
```lua
function GetExpedition_ChoiceTabLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_ChoiceTabRegionByName.lua.lua
**Functions:**
- GetExpedition_ChoiceTabRegionUis
**Snippet:**
```lua
function GetExpedition_ChoiceTabRegionUis(ui)
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

## EF/Expedition_CoverProgressByName.lua.lua
**Functions:**
- GetExpedition_CoverProgressUis
**Snippet:**
```lua
function GetExpedition_CoverProgressUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_CoverReviewBtnByName.lua.lua
**Functions:**
- GetExpedition_CoverReviewBtnUis
**Snippet:**
```lua
function GetExpedition_CoverReviewBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_CoverRewardBtnByName.lua.lua
**Functions:**
- GetExpedition_CoverRewardBtnUis
**Snippet:**
```lua
function GetExpedition_CoverRewardBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_CoverStartBtnByName.lua.lua
**Functions:**
- GetExpedition_CoverStartBtnUis
**Requires:**
- Expedition_CoverProgressByName
**Snippet:**
```lua
require("Expedition_CoverProgressByName")

function GetExpedition_CoverStartBtnUis(ui)
  local uis = {}
  uis.CoverProgress = GetExpedition_CoverProgressUis(ui:GetChild("CoverProgress"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## EF/Expedition_CoverTimeByName.lua.lua
**Functions:**
- GetExpedition_CoverTimeUis
**Snippet:**
```lua
function GetExpedition_CoverTimeUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.Time1Txt = ui:GetChild("Time1Txt")
  uis.Time2Txt = ui:GetChild("Time2Txt")
  uis.EndTipsTxt = ui:GetChild("EndTipsTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## EF/Expedition_CoverTitleByName.lua.lua
**Functions:**
- GetExpedition_CoverTitleUis
**Snippet:**
```lua
function GetExpedition_CoverTitleUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_Expedition1ByName.lua.lua
**Functions:**
- GetExpedition_Expedition1Uis
**Requires:**
- CommonResource_BackGroundByName
- Expedition_CoverTitleByName
- Expedition_CoverTimeByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Expedition_CoverTitleByName")
require("Expedition_CoverTimeByName")
require("CommonResource_CurrencyReturnByName")

function GetExpedition_Expedition1Uis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.CoverTitle = GetExpedition_CoverTitleUis(ui:GetChild("CoverTitle"))
  uis.CoverStartBtn = ui:GetChild("CoverStartBtn")
```

---

## EF/Expedition_Expedition2ByName.lua.lua
**Functions:**
- GetExpedition_Expedition2Uis
**Requires:**
- Expedition_Expedition1ByName
**Snippet:**
```lua
require("Expedition_Expedition1ByName")

function GetExpedition_Expedition2Uis(ui)
  local uis = {}
  uis.Expedition1 = GetExpedition_Expedition1Uis(ui:GetChild("Expedition1"))
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_ExpeditionWindowByName.lua.lua
**Functions:**
- GetExpedition_ExpeditionWindowUis
**Requires:**
- Expedition_Expedition2ByName
**Snippet:**
```lua
require("Expedition_Expedition2ByName")

function GetExpedition_ExpeditionWindowUis(ui)
  local uis = {}
  uis.Main = GetExpedition_Expedition2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_Map1ByName.lua.lua
**Functions:**
- GetExpedition_Map1Uis
**Requires:**
- Expedition_MapTipsAniByName
**Snippet:**
```lua
require("Expedition_MapTipsAniByName")

function GetExpedition_Map1Uis(ui)
  local uis = {}
  uis.Tips1 = GetExpedition_MapTipsAniUis(ui:GetChild("Tips1"))
  uis.Tips2 = GetExpedition_MapTipsAniUis(ui:GetChild("Tips2"))
  uis.Tips3 = GetExpedition_MapTipsAniUis(ui:GetChild("Tips3"))
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_Map2ByName.lua.lua
**Functions:**
- GetExpedition_Map2Uis
**Requires:**
- Expedition_MapTipsAniByName
**Snippet:**
```lua
require("Expedition_MapTipsAniByName")

function GetExpedition_Map2Uis(ui)
  local uis = {}
  uis.Tips1 = GetExpedition_MapTipsAniUis(ui:GetChild("Tips1"))
  uis.Tips2 = GetExpedition_MapTipsAniUis(ui:GetChild("Tips2"))
  uis.Tips3 = GetExpedition_MapTipsAniUis(ui:GetChild("Tips3"))
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_Map3ByName.lua.lua
**Functions:**
- GetExpedition_Map3Uis
**Requires:**
- Expedition_MapTipsAniByName
**Snippet:**
```lua
require("Expedition_MapTipsAniByName")

function GetExpedition_Map3Uis(ui)
  local uis = {}
  uis.Tips1 = GetExpedition_MapTipsAniUis(ui:GetChild("Tips1"))
  uis.Tips2 = GetExpedition_MapTipsAniUis(ui:GetChild("Tips2"))
  uis.Tips3 = GetExpedition_MapTipsAniUis(ui:GetChild("Tips3"))
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_Map4ByName.lua.lua
**Functions:**
- GetExpedition_Map4Uis
**Requires:**
- Expedition_MapTipsAniByName
**Snippet:**
```lua
require("Expedition_MapTipsAniByName")

function GetExpedition_Map4Uis(ui)
  local uis = {}
  uis.Tips1 = GetExpedition_MapTipsAniUis(ui:GetChild("Tips1"))
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_MapTipsAniByName.lua.lua
**Functions:**
- GetExpedition_MapTipsAniUis
**Snippet:**
```lua
function GetExpedition_MapTipsAniUis(ui)
  local uis = {}
  
  uis.MapTipsBtn = ui:GetChild("MapTipsBtn")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_MapTipsBtnByName.lua.lua
**Functions:**
- GetExpedition_MapTipsBtnUis
**Snippet:**
```lua
function GetExpedition_MapTipsBtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.PicHolder = ui:GetChild("PicHolder")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
```

---

## EF/Expedition_ReviewProgressByName.lua.lua
**Functions:**
- GetExpedition_ReviewProgressUis
**Snippet:**
```lua
function GetExpedition_ReviewProgressUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_ReviewStarByName.lua.lua
**Functions:**
- GetExpedition_ReviewStarUis
**Snippet:**
```lua
function GetExpedition_ReviewStarUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_ReviewTabAniByName.lua.lua
**Functions:**
- GetExpedition_ReviewTabAniUis
**Snippet:**
```lua
function GetExpedition_ReviewTabAniUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_ReviewTabBtnByName.lua.lua
**Functions:**
- GetExpedition_ReviewTabBtnUis
**Requires:**
- Expedition_ReviewTabAniByName
**Snippet:**
```lua
require("Expedition_ReviewTabAniByName")

function GetExpedition_ReviewTabBtnUis(ui)
  local uis = {}
  uis.ReviewTabAni = GetExpedition_ReviewTabAniUis(ui:GetChild("ReviewTabAni"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## EF/Expedition_ReviewTabRegionByName.lua.lua
**Functions:**
- GetExpedition_ReviewTabRegionUis
**Snippet:**
```lua
function GetExpedition_ReviewTabRegionUis(ui)
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

## EF/Expedition_ReviewTips1ByName.lua.lua
**Functions:**
- GetExpedition_ReviewTips1Uis
**Snippet:**
```lua
function GetExpedition_ReviewTips1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.StarList = ui:GetChild("StarList")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_ReviewTips2ByName.lua.lua
**Functions:**
- GetExpedition_ReviewTips2Uis
**Requires:**
- Expedition_ReviewTips2_4ByName
**Snippet:**
```lua
require("Expedition_ReviewTips2_4ByName")

function GetExpedition_ReviewTips2Uis(ui)
  local uis = {}
  uis.Wave1 = GetExpedition_ReviewTips2_4Uis(ui:GetChild("Wave1"))
  uis.Wave2 = GetExpedition_ReviewTips2_4Uis(ui:GetChild("Wave2"))
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_ReviewTips2_1ByName.lua.lua
**Functions:**
- GetExpedition_ReviewTips2_1Uis
**Snippet:**
```lua
function GetExpedition_ReviewTips2_1Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_ReviewTips2_2BgByName.lua.lua
**Functions:**
- GetExpedition_ReviewTips2_2BgUis
**Snippet:**
```lua
function GetExpedition_ReviewTips2_2BgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_ReviewTips2_2ByName.lua.lua
**Functions:**
- GetExpedition_ReviewTips2_2Uis
**Requires:**
- Expedition_ReviewTips2_2BgByName
- CommonResource_OccupationByName
- CommonResource_CardBreachByName
**Snippet:**
```lua
require("Expedition_ReviewTips2_2BgByName")
require("CommonResource_OccupationByName")
require("CommonResource_CardBreachByName")

function GetExpedition_ReviewTips2_2Uis(ui)
  local uis = {}
  uis.HeadBg = GetExpedition_ReviewTips2_2BgUis(ui:GetChild("HeadBg"))
  uis.Occupation = GetCommonResource_OccupationUis(ui:GetChild("Occupation"))
  uis.ElementList = ui:GetChild("ElementList")
  uis.NameTxt = ui:GetChild("NameTxt")
```

---

## EF/Expedition_ReviewTips2_3BtnByName.lua.lua
**Functions:**
- GetExpedition_ReviewTips2_3BtnUis
**Snippet:**
```lua
function GetExpedition_ReviewTips2_3BtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_ReviewTips2_4ByName.lua.lua
**Functions:**
- GetExpedition_ReviewTips2_4Uis
**Requires:**
- Expedition_ReviewTips2_1ByName
**Snippet:**
```lua
require("Expedition_ReviewTips2_1ByName")

function GetExpedition_ReviewTips2_4Uis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.Wave = GetExpedition_ReviewTips2_1Uis(ui:GetChild("Wave"))
  uis.HeadList = ui:GetChild("HeadList")
  uis.SwitchBtn = ui:GetChild("SwitchBtn")
  uis.c1Ctr = ui:GetController("c1")
```

---

## EF/Expedition_ReviewTipsRegionBtnByName.lua.lua
**Functions:**
- GetExpedition_ReviewTipsRegionBtnUis
**Requires:**
- Expedition_ReviewTips1ByName
**Snippet:**
```lua
require("Expedition_ReviewTips1ByName")

function GetExpedition_ReviewTipsRegionBtnUis(ui)
  local uis = {}
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReviewTips1 = GetExpedition_ReviewTips1Uis(ui:GetChild("ReviewTips1"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_ReviewTitleByName.lua.lua
**Functions:**
- GetExpedition_ReviewTitleUis
**Snippet:**
```lua
function GetExpedition_ReviewTitleUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_RewardByName.lua.lua
**Functions:**
- GetExpedition_RewardUis
**Requires:**
- CommonResource_BackGroundByName
- Expedition_RewardTitleByName
- Expedition_RewardStarNumberByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Expedition_RewardTitleByName")
require("Expedition_RewardStarNumberByName")
require("CommonResource_CurrencyReturnByName")

function GetExpedition_RewardUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.RewardTitle = GetExpedition_RewardTitleUis(ui:GetChild("RewardTitle"))
  uis.RewardList = ui:GetChild("RewardList")
```

---

## EF/Expedition_RewardItemByName.lua.lua
**Functions:**
- GetExpedition_RewardItemUis
**Snippet:**
```lua
function GetExpedition_RewardItemUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_RewardStarNumberByName.lua.lua
**Functions:**
- GetExpedition_RewardStarNumberUis
**Snippet:**
```lua
function GetExpedition_RewardStarNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_RewardTipsAniByName.lua.lua
**Functions:**
- GetExpedition_RewardTipsAniUis
**Requires:**
- Expedition_RewardTipsByName
**Snippet:**
```lua
require("Expedition_RewardTipsByName")

function GetExpedition_RewardTipsAniUis(ui)
  local uis = {}
  uis.RewardTips = GetExpedition_RewardTipsUis(ui:GetChild("RewardTips"))
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_RewardTipsByName.lua.lua
**Functions:**
- GetExpedition_RewardTipsUis
**Snippet:**
```lua
function GetExpedition_RewardTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.WordNumberTxt = ui:GetChild("WordNumberTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.ProgressTxt = ui:GetChild("ProgressTxt")
  uis.GetTxt = ui:GetChild("GetTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## EF/Expedition_RewardTitleByName.lua.lua
**Functions:**
- GetExpedition_RewardTitleUis
**Snippet:**
```lua
function GetExpedition_RewardTitleUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Expedition_RewardWindowByName.lua.lua
**Functions:**
- GetExpedition_RewardWindowUis
**Requires:**
- Expedition_RewardByName
**Snippet:**
```lua
require("Expedition_RewardByName")

function GetExpedition_RewardWindowUis(ui)
  local uis = {}
  uis.Main = GetExpedition_RewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/ExploreAFKData.lua.lua
**Snippet:**
```lua
local level, exp, groups, tempGroupCards
local AddOrOverrideGroupInfo = function(groupInfo)
  groups = groups or {}
  local k = table.keyof(groups, groupInfo.groupId, "groupId")
  if not k then
    table.insert(groups, groupInfo)
  else
    groups[k] = groupInfo
  end
end
```

---

## EF/ExploreAFKMgr.lua.lua
**Snippet:**
```lua
local IsCardSelected = function(groupId, cardId)
  local tempCards = ExploreAFKData.GetTempGroupCards(groupId)
  if tempCards then
    return table.keyof(tempCards, cardId, "cardId")
  end
end
local IsSelected = function(groupId, index)
  local tempCards = ExploreAFKData.GetTempGroupCards(groupId)
  if tempCards then
    return table.keyof(tempCards, index, "index")
```

---

## EF/ExploreAFKScriptList.lua.lua
**Requires:**
- ExploreAFKData
- ExploreAFKMgr
- ExploreAFKService
**Snippet:**
```lua
ExploreAFKData = require("ExploreAFKData")
ExploreAFKMgr = require("ExploreAFKMgr")
ExploreAFKService = require("ExploreAFKService")
```

---

## EF/ExploreAFKService.lua.lua
**Snippet:**
```lua
local GetExploreAFKInfoReq = function(rspCallback)
  Net.Send(Proto.MsgName.GetDispatchInfoReq, nil, rspCallback)
end
local GetExploreAFKInfoRsp = function(msg)
  local exp = msg.exp
  local level = msg.level
  ExploreAFKData.SetExp(exp)
  ExploreAFKData.SetLevel(level)
  local groups = msg.groups
  ExploreAFKData.ClearAllGroupsInfo()
```

---

## EF/ExploreAFKWindow.lua.lua
**Functions:**
- ExploreAFKWindow.ReInitData
- ExploreAFKWindow.OnInit
- ExploreAFKWindow.UpdateInfo
- ExploreAFKWindow.InitBtn
- ExploreAFKWindow.OnShown
- ExploreAFKWindow.OnClose
- ExploreAFKWindow.HandleMessage
**Requires:**
- Explore_ExploreAFKWindowByName
**Snippet:**
```lua
require("Explore_ExploreAFKWindowByName")
local ExploreAFKWindow = {}
local uis, contentPane, teamsInfo, currentSelectedTeam, lastSelectedTeamIndex, playDropAnim, tweeners
local CardItemRenderer = function(i, gcmp)
  local index = i + 1
  local occupationType = currentSelectedTeam.occupationTypes[index]
  local holder = gcmp:GetChild("QBHolder")
  holder.visible = false
  local occupation = gcmp:GetChild("Occupation")
  ChangeUIController(occupation, "c1", occupationType - 1)
```

---

## EF/ExploreDevelop_AddBtnByName.lua.lua
**Functions:**
- GetExploreDevelop_AddBtnUis
**Snippet:**
```lua
function GetExploreDevelop_AddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_DefaultMaxBtnByName.lua.lua
**Functions:**
- GetExploreDevelop_DefaultMaxBtnUis
**Snippet:**
```lua
function GetExploreDevelop_DefaultMaxBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_DevelopAttributeByName.lua.lua
**Functions:**
- GetExploreDevelop_DevelopAttributeUis
**Snippet:**
```lua
function GetExploreDevelop_DevelopAttributeUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_DevelopByName.lua.lua
**Functions:**
- GetExploreDevelop_DevelopUis
**Requires:**
- CommonResource_BackGroundByName
- ExploreDevelop_DevelopWearRegionByName
- ExploreDevelop_SealRegionByName
- ExploreDevelop_DevelopEquipmentRegionByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ExploreDevelop_DevelopWearRegionByName")
require("ExploreDevelop_SealRegionByName")
require("ExploreDevelop_DevelopEquipmentRegionByName")
require("CommonResource_CurrencyReturnByName")

function GetExploreDevelop_DevelopUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.WearRegion = GetExploreDevelop_DevelopWearRegionUis(ui:GetChild("WearRegion"))
```

---

## EF/ExploreDevelop_DevelopEquipmentRegionByName.lua.lua
**Functions:**
- GetExploreDevelop_DevelopEquipmentRegionUis
**Requires:**
- ExploreDevelop_SealLevel_BreachByName
**Snippet:**
```lua
require("ExploreDevelop_SealLevel_BreachByName")

function GetExploreDevelop_DevelopEquipmentRegionUis(ui)
  local uis = {}
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Effect3Holder = ui:GetChild("Effect3Holder")
  uis.PopupCloseBtn = ui:GetChild("PopupCloseBtn")
  uis.Slot1Btn = ui:GetChild("Slot1Btn")
  uis.Slot2Btn = ui:GetChild("Slot2Btn")
```

---

## EF/ExploreDevelop_DevelopEquipmentSlotBtnByName.lua.lua
**Functions:**
- GetExploreDevelop_DevelopEquipmentSlotBtnUis
**Snippet:**
```lua
function GetExploreDevelop_DevelopEquipmentSlotBtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.colorCtr = ui:GetController("color")
```

---

## EF/ExploreDevelop_DevelopOccupationByName.lua.lua
**Functions:**
- GetExploreDevelop_DevelopOccupationUis
**Snippet:**
```lua
function GetExploreDevelop_DevelopOccupationUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_DevelopSynthesisBtnByName.lua.lua
**Functions:**
- GetExploreDevelop_DevelopSynthesisBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetExploreDevelop_DevelopSynthesisBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_DevelopTabBtnByName.lua.lua
**Functions:**
- GetExploreDevelop_DevelopTabBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetExploreDevelop_DevelopTabBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_DevelopWearItemAniByName.lua.lua
**Functions:**
- GetExploreDevelop_DevelopWearItemAniUis
**Snippet:**
```lua
function GetExploreDevelop_DevelopWearItemAniUis(ui)
  local uis = {}
  
  uis.DevelopWearItemBtn = ui:GetChild("DevelopWearItemBtn")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_DevelopWearItemBtnByName.lua.lua
**Functions:**
- GetExploreDevelop_DevelopWearItemBtnUis
**Snippet:**
```lua
function GetExploreDevelop_DevelopWearItemBtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.AttributeTxt = ui:GetChild("AttributeTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
```

---

## EF/ExploreDevelop_DevelopWearRegionByName.lua.lua
**Functions:**
- GetExploreDevelop_DevelopWearRegionUis
**Snippet:**
```lua
function GetExploreDevelop_DevelopWearRegionUis(ui)
  local uis = {}
  
  uis.WearList = ui:GetChild("WearList")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_DevelopWearRegionListByName.lua.lua
**Functions:**
- GetExploreDevelop_DevelopWearRegionListUis
**Snippet:**
```lua
function GetExploreDevelop_DevelopWearRegionListUis(ui)
  local uis = {}
  
  uis.TitleBtn = ui:GetChild("TitleBtn")
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_DevelopWearTitleAttributeByName.lua.lua
**Functions:**
- GetExploreDevelop_DevelopWearTitleAttributeUis
**Snippet:**
```lua
function GetExploreDevelop_DevelopWearTitleAttributeUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_DevelopWearTitleBtnByName.lua.lua
**Functions:**
- GetExploreDevelop_DevelopWearTitleBtnUis
**Requires:**
- ExploreDevelop_DevelopWearTitleAttributeByName
**Snippet:**
```lua
require("ExploreDevelop_DevelopWearTitleAttributeByName")

function GetExploreDevelop_DevelopWearTitleBtnUis(ui)
  local uis = {}
  uis.Attribute = GetExploreDevelop_DevelopWearTitleAttributeUis(ui:GetChild("Attribute"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## EF/ExploreDevelop_DevelopWindowByName.lua.lua
**Functions:**
- GetExploreDevelop_DevelopWindowUis
**Requires:**
- ExploreDevelop_DevelopByName
**Snippet:**
```lua
require("ExploreDevelop_DevelopByName")

function GetExploreDevelop_DevelopWindowUis(ui)
  local uis = {}
  uis.Main = GetExploreDevelop_DevelopUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_MaxBtnByName.lua.lua
**Functions:**
- GetExploreDevelop_MaxBtnUis
**Snippet:**
```lua
function GetExploreDevelop_MaxBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_MinBtnByName.lua.lua
**Functions:**
- GetExploreDevelop_MinBtnUis
**Snippet:**
```lua
function GetExploreDevelop_MinBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_NumberStripByName.lua.lua
**Functions:**
- GetExploreDevelop_NumberStripUis
**Snippet:**
```lua
function GetExploreDevelop_NumberStripUis(ui)
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

## EF/ExploreDevelop_ReduceBtnByName.lua.lua
**Functions:**
- GetExploreDevelop_ReduceBtnUis
**Snippet:**
```lua
function GetExploreDevelop_ReduceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SealForge_FirstLockByName.lua.lua
**Functions:**
- GetExploreDevelop_SealForge_FirstLockUis
**Snippet:**
```lua
function GetExploreDevelop_SealForge_FirstLockUis(ui)
  local uis = {}
  
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SealForge_ForgeRegionByName.lua.lua
**Functions:**
- GetExploreDevelop_SealForge_ForgeRegionUis
**Requires:**
- ExploreDevelop_SealForge_PicByName
- ExploreDevelop_SealForge_NumberByName
- ExploreDevelop_SealForge_PartAttributeRegionByName
- ExploreDevelop_SealForge_MaxByName
- ExploreDevelop_SealForge_FirstLockByName
- ExploreDevelop_SealForge_LimitLockByName
**Snippet:**
```lua
require("ExploreDevelop_SealForge_PicByName")
require("ExploreDevelop_SealForge_NumberByName")
require("ExploreDevelop_SealForge_PartAttributeRegionByName")
require("ExploreDevelop_SealForge_MaxByName")
require("ExploreDevelop_SealForge_FirstLockByName")
require("ExploreDevelop_SealForge_LimitLockByName")

function GetExploreDevelop_SealForge_ForgeRegionUis(ui)
  local uis = {}
  uis.Pic = GetExploreDevelop_SealForge_PicUis(ui:GetChild("Pic"))
```

---

## EF/ExploreDevelop_SealForge_LimitLockByName.lua.lua
**Functions:**
- GetExploreDevelop_SealForge_LimitLockUis
**Snippet:**
```lua
function GetExploreDevelop_SealForge_LimitLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SealForge_MaxByName.lua.lua
**Functions:**
- GetExploreDevelop_SealForge_MaxUis
**Snippet:**
```lua
function GetExploreDevelop_SealForge_MaxUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SealForge_NumberByName.lua.lua
**Functions:**
- GetExploreDevelop_SealForge_NumberUis
**Snippet:**
```lua
function GetExploreDevelop_SealForge_NumberUis(ui)
  local uis = {}
  
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SealForge_PartAttributeByName.lua.lua
**Functions:**
- GetExploreDevelop_SealForge_PartAttributeUis
**Snippet:**
```lua
function GetExploreDevelop_SealForge_PartAttributeUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## EF/ExploreDevelop_SealForge_PartAttributeRegionByName.lua.lua
**Functions:**
- GetExploreDevelop_SealForge_PartAttributeRegionUis
**Snippet:**
```lua
function GetExploreDevelop_SealForge_PartAttributeRegionUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PartAttributeList = ui:GetChild("PartAttributeList")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SealForge_PicByName.lua.lua
**Functions:**
- GetExploreDevelop_SealForge_PicUis
**Snippet:**
```lua
function GetExploreDevelop_SealForge_PicUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SealForge_UpBtnByName.lua.lua
**Functions:**
- GetExploreDevelop_SealForge_UpBtnUis
**Snippet:**
```lua
function GetExploreDevelop_SealForge_UpBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SealLevelUpTipsByName.lua.lua
**Functions:**
- GetExploreDevelop_SealLevelUpTipsUis
**Requires:**
- ExploreDevelop_SealLevel_UpTipsAni1ByName
- ExploreDevelop_SealLevel_UpTipsAni2ByName
- ExploreDevelop_SealLevel_BreachByName
**Snippet:**
```lua
require("ExploreDevelop_SealLevel_UpTipsAni1ByName")
require("ExploreDevelop_SealLevel_UpTipsAni2ByName")
require("ExploreDevelop_SealLevel_BreachByName")

function GetExploreDevelop_SealLevelUpTipsUis(ui)
  local uis = {}
  uis.TipsAni1 = GetExploreDevelop_SealLevel_UpTipsAni1Uis(ui:GetChild("TipsAni1"))
  uis.TipsAni2 = GetExploreDevelop_SealLevel_UpTipsAni2Uis(ui:GetChild("TipsAni2"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.Breach = GetExploreDevelop_SealLevel_BreachUis(ui:GetChild("Breach"))
```

---

## EF/ExploreDevelop_SealLevelUpTipsWindowByName.lua.lua
**Functions:**
- GetExploreDevelop_SealLevelUpTipsWindowUis
**Requires:**
- ExploreDevelop_SealLevel_UpUpTipsByName
**Snippet:**
```lua
require("ExploreDevelop_SealLevel_UpUpTipsByName")

function GetExploreDevelop_SealLevelUpTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetExploreDevelop_SealLevel_UpUpTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SealLevel_AttributeByName.lua.lua
**Functions:**
- GetExploreDevelop_SealLevel_AttributeUis
**Snippet:**
```lua
function GetExploreDevelop_SealLevel_AttributeUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.breachCtr = ui:GetController("breach")
  uis.root = ui
  return uis
```

---

## EF/ExploreDevelop_SealLevel_AttributeRegionByName.lua.lua
**Functions:**
- GetExploreDevelop_SealLevel_AttributeRegionUis
**Requires:**
- ExploreDevelop_SealLevel_BreachUpByName
**Snippet:**
```lua
require("ExploreDevelop_SealLevel_BreachUpByName")

function GetExploreDevelop_SealLevel_AttributeRegionUis(ui)
  local uis = {}
  uis.BreachUp = GetExploreDevelop_SealLevel_BreachUpUis(ui:GetChild("BreachUp"))
  uis.AttributeList = ui:GetChild("AttributeList")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SealLevel_BreachByName.lua.lua
**Functions:**
- GetExploreDevelop_SealLevel_BreachUis
**Snippet:**
```lua
function GetExploreDevelop_SealLevel_BreachUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SealLevel_BreachUpByName.lua.lua
**Functions:**
- GetExploreDevelop_SealLevel_BreachUpUis
**Snippet:**
```lua
function GetExploreDevelop_SealLevel_BreachUpUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SealLevel_ExpProgressBarByName.lua.lua
**Functions:**
- GetExploreDevelop_SealLevel_ExpProgressBarUis
**Snippet:**
```lua
function GetExploreDevelop_SealLevel_ExpProgressBarUis(ui)
  local uis = {}
  
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.LevelAniTxt = ui:GetChild("LevelAniTxt")
  uis.Level1Txt = ui:GetChild("Level1Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SealLevel_LevelRegionByName.lua.lua
**Functions:**
- GetExploreDevelop_SealLevel_LevelRegionUis
**Requires:**
- ExploreDevelop_SealLevel_BreachByName
- ExploreDevelop_SealLevel_AttributeRegionByName
- ExploreDevelop_SealLevel_MaxByName
**Snippet:**
```lua
require("ExploreDevelop_SealLevel_BreachByName")
require("ExploreDevelop_SealLevel_AttributeRegionByName")
require("ExploreDevelop_SealLevel_MaxByName")

function GetExploreDevelop_SealLevel_LevelRegionUis(ui)
  local uis = {}
  uis.ExpProgressBar = ui:GetChild("ExpProgressBar")
  uis.Breach = GetExploreDevelop_SealLevel_BreachUis(ui:GetChild("Breach"))
  uis.AttributeRegion = GetExploreDevelop_SealLevel_AttributeRegionUis(ui:GetChild("AttributeRegion"))
  uis.SpendList = ui:GetChild("SpendList")
```

---

## EF/ExploreDevelop_SealLevel_MaxByName.lua.lua
**Functions:**
- GetExploreDevelop_SealLevel_MaxUis
**Snippet:**
```lua
function GetExploreDevelop_SealLevel_MaxUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SealLevel_SpendByName.lua.lua
**Functions:**
- GetExploreDevelop_SealLevel_SpendUis
**Snippet:**
```lua
function GetExploreDevelop_SealLevel_SpendUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SealLevel_UpAttribute1ByName.lua.lua
**Functions:**
- GetExploreDevelop_SealLevel_UpAttribute1Uis
**Snippet:**
```lua
function GetExploreDevelop_SealLevel_UpAttribute1Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SealLevel_UpAttribute2ByName.lua.lua
**Functions:**
- GetExploreDevelop_SealLevel_UpAttribute2Uis
**Snippet:**
```lua
function GetExploreDevelop_SealLevel_UpAttribute2Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## EF/ExploreDevelop_SealLevel_UpBtnByName.lua.lua
**Functions:**
- GetExploreDevelop_SealLevel_UpBtnUis
**Snippet:**
```lua
function GetExploreDevelop_SealLevel_UpBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SealLevel_UpTipsAni1ByName.lua.lua
**Functions:**
- GetExploreDevelop_SealLevel_UpTipsAni1Uis
**Snippet:**
```lua
function GetExploreDevelop_SealLevel_UpTipsAni1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SealLevel_UpTipsAni2ByName.lua.lua
**Functions:**
- GetExploreDevelop_SealLevel_UpTipsAni2Uis
**Snippet:**
```lua
function GetExploreDevelop_SealLevel_UpTipsAni2Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SealLevel_UpUpTipsByName.lua.lua
**Functions:**
- GetExploreDevelop_SealLevel_UpUpTipsUis
**Requires:**
- CommonResource_PopupBgByName
- ExploreDevelop_SealLevelUpTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ExploreDevelop_SealLevelUpTipsByName")

function GetExploreDevelop_SealLevel_UpUpTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.LevelUpTipsContent = GetExploreDevelop_SealLevelUpTipsUis(ui:GetChild("LevelUpTipsContent"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.root = ui
  return uis
```

---

## EF/ExploreDevelop_SealRegionByName.lua.lua
**Functions:**
- GetExploreDevelop_SealRegionUis
**Requires:**
- ExploreDevelop_SealLevel_LevelRegionByName
- ExploreDevelop_SealForge_ForgeRegionByName
**Snippet:**
```lua
require("ExploreDevelop_SealLevel_LevelRegionByName")
require("ExploreDevelop_SealForge_ForgeRegionByName")

function GetExploreDevelop_SealRegionUis(ui)
  local uis = {}
  uis.LevelRegion = GetExploreDevelop_SealLevel_LevelRegionUis(ui:GetChild("LevelRegion"))
  uis.ForgeRegion = GetExploreDevelop_SealForge_ForgeRegionUis(ui:GetChild("ForgeRegion"))
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.TabList = ui:GetChild("TabList")
  uis.c1Ctr = ui:GetController("c1")
```

---

## EF/ExploreDevelop_SealTabBtnByName.lua.lua
**Functions:**
- GetExploreDevelop_SealTabBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetExploreDevelop_SealTabBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## EF/ExploreDevelop_SynthesisByName.lua.lua
**Functions:**
- GetExploreDevelop_SynthesisUis
**Requires:**
- CommonResource_BackGroundByName
- ExploreDevelop_SynthesisMidRegionByName
- ExploreDevelop_SynthesisMidNothingByName
- ExploreDevelop_SynthesisLeftRegionByName
- ExploreDevelop_NumberStripByName
- ExploreDevelop_SynthesisRightRegionByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ExploreDevelop_SynthesisMidRegionByName")
require("ExploreDevelop_SynthesisMidNothingByName")
require("ExploreDevelop_SynthesisLeftRegionByName")
require("ExploreDevelop_NumberStripByName")
require("ExploreDevelop_SynthesisRightRegionByName")
require("CommonResource_CurrencyReturnByName")

function GetExploreDevelop_SynthesisUis(ui)
  local uis = {}
```

---

## EF/ExploreDevelop_SynthesisItemByName.lua.lua
**Functions:**
- GetExploreDevelop_SynthesisItemUis
**Snippet:**
```lua
function GetExploreDevelop_SynthesisItemUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.colorCtr = ui:GetController("color")
  uis.c2Ctr = ui:GetController("c2")
```

---

## EF/ExploreDevelop_SynthesisItemListByName.lua.lua
**Functions:**
- GetExploreDevelop_SynthesisItemListUis
**Snippet:**
```lua
function GetExploreDevelop_SynthesisItemListUis(ui)
  local uis = {}
  
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SynthesisItemTips1ByName.lua.lua
**Functions:**
- GetExploreDevelop_SynthesisItemTips1Uis
**Requires:**
- ExploreDevelop_SynthesisItemTitle1ByName
- ExploreDevelop_SynthesisItemTitle2ByName
**Snippet:**
```lua
require("ExploreDevelop_SynthesisItemTitle1ByName")
require("ExploreDevelop_SynthesisItemTitle2ByName")

function GetExploreDevelop_SynthesisItemTips1Uis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.TitleEffectHolder = ui:GetChild("TitleEffectHolder")
  uis.Title1 = GetExploreDevelop_SynthesisItemTitle1Uis(ui:GetChild("Title1"))
  uis.Title2 = GetExploreDevelop_SynthesisItemTitle2Uis(ui:GetChild("Title2"))
```

---

## EF/ExploreDevelop_SynthesisItemTips2ByName.lua.lua
**Functions:**
- GetExploreDevelop_SynthesisItemTips2Uis
**Requires:**
- CommonResource_PopupBgByName
- ExploreDevelop_SynthesisItemTips1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ExploreDevelop_SynthesisItemTips1ByName")

function GetExploreDevelop_SynthesisItemTips2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.GetItemTips1 = GetExploreDevelop_SynthesisItemTips1Uis(ui:GetChild("GetItemTips1"))
  uis.root = ui
```

---

## EF/ExploreDevelop_SynthesisItemTipsWindowByName.lua.lua
**Functions:**
- GetExploreDevelop_SynthesisItemTipsWindowUis
**Requires:**
- ExploreDevelop_SynthesisItemTips2ByName
**Snippet:**
```lua
require("ExploreDevelop_SynthesisItemTips2ByName")

function GetExploreDevelop_SynthesisItemTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetExploreDevelop_SynthesisItemTips2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SynthesisItemTitle1ByName.lua.lua
**Functions:**
- GetExploreDevelop_SynthesisItemTitle1Uis
**Requires:**
- ExploreDevelop_SynthesisItemListByName
**Snippet:**
```lua
require("ExploreDevelop_SynthesisItemListByName")

function GetExploreDevelop_SynthesisItemTitle1Uis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = GetExploreDevelop_SynthesisItemListUis(ui:GetChild("ItemList"))
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SynthesisItemTitle2ByName.lua.lua
**Functions:**
- GetExploreDevelop_SynthesisItemTitle2Uis
**Requires:**
- ExploreDevelop_SynthesisItemListByName
**Snippet:**
```lua
require("ExploreDevelop_SynthesisItemListByName")

function GetExploreDevelop_SynthesisItemTitle2Uis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = GetExploreDevelop_SynthesisItemListUis(ui:GetChild("ItemList"))
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SynthesisLeftItemAniByName.lua.lua
**Functions:**
- GetExploreDevelop_SynthesisLeftItemAniUis
**Snippet:**
```lua
function GetExploreDevelop_SynthesisLeftItemAniUis(ui)
  local uis = {}
  
  uis.DevelopWearItemBtn = ui:GetChild("DevelopWearItemBtn")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SynthesisLeftItemBtnByName.lua.lua
**Functions:**
- GetExploreDevelop_SynthesisLeftItemBtnUis
**Snippet:**
```lua
function GetExploreDevelop_SynthesisLeftItemBtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.AttributeTxt = ui:GetChild("AttributeTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
```

---

## EF/ExploreDevelop_SynthesisLeftRegionByName.lua.lua
**Functions:**
- GetExploreDevelop_SynthesisLeftRegionUis
**Snippet:**
```lua
function GetExploreDevelop_SynthesisLeftRegionUis(ui)
  local uis = {}
  
  uis.WearList = ui:GetChild("WearList")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SynthesisLeftRegionListByName.lua.lua
**Functions:**
- GetExploreDevelop_SynthesisLeftRegionListUis
**Snippet:**
```lua
function GetExploreDevelop_SynthesisLeftRegionListUis(ui)
  local uis = {}
  
  uis.TitleBtn = ui:GetChild("TitleBtn")
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SynthesisLeftTitleBtnByName.lua.lua
**Functions:**
- GetExploreDevelop_SynthesisLeftTitleBtnUis
**Requires:**
- ExploreDevelop_DevelopWearTitleAttributeByName
**Snippet:**
```lua
require("ExploreDevelop_DevelopWearTitleAttributeByName")

function GetExploreDevelop_SynthesisLeftTitleBtnUis(ui)
  local uis = {}
  uis.Attribute = GetExploreDevelop_DevelopWearTitleAttributeUis(ui:GetChild("Attribute"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## EF/ExploreDevelop_SynthesisMidNothingByName.lua.lua
**Functions:**
- GetExploreDevelop_SynthesisMidNothingUis
**Snippet:**
```lua
function GetExploreDevelop_SynthesisMidNothingUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SynthesisMidRegionByName.lua.lua
**Functions:**
- GetExploreDevelop_SynthesisMidRegionUis
**Snippet:**
```lua
function GetExploreDevelop_SynthesisMidRegionUis(ui)
  local uis = {}
  
  uis.Slot1Btn = ui:GetChild("Slot1Btn")
  uis.Slot2Btn = ui:GetChild("Slot2Btn")
  uis.Slot3Btn = ui:GetChild("Slot3Btn")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
```

---

## EF/ExploreDevelop_SynthesisRightItemBtnByName.lua.lua
**Functions:**
- GetExploreDevelop_SynthesisRightItemBtnUis
**Snippet:**
```lua
function GetExploreDevelop_SynthesisRightItemBtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SynthesisRightRegionByName.lua.lua
**Functions:**
- GetExploreDevelop_SynthesisRightRegionUis
**Requires:**
- ExploreDevelop_SynthesisRightSpendByName
**Snippet:**
```lua
require("ExploreDevelop_SynthesisRightSpendByName")

function GetExploreDevelop_SynthesisRightRegionUis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.ProbabilityTxt = ui:GetChild("ProbabilityTxt")
  uis.ItemBtn = ui:GetChild("ItemBtn")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Spend = GetExploreDevelop_SynthesisRightSpendUis(ui:GetChild("Spend"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## EF/ExploreDevelop_SynthesisRightSpendByName.lua.lua
**Functions:**
- GetExploreDevelop_SynthesisRightSpendUis
**Requires:**
- ExploreDevelop_SynthesisRightSpendNumberByName
- ExploreDevelop_SynthesisRightSpendLackWordByName
**Snippet:**
```lua
require("ExploreDevelop_SynthesisRightSpendNumberByName")
require("ExploreDevelop_SynthesisRightSpendLackWordByName")

function GetExploreDevelop_SynthesisRightSpendUis(ui)
  local uis = {}
  uis.Spend = GetExploreDevelop_SynthesisRightSpendNumberUis(ui:GetChild("Spend"))
  uis.SureBtn = ui:GetChild("SureBtn")
  uis.LackWord = GetExploreDevelop_SynthesisRightSpendLackWordUis(ui:GetChild("LackWord"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## EF/ExploreDevelop_SynthesisRightSpendLackWordByName.lua.lua
**Functions:**
- GetExploreDevelop_SynthesisRightSpendLackWordUis
**Snippet:**
```lua
function GetExploreDevelop_SynthesisRightSpendLackWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SynthesisRightSpendNumberByName.lua.lua
**Functions:**
- GetExploreDevelop_SynthesisRightSpendNumberUis
**Snippet:**
```lua
function GetExploreDevelop_SynthesisRightSpendNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SynthesisRightSpendSureBtnByName.lua.lua
**Functions:**
- GetExploreDevelop_SynthesisRightSpendSureBtnUis
**Snippet:**
```lua
function GetExploreDevelop_SynthesisRightSpendSureBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDevelop_SynthesisWindowByName.lua.lua
**Functions:**
- GetExploreDevelop_SynthesisWindowUis
**Requires:**
- ExploreDevelop_SynthesisByName
**Snippet:**
```lua
require("ExploreDevelop_SynthesisByName")

function GetExploreDevelop_SynthesisWindowUis(ui)
  local uis = {}
  uis.Main = GetExploreDevelop_SynthesisUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDispatchWindow.lua.lua
**Functions:**
- cardlist.itemRenderer
- ExploreDispatchWindow.ReInitData
- ExploreDispatchWindow.OnInit
- ExploreDispatchWindow.UpdateInfo
- ExploreDispatchWindow.InitBtn
- ExploreDispatchWindow.OnClose
**Requires:**
- Explore_DispatchWindowByName
**Snippet:**
```lua
require("Explore_DispatchWindowByName")
local ExploreDispatchWindow = {}
local uis, contentPane, groupId, type_cardlist
local RefreshPanelInfo = function()
  local config = TableData.GetConfig(groupId, "BaseDispatchTeam")
  local job_num = config.job_num
  local cardlist = uis.Main.DispatchTips.CardList
  cardlist.numItems = #job_num
end
local CardItemRenderer = function(i, gcmp)
```

---

## EF/ExploreDungeonBreakthroughWindow.lua.lua
**Functions:**
- ExploreDungeonBreakthroughWindow.ReInitData
- ExploreDungeonBreakthroughWindow.OnInit
- ExploreDungeonBreakthroughWindow.UpdateInfo
- ExploreDungeonBreakthroughWindow.InitBtn
- ExploreDungeonBreakthroughWindow.OnClose
**Requires:**
- ExploreDungeon_BreachWindowByName
**Snippet:**
```lua
require("ExploreDungeon_BreachWindowByName")
local ExploreDungeonBreakthroughWindow = {}
local uis, contentPane
ld("ExploreDungeon")
local targetStageId
local jobs = {
  1,
  2,
  4,
  5
```

---

## EF/ExploreDungeonData.lua.lua
**Snippet:**
```lua
local playerInfo, dungeons
local SetPlayerInfo = function(info)
  playerInfo = info
end
local SetDungeonInfo = function(info)
  dungeons = dungeons or {}
  dungeons[info.sceneType] = info
end
local GetPlayerInfo = function()
  return playerInfo
```

---

## EF/ExploreDungeonFastCollectWindow.lua.lua
**Functions:**
- ExploreDungeonFastCollectWindow.ReInitData
- ExploreDungeonFastCollectWindow.OnInit
- ExploreDungeonFastCollectWindow.UpdateInfo
- panel.SpendList.itemRenderer
- panel.ItemList.itemRenderer
- ExploreDungeonFastCollectWindow.InitBtn
- ExploreDungeonFastCollectWindow.OnClose
- ExploreDungeonFastCollectWindow.HandleMessage
**Requires:**
- ExploreDungeon_LevelQuickWindowByName
**Snippet:**
```lua
require("ExploreDungeon_LevelQuickWindowByName")
local ExploreDungeonFastCollectWindow = {}
local uis, contentPane, consumes, selectedConsumeIndex
local parseItemStrs = function(strs)
  local list = {}
  for _, str in ipairs(strs) do
    local splits = Split(str, ":")
    table.insert(list, {
      itemType = tonumber(splits[1]),
      itemId = tonumber(splits[2]),
```

---

## EF/ExploreDungeonMainWindow.lua.lua
**Functions:**
- ExploreDungeonMainWindow.ReInitData
- ExploreDungeonMainWindow.OnInit
- ExploreDungeonMainWindow.UpdateInfo
- ExploreDungeonMainWindow.InitBtn
- ExploreDungeonMainWindow.OnClose
**Requires:**
- ExploreDungeon_ExploreAdventureWindowByName
**Snippet:**
```lua
require("ExploreDungeon_ExploreAdventureWindowByName")
local ExploreDungeonMainWindow = {}
local uis, contentPane
local ENTRANCE_LIST = {
  [1] = {
    name = T(20741),
    desc = T(20742),
    window = WinResConfig.ExploreDungeonUpgradeWindow.name,
    func_id = FEATURE_ENUM.SEAL_DUNGEON_UPGRADE
  },
```

---

## EF/ExploreDungeonMgr.lua.lua
**Snippet:**
```lua
local CardIsUsedInUpgradeDungeon = function(cardId)
  local info = ExploreDungeonData.GetPlayerInfo()
  local usedCards = info.usedCards
  if usedCards then
    local k = table.keyof(usedCards, cardId)
    return type(k) == "number"
  end
  return false
end
local GetChapters = function(buffer)
```

---

## EF/ExploreDungeonScriptList.lua.lua
**Requires:**
- ExploreDungeonData
- ExploreDungeonService
- ExploreDungeonMgr
**Snippet:**
```lua
ExploreDungeonData = require("ExploreDungeonData")
ExploreDungeonService = require("ExploreDungeonService")
ExploreDungeonMgr = require("ExploreDungeonMgr")
```

---

## EF/ExploreDungeonService.lua.lua
**Snippet:**
```lua
local getDungeonInfoMsg = {
  sceneTypes = {
    ProtoEnum.SCENE_TYPE.SEAL_QUALITY_UP
  }
}
local GetPlayerInfoReq = function(rspCallback)
  Net.Send(Proto.MsgName.GetSealBigHookInfoReq, nil, rspCallback)
end
local GetPlayerInfoRsp = function(msg)
  ExploreDungeonData.SetPlayerInfo(msg.info)
```

---

## EF/ExploreDungeonUpgradeExplainWindow.lua.lua
**Functions:**
- ExploreDungeonUpgradeExplainWindow.ReInitData
- ExploreDungeonUpgradeExplainWindow.OnInit
- ExploreDungeonUpgradeExplainWindow.UpdateInfo
- panel.InfoList.itemRenderer
- ExploreDungeonUpgradeExplainWindow.InitBtn
- ExploreDungeonUpgradeExplainWindow.OnClose
**Requires:**
- ExploreDungeon_LevelExplainWindowByName
**Snippet:**
```lua
require("ExploreDungeon_LevelExplainWindowByName")
local ExploreDungeonUpgradeExplainWindow = {}
local uis, contentPane

function ExploreDungeonUpgradeExplainWindow.ReInitData()
end

function ExploreDungeonUpgradeExplainWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ExploreDungeonUpgradeExplainWindow.package, WinResConfig.ExploreDungeonUpgradeExplainWindow.comName, function(com)
    contentPane = com
```

---

## EF/ExploreDungeonUpgradeWindow.lua.lua
**Functions:**
- list.itemRenderer
- RefreshRewardInfo
- RefreshPanelInfo
- ExploreDungeonUpgradeWindow.ReInitData
- ExploreDungeonUpgradeWindow.OnInit
- ExploreDungeonUpgradeWindow.UpdateInfo
- ExploreDungeonUpgradeWindow.InitBtn
- ExploreDungeonUpgradeWindow.OnClose
- ExploreDungeonUpgradeWindow.HandleMessage
**Requires:**
- ExploreDungeon_LevelUpWindowByName
**Snippet:**
```lua
require("ExploreDungeon_LevelUpWindowByName")
local ExploreDungeonUpgradeWindow = {}
local uis, contentPane, chapters, outputs, hangingTimer, RefreshPanelInfo, cachedMapObj
local FormatTime = function(time)
  time = math.floor(time)
  local hours, minutes, seconds
  hours = math.floor(time / 3600)
  time = time % 3600
  minutes = math.floor(time / 60)
  seconds = time % 60
```

---

## EF/ExploreDungeon_AdventureEnterBtnByName.lua.lua
**Functions:**
- GetExploreDungeon_AdventureEnterBtnUis
**Snippet:**
```lua
function GetExploreDungeon_AdventureEnterBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
```

---

## EF/ExploreDungeon_BreachByName.lua.lua
**Functions:**
- GetExploreDungeon_BreachUis
**Requires:**
- CommonResource_BackGroundByName
- ExploreDungeon_Breach_TipsAniByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ExploreDungeon_Breach_TipsAniByName")
require("CommonResource_CurrencyReturnByName")

function GetExploreDungeon_BreachUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Tips1 = GetExploreDungeon_Breach_TipsAniUis(ui:GetChild("Tips1"))
  uis.Tips2 = GetExploreDungeon_Breach_TipsAniUis(ui:GetChild("Tips2"))
  uis.Tips3 = GetExploreDungeon_Breach_TipsAniUis(ui:GetChild("Tips3"))
```

---

## EF/ExploreDungeon_BreachWindowByName.lua.lua
**Functions:**
- GetExploreDungeon_BreachWindowUis
**Requires:**
- ExploreDungeon_BreachByName
**Snippet:**
```lua
require("ExploreDungeon_BreachByName")

function GetExploreDungeon_BreachWindowUis(ui)
  local uis = {}
  uis.Main = GetExploreDungeon_BreachUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_Breach_TipsAniByName.lua.lua
**Functions:**
- GetExploreDungeon_Breach_TipsAniUis
**Snippet:**
```lua
function GetExploreDungeon_Breach_TipsAniUis(ui)
  local uis = {}
  
  uis.TipsBtn = ui:GetChild("TipsBtn")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_Breach_TipsBtnByName.lua.lua
**Functions:**
- GetExploreDungeon_Breach_TipsBtnUis
**Snippet:**
```lua
function GetExploreDungeon_Breach_TipsBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_ExploreAdventureByName.lua.lua
**Functions:**
- GetExploreDungeon_ExploreAdventureUis
**Requires:**
- CommonResource_BackGroundByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("CommonResource_CurrencyReturnByName")

function GetExploreDungeon_ExploreAdventureUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.EnterList = ui:GetChild("EnterList")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.CurrencyReturn = GetCommonResource_CurrencyReturnUis(ui:GetChild("CurrencyReturn"))
  uis.root = ui
```

---

## EF/ExploreDungeon_ExploreAdventureWindowByName.lua.lua
**Functions:**
- GetExploreDungeon_ExploreAdventureWindowUis
**Requires:**
- ExploreDungeon_ExploreAdventureByName
**Snippet:**
```lua
require("ExploreDungeon_ExploreAdventureByName")

function GetExploreDungeon_ExploreAdventureWindowUis(ui)
  local uis = {}
  uis.Main = GetExploreDungeon_ExploreAdventureUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelExplainByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelExplainUis
**Requires:**
- CommonResource_PopupBgByName
- ExploreDungeon_LevelExplain_TipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ExploreDungeon_LevelExplain_TipsByName")

function GetExploreDungeon_LevelExplainUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Tips = GetExploreDungeon_LevelExplain_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
```

---

## EF/ExploreDungeon_LevelExplainWindowByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelExplainWindowUis
**Requires:**
- ExploreDungeon_LevelExplainByName
**Snippet:**
```lua
require("ExploreDungeon_LevelExplainByName")

function GetExploreDungeon_LevelExplainWindowUis(ui)
  local uis = {}
  uis.Main = GetExploreDungeon_LevelExplainUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelExplain_CloseBtnByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelExplain_CloseBtnUis
**Snippet:**
```lua
function GetExploreDungeon_LevelExplain_CloseBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelExplain_InfoByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelExplain_InfoUis
**Requires:**
- CommonResource_ItemFrameByName
**Snippet:**
```lua
require("CommonResource_ItemFrameByName")

function GetExploreDungeon_LevelExplain_InfoUis(ui)
  local uis = {}
  uis.n2 = GetCommonResource_ItemFrameUis(ui:GetChild("n2"))
  uis.NowTxt = ui:GetChild("NowTxt")
  uis.AfterTxt = ui:GetChild("AfterTxt")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelExplain_TipsByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelExplain_TipsUis
**Snippet:**
```lua
function GetExploreDungeon_LevelExplain_TipsUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.InfoList = ui:GetChild("InfoList")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelQuickByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelQuickUis
**Requires:**
- CommonResource_PopupBgByName
- ExploreDungeon_LevelQuick_TipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ExploreDungeon_LevelQuick_TipsByName")

function GetExploreDungeon_LevelQuickUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Tips = GetExploreDungeon_LevelQuick_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
```

---

## EF/ExploreDungeon_LevelQuickWindowByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelQuickWindowUis
**Requires:**
- ExploreDungeon_LevelQuickByName
**Snippet:**
```lua
require("ExploreDungeon_LevelQuickByName")

function GetExploreDungeon_LevelQuickWindowUis(ui)
  local uis = {}
  uis.Main = GetExploreDungeon_LevelQuickUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelQuick_SpendBtnByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelQuick_SpendBtnUis
**Snippet:**
```lua
function GetExploreDungeon_LevelQuick_SpendBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## EF/ExploreDungeon_LevelQuick_SureBtnByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelQuick_SureBtnUis
**Snippet:**
```lua
function GetExploreDungeon_LevelQuick_SureBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelQuick_TipsByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelQuick_TipsUis
**Snippet:**
```lua
function GetExploreDungeon_LevelQuick_TipsUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.SpendList = ui:GetChild("SpendList")
  uis.SureBtn = ui:GetChild("SureBtn")
  uis.root = ui
```

---

## EF/ExploreDungeon_LevelUpByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUpUis
**Requires:**
- CommonResource_BackGroundByName
- ExploreDungeon_LevelUp_MapRegionByName
- ExploreDungeon_LevelUp_TitleByName
- ExploreDungeon_LevelUp_AFKRegionByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ExploreDungeon_LevelUp_MapRegionByName")
require("ExploreDungeon_LevelUp_TitleByName")
require("ExploreDungeon_LevelUp_AFKRegionByName")
require("CommonResource_CurrencyReturnByName")

function GetExploreDungeon_LevelUpUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.MapRegion = GetExploreDungeon_LevelUp_MapRegionUis(ui:GetChild("MapRegion"))
```

---

## EF/ExploreDungeon_LevelUpMap01ByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUpMap01Uis
**Requires:**
- ExploreDungeon_LevelUp_TipsAniByName
**Snippet:**
```lua
require("ExploreDungeon_LevelUp_TipsAniByName")

function GetExploreDungeon_LevelUpMap01Uis(ui)
  local uis = {}
  uis.Tips1 = GetExploreDungeon_LevelUp_TipsAniUis(ui:GetChild("Tips1"))
  uis.Tips2 = GetExploreDungeon_LevelUp_TipsAniUis(ui:GetChild("Tips2"))
  uis.Tips3 = GetExploreDungeon_LevelUp_TipsAniUis(ui:GetChild("Tips3"))
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelUpMap02ByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUpMap02Uis
**Requires:**
- ExploreDungeon_LevelUp_TipsAniByName
**Snippet:**
```lua
require("ExploreDungeon_LevelUp_TipsAniByName")

function GetExploreDungeon_LevelUpMap02Uis(ui)
  local uis = {}
  uis.Tips1 = GetExploreDungeon_LevelUp_TipsAniUis(ui:GetChild("Tips1"))
  uis.Tips2 = GetExploreDungeon_LevelUp_TipsAniUis(ui:GetChild("Tips2"))
  uis.Tips3 = GetExploreDungeon_LevelUp_TipsAniUis(ui:GetChild("Tips3"))
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelUpMap03ByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUpMap03Uis
**Requires:**
- ExploreDungeon_LevelUp_TipsAniByName
**Snippet:**
```lua
require("ExploreDungeon_LevelUp_TipsAniByName")

function GetExploreDungeon_LevelUpMap03Uis(ui)
  local uis = {}
  uis.Tips1 = GetExploreDungeon_LevelUp_TipsAniUis(ui:GetChild("Tips1"))
  uis.Tips2 = GetExploreDungeon_LevelUp_TipsAniUis(ui:GetChild("Tips2"))
  uis.Tips3 = GetExploreDungeon_LevelUp_TipsAniUis(ui:GetChild("Tips3"))
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelUpMap04ByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUpMap04Uis
**Requires:**
- ExploreDungeon_LevelUp_TipsAniByName
**Snippet:**
```lua
require("ExploreDungeon_LevelUp_TipsAniByName")

function GetExploreDungeon_LevelUpMap04Uis(ui)
  local uis = {}
  uis.Tips1 = GetExploreDungeon_LevelUp_TipsAniUis(ui:GetChild("Tips1"))
  uis.Tips2 = GetExploreDungeon_LevelUp_TipsAniUis(ui:GetChild("Tips2"))
  uis.Tips3 = GetExploreDungeon_LevelUp_TipsAniUis(ui:GetChild("Tips3"))
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelUpMap05ByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUpMap05Uis
**Requires:**
- ExploreDungeon_LevelUp_TipsAniByName
**Snippet:**
```lua
require("ExploreDungeon_LevelUp_TipsAniByName")

function GetExploreDungeon_LevelUpMap05Uis(ui)
  local uis = {}
  uis.Tips1 = GetExploreDungeon_LevelUp_TipsAniUis(ui:GetChild("Tips1"))
  uis.Tips2 = GetExploreDungeon_LevelUp_TipsAniUis(ui:GetChild("Tips2"))
  uis.Tips3 = GetExploreDungeon_LevelUp_TipsAniUis(ui:GetChild("Tips3"))
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelUpWindowByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUpWindowUis
**Requires:**
- ExploreDungeon_LevelUpByName
**Snippet:**
```lua
require("ExploreDungeon_LevelUpByName")

function GetExploreDungeon_LevelUpWindowUis(ui)
  local uis = {}
  uis.Main = GetExploreDungeon_LevelUpUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelUp_AFKRegionByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUp_AFKRegionUis
**Requires:**
- ExploreDungeon_LevelUp_QuickGetNumberByName
**Snippet:**
```lua
require("ExploreDungeon_LevelUp_QuickGetNumberByName")

function GetExploreDungeon_LevelUp_AFKRegionUis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.ProduceList = ui:GetChild("ProduceList")
  uis.RewardList = ui:GetChild("RewardList")
  uis.ProduceProgressBar = ui:GetChild("ProduceProgressBar")
  uis.QuickGetBtn = ui:GetChild("QuickGetBtn")
  uis.GetBtn = ui:GetChild("GetBtn")
```

---

## EF/ExploreDungeon_LevelUp_ExplainBtnByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUp_ExplainBtnUis
**Snippet:**
```lua
function GetExploreDungeon_LevelUp_ExplainBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelUp_ExpProgressBarByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUp_ExpProgressBarUis
**Requires:**
- ExploreDungeon_LevelUp_ExpProgressFillByName
**Snippet:**
```lua
require("ExploreDungeon_LevelUp_ExpProgressFillByName")

function GetExploreDungeon_LevelUp_ExpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetExploreDungeon_LevelUp_ExpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelUp_ExpProgressFillByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUp_ExpProgressFillUis
**Snippet:**
```lua
function GetExploreDungeon_LevelUp_ExpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelUp_GetBtnByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUp_GetBtnUis
**Snippet:**
```lua
function GetExploreDungeon_LevelUp_GetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelUp_MapRegionByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUp_MapRegionUis
**Snippet:**
```lua
function GetExploreDungeon_LevelUp_MapRegionUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelUp_NewByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUp_NewUis
**Snippet:**
```lua
function GetExploreDungeon_LevelUp_NewUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelUp_ProduceByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUp_ProduceUis
**Snippet:**
```lua
function GetExploreDungeon_LevelUp_ProduceUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelUp_ProduceProgressBarByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUp_ProduceProgressBarUis
**Requires:**
- ExploreDungeon_LevelUp_ProduceProgressFillByName
**Snippet:**
```lua
require("ExploreDungeon_LevelUp_ProduceProgressFillByName")

function GetExploreDungeon_LevelUp_ProduceProgressBarUis(ui)
  local uis = {}
  uis.bar = GetExploreDungeon_LevelUp_ProduceProgressFillUis(ui:GetChild("bar"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ScaleHolder = ui:GetChild("ScaleHolder")
  uis.ScaleLoader = ui:GetChild("ScaleLoader")
  uis.root = ui
  return uis
```

---

## EF/ExploreDungeon_LevelUp_ProduceProgressFillByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUp_ProduceProgressFillUis
**Snippet:**
```lua
function GetExploreDungeon_LevelUp_ProduceProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelUp_QuickGetBtnByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUp_QuickGetBtnUis
**Snippet:**
```lua
function GetExploreDungeon_LevelUp_QuickGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelUp_QuickGetNumberByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUp_QuickGetNumberUis
**Snippet:**
```lua
function GetExploreDungeon_LevelUp_QuickGetNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelUp_RoundByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUp_RoundUis
**Snippet:**
```lua
function GetExploreDungeon_LevelUp_RoundUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelUp_ShopBtnByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUp_ShopBtnUis
**Snippet:**
```lua
function GetExploreDungeon_LevelUp_ShopBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelUp_TabBtnByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUp_TabBtnUis
**Snippet:**
```lua
function GetExploreDungeon_LevelUp_TabBtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelUp_TipsAniByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUp_TipsAniUis
**Snippet:**
```lua
function GetExploreDungeon_LevelUp_TipsAniUis(ui)
  local uis = {}
  
  uis.TipsBtn = ui:GetChild("TipsBtn")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelUp_TipsBtnByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUp_TipsBtnUis
**Requires:**
- ExploreDungeon_LevelUp_TipsRoundByName
- ExploreDungeon_LevelUp_NewByName
- ExploreDungeon_LevelUp_TitleLockByName
**Snippet:**
```lua
require("ExploreDungeon_LevelUp_TipsRoundByName")
require("ExploreDungeon_LevelUp_NewByName")
require("ExploreDungeon_LevelUp_TitleLockByName")

function GetExploreDungeon_LevelUp_TipsBtnUis(ui)
  local uis = {}
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.TipsRound = GetExploreDungeon_LevelUp_TipsRoundUis(ui:GetChild("TipsRound"))
  uis.New = GetExploreDungeon_LevelUp_NewUis(ui:GetChild("New"))
  uis.Lock = GetExploreDungeon_LevelUp_TitleLockUis(ui:GetChild("Lock"))
```

---

## EF/ExploreDungeon_LevelUp_TipsRoundByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUp_TipsRoundUis
**Snippet:**
```lua
function GetExploreDungeon_LevelUp_TipsRoundUis(ui)
  local uis = {}
  
  uis.RoundList = ui:GetChild("RoundList")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreDungeon_LevelUp_TitleByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUp_TitleUis
**Snippet:**
```lua
function GetExploreDungeon_LevelUp_TitleUis(ui)
  local uis = {}
  
  uis.ExpProgressBar = ui:GetChild("ExpProgressBar")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.ExpTxt = ui:GetChild("ExpTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ExpMaxTxt = ui:GetChild("ExpMaxTxt")
```

---

## EF/ExploreDungeon_LevelUp_TitleLockByName.lua.lua
**Functions:**
- GetExploreDungeon_LevelUp_TitleLockUis
**Snippet:**
```lua
function GetExploreDungeon_LevelUp_TitleLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSettlementWindow.lua.lua
**Functions:**
- ExploreSettlementWindow.ReInitData
- ExploreSettlementWindow.OnInit
- ExploreSettlementWindow.UpdateInfo
- cardlist.itemRenderer
- rewardlist.itemRenderer
- ExploreSettlementWindow.InitBtn
- ExploreSettlementWindow.OnClose
**Requires:**
- Explore_SettlementWindowByName
**Snippet:**
```lua
require("Explore_SettlementWindowByName")
local ExploreSettlementWindow = {}
local uis, contentPane, prevExp, prevLevel, cards, rewardId, rewards, soundEvent
local PlayLevelupExpIncrease = function(gcmp, prevLevel, prevExp, curLevel, curExp, onComplete)
  local progressBar = gcmp:GetChild("ExpProgressBar")
  local maxLevel = ExploreAFKData.GetMaxLevel()
  local levelup = prevLevel < curLevel
  local alreadyMaxLevel = prevLevel >= maxLevel
  local currentMaxLevel = curLevel >= maxLevel
  local threshold = ExploreAFKData.GetLevelExpThreshold(prevLevel)
```

---

## EF/ExploreSign01_CloseBtnByName.lua.lua
**Functions:**
- GetExploreSign01_CloseBtnUis
**Snippet:**
```lua
function GetExploreSign01_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign01_EffectByName.lua.lua
**Functions:**
- GetExploreSign01_EffectUis
**Snippet:**
```lua
function GetExploreSign01_EffectUis(ui)
  local uis = {}
  
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign01_ExploreBtnAniByName.lua.lua
**Functions:**
- GetExploreSign01_ExploreBtnAniUis
**Snippet:**
```lua
function GetExploreSign01_ExploreBtnAniUis(ui)
  local uis = {}
  
  uis.ExploreBtn = ui:GetChild("ExploreBtn")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign01_ExploreBtnByName.lua.lua
**Functions:**
- GetExploreSign01_ExploreBtnUis
**Snippet:**
```lua
function GetExploreSign01_ExploreBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign01_ExploreSignByName.lua.lua
**Functions:**
- GetExploreSign01_ExploreSignUis
**Requires:**
- CommonResource_PopupBgByName
- ExploreSign01_MapByName
- ExploreSign01_ExploreBtnAniByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ExploreSign01_MapByName")
require("ExploreSign01_ExploreBtnAniByName")

function GetExploreSign01_ExploreSignUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.Map = GetExploreSign01_MapUis(ui:GetChild("Map"))
  uis.Explore = GetExploreSign01_ExploreBtnAniUis(ui:GetChild("Explore"))
  uis.CloseBtn = ui:GetChild("CloseBtn")
```

---

## EF/ExploreSign01_ExploreSignWindowByName.lua.lua
**Functions:**
- GetExploreSign01_ExploreSignWindowUis
**Requires:**
- ExploreSign01_ExploreSignByName
**Snippet:**
```lua
require("ExploreSign01_ExploreSignByName")

function GetExploreSign01_ExploreSignWindowUis(ui)
  local uis = {}
  uis.Main = GetExploreSign01_ExploreSignUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign01_ExploreWordByName.lua.lua
**Functions:**
- GetExploreSign01_ExploreWordUis
**Snippet:**
```lua
function GetExploreSign01_ExploreWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign01_GetWordByName.lua.lua
**Functions:**
- GetExploreSign01_GetWordUis
**Snippet:**
```lua
function GetExploreSign01_GetWordUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign01_MapByName.lua.lua
**Functions:**
- GetExploreSign01_MapUis
**Requires:**
- ExploreSign01_ExploreWordByName
- ExploreSign01_Place1AniByName
- ExploreSign01_Place2AniByName
- ExploreSign01_Place3AniByName
- ExploreSign01_Place4AniByName
- ExploreSign01_Place5AniByName
- ExploreSign01_Place6AniByName
**Snippet:**
```lua
require("ExploreSign01_ExploreWordByName")
require("ExploreSign01_Place1AniByName")
require("ExploreSign01_Place2AniByName")
require("ExploreSign01_Place3AniByName")
require("ExploreSign01_Place4AniByName")
require("ExploreSign01_Place5AniByName")
require("ExploreSign01_Place6AniByName")

function GetExploreSign01_MapUis(ui)
  local uis = {}
```

---

## EF/ExploreSign01_Place1AniByName.lua.lua
**Functions:**
- GetExploreSign01_Place1AniUis
**Snippet:**
```lua
function GetExploreSign01_Place1AniUis(ui)
  local uis = {}
  
  uis.PlaceBtn = ui:GetChild("PlaceBtn")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign01_Place1BtnByName.lua.lua
**Functions:**
- GetExploreSign01_Place1BtnUis
**Requires:**
- ExploreSign01_GetWordByName
**Snippet:**
```lua
require("ExploreSign01_GetWordByName")

function GetExploreSign01_Place1BtnUis(ui)
  local uis = {}
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.GetWord = GetExploreSign01_GetWordUis(ui:GetChild("GetWord"))
  uis.buttonCtr = ui:GetController("button")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## EF/ExploreSign01_Place2AniByName.lua.lua
**Functions:**
- GetExploreSign01_Place2AniUis
**Snippet:**
```lua
function GetExploreSign01_Place2AniUis(ui)
  local uis = {}
  
  uis.PlaceBtn = ui:GetChild("PlaceBtn")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign01_Place2BtnByName.lua.lua
**Functions:**
- GetExploreSign01_Place2BtnUis
**Requires:**
- ExploreSign01_GetWordByName
**Snippet:**
```lua
require("ExploreSign01_GetWordByName")

function GetExploreSign01_Place2BtnUis(ui)
  local uis = {}
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.GetWord = GetExploreSign01_GetWordUis(ui:GetChild("GetWord"))
  uis.buttonCtr = ui:GetController("button")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## EF/ExploreSign01_Place3AniByName.lua.lua
**Functions:**
- GetExploreSign01_Place3AniUis
**Snippet:**
```lua
function GetExploreSign01_Place3AniUis(ui)
  local uis = {}
  
  uis.PlaceBtn = ui:GetChild("PlaceBtn")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign01_Place3BtnByName.lua.lua
**Functions:**
- GetExploreSign01_Place3BtnUis
**Requires:**
- ExploreSign01_GetWordByName
**Snippet:**
```lua
require("ExploreSign01_GetWordByName")

function GetExploreSign01_Place3BtnUis(ui)
  local uis = {}
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.GetWord = GetExploreSign01_GetWordUis(ui:GetChild("GetWord"))
  uis.buttonCtr = ui:GetController("button")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## EF/ExploreSign01_Place4AniByName.lua.lua
**Functions:**
- GetExploreSign01_Place4AniUis
**Snippet:**
```lua
function GetExploreSign01_Place4AniUis(ui)
  local uis = {}
  
  uis.PlaceBtn = ui:GetChild("PlaceBtn")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign01_Place4BtnByName.lua.lua
**Functions:**
- GetExploreSign01_Place4BtnUis
**Requires:**
- ExploreSign01_GetWordByName
**Snippet:**
```lua
require("ExploreSign01_GetWordByName")

function GetExploreSign01_Place4BtnUis(ui)
  local uis = {}
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.GetWord = GetExploreSign01_GetWordUis(ui:GetChild("GetWord"))
  uis.buttonCtr = ui:GetController("button")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## EF/ExploreSign01_Place5AniByName.lua.lua
**Functions:**
- GetExploreSign01_Place5AniUis
**Snippet:**
```lua
function GetExploreSign01_Place5AniUis(ui)
  local uis = {}
  
  uis.PlaceBtn = ui:GetChild("PlaceBtn")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign01_Place5BtnByName.lua.lua
**Functions:**
- GetExploreSign01_Place5BtnUis
**Requires:**
- ExploreSign01_GetWordByName
**Snippet:**
```lua
require("ExploreSign01_GetWordByName")

function GetExploreSign01_Place5BtnUis(ui)
  local uis = {}
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.GetWord = GetExploreSign01_GetWordUis(ui:GetChild("GetWord"))
  uis.buttonCtr = ui:GetController("button")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## EF/ExploreSign01_Place6AniByName.lua.lua
**Functions:**
- GetExploreSign01_Place6AniUis
**Snippet:**
```lua
function GetExploreSign01_Place6AniUis(ui)
  local uis = {}
  
  uis.PlaceBtn = ui:GetChild("PlaceBtn")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign01_Place6BtnByName.lua.lua
**Functions:**
- GetExploreSign01_Place6BtnUis
**Requires:**
- ExploreSign01_GetWordByName
**Snippet:**
```lua
require("ExploreSign01_GetWordByName")

function GetExploreSign01_Place6BtnUis(ui)
  local uis = {}
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.GetWord = GetExploreSign01_GetWordUis(ui:GetChild("GetWord"))
  uis.buttonCtr = ui:GetController("button")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## EF/ExploreSign02_CloseBtnByName.lua.lua
**Functions:**
- GetExploreSign02_CloseBtnUis
**Snippet:**
```lua
function GetExploreSign02_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign02_EffectByName.lua.lua
**Functions:**
- GetExploreSign02_EffectUis
**Snippet:**
```lua
function GetExploreSign02_EffectUis(ui)
  local uis = {}
  
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign02_ExploreBtnAniByName.lua.lua
**Functions:**
- GetExploreSign02_ExploreBtnAniUis
**Snippet:**
```lua
function GetExploreSign02_ExploreBtnAniUis(ui)
  local uis = {}
  
  uis.ExploreBtn = ui:GetChild("ExploreBtn")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign02_ExploreBtnByName.lua.lua
**Functions:**
- GetExploreSign02_ExploreBtnUis
**Snippet:**
```lua
function GetExploreSign02_ExploreBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign02_ExploreSignByName.lua.lua
**Functions:**
- GetExploreSign02_ExploreSignUis
**Requires:**
- CommonResource_PopupBgByName
- ExploreSign02_MapByName
- ExploreSign02_ExploreBtnAniByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ExploreSign02_MapByName")
require("ExploreSign02_ExploreBtnAniByName")

function GetExploreSign02_ExploreSignUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.Map = GetExploreSign02_MapUis(ui:GetChild("Map"))
  uis.Explore = GetExploreSign02_ExploreBtnAniUis(ui:GetChild("Explore"))
  uis.CloseBtn = ui:GetChild("CloseBtn")
```

---

## EF/ExploreSign02_ExploreSignWindowByName.lua.lua
**Functions:**
- GetExploreSign02_ExploreSignWindowUis
**Requires:**
- ExploreSign02_ExploreSignByName
**Snippet:**
```lua
require("ExploreSign02_ExploreSignByName")

function GetExploreSign02_ExploreSignWindowUis(ui)
  local uis = {}
  uis.Main = GetExploreSign02_ExploreSignUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign02_ExploreWordByName.lua.lua
**Functions:**
- GetExploreSign02_ExploreWordUis
**Snippet:**
```lua
function GetExploreSign02_ExploreWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign02_GetWordByName.lua.lua
**Functions:**
- GetExploreSign02_GetWordUis
**Snippet:**
```lua
function GetExploreSign02_GetWordUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign02_MapByName.lua.lua
**Functions:**
- GetExploreSign02_MapUis
**Requires:**
- ExploreSign02_ExploreWordByName
- ExploreSign02_Place1AniByName
- ExploreSign02_Place2AniByName
- ExploreSign02_Place3AniByName
- ExploreSign02_Place4AniByName
- ExploreSign02_Place5AniByName
- ExploreSign02_Place6AniByName
**Snippet:**
```lua
require("ExploreSign02_ExploreWordByName")
require("ExploreSign02_Place1AniByName")
require("ExploreSign02_Place2AniByName")
require("ExploreSign02_Place3AniByName")
require("ExploreSign02_Place4AniByName")
require("ExploreSign02_Place5AniByName")
require("ExploreSign02_Place6AniByName")

function GetExploreSign02_MapUis(ui)
  local uis = {}
```

---

## EF/ExploreSign02_Place1AniByName.lua.lua
**Functions:**
- GetExploreSign02_Place1AniUis
**Snippet:**
```lua
function GetExploreSign02_Place1AniUis(ui)
  local uis = {}
  
  uis.PlaceBtn = ui:GetChild("PlaceBtn")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign02_Place1BtnByName.lua.lua
**Functions:**
- GetExploreSign02_Place1BtnUis
**Requires:**
- ExploreSign02_GetWordByName
**Snippet:**
```lua
require("ExploreSign02_GetWordByName")

function GetExploreSign02_Place1BtnUis(ui)
  local uis = {}
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.GetWord = GetExploreSign02_GetWordUis(ui:GetChild("GetWord"))
  uis.buttonCtr = ui:GetController("button")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## EF/ExploreSign02_Place2AniByName.lua.lua
**Functions:**
- GetExploreSign02_Place2AniUis
**Snippet:**
```lua
function GetExploreSign02_Place2AniUis(ui)
  local uis = {}
  
  uis.PlaceBtn = ui:GetChild("PlaceBtn")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign02_Place2BtnByName.lua.lua
**Functions:**
- GetExploreSign02_Place2BtnUis
**Requires:**
- ExploreSign02_GetWordByName
**Snippet:**
```lua
require("ExploreSign02_GetWordByName")

function GetExploreSign02_Place2BtnUis(ui)
  local uis = {}
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.GetWord = GetExploreSign02_GetWordUis(ui:GetChild("GetWord"))
  uis.buttonCtr = ui:GetController("button")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## EF/ExploreSign02_Place3AniByName.lua.lua
**Functions:**
- GetExploreSign02_Place3AniUis
**Snippet:**
```lua
function GetExploreSign02_Place3AniUis(ui)
  local uis = {}
  
  uis.PlaceBtn = ui:GetChild("PlaceBtn")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign02_Place3BtnByName.lua.lua
**Functions:**
- GetExploreSign02_Place3BtnUis
**Requires:**
- ExploreSign02_GetWordByName
**Snippet:**
```lua
require("ExploreSign02_GetWordByName")

function GetExploreSign02_Place3BtnUis(ui)
  local uis = {}
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.GetWord = GetExploreSign02_GetWordUis(ui:GetChild("GetWord"))
  uis.buttonCtr = ui:GetController("button")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## EF/ExploreSign02_Place4AniByName.lua.lua
**Functions:**
- GetExploreSign02_Place4AniUis
**Snippet:**
```lua
function GetExploreSign02_Place4AniUis(ui)
  local uis = {}
  
  uis.PlaceBtn = ui:GetChild("PlaceBtn")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign02_Place4BtnByName.lua.lua
**Functions:**
- GetExploreSign02_Place4BtnUis
**Requires:**
- ExploreSign02_GetWordByName
**Snippet:**
```lua
require("ExploreSign02_GetWordByName")

function GetExploreSign02_Place4BtnUis(ui)
  local uis = {}
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.GetWord = GetExploreSign02_GetWordUis(ui:GetChild("GetWord"))
  uis.buttonCtr = ui:GetController("button")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## EF/ExploreSign02_Place5AniByName.lua.lua
**Functions:**
- GetExploreSign02_Place5AniUis
**Snippet:**
```lua
function GetExploreSign02_Place5AniUis(ui)
  local uis = {}
  
  uis.PlaceBtn = ui:GetChild("PlaceBtn")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign02_Place5BtnByName.lua.lua
**Functions:**
- GetExploreSign02_Place5BtnUis
**Requires:**
- ExploreSign02_GetWordByName
**Snippet:**
```lua
require("ExploreSign02_GetWordByName")

function GetExploreSign02_Place5BtnUis(ui)
  local uis = {}
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.GetWord = GetExploreSign02_GetWordUis(ui:GetChild("GetWord"))
  uis.buttonCtr = ui:GetController("button")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## EF/ExploreSign02_Place6AniByName.lua.lua
**Functions:**
- GetExploreSign02_Place6AniUis
**Snippet:**
```lua
function GetExploreSign02_Place6AniUis(ui)
  local uis = {}
  
  uis.PlaceBtn = ui:GetChild("PlaceBtn")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign02_Place6BtnByName.lua.lua
**Functions:**
- GetExploreSign02_Place6BtnUis
**Requires:**
- ExploreSign02_GetWordByName
**Snippet:**
```lua
require("ExploreSign02_GetWordByName")

function GetExploreSign02_Place6BtnUis(ui)
  local uis = {}
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.GetWord = GetExploreSign02_GetWordUis(ui:GetChild("GetWord"))
  uis.buttonCtr = ui:GetController("button")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## EF/ExploreSign1Window.lua.lua
**Functions:**
- ExploreSign1Window.ReInitData
- ExploreSign1Window.OnInit
- ExploreSign1Window.ShowItem
- ExploreSign1Window.UpdateTextDisplay
- ExploreSign1Window.InitBtn
- ExploreSign1Window.ShowItemReward
- ExploreSign1Window.ShowReward
- ExploreSign1Window.ShowRewardEffect
- ExploreSign1Window.OnClose
- ExploreSign1Window.CheckActivityEnd
- ExploreSign1Window.HandleMessage
**Requires:**
- ExploreSign01_ExploreSignWindowByName
**Snippet:**
```lua
require("ExploreSign01_ExploreSignWindowByName")
local ExploreSign1Window = {}
local uis, contentPane, data, activityData, signIndex, isAct, pos, showIndex

function ExploreSign1Window.ReInitData()
end

function ExploreSign1Window.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ExploreSign1Window.package, WinResConfig.ExploreSign1Window.comName, function(com)
    contentPane = com
```

---

## EF/ExploreSign2Window.lua.lua
**Functions:**
- ExploreSign2Window.ReInitData
- ExploreSign2Window.OnInit
- ExploreSign2Window.ShowItem
- ExploreSign2Window.UpdateTextDisplay
- ExploreSign2Window.InitBtn
- ExploreSign2Window.ShowItemReward
- ExploreSign2Window.ShowReward
- ExploreSign2Window.ShowRewardEffect
- ExploreSign2Window.OnClose
- ExploreSign2Window.CheckActivityEnd
- ExploreSign2Window.HandleMessage
**Requires:**
- ExploreSign02_ExploreSignWindowByName
**Snippet:**
```lua
require("ExploreSign02_ExploreSignWindowByName")
local ExploreSign2Window = {}
local uis, contentPane, data, activityData, signIndex, isAct, pos, showIndex

function ExploreSign2Window.ReInitData()
end

function ExploreSign2Window.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ExploreSign2Window.package, WinResConfig.ExploreSign2Window.comName, function(com)
    contentPane = com
```

---

## EF/ExploreSignEndWindow.lua.lua
**Functions:**
- ExploreSignEndWindow.OnInit
- ExploreSignEndWindow.InitList
- uis.Main.ItemList.itemRenderer
- ExploreSignEndWindow.UpdateTextDisplay
- ExploreSignEndWindow.InitBtn
- ExploreSignEndWindow.HandleMessage
- ExploreSignEndWindow.OnClose
**Requires:**
- ExploreSign_EndWindowByName
**Snippet:**
```lua
require("ExploreSign_EndWindowByName")
local ExploreSignEndWindow = {}
local uis, contentPane, param

function ExploreSignEndWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ExploreSignEndWindow.package, WinResConfig.ExploreSignEndWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetExploreSign_EndWindowUis(contentPane)
    param = bridgeObj.argTable[1]
```

---

## EF/ExploreSignWindow.lua.lua
**Functions:**
- ExploreSignWindow.OnInit
- ExploreSignWindow.ShowItem
- ExploreSignWindow.UpdateTextDisplay
- ExploreSignWindow.InitBtn
- ExploreSignWindow.ShowItemReward
- ExploreSignWindow.ShowReward
- ExploreSignWindow.ShowRewardEffect
- ExploreSignWindow.HandleMessage
- ExploreSignWindow.OnClose
**Requires:**
- ExploreSign_ExploreSignWindowByName
**Snippet:**
```lua
require("ExploreSign_ExploreSignWindowByName")
local ExploreSignWindow = {}
local uis, contentPane, data, activityData, signIndex, isAct, pos
local unChoose = "Assets/Art/Effects/Prefab/UI_prefab/spcheckin/FX_ui_spcheckin_unchoose.prefab"
local choose = "Assets/Art/Effects/Prefab/UI_prefab/spcheckin/FX_ui_spcheckin_choose.prefab"
local search = "Assets/Art/Effects/Prefab/UI_prefab/spcheckin/FX_ui_spcheckin_serch.prefab"
local effectIn = "Assets/Art/Effects/Prefab/UI_prefab/NewGuyCheckin/FX_ui_spcheckin_in.prefab"
local effBg = "Assets/Art/Effects/Prefab/UI_prefab/NewGuyCheckin/FX_ui_spcheckin_eff.prefab"
local showIndex

```

---

## EF/ExploreSign_CloseBtnByName.lua.lua
**Functions:**
- GetExploreSign_CloseBtnUis
**Snippet:**
```lua
function GetExploreSign_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign_EffectByName.lua.lua
**Functions:**
- GetExploreSign_EffectUis
**Snippet:**
```lua
function GetExploreSign_EffectUis(ui)
  local uis = {}
  
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign_EndBgByName.lua.lua
**Functions:**
- GetExploreSign_EndBgUis
**Snippet:**
```lua
function GetExploreSign_EndBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign_EndByName.lua.lua
**Functions:**
- GetExploreSign_EndUis
**Requires:**
- CommonResource_PopupBgByName
- ExploreSign_EndBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ExploreSign_EndBgByName")

function GetExploreSign_EndUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.EndBg = GetExploreSign_EndBgUis(ui:GetChild("EndBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
```

---

## EF/ExploreSign_EndWindowByName.lua.lua
**Functions:**
- GetExploreSign_EndWindowUis
**Requires:**
- ExploreSign_EndByName
**Snippet:**
```lua
require("ExploreSign_EndByName")

function GetExploreSign_EndWindowUis(ui)
  local uis = {}
  uis.Main = GetExploreSign_EndUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign_ExploreBtnAniByName.lua.lua
**Functions:**
- GetExploreSign_ExploreBtnAniUis
**Snippet:**
```lua
function GetExploreSign_ExploreBtnAniUis(ui)
  local uis = {}
  
  uis.ExploreBtn = ui:GetChild("ExploreBtn")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign_ExploreBtnByName.lua.lua
**Functions:**
- GetExploreSign_ExploreBtnUis
**Snippet:**
```lua
function GetExploreSign_ExploreBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign_ExploreSignByName.lua.lua
**Functions:**
- GetExploreSign_ExploreSignUis
**Requires:**
- CommonResource_PopupBgByName
- ExploreSign_MapByName
- ExploreSign_TitleByName
- ExploreSign_ExploreBtnAniByName
- ExploreSign_TipsWordByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ExploreSign_MapByName")
require("ExploreSign_TitleByName")
require("ExploreSign_ExploreBtnAniByName")
require("ExploreSign_TipsWordByName")

function GetExploreSign_ExploreSignUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.Map = GetExploreSign_MapUis(ui:GetChild("Map"))
```

---

## EF/ExploreSign_ExploreSignWindowByName.lua.lua
**Functions:**
- GetExploreSign_ExploreSignWindowUis
**Requires:**
- ExploreSign_ExploreSignByName
**Snippet:**
```lua
require("ExploreSign_ExploreSignByName")

function GetExploreSign_ExploreSignWindowUis(ui)
  local uis = {}
  uis.Main = GetExploreSign_ExploreSignUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign_GetWordByName.lua.lua
**Functions:**
- GetExploreSign_GetWordUis
**Snippet:**
```lua
function GetExploreSign_GetWordUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign_MapByName.lua.lua
**Functions:**
- GetExploreSign_MapUis
**Requires:**
- ExploreSign_PlaceAniByName
**Snippet:**
```lua
require("ExploreSign_PlaceAniByName")

function GetExploreSign_MapUis(ui)
  local uis = {}
  uis.MapLoader = ui:GetChild("MapLoader")
  uis.MapHolder = ui:GetChild("MapHolder")
  uis.Place1Btn = GetExploreSign_PlaceAniUis(ui:GetChild("Place1Btn"))
  uis.Place2Btn = GetExploreSign_PlaceAniUis(ui:GetChild("Place2Btn"))
  uis.Place3Btn = GetExploreSign_PlaceAniUis(ui:GetChild("Place3Btn"))
  uis.Place4Btn = GetExploreSign_PlaceAniUis(ui:GetChild("Place4Btn"))
```

---

## EF/ExploreSign_PlaceAniByName.lua.lua
**Functions:**
- GetExploreSign_PlaceAniUis
**Snippet:**
```lua
function GetExploreSign_PlaceAniUis(ui)
  local uis = {}
  
  uis.PlaceBtn = ui:GetChild("PlaceBtn")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign_PlaceBtnByName.lua.lua
**Functions:**
- GetExploreSign_PlaceBtnUis
**Requires:**
- ExploreSign_EffectByName
- ExploreSign_SelectedWordByName
- ExploreSign_GetWordByName
**Snippet:**
```lua
require("ExploreSign_EffectByName")
require("ExploreSign_SelectedWordByName")
require("ExploreSign_GetWordByName")

function GetExploreSign_PlaceBtnUis(ui)
  local uis = {}
  uis.Effect = GetExploreSign_EffectUis(ui:GetChild("Effect"))
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.SelectedWord = GetExploreSign_SelectedWordUis(ui:GetChild("SelectedWord"))
```

---

## EF/ExploreSign_SelectedWordByName.lua.lua
**Functions:**
- GetExploreSign_SelectedWordUis
**Snippet:**
```lua
function GetExploreSign_SelectedWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign_TipsWordByName.lua.lua
**Functions:**
- GetExploreSign_TipsWordUis
**Snippet:**
```lua
function GetExploreSign_TipsWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreSign_TitleByName.lua.lua
**Functions:**
- GetExploreSign_TitleUis
**Snippet:**
```lua
function GetExploreSign_TitleUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.TimeWordTxt = ui:GetChild("TimeWordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## EF/ExploreWindow.lua.lua
**Functions:**
- ExploreWindow.ReInitData
- ExploreWindow.OnInit
- ExploreWindow.UpdateInfo
- ExploreWindow.InitBtn
- ExploreWindow.OnClose
**Requires:**
- Explore_ExploreWindowByName
**Snippet:**
```lua
require("Explore_ExploreWindowByName")
local ExploreWindow = {}
local uis, contentPane

function ExploreWindow.ReInitData()
end

function ExploreWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ExploreWindow.package, WinResConfig.ExploreWindow.comName, function(com)
    contentPane = com
```

---

## EF/Explore_AFKCardChoiceBtnByName.lua.lua
**Functions:**
- GetExplore_AFKCardChoiceBtnUis
**Requires:**
- CommonResource_OccupationByName
**Snippet:**
```lua
require("CommonResource_OccupationByName")

function GetExplore_AFKCardChoiceBtnUis(ui)
  local uis = {}
  uis.QBHolder = ui:GetChild("QBHolder")
  uis.Occupation = GetCommonResource_OccupationUis(ui:GetChild("Occupation"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## EF/Explore_AFKCountdownByName.lua.lua
**Functions:**
- GetExplore_AFKCountdownUis
**Requires:**
- Explore_AFKCountdownTimeByName
**Snippet:**
```lua
require("Explore_AFKCountdownTimeByName")

function GetExplore_AFKCountdownUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Time = GetExplore_AFKCountdownTimeUis(ui:GetChild("Time"))
  uis.CountdownProgressBar = ui:GetChild("CountdownProgressBar")
  uis.WordTipsTxt = ui:GetChild("WordTipsTxt")
  uis.root = ui
  return uis
```

---

## EF/Explore_AFKCountdownProgressBarByName.lua.lua
**Functions:**
- GetExplore_AFKCountdownProgressBarUis
**Requires:**
- Explore_AFKCountdownProgressFillByName
**Snippet:**
```lua
require("Explore_AFKCountdownProgressFillByName")

function GetExplore_AFKCountdownProgressBarUis(ui)
  local uis = {}
  uis.bar = GetExplore_AFKCountdownProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## EF/Explore_AFKCountdownProgressFillByName.lua.lua
**Functions:**
- GetExplore_AFKCountdownProgressFillUis
**Snippet:**
```lua
function GetExplore_AFKCountdownProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## EF/Explore_AFKCountdownTimeByName.lua.lua
**Functions:**
- GetExplore_AFKCountdownTimeUis
**Snippet:**
```lua
function GetExplore_AFKCountdownTimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Explore_AFKEndByName.lua.lua
**Functions:**
- GetExplore_AFKEndUis
**Snippet:**
```lua
function GetExplore_AFKEndUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Explore_AFKExpProgressBarByName.lua.lua
**Functions:**
- GetExplore_AFKExpProgressBarUis
**Requires:**
- Explore_AFKExpProgressFillByName
**Snippet:**
```lua
require("Explore_AFKExpProgressFillByName")

function GetExplore_AFKExpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetExplore_AFKExpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## EF/Explore_AFKExpProgressFillByName.lua.lua
**Functions:**
- GetExplore_AFKExpProgressFillUis
**Snippet:**
```lua
function GetExplore_AFKExpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## EF/Explore_AFKGetBtnByName.lua.lua
**Functions:**
- GetExplore_AFKGetBtnUis
**Snippet:**
```lua
function GetExplore_AFKGetBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Explore_AFKGiveUpBtnByName.lua.lua
**Functions:**
- GetExplore_AFKGiveUpBtnUis
**Snippet:**
```lua
function GetExplore_AFKGiveUpBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Explore_AFKRegoinByName.lua.lua
**Functions:**
- GetExplore_AFKRegoinUis
**Requires:**
- Explore_AFKTimeChoiceRegionByName
- Explore_AFKRewardUpRegionByName
- Explore_AFKCountdownByName
- Explore_AFKEndByName
- Explore_AFKUseWordByName
**Snippet:**
```lua
require("Explore_AFKTimeChoiceRegionByName")
require("Explore_AFKRewardUpRegionByName")
require("Explore_AFKCountdownByName")
require("Explore_AFKEndByName")
require("Explore_AFKUseWordByName")

function GetExplore_AFKRegoinUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.CardList = ui:GetChild("CardList")
```

---

## EF/Explore_AFKRewardInfo1ByName.lua.lua
**Functions:**
- GetExplore_AFKRewardInfo1Uis
**Requires:**
- Explore_AFKRewardItemByName
**Snippet:**
```lua
require("Explore_AFKRewardItemByName")

function GetExplore_AFKRewardInfo1Uis(ui)
  local uis = {}
  uis.Item = GetExplore_AFKRewardItemUis(ui:GetChild("Item"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.AddNumberTxt = ui:GetChild("AddNumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## EF/Explore_AFKRewardInfoByName.lua.lua
**Functions:**
- GetExplore_AFKRewardInfoUis
**Snippet:**
```lua
function GetExplore_AFKRewardInfoUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.ShopBtn = ui:GetChild("ShopBtn")
  uis.root = ui
  return uis
end
```

---

## EF/Explore_AFKRewardItemByName.lua.lua
**Functions:**
- GetExplore_AFKRewardItemUis
**Snippet:**
```lua
function GetExplore_AFKRewardItemUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Explore_AFKRewardShopBtnByName.lua.lua
**Functions:**
- GetExplore_AFKRewardShopBtnUis
**Snippet:**
```lua
function GetExplore_AFKRewardShopBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Explore_AFKRewardUpRegionByName.lua.lua
**Functions:**
- GetExplore_AFKRewardUpRegionUis
**Snippet:**
```lua
function GetExplore_AFKRewardUpRegionUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SpendList = ui:GetChild("SpendList")
  uis.root = ui
  return uis
end
```

---

## EF/Explore_AFKRewardUpSpendBtnByName.lua.lua
**Functions:**
- GetExplore_AFKRewardUpSpendBtnUis
**Snippet:**
```lua
function GetExplore_AFKRewardUpSpendBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## EF/Explore_AFKStartBtnByName.lua.lua
**Functions:**
- GetExplore_AFKStartBtnUis
**Snippet:**
```lua
function GetExplore_AFKStartBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Explore_AFKStartTipsByName.lua.lua
**Functions:**
- GetExplore_AFKStartTipsUis
**Snippet:**
```lua
function GetExplore_AFKStartTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Explore_AFKTeamSwitchBtnByName.lua.lua
**Functions:**
- GetExplore_AFKTeamSwitchBtnUis
**Snippet:**
```lua
function GetExplore_AFKTeamSwitchBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NothingTxt = ui:GetChild("NothingTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## EF/Explore_AFKTimeChoiceBtnByName.lua.lua
**Functions:**
- GetExplore_AFKTimeChoiceBtnUis
**Snippet:**
```lua
function GetExplore_AFKTimeChoiceBtnUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Explore_AFKTimeChoiceRegionByName.lua.lua
**Functions:**
- GetExplore_AFKTimeChoiceRegionUis
**Snippet:**
```lua
function GetExplore_AFKTimeChoiceRegionUis(ui)
  local uis = {}
  
  uis.TimeList = ui:GetChild("TimeList")
  uis.root = ui
  return uis
end
```

---

## EF/Explore_AFKTitleByName.lua.lua
**Functions:**
- GetExplore_AFKTitleUis
**Snippet:**
```lua
function GetExplore_AFKTitleUis(ui)
  local uis = {}
  
  uis.ExpProgressBar = ui:GetChild("ExpProgressBar")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.ExpTxt = ui:GetChild("ExpTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ExpMaxTxt = ui:GetChild("ExpMaxTxt")
```

---

## EF/Explore_AFKUseWordByName.lua.lua
**Functions:**
- GetExplore_AFKUseWordUis
**Snippet:**
```lua
function GetExplore_AFKUseWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Explore_CardBreachByName.lua.lua
**Functions:**
- GetExplore_CardBreachUis
**Snippet:**
```lua
function GetExplore_CardBreachUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## EF/Explore_DispatchByName.lua.lua
**Functions:**
- GetExplore_DispatchUis
**Requires:**
- CommonResource_PopupBgByName
- Explore_DispatchTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Explore_DispatchTipsByName")

function GetExplore_DispatchUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.DispatchTips = GetExplore_DispatchTipsUis(ui:GetChild("DispatchTips"))
  uis.root = ui
  return uis
```

---

## EF/Explore_DispatchCardBgByName.lua.lua
**Functions:**
- GetExplore_DispatchCardBgUis
**Snippet:**
```lua
function GetExplore_DispatchCardBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## EF/Explore_DispatchCardByName.lua.lua
**Functions:**
- GetExplore_DispatchCardUis
**Requires:**
- Explore_DispatchCardBgByName
- Explore_CardBreachByName
**Snippet:**
```lua
require("Explore_DispatchCardBgByName")
require("Explore_CardBreachByName")

function GetExplore_DispatchCardUis(ui)
  local uis = {}
  uis.CardBg = GetExplore_DispatchCardBgUis(ui:GetChild("CardBg"))
  uis.CardBreach = GetExplore_CardBreachUis(ui:GetChild("CardBreach"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## EF/Explore_DispatchCardRegionByName.lua.lua
**Functions:**
- GetExplore_DispatchCardRegionUis
**Requires:**
- Explore_DispatchCardByName
**Snippet:**
```lua
require("Explore_DispatchCardByName")

function GetExplore_DispatchCardRegionUis(ui)
  local uis = {}
  uis.CardList = ui:GetChild("CardList")
  uis.Card = GetExplore_DispatchCardUis(ui:GetChild("Card"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## EF/Explore_DispatchClearBtnByName.lua.lua
**Functions:**
- GetExplore_DispatchClearBtnUis
**Snippet:**
```lua
function GetExplore_DispatchClearBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Explore_DispatchCloseBtnByName.lua.lua
**Functions:**
- GetExplore_DispatchCloseBtnUis
**Snippet:**
```lua
function GetExplore_DispatchCloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Explore_DispatchSureBtnByName.lua.lua
**Functions:**
- GetExplore_DispatchSureBtnUis
**Snippet:**
```lua
function GetExplore_DispatchSureBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Explore_DispatchTipsByName.lua.lua
**Functions:**
- GetExplore_DispatchTipsUis
**Snippet:**
```lua
function GetExplore_DispatchTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.CardList = ui:GetChild("CardList")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.ClearBtn = ui:GetChild("ClearBtn")
  uis.SureBtn = ui:GetChild("SureBtn")
  uis.WordTipsTxt = ui:GetChild("WordTipsTxt")
  uis.root = ui
```

---

## EF/Explore_DispatchWindowByName.lua.lua
**Functions:**
- GetExplore_DispatchWindowUis
**Requires:**
- Explore_DispatchByName
**Snippet:**
```lua
require("Explore_DispatchByName")

function GetExplore_DispatchWindowUis(ui)
  local uis = {}
  uis.Main = GetExplore_DispatchUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/Explore_ExploreAFKByName.lua.lua
**Functions:**
- GetExplore_ExploreAFKUis
**Requires:**
- CommonResource_BackGroundByName
- Explore_AFKRegoinByName
- Explore_AFKTitleByName
- Explore_AFKRewardInfoByName
- Explore_AFKStartTipsByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Explore_AFKRegoinByName")
require("Explore_AFKTitleByName")
require("Explore_AFKRewardInfoByName")
require("Explore_AFKStartTipsByName")
require("CommonResource_CurrencyReturnByName")

function GetExplore_ExploreAFKUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
```

---

## EF/Explore_ExploreAFKWindowByName.lua.lua
**Functions:**
- GetExplore_ExploreAFKWindowUis
**Requires:**
- Explore_ExploreAFKByName
**Snippet:**
```lua
require("Explore_ExploreAFKByName")

function GetExplore_ExploreAFKWindowUis(ui)
  local uis = {}
  uis.Main = GetExplore_ExploreAFKUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/Explore_ExploreByName.lua.lua
**Functions:**
- GetExplore_ExploreUis
**Requires:**
- CommonResource_BackGroundByName
- Explore_ExploreWordByName
- Explore_ExploreTouchWordByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Explore_ExploreWordByName")
require("Explore_ExploreTouchWordByName")
require("CommonResource_CurrencyReturnByName")

function GetExplore_ExploreUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Word = GetExplore_ExploreWordUis(ui:GetChild("Word"))
  uis.TouchWord = GetExplore_ExploreTouchWordUis(ui:GetChild("TouchWord"))
```

---

## EF/Explore_ExploreTouchWordByName.lua.lua
**Functions:**
- GetExplore_ExploreTouchWordUis
**Snippet:**
```lua
function GetExplore_ExploreTouchWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Explore_ExploreWindowByName.lua.lua
**Functions:**
- GetExplore_ExploreWindowUis
**Requires:**
- Explore_ExploreByName
**Snippet:**
```lua
require("Explore_ExploreByName")

function GetExplore_ExploreWindowUis(ui)
  local uis = {}
  uis.Main = GetExplore_ExploreUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/Explore_ExploreWordByName.lua.lua
**Functions:**
- GetExplore_ExploreWordUis
**Snippet:**
```lua
function GetExplore_ExploreWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Explore_SettlementByName.lua.lua
**Functions:**
- GetExplore_SettlementUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetExplore_SettlementUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.EndList = ui:GetChild("EndList")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.root = ui
  return uis
```

---

## EF/Explore_SettlementCardByName.lua.lua
**Functions:**
- GetExplore_SettlementCardUis
**Snippet:**
```lua
function GetExplore_SettlementCardUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.CardList = ui:GetChild("CardList")
  uis.root = ui
  return uis
end
```

---

## EF/Explore_SettlementCardHeadBgByName.lua.lua
**Functions:**
- GetExplore_SettlementCardHeadBgUis
**Snippet:**
```lua
function GetExplore_SettlementCardHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## EF/Explore_SettlementCardHeadByName.lua.lua
**Functions:**
- GetExplore_SettlementCardHeadUis
**Requires:**
- Explore_SettlementCardHeadBgByName
**Snippet:**
```lua
require("Explore_SettlementCardHeadBgByName")

function GetExplore_SettlementCardHeadUis(ui)
  local uis = {}
  uis.HeadBg = GetExplore_SettlementCardHeadBgUis(ui:GetChild("HeadBg"))
  uis.root = ui
  return uis
end
```

---

## EF/Explore_SettlementExpByName.lua.lua
**Functions:**
- GetExplore_SettlementExpUis
**Snippet:**
```lua
function GetExplore_SettlementExpUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ExpProgressBar = ui:GetChild("ExpProgressBar")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.ExpTxt = ui:GetChild("ExpTxt")
  uis.ExpMaxTxt = ui:GetChild("ExpMaxTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## EF/Explore_SettlementRewardByName.lua.lua
**Functions:**
- GetExplore_SettlementRewardUis
**Snippet:**
```lua
function GetExplore_SettlementRewardUis(ui)
  local uis = {}
  
  uis.ItemList = ui:GetChild("ItemList")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Explore_SettlementTimeByName.lua.lua
**Functions:**
- GetExplore_SettlementTimeUis
**Snippet:**
```lua
function GetExplore_SettlementTimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Explore_SettlementWindowByName.lua.lua
**Functions:**
- GetExplore_SettlementWindowUis
**Requires:**
- Explore_SettlementByName
**Snippet:**
```lua
require("Explore_SettlementByName")

function GetExplore_SettlementWindowUis(ui)
  local uis = {}
  uis.Main = GetExplore_SettlementUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/FloatTipsUtil.lua.lua
**Functions:**
- FloatTipsUtil.ClearQueue
- FloatTipsUtil.AddPopupItem
- FloatTipsUtil.TimerCallback
- FloatTipsUtil.GetFloatTips
- FloatTipsUtil.AddAndPlayTips
- FloatTipsUtil.ShowPopupItemTips
- FloatTipsUtil.ShowWarnTips
- FloatTipsUtil.TestBasic
**Snippet:**
```lua
local FloatTipsUtil = {}
local floatTipsQueue = {}
local floatTipsUrl, popupLayer, floatTipsPlayTimer
local messageTipsPool = FairyGUI.GObjectPool(CS.Launch.Singleton.transform)

function FloatTipsUtil.ClearQueue()
  floatTipsQueue = {}
end

function FloatTipsUtil.AddPopupItem(itemId, itemCount)
```

---

## EF/FormationBuffTipsWindow.lua.lua
**Functions:**
- FormationBuffTipsWindow.ReInitData
- FormationBuffTipsWindow.OnInit
- FormationBuffTipsWindow.UpdateInfo
- moduleList.itemRenderer
- FormationBuffTipsWindow.InitBtn
- FormationBuffTipsWindow.Close
- FormationBuffTipsWindow.OnClose
**Requires:**
- Formation_BuffTipsWindowByName
**Snippet:**
```lua
require("Formation_BuffTipsWindowByName")
local FormationBuffTipsWindow = {}
local uis, contentPane

function FormationBuffTipsWindow.ReInitData()
end

local preBuffIds

function FormationBuffTipsWindow.OnInit(bridgeObj)
```

---

## EF/FormationBuildTipsWindow.lua.lua
**Functions:**
- FormationBuildTipsWindow.ReInitData
- FormationBuildTipsWindow.OnInit
- FormationBuildTipsWindow.UpdateInfo
- FormationBuildTipsWindow.InitBtn
- FormationBuildTipsWindow.Close
- FormationBuildTipsWindow.OnClose
**Requires:**
- Formation_BuildTipsWindowByName
**Snippet:**
```lua
require("Formation_BuildTipsWindowByName")
local FormationBuildTipsWindow = {}
local uis, contentPane

function FormationBuildTipsWindow.ReInitData()
end

local buildingId, closeCallback, params

function FormationBuildTipsWindow.OnInit(bridgeObj)
```

---

## EF/FormationCardTipsWindow.lua.lua
**Functions:**
- FormationCardTipsWindow.ReInitData
- FormationCardTipsWindow.OnInit
- FormationCardTipsWindow.UpdateInfo
- skillList.itemRenderer
- FormationCardTipsWindow.InitRogueBadgeList
- uis.Main.BadgeList.itemRenderer
- list.itemRenderer
- suitList.itemRenderer
- suitDesList.itemRenderer
- FormationCardTipsWindow.ShowSkillDetail
- FormationCardTipsWindow.GetBadgeInfoByUid
- FormationCardTipsWindow.InitBadgeList
- uis.Main.BadgeList.itemRenderer
- list.itemRenderer
- suitList.itemRenderer
- suitDesList.itemRenderer
- FormationCardTipsWindow.ShowAttribute
- AttributeList.itemRenderer
- FormationCardTipsWindow.InitBtn
- FormationCardTipsWindow.Close
- FormationCardTipsWindow.OnShown
- FormationCardTipsWindow.OnClose
- FormationCardTipsWindow.HandleMessage
**Requires:**
- Formation_CardTipsWindowByName
**Snippet:**
```lua
require("Formation_CardTipsWindowByName")
local FormationCardTipsWindow = {}
local uis, contentPane

function FormationCardTipsWindow.ReInitData()
end

local cardInfo, closeCallback, params, page, sceneType, curShowSkillId, allBadges

function FormationCardTipsWindow.OnInit(bridgeObj)
```

---

## EF/FormationData.lua.lua
**Functions:**
- FormationData.Init
- FormationData.GetQualifiedCard
- FormationData.GetEmbattledLimitCardNum
- FormationData.GetEmbattledLimitBuildingNum
- FormationData.GetArenaMap
- FormationData.GetOwnBuilding
- FormationData.GetBuildingByUid
- FormationData.SaveBattleTeamState
- FormationData.IsLimitCardType
- FormationData.SaveStagePrepareInfo
- FormationData.GetStagePrepareInfo
- FormationData.GetChildIndexByGridIndex
- FormationData.GetOppositeIndex
- FormationData.GetBadgeList
- FormationData.UpdateEnemyCache
- FormationData.ClearEnemyCache
- FormationData.GetCardDataByUid
- FormationData.GetLeaderSkillInfo
- FormationData.GetRogueEffectFormation
- FormationData.ClearCacheData
**Snippet:**
```lua
FormationData = {
  bottomGridWidth = 80,
  bottomGridUIWidth = 80,
  rotation = -60,
  bottomGridScale = 1,
  cachedArenaMapList = nil,
  cachedStagePrepareInfo = nil,
  cachedTeamStateLeft = nil,
  cachedTeamStateRight = nil,
  cachedEnemyList = {}
```

---

## EF/FormationDragDrop.lua.lua

---

## EF/FormationExpeditionBuffTipsWindow.lua.lua
**Functions:**
- FormationExpeditionBuffTipsWindow.ReInitData
- FormationExpeditionBuffTipsWindow.OnInit
- FormationExpeditionBuffTipsWindow.UpdateInfo
- FormationExpeditionBuffTipsWindow.InitBtn
- FormationExpeditionBuffTipsWindow.OnClose
**Requires:**
- Formation_ExpeditionBuffTipsWindowByName
**Snippet:**
```lua
require("Formation_ExpeditionBuffTipsWindowByName")
local FormationExpeditionBuffTipsWindow = {}
local uis, contentPane

function FormationExpeditionBuffTipsWindow.ReInitData()
end

function FormationExpeditionBuffTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.FormationExpeditionBuffTipsWindow.package, WinResConfig.FormationExpeditionBuffTipsWindow.comName, function(com)
    contentPane = com
```

---

## EF/FormationMgr.lua.lua
**Functions:**
- FormationMgr.ReopenFormationWindow
- FormationMgr.ClearCache
- FormationMgr.TryOpenFormationWindow
- FormationMgr.OpenFormationWindow
- FormationMgr.SendBattleReq
- FormationMgr.ShowMapChoiceInfo
- list.itemRenderer
- FormationMgr.ShowTargetLine
- FormationMgr.GetPrepareSceneType
**Snippet:**
```lua
FormationMgr = {
  cacheFormationParams = nil,
  cachedLastFormationParams = nil,
  cachedLastFormationOpenWindowAfterRsp = nil
}

function FormationMgr.ReopenFormationWindow()
  FormationMgr.TryOpenFormationWindow(FormationMgr.cachedLastFormationParams, FormationMgr.cachedLastFormationOpenWindowAfterRsp)
end

```

---

## EF/FormationMonsterTipsWindow.lua.lua
**Functions:**
- FormationMonsterTipsWindow.ReInitData
- FormationMonsterTipsWindow.OnInit
- FormationMonsterTipsWindow.UpdateInfo
- FormationMonsterTipsWindow.InitBtn
- FormationMonsterTipsWindow.Close
- FormationMonsterTipsWindow.OnClose
**Requires:**
- Formation_MonsterTipsWindowByName
- Formation_MonsterInfoByName
**Snippet:**
```lua
require("Formation_MonsterTipsWindowByName")
local FormationMonsterTipsWindow = {}
local uis, contentPane

function FormationMonsterTipsWindow.ReInitData()
end

local monsterConfig, closeCallback, params

function FormationMonsterTipsWindow.OnInit(bridgeObj)
```

---

## EF/FormationRestraintTipsWindow.lua.lua
**Functions:**
- FormationRestraintTipsWindow.ReInitData
- FormationRestraintTipsWindow.OnInit
- FormationRestraintTipsWindow.UpdateInfo
- FormationRestraintTipsWindow.InitBtn
- FormationRestraintTipsWindow.Close
- FormationRestraintTipsWindow.OnClose
**Requires:**
- Formation_RestraintTipsWindowByName
**Snippet:**
```lua
require("Formation_RestraintTipsWindowByName")
local FormationRestraintTipsWindow = {}
local uis, contentPane

function FormationRestraintTipsWindow.ReInitData()
end

function FormationRestraintTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.FormationRestraintTipsWindow.package, WinResConfig.FormationRestraintTipsWindow.comName, function(com)
    contentPane = com
```

---

## EF/FormationScriptList.lua.lua
**Requires:**
- FormationUnit
- FormationData
- FormationMgr
- FormationService
**Snippet:**
```lua
local require = require
require("FormationUnit")
require("FormationData")
require("FormationMgr")
require("FormationService")
```

---

## EF/FormationService.lua.lua
**Functions:**
- FormationService.Init
- FormationService.GetStagePrepareInfoReq
- FormationService.DealGetStagePrepareInfoRsp
- FormationService.GetOtherCardInfoReq
- FormationService.DealGetOtherCardInfoRsp
- FormationService.ExitStagePrepareReq
- FormationService.ExitStagePrepareRsp
**Snippet:**
```lua
FormationService = {}

function FormationService.Init()
  Net.AddListener(Proto.MsgName.GetStagePrepareInfoRsp, FormationService.DealGetStagePrepareInfoRsp)
  Net.AddListener(Proto.MsgName.GetOtherCardInfoRsp, FormationService.DealGetOtherCardInfoRsp)
  Net.AddListener(Proto.MsgName.ExitStagePrepareRsp, FormationService.ExitStagePrepareRsp)
end

function FormationService.GetStagePrepareInfoReq(sceneType, stageId, callback, params)
  local msg = {}
```

---

## EF/FormationUnit.lua.lua
**Functions:**
- FormationUnit.New
- FormationUnit.GetCurTarget
- FormationUnit.IsTargetCounter
**Snippet:**
```lua
FormationUnit = {}

function FormationUnit.New(position, range, cardType, buildingType)
  local card = {}
  card.position = position
  card.range = range
  card.cardType = cardType
  card.buildingType = buildingType
  return card
end
```

---

## EF/FormationWindow.lua.lua
**Functions:**
- FormationWindow.Init
- FormationWindow.InitLocalData
- FormationWindow.Destroy
- FormationWindow.OnInit
- FormationWindow.InitRedDot
- FormationWindow.InitExpeditionCardList
- FormationWindow.UpdateDefenseFormationLeaderCard
- FormationWindow.UpdateDefenseFormationBurstOrderSetting
- FormationWindow.UpdateDefenseFormationCard
- FormationWindow.UpdateDefenseFormationBuilding
- FormationWindow.UpdateDefenseFormationMap
- FormationWindow.InitText
- FormationWindow.InitScreenTips
- FormationWindow.UpdateInfo
- FormationWindow.UpdateTips
- FormationWindow.UpdateCardQuickOperation
- FormationWindow.UpdateGuildWarSkill
- skillList.itemRenderer
- FormationWindow.GetDefaultTeamId
- FormationWindow.UpdateGuildWarSkillChoose
- teamList.itemRenderer
- FormationWindow.UpdateGuildWarSkillRegion
- list.itemRenderer
- FormationWindow.UpdateAllSkill
- choiceList.itemRenderer
- FormationWindow.UpdateSkillInfo
- numberList.itemRenderer
- elementList.itemRenderer
- tacticSkill.WordList.itemRenderer
- effectList.itemRenderer
- FormationWindow.GetAllSkillEffect
- FormationWindow.GetCardListByType
- FormationWindow.IsCardEnableInGuildWar
- FormationWindow.GetCardEnableList
- FormationWindow.GetEmbattledCardCount
- FormationWindow.GetEmbattledCardMaxCount
- FormationWindow.GetEmbattledCardCountByType
- FormationWindow.GetEmbattledCardCountSplitByType
- FormationWindow.IsAssistCard
- FormationWindow.GetEmbattledAssistCount
- FormationWindow.GetEmbattledAssistMaxCount
- FormationWindow.GetEmbattledBuildingCost
- FormationWindow.GetBuildingCostMax
- FormationWindow.UpdateExpeditionInfo
- FormationWindow.UpdateExpeditionOtherTeamInfo
- FormationWindow.UpdateMap
- FormationWindow.UpdateMapEffect
- FormationWindow.UpdateMapInfo
- FormationWindow.UpdateMapBuffList
- FormationWindow.UpdateBurst
- FormationWindow.GetEmbattleCardById
- FormationWindow.ShowChoiceOprTips
- FormationWindow.ShowMapChoice
- FormationWindow.RenderOneMap
- FormationWindow.UpdateCurMapDetail
- FormationWindow.UpdateBottomList
- FormationWindow.IsCardSelect
- FormationWindow.IsBuildingSelect
- FormationWindow.IsBuildingBeyondCost
- FormationWindow.IsCardDead
- FormationWindow.IsMapSelect
- FormationWindow.RefreshItem
- FormationWindow.EmbattleSameCard
- FormationWindow.TouchItem
- FormationWindow.UpdateListWhenDrag
- FormationWindow.UpdateCardList
- filterFunc
- filterFunc
- filterFunc
- filterFunc
- filterFunc
- filterFunc
- filterFunc
- filterFunc
- filterFunc
- filterFunc
- filterFunc
- filterFunc
- filterFunc
- FormationWindow.SortCardListForGuildWar
- FormationWindow.UpdateBuildingList
- FormationWindow.ClearOneMapNew
- FormationWindow.ClearMapNew
- FormationWindow.ClearOneBuildingNew
- FormationWindow.ClearBuildingNew
- FormationWindow.IsRecommendCard
- FormationWindow.GetBattleState
- FormationWindow.UpdateLabel
- FormationWindow.CreateOneLabel
- FormationWindow.MapTabVisible
- FormationWindow.BuildingTabVisible
- FormationWindow.LimitCardType
- FormationWindow.LimitUsedCard
- FormationWindow.IsRogueGame
- FormationWindow.LimitDeadCard
- FormationWindow.HaveRecommendCard
- FormationWindow.HaveGuildAssist
- FormationWindow.IsSealDungeon
- FormationWindow.InitBtn
- FormationWindow.AutoChooseOneCard
- FormationWindow.TouchCardUp
- FormationWindow.TouchCardDown
- FormationWindow.ChangeTeamIndex
- FormationWindow.OnShowAnimationEnd
- FormationWindow.OnPreClose
- FormationWindow.ClickBattle
- FormationWindow.OnShown
- FormationWindow.OnHide
- FormationWindow.StopTalk
- FormationWindow.OnClose
- FormationWindow.HandleMessage
- FormationWindow.InitSwipeGesture
- FormationWindow.UpdateTargetHolderVisible
- FormationWindow.ShowDragCardRecord
- FormationWindow.ClearDragCardRecord
- FormationWindow.ShowDragBuildingRecord
- FormationWindow.ClearDragBuildingRecord
- FormationWindow.OnDragStart
- FormationWindow.OnDragMove
- FormationWindow.GetGridInfo
- FormationWindow.ShowTouchState
- FormationWindow.GetCoverGridShowList
- FormationWindow.GetPlaceGridStateSimple
- FormationWindow.GetPlaceGridState
- FormationWindow.OnDragEnd
- FormationWindow.DragOutFormation
- FormationWindow.SetRangeRectVisible
- FormationWindow.GetAllEnableGrid
- FormationWindow.ClearByUid
- FormationWindow.GetSwipeGesture
- FormationWindow.SetSwipeGestureEnable
- FormationWindow.SetDragGridMapVisible
- FormationWindow.ClearDrag
- FormationWindow.SetTouchableWhenDrag
- FormationWindow.ShowCardOrBuildingInMap
- FormationWindow.ShowUnavailableCardInMap
- FormationWindow.GetAvailablePos
- FormationWindow.UpdateUnavailableCards
- FormationWindow.ShowLeft
- FormationWindow.ShowOther
- FormationWindow.ShowGuildBossHp
- FormationWindow.ShowEnemyFormation
- FormationWindow.UpdateSort
- FormationWindow.UpdateSpecialEffect
- FormationWindow.GetCardById
- FormationWindow.InitMap
- FormationWindow.GetInitPosition
- FormationWindow.CheckGuideComplete
- FormationWindow.GetGuideTargetDragPos
- FormationWindow.UpdateGuideDraggable
- FormationWindow.CreateGuideLine
- FormationWindow.ShowMoveEffect
- FormationWindow.DragTargetGridEffect
- FormationWindow.ShowDragGuide
- FormationWindow.HideDragGuide
- FormationWindow.RefreshGuide
**Requires:**
- Formation_FormationWindowByName
**Snippet:**
```lua
require("Formation_FormationWindowByName")
local FormationWindow = {}
local LABEL_TYPE_ENUM = {
  CARD = 1,
  BUILDING = 2,
  USED_CARD = 3,
  UNUSED_CARD = 4,
  CAN_USE = 5,
  FORBIDDEN = 6,
  AVAILABLE_UNUSED = 7,
```

---

## EF/Formation_20BtnByName.lua.lua
**Functions:**
- GetFormation_20BtnUis
**Requires:**
- Formation_BgAniByName
**Snippet:**
```lua
require("Formation_BgAniByName")

function GetFormation_20BtnUis(ui)
  local uis = {}
  uis.BgAni = GetFormation_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_45BtnByName.lua.lua
**Functions:**
- GetFormation_45BtnUis
**Requires:**
- Formation_BgAniByName
**Snippet:**
```lua
require("Formation_BgAniByName")

function GetFormation_45BtnUis(ui)
  local uis = {}
  uis.BgAni = GetFormation_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_70BtnByName.lua.lua
**Functions:**
- GetFormation_70BtnUis
**Requires:**
- Formation_BgAniByName
**Snippet:**
```lua
require("Formation_BgAniByName")

function GetFormation_70BtnUis(ui)
  local uis = {}
  uis.BgAni = GetFormation_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_AnBtnByName.lua.lua
**Functions:**
- GetFormation_AnBtnUis
**Requires:**
- Formation_BgAniByName
**Snippet:**
```lua
require("Formation_BgAniByName")

function GetFormation_AnBtnUis(ui)
  local uis = {}
  uis.BgAni = GetFormation_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BattleBtnByName.lua.lua
**Functions:**
- GetFormation_BattleBtnUis
**Snippet:**
```lua
function GetFormation_BattleBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BattleLatticeByName.lua.lua
**Functions:**
- GetFormation_BattleLatticeUis
**Snippet:**
```lua
function GetFormation_BattleLatticeUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BattlePlayerNumberByName.lua.lua
**Functions:**
- GetFormation_BattlePlayerNumberUis
**Requires:**
- CommonResource_PopupBgByName
- Formation_BattlePlayerNumberRegionByName
- Formation_BattlePlayerNumberWordByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Formation_BattlePlayerNumberRegionByName")
require("Formation_BattlePlayerNumberWordByName")

function GetFormation_BattlePlayerNumberUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.Region = GetFormation_BattlePlayerNumberRegionUis(ui:GetChild("Region"))
  uis.Word = GetFormation_BattlePlayerNumberWordUis(ui:GetChild("Word"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
```

---

## EF/Formation_BattlePlayerNumberRegion1ByName.lua.lua
**Functions:**
- GetFormation_BattlePlayerNumberRegion1Uis
**Snippet:**
```lua
function GetFormation_BattlePlayerNumberRegion1Uis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BattlePlayerNumberRegionByName.lua.lua
**Functions:**
- GetFormation_BattlePlayerNumberRegionUis
**Requires:**
- Formation_BattlePlayerNumberRegion1ByName
**Snippet:**
```lua
require("Formation_BattlePlayerNumberRegion1ByName")

function GetFormation_BattlePlayerNumberRegionUis(ui)
  local uis = {}
  uis.Before = GetFormation_BattlePlayerNumberRegion1Uis(ui:GetChild("Before"))
  uis.After = GetFormation_BattlePlayerNumberRegion1Uis(ui:GetChild("After"))
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BattlePlayerNumberWindowByName.lua.lua
**Functions:**
- GetFormation_BattlePlayerNumberWindowUis
**Requires:**
- Formation_BattlePlayerNumberByName
**Snippet:**
```lua
require("Formation_BattlePlayerNumberByName")

function GetFormation_BattlePlayerNumberWindowUis(ui)
  local uis = {}
  uis.Main = GetFormation_BattlePlayerNumberUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BattlePlayerNumberWordByName.lua.lua
**Functions:**
- GetFormation_BattlePlayerNumberWordUis
**Requires:**
- Formation_BattlePlayerNumberWordEffectByName
**Snippet:**
```lua
require("Formation_BattlePlayerNumberWordEffectByName")

function GetFormation_BattlePlayerNumberWordUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Effect = GetFormation_BattlePlayerNumberWordEffectUis(ui:GetChild("Effect"))
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BattlePlayerNumberWordEffectByName.lua.lua
**Functions:**
- GetFormation_BattlePlayerNumberWordEffectUis
**Snippet:**
```lua
function GetFormation_BattlePlayerNumberWordEffectUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BgAniByName.lua.lua
**Functions:**
- GetFormation_BgAniUis
**Snippet:**
```lua
function GetFormation_BgAniUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BianDuiBtnByName.lua.lua
**Functions:**
- GetFormation_BianDuiBtnUis
**Requires:**
- Formation_BgAniByName
**Snippet:**
```lua
require("Formation_BgAniByName")

function GetFormation_BianDuiBtnUis(ui)
  local uis = {}
  uis.BgAni = GetFormation_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## EF/Formation_BuffTipsByName.lua.lua
**Functions:**
- GetFormation_BuffTipsUis
**Requires:**
- CommonResource_PopupBgByName
- Formation_BuffTipsRegionByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Formation_BuffTipsRegionByName")

function GetFormation_BuffTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.BuffTipsRegion = GetFormation_BuffTipsRegionUis(ui:GetChild("BuffTipsRegion"))
  uis.root = ui
  return uis
```

---

## EF/Formation_BuffTipsDescribeByName.lua.lua
**Functions:**
- GetFormation_BuffTipsDescribeUis
**Snippet:**
```lua
function GetFormation_BuffTipsDescribeUis(ui)
  local uis = {}
  
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BuffTipsMainBtnByName.lua.lua
**Functions:**
- GetFormation_BuffTipsMainBtnUis
**Snippet:**
```lua
function GetFormation_BuffTipsMainBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BuffTipsRegionByName.lua.lua
**Functions:**
- GetFormation_BuffTipsRegionUis
**Snippet:**
```lua
function GetFormation_BuffTipsRegionUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.ModuleList = ui:GetChild("ModuleList")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BuffTipsWindowByName.lua.lua
**Functions:**
- GetFormation_BuffTipsWindowUis
**Requires:**
- Formation_BuffTipsByName
**Snippet:**
```lua
require("Formation_BuffTipsByName")

function GetFormation_BuffTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetFormation_BuffTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BuildAttributeByName.lua.lua
**Functions:**
- GetFormation_BuildAttributeUis
**Snippet:**
```lua
function GetFormation_BuildAttributeUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BuildCostLeftByName.lua.lua
**Functions:**
- GetFormation_BuildCostLeftUis
**Snippet:**
```lua
function GetFormation_BuildCostLeftUis(ui)
  local uis = {}
  
  uis.BuildTxt = ui:GetChild("BuildTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BuildCostRightByName.lua.lua
**Functions:**
- GetFormation_BuildCostRightUis
**Snippet:**
```lua
function GetFormation_BuildCostRightUis(ui)
  local uis = {}
  
  uis.BuildTxt = ui:GetChild("BuildTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BuildLockByName.lua.lua
**Functions:**
- GetFormation_BuildLockUis
**Snippet:**
```lua
function GetFormation_BuildLockUis(ui)
  local uis = {}
  
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BuildTipsByName.lua.lua
**Functions:**
- GetFormation_BuildTipsUis
**Requires:**
- CommonResource_PopupBgByName
- Formation_BuildLockByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Formation_BuildLockByName")

function GetFormation_BuildTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.ElementList = ui:GetChild("ElementList")
```

---

## EF/Formation_BuildTipsWindowByName.lua.lua
**Functions:**
- GetFormation_BuildTipsWindowUis
**Requires:**
- Formation_BuildTipsByName
**Snippet:**
```lua
require("Formation_BuildTipsByName")

function GetFormation_BuildTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetFormation_BuildTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BuildWordByName.lua.lua
**Functions:**
- GetFormation_BuildWordUis
**Snippet:**
```lua
function GetFormation_BuildWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BurstContentByName.lua.lua
**Functions:**
- GetFormation_BurstContentUis
**Snippet:**
```lua
function GetFormation_BurstContentUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BurstLeaderBgByName.lua.lua
**Functions:**
- GetFormation_BurstLeaderBgUis
**Snippet:**
```lua
function GetFormation_BurstLeaderBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BurstLeaderBtnByName.lua.lua
**Functions:**
- GetFormation_BurstLeaderBtnUis
**Requires:**
- Formation_BurstLeaderBgByName
**Snippet:**
```lua
require("Formation_BurstLeaderBgByName")

function GetFormation_BurstLeaderBtnUis(ui)
  local uis = {}
  uis.BurstLeaderBg = GetFormation_BurstLeaderBgUis(ui:GetChild("BurstLeaderBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## EF/Formation_BurstLeaderContentByName.lua.lua
**Functions:**
- GetFormation_BurstLeaderContentUis
**Snippet:**
```lua
function GetFormation_BurstLeaderContentUis(ui)
  local uis = {}
  
  uis.WordList = ui:GetChild("WordList")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BurstLeaderSkillRegionByName.lua.lua
**Functions:**
- GetFormation_BurstLeaderSkillRegionUis
**Requires:**
- Formation_LeaderHeadByName
**Snippet:**
```lua
require("Formation_LeaderHeadByName")

function GetFormation_BurstLeaderSkillRegionUis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.LeaderHead = GetFormation_LeaderHeadUis(ui:GetChild("LeaderHead"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.HeadList = ui:GetChild("HeadList")
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## EF/Formation_BurstLeaderSkillWordByName.lua.lua
**Functions:**
- GetFormation_BurstLeaderSkillWordUis
**Snippet:**
```lua
function GetFormation_BurstLeaderSkillWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BurstLeaderWordByName.lua.lua
**Functions:**
- GetFormation_BurstLeaderWordUis
**Snippet:**
```lua
function GetFormation_BurstLeaderWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BurstOccupationByName.lua.lua
**Functions:**
- GetFormation_BurstOccupationUis
**Snippet:**
```lua
function GetFormation_BurstOccupationUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BurstStripByName.lua.lua
**Functions:**
- GetFormation_BurstStripUis
**Requires:**
- Formation_LeaderHeadByName
- Formation_BurstStripTipsByName
**Snippet:**
```lua
require("Formation_LeaderHeadByName")
require("Formation_BurstStripTipsByName")

function GetFormation_BurstStripUis(ui)
  local uis = {}
  uis.LeaderHead = GetFormation_LeaderHeadUis(ui:GetChild("LeaderHead"))
  uis.OccupationList = ui:GetChild("OccupationList")
  uis.BurstStripTips = GetFormation_BurstStripTipsUis(ui:GetChild("BurstStripTips"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
```

---

## EF/Formation_BurstStripTipsByName.lua.lua
**Functions:**
- GetFormation_BurstStripTipsUis
**Snippet:**
```lua
function GetFormation_BurstStripTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BurstTab1BtnByName.lua.lua
**Functions:**
- GetFormation_BurstTab1BtnUis
**Snippet:**
```lua
function GetFormation_BurstTab1BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BurstTab2BtnByName.lua.lua
**Functions:**
- GetFormation_BurstTab2BtnUis
**Snippet:**
```lua
function GetFormation_BurstTab2BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BurstTab3BtnByName.lua.lua
**Functions:**
- GetFormation_BurstTab3BtnUis
**Snippet:**
```lua
function GetFormation_BurstTab3BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BurstTips1ByName.lua.lua
**Functions:**
- GetFormation_BurstTips1Uis
**Snippet:**
```lua
function GetFormation_BurstTips1Uis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.ContentList = ui:GetChild("ContentList")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BurstTips2ByName.lua.lua
**Functions:**
- GetFormation_BurstTips2Uis
**Snippet:**
```lua
function GetFormation_BurstTips2Uis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.ContentList = ui:GetChild("ContentList")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BurstTips3ByName.lua.lua
**Functions:**
- GetFormation_BurstTips3Uis
**Requires:**
- Formation_SetRoundRegionByName
**Snippet:**
```lua
require("Formation_SetRoundRegionByName")

function GetFormation_BurstTips3Uis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.HeadList = ui:GetChild("HeadList")
  uis.SetRoundRegion = GetFormation_SetRoundRegionUis(ui:GetChild("SetRoundRegion"))
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BurstTipsByName.lua.lua
**Functions:**
- GetFormation_BurstTipsUis
**Requires:**
- CommonResource_PopupBgByName
- Formation_BurstTipsRegionByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Formation_BurstTipsRegionByName")

function GetFormation_BurstTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.BurstTips = GetFormation_BurstTipsRegionUis(ui:GetChild("BurstTips"))
  uis.root = ui
  return uis
```

---

## EF/Formation_BurstTipsRegionByName.lua.lua
**Functions:**
- GetFormation_BurstTipsRegionUis
**Requires:**
- Formation_BurstTips1ByName
- Formation_BurstTips2ByName
- Formation_BurstTips3ByName
**Snippet:**
```lua
require("Formation_BurstTips1ByName")
require("Formation_BurstTips2ByName")
require("Formation_BurstTips3ByName")

function GetFormation_BurstTipsRegionUis(ui)
  local uis = {}
  uis.BurstTab1Btn = ui:GetChild("BurstTab1Btn")
  uis.BurstTab2Btn = ui:GetChild("BurstTab2Btn")
  uis.BurstTab3Btn = ui:GetChild("BurstTab3Btn")
  uis.BurstTips1 = GetFormation_BurstTips1Uis(ui:GetChild("BurstTips1"))
```

---

## EF/Formation_BurstTipsWindowByName.lua.lua
**Functions:**
- GetFormation_BurstTipsWindowUis
**Requires:**
- Formation_BurstTipsByName
**Snippet:**
```lua
require("Formation_BurstTipsByName")

function GetFormation_BurstTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetFormation_BurstTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/Formation_BurstWordByName.lua.lua
**Functions:**
- GetFormation_BurstWordUis
**Snippet:**
```lua
function GetFormation_BurstWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_CardAttributeBadgeBtnByName.lua.lua
**Functions:**
- GetFormation_CardAttributeBadgeBtnUis
**Snippet:**
```lua
function GetFormation_CardAttributeBadgeBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_CardAttributeByName.lua.lua
**Functions:**
- GetFormation_CardAttributeUis
**Snippet:**
```lua
function GetFormation_CardAttributeUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_CardAttributeModuleByName.lua.lua
**Functions:**
- GetFormation_CardAttributeModuleUis
**Snippet:**
```lua
function GetFormation_CardAttributeModuleUis(ui)
  local uis = {}
  
  uis.ContentList = ui:GetChild("ContentList")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_CardBadgeAttributeByName.lua.lua
**Functions:**
- GetFormation_CardBadgeAttributeUis
**Requires:**
- Formation_CardBadgeAttributeInfo1ByName
**Snippet:**
```lua
require("Formation_CardBadgeAttributeInfo1ByName")

function GetFormation_CardBadgeAttributeUis(ui)
  local uis = {}
  uis.AttributeInfo = GetFormation_CardBadgeAttributeInfo1Uis(ui:GetChild("AttributeInfo"))
  uis.AttributeList = ui:GetChild("AttributeList")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_CardBadgeAttributeInfo1ByName.lua.lua
**Functions:**
- GetFormation_CardBadgeAttributeInfo1Uis
**Snippet:**
```lua
function GetFormation_CardBadgeAttributeInfo1Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_CardBadgeAttributeInfo2ByName.lua.lua
**Functions:**
- GetFormation_CardBadgeAttributeInfo2Uis
**Snippet:**
```lua
function GetFormation_CardBadgeAttributeInfo2Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_CardBadgeByName.lua.lua
**Functions:**
- GetFormation_CardBadgeUis
**Requires:**
- Formation_CardBadgeIconByName
- Formation_CardBadgeAttributeByName
**Snippet:**
```lua
require("Formation_CardBadgeIconByName")
require("Formation_CardBadgeAttributeByName")

function GetFormation_CardBadgeUis(ui)
  local uis = {}
  uis.BadgeIcon = GetFormation_CardBadgeIconUis(ui:GetChild("BadgeIcon"))
  uis.adgeAttribute = GetFormation_CardBadgeAttributeUis(ui:GetChild("adgeAttribute"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## EF/Formation_CardBadgeIconByName.lua.lua
**Functions:**
- GetFormation_CardBadgeIconUis
**Snippet:**
```lua
function GetFormation_CardBadgeIconUis(ui)
  local uis = {}
  
  uis.IconLoader = ui:GetChild("IconLoader")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_CardBadgeIconStarByName.lua.lua
**Functions:**
- GetFormation_CardBadgeIconStarUis
**Snippet:**
```lua
function GetFormation_CardBadgeIconStarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## EF/Formation_CardBadgeRegionByName.lua.lua
**Functions:**
- GetFormation_CardBadgeRegionUis
**Requires:**
- Formation_CardBageSuitByName
**Snippet:**
```lua
require("Formation_CardBageSuitByName")

function GetFormation_CardBadgeRegionUis(ui)
  local uis = {}
  uis.BadgeList = ui:GetChild("BadgeList")
  uis.Suit = GetFormation_CardBageSuitUis(ui:GetChild("Suit"))
  uis.root = ui
  return uis
end
```

---

## EF/Formation_CardBageSuit1ByName.lua.lua
**Functions:**
- GetFormation_CardBageSuit1Uis
**Snippet:**
```lua
function GetFormation_CardBageSuit1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_CardBageSuit2ByName.lua.lua
**Functions:**
- GetFormation_CardBageSuit2Uis
**Snippet:**
```lua
function GetFormation_CardBageSuit2Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SuitList = ui:GetChild("SuitList")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_CardBageSuitByName.lua.lua
**Functions:**
- GetFormation_CardBageSuitUis
**Snippet:**
```lua
function GetFormation_CardBageSuitUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.AllSuitList = ui:GetChild("AllSuitList")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_CardDownBtnByName.lua.lua
**Functions:**
- GetFormation_CardDownBtnUis
**Snippet:**
```lua
function GetFormation_CardDownBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_CardInfoByName.lua.lua
**Functions:**
- GetFormation_CardInfoUis
**Requires:**
- CommonResource_OccupationByName
- CommonResource_CardBreachByName
- Formation_CardAttributeModuleByName
**Snippet:**
```lua
require("CommonResource_OccupationByName")
require("CommonResource_CardBreachByName")
require("Formation_CardAttributeModuleByName")

function GetFormation_CardInfoUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.StarList = ui:GetChild("StarList")
  uis.Occupation = GetCommonResource_OccupationUis(ui:GetChild("Occupation"))
  uis.OccupationTxt = ui:GetChild("OccupationTxt")
```

---

## EF/Formation_CardInfoLeftByName.lua.lua
**Functions:**
- GetFormation_CardInfoLeftUis
**Requires:**
- Formation_BuildCostLeftByName
- CommonResource_OccupationByName
- Formation_PlayerHPByName
**Snippet:**
```lua
require("Formation_BuildCostLeftByName")
require("CommonResource_OccupationByName")
require("Formation_PlayerHPByName")

function GetFormation_CardInfoLeftUis(ui)
  local uis = {}
  uis.CardHolder = ui:GetChild("CardHolder")
  uis.BuildingHolder = ui:GetChild("BuildingHolder")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.BuildCost = GetFormation_BuildCostLeftUis(ui:GetChild("BuildCost"))
```

---

## EF/Formation_CardInfoRightByName.lua.lua
**Functions:**
- GetFormation_CardInfoRightUis
**Requires:**
- Formation_BuildCostRightByName
- CommonResource_OccupationByName
- Formation_PlayerHPByName
**Snippet:**
```lua
require("Formation_BuildCostRightByName")
require("CommonResource_OccupationByName")
require("Formation_PlayerHPByName")

function GetFormation_CardInfoRightUis(ui)
  local uis = {}
  uis.CardHolder = ui:GetChild("CardHolder")
  uis.BuildingHolder = ui:GetChild("BuildingHolder")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.BuildCost = GetFormation_BuildCostRightUis(ui:GetChild("BuildCost"))
```

---

## EF/Formation_CardPicBgByName.lua.lua
**Functions:**
- GetFormation_CardPicBgUis
**Snippet:**
```lua
function GetFormation_CardPicBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_CardSkillDescribeBtnByName.lua.lua
**Functions:**
- GetFormation_CardSkillDescribeBtnUis
**Requires:**
- CommonResource_SkillByName
- CommonResource_SkillDetailsTagByName
- CommonResource_SkillDetailsCDByName
- CommonResource_SkillLockByName
**Snippet:**
```lua
require("CommonResource_SkillByName")
require("CommonResource_SkillDetailsTagByName")
require("CommonResource_SkillDetailsCDByName")
require("CommonResource_SkillLockByName")

function GetFormation_CardSkillDescribeBtnUis(ui)
  local uis = {}
  uis.Skill = GetCommonResource_SkillUis(ui:GetChild("Skill"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SkillDetailsTag = GetCommonResource_SkillDetailsTagUis(ui:GetChild("SkillDetailsTag"))
```

---

## EF/Formation_CardSkillModuleByName.lua.lua
**Functions:**
- GetFormation_CardSkillModuleUis
**Snippet:**
```lua
function GetFormation_CardSkillModuleUis(ui)
  local uis = {}
  
  uis.ContentList = ui:GetChild("ContentList")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_CardSkillTypeByName.lua.lua
**Functions:**
- GetFormation_CardSkillTypeUis
**Snippet:**
```lua
function GetFormation_CardSkillTypeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_CardSkillWordByName.lua.lua
**Functions:**
- GetFormation_CardSkillWordUis
**Requires:**
- Formation_CardSkillTypeByName
**Snippet:**
```lua
require("Formation_CardSkillTypeByName")

function GetFormation_CardSkillWordUis(ui)
  local uis = {}
  uis.CardSkillType = GetFormation_CardSkillTypeUis(ui:GetChild("CardSkillType"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_CardTipsByName.lua.lua
**Functions:**
- GetFormation_CardTipsUis
**Requires:**
- CommonResource_PopupBgByName
- Formation_CardPicBgByName
- Formation_CardInfoByName
- Formation_CardSkillModuleByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Formation_CardPicBgByName")
require("Formation_CardInfoByName")
require("Formation_CardSkillModuleByName")

function GetFormation_CardTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.CardPicBg = GetFormation_CardPicBgUis(ui:GetChild("CardPicBg"))
```

---

## EF/Formation_CardTipsWindowByName.lua.lua
**Functions:**
- GetFormation_CardTipsWindowUis
**Requires:**
- Formation_CardTipsByName
**Snippet:**
```lua
require("Formation_CardTipsByName")

function GetFormation_CardTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetFormation_CardTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/Formation_CardUpBtnByName.lua.lua
**Functions:**
- GetFormation_CardUpBtnUis
**Snippet:**
```lua
function GetFormation_CardUpBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_ChoiceAniByName.lua.lua
**Functions:**
- GetFormation_ChoiceAniUis
**Snippet:**
```lua
function GetFormation_ChoiceAniUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## EF/Formation_ChoiceBtnByName.lua.lua
**Functions:**
- GetFormation_ChoiceBtnUis
**Requires:**
- Formation_ChoiceAniByName
**Snippet:**
```lua
require("Formation_ChoiceAniByName")

function GetFormation_ChoiceBtnUis(ui)
  local uis = {}
  uis.ChoiceAni = GetFormation_ChoiceAniUis(ui:GetChild("ChoiceAni"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## EF/Formation_ChoiceByName.lua.lua
**Functions:**
- GetFormation_ChoiceUis
**Requires:**
- Formation_LabeRegionByName
- Formation_ExtendLockByName
**Snippet:**
```lua
require("Formation_LabeRegionByName")
require("Formation_ExtendLockByName")

function GetFormation_ChoiceUis(ui)
  local uis = {}
  uis.TipsList = ui:GetChild("TipsList")
  uis.LabeRegion = GetFormation_LabeRegionUis(ui:GetChild("LabeRegion"))
  uis.CardList = ui:GetChild("CardList")
  uis.ScreenBtn = ui:GetChild("ScreenBtn")
  uis.CardDownBtn = ui:GetChild("CardDownBtn")
```

---

## EF/Formation_ConquersBtnByName.lua.lua
**Functions:**
- GetFormation_ConquersBtnUis
**Snippet:**
```lua
function GetFormation_ConquersBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_DragInfoByName.lua.lua
**Functions:**
- GetFormation_DragInfoUis
**Snippet:**
```lua
function GetFormation_DragInfoUis(ui)
  local uis = {}
  
  uis.DragHolder = ui:GetChild("DragHolder")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_ElementChoiceByName.lua.lua
**Functions:**
- GetFormation_ElementChoiceUis
**Snippet:**
```lua
function GetFormation_ElementChoiceUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.ShuiBtn = ui:GetChild("ShuiBtn")
  uis.HuoBtn = ui:GetChild("HuoBtn")
  uis.MuBtn = ui:GetChild("MuBtn")
  uis.AnBtn = ui:GetChild("AnBtn")
  uis.GuangBtn = ui:GetChild("GuangBtn")
```

---

## EF/Formation_ExpeditionBuffTipsBgByName.lua.lua
**Functions:**
- GetFormation_ExpeditionBuffTipsBgUis
**Snippet:**
```lua
function GetFormation_ExpeditionBuffTipsBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## EF/Formation_ExpeditionBuffTipsByName.lua.lua
**Functions:**
- GetFormation_ExpeditionBuffTipsUis
**Requires:**
- CommonResource_PopupBgByName
- Formation_ExpeditionBuffTipsBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Formation_ExpeditionBuffTipsBgByName")

function GetFormation_ExpeditionBuffTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.BuffTipsBg = GetFormation_ExpeditionBuffTipsBgUis(ui:GetChild("BuffTipsBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
```

---

## EF/Formation_ExpeditionBuffTipsWindowByName.lua.lua
**Functions:**
- GetFormation_ExpeditionBuffTipsWindowUis
**Requires:**
- Formation_ExpeditionBuffTipsByName
**Snippet:**
```lua
require("Formation_ExpeditionBuffTipsByName")

function GetFormation_ExpeditionBuffTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetFormation_ExpeditionBuffTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/Formation_ExpeditionWaveBtnByName.lua.lua
**Functions:**
- GetFormation_ExpeditionWaveBtnUis
**Snippet:**
```lua
function GetFormation_ExpeditionWaveBtnUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_ExpeditionWaveByName.lua.lua
**Functions:**
- GetFormation_ExpeditionWaveUis
**Requires:**
- Formation_ExpeditionWaveCardListByName
**Snippet:**
```lua
require("Formation_ExpeditionWaveCardListByName")

function GetFormation_ExpeditionWaveUis(ui)
  local uis = {}
  uis.CardList = GetFormation_ExpeditionWaveCardListUis(ui:GetChild("CardList"))
  uis.Wave1Btn = ui:GetChild("Wave1Btn")
  uis.Wave2Btn = ui:GetChild("Wave2Btn")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## EF/Formation_ExpeditionWaveCardAniByName.lua.lua
**Functions:**
- GetFormation_ExpeditionWaveCardAniUis
**Requires:**
- Formation_ExpeditionWaveCardByName
**Snippet:**
```lua
require("Formation_ExpeditionWaveCardByName")

function GetFormation_ExpeditionWaveCardAniUis(ui)
  local uis = {}
  uis.Card = GetFormation_ExpeditionWaveCardUis(ui:GetChild("Card"))
  uis.root = ui
  return uis
end
```

---

## EF/Formation_ExpeditionWaveCardBgByName.lua.lua
**Functions:**
- GetFormation_ExpeditionWaveCardBgUis
**Snippet:**
```lua
function GetFormation_ExpeditionWaveCardBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_ExpeditionWaveCardByName.lua.lua
**Functions:**
- GetFormation_ExpeditionWaveCardUis
**Requires:**
- Formation_ExpeditionWaveCardBgByName
**Snippet:**
```lua
require("Formation_ExpeditionWaveCardBgByName")

function GetFormation_ExpeditionWaveCardUis(ui)
  local uis = {}
  uis.HeadBg = GetFormation_ExpeditionWaveCardBgUis(ui:GetChild("HeadBg"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_ExpeditionWaveCardListByName.lua.lua
**Functions:**
- GetFormation_ExpeditionWaveCardListUis
**Snippet:**
```lua
function GetFormation_ExpeditionWaveCardListUis(ui)
  local uis = {}
  
  uis.CardList = ui:GetChild("CardList")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_ExpeditionWaveSwitchBtnByName.lua.lua
**Functions:**
- GetFormation_ExpeditionWaveSwitchBtnUis
**Snippet:**
```lua
function GetFormation_ExpeditionWaveSwitchBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_ExtendLockByName.lua.lua
**Functions:**
- GetFormation_ExtendLockUis
**Snippet:**
```lua
function GetFormation_ExtendLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_FangYuBtnByName.lua.lua
**Functions:**
- GetFormation_FangYuBtnUis
**Requires:**
- Formation_BgAniByName
**Snippet:**
```lua
require("Formation_BgAniByName")

function GetFormation_FangYuBtnUis(ui)
  local uis = {}
  uis.BgAni = GetFormation_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_FaShiBtnByName.lua.lua
**Functions:**
- GetFormation_FaShiBtnUis
**Requires:**
- Formation_BgAniByName
**Snippet:**
```lua
require("Formation_BgAniByName")

function GetFormation_FaShiBtnUis(ui)
  local uis = {}
  uis.BgAni = GetFormation_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_FormationByName.lua.lua
**Functions:**
- GetFormation_FormationUis
**Requires:**
- CommonResource_BackGroundByName
- Formation_FormationGridByName
- Formation_GuildBossHPRegionByName
- Formation_ExpeditionWaveByName
- Formation_ChoiceByName
- Formation_BurstStripByName
- CommonResource_CurrencyReturnByName
- Formation_ScreenChoiceByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Formation_FormationGridByName")
require("Formation_GuildBossHPRegionByName")
require("Formation_ExpeditionWaveByName")
require("Formation_ChoiceByName")
require("Formation_BurstStripByName")
require("CommonResource_CurrencyReturnByName")
require("Formation_ScreenChoiceByName")

function GetFormation_FormationUis(ui)
```

---

## EF/Formation_FormationGridByName.lua.lua
**Functions:**
- GetFormation_FormationGridUis
**Snippet:**
```lua
function GetFormation_FormationGridUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## EF/Formation_FormationGridCenterByName.lua.lua
**Functions:**
- GetFormation_FormationGridCenterUis
**Snippet:**
```lua
function GetFormation_FormationGridCenterUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## EF/Formation_FormationGridEdgeByName.lua.lua
**Functions:**
- GetFormation_FormationGridEdgeUis
**Snippet:**
```lua
function GetFormation_FormationGridEdgeUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## EF/Formation_FormationGridEdgeVerByName.lua.lua
**Functions:**
- GetFormation_FormationGridEdgeVerUis
**Snippet:**
```lua
function GetFormation_FormationGridEdgeVerUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## EF/Formation_FormationGridLineByName.lua.lua
**Functions:**
- GetFormation_FormationGridLineUis
**Requires:**
- Formation_FormationGridCenterByName
- Formation_FormationGridEdgeByName
- Formation_FormationGridEdgeVerByName
**Snippet:**
```lua
require("Formation_FormationGridCenterByName")
require("Formation_FormationGridEdgeByName")
require("Formation_FormationGridEdgeVerByName")

function GetFormation_FormationGridLineUis(ui)
  local uis = {}
  uis.Center = GetFormation_FormationGridCenterUis(ui:GetChild("Center"))
  uis.Top = GetFormation_FormationGridEdgeUis(ui:GetChild("Top"))
  uis.Down = GetFormation_FormationGridEdgeUis(ui:GetChild("Down"))
  uis.Left = GetFormation_FormationGridEdgeVerUis(ui:GetChild("Left"))
```

---

## EF/Formation_FormationWindowByName.lua.lua
**Functions:**
- GetFormation_FormationWindowUis
**Requires:**
- Formation_FormationByName
**Snippet:**
```lua
require("Formation_FormationByName")

function GetFormation_FormationWindowUis(ui)
  local uis = {}
  uis.Main = GetFormation_FormationUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/Formation_GongJianBtnByName.lua.lua
**Functions:**
- GetFormation_GongJianBtnUis
**Requires:**
- Formation_BgAniByName
**Snippet:**
```lua
require("Formation_BgAniByName")

function GetFormation_GongJianBtnUis(ui)
  local uis = {}
  uis.BgAni = GetFormation_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_GoToBtnByName.lua.lua
**Functions:**
- GetFormation_GoToBtnUis
**Snippet:**
```lua
function GetFormation_GoToBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_GuangBtnByName.lua.lua
**Functions:**
- GetFormation_GuangBtnUis
**Requires:**
- Formation_BgAniByName
**Snippet:**
```lua
require("Formation_BgAniByName")

function GetFormation_GuangBtnUis(ui)
  local uis = {}
  uis.BgAni = GetFormation_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_GuildBossHPHeadBgByName.lua.lua
**Functions:**
- GetFormation_GuildBossHPHeadBgUis
**Snippet:**
```lua
function GetFormation_GuildBossHPHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_GuildBossHPHeadByName.lua.lua
**Functions:**
- GetFormation_GuildBossHPHeadUis
**Requires:**
- Formation_GuildBossHPHeadBgByName
**Snippet:**
```lua
require("Formation_GuildBossHPHeadBgByName")

function GetFormation_GuildBossHPHeadUis(ui)
  local uis = {}
  uis.Pic = GetFormation_GuildBossHPHeadBgUis(ui:GetChild("Pic"))
  uis.root = ui
  return uis
end
```

---

## EF/Formation_GuildBossHPProgressBarByName.lua.lua
**Functions:**
- GetFormation_GuildBossHPProgressBarUis
**Requires:**
- Formation_GuildBossHPProgressFillByName
**Snippet:**
```lua
require("Formation_GuildBossHPProgressFillByName")

function GetFormation_GuildBossHPProgressBarUis(ui)
  local uis = {}
  uis.bar = GetFormation_GuildBossHPProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## EF/Formation_GuildBossHPProgressFillByName.lua.lua
**Functions:**
- GetFormation_GuildBossHPProgressFillUis
**Snippet:**
```lua
function GetFormation_GuildBossHPProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## EF/Formation_GuildBossHPRegionByName.lua.lua
**Functions:**
- GetFormation_GuildBossHPRegionUis
**Requires:**
- CommonResource_OccupationByName
- Formation_GuildBossHPHeadByName
**Snippet:**
```lua
require("CommonResource_OccupationByName")
require("Formation_GuildBossHPHeadByName")

function GetFormation_GuildBossHPRegionUis(ui)
  local uis = {}
  uis.HPProgressBar = ui:GetChild("HPProgressBar")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Occupation = GetCommonResource_OccupationUis(ui:GetChild("Occupation"))
  uis.ElementList = ui:GetChild("ElementList")
  uis.Head = GetFormation_GuildBossHPHeadUis(ui:GetChild("Head"))
```

---

## EF/Formation_HuoBtnByName.lua.lua
**Functions:**
- GetFormation_HuoBtnUis
**Requires:**
- Formation_BgAniByName
**Snippet:**
```lua
require("Formation_BgAniByName")

function GetFormation_HuoBtnUis(ui)
  local uis = {}
  uis.BgAni = GetFormation_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_JinZhanBtnByName.lua.lua
**Functions:**
- GetFormation_JinZhanBtnUis
**Requires:**
- Formation_BgAniByName
**Snippet:**
```lua
require("Formation_BgAniByName")

function GetFormation_JinZhanBtnUis(ui)
  local uis = {}
  uis.BgAni = GetFormation_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_LabelDownBtnByName.lua.lua
**Functions:**
- GetFormation_LabelDownBtnUis
**Snippet:**
```lua
function GetFormation_LabelDownBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_LabelTopBtnByName.lua.lua
**Functions:**
- GetFormation_LabelTopBtnUis
**Snippet:**
```lua
function GetFormation_LabelTopBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_LabeRegionByName.lua.lua
**Functions:**
- GetFormation_LabeRegionUis
**Requires:**
- CommonResource_ArenaDefendNewByName
**Snippet:**
```lua
require("CommonResource_ArenaDefendNewByName")

function GetFormation_LabeRegionUis(ui)
  local uis = {}
  uis.LabelTopBtn = ui:GetChild("LabelTopBtn")
  uis.LabelDownBtn = ui:GetChild("LabelDownBtn")
  uis.New = GetCommonResource_ArenaDefendNewUis(ui:GetChild("New"))
  uis.c1Ctr = ui:GetController("c1")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
```

---

## EF/Formation_LeaderHeadBgByName.lua.lua
**Functions:**
- GetFormation_LeaderHeadBgUis
**Snippet:**
```lua
function GetFormation_LeaderHeadBgUis(ui)
  local uis = {}
  
  uis.HeadLoader = ui:GetChild("HeadLoader")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_LeaderHeadByName.lua.lua
**Functions:**
- GetFormation_LeaderHeadUis
**Requires:**
- Formation_LeaderHeadBgByName
**Snippet:**
```lua
require("Formation_LeaderHeadBgByName")

function GetFormation_LeaderHeadUis(ui)
  local uis = {}
  uis.LeaderHeadBg = GetFormation_LeaderHeadBgUis(ui:GetChild("LeaderHeadBg"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_LockTipsByName.lua.lua
**Functions:**
- GetFormation_LockTipsUis
**Snippet:**
```lua
function GetFormation_LockTipsUis(ui)
  local uis = {}
  
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_MapBtnByName.lua.lua
**Functions:**
- GetFormation_MapBtnUis
**Requires:**
- Formation_MapPicByName
- CommonResource_ArenaDefendNewByName
**Snippet:**
```lua
require("Formation_MapPicByName")
require("CommonResource_ArenaDefendNewByName")

function GetFormation_MapBtnUis(ui)
  local uis = {}
  uis.MapPic = GetFormation_MapPicUis(ui:GetChild("MapPic"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.New = GetCommonResource_ArenaDefendNewUis(ui:GetChild("New"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
```

---

## EF/Formation_MapIconBtnByName.lua.lua
**Functions:**
- GetFormation_MapIconBtnUis
**Requires:**
- Formation_MapIconPicByName
- Formation_UseTipsByName
- CommonResource_ArenaDefendNewByName
**Snippet:**
```lua
require("Formation_MapIconPicByName")
require("Formation_UseTipsByName")
require("CommonResource_ArenaDefendNewByName")

function GetFormation_MapIconBtnUis(ui)
  local uis = {}
  uis.MapIconPic = GetFormation_MapIconPicUis(ui:GetChild("MapIconPic"))
  uis.UseTips = GetFormation_UseTipsUis(ui:GetChild("UseTips"))
  uis.New = GetCommonResource_ArenaDefendNewUis(ui:GetChild("New"))
  uis.buttonCtr = ui:GetController("button")
```

---

## EF/Formation_MapIconPicByName.lua.lua
**Functions:**
- GetFormation_MapIconPicUis
**Snippet:**
```lua
function GetFormation_MapIconPicUis(ui)
  local uis = {}
  
  uis.IconLoader = ui:GetChild("IconLoader")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_MapInfoByName.lua.lua
**Functions:**
- GetFormation_MapInfoUis
**Snippet:**
```lua
function GetFormation_MapInfoUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_MapPicByName.lua.lua
**Functions:**
- GetFormation_MapPicUis
**Snippet:**
```lua
function GetFormation_MapPicUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_MonsterAttributeByName.lua.lua
**Functions:**
- GetFormation_MonsterAttributeUis
**Snippet:**
```lua
function GetFormation_MonsterAttributeUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_MonsterAttributeModuleByName.lua.lua
**Functions:**
- GetFormation_MonsterAttributeModuleUis
**Snippet:**
```lua
function GetFormation_MonsterAttributeModuleUis(ui)
  local uis = {}
  
  uis.ContentList = ui:GetChild("ContentList")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_MonsterInfoByName.lua.lua
**Functions:**
- GetFormation_MonsterInfoUis
**Requires:**
- Formation_MonsterTypeByName
- CommonResource_OccupationByName
- Formation_MonsterAttributeModuleByName
**Snippet:**
```lua
require("Formation_MonsterTypeByName")
require("CommonResource_OccupationByName")
require("Formation_MonsterAttributeModuleByName")

function GetFormation_MonsterInfoUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.MonsterType = GetFormation_MonsterTypeUis(ui:GetChild("MonsterType"))
  uis.Occupation = GetCommonResource_OccupationUis(ui:GetChild("Occupation"))
  uis.OccupationTxt = ui:GetChild("OccupationTxt")
```

---

## EF/Formation_MonsterPicByName.lua.lua
**Functions:**
- GetFormation_MonsterPicUis
**Snippet:**
```lua
function GetFormation_MonsterPicUis(ui)
  local uis = {}
  
  uis.MonsterLoader = ui:GetChild("MonsterLoader")
  uis.MonsterHolder = ui:GetChild("MonsterHolder")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_MonsterSkillByName.lua.lua
**Functions:**
- GetFormation_MonsterSkillUis
**Snippet:**
```lua
function GetFormation_MonsterSkillUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_MonsterTipsByName.lua.lua
**Functions:**
- GetFormation_MonsterTipsUis
**Requires:**
- CommonResource_PopupBgByName
- Formation_MonsterPicByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Formation_MonsterPicByName")

function GetFormation_MonsterTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.MonsterInfoList = ui:GetChild("MonsterInfoList")
  uis.MonsterPic = GetFormation_MonsterPicUis(ui:GetChild("MonsterPic"))
  uis.root = ui
```

---

## EF/Formation_MonsterTipsWindowByName.lua.lua
**Functions:**
- GetFormation_MonsterTipsWindowUis
**Requires:**
- Formation_MonsterTipsByName
**Snippet:**
```lua
require("Formation_MonsterTipsByName")

function GetFormation_MonsterTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetFormation_MonsterTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/Formation_MonsterTypeByName.lua.lua
**Functions:**
- GetFormation_MonsterTypeUis
**Snippet:**
```lua
function GetFormation_MonsterTypeUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_MuBtnByName.lua.lua
**Functions:**
- GetFormation_MuBtnUis
**Requires:**
- Formation_BgAniByName
**Snippet:**
```lua
require("Formation_BgAniByName")

function GetFormation_MuBtnUis(ui)
  local uis = {}
  uis.BgAni = GetFormation_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_NumberInfoByName.lua.lua
**Functions:**
- GetFormation_NumberInfoUis
**Snippet:**
```lua
function GetFormation_NumberInfoUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_OccupationChoiceByName.lua.lua
**Functions:**
- GetFormation_OccupationChoiceUis
**Snippet:**
```lua
function GetFormation_OccupationChoiceUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.FangYuBtn = ui:GetChild("FangYuBtn")
  uis.JinZhanBtn = ui:GetChild("JinZhanBtn")
  uis.FaShiBtn = ui:GetChild("FaShiBtn")
  uis.GongJianBtn = ui:GetChild("GongJianBtn")
  uis.c1Ctr = ui:GetController("c1")
```

---

## EF/Formation_OpenTipsByName.lua.lua
**Functions:**
- GetFormation_OpenTipsUis
**Snippet:**
```lua
function GetFormation_OpenTipsUis(ui)
  local uis = {}
  
  uis.NumberTipsTxt = ui:GetChild("NumberTipsTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_OprTipsByName.lua.lua
**Functions:**
- GetFormation_OprTipsUis
**Requires:**
- Formation_OprTipsMapByName
**Snippet:**
```lua
require("Formation_OprTipsMapByName")

function GetFormation_OprTipsUis(ui)
  local uis = {}
  uis.OprTipsMap = GetFormation_OprTipsMapUis(ui:GetChild("OprTipsMap"))
  uis.MapBtn = ui:GetChild("MapBtn")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_OprTipsMapByName.lua.lua
**Functions:**
- GetFormation_OprTipsMapUis
**Requires:**
- Formation_LockTipsByName
**Snippet:**
```lua
require("Formation_LockTipsByName")

function GetFormation_OprTipsMapUis(ui)
  local uis = {}
  uis.MapList = ui:GetChild("MapList")
  uis.ContentList = ui:GetChild("ContentList")
  uis.UseBtn = ui:GetChild("UseBtn")
  uis.LockTips = GetFormation_LockTipsUis(ui:GetChild("LockTips"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## EF/Formation_OprTipsMapRegionByName.lua.lua
**Functions:**
- GetFormation_OprTipsMapRegionUis
**Snippet:**
```lua
function GetFormation_OprTipsMapRegionUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.ContentList = ui:GetChild("ContentList")
  uis.NoBuffTxt = ui:GetChild("NoBuffTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## EF/Formation_PlaceLatticeByName.lua.lua
**Functions:**
- GetFormation_PlaceLatticeUis
**Snippet:**
```lua
function GetFormation_PlaceLatticeUis(ui)
  local uis = {}
  
  uis.PlaceEnableHolder = ui:GetChild("PlaceEnableHolder")
  uis.PlaceUnableHolder = ui:GetChild("PlaceUnableHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_PlayerHPByName.lua.lua
**Functions:**
- GetFormation_PlayerHPUis
**Snippet:**
```lua
function GetFormation_PlayerHPUis(ui)
  local uis = {}
  
  uis.HpProgressBar = ui:GetChild("HpProgressBar")
  uis.HpMonsterProgressBar = ui:GetChild("HpMonsterProgressBar")
  uis.HpEliteProgressBar = ui:GetChild("HpEliteProgressBar")
  uis.HpBossProgressBar = ui:GetChild("HpBossProgressBar")
  uis.HpBuildProgressBar = ui:GetChild("HpBuildProgressBar")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## EF/Formation_QueueChoiceByName.lua.lua
**Functions:**
- GetFormation_QueueChoiceUis
**Snippet:**
```lua
function GetFormation_QueueChoiceUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.TeamList = ui:GetChild("TeamList")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_RangeLatticeByName.lua.lua
**Functions:**
- GetFormation_RangeLatticeUis
**Snippet:**
```lua
function GetFormation_RangeLatticeUis(ui)
  local uis = {}
  
  uis.RangeHolder = ui:GetChild("RangeHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_RestraintTipsByName.lua.lua
**Functions:**
- GetFormation_RestraintTipsUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetFormation_RestraintTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_RestraintTipsWindowByName.lua.lua
**Functions:**
- GetFormation_RestraintTipsWindowUis
**Requires:**
- Formation_RestraintTipsByName
**Snippet:**
```lua
require("Formation_RestraintTipsByName")

function GetFormation_RestraintTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetFormation_RestraintTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/Formation_RoundStripAddBtnByName.lua.lua
**Functions:**
- GetFormation_RoundStripAddBtnUis
**Snippet:**
```lua
function GetFormation_RoundStripAddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_RoundStripByName.lua.lua
**Functions:**
- GetFormation_RoundStripUis
**Requires:**
- Formation_RoundStripCardByName
**Snippet:**
```lua
require("Formation_RoundStripCardByName")

function GetFormation_RoundStripUis(ui)
  local uis = {}
  uis.AddBtn = ui:GetChild("AddBtn")
  uis.StripCard = GetFormation_RoundStripCardUis(ui:GetChild("StripCard"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_RoundStripCardByName.lua.lua
**Functions:**
- GetFormation_RoundStripCardUis
**Requires:**
- Formation_SetChoiceTimeByName
**Snippet:**
```lua
require("Formation_SetChoiceTimeByName")

function GetFormation_RoundStripCardUis(ui)
  local uis = {}
  uis.SetChoiceTime = GetFormation_SetChoiceTimeUis(ui:GetChild("SetChoiceTime"))
  uis.HeadList = ui:GetChild("HeadList")
  uis.RoundTxt = ui:GetChild("RoundTxt")
  uis.DeleteBtn = ui:GetChild("DeleteBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## EF/Formation_RoundStripCardHeadBgByName.lua.lua
**Functions:**
- GetFormation_RoundStripCardHeadBgUis
**Snippet:**
```lua
function GetFormation_RoundStripCardHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_RoundStripCardHeadByName.lua.lua
**Functions:**
- GetFormation_RoundStripCardHeadUis
**Requires:**
- Formation_RoundStripCardHeadBgByName
- CommonResource_OccupationByName
**Snippet:**
```lua
require("Formation_RoundStripCardHeadBgByName")
require("CommonResource_OccupationByName")

function GetFormation_RoundStripCardHeadUis(ui)
  local uis = {}
  uis.HeadBg = GetFormation_RoundStripCardHeadBgUis(ui:GetChild("HeadBg"))
  uis.Occupation = GetCommonResource_OccupationUis(ui:GetChild("Occupation"))
  uis.ElementList = ui:GetChild("ElementList")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## EF/Formation_RoundStripDeleteBtnByName.lua.lua
**Functions:**
- GetFormation_RoundStripDeleteBtnUis
**Snippet:**
```lua
function GetFormation_RoundStripDeleteBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_RoundStripOcpByName.lua.lua
**Functions:**
- GetFormation_RoundStripOcpUis
**Requires:**
- Formation_RoundStripOcpTitleByName
**Snippet:**
```lua
require("Formation_RoundStripOcpTitleByName")

function GetFormation_RoundStripOcpUis(ui)
  local uis = {}
  uis.RoundStripOcpTitle = GetFormation_RoundStripOcpTitleUis(ui:GetChild("RoundStripOcpTitle"))
  uis.HeadList = ui:GetChild("HeadList")
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## EF/Formation_RoundStripOcpHeadBgByName.lua.lua
**Functions:**
- GetFormation_RoundStripOcpHeadBgUis
**Snippet:**
```lua
function GetFormation_RoundStripOcpHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_RoundStripOcpHeadByName.lua.lua
**Functions:**
- GetFormation_RoundStripOcpHeadUis
**Requires:**
- Formation_RoundStripOcpHeadBgByName
- CommonResource_OccupationByName
**Snippet:**
```lua
require("Formation_RoundStripOcpHeadBgByName")
require("CommonResource_OccupationByName")

function GetFormation_RoundStripOcpHeadUis(ui)
  local uis = {}
  uis.HeadBg = GetFormation_RoundStripOcpHeadBgUis(ui:GetChild("HeadBg"))
  uis.Occupation = GetCommonResource_OccupationUis(ui:GetChild("Occupation"))
  uis.ElementList = ui:GetChild("ElementList")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
```

---

## EF/Formation_RoundStripOcpTitleByName.lua.lua
**Functions:**
- GetFormation_RoundStripOcpTitleUis
**Snippet:**
```lua
function GetFormation_RoundStripOcpTitleUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_RoundStripWord1ByName.lua.lua
**Functions:**
- GetFormation_RoundStripWord1Uis
**Snippet:**
```lua
function GetFormation_RoundStripWord1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_RoundStripWordByName.lua.lua
**Functions:**
- GetFormation_RoundStripWordUis
**Snippet:**
```lua
function GetFormation_RoundStripWordUis(ui)
  local uis = {}
  
  uis.WordList = ui:GetChild("WordList")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_RoundSwitchBtnByName.lua.lua
**Functions:**
- GetFormation_RoundSwitchBtnUis
**Snippet:**
```lua
function GetFormation_RoundSwitchBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_RoundTimeSetByName.lua.lua
**Functions:**
- GetFormation_RoundTimeSetUis
**Requires:**
- Formation_TimeSetStripByName
**Snippet:**
```lua
require("Formation_TimeSetStripByName")

function GetFormation_RoundTimeSetUis(ui)
  local uis = {}
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.TimeSetStrip = GetFormation_TimeSetStripUis(ui:GetChild("TimeSetStrip"))
  uis.root = ui
  return uis
end
```

---

## EF/Formation_ScreenBtnByName.lua.lua
**Functions:**
- GetFormation_ScreenBtnUis
**Snippet:**
```lua
function GetFormation_ScreenBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_ScreenChoiceByName.lua.lua
**Functions:**
- GetFormation_ScreenChoiceUis
**Requires:**
- Formation_ScreenTipsByName
- Formation_OprTipsByName
- Formation_TacticSkillByName
**Snippet:**
```lua
require("Formation_ScreenTipsByName")
require("Formation_OprTipsByName")
require("Formation_TacticSkillByName")

function GetFormation_ScreenChoiceUis(ui)
  local uis = {}
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.ScreenTips = GetFormation_ScreenTipsUis(ui:GetChild("ScreenTips"))
  uis.OprTips = GetFormation_OprTipsUis(ui:GetChild("OprTips"))
  uis.TacticSkill = GetFormation_TacticSkillUis(ui:GetChild("TacticSkill"))
```

---

## EF/Formation_ScreenTipsByName.lua.lua
**Functions:**
- GetFormation_ScreenTipsUis
**Requires:**
- Formation_ElementChoiceByName
- Formation_OccupationChoiceByName
- Formation_QueueChoiceByName
- Formation_SkillCDChoiceByName
**Snippet:**
```lua
require("Formation_ElementChoiceByName")
require("Formation_OccupationChoiceByName")
require("Formation_QueueChoiceByName")
require("Formation_SkillCDChoiceByName")

function GetFormation_ScreenTipsUis(ui)
  local uis = {}
  uis.ElementChoice = GetFormation_ElementChoiceUis(ui:GetChild("ElementChoice"))
  uis.OccupationChoice = GetFormation_OccupationChoiceUis(ui:GetChild("OccupationChoice"))
  uis.QueueChoice = GetFormation_QueueChoiceUis(ui:GetChild("QueueChoice"))
```

---

## EF/Formation_SetCDByName.lua.lua
**Functions:**
- GetFormation_SetCDUis
**Snippet:**
```lua
function GetFormation_SetCDUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_SetChoiceCardBgByName.lua.lua
**Functions:**
- GetFormation_SetChoiceCardBgUis
**Snippet:**
```lua
function GetFormation_SetChoiceCardBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_SetChoiceCardBtnByName.lua.lua
**Functions:**
- GetFormation_SetChoiceCardBtnUis
**Requires:**
- Formation_SetChoiceCardByName
- Formation_SetSelectedByName
- Formation_SetSelected1ByName
**Snippet:**
```lua
require("Formation_SetChoiceCardByName")
require("Formation_SetSelectedByName")
require("Formation_SetSelected1ByName")

function GetFormation_SetChoiceCardBtnUis(ui)
  local uis = {}
  uis.CardHead = GetFormation_SetChoiceCardUis(ui:GetChild("CardHead"))
  uis.SetSelected = GetFormation_SetSelectedUis(ui:GetChild("SetSelected"))
  uis.SetSelected1 = GetFormation_SetSelected1Uis(ui:GetChild("SetSelected1"))
  uis.buttonCtr = ui:GetController("button")
```

---

## EF/Formation_SetChoiceCardByName.lua.lua
**Functions:**
- GetFormation_SetChoiceCardUis
**Requires:**
- Formation_SetChoiceCardBgByName
- CommonResource_OccupationByName
**Snippet:**
```lua
require("Formation_SetChoiceCardBgByName")
require("CommonResource_OccupationByName")

function GetFormation_SetChoiceCardUis(ui)
  local uis = {}
  uis.PicMask = GetFormation_SetChoiceCardBgUis(ui:GetChild("PicMask"))
  uis.Occupation = GetCommonResource_OccupationUis(ui:GetChild("Occupation"))
  uis.ElementList = ui:GetChild("ElementList")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## EF/Formation_SetChoiceTimeBgByName.lua.lua
**Functions:**
- GetFormation_SetChoiceTimeBgUis
**Snippet:**
```lua
function GetFormation_SetChoiceTimeBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## EF/Formation_SetChoiceTimeByName.lua.lua
**Functions:**
- GetFormation_SetChoiceTimeUis
**Requires:**
- Formation_SetChoiceTimeBgByName
**Snippet:**
```lua
require("Formation_SetChoiceTimeBgByName")

function GetFormation_SetChoiceTimeUis(ui)
  local uis = {}
  uis.n6 = GetFormation_SetChoiceTimeBgUis(ui:GetChild("n6"))
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_SetRoundRegionByName.lua.lua
**Functions:**
- GetFormation_SetRoundRegionUis
**Snippet:**
```lua
function GetFormation_SetRoundRegionUis(ui)
  local uis = {}
  
  uis.CardList = ui:GetChild("CardList")
  uis.WordList = ui:GetChild("WordList")
  uis.SwitchBtn = ui:GetChild("SwitchBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_SetSelected1ByName.lua.lua
**Functions:**
- GetFormation_SetSelected1Uis
**Snippet:**
```lua
function GetFormation_SetSelected1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_SetSelectedByName.lua.lua
**Functions:**
- GetFormation_SetSelectedUis
**Snippet:**
```lua
function GetFormation_SetSelectedUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_ShuiBtnByName.lua.lua
**Functions:**
- GetFormation_ShuiBtnUis
**Requires:**
- Formation_BgAniByName
**Snippet:**
```lua
require("Formation_BgAniByName")

function GetFormation_ShuiBtnUis(ui)
  local uis = {}
  uis.BgAni = GetFormation_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_SkillCDChoiceByName.lua.lua
**Functions:**
- GetFormation_SkillCDChoiceUis
**Snippet:**
```lua
function GetFormation_SkillCDChoiceUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.Time20Btn = ui:GetChild("Time20Btn")
  uis.Time45Btn = ui:GetChild("Time45Btn")
  uis.Time70Btn = ui:GetChild("Time70Btn")
  uis.TimeSpecialBtn = ui:GetChild("TimeSpecialBtn")
  uis.c1Ctr = ui:GetController("c1")
```

---

## EF/Formation_SpecialBtnByName.lua.lua
**Functions:**
- GetFormation_SpecialBtnUis
**Requires:**
- Formation_BgAniByName
**Snippet:**
```lua
require("Formation_BgAniByName")

function GetFormation_SpecialBtnUis(ui)
  local uis = {}
  uis.BgAni = GetFormation_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_StarConditionBgByName.lua.lua
**Functions:**
- GetFormation_StarConditionBgUis
**Snippet:**
```lua
function GetFormation_StarConditionBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## EF/Formation_StarConditionBtnByName.lua.lua
**Functions:**
- GetFormation_StarConditionBtnUis
**Snippet:**
```lua
function GetFormation_StarConditionBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_StarConditionTargetAniByName.lua.lua
**Functions:**
- GetFormation_StarConditionTargetAniUis
**Requires:**
- Formation_StarConditionTargetByName
**Snippet:**
```lua
require("Formation_StarConditionTargetByName")

function GetFormation_StarConditionTargetAniUis(ui)
  local uis = {}
  uis.Target = GetFormation_StarConditionTargetUis(ui:GetChild("Target"))
  uis.root = ui
  return uis
end
```

---

## EF/Formation_StarConditionTargetByName.lua.lua
**Functions:**
- GetFormation_StarConditionTargetUis
**Snippet:**
```lua
function GetFormation_StarConditionTargetUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_StarConditionTipsByName.lua.lua
**Functions:**
- GetFormation_StarConditionTipsUis
**Requires:**
- CommonResource_PopupBgByName
- Formation_StarConditionBgByName
- Formation_StarConditionTitleByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Formation_StarConditionBgByName")
require("Formation_StarConditionTitleByName")

function GetFormation_StarConditionTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.StarConditionBg = GetFormation_StarConditionBgUis(ui:GetChild("StarConditionBg"))
  uis.Title = GetFormation_StarConditionTitleUis(ui:GetChild("Title"))
```

---

## EF/Formation_StarConditionTipsWindowByName.lua.lua
**Functions:**
- GetFormation_StarConditionTipsWindowUis
**Requires:**
- Formation_StarConditionTipsByName
**Snippet:**
```lua
require("Formation_StarConditionTipsByName")

function GetFormation_StarConditionTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetFormation_StarConditionTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/Formation_StarConditionTitleByName.lua.lua
**Functions:**
- GetFormation_StarConditionTitleUis
**Snippet:**
```lua
function GetFormation_StarConditionTitleUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_TacticBtnByName.lua.lua
**Functions:**
- GetFormation_TacticBtnUis
**Snippet:**
```lua
function GetFormation_TacticBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_TacticProgrammeUseBtnByName.lua.lua
**Functions:**
- GetFormation_TacticProgrammeUseBtnUis
**Snippet:**
```lua
function GetFormation_TacticProgrammeUseBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_TacticProgrammeUseStateByName.lua.lua
**Functions:**
- GetFormation_TacticProgrammeUseStateUis
**Snippet:**
```lua
function GetFormation_TacticProgrammeUseStateUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_TacticSkill1ByName.lua.lua
**Functions:**
- GetFormation_TacticSkill1Uis
**Snippet:**
```lua
function GetFormation_TacticSkill1Uis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_TacticSkillByName.lua.lua
**Functions:**
- GetFormation_TacticSkillUis
**Requires:**
- Formation_TacticSkillEffectRegionByName
- Formation_TacticSkillRegionByName
- Formation_TacticSkillLevelByName
- Formation_TacticSkillLockByName
**Snippet:**
```lua
require("Formation_TacticSkillEffectRegionByName")
require("Formation_TacticSkillRegionByName")
require("Formation_TacticSkillLevelByName")
require("Formation_TacticSkillLockByName")

function GetFormation_TacticSkillUis(ui)
  local uis = {}
  uis.EffectRegion = GetFormation_TacticSkillEffectRegionUis(ui:GetChild("EffectRegion"))
  uis.ProgrammeList = ui:GetChild("ProgrammeList")
  uis.SkillRegion = GetFormation_TacticSkillRegionUis(ui:GetChild("SkillRegion"))
```

---

## EF/Formation_TacticSkillEffectLevelByName.lua.lua
**Functions:**
- GetFormation_TacticSkillEffectLevelUis
**Requires:**
- Formation_TacticSkillEffectLevelSignByName
**Snippet:**
```lua
require("Formation_TacticSkillEffectLevelSignByName")

function GetFormation_TacticSkillEffectLevelUis(ui)
  local uis = {}
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Sign = GetFormation_TacticSkillEffectLevelSignUis(ui:GetChild("Sign"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## EF/Formation_TacticSkillEffectLevelSignByName.lua.lua
**Functions:**
- GetFormation_TacticSkillEffectLevelSignUis
**Snippet:**
```lua
function GetFormation_TacticSkillEffectLevelSignUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_TacticSkillEffectRegionByName.lua.lua
**Functions:**
- GetFormation_TacticSkillEffectRegionUis
**Snippet:**
```lua
function GetFormation_TacticSkillEffectRegionUis(ui)
  local uis = {}
  
  uis.EffectList = ui:GetChild("EffectList")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_TacticSkillGoBtnByName.lua.lua
**Functions:**
- GetFormation_TacticSkillGoBtnUis
**Snippet:**
```lua
function GetFormation_TacticSkillGoBtnUis(ui)
  local uis = {}
  
  uis.SkillList = ui:GetChild("SkillList")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_TacticSkillLevelByName.lua.lua
**Functions:**
- GetFormation_TacticSkillLevelUis
**Snippet:**
```lua
function GetFormation_TacticSkillLevelUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.maxCtr = ui:GetController("max")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_TacticSkillLockByName.lua.lua
**Functions:**
- GetFormation_TacticSkillLockUis
**Snippet:**
```lua
function GetFormation_TacticSkillLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_TacticSkillLookBtnByName.lua.lua
**Functions:**
- GetFormation_TacticSkillLookBtnUis
**Snippet:**
```lua
function GetFormation_TacticSkillLookBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_TacticSkillModuleBtnByName.lua.lua
**Functions:**
- GetFormation_TacticSkillModuleBtnUis
**Requires:**
- Formation_TacticSkillWearByName
**Snippet:**
```lua
require("Formation_TacticSkillWearByName")

function GetFormation_TacticSkillModuleBtnUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.Wear = GetFormation_TacticSkillWearUis(ui:GetChild("Wear"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.wearCtr = ui:GetController("wear")
```

---

## EF/Formation_TacticSkillNumberByName.lua.lua
**Functions:**
- GetFormation_TacticSkillNumberUis
**Snippet:**
```lua
function GetFormation_TacticSkillNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.ElementList = ui:GetChild("ElementList")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## EF/Formation_TacticSkillRegionByName.lua.lua
**Functions:**
- GetFormation_TacticSkillRegionUis
**Requires:**
- Formation_TacticProgrammeUseStateByName
**Snippet:**
```lua
require("Formation_TacticProgrammeUseStateByName")

function GetFormation_TacticSkillRegionUis(ui)
  local uis = {}
  uis.SkillList = ui:GetChild("SkillList")
  uis.UseBtn = ui:GetChild("UseBtn")
  uis.UseState = GetFormation_TacticProgrammeUseStateUis(ui:GetChild("UseState"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## EF/Formation_TacticSkillUpBtnByName.lua.lua
**Functions:**
- GetFormation_TacticSkillUpBtnUis
**Snippet:**
```lua
function GetFormation_TacticSkillUpBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## EF/Formation_TacticSkillWearBtnByName.lua.lua
**Functions:**
- GetFormation_TacticSkillWearBtnUis
**Snippet:**
```lua
function GetFormation_TacticSkillWearBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.maxCtr = ui:GetController("max")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_TacticSkillWearByName.lua.lua
**Functions:**
- GetFormation_TacticSkillWearUis
**Snippet:**
```lua
function GetFormation_TacticSkillWearUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_TacticSkillWordByName.lua.lua
**Functions:**
- GetFormation_TacticSkillWordUis
**Snippet:**
```lua
function GetFormation_TacticSkillWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_TargetLatticeByName.lua.lua
**Functions:**
- GetFormation_TargetLatticeUis
**Snippet:**
```lua
function GetFormation_TargetLatticeUis(ui)
  local uis = {}
  
  uis.TargetHolder = ui:GetChild("TargetHolder")
  uis.WhiteTargetHolder = ui:GetChild("WhiteTargetHolder")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_TargetLineInfoByName.lua.lua
**Functions:**
- GetFormation_TargetLineInfoUis
**Snippet:**
```lua
function GetFormation_TargetLineInfoUis(ui)
  local uis = {}
  
  uis.TargetLineHolder = ui:GetChild("TargetLineHolder")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_TimeAddBtnByName.lua.lua
**Functions:**
- GetFormation_TimeAddBtnUis
**Snippet:**
```lua
function GetFormation_TimeAddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_TimeReduceBtnByName.lua.lua
**Functions:**
- GetFormation_TimeReduceBtnUis
**Snippet:**
```lua
function GetFormation_TimeReduceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_TimeScaleByName.lua.lua
**Functions:**
- GetFormation_TimeScaleUis
**Snippet:**
```lua
function GetFormation_TimeScaleUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_TimeSetStripByName.lua.lua
**Functions:**
- GetFormation_TimeSetStripUis
**Snippet:**
```lua
function GetFormation_TimeSetStripUis(ui)
  local uis = {}
  
  uis.ScaleList = ui:GetChild("ScaleList")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.AddBtn = ui:GetChild("AddBtn")
  uis.ReduceBtn = ui:GetChild("ReduceBtn")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_TuXiBtnByName.lua.lua
**Functions:**
- GetFormation_TuXiBtnUis
**Requires:**
- Formation_BgAniByName
**Snippet:**
```lua
require("Formation_BgAniByName")

function GetFormation_TuXiBtnUis(ui)
  local uis = {}
  uis.BgAni = GetFormation_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_UseBtnByName.lua.lua
**Functions:**
- GetFormation_UseBtnUis
**Snippet:**
```lua
function GetFormation_UseBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Formation_UseTipsByName.lua.lua
**Functions:**
- GetFormation_UseTipsUis
**Snippet:**
```lua
function GetFormation_UseTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/FriendData.lua.lua
**Functions:**
- FriendData.InitFriendData
- FriendData.SaveAllDefenseFormation
- FriendData.GetDefenseFormation
- FriendData.UpdateRelationInfo
- FriendData.GetRelationState
- FriendData.UpdateTarget
- FriendData.DeleteApplication
- FriendData.GetActorMirrorByUid
- FriendData.SaveFriends
- FriendData.GetRelationList
- FriendData.GetCurSearchResult
- FriendData.SaveSearchResult
- FriendData.DeleteSearchResult
- FriendData.GetFriendMaxNumber
- FriendData.GetAppliedMaxNumber
- FriendData.GetBlockMaxNumber
- FriendData.IsActorBlock
- FriendData.ClearBattleRecord
- FriendData.CacheBattleRecord
- FriendData.GetBattleRecord
- FriendData.SaveChallengeStageRsp
- FriendData.GetChallengeStageRsp
**Snippet:**
```lua
FriendData = {}
local cachedBattleRecord = {}

function FriendData.InitFriendData()
  FriendData.init = false
  FriendData.cachedRelationInfoList = {}
  FriendData.cachedUid2Target = {}
  FriendData.cachedTargetUin2State = {}
  FriendData.cachedSearchResult = nil
  FriendData.defenseFormation = nil
```

---

## EF/FriendMgr.lua.lua
**Functions:**
- FriendMgr.TryToOpenFriendWindow
- FriendMgr.OpenActorInfo
**Snippet:**
```lua
FriendMgr = {}

function FriendMgr.TryToOpenFriendWindow(jump)
  if EnterClampUtil.WhetherToEnter(FEATURE_ENUM.HOME_FRIEND) then
    if jump then
      JumpToWindow(WinResConfig.FriendWindow.name, nil, nil, function()
        if FriendData.init == true then
          UIMgr:SendWindowMessage(WinResConfig.FriendWindow.name, WindowMsgEnum.FRIEND.UPDATE_FRIEND_WINDOW)
        else
          FriendService.GetFriendsReq()
```

---

## EF/FriendScriptList.lua.lua
**Requires:**
- FriendMgr
- FriendData
- FriendService
**Snippet:**
```lua
local require = require
require("FriendMgr")
require("FriendData")
require("FriendService")
```

---

## EF/FriendService.lua.lua
**Functions:**
- FriendService.Init
- FriendService.GetFriendsReq
- FriendService.DealGetFriendsRsp
- FriendService.ApplyAddFriendReq
- FriendService.DealApplyAddFriendRsp
- FriendService.AgreeFriendApplyReq
- FriendService.DealAgreeFriendApplyRsp
- FriendService.DisagreeFriendReq
- FriendService.DealDisagreeFriendRsp
- FriendService.BlockTargetReq
- FriendService.DealBlockTargetRsp
- FriendService.DeleteRelationReq
- FriendService.DealDeleteRelationRsp
- FriendService.SearchTargetReq
- FriendService.DealSearchTargetRsp
- FriendService.SetRelationRemarkReq
- FriendService.DealSetRelationRemarkRsp
- FriendService.GetFriendFightRecordReq
- FriendService.DealGetFriendFightRecordRsp
**Snippet:**
```lua
FriendService = {}

function FriendService.Init()
  Net.AddListener(Proto.MsgName.GetFriendsRsp, FriendService.DealGetFriendsRsp)
  Net.AddListener(Proto.MsgName.ApplyAddFriendRsp, FriendService.DealApplyAddFriendRsp)
  Net.AddListener(Proto.MsgName.AgreeFriendApplyRsp, FriendService.DealAgreeFriendApplyRsp)
  Net.AddListener(Proto.MsgName.DisagreeFriendRsp, FriendService.DealDisagreeFriendRsp)
  Net.AddListener(Proto.MsgName.BlockTargetRsp, FriendService.DealBlockTargetRsp)
  Net.AddListener(Proto.MsgName.DeleteRelationRsp, FriendService.DealDeleteRelationRsp)
  Net.AddListener(Proto.MsgName.SearchTargetRsp, FriendService.DealSearchTargetRsp)
```

---

## EF/FriendWindow.lua.lua
**Functions:**
- FriendWindow.ReInitData
- FriendWindow.OnInit
- FriendWindow.UpdateInfo
- FriendWindow.FormatRemainTime
- FriendWindow.RenderChallengeRecord
- FriendWindow.RenderFriend
- FriendWindow.UpdateFriendShowControl
- FriendWindow.UpdateTab
- FriendWindow.SetCurRelationInfoList
- FriendWindow.UpdateWord
- FriendWindow.UpdateFriendList
- FriendWindow.UpdateFriendNum
- FriendWindow.UpdateBlockNum
- FriendWindow.InitBtn
- FriendWindow.UpdateDeleteBtnState
- FriendWindow.ClickSearchBtn
- FriendWindow.ClickAgreeBtn
- FriendWindow.ClickRefuseBtn
- FriendWindow.ClickDefenseBtn
- FriendWindow.ClickDeleteBtn
- FriendWindow.ClearSearchText
- FriendWindow.RefreshListAnim
- FriendWindow.OnShown
- FriendWindow.OnHide
- FriendWindow.OnClose
- FriendWindow.HandleMessage
**Requires:**
- Friend_FriendWindowByName
**Snippet:**
```lua
require("Friend_FriendWindowByName")
local FriendWindow = {}
local uis, contentPane
FRIEND_WINDOW_TAB = {
  FRIEND = 1,
  APPLICANT = 2,
  BLOCK = 3,
  CHALLENGE = 4
}
local FRIEND_LIST_TYPE = {
```

---

## EF/Friend_AddBtnByName.lua.lua
**Functions:**
- GetFriend_AddBtnUis
**Snippet:**
```lua
function GetFriend_AddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Friend_AgreeBtnByName.lua.lua
**Functions:**
- GetFriend_AgreeBtnUis
**Snippet:**
```lua
function GetFriend_AgreeBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Friend_BattleDEFBtnByName.lua.lua
**Functions:**
- GetFriend_BattleDEFBtnUis
**Snippet:**
```lua
function GetFriend_BattleDEFBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Friend_DataBtnByName.lua.lua
**Functions:**
- GetFriend_DataBtnUis
**Snippet:**
```lua
function GetFriend_DataBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Friend_DelBtnByName.lua.lua
**Functions:**
- GetFriend_DelBtnUis
**Snippet:**
```lua
function GetFriend_DelBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Friend_DelNumberBtnByName.lua.lua
**Functions:**
- GetFriend_DelNumberBtnUis
**Snippet:**
```lua
function GetFriend_DelNumberBtnUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Friend_EmptyByName.lua.lua
**Functions:**
- GetFriend_EmptyUis
**Snippet:**
```lua
function GetFriend_EmptyUis(ui)
  local uis = {}
  
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Friend_FriendBattleTipsAniByName.lua.lua
**Functions:**
- GetFriend_FriendBattleTipsAniUis
**Requires:**
- Friend_FriendBattleTipsByName
**Snippet:**
```lua
require("Friend_FriendBattleTipsByName")

function GetFriend_FriendBattleTipsAniUis(ui)
  local uis = {}
  uis.FriendInfo = GetFriend_FriendBattleTipsUis(ui:GetChild("FriendInfo"))
  uis.root = ui
  return uis
end
```

---

## EF/Friend_FriendBattleTipsByName.lua.lua
**Functions:**
- GetFriend_FriendBattleTipsUis
**Requires:**
- CommonResource_HeadByName
**Snippet:**
```lua
require("CommonResource_HeadByName")

function GetFriend_FriendBattleTipsUis(ui)
  local uis = {}
  uis.Head = GetCommonResource_HeadUis(ui:GetChild("Head"))
  uis.GuildTxt = ui:GetChild("GuildTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.ResultTxt = ui:GetChild("ResultTxt")
```

---

## EF/Friend_FriendByName.lua.lua
**Functions:**
- GetFriend_FriendUis
**Requires:**
- CommonResource_BackGroundByName
- Friend_TabRegionByName
- Friend_EmptyByName
- Friend_SearchByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Friend_TabRegionByName")
require("Friend_EmptyByName")
require("Friend_SearchByName")
require("CommonResource_CurrencyReturnByName")

function GetFriend_FriendUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TabRegion = GetFriend_TabRegionUis(ui:GetChild("TabRegion"))
```

---

## EF/Friend_FriendInfoAniByName.lua.lua
**Functions:**
- GetFriend_FriendInfoAniUis
**Requires:**
- Friend_FriendInfoByName
**Snippet:**
```lua
require("Friend_FriendInfoByName")

function GetFriend_FriendInfoAniUis(ui)
  local uis = {}
  uis.FriendInfo = GetFriend_FriendInfoUis(ui:GetChild("FriendInfo"))
  uis.root = ui
  return uis
end
```

---

## EF/Friend_FriendInfoByName.lua.lua
**Functions:**
- GetFriend_FriendInfoUis
**Requires:**
- CommonResource_HeadByName
- Friend_OnLineByName
- Friend_LapseByName
**Snippet:**
```lua
require("CommonResource_HeadByName")
require("Friend_OnLineByName")
require("Friend_LapseByName")

function GetFriend_FriendInfoUis(ui)
  local uis = {}
  uis.Head = GetCommonResource_HeadUis(ui:GetChild("Head"))
  uis.GuildTxt = ui:GetChild("GuildTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TaggingTxt = ui:GetChild("TaggingTxt")
```

---

## EF/Friend_FriendWindowByName.lua.lua
**Functions:**
- GetFriend_FriendWindowUis
**Requires:**
- Friend_FriendByName
**Snippet:**
```lua
require("Friend_FriendByName")

function GetFriend_FriendWindowUis(ui)
  local uis = {}
  uis.Main = GetFriend_FriendUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/Friend_HeadByName.lua.lua
**Functions:**
- GetFriend_HeadUis
**Snippet:**
```lua
function GetFriend_HeadUis(ui)
  local uis = {}
  
  uis.HeadLoader = ui:GetChild("HeadLoader")
  uis.root = ui
  return uis
end
```

---

## EF/Friend_LapseByName.lua.lua
**Functions:**
- GetFriend_LapseUis
**Snippet:**
```lua
function GetFriend_LapseUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/Friend_ListTabBgByName.lua.lua
**Functions:**
- GetFriend_ListTabBgUis
**Snippet:**
```lua
function GetFriend_ListTabBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## EF/Friend_ListTabBtnByName.lua.lua
**Functions:**
- GetFriend_ListTabBtnUis
**Requires:**
- Friend_ListTabBgByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("Friend_ListTabBgByName")
require("CommonResource_RedDotByName")

function GetFriend_ListTabBtnUis(ui)
  local uis = {}
  uis.ListTabBg = GetFriend_ListTabBgUis(ui:GetChild("ListTabBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
```

---

## EF/Friend_OnLineByName.lua.lua
**Functions:**
- GetFriend_OnLineUis
**Snippet:**
```lua
function GetFriend_OnLineUis(ui)
  local uis = {}
  
  uis.OnLineTxt = ui:GetChild("OnLineTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## EF/Friend_PlayBackBtnByName.lua.lua
**Functions:**
- GetFriend_PlayBackBtnUis
**Snippet:**
```lua
function GetFriend_PlayBackBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Friend_RefuseBtnByName.lua.lua
**Functions:**
- GetFriend_RefuseBtnUis
**Snippet:**
```lua
function GetFriend_RefuseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Friend_SearchBtnByName.lua.lua
**Functions:**
- GetFriend_SearchBtnUis
**Snippet:**
```lua
function GetFriend_SearchBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/Friend_SearchByName.lua.lua
**Functions:**
- GetFriend_SearchUis
**Snippet:**
```lua
function GetFriend_SearchUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SearchBtn = ui:GetChild("SearchBtn")
  uis.root = ui
  return uis
end
```

---

## EF/Friend_TabRegionByName.lua.lua
**Functions:**
- GetFriend_TabRegionUis
**Snippet:**
```lua
function GetFriend_TabRegionUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## EF/Friend_TimeAxisBtnByName.lua.lua
**Functions:**
- GetFriend_TimeAxisBtnUis
**Snippet:**
```lua
function GetFriend_TimeAxisBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## EF/FrostDungeonData.lua.lua
**Snippet:**
```lua
local dungeonInfo
local ChallengeComparer = function(x, y)
  return x.id < y.id
end
local SetLevelTargetList = function(item)
  if item and item.targets and not item.targets_list then
    local map = item.targets
    local list = {}
    local stageId = item.stageId
    local conf = TableData.GetConfig(stageId, "BaseStage")
```

---

## EF/FrostDungeonDetailsWindow.lua.lua
**Functions:**
- wordList.itemRenderer
- wordList.itemRenderer
- wordList.itemRenderer
- FrostDungeonDetailsWindow.ReInitData
- FrostDungeonDetailsWindow.OnInit
- FrostDungeonDetailsWindow.UpdateInfo
- recommendBufflist.itemRenderer
- recommendCardlist.itemRenderer
- bufflist.itemProvider
- FrostDungeonDetailsWindow.InitBtn
- FrostDungeonDetailsWindow.OnClose
**Requires:**
- SuperDungeon_PlayDetailsWindowByName
**Snippet:**
```lua
require("SuperDungeon_PlayDetailsWindowByName")
local FrostDungeonDetailsWindow = {}
local uis, contentPane, stageId, stageBuffList, selectedBuffs
local BuffItemRenderer = function(i, gcmp)
  local buffName, buffDesc
  local info = FrostDungeonData.GetFrostDungeonInfo()
  local index = table.keyof(info.stages, stageId, "stageId")
  local item = info.stages[index]
  local buffNumberDesc = ""
  local loader = gcmp:GetChild("PicLoader")
```

---

## EF/FrostDungeonMgr.lua.lua
**Snippet:**
```lua
local GetLevelIndex = function(stageId)
  local list = FrostDungeonData.GetLevelList()
  if list then
    local i = table.keyof(list, stageId)
    return i
  end
  return 0
end
local IsLevelUnlock = function(stageId)
  local info = FrostDungeonData.GetFrostDungeonInfo()
```

---

## EF/FrostDungeonRewardWindow.lua.lua
**Functions:**
- specialItemlist.itemRenderer
- itemlist.itemRenderer
- FrostDungeonRewardWindow.ReInitData
- FrostDungeonRewardWindow.OnInit
- FrostDungeonRewardWindow.UpdateInfo
- FrostDungeonRewardWindow.InitBtn
- FrostDungeonRewardWindow.OnClose
- FrostDungeonRewardWindow.HandleMessage
**Requires:**
- SuperDungeon_RewardGetWindowByName
**Snippet:**
```lua
require("SuperDungeon_RewardGetWindowByName")
local FrostDungeonRewardWindow = {}
local uis, contentPane, selectedStageId, challenges
local RefreshRewardItems = function(selectedLevelIndex)
  local info = FrostDungeonData.GetFrostDungeonInfo()
  local chapterConf = TableData.GetConfig(info.chapterId, "BaseChapter")
  local stageId = chapterConf.stages[selectedLevelIndex + 1]
  local conf = TableData.GetConfig(stageId, "BaseStage")
  selectedStageId = stageId
  challenges = FrostDungeonData.GetLevelChallenges(selectedStageId)
```

---

## EF/FrostDungeonScriptList.lua.lua
**Requires:**
- FrostDungeonMgr
- FrostDungeonData
- FrostDungeonService
**Snippet:**
```lua
FrostDungeonMgr = require("FrostDungeonMgr")
FrostDungeonData = require("FrostDungeonData")
FrostDungeonService = require("FrostDungeonService")
```

---

## EF/FrostDungeonService.lua.lua
**Snippet:**
```lua
local GetFrostDungeonInfoReq = function(rspCallback)
  Net.Send(Proto.MsgName.BuffStageGetInfoReq, nil, rspCallback)
end
local GetFrostDungeonInfoRsp = function(msg)
  FrostDungeonData.SetFrostDungeonInfo(msg)
  UIMgr:SendWindowMessage(WinResConfig.FrostDungeonWindow.name, WindowMsgEnum.FrostDungeonWindow.REFRESH_PANEL_INFO)
end
local get_reward_msg = {}
local GetFrostDungeonRewardReq = function(stageId, rewardId, rspCallback)
  get_reward_msg.rewardStage = stageId
```

---

## EF/FrostDungeonWindow.lua.lua
**Functions:**
- starlist.itemRenderer
- FrostDungeonWindow.ReInitData
- FrostDungeonWindow.OnInit
- FrostDungeonWindow.UpdateInfo
- FrostDungeonWindow.InitBtn
- FrostDungeonWindow.OnShown
- FrostDungeonWindow.OnClose
- FrostDungeonWindow.HandleMessage
**Requires:**
- SuperDungeon_SuperWindowByName
**Snippet:**
```lua
require("SuperDungeon_SuperWindowByName")
local FrostDungeonWindow = {}
local uis, contentPane, bgEffect
local STAGE_EFFECT_LOOKUP = {
  [1] = "icon1_Columns",
  [2] = "icon2_Columns",
  [3] = "icon3_Columns",
  [4] = "icon4_Columns",
  [5] = "icon5_boss"
}
```

---

## EF/FunctionOpen_FunctionByName.lua.lua
**Functions:**
- GetFunctionOpen_FunctionUis
**Requires:**
- FunctionOpen_PopupBgByName
- FunctionOpen_LineRightByName
- FunctionOpen_LineLeftByName
- FunctionOpen_LockWordByName
**Snippet:**
```lua
require("FunctionOpen_PopupBgByName")
require("FunctionOpen_LineRightByName")
require("FunctionOpen_LineLeftByName")
require("FunctionOpen_LockWordByName")

function GetFunctionOpen_FunctionUis(ui)
  local uis = {}
  uis.PopupBg = GetFunctionOpen_PopupBgUis(ui:GetChild("PopupBg"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.PicLoader = ui:GetChild("PicLoader")
```

---

## EF/FunctionOpen_FunctionWindowByName.lua.lua
**Functions:**
- GetFunctionOpen_FunctionWindowUis
**Requires:**
- FunctionOpen_FunctionByName
**Snippet:**
```lua
require("FunctionOpen_FunctionByName")

function GetFunctionOpen_FunctionWindowUis(ui)
  local uis = {}
  uis.Main = GetFunctionOpen_FunctionUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## EF/FunctionOpen_LineLeftByName.lua.lua
**Functions:**
- GetFunctionOpen_LineLeftUis
**Snippet:**
```lua
function GetFunctionOpen_LineLeftUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## EF/FunctionOpen_LineRightByName.lua.lua
**Functions:**
- GetFunctionOpen_LineRightUis
**Snippet:**
```lua
function GetFunctionOpen_LineRightUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## EF/FunctionOpen_LockWordByName.lua.lua
**Functions:**
- GetFunctionOpen_LockWordUis
**Snippet:**
```lua
function GetFunctionOpen_LockWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## EF/FunctionOpen_PopupBgByName.lua.lua
**Functions:**
- GetFunctionOpen_PopupBgUis
**Snippet:**
```lua
function GetFunctionOpen_PopupBgUis(ui)
  local uis = {}
  
  uis.BlurLoader = ui:GetChild("BlurLoader")
  uis.root = ui
  return uis
end
```

---

## EF/FunctionQueueUtil.lua.lua
**Functions:**
- FunctionQueueUtil.Add
- FunctionQueueUtil.Remove
- FunctionQueueUtil.SetFunEnd
- FunctionQueueUtil.Update
- FunctionQueueUtil.CheckHomeIsEnd
- FunctionQueueUtil.Start
- FunctionQueueUtil.Stop
**Snippet:**
```lua
local FunctionQueueUtil = {}
local funTb = {}
local start = false
local curFun
local Sort = function()
  if #funTb > 1 then
    table.sort(funTb, function(a, b)
      return a.weight < b.weight
    end)
  end
```

---

## EF/FunctionWindow.lua.lua
**Functions:**
- FunctionWindow.ReInitData
- FunctionWindow.OnInit
- FunctionWindow.UpdateInfo
- FunctionWindow.InitBtn
- FunctionWindow.OnClose
**Requires:**
- FunctionOpen_FunctionWindowByName
**Snippet:**
```lua
require("FunctionOpen_FunctionWindowByName")
local FunctionWindow = {}
local uis, contentPane, closeCallBack, lockedId, index

function FunctionWindow.ReInitData()
end

function FunctionWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.FunctionWindow.package, WinResConfig.FunctionWindow.comName, function(com)
    contentPane = com
```

---
