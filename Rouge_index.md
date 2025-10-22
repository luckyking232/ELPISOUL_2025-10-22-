# Rouge

## Rouge/QBSwitchWindow.lua.lua
**Functions:**
- QBSwitchWindow.ReInitData
- QBSwitchWindow.OnInit
- QBSwitchWindow.UpdateInfo
- headlist.itemRenderer
- QBSwitchWindow.InitBtn
- QBSwitchWindow.OnClose
**Requires:**
- Abyss_QBSwitchWindowByName
**Snippet:**
```lua
require("Abyss_QBSwitchWindowByName")
local QBSwitchWindow = {}
local uis, contentPane

function QBSwitchWindow.ReInitData()
end

function QBSwitchWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.QBSwitchWindow.package, WinResConfig.QBSwitchWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/Raffle01_BoxBtnByName.lua.lua
**Functions:**
- GetRaffle01_BoxBtnUis
**Snippet:**
```lua
function GetRaffle01_BoxBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/Raffle01_BoxByName.lua.lua
**Functions:**
- GetRaffle01_BoxUis
**Requires:**
- Raffle01_BoxSpendByName
**Snippet:**
```lua
require("Raffle01_BoxSpendByName")

function GetRaffle01_BoxUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Spend = GetRaffle01_BoxSpendUis(ui:GetChild("Spend"))
  uis.BoxBtn = ui:GetChild("BoxBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Rouge/Raffle01_BoxSpendByName.lua.lua
**Functions:**
- GetRaffle01_BoxSpendUis
**Snippet:**
```lua
function GetRaffle01_BoxSpendUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/Raffle01_ExplainContentByName.lua.lua
**Functions:**
- GetRaffle01_ExplainContentUis
**Snippet:**
```lua
function GetRaffle01_ExplainContentUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.root = ui
  return uis
end
```

---

## Rouge/Raffle01_ExplainTipsByName.lua.lua
**Functions:**
- GetRaffle01_ExplainTipsUis
**Requires:**
- CommonResource_PopupBgByName
- Raffle01_ExplainTipsRegionByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Raffle01_ExplainTipsRegionByName")

function GetRaffle01_ExplainTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.ExplainTips = GetRaffle01_ExplainTipsRegionUis(ui:GetChild("ExplainTips"))
  uis.root = ui
  return uis
```

---

## Rouge/Raffle01_ExplainTipsInfoByName.lua.lua
**Functions:**
- GetRaffle01_ExplainTipsInfoUis
**Snippet:**
```lua
function GetRaffle01_ExplainTipsInfoUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.ContentList = ui:GetChild("ContentList")
  uis.root = ui
  return uis
end
```

---

## Rouge/Raffle01_ExplainTipsRegionByName.lua.lua
**Functions:**
- GetRaffle01_ExplainTipsRegionUis
**Requires:**
- Raffle01_ExplainTipsInfoByName
**Snippet:**
```lua
require("Raffle01_ExplainTipsInfoByName")

function GetRaffle01_ExplainTipsRegionUis(ui)
  local uis = {}
  uis.Tips = GetRaffle01_ExplainTipsInfoUis(ui:GetChild("Tips"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/Raffle01_ExplainTipsWindowByName.lua.lua
**Functions:**
- GetRaffle01_ExplainTipsWindowUis
**Requires:**
- Raffle01_ExplainTipsByName
**Snippet:**
```lua
require("Raffle01_ExplainTipsByName")

function GetRaffle01_ExplainTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetRaffle01_ExplainTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/Raffle01_ExplainWordByName.lua.lua
**Functions:**
- GetRaffle01_ExplainWordUis
**Snippet:**
```lua
function GetRaffle01_ExplainWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/Raffle01_RaffleByName.lua.lua
**Functions:**
- GetRaffle01_RaffleUis
**Requires:**
- CommonResource_BackGroundByName
- Raffle01_Raffle_TimeByName
- Raffle01_Task_ItemRegionByName
- Raffle01_BoxByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Raffle01_Raffle_TimeByName")
require("Raffle01_Task_ItemRegionByName")
require("Raffle01_BoxByName")
require("CommonResource_CurrencyReturnByName")

function GetRaffle01_RaffleUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
```

---

## Rouge/Raffle01_RaffleWindowByName.lua.lua
**Functions:**
- GetRaffle01_RaffleWindowUis
**Requires:**
- Raffle01_RaffleByName
**Snippet:**
```lua
require("Raffle01_RaffleByName")

function GetRaffle01_RaffleWindowUis(ui)
  local uis = {}
  uis.Main = GetRaffle01_RaffleUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/Raffle01_Raffle_TimeByName.lua.lua
**Functions:**
- GetRaffle01_Raffle_TimeUis
**Snippet:**
```lua
function GetRaffle01_Raffle_TimeUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/Raffle01_Reward_GetWordByName.lua.lua
**Functions:**
- GetRaffle01_Reward_GetWordUis
**Snippet:**
```lua
function GetRaffle01_Reward_GetWordUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/Raffle01_Reward_ItemByName.lua.lua
**Functions:**
- GetRaffle01_Reward_ItemUis
**Requires:**
- CommonResource_ItemFrameByName
- Raffle01_Reward_MoveWordByName
- Raffle01_Reward_ProbabilityByName
- Raffle01_Reward_NumberLockByName
- Raffle01_Reward_GetWordByName
**Snippet:**
```lua
require("CommonResource_ItemFrameByName")
require("Raffle01_Reward_MoveWordByName")
require("Raffle01_Reward_ProbabilityByName")
require("Raffle01_Reward_NumberLockByName")
require("Raffle01_Reward_GetWordByName")

function GetRaffle01_Reward_ItemUis(ui)
  local uis = {}
  uis.Item = GetCommonResource_ItemFrameUis(ui:GetChild("Item"))
  uis.MoveWord = GetRaffle01_Reward_MoveWordUis(ui:GetChild("MoveWord"))
```

---

## Rouge/Raffle01_Reward_MoveWordByName.lua.lua
**Functions:**
- GetRaffle01_Reward_MoveWordUis
**Snippet:**
```lua
function GetRaffle01_Reward_MoveWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/Raffle01_Reward_NowByName.lua.lua
**Functions:**
- GetRaffle01_Reward_NowUis
**Snippet:**
```lua
function GetRaffle01_Reward_NowUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/Raffle01_Reward_NumberLockByName.lua.lua
**Functions:**
- GetRaffle01_Reward_NumberLockUis
**Snippet:**
```lua
function GetRaffle01_Reward_NumberLockUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/Raffle01_Reward_ProbabilityByName.lua.lua
**Functions:**
- GetRaffle01_Reward_ProbabilityUis
**Snippet:**
```lua
function GetRaffle01_Reward_ProbabilityUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/Raffle01_Reward_TabBtnByName.lua.lua
**Functions:**
- GetRaffle01_Reward_TabBtnUis
**Requires:**
- Raffle01_Reward_NowByName
- Raffle01_Reward_TimeLockByName
**Snippet:**
```lua
require("Raffle01_Reward_NowByName")
require("Raffle01_Reward_TimeLockByName")

function GetRaffle01_Reward_TabBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Now = GetRaffle01_Reward_NowUis(ui:GetChild("Now"))
  uis.Lcok = GetRaffle01_Reward_TimeLockUis(ui:GetChild("Lcok"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Rouge/Raffle01_Reward_TimeLockByName.lua.lua
**Functions:**
- GetRaffle01_Reward_TimeLockUis
**Snippet:**
```lua
function GetRaffle01_Reward_TimeLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/Raffle01_Task_ItemByName.lua.lua
**Functions:**
- GetRaffle01_Task_ItemUis
**Snippet:**
```lua
function GetRaffle01_Task_ItemUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.PriceTxt = ui:GetChild("PriceTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/Raffle01_Task_ItemRegionByName.lua.lua
**Functions:**
- GetRaffle01_Task_ItemRegionUis
**Requires:**
- Raffle01_Task_ItemByName
**Snippet:**
```lua
require("Raffle01_Task_ItemByName")

function GetRaffle01_Task_ItemRegionUis(ui)
  local uis = {}
  uis.DayItem = GetRaffle01_Task_ItemUis(ui:GetChild("DayItem"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
```

---

## Rouge/RaffleExplainTipsWindow.lua.lua
**Functions:**
- RaffleExplainTipsWindow.ReInitData
- RaffleExplainTipsWindow.OnInit
- RaffleExplainTipsWindow.UpdateInfo
- tips.Tips.ContentList.itemRenderer
- wordList.itemRenderer
- RaffleExplainTipsWindow.InitBtn
- RaffleExplainTipsWindow.OnClose
**Requires:**
- Raffle01_ExplainTipsWindowByName
**Snippet:**
```lua
require("Raffle01_ExplainTipsWindowByName")
local RaffleExplainTipsWindow = {}
local uis, contentPane

function RaffleExplainTipsWindow.ReInitData()
end

function RaffleExplainTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RaffleExplainTipsWindow.package, WinResConfig.RaffleExplainTipsWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/RaffleWindow.lua.lua
**Functions:**
- RaffleWindow.ReInitData
- RaffleWindow.OnInit
- RaffleWindow.UpdateInfo
- list.itemRenderer
- RaffleWindow.ShowReward
- list.itemRenderer
- RaffleWindow.ShowRecharge
- tips.ItemList.itemRenderer
- RaffleWindow.GetPoolInfo
- RaffleWindow.GetData
- RaffleWindow.InitAssetsTips
- uis.Main.AssetsTipsList.itemRenderer
- RaffleWindow.GetCost
- RaffleWindow.ShowBox
- RaffleWindow.InitBtn
- RaffleWindow.OnShown
- RaffleWindow.OnClose
- RaffleWindow.CheckActivityEnd
- RaffleWindow.HandleMessage
**Requires:**
- Raffle01_RaffleWindowByName
**Snippet:**
```lua
require("Raffle01_RaffleWindowByName")
local RaffleWindow = {}
local uis, contentPane, jumpTb, lastItem, rechargeConf, costType, roundInfo

function RaffleWindow.ReInitData()
end

function RaffleWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RaffleWindow.package, WinResConfig.RaffleWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/RageSkillWindow.lua.lua
**Functions:**
- RageSkillWindow.ReInitData
- RageSkillWindow.OnInit
- RageSkillWindow.UpdateInfo
- RageSkillWindow.InitBtn
- RageSkillWindow.TouchClose
- RageSkillWindow.OnClose
**Requires:**
- RaidBossTips_RageSkillWindowByName
**Snippet:**
```lua
require("RaidBossTips_RageSkillWindowByName")
local RageSkillWindow = {}
local uis, contentPane, monsterIdList

function RageSkillWindow.ReInitData()
end

function RageSkillWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RageSkillWindow.package, WinResConfig.RageSkillWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/RageWindow.lua.lua
**Functions:**
- RageWindow.ReInitData
- RageWindow.OnInit
- RageWindow.UpdateInfo
- RageWindow.InitBtn
- RageWindow.TouchLookSkill
- RageWindow.TouchClose
- RageWindow.OnShowAnimationEnd
- RageWindow.OnClose
**Requires:**
- Battle_RageWindowByName
**Snippet:**
```lua
require("Battle_RageWindowByName")
local RageWindow = {}
local uis, contentPane, tempBattleUnit

function RageWindow.ReInitData()
end

function RageWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RageWindow.package, WinResConfig.RageWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/RaidBossActionRecordWindow.lua.lua
**Functions:**
- list.itemRenderer
- headlist.itemRenderer
- RaidBossActionRecordWindow.ReInitData
- RaidBossActionRecordWindow.OnInit
- RaidBossActionRecordWindow.UpdateInfo
- RaidBossActionRecordWindow.InitBtn
- RaidBossActionRecordWindow.OnClose
- RaidBossActionRecordWindow.HandleMessage
**Requires:**
- RaidBoss_ActionRecordWindowByName
**Snippet:**
```lua
require("RaidBoss_ActionRecordWindowByName")
local RaidBossActionRecordWindow = {}
local uis, contentPane, uin, challenges, selfInfo, stageId, showCurDamage
local RefreshRecordsInfo = function(challenges)
  local maxRounds = 3
  if stageId then
    local conf = TableData.GetConfig(stageId, "BaseStage")
    if conf and conf.rounds then
      maxRounds = conf.rounds
    end
```

---

## Rouge/RaidBossConfig.lua.lua
**Snippet:**
```lua
return {
  [1] = {
    cover_effect_path = "Assets/Art/Effects/Prefab/UI_prefab/SoloBosschallenge/FX_ui_back_solobosschallenge.prefab",
    home_effect_path = "Assets/Art/Effects/Prefab/UI_prefab/SoloBosschallenge/FX_ui_back_solobosschallenge_in.prefab",
    presets_paths = {
      {
        path = "Assets/Art/Models/UI_spine/prefab/SoloBossChallenge/BOSS_001/boss001_yinyi.prefab"
      },
      {
        path = "Assets/Art/Effects/Prefab/UI_prefab/SoloBosschallenge/FX_ui_solo_bosschallenge_yinyi_zhezhao.prefab"
```

---

## Rouge/RaidBossData.lua.lua
**Snippet:**
```lua
local raidBossData, playersRankData, playersRankInfoList
local GetLevelList = function()
  local data = RaidBossData.GetRaidBossData()
  local chapter = data.curChapter
  local conf = TableData.GetConfig(chapter, "BaseChapter")
  return conf.stages
end
local GetLevelIdByDifficult = function(diff)
  local levels = GetLevelList()
  if levels then
```

---

## Rouge/RaidBossGiveUpWindow.lua.lua
**Functions:**
- RaidBossGiveUpWindow.ReInitData
- RaidBossGiveUpWindow.OnInit
- RaidBossGiveUpWindow.UpdateInfo
- RaidBossGiveUpWindow.InitBtn
- RaidBossGiveUpWindow.OnClose
**Requires:**
- RaidBoss_GiveUpWindowByName
**Snippet:**
```lua
require("RaidBoss_GiveUpWindowByName")
local RaidBossGiveUpWindow = {}
local uis, contentPane, stageId, callback

function RaidBossGiveUpWindow.ReInitData()
end

function RaidBossGiveUpWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RaidBossGiveUpWindow.package, WinResConfig.RaidBossGiveUpWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/RaidBossMgr.lua.lua
**Snippet:**
```lua
local GetLevelIndex = function(stageId)
  local levels = RaidBossData.GetLevelList()
  local result = 0
  for i = 1, #levels do
    if stageId == levels[i] then
      result = i - 1
      break
    end
  end
  return result
```

---

## Rouge/RaidBossPlayerRankWindow.lua.lua
**Functions:**
- RaidBossPlayerRankWindow.ReInitData
- RaidBossPlayerRankWindow.OnInit
- RaidBossPlayerRankWindow.UpdateInfo
- RaidBossPlayerRankWindow.InitBtn
- RaidBossPlayerRankWindow.OnClose
- RaidBossPlayerRankWindow.HandleMessage
**Requires:**
- RaidBoss_PlayerRankWindowByName
**Snippet:**
```lua
require("RaidBoss_PlayerRankWindowByName")
local RaidBossPlayerRankWindow = {}
local uis, contentPane
local PlayerRankInfoItemRenderer = function(i, gcmp)
  local rank = i + 1
  local info = RaidBossData.GetPlayerRankInfoAt(rank)
  local child = gcmp:GetChild("PlayerRankTips")
  local playerNumber = child:GetChild("PlayerNumber")
  UIUtil.SetText(playerNumber, rank, "NumberTxt")
  if rank <= 3 then
```

---

## Rouge/RaidBossQuickBattleWindow.lua.lua
**Functions:**
- RaidBossQuickBattleWindow.ReInitData
- RaidBossQuickBattleWindow.OnInit
- RaidBossQuickBattleWindow.UpdateInfo
- RaidBossQuickBattleWindow.InitBtn
- RaidBossQuickBattleWindow.OnClose
**Requires:**
- RaidBoss_QuickBattleWindowByName
**Snippet:**
```lua
require("RaidBoss_QuickBattleWindowByName")
local RaidBossQuickBattleWindow = {}
local uis, contentPane, sweepingNum, stageId
local RefreshSweepingDisplay = function(maxSweepingNum)
  local content = string.format("%s[color=#949494]/%s[/color]", sweepingNum, maxSweepingNum)
  uis.Main.QuickBattleContent.NumberRegion.NumberTxt.text = content
end

function RaidBossQuickBattleWindow.ReInitData()
end
```

---

## Rouge/RaidBossQuickRewardWindow.lua.lua
**Functions:**
- RaidBossQuickRewardWindow.ReInitData
- RaidBossQuickRewardWindow.OnInit
- RaidBossQuickRewardWindow.UpdateInfo
- list.itemRenderer
- RaidBossQuickRewardWindow.InitBtn
- RaidBossQuickRewardWindow.OnClose
**Requires:**
- RaidBoss_QuickRewardWindowByName
**Snippet:**
```lua
require("RaidBoss_QuickRewardWindowByName")
local RaidBossQuickRewardWindow = {}
local uis, contentPane, rewards, distinct

function RaidBossQuickRewardWindow.ReInitData()
end

function RaidBossQuickRewardWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RaidBossQuickRewardWindow.package, WinResConfig.RaidBossQuickRewardWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/RaidBossRankChangeWindow.lua.lua
**Functions:**
- RaidBossRankChangeWindow.ReInitData
- RaidBossRankChangeWindow.OnInit
- RaidBossRankChangeWindow.UpdateInfo
- RaidBossRankChangeWindow.InitBtn
- RaidBossRankChangeWindow.OnClose
**Requires:**
- RaidBoss_RankChangeWindowByName
**Snippet:**
```lua
require("RaidBoss_RankChangeWindowByName")
local RaidBossRankChangeWindow = {}
local uis, contentPane, rankUpInfo

function RaidBossRankChangeWindow.ReInitData()
end

function RaidBossRankChangeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RaidBossRankChangeWindow.package, WinResConfig.RaidBossRankChangeWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/RaidBossRewardShowWindow.lua.lua
**Functions:**
- glist.itemRenderer
- RaidBossRewardShowWindow.ReInitData
- RaidBossRewardShowWindow.OnInit
- RaidBossRewardShowWindow.UpdateInfo
- RaidBossRewardShowWindow.InitBtn
- RaidBossRewardShowWindow.OnClose
- RaidBossRewardShowWindow.HandleMessage
**Requires:**
- RaidBoss_RewardShowWindowByName
**Snippet:**
```lua
require("RaidBoss_RewardShowWindowByName")
local RaidBossRewardShowWindow = {}
local uis, contentPane, rankRewards, levelRewards
local tablist = {
  [1] = {
    ctrl = 0,
    title = T(20283)
  },
  [2] = {
    ctrl = 1,
```

---

## Rouge/RaidBossScriptList.lua.lua
**Requires:**
- RaidBossConfig
- RaidBossService
- RaidBossData
- RaidBossMgr
**Snippet:**
```lua
RaidBossConfig = require("RaidBossConfig")
RaidBossService = require("RaidBossService")
RaidBossData = require("RaidBossData")
RaidBossMgr = require("RaidBossMgr")
```

---

## Rouge/RaidBossService.lua.lua
**Snippet:**
```lua
local GetRaidBossInfoReq = function(rspCallback)
  Net.Send(Proto.MsgName.GetBossInfoReq, nil, rspCallback)
end
local GetRaidBossInfoRsp = function(msg)
  RaidBossData.SetRaidBossData(msg)
  UIMgr:SendWindowMessage(WinResConfig.AdventureWindow.name, WindowMsgEnum.Adventure.REFRESH_BOSS_MAP)
  RedDotMgr.UpdateNode(RED_DOT_DATA_TYPE.ADVENTURE)
  UIMgr:SendWindowMessage(WinResConfig.RaidBossWindow.name, WindowMsgEnum.RaidBossWindow.REFRESH_PANEL_INFO)
end
local player_rank_info_msg = {}
```

---

## Rouge/RaidBossTips_RageSkillByName.lua.lua
**Functions:**
- GetRaidBossTips_RageSkillUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetRaidBossTips_RageSkillUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.SkillList = ui:GetChild("SkillList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBossTips_RageSkillReturnBtnByName.lua.lua
**Functions:**
- GetRaidBossTips_RageSkillReturnBtnUis
**Snippet:**
```lua
function GetRaidBossTips_RageSkillReturnBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBossTips_RageSkillTipsByName.lua.lua
**Functions:**
- GetRaidBossTips_RageSkillTipsUis
**Requires:**
- RaidBossTips_RageSkillWordByName
**Snippet:**
```lua
require("RaidBossTips_RageSkillWordByName")

function GetRaidBossTips_RageSkillTipsUis(ui)
  local uis = {}
  uis.killWord1 = GetRaidBossTips_RageSkillWordUis(ui:GetChild("killWord1"))
  uis.killWord2 = GetRaidBossTips_RageSkillWordUis(ui:GetChild("killWord2"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBossTips_RageSkillWindowByName.lua.lua
**Functions:**
- GetRaidBossTips_RageSkillWindowUis
**Requires:**
- RaidBossTips_RageSkillByName
**Snippet:**
```lua
require("RaidBossTips_RageSkillByName")

function GetRaidBossTips_RageSkillWindowUis(ui)
  local uis = {}
  uis.Main = GetRaidBossTips_RageSkillUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBossTips_RageSkillWordByName.lua.lua
**Functions:**
- GetRaidBossTips_RageSkillWordUis
**Snippet:**
```lua
function GetRaidBossTips_RageSkillWordUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBossWindow.lua.lua
**Functions:**
- RefreshPanelInfo
- RaidBossWindow.ReInitData
- RaidBossWindow.OnInit
- RaidBossWindow.UpdateInfo
- RaidBossWindow.InitBtn
- RaidBossWindow.OnClose
- RaidBossWindow.HandleMessage
**Requires:**
- RaidBoss_RaidBossWindowByName
**Snippet:**
```lua
require("RaidBoss_RaidBossWindowByName")
local RaidBossWindow = {}
local uis, contentPane, selectedLevelIndex, selectedRoundIndex, loaded, gameObjects, spine_parts, backgroundEffect
local level_color_lookup = {
  [1] = {
    0,
    0,
    48,
    100
  },
```

---

## Rouge/RaidBoss_ActionRecordByName.lua.lua
**Functions:**
- GetRaidBoss_ActionRecordUis
**Requires:**
- CommonResource_PopupBgByName
- RaidBoss_ActionRecordTitleByName
- RaidBoss_ActionRecordNowRankByName
- RaidBoss_ActionRecordTipsListByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("RaidBoss_ActionRecordTitleByName")
require("RaidBoss_ActionRecordNowRankByName")
require("RaidBoss_ActionRecordTipsListByName")

function GetRaidBoss_ActionRecordUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.ActionRecordTitle = GetRaidBoss_ActionRecordTitleUis(ui:GetChild("ActionRecordTitle"))
  uis.NowRank = GetRaidBoss_ActionRecordNowRankUis(ui:GetChild("NowRank"))
```

---

## Rouge/RaidBoss_ActionRecordNowRankByName.lua.lua
**Functions:**
- GetRaidBoss_ActionRecordNowRankUis
**Snippet:**
```lua
function GetRaidBoss_ActionRecordNowRankUis(ui)
  local uis = {}
  
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.Rank1Txt = ui:GetChild("Rank1Txt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.RankTxt = ui:GetChild("RankTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Rouge/RaidBoss_ActionRecordTipsAniByName.lua.lua
**Functions:**
- GetRaidBoss_ActionRecordTipsAniUis
**Requires:**
- RaidBoss_ActionRecordTipsByName
**Snippet:**
```lua
require("RaidBoss_ActionRecordTipsByName")

function GetRaidBoss_ActionRecordTipsAniUis(ui)
  local uis = {}
  uis.ActionRecordTips = GetRaidBoss_ActionRecordTipsUis(ui:GetChild("ActionRecordTips"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_ActionRecordTipsByName.lua.lua
**Functions:**
- GetRaidBoss_ActionRecordTipsUis
**Snippet:**
```lua
function GetRaidBoss_ActionRecordTipsUis(ui)
  local uis = {}
  
  uis.RoundTxt = ui:GetChild("RoundTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.HeadList = ui:GetChild("HeadList")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_ActionRecordTipsCloseBtnByName.lua.lua
**Functions:**
- GetRaidBoss_ActionRecordTipsCloseBtnUis
**Snippet:**
```lua
function GetRaidBoss_ActionRecordTipsCloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_ActionRecordTipsListByName.lua.lua
**Functions:**
- GetRaidBoss_ActionRecordTipsListUis
**Snippet:**
```lua
function GetRaidBoss_ActionRecordTipsListUis(ui)
  local uis = {}
  
  uis.RewardTipsList = ui:GetChild("RewardTipsList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_ActionRecordTitleByName.lua.lua
**Functions:**
- GetRaidBoss_ActionRecordTitleUis
**Snippet:**
```lua
function GetRaidBoss_ActionRecordTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_ActionRecordWindowByName.lua.lua
**Functions:**
- GetRaidBoss_ActionRecordWindowUis
**Requires:**
- RaidBoss_ActionRecordByName
**Snippet:**
```lua
require("RaidBoss_ActionRecordByName")

function GetRaidBoss_ActionRecordWindowUis(ui)
  local uis = {}
  uis.Main = GetRaidBoss_ActionRecordUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_BattleBeforeInfoByName.lua.lua
**Functions:**
- GetRaidBoss_BattleBeforeInfoUis
**Requires:**
- RaidBoss_BossNameByName
- RaidBoss_BattleNumberByName
- RaidBoss_BattleClearByName
**Snippet:**
```lua
require("RaidBoss_BossNameByName")
require("RaidBoss_BattleNumberByName")
require("RaidBoss_BattleClearByName")

function GetRaidBoss_BattleBeforeInfoUis(ui)
  local uis = {}
  uis.BossName = GetRaidBoss_BossNameUis(ui:GetChild("BossName"))
  uis.BattleNumber = GetRaidBoss_BattleNumberUis(ui:GetChild("BattleNumber"))
  uis.GoBattleBtn = ui:GetChild("GoBattleBtn")
  uis.BattleClear = GetRaidBoss_BattleClearUis(ui:GetChild("BattleClear"))
```

---

## Rouge/RaidBoss_BattleClearByName.lua.lua
**Functions:**
- GetRaidBoss_BattleClearUis
**Snippet:**
```lua
function GetRaidBoss_BattleClearUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_BattleInfo1ByName.lua.lua
**Functions:**
- GetRaidBoss_BattleInfo1Uis
**Requires:**
- RaidBoss_BossHPInfoByName
- RaidBoss_BattleNumberRegionByName
**Snippet:**
```lua
require("RaidBoss_BossHPInfoByName")
require("RaidBoss_BattleNumberRegionByName")

function GetRaidBoss_BattleInfo1Uis(ui)
  local uis = {}
  uis.BossHPInfo = GetRaidBoss_BossHPInfoUis(ui:GetChild("BossHPInfo"))
  uis.BattleNumberRegion = GetRaidBoss_BattleNumberRegionUis(ui:GetChild("BattleNumberRegion"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Rouge/RaidBoss_BattleInfoByName.lua.lua
**Functions:**
- GetRaidBoss_BattleInfoUis
**Requires:**
- RaidBoss_BattleRoundByName
- RaidBoss_BattleNumberByName
**Snippet:**
```lua
require("RaidBoss_BattleRoundByName")
require("RaidBoss_BattleNumberByName")

function GetRaidBoss_BattleInfoUis(ui)
  local uis = {}
  uis.BattleRound = GetRaidBoss_BattleRoundUis(ui:GetChild("BattleRound"))
  uis.BattleNumber = GetRaidBoss_BattleNumberUis(ui:GetChild("BattleNumber"))
  uis.HeadList = ui:GetChild("HeadList")
  uis.TestBattleBtn = ui:GetChild("TestBattleBtn")
  uis.GoBattleBtn = ui:GetChild("GoBattleBtn")
```

---

## Rouge/RaidBoss_BattleNumberByName.lua.lua
**Functions:**
- GetRaidBoss_BattleNumberUis
**Snippet:**
```lua
function GetRaidBoss_BattleNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_BattleNumberNewByName.lua.lua
**Functions:**
- GetRaidBoss_BattleNumberNewUis
**Snippet:**
```lua
function GetRaidBoss_BattleNumberNewUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_BattleNumberRecordByName.lua.lua
**Functions:**
- GetRaidBoss_BattleNumberRecordUis
**Snippet:**
```lua
function GetRaidBoss_BattleNumberRecordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_BattleNumberRegionByName.lua.lua
**Functions:**
- GetRaidBoss_BattleNumberRegionUis
**Requires:**
- RaidBoss_BattleNumberRecordByName
- RaidBoss_BattleNumberNewByName
**Snippet:**
```lua
require("RaidBoss_BattleNumberRecordByName")
require("RaidBoss_BattleNumberNewByName")

function GetRaidBoss_BattleNumberRegionUis(ui)
  local uis = {}
  uis.BattleNumberRecord = GetRaidBoss_BattleNumberRecordUis(ui:GetChild("BattleNumberRecord"))
  uis.BattleNumberNew = GetRaidBoss_BattleNumberNewUis(ui:GetChild("BattleNumberNew"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_BattleOutBtnByName.lua.lua
**Functions:**
- GetRaidBoss_BattleOutBtnUis
**Snippet:**
```lua
function GetRaidBoss_BattleOutBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_BattleRecordBtnByName.lua.lua
**Functions:**
- GetRaidBoss_BattleRecordBtnUis
**Snippet:**
```lua
function GetRaidBoss_BattleRecordBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_BattleRoundBtnByName.lua.lua
**Functions:**
- GetRaidBoss_BattleRoundBtnUis
**Snippet:**
```lua
function GetRaidBoss_BattleRoundBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_BattleRoundByName.lua.lua
**Functions:**
- GetRaidBoss_BattleRoundUis
**Snippet:**
```lua
function GetRaidBoss_BattleRoundUis(ui)
  local uis = {}
  
  uis.RoundList = ui:GetChild("RoundList")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_BattleStartBtnByName.lua.lua
**Functions:**
- GetRaidBoss_BattleStartBtnUis
**Snippet:**
```lua
function GetRaidBoss_BattleStartBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_BattleStartMainByName.lua.lua
**Functions:**
- GetRaidBoss_BattleStartMainUis
**Requires:**
- RaidBoss_BattleInfo1ByName
- RaidBoss_BattleInfoByName
**Snippet:**
```lua
require("RaidBoss_BattleInfo1ByName")
require("RaidBoss_BattleInfoByName")

function GetRaidBoss_BattleStartMainUis(ui)
  local uis = {}
  uis.BattleInfo1 = GetRaidBoss_BattleInfo1Uis(ui:GetChild("BattleInfo1"))
  uis.BattleOutBtn = ui:GetChild("BattleOutBtn")
  uis.BattleRecordBtn = ui:GetChild("BattleRecordBtn")
  uis.BattleInfo = GetRaidBoss_BattleInfoUis(ui:GetChild("BattleInfo"))
  uis.root = ui
```

---

## Rouge/RaidBoss_BossHPInfiniteByName.lua.lua
**Functions:**
- GetRaidBoss_BossHPInfiniteUis
**Snippet:**
```lua
function GetRaidBoss_BossHPInfiniteUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_BossHPInfoByName.lua.lua
**Functions:**
- GetRaidBoss_BossHPInfoUis
**Requires:**
- RaidBoss_DifficultyDotByName
- RaidBoss_BossHPInfiniteByName
**Snippet:**
```lua
require("RaidBoss_DifficultyDotByName")
require("RaidBoss_BossHPInfiniteByName")

function GetRaidBoss_BossHPInfoUis(ui)
  local uis = {}
  uis.HPProgressBar = ui:GetChild("HPProgressBar")
  uis.DifficultyDot = GetRaidBoss_DifficultyDotUis(ui:GetChild("DifficultyDot"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.Infinite = GetRaidBoss_BossHPInfiniteUis(ui:GetChild("Infinite"))
```

---

## Rouge/RaidBoss_BossMainByName.lua.lua
**Functions:**
- GetRaidBoss_BossMainUis
**Requires:**
- RaidBoss_DifficultyByName
- RaidBoss_BattleNumberRecordByName
- RaidBoss_BattleBeforeInfoByName
**Snippet:**
```lua
require("RaidBoss_DifficultyByName")
require("RaidBoss_BattleNumberRecordByName")
require("RaidBoss_BattleBeforeInfoByName")

function GetRaidBoss_BossMainUis(ui)
  local uis = {}
  uis.Difficulty = GetRaidBoss_DifficultyUis(ui:GetChild("Difficulty"))
  uis.BattleNumberRecord = GetRaidBoss_BattleNumberRecordUis(ui:GetChild("BattleNumberRecord"))
  uis.LeftArrowBtn = ui:GetChild("LeftArrowBtn")
  uis.RightArrowBtn = ui:GetChild("RightArrowBtn")
```

---

## Rouge/RaidBoss_BossNameByName.lua.lua
**Functions:**
- GetRaidBoss_BossNameUis
**Snippet:**
```lua
function GetRaidBoss_BossNameUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_CardHeadAniByName.lua.lua
**Functions:**
- GetRaidBoss_CardHeadAniUis
**Snippet:**
```lua
function GetRaidBoss_CardHeadAniUis(ui)
  local uis = {}
  
  uis.CardHeadBtn = ui:GetChild("CardHeadBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_CardHeadBgByName.lua.lua
**Functions:**
- GetRaidBoss_CardHeadBgUis
**Snippet:**
```lua
function GetRaidBoss_CardHeadBgUis(ui)
  local uis = {}
  
  uis.CardPicLoader = ui:GetChild("CardPicLoader")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_CardHeadBtnByName.lua.lua
**Functions:**
- GetRaidBoss_CardHeadBtnUis
**Requires:**
- RaidBoss_CardHeadBgByName
- CommonResource_OccupationByName
**Snippet:**
```lua
require("RaidBoss_CardHeadBgByName")
require("CommonResource_OccupationByName")

function GetRaidBoss_CardHeadBtnUis(ui)
  local uis = {}
  uis.CardPic = GetRaidBoss_CardHeadBgUis(ui:GetChild("CardPic"))
  uis.ElementList = ui:GetChild("ElementList")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Occupation = GetCommonResource_OccupationUis(ui:GetChild("Occupation"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## Rouge/RaidBoss_DifficultyByName.lua.lua
**Functions:**
- GetRaidBoss_DifficultyUis
**Snippet:**
```lua
function GetRaidBoss_DifficultyUis(ui)
  local uis = {}
  
  uis.DotList = ui:GetChild("DotList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_DifficultyDot1ByName.lua.lua
**Functions:**
- GetRaidBoss_DifficultyDot1Uis
**Snippet:**
```lua
function GetRaidBoss_DifficultyDot1Uis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_DifficultyDotByName.lua.lua
**Functions:**
- GetRaidBoss_DifficultyDotUis
**Snippet:**
```lua
function GetRaidBoss_DifficultyDotUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_DifficultyDotRegionByName.lua.lua
**Functions:**
- GetRaidBoss_DifficultyDotRegionUis
**Requires:**
- RaidBoss_DifficultyDotByName
- RaidBoss_DifficultyDot1ByName
**Snippet:**
```lua
require("RaidBoss_DifficultyDotByName")
require("RaidBoss_DifficultyDot1ByName")

function GetRaidBoss_DifficultyDotRegionUis(ui)
  local uis = {}
  uis.Dot = GetRaidBoss_DifficultyDotUis(ui:GetChild("Dot"))
  uis.Dot1 = GetRaidBoss_DifficultyDot1Uis(ui:GetChild("Dot1"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Rouge/RaidBoss_DifficultyRewardNumberByName.lua.lua
**Functions:**
- GetRaidBoss_DifficultyRewardNumberUis
**Snippet:**
```lua
function GetRaidBoss_DifficultyRewardNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_DifficultyRewardTipsAniByName.lua.lua
**Functions:**
- GetRaidBoss_DifficultyRewardTipsAniUis
**Requires:**
- RaidBoss_DifficultyRewardTipsByName
**Snippet:**
```lua
require("RaidBoss_DifficultyRewardTipsByName")

function GetRaidBoss_DifficultyRewardTipsAniUis(ui)
  local uis = {}
  uis.DifficultyRewardTips = GetRaidBoss_DifficultyRewardTipsUis(ui:GetChild("DifficultyRewardTips"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_DifficultyRewardTipsByName.lua.lua
**Functions:**
- GetRaidBoss_DifficultyRewardTipsUis
**Requires:**
- RaidBoss_DifficultyRewardNumberByName
- RaidBoss_DifficultyRewardTipsProgressByName
**Snippet:**
```lua
require("RaidBoss_DifficultyRewardNumberByName")
require("RaidBoss_DifficultyRewardTipsProgressByName")

function GetRaidBoss_DifficultyRewardTipsUis(ui)
  local uis = {}
  uis.DifficultyRewardNumber = GetRaidBoss_DifficultyRewardNumberUis(ui:GetChild("DifficultyRewardNumber"))
  uis.RewardList = ui:GetChild("RewardList")
  uis.Progress = GetRaidBoss_DifficultyRewardTipsProgressUis(ui:GetChild("Progress"))
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Rouge/RaidBoss_DifficultyRewardTipsGetBtnByName.lua.lua
**Functions:**
- GetRaidBoss_DifficultyRewardTipsGetBtnUis
**Snippet:**
```lua
function GetRaidBoss_DifficultyRewardTipsGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_DifficultyRewardTipsListByName.lua.lua
**Functions:**
- GetRaidBoss_DifficultyRewardTipsListUis
**Snippet:**
```lua
function GetRaidBoss_DifficultyRewardTipsListUis(ui)
  local uis = {}
  
  uis.RewardTipsList = ui:GetChild("RewardTipsList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_DifficultyRewardTipsProgressByName.lua.lua
**Functions:**
- GetRaidBoss_DifficultyRewardTipsProgressUis
**Snippet:**
```lua
function GetRaidBoss_DifficultyRewardTipsProgressUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_GiveUpByName.lua.lua
**Functions:**
- GetRaidBoss_GiveUpUis
**Requires:**
- CommonResource_PopupBgByName
- RaidBoss_GiveUpContentByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("RaidBoss_GiveUpContentByName")

function GetRaidBoss_GiveUpUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.GiveUpContent = GetRaidBoss_GiveUpContentUis(ui:GetChild("GiveUpContent"))
  uis.root = ui
  return uis
```

---

## Rouge/RaidBoss_GiveUpCloseBtnByName.lua.lua
**Functions:**
- GetRaidBoss_GiveUpCloseBtnUis
**Snippet:**
```lua
function GetRaidBoss_GiveUpCloseBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_GiveUpContentByName.lua.lua
**Functions:**
- GetRaidBoss_GiveUpContentUis
**Snippet:**
```lua
function GetRaidBoss_GiveUpContentUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.SureBtn = ui:GetChild("SureBtn")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_GiveUpSureBtnByName.lua.lua
**Functions:**
- GetRaidBoss_GiveUpSureBtnUis
**Snippet:**
```lua
function GetRaidBoss_GiveUpSureBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_GiveUpWindowByName.lua.lua
**Functions:**
- GetRaidBoss_GiveUpWindowUis
**Requires:**
- RaidBoss_GiveUpByName
**Snippet:**
```lua
require("RaidBoss_GiveUpByName")

function GetRaidBoss_GiveUpWindowUis(ui)
  local uis = {}
  uis.Main = GetRaidBoss_GiveUpUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_GoBattleBtnByName.lua.lua
**Functions:**
- GetRaidBoss_GoBattleBtnUis
**Snippet:**
```lua
function GetRaidBoss_GoBattleBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_HPProgressBarByName.lua.lua
**Functions:**
- GetRaidBoss_HPProgressBarUis
**Requires:**
- RaidBoss_HPProgressFillByName
**Snippet:**
```lua
require("RaidBoss_HPProgressFillByName")

function GetRaidBoss_HPProgressBarUis(ui)
  local uis = {}
  uis.bar = GetRaidBoss_HPProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_HPProgressFillByName.lua.lua
**Functions:**
- GetRaidBoss_HPProgressFillUis
**Snippet:**
```lua
function GetRaidBoss_HPProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_LeftArrowBtnByName.lua.lua
**Functions:**
- GetRaidBoss_LeftArrowBtnUis
**Snippet:**
```lua
function GetRaidBoss_LeftArrowBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_NowRank1ByName.lua.lua
**Functions:**
- GetRaidBoss_NowRank1Uis
**Snippet:**
```lua
function GetRaidBoss_NowRank1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.RankTxt = ui:GetChild("RankTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_NowRank2ByName.lua.lua
**Functions:**
- GetRaidBoss_NowRank2Uis
**Snippet:**
```lua
function GetRaidBoss_NowRank2Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.RankTxt = ui:GetChild("RankTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_NowRankByName.lua.lua
**Functions:**
- GetRaidBoss_NowRankUis
**Snippet:**
```lua
function GetRaidBoss_NowRankUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.RankTxt = ui:GetChild("RankTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_OwnByName.lua.lua
**Functions:**
- GetRaidBoss_OwnUis
**Snippet:**
```lua
function GetRaidBoss_OwnUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_PlayerHeadPicHeadPicByName.lua.lua
**Functions:**
- GetRaidBoss_PlayerHeadPicHeadPicUis
**Snippet:**
```lua
function GetRaidBoss_PlayerHeadPicHeadPicUis(ui)
  local uis = {}
  
  uis.HeadLoader = ui:GetChild("HeadLoader")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_PlayerLookBtnByName.lua.lua
**Functions:**
- GetRaidBoss_PlayerLookBtnUis
**Snippet:**
```lua
function GetRaidBoss_PlayerLookBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_PlayerNumberByName.lua.lua
**Functions:**
- GetRaidBoss_PlayerNumberUis
**Snippet:**
```lua
function GetRaidBoss_PlayerNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_PlayerRankByName.lua.lua
**Functions:**
- GetRaidBoss_PlayerRankUis
**Requires:**
- CommonResource_PopupBgByName
- RaidBoss_PlayerRankTitleByName
- RaidBoss_NowRank1ByName
- RaidBoss_NowRank2ByName
- RaidBoss_PlayerRankEmptyByName
- RaidBoss_PlayerRankTipsListByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("RaidBoss_PlayerRankTitleByName")
require("RaidBoss_NowRank1ByName")
require("RaidBoss_NowRank2ByName")
require("RaidBoss_PlayerRankEmptyByName")
require("RaidBoss_PlayerRankTipsListByName")

function GetRaidBoss_PlayerRankUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
```

---

## Rouge/RaidBoss_PlayerRankEmptyByName.lua.lua
**Functions:**
- GetRaidBoss_PlayerRankEmptyUis
**Snippet:**
```lua
function GetRaidBoss_PlayerRankEmptyUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_PlayerRankTipsAniByName.lua.lua
**Functions:**
- GetRaidBoss_PlayerRankTipsAniUis
**Requires:**
- RaidBoss_PlayerRankTipsByName
**Snippet:**
```lua
require("RaidBoss_PlayerRankTipsByName")

function GetRaidBoss_PlayerRankTipsAniUis(ui)
  local uis = {}
  uis.PlayerRankTips = GetRaidBoss_PlayerRankTipsUis(ui:GetChild("PlayerRankTips"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_PlayerRankTipsByName.lua.lua
**Functions:**
- GetRaidBoss_PlayerRankTipsUis
**Requires:**
- RaidBoss_PlayerNumberByName
- CommonResource_HeadByName
**Snippet:**
```lua
require("RaidBoss_PlayerNumberByName")
require("CommonResource_HeadByName")

function GetRaidBoss_PlayerRankTipsUis(ui)
  local uis = {}
  uis.PlayerNumber = GetRaidBoss_PlayerNumberUis(ui:GetChild("PlayerNumber"))
  uis.Head = GetCommonResource_HeadUis(ui:GetChild("Head"))
  uis.GuildTxt = ui:GetChild("GuildTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
```

---

## Rouge/RaidBoss_PlayerRankTipsListByName.lua.lua
**Functions:**
- GetRaidBoss_PlayerRankTipsListUis
**Snippet:**
```lua
function GetRaidBoss_PlayerRankTipsListUis(ui)
  local uis = {}
  
  uis.RewardTipsList = ui:GetChild("RewardTipsList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_PlayerRankTitleByName.lua.lua
**Functions:**
- GetRaidBoss_PlayerRankTitleUis
**Snippet:**
```lua
function GetRaidBoss_PlayerRankTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_PlayerRankWindowByName.lua.lua
**Functions:**
- GetRaidBoss_PlayerRankWindowUis
**Requires:**
- RaidBoss_PlayerRankByName
**Snippet:**
```lua
require("RaidBoss_PlayerRankByName")

function GetRaidBoss_PlayerRankWindowUis(ui)
  local uis = {}
  uis.Main = GetRaidBoss_PlayerRankUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_QuickBattleAddBtnByName.lua.lua
**Functions:**
- GetRaidBoss_QuickBattleAddBtnUis
**Snippet:**
```lua
function GetRaidBoss_QuickBattleAddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_QuickBattleByName.lua.lua
**Functions:**
- GetRaidBoss_QuickBattleUis
**Requires:**
- CommonResource_PopupBgByName
- RaidBoss_QuickBattleContentByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("RaidBoss_QuickBattleContentByName")

function GetRaidBoss_QuickBattleUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.QuickBattleContent = GetRaidBoss_QuickBattleContentUis(ui:GetChild("QuickBattleContent"))
  uis.root = ui
  return uis
```

---

## Rouge/RaidBoss_QuickBattleContentByName.lua.lua
**Functions:**
- GetRaidBoss_QuickBattleContentUis
**Requires:**
- RaidBoss_QuickBattleNumberRegionByName
**Snippet:**
```lua
require("RaidBoss_QuickBattleNumberRegionByName")

function GetRaidBoss_QuickBattleContentUis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberRegion = GetRaidBoss_QuickBattleNumberRegionUis(ui:GetChild("NumberRegion"))
  uis.SureBtn = ui:GetChild("SureBtn")
  uis.root = ui
  return uis
```

---

## Rouge/RaidBoss_QuickBattleNumberRegionByName.lua.lua
**Functions:**
- GetRaidBoss_QuickBattleNumberRegionUis
**Snippet:**
```lua
function GetRaidBoss_QuickBattleNumberRegionUis(ui)
  local uis = {}
  
  uis.AddBtn = ui:GetChild("AddBtn")
  uis.ReduceBtn = ui:GetChild("ReduceBtn")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_QuickBattleReduceBtnByName.lua.lua
**Functions:**
- GetRaidBoss_QuickBattleReduceBtnUis
**Snippet:**
```lua
function GetRaidBoss_QuickBattleReduceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_QuickBattleSureBtnByName.lua.lua
**Functions:**
- GetRaidBoss_QuickBattleSureBtnUis
**Snippet:**
```lua
function GetRaidBoss_QuickBattleSureBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_QuickBattleWindowByName.lua.lua
**Functions:**
- GetRaidBoss_QuickBattleWindowUis
**Requires:**
- RaidBoss_QuickBattleByName
**Snippet:**
```lua
require("RaidBoss_QuickBattleByName")

function GetRaidBoss_QuickBattleWindowUis(ui)
  local uis = {}
  uis.Main = GetRaidBoss_QuickBattleUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_QuickRewardByName.lua.lua
**Functions:**
- GetRaidBoss_QuickRewardUis
**Requires:**
- CommonResource_PopupBgByName
- RaidBoss_QuickRewardContentByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("RaidBoss_QuickRewardContentByName")

function GetRaidBoss_QuickRewardUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.QuickRewardContent = GetRaidBoss_QuickRewardContentUis(ui:GetChild("QuickRewardContent"))
  uis.root = ui
  return uis
```

---

## Rouge/RaidBoss_QuickRewardContentByName.lua.lua
**Functions:**
- GetRaidBoss_QuickRewardContentUis
**Snippet:**
```lua
function GetRaidBoss_QuickRewardContentUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_QuickRewardWindowByName.lua.lua
**Functions:**
- GetRaidBoss_QuickRewardWindowUis
**Requires:**
- RaidBoss_QuickRewardByName
**Snippet:**
```lua
require("RaidBoss_QuickRewardByName")

function GetRaidBoss_QuickRewardWindowUis(ui)
  local uis = {}
  uis.Main = GetRaidBoss_QuickRewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_RaidBossByName.lua.lua
**Functions:**
- GetRaidBoss_RaidBossUis
**Requires:**
- CommonResource_BackGroundByName
- RaidBoss_BossMainByName
- RaidBoss_BattleStartMainByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("RaidBoss_BossMainByName")
require("RaidBoss_BattleStartMainByName")
require("CommonResource_CurrencyReturnByName")

function GetRaidBoss_RaidBossUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BossMain = GetRaidBoss_BossMainUis(ui:GetChild("BossMain"))
  uis.BattleStartMain = GetRaidBoss_BattleStartMainUis(ui:GetChild("BattleStartMain"))
```

---

## Rouge/RaidBoss_RaidBossWindowByName.lua.lua
**Functions:**
- GetRaidBoss_RaidBossWindowUis
**Requires:**
- RaidBoss_RaidBossByName
**Snippet:**
```lua
require("RaidBoss_RaidBossByName")

function GetRaidBoss_RaidBossWindowUis(ui)
  local uis = {}
  uis.Main = GetRaidBoss_RaidBossUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_RankBtnByName.lua.lua
**Functions:**
- GetRaidBoss_RankBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetRaidBoss_RankBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_RankChangeByName.lua.lua
**Functions:**
- GetRaidBoss_RankChangeUis
**Requires:**
- CommonResource_PopupBgByName
- RaidBoss_RankChangeContentByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("RaidBoss_RankChangeContentByName")

function GetRaidBoss_RankChangeUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.RankChangeContent = GetRaidBoss_RankChangeContentUis(ui:GetChild("RankChangeContent"))
  uis.root = ui
  return uis
```

---

## Rouge/RaidBoss_RankChangeContentByName.lua.lua
**Functions:**
- GetRaidBoss_RankChangeContentUis
**Requires:**
- RaidBoss_RankChangeNumberByName
- RaidBoss_RankChangeRecordByName
**Snippet:**
```lua
require("RaidBoss_RankChangeNumberByName")
require("RaidBoss_RankChangeRecordByName")

function GetRaidBoss_RankChangeContentUis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.ChangeNumber = GetRaidBoss_RankChangeNumberUis(ui:GetChild("ChangeNumber"))
  uis.ChangeRecord = GetRaidBoss_RankChangeRecordUis(ui:GetChild("ChangeRecord"))
  uis.root = ui
  return uis
```

---

## Rouge/RaidBoss_RankChangeNumberByName.lua.lua
**Functions:**
- GetRaidBoss_RankChangeNumberUis
**Snippet:**
```lua
function GetRaidBoss_RankChangeNumberUis(ui)
  local uis = {}
  
  uis.RankTxt = ui:GetChild("RankTxt")
  uis.ChangeTxt = ui:GetChild("ChangeTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_RankChangeRecordByName.lua.lua
**Functions:**
- GetRaidBoss_RankChangeRecordUis
**Snippet:**
```lua
function GetRaidBoss_RankChangeRecordUis(ui)
  local uis = {}
  
  uis.RecordTxt = ui:GetChild("RecordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_RankChangeWindowByName.lua.lua
**Functions:**
- GetRaidBoss_RankChangeWindowUis
**Requires:**
- RaidBoss_RankChangeByName
**Snippet:**
```lua
require("RaidBoss_RankChangeByName")

function GetRaidBoss_RankChangeWindowUis(ui)
  local uis = {}
  uis.Main = GetRaidBoss_RankChangeUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_RankRewardNumberByName.lua.lua
**Functions:**
- GetRaidBoss_RankRewardNumberUis
**Snippet:**
```lua
function GetRaidBoss_RankRewardNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_RankRewardTab1BtnByName.lua.lua
**Functions:**
- GetRaidBoss_RankRewardTab1BtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetRaidBoss_RankRewardTab1BtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_RankRewardTab2BtnByName.lua.lua
**Functions:**
- GetRaidBoss_RankRewardTab2BtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetRaidBoss_RankRewardTab2BtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_RankRewardTipsAniByName.lua.lua
**Functions:**
- GetRaidBoss_RankRewardTipsAniUis
**Requires:**
- RaidBoss_RankRewardTipsByName
**Snippet:**
```lua
require("RaidBoss_RankRewardTipsByName")

function GetRaidBoss_RankRewardTipsAniUis(ui)
  local uis = {}
  uis.RankRewardTips = GetRaidBoss_RankRewardTipsUis(ui:GetChild("RankRewardTips"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_RankRewardTipsByName.lua.lua
**Functions:**
- GetRaidBoss_RankRewardTipsUis
**Requires:**
- RaidBoss_RankRewardNumberByName
**Snippet:**
```lua
require("RaidBoss_RankRewardNumberByName")

function GetRaidBoss_RankRewardTipsUis(ui)
  local uis = {}
  uis.RankRewardNumber = GetRaidBoss_RankRewardNumberUis(ui:GetChild("RankRewardNumber"))
  uis.RewardList = ui:GetChild("RewardList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_RankRewardTipsListByName.lua.lua
**Functions:**
- GetRaidBoss_RankRewardTipsListUis
**Snippet:**
```lua
function GetRaidBoss_RankRewardTipsListUis(ui)
  local uis = {}
  
  uis.RewardTipsList = ui:GetChild("RewardTipsList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_RewardBtnByName.lua.lua
**Functions:**
- GetRaidBoss_RewardBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetRaidBoss_RewardBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_RewardItemByName.lua.lua
**Functions:**
- GetRaidBoss_RewardItemUis
**Snippet:**
```lua
function GetRaidBoss_RewardItemUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_RewardShowByName.lua.lua
**Functions:**
- GetRaidBoss_RewardShowUis
**Requires:**
- CommonResource_PopupBgByName
- RaidBoss_RewardTitleByName
- RaidBoss_DifficultyRewardTipsListByName
- RaidBoss_RankRewardTipsListByName
- RaidBoss_NowRankByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("RaidBoss_RewardTitleByName")
require("RaidBoss_DifficultyRewardTipsListByName")
require("RaidBoss_RankRewardTipsListByName")
require("RaidBoss_NowRankByName")

function GetRaidBoss_RewardShowUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.RewardTitle = GetRaidBoss_RewardTitleUis(ui:GetChild("RewardTitle"))
```

---

## Rouge/RaidBoss_RewardShowWindowByName.lua.lua
**Functions:**
- GetRaidBoss_RewardShowWindowUis
**Requires:**
- RaidBoss_RewardShowByName
**Snippet:**
```lua
require("RaidBoss_RewardShowByName")

function GetRaidBoss_RewardShowWindowUis(ui)
  local uis = {}
  uis.Main = GetRaidBoss_RewardShowUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_RewardTitleByName.lua.lua
**Functions:**
- GetRaidBoss_RewardTitleUis
**Snippet:**
```lua
function GetRaidBoss_RewardTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_RightArrowBtnByName.lua.lua
**Functions:**
- GetRaidBoss_RightArrowBtnUis
**Snippet:**
```lua
function GetRaidBoss_RightArrowBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RaidBoss_TestBattleBtnByName.lua.lua
**Functions:**
- GetRaidBoss_TestBattleBtnUis
**Snippet:**
```lua
function GetRaidBoss_TestBattleBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RandomTipsWindow.lua.lua
**Functions:**
- RandomTipsWindow.ReInitData
- RandomTipsWindow.OnInit
- RandomTipsWindow.UpdateInfo
- story_reader.getOptionDes
- story_reader.getOptionNext
- RandomTipsWindow.InitBtn
- RandomTipsWindow.OnShown
- RandomTipsWindow.OnClose
**Requires:**
- Abyss_RandomTipsWindowByName
**Snippet:**
```lua
require("Abyss_RandomTipsWindowByName")
local RandomTipsWindow = {}
local uis, contentPane, storyId, eventInfo, callback

function RandomTipsWindow.ReInitData()
end

function RandomTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RandomTipsWindow.package, WinResConfig.RandomTipsWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/RangeUtil.lua.lua
**Functions:**
- RangeUtil.CurveRange
- RangeUtil.CircleRange
- RangeUtil.SquareRange
- RangeUtil.TriangleRange
**Snippet:**
```lua
local RangeUtil = {}

function RangeUtil.CurveRange()
end

function RangeUtil.CircleRange()
end

function RangeUtil.SquareRange()
end
```

---

## Rouge/RankingList_Rank1ByName.lua.lua
**Functions:**
- GetRankingList_Rank1Uis
**Requires:**
- RankingList_RankNumberByName
- CommonResource_HeadByName
**Snippet:**
```lua
require("RankingList_RankNumberByName")
require("CommonResource_HeadByName")

function GetRankingList_Rank1Uis(ui)
  local uis = {}
  uis.Number = GetRankingList_RankNumberUis(ui:GetChild("Number"))
  uis.Head = GetCommonResource_HeadUis(ui:GetChild("Head"))
  uis.GulidIconLoader = ui:GetChild("GulidIconLoader")
  uis.typeCtr = ui:GetController("type")
  uis.root = ui
```

---

## Rouge/RankingList_Rank2ByName.lua.lua
**Functions:**
- GetRankingList_Rank2Uis
**Requires:**
- RankingList_RankNumberByName
- CommonResource_HeadByName
**Snippet:**
```lua
require("RankingList_RankNumberByName")
require("CommonResource_HeadByName")

function GetRankingList_Rank2Uis(ui)
  local uis = {}
  uis.Number = GetRankingList_RankNumberUis(ui:GetChild("Number"))
  uis.Head = GetCommonResource_HeadUis(ui:GetChild("Head"))
  uis.GulidIconLoader = ui:GetChild("GulidIconLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.typeCtr = ui:GetController("type")
```

---

## Rouge/RankingList_Rank3ByName.lua.lua
**Functions:**
- GetRankingList_Rank3Uis
**Requires:**
- RankingList_RankNumberByName
- CommonResource_HeadByName
**Snippet:**
```lua
require("RankingList_RankNumberByName")
require("CommonResource_HeadByName")

function GetRankingList_Rank3Uis(ui)
  local uis = {}
  uis.Number = GetRankingList_RankNumberUis(ui:GetChild("Number"))
  uis.Head = GetCommonResource_HeadUis(ui:GetChild("Head"))
  uis.GulidIconLoader = ui:GetChild("GulidIconLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.typeCtr = ui:GetController("type")
```

---

## Rouge/RankingList_RankEmptyByName.lua.lua
**Functions:**
- GetRankingList_RankEmptyUis
**Snippet:**
```lua
function GetRankingList_RankEmptyUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RankingList_RankInfo1ByName.lua.lua
**Functions:**
- GetRankingList_RankInfo1Uis
**Snippet:**
```lua
function GetRankingList_RankInfo1Uis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RankingList_RankInfoByName.lua.lua
**Functions:**
- GetRankingList_RankInfoUis
**Requires:**
- RankingList_RankInfo1ByName
**Snippet:**
```lua
require("RankingList_RankInfo1ByName")

function GetRankingList_RankInfoUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Info1 = GetRankingList_RankInfo1Uis(ui:GetChild("Info1"))
  uis.GoBtn = ui:GetChild("GoBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Rouge/RankingList_RankInfoGoBtnByName.lua.lua
**Functions:**
- GetRankingList_RankInfoGoBtnUis
**Snippet:**
```lua
function GetRankingList_RankInfoGoBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RankingList_RankingByName.lua.lua
**Functions:**
- GetRankingList_RankingUis
**Requires:**
- CommonResource_PopupBgByName
- RankingList_RankEmptyByName
- RankingList_RankListByName
- RankingList_RankInfoByName
- RankingList_RankRegionByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("RankingList_RankEmptyByName")
require("RankingList_RankListByName")
require("RankingList_RankInfoByName")
require("RankingList_RankRegionByName")

function GetRankingList_RankingUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TabList = ui:GetChild("TabList")
```

---

## Rouge/RankingList_RankingWindowByName.lua.lua
**Functions:**
- GetRankingList_RankingWindowUis
**Requires:**
- RankingList_RankingByName
**Snippet:**
```lua
require("RankingList_RankingByName")

function GetRankingList_RankingWindowUis(ui)
  local uis = {}
  uis.Main = GetRankingList_RankingUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RankingList_RankListByName.lua.lua
**Functions:**
- GetRankingList_RankListUis
**Snippet:**
```lua
function GetRankingList_RankListUis(ui)
  local uis = {}
  
  uis.RankList = ui:GetChild("RankList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RankingList_RankNumberByName.lua.lua
**Functions:**
- GetRankingList_RankNumberUis
**Snippet:**
```lua
function GetRankingList_RankNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Rouge/RankingList_RankRegionByName.lua.lua
**Functions:**
- GetRankingList_RankRegionUis
**Requires:**
- RankingList_Rank1ByName
- RankingList_Rank2ByName
- RankingList_Rank3ByName
**Snippet:**
```lua
require("RankingList_Rank1ByName")
require("RankingList_Rank2ByName")
require("RankingList_Rank3ByName")

function GetRankingList_RankRegionUis(ui)
  local uis = {}
  uis.Rank1 = GetRankingList_Rank1Uis(ui:GetChild("Rank1"))
  uis.Rank2 = GetRankingList_Rank2Uis(ui:GetChild("Rank2"))
  uis.Rank3 = GetRankingList_Rank3Uis(ui:GetChild("Rank3"))
  uis.root = ui
```

---

## Rouge/RankingList_RankTipsAniByName.lua.lua
**Functions:**
- GetRankingList_RankTipsAniUis
**Requires:**
- RankingList_RankTipsByName
**Snippet:**
```lua
require("RankingList_RankTipsByName")

function GetRankingList_RankTipsAniUis(ui)
  local uis = {}
  uis.PlayerRankTips = GetRankingList_RankTipsUis(ui:GetChild("PlayerRankTips"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RankingList_RankTipsByName.lua.lua
**Functions:**
- GetRankingList_RankTipsUis
**Requires:**
- RankingList_RankNumberByName
- CommonResource_HeadByName
**Snippet:**
```lua
require("RankingList_RankNumberByName")
require("CommonResource_HeadByName")

function GetRankingList_RankTipsUis(ui)
  local uis = {}
  uis.Number = GetRankingList_RankNumberUis(ui:GetChild("Number"))
  uis.Head = GetCommonResource_HeadUis(ui:GetChild("Head"))
  uis.GulidIconLoader = ui:GetChild("GulidIconLoader")
  uis.Name1Txt = ui:GetChild("Name1Txt")
  uis.NameTxt = ui:GetChild("NameTxt")
```

---

## Rouge/RankingList_TabBtnByName.lua.lua
**Functions:**
- GetRankingList_TabBtnUis
**Snippet:**
```lua
function GetRankingList_TabBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RankingWindow.lua.lua
**Functions:**
- RankingWindow.ReInitData
- RankingWindow.OnInit
- RankingWindow.UpdateInfo
- list.itemRenderer
- RankingWindow.InitBtn
- RankingWindow.OnClose
**Requires:**
- RankingList_RankingWindowByName
**Snippet:**
```lua
require("RankingList_RankingWindowByName")
ld("Ranklist")
local RankingWindow = {}
local uis, contentPane, playAnim, selectedIndex, lastSelectedIndex, TAB_LIST
local TAB_INDEX = {
  MAIN_LINE = 1,
  TOWER = 2,
  PVP = 3,
  BOSS = 4,
  GUILDWAR = 5
```

---

## Rouge/RanklistData.lua.lua
**Snippet:**
```lua
local rankInfoLookup, guildWarRankInfo
local SetRankInfo = function(data)
  rankInfoLookup = rankInfoLookup or {}
  local sceneType = data.sceneType
  local exits = rankInfoLookup[sceneType] or data
  local index = data.startIndex
  local rankList = data.members
  for i = 1, #rankList do
    exits.members[i + index] = rankList[i]
  end
```

---

## Rouge/RanklistMgr.lua.lua
**Snippet:**
```lua
local indexesBufferLookup
local RequireRankInfo = function(r_type, startIndex, rspCallback)
  indexesBufferLookup = indexesBufferLookup or {}
  indexesBufferLookup[r_type] = indexesBufferLookup[r_type] or {}
  local indexesBuffer = indexesBufferLookup[r_type]
  local length = 10
  for i, v in ipairs(indexesBuffer) do
    if v <= startIndex and startIndex < v + length then
      return
    end
```

---

## Rouge/RanklistScriptList.lua.lua
**Requires:**
- RanklistData
- RanklistService
- RanklistMgr
**Snippet:**
```lua
RanklistData = require("RanklistData")
RanklistService = require("RanklistService")
RanklistMgr = require("RanklistMgr")
```

---

## Rouge/RanklistService.lua.lua
**Snippet:**
```lua
local GetRankInfoReq = function(r_type, index, rspCallback)
  Net.Send(Proto.MsgName.GetSceneRankReq, {sceneType = r_type, startIndex = index}, rspCallback)
end
local GetGuildRankInfoReq = function(rspCallback)
  Net.Send(Proto.MsgName.GetGuildWarRankExtReq, nil, rspCallback)
end
local GetRankInfoRsp = function(msg)
  RanklistData.SetRankInfo(msg)
end
local GetGuildRankInfoRsp = function(msg)
```

---

## Rouge/RecommendScreenWindow.lua.lua
**Functions:**
- RecommendScreenWindow.ReInitData
- RecommendScreenWindow.OnInit
- RecommendScreenWindow.UpdateInfo
- RecommendScreenWindow.InitBtn
- RecommendScreenWindow.OnClose
**Requires:**
- GuildBoss_RecommendScreenWindowByName
**Snippet:**
```lua
require("GuildBoss_RecommendScreenWindowByName")
local RecommendScreenWindow = {}
local uis, contentPane, filterCardIdList

function RecommendScreenWindow.ReInitData()
end

function RecommendScreenWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RecommendScreenWindow.package, WinResConfig.RecommendScreenWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/Rectangle.lua.lua
**Functions:**
- Rectangle:__ctor
**Snippet:**
```lua
local base = Polygon
local Rectangle = Create("Rectangle", base)

function Rectangle:__ctor()
  self.shapeType = ShapeType.Poly
  self.mass = 0
  self.inertia = 0
end

return Rectangle
```

---

## Rouge/RedDotData.lua.lua
**Functions:**
- RedDotData.Init
- RedDotData.Clear
- RedDotData.AddNode
- RedDotData.UpdateNode
- RedDotData.UpdateNodeByWindowName
- RedDotData.RemoveNode
- RedDotData.RemoveOneNode
- RedDotData.CreateOneNode
- redDotNode:Init
- redDotNode:Update
- redDotNode:UpdateVisible
**Snippet:**
```lua
RedDotData = {}
RED_DOT_DATA_TYPE = {
  CARD = 1,
  BADGE = 2,
  TASK = 3,
  PASSPORT = 4,
  GACHA = 5,
  MAIL = 6,
  NOTICE = 7,
  BIOGRAHY = 8,
```

---

## Rouge/RedDotMgr.lua.lua
**Functions:**
- RedDotMgr.Init
- RedDotMgr.Clear
- RedDotMgr.AddNode
- RedDotMgr.UpdateNode
- RedDotMgr.UpdateNodeByWindowName
- RedDotMgr.RemoveNode
- RedDotMgr.RemoveOneNode
- RedDotMgr.SetRedVisible
**Snippet:**
```lua
RedDotMgr = {}

function RedDotMgr.Init()
end

function RedDotMgr.Clear()
end

function RedDotMgr.AddNode(param)
  RedDotData.AddNode(param)
```

---

## Rouge/RedDotScriptList.lua.lua
**Requires:**
- RedDot_Card
- RedDot_Gacha
- RedDot_Passport
- RedDot_Task
- RedDot_Mail
- RedDot_Notice
- RedDot_Abyss
- RedDot_Exped
- RedDot_Story
- RedDot_Guild
- RedDot_Shop
- RedDot_Sgin
- RedDot_Chat
- RedDot_Friend
- RedDot_Arena
- RedDot_PlotDungeon
- RedDot_Badge
- RedDot_RaidBoss
- RedDot_Tower
- RedDot_FrostDungeon
- RedDot_Rogue
- RedDot_ActivityDungeon
- RedDot_GuildWar
- RedDot_ExploreAFK
- RedDot_Seal
- RedDot_TimeLimitedTower
- RedDot_Schedule
- RedDot_Watch
- RedDot_ExploreDungeon
- RedDot_PlayerReturn
- RedDotMgr
- RedDotData
**Snippet:**
```lua
local require = require
require("RedDot_Card")
require("RedDot_Gacha")
require("RedDot_Passport")
require("RedDot_Task")
require("RedDot_Mail")
require("RedDot_Notice")
require("RedDot_Abyss")
require("RedDot_Exped")
require("RedDot_Story")
```

---

## Rouge/RedDot_Abyss.lua.lua
**Functions:**
- RedDotAbyss.Init
- RedDotAbyss.SaveInspectedGrid
- RedDotAbyss.SaveInspectedGrids
- RedDotAbyss.Inspected
- RedDotAbyss.HasNewGoods
- RedDotAbyss.HasNewGoodsWithShopType
- RedDotAbyss.HasNewTreasures
- RedDotAbyss.HasNewTreasuresWithRegionId
- RedDotAbyss.SaveInspectedTreasure
- RedDotAbyss.BossChallengeIsNew
- RedDotAbyss.ExpeditionIsNew
- RedDotAbyss.BuildingIsNew
- RedDotAbyss.RoguelikeIsNew
- RedDotAbyss.FrostDungeonIsNew
- RedDotAbyss.ExploreAFKIsNew
- RedDotAbyss.ExploreDungeonIsNew
- RedDotAbyss.HasNewFunction
- RedDotAbyss.TideDungeonHasAnyRewardsByType
- RedDotAbyss.TideDungeonHasAnyRewards
**Snippet:**
```lua
RedDotAbyss = {}
local inspectedGrids, inspectedTreasures

function RedDotAbyss.Init()
  local str = PlayerPrefsUtil.GetString(PLAYER_PREF_ENUM.ABYSS_SHOP_INSPECTED_ITEMS, "")
  if string.isEmptyOrNil(str) then
    inspectedGrids = {}
  else
    inspectedGrids = Json.decode(str)
  end
```

---

## Rouge/RedDot_ActivityDungeon.lua.lua
**Functions:**
- RedDotActivityDungeon.CanShowHome
- RedDotActivityDungeon.CanTask
- RedDotActivityDungeon.CanSgin
- RedDotActivityDungeon.CanHomePass
- RedDotActivityDungeon.CanReward
- RedDotActivityDungeon.DailyTaskComplete
- RedDotActivityDungeon.CanMaterialRed
- RedDotActivityDungeon.CanDailyNew
- RedDotActivityDungeon.CanBossNew
- RedDotActivityDungeon.MiniGame1_TaskRewardable
- RedDotActivityDungeon.MiniGame1_DailyTaskRewardable
- RedDotActivityDungeon.MiniGame2_TaskRewardable
- RedDotActivityDungeon.MiniGame2_DailyTaskRewardable
- RedDotActivityDungeon.MiniGame3_TaskRewardable
- RedDotActivityDungeon.MiniGame3_DailyTaskRewardable
- RedDotActivityDungeon.MiniGame4_TaskRewardable
- RedDotActivityDungeon.MiniGame4_DailyTaskRewardable
- RedDotActivityDungeon.MiniGame5_FishTaskRewardable
- RedDotActivityDungeon.MiniGame5_FishDailyTaskRewardable
- RedDotActivityDungeon.MiniGame5_FishBookRewardable
- RedDotActivityDungeon.MiniGame5_TaskRewardable
- RedDotActivityDungeon.MiniGame5_DailyTaskRewardable
- RedDotActivityDungeon.MiniGame6_TaskRewardable
- RedDotActivityDungeon.MiniGame6_DailyTaskRewardable
- RedDotActivityDungeon.MiniGame10_TaskRewardable
- RedDotActivityDungeon.MiniGame10_DailyTaskRewardable
- RedDotActivityDungeon.MiniGame7_TaskRewardable
- RedDotActivityDungeon.MiniGame7_DailyTaskRewardable
- RedDotActivityDungeon.MiniGame8_TaskRewardable
- RedDotActivityDungeon.MiniGame8_DailyTaskRewardable
- RedDotActivityDungeon.MiniGame9_TaskRewardable
- RedDotActivityDungeon.MiniGame9_DailyTaskRewardable
- RedDotActivityDungeon.MiniGame11_TaskRewardable
- RedDotActivityDungeon.MiniGame11_DailyTaskRewardable
- RedDotActivityDungeon.MiniGame12_TaskRewardable
- RedDotActivityDungeon.MiniGame12_DailyTaskRewardable
- RedDotActivityDungeon.MiniGame13_TaskRewardable
- RedDotActivityDungeon.MiniGame13_DailyTaskRewardable
- RedDotActivityDungeon.MiniGame14_TaskRewardable
- RedDotActivityDungeon.MiniGame14_DailyTaskRewardable
- RedDotActivityDungeon.MiniGame15_TaskRewardable
- RedDotActivityDungeon.MiniGame15_DailyTaskRewardable
- RedDotActivityDungeon.MiniGame16_TaskRewardable
- RedDotActivityDungeon.MiniGame16_DailyTaskRewardable
- RedDotActivityDungeon.MiniGame17_DailyTaskRewardable
- RedDotActivityDungeon.MiniGame17_TaskRewardable
- RedDotActivityDungeon.MiniGame18_TaskRewardable
- RedDotActivityDungeon.MiniGame18_DailyTaskRewardable
- RedDotActivityDungeon.MiniGame19_TaskRewardable
- RedDotActivityDungeon.MiniGame19_DailyTaskRewardable
- RedDotActivityDungeon.MiniGame20_TaskRewardable
- RedDotActivityDungeon.MiniGame20_DailyTaskRewardable
- RedDotActivityDungeon.MiniGame21_TaskRewardable
- RedDotActivityDungeon.MiniGame21_DailyTaskRewardable
- RedDotActivityDungeon.MiniGame22_TaskRewardable
- RedDotActivityDungeon.MiniGame22_DailyTaskRewardable
**Snippet:**
```lua
RedDotActivityDungeon = {}

function RedDotActivityDungeon.CanShowHome(showId)
  return RedDotActivityDungeon.CanMaterialRed(showId) or RedDotActivityDungeon.CanHomePass(showId) or RedDotActivityDungeon.CanTask(showId) or RedDotActivityDungeon.CanSgin(showId)
end

function RedDotActivityDungeon.CanTask(showId)
  if ActivityDungeonData then
    local activityInfo = ActivityDungeonData.GetActivityInfo(showId)
    if activityInfo then
```

---

## Rouge/RedDot_Arena.lua.lua
**Functions:**
- RedDotArena.ShowHome
- RedDotArena.ShowArenaDefense
- RedDotArena.ArenaDefenseEnterNew
- RedDotArena.ArenaDefenseMapNew
- RedDotArena.ArenaDefenseBuildingNew
- RedDotArena.ArenaOneMapNew
- RedDotArena.ArenaOneBuildingNew
**Snippet:**
```lua
RedDotArena = {}

function RedDotArena.ShowHome()
  if ArenaData.Info and ArenaData.Info.highRank and ArenaData.Info.rewardPhase and EnterClampUtil.WhetherToEnter(FEATURE_ENUM.ADVENTURE_ARENA, false) then
    local config = TableData.GetTable("BaseArenaRankReward")
    for i, v in pairs(config) do
      if v.phase == ArenaData.Info.rewardPhase and ArenaData.Info.highRank <= v.rank_low and not table.contain(ArenaData.Info.rewardList, v.id) then
        return true
      end
    end
```

---

## Rouge/RedDot_Badge.lua.lua
**Functions:**
- RedDotBadge.CanShowHome
- RedDotBadge.CanCardRanRankWear
- RedDotBadge.CanCardWear
**Snippet:**
```lua
RedDotBadge = {}

function RedDotBadge.CanShowHome()
  if not EnterClampUtil.WhetherToEnter(FEATURE_ENUM.HOME_BADGE, false) then
    return false
  end
  local allCard = ActorData.GetCardList()
  for i, v in pairs(allCard) do
    if RedDotBadge.CanCardRanRankWear(v.cardId) then
      return true
```

---

## Rouge/RedDot_Card.lua.lua
**Functions:**
- RedDotCard.InitItemList
- RedDotCard.GetAllItemExp
- RedDotCard.CanAnyCardGrowUp
- RedDotCard.CanGrowUp
- RedDotCard.CanCardListStarUp
- RedDotCard.CannCardListGrowUp
- RedDotCard.CanCardNew
- RedDotCard.CanCardUp
- RedDotCard.CanLevelUp
- RedDotCard.CanBreachUp
- RedDotCard.CanStarUp
- RedDotCard.CanSkillUp
- RedDotCard.CanClothes
- RedDotCard.CanPlot
- RedDotCard.CanStory
- RedDotCard.CanVoice
**Snippet:**
```lua
RedDotCard = {}
local cardLevelUpItemList

function RedDotCard.InitItemList()
  if nil == cardLevelUpItemList then
    local fixedData = TableData.GetConfig(70010006, "BaseFixed")
    cardLevelUpItemList = Split(fixedData.array_value, "|")
    for i, v in ipairs(cardLevelUpItemList) do
      cardLevelUpItemList[i] = tonumber(v)
    end
```

---

## Rouge/RedDot_Chat.lua.lua
**Functions:**
- RedDotChat.HaveUnreadUnionMsg
- RedDotChat.HaveUnreadPrivateMsg
- RedDotChat.IsUnreadPrivateTarget
**Snippet:**
```lua
RedDotChat = {}

function RedDotChat.HaveUnreadUnionMsg()
  if EnterClampUtil.WhetherToEnter(FEATURE_ENUM.HOME_GUILD, false) == false then
    return false
  end
  if false == EnterClampUtil.WhetherToEnter(FEATURE_ENUM.HOME_CHAT, false) then
    return false
  end
  ld("Chat")
```

---

## Rouge/RedDot_Exped.lua.lua
**Functions:**
- RedDotExped.Init
- RedDotExped.HasAnyRewards
**Snippet:**
```lua
RedDotExped = {}

function RedDotExped.Init()
end

function RedDotExped.HasAnyRewards()
  local expedData = ExpeditionData.GetData()
  local gotRewards = ExpeditionData.GetRewardsInfo()
  local numStars = expedData.highPassStar or 0
  local rewardTbl = TableData.GetTable("BaseExpeditionReward")
```

---

## Rouge/RedDot_ExploreAFK.lua.lua
**Snippet:**
```lua
RedDotExploreAFK = {}
local HasAnyFinishedDispatch = function()
  if not ExploreAFKData then
    return
  end
  local allGroupsInfo = ExploreAFKData.GetAllGroupsInfo()
  if allGroupsInfo then
    local timestamp = LoginData.GetCurServerTime()
    for _, groupInfo in ipairs(allGroupsInfo) do
      if timestamp >= groupInfo.overStamp then
```

---

## Rouge/RedDot_ExploreDungeon.lua.lua
**Snippet:**
```lua
RedDotExploreDungeon = {}
local Collectable = function()
  if not ExploreDungeonData then
    return
  end
  local info = ExploreDungeonData.GetPlayerInfo()
  local duration = LoginData.GetCurServerTime() - info.produceStartTime
  local interval = TableData.GetConfig(70011701, "BaseFixed").int_value
  return duration > interval
end
```

---

## Rouge/RedDot_Friend.lua.lua
**Functions:**
- RedDotFriend.HaveAddFriendSeat
- RedDotFriend.HaveAddFriendRequest
**Snippet:**
```lua
RedDotFriend = {}

function RedDotFriend.HaveAddFriendSeat()
  local list = FriendData.GetRelationList(ProtoEnum.RELATION_STATE.FRIEND)
  return #list < FriendData.GetFriendMaxNumber()
end

function RedDotFriend.HaveAddFriendRequest()
  local list = FriendData.GetRelationList(ProtoEnum.RELATION_STATE.APPLIED)
  return #list > 0
```

---

## Rouge/RedDot_FrostDungeon.lua.lua
**Snippet:**
```lua
RedDotFrostDungeon = {}
local HasAnyRewardsByStageId = function(stageId)
  local challenges = FrostDungeonData.GetLevelChallenges(stageId)
  if challenges then
    for i, v in pairs(challenges) do
      if v.state == ProtoEnum.CHALLENGE_STAT_TYPE.CST_FINISH then
        return true
      end
    end
  end
```

---

## Rouge/RedDot_Gacha.lua.lua
**Functions:**
- RedDotGacha.ShowHome
- RedDotGacha.CanFreeCoupon
**Snippet:**
```lua
RedDotGacha = {}

function RedDotGacha.ShowHome()
  if LotteryData and LotteryData.Info and LotteryData.Info.openList then
    for i, v in pairs(LotteryData.Info.openList) do
      local data = TableData.GetConfig(i, "BaseGacha")
      if data and RedDotGacha.CanFreeCoupon(data) then
        return true
      end
    end
```

---

## Rouge/RedDot_Guild.lua.lua
**Functions:**
- RedDotGuild.HomeTaskRed
- RedDotGuild.CanAuditJoin
- RedDotGuild.CanSign
- RedDotGuild.CanVote
**Snippet:**
```lua
RedDotGuild = {}

function RedDotGuild.HomeTaskRed()
  return RedDotGuild.CanSign() or RedDotGuild.CanVote() or RedDotGuild.CanAuditJoin()
end

function RedDotGuild.CanAuditJoin()
  if GuildData.GuildInfo and GuildData.GuildInfo.applicants and #GuildData.GuildInfo.applicants > 0 then
    local itemData = GuildData.GetGuildItemData(ActorData.GetUin())
    if itemData and (itemData.roleType == ProtoEnum.GUILD_ROLE_TYPE.GRT_LEADER or itemData.roleType == ProtoEnum.GUILD_ROLE_TYPE.GRT_VICE_LEADER) then
```

---

## Rouge/RedDot_GuildWar.lua.lua
**Functions:**
- RedDotGuildWar.CanShowHome
- RedDotGuildWar.CanTask
**Snippet:**
```lua
RedDotGuildWar = {}
local TodayHasFightCount = function()
  ld("GuildWar")
  local scheduleInfo = GuildWarData.GetGuildScheduleInfo()
  if scheduleInfo and scheduleInfo.state == ProtoEnum.GuildWarState.GWS_FIGHT then
    local lastTimestamp = PlayerPrefsUtil.GetFloat(PLAYER_PREF_ENUM.GUILD_WAR_TODAY_HAS_FIGHT_COUNT, 0)
    local timestamp = LoginData.GetCurServerTime()
    local day, lastDay = math.floor(timestamp / 86400), math.floor(lastTimestamp / 86400)
    if day > lastDay then
      local playerInfo = GuildWarData.GetGuildPlayerInfo()
```

---

## Rouge/RedDot_Mail.lua.lua
**Functions:**
- RedDot_Mail.ShowHome
- RedDot_Mail.CanGetItem
**Snippet:**
```lua
RedDot_Mail = {}

function RedDot_Mail.ShowHome()
  return RedDot_Mail.CanGetItem()
end

function RedDot_Mail.CanGetItem()
  if MailData.mails then
    local time = LoginData.GetCurServerTime()
    for i, v in pairs(MailData.mails) do
```

---

## Rouge/RedDot_Notice.lua.lua
**Functions:**
- RedDot_Notice.ShowHome
- RedDot_Notice.UnreadByType
- RedDot_Notice.Unread
**Snippet:**
```lua
RedDot_Notice = {}

function RedDot_Notice.ShowHome()
  return RedDot_Notice.Unread()
end

function RedDot_Notice.UnreadByType(notice)
  if notice then
    for i, v in pairs(notice) do
      if NoticeData.NewIsShow(v.uid) then
```

---

## Rouge/RedDot_Passport.lua.lua
**Functions:**
- RedDotPassport.ShowHome
- RedDotPassport.DailyTaskComplete
- RedDotPassport.WeeklyTaskComplete
- RedDotPassport.TotalTaskComplete
- RedDotPassport.TaskComplete
- RedDotPassport.CanReward
- RedDotPassport.CanTask
**Snippet:**
```lua
RedDotPassport = {}

function RedDotPassport.ShowHome()
  if PassportData and PassportData.infoArr and #PassportData.infoArr > 0 then
    for _, v in pairs(PassportData.GetAllPassport()) do
      if RedDotPassport.CanTask(v.passPortId) or RedDotPassport.CanReward(v.passPortId) then
        return true
      end
    end
  end
```

---

## Rouge/RedDot_PlayerReturn.lua.lua
**Functions:**
- RedDotPlayerReturn.HasMultiDroppedCount
- RedDotPlayerReturn.HasAnyLoginReward
- RedDotPlayerReturn.HasAnySignReward
- RedDotPlayerReturn.HasAnyTaskReward
**Snippet:**
```lua
RedDotPlayerReturn = {}
local HasMultiDroppedCount = function()
  local activInfo = ActivityReturnData.GetActivityInfo()
  if not activInfo then
    return
  end
  local entries = ActivityReturnMgr.GetMultiDroppedEntries()
  local multiDrops = activInfo.dailyDrop
  if multiDrops then
    for i, v in ipairs(entries) do
```

---

## Rouge/RedDot_PlotDungeon.lua.lua
**Functions:**
- RedDotPlotDungeon.ShowHome
**Snippet:**
```lua
RedDotPlotDungeon = {}

function RedDotPlotDungeon.ShowHome()
  if AdventureData then
    local screenInfo = AdventureData.GetSceneData(ProtoEnum.SCENE_TYPE.MAIN_LINE)
    if screenInfo then
      local nextChapterId = AdventureMgr.GetNextRewardedChapter(screenInfo.rewardedChapter)
      nextChapterId = nextChapterId >= screenInfo.currentChapter and screenInfo.currentChapter or nextChapterId
      local data = TableData.GetConfig(nextChapterId, "BaseChapter")
      if nextChapterId > screenInfo.rewardedChapter and (data.chapter_reward_stage < screenInfo.currentStage or 0 == screenInfo.currentStage) then
```

---

## Rouge/RedDot_RaidBoss.lua.lua
**Functions:**
- RedDotRaidBoss.TodayHasChallengeCount
- RedDotRaidBoss.IsNewSeason
- RedDotRaidBoss.IsNearlyDeadline
- RedDotRaidBoss.HasAnyRewards
**Snippet:**
```lua
RedDotRaidBoss = {}

function RedDotRaidBoss.TodayHasChallengeCount()
  if not RaidBossMgr.IsInProgress() then
    return false
  end
  local serverTimestamp = LoginData.GetCurServerTime()
  local content = TimeUtil.FormatDate("%Y_%m_%d", serverTimestamp)
  local value = PlayerPrefsUtil.GetString(PLAYER_PREF_ENUM.RAID_BOSS_HAS_CHALLENGE_COUNT, "")
  if content == value then
```

---

## Rouge/RedDot_Rogue.lua.lua
**Snippet:**
```lua
RedDotRogue = {}
local HasNesTreasure = function()
  local themeInfo = RogueGameData.GetThemeInfo()
  local startTimestamp = themeInfo.startTime
  local themeId = themeInfo.themeId
  local jsonStr = PlayerPrefsUtil.GetString(PLAYER_PREF_ENUM.ROGUE_GAME_TREASURE, "", themeId)
  local o
  if not string.isEmptyOrNil(jsonStr) then
    o = Json.decode(jsonStr)
  end
```

---

## Rouge/RedDot_Schedule.lua.lua
**Functions:**
- RedDotSchedule.ShowHome
- RedDotSchedule.ShowHomeNew
- RedDotSchedule.SaveOpen
- RedDotSchedule.CanItem
**Snippet:**
```lua
RedDotSchedule = {}

function RedDotSchedule.ShowHome()
  local stamp = PlayerPrefsUtil.GetInt(PLAYER_PREF_ENUM.SCHEDULE_DAY)
  if nil == stamp or 0 == stamp then
    PlayerPrefsUtil.SetInt(PLAYER_PREF_ENUM.SCHEDULE_DAY, LoginData.GetCurServerTime())
    return true
  end
  local teamStamp = ResetFiveStamp(stamp)
  local time = math.floor(LoginData.GetCurServerTime() - teamStamp)
```

---

## Rouge/RedDot_Seal.lua.lua
**Snippet:**
```lua
RedDotSeal = {}
local ATTR_ENUM = {
  ATK = 1,
  DEF = 2,
  HP = 3
}
local attributeBuffer = {}
local jobs = {
  1,
  2,
```

---

## Rouge/RedDot_Sgin.lua.lua
**Functions:**
- RedDotSign.HomeTaskRed
- RedDotSign.HomeReservationRed
- RedDotSign.HomeReturnGiftRed
- RedDotSign.TurnTableShowFree
- RedDotSign.HomeRoundActRed
- RedDotSign.CanHomeTurnTable
- RedDotSign.CanFreeBuy
- RedDotSign.CanFreeNum
**Snippet:**
```lua
RedDotSign = {}

function RedDotSign.HomeTaskRed(data)
  if data.type == SignTypeEnum.SIGN_IN_ACT then
    local reward = SignData.GetSignData(tonumber(data.parameter))
    local day = #reward or -1
    if SignData.activityData[data.id].isTodaySignIn == false and day > SignData.activityData[data.id].curDay and SignData.activityData[data.id].baseInfo.endStamp - LoginData.GetCurServerTime() > 0 then
      return true
    end
  elseif data.type == SignTypeEnum.SEARCH_ACT and false == SignData.activityData[data.id].isTodaySearch and SignData.activityData[data.id].baseInfo.endStamp - LoginData.GetCurServerTime() > 0 then
```

---

## Rouge/RedDot_Shop.lua.lua
**Functions:**
- RedDotShop.HomeTaskRed
- RedDotShop.CanFreeGift
- RedDotShop.CanFirstGift
- RedDotShop.CanAgreementGift
- RedDotShop.CanAgreementGiftBySeasonId
- RedDotShop.CanWeekShop
**Snippet:**
```lua
RedDotShop = {}

function RedDotShop.HomeTaskRed()
  return RedDotShop.CanFreeGift() or RedDotShop.CanFirstGift() or RedDotShop.CanAgreementGift()
end

function RedDotShop.CanFreeGift(bannerGroup)
  local data = TableData.GetTable("BaseGift")
  for i, v in pairs(data) do
    if (nil == bannerGroup or v.banner_group and v.banner_group == bannerGroup) and v.group_id and nil == v.not_show_red then
```

---

## Rouge/RedDot_Story.lua.lua
**Functions:**
- RedDotStory.HomeTaskRed
- RedDotStory.CGRedDotByTypeData
- RedDotStory.MusicShowByChapterId
- RedDotStory.MusicOneShowByChapterId
- RedDotStory.MusicRedDot
- RedDotStory.MonsterByCamp
- RedDotStory.MonsterOneLock
- RedDotStory.MonsterRedDot
- RedDotStory.ItemOneLock
- RedDotStory.ItemRedDot
- RedDotStory.GetStar
- RedDotStory.CanCradStarUp
- RedDotStory.CanCradBookReward
**Snippet:**
```lua
RedDotStory = {}

function RedDotStory.HomeTaskRed()
  return RedDotStory.ItemRedDot() or RedDotStory.CanCradBookReward() or RedDotStory.MonsterRedDot(TableData.GetTable("BaseStoryMonster")) or RedDotStory.MusicRedDot(TableData.GetTable("BaseSound")) or RedDotStory.CGRedDotByTypeData(TableData.GetTable("BaseStoryCg"))
end

function RedDotStory.CGRedDotByTypeData(data)
  for i, v in pairs(data) do
    if RedDotStory.MusicOneShowByChapterId(v.id) then
      return true
```

---

## Rouge/RedDot_Task.lua.lua
**Functions:**
- RedDotTask.HomeTaskRed
- RedDotTask.InitialCarnivalRed
- RedDotTask.CanCarnivalTask
- RedDotTask.CanCarnivalTarget
- RedDotTask.CanDayTask
- RedDotTask.InitialSignRed
- RedDotTask.CanInitialSign
- RedDotTask.DailyTaskRed
- RedDotTask.CanDailyTask
- RedDotTask.CanGrowTarget
- RedDotTask.CanDailyTarget
- RedDotTask.BiographyRed
- RedDotTask.CanBiographyTask
- RedDotTask.CanBiographyFlower
- RedDotTask.CanLvGift
- RedDotTask.HasAnySupplies
**Snippet:**
```lua
RedDotTask = {}

function RedDotTask.HomeTaskRed()
  return CarnivalData.SignIsShowHome() or CarnivalData.BiographyShowHome() or RedDotTask.InitialCarnivalRed() or RedDotTask.InitialSignRed() or RedDotTask.DailyTaskRed() or RedDotTask.BiographyRed() or RedDotTask.CanLvGift() or RedDotTask.HasAnySupplies()
end

function RedDotTask.InitialCarnivalRed()
  return RedDotTask.CanCarnivalTarget() or RedDotTask.CanCarnivalTask()
end

```

---

## Rouge/RedDot_TimeLimitedTower.lua.lua
**Functions:**
- RedDotTimeLimitedTower.IsNewSeason
- RedDotTimeLimitedTower.IsNearlyDeadline
- RedDotTimeLimitedTower.HasAnyFinishedTask
**Snippet:**
```lua
RedDotTimeLimitedTower = {}

function RedDotTimeLimitedTower.IsNewSeason()
  local timestamp = PlayerPrefsUtil.GetInt(PLAYER_PREF_ENUM.TIME_LIMITED_SEASON_RECORD, -1)
  local curStartTimestamp = TimeLimitedTowerData.GetStartTimestamp()
  if curStartTimestamp and curStartTimestamp ~= timestamp then
    return true
  end
end

```

---

## Rouge/RedDot_Tower.lua.lua
**Functions:**
- RedDotTower.ShowHome
**Snippet:**
```lua
RedDotTower = {}

function RedDotTower.ShowHome()
  if AdventureData then
    local screenInfo = AdventureData.GetSceneData(ProtoEnum.SCENE_TYPE.CLIMB_TOWER)
    if screenInfo then
      local nextChapterId = AdventureMgr.GetTowerNextChapterId(screenInfo.rewardedChapter)
      nextChapterId = nextChapterId >= screenInfo.currentChapter and screenInfo.currentChapter or nextChapterId
      local data = TableData.GetConfig(nextChapterId, "BaseChapter")
      if nextChapterId > screenInfo.rewardedChapter and (data.chapter_reward_stage < screenInfo.currentStage or 0 == screenInfo.currentStage) then
```

---

## Rouge/RedDot_Watch.lua.lua
**Functions:**
- RedDotWatch.ShowHome
**Snippet:**
```lua
RedDotWatch = {}

function RedDotWatch.ShowHome()
  local config = TableData.GetTable("BaseFashion")
  local tb = {}
  local newFashion = OprRecordUtil.GetRecord(PLAYER_OPERATION_ENUM.SPECIAL_FASHION_NEW)
  for i, v in pairs(config) do
    if 2 == v.skin_type and CardData.FashionIsContain(v.id) and not table.contain(newFashion, v.id) then
      return true
    end
```

---

## Rouge/RegressionSignWindow.lua.lua
**Functions:**
- RegressionSignWindow.ReInitData
- RegressionSignWindow.OnInit
- RegressionSignWindow.UpdateInfo
- list.itemRenderer
- RegressionSignWindow.ShowReward
- list.itemRenderer
- RegressionSignWindow.SetDayTips
- RegressionSignWindow.InitBtn
- RegressionSignWindow.CloseWindow
- RegressionSignWindow.OnClose
**Requires:**
- RegressionSign_SignWindowByName
**Snippet:**
```lua
require("RegressionSign_SignWindowByName")
local RegressionSignWindow = {}
local uis, contentPane, signData, data

function RegressionSignWindow.ReInitData()
end

function RegressionSignWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RegressionSignWindow.package, WinResConfig.RegressionSignWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/RegressionSign_ItemFrameByName.lua.lua
**Functions:**
- GetRegressionSign_ItemFrameUis
**Requires:**
- CommonResource_ItemCardPicByName
- CommonResource_ItemTimeByName
**Snippet:**
```lua
require("CommonResource_ItemCardPicByName")
require("CommonResource_ItemTimeByName")

function GetRegressionSign_ItemFrameUis(ui)
  local uis = {}
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.ItemCardPic = GetCommonResource_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.ItemTime = GetCommonResource_ItemTimeUis(ui:GetChild("ItemTime"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
```

---

## Rouge/RegressionSign_Module1ByName.lua.lua
**Functions:**
- GetRegressionSign_Module1Uis
**Snippet:**
```lua
function GetRegressionSign_Module1Uis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RegressionSign_Module1CloseBtnByName.lua.lua
**Functions:**
- GetRegressionSign_Module1CloseBtnUis
**Snippet:**
```lua
function GetRegressionSign_Module1CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RegressionSign_Module1InfoByName.lua.lua
**Functions:**
- GetRegressionSign_Module1InfoUis
**Requires:**
- RegressionSign_Mudule1ColorTipsByName
- RegressionSign_Mudule1GreenTipsByName
**Snippet:**
```lua
require("RegressionSign_Mudule1ColorTipsByName")
require("RegressionSign_Mudule1GreenTipsByName")

function GetRegressionSign_Module1InfoUis(ui)
  local uis = {}
  uis.ColorTips = GetRegressionSign_Mudule1ColorTipsUis(ui:GetChild("ColorTips"))
  uis.GreenTips = GetRegressionSign_Mudule1GreenTipsUis(ui:GetChild("GreenTips"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
```

---

## Rouge/RegressionSign_Mudule1ColorTipsByName.lua.lua
**Functions:**
- GetRegressionSign_Mudule1ColorTipsUis
**Snippet:**
```lua
function GetRegressionSign_Mudule1ColorTipsUis(ui)
  local uis = {}
  
  uis.NumberDecTxt = ui:GetChild("NumberDecTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RegressionSign_Mudule1GreenTipsByName.lua.lua
**Functions:**
- GetRegressionSign_Mudule1GreenTipsUis
**Snippet:**
```lua
function GetRegressionSign_Mudule1GreenTipsUis(ui)
  local uis = {}
  
  uis.NumberDecTxt = ui:GetChild("NumberDecTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RegressionSign_Sign1ByName.lua.lua
**Functions:**
- GetRegressionSign_Sign1Uis
**Requires:**
- RegressionSign_Module1ByName
**Snippet:**
```lua
require("RegressionSign_Module1ByName")

function GetRegressionSign_Sign1Uis(ui)
  local uis = {}
  uis.Pic1Loader = ui:GetChild("Pic1Loader")
  uis.Module1 = GetRegressionSign_Module1Uis(ui:GetChild("Module1"))
  uis.Close1Btn = ui:GetChild("Close1Btn")
  uis.root = ui
  return uis
end
```

---

## Rouge/RegressionSign_Sign2ByName.lua.lua
**Functions:**
- GetRegressionSign_Sign2Uis
**Requires:**
- CommonResource_PopupBgByName
- RegressionSign_Sign1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("RegressionSign_Sign1ByName")

function GetRegressionSign_Sign2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Sign1 = GetRegressionSign_Sign1Uis(ui:GetChild("Sign1"))
  uis.root = ui
  return uis
```

---

## Rouge/RegressionSign_SignWindowByName.lua.lua
**Functions:**
- GetRegressionSign_SignWindowUis
**Requires:**
- RegressionSign_Sign2ByName
**Snippet:**
```lua
require("RegressionSign_Sign2ByName")

function GetRegressionSign_SignWindowUis(ui)
  local uis = {}
  uis.Main = GetRegressionSign_Sign2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RenameWindow.lua.lua
**Functions:**
- RenameWindow.ReInitData
- RenameWindow.OnInit
- RenameWindow.UpdateInfo
- RenameWindow.UpdateCost
- RenameWindow.ClickClose
- RenameWindow.ClickSureBtn
- RenameWindow.InitBtn
- RenameWindow.OnShown
- RenameWindow.OnHide
- RenameWindow.OnClose
- RenameWindow.HandleMessage
**Requires:**
- Message_RenameWindowByName
**Snippet:**
```lua
require("Message_RenameWindowByName")
local RenameWindow = {}
local uis, contentPane, params
local costEnough = true

function RenameWindow.ReInitData()
end

function RenameWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RenameWindow.package, WinResConfig.RenameWindow.comName, function(com)
```

---

## Rouge/ResDownload_BackGroundByName.lua.lua
**Functions:**
- GetResDownload_BackGroundUis
**Snippet:**
```lua
function GetResDownload_BackGroundUis(ui)
  local uis = {}
  
  uis.BackGroundLoader = ui:GetChild("BackGroundLoader")
  uis.BackGroundHolder = ui:GetChild("BackGroundHolder")
  uis.root = ui
  return uis
end
```

---

## Rouge/ResDownload_Button_Red_BByName.lua.lua
**Functions:**
- GetResDownload_Button_Red_BUis
**Snippet:**
```lua
function GetResDownload_Button_Red_BUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/ResDownload_Button_Red_B_BtnByName.lua.lua
**Functions:**
- GetResDownload_Button_Red_B_BtnUis
**Requires:**
- ResDownload_Button_Red_BByName
**Snippet:**
```lua
require("ResDownload_Button_Red_BByName")

function GetResDownload_Button_Red_B_BtnUis(ui)
  local uis = {}
  uis.ButtonShadow = GetResDownload_Button_Red_BUis(ui:GetChild("ButtonShadow"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## Rouge/ResDownload_LightByName.lua.lua
**Functions:**
- GetResDownload_LightUis
**Snippet:**
```lua
function GetResDownload_LightUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Rouge/ResDownload_PopupBgByName.lua.lua
**Functions:**
- GetResDownload_PopupBgUis
**Snippet:**
```lua
function GetResDownload_PopupBgUis(ui)
  local uis = {}
  
  uis.BlurLoader = ui:GetChild("BlurLoader")
  uis.root = ui
  return uis
end
```

---

## Rouge/ResDownload_PopupCloseBtnByName.lua.lua
**Functions:**
- GetResDownload_PopupCloseBtnUis
**Snippet:**
```lua
function GetResDownload_PopupCloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/ResDownload_Popup_BByName.lua.lua
**Functions:**
- GetResDownload_Popup_BUis
**Snippet:**
```lua
function GetResDownload_Popup_BUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Rouge/ResDownload_ResDownloadBarByName.lua.lua
**Functions:**
- GetResDownload_ResDownloadBarUis
**Requires:**
- ResDownload_ResDownloadFillByName
- ResDownload_LightByName
**Snippet:**
```lua
require("ResDownload_ResDownloadFillByName")
require("ResDownload_LightByName")

function GetResDownload_ResDownloadBarUis(ui)
  local uis = {}
  uis.bar = GetResDownload_ResDownloadFillUis(ui:GetChild("bar"))
  uis.n6 = GetResDownload_LightUis(ui:GetChild("n6"))
  uis.root = ui
  return uis
end
```

---

## Rouge/ResDownload_ResDownloadByName.lua.lua
**Functions:**
- GetResDownload_ResDownloadUis
**Requires:**
- ResDownload_BackGroundByName
**Snippet:**
```lua
require("ResDownload_BackGroundByName")

function GetResDownload_ResDownloadUis(ui)
  local uis = {}
  uis.BackGround = GetResDownload_BackGroundUis(ui:GetChild("BackGround"))
  uis.ResDownLoadProgressBar = ui:GetChild("ResDownLoadProgressBar")
  uis.SizeTxt = ui:GetChild("SizeTxt")
  uis.SpeedTxt = ui:GetChild("SpeedTxt")
  uis.PercentageTxt = ui:GetChild("PercentageTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
```

---

## Rouge/ResDownload_ResDownloadFillByName.lua.lua
**Functions:**
- GetResDownload_ResDownloadFillUis
**Snippet:**
```lua
function GetResDownload_ResDownloadFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Rouge/ResDownload_TouchScreenBtnByName.lua.lua
**Functions:**
- GetResDownload_TouchScreenBtnUis
**Snippet:**
```lua
function GetResDownload_TouchScreenBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/ResDownload_Update1ByName.lua.lua
**Functions:**
- GetResDownload_Update1Uis
**Snippet:**
```lua
function GetResDownload_Update1Uis(ui)
  local uis = {}
  
  uis.PopupCloseBtn = ui:GetChild("PopupCloseBtn")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.CancelBtn = ui:GetChild("CancelBtn")
  uis.SureBtn = ui:GetChild("SureBtn")
  uis.root = ui
```

---

## Rouge/ResDownload_Update2ByName.lua.lua
**Functions:**
- GetResDownload_Update2Uis
**Requires:**
- ResDownload_PopupBgByName
- ResDownload_Popup_BByName
- ResDownload_Update1ByName
**Snippet:**
```lua
require("ResDownload_PopupBgByName")
require("ResDownload_Popup_BByName")
require("ResDownload_Update1ByName")

function GetResDownload_Update2Uis(ui)
  local uis = {}
  uis.PopupBg = GetResDownload_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Popup_B = GetResDownload_Popup_BUis(ui:GetChild("Popup_B"))
  uis.Update1 = GetResDownload_Update1Uis(ui:GetChild("Update1"))
```

---

## Rouge/ResDownload_UpdateWindowByName.lua.lua
**Functions:**
- GetResDownload_UpdateWindowUis
**Requires:**
- ResDownload_Update2ByName
**Snippet:**
```lua
require("ResDownload_Update2ByName")

function GetResDownload_UpdateWindowUis(ui)
  local uis = {}
  uis.Main = GetResDownload_Update2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/ResendPak.lua.lua
**Functions:**
- ResendPak.Resend
- ResendPak.DoReconnect
- ResendPak.Reset
- ResendPak.StartConnectGate
- ResendPak.ClearTime
- ResendPak.ConnectServerOk
**Requires:**
- MsgWaiter
- MsgWaiter
- MsgWaiter
**Snippet:**
```lua
local ResendPak = {
  isReconnect = false,
  connectTime = nil,
  connectNeedTime = 5,
  retryNum = 1
}

function ResendPak.Resend()
  local MsgWaiterObj = require("MsgWaiter")
  MsgWaiterObj.ResendAllTimeoutMsg()
```

---

## Rouge/ReservationWindow.lua.lua
**Functions:**
- ReservationWindow.ReInitData
- ReservationWindow.OnInit
- ReservationWindow.UpdateInfo
- ReservationWindow.TouchClose
- ReservationWindow.InitBtn
- ReservationWindow.OnClose
**Requires:**
- Reservation_ReservationWindowByName
**Snippet:**
```lua
require("Reservation_ReservationWindowByName")
local ReservationWindow = {}
local uis, contentPane

function ReservationWindow.ReInitData()
end

function ReservationWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ReservationWindow.package, WinResConfig.ReservationWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/Reservation_CloseBtnByName.lua.lua
**Functions:**
- GetReservation_CloseBtnUis
**Snippet:**
```lua
function GetReservation_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/Reservation_EmptyBtnByName.lua.lua
**Functions:**
- GetReservation_EmptyBtnUis
**Snippet:**
```lua
function GetReservation_EmptyBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/Reservation_GetBtnByName.lua.lua
**Functions:**
- GetReservation_GetBtnUis
**Snippet:**
```lua
function GetReservation_GetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/Reservation_LockByName.lua.lua
**Functions:**
- GetReservation_LockUis
**Snippet:**
```lua
function GetReservation_LockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/Reservation_ReservationByName.lua.lua
**Functions:**
- GetReservation_ReservationUis
**Requires:**
- CommonResource_PopupBgByName
- Reservation_ReservationTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Reservation_ReservationTipsByName")

function GetReservation_ReservationUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Tips = GetReservation_ReservationTipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
```

---

## Rouge/Reservation_ReservationTipsByName.lua.lua
**Functions:**
- GetReservation_ReservationTipsUis
**Requires:**
- Reservation_LockByName
**Snippet:**
```lua
require("Reservation_LockByName")

function GetReservation_ReservationTipsUis(ui)
  local uis = {}
  uis.Lock = GetReservation_LockUis(ui:GetChild("Lock"))
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.RewardGetBtn = ui:GetChild("RewardGetBtn")
  uis.CardLookBtn = ui:GetChild("CardLookBtn")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Rouge/Reservation_ReservationWindowByName.lua.lua
**Functions:**
- GetReservation_ReservationWindowUis
**Requires:**
- Reservation_ReservationByName
**Snippet:**
```lua
require("Reservation_ReservationByName")

function GetReservation_ReservationWindowUis(ui)
  local uis = {}
  uis.Main = GetReservation_ReservationUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/ResolutionHandler.lua.lua
**Functions:**
- ResolutionHandler.Init
**Snippet:**
```lua
local ResolutionHandler = {}
local _screenWidth = CS.UnityEngine.Screen.width
local _screenHeight = CS.UnityEngine.Screen.height
local _designScreenWidth = DesignScreen.width
local _designScreenHeight = DesignScreen.height
ResolutionHandler.Width = _designScreenWidth
ResolutionHandler.Height = _designScreenHeight
ResolutionHandler.AdaptOffset = {X = 0, Y = 0}
ResolutionHandler.ScreenScale = {X = 1, Y = 1}
ResolutionHandler.UIScale = 0.01333333
```

---

## Rouge/RewardShowWindow.lua.lua
**Functions:**
- RewardShowWindow.OnInit
- RewardShowWindow.Init
- RewardShowWindow.InitBtn
- RewardShowWindow.HandleMessage
- RewardShowWindow.OnClose
**Requires:**
- Message_RewardShowWindowByName
**Snippet:**
```lua
require("Message_RewardShowWindowByName")
local RewardShowWindow = {}
local contain = table.contain
local uis, contentPane, info

function RewardShowWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RewardShowWindow.package, WinResConfig.RewardShowWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetMessage_RewardShowWindowUis(contentPane)
```

---

## Rouge/RogueAchieveRewardTipsWindow.lua.lua
**Functions:**
- RogueAchieveRewardTipsWindow.ReInitData
- RogueAchieveRewardTipsWindow.OnInit
- RogueAchieveRewardTipsWindow.UpdateInfo
- tips.TabList.itemRenderer
- item.testEnableOnClick
- RogueAchieveRewardTipsWindow.ShowTaskInfo
- tips.WordList.itemRenderer
- taskRoot.ItemList.itemRenderer
- tips.LetterRegion.ChatList.itemRenderer
- RogueAchieveRewardTipsWindow.GetAllStorySimple
- RogueAchieveRewardTipsWindow.InitBtn
- RogueAchieveRewardTipsWindow.OnClose
**Requires:**
- RogueBuild01_AchieveRewardTipsWindowByName
**Snippet:**
```lua
require("RogueBuild01_AchieveRewardTipsWindowByName")
local RogueAchieveRewardTipsWindow = {}
local uis, contentPane, chapterData, allStory

function RogueAchieveRewardTipsWindow.ReInitData()
end

function RogueAchieveRewardTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RogueAchieveRewardTipsWindow.package, WinResConfig.RogueAchieveRewardTipsWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/RogueBookEndWindow.lua.lua
**Functions:**
- RogueBookEndWindow.ReInitData
- RogueBookEndWindow.OnInit
- RogueBookEndWindow.UpdateInfo
- uis.Main.TabList.itemRenderer
- item.testEnableOnClick
- RogueBookEndWindow.ShowInfo
- RogueBookEndWindow.GetEndingData
- RogueBookEndWindow.InitBtn
- RogueBookEndWindow.OnClose
**Requires:**
- RogueBuild01_BookEndWindowByName
**Snippet:**
```lua
require("RogueBuild01_BookEndWindowByName")
local RogueBookEndWindow = {}
local uis, contentPane, jumpTb, endingData

function RogueBookEndWindow.ReInitData()
end

function RogueBookEndWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RogueBookEndWindow.package, WinResConfig.RogueBookEndWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/RogueBookEventWindow.lua.lua
**Functions:**
- RogueBookEventWindow.ReInitData
- RogueBookEventWindow.OnInit
- RogueBookEventWindow.UpdateInfo
- uis.Main.TabList.itemRenderer
- btn.testEnableOnClick
- RogueBookEventWindow.ShowInfo
- RogueBookEventWindow.GetEventData
- RogueBookEventWindow.InitBtn
- RogueBookEventWindow.OnClose
**Requires:**
- RogueBuild01_BookEventWindowByName
**Snippet:**
```lua
require("RogueBuild01_BookEventWindowByName")
local RogueBookEventWindow = {}
local uis, contentPane, jumpTb, eventData

function RogueBookEventWindow.ReInitData()
end

function RogueBookEventWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RogueBookEventWindow.package, WinResConfig.RogueBookEventWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/RogueBookTreasureWindow.lua.lua
**Functions:**
- RogueBookTreasureWindow.ReInitData
- RogueBookTreasureWindow.OnInit
- RogueBookTreasureWindow.UpdateInfo
- RogueBookTreasureWindow.InitSacred
- tips.ItemList.itemRenderer
- RogueBookTreasureWindow.GetTipsName
- RogueBookTreasureWindow.ShowSacredInfo
- tips.Condition.ItemList.itemRenderer
- tips.WordList.itemRenderer
- RogueBookTreasureWindow.GetSacredUnlockData
- RogueBookTreasureWindow.ShowTips
- tips.WordList.itemRenderer
- RogueBookTreasureWindow.InitTreasure
- treasureTips.ItemList.itemRenderer
- RogueBookTreasureWindow.GetUnLockNum
- RogueBookTreasureWindow.ShowTreasureInfo
- tips.WordList.itemRenderer
- RogueBookTreasureWindow.StopAnim
- RogueBookTreasureWindow.InitScreen
- list.itemRenderer
- RogueBookTreasureWindow.GetScreenState
- RogueBookTreasureWindow.ResetScreenState
- RogueBookTreasureWindow.UpdateTreasureList
- RogueBookTreasureWindow.GetTreasureData
- RogueBookTreasureWindow.GetHolyData
- RogueBookTreasureWindow.InitBtn
- RogueBookTreasureWindow.OnClose
**Requires:**
- RogueBuild01_BookTreasureWindowByName
**Snippet:**
```lua
require("RogueBuild01_BookTreasureWindowByName")
local RogueBookTreasureWindow = {}
local uis, contentPane, jumpTb, treasureData, allTreasureData, holyData, animTime, isPlayAnim, holyPlayAnim, picInfo, lastTreasureId, cacheHoly
local timeIndex = 0
local treasureGroupId

function RogueBookTreasureWindow.ReInitData()
end

function RogueBookTreasureWindow.OnInit(bridgeObj)
```

---

## Rouge/RogueBuild01_AchieveContentAniByName.lua.lua
**Functions:**
- GetRogueBuild01_AchieveContentAniUis
**Snippet:**
```lua
function GetRogueBuild01_AchieveContentAniUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_AchieveContentBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_AchieveContentBtnUis
**Requires:**
- RogueBuild01_AchieveContent_ProgressByName
- RogueBuild01_AchieveContent_NewByName
- CommonResource_RedDotByName
- RogueBuild01_AchieveContent_LockByName
**Snippet:**
```lua
require("RogueBuild01_AchieveContent_ProgressByName")
require("RogueBuild01_AchieveContent_NewByName")
require("CommonResource_RedDotByName")
require("RogueBuild01_AchieveContent_LockByName")

function GetRogueBuild01_AchieveContentBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Progress = GetRogueBuild01_AchieveContent_ProgressUis(ui:GetChild("Progress"))
```

---

## Rouge/RogueBuild01_AchieveContentByName.lua.lua
**Functions:**
- GetRogueBuild01_AchieveContentUis
**Snippet:**
```lua
function GetRogueBuild01_AchieveContentUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.LookBtn = ui:GetChild("LookBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.choiceCtr = ui:GetController("choice")
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_AchieveContentLookBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_AchieveContentLookBtnUis
**Snippet:**
```lua
function GetRogueBuild01_AchieveContentLookBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_AchieveContent_LockByName.lua.lua
**Functions:**
- GetRogueBuild01_AchieveContent_LockUis
**Snippet:**
```lua
function GetRogueBuild01_AchieveContent_LockUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_AchieveContent_NewByName.lua.lua
**Functions:**
- GetRogueBuild01_AchieveContent_NewUis
**Snippet:**
```lua
function GetRogueBuild01_AchieveContent_NewUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_AchieveContent_ProgressByName.lua.lua
**Functions:**
- GetRogueBuild01_AchieveContent_ProgressUis
**Snippet:**
```lua
function GetRogueBuild01_AchieveContent_ProgressUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_AchieveRewardByName.lua.lua
**Functions:**
- GetRogueBuild01_AchieveRewardUis
**Snippet:**
```lua
function GetRogueBuild01_AchieveRewardUis(ui)
  local uis = {}
  
  uis.ContentList = ui:GetChild("ContentList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_AchieveRewardTips1ByName.lua.lua
**Functions:**
- GetRogueBuild01_AchieveRewardTips1Uis
**Requires:**
- RogueBuild01_AchieveRewardTips_TaskByName
- RogueBuild01_LetterRegionByName
**Snippet:**
```lua
require("RogueBuild01_AchieveRewardTips_TaskByName")
require("RogueBuild01_LetterRegionByName")

function GetRogueBuild01_AchieveRewardTips1Uis(ui)
  local uis = {}
  uis.TabList = ui:GetChild("TabList")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.Task = GetRogueBuild01_AchieveRewardTips_TaskUis(ui:GetChild("Task"))
  uis.LetterRegion = GetRogueBuild01_LetterRegionUis(ui:GetChild("LetterRegion"))
```

---

## Rouge/RogueBuild01_AchieveRewardTips2ByName.lua.lua
**Functions:**
- GetRogueBuild01_AchieveRewardTips2Uis
**Requires:**
- CommonResource_PopupBgByName
- RogueBuild01_AchieveRewardTips1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("RogueBuild01_AchieveRewardTips1ByName")

function GetRogueBuild01_AchieveRewardTips2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Tips = GetRogueBuild01_AchieveRewardTips1Uis(ui:GetChild("Tips"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Rouge/RogueBuild01_AchieveRewardTipsByName.lua.lua
**Functions:**
- GetRogueBuild01_AchieveRewardTipsUis
**Requires:**
- RogueBuild01_DayRewardConditionByName
- RogueBuild01_DayRewardItemByName
**Snippet:**
```lua
require("RogueBuild01_DayRewardConditionByName")
require("RogueBuild01_DayRewardItemByName")

function GetRogueBuild01_AchieveRewardTipsUis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.Condition = GetRogueBuild01_DayRewardConditionUis(ui:GetChild("Condition"))
  uis.RewardItem = GetRogueBuild01_DayRewardItemUis(ui:GetChild("RewardItem"))
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_AchieveRewardTipsWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_AchieveRewardTipsWindowUis
**Requires:**
- RogueBuild01_AchieveRewardTips2ByName
**Snippet:**
```lua
require("RogueBuild01_AchieveRewardTips2ByName")

function GetRogueBuild01_AchieveRewardTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_AchieveRewardTips2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_AchieveRewardTips_GetBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_AchieveRewardTips_GetBtnUis
**Snippet:**
```lua
function GetRogueBuild01_AchieveRewardTips_GetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_AchieveRewardTips_GetWordByName.lua.lua
**Functions:**
- GetRogueBuild01_AchieveRewardTips_GetWordUis
**Snippet:**
```lua
function GetRogueBuild01_AchieveRewardTips_GetWordUis(ui)
  local uis = {}
  
  uis.GetTxt = ui:GetChild("GetTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_AchieveRewardTips_ItemByName.lua.lua
**Functions:**
- GetRogueBuild01_AchieveRewardTips_ItemUis
**Requires:**
- RogueBuild01_AchieveRewardTips_ItemCardPicByName
**Snippet:**
```lua
require("RogueBuild01_AchieveRewardTips_ItemCardPicByName")

function GetRogueBuild01_AchieveRewardTips_ItemUis(ui)
  local uis = {}
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.ItemCardPic = GetRogueBuild01_AchieveRewardTips_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.typeCtr = ui:GetController("type")
```

---

## Rouge/RogueBuild01_AchieveRewardTips_ItemCardPicByName.lua.lua
**Functions:**
- GetRogueBuild01_AchieveRewardTips_ItemCardPicUis
**Snippet:**
```lua
function GetRogueBuild01_AchieveRewardTips_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.GetCtr = ui:GetController("Get")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_AchieveRewardTips_LockByName.lua.lua
**Functions:**
- GetRogueBuild01_AchieveRewardTips_LockUis
**Snippet:**
```lua
function GetRogueBuild01_AchieveRewardTips_LockUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_AchieveRewardTips_PlotByName.lua.lua
**Functions:**
- GetRogueBuild01_AchieveRewardTips_PlotUis
**Snippet:**
```lua
function GetRogueBuild01_AchieveRewardTips_PlotUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_AchieveRewardTips_ProgressByName.lua.lua
**Functions:**
- GetRogueBuild01_AchieveRewardTips_ProgressUis
**Snippet:**
```lua
function GetRogueBuild01_AchieveRewardTips_ProgressUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_AchieveRewardTips_TabBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_AchieveRewardTips_TabBtnUis
**Requires:**
- RogueBuild01_AchieveRewardTips_TabByName
**Snippet:**
```lua
require("RogueBuild01_AchieveRewardTips_TabByName")

function GetRogueBuild01_AchieveRewardTips_TabBtnUis(ui)
  local uis = {}
  uis.Tab = GetRogueBuild01_AchieveRewardTips_TabUis(ui:GetChild("Tab"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_AchieveRewardTips_TabByName.lua.lua
**Functions:**
- GetRogueBuild01_AchieveRewardTips_TabUis
**Requires:**
- CommonResource_RedDotByName
- RogueBuild01_AchieveRewardTips_LockByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")
require("RogueBuild01_AchieveRewardTips_LockByName")

function GetRogueBuild01_AchieveRewardTips_TabUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.Lock = GetRogueBuild01_AchieveRewardTips_LockUis(ui:GetChild("Lock"))
  uis.c2Ctr = ui:GetController("c2")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Rouge/RogueBuild01_AchieveRewardTips_TaskByName.lua.lua
**Functions:**
- GetRogueBuild01_AchieveRewardTips_TaskUis
**Requires:**
- RogueBuild01_AchieveRewardTips_ProgressByName
- RogueBuild01_AchieveRewardTips_GetWordByName
**Snippet:**
```lua
require("RogueBuild01_AchieveRewardTips_ProgressByName")
require("RogueBuild01_AchieveRewardTips_GetWordByName")

function GetRogueBuild01_AchieveRewardTips_TaskUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Progress = GetRogueBuild01_AchieveRewardTips_ProgressUis(ui:GetChild("Progress"))
  uis.GetWord = GetRogueBuild01_AchieveRewardTips_GetWordUis(ui:GetChild("GetWord"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.GetBtn = ui:GetChild("GetBtn")
```

---

## Rouge/RogueBuild01_BattleReward_EventAniByName.lua.lua
**Functions:**
- GetRogueBuild01_BattleReward_EventAniUis
**Requires:**
- RogueBuild01_BattleReward_EventByName
**Snippet:**
```lua
require("RogueBuild01_BattleReward_EventByName")

function GetRogueBuild01_BattleReward_EventAniUis(ui)
  local uis = {}
  uis.Event = GetRogueBuild01_BattleReward_EventUis(ui:GetChild("Event"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BattleReward_EventByName.lua.lua
**Functions:**
- GetRogueBuild01_BattleReward_EventUis
**Requires:**
- RogueBuild01_BattleReward_EventExecuteEndByName
**Snippet:**
```lua
require("RogueBuild01_BattleReward_EventExecuteEndByName")

function GetRogueBuild01_BattleReward_EventUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.ExecuteBtn = ui:GetChild("ExecuteBtn")
  uis.ExecuteEnd = GetRogueBuild01_BattleReward_EventExecuteEndUis(ui:GetChild("ExecuteEnd"))
  uis.UnExecuteBtn = ui:GetChild("UnExecuteBtn")
```

---

## Rouge/RogueBuild01_BattleReward_EventExecuteBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_BattleReward_EventExecuteBtnUis
**Snippet:**
```lua
function GetRogueBuild01_BattleReward_EventExecuteBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BattleReward_EventExecuteEndByName.lua.lua
**Functions:**
- GetRogueBuild01_BattleReward_EventExecuteEndUis
**Snippet:**
```lua
function GetRogueBuild01_BattleReward_EventExecuteEndUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BattleReward_EventUnExecuteBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_BattleReward_EventUnExecuteBtnUis
**Snippet:**
```lua
function GetRogueBuild01_BattleReward_EventUnExecuteBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BattleReward_EventWordByName.lua.lua
**Functions:**
- GetRogueBuild01_BattleReward_EventWordUis
**Snippet:**
```lua
function GetRogueBuild01_BattleReward_EventWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BookEndBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_BookEndBtnUis
**Snippet:**
```lua
function GetRogueBuild01_BookEndBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_BookEndByName.lua.lua
**Functions:**
- GetRogueBuild01_BookEndUis
**Requires:**
- CommonResource_BackGroundByName
- RogueBuild01_BookEndWordByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("RogueBuild01_BookEndWordByName")
require("CommonResource_CurrencyReturnByName")

function GetRogueBuild01_BookEndUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Word = GetRogueBuild01_BookEndWordUis(ui:GetChild("Word"))
  uis.TabList = ui:GetChild("TabList")
  uis.CurrencyReturn = GetCommonResource_CurrencyReturnUis(ui:GetChild("CurrencyReturn"))
```

---

## Rouge/RogueBuild01_BookEndLookBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_BookEndLookBtnUis
**Snippet:**
```lua
function GetRogueBuild01_BookEndLookBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BookEndTabBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_BookEndTabBtnUis
**Requires:**
- RogueBuild01_BookEndTabLockByName
**Snippet:**
```lua
require("RogueBuild01_BookEndTabLockByName")

function GetRogueBuild01_BookEndTabBtnUis(ui)
  local uis = {}
  uis.Lock = GetRogueBuild01_BookEndTabLockUis(ui:GetChild("Lock"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Rouge/RogueBuild01_BookEndTabLockByName.lua.lua
**Functions:**
- GetRogueBuild01_BookEndTabLockUis
**Snippet:**
```lua
function GetRogueBuild01_BookEndTabLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BookEndWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_BookEndWindowUis
**Requires:**
- RogueBuild01_BookEndByName
**Snippet:**
```lua
require("RogueBuild01_BookEndByName")

function GetRogueBuild01_BookEndWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_BookEndUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BookEndWordByName.lua.lua
**Functions:**
- GetRogueBuild01_BookEndWordUis
**Snippet:**
```lua
function GetRogueBuild01_BookEndWordUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.LookBtn = ui:GetChild("LookBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_BookEventBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_BookEventBtnUis
**Snippet:**
```lua
function GetRogueBuild01_BookEventBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_BookEventByName.lua.lua
**Functions:**
- GetRogueBuild01_BookEventUis
**Requires:**
- CommonResource_BackGroundByName
- RogueBuild01_BookEventPicByName
- RogueBuild01_BookEventTitleByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("RogueBuild01_BookEventPicByName")
require("RogueBuild01_BookEventTitleByName")
require("CommonResource_CurrencyReturnByName")

function GetRogueBuild01_BookEventUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.EventPic = GetRogueBuild01_BookEventPicUis(ui:GetChild("EventPic"))
  uis.Title = GetRogueBuild01_BookEventTitleUis(ui:GetChild("Title"))
```

---

## Rouge/RogueBuild01_BookEventPicByName.lua.lua
**Functions:**
- GetRogueBuild01_BookEventPicUis
**Snippet:**
```lua
function GetRogueBuild01_BookEventPicUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_BookEventTabAniByName.lua.lua
**Functions:**
- GetRogueBuild01_BookEventTabAniUis
**Snippet:**
```lua
function GetRogueBuild01_BookEventTabAniUis(ui)
  local uis = {}
  
  uis.TabBtn = ui:GetChild("TabBtn")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BookEventTabBtnBgByName.lua.lua
**Functions:**
- GetRogueBuild01_BookEventTabBtnBgUis
**Snippet:**
```lua
function GetRogueBuild01_BookEventTabBtnBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BookEventTabBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_BookEventTabBtnUis
**Requires:**
- RogueBuild01_BookEventTabBtnBgByName
- RogueBuild01_BookEventTabLockByName
**Snippet:**
```lua
require("RogueBuild01_BookEventTabBtnBgByName")
require("RogueBuild01_BookEventTabLockByName")

function GetRogueBuild01_BookEventTabBtnUis(ui)
  local uis = {}
  uis.Bg = GetRogueBuild01_BookEventTabBtnBgUis(ui:GetChild("Bg"))
  uis.Lock = GetRogueBuild01_BookEventTabLockUis(ui:GetChild("Lock"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Rouge/RogueBuild01_BookEventTabLockByName.lua.lua
**Functions:**
- GetRogueBuild01_BookEventTabLockUis
**Snippet:**
```lua
function GetRogueBuild01_BookEventTabLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BookEventTitleByName.lua.lua
**Functions:**
- GetRogueBuild01_BookEventTitleUis
**Snippet:**
```lua
function GetRogueBuild01_BookEventTitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BookEventWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_BookEventWindowUis
**Requires:**
- RogueBuild01_BookEventByName
**Snippet:**
```lua
require("RogueBuild01_BookEventByName")

function GetRogueBuild01_BookEventWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_BookEventUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BookSacredConditionByName.lua.lua
**Functions:**
- GetRogueBuild01_BookSacredConditionUis
**Snippet:**
```lua
function GetRogueBuild01_BookSacredConditionUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BookSacredConditionInfoByName.lua.lua
**Functions:**
- GetRogueBuild01_BookSacredConditionInfoUis
**Snippet:**
```lua
function GetRogueBuild01_BookSacredConditionInfoUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.IDTxt = ui:GetChild("IDTxt")
  uis.TypeTxt = ui:GetChild("TypeTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.LockBtn = ui:GetChild("LockBtn")
```

---

## Rouge/RogueBuild01_BookSacredConditionItemBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_BookSacredConditionItemBtnUis
**Snippet:**
```lua
function GetRogueBuild01_BookSacredConditionItemBtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.IDTxt = ui:GetChild("IDTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Rouge/RogueBuild01_BookSacredHeadBgByName.lua.lua
**Functions:**
- GetRogueBuild01_BookSacredHeadBgUis
**Snippet:**
```lua
function GetRogueBuild01_BookSacredHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BookSacredHeadByName.lua.lua
**Functions:**
- GetRogueBuild01_BookSacredHeadUis
**Requires:**
- RogueBuild01_BookSacredHeadBgByName
**Snippet:**
```lua
require("RogueBuild01_BookSacredHeadBgByName")

function GetRogueBuild01_BookSacredHeadUis(ui)
  local uis = {}
  uis.HeadBg = GetRogueBuild01_BookSacredHeadBgUis(ui:GetChild("HeadBg"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BookSacredInfoByName.lua.lua
**Functions:**
- GetRogueBuild01_BookSacredInfoUis
**Requires:**
- RogueBuild01_BookSacredConditionInfoByName
- RogueBuild01_BookSacredHeadByName
- RogueBuild01_BookSacredConditionByName
**Snippet:**
```lua
require("RogueBuild01_BookSacredConditionInfoByName")
require("RogueBuild01_BookSacredHeadByName")
require("RogueBuild01_BookSacredConditionByName")

function GetRogueBuild01_BookSacredInfoUis(ui)
  local uis = {}
  uis.ConditionInfo = GetRogueBuild01_BookSacredConditionInfoUis(ui:GetChild("ConditionInfo"))
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
```

---

## Rouge/RogueBuild01_BookSacredInfoLockBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_BookSacredInfoLockBtnUis
**Snippet:**
```lua
function GetRogueBuild01_BookSacredInfoLockBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BookSacredItemAniByName.lua.lua
**Functions:**
- GetRogueBuild01_BookSacredItemAniUis
**Snippet:**
```lua
function GetRogueBuild01_BookSacredItemAniUis(ui)
  local uis = {}
  
  uis.ItemBtn = ui:GetChild("ItemBtn")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BookSacredItemBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_BookSacredItemBtnUis
**Snippet:**
```lua
function GetRogueBuild01_BookSacredItemBtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.IDTxt = ui:GetChild("IDTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.buttonCtr = ui:GetController("button")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_BookSacredTipsByName.lua.lua
**Functions:**
- GetRogueBuild01_BookSacredTipsUis
**Requires:**
- RogueBuild01_BookSacredTitleByName
- RogueBuild01_BookSacredInfoByName
**Snippet:**
```lua
require("RogueBuild01_BookSacredTitleByName")
require("RogueBuild01_BookSacredInfoByName")

function GetRogueBuild01_BookSacredTipsUis(ui)
  local uis = {}
  uis.Title = GetRogueBuild01_BookSacredTitleUis(ui:GetChild("Title"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.Info = GetRogueBuild01_BookSacredInfoUis(ui:GetChild("Info"))
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_BookSacredTitleByName.lua.lua
**Functions:**
- GetRogueBuild01_BookSacredTitleUis
**Requires:**
- RogueBuild01_BookTreasureGetByName
**Snippet:**
```lua
require("RogueBuild01_BookTreasureGetByName")

function GetRogueBuild01_BookSacredTitleUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.GetTips = GetRogueBuild01_BookTreasureGetUis(ui:GetChild("GetTips"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BookTab01BtnByName.lua.lua
**Functions:**
- GetRogueBuild01_BookTab01BtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetRogueBuild01_BookTab01BtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BookTab02BtnByName.lua.lua
**Functions:**
- GetRogueBuild01_BookTab02BtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetRogueBuild01_BookTab02BtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BookTabRegionByName.lua.lua
**Functions:**
- GetRogueBuild01_BookTabRegionUis
**Snippet:**
```lua
function GetRogueBuild01_BookTabRegionUis(ui)
  local uis = {}
  
  uis.Tab01Btn = ui:GetChild("Tab01Btn")
  uis.Tab02Btn = ui:GetChild("Tab02Btn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BookTreasureBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_BookTreasureBtnUis
**Snippet:**
```lua
function GetRogueBuild01_BookTreasureBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BookTreasureByName.lua.lua
**Functions:**
- GetRogueBuild01_BookTreasureUis
**Requires:**
- CommonResource_BackGroundByName
- RogueBuild01_BookTreasureTipsByName
- RogueBuild01_BookSacredTipsByName
- RogueBuild01_BookTabRegionByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("RogueBuild01_BookTreasureTipsByName")
require("RogueBuild01_BookSacredTipsByName")
require("RogueBuild01_BookTabRegionByName")
require("CommonResource_CurrencyReturnByName")

function GetRogueBuild01_BookTreasureUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BookTreasureTips = GetRogueBuild01_BookTreasureTipsUis(ui:GetChild("BookTreasureTips"))
```

---

## Rouge/RogueBuild01_BookTreasureChoice1ByName.lua.lua
**Functions:**
- GetRogueBuild01_BookTreasureChoice1Uis
**Snippet:**
```lua
function GetRogueBuild01_BookTreasureChoice1Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BookTreasureChoice2ByName.lua.lua
**Functions:**
- GetRogueBuild01_BookTreasureChoice2Uis
**Snippet:**
```lua
function GetRogueBuild01_BookTreasureChoice2Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BookTreasureChoice3ByName.lua.lua
**Functions:**
- GetRogueBuild01_BookTreasureChoice3Uis
**Snippet:**
```lua
function GetRogueBuild01_BookTreasureChoice3Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BookTreasureChoiceByName.lua.lua
**Functions:**
- GetRogueBuild01_BookTreasureChoiceUis
**Requires:**
- RogueBuild01_BookTreasureChoice1ByName
- RogueBuild01_BookTreasureChoice2ByName
- RogueBuild01_BookTreasureChoice3ByName
**Snippet:**
```lua
require("RogueBuild01_BookTreasureChoice1ByName")
require("RogueBuild01_BookTreasureChoice2ByName")
require("RogueBuild01_BookTreasureChoice3ByName")

function GetRogueBuild01_BookTreasureChoiceUis(ui)
  local uis = {}
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.Choice1 = GetRogueBuild01_BookTreasureChoice1Uis(ui:GetChild("Choice1"))
  uis.Choice2 = GetRogueBuild01_BookTreasureChoice2Uis(ui:GetChild("Choice2"))
  uis.Choice3 = GetRogueBuild01_BookTreasureChoice3Uis(ui:GetChild("Choice3"))
```

---

## Rouge/RogueBuild01_BookTreasureChoiceResetBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_BookTreasureChoiceResetBtnUis
**Snippet:**
```lua
function GetRogueBuild01_BookTreasureChoiceResetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BookTreasureGetByName.lua.lua
**Functions:**
- GetRogueBuild01_BookTreasureGetUis
**Snippet:**
```lua
function GetRogueBuild01_BookTreasureGetUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BookTreasureInfoByName.lua.lua
**Functions:**
- GetRogueBuild01_BookTreasureInfoUis
**Snippet:**
```lua
function GetRogueBuild01_BookTreasureInfoUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.IDTxt = ui:GetChild("IDTxt")
  uis.TypeTxt = ui:GetChild("TypeTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.LockBtn = ui:GetChild("LockBtn")
```

---

## Rouge/RogueBuild01_BookTreasureInfoWordByName.lua.lua
**Functions:**
- GetRogueBuild01_BookTreasureInfoWordUis
**Snippet:**
```lua
function GetRogueBuild01_BookTreasureInfoWordUis(ui)
  local uis = {}
  
  uis.EffectTxt = ui:GetChild("EffectTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BookTreasureItemAniByName.lua.lua
**Functions:**
- GetRogueBuild01_BookTreasureItemAniUis
**Snippet:**
```lua
function GetRogueBuild01_BookTreasureItemAniUis(ui)
  local uis = {}
  
  uis.ItemBtn = ui:GetChild("ItemBtn")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BookTreasureItemBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_BookTreasureItemBtnUis
**Snippet:**
```lua
function GetRogueBuild01_BookTreasureItemBtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.IDTxt = ui:GetChild("IDTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.buttonCtr = ui:GetController("button")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_BookTreasureTipsByName.lua.lua
**Functions:**
- GetRogueBuild01_BookTreasureTipsUis
**Requires:**
- RogueBuild01_BookTreasureInfoByName
- RogueBuild01_BookTreasureTitleByName
- RogueBuild01_BookTreasureChoiceByName
**Snippet:**
```lua
require("RogueBuild01_BookTreasureInfoByName")
require("RogueBuild01_BookTreasureTitleByName")
require("RogueBuild01_BookTreasureChoiceByName")

function GetRogueBuild01_BookTreasureTipsUis(ui)
  local uis = {}
  uis.Info = GetRogueBuild01_BookTreasureInfoUis(ui:GetChild("Info"))
  uis.Title = GetRogueBuild01_BookTreasureTitleUis(ui:GetChild("Title"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.ScreenBtn = ui:GetChild("ScreenBtn")
```

---

## Rouge/RogueBuild01_BookTreasureTitleByName.lua.lua
**Functions:**
- GetRogueBuild01_BookTreasureTitleUis
**Requires:**
- RogueBuild01_BookTreasureGetByName
**Snippet:**
```lua
require("RogueBuild01_BookTreasureGetByName")

function GetRogueBuild01_BookTreasureTitleUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.GetTips = GetRogueBuild01_BookTreasureGetUis(ui:GetChild("GetTips"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_BookTreasureWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_BookTreasureWindowUis
**Requires:**
- RogueBuild01_BookTreasureByName
**Snippet:**
```lua
require("RogueBuild01_BookTreasureByName")

function GetRogueBuild01_BookTreasureWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_BookTreasureUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BuySacred_ConditionByName.lua.lua
**Functions:**
- GetRogueBuild01_BuySacred_ConditionUis
**Snippet:**
```lua
function GetRogueBuild01_BuySacred_ConditionUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_BuySacred_TipsByName.lua.lua
**Functions:**
- GetRogueBuild01_BuySacred_TipsUis
**Requires:**
- RogueBuild01_BookSacredHeadByName
- RogueBuild01_BuySacred_ConditionByName
**Snippet:**
```lua
require("RogueBuild01_BookSacredHeadByName")
require("RogueBuild01_BuySacred_ConditionByName")

function GetRogueBuild01_BuySacred_TipsUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.Head = GetRogueBuild01_BookSacredHeadUis(ui:GetChild("Head"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Condition = GetRogueBuild01_BuySacred_ConditionUis(ui:GetChild("Condition"))
  uis.IDTxt = ui:GetChild("IDTxt")
```

---

## Rouge/RogueBuild01_BuySacred_TipsWordByName.lua.lua
**Functions:**
- GetRogueBuild01_BuySacred_TipsWordUis
**Snippet:**
```lua
function GetRogueBuild01_BuySacred_TipsWordUis(ui)
  local uis = {}
  
  uis.EffectTxt = ui:GetChild("EffectTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Buy_GetByName.lua.lua
**Functions:**
- GetRogueBuild01_Buy_GetUis
**Snippet:**
```lua
function GetRogueBuild01_Buy_GetUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Buy_LackWordByName.lua.lua
**Functions:**
- GetRogueBuild01_Buy_LackWordUis
**Snippet:**
```lua
function GetRogueBuild01_Buy_LackWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Buy_LookBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_Buy_LookBtnUis
**Snippet:**
```lua
function GetRogueBuild01_Buy_LookBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Buy_SpendByName.lua.lua
**Functions:**
- GetRogueBuild01_Buy_SpendUis
**Snippet:**
```lua
function GetRogueBuild01_Buy_SpendUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Buy_SureBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_Buy_SureBtnUis
**Requires:**
- RogueBuild01_Buy_SpendByName
**Snippet:**
```lua
require("RogueBuild01_Buy_SpendByName")

function GetRogueBuild01_Buy_SureBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Spend = GetRogueBuild01_Buy_SpendUis(ui:GetChild("Spend"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_Buy_TipsByName.lua.lua
**Functions:**
- GetRogueBuild01_Buy_TipsUis
**Requires:**
- RogueBuild01_TreasureLevelByName
- RogueBuild01_TreasureTypeByName
- RogueBuild01_Buy_GetByName
**Snippet:**
```lua
require("RogueBuild01_TreasureLevelByName")
require("RogueBuild01_TreasureTypeByName")
require("RogueBuild01_Buy_GetByName")

function GetRogueBuild01_Buy_TipsUis(ui)
  local uis = {}
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.IDTxt = ui:GetChild("IDTxt")
```

---

## Rouge/RogueBuild01_Buy_TipsRegionByName.lua.lua
**Functions:**
- GetRogueBuild01_Buy_TipsRegionUis
**Requires:**
- RogueBuild01_Buy_TipsByName
- RogueBuild01_BuySacred_TipsByName
**Snippet:**
```lua
require("RogueBuild01_Buy_TipsByName")
require("RogueBuild01_BuySacred_TipsByName")

function GetRogueBuild01_Buy_TipsRegionUis(ui)
  local uis = {}
  uis.BuyTips = GetRogueBuild01_Buy_TipsUis(ui:GetChild("BuyTips"))
  uis.SacredTips = GetRogueBuild01_BuySacred_TipsUis(ui:GetChild("SacredTips"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_Buy_WordByName.lua.lua
**Functions:**
- GetRogueBuild01_Buy_WordUis
**Snippet:**
```lua
function GetRogueBuild01_Buy_WordUis(ui)
  local uis = {}
  
  uis.EffectTxt = ui:GetChild("EffectTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_EventAniByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_EventAniUis
**Requires:**
- RogueBuild01_Camp_EventByName
**Snippet:**
```lua
require("RogueBuild01_Camp_EventByName")

function GetRogueBuild01_Camp_EventAniUis(ui)
  local uis = {}
  uis.Event = GetRogueBuild01_Camp_EventUis(ui:GetChild("Event"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_EventByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_EventUis
**Requires:**
- RogueBuild01_Camp_EventExecuteEndByName
**Snippet:**
```lua
require("RogueBuild01_Camp_EventExecuteEndByName")

function GetRogueBuild01_Camp_EventUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.ExecuteBtn = ui:GetChild("ExecuteBtn")
  uis.ExecuteEnd = GetRogueBuild01_Camp_EventExecuteEndUis(ui:GetChild("ExecuteEnd"))
  uis.UnExecuteBtn = ui:GetChild("UnExecuteBtn")
```

---

## Rouge/RogueBuild01_Camp_EventExecuteBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_EventExecuteBtnUis
**Snippet:**
```lua
function GetRogueBuild01_Camp_EventExecuteBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_EventExecuteEndByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_EventExecuteEndUis
**Snippet:**
```lua
function GetRogueBuild01_Camp_EventExecuteEndUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_EventNumberByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_EventNumberUis
**Snippet:**
```lua
function GetRogueBuild01_Camp_EventNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_EventUnExecuteBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_EventUnExecuteBtnUis
**Snippet:**
```lua
function GetRogueBuild01_Camp_EventUnExecuteBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_EventWordByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_EventWordUis
**Snippet:**
```lua
function GetRogueBuild01_Camp_EventWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_GetAttributeTipsByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_GetAttributeTipsUis
**Requires:**
- CommonResource_PopupBgByName
- RogueBuild01_Camp_GetAttributeTipsRegionByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("RogueBuild01_Camp_GetAttributeTipsRegionByName")

function GetRogueBuild01_Camp_GetAttributeTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TipsRegion = GetRogueBuild01_Camp_GetAttributeTipsRegionUis(ui:GetChild("TipsRegion"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_GetAttributeTipsRegionByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_GetAttributeTipsRegionUis
**Snippet:**
```lua
function GetRogueBuild01_Camp_GetAttributeTipsRegionUis(ui)
  local uis = {}
  
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_GetAttributeTipsWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_GetAttributeTipsWindowUis
**Requires:**
- RogueBuild01_Camp_GetAttributeTipsByName
**Snippet:**
```lua
require("RogueBuild01_Camp_GetAttributeTipsByName")

function GetRogueBuild01_Camp_GetAttributeTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_Camp_GetAttributeTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_GetCurrencyTipsByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_GetCurrencyTipsUis
**Requires:**
- CommonResource_PopupBgByName
- RogueBuild01_Camp_GetCurrencyTipsRegionByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("RogueBuild01_Camp_GetCurrencyTipsRegionByName")

function GetRogueBuild01_Camp_GetCurrencyTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TipsRegion = GetRogueBuild01_Camp_GetCurrencyTipsRegionUis(ui:GetChild("TipsRegion"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_GetCurrencyTipsRegionByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_GetCurrencyTipsRegionUis
**Snippet:**
```lua
function GetRogueBuild01_Camp_GetCurrencyTipsRegionUis(ui)
  local uis = {}
  
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_GetCurrencyTipsWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_GetCurrencyTipsWindowUis
**Requires:**
- RogueBuild01_Camp_GetCurrencyTipsByName
**Snippet:**
```lua
require("RogueBuild01_Camp_GetCurrencyTipsByName")

function GetRogueBuild01_Camp_GetCurrencyTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_Camp_GetCurrencyTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_ItemTipsByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_ItemTipsUis
**Requires:**
- CommonResource_PopupBgByName
- RogueBuild01_Camp_ItemTipsRegionByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("RogueBuild01_Camp_ItemTipsRegionByName")

function GetRogueBuild01_Camp_ItemTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TipsRegion = GetRogueBuild01_Camp_ItemTipsRegionUis(ui:GetChild("TipsRegion"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_ItemTipsRegionByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_ItemTipsRegionUis
**Requires:**
- RogueBuild01_TreasureLevelByName
- RogueBuild01_TreasureTypeByName
**Snippet:**
```lua
require("RogueBuild01_TreasureLevelByName")
require("RogueBuild01_TreasureTypeByName")

function GetRogueBuild01_Camp_ItemTipsRegionUis(ui)
  local uis = {}
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.IDTxt = ui:GetChild("IDTxt")
  uis.Level = GetRogueBuild01_TreasureLevelUis(ui:GetChild("Level"))
  uis.Type = GetRogueBuild01_TreasureTypeUis(ui:GetChild("Type"))
```

---

## Rouge/RogueBuild01_Camp_ItemTipsWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_ItemTipsWindowUis
**Requires:**
- RogueBuild01_Camp_ItemTipsByName
**Snippet:**
```lua
require("RogueBuild01_Camp_ItemTipsByName")

function GetRogueBuild01_Camp_ItemTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_Camp_ItemTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_ItemTipsWordByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_ItemTipsWordUis
**Snippet:**
```lua
function GetRogueBuild01_Camp_ItemTipsWordUis(ui)
  local uis = {}
  
  uis.EffectTxt = ui:GetChild("EffectTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_RebirthTipsByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_RebirthTipsUis
**Requires:**
- CommonResource_PopupBgByName
- RogueBuild01_Camp_RebirthTipsRegionByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("RogueBuild01_Camp_RebirthTipsRegionByName")

function GetRogueBuild01_Camp_RebirthTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TipsRegion = GetRogueBuild01_Camp_RebirthTipsRegionUis(ui:GetChild("TipsRegion"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_RebirthTipsRegionByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_RebirthTipsRegionUis
**Requires:**
- RogueBuild01_Camp_RecruitTipsHeadByName
**Snippet:**
```lua
require("RogueBuild01_Camp_RecruitTipsHeadByName")

function GetRogueBuild01_Camp_RebirthTipsRegionUis(ui)
  local uis = {}
  uis.Head = GetRogueBuild01_Camp_RecruitTipsHeadUis(ui:GetChild("Head"))
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.HpProgressBar = ui:GetChild("HpProgressBar")
  uis.root = ui
```

---

## Rouge/RogueBuild01_Camp_RebirthTipsWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_RebirthTipsWindowUis
**Requires:**
- RogueBuild01_Camp_RebirthTipsByName
**Snippet:**
```lua
require("RogueBuild01_Camp_RebirthTipsByName")

function GetRogueBuild01_Camp_RebirthTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_Camp_RebirthTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_RecoveryTipsByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_RecoveryTipsUis
**Requires:**
- CommonResource_PopupBgByName
- RogueBuild01_Camp_RecoveryTipsRegionByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("RogueBuild01_Camp_RecoveryTipsRegionByName")

function GetRogueBuild01_Camp_RecoveryTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TipsRegion = GetRogueBuild01_Camp_RecoveryTipsRegionUis(ui:GetChild("TipsRegion"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_RecoveryTipsHeadBgByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_RecoveryTipsHeadBgUis
**Snippet:**
```lua
function GetRogueBuild01_Camp_RecoveryTipsHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_RecoveryTipsHeadByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_RecoveryTipsHeadUis
**Requires:**
- RogueBuild01_Camp_RecoveryTipsHeadBgByName
**Snippet:**
```lua
require("RogueBuild01_Camp_RecoveryTipsHeadBgByName")

function GetRogueBuild01_Camp_RecoveryTipsHeadUis(ui)
  local uis = {}
  uis.HeadBg = GetRogueBuild01_Camp_RecoveryTipsHeadBgUis(ui:GetChild("HeadBg"))
  uis.HpProgressBar = ui:GetChild("HpProgressBar")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_RecoveryTipsHpProgressBarByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_RecoveryTipsHpProgressBarUis
**Requires:**
- RogueBuild01_Camp_RecoveryTipsHpProgressFillByName
**Snippet:**
```lua
require("RogueBuild01_Camp_RecoveryTipsHpProgressFillByName")

function GetRogueBuild01_Camp_RecoveryTipsHpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetRogueBuild01_Camp_RecoveryTipsHpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_RecoveryTipsHpProgressFillByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_RecoveryTipsHpProgressFillUis
**Snippet:**
```lua
function GetRogueBuild01_Camp_RecoveryTipsHpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_RecoveryTipsRegionByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_RecoveryTipsRegionUis
**Snippet:**
```lua
function GetRogueBuild01_Camp_RecoveryTipsRegionUis(ui)
  local uis = {}
  
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.HeadList = ui:GetChild("HeadList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_RecoveryTipsWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_RecoveryTipsWindowUis
**Requires:**
- RogueBuild01_Camp_RecoveryTipsByName
**Snippet:**
```lua
require("RogueBuild01_Camp_RecoveryTipsByName")

function GetRogueBuild01_Camp_RecoveryTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_Camp_RecoveryTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_RecruitTipsByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_RecruitTipsUis
**Requires:**
- CommonResource_PopupBgByName
- RogueBuild01_Camp_RecruitTipsRegionByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("RogueBuild01_Camp_RecruitTipsRegionByName")

function GetRogueBuild01_Camp_RecruitTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TipsRegion = GetRogueBuild01_Camp_RecruitTipsRegionUis(ui:GetChild("TipsRegion"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_RecruitTipsHeadBgByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_RecruitTipsHeadBgUis
**Snippet:**
```lua
function GetRogueBuild01_Camp_RecruitTipsHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_RecruitTipsHeadByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_RecruitTipsHeadUis
**Requires:**
- RogueBuild01_Camp_RecruitTipsHeadBgByName
**Snippet:**
```lua
require("RogueBuild01_Camp_RecruitTipsHeadBgByName")

function GetRogueBuild01_Camp_RecruitTipsHeadUis(ui)
  local uis = {}
  uis.Bg = GetRogueBuild01_Camp_RecruitTipsHeadBgUis(ui:GetChild("Bg"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Camp_RecruitTipsRegionByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_RecruitTipsRegionUis
**Requires:**
- RogueBuild01_Camp_RecruitTipsHeadByName
**Snippet:**
```lua
require("RogueBuild01_Camp_RecruitTipsHeadByName")

function GetRogueBuild01_Camp_RecruitTipsRegionUis(ui)
  local uis = {}
  uis.Head = GetRogueBuild01_Camp_RecruitTipsHeadUis(ui:GetChild("Head"))
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_Camp_RecruitTipsWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_Camp_RecruitTipsWindowUis
**Requires:**
- RogueBuild01_Camp_RecruitTipsByName
**Snippet:**
```lua
require("RogueBuild01_Camp_RecruitTipsByName")

function GetRogueBuild01_Camp_RecruitTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_Camp_RecruitTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_CardUp_AssetsByName.lua.lua
**Functions:**
- GetRogueBuild01_CardUp_AssetsUis
**Snippet:**
```lua
function GetRogueBuild01_CardUp_AssetsUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_CardUp_CardAniByName.lua.lua
**Functions:**
- GetRogueBuild01_CardUp_CardAniUis
**Requires:**
- RogueBuild01_CardUp_CardByName
**Snippet:**
```lua
require("RogueBuild01_CardUp_CardByName")

function GetRogueBuild01_CardUp_CardAniUis(ui)
  local uis = {}
  uis.Card = GetRogueBuild01_CardUp_CardUis(ui:GetChild("Card"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_CardUp_CardByName.lua.lua
**Functions:**
- GetRogueBuild01_CardUp_CardUis
**Requires:**
- RogueBuild01_ChoiceCardList_CardBgByName
- RogueBuild01_DetailsCardAttributeByName
- RogueBuild01_CardUp_CardDieSignByName
**Snippet:**
```lua
require("RogueBuild01_ChoiceCardList_CardBgByName")
require("RogueBuild01_DetailsCardAttributeByName")
require("RogueBuild01_CardUp_CardDieSignByName")

function GetRogueBuild01_CardUp_CardUis(ui)
  local uis = {}
  uis.CardBg = GetRogueBuild01_ChoiceCardList_CardBgUis(ui:GetChild("CardBg"))
  uis.CardNameTxt = ui:GetChild("CardNameTxt")
  uis.StarList = ui:GetChild("StarList")
  uis.Attribute1 = GetRogueBuild01_DetailsCardAttributeUis(ui:GetChild("Attribute1"))
```

---

## Rouge/RogueBuild01_CardUp_CardDieSignByName.lua.lua
**Functions:**
- GetRogueBuild01_CardUp_CardDieSignUis
**Snippet:**
```lua
function GetRogueBuild01_CardUp_CardDieSignUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_CardUp_HpProgressBarByName.lua.lua
**Functions:**
- GetRogueBuild01_CardUp_HpProgressBarUis
**Requires:**
- RogueBuild01_CardUp_HpProgressFillByName
**Snippet:**
```lua
require("RogueBuild01_CardUp_HpProgressFillByName")

function GetRogueBuild01_CardUp_HpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetRogueBuild01_CardUp_HpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_CardUp_HpProgressFillByName.lua.lua
**Functions:**
- GetRogueBuild01_CardUp_HpProgressFillUis
**Snippet:**
```lua
function GetRogueBuild01_CardUp_HpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_CardUp_Info1ByName.lua.lua
**Functions:**
- GetRogueBuild01_CardUp_Info1Uis
**Requires:**
- CommonResource_OccupationByName
- CommonResource_CardBreachByName
**Snippet:**
```lua
require("CommonResource_OccupationByName")
require("CommonResource_CardBreachByName")

function GetRogueBuild01_CardUp_Info1Uis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.StarList = ui:GetChild("StarList")
  uis.ElementList = ui:GetChild("ElementList")
  uis.Occupation = GetCommonResource_OccupationUis(ui:GetChild("Occupation"))
```

---

## Rouge/RogueBuild01_CardUp_Info2ByName.lua.lua
**Functions:**
- GetRogueBuild01_CardUp_Info2Uis
**Requires:**
- RogueBuild01_ChoiceCardList_Info2_TitleByName
**Snippet:**
```lua
require("RogueBuild01_ChoiceCardList_Info2_TitleByName")

function GetRogueBuild01_CardUp_Info2Uis(ui)
  local uis = {}
  uis.Title = GetRogueBuild01_ChoiceCardList_Info2_TitleUis(ui:GetChild("Title"))
  uis.AttributeList = ui:GetChild("AttributeList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_CardUp_Info3AttributeByName.lua.lua
**Functions:**
- GetRogueBuild01_CardUp_Info3AttributeUis
**Snippet:**
```lua
function GetRogueBuild01_CardUp_Info3AttributeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.choiceCtr = ui:GetController("choice")
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_CardUp_Info3ByName.lua.lua
**Functions:**
- GetRogueBuild01_CardUp_Info3Uis
**Requires:**
- RogueBuild01_ChoiceCardList_Info2_TitleByName
- RogueBuild01_CardUp_Info3AttributeByName
- RogueBuild01_CardUp_Info3NoUpByName
- RogueBuild01_CardUp_Info3MaxByName
**Snippet:**
```lua
require("RogueBuild01_ChoiceCardList_Info2_TitleByName")
require("RogueBuild01_CardUp_Info3AttributeByName")
require("RogueBuild01_CardUp_Info3NoUpByName")
require("RogueBuild01_CardUp_Info3MaxByName")

function GetRogueBuild01_CardUp_Info3Uis(ui)
  local uis = {}
  uis.Title = GetRogueBuild01_ChoiceCardList_Info2_TitleUis(ui:GetChild("Title"))
  uis.Attribute1 = GetRogueBuild01_CardUp_Info3AttributeUis(ui:GetChild("Attribute1"))
  uis.Attribute2 = GetRogueBuild01_CardUp_Info3AttributeUis(ui:GetChild("Attribute2"))
```

---

## Rouge/RogueBuild01_CardUp_Info3MaxByName.lua.lua
**Functions:**
- GetRogueBuild01_CardUp_Info3MaxUis
**Snippet:**
```lua
function GetRogueBuild01_CardUp_Info3MaxUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_CardUp_Info3NoUpByName.lua.lua
**Functions:**
- GetRogueBuild01_CardUp_Info3NoUpUis
**Requires:**
- RogueBuild01_CardUp_Info3UpNumberByName
**Snippet:**
```lua
require("RogueBuild01_CardUp_Info3UpNumberByName")

function GetRogueBuild01_CardUp_Info3NoUpUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Spend = GetRogueBuild01_CardUp_Info3UpNumberUis(ui:GetChild("Spend"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_CardUp_Info3UpBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_CardUp_Info3UpBtnUis
**Requires:**
- RogueBuild01_CardUp_Info3UpNumberByName
**Snippet:**
```lua
require("RogueBuild01_CardUp_Info3UpNumberByName")

function GetRogueBuild01_CardUp_Info3UpBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Spend = GetRogueBuild01_CardUp_Info3UpNumberUis(ui:GetChild("Spend"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_CardUp_Info3UpNumberByName.lua.lua
**Functions:**
- GetRogueBuild01_CardUp_Info3UpNumberUis
**Snippet:**
```lua
function GetRogueBuild01_CardUp_Info3UpNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_CardUp_Info4NumberByName.lua.lua
**Functions:**
- GetRogueBuild01_CardUp_Info4NumberUis
**Snippet:**
```lua
function GetRogueBuild01_CardUp_Info4NumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_CardUp_InfoByName.lua.lua
**Functions:**
- GetRogueBuild01_CardUp_InfoUis
**Requires:**
- RogueBuild01_CardUp_Info1ByName
- RogueBuild01_CardUp_Info2ByName
- RogueBuild01_CardUp_Info3ByName
- RogueBuild01_ChoiceCardList_Info4ByName
**Snippet:**
```lua
require("RogueBuild01_CardUp_Info1ByName")
require("RogueBuild01_CardUp_Info2ByName")
require("RogueBuild01_CardUp_Info3ByName")
require("RogueBuild01_ChoiceCardList_Info4ByName")

function GetRogueBuild01_CardUp_InfoUis(ui)
  local uis = {}
  uis.Info1 = GetRogueBuild01_CardUp_Info1Uis(ui:GetChild("Info1"))
  uis.Info2 = GetRogueBuild01_CardUp_Info2Uis(ui:GetChild("Info2"))
  uis.Info3 = GetRogueBuild01_CardUp_Info3Uis(ui:GetChild("Info3"))
```

---

## Rouge/RogueBuild01_CardUp_ReviveBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_CardUp_ReviveBtnUis
**Requires:**
- RogueBuild01_CardUp_Info3UpNumberByName
**Snippet:**
```lua
require("RogueBuild01_CardUp_Info3UpNumberByName")

function GetRogueBuild01_CardUp_ReviveBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Spend = GetRogueBuild01_CardUp_Info3UpNumberUis(ui:GetChild("Spend"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_CardUp_SwitchBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_CardUp_SwitchBtnUis
**Snippet:**
```lua
function GetRogueBuild01_CardUp_SwitchBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ChoiceCardList_CardAniByName.lua.lua
**Functions:**
- GetRogueBuild01_ChoiceCardList_CardAniUis
**Requires:**
- RogueBuild01_ChoiceCardList_CardByName
**Snippet:**
```lua
require("RogueBuild01_ChoiceCardList_CardByName")

function GetRogueBuild01_ChoiceCardList_CardAniUis(ui)
  local uis = {}
  uis.Card = GetRogueBuild01_ChoiceCardList_CardUis(ui:GetChild("Card"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ChoiceCardList_CardBgByName.lua.lua
**Functions:**
- GetRogueBuild01_ChoiceCardList_CardBgUis
**Snippet:**
```lua
function GetRogueBuild01_ChoiceCardList_CardBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ChoiceCardList_CardByName.lua.lua
**Functions:**
- GetRogueBuild01_ChoiceCardList_CardUis
**Requires:**
- RogueBuild01_ChoiceCardList_CardBgByName
- CommonResource_OccupationByName
- CommonResource_CardBreachByName
**Snippet:**
```lua
require("RogueBuild01_ChoiceCardList_CardBgByName")
require("CommonResource_OccupationByName")
require("CommonResource_CardBreachByName")

function GetRogueBuild01_ChoiceCardList_CardUis(ui)
  local uis = {}
  uis.CardBg = GetRogueBuild01_ChoiceCardList_CardBgUis(ui:GetChild("CardBg"))
  uis.Occupation = GetCommonResource_OccupationUis(ui:GetChild("Occupation"))
  uis.ElementList = ui:GetChild("ElementList")
  uis.StarList = ui:GetChild("StarList")
```

---

## Rouge/RogueBuild01_ChoiceCardList_Info1ByName.lua.lua
**Functions:**
- GetRogueBuild01_ChoiceCardList_Info1Uis
**Requires:**
- CommonResource_OccupationByName
- CommonResource_CardBreachByName
**Snippet:**
```lua
require("CommonResource_OccupationByName")
require("CommonResource_CardBreachByName")

function GetRogueBuild01_ChoiceCardList_Info1Uis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.StarList = ui:GetChild("StarList")
  uis.ElementList = ui:GetChild("ElementList")
  uis.Occupation = GetCommonResource_OccupationUis(ui:GetChild("Occupation"))
```

---

## Rouge/RogueBuild01_ChoiceCardList_Info2ByName.lua.lua
**Functions:**
- GetRogueBuild01_ChoiceCardList_Info2Uis
**Requires:**
- RogueBuild01_ChoiceCardList_Info2_TitleByName
**Snippet:**
```lua
require("RogueBuild01_ChoiceCardList_Info2_TitleByName")

function GetRogueBuild01_ChoiceCardList_Info2Uis(ui)
  local uis = {}
  uis.AttributeList = ui:GetChild("AttributeList")
  uis.Title = GetRogueBuild01_ChoiceCardList_Info2_TitleUis(ui:GetChild("Title"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ChoiceCardList_Info2_AttributeByName.lua.lua
**Functions:**
- GetRogueBuild01_ChoiceCardList_Info2_AttributeUis
**Snippet:**
```lua
function GetRogueBuild01_ChoiceCardList_Info2_AttributeUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ChoiceCardList_Info2_TitleByName.lua.lua
**Functions:**
- GetRogueBuild01_ChoiceCardList_Info2_TitleUis
**Snippet:**
```lua
function GetRogueBuild01_ChoiceCardList_Info2_TitleUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ChoiceCardList_Info3ByName.lua.lua
**Functions:**
- GetRogueBuild01_ChoiceCardList_Info3Uis
**Requires:**
- RogueBuild01_ChoiceCardList_Info2_TitleByName
**Snippet:**
```lua
require("RogueBuild01_ChoiceCardList_Info2_TitleByName")

function GetRogueBuild01_ChoiceCardList_Info3Uis(ui)
  local uis = {}
  uis.Title = GetRogueBuild01_ChoiceCardList_Info2_TitleUis(ui:GetChild("Title"))
  uis.SkillList = ui:GetChild("SkillList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ChoiceCardList_Info3_SkillByName.lua.lua
**Functions:**
- GetRogueBuild01_ChoiceCardList_Info3_SkillUis
**Requires:**
- CommonResource_SkillByName
- RogueBuild01_ChoiceCardList_Info3_SkillCDInfoByName
- CommonResource_SkillDetailsTagByName
**Snippet:**
```lua
require("CommonResource_SkillByName")
require("RogueBuild01_ChoiceCardList_Info3_SkillCDInfoByName")
require("CommonResource_SkillDetailsTagByName")

function GetRogueBuild01_ChoiceCardList_Info3_SkillUis(ui)
  local uis = {}
  uis.BackImage = ui:GetChild("BackImage")
  uis.Skill = GetCommonResource_SkillUis(ui:GetChild("Skill"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
```

---

## Rouge/RogueBuild01_ChoiceCardList_Info3_SkillCDInfoByName.lua.lua
**Functions:**
- GetRogueBuild01_ChoiceCardList_Info3_SkillCDInfoUis
**Snippet:**
```lua
function GetRogueBuild01_ChoiceCardList_Info3_SkillCDInfoUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ChoiceCardList_Info4ByName.lua.lua
**Functions:**
- GetRogueBuild01_ChoiceCardList_Info4Uis
**Snippet:**
```lua
function GetRogueBuild01_ChoiceCardList_Info4Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ChoiceCardList_Info5ByName.lua.lua
**Functions:**
- GetRogueBuild01_ChoiceCardList_Info5Uis
**Snippet:**
```lua
function GetRogueBuild01_ChoiceCardList_Info5Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ChoiceCardList_InfoByName.lua.lua
**Functions:**
- GetRogueBuild01_ChoiceCardList_InfoUis
**Requires:**
- RogueBuild01_ChoiceCardList_Info1ByName
- RogueBuild01_ChoiceCardList_Info2ByName
- RogueBuild01_ChoiceCardList_Info3ByName
- RogueBuild01_ChoiceCardList_Info4ByName
**Snippet:**
```lua
require("RogueBuild01_ChoiceCardList_Info1ByName")
require("RogueBuild01_ChoiceCardList_Info2ByName")
require("RogueBuild01_ChoiceCardList_Info3ByName")
require("RogueBuild01_ChoiceCardList_Info4ByName")

function GetRogueBuild01_ChoiceCardList_InfoUis(ui)
  local uis = {}
  uis.Info1 = GetRogueBuild01_ChoiceCardList_Info1Uis(ui:GetChild("Info1"))
  uis.Info2 = GetRogueBuild01_ChoiceCardList_Info2Uis(ui:GetChild("Info2"))
  uis.Info3 = GetRogueBuild01_ChoiceCardList_Info3Uis(ui:GetChild("Info3"))
```

---

## Rouge/RogueBuild01_ChoiceCardList_OccupationBtnBgByName.lua.lua
**Functions:**
- GetRogueBuild01_ChoiceCardList_OccupationBtnBgUis
**Snippet:**
```lua
function GetRogueBuild01_ChoiceCardList_OccupationBtnBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ChoiceCardList_OccupationBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_ChoiceCardList_OccupationBtnUis
**Requires:**
- RogueBuild01_ChoiceCardList_OccupationBtnBgByName
**Snippet:**
```lua
require("RogueBuild01_ChoiceCardList_OccupationBtnBgByName")

function GetRogueBuild01_ChoiceCardList_OccupationBtnUis(ui)
  local uis = {}
  uis.OccupationBtnBg = GetRogueBuild01_ChoiceCardList_OccupationBtnBgUis(ui:GetChild("OccupationBtnBg"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ChoiceCardList_OccupationByName.lua.lua
**Functions:**
- GetRogueBuild01_ChoiceCardList_OccupationUis
**Snippet:**
```lua
function GetRogueBuild01_ChoiceCardList_OccupationUis(ui)
  local uis = {}
  
  uis.BtnList = ui:GetChild("BtnList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ChoiceCardList_SureBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_ChoiceCardList_SureBtnUis
**Snippet:**
```lua
function GetRogueBuild01_ChoiceCardList_SureBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_CoverDifficultyBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_CoverDifficultyBtnUis
**Snippet:**
```lua
function GetRogueBuild01_CoverDifficultyBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_CoverGiveUpBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_CoverGiveUpBtnUis
**Snippet:**
```lua
function GetRogueBuild01_CoverGiveUpBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_CoverHandBookBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_CoverHandBookBtnUis
**Snippet:**
```lua
function GetRogueBuild01_CoverHandBookBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_CoverLayersByName.lua.lua
**Functions:**
- GetRogueBuild01_CoverLayersUis
**Snippet:**
```lua
function GetRogueBuild01_CoverLayersUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_CoverLetterBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_CoverLetterBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetRogueBuild01_CoverLetterBtnUis(ui)
  local uis = {}
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_CoverRewardExpandByName.lua.lua
**Functions:**
- GetRogueBuild01_CoverRewardExpandUis
**Snippet:**
```lua
function GetRogueBuild01_CoverRewardExpandUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_CoverScoreBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_CoverScoreBtnUis
**Snippet:**
```lua
function GetRogueBuild01_CoverScoreBtnUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_CoverScoreRewardBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_CoverScoreRewardBtnUis
**Requires:**
- RogueBuild01_CoverRewardExpandByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("RogueBuild01_CoverRewardExpandByName")
require("CommonResource_RedDotByName")

function GetRogueBuild01_CoverScoreRewardBtnUis(ui)
  local uis = {}
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.RewardExpand = GetRogueBuild01_CoverRewardExpandUis(ui:GetChild("RewardExpand"))
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
```

---

## Rouge/RogueBuild01_CoverStartBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_CoverStartBtnUis
**Snippet:**
```lua
function GetRogueBuild01_CoverStartBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_CoverSweepBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_CoverSweepBtnUis
**Snippet:**
```lua
function GetRogueBuild01_CoverSweepBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_CoverTalentBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_CoverTalentBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetRogueBuild01_CoverTalentBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.newCtr = ui:GetController("new")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Rouge/RogueBuild01_CoverTitleByName.lua.lua
**Functions:**
- GetRogueBuild01_CoverTitleUis
**Snippet:**
```lua
function GetRogueBuild01_CoverTitleUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_CoverTreasureScreen1BtnByName.lua.lua
**Functions:**
- GetRogueBuild01_CoverTreasureScreen1BtnUis
**Snippet:**
```lua
function GetRogueBuild01_CoverTreasureScreen1BtnUis(ui)
  local uis = {}
  
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_CoverTreasureScreenBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_CoverTreasureScreenBtnUis
**Snippet:**
```lua
function GetRogueBuild01_CoverTreasureScreenBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DayContentAniByName.lua.lua
**Functions:**
- GetRogueBuild01_DayContentAniUis
**Requires:**
- RogueBuild01_DayContentByName
**Snippet:**
```lua
require("RogueBuild01_DayContentByName")

function GetRogueBuild01_DayContentAniUis(ui)
  local uis = {}
  uis.Content = GetRogueBuild01_DayContentUis(ui:GetChild("Content"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DayContentByName.lua.lua
**Functions:**
- GetRogueBuild01_DayContentUis
**Snippet:**
```lua
function GetRogueBuild01_DayContentUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.LookBtn = ui:GetChild("LookBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.choiceCtr = ui:GetController("choice")
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_DayContentLookBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_DayContentLookBtnUis
**Snippet:**
```lua
function GetRogueBuild01_DayContentLookBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DayRewardByName.lua.lua
**Functions:**
- GetRogueBuild01_DayRewardUis
**Requires:**
- RogueBuild01_DayRewardTimeByName
- RogueBuild01_DayRewardProgressByName
**Snippet:**
```lua
require("RogueBuild01_DayRewardTimeByName")
require("RogueBuild01_DayRewardProgressByName")

function GetRogueBuild01_DayRewardUis(ui)
  local uis = {}
  uis.Number = GetRogueBuild01_DayRewardTimeUis(ui:GetChild("Number"))
  uis.ContentList = ui:GetChild("ContentList")
  uis.Progress = GetRogueBuild01_DayRewardProgressUis(ui:GetChild("Progress"))
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_DayRewardConditionByName.lua.lua
**Functions:**
- GetRogueBuild01_DayRewardConditionUis
**Snippet:**
```lua
function GetRogueBuild01_DayRewardConditionUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DayRewardConditionWordByName.lua.lua
**Functions:**
- GetRogueBuild01_DayRewardConditionWordUis
**Snippet:**
```lua
function GetRogueBuild01_DayRewardConditionWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DayRewardIntegralByName.lua.lua
**Functions:**
- GetRogueBuild01_DayRewardIntegralUis
**Snippet:**
```lua
function GetRogueBuild01_DayRewardIntegralUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DayRewardItemBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_DayRewardItemBtnUis
**Requires:**
- RogueBuild01_DayRewardItemLookByName
**Snippet:**
```lua
require("RogueBuild01_DayRewardItemLookByName")

function GetRogueBuild01_DayRewardItemBtnUis(ui)
  local uis = {}
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.ItemLook = GetRogueBuild01_DayRewardItemLookUis(ui:GetChild("ItemLook"))
  uis.TouchBtn = ui:GetChild("TouchBtn")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Rouge/RogueBuild01_DayRewardItemByName.lua.lua
**Functions:**
- GetRogueBuild01_DayRewardItemUis
**Requires:**
- RogueBuild01_DayRewardItemState1ByName
- RogueBuild01_DayRewardItemState3ByName
- RogueBuild01_DayRewardItemState4ByName
**Snippet:**
```lua
require("RogueBuild01_DayRewardItemState1ByName")
require("RogueBuild01_DayRewardItemState3ByName")
require("RogueBuild01_DayRewardItemState4ByName")

function GetRogueBuild01_DayRewardItemUis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.State1 = GetRogueBuild01_DayRewardItemState1Uis(ui:GetChild("State1"))
  uis.State2Btn = ui:GetChild("State2Btn")
```

---

## Rouge/RogueBuild01_DayRewardItemLookByName.lua.lua
**Functions:**
- GetRogueBuild01_DayRewardItemLookUis
**Snippet:**
```lua
function GetRogueBuild01_DayRewardItemLookUis(ui)
  local uis = {}
  
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DayRewardItemState1ByName.lua.lua
**Functions:**
- GetRogueBuild01_DayRewardItemState1Uis
**Snippet:**
```lua
function GetRogueBuild01_DayRewardItemState1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DayRewardItemState2BtnByName.lua.lua
**Functions:**
- GetRogueBuild01_DayRewardItemState2BtnUis
**Snippet:**
```lua
function GetRogueBuild01_DayRewardItemState2BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DayRewardItemState3ByName.lua.lua
**Functions:**
- GetRogueBuild01_DayRewardItemState3Uis
**Snippet:**
```lua
function GetRogueBuild01_DayRewardItemState3Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DayRewardItemState4ByName.lua.lua
**Functions:**
- GetRogueBuild01_DayRewardItemState4Uis
**Snippet:**
```lua
function GetRogueBuild01_DayRewardItemState4Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DayRewardNumberByName.lua.lua
**Functions:**
- GetRogueBuild01_DayRewardNumberUis
**Snippet:**
```lua
function GetRogueBuild01_DayRewardNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DayRewardProgressByName.lua.lua
**Functions:**
- GetRogueBuild01_DayRewardProgressUis
**Snippet:**
```lua
function GetRogueBuild01_DayRewardProgressUis(ui)
  local uis = {}
  
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Rouge/RogueBuild01_DayRewardTimeByName.lua.lua
**Functions:**
- GetRogueBuild01_DayRewardTimeUis
**Snippet:**
```lua
function GetRogueBuild01_DayRewardTimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DayRewardTipsAniByName.lua.lua
**Functions:**
- GetRogueBuild01_DayRewardTipsAniUis
**Requires:**
- RogueBuild01_DayRewardTipsByName
**Snippet:**
```lua
require("RogueBuild01_DayRewardTipsByName")

function GetRogueBuild01_DayRewardTipsAniUis(ui)
  local uis = {}
  uis.DayRewardTips = GetRogueBuild01_DayRewardTipsUis(ui:GetChild("DayRewardTips"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DayRewardTipsByName.lua.lua
**Functions:**
- GetRogueBuild01_DayRewardTipsUis
**Requires:**
- RogueBuild01_DayRewardIntegralByName
**Snippet:**
```lua
require("RogueBuild01_DayRewardIntegralByName")

function GetRogueBuild01_DayRewardTipsUis(ui)
  local uis = {}
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Integral = GetRogueBuild01_DayRewardIntegralUis(ui:GetChild("Integral"))
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Rouge/RogueBuild01_DetailsCardAniByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsCardAniUis
**Requires:**
- RogueBuild01_DetailsCardByName
**Snippet:**
```lua
require("RogueBuild01_DetailsCardByName")

function GetRogueBuild01_DetailsCardAniUis(ui)
  local uis = {}
  uis.Card = GetRogueBuild01_DetailsCardUis(ui:GetChild("Card"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsCardAttributeByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsCardAttributeUis
**Snippet:**
```lua
function GetRogueBuild01_DetailsCardAttributeUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsCardBgByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsCardBgUis
**Snippet:**
```lua
function GetRogueBuild01_DetailsCardBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsCardByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsCardUis
**Requires:**
- RogueBuild01_DetailsCardBgByName
- RogueBuild01_DetailsCardAttributeByName
**Snippet:**
```lua
require("RogueBuild01_DetailsCardBgByName")
require("RogueBuild01_DetailsCardAttributeByName")

function GetRogueBuild01_DetailsCardUis(ui)
  local uis = {}
  uis.CardBg = GetRogueBuild01_DetailsCardBgUis(ui:GetChild("CardBg"))
  uis.CardNameTxt = ui:GetChild("CardNameTxt")
  uis.StarList = ui:GetChild("StarList")
  uis.Attribute1 = GetRogueBuild01_DetailsCardAttributeUis(ui:GetChild("Attribute1"))
  uis.Attribute2 = GetRogueBuild01_DetailsCardAttributeUis(ui:GetChild("Attribute2"))
```

---

## Rouge/RogueBuild01_DetailsDifficultyByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsDifficultyUis
**Snippet:**
```lua
function GetRogueBuild01_DetailsDifficultyUis(ui)
  local uis = {}
  
  uis.DifficultyTxt = ui:GetChild("DifficultyTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsItem1AniByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsItem1AniUis
**Requires:**
- RogueBuild01_DetailsItem1ByName
**Snippet:**
```lua
require("RogueBuild01_DetailsItem1ByName")

function GetRogueBuild01_DetailsItem1AniUis(ui)
  local uis = {}
  uis.Item = GetRogueBuild01_DetailsItem1Uis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsItem1ByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsItem1Uis
**Snippet:**
```lua
function GetRogueBuild01_DetailsItem1Uis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsItem2AniByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsItem2AniUis
**Requires:**
- RogueBuild01_DetailsItem2ByName
**Snippet:**
```lua
require("RogueBuild01_DetailsItem2ByName")

function GetRogueBuild01_DetailsItem2AniUis(ui)
  local uis = {}
  uis.Item = GetRogueBuild01_DetailsItem2Uis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsItem2ByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsItem2Uis
**Requires:**
- RogueBuild01_BookSacredHeadByName
**Snippet:**
```lua
require("RogueBuild01_BookSacredHeadByName")

function GetRogueBuild01_DetailsItem2Uis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Head = GetRogueBuild01_BookSacredHeadUis(ui:GetChild("Head"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Rouge/RogueBuild01_DetailsLayersByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsLayersUis
**Snippet:**
```lua
function GetRogueBuild01_DetailsLayersUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.LayersTxt = ui:GetChild("LayersTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsRegion1TypeByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsRegion1TypeUis
**Snippet:**
```lua
function GetRogueBuild01_DetailsRegion1TypeUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsRegion1_CardAniByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsRegion1_CardAniUis
**Requires:**
- RogueBuild01_DetailsCardByName
**Snippet:**
```lua
require("RogueBuild01_DetailsCardByName")

function GetRogueBuild01_DetailsRegion1_CardAniUis(ui)
  local uis = {}
  uis.Card = GetRogueBuild01_DetailsCardUis(ui:GetChild("Card"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsRegion1_CardByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsRegion1_CardUis
**Requires:**
- RogueBuild01_DetailsRegion1TypeByName
**Snippet:**
```lua
require("RogueBuild01_DetailsRegion1TypeByName")

function GetRogueBuild01_DetailsRegion1_CardUis(ui)
  local uis = {}
  uis.Type = GetRogueBuild01_DetailsRegion1TypeUis(ui:GetChild("Type"))
  uis.CardList = ui:GetChild("CardList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsRegion1_Item1AniByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsRegion1_Item1AniUis
**Requires:**
- RogueBuild01_DetailsRegion1_Item1_1ByName
**Snippet:**
```lua
require("RogueBuild01_DetailsRegion1_Item1_1ByName")

function GetRogueBuild01_DetailsRegion1_Item1AniUis(ui)
  local uis = {}
  uis.Item = GetRogueBuild01_DetailsRegion1_Item1_1Uis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsRegion1_Item1ByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsRegion1_Item1Uis
**Requires:**
- RogueBuild01_DetailsRegion1TypeByName
**Snippet:**
```lua
require("RogueBuild01_DetailsRegion1TypeByName")

function GetRogueBuild01_DetailsRegion1_Item1Uis(ui)
  local uis = {}
  uis.Type = GetRogueBuild01_DetailsRegion1TypeUis(ui:GetChild("Type"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsRegion1_Item1_1ByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsRegion1_Item1_1Uis
**Snippet:**
```lua
function GetRogueBuild01_DetailsRegion1_Item1_1Uis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsRegion1_Item2AniByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsRegion1_Item2AniUis
**Requires:**
- RogueBuild01_DetailsRegion1_Item2_1ByName
**Snippet:**
```lua
require("RogueBuild01_DetailsRegion1_Item2_1ByName")

function GetRogueBuild01_DetailsRegion1_Item2AniUis(ui)
  local uis = {}
  uis.Item = GetRogueBuild01_DetailsRegion1_Item2_1Uis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsRegion1_Item2ByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsRegion1_Item2Uis
**Requires:**
- RogueBuild01_DetailsRegion1TypeByName
**Snippet:**
```lua
require("RogueBuild01_DetailsRegion1TypeByName")

function GetRogueBuild01_DetailsRegion1_Item2Uis(ui)
  local uis = {}
  uis.Type = GetRogueBuild01_DetailsRegion1TypeUis(ui:GetChild("Type"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsRegion1_Item2_1ByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsRegion1_Item2_1Uis
**Requires:**
- RogueBuild01_BookSacredHeadByName
**Snippet:**
```lua
require("RogueBuild01_BookSacredHeadByName")

function GetRogueBuild01_DetailsRegion1_Item2_1Uis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Head = GetRogueBuild01_BookSacredHeadUis(ui:GetChild("Head"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Rouge/RogueBuild01_DetailsRegion1_WordByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsRegion1_WordUis
**Snippet:**
```lua
function GetRogueBuild01_DetailsRegion1_WordUis(ui)
  local uis = {}
  
  uis.WordList = ui:GetChild("WordList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsRegion1_WordContentByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsRegion1_WordContentUis
**Snippet:**
```lua
function GetRogueBuild01_DetailsRegion1_WordContentUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsRegion2_Difficulty1ByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsRegion2_Difficulty1Uis
**Snippet:**
```lua
function GetRogueBuild01_DetailsRegion2_Difficulty1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsRegion2_Difficulty2ByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsRegion2_Difficulty2Uis
**Snippet:**
```lua
function GetRogueBuild01_DetailsRegion2_Difficulty2Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsRegion2_DifficultyByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsRegion2_DifficultyUis
**Requires:**
- RogueBuild01_DetailsRegion2_Difficulty1ByName
- RogueBuild01_DetailsRegion2_Difficulty2ByName
**Snippet:**
```lua
require("RogueBuild01_DetailsRegion2_Difficulty1ByName")
require("RogueBuild01_DetailsRegion2_Difficulty2ByName")

function GetRogueBuild01_DetailsRegion2_DifficultyUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Difficulty = GetRogueBuild01_DetailsRegion2_Difficulty1Uis(ui:GetChild("Difficulty"))
  uis.Score = GetRogueBuild01_DetailsRegion2_Difficulty2Uis(ui:GetChild("Score"))
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_DetailsRegion2_ExitBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsRegion2_ExitBtnUis
**Snippet:**
```lua
function GetRogueBuild01_DetailsRegion2_ExitBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsRegion2_Exp1ByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsRegion2_Exp1Uis
**Snippet:**
```lua
function GetRogueBuild01_DetailsRegion2_Exp1Uis(ui)
  local uis = {}
  
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.ExpProgressBar = ui:GetChild("ExpProgressBar")
  uis.MaxTxt = ui:GetChild("MaxTxt")
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Rouge/RogueBuild01_DetailsRegion2_Exp1ProgressBarByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsRegion2_Exp1ProgressBarUis
**Requires:**
- RogueBuild01_DetailsRegion2_Exp1ProgressFillByName
**Snippet:**
```lua
require("RogueBuild01_DetailsRegion2_Exp1ProgressFillByName")

function GetRogueBuild01_DetailsRegion2_Exp1ProgressBarUis(ui)
  local uis = {}
  uis.bar = GetRogueBuild01_DetailsRegion2_Exp1ProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsRegion2_Exp1ProgressFillByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsRegion2_Exp1ProgressFillUis
**Snippet:**
```lua
function GetRogueBuild01_DetailsRegion2_Exp1ProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsRegion2_Exp2ByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsRegion2_Exp2Uis
**Snippet:**
```lua
function GetRogueBuild01_DetailsRegion2_Exp2Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsRegion2_ExpByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsRegion2_ExpUis
**Requires:**
- RogueBuild01_DetailsRegion2_Exp1ByName
- RogueBuild01_DetailsRegion2_Exp2ByName
**Snippet:**
```lua
require("RogueBuild01_DetailsRegion2_Exp1ByName")
require("RogueBuild01_DetailsRegion2_Exp2ByName")

function GetRogueBuild01_DetailsRegion2_ExpUis(ui)
  local uis = {}
  uis.Exp = GetRogueBuild01_DetailsRegion2_Exp1Uis(ui:GetChild("Exp"))
  uis.ExitBtn = ui:GetChild("ExitBtn")
  uis.Talent = GetRogueBuild01_DetailsRegion2_Exp2Uis(ui:GetChild("Talent"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Rouge/RogueBuild01_DetailsRegion2_InfoByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsRegion2_InfoUis
**Snippet:**
```lua
function GetRogueBuild01_DetailsRegion2_InfoUis(ui)
  local uis = {}
  
  uis.InfoList = ui:GetChild("InfoList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsRegion2_InfoTypeByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsRegion2_InfoTypeUis
**Snippet:**
```lua
function GetRogueBuild01_DetailsRegion2_InfoTypeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsRegion2_ScoreByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsRegion2_ScoreUis
**Snippet:**
```lua
function GetRogueBuild01_DetailsRegion2_ScoreUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsScoreByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsScoreUis
**Snippet:**
```lua
function GetRogueBuild01_DetailsScoreUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsTimeByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsTimeUis
**Snippet:**
```lua
function GetRogueBuild01_DetailsTimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DetailsTitleByName.lua.lua
**Functions:**
- GetRogueBuild01_DetailsTitleUis
**Snippet:**
```lua
function GetRogueBuild01_DetailsTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DifficultyChoiceByName.lua.lua
**Functions:**
- GetRogueBuild01_DifficultyChoiceUis
**Requires:**
- CommonResource_BackGroundByName
- RogueBuild01_DifficultyPositionShowByName
- RogueBuild01_DifficultyTipsByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("RogueBuild01_DifficultyPositionShowByName")
require("RogueBuild01_DifficultyTipsByName")
require("CommonResource_CurrencyReturnByName")

function GetRogueBuild01_DifficultyChoiceUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.PositionShow = GetRogueBuild01_DifficultyPositionShowUis(ui:GetChild("PositionShow"))
  uis.DifficultyTips = GetRogueBuild01_DifficultyTipsUis(ui:GetChild("DifficultyTips"))
```

---

## Rouge/RogueBuild01_DifficultyChoiceWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_DifficultyChoiceWindowUis
**Requires:**
- RogueBuild01_DifficultyChoiceByName
**Snippet:**
```lua
require("RogueBuild01_DifficultyChoiceByName")

function GetRogueBuild01_DifficultyChoiceWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_DifficultyChoiceUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DifficultyLook_EffectAniByName.lua.lua
**Functions:**
- GetRogueBuild01_DifficultyLook_EffectAniUis
**Requires:**
- RogueBuild01_DifficultyLook_EffectByName
**Snippet:**
```lua
require("RogueBuild01_DifficultyLook_EffectByName")

function GetRogueBuild01_DifficultyLook_EffectAniUis(ui)
  local uis = {}
  uis.Effect = GetRogueBuild01_DifficultyLook_EffectUis(ui:GetChild("Effect"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DifficultyLook_EffectByName.lua.lua
**Functions:**
- GetRogueBuild01_DifficultyLook_EffectUis
**Snippet:**
```lua
function GetRogueBuild01_DifficultyLook_EffectUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DifficultyLook_NumberByName.lua.lua
**Functions:**
- GetRogueBuild01_DifficultyLook_NumberUis
**Requires:**
- RogueBuild01_DifficultyLook_ScoreAddByName
**Snippet:**
```lua
require("RogueBuild01_DifficultyLook_ScoreAddByName")

function GetRogueBuild01_DifficultyLook_NumberUis(ui)
  local uis = {}
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ScoreAdd = GetRogueBuild01_DifficultyLook_ScoreAddUis(ui:GetChild("ScoreAdd"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_DifficultyLook_ScoreAddByName.lua.lua
**Functions:**
- GetRogueBuild01_DifficultyLook_ScoreAddUis
**Snippet:**
```lua
function GetRogueBuild01_DifficultyLook_ScoreAddUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxtTxt = ui:GetChild("WordTxtTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DifficultyLook_TipsBgByName.lua.lua
**Functions:**
- GetRogueBuild01_DifficultyLook_TipsBgUis
**Snippet:**
```lua
function GetRogueBuild01_DifficultyLook_TipsBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DifficultyLook_TipsByName.lua.lua
**Functions:**
- GetRogueBuild01_DifficultyLook_TipsUis
**Requires:**
- RogueBuild01_DifficultyLook_TipsBgByName
- RogueBuild01_DifficultyLook_NumberByName
**Snippet:**
```lua
require("RogueBuild01_DifficultyLook_TipsBgByName")
require("RogueBuild01_DifficultyLook_NumberByName")

function GetRogueBuild01_DifficultyLook_TipsUis(ui)
  local uis = {}
  uis.Bg = GetRogueBuild01_DifficultyLook_TipsBgUis(ui:GetChild("Bg"))
  uis.Number = GetRogueBuild01_DifficultyLook_NumberUis(ui:GetChild("Number"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DifficultyPositionByName.lua.lua
**Functions:**
- GetRogueBuild01_DifficultyPositionUis
**Requires:**
- RogueBuild01_DifficultyPositionTitleByName
- RogueBuild01_DifficultyPositionLockByName
**Snippet:**
```lua
require("RogueBuild01_DifficultyPositionTitleByName")
require("RogueBuild01_DifficultyPositionLockByName")

function GetRogueBuild01_DifficultyPositionUis(ui)
  local uis = {}
  uis.Title = GetRogueBuild01_DifficultyPositionTitleUis(ui:GetChild("Title"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SureBtn = ui:GetChild("SureBtn")
  uis.Lock = GetRogueBuild01_DifficultyPositionLockUis(ui:GetChild("Lock"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## Rouge/RogueBuild01_DifficultyPositionLockByName.lua.lua
**Functions:**
- GetRogueBuild01_DifficultyPositionLockUis
**Snippet:**
```lua
function GetRogueBuild01_DifficultyPositionLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DifficultyPositionShowByName.lua.lua
**Functions:**
- GetRogueBuild01_DifficultyPositionShowUis
**Snippet:**
```lua
function GetRogueBuild01_DifficultyPositionShowUis(ui)
  local uis = {}
  
  uis.PositionList = ui:GetChild("PositionList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DifficultyPositionSureBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_DifficultyPositionSureBtnUis
**Snippet:**
```lua
function GetRogueBuild01_DifficultyPositionSureBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DifficultyPositionTitleByName.lua.lua
**Functions:**
- GetRogueBuild01_DifficultyPositionTitleUis
**Snippet:**
```lua
function GetRogueBuild01_DifficultyPositionTitleUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DifficultyScoreAddByName.lua.lua
**Functions:**
- GetRogueBuild01_DifficultyScoreAddUis
**Snippet:**
```lua
function GetRogueBuild01_DifficultyScoreAddUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxtTxt = ui:GetChild("WordTxtTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DifficultyTipsByName.lua.lua
**Functions:**
- GetRogueBuild01_DifficultyTipsUis
**Requires:**
- RogueBuild01_DifficultyScoreAddByName
**Snippet:**
```lua
require("RogueBuild01_DifficultyScoreAddByName")

function GetRogueBuild01_DifficultyTipsUis(ui)
  local uis = {}
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ScoreAdd = GetRogueBuild01_DifficultyScoreAddUis(ui:GetChild("ScoreAdd"))
  uis.EffectList = ui:GetChild("EffectList")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Rouge/RogueBuild01_DifficultyTipsEffectAniByName.lua.lua
**Functions:**
- GetRogueBuild01_DifficultyTipsEffectAniUis
**Requires:**
- RogueBuild01_DifficultyTipsEffectByName
**Snippet:**
```lua
require("RogueBuild01_DifficultyTipsEffectByName")

function GetRogueBuild01_DifficultyTipsEffectAniUis(ui)
  local uis = {}
  uis.Effect = GetRogueBuild01_DifficultyTipsEffectUis(ui:GetChild("Effect"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DifficultyTipsEffectByName.lua.lua
**Functions:**
- GetRogueBuild01_DifficultyTipsEffectUis
**Snippet:**
```lua
function GetRogueBuild01_DifficultyTipsEffectUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DungeonInfo_MidByName.lua.lua
**Functions:**
- GetRogueBuild01_DungeonInfo_MidUis
**Snippet:**
```lua
function GetRogueBuild01_DungeonInfo_MidUis(ui)
  local uis = {}
  
  uis.WordList = ui:GetChild("WordList")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DungeonInfo_MidEffectByName.lua.lua
**Functions:**
- GetRogueBuild01_DungeonInfo_MidEffectUis
**Snippet:**
```lua
function GetRogueBuild01_DungeonInfo_MidEffectUis(ui)
  local uis = {}
  
  uis.EffectTxt = ui:GetChild("EffectTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DungeonInfo_MidWordByName.lua.lua
**Functions:**
- GetRogueBuild01_DungeonInfo_MidWordUis
**Snippet:**
```lua
function GetRogueBuild01_DungeonInfo_MidWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DungeonInfo_SureBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_DungeonInfo_SureBtnUis
**Snippet:**
```lua
function GetRogueBuild01_DungeonInfo_SureBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_DungeonInfo_TipsByName.lua.lua
**Functions:**
- GetRogueBuild01_DungeonInfo_TipsUis
**Requires:**
- RogueBuild01_DungeonInfo_TitleByName
- RogueBuild01_DungeonInfo_MidByName
**Snippet:**
```lua
require("RogueBuild01_DungeonInfo_TitleByName")
require("RogueBuild01_DungeonInfo_MidByName")

function GetRogueBuild01_DungeonInfo_TipsUis(ui)
  local uis = {}
  uis.Title = GetRogueBuild01_DungeonInfo_TitleUis(ui:GetChild("Title"))
  uis.Mid = GetRogueBuild01_DungeonInfo_MidUis(ui:GetChild("Mid"))
  uis.SureBtn = ui:GetChild("SureBtn")
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_DungeonInfo_TitleByName.lua.lua
**Functions:**
- GetRogueBuild01_DungeonInfo_TitleUis
**Snippet:**
```lua
function GetRogueBuild01_DungeonInfo_TitleUis(ui)
  local uis = {}
  
  uis.BattleTxt = ui:GetChild("BattleTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_GiveUp1ByName.lua.lua
**Functions:**
- GetRogueBuild01_GiveUp1Uis
**Snippet:**
```lua
function GetRogueBuild01_GiveUp1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_GiveUp2ByName.lua.lua
**Functions:**
- GetRogueBuild01_GiveUp2Uis
**Requires:**
- CommonResource_PopupBgByName
- CommonResource_Popup_BByName
- RogueBuild01_GiveUp1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("CommonResource_Popup_BByName")
require("RogueBuild01_GiveUp1ByName")

function GetRogueBuild01_GiveUp2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Popup_B = GetCommonResource_Popup_BUis(ui:GetChild("Popup_B"))
  uis.Currency1 = GetRogueBuild01_GiveUp1Uis(ui:GetChild("Currency1"))
```

---

## Rouge/RogueBuild01_GiveUpWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_GiveUpWindowUis
**Requires:**
- RogueBuild01_GiveUp2ByName
**Snippet:**
```lua
require("RogueBuild01_GiveUp2ByName")

function GetRogueBuild01_GiveUpWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_GiveUp2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_HandBookByName.lua.lua
**Functions:**
- GetRogueBuild01_HandBookUis
**Requires:**
- CommonResource_BackGroundByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("CommonResource_CurrencyReturnByName")

function GetRogueBuild01_HandBookUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BookEndBtn = ui:GetChild("BookEndBtn")
  uis.BookEventBtn = ui:GetChild("BookEventBtn")
  uis.BookTreasureBtn = ui:GetChild("BookTreasureBtn")
  uis.CurrencyReturn = GetCommonResource_CurrencyReturnUis(ui:GetChild("CurrencyReturn"))
```

---

## Rouge/RogueBuild01_HandBookWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_HandBookWindowUis
**Requires:**
- RogueBuild01_HandBookByName
**Snippet:**
```lua
require("RogueBuild01_HandBookByName")

function GetRogueBuild01_HandBookWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_HandBookUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideBattleRewardByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideBattleRewardUis
**Requires:**
- CommonResource_BackGroundByName
- RogueBuild01_InsideMapBottomByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("RogueBuild01_InsideMapBottomByName")

function GetRogueBuild01_InsideBattleRewardUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.OutBtn = ui:GetChild("OutBtn")
  uis.Botton = GetRogueBuild01_InsideMapBottomUis(ui:GetChild("Botton"))
  uis.AssetsList = ui:GetChild("AssetsList")
  uis.EventList = ui:GetChild("EventList")
```

---

## Rouge/RogueBuild01_InsideBattleRewardWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideBattleRewardWindowUis
**Requires:**
- RogueBuild01_InsideBattleRewardByName
**Snippet:**
```lua
require("RogueBuild01_InsideBattleRewardByName")

function GetRogueBuild01_InsideBattleRewardWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_InsideBattleRewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideCampByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideCampUis
**Requires:**
- CommonResource_BackGroundByName
- RogueBuild01_InsideMapBottomByName
- RogueBuild01_Camp_EventNumberByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("RogueBuild01_InsideMapBottomByName")
require("RogueBuild01_Camp_EventNumberByName")

function GetRogueBuild01_InsideCampUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.OutBtn = ui:GetChild("OutBtn")
  uis.Botton = GetRogueBuild01_InsideMapBottomUis(ui:GetChild("Botton"))
  uis.EventList = ui:GetChild("EventList")
```

---

## Rouge/RogueBuild01_InsideCampWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideCampWindowUis
**Requires:**
- RogueBuild01_InsideCampByName
**Snippet:**
```lua
require("RogueBuild01_InsideCampByName")

function GetRogueBuild01_InsideCampWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_InsideCampUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideCardUpByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideCardUpUis
**Requires:**
- CommonResource_BackGroundByName
- RogueBuild01_CardUp_InfoByName
- RogueBuild01_ChoiceCardList_InfoByName
- RogueBuild01_CardUp_Info4NumberByName
- RogueBuild01_ChoiceCardList_OccupationByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("RogueBuild01_CardUp_InfoByName")
require("RogueBuild01_ChoiceCardList_InfoByName")
require("RogueBuild01_CardUp_Info4NumberByName")
require("RogueBuild01_ChoiceCardList_OccupationByName")

function GetRogueBuild01_InsideCardUpUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Info1 = GetRogueBuild01_CardUp_InfoUis(ui:GetChild("Info1"))
```

---

## Rouge/RogueBuild01_InsideCardUpWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideCardUpWindowUis
**Requires:**
- RogueBuild01_InsideCardUpByName
**Snippet:**
```lua
require("RogueBuild01_InsideCardUpByName")

function GetRogueBuild01_InsideCardUpWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_InsideCardUpUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideDifficultyLookByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideDifficultyLookUis
**Requires:**
- CommonResource_PopupBgByName
- RogueBuild01_DifficultyLook_TipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("RogueBuild01_DifficultyLook_TipsByName")

function GetRogueBuild01_InsideDifficultyLookUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Tips = GetRogueBuild01_DifficultyLook_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_InsideDifficultyLookWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideDifficultyLookWindowUis
**Requires:**
- RogueBuild01_InsideDifficultyLookByName
**Snippet:**
```lua
require("RogueBuild01_InsideDifficultyLookByName")

function GetRogueBuild01_InsideDifficultyLookWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_InsideDifficultyLookUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideDungeonInfoByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideDungeonInfoUis
**Requires:**
- RogueBuild01_DungeonInfo_TipsByName
**Snippet:**
```lua
require("RogueBuild01_DungeonInfo_TipsByName")

function GetRogueBuild01_InsideDungeonInfoUis(ui)
  local uis = {}
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.DungeonInfoTips = GetRogueBuild01_DungeonInfo_TipsUis(ui:GetChild("DungeonInfoTips"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideDungeonInfoWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideDungeonInfoWindowUis
**Requires:**
- RogueBuild01_InsideDungeonInfoByName
**Snippet:**
```lua
require("RogueBuild01_InsideDungeonInfoByName")

function GetRogueBuild01_InsideDungeonInfoWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_InsideDungeonInfoUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideEndByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideEndUis
**Snippet:**
```lua
function GetRogueBuild01_InsideEndUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideEndDetailsByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideEndDetailsUis
**Requires:**
- CommonResource_BackGroundByName
- RogueBuild01_InsideEndDetailsTitleByName
- RogueBuild01_InsideEndDetailsRegion1ByName
- RogueBuild01_InsideEndDetailsRegion2ByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("RogueBuild01_InsideEndDetailsTitleByName")
require("RogueBuild01_InsideEndDetailsRegion1ByName")
require("RogueBuild01_InsideEndDetailsRegion2ByName")

function GetRogueBuild01_InsideEndDetailsUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Title = GetRogueBuild01_InsideEndDetailsTitleUis(ui:GetChild("Title"))
  uis.Region1 = GetRogueBuild01_InsideEndDetailsRegion1Uis(ui:GetChild("Region1"))
```

---

## Rouge/RogueBuild01_InsideEndDetailsLastBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideEndDetailsLastBtnUis
**Snippet:**
```lua
function GetRogueBuild01_InsideEndDetailsLastBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideEndDetailsNextBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideEndDetailsNextBtnUis
**Snippet:**
```lua
function GetRogueBuild01_InsideEndDetailsNextBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideEndDetailsRegion1ByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideEndDetailsRegion1Uis
**Requires:**
- RogueBuild01_DetailsRegion1_WordByName
- RogueBuild01_DetailsRegion1_CardByName
- RogueBuild01_DetailsRegion1_Item1ByName
- RogueBuild01_DetailsRegion1_Item2ByName
**Snippet:**
```lua
require("RogueBuild01_DetailsRegion1_WordByName")
require("RogueBuild01_DetailsRegion1_CardByName")
require("RogueBuild01_DetailsRegion1_Item1ByName")
require("RogueBuild01_DetailsRegion1_Item2ByName")

function GetRogueBuild01_InsideEndDetailsRegion1Uis(ui)
  local uis = {}
  uis.Word = GetRogueBuild01_DetailsRegion1_WordUis(ui:GetChild("Word"))
  uis.Card = GetRogueBuild01_DetailsRegion1_CardUis(ui:GetChild("Card"))
  uis.Item1 = GetRogueBuild01_DetailsRegion1_Item1Uis(ui:GetChild("Item1"))
```

---

## Rouge/RogueBuild01_InsideEndDetailsRegion2ByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideEndDetailsRegion2Uis
**Requires:**
- RogueBuild01_DetailsRegion2_ScoreByName
- RogueBuild01_DetailsRegion2_DifficultyByName
- RogueBuild01_DetailsRegion2_ExpByName
- RogueBuild01_DetailsRegion2_InfoByName
**Snippet:**
```lua
require("RogueBuild01_DetailsRegion2_ScoreByName")
require("RogueBuild01_DetailsRegion2_DifficultyByName")
require("RogueBuild01_DetailsRegion2_ExpByName")
require("RogueBuild01_DetailsRegion2_InfoByName")

function GetRogueBuild01_InsideEndDetailsRegion2Uis(ui)
  local uis = {}
  uis.Score = GetRogueBuild01_DetailsRegion2_ScoreUis(ui:GetChild("Score"))
  uis.Difficulty = GetRogueBuild01_DetailsRegion2_DifficultyUis(ui:GetChild("Difficulty"))
  uis.Exp = GetRogueBuild01_DetailsRegion2_ExpUis(ui:GetChild("Exp"))
```

---

## Rouge/RogueBuild01_InsideEndDetailsTitleByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideEndDetailsTitleUis
**Snippet:**
```lua
function GetRogueBuild01_InsideEndDetailsTitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideEndDetailsWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideEndDetailsWindowUis
**Requires:**
- RogueBuild01_InsideEndDetailsByName
**Snippet:**
```lua
require("RogueBuild01_InsideEndDetailsByName")

function GetRogueBuild01_InsideEndDetailsWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_InsideEndDetailsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideEndWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideEndWindowUis
**Requires:**
- RogueBuild01_InsideEndByName
**Snippet:**
```lua
require("RogueBuild01_InsideEndByName")

function GetRogueBuild01_InsideEndWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_InsideEndUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideItemLookByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideItemLookUis
**Requires:**
- CommonResource_BackGroundByName
- RogueBuild01_ItemLook_TreasureTipsByName
- RogueBuild01_ItemLook_SacredTipsByName
- RogueBuild01_ItemLook_TabRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("RogueBuild01_ItemLook_TreasureTipsByName")
require("RogueBuild01_ItemLook_SacredTipsByName")
require("RogueBuild01_ItemLook_TabRegionByName")

function GetRogueBuild01_InsideItemLookUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TreasureTips = GetRogueBuild01_ItemLook_TreasureTipsUis(ui:GetChild("TreasureTips"))
  uis.SacredTips = GetRogueBuild01_ItemLook_SacredTipsUis(ui:GetChild("SacredTips"))
```

---

## Rouge/RogueBuild01_InsideItemLookWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideItemLookWindowUis
**Requires:**
- RogueBuild01_InsideItemLookByName
**Snippet:**
```lua
require("RogueBuild01_InsideItemLookByName")

function GetRogueBuild01_InsideItemLookWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_InsideItemLookUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideMapBottomByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideMapBottomUis
**Snippet:**
```lua
function GetRogueBuild01_InsideMapBottomUis(ui)
  local uis = {}
  
  uis.DifficultyBtn = ui:GetChild("DifficultyBtn")
  uis.ItemBtn = ui:GetChild("ItemBtn")
  uis.CardBtn = ui:GetChild("CardBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
```

---

## Rouge/RogueBuild01_InsideMapBottomCardBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideMapBottomCardBtnUis
**Snippet:**
```lua
function GetRogueBuild01_InsideMapBottomCardBtnUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideMapBottomDifficultyBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideMapBottomDifficultyBtnUis
**Snippet:**
```lua
function GetRogueBuild01_InsideMapBottomDifficultyBtnUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideMapBottomItemBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideMapBottomItemBtnUis
**Snippet:**
```lua
function GetRogueBuild01_InsideMapBottomItemBtnUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_InsideMapBottomItemByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideMapBottomItemUis
**Snippet:**
```lua
function GetRogueBuild01_InsideMapBottomItemUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideMapByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideMapUis
**Requires:**
- CommonResource_BackGroundByName
- RogueBuild01_InsideMapLayerByName
- RogueBuild01_MapListByName
- RogueBuild01_InsideMapBottomByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("RogueBuild01_InsideMapLayerByName")
require("RogueBuild01_MapListByName")
require("RogueBuild01_InsideMapBottomByName")

function GetRogueBuild01_InsideMapUis(ui)
  local uis = {}
  uis.BgList = ui:GetChild("BgList")
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Layer = GetRogueBuild01_InsideMapLayerUis(ui:GetChild("Layer"))
```

---

## Rouge/RogueBuild01_InsideMapEvent_AllByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideMapEvent_AllUis
**Requires:**
- RogueBuild01_InsideMapEvent_Battle1ByName
- RogueBuild01_InsideMapEvent_Battle2ByName
- RogueBuild01_InsideMapEvent_Battle3ByName
- RogueBuild01_InsideMapEvent_CampByName
- RogueBuild01_InsideMapEvent_PlotByName
- RogueBuild01_InsideMapEvent_ShopByName
**Snippet:**
```lua
require("RogueBuild01_InsideMapEvent_Battle1ByName")
require("RogueBuild01_InsideMapEvent_Battle2ByName")
require("RogueBuild01_InsideMapEvent_Battle3ByName")
require("RogueBuild01_InsideMapEvent_CampByName")
require("RogueBuild01_InsideMapEvent_PlotByName")
require("RogueBuild01_InsideMapEvent_ShopByName")

function GetRogueBuild01_InsideMapEvent_AllUis(ui)
  local uis = {}
  uis.Battle1 = GetRogueBuild01_InsideMapEvent_Battle1Uis(ui:GetChild("Battle1"))
```

---

## Rouge/RogueBuild01_InsideMapEvent_Battle1ByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideMapEvent_Battle1Uis
**Requires:**
- RogueBuild01_InsideMapEvent_LineDotByName
**Snippet:**
```lua
require("RogueBuild01_InsideMapEvent_LineDotByName")

function GetRogueBuild01_InsideMapEvent_Battle1Uis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.Light1_1 = GetRogueBuild01_InsideMapEvent_LineDotUis(ui:GetChild("Light1_1"))
  uis.Light2_1 = GetRogueBuild01_InsideMapEvent_LineDotUis(ui:GetChild("Light2_1"))
  uis.Light2_2 = GetRogueBuild01_InsideMapEvent_LineDotUis(ui:GetChild("Light2_2"))
```

---

## Rouge/RogueBuild01_InsideMapEvent_Battle2ByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideMapEvent_Battle2Uis
**Requires:**
- RogueBuild01_InsideMapEvent_LineDotByName
**Snippet:**
```lua
require("RogueBuild01_InsideMapEvent_LineDotByName")

function GetRogueBuild01_InsideMapEvent_Battle2Uis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.Light1_1 = GetRogueBuild01_InsideMapEvent_LineDotUis(ui:GetChild("Light1_1"))
  uis.Light2_1 = GetRogueBuild01_InsideMapEvent_LineDotUis(ui:GetChild("Light2_1"))
  uis.Light2_2 = GetRogueBuild01_InsideMapEvent_LineDotUis(ui:GetChild("Light2_2"))
```

---

## Rouge/RogueBuild01_InsideMapEvent_Battle3ByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideMapEvent_Battle3Uis
**Requires:**
- RogueBuild01_InsideMapEvent_LineDotByName
**Snippet:**
```lua
require("RogueBuild01_InsideMapEvent_LineDotByName")

function GetRogueBuild01_InsideMapEvent_Battle3Uis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.Light1_1 = GetRogueBuild01_InsideMapEvent_LineDotUis(ui:GetChild("Light1_1"))
  uis.Light2_1 = GetRogueBuild01_InsideMapEvent_LineDotUis(ui:GetChild("Light2_1"))
  uis.Light2_2 = GetRogueBuild01_InsideMapEvent_LineDotUis(ui:GetChild("Light2_2"))
```

---

## Rouge/RogueBuild01_InsideMapEvent_CampByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideMapEvent_CampUis
**Requires:**
- RogueBuild01_InsideMapEvent_LineDotByName
**Snippet:**
```lua
require("RogueBuild01_InsideMapEvent_LineDotByName")

function GetRogueBuild01_InsideMapEvent_CampUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.Light1_1 = GetRogueBuild01_InsideMapEvent_LineDotUis(ui:GetChild("Light1_1"))
  uis.Light2_1 = GetRogueBuild01_InsideMapEvent_LineDotUis(ui:GetChild("Light2_1"))
  uis.Light2_2 = GetRogueBuild01_InsideMapEvent_LineDotUis(ui:GetChild("Light2_2"))
```

---

## Rouge/RogueBuild01_InsideMapEvent_LineDotByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideMapEvent_LineDotUis
**Snippet:**
```lua
function GetRogueBuild01_InsideMapEvent_LineDotUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideMapEvent_Line_10001ByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideMapEvent_Line_10001Uis
**Snippet:**
```lua
function GetRogueBuild01_InsideMapEvent_Line_10001Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideMapEvent_PlotByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideMapEvent_PlotUis
**Requires:**
- RogueBuild01_InsideMapEvent_LineDotByName
**Snippet:**
```lua
require("RogueBuild01_InsideMapEvent_LineDotByName")

function GetRogueBuild01_InsideMapEvent_PlotUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.Light1_1 = GetRogueBuild01_InsideMapEvent_LineDotUis(ui:GetChild("Light1_1"))
  uis.Light2_1 = GetRogueBuild01_InsideMapEvent_LineDotUis(ui:GetChild("Light2_1"))
  uis.Light2_2 = GetRogueBuild01_InsideMapEvent_LineDotUis(ui:GetChild("Light2_2"))
```

---

## Rouge/RogueBuild01_InsideMapEvent_ShopByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideMapEvent_ShopUis
**Requires:**
- RogueBuild01_InsideMapEvent_LineDotByName
**Snippet:**
```lua
require("RogueBuild01_InsideMapEvent_LineDotByName")

function GetRogueBuild01_InsideMapEvent_ShopUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.Light1_1 = GetRogueBuild01_InsideMapEvent_LineDotUis(ui:GetChild("Light1_1"))
  uis.Light2_1 = GetRogueBuild01_InsideMapEvent_LineDotUis(ui:GetChild("Light2_1"))
  uis.Light2_2 = GetRogueBuild01_InsideMapEvent_LineDotUis(ui:GetChild("Light2_2"))
```

---

## Rouge/RogueBuild01_InsideMapLayerByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideMapLayerUis
**Requires:**
- RogueBuild01_InsideMapLayer_Dot1ByName
- RogueBuild01_InsideMapLayer_Dot2ByName
- RogueBuild01_InsideMapLayer_Dot3ByName
- RogueBuild01_InsideMapLayer_Dot4ByName
- RogueBuild01_InsideMapLayer_Dot5ByName
- RogueBuild01_InsideMapLayer_DotSpByName
**Snippet:**
```lua
require("RogueBuild01_InsideMapLayer_Dot1ByName")
require("RogueBuild01_InsideMapLayer_Dot2ByName")
require("RogueBuild01_InsideMapLayer_Dot3ByName")
require("RogueBuild01_InsideMapLayer_Dot4ByName")
require("RogueBuild01_InsideMapLayer_Dot5ByName")
require("RogueBuild01_InsideMapLayer_DotSpByName")

function GetRogueBuild01_InsideMapLayerUis(ui)
  local uis = {}
  uis.Dot1 = GetRogueBuild01_InsideMapLayer_Dot1Uis(ui:GetChild("Dot1"))
```

---

## Rouge/RogueBuild01_InsideMapLayer_Dot1ByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideMapLayer_Dot1Uis
**Snippet:**
```lua
function GetRogueBuild01_InsideMapLayer_Dot1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideMapLayer_Dot2ByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideMapLayer_Dot2Uis
**Snippet:**
```lua
function GetRogueBuild01_InsideMapLayer_Dot2Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideMapLayer_Dot3ByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideMapLayer_Dot3Uis
**Snippet:**
```lua
function GetRogueBuild01_InsideMapLayer_Dot3Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideMapLayer_Dot4ByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideMapLayer_Dot4Uis
**Snippet:**
```lua
function GetRogueBuild01_InsideMapLayer_Dot4Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideMapLayer_Dot5ByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideMapLayer_Dot5Uis
**Snippet:**
```lua
function GetRogueBuild01_InsideMapLayer_Dot5Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideMapLayer_DotSpByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideMapLayer_DotSpUis
**Snippet:**
```lua
function GetRogueBuild01_InsideMapLayer_DotSpUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideMapWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideMapWindowUis
**Requires:**
- RogueBuild01_InsideMapByName
**Snippet:**
```lua
require("RogueBuild01_InsideMapByName")

function GetRogueBuild01_InsideMapWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_InsideMapUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideMidAni_01ByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideMidAni_01Uis
**Snippet:**
```lua
function GetRogueBuild01_InsideMidAni_01Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideMidByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideMidUis
**Requires:**
- RogueBuild01_InsideMidAni_01ByName
**Snippet:**
```lua
require("RogueBuild01_InsideMidAni_01ByName")

function GetRogueBuild01_InsideMidUis(ui)
  local uis = {}
  uis.n003 = GetRogueBuild01_InsideMidAni_01Uis(ui:GetChild("n003"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_InsideMidWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideMidWindowUis
**Requires:**
- RogueBuild01_InsideMidByName
**Snippet:**
```lua
require("RogueBuild01_InsideMidByName")

function GetRogueBuild01_InsideMidWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_InsideMidUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsidePlotEndByName.lua.lua
**Functions:**
- GetRogueBuild01_InsidePlotEndUis
**Requires:**
- CommonResource_BackGroundByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")

function GetRogueBuild01_InsidePlotEndUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.WordList = ui:GetChild("WordList")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
```

---

## Rouge/RogueBuild01_InsidePlotEndWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_InsidePlotEndWindowUis
**Requires:**
- RogueBuild01_InsidePlotEndByName
**Snippet:**
```lua
require("RogueBuild01_InsidePlotEndByName")

function GetRogueBuild01_InsidePlotEndWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_InsidePlotEndUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsidePlotEnd_CloseBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_InsidePlotEnd_CloseBtnUis
**Snippet:**
```lua
function GetRogueBuild01_InsidePlotEnd_CloseBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsidePlotEnd_WordByName.lua.lua
**Functions:**
- GetRogueBuild01_InsidePlotEnd_WordUis
**Snippet:**
```lua
function GetRogueBuild01_InsidePlotEnd_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsidePlotEventByName.lua.lua
**Functions:**
- GetRogueBuild01_InsidePlotEventUis
**Requires:**
- CommonResource_BackGroundByName
- RogueBuild01_PlotEvent_WordByName
- RogueBuild01_InsideMapBottomByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("RogueBuild01_PlotEvent_WordByName")
require("RogueBuild01_InsideMapBottomByName")

function GetRogueBuild01_InsidePlotEventUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.AssetsList = ui:GetChild("AssetsList")
  uis.Word = GetRogueBuild01_PlotEvent_WordUis(ui:GetChild("Word"))
```

---

## Rouge/RogueBuild01_InsidePlotEventWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_InsidePlotEventWindowUis
**Requires:**
- RogueBuild01_InsidePlotEventByName
**Snippet:**
```lua
require("RogueBuild01_InsidePlotEventByName")

function GetRogueBuild01_InsidePlotEventWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_InsidePlotEventUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideSacredByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideSacredUis
**Requires:**
- CommonResource_PopupBgByName
- RogueBuild01_Sacred_TipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("RogueBuild01_Sacred_TipsByName")

function GetRogueBuild01_InsideSacredUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.Tips = GetRogueBuild01_Sacred_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideSacredWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideSacredWindowUis
**Requires:**
- RogueBuild01_InsideSacredByName
**Snippet:**
```lua
require("RogueBuild01_InsideSacredByName")

function GetRogueBuild01_InsideSacredWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_InsideSacredUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideShopByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideShopUis
**Requires:**
- CommonResource_BackGroundByName
- RogueBuild01_InsideMapBottomByName
- RogueBuild01_Shop_TimesByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("RogueBuild01_InsideMapBottomByName")
require("RogueBuild01_Shop_TimesByName")

function GetRogueBuild01_InsideShopUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.OutBtn = ui:GetChild("OutBtn")
  uis.Botton = GetRogueBuild01_InsideMapBottomUis(ui:GetChild("Botton"))
  uis.AssetsList = ui:GetChild("AssetsList")
```

---

## Rouge/RogueBuild01_InsideShopWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideShopWindowUis
**Requires:**
- RogueBuild01_InsideShopByName
**Snippet:**
```lua
require("RogueBuild01_InsideShopByName")

function GetRogueBuild01_InsideShopWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_InsideShopUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideSmallByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideSmallUis
**Snippet:**
```lua
function GetRogueBuild01_InsideSmallUis(ui)
  local uis = {}
  
  uis.TipsList = ui:GetChild("TipsList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideSmallWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideSmallWindowUis
**Requires:**
- RogueBuild01_InsideSmallByName
**Snippet:**
```lua
require("RogueBuild01_InsideSmallByName")

function GetRogueBuild01_InsideSmallWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_InsideSmallUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideStartByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideStartUis
**Requires:**
- RogueBuild01_InsideStart_AniByName
**Snippet:**
```lua
require("RogueBuild01_InsideStart_AniByName")

function GetRogueBuild01_InsideStartUis(ui)
  local uis = {}
  uis.Ani = GetRogueBuild01_InsideStart_AniUis(ui:GetChild("Ani"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideStartChoiceByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideStartChoiceUis
**Requires:**
- CommonResource_BackGroundByName
- RogueBuild01_InsideStartChoiceTitleByName
- RogueBuild01_InsideMapBottomByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("RogueBuild01_InsideStartChoiceTitleByName")
require("RogueBuild01_InsideMapBottomByName")

function GetRogueBuild01_InsideStartChoiceUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Title = GetRogueBuild01_InsideStartChoiceTitleUis(ui:GetChild("Title"))
  uis.NextBtn = ui:GetChild("NextBtn")
  uis.ItemList = ui:GetChild("ItemList")
```

---

## Rouge/RogueBuild01_InsideStartChoiceNextBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideStartChoiceNextBtnUis
**Snippet:**
```lua
function GetRogueBuild01_InsideStartChoiceNextBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideStartChoiceTitleByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideStartChoiceTitleUis
**Snippet:**
```lua
function GetRogueBuild01_InsideStartChoiceTitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideStartChoiceWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideStartChoiceWindowUis
**Requires:**
- RogueBuild01_InsideStartChoiceByName
**Snippet:**
```lua
require("RogueBuild01_InsideStartChoiceByName")

function GetRogueBuild01_InsideStartChoiceWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_InsideStartChoiceUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideStartWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideStartWindowUis
**Requires:**
- RogueBuild01_InsideStartByName
**Snippet:**
```lua
require("RogueBuild01_InsideStartByName")

function GetRogueBuild01_InsideStartWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_InsideStartUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_InsideStart_AniByName.lua.lua
**Functions:**
- GetRogueBuild01_InsideStart_AniUis
**Snippet:**
```lua
function GetRogueBuild01_InsideStart_AniUis(ui)
  local uis = {}
  
  uis.TitleLoader = ui:GetChild("TitleLoader")
  uis.TitleHolder = ui:GetChild("TitleHolder")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ItemLook_SacredConditionByName.lua.lua
**Functions:**
- GetRogueBuild01_ItemLook_SacredConditionUis
**Snippet:**
```lua
function GetRogueBuild01_ItemLook_SacredConditionUis(ui)
  local uis = {}
  
  uis.ItemList = ui:GetChild("ItemList")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ItemLook_SacredConditionItemBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_ItemLook_SacredConditionItemBtnUis
**Snippet:**
```lua
function GetRogueBuild01_ItemLook_SacredConditionItemBtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ItemLook_SacredItemAniByName.lua.lua
**Functions:**
- GetRogueBuild01_ItemLook_SacredItemAniUis
**Requires:**
- RogueBuild01_ItemLook_SacredItemByName
**Snippet:**
```lua
require("RogueBuild01_ItemLook_SacredItemByName")

function GetRogueBuild01_ItemLook_SacredItemAniUis(ui)
  local uis = {}
  uis.Item = GetRogueBuild01_ItemLook_SacredItemUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ItemLook_SacredItemByName.lua.lua
**Functions:**
- GetRogueBuild01_ItemLook_SacredItemUis
**Requires:**
- RogueBuild01_ItemLook_SacredStateByName
- RogueBuild01_BookSacredHeadByName
- RogueBuild01_ItemLook_SacredConditionByName
**Snippet:**
```lua
require("RogueBuild01_ItemLook_SacredStateByName")
require("RogueBuild01_BookSacredHeadByName")
require("RogueBuild01_ItemLook_SacredConditionByName")

function GetRogueBuild01_ItemLook_SacredItemUis(ui)
  local uis = {}
  uis.State = GetRogueBuild01_ItemLook_SacredStateUis(ui:GetChild("State"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.Head = GetRogueBuild01_BookSacredHeadUis(ui:GetChild("Head"))
```

---

## Rouge/RogueBuild01_ItemLook_SacredStateByName.lua.lua
**Functions:**
- GetRogueBuild01_ItemLook_SacredStateUis
**Snippet:**
```lua
function GetRogueBuild01_ItemLook_SacredStateUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ItemLook_SacredTipsByName.lua.lua
**Functions:**
- GetRogueBuild01_ItemLook_SacredTipsUis
**Snippet:**
```lua
function GetRogueBuild01_ItemLook_SacredTipsUis(ui)
  local uis = {}
  
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ItemLook_SacredWordByName.lua.lua
**Functions:**
- GetRogueBuild01_ItemLook_SacredWordUis
**Snippet:**
```lua
function GetRogueBuild01_ItemLook_SacredWordUis(ui)
  local uis = {}
  
  uis.EffectTxt = ui:GetChild("EffectTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ItemLook_Tab01BtnByName.lua.lua
**Functions:**
- GetRogueBuild01_ItemLook_Tab01BtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetRogueBuild01_ItemLook_Tab01BtnUis(ui)
  local uis = {}
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_ItemLook_Tab02BtnByName.lua.lua
**Functions:**
- GetRogueBuild01_ItemLook_Tab02BtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetRogueBuild01_ItemLook_Tab02BtnUis(ui)
  local uis = {}
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_ItemLook_TabRegionByName.lua.lua
**Functions:**
- GetRogueBuild01_ItemLook_TabRegionUis
**Snippet:**
```lua
function GetRogueBuild01_ItemLook_TabRegionUis(ui)
  local uis = {}
  
  uis.Tab01Btn = ui:GetChild("Tab01Btn")
  uis.Tab02Btn = ui:GetChild("Tab02Btn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ItemLook_TreasureChoiceByName.lua.lua
**Functions:**
- GetRogueBuild01_ItemLook_TreasureChoiceUis
**Requires:**
- RogueBuild01_BookTreasureChoice2ByName
- RogueBuild01_BookTreasureChoice3ByName
**Snippet:**
```lua
require("RogueBuild01_BookTreasureChoice2ByName")
require("RogueBuild01_BookTreasureChoice3ByName")

function GetRogueBuild01_ItemLook_TreasureChoiceUis(ui)
  local uis = {}
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.Choice2 = GetRogueBuild01_BookTreasureChoice2Uis(ui:GetChild("Choice2"))
  uis.Choice3 = GetRogueBuild01_BookTreasureChoice3Uis(ui:GetChild("Choice3"))
  uis.ResetBtn = ui:GetChild("ResetBtn")
  uis.root = ui
```

---

## Rouge/RogueBuild01_ItemLook_TreasureItemAniByName.lua.lua
**Functions:**
- GetRogueBuild01_ItemLook_TreasureItemAniUis
**Snippet:**
```lua
function GetRogueBuild01_ItemLook_TreasureItemAniUis(ui)
  local uis = {}
  
  uis.ItemBtn = ui:GetChild("ItemBtn")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ItemLook_TreasureItemBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_ItemLook_TreasureItemBtnUis
**Requires:**
- RogueBuild01_TreasureTypeByName
- RogueBuild01_TreasureLevelByName
**Snippet:**
```lua
require("RogueBuild01_TreasureTypeByName")
require("RogueBuild01_TreasureLevelByName")

function GetRogueBuild01_ItemLook_TreasureItemBtnUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.IDTxt = ui:GetChild("IDTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Type = GetRogueBuild01_TreasureTypeUis(ui:GetChild("Type"))
  uis.Level = GetRogueBuild01_TreasureLevelUis(ui:GetChild("Level"))
```

---

## Rouge/RogueBuild01_ItemLook_TreasureTipsByName.lua.lua
**Functions:**
- GetRogueBuild01_ItemLook_TreasureTipsUis
**Requires:**
- RogueBuild01_BookTreasureInfoByName
- RogueBuild01_ItemLook_TreasureChoiceByName
**Snippet:**
```lua
require("RogueBuild01_BookTreasureInfoByName")
require("RogueBuild01_ItemLook_TreasureChoiceByName")

function GetRogueBuild01_ItemLook_TreasureTipsUis(ui)
  local uis = {}
  uis.Info = GetRogueBuild01_BookTreasureInfoUis(ui:GetChild("Info"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.ScreenBtn = ui:GetChild("ScreenBtn")
  uis.Choice = GetRogueBuild01_ItemLook_TreasureChoiceUis(ui:GetChild("Choice"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## Rouge/RogueBuild01_LetterChatHeadBgByName.lua.lua
**Functions:**
- GetRogueBuild01_LetterChatHeadBgUis
**Snippet:**
```lua
function GetRogueBuild01_LetterChatHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_LetterChatHeadByName.lua.lua
**Functions:**
- GetRogueBuild01_LetterChatHeadUis
**Requires:**
- RogueBuild01_LetterChatHeadBgByName
**Snippet:**
```lua
require("RogueBuild01_LetterChatHeadBgByName")

function GetRogueBuild01_LetterChatHeadUis(ui)
  local uis = {}
  uis.Bg = GetRogueBuild01_LetterChatHeadBgUis(ui:GetChild("Bg"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_LetterChatWordByName.lua.lua
**Functions:**
- GetRogueBuild01_LetterChatWordUis
**Requires:**
- RogueBuild01_LetterChatHeadByName
**Snippet:**
```lua
require("RogueBuild01_LetterChatHeadByName")

function GetRogueBuild01_LetterChatWordUis(ui)
  local uis = {}
  uis.Head = GetRogueBuild01_LetterChatHeadUis(ui:GetChild("Head"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_LetterRegionByName.lua.lua
**Functions:**
- GetRogueBuild01_LetterRegionUis
**Snippet:**
```lua
function GetRogueBuild01_LetterRegionUis(ui)
  local uis = {}
  
  uis.ChatList = ui:GetChild("ChatList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_LetterRewardByName.lua.lua
**Functions:**
- GetRogueBuild01_LetterRewardUis
**Requires:**
- CommonResource_BackGroundByName
- RogueBuild01_DayRewardByName
- RogueBuild01_AchieveRewardByName
- RogueBuild01_LetterRewardTabRegionByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("RogueBuild01_DayRewardByName")
require("RogueBuild01_AchieveRewardByName")
require("RogueBuild01_LetterRewardTabRegionByName")
require("CommonResource_CurrencyReturnByName")

function GetRogueBuild01_LetterRewardUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.DayReward = GetRogueBuild01_DayRewardUis(ui:GetChild("DayReward"))
```

---

## Rouge/RogueBuild01_LetterRewardTab1BtnByName.lua.lua
**Functions:**
- GetRogueBuild01_LetterRewardTab1BtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetRogueBuild01_LetterRewardTab1BtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_LetterRewardTab2BtnByName.lua.lua
**Functions:**
- GetRogueBuild01_LetterRewardTab2BtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetRogueBuild01_LetterRewardTab2BtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_LetterRewardTabRegionByName.lua.lua
**Functions:**
- GetRogueBuild01_LetterRewardTabRegionUis
**Snippet:**
```lua
function GetRogueBuild01_LetterRewardTabRegionUis(ui)
  local uis = {}
  
  uis.Tab1Btn = ui:GetChild("Tab1Btn")
  uis.Tab2Btn = ui:GetChild("Tab2Btn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_LetterRewardWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_LetterRewardWindowUis
**Requires:**
- RogueBuild01_LetterRewardByName
**Snippet:**
```lua
require("RogueBuild01_LetterRewardByName")

function GetRogueBuild01_LetterRewardWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_LetterRewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_LetterTipsByName.lua.lua
**Functions:**
- GetRogueBuild01_LetterTipsUis
**Requires:**
- CommonResource_PopupBgByName
- RogueBuild01_LetterRegionByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("RogueBuild01_LetterRegionByName")

function GetRogueBuild01_LetterTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.LetterRegion = GetRogueBuild01_LetterRegionUis(ui:GetChild("LetterRegion"))
  uis.root = ui
```

---

## Rouge/RogueBuild01_LetterTipsWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_LetterTipsWindowUis
**Requires:**
- RogueBuild01_LetterTipsByName
**Snippet:**
```lua
require("RogueBuild01_LetterTipsByName")

function GetRogueBuild01_LetterTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_LetterTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_LetterTipsWordByName.lua.lua
**Functions:**
- GetRogueBuild01_LetterTipsWordUis
**Snippet:**
```lua
function GetRogueBuild01_LetterTipsWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_MapListByName.lua.lua
**Functions:**
- GetRogueBuild01_MapListUis
**Snippet:**
```lua
function GetRogueBuild01_MapListUis(ui)
  local uis = {}
  
  uis.MapList = ui:GetChild("MapList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Map_101ByName.lua.lua
**Functions:**
- GetRogueBuild01_Map_101Uis
**Requires:**
- RogueBuild01_InsideMapEvent_Line_10001ByName
- RogueBuild01_InsideMapEvent_Battle1ByName
- RogueBuild01_InsideMapEvent_PlotByName
- RogueBuild01_InsideMapEvent_ShopByName
**Snippet:**
```lua
require("RogueBuild01_InsideMapEvent_Line_10001ByName")
require("RogueBuild01_InsideMapEvent_Battle1ByName")
require("RogueBuild01_InsideMapEvent_PlotByName")
require("RogueBuild01_InsideMapEvent_ShopByName")

function GetRogueBuild01_Map_101Uis(ui)
  local uis = {}
  uis.n24 = GetRogueBuild01_InsideMapEvent_Line_10001Uis(ui:GetChild("n24"))
  uis.n25 = GetRogueBuild01_InsideMapEvent_Line_10001Uis(ui:GetChild("n25"))
  uis.n26 = GetRogueBuild01_InsideMapEvent_Line_10001Uis(ui:GetChild("n26"))
```

---

## Rouge/RogueBuild01_Map_102ByName.lua.lua
**Functions:**
- GetRogueBuild01_Map_102Uis
**Requires:**
- RogueBuild01_InsideMapEvent_Line_10001ByName
- RogueBuild01_InsideMapEvent_Battle1ByName
- RogueBuild01_InsideMapEvent_PlotByName
- RogueBuild01_InsideMapEvent_ShopByName
**Snippet:**
```lua
require("RogueBuild01_InsideMapEvent_Line_10001ByName")
require("RogueBuild01_InsideMapEvent_Battle1ByName")
require("RogueBuild01_InsideMapEvent_PlotByName")
require("RogueBuild01_InsideMapEvent_ShopByName")

function GetRogueBuild01_Map_102Uis(ui)
  local uis = {}
  uis.n27 = GetRogueBuild01_InsideMapEvent_Line_10001Uis(ui:GetChild("n27"))
  uis.n28 = GetRogueBuild01_InsideMapEvent_Line_10001Uis(ui:GetChild("n28"))
  uis.n29 = GetRogueBuild01_InsideMapEvent_Line_10001Uis(ui:GetChild("n29"))
```

---

## Rouge/RogueBuild01_Map_103ByName.lua.lua
**Functions:**
- GetRogueBuild01_Map_103Uis
**Requires:**
- RogueBuild01_InsideMapEvent_Line_10001ByName
- RogueBuild01_InsideMapEvent_Battle1ByName
- RogueBuild01_InsideMapEvent_PlotByName
- RogueBuild01_InsideMapEvent_ShopByName
**Snippet:**
```lua
require("RogueBuild01_InsideMapEvent_Line_10001ByName")
require("RogueBuild01_InsideMapEvent_Battle1ByName")
require("RogueBuild01_InsideMapEvent_PlotByName")
require("RogueBuild01_InsideMapEvent_ShopByName")

function GetRogueBuild01_Map_103Uis(ui)
  local uis = {}
  uis.n29 = GetRogueBuild01_InsideMapEvent_Line_10001Uis(ui:GetChild("n29"))
  uis.n30 = GetRogueBuild01_InsideMapEvent_Line_10001Uis(ui:GetChild("n30"))
  uis.n31 = GetRogueBuild01_InsideMapEvent_Line_10001Uis(ui:GetChild("n31"))
```

---

## Rouge/RogueBuild01_Map_1ByName.lua.lua
**Functions:**
- GetRogueBuild01_Map_1Uis
**Snippet:**
```lua
function GetRogueBuild01_Map_1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Map_201ByName.lua.lua
**Functions:**
- GetRogueBuild01_Map_201Uis
**Requires:**
- RogueBuild01_InsideMapEvent_Battle1ByName
- RogueBuild01_InsideMapEvent_PlotByName
- RogueBuild01_InsideMapEvent_ShopByName
- RogueBuild01_InsideMapEvent_CampByName
**Snippet:**
```lua
require("RogueBuild01_InsideMapEvent_Battle1ByName")
require("RogueBuild01_InsideMapEvent_PlotByName")
require("RogueBuild01_InsideMapEvent_ShopByName")
require("RogueBuild01_InsideMapEvent_CampByName")

function GetRogueBuild01_Map_201Uis(ui)
  local uis = {}
  uis.Dot_A_01 = GetRogueBuild01_InsideMapEvent_Battle1Uis(ui:GetChild("Dot_A_01"))
  uis.Dot_B_01 = GetRogueBuild01_InsideMapEvent_PlotUis(ui:GetChild("Dot_B_01"))
  uis.Dot_B_02 = GetRogueBuild01_InsideMapEvent_Battle1Uis(ui:GetChild("Dot_B_02"))
```

---

## Rouge/RogueBuild01_Map_202ByName.lua.lua
**Functions:**
- GetRogueBuild01_Map_202Uis
**Requires:**
- RogueBuild01_InsideMapEvent_PlotByName
- RogueBuild01_InsideMapEvent_Battle1ByName
- RogueBuild01_InsideMapEvent_Battle2ByName
- RogueBuild01_InsideMapEvent_ShopByName
- RogueBuild01_InsideMapEvent_CampByName
**Snippet:**
```lua
require("RogueBuild01_InsideMapEvent_PlotByName")
require("RogueBuild01_InsideMapEvent_Battle1ByName")
require("RogueBuild01_InsideMapEvent_Battle2ByName")
require("RogueBuild01_InsideMapEvent_ShopByName")
require("RogueBuild01_InsideMapEvent_CampByName")

function GetRogueBuild01_Map_202Uis(ui)
  local uis = {}
  uis.Dot_A_01 = GetRogueBuild01_InsideMapEvent_PlotUis(ui:GetChild("Dot_A_01"))
  uis.Dot_A_02 = GetRogueBuild01_InsideMapEvent_Battle1Uis(ui:GetChild("Dot_A_02"))
```

---

## Rouge/RogueBuild01_Map_203ByName.lua.lua
**Functions:**
- GetRogueBuild01_Map_203Uis
**Requires:**
- RogueBuild01_InsideMapEvent_Battle1ByName
- RogueBuild01_InsideMapEvent_Battle2ByName
- RogueBuild01_InsideMapEvent_PlotByName
- RogueBuild01_InsideMapEvent_ShopByName
- RogueBuild01_InsideMapEvent_CampByName
**Snippet:**
```lua
require("RogueBuild01_InsideMapEvent_Battle1ByName")
require("RogueBuild01_InsideMapEvent_Battle2ByName")
require("RogueBuild01_InsideMapEvent_PlotByName")
require("RogueBuild01_InsideMapEvent_ShopByName")
require("RogueBuild01_InsideMapEvent_CampByName")

function GetRogueBuild01_Map_203Uis(ui)
  local uis = {}
  uis.Dot_A_01 = GetRogueBuild01_InsideMapEvent_Battle1Uis(ui:GetChild("Dot_A_01"))
  uis.Dot_B_01 = GetRogueBuild01_InsideMapEvent_Battle2Uis(ui:GetChild("Dot_B_01"))
```

---

## Rouge/RogueBuild01_Map_2ByName.lua.lua
**Functions:**
- GetRogueBuild01_Map_2Uis
**Snippet:**
```lua
function GetRogueBuild01_Map_2Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Map_301ByName.lua.lua
**Functions:**
- GetRogueBuild01_Map_301Uis
**Requires:**
- RogueBuild01_InsideMapEvent_PlotByName
- RogueBuild01_InsideMapEvent_Battle1ByName
- RogueBuild01_InsideMapEvent_Battle2ByName
- RogueBuild01_InsideMapEvent_ShopByName
- RogueBuild01_InsideMapEvent_CampByName
- RogueBuild01_InsideMapEvent_Battle3ByName
**Snippet:**
```lua
require("RogueBuild01_InsideMapEvent_PlotByName")
require("RogueBuild01_InsideMapEvent_Battle1ByName")
require("RogueBuild01_InsideMapEvent_Battle2ByName")
require("RogueBuild01_InsideMapEvent_ShopByName")
require("RogueBuild01_InsideMapEvent_CampByName")
require("RogueBuild01_InsideMapEvent_Battle3ByName")

function GetRogueBuild01_Map_301Uis(ui)
  local uis = {}
  uis.Dot_A_01 = GetRogueBuild01_InsideMapEvent_PlotUis(ui:GetChild("Dot_A_01"))
```

---

## Rouge/RogueBuild01_Map_302ByName.lua.lua
**Functions:**
- GetRogueBuild01_Map_302Uis
**Requires:**
- RogueBuild01_InsideMapEvent_PlotByName
- RogueBuild01_InsideMapEvent_Battle2ByName
- RogueBuild01_InsideMapEvent_Battle1ByName
- RogueBuild01_InsideMapEvent_CampByName
- RogueBuild01_InsideMapEvent_ShopByName
- RogueBuild01_InsideMapEvent_Battle3ByName
**Snippet:**
```lua
require("RogueBuild01_InsideMapEvent_PlotByName")
require("RogueBuild01_InsideMapEvent_Battle2ByName")
require("RogueBuild01_InsideMapEvent_Battle1ByName")
require("RogueBuild01_InsideMapEvent_CampByName")
require("RogueBuild01_InsideMapEvent_ShopByName")
require("RogueBuild01_InsideMapEvent_Battle3ByName")

function GetRogueBuild01_Map_302Uis(ui)
  local uis = {}
  uis.Dot_A_01 = GetRogueBuild01_InsideMapEvent_PlotUis(ui:GetChild("Dot_A_01"))
```

---

## Rouge/RogueBuild01_Map_303ByName.lua.lua
**Functions:**
- GetRogueBuild01_Map_303Uis
**Requires:**
- RogueBuild01_InsideMapEvent_PlotByName
- RogueBuild01_InsideMapEvent_Battle1ByName
- RogueBuild01_InsideMapEvent_Battle2ByName
- RogueBuild01_InsideMapEvent_ShopByName
- RogueBuild01_InsideMapEvent_CampByName
- RogueBuild01_InsideMapEvent_Battle3ByName
**Snippet:**
```lua
require("RogueBuild01_InsideMapEvent_PlotByName")
require("RogueBuild01_InsideMapEvent_Battle1ByName")
require("RogueBuild01_InsideMapEvent_Battle2ByName")
require("RogueBuild01_InsideMapEvent_ShopByName")
require("RogueBuild01_InsideMapEvent_CampByName")
require("RogueBuild01_InsideMapEvent_Battle3ByName")

function GetRogueBuild01_Map_303Uis(ui)
  local uis = {}
  uis.Dot_A_01 = GetRogueBuild01_InsideMapEvent_PlotUis(ui:GetChild("Dot_A_01"))
```

---

## Rouge/RogueBuild01_Map_3ByName.lua.lua
**Functions:**
- GetRogueBuild01_Map_3Uis
**Snippet:**
```lua
function GetRogueBuild01_Map_3Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Map_401ByName.lua.lua
**Functions:**
- GetRogueBuild01_Map_401Uis
**Requires:**
- RogueBuild01_InsideMapEvent_PlotByName
- RogueBuild01_InsideMapEvent_Battle1ByName
- RogueBuild01_InsideMapEvent_Battle2ByName
- RogueBuild01_InsideMapEvent_CampByName
- RogueBuild01_InsideMapEvent_ShopByName
**Snippet:**
```lua
require("RogueBuild01_InsideMapEvent_PlotByName")
require("RogueBuild01_InsideMapEvent_Battle1ByName")
require("RogueBuild01_InsideMapEvent_Battle2ByName")
require("RogueBuild01_InsideMapEvent_CampByName")
require("RogueBuild01_InsideMapEvent_ShopByName")

function GetRogueBuild01_Map_401Uis(ui)
  local uis = {}
  uis.Dot_A_01 = GetRogueBuild01_InsideMapEvent_PlotUis(ui:GetChild("Dot_A_01"))
  uis.Dot_B_01 = GetRogueBuild01_InsideMapEvent_Battle1Uis(ui:GetChild("Dot_B_01"))
```

---

## Rouge/RogueBuild01_Map_402ByName.lua.lua
**Functions:**
- GetRogueBuild01_Map_402Uis
**Requires:**
- RogueBuild01_InsideMapEvent_Battle1ByName
- RogueBuild01_InsideMapEvent_Battle2ByName
- RogueBuild01_InsideMapEvent_PlotByName
- RogueBuild01_InsideMapEvent_CampByName
- RogueBuild01_InsideMapEvent_ShopByName
**Snippet:**
```lua
require("RogueBuild01_InsideMapEvent_Battle1ByName")
require("RogueBuild01_InsideMapEvent_Battle2ByName")
require("RogueBuild01_InsideMapEvent_PlotByName")
require("RogueBuild01_InsideMapEvent_CampByName")
require("RogueBuild01_InsideMapEvent_ShopByName")

function GetRogueBuild01_Map_402Uis(ui)
  local uis = {}
  uis.Dot_A_01 = GetRogueBuild01_InsideMapEvent_Battle1Uis(ui:GetChild("Dot_A_01"))
  uis.Dot_B_01 = GetRogueBuild01_InsideMapEvent_Battle1Uis(ui:GetChild("Dot_B_01"))
```

---

## Rouge/RogueBuild01_Map_4ByName.lua.lua
**Functions:**
- GetRogueBuild01_Map_4Uis
**Snippet:**
```lua
function GetRogueBuild01_Map_4Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Map_501ByName.lua.lua
**Functions:**
- GetRogueBuild01_Map_501Uis
**Requires:**
- RogueBuild01_InsideMapEvent_PlotByName
- RogueBuild01_InsideMapEvent_Battle1ByName
- RogueBuild01_InsideMapEvent_Battle2ByName
- RogueBuild01_InsideMapEvent_CampByName
- RogueBuild01_InsideMapEvent_ShopByName
- RogueBuild01_InsideMapEvent_Battle3ByName
**Snippet:**
```lua
require("RogueBuild01_InsideMapEvent_PlotByName")
require("RogueBuild01_InsideMapEvent_Battle1ByName")
require("RogueBuild01_InsideMapEvent_Battle2ByName")
require("RogueBuild01_InsideMapEvent_CampByName")
require("RogueBuild01_InsideMapEvent_ShopByName")
require("RogueBuild01_InsideMapEvent_Battle3ByName")

function GetRogueBuild01_Map_501Uis(ui)
  local uis = {}
  uis.Dot_A_01 = GetRogueBuild01_InsideMapEvent_PlotUis(ui:GetChild("Dot_A_01"))
```

---

## Rouge/RogueBuild01_Map_5ByName.lua.lua
**Functions:**
- GetRogueBuild01_Map_5Uis
**Snippet:**
```lua
function GetRogueBuild01_Map_5Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Map_6ByName.lua.lua
**Functions:**
- GetRogueBuild01_Map_6Uis
**Snippet:**
```lua
function GetRogueBuild01_Map_6Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Map_S001ByName.lua.lua
**Functions:**
- GetRogueBuild01_Map_S001Uis
**Requires:**
- RogueBuild01_InsideMapEvent_Battle1ByName
- RogueBuild01_InsideMapEvent_PlotByName
- RogueBuild01_InsideMapEvent_CampByName
- RogueBuild01_InsideMapEvent_Battle2ByName
- RogueBuild01_InsideMapEvent_Battle3ByName
**Snippet:**
```lua
require("RogueBuild01_InsideMapEvent_Battle1ByName")
require("RogueBuild01_InsideMapEvent_PlotByName")
require("RogueBuild01_InsideMapEvent_CampByName")
require("RogueBuild01_InsideMapEvent_Battle2ByName")
require("RogueBuild01_InsideMapEvent_Battle3ByName")

function GetRogueBuild01_Map_S001Uis(ui)
  local uis = {}
  uis.Dot_A_01 = GetRogueBuild01_InsideMapEvent_Battle1Uis(ui:GetChild("Dot_A_01"))
  uis.Dot_B_01 = GetRogueBuild01_InsideMapEvent_PlotUis(ui:GetChild("Dot_B_01"))
```

---

## Rouge/RogueBuild01_PlotEvent_NextBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_PlotEvent_NextBtnUis
**Snippet:**
```lua
function GetRogueBuild01_PlotEvent_NextBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_PlotEvent_OptionAniByName.lua.lua
**Functions:**
- GetRogueBuild01_PlotEvent_OptionAniUis
**Requires:**
- RogueBuild01_PlotEvent_OptionByName
**Snippet:**
```lua
require("RogueBuild01_PlotEvent_OptionByName")

function GetRogueBuild01_PlotEvent_OptionAniUis(ui)
  local uis = {}
  uis.Option = GetRogueBuild01_PlotEvent_OptionUis(ui:GetChild("Option"))
  uis.choiceCtr = ui:GetController("choice")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_PlotEvent_OptionByName.lua.lua
**Functions:**
- GetRogueBuild01_PlotEvent_OptionUis
**Snippet:**
```lua
function GetRogueBuild01_PlotEvent_OptionUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.LookBtn = ui:GetChild("LookBtn")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ChoiceBtn = ui:GetChild("ChoiceBtn")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.choiceCtr = ui:GetController("choice")
```

---

## Rouge/RogueBuild01_PlotEvent_OptionChoiceBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_PlotEvent_OptionChoiceBtnUis
**Snippet:**
```lua
function GetRogueBuild01_PlotEvent_OptionChoiceBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_PlotEvent_OptionLookBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_PlotEvent_OptionLookBtnUis
**Snippet:**
```lua
function GetRogueBuild01_PlotEvent_OptionLookBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_PlotEvent_WordByName.lua.lua
**Functions:**
- GetRogueBuild01_PlotEvent_WordUis
**Snippet:**
```lua
function GetRogueBuild01_PlotEvent_WordUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_RogueByName.lua.lua
**Functions:**
- GetRogueBuild01_RogueUis
**Requires:**
- CommonResource_BackGroundByName
- RogueBuild01_CoverTitleByName
- RogueBuild01_CoverLayersByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("RogueBuild01_CoverTitleByName")
require("RogueBuild01_CoverLayersByName")
require("CommonResource_CurrencyReturnByName")

function GetRogueBuild01_RogueUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.CoverTitle = GetRogueBuild01_CoverTitleUis(ui:GetChild("CoverTitle"))
  uis.CoverStartBtn = ui:GetChild("CoverStartBtn")
```

---

## Rouge/RogueBuild01_RogueWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_RogueWindowUis
**Requires:**
- RogueBuild01_RogueByName
**Snippet:**
```lua
require("RogueBuild01_RogueByName")

function GetRogueBuild01_RogueWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_RogueUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Sacred_TipsByName.lua.lua
**Functions:**
- GetRogueBuild01_Sacred_TipsUis
**Requires:**
- RogueBuild01_Sacred_TipsTitleByName
- RogueBuild01_Sacred_TipsNameByName
- RogueBuild01_Sacred_TipsItemByName
- RogueBuild01_BookSacredHeadByName
**Snippet:**
```lua
require("RogueBuild01_Sacred_TipsTitleByName")
require("RogueBuild01_Sacred_TipsNameByName")
require("RogueBuild01_Sacred_TipsItemByName")
require("RogueBuild01_BookSacredHeadByName")

function GetRogueBuild01_Sacred_TipsUis(ui)
  local uis = {}
  uis.Title = GetRogueBuild01_Sacred_TipsTitleUis(ui:GetChild("Title"))
  uis.Name = GetRogueBuild01_Sacred_TipsNameUis(ui:GetChild("Name"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
```

---

## Rouge/RogueBuild01_Sacred_TipsItemByName.lua.lua
**Functions:**
- GetRogueBuild01_Sacred_TipsItemUis
**Snippet:**
```lua
function GetRogueBuild01_Sacred_TipsItemUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Sacred_TipsNameByName.lua.lua
**Functions:**
- GetRogueBuild01_Sacred_TipsNameUis
**Snippet:**
```lua
function GetRogueBuild01_Sacred_TipsNameUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Sacred_TipsTitleByName.lua.lua
**Functions:**
- GetRogueBuild01_Sacred_TipsTitleUis
**Snippet:**
```lua
function GetRogueBuild01_Sacred_TipsTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Sacred_WordByName.lua.lua
**Functions:**
- GetRogueBuild01_Sacred_WordUis
**Snippet:**
```lua
function GetRogueBuild01_Sacred_WordUis(ui)
  local uis = {}
  
  uis.EffectTxt = ui:GetChild("EffectTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ScoreDetailsByName.lua.lua
**Functions:**
- GetRogueBuild01_ScoreDetailsUis
**Requires:**
- CommonResource_BackGroundByName
- RogueBuild01_DetailsScoreByName
- RogueBuild01_DetailsTitleByName
- RogueBuild01_DetailsTimeByName
- RogueBuild01_DetailsDifficultyByName
- RogueBuild01_DetailsLayersByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("RogueBuild01_DetailsScoreByName")
require("RogueBuild01_DetailsTitleByName")
require("RogueBuild01_DetailsTimeByName")
require("RogueBuild01_DetailsDifficultyByName")
require("RogueBuild01_DetailsLayersByName")
require("CommonResource_CurrencyReturnByName")

function GetRogueBuild01_ScoreDetailsUis(ui)
  local uis = {}
```

---

## Rouge/RogueBuild01_ScoreDetailsWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_ScoreDetailsWindowUis
**Requires:**
- RogueBuild01_ScoreDetailsByName
**Snippet:**
```lua
require("RogueBuild01_ScoreDetailsByName")

function GetRogueBuild01_ScoreDetailsWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_ScoreDetailsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ScoreRewardByName.lua.lua
**Functions:**
- GetRogueBuild01_ScoreRewardUis
**Requires:**
- CommonResource_BackGroundByName
- RogueBuild01_ScoreRewardShowByName
- RogueBuild01_ScoreRewardListRegionByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("RogueBuild01_ScoreRewardShowByName")
require("RogueBuild01_ScoreRewardListRegionByName")
require("CommonResource_CurrencyReturnByName")

function GetRogueBuild01_ScoreRewardUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Show = GetRogueBuild01_ScoreRewardShowUis(ui:GetChild("Show"))
  uis.RewardList = GetRogueBuild01_ScoreRewardListRegionUis(ui:GetChild("RewardList"))
```

---

## Rouge/RogueBuild01_ScoreRewardExpProgressBarByName.lua.lua
**Functions:**
- GetRogueBuild01_ScoreRewardExpProgressBarUis
**Requires:**
- RogueBuild01_ScoreRewardExpProgressFillByName
**Snippet:**
```lua
require("RogueBuild01_ScoreRewardExpProgressFillByName")

function GetRogueBuild01_ScoreRewardExpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetRogueBuild01_ScoreRewardExpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ScoreRewardExpProgressFillByName.lua.lua
**Functions:**
- GetRogueBuild01_ScoreRewardExpProgressFillUis
**Snippet:**
```lua
function GetRogueBuild01_ScoreRewardExpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ScoreRewardItemByName.lua.lua
**Functions:**
- GetRogueBuild01_ScoreRewardItemUis
**Requires:**
- RogueBuild01_ScoreRewardItemCardPicByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("RogueBuild01_ScoreRewardItemCardPicByName")
require("CommonResource_RedDotByName")

function GetRogueBuild01_ScoreRewardItemUis(ui)
  local uis = {}
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.ItemCardPic = GetRogueBuild01_ScoreRewardItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
```

---

## Rouge/RogueBuild01_ScoreRewardItemCardPicByName.lua.lua
**Functions:**
- GetRogueBuild01_ScoreRewardItemCardPicUis
**Snippet:**
```lua
function GetRogueBuild01_ScoreRewardItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ScoreRewardItemDotByName.lua.lua
**Functions:**
- GetRogueBuild01_ScoreRewardItemDotUis
**Snippet:**
```lua
function GetRogueBuild01_ScoreRewardItemDotUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ScoreRewardItemStripByName.lua.lua
**Functions:**
- GetRogueBuild01_ScoreRewardItemStripUis
**Snippet:**
```lua
function GetRogueBuild01_ScoreRewardItemStripUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ScoreRewardListByName.lua.lua
**Functions:**
- GetRogueBuild01_ScoreRewardListUis
**Snippet:**
```lua
function GetRogueBuild01_ScoreRewardListUis(ui)
  local uis = {}
  
  uis.ItemList = ui:GetChild("ItemList")
  uis.DotProgressBar = ui:GetChild("DotProgressBar")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ScoreRewardListRegionByName.lua.lua
**Functions:**
- GetRogueBuild01_ScoreRewardListRegionUis
**Snippet:**
```lua
function GetRogueBuild01_ScoreRewardListRegionUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ScoreRewardProgressBarByName.lua.lua
**Functions:**
- GetRogueBuild01_ScoreRewardProgressBarUis
**Requires:**
- RogueBuild01_ScoreRewardProgressFillByName
- RogueBuild01_ScoreRewardItemStripByName
**Snippet:**
```lua
require("RogueBuild01_ScoreRewardProgressFillByName")
require("RogueBuild01_ScoreRewardItemStripByName")

function GetRogueBuild01_ScoreRewardProgressBarUis(ui)
  local uis = {}
  uis.bar = GetRogueBuild01_ScoreRewardProgressFillUis(ui:GetChild("bar"))
  uis.Strip = GetRogueBuild01_ScoreRewardItemStripUis(ui:GetChild("Strip"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ScoreRewardProgressFillByName.lua.lua
**Functions:**
- GetRogueBuild01_ScoreRewardProgressFillUis
**Snippet:**
```lua
function GetRogueBuild01_ScoreRewardProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ScoreRewardShowBgByName.lua.lua
**Functions:**
- GetRogueBuild01_ScoreRewardShowBgUis
**Snippet:**
```lua
function GetRogueBuild01_ScoreRewardShowBgUis(ui)
  local uis = {}
  
  uis.BackGroundLoader = ui:GetChild("BackGroundLoader")
  uis.BackGroundHolder = ui:GetChild("BackGroundHolder")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ScoreRewardShowByName.lua.lua
**Functions:**
- GetRogueBuild01_ScoreRewardShowUis
**Snippet:**
```lua
function GetRogueBuild01_ScoreRewardShowUis(ui)
  local uis = {}
  
  uis.ExpProgressBar = ui:GetChild("ExpProgressBar")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.ExpTxt = ui:GetChild("ExpTxt")
  uis.MaxTxt = ui:GetChild("MaxTxt")
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Rouge/RogueBuild01_ScoreRewardSpecialByName.lua.lua
**Functions:**
- GetRogueBuild01_ScoreRewardSpecialUis
**Snippet:**
```lua
function GetRogueBuild01_ScoreRewardSpecialUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ScoreRewardTipsAniByName.lua.lua
**Functions:**
- GetRogueBuild01_ScoreRewardTipsAniUis
**Requires:**
- RogueBuild01_ScoreRewardTipsByName
**Snippet:**
```lua
require("RogueBuild01_ScoreRewardTipsByName")

function GetRogueBuild01_ScoreRewardTipsAniUis(ui)
  local uis = {}
  uis.ScoreRewardTips = GetRogueBuild01_ScoreRewardTipsUis(ui:GetChild("ScoreRewardTips"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ScoreRewardTipsByName.lua.lua
**Functions:**
- GetRogueBuild01_ScoreRewardTipsUis
**Requires:**
- RogueBuild01_ScoreRewardTipsListByName
- RogueBuild01_ScoreRewardSpecialByName
**Snippet:**
```lua
require("RogueBuild01_ScoreRewardTipsListByName")
require("RogueBuild01_ScoreRewardSpecialByName")

function GetRogueBuild01_ScoreRewardTipsUis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.RewardList = GetRogueBuild01_ScoreRewardTipsListUis(ui:GetChild("RewardList"))
  uis.RewardSpecial = GetRogueBuild01_ScoreRewardSpecialUis(ui:GetChild("RewardSpecial"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Rouge/RogueBuild01_ScoreRewardTipsListByName.lua.lua
**Functions:**
- GetRogueBuild01_ScoreRewardTipsListUis
**Snippet:**
```lua
function GetRogueBuild01_ScoreRewardTipsListUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ScoreRewardWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_ScoreRewardWindowUis
**Requires:**
- RogueBuild01_ScoreRewardByName
**Snippet:**
```lua
require("RogueBuild01_ScoreRewardByName")

function GetRogueBuild01_ScoreRewardWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_ScoreRewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_ShopBuyByName.lua.lua
**Functions:**
- GetRogueBuild01_ShopBuyUis
**Requires:**
- CommonResource_PopupBgByName
- RogueBuild01_Buy_TipsRegionByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("RogueBuild01_Buy_TipsRegionByName")

function GetRogueBuild01_ShopBuyUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TipsRegion = GetRogueBuild01_Buy_TipsRegionUis(ui:GetChild("TipsRegion"))
  uis.AssetsList = ui:GetChild("AssetsList")
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_ShopBuyWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_ShopBuyWindowUis
**Requires:**
- RogueBuild01_ShopBuyByName
**Snippet:**
```lua
require("RogueBuild01_ShopBuyByName")

function GetRogueBuild01_ShopBuyWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_ShopBuyUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Shop_ItemAniByName.lua.lua
**Functions:**
- GetRogueBuild01_Shop_ItemAniUis
**Requires:**
- RogueBuild01_Shop_ItemByName
**Snippet:**
```lua
require("RogueBuild01_Shop_ItemByName")

function GetRogueBuild01_Shop_ItemAniUis(ui)
  local uis = {}
  uis.Item = GetRogueBuild01_Shop_ItemUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Shop_ItemByName.lua.lua
**Functions:**
- GetRogueBuild01_Shop_ItemUis
**Requires:**
- RogueBuild01_Shop_PointItemByName
- RogueBuild01_TreasureTypeByName
- RogueBuild01_TreasureLevelByName
**Snippet:**
```lua
require("RogueBuild01_Shop_PointItemByName")
require("RogueBuild01_TreasureTypeByName")
require("RogueBuild01_TreasureLevelByName")

function GetRogueBuild01_Shop_ItemUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.PointItem = GetRogueBuild01_Shop_PointItemUis(ui:GetChild("PointItem"))
  uis.IDTxt = ui:GetChild("IDTxt")
```

---

## Rouge/RogueBuild01_Shop_ItemWordByName.lua.lua
**Functions:**
- GetRogueBuild01_Shop_ItemWordUis
**Snippet:**
```lua
function GetRogueBuild01_Shop_ItemWordUis(ui)
  local uis = {}
  
  uis.EffectTxt = ui:GetChild("EffectTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Shop_OutBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_Shop_OutBtnUis
**Snippet:**
```lua
function GetRogueBuild01_Shop_OutBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Shop_PointItemBgByName.lua.lua
**Functions:**
- GetRogueBuild01_Shop_PointItemBgUis
**Snippet:**
```lua
function GetRogueBuild01_Shop_PointItemBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Shop_PointItemByName.lua.lua
**Functions:**
- GetRogueBuild01_Shop_PointItemUis
**Requires:**
- RogueBuild01_Shop_PointItemBgByName
**Snippet:**
```lua
require("RogueBuild01_Shop_PointItemBgByName")

function GetRogueBuild01_Shop_PointItemUis(ui)
  local uis = {}
  uis.Bg = GetRogueBuild01_Shop_PointItemBgUis(ui:GetChild("Bg"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Shop_ResetBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_Shop_ResetBtnUis
**Requires:**
- RogueBuild01_Shop_ResetNumberByName
**Snippet:**
```lua
require("RogueBuild01_Shop_ResetNumberByName")

function GetRogueBuild01_Shop_ResetBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Spend = GetRogueBuild01_Shop_ResetNumberUis(ui:GetChild("Spend"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_Shop_ResetNumberByName.lua.lua
**Functions:**
- GetRogueBuild01_Shop_ResetNumberUis
**Snippet:**
```lua
function GetRogueBuild01_Shop_ResetNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Shop_TimesByName.lua.lua
**Functions:**
- GetRogueBuild01_Shop_TimesUis
**Snippet:**
```lua
function GetRogueBuild01_Shop_TimesUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_Shop_TitleByName.lua.lua
**Functions:**
- GetRogueBuild01_Shop_TitleUis
**Snippet:**
```lua
function GetRogueBuild01_Shop_TitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_SmallTipsAniByName.lua.lua
**Functions:**
- GetRogueBuild01_SmallTipsAniUis
**Requires:**
- RogueBuild01_SmallTipsByName
**Snippet:**
```lua
require("RogueBuild01_SmallTipsByName")

function GetRogueBuild01_SmallTipsAniUis(ui)
  local uis = {}
  uis.SmallTips = GetRogueBuild01_SmallTipsUis(ui:GetChild("SmallTips"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_SmallTipsByName.lua.lua
**Functions:**
- GetRogueBuild01_SmallTipsUis
**Requires:**
- RogueBuild01_SmallTipsHeadByName
**Snippet:**
```lua
require("RogueBuild01_SmallTipsHeadByName")

function GetRogueBuild01_SmallTipsUis(ui)
  local uis = {}
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.Head = GetRogueBuild01_SmallTipsHeadUis(ui:GetChild("Head"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.typeCtr = ui:GetController("type")
  uis.root = ui
```

---

## Rouge/RogueBuild01_SmallTipsHeadBgByName.lua.lua
**Functions:**
- GetRogueBuild01_SmallTipsHeadBgUis
**Snippet:**
```lua
function GetRogueBuild01_SmallTipsHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_SmallTipsHeadByName.lua.lua
**Functions:**
- GetRogueBuild01_SmallTipsHeadUis
**Requires:**
- RogueBuild01_SmallTipsHeadBgByName
**Snippet:**
```lua
require("RogueBuild01_SmallTipsHeadBgByName")

function GetRogueBuild01_SmallTipsHeadUis(ui)
  local uis = {}
  uis.HeadBg = GetRogueBuild01_SmallTipsHeadBgUis(ui:GetChild("HeadBg"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_StartChoiceCardListByName.lua.lua
**Functions:**
- GetRogueBuild01_StartChoiceCardListUis
**Requires:**
- CommonResource_BackGroundByName
- RogueBuild01_ChoiceCardList_InfoByName
- RogueBuild01_ChoiceCardList_Info5ByName
- RogueBuild01_ChoiceCardList_OccupationByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("RogueBuild01_ChoiceCardList_InfoByName")
require("RogueBuild01_ChoiceCardList_Info5ByName")
require("RogueBuild01_ChoiceCardList_OccupationByName")

function GetRogueBuild01_StartChoiceCardListUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Info = GetRogueBuild01_ChoiceCardList_InfoUis(ui:GetChild("Info"))
  uis.ChoiceNumber = GetRogueBuild01_ChoiceCardList_Info5Uis(ui:GetChild("ChoiceNumber"))
```

---

## Rouge/RogueBuild01_StartChoiceCardListWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_StartChoiceCardListWindowUis
**Requires:**
- RogueBuild01_StartChoiceCardListByName
**Snippet:**
```lua
require("RogueBuild01_StartChoiceCardListByName")

function GetRogueBuild01_StartChoiceCardListWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_StartChoiceCardListUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_StartChoiceRegion_CardAniByName.lua.lua
**Functions:**
- GetRogueBuild01_StartChoiceRegion_CardAniUis
**Requires:**
- RogueBuild01_StartChoiceRegion_CardByName
**Snippet:**
```lua
require("RogueBuild01_StartChoiceRegion_CardByName")

function GetRogueBuild01_StartChoiceRegion_CardAniUis(ui)
  local uis = {}
  uis.Card = GetRogueBuild01_StartChoiceRegion_CardUis(ui:GetChild("Card"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_StartChoiceRegion_CardBgByName.lua.lua
**Functions:**
- GetRogueBuild01_StartChoiceRegion_CardBgUis
**Snippet:**
```lua
function GetRogueBuild01_StartChoiceRegion_CardBgUis(ui)
  local uis = {}
  
  uis.CardPicLoader = ui:GetChild("CardPicLoader")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_StartChoiceRegion_CardByName.lua.lua
**Functions:**
- GetRogueBuild01_StartChoiceRegion_CardUis
**Requires:**
- RogueBuild01_StartChoiceRegion_CardBgByName
- CommonResource_OccupationByName
- CommonResource_CardBreachByName
**Snippet:**
```lua
require("RogueBuild01_StartChoiceRegion_CardBgByName")
require("CommonResource_OccupationByName")
require("CommonResource_CardBreachByName")

function GetRogueBuild01_StartChoiceRegion_CardUis(ui)
  local uis = {}
  uis.CardPic = GetRogueBuild01_StartChoiceRegion_CardBgUis(ui:GetChild("CardPic"))
  uis.Occupation = GetCommonResource_OccupationUis(ui:GetChild("Occupation"))
  uis.ElementList = ui:GetChild("ElementList")
  uis.StarList = ui:GetChild("StarList")
```

---

## Rouge/RogueBuild01_StartChoiceRegion_ItemAniByName.lua.lua
**Functions:**
- GetRogueBuild01_StartChoiceRegion_ItemAniUis
**Requires:**
- RogueBuild01_StartChoiceRegion_ItemByName
**Snippet:**
```lua
require("RogueBuild01_StartChoiceRegion_ItemByName")

function GetRogueBuild01_StartChoiceRegion_ItemAniUis(ui)
  local uis = {}
  uis.Item = GetRogueBuild01_StartChoiceRegion_ItemUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_StartChoiceRegion_ItemByName.lua.lua
**Functions:**
- GetRogueBuild01_StartChoiceRegion_ItemUis
**Requires:**
- RogueBuild01_Shop_PointItemByName
- RogueBuild01_TreasureTypeByName
- RogueBuild01_TreasureLevelByName
**Snippet:**
```lua
require("RogueBuild01_Shop_PointItemByName")
require("RogueBuild01_TreasureTypeByName")
require("RogueBuild01_TreasureLevelByName")

function GetRogueBuild01_StartChoiceRegion_ItemUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.PointItem = GetRogueBuild01_Shop_PointItemUis(ui:GetChild("PointItem"))
  uis.IDTxt = ui:GetChild("IDTxt")
```

---

## Rouge/RogueBuild01_StartChoiceRegion_WordByName.lua.lua
**Functions:**
- GetRogueBuild01_StartChoiceRegion_WordUis
**Snippet:**
```lua
function GetRogueBuild01_StartChoiceRegion_WordUis(ui)
  local uis = {}
  
  uis.EffectTxt = ui:GetChild("EffectTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_SweepByName.lua.lua
**Functions:**
- GetRogueBuild01_SweepUis
**Requires:**
- CommonResource_PopupBgByName
- RogueBuild01_SweepTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("RogueBuild01_SweepTipsByName")

function GetRogueBuild01_SweepUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.SweepTips = GetRogueBuild01_SweepTipsUis(ui:GetChild("SweepTips"))
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_SweepCloseBtnByName.lua.lua
**Functions:**
- GetRogueBuild01_SweepCloseBtnUis
**Snippet:**
```lua
function GetRogueBuild01_SweepCloseBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_SweepTipsByName.lua.lua
**Functions:**
- GetRogueBuild01_SweepTipsUis
**Requires:**
- RogueBuild01_DetailsRegion2_Exp1ByName
- RogueBuild01_DetailsRegion2_Exp2ByName
**Snippet:**
```lua
require("RogueBuild01_DetailsRegion2_Exp1ByName")
require("RogueBuild01_DetailsRegion2_Exp2ByName")

function GetRogueBuild01_SweepTipsUis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Exp = GetRogueBuild01_DetailsRegion2_Exp1Uis(ui:GetChild("Exp"))
  uis.Talent = GetRogueBuild01_DetailsRegion2_Exp2Uis(ui:GetChild("Talent"))
```

---

## Rouge/RogueBuild01_SweepWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_SweepWindowUis
**Requires:**
- RogueBuild01_SweepByName
**Snippet:**
```lua
require("RogueBuild01_SweepByName")

function GetRogueBuild01_SweepWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_SweepUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_TalentBottomRegionByName.lua.lua
**Functions:**
- GetRogueBuild01_TalentBottomRegionUis
**Requires:**
- RogueBuild01_TalentState1ByName
- RogueBuild01_TalentState3ByName
- RogueBuild01_TalentState4ByName
- RogueBuild01_TalentState5ByName
**Snippet:**
```lua
require("RogueBuild01_TalentState1ByName")
require("RogueBuild01_TalentState3ByName")
require("RogueBuild01_TalentState4ByName")
require("RogueBuild01_TalentState5ByName")

function GetRogueBuild01_TalentBottomRegionUis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.State2Btn = ui:GetChild("State2Btn")
```

---

## Rouge/RogueBuild01_TalentByName.lua.lua
**Functions:**
- GetRogueBuild01_TalentUis
**Requires:**
- CommonResource_BackGroundByName
- RogueBuild01_TalentBottomRegionByName
- RogueBuild01_TalentHaveNumberByName
- RogueBuild01_TalentLeftRegionByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("RogueBuild01_TalentBottomRegionByName")
require("RogueBuild01_TalentHaveNumberByName")
require("RogueBuild01_TalentLeftRegionByName")
require("CommonResource_CurrencyReturnByName")

function GetRogueBuild01_TalentUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TalentBottomRegion = GetRogueBuild01_TalentBottomRegionUis(ui:GetChild("TalentBottomRegion"))
```

---

## Rouge/RogueBuild01_TalentDot1ByName.lua.lua
**Functions:**
- GetRogueBuild01_TalentDot1Uis
**Snippet:**
```lua
function GetRogueBuild01_TalentDot1Uis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.typeCtr = ui:GetController("type")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_TalentDot2ByName.lua.lua
**Functions:**
- GetRogueBuild01_TalentDot2Uis
**Snippet:**
```lua
function GetRogueBuild01_TalentDot2Uis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.typeCtr = ui:GetController("type")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_TalentHaveNumberByName.lua.lua
**Functions:**
- GetRogueBuild01_TalentHaveNumberUis
**Snippet:**
```lua
function GetRogueBuild01_TalentHaveNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_TalentLeftOrdinaryRegionByName.lua.lua
**Functions:**
- GetRogueBuild01_TalentLeftOrdinaryRegionUis
**Snippet:**
```lua
function GetRogueBuild01_TalentLeftOrdinaryRegionUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_TalentLeftOrdinaryWordByName.lua.lua
**Functions:**
- GetRogueBuild01_TalentLeftOrdinaryWordUis
**Snippet:**
```lua
function GetRogueBuild01_TalentLeftOrdinaryWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_TalentLeftRegionByName.lua.lua
**Functions:**
- GetRogueBuild01_TalentLeftRegionUis
**Requires:**
- RogueBuild01_TalentLeftOrdinaryRegionByName
- RogueBuild01_TalentLeftSpecialRegionByName
**Snippet:**
```lua
require("RogueBuild01_TalentLeftOrdinaryRegionByName")
require("RogueBuild01_TalentLeftSpecialRegionByName")

function GetRogueBuild01_TalentLeftRegionUis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.OrdinaryRegion = GetRogueBuild01_TalentLeftOrdinaryRegionUis(ui:GetChild("OrdinaryRegion"))
  uis.SpecialRegion = GetRogueBuild01_TalentLeftSpecialRegionUis(ui:GetChild("SpecialRegion"))
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_TalentLeftSpecialRegionByName.lua.lua
**Functions:**
- GetRogueBuild01_TalentLeftSpecialRegionUis
**Snippet:**
```lua
function GetRogueBuild01_TalentLeftSpecialRegionUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_TalentLeftSpecialWordByName.lua.lua
**Functions:**
- GetRogueBuild01_TalentLeftSpecialWordUis
**Snippet:**
```lua
function GetRogueBuild01_TalentLeftSpecialWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_TalentLine1ByName.lua.lua
**Functions:**
- GetRogueBuild01_TalentLine1Uis
**Snippet:**
```lua
function GetRogueBuild01_TalentLine1Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_TalentLine2ByName.lua.lua
**Functions:**
- GetRogueBuild01_TalentLine2Uis
**Snippet:**
```lua
function GetRogueBuild01_TalentLine2Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_TalentLine2_LeftByName.lua.lua
**Functions:**
- GetRogueBuild01_TalentLine2_LeftUis
**Snippet:**
```lua
function GetRogueBuild01_TalentLine2_LeftUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_TalentLine2_RightByName.lua.lua
**Functions:**
- GetRogueBuild01_TalentLine2_RightUis
**Snippet:**
```lua
function GetRogueBuild01_TalentLine2_RightUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_TalentLine3ByName.lua.lua
**Functions:**
- GetRogueBuild01_TalentLine3Uis
**Snippet:**
```lua
function GetRogueBuild01_TalentLine3Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_TalentLine4ByName.lua.lua
**Functions:**
- GetRogueBuild01_TalentLine4Uis
**Snippet:**
```lua
function GetRogueBuild01_TalentLine4Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_TalentLine4_LeftByName.lua.lua
**Functions:**
- GetRogueBuild01_TalentLine4_LeftUis
**Snippet:**
```lua
function GetRogueBuild01_TalentLine4_LeftUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_TalentLine4_RightByName.lua.lua
**Functions:**
- GetRogueBuild01_TalentLine4_RightUis
**Snippet:**
```lua
function GetRogueBuild01_TalentLine4_RightUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_TalentSpendNumberByName.lua.lua
**Functions:**
- GetRogueBuild01_TalentSpendNumberUis
**Snippet:**
```lua
function GetRogueBuild01_TalentSpendNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_TalentState1ByName.lua.lua
**Functions:**
- GetRogueBuild01_TalentState1Uis
**Requires:**
- RogueBuild01_TalentSpendNumberByName
**Snippet:**
```lua
require("RogueBuild01_TalentSpendNumberByName")

function GetRogueBuild01_TalentState1Uis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Spend = GetRogueBuild01_TalentSpendNumberUis(ui:GetChild("Spend"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_TalentState2BtnByName.lua.lua
**Functions:**
- GetRogueBuild01_TalentState2BtnUis
**Requires:**
- RogueBuild01_TalentSpendNumberByName
**Snippet:**
```lua
require("RogueBuild01_TalentSpendNumberByName")

function GetRogueBuild01_TalentState2BtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Spend = GetRogueBuild01_TalentSpendNumberUis(ui:GetChild("Spend"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_TalentState3ByName.lua.lua
**Functions:**
- GetRogueBuild01_TalentState3Uis
**Snippet:**
```lua
function GetRogueBuild01_TalentState3Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_TalentState4ByName.lua.lua
**Functions:**
- GetRogueBuild01_TalentState4Uis
**Snippet:**
```lua
function GetRogueBuild01_TalentState4Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_TalentState5ByName.lua.lua
**Functions:**
- GetRogueBuild01_TalentState5Uis
**Snippet:**
```lua
function GetRogueBuild01_TalentState5Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_TalentTreeByName.lua.lua
**Functions:**
- GetRogueBuild01_TalentTreeUis
**Requires:**
- RogueBuild01_TalentLine1ByName
- RogueBuild01_TalentLine2_LeftByName
- RogueBuild01_TalentLine3ByName
- RogueBuild01_TalentLine4_LeftByName
- RogueBuild01_TalentLine2_RightByName
- RogueBuild01_TalentLine4_RightByName
- RogueBuild01_TalentDot1ByName
- RogueBuild01_TalentDot2ByName
**Snippet:**
```lua
require("RogueBuild01_TalentLine1ByName")
require("RogueBuild01_TalentLine2_LeftByName")
require("RogueBuild01_TalentLine3ByName")
require("RogueBuild01_TalentLine4_LeftByName")
require("RogueBuild01_TalentLine2_RightByName")
require("RogueBuild01_TalentLine4_RightByName")
require("RogueBuild01_TalentDot1ByName")
require("RogueBuild01_TalentDot2ByName")

function GetRogueBuild01_TalentTreeUis(ui)
```

---

## Rouge/RogueBuild01_TalentWindowByName.lua.lua
**Functions:**
- GetRogueBuild01_TalentWindowUis
**Requires:**
- RogueBuild01_TalentByName
**Snippet:**
```lua
require("RogueBuild01_TalentByName")

function GetRogueBuild01_TalentWindowUis(ui)
  local uis = {}
  uis.Main = GetRogueBuild01_TalentUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_TreasureChoice1BtnByName.lua.lua
**Functions:**
- GetRogueBuild01_TreasureChoice1BtnUis
**Requires:**
- RogueBuild01_TreasureChoiceBgByName
**Snippet:**
```lua
require("RogueBuild01_TreasureChoiceBgByName")

function GetRogueBuild01_TreasureChoice1BtnUis(ui)
  local uis = {}
  uis.Bg = GetRogueBuild01_TreasureChoiceBgUis(ui:GetChild("Bg"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_TreasureChoice2BtnByName.lua.lua
**Functions:**
- GetRogueBuild01_TreasureChoice2BtnUis
**Requires:**
- RogueBuild01_TreasureChoiceBgByName
**Snippet:**
```lua
require("RogueBuild01_TreasureChoiceBgByName")

function GetRogueBuild01_TreasureChoice2BtnUis(ui)
  local uis = {}
  uis.Bg = GetRogueBuild01_TreasureChoiceBgUis(ui:GetChild("Bg"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_TreasureChoice3BtnByName.lua.lua
**Functions:**
- GetRogueBuild01_TreasureChoice3BtnUis
**Requires:**
- RogueBuild01_TreasureChoiceBgByName
**Snippet:**
```lua
require("RogueBuild01_TreasureChoiceBgByName")

function GetRogueBuild01_TreasureChoice3BtnUis(ui)
  local uis = {}
  uis.Bg = GetRogueBuild01_TreasureChoiceBgUis(ui:GetChild("Bg"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Rouge/RogueBuild01_TreasureChoiceBgByName.lua.lua
**Functions:**
- GetRogueBuild01_TreasureChoiceBgUis
**Snippet:**
```lua
function GetRogueBuild01_TreasureChoiceBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_TreasureLevelByName.lua.lua
**Functions:**
- GetRogueBuild01_TreasureLevelUis
**Snippet:**
```lua
function GetRogueBuild01_TreasureLevelUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueBuild01_TreasureTypeByName.lua.lua
**Functions:**
- GetRogueBuild01_TreasureTypeUis
**Snippet:**
```lua
function GetRogueBuild01_TreasureTypeUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Rouge/RogueData.lua.lua
**Functions:**
- RogueData.SaveWeekTask
- RogueData.GetWeekTask
- RogueData.SaveWeekReward
- RogueData.GetWeekReward
- RogueData.GetRogueInfo
- RogueData.GetRogueTheme
- RogueData.GetRogueTrend
- RogueData.GetRogueTrendById
- RogueData.UpdateThemeInfo
- RogueData.UpdateTrendInfos
- RogueData.UpdateOneTrendInfos
- RogueData.SaveRogueInfo
- RogueData.SavePicInfo
- RogueData.UpdatePicInfoNew
- RogueData.GetPicInfoBuyType
- RogueData.SavePicNewId
- RogueData.GetPicNewByType
- RogueData.ClearPicNewByType
**Snippet:**
```lua
RogueData = {record = nil, taskRefreshStamp = nil}
local rogueInfo
local picInfo = {}
local picNewId = {}
local weekTask = {}
local weekReward = {}

function RogueData.SaveWeekTask(taskList)
  weekTask = taskList
end
```

---

## Rouge/RogueDifficultyChoiceWindow.lua.lua
**Functions:**
- RogueDifficultyChoiceWindow.ReInitData
- RogueDifficultyChoiceWindow.OnInit
- RogueDifficultyChoiceWindow.UpdateInfo
- list.itemRenderer
- RogueDifficultyChoiceWindow.ShowInfo
- tips.EffectList.itemRenderer
- tips.EffectList.itemRenderer
- RogueDifficultyChoiceWindow.GetDifficultyData
- RogueDifficultyChoiceWindow.InitBtn
- RogueDifficultyChoiceWindow.OnClose
**Requires:**
- RogueBuild01_DifficultyChoiceWindowByName
**Snippet:**
```lua
require("RogueBuild01_DifficultyChoiceWindowByName")
local RogueDifficultyChoiceWindow = {}
local uis, contentPane, jumpTb, difficultyData, curPlay

function RogueDifficultyChoiceWindow.ReInitData()
end

function RogueDifficultyChoiceWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RogueDifficultyChoiceWindow.package, WinResConfig.RogueDifficultyChoiceWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/RogueGameBackpackWindow.lua.lua
**Functions:**
- wordlist.itemRenderer
- list.itemRenderer
- list.itemRenderer
- RogueGameBackpackWindow.ReInitData
- RogueGameBackpackWindow.OnInit
- RogueGameBackpackWindow.UpdateInfo
- RogueGameBackpackWindow.InitBtn
- RogueGameBackpackWindow.OnClose
**Requires:**
- RogueBuild01_InsideItemLookWindowByName
**Snippet:**
```lua
require("RogueBuild01_InsideItemLookWindowByName")
local RogueGameBackpackWindow = {}
local uis, contentPane, allHalidom, allTreasures, maskedTreasures, LEVEL_MASK, TYPE_MASK, selectedTreasureId
local TREASURE_TYPE_NAME_LOOKUP = {
  [RogueTreasureType.ATTR_GOT] = T(1404),
  [RogueTreasureType.COIN_GOT] = T(1405),
  [RogueTreasureType.ATK] = T(1406),
  [RogueTreasureType.DEF] = T(1407),
  [RogueTreasureType.HP] = T(1408),
  [RogueTreasureType.ATK_SPD] = T(1409),
```

---

## Rouge/RogueGameCardUpWindow.lua.lua
**Functions:**
- RefreshStrengthenPanel
- RogueGameCardUpWindow.ReInitData
- RogueGameCardUpWindow.OnInit
- RogueGameCardUpWindow.UpdateInfo
- RogueGameCardUpWindow.InitBtn
- RogueGameCardUpWindow.OnClose
- RogueGameCardUpWindow.HandleMessage
**Requires:**
- RogueBuild01_InsideCardUpWindowByName
**Snippet:**
```lua
require("RogueBuild01_InsideCardUpWindowByName")
local RogueGameCardUpWindow = {}
local uis, contentPane, cardsBuffer, occupationsBuffer, selectedCardId, selectedAttributeId, cardFinalAttributes, CARD_MASK, revivalCallback, rewardId, changed_attribute, tweenCollect
local STRENGTHENABLE_ATTR = {
  CardAttribute.GetIdByName(ATTR_ENUM.atk),
  CardAttribute.GetIdByName(ATTR_ENUM.def),
  CardAttribute.GetIdByName(ATTR_ENUM.max_hp)
}
local DefaultSort = function(x, y)
  local a, b = x.info or x, y.info or y
```

---

## Rouge/RogueGameConst.lua.lua
**Snippet:**
```lua
RogueGameNodeType = {
  BATTLE_NORMAL = 1,
  BATTLE_ENCOUNTER = 2,
  BATTLE_BOSS = 3,
  SHOP = 11,
  EVENT = 12,
  SUPPLY = 13
}
RogueBattleType = {
  NORMAL = 1,
```

---

## Rouge/RogueGameData.lua.lua
**Snippet:**
```lua
local themeInfo, chapterInfo, cardInfos, battleCardInfos
local SetThemeInfo = function(info)
  themeInfo = info
end
local GetThemeInfo = function()
  return themeInfo
end
local SetChapterInfo = function(info)
  chapterInfo = info
end
```

---

## Rouge/RogueGameDifficultyInfoWindow.lua.lua
**Functions:**
- RogueGameDifficultyInfoWindow.ReInitData
- RogueGameDifficultyInfoWindow.OnInit
- RogueGameDifficultyInfoWindow.UpdateInfo
- list.itemRenderer
- list.itemRenderer
- RogueGameDifficultyInfoWindow.InitBtn
- RogueGameDifficultyInfoWindow.OnClose
**Requires:**
- RogueBuild01_InsideDifficultyLookWindowByName
**Snippet:**
```lua
require("RogueBuild01_InsideDifficultyLookWindowByName")
local RogueGameDifficultyInfoWindow = {}
local uis, contentPane

function RogueGameDifficultyInfoWindow.ReInitData()
end

function RogueGameDifficultyInfoWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RogueGameDifficultyInfoWindow.package, WinResConfig.RogueGameDifficultyInfoWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/RogueGameEndingWindow.lua.lua
**Functions:**
- ScrollCaption
- RogueGameEndingWindow.ReInitData
- RogueGameEndingWindow.OnInit
- RogueGameEndingWindow.UpdateInfo
- list.itemRenderer
- RogueGameEndingWindow.InitBtn
- RogueGameEndingWindow.OnClose
**Requires:**
- RogueBuild01_InsidePlotEndWindowByName
**Snippet:**
```lua
require("RogueBuild01_InsidePlotEndWindowByName")
local RogueGameEndingWindow = {}
local uis, contentPane, endingId, callback
local CATION_FADE_SPEED = 1.05
local CATION_FADE_DURATION = 1
local CATION_SCROLL_SPEED = 27
local START_SCROLL_DELAY = 10
local stories
local elapse = 0
local cation_fade_speed_scale = 1
```

---

## Rouge/RogueGameEndWindow.lua.lua
**Functions:**
- RogueGameEndWindow.ReInitData
- RogueGameEndWindow.OnInit
- RogueGameEndWindow.UpdateInfo
- RogueGameEndWindow.InitBtn
- RogueGameEndWindow.OnClose
**Requires:**
- RogueBuild01_InsideEndWindowByName
**Snippet:**
```lua
require("RogueBuild01_InsideEndWindowByName")
local RogueGameEndWindow = {}
local uis, contentPane, callback, endingId
local duration = 2
local tweenId
local Finish = function()
  if type(endingId) == "number" and endingId > 0 then
    OpenWindow(WinResConfig.RogueGameEndingWindow.name, nil, endingId, callback)
  elseif callback then
    callback()
```

---

## Rouge/RogueGameEventWindow.lua.lua
**Functions:**
- currentTypingEffect.effectEndAction
- RogueGameEventWindow.ReInitData
- RogueGameEventWindow.OnInit
- RogueGameEventWindow.UpdateInfo
- RogueGameEventWindow.InitBtn
- RogueGameEventWindow.OnShown
- RogueGameEventWindow.OnHide
- RogueGameEventWindow.OnClose
- RogueGameEventWindow.HandleMessage
**Requires:**
- RogueBuild01_InsidePlotEventWindowByName
**Snippet:**
```lua
require("RogueBuild01_InsidePlotEventWindowByName")
local RogueGameEventWindow = {}
local uis, contentPane, rogueNode, callback, story_reader, currentTypingEffect
local typingInterval = 0.05
local typingSpeedUpInterval = 0.001
local tweenId
local IsTriggerKeyStep = function(storyConf)
  local trigger = false
  if storyConf and type(storyConf.option_condition) == "string" then
    local splits = Split(storyConf.option_condition, "|")
```

---

## Rouge/RogueGameGetAttributeTipsWindow.lua.lua
**Functions:**
- RogueGameGetAttributeTipsWindow.ReInitData
- RogueGameGetAttributeTipsWindow.OnInit
- RogueGameGetAttributeTipsWindow.UpdateInfo
- RogueGameGetAttributeTipsWindow.InitBtn
- RogueGameGetAttributeTipsWindow.OnClose
**Requires:**
- RogueBuild01_Camp_GetAttributeTipsWindowByName
**Snippet:**
```lua
require("RogueBuild01_Camp_GetAttributeTipsWindowByName")
local RogueGameGetAttributeTipsWindow = {}
local uis, contentPane, rewards
local DisplayReward = function(itemId, cnt)
  uis.Main.TipsRegion.WordTxt.text = T(20425, cnt)
end

function RogueGameGetAttributeTipsWindow.ReInitData()
end

```

---

## Rouge/RogueGameGetCurrencyTipsWindow.lua.lua
**Functions:**
- RogueGameGetCurrencyTipsWindow.ReInitData
- RogueGameGetCurrencyTipsWindow.OnInit
- RogueGameGetCurrencyTipsWindow.UpdateInfo
- RogueGameGetCurrencyTipsWindow.InitBtn
- RogueGameGetCurrencyTipsWindow.OnClose
**Requires:**
- RogueBuild01_Camp_GetCurrencyTipsWindowByName
**Snippet:**
```lua
require("RogueBuild01_Camp_GetCurrencyTipsWindowByName")
local RogueGameGetCurrencyTipsWindow = {}
local uis, contentPane, rewards
local DisplayReward = function(itemId, cnt)
  uis.Main.TipsRegion.WordTxt.text = T(20427, cnt)
end

function RogueGameGetCurrencyTipsWindow.ReInitData()
end

```

---

## Rouge/RogueGameInfoTipsWindow.lua.lua
**Functions:**
- PopupNotify
- RogueGameInfoTipsWindow.ReInitData
- RogueGameInfoTipsWindow.OnInit
- RogueGameInfoTipsWindow.UpdateInfo
- RogueGameInfoTipsWindow.InitBtn
- RogueGameInfoTipsWindow.OnClose
- RogueGameInfoTipsWindow.HandleMessage
**Requires:**
- RogueBuild01_InsideSmallWindowByName
**Snippet:**
```lua
require("RogueBuild01_InsideSmallWindowByName")
local RogueGameInfoTipsWindow = {}
local uis, contentPane, notifyCollector
local notifyCnt = 0
local notifyDelay = 0
local interval = 0.15
local PopupNotify
local TransitionCallback = function()
  notifyCnt = notifyCnt - 1
  notifyDelay = math.max(notifyDelay - interval, 0)
```

---

## Rouge/RogueGameItemTipsWindow.lua.lua
**Functions:**
- wordlist.itemRenderer
- RogueGameItemTipsWindow.ReInitData
- RogueGameItemTipsWindow.OnInit
- RogueGameItemTipsWindow.UpdateInfo
- RogueGameItemTipsWindow.InitBtn
- RogueGameItemTipsWindow.OnClose
**Requires:**
- RogueBuild01_Camp_ItemTipsWindowByName
**Snippet:**
```lua
require("RogueBuild01_Camp_ItemTipsWindowByName")
local RogueGameItemTipsWindow = {}
local uis, contentPane, treasure, treasureIdList, unlokedHalidoms, lookover
local DisplayTreasure = function(treasureId)
  if lookover then
    SoundUtil.PlayUISfx("event:/sfx/sfx_ui/ui_sys/ui_yuantu_item_reward_static")
  else
    SoundUtil.PlayUISfx("event:/sfx/sfx_ui/ui_sys/ui_yuantu_item_reward")
  end
  local conf = TableData.GetConfig(treasureId, "BaseRogueTreasure")
```

---

## Rouge/RogueGameMapWindow.lua.lua
**Functions:**
- RogueGameMapWindow.ReInitData
- RogueGameMapWindow.OnInit
- RogueGameMapWindow.UpdateInfo
- RogueGameMapWindow.InitBtn
- RogueGameMapWindow.OnShown
- RogueGameMapWindow.OnClose
- RogueGameMapWindow.HandleMessage
**Requires:**
- RogueBuild01_InsideMapWindowByName
**Snippet:**
```lua
require("RogueBuild01_InsideMapWindowByName")
local RogueGameMapWindow = {}
local uis, contentPane, rogueNodes, nodeObjs, chapterIdCache, scrollingTweenId
local RELATION_STATE = {
  NOT_OPEN = 0,
  UNDERWAY = 1,
  COMPLETE = 2,
  CLOSED = 3,
  SELECTABLE = 4
}
```

---

## Rouge/RogueGameMgr.lua.lua
**Functions:**
- buildTree
- IsReachable
- attributelist.itemRenderer
- skilllist.itemRenderer
- assetlist.itemRenderer
**Snippet:**
```lua
local nodesBuffer, parentsBuffer, childrenBuffer, rogueNodes

local function buildTree(nodeConf, nodeArray, nodeLayer)
  local node
  local next = nodeConf.next
  local exists = table.keyof(nodeArray, nodeConf.id, "id")
  if not exists then
    node = {
      id = nodeConf.id,
      layer = nodeLayer,
```

---

## Rouge/RogueGameNodeHandleWindow.lua.lua
**Functions:**
- RogueGameNodeHandleWindow.ReInitData
- RogueGameNodeHandleWindow.OnInit
- RogueGameNodeHandleWindow.UpdateInfo
- wordlist.itemProvider
- wordlist.itemRenderer
- RogueGameNodeHandleWindow.InitBtn
- RogueGameNodeHandleWindow.OnClose
**Requires:**
- RogueBuild01_InsideDungeonInfoWindowByName
**Snippet:**
```lua
require("RogueBuild01_InsideDungeonInfoWindowByName")
local RogueGameNodeHandleWindow = {}
local uis, contentPane, nodeId, handleCallback, cancelCallback
local CONTROLLER_LOOKUP = {
  BATTLE_NORMAL = 0,
  BATTLE_ENCOUNTER = 1,
  BATTLE_BOSS = 2,
  EVENT = 3,
  SHOP = 4,
  SUPPLY = 5,
```

---

## Rouge/RogueGameRebirthTipsWindow.lua.lua
**Functions:**
- RogueGameRebirthTipsWindow.ReInitData
- RogueGameRebirthTipsWindow.OnInit
- RogueGameRebirthTipsWindow.UpdateInfo
- RogueGameRebirthTipsWindow.InitBtn
- RogueGameRebirthTipsWindow.OnClose
**Requires:**
- RogueBuild01_Camp_RebirthTipsWindowByName
**Snippet:**
```lua
require("RogueBuild01_Camp_RebirthTipsWindowByName")
local RogueGameRebirthTipsWindow = {}
local uis, contentPane, revivalCards, maskTexture
local DisplayRevivalInfo = function(cardId)
  SoundUtil.PlayUISfx("event:/sfx/sfx_ui/ui_sys/ui_yuantu_item_reward")
  local conf = TableData.GetConfig(cardId, "BaseCard")
  uis.Main.TipsRegion.NameTxt.text = T(20463)
  uis.Main.TipsRegion.WordTxt.text = T(20430, conf.name())
  if not maskTexture then
    maskTexture = ResourceManager.LoadTexture("Assets/Art/TextureSingle/UI/Camp_RecruitTipsHead.png")
```

---

## Rouge/RogueGameRecoveryTipsWindow.lua.lua
**Functions:**
- RogueGameRecoveryTipsWindow.ReInitData
- RogueGameRecoveryTipsWindow.OnInit
- RogueGameRecoveryTipsWindow.UpdateInfo
- list.itemRenderer
- RogueGameRecoveryTipsWindow.InitBtn
- RogueGameRecoveryTipsWindow.OnClose
**Requires:**
- RogueBuild01_Camp_RecoveryTipsWindowByName
**Snippet:**
```lua
require("RogueBuild01_Camp_RecoveryTipsWindowByName")
local RogueGameRecoveryTipsWindow = {}
local uis, contentPane, rewardId, recoverCards

function RogueGameRecoveryTipsWindow.ReInitData()
end

function RogueGameRecoveryTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RogueGameRecoveryTipsWindow.package, WinResConfig.RogueGameRecoveryTipsWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/RogueGameRecruitTipsWindow.lua.lua
**Functions:**
- RogueGameRecruitTipsWindow.ReInitData
- RogueGameRecruitTipsWindow.OnInit
- RogueGameRecruitTipsWindow.UpdateInfo
- RogueGameRecruitTipsWindow.InitBtn
- RogueGameRecruitTipsWindow.OnClose
**Requires:**
- RogueBuild01_Camp_RecruitTipsWindowByName
**Snippet:**
```lua
require("RogueBuild01_Camp_RecruitTipsWindowByName")
local RogueGameRecruitTipsWindow = {}
local uis, contentPane, maskTexture, recruitCards
local DisplayRecruitTips = function(cardId)
  SoundUtil.PlayUISfx("event:/sfx/sfx_ui/ui_sys/ui_yuantu_item_reward")
  local conf = TableData.GetConfig(cardId, "BaseCard")
  local recruitTipsText = T(20423, conf.name())
  uis.Main.TipsRegion.NameTxt.text = T(20462)
  uis.Main.TipsRegion.WordTxt.text = recruitTipsText
  if not maskTexture then
```

---

## Rouge/RogueGameRewardsWindow.lua.lua
**Functions:**
- wordlist.itemRenderer
- RogueGameRewardsWindow.ReInitData
- RogueGameRewardsWindow.OnInit
- RogueGameRewardsWindow.UpdateInfo
- RogueGameRewardsWindow.InitBtn
- RogueGameRewardsWindow.OnClose
- RogueGameRewardsWindow.HandleMessage
**Requires:**
- RogueBuild01_InsideCampWindowByName
**Snippet:**
```lua
require("RogueBuild01_InsideCampWindowByName")
local RogueGameRewardsWindow = {}
local uis, contentPane, rogueNode, displayReturnBtn, rewards, gotRewards
local REWARD_CONTROLLER_LOOKUP = {
  [RogueGameRewardType.RECRUITING_TICKET] = 0,
  [RogueGameRewardType.TREAT] = 1,
  [RogueGameRewardType.REVIVE] = 2,
  [RogueGameRewardType.RANDOM_COIN] = 3,
  [RogueGameRewardType.RANDOM_ATTR] = 4,
  [RogueGameRewardType.SPECIAL_TREASURE] = 5,
```

---

## Rouge/RogueGameService.lua.lua
**Snippet:**
```lua
local GetRogueInfoReq = function()
end
local GetRougeInfoRsp = function(msg)
end
local StartRogueGameReq = function(difficultyLevel, rspCallback)
  Net.Send(Proto.MsgName.StartRogueGameReq, {difficultyLevel = difficultyLevel}, rspCallback)
end
local StartRogueGameRsp = function(msg)
  RogueGameData.SetThemeInfo(msg.themeInfo)
  RogueGameData.SetChapterInfo(msg.chapterInfo)
```

---

## Rouge/RogueGameSettlementWindow.lua.lua
**Functions:**
- wordlist.itemRenderer
- cardlist.itemRenderer
- treasurelist.itemRenderer
- halidomlist.itemRenderer
- infolist.itemRenderer
- infolist.itemRenderer
- RogueGameSettlementWindow.ReInitData
- RogueGameSettlementWindow.OnInit
- RogueGameSettlementWindow.UpdateInfo
- RogueGameSettlementWindow.InitBtn
- RogueGameSettlementWindow.OnClose
**Requires:**
- RogueBuild01_InsideEndDetailsWindowByName
**Snippet:**
```lua
require("RogueBuild01_InsideEndDetailsWindowByName")
local RogueGameSettlementWindow = {}
local uis, contentPane, settlementInfo, rogueRecord, themeInfo
local STRENGTHENABLE_ATTR = {
  CardAttribute.GetIdByName(ATTR_ENUM.atk),
  CardAttribute.GetIdByName(ATTR_ENUM.def),
  CardAttribute.GetIdByName(ATTR_ENUM.max_hp)
}
local DETAILS_INFO_LOOKUP = {
  {
```

---

## Rouge/RogueGameShopPurchaseWindow.lua.lua
**Functions:**
- RogueGameShopPurchaseWindow.ReInitData
- RogueGameShopPurchaseWindow.OnInit
- RogueGameShopPurchaseWindow.UpdateInfo
- wordlist.itemRenderer
- list.itemRenderer
- list.itemRenderer
- RogueGameShopPurchaseWindow.InitBtn
- RogueGameShopPurchaseWindow.OnClose
**Requires:**
- RogueBuild01_ShopBuyWindowByName
**Snippet:**
```lua
require("RogueBuild01_ShopBuyWindowByName")
local RogueGameShopPurchaseWindow = {}
local uis, contentPane, treasureId

function RogueGameShopPurchaseWindow.ReInitData()
end

function RogueGameShopPurchaseWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RogueGameShopPurchaseWindow.package, WinResConfig.RogueGameShopPurchaseWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/RogueGameShopWindow.lua.lua
**Functions:**
- RefreshResetBtnStatus
- RogueGameShopWindow.ReInitData
- RogueGameShopWindow.OnInit
- RogueGameShopWindow.UpdateInfo
- RogueGameShopWindow.InitBtn
- RogueGameShopWindow.OnClose
- RogueGameShopWindow.HandleMessage
**Requires:**
- RogueBuild01_InsideShopWindowByName
**Snippet:**
```lua
require("RogueBuild01_InsideShopWindowByName")
local RogueGameShopWindow = {}
local uis, contentPane, rogueNode, selectedShopId, treasureIdList
local ShopTreasureItemRenderer = function(i, gcmp)
  local item = gcmp:GetChild("Item")
  item.alpha = 0
  PlayUITrans(gcmp, "up", nil, i * 0.03)
  local id = treasureIdList[i + 1]
  local conf = TableData.GetConfig(id, "BaseRogueTreasure")
  item:GetChild("PicLoader").url = UIUtil.GetResUrl(conf.icon)
```

---

## Rouge/RogueGameStartChoiceCardListWindow.lua.lua
**Functions:**
- RogueGameStartChoiceCardListWindow.ReInitData
- RogueGameStartChoiceCardListWindow.OnInit
- RogueGameStartChoiceCardListWindow.UpdateInfo
- RogueGameStartChoiceCardListWindow.InitBtn
- RogueGameStartChoiceCardListWindow.OnClose
**Requires:**
- RogueBuild01_StartChoiceCardListWindowByName
**Snippet:**
```lua
require("RogueBuild01_StartChoiceCardListWindowByName")
local RogueGameStartChoiceCardListWindow = {}
local uis, contentPane, cardsBuffer, occupationsBuffer, selectedCards, templateSelectedCards
local CARD_MASK = -1
local recruitCallback, cost_lookup
local DefaultSort = function(x, y)
  local a, b = x.info or x, y.info or y
  if a.level == b.level then
    local aData = CardData.GetBaseConfig(a.cardId)
    local bData = CardData.GetBaseConfig(b.cardId)
```

---

## Rouge/RogueGameStartChoiceWindow.lua.lua
**Functions:**
- list.itemRenderer
- RogueGameStartChoiceWindow.ReInitData
- RogueGameStartChoiceWindow.OnInit
- RogueGameStartChoiceWindow.UpdateInfo
- RogueGameStartChoiceWindow.InitBtn
- RogueGameStartChoiceWindow.OnShown
- RogueGameStartChoiceWindow.OnClose
- RogueGameStartChoiceWindow.HandleMessage
**Requires:**
- RogueBuild01_InsideStartChoiceWindowByName
**Snippet:**
```lua
require("RogueBuild01_InsideStartChoiceWindowByName")
local RogueGameStartChoiceWindow = {}
local uis, contentPane, selectedCards, selectedTreasures, defaultSelectTabIndex
local CardItemRenderer = function(i, gcmp)
  local index = i + 1
  local card = gcmp:GetChild("Card")
  card.alpha = 0
  PlayUITrans(gcmp, "up", nil, i * 0.03)
  TimerUtil.setTimeout(i * 0.03, function()
    SoundUtil.PlayUISfx(SOUND_EVENT_ENUM.CARD_LIST_MOVE)
```

---

## Rouge/RogueGameStartWindow.lua.lua
**Functions:**
- RogueGameStartWindow.ReInitData
- RogueGameStartWindow.OnInit
- RogueGameStartWindow.UpdateInfo
- RogueGameStartWindow.InitBtn
- RogueGameStartWindow.OnClose
**Requires:**
- RogueBuild01_InsideStartWindowByName
**Snippet:**
```lua
require("RogueBuild01_InsideStartWindowByName")
local RogueGameStartWindow = {}
local uis, contentPane, tweenId

function RogueGameStartWindow.ReInitData()
end

function RogueGameStartWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RogueGameStartWindow.package, WinResConfig.RogueGameStartWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/RogueGameStoryUtils.lua.lua
**Functions:**
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

## Rouge/RogueGameTransitionWindow.lua.lua
**Functions:**
- RogueGameTransitionWindow.ReInitData
- RogueGameTransitionWindow.OnInit
- RogueGameTransitionWindow.UpdateInfo
- RogueGameTransitionWindow.InitBtn
- RogueGameTransitionWindow.OnClose
**Requires:**
- RogueBuild01_InsideMidWindowByName
**Snippet:**
```lua
require("RogueBuild01_InsideMidWindowByName")
local RogueGameTransitionWindow = {}
local uis, contentPane
local DURATION = 2.5
local tweenId, chapterId

function RogueGameTransitionWindow.ReInitData()
end

function RogueGameTransitionWindow.OnInit(bridgeObj)
```

---

## Rouge/RogueGameUnlockHalidomTipsWindow.lua.lua
**Functions:**
- list.itemRenderer
- RogueGameUnlockHalidomTipsWindow.ReInitData
- RogueGameUnlockHalidomTipsWindow.OnInit
- RogueGameUnlockHalidomTipsWindow.UpdateInfo
- RogueGameUnlockHalidomTipsWindow.InitBtn
- RogueGameUnlockHalidomTipsWindow.OnClose
**Requires:**
- RogueBuild01_InsideSacredWindowByName
**Snippet:**
```lua
require("RogueBuild01_InsideSacredWindowByName")
local RogueGameUnlockHalidomTipsWindow = {}
local uis, contentPane, halidomList, lookover
local DisplayHalidomInfo = function(halidomId)
  local panel = uis.Main.Tips
  local conf = TableData.GetConfig(halidomId, "BaseRogueHoly")
  panel.Name.NameTxt.text = conf.name()
  panel.Item.PicLoader.url = UIUtil.GetResUrl(conf.icon)
  if not lookover then
    SoundUtil.PlayUISfx("event:/sfx/sfx_ui/ui_sys/ui_yuantu_holy_reward")
```

---

## Rouge/RogueGiveUpWindow.lua.lua
**Functions:**
- RogueGiveUpWindow.ReInitData
- RogueGiveUpWindow.OnInit
- RogueGiveUpWindow.UpdateInfo
- RogueGiveUpWindow.InitBtn
- RogueGiveUpWindow.ClickClose
- RogueGiveUpWindow.OnClose
**Requires:**
- RogueBuild01_GiveUpWindowByName
**Snippet:**
```lua
require("RogueBuild01_GiveUpWindowByName")
local RogueGiveUpWindow = {}
local uis, contentPane

function RogueGiveUpWindow.ReInitData()
end

function RogueGiveUpWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RogueGiveUpWindow.package, WinResConfig.RogueGiveUpWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/RogueHandBookWindow.lua.lua
**Functions:**
- RogueHandBookWindow.ReInitData
- RogueHandBookWindow.OnInit
- RogueHandBookWindow.UpdateInfo
- RogueHandBookWindow.InitBtn
- RogueHandBookWindow.getLen
- RogueHandBookWindow.UpdateRed
- RogueHandBookWindow.OnShown
- RogueHandBookWindow.OnClose
**Requires:**
- RogueBuild01_HandBookWindowByName
**Snippet:**
```lua
require("RogueBuild01_HandBookWindowByName")
local RogueHandBookWindow = {}
local uis, contentPane, jumpTb

function RogueHandBookWindow.ReInitData()
end

function RogueHandBookWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RogueHandBookWindow.package, WinResConfig.RogueHandBookWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/RogueLetterRewardWindow.lua.lua
**Functions:**
- RogueLetterRewardWindow.ReInitData
- RogueLetterRewardWindow.OnInit
- RogueLetterRewardWindow.InitRedDot
- RogueLetterRewardWindow.UpdateWeekTask
- taskTips.ContentList.itemRenderer
- RogueLetterRewardWindow.UpdateWeekReward
- taskTips.Progress.ItemList.itemRenderer
- itemList.itemRenderer
- RogueLetterRewardWindow.CheckWeekReward
- RogueLetterRewardWindow.UpdateUpTask
- tips.ContentList.itemRenderer
- RogueLetterRewardWindow.CanPreChapterUnlock
- RogueLetterRewardWindow.GetUnlock
- RogueLetterRewardWindow.CanTaskReWard
- RogueLetterRewardWindow.GetChapterData
- RogueLetterRewardWindow.InitBtn
- RogueLetterRewardWindow.OnShown
- RogueLetterRewardWindow.OnClose
- RogueLetterRewardWindow.HandleMessage
**Requires:**
- RogueBuild01_LetterRewardWindowByName
**Snippet:**
```lua
require("RogueBuild01_LetterRewardWindowByName")
local RogueLetterRewardWindow = {}
local uis, contentPane, jumpTb, letterData, allTrends

function RogueLetterRewardWindow.ReInitData()
end

function RogueLetterRewardWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RogueLetterRewardWindow.package, WinResConfig.RogueLetterRewardWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/RogueLetterTipsWindow.lua.lua
**Functions:**
- RogueLetterTipsWindow.ReInitData
- RogueLetterTipsWindow.OnInit
- RogueLetterTipsWindow.UpdateInfo
- wordList.itemRenderer
- tips.ChatList.itemRenderer
- RogueLetterTipsWindow.GetAllStorySimple
- RogueLetterTipsWindow.ClickClose
- RogueLetterTipsWindow.InitBtn
- RogueLetterTipsWindow.OnClose
**Requires:**
- RogueBuild01_LetterTipsWindowByName
**Snippet:**
```lua
require("RogueBuild01_LetterTipsWindowByName")
local RogueLetterTipsWindow = {}
local uis, contentPane, trendsData

function RogueLetterTipsWindow.ReInitData()
end

function RogueLetterTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RogueLetterTipsWindow.package, WinResConfig.RogueLetterTipsWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/RogueMgr.lua.lua
**Functions:**
- RogueMgr.GetTreasureType
- RogueMgr.GetTreasureLevel
- RogueMgr.GetRogueTrendBar
- RogueMgr.ClearNewByType
- RogueMgr.CanMapNew
- RogueMgr.CanEventNew
- RogueMgr.CanEndindNew
- RogueMgr.CanTalentNew
- RogueMgr.GetDifficultyData
- RogueMgr.GetWeekTarget
**Snippet:**
```lua
RogueMgr = {difficultyLevel = 0}

function RogueMgr.GetTreasureType(type)
  local data = {
    [1] = T(1404),
    [2] = T(1405),
    [3] = T(1406),
    [4] = T(1407),
    [5] = T(1408),
    [6] = T(1409),
```

---

## Rouge/RogueScoreDetailsWindow.lua.lua
**Functions:**
- RogueScoreDetailsWindow.ReInitData
- RogueScoreDetailsWindow.OnInit
- RogueScoreDetailsWindow.UpdateInfo
- cardList.itemRenderer
- treasureList.itemRenderer
- holyList.itemRenderer
- RogueScoreDetailsWindow.ShowAttribute
- RogueScoreDetailsWindow.GetDifficultyTxt
- RogueScoreDetailsWindow.InitBtn
- RogueScoreDetailsWindow.OnClose
**Requires:**
- RogueBuild01_ScoreDetailsWindowByName
**Snippet:**
```lua
require("RogueBuild01_ScoreDetailsWindowByName")
local RogueScoreDetailsWindow = {}
local uis, contentPane, jumpTb

function RogueScoreDetailsWindow.ReInitData()
end

function RogueScoreDetailsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RogueScoreDetailsWindow.package, WinResConfig.RogueScoreDetailsWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/RogueScoreRewardWindow.lua.lua
**Functions:**
- RogueScoreRewardWindow.ReInitData
- RogueScoreRewardWindow.OnInit
- RogueScoreRewardWindow.UpdateInfo
- list.itemRenderer
- RogueScoreRewardWindow.ShowOneItem
- list.itemRenderer
- rewardList.itemRenderer
- RogueScoreRewardWindow.ShowLeftInfo
- RogueScoreRewardWindow.GetPhaseTitle
- RogueScoreRewardWindow.GetRogueLevelData
- RogueScoreRewardWindow.GetData
- RogueScoreRewardWindow.InitBtn
- RogueScoreRewardWindow.OnClose
- RogueScoreRewardWindow.HandleMessage
**Requires:**
- RogueBuild01_ScoreRewardWindowByName
**Snippet:**
```lua
require("RogueBuild01_ScoreRewardWindowByName")
local RogueScoreRewardWindow = {}
local uis, contentPane, jumpTb, rewardData, themeInfo

function RogueScoreRewardWindow.ReInitData()
end

function RogueScoreRewardWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RogueScoreRewardWindow.package, WinResConfig.RogueScoreRewardWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/RogueScriptList.lua.lua
**Requires:**
- RogueData
- RogueService
- RogueMgr
- RogueGameConst
- RogueGameData
- RogueGameMgr
- RogueGameService
- RogueGameStoryUtils
**Snippet:**
```lua
local require = require
require("RogueData")
require("RogueService")
require("RogueMgr")
require("RogueGameConst")
RogueGameData = require("RogueGameData")
RogueGameMgr = require("RogueGameMgr")
RogueGameService = require("RogueGameService")
RogueGameStoryUtils = require("RogueGameStoryUtils")
```

---

## Rouge/RogueService.lua.lua
**Functions:**
- RogueService.Init
- RogueService.GetRogueInfoReq
- RogueService.GetRogueInfoRsp
- RogueService.ActivateRogueTalentReq
- RogueService.ActivateRogueTalentRsp
- RogueService.FetchRogueThemeLevelRewardReq
- RogueService.FetchRogueThemeLevelRewardRsp
- RogueService.GetRogueTopScoreRecordReq
- RogueService.GetRogueTopScoreRecordRsp
- RogueService.FetchRogueTrendTaskRewardReq
- RogueService.FetchRogueTrendTaskRewardRsp
- RogueService.GetRogueTrendsReq
- RogueService.GetRogueTrendsRsp
- RogueService.GetRogueAllPicReq
- RogueService.GetRogueAllPicRsp
- RogueService.GetRoguePicNewStateReq
- RogueService.GetRoguePicNewStateRsp
- RogueService.ClearRoguePicNewStateReq
- RogueService.ClearRoguePicNewStateRsp
- RogueService.QuitRogueGameReq
- RogueService.QuitRogueGameRsp
- RogueService.GetCycleTaskInfoReq
- RogueService.GetCycleTaskInfoRsp
- RogueService.CycleTaskRewardReq
- RogueService.CycleTaskRewardRsp
- RogueService.SweepReq
- RogueService.SweepRsp
**Snippet:**
```lua
RogueService = {}

function RogueService.Init()
  Net.AddListener(Proto.MsgName.GetRogueInfoRsp, RogueService.GetRogueInfoRsp)
  Net.AddListener(Proto.MsgName.ActivateRogueTalentRsp, RogueService.ActivateRogueTalentRsp)
  Net.AddListener(Proto.MsgName.FetchRogueThemeLevelRewardRsp, RogueService.FetchRogueThemeLevelRewardRsp)
  Net.AddListener(Proto.MsgName.GetRogueTopScoreRecordRsp, RogueService.GetRogueTopScoreRecordRsp)
  Net.AddListener(Proto.MsgName.GetRogueAllPicRsp, RogueService.GetRogueAllPicRsp)
  Net.AddListener(Proto.MsgName.FetchRogueTrendTaskRewardRsp, RogueService.FetchRogueTrendTaskRewardRsp)
  Net.AddListener(Proto.MsgName.GetRoguePicNewStateRsp, RogueService.GetRoguePicNewStateRsp)
```

---

## Rouge/RogueSweepWindow.lua.lua
**Functions:**
- RogueSweepWindow.ReInitData
- RogueSweepWindow.OnInit
- RogueSweepWindow.UpdateInfo
- RogueSweepWindow.InitBtn
- RogueSweepWindow.OnClose
**Requires:**
- RogueBuild01_SweepWindowByName
**Snippet:**
```lua
require("RogueBuild01_SweepWindowByName")
local RogueSweepWindow = {}
local uis, contentPane, sweepResult

function RogueSweepWindow.ReInitData()
end

function RogueSweepWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RogueSweepWindow.package, WinResConfig.RogueSweepWindow.comName, function(com)
    contentPane = com
```

---

## Rouge/RogueTalentWindow.lua.lua
**Functions:**
- RogueTalentWindow.ReInitData
- RogueTalentWindow.OnInit
- RogueTalentWindow.UpdateInfo
- uis.Main.TreeList.itemRenderer
- ordinaryTips.WordList.itemRenderer
- specialList.itemRenderer
- RogueTalentWindow.SetSpecialPre
- RogueTalentWindow.InitTalentUp
- RogueTalentWindow.ShowTalentInfo
- RogueTalentWindow.PreIsContain
- RogueTalentWindow.GetConfigAttribute
- RogueTalentWindow.GetallAttributeVaule
- RogueTalentWindow.GetallAttributeName
- RogueTalentWindow.InitBtn
- RogueTalentWindow.OnClose
**Requires:**
- RogueBuild01_TalentWindowByName
**Snippet:**
```lua
require("RogueBuild01_TalentWindowByName")
local RogueTalentWindow = {}
local uis, contentPane, jumpTb, talentIds, talentItemId, rogueThemeData, themeInfo, lastItem, specialDes
local effectPath = {
  [1] = "Assets/Art/Effects/Prefab/UI_prefab/Rugel/FX_ui_RogueEquipment_levelup_f.prefab",
  [2] = "Assets/Art/Effects/Prefab/UI_prefab/Rugel/FX_ui_RogueEquipment_levelup_y.prefab",
  [3] = "Assets/Art/Effects/Prefab/UI_prefab/Rugel/FX_ui_RogueEquipment_levelup_s.prefab",
  [4] = "Assets/Art/Effects/Prefab/UI_prefab/Rugel/FX_ui_RogueEquipment_levelup_y_huge.prefab"
}

```

---

## Rouge/RogueWindow.lua.lua
**Functions:**
- RogueWindow.ReInitData
- RogueWindow.OnInit
- RogueWindow.InitRedDot
- RogueWindow.UpdateInfo
- RogueWindow.ShowMapNew
- RogueWindow.UpdateTxt
- RogueWindow.InitBtn
- RogueWindow.OnShown
- RogueWindow.OnClose
- RogueWindow.HandleMessage
**Requires:**
- RogueBuild01_RogueWindowByName
**Snippet:**
```lua
require("RogueBuild01_RogueWindowByName")
local RogueWindow = {}
local uis, contentPane, jumpTb, rogueThemeData, rogueInfo, tween

function RogueWindow.ReInitData()
end

function RogueWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.RogueWindow.package, WinResConfig.RogueWindow.comName, function(com)
    contentPane = com
```

---
