# GL

## GL/GetItemTips.lua.lua
**Functions:**
- GetItemTips.Show
- GetItemTips.GetCardChangeItem
**Snippet:**
```lua
local GetItemTips = {}

function GetItemTips.Show(reward, notSort, closeCallback)
  local cardTb = {}
  local itemTb = {}
  local fashionId = {}
  local type
  for _, v in pairs(reward) do
    type = v.item and v.item.tupleType or v.tupleType
    if type == ProtoEnum.TUPLE_TYPE.ITEM or type == ProtoEnum.TUPLE_TYPE.BADGE or type == ProtoEnum.TUPLE_TYPE.BGM then
```

---

## GL/GetItemTipsWindow.lua.lua
**Functions:**
- GetItemTipsWindow.ReInitData
- GetItemTipsWindow.OnInit
- GetItemTipsWindow.OnShowAnimationEnd
- GetItemTipsWindow.OnPreClose
- GetItemTipsWindow.SortByBaseItem
- GetItemTipsWindow.InitList
- GetItemTipsWindow.UpdateTextDisplay
- GetItemTipsWindow.CloseWindow
- GetItemTipsWindow.InitBtn
- GetItemTipsWindow.OnClose
**Requires:**
- ItemGetShow_GetItemTipsWindowByName
**Snippet:**
```lua
require("ItemGetShow_GetItemTipsWindowByName")
local GetItemTipsWindow = {}
local uis, contentPane, msg
local pitchOn = true
local notSort = true
local closeCallback

function GetItemTipsWindow.ReInitData()
end

```

---

## GL/GlobalConfig.lua.lua
**Functions:**
- GameConfig.SetScreenRatio
- GameConfig.GetScreenRatio
**Snippet:**
```lua
GameConfig = {screenRatio = 10000}

function GameConfig.SetScreenRatio(ratio)
  GameConfig.screenRatio = ratio
end

function GameConfig.GetScreenRatio()
  return GameConfig.screenRatio
end
```

---

## GL/GlobalConst.lua.lua
**Snippet:**
```lua
COMPARE_TYPE = {
  GREATER = 1,
  EQUAL = 2,
  LESS = 3,
  LESS_EQUAL = 4,
  GREATER_EQUAL = 5,
  NOT_EQUAL = 6
}
COMMON_ITEM_ID = {
  GAME_COIN = 21000003,
```

---

## GL/GMCommand_GMByName.lua.lua
**Functions:**
- GetGMCommand_GMUis
**Snippet:**
```lua
function GetGMCommand_GMUis(ui)
  local uis = {}
  
  uis.Title1Txt = ui:GetChild("Title1Txt")
  uis.Subtitle1Txt = ui:GetChild("Subtitle1Txt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SureBtn = ui:GetChild("SureBtn")
  uis.Title2Txt = ui:GetChild("Title2Txt")
  uis.Subtitle2Txt = ui:GetChild("Subtitle2Txt")
  uis.OtherList = ui:GetChild("OtherList")
```

---

## GL/GMCommand_SureBtnByName.lua.lua
**Functions:**
- GetGMCommand_SureBtnUis
**Snippet:**
```lua
function GetGMCommand_SureBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GMPopup.lua.lua
**Functions:**
- GMPopup.ReInitData
- GMPopup.OnInit
- GMPopup.UpdateInfo
- GMPopup.ClickBattleTest
- GMPopup.ActorGmReq
- GMPopup.InitBtn
- GMPopup.OnShown
- GMPopup.OnHide
- GMPopup.OnClose
- GMPopup.HandleMessage
**Requires:**
- GMCommand_GMByName
- BattleTestBalance
- BattleDataTest
**Snippet:**
```lua
require("GMCommand_GMByName")
local GMPopup = {}
local uis, contentPane

function GMPopup.ReInitData()
end

function GMPopup.OnInit(bridgeObj)
  bridgeObj:SetView(WinResConfig.GMPopup.package, WinResConfig.GMPopup.comName, function(com)
    contentPane = com
```

---

## GL/GuideBoardWindow.lua.lua
**Functions:**
- GuideBoardWindow.ReInitData
- GuideBoardWindow.OnInit
- GuideBoardWindow.UpdateInfo
- list.itemRenderer
- GuideBoardWindow.InitBtn
- GuideBoardWindow.OnClose
**Requires:**
- Abyss_GuideBoardWindowByName
**Snippet:**
```lua
require("Abyss_GuideBoardWindowByName")
local GuideBoardWindow = {}
local uis, contentPane, eventInfo

function GuideBoardWindow.ReInitData()
end

function GuideBoardWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.GuideBoardWindow.package, WinResConfig.GuideBoardWindow.comName, function(com)
    contentPane = com
```

---

## GL/GuideData.lua.lua
**Functions:**
- GuideData.GuideIsEnd
- GuideData.GuideIsTrigger
- GuideData.GetLastKey
- GuideData.GetGuideIdByWindowId
- GuideData.InitCaptionOpenData
- GuideData.SaveCaptionOpen
- GuideData.CanShowCaption
- GuideData.ClearData
**Snippet:**
```lua
GuideData = {}
GUIDE_STEP_TYPE_ENUM = {
  HIDE_GUIDE_WINDOW = 0,
  NORMAL = 1,
  SHOW_TIPS = 2,
  SKILL_HINT = 3,
  GIRD = 4,
  NOT_CHANGE_LAYER = 5,
  LV_BACK = 6,
  PLOT_STAGE = 7,
```

---

## GL/GuideMgr.lua.lua
**Functions:**
- GuideMgr.SaveStageID
- GuideMgr.Log
- GuideMgr.ClearData
- GuideMgr.Init
- GuideMgr.CheckReconnection
- GuideMgr.InitGuideInfo
- GuideMgr.DealKeyStepComplete
- GuideMgr.InitData
- GuideMgr.Refresh
- GuideMgr.AddIndex
- GuideMgr.AfterShownFunc
- GuideMgr.PlayGuideCaption
- GuideMgr.GetProcessDataById
- GuideMgr.GetNextStepData
- GuideMgr.SetStepData
- GuideMgr.GetStepData
- GuideMgr.IsGuideEnd
- GuideMgr.IsTrigger
- GuideMgr.IsBossWindow
- GuideMgr.CheckIsTriggerGuide
- GuideMgr.CheckJumpGuide
- GuideMgr.NeedShowSpecialGuide
- GuideMgr.NeedShowBattleSettingBtn
- GuideMgr.PlayGuideProcess
- GuideMgr.PlayGuide
- BattleMgr.beforeBattleCallback
- BattleMgr.beforeBattleCallback
- GuideMgr.SafeOpenGuideWindow
- GuideMgr.PlayStep
- GuideMgr.RemoveProcessDataById
- GuideMgr.TestListenCompleteFunc
- GuideMgr.Next
- GuideMgr.SaveGuideProgress
- GuideMgr.FindComponent
- GuideMgr.FindComponentByPath
- GuideMgr.FindChildByName
- GuideMgr.InitUiRoot
- GuideMgr.IsStageComplete
- GuideMgr.IsBurstEnergyFull
- GuideMgr.IsBurstActive
- GuideMgr.IsCtrlCreated
- GuideMgr.BurstChooseCardCount
- GuideMgr.IsCtrlCanTouch
- GuideMgr.IsCardLvUp
- GuideMgr.CardLvIsEqual
- GuideMgr.IsWindowOpen
- GuideMgr.OpenFormationWindow
- GuideMgr.OpenPlotDungeonWindow
- GuideMgr.IsInRaidBoss
- GuideMgr.GuidePlayEnd
- GuideMgr.QuitPictureOrStory
- GuideMgr.HideWindow
- GuideMgr.CloseWindow
**Snippet:**
```lua
GuideMgr = {
  jumpNewHand = false,
  curTriggerId = 0,
  curStepId = 0,
  curStepIndex = 1,
  curGroupStepIndex = 0,
  curGuideIsPlay = false,
  curTriggerWindowName = "",
  delayWin = nil,
  guideBol = false
```

---

## GL/GuidePicLookWindow.lua.lua
**Functions:**
- GuidePicLookWindow.OnInit
- GuidePicLookWindow.ShowEffEct
- GuidePicLookWindow.DestroyEffect
- GuidePicLookWindow.Update
- GuidePicLookWindow.InitPicture
- uis.Main.PicList.itemRenderer
- GuidePicLookWindow.SetPageShow
- uis.Main.PageNumberList.itemRenderer
- GuidePicLookWindow.HandleMessage
- GuidePicLookWindow.OnClose
**Requires:**
- Guide_PicLookWindowByName
**Snippet:**
```lua
require("Guide_PicLookWindowByName")
local GuidePicLookWindow = {}
local uis, contentPane, pictureData, listPage, closeCallback, captionId, showCloseBtn
local effect = "Assets/Art/Effects/Prefab/UI_prefab/NewGuyFinger/FX_NewGuy_Finger_pointlight.prefab"
local time = 0
local startTime, tempItem, lastCtr, itemEffect

function GuidePicLookWindow.OnInit(bridgeObj)
  bridgeObj:SetView(WinResConfig.GuidePicLookWindow.package, WinResConfig.GuidePicLookWindow.comName, function(com)
    contentPane = com
```

---

## GL/GuideScriptList.lua.lua
**Requires:**
- GuideData
- GuideMgr
**Snippet:**
```lua
local require = require
require("GuideData")
require("GuideMgr")
```

---

## GL/GuideWindow.lua.lua
**Functions:**
- GuideWindow.OnInit
- GuideWindow.Init
- GuideWindow.CreateSpecialCom
- GuideWindow.CreateSpecialEffect
- GuideWindow.Clear
- GuideWindow.InitStep
- GuideWindow.SetMaskInfo
- GuideWindow.SetLevelUpDelayed
- GuideWindow.GetScreenOffset
- GuideWindow.SetClickCtrPos
- GuideWindow.ClickCtrOnClick
- GuideWindow.OnShown
- GuideWindow.QuitStep
- GuideWindow.HandleMessage
- GuideWindow.OnClose
**Requires:**
- Guide_GuideWindowByName
**Snippet:**
```lua
require("Guide_GuideWindowByName")
local GuideWindow = {}
local uis, contentPane, stepData, clickCtr, lastParent, lastXy, lastPos, lastIndex
local mask = "Assets/Art/Models/UI_spine/prefab/FX_NewGuy_Finger_mask.prefab"
local effectPath = "Assets/Art/Models/UI_spine/prefab/FX_NewGuy_Finger.prefab"
local effectObj, maskPlaneTransform, spineRoot, initedStepId, outAnimWait, startAnimWait

function GuideWindow.OnInit(bridgeObj)
  bridgeObj:SetView(WinResConfig.GuideWindow.package, WinResConfig.GuideWindow.comName, function(com)
    contentPane = com
```

---

## GL/Guide_Arena_001ByName.lua.lua
**Functions:**
- GetGuide_Arena_001Uis
**Snippet:**
```lua
function GetGuide_Arena_001Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Guide_Arena_002ByName.lua.lua
**Functions:**
- GetGuide_Arena_002Uis
**Snippet:**
```lua
function GetGuide_Arena_002Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Guide_CloseBtnByName.lua.lua
**Functions:**
- GetGuide_CloseBtnUis
**Snippet:**
```lua
function GetGuide_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Guide_ExplainByName.lua.lua
**Functions:**
- GetGuide_ExplainUis
**Snippet:**
```lua
function GetGuide_ExplainUis(ui)
  local uis = {}
  
  uis.ExplainLoader = ui:GetChild("ExplainLoader")
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.root = ui
  return uis
end
```

---

## GL/Guide_FrameByName.lua.lua
**Functions:**
- GetGuide_FrameUis
**Snippet:**
```lua
function GetGuide_FrameUis(ui)
  local uis = {}
  
  uis.EffectLoader = ui:GetChild("EffectLoader")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## GL/Guide_GuideByName.lua.lua
**Functions:**
- GetGuide_GuideUis
**Requires:**
- Guide_PointerByName
- Guide_WordByName
- Guide_FrameByName
**Snippet:**
```lua
require("Guide_PointerByName")
require("Guide_WordByName")
require("Guide_FrameByName")

function GetGuide_GuideUis(ui)
  local uis = {}
  uis.Mask = GetGuide_PointerUis(ui:GetChild("Mask"))
  uis.Pointer = GetGuide_PointerUis(ui:GetChild("Pointer"))
  uis.Word = GetGuide_WordUis(ui:GetChild("Word"))
  uis.Frame = GetGuide_FrameUis(ui:GetChild("Frame"))
```

---

## GL/Guide_GuideMergeByName.lua.lua
**Functions:**
- GetGuide_GuideMergeUis
**Requires:**
- Guide_GuideByName
- Guide_ExplainByName
**Snippet:**
```lua
require("Guide_GuideByName")
require("Guide_ExplainByName")

function GetGuide_GuideMergeUis(ui)
  local uis = {}
  uis.Guide = GetGuide_GuideUis(ui:GetChild("Guide"))
  uis.Eeplain = GetGuide_ExplainUis(ui:GetChild("Eeplain"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## GL/Guide_GuideWindowByName.lua.lua
**Functions:**
- GetGuide_GuideWindowUis
**Requires:**
- Guide_GuideMergeByName
**Snippet:**
```lua
require("Guide_GuideMergeByName")

function GetGuide_GuideWindowUis(ui)
  local uis = {}
  uis.Main = GetGuide_GuideMergeUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/Guide_LeftBtnByName.lua.lua
**Functions:**
- GetGuide_LeftBtnUis
**Snippet:**
```lua
function GetGuide_LeftBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Guide_PageByName.lua.lua
**Functions:**
- GetGuide_PageUis
**Snippet:**
```lua
function GetGuide_PageUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/Guide_PicByName.lua.lua
**Functions:**
- GetGuide_PicUis
**Snippet:**
```lua
function GetGuide_PicUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.LeftBtn = ui:GetChild("LeftBtn")
  uis.RightBtn = ui:GetChild("RightBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/Guide_PicLookByName.lua.lua
**Functions:**
- GetGuide_PicLookUis
**Snippet:**
```lua
function GetGuide_PicLookUis(ui)
  local uis = {}
  
  uis.PicList = ui:GetChild("PicList")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.PageNumberList = ui:GetChild("PageNumberList")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/Guide_PicLookWindowByName.lua.lua
**Functions:**
- GetGuide_PicLookWindowUis
**Requires:**
- CommonResource_PopupBgByName
- Guide_PicLookByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Guide_PicLookByName")

function GetGuide_PicLookWindowUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Main = GetGuide_PicLookUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
```

---

## GL/Guide_PointerByName.lua.lua
**Functions:**
- GetGuide_PointerUis
**Snippet:**
```lua
function GetGuide_PointerUis(ui)
  local uis = {}
  
  uis.PointerLoader = ui:GetChild("PointerLoader")
  uis.PointerHolder = ui:GetChild("PointerHolder")
  uis.root = ui
  return uis
end
```

---

## GL/Guide_RightBtnByName.lua.lua
**Functions:**
- GetGuide_RightBtnUis
**Snippet:**
```lua
function GetGuide_RightBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Guide_Special_001ByName.lua.lua
**Functions:**
- GetGuide_Special_001Uis
**Snippet:**
```lua
function GetGuide_Special_001Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Guide_Special_002ByName.lua.lua
**Functions:**
- GetGuide_Special_002Uis
**Snippet:**
```lua
function GetGuide_Special_002Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Guide_Special_003ByName.lua.lua
**Functions:**
- GetGuide_Special_003Uis
**Snippet:**
```lua
function GetGuide_Special_003Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Guide_WordByName.lua.lua
**Functions:**
- GetGuide_WordUis
**Snippet:**
```lua
function GetGuide_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBattleRecordWindow.lua.lua
**Functions:**
- GuildBattleRecordWindow.ReInitData
- GuildBattleRecordWindow.OnInit
- GuildBattleRecordWindow.UpdateInfo
- list.itemRenderer
- GuildBattleRecordWindow.InitBtn
- GuildBattleRecordWindow.OnClose
**Requires:**
- GuildBoss_GuildBattleRecordWindowByName
**Snippet:**
```lua
require("GuildBoss_GuildBattleRecordWindowByName")
local GuildBattleRecordWindow = {}
local uis, contentPane

function GuildBattleRecordWindow.ReInitData()
end

function GuildBattleRecordWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.GuildBattleRecordWindow.package, WinResConfig.GuildBattleRecordWindow.comName, function(com)
    contentPane = com
```

---

## GL/GuildBossDetailInfoWindow.lua.lua
**Functions:**
- GuildBossDetailInfoWindow.ReInitData
- GuildBossDetailInfoWindow.OnInit
- GuildBossDetailInfoWindow.UpdateInfo
- skilllist.itemRenderer
- wordlist.itemRenderer
- GuildBossDetailInfoWindow.InitBtn
- GuildBossDetailInfoWindow.OnClose
**Requires:**
- GuildBoss_DungeonInfoWindowByName
**Snippet:**
```lua
require("GuildBoss_DungeonInfoWindowByName")
local GuildBossDetailInfoWindow = {}
local uis, contentPane, conf

function GuildBossDetailInfoWindow.ReInitData()
end

function GuildBossDetailInfoWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.GuildBossDetailInfoWindow.package, WinResConfig.GuildBossDetailInfoWindow.comName, function(com)
    contentPane = com
```

---

## GL/GuildBossEndWindow.lua.lua
**Functions:**
- GuildBossEndWindow.ReInitData
- GuildBossEndWindow.OnInit
- GuildBossEndWindow.UpdateInfo
- GuildBossEndWindow.InitBtn
- GuildBossEndWindow.OnClose
**Requires:**
- GuildBoss_BossEndWindowByName
**Snippet:**
```lua
require("GuildBoss_BossEndWindowByName")
local GuildBossEndWindow = {}
local uis, contentPane

function GuildBossEndWindow.ReInitData()
end

function GuildBossEndWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.GuildBossEndWindow.package, WinResConfig.GuildBossEndWindow.comName, function(com)
    contentPane = com
```

---

## GL/GuildBossMainWindow.lua.lua
**Functions:**
- GuildBossMainWindow.ReInitData
- GuildBossMainWindow.OnInit
- GuildBossMainWindow.UpdateInfo
- GuildBossMainWindow.InitBtn
- GuildBossMainWindow.OnClose
**Requires:**
- GuildBoss_GuildBossWindowByName
**Snippet:**
```lua
require("GuildBoss_GuildBossWindowByName")
local GuildBossMainWindow = {}
local uis, contentPane
local RefreshPanelInfo = function()
  local title = uis.Main.Title
  title.NameTxt.text = GuildData.GuildInfo.info.name
  title.NumberTxt.text = GuildData.GuildInfo.info.memberCount
  title.LevelTxt.text = GuildData.GuildInfo.info.level
  local headData = TableData.GetConfig(GuildData.GuildInfo.info.iconId, "BaseGuildHeadIcon")
  if headData then
```

---

## GL/GuildBossPreviewWindow.lua.lua
**Functions:**
- GuildBossPreviewWindow.ReInitData
- GuildBossPreviewWindow.OnInit
- GuildBossPreviewWindow.UpdateInfo
- GuildBossPreviewWindow.InitBtn
- GuildBossPreviewWindow.OnClose
**Requires:**
- GuildBoss_BossPreviewWindowByName
**Snippet:**
```lua
require("GuildBoss_BossPreviewWindowByName")
local GuildBossPreviewWindow = {}
local uis, contentPane

function GuildBossPreviewWindow.ReInitData()
end

function GuildBossPreviewWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.GuildBossPreviewWindow.package, WinResConfig.GuildBossPreviewWindow.comName, function(com)
    contentPane = com
```

---

## GL/GuildBossSelectedWindow.lua.lua
**Functions:**
- list.itemRenderer
- GuildBossSelectedWindow.ReInitData
- GuildBossSelectedWindow.OnInit
- GuildBossSelectedWindow.UpdateInfo
- GuildBossSelectedWindow.InitBtn
- GuildBossSelectedWindow.OnClose
**Requires:**
- GuildBoss_BossBattleWindowByName
**Snippet:**
```lua
require("GuildBoss_BossBattleWindowByName")
local GuildBossSelectedWindow = {}
local uis, contentPane
local RefreshPanelInfo = function()
  local progressInfo = GuildWarData.GetGuildWarProgressInfo()
  local round = progressInfo.round
  uis.Main.Round.WordTxt.text = round
  local list = uis.Main.BossList
  local bossStates = progressInfo.bossStates
  local curStageId = progressInfo.stageId
```

---

## GL/GuildBoss_BossBattleByName.lua.lua
**Functions:**
- GetGuildBoss_BossBattleUis
**Requires:**
- CommonResource_BackGroundByName
- GuildBoss_BossBattleRoundByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("GuildBoss_BossBattleRoundByName")

function GetGuildBoss_BossBattleUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.FunctionDetailsBtn = ui:GetChild("FunctionDetailsBtn")
  uis.BossList = ui:GetChild("BossList")
  uis.Round = GetGuildBoss_BossBattleRoundUis(ui:GetChild("Round"))
```

---

## GL/GuildBoss_BossBattleHpProgressBarByName.lua.lua
**Functions:**
- GetGuildBoss_BossBattleHpProgressBarUis
**Requires:**
- GuildBoss_BossBattleHpProgressFillByName
**Snippet:**
```lua
require("GuildBoss_BossBattleHpProgressFillByName")

function GetGuildBoss_BossBattleHpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetGuildBoss_BossBattleHpProgressFillUis(ui:GetChild("bar"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_BossBattleHpProgressFillByName.lua.lua
**Functions:**
- GetGuildBoss_BossBattleHpProgressFillUis
**Snippet:**
```lua
function GetGuildBoss_BossBattleHpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_BossBattleKillByName.lua.lua
**Functions:**
- GetGuildBoss_BossBattleKillUis
**Snippet:**
```lua
function GetGuildBoss_BossBattleKillUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_BossBattleLockByName.lua.lua
**Functions:**
- GetGuildBoss_BossBattleLockUis
**Snippet:**
```lua
function GetGuildBoss_BossBattleLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_BossBattleNameByName.lua.lua
**Functions:**
- GetGuildBoss_BossBattleNameUis
**Snippet:**
```lua
function GetGuildBoss_BossBattleNameUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_BossBattleRoundByName.lua.lua
**Functions:**
- GetGuildBoss_BossBattleRoundUis
**Snippet:**
```lua
function GetGuildBoss_BossBattleRoundUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_BossBattleTipsAniByName.lua.lua
**Functions:**
- GetGuildBoss_BossBattleTipsAniUis
**Requires:**
- GuildBoss_BossBattleTipsByName
**Snippet:**
```lua
require("GuildBoss_BossBattleTipsByName")

function GetGuildBoss_BossBattleTipsAniUis(ui)
  local uis = {}
  uis.Tips = GetGuildBoss_BossBattleTipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_BossBattleTipsByName.lua.lua
**Functions:**
- GetGuildBoss_BossBattleTipsUis
**Requires:**
- GuildBoss_BossBattleNameByName
- CommonResource_OccupationByName
- GuildBoss_BossBattleLockByName
- GuildBoss_BossBattleKillByName
**Snippet:**
```lua
require("GuildBoss_BossBattleNameByName")
require("CommonResource_OccupationByName")
require("GuildBoss_BossBattleLockByName")
require("GuildBoss_BossBattleKillByName")

function GetGuildBoss_BossBattleTipsUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.Name = GetGuildBoss_BossBattleNameUis(ui:GetChild("Name"))
  uis.HpProgressBar = ui:GetChild("HpProgressBar")
```

---

## GL/GuildBoss_BossBattleWindowByName.lua.lua
**Functions:**
- GetGuildBoss_BossBattleWindowUis
**Requires:**
- GuildBoss_BossBattleByName
**Snippet:**
```lua
require("GuildBoss_BossBattleByName")

function GetGuildBoss_BossBattleWindowUis(ui)
  local uis = {}
  uis.Main = GetGuildBoss_BossBattleUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_BossEndByName.lua.lua
**Functions:**
- GetGuildBoss_BossEndUis
**Requires:**
- CommonResource_BackGroundByName
- GuildBoss_BossEndWordByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("GuildBoss_BossEndWordByName")

function GetGuildBoss_BossEndUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Word = GetGuildBoss_BossEndWordUis(ui:GetChild("Word"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.RankRewardBtn = ui:GetChild("RankRewardBtn")
  uis.SkillBtn = ui:GetChild("SkillBtn")
```

---

## GL/GuildBoss_BossEndHelpBtnByName.lua.lua
**Functions:**
- GetGuildBoss_BossEndHelpBtnUis
**Snippet:**
```lua
function GetGuildBoss_BossEndHelpBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_BossEndRankBtnByName.lua.lua
**Functions:**
- GetGuildBoss_BossEndRankBtnUis
**Snippet:**
```lua
function GetGuildBoss_BossEndRankBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.RankTxt = ui:GetChild("RankTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_BossEndSkillBtnByName.lua.lua
**Functions:**
- GetGuildBoss_BossEndSkillBtnUis
**Snippet:**
```lua
function GetGuildBoss_BossEndSkillBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_BossEndWindowByName.lua.lua
**Functions:**
- GetGuildBoss_BossEndWindowUis
**Requires:**
- GuildBoss_BossEndByName
**Snippet:**
```lua
require("GuildBoss_BossEndByName")

function GetGuildBoss_BossEndWindowUis(ui)
  local uis = {}
  uis.Main = GetGuildBoss_BossEndUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_BossEndWordByName.lua.lua
**Functions:**
- GetGuildBoss_BossEndWordUis
**Snippet:**
```lua
function GetGuildBoss_BossEndWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_BossPreviewByName.lua.lua
**Functions:**
- GetGuildBoss_BossPreviewUis
**Requires:**
- CommonResource_BackGroundByName
- GuildBoss_BossPreviewTimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("GuildBoss_BossPreviewTimeByName")

function GetGuildBoss_BossPreviewUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.Time = GetGuildBoss_BossPreviewTimeUis(ui:GetChild("Time"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
```

---

## GL/GuildBoss_BossPreviewTimeByName.lua.lua
**Functions:**
- GetGuildBoss_BossPreviewTimeUis
**Snippet:**
```lua
function GetGuildBoss_BossPreviewTimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_BossPreviewTitleByName.lua.lua
**Functions:**
- GetGuildBoss_BossPreviewTitleUis
**Snippet:**
```lua
function GetGuildBoss_BossPreviewTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_BossPreviewWindowByName.lua.lua
**Functions:**
- GetGuildBoss_BossPreviewWindowUis
**Requires:**
- GuildBoss_BossPreviewByName
**Snippet:**
```lua
require("GuildBoss_BossPreviewByName")

function GetGuildBoss_BossPreviewWindowUis(ui)
  local uis = {}
  uis.Main = GetGuildBoss_BossPreviewUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_CompensateBattleBtnByName.lua.lua
**Functions:**
- GetGuildBoss_CompensateBattleBtnUis
**Snippet:**
```lua
function GetGuildBoss_CompensateBattleBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_CompensateCardHeadAniByName.lua.lua
**Functions:**
- GetGuildBoss_CompensateCardHeadAniUis
**Snippet:**
```lua
function GetGuildBoss_CompensateCardHeadAniUis(ui)
  local uis = {}
  
  uis.CardHeadBtn = ui:GetChild("CardHeadBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_CompensateCardHeadBgByName.lua.lua
**Functions:**
- GetGuildBoss_CompensateCardHeadBgUis
**Snippet:**
```lua
function GetGuildBoss_CompensateCardHeadBgUis(ui)
  local uis = {}
  
  uis.CardPicLoader = ui:GetChild("CardPicLoader")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_CompensateCardHeadBtnByName.lua.lua
**Functions:**
- GetGuildBoss_CompensateCardHeadBtnUis
**Requires:**
- GuildBoss_CompensateCardHeadBgByName
- CommonResource_OccupationByName
**Snippet:**
```lua
require("GuildBoss_CompensateCardHeadBgByName")
require("CommonResource_OccupationByName")

function GetGuildBoss_CompensateCardHeadBtnUis(ui)
  local uis = {}
  uis.CardPic = GetGuildBoss_CompensateCardHeadBgUis(ui:GetChild("CardPic"))
  uis.ElementList = ui:GetChild("ElementList")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Occupation = GetCommonResource_OccupationUis(ui:GetChild("Occupation"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## GL/GuildBoss_CompensateCloseBtnByName.lua.lua
**Functions:**
- GetGuildBoss_CompensateCloseBtnUis
**Snippet:**
```lua
function GetGuildBoss_CompensateCloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_CompensateLineupBtnByName.lua.lua
**Functions:**
- GetGuildBoss_CompensateLineupBtnUis
**Snippet:**
```lua
function GetGuildBoss_CompensateLineupBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_CompensateLineupByName.lua.lua
**Functions:**
- GetGuildBoss_CompensateLineupUis
**Snippet:**
```lua
function GetGuildBoss_CompensateLineupUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.HeadList = ui:GetChild("HeadList")
  uis.BattleBtn = ui:GetChild("BattleBtn")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_CompensateNumberByName.lua.lua
**Functions:**
- GetGuildBoss_CompensateNumberUis
**Snippet:**
```lua
function GetGuildBoss_CompensateNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_CompensateTipsByName.lua.lua
**Functions:**
- GetGuildBoss_CompensateTipsUis
**Requires:**
- GuildBoss_CompensateTitleByName
- GuildBoss_CompensateNumberByName
- GuildBoss_CompensateZeroNumberByName
**Snippet:**
```lua
require("GuildBoss_CompensateTitleByName")
require("GuildBoss_CompensateNumberByName")
require("GuildBoss_CompensateZeroNumberByName")

function GetGuildBoss_CompensateTipsUis(ui)
  local uis = {}
  uis.Title1 = GetGuildBoss_CompensateTitleUis(ui:GetChild("Title1"))
  uis.LineupList = ui:GetChild("LineupList")
  uis.Title2 = GetGuildBoss_CompensateTitleUis(ui:GetChild("Title2"))
  uis.Number = GetGuildBoss_CompensateNumberUis(ui:GetChild("Number"))
```

---

## GL/GuildBoss_CompensateTitleByName.lua.lua
**Functions:**
- GetGuildBoss_CompensateTitleUis
**Snippet:**
```lua
function GetGuildBoss_CompensateTitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_CompensateZeroNumberByName.lua.lua
**Functions:**
- GetGuildBoss_CompensateZeroNumberUis
**Snippet:**
```lua
function GetGuildBoss_CompensateZeroNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_DungeonInfoBattleNumberByName.lua.lua
**Functions:**
- GetGuildBoss_DungeonInfoBattleNumberUis
**Snippet:**
```lua
function GetGuildBoss_DungeonInfoBattleNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_DungeonInfoBattleStartBtnByName.lua.lua
**Functions:**
- GetGuildBoss_DungeonInfoBattleStartBtnUis
**Snippet:**
```lua
function GetGuildBoss_DungeonInfoBattleStartBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_DungeonInfoByName.lua.lua
**Functions:**
- GetGuildBoss_DungeonInfoUis
**Requires:**
- GuildBoss_DungeonInfoTipsByName
**Snippet:**
```lua
require("GuildBoss_DungeonInfoTipsByName")

function GetGuildBoss_DungeonInfoUis(ui)
  local uis = {}
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.DungeonInfoTips = GetGuildBoss_DungeonInfoTipsUis(ui:GetChild("DungeonInfoTips"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_DungeonInfoExplainTitleByName.lua.lua
**Functions:**
- GetGuildBoss_DungeonInfoExplainTitleUis
**Snippet:**
```lua
function GetGuildBoss_DungeonInfoExplainTitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_DungeonInfoIntegralByName.lua.lua
**Functions:**
- GetGuildBoss_DungeonInfoIntegralUis
**Snippet:**
```lua
function GetGuildBoss_DungeonInfoIntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_DungeonInfoRecommendBtnByName.lua.lua
**Functions:**
- GetGuildBoss_DungeonInfoRecommendBtnUis
**Snippet:**
```lua
function GetGuildBoss_DungeonInfoRecommendBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_DungeonInfoSkillByName.lua.lua
**Functions:**
- GetGuildBoss_DungeonInfoSkillUis
**Snippet:**
```lua
function GetGuildBoss_DungeonInfoSkillUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_DungeonInfoTestBtnByName.lua.lua
**Functions:**
- GetGuildBoss_DungeonInfoTestBtnUis
**Snippet:**
```lua
function GetGuildBoss_DungeonInfoTestBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_DungeonInfoTipsByName.lua.lua
**Functions:**
- GetGuildBoss_DungeonInfoTipsUis
**Requires:**
- GuildBoss_DungeonInfoBattleNumberByName
- GuildBoss_DungeonInfoIntegralByName
- GuildBoss_DungeonInfoExplainTitleByName
**Snippet:**
```lua
require("GuildBoss_DungeonInfoBattleNumberByName")
require("GuildBoss_DungeonInfoIntegralByName")
require("GuildBoss_DungeonInfoExplainTitleByName")

function GetGuildBoss_DungeonInfoTipsUis(ui)
  local uis = {}
  uis.BattleNumber = GetGuildBoss_DungeonInfoBattleNumberUis(ui:GetChild("BattleNumber"))
  uis.Integral = GetGuildBoss_DungeonInfoIntegralUis(ui:GetChild("Integral"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TitleTxt = ui:GetChild("TitleTxt")
```

---

## GL/GuildBoss_DungeonInfoWindowByName.lua.lua
**Functions:**
- GetGuildBoss_DungeonInfoWindowUis
**Requires:**
- GuildBoss_DungeonInfoByName
**Snippet:**
```lua
require("GuildBoss_DungeonInfoByName")

function GetGuildBoss_DungeonInfoWindowUis(ui)
  local uis = {}
  uis.Main = GetGuildBoss_DungeonInfoUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_DungeonInfoWordByName.lua.lua
**Functions:**
- GetGuildBoss_DungeonInfoWordUis
**Snippet:**
```lua
function GetGuildBoss_DungeonInfoWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBattleRecordByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBattleRecordUis
**Requires:**
- CommonResource_BackGroundByName
- GuildBoss_GuildBattleRecordTitleByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("GuildBoss_GuildBattleRecordTitleByName")

function GetGuildBoss_GuildBattleRecordUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.Title = GetGuildBoss_GuildBattleRecordTitleUis(ui:GetChild("Title"))
  uis.RewardTipsList = ui:GetChild("RewardTipsList")
  uis.root = ui
```

---

## GL/GuildBoss_GuildBattleRecordDataBtnByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBattleRecordDataBtnUis
**Snippet:**
```lua
function GetGuildBoss_GuildBattleRecordDataBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBattleRecordHeadBgByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBattleRecordHeadBgUis
**Snippet:**
```lua
function GetGuildBoss_GuildBattleRecordHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBattleRecordHeadByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBattleRecordHeadUis
**Requires:**
- GuildBoss_GuildBattleRecordHeadBgByName
**Snippet:**
```lua
require("GuildBoss_GuildBattleRecordHeadBgByName")

function GetGuildBoss_GuildBattleRecordHeadUis(ui)
  local uis = {}
  uis.Pic = GetGuildBoss_GuildBattleRecordHeadBgUis(ui:GetChild("Pic"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBattleRecordPlayBackBtnByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBattleRecordPlayBackBtnUis
**Snippet:**
```lua
function GetGuildBoss_GuildBattleRecordPlayBackBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBattleRecordTimeAxisBtnByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBattleRecordTimeAxisBtnUis
**Snippet:**
```lua
function GetGuildBoss_GuildBattleRecordTimeAxisBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBattleRecordTipsAniByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBattleRecordTipsAniUis
**Requires:**
- GuildBoss_GuildBattleRecordTipsByName
**Snippet:**
```lua
require("GuildBoss_GuildBattleRecordTipsByName")

function GetGuildBoss_GuildBattleRecordTipsAniUis(ui)
  local uis = {}
  uis.RankTips = GetGuildBoss_GuildBattleRecordTipsUis(ui:GetChild("RankTips"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBattleRecordTipsByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBattleRecordTipsUis
**Requires:**
- GuildBoss_GuildBattleRecordHeadByName
**Snippet:**
```lua
require("GuildBoss_GuildBattleRecordHeadByName")

function GetGuildBoss_GuildBattleRecordTipsUis(ui)
  local uis = {}
  uis.Head = GetGuildBoss_GuildBattleRecordHeadUis(ui:GetChild("Head"))
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.RoundTxt = ui:GetChild("RoundTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.TimeAxisBtn = ui:GetChild("TimeAxisBtn")
```

---

## GL/GuildBoss_GuildBattleRecordTitleByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBattleRecordTitleUis
**Snippet:**
```lua
function GetGuildBoss_GuildBattleRecordTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBattleRecordWindowByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBattleRecordWindowUis
**Requires:**
- GuildBoss_GuildBattleRecordByName
**Snippet:**
```lua
require("GuildBoss_GuildBattleRecordByName")

function GetGuildBoss_GuildBattleRecordWindowUis(ui)
  local uis = {}
  uis.Main = GetGuildBoss_GuildBattleRecordUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBossBadgeBtnByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossBadgeBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetGuildBoss_GuildBossBadgeBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
```

---

## GL/GuildBoss_GuildBossBattleBtnByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossBattleBtnUis
**Snippet:**
```lua
function GetGuildBoss_GuildBossBattleBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBossBattleNumberByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossBattleNumberUis
**Snippet:**
```lua
function GetGuildBoss_GuildBossBattleNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBossByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossUis
**Requires:**
- CommonResource_BackGroundByName
- GuildBoss_GuildBossTitleByName
- GuildBoss_GuildBossRoundByName
- GuildBoss_GuildBossTimeByName
- GuildBoss_GuildBossBattleNumberByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("GuildBoss_GuildBossTitleByName")
require("GuildBoss_GuildBossRoundByName")
require("GuildBoss_GuildBossTimeByName")
require("GuildBoss_GuildBossBattleNumberByName")

function GetGuildBoss_GuildBossUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## GL/GuildBoss_GuildBossExplainBtnByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossExplainBtnUis
**Snippet:**
```lua
function GetGuildBoss_GuildBossExplainBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBossHelpBtnByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossHelpBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetGuildBoss_GuildBossHelpBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBossLogBtnByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossLogBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetGuildBoss_GuildBossLogBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBossMemberBtnByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossMemberBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetGuildBoss_GuildBossMemberBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBossRankBtnByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossRankBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetGuildBoss_GuildBossRankBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.RankTxt = ui:GetChild("RankTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## GL/GuildBoss_GuildBossRankRewardBtnByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossRankRewardBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetGuildBoss_GuildBossRankRewardBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBossReturnBtnByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossReturnBtnUis
**Snippet:**
```lua
function GetGuildBoss_GuildBossReturnBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBossRoundByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossRoundUis
**Snippet:**
```lua
function GetGuildBoss_GuildBossRoundUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBossSkillBtnByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossSkillBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetGuildBoss_GuildBossSkillBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBossTaskBtnByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossTaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetGuildBoss_GuildBossTaskBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBossTaskByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossTaskUis
**Requires:**
- CommonResource_BackGroundByName
- GuildBoss_GuildBossTaskNumberByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("GuildBoss_GuildBossTaskNumberByName")

function GetGuildBoss_GuildBossTaskUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TaskList = ui:GetChild("TaskList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.Number = GetGuildBoss_GuildBossTaskNumberUis(ui:GetChild("Number"))
  uis.FunctionDetailsBtn = ui:GetChild("FunctionDetailsBtn")
```

---

## GL/GuildBoss_GuildBossTaskCompleteByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossTaskCompleteUis
**Snippet:**
```lua
function GetGuildBoss_GuildBossTaskCompleteUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBossTaskGetBtnByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossTaskGetBtnUis
**Snippet:**
```lua
function GetGuildBoss_GuildBossTaskGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBossTaskNumberByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossTaskNumberUis
**Snippet:**
```lua
function GetGuildBoss_GuildBossTaskNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBossTaskProgressBarByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossTaskProgressBarUis
**Requires:**
- GuildBoss_GuildBossTaskProgressFillByName
**Snippet:**
```lua
require("GuildBoss_GuildBossTaskProgressFillByName")

function GetGuildBoss_GuildBossTaskProgressBarUis(ui)
  local uis = {}
  uis.bar = GetGuildBoss_GuildBossTaskProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBossTaskProgressByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossTaskProgressUis
**Snippet:**
```lua
function GetGuildBoss_GuildBossTaskProgressUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBossTaskProgressFillByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossTaskProgressFillUis
**Snippet:**
```lua
function GetGuildBoss_GuildBossTaskProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBossTaskTipsAniByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossTaskTipsAniUis
**Requires:**
- GuildBoss_GuildBossTaskTipsByName
**Snippet:**
```lua
require("GuildBoss_GuildBossTaskTipsByName")

function GetGuildBoss_GuildBossTaskTipsAniUis(ui)
  local uis = {}
  uis.Tips = GetGuildBoss_GuildBossTaskTipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBossTaskTipsByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossTaskTipsUis
**Requires:**
- GuildBoss_GuildBossTaskProgressByName
- CommonResource_ItemFrameByName
- GuildBoss_GuildBossTaskCompleteByName
**Snippet:**
```lua
require("GuildBoss_GuildBossTaskProgressByName")
require("CommonResource_ItemFrameByName")
require("GuildBoss_GuildBossTaskCompleteByName")

function GetGuildBoss_GuildBossTaskTipsUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TaskProgressBar = ui:GetChild("TaskProgressBar")
  uis.Progress = GetGuildBoss_GuildBossTaskProgressUis(ui:GetChild("Progress"))
  uis.WordList = ui:GetChild("WordList")
```

---

## GL/GuildBoss_GuildBossTaskWindowByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossTaskWindowUis
**Requires:**
- GuildBoss_GuildBossTaskByName
**Snippet:**
```lua
require("GuildBoss_GuildBossTaskByName")

function GetGuildBoss_GuildBossTaskWindowUis(ui)
  local uis = {}
  uis.Main = GetGuildBoss_GuildBossTaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBossTaskWordByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossTaskWordUis
**Snippet:**
```lua
function GetGuildBoss_GuildBossTaskWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBossTimeByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossTimeUis
**Snippet:**
```lua
function GetGuildBoss_GuildBossTimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBossTitleByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossTitleUis
**Snippet:**
```lua
function GetGuildBoss_GuildBossTitleUis(ui)
  local uis = {}
  
  uis.GulidIconLoader = ui:GetChild("GulidIconLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildBossWindowByName.lua.lua
**Functions:**
- GetGuildBoss_GuildBossWindowUis
**Requires:**
- GuildBoss_GuildBossByName
**Snippet:**
```lua
require("GuildBoss_GuildBossByName")

function GetGuildBoss_GuildBossWindowUis(ui)
  local uis = {}
  uis.Main = GetGuildBoss_GuildBossUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildCardAssistByName.lua.lua
**Functions:**
- GetGuildBoss_GuildCardAssistUis
**Requires:**
- CommonResource_BackGroundByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")

function GetGuildBoss_GuildCardAssistUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.FunctionDetailsBtn = ui:GetChild("FunctionDetailsBtn")
  uis.root = ui
  return uis
```

---

## GL/GuildBoss_GuildCardAssistNumberByName.lua.lua
**Functions:**
- GetGuildBoss_GuildCardAssistNumberUis
**Snippet:**
```lua
function GetGuildBoss_GuildCardAssistNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildCardAssistTipsAniByName.lua.lua
**Functions:**
- GetGuildBoss_GuildCardAssistTipsAniUis
**Requires:**
- GuildBoss_GuildCardAssistTipsByName
- GuildBoss_GuildCardAssistNumberByName
**Snippet:**
```lua
require("GuildBoss_GuildCardAssistTipsByName")
require("GuildBoss_GuildCardAssistNumberByName")

function GetGuildBoss_GuildCardAssistTipsAniUis(ui)
  local uis = {}
  uis.Tips = GetGuildBoss_GuildCardAssistTipsUis(ui:GetChild("Tips"))
  uis.Number = GetGuildBoss_GuildCardAssistNumberUis(ui:GetChild("Number"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## GL/GuildBoss_GuildCardAssistTipsByName.lua.lua
**Functions:**
- GetGuildBoss_GuildCardAssistTipsUis
**Requires:**
- GuildBoss_GuildCardAssistTipsPicByName
- CommonResource_CardBreachByName
- CommonResource_OccupationByName
**Snippet:**
```lua
require("GuildBoss_GuildCardAssistTipsPicByName")
require("CommonResource_CardBreachByName")
require("CommonResource_OccupationByName")

function GetGuildBoss_GuildCardAssistTipsUis(ui)
  local uis = {}
  uis.CardPic = GetGuildBoss_GuildCardAssistTipsPicUis(ui:GetChild("CardPic"))
  uis.StarList = ui:GetChild("StarList")
  uis.CardBreach = GetCommonResource_CardBreachUis(ui:GetChild("CardBreach"))
  uis.NameTxt = ui:GetChild("NameTxt")
```

---

## GL/GuildBoss_GuildCardAssistTipsPicByName.lua.lua
**Functions:**
- GetGuildBoss_GuildCardAssistTipsPicUis
**Snippet:**
```lua
function GetGuildBoss_GuildCardAssistTipsPicUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildCardAssistWindowByName.lua.lua
**Functions:**
- GetGuildBoss_GuildCardAssistWindowUis
**Requires:**
- GuildBoss_GuildCardAssistByName
**Snippet:**
```lua
require("GuildBoss_GuildCardAssistByName")

function GetGuildBoss_GuildCardAssistWindowUis(ui)
  local uis = {}
  uis.Main = GetGuildBoss_GuildCardAssistUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildCompensateByName.lua.lua
**Functions:**
- GetGuildBoss_GuildCompensateUis
**Requires:**
- CommonResource_PopupBgByName
- GuildBoss_CompensateTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("GuildBoss_CompensateTipsByName")

function GetGuildBoss_GuildCompensateUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Tips = GetGuildBoss_CompensateTipsUis(ui:GetChild("Tips"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## GL/GuildBoss_GuildCompensateWindowByName.lua.lua
**Functions:**
- GetGuildBoss_GuildCompensateWindowUis
**Requires:**
- GuildBoss_GuildCompensateByName
**Snippet:**
```lua
require("GuildBoss_GuildCompensateByName")

function GetGuildBoss_GuildCompensateWindowUis(ui)
  local uis = {}
  uis.Main = GetGuildBoss_GuildCompensateUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildRankByName.lua.lua
**Functions:**
- GetGuildBoss_GuildRankUis
**Requires:**
- CommonResource_BackGroundByName
- GuildBoss_GuildRankTitleByName
- GuildBoss_GuildRankInfoByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("GuildBoss_GuildRankTitleByName")
require("GuildBoss_GuildRankInfoByName")

function GetGuildBoss_GuildRankUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.Tab1Btn = ui:GetChild("Tab1Btn")
  uis.Tab2Btn = ui:GetChild("Tab2Btn")
```

---

## GL/GuildBoss_GuildRankCardTipsAniByName.lua.lua
**Functions:**
- GetGuildBoss_GuildRankCardTipsAniUis
**Requires:**
- GuildBoss_GuildRankCardTipsByName
**Snippet:**
```lua
require("GuildBoss_GuildRankCardTipsByName")

function GetGuildBoss_GuildRankCardTipsAniUis(ui)
  local uis = {}
  uis.RankTips = GetGuildBoss_GuildRankCardTipsUis(ui:GetChild("RankTips"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildRankCardTipsByName.lua.lua
**Functions:**
- GetGuildBoss_GuildRankCardTipsUis
**Requires:**
- CommonResource_HeadByName
**Snippet:**
```lua
require("CommonResource_HeadByName")

function GetGuildBoss_GuildRankCardTipsUis(ui)
  local uis = {}
  uis.RankTxt = ui:GetChild("RankTxt")
  uis.Head = GetCommonResource_HeadUis(ui:GetChild("Head"))
  uis.GuildTxt = ui:GetChild("GuildTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.NumberWordTxt = ui:GetChild("NumberWordTxt")
```

---

## GL/GuildBoss_GuildRankInfoByName.lua.lua
**Functions:**
- GetGuildBoss_GuildRankInfoUis
**Requires:**
- GuildBoss_GuildRankInfoOwnByName
- GuildBoss_GuildRankInfoGuildByName
**Snippet:**
```lua
require("GuildBoss_GuildRankInfoOwnByName")
require("GuildBoss_GuildRankInfoGuildByName")

function GetGuildBoss_GuildRankInfoUis(ui)
  local uis = {}
  uis.Own = GetGuildBoss_GuildRankInfoOwnUis(ui:GetChild("Own"))
  uis.Guild = GetGuildBoss_GuildRankInfoGuildUis(ui:GetChild("Guild"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildRankInfoGuildByName.lua.lua
**Functions:**
- GetGuildBoss_GuildRankInfoGuildUis
**Snippet:**
```lua
function GetGuildBoss_GuildRankInfoGuildUis(ui)
  local uis = {}
  
  uis.RankTxt = ui:GetChild("RankTxt")
  uis.GulidIconLoader = ui:GetChild("GulidIconLoader")
  uis.GuildTxt = ui:GetChild("GuildTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.RoundTxt = ui:GetChild("RoundTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
```

---

## GL/GuildBoss_GuildRankInfoOwnByName.lua.lua
**Functions:**
- GetGuildBoss_GuildRankInfoOwnUis
**Requires:**
- CommonResource_HeadByName
**Snippet:**
```lua
require("CommonResource_HeadByName")

function GetGuildBoss_GuildRankInfoOwnUis(ui)
  local uis = {}
  uis.Head = GetCommonResource_HeadUis(ui:GetChild("Head"))
  uis.RankTxt = ui:GetChild("RankTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberWordTxt = ui:GetChild("NumberWordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## GL/GuildBoss_GuildRankRewardByName.lua.lua
**Functions:**
- GetGuildBoss_GuildRankRewardUis
**Requires:**
- CommonResource_BackGroundByName
- GuildBoss_GuildRankRewardTitleByName
- GuildBoss_GuildRankRewardInfoByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("GuildBoss_GuildRankRewardTitleByName")
require("GuildBoss_GuildRankRewardInfoByName")

function GetGuildBoss_GuildRankRewardUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.Title = GetGuildBoss_GuildRankRewardTitleUis(ui:GetChild("Title"))
  uis.RewardTipsList = ui:GetChild("RewardTipsList")
```

---

## GL/GuildBoss_GuildRankRewardInfoByName.lua.lua
**Functions:**
- GetGuildBoss_GuildRankRewardInfoUis
**Snippet:**
```lua
function GetGuildBoss_GuildRankRewardInfoUis(ui)
  local uis = {}
  
  uis.RankWordTxt = ui:GetChild("RankWordTxt")
  uis.RankNumberTxt = ui:GetChild("RankNumberTxt")
  uis.TimeWordTxt = ui:GetChild("TimeWordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildRankRewardNumberByName.lua.lua
**Functions:**
- GetGuildBoss_GuildRankRewardNumberUis
**Snippet:**
```lua
function GetGuildBoss_GuildRankRewardNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildRankRewardTipsAniByName.lua.lua
**Functions:**
- GetGuildBoss_GuildRankRewardTipsAniUis
**Requires:**
- GuildBoss_GuildRankRewardTipsByName
**Snippet:**
```lua
require("GuildBoss_GuildRankRewardTipsByName")

function GetGuildBoss_GuildRankRewardTipsAniUis(ui)
  local uis = {}
  uis.RankRewardTips = GetGuildBoss_GuildRankRewardTipsUis(ui:GetChild("RankRewardTips"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildRankRewardTipsByName.lua.lua
**Functions:**
- GetGuildBoss_GuildRankRewardTipsUis
**Requires:**
- GuildBoss_GuildRankRewardNumberByName
**Snippet:**
```lua
require("GuildBoss_GuildRankRewardNumberByName")

function GetGuildBoss_GuildRankRewardTipsUis(ui)
  local uis = {}
  uis.RankRewardNumber = GetGuildBoss_GuildRankRewardNumberUis(ui:GetChild("RankRewardNumber"))
  uis.RewardList = ui:GetChild("RewardList")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildRankRewardTipsListByName.lua.lua
**Functions:**
- GetGuildBoss_GuildRankRewardTipsListUis
**Snippet:**
```lua
function GetGuildBoss_GuildRankRewardTipsListUis(ui)
  local uis = {}
  
  uis.RewardTipsList = ui:GetChild("RewardTipsList")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildRankRewardTitleByName.lua.lua
**Functions:**
- GetGuildBoss_GuildRankRewardTitleUis
**Snippet:**
```lua
function GetGuildBoss_GuildRankRewardTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildRankRewardWindowByName.lua.lua
**Functions:**
- GetGuildBoss_GuildRankRewardWindowUis
**Requires:**
- GuildBoss_GuildRankRewardByName
**Snippet:**
```lua
require("GuildBoss_GuildRankRewardByName")

function GetGuildBoss_GuildRankRewardWindowUis(ui)
  local uis = {}
  uis.Main = GetGuildBoss_GuildRankRewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildRankTab1BtnByName.lua.lua
**Functions:**
- GetGuildBoss_GuildRankTab1BtnUis
**Snippet:**
```lua
function GetGuildBoss_GuildRankTab1BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildRankTab2BtnByName.lua.lua
**Functions:**
- GetGuildBoss_GuildRankTab2BtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetGuildBoss_GuildRankTab2BtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildRankTipsAniByName.lua.lua
**Functions:**
- GetGuildBoss_GuildRankTipsAniUis
**Requires:**
- GuildBoss_GuildRankTipsByName
**Snippet:**
```lua
require("GuildBoss_GuildRankTipsByName")

function GetGuildBoss_GuildRankTipsAniUis(ui)
  local uis = {}
  uis.RankTips = GetGuildBoss_GuildRankTipsUis(ui:GetChild("RankTips"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildRankTipsByName.lua.lua
**Functions:**
- GetGuildBoss_GuildRankTipsUis
**Snippet:**
```lua
function GetGuildBoss_GuildRankTipsUis(ui)
  local uis = {}
  
  uis.RankTxt = ui:GetChild("RankTxt")
  uis.GulidIconLoader = ui:GetChild("GulidIconLoader")
  uis.CardNumberTxt = ui:GetChild("CardNumberTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.RoundTxt = ui:GetChild("RoundTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
```

---

## GL/GuildBoss_GuildRankTitleByName.lua.lua
**Functions:**
- GetGuildBoss_GuildRankTitleUis
**Snippet:**
```lua
function GetGuildBoss_GuildRankTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildRankWindowByName.lua.lua
**Functions:**
- GetGuildBoss_GuildRankWindowUis
**Requires:**
- GuildBoss_GuildRankByName
**Snippet:**
```lua
require("GuildBoss_GuildRankByName")

function GetGuildBoss_GuildRankWindowUis(ui)
  local uis = {}
  uis.Main = GetGuildBoss_GuildRankUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildSkillByName.lua.lua
**Functions:**
- GetGuildBoss_GuildSkillUis
**Requires:**
- CommonResource_BackGroundByName
- GuildBoss_GuildSkillWordByName
- GuildBoss_GuildSkillModuleRegionByName
- GuildBoss_GuildSkillProgrammeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("GuildBoss_GuildSkillWordByName")
require("GuildBoss_GuildSkillModuleRegionByName")
require("GuildBoss_GuildSkillProgrammeByName")

function GetGuildBoss_GuildSkillUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Word = GetGuildBoss_GuildSkillWordUis(ui:GetChild("Word"))
  uis.ModuleRegion = GetGuildBoss_GuildSkillModuleRegionUis(ui:GetChild("ModuleRegion"))
```

---

## GL/GuildBoss_GuildSkillEditBtnByName.lua.lua
**Functions:**
- GetGuildBoss_GuildSkillEditBtnUis
**Snippet:**
```lua
function GetGuildBoss_GuildSkillEditBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildSkillEffectLevelByName.lua.lua
**Functions:**
- GetGuildBoss_GuildSkillEffectLevelUis
**Requires:**
- GuildBoss_GuildSkillEffectLevelSignByName
**Snippet:**
```lua
require("GuildBoss_GuildSkillEffectLevelSignByName")

function GetGuildBoss_GuildSkillEffectLevelUis(ui)
  local uis = {}
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Sign = GetGuildBoss_GuildSkillEffectLevelSignUis(ui:GetChild("Sign"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## GL/GuildBoss_GuildSkillEffectLevelSignByName.lua.lua
**Functions:**
- GetGuildBoss_GuildSkillEffectLevelSignUis
**Snippet:**
```lua
function GetGuildBoss_GuildSkillEffectLevelSignUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildSkillEffectRegionByName.lua.lua
**Functions:**
- GetGuildBoss_GuildSkillEffectRegionUis
**Snippet:**
```lua
function GetGuildBoss_GuildSkillEffectRegionUis(ui)
  local uis = {}
  
  uis.EffectList = ui:GetChild("EffectList")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildSkillModuleBtnByName.lua.lua
**Functions:**
- GetGuildBoss_GuildSkillModuleBtnUis
**Requires:**
- GuildBoss_GuildSkillWearByName
**Snippet:**
```lua
require("GuildBoss_GuildSkillWearByName")

function GetGuildBoss_GuildSkillModuleBtnUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.Wear = GetGuildBoss_GuildSkillWearUis(ui:GetChild("Wear"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.wearCtr = ui:GetController("wear")
```

---

## GL/GuildBoss_GuildSkillModuleRegionByName.lua.lua
**Functions:**
- GetGuildBoss_GuildSkillModuleRegionUis
**Snippet:**
```lua
function GetGuildBoss_GuildSkillModuleRegionUis(ui)
  local uis = {}
  
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.SkillModule1Btn = ui:GetChild("SkillModule1Btn")
  uis.SkillModule2Btn = ui:GetChild("SkillModule2Btn")
  uis.SkillModule3Btn = ui:GetChild("SkillModule3Btn")
  uis.SkillModule4Btn = ui:GetChild("SkillModule4Btn")
  uis.SkillModule5Btn = ui:GetChild("SkillModule5Btn")
  uis.c1Ctr = ui:GetController("c1")
```

---

## GL/GuildBoss_GuildSkillProgrammeByName.lua.lua
**Functions:**
- GetGuildBoss_GuildSkillProgrammeUis
**Requires:**
- GuildBoss_GuildSkillEffectRegionByName
- GuildBoss_ProgrammeSkillRegionByName
- GuildBoss_ProgrammeSkillLevelByName
- GuildBoss_ProgrammeSkillLockByName
**Snippet:**
```lua
require("GuildBoss_GuildSkillEffectRegionByName")
require("GuildBoss_ProgrammeSkillRegionByName")
require("GuildBoss_ProgrammeSkillLevelByName")
require("GuildBoss_ProgrammeSkillLockByName")

function GetGuildBoss_GuildSkillProgrammeUis(ui)
  local uis = {}
  uis.EffectRegion = GetGuildBoss_GuildSkillEffectRegionUis(ui:GetChild("EffectRegion"))
  uis.ProgrammeList = ui:GetChild("ProgrammeList")
  uis.SkillRegion = GetGuildBoss_ProgrammeSkillRegionUis(ui:GetChild("SkillRegion"))
```

---

## GL/GuildBoss_GuildSkillWearByName.lua.lua
**Functions:**
- GetGuildBoss_GuildSkillWearUis
**Snippet:**
```lua
function GetGuildBoss_GuildSkillWearUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildSkillWindowByName.lua.lua
**Functions:**
- GetGuildBoss_GuildSkillWindowUis
**Requires:**
- GuildBoss_GuildSkillByName
**Snippet:**
```lua
require("GuildBoss_GuildSkillByName")

function GetGuildBoss_GuildSkillWindowUis(ui)
  local uis = {}
  uis.Main = GetGuildBoss_GuildSkillUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_GuildSkillWordByName.lua.lua
**Functions:**
- GetGuildBoss_GuildSkillWordUis
**Snippet:**
```lua
function GetGuildBoss_GuildSkillWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_ProgrammeBtnByName.lua.lua
**Functions:**
- GetGuildBoss_ProgrammeBtnUis
**Snippet:**
```lua
function GetGuildBoss_ProgrammeBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_ProgrammeSkillByName.lua.lua
**Functions:**
- GetGuildBoss_ProgrammeSkillUis
**Snippet:**
```lua
function GetGuildBoss_ProgrammeSkillUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_ProgrammeSkillLevelByName.lua.lua
**Functions:**
- GetGuildBoss_ProgrammeSkillLevelUis
**Snippet:**
```lua
function GetGuildBoss_ProgrammeSkillLevelUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.maxCtr = ui:GetController("max")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_ProgrammeSkillLockByName.lua.lua
**Functions:**
- GetGuildBoss_ProgrammeSkillLockUis
**Snippet:**
```lua
function GetGuildBoss_ProgrammeSkillLockUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_ProgrammeSkillLookBtnByName.lua.lua
**Functions:**
- GetGuildBoss_ProgrammeSkillLookBtnUis
**Snippet:**
```lua
function GetGuildBoss_ProgrammeSkillLookBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_ProgrammeSkillNumberByName.lua.lua
**Functions:**
- GetGuildBoss_ProgrammeSkillNumberUis
**Snippet:**
```lua
function GetGuildBoss_ProgrammeSkillNumberUis(ui)
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

## GL/GuildBoss_ProgrammeSkillRegionByName.lua.lua
**Functions:**
- GetGuildBoss_ProgrammeSkillRegionUis
**Snippet:**
```lua
function GetGuildBoss_ProgrammeSkillRegionUis(ui)
  local uis = {}
  
  uis.SkillList = ui:GetChild("SkillList")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_ProgrammeSkillUpBtnByName.lua.lua
**Functions:**
- GetGuildBoss_ProgrammeSkillUpBtnUis
**Snippet:**
```lua
function GetGuildBoss_ProgrammeSkillUpBtnUis(ui)
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

## GL/GuildBoss_ProgrammeSkillWearBtnByName.lua.lua
**Functions:**
- GetGuildBoss_ProgrammeSkillWearBtnUis
**Snippet:**
```lua
function GetGuildBoss_ProgrammeSkillWearBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.maxCtr = ui:GetController("max")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_ProgrammeSkillWordByName.lua.lua
**Functions:**
- GetGuildBoss_ProgrammeSkillWordUis
**Snippet:**
```lua
function GetGuildBoss_ProgrammeSkillWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_RecommendByName.lua.lua
**Functions:**
- GetGuildBoss_RecommendUis
**Requires:**
- CommonResource_PopupBgByName
- GuildBoss_RecommendNothingByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("GuildBoss_RecommendNothingByName")

function GetGuildBoss_RecommendUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.ScreenBtn = ui:GetChild("ScreenBtn")
  uis.Nothing = GetGuildBoss_RecommendNothingUis(ui:GetChild("Nothing"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## GL/GuildBoss_RecommendCardHeadAniByName.lua.lua
**Functions:**
- GetGuildBoss_RecommendCardHeadAniUis
**Snippet:**
```lua
function GetGuildBoss_RecommendCardHeadAniUis(ui)
  local uis = {}
  
  uis.CardHeadBtn = ui:GetChild("CardHeadBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_RecommendCardHeadBgByName.lua.lua
**Functions:**
- GetGuildBoss_RecommendCardHeadBgUis
**Snippet:**
```lua
function GetGuildBoss_RecommendCardHeadBgUis(ui)
  local uis = {}
  
  uis.CardPicLoader = ui:GetChild("CardPicLoader")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_RecommendCardHeadBtnByName.lua.lua
**Functions:**
- GetGuildBoss_RecommendCardHeadBtnUis
**Requires:**
- GuildBoss_RecommendCardHeadBgByName
- CommonResource_OccupationByName
- CommonResource_CardBreachByName
- GuildBoss_RecommendCardStateByName
**Snippet:**
```lua
require("GuildBoss_RecommendCardHeadBgByName")
require("CommonResource_OccupationByName")
require("CommonResource_CardBreachByName")
require("GuildBoss_RecommendCardStateByName")

function GetGuildBoss_RecommendCardHeadBtnUis(ui)
  local uis = {}
  uis.CardPic = GetGuildBoss_RecommendCardHeadBgUis(ui:GetChild("CardPic"))
  uis.ElementList = ui:GetChild("ElementList")
  uis.NameTxt = ui:GetChild("NameTxt")
```

---

## GL/GuildBoss_RecommendCardStateByName.lua.lua
**Functions:**
- GetGuildBoss_RecommendCardStateUis
**Snippet:**
```lua
function GetGuildBoss_RecommendCardStateUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_RecommendCurrency1ByName.lua.lua
**Functions:**
- GetGuildBoss_RecommendCurrency1Uis
**Snippet:**
```lua
function GetGuildBoss_RecommendCurrency1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_RecommendCurrency2ByName.lua.lua
**Functions:**
- GetGuildBoss_RecommendCurrency2Uis
**Requires:**
- CommonResource_PopupBgByName
- CommonResource_Popup_BByName
- GuildBoss_RecommendCurrency1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("CommonResource_Popup_BByName")
require("GuildBoss_RecommendCurrency1ByName")

function GetGuildBoss_RecommendCurrency2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Popup_B = GetCommonResource_Popup_BUis(ui:GetChild("Popup_B"))
  uis.Currency1 = GetGuildBoss_RecommendCurrency1Uis(ui:GetChild("Currency1"))
```

---

## GL/GuildBoss_RecommendCurrencyWindowByName.lua.lua
**Functions:**
- GetGuildBoss_RecommendCurrencyWindowUis
**Requires:**
- GuildBoss_RecommendCurrency2ByName
**Snippet:**
```lua
require("GuildBoss_RecommendCurrency2ByName")

function GetGuildBoss_RecommendCurrencyWindowUis(ui)
  local uis = {}
  uis.Main = GetGuildBoss_RecommendCurrency2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_RecommendDataBtnByName.lua.lua
**Functions:**
- GetGuildBoss_RecommendDataBtnUis
**Snippet:**
```lua
function GetGuildBoss_RecommendDataBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_RecommendIntegralByName.lua.lua
**Functions:**
- GetGuildBoss_RecommendIntegralUis
**Snippet:**
```lua
function GetGuildBoss_RecommendIntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_RecommendNothingByName.lua.lua
**Functions:**
- GetGuildBoss_RecommendNothingUis
**Snippet:**
```lua
function GetGuildBoss_RecommendNothingUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_RecommendPlayBackBtnByName.lua.lua
**Functions:**
- GetGuildBoss_RecommendPlayBackBtnUis
**Snippet:**
```lua
function GetGuildBoss_RecommendPlayBackBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_RecommendScreenBtnByName.lua.lua
**Functions:**
- GetGuildBoss_RecommendScreenBtnUis
**Snippet:**
```lua
function GetGuildBoss_RecommendScreenBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_RecommendScreenByName.lua.lua
**Functions:**
- GetGuildBoss_RecommendScreenUis
**Requires:**
- CommonResource_PopupBgByName
- GuildBoss_ScreenTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("GuildBoss_ScreenTipsByName")

function GetGuildBoss_RecommendScreenUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Tips = GetGuildBoss_ScreenTipsUis(ui:GetChild("Tips"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## GL/GuildBoss_RecommendScreenWindowByName.lua.lua
**Functions:**
- GetGuildBoss_RecommendScreenWindowUis
**Requires:**
- GuildBoss_RecommendScreenByName
**Snippet:**
```lua
require("GuildBoss_RecommendScreenByName")

function GetGuildBoss_RecommendScreenWindowUis(ui)
  local uis = {}
  uis.Main = GetGuildBoss_RecommendScreenUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_RecommendSkillByName.lua.lua
**Functions:**
- GetGuildBoss_RecommendSkillUis
**Snippet:**
```lua
function GetGuildBoss_RecommendSkillUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_RecommendTimeAxisBtnByName.lua.lua
**Functions:**
- GetGuildBoss_RecommendTimeAxisBtnUis
**Snippet:**
```lua
function GetGuildBoss_RecommendTimeAxisBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_RecommendTipsAniByName.lua.lua
**Functions:**
- GetGuildBoss_RecommendTipsAniUis
**Requires:**
- GuildBoss_RecommendTipsByName
**Snippet:**
```lua
require("GuildBoss_RecommendTipsByName")

function GetGuildBoss_RecommendTipsAniUis(ui)
  local uis = {}
  uis.Tips = GetGuildBoss_RecommendTipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_RecommendTipsByName.lua.lua
**Functions:**
- GetGuildBoss_RecommendTipsUis
**Requires:**
- GuildBoss_RecommendIntegralByName
**Snippet:**
```lua
require("GuildBoss_RecommendIntegralByName")

function GetGuildBoss_RecommendTipsUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.SkillList = ui:GetChild("SkillList")
  uis.HeadList = ui:GetChild("HeadList")
  uis.Integral = GetGuildBoss_RecommendIntegralUis(ui:GetChild("Integral"))
  uis.TimeAxisBtn = ui:GetChild("TimeAxisBtn")
```

---

## GL/GuildBoss_RecommendUseBtnByName.lua.lua
**Functions:**
- GetGuildBoss_RecommendUseBtnUis
**Snippet:**
```lua
function GetGuildBoss_RecommendUseBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_RecommendWindowByName.lua.lua
**Functions:**
- GetGuildBoss_RecommendWindowUis
**Requires:**
- GuildBoss_RecommendByName
**Snippet:**
```lua
require("GuildBoss_RecommendByName")

function GetGuildBoss_RecommendWindowUis(ui)
  local uis = {}
  uis.Main = GetGuildBoss_RecommendUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_ScreenCardHeadAniByName.lua.lua
**Functions:**
- GetGuildBoss_ScreenCardHeadAniUis
**Snippet:**
```lua
function GetGuildBoss_ScreenCardHeadAniUis(ui)
  local uis = {}
  
  uis.CardHeadBtn = ui:GetChild("CardHeadBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_ScreenCardHeadBgByName.lua.lua
**Functions:**
- GetGuildBoss_ScreenCardHeadBgUis
**Snippet:**
```lua
function GetGuildBoss_ScreenCardHeadBgUis(ui)
  local uis = {}
  
  uis.CardPicLoader = ui:GetChild("CardPicLoader")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_ScreenCardHeadBtnByName.lua.lua
**Functions:**
- GetGuildBoss_ScreenCardHeadBtnUis
**Requires:**
- GuildBoss_ScreenCardHeadBgByName
- CommonResource_OccupationByName
- GuildBoss_ScreenCardStateByName
**Snippet:**
```lua
require("GuildBoss_ScreenCardHeadBgByName")
require("CommonResource_OccupationByName")
require("GuildBoss_ScreenCardStateByName")

function GetGuildBoss_ScreenCardHeadBtnUis(ui)
  local uis = {}
  uis.CardPic = GetGuildBoss_ScreenCardHeadBgUis(ui:GetChild("CardPic"))
  uis.ElementList = ui:GetChild("ElementList")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Occupation = GetCommonResource_OccupationUis(ui:GetChild("Occupation"))
```

---

## GL/GuildBoss_ScreenCardStateByName.lua.lua
**Functions:**
- GetGuildBoss_ScreenCardStateUis
**Snippet:**
```lua
function GetGuildBoss_ScreenCardStateUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_ScreenTipsByName.lua.lua
**Functions:**
- GetGuildBoss_ScreenTipsUis
**Requires:**
- GuildBoss_ScreenTipsTitleByName
**Snippet:**
```lua
require("GuildBoss_ScreenTipsTitleByName")

function GetGuildBoss_ScreenTipsUis(ui)
  local uis = {}
  uis.Popup_S_Black_Btn = ui:GetChild("Popup_S_Black_Btn")
  uis.Popup_S_Green_Btn = ui:GetChild("Popup_S_Green_Btn")
  uis.Title1 = GetGuildBoss_ScreenTipsTitleUis(ui:GetChild("Title1"))
  uis.CardList = ui:GetChild("CardList")
  uis.Title2 = GetGuildBoss_ScreenTipsTitleUis(ui:GetChild("Title2"))
  uis.ScreenList = ui:GetChild("ScreenList")
```

---

## GL/GuildBoss_ScreenTipsResetBtnByName.lua.lua
**Functions:**
- GetGuildBoss_ScreenTipsResetBtnUis
**Snippet:**
```lua
function GetGuildBoss_ScreenTipsResetBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_ScreenTipsSureBtnByName.lua.lua
**Functions:**
- GetGuildBoss_ScreenTipsSureBtnUis
**Snippet:**
```lua
function GetGuildBoss_ScreenTipsSureBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildBoss_ScreenTipsTitleByName.lua.lua
**Functions:**
- GetGuildBoss_ScreenTipsTitleUis
**Snippet:**
```lua
function GetGuildBoss_ScreenTipsTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildData.lua.lua
**Functions:**
- GuildData.GetGuildItemData
- GuildData.GetViceCaptainNum
- GuildData.SetGuildSimpleInfo
- GuildData.GetGuildSimpleInfo
- GuildData.GetGuildNoticeFromSimpleInfo
- GuildData.GetGuildRoleTypeFromSimpleInfo
- GuildData.UpdateNotice
- GuildData.ClearTrainData
- GuildData.SaveTrainRankData
- GuildData.GetTrainRankData
- GuildData.SaveTrainDetailsData
- GuildData.GetDetailsData
- GuildData.Close
**Snippet:**
```lua
GuildData = {simpleInfo = nil, signInInfo = nil}

function GuildData.GetGuildItemData(uin)
  for _, v in ipairs(GuildData.GuildInfo.members) do
    if v.uin == uin then
      return v
    end
  end
end

```

---

## GL/GuildFilterWindow.lua.lua
**Functions:**
- GuildFilterWindow.ReInitData
- GuildFilterWindow.OnInit
- GuildFilterWindow.SettingInfo
- policyList.itemRenderer
- GuildFilterWindow.SearchInfo
- optionList.itemRenderer
- limitList.itemRenderer
- policyList.itemRenderer
- bossRankList.itemRenderer
- GuildFilterWindow.GetPolicy
- GuildFilterWindow.GetNumber
- GuildFilterWindow.CloseWindow
- GuildFilterWindow.InitBtn
- GuildFilterWindow.OnClose
**Requires:**
- Guild_GuildFilterWindowByName
**Snippet:**
```lua
require("Guild_GuildFilterWindowByName")
local GuildFilterWindow = {}
local uis, contentPane, searchTxt, policyId, searchName, guildMin, guildMax, guildLimit, bossRank

function GuildFilterWindow.ReInitData()
end

function GuildFilterWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.GuildFilterWindow.package, WinResConfig.GuildFilterWindow.comName, function(com)
    contentPane = com
```

---

## GL/GuildIconChoiceWindow.lua.lua
**Functions:**
- GuildIconChoiceWindow.OnInit
- GuildIconChoiceWindow.UpdateTextDisplay
- GuildIconChoiceWindow.RefreshIconItem
- GuildIconChoiceWindow.ItemOnClick
- GuildIconChoiceWindow.ClickClose
- GuildIconChoiceWindow.InitBtn
- GuildIconChoiceWindow.HandleMessage
- GuildIconChoiceWindow.OnClose
**Requires:**
- Guild_IconChoiceWindowByName
**Snippet:**
```lua
require("Guild_IconChoiceWindowByName")
local GuildIconChoiceWindow = {}
local uis, contentPane, listData, selectId, curId

function GuildIconChoiceWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.GuildIconChoiceWindow.package, WinResConfig.GuildIconChoiceWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    curId = bridgeObj.argTable[1]
    uis = GetGuild_IconChoiceWindowUis(contentPane)
```

---

## GL/GuildLevelUpTipsWindow.lua.lua
**Functions:**
- GuildLevelUpTipsWindow.ReInitData
- GuildLevelUpTipsWindow.OnInit
- GuildLevelUpTipsWindow.UpdateTextDisplay
- GuildLevelUpTipsWindow.InitBtn
- GuildLevelUpTipsWindow.OnClose
- GuildLevelUpTipsWindow.HandleMessage
**Requires:**
- Guild_LevelUpTipsWindowByName
**Snippet:**
```lua
require("Guild_LevelUpTipsWindowByName")
local GuildLevelUpTipsWindow = {}
local uis, contentPane, lv

function GuildLevelUpTipsWindow.ReInitData()
end

function GuildLevelUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.GuildLevelUpTipsWindow.package, WinResConfig.GuildLevelUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## GL/GuildListWindow.lua.lua
**Functions:**
- GuildListWindow.OnInit
- GuildListWindow.UpdateTextDisplay
- GuildListWindow.ShowJoinCdTime
- GuildListWindow.InitApplied
- GuildListWindow.InitList
- GuildListWindow.RefreshGuildItem
- GuildListWindow.GetPolicy
- GuildListWindow.RefreshApplyState
- GuildListWindow.ApplyOnClick
- GuildListWindow.GetGuildDataById
- GuildListWindow.CancelJoinGuild
- GuildListWindow.ApplyJoinGuild
- GuildListWindow:StopDownTime
- GuildListWindow.JoinTips
- GuildListWindow.CreateTips
- GuildListWindow.InitBtn
- GuildListWindow.CreateGuild
- GuildListWindow.HandleMessage
- GuildListWindow.OnClose
**Requires:**
- Guild_GuildListWindowByName
**Snippet:**
```lua
require("Guild_GuildListWindowByName")
local GuildListWindow = {}
local uis
local itemTb = {}
local countDownTb = {}
local activeDesData, contentPane, applyText, cancelUid, joinCdTimeInfo, creationData, listType, jumpTb, tween, playAnim

function GuildListWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.GuildListWindow.package, WinResConfig.GuildListWindow.comName, function(com)
    contentPane = com
```

---

## GL/GuildMgr.lua.lua
**Functions:**
- GuildMgr.SortByRoleType
- GuildMgr.SortByGuildId
- GuildMgr.GetDownTime
- GuildMgr.FormatTime
- GuildMgr.GetServiceId
- GuildMgr.UpdateApplyJoin
- GuildMgr.UpdateGuildSign
**Snippet:**
```lua
GuildMgr = {}
GuildEnum = {
  ACTIVE_ID = 70010313,
  GUILD_LEVEL_UP_ID = 7007010,
  MAX_LEVEL_ID = 70010314,
  RENAME_NAME_ID = 70010311,
  CREATION_GUILD = 70010301
}

function GuildMgr.SortByRoleType(tb)
```

---

## GL/GuildScriptList.lua.lua
**Requires:**
- GuildData
- GuildMgr
- GuildService
**Snippet:**
```lua
local require = require
require("GuildData")
require("GuildMgr")
require("GuildService")
```

---

## GL/GuildService.lua.lua
**Functions:**
- GuildService.Init
- GuildService.SearchGuildByConditionsReq
- GuildService.SearchGuildByConditionsRsp
- GuildService.SetGuildPolicyReq
- GuildService.SetGuildPolicyRsp
- GuildService.GetMyGuildSimpleInfoReq
- GuildService.GetMyGuildSimpleInfoRsp
- GuildService.EnterGuild
- GuildService.GetMyGuildInfoReq
- GuildService.GetMyGuildInfoRsp
- GuildService.GetRecommendGuildReq
- GuildService.GetRecommendGuildRsp
- GuildService.ApplyJoinGuildReq
- GuildService.ApplyJoinGuildRsp
- GuildService.CancelJoinGuildReq
- GuildService.CancelJoinGuildRsp
- GuildService.GetAppliedGuildsReq
- GuildService.GetAppliedGuildsRsp
- GuildService.QuickJoinGuildReq
- GuildService.QuickJoinGuildRsp
- GuildService.CreateGuildReq
- GuildService.CreateGuildRsp
- GuildService.SearchGuildByNameReq
- GuildService.SearchGuildByNameRsp
- GuildService.SetGuildLevelLimitReq
- GuildService.SetGuildLevelLimitRsp
- GuildService.SetGuildTargetReq
- GuildService.SetGuildTargetRsp
- GuildService.ChangeGuildNameReq
- GuildService.ChangeGuildNameRsp
- GuildService.ProcessGuildJoinApplyReq
- GuildService.ProcessGuildJoinApplyRsp
- GuildService.ExitGuildReq
- GuildService.ExitGuildRsp
- GuildService.DismissGuildReq
- GuildService.DismissGuildRsp
- GuildService.StartImpeachGuildLeaderReq
- GuildService.StartImpeachGuildLeaderRsp
- GuildService.VoteImpeachGuildLeaderReq
- GuildService.VoteImpeachGuildLeaderRsp
- GuildService.ChangeGuildIconReq
- GuildService.ChangeGuildIconRsp
- GuildService.OperateGuildViceLeaderReq
- GuildService.OperateGuildViceLeaderRsp
- GuildService.KickOutGuildMemberReq
- GuildService.KickOutGuildMemberRsp
- GuildService.TransferGuildLeaderReq
- GuildService.TransferGuildLeaderRsp
- GuildService.GetGuildMembersReq
- GuildService.GetGuildMembersRsp
- GuildService.GetImpeachInfoReq
- GuildService.GetImpeachInfoRsp
- GuildService.GetActorSignInReq
- GuildService.GetActorSignInRsp
- GuildService.ChangeGuildNoticeReq
- GuildService.ChangeGuildNoticeRsp
- GuildService.ActorSignInReq
- GuildService.ActorSignInRsp
- GuildService.GetGuildPracticeRankReq
- GuildService.GetGuildPracticeRankRsp
- GuildService.GetGuildPracticeRecordReq
- GuildService.GetGuildPracticeRecordRsp
**Snippet:**
```lua
GuildService = {}

function GuildService.Init()
  Net.AddListener(Proto.MsgName.GetMyGuildInfoRsp, GuildService.GetMyGuildInfoRsp)
  Net.AddListener(Proto.MsgName.GetRecommendGuildRsp, GuildService.GetRecommendGuildRsp)
  Net.AddListener(Proto.MsgName.ApplyJoinGuildRsp, GuildService.ApplyJoinGuildRsp)
  Net.AddListener(Proto.MsgName.CancelJoinGuildRsp, GuildService.CancelJoinGuildRsp)
  Net.AddListener(Proto.MsgName.GetAppliedGuildsRsp, GuildService.GetAppliedGuildsRsp)
  Net.AddListener(Proto.MsgName.QuickJoinGuildRsp, GuildService.QuickJoinGuildRsp)
  Net.AddListener(Proto.MsgName.CreateGuildRsp, GuildService.CreateGuildRsp)
```

---

## GL/GuildSupplyWindow.lua.lua
**Functions:**
- GuildSupplyWindow.OnInit
- GuildSupplyWindow.GetData
- GuildSupplyWindow.Init
- GuildSupplyWindow.InitBtn
- GuildSupplyWindow.HandleMessage
- GuildSupplyWindow.OnClose
**Requires:**
- GuildSupply_GuildSupplyWindowByName
**Snippet:**
```lua
require("GuildSupply_GuildSupplyWindowByName")
local GuildSupplyWindow = {}
local uis, contentPane, supplyData, index, listIndex, jumpTb

function GuildSupplyWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.GuildSupplyWindow.package, WinResConfig.GuildSupplyWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetGuildSupply_GuildSupplyWindowUis(contentPane)
    uis.Main.BackGround.BackGroundLoader.url = UIUtil.GetBackgroundUrl(FEATURE_ENUM.GUILD_SIGN_IN)
```

---

## GL/GuildSupply_GuildSupplyByName.lua.lua
**Functions:**
- GetGuildSupply_GuildSupplyUis
**Requires:**
- CommonResource_BackGroundByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("CommonResource_CurrencyReturnByName")

function GetGuildSupply_GuildSupplyUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.CurrencyReturn = GetCommonResource_CurrencyReturnUis(ui:GetChild("CurrencyReturn"))
  uis.root = ui
  return uis
```

---

## GL/GuildSupply_GuildSupplyWindowByName.lua.lua
**Functions:**
- GetGuildSupply_GuildSupplyWindowUis
**Requires:**
- GuildSupply_GuildSupplyByName
**Snippet:**
```lua
require("GuildSupply_GuildSupplyByName")

function GetGuildSupply_GuildSupplyWindowUis(ui)
  local uis = {}
  uis.Main = GetGuildSupply_GuildSupplyUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildSupply_ItemByName.lua.lua
**Functions:**
- GetGuildSupply_ItemUis
**Snippet:**
```lua
function GetGuildSupply_ItemUis(ui)
  local uis = {}
  
  uis.IconLoader = ui:GetChild("IconLoader")
  uis.root = ui
  return uis
end
```

---

## GL/GuildSupply_QualityByName.lua.lua
**Functions:**
- GetGuildSupply_QualityUis
**Snippet:**
```lua
function GetGuildSupply_QualityUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/GuildSupply_Tips1ByName.lua.lua
**Functions:**
- GetGuildSupply_Tips1Uis
**Requires:**
- GuildSupply_ItemByName
- GuildSupply_QualityByName
**Snippet:**
```lua
require("GuildSupply_ItemByName")
require("GuildSupply_QualityByName")

function GetGuildSupply_Tips1Uis(ui)
  local uis = {}
  uis.OrderTxt = ui:GetChild("OrderTxt")
  uis.DayTxt = ui:GetChild("DayTxt")
  uis.Item = GetGuildSupply_ItemUis(ui:GetChild("Item"))
  uis.Quality = GetGuildSupply_QualityUis(ui:GetChild("Quality"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
```

---

## GL/GuildSupply_Tips2ByName.lua.lua
**Functions:**
- GetGuildSupply_Tips2Uis
**Requires:**
- GuildSupply_ItemByName
- GuildSupply_QualityByName
**Snippet:**
```lua
require("GuildSupply_ItemByName")
require("GuildSupply_QualityByName")

function GetGuildSupply_Tips2Uis(ui)
  local uis = {}
  uis.OrderTxt = ui:GetChild("OrderTxt")
  uis.DayTxt = ui:GetChild("DayTxt")
  uis.Item = GetGuildSupply_ItemUis(ui:GetChild("Item"))
  uis.Quality = GetGuildSupply_QualityUis(ui:GetChild("Quality"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
```

---

## GL/GuildSupply_Tips3ByName.lua.lua
**Functions:**
- GetGuildSupply_Tips3Uis
**Requires:**
- GuildSupply_ItemByName
- GuildSupply_QualityByName
**Snippet:**
```lua
require("GuildSupply_ItemByName")
require("GuildSupply_QualityByName")

function GetGuildSupply_Tips3Uis(ui)
  local uis = {}
  uis.OrderTxt = ui:GetChild("OrderTxt")
  uis.DayTxt = ui:GetChild("DayTxt")
  uis.Item = GetGuildSupply_ItemUis(ui:GetChild("Item"))
  uis.Quality = GetGuildSupply_QualityUis(ui:GetChild("Quality"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
```

---

## GL/GuildSupply_Tips4ByName.lua.lua
**Functions:**
- GetGuildSupply_Tips4Uis
**Requires:**
- GuildSupply_ItemByName
- GuildSupply_QualityByName
**Snippet:**
```lua
require("GuildSupply_ItemByName")
require("GuildSupply_QualityByName")

function GetGuildSupply_Tips4Uis(ui)
  local uis = {}
  uis.OrderTxt = ui:GetChild("OrderTxt")
  uis.DayTxt = ui:GetChild("DayTxt")
  uis.Item = GetGuildSupply_ItemUis(ui:GetChild("Item"))
  uis.Quality = GetGuildSupply_QualityUis(ui:GetChild("Quality"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
```

---

## GL/GuildSupply_Tips5ByName.lua.lua
**Functions:**
- GetGuildSupply_Tips5Uis
**Requires:**
- GuildSupply_ItemByName
- GuildSupply_QualityByName
**Snippet:**
```lua
require("GuildSupply_ItemByName")
require("GuildSupply_QualityByName")

function GetGuildSupply_Tips5Uis(ui)
  local uis = {}
  uis.OrderTxt = ui:GetChild("OrderTxt")
  uis.DayTxt = ui:GetChild("DayTxt")
  uis.Item = GetGuildSupply_ItemUis(ui:GetChild("Item"))
  uis.Quality = GetGuildSupply_QualityUis(ui:GetChild("Quality"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
```

---

## GL/GuildSupply_Tips6ByName.lua.lua
**Functions:**
- GetGuildSupply_Tips6Uis
**Requires:**
- GuildSupply_ItemByName
- GuildSupply_QualityByName
**Snippet:**
```lua
require("GuildSupply_ItemByName")
require("GuildSupply_QualityByName")

function GetGuildSupply_Tips6Uis(ui)
  local uis = {}
  uis.OrderTxt = ui:GetChild("OrderTxt")
  uis.DayTxt = ui:GetChild("DayTxt")
  uis.Item = GetGuildSupply_ItemUis(ui:GetChild("Item"))
  uis.Quality = GetGuildSupply_QualityUis(ui:GetChild("Quality"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
```

---

## GL/GuildSupply_Tips7ByName.lua.lua
**Functions:**
- GetGuildSupply_Tips7Uis
**Requires:**
- GuildSupply_ItemByName
- GuildSupply_QualityByName
**Snippet:**
```lua
require("GuildSupply_ItemByName")
require("GuildSupply_QualityByName")

function GetGuildSupply_Tips7Uis(ui)
  local uis = {}
  uis.OrderTxt = ui:GetChild("OrderTxt")
  uis.DayTxt = ui:GetChild("DayTxt")
  uis.Item = GetGuildSupply_ItemUis(ui:GetChild("Item"))
  uis.Quality = GetGuildSupply_QualityUis(ui:GetChild("Quality"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
```

---

## GL/GuildTrainWindow.lua.lua
**Functions:**
- GuildTrainWindow.ReInitData
- GuildTrainWindow.OnInit
- GuildTrainWindow.UpdateInfo
- rankInfo.ElementList.itemRenderer
- GuildTrainWindow.ShowStage
- GuildTrainWindow.UpdateRankList
- rankInfo.RankList.itemRenderer
- GuildTrainWindow.StopAnim
- GuildTrainWindow.GetChapterData
- GuildTrainWindow.GetSelfRankData
- GuildTrainWindow.SufficientQuantity
- GuildTrainWindow.InitBtn
- GuildTrainWindow.OnClose
- GuildTrainWindow.HandleMessage
**Requires:**
- GuildTrain_GuildTrainWindowByName
**Snippet:**
```lua
require("GuildTrain_GuildTrainWindowByName")
local GuildTrainWindow = {}
local uis, contentPane, jumpTb, curType, curStageId, curPage, stagePage, isPlay, first, animTran

function GuildTrainWindow.ReInitData()
end

function GuildTrainWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.GuildTrainWindow.package, WinResConfig.GuildTrainWindow.comName, function(com)
    contentPane = com
```

---

## GL/GuildTrain_BattleLatticeByName.lua.lua
**Functions:**
- GetGuildTrain_BattleLatticeUis
**Snippet:**
```lua
function GetGuildTrain_BattleLatticeUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_BurstOccupationByName.lua.lua
**Functions:**
- GetGuildTrain_BurstOccupationUis
**Snippet:**
```lua
function GetGuildTrain_BurstOccupationUis(ui)
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

## GL/GuildTrain_BurstStripByName.lua.lua
**Functions:**
- GetGuildTrain_BurstStripUis
**Requires:**
- GuildTrain_LeaderHeadByName
- GuildTrain_BurstStripTipsByName
**Snippet:**
```lua
require("GuildTrain_LeaderHeadByName")
require("GuildTrain_BurstStripTipsByName")

function GetGuildTrain_BurstStripUis(ui)
  local uis = {}
  uis.LeaderHead = GetGuildTrain_LeaderHeadUis(ui:GetChild("LeaderHead"))
  uis.OccupationList = ui:GetChild("OccupationList")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.BurstStripTips = GetGuildTrain_BurstStripTipsUis(ui:GetChild("BurstStripTips"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## GL/GuildTrain_BurstStripTipsByName.lua.lua
**Functions:**
- GetGuildTrain_BurstStripTipsUis
**Snippet:**
```lua
function GetGuildTrain_BurstStripTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_CardHeadBgByName.lua.lua
**Functions:**
- GetGuildTrain_CardHeadBgUis
**Snippet:**
```lua
function GetGuildTrain_CardHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_CardHeadByName.lua.lua
**Functions:**
- GetGuildTrain_CardHeadUis
**Requires:**
- GuildTrain_CardHeadBgByName
- CommonResource_OccupationByName
- CommonResource_CardBreachByName
**Snippet:**
```lua
require("GuildTrain_CardHeadBgByName")
require("CommonResource_OccupationByName")
require("CommonResource_CardBreachByName")

function GetGuildTrain_CardHeadUis(ui)
  local uis = {}
  uis.PicMask = GetGuildTrain_CardHeadBgUis(ui:GetChild("PicMask"))
  uis.Occupation = GetCommonResource_OccupationUis(ui:GetChild("Occupation"))
  uis.ElementList = ui:GetChild("ElementList")
  uis.StarList = ui:GetChild("StarList")
```

---

## GL/GuildTrain_CardHeadTipsBtnByName.lua.lua
**Functions:**
- GetGuildTrain_CardHeadTipsBtnUis
**Requires:**
- GuildTrain_CardHeadByName
**Snippet:**
```lua
require("GuildTrain_CardHeadByName")

function GetGuildTrain_CardHeadTipsBtnUis(ui)
  local uis = {}
  uis.CardHead = GetGuildTrain_CardHeadUis(ui:GetChild("CardHead"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.DamageProgressBar = ui:GetChild("DamageProgressBar")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
```

---

## GL/GuildTrain_CardInfoLeftByName.lua.lua
**Functions:**
- GetGuildTrain_CardInfoLeftUis
**Requires:**
- CommonResource_OccupationByName
**Snippet:**
```lua
require("CommonResource_OccupationByName")

function GetGuildTrain_CardInfoLeftUis(ui)
  local uis = {}
  uis.CardHolder = ui:GetChild("CardHolder")
  uis.Occupation = GetCommonResource_OccupationUis(ui:GetChild("Occupation"))
  uis.ElementList = ui:GetChild("ElementList")
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_DamageProgressBarByName.lua.lua
**Functions:**
- GetGuildTrain_DamageProgressBarUis
**Requires:**
- GuildTrain_DamageProgressFillByName
**Snippet:**
```lua
require("GuildTrain_DamageProgressFillByName")

function GetGuildTrain_DamageProgressBarUis(ui)
  local uis = {}
  uis.bar = GetGuildTrain_DamageProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_DamageProgressFillByName.lua.lua
**Functions:**
- GetGuildTrain_DamageProgressFillUis
**Snippet:**
```lua
function GetGuildTrain_DamageProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_ElementTabBgByName.lua.lua
**Functions:**
- GetGuildTrain_ElementTabBgUis
**Snippet:**
```lua
function GetGuildTrain_ElementTabBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_ElementTabBtnByName.lua.lua
**Functions:**
- GetGuildTrain_ElementTabBtnUis
**Requires:**
- GuildTrain_ElementTabBgByName
**Snippet:**
```lua
require("GuildTrain_ElementTabBgByName")

function GetGuildTrain_ElementTabBtnUis(ui)
  local uis = {}
  uis.ElementTabBg = GetGuildTrain_ElementTabBgUis(ui:GetChild("ElementTabBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## GL/GuildTrain_FormationGridByName.lua.lua
**Functions:**
- GetGuildTrain_FormationGridUis
**Snippet:**
```lua
function GetGuildTrain_FormationGridUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_FormationGridCenterByName.lua.lua
**Functions:**
- GetGuildTrain_FormationGridCenterUis
**Snippet:**
```lua
function GetGuildTrain_FormationGridCenterUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_FormationGridEdgeByName.lua.lua
**Functions:**
- GetGuildTrain_FormationGridEdgeUis
**Snippet:**
```lua
function GetGuildTrain_FormationGridEdgeUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_FormationGridEdgeVerByName.lua.lua
**Functions:**
- GetGuildTrain_FormationGridEdgeVerUis
**Snippet:**
```lua
function GetGuildTrain_FormationGridEdgeVerUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_FormationGridLineByName.lua.lua
**Functions:**
- GetGuildTrain_FormationGridLineUis
**Requires:**
- GuildTrain_FormationGridCenterByName
- GuildTrain_FormationGridEdgeByName
- GuildTrain_FormationGridEdgeVerByName
**Snippet:**
```lua
require("GuildTrain_FormationGridCenterByName")
require("GuildTrain_FormationGridEdgeByName")
require("GuildTrain_FormationGridEdgeVerByName")

function GetGuildTrain_FormationGridLineUis(ui)
  local uis = {}
  uis.Center = GetGuildTrain_FormationGridCenterUis(ui:GetChild("Center"))
  uis.Top = GetGuildTrain_FormationGridEdgeUis(ui:GetChild("Top"))
  uis.Down = GetGuildTrain_FormationGridEdgeUis(ui:GetChild("Down"))
  uis.Left = GetGuildTrain_FormationGridEdgeVerUis(ui:GetChild("Left"))
```

---

## GL/GuildTrain_GuildTrainByName.lua.lua
**Functions:**
- GetGuildTrain_GuildTrainUis
**Requires:**
- CommonResource_BackGroundByName
- GuildTrain_RankRegionByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("GuildTrain_RankRegionByName")
require("CommonResource_CurrencyReturnByName")

function GetGuildTrain_GuildTrainUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.RankRegion = GetGuildTrain_RankRegionUis(ui:GetChild("RankRegion"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.TrainStartBtn = ui:GetChild("TrainStartBtn")
```

---

## GL/GuildTrain_GuildTrainWindowByName.lua.lua
**Functions:**
- GetGuildTrain_GuildTrainWindowUis
**Requires:**
- GuildTrain_GuildTrainByName
**Snippet:**
```lua
require("GuildTrain_GuildTrainByName")

function GetGuildTrain_GuildTrainWindowUis(ui)
  local uis = {}
  uis.Main = GetGuildTrain_GuildTrainUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_LeaderHeadBgByName.lua.lua
**Functions:**
- GetGuildTrain_LeaderHeadBgUis
**Snippet:**
```lua
function GetGuildTrain_LeaderHeadBgUis(ui)
  local uis = {}
  
  uis.HeadLoader = ui:GetChild("HeadLoader")
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_LeaderHeadByName.lua.lua
**Functions:**
- GetGuildTrain_LeaderHeadUis
**Requires:**
- GuildTrain_LeaderHeadBgByName
**Snippet:**
```lua
require("GuildTrain_LeaderHeadBgByName")

function GetGuildTrain_LeaderHeadUis(ui)
  local uis = {}
  uis.LeaderHeadBg = GetGuildTrain_LeaderHeadBgUis(ui:GetChild("LeaderHeadBg"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_PlaceLatticeByName.lua.lua
**Functions:**
- GetGuildTrain_PlaceLatticeUis
**Snippet:**
```lua
function GetGuildTrain_PlaceLatticeUis(ui)
  local uis = {}
  
  uis.PlaceEnableHolder = ui:GetChild("PlaceEnableHolder")
  uis.PlaceUnableHolder = ui:GetChild("PlaceUnableHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_RangeLatticeByName.lua.lua
**Functions:**
- GetGuildTrain_RangeLatticeUis
**Snippet:**
```lua
function GetGuildTrain_RangeLatticeUis(ui)
  local uis = {}
  
  uis.RangeHolder = ui:GetChild("RangeHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_RankNumberByName.lua.lua
**Functions:**
- GetGuildTrain_RankNumberUis
**Snippet:**
```lua
function GetGuildTrain_RankNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_RankOwnPlayerByName.lua.lua
**Functions:**
- GetGuildTrain_RankOwnPlayerUis
**Requires:**
- GuildTrain_RankNumberByName
- CommonResource_HeadByName
**Snippet:**
```lua
require("GuildTrain_RankNumberByName")
require("CommonResource_HeadByName")

function GetGuildTrain_RankOwnPlayerUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.RankNumber = GetGuildTrain_RankNumberUis(ui:GetChild("RankNumber"))
  uis.LookBtn = ui:GetChild("LookBtn")
  uis.Head = GetCommonResource_HeadUis(ui:GetChild("Head"))
```

---

## GL/GuildTrain_RankOwnPlayerLookBtnByName.lua.lua
**Functions:**
- GetGuildTrain_RankOwnPlayerLookBtnUis
**Snippet:**
```lua
function GetGuildTrain_RankOwnPlayerLookBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_RankPlayerAniByName.lua.lua
**Functions:**
- GetGuildTrain_RankPlayerAniUis
**Requires:**
- GuildTrain_RankPlayerByName
**Snippet:**
```lua
require("GuildTrain_RankPlayerByName")

function GetGuildTrain_RankPlayerAniUis(ui)
  local uis = {}
  uis.RankPlayer = GetGuildTrain_RankPlayerUis(ui:GetChild("RankPlayer"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_RankPlayerByName.lua.lua
**Functions:**
- GetGuildTrain_RankPlayerUis
**Requires:**
- GuildTrain_RankNumberByName
- CommonResource_HeadByName
**Snippet:**
```lua
require("GuildTrain_RankNumberByName")
require("CommonResource_HeadByName")

function GetGuildTrain_RankPlayerUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.RankNumber = GetGuildTrain_RankNumberUis(ui:GetChild("RankNumber"))
  uis.Head = GetCommonResource_HeadUis(ui:GetChild("Head"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## GL/GuildTrain_RankRegionByName.lua.lua
**Functions:**
- GetGuildTrain_RankRegionUis
**Requires:**
- GuildTrain_RankOwnPlayerByName
**Snippet:**
```lua
require("GuildTrain_RankOwnPlayerByName")

function GetGuildTrain_RankRegionUis(ui)
  local uis = {}
  uis.Time90Btn = ui:GetChild("Time90Btn")
  uis.Time180Btn = ui:GetChild("Time180Btn")
  uis.RankList = ui:GetChild("RankList")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.RankOwnPlayer = GetGuildTrain_RankOwnPlayerUis(ui:GetChild("RankOwnPlayer"))
  uis.ElementList = ui:GetChild("ElementList")
```

---

## GL/GuildTrain_TargetLatticeByName.lua.lua
**Functions:**
- GetGuildTrain_TargetLatticeUis
**Snippet:**
```lua
function GetGuildTrain_TargetLatticeUis(ui)
  local uis = {}
  
  uis.TargetHolder = ui:GetChild("TargetHolder")
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_TeamDetailsByName.lua.lua
**Functions:**
- GetGuildTrain_TeamDetailsUis
**Requires:**
- CommonResource_BackGroundByName
- GuildTrain_TotalDamageByName
- GuildTrain_TotalTimeByName
- GuildTrain_FormationGridLineByName
- GuildTrain_BurstStripByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("GuildTrain_TotalDamageByName")
require("GuildTrain_TotalTimeByName")
require("GuildTrain_FormationGridLineByName")
require("GuildTrain_BurstStripByName")
require("CommonResource_CurrencyReturnByName")

function GetGuildTrain_TeamDetailsUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
```

---

## GL/GuildTrain_TeamDetailsWindowByName.lua.lua
**Functions:**
- GetGuildTrain_TeamDetailsWindowUis
**Requires:**
- GuildTrain_TeamDetailsByName
**Snippet:**
```lua
require("GuildTrain_TeamDetailsByName")

function GetGuildTrain_TeamDetailsWindowUis(ui)
  local uis = {}
  uis.Main = GetGuildTrain_TeamDetailsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_TimeTab1BtnByName.lua.lua
**Functions:**
- GetGuildTrain_TimeTab1BtnUis
**Requires:**
- GuildTrain_TimeTabDown1ByName
- GuildTrain_TimeTabUp1ByName
- GuildTrain_TimeTabBg1ByName
**Snippet:**
```lua
require("GuildTrain_TimeTabDown1ByName")
require("GuildTrain_TimeTabUp1ByName")
require("GuildTrain_TimeTabBg1ByName")

function GetGuildTrain_TimeTab1BtnUis(ui)
  local uis = {}
  uis.Down = GetGuildTrain_TimeTabDown1Uis(ui:GetChild("Down"))
  uis.Up = GetGuildTrain_TimeTabUp1Uis(ui:GetChild("Up"))
  uis.TimeTabBg = GetGuildTrain_TimeTabBg1Uis(ui:GetChild("TimeTabBg"))
  uis.buttonCtr = ui:GetController("button")
```

---

## GL/GuildTrain_TimeTabBg1ByName.lua.lua
**Functions:**
- GetGuildTrain_TimeTabBg1Uis
**Snippet:**
```lua
function GetGuildTrain_TimeTabBg1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_TimeTabBgByName.lua.lua
**Functions:**
- GetGuildTrain_TimeTabBgUis
**Snippet:**
```lua
function GetGuildTrain_TimeTabBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_TimeTabBtnByName.lua.lua
**Functions:**
- GetGuildTrain_TimeTabBtnUis
**Requires:**
- GuildTrain_TimeTabDownByName
- GuildTrain_TimeTabUpByName
- GuildTrain_TimeTabBgByName
**Snippet:**
```lua
require("GuildTrain_TimeTabDownByName")
require("GuildTrain_TimeTabUpByName")
require("GuildTrain_TimeTabBgByName")

function GetGuildTrain_TimeTabBtnUis(ui)
  local uis = {}
  uis.Down = GetGuildTrain_TimeTabDownUis(ui:GetChild("Down"))
  uis.Up = GetGuildTrain_TimeTabUpUis(ui:GetChild("Up"))
  uis.TimeTabBg = GetGuildTrain_TimeTabBgUis(ui:GetChild("TimeTabBg"))
  uis.buttonCtr = ui:GetController("button")
```

---

## GL/GuildTrain_TimeTabDown1ByName.lua.lua
**Functions:**
- GetGuildTrain_TimeTabDown1Uis
**Snippet:**
```lua
function GetGuildTrain_TimeTabDown1Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_TimeTabDownByName.lua.lua
**Functions:**
- GetGuildTrain_TimeTabDownUis
**Snippet:**
```lua
function GetGuildTrain_TimeTabDownUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_TimeTabUp1ByName.lua.lua
**Functions:**
- GetGuildTrain_TimeTabUp1Uis
**Snippet:**
```lua
function GetGuildTrain_TimeTabUp1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_TimeTabUpByName.lua.lua
**Functions:**
- GetGuildTrain_TimeTabUpUis
**Snippet:**
```lua
function GetGuildTrain_TimeTabUpUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_TotalDamageByName.lua.lua
**Functions:**
- GetGuildTrain_TotalDamageUis
**Snippet:**
```lua
function GetGuildTrain_TotalDamageUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_TotalTimeByName.lua.lua
**Functions:**
- GetGuildTrain_TotalTimeUis
**Snippet:**
```lua
function GetGuildTrain_TotalTimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## GL/GuildTrain_TrainStartBtnByName.lua.lua
**Functions:**
- GetGuildTrain_TrainStartBtnUis
**Snippet:**
```lua
function GetGuildTrain_TrainStartBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/GuildVoteWindow.lua.lua
**Functions:**
- GuildVoteWindow.OnInit
- GuildVoteWindow.UpdateTextDisplay
- GuildVoteWindow.RefreshUI
- GuildVoteWindow.GetVoteName
- GuildVoteWindow.CloseWindow
- GuildVoteWindow.InitBtn
- GuildVoteWindow.HandleMessage
- GuildVoteWindow.StopTime
- GuildVoteWindow.OnClose
**Requires:**
- Guild_VoteWindowByName
**Snippet:**
```lua
require("Guild_VoteWindowByName")
local GuildVoteWindow = {}
local uis, contentPane, timeInfo

function GuildVoteWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.GuildVoteWindow.package, WinResConfig.GuildVoteWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetGuild_VoteWindowUis(contentPane)
    GuildVoteWindow.UpdateTextDisplay()
```

---

## GL/GuildWarBossTaskWindow.lua.lua
**Functions:**
- GuildWarBossTaskWindow.ReInitData
- GuildWarBossTaskWindow.OnInit
- GuildWarBossTaskWindow.UpdateInfo
- list.itemRenderer
- GuildWarBossTaskWindow.GetRewardNum
- GuildWarBossTaskWindow.ShowWordList
- list.itemRenderer
- GuildWarBossTaskWindow.InitBtn
- GuildWarBossTaskWindow.OnClose
**Requires:**
- GuildBoss_GuildBossTaskWindowByName
**Snippet:**
```lua
require("GuildBoss_GuildBossTaskWindowByName")
local GuildWarBossTaskWindow = {}
local uis, contentPane

function GuildWarBossTaskWindow.ReInitData()
end

function GuildWarBossTaskWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.GuildWarBossTaskWindow.package, WinResConfig.GuildWarBossTaskWindow.comName, function(com)
    contentPane = com
```

---

## GL/GuildWarCardAssistWindow.lua.lua
**Functions:**
- GuildWarCardAssistWindow.ReInitData
- GuildWarCardAssistWindow.OnInit
- GuildWarCardAssistWindow.UpdateInfo
- uis.Main.TipsList.itemRenderer
- GuildWarCardAssistWindow.InitBtn
- GuildWarCardAssistWindow.OnShown
- GuildWarCardAssistWindow.OnClose
**Requires:**
- GuildBoss_GuildCardAssistWindowByName
**Snippet:**
```lua
require("GuildBoss_GuildCardAssistWindowByName")
local GuildWarCardAssistWindow = {}
local uis, contentPane, max, info

function GuildWarCardAssistWindow.ReInitData()
end

function GuildWarCardAssistWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.GuildWarCardAssistWindow.package, WinResConfig.GuildWarCardAssistWindow.comName, function(com)
    contentPane = com
```

---

## GL/GuildWarCompensateWindow.lua.lua
**Functions:**
- GuildWarCompensateWindow.ReInitData
- GuildWarCompensateWindow.OnInit
- GuildWarCompensateWindow.UpdateInfo
- GuildWarCompensateWindow.UpdateList
- list.itemRenderer
- headList.itemRenderer
- GuildWarCompensateWindow.CompensateBattle
- GuildWarCompensateWindow.GetCardList
- GuildWarCompensateWindow.TouchNormalBattle
- GuildWarCompensateWindow.TouchClose
- GuildWarCompensateWindow.InitBtn
- GuildWarCompensateWindow.OnClose
**Requires:**
- GuildBoss_GuildCompensateWindowByName
**Snippet:**
```lua
require("GuildBoss_GuildCompensateWindowByName")
local GuildWarCompensateWindow = {}
local uis, contentPane, formations, simulated, stageId

function GuildWarCompensateWindow.ReInitData()
end

function GuildWarCompensateWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.GuildWarCompensateWindow.package, WinResConfig.GuildWarCompensateWindow.comName, function(com)
    contentPane = com
```

---

## GL/GuildWarData.lua.lua
**Snippet:**
```lua
local scheduleInfo, progressInfo, playerInfo, guildWarConfig, warRankInfo, taskInfo, battleRecord
local cachedBattleDetailRecord = {}
local challengeStageRsp
local SetGuildScheduleInfo = function(info)
  scheduleInfo = info
  if info then
    local guildData = TableData.GetTable("BaseGuildWar")
    for i, v in pairs(guildData) do
      if v.phase == info.phase then
        guildWarConfig = v
```

---

## GL/GuildWarEditTeamWindow.lua.lua
**Functions:**
- GuildWarEditTeamWindow.ReInitData
- GuildWarEditTeamWindow.OnInit
- GuildWarEditTeamWindow.IsSameCardType
- GuildWarEditTeamWindow.GetCardList
- GuildWarEditTeamWindow.UpdateInfo
- GuildWarEditTeamWindow.GetTeamEndCardId
- GuildWarEditTeamWindow.UpdateOccupationRegion
- GuildWarEditTeamWindow.UpdateTeamList
- GuildWarEditTeamWindow.GetTeamCardLimitNum
- GuildWarEditTeamWindow.UpdateCardNum
- GuildWarEditTeamWindow.UpdateCardDetail
- GuildWarEditTeamWindow.RefreshCard
- GuildWarEditTeamWindow.UpdateAllIndex
- GuildWarEditTeamWindow.UpdateInTeamIndex
- GuildWarEditTeamWindow.InitBtn
- GuildWarEditTeamWindow.ClickCancelBtn
- GuildWarEditTeamWindow.ClickSureBtn
- GuildWarEditTeamWindow.UpdateCardInfoList
- GuildWarEditTeamWindow.OnShown
- GuildWarEditTeamWindow.OnClose
**Requires:**
- TeamCardChoice_EditTeamWindowByName
**Snippet:**
```lua
require("TeamCardChoice_EditTeamWindowByName")
local GuildWarEditTeamWindow = {}
local uis, contentPane
local curCardInfoList = {}
local selectCardType
local tempTeamInfo = {}
local lastSelectCardId, jumpTb, curCardId, playAnim

function GuildWarEditTeamWindow.ReInitData()
end
```

---

## GL/GuildWarLevelDetailInfoWindow.lua.lua
**Functions:**
- GuildWarLevelDetailInfoWindow.ReInitData
- GuildWarLevelDetailInfoWindow.OnInit
- GuildWarLevelDetailInfoWindow.UpdateInfo
- skilllist.itemRenderer
- wordlist.itemRenderer
- GuildWarLevelDetailInfoWindow.InitBtn
- GuildWarLevelDetailInfoWindow.OnShown
- GuildWarLevelDetailInfoWindow.OnClose
- GuildWarLevelDetailInfoWindow.HandleMessage
**Requires:**
- GuildBoss_DungeonInfoWindowByName
**Snippet:**
```lua
require("GuildBoss_DungeonInfoWindowByName")
local GuildWarLevelDetailInfoWindow = {}
local uis, contentPane, conf
local RefreshChallengeCount = function()
  local panel = uis.Main.DungeonInfoTips
  local fightCnt = GuildWarData.GetGuildPlayerInfo().fightCount
  local maxFightCnt = TableData.GetConfig(70011405, "BaseFixed").int_value
  local remainFightCnt = maxFightCnt - fightCnt
  panel.BattleNumber.WordTxt.text = T(11702, remainFightCnt, maxFightCnt)
end
```

---

## GL/GuildWarLevelSelectedWindow.lua.lua
**Functions:**
- GuildWarLevelSelectedWindow.ReInitData
- GuildWarLevelSelectedWindow.OnInit
- GuildWarLevelSelectedWindow.UpdateInfo
- GuildWarLevelSelectedWindow.InitBtn
- GuildWarLevelSelectedWindow.OnClose
- GuildWarLevelSelectedWindow.HandleMessage
**Requires:**
- GuildBoss_BossBattleWindowByName
**Snippet:**
```lua
require("GuildBoss_BossBattleWindowByName")
local GuildWarLevelSelectedWindow = {}
local uis, contentPane, timer, timer2, delayTween
local GetOrCreateHolder = function(root, name)
  local holder = root:GetChild(name)
  if not holder then
    holder = FairyGUI.UIObjectFactory.NewObject(FairyGUI.ObjectType.Graph)
    holder.name = name
    holder.pivotAsAnchor = true
    holder:SetPivot(0.5, 0.5)
```

---

## GL/GuildWarMainWindow.lua.lua
**Functions:**
- GuildWarMainWindow.ReInitData
- GuildWarMainWindow.OnInit
- GuildWarMainWindow.UpdateInfo
- GuildWarMainWindow.InitBtn
- GuildWarMainWindow.InitRedDot
- GuildWarMainWindow.OnShown
- GuildWarMainWindow.UpdateRank
- GuildWarMainWindow.OnHide
- GuildWarMainWindow.OnClose
**Requires:**
- GuildBoss_GuildBossWindowByName
**Snippet:**
```lua
require("GuildBoss_GuildBossWindowByName")
local GuildWarMainWindow = {}
local uis, contentPane, prevMapId
local RefreshPanelInfo = function()
  local title = uis.Main.Title
  title.NameTxt.text = GuildData.GuildInfo.info.name
  local level = GuildData.GuildInfo.info.level
  local data = TableData.GetConfig(GuildEnum.GUILD_LEVEL_UP_ID * 10 + level, "BaseGuildLevelUp")
  if data then
    title.NumberTxt.text = T(20504, GuildData.GuildInfo.info.memberCount, data.max_member)
```

---

## GL/GuildWarMgr.lua.lua
**Functions:**
- GuildWarMgr.OpenGuildWarWindow
- GuildWarMgr.PrepareEnterBattle
- GuildWarMgr.OnBattleComplete
- GuildWarMgr.IsFightCountEnough
- GuildWarMgr.SetFontSize
- GuildWarMgr.GetRound
- GuildWarMgr.GetMinRound
- GuildWarMgr.GetBossIndex
**Snippet:**
```lua
GuildWarMgr = {}

function GuildWarMgr.OpenGuildWarWindow()
  GuildWarService.GetGuildWarScheduleReq(function(msg)
    if msg.inGuild then
      ld("Guild")
      GuildService.GetMyGuildSimpleInfoReq()
      local state = msg.schedule.state
      if state == ProtoEnum.GuildWarState.GWS_NOTICE then
        OpenWindow(WinResConfig.GuildBossPreviewWindow.name)
```

---

## GL/GuildWarRankRewardWindow.lua.lua
**Functions:**
- GuildWarRankRewardWindow.ReInitData
- GuildWarRankRewardWindow.OnInit
- GuildWarRankRewardWindow.UpdateInfo
- list.itemRenderer
- GuildWarRankRewardWindow.ShowRewardIcon
- list.itemRenderer
- GuildWarRankRewardWindow.GetRewardData
- GuildWarRankRewardWindow.InitBtn
- GuildWarRankRewardWindow.OnClose
**Requires:**
- GuildBoss_GuildRankRewardWindowByName
**Snippet:**
```lua
require("GuildBoss_GuildRankRewardWindowByName")
local GuildWarRankRewardWindow = {}
local uis, contentPane

function GuildWarRankRewardWindow.ReInitData()
end

function GuildWarRankRewardWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.GuildWarRankRewardWindow.package, WinResConfig.GuildWarRankRewardWindow.comName, function(com)
    contentPane = com
```

---

## GL/GuildWarRankWindow.lua.lua
**Functions:**
- GuildWarRankWindow.ReInitData
- GuildWarRankWindow.OnInit
- GuildWarRankWindow.ShowGuildList
- GuildWarRankWindow.ShowCardList
- GuildWarRankWindow.GuildRankRenderer
- GuildWarRankWindow.CardRankRenderer
- GuildWarRankWindow.GetChildSlefData
- GuildWarRankWindow.ShowInfo
- GuildWarRankWindow.InitBtn
- GuildWarRankWindow.OnClose
**Requires:**
- GuildBoss_GuildRankWindowByName
**Snippet:**
```lua
require("GuildBoss_GuildRankWindowByName")
local GuildWarRankWindow = {}
local uis, contentPane, rankInfo, guildPlayAnim, cardPlayAnim, myRank, showType

function GuildWarRankWindow.ReInitData()
end

function GuildWarRankWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.GuildWarRankWindow.package, WinResConfig.GuildWarRankWindow.comName, function(com)
    contentPane = com
```

---

## GL/GuildWarRecommendScreenWindow.lua.lua
**Functions:**
- GuildWarRecommendScreenWindow.ReInitData
- GuildWarRecommendScreenWindow.OnInit
- GuildWarRecommendScreenWindow.InitText
- GuildWarRecommendScreenWindow.UpdateInfo
- GuildWarRecommendScreenWindow.GetFilterCardList
- GuildWarRecommendScreenWindow.UpdateAllCards
- cardList.itemRenderer
- GuildWarRecommendScreenWindow.UpdateSelectCards
- screenList.itemRenderer
- GuildWarRecommendScreenWindow.InitBtn
- GuildWarRecommendScreenWindow.OnClose
**Requires:**
- GuildBoss_RecommendScreenWindowByName
**Snippet:**
```lua
require("GuildBoss_RecommendScreenWindowByName")
local GuildWarRecommendScreenWindow = {}
local uis, contentPane
local filterCardIdList = {}

function GuildWarRecommendScreenWindow.ReInitData()
end

function GuildWarRecommendScreenWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.GuildWarRecommendScreenWindow.package, WinResConfig.GuildWarRecommendScreenWindow.comName, function(com)
```

---

## GL/GuildWarRecommendWindow.lua.lua
**Functions:**
- GuildWarRecommendWindow.ReInitData
- GuildWarRecommendWindow.OnInit
- GuildWarRecommendWindow.GetFilterFormations
- GuildWarRecommendWindow.UpdateInfo
- GuildWarRecommendWindow.InitBtn
- GuildWarRecommendWindow.UpdateList
- list.itemRenderer
- headList.itemRenderer
- skillList.itemRenderer
- GuildWarRecommendWindow.TouchUseFormation
- GuildWarRecommendWindow.TestFormationCardAvailable
- GuildWarRecommendWindow.GetCardList
- GuildWarRecommendWindow.OnClose
- GuildWarRecommendWindow.HandleMessage
**Requires:**
- GuildBoss_RecommendWindowByName
**Snippet:**
```lua
require("GuildBoss_RecommendWindowByName")
local GuildWarRecommendWindow = {}
local uis, contentPane
local filterCardIdList = {}
local stageId

function GuildWarRecommendWindow.ReInitData()
end

function GuildWarRecommendWindow.OnInit(bridgeObj)
```

---

## GL/GuildWarScriptList.lua.lua
**Requires:**
- GuildWarMgr
- GuildWarData
- GuildWarService
**Snippet:**
```lua
local require = require
GuildWarMgr = require("GuildWarMgr")
GuildWarData = require("GuildWarData")
GuildWarService = require("GuildWarService")
```

---

## GL/GuildWarService.lua.lua
**Snippet:**
```lua
local GetGuildWarScheduleReq = function(rspCallback)
  Net.Send(Proto.MsgName.GetGuildWarScheduleReq, nil, rspCallback)
end
local GetGuildWarScheduleRsp = function(msg)
  GuildWarData.SetGuildScheduleInfo(msg.schedule)
end
local GetGuildWarAllInfoReq = function(rspCallback)
  Net.Send(Proto.MsgName.GetGuildWarAllInfoReq, nil, rspCallback)
end
local GetGuildWarAllInfoRsp = function(msg)
```

---

## GL/GuildWarSkillWindow.lua.lua
**Functions:**
- GuildWarSkillWindow.ReInitData
- GuildWarSkillWindow.OnInit
- GuildWarSkillWindow.UpdateInfo
- GuildWarSkillWindow.ShowSkillInfo
- tips.WordList.itemRenderer
- tips.NumberList.itemRenderer
- tips.ProgrammeList.itemRenderer
- effectList.itemRenderer
- GuildWarSkillWindow.UpdateWear
- GuildWarSkillWindow.UpdateLvTxt
- GuildWarSkillWindow.ShowSkillRegion
- list.itemRenderer
- GuildWarSkillWindow.GetAllSkillEffect
- GuildWarSkillWindow.InitBtn
- GuildWarSkillWindow.OnClose
**Requires:**
- GuildBoss_GuildSkillWindowByName
**Snippet:**
```lua
require("GuildBoss_GuildSkillWindowByName")
local GuildWarSkillWindow = {}
local uis, contentPane, lastBtn, teamId

function GuildWarSkillWindow.ReInitData()
end

function GuildWarSkillWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.GuildWarSkillWindow.package, WinResConfig.GuildWarSkillWindow.comName, function(com)
    contentPane = com
```

---

## GL/GuildWindow.lua.lua
**Functions:**
- GuildWindow.OnInit
- GuildWindow.InitRedDot
- GuildWindow.UpdateTextDisplay
- GuildWindow.RefreshGuildPolicy
- GuildWindow.RefreshGuildName
- GuildWindow.RefreshGuildHead
- GuildWindow.ShowNotice
- GuildWindow.InitChat
- GuildWindow.GetGuildWordItemResource
- GuildWindow.UpdateChatText
- GuildWindow.RenderText
- GuildWindow.Init
- GuildWindow.UpdateGuildCondition
- GuildWindow.InputLevelLimit
- GuildWindow.ShowLevelUp
- GuildWindow.ChangeAuditUI
- GuildWindow.GetGuildCaptainData
- GuildWindow.InitMember
- GuildWindow.InitImpeach
- GuildWindow.QuitGuild
- GuildWindow.SetButtonState
- GuildWindow.InitManager
- GuildWindow.GetRenameCost
- GuildWindow.InitPlayerList
- GuildWindow.RefreshPlayerInfoItem
- GuildWindow.StartImpeachSucceed
- GuildWindow.InitBtn
- GuildWindow.UpdateGuild
- GuildWindow.HandleMessage
- GuildWindow.OnClose
**Requires:**
- Guild_GuildWindowByName
**Snippet:**
```lua
require("Guild_GuildWindowByName")
local GuildWindow = {}
local uis, contentPane, listData, timeInfo, allJoin, minLv, maxMember, isRefreshCaptain, showAddBtn, onLineTime, jumpTb, newMessage, LevelTxt, lastLv

function GuildWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.GuildWindow.package, WinResConfig.GuildWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetGuild_GuildWindowUis(contentPane)
    uis.Main.BackGround.BackGroundLoader.url = UIUtil.GetBackgroundUrl(FEATURE_ENUM.HOME_GUILD)
```

---

## GL/Guild_AdoptBtnByName.lua.lua
**Functions:**
- GetGuild_AdoptBtnUis
**Snippet:**
```lua
function GetGuild_AdoptBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_AgreeBtnByName.lua.lua
**Functions:**
- GetGuild_AgreeBtnUis
**Snippet:**
```lua
function GetGuild_AgreeBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_AgreeProgressBarByName.lua.lua
**Functions:**
- GetGuild_AgreeProgressBarUis
**Requires:**
- Guild_AgreeProgressFillByName
**Snippet:**
```lua
require("Guild_AgreeProgressFillByName")

function GetGuild_AgreeProgressBarUis(ui)
  local uis = {}
  uis.bar = GetGuild_AgreeProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## GL/Guild_AgreeProgressFillByName.lua.lua
**Functions:**
- GetGuild_AgreeProgressFillUis
**Snippet:**
```lua
function GetGuild_AgreeProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/Guild_AllAdoptBtnByName.lua.lua
**Functions:**
- GetGuild_AllAdoptBtnUis
**Snippet:**
```lua
function GetGuild_AllAdoptBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_AllRefuseBtnByName.lua.lua
**Functions:**
- GetGuild_AllRefuseBtnUis
**Snippet:**
```lua
function GetGuild_AllRefuseBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_ApplyButtonBtnByName.lua.lua
**Functions:**
- GetGuild_ApplyButtonBtnUis
**Requires:**
- Guild_Time2ByName
**Snippet:**
```lua
require("Guild_Time2ByName")

function GetGuild_ApplyButtonBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Time = GetGuild_Time2Uis(ui:GetChild("Time"))
  uis.buttonAniCtr = ui:GetController("buttonAni")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_BossBtnByName.lua.lua
**Functions:**
- GetGuild_BossBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetGuild_BossBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## GL/Guild_CaptainPicByName.lua.lua
**Functions:**
- GetGuild_CaptainPicUis
**Snippet:**
```lua
function GetGuild_CaptainPicUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_Captain_infoByName.lua.lua
**Functions:**
- GetGuild_Captain_infoUis
**Requires:**
- Guild_CaptainPicByName
- Guild_PositionByName
- Guild_VoteTipsByName
**Snippet:**
```lua
require("Guild_CaptainPicByName")
require("Guild_PositionByName")
require("Guild_VoteTipsByName")

function GetGuild_Captain_infoUis(ui)
  local uis = {}
  uis.CaptainPic = GetGuild_CaptainPicUis(ui:GetChild("CaptainPic"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.Position = GetGuild_PositionUis(ui:GetChild("Position"))
```

---

## GL/Guild_ChatWordLeft1ByName.lua.lua
**Functions:**
- GetGuild_ChatWordLeft1Uis
**Snippet:**
```lua
function GetGuild_ChatWordLeft1Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_ChatWordLeftByName.lua.lua
**Functions:**
- GetGuild_ChatWordLeftUis
**Snippet:**
```lua
function GetGuild_ChatWordLeftUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_ChatWordRegion1ByName.lua.lua
**Functions:**
- GetGuild_ChatWordRegion1Uis
**Requires:**
- Guild_ChatWordLeft1ByName
- Guild_ChatWordRight1ByName
**Snippet:**
```lua
require("Guild_ChatWordLeft1ByName")
require("Guild_ChatWordRight1ByName")

function GetGuild_ChatWordRegion1Uis(ui)
  local uis = {}
  uis.ChatWordLeft = GetGuild_ChatWordLeft1Uis(ui:GetChild("ChatWordLeft"))
  uis.ChatWordRight = GetGuild_ChatWordRight1Uis(ui:GetChild("ChatWordRight"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## GL/Guild_ChatWordRegionByName.lua.lua
**Functions:**
- GetGuild_ChatWordRegionUis
**Requires:**
- Guild_ChatWordLeftByName
- Guild_ChatWordRightByName
**Snippet:**
```lua
require("Guild_ChatWordLeftByName")
require("Guild_ChatWordRightByName")

function GetGuild_ChatWordRegionUis(ui)
  local uis = {}
  uis.ChatWordLeft = GetGuild_ChatWordLeftUis(ui:GetChild("ChatWordLeft"))
  uis.ChatWordRight = GetGuild_ChatWordRightUis(ui:GetChild("ChatWordRight"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## GL/Guild_ChatWordRight1ByName.lua.lua
**Functions:**
- GetGuild_ChatWordRight1Uis
**Snippet:**
```lua
function GetGuild_ChatWordRight1Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_ChatWordRightByName.lua.lua
**Functions:**
- GetGuild_ChatWordRightUis
**Snippet:**
```lua
function GetGuild_ChatWordRightUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_Chat_infoByName.lua.lua
**Functions:**
- GetGuild_Chat_infoUis
**Snippet:**
```lua
function GetGuild_Chat_infoUis(ui)
  local uis = {}
  
  uis.ChatList = ui:GetChild("ChatList")
  uis.NoticeTxt = ui:GetChild("NoticeTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_CloseTipsByName.lua.lua
**Functions:**
- GetGuild_CloseTipsUis
**Snippet:**
```lua
function GetGuild_CloseTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_Condition1BtnByName.lua.lua
**Functions:**
- GetGuild_Condition1BtnUis
**Snippet:**
```lua
function GetGuild_Condition1BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.specialCtr = ui:GetController("special")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_Condition2BtnByName.lua.lua
**Functions:**
- GetGuild_Condition2BtnUis
**Snippet:**
```lua
function GetGuild_Condition2BtnUis(ui)
  local uis = {}
  
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.InPutTxt = ui:GetChild("InPutTxt")
  uis.specialCtr = ui:GetController("special")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_Condition3BtnByName.lua.lua
**Functions:**
- GetGuild_Condition3BtnUis
**Snippet:**
```lua
function GetGuild_Condition3BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.specialCtr = ui:GetController("special")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_DisagreeBtnByName.lua.lua
**Functions:**
- GetGuild_DisagreeBtnUis
**Snippet:**
```lua
function GetGuild_DisagreeBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_DisagreeProgressBarByName.lua.lua
**Functions:**
- GetGuild_DisagreeProgressBarUis
**Requires:**
- Guild_DisagreeProgressFillByName
**Snippet:**
```lua
require("Guild_DisagreeProgressFillByName")

function GetGuild_DisagreeProgressBarUis(ui)
  local uis = {}
  uis.bar = GetGuild_DisagreeProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## GL/Guild_DisagreeProgressFillByName.lua.lua
**Functions:**
- GetGuild_DisagreeProgressFillUis
**Snippet:**
```lua
function GetGuild_DisagreeProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/Guild_DissolutionBtnByName.lua.lua
**Functions:**
- GetGuild_DissolutionBtnUis
**Snippet:**
```lua
function GetGuild_DissolutionBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_EstablishBtnByName.lua.lua
**Functions:**
- GetGuild_EstablishBtnUis
**Snippet:**
```lua
function GetGuild_EstablishBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_Examine_infoByName.lua.lua
**Functions:**
- GetGuild_Examine_infoUis
**Snippet:**
```lua
function GetGuild_Examine_infoUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.AllRefuseBtn = ui:GetChild("AllRefuseBtn")
  uis.AllAdoptBtn = ui:GetChild("AllAdoptBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## GL/Guild_ExpProgressBarByName.lua.lua
**Functions:**
- GetGuild_ExpProgressBarUis
**Requires:**
- Guild_ExpProgressFillByName
**Snippet:**
```lua
require("Guild_ExpProgressFillByName")

function GetGuild_ExpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetGuild_ExpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## GL/Guild_ExpProgressFillByName.lua.lua
**Functions:**
- GetGuild_ExpProgressFillUis
**Snippet:**
```lua
function GetGuild_ExpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/Guild_GuildApplyByName.lua.lua
**Functions:**
- GetGuild_GuildApplyUis
**Requires:**
- Guild_GuildEmptyByName
- Guild_Time1ByName
**Snippet:**
```lua
require("Guild_GuildEmptyByName")
require("Guild_Time1ByName")

function GetGuild_GuildApplyUis(ui)
  local uis = {}
  uis.GuildEmpty = GetGuild_GuildEmptyUis(ui:GetChild("GuildEmpty"))
  uis.GuildTipsList = ui:GetChild("GuildTipsList")
  uis.Time1 = GetGuild_Time1Uis(ui:GetChild("Time1"))
  uis.RefreshBtn = ui:GetChild("RefreshBtn")
  uis.JoinBtn = ui:GetChild("JoinBtn")
```

---

## GL/Guild_GuildBossRankByName.lua.lua
**Functions:**
- GetGuild_GuildBossRankUis
**Snippet:**
```lua
function GetGuild_GuildBossRankUis(ui)
  local uis = {}
  
  uis.RankTxt = ui:GetChild("RankTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_GuildByName.lua.lua
**Functions:**
- GetGuild_GuildUis
**Requires:**
- CommonResource_BackGroundByName
- Guild_GuildMainByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Guild_GuildMainByName")
require("CommonResource_CurrencyReturnByName")

function GetGuild_GuildUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.GuildMain = GetGuild_GuildMainUis(ui:GetChild("GuildMain"))
  uis.CurrencyReturn = GetCommonResource_CurrencyReturnUis(ui:GetChild("CurrencyReturn"))
  uis.root = ui
```

---

## GL/Guild_GuildEmptyByName.lua.lua
**Functions:**
- GetGuild_GuildEmptyUis
**Snippet:**
```lua
function GetGuild_GuildEmptyUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_GuildFilterBtnByName.lua.lua
**Functions:**
- GetGuild_GuildFilterBtnUis
**Snippet:**
```lua
function GetGuild_GuildFilterBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_GuildFilterByName.lua.lua
**Functions:**
- GetGuild_GuildFilterUis
**Requires:**
- CommonResource_PopupBgByName
- Guild_GuildFilter_TipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Guild_GuildFilter_TipsByName")

function GetGuild_GuildFilterUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Tips = GetGuild_GuildFilter_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
```

---

## GL/Guild_GuildFilterWindowByName.lua.lua
**Functions:**
- GetGuild_GuildFilterWindowUis
**Requires:**
- Guild_GuildFilterByName
**Snippet:**
```lua
require("Guild_GuildFilterByName")

function GetGuild_GuildFilterWindowUis(ui)
  local uis = {}
  uis.Main = GetGuild_GuildFilterUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/Guild_GuildFilter_CloseBtnByName.lua.lua
**Functions:**
- GetGuild_GuildFilter_CloseBtnUis
**Snippet:**
```lua
function GetGuild_GuildFilter_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_GuildFilter_Info1ByName.lua.lua
**Functions:**
- GetGuild_GuildFilter_Info1Uis
**Snippet:**
```lua
function GetGuild_GuildFilter_Info1Uis(ui)
  local uis = {}
  
  uis.TtileTxt = ui:GetChild("TtileTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_GuildFilter_Info2ByName.lua.lua
**Functions:**
- GetGuild_GuildFilter_Info2Uis
**Snippet:**
```lua
function GetGuild_GuildFilter_Info2Uis(ui)
  local uis = {}
  
  uis.TtileTxt = ui:GetChild("TtileTxt")
  uis.OptionList = ui:GetChild("OptionList")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_GuildFilter_InfoBtnByName.lua.lua
**Functions:**
- GetGuild_GuildFilter_InfoBtnUis
**Requires:**
- Guild_GuildFilter_InfoMoveWordByName
**Snippet:**
```lua
require("Guild_GuildFilter_InfoMoveWordByName")

function GetGuild_GuildFilter_InfoBtnUis(ui)
  local uis = {}
  uis.MoveWord = GetGuild_GuildFilter_InfoMoveWordUis(ui:GetChild("MoveWord"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_GuildFilter_InfoMoveWordByName.lua.lua
**Functions:**
- GetGuild_GuildFilter_InfoMoveWordUis
**Snippet:**
```lua
function GetGuild_GuildFilter_InfoMoveWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_GuildFilter_ResetBtnByName.lua.lua
**Functions:**
- GetGuild_GuildFilter_ResetBtnUis
**Snippet:**
```lua
function GetGuild_GuildFilter_ResetBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_GuildFilter_SearchBtnByName.lua.lua
**Functions:**
- GetGuild_GuildFilter_SearchBtnUis
**Snippet:**
```lua
function GetGuild_GuildFilter_SearchBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_GuildFilter_SureBtnByName.lua.lua
**Functions:**
- GetGuild_GuildFilter_SureBtnUis
**Snippet:**
```lua
function GetGuild_GuildFilter_SureBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_GuildFilter_TipsByName.lua.lua
**Functions:**
- GetGuild_GuildFilter_TipsUis
**Snippet:**
```lua
function GetGuild_GuildFilter_TipsUis(ui)
  local uis = {}
  
  uis.SearchList = ui:GetChild("SearchList")
  uis.SetList = ui:GetChild("SetList")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.ResetBtn = ui:GetChild("ResetBtn")
  uis.SearchBtn = ui:GetChild("SearchBtn")
  uis.SureBtn = ui:GetChild("SureBtn")
  uis.c1Ctr = ui:GetController("c1")
```

---

## GL/Guild_GuildListByName.lua.lua
**Functions:**
- GetGuild_GuildListUis
**Requires:**
- CommonResource_BackGroundByName
- Guild_GuildApplyByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Guild_GuildApplyByName")
require("CommonResource_CurrencyReturnByName")

function GetGuild_GuildListUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.GuildApply = GetGuild_GuildApplyUis(ui:GetChild("GuildApply"))
  uis.CurrencyReturn = GetCommonResource_CurrencyReturnUis(ui:GetChild("CurrencyReturn"))
  uis.root = ui
```

---

## GL/Guild_GuildListWindowByName.lua.lua
**Functions:**
- GetGuild_GuildListWindowUis
**Requires:**
- Guild_GuildListByName
**Snippet:**
```lua
require("Guild_GuildListByName")

function GetGuild_GuildListWindowUis(ui)
  local uis = {}
  uis.Main = GetGuild_GuildListUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/Guild_GuildMainByName.lua.lua
**Functions:**
- GetGuild_GuildMainUis
**Requires:**
- Guild_Guild_infoByName
- Guild_Captain_infoByName
- Guild_JoinCondition_infoByName
- Guild_Examine_infoByName
- Guild_Chat_infoByName
- Guild_GuildEmptyByName
**Snippet:**
```lua
require("Guild_Guild_infoByName")
require("Guild_Captain_infoByName")
require("Guild_JoinCondition_infoByName")
require("Guild_Examine_infoByName")
require("Guild_Chat_infoByName")
require("Guild_GuildEmptyByName")

function GetGuild_GuildMainUis(ui)
  local uis = {}
  uis.Guild_info = GetGuild_Guild_infoUis(ui:GetChild("Guild_info"))
```

---

## GL/Guild_GuildSystemWordItemByName.lua.lua
**Functions:**
- GetGuild_GuildSystemWordItemUis
**Snippet:**
```lua
function GetGuild_GuildSystemWordItemUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_GuildTargetBtnByName.lua.lua
**Functions:**
- GetGuild_GuildTargetBtnUis
**Snippet:**
```lua
function GetGuild_GuildTargetBtnUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_GuildTipsAniByName.lua.lua
**Functions:**
- GetGuild_GuildTipsAniUis
**Requires:**
- Guild_GuildTipsByName
**Snippet:**
```lua
require("Guild_GuildTipsByName")

function GetGuild_GuildTipsAniUis(ui)
  local uis = {}
  uis.GuildTips = GetGuild_GuildTipsUis(ui:GetChild("GuildTips"))
  uis.root = ui
  return uis
end
```

---

## GL/Guild_GuildTipsByName.lua.lua
**Functions:**
- GetGuild_GuildTipsUis
**Requires:**
- Guild_LevelTipsByName
- Guild_CloseTipsByName
- Guild_GuildBossRankByName
**Snippet:**
```lua
require("Guild_LevelTipsByName")
require("Guild_CloseTipsByName")
require("Guild_GuildBossRankByName")

function GetGuild_GuildTipsUis(ui)
  local uis = {}
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.StageTxt = ui:GetChild("StageTxt")
  uis.StateTxt = ui:GetChild("StateTxt")
  uis.GulidIconLoader = ui:GetChild("GulidIconLoader")
```

---

## GL/Guild_GuildWindowByName.lua.lua
**Functions:**
- GetGuild_GuildWindowUis
**Requires:**
- Guild_GuildByName
**Snippet:**
```lua
require("Guild_GuildByName")

function GetGuild_GuildWindowUis(ui)
  local uis = {}
  uis.Main = GetGuild_GuildUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/Guild_Guild_infoByName.lua.lua
**Functions:**
- GetGuild_Guild_infoUis
**Snippet:**
```lua
function GetGuild_Guild_infoUis(ui)
  local uis = {}
  
  uis.GulidIconLoader = ui:GetChild("GulidIconLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.RenameBtn = ui:GetChild("RenameBtn")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.ExpTxt = ui:GetChild("ExpTxt")
  uis.ExpProgressBar = ui:GetChild("ExpProgressBar")
```

---

## GL/Guild_IconBtnByName.lua.lua
**Functions:**
- GetGuild_IconBtnUis
**Snippet:**
```lua
function GetGuild_IconBtnUis(ui)
  local uis = {}
  
  uis.GulidIconLoader = ui:GetChild("GulidIconLoader")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_IconChoice1ByName.lua.lua
**Functions:**
- GetGuild_IconChoice1Uis
**Snippet:**
```lua
function GetGuild_IconChoice1Uis(ui)
  local uis = {}
  
  uis.IconList = ui:GetChild("IconList")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_IconChoice2ByName.lua.lua
**Functions:**
- GetGuild_IconChoice2Uis
**Requires:**
- CommonResource_PopupBgByName
- CommonResource_Popup_BByName
- Guild_IconChoice1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("CommonResource_Popup_BByName")
require("Guild_IconChoice1ByName")

function GetGuild_IconChoice2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Popup_B = GetCommonResource_Popup_BUis(ui:GetChild("Popup_B"))
  uis.IconChoice1 = GetGuild_IconChoice1Uis(ui:GetChild("IconChoice1"))
```

---

## GL/Guild_IconChoiceWindowByName.lua.lua
**Functions:**
- GetGuild_IconChoiceWindowUis
**Requires:**
- Guild_IconChoice2ByName
**Snippet:**
```lua
require("Guild_IconChoice2ByName")

function GetGuild_IconChoiceWindowUis(ui)
  local uis = {}
  uis.Main = GetGuild_IconChoice2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/Guild_ImpeachmentBtnByName.lua.lua
**Functions:**
- GetGuild_ImpeachmentBtnUis
**Snippet:**
```lua
function GetGuild_ImpeachmentBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_InputNameByName.lua.lua
**Functions:**
- GetGuild_InputNameUis
**Snippet:**
```lua
function GetGuild_InputNameUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SearchBtn = ui:GetChild("SearchBtn")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_JoinBtnByName.lua.lua
**Functions:**
- GetGuild_JoinBtnUis
**Snippet:**
```lua
function GetGuild_JoinBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_JoinCondition_infoByName.lua.lua
**Functions:**
- GetGuild_JoinCondition_infoUis
**Snippet:**
```lua
function GetGuild_JoinCondition_infoUis(ui)
  local uis = {}
  
  uis.Condition1Btn = ui:GetChild("Condition1Btn")
  uis.Condition2Btn = ui:GetChild("Condition2Btn")
  uis.Condition3Btn = ui:GetChild("Condition3Btn")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## GL/Guild_LevelTipsByName.lua.lua
**Functions:**
- GetGuild_LevelTipsUis
**Snippet:**
```lua
function GetGuild_LevelTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_LevelUpTips1ByName.lua.lua
**Functions:**
- GetGuild_LevelUpTips1Uis
**Snippet:**
```lua
function GetGuild_LevelUpTips1Uis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.LevelNameTxt = ui:GetChild("LevelNameTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_LevelUpTips2ByName.lua.lua
**Functions:**
- GetGuild_LevelUpTips2Uis
**Requires:**
- CommonResource_PopupBgByName
- Guild_Popup_S1ByName
- Guild_LevelUpTips1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Guild_Popup_S1ByName")
require("Guild_LevelUpTips1ByName")

function GetGuild_LevelUpTips2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Popup_S = GetGuild_Popup_S1Uis(ui:GetChild("Popup_S"))
  uis.LevelUpTips1 = GetGuild_LevelUpTips1Uis(ui:GetChild("LevelUpTips1"))
```

---

## GL/Guild_LevelUpTipsWindowByName.lua.lua
**Functions:**
- GetGuild_LevelUpTipsWindowUis
**Requires:**
- Guild_LevelUpTips2ByName
**Snippet:**
```lua
require("Guild_LevelUpTips2ByName")

function GetGuild_LevelUpTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetGuild_LevelUpTips2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/Guild_OutBtnByName.lua.lua
**Functions:**
- GetGuild_OutBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetGuild_OutBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## GL/Guild_PlayerInfoByName.lua.lua
**Functions:**
- GetGuild_PlayerInfoUis
**Requires:**
- Guild_PlayerPicByName
- Guild_PositionByName
- Guild_PlayerOnlineByName
**Snippet:**
```lua
require("Guild_PlayerPicByName")
require("Guild_PositionByName")
require("Guild_PlayerOnlineByName")

function GetGuild_PlayerInfoUis(ui)
  local uis = {}
  uis.PlayerPic = GetGuild_PlayerPicUis(ui:GetChild("PlayerPic"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.Position = GetGuild_PositionUis(ui:GetChild("Position"))
```

---

## GL/Guild_PlayerOnlineByName.lua.lua
**Functions:**
- GetGuild_PlayerOnlineUis
**Snippet:**
```lua
function GetGuild_PlayerOnlineUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_PlayerPicByName.lua.lua
**Functions:**
- GetGuild_PlayerPicUis
**Snippet:**
```lua
function GetGuild_PlayerPicUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_Popup_S1ByName.lua.lua
**Functions:**
- GetGuild_Popup_S1Uis
**Snippet:**
```lua
function GetGuild_Popup_S1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/Guild_PositionByName.lua.lua
**Functions:**
- GetGuild_PositionUis
**Snippet:**
```lua
function GetGuild_PositionUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_RecordBtnByName.lua.lua
**Functions:**
- GetGuild_RecordBtnUis
**Snippet:**
```lua
function GetGuild_RecordBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_RefreshBtnByName.lua.lua
**Functions:**
- GetGuild_RefreshBtnUis
**Snippet:**
```lua
function GetGuild_RefreshBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_RefuseBtnByName.lua.lua
**Functions:**
- GetGuild_RefuseBtnUis
**Snippet:**
```lua
function GetGuild_RefuseBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_RenameBtnByName.lua.lua
**Functions:**
- GetGuild_RenameBtnUis
**Snippet:**
```lua
function GetGuild_RenameBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_SearchBtnByName.lua.lua
**Functions:**
- GetGuild_SearchBtnUis
**Snippet:**
```lua
function GetGuild_SearchBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_SupplyBtnByName.lua.lua
**Functions:**
- GetGuild_SupplyBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetGuild_SupplyBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.bossCtr = ui:GetController("boss")
  uis.root = ui
```

---

## GL/Guild_Time1ByName.lua.lua
**Functions:**
- GetGuild_Time1Uis
**Snippet:**
```lua
function GetGuild_Time1Uis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_Time2ByName.lua.lua
**Functions:**
- GetGuild_Time2Uis
**Snippet:**
```lua
function GetGuild_Time2Uis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_TrainBtnByName.lua.lua
**Functions:**
- GetGuild_TrainBtnUis
**Snippet:**
```lua
function GetGuild_TrainBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.bossCtr = ui:GetController("boss")
  uis.root = ui
  return uis
end
```

---

## GL/Guild_Vote1ByName.lua.lua
**Functions:**
- GetGuild_Vote1Uis
**Snippet:**
```lua
function GetGuild_Vote1Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.AgreeTxt = ui:GetChild("AgreeTxt")
  uis.DisagreeTxt = ui:GetChild("DisagreeTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.AgreeProgressBar = ui:GetChild("AgreeProgressBar")
  uis.DisagreeProgressBar = ui:GetChild("DisagreeProgressBar")
  uis.AgreeNumberTxt = ui:GetChild("AgreeNumberTxt")
```

---

## GL/Guild_Vote2ByName.lua.lua
**Functions:**
- GetGuild_Vote2Uis
**Requires:**
- CommonResource_PopupBgByName
- CommonResource_Popup_BByName
- Guild_Vote1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("CommonResource_Popup_BByName")
require("Guild_Vote1ByName")

function GetGuild_Vote2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Popup_B = GetCommonResource_Popup_BUis(ui:GetChild("Popup_B"))
  uis.Vote1 = GetGuild_Vote1Uis(ui:GetChild("Vote1"))
```

---

## GL/Guild_VoteTipsByName.lua.lua
**Functions:**
- GetGuild_VoteTipsUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetGuild_VoteTipsUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.AgreeTxt = ui:GetChild("AgreeTxt")
  uis.DisagreeTxt = ui:GetChild("DisagreeTxt")
  uis.AgreeProgressBar = ui:GetChild("AgreeProgressBar")
  uis.DisagreeProgressBar = ui:GetChild("DisagreeProgressBar")
```

---

## GL/Guild_VoteWindowByName.lua.lua
**Functions:**
- GetGuild_VoteWindowUis
**Requires:**
- Guild_Vote2ByName
**Snippet:**
```lua
require("Guild_Vote2ByName")

function GetGuild_VoteWindowUis(ui)
  local uis = {}
  uis.Main = GetGuild_Vote2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/HandBookEventWindow.lua.lua
**Functions:**
- HandBookEventWindow.ReInitData
- HandBookEventWindow.OnInit
- HandBookEventWindow.UpdateInfo
- HandBookEventWindow.InitBtn
- HandBookEventWindow.OnClose
**Requires:**
- Abyss_HandBookEventWindowByName
**Snippet:**
```lua
require("Abyss_HandBookEventWindowByName")
local HandBookEventWindow = {}
local uis, contentPane

function HandBookEventWindow.ReInitData()
end

local bgm_monster, illustrationId, soundInst, effWrapper, effWrapper2, delayPlaySoundTweenId

function HandBookEventWindow.OnInit(bridgeObj)
```

---

## GL/Handler.lua.lua
**Functions:**
- Handler:ctor
- Handler:RunHandles
- Handler:RunId
- Handler:getHandIndex
- Handler:GetHandleCount
- Handler:AddHandle
- Handler:RemoveHandle
- Handler:RemoveAllHandle
- Handler:innerRemove
- GetNewHandler
**Requires:**
- Class
**Snippet:**
```lua
require("Class")
local Handler = class()

function Handler:ctor()
  self.handles = {}
  self.inHand = false
  self.hasRemoveHand = false
end

function Handler:RunHandles(hands, data)
```

---

## GL/HomeData.lua.lua
**Functions:**
- HomeData.IsFogging
- HomeData.CanFogging
- HomeData.SetIsFogging
- HomeData.SetTestTime
- HomeData.GetTimeEnum
- HomeData.GetWeatherBackground
- HomeData.UpdateWeatherLightParam
- HomeData.UpdateWeatherModelParam
**Snippet:**
```lua
HomeData = {}
local data = {curBgPath = nil, isFogging = false}
local testTime

function HomeData.IsFogging()
  return data.isFogging
end

function HomeData.CanFogging()
  return true
```

---

## GL/HomeMusic_MusicByName.lua.lua
**Functions:**
- GetHomeMusic_MusicUis
**Requires:**
- HomeMusic_MusicPlayListByName
- HomeMusic_MusicChoiceRegionByName
**Snippet:**
```lua
require("HomeMusic_MusicPlayListByName")
require("HomeMusic_MusicChoiceRegionByName")

function GetHomeMusic_MusicUis(ui)
  local uis = {}
  uis.MusicPlayList = GetHomeMusic_MusicPlayListUis(ui:GetChild("MusicPlayList"))
  uis.MusicChoiceRegion = GetHomeMusic_MusicChoiceRegionUis(ui:GetChild("MusicChoiceRegion"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## GL/HomeMusic_MusicChoiceRegionByName.lua.lua
**Functions:**
- GetHomeMusic_MusicChoiceRegionUis
**Requires:**
- HomeMusic_MusicInfoByName
- HomeMusic_MusicListByName
**Snippet:**
```lua
require("HomeMusic_MusicInfoByName")
require("HomeMusic_MusicListByName")

function GetHomeMusic_MusicChoiceRegionUis(ui)
  local uis = {}
  uis.MusicInfo = GetHomeMusic_MusicInfoUis(ui:GetChild("MusicInfo"))
  uis.MusicList = GetHomeMusic_MusicListUis(ui:GetChild("MusicList"))
  uis.root = ui
  return uis
end
```

---

## GL/HomeMusic_MusicInfoByName.lua.lua
**Functions:**
- GetHomeMusic_MusicInfoUis
**Requires:**
- HomeMusic_MusicInfo_RecordAniByName
**Snippet:**
```lua
require("HomeMusic_MusicInfo_RecordAniByName")

function GetHomeMusic_MusicInfoUis(ui)
  local uis = {}
  uis.RecordAni = GetHomeMusic_MusicInfo_RecordAniUis(ui:GetChild("RecordAni"))
  uis.PlayListBtn = ui:GetChild("PlayListBtn")
  uis.MusicTxt = ui:GetChild("MusicTxt")
  uis.ComposerTxt = ui:GetChild("ComposerTxt")
  uis.CollectBtn = ui:GetChild("CollectBtn")
  uis.AddLiveBtn = ui:GetChild("AddLiveBtn")
```

---

## GL/HomeMusic_MusicInfo_AddLiveBtnByName.lua.lua
**Functions:**
- GetHomeMusic_MusicInfo_AddLiveBtnUis
**Snippet:**
```lua
function GetHomeMusic_MusicInfo_AddLiveBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/HomeMusic_MusicInfo_CollectBtnByName.lua.lua
**Functions:**
- GetHomeMusic_MusicInfo_CollectBtnUis
**Snippet:**
```lua
function GetHomeMusic_MusicInfo_CollectBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/HomeMusic_MusicInfo_PlayListBtnByName.lua.lua
**Functions:**
- GetHomeMusic_MusicInfo_PlayListBtnUis
**Snippet:**
```lua
function GetHomeMusic_MusicInfo_PlayListBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/HomeMusic_MusicInfo_RecordAniByName.lua.lua
**Functions:**
- GetHomeMusic_MusicInfo_RecordAniUis
**Snippet:**
```lua
function GetHomeMusic_MusicInfo_RecordAniUis(ui)
  local uis = {}
  
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Effect3Holder = ui:GetChild("Effect3Holder")
  uis.root = ui
  return uis
end
```

---

## GL/HomeMusic_MusicListByName.lua.lua
**Functions:**
- GetHomeMusic_MusicListUis
**Snippet:**
```lua
function GetHomeMusic_MusicListUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.TipsList = ui:GetChild("TipsList")
  uis.root = ui
  return uis
end
```

---

## GL/HomeMusic_MusicListTipsAniByName.lua.lua
**Functions:**
- GetHomeMusic_MusicListTipsAniUis
**Requires:**
- HomeMusic_MusicListTipsByName
**Snippet:**
```lua
require("HomeMusic_MusicListTipsByName")

function GetHomeMusic_MusicListTipsAniUis(ui)
  local uis = {}
  uis.Tips = GetHomeMusic_MusicListTipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## GL/HomeMusic_MusicListTipsByName.lua.lua
**Functions:**
- GetHomeMusic_MusicListTipsUis
**Snippet:**
```lua
function GetHomeMusic_MusicListTipsUis(ui)
  local uis = {}
  
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.CollectBtn = ui:GetChild("CollectBtn")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## GL/HomeMusic_MusicList_Tab1ByName.lua.lua
**Functions:**
- GetHomeMusic_MusicList_Tab1Uis
**Snippet:**
```lua
function GetHomeMusic_MusicList_Tab1Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/HomeMusic_MusicList_Tab2ByName.lua.lua
**Functions:**
- GetHomeMusic_MusicList_Tab2Uis
**Snippet:**
```lua
function GetHomeMusic_MusicList_Tab2Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/HomeMusic_MusicList_TabBtnByName.lua.lua
**Functions:**
- GetHomeMusic_MusicList_TabBtnUis
**Requires:**
- HomeMusic_MusicList_Tab1ByName
- HomeMusic_MusicList_Tab2ByName
**Snippet:**
```lua
require("HomeMusic_MusicList_Tab1ByName")
require("HomeMusic_MusicList_Tab2ByName")

function GetHomeMusic_MusicList_TabBtnUis(ui)
  local uis = {}
  uis.Tab1 = GetHomeMusic_MusicList_Tab1Uis(ui:GetChild("Tab1"))
  uis.Tab2 = GetHomeMusic_MusicList_Tab2Uis(ui:GetChild("Tab2"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## GL/HomeMusic_MusicPlayListByName.lua.lua
**Functions:**
- GetHomeMusic_MusicPlayListUis
**Snippet:**
```lua
function GetHomeMusic_MusicPlayListUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TipsList = ui:GetChild("TipsList")
  uis.UpBtn = ui:GetChild("UpBtn")
  uis.DownBtn = ui:GetChild("DownBtn")
  uis.DeleteBtn = ui:GetChild("DeleteBtn")
  uis.root = ui
  return uis
```

---

## GL/HomeMusic_MusicPlayList_DeleteBtnByName.lua.lua
**Functions:**
- GetHomeMusic_MusicPlayList_DeleteBtnUis
**Snippet:**
```lua
function GetHomeMusic_MusicPlayList_DeleteBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/HomeMusic_MusicPlayList_DownBtnByName.lua.lua
**Functions:**
- GetHomeMusic_MusicPlayList_DownBtnUis
**Snippet:**
```lua
function GetHomeMusic_MusicPlayList_DownBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/HomeMusic_MusicPlayList_TipsBtnByName.lua.lua
**Functions:**
- GetHomeMusic_MusicPlayList_TipsBtnUis
**Snippet:**
```lua
function GetHomeMusic_MusicPlayList_TipsBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/HomeMusic_MusicPlayList_UpBtnByName.lua.lua
**Functions:**
- GetHomeMusic_MusicPlayList_UpBtnUis
**Snippet:**
```lua
function GetHomeMusic_MusicPlayList_UpBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/HomeMusic_MusicWindowByName.lua.lua
**Functions:**
- GetHomeMusic_MusicWindowUis
**Requires:**
- HomeMusic_MusicByName
**Snippet:**
```lua
require("HomeMusic_MusicByName")

function GetHomeMusic_MusicWindowUis(ui)
  local uis = {}
  uis.Main = GetHomeMusic_MusicUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/HomeScriptList.lua.lua
**Requires:**
- HomeData
**Snippet:**
```lua
local require = require
require("HomeData")
```

---

## GL/HomeWindow.lua.lua
**Functions:**
- HomeWindow.ReInitData
- HomeWindow.OnInit
- HomeWindow.UpdateLanguage
- HomeWindow.UpdateBackground
- HomeWindow.UpdateModel
- HomeWindow.UpdateModelPosition
- HomeWindow.UpdateModelScale
- HomeWindow.UpdateTextDisplay
- HomeWindow.UpdateAbyssNoviceBonus
- HomeWindow.UpdateInfo
- HomeWindow.GetTaskInfo
- HomeWindow.UpdateBatteryLevel
- HomeWindow.UpdateActivityTxt
- HomeWindow.UpdatePlayerInformation
- HomeWindow.OpenActorInfoWindow
- HomeWindow.UpdateLotteryInfo
- HomeWindow.UpdateServerTime
- HomeWindow.UpdateAssetsTips
- HomeWindow.UpdateHeadRect
- HomeWindow.UpdateAdventureInfo
- HomeWindow.UpdateEnergy
- HomeWindow.UpdateMessage
- HomeWindow.InitRedDot
- HomeWindow.InitRedDotDataReq
- HomeWindow.InitBtn
- HomeWindow.CheckGuildWarState
- HomeWindow.CheckActivityDungeonState
- HomeWindow.CheckPlayerReturnActivityState
- HomeWindow.ShowGuildWar
- HomeWindow.ShowActivityDungeon
- HomeWindow.RemoveActivityButton
- HomeWindow.ShowPlayerReturnActivity
- HomeWindow.OpenCodeWindow
- HomeWindow.InitSettingModel
- HomeWindow.SetRoleUiPos
- HomeWindow.ResetLookRoleInfo
- HomeWindow.SaveLookRoleInfo
- HomeWindow.EnterSettingModel
- HomeWindow.QuitSettingModel
- HomeWindow.UpdateTextPosition
- HomeWindow.ShowReservationGift
- HomeWindow.ShowMultiDrop
- HomeWindow.NotShowMultiDrop
- HomeWindow.CheckRemoveMultiDrop
- HomeWindow.ShowMonthCard
- HomeWindow.ShowRaffleButton
- HomeWindow.ShowActivitySign
- HomeWindow.ShowSingInGiftButton
- HomeWindow.CanRemoveSingInGift
- HomeWindow.CheckRemoveSingInGift
- HomeWindow.CanRemoveReturnGift
- HomeWindow.CheckRemoveReturnGift
- HomeWindow.ShowSchedule
- HomeWindow.ShowTurnTable
- HomeWindow.SetHomeTouchable
- HomeWindow.InitBackground
- HomeWindow.UpdateFuncUnlock
- HomeWindow.OnShown
- HomeWindow.OpenTotalOpr
- HomeWindow.HideTotalOpr
- HomeWindow.UpdateBGMParameter
- HomeWindow.PlayLoginTalk
- HomeWindow.PlayFestivalTalkIfNecessary
- HomeWindow.UpdateTalkWord
- HomeWindow.StopTalk
- HomeWindow.StartTalkTimer
- HomeWindow.StopTalkTimer
- HomeWindow.StartBannerTimer
- HomeWindow.StopBannerTimer
- HomeWindow.SpeedUpTypingEffect
- HomeWindow.StopTypingEffect
- HomeWindow.OnPreHide
- HomeWindow.OnHide
- HomeWindow.OnClose
- HomeWindow.ShowCrossDayTips
- HomeWindow.HandleMessage
**Requires:**
- Home_HomeWindowByName
**Snippet:**
```lua
require("Home_HomeWindowByName")
local HomeWindow = {}
local uis, contentPane, curResPath, lastSceneObject, curSceneObject, cardShowObject, lastSceneCamera, curSceneCamera
local cachedEffect = {}
local tempGraph, curRolePos, lastRolePos, curFaceId, defaultPos, normalScale
local sliderScale = 0.5
local lastScale, curTypingEffect, curSoundEventIns, lastSoundTime, curTalkTimer, canTalkPlay, bannerTimer, enterActivityId, enterActivityIndex, bannerIndex, monthListBtn, reservationGiftItem, raffleListBtn, acPicListIndex, acPicListByActivity, multiDropItem, returnGiftItem, returnGiftId, signGiftItem, tempSetRoleInfo, canOpenTheDay, roleChanged, playerReturnBtn

function HomeWindow.ReInitData()
end
```

---

## GL/Home_AcBannerByName.lua.lua
**Functions:**
- GetHome_AcBannerUis
**Snippet:**
```lua
function GetHome_AcBannerUis(ui)
  local uis = {}
  
  uis.PicList = ui:GetChild("PicList")
  uis.root = ui
  return uis
end
```

---

## GL/Home_AcLockByName.lua.lua
**Functions:**
- GetHome_AcLockUis
**Snippet:**
```lua
function GetHome_AcLockUis(ui)
  local uis = {}
  
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Home_AcPageByName.lua.lua
**Functions:**
- GetHome_AcPageUis
**Snippet:**
```lua
function GetHome_AcPageUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/Home_AcPicLoaderBtnByName.lua.lua
**Functions:**
- GetHome_AcPicLoaderBtnUis
**Requires:**
- Home_AcLockByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("Home_AcLockByName")
require("CommonResource_RedDotByName")

function GetHome_AcPicLoaderBtnUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.AcLock = GetHome_AcLockUis(ui:GetChild("AcLock"))
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
```

---

## GL/Home_ActivityBannerByName.lua.lua
**Functions:**
- GetHome_ActivityBannerUis
**Snippet:**
```lua
function GetHome_ActivityBannerUis(ui)
  local uis = {}
  
  uis.PicList = ui:GetChild("PicList")
  uis.PageNumberList = ui:GetChild("PageNumberList")
  uis.root = ui
  return uis
end
```

---

## GL/Home_ActivityBtnByName.lua.lua
**Functions:**
- GetHome_ActivityBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetHome_ActivityBtnUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.TitleWordTxt = ui:GetChild("TitleWordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
```

---

## GL/Home_AdventureBtnByName.lua.lua
**Functions:**
- GetHome_AdventureBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetHome_AdventureBtnUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.PlotNameTxt = ui:GetChild("PlotNameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
```

---

## GL/Home_AssetsBtnByName.lua.lua
**Functions:**
- GetHome_AssetsBtnUis
**Snippet:**
```lua
function GetHome_AssetsBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Home_AssetsTipsByName.lua.lua
**Functions:**
- GetHome_AssetsTipsUis
**Snippet:**
```lua
function GetHome_AssetsTipsUis(ui)
  local uis = {}
  
  uis.IconLoader = ui:GetChild("IconLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.AssetsBtn = ui:GetChild("AssetsBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/Home_AssetsTipsGroupByName.lua.lua
**Functions:**
- GetHome_AssetsTipsGroupUis
**Snippet:**
```lua
function GetHome_AssetsTipsGroupUis(ui)
  local uis = {}
  
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.RankBtn = ui:GetChild("RankBtn")
  uis.BagBtn = ui:GetChild("BagBtn")
  uis.MailBtn = ui:GetChild("MailBtn")
  uis.NoticeBtn = ui:GetChild("NoticeBtn")
  uis.ChatBtn = ui:GetChild("ChatBtn")
  uis.TotalBtn = ui:GetChild("TotalBtn")
```

---

## GL/Home_BadgeBtnByName.lua.lua
**Functions:**
- GetHome_BadgeBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetHome_BadgeBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
```

---

## GL/Home_BagBtnByName.lua.lua
**Functions:**
- GetHome_BagBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetHome_BagBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Home_BatteryProgressBarByName.lua.lua
**Functions:**
- GetHome_BatteryProgressBarUis
**Requires:**
- Home_BatteryProgressFillByName
**Snippet:**
```lua
require("Home_BatteryProgressFillByName")

function GetHome_BatteryProgressBarUis(ui)
  local uis = {}
  uis.bar = GetHome_BatteryProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## GL/Home_BatteryProgressFillByName.lua.lua
**Functions:**
- GetHome_BatteryProgressFillUis
**Snippet:**
```lua
function GetHome_BatteryProgressFillUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/Home_BottomAreaByName.lua.lua
**Functions:**
- GetHome_BottomAreaUis
**Snippet:**
```lua
function GetHome_BottomAreaUis(ui)
  local uis = {}
  
  uis.MemberBtn = ui:GetChild("MemberBtn")
  uis.BadgeBtn = ui:GetChild("BadgeBtn")
  uis.GuildBtn = ui:GetChild("GuildBtn")
  uis.PlotBtn = ui:GetChild("PlotBtn")
  uis.root = ui
  return uis
end
```

---

## GL/Home_BottomLeftByName.lua.lua
**Functions:**
- GetHome_BottomLeftUis
**Requires:**
- Home_AcBannerByName
- Home_TemporaryTipsByName
**Snippet:**
```lua
require("Home_AcBannerByName")
require("Home_TemporaryTipsByName")

function GetHome_BottomLeftUis(ui)
  local uis = {}
  uis.ScheduleBtn = ui:GetChild("ScheduleBtn")
  uis.AcBanner = GetHome_AcBannerUis(ui:GetChild("AcBanner"))
  uis.TemporaryTips = GetHome_TemporaryTipsUis(ui:GetChild("TemporaryTips"))
  uis.ServerTxt = ui:GetChild("ServerTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## GL/Home_CardShowByName.lua.lua
**Functions:**
- GetHome_CardShowUis
**Snippet:**
```lua
function GetHome_CardShowUis(ui)
  local uis = {}
  
  uis.CardShowLoader = ui:GetChild("CardShowLoader")
  uis.CardShowHolder = ui:GetChild("CardShowHolder")
  uis.root = ui
  return uis
end
```

---

## GL/Home_CardShowNullByName.lua.lua
**Functions:**
- GetHome_CardShowNullUis
**Requires:**
- Home_CardShowByName
**Snippet:**
```lua
require("Home_CardShowByName")

function GetHome_CardShowNullUis(ui)
  local uis = {}
  uis.CardShow = GetHome_CardShowUis(ui:GetChild("CardShow"))
  uis.root = ui
  return uis
end
```

---

## GL/Home_CasketBtnByName.lua.lua
**Functions:**
- GetHome_CasketBtnUis
**Snippet:**
```lua
function GetHome_CasketBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## GL/Home_Chat1BtnByName.lua.lua
**Functions:**
- GetHome_Chat1BtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetHome_Chat1BtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## GL/Home_ChatBtnByName.lua.lua
**Functions:**
- GetHome_ChatBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetHome_ChatBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## GL/Home_CloseBtnByName.lua.lua
**Functions:**
- GetHome_CloseBtnUis
**Snippet:**
```lua
function GetHome_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Home_CodeBtnByName.lua.lua
**Functions:**
- GetHome_CodeBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetHome_CodeBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## GL/Home_DayBtnByName.lua.lua
**Functions:**
- GetHome_DayBtnUis
**Snippet:**
```lua
function GetHome_DayBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Home_DayByName.lua.lua
**Functions:**
- GetHome_DayUis
**Snippet:**
```lua
function GetHome_DayUis(ui)
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

## GL/Home_DefaultBtnByName.lua.lua
**Functions:**
- GetHome_DefaultBtnUis
**Snippet:**
```lua
function GetHome_DefaultBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Home_DuskBtnByName.lua.lua
**Functions:**
- GetHome_DuskBtnUis
**Snippet:**
```lua
function GetHome_DuskBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Home_ExploreSignBtnByName.lua.lua
**Functions:**
- GetHome_ExploreSignBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetHome_ExploreSignBtnUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## GL/Home_ExpProgressBarByName.lua.lua
**Functions:**
- GetHome_ExpProgressBarUis
**Requires:**
- Home_ExpProgressFillByName
**Snippet:**
```lua
require("Home_ExpProgressFillByName")

function GetHome_ExpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetHome_ExpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## GL/Home_ExpProgressFillByName.lua.lua
**Functions:**
- GetHome_ExpProgressFillUis
**Snippet:**
```lua
function GetHome_ExpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/Home_FriendBtnByName.lua.lua
**Functions:**
- GetHome_FriendBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetHome_FriendBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## GL/Home_GaChaBtnByName.lua.lua
**Functions:**
- GetHome_GaChaBtnUis
**Requires:**
- Home_GaChaPicSwitchByName
- CommonResource_RedDotByName
- CommonResource_LotteryFreeByName
**Snippet:**
```lua
require("Home_GaChaPicSwitchByName")
require("CommonResource_RedDotByName")
require("CommonResource_LotteryFreeByName")

function GetHome_GaChaBtnUis(ui)
  local uis = {}
  uis.Pic = GetHome_GaChaPicSwitchUis(ui:GetChild("Pic"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.LotteryFree = GetCommonResource_LotteryFreeUis(ui:GetChild("LotteryFree"))
```

---

## GL/Home_GaChaPicSwitchByName.lua.lua
**Functions:**
- GetHome_GaChaPicSwitchUis
**Snippet:**
```lua
function GetHome_GaChaPicSwitchUis(ui)
  local uis = {}
  
  uis.Pic1Loader = ui:GetChild("Pic1Loader")
  uis.Pic2Loader = ui:GetChild("Pic2Loader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/Home_GuildBtnByName.lua.lua
**Functions:**
- GetHome_GuildBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetHome_GuildBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
```

---

## GL/Home_HomeBtnByName.lua.lua
**Functions:**
- GetHome_HomeBtnUis
**Requires:**
- CommonResource_AbyssSignByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_AbyssSignByName")
require("CommonResource_RedDotByName")

function GetHome_HomeBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.AbyssSign = GetCommonResource_AbyssSignUis(ui:GetChild("AbyssSign"))
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
```

---

## GL/Home_HomeByName.lua.lua
**Functions:**
- GetHome_HomeUis
**Requires:**
- CommonResource_BackGroundByName
- Home_CardShowNullByName
- Home_TalkWordByName
- Home_PlayerInformationByName
- Home_SignByName
- Home_MiddleZoneByName
- Home_AssetsTipsGroupByName
- Home_BottomAreaByName
- Home_BottomLeftByName
- Home_PositionMaskByName
- Home_PositionByName
- Home_TotalOprByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Home_CardShowNullByName")
require("Home_TalkWordByName")
require("Home_PlayerInformationByName")
require("Home_SignByName")
require("Home_MiddleZoneByName")
require("Home_AssetsTipsGroupByName")
require("Home_BottomAreaByName")
require("Home_BottomLeftByName")
require("Home_PositionMaskByName")
```

---

## GL/Home_HomeWindowByName.lua.lua
**Functions:**
- GetHome_HomeWindowUis
**Requires:**
- Home_HomeByName
**Snippet:**
```lua
require("Home_HomeByName")

function GetHome_HomeWindowUis(ui)
  local uis = {}
  uis.Main = GetHome_HomeUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/Home_KeepBtnByName.lua.lua
**Functions:**
- GetHome_KeepBtnUis
**Snippet:**
```lua
function GetHome_KeepBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Home_LookBtnByName.lua.lua
**Functions:**
- GetHome_LookBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetHome_LookBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Home_MailBtnByName.lua.lua
**Functions:**
- GetHome_MailBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetHome_MailBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Home_MemberBtnByName.lua.lua
**Functions:**
- GetHome_MemberBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetHome_MemberBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## GL/Home_MiddleZoneByName.lua.lua
**Functions:**
- GetHome_MiddleZoneUis
**Snippet:**
```lua
function GetHome_MiddleZoneUis(ui)
  local uis = {}
  
  uis.HomeBtn = ui:GetChild("HomeBtn")
  uis.AbyssNewPeopleBtn = ui:GetChild("AbyssNewPeopleBtn")
  uis.GaChaBtn = ui:GetChild("GaChaBtn")
  uis.AdventureBtn = ui:GetChild("AdventureBtn")
  uis.ReasonBtn = ui:GetChild("ReasonBtn")
  uis.ActivityBtn = ui:GetChild("ActivityBtn")
  uis.CasketBtn = ui:GetChild("CasketBtn")
```

---

## GL/Home_MonthBtnByName.lua.lua
**Functions:**
- GetHome_MonthBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetHome_MonthBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Home_MultipleBtnByName.lua.lua
**Functions:**
- GetHome_MultipleBtnUis
**Requires:**
- Home_MultipleNmuberByName
**Snippet:**
```lua
require("Home_MultipleNmuberByName")

function GetHome_MultipleBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Nmuber = GetHome_MultipleNmuberUis(ui:GetChild("Nmuber"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Home_MultipleNmuberByName.lua.lua
**Functions:**
- GetHome_MultipleNmuberUis
**Snippet:**
```lua
function GetHome_MultipleNmuberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Home_MusicBtnByName.lua.lua
**Functions:**
- GetHome_MusicBtnUis
**Snippet:**
```lua
function GetHome_MusicBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Home_NewByName.lua.lua
**Functions:**
- GetHome_NewUis
**Snippet:**
```lua
function GetHome_NewUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## GL/Home_NightBtnByName.lua.lua
**Functions:**
- GetHome_NightBtnUis
**Snippet:**
```lua
function GetHome_NightBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Home_NoticeBtnByName.lua.lua
**Functions:**
- GetHome_NoticeBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetHome_NoticeBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Home_PageByName.lua.lua
**Functions:**
- GetHome_PageUis
**Snippet:**
```lua
function GetHome_PageUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/Home_PassportBtnByName.lua.lua
**Functions:**
- GetHome_PassportBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetHome_PassportBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.casketCtr = ui:GetController("casket")
  uis.root = ui
```

---

## GL/Home_PicLoaderBtnByName.lua.lua
**Functions:**
- GetHome_PicLoaderBtnUis
**Snippet:**
```lua
function GetHome_PicLoaderBtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Home_PlayerInfoBtnByName.lua.lua
**Functions:**
- GetHome_PlayerInfoBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetHome_PlayerInfoBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Home_PlayerInformationByName.lua.lua
**Functions:**
- GetHome_PlayerInformationUis
**Requires:**
- Home_DayByName
**Snippet:**
```lua
require("Home_DayByName")

function GetHome_PlayerInformationUis(ui)
  local uis = {}
  uis.Day = GetHome_DayUis(ui:GetChild("Day"))
  uis.IdNumberTxt = ui:GetChild("IdNumberTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.PlayerLevelTxt = ui:GetChild("PlayerLevelTxt")
  uis.PlayerNameTxt = ui:GetChild("PlayerNameTxt")
  uis.BatteryProgressBar = ui:GetChild("BatteryProgressBar")
```

---

## GL/Home_PlotBtnByName.lua.lua
**Functions:**
- GetHome_PlotBtnUis
**Requires:**
- Home_NewByName
**Snippet:**
```lua
require("Home_NewByName")

function GetHome_PlotBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.Red = GetHome_NewUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
```

---

## GL/Home_PositionByName.lua.lua
**Functions:**
- GetHome_PositionUis
**Snippet:**
```lua
function GetHome_PositionUis(ui)
  local uis = {}
  
  uis.PosTxt = ui:GetChild("PosTxt")
  uis.PosNumberTxt = ui:GetChild("PosNumberTxt")
  uis.ZoomTxt = ui:GetChild("ZoomTxt")
  uis.ZoomSlider = ui:GetChild("ZoomSlider")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.DefaultBtn = ui:GetChild("DefaultBtn")
  uis.KeepBtn = ui:GetChild("KeepBtn")
```

---

## GL/Home_PositionMaskByName.lua.lua
**Functions:**
- GetHome_PositionMaskUis
**Snippet:**
```lua
function GetHome_PositionMaskUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/Home_ReasonBtnByName.lua.lua
**Functions:**
- GetHome_ReasonBtnUis
**Snippet:**
```lua
function GetHome_ReasonBtnUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Home_RegressionSignBtnByName.lua.lua
**Functions:**
- GetHome_RegressionSignBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetHome_RegressionSignBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Home_ReservationBtnByName.lua.lua
**Functions:**
- GetHome_ReservationBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetHome_ReservationBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Home_ScheduleBtnByName.lua.lua
**Functions:**
- GetHome_ScheduleBtnUis
**Requires:**
- CommonResource_RedDotByName
- CommonResource_CardGetNewByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")
require("CommonResource_CardGetNewByName")

function GetHome_ScheduleBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.TimeHolder = ui:GetChild("TimeHolder")
  uis.New = GetCommonResource_CardGetNewUis(ui:GetChild("New"))
  uis.buttonCtr = ui:GetController("button")
```

---

## GL/Home_SetBtnByName.lua.lua
**Functions:**
- GetHome_SetBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetHome_SetBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Home_ShopBtnByName.lua.lua
**Functions:**
- GetHome_ShopBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetHome_ShopBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.casketCtr = ui:GetController("casket")
```

---

## GL/Home_SignBtnByName.lua.lua
**Functions:**
- GetHome_SignBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetHome_SignBtnUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
```

---

## GL/Home_SignByName.lua.lua
**Functions:**
- GetHome_SignUis
**Snippet:**
```lua
function GetHome_SignUis(ui)
  local uis = {}
  
  uis.SignList = ui:GetChild("SignList")
  uis.root = ui
  return uis
end
```

---

## GL/Home_SmallChatBtnByName.lua.lua
**Functions:**
- GetHome_SmallChatBtnUis
**Snippet:**
```lua
function GetHome_SmallChatBtnUis(ui)
  local uis = {}
  
  uis.ChatWordTxt = ui:GetChild("ChatWordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Home_TalkWordByName.lua.lua
**Functions:**
- GetHome_TalkWordUis
**Snippet:**
```lua
function GetHome_TalkWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Home_TemporaryTipsByName.lua.lua
**Functions:**
- GetHome_TemporaryTipsUis
**Snippet:**
```lua
function GetHome_TemporaryTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Home_TotalBtnByName.lua.lua
**Functions:**
- GetHome_TotalBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetHome_TotalBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Home_TotalOprBtnByName.lua.lua
**Functions:**
- GetHome_TotalOprBtnUis
**Snippet:**
```lua
function GetHome_TotalOprBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Home_TotalOprByName.lua.lua
**Functions:**
- GetHome_TotalOprUis
**Snippet:**
```lua
function GetHome_TotalOprUis(ui)
  local uis = {}
  
  uis.PlayerInfoBtn = ui:GetChild("PlayerInfoBtn")
  uis.SetBtn = ui:GetChild("SetBtn")
  uis.ChatBtn = ui:GetChild("ChatBtn")
  uis.FriendBtn = ui:GetChild("FriendBtn")
  uis.CodeBtn = ui:GetChild("CodeBtn")
  uis.root = ui
  return uis
```

---

## GL/Home_ZoomSliderByName.lua.lua
**Functions:**
- GetHome_ZoomSliderUis
**Snippet:**
```lua
function GetHome_ZoomSliderUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/Home_ZoomSlider_gripByName.lua.lua
**Functions:**
- GetHome_ZoomSlider_gripUis
**Snippet:**
```lua
function GetHome_ZoomSlider_gripUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/InfoTipsUtil.lua.lua
**Functions:**
- InfoTipsUtil.ShowCardTipsWindow
- InfoTipsUtil.ShowBuildingTipsWindow
- InfoTipsUtil.ShowBuffTipsWindow
- InfoTipsUtil.ShowExpeditionBuffTipsWindow
- InfoTipsUtil.ShowRestraintTipsWindow
- InfoTipsUtil.CloseTips
**Snippet:**
```lua
local InfoTipsUtil = {}

function InfoTipsUtil.ShowCardTipsWindow(cardInfo, closeCallback, params, sceneType, stageId)
  local id = cardInfo.id or cardInfo.cardId
  local config, isMonster = CardData.GetBaseConfig(id)
  if isMonster then
    if config.transform then
      local transform = Split(config.transform[1], ":")
      local monsterIdList = {
        id,
```

---

## GL/InitialCarnivalWindow.lua.lua
**Functions:**
- InitialCarnivalWindow.OnInit
- InitialCarnivalWindow.InitRedDot
- InitialCarnivalWindow.LoadBgTexture
- InitialCarnivalWindow.IsSeasonSettle
- InitialCarnivalWindow.GetCarnivalDataById
- InitialCarnivalWindow.GetServiceCarnivalById
- InitialCarnivalWindow.GetCarnivalDataByTaskId
- InitialCarnivalWindow.GetCurStage
- InitialCarnivalWindow.GetCarnivalData
- InitialCarnivalWindow.UpdateDayState
- InitialCarnivalWindow.Init
- carnival.Tab.TabList.itemRenderer
- InitialCarnivalWindow.UpdateRewardBar
- InitialCarnivalWindow.RefreshList
- InitialCarnivalWindow.RefreshIntegral
- InitialCarnivalWindow.GetInfoData
- InitialCarnivalWindow.UpdateTaskInfo
- InitialCarnivalWindow.RefreshTaskList
- InitialCarnivalWindow.InitBtn
- InitialCarnivalWindow.UpdateTaskNum
- InitialCarnivalWindow.OnShow
- InitialCarnivalWindow.HandleMessage
- InitialCarnivalWindow.OnClose
**Requires:**
- InitialCarnival_CarnivalByName
**Snippet:**
```lua
require("InitialCarnival_CarnivalByName")
InitialCarnivalWindow = {}
local lerp = Mathf.Lerp
local carnivalData, targetData, curPageIndex, curStageId, integralIcon, integralNum, settleTime, carnival, curId, labelItem, firstEnter, unLocked
local width = 81
local tween, isMove, getId, getNum, isGetReward
local taskIconId = 21000008
local curIndex
local AlignType = {
  None = 0,
```

---

## GL/InitialCarnival_CarnivalByName.lua.lua
**Functions:**
- GetInitialCarnival_CarnivalUis
**Requires:**
- CommonResource_BackGroundByName
- InitialCarnival_TaskByName
- InitialCarnival_ShowByName
- InitialCarnival_CarnivalTabByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("InitialCarnival_TaskByName")
require("InitialCarnival_ShowByName")
require("InitialCarnival_CarnivalTabByName")

function GetInitialCarnival_CarnivalUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Task1 = GetInitialCarnival_TaskUis(ui:GetChild("Task1"))
  uis.Task2 = GetInitialCarnival_TaskUis(ui:GetChild("Task2"))
```

---

## GL/InitialCarnival_CarnivalTabBigByName.lua.lua
**Functions:**
- GetInitialCarnival_CarnivalTabBigUis
**Snippet:**
```lua
function GetInitialCarnival_CarnivalTabBigUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/InitialCarnival_CarnivalTabByName.lua.lua
**Functions:**
- GetInitialCarnival_CarnivalTabUis
**Requires:**
- InitialCarnival_CarnivalTabProgressByName
**Snippet:**
```lua
require("InitialCarnival_CarnivalTabProgressByName")

function GetInitialCarnival_CarnivalTabUis(ui)
  local uis = {}
  uis.TabList = ui:GetChild("TabList")
  uis.CarnivalTabProgress = GetInitialCarnival_CarnivalTabProgressUis(ui:GetChild("CarnivalTabProgress"))
  uis.root = ui
  return uis
end
```

---

## GL/InitialCarnival_CarnivalTabProgressByName.lua.lua
**Functions:**
- GetInitialCarnival_CarnivalTabProgressUis
**Snippet:**
```lua
function GetInitialCarnival_CarnivalTabProgressUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## GL/InitialCarnival_CarnivalTabSmallByName.lua.lua
**Functions:**
- GetInitialCarnival_CarnivalTabSmallUis
**Snippet:**
```lua
function GetInitialCarnival_CarnivalTabSmallUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/InitialCarnival_CarnivalTabTipsByName.lua.lua
**Functions:**
- GetInitialCarnival_CarnivalTabTipsUis
**Requires:**
- InitialCarnival_CarnivalTabBigByName
- InitialCarnival_CarnivalTabSmallByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("InitialCarnival_CarnivalTabBigByName")
require("InitialCarnival_CarnivalTabSmallByName")
require("CommonResource_RedDotByName")

function GetInitialCarnival_CarnivalTabTipsUis(ui)
  local uis = {}
  uis.Big = GetInitialCarnival_CarnivalTabBigUis(ui:GetChild("Big"))
  uis.Small = GetInitialCarnival_CarnivalTabSmallUis(ui:GetChild("Small"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
```

---

## GL/InitialCarnival_CurrentIntegralByName.lua.lua
**Functions:**
- GetInitialCarnival_CurrentIntegralUis
**Snippet:**
```lua
function GetInitialCarnival_CurrentIntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## GL/InitialCarnival_GetIntegralByName.lua.lua
**Functions:**
- GetInitialCarnival_GetIntegralUis
**Snippet:**
```lua
function GetInitialCarnival_GetIntegralUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## GL/InitialCarnival_ItemFrameByName.lua.lua
**Functions:**
- GetInitialCarnival_ItemFrameUis
**Requires:**
- CommonResource_ItemCardPicByName
**Snippet:**
```lua
require("CommonResource_ItemCardPicByName")

function GetInitialCarnival_ItemFrameUis(ui)
  local uis = {}
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.ItemCardPic = GetCommonResource_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.typeCtr = ui:GetController("type")
```

---

## GL/InitialCarnival_PositionBtnByName.lua.lua
**Functions:**
- GetInitialCarnival_PositionBtnUis
**Snippet:**
```lua
function GetInitialCarnival_PositionBtnUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.ProgressTxt = ui:GetChild("ProgressTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/InitialCarnival_RewardItemByName.lua.lua
**Functions:**
- GetInitialCarnival_RewardItemUis
**Requires:**
- InitialCarnival_ItemFrameByName
- InitialCarnival_GetIntegralByName
**Snippet:**
```lua
require("InitialCarnival_ItemFrameByName")
require("InitialCarnival_GetIntegralByName")

function GetInitialCarnival_RewardItemUis(ui)
  local uis = {}
  uis.RewardItem = GetInitialCarnival_ItemFrameUis(ui:GetChild("RewardItem"))
  uis.GetIntegral = GetInitialCarnival_GetIntegralUis(ui:GetChild("GetIntegral"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## GL/InitialCarnival_RewardList1ByName.lua.lua
**Functions:**
- GetInitialCarnival_RewardList1Uis
**Requires:**
- InitialCarnival_CurrentIntegralByName
**Snippet:**
```lua
require("InitialCarnival_CurrentIntegralByName")

function GetInitialCarnival_RewardList1Uis(ui)
  local uis = {}
  uis.RewardItemList = ui:GetChild("RewardItemList")
  uis.CurrentIntegral = GetInitialCarnival_CurrentIntegralUis(ui:GetChild("CurrentIntegral"))
  uis.root = ui
  return uis
end
```

---

## GL/InitialCarnival_RewardList2ByName.lua.lua
**Functions:**
- GetInitialCarnival_RewardList2Uis
**Requires:**
- CommonResource_PopupBgByName
- InitialCarnival_RewardList1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("InitialCarnival_RewardList1ByName")

function GetInitialCarnival_RewardList2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.RewardList1 = GetInitialCarnival_RewardList1Uis(ui:GetChild("RewardList1"))
  uis.root = ui
  return uis
```

---

## GL/InitialCarnival_RewardListWindowByName.lua.lua
**Functions:**
- GetInitialCarnival_RewardListWindowUis
**Requires:**
- InitialCarnival_RewardList2ByName
**Snippet:**
```lua
require("InitialCarnival_RewardList2ByName")

function GetInitialCarnival_RewardListWindowUis(ui)
  local uis = {}
  uis.Main = GetInitialCarnival_RewardList2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/InitialCarnival_ShowByName.lua.lua
**Functions:**
- GetInitialCarnival_ShowUis
**Requires:**
- InitialCarnival_TargetByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("InitialCarnival_TargetByName")
require("CommonResource_RedDotByName")

function GetInitialCarnival_ShowUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.PicHolder = ui:GetChild("PicHolder")
  uis.Target = GetInitialCarnival_TargetUis(ui:GetChild("Target"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
```

---

## GL/InitialCarnival_TargetByName.lua.lua
**Functions:**
- GetInitialCarnival_TargetUis
**Snippet:**
```lua
function GetInitialCarnival_TargetUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.IntegralTxt = ui:GetChild("IntegralTxt")
  uis.root = ui
  return uis
end
```

---

## GL/InitialCarnival_TaskByName.lua.lua
**Functions:**
- GetInitialCarnival_TaskUis
**Requires:**
- InitialCarnival_TaskItemByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("InitialCarnival_TaskItemByName")
require("CommonResource_RedDotByName")

function GetInitialCarnival_TaskUis(ui)
  local uis = {}
  uis.TaskItem = GetInitialCarnival_TaskItemUis(ui:GetChild("TaskItem"))
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## GL/InitialCarnival_TaskDetails1BtnByName.lua.lua
**Functions:**
- GetInitialCarnival_TaskDetails1BtnUis
**Snippet:**
```lua
function GetInitialCarnival_TaskDetails1BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/InitialCarnival_TaskDetails2BtnByName.lua.lua
**Functions:**
- GetInitialCarnival_TaskDetails2BtnUis
**Snippet:**
```lua
function GetInitialCarnival_TaskDetails2BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/InitialCarnival_TaskDetailsByName.lua.lua
**Functions:**
- GetInitialCarnival_TaskDetailsUis
**Requires:**
- CommonResource_PopupBgByName
- InitialCarnival_TaskDetailsTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("InitialCarnival_TaskDetailsTipsByName")

function GetInitialCarnival_TaskDetailsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.TaskDetailsTips = GetInitialCarnival_TaskDetailsTipsUis(ui:GetChild("TaskDetailsTips"))
  uis.root = ui
  return uis
```

---

## GL/InitialCarnival_TaskDetailsCompleteByName.lua.lua
**Functions:**
- GetInitialCarnival_TaskDetailsCompleteUis
**Snippet:**
```lua
function GetInitialCarnival_TaskDetailsCompleteUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/InitialCarnival_TaskDetailsProgressByName.lua.lua
**Functions:**
- GetInitialCarnival_TaskDetailsProgressUis
**Snippet:**
```lua
function GetInitialCarnival_TaskDetailsProgressUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/InitialCarnival_TaskDetailsTimeByName.lua.lua
**Functions:**
- GetInitialCarnival_TaskDetailsTimeUis
**Snippet:**
```lua
function GetInitialCarnival_TaskDetailsTimeUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## GL/InitialCarnival_TaskDetailsTipsByName.lua.lua
**Functions:**
- GetInitialCarnival_TaskDetailsTipsUis
**Requires:**
- InitialCarnival_TaskDetailsTimeByName
- InitialCarnival_TaskDetailsProgressByName
- InitialCarnival_TaskDetailsCompleteByName
**Snippet:**
```lua
require("InitialCarnival_TaskDetailsTimeByName")
require("InitialCarnival_TaskDetailsProgressByName")
require("InitialCarnival_TaskDetailsCompleteByName")

function GetInitialCarnival_TaskDetailsTipsUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Time = GetInitialCarnival_TaskDetailsTimeUis(ui:GetChild("Time"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Progress = GetInitialCarnival_TaskDetailsProgressUis(ui:GetChild("Progress"))
```

---

## GL/InitialCarnival_TaskDetailsWindowByName.lua.lua
**Functions:**
- GetInitialCarnival_TaskDetailsWindowUis
**Requires:**
- InitialCarnival_TaskDetailsByName
**Snippet:**
```lua
require("InitialCarnival_TaskDetailsByName")

function GetInitialCarnival_TaskDetailsWindowUis(ui)
  local uis = {}
  uis.Main = GetInitialCarnival_TaskDetailsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/InitialCarnival_TaskItemByName.lua.lua
**Functions:**
- GetInitialCarnival_TaskItemUis
**Snippet:**
```lua
function GetInitialCarnival_TaskItemUis(ui)
  local uis = {}
  
  uis.ItemEffectHolder = ui:GetChild("ItemEffectHolder")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ProgressTxt = ui:GetChild("ProgressTxt")
  uis.SubmitTxt = ui:GetChild("SubmitTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## GL/InitialEnergyWindow.lua.lua
**Functions:**
- InitialEnergyWindow.OnInit
- InitialEnergyWindow.OnShow
- InitialEnergyWindow.OnHide
- InitialEnergyWindow.OnClose
- InitialEnergyWindow.HandleMessage
**Requires:**
- InitialEnergy_InitialEnergyByName
**Snippet:**
```lua
require("InitialEnergy_InitialEnergyByName")
InitialEnergyWindow = {}
local uis, rewards
local UpdateRedDot = function()
  RedDotMgr.UpdateNode(RED_DOT_DATA_TYPE.TASK)
end
local RewardItemRenderer = function(i, gcmp)
  local rewardConf = rewards[i]
  local rewardId = rewardConf.id
  UIUtil.SetText(gcmp, rewardConf.name(), "NameTxt")
```

---

## GL/InitialEnergy_EnergyGetByName.lua.lua
**Functions:**
- GetInitialEnergy_EnergyGetUis
**Snippet:**
```lua
function GetInitialEnergy_EnergyGetUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/InitialEnergy_EnergyNowByName.lua.lua
**Functions:**
- GetInitialEnergy_EnergyNowUis
**Snippet:**
```lua
function GetInitialEnergy_EnergyNowUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/InitialEnergy_EnergyNumberByName.lua.lua
**Functions:**
- GetInitialEnergy_EnergyNumberUis
**Snippet:**
```lua
function GetInitialEnergy_EnergyNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/InitialEnergy_EnergyPicByName.lua.lua
**Functions:**
- GetInitialEnergy_EnergyPicUis
**Snippet:**
```lua
function GetInitialEnergy_EnergyPicUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## GL/InitialEnergy_EnergyRepairByName.lua.lua
**Functions:**
- GetInitialEnergy_EnergyRepairUis
**Snippet:**
```lua
function GetInitialEnergy_EnergyRepairUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/InitialEnergy_EnergyTipsByName.lua.lua
**Functions:**
- GetInitialEnergy_EnergyTipsUis
**Requires:**
- InitialEnergy_EnergyPicByName
- InitialEnergy_EnergyGetByName
- InitialEnergy_EnergyNumberByName
**Snippet:**
```lua
require("InitialEnergy_EnergyPicByName")
require("InitialEnergy_EnergyGetByName")
require("InitialEnergy_EnergyNumberByName")

function GetInitialEnergy_EnergyTipsUis(ui)
  local uis = {}
  uis.PointImage = ui:GetChild("PointImage")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.EnergyPic = GetInitialEnergy_EnergyPicUis(ui:GetChild("EnergyPic"))
```

---

## GL/InitialEnergy_InitialEnergyByName.lua.lua
**Functions:**
- GetInitialEnergy_InitialEnergyUis
**Requires:**
- CommonResource_BackGroundByName
- InitialEnergy_EnergyTipsByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("InitialEnergy_EnergyTipsByName")

function GetInitialEnergy_InitialEnergyUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EnergyTips1 = GetInitialEnergy_EnergyTipsUis(ui:GetChild("EnergyTips1"))
  uis.EnergyTips2 = GetInitialEnergy_EnergyTipsUis(ui:GetChild("EnergyTips2"))
  uis.EnergyTips3 = GetInitialEnergy_EnergyTipsUis(ui:GetChild("EnergyTips3"))
```

---

## GL/InitialLevelRewardWindow.lua.lua
**Functions:**
- InitialLevelRewardWindow.OnInit
- InitialLevelRewardWindow.Next
- InitialLevelRewardWindow.GetCurRewardId
- InitialLevelRewardWindow.LoadBgTexture
- InitialLevelRewardWindow.InitInfo
- uis.LetterContent.WordList.itemRenderer
- uis.LetterReward.ItemList.itemRenderer
- InitialLevelRewardWindow.ShowOneReward
- InitialLevelRewardWindow.OnShow
- InitialLevelRewardWindow.HandleMessage
- InitialLevelRewardWindow.OnClose
**Requires:**
- InitialLevelReward_InitialLevelRewardByName
**Snippet:**
```lua
require("InitialLevelReward_InitialLevelRewardByName")
InitialLevelRewardWindow = {}
local uis, giftInfo, rewardLvData, lockLv, giftSpine, endIndex

function InitialLevelRewardWindow.OnInit(com)
  uis = GetInitialLevelReward_InitialLevelRewardUis(com)
  local rewardId = InitialLevelRewardWindow.GetCurRewardId()
  uis.BackGround.BackGroundLoader.url = UIUtil.GetBackgroundUrl(FEATURE_ENUM.LV_GIFT)
  if rewardId and giftInfo then
    rewardLvData = TableData.GetConfig(rewardId, "BaseGiftReward")
```

---

## GL/InitialLevelReward_AllFrameByName.lua.lua
**Functions:**
- GetInitialLevelReward_AllFrameUis
**Requires:**
- InitialLevelReward_ItemFrameByName
- InitialLevelReward_CardFrameByName
**Snippet:**
```lua
require("InitialLevelReward_ItemFrameByName")
require("InitialLevelReward_CardFrameByName")

function GetInitialLevelReward_AllFrameUis(ui)
  local uis = {}
  uis.ItemFrame = GetInitialLevelReward_ItemFrameUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetInitialLevelReward_CardFrameUis(ui:GetChild("CardFrame"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## GL/InitialLevelReward_CardFrameByName.lua.lua
**Functions:**
- GetInitialLevelReward_CardFrameUis
**Requires:**
- Passport_ItemCardPicByName
**Snippet:**
```lua
require("Passport_ItemCardPicByName")

function GetInitialLevelReward_CardFrameUis(ui)
  local uis = {}
  uis.ItemCardPic = GetPassport_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## GL/InitialLevelReward_GetWord1BtnByName.lua.lua
**Functions:**
- GetInitialLevelReward_GetWord1BtnUis
**Snippet:**
```lua
function GetInitialLevelReward_GetWord1BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/InitialLevelReward_GetWord2ByName.lua.lua
**Functions:**
- GetInitialLevelReward_GetWord2Uis
**Snippet:**
```lua
function GetInitialLevelReward_GetWord2Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/InitialLevelReward_GetWord3ByName.lua.lua
**Functions:**
- GetInitialLevelReward_GetWord3Uis
**Snippet:**
```lua
function GetInitialLevelReward_GetWord3Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/InitialLevelReward_InitialLevelRewardByName.lua.lua
**Functions:**
- GetInitialLevelReward_InitialLevelRewardUis
**Requires:**
- CommonResource_BackGroundByName
- InitialLevelReward_LetterContentByName
- InitialLevelReward_LetterRewardByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("InitialLevelReward_LetterContentByName")
require("InitialLevelReward_LetterRewardByName")

function GetInitialLevelReward_InitialLevelRewardUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.PicHolder = ui:GetChild("PicHolder")
  uis.LetterContent = GetInitialLevelReward_LetterContentUis(ui:GetChild("LetterContent"))
  uis.LetterReward = GetInitialLevelReward_LetterRewardUis(ui:GetChild("LetterReward"))
```

---

## GL/InitialLevelReward_ItemFrameByName.lua.lua
**Functions:**
- GetInitialLevelReward_ItemFrameUis
**Snippet:**
```lua
function GetInitialLevelReward_ItemFrameUis(ui)
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

## GL/InitialLevelReward_LetterContentByName.lua.lua
**Functions:**
- GetInitialLevelReward_LetterContentUis
**Snippet:**
```lua
function GetInitialLevelReward_LetterContentUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.root = ui
  return uis
end
```

---

## GL/InitialLevelReward_LetterRewardByName.lua.lua
**Functions:**
- GetInitialLevelReward_LetterRewardUis
**Requires:**
- InitialLevelReward_GetWord2ByName
- InitialLevelReward_GetWord3ByName
**Snippet:**
```lua
require("InitialLevelReward_GetWord2ByName")
require("InitialLevelReward_GetWord3ByName")

function GetInitialLevelReward_LetterRewardUis(ui)
  local uis = {}
  uis.ConditionWordTxt = ui:GetChild("ConditionWordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.Word1Btn = ui:GetChild("Word1Btn")
  uis.Word2 = GetInitialLevelReward_GetWord2Uis(ui:GetChild("Word2"))
  uis.Word3 = GetInitialLevelReward_GetWord3Uis(ui:GetChild("Word3"))
```

---

## GL/InitialLevelReward_LetterWordByName.lua.lua
**Functions:**
- GetInitialLevelReward_LetterWordUis
**Snippet:**
```lua
function GetInitialLevelReward_LetterWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/InitialSignAutoWindow.lua.lua
**Functions:**
- InitialSignAutoWindow.ReInitData
- InitialSignAutoWindow.OnInit
- InitialSignAutoWindow.UpdateInfo
- InitialSignAutoWindow.UpdateUI
- InitialSignAutoWindow.QuitDestroy
- InitialSignAutoWindow.InitBtn
- InitialSignAutoWindow.OnClose
**Requires:**
- InitialSign_InitialSignAutoWindowByName
- InitialSign_SignItemByName
**Snippet:**
```lua
require("InitialSign_InitialSignAutoWindowByName")
require("InitialSign_SignItemByName")
local InitialSignAutoWindow = {}
local uis, contentPane, item, bg, signInData, SceneRoot, signIndex, signSceneCamera, rewardData

function InitialSignAutoWindow.ReInitData()
end

function InitialSignAutoWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.InitialSignAutoWindow.package, WinResConfig.InitialSignAutoWindow.comName, function(com)
```

---

## GL/InitialSignRewardShowWindow.lua.lua
**Functions:**
- InitialSignRewardShowWindow.OnInit
- InitialSignRewardShowWindow.Init
- list.itemRenderer
- InitialSignRewardShowWindow.ShowReward
- list.itemRenderer
- InitialSignRewardShowWindow.InitBtn
- InitialSignRewardShowWindow.HandleMessage
- InitialSignRewardShowWindow.OnClose
**Requires:**
- InitialSign_RewardShowWindowByName
**Snippet:**
```lua
require("InitialSign_RewardShowWindowByName")
local InitialSignRewardShowWindow = {}
local uis, contentPane, msg

function InitialSignRewardShowWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.InitialSignRewardShowWindow.package, WinResConfig.InitialSignRewardShowWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetInitialSign_RewardShowWindowUis(contentPane)
    msg = bridgeObj.argTable[1]
```

---

## GL/InitialSignWindow.lua.lua
**Functions:**
- InitialSignWindow.OnInit
- InitialSignWindow.Init
- ce.clickFunc
- InitialSignWindow.UpdateUI
- InitialSignWindow.ShowSceneBg
- InitialSignWindow.QuitHide
- InitialSignWindow.InitBtn
- InitialSignWindow.HandleMessage
- InitialSignWindow.OnClose
**Requires:**
- InitialSign_InitialSignByName
- InitialSign_SignItemByName
**Snippet:**
```lua
require("InitialSign_InitialSignByName")
require("InitialSign_SignItemByName")
InitialSignWindow = {}
local sign, activateData, rewardData, signSceneCamera, item, bg, signInData, SceneRoot, signIndex

function InitialSignWindow.OnInit(com, data)
  sign = GetInitialSign_InitialSignUis(com)
  activateData = data
  signInData = SignData.activityData[activateData.id]
  InitialSignWindow.InitBtn()
```

---

## GL/InitialSign_CloseBtnByName.lua.lua
**Functions:**
- GetInitialSign_CloseBtnUis
**Snippet:**
```lua
function GetInitialSign_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/InitialSign_InitialSignAutoByName.lua.lua
**Functions:**
- GetInitialSign_InitialSignAutoUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetInitialSign_InitialSignAutoUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.BgLoader = ui:GetChild("BgLoader")
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.CloseBtn = ui:GetChild("CloseBtn")
```

---

## GL/InitialSign_InitialSignAutoWindowByName.lua.lua
**Functions:**
- GetInitialSign_InitialSignAutoWindowUis
**Requires:**
- InitialSign_InitialSignAutoByName
**Snippet:**
```lua
require("InitialSign_InitialSignAutoByName")

function GetInitialSign_InitialSignAutoWindowUis(ui)
  local uis = {}
  uis.Main = GetInitialSign_InitialSignAutoUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/InitialSign_InitialSignByName.lua.lua
**Functions:**
- GetInitialSign_InitialSignUis
**Requires:**
- CommonResource_BackGroundByName
- InitialSign_SignTipsByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("InitialSign_SignTipsByName")

function GetInitialSign_InitialSignUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.SignTips = GetInitialSign_SignTipsUis(ui:GetChild("SignTips"))
  uis.RewardShowBtn = ui:GetChild("RewardShowBtn")
```

---

## GL/InitialSign_PopupBgByName.lua.lua
**Functions:**
- GetInitialSign_PopupBgUis
**Snippet:**
```lua
function GetInitialSign_PopupBgUis(ui)
  local uis = {}
  
  uis.BlurLoader = ui:GetChild("BlurLoader")
  uis.root = ui
  return uis
end
```

---

## GL/InitialSign_RewardShowBtnByName.lua.lua
**Functions:**
- GetInitialSign_RewardShowBtnUis
**Snippet:**
```lua
function GetInitialSign_RewardShowBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/InitialSign_RewardShowByName.lua.lua
**Functions:**
- GetInitialSign_RewardShowUis
**Requires:**
- InitialSign_PopupBgByName
- InitialSign_RewardShowListByName
**Snippet:**
```lua
require("InitialSign_PopupBgByName")
require("InitialSign_RewardShowListByName")

function GetInitialSign_RewardShowUis(ui)
  local uis = {}
  uis.PopupBg = GetInitialSign_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.RewardShowList = GetInitialSign_RewardShowListUis(ui:GetChild("RewardShowList"))
  uis.root = ui
  return uis
```

---

## GL/InitialSign_RewardShowListByName.lua.lua
**Functions:**
- GetInitialSign_RewardShowListUis
**Snippet:**
```lua
function GetInitialSign_RewardShowListUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.root = ui
  return uis
end
```

---

## GL/InitialSign_RewardShowWindowByName.lua.lua
**Functions:**
- GetInitialSign_RewardShowWindowUis
**Requires:**
- InitialSign_RewardShowByName
**Snippet:**
```lua
require("InitialSign_RewardShowByName")

function GetInitialSign_RewardShowWindowUis(ui)
  local uis = {}
  uis.Main = GetInitialSign_RewardShowUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/InitialSign_ShowItemTipsAniByName.lua.lua
**Functions:**
- GetInitialSign_ShowItemTipsAniUis
**Requires:**
- InitialSign_ShowItemTipsByName
**Snippet:**
```lua
require("InitialSign_ShowItemTipsByName")

function GetInitialSign_ShowItemTipsAniUis(ui)
  local uis = {}
  uis.ShowItemTips = GetInitialSign_ShowItemTipsUis(ui:GetChild("ShowItemTips"))
  uis.root = ui
  return uis
end
```

---

## GL/InitialSign_ShowItemTipsByName.lua.lua
**Functions:**
- GetInitialSign_ShowItemTipsUis
**Snippet:**
```lua
function GetInitialSign_ShowItemTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.DayTxt = ui:GetChild("DayTxt")
  uis.Day1Txt = ui:GetChild("Day1Txt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.ItemList = ui:GetChild("ItemList")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## GL/InitialSign_SignItemAniByName.lua.lua
**Functions:**
- GetInitialSign_SignItemAniUis
**Requires:**
- InitialSign_SignItemByName
**Snippet:**
```lua
require("InitialSign_SignItemByName")

function GetInitialSign_SignItemAniUis(ui)
  local uis = {}
  uis.SignItem = GetInitialSign_SignItemUis(ui:GetChild("SignItem"))
  uis.root = ui
  return uis
end
```

---

## GL/InitialSign_SignItemByName.lua.lua
**Functions:**
- GetInitialSign_SignItemUis
**Snippet:**
```lua
function GetInitialSign_SignItemUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## GL/InitialSign_SignTipsByName.lua.lua
**Functions:**
- GetInitialSign_SignTipsUis
**Snippet:**
```lua
function GetInitialSign_SignTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/InputTextUtil.lua.lua
**Functions:**
- InputTextUtil.SetPasswordTextSetting
- InputTextUtil.IsPasswordLegal
- InputTextUtil.SetAccountTextSetting
**Snippet:**
```lua
local InputTextUtil = {}

function InputTextUtil.SetPasswordTextSetting(inputTextField)
  inputTextField.keyboardType = TouchScreenKeyboardType.NumberPad
  inputTextField.restrict = REGEX_TYPE_ENUM["A_Z&0_9"]
end

function InputTextUtil.IsPasswordLegal(password1, password2, showFloatTips)
  if nil == showFloatTips then
    showFloatTips = true
```

---

## GL/ItemGetShow_GetItemTips1ByName.lua.lua
**Functions:**
- GetItemGetShow_GetItemTips1Uis
**Requires:**
- ItemGetShow_ItemListByName
**Snippet:**
```lua
require("ItemGetShow_ItemListByName")

function GetItemGetShow_GetItemTips1Uis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.Item = GetItemGetShow_ItemListUis(ui:GetChild("Item"))
  uis.TitleEffectHolder = ui:GetChild("TitleEffectHolder")
  uis.root = ui
  return uis
```

---

## GL/ItemGetShow_GetItemTips2ByName.lua.lua
**Functions:**
- GetItemGetShow_GetItemTips2Uis
**Requires:**
- ItemGetShow_PopupBgByName
- ItemGetShow_GetItemTips1ByName
**Snippet:**
```lua
require("ItemGetShow_PopupBgByName")
require("ItemGetShow_GetItemTips1ByName")

function GetItemGetShow_GetItemTips2Uis(ui)
  local uis = {}
  uis.PopupBg = GetItemGetShow_PopupBgUis(ui:GetChild("PopupBg"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.GetItemTips1 = GetItemGetShow_GetItemTips1Uis(ui:GetChild("GetItemTips1"))
  uis.root = ui
```

---

## GL/ItemGetShow_GetItemTipsWindowByName.lua.lua
**Functions:**
- GetItemGetShow_GetItemTipsWindowUis
**Requires:**
- ItemGetShow_GetItemTips2ByName
**Snippet:**
```lua
require("ItemGetShow_GetItemTips2ByName")

function GetItemGetShow_GetItemTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetItemGetShow_GetItemTips2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/ItemGetShow_ItemListByName.lua.lua
**Functions:**
- GetItemGetShow_ItemListUis
**Snippet:**
```lua
function GetItemGetShow_ItemListUis(ui)
  local uis = {}
  
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## GL/ItemGetShow_PopupBgByName.lua.lua
**Functions:**
- GetItemGetShow_PopupBgUis
**Snippet:**
```lua
function GetItemGetShow_PopupBgUis(ui)
  local uis = {}
  
  uis.BlurLoader = ui:GetChild("BlurLoader")
  uis.root = ui
  return uis
end
```

---

## GL/ItemGetTipsWindow.lua.lua
**Functions:**
- ItemGetTipsWindow.ReInitData
- ItemGetTipsWindow.OnInit
- ItemGetTipsWindow.UpdateInfo
- uis.Main.WordList.itemRenderer
- uis.Main.WordList.itemRenderer
- ItemGetTipsWindow.GetGoToData
- ItemGetTipsWindow.StageIsUnlock
- ItemGetTipsWindow.ShowAllGoTo
- uis.Main.Way.GetStripList.itemRenderer
- ItemGetTipsWindow.GetCanLvLock
- ItemGetTipsWindow.ShowGoTo
- uis.Main.Way.GetStripList.itemRenderer
- ItemGetTipsWindow.InitBtn
- ItemGetTipsWindow.CloseWindow
- ItemGetTipsWindow.OnShown
- ItemGetTipsWindow.OnHide
- ItemGetTipsWindow.OnClose
- ItemGetTipsWindow.HandleMessage
**Requires:**
- Message_ItemGetTipsWindowByName
**Snippet:**
```lua
require("Message_ItemGetTipsWindowByName")
local ItemGetTipsWindow = {}
local uis, contentPane, itemConfig, wayData, itemId, itemNeedCount, fromCardId, isJump, jumpData, notShowWay

function ItemGetTipsWindow.ReInitData()
end

function ItemGetTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ItemGetTipsWindow.package, WinResConfig.ItemGetTipsWindow.comName, function(com)
    contentPane = com
```

---

## GL/ItemTipsWindow.lua.lua
**Functions:**
- ItemTipsWindow.ReInitData
- ItemTipsWindow.OnInit
- ItemTipsWindow.CheckItemTime
- ItemTipsWindow.InitItemInfo
- Modular.WordList.itemRenderer
- ItemTipsWindow.LoadLookBtn
- ItemTipsWindow.LookGift
- ItemTipsWindow.GetEnergyMax
- ItemTipsWindow.GetMonthPayProductData
- ItemTipsWindow.InitStrip
- ItemTipsWindow.GetGesture
- ItemTipsWindow.UpdateInfo
- uis.Main.NumberModular.WordList.itemRenderer
- ItemTipsWindow.GetSelectItem
- ItemTipsWindow.InitSuperPassPart
- passTips.ItemList.itemRenderer
- ItemTipsWindow.InitHighPassPart
- passTips.ItemList.itemRenderer
- ItemTipsWindow.InitMonthCard
- ItemTipsWindow.InitBreachGift
- tips.ItemList.itemRenderer
- itemList.itemRenderer
- uis.Main.NumberModular.WordList.itemRenderer
- ItemTipsWindow.GetBreachGiftItemData
- ItemTipsWindow.GetSelectCardData
- ItemTipsWindow.SelectCard
- ItemTipsWindow.ShowCardOneLine
- list.itemRenderer
- ItemTipsWindow.ShowCardDetails
- skillList.itemRenderer
- ItemTipsWindow.GetMessageBoxTips
- ItemTipsWindow.GetSelectFashionData
- ItemTipsWindow.SelectFashion
- clothesCom.ClothesList.itemRenderer
- ItemTipsWindow.ShowFashionDetails
- ItemTipsWindow.SelectItem
- uis.Main.NumberModular.WordList.itemRenderer
- uis.Main.NumberModular.WordList.itemRenderer
- ItemTipsWindow.CheckIsEnergy
- ItemTipsWindow.ConvertItem
- Modular.WordList.itemRenderer
- ItemTipsWindow.GetGoToData
- ItemTipsWindow.StageIsUnlock
- ItemTipsWindow.ShowAllGoTo
- uis.Main.MainModular.Way.GetStripList.itemRenderer
- ItemTipsWindow.GetCanLvLock
- ItemTipsWindow.ShowGoTo
- uis.Main.MainModular.Way.GetStripList.itemRenderer
- ItemTipsWindow.UpdateExpireTime
- ItemTipsWindow.InitBtn
- ItemTipsWindow.CloseWindow
- ItemTipsWindow.OnShown
- ItemTipsWindow.OnHide
- ItemTipsWindow.OnClose
- ItemTipsWindow.HandleMessage
**Requires:**
- Message_ItemTipsWindowByName
**Snippet:**
```lua
require("Message_ItemTipsWindowByName")
local ItemTipsWindow = {}
local uis, contentPane, itemInfo, itemConfig, selectIndex, selectItemId, isLook, isUse, wayData, energyNum, energyMax, itemType, haveCount, indexMap, jumpData, itemTime, viewOnly, sureCallback, buyNum
local SELECT_TYPE = {
  Item = 1,
  Card = 2,
  Fashion = 3
}

function ItemTipsWindow.ReInitData()
```

---

## GL/Json.lua.lua
**Functions:**
- json.encode
- json.decode
- json.null
- decode_scanArray
- decode_scanComment
- decode_scanConstant
- decode_scanNumber
- decode_scanObject
- decode_scanString
- decode_scanWhitespace
- json_private.encodeString
- isArray
- isEncodable
**Requires:**
- math
- string
- table
**Snippet:**
```lua
local math = require("math")
local string = require("string")
local table = require("table")
local json = {}
local json_private = {}
json.EMPTY_ARRAY = {}
json.EMPTY_OBJECT = {}
local decode_scanArray, decode_scanComment, decode_scanConstant, decode_scanNumber, decode_scanObject, decode_scanString, decode_scanWhitespace, isArray, isEncodable

function json.encode(v)
```

---

## GL/Land_AccountBtnByName.lua.lua
**Functions:**
- GetLand_AccountBtnUis
**Snippet:**
```lua
function GetLand_AccountBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Land_AccountByName.lua.lua
**Functions:**
- GetLand_AccountUis
**Requires:**
- Land_AccountInputByName
- Land_AccountRegisterByName
**Snippet:**
```lua
require("Land_AccountInputByName")
require("Land_AccountRegisterByName")

function GetLand_AccountUis(ui)
  local uis = {}
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.AccountInput = GetLand_AccountInputUis(ui:GetChild("AccountInput"))
  uis.AccountRegister = GetLand_AccountRegisterUis(ui:GetChild("AccountRegister"))
  uis.SwitchBtn = ui:GetChild("SwitchBtn")
  uis.c1Ctr = ui:GetController("c1")
```

---

## GL/Land_AccountDisplayByName.lua.lua
**Functions:**
- GetLand_AccountDisplayUis
**Snippet:**
```lua
function GetLand_AccountDisplayUis(ui)
  local uis = {}
  
  uis.AccountTxt = ui:GetChild("AccountTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Land_AccountInputByName.lua.lua
**Functions:**
- GetLand_AccountInputUis
**Requires:**
- Land_InputWordByName
**Snippet:**
```lua
require("Land_InputWordByName")

function GetLand_AccountInputUis(ui)
  local uis = {}
  uis.Account = GetLand_InputWordUis(ui:GetChild("Account"))
  uis.Password1 = GetLand_InputWordUis(ui:GetChild("Password1"))
  uis.AccountBtn = ui:GetChild("AccountBtn")
  uis.root = ui
  return uis
end
```

---

## GL/Land_AccountRegisterByName.lua.lua
**Functions:**
- GetLand_AccountRegisterUis
**Requires:**
- Land_InputWordByName
**Snippet:**
```lua
require("Land_InputWordByName")

function GetLand_AccountRegisterUis(ui)
  local uis = {}
  uis.Account = GetLand_InputWordUis(ui:GetChild("Account"))
  uis.Password1 = GetLand_InputWordUis(ui:GetChild("Password1"))
  uis.Password2 = GetLand_InputWordUis(ui:GetChild("Password2"))
  uis.AgreeCheckBtn = ui:GetChild("AgreeCheckBtn")
  uis.AccountBtn = ui:GetChild("AccountBtn")
  uis.root = ui
```

---

## GL/Land_AgeBtnByName.lua.lua
**Functions:**
- GetLand_AgeBtnUis
**Snippet:**
```lua
function GetLand_AgeBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Land_AgeTipsByName.lua.lua
**Functions:**
- GetLand_AgeTipsUis
**Snippet:**
```lua
function GetLand_AgeTipsUis(ui)
  local uis = {}
  
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.SurBtn = ui:GetChild("SurBtn")
  uis.WordList = ui:GetChild("WordList")
  uis.root = ui
  return uis
end
```

---

## GL/Land_AgeWordByName.lua.lua
**Functions:**
- GetLand_AgeWordUis
**Snippet:**
```lua
function GetLand_AgeWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Land_AgreeCheckBtnByName.lua.lua
**Functions:**
- GetLand_AgreeCheckBtnUis
**Snippet:**
```lua
function GetLand_AgreeCheckBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/Land_AgreementByName.lua.lua
**Functions:**
- GetLand_AgreementUis
**Snippet:**
```lua
function GetLand_AgreementUis(ui)
  local uis = {}
  
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.AgreeCheckBtn = ui:GetChild("AgreeCheckBtn")
  uis.SurBtn = ui:GetChild("SurBtn")
  uis.WordList = ui:GetChild("WordList")
  uis.root = ui
  return uis
```

---

## GL/Land_BackGroundByName.lua.lua
**Functions:**
- GetLand_BackGroundUis
**Snippet:**
```lua
function GetLand_BackGroundUis(ui)
  local uis = {}
  
  uis.BackGroundLoader = ui:GetChild("BackGroundLoader")
  uis.BackGroundHolder = ui:GetChild("BackGroundHolder")
  uis.root = ui
  return uis
end
```

---

## GL/Land_CloseBtnByName.lua.lua
**Functions:**
- GetLand_CloseBtnUis
**Snippet:**
```lua
function GetLand_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Land_FilingsWordByName.lua.lua
**Functions:**
- GetLand_FilingsWordUis
**Snippet:**
```lua
function GetLand_FilingsWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Land_InputWordByName.lua.lua
**Functions:**
- GetLand_InputWordUis
**Snippet:**
```lua
function GetLand_InputWordUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Land_LandByName.lua.lua
**Functions:**
- GetLand_LandUis
**Requires:**
- Land_BackGroundByName
- Land_StateByName
- Land_AccountByName
- Land_FilingsWordByName
- Land_TabRegionScreenByName
- Land_PopupByName
**Snippet:**
```lua
require("Land_BackGroundByName")
require("Land_StateByName")
require("Land_AccountByName")
require("Land_FilingsWordByName")
require("Land_TabRegionScreenByName")
require("Land_PopupByName")

function GetLand_LandUis(ui)
  local uis = {}
  uis.BackGround = GetLand_BackGroundUis(ui:GetChild("BackGround"))
```

---

## GL/Land_LandTestByName.lua.lua
**Functions:**
- GetLand_LandTestUis
**Snippet:**
```lua
function GetLand_LandTestUis(ui)
  local uis = {}
  
  uis.Title1Txt = ui:GetChild("Title1Txt")
  uis.Subtitle1Txt = ui:GetChild("Subtitle1Txt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PasswordTxt = ui:GetChild("PasswordTxt")
  uis.Title2Txt = ui:GetChild("Title2Txt")
  uis.Subtitle2Txt = ui:GetChild("Subtitle2Txt")
  uis.OtherList = ui:GetChild("OtherList")
```

---

## GL/Land_LandWindowByName.lua.lua
**Functions:**
- GetLand_LandWindowUis
**Requires:**
- Land_LandByName
**Snippet:**
```lua
require("Land_LandByName")

function GetLand_LandWindowUis(ui)
  local uis = {}
  uis.Main = GetLand_LandUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/Land_MaintenanceByName.lua.lua
**Functions:**
- GetLand_MaintenanceUis
**Snippet:**
```lua
function GetLand_MaintenanceUis(ui)
  local uis = {}
  
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.SurBtn = ui:GetChild("SurBtn")
  uis.WordList = ui:GetChild("WordList")
  uis.root = ui
  return uis
end
```

---

## GL/Land_MaintenanceWordByName.lua.lua
**Functions:**
- GetLand_MaintenanceWordUis
**Snippet:**
```lua
function GetLand_MaintenanceWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Land_NoticeByName.lua.lua
**Functions:**
- GetLand_NoticeUis
**Snippet:**
```lua
function GetLand_NoticeUis(ui)
  local uis = {}
  
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.root = ui
  return uis
end
```

---

## GL/Land_NoticeCloseBtnByName.lua.lua
**Functions:**
- GetLand_NoticeCloseBtnUis
**Snippet:**
```lua
function GetLand_NoticeCloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Land_NoticePicByName.lua.lua
**Functions:**
- GetLand_NoticePicUis
**Snippet:**
```lua
function GetLand_NoticePicUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## GL/Land_NoticeWordByName.lua.lua
**Functions:**
- GetLand_NoticeWordUis
**Snippet:**
```lua
function GetLand_NoticeWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Land_PopupBgByName.lua.lua
**Functions:**
- GetLand_PopupBgUis
**Snippet:**
```lua
function GetLand_PopupBgUis(ui)
  local uis = {}
  
  uis.BlurLoader = ui:GetChild("BlurLoader")
  uis.root = ui
  return uis
end
```

---

## GL/Land_PopupByName.lua.lua
**Functions:**
- GetLand_PopupUis
**Requires:**
- Land_PopupBgByName
- Land_AgreementByName
- Land_NoticeByName
- Land_RepairByName
- Land_AgeTipsByName
- Land_MaintenanceByName
**Snippet:**
```lua
require("Land_PopupBgByName")
require("Land_AgreementByName")
require("Land_NoticeByName")
require("Land_RepairByName")
require("Land_AgeTipsByName")
require("Land_MaintenanceByName")

function GetLand_PopupUis(ui)
  local uis = {}
  uis.PopupBgLand = GetLand_PopupBgUis(ui:GetChild("PopupBgLand"))
```

---

## GL/Land_RepairByName.lua.lua
**Functions:**
- GetLand_RepairUis
**Snippet:**
```lua
function GetLand_RepairUis(ui)
  local uis = {}
  
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SurBtn = ui:GetChild("SurBtn")
  uis.root = ui
  return uis
end
```

---

## GL/Land_SetBtnByName.lua.lua
**Functions:**
- GetLand_SetBtnUis
**Snippet:**
```lua
function GetLand_SetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Land_StateByName.lua.lua
**Functions:**
- GetLand_StateUis
**Requires:**
- Land_AccountDisplayByName
**Snippet:**
```lua
require("Land_AccountDisplayByName")

function GetLand_StateUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.CloseTipsTxt = ui:GetChild("CloseTipsTxt")
  uis.AccountDisplay = GetLand_AccountDisplayUis(ui:GetChild("AccountDisplay"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## GL/Land_SurBtnByName.lua.lua
**Functions:**
- GetLand_SurBtnUis
**Snippet:**
```lua
function GetLand_SurBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Land_SwitchBtnByName.lua.lua
**Functions:**
- GetLand_SwitchBtnUis
**Snippet:**
```lua
function GetLand_SwitchBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Land_TabBtnByName.lua.lua
**Functions:**
- GetLand_TabBtnUis
**Snippet:**
```lua
function GetLand_TabBtnUis(ui)
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

## GL/Land_TabRegionByName.lua.lua
**Functions:**
- GetLand_TabRegionUis
**Snippet:**
```lua
function GetLand_TabRegionUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## GL/Land_TabRegionScreenByName.lua.lua
**Functions:**
- GetLand_TabRegionScreenUis
**Requires:**
- Land_TabRegionByName
**Snippet:**
```lua
require("Land_TabRegionByName")

function GetLand_TabRegionScreenUis(ui)
  local uis = {}
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.TabRegion = GetLand_TabRegionUis(ui:GetChild("TabRegion"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/Land_TouchStartBtnByName.lua.lua
**Functions:**
- GetLand_TouchStartBtnUis
**Snippet:**
```lua
function GetLand_TouchStartBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Land_VerticalScroll1BarByName.lua.lua
**Functions:**
- GetLand_VerticalScroll1BarUis
**Snippet:**
```lua
function GetLand_VerticalScroll1BarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/Land_VerticalScroll1Bar_gripByName.lua.lua
**Functions:**
- GetLand_VerticalScroll1Bar_gripUis
**Snippet:**
```lua
function GetLand_VerticalScroll1Bar_gripUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Land_WordByName.lua.lua
**Functions:**
- GetLand_WordUis
**Snippet:**
```lua
function GetLand_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Language.lua.lua
**Functions:**
- Language.Init
- Language.UpdateLanguage
- Language.UpdateLanguageVoice
- Language.ReplaceLanguageVoicePath
**Snippet:**
```lua
local Language = {
  curLanguage = nil,
  curLanguageVoice = nil,
  curVoiceFolder = nil,
  wordConfigName = nil
}
LANGUAGE_ENUM = {
  CN = "cn",
  JP = "jp",
  TC = "tc"
```

---

## GL/LevelUpTipsWindow.lua.lua
**Functions:**
- LevelUpTipsWindow.ReInitData
- LevelUpTipsWindow.OnInit
- LevelUpTipsWindow.UpdateTextDisplay
- LevelUpTipsWindow.InitBtn
- LevelUpTipsWindow.OnClose
**Requires:**
- Card_LevelUpTipsWindowByName
**Snippet:**
```lua
require("Card_LevelUpTipsWindowByName")
local LevelUpTipsWindow = {}
local uis, contentPane, lv

function LevelUpTipsWindow.ReInitData()
end

function LevelUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.LevelUpTipsWindow.package, WinResConfig.LevelUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## GL/LevelUpWindow.lua.lua
**Functions:**
- LevelUpWindow.ReInitData
- LevelUpWindow.OnInit
- LevelUpWindow.LoadBgTexture
- LevelUpWindow.UpdateInfo
- uis.Main.ContentList.itemRenderer
- LevelUpWindow.GetUnlocked
- LevelUpWindow.InitBtn
- LevelUpWindow.OnClose
**Requires:**
- PlayerLevelUp_LevelUpWindowByName
**Snippet:**
```lua
require("PlayerLevelUp_LevelUpWindowByName")
local LevelUpWindow = {}
local uis, contentPane, bgPrefab, closeCallBack

function LevelUpWindow.ReInitData()
end

function LevelUpWindow.OnInit(bridgeObj)
  bridgeObj:SetView(WinResConfig.LevelUpWindow.package, WinResConfig.LevelUpWindow.comName, function(com)
    contentPane = com
```

---

## GL/LoadCSVariable.lua.lua
**Functions:**
- LoadCSVariable
**Snippet:**
```lua
DesignScreen = {width = 1334, height = 750}
local CS = CS
local UnityEngine = CS.UnityEngine
local fairyGUI = CS.FairyGUI

function LoadCSVariable()
  GameObject = UnityEngine.GameObject
  Camera = UnityEngine.Camera
  Vector2 = UnityEngine.Vector2
  Vector3 = UnityEngine.Vector3
```

---

## GL/Loading_BattleLoadingWindowByName.lua.lua
**Functions:**
- GetLoading_BattleLoadingWindowUis
**Requires:**
- Loading_EffectAniByName
**Snippet:**
```lua
require("Loading_EffectAniByName")

function GetLoading_BattleLoadingWindowUis(ui)
  local uis = {}
  uis.EffectAni = GetLoading_EffectAniUis(ui:GetChild("EffectAni"))
  uis.root = ui
  return uis
end
```

---

## GL/Loading_EffectAniByName.lua.lua
**Functions:**
- GetLoading_EffectAniUis
**Snippet:**
```lua
function GetLoading_EffectAniUis(ui)
  local uis = {}
  
  uis.EffectLoader = ui:GetChild("EffectLoader")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## GL/Loading_LoginLoadingWindowByName.lua.lua
**Functions:**
- GetLoading_LoginLoadingWindowUis
**Requires:**
- Loading_EffectAniByName
**Snippet:**
```lua
require("Loading_EffectAniByName")

function GetLoading_LoginLoadingWindowUis(ui)
  local uis = {}
  uis.EffectAni = GetLoading_EffectAniUis(ui:GetChild("EffectAni"))
  uis.root = ui
  return uis
end
```

---

## GL/Loading_NetCheckByName.lua.lua
**Functions:**
- GetLoading_NetCheckUis
**Requires:**
- CommonResource_PopupBgByName
- Loading_EffectAniByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Loading_EffectAniByName")

function GetLoading_NetCheckUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.EffectAni = GetLoading_EffectAniUis(ui:GetChild("EffectAni"))
  uis.root = ui
  return uis
end
```

---

## GL/LoadLuaVariable.lua.lua
**Functions:**
- LoadLuaVariable
**Requires:**
- Util
- LoadModule
- UpdateManager
- CameraUtil
- SortingHelper
- GlobalConst
- GlobalConfig
- UIHelper
- MathUtil
- NumberUtil
- UIUtil
- ModelUtil
- TimeUtil
- TimerUtil
- EffectUtil
- FloatTipsUtil
- InfoTipsUtil
- MessageBox
- EnterClampUtil
- PlayerPrefsUtil
- OprRecordUtil
- StringUtil
- FunctionQueueUtil
- SettingUtil
- SoundUtil
- GetItemTips
- ResolutionHandler
- TableData
- CurrencyReturnWindow
- Net
- InputTextUtil
- Json
- MsgWaiter
- Language
**Snippet:**
```lua
local require = require

function LoadLuaVariable()
  require("Util")
  require("LoadModule")
  UpdateManager = require("UpdateManager")
  CameraUtil = require("CameraUtil")
  SortingHelper = require("SortingHelper")
  require("GlobalConst")
  require("GlobalConfig")
```

---

## GL/LoadModule.lua.lua
**Functions:**
- ld
**Snippet:**
```lua
function ld(folder_name, callBack)
  if nil == folder_name then
    print("传入的module name 为空")
    
    return
  end
  local lua_str = folder_name .. "ScriptList"
  if nil ~= package.loaded[lua_str] then
    if callBack then
      callBack()
```

---

## GL/LoadPersistUIPackage.lua.lua
**Functions:**
- LoadPersistUIPackage
**Snippet:**
```lua
function LoadPersistUIPackage()
  UIMgr:LoadPackages({
    "CommonResource",
    
    "ItemIcon",
    "SkillIcon",
    "SkillStarIcon",
    "Message",
    "UIFont",
    "UIBackGround",
```

---

## GL/LoadSensitiveWord.lua.lua
**Functions:**
- LoadSensitiveWord
**Requires:**
- SensitiveWordsUtil
**Snippet:**
```lua
function LoadSensitiveWord()
  require("SensitiveWordsUtil")
  
  SensitiveWordsUtil.InitWords()
end

LoadSensitiveWord()
```

---

## GL/LoginData.lua.lua
**Functions:**
- LoginData.Init
- LoginData.ClearData
- LoginData.SetTimeScale
- LoginData.SaveLoginData
- LoginData.SaveLoginAddress
- LoginData.SaveTimezoneOffset
- LoginData.GetConnectIpAndPort
- LoginData.GetAccount
- LoginData.GetPassword
- LoginData.SetAccount
- LoginData.GetAuthUrl
- LoginData.GetSDKServerId
- LoginData.GetClientServiceUrl
- LoginData.GetSelectAuthInfo
- LoginData.SetSelectAuthInfo
- LoginData.SetSeverVersion
- LoginData.GetServerVersion
- LoginData.GetPlatform
- LoginData.SetSeverTime
- LoginData.SetRefreshDaySec
- LoginData.GetRefreshDaySecTime
- LoginData.SetLoginDays
- LoginData.SetResVersion
- LoginData.UpdateResVersion
- LoginData.GetCurServerTime
- LoginData.ClearLastAccount
**Snippet:**
```lua
LoginData = {}

function LoginData.Init()
  LoginData.selectAuthInfo = {address = "", name = ""}
  LoginData.lastAccount = nil
  LoginData.lastPassword = nil
end

function LoginData.ClearData()
  LoginData.token = nil
```

---

## GL/LoginLoadingWindow.lua.lua
**Functions:**
- LoginLoadingWindow.ReInitData
- LoginLoadingWindow.OnInit
- LoginLoadingWindow.UpdateInfo
- LoginLoadingWindow.ShowAnimOut
- LoginLoadingWindow.InitBtn
- LoginLoadingWindow.OnClose
- LoginLoadingWindow.HandleMessage
**Requires:**
- Loading_LoginLoadingWindowByName
**Snippet:**
```lua
require("Loading_LoginLoadingWindowByName")
local LoginLoadingWindow = {}
local uis, contentPane, onShowAnimationEndCallback, addCallbackIn

function LoginLoadingWindow.ReInitData()
end

local effect, dontShowEffect

function LoginLoadingWindow.OnInit(bridgeObj)
```

---

## GL/LoginMgr.lua.lua
**Functions:**
- LoginMgr.InitLoginStatus
- LoginMgr.ConnectSDKAuth
- LoginMgr.DealSDKCallback
- LoginMgr.Register
- LoginMgr.ConnectLoginServer
- LoginMgr.ConnectSocket
- LoginMgr.InitHeartBeatCheck
- LoginMgr.CorrectTimeScale
- LoginMgr.HeartBeatCheckLoop
- LoginMgr.ReturnToLogin
- LoginMgr.StopGame
- LoginMgr.GetLandNotice
- LoginMgr.Logout
- LoginMgr.ChangeAccount
- LoginMgr.OpenBugReport
- LoginMgr.OpenUserCenter
- LoginMgr.LoginCallback
- LoginMgr.LogoutCallback
- LoginMgr.PayCallback
- LoginMgr.ExitCallback
- LoginMgr.GetDeviceIdCallback
- LoginMgr.GetChannelIdCallback
- LoginMgr.CloseAccountCallback
**Requires:**
- MsgWaiter
**Snippet:**
```lua
LoginMgr = {
  maxResId = nil,
  bilibili_uid = nil,
  bilibili_username = nil
}
local HEART_BEAT_INTERVAL = 25
local GET_ACTOR_INFO_INTERVAL = 300
local UPDATE_BATTERY_INTERVAL = 300
local SOCKET_CHECK_INTERVAL = 3
local sendTime = 0
```

---

## GL/LoginScriptList.lua.lua
**Requires:**
- LoginMgr
- LoginData
- LoginService
**Snippet:**
```lua
local require = require
require("LoginMgr")
require("LoginData")
require("LoginService")
```

---

## GL/LoginService.lua.lua
**Functions:**
- LoginService.Init
- LoginService.EnterGameReq
- LoginService.DealEnterGameRsp
- LoginService.HeartBeatReq
- LoginService.DealHeartBeatRsp
- LoginService.DealKickOffNotify
**Requires:**
- LoadSensitiveWord
- LoadSensitiveWord
- LoadSensitiveWord
**Snippet:**
```lua
LoginService = {}

function LoginService.Init()
  Net.AddListener(Proto.MsgName.EnterGameRsp, LoginService.DealEnterGameRsp)
  Net.AddListener(Proto.MsgName.HeartBeatRsp, LoginService.DealHeartBeatRsp)
  Net.AddListener(Proto.MsgName.KickOffNotify, LoginService.DealKickOffNotify)
end

function LoginService.EnterGameReq()
  local msg = {}
```

---

## GL/LoginWindow.lua.lua
**Functions:**
- LoginWindow.ReInitData
- LoginWindow.OnInit
- LoginWindow.OnShowAnimationEnd
- LoginWindow.UpdateInfo
- LoginWindow.UpdateVersion
- LoginWindow.UpdateID
- LoginWindow.UpdateBackground
- LoginWindow.InitBtn
- LoginWindow.UpdateDefault
- LoginWindow.OpenAge
- LoginWindow.UpdateSetting
- LoginWindow.UpdateRegister
- LoginWindow.UpdateLogin
- LoginWindow.UpdateServerClose
- LoginWindow.UpdateBan
- LoginWindow.UpdatePolicy
- LoginWindow.UpdateAgreement
- LoginWindow.OpenBilibiliPolicy
- LoginWindow.OpenBilibiliAgreement
- LoginWindow.OpenHaoplayPolicy
- LoginWindow.OpenHaoplayAgreement
- LoginWindow.UpdateNotice
- LoginWindow.ClickLink
- LoginWindow.UpdateRepair
- LoginWindow.ChangeAccount
- LoginWindow.UpdateLogout
- LoginWindow.ShowAccountPanel
- LoginWindow.HideAccountPanel
- LoginWindow.CreateServerList
- LoginWindow.ClickEnterGame
- LoginWindow.OnShown
- LoginWindow.OnHide
- LoginWindow.OnPreClose
- LoginWindow.OnClose
- LoginWindow.HandleMessage
**Requires:**
- Land_LandByName
- Land_LandTestByName
- MsgWaiter
- MsgWaiter
**Snippet:**
```lua
require("Land_LandByName")
require("Land_LandTestByName")
local testLogin = true
local LoginWindow = {}
local uis, contentPane, landTestUis
VideoManager = CS.VideoManager.Singleton
SDKManager = CS.SDKManager.Instance

function LoginWindow.ReInitData()
end
```

---

## GL/LotteryCardShow_CardTipsByName.lua.lua
**Functions:**
- GetLotteryCardShow_CardTipsUis
**Snippet:**
```lua
function GetLotteryCardShow_CardTipsUis(ui)
  local uis = {}
  
  uis.StarList = ui:GetChild("StarList")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.CardNameENTxt = ui:GetChild("CardNameENTxt")
  uis.ElementList = ui:GetChild("ElementList")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## GL/LotteryCardShow_ContentTipsByName.lua.lua
**Functions:**
- GetLotteryCardShow_ContentTipsUis
**Requires:**
- LotteryCardShow_ContentTipsHeadByName
**Snippet:**
```lua
require("LotteryCardShow_ContentTipsHeadByName")

function GetLotteryCardShow_ContentTipsUis(ui)
  local uis = {}
  uis.HeadLoader = GetLotteryCardShow_ContentTipsHeadUis(ui:GetChild("HeadLoader"))
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## GL/LotteryCardShow_ContentTipsHeadByName.lua.lua
**Functions:**
- GetLotteryCardShow_ContentTipsHeadUis
**Snippet:**
```lua
function GetLotteryCardShow_ContentTipsHeadUis(ui)
  local uis = {}
  
  uis.HeadLoader = ui:GetChild("HeadLoader")
  uis.root = ui
  return uis
end
```

---

## GL/LotteryCardShow_DialogueByName.lua.lua
**Functions:**
- GetLotteryCardShow_DialogueUis
**Snippet:**
```lua
function GetLotteryCardShow_DialogueUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/LotteryCardShow_ElementByName.lua.lua
**Functions:**
- GetLotteryCardShow_ElementUis
**Snippet:**
```lua
function GetLotteryCardShow_ElementUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/LotteryCardShow_OccupationByName.lua.lua
**Functions:**
- GetLotteryCardShow_OccupationUis
**Snippet:**
```lua
function GetLotteryCardShow_OccupationUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/LotteryCardShow_PaintingShowByName.lua.lua
**Functions:**
- GetLotteryCardShow_PaintingShowUis
**Requires:**
- CommonResource_BackGroundByName
- LotteryCardShow_OccupationByName
- LotteryCardShow_PicByName
- LotteryCardShow_CardTipsByName
- LotteryCardShow_DialogueByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("LotteryCardShow_OccupationByName")
require("LotteryCardShow_PicByName")
require("LotteryCardShow_CardTipsByName")
require("LotteryCardShow_DialogueByName")

function GetLotteryCardShow_PaintingShowUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Occupation = GetLotteryCardShow_OccupationUis(ui:GetChild("Occupation"))
```

---

## GL/LotteryCardShow_PaintingShowWindowByName.lua.lua
**Functions:**
- GetLotteryCardShow_PaintingShowWindowUis
**Requires:**
- LotteryCardShow_PaintingShowByName
**Snippet:**
```lua
require("LotteryCardShow_PaintingShowByName")

function GetLotteryCardShow_PaintingShowWindowUis(ui)
  local uis = {}
  uis.Main = GetLotteryCardShow_PaintingShowUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/LotteryCardShow_PicByName.lua.lua
**Functions:**
- GetLotteryCardShow_PicUis
**Snippet:**
```lua
function GetLotteryCardShow_PicUis(ui)
  local uis = {}
  
  uis.CardShowLoader = ui:GetChild("CardShowLoader")
  uis.CardShowHolder = ui:GetChild("CardShowHolder")
  uis.root = ui
  return uis
end
```

---

## GL/LotteryCardShow_SkipBtnByName.lua.lua
**Functions:**
- GetLotteryCardShow_SkipBtnUis
**Snippet:**
```lua
function GetLotteryCardShow_SkipBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/LotteryCardShow_StarByName.lua.lua
**Functions:**
- GetLotteryCardShow_StarUis
**Snippet:**
```lua
function GetLotteryCardShow_StarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/LotteryComplementWindow.lua.lua
**Functions:**
- LotteryComplementWindow.ReInitData
- LotteryComplementWindow.OnInit
- LotteryComplementWindow.UpdateInfo
- LotteryComplementWindow.CloseWindow
- LotteryComplementWindow.InitBtn
- LotteryComplementWindow.OnClose
**Requires:**
- Lottery_ComplementWindowByName
**Snippet:**
```lua
require("Lottery_ComplementWindowByName")
local LotteryComplementWindow = {}
local uis, contentPane, costInfo, callBack

function LotteryComplementWindow.ReInitData()
end

function LotteryComplementWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.LotteryComplementWindow.package, WinResConfig.LotteryComplementWindow.comName, function(com)
    contentPane = com
```

---

## GL/LotteryData.lua.lua
**Functions:**
- LotteryData.IsOpenById
- LotteryData.GetTpById
- LotteryData.GetGachaPool
- LotteryData.GetExchangeNumById
- LotteryData.SavePoint
**Snippet:**
```lua
LotteryData = {
  Info = {},
  curPage = 0,
  drops = {},
  curPoolId = 0,
  showReview = false
}

function LotteryData.IsOpenById(id)
  if id and LotteryData.Info.openList then
```

---

## GL/LotteryEffect.lua.lua
**Functions:**
- LotteryEffect.GetResultSoundPath
- LotteryEffect.ShowLotteryScene
- LotteryEffect.CloseLotteryScene
- LotteryEffect.PlayCardEffect
- LotteryEffect.CloseCardEffect
- LotteryEffect.AutoClick
**Snippet:**
```lua
LotteryEffect = {}
local sceneEffect, cardEffect
local lotteryEffectPath = "Assets/Art/Effects/Prefab/UI_prefab/Gacha/FX_gacha_all.prefab"
local lotteryOneCardEffectPath = "Assets/Art/Effects/Prefab/UI_prefab/Gacha/FX_gacha_showcase.prefab"
local lotteryOneCardHighEffectPath = "Assets/Art/Effects/Prefab/UI_prefab/Gacha/FX_gacha_showcase_high.prefab"
local lotteryOneCardOrangeEffectPath = "Assets/Art/Effects/Prefab/UI_prefab/Gacha/FX_gacha_showcase_orange.prefab"
local lotterySoundPath = {
  IN = "event:/sfx/sfx_ui/ui_zhaomu/zhaomu_p1",
  CLICK = "event:/sfx/sfx_ui/ui_zhaomu/zhaomu_click",
  END_1 = "event:/sfx/sfx_ui/ui_zhaomu/zhaomu_explosion_comn",
```

---

## GL/LotteryExchangeWindow.lua.lua
**Functions:**
- LotteryExchangeWindow.OnInit
- LotteryExchangeWindow.GetItemName
- LotteryExchangeWindow.UpdateText
- LotteryExchangeWindow.RefreshTp
- LotteryExchangeWindow.GetAddAttrList
- LotteryExchangeWindow.InitList
- uis.Main.ExchangeList.itemRenderer
- starList.itemRenderer
- LotteryExchangeWindow.GetCardNameById
- LotteryExchangeWindow.IsExchangeMax
- LotteryExchangeWindow.InitBtn
- LotteryExchangeWindow.HandleMessage
- LotteryExchangeWindow.OnClose
**Requires:**
- Lottery_ExchangeWindowByName
**Snippet:**
```lua
require("Lottery_ExchangeWindowByName")
local LotteryExchangeWindow = {}
local uis, contentPane, gachaId, tp, data, jumpTb

function LotteryExchangeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.LotteryExchangeWindow.package, WinResConfig.LotteryExchangeWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetLottery_ExchangeWindowUis(contentPane)
    gachaId = bridgeObj.argTable[1]
```

---

## GL/LotteryMgr.lua.lua
**Functions:**
- LotteryMgr.SetCardTips
- starList.itemRenderer
- LotteryMgr.GetGachaNumber
- LotteryMgr.ShowReview
**Snippet:**
```lua
LotteryMgr = {}

function LotteryMgr.SetCardTips(cardTips, data)
  if data then
    cardTips:GetChild("NameTxt").text = data.name()
    cardTips:GetChild("CVTxt").text = data.cv_name()
    local element = cardTips:GetChild("Element")
    if element then
      ChangeUIController(element, nil, data.element_type[1])
    end
```

---

## GL/LotteryPaintingShowWindow.lua.lua
**Functions:**
- LotteryPaintingShowWindow.OnInit
- LotteryPaintingShowWindow.Init
- uis.Main.CardTips.StarList.itemRenderer
- LotteryPaintingShowWindow.StopTalk
- LotteryPaintingShowWindow.HideTips
- LotteryPaintingShowWindow.UpdateTips
- LotteryPaintingShowWindow.CreateTips
- LotteryPaintingShowWindow.GetItemArr
- LotteryPaintingShowWindow.Next
- LotteryPaintingShowWindow.InitBtn
- LotteryPaintingShowWindow.TouchSkip
- LotteryPaintingShowWindow.HandleMessage
- LotteryPaintingShowWindow.OnClose
**Requires:**
- LotteryCardShow_PaintingShowWindowByName
**Snippet:**
```lua
require("LotteryCardShow_PaintingShowWindowByName")
local LotteryPaintingShowWindow = {}
local uis, contentPane, rewardData, index, tipsArr, curNum, curTypingEffect, curSoundEventIns, closeCallback, notShowResultWindow, notShowChangeItem
local closeTouchable = false

function LotteryPaintingShowWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.LotteryPaintingShowWindow.package, WinResConfig.LotteryPaintingShowWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetLotteryCardShow_PaintingShowWindowUis(contentPane)
```

---

## GL/LotteryProbabilityWindow.lua.lua
**Functions:**
- LotteryProbabilityWindow.OnInit
- LotteryProbabilityWindow.InitList
- list.itemRenderer
- LotteryProbabilityWindow.SetBUPTitle
- LotteryProbabilityWindow.SetBTitle
- LotteryProbabilityWindow.SetTitle
- LotteryProbabilityWindow.SetCardBList
- list.itemRenderer
- LotteryProbabilityWindow.SetCardList
- list.itemRenderer
- LotteryProbabilityWindow.InitBtn
- LotteryProbabilityWindow.HandleMessage
- LotteryProbabilityWindow.OnClose
**Requires:**
- Lottery_ProbabilityWindowByName
**Snippet:**
```lua
require("Lottery_ProbabilityWindowByName")
local LotteryProbabilityWindow = {}
local uis, contentPane, gachaId, jumpTb

function LotteryProbabilityWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.LotteryProbabilityWindow.package, WinResConfig.LotteryProbabilityWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetLottery_ProbabilityWindowUis(contentPane)
    gachaId = bridgeObj.argTable[1]
```

---

## GL/LotteryRecordWindow.lua.lua
**Functions:**
- LotteryRecordWindow.OnInit
- LotteryRecordWindow.InitList
- uis.Main.RecordList.itemRenderer
- LotteryRecordWindow.SetReward
- list.itemRenderer
- LotteryRecordWindow.InitBtn
- LotteryRecordWindow.HandleMessage
- LotteryRecordWindow.OnClose
**Requires:**
- Lottery_RecordWindowByName
**Snippet:**
```lua
require("Lottery_RecordWindowByName")
local LotteryRecordWindow = {}
local uis, contentPane, recordData, jumpTb

function LotteryRecordWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.LotteryRecordWindow.package, WinResConfig.LotteryRecordWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetLottery_RecordWindowUis(contentPane)
    recordData = bridgeObj.argTable[1]
```

---

## GL/LotteryResultWindow.lua.lua
**Functions:**
- LotteryResultWindow.OnInit
- LotteryResultWindow.InitBg
- LotteryResultWindow.Sort
- LotteryResultWindow.InitList
- starList.itemRenderer
- LotteryResultWindow.OnShowAnimationEnd
- LotteryResultWindow.InitBtn
- LotteryResultWindow.HandleMessage
- LotteryResultWindow.OnClose
**Requires:**
- Lottery_ResultWindowByName
**Snippet:**
```lua
require("Lottery_ResultWindowByName")
local LotteryResultWindow = {}
local uis, contentPane, rewardData
local effectBgList = {
  "Assets/Art/Effects/Prefab/UI_prefab/Gachaendshow/gahcaendlevel/FX_ui_gacha_end_level_green.prefab",
  "Assets/Art/Effects/Prefab/UI_prefab/Gachaendshow/gahcaendlevel/FX_ui_gacha_end_level_blue.prefab",
  "Assets/Art/Effects/Prefab/UI_prefab/Gachaendshow/gahcaendlevel/FX_ui_gacha_end_level_purple.prefab",
  "Assets/Art/Effects/Prefab/UI_prefab/Gachaendshow/gahcaendlevel/FX_ui_gacha_end_level_yellow.prefab",
  "Assets/Art/Effects/Prefab/UI_prefab/Gachaendshow/gahcaendlevel/FX_ui_gacha_end_level_orange.prefab"
}
```

---

## GL/LotteryScriptList.lua.lua
**Requires:**
- LotteryData
- LotteryService
- LotteryMgr
- LotteryEffect
**Snippet:**
```lua
local require = require
require("LotteryData")
require("LotteryService")
require("LotteryMgr")
require("LotteryEffect")
```

---

## GL/LotteryService.lua.lua
**Functions:**
- LotteryService.Init
- LotteryService.GetGachaInfoReq
- LotteryService.GetGachaInfoRsp
- LotteryService.DoGachaReq
- LotteryService.DoGachaRsp
- LotteryService.ExchangeGachaReq
- LotteryService.ExchangeGachaRsp
- LotteryService.GetGachaRecordsReq
- LotteryService.GetGachaRecordsRsp
- LotteryService.GetGachaExtraReq
- LotteryService.GetGachaExtraRsp
**Snippet:**
```lua
LotteryService = {}
local isJump

function LotteryService.Init()
  Net.AddListener(Proto.MsgName.GetGachaInfoRsp, LotteryService.GetGachaInfoRsp)
  Net.AddListener(Proto.MsgName.DoGachaRsp, LotteryService.DoGachaRsp)
  Net.AddListener(Proto.MsgName.ExchangeGachaRsp, LotteryService.ExchangeGachaRsp)
  Net.AddListener(Proto.MsgName.GetGachaRecordsRsp, LotteryService.GetGachaRecordsRsp)
  Net.AddListener(Proto.MsgName.GetGachaExtraRsp, LotteryService.GetGachaExtraRsp)
end
```

---

## GL/LotteryStartChoiceWindow.lua.lua
**Functions:**
- LotteryStartChoiceWindow.ReInitData
- LotteryStartChoiceWindow.OnInit
- LotteryStartChoiceWindow.UpdateInfo
- LotteryStartChoiceWindow.UpdateBtnPos
- LotteryStartChoiceWindow.CreateBtn
- LotteryStartChoiceWindow.CloseWindow
- LotteryStartChoiceWindow.InitBtn
- LotteryStartChoiceWindow.OnShown
- LotteryStartChoiceWindow.OnClose
**Requires:**
- Lottery_StartChoiceWindowByName
**Snippet:**
```lua
require("Lottery_StartChoiceWindowByName")
local LotteryStartChoiceWindow = {}
local uis, contentPane, data, curIndex, tween
local cardTran = {}
local cardBtn = {}
local deatailsButton = {}
local deatailsTran = {}
local w, h = 288, 448
local dw = 48

```

---

## GL/LotteryTokenExplainWindow.lua.lua
**Functions:**
- LotteryTokenExplainWindow.ReInitData
- LotteryTokenExplainWindow.OnInit
- LotteryTokenExplainWindow.UpdateInfo
- LotteryTokenExplainWindow.InitBtn
- LotteryTokenExplainWindow.OnClose
**Requires:**
- ShopTips_TokenExplainWindowByName
**Snippet:**
```lua
require("ShopTips_TokenExplainWindowByName")
local LotteryTokenExplainWindow = {}
local uis, contentPane

function LotteryTokenExplainWindow.ReInitData()
end

function LotteryTokenExplainWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.LotteryTokenExplainWindow.package, WinResConfig.LotteryTokenExplainWindow.comName, function(com)
    contentPane = com
```

---

## GL/LotteryWindow.lua.lua
**Functions:**
- LotteryWindow.OnInit
- LotteryWindow.Init
- LotteryWindow.RefreshWordTxt
- LotteryWindow.SetPage
- LotteryWindow.SetGachaBtn
- waitFun
- waitFun
- waitFun
- LotteryWindow.CheckTime
- LotteryWindow.OnShown
- LotteryWindow.IsGachaByCount
- LotteryWindow.GetCost
- LotteryWindow.CreatedCardInfo
- LotteryWindow.GetInfoItem
- LotteryWindow.GetTipsData
- LotteryWindow.InitBannerList
- uis.Main.CardShowRegion.BannerList.itemRenderer
- LotteryWindow.SortGacha
- LotteryWindow.IsRestrict
- LotteryWindow.InitBtn
- uis.Main.CardShowRegion.FunctionList.itemRenderer
- LotteryWindow.FunctionListClick
- LotteryWindow.HandleMessage
- LotteryWindow.IsChangePage
- LotteryWindow.OnClose
**Requires:**
- Lottery_LotteryWindowByName
**Snippet:**
```lua
require("Lottery_LotteryWindowByName")
local LotteryWindow = {}
local uis, contentPane, skipCom, curId, openLotteryId, jumpTb, curPoolId, waitFun, curTitleData, showStartChoice

function LotteryWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.LotteryWindow.package, WinResConfig.LotteryWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetLottery_LotteryWindowUis(contentPane)
    openLotteryId = bridgeObj.argTable[1]
```

---

## GL/Lottery_10TimesBtnByName.lua.lua
**Functions:**
- GetLottery_10TimesBtnUis
**Snippet:**
```lua
function GetLottery_10TimesBtnUis(ui)
  local uis = {}
  
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## GL/Lottery_1TimeBtnByName.lua.lua
**Functions:**
- GetLottery_1TimeBtnUis
**Snippet:**
```lua
function GetLottery_1TimeBtnUis(ui)
  local uis = {}
  
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## GL/Lottery_AssetsTipsGroupByName.lua.lua
**Functions:**
- GetLottery_AssetsTipsGroupUis
**Snippet:**
```lua
function GetLottery_AssetsTipsGroupUis(ui)
  local uis = {}
  
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_BannerBtnBgByName.lua.lua
**Functions:**
- GetLottery_BannerBtnBgUis
**Snippet:**
```lua
function GetLottery_BannerBtnBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_BannerBtnByName.lua.lua
**Functions:**
- GetLottery_BannerBtnUis
**Requires:**
- Lottery_BannerBtnBgByName
- CommonResource_RedDotByName
- CommonResource_LotteryFreeByName
**Snippet:**
```lua
require("Lottery_BannerBtnBgByName")
require("CommonResource_RedDotByName")
require("CommonResource_LotteryFreeByName")

function GetLottery_BannerBtnUis(ui)
  local uis = {}
  uis.BannerLoader = ui:GetChild("BannerLoader")
  uis.BannerBtnBg = GetLottery_BannerBtnBgUis(ui:GetChild("BannerBtnBg"))
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.LotteryFree = GetCommonResource_LotteryFreeUis(ui:GetChild("LotteryFree"))
```

---

## GL/Lottery_CardShowByName.lua.lua
**Functions:**
- GetLottery_CardShowUis
**Requires:**
- Lottery_CardTipsContainerByName
**Snippet:**
```lua
require("Lottery_CardTipsContainerByName")

function GetLottery_CardShowUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.PicHolder = ui:GetChild("PicHolder")
  uis.CardTipsContainer = GetLottery_CardTipsContainerUis(ui:GetChild("CardTipsContainer"))
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_CardShowComByName.lua.lua
**Functions:**
- GetLottery_CardShowComUis
**Snippet:**
```lua
function GetLottery_CardShowComUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_CardShowRegionByName.lua.lua
**Functions:**
- GetLottery_CardShowRegionUis
**Requires:**
- Lottery_AssetsTipsGroupByName
- Lottery_GaChaRegionByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("Lottery_AssetsTipsGroupByName")
require("Lottery_GaChaRegionByName")
require("CommonResource_CurrencyReturnByName")

function GetLottery_CardShowRegionUis(ui)
  local uis = {}
  uis.CardShowList = ui:GetChild("CardShowList")
  uis.AssetsTipsGroup = GetLottery_AssetsTipsGroupUis(ui:GetChild("AssetsTipsGroup"))
  uis.GaChaRegion = GetLottery_GaChaRegionUis(ui:GetChild("GaChaRegion"))
  uis.FunctionList = ui:GetChild("FunctionList")
```

---

## GL/Lottery_CardTipsContainerByName.lua.lua
**Functions:**
- GetLottery_CardTipsContainerUis
**Snippet:**
```lua
function GetLottery_CardTipsContainerUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_ChoiceCardByName.lua.lua
**Functions:**
- GetLottery_ChoiceCardUis
**Requires:**
- Lottery_ChoiceNumberAniByName
**Snippet:**
```lua
require("Lottery_ChoiceNumberAniByName")

function GetLottery_ChoiceCardUis(ui)
  local uis = {}
  uis.ChoiceNumberAni = GetLottery_ChoiceNumberAniUis(ui:GetChild("ChoiceNumberAni"))
  uis.SkipBtn = ui:GetChild("SkipBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_ChoiceNumberAniByName.lua.lua
**Functions:**
- GetLottery_ChoiceNumberAniUis
**Requires:**
- Lottery_ChoiceNumberByName
**Snippet:**
```lua
require("Lottery_ChoiceNumberByName")

function GetLottery_ChoiceNumberAniUis(ui)
  local uis = {}
  uis.ChoiceNumber = GetLottery_ChoiceNumberUis(ui:GetChild("ChoiceNumber"))
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_ChoiceNumberByName.lua.lua
**Functions:**
- GetLottery_ChoiceNumberUis
**Snippet:**
```lua
function GetLottery_ChoiceNumberUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_Complement1ByName.lua.lua
**Functions:**
- GetLottery_Complement1Uis
**Requires:**
- Lottery_ComplementItemRegionByName
**Snippet:**
```lua
require("Lottery_ComplementItemRegionByName")

function GetLottery_Complement1Uis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemRegion = GetLottery_ComplementItemRegionUis(ui:GetChild("ItemRegion"))
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_Complement2ByName.lua.lua
**Functions:**
- GetLottery_Complement2Uis
**Requires:**
- CommonResource_PopupBgByName
- CommonResource_Popup_BByName
- Lottery_Complement1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("CommonResource_Popup_BByName")
require("Lottery_Complement1ByName")

function GetLottery_Complement2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Popup_B = GetCommonResource_Popup_BUis(ui:GetChild("Popup_B"))
  uis.Currency1 = GetLottery_Complement1Uis(ui:GetChild("Currency1"))
```

---

## GL/Lottery_ComplementItemByName.lua.lua
**Functions:**
- GetLottery_ComplementItemUis
**Snippet:**
```lua
function GetLottery_ComplementItemUis(ui)
  local uis = {}
  
  uis.SpendTxt = ui:GetChild("SpendTxt")
  uis.IconLoader = ui:GetChild("IconLoader")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_ComplementItemRegionByName.lua.lua
**Functions:**
- GetLottery_ComplementItemRegionUis
**Requires:**
- Lottery_ComplementItemByName
**Snippet:**
```lua
require("Lottery_ComplementItemByName")

function GetLottery_ComplementItemRegionUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Item1 = GetLottery_ComplementItemUis(ui:GetChild("Item1"))
  uis.Item2 = GetLottery_ComplementItemUis(ui:GetChild("Item2"))
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_ComplementWindowByName.lua.lua
**Functions:**
- GetLottery_ComplementWindowUis
**Requires:**
- Lottery_Complement2ByName
**Snippet:**
```lua
require("Lottery_Complement2ByName")

function GetLottery_ComplementWindowUis(ui)
  local uis = {}
  uis.Main = GetLottery_Complement2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_EveryDayBtnByName.lua.lua
**Functions:**
- GetLottery_EveryDayBtnUis
**Snippet:**
```lua
function GetLottery_EveryDayBtnUis(ui)
  local uis = {}
  
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.Word3Txt = ui:GetChild("Word3Txt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
```

---

## GL/Lottery_ExchangeByName.lua.lua
**Functions:**
- GetLottery_ExchangeUis
**Requires:**
- Lottery_PopupBgByName
- Lottery_E_TitleByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("Lottery_PopupBgByName")
require("Lottery_E_TitleByName")
require("CommonResource_CurrencyReturnByName")

function GetLottery_ExchangeUis(ui)
  local uis = {}
  uis.PopupBg = GetLottery_PopupBgUis(ui:GetChild("PopupBg"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.ExchangeList = ui:GetChild("ExchangeList")
  uis.E_Title = GetLottery_E_TitleUis(ui:GetChild("E_Title"))
```

---

## GL/Lottery_ExchangeQualityByName.lua.lua
**Functions:**
- GetLottery_ExchangeQualityUis
**Snippet:**
```lua
function GetLottery_ExchangeQualityUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_ExchangeTipsByName.lua.lua
**Functions:**
- GetLottery_ExchangeTipsUis
**Requires:**
- Lottery_ExchangeTipsPicByName
- Lottery_ExchangeQualityByName
- Lottery_NewByName
- CommonResource_OccupationByName
**Snippet:**
```lua
require("Lottery_ExchangeTipsPicByName")
require("Lottery_ExchangeQualityByName")
require("Lottery_NewByName")
require("CommonResource_OccupationByName")

function GetLottery_ExchangeTipsUis(ui)
  local uis = {}
  uis.ResultTipsPic = GetLottery_ExchangeTipsPicUis(ui:GetChild("ResultTipsPic"))
  uis.Quality = GetLottery_ExchangeQualityUis(ui:GetChild("Quality"))
  uis.CardNameTxt = ui:GetChild("CardNameTxt")
```

---

## GL/Lottery_ExchangeTipsPicByName.lua.lua
**Functions:**
- GetLottery_ExchangeTipsPicUis
**Snippet:**
```lua
function GetLottery_ExchangeTipsPicUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_ExchangeWindowByName.lua.lua
**Functions:**
- GetLottery_ExchangeWindowUis
**Requires:**
- Lottery_ExchangeByName
**Snippet:**
```lua
require("Lottery_ExchangeByName")

function GetLottery_ExchangeWindowUis(ui)
  local uis = {}
  uis.Main = GetLottery_ExchangeUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_E_TipsByName.lua.lua
**Functions:**
- GetLottery_E_TipsUis
**Requires:**
- Lottery_ExchangeTipsByName
**Snippet:**
```lua
require("Lottery_ExchangeTipsByName")

function GetLottery_E_TipsUis(ui)
  local uis = {}
  uis.ResultTips = GetLottery_ExchangeTipsUis(ui:GetChild("ResultTips"))
  uis.TpBtn = ui:GetChild("TpBtn")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_E_TitleByName.lua.lua
**Functions:**
- GetLottery_E_TitleUis
**Snippet:**
```lua
function GetLottery_E_TitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_FunctionBtnByName.lua.lua
**Functions:**
- GetLottery_FunctionBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetLottery_FunctionBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_GaChaCountByName.lua.lua
**Functions:**
- GetLottery_GaChaCountUis
**Snippet:**
```lua
function GetLottery_GaChaCountUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_GaChaRegionByName.lua.lua
**Functions:**
- GetLottery_GaChaRegionUis
**Requires:**
- Lottery_Word1TipsByName
- Lottery_GaChaCountByName
- Lottery_Word2TipsByName
- CommonResource_LotteryFreeTimeByName
**Snippet:**
```lua
require("Lottery_Word1TipsByName")
require("Lottery_GaChaCountByName")
require("Lottery_Word2TipsByName")
require("CommonResource_LotteryFreeTimeByName")

function GetLottery_GaChaRegionUis(ui)
  local uis = {}
  uis.Word1Tips = GetLottery_Word1TipsUis(ui:GetChild("Word1Tips"))
  uis.GaChaCount = GetLottery_GaChaCountUis(ui:GetChild("GaChaCount"))
  uis.EveryDayBtn = ui:GetChild("EveryDayBtn")
```

---

## GL/Lottery_LotteryByName.lua.lua
**Functions:**
- GetLottery_LotteryUis
**Requires:**
- CommonResource_BackGroundByName
- Lottery_CardShowRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Lottery_CardShowRegionByName")

function GetLottery_LotteryUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.CardShowRegion = GetLottery_CardShowRegionUis(ui:GetChild("CardShowRegion"))
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_LotteryWindowByName.lua.lua
**Functions:**
- GetLottery_LotteryWindowUis
**Requires:**
- Lottery_LotteryByName
**Snippet:**
```lua
require("Lottery_LotteryByName")

function GetLottery_LotteryWindowUis(ui)
  local uis = {}
  uis.Main = GetLottery_LotteryUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_NewByName.lua.lua
**Functions:**
- GetLottery_NewUis
**Snippet:**
```lua
function GetLottery_NewUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_NoviceGaChaBtnByName.lua.lua
**Functions:**
- GetLottery_NoviceGaChaBtnUis
**Snippet:**
```lua
function GetLottery_NoviceGaChaBtnUis(ui)
  local uis = {}
  
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.Word3Txt = ui:GetChild("Word3Txt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
```

---

## GL/Lottery_NoviceGaChaChoiceBtnByName.lua.lua
**Functions:**
- GetLottery_NoviceGaChaChoiceBtnUis
**Snippet:**
```lua
function GetLottery_NoviceGaChaChoiceBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_PopupBgByName.lua.lua
**Functions:**
- GetLottery_PopupBgUis
**Snippet:**
```lua
function GetLottery_PopupBgUis(ui)
  local uis = {}
  
  uis.BlurLoader = ui:GetChild("BlurLoader")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_ProbabilityByName.lua.lua
**Functions:**
- GetLottery_ProbabilityUis
**Requires:**
- Lottery_PopupBgByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("Lottery_PopupBgByName")
require("CommonResource_CurrencyReturnByName")

function GetLottery_ProbabilityUis(ui)
  local uis = {}
  uis.PopupBg = GetLottery_PopupBgUis(ui:GetChild("PopupBg"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.ProbabilityList = ui:GetChild("ProbabilityList")
  uis.ProbabilityLookBtn = ui:GetChild("ProbabilityLookBtn")
  uis.CurrencyReturn = GetCommonResource_CurrencyReturnUis(ui:GetChild("CurrencyReturn"))
```

---

## GL/Lottery_ProbabilityLookBtnByName.lua.lua
**Functions:**
- GetLottery_ProbabilityLookBtnUis
**Snippet:**
```lua
function GetLottery_ProbabilityLookBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_ProbabilityWindowByName.lua.lua
**Functions:**
- GetLottery_ProbabilityWindowUis
**Requires:**
- Lottery_ProbabilityByName
**Snippet:**
```lua
require("Lottery_ProbabilityByName")

function GetLottery_ProbabilityWindowUis(ui)
  local uis = {}
  uis.Main = GetLottery_ProbabilityUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_P_AByName.lua.lua
**Functions:**
- GetLottery_P_AUis
**Requires:**
- Lottery_P_TitleByName
**Snippet:**
```lua
require("Lottery_P_TitleByName")

function GetLottery_P_AUis(ui)
  local uis = {}
  uis.P_Title = GetLottery_P_TitleUis(ui:GetChild("P_Title"))
  uis.InfoList = ui:GetChild("InfoList")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_P_BByName.lua.lua
**Functions:**
- GetLottery_P_BUis
**Requires:**
- Lottery_P_TitleByName
**Snippet:**
```lua
require("Lottery_P_TitleByName")

function GetLottery_P_BUis(ui)
  local uis = {}
  uis.P_Title = GetLottery_P_TitleUis(ui:GetChild("P_Title"))
  uis.HeadList = ui:GetChild("HeadList")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_P_B_CardHeadBgByName.lua.lua
**Functions:**
- GetLottery_P_B_CardHeadBgUis
**Snippet:**
```lua
function GetLottery_P_B_CardHeadBgUis(ui)
  local uis = {}
  
  uis.CardPicLoader = ui:GetChild("CardPicLoader")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_P_B_CardHeadBtnByName.lua.lua
**Functions:**
- GetLottery_P_B_CardHeadBtnUis
**Requires:**
- Lottery_P_B_CardHeadBgByName
- CommonResource_OccupationByName
**Snippet:**
```lua
require("Lottery_P_B_CardHeadBgByName")
require("CommonResource_OccupationByName")

function GetLottery_P_B_CardHeadBtnUis(ui)
  local uis = {}
  uis.CardPic = GetLottery_P_B_CardHeadBgUis(ui:GetChild("CardPic"))
  uis.Occupation = GetCommonResource_OccupationUis(ui:GetChild("Occupation"))
  uis.ElementList = ui:GetChild("ElementList")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## GL/Lottery_P_CardInfo1ByName.lua.lua
**Functions:**
- GetLottery_P_CardInfo1Uis
**Requires:**
- Lottery_Quality1_1ByName
- Lottery_P_CardInfoPicByName
- Lottery_Quality1_2ByName
- CommonResource_OccupationByName
**Snippet:**
```lua
require("Lottery_Quality1_1ByName")
require("Lottery_P_CardInfoPicByName")
require("Lottery_Quality1_2ByName")
require("CommonResource_OccupationByName")

function GetLottery_P_CardInfo1Uis(ui)
  local uis = {}
  uis.Quality1_1 = GetLottery_Quality1_1Uis(ui:GetChild("Quality1_1"))
  uis.CardPic = GetLottery_P_CardInfoPicUis(ui:GetChild("CardPic"))
  uis.Quality1_2 = GetLottery_Quality1_2Uis(ui:GetChild("Quality1_2"))
```

---

## GL/Lottery_P_CardInfo2ByName.lua.lua
**Functions:**
- GetLottery_P_CardInfo2Uis
**Requires:**
- Lottery_P_CardInfo1ByName
**Snippet:**
```lua
require("Lottery_P_CardInfo1ByName")

function GetLottery_P_CardInfo2Uis(ui)
  local uis = {}
  uis.P_CardInfo1 = GetLottery_P_CardInfo1Uis(ui:GetChild("P_CardInfo1"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_P_CardInfoPicByName.lua.lua
**Functions:**
- GetLottery_P_CardInfoPicUis
**Snippet:**
```lua
function GetLottery_P_CardInfoPicUis(ui)
  local uis = {}
  
  uis.CardPicLoader = ui:GetChild("CardPicLoader")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_P_TitleByName.lua.lua
**Functions:**
- GetLottery_P_TitleUis
**Snippet:**
```lua
function GetLottery_P_TitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_P_Word1ByName.lua.lua
**Functions:**
- GetLottery_P_Word1Uis
**Snippet:**
```lua
function GetLottery_P_Word1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_P_WordByName.lua.lua
**Functions:**
- GetLottery_P_WordUis
**Snippet:**
```lua
function GetLottery_P_WordUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_Quality1_1ByName.lua.lua
**Functions:**
- GetLottery_Quality1_1Uis
**Snippet:**
```lua
function GetLottery_Quality1_1Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_Quality1_2ByName.lua.lua
**Functions:**
- GetLottery_Quality1_2Uis
**Snippet:**
```lua
function GetLottery_Quality1_2Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_RecordByName.lua.lua
**Functions:**
- GetLottery_RecordUis
**Requires:**
- Lottery_PopupBgByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("Lottery_PopupBgByName")
require("CommonResource_CurrencyReturnByName")

function GetLottery_RecordUis(ui)
  local uis = {}
  uis.PopupBg = GetLottery_PopupBgUis(ui:GetChild("PopupBg"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.RecordList = ui:GetChild("RecordList")
  uis.CurrencyReturn = GetCommonResource_CurrencyReturnUis(ui:GetChild("CurrencyReturn"))
  uis.root = ui
```

---

## GL/Lottery_RecordWindowByName.lua.lua
**Functions:**
- GetLottery_RecordWindowUis
**Requires:**
- Lottery_RecordByName
**Snippet:**
```lua
require("Lottery_RecordByName")

function GetLottery_RecordWindowUis(ui)
  local uis = {}
  uis.Main = GetLottery_RecordUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_ResultByName.lua.lua
**Functions:**
- GetLottery_ResultUis
**Requires:**
- CommonResource_BackGroundByName
- Lottery_CardShowComByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Lottery_CardShowComByName")

function GetLottery_ResultUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.TipsList = ui:GetChild("TipsList")
  uis.CardShowCom = GetLottery_CardShowComUis(ui:GetChild("CardShowCom"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
```

---

## GL/Lottery_ResultEffectByName.lua.lua
**Functions:**
- GetLottery_ResultEffectUis
**Snippet:**
```lua
function GetLottery_ResultEffectUis(ui)
  local uis = {}
  
  uis.EffectLoader = ui:GetChild("EffectLoader")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_ResultOccupationByName.lua.lua
**Functions:**
- GetLottery_ResultOccupationUis
**Snippet:**
```lua
function GetLottery_ResultOccupationUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_ResultStarByName.lua.lua
**Functions:**
- GetLottery_ResultStarUis
**Snippet:**
```lua
function GetLottery_ResultStarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_ResultTipsAniByName.lua.lua
**Functions:**
- GetLottery_ResultTipsAniUis
**Requires:**
- Lottery_ResultTipsEmpty0ByName
**Snippet:**
```lua
require("Lottery_ResultTipsEmpty0ByName")

function GetLottery_ResultTipsAniUis(ui)
  local uis = {}
  uis.ResultTipsEmpty0 = GetLottery_ResultTipsEmpty0Uis(ui:GetChild("ResultTipsEmpty0"))
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_ResultTipsByName.lua.lua
**Functions:**
- GetLottery_ResultTipsUis
**Requires:**
- Lottery_ResultEffectByName
- Lottery_ResultOccupationByName
- Lottery_ResultTipsPicByName
- Lottery_NewByName
**Snippet:**
```lua
require("Lottery_ResultEffectByName")
require("Lottery_ResultOccupationByName")
require("Lottery_ResultTipsPicByName")
require("Lottery_NewByName")

function GetLottery_ResultTipsUis(ui)
  local uis = {}
  uis.Effect1 = GetLottery_ResultEffectUis(ui:GetChild("Effect1"))
  uis.Pic1Image = ui:GetChild("Pic1Image")
  uis.Occupation = GetLottery_ResultOccupationUis(ui:GetChild("Occupation"))
```

---

## GL/Lottery_ResultTipsEmpty0ByName.lua.lua
**Functions:**
- GetLottery_ResultTipsEmpty0Uis
**Requires:**
- Lottery_ResultTipsEmpty1ByName
**Snippet:**
```lua
require("Lottery_ResultTipsEmpty1ByName")

function GetLottery_ResultTipsEmpty0Uis(ui)
  local uis = {}
  uis.ResultTipsEmpty1 = GetLottery_ResultTipsEmpty1Uis(ui:GetChild("ResultTipsEmpty1"))
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_ResultTipsEmpty1ByName.lua.lua
**Functions:**
- GetLottery_ResultTipsEmpty1Uis
**Requires:**
- Lottery_ResultTipsEmpty2ByName
**Snippet:**
```lua
require("Lottery_ResultTipsEmpty2ByName")

function GetLottery_ResultTipsEmpty1Uis(ui)
  local uis = {}
  uis.ResultTipsEmpty2 = GetLottery_ResultTipsEmpty2Uis(ui:GetChild("ResultTipsEmpty2"))
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_ResultTipsEmpty2ByName.lua.lua
**Functions:**
- GetLottery_ResultTipsEmpty2Uis
**Requires:**
- Lottery_ResultTipsByName
**Snippet:**
```lua
require("Lottery_ResultTipsByName")

function GetLottery_ResultTipsEmpty2Uis(ui)
  local uis = {}
  uis.ResultTips = GetLottery_ResultTipsUis(ui:GetChild("ResultTips"))
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_ResultTipsPicByName.lua.lua
**Functions:**
- GetLottery_ResultTipsPicUis
**Snippet:**
```lua
function GetLottery_ResultTipsPicUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_ResultWindowByName.lua.lua
**Functions:**
- GetLottery_ResultWindowUis
**Requires:**
- Lottery_ResultByName
**Snippet:**
```lua
require("Lottery_ResultByName")

function GetLottery_ResultWindowUis(ui)
  local uis = {}
  uis.Main = GetLottery_ResultUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_R_AByName.lua.lua
**Functions:**
- GetLottery_R_AUis
**Requires:**
- Lottery_R_TitleByName
**Snippet:**
```lua
require("Lottery_R_TitleByName")

function GetLottery_R_AUis(ui)
  local uis = {}
  uis.R_Title = GetLottery_R_TitleUis(ui:GetChild("R_Title"))
  uis.HeadList = ui:GetChild("HeadList")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_R_TipsByName.lua.lua
**Functions:**
- GetLottery_R_TipsUis
**Requires:**
- Lottery_P_CardInfo1ByName
**Snippet:**
```lua
require("Lottery_P_CardInfo1ByName")

function GetLottery_R_TipsUis(ui)
  local uis = {}
  uis.P_CardInfo1 = GetLottery_P_CardInfo1Uis(ui:GetChild("P_CardInfo1"))
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_R_TitleByName.lua.lua
**Functions:**
- GetLottery_R_TitleUis
**Snippet:**
```lua
function GetLottery_R_TitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_SkipBtnByName.lua.lua
**Functions:**
- GetLottery_SkipBtnUis
**Snippet:**
```lua
function GetLottery_SkipBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_StartChoiceByName.lua.lua
**Functions:**
- GetLottery_StartChoiceUis
**Requires:**
- Lottery_PopupBgByName
- Lottery_StartChoice_WordByName
- Lottery_StartChoice_LockWordByName
**Snippet:**
```lua
require("Lottery_PopupBgByName")
require("Lottery_StartChoice_WordByName")
require("Lottery_StartChoice_LockWordByName")

function GetLottery_StartChoiceUis(ui)
  local uis = {}
  uis.PopupBg = GetLottery_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.Word = GetLottery_StartChoice_WordUis(ui:GetChild("Word"))
```

---

## GL/Lottery_StartChoiceWindowByName.lua.lua
**Functions:**
- GetLottery_StartChoiceWindowUis
**Requires:**
- Lottery_StartChoiceByName
**Snippet:**
```lua
require("Lottery_StartChoiceByName")

function GetLottery_StartChoiceWindowUis(ui)
  local uis = {}
  uis.Main = GetLottery_StartChoiceUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_StartChoice_LockWordByName.lua.lua
**Functions:**
- GetLottery_StartChoice_LockWordUis
**Snippet:**
```lua
function GetLottery_StartChoice_LockWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_StartChoice_SureBtnByName.lua.lua
**Functions:**
- GetLottery_StartChoice_SureBtnUis
**Snippet:**
```lua
function GetLottery_StartChoice_SureBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_StartChoice_WordByName.lua.lua
**Functions:**
- GetLottery_StartChoice_WordUis
**Snippet:**
```lua
function GetLottery_StartChoice_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_TpBtnByName.lua.lua
**Functions:**
- GetLottery_TpBtnUis
**Snippet:**
```lua
function GetLottery_TpBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_Word1TipsByName.lua.lua
**Functions:**
- GetLottery_Word1TipsUis
**Snippet:**
```lua
function GetLottery_Word1TipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/Lottery_Word2TipsByName.lua.lua
**Functions:**
- GetLottery_Word2TipsUis
**Snippet:**
```lua
function GetLottery_Word2TipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## GL/luaTest.lua.lua
**Requires:**
- Lplus
- TrieTree
- Utility
- SensitiveWords
- profiler
- ACTrie
**Snippet:**
```lua
require("Lplus")
require("TrieTree")
require("Utility")
_G.block_word_list = {}
require("SensitiveWords")
local len = #SensitiveWords
print(string.format("屏蔽词库共有%d词条", len))
local testStr = "我爱胡锦涛"
print("被检查词条长度", #GetDivideStringList(testStr))
local profiler = require("profiler")
```

---

## GL/LuaWinRegister.lua.lua
**Snippet:**
```lua
UIMgr = CS.UIManager.Singleton
WinResConfig = {
  BattleUIWindow = {
    name = "BattleUIWindow",
    package = "Battle",
    comName = "BattleUIWindow",
    belowWindowOpr = "close",
    notReopen = true
  },
  LoginWindow = {
```

---
