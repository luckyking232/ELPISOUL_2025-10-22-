# other_A

## other_A/AccountTipsWindow.lua.lua
**Functions:**
- AccountTipsWindow.ReInitData
- AccountTipsWindow.OnInit
- AccountTipsWindow.UpdateInfo
- AccountTipsWindow.ResetPassword
- AccountTipsWindow.ReturnToLogin
- AccountTipsWindow.ReviewProtocol
- AccountTipsWindow.InitBtn
- AccountTipsWindow.Close
- AccountTipsWindow.OnClose
**Requires:**
- ActorInfo_AccountTipsWindowByName
**Snippet:**
```lua
require("ActorInfo_AccountTipsWindowByName")
local AccountTipsWindow = {}
local uis, contentPane, oprType

function AccountTipsWindow.ReInitData()
end

function AccountTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.AccountTipsWindow.package, WinResConfig.AccountTipsWindow.comName, function(com)
    contentPane = com
```

---

## other_A/ActorData.lua.lua
**Functions:**
- ActorData.ClearData
- ActorData.SaveActorData
- ActorData.UpdateActorInfo
- ActorData.SaveFaceId
- ActorData.SaveActorHead
- ActorData.SaveItemData
- ActorData.SaveCardData
- ActorData.SetCardSyncKey
- ActorData.SetBadgeSyncKey
- ActorData.SaveAllTeamData
- ActorData.SaveStoryUnlockData
- ActorData.SaveGuideProgress
- ActorData.UpdateGuideProgress
- ActorData.SaveOpenFeature
- ActorData.UpdateOpenFeature
- ActorData.UpdateItem
- ActorData.UpdateCard
- ActorData.AddCard
- ActorData.DeleteCard
- ActorData.UpdateOneItem
- ActorData.DeleteOneItem
- ActorData.GetItemInfoById
- ActorData.GetItemInfoByUid
- ActorData.GetItemCount
- ActorData.GetItemCountByUid
- ActorData.GetItemCountByExpire
- ActorData.GetItemUid
- ActorData.GetItemListByType
- ActorData.InitHeadNew
- ActorData.CanHeadIsNew
- ActorData.SaveHeadNew
- ActorData.SaveBadgeData
- ActorData.UpdateOneBadgeData
- ActorData.UpdateBadgeNew
- ActorData.GetAllBadge
- ActorData.GetBadgeInfoByUid
- ActorData.GetBadgeCount
- ActorData.DeleteOneBadgeData
- ActorData.SaveSpecialFashion
- ActorData.CanShowSpecialFashion
- ActorData.DeleteSpecialFashion
- ActorData.GetItemSyncKey
- ActorData.GetCardSyncKey
- ActorData.GetBadgeSyncKey
- ActorData.GetActorInfo
- ActorData.GetOpenId
- ActorData.GetUin
- ActorData.GetLevel
- ActorData.GetExp
- ActorData.GetPower
- ActorData.GetName
- ActorData.GetFaceId
- ActorData.GetHeadInfo
- ActorData.GetCreateStamp
- ActorData.GetChangNameCount
- ActorData.GetBirthday
- ActorData.GetExpMax
- ActorData.GetGuideInfo
- ActorData.GetCardList
- ActorData.GetItems
- ActorData.GetAllTeam
- ActorData.GetEnergyMax
- ActorData.GetLoginDays
- ActorData.GetStoryList
- ActorData.GetFeatureIsUnlock
- ActorData.GetRandomBubbleSoundId
- ActorData.GetRandomName
- ActorData.InitFashionPosInfo
- ActorData.GetFashionPosInfoByIndex
- ActorData.UpdateFashionPosInfo
- ActorData.RemoveFashionPosInfo
- ActorData.AddFashionPosInfo
**Snippet:**
```lua
ActorData = {}
local _info = {}
local _itemInfo = {}
local _cardList = {}
local _badgeList = {}
local _cardTeamList = {}
local _badgeSyncKey = 0
local _itemSyncKey = 0
local _cardSyncKey = 0
local _storyList = {}
```

---

## other_A/ActorInfoWindow.lua.lua
**Functions:**
- ActorInfoWindow.ReInitData
- ActorInfoWindow.RefreshWindow
- ActorInfoWindow.OnInit
- ActorInfoWindow.InitTabListData
- ActorInfoWindow.UpdateInfo
- ActorInfoWindow.UpdateTabList
- ActorInfoWindow.UpdateTab
- ActorInfoWindow.TouchTab
- ActorInfoWindow.UpdatePanel
- ActorInfoWindow.UpdateAccount
- ActorInfoWindow.UpdateGame
- ActorInfoWindow.UpdateBattle
- ActorInfoWindow.UpdateSound
- ActorInfoWindow.UpdateTipsList
- ActorInfoWindow.UpdateSetTips
- burstShowList.itemRenderer
- languageList.itemRenderer
- ActorInfoWindow.UpdateLanguageListBtn
- ActorInfoWindow.UpdateRatioListBtn
- ActorInfoWindow.UpdateSwitchBtn
- ActorInfoWindow.TouchSwitchBtn
- ActorInfoWindow.InitBtn
- ActorInfoWindow.OnShown
- ActorInfoWindow.OnHide
- ActorInfoWindow.OnClose
- ActorInfoWindow.HandleMessage
**Requires:**
- ActorInfo_ActorInfoWindowByName
- ActorInfo_SetTipsByName
**Snippet:**
```lua
require("ActorInfo_ActorInfoWindowByName")
local ActorInfoWindow = {}
local uis, contentPane, _tab_list, curSettingList, curSettingType, openSettingType, jumpTb
local cachedHandByKey = {}

function ActorInfoWindow.ReInitData()
end

function ActorInfoWindow.RefreshWindow()
  curSettingType = nil
```

---

## other_A/ActorInfo_AccountTipsByName.lua.lua
**Functions:**
- GetActorInfo_AccountTipsUis
**Requires:**
- ActorInfo_PasswordModificationByName
- ActorInfo_ReturnLoginByName
- ActorInfo_ConcealByName
**Snippet:**
```lua
require("ActorInfo_PasswordModificationByName")
require("ActorInfo_ReturnLoginByName")
require("ActorInfo_ConcealByName")

function GetActorInfo_AccountTipsUis(ui)
  local uis = {}
  uis.PasswordModification = GetActorInfo_PasswordModificationUis(ui:GetChild("PasswordModification"))
  uis.ReturnLogin = GetActorInfo_ReturnLoginUis(ui:GetChild("ReturnLogin"))
  uis.Conceal = GetActorInfo_ConcealUis(ui:GetChild("Conceal"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## other_A/ActorInfo_AccountTipsWindowByName.lua.lua
**Functions:**
- GetActorInfo_AccountTipsWindowUis
**Requires:**
- CommonResource_PopupBgByName
- ActorInfo_AccountTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActorInfo_AccountTipsByName")

function GetActorInfo_AccountTipsWindowUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.AccountTips = GetActorInfo_AccountTipsUis(ui:GetChild("AccountTips"))
  uis.root = ui
  return uis
```

---

## other_A/ActorInfo_Account_1ByName.lua.lua
**Functions:**
- GetActorInfo_Account_1Uis
**Snippet:**
```lua
function GetActorInfo_Account_1Uis(ui)
  local uis = {}
  
  uis.stateCtr = ui:GetController("state")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_Account_2ByName.lua.lua
**Functions:**
- GetActorInfo_Account_2Uis
**Snippet:**
```lua
function GetActorInfo_Account_2Uis(ui)
  local uis = {}
  
  uis.stateCtr = ui:GetController("state")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_Account_3ByName.lua.lua
**Functions:**
- GetActorInfo_Account_3Uis
**Snippet:**
```lua
function GetActorInfo_Account_3Uis(ui)
  local uis = {}
  
  uis.stateCtr = ui:GetController("state")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_Account_4ByName.lua.lua
**Functions:**
- GetActorInfo_Account_4Uis
**Snippet:**
```lua
function GetActorInfo_Account_4Uis(ui)
  local uis = {}
  
  uis.stateCtr = ui:GetController("state")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_ActorInfoByName.lua.lua
**Functions:**
- GetActorInfo_ActorInfoUis
**Requires:**
- CommonResource_BackGroundByName
- ActorInfo_GameSetByName
- ActorInfo_TabRegionByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActorInfo_GameSetByName")
require("ActorInfo_TabRegionByName")
require("CommonResource_CurrencyReturnByName")

function GetActorInfo_ActorInfoUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.GameSet = GetActorInfo_GameSetUis(ui:GetChild("GameSet"))
  uis.TabRegion = GetActorInfo_TabRegionUis(ui:GetChild("TabRegion"))
```

---

## other_A/ActorInfo_ActorInfoWindowByName.lua.lua
**Functions:**
- GetActorInfo_ActorInfoWindowUis
**Requires:**
- ActorInfo_ActorInfoByName
**Snippet:**
```lua
require("ActorInfo_ActorInfoByName")

function GetActorInfo_ActorInfoWindowUis(ui)
  local uis = {}
  uis.Main = GetActorInfo_ActorInfoUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_AdaptBtnByName.lua.lua
**Functions:**
- GetActorInfo_AdaptBtnUis
**Snippet:**
```lua
function GetActorInfo_AdaptBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_AutoBtnByName.lua.lua
**Functions:**
- GetActorInfo_AutoBtnUis
**Snippet:**
```lua
function GetActorInfo_AutoBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_BattleInfoByName.lua.lua
**Functions:**
- GetActorInfo_BattleInfoUis
**Requires:**
- CommonResource_PopupBgByName
- ActorInfo_BattleInfoTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActorInfo_BattleInfoTipsByName")

function GetActorInfo_BattleInfoUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.BattleInfoTips = GetActorInfo_BattleInfoTipsUis(ui:GetChild("BattleInfoTips"))
  uis.root = ui
  return uis
```

---

## other_A/ActorInfo_BattleInfoCloseBtnByName.lua.lua
**Functions:**
- GetActorInfo_BattleInfoCloseBtnUis
**Snippet:**
```lua
function GetActorInfo_BattleInfoCloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_BattleInfoTips1ByName.lua.lua
**Functions:**
- GetActorInfo_BattleInfoTips1Uis
**Requires:**
- ActorInfo_SetIconByName
- ActorInfo_WeatherByName
- ActorInfo_LanguageByName
- ActorInfo_BurstShowByName
**Snippet:**
```lua
require("ActorInfo_SetIconByName")
require("ActorInfo_WeatherByName")
require("ActorInfo_LanguageByName")
require("ActorInfo_BurstShowByName")

function GetActorInfo_BattleInfoTips1Uis(ui)
  local uis = {}
  uis.SetIcon = GetActorInfo_SetIconUis(ui:GetChild("SetIcon"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.VoiceSlider = ui:GetChild("VoiceSlider")
```

---

## other_A/ActorInfo_BattleInfoTipsByName.lua.lua
**Functions:**
- GetActorInfo_BattleInfoTipsUis
**Snippet:**
```lua
function GetActorInfo_BattleInfoTipsUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.SetTipsList = ui:GetChild("SetTipsList")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_BattleInfoWindowByName.lua.lua
**Functions:**
- GetActorInfo_BattleInfoWindowUis
**Requires:**
- ActorInfo_BattleInfoByName
**Snippet:**
```lua
require("ActorInfo_BattleInfoByName")

function GetActorInfo_BattleInfoWindowUis(ui)
  local uis = {}
  uis.Main = GetActorInfo_BattleInfoUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_Battle_1ByName.lua.lua
**Functions:**
- GetActorInfo_Battle_1Uis
**Snippet:**
```lua
function GetActorInfo_Battle_1Uis(ui)
  local uis = {}
  
  uis.stateCtr = ui:GetController("state")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_Battle_2ByName.lua.lua
**Functions:**
- GetActorInfo_Battle_2Uis
**Snippet:**
```lua
function GetActorInfo_Battle_2Uis(ui)
  local uis = {}
  
  uis.stateCtr = ui:GetController("state")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_Battle_3ByName.lua.lua
**Functions:**
- GetActorInfo_Battle_3Uis
**Snippet:**
```lua
function GetActorInfo_Battle_3Uis(ui)
  local uis = {}
  
  uis.stateCtr = ui:GetController("state")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_Battle_4ByName.lua.lua
**Functions:**
- GetActorInfo_Battle_4Uis
**Snippet:**
```lua
function GetActorInfo_Battle_4Uis(ui)
  local uis = {}
  
  uis.stateCtr = ui:GetController("state")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_Battle_5ByName.lua.lua
**Functions:**
- GetActorInfo_Battle_5Uis
**Snippet:**
```lua
function GetActorInfo_Battle_5Uis(ui)
  local uis = {}
  
  uis.stateCtr = ui:GetController("state")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_BurstShowBtnByName.lua.lua
**Functions:**
- GetActorInfo_BurstShowBtnUis
**Snippet:**
```lua
function GetActorInfo_BurstShowBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_BurstShowByName.lua.lua
**Functions:**
- GetActorInfo_BurstShowUis
**Snippet:**
```lua
function GetActorInfo_BurstShowUis(ui)
  local uis = {}
  
  uis.BurstShowList = ui:GetChild("BurstShowList")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_ConcealByName.lua.lua
**Functions:**
- GetActorInfo_ConcealUis
**Snippet:**
```lua
function GetActorInfo_ConcealUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.SureBtn = ui:GetChild("SureBtn")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_ConcealWordByName.lua.lua
**Functions:**
- GetActorInfo_ConcealWordUis
**Snippet:**
```lua
function GetActorInfo_ConcealWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_DayBtnByName.lua.lua
**Functions:**
- GetActorInfo_DayBtnUis
**Snippet:**
```lua
function GetActorInfo_DayBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_DuskBtnByName.lua.lua
**Functions:**
- GetActorInfo_DuskBtnUis
**Snippet:**
```lua
function GetActorInfo_DuskBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_GameSetByName.lua.lua
**Functions:**
- GetActorInfo_GameSetUis
**Requires:**
- ActorInfo_SetUIByName
**Snippet:**
```lua
require("ActorInfo_SetUIByName")

function GetActorInfo_GameSetUis(ui)
  local uis = {}
  uis.SetUI = GetActorInfo_SetUIUis(ui:GetChild("SetUI"))
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_Game_1ByName.lua.lua
**Functions:**
- GetActorInfo_Game_1Uis
**Snippet:**
```lua
function GetActorInfo_Game_1Uis(ui)
  local uis = {}
  
  uis.stateCtr = ui:GetController("state")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_Game_2ByName.lua.lua
**Functions:**
- GetActorInfo_Game_2Uis
**Snippet:**
```lua
function GetActorInfo_Game_2Uis(ui)
  local uis = {}
  
  uis.stateCtr = ui:GetController("state")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_Game_3ByName.lua.lua
**Functions:**
- GetActorInfo_Game_3Uis
**Snippet:**
```lua
function GetActorInfo_Game_3Uis(ui)
  local uis = {}
  
  uis.stateCtr = ui:GetController("state")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_Game_4ByName.lua.lua
**Functions:**
- GetActorInfo_Game_4Uis
**Snippet:**
```lua
function GetActorInfo_Game_4Uis(ui)
  local uis = {}
  
  uis.stateCtr = ui:GetController("state")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_Game_5ByName.lua.lua
**Functions:**
- GetActorInfo_Game_5Uis
**Snippet:**
```lua
function GetActorInfo_Game_5Uis(ui)
  local uis = {}
  
  uis.stateCtr = ui:GetController("state")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_Game_6ByName.lua.lua
**Functions:**
- GetActorInfo_Game_6Uis
**Snippet:**
```lua
function GetActorInfo_Game_6Uis(ui)
  local uis = {}
  
  uis.stateCtr = ui:GetController("state")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_Game_7ByName.lua.lua
**Functions:**
- GetActorInfo_Game_7Uis
**Snippet:**
```lua
function GetActorInfo_Game_7Uis(ui)
  local uis = {}
  
  uis.stateCtr = ui:GetController("state")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_Game_8ByName.lua.lua
**Functions:**
- GetActorInfo_Game_8Uis
**Snippet:**
```lua
function GetActorInfo_Game_8Uis(ui)
  local uis = {}
  
  uis.stateCtr = ui:GetController("state")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_Game_9ByName.lua.lua
**Functions:**
- GetActorInfo_Game_9Uis
**Snippet:**
```lua
function GetActorInfo_Game_9Uis(ui)
  local uis = {}
  
  uis.stateCtr = ui:GetController("state")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_Green_B_BtnByName.lua.lua
**Functions:**
- GetActorInfo_Green_B_BtnUis
**Snippet:**
```lua
function GetActorInfo_Green_B_BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_Green_S_BtnByName.lua.lua
**Functions:**
- GetActorInfo_Green_S_BtnUis
**Snippet:**
```lua
function GetActorInfo_Green_S_BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_LanguageBtnByName.lua.lua
**Functions:**
- GetActorInfo_LanguageBtnUis
**Snippet:**
```lua
function GetActorInfo_LanguageBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_LanguageByName.lua.lua
**Functions:**
- GetActorInfo_LanguageUis
**Snippet:**
```lua
function GetActorInfo_LanguageUis(ui)
  local uis = {}
  
  uis.LanguageList = ui:GetChild("LanguageList")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_NightBtnByName.lua.lua
**Functions:**
- GetActorInfo_NightBtnUis
**Snippet:**
```lua
function GetActorInfo_NightBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_PasswordByName.lua.lua
**Functions:**
- GetActorInfo_PasswordUis
**Snippet:**
```lua
function GetActorInfo_PasswordUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_PasswordModificationByName.lua.lua
**Functions:**
- GetActorInfo_PasswordModificationUis
**Snippet:**
```lua
function GetActorInfo_PasswordModificationUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.PasswordList = ui:GetChild("PasswordList")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.SureBtn = ui:GetChild("SureBtn")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_ReturnLoginByName.lua.lua
**Functions:**
- GetActorInfo_ReturnLoginUis
**Snippet:**
```lua
function GetActorInfo_ReturnLoginUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.SureBtn = ui:GetChild("SureBtn")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_SetIconByName.lua.lua
**Functions:**
- GetActorInfo_SetIconUis
**Requires:**
- ActorInfo_Game_1ByName
- ActorInfo_Game_2ByName
- ActorInfo_Game_3ByName
- ActorInfo_Game_4ByName
- ActorInfo_Game_5ByName
- ActorInfo_Game_6ByName
- ActorInfo_Game_7ByName
- ActorInfo_Game_8ByName
- ActorInfo_Game_9ByName
- ActorInfo_Battle_1ByName
- ActorInfo_Battle_2ByName
- ActorInfo_Battle_3ByName
- ActorInfo_Battle_4ByName
- ActorInfo_Battle_5ByName
- ActorInfo_Voice_1ByName
- ActorInfo_Voice_2ByName
- ActorInfo_Voice_3ByName
- ActorInfo_Account_1ByName
- ActorInfo_Account_2ByName
- ActorInfo_Account_3ByName
- ActorInfo_Account_4ByName
**Snippet:**
```lua
require("ActorInfo_Game_1ByName")
require("ActorInfo_Game_2ByName")
require("ActorInfo_Game_3ByName")
require("ActorInfo_Game_4ByName")
require("ActorInfo_Game_5ByName")
require("ActorInfo_Game_6ByName")
require("ActorInfo_Game_7ByName")
require("ActorInfo_Game_8ByName")
require("ActorInfo_Game_9ByName")
require("ActorInfo_Battle_1ByName")
```

---

## other_A/ActorInfo_SetSwitchBtnByName.lua.lua
**Functions:**
- GetActorInfo_SetSwitchBtnUis
**Snippet:**
```lua
function GetActorInfo_SetSwitchBtnUis(ui)
  local uis = {}
  
  uis.CloseTxt = ui:GetChild("CloseTxt")
  uis.OpenTxt = ui:GetChild("OpenTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_SetTipsByName.lua.lua
**Functions:**
- GetActorInfo_SetTipsUis
**Requires:**
- ActorInfo_SetIconByName
- ActorInfo_WeatherByName
- ActorInfo_LanguageByName
- ActorInfo_BurstShowByName
**Snippet:**
```lua
require("ActorInfo_SetIconByName")
require("ActorInfo_WeatherByName")
require("ActorInfo_LanguageByName")
require("ActorInfo_BurstShowByName")

function GetActorInfo_SetTipsUis(ui)
  local uis = {}
  uis.SetIcon = GetActorInfo_SetIconUis(ui:GetChild("SetIcon"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.VoiceSlider = ui:GetChild("VoiceSlider")
```

---

## other_A/ActorInfo_SetUIByName.lua.lua
**Functions:**
- GetActorInfo_SetUIUis
**Snippet:**
```lua
function GetActorInfo_SetUIUis(ui)
  local uis = {}
  
  uis.SetTipsList = ui:GetChild("SetTipsList")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_TabBtnBgByName.lua.lua
**Functions:**
- GetActorInfo_TabBtnBgUis
**Snippet:**
```lua
function GetActorInfo_TabBtnBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_TabBtnByName.lua.lua
**Functions:**
- GetActorInfo_TabBtnUis
**Requires:**
- ActorInfo_TabBtnBgByName
**Snippet:**
```lua
require("ActorInfo_TabBtnBgByName")

function GetActorInfo_TabBtnUis(ui)
  local uis = {}
  uis.TabBtnBg = GetActorInfo_TabBtnBgUis(ui:GetChild("TabBtnBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## other_A/ActorInfo_TabRegionByName.lua.lua
**Functions:**
- GetActorInfo_TabRegionUis
**Snippet:**
```lua
function GetActorInfo_TabRegionUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_VoiceSliderByName.lua.lua
**Functions:**
- GetActorInfo_VoiceSliderUis
**Snippet:**
```lua
function GetActorInfo_VoiceSliderUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_VoiceSlider_gripByName.lua.lua
**Functions:**
- GetActorInfo_VoiceSlider_gripUis
**Snippet:**
```lua
function GetActorInfo_VoiceSlider_gripUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_Voice_1ByName.lua.lua
**Functions:**
- GetActorInfo_Voice_1Uis
**Snippet:**
```lua
function GetActorInfo_Voice_1Uis(ui)
  local uis = {}
  
  uis.stateCtr = ui:GetController("state")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_Voice_2ByName.lua.lua
**Functions:**
- GetActorInfo_Voice_2Uis
**Snippet:**
```lua
function GetActorInfo_Voice_2Uis(ui)
  local uis = {}
  
  uis.stateCtr = ui:GetController("state")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_Voice_3ByName.lua.lua
**Functions:**
- GetActorInfo_Voice_3Uis
**Snippet:**
```lua
function GetActorInfo_Voice_3Uis(ui)
  local uis = {}
  
  uis.stateCtr = ui:GetController("state")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorInfo_WeatherByName.lua.lua
**Functions:**
- GetActorInfo_WeatherUis
**Snippet:**
```lua
function GetActorInfo_WeatherUis(ui)
  local uis = {}
  
  uis.AutoBtn = ui:GetChild("AutoBtn")
  uis.DayBtn = ui:GetChild("DayBtn")
  uis.DuskBtn = ui:GetChild("DuskBtn")
  uis.NightBtn = ui:GetChild("NightBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## other_A/ActorInfo_White_S_BtnByName.lua.lua
**Functions:**
- GetActorInfo_White_S_BtnUis
**Snippet:**
```lua
function GetActorInfo_White_S_BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other_A/ActorMgr.lua.lua
**Functions:**
- ActorMgr.EnterHome
- ActorMgr.ReqNecessaryInfo
- ActorMgr.AddNeedLoadMsg
- ActorMgr.ClearCacheData
- ActorMgr.ShowUin
**Snippet:**
```lua
ActorMgr = {necessaryInfoSuccess = false}

function ActorMgr.EnterHome()
  local callBack = function()
    SettingUtil.UpdateFPS()
    if GuideMgr.jumpNewHand == true or GuideMgr.NeedShowSpecialGuide() == false then
      if false == UIMgr:IsWindowInList(WinResConfig.HomeWindow.name) then
        ld("Home", function()
          UIUtil.ChangeLoginScreenEffectIn(function()
            OpenWindow(WinResConfig.HomeWindow.name, UILayer.MainUI)
```

---

## other_A/ActorScriptList.lua.lua
**Requires:**
- ActorMgr
- ActorData
- ActorService
**Snippet:**
```lua
local require = require
require("ActorMgr")
require("ActorData")
if IsBattleServer ~= true then
  require("ActorService")
end
```

---

## other_A/ActorService.lua.lua
**Functions:**
- ActorService.Init
- ActorService.CreateActorReq
- ActorService.DealCreateActorRsp
- ActorService.GetActorInfoReq
- ActorService.DealGetActorInfoRsp
- ActorService.ChangeNameReq
- ActorService.DealChangeNameRsp
- ActorService.ChangeFaceReq
- ActorService.DealChangeFaceRsp
- ActorService.ChangeHeadReq
- ActorService.DealChangeHeadRsp
- ActorService.GetItemsReq
- ActorService.DealGetItemsRsp
- ActorService.GetAllCardsReq
- ActorService.DealGetAllCardsRsp
- ActorService.GetAllBadgesReq
- ActorService.DealGetAllBadgesRsp
- ActorService.GetCardAllTeamReq
- ActorService.DealGetCardAllTeamRsp
- ActorService.SyncItemsReq
- ActorService.DealSyncItemsRsp
- ActorService.GetOtherDetailInfoReq
- ActorService.DealGetOtherDetailInfoRsp
- ActorService.GetSelfDetailInfoReq
- ActorService.DealGetSelfDetailInfoRsp
- ActorService.SetProfileDisplayCardsReq
- ActorService.DealSetProfileDisplayCardsRsp
- ActorService.SetProfileShowResourceReq
- ActorService.DealSetProfileShowResourceRsp
- ActorService.SaveSettingsReq
- ActorService.DealSaveSettingsRsp
- ActorService.ReportOperateRecordReq
- ActorService.ReportOperateRecordRsp
- ActorService.GetOperateRecordReq
- ActorService.GetOperateRecordRsp
- ActorService.UseExchangeCodeReq
- ActorService.UseExchangeCodeRsp
- ActorService.ClientAbnormalReportReq
- ActorService.ClientAbnormalReportRsp
- ActorService.SetCardFashionShowReq
- ActorService.SetCardFashionShowRsp
- ActorService.GetGuideProgressReq
- ActorService.DealGetGuideProgressRsp
- ActorService.FinishGuideReq
- ActorService.DealFinishGuideRsp
- ActorService.CheckFeatureOpenReq
- ActorService.DealCheckFeatureOpenRsp
- ActorService.GetStoryListReq
- ActorService.DealGetStoryListRsp
- ActorService.DealCardUpdateNotify
- ActorService.DealActorInfoUpdateNotify
- ActorService.DealNewMessageNotify
- ActorService.DealMutedBySystemNotify
- ActorService.DealNewMailNotify
- ActorService.DealRelationChangedNotify
- ActorService.DealRelationDelApplicantNotify
- ActorService.DealGuildEventNotify
- ActorService.DealNewBadgeNotify
- ActorService.DealFashionAddNotify
- ActorService.DealActorGmRsp
- ActorService.DealEventNotifyRsp
- ActorService.ChangePasswordReq
- ActorService.DealChangePasswordRsp
- ActorService.DealNothing
- ActorService.BatchSyncResReq
- ActorService.DealBatchSyncResRsp
- ActorService.GetFriendDefenceFormationReq
- ActorService.GetFriendDefenceFormationRsp
- ActorService.SetBirthdayReq
- ActorService.SetBirthdayRsp
**Snippet:**
```lua
ActorService = {}

function ActorService.Init()
  Net.AddListener(Proto.MsgName.CreateActorRsp, ActorService.DealCreateActorRsp)
  Net.AddListener(Proto.MsgName.GetActorInfoRsp, ActorService.DealGetActorInfoRsp)
  Net.AddListener(Proto.MsgName.GetItemsRsp, ActorService.DealGetItemsRsp)
  Net.AddListener(Proto.MsgName.GetAllCardsRsp, ActorService.DealGetAllCardsRsp)
  Net.AddListener(Proto.MsgName.GetCardAllTeamRsp, ActorService.DealGetCardAllTeamRsp)
  Net.AddListener(Proto.MsgName.SyncItemsRsp, ActorService.DealSyncItemsRsp)
  Net.AddListener(Proto.MsgName.EventNotifyRsp, ActorService.DealEventNotifyRsp)
```

---

## other_A/AdventureData.lua.lua
**Functions:**
- AdventureData.ClearData
- AdventureData.GetMultiDropInfo
- AdventureData.SaveMultiDropInfo
- AdventureData.GetAllMultiDropInfo
- AdventureData.GetMultiDropConfig
- AdventureData.GetSceneData
- AdventureData.GetSceneChapter
- AdventureData.GetPassedStageInfo
- AdventureData.GetChapterUnlocked
- AdventureData.UpdateChapterStageData
- AdventureData.ChallengeTableKey
- AdventureData.SaveOneChapterData
- AdventureData.SaveOneStageInfo
- AdventureData.SaveSceneData
- AdventureData.SaveRewardedChapter
- AdventureData.SaveDailyStageNew
- AdventureData.CanShowStageNew
- AdventureData.GetStageData
- AdventureData.GetStageOpen
- AdventureData.GetMainPlotStageIsOpen
- AdventureData.IsStagePassed
- AdventureData.StageCanSweep
**Snippet:**
```lua
AdventureData = {}
local sceneChaptersData = {}
local sceneInfos = {}
local multiDrop = {}

function AdventureData.ClearData()
  sceneChaptersData = {}
  sceneInfos = {}
  multiDrop = {}
end
```

---

## other_A/AdventureMgr.lua.lua
**Functions:**
- AdventureMgr.UpdateChallengeStageData
- AdventureMgr.SaveDailyStageNew
- AdventureMgr.GetTowerNextChapterId
- AdventureMgr.GetAllPlotChapterId
- AdventureMgr.GetNextRewardedChapter
- AdventureMgr.EnterPlotMain
- AdventureMgr.ClearChapterEnd
- AdventureMgr.GetPlayEndChapterId
- AdventureMgr.SaveChangeChapterId
- AdventureMgr.ShowChapterEndTips
- AdventureMgr.Init
**Snippet:**
```lua
AdventureMgr = {
  curType = 1,
  dataType = {1},
  dailyMapIndex = 1,
  currentChapter = nil,
  lastPlotChapter = 0
}
AdventureType = {
  STORY_ADVENTURE = 1,
  EXPERIMENT = 2,
```

---

## other_A/AdventureScriptList.lua.lua
**Requires:**
- AdventureMgr
- AdventureService
- AdventureData
**Snippet:**
```lua
local require = require
require("AdventureMgr")
require("AdventureService")
require("AdventureData")
```

---

## other_A/AdventureService.lua.lua
**Functions:**
- AdventureService.Init
- AdventureService.GetSceneInfoReq
- AdventureService.GetSceneInfoRsp
- AdventureService.GetChapterStageReq
- AdventureService.GetChapterStageRsp
- AdventureService.FetchSceneChapterRewardReq
- AdventureService.FetchSceneChapterRewardRsp
- AdventureService.GetOpenStagesReq
- AdventureService.GetOpenStagesRsp
**Snippet:**
```lua
AdventureService = {}

function AdventureService.Init()
  Net.AddListener(Proto.MsgName.GetSceneInfoRsp, AdventureService.GetSceneInfoRsp)
  Net.AddListener(Proto.MsgName.GetChapterStageRsp, AdventureService.GetChapterStageRsp)
  Net.AddListener(Proto.MsgName.FetchSceneChapterRewardRsp, AdventureService.FetchSceneChapterRewardRsp)
  Net.AddListener(Proto.MsgName.GetOpenStagesRsp, AdventureService.GetOpenStagesRsp)
end

function AdventureService.GetSceneInfoReq(type, rspCallBack)
```

---

## other_A/AdventureWindow.lua.lua
**Functions:**
- AdventureWindow.OnInit
- AdventureWindow.InitRedDot
- AdventureWindow.InitList
- AdventureWindow.TabOnClick
- AdventureWindow.InitData
- AdventureWindow.GetSceneInfoReq
- AdventureWindow.RefreshMapList
- AdventureWindow.ChangePage
- AdventureWindow.RefreshManBar
- AdventureWindow.ShowPlotTag
- AdventureWindow.RefreshTowerInfo
- AdventureWindow.ShowTowerNew
- AdventureWindow.GetTowerDes
- AdventureWindow.GetDailyDungeonData
- AdventureWindow.RefreshExperimentInfo
- list.itemRenderer
- AdventureWindow.ShowMap
- AdventureWindow.RefreshArenaInfo
- AdventureWindow.ShowSeasonTime
- AdventureWindow.RefreshRaidBossInfo
- AdventureWindow.LoadBgEffect
- AdventureWindow.InitMapInfo
- AdventureWindow.RefreshDailyDungeonMapItem
- AdventureWindow.RefreshTowerMapItem
- AdventureWindow.RefreshArenaMapItem
- AdventureWindow.RefreshStoryMapItem
- AdventureWindow.RefreshRaidBossItem
- AdventureWindow.ItemClick
- AdventureWindow.InitBtn
- AdventureWindow.RefreshMapUnlockUI
- AdventureWindow.HandleMessage
- AdventureWindow.OnClose
**Requires:**
- Adventure_AdventureWindowByName
**Snippet:**
```lua
require("Adventure_AdventureWindowByName")
local AdventureWindow = {}
local uis, chapterId, chapterData, chapterTypeMap, contentPane, isFirst, trans, jumpTb
local lastIndex = 0
local dailyDungeonData, arenaTempDay
local effectPath = {
  [AdventureType.ARENA] = "Assets/Art/Effects/Prefab/UI_prefab/Adventuredoor/FX_ui_adventuredoor_battleground.prefab",
  [AdventureType.STORY_ADVENTURE] = "Assets/Art/Effects/Prefab/UI_prefab/Adventuredoor/FX_ui_adventuredoor_adventure.prefab",
  [AdventureType.EXPERIMENT] = "Assets/Art/Effects/Prefab/UI_prefab/Adventuredoor/FX_ui_adventuredoor_itemcollet.prefab",
  [AdventureType.TOWER] = "Assets/Art/Effects/Prefab/UI_prefab/Adventuredoor/FX_ui_adventuredoor_pata.prefab",
```

---

## other_A/Adventure_AdventureByName.lua.lua
**Functions:**
- GetAdventure_AdventureUis
**Requires:**
- CommonResource_BackGroundByName
- Adventure_ContentByName
- Adventure_TabRegionByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Adventure_ContentByName")
require("Adventure_TabRegionByName")
require("CommonResource_CurrencyReturnByName")

function GetAdventure_AdventureUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Content = GetAdventure_ContentUis(ui:GetChild("Content"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
```

---

## other_A/Adventure_AdventureWindowByName.lua.lua
**Functions:**
- GetAdventure_AdventureWindowUis
**Requires:**
- Adventure_AdventureByName
**Snippet:**
```lua
require("Adventure_AdventureByName")

function GetAdventure_AdventureWindowUis(ui)
  local uis = {}
  uis.Main = GetAdventure_AdventureUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other_A/Adventure_ArenaMapByName.lua.lua
**Functions:**
- GetAdventure_ArenaMapUis
**Requires:**
- Adventure_PicMapByName
- Adventure_ArenaTimeByName
- Adventure_ArenaRankByName
**Snippet:**
```lua
require("Adventure_PicMapByName")
require("Adventure_ArenaTimeByName")
require("Adventure_ArenaRankByName")

function GetAdventure_ArenaMapUis(ui)
  local uis = {}
  uis.PicMap = GetAdventure_PicMapUis(ui:GetChild("PicMap"))
  uis.ArenaTime = GetAdventure_ArenaTimeUis(ui:GetChild("ArenaTime"))
  uis.ArenaRank = GetAdventure_ArenaRankUis(ui:GetChild("ArenaRank"))
  uis.ArenaStartBtn = ui:GetChild("ArenaStartBtn")
```

---

## other_A/Adventure_ArenaRankByName.lua.lua
**Functions:**
- GetAdventure_ArenaRankUis
**Snippet:**
```lua
function GetAdventure_ArenaRankUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumbrTxt = ui:GetChild("NumbrTxt")
  uis.root = ui
  return uis
end
```

---

## other_A/Adventure_ArenaStartBtnByName.lua.lua
**Functions:**
- GetAdventure_ArenaStartBtnUis
**Snippet:**
```lua
function GetAdventure_ArenaStartBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other_A/Adventure_ArenaTimeByName.lua.lua
**Functions:**
- GetAdventure_ArenaTimeUis
**Snippet:**
```lua
function GetAdventure_ArenaTimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other_A/Adventure_ContentByName.lua.lua
**Functions:**
- GetAdventure_ContentUis
**Snippet:**
```lua
function GetAdventure_ContentUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## other_A/Adventure_DailyDungeonMapByName.lua.lua
**Functions:**
- GetAdventure_DailyDungeonMapUis
**Requires:**
- Adventure_PicMapByName
**Snippet:**
```lua
require("Adventure_PicMapByName")

function GetAdventure_DailyDungeonMapUis(ui)
  local uis = {}
  uis.PicMap = GetAdventure_PicMapUis(ui:GetChild("PicMap"))
  uis.DailyTypeList = ui:GetChild("DailyTypeList")
  uis.DailyStartBtn = ui:GetChild("DailyStartBtn")
  uis.root = ui
  return uis
end
```

---

## other_A/Adventure_DailyStartBtnByName.lua.lua
**Functions:**
- GetAdventure_DailyStartBtnUis
**Snippet:**
```lua
function GetAdventure_DailyStartBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other_A/Adventure_DailyTypeByName.lua.lua
**Functions:**
- GetAdventure_DailyTypeUis
**Snippet:**
```lua
function GetAdventure_DailyTypeUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## other_A/Adventure_PicMapByName.lua.lua
**Functions:**
- GetAdventure_PicMapUis
**Snippet:**
```lua
function GetAdventure_PicMapUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.PicHolder = ui:GetChild("PicHolder")
  uis.root = ui
  return uis
end
```

---

## other_A/Adventure_PlotDungeonMapByName.lua.lua
**Functions:**
- GetAdventure_PlotDungeonMapUis
**Requires:**
- Adventure_PicMapByName
- Adventure_PlotTitleByName
**Snippet:**
```lua
require("Adventure_PicMapByName")
require("Adventure_PlotTitleByName")

function GetAdventure_PlotDungeonMapUis(ui)
  local uis = {}
  uis.PicMap = GetAdventure_PicMapUis(ui:GetChild("PicMap"))
  uis.PlotTitle = GetAdventure_PlotTitleUis(ui:GetChild("PlotTitle"))
  uis.PlotStartBtn = ui:GetChild("PlotStartBtn")
  uis.root = ui
  return uis
```

---

## other_A/Adventure_PlotStartBtnByName.lua.lua
**Functions:**
- GetAdventure_PlotStartBtnUis
**Snippet:**
```lua
function GetAdventure_PlotStartBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other_A/Adventure_PlotTitleByName.lua.lua
**Functions:**
- GetAdventure_PlotTitleUis
**Snippet:**
```lua
function GetAdventure_PlotTitleUis(ui)
  local uis = {}
  
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other_A/Adventure_RaidBossMapByName.lua.lua
**Functions:**
- GetAdventure_RaidBossMapUis
**Requires:**
- Adventure_PicMapByName
- Adventure_RaidBossTimeByName
- Adventure_RaidBossUnopenByName
**Snippet:**
```lua
require("Adventure_PicMapByName")
require("Adventure_RaidBossTimeByName")
require("Adventure_RaidBossUnopenByName")

function GetAdventure_RaidBossMapUis(ui)
  local uis = {}
  uis.PicMap = GetAdventure_PicMapUis(ui:GetChild("PicMap"))
  uis.RaidBossTime = GetAdventure_RaidBossTimeUis(ui:GetChild("RaidBossTime"))
  uis.RaidBossUnopen = GetAdventure_RaidBossUnopenUis(ui:GetChild("RaidBossUnopen"))
  uis.RaidBossStartBtn = ui:GetChild("RaidBossStartBtn")
```

---

## other_A/Adventure_RaidBossStartBtnByName.lua.lua
**Functions:**
- GetAdventure_RaidBossStartBtnUis
**Snippet:**
```lua
function GetAdventure_RaidBossStartBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other_A/Adventure_RaidBossTimeByName.lua.lua
**Functions:**
- GetAdventure_RaidBossTimeUis
**Snippet:**
```lua
function GetAdventure_RaidBossTimeUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## other_A/Adventure_RaidBossUnopenByName.lua.lua
**Functions:**
- GetAdventure_RaidBossUnopenUis
**Snippet:**
```lua
function GetAdventure_RaidBossUnopenUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other_A/Adventure_TabBtnByName.lua.lua
**Functions:**
- GetAdventure_TabBtnUis
**Requires:**
- CommonResource_RedDotByName
- CommonResource_ArenaNewSeasonByName
- CommonResource_ArenaTimeByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")
require("CommonResource_ArenaNewSeasonByName")
require("CommonResource_ArenaTimeByName")

function GetAdventure_TabBtnUis(ui)
  local uis = {}
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.ArenaNewSeason = GetCommonResource_ArenaNewSeasonUis(ui:GetChild("ArenaNewSeason"))
```

---

## other_A/Adventure_TabRegionByName.lua.lua
**Functions:**
- GetAdventure_TabRegionUis
**Snippet:**
```lua
function GetAdventure_TabRegionUis(ui)
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

## other_A/Adventure_TowerMapByName.lua.lua
**Functions:**
- GetAdventure_TowerMapUis
**Requires:**
- Adventure_PicMapByName
- Adventure_TowerProgressByName
**Snippet:**
```lua
require("Adventure_PicMapByName")
require("Adventure_TowerProgressByName")

function GetAdventure_TowerMapUis(ui)
  local uis = {}
  uis.PicMap = GetAdventure_PicMapUis(ui:GetChild("PicMap"))
  uis.TowerProgress = GetAdventure_TowerProgressUis(ui:GetChild("TowerProgress"))
  uis.TowerStartBtn = ui:GetChild("TowerStartBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## other_A/Adventure_TowerProgressByName.lua.lua
**Functions:**
- GetAdventure_TowerProgressUis
**Snippet:**
```lua
function GetAdventure_TowerProgressUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## other_A/Adventure_TowerStartBtnByName.lua.lua
**Functions:**
- GetAdventure_TowerStartBtnUis
**Snippet:**
```lua
function GetAdventure_TowerStartBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other_A/Arbiter.lua.lua
**Functions:**
- Arbiter:__ctor
- Arbiter:set
- Arbiter:addContact
- Arbiter:isFirstContact
- Arbiter:isDisabled
- Arbiter:preSolve
- Arbiter:solve
**Snippet:**
```lua
local Arbiter = Create("Arbiter")
local BodyType = BodyType

function Arbiter:__ctor(bodyA, bodyB)
  self.bodyA = nil
  self.bodyB = nil
  self.normal = nil
  self.restitution = 0
  self.friction = 0
  self.contacts = {}
```

---

## other_A/ArenaData.lua.lua
**Functions:**
- ArenaData.GetCurArenaLevel
- ArenaData.SaveAllDefenseFormation
- ArenaData.GetDefenseFormation
- ArenaData.ModifyDefensePos
- ArenaData.SaveChallengeStageRsp
- ArenaData.GetChallengeStageRsp
- ArenaData.ClearBattleRecord
- ArenaData.CacheBattleRecord
- ArenaData.GetBattleRecord
**Snippet:**
```lua
ArenaData = {defenseFormation = nil}
ArenaData.Rank = nil
ArenaData.Info = nil
ArenaData.records = nil
local cachedBattleRecord = {}

function ArenaData.GetCurArenaLevel()
  if 0 == ArenaData.Info.matchInfo.level then
    return 1
  end
```

---

## other_A/ArenaExplainWindow.lua.lua
**Functions:**
- ArenaExplainWindow.OnInit
- ArenaExplainWindow.UpdateTextDisplay
- uis.Main.Explain1.ExplainWordList.itemRenderer
- ArenaExplainWindow.GetData
- ArenaExplainWindow.InitList
- uis.Main.Explain1.RewardShowList.itemRenderer
- ArenaExplainWindow.ShowRewardIcon
- ArenaExplainWindow.InitBtn
- ArenaExplainWindow.HandleMessage
- ArenaExplainWindow.OnClose
**Requires:**
- Arena_ExplainWindowByName
**Snippet:**
```lua
require("Arena_ExplainWindowByName")
local ArenaExplainWindow = {}
local uis, contentPane, data

function ArenaExplainWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ArenaExplainWindow.package, WinResConfig.ArenaExplainWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetArena_ExplainWindowUis(contentPane)
    data = TableData.GetConfig(FEATURE_ENUM.ADVENTURE_ARENA, "BaseFeature")
```

---

## other_A/ArenaMgr.lua.lua
**Functions:**
- ArenaMgr.UpdateText
- ArenaMgr.GetRank
- ArenaMgr.GetRobotName
- ArenaMgr.CheckTime
**Snippet:**
```lua
ArenaMgr = {minRank = 2000, DefenseWinId = 11202}
ARENA_ENUM = {
  BATTLE_NUM_ICON = 70010107,
  BATTLE_CD_EXPEND = 70010108,
  BATTLE_CD_WIN = 70010109,
  BATTLE_CD_LOSER = 70010110,
  UPDATE_ENEMY_CD = 70010112
}

function ArenaMgr.UpdateText(title, name, name_en, des)
```

---

## other_A/ArenaRankWindow.lua.lua
**Functions:**
- ArenaRankWindow.OnInit
- ArenaRankWindow.UpdateTextDisplay
- ArenaRankWindow.Init
- uis.Main.Glory.GloryList.itemRenderer
- ArenaRankWindow.RefreshRankItem
- list.itemRenderer
- ArenaRankWindow.GetArenaMedal
- ArenaRankWindow.InitBtn
- ArenaRankWindow.HandleMessage
- ArenaRankWindow.OnClose
**Requires:**
- Arena_RankWindowByName
**Snippet:**
```lua
require("Arena_RankWindowByName")
local ArenaRankWindow = {}
local uis, contentPane, rankData, jumpTb

function ArenaRankWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ArenaRankWindow.package, WinResConfig.ArenaRankWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetArena_RankWindowUis(contentPane)
    rankData = ArenaData.Rank.rankList
```

---

## other_A/ArenaRecordWindow.lua.lua
**Functions:**
- ArenaRecordWindow.OnInit
- ArenaRecordWindow.UpdateTextDisplay
- ArenaRecordWindow.Init
- ArenaRecordWindow.RefreshRecordItem
- ArenaRecordWindow.FormatRemainTime
- ArenaRecordWindow.InitBtn
- ArenaRecordWindow.HandleMessage
- ArenaRecordWindow.OnClose
**Requires:**
- Arena_RecordWindowByName
**Snippet:**
```lua
require("Arena_RecordWindowByName")
local ArenaRecordWindow = {}
local uis, contentPane, jumpTb

function ArenaRecordWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ArenaRecordWindow.package, WinResConfig.ArenaRecordWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetArena_RecordWindowUis(contentPane)
    uis.Main.BackGround.BackGroundLoader.url = UIUtil.GetBackgroundUrl(FEATURE_ENUM.ARENA_WINDOWS)
```

---

## other_A/ArenaRewardWindow.lua.lua
**Functions:**
- ArenaRewardWindow.OnInit
- ArenaRewardWindow.InitRedDot
- ArenaRewardWindow.UpdateTextDisplay
- ArenaRewardWindow.CheckNewSeasonTime
- ArenaRewardWindow.GetRewardData
- ArenaRewardWindow.GetWeekData
- ArenaRewardWindow.Sort
- ArenaRewardWindow.ShowTime
- ArenaRewardWindow.Init
- ArenaRewardWindow.RefreshRankItem
- ArenaRewardWindow.ShowRewardIcon
- list.itemRenderer
- ArenaRewardWindow.GetState
- ArenaRewardWindow.InitBtn
- ArenaRewardWindow.HandleMessage
- ArenaRewardWindow.OnClose
**Requires:**
- Arena_RewardWindowByName
**Snippet:**
```lua
require("Arena_RewardWindowByName")
local ArenaRewardWindow = {}
local uis, contentPane, rewardData, isReward, isWeek, jumpTb

function ArenaRewardWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ArenaRewardWindow.package, WinResConfig.ArenaRewardWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetArena_RewardWindowUis(contentPane)
    uis.Main.BackGround.BackGroundLoader.url = UIUtil.GetBackgroundUrl(FEATURE_ENUM.ARENA_WINDOWS)
```

---

## other_A/ArenaScriptList.lua.lua
**Requires:**
- ArenaData
- ArenaService
- ArenaMgr
**Snippet:**
```lua
local require = require
require("ArenaData")
require("ArenaService")
require("ArenaMgr")
```

---

## other_A/ArenaSeasonTipsWindow.lua.lua
**Functions:**
- ArenaSeasonTipsWindow.OnInit
- ArenaSeasonTipsWindow.UpdateTextDisplay
- ArenaSeasonTipsWindow.InitBtn
- ArenaSeasonTipsWindow.OnClose
**Requires:**
- Arena_SeasonTipsWindowByName
**Snippet:**
```lua
require("Arena_SeasonTipsWindowByName")
local ArenaSeasonTipsWindow = {}
local uis, contentPane

function ArenaSeasonTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ArenaSeasonTipsWindow.package, WinResConfig.ArenaSeasonTipsWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetArena_SeasonTipsWindowUis(contentPane)
    ArenaSeasonTipsWindow.InitBtn()
```

---

## other_A/ArenaService.lua.lua
**Functions:**
- ArenaService.Init
- ArenaService.ArenaGetAllReq
- ArenaService.ArenaGetAllRsp
- ArenaService.ArenaGetMatchReq
- ArenaService.ArenaGetMatchRsp
- ArenaService.ArenaResetFightNumReq
- ArenaService.ArenaResetFightNumRsp
- ArenaService.ArenaGetTopRankReq
- ArenaService.ArenaGetTopRankRsp
- ArenaService.ArenaRefreshFightCDReq
- ArenaService.ArenaRefreshFightCDRsp
- ArenaService.ArenaGetRankRewardReq
- ArenaService.ArenaGetRankRewardRsp
- ArenaService.ArenaGetAllDefenseReq
- ArenaService.ArenaGetAllDefenseRsp
- ArenaService.ArenaSetDefenseReq
- ArenaService.ArenaSetDefenseRsp
- ArenaService.ArenaGetOpponentFormationReq
- ArenaService.ArenaGetOpponentFormationRsp
- ArenaService.ArenaGetRecordReq
- ArenaService.ArenaGetRecordRsp
**Snippet:**
```lua
ArenaService = {}

function ArenaService.Init()
  Net.AddListener(Proto.MsgName.ArenaGetAllRsp, ArenaService.ArenaGetAllRsp)
  Net.AddListener(Proto.MsgName.ArenaGetMatchRsp, ArenaService.ArenaGetMatchRsp)
  Net.AddListener(Proto.MsgName.ArenaResetFightNumRsp, ArenaService.ArenaResetFightNumRsp)
  Net.AddListener(Proto.MsgName.ArenaGetTopRankRsp, ArenaService.ArenaGetTopRankRsp)
  Net.AddListener(Proto.MsgName.ArenaRefreshFightCDRsp, ArenaService.ArenaRefreshFightCDRsp)
  Net.AddListener(Proto.MsgName.ArenaGetRankRewardRsp, ArenaService.ArenaGetRankRewardRsp)
  Net.AddListener(Proto.MsgName.ArenaGetAllDefenseRsp, ArenaService.ArenaGetAllDefenseRsp)
```

---

## other_A/ArenaWindow.lua.lua
**Functions:**
- ArenaWindow.OnInit
- ArenaWindow.InitRedDot
- ArenaWindow.UpdateTextDisplay
- ArenaWindow.Init
- ArenaWindow.InitBuilding
- ArenaWindow.InitMap
- ArenaWindow.CheckNewSeasonTime
- ArenaWindow.LoadBgTexture
- ArenaWindow.IsNewSeason
- ArenaWindow.RefreshTextInfo
- ArenaWindow.UpdateEnemy
- ArenaWindow.StartBattle
- ArenaWindow.ShowCD
- ArenaWindow.GetBuyNum
- ArenaWindow.InitBtn
- ArenaWindow.ClearCd
- ArenaWindow.ShowBuyNum
- ArenaWindow.HandleMessage
- ArenaWindow.OnClose
**Requires:**
- Arena_ArenaWindowByName
- Arena_EnemyInfoBtnByName
**Snippet:**
```lua
require("Arena_ArenaWindowByName")
require("Arena_EnemyInfoBtnByName")
local ArenaWindow = {}
local uis, contentPane, timeInfo, iconUrl, isSettle, rank, buyNum, bgPrefab, timeLineObj
local updateCd = 1
local tween, root, jumpTb, headScale, buildingListData, mapListData

function ArenaWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ArenaWindow.package, WinResConfig.ArenaWindow.comName, function(com)
    contentPane = com
```

---

## other_A/Arena_ArenaByName.lua.lua
**Functions:**
- GetArena_ArenaUis
**Requires:**
- CommonResource_BackGroundByName
- Arena_BattleInfoByName
- Arena_MyRankByName
- Arena_TimeByName
- Arena_LockEntryByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Arena_BattleInfoByName")
require("Arena_MyRankByName")
require("Arena_TimeByName")
require("Arena_LockEntryByName")
require("CommonResource_CurrencyReturnByName")

function GetArena_ArenaUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
```

---

## other_A/Arena_ArenaWindowByName.lua.lua
**Functions:**
- GetArena_ArenaWindowUis
**Requires:**
- Arena_ArenaByName
**Snippet:**
```lua
require("Arena_ArenaByName")

function GetArena_ArenaWindowUis(ui)
  local uis = {}
  uis.Main = GetArena_ArenaUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_BattleInfoByName.lua.lua
**Functions:**
- GetArena_BattleInfoUis
**Snippet:**
```lua
function GetArena_BattleInfoUis(ui)
  local uis = {}
  
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_BattleNumber1ByName.lua.lua
**Functions:**
- GetArena_BattleNumber1Uis
**Snippet:**
```lua
function GetArena_BattleNumber1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_BattleNumber2ByName.lua.lua
**Functions:**
- GetArena_BattleNumber2Uis
**Requires:**
- CommonResource_PopupBgByName
- CommonResource_Popup_BByName
- Arena_BattleNumber1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("CommonResource_Popup_BByName")
require("Arena_BattleNumber1ByName")

function GetArena_BattleNumber2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Popup_B = GetCommonResource_Popup_BUis(ui:GetChild("Popup_B"))
  uis.BattleNumber1 = GetArena_BattleNumber1Uis(ui:GetChild("BattleNumber1"))
```

---

## other_A/Arena_BattleNumberWindowByName.lua.lua
**Functions:**
- GetArena_BattleNumberWindowUis
**Requires:**
- Arena_BattleNumber2ByName
**Snippet:**
```lua
require("Arena_BattleNumber2ByName")

function GetArena_BattleNumberWindowUis(ui)
  local uis = {}
  uis.Main = GetArena_BattleNumber2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_BuildIconBgByName.lua.lua
**Functions:**
- GetArena_BuildIconBgUis
**Snippet:**
```lua
function GetArena_BuildIconBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_BuildIconByName.lua.lua
**Functions:**
- GetArena_BuildIconUis
**Requires:**
- Arena_BuildIconBgByName
- Arena_OpenStateByName
- Arena_LockStateByName
**Snippet:**
```lua
require("Arena_BuildIconBgByName")
require("Arena_OpenStateByName")
require("Arena_LockStateByName")

function GetArena_BuildIconUis(ui)
  local uis = {}
  uis.BuildIconBg = GetArena_BuildIconBgUis(ui:GetChild("BuildIconBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.OpenState = GetArena_OpenStateUis(ui:GetChild("OpenState"))
  uis.LockState = GetArena_LockStateUis(ui:GetChild("LockState"))
```

---

## other_A/Arena_BuildLockByName.lua.lua
**Functions:**
- GetArena_BuildLockUis
**Requires:**
- CommonResource_PopupBgByName
- Arena_LockTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Arena_LockTipsByName")

function GetArena_BuildLockUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.BuildLockTips = GetArena_LockTipsUis(ui:GetChild("BuildLockTips"))
  uis.root = ui
  return uis
```

---

## other_A/Arena_BuildLockEntryBtnByName.lua.lua
**Functions:**
- GetArena_BuildLockEntryBtnUis
**Snippet:**
```lua
function GetArena_BuildLockEntryBtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## other_A/Arena_BuildLockTipsByName.lua.lua
**Functions:**
- GetArena_BuildLockTipsUis
**Snippet:**
```lua
function GetArena_BuildLockTipsUis(ui)
  local uis = {}
  
  uis.BuildList = ui:GetChild("BuildList")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_BuildLockWindowByName.lua.lua
**Functions:**
- GetArena_BuildLockWindowUis
**Requires:**
- Arena_BuildLockByName
**Snippet:**
```lua
require("Arena_BuildLockByName")

function GetArena_BuildLockWindowUis(ui)
  local uis = {}
  uis.Main = GetArena_BuildLockUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_ButtonGreenBtnByName.lua.lua
**Functions:**
- GetArena_ButtonGreenBtnUis
**Snippet:**
```lua
function GetArena_ButtonGreenBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_ButtonWhiteBtnByName.lua.lua
**Functions:**
- GetArena_ButtonWhiteBtnUis
**Requires:**
- CommonResource_ArenaDefendNewByName
**Snippet:**
```lua
require("CommonResource_ArenaDefendNewByName")

function GetArena_ButtonWhiteBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.New = GetCommonResource_ArenaDefendNewUis(ui:GetChild("New"))
  uis.buttonCtr = ui:GetController("button")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
```

---

## other_A/Arena_BuyNumberBtnByName.lua.lua
**Functions:**
- GetArena_BuyNumberBtnUis
**Snippet:**
```lua
function GetArena_BuyNumberBtnUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## other_A/Arena_CardPicByName.lua.lua
**Functions:**
- GetArena_CardPicUis
**Snippet:**
```lua
function GetArena_CardPicUis(ui)
  local uis = {}
  
  uis.CardPicLoader = ui:GetChild("CardPicLoader")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_CompleteTipsByName.lua.lua
**Functions:**
- GetArena_CompleteTipsUis
**Snippet:**
```lua
function GetArena_CompleteTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_EnemyInfoBtnByName.lua.lua
**Functions:**
- GetArena_EnemyInfoBtnUis
**Requires:**
- Arena_CardPicByName
- Arena_EnemyRankByName
**Snippet:**
```lua
require("Arena_CardPicByName")
require("Arena_EnemyRankByName")

function GetArena_EnemyInfoBtnUis(ui)
  local uis = {}
  uis.CardPic = GetArena_CardPicUis(ui:GetChild("CardPic"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.EnemyRank = GetArena_EnemyRankUis(ui:GetChild("EnemyRank"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
```

---

## other_A/Arena_EnemyRankByName.lua.lua
**Functions:**
- GetArena_EnemyRankUis
**Snippet:**
```lua
function GetArena_EnemyRankUis(ui)
  local uis = {}
  
  uis.RankTxt = ui:GetChild("RankTxt")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_GloryByName.lua.lua
**Functions:**
- GetArena_GloryUis
**Snippet:**
```lua
function GetArena_GloryUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.GloryList = ui:GetChild("GloryList")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_HeadPicByName.lua.lua
**Functions:**
- GetArena_HeadPicUis
**Snippet:**
```lua
function GetArena_HeadPicUis(ui)
  local uis = {}
  
  uis.HeadLoader = ui:GetChild("HeadLoader")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_LockEntryByName.lua.lua
**Functions:**
- GetArena_LockEntryUis
**Snippet:**
```lua
function GetArena_LockEntryUis(ui)
  local uis = {}
  
  uis.MapLockEntryBtn = ui:GetChild("MapLockEntryBtn")
  uis.BuildLockEntryBtn = ui:GetChild("BuildLockEntryBtn")
  uis.SwitchBtn = ui:GetChild("SwitchBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## other_A/Arena_LockEntrySwitchBtnByName.lua.lua
**Functions:**
- GetArena_LockEntrySwitchBtnUis
**Snippet:**
```lua
function GetArena_LockEntrySwitchBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_LockStateByName.lua.lua
**Functions:**
- GetArena_LockStateUis
**Snippet:**
```lua
function GetArena_LockStateUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_LockTipsByName.lua.lua
**Functions:**
- GetArena_LockTipsUis
**Requires:**
- Arena_BuildLockTipsByName
- Arena_MapLockTipsByName
**Snippet:**
```lua
require("Arena_BuildLockTipsByName")
require("Arena_MapLockTipsByName")

function GetArena_LockTipsUis(ui)
  local uis = {}
  uis.BuildLockTips = GetArena_BuildLockTipsUis(ui:GetChild("BuildLockTips"))
  uis.MapLockTips = GetArena_MapLockTipsUis(ui:GetChild("MapLockTips"))
  uis.Tab1Btn = ui:GetChild("Tab1Btn")
  uis.Tab2Btn = ui:GetChild("Tab2Btn")
  uis.c1Ctr = ui:GetController("c1")
```

---

## other_A/Arena_LockTipsTab1BtnByName.lua.lua
**Functions:**
- GetArena_LockTipsTab1BtnUis
**Snippet:**
```lua
function GetArena_LockTipsTab1BtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_LockTipsTab2BtnByName.lua.lua
**Functions:**
- GetArena_LockTipsTab2BtnUis
**Snippet:**
```lua
function GetArena_LockTipsTab2BtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_MapIconBgByName.lua.lua
**Functions:**
- GetArena_MapIconBgUis
**Snippet:**
```lua
function GetArena_MapIconBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_MapIconByName.lua.lua
**Functions:**
- GetArena_MapIconUis
**Requires:**
- Arena_MapIconBgByName
- Arena_OpenStateByName
- Arena_LockStateByName
**Snippet:**
```lua
require("Arena_MapIconBgByName")
require("Arena_OpenStateByName")
require("Arena_LockStateByName")

function GetArena_MapIconUis(ui)
  local uis = {}
  uis.MapIconBg = GetArena_MapIconBgUis(ui:GetChild("MapIconBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.OpenState = GetArena_OpenStateUis(ui:GetChild("OpenState"))
  uis.LockState = GetArena_LockStateUis(ui:GetChild("LockState"))
```

---

## other_A/Arena_MapLockEntryBtnByName.lua.lua
**Functions:**
- GetArena_MapLockEntryBtnUis
**Snippet:**
```lua
function GetArena_MapLockEntryBtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## other_A/Arena_MapLockTipsByName.lua.lua
**Functions:**
- GetArena_MapLockTipsUis
**Snippet:**
```lua
function GetArena_MapLockTipsUis(ui)
  local uis = {}
  
  uis.MapList = ui:GetChild("MapList")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_MedalByName.lua.lua
**Functions:**
- GetArena_MedalUis
**Snippet:**
```lua
function GetArena_MedalUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_MyRankByName.lua.lua
**Functions:**
- GetArena_MyRankUis
**Snippet:**
```lua
function GetArena_MyRankUis(ui)
  local uis = {}
  
  uis.RankTxt = ui:GetChild("RankTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_NowRankByName.lua.lua
**Functions:**
- GetArena_NowRankUis
**Snippet:**
```lua
function GetArena_NowRankUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.RankTxt = ui:GetChild("RankTxt")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_OpenStateByName.lua.lua
**Functions:**
- GetArena_OpenStateUis
**Snippet:**
```lua
function GetArena_OpenStateUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_OwnByName.lua.lua
**Functions:**
- GetArena_OwnUis
**Snippet:**
```lua
function GetArena_OwnUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_PopupByName.lua.lua
**Functions:**
- GetArena_PopupUis
**Snippet:**
```lua
function GetArena_PopupUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_RankBtnByName.lua.lua
**Functions:**
- GetArena_RankBtnUis
**Snippet:**
```lua
function GetArena_RankBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_RankByName.lua.lua
**Functions:**
- GetArena_RankUis
**Requires:**
- CommonResource_BackGroundByName
- Arena_TitleByName
- Arena_GloryByName
- Arena_NowRankByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Arena_TitleByName")
require("Arena_GloryByName")
require("Arena_NowRankByName")
require("CommonResource_CurrencyReturnByName")

function GetArena_RankUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Title = GetArena_TitleUis(ui:GetChild("Title"))
```

---

## other_A/Arena_RankTipsAniByName.lua.lua
**Functions:**
- GetArena_RankTipsAniUis
**Requires:**
- Arena_RankTipsByName
**Snippet:**
```lua
require("Arena_RankTipsByName")

function GetArena_RankTipsAniUis(ui)
  local uis = {}
  uis.RankTips = GetArena_RankTipsUis(ui:GetChild("RankTips"))
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_RankTipsByName.lua.lua
**Functions:**
- GetArena_RankTipsUis
**Requires:**
- CommonResource_HeadByName
**Snippet:**
```lua
require("CommonResource_HeadByName")

function GetArena_RankTipsUis(ui)
  local uis = {}
  uis.RankTxt = ui:GetChild("RankTxt")
  uis.Head = GetCommonResource_HeadUis(ui:GetChild("Head"))
  uis.GuildTxt = ui:GetChild("GuildTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.GloryList = ui:GetChild("GloryList")
```

---

## other_A/Arena_RankWindowByName.lua.lua
**Functions:**
- GetArena_RankWindowUis
**Requires:**
- Arena_RankByName
**Snippet:**
```lua
require("Arena_RankByName")

function GetArena_RankWindowUis(ui)
  local uis = {}
  uis.Main = GetArena_RankUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_RecordByName.lua.lua
**Functions:**
- GetArena_RecordUis
**Requires:**
- CommonResource_BackGroundByName
- Arena_TitleByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Arena_TitleByName")
require("CommonResource_CurrencyReturnByName")

function GetArena_RecordUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Title = GetArena_TitleUis(ui:GetChild("Title"))
  uis.RecordTipsList = ui:GetChild("RecordTipsList")
  uis.CurrencyReturn = GetCommonResource_CurrencyReturnUis(ui:GetChild("CurrencyReturn"))
```

---

## other_A/Arena_RecordDataBtnByName.lua.lua
**Functions:**
- GetArena_RecordDataBtnUis
**Snippet:**
```lua
function GetArena_RecordDataBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_RecordPlayBackBtnByName.lua.lua
**Functions:**
- GetArena_RecordPlayBackBtnUis
**Snippet:**
```lua
function GetArena_RecordPlayBackBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_RecordTipsAniByName.lua.lua
**Functions:**
- GetArena_RecordTipsAniUis
**Requires:**
- Arena_RecordTipsByName
**Snippet:**
```lua
require("Arena_RecordTipsByName")

function GetArena_RecordTipsAniUis(ui)
  local uis = {}
  uis.RecordTips = GetArena_RecordTipsUis(ui:GetChild("RecordTips"))
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_RecordTipsByName.lua.lua
**Functions:**
- GetArena_RecordTipsUis
**Requires:**
- CommonResource_HeadByName
**Snippet:**
```lua
require("CommonResource_HeadByName")

function GetArena_RecordTipsUis(ui)
  local uis = {}
  uis.Head = GetCommonResource_HeadUis(ui:GetChild("Head"))
  uis.ResultTxt = ui:GetChild("ResultTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.GuildTxt = ui:GetChild("GuildTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
```

---

## other_A/Arena_RecordWindowByName.lua.lua
**Functions:**
- GetArena_RecordWindowUis
**Requires:**
- Arena_RecordByName
**Snippet:**
```lua
require("Arena_RecordByName")

function GetArena_RecordWindowUis(ui)
  local uis = {}
  uis.Main = GetArena_RecordUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_RefreshBtnByName.lua.lua
**Functions:**
- GetArena_RefreshBtnUis
**Snippet:**
```lua
function GetArena_RefreshBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_RewardBtnByName.lua.lua
**Functions:**
- GetArena_RewardBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetArena_RewardBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_RewardByName.lua.lua
**Functions:**
- GetArena_RewardUis
**Requires:**
- CommonResource_BackGroundByName
- Arena_TitleByName
- Arena_SeasonTimeByName
- Arena_TabRegionByName
- Arena_RewardTipsListByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Arena_TitleByName")
require("Arena_SeasonTimeByName")
require("Arena_TabRegionByName")
require("Arena_RewardTipsListByName")
require("CommonResource_CurrencyReturnByName")

function GetArena_RewardUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
```

---

## other_A/Arena_RewardGetRegionByName.lua.lua
**Functions:**
- GetArena_RewardGetRegionUis
**Snippet:**
```lua
function GetArena_RewardGetRegionUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_RewardItemByName.lua.lua
**Functions:**
- GetArena_RewardItemUis
**Snippet:**
```lua
function GetArena_RewardItemUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_RewardTipsAniByName.lua.lua
**Functions:**
- GetArena_RewardTipsAniUis
**Snippet:**
```lua
function GetArena_RewardTipsAniUis(ui)
  local uis = {}
  
  uis.RewardTipsBtn = ui:GetChild("RewardTipsBtn")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_RewardTipsBtnByName.lua.lua
**Functions:**
- GetArena_RewardTipsBtnUis
**Requires:**
- Arena_RewardGetRegionByName
- Arena_CompleteTipsByName
**Snippet:**
```lua
require("Arena_RewardGetRegionByName")
require("Arena_CompleteTipsByName")

function GetArena_RewardTipsBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.ProgressTxt = ui:GetChild("ProgressTxt")
  uis.RewardGetRegion = GetArena_RewardGetRegionUis(ui:GetChild("RewardGetRegion"))
  uis.RewardList = ui:GetChild("RewardList")
```

---

## other_A/Arena_RewardTipsListByName.lua.lua
**Functions:**
- GetArena_RewardTipsListUis
**Snippet:**
```lua
function GetArena_RewardTipsListUis(ui)
  local uis = {}
  
  uis.RewardTipsList = ui:GetChild("RewardTipsList")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_RewardWindowByName.lua.lua
**Functions:**
- GetArena_RewardWindowUis
**Requires:**
- Arena_RewardByName
**Snippet:**
```lua
require("Arena_RewardByName")

function GetArena_RewardWindowUis(ui)
  local uis = {}
  uis.Main = GetArena_RewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_SeasonTimeByName.lua.lua
**Functions:**
- GetArena_SeasonTimeUis
**Snippet:**
```lua
function GetArena_SeasonTimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.RankTxt = ui:GetChild("RankTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_SeasonTips1ByName.lua.lua
**Functions:**
- GetArena_SeasonTips1Uis
**Snippet:**
```lua
function GetArena_SeasonTips1Uis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_SeasonTips2ByName.lua.lua
**Functions:**
- GetArena_SeasonTips2Uis
**Requires:**
- CommonResource_PopupBgByName
- Arena_PopupByName
- Arena_SeasonTips1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Arena_PopupByName")
require("Arena_SeasonTips1ByName")

function GetArena_SeasonTips2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Popup_S = GetArena_PopupUis(ui:GetChild("Popup_S"))
  uis.SeasonTips1 = GetArena_SeasonTips1Uis(ui:GetChild("SeasonTips1"))
```

---

## other_A/Arena_SeasonTipsWindowByName.lua.lua
**Functions:**
- GetArena_SeasonTipsWindowUis
**Requires:**
- Arena_SeasonTips2ByName
**Snippet:**
```lua
require("Arena_SeasonTips2ByName")

function GetArena_SeasonTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetArena_SeasonTips2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_Tab1BtnByName.lua.lua
**Functions:**
- GetArena_Tab1BtnUis
**Snippet:**
```lua
function GetArena_Tab1BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_Tab2BtnByName.lua.lua
**Functions:**
- GetArena_Tab2BtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetArena_Tab2BtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_TabRegionByName.lua.lua
**Functions:**
- GetArena_TabRegionUis
**Snippet:**
```lua
function GetArena_TabRegionUis(ui)
  local uis = {}
  
  uis.Tab1Btn = ui:GetChild("Tab1Btn")
  uis.Tab2Btn = ui:GetChild("Tab2Btn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_TimeAxisBtnByName.lua.lua
**Functions:**
- GetArena_TimeAxisBtnUis
**Snippet:**
```lua
function GetArena_TimeAxisBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_TimeByName.lua.lua
**Functions:**
- GetArena_TimeUis
**Snippet:**
```lua
function GetArena_TimeUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## other_A/Arena_TitleByName.lua.lua
**Functions:**
- GetArena_TitleUis
**Snippet:**
```lua
function GetArena_TitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## other_A/AttributeDesWindow.lua.lua
**Functions:**
- AttributeDesWindow.ReInitData
- AttributeDesWindow.OnInit
- AttributeDesWindow.GetData
- AttributeDesWindow.ShowAttribute
- list.itemRenderer
- list.itemRenderer
- list.itemRenderer
- list.itemRenderer
- list.itemRenderer
- detailItemlist.itemRenderer
- AttributeDesWindow.InitUI
- tablist.itemRenderer
- AttributeDesWindow.Quit
- AttributeDesWindow.InitBtn
- AttributeDesWindow.OnClose
- AttributeDesWindow.HandleMessage
**Requires:**
- CardAttribute_AttributeDesWindowByName
**Snippet:**
```lua
require("CardAttribute_AttributeDesWindowByName")
local AttributeDesWindow = {}
local uis, contentPane, displayDetailMode

function AttributeDesWindow.ReInitData()
end

function AttributeDesWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.AttributeDesWindow.package, WinResConfig.AttributeDesWindow.comName, function(com)
    contentPane = com
```

---
