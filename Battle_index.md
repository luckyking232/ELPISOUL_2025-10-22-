# Battle

## Battle/BattleAction.lua.lua
**Functions:**
- BattleAction.InitLocalVar
- BattleAction.DealPreBattle
- BattleAction.DealBuffPre
- BattleAction.DealUnitBasicBuff
- BattleAction.DealStart
- BattleAction.DealStand
- BattleAction.DealTrick
- BattleAction.DealMove
- BattleAction.DealWaitAttack
- BattleAction.DealAttack
- BattleAction.DealAttackOver
- BattleAction.DealDying
- BattleAction.DealDead
- BattleAction.DealRevive
- BattleAction.DealBeatBack
- BattleAction.DealDevour
- BattleAction.DealFear
- BattleAction.DealPortal
- BattleAction.DealSpecial
- BattleAction.DealSpecialEnd
- BattleAction.ForceChangeState
- BattleAction.DealStopAttack
- BattleAction.ClearAttackInfo
- BattleAction.DealStopMove
- BattleAction.DealSummon
- BattleAction.DealHurt
- BattleAction.DealDamageToTreat
- BattleAction.DealRageChange
- BattleAction.DealBuffSettle
- BattleAction.DealBuffRemove
- BattleAction.DealCheckSkill
- BattleAction.DealTriggerPassiveSkill
- BattleAction.DealTriggerBurstSkill
- BattleAction.DealTriggerSkill
- BattleAction.DealUnitSkill
- BattleAction.DealTriggerSkillCondition
- BattleAction.IsIgnoreTargetInRange
- BattleAction.InitBeatBackUnitData
- BattleAction.InitDevourUnitData
- BattleAction.InitFearUnitData
- BattleAction.DealMoveToAttack
- BattleAction.UpdateModelFlipWhenAttack
- BattleAction.UpdateModelTimescale
**Snippet:**
```lua
BattleAction = {}
local sqrt = math.sqrt
local t_insert = table.insert
local floor = math.floor
local ceil = math.ceil
local tonumber = tonumber
local BATTLE_STATE_ENUM = BATTLE_STATE_ENUM
local TRIGGER_CONDITION = TRIGGER_CONDITION
local BUFF_DEDUCE_TYPE = BUFF_DEDUCE_TYPE
local BUFF_SETTLE_TYPE = BUFF_SETTLE_TYPE
```

---

## Battle/BattleActionDisplay.lua.lua
**Functions:**
- BattleActionDisplay.Init
- BattleActionDisplay.ClearAction
- BattleActionDisplay.GetWaitWarningEffectIndex
- BattleActionDisplay.AddWaitDealSound
- BattleActionDisplay.AddWaitDealEffect
- BattleActionDisplay.AddWaitDealVoice
- BattleActionDisplay.AddWaitDealWarningEffect
- BattleActionDisplay.DealWaitAction
- BattleActionDisplay.InitLocalVar
- BattleActionDisplay.PlayStart
- BattleActionDisplay.PlayStand
- BattleActionDisplay.PlayMove
- BattleActionDisplay.PlayWaitAttack
- BattleActionDisplay.GetUnitRotation
- BattleActionDisplay.PlayAttack
- BattleActionDisplay.PlayDead
- BattleActionDisplay.PlayRevive
- BattleActionDisplay.PlayDestroy
- trackEntry.completeAction
- BattleActionDisplay.PlayStun
- BattleActionDisplay.PlayBeatBack
- BattleActionDisplay.PlayDevour
- BattleActionDisplay.PlayFear
- BattleActionDisplay.PlaySpecial
- BattleActionDisplay.PlayPersistCast
- BattleActionDisplay.PlayHurt
- BattleActionDisplay.PlayRandomHit
- BattleActionDisplay.PlayRage
- BattleActionDisplay.PlayBuffWords
- BattleActionDisplay.PlayBuffEffect
- BattleActionDisplay.PlayHitEffect
- BattleActionDisplay.PlayBuffIconRefresh
- BattleActionDisplay.ClearAttackDisplay
- BattleActionDisplay.ClearSkillEffect
- BattleActionDisplay.UpdateModelFlipWhenAttack
- BattleActionDisplay.UpdateModelTimescale
- BattleActionDisplay.UpdateControlDisplay
- BattleActionDisplay.ShowStealthDisplay
- BattleActionDisplay.ShowFreezeDisplay
- BattleActionDisplay.ShowPetrifiedDisplay
- BattleActionDisplay.PlayBeatBackTrapState
- BattleActionDisplay.PlayTransform
**Snippet:**
```lua
BattleActionDisplay = {}
local waitSoundAction = {}
local waitVoiceAction = {}
local waitEffectAction = {}
local waitWarningEffectAction = {}
local waitWarningEffectIndex

function BattleActionDisplay.Init()
  BattleActionDisplay.ClearAction()
end
```

---

## Battle/BattleAxisWindow.lua.lua
**Functions:**
- BattleAxisWindow.ReInitData
- BattleAxisWindow.OnInit
- BattleAxisWindow.CreateWaveList
- list.itemRenderer
- BattleAxisWindow.ClickRoundBtn
- BattleAxisWindow.UpdateBattleData
- BattleAxisWindow.IsWin
- BattleAxisWindow.UpdateAll
- BattleAxisWindow.InitTimelineData
- BattleAxisWindow.InitComp
- BattleAxisWindow.UpdateInfo
- BattleAxisWindow.CreateHand
- BattleAxisWindow.CreateHead
- BattleAxisWindow.UpdateHead
- BattleAxisWindow.CreateBurst
- BattleAxisWindow.CreateManuallySkill
- BattleAxisWindow.CreateUniqueSkill
- BattleAxisWindow.CreateBurstCardSkill
- BattleAxisWindow.CreateSmallSkill
- BattleAxisWindow.CreateDeathSkill
- BattleAxisWindow.UpdateHeadVisible
- BattleAxisWindow.InitBtn
- BattleAxisWindow.ClickUniqueSkillBtn
- BattleAxisWindow.ClickSpecialSkillBtn
- BattleAxisWindow.ClickDeathBtn
- BattleAxisWindow.ClickManuallySkillBtn
- BattleAxisWindow.ClickHand
- BattleAxisWindow.ShowSkillTips
- BattleAxisWindow.IsMonster
- BattleAxisWindow.CloseSkillTips
- BattleAxisWindow.GetShowHeadDataList
- BattleAxisWindow.CloseHeadTips
- BattleAxisWindow.OnShown
- BattleAxisWindow.OnHide
- BattleAxisWindow.OnClose
- BattleAxisWindow.HandleMessage
**Requires:**
- BattleData_BattleAxisWindowByName
**Snippet:**
```lua
require("BattleData_BattleAxisWindowByName")
local BattleAxisWindow = {}
local uis, contentPane, timelineCom, showBurstCardSkill, showSpecialSkill, showDeath, showManuallySkill, totalFrame, totalSecond
local UNIT_INTERVAL = 10
local UNIT_PIXEL = 720
local MIN_INTERVAL = 0.1
local MIN_FRAME_INTERVAL = BATTLE_CONFIG_ENUM.FIXED_FPS * MIN_INTERVAL
local PIXEL_PER_INTERVAL = MIN_INTERVAL * UNIT_PIXEL / UNIT_INTERVAL
local showRange = 1 / MIN_INTERVAL
local maxIndex, burstSkillInfoList, burstCardSkillInfoList, uniqueSkillInfoList, smallSkillInfoList, deathInfoList, manuallySkillInfoList, burstSkillList, burstCardSkillList, uniqueSkillList, smallSkillList, deathList, manuallySkillList, curChallengeStageRsp, challengeStageRspList, curIndex, isWin
```

---

## Battle/BattleBackground.lua.lua
**Functions:**
- BattleBackground.Init
- BattleBackground.Clear
**Requires:**
- SortingHelper
**Snippet:**
```lua
BattleBackground = {
  model = nil,
  modelUp = nil,
  sound = nil
}

function BattleBackground.Init()
  local mapId = BattleScene.GetMapId()
  local mapConfig = TableData.GetConfig(mapId, "BaseMap")
  local model = ResourceManager.Instantiate(ModelUtil.GetFullPath(mapConfig.background_path, RES_PATH_PREFIX.MAP_BACKGROUND))
```

---

## Battle/BattleBomb.lua.lua
**Functions:**
- BattleBomb.InitLocalVar
- BattleBomb.NewBomb
- bomb:Init
- bomb:ResetSplitHurtInfo
- bomb:CreateModel
- bomb:UpdateDisplay
- bomb:UpdateEffectLine
- bomb:AddBuff
- bomb:RemoveBuff
- bomb:UpdateCachedBuffEffect
- bomb:Update
- bomb:SetVisible
- bomb:DealHurt
- bomb:UpdateSortingOrder
- bomb:Destroy
- bomb:RemoveAllBuff
**Snippet:**
```lua
BattleBomb = {}

function BattleBomb.InitLocalVar()
end

function BattleBomb.NewBomb(showDisplayConfig, fromUnit, targetUnit, skillId, subSkillId, bombExtraParams)
  local bomb = {
    inited = false,
    id = nil,
    uid = nil,
```

---

## Battle/BattleBuff.lua.lua
**Functions:**
- BattleBuff.InitLocalVar
- BattleBuff.NewBuff
- buff:Init
- buff:Clear
- buff:SetDeduceTriggerUnitUid
- buff:AddTargetUid
- buff:IsAlreadyInTarget
- buff:ClearAlreadyInTarget
- buff:ContainEffectIdBeforeSettle
- buff:ContainEffectTagBeforeSettle
- buff:Settle
- buff:Deduce
- buff:DealActiveForeverEffect
- buff:DealFireJump
- buff:DealSummon
- buff:ContainEffectId
- buff:GetEffectListById
- buff:GetEffectTotalValue
- buff:GetAttributeValue
- buff:ContainEffectTag
- buff:ContainPersistentDamage
- buff:ContainControl
- buff:ContainAttributeId
- buff:GetAllAttributeValue
- buff:UpdateDeduceValue
- buff:DealClean
- buff:UpdateEffectValue
- buff:Reset
- buff:TriggerRemove
- buff:Remove
- buff:TriggerUnitAttrChanged
- buff:TriggerUnitShieldGot
- buff:IsShieldSpecialUsedUp
- buff:IsShieldUsedUp
- buff:IsTenacityUsedUp
- buff:NeedRemove
- buff:Update
- buff:CanSettle
- buff:TestCondition
- buff:CanEffective
- buff:IsBuffImmune
- buff:SetState
- buff:UpdateDisplay
- buff:Destroy
**Snippet:**
```lua
BattleBuff = {}

function BattleBuff.InitLocalVar()
end

function BattleBuff.NewBuff(_id, _from, _to, _settleNow, _extraParams, _delayParams)
  local buff = {}
  local tonumber = tonumber
  local ATTR_ENUM = ATTR_ENUM
  local ATTR_ID = ProtoEnum.ATTR_ID
```

---

## Battle/BattleBuffEffect.lua.lua
**Functions:**
- BattleBuffEffect.InitLocalVar
- BattleBuffEffect.NewEffect
- effect:Init
- effect:UpdateValue
- effect:ContainPersistentDamage
- effect:UpdateShieldValue
- effect:UpdateShieldSpecialValue
- effect:UpdateTenacityValue
- effect:IsValidAttributeEffect
- effect:IsEffectiveForSkill
- effect:Destroy
- BattleBuffEffect.DealBeAffectedWithEffect
- BattleBuffEffect.GetEffectValue
**Snippet:**
```lua
BattleBuffEffect = {}
local tonumber = tonumber
local floor = math.floor
local ceil = math.ceil
local BUFF_EFFECT_VALUE = BUFF_EFFECT_VALUE
local BATTLE_DEPEND_TYPE = BATTLE_DEPEND_TYPE
local EFFECT_ATTR_CAL_TYPE = EFFECT_ATTR_CAL_TYPE
local BUFF_EFFECT_ID = BUFF_EFFECT_ID
local ATTR_ENUM = ATTR_ENUM
local ATTR_ID = ProtoEnum.ATTR_ID
```

---

## Battle/BattleBuffMgr.lua.lua
**Functions:**
- BattleBuffMgr.InitLocalVar
- BattleBuffMgr.Init
- BattleBuffMgr.GetForceControlEffectIdList
- BattleBuffMgr.NewBuff
- BattleBuffMgr.AddToBuffList
- BattleBuffMgr.RemoveFromBuffList
- BattleBuffMgr.ClearBuffByBuffId
- BattleBuffMgr.ClearBuffByEffectId
- BattleBuffMgr.ClearAllBuff
- BattleBuffMgr.RegisterSettleListener
- BattleBuffMgr.RegisterDeduceListener
- BattleBuffMgr.RegisterRemoveListener
- BattleBuffMgr.UnRegisterSettleListenerByUnitUid
- BattleBuffMgr.UnRegisterSettleListener
- BattleBuffMgr.UnRegisterDeduceListener
- BattleBuffMgr.UnRegisterRemoveListener
- BattleBuffMgr.RefreshRegisterDeduceListener
- BattleBuffMgr.TriggerRemoveListener
- BattleBuffMgr.TriggerUnitListener
- BattleBuffMgr.TriggerBulletListener
- BattleBuffMgr.TriggerBombListener
- BattleBuffMgr.TriggerCampListener
- BattleBuffMgr.TriggerListener
- BattleBuffMgr.TriggerListenerBuffAdd
- BattleBuffMgr.GetBuffGlobalIndex
- BattleBuffMgr.GetAllBuff
- BattleBuffMgr.GetAllBurstBuff
- BattleBuffMgr.GetAllBulletBuff
- BattleBuffMgr.GetAllBombBuff
- BattleBuffMgr.DealBulletDirectDamage
- BattleBuffMgr.DealBulletFinalDamageAdd
- BattleBuffMgr.AnalysisBuffList
- BattleBuffMgr.GetBuffByUid
- BattleBuffMgr.GetSavedBuffList
- BattleBuffMgr.UpdateAllBuff
- BattleBuffMgr.GetListenerSettleList
- BattleBuffMgr.GetListenerRemoveList
- BattleBuffMgr.GetListenerDeduceList
- BattleBuffMgr.GetBuffValue
- BattleBuffMgr.GetValueById
- BattleBuffMgr.GetValueByCampAndId
- BattleBuffMgr.GetBuffCountByUnitAndTag
- BattleBuffMgr.GetBuffCountByCampAndId
- BattleBuffMgr.GetEffectCountByCampAndTag
- BattleBuffMgr.GetSummonCountByCamp
- BattleBuffMgr.GetAliveUnitCountByCamp
- BattleBuffMgr.UpdateUnitBuffShield
- BattleBuffMgr.GetUnitListContainEffect
- BattleBuffMgr.ContainEffectId
- BattleBuffMgr.GetContainedEffect
- BattleBuffMgr.GetBombContainedEffect
- BattleBuffMgr.GetSettledBuffByUnitAndId
- BattleBuffMgr.GetSettledBuffByUnitAndType
- BattleBuffMgr.GetSettledBuffByUnitAndEffectID
- BattleBuffMgr.GetSettledBuffByUnitAndEffectTag
- BattleBuffMgr.GetSettledBuffByCampAndId
- BattleBuffMgr.GetSettledBuffByCampAndType
- BattleBuffMgr.GetSettledBuffByCampAndEffectID
- BattleBuffMgr.GetSettledBuffByCampAndEffectTag
- BattleBuffMgr.IsContainBuffFromBuffUid
- BattleBuffMgr.IsBuffImmune
- BattleBuffMgr.IsUnitUntreatable
- BattleBuffMgr.IsUnitUnyielding
- BattleBuffMgr.IsUnitImmuneAllHurt
- BattleBuffMgr.IsUnitInvincible
- BattleBuffMgr.IsUnitStealth
- BattleBuffMgr.IsUnitImmuneBuffHurt
**Snippet:**
```lua
BattleBuffMgr = {}
local t_remove = table.remove
local t_sort = table.sort
local tonumber = tonumber
local pairs = pairs
local listenerSettleList = {}
local listenerDeduceList = {}
local listenerRemoveList = {}
local savedBuffList = {}
local sortBuffList = {}
```

---

## Battle/BattleBuffTips_BuffCountByName.lua.lua
**Functions:**
- GetBattleBuffTips_BuffCountUis
**Snippet:**
```lua
function GetBattleBuffTips_BuffCountUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.BuffTxt = ui:GetChild("BuffTxt")
  uis.DeBuffTxt = ui:GetChild("DeBuffTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleBuffTips_BuffInfoByName.lua.lua
**Functions:**
- GetBattleBuffTips_BuffInfoUis
**Snippet:**
```lua
function GetBattleBuffTips_BuffInfoUis(ui)
  local uis = {}
  
  uis.BuffLoader = ui:GetChild("BuffLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleBuffTips_BuffNothingByName.lua.lua
**Functions:**
- GetBattleBuffTips_BuffNothingUis
**Snippet:**
```lua
function GetBattleBuffTips_BuffNothingUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleBuffTips_BuffRegionByName.lua.lua
**Functions:**
- GetBattleBuffTips_BuffRegionUis
**Requires:**
- BattleBuffTips_BuffNothingByName
- BattleBuffTips_BuffTitleByName
**Snippet:**
```lua
require("BattleBuffTips_BuffNothingByName")
require("BattleBuffTips_BuffTitleByName")

function GetBattleBuffTips_BuffRegionUis(ui)
  local uis = {}
  uis.BuffNothing = GetBattleBuffTips_BuffNothingUis(ui:GetChild("BuffNothing"))
  uis.BuffTitle = GetBattleBuffTips_BuffTitleUis(ui:GetChild("BuffTitle"))
  uis.BuffList = ui:GetChild("BuffList")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Battle/BattleBuffTips_BuffTipsByName.lua.lua
**Functions:**
- GetBattleBuffTips_BuffTipsUis
**Requires:**
- BattleBuffTips_CardShowByName
- BattleBuffTips_MonterShowByName
- BattleBuffTips_BuffCountByName
**Snippet:**
```lua
require("BattleBuffTips_CardShowByName")
require("BattleBuffTips_MonterShowByName")
require("BattleBuffTips_BuffCountByName")

function GetBattleBuffTips_BuffTipsUis(ui)
  local uis = {}
  uis.CardShow = GetBattleBuffTips_CardShowUis(ui:GetChild("CardShow"))
  uis.MonterShow = GetBattleBuffTips_MonterShowUis(ui:GetChild("MonterShow"))
  uis.BuffCount = GetBattleBuffTips_BuffCountUis(ui:GetChild("BuffCount"))
  uis.HeadList = ui:GetChild("HeadList")
```

---

## Battle/BattleBuffTips_BuffTipsWindowByName.lua.lua
**Functions:**
- GetBattleBuffTips_BuffTipsWindowUis
**Requires:**
- BattleBuffTips_BuffTipsByName
**Snippet:**
```lua
require("BattleBuffTips_BuffTipsByName")

function GetBattleBuffTips_BuffTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetBattleBuffTips_BuffTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Battle/BattleBuffTips_BuffTitleByName.lua.lua
**Functions:**
- GetBattleBuffTips_BuffTitleUis
**Snippet:**
```lua
function GetBattleBuffTips_BuffTitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleBuffTips_CardHeadBgByName.lua.lua
**Functions:**
- GetBattleBuffTips_CardHeadBgUis
**Snippet:**
```lua
function GetBattleBuffTips_CardHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleBuffTips_CardHeadByName.lua.lua
**Functions:**
- GetBattleBuffTips_CardHeadUis
**Requires:**
- BattleBuffTips_CardHeadBgByName
- CommonResource_OccupationByName
**Snippet:**
```lua
require("BattleBuffTips_CardHeadBgByName")
require("CommonResource_OccupationByName")

function GetBattleBuffTips_CardHeadUis(ui)
  local uis = {}
  uis.Pic = GetBattleBuffTips_CardHeadBgUis(ui:GetChild("Pic"))
  uis.Occupation = GetCommonResource_OccupationUis(ui:GetChild("Occupation"))
  uis.ElementList = ui:GetChild("ElementList")
  uis.HpProgressBar = ui:GetChild("HpProgressBar")
  uis.BuffList = ui:GetChild("BuffList")
```

---

## Battle/BattleBuffTips_CardShowByName.lua.lua
**Functions:**
- GetBattleBuffTips_CardShowUis
**Snippet:**
```lua
function GetBattleBuffTips_CardShowUis(ui)
  local uis = {}
  
  uis.ShowHolder = ui:GetChild("ShowHolder")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleBuffTips_HeadBtnByName.lua.lua
**Functions:**
- GetBattleBuffTips_HeadBtnUis
**Requires:**
- BattleBuffTips_CardHeadByName
- BattleBuffTips_MonsterHeadByName
**Snippet:**
```lua
require("BattleBuffTips_CardHeadByName")
require("BattleBuffTips_MonsterHeadByName")

function GetBattleBuffTips_HeadBtnUis(ui)
  local uis = {}
  uis.CardHead = GetBattleBuffTips_CardHeadUis(ui:GetChild("CardHead"))
  uis.MonsterHead = GetBattleBuffTips_MonsterHeadUis(ui:GetChild("MonsterHead"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Battle/BattleBuffTips_HeadSwitchBtnByName.lua.lua
**Functions:**
- GetBattleBuffTips_HeadSwitchBtnUis
**Snippet:**
```lua
function GetBattleBuffTips_HeadSwitchBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleBuffTips_HpProgressBarByName.lua.lua
**Functions:**
- GetBattleBuffTips_HpProgressBarUis
**Snippet:**
```lua
function GetBattleBuffTips_HpProgressBarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/BattleBuffTips_HpProgressFillByName.lua.lua
**Functions:**
- GetBattleBuffTips_HpProgressFillUis
**Snippet:**
```lua
function GetBattleBuffTips_HpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/BattleBuffTips_MonsterHeadBgByName.lua.lua
**Functions:**
- GetBattleBuffTips_MonsterHeadBgUis
**Snippet:**
```lua
function GetBattleBuffTips_MonsterHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleBuffTips_MonsterHeadByName.lua.lua
**Functions:**
- GetBattleBuffTips_MonsterHeadUis
**Requires:**
- BattleBuffTips_MonsterHeadBgByName
- CommonResource_OccupationByName
- BattleBuffTips_MonsterSignByName
**Snippet:**
```lua
require("BattleBuffTips_MonsterHeadBgByName")
require("CommonResource_OccupationByName")
require("BattleBuffTips_MonsterSignByName")

function GetBattleBuffTips_MonsterHeadUis(ui)
  local uis = {}
  uis.Pic = GetBattleBuffTips_MonsterHeadBgUis(ui:GetChild("Pic"))
  uis.Occupation = GetCommonResource_OccupationUis(ui:GetChild("Occupation"))
  uis.ElementList = ui:GetChild("ElementList")
  uis.HpProgressBar = ui:GetChild("HpProgressBar")
```

---

## Battle/BattleBuffTips_MonsterSignByName.lua.lua
**Functions:**
- GetBattleBuffTips_MonsterSignUis
**Snippet:**
```lua
function GetBattleBuffTips_MonsterSignUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleBuffTips_MonterShowByName.lua.lua
**Functions:**
- GetBattleBuffTips_MonterShowUis
**Snippet:**
```lua
function GetBattleBuffTips_MonterShowUis(ui)
  local uis = {}
  
  uis.ShowHolder = ui:GetChild("ShowHolder")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleBullet.lua.lua
**Functions:**
- BattleBullet.InitLocalVar
- BattleBullet.NewBullet
- bullet:Init
- bullet:CreateModel
- bullet:IsTargetInRange
- bullet:IsTargetInMoveRange
- bullet:Update
- bullet:SetVisible
- bullet:DealMove
- bullet:TriggerTargetDeadBuff
- bullet:DealHurt
- bullet:AddBuff
- bullet:RemoveBuff
- bullet:UpdateCachedBuffEffect
- bullet:SetPosition
- bullet:UpdateSortingOrder
- bullet:Destroy
- bullet:RemoveAllBuff
**Snippet:**
```lua
BattleBullet = {}
local pairs = pairs
local BATTLE_CONFIG_ENUM = BATTLE_CONFIG_ENUM

function BattleBullet.InitLocalVar()
end

local BULLET_TYPE_ENUM = {NORMAL = 1, DIRECT_MOVE = 2}

function BattleBullet.NewBullet(showDisplayConfig, fromUnit, defUnit, fromPos, toPos, subSkillId, skillId, speed, bulletExtraParams)
```

---

## Battle/BattleBurst.lua.lua
**Functions:**
- BattleBurst.InitLocalVar
- BattleBurst.NewBurst
- burst:AddBuff
- burst:RemoveBuff
- burst:Init
- burst:GetSkill
- burst:GetEnergySkillState
- burst:ChangeEnergy
- burst:ChangeEnergyAdd
- burst:UpdateEnergyPerFrame
- burst:GetEffectValue
- burst:ContainBuffId
- burst:UpdateEnergy
- burst:SaveLastActiveSkill
- burst:DealCardBurstStart
- burst:Update
- burst:DealChooseCardProcess
- burst:AddEnergySkillCard
- burst:SaveAutoManuallySkill
- burst:GetCurUnitType
- burst:StartEnergySkill
- burst:ChooseEnergySkillCard
- burst:IsAllCardCannotChooseByJob
- burst:ChooseAutoBurstSkillUnit
- burst:IsAllCardSkillDeal
- burst:DealCardBurst
- burst:ResetCardBurstWaitFrame
- burst:StopEnergySkill
- burst:ClearCardBurstSkill
- burst:UpdateEnergyFrameEnd
- burst:ClearData
- burst:DestroySkills
- burst:Destroy
**Snippet:**
```lua
BattleBurst = {}
local tonumber = tonumber
local min = math.min
local max = math.max
local BATTLE_CAMP_FLAG = BATTLE_CAMP_FLAG
local BUFF_EFFECT_ID = BUFF_EFFECT_ID

function BattleBurst.InitLocalVar()
end

```

---

## Battle/BattleBurstSkill.lua.lua
**Functions:**
- BattleBurstSkill.InitLocalVar
- BattleBurstSkill.NewSkill
- skill:GetSkillConfig
- skill:GetSkillLevelUpConfig
- skill:Init
- skill:CanAutoChosen
- skill:TriggerSkillBuff
- skill:Destroy
**Snippet:**
```lua
BattleBurstSkill = {}
local ATTR_ENUM = ATTR_ENUM
local BATTLE_UNIT_TYPE = BATTLE_UNIT_TYPE

function BattleBurstSkill.InitLocalVar()
end

function BattleBurstSkill.NewSkill(skillId, camp, burstId)
  local skill = {
    burstId = nil,
```

---

## Battle/BattleCamp.lua.lua
**Functions:**
- BattleCamp.NewCamp
- campObject:AddCanChargeUnit
- campObject:DealCharge
- campObject:AddTimePause
- campObject:AddBuff
- campObject:RemoveBuff
- campObject:Init
- campObject:Destroy
- BattleCamp.DealCampCharge
**Snippet:**
```lua
BattleCamp = {}

function BattleCamp.NewCamp(camp)
  local campObject = {
    buffUidList = {},
    triggerTimePauseCount = 0,
    canChargeUnitUidList = {}
  }
  
  function campObject:AddCanChargeUnit(unit)
```

---

## Battle/BattleChoose.lua.lua
**Functions:**
- BattleChoose.InitLocalVar
- BattleChoose.GetRangeInfo
- BattleChoose.GetTargetType
- BattleChoose.GetTargetUnitList
- BattleChoose.GetSkillTargetUnitList
- BattleChoose.GetBuffTargetUnitList
- BattleChoose.GetNearestUnit
- BattleChoose.GetUnitFor2621
- BattleChoose.GetUnitForChooseMoveTarget
- BattleChoose.GetUnitListBySide
- BattleChoose.GetTopAtkSpdUnitList
- BattleChoose.GetTopHpUnitList
- BattleChoose.GetMinHpPerUnit
- BattleChoose.GetTopAtkUnitList
- BattleChoose.GetTopMoveSpdUnitList
- BattleChoose.GetTopDefUnitList
- BattleChoose.GetSummonUnit
- BattleChoose.GetNotSummonUnit
- BattleChoose.GetSameCampCardListWithHp
- BattleChoose.GetDyingUnitList
- BattleChoose.GetUnitListByType
- BattleChoose.GetRandomUnitList
- BattleChoose.GetUnitListForUnit10064
- BattleChoose.GetGridByRatio
- BattleChoose.GetBuffMaxOverlayUnreachedCards
- BattleChoose.GetContainEffectIdCards
- BattleChoose.GetUnitListContainEffectTag
- BattleChoose.GetTopBuffEffectTagCountUnitList
- BattleChoose.GetRandomSort
- BattleChoose.GetRandomGridList
- BattleChoose.GetAllSummonByUnit
- BattleChoose.GetAllSummonBySide
- BattleChoose.GetBulletHurtUnitList
- BattleChoose.GetUnitsFor3120
**Snippet:**
```lua
BattleChoose = {}
local t_sort = table.sort
local ATTR_ENUM = ATTR_ENUM
local BATTLE_UNIT_TYPE = BATTLE_UNIT_TYPE

function BattleChoose.InitLocalVar()
end

function BattleChoose.GetRangeInfo(skillLevelUpConfig, buffConfig, fromUnit)
  local range_type, range_x, range_y
```

---

## Battle/BattleConst.lua.lua
**Snippet:**
```lua
BATTLE_STATE_ENUM = {
  START = "START",
  STAND = "STAND",
  MOVE = "MOVE",
  WAIT_ATTACK = "WAIT_ATTACK",
  ATTACK = "ATTACK",
  ATTACK_OVER = "ATTACK_OVER",
  DYING = "DYING",
  DEAD = "DEAD",
  DESTROY = "DESTROY",
```

---

## Battle/BattleControl.lua.lua
**Functions:**
- BattleControl.InitLocalVar
- BattleControl.Init
- BattleControl.Start
- BattleControl.UpdateProcess
- BattleControl.UpdateProcess_2
- BattleControl.UpdateDisplay
- BattleControl.UniqueSkillPause
- BattleControl.SlowTime
- BattleControl.Pause
- BattleControl.Continue
- BattleControl.Stop
**Snippet:**
```lua
BattleControl = {
  curFixedFrame = 0,
  curFrame = 0,
  isPause = false,
  uniqueSkillUnitUid = nil,
  delayStopBattleFrame = nil,
  timeSinceLastUpdate = 0,
  baseTimeScale = nil,
  timescaleSlowRatio = nil
}
```

---

## Battle/BattleData.lua.lua
**Functions:**
- BattleData.InitData
- BattleData.GetAllUnitData
- BattleData.SortUnitListInit
- BattleData.GetRandomForChooseGrid
- BattleData.GetRandomForChooseShowDisplay
- BattleData.GetRandomSeed
- BattleData.GetRandomSeed2
- BattleData.GetRandomForAutoSkill
- BattleData.GetRandomForDisplay
- BattleData.IsBattleNoFail
- BattleData.IsBattlePVP
- BattleData.IsGuildTrain
- BattleData.IsEffectSkill
- BattleData.Clear
- BattleData.CacheChallengeStageRsp
- BattleData.ClearCachedChallengeStageRsp
- BattleData.UpdateBattleScore
- BattleData.GetRogueAliveCountByType
- BattleData.GetSkillShowIdFromGroup
**Snippet:**
```lua
BattleData = {
  totalFixedFrames = 0,
  isAuto = false,
  speedIndex = 1,
  speedList = {},
  savedConfigPool = {},
  burstLeft = nil,
  burstRight = nil,
  battleCameraScale = nil,
  battleRootScale = nil,
```

---

## Battle/BattleDataCount.lua.lua
**Functions:**
- BattleDataCount.InitLocalVar
- BattleDataCount.Init
- BattleDataCount.PanDingKeZhiBuff
- BattleDataCount.GetSkillHurt
- BattleDataCount.DealBuffEffect
- BattleDataCount.DealSpecialDamageAdd
- BattleDataCount.GetManuallySkillHurt
**Snippet:**
```lua
BattleDataCount = {isInit = false}
local ceil = math.ceil
local floor = math.floor
local min = math.min
local max = math.max
local ATTR_ENUM = ATTR_ENUM
local BUFF_EFFECT_ID = BUFF_EFFECT_ID
local BATTLE_UNIT_TYPE = BATTLE_UNIT_TYPE
local BATTLE_SKILL_ENUM = SKILL_TYPE_ENUM
local BUFF_DEDUCE_TYPE = BUFF_DEDUCE_TYPE
```

---

## Battle/BattleDataWindow.lua.lua
**Functions:**
- BattleDataWindow.ReInitData
- BattleDataWindow.OnInit
- BattleDataWindow.CreateWaveList
- list.itemRenderer
- BattleDataWindow.ClickRoundBtn
- BattleDataWindow.UpdateBattleData
- BattleDataWindow.IsWin
- BattleDataWindow.UpdateAll
- BattleDataWindow.InitTextAndBtn
- BattleDataWindow.GetKilledCountByUid
- BattleDataWindow.InitDamageData
- BattleDataWindow.UpdateUnitInfo
- BattleDataWindow.UpdateList
- BattleDataWindow.UpdateOneItem
- BattleDataWindow.UpdateSkillInfo
- BattleDataWindow.CloseWindow
- BattleDataWindow.RefreshBtn
- BattleDataWindow.RefreshSkillBtn
- BattleDataWindow.SwitchData
- BattleDataWindow.OnShown
- BattleDataWindow.OnHide
- BattleDataWindow.OnClose
- BattleDataWindow.HandleMessage
**Requires:**
- BattleData_BattleDataWindowByName
**Snippet:**
```lua
require("BattleData_BattleDataWindowByName")
local BattleDataWindow = {}
local uis, contentPane, curDataType
local DATA_TYPE_ENUM = {UNIT = 1, SKILL = 2}
local battleData, curChallengeStageRsp, challengeStageRspList, curIndex, dataOwnComp, dataOwnSkillComp, dataEnemyComp, dataEnemySkillComp
local leftUnitDamage, rightUnitDamage = {}, {}
local leftSkillDamage, rightSkillDamage = {}, {}
local maxDamageUnit, maxDamagedUnit, maxTreatUnit, maxTreatedUnit = 0, 0, 0, 0
local maxDamageSkill, maxTreatSkill, maxShieldSkill = 0, 0, 0, 0
local isWin, leftHaveSkill, rightHaveSkill
```

---

## Battle/BattleData_AxisCardTypeByName.lua.lua
**Functions:**
- GetBattleData_AxisCardTypeUis
**Snippet:**
```lua
function GetBattleData_AxisCardTypeUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_AxisEnemyTileByName.lua.lua
**Functions:**
- GetBattleData_AxisEnemyTileUis
**Snippet:**
```lua
function GetBattleData_AxisEnemyTileUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_AxisGuildSkillBtnByName.lua.lua
**Functions:**
- GetBattleData_AxisGuildSkillBtnUis
**Requires:**
- BattleData_AxisGuildSkillTypeByName
**Snippet:**
```lua
require("BattleData_AxisGuildSkillTypeByName")

function GetBattleData_AxisGuildSkillBtnUis(ui)
  local uis = {}
  uis.GuildSkill = GetBattleData_AxisGuildSkillTypeUis(ui:GetChild("GuildSkill"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_AxisGuildSkillTypeByName.lua.lua
**Functions:**
- GetBattleData_AxisGuildSkillTypeUis
**Snippet:**
```lua
function GetBattleData_AxisGuildSkillTypeUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_AxisHeadBtnByName.lua.lua
**Functions:**
- GetBattleData_AxisHeadBtnUis
**Requires:**
- BattleData_AxisCardTypeByName
- BattleData_AxisMonsterTypeByName
- BattleData_MonsterSignByName
**Snippet:**
```lua
require("BattleData_AxisCardTypeByName")
require("BattleData_AxisMonsterTypeByName")
require("BattleData_MonsterSignByName")

function GetBattleData_AxisHeadBtnUis(ui)
  local uis = {}
  uis.PlayerHead = GetBattleData_AxisCardTypeUis(ui:GetChild("PlayerHead"))
  uis.MonsterLoader = GetBattleData_AxisMonsterTypeUis(ui:GetChild("MonsterLoader"))
  uis.MonsterSign = GetBattleData_MonsterSignUis(ui:GetChild("MonsterSign"))
  uis.buttonCtr = ui:GetController("button")
```

---

## Battle/BattleData_AxisHeadByName.lua.lua
**Functions:**
- GetBattleData_AxisHeadUis
**Requires:**
- BattleData_StateTypeByName
**Snippet:**
```lua
require("BattleData_StateTypeByName")

function GetBattleData_AxisHeadUis(ui)
  local uis = {}
  uis.HeadBtn = ui:GetChild("HeadBtn")
  uis.BuildHeadBtn = ui:GetChild("BuildHeadBtn")
  uis.GuildSkillBtn = ui:GetChild("GuildSkillBtn")
  uis.StateType = GetBattleData_StateTypeUis(ui:GetChild("StateType"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## Battle/BattleData_AxisMonsterTypeByName.lua.lua
**Functions:**
- GetBattleData_AxisMonsterTypeUis
**Snippet:**
```lua
function GetBattleData_AxisMonsterTypeUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_AxisOwnTileByName.lua.lua
**Functions:**
- GetBattleData_AxisOwnTileUis
**Snippet:**
```lua
function GetBattleData_AxisOwnTileUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_BallteGuildBoss_TimeByName.lua.lua
**Functions:**
- GetBattleData_BallteGuildBoss_TimeUis
**Snippet:**
```lua
function GetBattleData_BallteGuildBoss_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_BallteRaid_RegionByName.lua.lua
**Functions:**
- GetBattleData_BallteRaid_RegionUis
**Requires:**
- BattleData_BallteRaid_SureByName
- BattleData_BallteRaid_ResignByName
**Snippet:**
```lua
require("BattleData_BallteRaid_SureByName")
require("BattleData_BallteRaid_ResignByName")

function GetBattleData_BallteRaid_RegionUis(ui)
  local uis = {}
  uis.ResignBtn = ui:GetChild("ResignBtn")
  uis.SureBtn = ui:GetChild("SureBtn")
  uis.Sure = GetBattleData_BallteRaid_SureUis(ui:GetChild("Sure"))
  uis.Resign = GetBattleData_BallteRaid_ResignUis(ui:GetChild("Resign"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## Battle/BattleData_BallteRaid_ResignBtnByName.lua.lua
**Functions:**
- GetBattleData_BallteRaid_ResignBtnUis
**Snippet:**
```lua
function GetBattleData_BallteRaid_ResignBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_BallteRaid_ResignByName.lua.lua
**Functions:**
- GetBattleData_BallteRaid_ResignUis
**Requires:**
- BattleData_BallteRaid_ResignWordByName
**Snippet:**
```lua
require("BattleData_BallteRaid_ResignWordByName")

function GetBattleData_BallteRaid_ResignUis(ui)
  local uis = {}
  uis.Word = GetBattleData_BallteRaid_ResignWordUis(ui:GetChild("Word"))
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_BallteRaid_ResignWordByName.lua.lua
**Functions:**
- GetBattleData_BallteRaid_ResignWordUis
**Snippet:**
```lua
function GetBattleData_BallteRaid_ResignWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_BallteRaid_SureBtnByName.lua.lua
**Functions:**
- GetBattleData_BallteRaid_SureBtnUis
**Snippet:**
```lua
function GetBattleData_BallteRaid_SureBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_BallteRaid_SureByName.lua.lua
**Functions:**
- GetBattleData_BallteRaid_SureUis
**Requires:**
- BattleData_BallteRaid_SureWordByName
**Snippet:**
```lua
require("BattleData_BallteRaid_SureWordByName")

function GetBattleData_BallteRaid_SureUis(ui)
  local uis = {}
  uis.Word = GetBattleData_BallteRaid_SureWordUis(ui:GetChild("Word"))
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_BallteRaid_SureWordByName.lua.lua
**Functions:**
- GetBattleData_BallteRaid_SureWordUis
**Snippet:**
```lua
function GetBattleData_BallteRaid_SureWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_BattleAxisByName.lua.lua
**Functions:**
- GetBattleData_BattleAxisUis
**Requires:**
- CommonResource_BackGroundByName
- BattleData_AxisOwnTileByName
- BattleData_AxisEnemyTileByName
- BattleData_BattleTimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("BattleData_AxisOwnTileByName")
require("BattleData_AxisEnemyTileByName")
require("BattleData_BattleTimeByName")

function GetBattleData_BattleAxisUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.NameWinTxt = ui:GetChild("NameWinTxt")
  uis.NameFailTxt = ui:GetChild("NameFailTxt")
```

---

## Battle/BattleData_BattleAxisWindowByName.lua.lua
**Functions:**
- GetBattleData_BattleAxisWindowUis
**Requires:**
- BattleData_BattleAxisByName
**Snippet:**
```lua
require("BattleData_BattleAxisByName")

function GetBattleData_BattleAxisWindowUis(ui)
  local uis = {}
  uis.Main = GetBattleData_BattleAxisUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_BattleDataByName.lua.lua
**Functions:**
- GetBattleData_BattleDataUis
**Requires:**
- CommonResource_BackGroundByName
- BattleData_OwnByName
- BattleData_GuildSkillRegionByName
- BattleData_EnemyByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("BattleData_OwnByName")
require("BattleData_GuildSkillRegionByName")
require("BattleData_EnemyByName")

function GetBattleData_BattleDataUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TitleWinTxt = ui:GetChild("TitleWinTxt")
  uis.TitleFailTxt = ui:GetChild("TitleFailTxt")
```

---

## Battle/BattleData_BattleDataWindowByName.lua.lua
**Functions:**
- GetBattleData_BattleDataWindowUis
**Requires:**
- BattleData_BattleDataByName
**Snippet:**
```lua
require("BattleData_BattleDataByName")

function GetBattleData_BattleDataWindowUis(ui)
  local uis = {}
  uis.Main = GetBattleData_BattleDataUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_BattleFinishByName.lua.lua
**Functions:**
- GetBattleData_BattleFinishUis
**Requires:**
- CommonResource_BackGroundByName
- BattleData_CardShowByName
- BattleData_TitleWordByName
- BattleData_CardLevelByName
- BattleData_GuildTrainInfoByName
- BattleData_MonsterHPRegionByName
- BattleData_TalkWordByName
- BattleData_BallteRaid_RegionByName
- BattleData_BallteGuildBoss_TimeByName
- BattleData_SetAutoRegionByName
- BattleData_TargetTipsByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("BattleData_CardShowByName")
require("BattleData_TitleWordByName")
require("BattleData_CardLevelByName")
require("BattleData_GuildTrainInfoByName")
require("BattleData_MonsterHPRegionByName")
require("BattleData_TalkWordByName")
require("BattleData_BallteRaid_RegionByName")
require("BattleData_BallteGuildBoss_TimeByName")
require("BattleData_SetAutoRegionByName")
```

---

## Battle/BattleData_BattleFinishFailByName.lua.lua
**Functions:**
- GetBattleData_BattleFinishFailUis
**Requires:**
- CommonResource_BackGroundByName
- BattleData_FailTitleWordByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("BattleData_FailTitleWordByName")

function GetBattleData_BattleFinishFailUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TitleWord = GetBattleData_FailTitleWordUis(ui:GetChild("TitleWord"))
  uis.WordList = ui:GetChild("WordList")
  uis.FailAgainBtn = ui:GetChild("FailAgainBtn")
  uis.FailOutBtn = ui:GetChild("FailOutBtn")
```

---

## Battle/BattleData_BattleFinishFailWindowByName.lua.lua
**Functions:**
- GetBattleData_BattleFinishFailWindowUis
**Requires:**
- BattleData_BattleFinishFailByName
**Snippet:**
```lua
require("BattleData_BattleFinishFailByName")

function GetBattleData_BattleFinishFailWindowUis(ui)
  local uis = {}
  uis.Main = GetBattleData_BattleFinishFailUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_BattleFinishWindowByName.lua.lua
**Functions:**
- GetBattleData_BattleFinishWindowUis
**Requires:**
- BattleData_BattleFinishByName
**Snippet:**
```lua
require("BattleData_BattleFinishByName")

function GetBattleData_BattleFinishWindowUis(ui)
  local uis = {}
  uis.Main = GetBattleData_BattleFinishUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_BattleSkillTipsByName.lua.lua
**Functions:**
- GetBattleData_BattleSkillTipsUis
**Snippet:**
```lua
function GetBattleData_BattleSkillTipsUis(ui)
  local uis = {}
  
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.UnitList = ui:GetChild("UnitList")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Battle/BattleData_BattleSkillTipsUnitByName.lua.lua
**Functions:**
- GetBattleData_BattleSkillTipsUnitUis
**Snippet:**
```lua
function GetBattleData_BattleSkillTipsUnitUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_BattleTimeByName.lua.lua
**Functions:**
- GetBattleData_BattleTimeUis
**Snippet:**
```lua
function GetBattleData_BattleTimeUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_BuildHeadBtnByName.lua.lua
**Functions:**
- GetBattleData_BuildHeadBtnUis
**Requires:**
- BattleData_BuildTypeByName
**Snippet:**
```lua
require("BattleData_BuildTypeByName")

function GetBattleData_BuildHeadBtnUis(ui)
  local uis = {}
  uis.BuildType = GetBattleData_BuildTypeUis(ui:GetChild("BuildType"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_BuildTypeByName.lua.lua
**Functions:**
- GetBattleData_BuildTypeUis
**Snippet:**
```lua
function GetBattleData_BuildTypeUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_BurstSignByName.lua.lua
**Functions:**
- GetBattleData_BurstSignUis
**Snippet:**
```lua
function GetBattleData_BurstSignUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_CardLevelByName.lua.lua
**Functions:**
- GetBattleData_CardLevelUis
**Snippet:**
```lua
function GetBattleData_CardLevelUis(ui)
  local uis = {}
  
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.ExpProgressBar = ui:GetChild("ExpProgressBar")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_CardShowByName.lua.lua
**Functions:**
- GetBattleData_CardShowUis
**Snippet:**
```lua
function GetBattleData_CardShowUis(ui)
  local uis = {}
  
  uis.CardShowLoader = ui:GetChild("CardShowLoader")
  uis.CardShowHolder = ui:GetChild("CardShowHolder")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_CardTypeByName.lua.lua
**Functions:**
- GetBattleData_CardTypeUis
**Snippet:**
```lua
function GetBattleData_CardTypeUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_CureByName.lua.lua
**Functions:**
- GetBattleData_CureUis
**Snippet:**
```lua
function GetBattleData_CureUis(ui)
  local uis = {}
  
  uis.CureProgressBar = ui:GetChild("CureProgressBar")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_CureProgressBarByName.lua.lua
**Functions:**
- GetBattleData_CureProgressBarUis
**Requires:**
- BattleData_CureProgressFillByName
**Snippet:**
```lua
require("BattleData_CureProgressFillByName")

function GetBattleData_CureProgressBarUis(ui)
  local uis = {}
  uis.bar = GetBattleData_CureProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_CureProgressFillByName.lua.lua
**Functions:**
- GetBattleData_CureProgressFillUis
**Snippet:**
```lua
function GetBattleData_CureProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_DamageByName.lua.lua
**Functions:**
- GetBattleData_DamageUis
**Snippet:**
```lua
function GetBattleData_DamageUis(ui)
  local uis = {}
  
  uis.DamageProgressBar = ui:GetChild("DamageProgressBar")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_DamageProgressBarByName.lua.lua
**Functions:**
- GetBattleData_DamageProgressBarUis
**Requires:**
- BattleData_DamageProgressFillByName
**Snippet:**
```lua
require("BattleData_DamageProgressFillByName")

function GetBattleData_DamageProgressBarUis(ui)
  local uis = {}
  uis.bar = GetBattleData_DamageProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_DamageProgressFillByName.lua.lua
**Functions:**
- GetBattleData_DamageProgressFillUis
**Snippet:**
```lua
function GetBattleData_DamageProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_DataBtnByName.lua.lua
**Functions:**
- GetBattleData_DataBtnUis
**Snippet:**
```lua
function GetBattleData_DataBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_DataLabelBtnBgByName.lua.lua
**Functions:**
- GetBattleData_DataLabelBtnBgUis
**Snippet:**
```lua
function GetBattleData_DataLabelBtnBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_DataLabelBtnByName.lua.lua
**Functions:**
- GetBattleData_DataLabelBtnUis
**Requires:**
- BattleData_DataLabelBtnBgByName
**Snippet:**
```lua
require("BattleData_DataLabelBtnBgByName")

function GetBattleData_DataLabelBtnUis(ui)
  local uis = {}
  uis.DataLabelBtnBg = GetBattleData_DataLabelBtnBgUis(ui:GetChild("DataLabelBtnBg"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## Battle/BattleData_DieTimeByName.lua.lua
**Functions:**
- GetBattleData_DieTimeUis
**Snippet:**
```lua
function GetBattleData_DieTimeUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_EnemyBurstBottomByName.lua.lua
**Functions:**
- GetBattleData_EnemyBurstBottomUis
**Requires:**
- BattleData_BurstSignByName
**Snippet:**
```lua
require("BattleData_BurstSignByName")

function GetBattleData_EnemyBurstBottomUis(ui)
  local uis = {}
  uis.BurstSign = GetBattleData_BurstSignUis(ui:GetChild("BurstSign"))
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_EnemyByName.lua.lua
**Functions:**
- GetBattleData_EnemyUis
**Snippet:**
```lua
function GetBattleData_EnemyUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.DataLabel1Btn = ui:GetChild("DataLabel1Btn")
  uis.DataLabel2Btn = ui:GetChild("DataLabel2Btn")
  uis.DataLabel3Btn = ui:GetChild("DataLabel3Btn")
  uis.DataLabel4Btn = ui:GetChild("DataLabel4Btn")
  uis.EnemyCardList = ui:GetChild("EnemyCardList")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Battle/BattleData_EnemyCardTipsByName.lua.lua
**Functions:**
- GetBattleData_EnemyCardTipsUis
**Requires:**
- CommonResource_OccupationByName
- BattleData_DamageByName
- BattleData_SufferDamageByName
- BattleData_CureByName
- BattleData_SufferCureByName
- BattleData_EnemyMonsterNumberByName
**Snippet:**
```lua
require("CommonResource_OccupationByName")
require("BattleData_DamageByName")
require("BattleData_SufferDamageByName")
require("BattleData_CureByName")
require("BattleData_SufferCureByName")
require("BattleData_EnemyMonsterNumberByName")

function GetBattleData_EnemyCardTipsUis(ui)
  local uis = {}
  uis.HeadBtn = ui:GetChild("HeadBtn")
```

---

## Battle/BattleData_EnemyHeadByName.lua.lua
**Functions:**
- GetBattleData_EnemyHeadUis
**Snippet:**
```lua
function GetBattleData_EnemyHeadUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_EnemyMonsterNumberByName.lua.lua
**Functions:**
- GetBattleData_EnemyMonsterNumberUis
**Snippet:**
```lua
function GetBattleData_EnemyMonsterNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_EnemyPlayerByName.lua.lua
**Functions:**
- GetBattleData_EnemyPlayerUis
**Requires:**
- BattleData_EnemyHeadByName
**Snippet:**
```lua
require("BattleData_EnemyHeadByName")

function GetBattleData_EnemyPlayerUis(ui)
  local uis = {}
  uis.AxisHead = GetBattleData_EnemyHeadUis(ui:GetChild("AxisHead"))
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_ExpProgressBarByName.lua.lua
**Functions:**
- GetBattleData_ExpProgressBarUis
**Requires:**
- BattleData_ExpProgressFillByName
**Snippet:**
```lua
require("BattleData_ExpProgressFillByName")

function GetBattleData_ExpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetBattleData_ExpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_ExpProgressFillByName.lua.lua
**Functions:**
- GetBattleData_ExpProgressFillUis
**Snippet:**
```lua
function GetBattleData_ExpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_FailAgainBtnByName.lua.lua
**Functions:**
- GetBattleData_FailAgainBtnUis
**Snippet:**
```lua
function GetBattleData_FailAgainBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_FailExplainWordByName.lua.lua
**Functions:**
- GetBattleData_FailExplainWordUis
**Snippet:**
```lua
function GetBattleData_FailExplainWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_FailOutBtnByName.lua.lua
**Functions:**
- GetBattleData_FailOutBtnUis
**Snippet:**
```lua
function GetBattleData_FailOutBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_FailTitleWordByName.lua.lua
**Functions:**
- GetBattleData_FailTitleWordUis
**Snippet:**
```lua
function GetBattleData_FailTitleWordUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordFailTxt = ui:GetChild("WordFailTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_GuildSkillRegionByName.lua.lua
**Functions:**
- GetBattleData_GuildSkillRegionUis
**Snippet:**
```lua
function GetBattleData_GuildSkillRegionUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.DataLabel1Btn = ui:GetChild("DataLabel1Btn")
  uis.DataLabel2Btn = ui:GetChild("DataLabel2Btn")
  uis.DataLabel3Btn = ui:GetChild("DataLabel3Btn")
  uis.OwnSkillList = ui:GetChild("OwnSkillList")
  uis.root = ui
  return uis
```

---

## Battle/BattleData_GuildSkill_CureByName.lua.lua
**Functions:**
- GetBattleData_GuildSkill_CureUis
**Snippet:**
```lua
function GetBattleData_GuildSkill_CureUis(ui)
  local uis = {}
  
  uis.CureProgressBar = ui:GetChild("CureProgressBar")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_GuildSkill_CureProgressBarByName.lua.lua
**Functions:**
- GetBattleData_GuildSkill_CureProgressBarUis
**Requires:**
- BattleData_GuildSkill_CureProgressFillByName
**Snippet:**
```lua
require("BattleData_GuildSkill_CureProgressFillByName")

function GetBattleData_GuildSkill_CureProgressBarUis(ui)
  local uis = {}
  uis.bar = GetBattleData_GuildSkill_CureProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_GuildSkill_CureProgressFillByName.lua.lua
**Functions:**
- GetBattleData_GuildSkill_CureProgressFillUis
**Snippet:**
```lua
function GetBattleData_GuildSkill_CureProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_GuildSkill_DamageByName.lua.lua
**Functions:**
- GetBattleData_GuildSkill_DamageUis
**Snippet:**
```lua
function GetBattleData_GuildSkill_DamageUis(ui)
  local uis = {}
  
  uis.DamageProgressBar = ui:GetChild("DamageProgressBar")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_GuildSkill_DamageProgressBarByName.lua.lua
**Functions:**
- GetBattleData_GuildSkill_DamageProgressBarUis
**Requires:**
- BattleData_GuildSkill_DamageProgressFillByName
**Snippet:**
```lua
require("BattleData_GuildSkill_DamageProgressFillByName")

function GetBattleData_GuildSkill_DamageProgressBarUis(ui)
  local uis = {}
  uis.bar = GetBattleData_GuildSkill_DamageProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_GuildSkill_DamageProgressFillByName.lua.lua
**Functions:**
- GetBattleData_GuildSkill_DamageProgressFillUis
**Snippet:**
```lua
function GetBattleData_GuildSkill_DamageProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_GuildSkill_DataLabelBtnBgByName.lua.lua
**Functions:**
- GetBattleData_GuildSkill_DataLabelBtnBgUis
**Snippet:**
```lua
function GetBattleData_GuildSkill_DataLabelBtnBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_GuildSkill_DataLabelBtnByName.lua.lua
**Functions:**
- GetBattleData_GuildSkill_DataLabelBtnUis
**Requires:**
- BattleData_GuildSkill_DataLabelBtnBgByName
**Snippet:**
```lua
require("BattleData_GuildSkill_DataLabelBtnBgByName")

function GetBattleData_GuildSkill_DataLabelBtnUis(ui)
  local uis = {}
  uis.DataLabelBtnBg = GetBattleData_GuildSkill_DataLabelBtnBgUis(ui:GetChild("DataLabelBtnBg"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## Battle/BattleData_GuildSkill_HeadBgByName.lua.lua
**Functions:**
- GetBattleData_GuildSkill_HeadBgUis
**Snippet:**
```lua
function GetBattleData_GuildSkill_HeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_GuildSkill_HeadBtnByName.lua.lua
**Functions:**
- GetBattleData_GuildSkill_HeadBtnUis
**Requires:**
- BattleData_GuildSkill_HeadBgByName
**Snippet:**
```lua
require("BattleData_GuildSkill_HeadBgByName")

function GetBattleData_GuildSkill_HeadBtnUis(ui)
  local uis = {}
  uis.Head = GetBattleData_GuildSkill_HeadBgUis(ui:GetChild("Head"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_GuildSkill_OwnSkillTipsByName.lua.lua
**Functions:**
- GetBattleData_GuildSkill_OwnSkillTipsUis
**Requires:**
- BattleData_GuildSkill_DamageByName
- BattleData_GuildSkill_CureByName
- BattleData_GuildSkill_ShieldByName
**Snippet:**
```lua
require("BattleData_GuildSkill_DamageByName")
require("BattleData_GuildSkill_CureByName")
require("BattleData_GuildSkill_ShieldByName")

function GetBattleData_GuildSkill_OwnSkillTipsUis(ui)
  local uis = {}
  uis.HeadBtn = ui:GetChild("HeadBtn")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.ElementList = ui:GetChild("ElementList")
```

---

## Battle/BattleData_GuildSkill_ShieldByName.lua.lua
**Functions:**
- GetBattleData_GuildSkill_ShieldUis
**Snippet:**
```lua
function GetBattleData_GuildSkill_ShieldUis(ui)
  local uis = {}
  
  uis.ShieldProgressBar = ui:GetChild("ShieldProgressBar")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_GuildSkill_ShieldProgressBarByName.lua.lua
**Functions:**
- GetBattleData_GuildSkill_ShieldProgressBarUis
**Requires:**
- BattleData_GuildSkill_ShieldProgressFillByName
**Snippet:**
```lua
require("BattleData_GuildSkill_ShieldProgressFillByName")

function GetBattleData_GuildSkill_ShieldProgressBarUis(ui)
  local uis = {}
  uis.bar = GetBattleData_GuildSkill_ShieldProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_GuildSkill_ShieldProgressFillByName.lua.lua
**Functions:**
- GetBattleData_GuildSkill_ShieldProgressFillUis
**Snippet:**
```lua
function GetBattleData_GuildSkill_ShieldProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_GuildSkill_SwitchBtnByName.lua.lua
**Functions:**
- GetBattleData_GuildSkill_SwitchBtnUis
**Snippet:**
```lua
function GetBattleData_GuildSkill_SwitchBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_GuildSkill_UseNumberByName.lua.lua
**Functions:**
- GetBattleData_GuildSkill_UseNumberUis
**Snippet:**
```lua
function GetBattleData_GuildSkill_UseNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_GuildTrainInfoByName.lua.lua
**Functions:**
- GetBattleData_GuildTrainInfoUis
**Snippet:**
```lua
function GetBattleData_GuildTrainInfoUis(ui)
  local uis = {}
  
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_HeadBtnByName.lua.lua
**Functions:**
- GetBattleData_HeadBtnUis
**Requires:**
- BattleData_CardTypeByName
- BattleData_MonsterTypeByName
- BattleData_MonsterSignByName
**Snippet:**
```lua
require("BattleData_CardTypeByName")
require("BattleData_MonsterTypeByName")
require("BattleData_MonsterSignByName")

function GetBattleData_HeadBtnUis(ui)
  local uis = {}
  uis.PlayerHead = GetBattleData_CardTypeUis(ui:GetChild("PlayerHead"))
  uis.MonsterLoader = GetBattleData_MonsterTypeUis(ui:GetChild("MonsterLoader"))
  uis.MonsterSign = GetBattleData_MonsterSignUis(ui:GetChild("MonsterSign"))
  uis.buttonCtr = ui:GetController("button")
```

---

## Battle/BattleData_KillNumberByName.lua.lua
**Functions:**
- GetBattleData_KillNumberUis
**Snippet:**
```lua
function GetBattleData_KillNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_MonsterHP1ByName.lua.lua
**Functions:**
- GetBattleData_MonsterHP1Uis
**Requires:**
- BattleData_MonsterHPWord2ByName
**Snippet:**
```lua
require("BattleData_MonsterHPWord2ByName")

function GetBattleData_MonsterHP1Uis(ui)
  local uis = {}
  uis.Word = GetBattleData_MonsterHPWord2Uis(ui:GetChild("Word"))
  uis.MonsterHPProgressBar = ui:GetChild("MonsterHPProgressBar")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_MonsterHP2ByName.lua.lua
**Functions:**
- GetBattleData_MonsterHP2Uis
**Requires:**
- BattleData_MonsterHPWordByName
- BattleData_MonsterHPWord1ByName
**Snippet:**
```lua
require("BattleData_MonsterHPWordByName")
require("BattleData_MonsterHPWord1ByName")

function GetBattleData_MonsterHP2Uis(ui)
  local uis = {}
  uis.Word = GetBattleData_MonsterHPWordUis(ui:GetChild("Word"))
  uis.Word1 = GetBattleData_MonsterHPWord1Uis(ui:GetChild("Word1"))
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_MonsterHPProgressBarByName.lua.lua
**Functions:**
- GetBattleData_MonsterHPProgressBarUis
**Requires:**
- BattleData_MonsterHPProgressFillByName
**Snippet:**
```lua
require("BattleData_MonsterHPProgressFillByName")

function GetBattleData_MonsterHPProgressBarUis(ui)
  local uis = {}
  uis.bar = GetBattleData_MonsterHPProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_MonsterHPProgressFillByName.lua.lua
**Functions:**
- GetBattleData_MonsterHPProgressFillUis
**Snippet:**
```lua
function GetBattleData_MonsterHPProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_MonsterHPRegionByName.lua.lua
**Functions:**
- GetBattleData_MonsterHPRegionUis
**Requires:**
- BattleData_MonsterHP1ByName
- BattleData_MonsterHP2ByName
**Snippet:**
```lua
require("BattleData_MonsterHP1ByName")
require("BattleData_MonsterHP2ByName")

function GetBattleData_MonsterHPRegionUis(ui)
  local uis = {}
  uis.MonsterHP1 = GetBattleData_MonsterHP1Uis(ui:GetChild("MonsterHP1"))
  uis.MonsterHP2 = GetBattleData_MonsterHP2Uis(ui:GetChild("MonsterHP2"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Battle/BattleData_MonsterHPWord1ByName.lua.lua
**Functions:**
- GetBattleData_MonsterHPWord1Uis
**Snippet:**
```lua
function GetBattleData_MonsterHPWord1Uis(ui)
  local uis = {}
  
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.Word3Txt = ui:GetChild("Word3Txt")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_MonsterHPWord2ByName.lua.lua
**Functions:**
- GetBattleData_MonsterHPWord2Uis
**Snippet:**
```lua
function GetBattleData_MonsterHPWord2Uis(ui)
  local uis = {}
  
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.Word3Txt = ui:GetChild("Word3Txt")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_MonsterHPWordByName.lua.lua
**Functions:**
- GetBattleData_MonsterHPWordUis
**Snippet:**
```lua
function GetBattleData_MonsterHPWordUis(ui)
  local uis = {}
  
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.Word3Txt = ui:GetChild("Word3Txt")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_MonsterSignByName.lua.lua
**Functions:**
- GetBattleData_MonsterSignUis
**Snippet:**
```lua
function GetBattleData_MonsterSignUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_MonsterTypeByName.lua.lua
**Functions:**
- GetBattleData_MonsterTypeUis
**Snippet:**
```lua
function GetBattleData_MonsterTypeUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_OverlapHeadByName.lua.lua
**Functions:**
- GetBattleData_OverlapHeadUis
**Requires:**
- BattleData_AxisHeadByName
**Snippet:**
```lua
require("BattleData_AxisHeadByName")

function GetBattleData_OverlapHeadUis(ui)
  local uis = {}
  uis.AxisHead = GetBattleData_AxisHeadUis(ui:GetChild("AxisHead"))
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_OverlapHeadTipsByName.lua.lua
**Functions:**
- GetBattleData_OverlapHeadTipsUis
**Snippet:**
```lua
function GetBattleData_OverlapHeadTipsUis(ui)
  local uis = {}
  
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.HeadList = ui:GetChild("HeadList")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_OwnBurstBottomByName.lua.lua
**Functions:**
- GetBattleData_OwnBurstBottomUis
**Requires:**
- BattleData_BurstSignByName
**Snippet:**
```lua
require("BattleData_BurstSignByName")

function GetBattleData_OwnBurstBottomUis(ui)
  local uis = {}
  uis.BurstSign = GetBattleData_BurstSignUis(ui:GetChild("BurstSign"))
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_OwnByName.lua.lua
**Functions:**
- GetBattleData_OwnUis
**Snippet:**
```lua
function GetBattleData_OwnUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.DataLabel1Btn = ui:GetChild("DataLabel1Btn")
  uis.DataLabel2Btn = ui:GetChild("DataLabel2Btn")
  uis.DataLabel3Btn = ui:GetChild("DataLabel3Btn")
  uis.DataLabel4Btn = ui:GetChild("DataLabel4Btn")
  uis.OwnCardList = ui:GetChild("OwnCardList")
  uis.root = ui
```

---

## Battle/BattleData_OwnCardTipsByName.lua.lua
**Functions:**
- GetBattleData_OwnCardTipsUis
**Requires:**
- CommonResource_OccupationByName
- BattleData_DamageByName
- BattleData_SufferDamageByName
- BattleData_CureByName
- BattleData_SufferCureByName
**Snippet:**
```lua
require("CommonResource_OccupationByName")
require("BattleData_DamageByName")
require("BattleData_SufferDamageByName")
require("BattleData_CureByName")
require("BattleData_SufferCureByName")

function GetBattleData_OwnCardTipsUis(ui)
  local uis = {}
  uis.HeadBtn = ui:GetChild("HeadBtn")
  uis.NameTxt = ui:GetChild("NameTxt")
```

---

## Battle/BattleData_OwnHeadByName.lua.lua
**Functions:**
- GetBattleData_OwnHeadUis
**Snippet:**
```lua
function GetBattleData_OwnHeadUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_OwnPlayerByName.lua.lua
**Functions:**
- GetBattleData_OwnPlayerUis
**Requires:**
- BattleData_OwnHeadByName
**Snippet:**
```lua
require("BattleData_OwnHeadByName")

function GetBattleData_OwnPlayerUis(ui)
  local uis = {}
  uis.AxisHead = GetBattleData_OwnHeadUis(ui:GetChild("AxisHead"))
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_ReturnBtnByName.lua.lua
**Functions:**
- GetBattleData_ReturnBtnUis
**Snippet:**
```lua
function GetBattleData_ReturnBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_RoundBtnByName.lua.lua
**Functions:**
- GetBattleData_RoundBtnUis
**Snippet:**
```lua
function GetBattleData_RoundBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_ScaleByName.lua.lua
**Functions:**
- GetBattleData_ScaleUis
**Snippet:**
```lua
function GetBattleData_ScaleUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_SetAutoCloseBtnByName.lua.lua
**Functions:**
- GetBattleData_SetAutoCloseBtnUis
**Snippet:**
```lua
function GetBattleData_SetAutoCloseBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_SetAutoRegionByName.lua.lua
**Functions:**
- GetBattleData_SetAutoRegionUis
**Requires:**
- BattleData_SetAutoTips1ByName
- BattleData_SetAutoTipsByName
**Snippet:**
```lua
require("BattleData_SetAutoTips1ByName")
require("BattleData_SetAutoTipsByName")

function GetBattleData_SetAutoRegionUis(ui)
  local uis = {}
  uis.Tips1 = GetBattleData_SetAutoTips1Uis(ui:GetChild("Tips1"))
  uis.Tips = GetBattleData_SetAutoTipsUis(ui:GetChild("Tips"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Battle/BattleData_SetAutoSureBtnByName.lua.lua
**Functions:**
- GetBattleData_SetAutoSureBtnUis
**Snippet:**
```lua
function GetBattleData_SetAutoSureBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_SetAutoTips1ByName.lua.lua
**Functions:**
- GetBattleData_SetAutoTips1Uis
**Snippet:**
```lua
function GetBattleData_SetAutoTips1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_SetAutoTipsByName.lua.lua
**Functions:**
- GetBattleData_SetAutoTipsUis
**Snippet:**
```lua
function GetBattleData_SetAutoTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.SureBtn = ui:GetChild("SureBtn")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_SpotByName.lua.lua
**Functions:**
- GetBattleData_SpotUis
**Snippet:**
```lua
function GetBattleData_SpotUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_StateTypeByName.lua.lua
**Functions:**
- GetBattleData_StateTypeUis
**Snippet:**
```lua
function GetBattleData_StateTypeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_SufferCure2ProgressBarByName.lua.lua
**Functions:**
- GetBattleData_SufferCure2ProgressBarUis
**Requires:**
- BattleData_SufferCure2ProgressFillByName
**Snippet:**
```lua
require("BattleData_SufferCure2ProgressFillByName")

function GetBattleData_SufferCure2ProgressBarUis(ui)
  local uis = {}
  uis.bar = GetBattleData_SufferCure2ProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_SufferCure2ProgressFillByName.lua.lua
**Functions:**
- GetBattleData_SufferCure2ProgressFillUis
**Snippet:**
```lua
function GetBattleData_SufferCure2ProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_SufferCureByName.lua.lua
**Functions:**
- GetBattleData_SufferCureUis
**Snippet:**
```lua
function GetBattleData_SufferCureUis(ui)
  local uis = {}
  
  uis.SufferCure2ProgressBar = ui:GetChild("SufferCure2ProgressBar")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_SufferDamage2ProgressBarByName.lua.lua
**Functions:**
- GetBattleData_SufferDamage2ProgressBarUis
**Requires:**
- BattleData_SufferDamage2ProgressFillByName
**Snippet:**
```lua
require("BattleData_SufferDamage2ProgressFillByName")

function GetBattleData_SufferDamage2ProgressBarUis(ui)
  local uis = {}
  uis.bar = GetBattleData_SufferDamage2ProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_SufferDamage2ProgressFillByName.lua.lua
**Functions:**
- GetBattleData_SufferDamage2ProgressFillUis
**Snippet:**
```lua
function GetBattleData_SufferDamage2ProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_SufferDamageByName.lua.lua
**Functions:**
- GetBattleData_SufferDamageUis
**Snippet:**
```lua
function GetBattleData_SufferDamageUis(ui)
  local uis = {}
  
  uis.SufferDamage2ProgressBar = ui:GetChild("SufferDamage2ProgressBar")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_Switch1BtnByName.lua.lua
**Functions:**
- GetBattleData_Switch1BtnUis
**Snippet:**
```lua
function GetBattleData_Switch1BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_SwitchBtnByName.lua.lua
**Functions:**
- GetBattleData_SwitchBtnUis
**Snippet:**
```lua
function GetBattleData_SwitchBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_TalkWordByName.lua.lua
**Functions:**
- GetBattleData_TalkWordUis
**Snippet:**
```lua
function GetBattleData_TalkWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_TargetTips1ByName.lua.lua
**Functions:**
- GetBattleData_TargetTips1Uis
**Snippet:**
```lua
function GetBattleData_TargetTips1Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_TargetTips2ByName.lua.lua
**Functions:**
- GetBattleData_TargetTips2Uis
**Snippet:**
```lua
function GetBattleData_TargetTips2Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_TargetTipsByName.lua.lua
**Functions:**
- GetBattleData_TargetTipsUis
**Requires:**
- BattleData_TargetTips1ByName
**Snippet:**
```lua
require("BattleData_TargetTips1ByName")

function GetBattleData_TargetTipsUis(ui)
  local uis = {}
  uis.Title = GetBattleData_TargetTips1Uis(ui:GetChild("Title"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_TimeBtnByName.lua.lua
**Functions:**
- GetBattleData_TimeBtnUis
**Snippet:**
```lua
function GetBattleData_TimeBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleData_TitleWordByName.lua.lua
**Functions:**
- GetBattleData_TitleWordUis
**Snippet:**
```lua
function GetBattleData_TitleWordUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordWinTxt = ui:GetChild("WordWinTxt")
  uis.WordFailTxt = ui:GetChild("WordFailTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Battle/BattleFinishFailWindow.lua.lua
**Functions:**
- BattleFinishFailWindow.ReInitData
- BattleFinishFailWindow.OnInit
- BattleFinishFailWindow.UpdateInfo
- BattleFinishFailWindow.UpdateResult
- BattleFinishFailWindow.UpdateCardVoice
- BattleFinishFailWindow.InitBtn
- BattleFinishFailWindow.TryAgain
- BattleFinishFailWindow.CloseWindow
- BattleFinishFailWindow.OpenDataWindow
- BattleFinishFailWindow.OpenAxisWindow
- BattleFinishFailWindow.UpdateAutoBtnText
- BattleFinishFailWindow.OnShown
- BattleFinishFailWindow.OnHide
- BattleFinishFailWindow.StopTalk
- BattleFinishFailWindow.OnClose
- BattleFinishFailWindow.HandleMessage
**Requires:**
- BattleData_BattleFinishFailWindowByName
**Snippet:**
```lua
require("BattleData_BattleFinishFailWindowByName")
local BattleFinishFailWindow = {}
local uis, contentPane

function BattleFinishFailWindow.ReInitData()
end

local challengeResult, curTypingEffect, curSoundEventIns
local expChangeTime = 1
local remove
```

---

## Battle/BattleFinishWindow.lua.lua
**Functions:**
- BattleFinishWindow.ReInitData
- BattleFinishWindow.OnInit
- BattleFinishWindow.UpdateInfo
- BattleFinishWindow.UpdateTarget
- tipsList.itemRenderer
- BattleFinishWindow.UpdateExp
- BattleFinishWindow.UpdateShowLevelUp
- BattleFinishWindow.IsWin
- BattleFinishWindow.IsOver
- BattleFinishWindow.ShowDamage
- BattleFinishWindow.ShowDamageInGuildWar
- BattleFinishWindow.ShowDamageInRaidBoss
- BattleFinishWindow.UpdateResult
- BattleFinishWindow.UpdateSceneType
- BattleFinishWindow.UpdateItem
- BattleFinishWindow.Sort
- BattleFinishWindow.UpdateCardShow
- BattleFinishWindow.InitBtn
- BattleFinishWindow.CloseWindow
- BattleFinishWindow.OpenDataWindow
- BattleFinishWindow.OpenAxisWindow
- BattleFinishWindow.InitText
- BattleFinishWindow.CancelSave
- BattleFinishWindow.UpdateAutoBtnText
- BattleFinishWindow.DelayedCall
- BattleFinishWindow.OnShown
- BattleFinishWindow.OnHide
- BattleFinishWindow.StopTalk
- BattleFinishWindow.OnClose
- BattleFinishWindow.HandleMessage
**Requires:**
- BattleData_BattleFinishWindowByName
**Snippet:**
```lua
require("BattleData_BattleFinishWindowByName")
local BattleFinishWindow = {}
local uis, contentPane

function BattleFinishWindow.ReInitData()
end

local showLevelUp = false
local challengeResult, curTypingEffect, curSoundEventIns
local expChangeTime = 1
```

---

## Battle/BattleGrid.lua.lua
**Functions:**
- BattleGrid.InitLocalVar
- BattleGrid.NewGrid
- grid:Init
- grid:CreateModel
- grid:Destroy
**Snippet:**
```lua
BattleGrid = {}

function BattleGrid.InitLocalVar()
end

function BattleGrid.NewGrid(indexX, indexY)
  local grid = {}
  
  function grid:Init()
    self.indexX = indexX
```

---

## Battle/BattleHurtNum.lua.lua
**Functions:**
- BattleHurtNum.Init
- BattleHurtNum.UpdateNormalHurtVisible
- BattleHurtNum.ClearPool
- BattleHurtNum.ShowHurtNum
- BattleHurtNum.ShowBuffWord
- BattleHurtNum.ShowPopWord
- BattleHurtNum.ShowExpression
- BattleHurtNum.ShowBattleSkillTipsAni
- BattleHurtNum.SetGrayAll
- BattleHurtNum.HideAll
- BattleHurtNum.ShowAll
- BattleHurtNum.ClearHurtNum
**Snippet:**
```lua
BattleHurtNum = {}
local BattleBuffWordType = {
  MISS = "Battle:buff_miss",
  INVINCIBLE = "Battle:buff_wudi",
  IMMUNE = "Battle:buff_mianyi"
}
local hudCom, buffCom, battlePopObjectPool
local floor = math.floor
local BattleHurtNumType = {
  NOR_HURT = "NormalHitNumberTips",
```

---

## Battle/BattleInfoWindow.lua.lua
**Functions:**
- BattleInfoWindow.ReInitData
- BattleInfoWindow.OnInit
- BattleInfoWindow.UpdateInfo
- BattleInfoWindow.UpdateSetTips
- burstShowList.itemRenderer
- BattleInfoWindow.UpdateRatioListBtn
- BattleInfoWindow.UpdateSwitchBtn
- BattleInfoWindow.TouchSwitchBtn
- BattleInfoWindow.InitBtn
- BattleInfoWindow.Quit
- BattleInfoWindow.OnClose
**Requires:**
- ActorInfo_BattleInfoWindowByName
- ActorInfo_SetTipsByName
**Snippet:**
```lua
require("ActorInfo_BattleInfoWindowByName")
local BattleInfoWindow = {}
local uis, contentPane, curSettingList
local cachedHandByKey = {}
local quitCallback

function BattleInfoWindow.ReInitData()
end

function BattleInfoWindow.OnInit(bridgeObj)
```

---

## Battle/BattleLoadingWindow.lua.lua
**Functions:**
- BattleLoadingWindow.ReInitData
- BattleLoadingWindow.OnInit
- BattleLoadingWindow.UpdateInfo
- BattleLoadingWindow.ShowAnimOut
- BattleLoadingWindow.InitBtn
- BattleLoadingWindow.OnShown
- BattleLoadingWindow.OnHide
- BattleLoadingWindow.OnClose
- BattleLoadingWindow.HandleMessage
**Requires:**
- Loading_BattleLoadingWindowByName
**Snippet:**
```lua
require("Loading_BattleLoadingWindowByName")
local BattleLoadingWindow = {}
local uis, contentPane, effect, onShowAnimationEndCallback, addCallbackIn

function BattleLoadingWindow.ReInitData()
end

function BattleLoadingWindow.OnInit(bridgeObj)
  bridgeObj:SetView(WinResConfig.BattleLoadingWindow.package, WinResConfig.BattleLoadingWindow.comName, function(com)
    contentPane = com
```

---

## Battle/BattleManuallySkill.lua.lua
**Functions:**
- BattleManuallySkill.InitLocalVar
- BattleManuallySkill.NewSkill
- skill:GetSkillConfig
- skill:GetSkillLevelUpConfig
- skill:GetSkillShowConfig
- skill:GetSkillShowDisplayConfig
- skill:GetSkillTotalFrame
- skill:Init
- skill:GetSkillAtk
- skill:CanAutoChosen
- skill:SetAutoPosition
- skill:GetPositionBetweenTwoUnit
- skill:Update
- skill:TriggerSkillBuff
- skill:DealSummon
- skill:GetHurt
- skill:SetWaitCDFrame
- skill:SetPosition
- skill:SetActive
- skill:GetAvailableTargets
- skill:GetInRangeUnit
- skill:IsTargetInRange
- skill:GetRange
- skill:IsEffective
- skill:ResetAllUnitInRangeState
- skill:UpdateDisplay
- skill:SaveDamage
- skill:SaveShield
- skill:ClearData
- skill:Destroy
- BattleManuallySkill.GetMinHpRangeUnit
**Snippet:**
```lua
BattleManuallySkill = {}
local BATTLE_UNIT_TYPE = BATTLE_UNIT_TYPE

function BattleManuallySkill.InitLocalVar()
end

function BattleManuallySkill.NewSkill(skillId, skillLevel, camp)
  local skill = {
    uid = nil,
    skillId = nil,
```

---

## Battle/BattleMessageBar.lua.lua
**Functions:**
- BattleMessageBar.BindInfo
- headInfo:Init
- headInfo:UpdateHp
- headInfo:UpdateRage
- headInfo:UpdateBuffList
- headInfo:CreateOneBuff
- headInfo:Hide
- headInfo:UpdateVisible
- headInfo:UpdateBuffVisible
- headInfo:UpdateSortingOrder
- headInfo:SetAlpha
- headInfo:Destroy
**Requires:**
- CommonResource_PlayerHPByName
- CommonResource_PlayerBuffByName
**Snippet:**
```lua
BattleMessageBar = {}
local min = math.min
local ceil = math.ceil

function BattleMessageBar.BindInfo(unit)
  require("CommonResource_PlayerHPByName")
  require("CommonResource_PlayerBuffByName")
  local headInfo = {
    buffListInfo = {},
    headObject = nil,
```

---

## Battle/BattleMgr.lua.lua
**Functions:**
- print_battle
- print_server
- BattleMgr.InitLocalVar
- BattleMgr.SaveCompleteData
- BattleMgr.InitBattle
- BattleMgr.StartBattle
- BattleMgr.CloseBattle
- BattleMgr.SendBattleOverMsg
- BattleMgr.OpenFinishWindow
- BattleMgr.GetWaveName
**Requires:**
- ShakeAnimPlay
**Snippet:**
```lua
BattleMgr = {
  showLeftDamageCount = false,
  showLeftHpCountTest = false,
  showCardUidTest = false,
  showPathTest = false,
  isTestBalance = false,
  isBattleServer = IsBattleServer or false,
  isPlotBattle = false,
  battleVersion = nil,
  localVarInited = false,
```

---

## Battle/BattleNumberWindow.lua.lua
**Functions:**
- BattleNumberWindow.OnInit
- BattleNumberWindow.Init
- BattleNumberWindow.InitTips
- BattleNumberWindow.InitBtn
- BattleNumberWindow.HandleMessage
- BattleNumberWindow.OnClose
**Requires:**
- Arena_BattleNumberWindowByName
**Snippet:**
```lua
require("Arena_BattleNumberWindowByName")
local BattleNumberWindow = {}
local uis, contentPane, arg

function BattleNumberWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BattleNumberWindow.package, WinResConfig.BattleNumberWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetArena_BattleNumberWindowUis(contentPane)
    arg = bridgeObj.argTable[1]
```

---

## Battle/BattleOperation.lua.lua
**Functions:**
- BattleOperation.InitLocalVar
- BattleOperation.Init
- BattleOperation.SavePausedBurst
- BattleOperation.GetPausedBurst
- BattleOperation.AddBurstOperation
- BattleOperation.AddManuallyOperation
- BattleOperation.DealOperationList
- BattleOperation.ChooseBurstSkill
- BattleOperation.DealManuallyOperationList
- BattleOperation.ChooseManuallySkill
- BattleOperation.GetAutoSkillConditionSort
- BattleOperation.Clear
**Snippet:**
```lua
BattleOperation = {}
local ATTR_ENUM = ATTR_ENUM
local burstOperationList = {}
local manuallyOperationList = {}
local pausedBurst, compareIntValue
local skillTypeToSort1 = {}
local skillTypeToSort2 = {}

function BattleOperation.InitLocalVar()
end
```

---

## Battle/BattlePathFinding.lua.lua
**Functions:**
- BattlePathFinding.Init
- BattlePathFinding.AddCloseIndex
- BattlePathFinding.RemoveCloseIndex
- BattlePathFinding.Clear
- BattlePathFinding.FindPath
- BattlePathFinding.ClearCachedPath
- BattlePathFinding.CreateTestGrid
- BattlePathFinding.ClearTestGrid
- BattlePathFinding.ChangeRed
- BattlePathFinding.ChangeEmpty
- BattlePathFinding.UpdateTestPath
**Snippet:**
```lua
BattlePathFinding = {}
local gridSplitNum = 2
local world = {}
local open = {}
local openMap = {}
local closed = {}
local path = {}
local maxX, maxY
local closedIndex = 0
local targetX = 0
```

---

## Battle/BattlePlayerNumberWindow.lua.lua
**Functions:**
- BattlePlayerNumberWindow.ReInitData
- BattlePlayerNumberWindow.OnInit
- BattlePlayerNumberWindow.UpdateInfo
- BattlePlayerNumberWindow.InitBtn
- BattlePlayerNumberWindow.Quit
- BattlePlayerNumberWindow.OnClose
**Requires:**
- Formation_BattlePlayerNumberWindowByName
**Snippet:**
```lua
require("Formation_BattlePlayerNumberWindowByName")
local BattlePlayerNumberWindow = {}
local uis, contentPane, preCount, nowCount

function BattlePlayerNumberWindow.ReInitData()
end

function BattlePlayerNumberWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.BattlePlayerNumberWindow.package, WinResConfig.BattlePlayerNumberWindow.comName, function(com)
    contentPane = com
```

---

## Battle/BattleRecord.lua.lua
**Functions:**
- BattleRecord.SetEnableRecord
- BattleRecord.Init
- BattleRecord.SaveBasic
- BattleRecord.SaveUnitInit
- BattleRecord.SaveUnitUpdate
- BattleRecord.SaveHurtDisplayList
- BattleRecord.SaveRageDisplayList
- BattleRecord.SaveBuffWordsDisplayList
- BattleRecord.SaveBuffEffectDisplayList
- BattleRecord.SaveBulletInit
- BattleRecord.SaveBulletUpdate
- BattleRecord.SaveRecordFile
**Snippet:**
```lua
BattleRecord = {}
local record = {}
local enableRecord = false

function BattleRecord.SetEnableRecord(enable)
  enableRecord = enable
end

function BattleRecord.Init()
  if true ~= enableRecord then
```

---

## Battle/BattleScene.lua.lua
**Functions:**
- BattleScene.InitLocalVar
- BattleScene.Init
- BattleScene.GetMapId
- BattleScene.GetArenaMapId
- BattleScene.InitBase
- BattleScene.InitMap
- BattleScene.InitAreaData
- BattleScene.GetSpace
- BattleScene.GetMapArray
- BattleScene.GetNoCoverGrid
- BattleScene.GetMapXCount
- BattleScene.GetMapYCount
- BattleScene.GetLeftCampXCount
- BattleScene.GetRightCampXCount
- BattleScene.GetInitPosition
- BattleScene.InitBg
- BattleScene.InitUI
- BattleScene.InitBullet
- BattleScene.InitBomb
- BattleScene.InitUnit
- BattleScene.GetMirrorPos
- BattleScene.GetAllGrid
- BattleScene.GetAllUnit
- BattleScene.GetAllAliveUnit
- BattleScene.GetGridListByCamp
- BattleScene.GetAliveJobCountByCamp
- BattleScene.GetAliveCardByCamp
- BattleScene.GetAliveUnitByCamp
- BattleScene.GetUnitListForBuffTips
- BattleScene.GetUnitListByCampForManuallySkill
- BattleScene.GetUnitListByCampForManuallySkill2
- BattleScene.GetUnitListByCamp
- BattleScene.GetBossHaveKOSkill
- BattleScene.GetAliveCardUnitListByCamp
- BattleScene.GetAllAliveCardUnitList
- BattleScene.GetUnitListByCampDirect
- BattleScene.GetUnitByUid
- BattleScene.GetAliveUnitById
- BattleScene.GetUnitById
- BattleScene.GetUnitListByUidList
- BattleScene.GetUidListByUnitList
- BattleScene.AddSkillInfo
- BattleScene.UpdateSkillInfo
- BattleScene.UpdateSkillStartFrameInfo
- BattleScene.GetSkillInfos
- BattleScene.AddManuallySkillInfo
- BattleScene.GetManuallySkillInfos
- BattleScene.AddUnit
- BattleScene.AddUnitToCampList
- BattleScene.RemoveUnit
- BattleScene.AddPartnerTrigger
- BattleScene.RemovePartnerTrigger
- BattleScene.AddEnemyTrigger
- BattleScene.RemoveEnemyTrigger
- BattleScene.GetUnitListByPartnerTrigger
- BattleScene.GetUnitListByEnemyTrigger
- BattleScene.GetUnitGlobalIndex
- BattleScene.LeftUnitDead
- BattleScene.RightUnitDead
- BattleScene.IsBattleWin
- BattleScene.IsBattleLoss
- BattleScene.AddBomb
- BattleScene.RemoveBomb
- BattleScene.GetBombGlobalIndex
- BattleScene.GetBombByUid
- BattleScene.GetSortBombList
- BattleScene.AddBullet
- BattleScene.RemoveBullet
- BattleScene.GetBulletGlobalIndex
- BattleScene.GetBulletByUid
- BattleScene.GetSortBulletList
- BattleScene.InitBurst
- BattleScene.AddBurst
- BattleScene.GetBurst
- BattleScene.GetCampObject
- BattleScene.InitManuallySkill
- BattleScene.AddManuallySkill
- BattleScene.GetManuallySkill
- BattleScene.GetManuallySkillByCamp
- BattleScene.GetAllManuallySkill
- BattleScene.GetManuallySkillGlobalIndex
- BattleScene.DealPreBattle
- BattleScene.GetTempAliveUnitList
- BattleScene.GetTempMoveStateAliveUnitList
- BattleScene.GetTempSpecialStageAliveUnitList
- BattleScene.UpdateProcess
- BattleScene.DealCardBurstStart
- BattleScene.UpdateDisplay
- BattleScene.Stop
- BattleScene.UpdateBattleOverState
- BattleScene.NeedShowKillEnemyCount
- BattleScene.IsBattleOver
- BattleScene.PlayDragSkill
- BattleScene.PlayBoomShow
- BattleScene.PlayBurstSkill
- BattleScene.SetCardBurstTimerUtilPause
- BattleScene.GetUnitListByTargetUid
- BattleScene.GetUnitBlockCountByTargetUid
- BattleScene.UpdateCacheDistance
- BattleScene.GetInRangeUnit
- BattleScene.GetInRangeUnitWithCamp
- BattleScene.IsTargetCounter
- BattleScene.IsTargetInRange
- BattleScene.GetOverlapTeammate
- BattleScene.GetPortalTargetPosition
- BattleScene.DealClearTarget
- BattleScene.IsMoveIntoTRAP
- BattleScene.IsBurstTime
- BattleScene.GetSpeed
- BattleScene.UpdateHeadInfo
- BattleScene.Clear
**Requires:**
- SortingHelper
- SortingHelper
- SortingHelper
**Snippet:**
```lua
BattleScene = {}
local _skillInfos = {}
local _manuallySkillInfos = {}
local _allUnit = {}
local _allAliveUnit = {}
local _allAliveUnitHaveRage = {}
local _allBulletUid = {}
local _allBombUid = {}
local _allBulletUidCopy = {}
local sortBulletListChanged
```

---

## Battle/BattleScriptList.lua.lua
**Requires:**
- BattleMgr
- BattleConst
- BattleControl
- BattleHurtNum
- BattleRecord
- BattleOperation
- BattleScene
- BattleBackground
- BattleBuffMgr
- BattleBuffEffect
- BattleMessageBar
- BattleData
- BattleBurst
- BattleBurstSkill
- BattleDataCount
- BattleChoose
- BattleAction
- BattleActionDisplay
- BattleBullet
- BattleUnit
- BattleBuff
- BattleCamp
- BattleSummonWait
- BattleSkillWait
- BattleVoice
- BattlePathFinding
- BattleTransform
- BattleBomb
- BattleManuallySkill
- BattleService
**Snippet:**
```lua
local require = require
require("BattleMgr")
require("BattleConst")
require("BattleControl")
require("BattleHurtNum")
require("BattleRecord")
require("BattleOperation")
require("BattleScene")
require("BattleBackground")
require("BattleBuffMgr")
```

---

## Battle/BattleService.lua.lua
**Functions:**
- BattleService.Init
- BattleService.SaveStagePrepareInfoReq
- BattleService.DealSaveStagePrepareInfoRsp
- BattleService.PrepareBattleReq
- BattleService.DealPrepareBattleRsp
- BattleService.ChallengeStageReq
- BattleService.DealChallengeStageRsp
- BattleService.GetBattleRecordReq
- BattleService.GetBattleRecordRsp
**Snippet:**
```lua
BattleService = {}

function BattleService.Init()
  Net.AddListener(Proto.MsgName.PrepareBattleRsp, BattleService.DealPrepareBattleRsp)
  Net.AddListener(Proto.MsgName.SaveStagePrepareInfoRsp, BattleService.DealSaveStagePrepareInfoRsp)
  Net.AddListener(Proto.MsgName.ChallengeStageRsp, BattleService.DealChallengeStageRsp)
  Net.AddListener(Proto.MsgName.GetBattleRecordRsp, BattleService.GetBattleRecordRsp)
end

function BattleService.SaveStagePrepareInfoReq(sceneType, cardUid2Pos, buildUid2Pos, leaderCardId, burstOrderSetting, callback)
```

---

## Battle/BattleSkillWait.lua.lua
**Functions:**
- BattleSkillWait.InitLocalVar
- BattleSkillWait.Init
- BattleSkillWait.AddSkill
- BattleSkillWait.IsSkillWait
- BattleSkillWait.DealSkillWaitList
- BattleSkillWait.RemoveSkillWait
- BattleSkillWait.Clear
**Snippet:**
```lua
BattleSkillWait = {}

function BattleSkillWait.InitLocalVar()
end

local skillWaitList = {}

function BattleSkillWait.Init()
  skillWaitList = {}
end
```

---

## Battle/BattleSummonWait.lua.lua
**Functions:**
- BattleSummonWait.Init
- BattleSummonWait.AddSummon
- BattleSummonWait.DealSummonWaitList
- BattleSummonWait.Clear
**Snippet:**
```lua
BattleSummonWait = {}
local summonWaitList = {}

function BattleSummonWait.Init()
  summonWaitList = {}
end

function BattleSummonWait.AddSummon(param, delayFrame)
  if delayFrame > 0 then
    table.insert(summonWaitList, 1, {summonData = param, delayFrame = delayFrame})
```

---

## Battle/BattleTransform.lua.lua
**Functions:**
- BattleTransform.InitLocalVar
- BattleTransform.Init
- BattleTransform.AddTransform
- BattleTransform.DealTransformWaitList
- BattleTransform.RemoveTransformWait
- BattleTransform.CanTransform
- BattleTransform.Clear
**Snippet:**
```lua
BattleTransform = {}

function BattleTransform.InitLocalVar()
end

local transformWaitList = {}

function BattleTransform.Init()
  transformWaitList = {}
end
```

---

## Battle/BattleUIWindow.lua.lua
**Functions:**
- BattleUIWindow.ReInitData
- BattleUIWindow.OnInit
- BattleUIWindow.UpdateHangUpState
- BattleUIWindow.UpdateSpeed
- BattleUIWindow.UpdateInfo
- BattleUIWindow.InitScoreInfo
- scoreTag.StartList.itemRenderer
- BattleUIWindow.UpdateScoreInfo
- BattleUIWindow.UpdateAutoTips
- BattleUIWindow.UpdateDamageCount
- BattleUIWindow.InitBtn
- BattleUIWindow.UpdateBtn
- BattleUIWindow.UpdateRemainTime
- BattleUIWindow.UpdateWave
- BattleUIWindow.ShowEnterAnim
- BattleUIWindow.ChangeWaveUI
- BattleUIWindow.ShowPlayBattleStart
- BattleUIWindow.StopUpdateShow
- BattleUIWindow.ShowPlayBattleOver
- BattleUIWindow.ShowPlayWaveStart
- BattleUIWindow.OnClickSkipBtn
- BattleUIWindow.OnClickSettingBtn
- BattleUIWindow.OnClickSetBtn
- BattleUIWindow.OnClickSpeedBtn
- BattleUIWindow.UpdateSpeedBtn
- BattleUIWindow.OnClickAutoBtn
- BattleUIWindow.UpdateAutoBtn
- BattleUIWindow.OnClickStopBtn
- BattleUIWindow.UpdateStopBtn
- BattleUIWindow.UpdateSettingUI
- BattleUIWindow.OnHide
- BattleUIWindow.BattleStart
- BattleUIWindow.BattleEnd
- BattleUIWindow.InitCardList
- BattleUIWindow.AddHeadToList
- BattleUIWindow.UpdateCard
- dotList.itemRenderer
- BattleUIWindow.AddCardChosenEffect
- BattleUIWindow.RemoveCardChosenEffect
- BattleUIWindow.AddCardPlayBurstSkillEffect
- BattleUIWindow.RemoveCardPlayBurstSkillEffect
- BattleUIWindow.AddCardBurstCdEffect
- BattleUIWindow.RemoveCardBurstCdEffect
- BattleUIWindow.ClickHead
- BattleUIWindow.UpdateCardSelectState
- BattleUIWindow.UpdateSkillArea
- BattleUIWindow.OnClickManuallySkillAutoBtn
- BattleUIWindow.UpdateManuallySkillAutoBtn
- BattleUIWindow.CreateOrUpdateOneSkill
- BattleUIWindow.OnDragStart
- BattleUIWindow.OnDragMove
- BattleUIWindow.OnDragEnd
- BattleUIWindow.UpdateDragPosition
- BattleUIWindow.UpdateSkillList
- BattleUIWindow.ClearSkillDrag
- BattleUIWindow.PlayBurstSkillGuide
- BattleUIWindow.PlayBurstSkillChooseCardGuide
- BattleUIWindow.PlayBurstSkillChooseCardGuide2
- BattleUIWindow.PlayBurstSkillChooseCardGuide3
- BattleUIWindow.PlayBurstCardSkillOverGuide
- BattleUIWindow.InitBurstEffect
- BattleUIWindow.UpdateBurstInfo
- BattleUIWindow.HideBurstEffect
- BattleUIWindow.ShowBurstEffect
- BattleUIWindow.UpdateUIVisibleInBurst
- BattleUIWindow.ShowBurstChooseCard
- BattleUIWindow.UpdateBurstChooseList
- BattleUIWindow.UpdateBurstChooseCardList
- BattleUIWindow.StartChooseCardTimer
- BattleUIWindow.UpdateCardDeadInBurst
- BattleUIWindow.ChooseBurstCardCallback
- BattleUIWindow.AutoChooseCardBurst
- BattleUIWindow.ChooseBurstCardComplete
- BattleUIWindow.UpdateBurstEffectRed
- BattleUIWindow.BossEnter
- BattleUIWindow.BossDie
- BattleUIWindow.BossHpChange
- BattleUIWindow.BossRageChange
- BattleUIWindow.BossBuffChange
- BattleUIWindow.CreateOneBuff
- BattleUIWindow.ShowKillEnemyCount
- BattleUIWindow.PreLoadBattleResource
- BattleUIWindow.OnShowAnimationEnd
- BattleUIWindow.OnPreClose
- BattleUIWindow.OnClose
- BattleUIWindow.HandleMessage
**Requires:**
- Battle_BattleUIWindowByName
- Battle_CardHeadByName
- Battle_TacticalSkillBtnByName
**Snippet:**
```lua
require("Battle_BattleUIWindowByName")
local BattleUIWindow = {}
local uis, contentPane, battleUIWindowObjectPool, skillIcon, skillDrag, skillDragIcon, curSkill, curLineEffectRed, curLineEffectBlue, curTargetLineRed, curTargetLineBlue, curTargetLine, lineStartX, lineStartY
local LineRendererHelper = CS.LineRendererHelper
local targetSpValue
local skillList = {}
local leftHpCountTestText, rightHpCountTestText
local cardList = {}
local cardChooseTweener, maskTexture, cardBuffTipsUnit, curTouchCardUid
local cachedCardBuffList = {}
```

---

## Battle/BattleUnit.lua.lua
**Functions:**
- BattleUnit.InitLocalVar
- BattleUnit.NewUnit
- unit:Init
- unit:InitBaseData
- unit:InitData
- dealCardSkill
- unit:GetChargeMax
- unit:IsSummonAlive
- unit:AddSummonUid
- unit:RemoveSummonUid
- unit:UpdateSkin
- unit:SetMotion
- unit:SaveCharge
- unit:ClearCharge
- unit:SaveSkillTrigger
- unit:RemoveSkillTrigger
- unit:CreateModel
- unit:SetAnimation
- unit:AddAnimationEvent
- unit:RemoveAnimationEvent
- unit:ChangeModel
- changeFunc
- unit:ShowModelDead
- unit:UpdateFlip
- unit:UpdateBuffEffectFlip
- unit:SetModelFlip
- unit:CreateFearTargetPosition
- unit:SavePosition
- unit:ResetToOriPosition
- unit:SetPosition
- unit:UpdatePathIndex
- unit:UpdateSortingOrder
- unit:ChangeAnimation
- callBack
- unit:DestroyModel
- unit:DestroyModelWhenTransform
- unit:DestroyModelDead
- unit:Destroy
- unit:ClearBuff
- unit:ContainBuffId
- unit:GetCachedDistance
- unit:SetState
- unit:SetStateToRevive
- unit:SetStateToDead
- unit:SetStateToDestroy
- unit:AddStateAction
- unit:TriggerTransBuff
- unit:Update
- unit:DealTriggerPartnerSkillAll
- unit:DealTriggerEnemySkillAll
- unit:DealTriggerPassiveSkill
- unit:DealTriggerSkillAll
- unit:UpdateState
- unit:DealStateAction
- unit:UpdateRagePerSecond
- unit:ChangeRemainTime
- unit:UpdateDisplay
- unit:UpdateCrosshair
- unit:UpdateEffectLine
- unit:UpdateShowInSkillRange
- unit:SetModelTimeScale
- unit:UpdateModelTimeScale
- unit:UpdateStateDisplay
- unit:ShowEffectInBurst
- unit:HideEffectInBurst
- unit:CreateEffect
- unit:CreateSkillEffect
- unit:GetHitPointName
- unit:GetPointPositionOffBySlotName
- unit:GetPointPositionBySlotName
- unit:UpdateEffectFlip
- unit:RemoveEffect
- unit:RemoveAllEffect
- unit:RemoveAllBuffEffect
- unit:RemoveAllSkillEffect
- unit:DealStateActionDisplay
- unit:ChooseMoveTarget
- unit:HaveEnemyAliveInAttackRange
- unit:ContainControlType
- unit:ContainBuffEffectTag
- unit:ContainPersistentDamage
- unit:ContainControl
- unit:CanMove
- unit:CanChoose
- unit:Transform
- unit:IsTargetInAttackRange
- unit:IsTargetInAttackRangeByUid
- unit:IsTargetInFindRange
- unit:IsTargetInFindRangeByUid
- unit:GetBaseConfig
- unit:GetBaseCardOrMonsterConfig
- unit:GetFashionBubbleConfig
- unit:GetFashionConfig
- unit:GetGradeUpConfig
- unit:InitSkillList
- unit:GetStartWaitFrame
- unit:GetDefaultWaitFrame
- unit:GetCurNeedWaitFrame
- unit:GetNormalSkillId
- unit:GetNormalSkillShowConfig
- unit:GetSmallSkillLevelUpIds
- unit:GetUniqueSkillLevelUpIds
- unit:GetBurstSkillLevelUpId
- unit:GetExSkillLevelUpIds
- unit:GetPassiveSkillLevelUpIds
- unit:GetCurSkillShowDisplayConfig
- unit:GetSkillLevelUpConfig
- unit:GetSubSkillConfig
- unit:GetSkillShowConfig
- unit:GetCurSkillTotalFrame
- unit:InitCoverRadius
- unit:GetBlockMax
- unit:GetBlockCount
- unit:IsCannotChooseType
- unit:CanRangeChosen
- unit:CanBuffChosen
- unit:CanTargetChosen
- unit:IsAlive
- unit:IsDying
- unit:IsRevive
- unit:IsDead
- unit:IsDestroy
- unit:GetJobConfig
- unit:GetSkillLevel
- unit:InitRestraint
- unit:InitAttrMap
- unit:InitAttrMapMonsterConfig
- unit:SetInitAttr
- unit:SetAttr
- unit:ChangeAttr
- unit:ResetBurstSkillFrame
- unit:GetHp
- unit:GetRage
- unit:GetSpdAtk
- unit:GetSpdMove
- unit:GetRealtimeAttr
- unit:GetAttr
- unit:GetBaseAttr
- unit:GetBuffAttr
- unit:UpdateAttrCacheFromBuff
- unit:AddMaxSpecialShield
- unit:ClearMaxSpecialShield
- unit:UpdateCachedBuffEffect
- unit:UpdateBuffDeduceValue
- unit:GetEffectTotalValue
- unit:UpdateBuffIcon
- unit:GetBuffIconList
- unit:UpdateActionSpeed
- unit:UpdateMoveSpeed
- unit:UpdateTrapBuff
- unit:GetLastFrameBySkillId
- unit:GetNormalSkillCountSinceLastSkill
- unit:GetSkillLevelUpTriggerParam
- unit:GetSkillAlreadyTriggerCount
- unit:SaveTriggerSkill
- unit:GetName
- unit:AddFollowPositionUnitUid
- unit:SaveSpecial1035SettleUid
- unit:ClearSpecial1035SettleUids
- unit:AddBuff
- unit:RemoveBuff
- unit:UpdateCurMotionState
- unit:AddMotionState
- unit:RemoveMotionState
- unit:RemoveClearMotionState
- unit:SetStun
- unit:SetFreeze
- unit:SetStealth
- unit:SetTimePause
- unit:SetPetrified
- unit:SetSilent
- unit:SetCharm
- unit:SetPersistCast
- unit:SetDefense
- unit:SetBlind
- unit:SetFear
- unit:SetTrick
- unit:SetUnableToSelect
- unit:SetGhost
- unit:ClearForceControlState
- unit:ClearControlState
- unit:SetBeAttractedUid
- unit:SetCharmUid
- unit:ChangeHpAdaptToMax
- unit:OnBuffAttrChanged
- unit:UpdateTempHpPerAndMessageBar
- unit:UpdateTempHpPer
- unit:GetTargetUidList
- unit:GetAttackTargetUid
- unit:GetMoveTargetUid
- unit:SetAttackTargetUid
- unit:ForceChangeAttackTarget
- unit:SetMoveTargetUid
- unit:SaveSkillDamageForTestBalance
- unit:SaveNormalSkillDamage
- unit:SaveSmallSkillDamage
- unit:SaveUniqueSkillDamage
- unit:SaveBurstSkillDamage
- unit:SaveBuffDamage
- unit:SaveDamage
- unit:SaveDamaged
- unit:SetMoveToPosition
**Snippet:**
```lua
BattleUnit = {}
local RestraintAddName = {
  "restraint_add1",
  "restraint_add2",
  "restraint_add3",
  "restraint_add4",
  "restraint_add5"
}
local RestraintSubName = {
  "restraint_sub1",
```

---

## Battle/BattleVoice.lua.lua
**Functions:**
- BattleVoice.PlayVoice
- BattleVoice.StopVoice
- BattleVoice.StopAllVoice
**Snippet:**
```lua
BattleVoice = {}
local curSoundEventInsList = {}

function BattleVoice.PlayVoice(unitUid, bubbleType)
  local soundEventIns = curSoundEventInsList[unitUid]
  if soundEventIns and SoundManager:IsPlaying(soundEventIns) then
    if bubbleType == BUBBLE_TYPE_ENUM.UNIQUE then
      BattleVoice.StopVoice(unitUid)
    else
      return
```

---

## Battle/Battle_AngerBarByName.lua.lua
**Functions:**
- GetBattle_AngerBarUis
**Requires:**
- Battle_AngerFillByName
**Snippet:**
```lua
require("Battle_AngerFillByName")

function GetBattle_AngerBarUis(ui)
  local uis = {}
  uis.bar = GetBattle_AngerFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_AngerBossBarByName.lua.lua
**Functions:**
- GetBattle_AngerBossBarUis
**Requires:**
- Battle_AngerBossFillByName
**Snippet:**
```lua
require("Battle_AngerBossFillByName")

function GetBattle_AngerBossBarUis(ui)
  local uis = {}
  uis.bar = GetBattle_AngerBossFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_AngerBossFillByName.lua.lua
**Functions:**
- GetBattle_AngerBossFillUis
**Snippet:**
```lua
function GetBattle_AngerBossFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_AngerFillByName.lua.lua
**Functions:**
- GetBattle_AngerFillUis
**Snippet:**
```lua
function GetBattle_AngerFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_AngryByName.lua.lua
**Functions:**
- GetBattle_AngryUis
**Snippet:**
```lua
function GetBattle_AngryUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_AutoBtnByName.lua.lua
**Functions:**
- GetBattle_AutoBtnUis
**Snippet:**
```lua
function GetBattle_AutoBtnUis(ui)
  local uis = {}
  
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_AutoByName.lua.lua
**Functions:**
- GetBattle_AutoUis
**Snippet:**
```lua
function GetBattle_AutoUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.DotTxt = ui:GetChild("DotTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BattleStartBgByName.lua.lua
**Functions:**
- GetBattle_BattleStartBgUis
**Snippet:**
```lua
function GetBattle_BattleStartBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BattleStartByName.lua.lua
**Functions:**
- GetBattle_BattleStartUis
**Requires:**
- Battle_BattleStartBgByName
- Battle_BattleStartWaveByName
**Snippet:**
```lua
require("Battle_BattleStartBgByName")
require("Battle_BattleStartWaveByName")

function GetBattle_BattleStartUis(ui)
  local uis = {}
  uis.BattleStartBg = GetBattle_BattleStartBgUis(ui:GetChild("BattleStartBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.BattleStartWave = GetBattle_BattleStartWaveUis(ui:GetChild("BattleStartWave"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## Battle/Battle_BattleStartWaveBgByName.lua.lua
**Functions:**
- GetBattle_BattleStartWaveBgUis
**Snippet:**
```lua
function GetBattle_BattleStartWaveBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BattleStartWaveByName.lua.lua
**Functions:**
- GetBattle_BattleStartWaveUis
**Requires:**
- Battle_BattleStartWaveBgByName
**Snippet:**
```lua
require("Battle_BattleStartWaveBgByName")

function GetBattle_BattleStartWaveUis(ui)
  local uis = {}
  uis.BattleStartWaveBg = GetBattle_BattleStartWaveBgUis(ui:GetChild("BattleStartWaveBg"))
  uis.WaveTxt = ui:GetChild("WaveTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BattleUIByName.lua.lua
**Functions:**
- GetBattle_BattleUIUis
**Requires:**
- Battle_TimeByName
- Battle_WaveByName
- Battle_AutoByName
- Battle_IntegralByName
- Battle_BuffAddTagByName
- Battle_BossBattleTipsByName
- Battle_BurstRegionByName
- Battle_BurstCardHeadRegionByName
- Battle_TopLeftByName
- Battle_StopByName
- Battle_HangUpWindowByName
**Snippet:**
```lua
require("Battle_TimeByName")
require("Battle_WaveByName")
require("Battle_AutoByName")
require("Battle_IntegralByName")
require("Battle_BuffAddTagByName")
require("Battle_BossBattleTipsByName")
require("Battle_BurstRegionByName")
require("Battle_BurstCardHeadRegionByName")
require("Battle_TopLeftByName")
require("Battle_StopByName")
```

---

## Battle/Battle_BattleUIWindowByName.lua.lua
**Functions:**
- GetBattle_BattleUIWindowUis
**Requires:**
- Battle_BattleUIByName
**Snippet:**
```lua
require("Battle_BattleUIByName")

function GetBattle_BattleUIWindowUis(ui)
  local uis = {}
  uis.Main = GetBattle_BattleUIUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BlockHitNumberByName.lua.lua
**Functions:**
- GetBattle_BlockHitNumberUis
**Snippet:**
```lua
function GetBattle_BlockHitNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.colorCtr = ui:GetController("color")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BlockHitNumberTipsByName.lua.lua
**Functions:**
- GetBattle_BlockHitNumberTipsUis
**Requires:**
- Battle_BlockHitNumberByName
**Snippet:**
```lua
require("Battle_BlockHitNumberByName")

function GetBattle_BlockHitNumberTipsUis(ui)
  local uis = {}
  uis.BlockHitNumber = GetBattle_BlockHitNumberUis(ui:GetChild("BlockHitNumber"))
  uis.colorCtr = ui:GetController("color")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BossBattleTipsByName.lua.lua
**Functions:**
- GetBattle_BossBattleTipsUis
**Requires:**
- Battle_BossHeadByName
- Battle_BossNameByName
- Battle_BossBattleTipsInfo1ByName
**Snippet:**
```lua
require("Battle_BossHeadByName")
require("Battle_BossNameByName")
require("Battle_BossBattleTipsInfo1ByName")

function GetBattle_BossBattleTipsUis(ui)
  local uis = {}
  uis.BossBattleTips = GetBattle_BossHeadUis(ui:GetChild("BossBattleTips"))
  uis.BossName = GetBattle_BossNameUis(ui:GetChild("BossName"))
  uis.HpBossBigProgressBar = ui:GetChild("HpBossBigProgressBar")
  uis.DefenseBossBigProgressBar = ui:GetChild("DefenseBossBigProgressBar")
```

---

## Battle/Battle_BossBattleTipsInfo1ByName.lua.lua
**Functions:**
- GetBattle_BossBattleTipsInfo1Uis
**Snippet:**
```lua
function GetBattle_BossBattleTipsInfo1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BossElementByName.lua.lua
**Functions:**
- GetBattle_BossElementUis
**Snippet:**
```lua
function GetBattle_BossElementUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BossHeadBgByName.lua.lua
**Functions:**
- GetBattle_BossHeadBgUis
**Snippet:**
```lua
function GetBattle_BossHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BossHeadByName.lua.lua
**Functions:**
- GetBattle_BossHeadUis
**Requires:**
- Battle_BossHeadBgByName
**Snippet:**
```lua
require("Battle_BossHeadBgByName")

function GetBattle_BossHeadUis(ui)
  local uis = {}
  uis.BossHeadBg = GetBattle_BossHeadBgUis(ui:GetChild("BossHeadBg"))
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BossNameByName.lua.lua
**Functions:**
- GetBattle_BossNameUis
**Snippet:**
```lua
function GetBattle_BossNameUis(ui)
  local uis = {}
  
  uis.BossNameTxt = ui:GetChild("BossNameTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BosssBuffIconByName.lua.lua
**Functions:**
- GetBattle_BosssBuffIconUis
**Snippet:**
```lua
function GetBattle_BosssBuffIconUis(ui)
  local uis = {}
  
  uis.BuffIconLoader = ui:GetChild("BuffIconLoader")
  uis.BuffIconProgressBar = ui:GetChild("BuffIconProgressBar")
  uis.LoaderTxt = ui:GetChild("LoaderTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BuffAddTag1ByName.lua.lua
**Functions:**
- GetBattle_BuffAddTag1Uis
**Snippet:**
```lua
function GetBattle_BuffAddTag1Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.TimeProgressBar = ui:GetChild("TimeProgressBar")
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Battle/Battle_BuffAddTag1ProgressBarByName.lua.lua
**Functions:**
- GetBattle_BuffAddTag1ProgressBarUis
**Requires:**
- Battle_BuffAddTag1ProgressFillByName
**Snippet:**
```lua
require("Battle_BuffAddTag1ProgressFillByName")

function GetBattle_BuffAddTag1ProgressBarUis(ui)
  local uis = {}
  uis.bar = GetBattle_BuffAddTag1ProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BuffAddTag1ProgressFillByName.lua.lua
**Functions:**
- GetBattle_BuffAddTag1ProgressFillUis
**Snippet:**
```lua
function GetBattle_BuffAddTag1ProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BuffAddTag2ByName.lua.lua
**Functions:**
- GetBattle_BuffAddTag2Uis
**Snippet:**
```lua
function GetBattle_BuffAddTag2Uis(ui)
  local uis = {}
  
  uis.StartList = ui:GetChild("StartList")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.IntegralTxt = ui:GetChild("IntegralTxt")
  uis.IntegralProgressTxt = ui:GetChild("IntegralProgressTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BuffAddTag2StartByName.lua.lua
**Functions:**
- GetBattle_BuffAddTag2StartUis
**Snippet:**
```lua
function GetBattle_BuffAddTag2StartUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BuffAddTagByName.lua.lua
**Functions:**
- GetBattle_BuffAddTagUis
**Requires:**
- Battle_BuffAddTag2ByName
- Battle_BuffAddTag1ByName
**Snippet:**
```lua
require("Battle_BuffAddTag2ByName")
require("Battle_BuffAddTag1ByName")

function GetBattle_BuffAddTagUis(ui)
  local uis = {}
  uis.Tag2 = GetBattle_BuffAddTag2Uis(ui:GetChild("Tag2"))
  uis.Tag1 = GetBattle_BuffAddTag1Uis(ui:GetChild("Tag1"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Battle/Battle_BuffHitNumberByName.lua.lua
**Functions:**
- GetBattle_BuffHitNumberUis
**Snippet:**
```lua
function GetBattle_BuffHitNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.colorCtr = ui:GetController("color")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BuffHitNumberTipsByName.lua.lua
**Functions:**
- GetBattle_BuffHitNumberTipsUis
**Requires:**
- Battle_BuffHitNumberByName
**Snippet:**
```lua
require("Battle_BuffHitNumberByName")

function GetBattle_BuffHitNumberTipsUis(ui)
  local uis = {}
  uis.BuffHitNumber = GetBattle_BuffHitNumberUis(ui:GetChild("BuffHitNumber"))
  uis.colorCtr = ui:GetController("color")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BuffIconBarByName.lua.lua
**Functions:**
- GetBattle_BuffIconBarUis
**Snippet:**
```lua
function GetBattle_BuffIconBarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BuffIconLookBarByName.lua.lua
**Functions:**
- GetBattle_BuffIconLookBarUis
**Snippet:**
```lua
function GetBattle_BuffIconLookBarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BuffListWordByName.lua.lua
**Functions:**
- GetBattle_BuffListWordUis
**Requires:**
- Battle_PlayerBuffLookByName
**Snippet:**
```lua
require("Battle_PlayerBuffLookByName")

function GetBattle_BuffListWordUis(ui)
  local uis = {}
  uis.PlayerBuff = GetBattle_PlayerBuffLookUis(ui:GetChild("PlayerBuff"))
  uis.LineImage = ui:GetChild("LineImage")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## Battle/Battle_BuffWordAniByName.lua.lua
**Functions:**
- GetBattle_BuffWordAniUis
**Requires:**
- Battle_BuffWordByName
**Snippet:**
```lua
require("Battle_BuffWordByName")

function GetBattle_BuffWordAniUis(ui)
  local uis = {}
  uis.BuffWord = GetBattle_BuffWordUis(ui:GetChild("BuffWord"))
  uis.colorCtr = ui:GetController("color")
  uis.arrowCtr = ui:GetController("arrow")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BuffWordByName.lua.lua
**Functions:**
- GetBattle_BuffWordUis
**Snippet:**
```lua
function GetBattle_BuffWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.colorCtr = ui:GetController("color")
  uis.arrowCtr = ui:GetController("arrow")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BurstAutoProgressBarByName.lua.lua
**Functions:**
- GetBattle_BurstAutoProgressBarUis
**Requires:**
- Battle_BurstAutoProgressFillByName
**Snippet:**
```lua
require("Battle_BurstAutoProgressFillByName")

function GetBattle_BurstAutoProgressBarUis(ui)
  local uis = {}
  uis.bar = GetBattle_BurstAutoProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BurstAutoProgressFillByName.lua.lua
**Functions:**
- GetBattle_BurstAutoProgressFillUis
**Snippet:**
```lua
function GetBattle_BurstAutoProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BurstBlockHitNumberByName.lua.lua
**Functions:**
- GetBattle_BurstBlockHitNumberUis
**Snippet:**
```lua
function GetBattle_BurstBlockHitNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.colorCtr = ui:GetController("color")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BurstBlockHitNumberTipsByName.lua.lua
**Functions:**
- GetBattle_BurstBlockHitNumberTipsUis
**Requires:**
- Battle_BurstBlockHitNumberByName
**Snippet:**
```lua
require("Battle_BurstBlockHitNumberByName")

function GetBattle_BurstBlockHitNumberTipsUis(ui)
  local uis = {}
  uis.BlockHitNumber = GetBattle_BurstBlockHitNumberUis(ui:GetChild("BlockHitNumber"))
  uis.colorCtr = ui:GetController("color")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BurstBtnByName.lua.lua
**Functions:**
- GetBattle_BurstBtnUis
**Requires:**
- Battle_BurstTimeByName
**Snippet:**
```lua
require("Battle_BurstTimeByName")

function GetBattle_BurstBtnUis(ui)
  local uis = {}
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Effect3Holder = ui:GetChild("Effect3Holder")
  uis.Effect4Holder = ui:GetChild("Effect4Holder")
  uis.BurstTime = GetBattle_BurstTimeUis(ui:GetChild("BurstTime"))
  uis.WordTxt = ui:GetChild("WordTxt")
```

---

## Battle/Battle_BurstBuffHitNumberByName.lua.lua
**Functions:**
- GetBattle_BurstBuffHitNumberUis
**Snippet:**
```lua
function GetBattle_BurstBuffHitNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.colorCtr = ui:GetController("color")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BurstBuffHitNumberTipsByName.lua.lua
**Functions:**
- GetBattle_BurstBuffHitNumberTipsUis
**Requires:**
- Battle_BurstBuffHitNumberByName
**Snippet:**
```lua
require("Battle_BurstBuffHitNumberByName")

function GetBattle_BurstBuffHitNumberTipsUis(ui)
  local uis = {}
  uis.BuffHitNumber = GetBattle_BurstBuffHitNumberUis(ui:GetChild("BuffHitNumber"))
  uis.colorCtr = ui:GetController("color")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BurstCardHeadAni1ByName.lua.lua
**Functions:**
- GetBattle_BurstCardHeadAni1Uis
**Requires:**
- Battle_BurstCardHeadAniByName
**Snippet:**
```lua
require("Battle_BurstCardHeadAniByName")

function GetBattle_BurstCardHeadAni1Uis(ui)
  local uis = {}
  uis.BurstCardHead = GetBattle_BurstCardHeadAniUis(ui:GetChild("BurstCardHead"))
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BurstCardHeadAniByName.lua.lua
**Functions:**
- GetBattle_BurstCardHeadAniUis
**Requires:**
- Battle_BurstCardHeadByName
**Snippet:**
```lua
require("Battle_BurstCardHeadByName")

function GetBattle_BurstCardHeadAniUis(ui)
  local uis = {}
  uis.BurstCardHead = GetBattle_BurstCardHeadUis(ui:GetChild("BurstCardHead"))
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BurstCardHeadBgByName.lua.lua
**Functions:**
- GetBattle_BurstCardHeadBgUis
**Snippet:**
```lua
function GetBattle_BurstCardHeadBgUis(ui)
  local uis = {}
  
  uis.HeadLoader = ui:GetChild("HeadLoader")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BurstCardHeadByName.lua.lua
**Functions:**
- GetBattle_BurstCardHeadUis
**Requires:**
- CommonResource_OccupationByName
- Battle_BurstCardHeadWordByName
**Snippet:**
```lua
require("CommonResource_OccupationByName")
require("Battle_BurstCardHeadWordByName")

function GetBattle_BurstCardHeadUis(ui)
  local uis = {}
  uis.Occupation = GetCommonResource_OccupationUis(ui:GetChild("Occupation"))
  uis.ElementList = ui:GetChild("ElementList")
  uis.BurstCardHeadWord = GetBattle_BurstCardHeadWordUis(ui:GetChild("BurstCardHeadWord"))
  uis.BurstCardHeadProgressBar = ui:GetChild("BurstCardHeadProgressBar")
  uis.c2Ctr = ui:GetController("c2")
```

---

## Battle/Battle_BurstCardHeadProgressBarByName.lua.lua
**Functions:**
- GetBattle_BurstCardHeadProgressBarUis
**Requires:**
- Battle_BurstCardHeadBgByName
**Snippet:**
```lua
require("Battle_BurstCardHeadBgByName")

function GetBattle_BurstCardHeadProgressBarUis(ui)
  local uis = {}
  uis.BurstCardHeadBg = GetBattle_BurstCardHeadBgUis(ui:GetChild("BurstCardHeadBg"))
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## Battle/Battle_BurstCardHeadRegion1ByName.lua.lua
**Functions:**
- GetBattle_BurstCardHeadRegion1Uis
**Snippet:**
```lua
function GetBattle_BurstCardHeadRegion1Uis(ui)
  local uis = {}
  
  uis.BurstCardHeadList = ui:GetChild("BurstCardHeadList")
  uis.BurstAutoProgressBar = ui:GetChild("BurstAutoProgressBar")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BurstCardHeadRegionByName.lua.lua
**Functions:**
- GetBattle_BurstCardHeadRegionUis
**Requires:**
- Battle_BurstCardHeadRegion1ByName
**Snippet:**
```lua
require("Battle_BurstCardHeadRegion1ByName")

function GetBattle_BurstCardHeadRegionUis(ui)
  local uis = {}
  uis.BurstCardHeadList = GetBattle_BurstCardHeadRegion1Uis(ui:GetChild("BurstCardHeadList"))
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BurstCardHeadWordByName.lua.lua
**Functions:**
- GetBattle_BurstCardHeadWordUis
**Snippet:**
```lua
function GetBattle_BurstCardHeadWordUis(ui)
  local uis = {}
  
  uis.IconLoader = ui:GetChild("IconLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BurstCDProgressBarByName.lua.lua
**Functions:**
- GetBattle_BurstCDProgressBarUis
**Requires:**
- Battle_BurstCDProgressFillByName
**Snippet:**
```lua
require("Battle_BurstCDProgressFillByName")

function GetBattle_BurstCDProgressBarUis(ui)
  local uis = {}
  uis.bar = GetBattle_BurstCDProgressFillUis(ui:GetChild("bar"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Battle/Battle_BurstCDProgressFillByName.lua.lua
**Functions:**
- GetBattle_BurstCDProgressFillUis
**Snippet:**
```lua
function GetBattle_BurstCDProgressFillUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BurstCritHitNumberByName.lua.lua
**Functions:**
- GetBattle_BurstCritHitNumberUis
**Snippet:**
```lua
function GetBattle_BurstCritHitNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.colorCtr = ui:GetController("color")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BurstCritHitNumberTipsByName.lua.lua
**Functions:**
- GetBattle_BurstCritHitNumberTipsUis
**Requires:**
- Battle_BurstCritHitNumberByName
**Snippet:**
```lua
require("Battle_BurstCritHitNumberByName")

function GetBattle_BurstCritHitNumberTipsUis(ui)
  local uis = {}
  uis.CritHitNumber = GetBattle_BurstCritHitNumberUis(ui:GetChild("CritHitNumber"))
  uis.colorCtr = ui:GetController("color")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BurstGreenHpNumberByName.lua.lua
**Functions:**
- GetBattle_BurstGreenHpNumberUis
**Snippet:**
```lua
function GetBattle_BurstGreenHpNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.colorCtr = ui:GetController("color")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BurstGreenHpNumberTipsByName.lua.lua
**Functions:**
- GetBattle_BurstGreenHpNumberTipsUis
**Requires:**
- Battle_BurstGreenHpNumberByName
**Snippet:**
```lua
require("Battle_BurstGreenHpNumberByName")

function GetBattle_BurstGreenHpNumberTipsUis(ui)
  local uis = {}
  uis.GreenHpNumber = GetBattle_BurstGreenHpNumberUis(ui:GetChild("GreenHpNumber"))
  uis.colorCtr = ui:GetController("color")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BurstNormalHitNumberByName.lua.lua
**Functions:**
- GetBattle_BurstNormalHitNumberUis
**Snippet:**
```lua
function GetBattle_BurstNormalHitNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.colorCtr = ui:GetController("color")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BurstNormalHitNumberTipsByName.lua.lua
**Functions:**
- GetBattle_BurstNormalHitNumberTipsUis
**Requires:**
- Battle_BurstNormalHitNumberByName
**Snippet:**
```lua
require("Battle_BurstNormalHitNumberByName")

function GetBattle_BurstNormalHitNumberTipsUis(ui)
  local uis = {}
  uis.NormalHitNumber = GetBattle_BurstNormalHitNumberUis(ui:GetChild("NormalHitNumber"))
  uis.colorCtr = ui:GetController("color")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BurstRegionByName.lua.lua
**Functions:**
- GetBattle_BurstRegionUis
**Requires:**
- Battle_TacticalSkillRegionByName
**Snippet:**
```lua
require("Battle_TacticalSkillRegionByName")

function GetBattle_BurstRegionUis(ui)
  local uis = {}
  uis.CardHeadList = ui:GetChild("CardHeadList")
  uis.BurstBtn = ui:GetChild("BurstBtn")
  uis.TacticalSkillRegion = GetBattle_TacticalSkillRegionUis(ui:GetChild("TacticalSkillRegion"))
  uis.BurstCtr = ui:GetController("Burst")
  uis.GuildBossCtr = ui:GetController("GuildBoss")
  uis.root = ui
```

---

## Battle/Battle_BurstShieldHitNumberByName.lua.lua
**Functions:**
- GetBattle_BurstShieldHitNumberUis
**Snippet:**
```lua
function GetBattle_BurstShieldHitNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.colorCtr = ui:GetController("color")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BurstShieldHitNumberTipsByName.lua.lua
**Functions:**
- GetBattle_BurstShieldHitNumberTipsUis
**Requires:**
- Battle_BurstShieldHitNumberByName
**Snippet:**
```lua
require("Battle_BurstShieldHitNumberByName")

function GetBattle_BurstShieldHitNumberTipsUis(ui)
  local uis = {}
  uis.ShieldHitNumber = GetBattle_BurstShieldHitNumberUis(ui:GetChild("ShieldHitNumber"))
  uis.colorCtr = ui:GetController("color")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BurstTimeByName.lua.lua
**Functions:**
- GetBattle_BurstTimeUis
**Snippet:**
```lua
function GetBattle_BurstTimeUis(ui)
  local uis = {}
  
  uis.BurstNumTxt = ui:GetChild("BurstNumTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BurstUniqueSkillTipsAniByName.lua.lua
**Functions:**
- GetBattle_BurstUniqueSkillTipsAniUis
**Requires:**
- Battle_BurstUniqueSkillTipsByName
**Snippet:**
```lua
require("Battle_BurstUniqueSkillTipsByName")

function GetBattle_BurstUniqueSkillTipsAniUis(ui)
  local uis = {}
  uis.SkillTips = GetBattle_BurstUniqueSkillTipsUis(ui:GetChild("SkillTips"))
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_BurstUniqueSkillTipsByName.lua.lua
**Functions:**
- GetBattle_BurstUniqueSkillTipsUis
**Snippet:**
```lua
function GetBattle_BurstUniqueSkillTipsUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_Card10059ByName.lua.lua
**Functions:**
- GetBattle_Card10059Uis
**Snippet:**
```lua
function GetBattle_Card10059Uis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_Card10075ByName.lua.lua
**Functions:**
- GetBattle_Card10075Uis
**Snippet:**
```lua
function GetBattle_Card10075Uis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_Card10080ByName.lua.lua
**Functions:**
- GetBattle_Card10080Uis
**Snippet:**
```lua
function GetBattle_Card10080Uis(ui)
  local uis = {}
  
  uis.CardProgressBar = ui:GetChild("CardProgressBar")
  uis.DotList = ui:GetChild("DotList")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_Card10080DotByName.lua.lua
**Functions:**
- GetBattle_Card10080DotUis
**Snippet:**
```lua
function GetBattle_Card10080DotUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_Card10080ProgressBarByName.lua.lua
**Functions:**
- GetBattle_Card10080ProgressBarUis
**Snippet:**
```lua
function GetBattle_Card10080ProgressBarUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_Card10101ByName.lua.lua
**Functions:**
- GetBattle_Card10101Uis
**Snippet:**
```lua
function GetBattle_Card10101Uis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_Card10103ByName.lua.lua
**Functions:**
- GetBattle_Card10103Uis
**Snippet:**
```lua
function GetBattle_Card10103Uis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_Card10108ByName.lua.lua
**Functions:**
- GetBattle_Card10108Uis
**Snippet:**
```lua
function GetBattle_Card10108Uis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_CardBuffTipsByName.lua.lua
**Functions:**
- GetBattle_CardBuffTipsUis
**Snippet:**
```lua
function GetBattle_CardBuffTipsUis(ui)
  local uis = {}
  
  uis.BuffList = ui:GetChild("BuffList")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_CardBuffTipsUnitByName.lua.lua
**Functions:**
- GetBattle_CardBuffTipsUnitUis
**Requires:**
- Battle_CardBuffTipsByName
**Snippet:**
```lua
require("Battle_CardBuffTipsByName")

function GetBattle_CardBuffTipsUnitUis(ui)
  local uis = {}
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.CardBuffTips = GetBattle_CardBuffTipsUis(ui:GetChild("CardBuffTips"))
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_CardBurstCDBarByName.lua.lua
**Functions:**
- GetBattle_CardBurstCDBarUis
**Snippet:**
```lua
function GetBattle_CardBurstCDBarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_CardBurstCDFillByName.lua.lua
**Functions:**
- GetBattle_CardBurstCDFillUis
**Snippet:**
```lua
function GetBattle_CardBurstCDFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_CardHeadBgByName.lua.lua
**Functions:**
- GetBattle_CardHeadBgUis
**Snippet:**
```lua
function GetBattle_CardHeadBgUis(ui)
  local uis = {}
  
  uis.HeadLoader = ui:GetChild("HeadLoader")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_CardHeadByName.lua.lua
**Functions:**
- GetBattle_CardHeadUis
**Requires:**
- Battle_CardHeadBgByName
- Battle_CardSignByName
- Battle_NumberRoundByName
**Snippet:**
```lua
require("Battle_CardHeadBgByName")
require("Battle_CardSignByName")
require("Battle_NumberRoundByName")

function GetBattle_CardHeadUis(ui)
  local uis = {}
  uis.CardHeadBg = GetBattle_CardHeadBgUis(ui:GetChild("CardHeadBg"))
  uis.BurstCDProgressBar = ui:GetChild("BurstCDProgressBar")
  uis.CardSign = GetBattle_CardSignUis(ui:GetChild("CardSign"))
  uis.HpProgressBar = ui:GetChild("HpProgressBar")
```

---

## Battle/Battle_CardHeadOccupationByName.lua.lua
**Functions:**
- GetBattle_CardHeadOccupationUis
**Snippet:**
```lua
function GetBattle_CardHeadOccupationUis(ui)
  local uis = {}
  
  uis.OccupationTxt = ui:GetChild("OccupationTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_CardHeadRegionByName.lua.lua
**Functions:**
- GetBattle_CardHeadRegionUis
**Requires:**
- Battle_CardHeadOccupationByName
**Snippet:**
```lua
require("Battle_CardHeadOccupationByName")

function GetBattle_CardHeadRegionUis(ui)
  local uis = {}
  uis.HeadList = ui:GetChild("HeadList")
  uis.Occupation = GetBattle_CardHeadOccupationUis(ui:GetChild("Occupation"))
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_CardSignByName.lua.lua
**Functions:**
- GetBattle_CardSignUis
**Requires:**
- Battle_Card10080ByName
- Battle_Card10059ByName
- Battle_Card10101ByName
- Battle_Card10103ByName
- Battle_Card10108ByName
- Battle_Card10075ByName
**Snippet:**
```lua
require("Battle_Card10080ByName")
require("Battle_Card10059ByName")
require("Battle_Card10101ByName")
require("Battle_Card10103ByName")
require("Battle_Card10108ByName")
require("Battle_Card10075ByName")

function GetBattle_CardSignUis(ui)
  local uis = {}
  uis.Card10080 = GetBattle_Card10080Uis(ui:GetChild("Card10080"))
```

---

## Battle/Battle_CritHitNumberByName.lua.lua
**Functions:**
- GetBattle_CritHitNumberUis
**Snippet:**
```lua
function GetBattle_CritHitNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.colorCtr = ui:GetController("color")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_CritHitNumberTipsByName.lua.lua
**Functions:**
- GetBattle_CritHitNumberTipsUis
**Requires:**
- Battle_CritHitNumberByName
**Snippet:**
```lua
require("Battle_CritHitNumberByName")

function GetBattle_CritHitNumberTipsUis(ui)
  local uis = {}
  uis.CritHitNumber = GetBattle_CritHitNumberUis(ui:GetChild("CritHitNumber"))
  uis.colorCtr = ui:GetController("color")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_DefenseBarByName.lua.lua
**Functions:**
- GetBattle_DefenseBarUis
**Requires:**
- Battle_DefenseFillBackByName
- Battle_DefenseFillByName
**Snippet:**
```lua
require("Battle_DefenseFillBackByName")
require("Battle_DefenseFillByName")

function GetBattle_DefenseBarUis(ui)
  local uis = {}
  uis.bar_delay1 = GetBattle_DefenseFillBackUis(ui:GetChild("bar_delay1"))
  uis.bar = GetBattle_DefenseFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_DefenseBossBigBarByName.lua.lua
**Functions:**
- GetBattle_DefenseBossBigBarUis
**Requires:**
- Battle_DefenseBossBigFillBackByName
- Battle_DefenseBossBigFillByName
**Snippet:**
```lua
require("Battle_DefenseBossBigFillBackByName")
require("Battle_DefenseBossBigFillByName")

function GetBattle_DefenseBossBigBarUis(ui)
  local uis = {}
  uis.bar_delay1 = GetBattle_DefenseBossBigFillBackUis(ui:GetChild("bar_delay1"))
  uis.bar = GetBattle_DefenseBossBigFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_DefenseBossBigFillBackByName.lua.lua
**Functions:**
- GetBattle_DefenseBossBigFillBackUis
**Snippet:**
```lua
function GetBattle_DefenseBossBigFillBackUis(ui)
  local uis = {}
  
  uis.ShieldImage = ui:GetChild("ShieldImage")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_DefenseBossBigFillByName.lua.lua
**Functions:**
- GetBattle_DefenseBossBigFillUis
**Snippet:**
```lua
function GetBattle_DefenseBossBigFillUis(ui)
  local uis = {}
  
  uis.ShieldImage = ui:GetChild("ShieldImage")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_DefenseFillBackByName.lua.lua
**Functions:**
- GetBattle_DefenseFillBackUis
**Snippet:**
```lua
function GetBattle_DefenseFillBackUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_DefenseFillByName.lua.lua
**Functions:**
- GetBattle_DefenseFillUis
**Snippet:**
```lua
function GetBattle_DefenseFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_EndBgByName.lua.lua
**Functions:**
- GetBattle_EndBgUis
**Snippet:**
```lua
function GetBattle_EndBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_EndByName.lua.lua
**Functions:**
- GetBattle_EndUis
**Requires:**
- Battle_EndBgByName
**Snippet:**
```lua
require("Battle_EndBgByName")

function GetBattle_EndUis(ui)
  local uis = {}
  uis.EndBg = GetBattle_EndBgUis(ui:GetChild("EndBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_FailBgByName.lua.lua
**Functions:**
- GetBattle_FailBgUis
**Snippet:**
```lua
function GetBattle_FailBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_FailByName.lua.lua
**Functions:**
- GetBattle_FailUis
**Requires:**
- Battle_FailBgByName
**Snippet:**
```lua
require("Battle_FailBgByName")

function GetBattle_FailUis(ui)
  local uis = {}
  uis.WinBg = GetBattle_FailBgUis(ui:GetChild("WinBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_Firm1BarByName.lua.lua
**Functions:**
- GetBattle_Firm1BarUis
**Requires:**
- Battle_Firm1FillByName
**Snippet:**
```lua
require("Battle_Firm1FillByName")

function GetBattle_Firm1BarUis(ui)
  local uis = {}
  uis.bar = GetBattle_Firm1FillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_Firm1FillByName.lua.lua
**Functions:**
- GetBattle_Firm1FillUis
**Snippet:**
```lua
function GetBattle_Firm1FillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_FirmBarByName.lua.lua
**Functions:**
- GetBattle_FirmBarUis
**Requires:**
- Battle_FirmFillByName
**Snippet:**
```lua
require("Battle_FirmFillByName")

function GetBattle_FirmBarUis(ui)
  local uis = {}
  uis.bar = GetBattle_FirmFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_FirmFillByName.lua.lua
**Functions:**
- GetBattle_FirmFillUis
**Snippet:**
```lua
function GetBattle_FirmFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_GreenHpNumberByName.lua.lua
**Functions:**
- GetBattle_GreenHpNumberUis
**Snippet:**
```lua
function GetBattle_GreenHpNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.colorCtr = ui:GetController("color")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_GreenHpNumberTipsByName.lua.lua
**Functions:**
- GetBattle_GreenHpNumberTipsUis
**Requires:**
- Battle_GreenHpNumberByName
**Snippet:**
```lua
require("Battle_GreenHpNumberByName")

function GetBattle_GreenHpNumberTipsUis(ui)
  local uis = {}
  uis.GreenHpNumber = GetBattle_GreenHpNumberUis(ui:GetChild("GreenHpNumber"))
  uis.colorCtr = ui:GetController("color")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_HangUpByName.lua.lua
**Functions:**
- GetBattle_HangUpUis
**Snippet:**
```lua
function GetBattle_HangUpUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.OutTxt = ui:GetChild("OutTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_HangUpWindowByName.lua.lua
**Functions:**
- GetBattle_HangUpWindowUis
**Requires:**
- Battle_HangUpByName
**Snippet:**
```lua
require("Battle_HangUpByName")

function GetBattle_HangUpWindowUis(ui)
  local uis = {}
  uis.HangUp = GetBattle_HangUpUis(ui:GetChild("HangUp"))
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_HpBarByName.lua.lua
**Functions:**
- GetBattle_HpBarUis
**Requires:**
- Battle_HpFillBackByName
- Battle_HpFillByName
**Snippet:**
```lua
require("Battle_HpFillBackByName")
require("Battle_HpFillByName")

function GetBattle_HpBarUis(ui)
  local uis = {}
  uis.bar_delay = GetBattle_HpFillBackUis(ui:GetChild("bar_delay"))
  uis.bar = GetBattle_HpFillUis(ui:GetChild("bar"))
  uis.FirmProgressBar = ui:GetChild("FirmProgressBar")
  uis.SoulProgressBar = ui:GetChild("SoulProgressBar")
  uis.root = ui
```

---

## Battle/Battle_HpBossBigBarByName.lua.lua
**Functions:**
- GetBattle_HpBossBigBarUis
**Requires:**
- Battle_HpBossBigFillBackByName
- Battle_HpBossBigFillByName
**Snippet:**
```lua
require("Battle_HpBossBigFillBackByName")
require("Battle_HpBossBigFillByName")

function GetBattle_HpBossBigBarUis(ui)
  local uis = {}
  uis.bar_delay = GetBattle_HpBossBigFillBackUis(ui:GetChild("bar_delay"))
  uis.bar = GetBattle_HpBossBigFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_HpBossBigFillBackByName.lua.lua
**Functions:**
- GetBattle_HpBossBigFillBackUis
**Snippet:**
```lua
function GetBattle_HpBossBigFillBackUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_HpBossBigFillByName.lua.lua
**Functions:**
- GetBattle_HpBossBigFillUis
**Snippet:**
```lua
function GetBattle_HpBossBigFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_HpFillBackByName.lua.lua
**Functions:**
- GetBattle_HpFillBackUis
**Snippet:**
```lua
function GetBattle_HpFillBackUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_HpFillByName.lua.lua
**Functions:**
- GetBattle_HpFillUis
**Snippet:**
```lua
function GetBattle_HpFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_IntegralByName.lua.lua
**Functions:**
- GetBattle_IntegralUis
**Snippet:**
```lua
function GetBattle_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_NormalHitNumberByName.lua.lua
**Functions:**
- GetBattle_NormalHitNumberUis
**Snippet:**
```lua
function GetBattle_NormalHitNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.colorCtr = ui:GetController("color")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_NormalHitNumberTipsByName.lua.lua
**Functions:**
- GetBattle_NormalHitNumberTipsUis
**Requires:**
- Battle_NormalHitNumberByName
**Snippet:**
```lua
require("Battle_NormalHitNumberByName")

function GetBattle_NormalHitNumberTipsUis(ui)
  local uis = {}
  uis.NormalHitNumber = GetBattle_NormalHitNumberUis(ui:GetChild("NormalHitNumber"))
  uis.colorCtr = ui:GetController("color")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_NumberRoundByName.lua.lua
**Functions:**
- GetBattle_NumberRoundUis
**Snippet:**
```lua
function GetBattle_NumberRoundUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_OutTips1BtnByName.lua.lua
**Functions:**
- GetBattle_OutTips1BtnUis
**Snippet:**
```lua
function GetBattle_OutTips1BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_OutTips2BtnByName.lua.lua
**Functions:**
- GetBattle_OutTips2BtnUis
**Snippet:**
```lua
function GetBattle_OutTips2BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_OutTips3BtnByName.lua.lua
**Functions:**
- GetBattle_OutTips3BtnUis
**Snippet:**
```lua
function GetBattle_OutTips3BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_OutTipsByName.lua.lua
**Functions:**
- GetBattle_OutTipsUis
**Snippet:**
```lua
function GetBattle_OutTipsUis(ui)
  local uis = {}
  
  uis.OutTips2Btn = ui:GetChild("OutTips2Btn")
  uis.OutTips1Btn = ui:GetChild("OutTips1Btn")
  uis.OutTips3Btn = ui:GetChild("OutTips3Btn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_PlayerBuffLookByName.lua.lua
**Functions:**
- GetBattle_PlayerBuffLookUis
**Snippet:**
```lua
function GetBattle_PlayerBuffLookUis(ui)
  local uis = {}
  
  uis.BuffLoader = ui:GetChild("BuffLoader")
  uis.BuffIconProgressBar = ui:GetChild("BuffIconProgressBar")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_RageBgByName.lua.lua
**Functions:**
- GetBattle_RageBgUis
**Snippet:**
```lua
function GetBattle_RageBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_RageByName.lua.lua
**Functions:**
- GetBattle_RageUis
**Requires:**
- Battle_RagePopupBgByName
- Battle_RageBgByName
- Battle_RageCircle1ByName
- Battle_RageCircle3ByName
**Snippet:**
```lua
require("Battle_RagePopupBgByName")
require("Battle_RageBgByName")
require("Battle_RageCircle1ByName")
require("Battle_RageCircle3ByName")

function GetBattle_RageUis(ui)
  local uis = {}
  uis.PopupBg = GetBattle_RagePopupBgUis(ui:GetChild("PopupBg"))
  uis.RageBg = GetBattle_RageBgUis(ui:GetChild("RageBg"))
  uis.Circle1 = GetBattle_RageCircle1Uis(ui:GetChild("Circle1"))
```

---

## Battle/Battle_RageCircle1ByName.lua.lua
**Functions:**
- GetBattle_RageCircle1Uis
**Snippet:**
```lua
function GetBattle_RageCircle1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_RageCircle3ByName.lua.lua
**Functions:**
- GetBattle_RageCircle3Uis
**Snippet:**
```lua
function GetBattle_RageCircle3Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_RageLookBtnByName.lua.lua
**Functions:**
- GetBattle_RageLookBtnUis
**Snippet:**
```lua
function GetBattle_RageLookBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_RagePopupBgByName.lua.lua
**Functions:**
- GetBattle_RagePopupBgUis
**Snippet:**
```lua
function GetBattle_RagePopupBgUis(ui)
  local uis = {}
  
  uis.BlurLoader = ui:GetChild("BlurLoader")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_RageWindowByName.lua.lua
**Functions:**
- GetBattle_RageWindowUis
**Requires:**
- Battle_RageByName
**Snippet:**
```lua
require("Battle_RageByName")

function GetBattle_RageWindowUis(ui)
  local uis = {}
  uis.Main = GetBattle_RageUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_RoadColorByName.lua.lua
**Functions:**
- GetBattle_RoadColorUis
**Snippet:**
```lua
function GetBattle_RoadColorUis(ui)
  local uis = {}
  
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_RoadTestByName.lua.lua
**Functions:**
- GetBattle_RoadTestUis
**Snippet:**
```lua
function GetBattle_RoadTestUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_SetBtnByName.lua.lua
**Functions:**
- GetBattle_SetBtnUis
**Snippet:**
```lua
function GetBattle_SetBtnUis(ui)
  local uis = {}
  
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_ShieldHitNumberByName.lua.lua
**Functions:**
- GetBattle_ShieldHitNumberUis
**Snippet:**
```lua
function GetBattle_ShieldHitNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.colorCtr = ui:GetController("color")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_ShieldHitNumberTipsByName.lua.lua
**Functions:**
- GetBattle_ShieldHitNumberTipsUis
**Requires:**
- Battle_ShieldHitNumberByName
**Snippet:**
```lua
require("Battle_ShieldHitNumberByName")

function GetBattle_ShieldHitNumberTipsUis(ui)
  local uis = {}
  uis.ShieldHitNumber = GetBattle_ShieldHitNumberUis(ui:GetChild("ShieldHitNumber"))
  uis.colorCtr = ui:GetController("color")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_SkipBtnByName.lua.lua
**Functions:**
- GetBattle_SkipBtnUis
**Snippet:**
```lua
function GetBattle_SkipBtnUis(ui)
  local uis = {}
  
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_SmallSkillTipsAniByName.lua.lua
**Functions:**
- GetBattle_SmallSkillTipsAniUis
**Requires:**
- Battle_SmallSkillTipsByName
**Snippet:**
```lua
require("Battle_SmallSkillTipsByName")

function GetBattle_SmallSkillTipsAniUis(ui)
  local uis = {}
  uis.SkillTips = GetBattle_SmallSkillTipsUis(ui:GetChild("SkillTips"))
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_SmallSkillTipsByName.lua.lua
**Functions:**
- GetBattle_SmallSkillTipsUis
**Snippet:**
```lua
function GetBattle_SmallSkillTipsUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_SoulBarByName.lua.lua
**Functions:**
- GetBattle_SoulBarUis
**Requires:**
- Battle_SoulFillByName
**Snippet:**
```lua
require("Battle_SoulFillByName")

function GetBattle_SoulBarUis(ui)
  local uis = {}
  uis.bar = GetBattle_SoulFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_SoulFillByName.lua.lua
**Functions:**
- GetBattle_SoulFillUis
**Snippet:**
```lua
function GetBattle_SoulFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_SpeedBtnByName.lua.lua
**Functions:**
- GetBattle_SpeedBtnUis
**Snippet:**
```lua
function GetBattle_SpeedBtnUis(ui)
  local uis = {}
  
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_StopBtnByName.lua.lua
**Functions:**
- GetBattle_StopBtnUis
**Snippet:**
```lua
function GetBattle_StopBtnUis(ui)
  local uis = {}
  
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_StopByName.lua.lua
**Functions:**
- GetBattle_StopUis
**Requires:**
- Battle_OutTipsByName
**Snippet:**
```lua
require("Battle_OutTipsByName")

function GetBattle_StopUis(ui)
  local uis = {}
  uis.WaveWordTxt = ui:GetChild("WaveWordTxt")
  uis.OutTips = GetBattle_OutTipsUis(ui:GetChild("OutTips"))
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_SurpriseByName.lua.lua
**Functions:**
- GetBattle_SurpriseUis
**Snippet:**
```lua
function GetBattle_SurpriseUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_SystemBtnByName.lua.lua
**Functions:**
- GetBattle_SystemBtnUis
**Snippet:**
```lua
function GetBattle_SystemBtnUis(ui)
  local uis = {}
  
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_TacticalSkillAutoBtnByName.lua.lua
**Functions:**
- GetBattle_TacticalSkillAutoBtnUis
**Snippet:**
```lua
function GetBattle_TacticalSkillAutoBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_TacticalSkillBtnByName.lua.lua
**Functions:**
- GetBattle_TacticalSkillBtnUis
**Snippet:**
```lua
function GetBattle_TacticalSkillBtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.SkillCDProgressBar = ui:GetChild("SkillCDProgressBar")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Battle/Battle_TacticalSkillCDProgressBarByName.lua.lua
**Functions:**
- GetBattle_TacticalSkillCDProgressBarUis
**Requires:**
- Battle_TacticalSkillCDProgressFillByName
**Snippet:**
```lua
require("Battle_TacticalSkillCDProgressFillByName")

function GetBattle_TacticalSkillCDProgressBarUis(ui)
  local uis = {}
  uis.bar1 = GetBattle_TacticalSkillCDProgressFillUis(ui:GetChild("bar1"))
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_TacticalSkillCDProgressFillByName.lua.lua
**Functions:**
- GetBattle_TacticalSkillCDProgressFillUis
**Snippet:**
```lua
function GetBattle_TacticalSkillCDProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_TacticalSkillRegionByName.lua.lua
**Functions:**
- GetBattle_TacticalSkillRegionUis
**Snippet:**
```lua
function GetBattle_TacticalSkillRegionUis(ui)
  local uis = {}
  
  uis.SkillList = ui:GetChild("SkillList")
  uis.AutoBtn = ui:GetChild("AutoBtn")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_TalkByName.lua.lua
**Functions:**
- GetBattle_TalkUis
**Snippet:**
```lua
function GetBattle_TalkUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_TimeByName.lua.lua
**Functions:**
- GetBattle_TimeUis
**Snippet:**
```lua
function GetBattle_TimeUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.TimeNumTxt = ui:GetChild("TimeNumTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_TopLeftByName.lua.lua
**Functions:**
- GetBattle_TopLeftUis
**Snippet:**
```lua
function GetBattle_TopLeftUis(ui)
  local uis = {}
  
  uis.FunctionList = ui:GetChild("FunctionList")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_UniqueSkillTipsAniByName.lua.lua
**Functions:**
- GetBattle_UniqueSkillTipsAniUis
**Requires:**
- Battle_UniqueSkillTipsByName
**Snippet:**
```lua
require("Battle_UniqueSkillTipsByName")

function GetBattle_UniqueSkillTipsAniUis(ui)
  local uis = {}
  uis.SkillTips = GetBattle_UniqueSkillTipsUis(ui:GetChild("SkillTips"))
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_UniqueSkillTipsByName.lua.lua
**Functions:**
- GetBattle_UniqueSkillTipsUis
**Snippet:**
```lua
function GetBattle_UniqueSkillTipsUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_WaveByName.lua.lua
**Functions:**
- GetBattle_WaveUis
**Snippet:**
```lua
function GetBattle_WaveUis(ui)
  local uis = {}
  
  uis.WaveTxt = ui:GetChild("WaveTxt")
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_WinBgByName.lua.lua
**Functions:**
- GetBattle_WinBgUis
**Snippet:**
```lua
function GetBattle_WinBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Battle/Battle_WinByName.lua.lua
**Functions:**
- GetBattle_WinUis
**Requires:**
- Battle_WinBgByName
**Snippet:**
```lua
require("Battle_WinBgByName")

function GetBattle_WinUis(ui)
  local uis = {}
  uis.WinBg = GetBattle_WinBgUis(ui:GetChild("WinBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.root = ui
  return uis
end
```

---
