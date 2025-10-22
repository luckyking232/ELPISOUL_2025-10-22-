# Activty/baseact

## Activty/baseact/Activity10BossBattleWindow.lua.lua
**Functions:**
- Activity10BossBattleWindow.ReInitData
- Activity10BossBattleWindow.OnInit
- Activity10BossBattleWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity10BossBattleWindow.FormatRemainTime
- Activity10BossBattleWindow.GetChapter
- Activity10BossBattleWindow.InitBtn
- Activity10BossBattleWindow.CloseWindow
- Activity10BossBattleWindow.OnClose
**Requires:**
- ActivityDungeon1010_BossBattleWindowByName
**Snippet:**
```lua
require("ActivityDungeon1010_BossBattleWindowByName")
local Activity10BossBattleWindow = {}
local uis, contentPane, activityInfo

function Activity10BossBattleWindow.ReInitData()
end

function Activity10BossBattleWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity10BossBattleWindow.package, WinResConfig.Activity10BossBattleWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity10BuyLevelDesWindow.lua.lua
**Functions:**
- Activity10BuyLevelDesWindow.ReInitData
- Activity10BuyLevelDesWindow.OnInit
- Activity10BuyLevelDesWindow.ShowAssetsTips
- Activity10BuyLevelDesWindow.UpdateTextDisplay
- Activity10BuyLevelDesWindow.Init
- Activity10BuyLevelDesWindow.GetGold
- Activity10BuyLevelDesWindow.ShowReward
- list.itemRenderer
- Activity10BuyLevelDesWindow.GetRewardItem
- Activity10BuyLevelDesWindow.GetLvData
- Activity10BuyLevelDesWindow.GetRewardLvData
- Activity10BuyLevelDesWindow.GetRewardByPhaseId
- Activity10BuyLevelDesWindow.BuyLevelRsp
- Activity10BuyLevelDesWindow.InitBtn
- waitFun
- Activity10BuyLevelDesWindow.HandleMessage
- Activity10BuyLevelDesWindow.OnShown
- Activity10BuyLevelDesWindow.OnClose
**Requires:**
- ActivityDungeon1010_BuyLevelDesWindowByName
**Snippet:**
```lua
require("ActivityDungeon1010_BuyLevelDesWindowByName")
local Activity10BuyLevelDesWindow = {}
local uis, contentPane, lvData, curLv, buyNum, itemId, lvMax, waitFun, rewardData, itemSort, transPlay, firstPlay, tatalGold, passInfo

function Activity10BuyLevelDesWindow.ReInitData()
end

function Activity10BuyLevelDesWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity10BuyLevelDesWindow.package, WinResConfig.Activity10BuyLevelDesWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity10ChallengeWindow.lua.lua
**Functions:**
- Activity10ChallengeWindow.ReInitData
- Activity10ChallengeWindow.OnInit
- Activity10ChallengeWindow.UpdateInfo
- uis.Main.ChapterList.itemRenderer
- Activity10ChallengeWindow.ShoweStage
- Activity10ChallengeWindow.StageItemClick
- Activity10ChallengeWindow.ShopInfo
- Activity10ChallengeWindow.GetChapterPassById
- Activity10ChallengeWindow.GetCurStage
- Activity10ChallengeWindow.GetFirstChapter
- Activity10ChallengeWindow.GetAllChapterId
- Activity10ChallengeWindow.InitBtn
- Activity10ChallengeWindow.CloseWindow
- Activity10ChallengeWindow.OnShown
- Activity10ChallengeWindow.OnClose
**Requires:**
- ActivityDungeon1010_ChallengeWindowByName
**Snippet:**
```lua
require("ActivityDungeon1010_ChallengeWindowByName")
local Activity10ChallengeWindow = {}
local uis, contentPane, activityInfo, scrollingTween

function Activity10ChallengeWindow.ReInitData()
end

function Activity10ChallengeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity10ChallengeWindow.package, WinResConfig.Activity10ChallengeWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity10DungeonWindow.lua.lua
**Functions:**
- Activity10DungeonWindow.ReInitData
- Activity10DungeonWindow.OnInit
- Activity10DungeonWindow.LoadBg
- Activity10DungeonWindow.InitRedDot
- Activity10DungeonWindow.UpdateInfo
- Activity10DungeonWindow.InitBtnTxt
- Activity10DungeonWindow.InitBtn
- Activity10DungeonWindow.OnShown
- Activity10DungeonWindow.OnClose
- Activity10DungeonWindow.HandleMessage
**Requires:**
- ActivityDungeon1010_ActivityDungeonWindowByName
**Snippet:**
```lua
require("ActivityDungeon1010_ActivityDungeonWindowByName")
local Activity10DungeonWindow = {}
local uis, contentPane, jumpTb, configData, activityInfo, effect
local InitMiniGameInfo = function()
  local data = ActivityDungeonData.GetActivityData()
  if data.id == 70440010 then
    ld("Activity10_MiniGame")
    Activity10_MiniGameService.MiniGameInfoReq(function()
      RedDotMgr.AddNode({
        windowName = WinResConfig.Activity10DungeonWindow.name,
```

---

## Activty/baseact/Activity10MaterialWindow.lua.lua
**Functions:**
- Activity10MaterialWindow.ReInitData
- Activity10MaterialWindow.OnInit
- Activity10MaterialWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity10MaterialWindow.GetChapter
- Activity10MaterialWindow.GetMaxCount
- Activity10MaterialWindow.InitBtn
- Activity10MaterialWindow.CloseWindow
- Activity10MaterialWindow.OnShown
- Activity10MaterialWindow.OnClose
**Requires:**
- ActivityDungeon1010_MaterialWindowByName
**Snippet:**
```lua
require("ActivityDungeon1010_MaterialWindowByName")
local Activity10MaterialWindow = {}
local uis, contentPane, activityInfo, maxCount, posX

function Activity10MaterialWindow.ReInitData()
end

function Activity10MaterialWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity10MaterialWindow.package, WinResConfig.Activity10MaterialWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity10MiniExplainWindow.lua.lua
**Functions:**
- Activity10MiniExplainWindow.ReInitData
- Activity10MiniExplainWindow.OnInit
- Activity10MiniExplainWindow.UpdateInfo
- Activity10MiniExplainWindow.ShowListWord
- list.itemRenderer
- Activity10MiniExplainWindow.InitBtn
- Activity10MiniExplainWindow.OnClose
**Requires:**
- ActivityDungeon1010_MiniExplainWindowByName
**Snippet:**
```lua
require("ActivityDungeon1010_MiniExplainWindowByName")
local Activity10MiniExplainWindow = {}
local uis, contentPane, closeCallback

function Activity10MiniExplainWindow.ReInitData()
end

function Activity10MiniExplainWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity10MiniExplainWindow.package, WinResConfig.Activity10MiniExplainWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity10MiniGameMainWindow.lua.lua
**Functions:**
- RefreshPanelInfo
- Activity10MiniGameMainWindow.ReInitData
- Activity10MiniGameMainWindow.OnInit
- Activity10MiniGameMainWindow.UpdateInfo
- Activity10MiniGameMainWindow.InitBtn
- Activity10MiniGameMainWindow.OnClose
- Activity10MiniGameMainWindow.HandleMessage
**Requires:**
- ActivityDungeon1010_MiniGameWindowByName
**Snippet:**
```lua
require("ActivityDungeon1010_MiniGameWindowByName")
ld("Activity10_MiniGame")
local Activity10MiniGameMainWindow = {}
local uis, contentPane

local function RefreshPanelInfo()
  local info = Activity10_MiniGameData.GetMiniGameInfo()
  local conf = TableData.GetConfig(Activity10_MiniGameData.gameId, "BaseActivityStageGame")
  local str = conf.game_day_reward[1]
  local splits = Split(str, ":")
```

---

## Activty/baseact/Activity10MiniGameSubmitWindow.lua.lua
**Functions:**
- Activity10MiniGameSubmitWindow.ReInitData
- Activity10MiniGameSubmitWindow.OnInit
- Activity10MiniGameSubmitWindow.UpdateInfo
- Activity10MiniGameSubmitWindow.InitBtn
- Activity10MiniGameSubmitWindow.OnClose
**Requires:**
- ActivityDungeon1010_MiniStart_EndRewardWindowByName
**Snippet:**
```lua
require("ActivityDungeon1010_MiniStart_EndRewardWindowByName")
local Activity10MiniGameSubmitWindow = {}
local uis, contentPane, nowIntegral

function Activity10MiniGameSubmitWindow.ReInitData()
end

function Activity10MiniGameSubmitWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity10MiniGameSubmitWindow.package, WinResConfig.Activity10MiniGameSubmitWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity10MiniGameTaskWindow.lua.lua
**Functions:**
- RefreshRewardList
- list.itemRenderer
- itemlist.itemRenderer
- Activity10MiniGameTaskWindow.ReInitData
- Activity10MiniGameTaskWindow.OnInit
- Activity10MiniGameTaskWindow.UpdateInfo
- Activity10MiniGameTaskWindow.InitBtn
- Activity10MiniGameTaskWindow.OnClose
**Requires:**
- ActivityDungeon1010_MiniTaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1010_MiniTaskWindowByName")
local Activity10MiniGameTaskWindow = {}
local uis, contentPane

local function RefreshRewardList()
  local info = Activity10_MiniGameData.GetMiniGameInfo()
  local minigame_tasks = info.taskList
  local list = uis.Main.TipsList
  list:SetVirtual()
  
```

---

## Activty/baseact/Activity10MiniGameWindow.lua.lua
**Functions:**
- Activity10MiniGameWindow.ReInitData
- Activity10MiniGameWindow.OnInit
- Activity10MiniGameWindow.ShowStartTips
- Activity10MiniGameWindow.UpdateInfo
- Activity10MiniGameWindow.Update
- Activity10MiniGameWindow.Resurrection
- Activity10MiniGameWindow.CheckDie
- Activity10MiniGameWindow.CheckEatItem
- Activity10MiniGameWindow.PlayItemAnim
- Activity10MiniGameWindow.Overlaps
- Activity10MiniGameWindow.Move
- Activity10MiniGameWindow.RefreshScore
- Activity10MiniGameWindow.CreateBgCom
- bgClass:LoadBg
- bgClass:Move
- bgClass.Dispose
- bgClass:DisposeAll
- Activity10MiniGameWindow.CreateBarrier
- Activity10MiniGameWindow.GetDownNum
- Activity10MiniGameWindow.GetCreateItemInfo
- Activity10MiniGameWindow.DisposeBarrier
- Activity10MiniGameWindow.GetConfData
- Activity10MiniGameWindow.GetConfig
- Activity10MiniGameWindow.GetRandomNum
- Activity10MiniGameWindow.GetItemConfig
- Activity10MiniGameWindow.OnGameOver
- Activity10MiniGameWindow.OnNext
- Activity10MiniGameWindow.InitBtn
- Activity10MiniGameWindow.HandleMessage
- Activity10MiniGameWindow.OnClose
**Requires:**
- ActivityDungeon1010_MiniGameStartWindowByName
**Snippet:**
```lua
require("ActivityDungeon1010_MiniGameStartWindowByName")
local Activity10MiniGameWindow = {}
local uis, contentPane, hpTxt, flyCom, bgComInfo, mapConfData, bgPrefab
local bgWidth = 16.68
local curConfData, allBarrier, playerX, barrierDis, dieDownY, itemConfig, itemIndex, itemCreateDis, itemConfIndex, score, hp, flyObj, stop, rootWidth, mapConfMax, mapLayer, itemInfo, detailsShow, stopDwon, targetY, fristGuide, tipsCom, downArrInfo, lastW, showPlay, curItemType
local itemEffectNum = {}
local tweenDie, stopTween, waitTween
local moveSpeed = 0
local downAddSpeed = 1380
local defaultSpeedUp = -400
```

---

## Activty/baseact/Activity10MiniRankWindow.lua.lua
**Functions:**
- Activity10MiniRankWindow.ReInitData
- Activity10MiniRankWindow.OnInit
- Activity10MiniRankWindow.UpdateInfo
- list.itemRenderer
- Activity10MiniRankWindow.InitBtn
- Activity10MiniRankWindow.ClosWindow
- Activity10MiniRankWindow.OnClose
**Requires:**
- ActivityDungeon1010_MiniRankWindowByName
**Snippet:**
```lua
require("ActivityDungeon1010_MiniRankWindowByName")
local Activity10MiniRankWindow = {}
local uis, contentPane

function Activity10MiniRankWindow.ReInitData()
end

function Activity10MiniRankWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity10MiniRankWindow.package, WinResConfig.Activity10MiniRankWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity10PassportLevelUpTipsWindow.lua.lua
**Functions:**
- Activity10PassportLevelUpTipsWindow.ReInitData
- Activity10PassportLevelUpTipsWindow.OnInit
- Activity10PassportLevelUpTipsWindow.UpdateInfo
- Activity10PassportLevelUpTipsWindow.InitBtn
- Activity10PassportLevelUpTipsWindow.OnClose
**Requires:**
- ActivityDungeon1010_PassportUp_LevelUpTipsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1010_PassportUp_LevelUpTipsWindowByName")
local Activity10PassportLevelUpTipsWindow = {}
local uis, contentPane, lv

function Activity10PassportLevelUpTipsWindow.ReInitData()
end

function Activity10PassportLevelUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity10PassportLevelUpTipsWindow.package, WinResConfig.Activity10PassportLevelUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity10PassportWindow.lua.lua
**Functions:**
- Activity10PassportWindow.ReInitData
- Activity10PassportWindow.OnInit
- Activity10PassportWindow.UpdateTextDisplay
- Activity10PassportWindow.InitPassport
- uis.Main.TabRegion.TabList.itemRenderer
- Activity10PassportWindow.InitEffect
- Activity10PassportWindow.InitLv
- Activity10PassportWindow.ShowLevelUp
- Activity10PassportWindow.SaveLevel
- Activity10PassportWindow.GetRewardByLv
- Activity10PassportWindow.GetRewardNum
- Activity10PassportWindow.IsGetAllReward
- Activity10PassportWindow.ShowReward
- Activity10PassportWindow.GetUpdateLv
- Activity10PassportWindow.RefreshListReward
- Activity10PassportWindow.CheckItemTime
- Activity10PassportWindow.ShowQuitTips
- Activity10PassportWindow.RefreshUI
- Activity10PassportWindow.GetExpMxp
- Activity10PassportWindow.SetLevelInfo
- Activity10PassportWindow.InitList
- list.itemRenderer
- Activity10PassportWindow.SetListPos
- Activity10PassportWindow.RefreshReward
- Activity10PassportWindow.ShowGetEffect
- Activity10PassportWindow.RewardItemClick
- Activity10PassportWindow.IsReward
- Activity10PassportWindow.RefreshRewardFirst
- Activity10PassportWindow.RefreshRewardEnd
- Activity10PassportWindow.ShowState
- Activity10PassportWindow.RefreshRewardShow
- Activity10PassportWindow.RefreshRewardState
- Activity10PassportWindow.PassportActivate
- Activity10PassportWindow.CloseWindow
- Activity10PassportWindow.InitBtn
- Activity10PassportWindow.ShowExpBarAnim
- Activity10PassportWindow.InitTask
- list.itemRenderer
- Activity10PassportWindow.InitClothes
- clothes.BuyReward.RewardList.itemRenderer
- Activity10PassportWindow.SetLastLv
- Activity10PassportWindow.PlayFirstRewardEffect
- Activity10PassportWindow.PlayEndRewardEffect
- Activity10PassportWindow.HandleMessage
- Activity10PassportWindow.OnShown
- Activity10PassportWindow.OnClose
**Requires:**
- ActivityDungeon1010_PassportWindowByName
**Snippet:**
```lua
require("ActivityDungeon1010_PassportWindowByName")
local Activity10PassportWindow = {}
local uis, contentPane, passInfo, lvMax, modelType, expMax, rewardData, rewardType, rewardLv, listPage, passLv, jumpTb, isShowAllGet, passPortConfig, lvTween, lastLv, waitMessageId, newPassPort, animTween

function Activity10PassportWindow.ReInitData()
end

function Activity10PassportWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity10PassportWindow.package, WinResConfig.Activity10PassportWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity10PlotWindow.lua.lua
**Functions:**
- Activity10PlotWindow.ReInitData
- Activity10PlotWindow.OnInit
- Activity10PlotWindow.UpdateInfo
- list.itemRenderer
- Activity10PlotWindow.InitBtn
- Activity10PlotWindow.CloseWindow
- Activity10PlotWindow.OnClose
**Requires:**
- ActivityDungeon1010_PlotWindowByName
**Snippet:**
```lua
require("ActivityDungeon1010_PlotWindowByName")
local Activity10PlotWindow = {}
local uis, contentPane, configData

function Activity10PlotWindow.ReInitData()
end

function Activity10PlotWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity10PlotWindow.package, WinResConfig.Activity10PlotWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity10ShopWindow.lua.lua
**Functions:**
- Activity10ShopWindow.ReInitData
- Activity10ShopWindow.OnInit
- Activity10ShopWindow.UpdateInfo
- uis.Main.ItemList.itemRenderer
- Activity10ShopWindow.ShowItem
- list.itemRenderer
- Activity10ShopWindow.ShowOneReward
- list.itemRenderer
- Activity10ShopWindow.GetShopGrid
- Activity10ShopWindow.InitBtn
- Activity10ShopWindow.CloseWindow
- Activity10ShopWindow.OnClose
- Activity10ShopWindow.HandleMessage
**Requires:**
- ActivityDungeon1010_ShopWindowByName
**Snippet:**
```lua
require("ActivityDungeon1010_ShopWindowByName")
local Activity10ShopWindow = {}
local uis, contentPane, activityInfo, tempAssetsTips

function Activity10ShopWindow.ReInitData()
end

function Activity10ShopWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity10ShopWindow.package, WinResConfig.Activity10ShopWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity10SignWindow.lua.lua
**Functions:**
- Activity10SignWindow.ReInitData
- Activity10SignWindow.OnInit
- Activity10SignWindow.UpdateInfo
- list.RewardList.itemRenderer
- Activity10SignWindow.ShowAllItemFrame
- Activity10SignWindow.GetRewardData
- Activity10SignWindow.InitBtn
- Activity10SignWindow.CloseWindow
- Activity10SignWindow.OnClose
**Requires:**
- ActivityDungeon1010_SignWindowByName
**Snippet:**
```lua
require("ActivityDungeon1010_SignWindowByName")
local Activity10SignWindow = {}
local uis, contentPane, activityInfo

function Activity10SignWindow.ReInitData()
end

function Activity10SignWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity10SignWindow.package, WinResConfig.Activity10SignWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity10TaskWindow.lua.lua
**Functions:**
- Activity10TaskWindow.ReInitData
- Activity10TaskWindow.OnInit
- Activity10TaskWindow.UpdateInfo
- list.itemRenderer
- rewardList.itemRenderer
- Activity10TaskWindow.GetRewardNum
- Activity10TaskWindow.ShowAllItemFrame
- Activity10TaskWindow.SortTask
- Activity10TaskWindow.InitBtn
- Activity10TaskWindow.CloseWindow
- Activity10TaskWindow.OnClose
**Requires:**
- ActivityDungeon1010_TaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1010_TaskWindowByName")
local Activity10TaskWindow = {}
local uis, contentPane

function Activity10TaskWindow.ReInitData()
end

function Activity10TaskWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity10TaskWindow.package, WinResConfig.Activity10TaskWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity10_MiniGameData.lua.lua
**Functions:**
- Activity10_MiniGameData.SetMiniGameInfo
- Activity10_MiniGameData.GetMiniGameInfo
**Snippet:**
```lua
Activity10_MiniGameData = {gameId = 70441012}
local miniGameInfo

function Activity10_MiniGameData.SetMiniGameInfo(info)
  miniGameInfo = info
end

function Activity10_MiniGameData.GetMiniGameInfo()
  return miniGameInfo
end
```

---

## Activty/baseact/Activity10_MiniGameScriptList.lua.lua
**Requires:**
- Activity10_MiniGameData
- Activity10_MiniGameService
**Snippet:**
```lua
require("Activity10_MiniGameData")
require("Activity10_MiniGameService")
```

---

## Activty/baseact/Activity10_MiniGameService.lua.lua
**Functions:**
- Activity10_MiniGameService.MiniGameInfoReq
- Activity10_MiniGameService.MiniGameInfoRsp
- Activity10_MiniGameService.MiniGameSubmitReq
- Activity10_MiniGameService.MiniGameSubmitRsp
- Activity10_MiniGameService.MiniGameGetDailyRewardReq
- Activity10_MiniGameService.MiniGameGetDailyRewardRsp
- Activity10_MiniGameService.ActivityGetGameTopRankReq
- Activity10_MiniGameService.ActivityGetGameTopRankRsp
- Activity10_MiniGameService.Init
**Snippet:**
```lua
Activity10_MiniGameService = {}
local gameId = Activity10_MiniGameData.gameId

function Activity10_MiniGameService.MiniGameInfoReq(rspCallback)
  local info = ActivityDungeonData.GetActivityInfo()
  local activityId = info.baseInfo.activityId
  Net.Send(Proto.MsgName.ActivityGetMiniGameReq, {gameId = gameId, activityId = activityId}, rspCallback)
end

function Activity10_MiniGameService.MiniGameInfoRsp(msg)
```

---

## Activty/baseact/Activity11BossBattleWindow.lua.lua
**Functions:**
- Activity11BossBattleWindow.ReInitData
- Activity11BossBattleWindow.OnInit
- Activity11BossBattleWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity11BossBattleWindow.FormatRemainTime
- Activity11BossBattleWindow.GetChapter
- Activity11BossBattleWindow.InitBtn
- Activity11BossBattleWindow.CloseWindow
- Activity11BossBattleWindow.OnClose
**Requires:**
- ActivityDungeon1011_BossBattleWindowByName
**Snippet:**
```lua
require("ActivityDungeon1011_BossBattleWindowByName")
local Activity11BossBattleWindow = {}
local uis, contentPane, activityInfo

function Activity11BossBattleWindow.ReInitData()
end

function Activity11BossBattleWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity11BossBattleWindow.package, WinResConfig.Activity11BossBattleWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity11BuyLevelDesWindow.lua.lua
**Functions:**
- Activity11BuyLevelDesWindow.ReInitData
- Activity11BuyLevelDesWindow.OnInit
- Activity11BuyLevelDesWindow.ShowAssetsTips
- Activity11BuyLevelDesWindow.UpdateTextDisplay
- Activity11BuyLevelDesWindow.Init
- Activity11BuyLevelDesWindow.GetGold
- Activity11BuyLevelDesWindow.ShowReward
- list.itemRenderer
- Activity11BuyLevelDesWindow.GetRewardItem
- Activity11BuyLevelDesWindow.GetLvData
- Activity11BuyLevelDesWindow.GetRewardLvData
- Activity11BuyLevelDesWindow.GetRewardByPhaseId
- Activity11BuyLevelDesWindow.BuyLevelRsp
- Activity11BuyLevelDesWindow.InitBtn
- waitFun
- Activity11BuyLevelDesWindow.HandleMessage
- Activity11BuyLevelDesWindow.OnShown
- Activity11BuyLevelDesWindow.OnClose
**Requires:**
- ActivityDungeon1011_BuyLevelDesWindowByName
**Snippet:**
```lua
require("ActivityDungeon1011_BuyLevelDesWindowByName")
local Activity11BuyLevelDesWindow = {}
local uis, contentPane, lvData, curLv, buyNum, itemId, lvMax, waitFun, rewardData, itemSort, transPlay, firstPlay, tatalGold, passInfo

function Activity11BuyLevelDesWindow.ReInitData()
end

function Activity11BuyLevelDesWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity11BuyLevelDesWindow.package, WinResConfig.Activity11BuyLevelDesWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity11ChallengeWindow.lua.lua
**Functions:**
- Activity11ChallengeWindow.ReInitData
- Activity11ChallengeWindow.OnInit
- Activity11ChallengeWindow.UpdateInfo
- uis.Main.ChapterList.itemRenderer
- Activity11ChallengeWindow.ShoweStage
- Activity11ChallengeWindow.StageItemClick
- Activity11ChallengeWindow.ShopInfo
- Activity11ChallengeWindow.GetChapterPassById
- Activity11ChallengeWindow.GetCurStage
- Activity11ChallengeWindow.GetFirstChapter
- Activity11ChallengeWindow.GetAllChapterId
- Activity11ChallengeWindow.InitBtn
- Activity11ChallengeWindow.CloseWindow
- Activity11ChallengeWindow.OnShown
- Activity11ChallengeWindow.OnClose
**Requires:**
- ActivityDungeon1011_ChallengeWindowByName
**Snippet:**
```lua
require("ActivityDungeon1011_ChallengeWindowByName")
local Activity11ChallengeWindow = {}
local uis, contentPane, activityInfo, scrollingTween

function Activity11ChallengeWindow.ReInitData()
end

function Activity11ChallengeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity11ChallengeWindow.package, WinResConfig.Activity11ChallengeWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity11DungeonWindow.lua.lua
**Functions:**
- Activity11DungeonWindow.ReInitData
- Activity11DungeonWindow.OnInit
- Activity11DungeonWindow.LoadBg
- Activity11DungeonWindow.InitRedDot
- Activity11DungeonWindow.UpdateInfo
- Activity11DungeonWindow.InitBtnTxt
- Activity11DungeonWindow.InitBtn
- Activity11DungeonWindow.OnShown
- Activity11DungeonWindow.OnClose
- Activity11DungeonWindow.HandleMessage
**Requires:**
- ActivityDungeon1011_ActivityDungeonWindowByName
**Snippet:**
```lua
require("ActivityDungeon1011_ActivityDungeonWindowByName")
local Activity11DungeonWindow = {}
local uis, contentPane, jumpTb, configData, activityInfo, effect
local InitMiniGameInfo = function()
  local data = ActivityDungeonData.GetActivityData()
  if data.id == 70440011 then
    ld("Activity11_MiniGame")
    Activity11_MiniGameService.MiniGameInfoReq(function()
      RedDotMgr.AddNode({
        windowName = WinResConfig.Activity11DungeonWindow.name,
```

---

## Activty/baseact/Activity11MaterialWindow.lua.lua
**Functions:**
- Activity11MaterialWindow.ReInitData
- Activity11MaterialWindow.OnInit
- Activity11MaterialWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity11MaterialWindow.GetChapter
- Activity11MaterialWindow.GetMaxCount
- Activity11MaterialWindow.InitBtn
- Activity11MaterialWindow.CloseWindow
- Activity11MaterialWindow.OnShown
- Activity11MaterialWindow.OnClose
**Requires:**
- ActivityDungeon1011_MaterialWindowByName
**Snippet:**
```lua
require("ActivityDungeon1011_MaterialWindowByName")
local Activity11MaterialWindow = {}
local uis, contentPane, activityInfo, maxCount, posX

function Activity11MaterialWindow.ReInitData()
end

function Activity11MaterialWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity11MaterialWindow.package, WinResConfig.Activity11MaterialWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity11MiniGameChoiceWindow.lua.lua
**Functions:**
- list.itemRenderer
- Activity11MiniGameChoiceWindow.ReInitData
- Activity11MiniGameChoiceWindow.OnInit
- Activity11MiniGameChoiceWindow.UpdateInfo
- Activity11MiniGameChoiceWindow.InitBtn
- Activity11MiniGameChoiceWindow.OnClose
- Activity11MiniGameChoiceWindow.HandleMessage
**Requires:**
- ActivityDungeon1011_MiniGameChoiceWindowByName
**Snippet:**
```lua
require("ActivityDungeon1011_MiniGameChoiceWindowByName")
local Activity11MiniGameChoiceWindow = {}
local uis, contentPane, selectedLevelIndex
local gameId = 70441013
local LevelIsUnlock = function(levelIndex)
  local info = Activity11_MiniGameData.GetMiniGameInfo(gameId)
  local remoteMap = info.extraCount
  local latestLevel = remoteMap and remoteMap[1] or 0
  return levelIndex <= latestLevel + 1
end
```

---

## Activty/baseact/Activity11MiniGameExplainWindow.lua.lua
**Functions:**
- Activity11MiniGameExplainWindow.ReInitData
- Activity11MiniGameExplainWindow.OnInit
- Activity11MiniGameExplainWindow.UpdateInfo
- list.itemRenderer
- wlist.itemRenderer
- Activity11MiniGameExplainWindow.InitBtn
- Activity11MiniGameExplainWindow.OnClose
**Requires:**
- ActivityDungeon1011_MiniExplainWindowByName
**Snippet:**
```lua
require("ActivityDungeon1011_MiniExplainWindowByName")
local Activity11MiniGameExplainWindow = {}
local uis, contentPane

function Activity11MiniGameExplainWindow.ReInitData()
end

function Activity11MiniGameExplainWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity11MiniGameExplainWindow.package, WinResConfig.Activity11MiniGameExplainWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity11MiniGameMainWindow.lua.lua
**Functions:**
- Activity11MiniGameMainWindow.ReInitData
- Activity11MiniGameMainWindow.OnInit
- Activity11MiniGameMainWindow.UpdateInfo
- Activity11MiniGameMainWindow.InitBtn
- Activity11MiniGameMainWindow.OnClose
- Activity11MiniGameMainWindow.HandleMessage
**Requires:**
- ActivityDungeon1011_MiniGameWindowByName
**Snippet:**
```lua
require("ActivityDungeon1011_MiniGameWindowByName")
local Activity11MiniGameMainWindow = {}
local uis, contentPane
local gameId = 70441013
ld("Activity11_MiniGame")
local RefreshPanelInfo = function()
  local highestScoreTxt = T(20679)
  local dailyScoreTxt = T(20485)
  local info = Activity11_MiniGameData.GetMiniGameInfo(gameId)
  local conf = TableData.GetConfig(gameId, "BaseActivityStageGame")
```

---

## Activty/baseact/Activity11MiniGameSubmitWindow.lua.lua
**Functions:**
- Activity11MiniGameSubmitWindow.ReInitData
- Activity11MiniGameSubmitWindow.OnInit
- Activity11MiniGameSubmitWindow.UpdateInfo
- Activity11MiniGameSubmitWindow.InitBtn
- Activity11MiniGameSubmitWindow.OnClose
**Requires:**
- ActivityDungeon1011_MiniStart_EndRewardWindowByName
**Snippet:**
```lua
require("ActivityDungeon1011_MiniStart_EndRewardWindowByName")
local Activity11MiniGameSubmitWindow = {}
local uis, contentPane
local gameId = 70441013
local succeed, score, consumeSeconds, levelId, lastLevel
local LevelIsReachedUnlockTime = function(levelIndex)
  local levelConfigs = Activity11_MiniGameData.GetOrLoadLevelConfigs()
  local config = levelConfigs[levelIndex]
  local unlockDay = config and config.unlockDay or 0
  local info = ActivityDungeonData.GetActivityInfo()
```

---

## Activty/baseact/Activity11MiniGameTaskWindow.lua.lua
**Functions:**
- RefreshRewardList
- list.itemRenderer
- itemlist.itemRenderer
- Activity11MiniGameTaskWindow.ReInitData
- Activity11MiniGameTaskWindow.OnInit
- Activity11MiniGameTaskWindow.UpdateInfo
- Activity11MiniGameTaskWindow.InitBtn
- Activity11MiniGameTaskWindow.OnClose
**Requires:**
- ActivityDungeon1011_MiniTaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1011_MiniTaskWindowByName")
local Activity11MiniGameTaskWindow = {}
local uis, contentPane
local gameId = 70441013

local function RefreshRewardList()
  local info = Activity11_MiniGameData.GetMiniGameInfo(gameId)
  local minigame_tasks = info.taskList
  local list = uis.Main.TipsList
  list:SetVirtual()
```

---

## Activty/baseact/Activity11MiniGameWindow.lua.lua
**Functions:**
- Activity11MiniGameWindow.ReInitData
- Activity11MiniGameWindow.OnInit
- Activity11MiniGameWindow.UpdateInfo
- Activity11MiniGameWindow.InitBtn
- Activity11MiniGameWindow.OnClose
- Activity11MiniGameWindow.HandleMessage
**Requires:**
- ActivityDungeon1011_MiniGameStartWindowByName
- Activity11_MiniGameController
**Snippet:**
```lua
require("ActivityDungeon1011_MiniGameStartWindowByName")
local Activity11MiniGameWindow = {}
local uis, contentPane
local controller = require("Activity11_MiniGameController")
local levelIndex, itemObjLookup, busy, bombCount, fireworksCount, itemTextLookup, score, levelConfig
local ANGLE_DELTA_DEFAULT = 0
local ANGLE_DELTA_ACC = 800
local MAX_SHOT_ANGLE = 70
local Screen2WorldPosition = function(global)
  local cam = StageCamera.main
```

---

## Activty/baseact/Activity11PassportLevelUpTipsWindow.lua.lua
**Functions:**
- Activity11PassportLevelUpTipsWindow.ReInitData
- Activity11PassportLevelUpTipsWindow.OnInit
- Activity11PassportLevelUpTipsWindow.UpdateInfo
- Activity11PassportLevelUpTipsWindow.InitBtn
- Activity11PassportLevelUpTipsWindow.OnClose
**Requires:**
- ActivityDungeon1011_PassportUp_LevelUpTipsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1011_PassportUp_LevelUpTipsWindowByName")
local Activity11PassportLevelUpTipsWindow = {}
local uis, contentPane, lv

function Activity11PassportLevelUpTipsWindow.ReInitData()
end

function Activity11PassportLevelUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity11PassportLevelUpTipsWindow.package, WinResConfig.Activity11PassportLevelUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity11PassportWindow.lua.lua
**Functions:**
- Activity11PassportWindow.ReInitData
- Activity11PassportWindow.OnInit
- Activity11PassportWindow.UpdateTextDisplay
- Activity11PassportWindow.InitPassport
- uis.Main.TabRegion.TabList.itemRenderer
- Activity11PassportWindow.InitEffect
- Activity11PassportWindow.InitLv
- Activity11PassportWindow.ShowLevelUp
- Activity11PassportWindow.SaveLevel
- Activity11PassportWindow.GetRewardByLv
- Activity11PassportWindow.GetRewardNum
- Activity11PassportWindow.IsGetAllReward
- Activity11PassportWindow.ShowReward
- Activity11PassportWindow.GetUpdateLv
- Activity11PassportWindow.RefreshListReward
- Activity11PassportWindow.CheckItemTime
- Activity11PassportWindow.ShowQuitTips
- Activity11PassportWindow.RefreshUI
- Activity11PassportWindow.GetExpMxp
- Activity11PassportWindow.SetLevelInfo
- Activity11PassportWindow.InitList
- list.itemRenderer
- Activity11PassportWindow.SetListPos
- Activity11PassportWindow.RefreshReward
- Activity11PassportWindow.ShowGetEffect
- Activity11PassportWindow.RewardItemClick
- Activity11PassportWindow.IsReward
- Activity11PassportWindow.RefreshRewardFirst
- Activity11PassportWindow.RefreshRewardEnd
- Activity11PassportWindow.ShowState
- Activity11PassportWindow.RefreshRewardShow
- Activity11PassportWindow.RefreshRewardState
- Activity11PassportWindow.PassportActivate
- Activity11PassportWindow.CloseWindow
- Activity11PassportWindow.InitBtn
- Activity11PassportWindow.ShowExpBarAnim
- Activity11PassportWindow.InitTask
- list.itemRenderer
- Activity11PassportWindow.InitClothes
- clothes.BuyReward.RewardList.itemRenderer
- Activity11PassportWindow.SetLastLv
- Activity11PassportWindow.PlayFirstRewardEffect
- Activity11PassportWindow.PlayEndRewardEffect
- Activity11PassportWindow.HandleMessage
- Activity11PassportWindow.OnShown
- Activity11PassportWindow.OnClose
**Requires:**
- ActivityDungeon1011_PassportWindowByName
**Snippet:**
```lua
require("ActivityDungeon1011_PassportWindowByName")
local Activity11PassportWindow = {}
local uis, contentPane, passInfo, lvMax, modelType, expMax, rewardData, rewardType, rewardLv, listPage, passLv, jumpTb, isShowAllGet, passPortConfig, lvTween, lastLv, waitMessageId, newPassPort, animTween

function Activity11PassportWindow.ReInitData()
end

function Activity11PassportWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity11PassportWindow.package, WinResConfig.Activity11PassportWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity11PlotWindow.lua.lua
**Functions:**
- Activity11PlotWindow.ReInitData
- Activity11PlotWindow.OnInit
- Activity11PlotWindow.UpdateInfo
- list.itemRenderer
- Activity11PlotWindow.InitBtn
- Activity11PlotWindow.CloseWindow
- Activity11PlotWindow.OnClose
**Requires:**
- ActivityDungeon1011_PlotWindowByName
**Snippet:**
```lua
require("ActivityDungeon1011_PlotWindowByName")
local Activity11PlotWindow = {}
local uis, contentPane, configData

function Activity11PlotWindow.ReInitData()
end

function Activity11PlotWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity11PlotWindow.package, WinResConfig.Activity11PlotWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity11ShopWindow.lua.lua
**Functions:**
- Activity11ShopWindow.ReInitData
- Activity11ShopWindow.OnInit
- Activity11ShopWindow.UpdateInfo
- uis.Main.ItemList.itemRenderer
- Activity11ShopWindow.ShowItem
- list.itemRenderer
- Activity11ShopWindow.ShowOneReward
- list.itemRenderer
- Activity11ShopWindow.GetShopGrid
- Activity11ShopWindow.InitBtn
- Activity11ShopWindow.CloseWindow
- Activity11ShopWindow.OnClose
- Activity11ShopWindow.HandleMessage
**Requires:**
- ActivityDungeon1011_ShopWindowByName
**Snippet:**
```lua
require("ActivityDungeon1011_ShopWindowByName")
local Activity11ShopWindow = {}
local uis, contentPane, activityInfo, tempAssetsTips

function Activity11ShopWindow.ReInitData()
end

function Activity11ShopWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity11ShopWindow.package, WinResConfig.Activity11ShopWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity11SignWindow.lua.lua
**Functions:**
- Activity11SignWindow.ReInitData
- Activity11SignWindow.OnInit
- Activity11SignWindow.UpdateInfo
- list.RewardList.itemRenderer
- Activity11SignWindow.ShowAllItemFrame
- Activity11SignWindow.GetRewardData
- Activity11SignWindow.InitBtn
- Activity11SignWindow.CloseWindow
- Activity11SignWindow.OnClose
**Requires:**
- ActivityDungeon1011_SignWindowByName
**Snippet:**
```lua
require("ActivityDungeon1011_SignWindowByName")
local Activity11SignWindow = {}
local uis, contentPane, activityInfo

function Activity11SignWindow.ReInitData()
end

function Activity11SignWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity11SignWindow.package, WinResConfig.Activity11SignWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity11TaskWindow.lua.lua
**Functions:**
- Activity11TaskWindow.ReInitData
- Activity11TaskWindow.OnInit
- Activity11TaskWindow.UpdateInfo
- list.itemRenderer
- rewardList.itemRenderer
- Activity11TaskWindow.GetRewardNum
- Activity11TaskWindow.ShowAllItemFrame
- Activity11TaskWindow.SortTask
- Activity11TaskWindow.InitBtn
- Activity11TaskWindow.CloseWindow
- Activity11TaskWindow.OnClose
**Requires:**
- ActivityDungeon1011_TaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1011_TaskWindowByName")
local Activity11TaskWindow = {}
local uis, contentPane

function Activity11TaskWindow.ReInitData()
end

function Activity11TaskWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity11TaskWindow.package, WinResConfig.Activity11TaskWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity11_MiniGameController.lua.lua
**Functions:**
- FillPositions
- CollectNeighborSameBalls
- CollectNeighborSameEffectBalls
- RayCastEdges
- TweenTrack
**Snippet:**
```lua
ld("Physics")
local direction_differences = {
  [0] = {
    {-1, 0},
    {1, 0},
    {-1, -1},
    {0, -1},
    {-1, 1},
    {0, 1}
  },
```

---

## Activty/baseact/Activity11_MiniGameData.lua.lua
**Requires:**
- Activity11_MiniGameDeserializer
**Snippet:**
```lua
local utils = require("Activity11_MiniGameDeserializer")
local miniGameInfoDict, levelConfigs
local SetMiniGameInfo = function(info)
  miniGameInfoDict = miniGameInfoDict or {}
  miniGameInfoDict[info.gameId] = info
end
local GetMiniGameInfo = function(gameId)
  if miniGameInfoDict then
    return miniGameInfoDict[gameId]
  end
```

---

## Activty/baseact/Activity11_MiniGameDeserializer.lua.lua
**Snippet:**
```lua
local DeserializeLevelConfigs = function(path)
  local bytes = ResourceManager.LoadTextAssetBytes(path)
  local stream = CS.ReadWriteStream(bytes)
  local configs = {}
  for i = 1, stream:ReadInt32() do
    local levelId = stream:ReadInt32()
    local shootNum = stream:ReadInt32()
    local maxRow = stream:ReadInt32()
    local maxCol = stream:ReadInt32()
    local balls = {}
```

---

## Activty/baseact/Activity11_MiniGameScriptList.lua.lua
**Requires:**
- Activity11_MiniGameData
- Activity11_MiniGameService
**Snippet:**
```lua
Activity11_MiniGameData = require("Activity11_MiniGameData")
Activity11_MiniGameService = require("Activity11_MiniGameService")
```

---

## Activty/baseact/Activity11_MiniGameService.lua.lua
**Snippet:**
```lua
local gameId = 70441013
local MiniGameInfoReq = function(rspCallback)
  local info = ActivityDungeonData.GetActivityStageByShowId(11)
  local activityId = info.baseInfo.activityId
  Net.Send(Proto.MsgName.ActivityGetMiniGameReq, {activityId = activityId, gameId = gameId}, rspCallback)
end
local MiniGameInfoRsp = function(msg)
  Activity11_MiniGameData.SetMiniGameInfo(msg)
  UIMgr:SendWindowMessage(WinResConfig.Activity11MiniGameMainWindow.name, WindowMsgEnum.Activity11_MiniGame.REFRESH_MINIGAME_INFO)
  UIMgr:SendWindowMessage(WinResConfig.Activity11MiniGameWindow.name, WindowMsgEnum.Activity11_MiniGame.REFRESH_MINIGAME_INFO)
```

---

## Activty/baseact/Activity12BossBattleWindow.lua.lua
**Functions:**
- Activity12BossBattleWindow.ReInitData
- Activity12BossBattleWindow.OnInit
- Activity12BossBattleWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity12BossBattleWindow.FormatRemainTime
- Activity12BossBattleWindow.GetChapter
- Activity12BossBattleWindow.InitBtn
- Activity12BossBattleWindow.CloseWindow
- Activity12BossBattleWindow.OnClose
**Requires:**
- ActivityDungeon1012_BossBattleWindowByName
**Snippet:**
```lua
require("ActivityDungeon1012_BossBattleWindowByName")
local Activity12BossBattleWindow = {}
local uis, contentPane, activityInfo

function Activity12BossBattleWindow.ReInitData()
end

function Activity12BossBattleWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity12BossBattleWindow.package, WinResConfig.Activity12BossBattleWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity12BuyLevelDesWindow.lua.lua
**Functions:**
- Activity12BuyLevelDesWindow.ReInitData
- Activity12BuyLevelDesWindow.OnInit
- Activity12BuyLevelDesWindow.ShowAssetsTips
- Activity12BuyLevelDesWindow.UpdateTextDisplay
- Activity12BuyLevelDesWindow.Init
- Activity12BuyLevelDesWindow.GetGold
- Activity12BuyLevelDesWindow.ShowReward
- list.itemRenderer
- Activity12BuyLevelDesWindow.GetRewardItem
- Activity12BuyLevelDesWindow.GetLvData
- Activity12BuyLevelDesWindow.GetRewardLvData
- Activity12BuyLevelDesWindow.GetRewardByPhaseId
- Activity12BuyLevelDesWindow.BuyLevelRsp
- Activity12BuyLevelDesWindow.InitBtn
- waitFun
- Activity12BuyLevelDesWindow.HandleMessage
- Activity12BuyLevelDesWindow.OnShown
- Activity12BuyLevelDesWindow.OnClose
**Requires:**
- ActivityDungeon1012_BuyLevelDesWindowByName
**Snippet:**
```lua
require("ActivityDungeon1012_BuyLevelDesWindowByName")
local Activity12BuyLevelDesWindow = {}
local uis, contentPane, lvData, curLv, buyNum, itemId, lvMax, waitFun, rewardData, itemSort, transPlay, firstPlay, tatalGold, passInfo

function Activity12BuyLevelDesWindow.ReInitData()
end

function Activity12BuyLevelDesWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity12BuyLevelDesWindow.package, WinResConfig.Activity12BuyLevelDesWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity12ChallengeWindow.lua.lua
**Functions:**
- Activity12ChallengeWindow.ReInitData
- Activity12ChallengeWindow.OnInit
- Activity12ChallengeWindow.UpdateInfo
- uis.Main.ChapterList.itemRenderer
- Activity12ChallengeWindow.ShoweStage
- Activity12ChallengeWindow.StageItemClick
- Activity12ChallengeWindow.ShopInfo
- Activity12ChallengeWindow.GetChapterPassById
- Activity12ChallengeWindow.GetCurStage
- Activity12ChallengeWindow.GetFirstChapter
- Activity12ChallengeWindow.GetAllChapterId
- Activity12ChallengeWindow.InitBtn
- Activity12ChallengeWindow.CloseWindow
- Activity12ChallengeWindow.OnShown
- Activity12ChallengeWindow.OnClose
**Requires:**
- ActivityDungeon1012_ChallengeWindowByName
**Snippet:**
```lua
require("ActivityDungeon1012_ChallengeWindowByName")
local Activity12ChallengeWindow = {}
local uis, contentPane, activityInfo, scrollingTween

function Activity12ChallengeWindow.ReInitData()
end

function Activity12ChallengeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity12ChallengeWindow.package, WinResConfig.Activity12ChallengeWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity12DungeonWindow.lua.lua
**Functions:**
- Activity12DungeonWindow.ReInitData
- Activity12DungeonWindow.OnInit
- Activity12DungeonWindow.LoadBg
- Activity12DungeonWindow.InitRedDot
- Activity12DungeonWindow.UpdateInfo
- Activity12DungeonWindow.InitBtnTxt
- Activity12DungeonWindow.InitBtn
- Activity12DungeonWindow.OnShown
- Activity12DungeonWindow.OnClose
- Activity12DungeonWindow.HandleMessage
**Requires:**
- ActivityDungeon1012_ActivityDungeonWindowByName
**Snippet:**
```lua
require("ActivityDungeon1012_ActivityDungeonWindowByName")
local Activity12DungeonWindow = {}
local uis, contentPane, jumpTb, configData, activityInfo, effect
local InitMiniGameInfo = function()
  local data = ActivityDungeonData.GetActivityData()
  if data.id == 70440012 then
    ld("Activity12_MiniGame")
    Activity12_MiniGameService.MiniGameInfoReq(function()
      RedDotMgr.AddNode({
        windowName = WinResConfig.Activity12DungeonWindow.name,
```

---

## Activty/baseact/Activity12MaterialWindow.lua.lua
**Functions:**
- Activity12MaterialWindow.ReInitData
- Activity12MaterialWindow.OnInit
- Activity12MaterialWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity12MaterialWindow.GetChapter
- Activity12MaterialWindow.GetMaxCount
- Activity12MaterialWindow.InitBtn
- Activity12MaterialWindow.CloseWindow
- Activity12MaterialWindow.OnShown
- Activity12MaterialWindow.OnClose
**Requires:**
- ActivityDungeon1012_MaterialWindowByName
**Snippet:**
```lua
require("ActivityDungeon1012_MaterialWindowByName")
local Activity12MaterialWindow = {}
local uis, contentPane, activityInfo, maxCount, posX

function Activity12MaterialWindow.ReInitData()
end

function Activity12MaterialWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity12MaterialWindow.package, WinResConfig.Activity12MaterialWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity12MiniGameMainWindow.lua.lua
**Functions:**
- Activity12MiniGameMainWindow.ReInitData
- Activity12MiniGameMainWindow.OnInit
- Activity12MiniGameMainWindow.UpdateInfo
- Activity12MiniGameMainWindow.InitBtn
- Activity12MiniGameMainWindow.OnClose
- Activity12MiniGameMainWindow.HandleMessage
**Requires:**
- ActivityDungeon1012_MiniGameWindowByName
**Snippet:**
```lua
require("ActivityDungeon1012_MiniGameWindowByName")
local Activity12MiniGameMainWindow = {}
local uis, contentPane
local gameId = 70441014
ld("Activity12_MiniGame")
local RefreshPanelInfo = function()
  local highestScoreTxt = T(1921)
  local info = Activity12_MiniGameData.GetMiniGameInfo()
  local conf = TableData.GetConfig(gameId, "BaseActivityStageGame")
  local str = conf.game_day_reward[1]
```

---

## Activty/baseact/Activity12MiniGameRecordWindow.lua.lua
**Functions:**
- Activity12MiniGameRecordWindow.ReInitData
- Activity12MiniGameRecordWindow.OnInit
- Activity12MiniGameRecordWindow.UpdateInfo
- list.itemRenderer
- Activity12MiniGameRecordWindow.GetGameTime
- Activity12MiniGameRecordWindow.InitBtn
- Activity12MiniGameRecordWindow.OnClose
**Requires:**
- ActivityDungeon1012_MiniIntegralWindowByName
**Snippet:**
```lua
require("ActivityDungeon1012_MiniIntegralWindowByName")
local Activity12MiniGameRecordWindow = {}
local uis, contentPane

function Activity12MiniGameRecordWindow.ReInitData()
end

function Activity12MiniGameRecordWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity12MiniGameRecordWindow.package, WinResConfig.Activity12MiniGameRecordWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity12MiniGameSubmitWindow.lua.lua
**Functions:**
- Activity12MiniGameSubmitWindow.ReInitData
- Activity12MiniGameSubmitWindow.OnInit
- Activity12MiniGameSubmitWindow.UpdateInfo
- Activity12MiniGameSubmitWindow.GetGameTime
- Activity12MiniGameSubmitWindow.InitBtn
- Activity12MiniGameSubmitWindow.OnClose
**Requires:**
- ActivityDungeon1012_MiniStart_EndRewardWindowByName
**Snippet:**
```lua
require("ActivityDungeon1012_MiniStart_EndRewardWindowByName")
local Activity12MiniGameSubmitWindow = {}
local uis, contentPane, succeed, stageId, fail

function Activity12MiniGameSubmitWindow.ReInitData()
end

function Activity12MiniGameSubmitWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity12MiniGameSubmitWindow.package, WinResConfig.Activity12MiniGameSubmitWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity12MiniGameTaskWindow.lua.lua
**Functions:**
- RefreshRewardList
- list.itemRenderer
- itemlist.itemRenderer
- Activity12MiniGameTaskWindow.ReInitData
- Activity12MiniGameTaskWindow.OnInit
- Activity12MiniGameTaskWindow.UpdateInfo
- Activity12MiniGameTaskWindow.InitBtn
- Activity12MiniGameTaskWindow.OnClose
**Requires:**
- ActivityDungeon1012_MiniTaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1012_MiniTaskWindowByName")
local Activity12MiniGameTaskWindow = {}
local uis, contentPane
local gameId = 70441014

local function RefreshRewardList()
  local info = Activity12_MiniGameData.GetMiniGameInfo()
  local minigame_tasks = info.taskList
  local list = uis.Main.TipsList
  list:SetVirtual()
```

---

## Activty/baseact/Activity12MiniGameWindow.lua.lua
**Functions:**
- Activity12MiniGameWindow.ReInitData
- Activity12MiniGameWindow.OnInit
- Activity12MiniGameWindow.UpdateInfo
- Activity12MiniGameWindow.InitStripList
- uis.Main.ArrangeRegion.StripList.itemRenderer
- Activity12MiniGameWindow.PlayEffect
- Activity12MiniGameWindow.CheckEffect
- Activity12MiniGameWindow.InitBottleList
- uis.Main.ArrangeRegion.BottleList.itemRenderer
- Activity12MiniGameWindow.GetInfo
- Activity12MiniGameWindow.Random
- Activity12MiniGameWindow.CheckAdjacentMax
- Activity12MiniGameWindow.ShowStartTips
- Activity12MiniGameWindow.ShowGameOverTips
- Activity12MiniGameWindow.CheckEqual
- Activity12MiniGameWindow.CheckGameOver
- Activity12MiniGameWindow.InitBtn
- Activity12MiniGameWindow.GetCurDifficulty
- Activity12MiniGameWindow.Next
- Activity12MiniGameWindow.OnClose
- Activity12MiniGameWindow.HandleMessage
**Requires:**
- ActivityDungeon1012_MiniGameStartWindowByName
**Snippet:**
```lua
require("ActivityDungeon1012_MiniGameStartWindowByName")
local Activity12MiniGameWindow = {}
local uis, contentPane, curGameTime, selectCol, selectIndex, columnInfo, moveInfo, oneColumnCount, difficultyData

function Activity12MiniGameWindow.ReInitData()
end

function Activity12MiniGameWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity12MiniGameWindow.package, WinResConfig.Activity12MiniGameWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity12PassportLevelUpTipsWindow.lua.lua
**Functions:**
- Activity12PassportLevelUpTipsWindow.ReInitData
- Activity12PassportLevelUpTipsWindow.OnInit
- Activity12PassportLevelUpTipsWindow.UpdateInfo
- Activity12PassportLevelUpTipsWindow.InitBtn
- Activity12PassportLevelUpTipsWindow.OnClose
**Requires:**
- ActivityDungeon1012_PassportUp_LevelUpTipsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1012_PassportUp_LevelUpTipsWindowByName")
local Activity12PassportLevelUpTipsWindow = {}
local uis, contentPane, lv

function Activity12PassportLevelUpTipsWindow.ReInitData()
end

function Activity12PassportLevelUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity12PassportLevelUpTipsWindow.package, WinResConfig.Activity12PassportLevelUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity12PassportWindow.lua.lua
**Functions:**
- Activity12PassportWindow.ReInitData
- Activity12PassportWindow.OnInit
- Activity12PassportWindow.UpdateTextDisplay
- Activity12PassportWindow.InitPassport
- uis.Main.TabRegion.TabList.itemRenderer
- Activity12PassportWindow.InitEffect
- Activity12PassportWindow.InitLv
- Activity12PassportWindow.ShowLevelUp
- Activity12PassportWindow.SaveLevel
- Activity12PassportWindow.GetRewardByLv
- Activity12PassportWindow.GetRewardNum
- Activity12PassportWindow.IsGetAllReward
- Activity12PassportWindow.ShowReward
- Activity12PassportWindow.GetUpdateLv
- Activity12PassportWindow.RefreshListReward
- Activity12PassportWindow.CheckItemTime
- Activity12PassportWindow.ShowQuitTips
- Activity12PassportWindow.RefreshUI
- Activity12PassportWindow.GetExpMxp
- Activity12PassportWindow.SetLevelInfo
- Activity12PassportWindow.InitList
- list.itemRenderer
- Activity12PassportWindow.SetListPos
- Activity12PassportWindow.RefreshReward
- Activity12PassportWindow.ShowGetEffect
- Activity12PassportWindow.RewardItemClick
- Activity12PassportWindow.IsReward
- Activity12PassportWindow.RefreshRewardFirst
- Activity12PassportWindow.RefreshRewardEnd
- Activity12PassportWindow.ShowState
- Activity12PassportWindow.RefreshRewardShow
- Activity12PassportWindow.RefreshRewardState
- Activity12PassportWindow.PassportActivate
- Activity12PassportWindow.CloseWindow
- Activity12PassportWindow.InitBtn
- Activity12PassportWindow.ShowExpBarAnim
- Activity12PassportWindow.InitTask
- list.itemRenderer
- Activity12PassportWindow.InitClothes
- clothes.BuyReward.RewardList.itemRenderer
- Activity12PassportWindow.SetLastLv
- Activity12PassportWindow.PlayFirstRewardEffect
- Activity12PassportWindow.PlayEndRewardEffect
- Activity12PassportWindow.HandleMessage
- Activity12PassportWindow.OnShown
- Activity12PassportWindow.OnClose
**Requires:**
- ActivityDungeon1012_PassportWindowByName
**Snippet:**
```lua
require("ActivityDungeon1012_PassportWindowByName")
local Activity12PassportWindow = {}
local uis, contentPane, passInfo, lvMax, modelType, expMax, rewardData, rewardType, rewardLv, listPage, passLv, jumpTb, isShowAllGet, passPortConfig, lvTween, lastLv, waitMessageId, newPassPort, animTween

function Activity12PassportWindow.ReInitData()
end

function Activity12PassportWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity12PassportWindow.package, WinResConfig.Activity12PassportWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity12PlotWindow.lua.lua
**Functions:**
- Activity12PlotWindow.ReInitData
- Activity12PlotWindow.OnInit
- Activity12PlotWindow.UpdateInfo
- list.itemRenderer
- Activity12PlotWindow.InitBtn
- Activity12PlotWindow.CloseWindow
- Activity12PlotWindow.OnClose
**Requires:**
- ActivityDungeon1012_PlotWindowByName
**Snippet:**
```lua
require("ActivityDungeon1012_PlotWindowByName")
local Activity12PlotWindow = {}
local uis, contentPane, configData

function Activity12PlotWindow.ReInitData()
end

function Activity12PlotWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity12PlotWindow.package, WinResConfig.Activity12PlotWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity12ShopWindow.lua.lua
**Functions:**
- Activity12ShopWindow.ReInitData
- Activity12ShopWindow.OnInit
- Activity12ShopWindow.UpdateInfo
- uis.Main.ItemList.itemRenderer
- Activity12ShopWindow.ShowItem
- list.itemRenderer
- Activity12ShopWindow.ShowOneReward
- list.itemRenderer
- Activity12ShopWindow.GetShopGrid
- Activity12ShopWindow.InitBtn
- Activity12ShopWindow.CloseWindow
- Activity12ShopWindow.OnClose
- Activity12ShopWindow.HandleMessage
**Requires:**
- ActivityDungeon1012_ShopWindowByName
**Snippet:**
```lua
require("ActivityDungeon1012_ShopWindowByName")
local Activity12ShopWindow = {}
local uis, contentPane, activityInfo, tempAssetsTips

function Activity12ShopWindow.ReInitData()
end

function Activity12ShopWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity12ShopWindow.package, WinResConfig.Activity12ShopWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity12SignWindow.lua.lua
**Functions:**
- Activity12SignWindow.ReInitData
- Activity12SignWindow.OnInit
- Activity12SignWindow.UpdateInfo
- list.RewardList.itemRenderer
- Activity12SignWindow.ShowAllItemFrame
- Activity12SignWindow.GetRewardData
- Activity12SignWindow.InitBtn
- Activity12SignWindow.CloseWindow
- Activity12SignWindow.OnClose
**Requires:**
- ActivityDungeon1012_SignWindowByName
**Snippet:**
```lua
require("ActivityDungeon1012_SignWindowByName")
local Activity12SignWindow = {}
local uis, contentPane, activityInfo

function Activity12SignWindow.ReInitData()
end

function Activity12SignWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity12SignWindow.package, WinResConfig.Activity12SignWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity12TaskWindow.lua.lua
**Functions:**
- Activity12TaskWindow.ReInitData
- Activity12TaskWindow.OnInit
- Activity12TaskWindow.UpdateInfo
- list.itemRenderer
- rewardList.itemRenderer
- Activity12TaskWindow.GetRewardNum
- Activity12TaskWindow.ShowAllItemFrame
- Activity12TaskWindow.SortTask
- Activity12TaskWindow.InitBtn
- Activity12TaskWindow.CloseWindow
- Activity12TaskWindow.OnClose
**Requires:**
- ActivityDungeon1012_TaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1012_TaskWindowByName")
local Activity12TaskWindow = {}
local uis, contentPane

function Activity12TaskWindow.ReInitData()
end

function Activity12TaskWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity12TaskWindow.package, WinResConfig.Activity12TaskWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity12_MiniGameData.lua.lua
**Functions:**
- Activity12_MiniGameData.SetMiniGameInfo
- Activity12_MiniGameData.GetMiniGameInfo
**Snippet:**
```lua
Activity12_MiniGameData = {gameId = 70441014}
local miniGameInfo

function Activity12_MiniGameData.SetMiniGameInfo(info)
  miniGameInfo = info
end

function Activity12_MiniGameData.GetMiniGameInfo()
  return miniGameInfo
end
```

---

## Activty/baseact/Activity12_MiniGameScriptList.lua.lua
**Requires:**
- Activity12_MiniGameData
- Activity12_MiniGameService
**Snippet:**
```lua
require("Activity12_MiniGameData")
require("Activity12_MiniGameService")
```

---

## Activty/baseact/Activity12_MiniGameService.lua.lua
**Functions:**
- Activity12_MiniGameService.MiniGameInfoReq
- Activity12_MiniGameService.MiniGameInfoRsp
- Activity12_MiniGameService.MiniGameSubmitReq
- Activity12_MiniGameService.MiniGameSubmitRsp
- Activity12_MiniGameService.MiniGameGetDailyRewardReq
- Activity12_MiniGameService.MiniGameGetDailyRewardRsp
- Activity12_MiniGameService.Init
**Snippet:**
```lua
Activity12_MiniGameService = {}
local gameId = Activity12_MiniGameData.gameId

function Activity12_MiniGameService.MiniGameInfoReq(rspCallback)
  local info = ActivityDungeonData.GetActivityInfo()
  local activityId = info.baseInfo.activityId
  Net.Send(Proto.MsgName.ActivityGetMiniGameReq, {gameId = gameId, activityId = activityId}, rspCallback)
end

function Activity12_MiniGameService.MiniGameInfoRsp(msg)
```

---

## Activty/baseact/Activity13BossBattleWindow.lua.lua
**Functions:**
- Activity13BossBattleWindow.ReInitData
- Activity13BossBattleWindow.OnInit
- Activity13BossBattleWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity13BossBattleWindow.FormatRemainTime
- Activity13BossBattleWindow.GetChapter
- Activity13BossBattleWindow.InitBtn
- Activity13BossBattleWindow.CloseWindow
- Activity13BossBattleWindow.OnClose
**Requires:**
- ActivityDungeon1013_BossBattleWindowByName
**Snippet:**
```lua
require("ActivityDungeon1013_BossBattleWindowByName")
local Activity13BossBattleWindow = {}
local uis, contentPane, activityInfo

function Activity13BossBattleWindow.ReInitData()
end

function Activity13BossBattleWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity13BossBattleWindow.package, WinResConfig.Activity13BossBattleWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity13BounceMiniGameMainWindow.lua.lua
**Functions:**
- Activity13BounceMiniGameMainWindow.ReInitData
- Activity13BounceMiniGameMainWindow.OnInit
- Activity13BounceMiniGameMainWindow.UpdateInfo
- Activity13BounceMiniGameMainWindow.InitBtn
- Activity13BounceMiniGameMainWindow.OnClose
- Activity13BounceMiniGameMainWindow.HandleMessage
**Requires:**
- ActivityDungeon1013_MiniGameWindowByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniGameWindowByName")
local Activity13BounceMiniGameMainWindow = {}
local uis, contentPane
ld("Activity13_MiniGame")
local gameId = 70441016
local RefreshPanelInfo = function()
  local info = Activity13_MiniGameData.GetMiniGameInfo(gameId)
  local conf = TableData.GetConfig(gameId, "BaseActivityStageGame")
  local str = conf.game_day_reward[1]
  local splits = Split(str, ":")
```

---

## Activty/baseact/Activity13BounceMiniGameRankWindow.lua.lua
**Functions:**
- Activity13BounceMiniGameRankWindow.ReInitData
- Activity13BounceMiniGameRankWindow.OnInit
- Activity13BounceMiniGameRankWindow.UpdateInfo
- list.itemRenderer
- Activity13BounceMiniGameRankWindow.InitBtn
- Activity13BounceMiniGameRankWindow.OnClose
**Requires:**
- ActivityDungeon1013_MiniRankWindowByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniRankWindowByName")
local Activity13BounceMiniGameRankWindow = {}
local uis, contentPane

function Activity13BounceMiniGameRankWindow.ReInitData()
end

function Activity13BounceMiniGameRankWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity13BounceMiniGameRankWindow.package, WinResConfig.Activity13BounceMiniGameRankWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity13BounceMiniGameSubmitWindow.lua.lua
**Functions:**
- Activity13BounceMiniGameSubmitWindow.ReInitData
- Activity13BounceMiniGameSubmitWindow.OnInit
- Activity13BounceMiniGameSubmitWindow.UpdateInfo
- Activity13BounceMiniGameSubmitWindow.InitBtn
- Activity13BounceMiniGameSubmitWindow.OnClose
**Requires:**
- ActivityDungeon1013_MiniStart_EndRewardWindowByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniStart_EndRewardWindowByName")
local Activity13BounceMiniGameSubmitWindow = {}
local uis, contentPane, score, succeed

function Activity13BounceMiniGameSubmitWindow.ReInitData()
end

function Activity13BounceMiniGameSubmitWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity13BounceMiniGameSubmitWindow.package, WinResConfig.Activity13BounceMiniGameSubmitWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity13BounceMiniGameTaskWindow.lua.lua
**Functions:**
- RefreshRewardList
- list.itemRenderer
- itemlist.itemRenderer
- Activity13BounceMiniGameTaskWindow.ReInitData
- Activity13BounceMiniGameTaskWindow.OnInit
- Activity13BounceMiniGameTaskWindow.UpdateInfo
- Activity13BounceMiniGameTaskWindow.InitBtn
- Activity13BounceMiniGameTaskWindow.OnClose
**Requires:**
- ActivityDungeon1013_MiniTaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniTaskWindowByName")
local Activity13BounceMiniGameTaskWindow = {}
local uis, contentPane
local gameId = 70441016

local function RefreshRewardList()
  local info = Activity13_MiniGameData.GetMiniGameInfo(gameId)
  local minigame_tasks = info.taskList
  local list = uis.Main.TipsList
  list:SetVirtual()
```

---

## Activty/baseact/Activity13BounceMiniGameTipsWindow.lua.lua
**Functions:**
- Activity13BounceMiniGameTipsWindow.ReInitData
- Activity13BounceMiniGameTipsWindow.OnInit
- Activity13BounceMiniGameTipsWindow.UpdateInfo
- Activity13BounceMiniGameTipsWindow.InitBtn
- Activity13BounceMiniGameTipsWindow.OnClose
**Requires:**
- ActivityDungeon1013_MiniTipsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniTipsWindowByName")
local Activity13BounceMiniGameTipsWindow = {}
local uis, contentPane
local AUTO_CLOSE_AFTER = 1
local delayTween

function Activity13BounceMiniGameTipsWindow.ReInitData()
end

function Activity13BounceMiniGameTipsWindow.OnInit(bridgeObj)
```

---

## Activty/baseact/Activity13BounceMiniGameWindow.lua.lua
**Functions:**
- Activity13BounceMiniGameWindow.ReInitData
- Activity13BounceMiniGameWindow.OnInit
- Activity13BounceMiniGameWindow.UpdateInfo
- Activity13BounceMiniGameWindow.InitBtn
- Activity13BounceMiniGameWindow.OnClose
- Activity13BounceMiniGameWindow.HandleMessage
**Requires:**
- ActivityDungeon1013_MiniGameStartWindowByName
- Activity13_BounceBallController
**Snippet:**
```lua
require("ActivityDungeon1013_MiniGameStartWindowByName")
local Activity13BounceMiniGameWindow = {}
local uis, contentPane
local gameId = 70441016
local MAX_SHOT_ANGLE = 70
local ANGLE_DELTA_DEFAULT = 0
local ANGLE_DELTA_ACC = 800
local TWINKLE_DURATION = 0.04
local controller = require("Activity13_BounceBallController")
local itemObjLookup, busy, touching, shootDirection, angleDelta, buttonDirection, buttonMode, dotline, points
```

---

## Activty/baseact/Activity13BuyLevelDesWindow.lua.lua
**Functions:**
- Activity13BuyLevelDesWindow.ReInitData
- Activity13BuyLevelDesWindow.OnInit
- Activity13BuyLevelDesWindow.ShowAssetsTips
- Activity13BuyLevelDesWindow.UpdateTextDisplay
- Activity13BuyLevelDesWindow.Init
- Activity13BuyLevelDesWindow.GetGold
- Activity13BuyLevelDesWindow.ShowReward
- list.itemRenderer
- Activity13BuyLevelDesWindow.GetRewardItem
- Activity13BuyLevelDesWindow.GetLvData
- Activity13BuyLevelDesWindow.GetRewardLvData
- Activity13BuyLevelDesWindow.GetRewardByPhaseId
- Activity13BuyLevelDesWindow.BuyLevelRsp
- Activity13BuyLevelDesWindow.InitBtn
- waitFun
- Activity13BuyLevelDesWindow.HandleMessage
- Activity13BuyLevelDesWindow.OnShown
- Activity13BuyLevelDesWindow.OnClose
**Requires:**
- ActivityDungeon1013_BuyLevelDesWindowByName
**Snippet:**
```lua
require("ActivityDungeon1013_BuyLevelDesWindowByName")
local Activity13BuyLevelDesWindow = {}
local uis, contentPane, lvData, curLv, buyNum, itemId, lvMax, waitFun, rewardData, itemSort, transPlay, firstPlay, tatalGold, passInfo

function Activity13BuyLevelDesWindow.ReInitData()
end

function Activity13BuyLevelDesWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity13BuyLevelDesWindow.package, WinResConfig.Activity13BuyLevelDesWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity13CarGameExplainWindow.lua.lua
**Functions:**
- Activity13CarGameExplainWindow.ReInitData
- Activity13CarGameExplainWindow.OnInit
- Activity13CarGameExplainWindow.UpdateInfo
- Activity13CarGameExplainWindow.ShowListWord
- root.WordList.itemRenderer
- Activity13CarGameExplainWindow.InitBtn
- Activity13CarGameExplainWindow.OnClose
**Requires:**
- ActivityDungeon1013_MiniExplain2WindowByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniExplain2WindowByName")
local Activity13CarGameExplainWindow = {}
local uis, contentPane, closeCallback

function Activity13CarGameExplainWindow.ReInitData()
end

function Activity13CarGameExplainWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity13CarGameExplainWindow.package, WinResConfig.Activity13CarGameExplainWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity13CarGameMainWindow.lua.lua
**Functions:**
- Activity13CarGameMainWindow.ReInitData
- Activity13CarGameMainWindow.OnInit
- Activity13CarGameMainWindow.UpdateInfo
- Activity13CarGameMainWindow.InitBtn
- Activity13CarGameMainWindow.OnClose
- Activity13CarGameMainWindow.HandleMessage
**Requires:**
- ActivityDungeon1013_MiniGame2WindowByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniGame2WindowByName")
local Activity13CarGameMainWindow = {}
local uis, contentPane
local RefreshPanelInfo = function()
  local gameId = 70441017
  local info = Activity13_MiniGameData.GetMiniGameInfo(gameId)
  local conf = TableData.GetConfig(gameId, "BaseActivityStageGame")
  local str = conf.game_day_reward[1]
  local splits = Split(str, ":")
  local itemType, itemId, count = tonumber(splits[1]), tonumber(splits[2]), tonumber(splits[3])
```

---

## Activty/baseact/Activity13CarGameSubmitWindow.lua.lua
**Functions:**
- Activity13CarGameSubmitWindow.ReInitData
- Activity13CarGameSubmitWindow.OnInit
- Activity13CarGameSubmitWindow.UpdateInfo
- Activity13CarGameSubmitWindow.InitBtn
- Activity13CarGameSubmitWindow.OnClose
**Requires:**
- ActivityDungeon1013_MiniStart2_EndRewardWindowByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniStart2_EndRewardWindowByName")
local Activity13CarGameSubmitWindow = {}
local uis, contentPane, nowIntegral, stageId

function Activity13CarGameSubmitWindow.ReInitData()
end

function Activity13CarGameSubmitWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity13CarGameSubmitWindow.package, WinResConfig.Activity13CarGameSubmitWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity13CarGameTaskWindow.lua.lua
**Functions:**
- RefreshRewardList
- list.itemRenderer
- itemlist.itemRenderer
- Activity13CarGameTaskWindow.ReInitData
- Activity13CarGameTaskWindow.OnInit
- Activity13CarGameTaskWindow.UpdateInfo
- Activity13CarGameTaskWindow.InitBtn
- Activity13CarGameTaskWindow.OnClose
**Requires:**
- ActivityDungeon1013_MiniTask2WindowByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniTask2WindowByName")
local Activity13CarGameTaskWindow = {}
local uis, contentPane

local function RefreshRewardList()
  local gameId = 70441017
  local info = Activity13_MiniGameData.GetMiniGameInfo(gameId)
  local minigame_tasks = info.taskList
  local list = uis.Main.TipsList
  list:SetVirtual()
```

---

## Activty/baseact/Activity13CarGameWindow.lua.lua
**Functions:**
- Activity13CarGameWindow.ReInitData
- Activity13CarGameWindow.OnInit
- Activity13CarGameWindow.UpdateInfo
- Activity13CarGameWindow.InitMap
- Activity13CarGameWindow.CheckPass
- Activity13CarGameWindow.ClearMapById
- Activity13CarGameWindow.GetLimitPos
- Activity13CarGameWindow.CreateItem
- Activity13CarGameWindow.GetResName
- Activity13CarGameWindow.SetGridMap
- Activity13CarGameWindow.InitStageData
- Activity13CarGameWindow.UpdateCount
- Activity13CarGameWindow.OnNext
- Activity13CarGameWindow.GetCurDifficulty
- Activity13CarGameWindow.InitBtn
- Activity13CarGameWindow.OnClose
- Activity13CarGameWindow.HandleMessage
**Requires:**
- ActivityDungeon1013_MiniGameStart2WindowByName
**Snippet:**
```lua
require("ActivityDungeon1013_MiniGameStart2WindowByName")
local Activity13CarGameWindow = {}
local uis, contentPane
local width, height = 106, 106
local targetUrl = "MiniStart2_Move00"
local twoUrl = {
  "MiniStart2_Move01",
  "MiniStart2_Move02",
  "MiniStart2_Move03",
  "MiniStart2_Move04",
```

---

## Activty/baseact/Activity13ChallengeWindow.lua.lua
**Functions:**
- Activity13ChallengeWindow.ReInitData
- Activity13ChallengeWindow.OnInit
- Activity13ChallengeWindow.UpdateInfo
- uis.Main.ChapterList.itemRenderer
- Activity13ChallengeWindow.ShoweStage
- Activity13ChallengeWindow.StageItemClick
- Activity13ChallengeWindow.ShopInfo
- Activity13ChallengeWindow.GetChapterPassById
- Activity13ChallengeWindow.GetCurStage
- Activity13ChallengeWindow.GetFirstChapter
- Activity13ChallengeWindow.GetAllChapterId
- Activity13ChallengeWindow.InitBtn
- Activity13ChallengeWindow.CloseWindow
- Activity13ChallengeWindow.OnShown
- Activity13ChallengeWindow.OnClose
**Requires:**
- ActivityDungeon1013_ChallengeWindowByName
**Snippet:**
```lua
require("ActivityDungeon1013_ChallengeWindowByName")
local Activity13ChallengeWindow = {}
local uis, contentPane, activityInfo, scrollingTween

function Activity13ChallengeWindow.ReInitData()
end

function Activity13ChallengeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity13ChallengeWindow.package, WinResConfig.Activity13ChallengeWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity13DungeonWindow.lua.lua
**Functions:**
- Activity13DungeonWindow.ReInitData
- Activity13DungeonWindow.OnInit
- Activity13DungeonWindow.InitRedDot
- Activity13DungeonWindow.LoadBg
- Activity13DungeonWindow.UpdateInfo
- Activity13DungeonWindow.InitBtnText
- Activity13DungeonWindow.InitBtn
- Activity13DungeonWindow.OnShown
- Activity13DungeonWindow.OnHide
- Activity13DungeonWindow.OnClose
- Activity13DungeonWindow.HandleMessage
**Requires:**
- ActivityDungeon1013_ActivityDungeonWindowByName
**Snippet:**
```lua
require("ActivityDungeon1013_ActivityDungeonWindowByName")
local Activity13DungeonWindow = {}
local uis, contentPane, jumpTb, configData, activityInfo, effect, eventTipsRoot, cursors, cursorRoot, soundSource, soundEvt3D
local OnPopupEventTips = function(events)
  local parent = uis.Main.root
  if not eventTipsRoot then
    eventTipsRoot = UIMgr:CreateObject("ActivityDungeon1013", "EventTipsList")
    eventTipsRoot.opaque = false
    local childIndex = parent:GetChildIndex(uis.Main.BackGround.root)
    parent:AddChildAt(eventTipsRoot, childIndex + 1)
```

---

## Activty/baseact/Activity13EntranceAnimWindow.lua.lua
**Functions:**
- FindChild
- PlayDailyEntranceAnim
- Activity13EntranceAnimWindow.ReInitData
- Activity13EntranceAnimWindow.OnInit
- Activity13EntranceAnimWindow.UpdateInfo
- Activity13EntranceAnimWindow.InitBtn
- Activity13EntranceAnimWindow.OnClose
**Requires:**
- ActivityDungeon1013_MainCoverWindowByName
**Snippet:**
```lua
require("ActivityDungeon1013_MainCoverWindowByName")
local Activity13EntranceAnimWindow = {}
local uis, contentPane, touchable
local setSpritesColor = function(go, color, fadeout)
  local spriteRenderers = go:GetComponentsInChildren(typeof(CS.UnityEngine.SpriteRenderer))
  if spriteRenderers then
    for i = 0, spriteRenderers.Length - 1 do
      local sr = spriteRenderers[i]
      if fadeout then
        color.a = math.min(color.a, sr.color.a)
```

---

## Activty/baseact/Activity13MaterialWindow.lua.lua
**Functions:**
- Activity13MaterialWindow.ReInitData
- Activity13MaterialWindow.OnInit
- Activity13MaterialWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity13MaterialWindow.GetChapter
- Activity13MaterialWindow.GetMaxCount
- Activity13MaterialWindow.InitBtn
- Activity13MaterialWindow.CloseWindow
- Activity13MaterialWindow.OnShown
- Activity13MaterialWindow.OnClose
**Requires:**
- ActivityDungeon1013_MaterialWindowByName
**Snippet:**
```lua
require("ActivityDungeon1013_MaterialWindowByName")
local Activity13MaterialWindow = {}
local uis, contentPane, activityInfo, maxCount, posX

function Activity13MaterialWindow.ReInitData()
end

function Activity13MaterialWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity13MaterialWindow.package, WinResConfig.Activity13MaterialWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity13PassportLevelUpTipsWindow.lua.lua
**Functions:**
- Activity13PassportLevelUpTipsWindow.ReInitData
- Activity13PassportLevelUpTipsWindow.OnInit
- Activity13PassportLevelUpTipsWindow.UpdateInfo
- Activity13PassportLevelUpTipsWindow.InitBtn
- Activity13PassportLevelUpTipsWindow.OnClose
**Requires:**
- ActivityDungeon1013_PassportUp_LevelUpTipsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1013_PassportUp_LevelUpTipsWindowByName")
local Activity13PassportLevelUpTipsWindow = {}
local uis, contentPane, lv

function Activity13PassportLevelUpTipsWindow.ReInitData()
end

function Activity13PassportLevelUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity13PassportLevelUpTipsWindow.package, WinResConfig.Activity13PassportLevelUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity13PassportWindow.lua.lua
**Functions:**
- Activity13PassportWindow.ReInitData
- Activity13PassportWindow.OnInit
- Activity13PassportWindow.UpdateTextDisplay
- Activity13PassportWindow.InitPassport
- uis.Main.TabRegion.TabList.itemRenderer
- Activity13PassportWindow.InitEffect
- Activity13PassportWindow.InitLv
- Activity13PassportWindow.ShowLevelUp
- Activity13PassportWindow.SaveLevel
- Activity13PassportWindow.GetRewardByLv
- Activity13PassportWindow.GetRewardNum
- Activity13PassportWindow.IsGetAllReward
- Activity13PassportWindow.ShowReward
- Activity13PassportWindow.GetUpdateLv
- Activity13PassportWindow.RefreshListReward
- Activity13PassportWindow.CheckItemTime
- Activity13PassportWindow.ShowQuitTips
- Activity13PassportWindow.RefreshUI
- Activity13PassportWindow.GetExpMxp
- Activity13PassportWindow.SetLevelInfo
- Activity13PassportWindow.InitList
- list.itemRenderer
- Activity13PassportWindow.SetListPos
- Activity13PassportWindow.RefreshReward
- Activity13PassportWindow.ShowGetEffect
- Activity13PassportWindow.RewardItemClick
- Activity13PassportWindow.IsReward
- Activity13PassportWindow.RefreshRewardFirst
- Activity13PassportWindow.RefreshRewardEnd
- Activity13PassportWindow.ShowState
- Activity13PassportWindow.RefreshRewardShow
- Activity13PassportWindow.RefreshRewardState
- Activity13PassportWindow.PassportActivate
- Activity13PassportWindow.CloseWindow
- Activity13PassportWindow.InitBtn
- Activity13PassportWindow.ShowExpBarAnim
- Activity13PassportWindow.InitTask
- list.itemRenderer
- Activity13PassportWindow.InitClothes
- clothes.BuyReward.RewardList.itemRenderer
- Activity13PassportWindow.SetLastLv
- Activity13PassportWindow.PlayFirstRewardEffect
- Activity13PassportWindow.PlayEndRewardEffect
- Activity13PassportWindow.HandleMessage
- Activity13PassportWindow.OnShown
- Activity13PassportWindow.OnClose
**Requires:**
- ActivityDungeon1013_PassportWindowByName
**Snippet:**
```lua
require("ActivityDungeon1013_PassportWindowByName")
local Activity13PassportWindow = {}
local uis, contentPane, passInfo, lvMax, modelType, expMax, rewardData, rewardType, rewardLv, listPage, passLv, jumpTb, isShowAllGet, passPortConfig, lvTween, lastLv, waitMessageId, newPassPort, animTween

function Activity13PassportWindow.ReInitData()
end

function Activity13PassportWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity13PassportWindow.package, WinResConfig.Activity13PassportWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity13PlotWindow.lua.lua
**Functions:**
- Activity13PlotWindow.ReInitData
- Activity13PlotWindow.OnInit
- Activity13PlotWindow.UpdateInfo
- list.itemRenderer
- Activity13PlotWindow.InitBtn
- Activity13PlotWindow.CloseWindow
- Activity13PlotWindow.OnClose
**Requires:**
- ActivityDungeon1013_PlotWindowByName
**Snippet:**
```lua
require("ActivityDungeon1013_PlotWindowByName")
local Activity13PlotWindow = {}
local uis, contentPane, configData

function Activity13PlotWindow.ReInitData()
end

function Activity13PlotWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity13PlotWindow.package, WinResConfig.Activity13PlotWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity13ShopWindow.lua.lua
**Functions:**
- Activity13ShopWindow.ReInitData
- Activity13ShopWindow.OnInit
- Activity13ShopWindow.UpdateInfo
- uis.Main.ItemList.itemRenderer
- Activity13ShopWindow.ShowItem
- list.itemRenderer
- Activity13ShopWindow.ShowOneReward
- list.itemRenderer
- Activity13ShopWindow.GetShopGrid
- Activity13ShopWindow.InitBtn
- Activity13ShopWindow.CloseWindow
- Activity13ShopWindow.OnClose
- Activity13ShopWindow.HandleMessage
**Requires:**
- ActivityDungeon1013_ShopWindowByName
**Snippet:**
```lua
require("ActivityDungeon1013_ShopWindowByName")
local Activity13ShopWindow = {}
local uis, contentPane, activityInfo, tempAssetsTips

function Activity13ShopWindow.ReInitData()
end

function Activity13ShopWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity13ShopWindow.package, WinResConfig.Activity13ShopWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity13SignWindow.lua.lua
**Functions:**
- Activity13SignWindow.ReInitData
- Activity13SignWindow.OnInit
- Activity13SignWindow.UpdateInfo
- list.RewardList.itemRenderer
- Activity13SignWindow.ShowAllItemFrame
- Activity13SignWindow.GetRewardData
- Activity13SignWindow.InitBtn
- Activity13SignWindow.CloseWindow
- Activity13SignWindow.OnClose
**Requires:**
- ActivityDungeon1013_SignWindowByName
**Snippet:**
```lua
require("ActivityDungeon1013_SignWindowByName")
local Activity13SignWindow = {}
local uis, contentPane, activityInfo

function Activity13SignWindow.ReInitData()
end

function Activity13SignWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity13SignWindow.package, WinResConfig.Activity13SignWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity13TaskWindow.lua.lua
**Functions:**
- Activity13TaskWindow.ReInitData
- Activity13TaskWindow.OnInit
- Activity13TaskWindow.UpdateInfo
- list.itemRenderer
- rewardList.itemRenderer
- Activity13TaskWindow.GetRewardNum
- Activity13TaskWindow.ShowAllItemFrame
- Activity13TaskWindow.SortTask
- Activity13TaskWindow.InitBtn
- Activity13TaskWindow.CloseWindow
- Activity13TaskWindow.OnClose
**Requires:**
- ActivityDungeon1013_TaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1013_TaskWindowByName")
local Activity13TaskWindow = {}
local uis, contentPane

function Activity13TaskWindow.ReInitData()
end

function Activity13TaskWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity13TaskWindow.package, WinResConfig.Activity13TaskWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity13_BounceBallConfigs.lua.lua
**Snippet:**
```lua
return "[{'type':1,'vertices':[{'y':0.04,'x':0.41},{'y':0.149999991,'x':0.34},{'y':0.25,'x':0.26},{'y':0.32,'x':0.26},{'y':0.35,'x':0.24},{'y':0.329999983,'x':0.07},{'y':0.29,'x':-0.07},{'y':0.359999985,'x':-0.149999991},{'y':0.359999985,'x':-0.21},{'y':0.35,'x':-0.229999989},{'y':0.26,'x':-0.25},{'y':0.19,'x':-0.229999989},{'y':0.199999988,'x':-0.35},{'y':0.14,'x':-0.38},{'y':-0.01,'x':-0.39},{'y':-0.17,'x':-0.42},{'y':-0.229999989,'x':-0.37},{'y':-0.32,'x':-0.32},{'y':-0.34,'x':-0.299999982},{'y':-0.359999985,'x':-0.12},{'y':-0.34,'x':0.02},{'y':-0.37,'x':0.11},{'y':-0.37,'x':0.269999981},{'y':-0.16,'x':0.32},{'y':-0.13,'x':0.359999985},{'y':-0.06,'x':0.41}]},{'type':2,'vertices':[{'y':-0.13,'x':0.41},{'y':0.01,'x':0.41},{'y':0.08,'x':0.359999985},{'y':0.14,'x':0.31},{'y':0.16,'x':0.31},{'y':0.24,'x':0.29},{'y':0.26,'x':0.269999981},{'y':0.26,'x':0.24},{'y':0.24,'x':0.199999988},{'y':0.229999989,'x':0.149999991},{'y':0.31,'x':0.03},{'y':0.38,'x':-0.06},{'y':0.38,'x':-0.0899999961},{'y':0.359999985,'x':-0.12},{'y':0.39,'x':-0.149999991},{'y':0.39,'x':-0.16},{'y':0.359999985,'x':-0.229999989},{'y':0.26,'x':-0.329999983},{'y':0.26,'x':-0.359999985},{'y':0.229999989,'x':-0.41},{'y':0.12,'x':-0.42},{'y':0.03,'x':-0.42},{'y':-0.01,'x':-0.41},{'y':-0.0899999961,'x':-0.37},{'y':-0.11,'x':-0.34},{'y':-0.11,'x':-0.29},{'y':-0.0899999961,'x':-0.24},{'y':-0.11,'x':-0.22},{'y':-0.11,'x':-0.21},{'y':-0.24,'x':-0.0899999961},{'y':-0.38,'x':0.06},{'y':-0.399999976,'x':0.099999994},{'y':-0.399999976,'x':0.19},{'y':-0.359999985,'x':0.26},{'y':-0.229999989,'x':0.359999985},{'y':-0.17,'x':0.399999976}]},{'type':3,'vertices':[{'y':-0.0899999961,'x':0.41},{'y':-0.01,'x':0.41},{'y':0.17,'x':0.359999985},{'y':0.29,'x':0.299999982},{'y':0.37,'x':0.229999989},{'y':0.41,'x':0.099999994},{'y':0.41,'x':0.02},{'y':0.399999976,'x':-0.02},{'y':0.32,'x':-0.179999992},{'y':0.25,'x':-0.329999983},{'y':0.16,'x':-0.37},{'y':0.049999997,'x':-0.42},{'y':-0.03,'x':-0.42},{'y':-0.229999989,'x':-0.38},{'y':-0.34,'x':-0.32},{'y':-0.41,'x':-0.24},{'y':-0.41,'x':-0.149999991},{'y':-0.399999976,'x':-0.11},{'y':-0.39,'x':0.01},{'y':-0.32,'x':0.19},{'y':-0.229999989,'x':0.32}]},{'type':4,'vertices':[{'y':0.11,'x':0.429999977},{'y':0.22,'x':0.38},{'y':0.38,'x':0.21},{'y':0.41,'x':0.13},{'y':0.41,'x':0.03},{'y':0.37,'x':-0.0899999961},{'y':0.13,'x':-0.35},{'y':0.11,'x':-0.39},{'y':0.01,'x':-0.429999977},{'y':-0.21,'x':-0.429999977},{'y':-0.25,'x':-0.41},{'y':-0.35,'x':-0.329999983},{'y':-0.41,'x':-0.24},{'y':-0.41,'x':0.02},{'y':-0.19,'x':0.35},{'y':-0.06,'x':0.429999977}]},{'type':5,'vertices':[{'y':-0.26,'x':0.04},{'y':-0.22,'x':0.06},{'y':-0.16,'x':0.07},{'y':-0.08,'x':0.07},{'y':-0.21,'x':0.07},{'y':-0.24,'x':0.099999994},{'y':-0.24,'x':0.13},{'y':-0.199999988,'x':0.21},{'y':-0.16,'x':0.31},{'y':-0.08,'x':0.39},{'y':0.04,'x':0.429999977},{'y':0.099999994,'x':0.429999977},{'y':0.199999988,'x':0.38},{'y':0.28,'x':0.31},{'y':0.359999985,'x':0.229999989},{'y':0.38,'x':0.14},{'y':0.38,'x':-0.01},{'y':0.35,'x':-0.21},{'y':0.14,'x':-0.329999983},{'y':0.06,'x':-0.31},{'y':-0.03,'x':-0.41},{'y':-0.25,'x':-0.429999977},{'y':-0.359999985,'x':-0.429999977},{'y':-0.399999976,'x':-0.37},{'y':-0.399999976,'x':-0.32},{'y':-0.359999985,'x':-0.21},{'y':-0.199999988,'x':-0.049999997},{'y':-0.229999989,'x':-0.049999997}]},{'type':6,'vertices':[{'y':-0.179999992,'x':0.429999977},{'y':-0.08,'x':0.429999977},{'y':0.049999997,'x':0.38},{'y':0.14,'x':0.31},{'y':0.21,'x':0.26},{'y':0.269999981,'x':0.21},{'y':0.35,'x':0.049999997},{'y':0.35,'x':-0.19},{'y':0.299999982,'x':-0.24},{'y':0.04,'x':-0.38},{'y':-0.07,'x':-0.429999977},{'y':-0.269999981,'x':-0.429999977},{'y':-0.299999982,'x':-0.359999985},{'y':-0.359999985,'x':0.06},{'y':-0.37,'x':0.11},{'y':-0.37,'x':0.17},{'y':-0.32,'x':0.229999989},{'y':-0.269999981,'x':0.37},{'y':-0.24,'x':0.42}]},{'type':7,'vertices':[{'y':-0.06,'x':0.39},{'y':0.08,'x':0.39},{'y':0.16,'x':0.35},{'y':0.38,'x':0.099999994},{'y':0.38,'x':-0.01},{'y':0.299999982,'x':-0.22},{'y':0.229999989,'x':-0.329999983},{'y':0.179999992,'x':-0.39},{'y':0.14,'x':-0.399999976},{'y':-0.02,'x':-0.399999976},{'y':-0.19,'x':-0.37},{'y':-0.35,'x':-0.21},{'y':-0.38,'x':-0.16},{'y':-0.38,'x':0.149999991},{'y':-0.329999983,'x':0.24},{'y':-0.22,'x':0.29},{'y':-0.13,'x':0.299999982}]},{'type':8,'vertices':[{'y':-0.08,'x':0.31},{'y':0.08,'x':0.37},{'y':0.22,'x':0.41},{'y':0.25,'x':0.35},{'y':0.31,'x':0.17},{'y':0.31,'x':0},{'y':0.34,'x':-0.03},{'y':0.38,'x':-0.19},{'y':0.38,'x':-0.229999989},{'y':0.29,'x':-0.39},{'y':0.25,'x':-0.42},{'y':0.16,'x':-0.42},{'y':0.049999997,'x':-0.35},{'y':-0.049999997,'x':-0.42},{'y':-0.22,'x':-0.42},{'y':-0.24,'x':-0.39},{'y':-0.269999981,'x':-0.229999989},{'y':-0.35,'x':-0.229999989},{'y':-0.399999976,'x':-0.19},{'y':-0.399999976,'x':-0.13},{'y':-0.37,'x':0.19},{'y':-0.31,'x':0.359999985},{'y':-0.25,'x':0.429999977},{'y':-0.179999992,'x':0.429999977}]},{'type':9,'vertices':[{'x':0.41,'y':0.01},{'x':0.41,'y':0.16},{'x':0.33,'y':0.31},{'x':0.2,'y':0.39},{'x':0.14,'y':0.39},{'x':-0.02,'y':0.34},{'x':-0.21,'y':0.29},{'x':-0.34,'y':0.25},{'x':-0.42,'y':0.16},{'x':-0.41,'y':0.03},{'x':-0.4,'y':-0.09},{'x':-0.42,'y':-0.18},{'x':-0.42,'y':-0.23},{'x':-0.33,'y':-0.27},{'x':-0.12,'y':-0.39},{'x':-0.08,'y':-0.39},{'x':0.18,'y':-0.27},{'x':0.38,'y':-0.22},{'x':0.4,'y':-0.2}]},{'type':10,'vertices':[{'x':0.26,'y':0.2},{'x':0.14,'y':0.4},{'x':0.08,'y':0.4},{'x':-0.12,'y':0.27},{'x':-0.32,'y':0.02},{'x':-0.32,'y':-0.12},{'x':-0.23,'y':-0.32},{'x':-0.15,'y':-0.41},{'x':0.02,'y':-0.41},{'x':0.12,'y':-0.4},{'x':0.29,'y':-0.28},{'x':0.31,'y':-0.2},{'x':0.31,'y':0.02}]},{'type':11,'vertices':[{'x':0.41,'y':0.09},{'x':0.38,'y':0.22},{'x':0.3,'y':0.2},{'x':0.24,'y':0.37},{'x':0.23,'y':0.4},{'x':0.18,'y':0.41},{'x':-0.06,'y':0.41},{'x':-0.14,'y':0.4},{'x':-0.33,'y':0.26},{'x':-0.4,'y':0.09},{'x':-0.41,'y':-0.01},{'x':-0.42,'y':-0.05},{'x':-0.42,'y':-0.14},{'x':-0.41,'y':-0.17},{'x':-0.31,'y':-0.2},{'x':-0.2,'y':-0.31},{'x':-0.18,'y':-0.4},{'x':-0.08,'y':-0.4},{'x':0.19,'y':-0.36},{'x':0.3,'y':-0.3},{'x':0.39,'y':-0.16},{'x':0.41,'y':-0.13}]},{'type':12,'vertices':[{'x':0.41,'y':0.09},{'x':0.38,'y':0.22},{'x':0.3,'y':0.2},{'x':0.24,'y':0.37},{'x':0.23,'y':0.4},{'x':0.18,'y':0.41},{'x':-0.06,'y':0.41},{'x':-0.14,'y':0.4},{'x':-0.33,'y':0.26},{'x':-0.4,'y':0.09},{'x':-0.41,'y':-0.01},{'x':-0.42,'y':-0.05},{'x':-0.42,'y':-0.14},{'x':-0.41,'y':-0.17},{'x':-0.31,'y':-0.2},{'x':-0.2,'y':-0.31},{'x':-0.18,'y':-0.4},{'x':-0.08,'y':-0.4},{'x':0.19,'y':-0.36},{'x':0.3,'y':-0.3},{'x':0.39,'y':-0.16},{'x':0.41,'y':-0.13}]},{'type':13,'vertices':[{'x':0.41,'y':0.09},{'x':0.38,'y':0.22},{'x':0.3,'y':0.2},{'x':0.24,'y':0.37},{'x':0.23,'y':0.4},{'x':0.18,'y':0.41},{'x':-0.06,'y':0.41},{'x':-0.14,'y':0.4},{'x':-0.33,'y':0.26},{'x':-0.4,'y':0.09},{'x':-0.41,'y':-0.01},{'x':-0.42,'y':-0.05},{'x':-0.42,'y':-0.14},{'x':-0.41,'y':-0.17},{'x':-0.31,'y':-0.2},{'x':-0.2,'y':-0.31},{'x':-0.18,'y':-0.4},{'x':-0.08,'y':-0.4},{'x':0.19,'y':-0.36},{'x':0.3,'y':-0.3},{'x':0.39,'y':-0.16},{'x':0.41,'y':-0.13}]}]"
```

---

## Activty/baseact/Activity13_BounceBallController.lua.lua
**Functions:**
- OnCollision
- OnCollisionEnter
- OnCollisionStay
- OnCollisionExit
**Requires:**
- Activity13_BounceBallConfigs
**Snippet:**
```lua
local DEFAULT_GRID_WIDTH = 0.9
local DEFAULT_GRID_HEIGHT = 0.7
local DEFAULT_SHOOT_NUM = 3
local LAUNCH_INTERVAL = 0.1
local AUTO_INCREASE_COUNT = 0
local EFFECT_INCREASE_COUNT = 1
local BALL_RADIUS = 0.15
local BALL_VELOCITY = 15
local GRAVITY_SCALE = 1
local MIN_VELOCITY = 1
```

---

## Activty/baseact/Activity13_MiniGameData.lua.lua
**Snippet:**
```lua
local miniGameInfoDict
local SetMiniGameInfo = function(info)
  miniGameInfoDict = miniGameInfoDict or {}
  miniGameInfoDict[info.gameId] = info
end
local GetMiniGameInfo = function(gameId)
  if miniGameInfoDict then
    return miniGameInfoDict[gameId]
  end
end
```

---

## Activty/baseact/Activity13_MiniGameScriptList.lua.lua
**Requires:**
- Activity13_MiniGameData
- Activity13_MiniGameService
**Snippet:**
```lua
Activity13_MiniGameData = require("Activity13_MiniGameData")
Activity13_MiniGameService = require("Activity13_MiniGameService")
```

---

## Activty/baseact/Activity13_MiniGameService.lua.lua
**Snippet:**
```lua
local cachedGameId
local MiniGameInfoReq = function(gameId, rspCallback)
  local info = ActivityDungeonData.GetActivityInfo()
  local activityId = info.baseInfo.activityId
  Net.Send(Proto.MsgName.ActivityGetMiniGameReq, {activityId = activityId, gameId = gameId}, rspCallback)
end
local MiniGameInfoRsp = function(msg)
  Activity13_MiniGameData.SetMiniGameInfo(msg)
  UIMgr:SendWindowMessage(WinResConfig.Activity13BounceMiniGameMainWindow.name, WindowMsgEnum.Activity13_MiniGame.REFRESH_MINIGAME_INFO)
  UIMgr:SendWindowMessage(WinResConfig.Activity13BounceMiniGameWindow.name, WindowMsgEnum.Activity13_MiniGame.REFRESH_MINIGAME_INFO)
```

---

## Activty/baseact/Activity14BossBattleWindow.lua.lua
**Functions:**
- Activity14BossBattleWindow.ReInitData
- Activity14BossBattleWindow.OnInit
- Activity14BossBattleWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity14BossBattleWindow.FormatRemainTime
- Activity14BossBattleWindow.GetChapter
- Activity14BossBattleWindow.InitBtn
- Activity14BossBattleWindow.CloseWindow
- Activity14BossBattleWindow.OnClose
**Requires:**
- ActivityDungeon1014_BossBattleWindowByName
**Snippet:**
```lua
require("ActivityDungeon1014_BossBattleWindowByName")
local Activity14BossBattleWindow = {}
local uis, contentPane, activityInfo

function Activity14BossBattleWindow.ReInitData()
end

function Activity14BossBattleWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity14BossBattleWindow.package, WinResConfig.Activity14BossBattleWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity14BuyLevelDesWindow.lua.lua
**Functions:**
- Activity14BuyLevelDesWindow.ReInitData
- Activity14BuyLevelDesWindow.OnInit
- Activity14BuyLevelDesWindow.ShowAssetsTips
- Activity14BuyLevelDesWindow.UpdateTextDisplay
- Activity14BuyLevelDesWindow.Init
- Activity14BuyLevelDesWindow.GetGold
- Activity14BuyLevelDesWindow.ShowReward
- list.itemRenderer
- Activity14BuyLevelDesWindow.GetRewardItem
- Activity14BuyLevelDesWindow.GetLvData
- Activity14BuyLevelDesWindow.GetRewardLvData
- Activity14BuyLevelDesWindow.GetRewardByPhaseId
- Activity14BuyLevelDesWindow.BuyLevelRsp
- Activity14BuyLevelDesWindow.InitBtn
- waitFun
- Activity14BuyLevelDesWindow.HandleMessage
- Activity14BuyLevelDesWindow.OnShown
- Activity14BuyLevelDesWindow.OnClose
**Requires:**
- ActivityDungeon1014_BuyLevelDesWindowByName
**Snippet:**
```lua
require("ActivityDungeon1014_BuyLevelDesWindowByName")
local Activity14BuyLevelDesWindow = {}
local uis, contentPane, lvData, curLv, buyNum, itemId, lvMax, waitFun, rewardData, itemSort, transPlay, firstPlay, tatalGold, passInfo

function Activity14BuyLevelDesWindow.ReInitData()
end

function Activity14BuyLevelDesWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity14BuyLevelDesWindow.package, WinResConfig.Activity14BuyLevelDesWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity14ChallengeWindow.lua.lua
**Functions:**
- Activity14ChallengeWindow.ReInitData
- Activity14ChallengeWindow.OnInit
- Activity14ChallengeWindow.UpdateInfo
- uis.Main.ChapterList.itemRenderer
- Activity14ChallengeWindow.ShoweStage
- Activity14ChallengeWindow.StageItemClick
- Activity14ChallengeWindow.ShopInfo
- Activity14ChallengeWindow.GetChapterPassById
- Activity14ChallengeWindow.GetCurStage
- Activity14ChallengeWindow.GetFirstChapter
- Activity14ChallengeWindow.GetAllChapterId
- Activity14ChallengeWindow.InitBtn
- Activity14ChallengeWindow.CloseWindow
- Activity14ChallengeWindow.OnShown
- Activity14ChallengeWindow.OnClose
**Requires:**
- ActivityDungeon1014_ChallengeWindowByName
**Snippet:**
```lua
require("ActivityDungeon1014_ChallengeWindowByName")
local Activity14ChallengeWindow = {}
local uis, contentPane, activityInfo, scrollingTween

function Activity14ChallengeWindow.ReInitData()
end

function Activity14ChallengeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity14ChallengeWindow.package, WinResConfig.Activity14ChallengeWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity14DungeonWindow.lua.lua
**Functions:**
- Activity14DungeonWindow.ReInitData
- Activity14DungeonWindow.OnInit
- Activity14DungeonWindow.LoadBg
- Activity14DungeonWindow.InitRedDot
- Activity14DungeonWindow.UpdateInfo
- Activity14DungeonWindow.InitBtnTxt
- Activity14DungeonWindow.InitBtn
- Activity14DungeonWindow.OnShown
- Activity14DungeonWindow.OnClose
- Activity14DungeonWindow.HandleMessage
**Requires:**
- ActivityDungeon1014_ActivityDungeonWindowByName
**Snippet:**
```lua
require("ActivityDungeon1014_ActivityDungeonWindowByName")
local Activity14DungeonWindow = {}
local uis, contentPane, jumpTb, configData, activityInfo, effect
local gameId = 70441018
local InitMiniGameInfo = function()
  local data = ActivityDungeonData.GetActivityData()
  if data.id == 70440014 then
    ld("Activity14_MiniGame")
    Activity14_MiniGameService.MiniGameInfoReq(gameId, function()
      RedDotMgr.AddNode({
```

---

## Activty/baseact/Activity14MaterialWindow.lua.lua
**Functions:**
- Activity14MaterialWindow.ReInitData
- Activity14MaterialWindow.OnInit
- Activity14MaterialWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity14MaterialWindow.GetChapter
- Activity14MaterialWindow.GetMaxCount
- Activity14MaterialWindow.InitBtn
- Activity14MaterialWindow.CloseWindow
- Activity14MaterialWindow.OnShown
- Activity14MaterialWindow.OnClose
**Requires:**
- ActivityDungeon1014_MaterialWindowByName
**Snippet:**
```lua
require("ActivityDungeon1014_MaterialWindowByName")
local Activity14MaterialWindow = {}
local uis, contentPane, activityInfo, maxCount, posX

function Activity14MaterialWindow.ReInitData()
end

function Activity14MaterialWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity14MaterialWindow.package, WinResConfig.Activity14MaterialWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity14MiniGameMainWindow.lua.lua
**Functions:**
- Activity14MiniGameMainWindow.ReInitData
- Activity14MiniGameMainWindow.OnInit
- Activity14MiniGameMainWindow.UpdateInfo
- Activity14MiniGameMainWindow.InitBtn
- Activity14MiniGameMainWindow.OnClose
- Activity14MiniGameMainWindow.HandleMessage
**Requires:**
- ActivityDungeon1014_MiniGameWindowByName
**Snippet:**
```lua
require("ActivityDungeon1014_MiniGameWindowByName")
local Activity14MiniGameMainWindow = {}
local uis, contentPane
local gameId = 70441018
ld("Activity14_MiniGame")
local RefreshPanelInfo = function()
  local info = Activity14_MiniGameData.GetMiniGameInfo(gameId)
  local conf = TableData.GetConfig(gameId, "BaseActivityStageGame")
  local str = conf.game_day_reward[1]
  local splits = Split(str, ":")
```

---

## Activty/baseact/Activity14MiniGameSubmitWindow.lua.lua
**Functions:**
- Activity14MiniGameSubmitWindow.ReInitData
- Activity14MiniGameSubmitWindow.OnInit
- Activity14MiniGameSubmitWindow.UpdateInfo
- Activity14MiniGameSubmitWindow.InitBtn
- Activity14MiniGameSubmitWindow.OnClose
**Requires:**
- ActivityDungeon1014_MiniStart_EndRewardWindowByName
**Snippet:**
```lua
require("ActivityDungeon1014_MiniStart_EndRewardWindowByName")
local Activity14MiniGameSubmitWindow = {}
local uis, contentPane, score

function Activity14MiniGameSubmitWindow.ReInitData()
end

function Activity14MiniGameSubmitWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity14MiniGameSubmitWindow.package, WinResConfig.Activity14MiniGameSubmitWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity14MiniGameTaskWindow.lua.lua
**Functions:**
- RefreshRewardList
- list.itemRenderer
- itemlist.itemRenderer
- Activity14MiniGameTaskWindow.ReInitData
- Activity14MiniGameTaskWindow.OnInit
- Activity14MiniGameTaskWindow.UpdateInfo
- Activity14MiniGameTaskWindow.InitBtn
- Activity14MiniGameTaskWindow.OnClose
**Requires:**
- ActivityDungeon1014_MiniTaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1014_MiniTaskWindowByName")
local Activity14MiniGameTaskWindow = {}
local uis, contentPane
local gameId = 70441018

local function RefreshRewardList()
  local info = Activity14_MiniGameData.GetMiniGameInfo(gameId)
  local minigame_tasks = info.taskList
  local list = uis.Main.TipsList
  list:SetVirtual()
```

---

## Activty/baseact/Activity14MiniGameWindow.lua.lua
**Functions:**
- Activity14MiniGameWindow.ReInitData
- Activity14MiniGameWindow.OnInit
- Activity14MiniGameWindow.UpdateInfo
- Activity14MiniGameWindow.InitBtn
- Activity14MiniGameWindow.OnClose
- Activity14MiniGameWindow.HandleMessage
**Requires:**
- ActivityDungeon1014_MiniGameStartWindowByName
- Activity14_MiniGameController
**Snippet:**
```lua
require("ActivityDungeon1014_MiniGameStartWindowByName")
local Activity14MiniGameWindow = {}
local uis, contentPane
local controller = require("Activity14_MiniGameController")
local blockObjs, sceneItemObjs, playerData, playerObj
local FADE_IN_DURATION = 0.8
local PLAYER_SCALE = 0.4
local BLOCK_ASSET_LOOKUP = {
  [1] = "Assets/Art/Effects/Prefab/UI_prefab/MiniGame/MiniGame016/Minigame016_type1_1_cube.prefab",
  [2] = "Assets/Art/Effects/Prefab/UI_prefab/MiniGame/MiniGame016/Minigame016_type1_2_cube.prefab",
```

---

## Activty/baseact/Activity14PassportLevelUpTipsWindow.lua.lua
**Functions:**
- Activity14PassportLevelUpTipsWindow.ReInitData
- Activity14PassportLevelUpTipsWindow.OnInit
- Activity14PassportLevelUpTipsWindow.UpdateInfo
- Activity14PassportLevelUpTipsWindow.InitBtn
- Activity14PassportLevelUpTipsWindow.OnClose
**Requires:**
- ActivityDungeon1014_PassportUp_LevelUpTipsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1014_PassportUp_LevelUpTipsWindowByName")
local Activity14PassportLevelUpTipsWindow = {}
local uis, contentPane, lv

function Activity14PassportLevelUpTipsWindow.ReInitData()
end

function Activity14PassportLevelUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity14PassportLevelUpTipsWindow.package, WinResConfig.Activity14PassportLevelUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity14PassportWindow.lua.lua
**Functions:**
- Activity14PassportWindow.ReInitData
- Activity14PassportWindow.OnInit
- Activity14PassportWindow.UpdateTextDisplay
- Activity14PassportWindow.InitPassport
- uis.Main.TabRegion.TabList.itemRenderer
- Activity14PassportWindow.InitEffect
- Activity14PassportWindow.InitLv
- Activity14PassportWindow.ShowLevelUp
- Activity14PassportWindow.SaveLevel
- Activity14PassportWindow.GetRewardByLv
- Activity14PassportWindow.GetRewardNum
- Activity14PassportWindow.IsGetAllReward
- Activity14PassportWindow.ShowReward
- Activity14PassportWindow.GetUpdateLv
- Activity14PassportWindow.RefreshListReward
- Activity14PassportWindow.CheckItemTime
- Activity14PassportWindow.ShowQuitTips
- Activity14PassportWindow.RefreshUI
- Activity14PassportWindow.GetExpMxp
- Activity14PassportWindow.SetLevelInfo
- Activity14PassportWindow.InitList
- list.itemRenderer
- Activity14PassportWindow.SetListPos
- Activity14PassportWindow.RefreshReward
- Activity14PassportWindow.ShowGetEffect
- Activity14PassportWindow.RewardItemClick
- Activity14PassportWindow.IsReward
- Activity14PassportWindow.RefreshRewardFirst
- Activity14PassportWindow.RefreshRewardEnd
- Activity14PassportWindow.ShowState
- Activity14PassportWindow.RefreshRewardShow
- Activity14PassportWindow.RefreshRewardState
- Activity14PassportWindow.PassportActivate
- Activity14PassportWindow.CloseWindow
- Activity14PassportWindow.InitBtn
- Activity14PassportWindow.ShowExpBarAnim
- Activity14PassportWindow.InitTask
- list.itemRenderer
- Activity14PassportWindow.InitClothes
- clothes.BuyReward.RewardList.itemRenderer
- Activity14PassportWindow.SetLastLv
- Activity14PassportWindow.PlayFirstRewardEffect
- Activity14PassportWindow.PlayEndRewardEffect
- Activity14PassportWindow.HandleMessage
- Activity14PassportWindow.OnShown
- Activity14PassportWindow.OnClose
**Requires:**
- ActivityDungeon1014_PassportWindowByName
**Snippet:**
```lua
require("ActivityDungeon1014_PassportWindowByName")
local Activity14PassportWindow = {}
local uis, contentPane, passInfo, lvMax, modelType, expMax, rewardData, rewardType, rewardLv, listPage, passLv, jumpTb, isShowAllGet, passPortConfig, lvTween, lastLv, waitMessageId, newPassPort, animTween

function Activity14PassportWindow.ReInitData()
end

function Activity14PassportWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity14PassportWindow.package, WinResConfig.Activity14PassportWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity14PlotWindow.lua.lua
**Functions:**
- Activity14PlotWindow.ReInitData
- Activity14PlotWindow.OnInit
- Activity14PlotWindow.UpdateInfo
- list.itemRenderer
- Activity14PlotWindow.InitBtn
- Activity14PlotWindow.CloseWindow
- Activity14PlotWindow.OnClose
**Requires:**
- ActivityDungeon1014_PlotWindowByName
**Snippet:**
```lua
require("ActivityDungeon1014_PlotWindowByName")
local Activity14PlotWindow = {}
local uis, contentPane, configData

function Activity14PlotWindow.ReInitData()
end

function Activity14PlotWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity14PlotWindow.package, WinResConfig.Activity14PlotWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity14ShopWindow.lua.lua
**Functions:**
- Activity14ShopWindow.ReInitData
- Activity14ShopWindow.OnInit
- Activity14ShopWindow.UpdateInfo
- uis.Main.ItemList.itemRenderer
- Activity14ShopWindow.ShowItem
- list.itemRenderer
- Activity14ShopWindow.ShowOneReward
- list.itemRenderer
- Activity14ShopWindow.GetShopGrid
- Activity14ShopWindow.InitBtn
- Activity14ShopWindow.CloseWindow
- Activity14ShopWindow.OnClose
- Activity14ShopWindow.HandleMessage
**Requires:**
- ActivityDungeon1014_ShopWindowByName
**Snippet:**
```lua
require("ActivityDungeon1014_ShopWindowByName")
local Activity14ShopWindow = {}
local uis, contentPane, activityInfo, tempAssetsTips

function Activity14ShopWindow.ReInitData()
end

function Activity14ShopWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity14ShopWindow.package, WinResConfig.Activity14ShopWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity14SignWindow.lua.lua
**Functions:**
- Activity14SignWindow.ReInitData
- Activity14SignWindow.OnInit
- Activity14SignWindow.UpdateInfo
- list.RewardList.itemRenderer
- Activity14SignWindow.ShowAllItemFrame
- Activity14SignWindow.GetRewardData
- Activity14SignWindow.InitBtn
- Activity14SignWindow.CloseWindow
- Activity14SignWindow.OnClose
**Requires:**
- ActivityDungeon1014_SignWindowByName
**Snippet:**
```lua
require("ActivityDungeon1014_SignWindowByName")
local Activity14SignWindow = {}
local uis, contentPane, activityInfo

function Activity14SignWindow.ReInitData()
end

function Activity14SignWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity14SignWindow.package, WinResConfig.Activity14SignWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity14TaskWindow.lua.lua
**Functions:**
- Activity14TaskWindow.ReInitData
- Activity14TaskWindow.OnInit
- Activity14TaskWindow.UpdateInfo
- list.itemRenderer
- rewardList.itemRenderer
- Activity14TaskWindow.GetRewardNum
- Activity14TaskWindow.ShowAllItemFrame
- Activity14TaskWindow.SortTask
- Activity14TaskWindow.InitBtn
- Activity14TaskWindow.CloseWindow
- Activity14TaskWindow.OnClose
**Requires:**
- ActivityDungeon1014_TaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1014_TaskWindowByName")
local Activity14TaskWindow = {}
local uis, contentPane

function Activity14TaskWindow.ReInitData()
end

function Activity14TaskWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity14TaskWindow.package, WinResConfig.Activity14TaskWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity14_MiniGameController.lua.lua
**Functions:**
- TweenPlayerJumpAndDrop
**Snippet:**
```lua
local GAP_VERTICAL, GAP_HORIZONTAL = 1, 0.75
local BLOCK_WIDTH, BLOCK_HEIGHT = 2, 2
local NUM_CHANNELS = 4
local PLAYER_PIVOT_Y = 0.5
local SCENE_OBJ_SCALE = 4.5
local VISIBLE_BLOCKS = 7
local VISIBLE_DISTANCE = 26
local JUMP_TIME_PERCENT = 0.5
local MAX_LONGITUDINAL_SEPARATION = 3
local MAX_HEIGHT = 2.5
```

---

## Activty/baseact/Activity14_MiniGameData.lua.lua
**Snippet:**
```lua
local miniGameInfoDict
local SetMiniGameInfo = function(info)
  miniGameInfoDict = miniGameInfoDict or {}
  miniGameInfoDict[info.gameId] = info
end
local GetMiniGameInfo = function(gameId)
  if miniGameInfoDict then
    return miniGameInfoDict[gameId]
  end
end
```

---

## Activty/baseact/Activity14_MiniGameScriptList.lua.lua
**Requires:**
- Activity14_MiniGameData
- Activity14_MiniGameService
**Snippet:**
```lua
Activity14_MiniGameData = require("Activity14_MiniGameData")
Activity14_MiniGameService = require("Activity14_MiniGameService")
```

---

## Activty/baseact/Activity14_MiniGameService.lua.lua
**Snippet:**
```lua
local cachedGameId
local MiniGameInfoReq = function(gameId, rspCallback)
  local info = ActivityDungeonData.GetActivityInfo()
  local activityId = info.baseInfo.activityId
  Net.Send(Proto.MsgName.ActivityGetMiniGameReq, {activityId = activityId, gameId = gameId}, rspCallback)
end
local MiniGameInfoRsp = function(msg)
  Activity14_MiniGameData.SetMiniGameInfo(msg)
  UIMgr:SendWindowMessage(WinResConfig.Activity14MiniGameMainWindow.name, WindowMsgEnum.Activity14_MiniGame.REFRESH_MINIGAME_INFO)
  UIMgr:SendWindowMessage(WinResConfig.Activity14MiniGameWindow.name, WindowMsgEnum.Activity14_MiniGame.REFRESH_MINIGAME_INFO)
```

---

## Activty/baseact/Activity15BossBattleWindow.lua.lua
**Functions:**
- Activity15BossBattleWindow.ReInitData
- Activity15BossBattleWindow.OnInit
- Activity15BossBattleWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity15BossBattleWindow.FormatRemainTime
- Activity15BossBattleWindow.GetChapter
- Activity15BossBattleWindow.InitBtn
- Activity15BossBattleWindow.CloseWindow
- Activity15BossBattleWindow.OnClose
**Requires:**
- ActivityDungeon1015_BossBattleWindowByName
**Snippet:**
```lua
require("ActivityDungeon1015_BossBattleWindowByName")
local Activity15BossBattleWindow = {}
local uis, contentPane, activityInfo

function Activity15BossBattleWindow.ReInitData()
end

function Activity15BossBattleWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity15BossBattleWindow.package, WinResConfig.Activity15BossBattleWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity15BuyLevelDesWindow.lua.lua
**Functions:**
- Activity15BuyLevelDesWindow.ReInitData
- Activity15BuyLevelDesWindow.OnInit
- Activity15BuyLevelDesWindow.ShowAssetsTips
- Activity15BuyLevelDesWindow.UpdateTextDisplay
- Activity15BuyLevelDesWindow.Init
- Activity15BuyLevelDesWindow.GetGold
- Activity15BuyLevelDesWindow.ShowReward
- list.itemRenderer
- Activity15BuyLevelDesWindow.GetRewardItem
- Activity15BuyLevelDesWindow.GetLvData
- Activity15BuyLevelDesWindow.GetRewardLvData
- Activity15BuyLevelDesWindow.GetRewardByPhaseId
- Activity15BuyLevelDesWindow.BuyLevelRsp
- Activity15BuyLevelDesWindow.InitBtn
- waitFun
- Activity15BuyLevelDesWindow.HandleMessage
- Activity15BuyLevelDesWindow.OnShown
- Activity15BuyLevelDesWindow.OnClose
**Requires:**
- ActivityDungeon1015_BuyLevelDesWindowByName
**Snippet:**
```lua
require("ActivityDungeon1015_BuyLevelDesWindowByName")
local Activity15BuyLevelDesWindow = {}
local uis, contentPane, lvData, curLv, buyNum, itemId, lvMax, waitFun, rewardData, itemSort, transPlay, firstPlay, tatalGold, passInfo

function Activity15BuyLevelDesWindow.ReInitData()
end

function Activity15BuyLevelDesWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity15BuyLevelDesWindow.package, WinResConfig.Activity15BuyLevelDesWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity15ChallengeWindow.lua.lua
**Functions:**
- Activity15ChallengeWindow.ReInitData
- Activity15ChallengeWindow.OnInit
- Activity15ChallengeWindow.UpdateInfo
- uis.Main.ChapterList.itemRenderer
- Activity15ChallengeWindow.ShoweStage
- Activity15ChallengeWindow.StageItemClick
- Activity15ChallengeWindow.ShopInfo
- Activity15ChallengeWindow.GetChapterPassById
- Activity15ChallengeWindow.GetCurStage
- Activity15ChallengeWindow.GetFirstChapter
- Activity15ChallengeWindow.GetAllChapterId
- Activity15ChallengeWindow.InitBtn
- Activity15ChallengeWindow.CloseWindow
- Activity15ChallengeWindow.OnShown
- Activity15ChallengeWindow.OnClose
**Requires:**
- ActivityDungeon1015_ChallengeWindowByName
**Snippet:**
```lua
require("ActivityDungeon1015_ChallengeWindowByName")
local Activity15ChallengeWindow = {}
local uis, contentPane, activityInfo, scrollingTween

function Activity15ChallengeWindow.ReInitData()
end

function Activity15ChallengeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity15ChallengeWindow.package, WinResConfig.Activity15ChallengeWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity15DungeonWindow.lua.lua
**Functions:**
- Activity15DungeonWindow.ReInitData
- Activity15DungeonWindow.OnInit
- Activity15DungeonWindow.LoadBg
- Activity15DungeonWindow.InitRedDot
- Activity15DungeonWindow.UpdateInfo
- Activity15DungeonWindow.InitBtnTxt
- Activity15DungeonWindow.InitBtn
- Activity15DungeonWindow.OnShown
- Activity15DungeonWindow.OnClose
- Activity15DungeonWindow.HandleMessage
**Requires:**
- ActivityDungeon1015_ActivityDungeonWindowByName
**Snippet:**
```lua
require("ActivityDungeon1015_ActivityDungeonWindowByName")
local Activity15DungeonWindow = {}
local uis, contentPane, jumpTb, configData, activityInfo, effect
local InitMiniGameInfo = function()
  local data = ActivityDungeonData.GetActivityData()
  if data.id == 70440015 then
    ld("Activity15_MiniGame")
    Activity15_MiniGameService.MiniGameInfoReq(function()
      RedDotMgr.AddNode({
        windowName = WinResConfig.Activity15DungeonWindow.name,
```

---

## Activty/baseact/Activity15MaterialWindow.lua.lua
**Functions:**
- Activity15MaterialWindow.ReInitData
- Activity15MaterialWindow.OnInit
- Activity15MaterialWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity15MaterialWindow.GetChapter
- Activity15MaterialWindow.GetMaxCount
- Activity15MaterialWindow.InitBtn
- Activity15MaterialWindow.CloseWindow
- Activity15MaterialWindow.OnShown
- Activity15MaterialWindow.OnClose
**Requires:**
- ActivityDungeon1015_MaterialWindowByName
**Snippet:**
```lua
require("ActivityDungeon1015_MaterialWindowByName")
local Activity15MaterialWindow = {}
local uis, contentPane, activityInfo, maxCount, posX

function Activity15MaterialWindow.ReInitData()
end

function Activity15MaterialWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity15MaterialWindow.package, WinResConfig.Activity15MaterialWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity15MiniExplainWindow.lua.lua
**Functions:**
- Activity15MiniExplainWindow.ReInitData
- Activity15MiniExplainWindow.OnInit
- Activity15MiniExplainWindow.UpdateInfo
- Activity15MiniExplainWindow.InitBtn
- Activity15MiniExplainWindow.OnClose
**Requires:**
- ActivityDungeon1015_MiniTipsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1015_MiniTipsWindowByName")
local Activity15MiniExplainWindow = {}
local uis, contentPane, closeCallback

function Activity15MiniExplainWindow.ReInitData()
end

function Activity15MiniExplainWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity15MiniExplainWindow.package, WinResConfig.Activity15MiniExplainWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity15MiniGameMainWindow.lua.lua
**Functions:**
- RefreshPanelInfo
- Activity15MiniGameMainWindow.ReInitData
- Activity15MiniGameMainWindow.OnInit
- Activity15MiniGameMainWindow.UpdateInfo
- Activity15MiniGameMainWindow.InitBtn
- Activity15MiniGameMainWindow.OnClose
- Activity15MiniGameMainWindow.HandleMessage
**Requires:**
- ActivityDungeon1015_MiniGameWindowByName
**Snippet:**
```lua
require("ActivityDungeon1015_MiniGameWindowByName")
ld("Activity15_MiniGame")
local Activity15MiniGameMainWindow = {}
local uis, contentPane

local function RefreshPanelInfo()
  local info = Activity15_MiniGameData.GetMiniGameInfo()
  local conf = TableData.GetConfig(Activity15_MiniGameData.gameId, "BaseActivityStageGame")
  local str = conf.game_day_reward[1]
  local splits = Split(str, ":")
```

---

## Activty/baseact/Activity15MiniGameSubmitWindow.lua.lua
**Functions:**
- Activity15MiniGameSubmitWindow.ReInitData
- Activity15MiniGameSubmitWindow.OnInit
- Activity15MiniGameSubmitWindow.UpdateInfo
- Activity15MiniGameSubmitWindow.InitBtn
- Activity15MiniGameSubmitWindow.OnClose
**Requires:**
- ActivityDungeon1015_MiniStart_EndRewardWindowByName
**Snippet:**
```lua
require("ActivityDungeon1015_MiniStart_EndRewardWindowByName")
local Activity15MiniGameSubmitWindow = {}
local uis, contentPane, nowIntegral

function Activity15MiniGameSubmitWindow.ReInitData()
end

function Activity15MiniGameSubmitWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity15MiniGameSubmitWindow.package, WinResConfig.Activity15MiniGameSubmitWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity15MiniGameTaskWindow.lua.lua
**Functions:**
- RefreshRewardList
- list.itemRenderer
- itemlist.itemRenderer
- Activity15MiniGameTaskWindow.ReInitData
- Activity15MiniGameTaskWindow.OnInit
- Activity15MiniGameTaskWindow.UpdateInfo
- Activity15MiniGameTaskWindow.InitBtn
- Activity15MiniGameTaskWindow.OnClose
**Requires:**
- ActivityDungeon1015_MiniTaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1015_MiniTaskWindowByName")
local Activity15MiniGameTaskWindow = {}
local uis, contentPane

local function RefreshRewardList()
  local info = Activity15_MiniGameData.GetMiniGameInfo()
  local minigame_tasks = info.taskList
  local list = uis.Main.TipsList
  list:SetVirtual()
  
```

---

## Activty/baseact/Activity15MiniGameWindow.lua.lua
**Functions:**
- Activity15MiniGameWindow.ReInitData
- Activity15MiniGameWindow.OnInit
- Activity15MiniGameWindow.UpdateInfo
- Activity15MiniGameWindow.Update
- Activity15MiniGameWindow.CheckJumpOver
- Activity15MiniGameWindow.SaveStartJumpState
- Activity15MiniGameWindow.DisposeItem
- Activity15MiniGameWindow.GetBallById
- Activity15MiniGameWindow.RemoveBallById
- Activity15MiniGameWindow.CreateBall
- ball.UpdateBallPos
- ball.CanDispose
- Activity15MiniGameWindow.InitInput
- Activity15MiniGameWindow.ClearTween
- Activity15MiniGameWindow.UpdateIntegral
- Activity15MiniGameWindow.GetConfigByTime
- Activity15MiniGameWindow.GetItemConfig
- Activity15MiniGameWindow.OnGameOver
- Activity15MiniGameWindow.OnNext
- Activity15MiniGameWindow.InitBtn
- Activity15MiniGameWindow.HandleMessage
- Activity15MiniGameWindow.OnClose
**Requires:**
- ActivityDungeon1015_MiniGameStartWindowByName
**Snippet:**
```lua
require("ActivityDungeon1015_MiniGameStartWindowByName")
local Activity15MiniGameWindow = {}
local uis, contentPane, score, configData, directionCom, bottom, chrAnimEffectHolder, allBall, gameTime, curData, playerRadius, createTime, startJumpPlayerInfo, idIndex, gameStop, jumpBtn, root, interval
local guguSpeed = 50
local moveSpeed = 400
local oneJumpDis = 150
local twoJumpDis = 100
local timeUpSpeed = 500
local timeDownSpeed = 580
local down = 650
```

---

## Activty/baseact/Activity15MiniSetWindow.lua.lua
**Functions:**
- Activity15MiniSetWindow.ReInitData
- Activity15MiniSetWindow.OnInit
- Activity15MiniSetWindow.UpdateInfo
- Activity15MiniSetWindow.InitBtn
- Activity15MiniSetWindow.OnClose
**Requires:**
- ActivityDungeon1015_MiniSetWindowByName
**Snippet:**
```lua
require("ActivityDungeon1015_MiniSetWindowByName")
local Activity15MiniSetWindow = {}
local uis, contentPane

function Activity15MiniSetWindow.ReInitData()
end

function Activity15MiniSetWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity15MiniSetWindow.package, WinResConfig.Activity15MiniSetWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity15PassportLevelUpTipsWindow.lua.lua
**Functions:**
- Activity15PassportLevelUpTipsWindow.ReInitData
- Activity15PassportLevelUpTipsWindow.OnInit
- Activity15PassportLevelUpTipsWindow.UpdateInfo
- Activity15PassportLevelUpTipsWindow.InitBtn
- Activity15PassportLevelUpTipsWindow.OnClose
**Requires:**
- ActivityDungeon1015_PassportUp_LevelUpTipsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1015_PassportUp_LevelUpTipsWindowByName")
local Activity15PassportLevelUpTipsWindow = {}
local uis, contentPane, lv

function Activity15PassportLevelUpTipsWindow.ReInitData()
end

function Activity15PassportLevelUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity15PassportLevelUpTipsWindow.package, WinResConfig.Activity15PassportLevelUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity15PassportWindow.lua.lua
**Functions:**
- Activity15PassportWindow.ReInitData
- Activity15PassportWindow.OnInit
- Activity15PassportWindow.UpdateTextDisplay
- Activity15PassportWindow.InitPassport
- uis.Main.TabRegion.TabList.itemRenderer
- Activity15PassportWindow.InitEffect
- Activity15PassportWindow.InitLv
- Activity15PassportWindow.ShowLevelUp
- Activity15PassportWindow.SaveLevel
- Activity15PassportWindow.GetRewardByLv
- Activity15PassportWindow.GetRewardNum
- Activity15PassportWindow.IsGetAllReward
- Activity15PassportWindow.ShowReward
- Activity15PassportWindow.GetUpdateLv
- Activity15PassportWindow.RefreshListReward
- Activity15PassportWindow.CheckItemTime
- Activity15PassportWindow.ShowQuitTips
- Activity15PassportWindow.RefreshUI
- Activity15PassportWindow.GetExpMxp
- Activity15PassportWindow.SetLevelInfo
- Activity15PassportWindow.InitList
- list.itemRenderer
- Activity15PassportWindow.SetListPos
- Activity15PassportWindow.RefreshReward
- Activity15PassportWindow.ShowGetEffect
- Activity15PassportWindow.RewardItemClick
- Activity15PassportWindow.IsReward
- Activity15PassportWindow.RefreshRewardFirst
- Activity15PassportWindow.RefreshRewardEnd
- Activity15PassportWindow.ShowState
- Activity15PassportWindow.RefreshRewardShow
- Activity15PassportWindow.RefreshRewardState
- Activity15PassportWindow.PassportActivate
- Activity15PassportWindow.CloseWindow
- Activity15PassportWindow.InitBtn
- Activity15PassportWindow.ShowExpBarAnim
- Activity15PassportWindow.InitTask
- list.itemRenderer
- Activity15PassportWindow.InitClothes
- clothes.BuyReward.RewardList.itemRenderer
- Activity15PassportWindow.SetLastLv
- Activity15PassportWindow.PlayFirstRewardEffect
- Activity15PassportWindow.PlayEndRewardEffect
- Activity15PassportWindow.HandleMessage
- Activity15PassportWindow.OnShown
- Activity15PassportWindow.OnClose
**Requires:**
- ActivityDungeon1015_PassportWindowByName
**Snippet:**
```lua
require("ActivityDungeon1015_PassportWindowByName")
local Activity15PassportWindow = {}
local uis, contentPane, passInfo, lvMax, modelType, expMax, rewardData, rewardType, rewardLv, listPage, passLv, jumpTb, isShowAllGet, passPortConfig, lvTween, lastLv, waitMessageId, newPassPort, animTween

function Activity15PassportWindow.ReInitData()
end

function Activity15PassportWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity15PassportWindow.package, WinResConfig.Activity15PassportWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity15PlotWindow.lua.lua
**Functions:**
- Activity15PlotWindow.ReInitData
- Activity15PlotWindow.OnInit
- Activity15PlotWindow.UpdateInfo
- list.itemRenderer
- Activity15PlotWindow.InitBtn
- Activity15PlotWindow.CloseWindow
- Activity15PlotWindow.OnClose
**Requires:**
- ActivityDungeon1015_PlotWindowByName
**Snippet:**
```lua
require("ActivityDungeon1015_PlotWindowByName")
local Activity15PlotWindow = {}
local uis, contentPane, configData

function Activity15PlotWindow.ReInitData()
end

function Activity15PlotWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity15PlotWindow.package, WinResConfig.Activity15PlotWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity15ShopWindow.lua.lua
**Functions:**
- Activity15ShopWindow.ReInitData
- Activity15ShopWindow.OnInit
- Activity15ShopWindow.UpdateInfo
- uis.Main.ItemList.itemRenderer
- Activity15ShopWindow.ShowItem
- list.itemRenderer
- Activity15ShopWindow.ShowOneReward
- list.itemRenderer
- Activity15ShopWindow.GetShopGrid
- Activity15ShopWindow.InitBtn
- Activity15ShopWindow.CloseWindow
- Activity15ShopWindow.OnClose
- Activity15ShopWindow.HandleMessage
**Requires:**
- ActivityDungeon1015_ShopWindowByName
**Snippet:**
```lua
require("ActivityDungeon1015_ShopWindowByName")
local Activity15ShopWindow = {}
local uis, contentPane, activityInfo, tempAssetsTips

function Activity15ShopWindow.ReInitData()
end

function Activity15ShopWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity15ShopWindow.package, WinResConfig.Activity15ShopWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity15SignWindow.lua.lua
**Functions:**
- Activity15SignWindow.ReInitData
- Activity15SignWindow.OnInit
- Activity15SignWindow.UpdateInfo
- list.RewardList.itemRenderer
- Activity15SignWindow.ShowAllItemFrame
- Activity15SignWindow.GetRewardData
- Activity15SignWindow.InitBtn
- Activity15SignWindow.CloseWindow
- Activity15SignWindow.OnClose
**Requires:**
- ActivityDungeon1015_SignWindowByName
**Snippet:**
```lua
require("ActivityDungeon1015_SignWindowByName")
local Activity15SignWindow = {}
local uis, contentPane, activityInfo

function Activity15SignWindow.ReInitData()
end

function Activity15SignWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity15SignWindow.package, WinResConfig.Activity15SignWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity15TaskWindow.lua.lua
**Functions:**
- Activity15TaskWindow.ReInitData
- Activity15TaskWindow.OnInit
- Activity15TaskWindow.UpdateInfo
- list.itemRenderer
- rewardList.itemRenderer
- Activity15TaskWindow.GetRewardNum
- Activity15TaskWindow.ShowAllItemFrame
- Activity15TaskWindow.SortTask
- Activity15TaskWindow.InitBtn
- Activity15TaskWindow.CloseWindow
- Activity15TaskWindow.OnClose
**Requires:**
- ActivityDungeon1015_TaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1015_TaskWindowByName")
local Activity15TaskWindow = {}
local uis, contentPane

function Activity15TaskWindow.ReInitData()
end

function Activity15TaskWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity15TaskWindow.package, WinResConfig.Activity15TaskWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity15_MiniGameData.lua.lua
**Functions:**
- Activity15_MiniGameData.SetMiniGameInfo
- Activity15_MiniGameData.GetMiniGameInfo
**Snippet:**
```lua
Activity15_MiniGameData = {gameId = 70441019}
local miniGameInfo

function Activity15_MiniGameData.SetMiniGameInfo(info)
  miniGameInfo = info
end

function Activity15_MiniGameData.GetMiniGameInfo()
  return miniGameInfo
end
```

---

## Activty/baseact/Activity15_MiniGameScriptList.lua.lua
**Requires:**
- Activity15_MiniGameData
- Activity15_MiniGameService
**Snippet:**
```lua
require("Activity15_MiniGameData")
require("Activity15_MiniGameService")
```

---

## Activty/baseact/Activity15_MiniGameService.lua.lua
**Functions:**
- Activity15_MiniGameService.MiniGameInfoReq
- Activity15_MiniGameService.MiniGameInfoRsp
- Activity15_MiniGameService.MiniGameSubmitReq
- Activity15_MiniGameService.MiniGameSubmitRsp
- Activity15_MiniGameService.MiniGameGetDailyRewardReq
- Activity15_MiniGameService.MiniGameGetDailyRewardRsp
- Activity15_MiniGameService.ActivityGetGameTopRankReq
- Activity15_MiniGameService.ActivityGetGameTopRankRsp
- Activity15_MiniGameService.Init
**Snippet:**
```lua
Activity15_MiniGameService = {}
local gameId = Activity15_MiniGameData.gameId

function Activity15_MiniGameService.MiniGameInfoReq(rspCallback)
  local info = ActivityDungeonData.GetActivityInfo()
  local activityId = info.baseInfo.activityId
  Net.Send(Proto.MsgName.ActivityGetMiniGameReq, {gameId = gameId, activityId = activityId}, rspCallback)
end

function Activity15_MiniGameService.MiniGameInfoRsp(msg)
```

---

## Activty/baseact/Activity16BossBattleWindow.lua.lua
**Functions:**
- Activity16BossBattleWindow.ReInitData
- Activity16BossBattleWindow.OnInit
- Activity16BossBattleWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity16BossBattleWindow.FormatRemainTime
- Activity16BossBattleWindow.GetChapter
- Activity16BossBattleWindow.InitBtn
- Activity16BossBattleWindow.CloseWindow
- Activity16BossBattleWindow.OnClose
**Requires:**
- ActivityDungeon1016_BossBattleWindowByName
**Snippet:**
```lua
require("ActivityDungeon1016_BossBattleWindowByName")
local Activity16BossBattleWindow = {}
local uis, contentPane, activityInfo

function Activity16BossBattleWindow.ReInitData()
end

function Activity16BossBattleWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity16BossBattleWindow.package, WinResConfig.Activity16BossBattleWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity16BuyLevelDesWindow.lua.lua
**Functions:**
- Activity16BuyLevelDesWindow.ReInitData
- Activity16BuyLevelDesWindow.OnInit
- Activity16BuyLevelDesWindow.ShowAssetsTips
- Activity16BuyLevelDesWindow.UpdateTextDisplay
- Activity16BuyLevelDesWindow.Init
- Activity16BuyLevelDesWindow.GetGold
- Activity16BuyLevelDesWindow.ShowReward
- list.itemRenderer
- Activity16BuyLevelDesWindow.GetRewardItem
- Activity16BuyLevelDesWindow.GetLvData
- Activity16BuyLevelDesWindow.GetRewardLvData
- Activity16BuyLevelDesWindow.GetRewardByPhaseId
- Activity16BuyLevelDesWindow.BuyLevelRsp
- Activity16BuyLevelDesWindow.InitBtn
- waitFun
- Activity16BuyLevelDesWindow.HandleMessage
- Activity16BuyLevelDesWindow.OnShown
- Activity16BuyLevelDesWindow.OnClose
**Requires:**
- ActivityDungeon1016_BuyLevelDesWindowByName
**Snippet:**
```lua
require("ActivityDungeon1016_BuyLevelDesWindowByName")
local Activity16BuyLevelDesWindow = {}
local uis, contentPane, lvData, curLv, buyNum, itemId, lvMax, waitFun, rewardData, itemSort, transPlay, firstPlay, tatalGold, passInfo

function Activity16BuyLevelDesWindow.ReInitData()
end

function Activity16BuyLevelDesWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity16BuyLevelDesWindow.package, WinResConfig.Activity16BuyLevelDesWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity16ChallengeWindow.lua.lua
**Functions:**
- Activity16ChallengeWindow.ReInitData
- Activity16ChallengeWindow.OnInit
- Activity16ChallengeWindow.UpdateInfo
- uis.Main.ChapterList.itemRenderer
- Activity16ChallengeWindow.ShoweStage
- Activity16ChallengeWindow.StageItemClick
- Activity16ChallengeWindow.ShopInfo
- Activity16ChallengeWindow.GetChapterPassById
- Activity16ChallengeWindow.GetCurStage
- Activity16ChallengeWindow.GetFirstChapter
- Activity16ChallengeWindow.GetAllChapterId
- Activity16ChallengeWindow.InitBtn
- Activity16ChallengeWindow.CloseWindow
- Activity16ChallengeWindow.OnShown
- Activity16ChallengeWindow.OnClose
**Requires:**
- ActivityDungeon1016_ChallengeWindowByName
**Snippet:**
```lua
require("ActivityDungeon1016_ChallengeWindowByName")
local Activity16ChallengeWindow = {}
local uis, contentPane, activityInfo, scrollingTween

function Activity16ChallengeWindow.ReInitData()
end

function Activity16ChallengeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity16ChallengeWindow.package, WinResConfig.Activity16ChallengeWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity16DungeonWindow.lua.lua
**Functions:**
- Activity16DungeonWindow.ReInitData
- Activity16DungeonWindow.OnInit
- Activity16DungeonWindow.LoadBg
- Activity16DungeonWindow.InitRedDot
- Activity16DungeonWindow.UpdateInfo
- Activity16DungeonWindow.InitBtnTxt
- Activity16DungeonWindow.InitBtn
- Activity16DungeonWindow.OnShown
- Activity16DungeonWindow.OnClose
- Activity16DungeonWindow.HandleMessage
**Requires:**
- ActivityDungeon1016_ActivityDungeonWindowByName
**Snippet:**
```lua
require("ActivityDungeon1016_ActivityDungeonWindowByName")
local Activity16DungeonWindow = {}
local uis, contentPane, jumpTb, configData, activityInfo, effect
local InitMiniGameInfo = function()
  local data = ActivityDungeonData.GetActivityData()
  if data.id == 70440016 then
    ld("Activity16_MiniGame")
    Activity16_MiniGameService.MiniGameInfoReq(function()
      RedDotMgr.AddNode({
        windowName = WinResConfig.Activity16DungeonWindow.name,
```

---

## Activty/baseact/Activity16MaterialWindow.lua.lua
**Functions:**
- Activity16MaterialWindow.ReInitData
- Activity16MaterialWindow.OnInit
- Activity16MaterialWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity16MaterialWindow.GetChapter
- Activity16MaterialWindow.GetMaxCount
- Activity16MaterialWindow.InitBtn
- Activity16MaterialWindow.CloseWindow
- Activity16MaterialWindow.OnShown
- Activity16MaterialWindow.OnClose
**Requires:**
- ActivityDungeon1016_MaterialWindowByName
**Snippet:**
```lua
require("ActivityDungeon1016_MaterialWindowByName")
local Activity16MaterialWindow = {}
local uis, contentPane, activityInfo, maxCount, posX

function Activity16MaterialWindow.ReInitData()
end

function Activity16MaterialWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity16MaterialWindow.package, WinResConfig.Activity16MaterialWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity16MiniGameMainWindow.lua.lua
**Functions:**
- Activity16MiniGameMainWindow.ReInitData
- Activity16MiniGameMainWindow.OnInit
- Activity16MiniGameMainWindow.UpdateInfo
- Activity16MiniGameMainWindow.InitBtn
- Activity16MiniGameMainWindow.OnClose
- Activity16MiniGameMainWindow.HandleMessage
**Requires:**
- ActivityDungeon1016_MiniGameWindowByName
**Snippet:**
```lua
require("ActivityDungeon1016_MiniGameWindowByName")
local Activity16MiniGameMainWindow = {}
local uis, contentPane
local gameId = 70441020
ld("Activity16_MiniGame")
local RefreshPanelInfo = function()
  local info = Activity16_MiniGameData.GetMiniGameInfo()
  local conf = TableData.GetConfig(gameId, "BaseActivityStageGame")
  local str = conf.game_day_reward[1]
  local splits = Split(str, ":")
```

---

## Activty/baseact/Activity16MiniGameSubmitWindow.lua.lua
**Functions:**
- Activity16MiniGameSubmitWindow.ReInitData
- Activity16MiniGameSubmitWindow.OnInit
- Activity16MiniGameSubmitWindow.UpdateInfo
- Activity16MiniGameSubmitWindow.InitBtn
- Activity16MiniGameSubmitWindow.OnClose
**Requires:**
- ActivityDungeon1016_MiniStart_EndRewardWindowByName
**Snippet:**
```lua
require("ActivityDungeon1016_MiniStart_EndRewardWindowByName")
local Activity16MiniGameSubmitWindow = {}
local uis, contentPane, score

function Activity16MiniGameSubmitWindow.ReInitData()
end

function Activity16MiniGameSubmitWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity16MiniGameSubmitWindow.package, WinResConfig.Activity16MiniGameSubmitWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity16MiniGameTaskWindow.lua.lua
**Functions:**
- RefreshRewardList
- list.itemRenderer
- itemlist.itemRenderer
- Activity16MiniGameTaskWindow.ReInitData
- Activity16MiniGameTaskWindow.OnInit
- Activity16MiniGameTaskWindow.UpdateInfo
- Activity16MiniGameTaskWindow.InitBtn
- Activity16MiniGameTaskWindow.OnClose
**Requires:**
- ActivityDungeon1016_MiniTaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1016_MiniTaskWindowByName")
local Activity16MiniGameTaskWindow = {}
local uis, contentPane
local gameId = 70441020

local function RefreshRewardList()
  local info = Activity16_MiniGameData.GetMiniGameInfo()
  local minigame_tasks = info.taskList
  local list = uis.Main.TipsList
  list:SetVirtual()
```

---

## Activty/baseact/Activity16MiniGameWindow.lua.lua
**Functions:**
- Activity16MiniGameWindow.ReInitData
- Activity16MiniGameWindow.OnInit
- Activity16MiniGameWindow.UpdateInfo
- Activity16MiniGameWindow.InitBtn
- Activity16MiniGameWindow.OnClose
- Activity16MiniGameWindow.HandleMessage
**Requires:**
- ActivityDungeon1016_MiniGameStartWindowByName
- Activity16_MiniGameController
**Snippet:**
```lua
require("ActivityDungeon1016_MiniGameStartWindowByName")
local Activity16MiniGameWindow = {}
local uis, contentPane
local controller = require("Activity16_MiniGameController")
local cellObjs, score, displayScore
local CLEAR_ALL_BLOCKS_SCORE = 300
local SHAKE_MAGNITUDE = 5
local DEFAULT_SHAKE_DURATION = 0.05
local DRAG_OFFSET_Y = 120
local OUTLINE_EFFECT_LOOKUP = {
```

---

## Activty/baseact/Activity16PassportLevelUpTipsWindow.lua.lua
**Functions:**
- Activity16PassportLevelUpTipsWindow.ReInitData
- Activity16PassportLevelUpTipsWindow.OnInit
- Activity16PassportLevelUpTipsWindow.UpdateInfo
- Activity16PassportLevelUpTipsWindow.InitBtn
- Activity16PassportLevelUpTipsWindow.OnClose
**Requires:**
- ActivityDungeon1016_PassportUp_LevelUpTipsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1016_PassportUp_LevelUpTipsWindowByName")
local Activity16PassportLevelUpTipsWindow = {}
local uis, contentPane, lv

function Activity16PassportLevelUpTipsWindow.ReInitData()
end

function Activity16PassportLevelUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity16PassportLevelUpTipsWindow.package, WinResConfig.Activity16PassportLevelUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity16PassportWindow.lua.lua
**Functions:**
- Activity16PassportWindow.ReInitData
- Activity16PassportWindow.OnInit
- Activity16PassportWindow.UpdateTextDisplay
- Activity16PassportWindow.InitPassport
- uis.Main.TabRegion.TabList.itemRenderer
- Activity16PassportWindow.InitEffect
- Activity16PassportWindow.InitLv
- Activity16PassportWindow.ShowLevelUp
- Activity16PassportWindow.SaveLevel
- Activity16PassportWindow.GetRewardByLv
- Activity16PassportWindow.GetRewardNum
- Activity16PassportWindow.IsGetAllReward
- Activity16PassportWindow.ShowReward
- Activity16PassportWindow.GetUpdateLv
- Activity16PassportWindow.RefreshListReward
- Activity16PassportWindow.CheckItemTime
- Activity16PassportWindow.ShowQuitTips
- Activity16PassportWindow.RefreshUI
- Activity16PassportWindow.GetExpMxp
- Activity16PassportWindow.SetLevelInfo
- Activity16PassportWindow.InitList
- list.itemRenderer
- Activity16PassportWindow.SetListPos
- Activity16PassportWindow.RefreshReward
- Activity16PassportWindow.ShowGetEffect
- Activity16PassportWindow.RewardItemClick
- Activity16PassportWindow.IsReward
- Activity16PassportWindow.RefreshRewardFirst
- Activity16PassportWindow.RefreshRewardEnd
- Activity16PassportWindow.ShowState
- Activity16PassportWindow.RefreshRewardShow
- Activity16PassportWindow.RefreshRewardState
- Activity16PassportWindow.PassportActivate
- Activity16PassportWindow.CloseWindow
- Activity16PassportWindow.InitBtn
- Activity16PassportWindow.ShowExpBarAnim
- Activity16PassportWindow.InitTask
- list.itemRenderer
- Activity16PassportWindow.InitClothes
- clothes.BuyReward.RewardList.itemRenderer
- Activity16PassportWindow.SetLastLv
- Activity16PassportWindow.PlayFirstRewardEffect
- Activity16PassportWindow.PlayEndRewardEffect
- Activity16PassportWindow.HandleMessage
- Activity16PassportWindow.OnShown
- Activity16PassportWindow.OnClose
**Requires:**
- ActivityDungeon1016_PassportWindowByName
**Snippet:**
```lua
require("ActivityDungeon1016_PassportWindowByName")
local Activity16PassportWindow = {}
local uis, contentPane, passInfo, lvMax, modelType, expMax, rewardData, rewardType, rewardLv, listPage, passLv, jumpTb, isShowAllGet, passPortConfig, lvTween, lastLv, waitMessageId, newPassPort, animTween

function Activity16PassportWindow.ReInitData()
end

function Activity16PassportWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity16PassportWindow.package, WinResConfig.Activity16PassportWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity16PlotWindow.lua.lua
**Functions:**
- Activity16PlotWindow.ReInitData
- Activity16PlotWindow.OnInit
- Activity16PlotWindow.UpdateInfo
- list.itemRenderer
- Activity16PlotWindow.InitBtn
- Activity16PlotWindow.CloseWindow
- Activity16PlotWindow.OnClose
**Requires:**
- ActivityDungeon1016_PlotWindowByName
**Snippet:**
```lua
require("ActivityDungeon1016_PlotWindowByName")
local Activity16PlotWindow = {}
local uis, contentPane, configData

function Activity16PlotWindow.ReInitData()
end

function Activity16PlotWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity16PlotWindow.package, WinResConfig.Activity16PlotWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity16ShopWindow.lua.lua
**Functions:**
- Activity16ShopWindow.ReInitData
- Activity16ShopWindow.OnInit
- Activity16ShopWindow.UpdateInfo
- uis.Main.ItemList.itemRenderer
- Activity16ShopWindow.ShowItem
- list.itemRenderer
- Activity16ShopWindow.ShowOneReward
- list.itemRenderer
- Activity16ShopWindow.GetShopGrid
- Activity16ShopWindow.InitBtn
- Activity16ShopWindow.CloseWindow
- Activity16ShopWindow.OnClose
- Activity16ShopWindow.HandleMessage
**Requires:**
- ActivityDungeon1016_ShopWindowByName
**Snippet:**
```lua
require("ActivityDungeon1016_ShopWindowByName")
local Activity16ShopWindow = {}
local uis, contentPane, activityInfo, tempAssetsTips

function Activity16ShopWindow.ReInitData()
end

function Activity16ShopWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity16ShopWindow.package, WinResConfig.Activity16ShopWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity16SignWindow.lua.lua
**Functions:**
- Activity16SignWindow.ReInitData
- Activity16SignWindow.OnInit
- Activity16SignWindow.UpdateInfo
- list.RewardList.itemRenderer
- Activity16SignWindow.ShowAllItemFrame
- Activity16SignWindow.GetRewardData
- Activity16SignWindow.InitBtn
- Activity16SignWindow.CloseWindow
- Activity16SignWindow.OnClose
**Requires:**
- ActivityDungeon1016_SignWindowByName
**Snippet:**
```lua
require("ActivityDungeon1016_SignWindowByName")
local Activity16SignWindow = {}
local uis, contentPane, activityInfo

function Activity16SignWindow.ReInitData()
end

function Activity16SignWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity16SignWindow.package, WinResConfig.Activity16SignWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity16TaskWindow.lua.lua
**Functions:**
- Activity16TaskWindow.ReInitData
- Activity16TaskWindow.OnInit
- Activity16TaskWindow.UpdateInfo
- list.itemRenderer
- rewardList.itemRenderer
- Activity16TaskWindow.GetRewardNum
- Activity16TaskWindow.ShowAllItemFrame
- Activity16TaskWindow.SortTask
- Activity16TaskWindow.InitBtn
- Activity16TaskWindow.CloseWindow
- Activity16TaskWindow.OnClose
**Requires:**
- ActivityDungeon1016_TaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1016_TaskWindowByName")
local Activity16TaskWindow = {}
local uis, contentPane

function Activity16TaskWindow.ReInitData()
end

function Activity16TaskWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity16TaskWindow.package, WinResConfig.Activity16TaskWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity16_MiniGameConfigs.lua.lua
**Snippet:**
```lua
return {
  [1] = {
    cells = {
      {x = 1, y = 1},
      {x = 2, y = 1},
      {x = 1, y = 2},
      {x = 2, y = 2}
    },
    anchor = 1,
    score = 0
```

---

## Activty/baseact/Activity16_MiniGameController.lua.lua
**Requires:**
- Activity16_MiniGameConfigs
**Snippet:**
```lua
local GRID_WIDTH, GRID_HEIGHT = 1, 1
local NUM_PREVIEW_TYPES = 3
local COMBO_PLACE_INTERVAL = 3
local MAX_COMBO = 5
local CLEAR_ALL_BLOCKS_SCORE = 300
local ACTIVITY16_MINIGAME_CONFIGS = require("Activity16_MiniGameConfigs")
local worldCenter, gridColumns, gridRows, grids, currentTetromino, tetrominos, dropTimer, previewEntries, elapse, combo, remainComboChance, score, __oncreatetetromino, __ondestroycell, __ongameover, __onmatched, __oncreatepreviewentry
local rotatePointAround = function(x, y, angle, aroundx, aroundy)
  local deg = math.rad(angle)
  local cos, sin = math.cos(deg), math.sin(deg)
```

---

## Activty/baseact/Activity16_MiniGameData.lua.lua
**Snippet:**
```lua
local miniGameInfo
local SetMiniGameInfo = function(info)
  miniGameInfo = info
end
local GetMiniGameInfo = function()
  return miniGameInfo
end
return {SetMiniGameInfo = SetMiniGameInfo, GetMiniGameInfo = GetMiniGameInfo}
```

---

## Activty/baseact/Activity16_MiniGameScriptList.lua.lua
**Requires:**
- Activity16_MiniGameData
- Activity16_MiniGameService
**Snippet:**
```lua
Activity16_MiniGameData = require("Activity16_MiniGameData")
Activity16_MiniGameService = require("Activity16_MiniGameService")
```

---

## Activty/baseact/Activity16_MiniGameService.lua.lua
**Snippet:**
```lua
local gameId = 70441020
local MiniGameInfoReq = function(rspCallback)
  local info = ActivityDungeonData.GetActivityInfo()
  local activityId = info.baseInfo.activityId
  Net.Send(Proto.MsgName.ActivityGetMiniGameReq, {gameId = gameId, activityId = activityId}, rspCallback)
end
local MiniGameInfoRsp = function(msg)
  Activity16_MiniGameData.SetMiniGameInfo(msg)
  UIMgr:SendWindowMessage(WinResConfig.Activity16MiniGameMainWindow.name, WindowMsgEnum.Activity16_MiniGame.REFRESH_MINIGAME_INFO)
  RedDotMgr.UpdateNode(RED_DOT_DATA_TYPE.ACTIVITY_DUNGENON)
```

---

## Activty/baseact/Activity17BossBattleWindow.lua.lua
**Functions:**
- Activity17BossBattleWindow.ReInitData
- Activity17BossBattleWindow.OnInit
- Activity17BossBattleWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity17BossBattleWindow.FormatRemainTime
- Activity17BossBattleWindow.GetChapter
- Activity17BossBattleWindow.InitBtn
- Activity17BossBattleWindow.CloseWindow
- Activity17BossBattleWindow.OnClose
**Requires:**
- ActivityDungeon1017_BossBattleWindowByName
**Snippet:**
```lua
require("ActivityDungeon1017_BossBattleWindowByName")
local Activity17BossBattleWindow = {}
local uis, contentPane, activityInfo

function Activity17BossBattleWindow.ReInitData()
end

function Activity17BossBattleWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity17BossBattleWindow.package, WinResConfig.Activity17BossBattleWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity17BuyLevelDesWindow.lua.lua
**Functions:**
- Activity17BuyLevelDesWindow.ReInitData
- Activity17BuyLevelDesWindow.OnInit
- Activity17BuyLevelDesWindow.ShowAssetsTips
- Activity17BuyLevelDesWindow.UpdateTextDisplay
- Activity17BuyLevelDesWindow.Init
- Activity17BuyLevelDesWindow.GetGold
- Activity17BuyLevelDesWindow.ShowReward
- list.itemRenderer
- Activity17BuyLevelDesWindow.GetRewardItem
- Activity17BuyLevelDesWindow.GetLvData
- Activity17BuyLevelDesWindow.GetRewardLvData
- Activity17BuyLevelDesWindow.GetRewardByPhaseId
- Activity17BuyLevelDesWindow.BuyLevelRsp
- Activity17BuyLevelDesWindow.InitBtn
- waitFun
- Activity17BuyLevelDesWindow.HandleMessage
- Activity17BuyLevelDesWindow.OnShown
- Activity17BuyLevelDesWindow.OnClose
**Requires:**
- ActivityDungeon1017_BuyLevelDesWindowByName
**Snippet:**
```lua
require("ActivityDungeon1017_BuyLevelDesWindowByName")
local Activity17BuyLevelDesWindow = {}
local uis, contentPane, lvData, curLv, buyNum, itemId, lvMax, waitFun, rewardData, itemSort, transPlay, firstPlay, tatalGold, passInfo

function Activity17BuyLevelDesWindow.ReInitData()
end

function Activity17BuyLevelDesWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity17BuyLevelDesWindow.package, WinResConfig.Activity17BuyLevelDesWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity17ChallengeWindow.lua.lua
**Functions:**
- Activity17ChallengeWindow.ReInitData
- Activity17ChallengeWindow.OnInit
- Activity17ChallengeWindow.UpdateInfo
- uis.Main.ChapterList.itemRenderer
- Activity17ChallengeWindow.ShoweStage
- Activity17ChallengeWindow.StageItemClick
- Activity17ChallengeWindow.ShopInfo
- Activity17ChallengeWindow.GetChapterPassById
- Activity17ChallengeWindow.GetCurStage
- Activity17ChallengeWindow.GetFirstChapter
- Activity17ChallengeWindow.GetAllChapterId
- Activity17ChallengeWindow.InitBtn
- Activity17ChallengeWindow.CloseWindow
- Activity17ChallengeWindow.OnShown
- Activity17ChallengeWindow.OnClose
**Requires:**
- ActivityDungeon1017_ChallengeWindowByName
**Snippet:**
```lua
require("ActivityDungeon1017_ChallengeWindowByName")
local Activity17ChallengeWindow = {}
local uis, contentPane, activityInfo, scrollingTween

function Activity17ChallengeWindow.ReInitData()
end

function Activity17ChallengeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity17ChallengeWindow.package, WinResConfig.Activity17ChallengeWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity17DodgerGameMainWindow.lua.lua
**Functions:**
- RefreshPanelInfo
- Activity17DodgerGameMainWindow.ReInitData
- Activity17DodgerGameMainWindow.OnInit
- Activity17DodgerGameMainWindow.UpdateInfo
- Activity17DodgerGameMainWindow.InitBtn
- Activity17DodgerGameMainWindow.OnClose
- Activity17DodgerGameMainWindow.HandleMessage
**Requires:**
- ActivityDungeon1017_MiniGameWindowByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniGameWindowByName")
local Activity17DodgerGameMainWindow = {}
local uis, contentPane
ld("Activity17_MiniGame")
local gameId = 70441021

local function RefreshPanelInfo()
  local info = Activity17_MiniGameData.GetMiniGameInfo(gameId)
  local conf = TableData.GetConfig(gameId, "BaseActivityStageGame")
  local str = conf.game_day_reward[1]
```

---

## Activty/baseact/Activity17DodgerGameSettingsWindow.lua.lua
**Functions:**
- Activity17DodgerGameSettingsWindow.ReInitData
- Activity17DodgerGameSettingsWindow.OnInit
- Activity17DodgerGameSettingsWindow.UpdateInfo
- list.itemRenderer
- Activity17DodgerGameSettingsWindow.InitBtn
- Activity17DodgerGameSettingsWindow.OnClose
**Requires:**
- ActivityDungeon1017_MiniOperateChoiceWindowByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniOperateChoiceWindowByName")
local Activity17DodgerGameSettingsWindow = {}
local uis, contentPane

function Activity17DodgerGameSettingsWindow.ReInitData()
end

function Activity17DodgerGameSettingsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity17DodgerGameSettingsWindow.package, WinResConfig.Activity17DodgerGameSettingsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity17DodgerGameSubmitWindow.lua.lua
**Functions:**
- Activity17DodgerGameSubmitWindow.ReInitData
- Activity17DodgerGameSubmitWindow.OnInit
- Activity17DodgerGameSubmitWindow.UpdateInfo
- Activity17DodgerGameSubmitWindow.InitBtn
- Activity17DodgerGameSubmitWindow.OnClose
**Requires:**
- ActivityDungeon1017_MiniStart_EndRewardWindowByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniStart_EndRewardWindowByName")
local Activity17DodgerGameSubmitWindow = {}
local uis, contentPane, score

function Activity17DodgerGameSubmitWindow.ReInitData()
end

function Activity17DodgerGameSubmitWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity17DodgerGameSubmitWindow.package, WinResConfig.Activity17DodgerGameSubmitWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity17DodgerGameTaskWindow.lua.lua
**Functions:**
- RefreshRewardList
- list.itemRenderer
- itemlist.itemRenderer
- Activity17DodgerGameTaskWindow.ReInitData
- Activity17DodgerGameTaskWindow.OnInit
- Activity17DodgerGameTaskWindow.UpdateInfo
- Activity17DodgerGameTaskWindow.InitBtn
- Activity17DodgerGameTaskWindow.OnClose
**Requires:**
- ActivityDungeon1017_MiniTaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniTaskWindowByName")
local Activity17DodgerGameTaskWindow = {}
local uis, contentPane
local gameId = 70441021

local function RefreshRewardList()
  local info = Activity17_MiniGameData.GetMiniGameInfo(gameId)
  local minigame_tasks = info.taskList
  local list = uis.Main.TipsList
  list:SetVirtual()
```

---

## Activty/baseact/Activity17DodgerGameWindow.lua.lua
**Functions:**
- Activity17DodgerGameWindow.ReInitData
- Activity17DodgerGameWindow.OnInit
- Activity17DodgerGameWindow.UpdateInfo
- Activity17DodgerGameWindow.InitBtn
- Activity17DodgerGameWindow.OnClose
- Activity17DodgerGameWindow.HandleMessage
**Requires:**
- ActivityDungeon1017_MiniGameStartWindowByName
- Activity17_DodgerGameController
**Snippet:**
```lua
require("ActivityDungeon1017_MiniGameStartWindowByName")
local Activity17DodgerGameWindow = {}
local uis, contentPane
local PLAYER_TWINKLE_DURATION = 0.333
local PLAYER_TWINKLE_COUNT = 9
local JOYSTICK_RADIUS = 240
local gameId = 70441021
local controller = require("Activity17_DodgerGameController")
local joystick, playerObj, objLookup, playerTwinkleDuration, playerTwinkleCount, twinkleColor, pause
local Screen2WorldPosition = function(screenPosition)
```

---

## Activty/baseact/Activity17DungeonWindow.lua.lua
**Functions:**
- Activity17DungeonWindow.ReInitData
- Activity17DungeonWindow.OnInit
- Activity17DungeonWindow.LoadBg
- Activity17DungeonWindow.InitRedDot
- Activity17DungeonWindow.UpdateInfo
- Activity17DungeonWindow.InitBtnTxt
- Activity17DungeonWindow.InitBtn
- Activity17DungeonWindow.OnShown
- Activity17DungeonWindow.OnHide
- Activity17DungeonWindow.OnClose
- Activity17DungeonWindow.HandleMessage
**Requires:**
- ActivityDungeon1017_ActivityDungeonWindowByName
**Snippet:**
```lua
require("ActivityDungeon1017_ActivityDungeonWindowByName")
local Activity17DungeonWindow = {}
local uis, contentPane, jumpTb, configData, activityInfo, effect
local gameId = 70441021
local eventTipsRoot, cursors, cursorRoot
local GetEventControllerIndex = function(etype, esubtype)
  local ctrlname, ctrlIndex = "c1", 0
  if etype == AbyssExploreEventID.ACTIVITY_BOSS then
    ctrlIndex = 3
  elseif etype == AbyssExploreEventID.ACTIVITY_STAGE then
```

---

## Activty/baseact/Activity17EntranceAnimWindow.lua.lua
**Functions:**
- FindChild
- PlayDailyEntranceAnim
- Activity17EntranceAnimWindow.ReInitData
- Activity17EntranceAnimWindow.OnInit
- Activity17EntranceAnimWindow.UpdateInfo
- Activity17EntranceAnimWindow.InitBtn
- Activity17EntranceAnimWindow.OnClose
**Requires:**
- ActivityDungeon1017_MainSeasonsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1017_MainSeasonsWindowByName")
local Activity17EntranceAnimWindow = {}
local uis, contentPane, touchable
local setSpritesColor = function(go, color, fadeout)
  local spriteRenderers = go:GetComponentsInChildren(typeof(CS.UnityEngine.SpriteRenderer))
  if spriteRenderers then
    for i = 0, spriteRenderers.Length - 1 do
      local sr = spriteRenderers[i]
      if fadeout then
        color.a = math.min(color.a, sr.color.a)
```

---

## Activty/baseact/Activity17MaterialWindow.lua.lua
**Functions:**
- Activity17MaterialWindow.ReInitData
- Activity17MaterialWindow.OnInit
- Activity17MaterialWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity17MaterialWindow.GetChapter
- Activity17MaterialWindow.GetMaxCount
- Activity17MaterialWindow.InitBtn
- Activity17MaterialWindow.CloseWindow
- Activity17MaterialWindow.OnShown
- Activity17MaterialWindow.OnClose
**Requires:**
- ActivityDungeon1017_MaterialWindowByName
**Snippet:**
```lua
require("ActivityDungeon1017_MaterialWindowByName")
local Activity17MaterialWindow = {}
local uis, contentPane, activityInfo, maxCount, posX

function Activity17MaterialWindow.ReInitData()
end

function Activity17MaterialWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity17MaterialWindow.package, WinResConfig.Activity17MaterialWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity17MiniGame2MainWindow.lua.lua
**Functions:**
- Activity17MiniGame2MainWindow.ReInitData
- Activity17MiniGame2MainWindow.OnInit
- Activity17MiniGame2MainWindow.UpdateInfo
- Activity17MiniGame2MainWindow.InitBtn
- Activity17MiniGame2MainWindow.TouchTask
- Activity17MiniGame2MainWindow.TouchStart
- Activity17MiniGame2MainWindow.TouchClose
- Activity17MiniGame2MainWindow.OnClose
- Activity17MiniGame2MainWindow.HandleMessage
**Requires:**
- ActivityDungeon1017_MiniGame2WindowByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniGame2WindowByName")
local Activity17MiniGame2MainWindow = {}
local uis, contentPane
local RefreshPanelInfo = function()
  local gameId = 70441022
  local info = Activity17_MiniGameData.GetMiniGameInfo(gameId)
  local conf = TableData.GetConfig(gameId, "BaseActivityStageGame")
  local str = conf.game_day_reward[1]
  local splits = Split(str, ":")
  local itemType, itemId, count = tonumber(splits[1]), tonumber(splits[2]), tonumber(splits[3])
```

---

## Activty/baseact/Activity17MiniGameChoice2Window.lua.lua
**Functions:**
- list.itemRenderer
- Activity17MiniGameChoice2Window.UpdateCardHead
- headList.itemRenderer
- Activity17MiniGameChoice2Window.ReInitData
- Activity17MiniGameChoice2Window.OnInit
- Activity17MiniGameChoice2Window.UpdateInfo
- Activity17MiniGameChoice2Window.InitBtn
- Activity17MiniGameChoice2Window.TouchClose
- Activity17MiniGameChoice2Window.OnClose
- Activity17MiniGameChoice2Window.HandleMessage
**Requires:**
- ActivityDungeon1017_MiniGameChoice2WindowByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniGameChoice2WindowByName")
local Activity17MiniGameChoice2Window = {}
local uis, contentPane, selectCardId
local gameId = 70441022
local GetStageUnlockStamp = function(stageId)
  local stageConfig = TableData.GetConfig(stageId, "BaseShootStage")
  local activityInfo = ActivityDungeonData.GetActivityInfo()
  local startStamp = activityInfo.baseInfo.startStamp
  local startHour = tonumber(TimeUtil.FormatDate("%H", startStamp))
  local unlockStamp = startStamp - (startHour - 5) * 3600 + stageConfig.unlock_day * 3600 * 24
```

---

## Activty/baseact/Activity17MiniGameChoice2_InfoSkillWindow.lua.lua
**Functions:**
- Activity17MiniGameChoice2_InfoSkillWindow.ReInitData
- Activity17MiniGameChoice2_InfoSkillWindow.OnInit
- Activity17MiniGameChoice2_InfoSkillWindow.UpdateInfo
- list.itemRenderer
- extList.itemRenderer
- Activity17MiniGameChoice2_InfoSkillWindow.InitBtn
- Activity17MiniGameChoice2_InfoSkillWindow.TouchClose
- Activity17MiniGameChoice2_InfoSkillWindow.OnClose
**Requires:**
- ActivityDungeon1017_MiniGameChoice2_InfoSkillWindowByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniGameChoice2_InfoSkillWindowByName")
local Activity17MiniGameChoice2_InfoSkillWindow = {}
local uis, contentPane, cardId, stageId

function Activity17MiniGameChoice2_InfoSkillWindow.ReInitData()
end

function Activity17MiniGameChoice2_InfoSkillWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity17MiniGameChoice2_InfoSkillWindow.package, WinResConfig.Activity17MiniGameChoice2_InfoSkillWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity17MiniTask2Window.lua.lua
**Functions:**
- RefreshRewardList
- list.itemRenderer
- itemlist.itemRenderer
- Activity17MiniTask2Window.ReInitData
- Activity17MiniTask2Window.OnInit
- Activity17MiniTask2Window.UpdateInfo
- Activity17MiniTask2Window.InitBtn
- Activity17MiniTask2Window.OnClose
**Requires:**
- ActivityDungeon1017_MiniTask2WindowByName
**Snippet:**
```lua
require("ActivityDungeon1017_MiniTask2WindowByName")
local Activity17MiniTask2Window = {}
local uis, contentPane

local function RefreshRewardList()
  local gameId = 70441022
  local info = Activity17_MiniGameData.GetMiniGameInfo(gameId)
  local minigame_tasks = info.taskList
  local list = uis.Main.TipsList
  list:SetVirtual()
```

---

## Activty/baseact/Activity17PassportLevelUpTipsWindow.lua.lua
**Functions:**
- Activity17PassportLevelUpTipsWindow.ReInitData
- Activity17PassportLevelUpTipsWindow.OnInit
- Activity17PassportLevelUpTipsWindow.UpdateInfo
- Activity17PassportLevelUpTipsWindow.InitBtn
- Activity17PassportLevelUpTipsWindow.OnClose
**Requires:**
- ActivityDungeon1017_PassportUp_LevelUpTipsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1017_PassportUp_LevelUpTipsWindowByName")
local Activity17PassportLevelUpTipsWindow = {}
local uis, contentPane, lv

function Activity17PassportLevelUpTipsWindow.ReInitData()
end

function Activity17PassportLevelUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity17PassportLevelUpTipsWindow.package, WinResConfig.Activity17PassportLevelUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity17PassportWindow.lua.lua
**Functions:**
- Activity17PassportWindow.ReInitData
- Activity17PassportWindow.OnInit
- Activity17PassportWindow.UpdateTextDisplay
- Activity17PassportWindow.InitPassport
- uis.Main.TabRegion.TabList.itemRenderer
- Activity17PassportWindow.InitEffect
- Activity17PassportWindow.InitLv
- Activity17PassportWindow.ShowLevelUp
- Activity17PassportWindow.SaveLevel
- Activity17PassportWindow.GetRewardByLv
- Activity17PassportWindow.GetRewardNum
- Activity17PassportWindow.IsGetAllReward
- Activity17PassportWindow.ShowReward
- Activity17PassportWindow.GetUpdateLv
- Activity17PassportWindow.RefreshListReward
- Activity17PassportWindow.CheckItemTime
- Activity17PassportWindow.ShowQuitTips
- Activity17PassportWindow.RefreshUI
- Activity17PassportWindow.GetExpMxp
- Activity17PassportWindow.SetLevelInfo
- Activity17PassportWindow.InitList
- list.itemRenderer
- Activity17PassportWindow.SetListPos
- Activity17PassportWindow.RefreshReward
- Activity17PassportWindow.ShowGetEffect
- Activity17PassportWindow.RewardItemClick
- Activity17PassportWindow.IsReward
- Activity17PassportWindow.RefreshRewardFirst
- Activity17PassportWindow.RefreshRewardEnd
- Activity17PassportWindow.ShowState
- Activity17PassportWindow.RefreshRewardShow
- Activity17PassportWindow.RefreshRewardState
- Activity17PassportWindow.PassportActivate
- Activity17PassportWindow.CloseWindow
- Activity17PassportWindow.InitBtn
- Activity17PassportWindow.ShowExpBarAnim
- Activity17PassportWindow.InitTask
- list.itemRenderer
- Activity17PassportWindow.InitClothes
- clothes.BuyReward.RewardList.itemRenderer
- Activity17PassportWindow.SetLastLv
- Activity17PassportWindow.PlayFirstRewardEffect
- Activity17PassportWindow.PlayEndRewardEffect
- Activity17PassportWindow.HandleMessage
- Activity17PassportWindow.OnShown
- Activity17PassportWindow.OnClose
**Requires:**
- ActivityDungeon1017_PassportWindowByName
**Snippet:**
```lua
require("ActivityDungeon1017_PassportWindowByName")
local Activity17PassportWindow = {}
local uis, contentPane, passInfo, lvMax, modelType, expMax, rewardData, rewardType, rewardLv, listPage, passLv, jumpTb, isShowAllGet, passPortConfig, lvTween, lastLv, waitMessageId, newPassPort, animTween

function Activity17PassportWindow.ReInitData()
end

function Activity17PassportWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity17PassportWindow.package, WinResConfig.Activity17PassportWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity17PlotWindow.lua.lua
**Functions:**
- Activity17PlotWindow.ReInitData
- Activity17PlotWindow.OnInit
- Activity17PlotWindow.UpdateInfo
- list.itemRenderer
- Activity17PlotWindow.InitBtn
- Activity17PlotWindow.CloseWindow
- Activity17PlotWindow.OnClose
**Requires:**
- ActivityDungeon1017_PlotWindowByName
**Snippet:**
```lua
require("ActivityDungeon1017_PlotWindowByName")
local Activity17PlotWindow = {}
local uis, contentPane, configData

function Activity17PlotWindow.ReInitData()
end

function Activity17PlotWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity17PlotWindow.package, WinResConfig.Activity17PlotWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity17ShopWindow.lua.lua
**Functions:**
- Activity17ShopWindow.ReInitData
- Activity17ShopWindow.OnInit
- Activity17ShopWindow.UpdateInfo
- uis.Main.ItemList.itemRenderer
- Activity17ShopWindow.ShowItem
- list.itemRenderer
- Activity17ShopWindow.ShowOneReward
- list.itemRenderer
- Activity17ShopWindow.GetShopGrid
- Activity17ShopWindow.InitBtn
- Activity17ShopWindow.CloseWindow
- Activity17ShopWindow.OnClose
- Activity17ShopWindow.HandleMessage
**Requires:**
- ActivityDungeon1017_ShopWindowByName
**Snippet:**
```lua
require("ActivityDungeon1017_ShopWindowByName")
local Activity17ShopWindow = {}
local uis, contentPane, activityInfo, tempAssetsTips

function Activity17ShopWindow.ReInitData()
end

function Activity17ShopWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity17ShopWindow.package, WinResConfig.Activity17ShopWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity17SignWindow.lua.lua
**Functions:**
- Activity17SignWindow.ReInitData
- Activity17SignWindow.OnInit
- Activity17SignWindow.UpdateInfo
- list.RewardList.itemRenderer
- Activity17SignWindow.ShowAllItemFrame
- Activity17SignWindow.GetRewardData
- Activity17SignWindow.InitBtn
- Activity17SignWindow.CloseWindow
- Activity17SignWindow.OnClose
**Requires:**
- ActivityDungeon1017_SignWindowByName
**Snippet:**
```lua
require("ActivityDungeon1017_SignWindowByName")
local Activity17SignWindow = {}
local uis, contentPane, activityInfo

function Activity17SignWindow.ReInitData()
end

function Activity17SignWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity17SignWindow.package, WinResConfig.Activity17SignWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity17TaskWindow.lua.lua
**Functions:**
- Activity17TaskWindow.ReInitData
- Activity17TaskWindow.OnInit
- Activity17TaskWindow.UpdateInfo
- list.itemRenderer
- rewardList.itemRenderer
- Activity17TaskWindow.GetRewardNum
- Activity17TaskWindow.ShowAllItemFrame
- Activity17TaskWindow.SortTask
- Activity17TaskWindow.InitBtn
- Activity17TaskWindow.CloseWindow
- Activity17TaskWindow.OnClose
**Requires:**
- ActivityDungeon1017_TaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1017_TaskWindowByName")
local Activity17TaskWindow = {}
local uis, contentPane

function Activity17TaskWindow.ReInitData()
end

function Activity17TaskWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity17TaskWindow.package, WinResConfig.Activity17TaskWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity17_DodgerGameController.lua.lua
**Functions:**
- OnCollision
**Snippet:**
```lua
local BULLET_RADIUS = 0.125
local PLAYER_RADIUS = 0.05
local HORIZONTAL_POSITIONS_GRANULARITY, VERTICAL_POSITIONS_GRANULARITY = 50, 50
local DEFAULT_HP = 3
local DEFAULT_SPEED = 5
local INVINCIBLE_DURATION = 3
local DELAY_SPAWN_BULLET = 2
local PHASE_CONFIG = {
  [1] = {
    time = 0,
```

---

## Activty/baseact/Activity17_MiniGameData.lua.lua
**Snippet:**
```lua
local miniGameInfoDict
local SetMiniGameInfo = function(info)
  miniGameInfoDict = miniGameInfoDict or {}
  miniGameInfoDict[info.gameId] = info
end
local GetMiniGameInfo = function(gameId)
  if miniGameInfoDict then
    return miniGameInfoDict[gameId]
  end
end
```

---

## Activty/baseact/Activity17_MiniGameScriptList.lua.lua
**Requires:**
- Activity17_MiniGameData
- Activity17_MiniGameService
**Snippet:**
```lua
Activity17_MiniGameData = require("Activity17_MiniGameData")
Activity17_MiniGameService = require("Activity17_MiniGameService")
```

---

## Activty/baseact/Activity17_MiniGameService.lua.lua
**Snippet:**
```lua
local cachedGameId
local MiniGameInfoReq = function(gameId, rspCallback)
  local info = ActivityDungeonData.GetActivityInfo()
  local activityId = info.baseInfo.activityId
  Net.Send(Proto.MsgName.ActivityGetMiniGameReq, {activityId = activityId, gameId = gameId}, rspCallback)
end
local MiniGameInfoRsp = function(msg)
  Activity17_MiniGameData.SetMiniGameInfo(msg)
  UIMgr:SendWindowMessage(WinResConfig.Activity17DodgerGameMainWindow.name, WindowMsgEnum.Activity17_MiniGame.REFRESH_MINIGAME_INFO)
  UIMgr:SendWindowMessage(WinResConfig.Activity17DodgerGameWindow.name, WindowMsgEnum.Activity17_MiniGame.REFRESH_MINIGAME_INFO)
```

---

## Activty/baseact/Activity18BossBattleWindow.lua.lua
**Functions:**
- Activity18BossBattleWindow.ReInitData
- Activity18BossBattleWindow.OnInit
- Activity18BossBattleWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity18BossBattleWindow.FormatRemainTime
- Activity18BossBattleWindow.GetChapter
- Activity18BossBattleWindow.InitBtn
- Activity18BossBattleWindow.CloseWindow
- Activity18BossBattleWindow.OnClose
**Requires:**
- ActivityDungeon1018_BossBattleWindowByName
**Snippet:**
```lua
require("ActivityDungeon1018_BossBattleWindowByName")
local Activity18BossBattleWindow = {}
local uis, contentPane, activityInfo

function Activity18BossBattleWindow.ReInitData()
end

function Activity18BossBattleWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity18BossBattleWindow.package, WinResConfig.Activity18BossBattleWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity18BuyLevelDesWindow.lua.lua
**Functions:**
- Activity18BuyLevelDesWindow.ReInitData
- Activity18BuyLevelDesWindow.OnInit
- Activity18BuyLevelDesWindow.ShowAssetsTips
- Activity18BuyLevelDesWindow.UpdateTextDisplay
- Activity18BuyLevelDesWindow.Init
- Activity18BuyLevelDesWindow.GetGold
- Activity18BuyLevelDesWindow.ShowReward
- list.itemRenderer
- Activity18BuyLevelDesWindow.GetRewardItem
- Activity18BuyLevelDesWindow.GetLvData
- Activity18BuyLevelDesWindow.GetRewardLvData
- Activity18BuyLevelDesWindow.GetRewardByPhaseId
- Activity18BuyLevelDesWindow.BuyLevelRsp
- Activity18BuyLevelDesWindow.InitBtn
- waitFun
- Activity18BuyLevelDesWindow.HandleMessage
- Activity18BuyLevelDesWindow.OnShown
- Activity18BuyLevelDesWindow.OnClose
**Requires:**
- ActivityDungeon1018_BuyLevelDesWindowByName
**Snippet:**
```lua
require("ActivityDungeon1018_BuyLevelDesWindowByName")
local Activity18BuyLevelDesWindow = {}
local uis, contentPane, lvData, curLv, buyNum, itemId, lvMax, waitFun, rewardData, itemSort, transPlay, firstPlay, tatalGold, passInfo

function Activity18BuyLevelDesWindow.ReInitData()
end

function Activity18BuyLevelDesWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity18BuyLevelDesWindow.package, WinResConfig.Activity18BuyLevelDesWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity18ChallengeWindow.lua.lua
**Functions:**
- Activity18ChallengeWindow.ReInitData
- Activity18ChallengeWindow.OnInit
- Activity18ChallengeWindow.UpdateInfo
- uis.Main.ChapterList.itemRenderer
- Activity18ChallengeWindow.ShoweStage
- Activity18ChallengeWindow.StageItemClick
- Activity18ChallengeWindow.ShopInfo
- Activity18ChallengeWindow.GetChapterPassById
- Activity18ChallengeWindow.GetCurStage
- Activity18ChallengeWindow.GetFirstChapter
- Activity18ChallengeWindow.GetAllChapterId
- Activity18ChallengeWindow.InitBtn
- Activity18ChallengeWindow.CloseWindow
- Activity18ChallengeWindow.OnShown
- Activity18ChallengeWindow.OnClose
**Requires:**
- ActivityDungeon1018_ChallengeWindowByName
**Snippet:**
```lua
require("ActivityDungeon1018_ChallengeWindowByName")
local Activity18ChallengeWindow = {}
local uis, contentPane, activityInfo, scrollingTween

function Activity18ChallengeWindow.ReInitData()
end

function Activity18ChallengeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity18ChallengeWindow.package, WinResConfig.Activity18ChallengeWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity18DungeonWindow.lua.lua
**Functions:**
- Activity18DungeonWindow.ReInitData
- Activity18DungeonWindow.OnInit
- Activity18DungeonWindow.LoadBg
- Activity18DungeonWindow.InitRedDot
- Activity18DungeonWindow.UpdateInfo
- Activity18DungeonWindow.InitBtnTxt
- Activity18DungeonWindow.InitBtn
- Activity18DungeonWindow.OnShown
- Activity18DungeonWindow.OnClose
- Activity18DungeonWindow.HandleMessage
**Requires:**
- ActivityDungeon1018_ActivityDungeonWindowByName
**Snippet:**
```lua
require("ActivityDungeon1018_ActivityDungeonWindowByName")
local Activity18DungeonWindow = {}
local uis, contentPane, jumpTb, configData, activityInfo, effect
local InitMiniGameInfo = function()
  local data = ActivityDungeonData.GetActivityData()
  if data.id == 70440018 then
    ld("Activity18_MiniGame")
    Activity18_MiniGameService.MiniGameInfoReq(function()
      RedDotMgr.AddNode({
        windowName = WinResConfig.Activity18DungeonWindow.name,
```

---

## Activty/baseact/Activity18MaterialWindow.lua.lua
**Functions:**
- Activity18MaterialWindow.ReInitData
- Activity18MaterialWindow.OnInit
- Activity18MaterialWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity18MaterialWindow.GetChapter
- Activity18MaterialWindow.GetMaxCount
- Activity18MaterialWindow.InitBtn
- Activity18MaterialWindow.CloseWindow
- Activity18MaterialWindow.OnShown
- Activity18MaterialWindow.OnClose
**Requires:**
- ActivityDungeon1018_MaterialWindowByName
**Snippet:**
```lua
require("ActivityDungeon1018_MaterialWindowByName")
local Activity18MaterialWindow = {}
local uis, contentPane, activityInfo, maxCount, posX

function Activity18MaterialWindow.ReInitData()
end

function Activity18MaterialWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity18MaterialWindow.package, WinResConfig.Activity18MaterialWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity18MiniGameMainWindow.lua.lua
**Functions:**
- RefreshPanelInfo
- Activity18MiniGameMainWindow.ReInitData
- Activity18MiniGameMainWindow.OnInit
- Activity18MiniGameMainWindow.UpdateInfo
- Activity18MiniGameMainWindow.InitBtn
- Activity18MiniGameMainWindow.OnClose
- Activity18MiniGameMainWindow.HandleMessage
**Requires:**
- ActivityDungeon1018_MiniGameWindowByName
**Snippet:**
```lua
require("ActivityDungeon1018_MiniGameWindowByName")
ld("Activity18_MiniGame")
local Activity18MiniGameMainWindow = {}
local uis, contentPane

local function RefreshPanelInfo()
  local info = Activity18_MiniGameData.GetMiniGameInfo()
  local conf = TableData.GetConfig(Activity18_MiniGameData.gameId, "BaseActivityStageGame")
  local str = conf.game_day_reward[1]
  local splits = Split(str, ":")
```

---

## Activty/baseact/Activity18MiniGameSubmitWindow.lua.lua
**Functions:**
- Activity18MiniGameSubmitWindow.ReInitData
- Activity18MiniGameSubmitWindow.OnInit
- Activity18MiniGameSubmitWindow.UpdateInfo
- Activity18MiniGameSubmitWindow.InitBtn
- Activity18MiniGameSubmitWindow.OnClose
**Requires:**
- ActivityDungeon1018_MiniStart_EndRewardWindowByName
**Snippet:**
```lua
require("ActivityDungeon1018_MiniStart_EndRewardWindowByName")
local Activity18MiniGameSubmitWindow = {}
local uis, contentPane, nowIntegral

function Activity18MiniGameSubmitWindow.ReInitData()
end

function Activity18MiniGameSubmitWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity18MiniGameSubmitWindow.package, WinResConfig.Activity18MiniGameSubmitWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity18MiniGameTaskWindow.lua.lua
**Functions:**
- RefreshRewardList
- list.itemRenderer
- itemlist.itemRenderer
- Activity18MiniGameTaskWindow.ReInitData
- Activity18MiniGameTaskWindow.OnInit
- Activity18MiniGameTaskWindow.UpdateInfo
- Activity18MiniGameTaskWindow.InitBtn
- Activity18MiniGameTaskWindow.OnClose
**Requires:**
- ActivityDungeon1018_MiniTaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1018_MiniTaskWindowByName")
local Activity18MiniGameTaskWindow = {}
local uis, contentPane

local function RefreshRewardList()
  local info = Activity18_MiniGameData.GetMiniGameInfo()
  local minigame_tasks = info.taskList
  local list = uis.Main.TipsList
  list:SetVirtual()
  
```

---

## Activty/baseact/Activity18MiniGameWindow.lua.lua
**Functions:**
- Activity18MiniGameWindow.ReInitData
- Activity18MiniGameWindow.OnInit
- Activity18MiniGameWindow.CreateBlock
- Activity18MiniGameWindow.GetOrCreateHolder
- Activity18MiniGameWindow.UpdateInfo
- Activity18MiniGameWindow.CreateNewDice
- Activity18MiniGameWindow.SetDicePage
- Activity18MiniGameWindow.InitInfo
- Activity18MiniGameWindow.OnDragStart
- Activity18MiniGameWindow.GetGridPosition
- Activity18MiniGameWindow.OnDragMove
- Activity18MiniGameWindow.CheckDragGrid
- Activity18MiniGameWindow.OnDragEnd
- Activity18MiniGameWindow.ClearDrag
- Activity18MiniGameWindow.InitGrid
- Activity18MiniGameWindow.GenerateDice
- Activity18MiniGameWindow:HasAdjacentEmptySpaces
- Activity18MiniGameWindow:CreateDice
- Activity18MiniGameWindow:GetCurrentProbabilityStage
- Activity18MiniGameWindow.IsValidPosition
- Activity18MiniGameWindow.CanPlaceDice
- Activity18MiniGameWindow.PlaceDice
- Activity18MiniGameWindow.HandleDirectionClick
- Activity18MiniGameWindow.CheckSynthesis
- findAdjacentDice
- Activity18MiniGameWindow.HideImage
- Activity18MiniGameWindow.UpdatePoints
- Activity18MiniGameWindow.OnGameOver
- Activity18MiniGameWindow.OnNext
- Activity18MiniGameWindow.InitBtn
- Activity18MiniGameWindow.HandleMessage
- Activity18MiniGameWindow.OnClose
**Requires:**
- ActivityDungeon1018_MiniGameStartWindowByName
**Snippet:**
```lua
require("ActivityDungeon1018_MiniGameStartWindowByName")
local Activity18MiniGameWindow = {}
local uis, contentPane
local config = {
  gridSize = 5,
  dragY = 120,
  effectWaitTime = 0.65,
  pointsForExtraDice = 500,
  diceRanks = {
    1,
```

---

## Activty/baseact/Activity18PassportLevelUpTipsWindow.lua.lua
**Functions:**
- Activity18PassportLevelUpTipsWindow.ReInitData
- Activity18PassportLevelUpTipsWindow.OnInit
- Activity18PassportLevelUpTipsWindow.UpdateInfo
- Activity18PassportLevelUpTipsWindow.InitBtn
- Activity18PassportLevelUpTipsWindow.OnClose
**Requires:**
- ActivityDungeon1018_PassportUp_LevelUpTipsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1018_PassportUp_LevelUpTipsWindowByName")
local Activity18PassportLevelUpTipsWindow = {}
local uis, contentPane, lv

function Activity18PassportLevelUpTipsWindow.ReInitData()
end

function Activity18PassportLevelUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity18PassportLevelUpTipsWindow.package, WinResConfig.Activity18PassportLevelUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity18PassportWindow.lua.lua
**Functions:**
- Activity18PassportWindow.ReInitData
- Activity18PassportWindow.OnInit
- Activity18PassportWindow.UpdateTextDisplay
- Activity18PassportWindow.InitPassport
- uis.Main.TabRegion.TabList.itemRenderer
- Activity18PassportWindow.InitEffect
- Activity18PassportWindow.InitLv
- Activity18PassportWindow.ShowLevelUp
- Activity18PassportWindow.SaveLevel
- Activity18PassportWindow.GetRewardByLv
- Activity18PassportWindow.GetRewardNum
- Activity18PassportWindow.IsGetAllReward
- Activity18PassportWindow.ShowReward
- Activity18PassportWindow.GetUpdateLv
- Activity18PassportWindow.RefreshListReward
- Activity18PassportWindow.CheckItemTime
- Activity18PassportWindow.ShowQuitTips
- Activity18PassportWindow.RefreshUI
- Activity18PassportWindow.GetExpMxp
- Activity18PassportWindow.SetLevelInfo
- Activity18PassportWindow.InitList
- list.itemRenderer
- Activity18PassportWindow.SetListPos
- Activity18PassportWindow.RefreshReward
- Activity18PassportWindow.ShowGetEffect
- Activity18PassportWindow.RewardItemClick
- Activity18PassportWindow.IsReward
- Activity18PassportWindow.RefreshRewardFirst
- Activity18PassportWindow.RefreshRewardEnd
- Activity18PassportWindow.ShowState
- Activity18PassportWindow.RefreshRewardShow
- Activity18PassportWindow.RefreshRewardState
- Activity18PassportWindow.PassportActivate
- Activity18PassportWindow.CloseWindow
- Activity18PassportWindow.InitBtn
- Activity18PassportWindow.ShowExpBarAnim
- Activity18PassportWindow.InitTask
- list.itemRenderer
- Activity18PassportWindow.InitClothes
- clothes.BuyReward.RewardList.itemRenderer
- Activity18PassportWindow.SetLastLv
- Activity18PassportWindow.PlayFirstRewardEffect
- Activity18PassportWindow.PlayEndRewardEffect
- Activity18PassportWindow.HandleMessage
- Activity18PassportWindow.OnShown
- Activity18PassportWindow.OnClose
**Requires:**
- ActivityDungeon1018_PassportWindowByName
**Snippet:**
```lua
require("ActivityDungeon1018_PassportWindowByName")
local Activity18PassportWindow = {}
local uis, contentPane, passInfo, lvMax, modelType, expMax, rewardData, rewardType, rewardLv, listPage, passLv, jumpTb, isShowAllGet, passPortConfig, lvTween, lastLv, waitMessageId, newPassPort, animTween

function Activity18PassportWindow.ReInitData()
end

function Activity18PassportWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity18PassportWindow.package, WinResConfig.Activity18PassportWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity18PlotWindow.lua.lua
**Functions:**
- Activity18PlotWindow.ReInitData
- Activity18PlotWindow.OnInit
- Activity18PlotWindow.UpdateInfo
- list.itemRenderer
- Activity18PlotWindow.InitBtn
- Activity18PlotWindow.CloseWindow
- Activity18PlotWindow.OnClose
**Requires:**
- ActivityDungeon1018_PlotWindowByName
**Snippet:**
```lua
require("ActivityDungeon1018_PlotWindowByName")
local Activity18PlotWindow = {}
local uis, contentPane, configData

function Activity18PlotWindow.ReInitData()
end

function Activity18PlotWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity18PlotWindow.package, WinResConfig.Activity18PlotWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity18ShopWindow.lua.lua
**Functions:**
- Activity18ShopWindow.ReInitData
- Activity18ShopWindow.OnInit
- Activity18ShopWindow.UpdateInfo
- uis.Main.ItemList.itemRenderer
- Activity18ShopWindow.ShowItem
- list.itemRenderer
- Activity18ShopWindow.ShowOneReward
- list.itemRenderer
- Activity18ShopWindow.GetShopGrid
- Activity18ShopWindow.InitBtn
- Activity18ShopWindow.CloseWindow
- Activity18ShopWindow.OnClose
- Activity18ShopWindow.HandleMessage
**Requires:**
- ActivityDungeon1018_ShopWindowByName
**Snippet:**
```lua
require("ActivityDungeon1018_ShopWindowByName")
local Activity18ShopWindow = {}
local uis, contentPane, activityInfo, tempAssetsTips

function Activity18ShopWindow.ReInitData()
end

function Activity18ShopWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity18ShopWindow.package, WinResConfig.Activity18ShopWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity18SignWindow.lua.lua
**Functions:**
- Activity18SignWindow.ReInitData
- Activity18SignWindow.OnInit
- Activity18SignWindow.UpdateInfo
- list.RewardList.itemRenderer
- Activity18SignWindow.ShowAllItemFrame
- Activity18SignWindow.GetRewardData
- Activity18SignWindow.InitBtn
- Activity18SignWindow.CloseWindow
- Activity18SignWindow.OnClose
**Requires:**
- ActivityDungeon1018_SignWindowByName
**Snippet:**
```lua
require("ActivityDungeon1018_SignWindowByName")
local Activity18SignWindow = {}
local uis, contentPane, activityInfo

function Activity18SignWindow.ReInitData()
end

function Activity18SignWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity18SignWindow.package, WinResConfig.Activity18SignWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity18TaskWindow.lua.lua
**Functions:**
- Activity18TaskWindow.ReInitData
- Activity18TaskWindow.OnInit
- Activity18TaskWindow.UpdateInfo
- list.itemRenderer
- rewardList.itemRenderer
- Activity18TaskWindow.GetRewardNum
- Activity18TaskWindow.ShowAllItemFrame
- Activity18TaskWindow.SortTask
- Activity18TaskWindow.InitBtn
- Activity18TaskWindow.CloseWindow
- Activity18TaskWindow.OnClose
**Requires:**
- ActivityDungeon1018_TaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1018_TaskWindowByName")
local Activity18TaskWindow = {}
local uis, contentPane

function Activity18TaskWindow.ReInitData()
end

function Activity18TaskWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity18TaskWindow.package, WinResConfig.Activity18TaskWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity18_MiniGameData.lua.lua
**Functions:**
- Activity18_MiniGameData.SetMiniGameInfo
- Activity18_MiniGameData.GetMiniGameInfo
**Snippet:**
```lua
Activity18_MiniGameData = {gameId = 70441023}
local miniGameInfo

function Activity18_MiniGameData.SetMiniGameInfo(info)
  miniGameInfo = info
end

function Activity18_MiniGameData.GetMiniGameInfo()
  return miniGameInfo
end
```

---

## Activty/baseact/Activity18_MiniGameScriptList.lua.lua
**Requires:**
- Activity18_MiniGameData
- Activity18_MiniGameService
**Snippet:**
```lua
require("Activity18_MiniGameData")
require("Activity18_MiniGameService")
```

---

## Activty/baseact/Activity18_MiniGameService.lua.lua
**Functions:**
- Activity18_MiniGameService.MiniGameInfoReq
- Activity18_MiniGameService.MiniGameInfoRsp
- Activity18_MiniGameService.MiniGameSubmitReq
- Activity18_MiniGameService.MiniGameSubmitRsp
- Activity18_MiniGameService.MiniGameGetDailyRewardReq
- Activity18_MiniGameService.MiniGameGetDailyRewardRsp
- Activity18_MiniGameService.ActivityGetGameTopRankReq
- Activity18_MiniGameService.ActivityGetGameTopRankRsp
- Activity18_MiniGameService.Init
**Snippet:**
```lua
Activity18_MiniGameService = {}
local gameId = Activity18_MiniGameData.gameId

function Activity18_MiniGameService.MiniGameInfoReq(rspCallback)
  local info = ActivityDungeonData.GetActivityInfo()
  local activityId = info.baseInfo.activityId
  Net.Send(Proto.MsgName.ActivityGetMiniGameReq, {gameId = gameId, activityId = activityId}, rspCallback)
end

function Activity18_MiniGameService.MiniGameInfoRsp(msg)
```

---

## Activty/baseact/Activity19BossBattleWindow.lua.lua
**Functions:**
- Activity19BossBattleWindow.ReInitData
- Activity19BossBattleWindow.OnInit
- Activity19BossBattleWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity19BossBattleWindow.FormatRemainTime
- Activity19BossBattleWindow.GetChapter
- Activity19BossBattleWindow.InitBtn
- Activity19BossBattleWindow.CloseWindow
- Activity19BossBattleWindow.OnClose
**Requires:**
- ActivityDungeon1019_BossBattleWindowByName
**Snippet:**
```lua
require("ActivityDungeon1019_BossBattleWindowByName")
local Activity19BossBattleWindow = {}
local uis, contentPane, activityInfo

function Activity19BossBattleWindow.ReInitData()
end

function Activity19BossBattleWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity19BossBattleWindow.package, WinResConfig.Activity19BossBattleWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity19BuyLevelDesWindow.lua.lua
**Functions:**
- Activity19BuyLevelDesWindow.ReInitData
- Activity19BuyLevelDesWindow.OnInit
- Activity19BuyLevelDesWindow.ShowAssetsTips
- Activity19BuyLevelDesWindow.UpdateTextDisplay
- Activity19BuyLevelDesWindow.Init
- Activity19BuyLevelDesWindow.GetGold
- Activity19BuyLevelDesWindow.ShowReward
- list.itemRenderer
- Activity19BuyLevelDesWindow.GetRewardItem
- Activity19BuyLevelDesWindow.GetLvData
- Activity19BuyLevelDesWindow.GetRewardLvData
- Activity19BuyLevelDesWindow.GetRewardByPhaseId
- Activity19BuyLevelDesWindow.BuyLevelRsp
- Activity19BuyLevelDesWindow.InitBtn
- waitFun
- Activity19BuyLevelDesWindow.HandleMessage
- Activity19BuyLevelDesWindow.OnShown
- Activity19BuyLevelDesWindow.OnClose
**Requires:**
- ActivityDungeon1019_BuyLevelDesWindowByName
**Snippet:**
```lua
require("ActivityDungeon1019_BuyLevelDesWindowByName")
local Activity19BuyLevelDesWindow = {}
local uis, contentPane, lvData, curLv, buyNum, itemId, lvMax, waitFun, rewardData, itemSort, transPlay, firstPlay, tatalGold, passInfo

function Activity19BuyLevelDesWindow.ReInitData()
end

function Activity19BuyLevelDesWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity19BuyLevelDesWindow.package, WinResConfig.Activity19BuyLevelDesWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity19ChallengeWindow.lua.lua
**Functions:**
- Activity19ChallengeWindow.ReInitData
- Activity19ChallengeWindow.OnInit
- Activity19ChallengeWindow.UpdateInfo
- uis.Main.ChapterList.itemRenderer
- Activity19ChallengeWindow.ShoweStage
- Activity19ChallengeWindow.StageItemClick
- Activity19ChallengeWindow.ShopInfo
- Activity19ChallengeWindow.GetChapterPassById
- Activity19ChallengeWindow.GetCurStage
- Activity19ChallengeWindow.GetFirstChapter
- Activity19ChallengeWindow.GetAllChapterId
- Activity19ChallengeWindow.InitBtn
- Activity19ChallengeWindow.CloseWindow
- Activity19ChallengeWindow.OnShown
- Activity19ChallengeWindow.OnClose
**Requires:**
- ActivityDungeon1019_ChallengeWindowByName
**Snippet:**
```lua
require("ActivityDungeon1019_ChallengeWindowByName")
local Activity19ChallengeWindow = {}
local uis, contentPane, activityInfo, scrollingTween

function Activity19ChallengeWindow.ReInitData()
end

function Activity19ChallengeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity19ChallengeWindow.package, WinResConfig.Activity19ChallengeWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity19DungeonWindow.lua.lua
**Functions:**
- Activity19DungeonWindow.ReInitData
- Activity19DungeonWindow.OnInit
- Activity19DungeonWindow.LoadBg
- Activity19DungeonWindow.InitRedDot
- Activity19DungeonWindow.UpdateInfo
- Activity19DungeonWindow.InitBtnTxt
- Activity19DungeonWindow.InitBtn
- Activity19DungeonWindow.OnShown
- Activity19DungeonWindow.OnClose
- Activity19DungeonWindow.HandleMessage
**Requires:**
- ActivityDungeon1019_ActivityDungeonWindowByName
**Snippet:**
```lua
require("ActivityDungeon1019_ActivityDungeonWindowByName")
local Activity19DungeonWindow = {}
local uis, contentPane, jumpTb, configData, activityInfo, effect
local InitMiniGameInfo = function()
  local data = ActivityDungeonData.GetActivityData()
  if data.id == 70440019 then
    ld("Activity19_MiniGame")
    Activity19_MiniGameService.MiniGameInfoReq(function()
      RedDotMgr.AddNode({
        windowName = WinResConfig.Activity19DungeonWindow.name,
```

---

## Activty/baseact/Activity19MaterialWindow.lua.lua
**Functions:**
- Activity19MaterialWindow.ReInitData
- Activity19MaterialWindow.OnInit
- Activity19MaterialWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity19MaterialWindow.GetChapter
- Activity19MaterialWindow.GetMaxCount
- Activity19MaterialWindow.InitBtn
- Activity19MaterialWindow.CloseWindow
- Activity19MaterialWindow.OnShown
- Activity19MaterialWindow.OnClose
**Requires:**
- ActivityDungeon1019_MaterialWindowByName
**Snippet:**
```lua
require("ActivityDungeon1019_MaterialWindowByName")
local Activity19MaterialWindow = {}
local uis, contentPane, activityInfo, maxCount, posX

function Activity19MaterialWindow.ReInitData()
end

function Activity19MaterialWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity19MaterialWindow.package, WinResConfig.Activity19MaterialWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity19MiniGameMainWindow.lua.lua
**Functions:**
- RefreshPanelInfo
- Activity19MiniGameMainWindow.ReInitData
- Activity19MiniGameMainWindow.OnInit
- Activity19MiniGameMainWindow.UpdateInfo
- Activity19MiniGameMainWindow.InitBtn
- Activity19MiniGameMainWindow.OnClose
- Activity19MiniGameMainWindow.HandleMessage
**Requires:**
- ActivityDungeon1019_MiniGameWindowByName
**Snippet:**
```lua
require("ActivityDungeon1019_MiniGameWindowByName")
local Activity19MiniGameMainWindow = {}
local uis, contentPane
local gameId = 70441024
ld("Activity19_MiniGame")

local function RefreshPanelInfo()
  local info = Activity19_MiniGameData.GetMiniGameInfo()
  local conf = TableData.GetConfig(gameId, "BaseActivityStageGame")
  local str = conf.game_day_reward[1]
```

---

## Activty/baseact/Activity19MiniGameSubmitWindow.lua.lua
**Functions:**
- Activity19MiniGameSubmitWindow.ReInitData
- Activity19MiniGameSubmitWindow.OnInit
- Activity19MiniGameSubmitWindow.UpdateInfo
- Activity19MiniGameSubmitWindow.InitBtn
- Activity19MiniGameSubmitWindow.OnClose
**Requires:**
- ActivityDungeon1019_MiniStart_EndRewardWindowByName
**Snippet:**
```lua
require("ActivityDungeon1019_MiniStart_EndRewardWindowByName")
local Activity19MiniGameSubmitWindow = {}
local uis, contentPane
local gameId = 70441024
local score, newRecord

function Activity19MiniGameSubmitWindow.ReInitData()
end

function Activity19MiniGameSubmitWindow.OnInit(bridgeObj)
```

---

## Activty/baseact/Activity19MiniGameTaskWindow.lua.lua
**Functions:**
- RefreshRewardList
- list.itemRenderer
- itemlist.itemRenderer
- Activity19MiniGameTaskWindow.ReInitData
- Activity19MiniGameTaskWindow.OnInit
- Activity19MiniGameTaskWindow.UpdateInfo
- Activity19MiniGameTaskWindow.InitBtn
- Activity19MiniGameTaskWindow.OnClose
**Requires:**
- ActivityDungeon1019_MiniTaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1019_MiniTaskWindowByName")
local Activity19MiniGameTaskWindow = {}
local uis, contentPane
local gameId = 70441024

local function RefreshRewardList()
  local info = Activity19_MiniGameData.GetMiniGameInfo(gameId)
  local minigame_tasks = info.taskList
  local list = uis.Main.TipsList
  list:SetVirtual()
```

---

## Activty/baseact/Activity19MiniGameWindow.lua.lua
**Functions:**
- Activity19MiniGameWindow.ReInitData
- Activity19MiniGameWindow.OnInit
- Activity19MiniGameWindow.UpdateInfo
- Activity19MiniGameWindow.InitBtn
- Activity19MiniGameWindow.OnClose
- Activity19MiniGameWindow.HandleMessage
**Requires:**
- ActivityDungeon1019_MiniGameStartWindowByName
- Activity19_MiniGameController
**Snippet:**
```lua
require("ActivityDungeon1019_MiniGameStartWindowByName")
local Activity19MiniGameWindow = {}
local uis, contentPane
local HP_REDUCE_DELAY = 1
local WAIT_FOR_SECONDS_WHEN_HP_REDUCE = 2
local controller = require("Activity19_MiniGameController")
local delayTween, itemObjLookup, touched, finger, backgroundTemplates, backgrounds, viewCenter, viewHeight
local WorldToScreenPoint = function(x, y)
  local cam = UICamera
  local sp = cam:WorldToScreenPoint(Vector3(x, y, 0))
```

---

## Activty/baseact/Activity19PassportLevelUpTipsWindow.lua.lua
**Functions:**
- Activity19PassportLevelUpTipsWindow.ReInitData
- Activity19PassportLevelUpTipsWindow.OnInit
- Activity19PassportLevelUpTipsWindow.UpdateInfo
- Activity19PassportLevelUpTipsWindow.InitBtn
- Activity19PassportLevelUpTipsWindow.OnClose
**Requires:**
- ActivityDungeon1019_PassportUp_LevelUpTipsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1019_PassportUp_LevelUpTipsWindowByName")
local Activity19PassportLevelUpTipsWindow = {}
local uis, contentPane, lv

function Activity19PassportLevelUpTipsWindow.ReInitData()
end

function Activity19PassportLevelUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity19PassportLevelUpTipsWindow.package, WinResConfig.Activity19PassportLevelUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity19PassportWindow.lua.lua
**Functions:**
- Activity19PassportWindow.ReInitData
- Activity19PassportWindow.OnInit
- Activity19PassportWindow.UpdateTextDisplay
- Activity19PassportWindow.InitPassport
- uis.Main.TabRegion.TabList.itemRenderer
- Activity19PassportWindow.InitEffect
- Activity19PassportWindow.InitLv
- Activity19PassportWindow.ShowLevelUp
- Activity19PassportWindow.SaveLevel
- Activity19PassportWindow.GetRewardByLv
- Activity19PassportWindow.GetRewardNum
- Activity19PassportWindow.IsGetAllReward
- Activity19PassportWindow.ShowReward
- Activity19PassportWindow.GetUpdateLv
- Activity19PassportWindow.RefreshListReward
- Activity19PassportWindow.CheckItemTime
- Activity19PassportWindow.ShowQuitTips
- Activity19PassportWindow.RefreshUI
- Activity19PassportWindow.GetExpMxp
- Activity19PassportWindow.SetLevelInfo
- Activity19PassportWindow.InitList
- list.itemRenderer
- Activity19PassportWindow.SetListPos
- Activity19PassportWindow.RefreshReward
- Activity19PassportWindow.ShowGetEffect
- Activity19PassportWindow.RewardItemClick
- Activity19PassportWindow.IsReward
- Activity19PassportWindow.RefreshRewardFirst
- Activity19PassportWindow.RefreshRewardEnd
- Activity19PassportWindow.ShowState
- Activity19PassportWindow.RefreshRewardShow
- Activity19PassportWindow.RefreshRewardState
- Activity19PassportWindow.PassportActivate
- Activity19PassportWindow.CloseWindow
- Activity19PassportWindow.InitBtn
- Activity19PassportWindow.ShowExpBarAnim
- Activity19PassportWindow.InitTask
- list.itemRenderer
- Activity19PassportWindow.InitClothes
- clothes.BuyReward.RewardList.itemRenderer
- Activity19PassportWindow.SetLastLv
- Activity19PassportWindow.PlayFirstRewardEffect
- Activity19PassportWindow.PlayEndRewardEffect
- Activity19PassportWindow.HandleMessage
- Activity19PassportWindow.OnShown
- Activity19PassportWindow.OnClose
**Requires:**
- ActivityDungeon1019_PassportWindowByName
**Snippet:**
```lua
require("ActivityDungeon1019_PassportWindowByName")
local Activity19PassportWindow = {}
local uis, contentPane, passInfo, lvMax, modelType, expMax, rewardData, rewardType, rewardLv, listPage, passLv, jumpTb, isShowAllGet, passPortConfig, lvTween, lastLv, waitMessageId, newPassPort, animTween

function Activity19PassportWindow.ReInitData()
end

function Activity19PassportWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity19PassportWindow.package, WinResConfig.Activity19PassportWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity19PlotWindow.lua.lua
**Functions:**
- Activity19PlotWindow.ReInitData
- Activity19PlotWindow.OnInit
- Activity19PlotWindow.UpdateInfo
- list.itemRenderer
- Activity19PlotWindow.InitBtn
- Activity19PlotWindow.CloseWindow
- Activity19PlotWindow.OnClose
**Requires:**
- ActivityDungeon1019_PlotWindowByName
**Snippet:**
```lua
require("ActivityDungeon1019_PlotWindowByName")
local Activity19PlotWindow = {}
local uis, contentPane, configData

function Activity19PlotWindow.ReInitData()
end

function Activity19PlotWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity19PlotWindow.package, WinResConfig.Activity19PlotWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity19ShopWindow.lua.lua
**Functions:**
- Activity19ShopWindow.ReInitData
- Activity19ShopWindow.OnInit
- Activity19ShopWindow.UpdateInfo
- uis.Main.ItemList.itemRenderer
- Activity19ShopWindow.ShowItem
- list.itemRenderer
- Activity19ShopWindow.ShowOneReward
- list.itemRenderer
- Activity19ShopWindow.GetShopGrid
- Activity19ShopWindow.InitBtn
- Activity19ShopWindow.CloseWindow
- Activity19ShopWindow.OnClose
- Activity19ShopWindow.HandleMessage
**Requires:**
- ActivityDungeon1019_ShopWindowByName
**Snippet:**
```lua
require("ActivityDungeon1019_ShopWindowByName")
local Activity19ShopWindow = {}
local uis, contentPane, activityInfo, tempAssetsTips

function Activity19ShopWindow.ReInitData()
end

function Activity19ShopWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity19ShopWindow.package, WinResConfig.Activity19ShopWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity19SignWindow.lua.lua
**Functions:**
- Activity19SignWindow.ReInitData
- Activity19SignWindow.OnInit
- Activity19SignWindow.UpdateInfo
- list.RewardList.itemRenderer
- Activity19SignWindow.ShowAllItemFrame
- Activity19SignWindow.GetRewardData
- Activity19SignWindow.InitBtn
- Activity19SignWindow.CloseWindow
- Activity19SignWindow.OnClose
**Requires:**
- ActivityDungeon1019_SignWindowByName
**Snippet:**
```lua
require("ActivityDungeon1019_SignWindowByName")
local Activity19SignWindow = {}
local uis, contentPane, activityInfo

function Activity19SignWindow.ReInitData()
end

function Activity19SignWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity19SignWindow.package, WinResConfig.Activity19SignWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity19TaskWindow.lua.lua
**Functions:**
- Activity19TaskWindow.ReInitData
- Activity19TaskWindow.OnInit
- Activity19TaskWindow.UpdateInfo
- list.itemRenderer
- rewardList.itemRenderer
- Activity19TaskWindow.GetRewardNum
- Activity19TaskWindow.ShowAllItemFrame
- Activity19TaskWindow.SortTask
- Activity19TaskWindow.InitBtn
- Activity19TaskWindow.CloseWindow
- Activity19TaskWindow.OnClose
**Requires:**
- ActivityDungeon1019_TaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1019_TaskWindowByName")
local Activity19TaskWindow = {}
local uis, contentPane

function Activity19TaskWindow.ReInitData()
end

function Activity19TaskWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity19TaskWindow.package, WinResConfig.Activity19TaskWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity19_MiniGameController.lua.lua
**Snippet:**
```lua
local TRAY_WIDTH, TRAY_HEIGHT = 0.8, 0.6
local ITEM_WIDTH, ITEM_HEIGHT = 0.7, 0.28
local BG_MOVE_SPEED = 0.5
local CAMERA_MOVE_SPEED = 2
local DEFAULT_HP = 3
local MAX_HORIZONTAL_OFFSET_RATIO = 0.02
local BOUNCE_DIST = 0.12
local LEFT_MARGIN = 0.5
local RIGHT_MARGIN = 0.5
local MAX_COUNT_IN_VIEW = 8
```

---

## Activty/baseact/Activity19_MiniGameData.lua.lua
**Snippet:**
```lua
local miniGameInfo
local SetMiniGameInfo = function(info)
  miniGameInfo = info
end
local GetMiniGameInfo = function()
  return miniGameInfo
end
return {SetMiniGameInfo = SetMiniGameInfo, GetMiniGameInfo = GetMiniGameInfo}
```

---

## Activty/baseact/Activity19_MiniGameScriptList.lua.lua
**Requires:**
- Activity19_MiniGameData
- Activity19_MiniGameService
**Snippet:**
```lua
Activity19_MiniGameData = require("Activity19_MiniGameData")
Activity19_MiniGameService = require("Activity19_MiniGameService")
```

---

## Activty/baseact/Activity19_MiniGameService.lua.lua
**Snippet:**
```lua
local gameId = 70441024
local MiniGameInfoReq = function(rspCallback)
  local info = ActivityDungeonData.GetActivityStageByShowId(19)
  local activityId = info.baseInfo.activityId
  Net.Send(Proto.MsgName.ActivityGetMiniGameReq, {activityId = activityId, gameId = gameId}, rspCallback)
end
local MiniGameInfoRsp = function(msg)
  Activity19_MiniGameData.SetMiniGameInfo(msg)
  UIMgr:SendWindowMessage(WinResConfig.Activity19MiniGameMainWindow.name, WindowMsgEnum.Activity19_MiniGame.REFRESH_MINIGAME_INFO)
  UIMgr:SendWindowMessage(WinResConfig.Activity19MiniGameWindow.name, WindowMsgEnum.Activity19_MiniGame.REFRESH_MINIGAME_INFO)
```

---

## Activty/baseact/Activity1_MiniGameController.lua.lua
**Snippet:**
```lua
local MINI_GAME_DURATION = 30
local ROW, COL = 3, 3
local FLOWER_ENUM = {
  A = 1,
  B = 2,
  C = 3
}
local FLOWER_GEN_DELAY = {
  [FLOWER_ENUM.A] = 0,
  [FLOWER_ENUM.B] = 5.5,
```

---

## Activty/baseact/Activity1_MiniGameData.lua.lua
**Snippet:**
```lua
local miniGameInfo
local SetMiniGameInfo = function(info)
  miniGameInfo = info
end
local GetMiniGameInfo = function()
  return miniGameInfo
end
return {SetMiniGameInfo = SetMiniGameInfo, GetMiniGameInfo = GetMiniGameInfo}
```

---

## Activty/baseact/Activity1_MiniGameScriptList.lua.lua
**Requires:**
- Activity1_MiniGameData
- Activity1_MiniGameService
- Activity1_MiniGameController
**Snippet:**
```lua
Activity1_MiniGameData = require("Activity1_MiniGameData")
Activity1_MiniGameService = require("Activity1_MiniGameService")
Activity1_MiniGameController = require("Activity1_MiniGameController")
```

---

## Activty/baseact/Activity1_MiniGameService.lua.lua
**Snippet:**
```lua
local gameId = 70441001
local MiniGameInfoReq = function(rspCallback)
  local info = ActivityDungeonData.GetActivityInfo()
  local activityId = info.baseInfo.activityId
  Net.Send(Proto.MsgName.ActivityGetMiniGameReq, {gameId = gameId, activityId = activityId}, rspCallback)
end
local MiniGameInfoRsp = function(msg)
  Activity1_MiniGameData.SetMiniGameInfo(msg)
  UIMgr:SendWindowMessage(WinResConfig.ActivityMiniGameMainWindow.name, WindowMsgEnum.Activity1_MiniGame.REFRESH_MINIGAME_INFO)
  RedDotMgr.UpdateNode(RED_DOT_DATA_TYPE.ACTIVITY_DUNGENON)
```

---

## Activty/baseact/Activity20BossBattleWindow.lua.lua
**Functions:**
- Activity20BossBattleWindow.ReInitData
- Activity20BossBattleWindow.OnInit
- Activity20BossBattleWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity20BossBattleWindow.FormatRemainTime
- Activity20BossBattleWindow.GetChapter
- Activity20BossBattleWindow.InitBtn
- Activity20BossBattleWindow.CloseWindow
- Activity20BossBattleWindow.OnClose
**Requires:**
- ActivityDungeon1020_BossBattleWindowByName
**Snippet:**
```lua
require("ActivityDungeon1020_BossBattleWindowByName")
local Activity20BossBattleWindow = {}
local uis, contentPane, activityInfo

function Activity20BossBattleWindow.ReInitData()
end

function Activity20BossBattleWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity20BossBattleWindow.package, WinResConfig.Activity20BossBattleWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity20BuyLevelDesWindow.lua.lua
**Functions:**
- Activity20BuyLevelDesWindow.ReInitData
- Activity20BuyLevelDesWindow.OnInit
- Activity20BuyLevelDesWindow.ShowAssetsTips
- Activity20BuyLevelDesWindow.UpdateTextDisplay
- Activity20BuyLevelDesWindow.Init
- Activity20BuyLevelDesWindow.GetGold
- Activity20BuyLevelDesWindow.ShowReward
- list.itemRenderer
- Activity20BuyLevelDesWindow.GetRewardItem
- Activity20BuyLevelDesWindow.GetLvData
- Activity20BuyLevelDesWindow.GetRewardLvData
- Activity20BuyLevelDesWindow.GetRewardByPhaseId
- Activity20BuyLevelDesWindow.BuyLevelRsp
- Activity20BuyLevelDesWindow.InitBtn
- waitFun
- Activity20BuyLevelDesWindow.HandleMessage
- Activity20BuyLevelDesWindow.OnShown
- Activity20BuyLevelDesWindow.OnClose
**Requires:**
- ActivityDungeon1020_BuyLevelDesWindowByName
**Snippet:**
```lua
require("ActivityDungeon1020_BuyLevelDesWindowByName")
local Activity20BuyLevelDesWindow = {}
local uis, contentPane, lvData, curLv, buyNum, itemId, lvMax, waitFun, rewardData, itemSort, transPlay, firstPlay, tatalGold, passInfo

function Activity20BuyLevelDesWindow.ReInitData()
end

function Activity20BuyLevelDesWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity20BuyLevelDesWindow.package, WinResConfig.Activity20BuyLevelDesWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity20ChallengeWindow.lua.lua
**Functions:**
- Activity20ChallengeWindow.ReInitData
- Activity20ChallengeWindow.OnInit
- Activity20ChallengeWindow.UpdateInfo
- uis.Main.ChapterList.itemRenderer
- Activity20ChallengeWindow.ShoweStage
- Activity20ChallengeWindow.StageItemClick
- Activity20ChallengeWindow.ShopInfo
- Activity20ChallengeWindow.GetChapterPassById
- Activity20ChallengeWindow.GetCurStage
- Activity20ChallengeWindow.GetFirstChapter
- Activity20ChallengeWindow.GetAllChapterId
- Activity20ChallengeWindow.InitBtn
- Activity20ChallengeWindow.CloseWindow
- Activity20ChallengeWindow.OnShown
- Activity20ChallengeWindow.OnClose
**Requires:**
- ActivityDungeon1020_ChallengeWindowByName
**Snippet:**
```lua
require("ActivityDungeon1020_ChallengeWindowByName")
local Activity20ChallengeWindow = {}
local uis, contentPane, activityInfo, scrollingTween

function Activity20ChallengeWindow.ReInitData()
end

function Activity20ChallengeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity20ChallengeWindow.package, WinResConfig.Activity20ChallengeWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity20DungeonWindow.lua.lua
**Functions:**
- Activity20DungeonWindow.ReInitData
- Activity20DungeonWindow.OnInit
- Activity20DungeonWindow.LoadBg
- Activity20DungeonWindow.InitRedDot
- Activity20DungeonWindow.UpdateInfo
- Activity20DungeonWindow.InitBtnTxt
- Activity20DungeonWindow.InitBtn
- Activity20DungeonWindow.OnShown
- Activity20DungeonWindow.OnClose
- Activity20DungeonWindow.HandleMessage
**Requires:**
- ActivityDungeon1020_ActivityDungeonWindowByName
**Snippet:**
```lua
require("ActivityDungeon1020_ActivityDungeonWindowByName")
local Activity20DungeonWindow = {}
local uis, contentPane, jumpTb, configData, activityInfo, effect
local InitMiniGameInfo = function()
  local data = ActivityDungeonData.GetActivityData()
  if data.id == 70440020 then
    ld("Activity20_MiniGame", function()
      Activity20_MiniGameService.MiniGameInfoReq(function()
        RedDotMgr.AddNode({
          windowName = WinResConfig.Activity20DungeonWindow.name,
```

---

## Activty/baseact/Activity20MaterialWindow.lua.lua
**Functions:**
- Activity20MaterialWindow.ReInitData
- Activity20MaterialWindow.OnInit
- Activity20MaterialWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity20MaterialWindow.GetChapter
- Activity20MaterialWindow.GetMaxCount
- Activity20MaterialWindow.InitBtn
- Activity20MaterialWindow.CloseWindow
- Activity20MaterialWindow.OnShown
- Activity20MaterialWindow.OnClose
**Requires:**
- ActivityDungeon1020_MaterialWindowByName
**Snippet:**
```lua
require("ActivityDungeon1020_MaterialWindowByName")
local Activity20MaterialWindow = {}
local uis, contentPane, activityInfo, maxCount, posX

function Activity20MaterialWindow.ReInitData()
end

function Activity20MaterialWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity20MaterialWindow.package, WinResConfig.Activity20MaterialWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity20MiniGameMainWindow.lua.lua
**Functions:**
- RefreshPanelInfo
- Activity20MiniGameMainWindow.ReInitData
- Activity20MiniGameMainWindow.OnInit
- Activity20MiniGameMainWindow.UpdateInfo
- Activity20MiniGameMainWindow.InitBtn
- Activity20MiniGameMainWindow.OnClose
- Activity20MiniGameMainWindow.HandleMessage
**Requires:**
- ActivityDungeon1020_MiniGameWindowByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniGameWindowByName")
ld("Activity20_MiniGame")
local Activity20MiniGameMainWindow = {}
local uis, contentPane

local function RefreshPanelInfo()
  local info = Activity20_MiniGameData.GetMiniGameInfo()
  local conf = TableData.GetConfig(Activity20_MiniGameData.gameId, "BaseActivityStageGame")
  local str = conf.game_day_reward[1]
  local splits = Split(str, ":")
```

---

## Activty/baseact/Activity20MiniGameSubmitWindow.lua.lua
**Functions:**
- Activity20MiniGameSubmitWindow.ReInitData
- Activity20MiniGameSubmitWindow.OnInit
- Activity20MiniGameSubmitWindow.UpdateInfo
- Activity20MiniGameSubmitWindow.InitBtn
- Activity20MiniGameSubmitWindow.OnClose
**Requires:**
- ActivityDungeon1020_MiniStart_EndRewardWindowByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniStart_EndRewardWindowByName")
local Activity20MiniGameSubmitWindow = {}
local uis, contentPane, progress, win, score

function Activity20MiniGameSubmitWindow.ReInitData()
end

function Activity20MiniGameSubmitWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity20MiniGameSubmitWindow.package, WinResConfig.Activity20MiniGameSubmitWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity20MiniGameTaskWindow.lua.lua
**Functions:**
- RefreshRewardList
- list.itemRenderer
- itemlist.itemRenderer
- Activity20MiniGameTaskWindow.ReInitData
- Activity20MiniGameTaskWindow.OnInit
- Activity20MiniGameTaskWindow.UpdateInfo
- Activity20MiniGameTaskWindow.InitBtn
- Activity20MiniGameTaskWindow.OnClose
**Requires:**
- ActivityDungeon1020_MiniTaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1020_MiniTaskWindowByName")
local Activity20MiniGameTaskWindow = {}
local uis, contentPane

local function RefreshRewardList()
  local info = Activity20_MiniGameData.GetMiniGameInfo()
  local minigame_tasks = info.taskList
  local list = uis.Main.TipsList
  list:SetVirtual()
  
```

---

## Activty/baseact/Activity20MiniGameWindow.lua.lua
**Functions:**
- Activity20MiniGameWindow.ReInitData
- Activity20MiniGameWindow.OnInit
- Activity20MiniGameWindow.UpdateInfo
- Activity20MiniGameWindow.InitBtn
- Activity20MiniGameWindow.HandleMessage
- Activity20MiniGameWindow.OnClose
**Requires:**
- ActivityDungeon1020_MiniGameStartWindowByName
- Activity20_MiniGameController
- Activity20_MiniGameConfigs
**Snippet:**
```lua
require("ActivityDungeon1020_MiniGameStartWindowByName")
local Activity20MiniGameWindow = {}
local uis, contentPane
local DRAG_OFFSET_Y = 120
local gameId = 70441025
local controller = require("Activity20_MiniGameController")
local cellObjs, guguObjs, positionObjs, levelIndex, displayNumber
local Screen2WorldPosition = function(global)
  local sc = StageCamera.main
  local position = sc:ScreenToWorldPoint(Vector3(global.x, Screen.height - global.y, -sc.transform.position.z))
```

---

## Activty/baseact/Activity20PassportLevelUpTipsWindow.lua.lua
**Functions:**
- Activity20PassportLevelUpTipsWindow.ReInitData
- Activity20PassportLevelUpTipsWindow.OnInit
- Activity20PassportLevelUpTipsWindow.UpdateInfo
- Activity20PassportLevelUpTipsWindow.InitBtn
- Activity20PassportLevelUpTipsWindow.OnClose
**Requires:**
- ActivityDungeon1020_PassportUp_LevelUpTipsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1020_PassportUp_LevelUpTipsWindowByName")
local Activity20PassportLevelUpTipsWindow = {}
local uis, contentPane, lv

function Activity20PassportLevelUpTipsWindow.ReInitData()
end

function Activity20PassportLevelUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity20PassportLevelUpTipsWindow.package, WinResConfig.Activity20PassportLevelUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity20PassportWindow.lua.lua
**Functions:**
- Activity20PassportWindow.ReInitData
- Activity20PassportWindow.OnInit
- Activity20PassportWindow.UpdateTextDisplay
- Activity20PassportWindow.InitPassport
- uis.Main.TabRegion.TabList.itemRenderer
- Activity20PassportWindow.InitEffect
- Activity20PassportWindow.InitLv
- Activity20PassportWindow.ShowLevelUp
- Activity20PassportWindow.SaveLevel
- Activity20PassportWindow.GetRewardByLv
- Activity20PassportWindow.GetRewardNum
- Activity20PassportWindow.IsGetAllReward
- Activity20PassportWindow.ShowReward
- Activity20PassportWindow.GetUpdateLv
- Activity20PassportWindow.RefreshListReward
- Activity20PassportWindow.CheckItemTime
- Activity20PassportWindow.ShowQuitTips
- Activity20PassportWindow.RefreshUI
- Activity20PassportWindow.GetExpMxp
- Activity20PassportWindow.SetLevelInfo
- Activity20PassportWindow.InitList
- list.itemRenderer
- Activity20PassportWindow.SetListPos
- Activity20PassportWindow.RefreshReward
- Activity20PassportWindow.ShowGetEffect
- Activity20PassportWindow.RewardItemClick
- Activity20PassportWindow.IsReward
- Activity20PassportWindow.RefreshRewardFirst
- Activity20PassportWindow.RefreshRewardEnd
- Activity20PassportWindow.ShowState
- Activity20PassportWindow.RefreshRewardShow
- Activity20PassportWindow.RefreshRewardState
- Activity20PassportWindow.PassportActivate
- Activity20PassportWindow.CloseWindow
- Activity20PassportWindow.InitBtn
- Activity20PassportWindow.ShowExpBarAnim
- Activity20PassportWindow.InitTask
- list.itemRenderer
- Activity20PassportWindow.InitClothes
- clothes.BuyReward.RewardList.itemRenderer
- Activity20PassportWindow.SetLastLv
- Activity20PassportWindow.PlayFirstRewardEffect
- Activity20PassportWindow.PlayEndRewardEffect
- Activity20PassportWindow.HandleMessage
- Activity20PassportWindow.OnShown
- Activity20PassportWindow.OnClose
**Requires:**
- ActivityDungeon1020_PassportWindowByName
**Snippet:**
```lua
require("ActivityDungeon1020_PassportWindowByName")
local Activity20PassportWindow = {}
local uis, contentPane, passInfo, lvMax, modelType, expMax, rewardData, rewardType, rewardLv, listPage, passLv, jumpTb, isShowAllGet, passPortConfig, lvTween, lastLv, waitMessageId, newPassPort, animTween

function Activity20PassportWindow.ReInitData()
end

function Activity20PassportWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity20PassportWindow.package, WinResConfig.Activity20PassportWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity20PlotWindow.lua.lua
**Functions:**
- Activity20PlotWindow.ReInitData
- Activity20PlotWindow.OnInit
- Activity20PlotWindow.UpdateInfo
- list.itemRenderer
- Activity20PlotWindow.InitBtn
- Activity20PlotWindow.CloseWindow
- Activity20PlotWindow.OnClose
**Requires:**
- ActivityDungeon1020_PlotWindowByName
**Snippet:**
```lua
require("ActivityDungeon1020_PlotWindowByName")
local Activity20PlotWindow = {}
local uis, contentPane, configData

function Activity20PlotWindow.ReInitData()
end

function Activity20PlotWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity20PlotWindow.package, WinResConfig.Activity20PlotWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity20ShopWindow.lua.lua
**Functions:**
- Activity20ShopWindow.ReInitData
- Activity20ShopWindow.OnInit
- Activity20ShopWindow.UpdateInfo
- uis.Main.ItemList.itemRenderer
- Activity20ShopWindow.ShowItem
- list.itemRenderer
- Activity20ShopWindow.ShowOneReward
- list.itemRenderer
- Activity20ShopWindow.GetShopGrid
- Activity20ShopWindow.InitBtn
- Activity20ShopWindow.CloseWindow
- Activity20ShopWindow.OnClose
- Activity20ShopWindow.HandleMessage
**Requires:**
- ActivityDungeon1020_ShopWindowByName
**Snippet:**
```lua
require("ActivityDungeon1020_ShopWindowByName")
local Activity20ShopWindow = {}
local uis, contentPane, activityInfo, tempAssetsTips

function Activity20ShopWindow.ReInitData()
end

function Activity20ShopWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity20ShopWindow.package, WinResConfig.Activity20ShopWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity20SignWindow.lua.lua
**Functions:**
- Activity20SignWindow.ReInitData
- Activity20SignWindow.OnInit
- Activity20SignWindow.UpdateInfo
- list.RewardList.itemRenderer
- Activity20SignWindow.ShowAllItemFrame
- Activity20SignWindow.GetRewardData
- Activity20SignWindow.InitBtn
- Activity20SignWindow.CloseWindow
- Activity20SignWindow.OnClose
**Requires:**
- ActivityDungeon1020_SignWindowByName
**Snippet:**
```lua
require("ActivityDungeon1020_SignWindowByName")
local Activity20SignWindow = {}
local uis, contentPane, activityInfo

function Activity20SignWindow.ReInitData()
end

function Activity20SignWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity20SignWindow.package, WinResConfig.Activity20SignWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity20TaskWindow.lua.lua
**Functions:**
- Activity20TaskWindow.ReInitData
- Activity20TaskWindow.OnInit
- Activity20TaskWindow.UpdateInfo
- list.itemRenderer
- rewardList.itemRenderer
- Activity20TaskWindow.GetRewardNum
- Activity20TaskWindow.ShowAllItemFrame
- Activity20TaskWindow.SortTask
- Activity20TaskWindow.InitBtn
- Activity20TaskWindow.CloseWindow
- Activity20TaskWindow.OnClose
**Requires:**
- ActivityDungeon1020_TaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1020_TaskWindowByName")
local Activity20TaskWindow = {}
local uis, contentPane

function Activity20TaskWindow.ReInitData()
end

function Activity20TaskWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity20TaskWindow.package, WinResConfig.Activity20TaskWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity20_MiniGameConfigs.lua.lua
**Snippet:**
```lua
return {
  [1] = {
    cells = {
      {x = 1, y = 1}
    },
    anchor = 1,
    score = 500
  },
  [2] = {
    cells = {
```

---

## Activty/baseact/Activity20_MiniGameConfigs2.lua.lua
**Snippet:**
```lua
return "[{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":1},{\"localColumn\":1,\"localRow\":2},{\"localColumn\":1,\"localRow\":3},{\"localColumn\":1,\"localRow\":4},{\"localColumn\":2,\"localRow\":4},{\"localColumn\":3,\"localRow\":4},{\"localColumn\":4,\"localRow\":4},{\"localColumn\":5,\"localRow\":4}],\"minRow\":0,\"maxCol\":5,\"maxRow\":4,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":-1},{\"localColumn\":2,\"localRow\":-1},{\"localColumn\":3,\"localRow\":-1},{\"localColumn\":3,\"localRow\":-2},{\"localColumn\":4,\"localRow\":-2},{\"localColumn\":4,\"localRow\":-3},{\"localColumn\":4,\"localRow\":-4},{\"localColumn\":5,\"localRow\":-4}],\"minRow\":-4,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":0},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":3,\"localRow\":0},{\"localColumn\":3,\"localRow\":1},{\"localColumn\":3,\"localRow\":2},{\"localColumn\":3,\"localRow\":3},{\"localColumn\":3,\"localRow\":4},{\"localColumn\":4,\"localRow\":4},{\"localColumn\":5,\"localRow\":4}],\"minRow\":0,\"maxCol\":5,\"maxRow\":4,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":3,\"localRow\":0},{\"localColumn\":4,\"localRow\":0},{\"localColumn\":5,\"localRow\":0},{\"localColumn\":5,\"localRow\":-1},{\"localColumn\":4,\"localRow\":-1},{\"localColumn\":4,\"localRow\":-2},{\"localColumn\":5,\"localRow\":-2}],\"minRow\":-2,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":0},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":-1},{\"localColumn\":2,\"localRow\":-1},{\"localColumn\":3,\"localRow\":-1},{\"localColumn\":4,\"localRow\":-1},{\"localColumn\":4,\"localRow\":0},{\"localColumn\":5,\"localRow\":0},{\"localColumn\":5,\"localRow\":1},{\"localColumn\":5,\"localRow\":2}],\"minRow\":-1,\"maxCol\":5,\"maxRow\":2,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":-1},{\"localColumn\":2,\"localRow\":-1},{\"localColumn\":3,\"localRow\":-1},{\"localColumn\":3,\"localRow\":0},{\"localColumn\":4,\"localRow\":0},{\"localColumn\":4,\"localRow\":1},{\"localColumn\":4,\"localRow\":2},{\"localColumn\":5,\"localRow\":2}],\"minRow\":-1,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":2},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":1},{\"localColumn\":2,\"localRow\":1},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":3,\"localRow\":0},{\"localColumn\":3,\"localRow\":1},{\"localColumn\":3,\"localRow\":2},{\"localColumn\":4,\"localRow\":2},{\"localColumn\":5,\"localRow\":2}],\"minRow\":0,\"maxCol\":5,\"maxRow\":2,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":3,\"localRow\":0},{\"localColumn\":3,\"localRow\":-1},{\"localColumn\":4,\"localRow\":-1},{\"localColumn\":4,\"localRow\":-2},{\"localColumn\":4,\"localRow\":-3},{\"localColumn\":4,\"localRow\":-4},{\"localColumn\":5,\"localRow\":-4}],\"minRow\":-4,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":0},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":3,\"localRow\":0},{\"localColumn\":3,\"localRow\":1},{\"localColumn\":4,\"localRow\":1},{\"localColumn\":4,\"localRow\":0},{\"localColumn\":4,\"localRow\":-1},{\"localColumn\":4,\"localRow\":-2},{\"localColumn\":5,\"localRow\":-2}],\"minRow\":-2,\"maxCol\":5,\"maxRow\":1,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":1},{\"localColumn\":2,\"localRow\":1},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":2,\"localRow\":-1},{\"localColumn\":3,\"localRow\":-1},{\"localColumn\":3,\"localRow\":0},{\"localColumn\":4,\"localRow\":0},{\"localColumn\":5,\"localRow\":0}],\"minRow\":-1,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":1},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":2,\"localRow\":-1},{\"localColumn\":3,\"localRow\":-1},{\"localColumn\":3,\"localRow\":-2},{\"localColumn\":4,\"localRow\":-2},{\"localColumn\":5,\"localRow\":-2},{\"localColumn\":5,\"localRow\":-1},{\"localColumn\":5,\"localRow\":0}],\"minRow\":-2,\"maxCol\":5,\"maxRow\":0,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":-1},{\"localColumn\":2,\"localRow\":-1},{\"localColumn\":2,\"localRow\":-2},{\"localColumn\":3,\"localRow\":-2},{\"localColumn\":4,\"localRow\":-2},{\"localColumn\":4,\"localRow\":-3},{\"localColumn\":5,\"localRow\":-3},{\"localColumn\":5,\"localRow\":-4}],\"minRow\":-4,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":0},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":1},{\"localColumn\":1,\"localRow\":2},{\"localColumn\":1,\"localRow\":3},{\"localColumn\":2,\"localRow\":3},{\"localColumn\":3,\"localRow\":3},{\"localColumn\":4,\"localRow\":3},{\"localColumn\":5,\"localRow\":3},{\"localColumn\":5,\"localRow\":2}],\"minRow\":0,\"maxCol\":5,\"maxRow\":3,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":1},{\"localColumn\":2,\"localRow\":1},{\"localColumn\":3,\"localRow\":1},{\"localColumn\":4,\"localRow\":1},{\"localColumn\":4,\"localRow\":2},{\"localColumn\":4,\"localRow\":3},{\"localColumn\":5,\"localRow\":3},{\"localColumn\":5,\"localRow\":2}],\"minRow\":0,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":3},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":2,\"localRow\":-1},{\"localColumn\":3,\"localRow\":-1},{\"localColumn\":4,\"localRow\":-1},{\"localColumn\":4,\"localRow\":0},{\"localColumn\":5,\"localRow\":0},{\"localColumn\":5,\"localRow\":-1},{\"localColumn\":5,\"localRow\":-2}],\"minRow\":-2,\"maxCol\":5,\"maxRow\":0,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":-1},{\"localColumn\":2,\"localRow\":-1},{\"localColumn\":2,\"localRow\":-2},{\"localColumn\":3,\"localRow\":-2},{\"localColumn\":3,\"localRow\":-3},{\"localColumn\":4,\"localRow\":-3},{\"localColumn\":5,\"localRow\":-3},{\"localColumn\":5,\"localRow\":-2}],\"minRow\":-3,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":0},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":1},{\"localColumn\":1,\"localRow\":2},{\"localColumn\":2,\"localRow\":2},{\"localColumn\":3,\"localRow\":2},{\"localColumn\":3,\"localRow\":1},{\"localColumn\":4,\"localRow\":1},{\"localColumn\":5,\"localRow\":1},{\"localColumn\":5,\"localRow\":2}],\"minRow\":0,\"maxCol\":5,\"maxRow\":2,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":-1},{\"localColumn\":2,\"localRow\":-1},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":2,\"localRow\":1},{\"localColumn\":2,\"localRow\":2},{\"localColumn\":3,\"localRow\":2},{\"localColumn\":4,\"localRow\":2},{\"localColumn\":5,\"localRow\":2}],\"minRow\":-1,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":2},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":2,\"localRow\":-1},{\"localColumn\":1,\"localRow\":-1},{\"localColumn\":1,\"localRow\":-2},{\"localColumn\":2,\"localRow\":-2},{\"localColumn\":3,\"localRow\":-2},{\"localColumn\":4,\"localRow\":-2},{\"localColumn\":5,\"localRow\":-2}],\"minRow\":-2,\"maxCol\":5,\"maxRow\":0,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":1},{\"localColumn\":1,\"localRow\":2},{\"localColumn\":2,\"localRow\":2},{\"localColumn\":2,\"localRow\":1},{\"localColumn\":3,\"localRow\":1},{\"localColumn\":3,\"localRow\":0},{\"localColumn\":4,\"localRow\":0},{\"localColumn\":5,\"localRow\":0}],\"minRow\":0,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":2},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":3,\"localRow\":0},{\"localColumn\":3,\"localRow\":-1},{\"localColumn\":3,\"localRow\":-2},{\"localColumn\":4,\"localRow\":-2},{\"localColumn\":4,\"localRow\":-1},{\"localColumn\":5,\"localRow\":-1},{\"localColumn\":5,\"localRow\":-2}],\"minRow\":-2,\"maxCol\":5,\"maxRow\":0,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":2,\"localRow\":-1},{\"localColumn\":3,\"localRow\":-1},{\"localColumn\":4,\"localRow\":-1},{\"localColumn\":4,\"localRow\":-2},{\"localColumn\":5,\"localRow\":-2},{\"localColumn\":5,\"localRow\":-1},{\"localColumn\":5,\"localRow\":0}],\"minRow\":-2,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":0},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":2,\"localRow\":-1},{\"localColumn\":3,\"localRow\":-1},{\"localColumn\":3,\"localRow\":-2},{\"localColumn\":3,\"localRow\":-3},{\"localColumn\":4,\"localRow\":-3},{\"localColumn\":4,\"localRow\":-2},{\"localColumn\":5,\"localRow\":-2}],\"minRow\":-3,\"maxCol\":5,\"maxRow\":0,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":3,\"localRow\":0},{\"localColumn\":3,\"localRow\":1},{\"localColumn\":3,\"localRow\":2},{\"localColumn\":4,\"localRow\":2},{\"localColumn\":4,\"localRow\":1},{\"localColumn\":5,\"localRow\":1},{\"localColumn\":5,\"localRow\":0}],\"minRow\":0,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":2},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":-1},{\"localColumn\":2,\"localRow\":-1},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":3,\"localRow\":0},{\"localColumn\":4,\"localRow\":0},{\"localColumn\":4,\"localRow\":1},{\"localColumn\":5,\"localRow\":1},{\"localColumn\":5,\"localRow\":0}],\"minRow\":-1,\"maxCol\":5,\"maxRow\":1,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":1},{\"localColumn\":2,\"localRow\":1},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":3,\"localRow\":0},{\"localColumn\":4,\"localRow\":0},{\"localColumn\":4,\"localRow\":1},{\"localColumn\":5,\"localRow\":1},{\"localColumn\":5,\"localRow\":0}],\"minRow\":0,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":1},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":-1},{\"localColumn\":2,\"localRow\":-1},{\"localColumn\":3,\"localRow\":-1},{\"localColumn\":4,\"localRow\":-1},{\"localColumn\":4,\"localRow\":0},{\"localColumn\":4,\"localRow\":1},{\"localColumn\":5,\"localRow\":1},{\"localColumn\":5,\"localRow\":2}],\"minRow\":-1,\"maxCol\":5,\"maxRow\":2,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":1},{\"localColumn\":1,\"localRow\":2},{\"localColumn\":2,\"localRow\":2},{\"localColumn\":2,\"localRow\":1},{\"localColumn\":3,\"localRow\":1},{\"localColumn\":4,\"localRow\":1},{\"localColumn\":4,\"localRow\":2},{\"localColumn\":5,\"localRow\":2}],\"minRow\":0,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":2},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":3,\"localRow\":0},{\"localColumn\":3,\"localRow\":1},{\"localColumn\":4,\"localRow\":1},{\"localColumn\":4,\"localRow\":0},{\"localColumn\":5,\"localRow\":0},{\"localColumn\":5,\"localRow\":1},{\"localColumn\":5,\"localRow\":2}],\"minRow\":0,\"maxCol\":5,\"maxRow\":2,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":-1},{\"localColumn\":2,\"localRow\":-1},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":3,\"localRow\":0},{\"localColumn\":3,\"localRow\":1},{\"localColumn\":3,\"localRow\":2},{\"localColumn\":4,\"localRow\":2},{\"localColumn\":5,\"localRow\":2}],\"minRow\":-1,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":2},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":1},{\"localColumn\":2,\"localRow\":1},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":3,\"localRow\":0},{\"localColumn\":4,\"localRow\":0},{\"localColumn\":4,\"localRow\":1},{\"localColumn\":4,\"localRow\":2},{\"localColumn\":5,\"localRow\":2}],\"minRow\":0,\"maxCol\":5,\"maxRow\":2,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":-1},{\"localColumn\":2,\"localRow\":-1},{\"localColumn\":3,\"localRow\":-1},{\"localColumn\":4,\"localRow\":-1},{\"localColumn\":4,\"localRow\":-2},{\"localColumn\":4,\"localRow\":-3},{\"localColumn\":5,\"localRow\":-3},{\"localColumn\":5,\"localRow\":-2}],\"minRow\":-3,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":0},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":1},{\"localColumn\":2,\"localRow\":1},{\"localColumn\":3,\"localRow\":1},{\"localColumn\":3,\"localRow\":2},{\"localColumn\":3,\"localRow\":3},{\"localColumn\":4,\"localRow\":3},{\"localColumn\":4,\"localRow\":2},{\"localColumn\":5,\"localRow\":2}],\"minRow\":0,\"maxCol\":5,\"maxRow\":3,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":3,\"localRow\":0},{\"localColumn\":4,\"localRow\":0},{\"localColumn\":5,\"localRow\":0},{\"localColumn\":5,\"localRow\":1},{\"localColumn\":5,\"localRow\":2},{\"localColumn\":5,\"localRow\":3},{\"localColumn\":5,\"localRow\":4}],\"minRow\":0,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":4},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":-1},{\"localColumn\":1,\"localRow\":-2},{\"localColumn\":2,\"localRow\":-2},{\"localColumn\":2,\"localRow\":-1},{\"localColumn\":3,\"localRow\":-1},{\"localColumn\":4,\"localRow\":-1},{\"localColumn\":4,\"localRow\":0},{\"localColumn\":5,\"localRow\":0}],\"minRow\":-2,\"maxCol\":5,\"maxRow\":0,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":1},{\"localColumn\":1,\"localRow\":2},{\"localColumn\":2,\"localRow\":2},{\"localColumn\":2,\"localRow\":3},{\"localColumn\":3,\"localRow\":3},{\"localColumn\":4,\"localRow\":3},{\"localColumn\":5,\"localRow\":3},{\"localColumn\":5,\"localRow\":2}],\"minRow\":0,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":3},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":-1},{\"localColumn\":1,\"localRow\":-2},{\"localColumn\":1,\"localRow\":-3},{\"localColumn\":1,\"localRow\":-4},{\"localColumn\":2,\"localRow\":-4},{\"localColumn\":3,\"localRow\":-4},{\"localColumn\":4,\"localRow\":-4},{\"localColumn\":5,\"localRow\":-4}],\"minRow\":-4,\"maxCol\":5,\"maxRow\":0,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":-1},{\"localColumn\":2,\"localRow\":-1},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":3,\"localRow\":0},{\"localColumn\":3,\"localRow\":-1},{\"localColumn\":4,\"localRow\":-1},{\"localColumn\":4,\"localRow\":0},{\"localColumn\":5,\"localRow\":0}],\"minRow\":-1,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":0},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":-1},{\"localColumn\":1,\"localRow\":-2},{\"localColumn\":2,\"localRow\":-2},{\"localColumn\":2,\"localRow\":-1},{\"localColumn\":3,\"localRow\":-1},{\"localColumn\":4,\"localRow\":-1},{\"localColumn\":5,\"localRow\":-1},{\"localColumn\":5,\"localRow\":0}],\"minRow\":-2,\"maxCol\":5,\"maxRow\":0,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":3,\"localRow\":0},{\"localColumn\":4,\"localRow\":0},{\"localColumn\":4,\"localRow\":1},{\"localColumn\":4,\"localRow\":2},{\"localColumn\":4,\"localRow\":3},{\"localColumn\":5,\"localRow\":3},{\"localColumn\":5,\"localRow\":2}],\"minRow\":0,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":3},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":3,\"localRow\":0},{\"localColumn\":3,\"localRow\":-1},{\"localColumn\":4,\"localRow\":-1},{\"localColumn\":4,\"localRow\":0},{\"localColumn\":4,\"localRow\":1},{\"localColumn\":5,\"localRow\":1},{\"localColumn\":5,\"localRow\":0}],\"minRow\":-1,\"maxCol\":5,\"maxRow\":1,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":1},{\"localColumn\":1,\"localRow\":2},{\"localColumn\":2,\"localRow\":2},{\"localColumn\":3,\"localRow\":2},{\"localColumn\":4,\"localRow\":2},{\"localColumn\":5,\"localRow\":2},{\"localColumn\":5,\"localRow\":1},{\"localColumn\":5,\"localRow\":0}],\"minRow\":0,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":2},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":3,\"localRow\":0},{\"localColumn\":3,\"localRow\":1},{\"localColumn\":4,\"localRow\":1},{\"localColumn\":4,\"localRow\":2},{\"localColumn\":4,\"localRow\":3},{\"localColumn\":5,\"localRow\":3},{\"localColumn\":5,\"localRow\":2}],\"minRow\":0,\"maxCol\":5,\"maxRow\":3,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":2,\"localRow\":-1},{\"localColumn\":3,\"localRow\":-1},{\"localColumn\":3,\"localRow\":-2},{\"localColumn\":4,\"localRow\":-2},{\"localColumn\":4,\"localRow\":-3},{\"localColumn\":5,\"localRow\":-3},{\"localColumn\":5,\"localRow\":-4}],\"minRow\":-4,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":0},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":2,\"localRow\":1},{\"localColumn\":3,\"localRow\":1},{\"localColumn\":4,\"localRow\":1},{\"localColumn\":4,\"localRow\":0},{\"localColumn\":5,\"localRow\":0},{\"localColumn\":5,\"localRow\":1}],\"minRow\":0,\"maxCol\":5,\"maxRow\":1,\"minCol\":0,\"length\":9},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":1},{\"localColumn\":1,\"localRow\":2},{\"localColumn\":2,\"localRow\":2},{\"localColumn\":2,\"localRow\":1},{\"localColumn\":3,\"localRow\":1},{\"localColumn\":3,\"localRow\":2},{\"localColumn\":4,\"localRow\":2},{\"localColumn\":5,\"localRow\":2}],\"minRow\":0,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":2},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":1},{\"localColumn\":1,\"localRow\":2},{\"localColumn\":2,\"localRow\":2},{\"localColumn\":3,\"localRow\":2},{\"localColumn\":3,\"localRow\":1},{\"localColumn\":3,\"localRow\":0},{\"localColumn\":4,\"localRow\":0},{\"localColumn\":5,\"localRow\":0}],\"minRow\":0,\"maxCol\":5,\"maxRow\":2,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":1},{\"localColumn\":2,\"localRow\":1},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":3,\"localRow\":0},{\"localColumn\":3,\"localRow\":1},{\"localColumn\":4,\"localRow\":1},{\"localColumn\":5,\"localRow\":1},{\"localColumn\":5,\"localRow\":0}],\"minRow\":0,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":1},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":1},{\"localColumn\":1,\"localRow\":2},{\"localColumn\":2,\"localRow\":2},{\"localColumn\":2,\"localRow\":1},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":3,\"localRow\":0},{\"localColumn\":4,\"localRow\":0},{\"localColumn\":5,\"localRow\":0}],\"minRow\":0,\"maxCol\":5,\"maxRow\":2,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":2,\"localRow\":1},{\"localColumn\":2,\"localRow\":2},{\"localColumn\":2,\"localRow\":3},{\"localColumn\":3,\"localRow\":3},{\"localColumn\":4,\"localRow\":3},{\"localColumn\":5,\"localRow\":3},{\"localColumn\":5,\"localRow\":4}],\"minRow\":0,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":4},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":1},{\"localColumn\":2,\"localRow\":1},{\"localColumn\":3,\"localRow\":1},{\"localColumn\":4,\"localRow\":1},{\"localColumn\":4,\"localRow\":0},{\"localColumn\":5,\"localRow\":0},{\"localColumn\":5,\"localRow\":1},{\"localColumn\":5,\"localRow\":2}],\"minRow\":0,\"maxCol\":5,\"maxRow\":2,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":1},{\"localColumn\":2,\"localRow\":1},{\"localColumn\":2,\"localRow\":2},{\"localColumn\":3,\"localRow\":2},{\"localColumn\":3,\"localRow\":1},{\"localColumn\":4,\"localRow\":1},{\"localColumn\":4,\"localRow\":0},{\"localColumn\":5,\"localRow\":0}],\"minRow\":0,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":2},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":-1},{\"localColumn\":2,\"localRow\":-1},{\"localColumn\":3,\"localRow\":-1},{\"localColumn\":4,\"localRow\":-1},{\"localColumn\":5,\"localRow\":-1},{\"localColumn\":5,\"localRow\":-2},{\"localColumn\":5,\"localRow\":-3},{\"localColumn\":5,\"localRow\":-4}],\"minRow\":-4,\"maxCol\":5,\"maxRow\":0,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":-1},{\"localColumn\":1,\"localRow\":-2},{\"localColumn\":2,\"localRow\":-2},{\"localColumn\":3,\"localRow\":-2},{\"localColumn\":3,\"localRow\":-3},{\"localColumn\":4,\"localRow\":-3},{\"localColumn\":5,\"localRow\":-3},{\"localColumn\":5,\"localRow\":-2}],\"minRow\":-3,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":0},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":1},{\"localColumn\":2,\"localRow\":1},{\"localColumn\":3,\"localRow\":1},{\"localColumn\":4,\"localRow\":1},{\"localColumn\":4,\"localRow\":0},{\"localColumn\":4,\"localRow\":-1},{\"localColumn\":5,\"localRow\":-1},{\"localColumn\":5,\"localRow\":-2}],\"minRow\":-2,\"maxCol\":5,\"maxRow\":1,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":1},{\"localColumn\":2,\"localRow\":1},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":3,\"localRow\":0},{\"localColumn\":4,\"localRow\":0},{\"localColumn\":4,\"localRow\":1},{\"localColumn\":5,\"localRow\":1},{\"localColumn\":5,\"localRow\":2}],\"minRow\":0,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":2},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":1},{\"localColumn\":1,\"localRow\":2},{\"localColumn\":2,\"localRow\":2},{\"localColumn\":3,\"localRow\":2},{\"localColumn\":3,\"localRow\":1},{\"localColumn\":4,\"localRow\":1},{\"localColumn\":5,\"localRow\":1},{\"localColumn\":5,\"localRow\":0}],\"minRow\":0,\"maxCol\":5,\"maxRow\":2,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":2,\"localRow\":1},{\"localColumn\":2,\"localRow\":2},{\"localColumn\":3,\"localRow\":2},{\"localColumn\":3,\"localRow\":1},{\"localColumn\":4,\"localRow\":1},{\"localColumn\":5,\"localRow\":1},{\"localColumn\":5,\"localRow\":0}],\"minRow\":0,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":2},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":2,\"localRow\":0},{\"localColumn\":2,\"localRow\":-1},{\"localColumn\":2,\"localRow\":-2},{\"localColumn\":3,\"localRow\":-2},{\"localColumn\":3,\"localRow\":-3},{\"localColumn\":4,\"localRow\":-3},{\"localColumn\":4,\"localRow\":-4},{\"localColumn\":5,\"localRow\":-4}],\"minRow\":-4,\"maxCol\":5,\"maxRow\":0,\"minCol\":0,\"length\":10},{\"list\":[{\"localColumn\":0,\"localRow\":0},{\"localColumn\":1,\"localRow\":0},{\"localColumn\":1,\"localRow\":-1},{\"localColumn\":2,\"localRow\":-1},{\"localColumn\":3,\"localRow\":-1},{\"localColumn\":4,\"localRow\":-1},{\"localColumn\":4,\"localRow\":0},{\"localColumn\":5,\"localRow\":0},{\"localColumn\":5,\"localRow\":-1},{\"localColumn\":5,\"localRow\":-2}],\"minRow\":-2,\"maxCol\":5,\"length\":10,\"minCol\":0,\"maxRow\":0}]"
```

---

## Activty/baseact/Activity20_MiniGameController.lua.lua
**Functions:**
- PopupGuguGotoSameColorCell
- t.oncomplete
**Requires:**
- Activity20_MiniGameConfigs
- rapidjson
- Activity20_MiniGameConfigs2
- rapidjson
- pathfinder
**Snippet:**
```lua
local ACTIVITY20_MINIGAME_CONFIGS = require("Activity20_MiniGameConfigs")
local NUM_PREVIEW_TYPES = 3
local GUGU_MOVE_SPEED = 5
local GUGU_MOVE_SPEED2 = 3
local GUGU_MOVE_SPEED3 = 4
local pathfinder, worldCenter, grids, gridRows, gridColumns, gridWidth, gridHeight, previewEntries, leftPositions, rightPositions, channels, gugus, tetrominos, guguRandomColors, randomTetrominos, guguIdx, motionTasks, filling, gameOver, elapse, score, winConditions, numRoads, gridsOfRoad, PopupGuguGotoSameColorCell, __oncreatetetromino, __ondestroycell, __oncreatepreviewentry, __oncreatechannel, __oncreategugu, __ondestroygugu, __onreached, __ongameover
local rotatePointAround = function(x, y, angle, aroundx, aroundy)
  local deg = math.rad(angle)
  local cos, sin = math.cos(deg), math.sin(deg)
  local newX = (x - aroundx) * cos - (y - aroundy) * sin + aroundx
```

---

## Activty/baseact/Activity20_MiniGameData.lua.lua
**Functions:**
- Activity20_MiniGameData.SetMiniGameInfo
- Activity20_MiniGameData.GetMiniGameInfo
**Snippet:**
```lua
Activity20_MiniGameData = {gameId = 70441025}
local miniGameInfo

function Activity20_MiniGameData.SetMiniGameInfo(info)
  miniGameInfo = info
end

function Activity20_MiniGameData.GetMiniGameInfo()
  return miniGameInfo
end
```

---

## Activty/baseact/Activity20_MiniGameScriptList.lua.lua
**Requires:**
- Activity20_MiniGameData
- Activity20_MiniGameService
**Snippet:**
```lua
require("Activity20_MiniGameData")
require("Activity20_MiniGameService")
```

---

## Activty/baseact/Activity20_MiniGameService.lua.lua
**Functions:**
- Activity20_MiniGameService.MiniGameInfoReq
- Activity20_MiniGameService.MiniGameInfoRsp
- Activity20_MiniGameService.MiniGameSubmitReq
- Activity20_MiniGameService.MiniGameSubmitRsp
- Activity20_MiniGameService.MiniGameGetDailyRewardReq
- Activity20_MiniGameService.MiniGameGetDailyRewardRsp
- Activity20_MiniGameService.ActivityGetGameTopRankReq
- Activity20_MiniGameService.ActivityGetGameTopRankRsp
- Activity20_MiniGameService.Init
**Snippet:**
```lua
Activity20_MiniGameService = {}
local gameId = Activity20_MiniGameData.gameId

function Activity20_MiniGameService.MiniGameInfoReq(rspCallback)
  local info = ActivityDungeonData.GetActivityInfo()
  local activityId = info.baseInfo.activityId
  Net.Send(Proto.MsgName.ActivityGetMiniGameReq, {gameId = gameId, activityId = activityId}, rspCallback)
end

function Activity20_MiniGameService.MiniGameInfoRsp(msg)
```

---

## Activty/baseact/Activity21BossBattleWindow.lua.lua
**Functions:**
- Activity21BossBattleWindow.ReInitData
- Activity21BossBattleWindow.OnInit
- Activity21BossBattleWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity21BossBattleWindow.FormatRemainTime
- Activity21BossBattleWindow.GetChapter
- Activity21BossBattleWindow.InitBtn
- Activity21BossBattleWindow.CloseWindow
- Activity21BossBattleWindow.OnClose
**Requires:**
- ActivityDungeon1021_BossBattleWindowByName
**Snippet:**
```lua
require("ActivityDungeon1021_BossBattleWindowByName")
local Activity21BossBattleWindow = {}
local uis, contentPane, activityInfo

function Activity21BossBattleWindow.ReInitData()
end

function Activity21BossBattleWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity21BossBattleWindow.package, WinResConfig.Activity21BossBattleWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity21BuyLevelDesWindow.lua.lua
**Functions:**
- Activity21BuyLevelDesWindow.ReInitData
- Activity21BuyLevelDesWindow.OnInit
- Activity21BuyLevelDesWindow.ShowAssetsTips
- Activity21BuyLevelDesWindow.UpdateTextDisplay
- Activity21BuyLevelDesWindow.Init
- Activity21BuyLevelDesWindow.GetGold
- Activity21BuyLevelDesWindow.ShowReward
- list.itemRenderer
- Activity21BuyLevelDesWindow.GetRewardItem
- Activity21BuyLevelDesWindow.GetLvData
- Activity21BuyLevelDesWindow.GetRewardLvData
- Activity21BuyLevelDesWindow.GetRewardByPhaseId
- Activity21BuyLevelDesWindow.BuyLevelRsp
- Activity21BuyLevelDesWindow.InitBtn
- waitFun
- Activity21BuyLevelDesWindow.HandleMessage
- Activity21BuyLevelDesWindow.OnShown
- Activity21BuyLevelDesWindow.OnClose
**Requires:**
- ActivityDungeon1021_BuyLevelDesWindowByName
**Snippet:**
```lua
require("ActivityDungeon1021_BuyLevelDesWindowByName")
local Activity21BuyLevelDesWindow = {}
local uis, contentPane, lvData, curLv, buyNum, itemId, lvMax, waitFun, rewardData, itemSort, transPlay, firstPlay, tatalGold, passInfo

function Activity21BuyLevelDesWindow.ReInitData()
end

function Activity21BuyLevelDesWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity21BuyLevelDesWindow.package, WinResConfig.Activity21BuyLevelDesWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity21ChallengeWindow.lua.lua
**Functions:**
- Activity21ChallengeWindow.ReInitData
- Activity21ChallengeWindow.OnInit
- Activity21ChallengeWindow.UpdateInfo
- uis.Main.ChapterList.itemRenderer
- Activity21ChallengeWindow.ShoweStage
- Activity21ChallengeWindow.StageItemClick
- Activity21ChallengeWindow.ShopInfo
- Activity21ChallengeWindow.GetChapterPassById
- Activity21ChallengeWindow.GetCurStage
- Activity21ChallengeWindow.GetFirstChapter
- Activity21ChallengeWindow.GetAllChapterId
- Activity21ChallengeWindow.InitBtn
- Activity21ChallengeWindow.CloseWindow
- Activity21ChallengeWindow.OnShown
- Activity21ChallengeWindow.OnClose
**Requires:**
- ActivityDungeon1021_ChallengeWindowByName
**Snippet:**
```lua
require("ActivityDungeon1021_ChallengeWindowByName")
local Activity21ChallengeWindow = {}
local uis, contentPane, activityInfo, scrollingTween

function Activity21ChallengeWindow.ReInitData()
end

function Activity21ChallengeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity21ChallengeWindow.package, WinResConfig.Activity21ChallengeWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity21DungeonWindow.lua.lua
**Functions:**
- Activity21DungeonWindow.ReInitData
- Activity21DungeonWindow.OnInit
- Activity21DungeonWindow.LoadBg
- Activity21DungeonWindow.InitRedDot
- Activity21DungeonWindow.UpdateInfo
- Activity21DungeonWindow.InitBtnTxt
- Activity21DungeonWindow.InitBtn
- Activity21DungeonWindow.OnShown
- Activity21DungeonWindow.OnClose
- Activity21DungeonWindow.HandleMessage
**Requires:**
- ActivityDungeon1021_ActivityDungeonWindowByName
**Snippet:**
```lua
require("ActivityDungeon1021_ActivityDungeonWindowByName")
local Activity21DungeonWindow = {}
local uis, contentPane, jumpTb, configData, activityInfo, effect
local InitMiniGameInfo = function()
  local data = ActivityDungeonData.GetActivityData()
  if data.id == 70440021 then
    ld("Activity21_MiniGame", function()
      Activity21_MiniGameService.MiniGameInfoReq(function()
        RedDotMgr.AddNode({
          windowName = WinResConfig.Activity21DungeonWindow.name,
```

---

## Activty/baseact/Activity21MaterialWindow.lua.lua
**Functions:**
- Activity21MaterialWindow.ReInitData
- Activity21MaterialWindow.OnInit
- Activity21MaterialWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity21MaterialWindow.GetChapter
- Activity21MaterialWindow.GetMaxCount
- Activity21MaterialWindow.InitBtn
- Activity21MaterialWindow.CloseWindow
- Activity21MaterialWindow.OnShown
- Activity21MaterialWindow.OnClose
**Requires:**
- ActivityDungeon1021_MaterialWindowByName
**Snippet:**
```lua
require("ActivityDungeon1021_MaterialWindowByName")
local Activity21MaterialWindow = {}
local uis, contentPane, activityInfo, maxCount, posX

function Activity21MaterialWindow.ReInitData()
end

function Activity21MaterialWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity21MaterialWindow.package, WinResConfig.Activity21MaterialWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity21MiniGameMainWindow.lua.lua
**Functions:**
- Activity21MiniGameMainWindow.ReInitData
- Activity21MiniGameMainWindow.OnInit
- Activity21MiniGameMainWindow.UpdateInfo
- Activity21MiniGameMainWindow.InitBtn
- Activity21MiniGameMainWindow.OnClose
- Activity21MiniGameMainWindow.HandleMessage
**Requires:**
- ActivityDungeon1021_MiniGameWindowByName
**Snippet:**
```lua
require("ActivityDungeon1021_MiniGameWindowByName")
local Activity21MiniGameMainWindow = {}
local uis, contentPane
local gameId = 70441026
ld("Activity21_MiniGame")
local RefreshPanel = function()
  local info = Activity21_MiniGameData.GetMiniGameInfo(gameId)
  local conf = TableData.GetConfig(gameId, "BaseActivityStageGame")
  local str = conf.game_day_reward[1]
  local splits = Split(str, ":")
```

---

## Activty/baseact/Activity21MiniGameSubmitWindow.lua.lua
**Functions:**
- Activity21MiniGameSubmitWindow.ReInitData
- Activity21MiniGameSubmitWindow.OnInit
- Activity21MiniGameSubmitWindow.UpdateInfo
- Activity21MiniGameSubmitWindow.InitBtn
- Activity21MiniGameSubmitWindow.OnClose
**Requires:**
- ActivityDungeon1021_MiniStart_EndRewardWindowByName
**Snippet:**
```lua
require("ActivityDungeon1021_MiniStart_EndRewardWindowByName")
local Activity21MiniGameSubmitWindow = {}
local uis, contentPane, score

function Activity21MiniGameSubmitWindow.ReInitData()
end

function Activity21MiniGameSubmitWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity21MiniGameSubmitWindow.package, WinResConfig.Activity21MiniGameSubmitWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity21MiniGameTaskWindow.lua.lua
**Functions:**
- RefreshRewardList
- list.itemRenderer
- itemlist.itemRenderer
- Activity21MiniGameTaskWindow.ReInitData
- Activity21MiniGameTaskWindow.OnInit
- Activity21MiniGameTaskWindow.UpdateInfo
- Activity21MiniGameTaskWindow.InitBtn
- Activity21MiniGameTaskWindow.OnClose
**Requires:**
- ActivityDungeon1021_MiniTaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1021_MiniTaskWindowByName")
local Activity21MiniGameTaskWindow = {}
local uis, contentPane
local gameId = 70441026

local function RefreshRewardList()
  local info = Activity21_MiniGameData.GetMiniGameInfo(gameId)
  local minigame_tasks = info.taskList
  local list = uis.Main.TipsList
  list:SetVirtual()
```

---

## Activty/baseact/Activity21MiniGameWindow.lua.lua
**Functions:**
- Activity21MiniGameWindow.ReInitData
- Activity21MiniGameWindow.OnInit
- Activity21MiniGameWindow.UpdateInfo
- Activity21MiniGameWindow.InitBtn
- Activity21MiniGameWindow.OnClose
- Activity21MiniGameWindow.HandleMessage
**Requires:**
- ActivityDungeon1021_MiniGameStartWindowByName
- Activity21_MiniGameController
- Activity21_MiniGameDelayDestroy
- Activity21_MiniGameConfigs
**Snippet:**
```lua
require("ActivityDungeon1021_MiniGameStartWindowByName")
local Activity21MiniGameWindow = {}
local uis, contentPane
local controller = require("Activity21_MiniGameController")
local GAME_ROWS = 140
local GAME_COLUMNS = 80
local itemObjLookup
local Screen2WorldPosition = function(global)
  local sc = StageCamera.main
  local position = sc:ScreenToWorldPoint(Vector3(global.x, Screen.height - global.y, -sc.transform.position.z))
```

---

## Activty/baseact/Activity21PassportLevelUpTipsWindow.lua.lua
**Functions:**
- Activity21PassportLevelUpTipsWindow.ReInitData
- Activity21PassportLevelUpTipsWindow.OnInit
- Activity21PassportLevelUpTipsWindow.UpdateInfo
- Activity21PassportLevelUpTipsWindow.InitBtn
- Activity21PassportLevelUpTipsWindow.OnClose
**Requires:**
- ActivityDungeon1021_PassportUp_LevelUpTipsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1021_PassportUp_LevelUpTipsWindowByName")
local Activity21PassportLevelUpTipsWindow = {}
local uis, contentPane, lv

function Activity21PassportLevelUpTipsWindow.ReInitData()
end

function Activity21PassportLevelUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity21PassportLevelUpTipsWindow.package, WinResConfig.Activity21PassportLevelUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity21PassportWindow.lua.lua
**Functions:**
- Activity21PassportWindow.ReInitData
- Activity21PassportWindow.OnInit
- Activity21PassportWindow.UpdateTextDisplay
- Activity21PassportWindow.InitPassport
- uis.Main.TabRegion.TabList.itemRenderer
- Activity21PassportWindow.InitEffect
- Activity21PassportWindow.InitLv
- Activity21PassportWindow.ShowLevelUp
- Activity21PassportWindow.SaveLevel
- Activity21PassportWindow.GetRewardByLv
- Activity21PassportWindow.GetRewardNum
- Activity21PassportWindow.IsGetAllReward
- Activity21PassportWindow.ShowReward
- Activity21PassportWindow.GetUpdateLv
- Activity21PassportWindow.RefreshListReward
- Activity21PassportWindow.CheckItemTime
- Activity21PassportWindow.ShowQuitTips
- Activity21PassportWindow.RefreshUI
- Activity21PassportWindow.GetExpMxp
- Activity21PassportWindow.SetLevelInfo
- Activity21PassportWindow.InitList
- list.itemRenderer
- Activity21PassportWindow.SetListPos
- Activity21PassportWindow.RefreshReward
- Activity21PassportWindow.ShowGetEffect
- Activity21PassportWindow.RewardItemClick
- Activity21PassportWindow.IsReward
- Activity21PassportWindow.RefreshRewardFirst
- Activity21PassportWindow.RefreshRewardEnd
- Activity21PassportWindow.ShowState
- Activity21PassportWindow.RefreshRewardShow
- Activity21PassportWindow.RefreshRewardState
- Activity21PassportWindow.PassportActivate
- Activity21PassportWindow.CloseWindow
- Activity21PassportWindow.InitBtn
- Activity21PassportWindow.ShowExpBarAnim
- Activity21PassportWindow.InitTask
- list.itemRenderer
- Activity21PassportWindow.InitClothes
- clothes.BuyReward.RewardList.itemRenderer
- Activity21PassportWindow.SetLastLv
- Activity21PassportWindow.PlayFirstRewardEffect
- Activity21PassportWindow.PlayEndRewardEffect
- Activity21PassportWindow.HandleMessage
- Activity21PassportWindow.OnShown
- Activity21PassportWindow.OnClose
**Requires:**
- ActivityDungeon1021_PassportWindowByName
**Snippet:**
```lua
require("ActivityDungeon1021_PassportWindowByName")
local Activity21PassportWindow = {}
local uis, contentPane, passInfo, lvMax, modelType, expMax, rewardData, rewardType, rewardLv, listPage, passLv, jumpTb, isShowAllGet, passPortConfig, lvTween, lastLv, waitMessageId, newPassPort, animTween

function Activity21PassportWindow.ReInitData()
end

function Activity21PassportWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity21PassportWindow.package, WinResConfig.Activity21PassportWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity21PlotWindow.lua.lua
**Functions:**
- Activity21PlotWindow.ReInitData
- Activity21PlotWindow.OnInit
- Activity21PlotWindow.UpdateInfo
- list.itemRenderer
- Activity21PlotWindow.InitBtn
- Activity21PlotWindow.CloseWindow
- Activity21PlotWindow.OnClose
**Requires:**
- ActivityDungeon1021_PlotWindowByName
**Snippet:**
```lua
require("ActivityDungeon1021_PlotWindowByName")
local Activity21PlotWindow = {}
local uis, contentPane, configData

function Activity21PlotWindow.ReInitData()
end

function Activity21PlotWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity21PlotWindow.package, WinResConfig.Activity21PlotWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity21ShopWindow.lua.lua
**Functions:**
- Activity21ShopWindow.ReInitData
- Activity21ShopWindow.OnInit
- Activity21ShopWindow.UpdateInfo
- uis.Main.ItemList.itemRenderer
- Activity21ShopWindow.ShowItem
- list.itemRenderer
- Activity21ShopWindow.ShowOneReward
- list.itemRenderer
- Activity21ShopWindow.GetShopGrid
- Activity21ShopWindow.InitBtn
- Activity21ShopWindow.CloseWindow
- Activity21ShopWindow.OnClose
- Activity21ShopWindow.HandleMessage
**Requires:**
- ActivityDungeon1021_ShopWindowByName
**Snippet:**
```lua
require("ActivityDungeon1021_ShopWindowByName")
local Activity21ShopWindow = {}
local uis, contentPane, activityInfo, tempAssetsTips

function Activity21ShopWindow.ReInitData()
end

function Activity21ShopWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity21ShopWindow.package, WinResConfig.Activity21ShopWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity21SignWindow.lua.lua
**Functions:**
- Activity21SignWindow.ReInitData
- Activity21SignWindow.OnInit
- Activity21SignWindow.UpdateInfo
- list.RewardList.itemRenderer
- Activity21SignWindow.ShowAllItemFrame
- Activity21SignWindow.GetRewardData
- Activity21SignWindow.InitBtn
- Activity21SignWindow.CloseWindow
- Activity21SignWindow.OnClose
**Requires:**
- ActivityDungeon1021_SignWindowByName
**Snippet:**
```lua
require("ActivityDungeon1021_SignWindowByName")
local Activity21SignWindow = {}
local uis, contentPane, activityInfo

function Activity21SignWindow.ReInitData()
end

function Activity21SignWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity21SignWindow.package, WinResConfig.Activity21SignWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity21TaskWindow.lua.lua
**Functions:**
- Activity21TaskWindow.ReInitData
- Activity21TaskWindow.OnInit
- Activity21TaskWindow.UpdateInfo
- list.itemRenderer
- rewardList.itemRenderer
- Activity21TaskWindow.GetRewardNum
- Activity21TaskWindow.ShowAllItemFrame
- Activity21TaskWindow.SortTask
- Activity21TaskWindow.InitBtn
- Activity21TaskWindow.CloseWindow
- Activity21TaskWindow.OnClose
**Requires:**
- ActivityDungeon1021_TaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1021_TaskWindowByName")
local Activity21TaskWindow = {}
local uis, contentPane

function Activity21TaskWindow.ReInitData()
end

function Activity21TaskWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity21TaskWindow.package, WinResConfig.Activity21TaskWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity21_MiniGameConfigs.lua.lua
**Snippet:**
```lua
return {
  [1] = {
    blocks = {
      {x = 1, y = 1},
      {x = 2, y = 1},
      {x = 1, y = 2},
      {x = 2, y = 2}
    },
    anchor = 1,
    anchorType = 1
```

---

## Activty/baseact/Activity21_MiniGameController.lua.lua
**Functions:**
- BinaryHeap:new
- BinaryHeap:insert
- BinaryHeap:swimUp
- BinaryHeap:compare
- BinaryHeap:swap
- BinaryHeap:peek
- BinaryHeap:removeat
- BinaryHeap:pop
- BinaryHeap:sinkDown
- BinaryHeap:remove
- BinaryHeap:foreach
- BinaryHeap:reset
- CollectNeighborSameColorCells
**Requires:**
- Activity21_MiniGameConfigs
**Snippet:**
```lua
local GRID_WIDTH, GRID_HEIGHT = 0.05, 0.05
local BLOCK_CELL_ROWS, BLOCK_CELL_COLUMN = 8, 8
local TETROMINO_DROP_INTERVAL = 0
local EXTRA_ROWS = 32
local DEFAULT_DROP_SPEED = 2
local PRESS_DROP_SPEED = 8
local PRESS_HORIZONTAL_SPEED = 2
local LONG_PRESS_HORIZONTAL_SPEED = 4
local FLOWING_SPEED = 1
local CELL_STATE = {
```

---

## Activty/baseact/Activity21_MiniGameData.lua.lua
**Snippet:**
```lua
local gameInfo
local SetMiniGameInfo = function(info)
  gameInfo = info
end
local GetMiniGameInfo = function()
  return gameInfo
end
return {SetMiniGameInfo = SetMiniGameInfo, GetMiniGameInfo = GetMiniGameInfo}
```

---

## Activty/baseact/Activity21_MiniGameDelayDestroy.lua.lua
**Functions:**
- OnUpdate
**Snippet:**
```lua
local MAX_COUNT_PER_FRAME_DESTROYED = 20
local gobjs, executing

local function OnUpdate()
  local len = gobjs and #gobjs or 0
  if len > 0 then
    local count = 0
    for _ = len, 1, -1 do
      local gobj = table.remove(gobjs)
      if gobj and not gobj.isDisposed then
```

---

## Activty/baseact/Activity21_MiniGameScriptList.lua.lua
**Requires:**
- Activity21_MiniGameData
- Activity21_MiniGameService
**Snippet:**
```lua
Activity21_MiniGameData = require("Activity21_MiniGameData")
Activity21_MiniGameService = require("Activity21_MiniGameService")
```

---

## Activty/baseact/Activity21_MiniGameService.lua.lua
**Snippet:**
```lua
local gameId = 70441026
local MiniGameInfoReq = function(rspCallback)
  local info = ActivityDungeonData.GetActivityStageByShowId(21)
  local activityId = info.baseInfo.activityId
  Net.Send(Proto.MsgName.ActivityGetMiniGameReq, {activityId = activityId, gameId = gameId}, rspCallback)
end
local MiniGameInfoRsp = function(msg)
  Activity21_MiniGameData.SetMiniGameInfo(msg)
  UIMgr:SendWindowMessage(WinResConfig.Activity21MiniGameMainWindow.name, WindowMsgEnum.Activity21_MiniGame.REFRESH_MINIGAME_INFO)
  UIMgr:SendWindowMessage(WinResConfig.Activity21MiniGameWindow.name, WindowMsgEnum.Activity21_MiniGame.REFRESH_MINIGAME_INFO)
```

---

## Activty/baseact/Activity22BossBattleWindow.lua.lua
**Functions:**
- Activity22BossBattleWindow.ReInitData
- Activity22BossBattleWindow.OnInit
- Activity22BossBattleWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity22BossBattleWindow.FormatRemainTime
- Activity22BossBattleWindow.GetChapter
- Activity22BossBattleWindow.InitBtn
- Activity22BossBattleWindow.CloseWindow
- Activity22BossBattleWindow.OnClose
**Requires:**
- ActivityDungeon1022_BossBattleWindowByName
**Snippet:**
```lua
require("ActivityDungeon1022_BossBattleWindowByName")
local Activity22BossBattleWindow = {}
local uis, contentPane, activityInfo

function Activity22BossBattleWindow.ReInitData()
end

function Activity22BossBattleWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity22BossBattleWindow.package, WinResConfig.Activity22BossBattleWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity22BuyLevelDesWindow.lua.lua
**Functions:**
- Activity22BuyLevelDesWindow.ReInitData
- Activity22BuyLevelDesWindow.OnInit
- Activity22BuyLevelDesWindow.ShowAssetsTips
- Activity22BuyLevelDesWindow.UpdateTextDisplay
- Activity22BuyLevelDesWindow.Init
- Activity22BuyLevelDesWindow.GetGold
- Activity22BuyLevelDesWindow.ShowReward
- list.itemRenderer
- Activity22BuyLevelDesWindow.GetRewardItem
- Activity22BuyLevelDesWindow.GetLvData
- Activity22BuyLevelDesWindow.GetRewardLvData
- Activity22BuyLevelDesWindow.GetRewardByPhaseId
- Activity22BuyLevelDesWindow.BuyLevelRsp
- Activity22BuyLevelDesWindow.InitBtn
- waitFun
- Activity22BuyLevelDesWindow.HandleMessage
- Activity22BuyLevelDesWindow.OnShown
- Activity22BuyLevelDesWindow.OnClose
**Requires:**
- ActivityDungeon1022_BuyLevelDesWindowByName
**Snippet:**
```lua
require("ActivityDungeon1022_BuyLevelDesWindowByName")
local Activity22BuyLevelDesWindow = {}
local uis, contentPane, lvData, curLv, buyNum, itemId, lvMax, waitFun, rewardData, itemSort, transPlay, firstPlay, tatalGold, passInfo

function Activity22BuyLevelDesWindow.ReInitData()
end

function Activity22BuyLevelDesWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity22BuyLevelDesWindow.package, WinResConfig.Activity22BuyLevelDesWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity22ChallengeWindow.lua.lua
**Functions:**
- Activity22ChallengeWindow.ReInitData
- Activity22ChallengeWindow.OnInit
- Activity22ChallengeWindow.UpdateInfo
- uis.Main.ChapterList.itemRenderer
- Activity22ChallengeWindow.ShoweStage
- Activity22ChallengeWindow.StageItemClick
- Activity22ChallengeWindow.ShopInfo
- Activity22ChallengeWindow.GetChapterPassById
- Activity22ChallengeWindow.GetCurStage
- Activity22ChallengeWindow.GetFirstChapter
- Activity22ChallengeWindow.GetAllChapterId
- Activity22ChallengeWindow.InitBtn
- Activity22ChallengeWindow.CloseWindow
- Activity22ChallengeWindow.OnShown
- Activity22ChallengeWindow.OnClose
**Requires:**
- ActivityDungeon1022_ChallengeWindowByName
**Snippet:**
```lua
require("ActivityDungeon1022_ChallengeWindowByName")
local Activity22ChallengeWindow = {}
local uis, contentPane, activityInfo, scrollingTween

function Activity22ChallengeWindow.ReInitData()
end

function Activity22ChallengeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity22ChallengeWindow.package, WinResConfig.Activity22ChallengeWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity22DungeonWindow.lua.lua
**Functions:**
- Activity22DungeonWindow.ReInitData
- Activity22DungeonWindow.OnInit
- Activity22DungeonWindow.LoadBg
- Activity22DungeonWindow.InitRedDot
- Activity22DungeonWindow.UpdateInfo
- Activity22DungeonWindow.InitBtnTxt
- Activity22DungeonWindow.InitBtn
- Activity22DungeonWindow.OnShown
- Activity22DungeonWindow.OnClose
- Activity22DungeonWindow.HandleMessage
**Requires:**
- ActivityDungeon1022_ActivityDungeonWindowByName
**Snippet:**
```lua
require("ActivityDungeon1022_ActivityDungeonWindowByName")
local Activity22DungeonWindow = {}
local uis, contentPane, jumpTb, configData, activityInfo, effect
local InitMiniGameInfo = function()
  local data = ActivityDungeonData.GetActivityData()
  if data.id == 70440022 then
    ld("Activity22_MiniGame", function()
      Activity22_MiniGameService.MiniGameInfoReq(function()
        RedDotMgr.AddNode({
          windowName = WinResConfig.Activity22DungeonWindow.name,
```

---

## Activty/baseact/Activity22MaterialWindow.lua.lua
**Functions:**
- Activity22MaterialWindow.ReInitData
- Activity22MaterialWindow.OnInit
- Activity22MaterialWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity22MaterialWindow.GetChapter
- Activity22MaterialWindow.GetMaxCount
- Activity22MaterialWindow.InitBtn
- Activity22MaterialWindow.CloseWindow
- Activity22MaterialWindow.OnShown
- Activity22MaterialWindow.OnClose
**Requires:**
- ActivityDungeon1022_MaterialWindowByName
**Snippet:**
```lua
require("ActivityDungeon1022_MaterialWindowByName")
local Activity22MaterialWindow = {}
local uis, contentPane, activityInfo, maxCount, posX

function Activity22MaterialWindow.ReInitData()
end

function Activity22MaterialWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity22MaterialWindow.package, WinResConfig.Activity22MaterialWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity22MiniGameMainWindow.lua.lua
**Functions:**
- RefreshPanelInfo
- Activity22MiniGameMainWindow.ReInitData
- Activity22MiniGameMainWindow.OnInit
- Activity22MiniGameMainWindow.UpdateInfo
- Activity22MiniGameMainWindow.InitBtn
- Activity22MiniGameMainWindow.OnClose
- Activity22MiniGameMainWindow.HandleMessage
**Requires:**
- ActivityDungeon1022_MiniGameWindowByName
**Snippet:**
```lua
require("ActivityDungeon1022_MiniGameWindowByName")
ld("Activity22_MiniGame")
local Activity22MiniGameMainWindow = {}
local uis, contentPane

local function RefreshPanelInfo()
  local info = Activity22_MiniGameData.GetMiniGameInfo()
  local conf = TableData.GetConfig(Activity22_MiniGameData.gameId, "BaseActivityStageGame")
  local str = conf.game_day_reward[1]
  local splits = Split(str, ":")
```

---

## Activty/baseact/Activity22MiniGameSubmitWindow.lua.lua
**Functions:**
- Activity22MiniGameSubmitWindow.ReInitData
- Activity22MiniGameSubmitWindow.OnInit
- Activity22MiniGameSubmitWindow.UpdateInfo
- Activity22MiniGameSubmitWindow.InitBtn
- Activity22MiniGameSubmitWindow.OnClose
**Requires:**
- ActivityDungeon1022_MiniStart_EndRewardWindowByName
**Snippet:**
```lua
require("ActivityDungeon1022_MiniStart_EndRewardWindowByName")
local Activity22MiniGameSubmitWindow = {}
local uis, contentPane, stageId

function Activity22MiniGameSubmitWindow.ReInitData()
end

function Activity22MiniGameSubmitWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity22MiniGameSubmitWindow.package, WinResConfig.Activity22MiniGameSubmitWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity22MiniGameTaskWindow.lua.lua
**Functions:**
- RefreshRewardList
- list.itemRenderer
- itemlist.itemRenderer
- Activity22MiniGameTaskWindow.ReInitData
- Activity22MiniGameTaskWindow.OnInit
- Activity22MiniGameTaskWindow.UpdateInfo
- Activity22MiniGameTaskWindow.InitBtn
- Activity22MiniGameTaskWindow.OnClose
**Requires:**
- ActivityDungeon1022_MiniTaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1022_MiniTaskWindowByName")
local Activity22MiniGameTaskWindow = {}
local uis, contentPane

local function RefreshRewardList()
  local info = Activity22_MiniGameData.GetMiniGameInfo()
  local minigame_tasks = info.taskList
  local list = uis.Main.TipsList
  list:SetVirtual()
  
```

---

## Activty/baseact/Activity22MiniGameWindow.lua.lua
**Functions:**
- Activity22MiniGameWindow.ReInitData
- Activity22MiniGameWindow.OnInit
- Activity22MiniGameWindow.UpdateInfo
- Activity22MiniGameWindow.CanHideLine
- Activity22MiniGameWindow.ResetHideLine
- Activity22MiniGameWindow.ResetGrid
- Activity22MiniGameWindow.ShowEffect
- Activity22MiniGameWindow.ShowLineLayer
- Activity22MiniGameWindow.SetItemLine
- Activity22MiniGameWindow.GetGraph
- Activity22MiniGameWindow.IsOldLine
- Activity22MiniGameWindow.ShowLine
- Activity22MiniGameWindow.CheckGameOver
- Activity22MiniGameWindow.RemoveGridColor
- Activity22MiniGameWindow.AddLineGrid
- Activity22MiniGameWindow.GetCellAtPosition
- Activity22MiniGameWindow.ShowColorBlack
- Activity22MiniGameWindow.LoadLine
- Activity22MiniGameWindow.IsAdjacent
- Activity22MiniGameWindow.GenerateItem
- Activity22MiniGameWindow.GetMapRoot
- Activity22MiniGameWindow.RandomItem
- Activity22MiniGameWindow.GetCurDifficulty
- Activity22MiniGameWindow.RemoveLine
- Activity22MiniGameWindow.Next
- Activity22MiniGameWindow.GetLineCom
- Activity22MiniGameWindow.HideLineCom
- Activity22MiniGameWindow.InitBtn
- Activity22MiniGameWindow.HandleMessage
- Activity22MiniGameWindow.OnClose
**Requires:**
- ActivityDungeon1022_MiniGameStartWindowByName
**Snippet:**
```lua
require("ActivityDungeon1022_MiniGameStartWindowByName")
local Activity22MiniGameWindow = {}
local uis, contentPane
local gameId = 70441027
local mapGridInfo, mapRoot, lineCom, lineComPool, cellLineList, curLineColor
local pageGridCtr = {
  [4] = 0,
  [5] = 1,
  [6] = 2,
  [7] = 3
```

---

## Activty/baseact/Activity22PassportLevelUpTipsWindow.lua.lua
**Functions:**
- Activity22PassportLevelUpTipsWindow.ReInitData
- Activity22PassportLevelUpTipsWindow.OnInit
- Activity22PassportLevelUpTipsWindow.UpdateInfo
- Activity22PassportLevelUpTipsWindow.InitBtn
- Activity22PassportLevelUpTipsWindow.OnClose
**Requires:**
- ActivityDungeon1022_PassportUp_LevelUpTipsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1022_PassportUp_LevelUpTipsWindowByName")
local Activity22PassportLevelUpTipsWindow = {}
local uis, contentPane, lv

function Activity22PassportLevelUpTipsWindow.ReInitData()
end

function Activity22PassportLevelUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity22PassportLevelUpTipsWindow.package, WinResConfig.Activity22PassportLevelUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity22PassportWindow.lua.lua
**Functions:**
- Activity22PassportWindow.ReInitData
- Activity22PassportWindow.OnInit
- Activity22PassportWindow.UpdateTextDisplay
- Activity22PassportWindow.InitPassport
- uis.Main.TabRegion.TabList.itemRenderer
- Activity22PassportWindow.InitEffect
- Activity22PassportWindow.InitLv
- Activity22PassportWindow.ShowLevelUp
- Activity22PassportWindow.SaveLevel
- Activity22PassportWindow.GetRewardByLv
- Activity22PassportWindow.GetRewardNum
- Activity22PassportWindow.IsGetAllReward
- Activity22PassportWindow.ShowReward
- Activity22PassportWindow.GetUpdateLv
- Activity22PassportWindow.RefreshListReward
- Activity22PassportWindow.CheckItemTime
- Activity22PassportWindow.ShowQuitTips
- Activity22PassportWindow.RefreshUI
- Activity22PassportWindow.GetExpMxp
- Activity22PassportWindow.SetLevelInfo
- Activity22PassportWindow.InitList
- list.itemRenderer
- Activity22PassportWindow.SetListPos
- Activity22PassportWindow.RefreshReward
- Activity22PassportWindow.ShowGetEffect
- Activity22PassportWindow.RewardItemClick
- Activity22PassportWindow.IsReward
- Activity22PassportWindow.RefreshRewardFirst
- Activity22PassportWindow.RefreshRewardEnd
- Activity22PassportWindow.ShowState
- Activity22PassportWindow.RefreshRewardShow
- Activity22PassportWindow.RefreshRewardState
- Activity22PassportWindow.PassportActivate
- Activity22PassportWindow.CloseWindow
- Activity22PassportWindow.InitBtn
- Activity22PassportWindow.ShowExpBarAnim
- Activity22PassportWindow.InitTask
- list.itemRenderer
- Activity22PassportWindow.InitClothes
- clothes.BuyReward.RewardList.itemRenderer
- Activity22PassportWindow.SetLastLv
- Activity22PassportWindow.PlayFirstRewardEffect
- Activity22PassportWindow.PlayEndRewardEffect
- Activity22PassportWindow.HandleMessage
- Activity22PassportWindow.OnShown
- Activity22PassportWindow.OnClose
**Requires:**
- ActivityDungeon1022_PassportWindowByName
**Snippet:**
```lua
require("ActivityDungeon1022_PassportWindowByName")
local Activity22PassportWindow = {}
local uis, contentPane, passInfo, lvMax, modelType, expMax, rewardData, rewardType, rewardLv, listPage, passLv, jumpTb, isShowAllGet, passPortConfig, lvTween, lastLv, waitMessageId, newPassPort, animTween

function Activity22PassportWindow.ReInitData()
end

function Activity22PassportWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity22PassportWindow.package, WinResConfig.Activity22PassportWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity22PlotWindow.lua.lua
**Functions:**
- Activity22PlotWindow.ReInitData
- Activity22PlotWindow.OnInit
- Activity22PlotWindow.UpdateInfo
- list.itemRenderer
- Activity22PlotWindow.InitBtn
- Activity22PlotWindow.CloseWindow
- Activity22PlotWindow.OnClose
**Requires:**
- ActivityDungeon1022_PlotWindowByName
**Snippet:**
```lua
require("ActivityDungeon1022_PlotWindowByName")
local Activity22PlotWindow = {}
local uis, contentPane, configData

function Activity22PlotWindow.ReInitData()
end

function Activity22PlotWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity22PlotWindow.package, WinResConfig.Activity22PlotWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity22ShopWindow.lua.lua
**Functions:**
- Activity22ShopWindow.ReInitData
- Activity22ShopWindow.OnInit
- Activity22ShopWindow.UpdateInfo
- uis.Main.ItemList.itemRenderer
- Activity22ShopWindow.ShowItem
- list.itemRenderer
- Activity22ShopWindow.ShowOneReward
- list.itemRenderer
- Activity22ShopWindow.GetShopGrid
- Activity22ShopWindow.InitBtn
- Activity22ShopWindow.CloseWindow
- Activity22ShopWindow.OnClose
- Activity22ShopWindow.HandleMessage
**Requires:**
- ActivityDungeon1022_ShopWindowByName
**Snippet:**
```lua
require("ActivityDungeon1022_ShopWindowByName")
local Activity22ShopWindow = {}
local uis, contentPane, activityInfo, tempAssetsTips

function Activity22ShopWindow.ReInitData()
end

function Activity22ShopWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity22ShopWindow.package, WinResConfig.Activity22ShopWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity22SignWindow.lua.lua
**Functions:**
- Activity22SignWindow.ReInitData
- Activity22SignWindow.OnInit
- Activity22SignWindow.UpdateInfo
- list.RewardList.itemRenderer
- Activity22SignWindow.ShowAllItemFrame
- Activity22SignWindow.GetRewardData
- Activity22SignWindow.InitBtn
- Activity22SignWindow.CloseWindow
- Activity22SignWindow.OnClose
**Requires:**
- ActivityDungeon1022_SignWindowByName
**Snippet:**
```lua
require("ActivityDungeon1022_SignWindowByName")
local Activity22SignWindow = {}
local uis, contentPane, activityInfo

function Activity22SignWindow.ReInitData()
end

function Activity22SignWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity22SignWindow.package, WinResConfig.Activity22SignWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity22TaskWindow.lua.lua
**Functions:**
- Activity22TaskWindow.ReInitData
- Activity22TaskWindow.OnInit
- Activity22TaskWindow.UpdateInfo
- list.itemRenderer
- rewardList.itemRenderer
- Activity22TaskWindow.GetRewardNum
- Activity22TaskWindow.ShowAllItemFrame
- Activity22TaskWindow.SortTask
- Activity22TaskWindow.InitBtn
- Activity22TaskWindow.CloseWindow
- Activity22TaskWindow.OnClose
**Requires:**
- ActivityDungeon1022_TaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1022_TaskWindowByName")
local Activity22TaskWindow = {}
local uis, contentPane

function Activity22TaskWindow.ReInitData()
end

function Activity22TaskWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity22TaskWindow.package, WinResConfig.Activity22TaskWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity22_MiniGameData.lua.lua
**Functions:**
- Activity22_MiniGameData.SetMiniGameInfo
- Activity22_MiniGameData.GetMiniGameInfo
**Snippet:**
```lua
Activity22_MiniGameData = {gameId = 70441027}
local miniGameInfo

function Activity22_MiniGameData.SetMiniGameInfo(info)
  miniGameInfo = info
end

function Activity22_MiniGameData.GetMiniGameInfo()
  return miniGameInfo
end
```

---

## Activty/baseact/Activity22_MiniGameScriptList.lua.lua
**Requires:**
- Activity22_MiniGameData
- Activity22_MiniGameService
**Snippet:**
```lua
require("Activity22_MiniGameData")
require("Activity22_MiniGameService")
```

---

## Activty/baseact/Activity22_MiniGameService.lua.lua
**Functions:**
- Activity22_MiniGameService.MiniGameInfoReq
- Activity22_MiniGameService.MiniGameInfoRsp
- Activity22_MiniGameService.MiniGameSubmitReq
- Activity22_MiniGameService.MiniGameSubmitRsp
- Activity22_MiniGameService.MiniGameGetDailyRewardReq
- Activity22_MiniGameService.MiniGameGetDailyRewardRsp
- Activity22_MiniGameService.ActivityGetGameTopRankReq
- Activity22_MiniGameService.ActivityGetGameTopRankRsp
- Activity22_MiniGameService.Init
**Snippet:**
```lua
Activity22_MiniGameService = {}
local gameId = Activity22_MiniGameData.gameId

function Activity22_MiniGameService.MiniGameInfoReq(rspCallback)
  local info = ActivityDungeonData.GetActivityInfo()
  local activityId = info.baseInfo.activityId
  Net.Send(Proto.MsgName.ActivityGetMiniGameReq, {gameId = gameId, activityId = activityId}, rspCallback)
end

function Activity22_MiniGameService.MiniGameInfoRsp(msg)
```

---

## Activty/baseact/Activity2BossBattleWindow.lua.lua
**Functions:**
- Activity2BossBattleWindow.ReInitData
- Activity2BossBattleWindow.OnInit
- Activity2BossBattleWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity2BossBattleWindow.FormatRemainTime
- Activity2BossBattleWindow.GetChapter
- Activity2BossBattleWindow.InitBtn
- Activity2BossBattleWindow.CloseWindow
- Activity2BossBattleWindow.OnClose
**Requires:**
- ActivityDungeon1001_BossBattleWindowByName
**Snippet:**
```lua
require("ActivityDungeon1001_BossBattleWindowByName")
local Activity2BossBattleWindow = {}
local uis, contentPane, activityInfo

function Activity2BossBattleWindow.ReInitData()
end

function Activity2BossBattleWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity2BossBattleWindow.package, WinResConfig.Activity2BossBattleWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity2BuyLevelDesWindow.lua.lua
**Functions:**
- Activity2BuyLevelDesWindow.ReInitData
- Activity2BuyLevelDesWindow.OnInit
- Activity2BuyLevelDesWindow.ShowAssetsTips
- Activity2BuyLevelDesWindow.UpdateTextDisplay
- Activity2BuyLevelDesWindow.Init
- Activity2BuyLevelDesWindow.GetGold
- Activity2BuyLevelDesWindow.ShowReward
- list.itemRenderer
- Activity2BuyLevelDesWindow.GetRewardItem
- Activity2BuyLevelDesWindow.GetLvData
- Activity2BuyLevelDesWindow.GetRewardLvData
- Activity2BuyLevelDesWindow.GetRewardByPhaseId
- Activity2BuyLevelDesWindow.BuyLevelRsp
- Activity2BuyLevelDesWindow.InitBtn
- waitFun
- Activity2BuyLevelDesWindow.HandleMessage
- Activity2BuyLevelDesWindow.OnShown
- Activity2BuyLevelDesWindow.OnClose
**Requires:**
- ActivityDungeon1001_BuyLevelDesWindowByName
**Snippet:**
```lua
require("ActivityDungeon1001_BuyLevelDesWindowByName")
local Activity2BuyLevelDesWindow = {}
local uis, contentPane, lvData, curLv, buyNum, itemId, lvMax, waitFun, rewardData, itemSort, transPlay, firstPlay, tatalGold, passInfo

function Activity2BuyLevelDesWindow.ReInitData()
end

function Activity2BuyLevelDesWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity2BuyLevelDesWindow.package, WinResConfig.Activity2BuyLevelDesWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity2ChallengeWindow.lua.lua
**Functions:**
- Activity2ChallengeWindow.ReInitData
- Activity2ChallengeWindow.OnInit
- Activity2ChallengeWindow.UpdateInfo
- uis.Main.ChapterList.itemRenderer
- Activity2ChallengeWindow.ShoweStage
- Activity2ChallengeWindow.StageItemClick
- Activity2ChallengeWindow.ShopInfo
- Activity2ChallengeWindow.GetChapterPassById
- Activity2ChallengeWindow.GetCurStage
- Activity2ChallengeWindow.GetFirstChapter
- Activity2ChallengeWindow.GetAllChapterId
- Activity2ChallengeWindow.InitBtn
- Activity2ChallengeWindow.CloseWindow
- Activity2ChallengeWindow.OnShown
- Activity2ChallengeWindow.OnClose
**Requires:**
- ActivityDungeon1001_ChallengeWindowByName
**Snippet:**
```lua
require("ActivityDungeon1001_ChallengeWindowByName")
local Activity2ChallengeWindow = {}
local uis, contentPane, activityInfo, scrollingTween

function Activity2ChallengeWindow.ReInitData()
end

function Activity2ChallengeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity2ChallengeWindow.package, WinResConfig.Activity2ChallengeWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity2DungeonWindow.lua.lua
**Functions:**
- Activity2DungeonWindow.ReInitData
- Activity2DungeonWindow.OnInit
- Activity2DungeonWindow.LoadBg
- Activity2DungeonWindow.InitRedDot
- Activity2DungeonWindow.UpdateInfo
- Activity2DungeonWindow.InitBtnTxt
- Activity2DungeonWindow.InitBtn
- Activity2DungeonWindow.OnShown
- Activity2DungeonWindow.OnClose
- Activity2DungeonWindow.HandleMessage
**Requires:**
- ActivityDungeon1001_ActivityDungeonWindowByName
**Snippet:**
```lua
require("ActivityDungeon1001_ActivityDungeonWindowByName")
local Activity2DungeonWindow = {}
local uis, contentPane, jumpTb, configData, activityInfo, effect
local InitMiniGameInfo = function()
  local data = ActivityDungeonData.GetActivityData()
  if data.id == 70440001 then
    ld("Activity1_MiniGame")
    Activity1_MiniGameService.MiniGameInfoReq(function()
      RedDotMgr.AddNode({
        windowName = WinResConfig.Activity2DungeonWindow.name,
```

---

## Activty/baseact/Activity2MaterialWindow.lua.lua
**Functions:**
- Activity2MaterialWindow.ReInitData
- Activity2MaterialWindow.OnInit
- Activity2MaterialWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity2MaterialWindow.GetChapter
- Activity2MaterialWindow.GetMaxCount
- Activity2MaterialWindow.InitBtn
- Activity2MaterialWindow.CloseWindow
- Activity2MaterialWindow.OnShown
- Activity2MaterialWindow.OnClose
**Requires:**
- ActivityDungeon1001_MaterialWindowByName
**Snippet:**
```lua
require("ActivityDungeon1001_MaterialWindowByName")
local Activity2MaterialWindow = {}
local uis, contentPane, activityInfo, maxCount, posX

function Activity2MaterialWindow.ReInitData()
end

function Activity2MaterialWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity2MaterialWindow.package, WinResConfig.Activity2MaterialWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity2MiniGameMainWindow.lua.lua
**Functions:**
- RefreshPanelInfo
- Activity2MiniGameMainWindow.ReInitData
- Activity2MiniGameMainWindow.OnInit
- Activity2MiniGameMainWindow.UpdateInfo
- Activity2MiniGameMainWindow.InitBtn
- Activity2MiniGameMainWindow.OnClose
- Activity2MiniGameMainWindow.HandleMessage
**Requires:**
- ActivityDungeon1001_MiniGameWindowByName
**Snippet:**
```lua
require("ActivityDungeon1001_MiniGameWindowByName")
ld("Activity2_MiniGame")
local Activity2MiniGameMainWindow = {}
local uis, contentPane

local function RefreshPanelInfo()
  local highestScoreTxt = T(20524)
  local info = Activity2_MiniGameData.GetMiniGameInfo()
  local conf = ActivityDungeonData.GetActivityData()
  local str = conf.game_day_reward[1]
```

---

## Activty/baseact/Activity2MiniGameRecordWindow.lua.lua
**Functions:**
- Activity2MiniGameRecordWindow.ReInitData
- Activity2MiniGameRecordWindow.OnInit
- Activity2MiniGameRecordWindow.UpdateInfo
- list.itemRenderer
- Activity2MiniGameRecordWindow.InitBtn
- Activity2MiniGameRecordWindow.OnClose
**Requires:**
- ActivityDungeon1001_MiniIntegralWindowByName
**Snippet:**
```lua
require("ActivityDungeon1001_MiniIntegralWindowByName")
local Activity2MiniGameRecordWindow = {}
local uis, contentPane

function Activity2MiniGameRecordWindow.ReInitData()
end

function Activity2MiniGameRecordWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity2MiniGameRecordWindow.package, WinResConfig.Activity2MiniGameRecordWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity2MiniGameSubmitWindow.lua.lua
**Functions:**
- Activity2MiniGameSubmitWindow.ReInitData
- Activity2MiniGameSubmitWindow.OnInit
- Activity2MiniGameSubmitWindow.UpdateInfo
- Activity2MiniGameSubmitWindow.InitBtn
- Activity2MiniGameSubmitWindow.OnClose
**Requires:**
- ActivityDungeon1001_MiniStart_EndRewardWindowByName
**Snippet:**
```lua
require("ActivityDungeon1001_MiniStart_EndRewardWindowByName")
local Activity2MiniGameSubmitWindow = {}
local uis, contentPane, score, consumeSeconds

function Activity2MiniGameSubmitWindow.ReInitData()
end

function Activity2MiniGameSubmitWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity2MiniGameSubmitWindow.package, WinResConfig.Activity2MiniGameSubmitWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity2MiniGameTaskWindow.lua.lua
**Functions:**
- RefreshRewardList
- list.itemRenderer
- itemlist.itemRenderer
- Activity2MiniGameTaskWindow.ReInitData
- Activity2MiniGameTaskWindow.OnInit
- Activity2MiniGameTaskWindow.UpdateInfo
- Activity2MiniGameTaskWindow.InitBtn
- Activity2MiniGameTaskWindow.OnClose
**Requires:**
- ActivityDungeon1001_MiniTaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1001_MiniTaskWindowByName")
local Activity2MiniGameTaskWindow = {}
local uis, contentPane

local function RefreshRewardList()
  local info = Activity2_MiniGameData.GetMiniGameInfo()
  local minigame_tasks = info.taskList
  local list = uis.Main.TipsList
  list:SetVirtual()
  
```

---

## Activty/baseact/Activity2MiniGameWindow.lua.lua
**Functions:**
- Activity2MiniGameWindow.ReInitData
- Activity2MiniGameWindow.OnInit
- Activity2MiniGameWindow.UpdateInfo
- Activity2MiniGameWindow.InitBtn
- Activity2MiniGameWindow.OnClose
- Activity2MiniGameWindow.HandleMessage
**Requires:**
- ActivityDungeon1001_MiniGameStartWindowByName
- Activity2_MiniGameController
**Snippet:**
```lua
require("ActivityDungeon1001_MiniGameStartWindowByName")
local FRUIT_LEVEL_ASSET_LOOKUP = {
  [1] = "ui://ActivityDungeon1001/Vegetable_1001",
  [2] = "ui://ActivityDungeon1001/Vegetable_1002",
  [3] = "ui://ActivityDungeon1001/Vegetable_1003",
  [4] = "ui://ActivityDungeon1001/Vegetable_1004",
  [5] = "ui://ActivityDungeon1001/Vegetable_1005",
  [6] = "ui://ActivityDungeon1001/Vegetable_1006",
  [7] = "ui://ActivityDungeon1001/Vegetable_1007",
  [8] = "ui://ActivityDungeon1001/Vegetable_1008",
```

---

## Activty/baseact/Activity2PassportLevelUpTipsWindow.lua.lua
**Functions:**
- Activity2PassportLevelUpTipsWindow.ReInitData
- Activity2PassportLevelUpTipsWindow.OnInit
- Activity2PassportLevelUpTipsWindow.UpdateInfo
- Activity2PassportLevelUpTipsWindow.InitBtn
- Activity2PassportLevelUpTipsWindow.OnClose
**Requires:**
- ActivityDungeon1001_PassportUp_LevelUpTipsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1001_PassportUp_LevelUpTipsWindowByName")
local Activity2PassportLevelUpTipsWindow = {}
local uis, contentPane, lv

function Activity2PassportLevelUpTipsWindow.ReInitData()
end

function Activity2PassportLevelUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity2PassportLevelUpTipsWindow.package, WinResConfig.Activity2PassportLevelUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity2PassportWindow.lua.lua
**Functions:**
- Activity2PassportWindow.ReInitData
- Activity2PassportWindow.OnInit
- Activity2PassportWindow.UpdateTextDisplay
- Activity2PassportWindow.InitPassport
- uis.Main.TabRegion.TabList.itemRenderer
- Activity2PassportWindow.InitEffect
- Activity2PassportWindow.InitLv
- Activity2PassportWindow.ShowLevelUp
- Activity2PassportWindow.SaveLevel
- Activity2PassportWindow.GetRewardByLv
- Activity2PassportWindow.GetRewardNum
- Activity2PassportWindow.IsGetAllReward
- Activity2PassportWindow.ShowReward
- Activity2PassportWindow.GetUpdateLv
- Activity2PassportWindow.RefreshListReward
- Activity2PassportWindow.CheckItemTime
- Activity2PassportWindow.ShowQuitTips
- Activity2PassportWindow.RefreshUI
- Activity2PassportWindow.GetExpMxp
- Activity2PassportWindow.SetLevelInfo
- Activity2PassportWindow.InitList
- list.itemRenderer
- Activity2PassportWindow.SetListPos
- Activity2PassportWindow.RefreshReward
- Activity2PassportWindow.ShowGetEffect
- Activity2PassportWindow.RewardItemClick
- Activity2PassportWindow.IsReward
- Activity2PassportWindow.RefreshRewardFirst
- Activity2PassportWindow.RefreshRewardEnd
- Activity2PassportWindow.ShowState
- Activity2PassportWindow.RefreshRewardShow
- Activity2PassportWindow.RefreshRewardState
- Activity2PassportWindow.PassportActivate
- Activity2PassportWindow.CloseWindow
- Activity2PassportWindow.InitBtn
- Activity2PassportWindow.ShowExpBarAnim
- Activity2PassportWindow.InitTask
- list.itemRenderer
- Activity2PassportWindow.InitClothes
- clothes.BuyReward.RewardList.itemRenderer
- Activity2PassportWindow.SetLastLv
- Activity2PassportWindow.PlayFirstRewardEffect
- Activity2PassportWindow.PlayEndRewardEffect
- Activity2PassportWindow.HandleMessage
- Activity2PassportWindow.OnShown
- Activity2PassportWindow.OnClose
**Requires:**
- ActivityDungeon1001_PassportWindowByName
**Snippet:**
```lua
require("ActivityDungeon1001_PassportWindowByName")
local Activity2PassportWindow = {}
local uis, contentPane, passInfo, lvMax, modelType, expMax, rewardData, rewardType, rewardLv, listPage, passLv, jumpTb, isShowAllGet, passPortConfig, lvTween, lastLv, waitMessageId, newPassPort, animTween

function Activity2PassportWindow.ReInitData()
end

function Activity2PassportWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity2PassportWindow.package, WinResConfig.Activity2PassportWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity2PlotWindow.lua.lua
**Functions:**
- Activity2PlotWindow.ReInitData
- Activity2PlotWindow.OnInit
- Activity2PlotWindow.UpdateInfo
- list.itemRenderer
- Activity2PlotWindow.InitBtn
- Activity2PlotWindow.CloseWindow
- Activity2PlotWindow.OnClose
**Requires:**
- ActivityDungeon1001_PlotWindowByName
**Snippet:**
```lua
require("ActivityDungeon1001_PlotWindowByName")
local Activity2PlotWindow = {}
local uis, contentPane, configData

function Activity2PlotWindow.ReInitData()
end

function Activity2PlotWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity2PlotWindow.package, WinResConfig.Activity2PlotWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity2ShopWindow.lua.lua
**Functions:**
- Activity2ShopWindow.ReInitData
- Activity2ShopWindow.OnInit
- Activity2ShopWindow.UpdateInfo
- uis.Main.ItemList.itemRenderer
- Activity2ShopWindow.ShowItem
- list.itemRenderer
- Activity2ShopWindow.ShowOneReward
- list.itemRenderer
- Activity2ShopWindow.GetShopGrid
- Activity2ShopWindow.InitBtn
- Activity2ShopWindow.CloseWindow
- Activity2ShopWindow.OnClose
- Activity2ShopWindow.HandleMessage
**Requires:**
- ActivityDungeon1001_ShopWindowByName
**Snippet:**
```lua
require("ActivityDungeon1001_ShopWindowByName")
local Activity2ShopWindow = {}
local uis, contentPane, activityInfo, tempAssetsTips

function Activity2ShopWindow.ReInitData()
end

function Activity2ShopWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity2ShopWindow.package, WinResConfig.Activity2ShopWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity2SignWindow.lua.lua
**Functions:**
- Activity2SignWindow.ReInitData
- Activity2SignWindow.OnInit
- Activity2SignWindow.UpdateInfo
- list.RewardList.itemRenderer
- Activity2SignWindow.ShowAllItemFrame
- Activity2SignWindow.GetRewardData
- Activity2SignWindow.InitBtn
- Activity2SignWindow.CloseWindow
- Activity2SignWindow.OnClose
**Requires:**
- ActivityDungeon1001_SignWindowByName
**Snippet:**
```lua
require("ActivityDungeon1001_SignWindowByName")
local Activity2SignWindow = {}
local uis, contentPane, activityInfo

function Activity2SignWindow.ReInitData()
end

function Activity2SignWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity2SignWindow.package, WinResConfig.Activity2SignWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity2TaskWindow.lua.lua
**Functions:**
- Activity2TaskWindow.ReInitData
- Activity2TaskWindow.OnInit
- Activity2TaskWindow.UpdateInfo
- list.itemRenderer
- rewardList.itemRenderer
- Activity2TaskWindow.GetRewardNum
- Activity2TaskWindow.ShowAllItemFrame
- Activity2TaskWindow.SortTask
- Activity2TaskWindow.InitBtn
- Activity2TaskWindow.CloseWindow
- Activity2TaskWindow.OnClose
**Requires:**
- ActivityDungeon1001_TaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1001_TaskWindowByName")
local Activity2TaskWindow = {}
local uis, contentPane

function Activity2TaskWindow.ReInitData()
end

function Activity2TaskWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity2TaskWindow.package, WinResConfig.Activity2TaskWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity2_Fruit8_Presets.lua.lua
**Snippet:**
```lua
local new_v2_list = CS.System.Collections.Generic.List(CS.UnityEngine.Vector2)
local list = new_v2_list(28)
list:Add(Vector2(164.1783, -87.00164))
list:Add(Vector2(155.029526, -80.25895))
list:Add(Vector2(166.652435, -42.3600349))
list:Add(Vector2(166.6852, -36.89))
list:Add(Vector2(146.0351, -43.7830238))
list:Add(Vector2(137.735443, -23.2959576))
list:Add(Vector2(120.557419, -3.30014634))
list:Add(Vector2(98.8335648, -3.54116821))
```

---

## Activty/baseact/Activity2_MiniGameController.lua.lua
**Functions:**
- Collision2DEnterCallback
- Collision2DStayCallback
- Trigger2DEnterCallback
- Trigger2DStayCallback
- Trigger2DExitCallback
**Requires:**
- PhysicsScriptList
**Snippet:**
```lua
local MAX_FRUIT_LEVEL = 11
local THICKNESS_OF_WALL = 2
local THICKNESS_OF_GAME_OVER_LINE = 0.02
local CONTAINER_ORIGIN = Vector3(0, 0, 0)
local CONTAINER_WIDTH, CONTAINER_HEIGHT = 5.28, 7.4
local FRUIT_LEVEL_COLLIDER_SETTINGS_LOOKUP = {
  [1] = {
    offset = Vector2(27, -27),
    radius = 27,
    radius_offset = 0,
```

---

## Activty/baseact/Activity2_MiniGameData.lua.lua
**Snippet:**
```lua
local miniGameInfo
local SetMiniGameInfo = function(info)
  miniGameInfo = info
end
local GetMiniGameInfo = function()
  return miniGameInfo
end
return {SetMiniGameInfo = SetMiniGameInfo, GetMiniGameInfo = GetMiniGameInfo}
```

---

## Activty/baseact/Activity2_MiniGameScriptList.lua.lua
**Requires:**
- Activity2_MiniGameData
- Activity2_MiniGameService
- Activity2_MiniGameController
**Snippet:**
```lua
Activity2_MiniGameData = require("Activity2_MiniGameData")
Activity2_MiniGameService = require("Activity2_MiniGameService")
Activity2_MiniGameController = require("Activity2_MiniGameController")
```

---

## Activty/baseact/Activity2_MiniGameService.lua.lua
**Snippet:**
```lua
local gameId = 70441002
local MiniGameInfoReq = function(rspCallback)
  local info = ActivityDungeonData.GetActivityInfo()
  local activityId = info.baseInfo.activityId
  Net.Send(Proto.MsgName.ActivityGetMiniGameReq, {gameId = gameId, activityId = activityId}, rspCallback)
end
local MiniGameInfoRsp = function(msg)
  Activity2_MiniGameData.SetMiniGameInfo(msg)
  UIMgr:SendWindowMessage(WinResConfig.Activity2MiniGameMainWindow.name, WindowMsgEnum.Activity2_MiniGame.REFRESH_MINIGAME_INFO)
  UIMgr:SendWindowMessage(WinResConfig.Activity2MiniGameWindow.name, WindowMsgEnum.Activity2_MiniGame.REFRESH_MINIGAME_INFO)
```

---

## Activty/baseact/Activity3BossBattleWindow.lua.lua
**Functions:**
- Activity3BossBattleWindow.ReInitData
- Activity3BossBattleWindow.OnInit
- Activity3BossBattleWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity3BossBattleWindow.FormatRemainTime
- Activity3BossBattleWindow.GetChapter
- Activity3BossBattleWindow.InitBtn
- Activity3BossBattleWindow.CloseWindow
- Activity3BossBattleWindow.OnClose
**Requires:**
- ActivityDungeon1002_BossBattleWindowByName
**Snippet:**
```lua
require("ActivityDungeon1002_BossBattleWindowByName")
local Activity3BossBattleWindow = {}
local uis, contentPane, activityInfo

function Activity3BossBattleWindow.ReInitData()
end

function Activity3BossBattleWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity3BossBattleWindow.package, WinResConfig.Activity3BossBattleWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity3BuyLevelDesWindow.lua.lua
**Functions:**
- Activity3BuyLevelDesWindow.ReInitData
- Activity3BuyLevelDesWindow.OnInit
- Activity3BuyLevelDesWindow.ShowAssetsTips
- Activity3BuyLevelDesWindow.UpdateTextDisplay
- Activity3BuyLevelDesWindow.Init
- Activity3BuyLevelDesWindow.GetGold
- Activity3BuyLevelDesWindow.ShowReward
- list.itemRenderer
- Activity3BuyLevelDesWindow.GetRewardItem
- Activity3BuyLevelDesWindow.GetLvData
- Activity3BuyLevelDesWindow.GetRewardLvData
- Activity3BuyLevelDesWindow.GetRewardByPhaseId
- Activity3BuyLevelDesWindow.BuyLevelRsp
- Activity3BuyLevelDesWindow.InitBtn
- waitFun
- Activity3BuyLevelDesWindow.HandleMessage
- Activity3BuyLevelDesWindow.OnShown
- Activity3BuyLevelDesWindow.OnClose
**Requires:**
- ActivityDungeon1002_BuyLevelDesWindowByName
**Snippet:**
```lua
require("ActivityDungeon1002_BuyLevelDesWindowByName")
local Activity3BuyLevelDesWindow = {}
local uis, contentPane, lvData, curLv, buyNum, itemId, lvMax, waitFun, rewardData, itemSort, transPlay, firstPlay, tatalGold, passInfo

function Activity3BuyLevelDesWindow.ReInitData()
end

function Activity3BuyLevelDesWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity3BuyLevelDesWindow.package, WinResConfig.Activity3BuyLevelDesWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity3ChallengeWindow.lua.lua
**Functions:**
- Activity3ChallengeWindow.ReInitData
- Activity3ChallengeWindow.OnInit
- Activity3ChallengeWindow.UpdateInfo
- uis.Main.ChapterList.itemRenderer
- Activity3ChallengeWindow.ShoweStage
- Activity3ChallengeWindow.StageItemClick
- Activity3ChallengeWindow.ShopInfo
- Activity3ChallengeWindow.GetChapterPassById
- Activity3ChallengeWindow.GetCurStage
- Activity3ChallengeWindow.GetFirstChapter
- Activity3ChallengeWindow.GetAllChapterId
- Activity3ChallengeWindow.InitBtn
- Activity3ChallengeWindow.CloseWindow
- Activity3ChallengeWindow.OnShown
- Activity3ChallengeWindow.OnClose
**Requires:**
- ActivityDungeon1002_ChallengeWindowByName
**Snippet:**
```lua
require("ActivityDungeon1002_ChallengeWindowByName")
local Activity3ChallengeWindow = {}
local uis, contentPane, activityInfo, scrollingTween

function Activity3ChallengeWindow.ReInitData()
end

function Activity3ChallengeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity3ChallengeWindow.package, WinResConfig.Activity3ChallengeWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity3DungeonWindow.lua.lua
**Functions:**
- Activity3DungeonWindow.ReInitData
- Activity3DungeonWindow.OnInit
- Activity3DungeonWindow.LoadBg
- Activity3DungeonWindow.InitRedDot
- Activity3DungeonWindow.UpdateInfo
- Activity3DungeonWindow.InitBtnTxt
- Activity3DungeonWindow.InitBtn
- Activity3DungeonWindow.OnShown
- Activity3DungeonWindow.OnClose
- Activity3DungeonWindow.HandleMessage
**Requires:**
- ActivityDungeon1002_ActivityDungeonWindowByName
**Snippet:**
```lua
require("ActivityDungeon1002_ActivityDungeonWindowByName")
local Activity3DungeonWindow = {}
local uis, contentPane, jumpTb, configData, activityInfo, effect
local InitMiniGameInfo = function()
  local data = ActivityDungeonData.GetActivityData()
  if data.id == 70440001 then
    ld("Activity1_MiniGame")
    Activity1_MiniGameService.MiniGameInfoReq(function()
      RedDotMgr.AddNode({
        windowName = WinResConfig.Activity3DungeonWindow.name,
```

---

## Activty/baseact/Activity3MaterialWindow.lua.lua
**Functions:**
- Activity3MaterialWindow.ReInitData
- Activity3MaterialWindow.OnInit
- Activity3MaterialWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity3MaterialWindow.GetChapter
- Activity3MaterialWindow.GetMaxCount
- Activity3MaterialWindow.InitBtn
- Activity3MaterialWindow.CloseWindow
- Activity3MaterialWindow.OnShown
- Activity3MaterialWindow.OnClose
**Requires:**
- ActivityDungeon1002_MaterialWindowByName
**Snippet:**
```lua
require("ActivityDungeon1002_MaterialWindowByName")
local Activity3MaterialWindow = {}
local uis, contentPane, activityInfo, maxCount, posX

function Activity3MaterialWindow.ReInitData()
end

function Activity3MaterialWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity3MaterialWindow.package, WinResConfig.Activity3MaterialWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity3MiniGameMainWindow.lua.lua
**Functions:**
- RefreshPanelInfo
- Activity3MiniGameMainWindow.ReInitData
- Activity3MiniGameMainWindow.OnInit
- Activity3MiniGameMainWindow.UpdateInfo
- Activity3MiniGameMainWindow.InitBtn
- Activity3MiniGameMainWindow.OnClose
- Activity3MiniGameMainWindow.HandleMessage
**Requires:**
- ActivityDungeon1002_MiniGameWindowByName
**Snippet:**
```lua
require("ActivityDungeon1002_MiniGameWindowByName")
ld("Activity3_MiniGame")
local Activity3MiniGameMainWindow = {}
local uis, contentPane

local function RefreshPanelInfo()
  local info = Activity3_MiniGameData.GetMiniGameInfo()
  local conf = ActivityDungeonData.GetActivityData()
  local str = conf.game_day_reward[1]
  local splits = Split(str, ":")
```

---

## Activty/baseact/Activity3MiniGameRecordWindow.lua.lua
**Functions:**
- Activity3MiniGameRecordWindow.ReInitData
- Activity3MiniGameRecordWindow.OnInit
- Activity3MiniGameRecordWindow.UpdateInfo
- list.itemRenderer
- Activity3MiniGameRecordWindow.InitBtn
- Activity3MiniGameRecordWindow.OnClose
**Requires:**
- ActivityDungeon1002_MiniIntegralWindowByName
**Snippet:**
```lua
require("ActivityDungeon1002_MiniIntegralWindowByName")
local Activity3MiniGameRecordWindow = {}
local uis, contentPane

function Activity3MiniGameRecordWindow.ReInitData()
end

function Activity3MiniGameRecordWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity3MiniGameRecordWindow.package, WinResConfig.Activity3MiniGameRecordWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity3MiniGameSubmitWindow.lua.lua
**Functions:**
- Activity3MiniGameSubmitWindow.ReInitData
- Activity3MiniGameSubmitWindow.OnInit
- Activity3MiniGameSubmitWindow.UpdateInfo
- Activity3MiniGameSubmitWindow.InitBtn
- Activity3MiniGameSubmitWindow.OnClose
**Requires:**
- ActivityDungeon1002_MiniStart_EndRewardWindowByName
**Snippet:**
```lua
require("ActivityDungeon1002_MiniStart_EndRewardWindowByName")
local Activity3MiniGameSubmitWindow = {}
local uis, contentPane

function Activity3MiniGameSubmitWindow.ReInitData()
end

function Activity3MiniGameSubmitWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity3MiniGameSubmitWindow.package, WinResConfig.Activity3MiniGameSubmitWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity3MiniGameTaskWindow.lua.lua
**Functions:**
- RefreshRewardList
- list.itemRenderer
- itemlist.itemRenderer
- Activity3MiniGameTaskWindow.ReInitData
- Activity3MiniGameTaskWindow.OnInit
- Activity3MiniGameTaskWindow.UpdateInfo
- Activity3MiniGameTaskWindow.InitBtn
- Activity3MiniGameTaskWindow.OnClose
**Requires:**
- ActivityDungeon1002_MiniTaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1002_MiniTaskWindowByName")
local Activity3MiniGameTaskWindow = {}
local uis, contentPane

local function RefreshRewardList()
  local info = Activity3_MiniGameData.GetMiniGameInfo()
  local minigame_tasks = info.taskList
  local list = uis.Main.TipsList
  list:SetVirtual()
  
```

---

## Activty/baseact/Activity3MiniGameWindow.lua.lua
**Functions:**
- Activity3MiniGameWindow.ReInitData
- Activity3MiniGameWindow.OnInit
- Activity3MiniGameWindow.UpdateInfo
- Activity3MiniGameWindow.InitMap
- Activity3MiniGameWindow.GetCurDifficulty
- Activity3MiniGameWindow.CreateStartLine
- Activity3MiniGameWindow.CreateMap
- Activity3MiniGameWindow.StartRandomRotation
- Activity3MiniGameWindow.GameOverAmin
- Activity3MiniGameWindow.UpdateLine
- Activity3MiniGameWindow.GetLen
- Activity3MiniGameWindow.CheckSpecialBol
- Activity3MiniGameWindow.UpdateRotationCtrPage
- Activity3MiniGameWindow.CheckLinePlayMusice
- Activity3MiniGameWindow.CheckConnectLine
- Activity3MiniGameWindow.CanCheck
- Activity3MiniGameWindow.GetGridByType
- Activity3MiniGameWindow.InitLine
- Activity3MiniGameWindow.ShowLatticeLine
- Activity3MiniGameWindow.OnGameOver
- Activity3MiniGameWindow.OnNext
- Activity3MiniGameWindow.ResetUI
- Activity3MiniGameWindow.InitBtn
- Activity3MiniGameWindow.OnClose
- Activity3MiniGameWindow.HandleMessage
**Requires:**
- ActivityDungeon1002_MiniGameStartWindowByName
**Snippet:**
```lua
require("ActivityDungeon1002_MiniGameStartWindowByName")
local Activity3MiniGameWindow = {}
local uis, contentPane
local mapW = 7
local mapH = 4
local mapAddH = 5
local map = {}
local mapIndex = {}
local tempMap = {}
local endPosRandom = {}
```

---

## Activty/baseact/Activity3PassportLevelUpTipsWindow.lua.lua
**Functions:**
- Activity3PassportLevelUpTipsWindow.ReInitData
- Activity3PassportLevelUpTipsWindow.OnInit
- Activity3PassportLevelUpTipsWindow.UpdateInfo
- Activity3PassportLevelUpTipsWindow.InitBtn
- Activity3PassportLevelUpTipsWindow.OnClose
**Requires:**
- ActivityDungeon1002_PassportUp_LevelUpTipsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1002_PassportUp_LevelUpTipsWindowByName")
local Activity3PassportLevelUpTipsWindow = {}
local uis, contentPane, lv

function Activity3PassportLevelUpTipsWindow.ReInitData()
end

function Activity3PassportLevelUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity3PassportLevelUpTipsWindow.package, WinResConfig.Activity3PassportLevelUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity3PassportWindow.lua.lua
**Functions:**
- Activity3PassportWindow.ReInitData
- Activity3PassportWindow.OnInit
- Activity3PassportWindow.UpdateTextDisplay
- Activity3PassportWindow.InitPassport
- uis.Main.TabRegion.TabList.itemRenderer
- Activity3PassportWindow.InitEffect
- Activity3PassportWindow.InitLv
- Activity3PassportWindow.ShowLevelUp
- Activity3PassportWindow.SaveLevel
- Activity3PassportWindow.GetRewardByLv
- Activity3PassportWindow.GetRewardNum
- Activity3PassportWindow.IsGetAllReward
- Activity3PassportWindow.ShowReward
- Activity3PassportWindow.GetUpdateLv
- Activity3PassportWindow.RefreshListReward
- Activity3PassportWindow.CheckItemTime
- Activity3PassportWindow.ShowQuitTips
- Activity3PassportWindow.RefreshUI
- Activity3PassportWindow.GetExpMxp
- Activity3PassportWindow.SetLevelInfo
- Activity3PassportWindow.InitList
- list.itemRenderer
- Activity3PassportWindow.SetListPos
- Activity3PassportWindow.RefreshReward
- Activity3PassportWindow.ShowGetEffect
- Activity3PassportWindow.RewardItemClick
- Activity3PassportWindow.IsReward
- Activity3PassportWindow.RefreshRewardFirst
- Activity3PassportWindow.RefreshRewardEnd
- Activity3PassportWindow.ShowState
- Activity3PassportWindow.RefreshRewardShow
- Activity3PassportWindow.RefreshRewardState
- Activity3PassportWindow.PassportActivate
- Activity3PassportWindow.CloseWindow
- Activity3PassportWindow.InitBtn
- Activity3PassportWindow.ShowExpBarAnim
- Activity3PassportWindow.InitTask
- list.itemRenderer
- Activity3PassportWindow.InitClothes
- clothes.BuyReward.RewardList.itemRenderer
- Activity3PassportWindow.SetLastLv
- Activity3PassportWindow.PlayFirstRewardEffect
- Activity3PassportWindow.PlayEndRewardEffect
- Activity3PassportWindow.HandleMessage
- Activity3PassportWindow.OnShown
- Activity3PassportWindow.OnClose
**Requires:**
- ActivityDungeon1002_PassportWindowByName
**Snippet:**
```lua
require("ActivityDungeon1002_PassportWindowByName")
local Activity3PassportWindow = {}
local uis, contentPane, passInfo, lvMax, modelType, expMax, rewardData, rewardType, rewardLv, listPage, passLv, jumpTb, isShowAllGet, passPortConfig, lvTween, lastLv, waitMessageId, newPassPort, animTween

function Activity3PassportWindow.ReInitData()
end

function Activity3PassportWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity3PassportWindow.package, WinResConfig.Activity3PassportWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity3PlotWindow.lua.lua
**Functions:**
- Activity3PlotWindow.ReInitData
- Activity3PlotWindow.OnInit
- Activity3PlotWindow.UpdateInfo
- list.itemRenderer
- Activity3PlotWindow.InitBtn
- Activity3PlotWindow.CloseWindow
- Activity3PlotWindow.OnClose
**Requires:**
- ActivityDungeon1002_PlotWindowByName
**Snippet:**
```lua
require("ActivityDungeon1002_PlotWindowByName")
local Activity3PlotWindow = {}
local uis, contentPane, configData

function Activity3PlotWindow.ReInitData()
end

function Activity3PlotWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity3PlotWindow.package, WinResConfig.Activity3PlotWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity3ShopWindow.lua.lua
**Functions:**
- Activity3ShopWindow.ReInitData
- Activity3ShopWindow.OnInit
- Activity3ShopWindow.UpdateInfo
- uis.Main.ItemList.itemRenderer
- Activity3ShopWindow.ShowItem
- list.itemRenderer
- Activity3ShopWindow.ShowOneReward
- list.itemRenderer
- Activity3ShopWindow.GetShopGrid
- Activity3ShopWindow.InitBtn
- Activity3ShopWindow.CloseWindow
- Activity3ShopWindow.OnClose
- Activity3ShopWindow.HandleMessage
**Requires:**
- ActivityDungeon1002_ShopWindowByName
**Snippet:**
```lua
require("ActivityDungeon1002_ShopWindowByName")
local Activity3ShopWindow = {}
local uis, contentPane, activityInfo, tempAssetsTips

function Activity3ShopWindow.ReInitData()
end

function Activity3ShopWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity3ShopWindow.package, WinResConfig.Activity3ShopWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity3SignWindow.lua.lua
**Functions:**
- Activity3SignWindow.ReInitData
- Activity3SignWindow.OnInit
- Activity3SignWindow.UpdateInfo
- list.RewardList.itemRenderer
- Activity3SignWindow.ShowAllItemFrame
- Activity3SignWindow.GetRewardData
- Activity3SignWindow.InitBtn
- Activity3SignWindow.CloseWindow
- Activity3SignWindow.OnClose
**Requires:**
- ActivityDungeon1002_SignWindowByName
**Snippet:**
```lua
require("ActivityDungeon1002_SignWindowByName")
local Activity3SignWindow = {}
local uis, contentPane, activityInfo

function Activity3SignWindow.ReInitData()
end

function Activity3SignWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity3SignWindow.package, WinResConfig.Activity3SignWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity3TaskWindow.lua.lua
**Functions:**
- Activity3TaskWindow.ReInitData
- Activity3TaskWindow.OnInit
- Activity3TaskWindow.UpdateInfo
- list.itemRenderer
- rewardList.itemRenderer
- Activity3TaskWindow.GetRewardNum
- Activity3TaskWindow.ShowAllItemFrame
- Activity3TaskWindow.SortTask
- Activity3TaskWindow.InitBtn
- Activity3TaskWindow.CloseWindow
- Activity3TaskWindow.OnClose
**Requires:**
- ActivityDungeon1002_TaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1002_TaskWindowByName")
local Activity3TaskWindow = {}
local uis, contentPane

function Activity3TaskWindow.ReInitData()
end

function Activity3TaskWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity3TaskWindow.package, WinResConfig.Activity3TaskWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity3_MiniGameData.lua.lua
**Functions:**
- Activity3_MiniGameData.SetMiniGameInfo
- Activity3_MiniGameData.GetMiniGameInfo
**Snippet:**
```lua
Activity3_MiniGameData = {}
local miniGameInfo

function Activity3_MiniGameData.SetMiniGameInfo(info)
  miniGameInfo = info
end

function Activity3_MiniGameData.GetMiniGameInfo()
  return miniGameInfo
end
```

---

## Activty/baseact/Activity3_MiniGameScriptList.lua.lua
**Requires:**
- Activity3_MiniGameData
- Activity3_MiniGameService
**Snippet:**
```lua
require("Activity3_MiniGameData")
require("Activity3_MiniGameService")
```

---

## Activty/baseact/Activity3_MiniGameService.lua.lua
**Functions:**
- Activity3_MiniGameService.MiniGameInfoReq
- Activity3_MiniGameService.MiniGameInfoRsp
- Activity3_MiniGameService.MiniGameSubmitReq
- Activity3_MiniGameService.MiniGameSubmitRsp
- Activity3_MiniGameService.MiniGameGetDailyRewardReq
- Activity3_MiniGameService.MiniGameGetDailyRewardRsp
- Activity3_MiniGameService.Init
**Snippet:**
```lua
Activity3_MiniGameService = {}
local gameId = 70441003

function Activity3_MiniGameService.MiniGameInfoReq(rspCallback)
  local info = ActivityDungeonData.GetActivityInfo()
  local activityId = info.baseInfo.activityId
  Net.Send(Proto.MsgName.ActivityGetMiniGameReq, {gameId = gameId, activityId = activityId}, rspCallback)
end

function Activity3_MiniGameService.MiniGameInfoRsp(msg)
```

---

## Activty/baseact/Activity4BossBattleWindow.lua.lua
**Functions:**
- Activity4BossBattleWindow.ReInitData
- Activity4BossBattleWindow.OnInit
- Activity4BossBattleWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity4BossBattleWindow.FormatRemainTime
- Activity4BossBattleWindow.GetChapter
- Activity4BossBattleWindow.InitBtn
- Activity4BossBattleWindow.CloseWindow
- Activity4BossBattleWindow.OnClose
**Requires:**
- ActivityDungeon1003_BossBattleWindowByName
**Snippet:**
```lua
require("ActivityDungeon1003_BossBattleWindowByName")
local Activity4BossBattleWindow = {}
local uis, contentPane, activityInfo

function Activity4BossBattleWindow.ReInitData()
end

function Activity4BossBattleWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity4BossBattleWindow.package, WinResConfig.Activity4BossBattleWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity4BuyLevelDesWindow.lua.lua
**Functions:**
- Activity4BuyLevelDesWindow.ReInitData
- Activity4BuyLevelDesWindow.OnInit
- Activity4BuyLevelDesWindow.ShowAssetsTips
- Activity4BuyLevelDesWindow.UpdateTextDisplay
- Activity4BuyLevelDesWindow.Init
- Activity4BuyLevelDesWindow.GetGold
- Activity4BuyLevelDesWindow.ShowReward
- list.itemRenderer
- Activity4BuyLevelDesWindow.GetRewardItem
- Activity4BuyLevelDesWindow.GetLvData
- Activity4BuyLevelDesWindow.GetRewardLvData
- Activity4BuyLevelDesWindow.GetRewardByPhaseId
- Activity4BuyLevelDesWindow.BuyLevelRsp
- Activity4BuyLevelDesWindow.InitBtn
- waitFun
- Activity4BuyLevelDesWindow.HandleMessage
- Activity4BuyLevelDesWindow.OnShown
- Activity4BuyLevelDesWindow.OnClose
**Requires:**
- ActivityDungeon1003_BuyLevelDesWindowByName
**Snippet:**
```lua
require("ActivityDungeon1003_BuyLevelDesWindowByName")
local Activity4BuyLevelDesWindow = {}
local uis, contentPane, lvData, curLv, buyNum, itemId, lvMax, waitFun, rewardData, itemSort, transPlay, firstPlay, tatalGold, passInfo

function Activity4BuyLevelDesWindow.ReInitData()
end

function Activity4BuyLevelDesWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity4BuyLevelDesWindow.package, WinResConfig.Activity4BuyLevelDesWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity4ChallengeWindow.lua.lua
**Functions:**
- Activity4ChallengeWindow.ReInitData
- Activity4ChallengeWindow.OnInit
- Activity4ChallengeWindow.UpdateInfo
- uis.Main.ChapterList.itemRenderer
- Activity4ChallengeWindow.ShoweStage
- Activity4ChallengeWindow.StageItemClick
- Activity4ChallengeWindow.ShopInfo
- Activity4ChallengeWindow.GetChapterPassById
- Activity4ChallengeWindow.GetCurStage
- Activity4ChallengeWindow.GetFirstChapter
- Activity4ChallengeWindow.GetAllChapterId
- Activity4ChallengeWindow.InitBtn
- Activity4ChallengeWindow.CloseWindow
- Activity4ChallengeWindow.OnShown
- Activity4ChallengeWindow.OnClose
**Requires:**
- ActivityDungeon1003_ChallengeWindowByName
**Snippet:**
```lua
require("ActivityDungeon1003_ChallengeWindowByName")
local Activity4ChallengeWindow = {}
local uis, contentPane, activityInfo, scrollingTween

function Activity4ChallengeWindow.ReInitData()
end

function Activity4ChallengeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity4ChallengeWindow.package, WinResConfig.Activity4ChallengeWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity4DungeonWindow.lua.lua
**Functions:**
- Activity4DungeonWindow.ReInitData
- Activity4DungeonWindow.OnInit
- Activity4DungeonWindow.LoadBg
- Activity4DungeonWindow.InitRedDot
- Activity4DungeonWindow.UpdateInfo
- Activity4DungeonWindow.InitBtnTxt
- Activity4DungeonWindow.InitBtn
- Activity4DungeonWindow.OnShown
- Activity4DungeonWindow.OnClose
- Activity4DungeonWindow.HandleMessage
**Requires:**
- ActivityDungeon1003_ActivityDungeonWindowByName
**Snippet:**
```lua
require("ActivityDungeon1003_ActivityDungeonWindowByName")
local Activity4DungeonWindow = {}
local uis, contentPane, jumpTb, configData, activityInfo, effect
local InitMiniGameInfo = function()
  local data = ActivityDungeonData.GetActivityData()
  if data.id == 70440001 then
    ld("Activity1_MiniGame")
    Activity1_MiniGameService.MiniGameInfoReq(function()
      RedDotMgr.AddNode({
        windowName = WinResConfig.Activity4DungeonWindow.name,
```

---

## Activty/baseact/Activity4MaterialWindow.lua.lua
**Functions:**
- Activity4MaterialWindow.ReInitData
- Activity4MaterialWindow.OnInit
- Activity4MaterialWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity4MaterialWindow.GetChapter
- Activity4MaterialWindow.GetMaxCount
- Activity4MaterialWindow.InitBtn
- Activity4MaterialWindow.CloseWindow
- Activity4MaterialWindow.OnShown
- Activity4MaterialWindow.OnClose
**Requires:**
- ActivityDungeon1003_MaterialWindowByName
**Snippet:**
```lua
require("ActivityDungeon1003_MaterialWindowByName")
local Activity4MaterialWindow = {}
local uis, contentPane, activityInfo, maxCount, posX

function Activity4MaterialWindow.ReInitData()
end

function Activity4MaterialWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity4MaterialWindow.package, WinResConfig.Activity4MaterialWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity4MiniGameCountdownWindow.lua.lua
**Functions:**
- Activity4MiniGameCountdownWindow.ReInitData
- Activity4MiniGameCountdownWindow.OnInit
- Activity4MiniGameCountdownWindow.UpdateInfo
- Activity4MiniGameCountdownWindow.InitBtn
- Activity4MiniGameCountdownWindow.OnClose
- Activity4MiniGameCountdownWindow.HandleMessage
**Requires:**
- ActivityDungeon1003_MiniStart_CountdownWindowByName
**Snippet:**
```lua
require("ActivityDungeon1003_MiniStart_CountdownWindowByName")
local Activity4MiniGameCountdownWindow = {}
local uis, contentPane

function Activity4MiniGameCountdownWindow.ReInitData()
end

function Activity4MiniGameCountdownWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity4MiniGameCountdownWindow.package, WinResConfig.Activity4MiniGameCountdownWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity4MiniGameMainWindow.lua.lua
**Functions:**
- RefreshPanelInfo
- Activity4MiniGameMainWindow.ReInitData
- Activity4MiniGameMainWindow.OnInit
- Activity4MiniGameMainWindow.UpdateInfo
- Activity4MiniGameMainWindow.InitBtn
- Activity4MiniGameMainWindow.OnClose
- Activity4MiniGameMainWindow.HandleMessage
**Requires:**
- ActivityDungeon1003_MiniGameWindowByName
**Snippet:**
```lua
require("ActivityDungeon1003_MiniGameWindowByName")
ld("Activity4_MiniGame")
local Activity4MiniGameMainWindow = {}
local uis, contentPane

local function RefreshPanelInfo()
  local info = Activity4_MiniGameData.GetMiniGameInfo()
  local conf = ActivityDungeonData.GetActivityData()
  local str = conf.game_day_reward[1]
  local splits = Split(str, ":")
```

---

## Activty/baseact/Activity4MiniGameRecordWindow.lua.lua
**Functions:**
- Activity4MiniGameRecordWindow.ReInitData
- Activity4MiniGameRecordWindow.OnInit
- Activity4MiniGameRecordWindow.UpdateInfo
- list.itemRenderer
- Activity4MiniGameRecordWindow.InitBtn
- Activity4MiniGameRecordWindow.OnClose
**Requires:**
- ActivityDungeon1003_MiniIntegralWindowByName
**Snippet:**
```lua
require("ActivityDungeon1003_MiniIntegralWindowByName")
local Activity4MiniGameRecordWindow = {}
local uis, contentPane

function Activity4MiniGameRecordWindow.ReInitData()
end

function Activity4MiniGameRecordWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity4MiniGameRecordWindow.package, WinResConfig.Activity4MiniGameRecordWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity4MiniGameSubmitWindow.lua.lua
**Functions:**
- Activity4MiniGameSubmitWindow.ReInitData
- Activity4MiniGameSubmitWindow.OnInit
- Activity4MiniGameSubmitWindow.UpdateInfo
- Activity4MiniGameSubmitWindow.InitBtn
- Activity4MiniGameSubmitWindow.OnClose
**Requires:**
- ActivityDungeon1003_MiniStart_EndRewardWindowByName
**Snippet:**
```lua
require("ActivityDungeon1003_MiniStart_EndRewardWindowByName")
local Activity4MiniGameSubmitWindow = {}
local uis, contentPane, nowIntegral, consumeSeconds

function Activity4MiniGameSubmitWindow.ReInitData()
end

function Activity4MiniGameSubmitWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity4MiniGameSubmitWindow.package, WinResConfig.Activity4MiniGameSubmitWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity4MiniGameTaskWindow.lua.lua
**Functions:**
- RefreshRewardList
- list.itemRenderer
- itemlist.itemRenderer
- Activity4MiniGameTaskWindow.ReInitData
- Activity4MiniGameTaskWindow.OnInit
- Activity4MiniGameTaskWindow.UpdateInfo
- Activity4MiniGameTaskWindow.InitBtn
- Activity4MiniGameTaskWindow.OnClose
**Requires:**
- ActivityDungeon1003_MiniTaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1003_MiniTaskWindowByName")
local Activity4MiniGameTaskWindow = {}
local uis, contentPane

local function RefreshRewardList()
  local info = Activity4_MiniGameData.GetMiniGameInfo()
  local minigame_tasks = info.taskList
  local list = uis.Main.TipsList
  list:SetVirtual()
  
```

---

## Activty/baseact/Activity4MiniGameWindow.lua.lua
**Functions:**
- Activity4MiniGameWindow.ReInitData
- Activity4MiniGameWindow.OnInit
- Activity4MiniGameWindow.UpdateInfo
- Activity4MiniGameWindow.UpdateBuffNum
- list.itemRenderer
- Activity4MiniGameWindow.CreateItem
- Activity4MiniGameWindow.ItemNew
- item:move
- item:catch
- Activity4MiniGameWindow.GetItemPos
- Activity4MiniGameWindow.CheckContain
- Activity4MiniGameWindow.Update
- Activity4MiniGameWindow.MoveItemGuGu
- Activity4MiniGameWindow.MoveClaw
- Activity4MiniGameWindow.Finish
- Activity4MiniGameWindow.CheckBuffAlpha
- Activity4MiniGameWindow.PlayEffect
- Activity4MiniGameWindow.DisposeEffect
- Activity4MiniGameWindow.RemoveHavePoint
- Activity4MiniGameWindow.AddBoxBuff
- Activity4MiniGameWindow.CheckGetItem
- Activity4MiniGameWindow.GetGameTime
- Activity4MiniGameWindow.RotationClaw
- Activity4MiniGameWindow.OnGameOver
- Activity4MiniGameWindow.Overlaps
- Activity4MiniGameWindow.OnNext
- Activity4MiniGameWindow.GetCurDifficulty
- Activity4MiniGameWindow.InitBtn
- Activity4MiniGameWindow.OnClose
- Activity4MiniGameWindow.HandleMessage
**Requires:**
- ActivityDungeon1003_MiniGameStartWindowByName
**Snippet:**
```lua
require("ActivityDungeon1003_MiniGameStartWindowByName")
local Activity4MiniGameWindow = {}
local uis, contentPane
local leftRotation = 70
local rightRotation = -70
local clawSpeed = 60
local curRot = 0
local totalGameTime = 60
local nowDir
local RotaDir = {left = 0, right = 1}
```

---

## Activty/baseact/Activity4PassportLevelUpTipsWindow.lua.lua
**Functions:**
- Activity4PassportLevelUpTipsWindow.ReInitData
- Activity4PassportLevelUpTipsWindow.OnInit
- Activity4PassportLevelUpTipsWindow.UpdateInfo
- Activity4PassportLevelUpTipsWindow.InitBtn
- Activity4PassportLevelUpTipsWindow.OnClose
**Requires:**
- ActivityDungeon1003_PassportUp_LevelUpTipsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1003_PassportUp_LevelUpTipsWindowByName")
local Activity4PassportLevelUpTipsWindow = {}
local uis, contentPane, lv

function Activity4PassportLevelUpTipsWindow.ReInitData()
end

function Activity4PassportLevelUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity4PassportLevelUpTipsWindow.package, WinResConfig.Activity4PassportLevelUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity4PassportWindow.lua.lua
**Functions:**
- Activity4PassportWindow.ReInitData
- Activity4PassportWindow.OnInit
- Activity4PassportWindow.UpdateTextDisplay
- Activity4PassportWindow.InitPassport
- uis.Main.TabRegion.TabList.itemRenderer
- Activity4PassportWindow.InitEffect
- Activity4PassportWindow.InitLv
- Activity4PassportWindow.ShowLevelUp
- Activity4PassportWindow.SaveLevel
- Activity4PassportWindow.GetRewardByLv
- Activity4PassportWindow.GetRewardNum
- Activity4PassportWindow.IsGetAllReward
- Activity4PassportWindow.ShowReward
- Activity4PassportWindow.GetUpdateLv
- Activity4PassportWindow.RefreshListReward
- Activity4PassportWindow.CheckItemTime
- Activity4PassportWindow.ShowQuitTips
- Activity4PassportWindow.RefreshUI
- Activity4PassportWindow.GetExpMxp
- Activity4PassportWindow.SetLevelInfo
- Activity4PassportWindow.InitList
- list.itemRenderer
- Activity4PassportWindow.SetListPos
- Activity4PassportWindow.RefreshReward
- Activity4PassportWindow.ShowGetEffect
- Activity4PassportWindow.RewardItemClick
- Activity4PassportWindow.IsReward
- Activity4PassportWindow.RefreshRewardFirst
- Activity4PassportWindow.RefreshRewardEnd
- Activity4PassportWindow.ShowState
- Activity4PassportWindow.RefreshRewardShow
- Activity4PassportWindow.RefreshRewardState
- Activity4PassportWindow.PassportActivate
- Activity4PassportWindow.CloseWindow
- Activity4PassportWindow.InitBtn
- Activity4PassportWindow.ShowExpBarAnim
- Activity4PassportWindow.InitTask
- list.itemRenderer
- Activity4PassportWindow.InitClothes
- clothes.BuyReward.RewardList.itemRenderer
- Activity4PassportWindow.SetLastLv
- Activity4PassportWindow.PlayFirstRewardEffect
- Activity4PassportWindow.PlayEndRewardEffect
- Activity4PassportWindow.HandleMessage
- Activity4PassportWindow.OnShown
- Activity4PassportWindow.OnClose
**Requires:**
- ActivityDungeon1003_PassportWindowByName
**Snippet:**
```lua
require("ActivityDungeon1003_PassportWindowByName")
local Activity4PassportWindow = {}
local uis, contentPane, passInfo, lvMax, modelType, expMax, rewardData, rewardType, rewardLv, listPage, passLv, jumpTb, isShowAllGet, passPortConfig, lvTween, lastLv, waitMessageId, newPassPort, animTween

function Activity4PassportWindow.ReInitData()
end

function Activity4PassportWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity4PassportWindow.package, WinResConfig.Activity4PassportWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity4PlotWindow.lua.lua
**Functions:**
- Activity4PlotWindow.ReInitData
- Activity4PlotWindow.OnInit
- Activity4PlotWindow.UpdateInfo
- list.itemRenderer
- Activity4PlotWindow.InitBtn
- Activity4PlotWindow.CloseWindow
- Activity4PlotWindow.OnClose
**Requires:**
- ActivityDungeon1003_PlotWindowByName
**Snippet:**
```lua
require("ActivityDungeon1003_PlotWindowByName")
local Activity4PlotWindow = {}
local uis, contentPane, configData

function Activity4PlotWindow.ReInitData()
end

function Activity4PlotWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity4PlotWindow.package, WinResConfig.Activity4PlotWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity4ShopWindow.lua.lua
**Functions:**
- Activity4ShopWindow.ReInitData
- Activity4ShopWindow.OnInit
- Activity4ShopWindow.UpdateInfo
- uis.Main.ItemList.itemRenderer
- Activity4ShopWindow.ShowItem
- list.itemRenderer
- Activity4ShopWindow.ShowOneReward
- list.itemRenderer
- Activity4ShopWindow.GetShopGrid
- Activity4ShopWindow.InitBtn
- Activity4ShopWindow.CloseWindow
- Activity4ShopWindow.OnClose
- Activity4ShopWindow.HandleMessage
**Requires:**
- ActivityDungeon1003_ShopWindowByName
**Snippet:**
```lua
require("ActivityDungeon1003_ShopWindowByName")
local Activity4ShopWindow = {}
local uis, contentPane, activityInfo, tempAssetsTips

function Activity4ShopWindow.ReInitData()
end

function Activity4ShopWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity4ShopWindow.package, WinResConfig.Activity4ShopWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity4SignWindow.lua.lua
**Functions:**
- Activity4SignWindow.ReInitData
- Activity4SignWindow.OnInit
- Activity4SignWindow.UpdateInfo
- list.RewardList.itemRenderer
- Activity4SignWindow.ShowAllItemFrame
- Activity4SignWindow.GetRewardData
- Activity4SignWindow.InitBtn
- Activity4SignWindow.CloseWindow
- Activity4SignWindow.OnClose
**Requires:**
- ActivityDungeon1003_SignWindowByName
**Snippet:**
```lua
require("ActivityDungeon1003_SignWindowByName")
local Activity4SignWindow = {}
local uis, contentPane, activityInfo

function Activity4SignWindow.ReInitData()
end

function Activity4SignWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity4SignWindow.package, WinResConfig.Activity4SignWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity4TaskWindow.lua.lua
**Functions:**
- Activity4TaskWindow.ReInitData
- Activity4TaskWindow.OnInit
- Activity4TaskWindow.UpdateInfo
- list.itemRenderer
- rewardList.itemRenderer
- Activity4TaskWindow.GetRewardNum
- Activity4TaskWindow.ShowAllItemFrame
- Activity4TaskWindow.SortTask
- Activity4TaskWindow.InitBtn
- Activity4TaskWindow.CloseWindow
- Activity4TaskWindow.OnClose
**Requires:**
- ActivityDungeon1003_TaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1003_TaskWindowByName")
local Activity4TaskWindow = {}
local uis, contentPane

function Activity4TaskWindow.ReInitData()
end

function Activity4TaskWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity4TaskWindow.package, WinResConfig.Activity4TaskWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity4_MiniGameData.lua.lua
**Functions:**
- Activity4_MiniGameData.SetMiniGameInfo
- Activity4_MiniGameData.GetMiniGameInfo
**Snippet:**
```lua
Activity4_MiniGameData = {}
local miniGameInfo

function Activity4_MiniGameData.SetMiniGameInfo(info)
  miniGameInfo = info
end

function Activity4_MiniGameData.GetMiniGameInfo()
  return miniGameInfo
end
```

---

## Activty/baseact/Activity4_MiniGameScriptList.lua.lua
**Requires:**
- Activity4_MiniGameData
- Activity4_MiniGameService
**Snippet:**
```lua
require("Activity4_MiniGameData")
require("Activity4_MiniGameService")
```

---

## Activty/baseact/Activity4_MiniGameService.lua.lua
**Functions:**
- Activity4_MiniGameService.MiniGameInfoReq
- Activity4_MiniGameService.MiniGameInfoRsp
- Activity4_MiniGameService.MiniGameSubmitReq
- Activity4_MiniGameService.MiniGameSubmitRsp
- Activity4_MiniGameService.MiniGameGetDailyRewardReq
- Activity4_MiniGameService.MiniGameGetDailyRewardRsp
- Activity4_MiniGameService.Init
**Snippet:**
```lua
Activity4_MiniGameService = {}
local gameId = 70441004

function Activity4_MiniGameService.MiniGameInfoReq(rspCallback)
  local info = ActivityDungeonData.GetActivityInfo()
  local activityId = info.baseInfo.activityId
  Net.Send(Proto.MsgName.ActivityGetMiniGameReq, {gameId = gameId, activityId = activityId}, rspCallback)
end

function Activity4_MiniGameService.MiniGameInfoRsp(msg)
```

---

## Activty/baseact/Activity5BossBattleWindow.lua.lua
**Functions:**
- Activity5BossBattleWindow.ReInitData
- Activity5BossBattleWindow.OnInit
- Activity5BossBattleWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity5BossBattleWindow.FormatRemainTime
- Activity5BossBattleWindow.GetChapter
- Activity5BossBattleWindow.InitBtn
- Activity5BossBattleWindow.CloseWindow
- Activity5BossBattleWindow.OnClose
**Requires:**
- ActivityDungeon1004_BossBattleWindowByName
**Snippet:**
```lua
require("ActivityDungeon1004_BossBattleWindowByName")
local Activity5BossBattleWindow = {}
local uis, contentPane, activityInfo

function Activity5BossBattleWindow.ReInitData()
end

function Activity5BossBattleWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity5BossBattleWindow.package, WinResConfig.Activity5BossBattleWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity5BuyLevelDesWindow.lua.lua
**Functions:**
- Activity5BuyLevelDesWindow.ReInitData
- Activity5BuyLevelDesWindow.OnInit
- Activity5BuyLevelDesWindow.ShowAssetsTips
- Activity5BuyLevelDesWindow.UpdateTextDisplay
- Activity5BuyLevelDesWindow.Init
- Activity5BuyLevelDesWindow.GetGold
- Activity5BuyLevelDesWindow.ShowReward
- list.itemRenderer
- Activity5BuyLevelDesWindow.GetRewardItem
- Activity5BuyLevelDesWindow.GetLvData
- Activity5BuyLevelDesWindow.GetRewardLvData
- Activity5BuyLevelDesWindow.GetRewardByPhaseId
- Activity5BuyLevelDesWindow.BuyLevelRsp
- Activity5BuyLevelDesWindow.InitBtn
- waitFun
- Activity5BuyLevelDesWindow.HandleMessage
- Activity5BuyLevelDesWindow.OnShown
- Activity5BuyLevelDesWindow.OnClose
**Requires:**
- ActivityDungeon1004_BuyLevelDesWindowByName
**Snippet:**
```lua
require("ActivityDungeon1004_BuyLevelDesWindowByName")
local Activity5BuyLevelDesWindow = {}
local uis, contentPane, lvData, curLv, buyNum, itemId, lvMax, waitFun, rewardData, itemSort, transPlay, firstPlay, tatalGold, passInfo

function Activity5BuyLevelDesWindow.ReInitData()
end

function Activity5BuyLevelDesWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity5BuyLevelDesWindow.package, WinResConfig.Activity5BuyLevelDesWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity5ChallengeWindow.lua.lua
**Functions:**
- Activity5ChallengeWindow.ReInitData
- Activity5ChallengeWindow.OnInit
- Activity5ChallengeWindow.UpdateInfo
- uis.Main.ChapterList.itemRenderer
- Activity5ChallengeWindow.ShoweStage
- Activity5ChallengeWindow.StageItemClick
- Activity5ChallengeWindow.ShopInfo
- Activity5ChallengeWindow.GetChapterPassById
- Activity5ChallengeWindow.GetCurStage
- Activity5ChallengeWindow.GetFirstChapter
- Activity5ChallengeWindow.GetAllChapterId
- Activity5ChallengeWindow.InitBtn
- Activity5ChallengeWindow.CloseWindow
- Activity5ChallengeWindow.OnShown
- Activity5ChallengeWindow.OnClose
**Requires:**
- ActivityDungeon1004_ChallengeWindowByName
**Snippet:**
```lua
require("ActivityDungeon1004_ChallengeWindowByName")
local Activity5ChallengeWindow = {}
local uis, contentPane, activityInfo, scrollingTween

function Activity5ChallengeWindow.ReInitData()
end

function Activity5ChallengeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity5ChallengeWindow.package, WinResConfig.Activity5ChallengeWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity5DungeonWindow.lua.lua
**Functions:**
- Activity5DungeonWindow.ReInitData
- Activity5DungeonWindow.OnInit
- Activity5DungeonWindow.LoadBg
- Activity5DungeonWindow.InitRedDot
- Activity5DungeonWindow.UpdateInfo
- Activity5DungeonWindow.InitBtnTxt
- Activity5DungeonWindow.InitBtn
- Activity5DungeonWindow.OnShown
- Activity5DungeonWindow.OnHide
- Activity5DungeonWindow.OnClose
- Activity5DungeonWindow.HandleMessage
**Requires:**
- ActivityDungeon1004_ActivityDungeonWindowByName
**Snippet:**
```lua
require("ActivityDungeon1004_ActivityDungeonWindowByName")
local Activity5DungeonWindow = {}
local uis, contentPane, jumpTb, configData, activityInfo, effect, eventTipsRoot, cursors, cursorRoot, reviewMode
local OnPopupEventTips = function(events)
  local parent = uis.Main.root
  if not eventTipsRoot then
    eventTipsRoot = UIMgr:CreateObject("ActivityDungeon1004", "EventTipsList")
    eventTipsRoot.opaque = false
    local childIndex = parent:GetChildIndex(uis.Main.BackGround.root)
    parent:AddChildAt(eventTipsRoot, childIndex + 1)
```

---

## Activty/baseact/Activity5EntranceAnimWindow.lua.lua
**Functions:**
- FindChild
- PlayDailyEntranceAnim
- Activity5EntranceAnimWindow.ReInitData
- Activity5EntranceAnimWindow.OnInit
- Activity5EntranceAnimWindow.UpdateInfo
- Activity5EntranceAnimWindow.InitBtn
- Activity5EntranceAnimWindow.OnClose
**Requires:**
- ActivityDungeon1004_MainSeasonsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1004_MainSeasonsWindowByName")
local Activity5EntranceAnimWindow = {}
local uis, contentPane, touchable, exitWhenDoubleClick
local setSpritesColor = function(go, color)
  local spriteRenderers = go:GetComponentsInChildren(typeof(CS.UnityEngine.SpriteRenderer))
  if spriteRenderers then
    for i = 0, spriteRenderers.Length - 1 do
      local sr = spriteRenderers[i]
      sr.color = color
    end
```

---

## Activty/baseact/Activity5FishBookWindow.lua.lua
**Functions:**
- Activity5FishBookWindow.ReInitData
- Activity5FishBookWindow.OnInit
- Activity5FishBookWindow.UpdateInfo
- list.itemRenderer
- Activity5FishBookWindow.GetAllFish
- Activity5FishBookWindow.InitBtn
- Activity5FishBookWindow.CanGet
- Activity5FishBookWindow.OnClose
- Activity5FishBookWindow.HandleMessage
**Requires:**
- ActivityDungeon1004_MiniBook2WindowByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniBook2WindowByName")
local Activity5FishBookWindow = {}
local uis, contentPane
local gameId = 70441006
local fishNew

function Activity5FishBookWindow.ReInitData()
end

function Activity5FishBookWindow.OnInit(bridgeObj)
```

---

## Activty/baseact/Activity5FishEndWindow.lua.lua
**Functions:**
- Activity5FishEndWindow.ReInitData
- Activity5FishEndWindow.OnInit
- Activity5FishEndWindow.UpdateInfo
- Activity5FishEndWindow.InitBtn
- Activity5FishEndWindow.OnClose
**Requires:**
- ActivityDungeon1004_MiniStart2_End1WindowByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniStart2_End1WindowByName")
local Activity5FishEndWindow = {}
local uis, contentPane, fishId, v2

function Activity5FishEndWindow.ReInitData()
end

function Activity5FishEndWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity5FishEndWindow.package, WinResConfig.Activity5FishEndWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity5FishMainWindow.lua.lua
**Functions:**
- Activity5FishMainWindow.ReInitData
- Activity5FishMainWindow.OnInit
- Activity5FishMainWindow.UpdateInfo
- Activity5FishMainWindow.InitBtn
- Activity5FishMainWindow.OnClose
- Activity5FishMainWindow.HandleMessage
**Requires:**
- ActivityDungeon1004_MiniGame2WindowByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniGame2WindowByName")
local Activity5FishMainWindow = {}
local uis, contentPane
local gameId = 70441006
ld("Activity5_MiniGame")
local RefreshPanelInfo = function()
  local info = Activity5_MiniGameData.GetMiniGameInfo(gameId)
  local conf = TableData.GetConfig(gameId, "BaseActivityStageGame")
  local str = conf.game_day_reward[1]
  local splits = Split(str, ":")
```

---

## Activty/baseact/Activity5FishNewEndWindow.lua.lua
**Functions:**
- Activity5FishNewEndWindow.ReInitData
- Activity5FishNewEndWindow.OnInit
- Activity5FishNewEndWindow.UpdateInfo
- Activity5FishNewEndWindow.InitBtn
- Activity5FishNewEndWindow.OnClose
**Requires:**
- ActivityDungeon1004_MiniStart2_End2WindowByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniStart2_End2WindowByName")
local Activity5FishNewEndWindow = {}
local uis, contentPane, fishId, v2

function Activity5FishNewEndWindow.ReInitData()
end

function Activity5FishNewEndWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity5FishNewEndWindow.package, WinResConfig.Activity5FishNewEndWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity5FishRecordWindow.lua.lua
**Functions:**
- Activity5FishRecordWindow.ReInitData
- Activity5FishRecordWindow.OnInit
- Activity5FishRecordWindow.UpdateInfo
- list.itemRenderer
- Activity5FishRecordWindow.InitBtn
- Activity5FishRecordWindow.OnClose
**Requires:**
- ActivityDungeon1004_MiniIntegralWindowByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniIntegralWindowByName")
local Activity5FishRecordWindow = {}
local uis, contentPane

function Activity5FishRecordWindow.ReInitData()
end

function Activity5FishRecordWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity5FishRecordWindow.package, WinResConfig.Activity5FishRecordWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity5FishTaskWindow.lua.lua
**Functions:**
- RefreshRewardList
- list.itemRenderer
- itemlist.itemRenderer
- Activity5FishTaskWindow.ReInitData
- Activity5FishTaskWindow.OnInit
- Activity5FishTaskWindow.UpdateInfo
- Activity5FishTaskWindow.InitBtn
- Activity5FishTaskWindow.OnClose
**Requires:**
- ActivityDungeon1004_MiniTask2WindowByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniTask2WindowByName")
local Activity5FishTaskWindow = {}
local uis, contentPane
local gameId = 70441006

local function RefreshRewardList()
  local info = Activity5_MiniGameData.GetMiniGameInfo(gameId)
  local minigame_tasks = info.taskList
  local list = uis.Main.TipsList
  list:SetVirtual()
```

---

## Activty/baseact/Activity5FishWindow.lua.lua
**Functions:**
- Activity5FishWindow.ReInitData
- Activity5FishWindow.OnInit
- Activity5FishWindow.UpdateInfo
- Activity5FishWindow.PlayFlowerAnim
- Activity5FishWindow.InitBtn
- Activity5FishWindow.SetPaused
- Activity5FishWindow.GetRandomFish
- Activity5FishWindow.GameOver
- Activity5FishWindow.GetAllFish
- Activity5FishWindow.InitGame
- Activity5FishWindow.Start
- Activity5FishWindow.InitNumber
- Activity5FishWindow.OnShowAnimationEnd
- Activity5FishWindow.OnPreClose
- Activity5FishWindow.OnClose
- Activity5FishWindow.HandleMessage
**Requires:**
- ActivityDungeon1004_MiniGameStart2WindowByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniGameStart2WindowByName")
local Activity5FishWindow = {}
local uis, contentPane, fishingRod, waitTimeTween, getFishTween, tweenScale, scaleRoot
local max = 4
local now = 0
local integral
local gameId = 70441006
local allFishCofn, barTweener, harvestTweener, holderShadow, objShadow, nowId, new
local nameShadow = {
  "big",
```

---

## Activty/baseact/Activity5MaterialWindow.lua.lua
**Functions:**
- Activity5MaterialWindow.ReInitData
- Activity5MaterialWindow.OnInit
- Activity5MaterialWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity5MaterialWindow.GetChapter
- Activity5MaterialWindow.GetMaxCount
- Activity5MaterialWindow.InitBtn
- Activity5MaterialWindow.CloseWindow
- Activity5MaterialWindow.OnShown
- Activity5MaterialWindow.OnClose
**Requires:**
- ActivityDungeon1004_MaterialWindowByName
**Snippet:**
```lua
require("ActivityDungeon1004_MaterialWindowByName")
local Activity5MaterialWindow = {}
local uis, contentPane, activityInfo, maxCount, posX

function Activity5MaterialWindow.ReInitData()
end

function Activity5MaterialWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity5MaterialWindow.package, WinResConfig.Activity5MaterialWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity5MiniGameMainWindow.lua.lua
**Functions:**
- Activity5MiniGameMainWindow.ReInitData
- Activity5MiniGameMainWindow.OnInit
- Activity5MiniGameMainWindow.UpdateInfo
- Activity5MiniGameMainWindow.InitBtn
- Activity5MiniGameMainWindow.OnClose
- Activity5MiniGameMainWindow.HandleMessage
**Requires:**
- ActivityDungeon1004_MiniGameWindowByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniGameWindowByName")
local Activity5MiniGameMainWindow = {}
local uis, contentPane
local gameId = 70441005
ld("Activity5_MiniGame")
local RefreshPanelInfo = function()
  local highestScoreTxt = T(20620)
  local dailyScoreTxt = T(20485)
  local info = Activity5_MiniGameData.GetMiniGameInfo(gameId)
  local conf = TableData.GetConfig(70441005, "BaseActivityStageGame")
```

---

## Activty/baseact/Activity5MiniGameRecordWindow.lua.lua
**Functions:**
- Activity5MiniGameRecordWindow.ReInitData
- Activity5MiniGameRecordWindow.OnInit
- Activity5MiniGameRecordWindow.UpdateInfo
- list.itemRenderer
- Activity5MiniGameRecordWindow.InitBtn
- Activity5MiniGameRecordWindow.OnClose
**Requires:**
- ActivityDungeon1004_MiniIntegralWindowByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniIntegralWindowByName")
local Activity5MiniGameRecordWindow = {}
local uis, contentPane
local gameId = 70441005

function Activity5MiniGameRecordWindow.ReInitData()
end

function Activity5MiniGameRecordWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity5MiniGameRecordWindow.package, WinResConfig.Activity5MiniGameRecordWindow.comName, function(com)
```

---

## Activty/baseact/Activity5MiniGameStartWindow.lua.lua
**Functions:**
- Activity5MiniGameStartWindow.ReInitData
- Activity5MiniGameStartWindow.OnInit
- Activity5MiniGameStartWindow.UpdateInfo
- uis.Main.ItemList.itemRenderer
- Activity5MiniGameStartWindow.InitBtn
- Activity5MiniGameStartWindow.OnClose
**Requires:**
- ActivityDungeon1004_MiniStart_WinTargetWindowByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniStart_WinTargetWindowByName")
local Activity5MiniGameStartWindow = {}
local uis, contentPane
local ITEM_URL_LOOKUP = {
  [1] = "ui://wyxy0raasxc4b9",
  [2] = "ui://wyxy0raasxc4bf",
  [3] = "ui://wyxy0raasxc4bz",
  [4] = "ui://wyxy0raasxc4bj",
  [5] = "ui://wyxy0raasxc4bb",
  [6] = "ui://wyxy0raasxc4bv",
```

---

## Activty/baseact/Activity5MiniGameSubmitWindow.lua.lua
**Functions:**
- Activity5MiniGameSubmitWindow.ReInitData
- Activity5MiniGameSubmitWindow.OnInit
- Activity5MiniGameSubmitWindow.UpdateInfo
- itemlist.itemRenderer
- Activity5MiniGameSubmitWindow.InitBtn
- Activity5MiniGameSubmitWindow.OnClose
**Requires:**
- ActivityDungeon1004_MiniStart_EndRewardWindowByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniStart_EndRewardWindowByName")
local Activity5MiniGameSubmitWindow = {}
local uis, contentPane, succeed, score, consumeSeconds, unmetlist
local gameId = 70441005

function Activity5MiniGameSubmitWindow.ReInitData()
end

function Activity5MiniGameSubmitWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity5MiniGameSubmitWindow.package, WinResConfig.Activity5MiniGameSubmitWindow.comName, function(com)
```

---

## Activty/baseact/Activity5MiniGameTaskWindow.lua.lua
**Functions:**
- RefreshRewardList
- list.itemRenderer
- itemlist.itemRenderer
- Activity5MiniGameTaskWindow.ReInitData
- Activity5MiniGameTaskWindow.OnInit
- Activity5MiniGameTaskWindow.UpdateInfo
- Activity5MiniGameTaskWindow.InitBtn
- Activity5MiniGameTaskWindow.OnClose
**Requires:**
- ActivityDungeon1004_MiniTaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniTaskWindowByName")
local Activity5MiniGameTaskWindow = {}
local uis, contentPane
local gameId = 70441005

local function RefreshRewardList()
  local info = Activity5_MiniGameData.GetMiniGameInfo(gameId)
  local minigame_tasks = info.taskList
  local list = uis.Main.TipsList
  list:SetVirtual()
```

---

## Activty/baseact/Activity5MiniGameWindow.lua.lua
**Functions:**
- CreateItem
- ResumeCoroutine
- GetDifficulties
- Activity5MiniGameWindow.ReInitData
- Activity5MiniGameWindow.OnInit
- Activity5MiniGameWindow.UpdateInfo
- Activity5MiniGameWindow.InitBtn
- Activity5MiniGameWindow.OnClose
- Activity5MiniGameWindow.HandleMessage
**Requires:**
- ActivityDungeon1004_MiniGameStartWindowByName
- Activity5_MiniGameController
**Snippet:**
```lua
require("ActivityDungeon1004_MiniGameStartWindowByName")
local Activity5MiniGameWindow = {}
local uis, contentPane, controller, startCoroutine
local ITEM_URL_LOOKUP = {
  [1] = "MiniStart_Item02",
  [2] = "MiniStart_Item03",
  [3] = "MiniStart_Item04",
  [4] = "MiniStart_Item05",
  [5] = "MiniStart_Item06",
  [6] = "MiniStart_Item07",
```

---

## Activty/baseact/Activity5MiniGameWinWindow.lua.lua
**Functions:**
- Activity5MiniGameWinWindow.ReInitData
- Activity5MiniGameWinWindow.OnInit
- Activity5MiniGameWinWindow.UpdateInfo
- Activity5MiniGameWinWindow.InitBtn
- Activity5MiniGameWinWindow.OnClose
**Requires:**
- ActivityDungeon1004_MiniStart_WinWindowByName
**Snippet:**
```lua
require("ActivityDungeon1004_MiniStart_WinWindowByName")
local Activity5MiniGameWinWindow = {}
local uis, contentPane

function Activity5MiniGameWinWindow.ReInitData()
end

function Activity5MiniGameWinWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity5MiniGameWinWindow.package, WinResConfig.Activity5MiniGameWinWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity5PassportLevelUpTipsWindow.lua.lua
**Functions:**
- Activity5PassportLevelUpTipsWindow.ReInitData
- Activity5PassportLevelUpTipsWindow.OnInit
- Activity5PassportLevelUpTipsWindow.UpdateInfo
- Activity5PassportLevelUpTipsWindow.InitBtn
- Activity5PassportLevelUpTipsWindow.OnClose
**Requires:**
- ActivityDungeon1004_PassportUp_LevelUpTipsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1004_PassportUp_LevelUpTipsWindowByName")
local Activity5PassportLevelUpTipsWindow = {}
local uis, contentPane, lv

function Activity5PassportLevelUpTipsWindow.ReInitData()
end

function Activity5PassportLevelUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity5PassportLevelUpTipsWindow.package, WinResConfig.Activity5PassportLevelUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity5PassportWindow.lua.lua
**Functions:**
- Activity5PassportWindow.ReInitData
- Activity5PassportWindow.OnInit
- Activity5PassportWindow.UpdateTextDisplay
- Activity5PassportWindow.InitPassport
- uis.Main.TabRegion.TabList.itemRenderer
- Activity5PassportWindow.InitEffect
- Activity5PassportWindow.InitLv
- Activity5PassportWindow.ShowLevelUp
- Activity5PassportWindow.SaveLevel
- Activity5PassportWindow.GetRewardByLv
- Activity5PassportWindow.GetRewardNum
- Activity5PassportWindow.IsGetAllReward
- Activity5PassportWindow.ShowReward
- Activity5PassportWindow.GetUpdateLv
- Activity5PassportWindow.RefreshListReward
- Activity5PassportWindow.CheckItemTime
- Activity5PassportWindow.ShowQuitTips
- Activity5PassportWindow.RefreshUI
- Activity5PassportWindow.GetExpMxp
- Activity5PassportWindow.SetLevelInfo
- Activity5PassportWindow.InitList
- list.itemRenderer
- Activity5PassportWindow.SetListPos
- Activity5PassportWindow.RefreshReward
- Activity5PassportWindow.ShowGetEffect
- Activity5PassportWindow.RewardItemClick
- Activity5PassportWindow.IsReward
- Activity5PassportWindow.RefreshRewardFirst
- Activity5PassportWindow.RefreshRewardEnd
- Activity5PassportWindow.ShowState
- Activity5PassportWindow.RefreshRewardShow
- Activity5PassportWindow.RefreshRewardState
- Activity5PassportWindow.PassportActivate
- Activity5PassportWindow.CloseWindow
- Activity5PassportWindow.InitBtn
- Activity5PassportWindow.ShowExpBarAnim
- Activity5PassportWindow.InitTask
- list.itemRenderer
- Activity5PassportWindow.InitClothes
- clothes.BuyReward.RewardList.itemRenderer
- Activity5PassportWindow.SetLastLv
- Activity5PassportWindow.PlayFirstRewardEffect
- Activity5PassportWindow.PlayEndRewardEffect
- Activity5PassportWindow.HandleMessage
- Activity5PassportWindow.OnShown
- Activity5PassportWindow.OnClose
**Requires:**
- ActivityDungeon1004_PassportWindowByName
**Snippet:**
```lua
require("ActivityDungeon1004_PassportWindowByName")
local Activity5PassportWindow = {}
local uis, contentPane, passInfo, lvMax, modelType, expMax, rewardData, rewardType, rewardLv, listPage, passLv, jumpTb, isShowAllGet, passPortConfig, lvTween, lastLv, waitMessageId, newPassPort, animTween

function Activity5PassportWindow.ReInitData()
end

function Activity5PassportWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity5PassportWindow.package, WinResConfig.Activity5PassportWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity5PlotWindow.lua.lua
**Functions:**
- Activity5PlotWindow.ReInitData
- Activity5PlotWindow.OnInit
- Activity5PlotWindow.UpdateInfo
- list.itemRenderer
- Activity5PlotWindow.InitBtn
- Activity5PlotWindow.CloseWindow
- Activity5PlotWindow.OnClose
**Requires:**
- ActivityDungeon1004_PlotWindowByName
**Snippet:**
```lua
require("ActivityDungeon1004_PlotWindowByName")
local Activity5PlotWindow = {}
local uis, contentPane, configData

function Activity5PlotWindow.ReInitData()
end

function Activity5PlotWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity5PlotWindow.package, WinResConfig.Activity5PlotWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity5ShopWindow.lua.lua
**Functions:**
- Activity5ShopWindow.ReInitData
- Activity5ShopWindow.OnInit
- Activity5ShopWindow.UpdateInfo
- uis.Main.ItemList.itemRenderer
- Activity5ShopWindow.ShowItem
- list.itemRenderer
- Activity5ShopWindow.ShowOneReward
- list.itemRenderer
- Activity5ShopWindow.GetShopGrid
- Activity5ShopWindow.InitBtn
- Activity5ShopWindow.CloseWindow
- Activity5ShopWindow.OnClose
- Activity5ShopWindow.HandleMessage
**Requires:**
- ActivityDungeon1004_ShopWindowByName
**Snippet:**
```lua
require("ActivityDungeon1004_ShopWindowByName")
local Activity5ShopWindow = {}
local uis, contentPane, activityInfo, tempAssetsTips

function Activity5ShopWindow.ReInitData()
end

function Activity5ShopWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity5ShopWindow.package, WinResConfig.Activity5ShopWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity5SignWindow.lua.lua
**Functions:**
- Activity5SignWindow.ReInitData
- Activity5SignWindow.OnInit
- Activity5SignWindow.UpdateInfo
- list.RewardList.itemRenderer
- Activity5SignWindow.ShowAllItemFrame
- Activity5SignWindow.GetRewardData
- Activity5SignWindow.InitBtn
- Activity5SignWindow.CloseWindow
- Activity5SignWindow.OnClose
**Requires:**
- ActivityDungeon1004_SignWindowByName
**Snippet:**
```lua
require("ActivityDungeon1004_SignWindowByName")
local Activity5SignWindow = {}
local uis, contentPane, activityInfo

function Activity5SignWindow.ReInitData()
end

function Activity5SignWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity5SignWindow.package, WinResConfig.Activity5SignWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity5TaskWindow.lua.lua
**Functions:**
- Activity5TaskWindow.ReInitData
- Activity5TaskWindow.OnInit
- Activity5TaskWindow.UpdateInfo
- list.itemRenderer
- rewardList.itemRenderer
- Activity5TaskWindow.GetRewardNum
- Activity5TaskWindow.ShowAllItemFrame
- Activity5TaskWindow.SortTask
- Activity5TaskWindow.InitBtn
- Activity5TaskWindow.CloseWindow
- Activity5TaskWindow.OnClose
**Requires:**
- ActivityDungeon1004_TaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1004_TaskWindowByName")
local Activity5TaskWindow = {}
local uis, contentPane

function Activity5TaskWindow.ReInitData()
end

function Activity5TaskWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity5TaskWindow.package, WinResConfig.Activity5TaskWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity5_MiniGameController.lua.lua
**Functions:**
- CollectSameItems
- CheckBoomEffect
- CreateSpecialItems
- ItemsDrop
- CreateNewItems
- AllBoom
**Snippet:**
```lua
local ITEM_TYPE = {
  A = 70076502,
  B = 70076503,
  C = 70076504,
  D = 70076505,
  E = 70076506,
  F = 70076507,
  G = 70076508,
  RAINBOW = 70076501
}
```

---

## Activty/baseact/Activity5_MiniGameData.lua.lua
**Snippet:**
```lua
local miniGameInfoDict
local fish = {}
local SetMiniGameInfo = function(info)
  miniGameInfoDict = miniGameInfoDict or {}
  miniGameInfoDict[info.gameId] = info
  if info.gameId == 70441006 then
    fish = info.extraCount
  end
end
local GetMiniGameInfo = function(gameId)
```

---

## Activty/baseact/Activity5_MiniGameScriptList.lua.lua
**Requires:**
- Activity5_MiniGameData
- Activity5_MiniGameService
**Snippet:**
```lua
Activity5_MiniGameData = require("Activity5_MiniGameData")
Activity5_MiniGameService = require("Activity5_MiniGameService")
```

---

## Activty/baseact/Activity5_MiniGameService.lua.lua
**Snippet:**
```lua
local cachedGameId
local MiniGameInfoReq = function(gameId, rspCallback)
  local info = ActivityDungeonData.GetActivityInfo()
  local activityId = info.baseInfo.activityId
  Net.Send(Proto.MsgName.ActivityGetMiniGameReq, {activityId = activityId, gameId = gameId}, rspCallback)
end
local MiniGameInfoRsp = function(msg)
  Activity5_MiniGameData.SetMiniGameInfo(msg)
  UIMgr:SendWindowMessage(WinResConfig.Activity5MiniGameMainWindow.name, WindowMsgEnum.Activity5_MiniGame.REFRESH_MINIGAME_INFO)
  UIMgr:SendWindowMessage(WinResConfig.Activity5MiniGameWindow.name, WindowMsgEnum.Activity5_MiniGame.REFRESH_MINIGAME_INFO)
```

---

## Activty/baseact/Activity6BossBattleWindow.lua.lua
**Functions:**
- Activity6BossBattleWindow.ReInitData
- Activity6BossBattleWindow.OnInit
- Activity6BossBattleWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity6BossBattleWindow.FormatRemainTime
- Activity6BossBattleWindow.GetChapter
- Activity6BossBattleWindow.InitBtn
- Activity6BossBattleWindow.CloseWindow
- Activity6BossBattleWindow.OnClose
**Requires:**
- ActivityDungeon1005_BossBattleWindowByName
**Snippet:**
```lua
require("ActivityDungeon1005_BossBattleWindowByName")
local Activity6BossBattleWindow = {}
local uis, contentPane, activityInfo

function Activity6BossBattleWindow.ReInitData()
end

function Activity6BossBattleWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity6BossBattleWindow.package, WinResConfig.Activity6BossBattleWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity6BuyLevelDesWindow.lua.lua
**Functions:**
- Activity6BuyLevelDesWindow.ReInitData
- Activity6BuyLevelDesWindow.OnInit
- Activity6BuyLevelDesWindow.ShowAssetsTips
- Activity6BuyLevelDesWindow.UpdateTextDisplay
- Activity6BuyLevelDesWindow.Init
- Activity6BuyLevelDesWindow.GetGold
- Activity6BuyLevelDesWindow.ShowReward
- list.itemRenderer
- Activity6BuyLevelDesWindow.GetRewardItem
- Activity6BuyLevelDesWindow.GetLvData
- Activity6BuyLevelDesWindow.GetRewardLvData
- Activity6BuyLevelDesWindow.GetRewardByPhaseId
- Activity6BuyLevelDesWindow.BuyLevelRsp
- Activity6BuyLevelDesWindow.InitBtn
- waitFun
- Activity6BuyLevelDesWindow.HandleMessage
- Activity6BuyLevelDesWindow.OnShown
- Activity6BuyLevelDesWindow.OnClose
**Requires:**
- ActivityDungeon1005_BuyLevelDesWindowByName
**Snippet:**
```lua
require("ActivityDungeon1005_BuyLevelDesWindowByName")
local Activity6BuyLevelDesWindow = {}
local uis, contentPane, lvData, curLv, buyNum, itemId, lvMax, waitFun, rewardData, itemSort, transPlay, firstPlay, tatalGold, passInfo

function Activity6BuyLevelDesWindow.ReInitData()
end

function Activity6BuyLevelDesWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity6BuyLevelDesWindow.package, WinResConfig.Activity6BuyLevelDesWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity6ChallengeWindow.lua.lua
**Functions:**
- Activity6ChallengeWindow.ReInitData
- Activity6ChallengeWindow.OnInit
- Activity6ChallengeWindow.UpdateInfo
- uis.Main.ChapterList.itemRenderer
- Activity6ChallengeWindow.ShoweStage
- Activity6ChallengeWindow.StageItemClick
- Activity6ChallengeWindow.ShopInfo
- Activity6ChallengeWindow.GetChapterPassById
- Activity6ChallengeWindow.GetCurStage
- Activity6ChallengeWindow.GetFirstChapter
- Activity6ChallengeWindow.GetAllChapterId
- Activity6ChallengeWindow.InitBtn
- Activity6ChallengeWindow.CloseWindow
- Activity6ChallengeWindow.OnShown
- Activity6ChallengeWindow.OnClose
**Requires:**
- ActivityDungeon1005_ChallengeWindowByName
**Snippet:**
```lua
require("ActivityDungeon1005_ChallengeWindowByName")
local Activity6ChallengeWindow = {}
local uis, contentPane, activityInfo, scrollingTween

function Activity6ChallengeWindow.ReInitData()
end

function Activity6ChallengeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity6ChallengeWindow.package, WinResConfig.Activity6ChallengeWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity6DungeonWindow.lua.lua
**Functions:**
- Activity6DungeonWindow.ReInitData
- Activity6DungeonWindow.OnInit
- Activity6DungeonWindow.LoadBg
- Activity6DungeonWindow.InitRedDot
- Activity6DungeonWindow.UpdateInfo
- Activity6DungeonWindow.InitBtnTxt
- Activity6DungeonWindow.InitBtn
- Activity6DungeonWindow.OnShown
- Activity6DungeonWindow.OnClose
- Activity6DungeonWindow.HandleMessage
**Requires:**
- ActivityDungeon1005_ActivityDungeonWindowByName
**Snippet:**
```lua
require("ActivityDungeon1005_ActivityDungeonWindowByName")
local Activity6DungeonWindow = {}
local uis, contentPane, jumpTb, configData, activityInfo, effect
local InitMiniGameInfo = function()
  local data = ActivityDungeonData.GetActivityData()
  if data.id == 70440001 then
    ld("Activity1_MiniGame")
    Activity1_MiniGameService.MiniGameInfoReq(function()
      RedDotMgr.AddNode({
        windowName = WinResConfig.Activity6DungeonWindow.name,
```

---

## Activty/baseact/Activity6MaterialWindow.lua.lua
**Functions:**
- Activity6MaterialWindow.ReInitData
- Activity6MaterialWindow.OnInit
- Activity6MaterialWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity6MaterialWindow.GetChapter
- Activity6MaterialWindow.GetMaxCount
- Activity6MaterialWindow.InitBtn
- Activity6MaterialWindow.CloseWindow
- Activity6MaterialWindow.OnShown
- Activity6MaterialWindow.OnClose
**Requires:**
- ActivityDungeon1005_MaterialWindowByName
**Snippet:**
```lua
require("ActivityDungeon1005_MaterialWindowByName")
local Activity6MaterialWindow = {}
local uis, contentPane, activityInfo, maxCount, posX

function Activity6MaterialWindow.ReInitData()
end

function Activity6MaterialWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity6MaterialWindow.package, WinResConfig.Activity6MaterialWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity6MiniGameChoiceWindow.lua.lua
**Functions:**
- Activity6MiniGameChoiceWindow.ReInitData
- Activity6MiniGameChoiceWindow.OnInit
- Activity6MiniGameChoiceWindow.UpdateInfo
- balllist.itemRenderer
- list.itemRenderer
- Activity6MiniGameChoiceWindow.InitBtn
- Activity6MiniGameChoiceWindow.OnClose
**Requires:**
- ActivityDungeon1005_MiniGameChoiceWindowByName
**Snippet:**
```lua
require("ActivityDungeon1005_MiniGameChoiceWindowByName")
local Activity6MiniGameChoiceWindow = {}
local uis, contentPane
local gameId = 70441007
local selectedConf, configs, shapeMode
local OnUpdate = function()
  local list = uis.Main.TipsList
  if configs and selectedConf then
    for i, v in ipairs(configs) do
      if v == selectedConf then
```

---

## Activty/baseact/Activity6MiniGameMainWindow.lua.lua
**Functions:**
- Activity6MiniGameMainWindow.ReInitData
- Activity6MiniGameMainWindow.OnInit
- Activity6MiniGameMainWindow.UpdateInfo
- Activity6MiniGameMainWindow.InitBtn
- Activity6MiniGameMainWindow.OnClose
- Activity6MiniGameMainWindow.HandleMessage
**Requires:**
- ActivityDungeon1005_MiniGameWindowByName
**Snippet:**
```lua
require("ActivityDungeon1005_MiniGameWindowByName")
local Activity6MiniGameMainWindow = {}
local uis, contentPane
local gameId = 70441007
ld("Activity6_MiniGame")
local RefreshPanelInfo = function()
  local highestScoreTxt = T(20620)
  local dailyScoreTxt = T(20485)
  local info = Activity6_MiniGameData.GetMiniGameInfo(gameId)
  local conf = TableData.GetConfig(gameId, "BaseActivityStageGame")
```

---

## Activty/baseact/Activity6MiniGameRecordWindow.lua.lua
**Functions:**
- Activity6MiniGameRecordWindow.ReInitData
- Activity6MiniGameRecordWindow.OnInit
- Activity6MiniGameRecordWindow.UpdateInfo
- list.itemRenderer
- Activity6MiniGameRecordWindow.InitBtn
- Activity6MiniGameRecordWindow.OnClose
**Requires:**
- ActivityDungeon1005_MiniIntegralWindowByName
**Snippet:**
```lua
require("ActivityDungeon1005_MiniIntegralWindowByName")
local Activity6MiniGameRecordWindow = {}
local uis, contentPane
local gameId = 70441007

function Activity6MiniGameRecordWindow.ReInitData()
end

function Activity6MiniGameRecordWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity6MiniGameRecordWindow.package, WinResConfig.Activity6MiniGameRecordWindow.comName, function(com)
```

---

## Activty/baseact/Activity6MiniGameSubmitWindow.lua.lua
**Functions:**
- Activity6MiniGameSubmitWindow.ReInitData
- Activity6MiniGameSubmitWindow.OnInit
- Activity6MiniGameSubmitWindow.UpdateInfo
- Activity6MiniGameSubmitWindow.InitBtn
- Activity6MiniGameSubmitWindow.OnClose
**Requires:**
- ActivityDungeon1005_MiniStart_EndRewardWindowByName
**Snippet:**
```lua
require("ActivityDungeon1005_MiniStart_EndRewardWindowByName")
local Activity6MiniGameSubmitWindow = {}
local uis, contentPane, succeed, score, consumeSeconds
local gameId = 70441007
local mapConfig

function Activity6MiniGameSubmitWindow.ReInitData()
end

function Activity6MiniGameSubmitWindow.OnInit(bridgeObj)
```

---

## Activty/baseact/Activity6MiniGameTaskWindow.lua.lua
**Functions:**
- RefreshRewardList
- list.itemRenderer
- itemlist.itemRenderer
- Activity6MiniGameTaskWindow.ReInitData
- Activity6MiniGameTaskWindow.OnInit
- Activity6MiniGameTaskWindow.UpdateInfo
- Activity6MiniGameTaskWindow.InitBtn
- Activity6MiniGameTaskWindow.OnClose
**Requires:**
- ActivityDungeon1005_MiniTaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1005_MiniTaskWindowByName")
local Activity6MiniGameTaskWindow = {}
local uis, contentPane
local gameId = 70441007

local function RefreshRewardList()
  local info = Activity6_MiniGameData.GetMiniGameInfo(gameId)
  local minigame_tasks = info.taskList
  local list = uis.Main.TipsList
  list:SetVirtual()
```

---

## Activty/baseact/Activity6MiniGameWindow.lua.lua
**Functions:**
- Activity6MiniGameWindow.ReInitData
- Activity6MiniGameWindow.OnInit
- GetDifficulties
- Activity6MiniGameWindow.UpdateInfo
- Activity6MiniGameWindow.InitBtn
- Activity6MiniGameWindow.OnClose
- Activity6MiniGameWindow.HandleMessage
**Requires:**
- ActivityDungeon1005_MiniGameStartWindowByName
- Activity6_MiniGameController
**Snippet:**
```lua
require("ActivityDungeon1005_MiniGameStartWindowByName")
local Activity6MiniGameWindow = {}
local uis, contentPane
local controller = require("Activity6_MiniGameController")
local ballObjLookup, ballFreezingHolderLookup, ballTextLookup, score
local gameId = 70441007
local mapObj, config, shapeMode
local WorldToScreenPoint = function(x, y)
  local cam = UICamera
  local sp = cam:WorldToScreenPoint(Vector3(x, y, 0))
```

---

## Activty/baseact/Activity6PassportLevelUpTipsWindow.lua.lua
**Functions:**
- Activity6PassportLevelUpTipsWindow.ReInitData
- Activity6PassportLevelUpTipsWindow.OnInit
- Activity6PassportLevelUpTipsWindow.UpdateInfo
- Activity6PassportLevelUpTipsWindow.InitBtn
- Activity6PassportLevelUpTipsWindow.OnClose
**Requires:**
- ActivityDungeon1005_PassportUp_LevelUpTipsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1005_PassportUp_LevelUpTipsWindowByName")
local Activity6PassportLevelUpTipsWindow = {}
local uis, contentPane, lv

function Activity6PassportLevelUpTipsWindow.ReInitData()
end

function Activity6PassportLevelUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity6PassportLevelUpTipsWindow.package, WinResConfig.Activity6PassportLevelUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity6PassportWindow.lua.lua
**Functions:**
- Activity6PassportWindow.ReInitData
- Activity6PassportWindow.OnInit
- Activity6PassportWindow.UpdateTextDisplay
- Activity6PassportWindow.InitPassport
- uis.Main.TabRegion.TabList.itemRenderer
- Activity6PassportWindow.InitEffect
- Activity6PassportWindow.InitLv
- Activity6PassportWindow.ShowLevelUp
- Activity6PassportWindow.SaveLevel
- Activity6PassportWindow.GetRewardByLv
- Activity6PassportWindow.GetRewardNum
- Activity6PassportWindow.IsGetAllReward
- Activity6PassportWindow.ShowReward
- Activity6PassportWindow.GetUpdateLv
- Activity6PassportWindow.RefreshListReward
- Activity6PassportWindow.CheckItemTime
- Activity6PassportWindow.ShowQuitTips
- Activity6PassportWindow.RefreshUI
- Activity6PassportWindow.GetExpMxp
- Activity6PassportWindow.SetLevelInfo
- Activity6PassportWindow.InitList
- list.itemRenderer
- Activity6PassportWindow.SetListPos
- Activity6PassportWindow.RefreshReward
- Activity6PassportWindow.ShowGetEffect
- Activity6PassportWindow.RewardItemClick
- Activity6PassportWindow.IsReward
- Activity6PassportWindow.RefreshRewardFirst
- Activity6PassportWindow.RefreshRewardEnd
- Activity6PassportWindow.ShowState
- Activity6PassportWindow.RefreshRewardShow
- Activity6PassportWindow.RefreshRewardState
- Activity6PassportWindow.PassportActivate
- Activity6PassportWindow.CloseWindow
- Activity6PassportWindow.InitBtn
- Activity6PassportWindow.ShowExpBarAnim
- Activity6PassportWindow.InitTask
- list.itemRenderer
- Activity6PassportWindow.InitClothes
- clothes.BuyReward.RewardList.itemRenderer
- Activity6PassportWindow.SetLastLv
- Activity6PassportWindow.PlayFirstRewardEffect
- Activity6PassportWindow.PlayEndRewardEffect
- Activity6PassportWindow.HandleMessage
- Activity6PassportWindow.OnShown
- Activity6PassportWindow.OnClose
**Requires:**
- ActivityDungeon1005_PassportWindowByName
**Snippet:**
```lua
require("ActivityDungeon1005_PassportWindowByName")
local Activity6PassportWindow = {}
local uis, contentPane, passInfo, lvMax, modelType, expMax, rewardData, rewardType, rewardLv, listPage, passLv, jumpTb, isShowAllGet, passPortConfig, lvTween, lastLv, waitMessageId, newPassPort, animTween

function Activity6PassportWindow.ReInitData()
end

function Activity6PassportWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity6PassportWindow.package, WinResConfig.Activity6PassportWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity6PlotWindow.lua.lua
**Functions:**
- Activity6PlotWindow.ReInitData
- Activity6PlotWindow.OnInit
- Activity6PlotWindow.UpdateInfo
- list.itemRenderer
- Activity6PlotWindow.InitBtn
- Activity6PlotWindow.CloseWindow
- Activity6PlotWindow.OnClose
**Requires:**
- ActivityDungeon1005_PlotWindowByName
**Snippet:**
```lua
require("ActivityDungeon1005_PlotWindowByName")
local Activity6PlotWindow = {}
local uis, contentPane, configData

function Activity6PlotWindow.ReInitData()
end

function Activity6PlotWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity6PlotWindow.package, WinResConfig.Activity6PlotWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity6ShopWindow.lua.lua
**Functions:**
- Activity6ShopWindow.ReInitData
- Activity6ShopWindow.OnInit
- Activity6ShopWindow.UpdateInfo
- uis.Main.ItemList.itemRenderer
- Activity6ShopWindow.ShowItem
- list.itemRenderer
- Activity6ShopWindow.ShowOneReward
- list.itemRenderer
- Activity6ShopWindow.GetShopGrid
- Activity6ShopWindow.InitBtn
- Activity6ShopWindow.CloseWindow
- Activity6ShopWindow.OnClose
- Activity6ShopWindow.HandleMessage
**Requires:**
- ActivityDungeon1005_ShopWindowByName
**Snippet:**
```lua
require("ActivityDungeon1005_ShopWindowByName")
local Activity6ShopWindow = {}
local uis, contentPane, activityInfo, tempAssetsTips

function Activity6ShopWindow.ReInitData()
end

function Activity6ShopWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity6ShopWindow.package, WinResConfig.Activity6ShopWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity6SignWindow.lua.lua
**Functions:**
- Activity6SignWindow.ReInitData
- Activity6SignWindow.OnInit
- Activity6SignWindow.UpdateInfo
- list.RewardList.itemRenderer
- Activity6SignWindow.ShowAllItemFrame
- Activity6SignWindow.GetRewardData
- Activity6SignWindow.InitBtn
- Activity6SignWindow.CloseWindow
- Activity6SignWindow.OnClose
**Requires:**
- ActivityDungeon1005_SignWindowByName
**Snippet:**
```lua
require("ActivityDungeon1005_SignWindowByName")
local Activity6SignWindow = {}
local uis, contentPane, activityInfo

function Activity6SignWindow.ReInitData()
end

function Activity6SignWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity6SignWindow.package, WinResConfig.Activity6SignWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity6TaskWindow.lua.lua
**Functions:**
- Activity6TaskWindow.ReInitData
- Activity6TaskWindow.OnInit
- Activity6TaskWindow.UpdateInfo
- list.itemRenderer
- rewardList.itemRenderer
- Activity6TaskWindow.GetRewardNum
- Activity6TaskWindow.ShowAllItemFrame
- Activity6TaskWindow.SortTask
- Activity6TaskWindow.InitBtn
- Activity6TaskWindow.CloseWindow
- Activity6TaskWindow.OnClose
**Requires:**
- ActivityDungeon1005_TaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1005_TaskWindowByName")
local Activity6TaskWindow = {}
local uis, contentPane

function Activity6TaskWindow.ReInitData()
end

function Activity6TaskWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity6TaskWindow.package, WinResConfig.Activity6TaskWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity6_MiniGameController.lua.lua
**Functions:**
- DOTweenRollToEnd
- DOTweenConnect
- CollectBoomBall
- DestroyMatchedBalls
**Requires:**
- VertexPath
**Snippet:**
```lua
ld("Physics")
local VertexPath = require("VertexPath")
local GAP = 0
local BALL_RADIUS = 0.24
local BALL_DIAMETER = 2 * BALL_RADIUS
local CLOSE_TERMINAL_DIST_PERCENT = 0.2
local MOVE_FORWARD_SPEED_WHEN_CLOSE_TERMINAL = 0.2
local MOVE_FORWARD_SPEED = 0.5
local INITIAL_NUM = 18
local LAUNCH_SPEED = 8
```

---

## Activty/baseact/Activity6_MiniGameData.lua.lua
**Snippet:**
```lua
local miniGameInfoDict
local fish = {}
local SetMiniGameInfo = function(info)
  miniGameInfoDict = miniGameInfoDict or {}
  miniGameInfoDict[info.gameId] = info
end
local GetMiniGameInfo = function(gameId)
  if miniGameInfoDict then
    return miniGameInfoDict[gameId]
  end
```

---

## Activty/baseact/Activity6_MiniGameScriptList.lua.lua
**Requires:**
- Activity6_MiniGameData
- Activity6_MiniGameService
**Snippet:**
```lua
Activity6_MiniGameData = require("Activity6_MiniGameData")
Activity6_MiniGameService = require("Activity6_MiniGameService")
```

---

## Activty/baseact/Activity6_MiniGameService.lua.lua
**Snippet:**
```lua
local MiniGameInfoReq = function(gameId, rspCallback)
  local info = ActivityDungeonData.GetActivityInfo()
  local activityId = info.baseInfo.activityId
  Net.Send(Proto.MsgName.ActivityGetMiniGameReq, {activityId = activityId, gameId = gameId}, rspCallback)
end
local MiniGameInfoRsp = function(msg)
  Activity6_MiniGameData.SetMiniGameInfo(msg)
  UIMgr:SendWindowMessage(WinResConfig.Activity6MiniGameMainWindow.name, WindowMsgEnum.Activity6_MiniGame.REFRESH_MINIGAME_INFO)
  UIMgr:SendWindowMessage(WinResConfig.Activity6MiniGameWindow.name, WindowMsgEnum.Activity6_MiniGame.REFRESH_MINIGAME_INFO)
  RedDotMgr.UpdateNode(RED_DOT_DATA_TYPE.ACTIVITY_DUNGENON)
```

---

## Activty/baseact/Activity7BossBattleWindow.lua.lua
**Functions:**
- Activity7BossBattleWindow.ReInitData
- Activity7BossBattleWindow.OnInit
- Activity7BossBattleWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity7BossBattleWindow.FormatRemainTime
- Activity7BossBattleWindow.GetChapter
- Activity7BossBattleWindow.InitBtn
- Activity7BossBattleWindow.CloseWindow
- Activity7BossBattleWindow.OnClose
**Requires:**
- ActivityDungeon1006_BossBattleWindowByName
**Snippet:**
```lua
require("ActivityDungeon1006_BossBattleWindowByName")
local Activity7BossBattleWindow = {}
local uis, contentPane, activityInfo

function Activity7BossBattleWindow.ReInitData()
end

function Activity7BossBattleWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity7BossBattleWindow.package, WinResConfig.Activity7BossBattleWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity7BuyLevelDesWindow.lua.lua
**Functions:**
- Activity7BuyLevelDesWindow.ReInitData
- Activity7BuyLevelDesWindow.OnInit
- Activity7BuyLevelDesWindow.ShowAssetsTips
- Activity7BuyLevelDesWindow.UpdateTextDisplay
- Activity7BuyLevelDesWindow.Init
- Activity7BuyLevelDesWindow.GetGold
- Activity7BuyLevelDesWindow.ShowReward
- list.itemRenderer
- Activity7BuyLevelDesWindow.GetRewardItem
- Activity7BuyLevelDesWindow.GetLvData
- Activity7BuyLevelDesWindow.GetRewardLvData
- Activity7BuyLevelDesWindow.GetRewardByPhaseId
- Activity7BuyLevelDesWindow.BuyLevelRsp
- Activity7BuyLevelDesWindow.InitBtn
- waitFun
- Activity7BuyLevelDesWindow.HandleMessage
- Activity7BuyLevelDesWindow.OnShown
- Activity7BuyLevelDesWindow.OnClose
**Requires:**
- ActivityDungeon1006_BuyLevelDesWindowByName
**Snippet:**
```lua
require("ActivityDungeon1006_BuyLevelDesWindowByName")
local Activity7BuyLevelDesWindow = {}
local uis, contentPane, lvData, curLv, buyNum, itemId, lvMax, waitFun, rewardData, itemSort, transPlay, firstPlay, tatalGold, passInfo

function Activity7BuyLevelDesWindow.ReInitData()
end

function Activity7BuyLevelDesWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity7BuyLevelDesWindow.package, WinResConfig.Activity7BuyLevelDesWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity7ChallengeWindow.lua.lua
**Functions:**
- Activity7ChallengeWindow.ReInitData
- Activity7ChallengeWindow.OnInit
- Activity7ChallengeWindow.UpdateInfo
- uis.Main.ChapterList.itemRenderer
- Activity7ChallengeWindow.ShoweStage
- Activity7ChallengeWindow.StageItemClick
- Activity7ChallengeWindow.ShopInfo
- Activity7ChallengeWindow.GetChapterPassById
- Activity7ChallengeWindow.GetCurStage
- Activity7ChallengeWindow.GetFirstChapter
- Activity7ChallengeWindow.GetAllChapterId
- Activity7ChallengeWindow.InitBtn
- Activity7ChallengeWindow.CloseWindow
- Activity7ChallengeWindow.OnShown
- Activity7ChallengeWindow.OnClose
**Requires:**
- ActivityDungeon1006_ChallengeWindowByName
**Snippet:**
```lua
require("ActivityDungeon1006_ChallengeWindowByName")
local Activity7ChallengeWindow = {}
local uis, contentPane, activityInfo, scrollingTween

function Activity7ChallengeWindow.ReInitData()
end

function Activity7ChallengeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity7ChallengeWindow.package, WinResConfig.Activity7ChallengeWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity7DungeonWindow.lua.lua
**Functions:**
- Activity7DungeonWindow.ReInitData
- Activity7DungeonWindow.OnInit
- Activity7DungeonWindow.LoadBg
- Activity7DungeonWindow.InitRedDot
- Activity7DungeonWindow.UpdateInfo
- Activity7DungeonWindow.InitBtnTxt
- Activity7DungeonWindow.InitBtn
- Activity7DungeonWindow.OnShown
- Activity7DungeonWindow.OnClose
- Activity7DungeonWindow.HandleMessage
**Requires:**
- ActivityDungeon1006_ActivityDungeonWindowByName
**Snippet:**
```lua
require("ActivityDungeon1006_ActivityDungeonWindowByName")
local Activity7DungeonWindow = {}
local uis, contentPane, jumpTb, configData, activityInfo, effect
local InitMiniGameInfo = function()
  local data = ActivityDungeonData.GetActivityData()
  if data.id == 70440001 then
    ld("Activity1_MiniGame")
    Activity1_MiniGameService.MiniGameInfoReq(function()
      RedDotMgr.AddNode({
        windowName = WinResConfig.Activity7DungeonWindow.name,
```

---

## Activty/baseact/Activity7MaterialWindow.lua.lua
**Functions:**
- Activity7MaterialWindow.ReInitData
- Activity7MaterialWindow.OnInit
- Activity7MaterialWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity7MaterialWindow.GetChapter
- Activity7MaterialWindow.GetMaxCount
- Activity7MaterialWindow.InitBtn
- Activity7MaterialWindow.CloseWindow
- Activity7MaterialWindow.OnShown
- Activity7MaterialWindow.OnClose
**Requires:**
- ActivityDungeon1006_MaterialWindowByName
**Snippet:**
```lua
require("ActivityDungeon1006_MaterialWindowByName")
local Activity7MaterialWindow = {}
local uis, contentPane, activityInfo, maxCount, posX

function Activity7MaterialWindow.ReInitData()
end

function Activity7MaterialWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity7MaterialWindow.package, WinResConfig.Activity7MaterialWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity7MiniGameCountdownWindow.lua.lua
**Functions:**
- Activity7MiniGameCountdownWindow.ReInitData
- Activity7MiniGameCountdownWindow.OnInit
- Activity7MiniGameCountdownWindow.UpdateInfo
- Activity7MiniGameCountdownWindow.InitBtn
- Activity7MiniGameCountdownWindow.OnClose
- Activity7MiniGameCountdownWindow.HandleMessage
**Requires:**
- ActivityDungeon1006_MiniStart_CountdownWindowByName
**Snippet:**
```lua
require("ActivityDungeon1006_MiniStart_CountdownWindowByName")
local Activity7MiniGameCountdownWindow = {}
local uis, contentPane

function Activity7MiniGameCountdownWindow.ReInitData()
end

function Activity7MiniGameCountdownWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity7MiniGameCountdownWindow.package, WinResConfig.Activity7MiniGameCountdownWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity7MiniGameMainWindow.lua.lua
**Functions:**
- RefreshPanelInfo
- Activity7MiniGameMainWindow.ReInitData
- Activity7MiniGameMainWindow.OnInit
- Activity7MiniGameMainWindow.UpdateInfo
- Activity7MiniGameMainWindow.InitBtn
- Activity7MiniGameMainWindow.OnClose
- Activity7MiniGameMainWindow.HandleMessage
**Requires:**
- ActivityDungeon1006_MiniGameWindowByName
**Snippet:**
```lua
require("ActivityDungeon1006_MiniGameWindowByName")
ld("Activity7_MiniGame")
local Activity7MiniGameMainWindow = {}
local uis, contentPane

local function RefreshPanelInfo()
  local info = Activity7_MiniGameData.GetMiniGameInfo()
  local conf = TableData.GetConfig(Activity7_MiniGameData.gameId, "BaseActivityStageGame")
  local str = conf.game_day_reward[1]
  local splits = Split(str, ":")
```

---

## Activty/baseact/Activity7MiniGameRecordWindow.lua.lua
**Functions:**
- Activity7MiniGameRecordWindow.ReInitData
- Activity7MiniGameRecordWindow.OnInit
- Activity7MiniGameRecordWindow.UpdateInfo
- list.itemRenderer
- Activity7MiniGameRecordWindow.GetGameTime
- Activity7MiniGameRecordWindow.InitBtn
- Activity7MiniGameRecordWindow.OnClose
**Requires:**
- ActivityDungeon1006_MiniIntegralWindowByName
**Snippet:**
```lua
require("ActivityDungeon1006_MiniIntegralWindowByName")
local Activity7MiniGameRecordWindow = {}
local uis, contentPane

function Activity7MiniGameRecordWindow.ReInitData()
end

function Activity7MiniGameRecordWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity7MiniGameRecordWindow.package, WinResConfig.Activity7MiniGameRecordWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity7MiniGameSubmitWindow.lua.lua
**Functions:**
- Activity7MiniGameSubmitWindow.ReInitData
- Activity7MiniGameSubmitWindow.OnInit
- Activity7MiniGameSubmitWindow.UpdateInfo
- Activity7MiniGameSubmitWindow.GetGameTime
- Activity7MiniGameSubmitWindow.InitBtn
- Activity7MiniGameSubmitWindow.OnClose
**Requires:**
- ActivityDungeon1006_MiniStart_EndRewardWindowByName
**Snippet:**
```lua
require("ActivityDungeon1006_MiniStart_EndRewardWindowByName")
local Activity7MiniGameSubmitWindow = {}
local uis, contentPane, nowIntegral, stageId

function Activity7MiniGameSubmitWindow.ReInitData()
end

function Activity7MiniGameSubmitWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity7MiniGameSubmitWindow.package, WinResConfig.Activity7MiniGameSubmitWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity7MiniGameTaskWindow.lua.lua
**Functions:**
- RefreshRewardList
- list.itemRenderer
- itemlist.itemRenderer
- Activity7MiniGameTaskWindow.ReInitData
- Activity7MiniGameTaskWindow.OnInit
- Activity7MiniGameTaskWindow.UpdateInfo
- Activity7MiniGameTaskWindow.InitBtn
- Activity7MiniGameTaskWindow.OnClose
**Requires:**
- ActivityDungeon1006_MiniTaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1006_MiniTaskWindowByName")
local Activity7MiniGameTaskWindow = {}
local uis, contentPane

local function RefreshRewardList()
  local info = Activity7_MiniGameData.GetMiniGameInfo()
  local minigame_tasks = info.taskList
  local list = uis.Main.TipsList
  list:SetVirtual()
  
```

---

## Activty/baseact/Activity7MiniGameWindow.lua.lua
**Functions:**
- Activity7MiniGameWindow.ReInitData
- Activity7MiniGameWindow.OnInit
- Activity7MiniGameWindow.UpdateInfo
- Activity7MiniGameWindow.Update
- Activity7MiniGameWindow.HiedTipsEffect
- Activity7MiniGameWindow.InitAllMap
- Activity7MiniGameWindow.CreateItem
- Activity7MiniGameWindow.PlayComb
- Activity7MiniGameWindow.ShowLine
- Activity7MiniGameWindow.GetCornerLineInfo
- Activity7MiniGameWindow.IsLink
- Activity7MiniGameWindow.OneCornerLink
- Activity7MiniGameWindow.CanCornerOne
- Activity7MiniGameWindow.CanCornerTwo
- Activity7MiniGameWindow.TwoCornerLink
- Activity7MiniGameWindow.Y_Link
- Activity7MiniGameWindow.X_Link
- Activity7MiniGameWindow.GetRandomIndex
- Activity7MiniGameWindow.GetGameTime
- Activity7MiniGameWindow.GetCurDifficulty
- Activity7MiniGameWindow.CreateLine
- Activity7MiniGameWindow.CheckCanLine
- Activity7MiniGameWindow.ChangeMap
- Activity7MiniGameWindow.CheckGameOver
- Activity7MiniGameWindow.OnGameOver
- Activity7MiniGameWindow.OnNext
- Activity7MiniGameWindow.InitBtn
- Activity7MiniGameWindow.OnClose
- Activity7MiniGameWindow.HandleMessage
**Requires:**
- ActivityDungeon1006_MiniGameStartWindowByName
**Snippet:**
```lua
require("ActivityDungeon1006_MiniGameStartWindowByName")
local Activity7MiniGameWindow = {}
local uis, contentPane, curGameTime, combTime, combNum, isPause
local rowNum = 7
local columNum = 10
local guideWaitTime = 5
local comboWaitTime = 3.25
local xMove, yMove, gridMap, randomMax, tweener, maps, lineCom, oneItemInfo, twoItemInfo, lineType, oneLineType, twoLinePos, hitTime, tipsInfo1, tipsInfo2, stageId
local LineDirectionEnum = {
  vertical = 1,
```

---

## Activty/baseact/Activity7PassportLevelUpTipsWindow.lua.lua
**Functions:**
- Activity7PassportLevelUpTipsWindow.ReInitData
- Activity7PassportLevelUpTipsWindow.OnInit
- Activity7PassportLevelUpTipsWindow.UpdateInfo
- Activity7PassportLevelUpTipsWindow.InitBtn
- Activity7PassportLevelUpTipsWindow.OnClose
**Requires:**
- ActivityDungeon1006_PassportUp_LevelUpTipsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1006_PassportUp_LevelUpTipsWindowByName")
local Activity7PassportLevelUpTipsWindow = {}
local uis, contentPane, lv

function Activity7PassportLevelUpTipsWindow.ReInitData()
end

function Activity7PassportLevelUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity7PassportLevelUpTipsWindow.package, WinResConfig.Activity7PassportLevelUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity7PassportWindow.lua.lua
**Functions:**
- Activity7PassportWindow.ReInitData
- Activity7PassportWindow.OnInit
- Activity7PassportWindow.UpdateTextDisplay
- Activity7PassportWindow.InitPassport
- uis.Main.TabRegion.TabList.itemRenderer
- Activity7PassportWindow.InitEffect
- Activity7PassportWindow.InitLv
- Activity7PassportWindow.ShowLevelUp
- Activity7PassportWindow.SaveLevel
- Activity7PassportWindow.GetRewardByLv
- Activity7PassportWindow.GetRewardNum
- Activity7PassportWindow.IsGetAllReward
- Activity7PassportWindow.ShowReward
- Activity7PassportWindow.GetUpdateLv
- Activity7PassportWindow.RefreshListReward
- Activity7PassportWindow.CheckItemTime
- Activity7PassportWindow.ShowQuitTips
- Activity7PassportWindow.RefreshUI
- Activity7PassportWindow.GetExpMxp
- Activity7PassportWindow.SetLevelInfo
- Activity7PassportWindow.InitList
- list.itemRenderer
- Activity7PassportWindow.SetListPos
- Activity7PassportWindow.RefreshReward
- Activity7PassportWindow.ShowGetEffect
- Activity7PassportWindow.RewardItemClick
- Activity7PassportWindow.IsReward
- Activity7PassportWindow.RefreshRewardFirst
- Activity7PassportWindow.RefreshRewardEnd
- Activity7PassportWindow.ShowState
- Activity7PassportWindow.RefreshRewardShow
- Activity7PassportWindow.RefreshRewardState
- Activity7PassportWindow.PassportActivate
- Activity7PassportWindow.CloseWindow
- Activity7PassportWindow.InitBtn
- Activity7PassportWindow.ShowExpBarAnim
- Activity7PassportWindow.InitTask
- list.itemRenderer
- Activity7PassportWindow.InitClothes
- clothes.BuyReward.RewardList.itemRenderer
- Activity7PassportWindow.SetLastLv
- Activity7PassportWindow.PlayFirstRewardEffect
- Activity7PassportWindow.PlayEndRewardEffect
- Activity7PassportWindow.HandleMessage
- Activity7PassportWindow.OnShown
- Activity7PassportWindow.OnClose
**Requires:**
- ActivityDungeon1006_PassportWindowByName
**Snippet:**
```lua
require("ActivityDungeon1006_PassportWindowByName")
local Activity7PassportWindow = {}
local uis, contentPane, passInfo, lvMax, modelType, expMax, rewardData, rewardType, rewardLv, listPage, passLv, jumpTb, isShowAllGet, passPortConfig, lvTween, lastLv, waitMessageId, newPassPort, animTween

function Activity7PassportWindow.ReInitData()
end

function Activity7PassportWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity7PassportWindow.package, WinResConfig.Activity7PassportWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity7PlotWindow.lua.lua
**Functions:**
- Activity7PlotWindow.ReInitData
- Activity7PlotWindow.OnInit
- Activity7PlotWindow.UpdateInfo
- list.itemRenderer
- Activity7PlotWindow.InitBtn
- Activity7PlotWindow.CloseWindow
- Activity7PlotWindow.OnClose
**Requires:**
- ActivityDungeon1006_PlotWindowByName
**Snippet:**
```lua
require("ActivityDungeon1006_PlotWindowByName")
local Activity7PlotWindow = {}
local uis, contentPane, configData

function Activity7PlotWindow.ReInitData()
end

function Activity7PlotWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity7PlotWindow.package, WinResConfig.Activity7PlotWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity7ShopWindow.lua.lua
**Functions:**
- Activity7ShopWindow.ReInitData
- Activity7ShopWindow.OnInit
- Activity7ShopWindow.UpdateInfo
- uis.Main.ItemList.itemRenderer
- Activity7ShopWindow.ShowItem
- list.itemRenderer
- Activity7ShopWindow.ShowOneReward
- list.itemRenderer
- Activity7ShopWindow.GetShopGrid
- Activity7ShopWindow.InitBtn
- Activity7ShopWindow.CloseWindow
- Activity7ShopWindow.OnClose
- Activity7ShopWindow.HandleMessage
**Requires:**
- ActivityDungeon1006_ShopWindowByName
**Snippet:**
```lua
require("ActivityDungeon1006_ShopWindowByName")
local Activity7ShopWindow = {}
local uis, contentPane, activityInfo, tempAssetsTips

function Activity7ShopWindow.ReInitData()
end

function Activity7ShopWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity7ShopWindow.package, WinResConfig.Activity7ShopWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity7SignWindow.lua.lua
**Functions:**
- Activity7SignWindow.ReInitData
- Activity7SignWindow.OnInit
- Activity7SignWindow.UpdateInfo
- list.RewardList.itemRenderer
- Activity7SignWindow.ShowAllItemFrame
- Activity7SignWindow.GetRewardData
- Activity7SignWindow.InitBtn
- Activity7SignWindow.CloseWindow
- Activity7SignWindow.OnClose
**Requires:**
- ActivityDungeon1006_SignWindowByName
**Snippet:**
```lua
require("ActivityDungeon1006_SignWindowByName")
local Activity7SignWindow = {}
local uis, contentPane, activityInfo

function Activity7SignWindow.ReInitData()
end

function Activity7SignWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity7SignWindow.package, WinResConfig.Activity7SignWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity7TaskWindow.lua.lua
**Functions:**
- Activity7TaskWindow.ReInitData
- Activity7TaskWindow.OnInit
- Activity7TaskWindow.UpdateInfo
- list.itemRenderer
- rewardList.itemRenderer
- Activity7TaskWindow.GetRewardNum
- Activity7TaskWindow.ShowAllItemFrame
- Activity7TaskWindow.SortTask
- Activity7TaskWindow.InitBtn
- Activity7TaskWindow.CloseWindow
- Activity7TaskWindow.OnClose
**Requires:**
- ActivityDungeon1006_TaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1006_TaskWindowByName")
local Activity7TaskWindow = {}
local uis, contentPane

function Activity7TaskWindow.ReInitData()
end

function Activity7TaskWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity7TaskWindow.package, WinResConfig.Activity7TaskWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity7_MiniGameData.lua.lua
**Functions:**
- Activity7_MiniGameData.SetMiniGameInfo
- Activity7_MiniGameData.GetMiniGameInfo
**Snippet:**
```lua
Activity7_MiniGameData = {gameId = 70441008}
local miniGameInfo

function Activity7_MiniGameData.SetMiniGameInfo(info)
  miniGameInfo = info
end

function Activity7_MiniGameData.GetMiniGameInfo()
  return miniGameInfo
end
```

---

## Activty/baseact/Activity7_MiniGameScriptList.lua.lua
**Requires:**
- Activity7_MiniGameData
- Activity7_MiniGameService
**Snippet:**
```lua
require("Activity7_MiniGameData")
require("Activity7_MiniGameService")
```

---

## Activty/baseact/Activity7_MiniGameService.lua.lua
**Functions:**
- Activity7_MiniGameService.MiniGameInfoReq
- Activity7_MiniGameService.MiniGameInfoRsp
- Activity7_MiniGameService.MiniGameSubmitReq
- Activity7_MiniGameService.MiniGameSubmitRsp
- Activity7_MiniGameService.MiniGameGetDailyRewardReq
- Activity7_MiniGameService.MiniGameGetDailyRewardRsp
- Activity7_MiniGameService.Init
**Snippet:**
```lua
Activity7_MiniGameService = {}
local gameId = Activity7_MiniGameData.gameId

function Activity7_MiniGameService.MiniGameInfoReq(rspCallback)
  local info = ActivityDungeonData.GetActivityInfo()
  local activityId = info.baseInfo.activityId
  Net.Send(Proto.MsgName.ActivityGetMiniGameReq, {gameId = gameId, activityId = activityId}, rspCallback)
end

function Activity7_MiniGameService.MiniGameInfoRsp(msg)
```

---

## Activty/baseact/Activity8BossBattleWindow.lua.lua
**Functions:**
- Activity8BossBattleWindow.ReInitData
- Activity8BossBattleWindow.OnInit
- Activity8BossBattleWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity8BossBattleWindow.FormatRemainTime
- Activity8BossBattleWindow.GetChapter
- Activity8BossBattleWindow.InitBtn
- Activity8BossBattleWindow.CloseWindow
- Activity8BossBattleWindow.OnClose
**Requires:**
- ActivityDungeon1007_BossBattleWindowByName
**Snippet:**
```lua
require("ActivityDungeon1007_BossBattleWindowByName")
local Activity8BossBattleWindow = {}
local uis, contentPane, activityInfo

function Activity8BossBattleWindow.ReInitData()
end

function Activity8BossBattleWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity8BossBattleWindow.package, WinResConfig.Activity8BossBattleWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity8BuyLevelDesWindow.lua.lua
**Functions:**
- Activity8BuyLevelDesWindow.ReInitData
- Activity8BuyLevelDesWindow.OnInit
- Activity8BuyLevelDesWindow.ShowAssetsTips
- Activity8BuyLevelDesWindow.UpdateTextDisplay
- Activity8BuyLevelDesWindow.Init
- Activity8BuyLevelDesWindow.GetGold
- Activity8BuyLevelDesWindow.ShowReward
- list.itemRenderer
- Activity8BuyLevelDesWindow.GetRewardItem
- Activity8BuyLevelDesWindow.GetLvData
- Activity8BuyLevelDesWindow.GetRewardLvData
- Activity8BuyLevelDesWindow.GetRewardByPhaseId
- Activity8BuyLevelDesWindow.BuyLevelRsp
- Activity8BuyLevelDesWindow.InitBtn
- waitFun
- Activity8BuyLevelDesWindow.HandleMessage
- Activity8BuyLevelDesWindow.OnShown
- Activity8BuyLevelDesWindow.OnClose
**Requires:**
- ActivityDungeon1007_BuyLevelDesWindowByName
**Snippet:**
```lua
require("ActivityDungeon1007_BuyLevelDesWindowByName")
local Activity8BuyLevelDesWindow = {}
local uis, contentPane, lvData, curLv, buyNum, itemId, lvMax, waitFun, rewardData, itemSort, transPlay, firstPlay, tatalGold, passInfo

function Activity8BuyLevelDesWindow.ReInitData()
end

function Activity8BuyLevelDesWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity8BuyLevelDesWindow.package, WinResConfig.Activity8BuyLevelDesWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity8ChallengeWindow.lua.lua
**Functions:**
- Activity8ChallengeWindow.ReInitData
- Activity8ChallengeWindow.OnInit
- Activity8ChallengeWindow.UpdateInfo
- uis.Main.ChapterList.itemRenderer
- Activity8ChallengeWindow.ShoweStage
- Activity8ChallengeWindow.StageItemClick
- Activity8ChallengeWindow.ShopInfo
- Activity8ChallengeWindow.GetChapterPassById
- Activity8ChallengeWindow.GetCurStage
- Activity8ChallengeWindow.GetFirstChapter
- Activity8ChallengeWindow.GetAllChapterId
- Activity8ChallengeWindow.InitBtn
- Activity8ChallengeWindow.CloseWindow
- Activity8ChallengeWindow.OnShown
- Activity8ChallengeWindow.OnClose
**Requires:**
- ActivityDungeon1007_ChallengeWindowByName
**Snippet:**
```lua
require("ActivityDungeon1007_ChallengeWindowByName")
local Activity8ChallengeWindow = {}
local uis, contentPane, activityInfo, scrollingTween

function Activity8ChallengeWindow.ReInitData()
end

function Activity8ChallengeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity8ChallengeWindow.package, WinResConfig.Activity8ChallengeWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity8DungeonWindow.lua.lua
**Functions:**
- Activity8DungeonWindow.ReInitData
- Activity8DungeonWindow.OnInit
- Activity8DungeonWindow.LoadBg
- Activity8DungeonWindow.InitRedDot
- Activity8DungeonWindow.UpdateInfo
- Activity8DungeonWindow.InitBtnTxt
- Activity8DungeonWindow.InitBtn
- Activity8DungeonWindow.OnShown
- Activity8DungeonWindow.OnClose
- Activity8DungeonWindow.HandleMessage
**Requires:**
- ActivityDungeon1007_ActivityDungeonWindowByName
**Snippet:**
```lua
require("ActivityDungeon1007_ActivityDungeonWindowByName")
local Activity8DungeonWindow = {}
local uis, contentPane, jumpTb, configData, activityInfo, effect
local InitMiniGameInfo = function()
  local data = ActivityDungeonData.GetActivityData()
  if data.id == 70440001 then
    ld("Activity1_MiniGame")
    Activity1_MiniGameService.MiniGameInfoReq(function()
      RedDotMgr.AddNode({
        windowName = WinResConfig.Activity8DungeonWindow.name,
```

---

## Activty/baseact/Activity8MaterialWindow.lua.lua
**Functions:**
- Activity8MaterialWindow.ReInitData
- Activity8MaterialWindow.OnInit
- Activity8MaterialWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity8MaterialWindow.GetChapter
- Activity8MaterialWindow.GetMaxCount
- Activity8MaterialWindow.InitBtn
- Activity8MaterialWindow.CloseWindow
- Activity8MaterialWindow.OnShown
- Activity8MaterialWindow.OnClose
**Requires:**
- ActivityDungeon1007_MaterialWindowByName
**Snippet:**
```lua
require("ActivityDungeon1007_MaterialWindowByName")
local Activity8MaterialWindow = {}
local uis, contentPane, activityInfo, maxCount, posX

function Activity8MaterialWindow.ReInitData()
end

function Activity8MaterialWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity8MaterialWindow.package, WinResConfig.Activity8MaterialWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity8MiniGameExplainWindow.lua.lua
**Functions:**
- Activity8MiniGameExplainWindow.ReInitData
- Activity8MiniGameExplainWindow.OnInit
- Activity8MiniGameExplainWindow.UpdateInfo
- uis.Main.Tips.Word1List.itemRenderer
- uis.Main.Tips.Word2List.itemRenderer
- uis.Main.Tips.Word3List.itemRenderer
- Activity8MiniGameExplainWindow.InitBtn
- Activity8MiniGameExplainWindow.OnClose
**Requires:**
- ActivityDungeon1007_MiniExplainWindowByName
**Snippet:**
```lua
require("ActivityDungeon1007_MiniExplainWindowByName")
local Activity8MiniGameExplainWindow = {}
local uis, contentPane

function Activity8MiniGameExplainWindow.ReInitData()
end

function Activity8MiniGameExplainWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity8MiniGameExplainWindow.package, WinResConfig.Activity8MiniGameExplainWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity8MiniGameGuideWindow.lua.lua
**Functions:**
- Activity8MiniGameGuideWindow.ReInitData
- Activity8MiniGameGuideWindow.OnInit
- Activity8MiniGameGuideWindow.UpdateInfo
- Activity8MiniGameGuideWindow.InitBtn
- Activity8MiniGameGuideWindow.OnClose
**Requires:**
- ActivityDungeon1007_MiniOperationWindowByName
**Snippet:**
```lua
require("ActivityDungeon1007_MiniOperationWindowByName")
local Activity8MiniGameGuideWindow = {}
local uis, contentPane

function Activity8MiniGameGuideWindow.ReInitData()
end

function Activity8MiniGameGuideWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity8MiniGameGuideWindow.package, WinResConfig.Activity8MiniGameGuideWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity8MiniGameMainWindow.lua.lua
**Functions:**
- Activity8MiniGameMainWindow.ReInitData
- Activity8MiniGameMainWindow.OnInit
- Activity8MiniGameMainWindow.UpdateInfo
- Activity8MiniGameMainWindow.InitBtn
- Activity8MiniGameMainWindow.OnClose
- Activity8MiniGameMainWindow.HandleMessage
**Requires:**
- ActivityDungeon1007_MiniGameWindowByName
**Snippet:**
```lua
require("ActivityDungeon1007_MiniGameWindowByName")
ld("Activity8_MiniGame")
local Activity8MiniGameMainWindow = {}
local uis, contentPane
local gameId = 70441009
local RefreshPanelInfo = function()
  local info = Activity8_MiniGameData.GetMiniGameInfo(gameId)
  local conf = TableData.GetConfig(gameId, "BaseActivityStageGame")
  local str = conf.game_day_reward[1]
  local splits = Split(str, ":")
```

---

## Activty/baseact/Activity8MiniGameRecordWindow.lua.lua
**Functions:**
- Activity8MiniGameRecordWindow.ReInitData
- Activity8MiniGameRecordWindow.OnInit
- Activity8MiniGameRecordWindow.UpdateInfo
- list.itemRenderer
- Activity8MiniGameRecordWindow.InitBtn
- Activity8MiniGameRecordWindow.OnClose
**Requires:**
- ActivityDungeon1007_MiniIntegralWindowByName
**Snippet:**
```lua
require("ActivityDungeon1007_MiniIntegralWindowByName")
local Activity8MiniGameRecordWindow = {}
local uis, contentPane
local gameId = 70441009

function Activity8MiniGameRecordWindow.ReInitData()
end

function Activity8MiniGameRecordWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity8MiniGameRecordWindow.package, WinResConfig.Activity8MiniGameRecordWindow.comName, function(com)
```

---

## Activty/baseact/Activity8MiniGameSubmitWindow.lua.lua
**Functions:**
- Activity8MiniGameSubmitWindow.ReInitData
- Activity8MiniGameSubmitWindow.OnInit
- Activity8MiniGameSubmitWindow.UpdateInfo
- Activity8MiniGameSubmitWindow.InitBtn
- Activity8MiniGameSubmitWindow.OnClose
**Requires:**
- ActivityDungeon1007_MiniStart_EndRewardWindowByName
**Snippet:**
```lua
require("ActivityDungeon1007_MiniStart_EndRewardWindowByName")
local Activity8MiniGameSubmitWindow = {}
local uis, contentPane, succeed, score, consumeSeconds
local gameId = 70441009

function Activity8MiniGameSubmitWindow.ReInitData()
end

function Activity8MiniGameSubmitWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity8MiniGameSubmitWindow.package, WinResConfig.Activity8MiniGameSubmitWindow.comName, function(com)
```

---

## Activty/baseact/Activity8MiniGameTaskWindow.lua.lua
**Functions:**
- RefreshRewardList
- list.itemRenderer
- itemlist.itemRenderer
- Activity8MiniGameTaskWindow.ReInitData
- Activity8MiniGameTaskWindow.OnInit
- Activity8MiniGameTaskWindow.UpdateInfo
- Activity8MiniGameTaskWindow.InitBtn
- Activity8MiniGameTaskWindow.OnClose
**Requires:**
- ActivityDungeon1007_MiniTaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1007_MiniTaskWindowByName")
local Activity8MiniGameTaskWindow = {}
local uis, contentPane
local gameId = 70441009

local function RefreshRewardList()
  local info = Activity8_MiniGameData.GetMiniGameInfo(gameId)
  local minigame_tasks = info.taskList
  local list = uis.Main.TipsList
  list:SetVirtual()
```

---

## Activty/baseact/Activity8MiniGameWindow.lua.lua
**Functions:**
- Activity8MiniGameWindow.ReInitData
- Activity8MiniGameWindow.OnInit
- Activity8MiniGameWindow.UpdateInfo
- list.itemRenderer
- Activity8MiniGameWindow.InitBtn
- Activity8MiniGameWindow.OnClose
- Activity8MiniGameWindow.HandleMessage
**Requires:**
- ActivityDungeon1007_MiniGameStartWindowByName
- Activity8_MiniGameController
**Snippet:**
```lua
require("ActivityDungeon1007_MiniGameStartWindowByName")
local Activity8MiniGameWindow = {}
local uis, contentPane
local gameId = 70441009
local controller = require("Activity8_MiniGameController")
local playerObj, touchable, pressTime, increase, dottedLine, fullLine
local Screen2WorldPosition = function(global)
  local cam = StageCamera.main
  local position = cam:ScreenToWorldPoint(Vector3(global.x, Screen.height - global.y, -cam.transform.position.z))
  return position
```

---

## Activty/baseact/Activity8PassportLevelUpTipsWindow.lua.lua
**Functions:**
- Activity8PassportLevelUpTipsWindow.ReInitData
- Activity8PassportLevelUpTipsWindow.OnInit
- Activity8PassportLevelUpTipsWindow.UpdateInfo
- Activity8PassportLevelUpTipsWindow.InitBtn
- Activity8PassportLevelUpTipsWindow.OnClose
**Requires:**
- ActivityDungeon1007_PassportUp_LevelUpTipsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1007_PassportUp_LevelUpTipsWindowByName")
local Activity8PassportLevelUpTipsWindow = {}
local uis, contentPane, lv

function Activity8PassportLevelUpTipsWindow.ReInitData()
end

function Activity8PassportLevelUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity8PassportLevelUpTipsWindow.package, WinResConfig.Activity8PassportLevelUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity8PassportWindow.lua.lua
**Functions:**
- Activity8PassportWindow.ReInitData
- Activity8PassportWindow.OnInit
- Activity8PassportWindow.UpdateTextDisplay
- Activity8PassportWindow.InitPassport
- uis.Main.TabRegion.TabList.itemRenderer
- Activity8PassportWindow.InitEffect
- Activity8PassportWindow.InitLv
- Activity8PassportWindow.ShowLevelUp
- Activity8PassportWindow.SaveLevel
- Activity8PassportWindow.GetRewardByLv
- Activity8PassportWindow.GetRewardNum
- Activity8PassportWindow.IsGetAllReward
- Activity8PassportWindow.ShowReward
- Activity8PassportWindow.GetUpdateLv
- Activity8PassportWindow.RefreshListReward
- Activity8PassportWindow.CheckItemTime
- Activity8PassportWindow.ShowQuitTips
- Activity8PassportWindow.RefreshUI
- Activity8PassportWindow.GetExpMxp
- Activity8PassportWindow.SetLevelInfo
- Activity8PassportWindow.InitList
- list.itemRenderer
- Activity8PassportWindow.SetListPos
- Activity8PassportWindow.RefreshReward
- Activity8PassportWindow.ShowGetEffect
- Activity8PassportWindow.RewardItemClick
- Activity8PassportWindow.IsReward
- Activity8PassportWindow.RefreshRewardFirst
- Activity8PassportWindow.RefreshRewardEnd
- Activity8PassportWindow.ShowState
- Activity8PassportWindow.RefreshRewardShow
- Activity8PassportWindow.RefreshRewardState
- Activity8PassportWindow.PassportActivate
- Activity8PassportWindow.CloseWindow
- Activity8PassportWindow.InitBtn
- Activity8PassportWindow.ShowExpBarAnim
- Activity8PassportWindow.InitTask
- list.itemRenderer
- Activity8PassportWindow.InitClothes
- clothes.BuyReward.RewardList.itemRenderer
- Activity8PassportWindow.SetLastLv
- Activity8PassportWindow.PlayFirstRewardEffect
- Activity8PassportWindow.PlayEndRewardEffect
- Activity8PassportWindow.HandleMessage
- Activity8PassportWindow.OnShown
- Activity8PassportWindow.OnClose
**Requires:**
- ActivityDungeon1007_PassportWindowByName
**Snippet:**
```lua
require("ActivityDungeon1007_PassportWindowByName")
local Activity8PassportWindow = {}
local uis, contentPane, passInfo, lvMax, modelType, expMax, rewardData, rewardType, rewardLv, listPage, passLv, jumpTb, isShowAllGet, passPortConfig, lvTween, lastLv, waitMessageId, newPassPort, animTween

function Activity8PassportWindow.ReInitData()
end

function Activity8PassportWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity8PassportWindow.package, WinResConfig.Activity8PassportWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity8PlotWindow.lua.lua
**Functions:**
- Activity8PlotWindow.ReInitData
- Activity8PlotWindow.OnInit
- Activity8PlotWindow.UpdateInfo
- list.itemRenderer
- Activity8PlotWindow.InitBtn
- Activity8PlotWindow.CloseWindow
- Activity8PlotWindow.OnClose
**Requires:**
- ActivityDungeon1007_PlotWindowByName
**Snippet:**
```lua
require("ActivityDungeon1007_PlotWindowByName")
local Activity8PlotWindow = {}
local uis, contentPane, configData

function Activity8PlotWindow.ReInitData()
end

function Activity8PlotWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity8PlotWindow.package, WinResConfig.Activity8PlotWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity8ShopWindow.lua.lua
**Functions:**
- Activity8ShopWindow.ReInitData
- Activity8ShopWindow.OnInit
- Activity8ShopWindow.UpdateInfo
- uis.Main.ItemList.itemRenderer
- Activity8ShopWindow.ShowItem
- list.itemRenderer
- Activity8ShopWindow.ShowOneReward
- list.itemRenderer
- Activity8ShopWindow.GetShopGrid
- Activity8ShopWindow.InitBtn
- Activity8ShopWindow.CloseWindow
- Activity8ShopWindow.OnClose
- Activity8ShopWindow.HandleMessage
**Requires:**
- ActivityDungeon1007_ShopWindowByName
**Snippet:**
```lua
require("ActivityDungeon1007_ShopWindowByName")
local Activity8ShopWindow = {}
local uis, contentPane, activityInfo, tempAssetsTips

function Activity8ShopWindow.ReInitData()
end

function Activity8ShopWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity8ShopWindow.package, WinResConfig.Activity8ShopWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity8SignWindow.lua.lua
**Functions:**
- Activity8SignWindow.ReInitData
- Activity8SignWindow.OnInit
- Activity8SignWindow.UpdateInfo
- list.RewardList.itemRenderer
- Activity8SignWindow.ShowAllItemFrame
- Activity8SignWindow.GetRewardData
- Activity8SignWindow.InitBtn
- Activity8SignWindow.CloseWindow
- Activity8SignWindow.OnClose
**Requires:**
- ActivityDungeon1007_SignWindowByName
**Snippet:**
```lua
require("ActivityDungeon1007_SignWindowByName")
local Activity8SignWindow = {}
local uis, contentPane, activityInfo

function Activity8SignWindow.ReInitData()
end

function Activity8SignWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity8SignWindow.package, WinResConfig.Activity8SignWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity8TaskWindow.lua.lua
**Functions:**
- Activity8TaskWindow.ReInitData
- Activity8TaskWindow.OnInit
- Activity8TaskWindow.UpdateInfo
- list.itemRenderer
- rewardList.itemRenderer
- Activity8TaskWindow.GetRewardNum
- Activity8TaskWindow.ShowAllItemFrame
- Activity8TaskWindow.SortTask
- Activity8TaskWindow.InitBtn
- Activity8TaskWindow.CloseWindow
- Activity8TaskWindow.OnClose
**Requires:**
- ActivityDungeon1007_TaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1007_TaskWindowByName")
local Activity8TaskWindow = {}
local uis, contentPane

function Activity8TaskWindow.ReInitData()
end

function Activity8TaskWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity8TaskWindow.package, WinResConfig.Activity8TaskWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity8_MiniGameController.lua.lua
**Snippet:**
```lua
ld("Physics")
local GRAVITY = 16
local VERTICAL_JUMP_IMPULSE_MIN = 6.5
local VERTICAL_JUMP_IMPULSE_FACTOR = 4
local VERTICAL_JUMP_IMPULSE_MAX = 12
local HORIZONTAL_JUMP_IMPULSE_FACTOR = 6.5
local HORIZONTAL_JUMP_IMPULSE_MIN = 4.5
local HORIZONTAL_JUMP_IMPULSE_MAX = 15
local HORIZONTAL_JUMP_IMPULSE_EXTEND_MAX = 15
local EXTEND_ITEM_GET_NUM = 3
```

---

## Activty/baseact/Activity8_MiniGameData.lua.lua
**Snippet:**
```lua
local miniGameInfoDict
local fish = {}
local SetMiniGameInfo = function(info)
  miniGameInfoDict = miniGameInfoDict or {}
  miniGameInfoDict[info.gameId] = info
end
local GetMiniGameInfo = function(gameId)
  if miniGameInfoDict then
    return miniGameInfoDict[gameId]
  end
```

---

## Activty/baseact/Activity8_MiniGameScriptList.lua.lua
**Requires:**
- Activity8_MiniGameData
- Activity8_MiniGameService
**Snippet:**
```lua
Activity8_MiniGameData = require("Activity8_MiniGameData")
Activity8_MiniGameService = require("Activity8_MiniGameService")
```

---

## Activty/baseact/Activity8_MiniGameService.lua.lua
**Snippet:**
```lua
local gameId = 70441009
local MiniGameInfoReq = function(rspCallback)
  local info = ActivityDungeonData.GetActivityStageByShowId(8)
  local activityId = info.baseInfo.activityId
  Net.Send(Proto.MsgName.ActivityGetMiniGameReq, {activityId = activityId, gameId = gameId}, rspCallback)
end
local MiniGameInfoRsp = function(msg)
  Activity8_MiniGameData.SetMiniGameInfo(msg)
  UIMgr:SendWindowMessage(WinResConfig.Activity8MiniGameMainWindow.name, WindowMsgEnum.Activity8_MiniGame.REFRESH_MINIGAME_INFO)
  UIMgr:SendWindowMessage(WinResConfig.Activity8MiniGameWindow.name, WindowMsgEnum.Activity8_MiniGame.REFRESH_MINIGAME_INFO)
```

---

## Activty/baseact/Activity9BossBattleWindow.lua.lua
**Functions:**
- Activity9BossBattleWindow.ReInitData
- Activity9BossBattleWindow.OnInit
- Activity9BossBattleWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity9BossBattleWindow.FormatRemainTime
- Activity9BossBattleWindow.GetChapter
- Activity9BossBattleWindow.InitBtn
- Activity9BossBattleWindow.CloseWindow
- Activity9BossBattleWindow.OnClose
**Requires:**
- ActivityDungeon1008_BossBattleWindowByName
**Snippet:**
```lua
require("ActivityDungeon1008_BossBattleWindowByName")
local Activity9BossBattleWindow = {}
local uis, contentPane, activityInfo

function Activity9BossBattleWindow.ReInitData()
end

function Activity9BossBattleWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity9BossBattleWindow.package, WinResConfig.Activity9BossBattleWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity9BuyLevelDesWindow.lua.lua
**Functions:**
- Activity9BuyLevelDesWindow.ReInitData
- Activity9BuyLevelDesWindow.OnInit
- Activity9BuyLevelDesWindow.ShowAssetsTips
- Activity9BuyLevelDesWindow.UpdateTextDisplay
- Activity9BuyLevelDesWindow.Init
- Activity9BuyLevelDesWindow.GetGold
- Activity9BuyLevelDesWindow.ShowReward
- list.itemRenderer
- Activity9BuyLevelDesWindow.GetRewardItem
- Activity9BuyLevelDesWindow.GetLvData
- Activity9BuyLevelDesWindow.GetRewardLvData
- Activity9BuyLevelDesWindow.GetRewardByPhaseId
- Activity9BuyLevelDesWindow.BuyLevelRsp
- Activity9BuyLevelDesWindow.InitBtn
- waitFun
- Activity9BuyLevelDesWindow.HandleMessage
- Activity9BuyLevelDesWindow.OnShown
- Activity9BuyLevelDesWindow.OnClose
**Requires:**
- ActivityDungeon1008_BuyLevelDesWindowByName
**Snippet:**
```lua
require("ActivityDungeon1008_BuyLevelDesWindowByName")
local Activity9BuyLevelDesWindow = {}
local uis, contentPane, lvData, curLv, buyNum, itemId, lvMax, waitFun, rewardData, itemSort, transPlay, firstPlay, tatalGold, passInfo

function Activity9BuyLevelDesWindow.ReInitData()
end

function Activity9BuyLevelDesWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity9BuyLevelDesWindow.package, WinResConfig.Activity9BuyLevelDesWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity9ChallengeWindow.lua.lua
**Functions:**
- Activity9ChallengeWindow.ReInitData
- Activity9ChallengeWindow.OnInit
- Activity9ChallengeWindow.UpdateInfo
- uis.Main.ChapterList.itemRenderer
- Activity9ChallengeWindow.ShoweStage
- Activity9ChallengeWindow.StageItemClick
- Activity9ChallengeWindow.ShopInfo
- Activity9ChallengeWindow.GetChapterPassById
- Activity9ChallengeWindow.GetCurStage
- Activity9ChallengeWindow.GetFirstChapter
- Activity9ChallengeWindow.GetAllChapterId
- Activity9ChallengeWindow.InitBtn
- Activity9ChallengeWindow.CloseWindow
- Activity9ChallengeWindow.OnShown
- Activity9ChallengeWindow.OnClose
**Requires:**
- ActivityDungeon1008_ChallengeWindowByName
**Snippet:**
```lua
require("ActivityDungeon1008_ChallengeWindowByName")
local Activity9ChallengeWindow = {}
local uis, contentPane, activityInfo, scrollingTween

function Activity9ChallengeWindow.ReInitData()
end

function Activity9ChallengeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity9ChallengeWindow.package, WinResConfig.Activity9ChallengeWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity9DungeonWindow.lua.lua
**Functions:**
- Activity9DungeonWindow.ReInitData
- Activity9DungeonWindow.OnInit
- Activity9DungeonWindow.InitRedDot
- Activity9DungeonWindow.UpdateInfo
- Activity9DungeonWindow.InitBtnTxt
- Activity9DungeonWindow.InitBtn
- Activity9DungeonWindow.OnShown
- Activity9DungeonWindow.OnHide
- Activity9DungeonWindow.OnClose
- Activity9DungeonWindow.HandleMessage
**Requires:**
- ActivityDungeon1008_ActivityDungeonWindowByName
**Snippet:**
```lua
require("ActivityDungeon1008_ActivityDungeonWindowByName")
local Activity9DungeonWindow = {}
local uis, contentPane, jumpTb, configData, activityInfo, effect, eventTipsRoot, cursors, cursorRoot, soundEvent, reviewMode, soundSource, soundEvt3D
local OnPopupEventTips = function(events)
  local parent = uis.Main.root
  if not eventTipsRoot then
    eventTipsRoot = UIMgr:CreateObject("ActivityDungeon1008", "EventTipsList")
    eventTipsRoot.opaque = false
    local childIndex = parent:GetChildIndex(uis.Main.BackGround.root)
    parent:AddChildAt(eventTipsRoot, childIndex + 1)
```

---

## Activty/baseact/Activity9EntranceAnimWindow.lua.lua
**Functions:**
- FindChild
- PlayDailyEntranceAnim
- Activity9EntranceAnimWindow.ReInitData
- Activity9EntranceAnimWindow.OnInit
- Activity9EntranceAnimWindow.UpdateInfo
- Activity9EntranceAnimWindow.InitBtn
- Activity9EntranceAnimWindow.OnClose
**Requires:**
- ActivityDungeon1008_MainSeasonsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1008_MainSeasonsWindowByName")
local Activity9EntranceAnimWindow = {}
local uis, contentPane, touchable
local setSpritesColor = function(go, color, fadeout)
  local spriteRenderers = go:GetComponentsInChildren(typeof(CS.UnityEngine.SpriteRenderer))
  if spriteRenderers then
    for i = 0, spriteRenderers.Length - 1 do
      local sr = spriteRenderers[i]
      if fadeout then
        color.a = math.min(color.a, sr.color.a)
```

---

## Activty/baseact/Activity9MaterialWindow.lua.lua
**Functions:**
- Activity9MaterialWindow.ReInitData
- Activity9MaterialWindow.OnInit
- Activity9MaterialWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- Activity9MaterialWindow.GetChapter
- Activity9MaterialWindow.GetMaxCount
- Activity9MaterialWindow.InitBtn
- Activity9MaterialWindow.CloseWindow
- Activity9MaterialWindow.OnShown
- Activity9MaterialWindow.OnClose
**Requires:**
- ActivityDungeon1008_MaterialWindowByName
**Snippet:**
```lua
require("ActivityDungeon1008_MaterialWindowByName")
local Activity9MaterialWindow = {}
local uis, contentPane, activityInfo, maxCount, posX

function Activity9MaterialWindow.ReInitData()
end

function Activity9MaterialWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity9MaterialWindow.package, WinResConfig.Activity9MaterialWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity9MiniGameChoiceWindow.lua.lua
**Functions:**
- Activity9MiniGameChoiceWindow.ReInitData
- Activity9MiniGameChoiceWindow.OnInit
- Activity9MiniGameChoiceWindow.UpdateInfo
- list.itemRenderer
- Activity9MiniGameChoiceWindow.GetMapData
- Activity9MiniGameChoiceWindow.InitBtn
- Activity9MiniGameChoiceWindow.OnClose
**Requires:**
- ActivityDungeon1008_MiniGameChoiceWindowByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniGameChoiceWindowByName")
local Activity9MiniGameChoiceWindow = {}
local uis, contentPane, stageData

function Activity9MiniGameChoiceWindow.ReInitData()
end

function Activity9MiniGameChoiceWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity9MiniGameChoiceWindow.package, WinResConfig.Activity9MiniGameChoiceWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity9MiniGameMainWindow.lua.lua
**Functions:**
- RefreshPanelInfo
- Activity9MiniGameMainWindow.ReInitData
- Activity9MiniGameMainWindow.OnInit
- Activity9MiniGameMainWindow.UpdateInfo
- Activity9MiniGameMainWindow.InitBtn
- Activity9MiniGameMainWindow.OnClose
- Activity9MiniGameMainWindow.HandleMessage
**Requires:**
- ActivityDungeon1008_MiniGameWindowByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniGameWindowByName")
ld("Activity9_MiniGame")
local Activity9MiniGameMainWindow = {}
local uis, contentPane

local function RefreshPanelInfo()
  local info = Activity9_MiniGameData.GetOneMiniGameInfo()
  local conf = TableData.GetConfig(Activity9_MiniGameData.gameId, "BaseActivityStageGame")
  local str = conf.game_day_reward[1]
  local splits = Split(str, ":")
```

---

## Activty/baseact/Activity9MiniGameRecordWindow.lua.lua
**Functions:**
- Activity9MiniGameRecordWindow.ReInitData
- Activity9MiniGameRecordWindow.OnInit
- Activity9MiniGameRecordWindow.UpdateInfo
- list.itemRenderer
- Activity9MiniGameRecordWindow.GetGameTime
- Activity9MiniGameRecordWindow.InitBtn
- Activity9MiniGameRecordWindow.OnClose
**Requires:**
- ActivityDungeon1008_MiniIntegralWindowByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniIntegralWindowByName")
local Activity9MiniGameRecordWindow = {}
local uis, contentPane

function Activity9MiniGameRecordWindow.ReInitData()
end

function Activity9MiniGameRecordWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity9MiniGameRecordWindow.package, WinResConfig.Activity9MiniGameRecordWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity9MiniGameSubmitWindow.lua.lua
**Functions:**
- Activity9MiniGameSubmitWindow.ReInitData
- Activity9MiniGameSubmitWindow.OnInit
- Activity9MiniGameSubmitWindow.UpdateInfo
- Activity9MiniGameSubmitWindow.CanPassAllStage
- Activity9MiniGameSubmitWindow.InitBtn
- Activity9MiniGameSubmitWindow.OnClose
**Requires:**
- ActivityDungeon1008_MiniStart_EndRewardWindowByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniStart_EndRewardWindowByName")
local Activity9MiniGameSubmitWindow = {}
local uis, contentPane, nowIntegral, stageId, fail

function Activity9MiniGameSubmitWindow.ReInitData()
end

function Activity9MiniGameSubmitWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity9MiniGameSubmitWindow.package, WinResConfig.Activity9MiniGameSubmitWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity9MiniGameTaskWindow.lua.lua
**Functions:**
- RefreshRewardList
- list.itemRenderer
- itemlist.itemRenderer
- Activity9MiniGameTaskWindow.ReInitData
- Activity9MiniGameTaskWindow.OnInit
- Activity9MiniGameTaskWindow.UpdateInfo
- Activity9MiniGameTaskWindow.InitBtn
- Activity9MiniGameTaskWindow.OnClose
**Requires:**
- ActivityDungeon1008_MiniTaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniTaskWindowByName")
local Activity9MiniGameTaskWindow = {}
local uis, contentPane

local function RefreshRewardList()
  local info = Activity9_MiniGameData.GetOneMiniGameInfo()
  local minigame_tasks = info.taskList
  local list = uis.Main.TipsList
  list:SetVirtual()
  
```

---

## Activty/baseact/Activity9MiniGameWindow.lua.lua
**Functions:**
- Activity9MiniGameWindow.ReInitData
- Activity9MiniGameWindow.OnInit
- Activity9MiniGameWindow.UpdateInfo
- Activity9MiniGameWindow.SetCanEatNum
- Activity9MiniGameWindow.MonsterNew
- monster:Control
- monster:GetDeathScore
- monster:EnterDeath
- monster:TimeUp
- monster:ChangeMode
- monster:SetAnimation
- monster:StopTwwen
- monster:GetTargetByDis
- monster:Move
- monster:GetRootByType
- monster:GetBlueTarget
- monster:GetGreenTarget
- monster:GetPinkTarget
- monster:GetTarget
- monster:AutoMove
- Activity9MiniGameWindow.ItemNew
- item:SetAnimation
- item:PlayEatAnimation
- Activity9MiniGameWindow.RefreshHp
- Activity9MiniGameWindow.RefreshScore
- Activity9MiniGameWindow.InitPosition
- Activity9MiniGameWindow.GetGridByPos
- Activity9MiniGameWindow.Update
- Activity9MiniGameWindow.GetJoystickDirCom
- Activity9MiniGameWindow.MonsterPaused
- Activity9MiniGameWindow.CheckDeath
- Activity9MiniGameWindow.MonsterControl
- Activity9MiniGameWindow.MonsterEnterFearMode
- Activity9MiniGameWindow.Move
- Activity9MiniGameWindow.CheckEat
- Activity9MiniGameWindow.ResetPos
- Activity9MiniGameWindow.MapCenterFollow
- Activity9MiniGameWindow.CreateTimeItem
- Activity9MiniGameWindow.FindGrid
- Activity9MiniGameWindow.CheckScnceGuide
- Activity9MiniGameWindow.RefreshJoystick
- Activity9MiniGameWindow:InitJoystick
- Activity9MiniGameWindow.GetItemDataByType
- Activity9MiniGameWindow.GetGuideItem
- Activity9MiniGameWindow.InitItemData
- Activity9MiniGameWindow.CheckGameOver
- Activity9MiniGameWindow.OnGameOver
- Activity9MiniGameWindow.OnNext
- Activity9MiniGameWindow.GetCurDifficulty
- Activity9MiniGameWindow.InitBtn
- Activity9MiniGameWindow.OnClose
- Activity9MiniGameWindow.HandleMessage
**Requires:**
- ActivityDungeon1008_MiniGameStartWindowByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniGameStartWindowByName")
local Activity9MiniGameWindow = {}
local uis, contentPane, stageData
local itemData = {}
local timeData = {}
local timeItemInfo = {}
local maxLine = 26
local gridWidth = 36
local eatWidth = 35
local guideCom, mapCom, mapFollowTwwen, moveTwwen, deathTwwen
```

---

## Activty/baseact/Activity9MiniOperateChoiceWindow.lua.lua
**Functions:**
- Activity9MiniOperateChoiceWindow.ReInitData
- Activity9MiniOperateChoiceWindow.OnInit
- Activity9MiniOperateChoiceWindow.UpdateInfo
- uis.Main.TipsList.itemRenderer
- uis.Main.TipsList.itemRenderer
- Activity9MiniOperateChoiceWindow.InitBtn
- Activity9MiniOperateChoiceWindow.CloseWindow
- Activity9MiniOperateChoiceWindow.OnClose
**Requires:**
- ActivityDungeon1008_MiniOperateChoiceWindowByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniOperateChoiceWindowByName")
local Activity9MiniOperateChoiceWindow = {}
local uis, contentPane, fromWindowName

function Activity9MiniOperateChoiceWindow.ReInitData()
end

function Activity9MiniOperateChoiceWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity9MiniOperateChoiceWindow.package, WinResConfig.Activity9MiniOperateChoiceWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity9PassportLevelUpTipsWindow.lua.lua
**Functions:**
- Activity9PassportLevelUpTipsWindow.ReInitData
- Activity9PassportLevelUpTipsWindow.OnInit
- Activity9PassportLevelUpTipsWindow.UpdateInfo
- Activity9PassportLevelUpTipsWindow.InitBtn
- Activity9PassportLevelUpTipsWindow.OnClose
**Requires:**
- ActivityDungeon1008_PassportUp_LevelUpTipsWindowByName
**Snippet:**
```lua
require("ActivityDungeon1008_PassportUp_LevelUpTipsWindowByName")
local Activity9PassportLevelUpTipsWindow = {}
local uis, contentPane, lv

function Activity9PassportLevelUpTipsWindow.ReInitData()
end

function Activity9PassportLevelUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity9PassportLevelUpTipsWindow.package, WinResConfig.Activity9PassportLevelUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity9PassportWindow.lua.lua
**Functions:**
- Activity9PassportWindow.ReInitData
- Activity9PassportWindow.OnInit
- Activity9PassportWindow.UpdateTextDisplay
- Activity9PassportWindow.InitPassport
- uis.Main.TabRegion.TabList.itemRenderer
- Activity9PassportWindow.InitEffect
- Activity9PassportWindow.InitLv
- Activity9PassportWindow.ShowLevelUp
- Activity9PassportWindow.SaveLevel
- Activity9PassportWindow.GetRewardByLv
- Activity9PassportWindow.GetRewardNum
- Activity9PassportWindow.IsGetAllReward
- Activity9PassportWindow.ShowReward
- Activity9PassportWindow.GetUpdateLv
- Activity9PassportWindow.RefreshListReward
- Activity9PassportWindow.CheckItemTime
- Activity9PassportWindow.ShowQuitTips
- Activity9PassportWindow.RefreshUI
- Activity9PassportWindow.GetExpMxp
- Activity9PassportWindow.SetLevelInfo
- Activity9PassportWindow.InitList
- list.itemRenderer
- Activity9PassportWindow.SetListPos
- Activity9PassportWindow.RefreshReward
- Activity9PassportWindow.ShowGetEffect
- Activity9PassportWindow.RewardItemClick
- Activity9PassportWindow.IsReward
- Activity9PassportWindow.RefreshRewardFirst
- Activity9PassportWindow.RefreshRewardEnd
- Activity9PassportWindow.ShowState
- Activity9PassportWindow.RefreshRewardShow
- Activity9PassportWindow.RefreshRewardState
- Activity9PassportWindow.PassportActivate
- Activity9PassportWindow.CloseWindow
- Activity9PassportWindow.InitBtn
- Activity9PassportWindow.ShowExpBarAnim
- Activity9PassportWindow.InitTask
- list.itemRenderer
- Activity9PassportWindow.InitClothes
- clothes.BuyReward.RewardList.itemRenderer
- Activity9PassportWindow.SetLastLv
- Activity9PassportWindow.PlayFirstRewardEffect
- Activity9PassportWindow.PlayEndRewardEffect
- Activity9PassportWindow.HandleMessage
- Activity9PassportWindow.OnShown
- Activity9PassportWindow.OnClose
**Requires:**
- ActivityDungeon1008_PassportWindowByName
**Snippet:**
```lua
require("ActivityDungeon1008_PassportWindowByName")
local Activity9PassportWindow = {}
local uis, contentPane, passInfo, lvMax, modelType, expMax, rewardData, rewardType, rewardLv, listPage, passLv, jumpTb, isShowAllGet, passPortConfig, lvTween, lastLv, waitMessageId, newPassPort, animTween

function Activity9PassportWindow.ReInitData()
end

function Activity9PassportWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity9PassportWindow.package, WinResConfig.Activity9PassportWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity9PlotWindow.lua.lua
**Functions:**
- Activity9PlotWindow.ReInitData
- Activity9PlotWindow.OnInit
- Activity9PlotWindow.UpdateInfo
- list.itemRenderer
- Activity9PlotWindow.InitBtn
- Activity9PlotWindow.CloseWindow
- Activity9PlotWindow.OnClose
**Requires:**
- ActivityDungeon1008_PlotWindowByName
**Snippet:**
```lua
require("ActivityDungeon1008_PlotWindowByName")
local Activity9PlotWindow = {}
local uis, contentPane, configData

function Activity9PlotWindow.ReInitData()
end

function Activity9PlotWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity9PlotWindow.package, WinResConfig.Activity9PlotWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity9ShopWindow.lua.lua
**Functions:**
- Activity9ShopWindow.ReInitData
- Activity9ShopWindow.OnInit
- Activity9ShopWindow.UpdateInfo
- uis.Main.ItemList.itemRenderer
- Activity9ShopWindow.ShowItem
- list.itemRenderer
- Activity9ShopWindow.ShowOneReward
- list.itemRenderer
- Activity9ShopWindow.GetShopGrid
- Activity9ShopWindow.InitBtn
- Activity9ShopWindow.CloseWindow
- Activity9ShopWindow.OnClose
- Activity9ShopWindow.HandleMessage
**Requires:**
- ActivityDungeon1008_ShopWindowByName
**Snippet:**
```lua
require("ActivityDungeon1008_ShopWindowByName")
local Activity9ShopWindow = {}
local uis, contentPane, activityInfo, tempAssetsTips

function Activity9ShopWindow.ReInitData()
end

function Activity9ShopWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity9ShopWindow.package, WinResConfig.Activity9ShopWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity9SignWindow.lua.lua
**Functions:**
- Activity9SignWindow.ReInitData
- Activity9SignWindow.OnInit
- Activity9SignWindow.UpdateInfo
- list.RewardList.itemRenderer
- Activity9SignWindow.ShowAllItemFrame
- Activity9SignWindow.GetRewardData
- Activity9SignWindow.InitBtn
- Activity9SignWindow.CloseWindow
- Activity9SignWindow.OnClose
**Requires:**
- ActivityDungeon1008_SignWindowByName
**Snippet:**
```lua
require("ActivityDungeon1008_SignWindowByName")
local Activity9SignWindow = {}
local uis, contentPane, activityInfo

function Activity9SignWindow.ReInitData()
end

function Activity9SignWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity9SignWindow.package, WinResConfig.Activity9SignWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity9SnakeGameMainWindow.lua.lua
**Functions:**
- RefreshPanelInfo
- Activity9SnakeGameMainWindow.ReInitData
- Activity9SnakeGameMainWindow.OnInit
- Activity9SnakeGameMainWindow.UpdateInfo
- Activity9SnakeGameMainWindow.InitBtn
- Activity9SnakeGameMainWindow.OnClose
- Activity9SnakeGameMainWindow.HandleMessage
**Requires:**
- ActivityDungeon1008_MiniGame2WindowByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniGame2WindowByName")
local Activity9SnakeGameMainWindow = {}
local uis, contentPane

local function RefreshPanelInfo()
  local gameId = Activity9_MiniGameData.snakeGameId
  local info = Activity9_MiniGameData.GetOneMiniGameInfo(gameId)
  local conf = TableData.GetConfig(gameId, "BaseActivityStageGame")
  local str = conf.game_day_reward[1]
  local splits = Split(str, ":")
```

---

## Activty/baseact/Activity9SnakeGameRecordWindow.lua.lua
**Functions:**
- Activity9SnakeGameRecordWindow.ReInitData
- Activity9SnakeGameRecordWindow.OnInit
- Activity9SnakeGameRecordWindow.UpdateInfo
- list.itemRenderer
- Activity9SnakeGameRecordWindow.GetGameTime
- Activity9SnakeGameRecordWindow.InitBtn
- Activity9SnakeGameRecordWindow.OnClose
**Requires:**
- ActivityDungeon1008_MiniIntegral2WindowByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniIntegral2WindowByName")
local Activity9SnakeGameRecordWindow = {}
local uis, contentPane

function Activity9SnakeGameRecordWindow.ReInitData()
end

function Activity9SnakeGameRecordWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity9SnakeGameRecordWindow.package, WinResConfig.Activity9SnakeGameRecordWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity9SnakeGameResultWindow.lua.lua
**Functions:**
- Activity9SnakeGameResultWindow.ReInitData
- Activity9SnakeGameResultWindow.OnInit
- Activity9SnakeGameResultWindow.UpdateInfo
- Activity9SnakeGameResultWindow.InitBtn
- Activity9SnakeGameResultWindow.OnClose
**Requires:**
- ActivityDungeon1008_MiniStart2_EndRewardWindowByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniStart2_EndRewardWindowByName")
local Activity9SnakeGameResultWindow = {}
local uis, contentPane

function Activity9SnakeGameResultWindow.ReInitData()
end

function Activity9SnakeGameResultWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity9SnakeGameResultWindow.package, WinResConfig.Activity9SnakeGameResultWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity9SnakeGameTaskWindow.lua.lua
**Functions:**
- RefreshRewardList
- list.itemRenderer
- itemlist.itemRenderer
- Activity9SnakeGameTaskWindow.ReInitData
- Activity9SnakeGameTaskWindow.OnInit
- Activity9SnakeGameTaskWindow.UpdateInfo
- Activity9SnakeGameTaskWindow.InitBtn
- Activity9SnakeGameTaskWindow.OnClose
**Requires:**
- ActivityDungeon1008_MiniTask2WindowByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniTask2WindowByName")
local Activity9SnakeGameTaskWindow = {}
local uis, contentPane

local function RefreshRewardList()
  local gameId = Activity9_MiniGameData.snakeGameId
  local info = Activity9_MiniGameData.GetOneMiniGameInfo(gameId)
  local minigame_tasks = info.taskList
  local list = uis.Main.TipsList
  list:SetVirtual()
```

---

## Activty/baseact/Activity9SnakeGameWindow.lua.lua
**Functions:**
- Activity9SnakeGameWindow.ReInitData
- Activity9SnakeGameWindow.CreateGrid
- grid:Init
- grid:GetNextGrid
- Activity9SnakeGameWindow.CreateSnake
- snake:AddPart
- snake:Init
- snake:Move
- snake:MoveToNext
- snake:EatFood
- snake:ChangeDirection
- snake:Destroy
- Activity9SnakeGameWindow.CreateSnakePart
- part:Init
- part:CreateModel
- part:SetMoveTargetGrid
- part:ChangeUIController
- part:SetVisible
- part:Move
- part:UpdatePosition
- part:Destroy
- Activity9SnakeGameWindow.CreateFood
- food:Init
- food:ChoosePosition
- food:CreateModel
- food:UpdatePosition
- food:Destroy
- Activity9SnakeGameWindow.OnInit
- Activity9SnakeGameWindow.UpdateInfo
- Activity9SnakeGameWindow.InitBtn
- Activity9SnakeGameWindow.UpdateScore
- Activity9SnakeGameWindow.InitGameInfo
- Activity9SnakeGameWindow.InitMap
- Activity9SnakeGameWindow.InitSnake
- Activity9SnakeGameWindow.StartGame
- Activity9SnakeGameWindow.StartTimer
- Activity9SnakeGameWindow.StopTimer
- Activity9SnakeGameWindow.UpdateGame
- Activity9SnakeGameWindow.PauseGame
- Activity9SnakeGameWindow.ResumeGame
- Activity9SnakeGameWindow.StopGame
- Activity9SnakeGameWindow.GameOver
- Activity9SnakeGameWindow.OnClose
- Activity9SnakeGameWindow.RefreshJoystick
- Activity9SnakeGameWindow:InitJoystick
- Activity9SnakeGameWindow.Update
- Activity9SnakeGameWindow.OnNext
- Activity9SnakeGameWindow.ClearCache
- Activity9SnakeGameWindow.HandleMessage
**Requires:**
- ActivityDungeon1008_MiniGameStart2WindowByName
**Snippet:**
```lua
require("ActivityDungeon1008_MiniGameStart2WindowByName")
local Activity9SnakeGameWindow = {}
local uis, contentPane

function Activity9SnakeGameWindow.ReInitData()
end

local MOVE_SPEED = 0.12
local curSnake, curSnakeDirection, foodList
local gridWH = 28
```

---

## Activty/baseact/Activity9TaskWindow.lua.lua
**Functions:**
- Activity9TaskWindow.ReInitData
- Activity9TaskWindow.OnInit
- Activity9TaskWindow.UpdateInfo
- list.itemRenderer
- rewardList.itemRenderer
- Activity9TaskWindow.GetRewardNum
- Activity9TaskWindow.ShowAllItemFrame
- Activity9TaskWindow.SortTask
- Activity9TaskWindow.InitBtn
- Activity9TaskWindow.CloseWindow
- Activity9TaskWindow.OnClose
**Requires:**
- ActivityDungeon1008_TaskWindowByName
**Snippet:**
```lua
require("ActivityDungeon1008_TaskWindowByName")
local Activity9TaskWindow = {}
local uis, contentPane

function Activity9TaskWindow.ReInitData()
end

function Activity9TaskWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.Activity9TaskWindow.package, WinResConfig.Activity9TaskWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/Activity9_MiniGameData.lua.lua
**Functions:**
- Activity9_MiniGameData.SetMiniGameInfo
- Activity9_MiniGameData.GetMiniGameInfo
- Activity9_MiniGameData.GetOneMiniGameInfo
**Snippet:**
```lua
Activity9_MiniGameData = {gameId = 70441010, snakeGameId = 70441011}
local miniGameInfoDict

function Activity9_MiniGameData.SetMiniGameInfo(info)
  miniGameInfoDict = miniGameInfoDict or {}
  miniGameInfoDict[info.gameId] = info
end

function Activity9_MiniGameData.GetMiniGameInfo(gameId)
  if miniGameInfoDict then
```

---

## Activty/baseact/Activity9_MiniGameGridsDataLoader.lua.lua
**Functions:**
- Activity9_MiniGameGridsDataLoader.Load
- Activity9_MiniGameGridsDataLoader.Transform
- Activity9_MiniGameGridsDataLoader.GetPath
**Snippet:**
```lua
Activity9_MiniGameGridsDataLoader = {}

function Activity9_MiniGameGridsDataLoader.Load(path)
  local bytes = ResourceManager.LoadTextAssetBytes(path)
  local stream = CS.ReadWriteStream(bytes)
  local length = stream:ReadInt32()
  local grids = {}
  for _ = 1, length do
    local coordinate = stream:ReadVector2Int()
    local centerPosition = stream:ReadVector3()
```

---

## Activty/baseact/Activity9_MiniGameScriptList.lua.lua
**Requires:**
- Activity9_MiniGameData
- Activity9_MiniGameService
- Activity9_MiniGameGridsDataLoader
**Snippet:**
```lua
require("Activity9_MiniGameData")
require("Activity9_MiniGameService")
require("Activity9_MiniGameGridsDataLoader")
```

---

## Activty/baseact/Activity9_MiniGameService.lua.lua
**Functions:**
- Activity9_MiniGameService.MiniGameInfoReq
- Activity9_MiniGameService.MiniGameInfoRsp
- Activity9_MiniGameService.MiniGameSubmitReq
- Activity9_MiniGameService.MiniGameSubmitRsp
- Activity9_MiniGameService.MiniGameGetDailyRewardReq
- Activity9_MiniGameService.MiniGameGetDailyRewardRsp
- Activity9_MiniGameService.Init
**Snippet:**
```lua
Activity9_MiniGameService = {}
local cachedGameId

function Activity9_MiniGameService.MiniGameInfoReq(gameId, rspCallback)
  local info = ActivityDungeonData.GetActivityInfo()
  local activityId = info.baseInfo.activityId
  cachedGameId = gameId
  Net.Send(Proto.MsgName.ActivityGetMiniGameReq, {gameId = gameId, activityId = activityId}, rspCallback)
end

```

---

## Activty/baseact/ActivityBossBattleWindow.lua.lua
**Functions:**
- ActivityBossBattleWindow.ReInitData
- ActivityBossBattleWindow.OnInit
- ActivityBossBattleWindow.UpdateInfo
- uis.Main.BattleList.itemRenderer
- ActivityBossBattleWindow.FormatRemainTime
- ActivityBossBattleWindow.GetChapter
- ActivityBossBattleWindow.InitBtn
- ActivityBossBattleWindow.CloseWindow
- ActivityBossBattleWindow.OnClose
**Requires:**
- ActivityDungeon1_BossBattleWindowByName
**Snippet:**
```lua
require("ActivityDungeon1_BossBattleWindowByName")
local ActivityBossBattleWindow = {}
local uis, contentPane, activityInfo

function ActivityBossBattleWindow.ReInitData()
end

function ActivityBossBattleWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ActivityBossBattleWindow.package, WinResConfig.ActivityBossBattleWindow.comName, function(com)
    contentPane = com
```

---

## Activty/baseact/ActivityBuyLevelDesWindow.lua.lua
**Functions:**
- ActivityBuyLevelDesWindow.ReInitData
- ActivityBuyLevelDesWindow.OnInit
- ActivityBuyLevelDesWindow.ShowAssetsTips
- ActivityBuyLevelDesWindow.UpdateTextDisplay
- ActivityBuyLevelDesWindow.Init
- ActivityBuyLevelDesWindow.GetGold
- ActivityBuyLevelDesWindow.ShowReward
- list.itemRenderer
- ActivityBuyLevelDesWindow.GetRewardItem
- ActivityBuyLevelDesWindow.GetLvData
- ActivityBuyLevelDesWindow.GetRewardLvData
- ActivityBuyLevelDesWindow.GetRewardByPhaseId
- ActivityBuyLevelDesWindow.BuyLevelRsp
- ActivityBuyLevelDesWindow.InitBtn
- waitFun
- ActivityBuyLevelDesWindow.HandleMessage
- ActivityBuyLevelDesWindow.OnShown
- ActivityBuyLevelDesWindow.OnClose
**Requires:**
- ActivityDungeon1_BuyLevelDesWindowByName
**Snippet:**
```lua
require("ActivityDungeon1_BuyLevelDesWindowByName")
local ActivityBuyLevelDesWindow = {}
local uis, contentPane, lvData, curLv, buyNum, itemId, lvMax, waitFun, rewardData, itemSort, transPlay, firstPlay, tatalGold, passInfo

function ActivityBuyLevelDesWindow.ReInitData()
end

function ActivityBuyLevelDesWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ActivityBuyLevelDesWindow.package, WinResConfig.ActivityBuyLevelDesWindow.comName, function(com)
    contentPane = com
```

---
