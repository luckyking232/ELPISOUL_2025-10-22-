# other

## other/ScheduleData.lua.lua
**Functions:**
- ScheduleData.SaveInfo
- ScheduleData.GetInfo
**Snippet:**
```lua
ScheduleData = {}
local info

function ScheduleData.SaveInfo(msg)
  info = msg
end

function ScheduleData.GetInfo()
  return info
end
```

---

## other/ScheduleScriptList.lua.lua
**Requires:**
- ScheduleData
- ScheduleService
**Snippet:**
```lua
local require = require
require("ScheduleData")
require("ScheduleService")
```

---

## other/ScheduleService.lua.lua
**Functions:**
- ScheduleService.Init
- ScheduleService.GetFeatureScheduleReq
- ScheduleService.GetFeatureScheduleRsp
- ScheduleService.ManorBatchProcessEventReq
- ScheduleService.ManorBatchProcessEventRsp
**Snippet:**
```lua
ScheduleService = {}

function ScheduleService.Init()
  Net.AddListener(Proto.MsgName.GetFeatureScheduleRsp, ScheduleService.GetFeatureScheduleRsp)
  Net.AddListener(Proto.MsgName.ManorBatchProcessEventRsp, ScheduleService.ManorBatchProcessEventRsp)
end

function ScheduleService.GetFeatureScheduleReq(rspCallback)
  local msg = {}
  Net.Send(Proto.MsgName.GetFeatureScheduleReq, msg, rspCallback)
```

---

## other/ScheduleWindow.lua.lua
**Functions:**
- ScheduleWindow.ReInitData
- ScheduleWindow.OnInit
- ScheduleWindow.Update
- ScheduleWindow.GetLoadingData
- ScheduleWindow.LoadingShow
- list.itemRenderer
- moduleList.itemRenderer
- ScheduleWindow.UpdateInfo
- ScheduleWindow.ShowTips
- ScheduleWindow.InitMap
- moduleList.itemRenderer
- list.itemRenderer
- ScheduleWindow.SealFormatTime
- ScheduleWindow.GetBuffStageNum
- ScheduleWindow.IsUnlock
- ScheduleWindow.GetWeekTarget
- ScheduleWindow.DisplayHourglass
- ScheduleWindow.GetDispatchInfo
- ScheduleWindow.GetDispatchTeamConfigs
- ScheduleWindow.GetBuildNum
- ScheduleWindow.RogueReward
- ScheduleWindow.ManorBossReward
- ScheduleWindow.BuffStageReward
- ScheduleWindow.InitDaily
- moduleList.itemRenderer
- ScheduleWindow.Arenareward
- ScheduleWindow.GetDayTask
- ScheduleWindow.InitActivity
- list.itemRenderer
- ScheduleWindow.SetPageShow
- pageList.itemRenderer
- ScheduleWindow.ShowActivityInfo
- ScheduleWindow.FinishedTask
- ScheduleWindow.ShowCardActivity
- ScheduleWindow.RaidBossRewards
- ScheduleWindow.ShowBoss
- ScheduleWindow.ShowGuildWar
- ScheduleWindow.ShowLimitTower
- ScheduleWindow.TowerIsOpen
- ScheduleWindow.GetLimitMaxNum
- ScheduleWindow.InitAsset
- assetList.itemRenderer
- itemList.itemRenderer
- ScheduleWindow.GetItemCountByExpire
- ScheduleWindow.InitBtn
- ScheduleWindow.OnShown
- ScheduleWindow.OnClose
- ScheduleWindow.HandleMessage
**Requires:**
- Schedule_ScheduleWindowByName
**Snippet:**
```lua
require("Schedule_ScheduleWindowByName")
local ScheduleWindow = {}
local uis, contentPane

function ScheduleWindow.ReInitData()
end

function ScheduleWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ScheduleWindow.package, WinResConfig.ScheduleWindow.comName, function(com)
    contentPane = com
```

---

## other/Schedule_Asset1ByName.lua.lua
**Functions:**
- GetSchedule_Asset1Uis
**Requires:**
- Schedule_AssetTitleByName
**Snippet:**
```lua
require("Schedule_AssetTitleByName")

function GetSchedule_Asset1Uis(ui)
  local uis = {}
  uis.Title1 = GetSchedule_AssetTitleUis(ui:GetChild("Title1"))
  uis.AssetList = ui:GetChild("AssetList")
  uis.Title2 = GetSchedule_AssetTitleUis(ui:GetChild("Title2"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
```

---

## other/Schedule_AssetByName.lua.lua
**Functions:**
- GetSchedule_AssetUis
**Snippet:**
```lua
function GetSchedule_AssetUis(ui)
  local uis = {}
  
  uis.AssetList = ui:GetChild("AssetList")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_AssetContentByName.lua.lua
**Functions:**
- GetSchedule_AssetContentUis
**Snippet:**
```lua
function GetSchedule_AssetContentUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_AssetTitleByName.lua.lua
**Functions:**
- GetSchedule_AssetTitleUis
**Snippet:**
```lua
function GetSchedule_AssetTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_BoxGetByName.lua.lua
**Functions:**
- GetSchedule_BoxGetUis
**Requires:**
- CommonResource_PopupBgByName
- Schedule_BoxGetTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Schedule_BoxGetTipsByName")

function GetSchedule_BoxGetUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.BoxGetTips = GetSchedule_BoxGetTipsUis(ui:GetChild("BoxGetTips"))
  uis.root = ui
  return uis
```

---

## other/Schedule_BoxGetCloseBtnByName.lua.lua
**Functions:**
- GetSchedule_BoxGetCloseBtnUis
**Snippet:**
```lua
function GetSchedule_BoxGetCloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_BoxGetTipsByName.lua.lua
**Functions:**
- GetSchedule_BoxGetTipsUis
**Requires:**
- Schedule_BoxGetTipsEntryListByName
**Snippet:**
```lua
require("Schedule_BoxGetTipsEntryListByName")

function GetSchedule_BoxGetTipsUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.EntryList = GetSchedule_BoxGetTipsEntryListUis(ui:GetChild("EntryList"))
  uis.root = ui
  return uis
end
```

---

## other/Schedule_BoxGetTipsEntryAniByName.lua.lua
**Functions:**
- GetSchedule_BoxGetTipsEntryAniUis
**Requires:**
- Schedule_BoxGetTipsEntryByName
**Snippet:**
```lua
require("Schedule_BoxGetTipsEntryByName")

function GetSchedule_BoxGetTipsEntryAniUis(ui)
  local uis = {}
  uis.Entry = GetSchedule_BoxGetTipsEntryUis(ui:GetChild("Entry"))
  uis.root = ui
  return uis
end
```

---

## other/Schedule_BoxGetTipsEntryByName.lua.lua
**Functions:**
- GetSchedule_BoxGetTipsEntryUis
**Snippet:**
```lua
function GetSchedule_BoxGetTipsEntryUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_BoxGetTipsEntryListByName.lua.lua
**Functions:**
- GetSchedule_BoxGetTipsEntryListUis
**Snippet:**
```lua
function GetSchedule_BoxGetTipsEntryListUis(ui)
  local uis = {}
  
  uis.EntryList = ui:GetChild("EntryList")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_BoxGetTipsEntryWordByName.lua.lua
**Functions:**
- GetSchedule_BoxGetTipsEntryWordUis
**Snippet:**
```lua
function GetSchedule_BoxGetTipsEntryWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_BoxGetWindowByName.lua.lua
**Functions:**
- GetSchedule_BoxGetWindowUis
**Requires:**
- Schedule_BoxGetByName
**Snippet:**
```lua
require("Schedule_BoxGetByName")

function GetSchedule_BoxGetWindowUis(ui)
  local uis = {}
  uis.Main = GetSchedule_BoxGetUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/Schedule_CloseBtnByName.lua.lua
**Functions:**
- GetSchedule_CloseBtnUis
**Snippet:**
```lua
function GetSchedule_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_CycleByName.lua.lua
**Functions:**
- GetSchedule_CycleUis
**Snippet:**
```lua
function GetSchedule_CycleUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## other/Schedule_CycleDate1ByName.lua.lua
**Functions:**
- GetSchedule_CycleDate1Uis
**Snippet:**
```lua
function GetSchedule_CycleDate1Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_CycleDateByName.lua.lua
**Functions:**
- GetSchedule_CycleDateUis
**Snippet:**
```lua
function GetSchedule_CycleDateUis(ui)
  local uis = {}
  
  uis.NowTxt = ui:GetChild("NowTxt")
  uis.DateTxt = ui:GetChild("DateTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_CycleDateRegionByName.lua.lua
**Functions:**
- GetSchedule_CycleDateRegionUis
**Requires:**
- Schedule_CycleDateByName
**Snippet:**
```lua
require("Schedule_CycleDateByName")

function GetSchedule_CycleDateRegionUis(ui)
  local uis = {}
  uis.CycleDate = GetSchedule_CycleDateUis(ui:GetChild("CycleDate"))
  uis.DateList = ui:GetChild("DateList")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_CycleModuleByName.lua.lua
**Functions:**
- GetSchedule_CycleModuleUis
**Requires:**
- Schedule_CycleModulePicByName
**Snippet:**
```lua
require("Schedule_CycleModulePicByName")

function GetSchedule_CycleModuleUis(ui)
  local uis = {}
  uis.Pic = GetSchedule_CycleModulePicUis(ui:GetChild("Pic"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## other/Schedule_CycleModulePicByName.lua.lua
**Functions:**
- GetSchedule_CycleModulePicUis
**Snippet:**
```lua
function GetSchedule_CycleModulePicUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_CycleTitleByName.lua.lua
**Functions:**
- GetSchedule_CycleTitleUis
**Snippet:**
```lua
function GetSchedule_CycleTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_LeftByName.lua.lua
**Functions:**
- GetSchedule_LeftUis
**Requires:**
- Schedule_LeftModuleLoadingByName
**Snippet:**
```lua
require("Schedule_LeftModuleLoadingByName")

function GetSchedule_LeftUis(ui)
  local uis = {}
  uis.LeftRegionList = ui:GetChild("LeftRegionList")
  uis.PageNumberList = ui:GetChild("PageNumberList")
  uis.Loading = GetSchedule_LeftModuleLoadingUis(ui:GetChild("Loading"))
  uis.c1Ctr = ui:GetController("c1")
  uis.loadingCtr = ui:GetController("loading")
  uis.root = ui
```

---

## other/Schedule_LeftModule1ByName.lua.lua
**Functions:**
- GetSchedule_LeftModule1Uis
**Requires:**
- Schedule_LeftModuleByName
**Snippet:**
```lua
require("Schedule_LeftModuleByName")

function GetSchedule_LeftModule1Uis(ui)
  local uis = {}
  uis.LeftModule = GetSchedule_LeftModuleUis(ui:GetChild("LeftModule"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_LeftModuleByName.lua.lua
**Functions:**
- GetSchedule_LeftModuleUis
**Requires:**
- Schedule_LeftModulePicByName
- Schedule_LeftModuleTimeOpenByName
- Schedule_LeftModuleTimeCloseByName
- Schedule_LeftModuleLockByName
- Schedule_LeftModuleIngByName
- Schedule_LeftModule_GuildBossRankByName
- Schedule_RightModuleRewardByName
**Snippet:**
```lua
require("Schedule_LeftModulePicByName")
require("Schedule_LeftModuleTimeOpenByName")
require("Schedule_LeftModuleTimeCloseByName")
require("Schedule_LeftModuleLockByName")
require("Schedule_LeftModuleIngByName")
require("Schedule_LeftModule_GuildBossRankByName")
require("Schedule_RightModuleRewardByName")

function GetSchedule_LeftModuleUis(ui)
  local uis = {}
```

---

## other/Schedule_LeftModuleIngByName.lua.lua
**Functions:**
- GetSchedule_LeftModuleIngUis
**Snippet:**
```lua
function GetSchedule_LeftModuleIngUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_LeftModuleLoadingByName.lua.lua
**Functions:**
- GetSchedule_LeftModuleLoadingUis
**Snippet:**
```lua
function GetSchedule_LeftModuleLoadingUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_LeftModuleLockByName.lua.lua
**Functions:**
- GetSchedule_LeftModuleLockUis
**Requires:**
- Schedule_LeftModuleLockWordByName
**Snippet:**
```lua
require("Schedule_LeftModuleLockWordByName")

function GetSchedule_LeftModuleLockUis(ui)
  local uis = {}
  uis.MoveWord = GetSchedule_LeftModuleLockWordUis(ui:GetChild("MoveWord"))
  uis.root = ui
  return uis
end
```

---

## other/Schedule_LeftModuleLockWordByName.lua.lua
**Functions:**
- GetSchedule_LeftModuleLockWordUis
**Snippet:**
```lua
function GetSchedule_LeftModuleLockWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_LeftModulePicByName.lua.lua
**Functions:**
- GetSchedule_LeftModulePicUis
**Snippet:**
```lua
function GetSchedule_LeftModulePicUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_LeftModuleTimeCloseByName.lua.lua
**Functions:**
- GetSchedule_LeftModuleTimeCloseUis
**Snippet:**
```lua
function GetSchedule_LeftModuleTimeCloseUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_LeftModuleTimeOpenByName.lua.lua
**Functions:**
- GetSchedule_LeftModuleTimeOpenUis
**Snippet:**
```lua
function GetSchedule_LeftModuleTimeOpenUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_LeftModule_GuildBossRankByName.lua.lua
**Functions:**
- GetSchedule_LeftModule_GuildBossRankUis
**Snippet:**
```lua
function GetSchedule_LeftModule_GuildBossRankUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_LeftPageByName.lua.lua
**Functions:**
- GetSchedule_LeftPageUis
**Snippet:**
```lua
function GetSchedule_LeftPageUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_LeftRegionByName.lua.lua
**Functions:**
- GetSchedule_LeftRegionUis
**Requires:**
- Schedule_LeftModule1ByName
**Snippet:**
```lua
require("Schedule_LeftModule1ByName")

function GetSchedule_LeftRegionUis(ui)
  local uis = {}
  uis.Module1 = GetSchedule_LeftModule1Uis(ui:GetChild("Module1"))
  uis.Module2 = GetSchedule_LeftModule1Uis(ui:GetChild("Module2"))
  uis.Module3 = GetSchedule_LeftModule1Uis(ui:GetChild("Module3"))
  uis.Module4 = GetSchedule_LeftModule1Uis(ui:GetChild("Module4"))
  uis.root = ui
  return uis
```

---

## other/Schedule_RightModule1ByName.lua.lua
**Functions:**
- GetSchedule_RightModule1Uis
**Requires:**
- Schedule_RightModuleTitleByName
**Snippet:**
```lua
require("Schedule_RightModuleTitleByName")

function GetSchedule_RightModule1Uis(ui)
  local uis = {}
  uis.Title = GetSchedule_RightModuleTitleUis(ui:GetChild("Title"))
  uis.ModuleList = ui:GetChild("ModuleList")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_RightModuleByName.lua.lua
**Functions:**
- GetSchedule_RightModuleUis
**Requires:**
- Schedule_RightModule_BuildByName
- Schedule_RightModule_SuperByName
- Schedule_RightModule_RogueByName
- Schedule_RightModule_BoxByName
- Schedule_RightModule_ExploreByName
- Schedule_RightModule_DailyTaskByName
- Schedule_RightModule_ArenaByName
- Schedule_RightModule_InitialEnergyByName
- Schedule_RightModule_ExploreDungeonByName
**Snippet:**
```lua
require("Schedule_RightModule_BuildByName")
require("Schedule_RightModule_SuperByName")
require("Schedule_RightModule_RogueByName")
require("Schedule_RightModule_BoxByName")
require("Schedule_RightModule_ExploreByName")
require("Schedule_RightModule_DailyTaskByName")
require("Schedule_RightModule_ArenaByName")
require("Schedule_RightModule_InitialEnergyByName")
require("Schedule_RightModule_ExploreDungeonByName")

```

---

## other/Schedule_RightModuleLoadingByName.lua.lua
**Functions:**
- GetSchedule_RightModuleLoadingUis
**Snippet:**
```lua
function GetSchedule_RightModuleLoadingUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_RightModuleLockByName.lua.lua
**Functions:**
- GetSchedule_RightModuleLockUis
**Snippet:**
```lua
function GetSchedule_RightModuleLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_RightModuleProgressByName.lua.lua
**Functions:**
- GetSchedule_RightModuleProgressUis
**Snippet:**
```lua
function GetSchedule_RightModuleProgressUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_RightModuleRewardByName.lua.lua
**Functions:**
- GetSchedule_RightModuleRewardUis
**Snippet:**
```lua
function GetSchedule_RightModuleRewardUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_RightModuleTimeCloseByName.lua.lua
**Functions:**
- GetSchedule_RightModuleTimeCloseUis
**Snippet:**
```lua
function GetSchedule_RightModuleTimeCloseUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_RightModuleTimeOpenByName.lua.lua
**Functions:**
- GetSchedule_RightModuleTimeOpenUis
**Snippet:**
```lua
function GetSchedule_RightModuleTimeOpenUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_RightModuleTitleByName.lua.lua
**Functions:**
- GetSchedule_RightModuleTitleUis
**Snippet:**
```lua
function GetSchedule_RightModuleTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_RightModuleTouchBtnByName.lua.lua
**Functions:**
- GetSchedule_RightModuleTouchBtnUis
**Snippet:**
```lua
function GetSchedule_RightModuleTouchBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_RightModule_ArenaByName.lua.lua
**Functions:**
- GetSchedule_RightModule_ArenaUis
**Requires:**
- Schedule_RightModuleTimeCloseByName
- Schedule_RightModuleLockByName
- Schedule_RightModule_ArenaProgressByName
- Schedule_RightModule_ArenaRankByName
- Schedule_RightModuleRewardByName
- Schedule_RightModuleLoadingByName
**Snippet:**
```lua
require("Schedule_RightModuleTimeCloseByName")
require("Schedule_RightModuleLockByName")
require("Schedule_RightModule_ArenaProgressByName")
require("Schedule_RightModule_ArenaRankByName")
require("Schedule_RightModuleRewardByName")
require("Schedule_RightModuleLoadingByName")

function GetSchedule_RightModule_ArenaUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
```

---

## other/Schedule_RightModule_ArenaProgressByName.lua.lua
**Functions:**
- GetSchedule_RightModule_ArenaProgressUis
**Snippet:**
```lua
function GetSchedule_RightModule_ArenaProgressUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_RightModule_ArenaRankByName.lua.lua
**Functions:**
- GetSchedule_RightModule_ArenaRankUis
**Snippet:**
```lua
function GetSchedule_RightModule_ArenaRankUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_RightModule_BoxByName.lua.lua
**Functions:**
- GetSchedule_RightModule_BoxUis
**Requires:**
- Schedule_RightModuleProgressByName
- Schedule_RightModuleLockByName
- Schedule_RightModuleLoadingByName
**Snippet:**
```lua
require("Schedule_RightModuleProgressByName")
require("Schedule_RightModuleLockByName")
require("Schedule_RightModuleLoadingByName")

function GetSchedule_RightModule_BoxUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Progress = GetSchedule_RightModuleProgressUis(ui:GetChild("Progress"))
  uis.Lock = GetSchedule_RightModuleLockUis(ui:GetChild("Lock"))
  uis.TouchBtn = ui:GetChild("TouchBtn")
```

---

## other/Schedule_RightModule_BoxGetBtnByName.lua.lua
**Functions:**
- GetSchedule_RightModule_BoxGetBtnUis
**Snippet:**
```lua
function GetSchedule_RightModule_BoxGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_RightModule_BuildByName.lua.lua
**Functions:**
- GetSchedule_RightModule_BuildUis
**Requires:**
- Schedule_RightModuleTimeOpenByName
- Schedule_RightModuleTimeCloseByName
- Schedule_RightModuleLockByName
- Schedule_RightModule_BuildProgressByName
- Schedule_RightModuleRewardByName
- Schedule_RightModuleLoadingByName
**Snippet:**
```lua
require("Schedule_RightModuleTimeOpenByName")
require("Schedule_RightModuleTimeCloseByName")
require("Schedule_RightModuleLockByName")
require("Schedule_RightModule_BuildProgressByName")
require("Schedule_RightModuleRewardByName")
require("Schedule_RightModuleLoadingByName")

function GetSchedule_RightModule_BuildUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
```

---

## other/Schedule_RightModule_BuildProgressByName.lua.lua
**Functions:**
- GetSchedule_RightModule_BuildProgressUis
**Snippet:**
```lua
function GetSchedule_RightModule_BuildProgressUis(ui)
  local uis = {}
  
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.Word3Txt = ui:GetChild("Word3Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
```

---

## other/Schedule_RightModule_DailyTaskByName.lua.lua
**Functions:**
- GetSchedule_RightModule_DailyTaskUis
**Requires:**
- Schedule_RightModuleTimeCloseByName
- Schedule_RightModuleLockByName
- Schedule_RightModule_DailyTaskProgressByName
- Schedule_RightModuleRewardByName
- Schedule_RightModuleLoadingByName
**Snippet:**
```lua
require("Schedule_RightModuleTimeCloseByName")
require("Schedule_RightModuleLockByName")
require("Schedule_RightModule_DailyTaskProgressByName")
require("Schedule_RightModuleRewardByName")
require("Schedule_RightModuleLoadingByName")

function GetSchedule_RightModule_DailyTaskUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TimeClose = GetSchedule_RightModuleTimeCloseUis(ui:GetChild("TimeClose"))
```

---

## other/Schedule_RightModule_DailyTaskProgressByName.lua.lua
**Functions:**
- GetSchedule_RightModule_DailyTaskProgressUis
**Snippet:**
```lua
function GetSchedule_RightModule_DailyTaskProgressUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_RightModule_ExploreByName.lua.lua
**Functions:**
- GetSchedule_RightModule_ExploreUis
**Requires:**
- Schedule_RightModuleTimeOpenByName
- Schedule_RightModuleLockByName
- Schedule_RightModuleLoadingByName
**Snippet:**
```lua
require("Schedule_RightModuleTimeOpenByName")
require("Schedule_RightModuleLockByName")
require("Schedule_RightModuleLoadingByName")

function GetSchedule_RightModule_ExploreUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TimeOpen = GetSchedule_RightModuleTimeOpenUis(ui:GetChild("TimeOpen"))
  uis.Lock = GetSchedule_RightModuleLockUis(ui:GetChild("Lock"))
  uis.StateList = ui:GetChild("StateList")
```

---

## other/Schedule_RightModule_ExploreDungeonByName.lua.lua
**Functions:**
- GetSchedule_RightModule_ExploreDungeonUis
**Requires:**
- Schedule_RightModuleLockByName
- Schedule_RightModuleLoadingByName
- Schedule_RightModule_ExploreDungeonProgressByName
**Snippet:**
```lua
require("Schedule_RightModuleLockByName")
require("Schedule_RightModuleLoadingByName")
require("Schedule_RightModule_ExploreDungeonProgressByName")

function GetSchedule_RightModule_ExploreDungeonUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Lock = GetSchedule_RightModuleLockUis(ui:GetChild("Lock"))
  uis.Loading = GetSchedule_RightModuleLoadingUis(ui:GetChild("Loading"))
  uis.n11 = GetSchedule_RightModule_ExploreDungeonProgressUis(ui:GetChild("n11"))
```

---

## other/Schedule_RightModule_ExploreDungeonGetBtnByName.lua.lua
**Functions:**
- GetSchedule_RightModule_ExploreDungeonGetBtnUis
**Snippet:**
```lua
function GetSchedule_RightModule_ExploreDungeonGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_RightModule_ExploreDungeonProgressByName.lua.lua
**Functions:**
- GetSchedule_RightModule_ExploreDungeonProgressUis
**Snippet:**
```lua
function GetSchedule_RightModule_ExploreDungeonProgressUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_RightModule_ExploreStateByName.lua.lua
**Functions:**
- GetSchedule_RightModule_ExploreStateUis
**Snippet:**
```lua
function GetSchedule_RightModule_ExploreStateUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_RightModule_InitialEnergyByName.lua.lua
**Functions:**
- GetSchedule_RightModule_InitialEnergyUis
**Requires:**
- Schedule_RightModule_InitialEnergyTimeByName
- Schedule_RightModuleLockByName
- Schedule_RightModule_InitialEnergyProgressByName
- Schedule_RightModuleLoadingByName
**Snippet:**
```lua
require("Schedule_RightModule_InitialEnergyTimeByName")
require("Schedule_RightModuleLockByName")
require("Schedule_RightModule_InitialEnergyProgressByName")
require("Schedule_RightModuleLoadingByName")

function GetSchedule_RightModule_InitialEnergyUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Time = GetSchedule_RightModule_InitialEnergyTimeUis(ui:GetChild("Time"))
  uis.Lock = GetSchedule_RightModuleLockUis(ui:GetChild("Lock"))
```

---

## other/Schedule_RightModule_InitialEnergyGetBtnByName.lua.lua
**Functions:**
- GetSchedule_RightModule_InitialEnergyGetBtnUis
**Snippet:**
```lua
function GetSchedule_RightModule_InitialEnergyGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_RightModule_InitialEnergyProgressByName.lua.lua
**Functions:**
- GetSchedule_RightModule_InitialEnergyProgressUis
**Snippet:**
```lua
function GetSchedule_RightModule_InitialEnergyProgressUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.c4Ctr = ui:GetController("c4")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_RightModule_InitialEnergyTimeByName.lua.lua
**Functions:**
- GetSchedule_RightModule_InitialEnergyTimeUis
**Snippet:**
```lua
function GetSchedule_RightModule_InitialEnergyTimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_RightModule_RogueByName.lua.lua
**Functions:**
- GetSchedule_RightModule_RogueUis
**Requires:**
- Schedule_RightModuleTimeOpenByName
- Schedule_RightModuleTimeCloseByName
- Schedule_RightModuleLockByName
- Schedule_RightModule_RogueProgressByName
- Schedule_RightModuleRewardByName
- Schedule_RightModuleLoadingByName
**Snippet:**
```lua
require("Schedule_RightModuleTimeOpenByName")
require("Schedule_RightModuleTimeCloseByName")
require("Schedule_RightModuleLockByName")
require("Schedule_RightModule_RogueProgressByName")
require("Schedule_RightModuleRewardByName")
require("Schedule_RightModuleLoadingByName")

function GetSchedule_RightModule_RogueUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
```

---

## other/Schedule_RightModule_RogueProgressByName.lua.lua
**Functions:**
- GetSchedule_RightModule_RogueProgressUis
**Snippet:**
```lua
function GetSchedule_RightModule_RogueProgressUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_RightModule_SuperByName.lua.lua
**Functions:**
- GetSchedule_RightModule_SuperUis
**Requires:**
- Schedule_RightModuleTimeOpenByName
- Schedule_RightModuleTimeCloseByName
- Schedule_RightModuleLockByName
- Schedule_RightModule_SuperProgressByName
- Schedule_RightModuleRewardByName
- Schedule_RightModuleLoadingByName
**Snippet:**
```lua
require("Schedule_RightModuleTimeOpenByName")
require("Schedule_RightModuleTimeCloseByName")
require("Schedule_RightModuleLockByName")
require("Schedule_RightModule_SuperProgressByName")
require("Schedule_RightModuleRewardByName")
require("Schedule_RightModuleLoadingByName")

function GetSchedule_RightModule_SuperUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
```

---

## other/Schedule_RightModule_SuperProgressByName.lua.lua
**Functions:**
- GetSchedule_RightModule_SuperProgressUis
**Snippet:**
```lua
function GetSchedule_RightModule_SuperProgressUis(ui)
  local uis = {}
  
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.Word3Txt = ui:GetChild("Word3Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
```

---

## other/Schedule_RightRegionByName.lua.lua
**Functions:**
- GetSchedule_RightRegionUis
**Snippet:**
```lua
function GetSchedule_RightRegionUis(ui)
  local uis = {}
  
  uis.RightRegionList = ui:GetChild("RightRegionList")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_RightWordTipsBtnByName.lua.lua
**Functions:**
- GetSchedule_RightWordTipsBtnUis
**Snippet:**
```lua
function GetSchedule_RightWordTipsBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Schedule_ScheduleByName.lua.lua
**Functions:**
- GetSchedule_ScheduleUis
**Requires:**
- CommonResource_PopupBgByName
- Schedule_ScheduleTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Schedule_ScheduleTipsByName")

function GetSchedule_ScheduleUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.ScheduleTips = GetSchedule_ScheduleTipsUis(ui:GetChild("ScheduleTips"))
  uis.root = ui
  return uis
```

---

## other/Schedule_ScheduleTipsByName.lua.lua
**Functions:**
- GetSchedule_ScheduleTipsUis
**Requires:**
- Schedule_LeftByName
- Schedule_RightRegionByName
- Schedule_AssetByName
**Snippet:**
```lua
require("Schedule_LeftByName")
require("Schedule_RightRegionByName")
require("Schedule_AssetByName")

function GetSchedule_ScheduleTipsUis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.TabSignBtn = ui:GetChild("TabSignBtn")
  uis.RightWordTipsBtn = ui:GetChild("RightWordTipsBtn")
```

---

## other/Schedule_ScheduleWindowByName.lua.lua
**Functions:**
- GetSchedule_ScheduleWindowUis
**Requires:**
- Schedule_ScheduleByName
**Snippet:**
```lua
require("Schedule_ScheduleByName")

function GetSchedule_ScheduleWindowUis(ui)
  local uis = {}
  uis.Main = GetSchedule_ScheduleUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/Schedule_TabSignBtnByName.lua.lua
**Functions:**
- GetSchedule_TabSignBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetSchedule_TabSignBtnUis(ui)
  local uis = {}
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## other/SealData.lua.lua
**Snippet:**
```lua
local sealsInfo, sealJobConfigs, allSeals
local UpdateSealInfo = function(info)
  sealsInfo = sealsInfo or {}
  sealsInfo[info.job] = info
end
local GetAllEquippedSealsInfo = function()
  return sealsInfo
end
local GetEquippedSealsInfoByJob = function(jobId)
  if sealsInfo then
```

---

## other/SealGetTipsWindow.lua.lua
**Functions:**
- SealGetTipsWindow.ReInitData
- SealGetTipsWindow.OnInit
- SealGetTipsWindow.UpdateInfo
- uis.Main.WordList.itemRenderer
- SealGetTipsWindow.GetGoToData
- SealGetTipsWindow.StageIsUnlock
- SealGetTipsWindow.ShowAllGoTo
- uis.Main.Way.GetStripList.itemRenderer
- SealGetTipsWindow.GetCanLvLock
- SealGetTipsWindow.ShowGoTo
- uis.Main.Way.GetStripList.itemRenderer
- SealGetTipsWindow.InitBtn
- SealGetTipsWindow.CloseWindow
- SealGetTipsWindow.OnClose
**Requires:**
- Message_ExploreGetTipsWindowByName
**Snippet:**
```lua
require("Message_ExploreGetTipsWindowByName")
local SealGetTipsWindow = {}
local uis, contentPane, itemConfig, wayData, itemId, itemNeedCount, fromCardId, isJump, jumpData, notShowWay

function SealGetTipsWindow.ReInitData()
end

function SealGetTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.SealGetTipsWindow.package, WinResConfig.SealGetTipsWindow.comName, function(com)
    contentPane = com
```

---

## other/SealMgr.lua.lua
**Snippet:**
```lua
local IsEquipped = function(jobType, attrType)
  local equippedInfo = SealData.GetEquippedSealsInfoByJob(jobType)
  local count = equippedInfo and equippedInfo.sealIds and #equippedInfo.sealIds or 0
  local equipped = false
  if count > 0 then
    for _, sealId in ipairs(equippedInfo.sealIds) do
      local sealConf = TableData.GetConfig(sealId, "BaseSeal")
      if sealConf.attr_type == attrType then
        equipped = sealId
        break
```

---

## other/SealScriptList.lua.lua
**Requires:**
- SealData
- SealMgr
- SealService
**Snippet:**
```lua
SealData = require("SealData")
SealMgr = require("SealMgr")
SealService = require("SealService")
```

---

## other/SealService.lua.lua
**Snippet:**
```lua
local GetEquippedSealInfoReq = function(rspCallback)
  Net.Send(Proto.MsgName.GetSealWearInfoReq, nil, rspCallback)
end
local GetEquippedSealInfoRsp = function(msg)
  local infos = msg.wearInfos
  if infos then
    for i, v in ipairs(infos) do
      SealData.UpdateSealInfo(v)
    end
  end
```

---

## other/SealSynthesisItemTipsWindow.lua.lua
**Functions:**
- SealSynthesisItemTipsWindow.ReInitData
- SealSynthesisItemTipsWindow.OnInit
- SealSynthesisItemTipsWindow.UpdateInfo
- itemlist.itemRenderer
- itemlist.itemRenderer
- SealSynthesisItemTipsWindow.InitBtn
- SealSynthesisItemTipsWindow.OnClose
**Requires:**
- ExploreDevelop_SynthesisItemTipsWindowByName
**Snippet:**
```lua
require("ExploreDevelop_SynthesisItemTipsWindowByName")
local SealSynthesisItemTipsWindow = {}
local uis, contentPane, sealId, combinedCount, resultCount
local LevelText = function(lv_size1, lv_size2, lv_val)
  return string.format("Lv.%s", lv_val)
end

function SealSynthesisItemTipsWindow.ReInitData()
end

```

---

## other/SealSynthesisWindow.lua.lua
**Functions:**
- RefreshUnequippedSeals
- list.itemRenderer
- itemlist.itemRenderer
- RefreshPanelInfo
- AutoAdd
- SealSynthesisWindow.ReInitData
- SealSynthesisWindow.OnInit
- SealSynthesisWindow.UpdateInfo
- tablist.itemRenderer
- SealSynthesisWindow.InitBtn
- SealSynthesisWindow.OnClose
- SealSynthesisWindow.HandleMessage
**Requires:**
- ExploreDevelop_SynthesisWindowByName
**Snippet:**
```lua
require("ExploreDevelop_SynthesisWindowByName")
local SealSynthesisWindow = {}
local uis, RefreshPanelInfo, AutoAdd, contentPane, jobType, tweenerCollection, max, lucky, selectedSlotIndex
local currentSeal, combinedCount = nil, 0
local wait
local IsEmpty = function()
  return nil == currentSeal
end
local HasSeal = function(index)
  if currentSeal then
```

---

## other/SealWindow.lua.lua
**Functions:**
- list.itemRenderer
- RefreshUnequippedSeals
- list.itemRenderer
- itemlist.itemRenderer
- spendList.itemRenderer
- RefreshMainSealPanel
- attributeList.itemRenderer
- attributeList.itemRenderer
- SealWindow.ReInitData
- SealWindow.OnInit
- SealWindow.UpdateInfo
- tablist.itemRenderer
- tablist.itemRenderer
- SealWindow.InitBtn
- detailFunc
- SealWindow.OnShown
- SealWindow.OnClose
- SealWindow.HandleMessage
**Requires:**
- ExploreDevelop_DevelopWindowByName
**Snippet:**
```lua
require("ExploreDevelop_DevelopWindowByName")
local SealWindow = {}
local uis, contentPane, selectedTabIndex, selectedAttrType, selectedMainSealTabIndex, tweenerCollection
local ATTR_TYPE_LOOKUP = {
  [1] = {
    id = ProtoEnum.ATTR_ID.ATK,
    name = T(80000103),
    index = 1
  },
  [2] = {
```

---

## other/Segment.lua.lua
**Functions:**
- Segment:__ctor
- Segment:initMassData
- Segment:containPoint
- Segment:pointRayCasting
**Snippet:**
```lua
local base = Polygon
local Segment = Create("Segment", base)

function Segment:__ctor()
  self.shapeType = ShapeType.Poly
  self.mass = 0
  self.inertia = 0
end

function Segment:initMassData()
```

---

## other/SensitiveWords.lua.lua
**Snippet:**
```lua
SensitiveWords = {
  "㊣",
  "㈱",
  "㈩",
  "㈨",
  "㈧",
  "㈥",
  "㈣",
  "㈢",
  "㈡",
```

---

## other/SensitiveWordsUtil.lua.lua
**Functions:**
- SensitiveWordsUtil.InitWords
- SensitiveWordsUtil.BuildWordTree
- SensitiveWordsUtil.FilterWord
- SensitiveWordsUtil.IsContainBlockedWord
**Requires:**
- SensitiveWords
- TrieTree
**Snippet:**
```lua
SensitiveWordsUtil = {}
local BlockWordTrieTree

function SensitiveWordsUtil.InitWords()
  if SensitiveWords == nil then
    require("SensitiveWords")
    local len = #SensitiveWords
    print(string.format("屏蔽词库共有%d词条", len))
    SensitiveWordsUtil.BuildWordTree()
  end
```

---

## other/SettingUtil.lua.lua
**Functions:**
- SettingUtil.ParseSetting
- SettingUtil.UpdateFPS
- SettingUtil.UpdateWeatherType
- SettingUtil.UpdateSfx
- SettingUtil.UpdateMusic
- SettingUtil.UpdateVoice
- SettingUtil.UpdateSfxVolume
- SettingUtil.UpdateMusicVolume
- SettingUtil.UpdateVoiceVolume
- SettingUtil.UpdateSetting
- SettingUtil.UpdateScreenAdaptRatio
- SettingUtil.ResetScreenAdaptRatio
- SettingUtil.AccountCenter
- SettingUtil.ChangeAccount
- SettingUtil.CustomService
- SettingUtil.CloseAccount
**Snippet:**
```lua
local SettingUtil = {
  savedSetting = {}
}
local PlayerPrefs = CS.UnityEngine.PlayerPrefs

function SettingUtil.ParseSetting(setting)
  if string.len(setting) > 0 then
    SettingUtil.savedSetting = Json.decode(setting)
    local savedSetting = SettingUtil.savedSetting
    for k, v in pairs(savedSetting) do
```

---

## other/ShakeAnimPlay.lua.lua
**Functions:**
- ShakeAnimPlay.Init
- ShakeAnimPlay.CheckData
- ShakeAnimPlay.OnStart
- ShakeAnimPlay.OnPlaying
- ShakeAnimPlay.EndPlay
- ShakeAnimPlay.PlayShake
- ShakeAnimPlay.EnableShake
**Snippet:**
```lua
local ShakeAnimPlay = {}
local Animator = CS.UnityEngine.Animator
local data, callback
local time = 0

function ShakeAnimPlay.Init(...)
end

function ShakeAnimPlay.CheckData(...)
end
```

---

## other/Shape.lua.lua
**Functions:**
- Shape:__ctor
- Shape:updateNormals
- Shape:setAngle
- Shape:inAABB
**Snippet:**
```lua
local base = Body
local Shape = Create("Shape", base)

function Shape:__ctor()
  self.shapeType = nil
  self.aabbExtension = 0
  self.aabb = nil
  self._updatedCount = 0
end

```

---

## other/ShopClothesDetailsWindow.lua.lua
**Functions:**
- ShopClothesDetailsWindow.OnInit
- ShopClothesDetailsWindow.InitList
- uis.Main.ClothesList.TipsList.itemRenderer
- ShopClothesDetailsWindow.ShowAnimList
- ShopClothesDetailsWindow.ShowClothesInfo
- ShopClothesDetailsWindow.SetFashionName
- ShopClothesDetailsWindow.UpdateModel
- ShopClothesDetailsWindow.InitBtn
- ShopClothesDetailsWindow.CloseWindow
- ShopClothesDetailsWindow.BuyClothes
- ShopClothesDetailsWindow.HandleMessage
- ShopClothesDetailsWindow.OnClose
**Requires:**
- Shop_ClothesDetailsWindowByName
**Snippet:**
```lua
require("Shop_ClothesDetailsWindowByName")
local ShopClothesDetailsWindow = {}
local uis, contentPane, curId, fashionData, cardData, cost, jumpTb, data, productInfo, firstEnter, showType

function ShopClothesDetailsWindow.OnInit(bridgeObj)
  curId = bridgeObj.argTable[1]
  showType = bridgeObj.argTable[2]
  bridgeObj:SetViewAsync(WinResConfig.ShopClothesDetailsWindow.package, WinResConfig.ShopClothesDetailsWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
```

---

## other/ShopData.lua.lua
**Functions:**
- ShopData.ClearData
- ShopData.GetAgreementInfoById
- ShopData.InitNew
- ShopData.SaveNew
- ShopData.NewIsShow
- ShopData.SaveProductInfo
- ShopData.CheckAllProductInfoTime
- ShopData.UpdateOneProductInfo
- ShopData.GetShopGoodsInfoById
- ShopData.GetProductInfoById
- ShopData.SaveShopInfo
- ShopData.SaveGiftInfo
- ShopData.GetGiftInfoById
- ShopData.UpdateOneGift
**Snippet:**
```lua
ShopData = {
  shopInfo = {},
  productInfo = {},
  giftInfo = {},
  limitRecord = {},
  curShopType = nil,
  RecommendInfo = {},
  monthCardDay = {},
  agreementInfo = nil
}
```

---

## other/ShopGiftTipsWindow.lua.lua
**Functions:**
- ShopGiftTipsWindow.ReInitData
- ShopGiftTipsWindow.OnInit
- ShopGiftTipsWindow.CheckItemTime
- ShopGiftTipsWindow.UpdateInfo
- gift1.GiftWordContent.WordList.itemRenderer
- list.itemRenderer
- list.itemRenderer
- list.itemRenderer
- ShopGiftTipsWindow.BuyGift
- ShopGiftTipsWindow.BuyProduct
- ShopGiftTipsWindow.GetReward
- ShopGiftTipsWindow.GetDayReward
- ShopGiftTipsWindow.InitBtn
- ShopGiftTipsWindow.CloseWindow
- ShopGiftTipsWindow.OnClose
- ShopGiftTipsWindow.HandleMessage
**Requires:**
- Message_GiftTipsWindowByName
**Snippet:**
```lua
require("Message_GiftTipsWindowByName")
local ShopGiftTipsWindow = {}
local uis, contentPane, productData, giftData, productInfo

function ShopGiftTipsWindow.ReInitData()
end

function ShopGiftTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ShopGiftTipsWindow.package, WinResConfig.ShopGiftTipsWindow.comName, function(com)
    contentPane = com
```

---

## other/ShopMgr.lua.lua
**Functions:**
- ShopMgr.TokenIsBuy
- ShopMgr.ProductIsBuy
- ShopMgr.BuyProduct
- ShopMgr.CheckMonthCardDay
- ShopMgr.CanCardSkillUp
- ShopMgr.CanCardQualityUp
- ShopMgr.GetLookDetailsBtn
- ShopMgr.LoadSpineByLoader
- ShopMgr.PlayIdleAnimation
- ShopMgr.GetMonthCardDay
- ShopMgr.GetPayProductIdByType
- ShopMgr.GetOneGiftReward
**Snippet:**
```lua
ShopMgr = {}
USE_TYPE = {
  NONE = 0,
  BADGE = 1,
  SKILL_UP = 2,
  QUALITY_UP = 3,
  CARD = 4
}

function ShopMgr.TokenIsBuy(id)
```

---

## other/ShopMonthExplainWindow.lua.lua
**Functions:**
- ShopMonthExplainWindow.ReInitData
- ShopMonthExplainWindow.OnInit
- ShopMonthExplainWindow.UpdateInfo
- uis.Main.MonthExplain.WordList.itemRenderer
- ShopMonthExplainWindow.CloseWindow
- ShopMonthExplainWindow.InitBtn
- ShopMonthExplainWindow.OnClose
**Requires:**
- Shop_MonthExplainWindowByName
**Snippet:**
```lua
require("Shop_MonthExplainWindowByName")
local ShopMonthExplainWindow = {}
local uis, contentPane

function ShopMonthExplainWindow.ReInitData()
end

function ShopMonthExplainWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ShopMonthExplainWindow.package, WinResConfig.ShopMonthExplainWindow.comName, function(com)
    contentPane = com
```

---

## other/ShopScriptList.lua.lua
**Requires:**
- ShopData
- ShopService
- ShopMgr
**Snippet:**
```lua
local require = require
require("ShopData")
require("ShopService")
require("ShopMgr")
```

---

## other/ShopService.lua.lua
**Functions:**
- ShopService.Init
- ShopService.GetShopInfoReq
- ShopService.GetShopInfoRsp
- ShopService.BuyShopGoodsReq
- ShopService.BuyShopGoodsRsp
- ShopService.BuySealShopGoodsReq
- ShopService.BuySealShopGoodsRsp
- ShopService.CreatePayOrderReq
- ShopService.CreatePayOrderRsp
- ShopService.PurchaseBuyReq
- ShopService.PurchaseBuyRsp
- ShopService.CancelPayOrderReq
- ShopService.CancelPayOrderRsp
- ShopService.PurchaseGetReq
- ShopService.PurchaseGetRsp
- ShopService.GetPurchaseProductsReq
- ShopService.GetPurchaseProductsRsp
- ShopService.FashionBuyReq
- ShopService.FashionBuyRsp
- ShopService.GetAllRecommendImgReq
- ShopService.GetAllRecommendImgRsp
- ShopService.MonthCardDailyRewardReq
- ShopService.MonthCardDailyRewardRsp
- ShopService.GetGiftInfoReq
- ShopService.GetGiftInfoRsp
- ShopService.BuyGiftReq
- ShopService.BuyGiftRsp
- ShopService.GetGiftRewardReq
- ShopService.GetGiftRewardRsp
- ShopService.GetAgreementInfoReq
- ShopService.GetAgreementInfoRsp
- ShopService.RewardAgreementReq
- ShopService.RewardAgreementRsp
- ShopService.FetchWeekPayRewardReq
- ShopService.FetchWeekPayRewardRsp
**Snippet:**
```lua
ShopService = {}

function ShopService.Init()
  Net.AddListener(Proto.MsgName.GetShopInfoRsp, ShopService.GetShopInfoRsp)
  Net.AddListener(Proto.MsgName.BuyShopGoodsRsp, ShopService.BuyShopGoodsRsp)
  Net.AddListener(Proto.MsgName.BuySealShopGoodsRsp, ShopService.BuySealShopGoodsRsp)
  Net.AddListener(Proto.MsgName.PurchaseBuyRsp, ShopService.PurchaseBuyRsp)
  Net.AddListener(Proto.MsgName.PurchaseGetRsp, ShopService.PurchaseGetRsp)
  Net.AddListener(Proto.MsgName.GetPurchaseProductsRsp, ShopService.GetPurchaseProductsRsp)
  Net.AddListener(Proto.MsgName.FashionBuyRsp, ShopService.FashionBuyRsp)
```

---

## other/ShopTips_ExplainStar1ByName.lua.lua
**Functions:**
- GetShopTips_ExplainStar1Uis
**Snippet:**
```lua
function GetShopTips_ExplainStar1Uis(ui)
  local uis = {}
  
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.root = ui
  return uis
end
```

---

## other/ShopTips_ExplainStar2ByName.lua.lua
**Functions:**
- GetShopTips_ExplainStar2Uis
**Snippet:**
```lua
function GetShopTips_ExplainStar2Uis(ui)
  local uis = {}
  
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.root = ui
  return uis
end
```

---

## other/ShopTips_ExplainStar3ByName.lua.lua
**Functions:**
- GetShopTips_ExplainStar3Uis
**Snippet:**
```lua
function GetShopTips_ExplainStar3Uis(ui)
  local uis = {}
  
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.Number3Txt = ui:GetChild("Number3Txt")
  uis.root = ui
  return uis
end
```

---

## other/ShopTips_ExplainStar4ByName.lua.lua
**Functions:**
- GetShopTips_ExplainStar4Uis
**Snippet:**
```lua
function GetShopTips_ExplainStar4Uis(ui)
  local uis = {}
  
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.root = ui
  return uis
end
```

---

## other/ShopTips_ExplainStar5ByName.lua.lua
**Functions:**
- GetShopTips_ExplainStar5Uis
**Snippet:**
```lua
function GetShopTips_ExplainStar5Uis(ui)
  local uis = {}
  
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.root = ui
  return uis
end
```

---

## other/ShopTips_ExplainTitleByName.lua.lua
**Functions:**
- GetShopTips_ExplainTitleUis
**Snippet:**
```lua
function GetShopTips_ExplainTitleUis(ui)
  local uis = {}
  
  uis.Title1Txt = ui:GetChild("Title1Txt")
  uis.Title2Txt = ui:GetChild("Title2Txt")
  uis.Title3Txt = ui:GetChild("Title3Txt")
  uis.root = ui
  return uis
end
```

---

## other/ShopTips_ExplainWordByName.lua.lua
**Functions:**
- GetShopTips_ExplainWordUis
**Snippet:**
```lua
function GetShopTips_ExplainWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/ShopTips_TokenExplainByName.lua.lua
**Functions:**
- GetShopTips_TokenExplainUis
**Requires:**
- CommonResource_PopupBgByName
- Message_AssetsTipsGroupByName
- ShopTips_ExplainTitleByName
- ShopTips_ExplainStar1ByName
- ShopTips_ExplainStar2ByName
- ShopTips_ExplainStar3ByName
- ShopTips_ExplainStar4ByName
- ShopTips_ExplainStar5ByName
- ShopTips_ExplainWordByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Message_AssetsTipsGroupByName")
require("ShopTips_ExplainTitleByName")
require("ShopTips_ExplainStar1ByName")
require("ShopTips_ExplainStar2ByName")
require("ShopTips_ExplainStar3ByName")
require("ShopTips_ExplainStar4ByName")
require("ShopTips_ExplainStar5ByName")
require("ShopTips_ExplainWordByName")

```

---

## other/ShopTips_TokenExplainWindowByName.lua.lua
**Functions:**
- GetShopTips_TokenExplainWindowUis
**Requires:**
- ShopTips_TokenExplainByName
**Snippet:**
```lua
require("ShopTips_TokenExplainByName")

function GetShopTips_TokenExplainWindowUis(ui)
  local uis = {}
  uis.Main = GetShopTips_TokenExplainUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/ShopTokensTipsWindow.lua.lua
**Functions:**
- ShopTokensTipsWindow.ReInitData
- ShopTokensTipsWindow.OnInit
- ShopTokensTipsWindow.CheckItemTime
- ShopTokensTipsWindow.UpdateInfo
- ShopTokensTipsWindow.GetMessageBoxTips
- ShopTokensTipsWindow.InitToken
- info.WordList.itemRenderer
- info.WordList.itemRenderer
- ShopTokensTipsWindow.ShowDiscount
- ShopTokensTipsWindow.UpdateBuyNum
- ShopTokensTipsWindow.ShowStripBuy
- ShopTokensTipsWindow.GetGesture
- ShopTokensTipsWindow.ShowBuyBtn
- ShopTokensTipsWindow.OpenLookInfo
- info.HeadList.itemRenderer
- ShopTokensTipsWindow.ShowDetailsInfo
- info.DemandList.itemRenderer
- info.DemandList.itemRenderer
- info.PageList.itemRenderer
- ShopTokensTipsWindow.InitBtn
- ShopTokensTipsWindow.OnClose
**Requires:**
- Message_TokensTipsWindowByName
**Snippet:**
```lua
require("Message_TokensTipsWindowByName")
local ShopTokensTipsWindow = {}
local uis, contentPane, curId, priceId, priceNum, shopData, shopGridData, itemData, serviceData, itemArr, itemNum, buyNum, totalNum, maxValue, longSpeed, isActivity, activityData

function ShopTokensTipsWindow.ReInitData()
end

function ShopTokensTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ShopTokensTipsWindow.package, WinResConfig.ShopTokensTipsWindow.comName, function(com)
    contentPane = com
```

---

## other/ShopWindow.lua.lua
**Functions:**
- ShopWindow.OnInit
- ShopWindow.InitReaDot
- ShopWindow.SetAssetsTips
- ShopWindow.GetServerData
- ShopWindow.GetPlatform
- ShopWindow.UpdateTextDisplay
- ShopWindow.InitTab
- list.itemRenderer
- ShopWindow.InitToken
- ShopWindow.RefreshTokenShopList
- uis.Main.Collection.Token.TokenItem.TokenList.itemRenderer
- ShopWindow.CanRefresh
- ShopWindow.SortGoods
- ShopWindow.GetTokenData
- ShopWindow.InitRecharge
- uis.Main.Collection.Recharge.RechargeList.itemRenderer
- ShopWindow.GetRechargeData
- ShopWindow.CheckRecommendTime
- ShopWindow.DisposeRecommend
- ShopWindow.RemoveFirstGiftByRecommend
- ShopWindow.InitRecommend
- tabList.itemRenderer
- ShopWindow.LoadTemplateInfo
- ShopWindow.JumpAddMaskAnim
- ShopWindow.JumpBuy
- ShopWindow.Buy
- ShopWindow.UpdateMonthDay
- ShopWindow.LoadTexture
- ShopWindow.DisposeMap
- ShopWindow.InitClothes
- ShopWindow.RemovePastTime
- ShopWindow.RefreshClothesList
- uis.Main.Collection.Clothes.ClothesList.itemRenderer
- ShopWindow.GetGiftData
- ShopWindow.InitGift
- ShopWindow.ShowWeekShopInfo
- region.ItemList.itemRenderer
- ShopWindow.GetWeekShopData
- ShopWindow.ShowAgreementInfo
- ShopWindow.RefreshOneGift
- tabList.itemRenderer
- ShopWindow.InitAgreementTips
- ShopWindow.PlayInitGetEffect
- ShopWindow.PlayUnlockEffect
- ShopWindow.RefreshGiftShopList
- uis.Main.Collection.Gift.RechargeList.RechargeList.itemRenderer
- ShopWindow.GetGiftDataByType
- ShopWindow.GetClientGift
- ShopWindow.RefreshFirstGift
- list.itemRenderer
- ShopWindow.ShowAllItemFrame
- ShopWindow.ChallengeTableKey
- ShopWindow.GetLimitNum
- ShopWindow.ShowOneReward
- list.itemRenderer
- ShopWindow.TabOnClick
- ShopWindow.CheckProductInfoTime
- ShopWindow.InitBtn
- ShopWindow.UpdateAssetsTips
- ShopWindow.UpdateCheckTime
- ShopWindow.HandleMessage
- ShopWindow.OnShown
- ShopWindow.OnClose
**Requires:**
- Shop_ShopWindowByName
**Snippet:**
```lua
require("Shop_ShopWindowByName")
local ShopWindow = {}
local uis, contentPane, maxRefreshNum, recommendMap, teamGiftType, PLATFORM_TYPE, tabInit, MonthTime, jumpTb, notReopen
local tokenShopBar = {}
local firstTran, lastIndex
local oneGiftInterval = 0.05
local showAgreementEffect
local firstGiftId = 27000100
local JumpTargetType = {
  Gold = 1,
```

---

## other/Shop_AccumulatePassByName.lua.lua
**Functions:**
- GetShop_AccumulatePassUis
**Requires:**
- Shop_AccumulatePass_RewardRegion2ByName
- Shop_AccumulatePass_WordByName
**Snippet:**
```lua
require("Shop_AccumulatePass_RewardRegion2ByName")
require("Shop_AccumulatePass_WordByName")

function GetShop_AccumulatePassUis(ui)
  local uis = {}
  uis.RewardRegion2 = GetShop_AccumulatePass_RewardRegion2Uis(ui:GetChild("RewardRegion2"))
  uis.Word = GetShop_AccumulatePass_WordUis(ui:GetChild("Word"))
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## other/Shop_AccumulatePassRegionByName.lua.lua
**Functions:**
- GetShop_AccumulatePassRegionUis
**Requires:**
- Shop_AccumulatePassByName
**Snippet:**
```lua
require("Shop_AccumulatePassByName")

function GetShop_AccumulatePassRegionUis(ui)
  local uis = {}
  uis.AccumulatePass = GetShop_AccumulatePassUis(ui:GetChild("AccumulatePass"))
  uis.root = ui
  return uis
end
```

---

## other/Shop_AccumulatePass_GetBtnByName.lua.lua
**Functions:**
- GetShop_AccumulatePass_GetBtnUis
**Snippet:**
```lua
function GetShop_AccumulatePass_GetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Shop_AccumulatePass_RewardItemByName.lua.lua
**Functions:**
- GetShop_AccumulatePass_RewardItemUis
**Snippet:**
```lua
function GetShop_AccumulatePass_RewardItemUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Shop_AccumulatePass_RewardItemStateByName.lua.lua
**Functions:**
- GetShop_AccumulatePass_RewardItemStateUis
**Requires:**
- Shop_AccumulatePass_RewardItemByName
**Snippet:**
```lua
require("Shop_AccumulatePass_RewardItemByName")

function GetShop_AccumulatePass_RewardItemStateUis(ui)
  local uis = {}
  uis.ProgressTxt = ui:GetChild("ProgressTxt")
  uis.Item = GetShop_AccumulatePass_RewardItemUis(ui:GetChild("Item"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## other/Shop_AccumulatePass_RewardRegion1ByName.lua.lua
**Functions:**
- GetShop_AccumulatePass_RewardRegion1Uis
**Snippet:**
```lua
function GetShop_AccumulatePass_RewardRegion1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.WordNumberTxt = ui:GetChild("WordNumberTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.Number3Txt = ui:GetChild("Number3Txt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## other/Shop_AccumulatePass_RewardRegion2ByName.lua.lua
**Functions:**
- GetShop_AccumulatePass_RewardRegion2Uis
**Snippet:**
```lua
function GetShop_AccumulatePass_RewardRegion2Uis(ui)
  local uis = {}
  
  uis.WordNumberTxt = ui:GetChild("WordNumberTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## other/Shop_AccumulatePass_WordByName.lua.lua
**Functions:**
- GetShop_AccumulatePass_WordUis
**Snippet:**
```lua
function GetShop_AccumulatePass_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_AssetsTipsGroupByName.lua.lua
**Functions:**
- GetShop_AssetsTipsGroupUis
**Snippet:**
```lua
function GetShop_AssetsTipsGroupUis(ui)
  local uis = {}
  
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.root = ui
  return uis
end
```

---

## other/Shop_CardHeadBgByName.lua.lua
**Functions:**
- GetShop_CardHeadBgUis
**Snippet:**
```lua
function GetShop_CardHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## other/Shop_CardQBByName.lua.lua
**Functions:**
- GetShop_CardQBUis
**Snippet:**
```lua
function GetShop_CardQBUis(ui)
  local uis = {}
  
  uis.QBHolder = ui:GetChild("QBHolder")
  uis.root = ui
  return uis
end
```

---

## other/Shop_CardShowByName.lua.lua
**Functions:**
- GetShop_CardShowUis
**Snippet:**
```lua
function GetShop_CardShowUis(ui)
  local uis = {}
  
  uis.CardShowLoader = ui:GetChild("CardShowLoader")
  uis.CardShowHolder = ui:GetChild("CardShowHolder")
  uis.root = ui
  return uis
end
```

---

## other/Shop_Clothes1NameByName.lua.lua
**Functions:**
- GetShop_Clothes1NameUis
**Snippet:**
```lua
function GetShop_Clothes1NameUis(ui)
  local uis = {}
  
  uis.CardNameTxt = ui:GetChild("CardNameTxt")
  uis.CardNameENTxt = ui:GetChild("CardNameENTxt")
  uis.ClothesNameTxt = ui:GetChild("ClothesNameTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Shop_ClothesByName.lua.lua
**Functions:**
- GetShop_ClothesUis
**Requires:**
- Shop_LeftTabByName
**Snippet:**
```lua
require("Shop_LeftTabByName")

function GetShop_ClothesUis(ui)
  local uis = {}
  uis.ClothesList = ui:GetChild("ClothesList")
  uis.LeftTab = GetShop_LeftTabUis(ui:GetChild("LeftTab"))
  uis.root = ui
  return uis
end
```

---

## other/Shop_ClothesCardInfoByName.lua.lua
**Functions:**
- GetShop_ClothesCardInfoUis
**Snippet:**
```lua
function GetShop_ClothesCardInfoUis(ui)
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

## other/Shop_ClothesCashPriceNumberByName.lua.lua
**Functions:**
- GetShop_ClothesCashPriceNumberUis
**Snippet:**
```lua
function GetShop_ClothesCashPriceNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_ClothesDetailsByName.lua.lua
**Functions:**
- GetShop_ClothesDetailsUis
**Requires:**
- CommonResource_BackGroundByName
- Shop_CardShowByName
- Shop_CardQBByName
- Shop_ClothesCardInfoByName
- Shop_ClothesListByName
- Shop_AssetsTipsGroupByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Shop_CardShowByName")
require("Shop_CardQBByName")
require("Shop_ClothesCardInfoByName")
require("Shop_ClothesListByName")
require("Shop_AssetsTipsGroupByName")
require("CommonResource_CurrencyReturnByName")

function GetShop_ClothesDetailsUis(ui)
  local uis = {}
```

---

## other/Shop_ClothesDetailsWindowByName.lua.lua
**Functions:**
- GetShop_ClothesDetailsWindowUis
**Requires:**
- Shop_ClothesDetailsByName
**Snippet:**
```lua
require("Shop_ClothesDetailsByName")

function GetShop_ClothesDetailsWindowUis(ui)
  local uis = {}
  uis.Main = GetShop_ClothesDetailsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/Shop_ClothesListByName.lua.lua
**Functions:**
- GetShop_ClothesListUis
**Requires:**
- Shop_ClothesNameByName
- Shop_WearingByName
- Shop_ClothesPriceByName
- Shop_NotHaveCardByName
**Snippet:**
```lua
require("Shop_ClothesNameByName")
require("Shop_WearingByName")
require("Shop_ClothesPriceByName")
require("Shop_NotHaveCardByName")

function GetShop_ClothesListUis(ui)
  local uis = {}
  uis.ClothesName = GetShop_ClothesNameUis(ui:GetChild("ClothesName"))
  uis.Wearing = GetShop_WearingUis(ui:GetChild("Wearing"))
  uis.ClothesPrice = GetShop_ClothesPriceUis(ui:GetChild("ClothesPrice"))
```

---

## other/Shop_ClothesNameByName.lua.lua
**Functions:**
- GetShop_ClothesNameUis
**Snippet:**
```lua
function GetShop_ClothesNameUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_ClothesPriceByName.lua.lua
**Functions:**
- GetShop_ClothesPriceUis
**Requires:**
- Shop_ClothesPriceNumberByName
- Shop_ClothesCashPriceNumberByName
**Snippet:**
```lua
require("Shop_ClothesPriceNumberByName")
require("Shop_ClothesCashPriceNumberByName")

function GetShop_ClothesPriceUis(ui)
  local uis = {}
  uis.Price = GetShop_ClothesPriceNumberUis(ui:GetChild("Price"))
  uis.CashPrice = GetShop_ClothesCashPriceNumberUis(ui:GetChild("CashPrice"))
  uis.SureBtn = ui:GetChild("SureBtn")
  uis.priceCtr = ui:GetController("price")
  uis.root = ui
```

---

## other/Shop_ClothesPriceNumberByName.lua.lua
**Functions:**
- GetShop_ClothesPriceNumberUis
**Snippet:**
```lua
function GetShop_ClothesPriceNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_ClothesShowByName.lua.lua
**Functions:**
- GetShop_ClothesShowUis
**Snippet:**
```lua
function GetShop_ClothesShowUis(ui)
  local uis = {}
  
  uis.ClothesShowLoader = ui:GetChild("ClothesShowLoader")
  uis.ClothesShowHolder = ui:GetChild("ClothesShowHolder")
  uis.root = ui
  return uis
end
```

---

## other/Shop_ClothesTimeByName.lua.lua
**Functions:**
- GetShop_ClothesTimeUis
**Snippet:**
```lua
function GetShop_ClothesTimeUis(ui)
  local uis = {}
  
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_ClothesTips1BtnByName.lua.lua
**Functions:**
- GetShop_ClothesTips1BtnUis
**Snippet:**
```lua
function GetShop_ClothesTips1BtnUis(ui)
  local uis = {}
  
  uis.ClothesShowLoader = ui:GetChild("ClothesShowLoader")
  uis.ClothesShowHolder = ui:GetChild("ClothesShowHolder")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c4Ctr = ui:GetController("c4")
  uis.c3Ctr = ui:GetController("c3")
```

---

## other/Shop_ClothesTipsBtnByName.lua.lua
**Functions:**
- GetShop_ClothesTipsBtnUis
**Requires:**
- Shop_ClothesShowByName
- Shop_Clothes1NameByName
- Shop_ClothesTimeByName
- Shop_ColthesPriceByName
- Shop_NewByName
**Snippet:**
```lua
require("Shop_ClothesShowByName")
require("Shop_Clothes1NameByName")
require("Shop_ClothesTimeByName")
require("Shop_ColthesPriceByName")
require("Shop_NewByName")

function GetShop_ClothesTipsBtnUis(ui)
  local uis = {}
  uis.ClothesShow = GetShop_ClothesShowUis(ui:GetChild("ClothesShow"))
  uis.ClothesName = GetShop_Clothes1NameUis(ui:GetChild("ClothesName"))
```

---

## other/Shop_ClothesTipsByName.lua.lua
**Functions:**
- GetShop_ClothesTipsUis
**Snippet:**
```lua
function GetShop_ClothesTipsUis(ui)
  local uis = {}
  
  uis.ClothesTipsBtn = ui:GetChild("ClothesTipsBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Shop_CollectionByName.lua.lua
**Functions:**
- GetShop_CollectionUis
**Requires:**
- Shop_RecommendByName
- Shop_RechargeByName
- Shop_GiftByName
- Shop_ClothesByName
- Shop_TokenByName
- Shop_AssetsTipsGroupByName
**Snippet:**
```lua
require("Shop_RecommendByName")
require("Shop_RechargeByName")
require("Shop_GiftByName")
require("Shop_ClothesByName")
require("Shop_TokenByName")
require("Shop_AssetsTipsGroupByName")

function GetShop_CollectionUis(ui)
  local uis = {}
  uis.Recommend = GetShop_RecommendUis(ui:GetChild("Recommend"))
```

---

## other/Shop_ColthesPriceByName.lua.lua
**Functions:**
- GetShop_ColthesPriceUis
**Snippet:**
```lua
function GetShop_ColthesPriceUis(ui)
  local uis = {}
  
  uis.PriceLoader = ui:GetChild("PriceLoader")
  uis.PriceTxt = ui:GetChild("PriceTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Shop_Day1ByName.lua.lua
**Functions:**
- GetShop_Day1Uis
**Snippet:**
```lua
function GetShop_Day1Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Shop_Day2ByName.lua.lua
**Functions:**
- GetShop_Day2Uis
**Snippet:**
```lua
function GetShop_Day2Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Shop_Day3ByName.lua.lua
**Functions:**
- GetShop_Day3Uis
**Snippet:**
```lua
function GetShop_Day3Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Shop_DiscountByName.lua.lua
**Functions:**
- GetShop_DiscountUis
**Snippet:**
```lua
function GetShop_DiscountUis(ui)
  local uis = {}
  
  uis.DiscountTxt = ui:GetChild("DiscountTxt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_DoubleByName.lua.lua
**Functions:**
- GetShop_DoubleUis
**Snippet:**
```lua
function GetShop_DoubleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_ExplainBtnByName.lua.lua
**Functions:**
- GetShop_ExplainBtnUis
**Snippet:**
```lua
function GetShop_ExplainBtnUis(ui)
  local uis = {}
  
  uis.SpendTxt = ui:GetChild("SpendTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Shop_ExplainStar1ByName.lua.lua
**Functions:**
- GetShop_ExplainStar1Uis
**Snippet:**
```lua
function GetShop_ExplainStar1Uis(ui)
  local uis = {}
  
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_ExplainStar2ByName.lua.lua
**Functions:**
- GetShop_ExplainStar2Uis
**Snippet:**
```lua
function GetShop_ExplainStar2Uis(ui)
  local uis = {}
  
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_ExplainStar3ByName.lua.lua
**Functions:**
- GetShop_ExplainStar3Uis
**Snippet:**
```lua
function GetShop_ExplainStar3Uis(ui)
  local uis = {}
  
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_ExplainStar4ByName.lua.lua
**Functions:**
- GetShop_ExplainStar4Uis
**Snippet:**
```lua
function GetShop_ExplainStar4Uis(ui)
  local uis = {}
  
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_ExplainStar5ByName.lua.lua
**Functions:**
- GetShop_ExplainStar5Uis
**Snippet:**
```lua
function GetShop_ExplainStar5Uis(ui)
  local uis = {}
  
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_ExplainTitleByName.lua.lua
**Functions:**
- GetShop_ExplainTitleUis
**Snippet:**
```lua
function GetShop_ExplainTitleUis(ui)
  local uis = {}
  
  uis.Title1Txt = ui:GetChild("Title1Txt")
  uis.Title2Txt = ui:GetChild("Title2Txt")
  uis.Title3Txt = ui:GetChild("Title3Txt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_ExplainWordByName.lua.lua
**Functions:**
- GetShop_ExplainWordUis
**Snippet:**
```lua
function GetShop_ExplainWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_FirstRechargeAllFrameByName.lua.lua
**Functions:**
- GetShop_FirstRechargeAllFrameUis
**Requires:**
- Shop_FirstRechargeItemFrameByName
- Shop_FirstRechargeCardFrameByName
**Snippet:**
```lua
require("Shop_FirstRechargeItemFrameByName")
require("Shop_FirstRechargeCardFrameByName")

function GetShop_FirstRechargeAllFrameUis(ui)
  local uis = {}
  uis.ItemFrame = GetShop_FirstRechargeItemFrameUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetShop_FirstRechargeCardFrameUis(ui:GetChild("CardFrame"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## other/Shop_FirstRechargeByName.lua.lua
**Functions:**
- GetShop_FirstRechargeUis
**Requires:**
- Shop_Day1ByName
- Shop_Day2ByName
- Shop_Day3ByName
- Shop_FirstRechargeCompleteByName
**Snippet:**
```lua
require("Shop_Day1ByName")
require("Shop_Day2ByName")
require("Shop_Day3ByName")
require("Shop_FirstRechargeCompleteByName")

function GetShop_FirstRechargeUis(ui)
  local uis = {}
  uis.Day1 = GetShop_Day1Uis(ui:GetChild("Day1"))
  uis.Day2 = GetShop_Day2Uis(ui:GetChild("Day2"))
  uis.Day3 = GetShop_Day3Uis(ui:GetChild("Day3"))
```

---

## other/Shop_FirstRechargeCardFrameByName.lua.lua
**Functions:**
- GetShop_FirstRechargeCardFrameUis
**Requires:**
- Shop_FirstRechargeItemCardPicByName
**Snippet:**
```lua
require("Shop_FirstRechargeItemCardPicByName")

function GetShop_FirstRechargeCardFrameUis(ui)
  local uis = {}
  uis.ItemCardPic = GetShop_FirstRechargeItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## other/Shop_FirstRechargeCompleteByName.lua.lua
**Functions:**
- GetShop_FirstRechargeCompleteUis
**Snippet:**
```lua
function GetShop_FirstRechargeCompleteUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_FirstRechargeGetBtnByName.lua.lua
**Functions:**
- GetShop_FirstRechargeGetBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetShop_FirstRechargeGetBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Shop_FirstRechargeGoBtnByName.lua.lua
**Functions:**
- GetShop_FirstRechargeGoBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetShop_FirstRechargeGoBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Shop_FirstRechargeItemCardPicByName.lua.lua
**Functions:**
- GetShop_FirstRechargeItemCardPicUis
**Snippet:**
```lua
function GetShop_FirstRechargeItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## other/Shop_FirstRechargeItemFrameByName.lua.lua
**Functions:**
- GetShop_FirstRechargeItemFrameUis
**Snippet:**
```lua
function GetShop_FirstRechargeItemFrameUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## other/Shop_FirstRechargeRegionByName.lua.lua
**Functions:**
- GetShop_FirstRechargeRegionUis
**Requires:**
- Shop_FirstRechargeByName
**Snippet:**
```lua
require("Shop_FirstRechargeByName")

function GetShop_FirstRechargeRegionUis(ui)
  local uis = {}
  uis.FirstRecharge = GetShop_FirstRechargeUis(ui:GetChild("FirstRecharge"))
  uis.root = ui
  return uis
end
```

---

## other/Shop_GetNumberByName.lua.lua
**Functions:**
- GetShop_GetNumberUis
**Snippet:**
```lua
function GetShop_GetNumberUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_GiftBuyPriceByName.lua.lua
**Functions:**
- GetShop_GiftBuyPriceUis
**Snippet:**
```lua
function GetShop_GiftBuyPriceUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_GiftByName.lua.lua
**Functions:**
- GetShop_GiftUis
**Requires:**
- Shop_GiftRechargeListByName
- Shop_FirstRechargeRegionByName
- Shop_PactCollectionByName
- Shop_AccumulatePassRegionByName
- Shop_LeftTabByName
**Snippet:**
```lua
require("Shop_GiftRechargeListByName")
require("Shop_FirstRechargeRegionByName")
require("Shop_PactCollectionByName")
require("Shop_AccumulatePassRegionByName")
require("Shop_LeftTabByName")

function GetShop_GiftUis(ui)
  local uis = {}
  uis.RechargeList = GetShop_GiftRechargeListUis(ui:GetChild("RechargeList"))
  uis.FirstRechargeRegion = GetShop_FirstRechargeRegionUis(ui:GetChild("FirstRechargeRegion"))
```

---

## other/Shop_GiftRechargeListByName.lua.lua
**Functions:**
- GetShop_GiftRechargeListUis
**Snippet:**
```lua
function GetShop_GiftRechargeListUis(ui)
  local uis = {}
  
  uis.RechargeList = ui:GetChild("RechargeList")
  uis.root = ui
  return uis
end
```

---

## other/Shop_GiftTipsBgByName.lua.lua
**Functions:**
- GetShop_GiftTipsBgUis
**Snippet:**
```lua
function GetShop_GiftTipsBgUis(ui)
  local uis = {}
  
  uis.PicHolder = ui:GetChild("PicHolder")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## other/Shop_GiftTipsBtnByName.lua.lua
**Functions:**
- GetShop_GiftTipsBtnUis
**Requires:**
- Shop_GiftTipsBgByName
- Shop_GiftWordTipsByName
- Shop_GiftTipsMoveWordByName
- Shop_MonthTimeByName
- Shop_GiftBuyPriceByName
- Shop_GiftTipsSaleByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("Shop_GiftTipsBgByName")
require("Shop_GiftWordTipsByName")
require("Shop_GiftTipsMoveWordByName")
require("Shop_MonthTimeByName")
require("Shop_GiftBuyPriceByName")
require("Shop_GiftTipsSaleByName")
require("CommonResource_RedDotByName")

function GetShop_GiftTipsBtnUis(ui)
  local uis = {}
```

---

## other/Shop_GiftTipsByName.lua.lua
**Functions:**
- GetShop_GiftTipsUis
**Requires:**
- Shop_SellOutByName
**Snippet:**
```lua
require("Shop_SellOutByName")

function GetShop_GiftTipsUis(ui)
  local uis = {}
  uis.GiftTipsBtn = ui:GetChild("GiftTipsBtn")
  uis.SellOut = GetShop_SellOutUis(ui:GetChild("SellOut"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Shop_GiftTipsMoveWordByName.lua.lua
**Functions:**
- GetShop_GiftTipsMoveWordUis
**Snippet:**
```lua
function GetShop_GiftTipsMoveWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_GiftTipsSaleByName.lua.lua
**Functions:**
- GetShop_GiftTipsSaleUis
**Snippet:**
```lua
function GetShop_GiftTipsSaleUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## other/Shop_GiftWordTipsByName.lua.lua
**Functions:**
- GetShop_GiftWordTipsUis
**Snippet:**
```lua
function GetShop_GiftWordTipsUis(ui)
  local uis = {}
  
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_GiveNumberByName.lua.lua
**Functions:**
- GetShop_GiveNumberUis
**Snippet:**
```lua
function GetShop_GiveNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_JapBtnByName.lua.lua
**Functions:**
- GetShop_JapBtnUis
**Snippet:**
```lua
function GetShop_JapBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Shop_LeftBtnByName.lua.lua
**Functions:**
- GetShop_LeftBtnUis
**Requires:**
- Shop_LeftTabTimeByName
- CommonResource_RedDotByName
- Shop_NewByName
**Snippet:**
```lua
require("Shop_LeftTabTimeByName")
require("CommonResource_RedDotByName")
require("Shop_NewByName")

function GetShop_LeftBtnUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.Time = GetShop_LeftTabTimeUis(ui:GetChild("Time"))
```

---

## other/Shop_LeftTabByName.lua.lua
**Functions:**
- GetShop_LeftTabUis
**Snippet:**
```lua
function GetShop_LeftTabUis(ui)
  local uis = {}
  
  uis.LeftTabList = ui:GetChild("LeftTabList")
  uis.root = ui
  return uis
end
```

---

## other/Shop_LeftTabTimeByName.lua.lua
**Functions:**
- GetShop_LeftTabTimeUis
**Snippet:**
```lua
function GetShop_LeftTabTimeUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_MonthBuyBtnByName.lua.lua
**Functions:**
- GetShop_MonthBuyBtnUis
**Requires:**
- Shop_MonthTimeByName
**Snippet:**
```lua
require("Shop_MonthTimeByName")

function GetShop_MonthBuyBtnUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.PicHolder = ui:GetChild("PicHolder")
  uis.MonthTime = GetShop_MonthTimeUis(ui:GetChild("MonthTime"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## other/Shop_MonthByName.lua.lua
**Functions:**
- GetShop_MonthUis
**Snippet:**
```lua
function GetShop_MonthUis(ui)
  local uis = {}
  
  uis.MonthBuyBtn = ui:GetChild("MonthBuyBtn")
  uis.MonthExplainBtn = ui:GetChild("MonthExplainBtn")
  uis.root = ui
  return uis
end
```

---

## other/Shop_MonthExplain1ByName.lua.lua
**Functions:**
- GetShop_MonthExplain1Uis
**Snippet:**
```lua
function GetShop_MonthExplain1Uis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.WordList = ui:GetChild("WordList")
  uis.root = ui
  return uis
end
```

---

## other/Shop_MonthExplain2ByName.lua.lua
**Functions:**
- GetShop_MonthExplain2Uis
**Requires:**
- CommonResource_PopupBgByName
- Shop_MonthExplain1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Shop_MonthExplain1ByName")

function GetShop_MonthExplain2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.MonthExplain = GetShop_MonthExplain1Uis(ui:GetChild("MonthExplain"))
  uis.root = ui
  return uis
```

---

## other/Shop_MonthExplainBtnByName.lua.lua
**Functions:**
- GetShop_MonthExplainBtnUis
**Snippet:**
```lua
function GetShop_MonthExplainBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Shop_MonthExplainCloseBtnByName.lua.lua
**Functions:**
- GetShop_MonthExplainCloseBtnUis
**Snippet:**
```lua
function GetShop_MonthExplainCloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Shop_MonthExplainWindowByName.lua.lua
**Functions:**
- GetShop_MonthExplainWindowUis
**Requires:**
- Shop_MonthExplain2ByName
**Snippet:**
```lua
require("Shop_MonthExplain2ByName")

function GetShop_MonthExplainWindowUis(ui)
  local uis = {}
  uis.Main = GetShop_MonthExplain2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/Shop_MonthExplainWordByName.lua.lua
**Functions:**
- GetShop_MonthExplainWordUis
**Snippet:**
```lua
function GetShop_MonthExplainWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_MonthStateByName.lua.lua
**Functions:**
- GetShop_MonthStateUis
**Snippet:**
```lua
function GetShop_MonthStateUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## other/Shop_MonthTimeByName.lua.lua
**Functions:**
- GetShop_MonthTimeUis
**Snippet:**
```lua
function GetShop_MonthTimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.GetWordTxt = ui:GetChild("GetWordTxt")
  uis.NoneTxt = ui:GetChild("NoneTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## other/Shop_NewByName.lua.lua
**Functions:**
- GetShop_NewUis
**Snippet:**
```lua
function GetShop_NewUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## other/Shop_NotHaveCardByName.lua.lua
**Functions:**
- GetShop_NotHaveCardUis
**Snippet:**
```lua
function GetShop_NotHaveCardUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_OneYuanPassByName.lua.lua
**Functions:**
- GetShop_OneYuanPassUis
**Requires:**
- Shop_OneYuanPass_ActivationByName
- Shop_OneYuanPass_WordByName
- Shop_OneYuanPass_ItemRegion1ByName
- Shop_OneYuanPass_ItemRegion2ByName
**Snippet:**
```lua
require("Shop_OneYuanPass_ActivationByName")
require("Shop_OneYuanPass_WordByName")
require("Shop_OneYuanPass_ItemRegion1ByName")
require("Shop_OneYuanPass_ItemRegion2ByName")

function GetShop_OneYuanPassUis(ui)
  local uis = {}
  uis.Activation = GetShop_OneYuanPass_ActivationUis(ui:GetChild("Activation"))
  uis.Word = GetShop_OneYuanPass_WordUis(ui:GetChild("Word"))
  uis.GetBtn = ui:GetChild("GetBtn")
```

---

## other/Shop_OneYuanPassRegionByName.lua.lua
**Functions:**
- GetShop_OneYuanPassRegionUis
**Requires:**
- Shop_OneYuanPassByName
**Snippet:**
```lua
require("Shop_OneYuanPassByName")

function GetShop_OneYuanPassRegionUis(ui)
  local uis = {}
  uis.OneYuanPass = GetShop_OneYuanPassUis(ui:GetChild("OneYuanPass"))
  uis.root = ui
  return uis
end
```

---

## other/Shop_OneYuanPassTipsByName.lua.lua
**Functions:**
- GetShop_OneYuanPassTipsUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetShop_OneYuanPassTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.root = ui
  return uis
```

---

## other/Shop_OneYuanPassTipsWindowByName.lua.lua
**Functions:**
- GetShop_OneYuanPassTipsWindowUis
**Requires:**
- Shop_OneYuanPassTipsByName
**Snippet:**
```lua
require("Shop_OneYuanPassTipsByName")

function GetShop_OneYuanPassTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetShop_OneYuanPassTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/Shop_OneYuanPass_ActivationByName.lua.lua
**Functions:**
- GetShop_OneYuanPass_ActivationUis
**Snippet:**
```lua
function GetShop_OneYuanPass_ActivationUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_OneYuanPass_AllFrameByName.lua.lua
**Functions:**
- GetShop_OneYuanPass_AllFrameUis
**Requires:**
- Shop_OneYuanPass_ItemFrameByName
- Shop_OneYuanPass_CardFrameByName
**Snippet:**
```lua
require("Shop_OneYuanPass_ItemFrameByName")
require("Shop_OneYuanPass_CardFrameByName")

function GetShop_OneYuanPass_AllFrameUis(ui)
  local uis = {}
  uis.ItemFrame = GetShop_OneYuanPass_ItemFrameUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetShop_OneYuanPass_CardFrameUis(ui:GetChild("CardFrame"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.c1Ctr = ui:GetController("c1")
```

---

## other/Shop_OneYuanPass_BuyBtnByName.lua.lua
**Functions:**
- GetShop_OneYuanPass_BuyBtnUis
**Snippet:**
```lua
function GetShop_OneYuanPass_BuyBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Shop_OneYuanPass_CardFrameByName.lua.lua
**Functions:**
- GetShop_OneYuanPass_CardFrameUis
**Requires:**
- Shop_OneYuanPass_ItemCardPicByName
**Snippet:**
```lua
require("Shop_OneYuanPass_ItemCardPicByName")

function GetShop_OneYuanPass_CardFrameUis(ui)
  local uis = {}
  uis.ItemCardPic = GetShop_OneYuanPass_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## other/Shop_OneYuanPass_GetBtnByName.lua.lua
**Functions:**
- GetShop_OneYuanPass_GetBtnUis
**Snippet:**
```lua
function GetShop_OneYuanPass_GetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Shop_OneYuanPass_ItemCardPicByName.lua.lua
**Functions:**
- GetShop_OneYuanPass_ItemCardPicUis
**Snippet:**
```lua
function GetShop_OneYuanPass_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## other/Shop_OneYuanPass_ItemFrameByName.lua.lua
**Functions:**
- GetShop_OneYuanPass_ItemFrameUis
**Snippet:**
```lua
function GetShop_OneYuanPass_ItemFrameUis(ui)
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

## other/Shop_OneYuanPass_ItemRegion1ByName.lua.lua
**Functions:**
- GetShop_OneYuanPass_ItemRegion1Uis
**Requires:**
- Shop_OneYuanPass_AllFrameByName
**Snippet:**
```lua
require("Shop_OneYuanPass_AllFrameByName")

function GetShop_OneYuanPass_ItemRegion1Uis(ui)
  local uis = {}
  uis.Top = GetShop_OneYuanPass_AllFrameUis(ui:GetChild("Top"))
  uis.Below = GetShop_OneYuanPass_AllFrameUis(ui:GetChild("Below"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## other/Shop_OneYuanPass_ItemRegion2ByName.lua.lua
**Functions:**
- GetShop_OneYuanPass_ItemRegion2Uis
**Requires:**
- Shop_OneYuanPass_AllFrameByName
**Snippet:**
```lua
require("Shop_OneYuanPass_AllFrameByName")

function GetShop_OneYuanPass_ItemRegion2Uis(ui)
  local uis = {}
  uis.Top = GetShop_OneYuanPass_AllFrameUis(ui:GetChild("Top"))
  uis.Below = GetShop_OneYuanPass_AllFrameUis(ui:GetChild("Below"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## other/Shop_OneYuanPass_WordByName.lua.lua
**Functions:**
- GetShop_OneYuanPass_WordUis
**Snippet:**
```lua
function GetShop_OneYuanPass_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_OriginalPriceByName.lua.lua
**Functions:**
- GetShop_OriginalPriceUis
**Snippet:**
```lua
function GetShop_OriginalPriceUis(ui)
  local uis = {}
  
  uis.OriginalPriceTxt = ui:GetChild("OriginalPriceTxt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_PactCollectionByName.lua.lua
**Functions:**
- GetShop_PactCollectionUis
**Requires:**
- Shop_OneYuanPassRegionByName
- Shop_PactPassRegionByName
**Snippet:**
```lua
require("Shop_OneYuanPassRegionByName")
require("Shop_PactPassRegionByName")

function GetShop_PactCollectionUis(ui)
  local uis = {}
  uis.OneYuanPass = GetShop_OneYuanPassRegionUis(ui:GetChild("OneYuanPass"))
  uis.PactPass = GetShop_PactPassRegionUis(ui:GetChild("PactPass"))
  uis.TabList = ui:GetChild("TabList")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## other/Shop_PactPassBuyBtnByName.lua.lua
**Functions:**
- GetShop_PactPassBuyBtnUis
**Snippet:**
```lua
function GetShop_PactPassBuyBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Shop_PactPassByName.lua.lua
**Functions:**
- GetShop_PactPassUis
**Requires:**
- Shop_PactPass_ActivationByName
- Shop_PactPass_WordByName
- Shop_PactPass_ItemRegion1ByName
- Shop_PactPass_ItemRegion2ByName
**Snippet:**
```lua
require("Shop_PactPass_ActivationByName")
require("Shop_PactPass_WordByName")
require("Shop_PactPass_ItemRegion1ByName")
require("Shop_PactPass_ItemRegion2ByName")

function GetShop_PactPassUis(ui)
  local uis = {}
  uis.Activation = GetShop_PactPass_ActivationUis(ui:GetChild("Activation"))
  uis.Word = GetShop_PactPass_WordUis(ui:GetChild("Word"))
  uis.GetBtn = ui:GetChild("GetBtn")
```

---

## other/Shop_PactPassRegionByName.lua.lua
**Functions:**
- GetShop_PactPassRegionUis
**Requires:**
- Shop_PactPassByName
**Snippet:**
```lua
require("Shop_PactPassByName")

function GetShop_PactPassRegionUis(ui)
  local uis = {}
  uis.PactPass = GetShop_PactPassUis(ui:GetChild("PactPass"))
  uis.root = ui
  return uis
end
```

---

## other/Shop_PactPassTipsByName.lua.lua
**Functions:**
- GetShop_PactPassTipsUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetShop_PactPassTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.root = ui
  return uis
```

---

## other/Shop_PactPassTipsWindowByName.lua.lua
**Functions:**
- GetShop_PactPassTipsWindowUis
**Requires:**
- Shop_PactPassTipsByName
**Snippet:**
```lua
require("Shop_PactPassTipsByName")

function GetShop_PactPassTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetShop_PactPassTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/Shop_PactPass_ActivationByName.lua.lua
**Functions:**
- GetShop_PactPass_ActivationUis
**Snippet:**
```lua
function GetShop_PactPass_ActivationUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_PactPass_AllFrameByName.lua.lua
**Functions:**
- GetShop_PactPass_AllFrameUis
**Requires:**
- Shop_PactPass_ItemFrameByName
- Shop_PactPass_CardFrameByName
**Snippet:**
```lua
require("Shop_PactPass_ItemFrameByName")
require("Shop_PactPass_CardFrameByName")

function GetShop_PactPass_AllFrameUis(ui)
  local uis = {}
  uis.ItemFrame = GetShop_PactPass_ItemFrameUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetShop_PactPass_CardFrameUis(ui:GetChild("CardFrame"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.c1Ctr = ui:GetController("c1")
```

---

## other/Shop_PactPass_CardFrameByName.lua.lua
**Functions:**
- GetShop_PactPass_CardFrameUis
**Requires:**
- Shop_PactPass_ItemCardPicByName
**Snippet:**
```lua
require("Shop_PactPass_ItemCardPicByName")

function GetShop_PactPass_CardFrameUis(ui)
  local uis = {}
  uis.ItemCardPic = GetShop_PactPass_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## other/Shop_PactPass_GetBtnByName.lua.lua
**Functions:**
- GetShop_PactPass_GetBtnUis
**Snippet:**
```lua
function GetShop_PactPass_GetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Shop_PactPass_ItemCardPicByName.lua.lua
**Functions:**
- GetShop_PactPass_ItemCardPicUis
**Snippet:**
```lua
function GetShop_PactPass_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## other/Shop_PactPass_ItemFrameByName.lua.lua
**Functions:**
- GetShop_PactPass_ItemFrameUis
**Snippet:**
```lua
function GetShop_PactPass_ItemFrameUis(ui)
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

## other/Shop_PactPass_ItemRegion1ByName.lua.lua
**Functions:**
- GetShop_PactPass_ItemRegion1Uis
**Requires:**
- Shop_PactPass_AllFrameByName
**Snippet:**
```lua
require("Shop_PactPass_AllFrameByName")

function GetShop_PactPass_ItemRegion1Uis(ui)
  local uis = {}
  uis.Top = GetShop_PactPass_AllFrameUis(ui:GetChild("Top"))
  uis.Below = GetShop_PactPass_AllFrameUis(ui:GetChild("Below"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## other/Shop_PactPass_ItemRegion2ByName.lua.lua
**Functions:**
- GetShop_PactPass_ItemRegion2Uis
**Requires:**
- Shop_PactPass_AllFrameByName
**Snippet:**
```lua
require("Shop_PactPass_AllFrameByName")

function GetShop_PactPass_ItemRegion2Uis(ui)
  local uis = {}
  uis.Top = GetShop_PactPass_AllFrameUis(ui:GetChild("Top"))
  uis.Below = GetShop_PactPass_AllFrameUis(ui:GetChild("Below"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## other/Shop_PactPass_WordByName.lua.lua
**Functions:**
- GetShop_PactPass_WordUis
**Snippet:**
```lua
function GetShop_PactPass_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_Pact_TabBtnByName.lua.lua
**Functions:**
- GetShop_Pact_TabBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetShop_Pact_TabBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Shop_RechargeByName.lua.lua
**Functions:**
- GetShop_RechargeUis
**Snippet:**
```lua
function GetShop_RechargeUis(ui)
  local uis = {}
  
  uis.RechargeList = ui:GetChild("RechargeList")
  uis.Jap1Btn = ui:GetChild("Jap1Btn")
  uis.Jap2Btn = ui:GetChild("Jap2Btn")
  uis.root = ui
  return uis
end
```

---

## other/Shop_RechargeTipsBtnByName.lua.lua
**Functions:**
- GetShop_RechargeTipsBtnUis
**Requires:**
- Shop_GetNumberByName
- Shop_GiveNumberByName
- Shop_DoubleByName
**Snippet:**
```lua
require("Shop_GetNumberByName")
require("Shop_GiveNumberByName")
require("Shop_DoubleByName")

function GetShop_RechargeTipsBtnUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.GetNumber = GetShop_GetNumberUis(ui:GetChild("GetNumber"))
  uis.GiveNumber = GetShop_GiveNumberUis(ui:GetChild("GiveNumber"))
```

---

## other/Shop_RecommendByName.lua.lua
**Functions:**
- GetShop_RecommendUis
**Requires:**
- Shop_LeftTabByName
**Snippet:**
```lua
require("Shop_LeftTabByName")

function GetShop_RecommendUis(ui)
  local uis = {}
  uis.LeftTab = GetShop_LeftTabUis(ui:GetChild("LeftTab"))
  uis.TemplateList = ui:GetChild("TemplateList")
  uis.root = ui
  return uis
end
```

---

## other/Shop_SellOutByName.lua.lua
**Functions:**
- GetShop_SellOutUis
**Snippet:**
```lua
function GetShop_SellOutUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_ShopByName.lua.lua
**Functions:**
- GetShop_ShopUis
**Requires:**
- CommonResource_BackGroundByName
- Shop_CollectionByName
- Shop_TabRegionByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Shop_CollectionByName")
require("Shop_TabRegionByName")
require("CommonResource_CurrencyReturnByName")

function GetShop_ShopUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Collection = GetShop_CollectionUis(ui:GetChild("Collection"))
  uis.TabRegion = GetShop_TabRegionUis(ui:GetChild("TabRegion"))
```

---

## other/Shop_ShopWindowByName.lua.lua
**Functions:**
- GetShop_ShopWindowUis
**Requires:**
- Shop_ShopByName
**Snippet:**
```lua
require("Shop_ShopByName")

function GetShop_ShopWindowUis(ui)
  local uis = {}
  uis.Main = GetShop_ShopUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/Shop_StarByName.lua.lua
**Functions:**
- GetShop_StarUis
**Snippet:**
```lua
function GetShop_StarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## other/Shop_TabBtnBgByName.lua.lua
**Functions:**
- GetShop_TabBtnBgUis
**Snippet:**
```lua
function GetShop_TabBtnBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## other/Shop_TabBtnByName.lua.lua
**Functions:**
- GetShop_TabBtnUis
**Requires:**
- Shop_TabBtnBgByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("Shop_TabBtnBgByName")
require("CommonResource_RedDotByName")

function GetShop_TabBtnUis(ui)
  local uis = {}
  uis.TabBtnBg = GetShop_TabBtnBgUis(ui:GetChild("TabBtnBg"))
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
```

---

## other/Shop_TabRegionByName.lua.lua
**Functions:**
- GetShop_TabRegionUis
**Snippet:**
```lua
function GetShop_TabRegionUis(ui)
  local uis = {}
  
  uis.Tab1Btn = ui:GetChild("Tab1Btn")
  uis.Tab2Btn = ui:GetChild("Tab2Btn")
  uis.Tab3Btn = ui:GetChild("Tab3Btn")
  uis.Tab4Btn = ui:GetChild("Tab4Btn")
  uis.Tab5Btn = ui:GetChild("Tab5Btn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## other/Shop_Template1ByName.lua.lua
**Functions:**
- GetShop_Template1Uis
**Snippet:**
```lua
function GetShop_Template1Uis(ui)
  local uis = {}
  
  uis.Push1Btn = ui:GetChild("Push1Btn")
  uis.root = ui
  return uis
end
```

---

## other/Shop_Template1_1BtnByName.lua.lua
**Functions:**
- GetShop_Template1_1BtnUis
**Snippet:**
```lua
function GetShop_Template1_1BtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.PicHolder = ui:GetChild("PicHolder")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Shop_Template2ByName.lua.lua
**Functions:**
- GetShop_Template2Uis
**Snippet:**
```lua
function GetShop_Template2Uis(ui)
  local uis = {}
  
  uis.Push1Btn = ui:GetChild("Push1Btn")
  uis.Push2Btn = ui:GetChild("Push2Btn")
  uis.root = ui
  return uis
end
```

---

## other/Shop_Template2_1BtnByName.lua.lua
**Functions:**
- GetShop_Template2_1BtnUis
**Snippet:**
```lua
function GetShop_Template2_1BtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.PicHolder = ui:GetChild("PicHolder")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Shop_Template2_2BtnByName.lua.lua
**Functions:**
- GetShop_Template2_2BtnUis
**Snippet:**
```lua
function GetShop_Template2_2BtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.PicHolder = ui:GetChild("PicHolder")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Shop_Template3ByName.lua.lua
**Functions:**
- GetShop_Template3Uis
**Snippet:**
```lua
function GetShop_Template3Uis(ui)
  local uis = {}
  
  uis.Push1Btn = ui:GetChild("Push1Btn")
  uis.Push2Btn = ui:GetChild("Push2Btn")
  uis.Push3Btn = ui:GetChild("Push3Btn")
  uis.root = ui
  return uis
end
```

---

## other/Shop_Template3_1BtnByName.lua.lua
**Functions:**
- GetShop_Template3_1BtnUis
**Snippet:**
```lua
function GetShop_Template3_1BtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.PicHolder = ui:GetChild("PicHolder")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Shop_Template3_2BtnByName.lua.lua
**Functions:**
- GetShop_Template3_2BtnUis
**Snippet:**
```lua
function GetShop_Template3_2BtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.PicHolder = ui:GetChild("PicHolder")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Shop_Template3_3BtnByName.lua.lua
**Functions:**
- GetShop_Template3_3BtnUis
**Snippet:**
```lua
function GetShop_Template3_3BtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.PicHolder = ui:GetChild("PicHolder")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Shop_TokenByName.lua.lua
**Functions:**
- GetShop_TokenUis
**Requires:**
- Shop_LeftTabByName
- Shop_TokenListByName
**Snippet:**
```lua
require("Shop_LeftTabByName")
require("Shop_TokenListByName")

function GetShop_TokenUis(ui)
  local uis = {}
  uis.LeftTab = GetShop_LeftTabUis(ui:GetChild("LeftTab"))
  uis.TokenItem = GetShop_TokenListUis(ui:GetChild("TokenItem"))
  uis.ExplainBtn = ui:GetChild("ExplainBtn")
  uis.root = ui
  return uis
```

---

## other/Shop_TokenExplainByName.lua.lua
**Functions:**
- GetShop_TokenExplainUis
**Requires:**
- CommonResource_PopupBgByName
- Message_AssetsTipsGroupByName
- Shop_ExplainTitleByName
- Shop_ExplainStar1ByName
- Shop_ExplainStar2ByName
- Shop_ExplainStar3ByName
- Shop_ExplainStar4ByName
- Shop_ExplainStar5ByName
- Shop_ExplainWordByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Message_AssetsTipsGroupByName")
require("Shop_ExplainTitleByName")
require("Shop_ExplainStar1ByName")
require("Shop_ExplainStar2ByName")
require("Shop_ExplainStar3ByName")
require("Shop_ExplainStar4ByName")
require("Shop_ExplainStar5ByName")
require("Shop_ExplainWordByName")

```

---

## other/Shop_TokenExplainWindowByName.lua.lua
**Functions:**
- GetShop_TokenExplainWindowUis
**Requires:**
- Shop_TokenExplainByName
**Snippet:**
```lua
require("Shop_TokenExplainByName")

function GetShop_TokenExplainWindowUis(ui)
  local uis = {}
  uis.Main = GetShop_TokenExplainUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/Shop_TokenListByName.lua.lua
**Functions:**
- GetShop_TokenListUis
**Snippet:**
```lua
function GetShop_TokenListUis(ui)
  local uis = {}
  
  uis.TokenList = ui:GetChild("TokenList")
  uis.root = ui
  return uis
end
```

---

## other/Shop_TokenSellOutByName.lua.lua
**Functions:**
- GetShop_TokenSellOutUis
**Snippet:**
```lua
function GetShop_TokenSellOutUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_TokenTipsAniByName.lua.lua
**Functions:**
- GetShop_TokenTipsAniUis
**Requires:**
- Shop_TokenTipsByName
**Snippet:**
```lua
require("Shop_TokenTipsByName")

function GetShop_TokenTipsAniUis(ui)
  local uis = {}
  uis.TokenTips = GetShop_TokenTipsUis(ui:GetChild("TokenTips"))
  uis.root = ui
  return uis
end
```

---

## other/Shop_TokenTipsBtnByName.lua.lua
**Functions:**
- GetShop_TokenTipsBtnUis
**Requires:**
- Shop_CardHeadBgByName
- Shop_DiscountByName
- Shop_OriginalPriceByName
- Shop_UseMarkByName
- Shop_TokenTipsTimeByName
**Snippet:**
```lua
require("Shop_CardHeadBgByName")
require("Shop_DiscountByName")
require("Shop_OriginalPriceByName")
require("Shop_UseMarkByName")
require("Shop_TokenTipsTimeByName")

function GetShop_TokenTipsBtnUis(ui)
  local uis = {}
  uis.CardHead = GetShop_CardHeadBgUis(ui:GetChild("CardHead"))
  uis.ItemLoader = ui:GetChild("ItemLoader")
```

---

## other/Shop_TokenTipsByName.lua.lua
**Functions:**
- GetShop_TokenTipsUis
**Requires:**
- Shop_TokenSellOutByName
**Snippet:**
```lua
require("Shop_TokenSellOutByName")

function GetShop_TokenTipsUis(ui)
  local uis = {}
  uis.TokenTipsBtn = ui:GetChild("TokenTipsBtn")
  uis.SellOut = GetShop_TokenSellOutUis(ui:GetChild("SellOut"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Shop_TokenTipsTimeByName.lua.lua
**Functions:**
- GetShop_TokenTipsTimeUis
**Snippet:**
```lua
function GetShop_TokenTipsTimeUis(ui)
  local uis = {}
  
  uis.TimeHolder = ui:GetChild("TimeHolder")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## other/Shop_UseMarkByName.lua.lua
**Functions:**
- GetShop_UseMarkUis
**Snippet:**
```lua
function GetShop_UseMarkUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Shop_WearingByName.lua.lua
**Functions:**
- GetShop_WearingUis
**Snippet:**
```lua
function GetShop_WearingUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/SignData.lua.lua
**Functions:**
- SignData.ClearData
- SignData.GetTurnActData
- SignData.SaveActivityData
- SignData.UpdateOneActivityData
- SignData.GetActivitySignInData
- SignData.GetSignData
- SignData.GetReservationData
- SignData.CanShowReservation
**Snippet:**
```lua
SignData = {
  activityData = {},
  showAct = {}
}
SignTypeEnum = {
  SIGN_IN_ACT = 10118,
  STAGE_ACT = 10119,
  SEARCH_ACT = 10123,
  RETURN_ACT = 10132,
  TURNTABLE_ACT = 10134
```

---

## other/SignScriptList.lua.lua
**Requires:**
- SignData
- SignService
**Snippet:**
```lua
local require = require
require("SignData")
require("SignService")
```

---

## other/SignService.lua.lua
**Functions:**
- SignService.Init
- SignService.GetActivityAllReq
- SignService.GetActivityAllRsp
- SignService.GetAllBannerReq
- SignService.GetAllBannerRsp
- SignService.ActivitySignInReq
- SignService.ActivitySignInRsp
- SignService.ActivitySearchReq
- SignService.ActivitySearchRsp
- SignService.ActivityReturnSignInReq
- SignService.ActivityReturnSignInRsp
- SignService.ActivityDoTurnTableReq
- SignService.ActivityDoTurnTableRsp
- SignService.ActivityDoTurnTableRoundReq
- SignService.ActivityDoTurnTableRoundRsp
- SignService.FetchAccumRechargeRewardReq
- SignService.FetchAccumRechargeRewardRsp
- SignService.ActivityTurnTableGetFreeReq
- SignService.ActivityTurnTableGetFreeRsp
**Snippet:**
```lua
SignService = {}

function SignService.Init()
  Net.AddListener(Proto.MsgName.GetActivityAllRsp, SignService.GetActivityAllRsp)
  Net.AddListener(Proto.MsgName.ActivitySignInRsp, SignService.ActivitySignInRsp)
  Net.AddListener(Proto.MsgName.ActivitySearchRsp, SignService.ActivitySearchRsp)
  Net.AddListener(Proto.MsgName.GetAllBannerRsp, SignService.GetAllBannerRsp)
  Net.AddListener(Proto.MsgName.ActivityReturnSignInRsp, SignService.ActivityReturnSignInRsp)
  Net.AddListener(Proto.MsgName.ActivityDoTurnTableRsp, SignService.ActivityDoTurnTableRsp)
  Net.AddListener(Proto.MsgName.ActivityDoTurnTableRoundRsp, SignService.ActivityDoTurnTableRoundRsp)
```

---

## other/SignWindow.lua.lua
**Functions:**
- SignWindow.OnInit
- SignWindow.InitModuleCard
- SignWindow.InitModuleFour
- SignWindow.InitModule
- SignWindow.SetDayTips
- SignWindow.InitModuleList
- list.itemRenderer
- SignWindow.ShowReward
- list.itemRenderer
- SignWindow.InitBtn
- SignWindow.CloseWindow
- SignWindow.HandleMessage
- SignWindow.OnClose
- SignWindow.CheckActivityEnd
- SignWindow.HandleMessage
**Requires:**
- Sign_SignWindowByName
**Snippet:**
```lua
require("Sign_SignWindowByName")
local SignWindow = {}
local uis, contentPane, data, activityData, signData

function SignWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.SignWindow.package, WinResConfig.SignWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetSign_SignWindowUis(contentPane)
    data = bridgeObj.argTable[1]
```

---

## other/Sign_ItemFrameByName.lua.lua
**Functions:**
- GetSign_ItemFrameUis
**Requires:**
- CommonResource_ItemCardPicByName
- CommonResource_ItemTimeByName
**Snippet:**
```lua
require("CommonResource_ItemCardPicByName")
require("CommonResource_ItemTimeByName")

function GetSign_ItemFrameUis(ui)
  local uis = {}
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.ItemCardPic = GetCommonResource_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.ItemTime = GetCommonResource_ItemTimeUis(ui:GetChild("ItemTime"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
```

---

## other/Sign_Module1ByName.lua.lua
**Functions:**
- GetSign_Module1Uis
**Snippet:**
```lua
function GetSign_Module1Uis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.root = ui
  return uis
end
```

---

## other/Sign_Module1CloseBtnByName.lua.lua
**Functions:**
- GetSign_Module1CloseBtnUis
**Snippet:**
```lua
function GetSign_Module1CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Sign_Module1InfoByName.lua.lua
**Functions:**
- GetSign_Module1InfoUis
**Requires:**
- Sign_Mudule1ColorTipsByName
- Sign_Mudule1GreenTipsByName
**Snippet:**
```lua
require("Sign_Mudule1ColorTipsByName")
require("Sign_Mudule1GreenTipsByName")

function GetSign_Module1InfoUis(ui)
  local uis = {}
  uis.ColorTips = GetSign_Mudule1ColorTipsUis(ui:GetChild("ColorTips"))
  uis.GreenTips = GetSign_Mudule1GreenTipsUis(ui:GetChild("GreenTips"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
```

---

## other/Sign_Module2ByName.lua.lua
**Functions:**
- GetSign_Module2Uis
**Snippet:**
```lua
function GetSign_Module2Uis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.root = ui
  return uis
end
```

---

## other/Sign_Module2InfoByName.lua.lua
**Functions:**
- GetSign_Module2InfoUis
**Requires:**
- Sign_Mudule2ColorTipsByName
- Sign_Mudule2GreyTipsByName
**Snippet:**
```lua
require("Sign_Mudule2ColorTipsByName")
require("Sign_Mudule2GreyTipsByName")

function GetSign_Module2InfoUis(ui)
  local uis = {}
  uis.ColorTips = GetSign_Mudule2ColorTipsUis(ui:GetChild("ColorTips"))
  uis.GreenTips = GetSign_Mudule2GreyTipsUis(ui:GetChild("GreenTips"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
```

---

## other/Sign_Module3BtnByName.lua.lua
**Functions:**
- GetSign_Module3BtnUis
**Snippet:**
```lua
function GetSign_Module3BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Sign_Module3ByName.lua.lua
**Functions:**
- GetSign_Module3Uis
**Requires:**
- CommonResource_ItemFrameByName
- Sign_Module3ReceivedByName
**Snippet:**
```lua
require("CommonResource_ItemFrameByName")
require("Sign_Module3ReceivedByName")

function GetSign_Module3Uis(ui)
  local uis = {}
  uis.Item = GetCommonResource_ItemFrameUis(ui:GetChild("Item"))
  uis.SureBtn = ui:GetChild("SureBtn")
  uis.Module3Received = GetSign_Module3ReceivedUis(ui:GetChild("Module3Received"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## other/Sign_Module3CloseBtnByName.lua.lua
**Functions:**
- GetSign_Module3CloseBtnUis
**Snippet:**
```lua
function GetSign_Module3CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Sign_Module3ReceivedByName.lua.lua
**Functions:**
- GetSign_Module3ReceivedUis
**Snippet:**
```lua
function GetSign_Module3ReceivedUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## other/Sign_Module4ByName.lua.lua
**Functions:**
- GetSign_Module4Uis
**Snippet:**
```lua
function GetSign_Module4Uis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Sign_Module4CloseBtnByName.lua.lua
**Functions:**
- GetSign_Module4CloseBtnUis
**Snippet:**
```lua
function GetSign_Module4CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Sign_Module4GetBtnByName.lua.lua
**Functions:**
- GetSign_Module4GetBtnUis
**Snippet:**
```lua
function GetSign_Module4GetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Sign_Module5ByName.lua.lua
**Functions:**
- GetSign_Module5Uis
**Requires:**
- Sign_Module5ObtainByName
**Snippet:**
```lua
require("Sign_Module5ObtainByName")

function GetSign_Module5Uis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.Obtain = GetSign_Module5ObtainUis(ui:GetChild("Obtain"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## other/Sign_Module5CloseBtnByName.lua.lua
**Functions:**
- GetSign_Module5CloseBtnUis
**Snippet:**
```lua
function GetSign_Module5CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Sign_Module5GetBtnByName.lua.lua
**Functions:**
- GetSign_Module5GetBtnUis
**Snippet:**
```lua
function GetSign_Module5GetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Sign_Module5ObtainByName.lua.lua
**Functions:**
- GetSign_Module5ObtainUis
**Snippet:**
```lua
function GetSign_Module5ObtainUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Sign_Mudule1ColorTipsByName.lua.lua
**Functions:**
- GetSign_Mudule1ColorTipsUis
**Snippet:**
```lua
function GetSign_Mudule1ColorTipsUis(ui)
  local uis = {}
  
  uis.NumberDecTxt = ui:GetChild("NumberDecTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## other/Sign_Mudule1GreenTipsByName.lua.lua
**Functions:**
- GetSign_Mudule1GreenTipsUis
**Snippet:**
```lua
function GetSign_Mudule1GreenTipsUis(ui)
  local uis = {}
  
  uis.NumberDecTxt = ui:GetChild("NumberDecTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Sign_Mudule2ColorTipsByName.lua.lua
**Functions:**
- GetSign_Mudule2ColorTipsUis
**Snippet:**
```lua
function GetSign_Mudule2ColorTipsUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.NumberDecTxt = ui:GetChild("NumberDecTxt")
  uis.root = ui
  return uis
end
```

---

## other/Sign_Mudule2GreyTipsByName.lua.lua
**Functions:**
- GetSign_Mudule2GreyTipsUis
**Snippet:**
```lua
function GetSign_Mudule2GreyTipsUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.NumberDecTxt = ui:GetChild("NumberDecTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Sign_Sign1ByName.lua.lua
**Functions:**
- GetSign_Sign1Uis
**Requires:**
- Sign_Module1ByName
- Sign_Module2ByName
- Sign_Module3ByName
- Sign_Module4ByName
- Sign_Module5ByName
**Snippet:**
```lua
require("Sign_Module1ByName")
require("Sign_Module2ByName")
require("Sign_Module3ByName")
require("Sign_Module4ByName")
require("Sign_Module5ByName")

function GetSign_Sign1Uis(ui)
  local uis = {}
  uis.Pic1Loader = ui:GetChild("Pic1Loader")
  uis.Pic2Loader = ui:GetChild("Pic2Loader")
```

---

## other/Sign_Sign2ByName.lua.lua
**Functions:**
- GetSign_Sign2Uis
**Requires:**
- CommonResource_PopupBgByName
- Sign_Sign1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Sign_Sign1ByName")

function GetSign_Sign2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Sign1 = GetSign_Sign1Uis(ui:GetChild("Sign1"))
  uis.root = ui
  return uis
```

---

## other/Sign_SignWindowByName.lua.lua
**Functions:**
- GetSign_SignWindowUis
**Requires:**
- Sign_Sign2ByName
**Snippet:**
```lua
require("Sign_Sign2ByName")

function GetSign_SignWindowUis(ui)
  local uis = {}
  uis.Main = GetSign_Sign2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/SimpleExpeditionRewardWindow.lua.lua
**Functions:**
- SimpleExpeditionRewardWindow.ReInitData
- SimpleExpeditionRewardWindow.OnInit
- SimpleExpeditionRewardWindow.UpdateInfo
- SimpleExpeditionRewardWindow.InitBtn
- SimpleExpeditionRewardWindow.OnShown
- SimpleExpeditionRewardWindow.OnClose
- SimpleExpeditionRewardWindow.HandleMessage
**Requires:**
- Abyss_ExpeditionRewardWindowByName
**Snippet:**
```lua
require("Abyss_ExpeditionRewardWindowByName")
local SimpleExpeditionRewardWindow = {}
local uis, contentPane, rewardBuffer
local RewardItemRenderer = function(i, gcmp)
  local gotRewards = ExpeditionData.GetRewardsInfo()
  local conf = rewardBuffer[i + 1]
  local rewardId = conf.id
  local subgcmp = gcmp:GetChild("Item")
  local btn = subgcmp
  local stateCtr = subgcmp:GetController("c1")
```

---

## other/SkillTipsWindow.lua.lua
**Functions:**
- SkillTipsWindow.ReInitData
- SkillTipsWindow.OnInit
- SkillTipsWindow.Init
- uis.Main.SkillTips1.UnitList.itemRenderer
- SkillTipsWindow.InitBtn
- SkillTipsWindow.OnShown
- SkillTipsWindow.OnHide
- SkillTipsWindow.OnClose
- SkillTipsWindow.HandleMessage
**Requires:**
- Message_SkillTipsWindowByName
**Snippet:**
```lua
require("Message_SkillTipsWindowByName")
local SkillTipsWindow = {}
local uis, contentPane, msg

function SkillTipsWindow.ReInitData()
end

function SkillTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.SkillTipsWindow.package, WinResConfig.SkillTipsWindow.comName, function(com)
    contentPane = com
```

---

## other/SkillUpSuccessWindow.lua.lua
**Functions:**
- SkillUpSuccessWindow.ReInitData
- SkillUpSuccessWindow.OnInit
- SkillUpSuccessWindow.UpdateInfo
- SkillUpSuccessWindow.InitBtn
- SkillUpSuccessWindow.OnClose
**Requires:**
- Card_SkillUpSuccessWindowByName
**Snippet:**
```lua
require("Card_SkillUpSuccessWindowByName")
local SkillUpSuccessWindow = {}
local uis, contentPane

function SkillUpSuccessWindow.ReInitData()
end

function SkillUpSuccessWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.SkillUpSuccessWindow.package, WinResConfig.SkillUpSuccessWindow.comName, function(com)
    contentPane = com
```

---

## other/SortingHelper.lua.lua
**Functions:**
- SortingHelper.SetOrderInLayer
**Snippet:**
```lua
local SortingHelper = {}

function SortingHelper.SetOrderInLayer(gameObject, layerInt)
  if IsNil(gameObject) == false then
    local layer = math.ceil(layerInt) or 0
    LuaUtil.SetChildrenOrderInLayer(gameObject, layer)
  else
    print("Error: GameObject is Nil")
  end
end
```

---

## other/SoundUtil.lua.lua
**Functions:**
- SoundUtil.SetSfxSpeedInBattle
- SoundUtil.PlaySfxInBattle
- SoundUtil.PlayUISfx
- SoundUtil.PlaySfx
- SoundUtil.PlaySfxByPath
- SoundUtil.PlayMusic
- SoundUtil.StopCurMusic
- SoundUtil.PlayLastMusic
- SoundUtil.PlayVoice
- SoundUtil.GetCurMusic
- SoundUtil.StopSoundEvent
- SoundUtil.PlayHomeMusic
**Snippet:**
```lua
SOUND_EVENT_ENUM = {
  COMMON_CLICK = "event:/sfx/sfx_ui/ui_sys/ui_click_gen",
  COMMON_BACK = "event:/sfx/sfx_ui/ui_sys/ui_click_back",
  COMMON_NOTICE = "event:/sfx/sfx_ui/ui_sys/ui_notif_illegal",
  COMMON_TAG_ON_CLICK = "event:/sfx/sfx_ui/ui_sys/ui_tag_1_chld",
  LV_UP_SUCCEED = "event:/sfx/sfx_ui/ui_sys/ui_role_lvup",
  TAB_TAG1 = "event:/sfx/sfx_ui/ui_sys/ui_tag_1",
  TAB_TAG2 = "event:/sfx/sfx_ui/ui_sys/ui_tag_2",
  TAB_TAG_BOTTOM = "event:/sfx/sfx_ui/ui_sys/ui_tag_bottom",
  SLIDE_EFFECT = "event:/sfx/sfx_ui/ui_sys/ui_slide_sidein",
```

---

## other/SpineInteractionMgr.lua.lua
**Snippet:**
```lua
local GESTURE_HANDLE_KEY = {
  CLICK = "CLICK",
  DOUBLE_CLICK = "DOUBLE_CLICK",
  LONG_PRESS = "LONG_PRESS",
  DRAG = "DRAG",
  SWIPE = "SWIPE",
  PINCH = "PINCH"
}
local GESTURE_HANDLE = {
  CLICK = "OnClick",
```

---

## other/StarConditionTipsWindow.lua.lua
**Functions:**
- StarConditionTipsWindow.ReInitData
- StarConditionTipsWindow.OnInit
- StarConditionTipsWindow.UpdateInfo
- goallist.itemRenderer
- StarConditionTipsWindow.InitBtn
- StarConditionTipsWindow.Close
- StarConditionTipsWindow.OnClose
**Requires:**
- Formation_StarConditionTipsWindowByName
**Snippet:**
```lua
require("Formation_StarConditionTipsWindowByName")
local StarConditionTipsWindow = {}
local uis, contentPane

function StarConditionTipsWindow.ReInitData()
end

function StarConditionTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.StarConditionTipsWindow.package, WinResConfig.StarConditionTipsWindow.comName, function(com)
    contentPane = com
```

---

## other/StarOneSkillWindow.lua.lua
**Functions:**
- StarOneSkillWindow.ReInitData
- StarOneSkillWindow.OnInit
- StarOneSkillWindow.UpdateInfo
- StarOneSkillWindow.InitBtn
- StarOneSkillWindow.OnClose
**Requires:**
- Message_StarOneSkillWindowByName
**Snippet:**
```lua
require("Message_StarOneSkillWindowByName")
local StarOneSkillWindow = {}
local uis, contentPane, msg

function StarOneSkillWindow.ReInitData()
end

function StarOneSkillWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.StarOneSkillWindow.package, WinResConfig.StarOneSkillWindow.comName, function(com)
    contentPane = com
```

---

## other/StarSkillWindow.lua.lua
**Functions:**
- StarSkillWindow.ReInitData
- StarSkillWindow.OnInit
- StarSkillWindow.UpdateInfo
- skillList.itemRenderer
- wordList.itemRenderer
- StarSkillWindow.InitBtn
- StarSkillWindow.Close
- StarSkillWindow.OnClose
**Requires:**
- Message_StarSkillWindowByName
**Snippet:**
```lua
require("Message_StarSkillWindowByName")
local StarSkillWindow = {}
local uis, contentPane, cardId

function StarSkillWindow.ReInitData()
end

function StarSkillWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.StarSkillWindow.package, WinResConfig.StarSkillWindow.comName, function(com)
    contentPane = com
```

---

## other/StarUpTipsWindow.lua.lua
**Functions:**
- StarUpTipsWindow.ReInitData
- StarUpTipsWindow.OnInit
- StarUpTipsWindow.LoadCardTexture
- StarUpTipsWindow.ShowStarEffect
- StarUpTipsWindow.InitInfo
- uis.Main.SkillInfoAni.WordList.itemRenderer
- StarUpTipsWindow.ShowStar
- StarUpTipsWindow.InitBtn
- StarUpTipsWindow.OnShown
- StarUpTipsWindow.OnHide
- StarUpTipsWindow.OnClose
- StarUpTipsWindow.HandleMessage
**Requires:**
- Card_StarUpTipsWindowByName
**Snippet:**
```lua
require("Card_StarUpTipsWindowByName")
local StarUpTipsWindow = {}
local uis, contentPane, msg, bgPrefab, startPos, backEffect

function StarUpTipsWindow.ReInitData()
end

function StarUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.StarUpTipsWindow.package, WinResConfig.StarUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## other/StoryCardStarWindow.lua.lua
**Functions:**
- StoryCardStarWindow.ReInitData
- StoryCardStarWindow.OnInit
- StoryCardStarWindow.UpdateInfo
- cardAttributeList.itemRenderer
- tips.DotList.itemRenderer
- StoryCardStarWindow.GetAttData
- StoryCardStarWindow.GetStar
- StoryCardStarWindow.InitBtn
- StoryCardStarWindow.OnClose
**Requires:**
- Story_CardStarWindowByName
**Snippet:**
```lua
require("Story_CardStarWindowByName")
local StoryCardStarWindow = {}
local uis, contentPane, handBookData, lastAttAdd

function StoryCardStarWindow.ReInitData()
end

function StoryCardStarWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.StoryCardStarWindow.package, WinResConfig.StoryCardStarWindow.comName, function(com)
    contentPane = com
```

---

## other/StoryMgr.lua.lua
**Functions:**
- StoryMgr.GetMonsterName
- StoryMgr.SaveMonsterId
- StoryMgr.SaveStoryId
- StoryMgr.SaveStoryEventId
- StoryMgr.CheckNew
- StoryMgr.SaveEventNewReq
- StoryMgr.InitTab
- list.itemRenderer
- StoryMgr.CheckNewStoryList
- StoryMgr.UnlockByData
- StoryMgr.GetMusicNum
- StoryMgr.GetUnlockData
- StoryMgr.InitData
- StoryMgr.GetUnlockId
- StoryMgr.GetPlotData
- StoryMgr.GetMusicData
- StoryMgr.GetMonsterDataByCampId
- StoryMgr.SortLock
- StoryMgr.GetPlotItem
- StoryMgr.GetCgData
**Snippet:**
```lua
StoryMgr = {
  storyList = {},
  musicData = {},
  plotData = {},
  cgData = {},
  monsterIds = {}
}

function StoryMgr.GetMonsterName(type)
  if 0 == type then
```

---

## other/StoryScriptList.lua.lua
**Requires:**
- StoryMgr
- StoryService
**Snippet:**
```lua
local require = require
require("StoryMgr")
require("StoryService")
```

---

## other/StoryService.lua.lua
**Functions:**
- StoryService.Init
- StoryService.GetStoryMonsterListReq
- StoryService.GetStoryMonsterListRsp
- StoryService.ClickStoryEventReportReq
- StoryService.ClickStoryEventReportRsp
**Snippet:**
```lua
StoryService = {}

function StoryService.Init()
  Net.AddListener(Proto.MsgName.GetStoryMonsterListRsp, StoryService.GetStoryMonsterListRsp)
  Net.AddListener(Proto.MsgName.ClickStoryEventReportRsp, StoryService.ClickStoryEventReportRsp)
end

function StoryService.GetStoryMonsterListReq(rspCallback)
  local msg = {}
  Net.Send(Proto.MsgName.GetStoryMonsterListReq, msg, rspCallback)
```

---

## other/StoryWindow.lua.lua
**Functions:**
- StoryWindow.OnInit
- StoryWindow.OpenMainPlot
- StoryWindow.SetPlotInfo
- main.SegmentRegion.SegmentList.itemRenderer
- StoryWindow.OpenBranchPlot
- StoryWindow.OpenCg
- list.itemRenderer
- StoryWindow.LoadList
- list.itemRenderer
- StoryWindow.OpenMusic
- list.itemRenderer
- StoryWindow.ShowSoundItem
- list.itemRenderer
- StoryWindow.GetMonsterCamp
- StoryWindow.OpenMonster
- uis.Main.Monster.MonsterList.itemRenderer
- StoryWindow.SetNewOnScroll
- StoryWindow.ShowMonsterInfo
- info.HeadList.itemRenderer
- info.Tab2Region.TabBtnList.itemRenderer
- StoryWindow.InitInfoWord
- StoryWindow.OpenWord
- StoryWindow.OpenItemInfo
- info.ItemList.itemRenderer
- ShowHaveCardInfo
- list.itemRenderer
- list.itemRenderer
- StoryWindow.InitCardScreenBtn
- StoryWindow.GetIsChoice
- StoryWindow.RefreshCardScreenUI
- StoryWindow.ShowChoiceList
- tips.CardList.itemRenderer
- StoryWindow.OpenCardMap
- tips.CardList.itemRenderer
- StoryWindow.InitBtn
- uis.Main.TabRegion.TabList.itemRenderer
- StoryWindow.HandleMessage
- StoryWindow.OnShown
- StoryWindow.OnClose
**Requires:**
- Story_StoryWindowByName
**Snippet:**
```lua
require("Story_StoryWindowByName")
local StoryWindow = {}
local uis, contentPane, allPlotItem, tabMainIndex, jumpTb, plotJump

function StoryWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.StoryWindow.package, WinResConfig.StoryWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetStory_StoryWindowUis(contentPane)
    uis.Main.BackGround.BackGroundLoader.url = UIUtil.GetBackgroundUrl(FEATURE_ENUM.HOME_STORY)
```

---

## other/Story_AnBtnByName.lua.lua
**Functions:**
- GetStory_AnBtnUis
**Requires:**
- Story_Card_BgAniByName
**Snippet:**
```lua
require("Story_Card_BgAniByName")

function GetStory_AnBtnUis(ui)
  local uis = {}
  uis.BgAni = GetStory_Card_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Story_AuthorInfoByName.lua.lua
**Functions:**
- GetStory_AuthorInfoUis
**Snippet:**
```lua
function GetStory_AuthorInfoUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## other/Story_CardByName.lua.lua
**Functions:**
- GetStory_CardUis
**Requires:**
- Story_Card_TitleByName
- Story_Card_ScreenByName
**Snippet:**
```lua
require("Story_Card_TitleByName")
require("Story_Card_ScreenByName")

function GetStory_CardUis(ui)
  local uis = {}
  uis.Title = GetStory_Card_TitleUis(ui:GetChild("Title"))
  uis.CardList = ui:GetChild("CardList")
  uis.RewardBtn = ui:GetChild("RewardBtn")
  uis.ScreenBtn = ui:GetChild("ScreenBtn")
  uis.Screen = GetStory_Card_ScreenUis(ui:GetChild("Screen"))
```

---

## other/Story_CardStarByName.lua.lua
**Functions:**
- GetStory_CardStarUis
**Requires:**
- CommonResource_PopupBgByName
- Story_CardStar_TipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Story_CardStar_TipsByName")

function GetStory_CardStarUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Tips = GetStory_CardStar_TipsUis(ui:GetChild("Tips"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## other/Story_CardStarWindowByName.lua.lua
**Functions:**
- GetStory_CardStarWindowUis
**Requires:**
- Story_CardStarByName
**Snippet:**
```lua
require("Story_CardStarByName")

function GetStory_CardStarWindowUis(ui)
  local uis = {}
  uis.Main = GetStory_CardStarUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/Story_CardStar_AttributeByName.lua.lua
**Functions:**
- GetStory_CardStar_AttributeUis
**Snippet:**
```lua
function GetStory_CardStar_AttributeUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Story_CardStar_Dot1ByName.lua.lua
**Functions:**
- GetStory_CardStar_Dot1Uis
**Snippet:**
```lua
function GetStory_CardStar_Dot1Uis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.EffectHolder1 = ui:GetChild("EffectHolder1")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## other/Story_CardStar_Dot2ByName.lua.lua
**Functions:**
- GetStory_CardStar_Dot2Uis
**Snippet:**
```lua
function GetStory_CardStar_Dot2Uis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Story_CardStar_Dot3ByName.lua.lua
**Functions:**
- GetStory_CardStar_Dot3Uis
**Snippet:**
```lua
function GetStory_CardStar_Dot3Uis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## other/Story_CardStar_Dot4BtnByName.lua.lua
**Functions:**
- GetStory_CardStar_Dot4BtnUis
**Snippet:**
```lua
function GetStory_CardStar_Dot4BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Story_CardStar_DotAniByName.lua.lua
**Functions:**
- GetStory_CardStar_DotAniUis
**Requires:**
- Story_CardStar_Dot1ByName
- Story_CardStar_Dot2ByName
- Story_CardStar_Dot3ByName
**Snippet:**
```lua
require("Story_CardStar_Dot1ByName")
require("Story_CardStar_Dot2ByName")
require("Story_CardStar_Dot3ByName")

function GetStory_CardStar_DotAniUis(ui)
  local uis = {}
  uis.Dot1 = GetStory_CardStar_Dot1Uis(ui:GetChild("Dot1"))
  uis.Dot2 = GetStory_CardStar_Dot2Uis(ui:GetChild("Dot2"))
  uis.Dot3 = GetStory_CardStar_Dot3Uis(ui:GetChild("Dot3"))
  uis.Dot4Btn = ui:GetChild("Dot4Btn")
```

---

## other/Story_CardStar_InfoByName.lua.lua
**Functions:**
- GetStory_CardStar_InfoUis
**Snippet:**
```lua
function GetStory_CardStar_InfoUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## other/Story_CardStar_TipsByName.lua.lua
**Functions:**
- GetStory_CardStar_TipsUis
**Requires:**
- Story_CardStar_InfoByName
**Snippet:**
```lua
require("Story_CardStar_InfoByName")

function GetStory_CardStar_TipsUis(ui)
  local uis = {}
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.AttributeList = ui:GetChild("AttributeList")
  uis.Info = GetStory_CardStar_InfoUis(ui:GetChild("Info"))
  uis.DotList = ui:GetChild("DotList")
  uis.root = ui
  return uis
```

---

## other/Story_Card_AllBtnByName.lua.lua
**Functions:**
- GetStory_Card_AllBtnUis
**Snippet:**
```lua
function GetStory_Card_AllBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Story_Card_BgAniByName.lua.lua
**Functions:**
- GetStory_Card_BgAniUis
**Snippet:**
```lua
function GetStory_Card_BgAniUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## other/Story_Card_ElementChoiceByName.lua.lua
**Functions:**
- GetStory_Card_ElementChoiceUis
**Snippet:**
```lua
function GetStory_Card_ElementChoiceUis(ui)
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

## other/Story_Card_GatherChoiceByName.lua.lua
**Functions:**
- GetStory_Card_GatherChoiceUis
**Requires:**
- Story_Card_ElementChoiceByName
- Story_Card_OccupationChoiceByName
**Snippet:**
```lua
require("Story_Card_ElementChoiceByName")
require("Story_Card_OccupationChoiceByName")

function GetStory_Card_GatherChoiceUis(ui)
  local uis = {}
  uis.ElementChoice = GetStory_Card_ElementChoiceUis(ui:GetChild("ElementChoice"))
  uis.OccupationChoice = GetStory_Card_OccupationChoiceUis(ui:GetChild("OccupationChoice"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.Number1Txt = ui:GetChild("Number1Txt")
```

---

## other/Story_Card_OccupationChoiceByName.lua.lua
**Functions:**
- GetStory_Card_OccupationChoiceUis
**Snippet:**
```lua
function GetStory_Card_OccupationChoiceUis(ui)
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

## other/Story_Card_RewardBtnByName.lua.lua
**Functions:**
- GetStory_Card_RewardBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetStory_Card_RewardBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Story_Card_ScreenBtnByName.lua.lua
**Functions:**
- GetStory_Card_ScreenBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetStory_Card_ScreenBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Story_Card_ScreenByName.lua.lua
**Functions:**
- GetStory_Card_ScreenUis
**Requires:**
- Story_Card_GatherChoiceByName
**Snippet:**
```lua
require("Story_Card_GatherChoiceByName")

function GetStory_Card_ScreenUis(ui)
  local uis = {}
  uis.PopupCloseBtn = ui:GetChild("PopupCloseBtn")
  uis.GatherChoice = GetStory_Card_GatherChoiceUis(ui:GetChild("GatherChoice"))
  uis.root = ui
  return uis
end
```

---

## other/Story_Card_TipsBgByName.lua.lua
**Functions:**
- GetStory_Card_TipsBgUis
**Snippet:**
```lua
function GetStory_Card_TipsBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Story_Card_TipsByName.lua.lua
**Functions:**
- GetStory_Card_TipsUis
**Requires:**
- Story_Card_TipsBgByName
**Snippet:**
```lua
require("Story_Card_TipsBgByName")

function GetStory_Card_TipsUis(ui)
  local uis = {}
  uis.TipsBg = GetStory_Card_TipsBgUis(ui:GetChild("TipsBg"))
  uis.StarList = ui:GetChild("StarList")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.RewardBtn = ui:GetChild("RewardBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## other/Story_Card_TipsRegionByName.lua.lua
**Functions:**
- GetStory_Card_TipsRegionUis
**Requires:**
- Story_Card_TipsTitleByName
**Snippet:**
```lua
require("Story_Card_TipsTitleByName")

function GetStory_Card_TipsRegionUis(ui)
  local uis = {}
  uis.Title = GetStory_Card_TipsTitleUis(ui:GetChild("Title"))
  uis.CardList = ui:GetChild("CardList")
  uis.root = ui
  return uis
end
```

---

## other/Story_Card_TipsRewardBtnByName.lua.lua
**Functions:**
- GetStory_Card_TipsRewardBtnUis
**Snippet:**
```lua
function GetStory_Card_TipsRewardBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Story_Card_TipsTitleByName.lua.lua
**Functions:**
- GetStory_Card_TipsTitleUis
**Snippet:**
```lua
function GetStory_Card_TipsTitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Story_Card_TitleByName.lua.lua
**Functions:**
- GetStory_Card_TitleUis
**Snippet:**
```lua
function GetStory_Card_TitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## other/Story_CGByName.lua.lua
**Functions:**
- GetStory_CGUis
**Requires:**
- Story_Tab2RegionByName
- Story_CGNumberByName
**Snippet:**
```lua
require("Story_Tab2RegionByName")
require("Story_CGNumberByName")

function GetStory_CGUis(ui)
  local uis = {}
  uis.Tab2Region = GetStory_Tab2RegionUis(ui:GetChild("Tab2Region"))
  uis.CGNumber = GetStory_CGNumberUis(ui:GetChild("CGNumber"))
  uis.CGList = ui:GetChild("CGList")
  uis.root = ui
  return uis
```

---

## other/Story_CGIconBtnAniByName.lua.lua
**Functions:**
- GetStory_CGIconBtnAniUis
**Snippet:**
```lua
function GetStory_CGIconBtnAniUis(ui)
  local uis = {}
  
  uis.CGIconBtn = ui:GetChild("CGIconBtn")
  uis.root = ui
  return uis
end
```

---

## other/Story_CGIconBtnByName.lua.lua
**Functions:**
- GetStory_CGIconBtnUis
**Requires:**
- Story_NewByName
**Snippet:**
```lua
require("Story_NewByName")

function GetStory_CGIconBtnUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.New = GetStory_NewUis(ui:GetChild("New"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
```

---

## other/Story_CGNumberByName.lua.lua
**Functions:**
- GetStory_CGNumberUis
**Snippet:**
```lua
function GetStory_CGNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## other/Story_CGShowByName.lua.lua
**Functions:**
- GetStory_CGShowUis
**Requires:**
- CommonResource_BackGroundByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")

function GetStory_CGShowUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.CGShowCloseBtn = ui:GetChild("CGShowCloseBtn")
  uis.HideWordBtn = ui:GetChild("HideWordBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## other/Story_CGShowCloseBtnByName.lua.lua
**Functions:**
- GetStory_CGShowCloseBtnUis
**Snippet:**
```lua
function GetStory_CGShowCloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Story_CGShowWindowByName.lua.lua
**Functions:**
- GetStory_CGShowWindowUis
**Requires:**
- Story_CGShowByName
**Snippet:**
```lua
require("Story_CGShowByName")

function GetStory_CGShowWindowUis(ui)
  local uis = {}
  uis.Main = GetStory_CGShowUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/Story_CoverBtnByName.lua.lua
**Functions:**
- GetStory_CoverBtnUis
**Requires:**
- Story_NewByName
**Snippet:**
```lua
require("Story_NewByName")

function GetStory_CoverBtnUis(ui)
  local uis = {}
  uis.CoverLoader = ui:GetChild("CoverLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.New = GetStory_NewUis(ui:GetChild("New"))
  uis.buttonCtr = ui:GetController("button")
  uis.FlagCtr = ui:GetController("Flag")
```

---

## other/Story_FangYuBtnByName.lua.lua
**Functions:**
- GetStory_FangYuBtnUis
**Requires:**
- Story_Card_BgAniByName
**Snippet:**
```lua
require("Story_Card_BgAniByName")

function GetStory_FangYuBtnUis(ui)
  local uis = {}
  uis.BgAni = GetStory_Card_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Story_FaShiBtnByName.lua.lua
**Functions:**
- GetStory_FaShiBtnUis
**Requires:**
- Story_Card_BgAniByName
**Snippet:**
```lua
require("Story_Card_BgAniByName")

function GetStory_FaShiBtnUis(ui)
  local uis = {}
  uis.BgAni = GetStory_Card_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Story_GongJianBtnByName.lua.lua
**Functions:**
- GetStory_GongJianBtnUis
**Requires:**
- Story_Card_BgAniByName
**Snippet:**
```lua
require("Story_Card_BgAniByName")

function GetStory_GongJianBtnUis(ui)
  local uis = {}
  uis.BgAni = GetStory_Card_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Story_GuangBtnByName.lua.lua
**Functions:**
- GetStory_GuangBtnUis
**Requires:**
- Story_Card_BgAniByName
**Snippet:**
```lua
require("Story_Card_BgAniByName")

function GetStory_GuangBtnUis(ui)
  local uis = {}
  uis.BgAni = GetStory_Card_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Story_HideWordBtnByName.lua.lua
**Functions:**
- GetStory_HideWordBtnUis
**Snippet:**
```lua
function GetStory_HideWordBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Story_HuoBtnByName.lua.lua
**Functions:**
- GetStory_HuoBtnUis
**Requires:**
- Story_Card_BgAniByName
**Snippet:**
```lua
require("Story_Card_BgAniByName")

function GetStory_HuoBtnUis(ui)
  local uis = {}
  uis.BgAni = GetStory_Card_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Story_Info1ByName.lua.lua
**Functions:**
- GetStory_Info1Uis
**Snippet:**
```lua
function GetStory_Info1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Story_Info2ByName.lua.lua
**Functions:**
- GetStory_Info2Uis
**Requires:**
- Story_LevelByName
**Snippet:**
```lua
require("Story_LevelByName")

function GetStory_Info2Uis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Level = GetStory_LevelUis(ui:GetChild("Level"))
  uis.root = ui
  return uis
end
```

---

## other/Story_Info3ByName.lua.lua
**Functions:**
- GetStory_Info3Uis
**Snippet:**
```lua
function GetStory_Info3Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Story_Info4ByName.lua.lua
**Functions:**
- GetStory_Info4Uis
**Snippet:**
```lua
function GetStory_Info4Uis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Story_ItemByName.lua.lua
**Functions:**
- GetStory_ItemUis
**Requires:**
- Story_MonsterTitleByName
- Story_ItemInfoByName
**Snippet:**
```lua
require("Story_MonsterTitleByName")
require("Story_ItemInfoByName")

function GetStory_ItemUis(ui)
  local uis = {}
  uis.MonsterTitle = GetStory_MonsterTitleUis(ui:GetChild("MonsterTitle"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.ItemInfo = GetStory_ItemInfoUis(ui:GetChild("ItemInfo"))
  uis.root = ui
  return uis
```

---

## other/Story_ItemIconByName.lua.lua
**Functions:**
- GetStory_ItemIconUis
**Requires:**
- Story_NewByName
**Snippet:**
```lua
require("Story_NewByName")

function GetStory_ItemIconUis(ui)
  local uis = {}
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.New = GetStory_NewUis(ui:GetChild("New"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.FlagCtr = ui:GetController("Flag")
```

---

## other/Story_ItemInfoByName.lua.lua
**Functions:**
- GetStory_ItemInfoUis
**Snippet:**
```lua
function GetStory_ItemInfoUis(ui)
  local uis = {}
  
  uis.InfoList = ui:GetChild("InfoList")
  uis.root = ui
  return uis
end
```

---

## other/Story_ItemInfoWordByName.lua.lua
**Functions:**
- GetStory_ItemInfoWordUis
**Snippet:**
```lua
function GetStory_ItemInfoWordUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemUseBtn = ui:GetChild("ItemUseBtn")
  uis.root = ui
  return uis
end
```

---

## other/Story_ItemUseBtnByName.lua.lua
**Functions:**
- GetStory_ItemUseBtnUis
**Snippet:**
```lua
function GetStory_ItemUseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Story_JinZhanBtnByName.lua.lua
**Functions:**
- GetStory_JinZhanBtnUis
**Requires:**
- Story_Card_BgAniByName
**Snippet:**
```lua
require("Story_Card_BgAniByName")

function GetStory_JinZhanBtnUis(ui)
  local uis = {}
  uis.BgAni = GetStory_Card_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Story_LevelByName.lua.lua
**Functions:**
- GetStory_LevelUis
**Snippet:**
```lua
function GetStory_LevelUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Story_ListBtnByName.lua.lua
**Functions:**
- GetStory_ListBtnUis
**Snippet:**
```lua
function GetStory_ListBtnUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Story_MainPlotPicByName.lua.lua
**Functions:**
- GetStory_MainPlotPicUis
**Snippet:**
```lua
function GetStory_MainPlotPicUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.PicHolder = ui:GetChild("PicHolder")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Story_MainPlotReviewByName.lua.lua
**Functions:**
- GetStory_MainPlotReviewUis
**Requires:**
- Story_MainPlotPicByName
- Story_Tab1RegionByName
- Story_SegmentRegionByName
**Snippet:**
```lua
require("Story_MainPlotPicByName")
require("Story_Tab1RegionByName")
require("Story_SegmentRegionByName")

function GetStory_MainPlotReviewUis(ui)
  local uis = {}
  uis.MainPlotPic = GetStory_MainPlotPicUis(ui:GetChild("MainPlotPic"))
  uis.Tab1Region = GetStory_Tab1RegionUis(ui:GetChild("Tab1Region"))
  uis.SegmentRegion = GetStory_SegmentRegionUis(ui:GetChild("SegmentRegion"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## other/Story_MonsterByName.lua.lua
**Functions:**
- GetStory_MonsterUis
**Requires:**
- Story_MonsterInfoByName
- CommonResource_ListRedDotByName
- CommonResource_ListRedDot1ByName
**Snippet:**
```lua
require("Story_MonsterInfoByName")
require("CommonResource_ListRedDotByName")
require("CommonResource_ListRedDot1ByName")

function GetStory_MonsterUis(ui)
  local uis = {}
  uis.MonsterList = ui:GetChild("MonsterList")
  uis.MonsterInfo = GetStory_MonsterInfoUis(ui:GetChild("MonsterInfo"))
  uis.ListRedDot = GetCommonResource_ListRedDotUis(ui:GetChild("ListRedDot"))
  uis.ListRedDot1 = GetCommonResource_ListRedDot1Uis(ui:GetChild("ListRedDot1"))
```

---

## other/Story_MonsterHeadBgByName.lua.lua
**Functions:**
- GetStory_MonsterHeadBgUis
**Snippet:**
```lua
function GetStory_MonsterHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## other/Story_MonsterHeadBtnByName.lua.lua
**Functions:**
- GetStory_MonsterHeadBtnUis
**Requires:**
- Story_MonsterHeadBgByName
- Story_NewByName
**Snippet:**
```lua
require("Story_MonsterHeadBgByName")
require("Story_NewByName")

function GetStory_MonsterHeadBtnUis(ui)
  local uis = {}
  uis.MonsterHeadBg = GetStory_MonsterHeadBgUis(ui:GetChild("MonsterHeadBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.New = GetStory_NewUis(ui:GetChild("New"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
```

---

## other/Story_MonsterInfoByName.lua.lua
**Functions:**
- GetStory_MonsterInfoUis
**Requires:**
- Story_Tab2RegionByName
- Story_MonsterTitleByName
- Story_MonsterInfoWordByName
**Snippet:**
```lua
require("Story_Tab2RegionByName")
require("Story_MonsterTitleByName")
require("Story_MonsterInfoWordByName")

function GetStory_MonsterInfoUis(ui)
  local uis = {}
  uis.Tab2Region = GetStory_Tab2RegionUis(ui:GetChild("Tab2Region"))
  uis.MonsterTitle = GetStory_MonsterTitleUis(ui:GetChild("MonsterTitle"))
  uis.HeadList = ui:GetChild("HeadList")
  uis.MonsterInfoWord = GetStory_MonsterInfoWordUis(ui:GetChild("MonsterInfoWord"))
```

---

## other/Story_MonsterInfoWordByName.lua.lua
**Functions:**
- GetStory_MonsterInfoWordUis
**Snippet:**
```lua
function GetStory_MonsterInfoWordUis(ui)
  local uis = {}
  
  uis.InfoList = ui:GetChild("InfoList")
  uis.root = ui
  return uis
end
```

---

## other/Story_MonsterTitleByName.lua.lua
**Functions:**
- GetStory_MonsterTitleUis
**Snippet:**
```lua
function GetStory_MonsterTitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Story_MonsterTypeBtnByName.lua.lua
**Functions:**
- GetStory_MonsterTypeBtnUis
**Requires:**
- Story_NewByName
**Snippet:**
```lua
require("Story_NewByName")

function GetStory_MonsterTypeBtnUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.New = GetStory_NewUis(ui:GetChild("New"))
  uis.buttonCtr = ui:GetController("button")
```

---

## other/Story_MuBtnByName.lua.lua
**Functions:**
- GetStory_MuBtnUis
**Requires:**
- Story_Card_BgAniByName
**Snippet:**
```lua
require("Story_Card_BgAniByName")

function GetStory_MuBtnUis(ui)
  local uis = {}
  uis.BgAni = GetStory_Card_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Story_MusicByName.lua.lua
**Functions:**
- GetStory_MusicUis
**Requires:**
- Story_SongNameRegionByName
- CommonResource_ListRedDotByName
- CommonResource_ListRedDot1ByName
**Snippet:**
```lua
require("Story_SongNameRegionByName")
require("CommonResource_ListRedDotByName")
require("CommonResource_ListRedDot1ByName")

function GetStory_MusicUis(ui)
  local uis = {}
  uis.CoverList = ui:GetChild("CoverList")
  uis.SongNameRegion = GetStory_SongNameRegionUis(ui:GetChild("SongNameRegion"))
  uis.CoverBtn = ui:GetChild("CoverBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## other/Story_MusicPlayByName.lua.lua
**Functions:**
- GetStory_MusicPlayUis
**Requires:**
- CommonResource_BackGroundByName
- Story_SongInfoByName
- Story_SongRegionAniByName
- Story_SongStartByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Story_SongInfoByName")
require("Story_SongRegionAniByName")
require("Story_SongStartByName")

function GetStory_MusicPlayUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.SongInfo = GetStory_SongInfoUis(ui:GetChild("SongInfo"))
  uis.SongRegionAni = GetStory_SongRegionAniUis(ui:GetChild("SongRegionAni"))
```

---

## other/Story_MusicPlayWindowByName.lua.lua
**Functions:**
- GetStory_MusicPlayWindowUis
**Requires:**
- Story_MusicPlayByName
**Snippet:**
```lua
require("Story_MusicPlayByName")

function GetStory_MusicPlayWindowUis(ui)
  local uis = {}
  uis.Main = GetStory_MusicPlayUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/Story_NewByName.lua.lua
**Functions:**
- GetStory_NewUis
**Snippet:**
```lua
function GetStory_NewUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## other/Story_PlayBtnByName.lua.lua
**Functions:**
- GetStory_PlayBtnUis
**Snippet:**
```lua
function GetStory_PlayBtnUis(ui)
  local uis = {}
  
  uis.EffectLoader = ui:GetChild("EffectLoader")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Story_ReturnBtnByName.lua.lua
**Functions:**
- GetStory_ReturnBtnUis
**Snippet:**
```lua
function GetStory_ReturnBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Story_RhythmAniByName.lua.lua
**Functions:**
- GetStory_RhythmAniUis
**Snippet:**
```lua
function GetStory_RhythmAniUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## other/Story_SegmentBtnByName.lua.lua
**Functions:**
- GetStory_SegmentBtnUis
**Snippet:**
```lua
function GetStory_SegmentBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Story_SegmentRegionByName.lua.lua
**Functions:**
- GetStory_SegmentRegionUis
**Snippet:**
```lua
function GetStory_SegmentRegionUis(ui)
  local uis = {}
  
  uis.SegmentList = ui:GetChild("SegmentList")
  uis.root = ui
  return uis
end
```

---

## other/Story_ShuiBtnByName.lua.lua
**Functions:**
- GetStory_ShuiBtnUis
**Requires:**
- Story_Card_BgAniByName
**Snippet:**
```lua
require("Story_Card_BgAniByName")

function GetStory_ShuiBtnUis(ui)
  local uis = {}
  uis.BgAni = GetStory_Card_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Story_SongAniByName.lua.lua
**Functions:**
- GetStory_SongAniUis
**Snippet:**
```lua
function GetStory_SongAniUis(ui)
  local uis = {}
  
  uis.SongBtn = ui:GetChild("SongBtn")
  uis.root = ui
  return uis
end
```

---

## other/Story_SongBtnByName.lua.lua
**Functions:**
- GetStory_SongBtnUis
**Requires:**
- Story_RhythmAniByName
**Snippet:**
```lua
require("Story_RhythmAniByName")

function GetStory_SongBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.RhythmAni = GetStory_RhythmAniUis(ui:GetChild("RhythmAni"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## other/Story_SongInfoByName.lua.lua
**Functions:**
- GetStory_SongInfoUis
**Snippet:**
```lua
function GetStory_SongInfoUis(ui)
  local uis = {}
  
  uis.PlayBtn = ui:GetChild("PlayBtn")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.AuthorInfo1List = ui:GetChild("AuthorInfo1List")
  uis.AuthorInfo2List = ui:GetChild("AuthorInfo2List")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.LyricTxt = ui:GetChild("LyricTxt")
  uis.root = ui
```

---

## other/Story_SongNameAniByName.lua.lua
**Functions:**
- GetStory_SongNameAniUis
**Snippet:**
```lua
function GetStory_SongNameAniUis(ui)
  local uis = {}
  
  uis.SongNameBtn = ui:GetChild("SongNameBtn")
  uis.root = ui
  return uis
end
```

---

## other/Story_SongNameBtnByName.lua.lua
**Functions:**
- GetStory_SongNameBtnUis
**Requires:**
- Story_NewByName
**Snippet:**
```lua
require("Story_NewByName")

function GetStory_SongNameBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.New = GetStory_NewUis(ui:GetChild("New"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.FlagCtr = ui:GetController("Flag")
  uis.root = ui
```

---

## other/Story_SongNameRegionByName.lua.lua
**Functions:**
- GetStory_SongNameRegionUis
**Snippet:**
```lua
function GetStory_SongNameRegionUis(ui)
  local uis = {}
  
  uis.SongNameList = ui:GetChild("SongNameList")
  uis.root = ui
  return uis
end
```

---

## other/Story_SongRegionAniByName.lua.lua
**Functions:**
- GetStory_SongRegionAniUis
**Requires:**
- Story_SongRegionByName
**Snippet:**
```lua
require("Story_SongRegionByName")

function GetStory_SongRegionAniUis(ui)
  local uis = {}
  uis.SongRegion = GetStory_SongRegionUis(ui:GetChild("SongRegion"))
  uis.root = ui
  return uis
end
```

---

## other/Story_SongRegionByName.lua.lua
**Functions:**
- GetStory_SongRegionUis
**Snippet:**
```lua
function GetStory_SongRegionUis(ui)
  local uis = {}
  
  uis.SongList = ui:GetChild("SongList")
  uis.root = ui
  return uis
end
```

---

## other/Story_SongStartByName.lua.lua
**Functions:**
- GetStory_SongStartUis
**Snippet:**
```lua
function GetStory_SongStartUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Story_StoryByName.lua.lua
**Functions:**
- GetStory_StoryUis
**Requires:**
- CommonResource_BackGroundByName
- Story_MainPlotReviewByName
- Story_CGByName
- Story_MusicByName
- Story_MonsterByName
- Story_ItemByName
- Story_CardByName
- Story_TabRegionByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Story_MainPlotReviewByName")
require("Story_CGByName")
require("Story_MusicByName")
require("Story_MonsterByName")
require("Story_ItemByName")
require("Story_CardByName")
require("Story_TabRegionByName")
require("CommonResource_CurrencyReturnByName")

```

---

## other/Story_StoryWindowByName.lua.lua
**Functions:**
- GetStory_StoryWindowUis
**Requires:**
- Story_StoryByName
**Snippet:**
```lua
require("Story_StoryByName")

function GetStory_StoryWindowUis(ui)
  local uis = {}
  uis.Main = GetStory_StoryUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/Story_Tab1BtnByName.lua.lua
**Functions:**
- GetStory_Tab1BtnUis
**Snippet:**
```lua
function GetStory_Tab1BtnUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Story_Tab1RegionByName.lua.lua
**Functions:**
- GetStory_Tab1RegionUis
**Snippet:**
```lua
function GetStory_Tab1RegionUis(ui)
  local uis = {}
  
  uis.TabBtnList = ui:GetChild("TabBtnList")
  uis.root = ui
  return uis
end
```

---

## other/Story_Tab2BtnByName.lua.lua
**Functions:**
- GetStory_Tab2BtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetStory_Tab2BtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## other/Story_Tab2RegionByName.lua.lua
**Functions:**
- GetStory_Tab2RegionUis
**Snippet:**
```lua
function GetStory_Tab2RegionUis(ui)
  local uis = {}
  
  uis.TabBtnList = ui:GetChild("TabBtnList")
  uis.root = ui
  return uis
end
```

---

## other/Story_TabBtnByName.lua.lua
**Functions:**
- GetStory_TabBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetStory_TabBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## other/Story_TabRegionByName.lua.lua
**Functions:**
- GetStory_TabRegionUis
**Snippet:**
```lua
function GetStory_TabRegionUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## other/Story_TuXiBtnByName.lua.lua
**Functions:**
- GetStory_TuXiBtnUis
**Requires:**
- Story_Card_BgAniByName
**Snippet:**
```lua
require("Story_Card_BgAniByName")

function GetStory_TuXiBtnUis(ui)
  local uis = {}
  uis.BgAni = GetStory_Card_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/StringUtil.lua.lua
**Functions:**
- StringUtil.enc
- StringUtil.dec
**Snippet:**
```lua
local StringUtil = {}
local b = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/"
local string_gsub = string.gsub
local string_char = string.char
local table_concat = table.concat

function StringUtil.enc(data)
  return (data:gsub(".", function(x)
    local r, b = "", x:byte()
    for i = 8, 1, -1 do
```

---

## other/SuperDungeon_BuffNumberLockByName.lua.lua
**Functions:**
- GetSuperDungeon_BuffNumberLockUis
**Snippet:**
```lua
function GetSuperDungeon_BuffNumberLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_LockByName.lua.lua
**Functions:**
- GetSuperDungeon_LockUis
**Requires:**
- SuperDungeon_TimeLockByName
- SuperDungeon_BuffNumberLockByName
**Snippet:**
```lua
require("SuperDungeon_TimeLockByName")
require("SuperDungeon_BuffNumberLockByName")

function GetSuperDungeon_LockUis(ui)
  local uis = {}
  uis.TimeLock = GetSuperDungeon_TimeLockUis(ui:GetChild("TimeLock"))
  uis.BuffNumberLock = GetSuperDungeon_BuffNumberLockUis(ui:GetChild("BuffNumberLock"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## other/SuperDungeon_MapBossDotByName.lua.lua
**Functions:**
- GetSuperDungeon_MapBossDotUis
**Requires:**
- SuperDungeon_LockByName
**Snippet:**
```lua
require("SuperDungeon_LockByName")

function GetSuperDungeon_MapBossDotUis(ui)
  local uis = {}
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.StarList = ui:GetChild("StarList")
  uis.Lock1 = GetSuperDungeon_LockUis(ui:GetChild("Lock1"))
  uis.Lock2 = GetSuperDungeon_LockUis(ui:GetChild("Lock2"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## other/SuperDungeon_MapDotBuffNumberByName.lua.lua
**Functions:**
- GetSuperDungeon_MapDotBuffNumberUis
**Snippet:**
```lua
function GetSuperDungeon_MapDotBuffNumberUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_MapDotByName.lua.lua
**Functions:**
- GetSuperDungeon_MapDotUis
**Requires:**
- SuperDungeon_LockByName
- SuperDungeon_MapDotBuffNumberByName
**Snippet:**
```lua
require("SuperDungeon_LockByName")
require("SuperDungeon_MapDotBuffNumberByName")

function GetSuperDungeon_MapDotUis(ui)
  local uis = {}
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.StarList = ui:GetChild("StarList")
  uis.Lock = GetSuperDungeon_LockUis(ui:GetChild("Lock"))
  uis.BuffNumber = GetSuperDungeon_MapDotBuffNumberUis(ui:GetChild("BuffNumber"))
```

---

## other/SuperDungeon_PlayBossBuffByName.lua.lua
**Functions:**
- GetSuperDungeon_PlayBossBuffUis
**Snippet:**
```lua
function GetSuperDungeon_PlayBossBuffUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.BuffList = ui:GetChild("BuffList")
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_PlayBossBuffContentBtnByName.lua.lua
**Functions:**
- GetSuperDungeon_PlayBossBuffContentBtnUis
**Snippet:**
```lua
function GetSuperDungeon_PlayBossBuffContentBtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_PlayBossBuffContentByName.lua.lua
**Functions:**
- GetSuperDungeon_PlayBossBuffContentUis
**Snippet:**
```lua
function GetSuperDungeon_PlayBossBuffContentUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordList = ui:GetChild("WordList")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_PlayBuffByName.lua.lua
**Functions:**
- GetSuperDungeon_PlayBuffUis
**Snippet:**
```lua
function GetSuperDungeon_PlayBuffUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.BuffList = ui:GetChild("BuffList")
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_PlayBuffContent1ByName.lua.lua
**Functions:**
- GetSuperDungeon_PlayBuffContent1Uis
**Snippet:**
```lua
function GetSuperDungeon_PlayBuffContent1Uis(ui)
  local uis = {}
  
  uis.BuffNameTxt = ui:GetChild("BuffNameTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_PlayBuffContent1WordByName.lua.lua
**Functions:**
- GetSuperDungeon_PlayBuffContent1WordUis
**Snippet:**
```lua
function GetSuperDungeon_PlayBuffContent1WordUis(ui)
  local uis = {}
  
  uis.BuffWordTxt = ui:GetChild("BuffWordTxt")
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_PlayBuffContent2ByName.lua.lua
**Functions:**
- GetSuperDungeon_PlayBuffContent2Uis
**Snippet:**
```lua
function GetSuperDungeon_PlayBuffContent2Uis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.BuffNameTxt = ui:GetChild("BuffNameTxt")
  uis.BuffWordTxt = ui:GetChild("BuffWordTxt")
  uis.PicBuffLoader = ui:GetChild("PicBuffLoader")
  uis.BuffNumberTxt = ui:GetChild("BuffNumberTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.root = ui
```

---

## other/SuperDungeon_PlayBuffContent2WordByName.lua.lua
**Functions:**
- GetSuperDungeon_PlayBuffContent2WordUis
**Snippet:**
```lua
function GetSuperDungeon_PlayBuffContent2WordUis(ui)
  local uis = {}
  
  uis.BuffWordTxt = ui:GetChild("BuffWordTxt")
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_PlayBuffContentByName.lua.lua
**Functions:**
- GetSuperDungeon_PlayBuffContentUis
**Snippet:**
```lua
function GetSuperDungeon_PlayBuffContentUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.BuffNameTxt = ui:GetChild("BuffNameTxt")
  uis.BuffNumberTxt = ui:GetChild("BuffNumberTxt")
  uis.BuffWordTxt = ui:GetChild("BuffWordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## other/SuperDungeon_PlayCloseBtnByName.lua.lua
**Functions:**
- GetSuperDungeon_PlayCloseBtnUis
**Snippet:**
```lua
function GetSuperDungeon_PlayCloseBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_PlayDetailsByName.lua.lua
**Functions:**
- GetSuperDungeon_PlayDetailsUis
**Requires:**
- CommonResource_PopupBgByName
- SuperDungeon_PlayTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("SuperDungeon_PlayTipsByName")

function GetSuperDungeon_PlayDetailsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.PlayTips = GetSuperDungeon_PlayTipsUis(ui:GetChild("PlayTips"))
  uis.root = ui
  return uis
```

---

## other/SuperDungeon_PlayDetailsWindowByName.lua.lua
**Functions:**
- GetSuperDungeon_PlayDetailsWindowUis
**Requires:**
- SuperDungeon_PlayDetailsByName
**Snippet:**
```lua
require("SuperDungeon_PlayDetailsByName")

function GetSuperDungeon_PlayDetailsWindowUis(ui)
  local uis = {}
  uis.Main = GetSuperDungeon_PlayDetailsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_PlayStartBtnByName.lua.lua
**Functions:**
- GetSuperDungeon_PlayStartBtnUis
**Snippet:**
```lua
function GetSuperDungeon_PlayStartBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_PlaySuggest1ByName.lua.lua
**Functions:**
- GetSuperDungeon_PlaySuggest1Uis
**Snippet:**
```lua
function GetSuperDungeon_PlaySuggest1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.BuffList = ui:GetChild("BuffList")
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_PlaySuggest1_WordByName.lua.lua
**Functions:**
- GetSuperDungeon_PlaySuggest1_WordUis
**Snippet:**
```lua
function GetSuperDungeon_PlaySuggest1_WordUis(ui)
  local uis = {}
  
  uis.BuffWordTxt = ui:GetChild("BuffWordTxt")
  uis.PicBuffLoader = ui:GetChild("PicBuffLoader")
  uis.BuffNumberTxt = ui:GetChild("BuffNumberTxt")
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_PlaySuggest2ByName.lua.lua
**Functions:**
- GetSuperDungeon_PlaySuggest2Uis
**Snippet:**
```lua
function GetSuperDungeon_PlaySuggest2Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.CardList = ui:GetChild("CardList")
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_PlaySuggest2_CardBgByName.lua.lua
**Functions:**
- GetSuperDungeon_PlaySuggest2_CardBgUis
**Snippet:**
```lua
function GetSuperDungeon_PlaySuggest2_CardBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_PlaySuggest2_CardByName.lua.lua
**Functions:**
- GetSuperDungeon_PlaySuggest2_CardUis
**Requires:**
- SuperDungeon_PlaySuggest2_CardBgByName
**Snippet:**
```lua
require("SuperDungeon_PlaySuggest2_CardBgByName")

function GetSuperDungeon_PlaySuggest2_CardUis(ui)
  local uis = {}
  uis.n2 = GetSuperDungeon_PlaySuggest2_CardBgUis(ui:GetChild("n2"))
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_PlayTargetByName.lua.lua
**Functions:**
- GetSuperDungeon_PlayTargetUis
**Snippet:**
```lua
function GetSuperDungeon_PlayTargetUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.ContentList = ui:GetChild("ContentList")
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_PlayTargetContentByName.lua.lua
**Functions:**
- GetSuperDungeon_PlayTargetContentUis
**Snippet:**
```lua
function GetSuperDungeon_PlayTargetContentUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_PlayTipsByName.lua.lua
**Functions:**
- GetSuperDungeon_PlayTipsUis
**Requires:**
- SuperDungeon_PlayTitleByName
- SuperDungeon_PlayTargetByName
- SuperDungeon_PlayBuffByName
- SuperDungeon_PlayBossBuffByName
- SuperDungeon_PlaySuggest1ByName
- SuperDungeon_PlaySuggest2ByName
**Snippet:**
```lua
require("SuperDungeon_PlayTitleByName")
require("SuperDungeon_PlayTargetByName")
require("SuperDungeon_PlayBuffByName")
require("SuperDungeon_PlayBossBuffByName")
require("SuperDungeon_PlaySuggest1ByName")
require("SuperDungeon_PlaySuggest2ByName")

function GetSuperDungeon_PlayTipsUis(ui)
  local uis = {}
  uis.Title = GetSuperDungeon_PlayTitleUis(ui:GetChild("Title"))
```

---

## other/SuperDungeon_PlayTitleByName.lua.lua
**Functions:**
- GetSuperDungeon_PlayTitleUis
**Snippet:**
```lua
function GetSuperDungeon_PlayTitleUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_RewardBtnByName.lua.lua
**Functions:**
- GetSuperDungeon_RewardBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetSuperDungeon_RewardBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_RewardGetByName.lua.lua
**Functions:**
- GetSuperDungeon_RewardGetUis
**Requires:**
- CommonResource_BackGroundByName
- SuperDungeon_RewardSpecialItemByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("SuperDungeon_RewardSpecialItemByName")
require("CommonResource_CurrencyReturnByName")

function GetSuperDungeon_RewardGetUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TabList = ui:GetChild("TabList")
  uis.ItemList = ui:GetChild("ItemList")
  uis.SpecialItem = GetSuperDungeon_RewardSpecialItemUis(ui:GetChild("SpecialItem"))
```

---

## other/SuperDungeon_RewardGetWindowByName.lua.lua
**Functions:**
- GetSuperDungeon_RewardGetWindowUis
**Requires:**
- SuperDungeon_RewardGetByName
**Snippet:**
```lua
require("SuperDungeon_RewardGetByName")

function GetSuperDungeon_RewardGetWindowUis(ui)
  local uis = {}
  uis.Main = GetSuperDungeon_RewardGetUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_RewardItem1ByName.lua.lua
**Functions:**
- GetSuperDungeon_RewardItem1Uis
**Snippet:**
```lua
function GetSuperDungeon_RewardItem1Uis(ui)
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

## other/SuperDungeon_RewardItemAniByName.lua.lua
**Functions:**
- GetSuperDungeon_RewardItemAniUis
**Requires:**
- SuperDungeon_RewardItemByName
**Snippet:**
```lua
require("SuperDungeon_RewardItemByName")

function GetSuperDungeon_RewardItemAniUis(ui)
  local uis = {}
  uis.RewardItem = GetSuperDungeon_RewardItemUis(ui:GetChild("RewardItem"))
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_RewardItemByName.lua.lua
**Functions:**
- GetSuperDungeon_RewardItemUis
**Requires:**
- SuperDungeon_RewardItemProgressByName
**Snippet:**
```lua
require("SuperDungeon_RewardItemProgressByName")

function GetSuperDungeon_RewardItemUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.ItemList = ui:GetChild("ItemList")
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.Progress = GetSuperDungeon_RewardItemProgressUis(ui:GetChild("Progress"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## other/SuperDungeon_RewardItemGetBtnByName.lua.lua
**Functions:**
- GetSuperDungeon_RewardItemGetBtnUis
**Snippet:**
```lua
function GetSuperDungeon_RewardItemGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_RewardItemProgressByName.lua.lua
**Functions:**
- GetSuperDungeon_RewardItemProgressUis
**Snippet:**
```lua
function GetSuperDungeon_RewardItemProgressUis(ui)
  local uis = {}
  
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_RewardSpecialItemByName.lua.lua
**Functions:**
- GetSuperDungeon_RewardSpecialItemUis
**Snippet:**
```lua
function GetSuperDungeon_RewardSpecialItemUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.ItemList = ui:GetChild("ItemList")
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## other/SuperDungeon_RewardSpecialItemGetBtnByName.lua.lua
**Functions:**
- GetSuperDungeon_RewardSpecialItemGetBtnUis
**Snippet:**
```lua
function GetSuperDungeon_RewardSpecialItemGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_RewardTabBtnByName.lua.lua
**Functions:**
- GetSuperDungeon_RewardTabBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetSuperDungeon_RewardTabBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## other/SuperDungeon_RewardTitleByName.lua.lua
**Functions:**
- GetSuperDungeon_RewardTitleUis
**Snippet:**
```lua
function GetSuperDungeon_RewardTitleUis(ui)
  local uis = {}
  
  uis.OrderTxt = ui:GetChild("OrderTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_StarByName.lua.lua
**Functions:**
- GetSuperDungeon_StarUis
**Snippet:**
```lua
function GetSuperDungeon_StarUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_SuperByName.lua.lua
**Functions:**
- GetSuperDungeon_SuperUis
**Requires:**
- CommonResource_BackGroundByName
- SuperDungeon_TitleByName
- SuperDungeon_MapDotByName
- SuperDungeon_MapBossDotByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("SuperDungeon_TitleByName")
require("SuperDungeon_MapDotByName")
require("SuperDungeon_MapBossDotByName")
require("CommonResource_CurrencyReturnByName")

function GetSuperDungeon_SuperUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
```

---

## other/SuperDungeon_SuperWindowByName.lua.lua
**Functions:**
- GetSuperDungeon_SuperWindowUis
**Requires:**
- SuperDungeon_SuperByName
**Snippet:**
```lua
require("SuperDungeon_SuperByName")

function GetSuperDungeon_SuperWindowUis(ui)
  local uis = {}
  uis.Main = GetSuperDungeon_SuperUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_TimeLockByName.lua.lua
**Functions:**
- GetSuperDungeon_TimeLockUis
**Snippet:**
```lua
function GetSuperDungeon_TimeLockUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## other/SuperDungeon_TitleByName.lua.lua
**Functions:**
- GetSuperDungeon_TitleUis
**Snippet:**
```lua
function GetSuperDungeon_TitleUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## other/SweepData.lua.lua
**Functions:**
- SweepData.InitSweepTarget
- SweepData.InitSweepRecord
- SweepData.GetFromCardId
- SweepData.GetItemId
- SweepData.GetItemGotCount
- SweepData.GetTargetItemCount
- SweepData.UpdateItemGotCount
- SweepData.GetSweepResult
- SweepData.ClearData
- SweepData.ClearSweepTarget
- SweepData.ClearSweepRecord
**Snippet:**
```lua
SweepData = {}

function SweepData.InitSweepTarget(data)
  SweepData.sweepTarget = data
end

function SweepData.InitSweepRecord(data)
  SweepData.sweepRecord = data
end

```

---

## other/SweepScriptList.lua.lua
**Requires:**
- SweepData
- SweepService
**Snippet:**
```lua
local require = require
require("SweepData")
require("SweepService")
```

---

## other/SweepService.lua.lua
**Functions:**
- SweepService.Init
- SweepService.SweepStageReq
- SweepService.SweepStageRsp
**Snippet:**
```lua
SweepService = {}

function SweepService.Init()
  Net.AddListener(Proto.MsgName.SweepStageRsp, SweepService.SweepStageRsp)
end

function SweepService.SweepStageReq(stageId, rspCallBack)
  local msg = {}
  msg.stageId = stageId
  Net.Send(Proto.MsgName.SweepStageReq, msg, rspCallBack)
```

---

## other/SweepWindow.lua.lua
**Functions:**
- SweepWindow.ReInitData
- SweepWindow.OnInit
- SweepWindow.UpdateInfo
- SweepWindow.UpdateStageInfo
- SweepWindow.UpdateReason
- SweepWindow.UpdateFallInfo
- SweepWindow.UpdateSweepResult
- itemList.itemRenderer
- SweepWindow.UpdateSweepBtn
- SweepWindow.ClickSweepBtn
- SweepWindow.UpdateTips
- SweepWindow.SetSweepState
- SweepWindow.StartSweep
- SweepWindow.EachSweepComplete
- SweepWindow.SendSweepStage
- SweepWindow.Sort
- SweepWindow.StopSweep
- SweepWindow.GetMultipleType
- SweepWindow.UpdateMultiDropInfo
- list.itemRenderer
- SweepWindow.UpdateMultiple
- SweepWindow.InitBtn
- SweepWindow.TouchClose
- SweepWindow.OnShowAnimationEnd
- SweepWindow.OnClose
- SweepWindow.HandleMessage
**Requires:**
- Message_SweepWindowByName
**Snippet:**
```lua
require("Message_SweepWindowByName")
local SweepWindow = {}
local uis, contentPane

function SweepWindow.ReInitData()
end

local stageId, stageConfig, stageCost, canClose
local isSweeping = false
local stopWhenItemEnough = false
```

---

## other/TableData.lua.lua
**Functions:**
- TableData.ClearCache
- TableData.ClearAllCache
- TableData.GetTable
- TableData.GetConfig
- TableData.GetConfigByType
- TableData.GetTupleTypeById
**Snippet:**
```lua
local TableData = {delayClear = false}
local require = require
local package = package
local globalTableCache = {}

function TableData.ClearCache(tableName)
  _G[tableName] = nil
  package.loaded[tableName] = nil
  globalTableCache[tableName] = nil
end
```

---

## other/TaskDetailsWindow.lua.lua
**Functions:**
- TaskDetailsWindow.ReInitData
- TaskDetailsWindow.OnInit
- TaskDetailsWindow.UpdateInfo
- tips.ItemList.itemRenderer
- TaskDetailsWindow.CloseWindow
- TaskDetailsWindow.InitBtn
- TaskDetailsWindow.OnClose
**Requires:**
- InitialCarnival_TaskDetailsWindowByName
**Snippet:**
```lua
require("InitialCarnival_TaskDetailsWindowByName")
local TaskDetailsWindow = {}
local uis, contentPane, arg, taskData

function TaskDetailsWindow.ReInitData()
end

function TaskDetailsWindow.OnInit(bridgeObj)
  bridgeObj:SetView(WinResConfig.TaskDetailsWindow.package, WinResConfig.TaskDetailsWindow.comName, function(com)
    contentPane = com
```

---

## other/TeamCardChoice_AttributeByName.lua.lua
**Functions:**
- GetTeamCardChoice_AttributeUis
**Snippet:**
```lua
function GetTeamCardChoice_AttributeUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/TeamCardChoice_CancelBtnByName.lua.lua
**Functions:**
- GetTeamCardChoice_CancelBtnUis
**Snippet:**
```lua
function GetTeamCardChoice_CancelBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/TeamCardChoice_CardPicByName.lua.lua
**Functions:**
- GetTeamCardChoice_CardPicUis
**Snippet:**
```lua
function GetTeamCardChoice_CardPicUis(ui)
  local uis = {}
  
  uis.CardPicLoader = ui:GetChild("CardPicLoader")
  uis.root = ui
  return uis
end
```

---

## other/TeamCardChoice_CardTipsByName.lua.lua
**Functions:**
- GetTeamCardChoice_CardTipsUis
**Requires:**
- TeamCardChoice_Quality1_1ByName
- TeamCardChoice_CardPicByName
- TeamCardChoice_Quality1_2ByName
- CommonResource_OccupationByName
- CommonResource_CardBreachByName
**Snippet:**
```lua
require("TeamCardChoice_Quality1_1ByName")
require("TeamCardChoice_CardPicByName")
require("TeamCardChoice_Quality1_2ByName")
require("CommonResource_OccupationByName")
require("CommonResource_CardBreachByName")

function GetTeamCardChoice_CardTipsUis(ui)
  local uis = {}
  uis.Quality1_1 = GetTeamCardChoice_Quality1_1Uis(ui:GetChild("Quality1_1"))
  uis.CardPic = GetTeamCardChoice_CardPicUis(ui:GetChild("CardPic"))
```

---

## other/TeamCardChoice_Delete1BtnByName.lua.lua
**Functions:**
- GetTeamCardChoice_Delete1BtnUis
**Snippet:**
```lua
function GetTeamCardChoice_Delete1BtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/TeamCardChoice_EditTeamByName.lua.lua
**Functions:**
- GetTeamCardChoice_EditTeamUis
**Requires:**
- CommonResource_BackGroundByName
- TeamCardChoice_InfoByName
- TeamCardChoice_NumberByName
- TeamCardChoice_OccupationRegionByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("TeamCardChoice_InfoByName")
require("TeamCardChoice_NumberByName")
require("TeamCardChoice_OccupationRegionByName")
require("CommonResource_CurrencyReturnByName")

function GetTeamCardChoice_EditTeamUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Info = GetTeamCardChoice_InfoUis(ui:GetChild("Info"))
```

---

## other/TeamCardChoice_EditTeamWindowByName.lua.lua
**Functions:**
- GetTeamCardChoice_EditTeamWindowUis
**Requires:**
- TeamCardChoice_EditTeamByName
**Snippet:**
```lua
require("TeamCardChoice_EditTeamByName")

function GetTeamCardChoice_EditTeamWindowUis(ui)
  local uis = {}
  uis.Main = GetTeamCardChoice_EditTeamUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/TeamCardChoice_EditTipsBtnAniByName.lua.lua
**Functions:**
- GetTeamCardChoice_EditTipsBtnAniUis
**Snippet:**
```lua
function GetTeamCardChoice_EditTipsBtnAniUis(ui)
  local uis = {}
  
  uis.EditTipsBtn = ui:GetChild("EditTipsBtn")
  uis.root = ui
  return uis
end
```

---

## other/TeamCardChoice_EditTipsBtnByName.lua.lua
**Functions:**
- GetTeamCardChoice_EditTipsBtnUis
**Requires:**
- TeamCardChoice_CardTipsByName
**Snippet:**
```lua
require("TeamCardChoice_CardTipsByName")

function GetTeamCardChoice_EditTipsBtnUis(ui)
  local uis = {}
  uis.CardTips = GetTeamCardChoice_CardTipsUis(ui:GetChild("CardTips"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## other/TeamCardChoice_Info1ByName.lua.lua
**Functions:**
- GetTeamCardChoice_Info1Uis
**Requires:**
- CommonResource_OccupationByName
- CommonResource_CardBreachByName
**Snippet:**
```lua
require("CommonResource_OccupationByName")
require("CommonResource_CardBreachByName")

function GetTeamCardChoice_Info1Uis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.StarList = ui:GetChild("StarList")
  uis.ElementList = ui:GetChild("ElementList")
  uis.Occupation = GetCommonResource_OccupationUis(ui:GetChild("Occupation"))
```

---

## other/TeamCardChoice_Info2ByName.lua.lua
**Functions:**
- GetTeamCardChoice_Info2Uis
**Snippet:**
```lua
function GetTeamCardChoice_Info2Uis(ui)
  local uis = {}
  
  uis.AttributeList = ui:GetChild("AttributeList")
  uis.TitleBtn = ui:GetChild("TitleBtn")
  uis.root = ui
  return uis
end
```

---

## other/TeamCardChoice_Info3ByName.lua.lua
**Functions:**
- GetTeamCardChoice_Info3Uis
**Snippet:**
```lua
function GetTeamCardChoice_Info3Uis(ui)
  local uis = {}
  
  uis.TitleBtn = ui:GetChild("TitleBtn")
  uis.SkillList = ui:GetChild("SkillList")
  uis.root = ui
  return uis
end
```

---

## other/TeamCardChoice_Info4ByName.lua.lua
**Functions:**
- GetTeamCardChoice_Info4Uis
**Snippet:**
```lua
function GetTeamCardChoice_Info4Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/TeamCardChoice_InfoByName.lua.lua
**Functions:**
- GetTeamCardChoice_InfoUis
**Requires:**
- TeamCardChoice_Info1ByName
- TeamCardChoice_Info2ByName
- TeamCardChoice_Info3ByName
- TeamCardChoice_Info4ByName
**Snippet:**
```lua
require("TeamCardChoice_Info1ByName")
require("TeamCardChoice_Info2ByName")
require("TeamCardChoice_Info3ByName")
require("TeamCardChoice_Info4ByName")

function GetTeamCardChoice_InfoUis(ui)
  local uis = {}
  uis.Info1 = GetTeamCardChoice_Info1Uis(ui:GetChild("Info1"))
  uis.Info2 = GetTeamCardChoice_Info2Uis(ui:GetChild("Info2"))
  uis.Info3 = GetTeamCardChoice_Info3Uis(ui:GetChild("Info3"))
```

---

## other/TeamCardChoice_NumberByName.lua.lua
**Functions:**
- GetTeamCardChoice_NumberUis
**Snippet:**
```lua
function GetTeamCardChoice_NumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## other/TeamCardChoice_OccupationBtnBgByName.lua.lua
**Functions:**
- GetTeamCardChoice_OccupationBtnBgUis
**Snippet:**
```lua
function GetTeamCardChoice_OccupationBtnBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## other/TeamCardChoice_OccupationBtnByName.lua.lua
**Functions:**
- GetTeamCardChoice_OccupationBtnUis
**Requires:**
- TeamCardChoice_OccupationBtnBgByName
**Snippet:**
```lua
require("TeamCardChoice_OccupationBtnBgByName")

function GetTeamCardChoice_OccupationBtnUis(ui)
  local uis = {}
  uis.OccupationBtnBg = GetTeamCardChoice_OccupationBtnBgUis(ui:GetChild("OccupationBtnBg"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/TeamCardChoice_OccupationRegionByName.lua.lua
**Functions:**
- GetTeamCardChoice_OccupationRegionUis
**Snippet:**
```lua
function GetTeamCardChoice_OccupationRegionUis(ui)
  local uis = {}
  
  uis.BtnList = ui:GetChild("BtnList")
  uis.root = ui
  return uis
end
```

---

## other/TeamCardChoice_Quality1_1ByName.lua.lua
**Functions:**
- GetTeamCardChoice_Quality1_1Uis
**Snippet:**
```lua
function GetTeamCardChoice_Quality1_1Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/TeamCardChoice_Quality1_2ByName.lua.lua
**Functions:**
- GetTeamCardChoice_Quality1_2Uis
**Snippet:**
```lua
function GetTeamCardChoice_Quality1_2Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/TeamCardChoice_SkillByName.lua.lua
**Functions:**
- GetTeamCardChoice_SkillUis
**Requires:**
- CommonResource_SkillByName
- TeamCardChoice_SkillCDInfoByName
- CommonResource_SkillDetailsTagByName
**Snippet:**
```lua
require("CommonResource_SkillByName")
require("TeamCardChoice_SkillCDInfoByName")
require("CommonResource_SkillDetailsTagByName")

function GetTeamCardChoice_SkillUis(ui)
  local uis = {}
  uis.BackImage = ui:GetChild("BackImage")
  uis.Skill = GetCommonResource_SkillUis(ui:GetChild("Skill"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
```

---

## other/TeamCardChoice_SkillCDInfoByName.lua.lua
**Functions:**
- GetTeamCardChoice_SkillCDInfoUis
**Snippet:**
```lua
function GetTeamCardChoice_SkillCDInfoUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/TeamCardChoice_SureBtnByName.lua.lua
**Functions:**
- GetTeamCardChoice_SureBtnUis
**Snippet:**
```lua
function GetTeamCardChoice_SureBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/TeamData.lua.lua
**Functions:**
- TeamData.GetTeamInfoById
- TeamData.IsCardInTeam
- TeamData.GetTeamCardLimitNum
- TeamData.UpdateTeamInfo
- TeamData.GetTeamNameById
- TeamData.HaveSameName
**Snippet:**
```lua
TeamData = {maxTeamIndex = 8}

function TeamData.GetTeamInfoById(teamId)
  local teamList = ActorData.GetAllTeam()
  for _, v in pairs(teamList) do
    if v.teamId == teamId then
      return v
    end
  end
end
```

---

## other/TeamDetailsWindow.lua.lua
**Functions:**
- TeamDetailsWindow.ReInitData
- TeamDetailsWindow.OnInit
- TeamDetailsWindow.InitMapPos
- TeamDetailsWindow.Show
- uis.Main.HeadList.itemRenderer
- TeamDetailsWindow.UpdateBurst
- TeamDetailsWindow.GetEmbattledCardCountSplitByType
- TeamDetailsWindow.GetListData
- TeamDetailsWindow.ShowCard
- TeamDetailsWindow.InitBtn
- TeamDetailsWindow.OnClose
- TeamDetailsWindow.HandleMessage
**Requires:**
- GuildTrain_TeamDetailsWindowByName
**Snippet:**
```lua
require("GuildTrain_TeamDetailsWindowByName")
local TeamDetailsWindow = {}
local uis, contentPane, jumpTb
local bottomGridMap = {}
local timeText, posCard, chooseEffect, stageData
local bottomGridWidth = 80
local rotation = 30

function TeamDetailsWindow.ReInitData()
end
```

---

## other/TeamEditWindow.lua.lua
**Functions:**
- TeamEditWindow.ReInitData
- TeamEditWindow.Init
- TeamEditWindow.OnInit
- TeamEditWindow.IsSameCardType
- TeamEditWindow.GetCardList
- TeamEditWindow.UpdateInfo
- TeamEditWindow.GetTeamEndCardId
- TeamEditWindow.UpdateOccupationRegion
- TeamEditWindow.UpdateTeamList
- TeamEditWindow.UpdateCardNum
- TeamEditWindow.UpdateCardDetail
- TeamEditWindow.RefreshCard
- TeamEditWindow.UpdateAllIndex
- TeamEditWindow.UpdateInTeamIndex
- TeamEditWindow.InitBtn
- TeamEditWindow.ClickDeleteBtn
- TeamEditWindow.ClickCancelBtn
- TeamEditWindow.ClickSureBtn
- TeamEditWindow.UpdateCardInfoList
- TeamEditWindow.OnShown
- TeamEditWindow.OnHide
- TeamEditWindow.OnClose
- TeamEditWindow.HandleMessage
**Requires:**
- Team_EditTeamWindowByName
**Snippet:**
```lua
require("Team_EditTeamWindowByName")
local TeamEditWindow = {}
local uis, contentPane, teamId, cardIndex, singleSelectCard
local curCardInfoList = {}
local selectCardType
local TEAM_EDIT_TYPE = {
  SINGLE = 1,
  QUICK = 2,
  ADD = 3
}
```

---

## other/TeamMgr.lua.lua
**Snippet:**
```lua
TeamMgr = {}
```

---

## other/TeamRenameWindow.lua.lua
**Functions:**
- TeamRenameWindow.ReInitData
- TeamRenameWindow.OnInit
- TeamRenameWindow.UpdateInfo
- TeamRenameWindow.ClickClose
- TeamRenameWindow.ClickSureBtn
- TeamRenameWindow.InitBtn
- TeamRenameWindow.OnShown
- TeamRenameWindow.OnHide
- TeamRenameWindow.OnClose
- TeamRenameWindow.HandleMessage
**Requires:**
- Message_RenameWindowByName
**Snippet:**
```lua
require("Message_RenameWindowByName")
local TeamRenameWindow = {}
local uis, contentPane, selectTeamId

function TeamRenameWindow.ReInitData()
end

local preTeamName

function TeamRenameWindow.OnInit(bridgeObj)
```

---

## other/TeamScriptList.lua.lua
**Requires:**
- TeamMgr
- TeamData
- TeamService
**Snippet:**
```lua
local require = require
require("TeamMgr")
require("TeamData")
require("TeamService")
```

---

## other/TeamService.lua.lua
**Functions:**
- TeamService.Init
- TeamService.SetCardTeamReq
- TeamService.DealSetCardTeamRsp
- TeamService.ChangeCardTeamNameReq
- TeamService.DealChangeCardTeamNameRsp
**Snippet:**
```lua
TeamService = {}

function TeamService.Init()
  Net.AddListener(Proto.MsgName.SetCardTeamRsp, TeamService.DealSetCardTeamRsp)
  Net.AddListener(Proto.MsgName.ChangeCardTeamNameRsp, TeamService.DealChangeCardTeamNameRsp)
end

function TeamService.SetCardTeamReq(teamId, cardIds, name)
  local msg = {}
  msg.teamId = teamId
```

---

## other/TeamWindow.lua.lua
**Functions:**
- TeamWindow.ReInitData
- TeamWindow.Init
- TeamWindow.OnInit
- TeamWindow.UpdateInfo
- TeamWindow.UpdateTeamList
- TeamWindow.UpdateTab
- TeamWindow.RefreshCard
- TeamWindow.TouchTeamCard
- TeamWindow.InitBtn
- TeamWindow.DeleteTeam
- TeamWindow.OnShown
- TeamWindow.OnHide
- TeamWindow.RefreshName
- TeamWindow.OnClose
- TeamWindow.HandleMessage
**Requires:**
- Team_TeamWindowByName
**Snippet:**
```lua
require("Team_TeamWindowByName")
local TeamWindow = {}
local uis, contentPane, curSelectTeamId, jumpTb, tapBtnList

function TeamWindow.ReInitData()
end

function TeamWindow.Init()
  if nil == curSelectTeamId then
    curSelectTeamId = 1
```

---

## other/Team_AdjustmentBtnByName.lua.lua
**Functions:**
- GetTeam_AdjustmentBtnUis
**Snippet:**
```lua
function GetTeam_AdjustmentBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Team_AttributeByName.lua.lua
**Functions:**
- GetTeam_AttributeUis
**Snippet:**
```lua
function GetTeam_AttributeUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Team_CancelBtnByName.lua.lua
**Functions:**
- GetTeam_CancelBtnUis
**Snippet:**
```lua
function GetTeam_CancelBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Team_CardPicByName.lua.lua
**Functions:**
- GetTeam_CardPicUis
**Snippet:**
```lua
function GetTeam_CardPicUis(ui)
  local uis = {}
  
  uis.CardPicLoader = ui:GetChild("CardPicLoader")
  uis.root = ui
  return uis
end
```

---

## other/Team_CardTipsByName.lua.lua
**Functions:**
- GetTeam_CardTipsUis
**Requires:**
- Team_Quality1_1ByName
- Team_CardPicByName
- Team_Quality1_2ByName
- CommonResource_OccupationByName
- CommonResource_CardBreachByName
**Snippet:**
```lua
require("Team_Quality1_1ByName")
require("Team_CardPicByName")
require("Team_Quality1_2ByName")
require("CommonResource_OccupationByName")
require("CommonResource_CardBreachByName")

function GetTeam_CardTipsUis(ui)
  local uis = {}
  uis.Quality1_1 = GetTeam_Quality1_1Uis(ui:GetChild("Quality1_1"))
  uis.CardPic = GetTeam_CardPicUis(ui:GetChild("CardPic"))
```

---

## other/Team_Delete1BtnByName.lua.lua
**Functions:**
- GetTeam_Delete1BtnUis
**Snippet:**
```lua
function GetTeam_Delete1BtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Team_DeleteBtnByName.lua.lua
**Functions:**
- GetTeam_DeleteBtnUis
**Snippet:**
```lua
function GetTeam_DeleteBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Team_EditTeamByName.lua.lua
**Functions:**
- GetTeam_EditTeamUis
**Requires:**
- CommonResource_BackGroundByName
- Team_InfoByName
- Team_NumberByName
- Team_OccupationRegionByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Team_InfoByName")
require("Team_NumberByName")
require("Team_OccupationRegionByName")
require("CommonResource_CurrencyReturnByName")

function GetTeam_EditTeamUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Info = GetTeam_InfoUis(ui:GetChild("Info"))
```

---

## other/Team_EditTeamWindowByName.lua.lua
**Functions:**
- GetTeam_EditTeamWindowUis
**Requires:**
- Team_EditTeamByName
**Snippet:**
```lua
require("Team_EditTeamByName")

function GetTeam_EditTeamWindowUis(ui)
  local uis = {}
  uis.Main = GetTeam_EditTeamUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/Team_EditTipsBtnAniByName.lua.lua
**Functions:**
- GetTeam_EditTipsBtnAniUis
**Snippet:**
```lua
function GetTeam_EditTipsBtnAniUis(ui)
  local uis = {}
  
  uis.EditTipsBtn = ui:GetChild("EditTipsBtn")
  uis.root = ui
  return uis
end
```

---

## other/Team_EditTipsBtnByName.lua.lua
**Functions:**
- GetTeam_EditTipsBtnUis
**Requires:**
- Team_CardTipsByName
**Snippet:**
```lua
require("Team_CardTipsByName")

function GetTeam_EditTipsBtnUis(ui)
  local uis = {}
  uis.CardTips = GetTeam_CardTipsUis(ui:GetChild("CardTips"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## other/Team_Info1ByName.lua.lua
**Functions:**
- GetTeam_Info1Uis
**Requires:**
- CommonResource_OccupationByName
- CommonResource_CardBreachByName
**Snippet:**
```lua
require("CommonResource_OccupationByName")
require("CommonResource_CardBreachByName")

function GetTeam_Info1Uis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.StarList = ui:GetChild("StarList")
  uis.ElementList = ui:GetChild("ElementList")
  uis.Occupation = GetCommonResource_OccupationUis(ui:GetChild("Occupation"))
```

---

## other/Team_Info2ByName.lua.lua
**Functions:**
- GetTeam_Info2Uis
**Snippet:**
```lua
function GetTeam_Info2Uis(ui)
  local uis = {}
  
  uis.AttributeList = ui:GetChild("AttributeList")
  uis.TitleBtn = ui:GetChild("TitleBtn")
  uis.root = ui
  return uis
end
```

---

## other/Team_Info3ByName.lua.lua
**Functions:**
- GetTeam_Info3Uis
**Snippet:**
```lua
function GetTeam_Info3Uis(ui)
  local uis = {}
  
  uis.TitleBtn = ui:GetChild("TitleBtn")
  uis.SkillList = ui:GetChild("SkillList")
  uis.root = ui
  return uis
end
```

---

## other/Team_Info4ByName.lua.lua
**Functions:**
- GetTeam_Info4Uis
**Snippet:**
```lua
function GetTeam_Info4Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Team_InfoByName.lua.lua
**Functions:**
- GetTeam_InfoUis
**Requires:**
- Team_Info1ByName
- Team_Info2ByName
- Team_Info3ByName
- Team_Info4ByName
**Snippet:**
```lua
require("Team_Info1ByName")
require("Team_Info2ByName")
require("Team_Info3ByName")
require("Team_Info4ByName")

function GetTeam_InfoUis(ui)
  local uis = {}
  uis.Info1 = GetTeam_Info1Uis(ui:GetChild("Info1"))
  uis.Info2 = GetTeam_Info2Uis(ui:GetChild("Info2"))
  uis.Info3 = GetTeam_Info3Uis(ui:GetChild("Info3"))
```

---

## other/Team_NumberByName.lua.lua
**Functions:**
- GetTeam_NumberUis
**Snippet:**
```lua
function GetTeam_NumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## other/Team_OccupationBtnBgByName.lua.lua
**Functions:**
- GetTeam_OccupationBtnBgUis
**Snippet:**
```lua
function GetTeam_OccupationBtnBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## other/Team_OccupationBtnByName.lua.lua
**Functions:**
- GetTeam_OccupationBtnUis
**Requires:**
- Team_OccupationBtnBgByName
**Snippet:**
```lua
require("Team_OccupationBtnBgByName")

function GetTeam_OccupationBtnUis(ui)
  local uis = {}
  uis.OccupationBtnBg = GetTeam_OccupationBtnBgUis(ui:GetChild("OccupationBtnBg"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Team_OccupationRegionByName.lua.lua
**Functions:**
- GetTeam_OccupationRegionUis
**Snippet:**
```lua
function GetTeam_OccupationRegionUis(ui)
  local uis = {}
  
  uis.BtnList = ui:GetChild("BtnList")
  uis.root = ui
  return uis
end
```

---

## other/Team_Quality1_1ByName.lua.lua
**Functions:**
- GetTeam_Quality1_1Uis
**Snippet:**
```lua
function GetTeam_Quality1_1Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Team_Quality1_2ByName.lua.lua
**Functions:**
- GetTeam_Quality1_2Uis
**Snippet:**
```lua
function GetTeam_Quality1_2Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Team_SkillByName.lua.lua
**Functions:**
- GetTeam_SkillUis
**Requires:**
- CommonResource_SkillByName
- Team_SkillCDInfoByName
- CommonResource_SkillDetailsTagByName
**Snippet:**
```lua
require("CommonResource_SkillByName")
require("Team_SkillCDInfoByName")
require("CommonResource_SkillDetailsTagByName")

function GetTeam_SkillUis(ui)
  local uis = {}
  uis.BackImage = ui:GetChild("BackImage")
  uis.Skill = GetCommonResource_SkillUis(ui:GetChild("Skill"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
```

---

## other/Team_SkillCDInfoByName.lua.lua
**Functions:**
- GetTeam_SkillCDInfoUis
**Snippet:**
```lua
function GetTeam_SkillCDInfoUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Team_SureBtnByName.lua.lua
**Functions:**
- GetTeam_SureBtnUis
**Snippet:**
```lua
function GetTeam_SureBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Team_TabBtnBgByName.lua.lua
**Functions:**
- GetTeam_TabBtnBgUis
**Snippet:**
```lua
function GetTeam_TabBtnBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## other/Team_TabBtnByName.lua.lua
**Functions:**
- GetTeam_TabBtnUis
**Requires:**
- Team_TabBtnBgByName
**Snippet:**
```lua
require("Team_TabBtnBgByName")

function GetTeam_TabBtnUis(ui)
  local uis = {}
  uis.TabBtnBg = GetTeam_TabBtnBgUis(ui:GetChild("TabBtnBg"))
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## other/Team_TabRegionByName.lua.lua
**Functions:**
- GetTeam_TabRegionUis
**Snippet:**
```lua
function GetTeam_TabRegionUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## other/Team_TeamByName.lua.lua
**Functions:**
- GetTeam_TeamUis
**Requires:**
- CommonResource_BackGroundByName
- Team_TabRegionByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Team_TabRegionByName")
require("CommonResource_CurrencyReturnByName")

function GetTeam_TeamUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.AdjustmentBtn = ui:GetChild("AdjustmentBtn")
  uis.DeleteBtn = ui:GetChild("DeleteBtn")
  uis.TeamList = ui:GetChild("TeamList")
```

---

## other/Team_TeamTipsByName.lua.lua
**Functions:**
- GetTeam_TeamTipsUis
**Requires:**
- Team_CardTipsByName
**Snippet:**
```lua
require("Team_CardTipsByName")

function GetTeam_TeamTipsUis(ui)
  local uis = {}
  uis.UnUseBtn = ui:GetChild("UnUseBtn")
  uis.CardTips = GetTeam_CardTipsUis(ui:GetChild("CardTips"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Team_TeamWindowByName.lua.lua
**Functions:**
- GetTeam_TeamWindowUis
**Requires:**
- Team_TeamByName
**Snippet:**
```lua
require("Team_TeamByName")

function GetTeam_TeamWindowUis(ui)
  local uis = {}
  uis.Main = GetTeam_TeamUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/Team_UnUseBtnByName.lua.lua
**Functions:**
- GetTeam_UnUseBtnUis
**Snippet:**
```lua
function GetTeam_UnUseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Team_UpBtnByName.lua.lua
**Functions:**
- GetTeam_UpBtnUis
**Snippet:**
```lua
function GetTeam_UpBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/TideDungeonData.lua.lua
**Snippet:**
```lua
local tideDungeons
local SetTideDungeonInfo = function(info)
  tideDungeons = tideDungeons or {}
  local key = table.keyof(tideDungeons, info.sceneType, "sceneType")
  if not key then
    table.insert(tideDungeons, info)
  else
    tideDungeons[key] = info
  end
end
```

---

## other/TideDungeonScriptList.lua.lua
**Requires:**
- TideDungeonData
- TideDungeonService
**Snippet:**
```lua
TideDungeonData = require("TideDungeonData")
TideDungeonService = require("TideDungeonService")
```

---

## other/TideDungeonService.lua.lua
**Snippet:**
```lua
local get_weekly_dungeon_msg = {}
local GetTideDungeonInfoReq = function(param, rspCallback)
  local sceneTypes = get_weekly_dungeon_msg.sceneTypes
  sceneTypes = sceneTypes or {}
  table.clear(sceneTypes)
  if "table" == type(param) then
    for _, v in pairs(param) do
      table.insert(sceneTypes, v)
    end
  elseif type(param) == "number" then
```

---

## other/TideDungeonTipsWindow.lua.lua
**Functions:**
- TideDungeonTipsWindow.ReInitData
- TideDungeonTipsWindow.OnInit
- TideDungeonTipsWindow.UpdateInfo
- TideDungeonTipsWindow.InitBtn
- TideDungeonTipsWindow.OnClose
**Requires:**
- TideDungeon_DungeonTipsWindowByName
**Snippet:**
```lua
require("TideDungeon_DungeonTipsWindowByName")
local TideDungeonTipsWindow = {}
local uis, contentPane, stageId, sceneType
local BuffItemRenderer = function(i, gcmp)
  local stageConf = TableData.GetConfig(stageId, "BaseStage")
  local buffId = stageConf.buff_list[i + 1]
  local conf = TableData.GetConfig(buffId, "BaseSkillBuffPre")
  local buffName = type(conf.name) == "function" and conf.name() or "未配置"
  local buffDesc = "function" == type(conf.des) and conf.des() or "未配置"
  UIUtil.SetText(gcmp, buffName, "NameTxt")
```

---

## other/TideDungeon_DungeonTipsByName.lua.lua
**Functions:**
- GetTideDungeon_DungeonTipsUis
**Requires:**
- CommonResource_PopupBgByName
- TideDungeon_ExplainTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("TideDungeon_ExplainTipsByName")

function GetTideDungeon_DungeonTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.ExplainTips = GetTideDungeon_ExplainTipsUis(ui:GetChild("ExplainTips"))
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_DungeonTipsWindowByName.lua.lua
**Functions:**
- GetTideDungeon_DungeonTipsWindowUis
**Requires:**
- TideDungeon_DungeonTipsByName
**Snippet:**
```lua
require("TideDungeon_DungeonTipsByName")

function GetTideDungeon_DungeonTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetTideDungeon_DungeonTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_ExplainBuffByName.lua.lua
**Functions:**
- GetTideDungeon_ExplainBuffUis
**Snippet:**
```lua
function GetTideDungeon_ExplainBuffUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_ExplainBuffRegionByName.lua.lua
**Functions:**
- GetTideDungeon_ExplainBuffRegionUis
**Snippet:**
```lua
function GetTideDungeon_ExplainBuffRegionUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.BuffList = ui:GetChild("BuffList")
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_ExplainCloseBtnByName.lua.lua
**Functions:**
- GetTideDungeon_ExplainCloseBtnUis
**Snippet:**
```lua
function GetTideDungeon_ExplainCloseBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_ExplainSureBtnByName.lua.lua
**Functions:**
- GetTideDungeon_ExplainSureBtnUis
**Snippet:**
```lua
function GetTideDungeon_ExplainSureBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_ExplainTipsByName.lua.lua
**Functions:**
- GetTideDungeon_ExplainTipsUis
**Requires:**
- TideDungeon_ExplainTitleByName
- TideDungeon_ExplainBuffRegionByName
**Snippet:**
```lua
require("TideDungeon_ExplainTitleByName")
require("TideDungeon_ExplainBuffRegionByName")

function GetTideDungeon_ExplainTipsUis(ui)
  local uis = {}
  uis.Title = GetTideDungeon_ExplainTitleUis(ui:GetChild("Title"))
  uis.Buff = GetTideDungeon_ExplainBuffRegionUis(ui:GetChild("Buff"))
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.AiBattleBtn = ui:GetChild("AiBattleBtn")
  uis.SureBtn = ui:GetChild("SureBtn")
```

---

## other/TideDungeon_ExplainTitleByName.lua.lua
**Functions:**
- GetTideDungeon_ExplainTitleUis
**Snippet:**
```lua
function GetTideDungeon_ExplainTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_RewardItemByName.lua.lua
**Functions:**
- GetTideDungeon_RewardItemUis
**Snippet:**
```lua
function GetTideDungeon_RewardItemUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_TabBgByName.lua.lua
**Functions:**
- GetTideDungeon_TabBgUis
**Snippet:**
```lua
function GetTideDungeon_TabBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_TabBtnByName.lua.lua
**Functions:**
- GetTideDungeon_TabBtnUis
**Requires:**
- TideDungeon_TabBgByName
**Snippet:**
```lua
require("TideDungeon_TabBgByName")

function GetTideDungeon_TabBtnUis(ui)
  local uis = {}
  uis.TabBg = GetTideDungeon_TabBgUis(ui:GetChild("TabBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
```

---

## other/TideDungeon_TabRegionByName.lua.lua
**Functions:**
- GetTideDungeon_TabRegionUis
**Snippet:**
```lua
function GetTideDungeon_TabRegionUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_TideByName.lua.lua
**Functions:**
- GetTideDungeon_TideUis
**Requires:**
- CommonResource_BackGroundByName
- TideDungeon_TideRegionByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("TideDungeon_TideRegionByName")
require("CommonResource_CurrencyReturnByName")

function GetTideDungeon_TideUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TideRegion = GetTideDungeon_TideRegionUis(ui:GetChild("TideRegion"))
  uis.CurrencyReturn = GetCommonResource_CurrencyReturnUis(ui:GetChild("CurrencyReturn"))
  uis.root = ui
```

---

## other/TideDungeon_TideCompleteByName.lua.lua
**Functions:**
- GetTideDungeon_TideCompleteUis
**Snippet:**
```lua
function GetTideDungeon_TideCompleteUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_TideLockByName.lua.lua
**Functions:**
- GetTideDungeon_TideLockUis
**Snippet:**
```lua
function GetTideDungeon_TideLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_TideRegionByName.lua.lua
**Functions:**
- GetTideDungeon_TideRegionUis
**Requires:**
- TideDungeon_TideTitleByName
- TideDungeon_TideTimeByName
- TideDungeon_TabRegionByName
**Snippet:**
```lua
require("TideDungeon_TideTitleByName")
require("TideDungeon_TideTimeByName")
require("TideDungeon_TabRegionByName")

function GetTideDungeon_TideRegionUis(ui)
  local uis = {}
  uis.Title = GetTideDungeon_TideTitleUis(ui:GetChild("Title"))
  uis.Time = GetTideDungeon_TideTimeUis(ui:GetChild("Time"))
  uis.RewardBtn = ui:GetChild("RewardBtn")
  uis.TipsList = ui:GetChild("TipsList")
```

---

## other/TideDungeon_TideRewardBtnByName.lua.lua
**Functions:**
- GetTideDungeon_TideRewardBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetTideDungeon_TideRewardBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_TideRewardByName.lua.lua
**Functions:**
- GetTideDungeon_TideRewardUis
**Requires:**
- CommonResource_BackGroundByName
- TideDungeon_TideRewardTitleByName
- TideDungeon_TideRewardTipsListByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("TideDungeon_TideRewardTitleByName")
require("TideDungeon_TideRewardTipsListByName")

function GetTideDungeon_TideRewardUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.RewardTitle = GetTideDungeon_TideRewardTitleUis(ui:GetChild("RewardTitle"))
  uis.RewardTipsList = GetTideDungeon_TideRewardTipsListUis(ui:GetChild("RewardTipsList"))
  uis.CloseBtn = ui:GetChild("CloseBtn")
```

---

## other/TideDungeon_TideRewardCloseBtnByName.lua.lua
**Functions:**
- GetTideDungeon_TideRewardCloseBtnUis
**Snippet:**
```lua
function GetTideDungeon_TideRewardCloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_TideRewardState1ByName.lua.lua
**Functions:**
- GetTideDungeon_TideRewardState1Uis
**Snippet:**
```lua
function GetTideDungeon_TideRewardState1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_TideRewardState2ByName.lua.lua
**Functions:**
- GetTideDungeon_TideRewardState2Uis
**Snippet:**
```lua
function GetTideDungeon_TideRewardState2Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_TideRewardState3ByName.lua.lua
**Functions:**
- GetTideDungeon_TideRewardState3Uis
**Snippet:**
```lua
function GetTideDungeon_TideRewardState3Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_TideRewardTab1BtnByName.lua.lua
**Functions:**
- GetTideDungeon_TideRewardTab1BtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetTideDungeon_TideRewardTab1BtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_TideRewardTab2BtnByName.lua.lua
**Functions:**
- GetTideDungeon_TideRewardTab2BtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetTideDungeon_TideRewardTab2BtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_TideRewardTab3BtnByName.lua.lua
**Functions:**
- GetTideDungeon_TideRewardTab3BtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetTideDungeon_TideRewardTab3BtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_TideRewardTipsAniByName.lua.lua
**Functions:**
- GetTideDungeon_TideRewardTipsAniUis
**Requires:**
- TideDungeon_TideRewardTipsByName
**Snippet:**
```lua
require("TideDungeon_TideRewardTipsByName")

function GetTideDungeon_TideRewardTipsAniUis(ui)
  local uis = {}
  uis.RewardTips = GetTideDungeon_TideRewardTipsUis(ui:GetChild("RewardTips"))
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_TideRewardTipsByName.lua.lua
**Functions:**
- GetTideDungeon_TideRewardTipsUis
**Requires:**
- TideDungeon_TideRewardState2ByName
- TideDungeon_TideRewardState1ByName
- TideDungeon_TideRewardState3ByName
**Snippet:**
```lua
require("TideDungeon_TideRewardState2ByName")
require("TideDungeon_TideRewardState1ByName")
require("TideDungeon_TideRewardState3ByName")

function GetTideDungeon_TideRewardTipsUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.RewardList = ui:GetChild("RewardList")
  uis.Progress = GetTideDungeon_TideRewardState2Uis(ui:GetChild("Progress"))
  uis.Get = GetTideDungeon_TideRewardState1Uis(ui:GetChild("Get"))
```

---

## other/TideDungeon_TideRewardTipsListByName.lua.lua
**Functions:**
- GetTideDungeon_TideRewardTipsListUis
**Snippet:**
```lua
function GetTideDungeon_TideRewardTipsListUis(ui)
  local uis = {}
  
  uis.RewardTipsList = ui:GetChild("RewardTipsList")
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_TideRewardTitleByName.lua.lua
**Functions:**
- GetTideDungeon_TideRewardTitleUis
**Snippet:**
```lua
function GetTideDungeon_TideRewardTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_TideRewardWindowByName.lua.lua
**Functions:**
- GetTideDungeon_TideRewardWindowUis
**Requires:**
- TideDungeon_TideRewardByName
**Snippet:**
```lua
require("TideDungeon_TideRewardByName")

function GetTideDungeon_TideRewardWindowUis(ui)
  local uis = {}
  uis.Main = GetTideDungeon_TideRewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_TideTimeByName.lua.lua
**Functions:**
- GetTideDungeon_TideTimeUis
**Snippet:**
```lua
function GetTideDungeon_TideTimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_TideTipsAniByName.lua.lua
**Functions:**
- GetTideDungeon_TideTipsAniUis
**Requires:**
- TideDungeon_TideTipsByName
**Snippet:**
```lua
require("TideDungeon_TideTipsByName")

function GetTideDungeon_TideTipsAniUis(ui)
  local uis = {}
  uis.TideTips = GetTideDungeon_TideTipsUis(ui:GetChild("TideTips"))
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_TideTipsByName.lua.lua
**Functions:**
- GetTideDungeon_TideTipsUis
**Requires:**
- TideDungeon_TideCompleteByName
- TideDungeon_TideLockByName
**Snippet:**
```lua
require("TideDungeon_TideCompleteByName")
require("TideDungeon_TideLockByName")

function GetTideDungeon_TideTipsUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TideComplete = GetTideDungeon_TideCompleteUis(ui:GetChild("TideComplete"))
  uis.TideLock = GetTideDungeon_TideLockUis(ui:GetChild("TideLock"))
```

---

## other/TideDungeon_TideTitleByName.lua.lua
**Functions:**
- GetTideDungeon_TideTitleUis
**Snippet:**
```lua
function GetTideDungeon_TideTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/TideDungeon_TideWindowByName.lua.lua
**Functions:**
- GetTideDungeon_TideWindowUis
**Requires:**
- TideDungeon_TideByName
**Snippet:**
```lua
require("TideDungeon_TideByName")

function GetTideDungeon_TideWindowUis(ui)
  local uis = {}
  uis.Main = GetTideDungeon_TideUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/TideRewardWindow.lua.lua
**Functions:**
- rewardlist.itemRenderer
- TideRewardWindow.ReInitData
- TideRewardWindow.OnInit
- TideRewardWindow.UpdateInfo
- TideRewardWindow.InitBtn
- TideRewardWindow.OnClose
- TideRewardWindow.HandleMessage
**Requires:**
- TideDungeon_TideRewardWindowByName
**Snippet:**
```lua
require("TideDungeon_TideRewardWindowByName")
local TideRewardWindow = {}
local uis, contentPane, curDungeonType, rewardItems
local TAB_DUNGEON_TYPE = {
  ProtoEnum.SCENE_TYPE.MANOR_WATER,
  ProtoEnum.SCENE_TYPE.MANOR_FIR,
  ProtoEnum.SCENE_TYPE.MANOR_WOOD
}
local ForeachTabBtns = function(func)
  if type(func) == "function" then
```

---

## other/TideWindow.lua.lua
**Functions:**
- RefreshStages
- RefreshTablist
- RefreshPanelInfo
- TideWindow.ReInitData
- TideWindow.OnInit
- TideWindow.UpdateInfo
- TideWindow.InitBtn
- TideWindow.OnShown
- TideWindow.OnClose
**Requires:**
- TideDungeon_TideWindowByName
**Snippet:**
```lua
require("TideDungeon_TideWindowByName")
local TideWindow = {}
local uis, contentPane, curDungeonType
local TAB_DUNGEON_TYPE = {
  ProtoEnum.SCENE_TYPE.MANOR_WATER,
  ProtoEnum.SCENE_TYPE.MANOR_FIR,
  ProtoEnum.SCENE_TYPE.MANOR_WOOD
}
local RefreshTablist, RefreshStages, RefreshPanelInfo
local GetStages = function()
```

---

## other/TimeLimitedTowerData.lua.lua
**Snippet:**
```lua
local activityId
local SetActivityId = function(id)
  activityId = id
end
local GetActivityId = function()
  return activityId
end
local passedStages
local SetPassedStages = function(stages)
  passedStages = stages
```

---

## other/TimeLimitedTowerMgr.lua.lua
**Snippet:**
```lua
local GetChapterConfig = function()
  local activityId = TimeLimitedTowerData.GetActivityId()
  local conf = TableData.GetConfig(activityId, "BaseActivity")
  if conf then
    local splits = Split(conf.parameter, "|")
    local chapterId = tonumber(splits[1])
    local chapterConf = TableData.GetConfig(chapterId, "BaseChapter")
    return chapterConf
  end
end
```

---

## other/TimeLimitedTowerRewardWindow.lua.lua
**Functions:**
- rewardlist.itemRenderer
- TimeLimitedTowerRewardWindow.ReInitData
- TimeLimitedTowerRewardWindow.OnInit
- TimeLimitedTowerRewardWindow.UpdateInfo
- TimeLimitedTowerRewardWindow.InitBtn
- TimeLimitedTowerRewardWindow.OnClose
**Requires:**
- TowerSpecial_RewardListWindowByName
**Snippet:**
```lua
require("TowerSpecial_RewardListWindowByName")
local TimeLimitedTowerRewardWindow = {}
local uis, contentPane
local RefreshPanelInfo = function(playanim)
  local itemlist = uis.Main.ItemList
  local tasks = TimeLimitedTowerData.GetTasks()
  itemlist.numItems = tasks and #tasks or 0
  if playanim then
    for i = 0, itemlist.numChildren - 1 do
      local child = itemlist:GetChildAt(i)
```

---

## other/TimeLimitedTowerScriptList.lua.lua
**Requires:**
- TimeLimitedTowerData
- TimeLimitedTowerService
- TimeLimitedTowerMgr
**Snippet:**
```lua
TimeLimitedTowerData = require("TimeLimitedTowerData")
TimeLimitedTowerService = require("TimeLimitedTowerService")
TimeLimitedTowerMgr = require("TimeLimitedTowerMgr")
```

---

## other/TimeLimitedTowerService.lua.lua
**Snippet:**
```lua
local GetTimeLimitedTowerInfoReq = function(rspCallback)
  Net.Send(Proto.MsgName.GetLimitChallengeInfoReq, nil, rspCallback)
end
local GetTimeLimitedTowerInfoRsp = function(msg)
  TimeLimitedTowerData.SetActivityId(msg.activityId)
  TimeLimitedTowerData.SetPassedStages(msg.passStages)
  TimeLimitedTowerData.SetTasks(msg.tasks)
  TimeLimitedTowerData.SetTimestamp(msg.startStamp, msg.endStamp)
end
local ResetTimeLimitedTowerReq = function(rspCallback, errorCallback)
```

---

## other/TimeLimitedTowerWindow.lua.lua
**Functions:**
- TimeLimitedTowerWindow.ReInitData
- TimeLimitedTowerWindow.OnInit
- TimeLimitedTowerWindow.UpdateInfo
- TimeLimitedTowerWindow.InitBtn
- TimeLimitedTowerWindow.OnShown
- TimeLimitedTowerWindow.OnClose
**Requires:**
- TowerSpecial_TowerSpecialWindowByName
**Snippet:**
```lua
require("TowerSpecial_TowerSpecialWindowByName")
local TimeLimitedTowerWindow = {}
local uis, contentPane
local SPECIAL_LEVEL_INDEX_TO_LAST = 2
local EventItemRenderer = function(i, gcmp)
  local stages = TimeLimitedTowerMgr.GetStages()
  local index = i + 1
  local len = #stages
  local stageId = stages[index]
  local subgcmp = gcmp:GetChild("BattleEventBtn")
```

---

## other/TimerUtil.lua.lua
**Functions:**
- TimerUtil.new
- obj:start
- obj:stop
- obj:Comp
- obj:pause
- obj:resume
- obj:restart
- obj:reset
- obj:_doTick
- obj:_tick
- obj:_comp
- obj:IsRunIng
- obj:_destroy
- obj:_delFromRunningTimers
- TimerUtil.StopAllTimer
- TimerUtil.fixedUpdateCallback
- TimerUtil.updateCallback
- TimerUtil.setTimeout
- TimerUtil.setInterval
**Snippet:**
```lua
local Time = Time
local getTime = function(unscaledTime)
  if unscaledTime then
    return Time.unscaledTime * 1000
  end
  return Time.fixedTime * 1000
end
local TimerUtil = {}
TimerUtil.runningTimersFixedUpdate = {}
TimerUtil.runningTimersUpdate = {}
```

---

## other/TimeUtil.lua.lua
**Functions:**
- TimeUtil.GetTimeStr
- TimeUtil.CountDown
- timerInfo:start
- timerInfo:Stop
- timerInfo:Complete
- timerInfo:Pause
- timerInfo:Resume
- TimeUtil.FormatRemainTimeRough
- TimeUtil.FormatTime
- TimeUtil.FormatDate
- TimeUtil.GetTimeZone
- TimeUtil.FormatOfflineTime
- TimeUtil.FormatEnTime
**Snippet:**
```lua
local TimeUtil = {}
local s_format = string.format
local mathFloor = math.floor
local osTime = os.time
local osDate = os.date
local osDifftime = os.difftime

function TimeUtil.GetTimeStr(time, showDay)
  time = mathFloor(time)
  local hours, minutes, seconds
```

---

## other/TokenExplainWindow.lua.lua
**Functions:**
- TokenExplainWindow.ReInitData
- TokenExplainWindow.OnInit
- TokenExplainWindow.UpdateInfo
- TokenExplainWindow.InitBtn
- TokenExplainWindow.OnClose
**Requires:**
- Shop_TokenExplainWindowByName
**Snippet:**
```lua
require("Shop_TokenExplainWindowByName")
local TokenExplainWindow = {}
local uis, contentPane

function TokenExplainWindow.ReInitData()
end

function TokenExplainWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.TokenExplainWindow.package, WinResConfig.TokenExplainWindow.comName, function(com)
    contentPane = com
```

---

## other/TouchCardTemplate.lua.lua

---

## other/touch_cardspine_10016_3.lua.lua
**Snippet:**
```lua
local OnClick = function(skeletonAnimation, animationName, gesture)
  local go = skeletonAnimation.gameObject
  local track = 1
  local current = skeletonAnimation.state:GetCurrent(track)
  if nil == current or current.IsComplete then
    SkeletonAnimationUtil.SetAnimation(go, track, animationName, false)
  end
end
return {OnClick = OnClick}
```

---

## other/touch_cardspine_10098_3.lua.lua
**Snippet:**
```lua
local CLICK_INTERVAL = 0
local OnClick = function(skeletonAnimation, animationName, gesture)
  local go = skeletonAnimation.gameObject
  local track = 0
  local current = skeletonAnimation.state:GetCurrent(track)
  if nil == current or current.Animation.Name ~= animationName or current.TrackTime >= CLICK_INTERVAL then
    SkeletonAnimationUtil.SetAnimation(go, track, animationName, false, function()
      SkeletonAnimationUtil.SetAnimation(go, track, "idle", true)
    end)
  end
```

---

## other/touch_cardspine_10102_3.lua.lua
**Snippet:**
```lua
local CLICK_INTERVAL = 0
local OnClick = function(skeletonAnimation, animationName, gesture)
  local go = skeletonAnimation.gameObject
  local track = 0
  local current = skeletonAnimation.state:GetCurrent(track)
  if nil == current or current.Animation.Name ~= animationName or current.TrackTime >= CLICK_INTERVAL then
    SkeletonAnimationUtil.SetAnimation(go, track, animationName, false, function()
      SkeletonAnimationUtil.SetAnimation(go, track, "idle", true)
    end)
  end
```

---

## other/touch_cardspine_10103_3.lua.lua
**Snippet:**
```lua
local CLICK_INTERVAL = 0
local OnClick = function(skeletonAnimation, animationName, gesture)
  local go = skeletonAnimation.gameObject
  local track = 0
  local current = skeletonAnimation.state:GetCurrent(track)
  if nil == current or current.Animation.Name ~= animationName or current.TrackTime >= CLICK_INTERVAL then
    SkeletonAnimationUtil.SetAnimation(go, track, animationName, false, function()
      SkeletonAnimationUtil.SetAnimation(go, track, "idle", true)
    end)
  end
```

---

## other/TowerListWindow.lua.lua
**Functions:**
- TowerListWindow.ReInitData
- TowerListWindow.OnInit
- TowerListWindow.UpdateInfo
- uis.Main.TipsList.itemRenderer
- TowerListWindow.SetCurPage
- TowerListWindow.GetListData
- TowerListWindow.InitBtn
- TowerListWindow.InitChapterReward
- TowerListWindow.OnShown
- TowerListWindow.OnClose
**Requires:**
- Tower_TowerListWindowByName
**Snippet:**
```lua
require("Tower_TowerListWindowByName")
local TowerListWindow = {}
local uis, contentPane, jumpTb, info, mapState

function TowerListWindow.ReInitData()
end

function TowerListWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.TowerListWindow.package, WinResConfig.TowerListWindow.comName, function(com)
    contentPane = com
```

---

## other/TowerRewardWindow.lua.lua
**Functions:**
- TowerRewardWindow.ReInitData
- TowerRewardWindow.OnInit
- TowerRewardWindow.Init
- TowerRewardWindow.GetName
- TowerRewardWindow.UpdateInfo
- tips.ItemList.itemRenderer
- TowerRewardWindow.InitBtn
- TowerRewardWindow.OnClose
**Requires:**
- Tower_TowerRewardWindowByName
**Snippet:**
```lua
require("Tower_TowerRewardWindowByName")
local TowerRewardWindow = {}
local uis, contentPane

function TowerRewardWindow.ReInitData()
end

function TowerRewardWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.TowerRewardWindow.package, WinResConfig.TowerRewardWindow.comName, function(com)
    contentPane = com
```

---

## other/TowerSpecial_BattleEventAniByName.lua.lua
**Functions:**
- GetTowerSpecial_BattleEventAniUis
**Snippet:**
```lua
function GetTowerSpecial_BattleEventAniUis(ui)
  local uis = {}
  
  uis.BattleEventBtn = ui:GetChild("BattleEventBtn")
  uis.root = ui
  return uis
end
```

---

## other/TowerSpecial_BattleEventBtnByName.lua.lua
**Functions:**
- GetTowerSpecial_BattleEventBtnUis
**Requires:**
- TowerSpecial_BattleEventSignByName
- TowerSpecial_BattleEventLockByName
**Snippet:**
```lua
require("TowerSpecial_BattleEventSignByName")
require("TowerSpecial_BattleEventLockByName")

function GetTowerSpecial_BattleEventBtnUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.Sign = GetTowerSpecial_BattleEventSignUis(ui:GetChild("Sign"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Lock = GetTowerSpecial_BattleEventLockUis(ui:GetChild("Lock"))
```

---

## other/TowerSpecial_BattleEventLockByName.lua.lua
**Functions:**
- GetTowerSpecial_BattleEventLockUis
**Snippet:**
```lua
function GetTowerSpecial_BattleEventLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/TowerSpecial_BattleEventRegionByName.lua.lua
**Functions:**
- GetTowerSpecial_BattleEventRegionUis
**Snippet:**
```lua
function GetTowerSpecial_BattleEventRegionUis(ui)
  local uis = {}
  
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.EventList = ui:GetChild("EventList")
  uis.root = ui
  return uis
end
```

---

## other/TowerSpecial_BattleEventSignByName.lua.lua
**Functions:**
- GetTowerSpecial_BattleEventSignUis
**Snippet:**
```lua
function GetTowerSpecial_BattleEventSignUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/TowerSpecial_CardHeadAniByName.lua.lua
**Functions:**
- GetTowerSpecial_CardHeadAniUis
**Snippet:**
```lua
function GetTowerSpecial_CardHeadAniUis(ui)
  local uis = {}
  
  uis.CardHeadBtn = ui:GetChild("CardHeadBtn")
  uis.root = ui
  return uis
end
```

---

## other/TowerSpecial_CardHeadBgByName.lua.lua
**Functions:**
- GetTowerSpecial_CardHeadBgUis
**Snippet:**
```lua
function GetTowerSpecial_CardHeadBgUis(ui)
  local uis = {}
  
  uis.CardPicLoader = ui:GetChild("CardPicLoader")
  uis.root = ui
  return uis
end
```

---

## other/TowerSpecial_CardHeadBtnByName.lua.lua
**Functions:**
- GetTowerSpecial_CardHeadBtnUis
**Requires:**
- TowerSpecial_CardHeadBgByName
- CommonResource_OccupationByName
**Snippet:**
```lua
require("TowerSpecial_CardHeadBgByName")
require("CommonResource_OccupationByName")

function GetTowerSpecial_CardHeadBtnUis(ui)
  local uis = {}
  uis.CardPic = GetTowerSpecial_CardHeadBgUis(ui:GetChild("CardPic"))
  uis.ElementList = ui:GetChild("ElementList")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Occupation = GetCommonResource_OccupationUis(ui:GetChild("Occupation"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## other/TowerSpecial_RecommendCardByName.lua.lua
**Functions:**
- GetTowerSpecial_RecommendCardUis
**Snippet:**
```lua
function GetTowerSpecial_RecommendCardUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.CardList = ui:GetChild("CardList")
  uis.root = ui
  return uis
end
```

---

## other/TowerSpecial_RewardBtnByName.lua.lua
**Functions:**
- GetTowerSpecial_RewardBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetTowerSpecial_RewardBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/TowerSpecial_RewardItemByName.lua.lua
**Functions:**
- GetTowerSpecial_RewardItemUis
**Snippet:**
```lua
function GetTowerSpecial_RewardItemUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/TowerSpecial_RewardItemListAniByName.lua.lua
**Functions:**
- GetTowerSpecial_RewardItemListAniUis
**Requires:**
- TowerSpecial_RewardItemListByName
**Snippet:**
```lua
require("TowerSpecial_RewardItemListByName")

function GetTowerSpecial_RewardItemListAniUis(ui)
  local uis = {}
  uis.Item = GetTowerSpecial_RewardItemListUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## other/TowerSpecial_RewardItemListByName.lua.lua
**Functions:**
- GetTowerSpecial_RewardItemListUis
**Snippet:**
```lua
function GetTowerSpecial_RewardItemListUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.GetTxt = ui:GetChild("GetTxt")
  uis.ProgressTxt = ui:GetChild("ProgressTxt")
  uis.RewardList = ui:GetChild("RewardList")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## other/TowerSpecial_RewardListByName.lua.lua
**Functions:**
- GetTowerSpecial_RewardListUis
**Requires:**
- CommonResource_BackGroundByName
- TowerSpecial_TitleByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("TowerSpecial_TitleByName")

function GetTowerSpecial_RewardListUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Title = GetTowerSpecial_TitleUis(ui:GetChild("Title"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## other/TowerSpecial_RewardListWindowByName.lua.lua
**Functions:**
- GetTowerSpecial_RewardListWindowUis
**Requires:**
- TowerSpecial_RewardListByName
**Snippet:**
```lua
require("TowerSpecial_RewardListByName")

function GetTowerSpecial_RewardListWindowUis(ui)
  local uis = {}
  uis.Main = GetTowerSpecial_RewardListUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/TowerSpecial_SpecialProgressBtnByName.lua.lua
**Functions:**
- GetTowerSpecial_SpecialProgressBtnUis
**Snippet:**
```lua
function GetTowerSpecial_SpecialProgressBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/TowerSpecial_SpecialProgressByName.lua.lua
**Functions:**
- GetTowerSpecial_SpecialProgressUis
**Snippet:**
```lua
function GetTowerSpecial_SpecialProgressUis(ui)
  local uis = {}
  
  uis.ProgressBtn = ui:GetChild("ProgressBtn")
  uis.DotList = ui:GetChild("DotList")
  uis.root = ui
  return uis
end
```

---

## other/TowerSpecial_SpecialProgressDotByName.lua.lua
**Functions:**
- GetTowerSpecial_SpecialProgressDotUis
**Snippet:**
```lua
function GetTowerSpecial_SpecialProgressDotUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/TowerSpecial_TitleByName.lua.lua
**Functions:**
- GetTowerSpecial_TitleUis
**Snippet:**
```lua
function GetTowerSpecial_TitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/TowerSpecial_TowerSpecialByName.lua.lua
**Functions:**
- GetTowerSpecial_TowerSpecialUis
**Requires:**
- CommonResource_BackGroundByName
- TowerSpecial_BattleEventRegionByName
- TowerSpecial_SpecialProgressByName
- TowerSpecial_RecommendCardByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("TowerSpecial_BattleEventRegionByName")
require("TowerSpecial_SpecialProgressByName")
require("TowerSpecial_RecommendCardByName")
require("CommonResource_CurrencyReturnByName")

function GetTowerSpecial_TowerSpecialUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleEventRegion = GetTowerSpecial_BattleEventRegionUis(ui:GetChild("BattleEventRegion"))
```

---

## other/TowerSpecial_TowerSpecialWindowByName.lua.lua
**Functions:**
- GetTowerSpecial_TowerSpecialWindowUis
**Requires:**
- TowerSpecial_TowerSpecialByName
**Snippet:**
```lua
require("TowerSpecial_TowerSpecialByName")

function GetTowerSpecial_TowerSpecialWindowUis(ui)
  local uis = {}
  uis.Main = GetTowerSpecial_TowerSpecialUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/TowerWindow.lua.lua
**Functions:**
- TowerWindow.OnInit
- TowerWindow.GetChaptersInfo
- TowerWindow.CheckTips
- TowerWindow.GetOpenConditionLv
- TowerWindow.OpenTips
- TowerWindow.UpdateInfo
- TowerWindow.ShowStageInfo
- TowerWindow.LoadStageInfo
- TowerWindow.ItemClick
- TowerWindow.InitBtn
- TowerWindow.InitChapterReward
- TowerWindow.OnShown
- TowerWindow.HandleMessage
- TowerWindow.OnClose
**Requires:**
- Tower_TowerWindowByName
**Snippet:**
```lua
require("Tower_TowerWindowByName")
local TowerWindow = {}
local contain = table.contain
local uis, contentPane, chapterData, jumpTb, towerMapData, sceneInfo, curBgPath, firstEnter

function TowerWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.TowerWindow.package, WinResConfig.TowerWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetTower_TowerWindowUis(contentPane)
```

---

## other/TowerWordContentWindow.lua.lua
**Functions:**
- TowerWordContentWindow.OnInit
- TowerWordContentWindow.Init
- uis.Main.WordList.itemRenderer
- TowerWordContentWindow.InitBtn
- TowerWordContentWindow.OnClose
**Requires:**
- Tower_WordContentWindowByName
**Snippet:**
```lua
require("Tower_WordContentWindowByName")
local TowerWordContentWindow = {}
local uis, contentPane, chapterData

function TowerWordContentWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.TowerWordContentWindow.package, WinResConfig.TowerWordContentWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetTower_WordContentWindowUis(contentPane)
    local id = bridgeObj.argTable[1]
```

---

## other/Tower_BattleListByName.lua.lua
**Functions:**
- GetTower_BattleListUis
**Snippet:**
```lua
function GetTower_BattleListUis(ui)
  local uis = {}
  
  uis.Checkpoint1Btn = ui:GetChild("Checkpoint1Btn")
  uis.Checkpoint2Btn = ui:GetChild("Checkpoint2Btn")
  uis.Checkpoint3Btn = ui:GetChild("Checkpoint3Btn")
  uis.Checkpoint4Btn = ui:GetChild("Checkpoint4Btn")
  uis.Checkpoint5Btn = ui:GetChild("Checkpoint5Btn")
  uis.root = ui
  return uis
```

---

## other/Tower_BattlePointBtnByName.lua.lua
**Functions:**
- GetTower_BattlePointBtnUis
**Requires:**
- Tower_BattlePointByName
**Snippet:**
```lua
require("Tower_BattlePointByName")

function GetTower_BattlePointBtnUis(ui)
  local uis = {}
  uis.BattlePoint = GetTower_BattlePointUis(ui:GetChild("BattlePoint"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Tower_BattlePointByName.lua.lua
**Functions:**
- GetTower_BattlePointUis
**Requires:**
- Tower_BattlePointDotByName
- Tower_BattlePointLockByName
**Snippet:**
```lua
require("Tower_BattlePointDotByName")
require("Tower_BattlePointLockByName")

function GetTower_BattlePointUis(ui)
  local uis = {}
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.IDTxt = ui:GetChild("IDTxt")
  uis.IDLockTxt = ui:GetChild("IDLockTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
```

---

## other/Tower_BattlePointDotByName.lua.lua
**Functions:**
- GetTower_BattlePointDotUis
**Snippet:**
```lua
function GetTower_BattlePointDotUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Tower_BattlePointLockByName.lua.lua
**Functions:**
- GetTower_BattlePointLockUis
**Snippet:**
```lua
function GetTower_BattlePointLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Tower_CheckpointAniByName.lua.lua
**Functions:**
- GetTower_CheckpointAniUis
**Snippet:**
```lua
function GetTower_CheckpointAniUis(ui)
  local uis = {}
  
  uis.CheckpointBtn = ui:GetChild("CheckpointBtn")
  uis.root = ui
  return uis
end
```

---

## other/Tower_CheckpointBtnByName.lua.lua
**Functions:**
- GetTower_CheckpointBtnUis
**Requires:**
- Tower_CheckpointNumberByName
**Snippet:**
```lua
require("Tower_CheckpointNumberByName")

function GetTower_CheckpointBtnUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.CheckpointNumber = GetTower_CheckpointNumberUis(ui:GetChild("CheckpointNumber"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## other/Tower_CheckpointNumberByName.lua.lua
**Functions:**
- GetTower_CheckpointNumberUis
**Snippet:**
```lua
function GetTower_CheckpointNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## other/Tower_GotoBtnByName.lua.lua
**Functions:**
- GetTower_GotoBtnUis
**Snippet:**
```lua
function GetTower_GotoBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Tower_LayersFutureByName.lua.lua
**Functions:**
- GetTower_LayersFutureUis
**Snippet:**
```lua
function GetTower_LayersFutureUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.root = ui
  return uis
end
```

---

## other/Tower_LayersLockByName.lua.lua
**Functions:**
- GetTower_LayersLockUis
**Snippet:**
```lua
function GetTower_LayersLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Tower_LayersNowByName.lua.lua
**Functions:**
- GetTower_LayersNowUis
**Snippet:**
```lua
function GetTower_LayersNowUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Tower_LayersTipsAniByName.lua.lua
**Functions:**
- GetTower_LayersTipsAniUis
**Requires:**
- Tower_LayersTipsByName
**Snippet:**
```lua
require("Tower_LayersTipsByName")

function GetTower_LayersTipsAniUis(ui)
  local uis = {}
  uis.LayersTips = GetTower_LayersTipsUis(ui:GetChild("LayersTips"))
  uis.root = ui
  return uis
end
```

---

## other/Tower_LayersTipsByName.lua.lua
**Functions:**
- GetTower_LayersTipsUis
**Requires:**
- Tower_LayersNowByName
- Tower_ProgressStripByName
- Tower_LayersLockByName
- Tower_LayersFutureByName
**Snippet:**
```lua
require("Tower_LayersNowByName")
require("Tower_ProgressStripByName")
require("Tower_LayersLockByName")
require("Tower_LayersFutureByName")

function GetTower_LayersTipsUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
```

---

## other/Tower_LockTipsBgByName.lua.lua
**Functions:**
- GetTower_LockTipsBgUis
**Snippet:**
```lua
function GetTower_LockTipsBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## other/Tower_LockTipsByName.lua.lua
**Functions:**
- GetTower_LockTipsUis
**Requires:**
- Tower_LockTipsBgByName
**Snippet:**
```lua
require("Tower_LockTipsBgByName")

function GetTower_LockTipsUis(ui)
  local uis = {}
  uis.LockTipsBg = GetTower_LockTipsBgUis(ui:GetChild("LockTipsBg"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.GotoBtn = ui:GetChild("GotoBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## other/Tower_Map_001_1ByName.lua.lua
**Functions:**
- GetTower_Map_001_1Uis
**Snippet:**
```lua
function GetTower_Map_001_1Uis(ui)
  local uis = {}
  
  uis.Point1Btn = ui:GetChild("Point1Btn")
  uis.Point2Btn = ui:GetChild("Point2Btn")
  uis.Point3Btn = ui:GetChild("Point3Btn")
  uis.Point4Btn = ui:GetChild("Point4Btn")
  uis.Point5Btn = ui:GetChild("Point5Btn")
  uis.root = ui
  return uis
```

---

## other/Tower_Map_001_2ByName.lua.lua
**Functions:**
- GetTower_Map_001_2Uis
**Snippet:**
```lua
function GetTower_Map_001_2Uis(ui)
  local uis = {}
  
  uis.Point1Btn = ui:GetChild("Point1Btn")
  uis.Point2Btn = ui:GetChild("Point2Btn")
  uis.Point3Btn = ui:GetChild("Point3Btn")
  uis.Point4Btn = ui:GetChild("Point4Btn")
  uis.Point5Btn = ui:GetChild("Point5Btn")
  uis.root = ui
  return uis
```

---

## other/Tower_Map_001_3ByName.lua.lua
**Functions:**
- GetTower_Map_001_3Uis
**Snippet:**
```lua
function GetTower_Map_001_3Uis(ui)
  local uis = {}
  
  uis.Point1Btn = ui:GetChild("Point1Btn")
  uis.Point2Btn = ui:GetChild("Point2Btn")
  uis.Point3Btn = ui:GetChild("Point3Btn")
  uis.Point4Btn = ui:GetChild("Point4Btn")
  uis.Point5Btn = ui:GetChild("Point5Btn")
  uis.root = ui
  return uis
```

---

## other/Tower_Map_001_4ByName.lua.lua
**Functions:**
- GetTower_Map_001_4Uis
**Snippet:**
```lua
function GetTower_Map_001_4Uis(ui)
  local uis = {}
  
  uis.Point1Btn = ui:GetChild("Point1Btn")
  uis.Point2Btn = ui:GetChild("Point2Btn")
  uis.Point3Btn = ui:GetChild("Point3Btn")
  uis.Point4Btn = ui:GetChild("Point4Btn")
  uis.Point5Btn = ui:GetChild("Point5Btn")
  uis.root = ui
  return uis
```

---

## other/Tower_Map_001_5ByName.lua.lua
**Functions:**
- GetTower_Map_001_5Uis
**Snippet:**
```lua
function GetTower_Map_001_5Uis(ui)
  local uis = {}
  
  uis.Point1Btn = ui:GetChild("Point1Btn")
  uis.Point2Btn = ui:GetChild("Point2Btn")
  uis.Point3Btn = ui:GetChild("Point3Btn")
  uis.Point4Btn = ui:GetChild("Point4Btn")
  uis.Point5Btn = ui:GetChild("Point5Btn")
  uis.root = ui
  return uis
```

---

## other/Tower_ProgressDotByName.lua.lua
**Functions:**
- GetTower_ProgressDotUis
**Snippet:**
```lua
function GetTower_ProgressDotUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Tower_ProgressStripByName.lua.lua
**Functions:**
- GetTower_ProgressStripUis
**Requires:**
- Tower_ProgressDotByName
**Snippet:**
```lua
require("Tower_ProgressDotByName")

function GetTower_ProgressStripUis(ui)
  local uis = {}
  uis.Dot1 = GetTower_ProgressDotUis(ui:GetChild("Dot1"))
  uis.Dot2 = GetTower_ProgressDotUis(ui:GetChild("Dot2"))
  uis.Dot3 = GetTower_ProgressDotUis(ui:GetChild("Dot3"))
  uis.Dot4 = GetTower_ProgressDotUis(ui:GetChild("Dot4"))
  uis.Dot5 = GetTower_ProgressDotUis(ui:GetChild("Dot5"))
  uis.root = ui
```

---

## other/Tower_RewardBtnByName.lua.lua
**Functions:**
- GetTower_RewardBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetTower_RewardBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Tower_RewardCompleteByName.lua.lua
**Functions:**
- GetTower_RewardCompleteUis
**Snippet:**
```lua
function GetTower_RewardCompleteUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Tower_RewardLockByName.lua.lua
**Functions:**
- GetTower_RewardLockUis
**Snippet:**
```lua
function GetTower_RewardLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Tower_RewardTipsByName.lua.lua
**Functions:**
- GetTower_RewardTipsUis
**Requires:**
- Tower_RewardCompleteByName
- Tower_RewardLockByName
**Snippet:**
```lua
require("Tower_RewardCompleteByName")
require("Tower_RewardLockByName")

function GetTower_RewardTipsUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Name1Txt = ui:GetChild("Name1Txt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.RewardTxt = ui:GetChild("RewardTxt")
  uis.Complete = GetTower_RewardCompleteUis(ui:GetChild("Complete"))
```

---

## other/Tower_SceneByName.lua.lua
**Functions:**
- GetTower_SceneUis
**Requires:**
- CommonResource_BackGroundByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")

function GetTower_SceneUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.MapList = ui:GetChild("MapList")
  uis.root = ui
  return uis
end
```

---

## other/Tower_TowerByName.lua.lua
**Functions:**
- GetTower_TowerUis
**Requires:**
- Tower_SceneByName
- Tower_BattleListByName
- Tower_LockTipsByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("Tower_SceneByName")
require("Tower_BattleListByName")
require("Tower_LockTipsByName")
require("CommonResource_CurrencyReturnByName")

function GetTower_TowerUis(ui)
  local uis = {}
  uis.Scene = GetTower_SceneUis(ui:GetChild("Scene"))
  uis.BattleList = GetTower_BattleListUis(ui:GetChild("BattleList"))
  uis.RewardBtn = ui:GetChild("RewardBtn")
```

---

## other/Tower_TowerListByName.lua.lua
**Functions:**
- GetTower_TowerListUis
**Requires:**
- CommonResource_BackGroundByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("CommonResource_CurrencyReturnByName")

function GetTower_TowerListUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.TipsList = ui:GetChild("TipsList")
  uis.RewardBtn = ui:GetChild("RewardBtn")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
```

---

## other/Tower_TowerListWindowByName.lua.lua
**Functions:**
- GetTower_TowerListWindowUis
**Requires:**
- Tower_TowerListByName
**Snippet:**
```lua
require("Tower_TowerListByName")

function GetTower_TowerListWindowUis(ui)
  local uis = {}
  uis.Main = GetTower_TowerListUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/Tower_TowerRewardByName.lua.lua
**Functions:**
- GetTower_TowerRewardUis
**Requires:**
- CommonResource_PopupBgByName
- Tower_RewardTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Tower_RewardTipsByName")

function GetTower_TowerRewardUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.RewardTips = GetTower_RewardTipsUis(ui:GetChild("RewardTips"))
  uis.root = ui
  return uis
```

---

## other/Tower_TowerRewardWindowByName.lua.lua
**Functions:**
- GetTower_TowerRewardWindowUis
**Requires:**
- Tower_TowerRewardByName
**Snippet:**
```lua
require("Tower_TowerRewardByName")

function GetTower_TowerRewardWindowUis(ui)
  local uis = {}
  uis.Main = GetTower_TowerRewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/Tower_TowerWindowByName.lua.lua
**Functions:**
- GetTower_TowerWindowUis
**Requires:**
- Tower_TowerByName
**Snippet:**
```lua
require("Tower_TowerByName")

function GetTower_TowerWindowUis(ui)
  local uis = {}
  uis.Main = GetTower_TowerUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/TrieTree.lua.lua
**Functions:**
- TrieTree.CreateTree
- tree:Init
- tree:Insert
- tree:IsContainBlockedWord
- tree:FilterBlockedWords
**Snippet:**
```lua
TrieTree = {}
local GetDivideStringList = function(sourceString)
  local divideList = {}
  local len = string.len(sourceString)
  local stPos = 1
  local utf8Sign = {
    192,
    224,
    240,
    248,
```

---

## other/UIHelper.lua.lua
**Functions:**
- CreateUIPage
- NewLuaWindow
- OpenPopWindow
- JumpToWindow
- OpenWindow
- OpenWindowWithFullArg
- OpenWindowImmediately
- OpenWindowWithFullArgImmediately
- ClearLuaWins
- PlayUITransToComplete
- IsUITransPlaying
- PlayUITransAdaptDuration
- PlayUITrans
- DisposeTrans
- GetTransitionDuration
- SetControllerIgnoreTimeScale
- ChangeUIController
- ChangeController
- GetControllerIndex
**Requires:**
- LuaWinRegister
**Snippet:**
```lua
UIMgr = CS.UIManager.Singleton
UILayer = CS.UILayer
BottomLayerEnum = CS.BottomLayerEnum
local LuaWins = {}
require("LuaWinRegister")

function CreateUIPage(cfg)
  return UIMgr:CreateUIPage(cfg.package, cfg.resName)
end

```

---

## other/UIUtil.lua.lua
**Functions:**
- UIUtil.GetResUrl
- UIUtil.GetBackgroundUrl
- UIUtil.SetIconById
- UIUtil.SetLoaderTexture
- UIUtil.OpenPreviewTips
- UIUtil.SetPopupBtnGroup
- UIUtil.SetTagButtonSwitch
- UIUtil.InitAssetsTips
- list.itemRenderer
- UIUtil.ClickAssetItem
- UIUtil.GetFormatCount
- UIUtil.FormatCountType1
- UIUtil.FormatCountType2
- UIUtil.SetMoveText
- UIUtil.SetText
- UIUtil.SetBtnText
- UIUtil.ShowElementList
- elementList.itemRenderer
- UIUtil.ShowItemFrame
- UIUtil.CommonItemClickCallback
- UIUtil.ShowBuildingHeadBtn
- UIUtil.ShowHeadBtn
- UIUtil.ShowPlayerHead
- UIUtil.ShowCardTips
- UIUtil.ShowBuildingTips
- UIUtil.ShowStarList
- starList.itemRenderer
- UIUtil.ShowCardSkill
- UIUtil.SetExpeditionCardList
- list.itemRenderer
- UIUtil.ShowCardSkillDes
- UIUtil.SetObjectToUI
- UIUtil.AddEffectToUITop
- UIUtil.AddEffectToUIBottom
- UIUtil.SetEffectToUI
- UIUtil.SetBattleSpineEffectIndexByGrade
- UIUtil.SetBattleSpineEffectFlip
- UIUtil.SetCardBattleSpine
- UIUtil.InitSpineSetting
- UIUtil.SetCardShowSpineAutoAlpha
- UIUtil.SetCardShowTexture
- UIUtil.SetCardShowToLoader
- UIUtil.SetSfxClipInList
- UIUtil.GetHeadUrl
- UIUtil.SetHeadByFaceId
- UIUtil.SetPrice
- UIUtil.SetHolderCenter
- UIUtil.ChangeLoginScreenEffectIn
- UIUtil.ChangeLoginScreenEffectOut
- UIUtil.ChangeBattleScreenEffectIn
- UIUtil.ChangeBattleScreenEffectOut
- UIUtil.ShowTalkWord
- curTypingEffect.effectEndAction
- UIUtil.ClickOpenUrl
- UIUtil.DealClientVersionOutdated
- updateFunc
**Snippet:**
```lua
local UIUtil = {}
local _CACHED_RES_URL = {}

function UIUtil.GetResUrl(resStr)
  if _CACHED_RES_URL[resStr] then
    return _CACHED_RES_URL[resStr]
  end
  local resStrTable = Split(resStr, ":")
  if resStrTable and #resStrTable > 1 then
    _CACHED_RES_URL[resStr] = UIMgr:GetItemUrl(resStrTable[1], resStrTable[2])
```

---

## other/UpdateManager.lua.lua
**Functions:**
- UpdateManager.AddUpdateHandler
- UpdateManager.RemoveUpdateHandler
- UpdateManager.AddLateUpdateHandler
- UpdateManager.RemoveLateUpdateHandler
- UpdateManager.AddFixedUpdateHandler
- UpdateManager.RemoveFixedUpdateHandler
- UpdateManager.ClearAll
**Requires:**
- Handler
**Snippet:**
```lua
local LuaUpdateMgr = CS.LuaUpdateManager.Singleton
require("Handler")
local updateHandler = GetNewHandler()
local UpdateManager = {}

function UpdateManager.AddUpdateHandler(func, tableobj)
  updateHandler:AddHandle(1, func, tableobj)
end

function UpdateManager.RemoveUpdateHandler(func)
```

---

## other/Util.lua.lua
**Functions:**
- table.getMaxKey
- table.contain
- table.getLen
- table.randomSort
- table.randomx
- table.equal
- table.reverseTable
- table.clear
- table.keyof
- table.swapByIndex
- table.mapKey2Array
- table.map2Array
- table.appendTail
- math.round
- string.getByteCount
- string.trim
- string.isEmptyOrNil
- string.formatNum
- print
- printWarning
- printError
- Split
- ParseConfigStr
- T
- T_S
- PrintTable
- _dump
- CopyOne
- SimpleCopy
- CompareNum
- GetAddAttrList
- GetConfigItemList
- GetStageRewardShow
- MergeTable
- MergeTableAttributes
- IsNil
- FormatUin
- FormatOpenId
- FormatValidateNum
- FormatStrByLen
- GetPreciseDecimal
- DicToTable
- DataTableToTable
- ListToTable
- GetBuyExpend
- GetDiamondConvertValue
- LevelIsWithTheRange
- PowerRankIsWithTheRange
- GetActivityWeight
- GetHomeRedDotSort
- Decimal2Binary
- GetDefaultPlatformFPSLevel
- GetDefaultScreenAdaptRatio
- NumberByCommaStyle
- ResetFiveStamp
**Snippet:**
```lua
local type = type
local s_sub = string.sub
local s_find = string.find
local s_len = string.len
local s_format = string.format
local t_concat = table.concat
local t_sort = table.sort
local pairs = pairs
local tostring = tostring

```

---

## other/Utility.lua.lua
**Functions:**
- _G.tableToString
- _dump
- _G.GetDivideStringList
**Snippet:**
```lua
local type = type

function _G.tableToString(t)
  local string_format = string.format
  local string_rep = string.rep
  local address = {}
  if "userdata" == type(t) then
    return tableToString(getmetatable(t))
  end
  if "table" ~= type(t) then
```

---

## other/VertexPath.lua.lua
**Functions:**
- VertexPath:__ctor
- VertexPath:__delete
- VertexPath:GetPointAtTime
- VertexPath:GetDirectionAtTime
- VertexPath:GetPoint
- VertexPath:GetPointAtDistance
- VertexPath:GetDirectionAtDistance
- VertexPath:GetClosestPointOnPath
- VertexPath:GetClosestDistanceAlongPath
- VertexPath:GetNumPoints
- VertexPath:DrawGizmos
**Requires:**
- Create
**Snippet:**
```lua
require("Create")
local VertexPath = Create("VertexPath")
EndOfPathInstruction = {
  LOOP = "LOOP",
  REVERSE = "REVERSE",
  STOP = "STOP"
}
local Clamp01 = function(val)
  return math.min(1, math.max(0, val))
end
```

---

## other/WatchWindow.lua.lua
**Functions:**
- WatchWindow.OnInit
- WatchWindow.InitAllTabList
- list.itemRenderer
- WatchWindow.ClearNew
- WatchWindow.GetAllSpecialFashion
- WatchWindow.SetSelectCardFirst
- WatchWindow.ShowMask
- WatchWindow.UpdateTextDisplay
- WatchWindow.InitList
- HeadList.itemRenderer
- WatchWindow.GetCardListByTime
- WatchWindow.SetChangeFashion
- list.itemRenderer
- WatchWindow.SetCardInfo
- list.itemRenderer
- WatchWindow.ClearShowInfo
- WatchWindow.InitBtn
- WatchWindow.OnClose
**Requires:**
- Watch_WatchWindowByName
**Snippet:**
```lua
require("Watch_WatchWindowByName")
local WatchWindow = {}
local uis, contentPane, cardId, curShowIndex, infoFaceId, lastChoice, isPlayUp, newFashion, sortInverted, sortCardList, reverseCardList, jumpTb, showId
local maxLen = 5
local curListId

function WatchWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.WatchWindow.package, WinResConfig.WatchWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
```

---

## other/Watch_BatchRegionByName.lua.lua
**Functions:**
- GetWatch_BatchRegionUis
**Snippet:**
```lua
function GetWatch_BatchRegionUis(ui)
  local uis = {}
  
  uis.CardList = ui:GetChild("CardList")
  uis.root = ui
  return uis
end
```

---

## other/Watch_Batch_CardAddBtnByName.lua.lua
**Functions:**
- GetWatch_Batch_CardAddBtnUis
**Snippet:**
```lua
function GetWatch_Batch_CardAddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Watch_Batch_CardByName.lua.lua
**Functions:**
- GetWatch_Batch_CardUis
**Requires:**
- Watch_Batch_CardPicByName
**Snippet:**
```lua
require("Watch_Batch_CardPicByName")

function GetWatch_Batch_CardUis(ui)
  local uis = {}
  uis.CardPic = GetWatch_Batch_CardPicUis(ui:GetChild("CardPic"))
  uis.AddBtn = ui:GetChild("AddBtn")
  uis.DelBtn = ui:GetChild("DelBtn")
  uis.choiceCtr = ui:GetController("choice")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## other/Watch_Batch_CardClothesByName.lua.lua
**Functions:**
- GetWatch_Batch_CardClothesUis
**Snippet:**
```lua
function GetWatch_Batch_CardClothesUis(ui)
  local uis = {}
  
  uis.HeadList = ui:GetChild("HeadList")
  uis.root = ui
  return uis
end
```

---

## other/Watch_Batch_CardClothesHeadBtnByName.lua.lua
**Functions:**
- GetWatch_Batch_CardClothesHeadBtnUis
**Requires:**
- Watch_Batch_CardClothesHeadPicByName
**Snippet:**
```lua
require("Watch_Batch_CardClothesHeadPicByName")

function GetWatch_Batch_CardClothesHeadBtnUis(ui)
  local uis = {}
  uis.CardHeadPic = GetWatch_Batch_CardClothesHeadPicUis(ui:GetChild("CardHeadPic"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
```

---

## other/Watch_Batch_CardClothesHeadPicByName.lua.lua
**Functions:**
- GetWatch_Batch_CardClothesHeadPicUis
**Snippet:**
```lua
function GetWatch_Batch_CardClothesHeadPicUis(ui)
  local uis = {}
  
  uis.HeadLoader = ui:GetChild("HeadLoader")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## other/Watch_Batch_CardDelBtnByName.lua.lua
**Functions:**
- GetWatch_Batch_CardDelBtnUis
**Snippet:**
```lua
function GetWatch_Batch_CardDelBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Watch_Batch_CardEmptyByName.lua.lua
**Functions:**
- GetWatch_Batch_CardEmptyUis
**Snippet:**
```lua
function GetWatch_Batch_CardEmptyUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Watch_Batch_CardPicByName.lua.lua
**Functions:**
- GetWatch_Batch_CardPicUis
**Snippet:**
```lua
function GetWatch_Batch_CardPicUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## other/Watch_Batch_WordByName.lua.lua
**Functions:**
- GetWatch_Batch_WordUis
**Snippet:**
```lua
function GetWatch_Batch_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Watch_CardHeadBtnByName.lua.lua
**Functions:**
- GetWatch_CardHeadBtnUis
**Requires:**
- Watch_CardHeadPicByName
- Watch_Special_SignByName
- Watch_Special_LockByName
**Snippet:**
```lua
require("Watch_CardHeadPicByName")
require("Watch_Special_SignByName")
require("Watch_Special_LockByName")

function GetWatch_CardHeadBtnUis(ui)
  local uis = {}
  uis.CardHeadPic = GetWatch_CardHeadPicUis(ui:GetChild("CardHeadPic"))
  uis.CardNameTxt = ui:GetChild("CardNameTxt")
  uis.Sign = GetWatch_Special_SignUis(ui:GetChild("Sign"))
  uis.Lock = GetWatch_Special_LockUis(ui:GetChild("Lock"))
```

---

## other/Watch_CardHeadByName.lua.lua
**Functions:**
- GetWatch_CardHeadUis
**Snippet:**
```lua
function GetWatch_CardHeadUis(ui)
  local uis = {}
  
  uis.CardHeadBtn = ui:GetChild("CardHeadBtn")
  uis.root = ui
  return uis
end
```

---

## other/Watch_CardHeadPicByName.lua.lua
**Functions:**
- GetWatch_CardHeadPicUis
**Snippet:**
```lua
function GetWatch_CardHeadPicUis(ui)
  local uis = {}
  
  uis.CardLoader = ui:GetChild("CardLoader")
  uis.root = ui
  return uis
end
```

---

## other/Watch_CardInfoByName.lua.lua
**Functions:**
- GetWatch_CardInfoUis
**Requires:**
- Watch_Batch_CardClothesByName
**Snippet:**
```lua
require("Watch_Batch_CardClothesByName")

function GetWatch_CardInfoUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.ClothesNameTxt = ui:GetChild("ClothesNameTxt")
  uis.CardClothes = GetWatch_Batch_CardClothesUis(ui:GetChild("CardClothes"))
  uis.CardInfoLookBtn = ui:GetChild("CardInfoLookBtn")
  uis.c1Ctr = ui:GetController("c1")
```

---

## other/Watch_CardInfoLookBtnByName.lua.lua
**Functions:**
- GetWatch_CardInfoLookBtnUis
**Snippet:**
```lua
function GetWatch_CardInfoLookBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Watch_ClothesBtnByName.lua.lua
**Functions:**
- GetWatch_ClothesBtnUis
**Snippet:**
```lua
function GetWatch_ClothesBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Watch_ClothesModularByName.lua.lua
**Functions:**
- GetWatch_ClothesModularUis
**Requires:**
- Watch_ClothesTipsByName
**Snippet:**
```lua
require("Watch_ClothesTipsByName")

function GetWatch_ClothesModularUis(ui)
  local uis = {}
  uis.PicList = ui:GetChild("PicList")
  uis.UseBtn = ui:GetChild("UseBtn")
  uis.ClothesTips = GetWatch_ClothesTipsUis(ui:GetChild("ClothesTips"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## other/Watch_ClothesPicBtnByName.lua.lua
**Functions:**
- GetWatch_ClothesPicBtnUis
**Requires:**
- Watch_ClothesPicByName
**Snippet:**
```lua
require("Watch_ClothesPicByName")

function GetWatch_ClothesPicBtnUis(ui)
  local uis = {}
  uis.ClothesPic = GetWatch_ClothesPicUis(ui:GetChild("ClothesPic"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.LineImage = ui:GetChild("LineImage")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
```

---

## other/Watch_ClothesPicByName.lua.lua
**Functions:**
- GetWatch_ClothesPicUis
**Snippet:**
```lua
function GetWatch_ClothesPicUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other/Watch_ClothesSetByName.lua.lua
**Functions:**
- GetWatch_ClothesSetUis
**Requires:**
- Watch_PicByName
- Watch_Batch_CardEmptyByName
- Watch_ClothesModularByName
- Watch_SetByName
- Watch_CardInfoByName
**Snippet:**
```lua
require("Watch_PicByName")
require("Watch_Batch_CardEmptyByName")
require("Watch_ClothesModularByName")
require("Watch_SetByName")
require("Watch_CardInfoByName")

function GetWatch_ClothesSetUis(ui)
  local uis = {}
  uis.Pic = GetWatch_PicUis(ui:GetChild("Pic"))
  uis.CardEmpty = GetWatch_Batch_CardEmptyUis(ui:GetChild("CardEmpty"))
```

---

## other/Watch_ClothesTipsByName.lua.lua
**Functions:**
- GetWatch_ClothesTipsUis
**Snippet:**
```lua
function GetWatch_ClothesTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Watch_PicByName.lua.lua
**Functions:**
- GetWatch_PicUis
**Snippet:**
```lua
function GetWatch_PicUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.PicHolder = ui:GetChild("PicHolder")
  uis.root = ui
  return uis
end
```

---

## other/Watch_PositionBtnByName.lua.lua
**Functions:**
- GetWatch_PositionBtnUis
**Snippet:**
```lua
function GetWatch_PositionBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Watch_SetByName.lua.lua
**Functions:**
- GetWatch_SetUis
**Requires:**
- Watch_BatchRegionByName
- Watch_Batch_WordByName
**Snippet:**
```lua
require("Watch_BatchRegionByName")
require("Watch_Batch_WordByName")

function GetWatch_SetUis(ui)
  local uis = {}
  uis.HeadList = ui:GetChild("HeadList")
  uis.BatchRegion = GetWatch_BatchRegionUis(ui:GetChild("BatchRegion"))
  uis.SortBtn = ui:GetChild("SortBtn")
  uis.PositionBtn = ui:GetChild("PositionBtn")
  uis.ClothesBtn = ui:GetChild("ClothesBtn")
```

---

## other/Watch_SortBtnByName.lua.lua
**Functions:**
- GetWatch_SortBtnUis
**Snippet:**
```lua
function GetWatch_SortBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other/Watch_Special_LockByName.lua.lua
**Functions:**
- GetWatch_Special_LockUis
**Requires:**
- Watch_Special_MoveWord1ByName
**Snippet:**
```lua
require("Watch_Special_MoveWord1ByName")

function GetWatch_Special_LockUis(ui)
  local uis = {}
  uis.MoveWord = GetWatch_Special_MoveWord1Uis(ui:GetChild("MoveWord"))
  uis.root = ui
  return uis
end
```

---

## other/Watch_Special_MoveWord1ByName.lua.lua
**Functions:**
- GetWatch_Special_MoveWord1Uis
**Snippet:**
```lua
function GetWatch_Special_MoveWord1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Watch_Special_MoveWordByName.lua.lua
**Functions:**
- GetWatch_Special_MoveWordUis
**Snippet:**
```lua
function GetWatch_Special_MoveWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other/Watch_Special_SignByName.lua.lua
**Functions:**
- GetWatch_Special_SignUis
**Requires:**
- Watch_Special_MoveWordByName
**Snippet:**
```lua
require("Watch_Special_MoveWordByName")

function GetWatch_Special_SignUis(ui)
  local uis = {}
  uis.MoveWord = GetWatch_Special_MoveWordUis(ui:GetChild("MoveWord"))
  uis.root = ui
  return uis
end
```

---

## other/Watch_Special_TabBtnByName.lua.lua
**Functions:**
- GetWatch_Special_TabBtnUis
**Snippet:**
```lua
function GetWatch_Special_TabBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
end
```

---

## other/Watch_WatchByName.lua.lua
**Functions:**
- GetWatch_WatchUis
**Requires:**
- CommonResource_BackGroundByName
- Watch_ClothesSetByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Watch_ClothesSetByName")
require("CommonResource_CurrencyReturnByName")

function GetWatch_WatchUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.ClothesSet = GetWatch_ClothesSetUis(ui:GetChild("ClothesSet"))
  uis.CurrencyReturn = GetCommonResource_CurrencyReturnUis(ui:GetChild("CurrencyReturn"))
  uis.root = ui
```

---

## other/Watch_WatchWindowByName.lua.lua
**Functions:**
- GetWatch_WatchWindowUis
**Requires:**
- Watch_WatchByName
**Snippet:**
```lua
require("Watch_WatchByName")

function GetWatch_WatchWindowUis(ui)
  local uis = {}
  uis.Main = GetWatch_WatchUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other/World.lua.lua
**Functions:**
- World:__ctor
- World:onInit
- World:initCollideManager
- World:addBody
- World:removeBody
- World:checkSleep
- World:preSolve
- World:solve
- World:step
- World:drawgizmos
**Snippet:**
```lua
local World = Create("World")

function World:__ctor(onCollidingCallback, onCollideCallback, onSeparatedCallback)
  self.bodies = nil
  self.gravityX = 0
  self.gravityY = 0
  self.forceX = 0
  self.forceY = 0
  self.allowSleep = true
  self.timeToSleep = 0.5
```

---
