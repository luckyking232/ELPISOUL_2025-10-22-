# BCD

## BCD/BiographyData.lua.lua
**Functions:**
- BiographyData.GetRefreshStamp
- BiographyData.RefreshRefreshStamp
- BiographyData.GetInfoByPlantId
- BiographyData.GetIndexByPlantId
- BiographyData.GetHomeShowTask
- CarnivalData.BiographyShowHome
**Snippet:**
```lua
BiographyData = {
  plantInfo = {}
}
local refreshStamp = 0

function BiographyData.GetRefreshStamp()
  return refreshStamp
end

function BiographyData.RefreshRefreshStamp(time)
```

---

## BCD/BiographyScriptList.lua.lua
**Requires:**
- BiographyData
- BiographyService
**Snippet:**
```lua
local require = require
require("BiographyData")
require("BiographyService")
```

---

## BCD/BiographyService.lua.lua
**Functions:**
- BiographyService.Init
- BiographyService.GetPlantInfoReq
- BiographyService.GetPlantInfoRsp
- BiographyService.RewardFlowerReq
- BiographyService.RewardFlowerRsp
- BiographyService.RewardPlantTaskReq
- BiographyService.RewardPlantTaskRsp
**Snippet:**
```lua
BiographyService = {}

function BiographyService.Init()
  Net.AddListener(Proto.MsgName.GetPlantInfoRsp, BiographyService.GetPlantInfoRsp)
  Net.AddListener(Proto.MsgName.RewardFlowerRsp, BiographyService.RewardFlowerRsp)
  Net.AddListener(Proto.MsgName.RewardPlantTaskRsp, BiographyService.RewardPlantTaskRsp)
end

function BiographyService.GetPlantInfoReq(rspCallback)
  local msg = {}
```

---

## BCD/BiographyWindow.lua.lua
**Functions:**
- BiographyWindow.OnInit
- BiographyWindow.InitData
- BiographyWindow.LoadSpine
- BiographyWindow.PlayFlowerAnim
- BiographyWindow.UpdateFlower
- BiographyWindow.GetFlowerBtn
- BiographyWindow.Init
- BiographyWindow.InitTaskInfo
- BiographyWindow.ShowPlantList
- BiographyWindow.ShowPageBtn
- BiographyWindow.RefreshTask
- BiographyWindow.InitBtn
- BiographyWindow.PlayFlowerByIndex
- BiographyWindow.HandleMessage
- BiographyWindow.OnHide
- BiographyWindow.OnShow
- BiographyWindow.OnClose
**Requires:**
- Biography_BiographyByName
**Snippet:**
```lua
require("Biography_BiographyByName")
BiographyWindow = {}
local uis, contentPane, curData
local animName = {
  "idle01",
  "idle01",
  "idle02"
}
local cirrusPrefab, maxLv, curFlowerIndex, flowerCom, curBtnPage, awardEffect, isChange
local posOff = {
```

---

## BCD/Biography_BiographyByName.lua.lua
**Functions:**
- GetBiography_BiographyUis
**Requires:**
- CommonResource_BackGroundByName
- Biography_FullScreenByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Biography_FullScreenByName")

function GetBiography_BiographyUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.FullScreen = GetBiography_FullScreenUis(ui:GetChild("FullScreen"))
  uis.TaskBtn = ui:GetChild("TaskBtn")
  uis.LeftBtn = ui:GetChild("LeftBtn")
  uis.RightBtn = ui:GetChild("RightBtn")
```

---

## BCD/Biography_BiographyWindowByName.lua.lua
**Functions:**
- GetBiography_BiographyWindowUis
**Requires:**
- Biography_BiographyByName
**Snippet:**
```lua
require("Biography_BiographyByName")

function GetBiography_BiographyWindowUis(ui)
  local uis = {}
  uis.Main = GetBiography_BiographyUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/Biography_CompleteTipsByName.lua.lua
**Functions:**
- GetBiography_CompleteTipsUis
**Snippet:**
```lua
function GetBiography_CompleteTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/Biography_FullScreenByName.lua.lua
**Functions:**
- GetBiography_FullScreenUis
**Snippet:**
```lua
function GetBiography_FullScreenUis(ui)
  local uis = {}
  
  uis.SpineLoader = ui:GetChild("SpineLoader")
  uis.SpineHolder = ui:GetChild("SpineHolder")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## BCD/Biography_GoToBtnByName.lua.lua
**Functions:**
- GetBiography_GoToBtnUis
**Snippet:**
```lua
function GetBiography_GoToBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Biography_LeftBtnByName.lua.lua
**Functions:**
- GetBiography_LeftBtnUis
**Snippet:**
```lua
function GetBiography_LeftBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Biography_RightBtnByName.lua.lua
**Functions:**
- GetBiography_RightBtnUis
**Snippet:**
```lua
function GetBiography_RightBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Biography_TaskBtnByName.lua.lua
**Functions:**
- GetBiography_TaskBtnUis
**Requires:**
- Biography_CompleteTipsByName
- CommonResource_ItemFrameByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("Biography_CompleteTipsByName")
require("CommonResource_ItemFrameByName")
require("CommonResource_RedDotByName")

function GetBiography_TaskBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NameNumberTxt = ui:GetChild("NameNumberTxt")
  uis.CompleteTips = GetBiography_CompleteTipsUis(ui:GetChild("CompleteTips"))
  uis.Item = GetCommonResource_ItemFrameUis(ui:GetChild("Item"))
```

---

## BCD/BirthdaySettingWindow.lua.lua
**Functions:**
- BirthdaySettingWindow.ReInitData
- BirthdaySettingWindow.OnInit
- BirthdaySettingWindow.UpdateInfo
- monthlist.itemRenderer
- daylist.itemRenderer
- BirthdaySettingWindow.InitBtn
- BirthdaySettingWindow.OnClose
**Requires:**
- PlayerInfo_BirthdayTipsWindowByName
**Snippet:**
```lua
require("PlayerInfo_BirthdayTipsWindowByName")
local BirthdaySettingWindow = {}
local uis, contentPane
local MONTHS = 12
local selectedDay, selectedMonth, monthTweener, dayTweener
local getDays = function(month)
  if type(month) ~= "number" or month < 1 or month > MONTHS then
    return math.huge
  end
  if 1 == month or 3 == month or 5 == month or 7 == month or 8 == month or 10 == month or 12 == month then
```

---

## BCD/Body.lua.lua
**Functions:**
- Body:__ctor
- Body:__delete
- Body:init
- Body:saveStatus
- Body:setMass
- Body:setInertia
- Body:setPos
- Body:setAngle
- Body:setForce
- Body:getVelSq
- Body:applyImpulse
- Body:applyForce
- Body:applyForceTorque
- Body:applyTorque
- Body:applyDamping
- Body:applyDampingAng
- Body:awake
- Body:update
- Body:integrate
- Body:integrateVel
- Body:integrateVelAngle
- Body:integrateAngle
- Body:integratePos
- Body:drawaabb
**Snippet:**
```lua
local Body = Create("Body")

function Body:__ctor()
  self.bodyType = BodyType.Dynamic
  self.disabled = false
  self.sleeping = false
  self.sleepTime = 0
  self.autoSleep = true
  self.x = nil
  self.y = nil
```

---

## BCD/BossBattleFireWindow.lua.lua
**Functions:**
- BossBattleFireWindow.ReInitData
- BossBattleFireWindow.OnInit
- BossBattleFireWindow.UpdateTextDisplay
- BossBattleFireWindow.LoadChangeEffect
- BossBattleFireWindow.ReleaseTexture
- BossBattleFireWindow.UpdateInfo
- list.itemRenderer
- BossBattleFireWindow.ShowStateInfo
- BossBattleFireWindow.ShowTips
- BossBattleFireWindow.StartBattle
- BossBattleFireWindow.AiBattleOnClick
- BossBattleFireWindow.InitBtn
- BossBattleFireWindow.UpdateMultiDropInfo
- list.itemRenderer
- BossBattleFireWindow.UpdateMultiple
- BossBattleFireWindow.OnShown
- BossBattleFireWindow.OnClose
**Requires:**
- BossDungeonFire_BossBattleWindowByName
**Snippet:**
```lua
require("BossDungeonFire_BossBattleWindowByName")
local BossBattleFireWindow = {}
local uis, contentPane, chapterData, curStageData, stageCost, jumpTb, bossSpineName, changeTexture, changeEffect, tween

function BossBattleFireWindow.ReInitData()
end

function BossBattleFireWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BossBattleFireWindow.package, WinResConfig.BossBattleFireWindow.comName, function(com)
    contentPane = com
```

---

## BCD/BossBattleWaterWindow.lua.lua
**Functions:**
- BossBattleWaterWindow.ReInitData
- BossBattleWaterWindow.OnInit
- BossBattleWaterWindow.UpdateTextDisplay
- BossBattleWaterWindow.LoadChangeEffect
- BossBattleWaterWindow.ReleaseTexture
- BossBattleWaterWindow.UpdateInfo
- list.itemRenderer
- BossBattleWaterWindow.ShowStateInfo
- BossBattleWaterWindow.ShowTips
- BossBattleWaterWindow.StartBattle
- BossBattleWaterWindow.AiBattleOnClick
- BossBattleWaterWindow.InitBtn
- BossBattleWaterWindow.UpdateMultiDropInfo
- list.itemRenderer
- BossBattleWaterWindow.UpdateMultiple
- BossBattleWaterWindow.OnShown
- BossBattleWaterWindow.OnClose
**Requires:**
- BossDungeonWater_BossBattleWindowByName
**Snippet:**
```lua
require("BossDungeonWater_BossBattleWindowByName")
local BossBattleWaterWindow = {}
local uis, contentPane, chapterData, curStageData, stageCost, jumpTb, bossSpineName, changeTexture, changeEffect, tween

function BossBattleWaterWindow.ReInitData()
end

function BossBattleWaterWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BossBattleWaterWindow.package, WinResConfig.BossBattleWaterWindow.comName, function(com)
    contentPane = com
```

---

## BCD/BossBattleWoodWindow.lua.lua
**Functions:**
- BossBattleWoodWindow.ReInitData
- BossBattleWoodWindow.OnInit
- BossBattleWoodWindow.UpdateTextDisplay
- BossBattleWoodWindow.LoadChangeEffect
- BossBattleWoodWindow.ReleaseTexture
- BossBattleWoodWindow.UpdateInfo
- list.itemRenderer
- BossBattleWoodWindow.ShowStateInfo
- BossBattleWoodWindow.ShowTips
- BossBattleWoodWindow.StartBattle
- BossBattleWoodWindow.AiBattleOnClick
- BossBattleWoodWindow.InitBtn
- BossBattleWoodWindow.UpdateMultiDropInfo
- list.itemRenderer
- BossBattleWoodWindow.UpdateMultiple
- BossBattleWoodWindow.OnShown
- BossBattleWoodWindow.OnClose
**Requires:**
- BossDungeonWood_BossBattleWindowByName
**Snippet:**
```lua
require("BossDungeonWood_BossBattleWindowByName")
local BossBattleWoodWindow = {}
local uis, contentPane, chapterData, curStageData, stageCost, jumpTb, bossSpineName, changeTexture, changeEffect, tween

function BossBattleWoodWindow.ReInitData()
end

function BossBattleWoodWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BossBattleWoodWindow.package, WinResConfig.BossBattleWoodWindow.comName, function(com)
    contentPane = com
```

---

## BCD/BossDungeonData.lua.lua
**Snippet:**
```lua
BossDungeonData = {}
```

---

## BCD/BossDungeonFireWindow.lua.lua
**Functions:**
- BossDungeonFireWindow.ReInitData
- BossDungeonFireWindow.OnInit
- BossDungeonFireWindow.UpdateInfo
- BossDungeonFireWindow.InitBtn
- BossDungeonFireWindow.OnClose
**Requires:**
- BossDungeonFire_BossDungeonWindowByName
**Snippet:**
```lua
require("BossDungeonFire_BossDungeonWindowByName")
local BossDungeonFireWindow = {}
local uis, contentPane, chapterId, jumpTb

function BossDungeonFireWindow.ReInitData()
end

function BossDungeonFireWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BossDungeonFireWindow.package, WinResConfig.BossDungeonFireWindow.comName, function(com)
    contentPane = com
```

---

## BCD/BossDungeonFire_BossBattleByName.lua.lua
**Functions:**
- GetBossDungeonFire_BossBattleUis
**Requires:**
- CommonResource_BackGroundByName
- BossDungeonFire_InfoByName
- BossDungeonFire_GradeRegionByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("BossDungeonFire_InfoByName")
require("BossDungeonFire_GradeRegionByName")
require("CommonResource_CurrencyReturnByName")

function GetBossDungeonFire_BossBattleUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Info = GetBossDungeonFire_InfoUis(ui:GetChild("Info"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
```

---

## BCD/BossDungeonFire_BossBattleWindowByName.lua.lua
**Functions:**
- GetBossDungeonFire_BossBattleWindowUis
**Requires:**
- BossDungeonFire_BossBattleByName
**Snippet:**
```lua
require("BossDungeonFire_BossBattleByName")

function GetBossDungeonFire_BossBattleWindowUis(ui)
  local uis = {}
  uis.Main = GetBossDungeonFire_BossBattleUis(ui:GetChild("Main"))
  uis.stageCtr = ui:GetController("stage")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonFire_BossDungeonByName.lua.lua
**Functions:**
- GetBossDungeonFire_BossDungeonUis
**Requires:**
- BossDungeonFire_BossMainByName
**Snippet:**
```lua
require("BossDungeonFire_BossMainByName")

function GetBossDungeonFire_BossDungeonUis(ui)
  local uis = {}
  uis.BossMain = GetBossDungeonFire_BossMainUis(ui:GetChild("BossMain"))
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonFire_BossDungeonWindowByName.lua.lua
**Functions:**
- GetBossDungeonFire_BossDungeonWindowUis
**Requires:**
- BossDungeonFire_BossDungeonByName
**Snippet:**
```lua
require("BossDungeonFire_BossDungeonByName")

function GetBossDungeonFire_BossDungeonWindowUis(ui)
  local uis = {}
  uis.Main = GetBossDungeonFire_BossDungeonUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonFire_BossMainByName.lua.lua
**Functions:**
- GetBossDungeonFire_BossMainUis
**Requires:**
- CommonResource_BackGroundByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("CommonResource_CurrencyReturnByName")

function GetBossDungeonFire_BossMainUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Enter1Btn = ui:GetChild("Enter1Btn")
  uis.Enter2Btn = ui:GetChild("Enter2Btn")
  uis.CurrencyReturn = GetCommonResource_CurrencyReturnUis(ui:GetChild("CurrencyReturn"))
  uis.root = ui
```

---

## BCD/BossDungeonFire_BuffByName.lua.lua
**Functions:**
- GetBossDungeonFire_BuffUis
**Snippet:**
```lua
function GetBossDungeonFire_BuffUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonFire_ButtonRegionByName.lua.lua
**Functions:**
- GetBossDungeonFire_ButtonRegionUis
**Requires:**
- BossDungeonFire_EnergyLabelByName
**Snippet:**
```lua
require("BossDungeonFire_EnergyLabelByName")

function GetBossDungeonFire_ButtonRegionUis(ui)
  local uis = {}
  uis.EnergyLabel = GetBossDungeonFire_EnergyLabelUis(ui:GetChild("EnergyLabel"))
  uis.DispatchBtn = ui:GetChild("DispatchBtn")
  uis.Star1Btn = ui:GetChild("Star1Btn")
  uis.Star2Btn = ui:GetChild("Star2Btn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## BCD/BossDungeonFire_DispatchBtnByName.lua.lua
**Functions:**
- GetBossDungeonFire_DispatchBtnUis
**Snippet:**
```lua
function GetBossDungeonFire_DispatchBtnUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonFire_EnergyLabelByName.lua.lua
**Functions:**
- GetBossDungeonFire_EnergyLabelUis
**Snippet:**
```lua
function GetBossDungeonFire_EnergyLabelUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonFire_Enter1BtnByName.lua.lua
**Functions:**
- GetBossDungeonFire_Enter1BtnUis
**Requires:**
- BossDungeonFire_TimeByName
**Snippet:**
```lua
require("BossDungeonFire_TimeByName")

function GetBossDungeonFire_Enter1BtnUis(ui)
  local uis = {}
  uis.Time = GetBossDungeonFire_TimeUis(ui:GetChild("Time"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.timeCtr = ui:GetController("time")
  uis.root = ui
  return uis
```

---

## BCD/BossDungeonFire_Enter2BtnByName.lua.lua
**Functions:**
- GetBossDungeonFire_Enter2BtnUis
**Requires:**
- BossDungeonFire_TimeByName
**Snippet:**
```lua
require("BossDungeonFire_TimeByName")

function GetBossDungeonFire_Enter2BtnUis(ui)
  local uis = {}
  uis.Time = GetBossDungeonFire_TimeUis(ui:GetChild("Time"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.timeCtr = ui:GetController("time")
  uis.root = ui
  return uis
```

---

## BCD/BossDungeonFire_GradeBtnByName.lua.lua
**Functions:**
- GetBossDungeonFire_GradeBtnUis
**Snippet:**
```lua
function GetBossDungeonFire_GradeBtnUis(ui)
  local uis = {}
  
  uis.GradeTxt = ui:GetChild("GradeTxt")
  uis.CardShowHolder = ui:GetChild("CardShowHolder")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
```

---

## BCD/BossDungeonFire_GradeRegionByName.lua.lua
**Functions:**
- GetBossDungeonFire_GradeRegionUis
**Snippet:**
```lua
function GetBossDungeonFire_GradeRegionUis(ui)
  local uis = {}
  
  uis.GradeList = ui:GetChild("GradeList")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonFire_InfoByName.lua.lua
**Functions:**
- GetBossDungeonFire_InfoUis
**Requires:**
- BossDungeonFire_TitleByName
- BossDungeonFire_OpinionByName
- BossDungeonFire_BuffByName
- BossDungeonFire_RewardByName
- BossDungeonFire_ButtonRegionByName
**Snippet:**
```lua
require("BossDungeonFire_TitleByName")
require("BossDungeonFire_OpinionByName")
require("BossDungeonFire_BuffByName")
require("BossDungeonFire_RewardByName")
require("BossDungeonFire_ButtonRegionByName")

function GetBossDungeonFire_InfoUis(ui)
  local uis = {}
  uis.Title = GetBossDungeonFire_TitleUis(ui:GetChild("Title"))
  uis.Opinion = GetBossDungeonFire_OpinionUis(ui:GetChild("Opinion"))
```

---

## BCD/BossDungeonFire_OpinionByName.lua.lua
**Functions:**
- GetBossDungeonFire_OpinionUis
**Snippet:**
```lua
function GetBossDungeonFire_OpinionUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonFire_RewardByName.lua.lua
**Functions:**
- GetBossDungeonFire_RewardUis
**Snippet:**
```lua
function GetBossDungeonFire_RewardUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonFire_Star1BtnByName.lua.lua
**Functions:**
- GetBossDungeonFire_Star1BtnUis
**Snippet:**
```lua
function GetBossDungeonFire_Star1BtnUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonFire_Star2BtnByName.lua.lua
**Functions:**
- GetBossDungeonFire_Star2BtnUis
**Snippet:**
```lua
function GetBossDungeonFire_Star2BtnUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonFire_TimeByName.lua.lua
**Functions:**
- GetBossDungeonFire_TimeUis
**Snippet:**
```lua
function GetBossDungeonFire_TimeUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonFire_TitleByName.lua.lua
**Functions:**
- GetBossDungeonFire_TitleUis
**Snippet:**
```lua
function GetBossDungeonFire_TitleUis(ui)
  local uis = {}
  
  uis.Title3Txt = ui:GetChild("Title3Txt")
  uis.Title1Txt = ui:GetChild("Title1Txt")
  uis.Title2Txt = ui:GetChild("Title2Txt")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonMgr.lua.lua
**Functions:**
- BossDungeonMgr.OpenWindow
- BossDungeonMgr.OpenBossBattleWindow
- BossDungeonMgr.GetJumpChapterId
- BossDungeonMgr.SufficientQuantity
- BossDungeonMgr.GetBadgeIdByRewardShow
- BossDungeonMgr.InitAssetsTips
**Snippet:**
```lua
BossDungeonMgr = {lastStageId = nil}

function BossDungeonMgr.OpenWindow(type, chapterId)
  AdventureService.GetChapterStageReq(chapterId, function()
    BossDungeonMgr.lastStageId = nil
    if type == ProtoEnum.SCENE_TYPE.BOSS_FIRE then
      OpenWindow(WinResConfig.BossDungeonFireWindow.name, nil, chapterId)
    elseif type == ProtoEnum.SCENE_TYPE.BOSS_WATER then
      OpenWindow(WinResConfig.BossDungeonWaterWindow.name, nil, chapterId)
    elseif type == ProtoEnum.SCENE_TYPE.BOSS_WOOD then
```

---

## BCD/BossDungeonScriptList.lua.lua
**Requires:**
- BossDungeonService
- BossDungeonData
- BossDungeonMgr
**Snippet:**
```lua
local require = require
require("BossDungeonService")
require("BossDungeonData")
require("BossDungeonMgr")
```

---

## BCD/BossDungeonService.lua.lua
**Snippet:**
```lua
BossDungeonService = {}
```

---

## BCD/BossDungeonWaterWindow.lua.lua
**Functions:**
- BossDungeonWaterWindow.ReInitData
- BossDungeonWaterWindow.OnInit
- BossDungeonWaterWindow.UpdateInfo
- BossDungeonWaterWindow.InitBtn
- BossDungeonWaterWindow.OnClose
**Requires:**
- BossDungeonWater_BossDungeonWindowByName
**Snippet:**
```lua
require("BossDungeonWater_BossDungeonWindowByName")
local BossDungeonWaterWindow = {}
local uis, contentPane, chapterId, jumpTb

function BossDungeonWaterWindow.ReInitData()
end

function BossDungeonWaterWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BossDungeonWaterWindow.package, WinResConfig.BossDungeonWaterWindow.comName, function(com)
    contentPane = com
```

---

## BCD/BossDungeonWater_BossBattleByName.lua.lua
**Functions:**
- GetBossDungeonWater_BossBattleUis
**Requires:**
- CommonResource_BackGroundByName
- BossDungeonWater_InfoByName
- BossDungeonWater_GradeRegionByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("BossDungeonWater_InfoByName")
require("BossDungeonWater_GradeRegionByName")
require("CommonResource_CurrencyReturnByName")

function GetBossDungeonWater_BossBattleUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Info = GetBossDungeonWater_InfoUis(ui:GetChild("Info"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
```

---

## BCD/BossDungeonWater_BossBattleWindowByName.lua.lua
**Functions:**
- GetBossDungeonWater_BossBattleWindowUis
**Requires:**
- BossDungeonWater_BossBattleByName
**Snippet:**
```lua
require("BossDungeonWater_BossBattleByName")

function GetBossDungeonWater_BossBattleWindowUis(ui)
  local uis = {}
  uis.Main = GetBossDungeonWater_BossBattleUis(ui:GetChild("Main"))
  uis.stageCtr = ui:GetController("stage")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonWater_BossDungeonByName.lua.lua
**Functions:**
- GetBossDungeonWater_BossDungeonUis
**Requires:**
- BossDungeonWater_BossMainByName
**Snippet:**
```lua
require("BossDungeonWater_BossMainByName")

function GetBossDungeonWater_BossDungeonUis(ui)
  local uis = {}
  uis.BossMain = GetBossDungeonWater_BossMainUis(ui:GetChild("BossMain"))
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonWater_BossDungeonWindowByName.lua.lua
**Functions:**
- GetBossDungeonWater_BossDungeonWindowUis
**Requires:**
- BossDungeonWater_BossDungeonByName
**Snippet:**
```lua
require("BossDungeonWater_BossDungeonByName")

function GetBossDungeonWater_BossDungeonWindowUis(ui)
  local uis = {}
  uis.Main = GetBossDungeonWater_BossDungeonUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonWater_BossMainByName.lua.lua
**Functions:**
- GetBossDungeonWater_BossMainUis
**Requires:**
- CommonResource_BackGroundByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("CommonResource_CurrencyReturnByName")

function GetBossDungeonWater_BossMainUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Enter1Btn = ui:GetChild("Enter1Btn")
  uis.Enter2Btn = ui:GetChild("Enter2Btn")
  uis.CurrencyReturn = GetCommonResource_CurrencyReturnUis(ui:GetChild("CurrencyReturn"))
  uis.root = ui
```

---

## BCD/BossDungeonWater_BuffByName.lua.lua
**Functions:**
- GetBossDungeonWater_BuffUis
**Snippet:**
```lua
function GetBossDungeonWater_BuffUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonWater_ButtonRegionByName.lua.lua
**Functions:**
- GetBossDungeonWater_ButtonRegionUis
**Requires:**
- BossDungeonWater_EnergyLabelByName
**Snippet:**
```lua
require("BossDungeonWater_EnergyLabelByName")

function GetBossDungeonWater_ButtonRegionUis(ui)
  local uis = {}
  uis.EnergyLabel = GetBossDungeonWater_EnergyLabelUis(ui:GetChild("EnergyLabel"))
  uis.DispatchBtn = ui:GetChild("DispatchBtn")
  uis.Star1Btn = ui:GetChild("Star1Btn")
  uis.Star2Btn = ui:GetChild("Star2Btn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## BCD/BossDungeonWater_DispatchBtnByName.lua.lua
**Functions:**
- GetBossDungeonWater_DispatchBtnUis
**Snippet:**
```lua
function GetBossDungeonWater_DispatchBtnUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonWater_EnergyLabelByName.lua.lua
**Functions:**
- GetBossDungeonWater_EnergyLabelUis
**Snippet:**
```lua
function GetBossDungeonWater_EnergyLabelUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonWater_Enter1BtnByName.lua.lua
**Functions:**
- GetBossDungeonWater_Enter1BtnUis
**Requires:**
- BossDungeonWater_TimeByName
**Snippet:**
```lua
require("BossDungeonWater_TimeByName")

function GetBossDungeonWater_Enter1BtnUis(ui)
  local uis = {}
  uis.Time = GetBossDungeonWater_TimeUis(ui:GetChild("Time"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.timeCtr = ui:GetController("time")
  uis.root = ui
  return uis
```

---

## BCD/BossDungeonWater_Enter2BtnByName.lua.lua
**Functions:**
- GetBossDungeonWater_Enter2BtnUis
**Requires:**
- BossDungeonWater_TimeByName
**Snippet:**
```lua
require("BossDungeonWater_TimeByName")

function GetBossDungeonWater_Enter2BtnUis(ui)
  local uis = {}
  uis.Time = GetBossDungeonWater_TimeUis(ui:GetChild("Time"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.timeCtr = ui:GetController("time")
  uis.root = ui
  return uis
```

---

## BCD/BossDungeonWater_GradeBtnByName.lua.lua
**Functions:**
- GetBossDungeonWater_GradeBtnUis
**Snippet:**
```lua
function GetBossDungeonWater_GradeBtnUis(ui)
  local uis = {}
  
  uis.GradeTxt = ui:GetChild("GradeTxt")
  uis.CardShowHolder = ui:GetChild("CardShowHolder")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
```

---

## BCD/BossDungeonWater_GradeRegionByName.lua.lua
**Functions:**
- GetBossDungeonWater_GradeRegionUis
**Snippet:**
```lua
function GetBossDungeonWater_GradeRegionUis(ui)
  local uis = {}
  
  uis.GradeList = ui:GetChild("GradeList")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonWater_InfoByName.lua.lua
**Functions:**
- GetBossDungeonWater_InfoUis
**Requires:**
- BossDungeonWater_TitleByName
- BossDungeonWater_OpinionByName
- BossDungeonWater_BuffByName
- BossDungeonWater_RewardByName
- BossDungeonWater_ButtonRegionByName
**Snippet:**
```lua
require("BossDungeonWater_TitleByName")
require("BossDungeonWater_OpinionByName")
require("BossDungeonWater_BuffByName")
require("BossDungeonWater_RewardByName")
require("BossDungeonWater_ButtonRegionByName")

function GetBossDungeonWater_InfoUis(ui)
  local uis = {}
  uis.Title = GetBossDungeonWater_TitleUis(ui:GetChild("Title"))
  uis.Opinion = GetBossDungeonWater_OpinionUis(ui:GetChild("Opinion"))
```

---

## BCD/BossDungeonWater_OpinionByName.lua.lua
**Functions:**
- GetBossDungeonWater_OpinionUis
**Snippet:**
```lua
function GetBossDungeonWater_OpinionUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonWater_RewardByName.lua.lua
**Functions:**
- GetBossDungeonWater_RewardUis
**Snippet:**
```lua
function GetBossDungeonWater_RewardUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonWater_Star1BtnByName.lua.lua
**Functions:**
- GetBossDungeonWater_Star1BtnUis
**Snippet:**
```lua
function GetBossDungeonWater_Star1BtnUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonWater_Star2BtnByName.lua.lua
**Functions:**
- GetBossDungeonWater_Star2BtnUis
**Snippet:**
```lua
function GetBossDungeonWater_Star2BtnUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonWater_TimeByName.lua.lua
**Functions:**
- GetBossDungeonWater_TimeUis
**Snippet:**
```lua
function GetBossDungeonWater_TimeUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonWater_TitleByName.lua.lua
**Functions:**
- GetBossDungeonWater_TitleUis
**Snippet:**
```lua
function GetBossDungeonWater_TitleUis(ui)
  local uis = {}
  
  uis.Title3Txt = ui:GetChild("Title3Txt")
  uis.Title1Txt = ui:GetChild("Title1Txt")
  uis.Title2Txt = ui:GetChild("Title2Txt")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonWoodWindow.lua.lua
**Functions:**
- BossDungeonWoodWindow.ReInitData
- BossDungeonWoodWindow.OnInit
- BossDungeonWoodWindow.UpdateInfo
- BossDungeonWoodWindow.InitBtn
- BossDungeonWoodWindow.OnClose
**Requires:**
- BossDungeonWood_BossDungeonWindowByName
**Snippet:**
```lua
require("BossDungeonWood_BossDungeonWindowByName")
local BossDungeonWoodWindow = {}
local uis, contentPane, chapterId, jumpTb

function BossDungeonWoodWindow.ReInitData()
end

function BossDungeonWoodWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BossDungeonWoodWindow.package, WinResConfig.BossDungeonWoodWindow.comName, function(com)
    contentPane = com
```

---

## BCD/BossDungeonWood_BossBattleByName.lua.lua
**Functions:**
- GetBossDungeonWood_BossBattleUis
**Requires:**
- CommonResource_BackGroundByName
- BossDungeonWood_InfoByName
- BossDungeonWood_GradeRegionByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("BossDungeonWood_InfoByName")
require("BossDungeonWood_GradeRegionByName")
require("CommonResource_CurrencyReturnByName")

function GetBossDungeonWood_BossBattleUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Info = GetBossDungeonWood_InfoUis(ui:GetChild("Info"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
```

---

## BCD/BossDungeonWood_BossBattleWindowByName.lua.lua
**Functions:**
- GetBossDungeonWood_BossBattleWindowUis
**Requires:**
- BossDungeonWood_BossBattleByName
**Snippet:**
```lua
require("BossDungeonWood_BossBattleByName")

function GetBossDungeonWood_BossBattleWindowUis(ui)
  local uis = {}
  uis.Main = GetBossDungeonWood_BossBattleUis(ui:GetChild("Main"))
  uis.stageCtr = ui:GetController("stage")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonWood_BossDungeonByName.lua.lua
**Functions:**
- GetBossDungeonWood_BossDungeonUis
**Requires:**
- BossDungeonWood_BossMainByName
**Snippet:**
```lua
require("BossDungeonWood_BossMainByName")

function GetBossDungeonWood_BossDungeonUis(ui)
  local uis = {}
  uis.BossMain = GetBossDungeonWood_BossMainUis(ui:GetChild("BossMain"))
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonWood_BossDungeonWindowByName.lua.lua
**Functions:**
- GetBossDungeonWood_BossDungeonWindowUis
**Requires:**
- BossDungeonWood_BossDungeonByName
**Snippet:**
```lua
require("BossDungeonWood_BossDungeonByName")

function GetBossDungeonWood_BossDungeonWindowUis(ui)
  local uis = {}
  uis.Main = GetBossDungeonWood_BossDungeonUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonWood_BossMainByName.lua.lua
**Functions:**
- GetBossDungeonWood_BossMainUis
**Requires:**
- CommonResource_BackGroundByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("CommonResource_CurrencyReturnByName")

function GetBossDungeonWood_BossMainUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Enter1Btn = ui:GetChild("Enter1Btn")
  uis.Enter2Btn = ui:GetChild("Enter2Btn")
  uis.CurrencyReturn = GetCommonResource_CurrencyReturnUis(ui:GetChild("CurrencyReturn"))
  uis.root = ui
```

---

## BCD/BossDungeonWood_BuffByName.lua.lua
**Functions:**
- GetBossDungeonWood_BuffUis
**Snippet:**
```lua
function GetBossDungeonWood_BuffUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonWood_ButtonRegionByName.lua.lua
**Functions:**
- GetBossDungeonWood_ButtonRegionUis
**Requires:**
- BossDungeonWood_EnergyLabelByName
**Snippet:**
```lua
require("BossDungeonWood_EnergyLabelByName")

function GetBossDungeonWood_ButtonRegionUis(ui)
  local uis = {}
  uis.EnergyLabel = GetBossDungeonWood_EnergyLabelUis(ui:GetChild("EnergyLabel"))
  uis.DispatchBtn = ui:GetChild("DispatchBtn")
  uis.Star1Btn = ui:GetChild("Star1Btn")
  uis.Star2Btn = ui:GetChild("Star2Btn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## BCD/BossDungeonWood_DispatchBtnByName.lua.lua
**Functions:**
- GetBossDungeonWood_DispatchBtnUis
**Snippet:**
```lua
function GetBossDungeonWood_DispatchBtnUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonWood_EnergyLabelByName.lua.lua
**Functions:**
- GetBossDungeonWood_EnergyLabelUis
**Snippet:**
```lua
function GetBossDungeonWood_EnergyLabelUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonWood_Enter1BtnByName.lua.lua
**Functions:**
- GetBossDungeonWood_Enter1BtnUis
**Requires:**
- BossDungeonWood_TimeByName
**Snippet:**
```lua
require("BossDungeonWood_TimeByName")

function GetBossDungeonWood_Enter1BtnUis(ui)
  local uis = {}
  uis.Time = GetBossDungeonWood_TimeUis(ui:GetChild("Time"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.timeCtr = ui:GetController("time")
  uis.root = ui
  return uis
```

---

## BCD/BossDungeonWood_Enter2BtnByName.lua.lua
**Functions:**
- GetBossDungeonWood_Enter2BtnUis
**Requires:**
- BossDungeonWood_TimeByName
**Snippet:**
```lua
require("BossDungeonWood_TimeByName")

function GetBossDungeonWood_Enter2BtnUis(ui)
  local uis = {}
  uis.Time = GetBossDungeonWood_TimeUis(ui:GetChild("Time"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.timeCtr = ui:GetController("time")
  uis.root = ui
  return uis
```

---

## BCD/BossDungeonWood_GradeBtnByName.lua.lua
**Functions:**
- GetBossDungeonWood_GradeBtnUis
**Snippet:**
```lua
function GetBossDungeonWood_GradeBtnUis(ui)
  local uis = {}
  
  uis.GradeTxt = ui:GetChild("GradeTxt")
  uis.CardShowHolder = ui:GetChild("CardShowHolder")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
```

---

## BCD/BossDungeonWood_GradeRegionByName.lua.lua
**Functions:**
- GetBossDungeonWood_GradeRegionUis
**Snippet:**
```lua
function GetBossDungeonWood_GradeRegionUis(ui)
  local uis = {}
  
  uis.GradeList = ui:GetChild("GradeList")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonWood_InfoByName.lua.lua
**Functions:**
- GetBossDungeonWood_InfoUis
**Requires:**
- BossDungeonWood_TitleByName
- BossDungeonWood_OpinionByName
- BossDungeonWood_BuffByName
- BossDungeonWood_RewardByName
- BossDungeonWood_ButtonRegionByName
**Snippet:**
```lua
require("BossDungeonWood_TitleByName")
require("BossDungeonWood_OpinionByName")
require("BossDungeonWood_BuffByName")
require("BossDungeonWood_RewardByName")
require("BossDungeonWood_ButtonRegionByName")

function GetBossDungeonWood_InfoUis(ui)
  local uis = {}
  uis.Title = GetBossDungeonWood_TitleUis(ui:GetChild("Title"))
  uis.Opinion = GetBossDungeonWood_OpinionUis(ui:GetChild("Opinion"))
```

---

## BCD/BossDungeonWood_OpinionByName.lua.lua
**Functions:**
- GetBossDungeonWood_OpinionUis
**Snippet:**
```lua
function GetBossDungeonWood_OpinionUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonWood_RewardByName.lua.lua
**Functions:**
- GetBossDungeonWood_RewardUis
**Snippet:**
```lua
function GetBossDungeonWood_RewardUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonWood_Star1BtnByName.lua.lua
**Functions:**
- GetBossDungeonWood_Star1BtnUis
**Snippet:**
```lua
function GetBossDungeonWood_Star1BtnUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonWood_Star2BtnByName.lua.lua
**Functions:**
- GetBossDungeonWood_Star2BtnUis
**Snippet:**
```lua
function GetBossDungeonWood_Star2BtnUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonWood_TimeByName.lua.lua
**Functions:**
- GetBossDungeonWood_TimeUis
**Snippet:**
```lua
function GetBossDungeonWood_TimeUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeonWood_TitleByName.lua.lua
**Functions:**
- GetBossDungeonWood_TitleUis
**Snippet:**
```lua
function GetBossDungeonWood_TitleUis(ui)
  local uis = {}
  
  uis.Title3Txt = ui:GetChild("Title3Txt")
  uis.Title1Txt = ui:GetChild("Title1Txt")
  uis.Title2Txt = ui:GetChild("Title2Txt")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeon_ActivityBossByName.lua.lua
**Functions:**
- GetBossDungeon_ActivityBossUis
**Requires:**
- BossDungeon_BossPicByName
- BossDungeon_BossInfoByName
**Snippet:**
```lua
require("BossDungeon_BossPicByName")
require("BossDungeon_BossInfoByName")

function GetBossDungeon_ActivityBossUis(ui)
  local uis = {}
  uis.BossPic = GetBossDungeon_BossPicUis(ui:GetChild("BossPic"))
  uis.BossInfo = GetBossDungeon_BossInfoUis(ui:GetChild("BossInfo"))
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeon_ActivityListByName.lua.lua
**Functions:**
- GetBossDungeon_ActivityListUis
**Requires:**
- CommonResource_BackGroundByName
- CommonResource_CurrencyReturnByName
- BossDungeon_TitleByName
- BossDungeon_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("CommonResource_CurrencyReturnByName")
require("BossDungeon_TitleByName")
require("BossDungeon_TimeByName")

function GetBossDungeon_ActivityListUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.CurrencyReturn = GetCommonResource_CurrencyReturnUis(ui:GetChild("CurrencyReturn"))
  uis.Title = GetBossDungeon_TitleUis(ui:GetChild("Title"))
```

---

## BCD/BossDungeon_ActivityListWindowByName.lua.lua
**Functions:**
- GetBossDungeon_ActivityListWindowUis
**Requires:**
- BossDungeon_ActivityListByName
**Snippet:**
```lua
require("BossDungeon_ActivityListByName")

function GetBossDungeon_ActivityListWindowUis(ui)
  local uis = {}
  uis.Main = GetBossDungeon_ActivityListUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeon_BossDungeonByName.lua.lua
**Functions:**
- GetBossDungeon_BossDungeonUis
**Requires:**
- CommonResource_BackGroundByName
- BossDungeon_TimeByName
- BossDungeon_BossLoadModuleByName
- BossDungeon_TabRegionByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("BossDungeon_TimeByName")
require("BossDungeon_BossLoadModuleByName")
require("BossDungeon_TabRegionByName")
require("CommonResource_CurrencyReturnByName")

function GetBossDungeon_BossDungeonUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Time = GetBossDungeon_TimeUis(ui:GetChild("Time"))
```

---

## BCD/BossDungeon_BossDungeonWindowByName.lua.lua
**Functions:**
- GetBossDungeon_BossDungeonWindowUis
**Requires:**
- BossDungeon_BossDungeonByName
**Snippet:**
```lua
require("BossDungeon_BossDungeonByName")

function GetBossDungeon_BossDungeonWindowUis(ui)
  local uis = {}
  uis.Main = GetBossDungeon_BossDungeonUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeon_BossInfoByName.lua.lua
**Functions:**
- GetBossDungeon_BossInfoUis
**Snippet:**
```lua
function GetBossDungeon_BossInfoUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.HpTxt = ui:GetChild("HpTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## BCD/BossDungeon_BossLoadModuleByName.lua.lua
**Functions:**
- GetBossDungeon_BossLoadModuleUis
**Snippet:**
```lua
function GetBossDungeon_BossLoadModuleUis(ui)
  local uis = {}
  
  uis.BossList = ui:GetChild("BossList")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeon_BossOpenTipsByName.lua.lua
**Functions:**
- GetBossDungeon_BossOpenTipsUis
**Requires:**
- CommonResource_PopupBgByName
- BossDungeon_TipsBgByName
- BossDungeon_TipsNumberByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("BossDungeon_TipsBgByName")
require("BossDungeon_TipsNumberByName")

function GetBossDungeon_BossOpenTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.TipsBg = GetBossDungeon_TipsBgUis(ui:GetChild("TipsBg"))
  uis.TipsNumber = GetBossDungeon_TipsNumberUis(ui:GetChild("TipsNumber"))
```

---

## BCD/BossDungeon_BossOpenTipsWindowByName.lua.lua
**Functions:**
- GetBossDungeon_BossOpenTipsWindowUis
**Requires:**
- BossDungeon_BossOpenTipsByName
**Snippet:**
```lua
require("BossDungeon_BossOpenTipsByName")

function GetBossDungeon_BossOpenTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetBossDungeon_BossOpenTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeon_BossPicByName.lua.lua
**Functions:**
- GetBossDungeon_BossPicUis
**Snippet:**
```lua
function GetBossDungeon_BossPicUis(ui)
  local uis = {}
  
  uis.BossLoader = ui:GetChild("BossLoader")
  uis.BossHolder = ui:GetChild("BossHolder")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeon_BossTipsAniByName.lua.lua
**Functions:**
- GetBossDungeon_BossTipsAniUis
**Requires:**
- BossDungeon_BossTipsByName
**Snippet:**
```lua
require("BossDungeon_BossTipsByName")

function GetBossDungeon_BossTipsAniUis(ui)
  local uis = {}
  uis.BossTips = GetBossDungeon_BossTipsUis(ui:GetChild("BossTips"))
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeon_BossTipsByName.lua.lua
**Functions:**
- GetBossDungeon_BossTipsUis
**Requires:**
- BossDungeon_StageByName
**Snippet:**
```lua
require("BossDungeon_StageByName")

function GetBossDungeon_BossTipsUis(ui)
  local uis = {}
  uis.Stage = GetBossDungeon_StageUis(ui:GetChild("Stage"))
  uis.HeadBtn = ui:GetChild("HeadBtn")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.ElementList = ui:GetChild("ElementList")
  uis.LookBtn = ui:GetChild("LookBtn")
  uis.ChoiceBtn = ui:GetChild("ChoiceBtn")
```

---

## BCD/BossDungeon_HeadPicByName.lua.lua
**Functions:**
- GetBossDungeon_HeadPicUis
**Snippet:**
```lua
function GetBossDungeon_HeadPicUis(ui)
  local uis = {}
  
  uis.HeadLoader = ui:GetChild("HeadLoader")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeon_HpBarByName.lua.lua
**Functions:**
- GetBossDungeon_HpBarUis
**Requires:**
- BossDungeon_HpFillByName
**Snippet:**
```lua
require("BossDungeon_HpFillByName")

function GetBossDungeon_HpBarUis(ui)
  local uis = {}
  uis.bar = GetBossDungeon_HpFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeon_HpFillByName.lua.lua
**Functions:**
- GetBossDungeon_HpFillUis
**Snippet:**
```lua
function GetBossDungeon_HpFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeon_LookBtnByName.lua.lua
**Functions:**
- GetBossDungeon_LookBtnUis
**Snippet:**
```lua
function GetBossDungeon_LookBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeon_NormalBossByName.lua.lua
**Functions:**
- GetBossDungeon_NormalBossUis
**Requires:**
- BossDungeon_BossPicByName
- BossDungeon_BossInfoByName
**Snippet:**
```lua
require("BossDungeon_BossPicByName")
require("BossDungeon_BossInfoByName")

function GetBossDungeon_NormalBossUis(ui)
  local uis = {}
  uis.BossPic = GetBossDungeon_BossPicUis(ui:GetChild("BossPic"))
  uis.BossInfo = GetBossDungeon_BossInfoUis(ui:GetChild("BossInfo"))
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeon_StageByName.lua.lua
**Functions:**
- GetBossDungeon_StageUis
**Snippet:**
```lua
function GetBossDungeon_StageUis(ui)
  local uis = {}
  
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeon_TabBtnByName.lua.lua
**Functions:**
- GetBossDungeon_TabBtnUis
**Snippet:**
```lua
function GetBossDungeon_TabBtnUis(ui)
  local uis = {}
  
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeon_TabRegionByName.lua.lua
**Functions:**
- GetBossDungeon_TabRegionUis
**Snippet:**
```lua
function GetBossDungeon_TabRegionUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeon_TimeByName.lua.lua
**Functions:**
- GetBossDungeon_TimeUis
**Snippet:**
```lua
function GetBossDungeon_TimeUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeon_TipsBgByName.lua.lua
**Functions:**
- GetBossDungeon_TipsBgUis
**Snippet:**
```lua
function GetBossDungeon_TipsBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeon_TipsNumberByName.lua.lua
**Functions:**
- GetBossDungeon_TipsNumberUis
**Snippet:**
```lua
function GetBossDungeon_TipsNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/BossDungeon_TitleByName.lua.lua
**Functions:**
- GetBossDungeon_TitleUis
**Snippet:**
```lua
function GetBossDungeon_TitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/BossOpenTipsWindow.lua.lua
**Functions:**
- BossOpenTipsWindow.ReInitData
- BossOpenTipsWindow.OnInit
- BossOpenTipsWindow.UpdateInfo
- BossOpenTipsWindow.InitBtn
- BossOpenTipsWindow.OnClose
**Requires:**
- BossDungeon_BossOpenTipsWindowByName
**Snippet:**
```lua
require("BossDungeon_BossOpenTipsWindowByName")
local BossOpenTipsWindow = {}
local uis, contentPane, callBack

function BossOpenTipsWindow.ReInitData()
end

function BossOpenTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BossOpenTipsWindow.package, WinResConfig.BossOpenTipsWindow.comName, function(com)
    contentPane = com
```

---

## BCD/BoxGetWindow.lua.lua
**Functions:**
- BoxGetWindow.ReInitData
- BoxGetWindow.OnInit
- BoxGetWindow.UpdateInfo
- list.itemRenderer
- BoxGetWindow.WordList
- list.itemRenderer
- BoxGetWindow.InitBtn
- BoxGetWindow.OnClose
**Requires:**
- Schedule_BoxGetWindowByName
**Snippet:**
```lua
require("Schedule_BoxGetWindowByName")
local BoxGetWindow = {}
local uis, contentPane

function BoxGetWindow.ReInitData()
end

function BoxGetWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BoxGetWindow.package, WinResConfig.BoxGetWindow.comName, function(com)
    contentPane = com
```

---

## BCD/BreachTipsWindow.lua.lua
**Functions:**
- BreachTipsWindow.ReInitData
- BreachTipsWindow.OnInit
- BreachTipsWindow.Init
- uis.Main.BreachBtnList.itemRenderer
- BreachTipsWindow.ListOnClick
- BreachTipsWindow.InitBtn
- BreachTipsWindow.OnShown
- BreachTipsWindow.OnHide
- BreachTipsWindow.OnClose
- BreachTipsWindow.HandleMessage
**Requires:**
- Message_BreachTipsWindowByName
**Snippet:**
```lua
require("Message_BreachTipsWindowByName")
local BreachTipsWindow = {}
local uis, contentPane, cardId, quality

function BreachTipsWindow.ReInitData()
end

function BreachTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BreachTipsWindow.package, WinResConfig.BreachTipsWindow.comName, function(com)
    contentPane = com
```

---

## BCD/BreachUpTipsWindow.lua.lua
**Functions:**
- BreachUpTipsWindow.ReInitData
- BreachUpTipsWindow.OnInit
- BreachUpTipsWindow.GetEffectType
- BreachUpTipsWindow.ShowInfoList
- BreachUpTipsWindow.LoadCardTexture
- BreachUpTipsWindow.UpdateTextDisplay
- BreachUpTipsWindow.InitBtn
- BreachUpTipsWindow.OnShown
- BreachUpTipsWindow.OnHide
- BreachUpTipsWindow.OnClose
- BreachUpTipsWindow.HandleMessage
**Requires:**
- Card_BreachUpTipsWindowByName
**Snippet:**
```lua
require("Card_BreachUpTipsWindowByName")
local BreachUpTipsWindow = {}
local uis, contentPane, lv, bgPrefab, isFourEffect, qualityMax

function BreachUpTipsWindow.ReInitData()
end

function BreachUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BreachUpTipsWindow.package, WinResConfig.BreachUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## BCD/BuffTipsWindow.lua.lua
**Functions:**
- BuffTipsWindow.ReInitData
- BuffTipsWindow.OnInit
- BuffTipsWindow.UpdateInfo
- list.itemRenderer
- BuffTipsWindow.ShowCardBuffInfo
- uis.Main.BuffList.itemRenderer
- BuffTipsWindow.LoadBuff
- buffList.itemRenderer
- BuffTipsWindow.SetController
- BuffTipsWindow.InitBtn
- BuffTipsWindow.OnClose
**Requires:**
- BattleBuffTips_BuffTipsWindowByName
**Snippet:**
```lua
require("BattleBuffTips_BuffTipsWindowByName")
local BuffTipsWindow = {}
local uis, contentPane, closeCallback, buffTipsInfo, curUid, curType, showAnim

function BuffTipsWindow.ReInitData()
end

function BuffTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BuffTipsWindow.package, WinResConfig.BuffTipsWindow.comName, function(com)
    contentPane = com
```

---

## BCD/BuildLockWindow.lua.lua
**Functions:**
- BuildLockWindow.ReInitData
- BuildLockWindow.OnInit
- BuildLockWindow.UpdateInfo
- list.itemRenderer
- BuildLockWindow.UpdateMap
- list.itemRenderer
- BuildLockWindow.InitBtn
- BuildLockWindow.OnClose
**Requires:**
- Arena_BuildLockWindowByName
**Snippet:**
```lua
require("Arena_BuildLockWindowByName")
local BuildLockWindow = {}
local uis, contentPane, buildingListData, mapListData

function BuildLockWindow.ReInitData()
end

function BuildLockWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BuildLockWindow.package, WinResConfig.BuildLockWindow.comName, function(com)
    contentPane = com
```

---

## BCD/BurstTipsWindow.lua.lua
**Functions:**
- BurstTipsWindow.ReInitData
- BurstTipsWindow.OnInit
- BurstTipsWindow.UpdateBurstOperationInfo
- headList.itemRenderer
- cardJobList.itemRenderer
- orderHeadList.itemRenderer
- BurstTipsWindow.AddIntoOrderList
- BurstTipsWindow.RemoveFromOrderList
- BurstTipsWindow.IsInOrder
- BurstTipsWindow.GetBurstOrderByType
- BurstTipsWindow.UpdateCaptainInfo
- headList.itemRenderer
- BurstTipsWindow.UpdateCurCaptainSkillInfo
- BurstTipsWindow.UpdateRuleInfo
- BurstTipsWindow.UpdateInfo
- BurstTipsWindow.ChangeToBurstOperationInfo
- BurstTipsWindow.ChangeToCaptainInfo
- BurstTipsWindow.ChangeToRuleInfo
- BurstTipsWindow.Close
- BurstTipsWindow.InitBtn
- BurstTipsWindow.OnClose
**Requires:**
- Formation_BurstTipsWindowByName
- Formation_BurstLeaderSkillRegionByName
**Snippet:**
```lua
require("Formation_BurstTipsWindowByName")
local BurstTipsWindow = {}
local uis, contentPane

function BurstTipsWindow.ReInitData()
end

local cardUidList, curCaptainCardId, curCaptainCard, curCard2Pos, curBurstOrderSetting, sceneType, skillChoose_uis

function BurstTipsWindow.OnInit(bridgeObj)
```

---

## BCD/CameraUtil.lua.lua
**Functions:**
- CameraUtil.SetCameraActive
- CameraUtil.SetCameraCullingMask
- CameraUtil.SetCameraOrthographicSize
- CameraUtil.SetCameraFOV
- CameraUtil.MoveCamera
- CameraUtil.GoNowCamera
- CameraUtil.TransparentPosition
- CameraUtil.SetCameraBloomActive
**Snippet:**
```lua
local CameraUtil = {}

function CameraUtil.SetCameraActive(camera, active)
  if camera then
    local component = camera:GetComponent(typeof(Camera))
    if component and component.enabled ~= active then
      component.enabled = active
    end
  end
end
```

---

## BCD/CardAttribute.lua.lua
**Functions:**
- CardAttribute.InitAttrEnum
- CardAttribute.GetIdByName
- CardAttribute.GetNameById
**Snippet:**
```lua
CardAttribute = {}
ATTR_ENUM = {
  hp = "hp",
  max_hp = "max_hp",
  atk = "atk",
  def = "def",
  crt = "crt",
  blk = "blk",
  eva = "eva",
  crt_int = "crt_int",
```

---

## BCD/CardAttributeTipsWindow.lua.lua
**Functions:**
- CardAttributeTipsWindow.ReInitData
- CardAttributeTipsWindow.OnInit
- CardAttributeTipsWindow.UpdateInfo
- CardAttributeTipsWindow.InitBtn
- CardAttributeTipsWindow.OnClose
**Requires:**
- CardAttribute_CardAttributeTipsWindowByName
**Snippet:**
```lua
require("CardAttribute_CardAttributeTipsWindowByName")
local CardAttributeTipsWindow = {}
local uis, contentPane, info

function CardAttributeTipsWindow.ReInitData()
end

function CardAttributeTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.CardAttributeTipsWindow.package, WinResConfig.CardAttributeTipsWindow.comName, function(com)
    contentPane = com
```

---

## BCD/CardAttribute_AttributeDes1ByName.lua.lua
**Functions:**
- GetCardAttribute_AttributeDes1Uis
**Requires:**
- CardAttribute_AttributeDes_TipsByName
**Snippet:**
```lua
require("CardAttribute_AttributeDes_TipsByName")

function GetCardAttribute_AttributeDes1Uis(ui)
  local uis = {}
  uis.Tips = GetCardAttribute_AttributeDes_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## BCD/CardAttribute_AttributeDes2ByName.lua.lua
**Functions:**
- GetCardAttribute_AttributeDes2Uis
**Requires:**
- CommonResource_PopupBgByName
- CardAttribute_AttributeDes1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("CardAttribute_AttributeDes1ByName")

function GetCardAttribute_AttributeDes2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.CardScreen1 = GetCardAttribute_AttributeDes1Uis(ui:GetChild("CardScreen1"))
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.root = ui
```

---

## BCD/CardAttribute_AttributeDesWindowByName.lua.lua
**Functions:**
- GetCardAttribute_AttributeDesWindowUis
**Requires:**
- CardAttribute_AttributeDes2ByName
**Snippet:**
```lua
require("CardAttribute_AttributeDes2ByName")

function GetCardAttribute_AttributeDesWindowUis(ui)
  local uis = {}
  uis.Main = GetCardAttribute_AttributeDes2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/CardAttribute_AttributeDes_ChoiceBtnByName.lua.lua
**Functions:**
- GetCardAttribute_AttributeDes_ChoiceBtnUis
**Snippet:**
```lua
function GetCardAttribute_AttributeDes_ChoiceBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/CardAttribute_AttributeDes_NumberRegionByName.lua.lua
**Functions:**
- GetCardAttribute_AttributeDes_NumberRegionUis
**Snippet:**
```lua
function GetCardAttribute_AttributeDes_NumberRegionUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CardAttribute_AttributeDes_TipsByName.lua.lua
**Functions:**
- GetCardAttribute_AttributeDes_TipsUis
**Snippet:**
```lua
function GetCardAttribute_AttributeDes_TipsUis(ui)
  local uis = {}
  
  uis.Type1List = ui:GetChild("Type1List")
  uis.Type2List = ui:GetChild("Type2List")
  uis.CardAttributeList = ui:GetChild("CardAttributeList")
  uis.ChoiceBtn = ui:GetChild("ChoiceBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## BCD/CardAttribute_AttributeDes_Type1BgByName.lua.lua
**Functions:**
- GetCardAttribute_AttributeDes_Type1BgUis
**Snippet:**
```lua
function GetCardAttribute_AttributeDes_Type1BgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CardAttribute_AttributeDes_Type1BtnByName.lua.lua
**Functions:**
- GetCardAttribute_AttributeDes_Type1BtnUis
**Requires:**
- CardAttribute_AttributeDes_Type1BgByName
**Snippet:**
```lua
require("CardAttribute_AttributeDes_Type1BgByName")

function GetCardAttribute_AttributeDes_Type1BtnUis(ui)
  local uis = {}
  uis.Bg = GetCardAttribute_AttributeDes_Type1BgUis(ui:GetChild("Bg"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/CardAttribute_AttributeDes_Type2BtnByName.lua.lua
**Functions:**
- GetCardAttribute_AttributeDes_Type2BtnUis
**Snippet:**
```lua
function GetCardAttribute_AttributeDes_Type2BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/CardAttribute_BadgeCardInfoByName.lua.lua
**Functions:**
- GetCardAttribute_BadgeCardInfoUis
**Requires:**
- CommonResource_PopupBgByName
- CardAttribute_AttributeDes1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("CardAttribute_AttributeDes1ByName")

function GetCardAttribute_BadgeCardInfoUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.CardScreen1 = GetCardAttribute_AttributeDes1Uis(ui:GetChild("CardScreen1"))
  uis.SpclSkillTipsList = ui:GetChild("SpclSkillTipsList")
  uis.SwitchBtn = ui:GetChild("SwitchBtn")
```

---

## BCD/CardAttribute_BadgeCardInfoWindowByName.lua.lua
**Functions:**
- GetCardAttribute_BadgeCardInfoWindowUis
**Requires:**
- CardAttribute_BadgeCardInfoByName
**Snippet:**
```lua
require("CardAttribute_BadgeCardInfoByName")

function GetCardAttribute_BadgeCardInfoWindowUis(ui)
  local uis = {}
  uis.Main = GetCardAttribute_BadgeCardInfoUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/CardAttribute_BadgeSwitchBtnByName.lua.lua
**Functions:**
- GetCardAttribute_BadgeSwitchBtnUis
**Snippet:**
```lua
function GetCardAttribute_BadgeSwitchBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/CardAttribute_CardAttributeAniByName.lua.lua
**Functions:**
- GetCardAttribute_CardAttributeAniUis
**Requires:**
- CardAttribute_CardAttributeByName
**Snippet:**
```lua
require("CardAttribute_CardAttributeByName")

function GetCardAttribute_CardAttributeAniUis(ui)
  local uis = {}
  uis.CardAttribute = GetCardAttribute_CardAttributeUis(ui:GetChild("CardAttribute"))
  uis.root = ui
  return uis
end
```

---

## BCD/CardAttribute_CardAttributeByName.lua.lua
**Functions:**
- GetCardAttribute_CardAttributeUis
**Snippet:**
```lua
function GetCardAttribute_CardAttributeUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.AddNumberTxt = ui:GetChild("AddNumberTxt")
  uis.CardAttributeTipsBtn = ui:GetChild("CardAttributeTipsBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
```

---

## BCD/CardAttribute_CardAttributeTipsBtnByName.lua.lua
**Functions:**
- GetCardAttribute_CardAttributeTipsBtnUis
**Snippet:**
```lua
function GetCardAttribute_CardAttributeTipsBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/CardAttribute_CardAttributeTipsByName.lua.lua
**Functions:**
- GetCardAttribute_CardAttributeTipsUis
**Requires:**
- CardAttribute_CardAttributeTipsWordByName
**Snippet:**
```lua
require("CardAttribute_CardAttributeTipsWordByName")

function GetCardAttribute_CardAttributeTipsUis(ui)
  local uis = {}
  uis.TipsWord = GetCardAttribute_CardAttributeTipsWordUis(ui:GetChild("TipsWord"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.root = ui
  return uis
end
```

---

## BCD/CardAttribute_CardAttributeTipsWindowByName.lua.lua
**Functions:**
- GetCardAttribute_CardAttributeTipsWindowUis
**Requires:**
- CardAttribute_CardAttributeTipsByName
**Snippet:**
```lua
require("CardAttribute_CardAttributeTipsByName")

function GetCardAttribute_CardAttributeTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetCardAttribute_CardAttributeTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/CardAttribute_CardAttributeTipsWordByName.lua.lua
**Functions:**
- GetCardAttribute_CardAttributeTipsWordUis
**Snippet:**
```lua
function GetCardAttribute_CardAttributeTipsWordUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/CardAttribute_DetailsAllSkillByName.lua.lua
**Functions:**
- GetCardAttribute_DetailsAllSkillUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetCardAttribute_DetailsAllSkillUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.SpclSkillTipsList = ui:GetChild("SpclSkillTipsList")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.root = ui
  return uis
```

---

## BCD/CardAttribute_DetailsAllSkillWindowByName.lua.lua
**Functions:**
- GetCardAttribute_DetailsAllSkillWindowUis
**Requires:**
- CardAttribute_DetailsAllSkillByName
**Snippet:**
```lua
require("CardAttribute_DetailsAllSkillByName")

function GetCardAttribute_DetailsAllSkillWindowUis(ui)
  local uis = {}
  uis.Main = GetCardAttribute_DetailsAllSkillUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/CardAttribute_DetailsSkillIconByName.lua.lua
**Functions:**
- GetCardAttribute_DetailsSkillIconUis
**Requires:**
- CommonResource_SkillByName
- CommonResource_SkillDetailsCDByName
- CommonResource_SkillDetailsTagByName
**Snippet:**
```lua
require("CommonResource_SkillByName")
require("CommonResource_SkillDetailsCDByName")
require("CommonResource_SkillDetailsTagByName")

function GetCardAttribute_DetailsSkillIconUis(ui)
  local uis = {}
  uis.Skill = GetCommonResource_SkillUis(ui:GetChild("Skill"))
  uis.SkillDetailsCD = GetCommonResource_SkillDetailsCDUis(ui:GetChild("SkillDetailsCD"))
  uis.SkillDetailsTag = GetCommonResource_SkillDetailsTagUis(ui:GetChild("SkillDetailsTag"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## BCD/CardAttribute_DetailsSkillInfo1ByName.lua.lua
**Functions:**
- GetCardAttribute_DetailsSkillInfo1Uis
**Snippet:**
```lua
function GetCardAttribute_DetailsSkillInfo1Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## BCD/CardAttribute_DetailsSkillInfo2ByName.lua.lua
**Functions:**
- GetCardAttribute_DetailsSkillInfo2Uis
**Snippet:**
```lua
function GetCardAttribute_DetailsSkillInfo2Uis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/CardAttribute_DetailsSkillInfoByName.lua.lua
**Functions:**
- GetCardAttribute_DetailsSkillInfoUis
**Snippet:**
```lua
function GetCardAttribute_DetailsSkillInfoUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.SkillList = ui:GetChild("SkillList")
  uis.root = ui
  return uis
end
```

---

## BCD/CardAttribute_DetailsSkillTipsAniByName.lua.lua
**Functions:**
- GetCardAttribute_DetailsSkillTipsAniUis
**Requires:**
- CardAttribute_SkillLeaderLcokByName
**Snippet:**
```lua
require("CardAttribute_SkillLeaderLcokByName")

function GetCardAttribute_DetailsSkillTipsAniUis(ui)
  local uis = {}
  uis.TipsList = ui:GetChild("TipsList")
  uis.SkillLeaderLcok = GetCardAttribute_SkillLeaderLcokUis(ui:GetChild("SkillLeaderLcok"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/CardAttribute_DetailsSkillTipsByName.lua.lua
**Functions:**
- GetCardAttribute_DetailsSkillTipsUis
**Requires:**
- CardAttribute_DetailsSkillIconByName
- CardAttribute_DetailsSkillInfoByName
- CardAttribute_DetailsSkillInfo2ByName
**Snippet:**
```lua
require("CardAttribute_DetailsSkillIconByName")
require("CardAttribute_DetailsSkillInfoByName")
require("CardAttribute_DetailsSkillInfo2ByName")

function GetCardAttribute_DetailsSkillTipsUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.DetailsSkillIcon = GetCardAttribute_DetailsSkillIconUis(ui:GetChild("DetailsSkillIcon"))
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
```

---

## BCD/CardAttribute_SkillLeaderLcokByName.lua.lua
**Functions:**
- GetCardAttribute_SkillLeaderLcokUis
**Snippet:**
```lua
function GetCardAttribute_SkillLeaderLcokUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/CardBreachUpWindow.lua.lua
**Functions:**
- CardBreachUpWindow.Open
- CardBreachUpWindow.UpdateTextDisplay
- CardBreachUpWindow.ShowBreachLv
- CardBreachUpWindow.BreachInit
- CardBreachUpWindow.InitUpTips
- CardBreachUpWindow.InitBreachUpList
- list.itemRenderer
- CardBreachUpWindow.BreachItem
- CardBreachUpWindow.InitBtn
- CardBreachUpWindow.GetOffsetPosX
- CardBreachUpWindow.HandleMessage
- CardBreachUpWindow.QuitHide
- CardBreachUpWindow.CloseBackShadow
- CardBreachUpWindow.OnClose
**Snippet:**
```lua
CardBreachUpWindow = {}
local uis, uisBack, breachItemData, breachItemNum, breachTipType, isPlay, shadowFashion

function CardBreachUpWindow.Open(_uis, _uisBack)
  uis = _uis
  uisBack = _uisBack
  isPlay = nil
  PlayUITrans(uis.root, "in")
  PlayUITrans(uisBack.root, "in")
  CardBreachUpWindow.UpdateTextDisplay()
```

---

## BCD/CardClothesWindow.lua.lua
**Functions:**
- CardClothesWindow.Open
- CardClothesWindow.UpdateTextDisplay
- CardClothesWindow.SetCardInfo
- CardClothesWindow.SetFashionName
- CardClothesWindow.GetSelectedIndex
- CardClothesWindow.OnInit
- CardClothesWindow.PicListItemRenderer
- CardClothesWindow.SetListSort
- CardClothesWindow.ShowAnimList
- CardClothesWindow.ItemClick
- CardClothesWindow.UpdateModel
- CardClothesWindow.InitBtn
- CardClothesWindow.UpdateCardInfo
- CardClothesWindow.OnClose
**Snippet:**
```lua
CardClothesWindow = {}
local uis, clothesData, currClothesData, wrapper, cardShowObject, curItem, curQbName, listFashion, tempFaceId

function CardClothesWindow.Open(_uis)
  uis = _uis
  PlayUITrans(uis.root, "in")
  CardClothesWindow.UpdateTextDisplay()
  CardClothesWindow.InitBtn()
  curQbName = ""
  CardService.GetAllShowFashionReq(function()
```

---

## BCD/CardData.lua.lua
**Functions:**
- CardData.InitCardJumpSkillData
- CardData.SaveJump
- CardData.RemoveJump
- CardData.CanJump
- CardData.CanOpenBadge
- CardData.SaveDetailsSortData
- CardData.GetDetailsSortData
- CardData.ClearDetailsSortData
- CardData.SaveFashion
- CardData.SaveOneFashion
- CardData.GetAllFashion
- CardData.FashionIsContain
- CardData.CreateClientUnit
- CardData.GetCardSkillFromConfig
- CardData.GetGradeUnlockSkill
- CardData.GetQualityUnlockSkill
- CardData.GetConfigSkill
- CardData.CalculatorCardAttr
- CardData.GetAllSealAttrList
- CardData.GetAllHandBookAttrList
- CardData.CalculatorCardAttrForRogue
- CardData.GetBaseConfig
- CardData.GetCardLevelUpConfig
- CardData.GetCardLevelUpCostConfig
- CardData.GetCardGradeUpConfig
- CardData.GetCardQualityUpConfig
- CardData.GetSkillAddAttrList
- CardData.GetCardDataById
- CardData.GetCardDataByUid
- CardData.GetSortCardList
- CardData.GetSortCardListByStar
- CardData.DefaultSortWithType
- CardData.DefaultSort
- CardData.SortByCardStar
- CardData.GetChoiceListData
- CardData.GetCardStarDebrisNum
- CardData.GetCardListByTeam
- CardData.GetMonsterFashionConfig
- CardData.GetCardGradeLv
- CardData.GetMonsterRankName
- CardData.GetSkillTypeName
- CardData.GetFormatNum
- CardData.GetElementTxt
- CardData.GetOccupationTxt
- CardData.SortTeamCardList
- CardData.GetBadgeAddAttribute
- CardData.GetSealAddAttribute
- CardData.GetLeaderSkillInfo
- CardData.GetLeaderSkillInfoFromSkill2Level
**Snippet:**
```lua
CardData = {tempSkillLv = 0}
CARD_SROT_TYPE = {STRENGRTH = 0, RARITY = 1}
local ownFashions = {}
local tempSortData = {}
local cardJumpSkill = {}

function CardData.InitCardJumpSkillData()
  cardJumpSkill = {}
  local str = PlayerPrefsUtil.GetString(PLAYER_PREF_ENUM.CARD_JUMP)
  if "" ~= str then
```

---

## BCD/CardDetailsWindow.lua.lua
**Functions:**
- CardDetailsWindow.ReInitData
- CardDetailsWindow.OnInit
- CardDetailsWindow.ChangeCard
- CardDetailsWindow.RefreshFashion
- CardDetailsWindow.SetCardSpineAlpha
- CardDetailsWindow.Sort
- CardDetailsWindow.InitCardShow
- list.itemRenderer
- CardDetailsWindow.SwitchDetailsBgEffect
- CardDetailsWindow.InitRedDot
- CardDetailsWindow.InitSet
- CardDetailsWindow.LoadCardTexture
- CardDetailsWindow.UpdateInfo
- StarList.itemRenderer
- CardDetailsWindow.UpdateTextDisplay
- CardDetailsWindow.InitAttribute
- cardAttributeList.itemRenderer
- CardDetailsWindow.RefreshUI
- CardDetailsWindow.ShowUnlockSkill
- skillList.itemRenderer
- CardDetailsWindow.ShowGradeStar
- StarList.itemRenderer
- CardDetailsWindow.RefreshDetailsNum
- CardDetailsWindow.SetCtrIndex
- CardDetailsWindow.InitBtn
- CardDetailsWindow.UpdateFuncUnlock
- CardDetailsWindow.Back
- CardDetailsWindow.ShowCurrencyReturn
- CardDetailsWindow.StopTalk
- CardDetailsWindow.OnClose
- CardDetailsWindow.OnShown
- CardDetailsWindow.ShowLeaderGuide
- CardDetailsWindow.HandleMessage
**Requires:**
- Card_CardDetailsWindowByName
- CardLevelUpWindow
- CardStarUpWindow
- CardSkillUpWindow
- CardStoryWindow
- CardClothesWindow
- CardBreachUpWindow
**Snippet:**
```lua
require("Card_CardDetailsWindowByName")
require("CardLevelUpWindow")
require("CardStarUpWindow")
require("CardSkillUpWindow")
require("CardStoryWindow")
require("CardClothesWindow")
require("CardBreachUpWindow")
local CardDetailsWindow = {}
local uis, contentPane, cardId, previewFashionId, jumpTb
local showIndex = 0
```

---

## BCD/CardLevelUpWindow.lua.lua
**Functions:**
- CardLevelUpWindow.Open
- CardLevelUpWindow.InitData
- CardLevelUpWindow.UpdateTextDisplay
- CardLevelUpWindow.UpdateExpUI
- attributeList.itemRenderer
- CardLevelUpWindow.GetScreenOffset
- CardLevelUpWindow.StopTween
- CardLevelUpWindow.OnInit
- CardLevelUpWindow.InitLongPressData
- CardLevelUpWindow.InitLongPressGesture
- CardLevelUpWindow.UpdateLongPressUI
- attributeList.itemRenderer
- CardLevelUpWindow.GetGesture
- CardLevelUpWindow.RefreshLvUp
- CardLevelUpWindow.HandleMessage
- CardLevelUpWindow.QuitHide
- CardLevelUpWindow.OnClose
**Snippet:**
```lua
CardLevelUpWindow = {}
local uis, levelUpItemID, tweener, firstOpen, tempAttribute
local lvUpItemCost = {}

function CardLevelUpWindow.Open(_uis)
  uis = _uis
  firstOpen = true
  tempAttribute = nil
  PlayUITrans(uis.root, "in")
  CardLevelUpWindow.InitData()
```

---

## BCD/CardListWindow.lua.lua
**Functions:**
- CardListWindow.ReInitData
- CardListWindow.OnInit
- CardListWindow.InitRedDot
- CardListWindow.UpdateTextDisplay
- CardListWindow.SetChooseType
- CardListWindow.UpdateInfo
- CardListWindow.RefreshCardItem
- CardListWindow.GetRank
- CardListWindow.ItemOnClick
- CardListWindow.GetAllRedNum
- CardListWindow.ShowRedDotCtr
- CardListWindow.RefreshUI
- CardListWindow.OpenCollect
- CardListWindow.InitBtn
- CardListWindow.UpdateFuncUnlock
- CardListWindow.InitChoiceData
- CardListWindow.InitCardScreenBtn
- CardListWindow.GetIsChoice
- CardListWindow.RefreshCardScreenUI
- CardListWindow.ChangeList
- CardListWindow.ClearAllNew
- CardListWindow.OnHide
- CardListWindow.OnClose
- CardListWindow.HandleMessage
**Requires:**
- Card_CardListWindowByName
**Snippet:**
```lua
require("Card_CardListWindowByName")
local CardListWindow = {}
local uis, contentPane
local CARD_LAYER_TYPE = {LIST = 0, GRID = 1}
local CHOOSE_TYPE = {
  NONE = 0,
  RED = 1,
  NEW = 2,
  ALL = 3
}
```

---

## BCD/CardMgr.lua.lua
**Functions:**
- CardMgr.InitData
- CardMgr.UpdateMsgData
- CardMgr.GetSkillISUnlock
- CardMgr.IsMaxLevel
- CardMgr.StarIsMax
- CardMgr.SaveFashionId
- CardMgr.GetCardAllFashionId
- CardMgr.GetCardAllFashionIdForChooseHead
- CardMgr.InitCtrIndex
- CardMgr.CardLvIsUp
- CardMgr.CardLvIsEqual
- CardMgr.GetItemIdByStarLv
- CardMgr.ShowSkillTypeInfo
- CardMgr.GetCurSkillLv
- CardMgr.GetPowerRank
- CardMgr.SaveClickedId
- CardMgr.UpdateOneClickedEventId
- CardMgr.SaveEventNewReq
- CardMgr.CheckClicked
- CardMgr.CheckCardClicked
- CardMgr.OnClose
**Snippet:**
```lua
CardMgr = {ctrIndex = 0}

function CardMgr.InitData(cardId)
  CardMgr.cardId = cardId
  CardMgr.cardConfigData = TableData.GetConfig(cardId, "BaseCard")
  CardMgr.cardInfoData = CardData.GetCardDataById(cardId)
  local gradeId = cardId * 1000 + CardMgr.cardInfoData.grade
  CardMgr.CardGradeUpData = TableData.GetConfig(gradeId, "BaseCardGradeUp")
  local lvId = CardMgr.cardConfigData.grow_cost_model_id * 1000 + CardMgr.cardInfoData.level
  local qualityUpId = cardId * 1000 + CardMgr.cardInfoData.quality
```

---

## BCD/CardPlotDetailsWindow.lua.lua
**Functions:**
- CardPlotDetailsWindow.ReInitData
- CardPlotDetailsWindow.OnInit
- CardPlotDetailsWindow.UpdateInfo
- CardPlotDetailsWindow.InitBtn
- CardPlotDetailsWindow.OnClose
**Requires:**
- Abyss_CardPlotDetailsWindowByName
**Snippet:**
```lua
require("Abyss_CardPlotDetailsWindowByName")
local CardPlotDetailsWindow = {}
local uis, contentPane, nodeConfs, cardId, branch
local GetAllNodesByEventId = function(eventId)
  local evtConf = TableData.GetConfig(eventId, "BaseManorEvent")
  local nodeConfTbl = TableData.GetTable("BaseManorNode")
  local result = {}
  for i, v in pairs(nodeConfTbl) do
    if v.group_id == tonumber(evtConf.parameter) then
      table.insert(result, v)
```

---

## BCD/CardPlotEndWindow.lua.lua
**Functions:**
- CardPlotEndWindow.ReInitData
- CardPlotEndWindow.OnInit
- CardPlotEndWindow.UpdateInfo
- CardPlotEndWindow.InitBtn
- CardPlotEndWindow.OnClose
**Requires:**
- Abyss_CardPlotEndWindowByName
**Snippet:**
```lua
require("Abyss_CardPlotEndWindowByName")
local CardPlotEndWindow = {}
local uis, contentPane, nodeConfig

function CardPlotEndWindow.ReInitData()
end

function CardPlotEndWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.CardPlotEndWindow.package, WinResConfig.CardPlotEndWindow.comName, function(com)
    contentPane = com
```

---

## BCD/CardPlotListWindow.lua.lua
**Functions:**
- scheduleList.itemRenderer
- list.itemProvider
- list.itemRenderer
- scheduleList.itemRenderer
- CardPlotListWindow.ReInitData
- CardPlotListWindow.OnInit
- CardPlotListWindow.UpdateInfo
- list.itemRenderer
- CardPlotListWindow.InitBtn
- CardPlotListWindow.OnClose
**Requires:**
- Abyss_CardPlotListWindowByName
- Abyss_CardPlotListTipsAniByName
**Snippet:**
```lua
require("Abyss_CardPlotListWindowByName")
require("Abyss_CardPlotListTipsAniByName")
local CardPlotListWindow = {}
local uis, contentPane, selectedIndex
local Branches = {
  [1] = {
    title = T(20342),
    filter = function(event)
      local config = TableData.GetConfig(event.eventId, "BaseManorEvent")
      if type(config.open_card) == "number" then
```

---

## BCD/CardPlotMainWindow.lua.lua
**Functions:**
- CardPlotMainWindow.ReInitData
- CardPlotMainWindow.OnInit
- CardPlotMainWindow.UpdateInfo
- CardPlotMainWindow.InitBtn
- CardPlotMainWindow.OnClose
**Requires:**
- Abyss_CardPlotMainWindowByName
**Snippet:**
```lua
require("Abyss_CardPlotMainWindowByName")
local CardPlotMainWindow = {}
local uis, contentPane

function CardPlotMainWindow.ReInitData()
end

function CardPlotMainWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.CardPlotMainWindow.package, WinResConfig.CardPlotMainWindow.comName, function(com)
    contentPane = com
```

---

## BCD/CardPlotStartWindow.lua.lua
**Functions:**
- CardPlotStartWindow.ReInitData
- CardPlotStartWindow.OnInit
- CardPlotStartWindow.UpdateInfo
- CardPlotStartWindow.InitBtn
- CardPlotStartWindow.OnClose
**Requires:**
- Abyss_CardPlotStartWindowByName
**Snippet:**
```lua
require("Abyss_CardPlotStartWindowByName")
local CardPlotStartWindow = {}
local uis, contentPane, branch, tweenId
local CloseWindow = function()
  if tweenId then
    LeanTween.cancel(tweenId)
  end
  tweenId = nil
  if branch then
    AbyssExploreMgr.Dispatch(AbyssExploreMsgEnum.BRANCH_START_ACK, branch.eventId)
```

---

## BCD/CardPlotTalkWindow.lua.lua
**Functions:**
- oncontinue
- reader.getOptionDes
- reader.getOptionNext
- CardPlotTalkWindow.ReInitData
- CardPlotTalkWindow.OnInit
- CardPlotTalkWindow.UpdateInfo
- CardPlotTalkWindow.InitBtn
- CardPlotTalkWindow.OnShown
- CardPlotTalkWindow.OnHide
- CardPlotTalkWindow.OnClose
- CardPlotTalkWindow.HandleMessage
**Requires:**
- Abyss_CardPlotTalkWindowByName
**Snippet:**
```lua
require("Abyss_CardPlotTalkWindowByName")
local CardPlotTalkWindow = {}
local uis, contentPane, num, story_reader, eventInfo, callback, init, nodeConfs, reviewMode
local autoPlay = false
local autoPlayInitialInterval = 1
local autoPlayIntervalScale = 0.01
local autoPlayInterval, autoPlayElapse = 0, 0
local skip
local AutoPlay_Update = function()
  if story_reader then
```

---

## BCD/CardPreviewWindow.lua.lua
**Functions:**
- CardPreviewWindow.ReInitData
- CardPreviewWindow.OnInit
- CardPreviewWindow.UpdateInfo
- CardPreviewWindow.GetSkillDesData
- CardPreviewWindow.InitBtn
- CardPreviewWindow.OnClose
**Requires:**
- CardPreview_CardPreviewWindowByName
**Snippet:**
```lua
require("CardPreview_CardPreviewWindowByName")
local CardPreviewWindow = {}
local uis, contentPane, jumpTb, cardId

function CardPreviewWindow.ReInitData()
end

function CardPreviewWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.CardPreviewWindow.package, WinResConfig.CardPreviewWindow.comName, function(com)
    contentPane = com
```

---

## BCD/CardPreview_AttributeByName.lua.lua
**Functions:**
- GetCardPreview_AttributeUis
**Snippet:**
```lua
function GetCardPreview_AttributeUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/CardPreview_BreachSkillByName.lua.lua
**Functions:**
- GetCardPreview_BreachSkillUis
**Snippet:**
```lua
function GetCardPreview_BreachSkillUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/CardPreview_CardHeadBgByName.lua.lua
**Functions:**
- GetCardPreview_CardHeadBgUis
**Snippet:**
```lua
function GetCardPreview_CardHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## BCD/CardPreview_CardHeadByName.lua.lua
**Functions:**
- GetCardPreview_CardHeadUis
**Requires:**
- CardPreview_CardHeadBgByName
**Snippet:**
```lua
require("CardPreview_CardHeadBgByName")

function GetCardPreview_CardHeadUis(ui)
  local uis = {}
  uis.CardHeadBg = GetCardPreview_CardHeadBgUis(ui:GetChild("CardHeadBg"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/CardPreview_CardNameByName.lua.lua
**Functions:**
- GetCardPreview_CardNameUis
**Snippet:**
```lua
function GetCardPreview_CardNameUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/CardPreview_CardPreviewByName.lua.lua
**Functions:**
- GetCardPreview_CardPreviewUis
**Requires:**
- CommonResource_BackGroundByName
- CardPreview_CardShowByName
- CardPreview_CardNameByName
- CardPreview_Info_1ByName
- CardPreview_Info_2ByName
- CardPreview_Info_3ByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("CardPreview_CardShowByName")
require("CardPreview_CardNameByName")
require("CardPreview_Info_1ByName")
require("CardPreview_Info_2ByName")
require("CardPreview_Info_3ByName")
require("CommonResource_CurrencyReturnByName")

function GetCardPreview_CardPreviewUis(ui)
  local uis = {}
```

---

## BCD/CardPreview_CardPreviewWindowByName.lua.lua
**Functions:**
- GetCardPreview_CardPreviewWindowUis
**Requires:**
- CardPreview_CardPreviewByName
**Snippet:**
```lua
require("CardPreview_CardPreviewByName")

function GetCardPreview_CardPreviewWindowUis(ui)
  local uis = {}
  uis.Main = GetCardPreview_CardPreviewUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/CardPreview_CardShowByName.lua.lua
**Functions:**
- GetCardPreview_CardShowUis
**Snippet:**
```lua
function GetCardPreview_CardShowUis(ui)
  local uis = {}
  
  uis.CardShowLoader = ui:GetChild("CardShowLoader")
  uis.CardShowHolder = ui:GetChild("CardShowHolder")
  uis.root = ui
  return uis
end
```

---

## BCD/CardPreview_CardSkillByName.lua.lua
**Functions:**
- GetCardPreview_CardSkillUis
**Requires:**
- CommonResource_SkillByName
**Snippet:**
```lua
require("CommonResource_SkillByName")

function GetCardPreview_CardSkillUis(ui)
  local uis = {}
  uis.Skill = GetCommonResource_SkillUis(ui:GetChild("Skill"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/CardPreview_Info_1ByName.lua.lua
**Functions:**
- GetCardPreview_Info_1Uis
**Requires:**
- CardPreview_CardHeadByName
- CommonResource_OccupationByName
- CommonResource_CardBreachByName
**Snippet:**
```lua
require("CardPreview_CardHeadByName")
require("CommonResource_OccupationByName")
require("CommonResource_CardBreachByName")

function GetCardPreview_Info_1Uis(ui)
  local uis = {}
  uis.CardHead = GetCardPreview_CardHeadUis(ui:GetChild("CardHead"))
  uis.StarList = ui:GetChild("StarList")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.ElementList = ui:GetChild("ElementList")
```

---

## BCD/CardPreview_Info_2ByName.lua.lua
**Functions:**
- GetCardPreview_Info_2Uis
**Snippet:**
```lua
function GetCardPreview_Info_2Uis(ui)
  local uis = {}
  
  uis.BreachSkillList = ui:GetChild("BreachSkillList")
  uis.root = ui
  return uis
end
```

---

## BCD/CardPreview_Info_3ByName.lua.lua
**Functions:**
- GetCardPreview_Info_3Uis
**Snippet:**
```lua
function GetCardPreview_Info_3Uis(ui)
  local uis = {}
  
  uis.CardSkillList = ui:GetChild("CardSkillList")
  uis.root = ui
  return uis
end
```

---

## BCD/CardPreview_LookBtnByName.lua.lua
**Functions:**
- GetCardPreview_LookBtnUis
**Snippet:**
```lua
function GetCardPreview_LookBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/CardPreview_StarByName.lua.lua
**Functions:**
- GetCardPreview_StarUis
**Snippet:**
```lua
function GetCardPreview_StarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CardQuickStarUpSuccessWindow.lua.lua
**Functions:**
- CardQuickStarUpSuccessWindow.ReInitData
- CardQuickStarUpSuccessWindow.OnInit
- CardQuickStarUpSuccessWindow.UpdateInfo
- skillList.itemRenderer
- wordList.itemRenderer
- CardQuickStarUpSuccessWindow.InitBtn
- CardQuickStarUpSuccessWindow.OnClose
**Requires:**
- Card_QuickStarUpSuccessWindowByName
**Snippet:**
```lua
require("Card_QuickStarUpSuccessWindowByName")
local CardQuickStarUpSuccessWindow = {}
local uis, contentPane, lastInfo, callback

function CardQuickStarUpSuccessWindow.ReInitData()
end

function CardQuickStarUpSuccessWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.CardQuickStarUpSuccessWindow.package, WinResConfig.CardQuickStarUpSuccessWindow.comName, function(com)
    contentPane = com
```

---

## BCD/CardQuickStarUpTipsWindow.lua.lua
**Functions:**
- CardQuickStarUpTipsWindow.ReInitData
- CardQuickStarUpTipsWindow.OnInit
- CardQuickStarUpTipsWindow.UpdateInfo
- CardQuickStarUpTipsWindow.InitBtn
- CardQuickStarUpTipsWindow.OnClose
**Requires:**
- Card_QuickStarUpTipsWindowByName
**Snippet:**
```lua
require("Card_QuickStarUpTipsWindowByName")
local CardQuickStarUpTipsWindow = {}
local uis, contentPane

function CardQuickStarUpTipsWindow.ReInitData()
end

function CardQuickStarUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.CardQuickStarUpTipsWindow.package, WinResConfig.CardQuickStarUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## BCD/CardScriptList.lua.lua
**Requires:**
- CardAttribute
- CardData
- CardMgr
- CardService
**Snippet:**
```lua
local require = require
require("CardAttribute")
require("CardData")
require("CardMgr")
if IsBattleServer ~= true then
  require("CardService")
end
```

---

## BCD/CardService.lua.lua
**Functions:**
- CardService.Init
- CardService.SetCardFocusReq
- CardService.SetCardFocusRsp
- CardService.GetCardClickedStoryEventsReq
- CardService.GetCardClickedStoryEventsRsp
- CardService.ClickCardStoryEventReportReq
- CardService.ClickCardStoryEventReportRsp
- CardService.LevelupCardReq
- CardService.QualityUpCardReq
- CardService.LevelupCardRsp
- CardService.QualityUpCardRsp
- CardService.StarUpCardReq
- CardService.GradeUpCardRsp
- CardService.MultiGradeUpCardReq
- CardService.MultiGradeUpCardRsp
- CardService.LevelupCardSkillReq
- CardService.LevelupCardSkillRsp
- CardService.ChangeCardFashionReq
- CardService.ChangeCardFashionRsp
- CardService.GetAllShowFashionReq
- CardService.GetAllShowFashionRsp
- CardService.GetAllCardFashionReq
- CardService.GetAllCardFashionRsp
- CardService.FetchHandBookRewardReq
- CardService.FetchHandBookRewardRsp
- CardService.ActivateHandBookGrowReq
- CardService.ActivateHandBookGrowRsp
**Snippet:**
```lua
CardService = {}

function CardService.Init()
  Net.AddListener(Proto.MsgName.LevelupCardRsp, CardService.LevelupCardRsp)
  Net.AddListener(Proto.MsgName.QualityUpCardRsp, CardService.QualityUpCardRsp)
  Net.AddListener(Proto.MsgName.MultiGradeUpCardRsp, CardService.MultiGradeUpCardRsp)
  Net.AddListener(Proto.MsgName.GradeUpCardRsp, CardService.GradeUpCardRsp)
  Net.AddListener(Proto.MsgName.LevelupCardSkillRsp, CardService.LevelupCardSkillRsp)
  Net.AddListener(Proto.MsgName.ChangeCardFashionRsp, CardService.ChangeCardFashionRsp)
  Net.AddListener(Proto.MsgName.GetAllShowFashionRsp, CardService.GetAllShowFashionRsp)
```

---

## BCD/CardSkillUpWindow.lua.lua
**Functions:**
- CardSkillUpWindow.Open
- CardSkillUpWindow.ShowHeadList
- list.itemRenderer
- CardSkillUpWindow.ShowSkillLv
- CardSkillUpWindow.SetUpEffect
- CardSkillUpWindow.OnInit
- CardSkillUpWindow.CanLvUp
- CardSkillUpWindow.ShowSkillTips
- CardSkillUpWindow.ShowSkillDes
- list.itemRenderer
- CardSkillUpWindow.UpdateInfo
- tips.WordList.itemRenderer
- tips.SkillWordNext.WordNextList.itemRenderer
- tips.StarList.itemRenderer
- CardSkillUpWindow.InitStarAddSkillLv
- CardSkillUpWindow.OpenSkillUpTips
- CardSkillUpWindow.UpdateBtnState
- CardSkillUpWindow.InitBtn
- CardSkillUpWindow.QuitHide
- CardSkillUpWindow.OnClose
**Snippet:**
```lua
CardSkillUpWindow = {}
local uis, starAddLv, selectedBtn, cardId, curSkillName

function CardSkillUpWindow.Open(_uis, _cardId)
  uis = _uis
  cardId = _cardId
  curSkillName = nil
  CardSkillUpWindow.InitBtn()
  UIUtil.SetEffectToUI("Assets/Art/Effects/Prefab/UI_prefab/Roleskills/FX_UI_roleskills.prefab", uis.Effect.EffectHolder)
  CardSkillUpWindow.ShowHeadList()
```

---

## BCD/CardStarUpWindow.lua.lua
**Functions:**
- CardStarUpWindow.Open
- CardStarUpWindow.UpdateTextDisplay
- CardStarUpWindow.ShowStarEffect
- CardStarUpWindow.OnInit
- uis.StarUp1.StarList.itemRenderer
- skillList.itemRenderer
- CardStarUpWindow.ShowCheckEffect
- CardStarUpWindow.RefreshSpendItem
- spendList.itemRenderer
- CardStarUpWindow.SpendItem
- CardStarUpWindow.RefreshStarUp
- CardStarUpWindow.StarIsMax
- CardStarUpWindow.InitBtn
- CardStarUpWindow.RefreshDebrisExchange
- CardStarUpWindow.ShowStarExchangeBtn
- CardStarUpWindow.HandleMessage
- CardStarUpWindow.OnHide
- CardStarUpWindow.OnClose
**Snippet:**
```lua
CardStarUpWindow = {}
local uis, starUpBol, backEffect, checkEffect

function CardStarUpWindow.Open(_uis)
  uis = _uis
  PlayUITrans(uis.root, "in")
  CardStarUpWindow.UpdateTextDisplay()
  CardStarUpWindow.OnInit()
  CardStarUpWindow.InitBtn()
end
```

---

## BCD/CardStoryWindow.lua.lua
**Functions:**
- CardStoryWindow.Open
- CardStoryWindow.UpdateTextDisplay
- CardStoryWindow.InitBaseTips
- CardStoryWindow.InitStoryTips
- CardStoryWindow.InitVoice
- StoryList.itemRenderer
- CardStoryWindow.FormatTime
- CardStoryWindow.ItemClick
- CardStoryWindow.CancelTween
- CardStoryWindow.ShowWordText
- CardStoryWindow.DestroyEffect
- CardStoryWindow.OnInit
- CardStoryWindow.OnClose
**Snippet:**
```lua
CardStoryWindow = {}
local uis, voiceData, lastItem
local tempMoveEffect = {}
local tween, animTween, timeDown, soundEventInstance
local animTime = 0.25
local effectObj = {}

function CardStoryWindow.Open(_uis)
  uis = _uis
  uis.c1Ctr.selectedIndex = 1
```

---

## BCD/Card_20BtnByName.lua.lua
**Functions:**
- GetCard_20BtnUis
**Requires:**
- Card_BgAniByName
**Snippet:**
```lua
require("Card_BgAniByName")

function GetCard_20BtnUis(ui)
  local uis = {}
  uis.BgAni = GetCard_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_45BtnByName.lua.lua
**Functions:**
- GetCard_45BtnUis
**Requires:**
- Card_BgAniByName
**Snippet:**
```lua
require("Card_BgAniByName")

function GetCard_45BtnUis(ui)
  local uis = {}
  uis.BgAni = GetCard_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_70BtnByName.lua.lua
**Functions:**
- GetCard_70BtnUis
**Requires:**
- Card_BgAniByName
**Snippet:**
```lua
require("Card_BgAniByName")

function GetCard_70BtnUis(ui)
  local uis = {}
  uis.BgAni = GetCard_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_AllBtnByName.lua.lua
**Functions:**
- GetCard_AllBtnUis
**Snippet:**
```lua
function GetCard_AllBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_AnBtnByName.lua.lua
**Functions:**
- GetCard_AnBtnUis
**Requires:**
- Card_BgAniByName
**Snippet:**
```lua
require("Card_BgAniByName")

function GetCard_AnBtnUis(ui)
  local uis = {}
  uis.BgAni = GetCard_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_ArrayBtnByName.lua.lua
**Functions:**
- GetCard_ArrayBtnUis
**Snippet:**
```lua
function GetCard_ArrayBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_AttributeAdd1ByName.lua.lua
**Functions:**
- GetCard_AttributeAdd1Uis
**Snippet:**
```lua
function GetCard_AttributeAdd1Uis(ui)
  local uis = {}
  
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_AttributeAddByName.lua.lua
**Functions:**
- GetCard_AttributeAddUis
**Snippet:**
```lua
function GetCard_AttributeAddUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_AttributeDes1ByName.lua.lua
**Functions:**
- GetCard_AttributeDes1Uis
**Snippet:**
```lua
function GetCard_AttributeDes1Uis(ui)
  local uis = {}
  
  uis.CardAttributeList = ui:GetChild("CardAttributeList")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_AttributeDes2ByName.lua.lua
**Functions:**
- GetCard_AttributeDes2Uis
**Requires:**
- CommonResource_PopupBgByName
- Card_AttributeDes1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Card_AttributeDes1ByName")

function GetCard_AttributeDes2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.CardScreen1 = GetCard_AttributeDes1Uis(ui:GetChild("CardScreen1"))
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.root = ui
```

---

## BCD/Card_AttributeDesWindowByName.lua.lua
**Functions:**
- GetCard_AttributeDesWindowUis
**Requires:**
- Card_AttributeDes2ByName
**Snippet:**
```lua
require("Card_AttributeDes2ByName")

function GetCard_AttributeDesWindowUis(ui)
  local uis = {}
  uis.Main = GetCard_AttributeDes2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/Card_BgAniByName.lua.lua
**Functions:**
- GetCard_BgAniUis
**Snippet:**
```lua
function GetCard_BgAniUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/Card_BreachItemBtnAniByName.lua.lua
**Functions:**
- GetCard_BreachItemBtnAniUis
**Snippet:**
```lua
function GetCard_BreachItemBtnAniUis(ui)
  local uis = {}
  
  uis.BreachItemBtn = ui:GetChild("BreachItemBtn")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_BreachItemBtnByName.lua.lua
**Functions:**
- GetCard_BreachItemBtnUis
**Snippet:**
```lua
function GetCard_BreachItemBtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_BreachLookBtnByName.lua.lua
**Functions:**
- GetCard_BreachLookBtnUis
**Snippet:**
```lua
function GetCard_BreachLookBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_BreachSkill1ByName.lua.lua
**Functions:**
- GetCard_BreachSkill1Uis
**Snippet:**
```lua
function GetCard_BreachSkill1Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.LineImage = ui:GetChild("LineImage")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_BreachSkill2ByName.lua.lua
**Functions:**
- GetCard_BreachSkill2Uis
**Snippet:**
```lua
function GetCard_BreachSkill2Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.LineImage = ui:GetChild("LineImage")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_BreachSkill3ByName.lua.lua
**Functions:**
- GetCard_BreachSkill3Uis
**Snippet:**
```lua
function GetCard_BreachSkill3Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.LineImage = ui:GetChild("LineImage")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_BreachSkillByName.lua.lua
**Functions:**
- GetCard_BreachSkillUis
**Snippet:**
```lua
function GetCard_BreachSkillUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.LineImage = ui:GetChild("LineImage")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_BreachUp1ByName.lua.lua
**Functions:**
- GetCard_BreachUp1Uis
**Requires:**
- CommonResource_CardBreachByName
**Snippet:**
```lua
require("CommonResource_CardBreachByName")

function GetCard_BreachUp1Uis(ui)
  local uis = {}
  uis.CardBreach1 = GetCommonResource_CardBreachUis(ui:GetChild("CardBreach1"))
  uis.CardBreach2 = GetCommonResource_CardBreachUis(ui:GetChild("CardBreach2"))
  uis.BreachSkillList = ui:GetChild("BreachSkillList")
  uis.BreachLookBtn = ui:GetChild("BreachLookBtn")
  uis.root = ui
  return uis
```

---

## BCD/Card_BreachUp2ByName.lua.lua
**Functions:**
- GetCard_BreachUp2Uis
**Snippet:**
```lua
function GetCard_BreachUp2Uis(ui)
  local uis = {}
  
  uis.ItemList = ui:GetChild("ItemList")
  uis.BreachUpBtn = ui:GetChild("BreachUpBtn")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_BreachUpBtnByName.lua.lua
**Functions:**
- GetCard_BreachUpBtnUis
**Snippet:**
```lua
function GetCard_BreachUpBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_BreachUpClothesByName.lua.lua
**Functions:**
- GetCard_BreachUpClothesUis
**Snippet:**
```lua
function GetCard_BreachUpClothesUis(ui)
  local uis = {}
  
  uis.LineImage = ui:GetChild("LineImage")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_BreachUpLevelByName.lua.lua
**Functions:**
- GetCard_BreachUpLevelUis
**Snippet:**
```lua
function GetCard_BreachUpLevelUis(ui)
  local uis = {}
  
  uis.LineImage = ui:GetChild("LineImage")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ResultTxt = ui:GetChild("ResultTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_BreachUpSkill1ByName.lua.lua
**Functions:**
- GetCard_BreachUpSkill1Uis
**Snippet:**
```lua
function GetCard_BreachUpSkill1Uis(ui)
  local uis = {}
  
  uis.LineImage = ui:GetChild("LineImage")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ResultTxt = ui:GetChild("ResultTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_BreachUpSkillByName.lua.lua
**Functions:**
- GetCard_BreachUpSkillUis
**Snippet:**
```lua
function GetCard_BreachUpSkillUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.LineImage = ui:GetChild("LineImage")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_BreachUpTipsByName.lua.lua
**Functions:**
- GetCard_BreachUpTipsUis
**Requires:**
- CommonResource_BackGroundByName
- Card_CardShowByName
- Card_EffectBreachByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Card_CardShowByName")
require("Card_EffectBreachByName")

function GetCard_BreachUpTipsUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.CardShow = GetCard_CardShowUis(ui:GetChild("CardShow"))
  uis.BackGroundHolder = ui:GetChild("BackGroundHolder")
  uis.EffectBreach = GetCard_EffectBreachUis(ui:GetChild("EffectBreach"))
```

---

## BCD/Card_BreachUpTipsWindowByName.lua.lua
**Functions:**
- GetCard_BreachUpTipsWindowUis
**Requires:**
- Card_BreachUpTipsByName
**Snippet:**
```lua
require("Card_BreachUpTipsByName")

function GetCard_BreachUpTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetCard_BreachUpTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardAListByName.lua.lua
**Functions:**
- GetCard_CardAListUis
**Snippet:**
```lua
function GetCard_CardAListUis(ui)
  local uis = {}
  
  uis.CardAList = ui:GetChild("CardAList")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardAttributeAniByName.lua.lua
**Functions:**
- GetCard_CardAttributeAniUis
**Requires:**
- Card_CardAttributeByName
**Snippet:**
```lua
require("Card_CardAttributeByName")

function GetCard_CardAttributeAniUis(ui)
  local uis = {}
  uis.CardAttribute = GetCard_CardAttributeUis(ui:GetChild("CardAttribute"))
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardAttributeByName.lua.lua
**Functions:**
- GetCard_CardAttributeUis
**Snippet:**
```lua
function GetCard_CardAttributeUis(ui)
  local uis = {}
  
  uis.ENTxt = ui:GetChild("ENTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardAttributeStripByName.lua.lua
**Functions:**
- GetCard_CardAttributeStripUis
**Snippet:**
```lua
function GetCard_CardAttributeStripUis(ui)
  local uis = {}
  
  uis.CardAttributeList = ui:GetChild("CardAttributeList")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardAttributeTipsBtnByName.lua.lua
**Functions:**
- GetCard_CardAttributeTipsBtnUis
**Snippet:**
```lua
function GetCard_CardAttributeTipsBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardAttributeTipsByName.lua.lua
**Functions:**
- GetCard_CardAttributeTipsUis
**Requires:**
- Card_CardAttributeTipsWordByName
**Snippet:**
```lua
require("Card_CardAttributeTipsWordByName")

function GetCard_CardAttributeTipsUis(ui)
  local uis = {}
  uis.TipsWord = GetCard_CardAttributeTipsWordUis(ui:GetChild("TipsWord"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardAttributeTipsWindowByName.lua.lua
**Functions:**
- GetCard_CardAttributeTipsWindowUis
**Requires:**
- Card_CardAttributeTipsByName
**Snippet:**
```lua
require("Card_CardAttributeTipsByName")

function GetCard_CardAttributeTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetCard_CardAttributeTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardAttributeTipsWordByName.lua.lua
**Functions:**
- GetCard_CardAttributeTipsWordUis
**Snippet:**
```lua
function GetCard_CardAttributeTipsWordUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardBListByName.lua.lua
**Functions:**
- GetCard_CardBListUis
**Snippet:**
```lua
function GetCard_CardBListUis(ui)
  local uis = {}
  
  uis.CardBList = ui:GetChild("CardBList")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardBreachByName.lua.lua
**Functions:**
- GetCard_CardBreachUis
**Snippet:**
```lua
function GetCard_CardBreachUis(ui)
  local uis = {}
  
  uis.BreachHolder = ui:GetChild("BreachHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardBreachUpBackByName.lua.lua
**Functions:**
- GetCard_CardBreachUpBackUis
**Requires:**
- Card_CardShowByName
**Snippet:**
```lua
require("Card_CardShowByName")

function GetCard_CardBreachUpBackUis(ui)
  local uis = {}
  uis.CardShow = GetCard_CardShowUis(ui:GetChild("CardShow"))
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardBreachUpByName.lua.lua
**Functions:**
- GetCard_CardBreachUpUis
**Requires:**
- Card_BreachUp1ByName
- Card_BreachUp2ByName
**Snippet:**
```lua
require("Card_BreachUp1ByName")
require("Card_BreachUp2ByName")

function GetCard_CardBreachUpUis(ui)
  local uis = {}
  uis.BreachUp1 = GetCard_BreachUp1Uis(ui:GetChild("BreachUp1"))
  uis.BreachUp2 = GetCard_BreachUp2Uis(ui:GetChild("BreachUp2"))
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.root = ui
  return uis
```

---

## BCD/Card_CardClothesByName.lua.lua
**Functions:**
- GetCard_CardClothesUis
**Requires:**
- Card_ClothesModularByName
- Card_CardQBByName
- Card_ClothesCardInfoByName
**Snippet:**
```lua
require("Card_ClothesModularByName")
require("Card_CardQBByName")
require("Card_ClothesCardInfoByName")

function GetCard_CardClothesUis(ui)
  local uis = {}
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.ClothesModular = GetCard_ClothesModularUis(ui:GetChild("ClothesModular"))
  uis.CardQB = GetCard_CardQBUis(ui:GetChild("CardQB"))
  uis.CardInfo = GetCard_ClothesCardInfoUis(ui:GetChild("CardInfo"))
```

---

## BCD/Card_CardCollectByName.lua.lua
**Functions:**
- GetCard_CardCollectUis
**Snippet:**
```lua
function GetCard_CardCollectUis(ui)
  local uis = {}
  
  uis.ClearBtn = ui:GetChild("ClearBtn")
  uis.SaveBtn = ui:GetChild("SaveBtn")
  uis.CollectCtr = ui:GetController("Collect")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardCollectClearBtnByName.lua.lua
**Functions:**
- GetCard_CardCollectClearBtnUis
**Snippet:**
```lua
function GetCard_CardCollectClearBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardCollectSaveBtnByName.lua.lua
**Functions:**
- GetCard_CardCollectSaveBtnUis
**Snippet:**
```lua
function GetCard_CardCollectSaveBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardCollectSignByName.lua.lua
**Functions:**
- GetCard_CardCollectSignUis
**Snippet:**
```lua
function GetCard_CardCollectSignUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardDetailsBadgeBtnByName.lua.lua
**Functions:**
- GetCard_CardDetailsBadgeBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetCard_CardDetailsBadgeBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardDetailsByName.lua.lua
**Functions:**
- GetCard_CardDetailsUis
**Requires:**
- CommonResource_BackGroundByName
- Card_OccupationByName
- Card_CardBreachUpBackByName
- Card_CardSkillUpBackByName
- Card_CardShowListAniByName
- Card_DetailsByName
- Card_CardLevelUpByName
- Card_CardSkillUpByName
- Card_CardStarUpByName
- Card_CardStoryByName
- Card_CardClothesByName
- Card_CardBreachUpByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Card_OccupationByName")
require("Card_CardBreachUpBackByName")
require("Card_CardSkillUpBackByName")
require("Card_CardShowListAniByName")
require("Card_DetailsByName")
require("Card_CardLevelUpByName")
require("Card_CardSkillUpByName")
require("Card_CardStarUpByName")
require("Card_CardStoryByName")
```

---

## BCD/Card_CardDetailsWindowByName.lua.lua
**Functions:**
- GetCard_CardDetailsWindowUis
**Requires:**
- Card_CardDetailsByName
**Snippet:**
```lua
require("Card_CardDetailsByName")

function GetCard_CardDetailsWindowUis(ui)
  local uis = {}
  uis.Main = GetCard_CardDetailsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardLevelUpByName.lua.lua
**Functions:**
- GetCard_CardLevelUpUis
**Requires:**
- Card_LevelUp1ByName
- Card_LevelUp3ByName
- Card_LevelUp2ByName
**Snippet:**
```lua
require("Card_LevelUp1ByName")
require("Card_LevelUp3ByName")
require("Card_LevelUp2ByName")

function GetCard_CardLevelUpUis(ui)
  local uis = {}
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.LevelUp1 = GetCard_LevelUp1Uis(ui:GetChild("LevelUp1"))
  uis.LevelUp3 = GetCard_LevelUp3Uis(ui:GetChild("LevelUp3"))
  uis.LevelUp2 = GetCard_LevelUp2Uis(ui:GetChild("LevelUp2"))
```

---

## BCD/Card_CardListBadgeBtnByName.lua.lua
**Functions:**
- GetCard_CardListBadgeBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetCard_CardListBadgeBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
```

---

## BCD/Card_CardListByName.lua.lua
**Functions:**
- GetCard_CardListUis
**Requires:**
- CommonResource_BackGroundByName
- Card_CardBListByName
- Card_CardAListByName
- Card_CardTypeChoiceByName
- Card_CardScreenByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Card_CardBListByName")
require("Card_CardAListByName")
require("Card_CardTypeChoiceByName")
require("Card_CardScreenByName")
require("CommonResource_CurrencyReturnByName")

function GetCard_CardListUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
```

---

## BCD/Card_CardListWindowByName.lua.lua
**Functions:**
- GetCard_CardListWindowUis
**Requires:**
- Card_CardListByName
**Snippet:**
```lua
require("Card_CardListByName")

function GetCard_CardListWindowUis(ui)
  local uis = {}
  uis.Main = GetCard_CardListUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardNameByName.lua.lua
**Functions:**
- GetCard_CardNameUis
**Snippet:**
```lua
function GetCard_CardNameUis(ui)
  local uis = {}
  
  uis.CardNameTxt = ui:GetChild("CardNameTxt")
  uis.CardNameENTxt = ui:GetChild("CardNameENTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SignatureTxt = ui:GetChild("SignatureTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## BCD/Card_CardPicAByName.lua.lua
**Functions:**
- GetCard_CardPicAUis
**Snippet:**
```lua
function GetCard_CardPicAUis(ui)
  local uis = {}
  
  uis.CardPicLoader = ui:GetChild("CardPicLoader")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardPicBByName.lua.lua
**Functions:**
- GetCard_CardPicBUis
**Snippet:**
```lua
function GetCard_CardPicBUis(ui)
  local uis = {}
  
  uis.CardPicLoader = ui:GetChild("CardPicLoader")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardQBByName.lua.lua
**Functions:**
- GetCard_CardQBUis
**Snippet:**
```lua
function GetCard_CardQBUis(ui)
  local uis = {}
  
  uis.QBHolder = ui:GetChild("QBHolder")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardScreenByName.lua.lua
**Functions:**
- GetCard_CardScreenUis
**Requires:**
- Card_GatherChoiceByName
**Snippet:**
```lua
require("Card_GatherChoiceByName")

function GetCard_CardScreenUis(ui)
  local uis = {}
  uis.PopupCloseBtn = ui:GetChild("PopupCloseBtn")
  uis.GatherChoice = GetCard_GatherChoiceUis(ui:GetChild("GatherChoice"))
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardShowByName.lua.lua
**Functions:**
- GetCard_CardShowUis
**Snippet:**
```lua
function GetCard_CardShowUis(ui)
  local uis = {}
  
  uis.CardShowLoader = ui:GetChild("CardShowLoader")
  uis.CardShowHolder = ui:GetChild("CardShowHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardShowListAniByName.lua.lua
**Functions:**
- GetCard_CardShowListAniUis
**Snippet:**
```lua
function GetCard_CardShowListAniUis(ui)
  local uis = {}
  
  uis.CardShowList = ui:GetChild("CardShowList")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardSkillTipsByName.lua.lua
**Functions:**
- GetCard_CardSkillTipsUis
**Requires:**
- Card_SkillTipsRegionByName
**Snippet:**
```lua
require("Card_SkillTipsRegionByName")

function GetCard_CardSkillTipsUis(ui)
  local uis = {}
  uis.SkillTips = GetCard_SkillTipsRegionUis(ui:GetChild("SkillTips"))
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardSkillUpBackByName.lua.lua
**Functions:**
- GetCard_CardSkillUpBackUis
**Snippet:**
```lua
function GetCard_CardSkillUpBackUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardSkillUpBreachByName.lua.lua
**Functions:**
- GetCard_CardSkillUpBreachUis
**Snippet:**
```lua
function GetCard_CardSkillUpBreachUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardSkillUpByName.lua.lua
**Functions:**
- GetCard_CardSkillUpUis
**Requires:**
- Card_CardSkillUpEffectByName
- Card_CardSkillTipsByName
**Snippet:**
```lua
require("Card_CardSkillUpEffectByName")
require("Card_CardSkillTipsByName")

function GetCard_CardSkillUpUis(ui)
  local uis = {}
  uis.Effect = GetCard_CardSkillUpEffectUis(ui:GetChild("Effect"))
  uis.PopupCloseBtn = ui:GetChild("PopupCloseBtn")
  uis.CardSkillTips = GetCard_CardSkillTipsUis(ui:GetChild("CardSkillTips"))
  uis.HeadList = ui:GetChild("HeadList")
  uis.c1Ctr = ui:GetController("c1")
```

---

## BCD/Card_CardSkillUpEffectByName.lua.lua
**Functions:**
- GetCard_CardSkillUpEffectUis
**Snippet:**
```lua
function GetCard_CardSkillUpEffectUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardSkillUpHeadBgByName.lua.lua
**Functions:**
- GetCard_CardSkillUpHeadBgUis
**Snippet:**
```lua
function GetCard_CardSkillUpHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardSkillUpHeadBtnByName.lua.lua
**Functions:**
- GetCard_CardSkillUpHeadBtnUis
**Requires:**
- Card_CardSkillUpHeadBgByName
- Card_CardSkillUpBreachByName
**Snippet:**
```lua
require("Card_CardSkillUpHeadBgByName")
require("Card_CardSkillUpBreachByName")

function GetCard_CardSkillUpHeadBtnUis(ui)
  local uis = {}
  uis.HeadBg = GetCard_CardSkillUpHeadBgUis(ui:GetChild("HeadBg"))
  uis.Breach = GetCard_CardSkillUpBreachUis(ui:GetChild("Breach"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## BCD/Card_CardStarUpByName.lua.lua
**Functions:**
- GetCard_CardStarUpUis
**Requires:**
- CommonResource_BackGroundByName
- Card_StarUp1ByName
- Card_StarUp2ByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Card_StarUp1ByName")
require("Card_StarUp2ByName")

function GetCard_CardStarUpUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.ResourcesHolder = ui:GetChild("ResourcesHolder")
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.StarUp1 = GetCard_StarUp1Uis(ui:GetChild("StarUp1"))
```

---

## BCD/Card_CardStoryByName.lua.lua
**Functions:**
- GetCard_CardStoryUis
**Requires:**
- Card_StoryByName
- Card_VoiceByName
- Card_VoiceWordByName
- Card_CVByName
**Snippet:**
```lua
require("Card_StoryByName")
require("Card_VoiceByName")
require("Card_VoiceWordByName")
require("Card_CVByName")

function GetCard_CardStoryUis(ui)
  local uis = {}
  uis.Story = GetCard_StoryUis(ui:GetChild("Story"))
  uis.Voice = GetCard_VoiceUis(ui:GetChild("Voice"))
  uis.Cultivate1Btn = ui:GetChild("Cultivate1Btn")
```

---

## BCD/Card_CardTipsAByName.lua.lua
**Functions:**
- GetCard_CardTipsAUis
**Requires:**
- Card_CardPicAByName
- Card_QualityByName
- CommonResource_CardBreachByName
- CommonResource_OccupationByName
- CommonResource_RedDotByName
- CommonResource_CardGetNewByName
- CommonResource_StarRedDot1ByName
- Card_CardCollectSignByName
**Snippet:**
```lua
require("Card_CardPicAByName")
require("Card_QualityByName")
require("CommonResource_CardBreachByName")
require("CommonResource_OccupationByName")
require("CommonResource_RedDotByName")
require("CommonResource_CardGetNewByName")
require("CommonResource_StarRedDot1ByName")
require("Card_CardCollectSignByName")

function GetCard_CardTipsAUis(ui)
```

---

## BCD/Card_CardTipsAniAByName.lua.lua
**Functions:**
- GetCard_CardTipsAniAUis
**Requires:**
- Card_CardTipsAByName
**Snippet:**
```lua
require("Card_CardTipsAByName")

function GetCard_CardTipsAniAUis(ui)
  local uis = {}
  uis.CardTips = GetCard_CardTipsAUis(ui:GetChild("CardTips"))
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardTipsAniBByName.lua.lua
**Functions:**
- GetCard_CardTipsAniBUis
**Requires:**
- Card_CardTipsBByName
**Snippet:**
```lua
require("Card_CardTipsBByName")

function GetCard_CardTipsAniBUis(ui)
  local uis = {}
  uis.CardTips = GetCard_CardTipsBUis(ui:GetChild("CardTips"))
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CardTipsBByName.lua.lua
**Functions:**
- GetCard_CardTipsBUis
**Requires:**
- Card_Quality1_1ByName
- Card_CardPicBByName
- Card_Quality1_2ByName
- CommonResource_OccupationByName
- CommonResource_CardBreachByName
- CommonResource_RedDotByName
- CommonResource_StarRedDotByName
- Card_CardCollectSignByName
- CommonResource_CardGetNewByName
**Snippet:**
```lua
require("Card_Quality1_1ByName")
require("Card_CardPicBByName")
require("Card_Quality1_2ByName")
require("CommonResource_OccupationByName")
require("CommonResource_CardBreachByName")
require("CommonResource_RedDotByName")
require("CommonResource_StarRedDotByName")
require("Card_CardCollectSignByName")
require("CommonResource_CardGetNewByName")

```

---

## BCD/Card_CardTypeChoiceByName.lua.lua
**Functions:**
- GetCard_CardTypeChoiceUis
**Requires:**
- Card_CardCollectByName
**Snippet:**
```lua
require("Card_CardCollectByName")

function GetCard_CardTypeChoiceUis(ui)
  local uis = {}
  uis.GreenBtn = ui:GetChild("GreenBtn")
  uis.TeamBtn = ui:GetChild("TeamBtn")
  uis.ArrayBtn = ui:GetChild("ArrayBtn")
  uis.ScreenBtn = ui:GetChild("ScreenBtn")
  uis.CardCollect = GetCard_CardCollectUis(ui:GetChild("CardCollect"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## BCD/Card_ClothesBtnByName.lua.lua
**Functions:**
- GetCard_ClothesBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetCard_ClothesBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_ClothesCardInfoByName.lua.lua
**Functions:**
- GetCard_ClothesCardInfoUis
**Snippet:**
```lua
function GetCard_ClothesCardInfoUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.ClothesNameTxt = ui:GetChild("ClothesNameTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## BCD/Card_ClothesModularByName.lua.lua
**Functions:**
- GetCard_ClothesModularUis
**Requires:**
- Card_ClothesTipsByName
**Snippet:**
```lua
require("Card_ClothesTipsByName")

function GetCard_ClothesModularUis(ui)
  local uis = {}
  uis.PicList = ui:GetChild("PicList")
  uis.UseBtn = ui:GetChild("UseBtn")
  uis.ClothesTips = GetCard_ClothesTipsUis(ui:GetChild("ClothesTips"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## BCD/Card_ClothesPicBtnByName.lua.lua
**Functions:**
- GetCard_ClothesPicBtnUis
**Requires:**
- Card_ClothesPicByName
**Snippet:**
```lua
require("Card_ClothesPicByName")

function GetCard_ClothesPicBtnUis(ui)
  local uis = {}
  uis.ClothesPic = GetCard_ClothesPicUis(ui:GetChild("ClothesPic"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.LineImage = ui:GetChild("LineImage")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
```

---

## BCD/Card_ClothesPicByName.lua.lua
**Functions:**
- GetCard_ClothesPicUis
**Snippet:**
```lua
function GetCard_ClothesPicUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_ClothesTipsByName.lua.lua
**Functions:**
- GetCard_ClothesTipsUis
**Snippet:**
```lua
function GetCard_ClothesTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_CultivateBtnByName.lua.lua
**Functions:**
- GetCard_CultivateBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetCard_CultivateBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## BCD/Card_CVByName.lua.lua
**Functions:**
- GetCard_CVUis
**Snippet:**
```lua
function GetCard_CVUis(ui)
  local uis = {}
  
  uis.CvTxt = ui:GetChild("CvTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_DataModular1ByName.lua.lua
**Functions:**
- GetCard_DataModular1Uis
**Requires:**
- Card_StoryTitleByName
**Snippet:**
```lua
require("Card_StoryTitleByName")

function GetCard_DataModular1Uis(ui)
  local uis = {}
  uis.StoryTitle = GetCard_StoryTitleUis(ui:GetChild("StoryTitle"))
  uis.DataList = ui:GetChild("DataList")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_DataModular2_LockByName.lua.lua
**Functions:**
- GetCard_DataModular2_LockUis
**Requires:**
- Card_StoryTitleByName
**Snippet:**
```lua
require("Card_StoryTitleByName")

function GetCard_DataModular2_LockUis(ui)
  local uis = {}
  uis.StoryTitle = GetCard_StoryTitleUis(ui:GetChild("StoryTitle"))
  uis.root = ui
  return uis
end
```

---

## BCD/Card_DataModular2_OpenByName.lua.lua
**Functions:**
- GetCard_DataModular2_OpenUis
**Requires:**
- Card_StoryTitleByName
**Snippet:**
```lua
require("Card_StoryTitleByName")

function GetCard_DataModular2_OpenUis(ui)
  local uis = {}
  uis.WordList = ui:GetChild("WordList")
  uis.StoryTitle = GetCard_StoryTitleUis(ui:GetChild("StoryTitle"))
  uis.root = ui
  return uis
end
```

---

## BCD/Card_DetailsByName.lua.lua
**Functions:**
- GetCard_DetailsUis
**Requires:**
- Card_OccupationByName
- Card_CardBreachByName
- Card_ExpByName
- Card_CardAttributeStripByName
- Card_CardNameByName
- Card_Label1ByName
**Snippet:**
```lua
require("Card_OccupationByName")
require("Card_CardBreachByName")
require("Card_ExpByName")
require("Card_CardAttributeStripByName")
require("Card_CardNameByName")
require("Card_Label1ByName")

function GetCard_DetailsUis(ui)
  local uis = {}
  uis.EffectHolder = ui:GetChild("EffectHolder")
```

---

## BCD/Card_EffectBreachByName.lua.lua
**Functions:**
- GetCard_EffectBreachUis
**Snippet:**
```lua
function GetCard_EffectBreachUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_ElementByName.lua.lua
**Functions:**
- GetCard_ElementUis
**Snippet:**
```lua
function GetCard_ElementUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_ElementChoiceByName.lua.lua
**Functions:**
- GetCard_ElementChoiceUis
**Snippet:**
```lua
function GetCard_ElementChoiceUis(ui)
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

## BCD/Card_Exp1ProgressBarByName.lua.lua
**Functions:**
- GetCard_Exp1ProgressBarUis
**Snippet:**
```lua
function GetCard_Exp1ProgressBarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/Card_ExpByName.lua.lua
**Functions:**
- GetCard_ExpUis
**Snippet:**
```lua
function GetCard_ExpUis(ui)
  local uis = {}
  
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_ExploreDevelopBtnByName.lua.lua
**Functions:**
- GetCard_ExploreDevelopBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetCard_ExploreDevelopBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
```

---

## BCD/Card_FangYuBtnByName.lua.lua
**Functions:**
- GetCard_FangYuBtnUis
**Requires:**
- Card_BgAniByName
**Snippet:**
```lua
require("Card_BgAniByName")

function GetCard_FangYuBtnUis(ui)
  local uis = {}
  uis.BgAni = GetCard_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_FaShiBtnByName.lua.lua
**Functions:**
- GetCard_FaShiBtnUis
**Requires:**
- Card_BgAniByName
**Snippet:**
```lua
require("Card_BgAniByName")

function GetCard_FaShiBtnUis(ui)
  local uis = {}
  uis.BgAni = GetCard_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_GatherChoiceByName.lua.lua
**Functions:**
- GetCard_GatherChoiceUis
**Requires:**
- Card_ElementChoiceByName
- Card_OccupationChoiceByName
- Card_SkillCDChoiceByName
**Snippet:**
```lua
require("Card_ElementChoiceByName")
require("Card_OccupationChoiceByName")
require("Card_SkillCDChoiceByName")

function GetCard_GatherChoiceUis(ui)
  local uis = {}
  uis.ElementChoice = GetCard_ElementChoiceUis(ui:GetChild("ElementChoice"))
  uis.OccupationChoice = GetCard_OccupationChoiceUis(ui:GetChild("OccupationChoice"))
  uis.SkillCDChoice = GetCard_SkillCDChoiceUis(ui:GetChild("SkillCDChoice"))
  uis.WordTxt = ui:GetChild("WordTxt")
```

---

## BCD/Card_GongJianBtnByName.lua.lua
**Functions:**
- GetCard_GongJianBtnUis
**Requires:**
- Card_BgAniByName
**Snippet:**
```lua
require("Card_BgAniByName")

function GetCard_GongJianBtnUis(ui)
  local uis = {}
  uis.BgAni = GetCard_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_GreenBtnByName.lua.lua
**Functions:**
- GetCard_GreenBtnUis
**Snippet:**
```lua
function GetCard_GreenBtnUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_GuangBtnByName.lua.lua
**Functions:**
- GetCard_GuangBtnUis
**Requires:**
- Card_BgAniByName
**Snippet:**
```lua
require("Card_BgAniByName")

function GetCard_GuangBtnUis(ui)
  local uis = {}
  uis.BgAni = GetCard_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_HuoBtnByName.lua.lua
**Functions:**
- GetCard_HuoBtnUis
**Requires:**
- Card_BgAniByName
**Snippet:**
```lua
require("Card_BgAniByName")

function GetCard_HuoBtnUis(ui)
  local uis = {}
  uis.BgAni = GetCard_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_ItemSpendBtnByName.lua.lua
**Functions:**
- GetCard_ItemSpendBtnUis
**Snippet:**
```lua
function GetCard_ItemSpendBtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_JinZhanBtnByName.lua.lua
**Functions:**
- GetCard_JinZhanBtnUis
**Requires:**
- Card_BgAniByName
**Snippet:**
```lua
require("Card_BgAniByName")

function GetCard_JinZhanBtnUis(ui)
  local uis = {}
  uis.BgAni = GetCard_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_Label1ByName.lua.lua
**Functions:**
- GetCard_Label1Uis
**Snippet:**
```lua
function GetCard_Label1Uis(ui)
  local uis = {}
  
  uis.BadgeBtn = ui:GetChild("BadgeBtn")
  uis.PlotBtn = ui:GetChild("PlotBtn")
  uis.ClothesBtn = ui:GetChild("ClothesBtn")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_LevelUp1ByName.lua.lua
**Functions:**
- GetCard_LevelUp1Uis
**Snippet:**
```lua
function GetCard_LevelUp1Uis(ui)
  local uis = {}
  
  uis.AttributeAddList = ui:GetChild("AttributeAddList")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_LevelUp2ByName.lua.lua
**Functions:**
- GetCard_LevelUp2Uis
**Requires:**
- Card_LevelUp4ByName
**Snippet:**
```lua
require("Card_LevelUp4ByName")

function GetCard_LevelUp2Uis(ui)
  local uis = {}
  uis.ItemSpend1Btn = ui:GetChild("ItemSpend1Btn")
  uis.ItemSpend2Btn = ui:GetChild("ItemSpend2Btn")
  uis.LevelUpBtn = ui:GetChild("LevelUpBtn")
  uis.LevelUp4 = GetCard_LevelUp4Uis(ui:GetChild("LevelUp4"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## BCD/Card_LevelUp3ByName.lua.lua
**Functions:**
- GetCard_LevelUp3Uis
**Snippet:**
```lua
function GetCard_LevelUp3Uis(ui)
  local uis = {}
  
  uis.ExpProgressBar = ui:GetChild("ExpProgressBar")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.LevelAniTxt = ui:GetChild("LevelAniTxt")
  uis.Level1Txt = ui:GetChild("Level1Txt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## BCD/Card_LevelUp4ByName.lua.lua
**Functions:**
- GetCard_LevelUp4Uis
**Snippet:**
```lua
function GetCard_LevelUp4Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_LevelUpBtnByName.lua.lua
**Functions:**
- GetCard_LevelUpBtnUis
**Snippet:**
```lua
function GetCard_LevelUpBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_LevelUpTips1ByName.lua.lua
**Functions:**
- GetCard_LevelUpTips1Uis
**Snippet:**
```lua
function GetCard_LevelUpTips1Uis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_LevelUpTips2ByName.lua.lua
**Functions:**
- GetCard_LevelUpTips2Uis
**Requires:**
- CommonResource_PopupBgByName
- CommonResource_Popup_SByName
- Card_LevelUpTips1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("CommonResource_Popup_SByName")
require("Card_LevelUpTips1ByName")

function GetCard_LevelUpTips2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Popup_S = GetCommonResource_Popup_SUis(ui:GetChild("Popup_S"))
  uis.LevelUpTips1 = GetCard_LevelUpTips1Uis(ui:GetChild("LevelUpTips1"))
```

---

## BCD/Card_LevelUpTipsWindowByName.lua.lua
**Functions:**
- GetCard_LevelUpTipsWindowUis
**Requires:**
- Card_LevelUpTips2ByName
**Snippet:**
```lua
require("Card_LevelUpTips2ByName")

function GetCard_LevelUpTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetCard_LevelUpTips2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/Card_LvUpBtnByName.lua.lua
**Functions:**
- GetCard_LvUpBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetCard_LvUpBtnUis(ui)
  local uis = {}
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
```

---

## BCD/Card_MuBtnByName.lua.lua
**Functions:**
- GetCard_MuBtnUis
**Requires:**
- Card_BgAniByName
**Snippet:**
```lua
require("Card_BgAniByName")

function GetCard_MuBtnUis(ui)
  local uis = {}
  uis.BgAni = GetCard_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_OccupationByName.lua.lua
**Functions:**
- GetCard_OccupationUis
**Snippet:**
```lua
function GetCard_OccupationUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_OccupationChoiceByName.lua.lua
**Functions:**
- GetCard_OccupationChoiceUis
**Snippet:**
```lua
function GetCard_OccupationChoiceUis(ui)
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

## BCD/Card_PlotBtnByName.lua.lua
**Functions:**
- GetCard_PlotBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetCard_PlotBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_Quality1_1ByName.lua.lua
**Functions:**
- GetCard_Quality1_1Uis
**Snippet:**
```lua
function GetCard_Quality1_1Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_Quality1_2ByName.lua.lua
**Functions:**
- GetCard_Quality1_2Uis
**Snippet:**
```lua
function GetCard_Quality1_2Uis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_QualityByName.lua.lua
**Functions:**
- GetCard_QualityUis
**Snippet:**
```lua
function GetCard_QualityUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_QuickStarUpBtnByName.lua.lua
**Functions:**
- GetCard_QuickStarUpBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetCard_QuickStarUpBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_QuickStarUpInfoByName.lua.lua
**Functions:**
- GetCard_QuickStarUpInfoUis
**Snippet:**
```lua
function GetCard_QuickStarUpInfoUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.OpenTxt = ui:GetChild("OpenTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
```

---

## BCD/Card_QuickStarUpSuccessByName.lua.lua
**Functions:**
- GetCard_QuickStarUpSuccessUis
**Requires:**
- CommonResource_BackGroundByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")

function GetCard_QuickStarUpSuccessUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.InfoList = ui:GetChild("InfoList")
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.root = ui
```

---

## BCD/Card_QuickStarUpSuccessWindowByName.lua.lua
**Functions:**
- GetCard_QuickStarUpSuccessWindowUis
**Requires:**
- Card_QuickStarUpSuccessByName
**Snippet:**
```lua
require("Card_QuickStarUpSuccessByName")

function GetCard_QuickStarUpSuccessWindowUis(ui)
  local uis = {}
  uis.Main = GetCard_QuickStarUpSuccessUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/Card_QuickStarUpTips1ByName.lua.lua
**Functions:**
- GetCard_QuickStarUpTips1Uis
**Snippet:**
```lua
function GetCard_QuickStarUpTips1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Star1List = ui:GetChild("Star1List")
  uis.Star2List = ui:GetChild("Star2List")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_QuickStarUpTips2ByName.lua.lua
**Functions:**
- GetCard_QuickStarUpTips2Uis
**Requires:**
- CommonResource_PopupBgByName
- CommonResource_Popup_OpalByName
- Card_QuickStarUpTips1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("CommonResource_Popup_OpalByName")
require("Card_QuickStarUpTips1ByName")

function GetCard_QuickStarUpTips2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Popup_Opal = GetCommonResource_Popup_OpalUis(ui:GetChild("Popup_Opal"))
  uis.Tips1 = GetCard_QuickStarUpTips1Uis(ui:GetChild("Tips1"))
```

---

## BCD/Card_QuickStarUpTipsWindowByName.lua.lua
**Functions:**
- GetCard_QuickStarUpTipsWindowUis
**Requires:**
- Card_QuickStarUpTips2ByName
**Snippet:**
```lua
require("Card_QuickStarUpTips2ByName")

function GetCard_QuickStarUpTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetCard_QuickStarUpTips2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/Card_RarityBtnByName.lua.lua
**Functions:**
- GetCard_RarityBtnUis
**Snippet:**
```lua
function GetCard_RarityBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_ScreenBtnByName.lua.lua
**Functions:**
- GetCard_ScreenBtnUis
**Snippet:**
```lua
function GetCard_ScreenBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_ShuiBtnByName.lua.lua
**Functions:**
- GetCard_ShuiBtnUis
**Requires:**
- Card_BgAniByName
**Snippet:**
```lua
require("Card_BgAniByName")

function GetCard_ShuiBtnUis(ui)
  local uis = {}
  uis.BgAni = GetCard_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_SkillAllLookBtnByName.lua.lua
**Functions:**
- GetCard_SkillAllLookBtnUis
**Snippet:**
```lua
function GetCard_SkillAllLookBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_SkillBtnByName.lua.lua
**Functions:**
- GetCard_SkillBtnUis
**Requires:**
- CommonResource_SkillByName
- CommonResource_SkillDetailsCDByName
- CommonResource_SkillDetailsTag1ByName
- CommonResource_SkillLockByName
**Snippet:**
```lua
require("CommonResource_SkillByName")
require("CommonResource_SkillDetailsCDByName")
require("CommonResource_SkillDetailsTag1ByName")
require("CommonResource_SkillLockByName")

function GetCard_SkillBtnUis(ui)
  local uis = {}
  uis.Skill = GetCommonResource_SkillUis(ui:GetChild("Skill"))
  uis.SkillDetailsCD = GetCommonResource_SkillDetailsCDUis(ui:GetChild("SkillDetailsCD"))
  uis.SkillDetailsTag = GetCommonResource_SkillDetailsTag1Uis(ui:GetChild("SkillDetailsTag"))
```

---

## BCD/Card_SkillCDChoiceByName.lua.lua
**Functions:**
- GetCard_SkillCDChoiceUis
**Snippet:**
```lua
function GetCard_SkillCDChoiceUis(ui)
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

## BCD/Card_SkillCDInfoByName.lua.lua
**Functions:**
- GetCard_SkillCDInfoUis
**Snippet:**
```lua
function GetCard_SkillCDInfoUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_SkillInfo1ByName.lua.lua
**Functions:**
- GetCard_SkillInfo1Uis
**Snippet:**
```lua
function GetCard_SkillInfo1Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_SkillInfoAniByName.lua.lua
**Functions:**
- GetCard_SkillInfoAniUis
**Snippet:**
```lua
function GetCard_SkillInfoAniUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.OpenTxt = ui:GetChild("OpenTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_SkillInfoAniWordByName.lua.lua
**Functions:**
- GetCard_SkillInfoAniWordUis
**Snippet:**
```lua
function GetCard_SkillInfoAniWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_SkillInfoByName.lua.lua
**Functions:**
- GetCard_SkillInfoUis
**Snippet:**
```lua
function GetCard_SkillInfoUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.SkillList = ui:GetChild("SkillList")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_SkillItemBtnByName.lua.lua
**Functions:**
- GetCard_SkillItemBtnUis
**Snippet:**
```lua
function GetCard_SkillItemBtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_SkillLockByName.lua.lua
**Functions:**
- GetCard_SkillLockUis
**Snippet:**
```lua
function GetCard_SkillLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_SkillLockTipsByName.lua.lua
**Functions:**
- GetCard_SkillLockTipsUis
**Snippet:**
```lua
function GetCard_SkillLockTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_SkillMaxByName.lua.lua
**Functions:**
- GetCard_SkillMaxUis
**Snippet:**
```lua
function GetCard_SkillMaxUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_SkillTipsNextBtnByName.lua.lua
**Functions:**
- GetCard_SkillTipsNextBtnUis
**Snippet:**
```lua
function GetCard_SkillTipsNextBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_SkillTipsRegionByName.lua.lua
**Functions:**
- GetCard_SkillTipsRegionUis
**Requires:**
- Card_SkillLockByName
- Card_SkillMaxByName
- Card_SkillWordNextByName
- Card_SkillCDInfoByName
**Snippet:**
```lua
require("Card_SkillLockByName")
require("Card_SkillMaxByName")
require("Card_SkillWordNextByName")
require("Card_SkillCDInfoByName")

function GetCard_SkillTipsRegionUis(ui)
  local uis = {}
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
```

---

## BCD/Card_SkillUpBtnByName.lua.lua
**Functions:**
- GetCard_SkillUpBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetCard_SkillUpBtnUis(ui)
  local uis = {}
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
```

---

## BCD/Card_SkillUpIcon1BtnByName.lua.lua
**Functions:**
- GetCard_SkillUpIcon1BtnUis
**Requires:**
- Card_SkillUpIconType1ByName
**Snippet:**
```lua
require("Card_SkillUpIconType1ByName")

function GetCard_SkillUpIcon1BtnUis(ui)
  local uis = {}
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Type = GetCard_SkillUpIconType1Uis(ui:GetChild("Type"))
```

---

## BCD/Card_SkillUpIcon2BtnByName.lua.lua
**Functions:**
- GetCard_SkillUpIcon2BtnUis
**Requires:**
- Card_SkillUpIconType2ByName
**Snippet:**
```lua
require("Card_SkillUpIconType2ByName")

function GetCard_SkillUpIcon2BtnUis(ui)
  local uis = {}
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Type = GetCard_SkillUpIconType2Uis(ui:GetChild("Type"))
  uis.buttonCtr = ui:GetController("button")
```

---

## BCD/Card_SkillUpIconType1ByName.lua.lua
**Functions:**
- GetCard_SkillUpIconType1Uis
**Snippet:**
```lua
function GetCard_SkillUpIconType1Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_SkillUpIconType2ByName.lua.lua
**Functions:**
- GetCard_SkillUpIconType2Uis
**Snippet:**
```lua
function GetCard_SkillUpIconType2Uis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_SkillUpSuccess1ByName.lua.lua
**Functions:**
- GetCard_SkillUpSuccess1Uis
**Snippet:**
```lua
function GetCard_SkillUpSuccess1Uis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_SkillUpSuccess2ByName.lua.lua
**Functions:**
- GetCard_SkillUpSuccess2Uis
**Requires:**
- CommonResource_PopupBgByName
- Card_SkillUpSuccessBgByName
- Card_SkillUpSuccess1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Card_SkillUpSuccessBgByName")
require("Card_SkillUpSuccess1ByName")

function GetCard_SkillUpSuccess2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Popup_S = GetCard_SkillUpSuccessBgUis(ui:GetChild("Popup_S"))
  uis.SkillUpSuccess1 = GetCard_SkillUpSuccess1Uis(ui:GetChild("SkillUpSuccess1"))
```

---

## BCD/Card_SkillUpSuccessBgByName.lua.lua
**Functions:**
- GetCard_SkillUpSuccessBgUis
**Snippet:**
```lua
function GetCard_SkillUpSuccessBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/Card_SkillUpSuccessWindowByName.lua.lua
**Functions:**
- GetCard_SkillUpSuccessWindowUis
**Requires:**
- Card_SkillUpSuccess2ByName
**Snippet:**
```lua
require("Card_SkillUpSuccess2ByName")

function GetCard_SkillUpSuccessWindowUis(ui)
  local uis = {}
  uis.Main = GetCard_SkillUpSuccess2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/Card_SkillUpSureBtnByName.lua.lua
**Functions:**
- GetCard_SkillUpSureBtnUis
**Snippet:**
```lua
function GetCard_SkillUpSureBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_SkillWordByName.lua.lua
**Functions:**
- GetCard_SkillWordUis
**Requires:**
- Card_SkillInfoByName
**Snippet:**
```lua
require("Card_SkillInfoByName")

function GetCard_SkillWordUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SkillInfo = GetCard_SkillInfoUis(ui:GetChild("SkillInfo"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_SkillWordNextByName.lua.lua
**Functions:**
- GetCard_SkillWordNextUis
**Snippet:**
```lua
function GetCard_SkillWordNextUis(ui)
  local uis = {}
  
  uis.LevelNextTxt = ui:GetChild("LevelNextTxt")
  uis.WordNextList = ui:GetChild("WordNextList")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_SpecialBtnByName.lua.lua
**Functions:**
- GetCard_SpecialBtnUis
**Requires:**
- Card_BgAniByName
**Snippet:**
```lua
require("Card_BgAniByName")

function GetCard_SpecialBtnUis(ui)
  local uis = {}
  uis.BgAni = GetCard_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_SpecialStarByName.lua.lua
**Functions:**
- GetCard_SpecialStarUis
**Snippet:**
```lua
function GetCard_SpecialStarUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_StarExchangeBtnByName.lua.lua
**Functions:**
- GetCard_StarExchangeBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetCard_StarExchangeBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_StarSkillBtnByName.lua.lua
**Functions:**
- GetCard_StarSkillBtnUis
**Requires:**
- Card_SkillLockTipsByName
**Snippet:**
```lua
require("Card_SkillLockTipsByName")

function GetCard_StarSkillBtnUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.Lock = GetCard_SkillLockTipsUis(ui:GetChild("Lock"))
  uis.buttonCtr = ui:GetController("button")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## BCD/Card_StarUp1ByName.lua.lua
**Functions:**
- GetCard_StarUp1Uis
**Snippet:**
```lua
function GetCard_StarUp1Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.StarList = ui:GetChild("StarList")
  uis.SkillList = ui:GetChild("SkillList")
  uis.SkillAllLookBtn = ui:GetChild("SkillAllLookBtn")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_StarUp2ByName.lua.lua
**Functions:**
- GetCard_StarUp2Uis
**Snippet:**
```lua
function GetCard_StarUp2Uis(ui)
  local uis = {}
  
  uis.StarList = ui:GetChild("StarList")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_StarUpBtnByName.lua.lua
**Functions:**
- GetCard_StarUpBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetCard_StarUpBtnUis(ui)
  local uis = {}
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
```

---

## BCD/Card_StarUpTipsByName.lua.lua
**Functions:**
- GetCard_StarUpTipsUis
**Requires:**
- CommonResource_BackGroundByName
- Card_CardShowByName
- Card_SkillInfoAniByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Card_CardShowByName")
require("Card_SkillInfoAniByName")

function GetCard_StarUpTipsUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.CardShow = GetCard_CardShowUis(ui:GetChild("CardShow"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
```

---

## BCD/Card_StarUpTipsWindowByName.lua.lua
**Functions:**
- GetCard_StarUpTipsWindowUis
**Requires:**
- Card_StarUpTipsByName
**Snippet:**
```lua
require("Card_StarUpTipsByName")

function GetCard_StarUpTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetCard_StarUpTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/Card_StoryByName.lua.lua
**Functions:**
- GetCard_StoryUis
**Snippet:**
```lua
function GetCard_StoryUis(ui)
  local uis = {}
  
  uis.StoryList = ui:GetChild("StoryList")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_StoryData1ByName.lua.lua
**Functions:**
- GetCard_StoryData1Uis
**Snippet:**
```lua
function GetCard_StoryData1Uis(ui)
  local uis = {}
  
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_StoryTitleByName.lua.lua
**Functions:**
- GetCard_StoryTitleUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetCard_StoryTitleUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## BCD/Card_StoryWordByName.lua.lua
**Functions:**
- GetCard_StoryWordUis
**Snippet:**
```lua
function GetCard_StoryWordUis(ui)
  local uis = {}
  
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_StrengthBtnByName.lua.lua
**Functions:**
- GetCard_StrengthBtnUis
**Snippet:**
```lua
function GetCard_StrengthBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_TeamBtnByName.lua.lua
**Functions:**
- GetCard_TeamBtnUis
**Snippet:**
```lua
function GetCard_TeamBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_TuXiBtnByName.lua.lua
**Functions:**
- GetCard_TuXiBtnUis
**Requires:**
- Card_BgAniByName
**Snippet:**
```lua
require("Card_BgAniByName")

function GetCard_TuXiBtnUis(ui)
  local uis = {}
  uis.BgAni = GetCard_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_VoiceByName.lua.lua
**Functions:**
- GetCard_VoiceUis
**Requires:**
- Card_VoiceTitleByName
- Card_VoiceListByName
**Snippet:**
```lua
require("Card_VoiceTitleByName")
require("Card_VoiceListByName")

function GetCard_VoiceUis(ui)
  local uis = {}
  uis.StoryTitle = GetCard_VoiceTitleUis(ui:GetChild("StoryTitle"))
  uis.VoiceList = GetCard_VoiceListUis(ui:GetChild("VoiceList"))
  uis.root = ui
  return uis
end
```

---

## BCD/Card_VoiceDataBtnByName.lua.lua
**Functions:**
- GetCard_VoiceDataBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetCard_VoiceDataBtnUis(ui)
  local uis = {}
  uis.VoicProgressBar = ui:GetChild("VoicProgressBar")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
```

---

## BCD/Card_VoiceListByName.lua.lua
**Functions:**
- GetCard_VoiceListUis
**Snippet:**
```lua
function GetCard_VoiceListUis(ui)
  local uis = {}
  
  uis.StoryList = ui:GetChild("StoryList")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_VoiceTitleByName.lua.lua
**Functions:**
- GetCard_VoiceTitleUis
**Snippet:**
```lua
function GetCard_VoiceTitleUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_VoiceWordByName.lua.lua
**Functions:**
- GetCard_VoiceWordUis
**Snippet:**
```lua
function GetCard_VoiceWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/Card_VoicProgressBarByName.lua.lua
**Functions:**
- GetCard_VoicProgressBarUis
**Requires:**
- Card_VoicProgressFillByName
**Snippet:**
```lua
require("Card_VoicProgressFillByName")

function GetCard_VoicProgressBarUis(ui)
  local uis = {}
  uis.bar = GetCard_VoicProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## BCD/Card_VoicProgressFillByName.lua.lua
**Functions:**
- GetCard_VoicProgressFillUis
**Snippet:**
```lua
function GetCard_VoicProgressFillUis(ui)
  local uis = {}
  
  uis.CardShowHolder = ui:GetChild("CardShowHolder")
  uis.root = ui
  return uis
end
```

---

## BCD/CarnivalData.lua.lua
**Functions:**
- CarnivalData.GetRefreshStamp
- CarnivalData.RefreshRefreshStamp
- CarnivalData.SaveHomeTaskId
- CarnivalData.GetHomeTaskId
- CarnivalData.GetEnterActivityId
- CarnivalData.SaveEnterActivityId
- CarnivalData.GetHomeShowTask
- CarnivalData.ActivityIsUnlock
- CarnivalData.InitialSignIsUnlock
- CarnivalData.SignIsShowHome
- CarnivalData.CarnivalIsUnlock
- CarnivalData.BiographyIsUnlock
- CarnivalData.LvGiftIsUnlock
- CarnivalData.GetLvGiftData
- CarnivalData.GetCarnivalTargetData
- CarnivalData.GetCarnivalTotalDay
- CarnivalData.GetCarnivalCurrentDay
- CarnivalData.ShowHomeCarnivalTarget
- CarnivalData.ShowHomeLvGift
**Snippet:**
```lua
CarnivalData = {info = nil}
local homeTaskId = 0
local refreshStamp = 0
local enterActivityId = 0

function CarnivalData.GetRefreshStamp()
  return refreshStamp
end

function CarnivalData.RefreshRefreshStamp(time)
```

---

## BCD/CarnivalRewardWindow.lua.lua
**Functions:**
- CarnivalRewardWindow.OnInit
- CarnivalRewardWindow.Init
- list.itemRenderer
- CarnivalRewardWindow.InitBtn
- CarnivalRewardWindow.HandleMessage
- CarnivalRewardWindow.OnClose
**Requires:**
- InitialCarnival_RewardListWindowByName
**Snippet:**
```lua
require("InitialCarnival_RewardListWindowByName")
local CarnivalRewardWindow = {}
local uis, contentPane, carnivalData

function CarnivalRewardWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.CarnivalRewardWindow.package, WinResConfig.CarnivalRewardWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetInitialCarnival_RewardListWindowUis(contentPane)
    CarnivalRewardWindow.Init()
```

---

## BCD/CarnivalScriptList.lua.lua
**Requires:**
- CarnivalData
- CarnivalService
**Snippet:**
```lua
local require = require
require("CarnivalData")
require("CarnivalService")
```

---

## BCD/CarnivalService.lua.lua
**Functions:**
- CarnivalService.Init
- CarnivalService.GetTaskRefreshStampReq
- CarnivalService.GetTaskRefreshStampRsp
- CarnivalService.GetCarnivalInfoReq
- CarnivalService.GetCarnivalInfoRsp
- CarnivalService.CarnivalGetRewardReq
- CarnivalService.CarnivalGetRewardRsp
**Snippet:**
```lua
CarnivalService = {}

function CarnivalService.Init()
  Net.AddListener(Proto.MsgName.GetCarnivalInfoRsp, CarnivalService.GetCarnivalInfoRsp)
  Net.AddListener(Proto.MsgName.CarnivalGetRewardRsp, CarnivalService.CarnivalGetRewardRsp)
  Net.AddListener(Proto.MsgName.GetTaskRefreshStampRsp, CarnivalService.GetTaskRefreshStampRsp)
end

function CarnivalService.GetTaskRefreshStampReq(rspCallBack)
  local msg = {}
```

---

## BCD/CarnivalWindow.lua.lua
**Functions:**
- CarnivalWindow.OnInit
- uis.Main.ActivityBtnList.itemRenderer
- CarnivalWindow.ActivityOnClick
- CarnivalWindow.ContentOnShow
- CarnivalWindow.ContentOnHide
- CarnivalWindow.GetCom
- CarnivalWindow.GetShowActivityData
- CarnivalWindow.ClearPackage
- CarnivalWindow.InitBtn
- CarnivalWindow.HandleMessage
- CarnivalWindow.OnClose
**Requires:**
- Carnival_ActivityWindowByName
- InitialCarnivalWindow
- InitialSignWindow
- DailyTaskWindow
- BiographyWindow
- InitialLevelRewardWindow
- InitialEnergyWindow
**Snippet:**
```lua
require("Carnival_ActivityWindowByName")
require("InitialCarnivalWindow")
require("InitialSignWindow")
require("DailyTaskWindow")
require("BiographyWindow")
require("InitialLevelRewardWindow")
require("InitialEnergyWindow")
local CarnivalWindow = {}
local uis, contentPane, tempLoadPackageName
local ActivityName = {
```

---

## BCD/Carnival_ActivityBtnByName.lua.lua
**Functions:**
- GetCarnival_ActivityBtnUis
**Requires:**
- Carnival_RepeatTipsByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("Carnival_RepeatTipsByName")
require("CommonResource_RedDotByName")

function GetCarnival_ActivityBtnUis(ui)
  local uis = {}
  uis.RepeatTips = GetCarnival_RepeatTipsUis(ui:GetChild("RepeatTips"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
```

---

## BCD/Carnival_ActivityByName.lua.lua
**Functions:**
- GetCarnival_ActivityUis
**Requires:**
- Carnival_ActivityContentByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("Carnival_ActivityContentByName")
require("CommonResource_CurrencyReturnByName")

function GetCarnival_ActivityUis(ui)
  local uis = {}
  uis.ActivityContent = GetCarnival_ActivityContentUis(ui:GetChild("ActivityContent"))
  uis.ActivityBtnList = ui:GetChild("ActivityBtnList")
  uis.CurrencyReturn = GetCommonResource_CurrencyReturnUis(ui:GetChild("CurrencyReturn"))
  uis.root = ui
  return uis
```

---

## BCD/Carnival_ActivityContentByName.lua.lua
**Functions:**
- GetCarnival_ActivityContentUis
**Snippet:**
```lua
function GetCarnival_ActivityContentUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/Carnival_ActivityWindowByName.lua.lua
**Functions:**
- GetCarnival_ActivityWindowUis
**Requires:**
- Carnival_ActivityByName
**Snippet:**
```lua
require("Carnival_ActivityByName")

function GetCarnival_ActivityWindowUis(ui)
  local uis = {}
  uis.Main = GetCarnival_ActivityUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/Carnival_RepeatTipsByName.lua.lua
**Functions:**
- GetCarnival_RepeatTipsUis
**Snippet:**
```lua
function GetCarnival_RepeatTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/CasketHomeWindow.lua.lua
**Functions:**
- CasketHomeWindow.ReInitData
- CasketHomeWindow.OnInit
- CasketHomeWindow.ShowState
- CasketHomeWindow.UpdateInfo
- list.itemRenderer
- CasketHomeWindow.InitBtn
- CasketHomeWindow.OnClose
**Requires:**
- ActivityCasketHome_CasketHomeWindowByName
**Snippet:**
```lua
require("ActivityCasketHome_CasketHomeWindowByName")
local CasketHomeWindow = {}
local uis, contentPane

function CasketHomeWindow.ReInitData()
end

function CasketHomeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.CasketHomeWindow.package, WinResConfig.CasketHomeWindow.comName, function(com)
    contentPane = com
```

---

## BCD/CGShowWindow.lua.lua
**Functions:**
- CGShowWindow.OnInit
- CGShowWindow.Init
- CGShowWindow.ShowUI
- CGShowWindow.HandleMessage
- CGShowWindow.OnClose
**Requires:**
- Story_CGShowWindowByName
**Snippet:**
```lua
require("Story_CGShowWindowByName")
local CGShowWindow = {}
local uis, contentPane, cgId, show

function CGShowWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.CGShowWindow.package, WinResConfig.CGShowWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetStory_CGShowWindowUis(contentPane)
    cgId = bridgeObj.argTable[1]
```

---

## BCD/ChatData.lua.lua
**Functions:**
- ChatData.InitChatData
- ChatData.ClearCacheMsg
- ChatData.RemoveTargetFromUnreadList
- ChatData.SaveTargetFromUnreadList
- ChatData.InitMessage
- ChatData.DealNewMessageNotify
- ChatData.UpdateSyncMessage
- ChatData.SaveFlushMsgTime
- ChatData.IsMessageCached
- ChatData.CacheMessage
- ChatData.UpdatePrivateMsg
- ChatData.CachePrivateMsg
- ChatData.GetPrivateMsg
- ChatData.GetCacheChatMsg
- ChatData.SetWorldLineList
- ChatData.GetWorldLineInfo
- ChatData.GetAllWorldLineList
- ChatData.SetSelfLineInfo
- ChatData.GetSelfLineInfo
- ChatData.GetSessionId
- ChatData.UpdateSenderInfos
- ChatData.GetSenderInfo
- ChatData.GetNewestWorldMessage
- ChatData.IsSelfMsg
- ChatData.SetSelectChannel
- ChatData.GetSelectChannel
- ChatData.GetLastChannel
- ChatData.GetSyncKey
- ChatData.SetSyncKey
- ChatData.CreateSystemMsg
- ChatData.GetSystemMsgId
- ChatData.SetPrivateTargetList
- ChatData.GetPrivateTargetList
- ChatData.UpdatePrivateTarget
- ChatData.RemovePrivateTarget
- ChatData.SetCurPrivateTargetUin
- ChatData.GetCurPrivateTargetUin
- ChatData.GetCurPrivateTarget
- ChatData.SetLatestEmojiList
- ChatData.GetLatestEmojiList
- ChatData.UpdateLatestEmoji
- ChatData.InitEmoji
- ChatData.GetCurGroupEmoji
- ChatData.SetGuildMemberList
- ChatData.GetGuildMemberList
- ChatData.SetChatState
- ChatData.GetChatState
- ChatData.GetChatStateByChannel
**Snippet:**
```lua
ChatData = {}

function ChatData.InitChatData()
  ChatData.lastChannel = nil
  ChatData.selectChannel = nil
  ChatData.msgInited = false
  ChatData.cacheChatMsg = {}
  ChatData.cachePrivateMsg = {}
  ChatData.cacheSyncKey = {}
  ChatData.cacheSenderInfos = {}
```

---

## BCD/ChatMgr.lua.lua
**Functions:**
- ChatMgr.FriendChatEnable
- ChatMgr.GuildChannelEnable
- ChatMgr.GetChatMsgInit
- ChatMgr.SyncAllMessage
- ChatMgr.SyncUnionMessage
- ChatMgr.UpdateLineProgress
- ChatMgr.GetLineName
- ChatMgr.OpenActorInfo
- ChatMgr.SendEmoji
**Snippet:**
```lua
ChatMgr = {}

function ChatMgr.FriendChatEnable(showTips)
  if EnterClampUtil.WhetherToEnter(FEATURE_ENUM.HOME_FRIEND, showTips) == false then
    return false
  end
  return true
end

function ChatMgr.GuildChannelEnable(showTips)
```

---

## BCD/ChatScriptList.lua.lua
**Requires:**
- ChatMgr
- ChatData
- ChatService
**Snippet:**
```lua
local require = require
require("ChatMgr")
require("ChatData")
require("ChatService")
```

---

## BCD/ChatService.lua.lua
**Functions:**
- ChatService.Init
- ChatService.GetChannelNewestMessageReq
- ChatService.DealGetChannelNewestMessageRsp
- ChatService.SyncMessageReq
- ChatService.DealSyncMessageRsp
- ChatService.SendMessageReq
- ChatService.DealSendMessageRsp
- ChatService.GetWorldLineInfoReq
- ChatService.DealGetWorldLineInfoRsp
- ChatService.SwitchWorldGroupReq
- ChatService.DealSwitchWorldGroupRsp
- ChatService.ReportUserReq
- ChatService.DealReportUserRsp
- ChatService.GetPrivateChattingTargetReq
- ChatService.DealGetPrivateChattingTargetRsp
- ChatService.ChangePrivateChattingTargetReq
- ChatService.DealChangePrivateChattingTargetRsp
- ChatService.GetEmojiReq
- ChatService.DealGetEmojiRsp
- ChatService.ReportLatestEmojiReq
- ChatService.DealReportLatestEmojiRsp
- ChatService.SyncPrivateHistoryMessageReq
- ChatService.DealSyncPrivateHistoryMessageRsp
- ChatService.GetChatStateReq
- ChatService.DealGetChatStateRsp
- ChatService.MarkMessageReadReq
- ChatService.DealMarkMessageReadRsp
**Snippet:**
```lua
ChatService = {}

function ChatService.Init()
  Net.AddListener(Proto.MsgName.SyncMessageRsp, ChatService.DealSyncMessageRsp)
  Net.AddListener(Proto.MsgName.SendMessageRsp, ChatService.DealSendMessageRsp)
  Net.AddListener(Proto.MsgName.GetChannelNewestMessageRsp, ChatService.DealGetChannelNewestMessageRsp)
  Net.AddListener(Proto.MsgName.GetWorldLineInfoRsp, ChatService.DealGetWorldLineInfoRsp)
  Net.AddListener(Proto.MsgName.SwitchWorldGroupRsp, ChatService.DealSwitchWorldGroupRsp)
  Net.AddListener(Proto.MsgName.ReportUserRsp, ChatService.DealReportUserRsp)
  Net.AddListener(Proto.MsgName.GetPrivateChattingTargetRsp, ChatService.DealGetPrivateChattingTargetRsp)
```

---

## BCD/ChatWindow.lua.lua
**Functions:**
- ChatWindow.ReInitData
- ChatWindow.OnInit
- ChatWindow.InitList
- ChatWindow.InitTextInput
- ChatWindow.UpdateInfo
- ChatWindow.UpdateWorldChannel
- ChatWindow.UpdateUnionChannel
- ChatWindow.UpdatePrivateChannel
- ChatWindow.UpdateSelectChannel
- ChatWindow.RenderChannel
- ChatWindow.RenderPrivate
- ChatWindow.GetOtherWordItemResource
- ChatWindow.GetGuildWordItemResource
- ChatWindow.RenderOtherWord
- ChatWindow.RenderGuildWord
- ChatWindow.GetPrivateWordItemResource
- ChatWindow.RenderPrivateWord
- ChatWindow.RenderEmojiGroup
- ChatWindow.RenderEmoji
- ChatWindow.RenderBanishPlayer
- ChatWindow.RenderFriend
- ChatWindow.UpdateEmojiList
- ChatWindow.UpdateEmojiGroupList
- ChatWindow.UpdateLine
- ChatWindow.UpdateChatWordList
- ChatWindow.UpdateDefaultWordList
- ChatWindow.UpdateGuildWordList
- ChatWindow.UpdateGuildNotice
- ChatWindow.UpdatePrivateWordList
- ChatWindow.UpdateChattingPlayerList
- ChatWindow.UpdateBanishList
- ChatWindow.UpdateFriendList
- ChatWindow.ShowFriendList
- ChatWindow.ShowBanishList
- ChatWindow.InitBtn
- ChatWindow.InitText
- ChatWindow.InitPlayerTabList
- ChatWindow.ClickPrivateReturnBtn
- ChatWindow.ClickBanishBtn
- ChatWindow.ClickLineBtn
- ChatWindow.ClickEmojiBtn
- ChatWindow.SetEmojiVisible
- ChatWindow.ClickSendBtn
- ChatWindow.SetPlayerList
- ChatWindow.ClickClose
- ChatWindow.OnShown
- ChatWindow.OnHide
- ChatWindow.OnClose
- ChatWindow.HandleMessage
**Requires:**
- Chat_ChatWindowByName
**Snippet:**
```lua
require("Chat_ChatWindowByName")
local ChatWindow = {}
local defaultChatChannel = {
  {
    name = "WorldBtn",
    channelBtn = nil,
    type = ProtoEnum.IM_SESSION_TYPE.WORLD,
    textId = 10070,
    subTextId = 10071,
    listSelectIndex = 0
```

---

## BCD/Chat_AddBtnByName.lua.lua
**Functions:**
- GetChat_AddBtnUis
**Snippet:**
```lua
function GetChat_AddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_AddTargetByName.lua.lua
**Functions:**
- GetChat_AddTargetUis
**Snippet:**
```lua
function GetChat_AddTargetUis(ui)
  local uis = {}
  
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_BanishBtnByName.lua.lua
**Functions:**
- GetChat_BanishBtnUis
**Snippet:**
```lua
function GetChat_BanishBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_ChannelBtnByName.lua.lua
**Functions:**
- GetChat_ChannelBtnUis
**Requires:**
- CommonResource_ChatByName
**Snippet:**
```lua
require("CommonResource_ChatByName")

function GetChat_ChannelBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.Red = GetCommonResource_ChatUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## BCD/Chat_ChannelListByName.lua.lua
**Functions:**
- GetChat_ChannelListUis
**Snippet:**
```lua
function GetChat_ChannelListUis(ui)
  local uis = {}
  
  uis.ChannelList = ui:GetChild("ChannelList")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_ChannelRegionByName.lua.lua
**Functions:**
- GetChat_ChannelRegionUis
**Requires:**
- Chat_ChannelListByName
- Chat_PrivateListByName
**Snippet:**
```lua
require("Chat_ChannelListByName")
require("Chat_PrivateListByName")

function GetChat_ChannelRegionUis(ui)
  local uis = {}
  uis.ChannelList = GetChat_ChannelListUis(ui:GetChild("ChannelList"))
  uis.PrivateList = GetChat_PrivateListUis(ui:GetChild("PrivateList"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## BCD/Chat_ChatByName.lua.lua
**Functions:**
- GetChat_ChatUis
**Requires:**
- Chat_FrameByName
- Chat_PlayerListAniByName
- Chat_EmojiChoiceByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("Chat_FrameByName")
require("Chat_PlayerListAniByName")
require("Chat_EmojiChoiceByName")
require("CommonResource_CurrencyReturnByName")

function GetChat_ChatUis(ui)
  local uis = {}
  uis.Frame = GetChat_FrameUis(ui:GetChild("Frame"))
  uis.PlayerListAni = GetChat_PlayerListAniUis(ui:GetChild("PlayerListAni"))
  uis.EmojiChoice = GetChat_EmojiChoiceUis(ui:GetChild("EmojiChoice"))
```

---

## BCD/Chat_ChatWindowByName.lua.lua
**Functions:**
- GetChat_ChatWindowUis
**Requires:**
- Chat_ChatByName
**Snippet:**
```lua
require("Chat_ChatByName")

function GetChat_ChatWindowUis(ui)
  local uis = {}
  uis.Main = GetChat_ChatUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_ChatWordItem1ByName.lua.lua
**Functions:**
- GetChat_ChatWordItem1Uis
**Requires:**
- Chat_LeftWord1ByName
- Chat_RightWord1ByName
**Snippet:**
```lua
require("Chat_LeftWord1ByName")
require("Chat_RightWord1ByName")

function GetChat_ChatWordItem1Uis(ui)
  local uis = {}
  uis.LeftWord = GetChat_LeftWord1Uis(ui:GetChild("LeftWord"))
  uis.RightWord = GetChat_RightWord1Uis(ui:GetChild("RightWord"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## BCD/Chat_ChatWordItemByName.lua.lua
**Functions:**
- GetChat_ChatWordItemUis
**Requires:**
- Chat_LeftWordByName
- Chat_RightWordByName
**Snippet:**
```lua
require("Chat_LeftWordByName")
require("Chat_RightWordByName")

function GetChat_ChatWordItemUis(ui)
  local uis = {}
  uis.LeftWord = GetChat_LeftWordUis(ui:GetChild("LeftWord"))
  uis.RightWord = GetChat_RightWordUis(ui:GetChild("RightWord"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## BCD/Chat_ChoiceLine1ByName.lua.lua
**Functions:**
- GetChat_ChoiceLine1Uis
**Requires:**
- Chat_LineTabByName
**Snippet:**
```lua
require("Chat_LineTabByName")

function GetChat_ChoiceLine1Uis(ui)
  local uis = {}
  uis.LineList = ui:GetChild("LineList")
  uis.LineTab = GetChat_LineTabUis(ui:GetChild("LineTab"))
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_ChoiceLine2ByName.lua.lua
**Functions:**
- GetChat_ChoiceLine2Uis
**Requires:**
- CommonResource_PopupBgByName
- CommonResource_Popup_BByName
- Chat_ChoiceLine1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("CommonResource_Popup_BByName")
require("Chat_ChoiceLine1ByName")

function GetChat_ChoiceLine2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Popup_B = GetCommonResource_Popup_BUis(ui:GetChild("Popup_B"))
  uis.ChoiceLine1 = GetChat_ChoiceLine1Uis(ui:GetChild("ChoiceLine1"))
```

---

## BCD/Chat_ChoiceLineWindowByName.lua.lua
**Functions:**
- GetChat_ChoiceLineWindowUis
**Requires:**
- Chat_ChoiceLine2ByName
**Snippet:**
```lua
require("Chat_ChoiceLine2ByName")

function GetChat_ChoiceLineWindowUis(ui)
  local uis = {}
  uis.Main = GetChat_ChoiceLine2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_CloseBtnByName.lua.lua
**Functions:**
- GetChat_CloseBtnUis
**Snippet:**
```lua
function GetChat_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_Complaint1ByName.lua.lua
**Functions:**
- GetChat_Complaint1Uis
**Requires:**
- Chat_ContentByName
**Snippet:**
```lua
require("Chat_ContentByName")

function GetChat_Complaint1Uis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Content = GetChat_ContentUis(ui:GetChild("Content"))
  uis.OptionList = ui:GetChild("OptionList")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_Complaint2ByName.lua.lua
**Functions:**
- GetChat_Complaint2Uis
**Requires:**
- CommonResource_PopupBgByName
- CommonResource_Popup_BByName
- Chat_Complaint1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("CommonResource_Popup_BByName")
require("Chat_Complaint1ByName")

function GetChat_Complaint2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Popup_B = GetCommonResource_Popup_BUis(ui:GetChild("Popup_B"))
  uis.Complaint1 = GetChat_Complaint1Uis(ui:GetChild("Complaint1"))
```

---

## BCD/Chat_ComplaintWindowByName.lua.lua
**Functions:**
- GetChat_ComplaintWindowUis
**Requires:**
- Chat_Complaint2ByName
**Snippet:**
```lua
require("Chat_Complaint2ByName")

function GetChat_ComplaintWindowUis(ui)
  local uis = {}
  uis.Main = GetChat_Complaint2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_ContentByName.lua.lua
**Functions:**
- GetChat_ContentUis
**Snippet:**
```lua
function GetChat_ContentUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_EmojiBtnByName.lua.lua
**Functions:**
- GetChat_EmojiBtnUis
**Snippet:**
```lua
function GetChat_EmojiBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_EmojiChoiceByName.lua.lua
**Functions:**
- GetChat_EmojiChoiceUis
**Snippet:**
```lua
function GetChat_EmojiChoiceUis(ui)
  local uis = {}
  
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.PicList = ui:GetChild("PicList")
  uis.TypeList = ui:GetChild("TypeList")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_EmojiPicBtnByName.lua.lua
**Functions:**
- GetChat_EmojiPicBtnUis
**Snippet:**
```lua
function GetChat_EmojiPicBtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.PicHolder = ui:GetChild("PicHolder")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_EmojiTypeBtnByName.lua.lua
**Functions:**
- GetChat_EmojiTypeBtnUis
**Requires:**
- Chat_EmojiTypePicByName
**Snippet:**
```lua
require("Chat_EmojiTypePicByName")

function GetChat_EmojiTypeBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EmojiTypePic = GetChat_EmojiTypePicUis(ui:GetChild("EmojiTypePic"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## BCD/Chat_EmojiTypePicByName.lua.lua
**Functions:**
- GetChat_EmojiTypePicUis
**Snippet:**
```lua
function GetChat_EmojiTypePicUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_FrameByName.lua.lua
**Functions:**
- GetChat_FrameUis
**Requires:**
- Chat_ChannelRegionByName
- Chat_InputWordByName
- Chat_WordListByName
**Snippet:**
```lua
require("Chat_ChannelRegionByName")
require("Chat_InputWordByName")
require("Chat_WordListByName")

function GetChat_FrameUis(ui)
  local uis = {}
  uis.ChannelRegion = GetChat_ChannelRegionUis(ui:GetChild("ChannelRegion"))
  uis.LineBtn = ui:GetChild("LineBtn")
  uis.BanishBtn = ui:GetChild("BanishBtn")
  uis.InputWord = GetChat_InputWordUis(ui:GetChild("InputWord"))
```

---

## BCD/Chat_FriendTabBtnByName.lua.lua
**Functions:**
- GetChat_FriendTabBtnUis
**Snippet:**
```lua
function GetChat_FriendTabBtnUis(ui)
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

## BCD/Chat_FriendTabRegionByName.lua.lua
**Functions:**
- GetChat_FriendTabRegionUis
**Snippet:**
```lua
function GetChat_FriendTabRegionUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_GuildSystemWordItemByName.lua.lua
**Functions:**
- GetChat_GuildSystemWordItemUis
**Snippet:**
```lua
function GetChat_GuildSystemWordItemUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_GulidNoticeBtnByName.lua.lua
**Functions:**
- GetChat_GulidNoticeBtnUis
**Snippet:**
```lua
function GetChat_GulidNoticeBtnUis(ui)
  local uis = {}
  
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## BCD/Chat_InputWordByName.lua.lua
**Functions:**
- GetChat_InputWordUis
**Snippet:**
```lua
function GetChat_InputWordUis(ui)
  local uis = {}
  
  uis.InputTxt = ui:GetChild("InputTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_LeftWord1ByName.lua.lua
**Functions:**
- GetChat_LeftWord1Uis
**Requires:**
- CommonResource_HeadByName
**Snippet:**
```lua
require("CommonResource_HeadByName")

function GetChat_LeftWord1Uis(ui)
  local uis = {}
  uis.Head = GetCommonResource_HeadUis(ui:GetChild("Head"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
```

---

## BCD/Chat_LeftWordByName.lua.lua
**Functions:**
- GetChat_LeftWordUis
**Requires:**
- CommonResource_HeadByName
**Snippet:**
```lua
require("CommonResource_HeadByName")

function GetChat_LeftWordUis(ui)
  local uis = {}
  uis.Head = GetCommonResource_HeadUis(ui:GetChild("Head"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
```

---

## BCD/Chat_LineBtnByName.lua.lua
**Functions:**
- GetChat_LineBtnUis
**Snippet:**
```lua
function GetChat_LineBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberProgressBar = ui:GetChild("NumberProgressBar")
  uis.c1Ctr = ui:GetController("c1")
  uis.ButtonCtr = ui:GetController("Button")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_LineTabBtnBgByName.lua.lua
**Functions:**
- GetChat_LineTabBtnBgUis
**Snippet:**
```lua
function GetChat_LineTabBtnBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_LineTabBtnByName.lua.lua
**Functions:**
- GetChat_LineTabBtnUis
**Requires:**
- Chat_LineTabBtnBgByName
**Snippet:**
```lua
require("Chat_LineTabBtnBgByName")

function GetChat_LineTabBtnUis(ui)
  local uis = {}
  uis.ChannelBtnBg = GetChat_LineTabBtnBgUis(ui:GetChild("ChannelBtnBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## BCD/Chat_LineTabByName.lua.lua
**Functions:**
- GetChat_LineTabUis
**Snippet:**
```lua
function GetChat_LineTabUis(ui)
  local uis = {}
  
  uis.LineList = ui:GetChild("LineList")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_NumberProgressBarByName.lua.lua
**Functions:**
- GetChat_NumberProgressBarUis
**Requires:**
- Chat_NumberProgressFillByName
**Snippet:**
```lua
require("Chat_NumberProgressFillByName")

function GetChat_NumberProgressBarUis(ui)
  local uis = {}
  uis.bar = GetChat_NumberProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_NumberProgressFillByName.lua.lua
**Functions:**
- GetChat_NumberProgressFillUis
**Snippet:**
```lua
function GetChat_NumberProgressFillUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_OnLineByName.lua.lua
**Functions:**
- GetChat_OnLineUis
**Snippet:**
```lua
function GetChat_OnLineUis(ui)
  local uis = {}
  
  uis.OnLineTxt = ui:GetChild("OnLineTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_OptionBtnByName.lua.lua
**Functions:**
- GetChat_OptionBtnUis
**Snippet:**
```lua
function GetChat_OptionBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_PlayerHeadBgByName.lua.lua
**Functions:**
- GetChat_PlayerHeadBgUis
**Snippet:**
```lua
function GetChat_PlayerHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_PlayerHeadByName.lua.lua
**Functions:**
- GetChat_PlayerHeadUis
**Requires:**
- Chat_PlayerHeadBgByName
**Snippet:**
```lua
require("Chat_PlayerHeadBgByName")

function GetChat_PlayerHeadUis(ui)
  local uis = {}
  uis.PlayerHeadBg = GetChat_PlayerHeadBgUis(ui:GetChild("PlayerHeadBg"))
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_PlayerInfoByName.lua.lua
**Functions:**
- GetChat_PlayerInfoUis
**Requires:**
- CommonResource_HeadByName
- Chat_ShieldOnLineByName
**Snippet:**
```lua
require("CommonResource_HeadByName")
require("Chat_ShieldOnLineByName")

function GetChat_PlayerInfoUis(ui)
  local uis = {}
  uis.Head = GetCommonResource_HeadUis(ui:GetChild("Head"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.OnLine = GetChat_ShieldOnLineUis(ui:GetChild("OnLine"))
  uis.DeleteBtn = ui:GetChild("DeleteBtn")
```

---

## BCD/Chat_PlayerListAniByName.lua.lua
**Functions:**
- GetChat_PlayerListAniUis
**Requires:**
- Chat_PlayerListByName
**Snippet:**
```lua
require("Chat_PlayerListByName")

function GetChat_PlayerListAniUis(ui)
  local uis = {}
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.PlayerList = GetChat_PlayerListUis(ui:GetChild("PlayerList"))
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_PlayerListByName.lua.lua
**Functions:**
- GetChat_PlayerListUis
**Requires:**
- Chat_FriendTabRegionByName
**Snippet:**
```lua
require("Chat_FriendTabRegionByName")

function GetChat_PlayerListUis(ui)
  local uis = {}
  uis.BanishList = ui:GetChild("BanishList")
  uis.FriendList = ui:GetChild("FriendList")
  uis.FriendTabRegion = GetChat_FriendTabRegionUis(ui:GetChild("FriendTabRegion"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## BCD/Chat_PrivateByName.lua.lua
**Functions:**
- GetChat_PrivateUis
**Snippet:**
```lua
function GetChat_PrivateUis(ui)
  local uis = {}
  
  uis.TargetBtn = ui:GetChild("TargetBtn")
  uis.DeletePrivateBtn = ui:GetChild("DeletePrivateBtn")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_PrivateListByName.lua.lua
**Functions:**
- GetChat_PrivateListUis
**Snippet:**
```lua
function GetChat_PrivateListUis(ui)
  local uis = {}
  
  uis.PrivateReturnBtn = ui:GetChild("PrivateReturnBtn")
  uis.PrivateList = ui:GetChild("PrivateList")
  uis.AddBtn = ui:GetChild("AddBtn")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_PrivateReturnBtnByName.lua.lua
**Functions:**
- GetChat_PrivateReturnBtnUis
**Snippet:**
```lua
function GetChat_PrivateReturnBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_PrivateTipsWordByName.lua.lua
**Functions:**
- GetChat_PrivateTipsWordUis
**Snippet:**
```lua
function GetChat_PrivateTipsWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_RelieveBtnByName.lua.lua
**Functions:**
- GetChat_RelieveBtnUis
**Snippet:**
```lua
function GetChat_RelieveBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_RightWord1ByName.lua.lua
**Functions:**
- GetChat_RightWord1Uis
**Requires:**
- CommonResource_HeadByName
**Snippet:**
```lua
require("CommonResource_HeadByName")

function GetChat_RightWord1Uis(ui)
  local uis = {}
  uis.Head = GetCommonResource_HeadUis(ui:GetChild("Head"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
```

---

## BCD/Chat_RightWordByName.lua.lua
**Functions:**
- GetChat_RightWordUis
**Requires:**
- CommonResource_HeadByName
**Snippet:**
```lua
require("CommonResource_HeadByName")

function GetChat_RightWordUis(ui)
  local uis = {}
  uis.Head = GetCommonResource_HeadUis(ui:GetChild("Head"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
```

---

## BCD/Chat_ShieldOnLineByName.lua.lua
**Functions:**
- GetChat_ShieldOnLineUis
**Snippet:**
```lua
function GetChat_ShieldOnLineUis(ui)
  local uis = {}
  
  uis.OnLineTxt = ui:GetChild("OnLineTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_SystemWordItemByName.lua.lua
**Functions:**
- GetChat_SystemWordItemUis
**Snippet:**
```lua
function GetChat_SystemWordItemUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_TargetBtnBgByName.lua.lua
**Functions:**
- GetChat_TargetBtnBgUis
**Snippet:**
```lua
function GetChat_TargetBtnBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## BCD/Chat_TargetBtnByName.lua.lua
**Functions:**
- GetChat_TargetBtnUis
**Requires:**
- Chat_TargetBtnBgByName
- Chat_OnLineByName
- CommonResource_ChatByName
**Snippet:**
```lua
require("Chat_TargetBtnBgByName")
require("Chat_OnLineByName")
require("CommonResource_ChatByName")

function GetChat_TargetBtnUis(ui)
  local uis = {}
  uis.PlayerHeadBg = GetChat_TargetBtnBgUis(ui:GetChild("PlayerHeadBg"))
  uis.OnLine = GetChat_OnLineUis(ui:GetChild("OnLine"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_ChatUis(ui:GetChild("Red"))
```

---

## BCD/Chat_WordListByName.lua.lua
**Functions:**
- GetChat_WordListUis
**Requires:**
- Chat_PrivateTipsWordByName
- Chat_AddTargetByName
**Snippet:**
```lua
require("Chat_PrivateTipsWordByName")
require("Chat_AddTargetByName")

function GetChat_WordListUis(ui)
  local uis = {}
  uis.OtherWordList = ui:GetChild("OtherWordList")
  uis.PrivateTipsWord = GetChat_PrivateTipsWordUis(ui:GetChild("PrivateTipsWord"))
  uis.PrivateWordList = ui:GetChild("PrivateWordList")
  uis.TipsTxt = GetChat_AddTargetUis(ui:GetChild("TipsTxt"))
  uis.GulidNoticeBtn = ui:GetChild("GulidNoticeBtn")
```

---

## BCD/ChoiceHeadWindow.lua.lua
**Functions:**
- ChoiceHeadWindow.ReInitData
- ChoiceHeadWindow.OnInit
- ChoiceHeadWindow.UpdateDefaultTabIndex
- ChoiceHeadWindow.UpdateTab
- ChoiceHeadWindow.TestEnableFunction
- ChoiceHeadWindow.GetMemberList
- ChoiceHeadWindow.TouchCardFashion
- ChoiceHeadWindow.UpdateDetailInfo
- ChoiceHeadWindow.UpdateInfo
- ChoiceHeadWindow.UpdateMemberHead
- headList.itemRenderer
- ChoiceHeadWindow.UpdateOtherHead
- headList.itemRenderer
- ChoiceHeadWindow.UpdateHeadRect
- headList.itemRenderer
- ChoiceHeadWindow.TouchCardItem
- subHeadList.itemRenderer
- ChoiceHeadWindow.TouchOtherItem
- detail.WordList.itemRenderer
- ChoiceHeadWindow.TouchHeadRectItem
- detail.WordList.itemRenderer
- ChoiceHeadWindow.InitBtn
- ChoiceHeadWindow.TouchClose
- ChoiceHeadWindow.OnClose
- ChoiceHeadWindow.HandleMessage
**Requires:**
- PlayerInfo_ChoiceHeadWindowByName
**Snippet:**
```lua
require("PlayerInfo_ChoiceHeadWindowByName")
local ChoiceHeadWindow = {}
local uis, contentPane, curSelectTabIndex, curSelectCardId, curSelectCardFashionId, curSelectHeadId, curSelectHeadRectId, curHeadItemList, curHeadRectItemList
local TAB_ENUM = {
  MEMBER = 0,
  OTHER = 1,
  HEAD_RECT = 2
}
local notPlayAnim, defaultPage

```

---

## BCD/ChoiceLineWindow.lua.lua
**Functions:**
- ChoiceLineWindow.ReInitData
- ChoiceLineWindow.OnInit
- ChoiceLineWindow.UpdateInfo
- ChoiceLineWindow.UpdateTab
- ChoiceLineWindow.UpdateLineList
- ChoiceLineWindow.InitBtn
- ChoiceLineWindow.ClickCloseBtn
- ChoiceLineWindow.OnShown
- ChoiceLineWindow.OnHide
- ChoiceLineWindow.OnClose
- ChoiceLineWindow.HandleMessage
**Requires:**
- Chat_ChoiceLineWindowByName
**Snippet:**
```lua
require("Chat_ChoiceLineWindowByName")
local ChoiceLineWindow = {}
local uis, contentPane

function ChoiceLineWindow.ReInitData()
end

local perPageCount = 20
local allLineList
local formatString = ""
```

---

## BCD/ChoiceWindow.lua.lua
**Functions:**
- ChoiceWindow.ReInitData
- ChoiceWindow.OnInit
- ChoiceWindow.GetCardDate
- ChoiceWindow.UpdateInfo
- ChoiceWindow.GetNumIndex
- ChoiceWindow.GetKey
- ChoiceWindow.RefreshCardItem
- ChoiceWindow.ShowDefaultCard
- ChoiceWindow.InitBtn
- ChoiceWindow.RefreshCardScreenUI
- ChoiceWindow.InitChoiceData
- ChoiceWindow.InitCardScreenBtn
- ChoiceWindow.GetIsChoice
- ChoiceWindow.OnClose
**Requires:**
- PlayerInfo_ChoiceWindowByName
**Snippet:**
```lua
require("PlayerInfo_ChoiceWindowByName")
local ChoiceWindow = {}
local uis, contentPane, sortType, cardListData, jumpTb, elementTab, occupation, btnTb, choiceData, choiceCards

function ChoiceWindow.ReInitData()
end

function ChoiceWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ChoiceWindow.package, WinResConfig.ChoiceWindow.comName, function(com)
    contentPane = com
```

---

## BCD/Circle.lua.lua
**Functions:**
- Circle:__ctor
- Circle:init
- Circle:initLocalData
- Circle:initMassData
- Circle:translateCentroid
- Circle:updateVertices
- Circle:updateCenter
- Circle:update
- Circle:setAngle
- Circle:setPos
- Circle:updateAABB
- Circle:containPoint
**Snippet:**
```lua
local base = Shape
local Circle = Create("Circle", base)

function Circle:__ctor(x, y, radius)
  self.shapeType = ShapeType.Circle
  self.x = x
  self.y = y
  self.radius = radius
  self.radiusSq = 0
  self.changed = false
```

---

## BCD/Class.lua.lua
**Functions:**
- class
- cls.ctor
- cls.new
- cls.new
**Snippet:**
```lua
function class(classname, super)
  local superType = type(super)
  
  local cls
  if "function" ~= superType and "table" ~= superType then
    super = nil
    superType = nil
  end
  if "function" == superType or super and 1 == super.__ctype then
    cls = {}
```

---

## BCD/ClothesDetailsWindow.lua.lua
**Functions:**
- ClothesDetailsWindow.ReInitData
- ClothesDetailsWindow.OnInit
- ClothesDetailsWindow.UpdateInfo
- ClothesDetailsWindow.SetFashionName
- ClothesDetailsWindow.UpdateModel
- ClothesDetailsWindow.InitBtn
- ClothesDetailsWindow.OnClose
**Requires:**
- Clothes_ClothesDetailsWindowByName
**Snippet:**
```lua
require("Clothes_ClothesDetailsWindowByName")
local ClothesDetailsWindow = {}
local uis, contentPane, curId, fashionData, cardData, jumpTb

function ClothesDetailsWindow.ReInitData()
end

function ClothesDetailsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ClothesDetailsWindow.package, WinResConfig.ClothesDetailsWindow.comName, function(com)
    contentPane = com
```

---

## BCD/ClothesGetShowWindow.lua.lua
**Functions:**
- ClothesGetShowWindow.ReInitData
- ClothesGetShowWindow.OnInit
- ClothesGetShowWindow.UpdateInfo
- callback
- uis.Main.TipsList.itemRenderer
- ClothesGetShowWindow.CloseWindow
- ClothesGetShowWindow.InitBtn
- ClothesGetShowWindow.OnClose
**Requires:**
- ClothesGetShow_ClothesGetShowWindowByName
**Snippet:**
```lua
require("ClothesGetShow_ClothesGetShowWindowByName")
local ClothesGetShowWindow = {}
local uis, contentPane, fashionId, closeCallback, index, fullScreenClose

function ClothesGetShowWindow.ReInitData()
end

function ClothesGetShowWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ClothesGetShowWindow.package, WinResConfig.ClothesGetShowWindow.comName, function(com)
    contentPane = com
```

---

## BCD/ClothesGetShow_CardNameByName.lua.lua
**Functions:**
- GetClothesGetShow_CardNameUis
**Snippet:**
```lua
function GetClothesGetShow_CardNameUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/ClothesGetShow_CardShowByName.lua.lua
**Functions:**
- GetClothesGetShow_CardShowUis
**Snippet:**
```lua
function GetClothesGetShow_CardShowUis(ui)
  local uis = {}
  
  uis.CardShowLoader = ui:GetChild("CardShowLoader")
  uis.CardShowHolder = ui:GetChild("CardShowHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/ClothesGetShow_CardTouchWordByName.lua.lua
**Functions:**
- GetClothesGetShow_CardTouchWordUis
**Snippet:**
```lua
function GetClothesGetShow_CardTouchWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/ClothesGetShow_ClothesGetShowByName.lua.lua
**Functions:**
- GetClothesGetShow_ClothesGetShowUis
**Requires:**
- CommonResource_BackGroundByName
- ClothesGetShow_CardShowByName
- ClothesGetShow_CardNameByName
- ClothesGetShow_CardTouchWordByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ClothesGetShow_CardShowByName")
require("ClothesGetShow_CardNameByName")
require("ClothesGetShow_CardTouchWordByName")

function GetClothesGetShow_ClothesGetShowUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.CardShow = GetClothesGetShow_CardShowUis(ui:GetChild("CardShow"))
  uis.CardName = GetClothesGetShow_CardNameUis(ui:GetChild("CardName"))
```

---

## BCD/ClothesGetShow_ClothesGetShowWindowByName.lua.lua
**Functions:**
- GetClothesGetShow_ClothesGetShowWindowUis
**Requires:**
- ClothesGetShow_ClothesGetShowByName
**Snippet:**
```lua
require("ClothesGetShow_ClothesGetShowByName")

function GetClothesGetShow_ClothesGetShowWindowUis(ui)
  local uis = {}
  uis.Main = GetClothesGetShow_ClothesGetShowUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/ClothesGetShow_ContentTipsByName.lua.lua
**Functions:**
- GetClothesGetShow_ContentTipsUis
**Snippet:**
```lua
function GetClothesGetShow_ContentTipsUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/Clothes_CardQBByName.lua.lua
**Functions:**
- GetClothes_CardQBUis
**Snippet:**
```lua
function GetClothes_CardQBUis(ui)
  local uis = {}
  
  uis.QBHolder = ui:GetChild("QBHolder")
  uis.root = ui
  return uis
end
```

---

## BCD/Clothes_CardShowByName.lua.lua
**Functions:**
- GetClothes_CardShowUis
**Snippet:**
```lua
function GetClothes_CardShowUis(ui)
  local uis = {}
  
  uis.CardShowLoader = ui:GetChild("CardShowLoader")
  uis.CardShowHolder = ui:GetChild("CardShowHolder")
  uis.root = ui
  return uis
end
```

---

## BCD/Clothes_ClothesCardInfoByName.lua.lua
**Functions:**
- GetClothes_ClothesCardInfoUis
**Snippet:**
```lua
function GetClothes_ClothesCardInfoUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.ClothesNameTxt = ui:GetChild("ClothesNameTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## BCD/Clothes_ClothesDetailsByName.lua.lua
**Functions:**
- GetClothes_ClothesDetailsUis
**Requires:**
- CommonResource_BackGroundByName
- Clothes_CardShowByName
- Clothes_CardQBByName
- Clothes_ClothesCardInfoByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Clothes_CardShowByName")
require("Clothes_CardQBByName")
require("Clothes_ClothesCardInfoByName")
require("CommonResource_CurrencyReturnByName")

function GetClothes_ClothesDetailsUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.CardShow = GetClothes_CardShowUis(ui:GetChild("CardShow"))
```

---

## BCD/Clothes_ClothesDetailsWindowByName.lua.lua
**Functions:**
- GetClothes_ClothesDetailsWindowUis
**Requires:**
- Clothes_ClothesDetailsByName
**Snippet:**
```lua
require("Clothes_ClothesDetailsByName")

function GetClothes_ClothesDetailsWindowUis(ui)
  local uis = {}
  uis.Main = GetClothes_ClothesDetailsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/CodeWindow.lua.lua
**Functions:**
- CodeWindow.ReInitData
- CodeWindow.OnInit
- CodeWindow.UpdateInfo
- CodeWindow.InitBtn
- CodeWindow.FormatText
- CodeWindow.TouchClose
- CodeWindow.OnClose
**Requires:**
- Message_CodeWindowByName
**Snippet:**
```lua
require("Message_CodeWindowByName")
local CodeWindow = {}
local uis, contentPane

function CodeWindow.ReInitData()
end

function CodeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.CodeWindow.package, WinResConfig.CodeWindow.comName, function(com)
    contentPane = com
```

---

## BCD/CollideManager.lua.lua
**Functions:**
- CollideManager:__ctor
- CollideManager:init
- CollideManager:collideGrid
- CollideManager:collideSimple
- CollideManager:collideTowBodies
- CollideManager:hasCollided
- CollideManager:getArbiter
- CollideManager:update
- CollideManager:preSolve
- CollideManager:solve
- CollideManager:onCollided
- CollideManager:onSeparated
- CollideManager:onColliding
- CollideManager:onCollideSolve
- CollideManager:circleCircle
- CollideManager:polyCircle
- CollideManager:featurePairPolyCircle
- CollideManager:polyPoly
- CollideManager:featurePairPolyPoly
- CollideManager:compSingle
- CollideManager:compComp
**Snippet:**
```lua
local CollideManager = Create("CollideManager")
local isCollidable = function(bodyA, bodyB)
  if bodyA.disabled or bodyB.disabled then
    return false
  end
  local layerA, layerMaskA = bodyA.layer, bodyA.layerMask
  local layerB, layerMaskB = bodyB.layer, bodyB.layerMask
  if type(layerA) == "number" and type(layerB) == "number" and type(layerMaskA) == "number" and type(layerMaskB) == "number" and (0 == layerMaskA & layerB or 0 == layerMaskB & layerA) then
    return false
  end
```

---

## BCD/CommonResource_AbyssBtnByName.lua.lua
**Functions:**
- GetCommonResource_AbyssBtnUis
**Snippet:**
```lua
function GetCommonResource_AbyssBtnUis(ui)
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

## BCD/CommonResource_AbyssNewPeopleBtnByName.lua.lua
**Functions:**
- GetCommonResource_AbyssNewPeopleBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetCommonResource_AbyssNewPeopleBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_AbyssSign1ByName.lua.lua
**Functions:**
- GetCommonResource_AbyssSign1Uis
**Snippet:**
```lua
function GetCommonResource_AbyssSign1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_AbyssSign2ByName.lua.lua
**Functions:**
- GetCommonResource_AbyssSign2Uis
**Snippet:**
```lua
function GetCommonResource_AbyssSign2Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_AbyssSign3ByName.lua.lua
**Functions:**
- GetCommonResource_AbyssSign3Uis
**Snippet:**
```lua
function GetCommonResource_AbyssSign3Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_AbyssSign4ByName.lua.lua
**Functions:**
- GetCommonResource_AbyssSign4Uis
**Snippet:**
```lua
function GetCommonResource_AbyssSign4Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_AbyssSignByName.lua.lua
**Functions:**
- GetCommonResource_AbyssSignUis
**Snippet:**
```lua
function GetCommonResource_AbyssSignUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_AbyssTipsBtnByName.lua.lua
**Functions:**
- GetCommonResource_AbyssTipsBtnUis
**Snippet:**
```lua
function GetCommonResource_AbyssTipsBtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_AbyssTipsWordByName.lua.lua
**Functions:**
- GetCommonResource_AbyssTipsWordUis
**Snippet:**
```lua
function GetCommonResource_AbyssTipsWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Activity17_HpBossBarByName.lua.lua
**Functions:**
- GetCommonResource_Activity17_HpBossBarUis
**Requires:**
- CommonResource_Activity17_HpBossFillByName
**Snippet:**
```lua
require("CommonResource_Activity17_HpBossFillByName")

function GetCommonResource_Activity17_HpBossBarUis(ui)
  local uis = {}
  uis.bar = GetCommonResource_Activity17_HpBossFillUis(ui:GetChild("bar"))
  uis.FirmProgressBar = ui:GetChild("FirmProgressBar")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Activity17_HpBossFillByName.lua.lua
**Functions:**
- GetCommonResource_Activity17_HpBossFillUis
**Snippet:**
```lua
function GetCommonResource_Activity17_HpBossFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Activity17_HpBossFirmBarByName.lua.lua
**Functions:**
- GetCommonResource_Activity17_HpBossFirmBarUis
**Requires:**
- CommonResource_Activity17_HpBossFirmFillByName
**Snippet:**
```lua
require("CommonResource_Activity17_HpBossFirmFillByName")

function GetCommonResource_Activity17_HpBossFirmBarUis(ui)
  local uis = {}
  uis.bar = GetCommonResource_Activity17_HpBossFirmFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Activity17_HpBossFirmFillByName.lua.lua
**Functions:**
- GetCommonResource_Activity17_HpBossFirmFillUis
**Snippet:**
```lua
function GetCommonResource_Activity17_HpBossFirmFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Activity17_HpEliteBarByName.lua.lua
**Functions:**
- GetCommonResource_Activity17_HpEliteBarUis
**Requires:**
- CommonResource_Activity17_HpEliteFillByName
**Snippet:**
```lua
require("CommonResource_Activity17_HpEliteFillByName")

function GetCommonResource_Activity17_HpEliteBarUis(ui)
  local uis = {}
  uis.bar = GetCommonResource_Activity17_HpEliteFillUis(ui:GetChild("bar"))
  uis.FirmProgressBar = ui:GetChild("FirmProgressBar")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Activity17_HpEliteFillByName.lua.lua
**Functions:**
- GetCommonResource_Activity17_HpEliteFillUis
**Snippet:**
```lua
function GetCommonResource_Activity17_HpEliteFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Activity17_HpEliteFirmBarByName.lua.lua
**Functions:**
- GetCommonResource_Activity17_HpEliteFirmBarUis
**Requires:**
- CommonResource_Activity17_HpEliteFirmFillByName
**Snippet:**
```lua
require("CommonResource_Activity17_HpEliteFirmFillByName")

function GetCommonResource_Activity17_HpEliteFirmBarUis(ui)
  local uis = {}
  uis.bar = GetCommonResource_Activity17_HpEliteFirmFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Activity17_HpEliteFirmFillByName.lua.lua
**Functions:**
- GetCommonResource_Activity17_HpEliteFirmFillUis
**Snippet:**
```lua
function GetCommonResource_Activity17_HpEliteFirmFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Activity17_HpMonsterBarByName.lua.lua
**Functions:**
- GetCommonResource_Activity17_HpMonsterBarUis
**Requires:**
- CommonResource_Activity17_HpMonsterFillByName
**Snippet:**
```lua
require("CommonResource_Activity17_HpMonsterFillByName")

function GetCommonResource_Activity17_HpMonsterBarUis(ui)
  local uis = {}
  uis.bar = GetCommonResource_Activity17_HpMonsterFillUis(ui:GetChild("bar"))
  uis.FirmProgressBar = ui:GetChild("FirmProgressBar")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Activity17_HpMonsterFillByName.lua.lua
**Functions:**
- GetCommonResource_Activity17_HpMonsterFillUis
**Snippet:**
```lua
function GetCommonResource_Activity17_HpMonsterFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Activity17_HpMonsterFirmBarByName.lua.lua
**Functions:**
- GetCommonResource_Activity17_HpMonsterFirmBarUis
**Requires:**
- CommonResource_Activity17_HpMonsterFirmFillByName
**Snippet:**
```lua
require("CommonResource_Activity17_HpMonsterFirmFillByName")

function GetCommonResource_Activity17_HpMonsterFirmBarUis(ui)
  local uis = {}
  uis.bar = GetCommonResource_Activity17_HpMonsterFirmFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Activity17_HpMonsterFirmFillByName.lua.lua
**Functions:**
- GetCommonResource_Activity17_HpMonsterFirmFillUis
**Snippet:**
```lua
function GetCommonResource_Activity17_HpMonsterFirmFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Activity17_MonsterHPByName.lua.lua
**Functions:**
- GetCommonResource_Activity17_MonsterHPUis
**Snippet:**
```lua
function GetCommonResource_Activity17_MonsterHPUis(ui)
  local uis = {}
  
  uis.HpMonsterProgressBar = ui:GetChild("HpMonsterProgressBar")
  uis.HpEliteProgressBar = ui:GetChild("HpEliteProgressBar")
  uis.HpBossProgressBar = ui:GetChild("HpBossProgressBar")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_ActivityBtnByName.lua.lua
**Functions:**
- GetCommonResource_ActivityBtnUis
**Snippet:**
```lua
function GetCommonResource_ActivityBtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_AdventureBtnByName.lua.lua
**Functions:**
- GetCommonResource_AdventureBtnUis
**Snippet:**
```lua
function GetCommonResource_AdventureBtnUis(ui)
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

## BCD/CommonResource_AllFrame_R_BtnByName.lua.lua
**Functions:**
- GetCommonResource_AllFrame_R_BtnUis
**Requires:**
- CommonResource_HeadFrame_RByName
- CommonResource_BuildFrame_RByName
- CommonResource_GuildBossCardSignByName
**Snippet:**
```lua
require("CommonResource_HeadFrame_RByName")
require("CommonResource_BuildFrame_RByName")
require("CommonResource_GuildBossCardSignByName")

function GetCommonResource_AllFrame_R_BtnUis(ui)
  local uis = {}
  uis.HeadFrame_R = GetCommonResource_HeadFrame_RUis(ui:GetChild("HeadFrame_R"))
  uis.BuildFrame_R = GetCommonResource_BuildFrame_RUis(ui:GetChild("BuildFrame_R"))
  uis.GuildBossCardSign = GetCommonResource_GuildBossCardSignUis(ui:GetChild("GuildBossCardSign"))
  uis.buttonCtr = ui:GetController("button")
```

---

## BCD/CommonResource_AngerBarByName.lua.lua
**Functions:**
- GetCommonResource_AngerBarUis
**Requires:**
- CommonResource_AngerFillByName
**Snippet:**
```lua
require("CommonResource_AngerFillByName")

function GetCommonResource_AngerBarUis(ui)
  local uis = {}
  uis.bar = GetCommonResource_AngerFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_AngerFillByName.lua.lua
**Functions:**
- GetCommonResource_AngerFillUis
**Snippet:**
```lua
function GetCommonResource_AngerFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_ArenaDefendNewByName.lua.lua
**Functions:**
- GetCommonResource_ArenaDefendNewUis
**Snippet:**
```lua
function GetCommonResource_ArenaDefendNewUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_ArenaNewSeasonByName.lua.lua
**Functions:**
- GetCommonResource_ArenaNewSeasonUis
**Snippet:**
```lua
function GetCommonResource_ArenaNewSeasonUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_ArenaTimeByName.lua.lua
**Functions:**
- GetCommonResource_ArenaTimeUis
**Snippet:**
```lua
function GetCommonResource_ArenaTimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_AssetsBossBtnByName.lua.lua
**Functions:**
- GetCommonResource_AssetsBossBtnUis
**Snippet:**
```lua
function GetCommonResource_AssetsBossBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_AssetsBossTipsByName.lua.lua
**Functions:**
- GetCommonResource_AssetsBossTipsUis
**Snippet:**
```lua
function GetCommonResource_AssetsBossTipsUis(ui)
  local uis = {}
  
  uis.IconLoader = ui:GetChild("IconLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.AssetsBtn = ui:GetChild("AssetsBtn")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_AssetsBtnByName.lua.lua
**Functions:**
- GetCommonResource_AssetsBtnUis
**Snippet:**
```lua
function GetCommonResource_AssetsBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_AssetsTipsByName.lua.lua
**Functions:**
- GetCommonResource_AssetsTipsUis
**Snippet:**
```lua
function GetCommonResource_AssetsTipsUis(ui)
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

## BCD/CommonResource_BackGroundByName.lua.lua
**Functions:**
- GetCommonResource_BackGroundUis
**Snippet:**
```lua
function GetCommonResource_BackGroundUis(ui)
  local uis = {}
  
  uis.BackGroundLoader = ui:GetChild("BackGroundLoader")
  uis.BackGroundHolder = ui:GetChild("BackGroundHolder")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_BadgeBtnByName.lua.lua
**Functions:**
- GetCommonResource_BadgeBtnUis
**Snippet:**
```lua
function GetCommonResource_BadgeBtnUis(ui)
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

## BCD/CommonResource_BadgeFrameByName.lua.lua
**Functions:**
- GetCommonResource_BadgeFrameUis
**Snippet:**
```lua
function GetCommonResource_BadgeFrameUis(ui)
  local uis = {}
  
  uis.HeadLoader = ui:GetChild("HeadLoader")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_BadgeHeadShowBgByName.lua.lua
**Functions:**
- GetCommonResource_BadgeHeadShowBgUis
**Snippet:**
```lua
function GetCommonResource_BadgeHeadShowBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_BadgeHeadShowByName.lua.lua
**Functions:**
- GetCommonResource_BadgeHeadShowUis
**Requires:**
- CommonResource_BadgeHeadShowBgByName
**Snippet:**
```lua
require("CommonResource_BadgeHeadShowBgByName")

function GetCommonResource_BadgeHeadShowUis(ui)
  local uis = {}
  uis.HeadShowBg = GetCommonResource_BadgeHeadShowBgUis(ui:GetChild("HeadShowBg"))
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_BtnGroupByName.lua.lua
**Functions:**
- GetCommonResource_BtnGroupUis
**Snippet:**
```lua
function GetCommonResource_BtnGroupUis(ui)
  local uis = {}
  
  uis.Popup_B_Green_Btn = ui:GetChild("Popup_B_Green_Btn")
  uis.Popup_S_Black_Btn = ui:GetChild("Popup_S_Black_Btn")
  uis.Popup_S_Green_Btn = ui:GetChild("Popup_S_Green_Btn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_BuffIconBarByName.lua.lua
**Functions:**
- GetCommonResource_BuffIconBarUis
**Snippet:**
```lua
function GetCommonResource_BuffIconBarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_BuildFrame_RByName.lua.lua
**Functions:**
- GetCommonResource_BuildFrame_RUis
**Requires:**
- CommonResource_BuildPicByName
- CommonResource_HeadFrameStateByName
- CommonResource_ArenaDefendNewByName
**Snippet:**
```lua
require("CommonResource_BuildPicByName")
require("CommonResource_HeadFrameStateByName")
require("CommonResource_ArenaDefendNewByName")

function GetCommonResource_BuildFrame_RUis(ui)
  local uis = {}
  uis.BuildPic = GetCommonResource_BuildPicUis(ui:GetChild("BuildPic"))
  uis.ElementList = ui:GetChild("ElementList")
  uis.State = GetCommonResource_HeadFrameStateUis(ui:GetChild("State"))
  uis.BuildTxt = ui:GetChild("BuildTxt")
```

---

## BCD/CommonResource_BuildPicByName.lua.lua
**Functions:**
- GetCommonResource_BuildPicUis
**Snippet:**
```lua
function GetCommonResource_BuildPicUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_BurstSkillNameByName.lua.lua
**Functions:**
- GetCommonResource_BurstSkillNameUis
**Snippet:**
```lua
function GetCommonResource_BurstSkillNameUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Button_Green_2_BtnByName.lua.lua
**Functions:**
- GetCommonResource_Button_Green_2_BtnUis
**Snippet:**
```lua
function GetCommonResource_Button_Green_2_BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Button_Green_3_BtnByName.lua.lua
**Functions:**
- GetCommonResource_Button_Green_3_BtnUis
**Snippet:**
```lua
function GetCommonResource_Button_Green_3_BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Button_White_2_BtnByName.lua.lua
**Functions:**
- GetCommonResource_Button_White_2_BtnUis
**Snippet:**
```lua
function GetCommonResource_Button_White_2_BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Button_White_3_BtnByName.lua.lua
**Functions:**
- GetCommonResource_Button_White_3_BtnUis
**Snippet:**
```lua
function GetCommonResource_Button_White_3_BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_CardBreachByName.lua.lua
**Functions:**
- GetCommonResource_CardBreachUis
**Snippet:**
```lua
function GetCommonResource_CardBreachUis(ui)
  local uis = {}
  
  uis.BreachHolder = ui:GetChild("BreachHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_CardBtnByName.lua.lua
**Functions:**
- GetCommonResource_CardBtnUis
**Snippet:**
```lua
function GetCommonResource_CardBtnUis(ui)
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

## BCD/CommonResource_CardGetNewByName.lua.lua
**Functions:**
- GetCommonResource_CardGetNewUis
**Snippet:**
```lua
function GetCommonResource_CardGetNewUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_CardTypeByName.lua.lua
**Functions:**
- GetCommonResource_CardTypeUis
**Snippet:**
```lua
function GetCommonResource_CardTypeUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_ChatByName.lua.lua
**Functions:**
- GetCommonResource_ChatUis
**Snippet:**
```lua
function GetCommonResource_ChatUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_CurrencyIndex1ByName.lua.lua
**Functions:**
- GetCommonResource_CurrencyIndex1Uis
**Requires:**
- CommonResource_Index1ByName
**Snippet:**
```lua
require("CommonResource_Index1ByName")

function GetCommonResource_CurrencyIndex1Uis(ui)
  local uis = {}
  uis.CurrencyIndex1 = GetCommonResource_Index1Uis(ui:GetChild("CurrencyIndex1"))
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_CurrencyIndex2ByName.lua.lua
**Functions:**
- GetCommonResource_CurrencyIndex2Uis
**Requires:**
- CommonResource_CurrencyIndex1ByName
**Snippet:**
```lua
require("CommonResource_CurrencyIndex1ByName")

function GetCommonResource_CurrencyIndex2Uis(ui)
  local uis = {}
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.CurrencyIndex1 = GetCommonResource_CurrencyIndex1Uis(ui:GetChild("CurrencyIndex1"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_CurrencyReturnByName.lua.lua
**Functions:**
- GetCommonResource_CurrencyReturnUis
**Requires:**
- CommonResource_CurrencyIndex2ByName
**Snippet:**
```lua
require("CommonResource_CurrencyIndex2ByName")

function GetCommonResource_CurrencyReturnUis(ui)
  local uis = {}
  uis.CurrencyIndex2 = GetCommonResource_CurrencyIndex2Uis(ui:GetChild("CurrencyIndex2"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.FunctionMainBtn = ui:GetChild("FunctionMainBtn")
  uis.FunctionJumpBtn = ui:GetChild("FunctionJumpBtn")
  uis.FunctionDetailsBtn = ui:GetChild("FunctionDetailsBtn")
  uis.c1Ctr = ui:GetController("c1")
```

---

## BCD/CommonResource_DefenseBarByName.lua.lua
**Functions:**
- GetCommonResource_DefenseBarUis
**Requires:**
- CommonResource_DefenseFillBackByName
- CommonResource_DefenseFillByName
**Snippet:**
```lua
require("CommonResource_DefenseFillBackByName")
require("CommonResource_DefenseFillByName")

function GetCommonResource_DefenseBarUis(ui)
  local uis = {}
  uis.bar_delay1 = GetCommonResource_DefenseFillBackUis(ui:GetChild("bar_delay1"))
  uis.bar = GetCommonResource_DefenseFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_DefenseFillBackByName.lua.lua
**Functions:**
- GetCommonResource_DefenseFillBackUis
**Snippet:**
```lua
function GetCommonResource_DefenseFillBackUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_DefenseFillByName.lua.lua
**Functions:**
- GetCommonResource_DefenseFillUis
**Snippet:**
```lua
function GetCommonResource_DefenseFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_ElementByName.lua.lua
**Functions:**
- GetCommonResource_ElementUis
**Snippet:**
```lua
function GetCommonResource_ElementUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Firm1BarByName.lua.lua
**Functions:**
- GetCommonResource_Firm1BarUis
**Requires:**
- CommonResource_Firm1FillByName
**Snippet:**
```lua
require("CommonResource_Firm1FillByName")

function GetCommonResource_Firm1BarUis(ui)
  local uis = {}
  uis.bar = GetCommonResource_Firm1FillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Firm1FillByName.lua.lua
**Functions:**
- GetCommonResource_Firm1FillUis
**Snippet:**
```lua
function GetCommonResource_Firm1FillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Firm2BarByName.lua.lua
**Functions:**
- GetCommonResource_Firm2BarUis
**Requires:**
- CommonResource_Firm2FillByName
**Snippet:**
```lua
require("CommonResource_Firm2FillByName")

function GetCommonResource_Firm2BarUis(ui)
  local uis = {}
  uis.bar = GetCommonResource_Firm2FillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Firm2FillByName.lua.lua
**Functions:**
- GetCommonResource_Firm2FillUis
**Snippet:**
```lua
function GetCommonResource_Firm2FillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_FirmBarByName.lua.lua
**Functions:**
- GetCommonResource_FirmBarUis
**Requires:**
- CommonResource_FirmFillByName
**Snippet:**
```lua
require("CommonResource_FirmFillByName")

function GetCommonResource_FirmBarUis(ui)
  local uis = {}
  uis.bar = GetCommonResource_FirmFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_FirmFillByName.lua.lua
**Functions:**
- GetCommonResource_FirmFillUis
**Snippet:**
```lua
function GetCommonResource_FirmFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_FormationProgressBarByName.lua.lua
**Functions:**
- GetCommonResource_FormationProgressBarUis
**Snippet:**
```lua
function GetCommonResource_FormationProgressBarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_FormationProgressFillByName.lua.lua
**Functions:**
- GetCommonResource_FormationProgressFillUis
**Snippet:**
```lua
function GetCommonResource_FormationProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_FunctionDetailsBtnByName.lua.lua
**Functions:**
- GetCommonResource_FunctionDetailsBtnUis
**Snippet:**
```lua
function GetCommonResource_FunctionDetailsBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_FunctionJumpBtnByName.lua.lua
**Functions:**
- GetCommonResource_FunctionJumpBtnUis
**Snippet:**
```lua
function GetCommonResource_FunctionJumpBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_FunctionMainBtnByName.lua.lua
**Functions:**
- GetCommonResource_FunctionMainBtnUis
**Snippet:**
```lua
function GetCommonResource_FunctionMainBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_GuildBossCardSignByName.lua.lua
**Functions:**
- GetCommonResource_GuildBossCardSignUis
**Snippet:**
```lua
function GetCommonResource_GuildBossCardSignUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_GuildByName.lua.lua
**Functions:**
- GetCommonResource_GuildUis
**Snippet:**
```lua
function GetCommonResource_GuildUis(ui)
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

## BCD/CommonResource_HeadBgByName.lua.lua
**Functions:**
- GetCommonResource_HeadBgUis
**Snippet:**
```lua
function GetCommonResource_HeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_HeadBtnByName.lua.lua
**Functions:**
- GetCommonResource_HeadBtnUis
**Requires:**
- CommonResource_CardTypeByName
**Snippet:**
```lua
require("CommonResource_CardTypeByName")

function GetCommonResource_HeadBtnUis(ui)
  local uis = {}
  uis.PlayerHead = GetCommonResource_CardTypeUis(ui:GetChild("PlayerHead"))
  uis.MonsterLoader = ui:GetChild("MonsterLoader")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
```

---

## BCD/CommonResource_HeadByName.lua.lua
**Functions:**
- GetCommonResource_HeadUis
**Requires:**
- CommonResource_HeadBgByName
**Snippet:**
```lua
require("CommonResource_HeadBgByName")

function GetCommonResource_HeadUis(ui)
  local uis = {}
  uis.HeadBg = GetCommonResource_HeadBgUis(ui:GetChild("HeadBg"))
  uis.FrameLoader = ui:GetChild("FrameLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_HeadFrameStateByName.lua.lua
**Functions:**
- GetCommonResource_HeadFrameStateUis
**Snippet:**
```lua
function GetCommonResource_HeadFrameStateUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_HeadFrameWaveByName.lua.lua
**Functions:**
- GetCommonResource_HeadFrameWaveUis
**Snippet:**
```lua
function GetCommonResource_HeadFrameWaveUis(ui)
  local uis = {}
  
  uis.WaveTxt = ui:GetChild("WaveTxt")
  uis.c4Ctr = ui:GetController("c4")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_HeadFrame_RByName.lua.lua
**Functions:**
- GetCommonResource_HeadFrame_RUis
**Requires:**
- CommonResource_PicMaskByName
- CommonResource_OccupationByName
- CommonResource_CardBreachByName
- CommonResource_HeadFrameStateByName
- CommonResource_HeadFrameWaveByName
**Snippet:**
```lua
require("CommonResource_PicMaskByName")
require("CommonResource_OccupationByName")
require("CommonResource_CardBreachByName")
require("CommonResource_HeadFrameStateByName")
require("CommonResource_HeadFrameWaveByName")

function GetCommonResource_HeadFrame_RUis(ui)
  local uis = {}
  uis.PicMask = GetCommonResource_PicMaskUis(ui:GetChild("PicMask"))
  uis.LevelTxt = ui:GetChild("LevelTxt")
```

---

## BCD/CommonResource_HpBarByName.lua.lua
**Functions:**
- GetCommonResource_HpBarUis
**Requires:**
- CommonResource_HpFillBackByName
- CommonResource_HpFillByName
**Snippet:**
```lua
require("CommonResource_HpFillBackByName")
require("CommonResource_HpFillByName")

function GetCommonResource_HpBarUis(ui)
  local uis = {}
  uis.bar_delay = GetCommonResource_HpFillBackUis(ui:GetChild("bar_delay"))
  uis.bar = GetCommonResource_HpFillUis(ui:GetChild("bar"))
  uis.FirmProgressBar = ui:GetChild("FirmProgressBar")
  uis.SoulProgressBar = ui:GetChild("SoulProgressBar")
  uis.delayCtr = ui:GetController("delay")
```

---

## BCD/CommonResource_HpBossBarByName.lua.lua
**Functions:**
- GetCommonResource_HpBossBarUis
**Requires:**
- CommonResource_HpBossFillBackByName
- CommonResource_HpBossFillByName
**Snippet:**
```lua
require("CommonResource_HpBossFillBackByName")
require("CommonResource_HpBossFillByName")

function GetCommonResource_HpBossBarUis(ui)
  local uis = {}
  uis.bar_delay = GetCommonResource_HpBossFillBackUis(ui:GetChild("bar_delay"))
  uis.bar = GetCommonResource_HpBossFillUis(ui:GetChild("bar"))
  uis.FirmProgressBar = ui:GetChild("FirmProgressBar")
  uis.delayCtr = ui:GetController("delay")
  uis.root = ui
```

---

## BCD/CommonResource_HpBossFillBackByName.lua.lua
**Functions:**
- GetCommonResource_HpBossFillBackUis
**Snippet:**
```lua
function GetCommonResource_HpBossFillBackUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_HpBossFillByName.lua.lua
**Functions:**
- GetCommonResource_HpBossFillUis
**Snippet:**
```lua
function GetCommonResource_HpBossFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_HpBuildBarByName.lua.lua
**Functions:**
- GetCommonResource_HpBuildBarUis
**Requires:**
- CommonResource_HpBuildFillBackByName
- CommonResource_HpBuildFillByName
- CommonResource_ScaleStripByName
**Snippet:**
```lua
require("CommonResource_HpBuildFillBackByName")
require("CommonResource_HpBuildFillByName")
require("CommonResource_ScaleStripByName")

function GetCommonResource_HpBuildBarUis(ui)
  local uis = {}
  uis.bar_delay = GetCommonResource_HpBuildFillBackUis(ui:GetChild("bar_delay"))
  uis.bar = GetCommonResource_HpBuildFillUis(ui:GetChild("bar"))
  uis.ScaleStrip = GetCommonResource_ScaleStripUis(ui:GetChild("ScaleStrip"))
  uis.FirmProgressBar = ui:GetChild("FirmProgressBar")
```

---

## BCD/CommonResource_HpBuildFillBackByName.lua.lua
**Functions:**
- GetCommonResource_HpBuildFillBackUis
**Snippet:**
```lua
function GetCommonResource_HpBuildFillBackUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_HpBuildFillByName.lua.lua
**Functions:**
- GetCommonResource_HpBuildFillUis
**Snippet:**
```lua
function GetCommonResource_HpBuildFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_HpEliteBarByName.lua.lua
**Functions:**
- GetCommonResource_HpEliteBarUis
**Requires:**
- CommonResource_HpEliteFillBackByName
- CommonResource_HpEliteFillByName
**Snippet:**
```lua
require("CommonResource_HpEliteFillBackByName")
require("CommonResource_HpEliteFillByName")

function GetCommonResource_HpEliteBarUis(ui)
  local uis = {}
  uis.bar_delay = GetCommonResource_HpEliteFillBackUis(ui:GetChild("bar_delay"))
  uis.bar = GetCommonResource_HpEliteFillUis(ui:GetChild("bar"))
  uis.FirmProgressBar = ui:GetChild("FirmProgressBar")
  uis.delayCtr = ui:GetController("delay")
  uis.root = ui
```

---

## BCD/CommonResource_HpEliteFillBackByName.lua.lua
**Functions:**
- GetCommonResource_HpEliteFillBackUis
**Snippet:**
```lua
function GetCommonResource_HpEliteFillBackUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_HpEliteFillByName.lua.lua
**Functions:**
- GetCommonResource_HpEliteFillUis
**Snippet:**
```lua
function GetCommonResource_HpEliteFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_HpFillBackByName.lua.lua
**Functions:**
- GetCommonResource_HpFillBackUis
**Snippet:**
```lua
function GetCommonResource_HpFillBackUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_HpFillByName.lua.lua
**Functions:**
- GetCommonResource_HpFillUis
**Snippet:**
```lua
function GetCommonResource_HpFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_HpMonsterBarByName.lua.lua
**Functions:**
- GetCommonResource_HpMonsterBarUis
**Requires:**
- CommonResource_HpMonsterFillBackByName
- CommonResource_HpMonsterFillByName
**Snippet:**
```lua
require("CommonResource_HpMonsterFillBackByName")
require("CommonResource_HpMonsterFillByName")

function GetCommonResource_HpMonsterBarUis(ui)
  local uis = {}
  uis.bar_delay = GetCommonResource_HpMonsterFillBackUis(ui:GetChild("bar_delay"))
  uis.bar = GetCommonResource_HpMonsterFillUis(ui:GetChild("bar"))
  uis.FirmProgressBar = ui:GetChild("FirmProgressBar")
  uis.delayCtr = ui:GetController("delay")
  uis.root = ui
```

---

## BCD/CommonResource_HpMonsterFillBackByName.lua.lua
**Functions:**
- GetCommonResource_HpMonsterFillBackUis
**Snippet:**
```lua
function GetCommonResource_HpMonsterFillBackUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_HpMonsterFillByName.lua.lua
**Functions:**
- GetCommonResource_HpMonsterFillUis
**Snippet:**
```lua
function GetCommonResource_HpMonsterFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Index1ByName.lua.lua
**Functions:**
- GetCommonResource_Index1Uis
**Snippet:**
```lua
function GetCommonResource_Index1Uis(ui)
  local uis = {}
  
  uis.AdventureBtn = ui:GetChild("AdventureBtn")
  uis.BadgeBtn = ui:GetChild("BadgeBtn")
  uis.CardBtn = ui:GetChild("CardBtn")
  uis.GuildBtn = ui:GetChild("GuildBtn")
  uis.LotteryBtn = ui:GetChild("LotteryBtn")
  uis.ShopBtn = ui:GetChild("ShopBtn")
  uis.StoryBtn = ui:GetChild("StoryBtn")
```

---

## BCD/CommonResource_ItemCardPicByName.lua.lua
**Functions:**
- GetCommonResource_ItemCardPicUis
**Snippet:**
```lua
function GetCommonResource_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_ItemFrameBtnByName.lua.lua
**Functions:**
- GetCommonResource_ItemFrameBtnUis
**Requires:**
- CommonResource_ItemFrameByName
**Snippet:**
```lua
require("CommonResource_ItemFrameByName")

function GetCommonResource_ItemFrameBtnUis(ui)
  local uis = {}
  uis.ItemFrame = GetCommonResource_ItemFrameUis(ui:GetChild("ItemFrame"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_ItemFrameByName.lua.lua
**Functions:**
- GetCommonResource_ItemFrameUis
**Requires:**
- CommonResource_ItemCardPicByName
- CommonResource_ItemTimeByName
- CommonResource_ItemSweepByName
- CommonResource_BadgeHeadShowByName
**Snippet:**
```lua
require("CommonResource_ItemCardPicByName")
require("CommonResource_ItemTimeByName")
require("CommonResource_ItemSweepByName")
require("CommonResource_BadgeHeadShowByName")

function GetCommonResource_ItemFrameUis(ui)
  local uis = {}
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.ItemCardPic = GetCommonResource_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
```

---

## BCD/CommonResource_ItemSweepByName.lua.lua
**Functions:**
- GetCommonResource_ItemSweepUis
**Snippet:**
```lua
function GetCommonResource_ItemSweepUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_ItemSynthesisBarByName.lua.lua
**Functions:**
- GetCommonResource_ItemSynthesisBarUis
**Requires:**
- CommonResource_ItemSynthesisFillByName
**Snippet:**
```lua
require("CommonResource_ItemSynthesisFillByName")

function GetCommonResource_ItemSynthesisBarUis(ui)
  local uis = {}
  uis.bar = GetCommonResource_ItemSynthesisFillUis(ui:GetChild("bar"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_ItemSynthesisFillByName.lua.lua
**Functions:**
- GetCommonResource_ItemSynthesisFillUis
**Snippet:**
```lua
function GetCommonResource_ItemSynthesisFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_ItemTimeByName.lua.lua
**Functions:**
- GetCommonResource_ItemTimeUis
**Snippet:**
```lua
function GetCommonResource_ItemTimeUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_ListRedDot1ByName.lua.lua
**Functions:**
- GetCommonResource_ListRedDot1Uis
**Snippet:**
```lua
function GetCommonResource_ListRedDot1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_ListRedDotByName.lua.lua
**Functions:**
- GetCommonResource_ListRedDotUis
**Snippet:**
```lua
function GetCommonResource_ListRedDotUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_LotteryByName.lua.lua
**Functions:**
- GetCommonResource_LotteryUis
**Snippet:**
```lua
function GetCommonResource_LotteryUis(ui)
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

## BCD/CommonResource_LotteryFreeByName.lua.lua
**Functions:**
- GetCommonResource_LotteryFreeUis
**Snippet:**
```lua
function GetCommonResource_LotteryFreeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_LotteryFreeTimeByName.lua.lua
**Functions:**
- GetCommonResource_LotteryFreeTimeUis
**Snippet:**
```lua
function GetCommonResource_LotteryFreeTimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_MultipleByName.lua.lua
**Functions:**
- GetCommonResource_MultipleUis
**Snippet:**
```lua
function GetCommonResource_MultipleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_NewByName.lua.lua
**Functions:**
- GetCommonResource_NewUis
**Snippet:**
```lua
function GetCommonResource_NewUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_OccupationByName.lua.lua
**Functions:**
- GetCommonResource_OccupationUis
**Snippet:**
```lua
function GetCommonResource_OccupationUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_PicMaskByName.lua.lua
**Functions:**
- GetCommonResource_PicMaskUis
**Snippet:**
```lua
function GetCommonResource_PicMaskUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_PlayerBuffByName.lua.lua
**Functions:**
- GetCommonResource_PlayerBuffUis
**Snippet:**
```lua
function GetCommonResource_PlayerBuffUis(ui)
  local uis = {}
  
  uis.BuffLoader = ui:GetChild("BuffLoader")
  uis.BuffIconProgressBar = ui:GetChild("BuffIconProgressBar")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_PlayerHeadByName.lua.lua
**Functions:**
- GetCommonResource_PlayerHeadUis
**Requires:**
- CommonResource_Quality1_1ByName
- CommonResource_Quality1_2ByName
**Snippet:**
```lua
require("CommonResource_Quality1_1ByName")
require("CommonResource_Quality1_2ByName")

function GetCommonResource_PlayerHeadUis(ui)
  local uis = {}
  uis.Quality1_1 = GetCommonResource_Quality1_1Uis(ui:GetChild("Quality1_1"))
  uis.HeadLoader = ui:GetChild("HeadLoader")
  uis.Quality1_2 = GetCommonResource_Quality1_2Uis(ui:GetChild("Quality1_2"))
  uis.root = ui
  return uis
```

---

## BCD/CommonResource_PlayerHPByName.lua.lua
**Functions:**
- GetCommonResource_PlayerHPUis
**Snippet:**
```lua
function GetCommonResource_PlayerHPUis(ui)
  local uis = {}
  
  uis.RageProgressBar = ui:GetChild("RageProgressBar")
  uis.HpProgressBar = ui:GetChild("HpProgressBar")
  uis.HpMonsterProgressBar = ui:GetChild("HpMonsterProgressBar")
  uis.HpEliteProgressBar = ui:GetChild("HpEliteProgressBar")
  uis.HpBossProgressBar = ui:GetChild("HpBossProgressBar")
  uis.HpBuildProgressBar = ui:GetChild("HpBuildProgressBar")
  uis.DefenseProgressBar = ui:GetChild("DefenseProgressBar")
```

---

## BCD/CommonResource_PlotDungeonByName.lua.lua
**Functions:**
- GetCommonResource_PlotDungeonUis
**Snippet:**
```lua
function GetCommonResource_PlotDungeonUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_PointerByName.lua.lua
**Functions:**
- GetCommonResource_PointerUis
**Snippet:**
```lua
function GetCommonResource_PointerUis(ui)
  local uis = {}
  
  uis.PointerLoader = ui:GetChild("PointerLoader")
  uis.PointerHolder = ui:GetChild("PointerHolder")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_PopupBgByName.lua.lua
**Functions:**
- GetCommonResource_PopupBgUis
**Snippet:**
```lua
function GetCommonResource_PopupBgUis(ui)
  local uis = {}
  
  uis.BlurLoader = ui:GetChild("BlurLoader")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Popup_BByName.lua.lua
**Functions:**
- GetCommonResource_Popup_BUis
**Requires:**
- CommonResource_BtnGroupByName
**Snippet:**
```lua
require("CommonResource_BtnGroupByName")

function GetCommonResource_Popup_BUis(ui)
  local uis = {}
  uis.BtnGroup = GetCommonResource_BtnGroupUis(ui:GetChild("BtnGroup"))
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Popup_B_Green_BtnByName.lua.lua
**Functions:**
- GetCommonResource_Popup_B_Green_BtnUis
**Snippet:**
```lua
function GetCommonResource_Popup_B_Green_BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Popup_OpalByName.lua.lua
**Functions:**
- GetCommonResource_Popup_OpalUis
**Requires:**
- CommonResource_BtnGroupByName
**Snippet:**
```lua
require("CommonResource_BtnGroupByName")

function GetCommonResource_Popup_OpalUis(ui)
  local uis = {}
  uis.BtnGroup = GetCommonResource_BtnGroupUis(ui:GetChild("BtnGroup"))
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Popup_SByName.lua.lua
**Functions:**
- GetCommonResource_Popup_SUis
**Snippet:**
```lua
function GetCommonResource_Popup_SUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Popup_S_Black_BtnByName.lua.lua
**Functions:**
- GetCommonResource_Popup_S_Black_BtnUis
**Snippet:**
```lua
function GetCommonResource_Popup_S_Black_BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Popup_S_Green_BtnByName.lua.lua
**Functions:**
- GetCommonResource_Popup_S_Green_BtnUis
**Snippet:**
```lua
function GetCommonResource_Popup_S_Green_BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Quality1_1ByName.lua.lua
**Functions:**
- GetCommonResource_Quality1_1Uis
**Snippet:**
```lua
function GetCommonResource_Quality1_1Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_Quality1_2ByName.lua.lua
**Functions:**
- GetCommonResource_Quality1_2Uis
**Snippet:**
```lua
function GetCommonResource_Quality1_2Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_RaidBossByName.lua.lua
**Functions:**
- GetCommonResource_RaidBossUis
**Snippet:**
```lua
function GetCommonResource_RaidBossUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_RedDotByName.lua.lua
**Functions:**
- GetCommonResource_RedDotUis
**Snippet:**
```lua
function GetCommonResource_RedDotUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_ReturnBtnByName.lua.lua
**Functions:**
- GetCommonResource_ReturnBtnUis
**Snippet:**
```lua
function GetCommonResource_ReturnBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_ScaleByName.lua.lua
**Functions:**
- GetCommonResource_ScaleUis
**Snippet:**
```lua
function GetCommonResource_ScaleUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_ScaleStripByName.lua.lua
**Functions:**
- GetCommonResource_ScaleStripUis
**Snippet:**
```lua
function GetCommonResource_ScaleStripUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_ShopBtnByName.lua.lua
**Functions:**
- GetCommonResource_ShopBtnUis
**Snippet:**
```lua
function GetCommonResource_ShopBtnUis(ui)
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

## BCD/CommonResource_SkillByName.lua.lua
**Functions:**
- GetCommonResource_SkillUis
**Snippet:**
```lua
function GetCommonResource_SkillUis(ui)
  local uis = {}
  
  uis.IconLoader = ui:GetChild("IconLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_SkillDetailsCDByName.lua.lua
**Functions:**
- GetCommonResource_SkillDetailsCDUis
**Snippet:**
```lua
function GetCommonResource_SkillDetailsCDUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_SkillDetailsTag1ByName.lua.lua
**Functions:**
- GetCommonResource_SkillDetailsTag1Uis
**Snippet:**
```lua
function GetCommonResource_SkillDetailsTag1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_SkillDetailsTagByName.lua.lua
**Functions:**
- GetCommonResource_SkillDetailsTagUis
**Snippet:**
```lua
function GetCommonResource_SkillDetailsTagUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_SkillLockByName.lua.lua
**Functions:**
- GetCommonResource_SkillLockUis
**Snippet:**
```lua
function GetCommonResource_SkillLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_SoulBarByName.lua.lua
**Functions:**
- GetCommonResource_SoulBarUis
**Requires:**
- CommonResource_SoulFillByName
**Snippet:**
```lua
require("CommonResource_SoulFillByName")

function GetCommonResource_SoulBarUis(ui)
  local uis = {}
  uis.bar = GetCommonResource_SoulFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_SoulFillByName.lua.lua
**Functions:**
- GetCommonResource_SoulFillUis
**Snippet:**
```lua
function GetCommonResource_SoulFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_StarByName.lua.lua
**Functions:**
- GetCommonResource_StarUis
**Snippet:**
```lua
function GetCommonResource_StarUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_StarCardUseByName.lua.lua
**Functions:**
- GetCommonResource_StarCardUseUis
**Snippet:**
```lua
function GetCommonResource_StarCardUseUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_StarRedDot1ByName.lua.lua
**Functions:**
- GetCommonResource_StarRedDot1Uis
**Snippet:**
```lua
function GetCommonResource_StarRedDot1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_StarRedDotByName.lua.lua
**Functions:**
- GetCommonResource_StarRedDotUis
**Snippet:**
```lua
function GetCommonResource_StarRedDotUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_StoryByName.lua.lua
**Functions:**
- GetCommonResource_StoryUis
**Snippet:**
```lua
function GetCommonResource_StoryUis(ui)
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

## BCD/CommonResource_TaskBtnByName.lua.lua
**Functions:**
- GetCommonResource_TaskBtnUis
**Snippet:**
```lua
function GetCommonResource_TaskBtnUis(ui)
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

## BCD/CommonResource_TitleBtnByName.lua.lua
**Functions:**
- GetCommonResource_TitleBtnUis
**Snippet:**
```lua
function GetCommonResource_TitleBtnUis(ui)
  local uis = {}
  
  uis.TitleImage = ui:GetChild("TitleImage")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_TouchScreenBtnByName.lua.lua
**Functions:**
- GetCommonResource_TouchScreenBtnUis
**Snippet:**
```lua
function GetCommonResource_TouchScreenBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_TowerByName.lua.lua
**Functions:**
- GetCommonResource_TowerUis
**Snippet:**
```lua
function GetCommonResource_TowerUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_VerticalScroll1BarByName.lua.lua
**Functions:**
- GetCommonResource_VerticalScroll1BarUis
**Snippet:**
```lua
function GetCommonResource_VerticalScroll1BarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_VerticalScroll1Bar_gripByName.lua.lua
**Functions:**
- GetCommonResource_VerticalScroll1Bar_gripUis
**Snippet:**
```lua
function GetCommonResource_VerticalScroll1Bar_gripUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_VerticalScrollBarByName.lua.lua
**Functions:**
- GetCommonResource_VerticalScrollBarUis
**Snippet:**
```lua
function GetCommonResource_VerticalScrollBarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/CommonResource_VerticalScrollBar_gripByName.lua.lua
**Functions:**
- GetCommonResource_VerticalScrollBar_gripUis
**Snippet:**
```lua
function GetCommonResource_VerticalScrollBar_gripUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/ComplaintWindow.lua.lua
**Functions:**
- ComplaintWindow.ReInitData
- ComplaintWindow.OnInit
- ComplaintWindow.UpdateInfo
- ComplaintWindow.InitBtn
- ComplaintWindow.ClickSureBtn
- ComplaintWindow.ClickCloseBtn
- ComplaintWindow.OnShown
- ComplaintWindow.OnHide
- ComplaintWindow.OnClose
- ComplaintWindow.HandleMessage
**Requires:**
- Chat_ComplaintWindowByName
**Snippet:**
```lua
require("Chat_ComplaintWindowByName")
local ComplaintWindow = {}
local uis, contentPane, actorInfo, msg
local selectReason = {}

function ComplaintWindow.ReInitData()
end

function ComplaintWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ComplaintWindow.package, WinResConfig.ComplaintWindow.comName, function(com)
```

---

## BCD/Create.lua.lua
**Functions:**
- Create
- class.New
- create
- inst:Delete
**Snippet:**
```lua
local _Class = {}
ClassType = {Class = 1, Instance = 2}

function Create(className, base)
  assert(type(className) == "string" and #className > 0)
  local class = {}
  class.__ctor = false
  class.__delete = false
  class.__cname = className
  class.__ctype = ClassType.Class
```

---

## BCD/CurrencyReturnWindow.lua.lua
**Functions:**
- CurrencyReturnWindow.AutoOpenCaption
- CurrencyReturnWindow.SetCurrencyReturn
- obj.Close
- obj.InitJump
- obj.InitBtn
- obj.HideWin
- CurrencyReturnWindow.SetJumpFun
- CurrencyReturnWindow.EnterWindow
- CurrencyReturnWindow.jumpAbyssExplore
- CurrencyReturnWindow.jumpAbyssShop
- CurrencyReturnWindow.jumpAbyssSealShop
- CurrencyReturnWindow.jumpAbyssMaterialTransaction
- CurrencyReturnWindow.jumpAbyssExpedition
- CurrencyReturnWindow.jumpAbyssBuilding
- CurrencyReturnWindow.jumpAbyssSealDungeon
- CurrencyReturnWindow.jumpBadgeDecompose
- CurrencyReturnWindow.jumpCardList
- CurrencyReturnWindow.jumpAdventure
- CurrencyReturnWindow.jumpTower
- CurrencyReturnWindow.jumpExperiment
- CurrencyReturnWindow.GetTrialDataByFeatureId
- CurrencyReturnWindow.jumpTrial
- CurrencyReturnWindow.jumpMainLine
- CurrencyReturnWindow.jumpBoss
- CurrencyReturnWindow.jumpMail
- CurrencyReturnWindow.jumpArena
- CurrencyReturnWindow.jumpPassport
- CurrencyReturnWindow.jumpGuild
- CurrencyReturnWindow.jumpLottery
- CurrencyReturnWindow.jumpCarnival
- CurrencyReturnWindow.jumpDayTask
- CurrencyReturnWindow.jumpFriend
- CurrencyReturnWindow.jumpSetting
- CurrencyReturnWindow.jumpLookRole
- CurrencyReturnWindow.jumpBadge
- CurrencyReturnWindow.jumpTakePhoto
- CurrencyReturnWindow.jumpBiography
- CurrencyReturnWindow.jumpChat
- CurrencyReturnWindow.jumpExplore
- CurrencyReturnWindow.jumpNotice
- CurrencyReturnWindow.jumpTaskList
- CurrencyReturnWindow.jumpStory
- CurrencyReturnWindow.jumpShop
- CurrencyReturnWindow.jumpItemShopOne
- CurrencyReturnWindow.jumpItemShopTwe
- CurrencyReturnWindow.jumpActivityItemDungeon
- CurrencyReturnWindow.jumpActivityMinGame
- CurrencyReturnWindow.jumpActivityTwoItemDungeon
- CurrencyReturnWindow.jumpActivityTwoMinGame
- CurrencyReturnWindow.jumpGuildSign
- CurrencyReturnWindow.jumpActivityThreeMinGame
- CurrencyReturnWindow.jumpActivityThreeItemDungeon
- CurrencyReturnWindow.jumpActivityFourMinGame
- CurrencyReturnWindow.jumpActivityFourItemDungeon
- CurrencyReturnWindow.jumpActivityFiveMinGame
- CurrencyReturnWindow.jumpActivityFiveFishGame
- CurrencyReturnWindow.jumpActivityFiveItemDungeon
- CurrencyReturnWindow.jumpActivitySixMinGame
- CurrencyReturnWindow.jumpActivitySixItemDungeon
- CurrencyReturnWindow.jumpActivityTenMinGame
- CurrencyReturnWindow.jumpActivityTenItemDungeon
- CurrencyReturnWindow.jumpActivitySevenMinGame
- CurrencyReturnWindow.jumpActivitySevenItemDungeon
- CurrencyReturnWindow.jumpActivityEightMinGame
- CurrencyReturnWindow.jumpActivityEightItemDungeon
- CurrencyReturnWindow.jumpActivityNineMinGame
- CurrencyReturnWindow.jumpActivityNineSnakeFishGame
- CurrencyReturnWindow.jumpActivityNineItemDungeon
- CurrencyReturnWindow.jumpActivityTwelveMinGame
- CurrencyReturnWindow.jumpActivityTwelveItemDungeon
- CurrencyReturnWindow.jumpActivityElevenMinGame
- CurrencyReturnWindow.jumpActivityElevenItemDungeon
- CurrencyReturnWindow.jumpActivityThirteenMinGame
- CurrencyReturnWindow.jumpActivityThirteenCarGame
- CurrencyReturnWindow.jumpActivityThirteenItemDungeon
- CurrencyReturnWindow.jumpActivityFourteenMinGame
- CurrencyReturnWindow.jumpActivityFourteenItemDungeon
- CurrencyReturnWindow.jumpActivityFifteenMinGame
- CurrencyReturnWindow.jumpActivityFifteenItemDungeon
- CurrencyReturnWindow.jumpActivitySixteenMinGame
- CurrencyReturnWindow.jumpActivitySixteenItemDungeon
- CurrencyReturnWindow.jumpActivitySevenTeenMinGameOne
- CurrencyReturnWindow.jumpActivitySevenTeenMinGameTwo
- CurrencyReturnWindow.jumpActivitySevenTeenItemDungeon
- CurrencyReturnWindow.jumpActivityEighTeenMinGame
- CurrencyReturnWindow.jumpActivityEighTeenItemDungeon
- CurrencyReturnWindow.jumpActivityNineTeenMinGame
- CurrencyReturnWindow.jumpActivityNineTeenItemDungeon
- CurrencyReturnWindow.jumpActivityTwentyMinGame
- CurrencyReturnWindow.jumpActivityTwentyItemDungeon
- CurrencyReturnWindow.jumpActivitTwentyOneMinGame
- CurrencyReturnWindow.jumpActivityTwentyOneItemDungeon
- CurrencyReturnWindow.jumpActivitTwentyTwoMinGame
- CurrencyReturnWindow.jumpActivityTwentyTwoItemDungeon
**Snippet:**
```lua
CurrencyReturnWindow = {}

function CurrencyReturnWindow.AutoOpenCaption(featureId, root, detailsBtn)
  local data = TableData.GetConfig(featureId, "BaseFeature")
  if data and data.caption_id then
    if data.auto_open_caption and GuideData.CanShowCaption(data.id) then
      root.touchable = false
      LeanTween.delayedCall(data.caption_time and data.caption_time or 0.28, function()
        WindowLoadPackages[WinResConfig.GuidePicLookWindow.name] = {
          "Guide_" .. Language.curLanguage
```

---

## BCD/CurrencyWindow.lua.lua
**Functions:**
- CurrencyWindow.OnInit
- CurrencyWindow.UpdateTextDisplay
- CurrencyWindow.InitBtn
- sureBtnParam.touchCallback
- cancelBtnParam.touchCallback
- CurrencyWindow.CloseWindow
- CurrencyWindow.OnClose
- CurrencyWindow.HandleMessage
**Requires:**
- Message_CurrencyWindowByName
**Snippet:**
```lua
require("Message_CurrencyWindowByName")
local CurrencyWindow = {}
local uis, contentPane, msg

function CurrencyWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.CurrencyWindow.package, WinResConfig.CurrencyWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetMessage_CurrencyWindowUis(contentPane)
    if bridgeObj.argTable[1] then
```

---

## BCD/DailyDungeonWindow.lua.lua
**Functions:**
- DailyDungeonWindow.OnInit
- DailyDungeonWindow.InitDailyDungeonSceneInfoData
- DailyDungeonWindow.LoadBgTexture
- DailyDungeonWindow.InitList
- uis.Main.TipsList.itemRenderer
- DailyDungeonWindow.SetItemTouchable
- DailyDungeonWindow.ItemOnClick
- DailyDungeonWindow.ShowSelected
- DailyDungeonWindow.OpenMap
- DailyDungeonWindow.InitBtn
- DailyDungeonWindow.HandleMessage
- DailyDungeonWindow.OnClose
**Requires:**
- DailyDungeon_DailyDungeonWindowByName
**Snippet:**
```lua
require("DailyDungeon_DailyDungeonWindowByName")
local DailyDungeonWindow = {}
local uis, curIndex, contentPane, jumpTb, totalSceneData

function DailyDungeonWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.DailyDungeonWindow.package, WinResConfig.DailyDungeonWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetDailyDungeon_DailyDungeonWindowUis(contentPane)
    DailyDungeonWindow.LoadBgTexture()
```

---

## BCD/DailyDungeon_Badge1ByName.lua.lua
**Functions:**
- GetDailyDungeon_Badge1Uis
**Snippet:**
```lua
function GetDailyDungeon_Badge1Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyDungeon_Badge2ByName.lua.lua
**Functions:**
- GetDailyDungeon_Badge2Uis
**Snippet:**
```lua
function GetDailyDungeon_Badge2Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyDungeon_CircleByName.lua.lua
**Functions:**
- GetDailyDungeon_CircleUis
**Snippet:**
```lua
function GetDailyDungeon_CircleUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/DailyDungeon_DailyDungeonByName.lua.lua
**Functions:**
- GetDailyDungeon_DailyDungeonUis
**Requires:**
- CommonResource_BackGroundByName
- DailyDungeon_DailyEffectByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("DailyDungeon_DailyEffectByName")
require("CommonResource_CurrencyReturnByName")

function GetDailyDungeon_DailyDungeonUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Effect1 = GetDailyDungeon_DailyEffectUis(ui:GetChild("Effect1"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.Effect2 = GetDailyDungeon_DailyEffectUis(ui:GetChild("Effect2"))
```

---

## BCD/DailyDungeon_DailyDungeonWindowByName.lua.lua
**Functions:**
- GetDailyDungeon_DailyDungeonWindowUis
**Requires:**
- DailyDungeon_DailyDungeonByName
**Snippet:**
```lua
require("DailyDungeon_DailyDungeonByName")

function GetDailyDungeon_DailyDungeonWindowUis(ui)
  local uis = {}
  uis.Main = GetDailyDungeon_DailyDungeonUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/DailyDungeon_DailyEffectByName.lua.lua
**Functions:**
- GetDailyDungeon_DailyEffectUis
**Snippet:**
```lua
function GetDailyDungeon_DailyEffectUis(ui)
  local uis = {}
  
  uis.EffectLoader = ui:GetChild("EffectLoader")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyDungeon_DailyMapByName.lua.lua
**Functions:**
- GetDailyDungeon_DailyMapUis
**Requires:**
- CommonResource_BackGroundByName
- DailyDungeon_TabRegionByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("DailyDungeon_TabRegionByName")
require("CommonResource_CurrencyReturnByName")

function GetDailyDungeon_DailyMapUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.MapList = ui:GetChild("MapList")
  uis.TabRegion = GetDailyDungeon_TabRegionUis(ui:GetChild("TabRegion"))
  uis.CurrencyReturn = GetCommonResource_CurrencyReturnUis(ui:GetChild("CurrencyReturn"))
```

---

## BCD/DailyDungeon_DailyMapWindowByName.lua.lua
**Functions:**
- GetDailyDungeon_DailyMapWindowUis
**Requires:**
- DailyDungeon_DailyMapByName
**Snippet:**
```lua
require("DailyDungeon_DailyMapByName")

function GetDailyDungeon_DailyMapWindowUis(ui)
  local uis = {}
  uis.Main = GetDailyDungeon_DailyMapUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/DailyDungeon_DailyTipsBtnByName.lua.lua
**Functions:**
- GetDailyDungeon_DailyTipsBtnUis
**Requires:**
- DailyDungeon_DailyTipsPicByName
**Snippet:**
```lua
require("DailyDungeon_DailyTipsPicByName")

function GetDailyDungeon_DailyTipsBtnUis(ui)
  local uis = {}
  uis.DailyTipsPic = GetDailyDungeon_DailyTipsPicUis(ui:GetChild("DailyTipsPic"))
  uis.touchCtr = ui:GetController("touch")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyDungeon_DailyTipsPicByName.lua.lua
**Functions:**
- GetDailyDungeon_DailyTipsPicUis
**Requires:**
- DailyDungeon_DailyTipsWordByName
**Snippet:**
```lua
require("DailyDungeon_DailyTipsWordByName")

function GetDailyDungeon_DailyTipsPicUis(ui)
  local uis = {}
  uis.Line135Image = ui:GetChild("Line135Image")
  uis.Line24Image = ui:GetChild("Line24Image")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.DailyTipsWord = GetDailyDungeon_DailyTipsWordUis(ui:GetChild("DailyTipsWord"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
```

---

## BCD/DailyDungeon_DailyTipsWordByName.lua.lua
**Functions:**
- GetDailyDungeon_DailyTipsWordUis
**Requires:**
- DailyDungeon_TypeIcon1ByName
- DailyDungeon_TypeIcon2ByName
**Snippet:**
```lua
require("DailyDungeon_TypeIcon1ByName")
require("DailyDungeon_TypeIcon2ByName")

function GetDailyDungeon_DailyTipsWordUis(ui)
  local uis = {}
  uis.TypeIcon1 = GetDailyDungeon_TypeIcon1Uis(ui:GetChild("TypeIcon1"))
  uis.TypeIcon2 = GetDailyDungeon_TypeIcon2Uis(ui:GetChild("TypeIcon2"))
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## BCD/DailyDungeon_Map1ByName.lua.lua
**Functions:**
- GetDailyDungeon_Map1Uis
**Requires:**
- DailyDungeon_CircleByName
- DailyDungeon_MapTipsByName
**Snippet:**
```lua
require("DailyDungeon_CircleByName")
require("DailyDungeon_MapTipsByName")

function GetDailyDungeon_Map1Uis(ui)
  local uis = {}
  uis.Circle = GetDailyDungeon_CircleUis(ui:GetChild("Circle"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.Tips1 = GetDailyDungeon_MapTipsUis(ui:GetChild("Tips1"))
  uis.Tips2 = GetDailyDungeon_MapTipsUis(ui:GetChild("Tips2"))
  uis.Tips3 = GetDailyDungeon_MapTipsUis(ui:GetChild("Tips3"))
```

---

## BCD/DailyDungeon_Map2ByName.lua.lua
**Functions:**
- GetDailyDungeon_Map2Uis
**Requires:**
- DailyDungeon_CircleByName
- DailyDungeon_MapTipsByName
**Snippet:**
```lua
require("DailyDungeon_CircleByName")
require("DailyDungeon_MapTipsByName")

function GetDailyDungeon_Map2Uis(ui)
  local uis = {}
  uis.Circle = GetDailyDungeon_CircleUis(ui:GetChild("Circle"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.Tips1 = GetDailyDungeon_MapTipsUis(ui:GetChild("Tips1"))
  uis.Tips2 = GetDailyDungeon_MapTipsUis(ui:GetChild("Tips2"))
  uis.Tips3 = GetDailyDungeon_MapTipsUis(ui:GetChild("Tips3"))
```

---

## BCD/DailyDungeon_Map3ByName.lua.lua
**Functions:**
- GetDailyDungeon_Map3Uis
**Requires:**
- DailyDungeon_CircleByName
- DailyDungeon_MapTipsByName
**Snippet:**
```lua
require("DailyDungeon_CircleByName")
require("DailyDungeon_MapTipsByName")

function GetDailyDungeon_Map3Uis(ui)
  local uis = {}
  uis.Circle = GetDailyDungeon_CircleUis(ui:GetChild("Circle"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.Tips1 = GetDailyDungeon_MapTipsUis(ui:GetChild("Tips1"))
  uis.Tips2 = GetDailyDungeon_MapTipsUis(ui:GetChild("Tips2"))
  uis.Tips3 = GetDailyDungeon_MapTipsUis(ui:GetChild("Tips3"))
```

---

## BCD/DailyDungeon_Map4PatternAniByName.lua.lua
**Functions:**
- GetDailyDungeon_Map4PatternAniUis
**Requires:**
- DailyDungeon_Map4PatternByName
**Snippet:**
```lua
require("DailyDungeon_Map4PatternByName")

function GetDailyDungeon_Map4PatternAniUis(ui)
  local uis = {}
  uis.Pattern = GetDailyDungeon_Map4PatternUis(ui:GetChild("Pattern"))
  uis.root = ui
  return uis
end
```

---

## BCD/DailyDungeon_Map4PatternByName.lua.lua
**Functions:**
- GetDailyDungeon_Map4PatternUis
**Snippet:**
```lua
function GetDailyDungeon_Map4PatternUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyDungeon_Map4_1ByName.lua.lua
**Functions:**
- GetDailyDungeon_Map4_1Uis
**Requires:**
- DailyDungeon_CircleByName
- DailyDungeon_Map4PatternAniByName
- DailyDungeon_MapTipsByName
**Snippet:**
```lua
require("DailyDungeon_CircleByName")
require("DailyDungeon_Map4PatternAniByName")
require("DailyDungeon_MapTipsByName")

function GetDailyDungeon_Map4_1Uis(ui)
  local uis = {}
  uis.Circle = GetDailyDungeon_CircleUis(ui:GetChild("Circle"))
  uis.PatternAni = GetDailyDungeon_Map4PatternAniUis(ui:GetChild("PatternAni"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.Tips1 = GetDailyDungeon_MapTipsUis(ui:GetChild("Tips1"))
```

---

## BCD/DailyDungeon_Map4_2ByName.lua.lua
**Functions:**
- GetDailyDungeon_Map4_2Uis
**Requires:**
- DailyDungeon_CircleByName
- DailyDungeon_Map4PatternAniByName
- DailyDungeon_MapTipsByName
**Snippet:**
```lua
require("DailyDungeon_CircleByName")
require("DailyDungeon_Map4PatternAniByName")
require("DailyDungeon_MapTipsByName")

function GetDailyDungeon_Map4_2Uis(ui)
  local uis = {}
  uis.Circle = GetDailyDungeon_CircleUis(ui:GetChild("Circle"))
  uis.PatternAni = GetDailyDungeon_Map4PatternAniUis(ui:GetChild("PatternAni"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.Tips1 = GetDailyDungeon_MapTipsUis(ui:GetChild("Tips1"))
```

---

## BCD/DailyDungeon_Map4_4ByName.lua.lua
**Functions:**
- GetDailyDungeon_Map4_4Uis
**Requires:**
- DailyDungeon_CircleByName
- DailyDungeon_Map4PatternAniByName
- DailyDungeon_MapTipsByName
**Snippet:**
```lua
require("DailyDungeon_CircleByName")
require("DailyDungeon_Map4PatternAniByName")
require("DailyDungeon_MapTipsByName")

function GetDailyDungeon_Map4_4Uis(ui)
  local uis = {}
  uis.Circle = GetDailyDungeon_CircleUis(ui:GetChild("Circle"))
  uis.PatternAni = GetDailyDungeon_Map4PatternAniUis(ui:GetChild("PatternAni"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.Tips1 = GetDailyDungeon_MapTipsUis(ui:GetChild("Tips1"))
```

---

## BCD/DailyDungeon_Map4_5ByName.lua.lua
**Functions:**
- GetDailyDungeon_Map4_5Uis
**Requires:**
- DailyDungeon_CircleByName
- DailyDungeon_Map4PatternAniByName
- DailyDungeon_MapTipsByName
**Snippet:**
```lua
require("DailyDungeon_CircleByName")
require("DailyDungeon_Map4PatternAniByName")
require("DailyDungeon_MapTipsByName")

function GetDailyDungeon_Map4_5Uis(ui)
  local uis = {}
  uis.Circle = GetDailyDungeon_CircleUis(ui:GetChild("Circle"))
  uis.PatternAni = GetDailyDungeon_Map4PatternAniUis(ui:GetChild("PatternAni"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.Tips1 = GetDailyDungeon_MapTipsUis(ui:GetChild("Tips1"))
```

---

## BCD/DailyDungeon_Map5PatternAniByName.lua.lua
**Functions:**
- GetDailyDungeon_Map5PatternAniUis
**Requires:**
- DailyDungeon_Map5PatternByName
**Snippet:**
```lua
require("DailyDungeon_Map5PatternByName")

function GetDailyDungeon_Map5PatternAniUis(ui)
  local uis = {}
  uis.Pattern = GetDailyDungeon_Map5PatternUis(ui:GetChild("Pattern"))
  uis.root = ui
  return uis
end
```

---

## BCD/DailyDungeon_Map5PatternByName.lua.lua
**Functions:**
- GetDailyDungeon_Map5PatternUis
**Snippet:**
```lua
function GetDailyDungeon_Map5PatternUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyDungeon_Map5_1ByName.lua.lua
**Functions:**
- GetDailyDungeon_Map5_1Uis
**Requires:**
- DailyDungeon_CircleByName
- DailyDungeon_Map5PatternAniByName
- DailyDungeon_MapTipsByName
**Snippet:**
```lua
require("DailyDungeon_CircleByName")
require("DailyDungeon_Map5PatternAniByName")
require("DailyDungeon_MapTipsByName")

function GetDailyDungeon_Map5_1Uis(ui)
  local uis = {}
  uis.Circle = GetDailyDungeon_CircleUis(ui:GetChild("Circle"))
  uis.PatternAni = GetDailyDungeon_Map5PatternAniUis(ui:GetChild("PatternAni"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.Tips1 = GetDailyDungeon_MapTipsUis(ui:GetChild("Tips1"))
```

---

## BCD/DailyDungeon_Map5_2ByName.lua.lua
**Functions:**
- GetDailyDungeon_Map5_2Uis
**Requires:**
- DailyDungeon_CircleByName
- DailyDungeon_Map5PatternAniByName
- DailyDungeon_MapTipsByName
**Snippet:**
```lua
require("DailyDungeon_CircleByName")
require("DailyDungeon_Map5PatternAniByName")
require("DailyDungeon_MapTipsByName")

function GetDailyDungeon_Map5_2Uis(ui)
  local uis = {}
  uis.Circle = GetDailyDungeon_CircleUis(ui:GetChild("Circle"))
  uis.PatternAni = GetDailyDungeon_Map5PatternAniUis(ui:GetChild("PatternAni"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.Tips1 = GetDailyDungeon_MapTipsUis(ui:GetChild("Tips1"))
```

---

## BCD/DailyDungeon_Map5_4ByName.lua.lua
**Functions:**
- GetDailyDungeon_Map5_4Uis
**Requires:**
- DailyDungeon_CircleByName
- DailyDungeon_Map5PatternAniByName
- DailyDungeon_MapTipsByName
**Snippet:**
```lua
require("DailyDungeon_CircleByName")
require("DailyDungeon_Map5PatternAniByName")
require("DailyDungeon_MapTipsByName")

function GetDailyDungeon_Map5_4Uis(ui)
  local uis = {}
  uis.Circle = GetDailyDungeon_CircleUis(ui:GetChild("Circle"))
  uis.PatternAni = GetDailyDungeon_Map5PatternAniUis(ui:GetChild("PatternAni"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.Tips1 = GetDailyDungeon_MapTipsUis(ui:GetChild("Tips1"))
```

---

## BCD/DailyDungeon_Map5_5ByName.lua.lua
**Functions:**
- GetDailyDungeon_Map5_5Uis
**Requires:**
- DailyDungeon_CircleByName
- DailyDungeon_Map5PatternAniByName
- DailyDungeon_MapTipsByName
**Snippet:**
```lua
require("DailyDungeon_CircleByName")
require("DailyDungeon_Map5PatternAniByName")
require("DailyDungeon_MapTipsByName")

function GetDailyDungeon_Map5_5Uis(ui)
  local uis = {}
  uis.Circle = GetDailyDungeon_CircleUis(ui:GetChild("Circle"))
  uis.PatternAni = GetDailyDungeon_Map5PatternAniUis(ui:GetChild("PatternAni"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.Tips1 = GetDailyDungeon_MapTipsUis(ui:GetChild("Tips1"))
```

---

## BCD/DailyDungeon_Map5_6ByName.lua.lua
**Functions:**
- GetDailyDungeon_Map5_6Uis
**Requires:**
- DailyDungeon_CircleByName
- DailyDungeon_Map5PatternAniByName
- DailyDungeon_MapTipsByName
**Snippet:**
```lua
require("DailyDungeon_CircleByName")
require("DailyDungeon_Map5PatternAniByName")
require("DailyDungeon_MapTipsByName")

function GetDailyDungeon_Map5_6Uis(ui)
  local uis = {}
  uis.Circle = GetDailyDungeon_CircleUis(ui:GetChild("Circle"))
  uis.PatternAni = GetDailyDungeon_Map5PatternAniUis(ui:GetChild("PatternAni"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.Tips1 = GetDailyDungeon_MapTipsUis(ui:GetChild("Tips1"))
```

---

## BCD/DailyDungeon_Map6PatternAniByName.lua.lua
**Functions:**
- GetDailyDungeon_Map6PatternAniUis
**Requires:**
- DailyDungeon_Map6PatternByName
**Snippet:**
```lua
require("DailyDungeon_Map6PatternByName")

function GetDailyDungeon_Map6PatternAniUis(ui)
  local uis = {}
  uis.Pattern = GetDailyDungeon_Map6PatternUis(ui:GetChild("Pattern"))
  uis.root = ui
  return uis
end
```

---

## BCD/DailyDungeon_Map6PatternByName.lua.lua
**Functions:**
- GetDailyDungeon_Map6PatternUis
**Snippet:**
```lua
function GetDailyDungeon_Map6PatternUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyDungeon_Map6_1ByName.lua.lua
**Functions:**
- GetDailyDungeon_Map6_1Uis
**Requires:**
- DailyDungeon_CircleByName
- DailyDungeon_Map6PatternAniByName
- DailyDungeon_MapTipsByName
**Snippet:**
```lua
require("DailyDungeon_CircleByName")
require("DailyDungeon_Map6PatternAniByName")
require("DailyDungeon_MapTipsByName")

function GetDailyDungeon_Map6_1Uis(ui)
  local uis = {}
  uis.Circle = GetDailyDungeon_CircleUis(ui:GetChild("Circle"))
  uis.PatternAni = GetDailyDungeon_Map6PatternAniUis(ui:GetChild("PatternAni"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.Tips1 = GetDailyDungeon_MapTipsUis(ui:GetChild("Tips1"))
```

---

## BCD/DailyDungeon_Map6_2ByName.lua.lua
**Functions:**
- GetDailyDungeon_Map6_2Uis
**Requires:**
- DailyDungeon_CircleByName
- DailyDungeon_Map6PatternAniByName
- DailyDungeon_MapTipsByName
**Snippet:**
```lua
require("DailyDungeon_CircleByName")
require("DailyDungeon_Map6PatternAniByName")
require("DailyDungeon_MapTipsByName")

function GetDailyDungeon_Map6_2Uis(ui)
  local uis = {}
  uis.Circle = GetDailyDungeon_CircleUis(ui:GetChild("Circle"))
  uis.PatternAni = GetDailyDungeon_Map6PatternAniUis(ui:GetChild("PatternAni"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.Tips1 = GetDailyDungeon_MapTipsUis(ui:GetChild("Tips1"))
```

---

## BCD/DailyDungeon_Map6_3ByName.lua.lua
**Functions:**
- GetDailyDungeon_Map6_3Uis
**Requires:**
- DailyDungeon_CircleByName
- DailyDungeon_Map6PatternAniByName
- DailyDungeon_MapTipsByName
**Snippet:**
```lua
require("DailyDungeon_CircleByName")
require("DailyDungeon_Map6PatternAniByName")
require("DailyDungeon_MapTipsByName")

function GetDailyDungeon_Map6_3Uis(ui)
  local uis = {}
  uis.Circle = GetDailyDungeon_CircleUis(ui:GetChild("Circle"))
  uis.PatternAni = GetDailyDungeon_Map6PatternAniUis(ui:GetChild("PatternAni"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.Tips1 = GetDailyDungeon_MapTipsUis(ui:GetChild("Tips1"))
```

---

## BCD/DailyDungeon_Map6_4ByName.lua.lua
**Functions:**
- GetDailyDungeon_Map6_4Uis
**Requires:**
- DailyDungeon_CircleByName
- DailyDungeon_Map6PatternAniByName
- DailyDungeon_MapTipsByName
**Snippet:**
```lua
require("DailyDungeon_CircleByName")
require("DailyDungeon_Map6PatternAniByName")
require("DailyDungeon_MapTipsByName")

function GetDailyDungeon_Map6_4Uis(ui)
  local uis = {}
  uis.Circle = GetDailyDungeon_CircleUis(ui:GetChild("Circle"))
  uis.PatternAni = GetDailyDungeon_Map6PatternAniUis(ui:GetChild("PatternAni"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.Tips1 = GetDailyDungeon_MapTipsUis(ui:GetChild("Tips1"))
```

---

## BCD/DailyDungeon_MapTipsBtnByName.lua.lua
**Functions:**
- GetDailyDungeon_MapTipsBtnUis
**Snippet:**
```lua
function GetDailyDungeon_MapTipsBtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.NewImage = ui:GetChild("NewImage")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.buttonCtr = ui:GetController("button")
```

---

## BCD/DailyDungeon_MapTipsByName.lua.lua
**Functions:**
- GetDailyDungeon_MapTipsUis
**Snippet:**
```lua
function GetDailyDungeon_MapTipsUis(ui)
  local uis = {}
  
  uis.MapTipsBtn = ui:GetChild("MapTipsBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyDungeon_Occupation1ByName.lua.lua
**Functions:**
- GetDailyDungeon_Occupation1Uis
**Snippet:**
```lua
function GetDailyDungeon_Occupation1Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyDungeon_Occupation2ByName.lua.lua
**Functions:**
- GetDailyDungeon_Occupation2Uis
**Snippet:**
```lua
function GetDailyDungeon_Occupation2Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyDungeon_Tab1BtnByName.lua.lua
**Functions:**
- GetDailyDungeon_Tab1BtnUis
**Requires:**
- DailyDungeon_TabBtnBgByName
- DailyDungeon_Badge2ByName
- DailyDungeon_Badge1ByName
**Snippet:**
```lua
require("DailyDungeon_TabBtnBgByName")
require("DailyDungeon_Badge2ByName")
require("DailyDungeon_Badge1ByName")

function GetDailyDungeon_Tab1BtnUis(ui)
  local uis = {}
  uis.TabBtnBg = GetDailyDungeon_TabBtnBgUis(ui:GetChild("TabBtnBg"))
  uis.Badge2 = GetDailyDungeon_Badge2Uis(ui:GetChild("Badge2"))
  uis.Badge1 = GetDailyDungeon_Badge1Uis(ui:GetChild("Badge1"))
  uis.WordTxt = ui:GetChild("WordTxt")
```

---

## BCD/DailyDungeon_TabBtnBgByName.lua.lua
**Functions:**
- GetDailyDungeon_TabBtnBgUis
**Snippet:**
```lua
function GetDailyDungeon_TabBtnBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/DailyDungeon_TabBtnByName.lua.lua
**Functions:**
- GetDailyDungeon_TabBtnUis
**Requires:**
- DailyDungeon_TabBtnBgByName
- DailyDungeon_Occupation2ByName
- DailyDungeon_Occupation1ByName
**Snippet:**
```lua
require("DailyDungeon_TabBtnBgByName")
require("DailyDungeon_Occupation2ByName")
require("DailyDungeon_Occupation1ByName")

function GetDailyDungeon_TabBtnUis(ui)
  local uis = {}
  uis.TabBtnBg = GetDailyDungeon_TabBtnBgUis(ui:GetChild("TabBtnBg"))
  uis.Badge2 = GetDailyDungeon_Occupation2Uis(ui:GetChild("Badge2"))
  uis.Badge1 = GetDailyDungeon_Occupation1Uis(ui:GetChild("Badge1"))
  uis.WordTxt = ui:GetChild("WordTxt")
```

---

## BCD/DailyDungeon_TabRegionByName.lua.lua
**Functions:**
- GetDailyDungeon_TabRegionUis
**Snippet:**
```lua
function GetDailyDungeon_TabRegionUis(ui)
  local uis = {}
  
  uis.Tab10Btn = ui:GetChild("Tab10Btn")
  uis.Tab11Btn = ui:GetChild("Tab11Btn")
  uis.Tab12Btn = ui:GetChild("Tab12Btn")
  uis.Tab13Btn = ui:GetChild("Tab13Btn")
  uis.Tab1Btn = ui:GetChild("Tab1Btn")
  uis.Tab2Btn = ui:GetChild("Tab2Btn")
  uis.Tab4Btn = ui:GetChild("Tab4Btn")
```

---

## BCD/DailyDungeon_TypeIcon1ByName.lua.lua
**Functions:**
- GetDailyDungeon_TypeIcon1Uis
**Snippet:**
```lua
function GetDailyDungeon_TypeIcon1Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyDungeon_TypeIcon2ByName.lua.lua
**Functions:**
- GetDailyDungeon_TypeIcon2Uis
**Snippet:**
```lua
function GetDailyDungeon_TypeIcon2Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyMapWindow.lua.lua
**Functions:**
- DailyMapWindow.OnInit
- DailyMapWindow.Init
- DailyMapWindow.IsQuality
- DailyMapWindow.InitData
- DailyMapWindow.InitList
- DailyMapWindow.RefreshMapList
- DailyMapWindow.PlayAnim
- DailyMapWindow.RefreshMapItem
- DailyMapWindow.StageItemClick
- DailyMapWindow.ChangeTabState
- DailyMapWindow.GetFeatureId
- DailyMapWindow.InitBtn
- DailyMapWindow.RefreshMapUnlockUI
- DailyMapWindow.ChangeUI
- DailyMapWindow.HandleMessage
- DailyMapWindow.OnShown
- DailyMapWindow.DisposeMap
- DailyMapWindow.OnClose
**Requires:**
- DailyDungeon_DailyMapWindowByName
**Snippet:**
```lua
require("DailyDungeon_DailyMapWindowByName")
local DailyMapWindow = {}
local uis, chapterData, chapterTypeMap, contentPane, stageId, dailyData, jumpTb, stageNum
local lastIndex = 0
local firstOpen, argTable
local bgEffectPath = "Assets/Art/Effects/Prefab/UI_prefab/DailyAdventure/%s"
local GetEffEctPath = function(name)
  return string.format(bgEffectPath, name)
end

```

---

## BCD/DailyRewardListWindow.lua.lua
**Functions:**
- DailyRewardListWindow.ReInitData
- DailyRewardListWindow.OnInit
- DailyRewardListWindow.UpdateInfo
- list.itemRenderer
- rewardList.itemRenderer
- DailyRewardListWindow.InitBtn
- DailyRewardListWindow.Close
- DailyRewardListWindow.OnClose
- DailyRewardListWindow.HandleMessage
**Requires:**
- DailyTask_DailyRewardListWindowByName
**Snippet:**
```lua
require("DailyTask_DailyRewardListWindowByName")
local DailyRewardListWindow = {}
local uis, contentPane

function DailyRewardListWindow.ReInitData()
end

function DailyRewardListWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.DailyRewardListWindow.package, WinResConfig.DailyRewardListWindow.comName, function(com)
    contentPane = com
```

---

## BCD/DailySupplyData.lua.lua
**Snippet:**
```lua
local supplies
local AddSupplies = function(supply_list)
  if supply_list and _G.next(supply_list) then
    supplies = supplies or {}
    for i, v in ipairs(supply_list) do
      table.insert(supplies, v)
    end
  end
end
local GetSupplies = function()
```

---

## BCD/DailySupplyMgr.lua.lua
**Snippet:**
```lua
local COMPARE_RESULT = {
  EQUAL = 0,
  LESS = -1,
  GREATER = 1
}
local CompareWithServerStamp = function(hour, minutes)
  local timestamp = math.ceil(LoginData.GetCurServerTime())
  local h = tonumber(TimeUtil.FormatDate("%H", timestamp))
  local m = tonumber(TimeUtil.FormatDate("%M", timestamp))
  if hour < h then
```

---

## BCD/DailySupplyScriptList.lua.lua
**Requires:**
- DailySupplyData
- DailySupplyService
- DailySupplyMgr
**Snippet:**
```lua
DailySupplyData = require("DailySupplyData")
DailySupplyService = require("DailySupplyService")
DailySupplyMgr = require("DailySupplyMgr")
DailySupplyService.Init()
```

---

## BCD/DailySupplyService.lua.lua
**Snippet:**
```lua
local GetSupplyInfoReq = function(rspCallback)
  Net.Send(Proto.MsgName.GetSupplyInfoReq, nil, rspCallback)
end
local OnGetSupplyInfoRsp = function(msg)
  DailySupplyData.Clear()
  DailySupplyData.AddSupplies(msg.rewarded)
end
local reward_supply_msg = {}
local RewardSupplyReq = function(rewardId, redeem, rspCallback)
  reward_supply_msg.rewardId = rewardId
```

---

## BCD/DailyTaskData.lua.lua
**Functions:**
- DailyTaskData.InitTaskData
- DailyTaskData.UpdateTaskData
- DailyTaskData.UpdateTaskReplace
- DailyTaskData.UpdateTaskReward
- DailyTaskData.GetRefreshStamp
- DailyTaskData.GetTaskList
- DailyTaskData.GetGrowItem
- DailyTaskData.GetGrowShow
- DailyTaskData.GetAllRewardGroupByPhase
- DailyTaskData.GetMaxPhaseId
- DailyTaskData.IsPhaseRewardGot
- DailyTaskData.GetDailyItem
- DailyTaskData.GetDailyReward
- DailyTaskData.IsRewardGot
- DailyTaskData.GetTaskCommonReward
- DailyTaskData.GetHomeShowTask
- DailyTaskData.ShowHomeDailyTarget
- DailyTaskData.CanDailyTask
**Snippet:**
```lua
DailyTaskData = {}
local taskList, dailyRewards, totalRewards
local refreshStamp = 0
local dailyItemId, totalItemId
DAILY_TASK_TAB = {DAILY = 0, EXPLORE = 1}
REWARD_PHASE_STATE = {
  INPROGRESS = 0,
  COMPLETE = 1,
  LOCK = 2
}
```

---

## BCD/DailyTaskMgr.lua.lua
**Snippet:**
```lua
DailyTaskMgr = {}
```

---

## BCD/DailyTaskScriptList.lua.lua
**Requires:**
- DailyTaskMgr
- DailyTaskData
- DailyTaskService
**Snippet:**
```lua
local require = require
require("DailyTaskMgr")
require("DailyTaskData")
require("DailyTaskService")
```

---

## BCD/DailyTaskService.lua.lua
**Functions:**
- DailyTaskService.Init
- DailyTaskService.GetCommonTaskInfoReq
- DailyTaskService.GetCommonTaskInfoRsp
- DailyTaskService.CommonTaskRewardReq
- DailyTaskService.CommonTaskRewardRsp
- DailyTaskService.CommonTaskReplaceReq
- DailyTaskService.CommonTaskReplaceRsp
**Snippet:**
```lua
DailyTaskService = {}

function DailyTaskService.Init()
  Net.AddListener(Proto.MsgName.GetCommonTaskInfoRsp, DailyTaskService.GetCommonTaskInfoRsp)
  Net.AddListener(Proto.MsgName.CommonTaskRewardRsp, DailyTaskService.CommonTaskRewardRsp)
  Net.AddListener(Proto.MsgName.CommonTaskReplaceRsp, DailyTaskService.CommonTaskReplaceRsp)
end

function DailyTaskService.GetCommonTaskInfoReq(rspCallback)
  local msg = {}
```

---

## BCD/DailyTaskWindow.lua.lua
**Functions:**
- DailyTaskWindow.OnInit
- DailyTaskWindow.UpdateTabContent
- DailyTaskWindow.InitRedDot
- DailyTaskWindow.LoadBgTexture
- DailyTaskWindow.Init
- DailyTaskWindow.InitTabRegion
- DailyTaskWindow.UpdateAll
- DailyTaskWindow.InitText
- DailyTaskWindow.InitBtn
- DailyTaskWindow.UpdateTaskShow
- DailyTaskWindow.UpdateAllGrowReward
- list.itemRenderer
- rewardList.itemRenderer
- DailyTaskWindow.UpdateDailyReward
- DailyTaskWindow.UpdateInfo
- DailyTaskWindow.UpdateDaily
- list.itemRenderer
- DailyTaskWindow.UpdateOneTask
- DailyTaskWindow.HandleMessage
- DailyTaskWindow.OnClose
**Requires:**
- DailyTask_DailyTaskByName
**Snippet:**
```lua
require("DailyTask_DailyTaskByName")
DailyTaskWindow = {}
local dailyTask, firstEnter
local delayTime = 0.08
local MAIN_TAB_ENUM = {TASK = 0, REWARD = 1}
local curSelectMainTabIndex

function DailyTaskWindow.OnInit(com)
  dailyTask = GetDailyTask_DailyTaskUis(com)
  firstEnter = true
```

---

## BCD/DailyTask_AllRewardRegionByName.lua.lua
**Functions:**
- GetDailyTask_AllRewardRegionUis
**Requires:**
- DailyTask_TaskShowByName
**Snippet:**
```lua
require("DailyTask_TaskShowByName")

function GetDailyTask_AllRewardRegionUis(ui)
  local uis = {}
  uis.TaskShow = GetDailyTask_TaskShowUis(ui:GetChild("TaskShow"))
  uis.RewardList = ui:GetChild("RewardList")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyTask_AllRewardTipsAniByName.lua.lua
**Functions:**
- GetDailyTask_AllRewardTipsAniUis
**Requires:**
- DailyTask_AllRewardTipsByName
**Snippet:**
```lua
require("DailyTask_AllRewardTipsByName")

function GetDailyTask_AllRewardTipsAniUis(ui)
  local uis = {}
  uis.AllRewardTips = GetDailyTask_AllRewardTipsUis(ui:GetChild("AllRewardTips"))
  uis.root = ui
  return uis
end
```

---

## BCD/DailyTask_AllRewardTipsByName.lua.lua
**Functions:**
- GetDailyTask_AllRewardTipsUis
**Requires:**
- DailyTask_UnOpenTipsByName
- DailyTask_CompleteTipsByName
**Snippet:**
```lua
require("DailyTask_UnOpenTipsByName")
require("DailyTask_CompleteTipsByName")

function GetDailyTask_AllRewardTipsUis(ui)
  local uis = {}
  uis.UnOpenTips = GetDailyTask_UnOpenTipsUis(ui:GetChild("UnOpenTips"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.RewardList = ui:GetChild("RewardList")
  uis.CompleteTips = GetDailyTask_CompleteTipsUis(ui:GetChild("CompleteTips"))
  uis.WordTxt = ui:GetChild("WordTxt")
```

---

## BCD/DailyTask_CloseBtnByName.lua.lua
**Functions:**
- GetDailyTask_CloseBtnUis
**Snippet:**
```lua
function GetDailyTask_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyTask_CompleteTipsByName.lua.lua
**Functions:**
- GetDailyTask_CompleteTipsUis
**Snippet:**
```lua
function GetDailyTask_CompleteTipsUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyTask_DailyRegionByName.lua.lua
**Functions:**
- GetDailyTask_DailyRegionUis
**Requires:**
- DailyTask_DayRewardByName
**Snippet:**
```lua
require("DailyTask_DayRewardByName")

function GetDailyTask_DailyRegionUis(ui)
  local uis = {}
  uis.DailyList = ui:GetChild("DailyList")
  uis.DayReward = GetDailyTask_DayRewardUis(ui:GetChild("DayReward"))
  uis.root = ui
  return uis
end
```

---

## BCD/DailyTask_DailyRewardList1ByName.lua.lua
**Functions:**
- GetDailyTask_DailyRewardList1Uis
**Snippet:**
```lua
function GetDailyTask_DailyRewardList1Uis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyTask_DailyRewardList2ByName.lua.lua
**Functions:**
- GetDailyTask_DailyRewardList2Uis
**Requires:**
- CommonResource_PopupBgByName
- DailyTask_DailyRewardList1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("DailyTask_DailyRewardList1ByName")

function GetDailyTask_DailyRewardList2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.DailyRewardList1 = GetDailyTask_DailyRewardList1Uis(ui:GetChild("DailyRewardList1"))
  uis.root = ui
  return uis
```

---

## BCD/DailyTask_DailyRewardListWindowByName.lua.lua
**Functions:**
- GetDailyTask_DailyRewardListWindowUis
**Requires:**
- DailyTask_DailyRewardList2ByName
**Snippet:**
```lua
require("DailyTask_DailyRewardList2ByName")

function GetDailyTask_DailyRewardListWindowUis(ui)
  local uis = {}
  uis.Main = GetDailyTask_DailyRewardList2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/DailyTask_DailyRewardStripByName.lua.lua
**Functions:**
- GetDailyTask_DailyRewardStripUis
**Snippet:**
```lua
function GetDailyTask_DailyRewardStripUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.RewardList = ui:GetChild("RewardList")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## BCD/DailyTask_DailyTaskByName.lua.lua
**Functions:**
- GetDailyTask_DailyTaskUis
**Requires:**
- CommonResource_BackGroundByName
- DailyTask_DailyRegionByName
- DailyTask_AllRewardRegionByName
- DailyTask_TabRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("DailyTask_DailyRegionByName")
require("DailyTask_AllRewardRegionByName")
require("DailyTask_TabRegionByName")

function GetDailyTask_DailyTaskUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.DailyRegion = GetDailyTask_DailyRegionUis(ui:GetChild("DailyRegion"))
```

---

## BCD/DailyTask_DailyTaskWindowByName.lua.lua
**Functions:**
- GetDailyTask_DailyTaskWindowUis
**Requires:**
- DailyTask_DailyTaskByName
**Snippet:**
```lua
require("DailyTask_DailyTaskByName")

function GetDailyTask_DailyTaskWindowUis(ui)
  local uis = {}
  uis.Main = GetDailyTask_DailyTaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/DailyTask_DailyTipsAniByName.lua.lua
**Functions:**
- GetDailyTask_DailyTipsAniUis
**Requires:**
- DailyTask_DailyTipsByName
**Snippet:**
```lua
require("DailyTask_DailyTipsByName")

function GetDailyTask_DailyTipsAniUis(ui)
  local uis = {}
  uis.DailyTips = GetDailyTask_DailyTipsUis(ui:GetChild("DailyTips"))
  uis.root = ui
  return uis
end
```

---

## BCD/DailyTask_DailyTipsByName.lua.lua
**Functions:**
- GetDailyTask_DailyTipsUis
**Requires:**
- DailyTask_RewardItem1ByName
**Snippet:**
```lua
require("DailyTask_RewardItem1ByName")

function GetDailyTask_DailyTipsUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.RewardItem1 = GetDailyTask_RewardItem1Uis(ui:GetChild("RewardItem1"))
  uis.RewardItem2 = GetDailyTask_RewardItem1Uis(ui:GetChild("RewardItem2"))
  uis.Submit1Txt = ui:GetChild("Submit1Txt")
  uis.RefreshBtn = ui:GetChild("RefreshBtn")
```

---

## BCD/DailyTask_DayRewardBtnByName.lua.lua
**Functions:**
- GetDailyTask_DayRewardBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetDailyTask_DayRewardBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## BCD/DailyTask_DayRewardByName.lua.lua
**Functions:**
- GetDailyTask_DayRewardUis
**Snippet:**
```lua
function GetDailyTask_DayRewardUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.ExpProgressBar = ui:GetChild("ExpProgressBar")
  uis.DayRewardBtn = ui:GetChild("DayRewardBtn")
  uis.TouchBtn = ui:GetChild("TouchBtn")
  uis.root = ui
  return uis
```

---

## BCD/DailyTask_DropByName.lua.lua
**Functions:**
- GetDailyTask_DropUis
**Snippet:**
```lua
function GetDailyTask_DropUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyTask_EmptyTouchBtnByName.lua.lua
**Functions:**
- GetDailyTask_EmptyTouchBtnUis
**Snippet:**
```lua
function GetDailyTask_EmptyTouchBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyTask_ExpNumberByName.lua.lua
**Functions:**
- GetDailyTask_ExpNumberUis
**Snippet:**
```lua
function GetDailyTask_ExpNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyTask_ExpProgressBarByName.lua.lua
**Functions:**
- GetDailyTask_ExpProgressBarUis
**Requires:**
- DailyTask_ExpProgressFillByName
- DailyTask_DropByName
- DailyTask_ExpNumberByName
**Snippet:**
```lua
require("DailyTask_ExpProgressFillByName")
require("DailyTask_DropByName")
require("DailyTask_ExpNumberByName")

function GetDailyTask_ExpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetDailyTask_ExpProgressFillUis(ui:GetChild("bar"))
  uis.Drop1 = GetDailyTask_DropUis(ui:GetChild("Drop1"))
  uis.Drop2 = GetDailyTask_DropUis(ui:GetChild("Drop2"))
  uis.Drop3 = GetDailyTask_DropUis(ui:GetChild("Drop3"))
```

---

## BCD/DailyTask_ExpProgressFillByName.lua.lua
**Functions:**
- GetDailyTask_ExpProgressFillUis
**Snippet:**
```lua
function GetDailyTask_ExpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/DailyTask_GetBtnByName.lua.lua
**Functions:**
- GetDailyTask_GetBtnUis
**Snippet:**
```lua
function GetDailyTask_GetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyTask_GoToBtnByName.lua.lua
**Functions:**
- GetDailyTask_GoToBtnUis
**Snippet:**
```lua
function GetDailyTask_GoToBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyTask_ItemCardPicByName.lua.lua
**Functions:**
- GetDailyTask_ItemCardPicUis
**Snippet:**
```lua
function GetDailyTask_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyTask_LookBtnByName.lua.lua
**Functions:**
- GetDailyTask_LookBtnUis
**Snippet:**
```lua
function GetDailyTask_LookBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyTask_RefreshBtnByName.lua.lua
**Functions:**
- GetDailyTask_RefreshBtnUis
**Snippet:**
```lua
function GetDailyTask_RefreshBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyTask_RewardItem1ByName.lua.lua
**Functions:**
- GetDailyTask_RewardItem1Uis
**Snippet:**
```lua
function GetDailyTask_RewardItem1Uis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyTask_RewardItem2ByName.lua.lua
**Functions:**
- GetDailyTask_RewardItem2Uis
**Snippet:**
```lua
function GetDailyTask_RewardItem2Uis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyTask_RewardItem4ByName.lua.lua
**Functions:**
- GetDailyTask_RewardItem4Uis
**Requires:**
- DailyTask_ItemCardPicByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("DailyTask_ItemCardPicByName")
require("CommonResource_RedDotByName")

function GetDailyTask_RewardItem4Uis(ui)
  local uis = {}
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.PicNumberTxt = ui:GetChild("PicNumberTxt")
```

---

## BCD/DailyTask_SubmitBtnByName.lua.lua
**Functions:**
- GetDailyTask_SubmitBtnUis
**Snippet:**
```lua
function GetDailyTask_SubmitBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyTask_TabBtnByName.lua.lua
**Functions:**
- GetDailyTask_TabBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetDailyTask_TabBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.FlagCtr = ui:GetController("Flag")
  uis.root = ui
  return uis
```

---

## BCD/DailyTask_TabRegionByName.lua.lua
**Functions:**
- GetDailyTask_TabRegionUis
**Snippet:**
```lua
function GetDailyTask_TabRegionUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyTask_TaskShowByName.lua.lua
**Functions:**
- GetDailyTask_TaskShowUis
**Snippet:**
```lua
function GetDailyTask_TaskShowUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.LookBtn = ui:GetChild("LookBtn")
  uis.root = ui
  return uis
end
```

---

## BCD/DailyTask_UnOpenTipsByName.lua.lua
**Functions:**
- GetDailyTask_UnOpenTipsUis
**Snippet:**
```lua
function GetDailyTask_UnOpenTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/DebrisWindow.lua.lua
**Functions:**
- DebrisWindow.ReInitData
- DebrisWindow.OnInit
- DebrisWindow.InitInfo
- DebrisWindow.UpdateTextDisplay
- DebrisWindow.InitBtn
- DebrisWindow.OnShown
- DebrisWindow.OnHide
- DebrisWindow.OnClose
- DebrisWindow.HandleMessage
**Requires:**
- Message_DebrisWindowByName
**Snippet:**
```lua
require("Message_DebrisWindowByName")
local DebrisWindow = {}
local uis, contentPane, targetId, itemId

function DebrisWindow.ReInitData()
end

function DebrisWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.DebrisWindow.package, WinResConfig.DebrisWindow.comName, function(com)
    contentPane = com
```

---

## BCD/DetailsAllSkillWindow.lua.lua
**Functions:**
- DetailsAllSkillWindow.ReInitData
- DetailsAllSkillWindow.OnInit
- DetailsAllSkillWindow.UpdateInfo
- uis.Main.SpclSkillTipsList.itemRenderer
- list.itemRenderer
- DetailsAllSkillWindow.ShowSkillDes
- list.itemRenderer
- DetailsAllSkillWindow.InitBtn
- DetailsAllSkillWindow.OnClose
**Requires:**
- CardAttribute_DetailsAllSkillWindowByName
**Snippet:**
```lua
require("CardAttribute_DetailsAllSkillWindowByName")
local DetailsAllSkillWindow = {}
local uis, contentPane, skillInfo

function DetailsAllSkillWindow.ReInitData()
end

function DetailsAllSkillWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.DetailsAllSkillWindow.package, WinResConfig.DetailsAllSkillWindow.comName, function(com)
    contentPane = com
```

---

## BCD/DiamondTips_CloseBtnByName.lua.lua
**Functions:**
- GetDiamondTips_CloseBtnUis
**Snippet:**
```lua
function GetDiamondTips_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/DiamondTips_DiamondByName.lua.lua
**Functions:**
- GetDiamondTips_DiamondUis
**Requires:**
- CommonResource_BackGroundByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")

function GetDiamondTips_DiamondUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.GoToBtn = ui:GetChild("GoToBtn")
  uis.CloseBtn = ui:GetChild("CloseBtn")
```

---

## BCD/DiamondTips_DiamondWindowByName.lua.lua
**Functions:**
- GetDiamondTips_DiamondWindowUis
**Requires:**
- DiamondTips_DiamondByName
**Snippet:**
```lua
require("DiamondTips_DiamondByName")

function GetDiamondTips_DiamondWindowUis(ui)
  local uis = {}
  uis.Main = GetDiamondTips_DiamondUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/DiamondTips_GoToBtnByName.lua.lua
**Functions:**
- GetDiamondTips_GoToBtnUis
**Snippet:**
```lua
function GetDiamondTips_GoToBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/DiamondWindow.lua.lua
**Functions:**
- DiamondWindow.ReInitData
- DiamondWindow.OnInit
- DiamondWindow.UpdateInfo
- DiamondWindow.InitBtn
- DiamondWindow.OnClose
**Requires:**
- DiamondTips_DiamondWindowByName
**Snippet:**
```lua
require("DiamondTips_DiamondWindowByName")
local DiamondWindow = {}
local uis, contentPane, notShopReopen

function DiamondWindow.ReInitData()
end

function DiamondWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.DiamondWindow.package, WinResConfig.DiamondWindow.comName, function(com)
    contentPane = com
```

---

## BCD/DispatchNumberWindow.lua.lua
**Functions:**
- DispatchNumberWindow.ReInitData
- DispatchNumberWindow.OnInit
- DispatchNumberWindow.InitText
- DispatchNumberWindow.UpdateInfo
- DispatchNumberWindow.GetGesture
- DispatchNumberWindow.InitBtn
- DispatchNumberWindow.CloseWindow
- DispatchNumberWindow.OnShown
- DispatchNumberWindow.OnHide
- DispatchNumberWindow.OnClose
- DispatchNumberWindow.HandleMessage
**Requires:**
- Message_DispatchNumberWindowByName
**Snippet:**
```lua
require("Message_DispatchNumberWindowByName")
local DispatchNumberWindow = {}
local uis, contentPane

function DispatchNumberWindow.ReInitData()
end

local stageId, buyNum, valueMin, valueMax, perCostValue

function DispatchNumberWindow.OnInit(bridgeObj)
```

---

## BCD/DungeonInfoWindow.lua.lua
**Functions:**
- DungeonInfoWindow.OnInit
- DungeonInfoWindow.InitShow
- DungeonInfoWindow.UpdateTextDisplay
- DungeonInfoWindow.InitUiInfo
- collection.WordExplainList.itemRenderer
- DungeonInfoWindow.ShowBuffList
- DungeonInfoWindow.InitStageCost
- DungeonInfoWindow.GetMonsterId
- DungeonInfoWindow.GetConfig
- DungeonInfoWindow.InitMonster
- collection.MonsterRegion.MonsterList.itemRenderer
- DungeonInfoWindow.MonsterHeadOnClick
- DungeonInfoWindow.GetSkillId
- DungeonInfoWindow.SufficientQuantity
- DungeonInfoWindow.StageOutOfDate
- DungeonInfoWindow.EnterBattle
- DungeonInfoWindow.AiBattleOnClick
- DungeonInfoWindow.UpdateSweep
- DungeonInfoWindow.UpdateSimulate
- DungeonInfoWindow.CloseWindow
- DungeonInfoWindow.InitBtn
- DungeonInfoWindow.HandleMessage
- DungeonInfoWindow.UpdateMultiDropInfo
- list.itemRenderer
- DungeonInfoWindow.UpdateMultiple
- DungeonInfoWindow.OnShown
- DungeonInfoWindow.OnClose
**Requires:**
- DungeonInfo_DungeonInfoWindowByName
**Snippet:**
```lua
require("DungeonInfo_DungeonInfoWindowByName")
local DungeonInfoWindow = {}
local uis, stageData, paramInfo, contentPane, collection, lastBtn, isInitMonster, itemDrops, numBol, closeFunc

function DungeonInfoWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.DungeonInfoWindow.package, WinResConfig.DungeonInfoWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetDungeonInfo_DungeonInfoWindowUis(contentPane)
    collection = uis.Main.DungeonInfoTips.CollectionRegion
```

---

## BCD/DungeonInfo_AiBattleBtnByName.lua.lua
**Functions:**
- GetDungeonInfo_AiBattleBtnUis
**Snippet:**
```lua
function GetDungeonInfo_AiBattleBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_BadgeBtnByName.lua.lua
**Functions:**
- GetDungeonInfo_BadgeBtnUis
**Snippet:**
```lua
function GetDungeonInfo_BadgeBtnUis(ui)
  local uis = {}
  
  uis.IconLoader = ui:GetChild("IconLoader")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_BattleBtnRegionByName.lua.lua
**Functions:**
- GetDungeonInfo_BattleBtnRegionUis
**Requires:**
- DungeonInfo_EnergyLabelByName
**Snippet:**
```lua
require("DungeonInfo_EnergyLabelByName")

function GetDungeonInfo_BattleBtnRegionUis(ui)
  local uis = {}
  uis.Battle_B_Btn = ui:GetChild("Battle_B_Btn")
  uis.AiBattleBtn = ui:GetChild("AiBattleBtn")
  uis.Battle_S_Btn = ui:GetChild("Battle_S_Btn")
  uis.EnergyLabel = GetDungeonInfo_EnergyLabelUis(ui:GetChild("EnergyLabel"))
  uis.SimulatedBattleBtn = ui:GetChild("SimulatedBattleBtn")
  uis.c1Ctr = ui:GetController("c1")
```

---

## BCD/DungeonInfo_BattleRecordBtnByName.lua.lua
**Functions:**
- GetDungeonInfo_BattleRecordBtnUis
**Snippet:**
```lua
function GetDungeonInfo_BattleRecordBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_Battle_B_BtnByName.lua.lua
**Functions:**
- GetDungeonInfo_Battle_B_BtnUis
**Snippet:**
```lua
function GetDungeonInfo_Battle_B_BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_Battle_S_BtnByName.lua.lua
**Functions:**
- GetDungeonInfo_Battle_S_BtnUis
**Snippet:**
```lua
function GetDungeonInfo_Battle_S_BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_BossHpByName.lua.lua
**Functions:**
- GetDungeonInfo_BossHpUis
**Snippet:**
```lua
function GetDungeonInfo_BossHpUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.BossHpProgressBar = ui:GetChild("BossHpProgressBar")
  uis.HpTxt = ui:GetChild("HpTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_BossHpProgressBarByName.lua.lua
**Functions:**
- GetDungeonInfo_BossHpProgressBarUis
**Requires:**
- DungeonInfo_BossHpProgressFillByName
**Snippet:**
```lua
require("DungeonInfo_BossHpProgressFillByName")

function GetDungeonInfo_BossHpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetDungeonInfo_BossHpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_BossHpProgressFillByName.lua.lua
**Functions:**
- GetDungeonInfo_BossHpProgressFillUis
**Snippet:**
```lua
function GetDungeonInfo_BossHpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_BossInfoByName.lua.lua
**Functions:**
- GetDungeonInfo_BossInfoUis
**Requires:**
- DungeonInfo_BossHpByName
**Snippet:**
```lua
require("DungeonInfo_BossHpByName")

function GetDungeonInfo_BossInfoUis(ui)
  local uis = {}
  uis.BossHp = GetDungeonInfo_BossHpUis(ui:GetChild("BossHp"))
  uis.RankList = ui:GetChild("RankList")
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_BossRegionByName.lua.lua
**Functions:**
- GetDungeonInfo_BossRegionUis
**Requires:**
- DungeonInfo_BossInfoByName
- DungeonInfo_PlayerInfoRegionByName
**Snippet:**
```lua
require("DungeonInfo_BossInfoByName")
require("DungeonInfo_PlayerInfoRegionByName")

function GetDungeonInfo_BossRegionUis(ui)
  local uis = {}
  uis.PlayerRankBtn = ui:GetChild("PlayerRankBtn")
  uis.BattleRecordBtn = ui:GetChild("BattleRecordBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.WordExplainList = ui:GetChild("WordExplainList")
  uis.BossInfo = GetDungeonInfo_BossInfoUis(ui:GetChild("BossInfo"))
```

---

## BCD/DungeonInfo_CollectionRegionByName.lua.lua
**Functions:**
- GetDungeonInfo_CollectionRegionUis
**Requires:**
- DungeonInfo_ExpeditionRegionByName
- DungeonInfo_RewardShowByName
- DungeonInfo_BossRegionByName
**Snippet:**
```lua
require("DungeonInfo_ExpeditionRegionByName")
require("DungeonInfo_RewardShowByName")
require("DungeonInfo_BossRegionByName")

function GetDungeonInfo_CollectionRegionUis(ui)
  local uis = {}
  uis.WordExplainList = ui:GetChild("WordExplainList")
  uis.ExpeditionRegion = GetDungeonInfo_ExpeditionRegionUis(ui:GetChild("ExpeditionRegion"))
  uis.RewardShow = GetDungeonInfo_RewardShowUis(ui:GetChild("RewardShow"))
  uis.BossRegion = GetDungeonInfo_BossRegionUis(ui:GetChild("BossRegion"))
```

---

## BCD/DungeonInfo_CopyBtnByName.lua.lua
**Functions:**
- GetDungeonInfo_CopyBtnUis
**Snippet:**
```lua
function GetDungeonInfo_CopyBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_DungeonInfoByName.lua.lua
**Functions:**
- GetDungeonInfo_DungeonInfoUis
**Requires:**
- DungeonInfo_DungeonInfoTipsByName
**Snippet:**
```lua
require("DungeonInfo_DungeonInfoTipsByName")

function GetDungeonInfo_DungeonInfoUis(ui)
  local uis = {}
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.DungeonInfoTips = GetDungeonInfo_DungeonInfoTipsUis(ui:GetChild("DungeonInfoTips"))
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_DungeonInfoTipsByName.lua.lua
**Functions:**
- GetDungeonInfo_DungeonInfoTipsUis
**Requires:**
- DungeonInfo_TitleByName
- DungeonInfo_CollectionRegionByName
- DungeonInfo_BattleBtnRegionByName
**Snippet:**
```lua
require("DungeonInfo_TitleByName")
require("DungeonInfo_CollectionRegionByName")
require("DungeonInfo_BattleBtnRegionByName")

function GetDungeonInfo_DungeonInfoTipsUis(ui)
  local uis = {}
  uis.Title = GetDungeonInfo_TitleUis(ui:GetChild("Title"))
  uis.CollectionRegion = GetDungeonInfo_CollectionRegionUis(ui:GetChild("CollectionRegion"))
  uis.BattleBtnRegion = GetDungeonInfo_BattleBtnRegionUis(ui:GetChild("BattleBtnRegion"))
  uis.NumberLabelList = ui:GetChild("NumberLabelList")
```

---

## BCD/DungeonInfo_DungeonInfoWindowByName.lua.lua
**Functions:**
- GetDungeonInfo_DungeonInfoWindowUis
**Requires:**
- DungeonInfo_DungeonInfoByName
**Snippet:**
```lua
require("DungeonInfo_DungeonInfoByName")

function GetDungeonInfo_DungeonInfoWindowUis(ui)
  local uis = {}
  uis.Main = GetDungeonInfo_DungeonInfoUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_EnergyLabelByName.lua.lua
**Functions:**
- GetDungeonInfo_EnergyLabelUis
**Snippet:**
```lua
function GetDungeonInfo_EnergyLabelUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_ExpeditionRegionByName.lua.lua
**Functions:**
- GetDungeonInfo_ExpeditionRegionUis
**Snippet:**
```lua
function GetDungeonInfo_ExpeditionRegionUis(ui)
  local uis = {}
  
  uis.SkillList = ui:GetChild("SkillList")
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_ExpeditionSkillByName.lua.lua
**Functions:**
- GetDungeonInfo_ExpeditionSkillUis
**Snippet:**
```lua
function GetDungeonInfo_ExpeditionSkillUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_HeadBtnBgByName.lua.lua
**Functions:**
- GetDungeonInfo_HeadBtnBgUis
**Snippet:**
```lua
function GetDungeonInfo_HeadBtnBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_HeadBtnByName.lua.lua
**Functions:**
- GetDungeonInfo_HeadBtnUis
**Requires:**
- DungeonInfo_HeadBtnBgByName
**Snippet:**
```lua
require("DungeonInfo_HeadBtnBgByName")

function GetDungeonInfo_HeadBtnUis(ui)
  local uis = {}
  uis.HeadBtnBg = GetDungeonInfo_HeadBtnBgUis(ui:GetChild("HeadBtnBg"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
```

---

## BCD/DungeonInfo_ItemFrameByName.lua.lua
**Functions:**
- GetDungeonInfo_ItemFrameUis
**Requires:**
- CommonResource_ItemCardPicByName
- DungeonInfo_ItemLabelByName
**Snippet:**
```lua
require("CommonResource_ItemCardPicByName")
require("DungeonInfo_ItemLabelByName")

function GetDungeonInfo_ItemFrameUis(ui)
  local uis = {}
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.ItemCardPic = GetCommonResource_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.ItemLabel = GetDungeonInfo_ItemLabelUis(ui:GetChild("ItemLabel"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## BCD/DungeonInfo_ItemLabelByName.lua.lua
**Functions:**
- GetDungeonInfo_ItemLabelUis
**Snippet:**
```lua
function GetDungeonInfo_ItemLabelUis(ui)
  local uis = {}
  
  uis.LabelWordTxt = ui:GetChild("LabelWordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_NumberLabel1ByName.lua.lua
**Functions:**
- GetDungeonInfo_NumberLabel1Uis
**Snippet:**
```lua
function GetDungeonInfo_NumberLabel1Uis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_NumberLabel2ByName.lua.lua
**Functions:**
- GetDungeonInfo_NumberLabel2Uis
**Snippet:**
```lua
function GetDungeonInfo_NumberLabel2Uis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_PlayBtnByName.lua.lua
**Functions:**
- GetDungeonInfo_PlayBtnUis
**Snippet:**
```lua
function GetDungeonInfo_PlayBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_PlayerATKByName.lua.lua
**Functions:**
- GetDungeonInfo_PlayerATKUis
**Snippet:**
```lua
function GetDungeonInfo_PlayerATKUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_PlayerBgAni1ByName.lua.lua
**Functions:**
- GetDungeonInfo_PlayerBgAni1Uis
**Snippet:**
```lua
function GetDungeonInfo_PlayerBgAni1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_PlayerBgAni2ByName.lua.lua
**Functions:**
- GetDungeonInfo_PlayerBgAni2Uis
**Snippet:**
```lua
function GetDungeonInfo_PlayerBgAni2Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_PlayerInfoAniByName.lua.lua
**Functions:**
- GetDungeonInfo_PlayerInfoAniUis
**Requires:**
- DungeonInfo_PlayerInfoByName
**Snippet:**
```lua
require("DungeonInfo_PlayerInfoByName")

function GetDungeonInfo_PlayerInfoAniUis(ui)
  local uis = {}
  uis.PlayerInfo = GetDungeonInfo_PlayerInfoUis(ui:GetChild("PlayerInfo"))
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_PlayerInfoByName.lua.lua
**Functions:**
- GetDungeonInfo_PlayerInfoUis
**Requires:**
- DungeonInfo_RankNumberByName
- DungeonInfo_PlayerATKByName
- DungeonInfo_PlayerTimeByName
**Snippet:**
```lua
require("DungeonInfo_RankNumberByName")
require("DungeonInfo_PlayerATKByName")
require("DungeonInfo_PlayerTimeByName")

function GetDungeonInfo_PlayerInfoUis(ui)
  local uis = {}
  uis.RankNumber = GetDungeonInfo_RankNumberUis(ui:GetChild("RankNumber"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SendBtn = ui:GetChild("SendBtn")
  uis.CopyBtn = ui:GetChild("CopyBtn")
```

---

## BCD/DungeonInfo_PlayerInfoRegionByName.lua.lua
**Functions:**
- GetDungeonInfo_PlayerInfoRegionUis
**Snippet:**
```lua
function GetDungeonInfo_PlayerInfoRegionUis(ui)
  local uis = {}
  
  uis.PlayerLabel1Btn = ui:GetChild("PlayerLabel1Btn")
  uis.PlayerLabel2Btn = ui:GetChild("PlayerLabel2Btn")
  uis.InfoList = ui:GetChild("InfoList")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_PlayerLabel1BtnByName.lua.lua
**Functions:**
- GetDungeonInfo_PlayerLabel1BtnUis
**Requires:**
- DungeonInfo_PlayerBgAni1ByName
**Snippet:**
```lua
require("DungeonInfo_PlayerBgAni1ByName")

function GetDungeonInfo_PlayerLabel1BtnUis(ui)
  local uis = {}
  uis.BgAni = GetDungeonInfo_PlayerBgAni1Uis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## BCD/DungeonInfo_PlayerLabel2BtnByName.lua.lua
**Functions:**
- GetDungeonInfo_PlayerLabel2BtnUis
**Requires:**
- DungeonInfo_PlayerBgAni2ByName
**Snippet:**
```lua
require("DungeonInfo_PlayerBgAni2ByName")

function GetDungeonInfo_PlayerLabel2BtnUis(ui)
  local uis = {}
  uis.BgAni = GetDungeonInfo_PlayerBgAni2Uis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## BCD/DungeonInfo_PlayerRankBtnByName.lua.lua
**Functions:**
- GetDungeonInfo_PlayerRankBtnUis
**Snippet:**
```lua
function GetDungeonInfo_PlayerRankBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_PlayerTimeByName.lua.lua
**Functions:**
- GetDungeonInfo_PlayerTimeUis
**Snippet:**
```lua
function GetDungeonInfo_PlayerTimeUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_RankAniByName.lua.lua
**Functions:**
- GetDungeonInfo_RankAniUis
**Requires:**
- DungeonInfo_RankByName
**Snippet:**
```lua
require("DungeonInfo_RankByName")

function GetDungeonInfo_RankAniUis(ui)
  local uis = {}
  uis.Rank = GetDungeonInfo_RankUis(ui:GetChild("Rank"))
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_RankByName.lua.lua
**Functions:**
- GetDungeonInfo_RankUis
**Requires:**
- DungeonInfo_RankNumberByName
**Snippet:**
```lua
require("DungeonInfo_RankNumberByName")

function GetDungeonInfo_RankUis(ui)
  local uis = {}
  uis.RankNumber = GetDungeonInfo_RankNumberUis(ui:GetChild("RankNumber"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_RankNumberByName.lua.lua
**Functions:**
- GetDungeonInfo_RankNumberUis
**Snippet:**
```lua
function GetDungeonInfo_RankNumberUis(ui)
  local uis = {}
  
  uis.RankTxt = ui:GetChild("RankTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_ReturnBtnByName.lua.lua
**Functions:**
- GetDungeonInfo_ReturnBtnUis
**Snippet:**
```lua
function GetDungeonInfo_ReturnBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_RewardShowByName.lua.lua
**Functions:**
- GetDungeonInfo_RewardShowUis
**Snippet:**
```lua
function GetDungeonInfo_RewardShowUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_SendBtnByName.lua.lua
**Functions:**
- GetDungeonInfo_SendBtnUis
**Snippet:**
```lua
function GetDungeonInfo_SendBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_SimulatedBattleBtnByName.lua.lua
**Functions:**
- GetDungeonInfo_SimulatedBattleBtnUis
**Snippet:**
```lua
function GetDungeonInfo_SimulatedBattleBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## BCD/DungeonInfo_TitleByName.lua.lua
**Functions:**
- GetDungeonInfo_TitleUis
**Snippet:**
```lua
function GetDungeonInfo_TitleUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.OrderTxt = ui:GetChild("OrderTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## BCD/DungeonInfo_WordExplainByName.lua.lua
**Functions:**
- GetDungeonInfo_WordExplainUis
**Snippet:**
```lua
function GetDungeonInfo_WordExplainUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---
