# MP

## MP/MailData.lua.lua
**Functions:**
- MailData.FormatMail
- MailData.GetMailInfoByUid
- MailData.DeleteMail
- MailData.ClearData
**Snippet:**
```lua
MailData = {}
MailData.mails = {}
MailData.deleteTempId = nil
local FormatParams = function(wordId, params)
  local id = tonumber(wordId)
  if id and params then
    if #params > 0 then
      local bol, str = pcall(T, id, table.unpack(params))
      if bol and str then
        return str
```

---

## MP/MailMgr.lua.lua
**Functions:**
- MailMgr.OpenMailWindow
- MailMgr.UpdateByHomeWindow
**Snippet:**
```lua
MailMgr = {}

function MailMgr.OpenMailWindow(isJump)
  if #MailData.mails > 0 then
    ld("Mail", function()
      if isJump then
        JumpToWindow(WinResConfig.MailWindow.nam)
      else
        OpenWindow(WinResConfig.MailWindow.name)
      end
```

---

## MP/MailScriptList.lua.lua
**Requires:**
- MailData
- MailService
- MailMgr
**Snippet:**
```lua
local require = require
require("MailData")
require("MailService")
require("MailMgr")
```

---

## MP/MailService.lua.lua
**Functions:**
- MailService.Init
- MailService.GetAllMailsReq
- MailService.GetAllMailsRsp
- MailService.DeleteMailReq
- MailService.DeleteMailRsp
- MailService.MarkMailReadReq
- MailService.MarkMailReadRsp
- MailService.FetchMailAttachmentReq
- MailService.FetchMailAttachmentRsp
**Snippet:**
```lua
MailService = {}

function MailService.Init()
  Net.AddListener(Proto.MsgName.GetAllMailsRsp, MailService.GetAllMailsRsp)
  Net.AddListener(Proto.MsgName.DeleteMailRsp, MailService.DeleteMailRsp)
  Net.AddListener(Proto.MsgName.MarkMailReadRsp, MailService.MarkMailReadRsp)
  Net.AddListener(Proto.MsgName.FetchMailAttachmentRsp, MailService.FetchMailAttachmentRsp)
end

function MailService.GetAllMailsReq(mailSeq, rspCallback)
```

---

## MP/MailWindow.lua.lua
**Functions:**
- MailWindow.OnInit
- MailWindow.UpdateTextDisplay
- MailWindow.InitList
- MailWindow.SortMail
- MailWindow.RefreshItem
- MailWindow.FormatTime
- MailWindow.InitAttachment
- MailWindow.MailOnClick
- MailWindow.ClickLink
- MailWindow.ClearListChild
- MailWindow.StopTime
- MailWindow.DeleteMail
- MailWindow.AllGetMail
- MailWindow.GetMail
- MailWindow.InitBtn
- MailWindow.HandleMessage
- MailWindow.OnClose
**Requires:**
- Mail_MailWindowByName
**Snippet:**
```lua
require("Mail_MailWindowByName")
local MailWindow = {}
local uis, contentPane, curMailData, lastBtn, downTime
local speed = 0.088
local isInitPlayAnim, isAllGetMail, isAllGetShow, selectMailIndex, jumpTb, enterShow

function MailWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.MailWindow.package, WinResConfig.MailWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
```

---

## MP/Mail_DeleteBtnByName.lua.lua
**Functions:**
- GetMail_DeleteBtnUis
**Snippet:**
```lua
function GetMail_DeleteBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/Mail_DetailedBtnAinByName.lua.lua
**Functions:**
- GetMail_DetailedBtnAinUis
**Snippet:**
```lua
function GetMail_DetailedBtnAinUis(ui)
  local uis = {}
  
  uis.DetailedBtn = ui:GetChild("DetailedBtn")
  uis.root = ui
  return uis
end
```

---

## MP/Mail_DetailedBtnBg1ByName.lua.lua
**Functions:**
- GetMail_DetailedBtnBg1Uis
**Snippet:**
```lua
function GetMail_DetailedBtnBg1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## MP/Mail_DetailedBtnBgByName.lua.lua
**Functions:**
- GetMail_DetailedBtnBgUis
**Snippet:**
```lua
function GetMail_DetailedBtnBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## MP/Mail_DetailedBtnByName.lua.lua
**Functions:**
- GetMail_DetailedBtnUis
**Requires:**
- Mail_DetailedBtnBg1ByName
- Mail_DetailedBtnBgByName
- Mail_TimeByName
**Snippet:**
```lua
require("Mail_DetailedBtnBg1ByName")
require("Mail_DetailedBtnBgByName")
require("Mail_TimeByName")

function GetMail_DetailedBtnUis(ui)
  local uis = {}
  uis.DetailedBtnBg1 = GetMail_DetailedBtnBg1Uis(ui:GetChild("DetailedBtnBg1"))
  uis.DetailedBtnBg = GetMail_DetailedBtnBgUis(ui:GetChild("DetailedBtnBg"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.SenderTxt = ui:GetChild("SenderTxt")
```

---

## MP/Mail_GetTipsByName.lua.lua
**Functions:**
- GetMail_GetTipsUis
**Snippet:**
```lua
function GetMail_GetTipsUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Mail_ItemByName.lua.lua
**Functions:**
- GetMail_ItemUis
**Snippet:**
```lua
function GetMail_ItemUis(ui)
  local uis = {}
  
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## MP/Mail_MailByName.lua.lua
**Functions:**
- GetMail_MailUis
**Requires:**
- CommonResource_BackGroundByName
- Mail_TipsByName
- Mail_NumberByName
- Mail_TitleByName
- Mail_ItemByName
- Mail_GetTipsByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Mail_TipsByName")
require("Mail_NumberByName")
require("Mail_TitleByName")
require("Mail_ItemByName")
require("Mail_GetTipsByName")
require("CommonResource_CurrencyReturnByName")

function GetMail_MailUis(ui)
  local uis = {}
```

---

## MP/Mail_MailWindowByName.lua.lua
**Functions:**
- GetMail_MailWindowUis
**Requires:**
- Mail_MailByName
**Snippet:**
```lua
require("Mail_MailByName")

function GetMail_MailWindowUis(ui)
  local uis = {}
  uis.Main = GetMail_MailUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Mail_NumberByName.lua.lua
**Functions:**
- GetMail_NumberUis
**Snippet:**
```lua
function GetMail_NumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Mail_TimeByName.lua.lua
**Functions:**
- GetMail_TimeUis
**Snippet:**
```lua
function GetMail_TimeUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Mail_TipsByName.lua.lua
**Functions:**
- GetMail_TipsUis
**Snippet:**
```lua
function GetMail_TipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Mail_TitleByName.lua.lua
**Functions:**
- GetMail_TitleUis
**Snippet:**
```lua
function GetMail_TitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Mail_WordTxtByName.lua.lua
**Functions:**
- GetMail_WordTxtUis
**Snippet:**
```lua
function GetMail_WordTxtUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Main.lua.lua
**Functions:**
- LoadGlobalObject
- OpenStartWindow
- UIMgr.OpenLoginAction
- BlockInTestPackage
**Snippet:**
```lua
math.randomseed(os.time())
if Debug and Application.platform ~= RuntimePlatform.WindowsEditor and Application.platform ~= RuntimePlatform.OSXEditor then
  if LogType then
    Debug.unityLogger.filterLogType = LogType.Error
  else
    Debug.unityLogger.logEnabled = false
  end
end

function LoadGlobalObject()
```

---

## MP/MainOpalExchangeWindow.lua.lua
**Functions:**
- MainOpalExchangeWindow.ReInitData
- MainOpalExchangeWindow.OnInit
- MainOpalExchangeWindow.UpdateInfo
- MainOpalExchangeWindow.GetGesture
- MainOpalExchangeWindow.CloseWindow
- MainOpalExchangeWindow.InitBtn
- MainOpalExchangeWindow.OnClose
**Requires:**
- Message_MainOpalExchangeWindowByName
**Snippet:**
```lua
require("Message_MainOpalExchangeWindowByName")
local MainOpalExchangeWindow = {}
local uis, contentPane, buyNum, itemInfo, wordId, priceNum

function MainOpalExchangeWindow.ReInitData()
end

function MainOpalExchangeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.MainOpalExchangeWindow.package, WinResConfig.MainOpalExchangeWindow.comName, function(com)
    contentPane = com
```

---

## MP/MainSealLevelUpTipsWindow.lua.lua
**Functions:**
- MainSealLevelUpTipsWindow.ReInitData
- MainSealLevelUpTipsWindow.OnInit
- MainSealLevelUpTipsWindow.UpdateInfo
- list.itemProvider
- list.itemRenderer
- MainSealLevelUpTipsWindow.InitBtn
- MainSealLevelUpTipsWindow.OnClose
**Requires:**
- ExploreDevelop_SealLevelUpTipsWindowByName
**Snippet:**
```lua
require("ExploreDevelop_SealLevelUpTipsWindowByName")
local MainSealLevelUpTipsWindow = {}
local uis, contentPane, levelUpOrQualityUp, jobIndex
local GetMainSealTitle = function(job, level, quality)
  local prefix = T(20699 + quality)
  local suffix
  if quality > 0 then
    local conf = SealData.GetMainSealQualityUpConfig(job, quality - 1)
    suffix = level - conf.level_max
  else
```

---

## MP/MapChoiceWindow.lua.lua
**Functions:**
- MapChoiceWindow.ReInitData
- MapChoiceWindow.OnInit
- MapChoiceWindow.UpdateInfo
- MapChoiceWindow.UpdateCurSelectMap
- buffWordList.itemRenderer
- MapChoiceWindow.RenderItem
- mapBuffList.itemRenderer
- MapChoiceWindow.InitBtn
- MapChoiceWindow.OnShown
- MapChoiceWindow.OnHide
- MapChoiceWindow.OnClose
- MapChoiceWindow.HandleMessage
**Requires:**
- Formation_MapChoiceWindowByName
**Snippet:**
```lua
require("Formation_MapChoiceWindowByName")
local MapChoiceWindow = {}
local uis, contentPane, lastMapId, curMapId, ownMaps

function MapChoiceWindow.ReInitData()
end

function MapChoiceWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.MapChoiceWindow.package, WinResConfig.MapChoiceWindow.comName, function(com)
    contentPane = com
```

---

## MP/MapTipsWindow.lua.lua
**Functions:**
- MapTipsWindow.ReInitData
- MapTipsWindow.OnInit
- MapTipsWindow.UpdateInfo
- list.itemRenderer
- buffList.itemRenderer
- MapTipsWindow.InitBtn
- MapTipsWindow.OnClose
**Requires:**
- Message_MapTipsWindowByName
**Snippet:**
```lua
require("Message_MapTipsWindowByName")
local MapTipsWindow = {}
local uis, contentPane

function MapTipsWindow.ReInitData()
end

function MapTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.MapTipsWindow.package, WinResConfig.MapTipsWindow.comName, function(com)
    contentPane = com
```

---

## MP/MathUtil.lua.lua
**Functions:**
- MathUtil.GetVector3Dot
- MathUtil.GetVector3Cross
- MathUtil.GetVector3Module
- MathUtil.GetVector3Angle
- MathUtil.GetNormVector3
- MathUtil.GetVector3Scale
- MathUtil.GetVector3Subtract
- MathUtil.GetVector3Add
- MathUtil.RotationWithY
- MathUtil.GetProjection
- MathUtil.GetDistanceToLine
- MathUtil.FormatFloatNum
- MathUtil.TruncateFloat
- MathUtil.TruncateFloatN
**Snippet:**
```lua
local MathUtil = {}
local m_sqrt = math.sqrt
local m_acos = math.acos
local m_sin = math.sin
local m_pi = math.pi

function MathUtil.GetVector3Dot(v1, v2)
  return v1.x * v2.x + v1.y * v2.y + v1.z * v2.z
end

```

---

## MP/MessageBox.lua.lua
**Functions:**
- MessageBox.Show
**Snippet:**
```lua
local MessageBox = {}

function MessageBox.Show(content, sureBtnParam, cancelBtnParam, touchScreenBtnParam, returnBtnParam, layer, checkboxParam)
  local tb = {}
  tb.text = content
  tb.sureBtnParam = sureBtnParam
  tb.cancelBtnParam = cancelBtnParam
  tb.touchScreenBtnParam = touchScreenBtnParam
  tb.returnBtnParam = returnBtnParam
  tb.checkboxParam = checkboxParam
```

---

## MP/MessageScriptList.lua.lua
**Requires:**
- MessageService
**Snippet:**
```lua
local require = require
require("MessageService")
```

---

## MP/MessageService.lua.lua
**Functions:**
- MessageService.Init
- MessageService.ExchangeCardFragmentReq
- MessageService.ExchangeCardFragmentRsp
**Snippet:**
```lua
MessageService = {}

function MessageService.Init()
  Net.AddListener(Proto.MsgName.ExchangeCardFragmentRsp, MessageService.ExchangeCardFragmentRsp)
end

function MessageService.ExchangeCardFragmentReq(id, count, targetId)
  local msg = {}
  msg.itemId = id
  msg.count = count
```

---

## MP/Message_AddBtnByName.lua.lua
**Functions:**
- GetMessage_AddBtnUis
**Snippet:**
```lua
function GetMessage_AddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_AssetsTipsGroupByName.lua.lua
**Functions:**
- GetMessage_AssetsTipsGroupUis
**Snippet:**
```lua
function GetMessage_AssetsTipsGroupUis(ui)
  local uis = {}
  
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.root = ui
  return uis
end
```

---

## MP/Message_BadgeDetailsInfo1ByName.lua.lua
**Functions:**
- GetMessage_BadgeDetailsInfo1Uis
**Requires:**
- Message_BadgeDetailsInfo1_1ByName
**Snippet:**
```lua
require("Message_BadgeDetailsInfo1_1ByName")

function GetMessage_BadgeDetailsInfo1Uis(ui)
  local uis = {}
  uis.BadgeDetailsInfo1_1 = GetMessage_BadgeDetailsInfo1_1Uis(ui:GetChild("BadgeDetailsInfo1_1"))
  uis.AttributeList = ui:GetChild("AttributeList")
  uis.root = ui
  return uis
end
```

---

## MP/Message_BadgeDetailsInfo1_1ByName.lua.lua
**Functions:**
- GetMessage_BadgeDetailsInfo1_1Uis
**Snippet:**
```lua
function GetMessage_BadgeDetailsInfo1_1Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_BadgeDetailsInfo1_2ByName.lua.lua
**Functions:**
- GetMessage_BadgeDetailsInfo1_2Uis
**Snippet:**
```lua
function GetMessage_BadgeDetailsInfo1_2Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_BadgeDetailsInfo2ByName.lua.lua
**Functions:**
- GetMessage_BadgeDetailsInfo2Uis
**Snippet:**
```lua
function GetMessage_BadgeDetailsInfo2Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SuitList = ui:GetChild("SuitList")
  uis.root = ui
  return uis
end
```

---

## MP/Message_BadgeDetailsInfo2_1ByName.lua.lua
**Functions:**
- GetMessage_BadgeDetailsInfo2_1Uis
**Snippet:**
```lua
function GetMessage_BadgeDetailsInfo2_1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_BadgeGetStarByName.lua.lua
**Functions:**
- GetMessage_BadgeGetStarUis
**Snippet:**
```lua
function GetMessage_BadgeGetStarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## MP/Message_BadgeGetTipsByName.lua.lua
**Functions:**
- GetMessage_BadgeGetTipsUis
**Requires:**
- CommonResource_PopupBgByName
- Message_BadgeGetWayByName
- Message_BadgeGetTipsNumberByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Message_BadgeGetWayByName")
require("Message_BadgeGetTipsNumberByName")

function GetMessage_BadgeGetTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.PicLoaderr = ui:GetChild("PicLoaderr")
  uis.NameTxt = ui:GetChild("NameTxt")
```

---

## MP/Message_BadgeGetTipsNumberByName.lua.lua
**Functions:**
- GetMessage_BadgeGetTipsNumberUis
**Snippet:**
```lua
function GetMessage_BadgeGetTipsNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_BadgeGetTipsWindowByName.lua.lua
**Functions:**
- GetMessage_BadgeGetTipsWindowUis
**Requires:**
- Message_BadgeGetTipsByName
**Snippet:**
```lua
require("Message_BadgeGetTipsByName")

function GetMessage_BadgeGetTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetMessage_BadgeGetTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_BadgeGetTipsWordByName.lua.lua
**Functions:**
- GetMessage_BadgeGetTipsWordUis
**Snippet:**
```lua
function GetMessage_BadgeGetTipsWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.UseTxt = ui:GetChild("UseTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_BadgeGetWayByName.lua.lua
**Functions:**
- GetMessage_BadgeGetWayUis
**Snippet:**
```lua
function GetMessage_BadgeGetWayUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.GetStripList = ui:GetChild("GetStripList")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## MP/Message_BadgeInfoLockByName.lua.lua
**Functions:**
- GetMessage_BadgeInfoLockUis
**Snippet:**
```lua
function GetMessage_BadgeInfoLockUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_BadgeInfoStarByName.lua.lua
**Functions:**
- GetMessage_BadgeInfoStarUis
**Snippet:**
```lua
function GetMessage_BadgeInfoStarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## MP/Message_BadgeInfoTipsByName.lua.lua
**Functions:**
- GetMessage_BadgeInfoTipsUis
**Requires:**
- CommonResource_PopupBgByName
- Message_BadgeInfoWayByName
- Message_BadgeInfoLockByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Message_BadgeInfoWayByName")
require("Message_BadgeInfoLockByName")

function GetMessage_BadgeInfoTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.PicLoaderr = ui:GetChild("PicLoaderr")
  uis.NameTxt = ui:GetChild("NameTxt")
```

---

## MP/Message_BadgeInfoTipsWindowByName.lua.lua
**Functions:**
- GetMessage_BadgeInfoTipsWindowUis
**Requires:**
- Message_BadgeInfoTipsByName
**Snippet:**
```lua
require("Message_BadgeInfoTipsByName")

function GetMessage_BadgeInfoTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetMessage_BadgeInfoTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_BadgeInfoWayByName.lua.lua
**Functions:**
- GetMessage_BadgeInfoWayUis
**Snippet:**
```lua
function GetMessage_BadgeInfoWayUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.GetStripList = ui:GetChild("GetStripList")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## MP/Message_BadgeStarByName.lua.lua
**Functions:**
- GetMessage_BadgeStarUis
**Requires:**
- Message_BadgeStarPicByName
**Snippet:**
```lua
require("Message_BadgeStarPicByName")

function GetMessage_BadgeStarUis(ui)
  local uis = {}
  uis.BadgeStar1 = GetMessage_BadgeStarPicUis(ui:GetChild("BadgeStar1"))
  uis.BadgeStar2 = GetMessage_BadgeStarPicUis(ui:GetChild("BadgeStar2"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_BadgeStarPicByName.lua.lua
**Functions:**
- GetMessage_BadgeStarPicUis
**Snippet:**
```lua
function GetMessage_BadgeStarPicUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_BadgeUnknownDetailsInfo1ByName.lua.lua
**Functions:**
- GetMessage_BadgeUnknownDetailsInfo1Uis
**Snippet:**
```lua
function GetMessage_BadgeUnknownDetailsInfo1Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SuitList = ui:GetChild("SuitList")
  uis.root = ui
  return uis
end
```

---

## MP/Message_BadgeUnknownDetailsInfo1_1ByName.lua.lua
**Functions:**
- GetMessage_BadgeUnknownDetailsInfo1_1Uis
**Snippet:**
```lua
function GetMessage_BadgeUnknownDetailsInfo1_1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_BadgeUnknownStarByName.lua.lua
**Functions:**
- GetMessage_BadgeUnknownStarUis
**Snippet:**
```lua
function GetMessage_BadgeUnknownStarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## MP/Message_BadgeUnknownTipsByName.lua.lua
**Functions:**
- GetMessage_BadgeUnknownTipsUis
**Requires:**
- CommonResource_PopupBgByName
- Message_BadgeUnknownWayByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Message_BadgeUnknownWayByName")

function GetMessage_BadgeUnknownTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.PicLoaderr = ui:GetChild("PicLoaderr")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordList = ui:GetChild("WordList")
```

---

## MP/Message_BadgeUnknownTipsWindowByName.lua.lua
**Functions:**
- GetMessage_BadgeUnknownTipsWindowUis
**Requires:**
- Message_BadgeUnknownTipsByName
**Snippet:**
```lua
require("Message_BadgeUnknownTipsByName")

function GetMessage_BadgeUnknownTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetMessage_BadgeUnknownTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_BadgeUnknownWayByName.lua.lua
**Functions:**
- GetMessage_BadgeUnknownWayUis
**Snippet:**
```lua
function GetMessage_BadgeUnknownWayUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.GetStripList = ui:GetChild("GetStripList")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## MP/Message_BreachAttributeByName.lua.lua
**Functions:**
- GetMessage_BreachAttributeUis
**Requires:**
- Message_BreachAttributeContentByName
**Snippet:**
```lua
require("Message_BreachAttributeContentByName")

function GetMessage_BreachAttributeUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.BreachSkillContent = GetMessage_BreachAttributeContentUis(ui:GetChild("BreachSkillContent"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_BreachAttributeContentByName.lua.lua
**Functions:**
- GetMessage_BreachAttributeContentUis
**Snippet:**
```lua
function GetMessage_BreachAttributeContentUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_BreachClothesByName.lua.lua
**Functions:**
- GetMessage_BreachClothesUis
**Snippet:**
```lua
function GetMessage_BreachClothesUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_BreachGiftChoiceBtnByName.lua.lua
**Functions:**
- GetMessage_BreachGiftChoiceBtnUis
**Snippet:**
```lua
function GetMessage_BreachGiftChoiceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_BreachGiftChoiceByName.lua.lua
**Functions:**
- GetMessage_BreachGiftChoiceUis
**Snippet:**
```lua
function GetMessage_BreachGiftChoiceUis(ui)
  local uis = {}
  
  uis.ChoiceBtn = ui:GetChild("ChoiceBtn")
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## MP/Message_BreachGiftModularByName.lua.lua
**Functions:**
- GetMessage_BreachGiftModularUis
**Snippet:**
```lua
function GetMessage_BreachGiftModularUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.Popup_S_Black_Btn = ui:GetChild("Popup_S_Black_Btn")
  uis.Popup_S_Green_Btn = ui:GetChild("Popup_S_Green_Btn")
  uis.root = ui
  return uis
```

---

## MP/Message_BreachLevelByName.lua.lua
**Functions:**
- GetMessage_BreachLevelUis
**Snippet:**
```lua
function GetMessage_BreachLevelUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_BreachSkillByName.lua.lua
**Functions:**
- GetMessage_BreachSkillUis
**Snippet:**
```lua
function GetMessage_BreachSkillUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SkillTxt = ui:GetChild("SkillTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_BreachTipsByName.lua.lua
**Functions:**
- GetMessage_BreachTipsUis
**Requires:**
- CommonResource_PopupBgByName
- CommonResource_CardBreachByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("CommonResource_CardBreachByName")

function GetMessage_BreachTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.CardBreach = GetCommonResource_CardBreachUis(ui:GetChild("CardBreach"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.BreachBtnList = ui:GetChild("BreachBtnList")
```

---

## MP/Message_BreachTipsWindowByName.lua.lua
**Functions:**
- GetMessage_BreachTipsWindowUis
**Requires:**
- Message_BreachTipsByName
**Snippet:**
```lua
require("Message_BreachTipsByName")

function GetMessage_BreachTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetMessage_BreachTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_BtnGroupByName.lua.lua
**Functions:**
- GetMessage_BtnGroupUis
**Snippet:**
```lua
function GetMessage_BtnGroupUis(ui)
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

## MP/Message_BuyItemByName.lua.lua
**Functions:**
- GetMessage_BuyItemUis
**Snippet:**
```lua
function GetMessage_BuyItemUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_BuyItemContentByName.lua.lua
**Functions:**
- GetMessage_BuyItemContentUis
**Requires:**
- Message_BuyItemByName
**Snippet:**
```lua
require("Message_BuyItemByName")

function GetMessage_BuyItemContentUis(ui)
  local uis = {}
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.Item = GetMessage_BuyItemUis(ui:GetChild("Item"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_CardAttributeByName.lua.lua
**Functions:**
- GetMessage_CardAttributeUis
**Requires:**
- CommonResource_OccupationByName
**Snippet:**
```lua
require("CommonResource_OccupationByName")

function GetMessage_CardAttributeUis(ui)
  local uis = {}
  uis.Occupation = GetCommonResource_OccupationUis(ui:GetChild("Occupation"))
  uis.ElementList = ui:GetChild("ElementList")
  uis.StarList = ui:GetChild("StarList")
  uis.root = ui
  return uis
end
```

---

## MP/Message_CardBreachBtnByName.lua.lua
**Functions:**
- GetMessage_CardBreachBtnUis
**Requires:**
- CommonResource_CardBreachByName
**Snippet:**
```lua
require("CommonResource_CardBreachByName")

function GetMessage_CardBreachBtnUis(ui)
  local uis = {}
  uis.CardBreach = GetCommonResource_CardBreachUis(ui:GetChild("CardBreach"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/Message_CardBreachByName.lua.lua
**Functions:**
- GetMessage_CardBreachUis
**Requires:**
- CommonResource_CardBreachByName
**Snippet:**
```lua
require("CommonResource_CardBreachByName")

function GetMessage_CardBreachUis(ui)
  local uis = {}
  uis.CardBreach1 = GetCommonResource_CardBreachUis(ui:GetChild("CardBreach1"))
  uis.CardBreach2 = GetCommonResource_CardBreachUis(ui:GetChild("CardBreach2"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_CardChangeModularByName.lua.lua
**Functions:**
- GetMessage_CardChangeModularUis
**Snippet:**
```lua
function GetMessage_CardChangeModularUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.CardList = ui:GetChild("CardList")
  uis.root = ui
  return uis
end
```

---

## MP/Message_CardDetailsModularByName.lua.lua
**Functions:**
- GetMessage_CardDetailsModularUis
**Requires:**
- Message_CardPicByName
- Message_CardNameByName
- Message_CardAttributeByName
**Snippet:**
```lua
require("Message_CardPicByName")
require("Message_CardNameByName")
require("Message_CardAttributeByName")

function GetMessage_CardDetailsModularUis(ui)
  local uis = {}
  uis.CardPic = GetMessage_CardPicUis(ui:GetChild("CardPic"))
  uis.CardName = GetMessage_CardNameUis(ui:GetChild("CardName"))
  uis.CardAttribute = GetMessage_CardAttributeUis(ui:GetChild("CardAttribute"))
  uis.SkillList = ui:GetChild("SkillList")
```

---

## MP/Message_CardHeadAniByName.lua.lua
**Functions:**
- GetMessage_CardHeadAniUis
**Snippet:**
```lua
function GetMessage_CardHeadAniUis(ui)
  local uis = {}
  
  uis.CardHeadBtn = ui:GetChild("CardHeadBtn")
  uis.root = ui
  return uis
end
```

---

## MP/Message_CardHeadBgByName.lua.lua
**Functions:**
- GetMessage_CardHeadBgUis
**Snippet:**
```lua
function GetMessage_CardHeadBgUis(ui)
  local uis = {}
  
  uis.CardPicLoader = ui:GetChild("CardPicLoader")
  uis.root = ui
  return uis
end
```

---

## MP/Message_CardHeadBtnByName.lua.lua
**Functions:**
- GetMessage_CardHeadBtnUis
**Requires:**
- Message_CardHeadBgByName
- CommonResource_OccupationByName
**Snippet:**
```lua
require("Message_CardHeadBgByName")
require("CommonResource_OccupationByName")

function GetMessage_CardHeadBtnUis(ui)
  local uis = {}
  uis.CardPic = GetMessage_CardHeadBgUis(ui:GetChild("CardPic"))
  uis.Occupation = GetCommonResource_OccupationUis(ui:GetChild("Occupation"))
  uis.ElementList = ui:GetChild("ElementList")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.StarList = ui:GetChild("StarList")
```

---

## MP/Message_CardListByName.lua.lua
**Functions:**
- GetMessage_CardListUis
**Snippet:**
```lua
function GetMessage_CardListUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.CardList = ui:GetChild("CardList")
  uis.root = ui
  return uis
end
```

---

## MP/Message_CardNameByName.lua.lua
**Functions:**
- GetMessage_CardNameUis
**Snippet:**
```lua
function GetMessage_CardNameUis(ui)
  local uis = {}
  
  uis.Name1Txt = ui:GetChild("Name1Txt")
  uis.Name2Txt = ui:GetChild("Name2Txt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_CardPicByName.lua.lua
**Functions:**
- GetMessage_CardPicUis
**Snippet:**
```lua
function GetMessage_CardPicUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## MP/Message_CardSkillByName.lua.lua
**Functions:**
- GetMessage_CardSkillUis
**Snippet:**
```lua
function GetMessage_CardSkillUis(ui)
  local uis = {}
  
  uis.Pic1Loader = ui:GetChild("Pic1Loader")
  uis.Pic2Loader = ui:GetChild("Pic2Loader")
  uis.Level1Txt = ui:GetChild("Level1Txt")
  uis.Level2Txt = ui:GetChild("Level2Txt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_ClothesCardAniByName.lua.lua
**Functions:**
- GetMessage_ClothesCardAniUis
**Snippet:**
```lua
function GetMessage_ClothesCardAniUis(ui)
  local uis = {}
  
  uis.ClothesCardBtn = ui:GetChild("ClothesCardBtn")
  uis.root = ui
  return uis
end
```

---

## MP/Message_ClothesCardBtnByName.lua.lua
**Functions:**
- GetMessage_ClothesCardBtnUis
**Snippet:**
```lua
function GetMessage_ClothesCardBtnUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.ClothesNameTxt = ui:GetChild("ClothesNameTxt")
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## MP/Message_ClothesChangeModularByName.lua.lua
**Functions:**
- GetMessage_ClothesChangeModularUis
**Snippet:**
```lua
function GetMessage_ClothesChangeModularUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.ClothesList = ui:GetChild("ClothesList")
  uis.root = ui
  return uis
end
```

---

## MP/Message_ClothesDetailsModularByName.lua.lua
**Functions:**
- GetMessage_ClothesDetailsModularUis
**Snippet:**
```lua
function GetMessage_ClothesDetailsModularUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Popup_S_Black_Btn = ui:GetChild("Popup_S_Black_Btn")
  uis.Popup_S_Green_Btn = ui:GetChild("Popup_S_Green_Btn")
  uis.ClothesNameTxt = ui:GetChild("ClothesNameTxt")
  uis.Name1Txt = ui:GetChild("Name1Txt")
  uis.Name2Txt = ui:GetChild("Name2Txt")
```

---

## MP/Message_Code1ByName.lua.lua
**Functions:**
- GetMessage_Code1Uis
**Snippet:**
```lua
function GetMessage_Code1Uis(ui)
  local uis = {}
  
  uis.NameInTxt = ui:GetChild("NameInTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_Code2ByName.lua.lua
**Functions:**
- GetMessage_Code2Uis
**Requires:**
- CommonResource_PopupBgByName
- CommonResource_Popup_BByName
- Message_Code1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("CommonResource_Popup_BByName")
require("Message_Code1ByName")

function GetMessage_Code2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Popup_B = GetCommonResource_Popup_BUis(ui:GetChild("Popup_B"))
  uis.Code1 = GetMessage_Code1Uis(ui:GetChild("Code1"))
```

---

## MP/Message_CodeWindowByName.lua.lua
**Functions:**
- GetMessage_CodeWindowUis
**Requires:**
- Message_Code2ByName
**Snippet:**
```lua
require("Message_Code2ByName")

function GetMessage_CodeWindowUis(ui)
  local uis = {}
  uis.Main = GetMessage_Code2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_Currency1ByName.lua.lua
**Functions:**
- GetMessage_Currency1Uis
**Snippet:**
```lua
function GetMessage_Currency1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.ChoiceBtn = ui:GetChild("ChoiceBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## MP/Message_Currency1ChoiceBtnByName.lua.lua
**Functions:**
- GetMessage_Currency1ChoiceBtnUis
**Snippet:**
```lua
function GetMessage_Currency1ChoiceBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/Message_Currency2ByName.lua.lua
**Functions:**
- GetMessage_Currency2Uis
**Requires:**
- CommonResource_PopupBgByName
- CommonResource_Popup_BByName
- Message_Currency1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("CommonResource_Popup_BByName")
require("Message_Currency1ByName")

function GetMessage_Currency2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Popup_B = GetCommonResource_Popup_BUis(ui:GetChild("Popup_B"))
  uis.Currency1 = GetMessage_Currency1Uis(ui:GetChild("Currency1"))
```

---

## MP/Message_CurrencyWindowByName.lua.lua
**Functions:**
- GetMessage_CurrencyWindowUis
**Requires:**
- Message_Currency2ByName
**Snippet:**
```lua
require("Message_Currency2ByName")

function GetMessage_CurrencyWindowUis(ui)
  local uis = {}
  uis.Main = GetMessage_Currency2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_DebrisByName.lua.lua
**Functions:**
- GetMessage_DebrisUis
**Requires:**
- CommonResource_BackGroundByName
- CommonResource_ItemFrameByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("CommonResource_ItemFrameByName")

function GetMessage_DebrisUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Item1 = GetCommonResource_ItemFrameUis(ui:GetChild("Item1"))
  uis.Item2 = GetCommonResource_ItemFrameUis(ui:GetChild("Item2"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TipsTxt = ui:GetChild("TipsTxt")
```

---

## MP/Message_DebrisCloseBtnByName.lua.lua
**Functions:**
- GetMessage_DebrisCloseBtnUis
**Snippet:**
```lua
function GetMessage_DebrisCloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/Message_DebrisSureBtnByName.lua.lua
**Functions:**
- GetMessage_DebrisSureBtnUis
**Snippet:**
```lua
function GetMessage_DebrisSureBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/Message_DebrisWindowByName.lua.lua
**Functions:**
- GetMessage_DebrisWindowUis
**Requires:**
- Message_DebrisByName
**Snippet:**
```lua
require("Message_DebrisByName")

function GetMessage_DebrisWindowUis(ui)
  local uis = {}
  uis.Main = GetMessage_DebrisUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_DemanBadgeBgByName.lua.lua
**Functions:**
- GetMessage_DemanBadgeBgUis
**Snippet:**
```lua
function GetMessage_DemanBadgeBgUis(ui)
  local uis = {}
  
  uis.CardPicLoader = ui:GetChild("CardPicLoader")
  uis.root = ui
  return uis
end
```

---

## MP/Message_DemandItemByName.lua.lua
**Functions:**
- GetMessage_DemandItemUis
**Snippet:**
```lua
function GetMessage_DemandItemUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_DemanHeadBgByName.lua.lua
**Functions:**
- GetMessage_DemanHeadBgUis
**Snippet:**
```lua
function GetMessage_DemanHeadBgUis(ui)
  local uis = {}
  
  uis.CardPicLoader = ui:GetChild("CardPicLoader")
  uis.root = ui
  return uis
end
```

---

## MP/Message_DemanHeadByName.lua.lua
**Functions:**
- GetMessage_DemanHeadUis
**Requires:**
- Message_DemanHeadBgByName
- Message_DemanBadgeBgByName
**Snippet:**
```lua
require("Message_DemanHeadBgByName")
require("Message_DemanBadgeBgByName")

function GetMessage_DemanHeadUis(ui)
  local uis = {}
  uis.HeadBg = GetMessage_DemanHeadBgUis(ui:GetChild("HeadBg"))
  uis.BadgeBg = GetMessage_DemanBadgeBgUis(ui:GetChild("BadgeBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.headCtr = ui:GetController("head")
  uis.buttonCtr = ui:GetController("button")
```

---

## MP/Message_DetailsAllSkillByName.lua.lua
**Functions:**
- GetMessage_DetailsAllSkillUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetMessage_DetailsAllSkillUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.SpclSkillTipsList = ui:GetChild("SpclSkillTipsList")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.root = ui
  return uis
```

---

## MP/Message_DetailsAllSkillWindowByName.lua.lua
**Functions:**
- GetMessage_DetailsAllSkillWindowUis
**Requires:**
- Message_DetailsAllSkillByName
**Snippet:**
```lua
require("Message_DetailsAllSkillByName")

function GetMessage_DetailsAllSkillWindowUis(ui)
  local uis = {}
  uis.Main = GetMessage_DetailsAllSkillUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_DetailsBtnByName.lua.lua
**Functions:**
- GetMessage_DetailsBtnUis
**Requires:**
- Message_TokensUseMarkByName
**Snippet:**
```lua
require("Message_TokensUseMarkByName")

function GetMessage_DetailsBtnUis(ui)
  local uis = {}
  uis.UseMark = GetMessage_TokensUseMarkUis(ui:GetChild("UseMark"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/Message_DetailsModularByName.lua.lua
**Functions:**
- GetMessage_DetailsModularUis
**Snippet:**
```lua
function GetMessage_DetailsModularUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.Popup_S_Black_Btn = ui:GetChild("Popup_S_Black_Btn")
  uis.Popup_S_Green_Btn = ui:GetChild("Popup_S_Green_Btn")
  uis.Popup_B_Green_Btn = ui:GetChild("Popup_B_Green_Btn")
  uis.c1Ctr = ui:GetController("c1")
```

---

## MP/Message_DetailsSkillIconByName.lua.lua
**Functions:**
- GetMessage_DetailsSkillIconUis
**Requires:**
- CommonResource_SkillByName
- CommonResource_SkillDetailsCDByName
- CommonResource_SkillDetailsTagByName
**Snippet:**
```lua
require("CommonResource_SkillByName")
require("CommonResource_SkillDetailsCDByName")
require("CommonResource_SkillDetailsTagByName")

function GetMessage_DetailsSkillIconUis(ui)
  local uis = {}
  uis.Skill = GetCommonResource_SkillUis(ui:GetChild("Skill"))
  uis.SkillDetailsCD = GetCommonResource_SkillDetailsCDUis(ui:GetChild("SkillDetailsCD"))
  uis.SkillDetailsTag = GetCommonResource_SkillDetailsTagUis(ui:GetChild("SkillDetailsTag"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## MP/Message_DetailsSkillInfo1ByName.lua.lua
**Functions:**
- GetMessage_DetailsSkillInfo1Uis
**Snippet:**
```lua
function GetMessage_DetailsSkillInfo1Uis(ui)
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

## MP/Message_DetailsSkillInfo2ByName.lua.lua
**Functions:**
- GetMessage_DetailsSkillInfo2Uis
**Snippet:**
```lua
function GetMessage_DetailsSkillInfo2Uis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_DetailsSkillInfoByName.lua.lua
**Functions:**
- GetMessage_DetailsSkillInfoUis
**Snippet:**
```lua
function GetMessage_DetailsSkillInfoUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.SkillList = ui:GetChild("SkillList")
  uis.root = ui
  return uis
end
```

---

## MP/Message_DetailsSkillTipsAniByName.lua.lua
**Functions:**
- GetMessage_DetailsSkillTipsAniUis
**Requires:**
- Message_SkillLeaderLcokByName
**Snippet:**
```lua
require("Message_SkillLeaderLcokByName")

function GetMessage_DetailsSkillTipsAniUis(ui)
  local uis = {}
  uis.TipsList = ui:GetChild("TipsList")
  uis.SkillLeaderLcok = GetMessage_SkillLeaderLcokUis(ui:GetChild("SkillLeaderLcok"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_DetailsSkillTipsByName.lua.lua
**Functions:**
- GetMessage_DetailsSkillTipsUis
**Requires:**
- Message_DetailsSkillIconByName
- Message_DetailsSkillInfoByName
- Message_DetailsSkillInfo2ByName
**Snippet:**
```lua
require("Message_DetailsSkillIconByName")
require("Message_DetailsSkillInfoByName")
require("Message_DetailsSkillInfo2ByName")

function GetMessage_DetailsSkillTipsUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.DetailsSkillIcon = GetMessage_DetailsSkillIconUis(ui:GetChild("DetailsSkillIcon"))
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
```

---

## MP/Message_DiscountByName.lua.lua
**Functions:**
- GetMessage_DiscountUis
**Snippet:**
```lua
function GetMessage_DiscountUis(ui)
  local uis = {}
  
  uis.DiscountTxt = ui:GetChild("DiscountTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_DispatchNumber1ByName.lua.lua
**Functions:**
- GetMessage_DispatchNumber1Uis
**Requires:**
- Message_HU_NumberStripByName
**Snippet:**
```lua
require("Message_HU_NumberStripByName")

function GetMessage_DispatchNumber1Uis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberStrip = GetMessage_HU_NumberStripUis(ui:GetChild("NumberStrip"))
  uis.ReasonTxt = ui:GetChild("ReasonTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_DispatchNumber2ByName.lua.lua
**Functions:**
- GetMessage_DispatchNumber2Uis
**Requires:**
- CommonResource_PopupBgByName
- CommonResource_Popup_BByName
- Message_DispatchNumber1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("CommonResource_Popup_BByName")
require("Message_DispatchNumber1ByName")

function GetMessage_DispatchNumber2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Popup_B = GetCommonResource_Popup_BUis(ui:GetChild("Popup_B"))
  uis.DispatchNumber1 = GetMessage_DispatchNumber1Uis(ui:GetChild("DispatchNumber1"))
```

---

## MP/Message_DispatchNumberWindowByName.lua.lua
**Functions:**
- GetMessage_DispatchNumberWindowUis
**Requires:**
- Message_DispatchNumber2ByName
**Snippet:**
```lua
require("Message_DispatchNumber2ByName")

function GetMessage_DispatchNumberWindowUis(ui)
  local uis = {}
  uis.Main = GetMessage_DispatchNumber2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_DispatchReward1ByName.lua.lua
**Functions:**
- GetMessage_DispatchReward1Uis
**Requires:**
- Message_DispatchRewardTitleByName
**Snippet:**
```lua
require("Message_DispatchRewardTitleByName")

function GetMessage_DispatchReward1Uis(ui)
  local uis = {}
  uis.DispatchRewardTitle = GetMessage_DispatchRewardTitleUis(ui:GetChild("DispatchRewardTitle"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_DispatchReward2ByName.lua.lua
**Functions:**
- GetMessage_DispatchReward2Uis
**Requires:**
- CommonResource_PopupBgByName
- Message_Popup_BByName
- Message_DispatchReward1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Message_Popup_BByName")
require("Message_DispatchReward1ByName")

function GetMessage_DispatchReward2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Popup_B = GetMessage_Popup_BUis(ui:GetChild("Popup_B"))
  uis.DispatchReward1 = GetMessage_DispatchReward1Uis(ui:GetChild("DispatchReward1"))
```

---

## MP/Message_DispatchRewardShowWindowByName.lua.lua
**Functions:**
- GetMessage_DispatchRewardShowWindowUis
**Requires:**
- Message_DispatchReward2ByName
**Snippet:**
```lua
require("Message_DispatchReward2ByName")

function GetMessage_DispatchRewardShowWindowUis(ui)
  local uis = {}
  uis.Main = GetMessage_DispatchReward2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_DispatchRewardTitleByName.lua.lua
**Functions:**
- GetMessage_DispatchRewardTitleUis
**Snippet:**
```lua
function GetMessage_DispatchRewardTitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_ExploreGetTipsByName.lua.lua
**Functions:**
- GetMessage_ExploreGetTipsUis
**Requires:**
- CommonResource_PopupBgByName
- Message_ExploreGetWayByName
- Message_ExploreGetTipsNumberByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Message_ExploreGetWayByName")
require("Message_ExploreGetTipsNumberByName")

function GetMessage_ExploreGetTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.PicLoaderr = ui:GetChild("PicLoaderr")
  uis.NameTxt = ui:GetChild("NameTxt")
```

---

## MP/Message_ExploreGetTipsNumberByName.lua.lua
**Functions:**
- GetMessage_ExploreGetTipsNumberUis
**Snippet:**
```lua
function GetMessage_ExploreGetTipsNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_ExploreGetTipsWindowByName.lua.lua
**Functions:**
- GetMessage_ExploreGetTipsWindowUis
**Requires:**
- Message_ExploreGetTipsByName
**Snippet:**
```lua
require("Message_ExploreGetTipsByName")

function GetMessage_ExploreGetTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetMessage_ExploreGetTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_ExploreGetTipsWordByName.lua.lua
**Functions:**
- GetMessage_ExploreGetTipsWordUis
**Snippet:**
```lua
function GetMessage_ExploreGetTipsWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.UseTxt = ui:GetChild("UseTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_ExploreGetWayByName.lua.lua
**Functions:**
- GetMessage_ExploreGetWayUis
**Snippet:**
```lua
function GetMessage_ExploreGetWayUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.GetStripList = ui:GetChild("GetStripList")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## MP/Message_FloatTipsByName.lua.lua
**Functions:**
- GetMessage_FloatTipsUis
**Snippet:**
```lua
function GetMessage_FloatTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_FloatTipsUnitByName.lua.lua
**Functions:**
- GetMessage_FloatTipsUnitUis
**Requires:**
- Message_FloatTipsByName
**Snippet:**
```lua
require("Message_FloatTipsByName")

function GetMessage_FloatTipsUnitUis(ui)
  local uis = {}
  uis.FloatTips = GetMessage_FloatTipsUis(ui:GetChild("FloatTips"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_GetStripBtnByName.lua.lua
**Functions:**
- GetMessage_GetStripBtnUis
**Requires:**
- Message_ItemLabelWordByName
- Message_GetStripLockByName
**Snippet:**
```lua
require("Message_ItemLabelWordByName")
require("Message_GetStripLockByName")

function GetMessage_GetStripBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemLabelWord = GetMessage_ItemLabelWordUis(ui:GetChild("ItemLabelWord"))
  uis.GetStripLock = GetMessage_GetStripLockUis(ui:GetChild("GetStripLock"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## MP/Message_GetStripLockByName.lua.lua
**Functions:**
- GetMessage_GetStripLockUis
**Snippet:**
```lua
function GetMessage_GetStripLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_GiftBuyPrice1ByName.lua.lua
**Functions:**
- GetMessage_GiftBuyPrice1Uis
**Snippet:**
```lua
function GetMessage_GiftBuyPrice1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_GiftBuyPrice2ByName.lua.lua
**Functions:**
- GetMessage_GiftBuyPrice2Uis
**Snippet:**
```lua
function GetMessage_GiftBuyPrice2Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_GiftBuyPrice3ByName.lua.lua
**Functions:**
- GetMessage_GiftBuyPrice3Uis
**Snippet:**
```lua
function GetMessage_GiftBuyPrice3Uis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_GiftBuyPriceByName.lua.lua
**Functions:**
- GetMessage_GiftBuyPriceUis
**Requires:**
- Message_GiftBuyPrice1ByName
- Message_GiftBuyPrice2ByName
- Message_GiftBuyPrice3ByName
**Snippet:**
```lua
require("Message_GiftBuyPrice1ByName")
require("Message_GiftBuyPrice2ByName")
require("Message_GiftBuyPrice3ByName")

function GetMessage_GiftBuyPriceUis(ui)
  local uis = {}
  uis.GiftBuyPrice1 = GetMessage_GiftBuyPrice1Uis(ui:GetChild("GiftBuyPrice1"))
  uis.GiftBuyPrice2 = GetMessage_GiftBuyPrice2Uis(ui:GetChild("GiftBuyPrice2"))
  uis.GiftBuyPrice3 = GetMessage_GiftBuyPrice3Uis(ui:GetChild("GiftBuyPrice3"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## MP/Message_GiftDemandItemByName.lua.lua
**Functions:**
- GetMessage_GiftDemandItemUis
**Snippet:**
```lua
function GetMessage_GiftDemandItemUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## MP/Message_GiftLimitationNumberByName.lua.lua
**Functions:**
- GetMessage_GiftLimitationNumberUis
**Snippet:**
```lua
function GetMessage_GiftLimitationNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_GiftMonthTimeByName.lua.lua
**Functions:**
- GetMessage_GiftMonthTimeUis
**Snippet:**
```lua
function GetMessage_GiftMonthTimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_GiftNameByName.lua.lua
**Functions:**
- GetMessage_GiftNameUis
**Snippet:**
```lua
function GetMessage_GiftNameUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_GiftRewardListByName.lua.lua
**Functions:**
- GetMessage_GiftRewardListUis
**Requires:**
- Message_GiftRewardMonthListByName
**Snippet:**
```lua
require("Message_GiftRewardMonthListByName")

function GetMessage_GiftRewardListUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.GiftRewardMonthList = GetMessage_GiftRewardMonthListUis(ui:GetChild("GiftRewardMonthList"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## MP/Message_GiftRewardMonthListByName.lua.lua
**Functions:**
- GetMessage_GiftRewardMonthListUis
**Requires:**
- Message_GiftDemandItemByName
**Snippet:**
```lua
require("Message_GiftDemandItemByName")

function GetMessage_GiftRewardMonthListUis(ui)
  local uis = {}
  uis.OnceItem = GetMessage_GiftDemandItemUis(ui:GetChild("OnceItem"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## MP/Message_GiftTips1ByName.lua.lua
**Functions:**
- GetMessage_GiftTips1Uis
**Requires:**
- Message_GiftNameByName
- Message_GiftWordContentByName
- Message_GiftBuyPriceByName
- Message_LackWordByName
- Message_GiftRewardListByName
**Snippet:**
```lua
require("Message_GiftNameByName")
require("Message_GiftWordContentByName")
require("Message_GiftBuyPriceByName")
require("Message_LackWordByName")
require("Message_GiftRewardListByName")

function GetMessage_GiftTips1Uis(ui)
  local uis = {}
  uis.GiftName = GetMessage_GiftNameUis(ui:GetChild("GiftName"))
  uis.GiftWordContent = GetMessage_GiftWordContentUis(ui:GetChild("GiftWordContent"))
```

---

## MP/Message_GiftTips2BgByName.lua.lua
**Functions:**
- GetMessage_GiftTips2BgUis
**Snippet:**
```lua
function GetMessage_GiftTips2BgUis(ui)
  local uis = {}
  
  uis.PicHolder = ui:GetChild("PicHolder")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## MP/Message_GiftTips2ByName.lua.lua
**Functions:**
- GetMessage_GiftTips2Uis
**Requires:**
- Message_GiftTips2BgByName
- Message_GiftMonthTimeByName
**Snippet:**
```lua
require("Message_GiftTips2BgByName")
require("Message_GiftMonthTimeByName")

function GetMessage_GiftTips2Uis(ui)
  local uis = {}
  uis.Bg = GetMessage_GiftTips2BgUis(ui:GetChild("Bg"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.GiftMonthTime = GetMessage_GiftMonthTimeUis(ui:GetChild("GiftMonthTime"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## MP/Message_GiftTipsByName.lua.lua
**Functions:**
- GetMessage_GiftTipsUis
**Requires:**
- CommonResource_PopupBgByName
- Message_GiftTips1ByName
- Message_GiftTips2ByName
- Message_AssetsTipsGroupByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Message_GiftTips1ByName")
require("Message_GiftTips2ByName")
require("Message_AssetsTipsGroupByName")

function GetMessage_GiftTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.GiftTips1 = GetMessage_GiftTips1Uis(ui:GetChild("GiftTips1"))
```

---

## MP/Message_GiftTipsWindowByName.lua.lua
**Functions:**
- GetMessage_GiftTipsWindowUis
**Requires:**
- Message_GiftTipsByName
**Snippet:**
```lua
require("Message_GiftTipsByName")

function GetMessage_GiftTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetMessage_GiftTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_GiftWordContentByName.lua.lua
**Functions:**
- GetMessage_GiftWordContentUis
**Requires:**
- Message_GiftLimitationNumberByName
**Snippet:**
```lua
require("Message_GiftLimitationNumberByName")

function GetMessage_GiftWordContentUis(ui)
  local uis = {}
  uis.WordList = ui:GetChild("WordList")
  uis.GiftLimitationNumber = GetMessage_GiftLimitationNumberUis(ui:GetChild("GiftLimitationNumber"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_GoodsLevelByName.lua.lua
**Functions:**
- GetMessage_GoodsLevelUis
**Snippet:**
```lua
function GetMessage_GoodsLevelUis(ui)
  local uis = {}
  
  uis.UseTxt = ui:GetChild("UseTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_GoodsTimeByName.lua.lua
**Functions:**
- GetMessage_GoodsTimeUis
**Snippet:**
```lua
function GetMessage_GoodsTimeUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_Green_B_BtnByName.lua.lua
**Functions:**
- GetMessage_Green_B_BtnUis
**Snippet:**
```lua
function GetMessage_Green_B_BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/Message_Green_S_BtnByName.lua.lua
**Functions:**
- GetMessage_Green_S_BtnUis
**Snippet:**
```lua
function GetMessage_Green_S_BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/Message_HU_AddBtnByName.lua.lua
**Functions:**
- GetMessage_HU_AddBtnUis
**Snippet:**
```lua
function GetMessage_HU_AddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_HU_MaxBtnByName.lua.lua
**Functions:**
- GetMessage_HU_MaxBtnUis
**Snippet:**
```lua
function GetMessage_HU_MaxBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_HU_MinBtnByName.lua.lua
**Functions:**
- GetMessage_HU_MinBtnUis
**Snippet:**
```lua
function GetMessage_HU_MinBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_HU_NumberStripByName.lua.lua
**Functions:**
- GetMessage_HU_NumberStripUis
**Snippet:**
```lua
function GetMessage_HU_NumberStripUis(ui)
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

## MP/Message_HU_ReduceBtnByName.lua.lua
**Functions:**
- GetMessage_HU_ReduceBtnUis
**Snippet:**
```lua
function GetMessage_HU_ReduceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_ItemAddBtnByName.lua.lua
**Functions:**
- GetMessage_ItemAddBtnUis
**Snippet:**
```lua
function GetMessage_ItemAddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_ItemGetTimeByName.lua.lua
**Functions:**
- GetMessage_ItemGetTimeUis
**Snippet:**
```lua
function GetMessage_ItemGetTimeUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_ItemGetTipsByName.lua.lua
**Functions:**
- GetMessage_ItemGetTipsUis
**Requires:**
- CommonResource_PopupBgByName
- Message_ItemGetWayByName
- Message_ItemGetTipsNumberByName
- Message_ItemGetTimeByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Message_ItemGetWayByName")
require("Message_ItemGetTipsNumberByName")
require("Message_ItemGetTimeByName")

function GetMessage_ItemGetTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.PicLoaderr = ui:GetChild("PicLoaderr")
```

---

## MP/Message_ItemGetTipsNumberByName.lua.lua
**Functions:**
- GetMessage_ItemGetTipsNumberUis
**Snippet:**
```lua
function GetMessage_ItemGetTipsNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_ItemGetTipsWindowByName.lua.lua
**Functions:**
- GetMessage_ItemGetTipsWindowUis
**Requires:**
- Message_ItemGetTipsByName
**Snippet:**
```lua
require("Message_ItemGetTipsByName")

function GetMessage_ItemGetTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetMessage_ItemGetTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_ItemGetTipsWordByName.lua.lua
**Functions:**
- GetMessage_ItemGetTipsWordUis
**Snippet:**
```lua
function GetMessage_ItemGetTipsWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.UseTxt = ui:GetChild("UseTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_ItemGetWayByName.lua.lua
**Functions:**
- GetMessage_ItemGetWayUis
**Snippet:**
```lua
function GetMessage_ItemGetWayUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.GetStripList = ui:GetChild("GetStripList")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## MP/Message_ItemLabelWordByName.lua.lua
**Functions:**
- GetMessage_ItemLabelWordUis
**Snippet:**
```lua
function GetMessage_ItemLabelWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_ItemLevelByName.lua.lua
**Functions:**
- GetMessage_ItemLevelUis
**Snippet:**
```lua
function GetMessage_ItemLevelUis(ui)
  local uis = {}
  
  uis.UseTxt = ui:GetChild("UseTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_ItemMaxBtnByName.lua.lua
**Functions:**
- GetMessage_ItemMaxBtnUis
**Snippet:**
```lua
function GetMessage_ItemMaxBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_ItemMinBtnByName.lua.lua
**Functions:**
- GetMessage_ItemMinBtnUis
**Snippet:**
```lua
function GetMessage_ItemMinBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_ItemNumberByName.lua.lua
**Functions:**
- GetMessage_ItemNumberUis
**Snippet:**
```lua
function GetMessage_ItemNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_ItemNumberStripByName.lua.lua
**Functions:**
- GetMessage_ItemNumberStripUis
**Snippet:**
```lua
function GetMessage_ItemNumberStripUis(ui)
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

## MP/Message_ItemNumberStripRegionByName.lua.lua
**Functions:**
- GetMessage_ItemNumberStripRegionUis
**Snippet:**
```lua
function GetMessage_ItemNumberStripRegionUis(ui)
  local uis = {}
  
  uis.Price1Txt = ui:GetChild("Price1Txt")
  uis.PriceTxt = ui:GetChild("PriceTxt")
  uis.PriceLoader = ui:GetChild("PriceLoader")
  uis.root = ui
  return uis
end
```

---

## MP/Message_ItemNumberWordByName.lua.lua
**Functions:**
- GetMessage_ItemNumberWordUis
**Snippet:**
```lua
function GetMessage_ItemNumberWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_ItemReduceBtnByName.lua.lua
**Functions:**
- GetMessage_ItemReduceBtnUis
**Snippet:**
```lua
function GetMessage_ItemReduceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_ItemTimeByName.lua.lua
**Functions:**
- GetMessage_ItemTimeUis
**Snippet:**
```lua
function GetMessage_ItemTimeUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_ItemTipsByName.lua.lua
**Functions:**
- GetMessage_ItemTipsUis
**Requires:**
- Message_MainModularByName
- Message_DetailsModularByName
- Message_NumberModularByName
- Message_CardChangeModularByName
- Message_CardDetailsModularByName
- Message_ClothesChangeModularByName
- Message_ClothesDetailsModularByName
- Message_BreachGiftModularByName
- Message_PassportModularByName
**Snippet:**
```lua
require("Message_MainModularByName")
require("Message_DetailsModularByName")
require("Message_NumberModularByName")
require("Message_CardChangeModularByName")
require("Message_CardDetailsModularByName")
require("Message_ClothesChangeModularByName")
require("Message_ClothesDetailsModularByName")
require("Message_BreachGiftModularByName")
require("Message_PassportModularByName")

```

---

## MP/Message_ItemTipsWindowByName.lua.lua
**Functions:**
- GetMessage_ItemTipsWindowUis
**Requires:**
- CommonResource_PopupBgByName
- Message_ItemTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Message_ItemTipsByName")

function GetMessage_ItemTipsWindowUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Main = GetMessage_ItemTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
```

---

## MP/Message_LackWordByName.lua.lua
**Functions:**
- GetMessage_LackWordUis
**Snippet:**
```lua
function GetMessage_LackWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_LookBtnByName.lua.lua
**Functions:**
- GetMessage_LookBtnUis
**Snippet:**
```lua
function GetMessage_LookBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/Message_MainItemWordByName.lua.lua
**Functions:**
- GetMessage_MainItemWordUis
**Snippet:**
```lua
function GetMessage_MainItemWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.UseTxt = ui:GetChild("UseTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_MainModularByName.lua.lua
**Functions:**
- GetMessage_MainModularUis
**Requires:**
- Message_WayByName
**Snippet:**
```lua
require("Message_WayByName")

function GetMessage_MainModularUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.InfoList = ui:GetChild("InfoList")
  uis.WordList = ui:GetChild("WordList")
  uis.Way = GetMessage_WayUis(ui:GetChild("Way"))
```

---

## MP/Message_MainOpalExchange1ByName.lua.lua
**Functions:**
- GetMessage_MainOpalExchange1Uis
**Requires:**
- Message_OpalNumberByName
- Message_OpalNumberStripByName
**Snippet:**
```lua
require("Message_OpalNumberByName")
require("Message_OpalNumberStripByName")

function GetMessage_MainOpalExchange1Uis(ui)
  local uis = {}
  uis.Pic1Loader = ui:GetChild("Pic1Loader")
  uis.Pic2Loader = ui:GetChild("Pic2Loader")
  uis.Number1 = GetMessage_OpalNumberUis(ui:GetChild("Number1"))
  uis.Number2 = GetMessage_OpalNumberUis(ui:GetChild("Number2"))
  uis.WordTxt = ui:GetChild("WordTxt")
```

---

## MP/Message_MainOpalExchange2ByName.lua.lua
**Functions:**
- GetMessage_MainOpalExchange2Uis
**Requires:**
- CommonResource_PopupBgByName
- CommonResource_Popup_OpalByName
- Message_MainOpalExchange1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("CommonResource_Popup_OpalByName")
require("Message_MainOpalExchange1ByName")

function GetMessage_MainOpalExchange2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Popup_Opal = GetCommonResource_Popup_OpalUis(ui:GetChild("Popup_Opal"))
  uis.MainOpalExchange1 = GetMessage_MainOpalExchange1Uis(ui:GetChild("MainOpalExchange1"))
```

---

## MP/Message_MainOpalExchangeWindowByName.lua.lua
**Functions:**
- GetMessage_MainOpalExchangeWindowUis
**Requires:**
- Message_MainOpalExchange2ByName
**Snippet:**
```lua
require("Message_MainOpalExchange2ByName")

function GetMessage_MainOpalExchangeWindowUis(ui)
  local uis = {}
  uis.Main = GetMessage_MainOpalExchange2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_MapContentByName.lua.lua
**Functions:**
- GetMessage_MapContentUis
**Snippet:**
```lua
function GetMessage_MapContentUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.InfoList = ui:GetChild("InfoList")
  uis.root = ui
  return uis
end
```

---

## MP/Message_MapInfo1ByName.lua.lua
**Functions:**
- GetMessage_MapInfo1Uis
**Snippet:**
```lua
function GetMessage_MapInfo1Uis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_MapInfoByName.lua.lua
**Functions:**
- GetMessage_MapInfoUis
**Snippet:**
```lua
function GetMessage_MapInfoUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EfectTxt = ui:GetChild("EfectTxt")
  uis.Info1List = ui:GetChild("Info1List")
  uis.NoBuffTxt = ui:GetChild("NoBuffTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## MP/Message_MapTipsByName.lua.lua
**Functions:**
- GetMessage_MapTipsUis
**Requires:**
- CommonResource_PopupBgByName
- Message_MapContentByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Message_MapContentByName")

function GetMessage_MapTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.MapContent = GetMessage_MapContentUis(ui:GetChild("MapContent"))
  uis.root = ui
  return uis
```

---

## MP/Message_MapTipsWindowByName.lua.lua
**Functions:**
- GetMessage_MapTipsWindowUis
**Requires:**
- Message_MapTipsByName
**Snippet:**
```lua
require("Message_MapTipsByName")

function GetMessage_MapTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetMessage_MapTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_MaxBtnByName.lua.lua
**Functions:**
- GetMessage_MaxBtnUis
**Snippet:**
```lua
function GetMessage_MaxBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_MinBtnByName.lua.lua
**Functions:**
- GetMessage_MinBtnUis
**Snippet:**
```lua
function GetMessage_MinBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_MonthByName.lua.lua
**Functions:**
- GetMessage_MonthUis
**Requires:**
- Message_MonthTimeByName
**Snippet:**
```lua
require("Message_MonthTimeByName")

function GetMessage_MonthUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.PicHolder = ui:GetChild("PicHolder")
  uis.MonthTime = GetMessage_MonthTimeUis(ui:GetChild("MonthTime"))
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.root = ui
  return uis
```

---

## MP/Message_MonthGetBtnByName.lua.lua
**Functions:**
- GetMessage_MonthGetBtnUis
**Snippet:**
```lua
function GetMessage_MonthGetBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/Message_MonthGetByName.lua.lua
**Functions:**
- GetMessage_MonthGetUis
**Requires:**
- CommonResource_PopupBgByName
- Message_MonthByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Message_MonthByName")

function GetMessage_MonthGetUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Month = GetMessage_MonthUis(ui:GetChild("Month"))
  uis.root = ui
  return uis
```

---

## MP/Message_MonthGetWindowByName.lua.lua
**Functions:**
- GetMessage_MonthGetWindowUis
**Requires:**
- Message_MonthGetByName
**Snippet:**
```lua
require("Message_MonthGetByName")

function GetMessage_MonthGetWindowUis(ui)
  local uis = {}
  uis.Main = GetMessage_MonthGetUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_MonthTimeByName.lua.lua
**Functions:**
- GetMessage_MonthTimeUis
**Snippet:**
```lua
function GetMessage_MonthTimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_NumberModularByName.lua.lua
**Functions:**
- GetMessage_NumberModularUis
**Requires:**
- Message_ItemNumberStripRegionByName
- Message_ItemNumberStripByName
**Snippet:**
```lua
require("Message_ItemNumberStripRegionByName")
require("Message_ItemNumberStripByName")

function GetMessage_NumberModularUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.ItemNumberStrip = GetMessage_ItemNumberStripRegionUis(ui:GetChild("ItemNumberStrip"))
  uis.NumberStrip = GetMessage_ItemNumberStripUis(ui:GetChild("NumberStrip"))
```

---

## MP/Message_NumberStrip1ByName.lua.lua
**Functions:**
- GetMessage_NumberStrip1Uis
**Snippet:**
```lua
function GetMessage_NumberStrip1Uis(ui)
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

## MP/Message_NumberStripByName.lua.lua
**Functions:**
- GetMessage_NumberStripUis
**Snippet:**
```lua
function GetMessage_NumberStripUis(ui)
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

## MP/Message_OpalAddBtnByName.lua.lua
**Functions:**
- GetMessage_OpalAddBtnUis
**Snippet:**
```lua
function GetMessage_OpalAddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_OpalExchange1ByName.lua.lua
**Functions:**
- GetMessage_OpalExchange1Uis
**Snippet:**
```lua
function GetMessage_OpalExchange1Uis(ui)
  local uis = {}
  
  uis.Pic1Loader = ui:GetChild("Pic1Loader")
  uis.Pic2Loader = ui:GetChild("Pic2Loader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_OpalExchange2ByName.lua.lua
**Functions:**
- GetMessage_OpalExchange2Uis
**Requires:**
- CommonResource_PopupBgByName
- CommonResource_Popup_OpalByName
- Message_OpalExchange1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("CommonResource_Popup_OpalByName")
require("Message_OpalExchange1ByName")

function GetMessage_OpalExchange2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Popup_Opal = GetCommonResource_Popup_OpalUis(ui:GetChild("Popup_Opal"))
  uis.Rename1 = GetMessage_OpalExchange1Uis(ui:GetChild("Rename1"))
```

---

## MP/Message_OpalExchangeWindowByName.lua.lua
**Functions:**
- GetMessage_OpalExchangeWindowUis
**Requires:**
- Message_OpalExchange2ByName
**Snippet:**
```lua
require("Message_OpalExchange2ByName")

function GetMessage_OpalExchangeWindowUis(ui)
  local uis = {}
  uis.Main = GetMessage_OpalExchange2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_OpalMaxBtnByName.lua.lua
**Functions:**
- GetMessage_OpalMaxBtnUis
**Snippet:**
```lua
function GetMessage_OpalMaxBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_OpalMinBtnByName.lua.lua
**Functions:**
- GetMessage_OpalMinBtnUis
**Snippet:**
```lua
function GetMessage_OpalMinBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_OpalNumberByName.lua.lua
**Functions:**
- GetMessage_OpalNumberUis
**Snippet:**
```lua
function GetMessage_OpalNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_OpalNumberStripByName.lua.lua
**Functions:**
- GetMessage_OpalNumberStripUis
**Snippet:**
```lua
function GetMessage_OpalNumberStripUis(ui)
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

## MP/Message_OpalReduceBtnByName.lua.lua
**Functions:**
- GetMessage_OpalReduceBtnUis
**Snippet:**
```lua
function GetMessage_OpalReduceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_PageByName.lua.lua
**Functions:**
- GetMessage_PageUis
**Snippet:**
```lua
function GetMessage_PageUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_PassportChoiceBtnByName.lua.lua
**Functions:**
- GetMessage_PassportChoiceBtnUis
**Snippet:**
```lua
function GetMessage_PassportChoiceBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
```

---

## MP/Message_PassportModularByName.lua.lua
**Functions:**
- GetMessage_PassportModularUis
**Snippet:**
```lua
function GetMessage_PassportModularUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.Popup_S_Black_Btn = ui:GetChild("Popup_S_Black_Btn")
  uis.Popup_S_Green_Btn = ui:GetChild("Popup_S_Green_Btn")
  uis.root = ui
  return uis
```

---

## MP/Message_Popup_BByName.lua.lua
**Functions:**
- GetMessage_Popup_BUis
**Snippet:**
```lua
function GetMessage_Popup_BUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## MP/Message_ReasonBtnByName.lua.lua
**Functions:**
- GetMessage_ReasonBtnUis
**Snippet:**
```lua
function GetMessage_ReasonBtnUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/Message_ReasonSpendByName.lua.lua
**Functions:**
- GetMessage_ReasonSpendUis
**Snippet:**
```lua
function GetMessage_ReasonSpendUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_ReduceBtnByName.lua.lua
**Functions:**
- GetMessage_ReduceBtnUis
**Snippet:**
```lua
function GetMessage_ReduceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_Rename1ByName.lua.lua
**Functions:**
- GetMessage_Rename1Uis
**Requires:**
- Message_SpendByName
**Snippet:**
```lua
require("Message_SpendByName")

function GetMessage_Rename1Uis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Spend = GetMessage_SpendUis(ui:GetChild("Spend"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## MP/Message_Rename2ByName.lua.lua
**Functions:**
- GetMessage_Rename2Uis
**Requires:**
- CommonResource_PopupBgByName
- CommonResource_Popup_BByName
- Message_Rename1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("CommonResource_Popup_BByName")
require("Message_Rename1ByName")

function GetMessage_Rename2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Popup_B = GetCommonResource_Popup_BUis(ui:GetChild("Popup_B"))
  uis.Rename1 = GetMessage_Rename1Uis(ui:GetChild("Rename1"))
```

---

## MP/Message_RenameWindowByName.lua.lua
**Functions:**
- GetMessage_RenameWindowUis
**Requires:**
- Message_Rename2ByName
**Snippet:**
```lua
require("Message_Rename2ByName")

function GetMessage_RenameWindowUis(ui)
  local uis = {}
  uis.Main = GetMessage_Rename2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_RewardShow1ByName.lua.lua
**Functions:**
- GetMessage_RewardShow1Uis
**Snippet:**
```lua
function GetMessage_RewardShow1Uis(ui)
  local uis = {}
  
  uis.ItemList = ui:GetChild("ItemList")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_RewardShow2ByName.lua.lua
**Functions:**
- GetMessage_RewardShow2Uis
**Requires:**
- CommonResource_PopupBgByName
- CommonResource_Popup_BByName
- Message_RewardShow1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("CommonResource_Popup_BByName")
require("Message_RewardShow1ByName")

function GetMessage_RewardShow2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Popup_B = GetCommonResource_Popup_BUis(ui:GetChild("Popup_B"))
  uis.RewardShow1 = GetMessage_RewardShow1Uis(ui:GetChild("RewardShow1"))
```

---

## MP/Message_RewardShowWindowByName.lua.lua
**Functions:**
- GetMessage_RewardShowWindowUis
**Requires:**
- Message_RewardShow2ByName
**Snippet:**
```lua
require("Message_RewardShow2ByName")

function GetMessage_RewardShowWindowUis(ui)
  local uis = {}
  uis.Main = GetMessage_RewardShow2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_SkillLeaderLcokByName.lua.lua
**Functions:**
- GetMessage_SkillLeaderLcokUis
**Snippet:**
```lua
function GetMessage_SkillLeaderLcokUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_SkillTips1ByName.lua.lua
**Functions:**
- GetMessage_SkillTips1Uis
**Requires:**
- CommonResource_SkillByName
- Message_SkillTypeByName
- Message_SkillTipsInfoByName
**Snippet:**
```lua
require("CommonResource_SkillByName")
require("Message_SkillTypeByName")
require("Message_SkillTipsInfoByName")

function GetMessage_SkillTips1Uis(ui)
  local uis = {}
  uis.Sikll = GetCommonResource_SkillUis(ui:GetChild("Sikll"))
  uis.SkillType = GetMessage_SkillTypeUis(ui:GetChild("SkillType"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
```

---

## MP/Message_SkillTipsByName.lua.lua
**Functions:**
- GetMessage_SkillTipsUis
**Requires:**
- CommonResource_PopupBgByName
- Message_SkillTips1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Message_SkillTips1ByName")

function GetMessage_SkillTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.SkillTips1 = GetMessage_SkillTips1Uis(ui:GetChild("SkillTips1"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.root = ui
  return uis
```

---

## MP/Message_SkillTipsInfoByName.lua.lua
**Functions:**
- GetMessage_SkillTipsInfoUis
**Snippet:**
```lua
function GetMessage_SkillTipsInfoUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_SkillTipsUnitByName.lua.lua
**Functions:**
- GetMessage_SkillTipsUnitUis
**Snippet:**
```lua
function GetMessage_SkillTipsUnitUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_SkillTipsWindowByName.lua.lua
**Functions:**
- GetMessage_SkillTipsWindowUis
**Requires:**
- Message_SkillTipsByName
**Snippet:**
```lua
require("Message_SkillTipsByName")

function GetMessage_SkillTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetMessage_SkillTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_SkillTypeByName.lua.lua
**Functions:**
- GetMessage_SkillTypeUis
**Snippet:**
```lua
function GetMessage_SkillTypeUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_SpendByName.lua.lua
**Functions:**
- GetMessage_SpendUis
**Snippet:**
```lua
function GetMessage_SpendUis(ui)
  local uis = {}
  
  uis.IconLoader = ui:GetChild("IconLoader")
  uis.SpendTxt = ui:GetChild("SpendTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_StarOneSkill1ByName.lua.lua
**Functions:**
- GetMessage_StarOneSkill1Uis
**Requires:**
- Message_StarOneSkillLockByName
**Snippet:**
```lua
require("Message_StarOneSkillLockByName")

function GetMessage_StarOneSkill1Uis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SkillLock = GetMessage_StarOneSkillLockUis(ui:GetChild("SkillLock"))
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## MP/Message_StarOneSkill2ByName.lua.lua
**Functions:**
- GetMessage_StarOneSkill2Uis
**Requires:**
- CommonResource_PopupBgByName
- Message_StarOneSkill1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Message_StarOneSkill1ByName")

function GetMessage_StarOneSkill2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.BadgeOneSkill1 = GetMessage_StarOneSkill1Uis(ui:GetChild("BadgeOneSkill1"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.root = ui
  return uis
```

---

## MP/Message_StarOneSkillLockByName.lua.lua
**Functions:**
- GetMessage_StarOneSkillLockUis
**Snippet:**
```lua
function GetMessage_StarOneSkillLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_StarOneSkillWindowByName.lua.lua
**Functions:**
- GetMessage_StarOneSkillWindowUis
**Requires:**
- Message_StarOneSkill2ByName
**Snippet:**
```lua
require("Message_StarOneSkill2ByName")

function GetMessage_StarOneSkillWindowUis(ui)
  local uis = {}
  uis.Main = GetMessage_StarOneSkill2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_StarSkill1ByName.lua.lua
**Functions:**
- GetMessage_StarSkill1Uis
**Requires:**
- Message_StarSkillLockByName
**Snippet:**
```lua
require("Message_StarSkillLockByName")

function GetMessage_StarSkill1Uis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.Lock = GetMessage_StarSkillLockUis(ui:GetChild("Lock"))
  uis.c2Ctr = ui:GetController("c2")
  uis.c1Ctr = ui:GetController("c1")
```

---

## MP/Message_StarSkill2ByName.lua.lua
**Functions:**
- GetMessage_StarSkill2Uis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetMessage_StarSkill2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.SkillList = ui:GetChild("SkillList")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.root = ui
  return uis
```

---

## MP/Message_StarSkillLockByName.lua.lua
**Functions:**
- GetMessage_StarSkillLockUis
**Snippet:**
```lua
function GetMessage_StarSkillLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_StarSkillWindowByName.lua.lua
**Functions:**
- GetMessage_StarSkillWindowUis
**Requires:**
- Message_StarSkill2ByName
**Snippet:**
```lua
require("Message_StarSkill2ByName")

function GetMessage_StarSkillWindowUis(ui)
  local uis = {}
  uis.Main = GetMessage_StarSkill2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_StarTipsWordByName.lua.lua
**Functions:**
- GetMessage_StarTipsWordUis
**Snippet:**
```lua
function GetMessage_StarTipsWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_Sweep10BtnByName.lua.lua
**Functions:**
- GetMessage_Sweep10BtnUis
**Snippet:**
```lua
function GetMessage_Sweep10BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/Message_Sweep10RegionByName.lua.lua
**Functions:**
- GetMessage_Sweep10RegionUis
**Requires:**
- Message_ReasonSpendByName
**Snippet:**
```lua
require("Message_ReasonSpendByName")

function GetMessage_Sweep10RegionUis(ui)
  local uis = {}
  uis.ReasonSpend = GetMessage_ReasonSpendUis(ui:GetChild("ReasonSpend"))
  uis.SweepBtn = ui:GetChild("SweepBtn")
  uis.root = ui
  return uis
end
```

---

## MP/Message_Sweep1BtnByName.lua.lua
**Functions:**
- GetMessage_Sweep1BtnUis
**Snippet:**
```lua
function GetMessage_Sweep1BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/Message_Sweep1RegionByName.lua.lua
**Functions:**
- GetMessage_Sweep1RegionUis
**Requires:**
- Message_ReasonSpendByName
**Snippet:**
```lua
require("Message_ReasonSpendByName")

function GetMessage_Sweep1RegionUis(ui)
  local uis = {}
  uis.ReasonSpend = GetMessage_ReasonSpendUis(ui:GetChild("ReasonSpend"))
  uis.SweepBtn = ui:GetChild("SweepBtn")
  uis.root = ui
  return uis
end
```

---

## MP/Message_SweepByName.lua.lua
**Functions:**
- GetMessage_SweepUis
**Requires:**
- CommonResource_PopupBgByName
- Message_SweepTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Message_SweepTipsByName")

function GetMessage_SweepUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.SweepTips = GetMessage_SweepTipsUis(ui:GetChild("SweepTips"))
  uis.root = ui
  return uis
```

---

## MP/Message_SweepCardBgByName.lua.lua
**Functions:**
- GetMessage_SweepCardBgUis
**Snippet:**
```lua
function GetMessage_SweepCardBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## MP/Message_SweepCardByName.lua.lua
**Functions:**
- GetMessage_SweepCardUis
**Requires:**
- Message_SweepCardBgByName
- Message_SweepCardItemByName
**Snippet:**
```lua
require("Message_SweepCardBgByName")
require("Message_SweepCardItemByName")

function GetMessage_SweepCardUis(ui)
  local uis = {}
  uis.SweepCardBg = GetMessage_SweepCardBgUis(ui:GetChild("SweepCardBg"))
  uis.SweepCardItem = GetMessage_SweepCardItemUis(ui:GetChild("SweepCardItem"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_SweepCardItemByName.lua.lua
**Functions:**
- GetMessage_SweepCardItemUis
**Requires:**
- CommonResource_ItemFrameByName
**Snippet:**
```lua
require("CommonResource_ItemFrameByName")

function GetMessage_SweepCardItemUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Item = GetCommonResource_ItemFrameUis(ui:GetChild("Item"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_SweepDecorationByName.lua.lua
**Functions:**
- GetMessage_SweepDecorationUis
**Snippet:**
```lua
function GetMessage_SweepDecorationUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## MP/Message_SweepFallByName.lua.lua
**Functions:**
- GetMessage_SweepFallUis
**Snippet:**
```lua
function GetMessage_SweepFallUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## MP/Message_SweepResultAniByName.lua.lua
**Functions:**
- GetMessage_SweepResultAniUis
**Requires:**
- Message_SweepResultByName
**Snippet:**
```lua
require("Message_SweepResultByName")

function GetMessage_SweepResultAniUis(ui)
  local uis = {}
  uis.SweepResult = GetMessage_SweepResultUis(ui:GetChild("SweepResult"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_SweepResultByName.lua.lua
**Functions:**
- GetMessage_SweepResultUis
**Snippet:**
```lua
function GetMessage_SweepResultUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## MP/Message_SweepResultListByName.lua.lua
**Functions:**
- GetMessage_SweepResultListUis
**Snippet:**
```lua
function GetMessage_SweepResultListUis(ui)
  local uis = {}
  
  uis.ResultList = ui:GetChild("ResultList")
  uis.root = ui
  return uis
end
```

---

## MP/Message_SweepTipsByName.lua.lua
**Functions:**
- GetMessage_SweepTipsUis
**Requires:**
- Message_Sweep10RegionByName
- Message_Sweep1RegionByName
- Message_SweepResultListByName
- Message_SweepWordByName
- Message_SweepCardByName
- Message_SweepFallByName
- Message_SweepDecorationByName
**Snippet:**
```lua
require("Message_Sweep10RegionByName")
require("Message_Sweep1RegionByName")
require("Message_SweepResultListByName")
require("Message_SweepWordByName")
require("Message_SweepCardByName")
require("Message_SweepFallByName")
require("Message_SweepDecorationByName")

function GetMessage_SweepTipsUis(ui)
  local uis = {}
```

---

## MP/Message_SweepWindowByName.lua.lua
**Functions:**
- GetMessage_SweepWindowUis
**Requires:**
- Message_SweepByName
**Snippet:**
```lua
require("Message_SweepByName")

function GetMessage_SweepWindowUis(ui)
  local uis = {}
  uis.Main = GetMessage_SweepUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_SweepWordByName.lua.lua
**Functions:**
- GetMessage_SweepWordUis
**Snippet:**
```lua
function GetMessage_SweepWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_TokensBuyByName.lua.lua
**Functions:**
- GetMessage_TokensBuyUis
**Requires:**
- Message_TokensBuyNumberByName
- Message_LackWordByName
**Snippet:**
```lua
require("Message_TokensBuyNumberByName")
require("Message_LackWordByName")

function GetMessage_TokensBuyUis(ui)
  local uis = {}
  uis.AllPrice = GetMessage_TokensBuyNumberUis(ui:GetChild("AllPrice"))
  uis.SureBtn = ui:GetChild("SureBtn")
  uis.LackWord = GetMessage_LackWordUis(ui:GetChild("LackWord"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## MP/Message_TokensBuyNumberByName.lua.lua
**Functions:**
- GetMessage_TokensBuyNumberUis
**Snippet:**
```lua
function GetMessage_TokensBuyNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_TokensCardByName.lua.lua
**Functions:**
- GetMessage_TokensCardUis
**Requires:**
- Message_DiscountByName
- Message_TokensPrice2_1ByName
- Message_TokensPrice2_2ByName
- Message_BuyItemContentByName
- Message_NumberStrip1ByName
- Message_TokensBuyByName
**Snippet:**
```lua
require("Message_DiscountByName")
require("Message_TokensPrice2_1ByName")
require("Message_TokensPrice2_2ByName")
require("Message_BuyItemContentByName")
require("Message_NumberStrip1ByName")
require("Message_TokensBuyByName")

function GetMessage_TokensCardUis(ui)
  local uis = {}
  uis.Discount = GetMessage_DiscountUis(ui:GetChild("Discount"))
```

---

## MP/Message_TokensDemandRegionByName.lua.lua
**Functions:**
- GetMessage_TokensDemandRegionUis
**Requires:**
- Message_CardBreachByName
- Message_CardSkillByName
- Message_BadgeStarByName
- Message_DemandItemByName
**Snippet:**
```lua
require("Message_CardBreachByName")
require("Message_CardSkillByName")
require("Message_BadgeStarByName")
require("Message_DemandItemByName")

function GetMessage_TokensDemandRegionUis(ui)
  local uis = {}
  uis.CardBreach = GetMessage_CardBreachUis(ui:GetChild("CardBreach"))
  uis.CardSkill = GetMessage_CardSkillUis(ui:GetChild("CardSkill"))
  uis.BadgeStar = GetMessage_BadgeStarUis(ui:GetChild("BadgeStar"))
```

---

## MP/Message_TokensHaveNumberByName.lua.lua
**Functions:**
- GetMessage_TokensHaveNumberUis
**Snippet:**
```lua
function GetMessage_TokensHaveNumberUis(ui)
  local uis = {}
  
  uis.HaveNumberTxt = ui:GetChild("HaveNumberTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_TokensItemPicByName.lua.lua
**Functions:**
- GetMessage_TokensItemPicUis
**Requires:**
- Message_TokensPic1ByName
- Message_TokensPic2ByName
**Snippet:**
```lua
require("Message_TokensPic1ByName")
require("Message_TokensPic2ByName")

function GetMessage_TokensItemPicUis(ui)
  local uis = {}
  uis.Pic1 = GetMessage_TokensPic1Uis(ui:GetChild("Pic1"))
  uis.Pic2 = GetMessage_TokensPic2Uis(ui:GetChild("Pic2"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## MP/Message_TokensPic1ByName.lua.lua
**Functions:**
- GetMessage_TokensPic1Uis
**Snippet:**
```lua
function GetMessage_TokensPic1Uis(ui)
  local uis = {}
  
  uis.IconLoader = ui:GetChild("IconLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_TokensPic2ByName.lua.lua
**Functions:**
- GetMessage_TokensPic2Uis
**Snippet:**
```lua
function GetMessage_TokensPic2Uis(ui)
  local uis = {}
  
  uis.IconLoader = ui:GetChild("IconLoader")
  uis.root = ui
  return uis
end
```

---

## MP/Message_TokensPrice1ByName.lua.lua
**Functions:**
- GetMessage_TokensPrice1Uis
**Requires:**
- Message_TokensPrice1_1ByName
- Message_TokensPrice1_2ByName
**Snippet:**
```lua
require("Message_TokensPrice1_1ByName")
require("Message_TokensPrice1_2ByName")

function GetMessage_TokensPrice1Uis(ui)
  local uis = {}
  uis.Price1 = GetMessage_TokensPrice1_1Uis(ui:GetChild("Price1"))
  uis.Price2 = GetMessage_TokensPrice1_2Uis(ui:GetChild("Price2"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## MP/Message_TokensPrice1_1ByName.lua.lua
**Functions:**
- GetMessage_TokensPrice1_1Uis
**Snippet:**
```lua
function GetMessage_TokensPrice1_1Uis(ui)
  local uis = {}
  
  uis.Price1Txt = ui:GetChild("Price1Txt")
  uis.PriceLoader = ui:GetChild("PriceLoader")
  uis.PriceTxt = ui:GetChild("PriceTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_TokensPrice1_2ByName.lua.lua
**Functions:**
- GetMessage_TokensPrice1_2Uis
**Snippet:**
```lua
function GetMessage_TokensPrice1_2Uis(ui)
  local uis = {}
  
  uis.Price1Txt = ui:GetChild("Price1Txt")
  uis.PriceLoader = ui:GetChild("PriceLoader")
  uis.PriceTxt = ui:GetChild("PriceTxt")
  uis.OriginalPriceTxt = ui:GetChild("OriginalPriceTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_TokensPrice2_1ByName.lua.lua
**Functions:**
- GetMessage_TokensPrice2_1Uis
**Snippet:**
```lua
function GetMessage_TokensPrice2_1Uis(ui)
  local uis = {}
  
  uis.Price1Txt = ui:GetChild("Price1Txt")
  uis.PriceLoader = ui:GetChild("PriceLoader")
  uis.PriceTxt = ui:GetChild("PriceTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_TokensPrice2_2ByName.lua.lua
**Functions:**
- GetMessage_TokensPrice2_2Uis
**Snippet:**
```lua
function GetMessage_TokensPrice2_2Uis(ui)
  local uis = {}
  
  uis.Price1Txt = ui:GetChild("Price1Txt")
  uis.PriceLoader = ui:GetChild("PriceLoader")
  uis.PriceTxt = ui:GetChild("PriceTxt")
  uis.OriginalPriceTxt = ui:GetChild("OriginalPriceTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_TokensTipsAniByName.lua.lua
**Functions:**
- GetMessage_TokensTipsAniUis
**Requires:**
- CommonResource_PopupBgByName
- Message_TokensTipsByName
- Message_AssetsTipsGroupByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Message_TokensTipsByName")
require("Message_AssetsTipsGroupByName")

function GetMessage_TokensTipsAniUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.TokensTips = GetMessage_TokensTipsUis(ui:GetChild("TokensTips"))
  uis.AssetsTipsGroup = GetMessage_AssetsTipsGroupUis(ui:GetChild("AssetsTipsGroup"))
```

---

## MP/Message_TokensTipsByName.lua.lua
**Functions:**
- GetMessage_TokensTipsUis
**Requires:**
- Message_TokensTipsMainByName
- Message_TokensCardByName
**Snippet:**
```lua
require("Message_TokensTipsMainByName")
require("Message_TokensCardByName")

function GetMessage_TokensTipsUis(ui)
  local uis = {}
  uis.TokensTipsMain = GetMessage_TokensTipsMainUis(ui:GetChild("TokensTipsMain"))
  uis.TokensCard = GetMessage_TokensCardUis(ui:GetChild("TokensCard"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## MP/Message_TokensTipsMainByName.lua.lua
**Functions:**
- GetMessage_TokensTipsMainUis
**Requires:**
- Message_TokensItemPicByName
- Message_ItemNumberByName
- Message_DiscountByName
- Message_TokensPrice1ByName
- Message_TokensHaveNumberByName
- Message_NumberStripByName
- Message_TokensBuyByName
**Snippet:**
```lua
require("Message_TokensItemPicByName")
require("Message_ItemNumberByName")
require("Message_DiscountByName")
require("Message_TokensPrice1ByName")
require("Message_TokensHaveNumberByName")
require("Message_NumberStripByName")
require("Message_TokensBuyByName")

function GetMessage_TokensTipsMainUis(ui)
  local uis = {}
```

---

## MP/Message_TokensTipsWindowByName.lua.lua
**Functions:**
- GetMessage_TokensTipsWindowUis
**Requires:**
- Message_TokensTipsAniByName
**Snippet:**
```lua
require("Message_TokensTipsAniByName")

function GetMessage_TokensTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetMessage_TokensTipsAniUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Message_TokensTipsWordByName.lua.lua
**Functions:**
- GetMessage_TokensTipsWordUis
**Snippet:**
```lua
function GetMessage_TokensTipsWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Message_TokensUseMarkByName.lua.lua
**Functions:**
- GetMessage_TokensUseMarkUis
**Snippet:**
```lua
function GetMessage_TokensUseMarkUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Message_WayByName.lua.lua
**Functions:**
- GetMessage_WayUis
**Snippet:**
```lua
function GetMessage_WayUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.GetStripList = ui:GetChild("GetStripList")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## MP/Message_White_S_BtnByName.lua.lua
**Functions:**
- GetMessage_White_S_BtnUis
**Snippet:**
```lua
function GetMessage_White_S_BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/Message_WordContentByName.lua.lua
**Functions:**
- GetMessage_WordContentUis
**Snippet:**
```lua
function GetMessage_WordContentUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/MiniGameBattleAction.lua.lua
**Functions:**
- MiniGameBattleAction.DealStart
- MiniGameBattleAction.DealStand
- MiniGameBattleAction.DealMove
- MiniGameBattleAction.DealAttack
- MiniGameBattleAction.DealAttackOver
- MiniGameBattleAction.ClearAttackInfo
- MiniGameBattleAction.DealDying
- MiniGameBattleAction.DealDead
- MiniGameBattleAction.InitBeatBackUnitData
- MiniGameBattleAction.DealBeatBack
- MiniGameBattleAction.ForceChangeState
- MiniGameBattleAction.DealStopMove
- MiniGameBattleAction.DealStopAttack
- MiniGameBattleAction.DealHurt
- MiniGameBattleAction.DealTriggerSkill
- MiniGameBattleAction.DealTriggerSkillCondition
- MiniGameBattleAction.DealUnitSkill
**Snippet:**
```lua
MiniGameBattleAction = {}

function MiniGameBattleAction.DealStart(battleUnit)
  battleUnit:SetState(BATTLE_STATE_ENUM.STAND)
end

function MiniGameBattleAction.DealStand(unit)
  if unit.isTrick == true then
    return
  end
```

---

## MP/MiniGameBattleActionDisplay.lua.lua
**Functions:**
- MiniGameBattleActionDisplay.PlayStart
- MiniGameBattleActionDisplay.PlayStand
- MiniGameBattleActionDisplay.PlayMove
- MiniGameBattleActionDisplay.PlayAttack
- MiniGameBattleActionDisplay.PlayDead
- MiniGameBattleActionDisplay.PlayStun
- MiniGameBattleActionDisplay.PlayBeatBack
- MiniGameBattleActionDisplay.PlayHurt
- MiniGameBattleActionDisplay.PlayHitEffect
- MiniGameBattleActionDisplay.PlayMonsterAppearEffect
- MiniGameBattleActionDisplay.PlayEffect
- MiniGameBattleActionDisplay.PlaySound
**Snippet:**
```lua
MiniGameBattleActionDisplay = {}

function MiniGameBattleActionDisplay.PlayStart(unit)
  unit:ChangeAnimation(MINI_GAME_UNIT_ANIMATION.IDLE)
end

function MiniGameBattleActionDisplay.PlayStand(unit)
  unit:ChangeAnimation(MINI_GAME_UNIT_ANIMATION.IDLE)
end

```

---

## MP/MiniGameBattleBackground.lua.lua
**Functions:**
- MiniGameBattleBackground.Init
- MiniGameBattleBackground.Clear
**Requires:**
- SortingHelper
**Snippet:**
```lua
MiniGameBattleBackground = {
  model = nil,
  modelUp = nil,
  sound = nil
}

function MiniGameBattleBackground.Init()
  local stageConfig = MiniGameBattleData.stageConfig
  local model = ResourceManager.Instantiate(stageConfig.background_path)
  SoundUtil.PlayMusic(stageConfig.sound_id)
```

---

## MP/MiniGameBattleBuff.lua.lua
**Functions:**
- MiniGameBattleBuff.InitLocalVar
- MiniGameBattleBuff.NewBuff
- buff:Init
- buff:Clear
- buff:SetDeduceTriggerUnitUid
- buff:AddTargetUid
- buff:IsAlreadyInTarget
- buff:ClearAlreadyInTarget
- buff:ContainEffectIdBeforeSettle
- buff:ContainEffectTagBeforeSettle
- buff:Settle
- buff:CanDeduce
- buff:Deduce
- buff:DealActiveForeverEffect
- buff:ContainEffectId
- buff:GetEffectTotalValue
- buff:GetAttributeValue
- buff:ContainAttributeId
- buff:Remove
- buff:TriggerUnitAttrChanged
- buff:NeedRemove
- buff:Update
- buff:CanSettle
- buff:SetState
- buff:UpdateDisplay
- buff:Destroy
**Snippet:**
```lua
MiniGameBattleBuff = {}

function MiniGameBattleBuff.InitLocalVar()
end

function MiniGameBattleBuff.NewBuff(buffId, from, to, settleNow, extraParams)
  local buff = {}
  
  function buff:Init()
    self:Clear()
```

---

## MP/MiniGameBattleBuffEffect.lua.lua
**Functions:**
- MiniGameBattleBuffEffect.NewEffect
- effect:Init
- effect:UpdateValue
- effect:Destroy
- MiniGameBattleBuffEffect.GetEffectValue
**Snippet:**
```lua
MiniGameBattleBuffEffect = {}
local tonumber = tonumber
local floor = math.floor
local ceil = math.ceil
local ATTR_ID = ProtoEnum.ATTR_ID

function MiniGameBattleBuffEffect.NewEffect(effectStr, belongBuffUid)
  local effect = {}
  
  function effect:Init()
```

---

## MP/MiniGameBattleBuffMgr.lua.lua
**Functions:**
- MiniGameBattleBuffMgr.InitLocalVar
- MiniGameBattleBuffMgr.Init
- MiniGameBattleBuffMgr.AddToBuffList
- MiniGameBattleBuffMgr.RemoveFromBuffList
- MiniGameBattleBuffMgr.ClearAllBuff
- MiniGameBattleBuffMgr.RegisterSettleListener
- MiniGameBattleBuffMgr.RegisterDeduceListener
- MiniGameBattleBuffMgr.RegisterRemoveListener
- MiniGameBattleBuffMgr.UnRegisterSettleListenerByUnitUid
- MiniGameBattleBuffMgr.UnRegisterSettleListener
- MiniGameBattleBuffMgr.UnRegisterDeduceListener
- MiniGameBattleBuffMgr.UnRegisterRemoveListener
- MiniGameBattleBuffMgr.RefreshRegisterDeduceListener
- MiniGameBattleBuffMgr.TriggerUnitListener
- MiniGameBattleBuffMgr.TriggerBulletListener
- MiniGameBattleBuffMgr.GetBuffGlobalIndex
- MiniGameBattleBuffMgr.AnalysisBuffList
- MiniGameBattleBuffMgr.GetBuffByUid
- MiniGameBattleBuffMgr.GetSavedBuffList
- MiniGameBattleBuffMgr.UpdateAllBuff
- MiniGameBattleBuffMgr.GetListenerSettleList
- MiniGameBattleBuffMgr.GetListenerDeduceList
- MiniGameBattleBuffMgr.GetContainedEffect
- MiniGameBattleBuffMgr.GetBulletContainedEffect
- MiniGameBattleBuffMgr.GetValueListByEffectId
- MiniGameBattleBuffMgr.GetValueById
- MiniGameBattleBuffMgr.GetSettledBuffByUnitAndId
**Snippet:**
```lua
MiniGameBattleBuffMgr = {}
local listenerSettleList = {}
local listenerDeduceList = {}
local listenerRemoveList = {}
local savedBuffList = {}
local sortBuffList = {}
local copySortBuffUidList = {}
local sortBuffListChanged
local buffGlobalIndex = 0

```

---

## MP/MiniGameBattleBullet.lua.lua
**Functions:**
- MiniGameBattleBullet.InitLocalVar
- MiniGameBattleBullet.NewBullet
- bullet:Init
- bullet:UpdateDirection
- bullet:SetHurtBuff
- bullet:CreateModel
- bullet:IsTargetHit
- bullet:Update
- bullet:SetVisible
- bullet:GetHurtMonsterList
- bullet:DealMove
- bullet:DealHurt
- bullet:UpdateDisplay
- bullet:AddBuff
- bullet:RemoveBuff
- bullet:UpdateCachedBuffEffect
- bullet:UpdateModelPosition
- bullet:UpdateSortingOrder
- bullet:Destroy
**Snippet:**
```lua
MiniGameBattleBullet = {}
local pairs = pairs

function MiniGameBattleBullet.InitLocalVar()
end

local BULLET_TYPE_ENUM = {NORMAL = 1, DIRECT_MOVE = 2}

function MiniGameBattleBullet.NewBullet(attackUnit, fromPos, toPos, bulletExtraParams)
  local bullet = {
```

---

## MP/MiniGameBattleChoose.lua.lua
**Functions:**
- MiniGameBattleChoose.InitLocalVar
- MiniGameBattleChoose.GetTargetUnitList
- MiniGameBattleChoose.GetSkillTargetUnitList
- MiniGameBattleChoose.GetBuffTargetUnitList
- MiniGameBattleChoose.GetNearestMonsterForCenterUnit
- MiniGameBattleChoose.GetNearestMonster
- MiniGameBattleChoose.GetOneFarthestMonster
- MiniGameBattleChoose.GetRandomMonster
- MiniGameBattleChoose.GetInRangeMonster
- MiniGameBattleChoose.GetInRangeMonsterByPosition
- MiniGameBattleChoose.IsTargetInRange
**Snippet:**
```lua
MiniGameBattleChoose = {}

function MiniGameBattleChoose.InitLocalVar()
end

function MiniGameBattleChoose.GetTargetUnitList(targetId, from, tos, skillConfig, buffConfig, chooseExtraParams)
  local targetUnitList = {}
  if 1000 == targetId then
    for i, v in ipairs(tos) do
      if v.unitUid then
```

---

## MP/MiniGameBattleConst.lua.lua
**Snippet:**
```lua
MINI_GAME_BATTLE_UNIT_TYPE = {
  CARD = 1,
  NORMAL_ENEMY = 2,
  ELIT_ENEMY = 3,
  BOSS_ENEMY = 4,
  WALL = 5,
  CARD_SUMMON = 6
}
MINI_GAME_BATTLE_SKILL_TYPE = {
  NORMAL = 1,
```

---

## MP/MiniGameBattleControl.lua.lua
**Functions:**
- MiniGameBattleControl.Init
- MiniGameBattleControl.Start
- MiniGameBattleControl.UpdateProcess
- MiniGameBattleControl.UpdateDisplay
- MiniGameBattleControl.Pause
- MiniGameBattleControl.Continue
- MiniGameBattleControl.Stop
**Snippet:**
```lua
MiniGameBattleControl = {}

function MiniGameBattleControl.Init()
  MiniGameBattleControl.curFixedFrame = 0
  MiniGameBattleControl.curFrame = 0
  MiniGameBattleControl.isPause = false
  MiniGameBattleControl.isOver = false
  MiniGameBattleControl.battleStartEnable = false
  MiniGameBattleControl.dealBuffPreCount = 0
  MiniGameBattleControl.baseTimeScale = MiniGameBattleData.speedList[MiniGameBattleData.speedIndex]
```

---

## MP/MiniGameBattleData.lua.lua
**Functions:**
- InitMiniGameBattleData
- ClearMiniGameBattleData
- MiniGameBattleDataMgr.AddExp
- MiniGameBattleDataMgr.DealExpAdd
**Snippet:**
```lua
function InitMiniGameBattleData(data)
  ClearMiniGameBattleData()
  
  MiniGameBattleData.stageId = data.stageId
  MiniGameBattleData.stageConfig = TableData.GetConfig(data.stageId, "BaseShootStage")
  MiniGameBattleData.buffList = {}
  MiniGameBattleData.isAuto = false
  local speed = PlayerPrefsUtil.GetInt(PLAYER_PREF_ENUM.MINI_GAME_BATTLE_SPEED, PLAYER_PREF_DEFAULT_VALUE.MINI_GAME_BATTLE_SPEED)
  if MiniGameBattleData.speedList[speed] then
    MiniGameBattleData.speedIndex = speed
```

---

## MP/MiniGameBattleDataCount.lua.lua
**Functions:**
- MiniGameBattleDataCount.Init
- MiniGameBattleDataCount.GetSkillHurt
**Snippet:**
```lua
MiniGameBattleDataCount = {}
local baoji_max, baoji_min

function MiniGameBattleDataCount.Init()
  local SkillParameterData = TableData.GetTable("BaseSkillParameter")
  baoji_max = SkillParameterData[40001003].data
  baoji_min = SkillParameterData[40001004].data
end

local PanDingBaoJi = function(atkUnit, defUnit, skillConfig)
```

---

## MP/MiniGameBattleEndWindow.lua.lua
**Functions:**
- MiniGameBattleEndWindow.ReInitData
- MiniGameBattleEndWindow.OnInit
- MiniGameBattleEndWindow.UpdateInfo
- MiniGameBattleEndWindow.InitBtn
- MiniGameBattleEndWindow.TouchClose
- MiniGameBattleEndWindow.OnClose
**Requires:**
- ActivityDungeon1017Battle_BattleEndWindowByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_BattleEndWindowByName")
local MiniGameBattleEndWindow = {}
local uis, contentPane, param

function MiniGameBattleEndWindow.ReInitData()
end

function MiniGameBattleEndWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.MiniGameBattleEndWindow.package, WinResConfig.MiniGameBattleEndWindow.comName, function(com)
    contentPane = com
```

---

## MP/MiniGameBattleExitWindow.lua.lua
**Functions:**
- MiniGameBattleExitWindow.ReInitData
- MiniGameBattleExitWindow.OnInit
- MiniGameBattleExitWindow.UpdateInfo
- MiniGameBattleExitWindow.InitBtn
- MiniGameBattleExitWindow.TouchClose
- MiniGameBattleExitWindow.TouchCloseBattle
- MiniGameBattleExitWindow.OnClose
**Requires:**
- ActivityDungeon1017Battle_BattleExitWindowByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_BattleExitWindowByName")
local MiniGameBattleExitWindow = {}
local uis, contentPane

function MiniGameBattleExitWindow.ReInitData()
end

function MiniGameBattleExitWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.MiniGameBattleExitWindow.package, WinResConfig.MiniGameBattleExitWindow.comName, function(com)
    contentPane = com
```

---

## MP/MiniGameBattleHurtNum.lua.lua
**Functions:**
- MiniGameBattleHurtNum.Init
- MiniGameBattleHurtNum.ClearPool
- MiniGameBattleHurtNum.ShowHurtNum
- MiniGameBattleHurtNum.ClearHurtNum
**Snippet:**
```lua
MiniGameBattleHurtNum = {}
local hudCom, battlePopObjectPool
local MiniGameBattleHurtNumType = {
  NOR_HURT = "NormalHitNumberTips",
  CRI_HURT = "CritHitNumberTips",
  NOR_TREATMENT = "GreenHpNumberTips"
}
local MiniGameBattleHurtNumComName = {
  NOR_HURT = "NormalHitNumber",
  CRI_HURT = "CritHitNumber",
```

---

## MP/MiniGameBattleMessageBar.lua.lua
**Functions:**
- MiniGameBattleMessageBar.BindInfo
- headInfo:Init
- headInfo:UpdateHp
- headInfo:Destroy
**Requires:**
- CommonResource_Activity17_MonsterHPByName
**Snippet:**
```lua
MiniGameBattleMessageBar = {}

function MiniGameBattleMessageBar.BindInfo(unit)
  require("CommonResource_Activity17_MonsterHPByName")
  local headInfo = {
    headObject = nil,
    curProgressBar = nil,
    uiPanel = nil,
    headInfoObj = nil,
    originParent = nil
```

---

## MP/MiniGameBattleMgr.lua.lua
**Functions:**
- MiniGameBattleMgr.InitBattle
- MiniGameBattleMgr.StartBattle
- MiniGameBattleMgr.CloseBattle
- MiniGameBattleMgr.SendBattleOverMsg
- MiniGameBattleMgr.GetRandom
- MiniGameBattleMgr.GetRandomNum
- MiniGameBattleMgr.LevelUp
**Snippet:**
```lua
MiniGameBattleMgr = {isBattleStart = false}

function MiniGameBattleMgr.InitBattle(data)
  ld("Battle")
  collectgarbage()
  MiniGameBattleCamera.enabled = true
  CameraUtil.SetCameraCullingMask(MiniGameBattleCameraObject, BATTLE_CONFIG_ENUM.CAMERA_CULLING_MASK)
  local baseWidth = 1334
  local baseHeight = 750
  local widthRatio = Screen.width / baseWidth
```

---

## MP/MiniGameBattlePauseWindow.lua.lua
**Functions:**
- MiniGameBattlePauseWindow.ReInitData
- MiniGameBattlePauseWindow.OnInit
- MiniGameBattlePauseWindow.UpdateInfo
- MiniGameBattlePauseWindow.InitBtn
- MiniGameBattlePauseWindow.TouchClose
- MiniGameBattlePauseWindow.OnClose
**Requires:**
- ActivityDungeon1017Battle_BattlePauseWindowByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_BattlePauseWindowByName")
local MiniGameBattlePauseWindow = {}
local uis, contentPane

function MiniGameBattlePauseWindow.ReInitData()
end

function MiniGameBattlePauseWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.MiniGameBattlePauseWindow.package, WinResConfig.MiniGameBattlePauseWindow.comName, function(com)
    contentPane = com
```

---

## MP/MiniGameBattleScene.lua.lua
**Functions:**
- InitMiniGameBattleScene
- ClearMiniGameBattleScene
- MiniGameBattleSceneMgr.InitBg
- MiniGameBattleSceneMgr.InitUI
- MiniGameBattleSceneMgr.InitUnit
- MiniGameBattleSceneMgr.AddUnit
- MiniGameBattleSceneMgr.RemoveUnit
- MiniGameBattleSceneMgr.RemoveFromAliveList
- MiniGameBattleSceneMgr.AddBullet
- MiniGameBattleSceneMgr.RemoveBullet
- MiniGameBattleSceneMgr.GetInitPosition
- MiniGameBattleSceneMgr.IsBattleOver
- MiniGameBattleSceneMgr.UpdateProcess
- MiniGameBattleSceneMgr.UpdateDisplay
- MiniGameBattleSceneMgr.UpdateBattleOverState
- MiniGameBattleSceneMgr.CreateMonster
- MiniGameBattleSceneMgr.GetPositionArea
- MiniGameBattleSceneMgr.GetRandomPositionIndex
- MiniGameBattleSceneMgr.AddMonster
- MiniGameBattleSceneMgr.GetUnitByUid
- MiniGameBattleSceneMgr.GetBulletByUid
- MiniGameBattleSceneMgr.DealClearTarget
- MiniGameBattleSceneMgr.Stop
**Snippet:**
```lua
function InitMiniGameBattleScene()
  ClearMiniGameBattleScene()
  
  local ceilLength = MiniGameBattleScene.ceilLength
  local stageConfig = MiniGameBattleData.stageConfig
  if stageConfig then
    local sizeX = stageConfig.size[1]
    local sizeY = stageConfig.size[2]
    MiniGameBattleScene.mapXCount = sizeX
    MiniGameBattleScene.mapYCount = sizeY
```

---

## MP/MiniGameBattleScriptList.lua.lua
**Requires:**
- MiniGameBattleMgr
- MiniGameBattleConst
- MiniGameBattleControl
- MiniGameBattleHurtNum
- MiniGameBattleScene
- MiniGameBattleBackground
- MiniGameBattleBuffMgr
- MiniGameBattleBuffEffect
- MiniGameBattleMessageBar
- MiniGameBattleData
- MiniGameBattleDataCount
- MiniGameBattleChoose
- MiniGameBattleAction
- MiniGameBattleActionDisplay
- MiniGameBattleBullet
- MiniGameBattleUnit
- MiniGameBattleBuff
**Snippet:**
```lua
local require = require
require("MiniGameBattleMgr")
require("MiniGameBattleConst")
require("MiniGameBattleControl")
require("MiniGameBattleHurtNum")
require("MiniGameBattleScene")
require("MiniGameBattleBackground")
require("MiniGameBattleBuffMgr")
require("MiniGameBattleBuffEffect")
require("MiniGameBattleMessageBar")
```

---

## MP/MiniGameBattleUIWindow.lua.lua
**Functions:**
- MiniGameBattleUIWindow.ReInitData
- MiniGameBattleUIWindow.OnInit
- MiniGameBattleUIWindow.InitInfo
- MiniGameBattleUIWindow.UpdateInfo
- MiniGameBattleUIWindow.UpdateTime
- MiniGameBattleUIWindow.UpdateWaveInfo
- MiniGameBattleUIWindow.UpdateKillInfo
- MiniGameBattleUIWindow.UpdateLevelInfo
- MiniGameBattleUIWindow.UpdateSelfHp
- MiniGameBattleUIWindow.UpdateSelfCardDamage
- MiniGameBattleUIWindow.UpdateSelfCardHead
- MiniGameBattleUIWindow.RenderCardHead
- skillList.itemRenderer
- MiniGameBattleUIWindow.InitBtn
- MiniGameBattleUIWindow.ClickReturnBtn
- MiniGameBattleUIWindow.ClickPauseBtn
- MiniGameBattleUIWindow.ClickSpeedBtn
- MiniGameBattleUIWindow.UpdateSpeedBtn
- MiniGameBattleUIWindow.UpdateSpeed
- MiniGameBattleUIWindow.ShowPlayBattleStart
- MiniGameBattleUIWindow.BattleStart
- MiniGameBattleUIWindow.ShowEnterAnim
- MiniGameBattleUIWindow.OnShowAnimationEnd
- MiniGameBattleUIWindow.OnClose
- MiniGameBattleUIWindow.HandleMessage
**Requires:**
- ActivityDungeon1017Battle_BattleUIWindowByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_BattleUIWindowByName")
local MiniGameBattleUIWindow = {}
local uis, contentPane
local selfUnitDamageList = {}

function MiniGameBattleUIWindow.ReInitData()
end

function MiniGameBattleUIWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.MiniGameBattleUIWindow.package, WinResConfig.MiniGameBattleUIWindow.comName, function(com)
```

---

## MP/MiniGameBattleUnit.lua.lua
**Functions:**
- MiniGameBattleUnit.NewUnit
- unit:Init
- unit:InitBaseData
- unit:InitData
- unit:InitAllSKillForChoose
- unit:GetCurSkillListForChoose
- unit:HaveSkills
- unit:GetTotalSkillLevel
- unit:GetSkillListForUI
- unit:GetSkillLevelBySkillTypes
- unit:GetSkillLevel
- unit:SaveSkill
- unit:DealBasicBuff
- unit:AddSummonUid
- unit:RemoveSummonUid
- unit:SaveSkillTrigger
- unit:CreateModel
- unit:GetAnimationTime
- unit:SetAnimation
- unit:AddAnimationEvent
- unit:RemoveAnimationEvent
- unit:UpdateFlip
- unit:SetModelFlip
- unit:SavePosition
- unit:UpdateModelPosition
- unit:UpdateSortingOrder
- unit:ChangeAnimation
- unit:DestroyModel
- unit:Destroy
- unit:ClearBuff
- unit:ContainEffectId
- unit:SetState
- unit:SetStateToDead
- unit:SetStateToDestroy
- unit:AddStateAction
- unit:Update
- unit:DealTriggerSkill
- unit:UpdateState
- unit:UpdateRagePerSecond
- unit:UpdateDisplay
- unit:UpdateBuffEffect
- unit:CreateEffect
- unit:SetModelTimeScale
- unit:UpdateModelTimeScale
- unit:UpdateStateDisplay
- unit:UpdateEffectFlip
- unit:RemoveEffect
- unit:RemoveAllEffect
- unit:RemoveAllBuffEffect
- unit:RemoveAllSkillEffect
- unit:IsWallInAttackTarget
- unit:IsTargetInAttackRange
- unit:HaveMonsterInAttackRange
- unit:GetDefaultWaitFrame
- unit:ResetNextAttackFrame
- unit:MeetAttackTimeCondition
- unit:IsCannotChooseType
- unit:CanRangeChosen
- unit:CanBuffChosen
- unit:IsAlive
- unit:IsDying
- unit:IsDead
- unit:IsDestroy
- unit:InitRestraint
- unit:InitAttrMap
- unit:SetInitAttr
- unit:SetAttr
- unit:ChangeAttr
- unit:GetHp
- unit:GetRage
- unit:GetSpdAtk
- unit:GetSpdMove
- unit:GetAttr
- unit:GetBaseAttr
- unit:GetBuffAttr
- unit:UpdateAttrCacheFromBuff
- unit:UpdateCachedBuffEffect
- unit:GetEffectTotalValue
- unit:GetLastFrameBySkillId
- unit:GetSkillAlreadyTriggerCount
- unit:SaveTriggerSkill
- unit:GetName
- unit:AddBuff
- unit:RemoveBuff
- unit:SetFreeze
- unit:SetTimePause
- unit:ClearControlState
- unit:OnBuffAttrChanged
- unit:UpdateTempHpPerAndMessageBar
- unit:UpdateTempHpPer
- unit:GetAttackTarget
- unit:SetAttackTargetUid
- unit:SaveDamage
- unit:SaveDamaged
**Snippet:**
```lua
MiniGameBattleUnit = {}
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

## MP/MiniGameSkillChoiceWindow.lua.lua
**Functions:**
- MiniGameSkillChoiceWindow.ReInitData
- MiniGameSkillChoiceWindow.OnInit
- MiniGameSkillChoiceWindow.RandomSkillList
- MiniGameSkillChoiceWindow.GetOneRandomSkill
- MiniGameSkillChoiceWindow.UpdateInfo
- MiniGameSkillChoiceWindow.StartCountdown
- MiniGameSkillChoiceWindow.UpdateSkillList
- MiniGameSkillChoiceWindow.InitBtn
- MiniGameSkillChoiceWindow.ClickSureBtn
- MiniGameSkillChoiceWindow.Close
- MiniGameSkillChoiceWindow.UpdateSkillSelect
- MiniGameSkillChoiceWindow.Select
- MiniGameSkillChoiceWindow.DealNextLevel
- MiniGameSkillChoiceWindow.OnClose
**Requires:**
- ActivityDungeon1017Battle_SkillChoiceWindowByName
**Snippet:**
```lua
require("ActivityDungeon1017Battle_SkillChoiceWindowByName")
local MiniGameSkillChoiceWindow = {}
local uis, contentPane, closeTimer
local closeDelayTime = 30
local selectSkill, skillHandList, cachedLevelUpList

function MiniGameSkillChoiceWindow.ReInitData()
end

function MiniGameSkillChoiceWindow.OnInit(bridgeObj)
```

---

## MP/ModelUtil.lua.lua
**Functions:**
- ModelUtil.GetFullPath
- ModelUtil.SetLive2dExpression
**Snippet:**
```lua
local ModelUtil = {}

function ModelUtil.GetFullPath(path, prefix)
  if path then
    prefix = prefix or RES_PATH_PREFIX.BATTLE_SPINE
    return prefix .. path
  end
end

function ModelUtil.SetLive2dExpression(gameObject, expression, pose)
```

---

## MP/MonthGetWindow.lua.lua
**Functions:**
- MonthGetWindow.OnInit
- MonthGetWindow.GetRechargeData
- MonthGetWindow.UpdateMonth
- MonthGetWindow.GetMonthId
- MonthGetWindow.ShowUI
- MonthGetWindow.InitBtn
- MonthGetWindow.ShowReward
- uis.Main.ItemList.itemRenderer
- MonthGetWindow.HandleMessage
- MonthGetWindow.OnClose
**Requires:**
- MonthlyPass_MonthGetWindowByName
**Snippet:**
```lua
require("MonthlyPass_MonthGetWindowByName")
local MonthGetWindow = {}
local uis, contentPane, data

function MonthGetWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.MonthGetWindow.package, WinResConfig.MonthGetWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetMonthlyPass_MonthGetWindowUis(contentPane)
    MonthGetWindow.InitBtn()
```

---

## MP/MonthlyPass_Circle1ByName.lua.lua
**Functions:**
- GetMonthlyPass_Circle1Uis
**Snippet:**
```lua
function GetMonthlyPass_Circle1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## MP/MonthlyPass_Circle2ByName.lua.lua
**Functions:**
- GetMonthlyPass_Circle2Uis
**Snippet:**
```lua
function GetMonthlyPass_Circle2Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## MP/MonthlyPass_MonthByName.lua.lua
**Functions:**
- GetMonthlyPass_MonthUis
**Snippet:**
```lua
function GetMonthlyPass_MonthUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.PicHolder = ui:GetChild("PicHolder")
  uis.root = ui
  return uis
end
```

---

## MP/MonthlyPass_MonthGetByName.lua.lua
**Functions:**
- GetMonthlyPass_MonthGetUis
**Requires:**
- CommonResource_PopupBgByName
- MonthlyPass_Circle2ByName
- MonthlyPass_Circle1ByName
- MonthlyPass_MonthByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("MonthlyPass_Circle2ByName")
require("MonthlyPass_Circle1ByName")
require("MonthlyPass_MonthByName")

function GetMonthlyPass_MonthGetUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.Circle2 = GetMonthlyPass_Circle2Uis(ui:GetChild("Circle2"))
  uis.Circle1 = GetMonthlyPass_Circle1Uis(ui:GetChild("Circle1"))
```

---

## MP/MonthlyPass_MonthGetWindowByName.lua.lua
**Functions:**
- GetMonthlyPass_MonthGetWindowUis
**Requires:**
- MonthlyPass_MonthGetByName
**Snippet:**
```lua
require("MonthlyPass_MonthGetByName")

function GetMonthlyPass_MonthGetWindowUis(ui)
  local uis = {}
  uis.Main = GetMonthlyPass_MonthGetUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/MoveEventTipsWindow.lua.lua
**Functions:**
- MoveEventTipsWindow.ReInitData
- MoveEventTipsWindow.OnInit
- MoveEventTipsWindow.UpdateInfo
- story_reader.getOptionDes
- story_reader.getOptionNext
- MoveEventTipsWindow.InitBtn
- MoveEventTipsWindow.OnShown
- MoveEventTipsWindow.OnClose
**Requires:**
- Abyss_MoveEventTipsWindowByName
**Snippet:**
```lua
require("Abyss_MoveEventTipsWindowByName")
local MoveEventTipsWindow = {}
local uis, contentPane, storyId, eventInfo, callback

function MoveEventTipsWindow.ReInitData()
end

function MoveEventTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.MoveEventTipsWindow.package, WinResConfig.MoveEventTipsWindow.comName, function(com)
    contentPane = com
```

---

## MP/MsgWaiter.lua.lua
**Functions:**
- MsgWaiter
- MsgWaiterObj.TryResendMsg
- MsgWaiterObj.ResetAllMsgResendInfo
- MsgWaiterObj.ResendAllTimeoutMsg
- MsgWaiterObj.ReceiveMsg
- MsgWaiterObj.Reset
- MsgWaiterObj.ClearCheckTimer
- MsgWaiterObj.Reconnect
- MsgWaiterObj.Destroy
- MsgWaiterObj.ShowWaitingWindow
- MsgWaiterObj.HideWaitingWindow
**Snippet:**
```lua
local MsgWaiterObj = {
  TIMEOUT_TIME = 15,
  RESEND_INTERVAL_LIST = {
    5,
    3,
    3
  },
  RESEND_MAX_COUNT = 3,
  waitMsgTable = {},
  sequenceMap = {}
```

---

## MP/MultipleMaterials_CloseBtnByName.lua.lua
**Functions:**
- GetMultipleMaterials_CloseBtnUis
**Snippet:**
```lua
function GetMultipleMaterials_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/MultipleMaterials_FunctionByName.lua.lua
**Functions:**
- GetMultipleMaterials_FunctionUis
**Snippet:**
```lua
function GetMultipleMaterials_FunctionUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.GoBtn = ui:GetChild("GoBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## MP/MultipleMaterials_GoBtnByName.lua.lua
**Functions:**
- GetMultipleMaterials_GoBtnUis
**Snippet:**
```lua
function GetMultipleMaterials_GoBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/MultipleMaterials_MultipleByName.lua.lua
**Functions:**
- GetMultipleMaterials_MultipleUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetMultipleMaterials_MultipleUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.FunctionList = ui:GetChild("FunctionList")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.root = ui
```

---

## MP/MultipleMaterials_MultipleWindowByName.lua.lua
**Functions:**
- GetMultipleMaterials_MultipleWindowUis
**Requires:**
- MultipleMaterials_MultipleByName
**Snippet:**
```lua
require("MultipleMaterials_MultipleByName")

function GetMultipleMaterials_MultipleWindowUis(ui)
  local uis = {}
  uis.Main = GetMultipleMaterials_MultipleUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/MultipleWindow.lua.lua
**Functions:**
- MultipleWindow.ReInitData
- MultipleWindow.OnInit
- MultipleWindow.UpdateInfo
- list.itemRenderer
- MultipleWindow.CloseWindow
- MultipleWindow.InitBtn
- MultipleWindow.OnClose
- MultipleWindow.CheckActivityEnd
- MultipleWindow.HandleMessage
**Requires:**
- MultipleMaterials_MultipleWindowByName
**Snippet:**
```lua
require("MultipleMaterials_MultipleWindowByName")
local MultipleWindow = {}
local uis, contentPane

function MultipleWindow.ReInitData()
end

function MultipleWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.MultipleWindow.package, WinResConfig.MultipleWindow.comName, function(com)
    contentPane = com
```

---

## MP/MusicPlaybackData.lua.lua
**Snippet:**
```lua
local playlist, favorites, playIndex
local SetPlaylist = function(list)
  playlist = list
end
local GetPlaylist = function()
  return playlist
end
local SetFavorites = function(list)
  favorites = list
end
```

---

## MP/MusicPlaybackMgr.lua.lua
**Snippet:**
```lua
local InPlaylist = function(soundId)
  local playlist = MusicPlaybackData.GetPlaylist()
  if playlist then
    local k = table.keyof(playlist, soundId)
    return type(k) == "number"
  end
  return false
end
local InFavorites = function(soundId)
  local favorites = MusicPlaybackData.GetFavorites()
```

---

## MP/MusicPlaybackScriptList.lua.lua
**Requires:**
- MusicPlaybackData
- MusicPlaybackMgr
- MusicPlaybackService
**Snippet:**
```lua
MusicPlaybackData = require("MusicPlaybackData")
MusicPlaybackMgr = require("MusicPlaybackMgr")
MusicPlaybackService = require("MusicPlaybackService")
```

---

## MP/MusicPlaybackService.lua.lua
**Snippet:**
```lua
local GetMusicPlaybackInfoReq = function(callback, rspCallback)
  Net.Send(Proto.MsgName.GetStoryListReq, {newStory = 0}, rspCallback)
end
local GetMusicPlaybackInfoRsp = function(msg)
  MusicPlaybackData.SetFavorites(msg.staredSoundLst)
  MusicPlaybackData.SetPlaylist(msg.soundPlaylist)
end
local FavoritesOperationReq = function(soundId, opType, rspCallback)
  Net.Send(Proto.MsgName.OperateStarSoundReq, {soundId = soundId, opType = opType}, rspCallback)
end
```

---

## MP/MusicPlayWindow.lua.lua
**Functions:**
- setAlpha
- MusicPlayWindow.OnInit
- MusicPlayWindow.LoadMusicBg
- MusicPlayWindow.ChangeSound
- uis.Main.SongInfo.AuthorInfo2List.itemRenderer
- uis.Main.SongInfo.AuthorInfo1List.itemRenderer
- MusicPlayWindow.Init
- list.itemRenderer
- MusicPlayWindow.Pause
- MusicPlayWindow.Resume
- MusicPlayWindow.FormationTime
- MusicPlayWindow.InitBtn
- MusicPlayWindow.HandleMessage
- MusicPlayWindow.OnPreClose
- MusicPlayWindow.OnClose
**Requires:**
- Story_MusicPlayWindowByName
**Snippet:**
```lua
require("Story_MusicPlayWindowByName")
local MusicPlayWindow = {}
local uis, contentPane, teamIndex, sound, chapterData, curSoundData, evtInstCache, audioVisualCtrl, entirety, musicPlayEffect, musicEnterEffect, postprocessvolumeCache, lastBtn
local elapse = 0
local lastElapse = 0
local fadeTime = 0.8
local isPause, isComplete, pauseTweenCache, stopTweenCache, volumeCache, lastEvt, tempLoader, bgmVolume
local bgmFadeTime = 1
local initAudioVisualiser = function()
  entirety = ResourceManager.Instantiate(RES_PATH_PREFIX.EFFECT .. "UI_prefab/Music/MusicGroup.prefab")
```

---

## MP/MusicWindow.lua.lua
**Functions:**
- RefreshPlaylist
- RefreshMusiclist
- RefreshPanelInfo
- MusicWindow.ReInitData
- MusicWindow.OnInit
- MusicWindow.UpdateInfo
- MusicWindow.InitBtn
- MusicWindow.OnClose
**Requires:**
- HomeMusic_MusicWindowByName
**Snippet:**
```lua
require("HomeMusic_MusicWindowByName")
local MusicWindow = {}
local uis, contentPane
local ALBUM_MUSIC_OFFSET = -1
local selectedMusiclist, selectedAlbumIndex, playingMusicSoundId, selectedPlaylistSoundId, RefreshPanelInfo, RefreshPlaylist, RefreshMusiclist, phonograph, playingEffects, maskTex, cachedMusicData
local RefreshPlayingMusicInfo = function()
  local musicInfoPanel = uis.Main.MusicChoiceRegion.MusicInfo
  local musicName, musicComposer, soundId
  if playingMusicSoundId then
    soundId = playingMusicSoundId
```

---

## MP/Net.lua.lua
**Functions:**
- Net.LuaMsgDispatcher
- Net.DecodePb
- Net.Send
- Net.AddListener
- Net.RemoveListener
- Net.OnConnected
- Net.OnDisConnect
- Net.OnError
- Net.ReConnect
- Net.IsConnect
- Net.IsReConnect
- Net.Connect
- Net.Init
- Net.Close
**Requires:**
- pb
- Protoc
- Proto
- ErrorCode
- Handler
- MsgWaiter
- MsgWaiter
**Snippet:**
```lua
local require = require
local pb = require("pb")
local protoc = require("Protoc")
Proto = require("Proto")
pb.option("enum_as_value")
pb.option("use_default_values")
assert(protoc:load(Proto.Schema))
local ErrorCode = require("ErrorCode")
require("Handler")
local SocketMgr = CS.LuaSocketManager.Singleton
```

---

## MP/NetCheckWindow.lua.lua
**Functions:**
- NetCheckWindow.ReInitData
- NetCheckWindow.OnInit
- NetCheckWindow.LaterShow
- NetCheckWindow.UpdateInfo
- NetCheckWindow.InitBtn
- NetCheckWindow.OnShown
- NetCheckWindow.OnHide
- NetCheckWindow.ClearTimer
- NetCheckWindow.OnClose
- NetCheckWindow.HandleMessage
**Requires:**
- Loading_NetCheckByName
**Snippet:**
```lua
require("Loading_NetCheckByName")
local NetCheckWindow = {}
local uis, contentPane, waitTimer, rightNow, effect

function NetCheckWindow.ReInitData()
end

function NetCheckWindow.OnInit(bridgeObj)
  bridgeObj:SetView(WinResConfig.NetCheckWindow.package, WinResConfig.NetCheckWindow.comName, function(com)
    contentPane = com
```

---

## MP/NoticeData.lua.lua
**Functions:**
- NoticeData.Init
- NoticeData.SaveRedDot
- NoticeData.NewIsShow
**Snippet:**
```lua
NoticeData = {
  notice = {}
}
local readUid = {}

function NoticeData.Init()
  local str = PlayerPrefsUtil.GetString(PLAYER_PREF_ENUM.NOTICE_NEW)
  if "0" ~= str then
    readUid = Json.decode(str)
  end
```

---

## MP/NoticeScriptList.lua.lua
**Requires:**
- NoticeData
- NoticeService
**Snippet:**
```lua
local require = require
require("NoticeData")
require("NoticeService")
```

---

## MP/NoticeService.lua.lua
**Functions:**
- NoticeService.Init
- NoticeService.GetAllNoticesReq
- NoticeService.GetAllMailsRsp
**Snippet:**
```lua
NoticeService = {}

function NoticeService.Init()
end

function NoticeService.GetAllNoticesReq(showTips, jump, notOpenWindow)
  local url = LoginData.GetClientServiceUrl() .. "/all_notices?channel=" .. LuaUtil.GetChannel()
  CS.HttpManager.Singleton:GetWebRequest(url, function()
    FunctionQueueUtil.SetFunEnd("Notice")
  end, function(str)
```

---

## MP/NoticeWindow.lua.lua
**Functions:**
- NoticeWindow.OnInit
- NoticeWindow.GetData
- NoticeWindow.CheckNoticeTime
- NoticeWindow.LoadTopTabRegion
- list.itemRenderer
- NoticeWindow.ClearListChild
- NoticeWindow.InitTab
- list.itemRenderer
- NoticeWindow.ClickLink
- NoticeWindow.StringSub
- NoticeWindow.LoadContent
- NoticeWindow.CloseWindow
- NoticeWindow.InitBtn
- NoticeWindow.HandleMessage
- NoticeWindow.OnClose
**Requires:**
- Notice_NoticeWindowByName
**Snippet:**
```lua
require("Notice_NoticeWindowByName")
local NoticeWindow = {}
local uis, contentPane, allNoticeUid, lastItem, noticeData

function NoticeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.NoticeWindow.package, WinResConfig.NoticeWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetNotice_NoticeWindowUis(contentPane)
    NoticeWindow.InitBtn()
```

---

## MP/Notice_CloseBtnByName.lua.lua
**Functions:**
- GetNotice_CloseBtnUis
**Snippet:**
```lua
function GetNotice_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/Notice_ContentPicByName.lua.lua
**Functions:**
- GetNotice_ContentPicUis
**Snippet:**
```lua
function GetNotice_ContentPicUis(ui)
  local uis = {}
  
  uis.PicBigLoader = ui:GetChild("PicBigLoader")
  uis.PicBigHolder = ui:GetChild("PicBigHolder")
  uis.root = ui
  return uis
end
```

---

## MP/Notice_ContentWordByName.lua.lua
**Functions:**
- GetNotice_ContentWordUis
**Snippet:**
```lua
function GetNotice_ContentWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Notice_LeftTabBtnAniByName.lua.lua
**Functions:**
- GetNotice_LeftTabBtnAniUis
**Snippet:**
```lua
function GetNotice_LeftTabBtnAniUis(ui)
  local uis = {}
  
  uis.LeftTabBtn = ui:GetChild("LeftTabBtn")
  uis.root = ui
  return uis
end
```

---

## MP/Notice_LeftTabBtnByName.lua.lua
**Functions:**
- GetNotice_LeftTabBtnUis
**Requires:**
- Notice_RedDotByName
**Snippet:**
```lua
require("Notice_RedDotByName")

function GetNotice_LeftTabBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.RedDot = GetNotice_RedDotUis(ui:GetChild("RedDot"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## MP/Notice_LeftTabRegionByName.lua.lua
**Functions:**
- GetNotice_LeftTabRegionUis
**Snippet:**
```lua
function GetNotice_LeftTabRegionUis(ui)
  local uis = {}
  
  uis.LeftTabList = ui:GetChild("LeftTabList")
  uis.root = ui
  return uis
end
```

---

## MP/Notice_NoticeByName.lua.lua
**Functions:**
- GetNotice_NoticeUis
**Requires:**
- CommonResource_PopupBgByName
- Notice_NoticeUIByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Notice_NoticeUIByName")

function GetNotice_NoticeUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.NoticeUI = GetNotice_NoticeUIUis(ui:GetChild("NoticeUI"))
  uis.root = ui
  return uis
```

---

## MP/Notice_NoticeUIByName.lua.lua
**Functions:**
- GetNotice_NoticeUIUis
**Requires:**
- Notice_LeftTabRegionByName
- Notice_TopTabRegionByName
**Snippet:**
```lua
require("Notice_LeftTabRegionByName")
require("Notice_TopTabRegionByName")

function GetNotice_NoticeUIUis(ui)
  local uis = {}
  uis.LeftTabRegion = GetNotice_LeftTabRegionUis(ui:GetChild("LeftTabRegion"))
  uis.TopTabRegion = GetNotice_TopTabRegionUis(ui:GetChild("TopTabRegion"))
  uis.ContentList = ui:GetChild("ContentList")
  uis.PicContentList = ui:GetChild("PicContentList")
  uis.CloseBtn = ui:GetChild("CloseBtn")
```

---

## MP/Notice_NoticeWindowByName.lua.lua
**Functions:**
- GetNotice_NoticeWindowUis
**Requires:**
- Notice_NoticeByName
**Snippet:**
```lua
require("Notice_NoticeByName")

function GetNotice_NoticeWindowUis(ui)
  local uis = {}
  uis.Main = GetNotice_NoticeUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Notice_RedDotByName.lua.lua
**Functions:**
- GetNotice_RedDotUis
**Snippet:**
```lua
function GetNotice_RedDotUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## MP/Notice_TopTabBtnBgByName.lua.lua
**Functions:**
- GetNotice_TopTabBtnBgUis
**Snippet:**
```lua
function GetNotice_TopTabBtnBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## MP/Notice_TopTabBtnByName.lua.lua
**Functions:**
- GetNotice_TopTabBtnUis
**Requires:**
- Notice_TopTabBtnBgByName
**Snippet:**
```lua
require("Notice_TopTabBtnBgByName")

function GetNotice_TopTabBtnUis(ui)
  local uis = {}
  uis.TopTabBtnBg = GetNotice_TopTabBtnBgUis(ui:GetChild("TopTabBtnBg"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## MP/Notice_TopTabRegionByName.lua.lua
**Functions:**
- GetNotice_TopTabRegionUis
**Snippet:**
```lua
function GetNotice_TopTabRegionUis(ui)
  local uis = {}
  
  uis.TopTabList = ui:GetChild("TopTabList")
  uis.root = ui
  return uis
end
```

---

## MP/NumberUtil.lua.lua
**Functions:**
- NumberUtil.IntToRome
**Snippet:**
```lua
local NumberUtil = {}
local romeList = {
  "Ⅰ",
  "Ⅱ",
  "Ⅲ",
  "Ⅳ",
  "Ⅴ",
  "Ⅵ",
  "Ⅶ",
  "Ⅷ",
```

---

## MP/OneYuanPassTipsWindow.lua.lua
**Functions:**
- OneYuanPassTipsWindow.ReInitData
- OneYuanPassTipsWindow.OnInit
- OneYuanPassTipsWindow.UpdateInfo
- OneYuanPassTipsWindow.InitBtn
- OneYuanPassTipsWindow.CloseWindow
- OneYuanPassTipsWindow.OnClose
**Requires:**
- Shop_OneYuanPassTipsWindowByName
**Snippet:**
```lua
require("Shop_OneYuanPassTipsWindowByName")
local OneYuanPassTipsWindow = {}
local uis, contentPane

function OneYuanPassTipsWindow.ReInitData()
end

function OneYuanPassTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.OneYuanPassTipsWindow.package, WinResConfig.OneYuanPassTipsWindow.comName, function(com)
    contentPane = com
```

---

## MP/OpalExchangeWindow.lua.lua
**Functions:**
- OpalExchangeWindow.ReInitData
- OpalExchangeWindow.OnInit
- OpalExchangeWindow.UpdateInfo
- OpalExchangeWindow.CloseWindow
- OpalExchangeWindow.InitBtn
- OpalExchangeWindow.OnClose
**Requires:**
- Message_OpalExchangeWindowByName
**Snippet:**
```lua
require("Message_OpalExchangeWindowByName")
local OpalExchangeWindow = {}
local uis, contentPane, num, closeFun, itemInfo, wordId

function OpalExchangeWindow.ReInitData()
end

function OpalExchangeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.OpalExchangeWindow.package, WinResConfig.OpalExchangeWindow.comName, function(com)
    contentPane = com
```

---

## MP/OpenSceneWindow.lua.lua
**Functions:**
- OpenSceneWindow.ReInitData
- OpenSceneWindow.OnInit
- OpenSceneWindow.UpdateInfo
- OpenSceneWindow.InitBtn
- OpenSceneWindow.CloseWindow
- OpenSceneWindow.OnInitEnd
- OpenSceneWindow.OnClose
**Requires:**
- PlotDungeon_OpenSceneWindowByName
**Snippet:**
```lua
require("PlotDungeon_OpenSceneWindowByName")
local OpenSceneWindow = {}
local uis, contentPane, chapterId, effect

function OpenSceneWindow.ReInitData()
end

function OpenSceneWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.OpenSceneWindow.package, WinResConfig.OpenSceneWindow.comName, function(com)
    contentPane = com
```

---

## MP/OpenTitleWindow.lua.lua
**Functions:**
- OpenTitleWindow.ReInitData
- OpenTitleWindow.OnInit
- OpenTitleWindow.UpdateInfo
- OpenTitleWindow.CloseWindow
- OpenTitleWindow.OnClose
**Requires:**
- PlotDungeon_OpenTitleWindowByName
**Snippet:**
```lua
require("PlotDungeon_OpenTitleWindowByName")
local OpenTitleWindow = {}
local uis, contentPane, effect, back

function OpenTitleWindow.ReInitData()
end

function OpenTitleWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.OpenTitleWindow.package, WinResConfig.OpenTitleWindow.comName, function(com)
    contentPane = com
```

---

## MP/OprRecordUtil.lua.lua
**Functions:**
- OprRecordUtil.SaveRecord
- OprRecordUtil.CacheRecord
- OprRecordUtil.GetRecord
- OprRecordUtil.IsAlreadyRecord
- OprRecordUtil.Clear
**Snippet:**
```lua
local OprRecordUtil = {}
local _records = {}
PLAYER_OPERATION_ENUM = {
  ARENA_MAP_NEW = 1,
  ARENA_BUILDING_NEW = 2,
  ADVENTURE_NEW = 3,
  OPEN_BADGE = 4,
  BOSS_STAGE_OPEN = 5,
  FISH_NEW = 6,
  SPECIAL_FASHION_NEW = 7
```

---

## MP/OtherPlayerInfoWindow.lua.lua
**Functions:**
- OtherPlayerInfoWindow.ReInitData
- OtherPlayerInfoWindow.OnInit
- OtherPlayerInfoWindow.UpdateInfo
- OtherPlayerInfoWindow.UpdateActorInfo
- OtherPlayerInfoWindow.UpdateCardShow
- OtherPlayerInfoWindow.GuildTeamVisible
- OtherPlayerInfoWindow.GuildViceCaptainVisible
- OtherPlayerInfoWindow.GuildLeaderVisible
- OtherPlayerInfoWindow.OutGuildVisible
- OtherPlayerInfoWindow.ReportVisible
- OtherPlayerInfoWindow.BlockVisible
- OtherPlayerInfoWindow.UnBlockVisible
- OtherPlayerInfoWindow.AddFriendVisible
- OtherPlayerInfoWindow.ChallengeVisible
- OtherPlayerInfoWindow.RemarkVisible
- OtherPlayerInfoWindow.SetGuildViceCaptain
- OtherPlayerInfoWindow.SetGuildLeader
- OtherPlayerInfoWindow.SetGuildTeam
- OtherPlayerInfoWindow.FreezeAuthorityTips
- OtherPlayerInfoWindow.KickOutGuild
- OtherPlayerInfoWindow.ClickInfoBtn
- OtherPlayerInfoWindow.ClickReportBtn
- OtherPlayerInfoWindow.ClickBlockBtn
- OtherPlayerInfoWindow.ClickUnBlockBtn
- OtherPlayerInfoWindow.ClickAddFriendBtn
- OtherPlayerInfoWindow.ClickPrivateChatBtn
- OtherPlayerInfoWindow.ClickChallengeBtn
- OtherPlayerInfoWindow.ClickRemarkBtn
- OtherPlayerInfoWindow.InitBtn
- OtherPlayerInfoWindow.Close
- OtherPlayerInfoWindow.OnClose
- OtherPlayerInfoWindow.HandleMessage
**Requires:**
- OtherPlayerInfo_OtherPlayerInfoWindowByName
**Snippet:**
```lua
require("OtherPlayerInfo_OtherPlayerInfoWindowByName")
local OtherPlayerInfoWindow = {}
local uis, contentPane, otherPlayerInfo, actorInfo, actorState, actorRemark, msg, isGuildEnter

function OtherPlayerInfoWindow.ReInitData()
end

function OtherPlayerInfoWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.OtherPlayerInfoWindow.package, WinResConfig.OtherPlayerInfoWindow.comName, function(com)
    contentPane = com
```

---

## MP/OtherPlayerInfo_CardShowAniByName.lua.lua
**Functions:**
- GetOtherPlayerInfo_CardShowAniUis
**Requires:**
- OtherPlayerInfo_CardShowByName
**Snippet:**
```lua
require("OtherPlayerInfo_CardShowByName")

function GetOtherPlayerInfo_CardShowAniUis(ui)
  local uis = {}
  uis.CardShow = GetOtherPlayerInfo_CardShowUis(ui:GetChild("CardShow"))
  uis.root = ui
  return uis
end
```

---

## MP/OtherPlayerInfo_CardShowByName.lua.lua
**Functions:**
- GetOtherPlayerInfo_CardShowUis
**Snippet:**
```lua
function GetOtherPlayerInfo_CardShowUis(ui)
  local uis = {}
  
  uis.CardShowLoader = ui:GetChild("CardShowLoader")
  uis.CardShowHolder = ui:GetChild("CardShowHolder")
  uis.root = ui
  return uis
end
```

---

## MP/OtherPlayerInfo_CloseBtnByName.lua.lua
**Functions:**
- GetOtherPlayerInfo_CloseBtnUis
**Snippet:**
```lua
function GetOtherPlayerInfo_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/OtherPlayerInfo_InfoBtnByName.lua.lua
**Functions:**
- GetOtherPlayerInfo_InfoBtnUis
**Snippet:**
```lua
function GetOtherPlayerInfo_InfoBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/OtherPlayerInfo_InfoByName.lua.lua
**Functions:**
- GetOtherPlayerInfo_InfoUis
**Requires:**
- OtherPlayerInfo_OnLineByName
**Snippet:**
```lua
require("OtherPlayerInfo_OnLineByName")

function GetOtherPlayerInfo_InfoUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.GuildTxt = ui:GetChild("GuildTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.OnLine = GetOtherPlayerInfo_OnLineUis(ui:GetChild("OnLine"))
  uis.FunctionList = ui:GetChild("FunctionList")
  uis.root = ui
```

---

## MP/OtherPlayerInfo_OnLineByName.lua.lua
**Functions:**
- GetOtherPlayerInfo_OnLineUis
**Snippet:**
```lua
function GetOtherPlayerInfo_OnLineUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/OtherPlayerInfo_OtherPlayerInfo1ByName.lua.lua
**Functions:**
- GetOtherPlayerInfo_OtherPlayerInfo1Uis
**Requires:**
- OtherPlayerInfo_CardShowAniByName
- OtherPlayerInfo_InfoByName
**Snippet:**
```lua
require("OtherPlayerInfo_CardShowAniByName")
require("OtherPlayerInfo_InfoByName")

function GetOtherPlayerInfo_OtherPlayerInfo1Uis(ui)
  local uis = {}
  uis.CardShowAni = GetOtherPlayerInfo_CardShowAniUis(ui:GetChild("CardShowAni"))
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.Info = GetOtherPlayerInfo_InfoUis(ui:GetChild("Info"))
  uis.root = ui
  return uis
```

---

## MP/OtherPlayerInfo_OtherPlayerInfo2ByName.lua.lua
**Functions:**
- GetOtherPlayerInfo_OtherPlayerInfo2Uis
**Requires:**
- OtherPlayerInfo_PopupBgByName
- OtherPlayerInfo_OtherPlayerInfo1ByName
**Snippet:**
```lua
require("OtherPlayerInfo_PopupBgByName")
require("OtherPlayerInfo_OtherPlayerInfo1ByName")

function GetOtherPlayerInfo_OtherPlayerInfo2Uis(ui)
  local uis = {}
  uis.PopupBg = GetOtherPlayerInfo_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.OtherPlayerInfo1 = GetOtherPlayerInfo_OtherPlayerInfo1Uis(ui:GetChild("OtherPlayerInfo1"))
  uis.root = ui
  return uis
```

---

## MP/OtherPlayerInfo_OtherPlayerInfoWindowByName.lua.lua
**Functions:**
- GetOtherPlayerInfo_OtherPlayerInfoWindowUis
**Requires:**
- OtherPlayerInfo_OtherPlayerInfo2ByName
**Snippet:**
```lua
require("OtherPlayerInfo_OtherPlayerInfo2ByName")

function GetOtherPlayerInfo_OtherPlayerInfoWindowUis(ui)
  local uis = {}
  uis.Main = GetOtherPlayerInfo_OtherPlayerInfo2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/OtherPlayerInfo_PopupBgByName.lua.lua
**Functions:**
- GetOtherPlayerInfo_PopupBgUis
**Snippet:**
```lua
function GetOtherPlayerInfo_PopupBgUis(ui)
  local uis = {}
  
  uis.BlurLoader = ui:GetChild("BlurLoader")
  uis.root = ui
  return uis
end
```

---

## MP/PactPassTipsWindow.lua.lua
**Functions:**
- PactPassTipsWindow.ReInitData
- PactPassTipsWindow.OnInit
- PactPassTipsWindow.UpdateInfo
- PactPassTipsWindow.InitBtn
- PactPassTipsWindow.CloseWindow
- PactPassTipsWindow.OnClose
**Requires:**
- Shop_PactPassTipsWindowByName
**Snippet:**
```lua
require("Shop_PactPassTipsWindowByName")
local PactPassTipsWindow = {}
local uis, contentPane

function PactPassTipsWindow.ReInitData()
end

function PactPassTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.PactPassTipsWindow.package, WinResConfig.PactPassTipsWindow.comName, function(com)
    contentPane = com
```

---

## MP/PassportBuyLevelWindow.lua.lua
**Functions:**
- PassportBuyLevelWindow.OnInit
- PassportBuyLevelWindow.ShowAssetsTips
- PassportBuyLevelWindow.OnShown
- PassportBuyLevelWindow.UpdateTextDisplay
- PassportBuyLevelWindow.Init
- PassportBuyLevelWindow.GetGold
- PassportBuyLevelWindow.ShowReward
- list.itemRenderer
- PassportBuyLevelWindow.GetRewardItem
- PassportBuyLevelWindow.GetLvData
- PassportBuyLevelWindow.GetRewardLvData
- PassportBuyLevelWindow.GetRewardByPhaseId
- PassportBuyLevelWindow.BuyLevelRsp
- PassportBuyLevelWindow.InitBtn
- waitFun
- PassportBuyLevelWindow.HandleMessage
- PassportBuyLevelWindow.OnClose
**Requires:**
- Passport_BuyLevelDesWindowByName
**Snippet:**
```lua
require("Passport_BuyLevelDesWindowByName")
local PassportBuyLevelWindow = {}
local uis, contentPane, lvData, curId, curLv, buyNum, itemId, lvMax, waitFun, rewardData, itemSort, transPlay, firstPlay, tatalGold

function PassportBuyLevelWindow.OnInit(bridgeObj)
  curId = bridgeObj.argTable[1]
  bridgeObj:SetViewAsync(WinResConfig.PassportBuyLevelWindow.package, WinResConfig.PassportBuyLevelWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetPassport_BuyLevelDesWindowUis(contentPane)
```

---

## MP/PassportBuyWindow.lua.lua
**Functions:**
- PassportBuyWindow.OnInit
- PassportBuyWindow.Init
- PassportBuyWindow.Close
- PassportBuyWindow.InitBtn
- PassportBuyWindow.HandleMessage
- PassportBuyWindow.OnClose
**Requires:**
- Passport_BuyWindowByName
**Snippet:**
```lua
require("Passport_BuyWindowByName")
local PassportBuyWindow = {}
local uis, contentPane, productId

function PassportBuyWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.PassportBuyWindow.package, WinResConfig.PassportBuyWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetPassport_BuyWindowUis(contentPane)
    PassportBuyWindow.InitBtn()
```

---

## MP/PassportData.lua.lua
**Functions:**
- PassportData.GetRewardDataByPhaseId
- PassportData.GetNextExpDataByPhaseId
- PassportData.GetPassInfo
- PassportData.GetNextPassport
- PassportData.GetAllPassport
- PassportData.GetActivityPassport
**Snippet:**
```lua
PassportData = {index = 0}
PassportData.infoArr = nil
PassportData.info = nil
PassportData.activityinfo = nil

function PassportData.GetRewardDataByPhaseId(phaseId)
  local data = {}
  local tb = {}
  local config = TableData.GetTable("BaseBattlePassReward")
  for i, v in pairs(config) do
```

---

## MP/PassportLevelUpTipsWindow.lua.lua
**Functions:**
- PassportLevelUpTipsWindow.ReInitData
- PassportLevelUpTipsWindow.OnInit
- PassportLevelUpTipsWindow.UpdateTextDisplay
- PassportLevelUpTipsWindow.InitBtn
- PassportLevelUpTipsWindow.OnShown
- PassportLevelUpTipsWindow.OnHide
- PassportLevelUpTipsWindow.OnClose
- PassportLevelUpTipsWindow.HandleMessage
**Requires:**
- Passport_LevelUpTipsWindowByName
**Snippet:**
```lua
require("Passport_LevelUpTipsWindowByName")
local PassportLevelUpTipsWindow = {}
local uis, contentPane, lv

function PassportLevelUpTipsWindow.ReInitData()
end

function PassportLevelUpTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.PassportLevelUpTipsWindow.package, WinResConfig.PassportLevelUpTipsWindow.comName, function(com)
    contentPane = com
```

---

## MP/PassportMgr.lua.lua
**Functions:**
- PassportMgr.OpenPassportWindow
- PassportMgr.GetPlatformId
- PassportMgr.UpdateByHomeWindow
**Snippet:**
```lua
PassportMgr = {}

function PassportMgr.OpenPassportWindow(isJump)
  if #PassportData.infoArr > 0 then
    PassportData.index = 0
    PassportData.tabIndex = 0
    PassportData.taskIndex = 0
    if isJump then
      JumpToWindow(WinResConfig.PassportWindow.name)
    else
```

---

## MP/PassportScriptList.lua.lua
**Requires:**
- PassportData
- PassportService
- PassportMgr
**Snippet:**
```lua
local require = require
require("PassportData")
require("PassportService")
require("PassportMgr")
```

---

## MP/PassportService.lua.lua
**Functions:**
- PassportService.Init
- PassportService.GetBattlePassInfoReq
- PassportService.GetBattlePassInfoRsp
- PassportService.BattlePassGetRewardReq
- PassportService.BattlePassGetRewardRsp
- PassportService.BattlePassTaskRewardReq
- PassportService.BattlePassTaskRewardRsp
- PassportService.BattlePassBuyLevelReq
- PassportService.BattlePassBuyLevelRsp
**Snippet:**
```lua
PassportService = {}

function PassportService.Init()
  Net.AddListener(Proto.MsgName.GetBattlePassInfoRsp, PassportService.GetBattlePassInfoRsp)
  Net.AddListener(Proto.MsgName.BattlePassGetRewardRsp, PassportService.BattlePassGetRewardRsp)
  Net.AddListener(Proto.MsgName.BattlePassTaskRewardRsp, PassportService.BattlePassTaskRewardRsp)
  Net.AddListener(Proto.MsgName.BattlePassBuyLevelRsp, PassportService.BattlePassBuyLevelRsp)
end

function PassportService.GetBattlePassInfoReq(rspCallback)
```

---

## MP/PassportWindow.lua.lua
**Functions:**
- PassportWindow.OnInit
- PassportWindow.GetBuyInfo
- PassportWindow.InitEffect
- PassportWindow.InitLv
- PassportWindow.ShowLevelUp
- PassportWindow.SaveLevel
- PassportWindow.GetRewardByLv
- PassportWindow.GetRewardNum
- PassportWindow.IsGetAllReward
- PassportWindow.LoadTabList
- uis.Main.TabList.itemRenderer
- PassportWindow.InitPassport
- uis.Main.TabRegion.TabList.itemRenderer
- PassportWindow.ShowReward
- PassportWindow.GetUpdateLv
- PassportWindow.RefreshListReward
- PassportWindow.UpdateTextDisplay
- PassportWindow.CheckItemTime
- PassportWindow.ShowQuitTips
- PassportWindow.RefreshUI
- PassportWindow.GetExpMxp
- PassportWindow.SetLevelInfo
- PassportWindow.InitList
- list.itemRenderer
- PassportWindow.SetListPos
- PassportWindow.RefreshReward
- PassportWindow.ShowGetEffect
- PassportWindow.RewardItemClick
- PassportWindow.IsReward
- PassportWindow.RefreshRewardFirst
- PassportWindow.RefreshRewardEnd
- PassportWindow.ShowState
- PassportWindow.RefreshRewardShow
- PassportWindow.RefreshRewardState
- PassportWindow.OpenBuyWindow
- PassportWindow.PassportActivate
- PassportWindow.InitBtn
- PassportWindow.ShowExpBarAnim
- PassportWindow.InitTask
- taskCycleList.itemRenderer
- PassportWindow.ShowTask
- list.itemRenderer
- PassportWindow.InitClothes
- PassportWindow.SetLastLv
- PassportWindow.OnShown
- PassportWindow.PlayFirstRewardEffect
- PassportWindow.PlayEndRewardEffect
- PassportWindow.HandleMessage
- PassportWindow.OnClose
**Requires:**
- Passport_PassportWindowByName
**Snippet:**
```lua
require("Passport_PassportWindowByName")
local PassportWindow = {}
local uis, contentPane, lvMax, modelType, expMax, rewardData, rewardType, rewardLv, listPage, passLv, jumpTb, isShowAllGet, passPortConfig, lvTween, lastLv, waitMessageId, newPassPort, animTween

function PassportWindow.OnInit(bridgeObj)
  bridgeObj:SetView(WinResConfig.PassportWindow.package, WinResConfig.PassportWindow.comName, function(com)
    contentPane = com
    contentPane:Center()
    uis = GetPassport_PassportWindowUis(contentPane)
    PassportWindow.GetBuyInfo()
```

---

## MP/Passport_AddBtnByName.lua.lua
**Functions:**
- GetPassport_AddBtnUis
**Snippet:**
```lua
function GetPassport_AddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_AllFrame_EByName.lua.lua
**Functions:**
- GetPassport_AllFrame_EUis
**Requires:**
- Passport_ItemFrame_EByName
- Passport_CardFrame_EByName
**Snippet:**
```lua
require("Passport_ItemFrame_EByName")
require("Passport_CardFrame_EByName")

function GetPassport_AllFrame_EUis(ui)
  local uis = {}
  uis.ItemFrame = GetPassport_ItemFrame_EUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetPassport_CardFrame_EUis(ui:GetChild("CardFrame"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## MP/Passport_AllFrame_MByName.lua.lua
**Functions:**
- GetPassport_AllFrame_MUis
**Requires:**
- Passport_ItemFrame_MByName
- Passport_CardFrame_MByName
**Snippet:**
```lua
require("Passport_ItemFrame_MByName")
require("Passport_CardFrame_MByName")

function GetPassport_AllFrame_MUis(ui)
  local uis = {}
  uis.ItemFrame = GetPassport_ItemFrame_MUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetPassport_CardFrame_MUis(ui:GetChild("CardFrame"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## MP/Passport_AllGetBtnByName.lua.lua
**Functions:**
- GetPassport_AllGetBtnUis
**Snippet:**
```lua
function GetPassport_AllGetBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_BigTabBtnBgByName.lua.lua
**Functions:**
- GetPassport_BigTabBtnBgUis
**Snippet:**
```lua
function GetPassport_BigTabBtnBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## MP/Passport_BigTabBtnByName.lua.lua
**Functions:**
- GetPassport_BigTabBtnUis
**Requires:**
- Passport_BigTabBtnCardBgByName
- Passport_BigTabBtnBgByName
**Snippet:**
```lua
require("Passport_BigTabBtnCardBgByName")
require("Passport_BigTabBtnBgByName")

function GetPassport_BigTabBtnUis(ui)
  local uis = {}
  uis.CardBg = GetPassport_BigTabBtnCardBgUis(ui:GetChild("CardBg"))
  uis.Bg = GetPassport_BigTabBtnBgUis(ui:GetChild("Bg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.buttonCtr = ui:GetController("button")
```

---

## MP/Passport_BigTabBtnCardBgByName.lua.lua
**Functions:**
- GetPassport_BigTabBtnCardBgUis
**Snippet:**
```lua
function GetPassport_BigTabBtnCardBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_BuyByName.lua.lua
**Functions:**
- GetPassport_BuyUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetPassport_BuyUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.PriceTxt = ui:GetChild("PriceTxt")
  uis.BuyItemBtn = ui:GetChild("BuyItemBtn")
  uis.root = ui
  return uis
```

---

## MP/Passport_BuyItemBtnByName.lua.lua
**Functions:**
- GetPassport_BuyItemBtnUis
**Snippet:**
```lua
function GetPassport_BuyItemBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_BuyLevelBtnByName.lua.lua
**Functions:**
- GetPassport_BuyLevelBtnUis
**Snippet:**
```lua
function GetPassport_BuyLevelBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_BuyLevelDes1ByName.lua.lua
**Functions:**
- GetPassport_BuyLevelDes1Uis
**Requires:**
- Passport_NumberStripByName
- Passport_BuyPriceNumberByName
**Snippet:**
```lua
require("Passport_NumberStripByName")
require("Passport_BuyPriceNumberByName")

function GetPassport_BuyLevelDes1Uis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.NumberStrip = GetPassport_NumberStripUis(ui:GetChild("NumberStrip"))
  uis.BuyPriceNumber = GetPassport_BuyPriceNumberUis(ui:GetChild("BuyPriceNumber"))
```

---

## MP/Passport_BuyLevelDes2ByName.lua.lua
**Functions:**
- GetPassport_BuyLevelDes2Uis
**Requires:**
- CommonResource_PopupBgByName
- Passport_BuyLevelDes1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Passport_BuyLevelDes1ByName")

function GetPassport_BuyLevelDes2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.BuyLevelDes1 = GetPassport_BuyLevelDes1Uis(ui:GetChild("BuyLevelDes1"))
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.root = ui
```

---

## MP/Passport_BuyLevelDesWindowByName.lua.lua
**Functions:**
- GetPassport_BuyLevelDesWindowUis
**Requires:**
- Passport_BuyLevelDes2ByName
**Snippet:**
```lua
require("Passport_BuyLevelDes2ByName")

function GetPassport_BuyLevelDesWindowUis(ui)
  local uis = {}
  uis.Main = GetPassport_BuyLevelDes2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Passport_BuyLevelItemByName.lua.lua
**Functions:**
- GetPassport_BuyLevelItemUis
**Requires:**
- Passport_AllFrame_MByName
**Snippet:**
```lua
require("Passport_AllFrame_MByName")

function GetPassport_BuyLevelItemUis(ui)
  local uis = {}
  uis.AllFrame_M = GetPassport_AllFrame_MUis(ui:GetChild("AllFrame_M"))
  uis.root = ui
  return uis
end
```

---

## MP/Passport_BuyPriceNumberByName.lua.lua
**Functions:**
- GetPassport_BuyPriceNumberUis
**Snippet:**
```lua
function GetPassport_BuyPriceNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_BuyWindowByName.lua.lua
**Functions:**
- GetPassport_BuyWindowUis
**Requires:**
- Passport_BuyByName
**Snippet:**
```lua
require("Passport_BuyByName")

function GetPassport_BuyWindowUis(ui)
  local uis = {}
  uis.Main = GetPassport_BuyUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Passport_CardClothesRegionByName.lua.lua
**Functions:**
- GetPassport_CardClothesRegionUis
**Requires:**
- Passport_ClothesTipsByName
- Passport_CardQBByName
- Passport_ClothesNameTipsByName
- Passport_Clothes_Grade1ByName
- Passport_Clothes_Grade2ByName
**Snippet:**
```lua
require("Passport_ClothesTipsByName")
require("Passport_CardQBByName")
require("Passport_ClothesNameTipsByName")
require("Passport_Clothes_Grade1ByName")
require("Passport_Clothes_Grade2ByName")

function GetPassport_CardClothesRegionUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.ClothesTips = GetPassport_ClothesTipsUis(ui:GetChild("ClothesTips"))
```

---

## MP/Passport_CardFrame_EByName.lua.lua
**Functions:**
- GetPassport_CardFrame_EUis
**Requires:**
- Passport_ItemCardPicByName
**Snippet:**
```lua
require("Passport_ItemCardPicByName")

function GetPassport_CardFrame_EUis(ui)
  local uis = {}
  uis.ItemCardPic = GetPassport_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## MP/Passport_CardFrame_MByName.lua.lua
**Functions:**
- GetPassport_CardFrame_MUis
**Requires:**
- Passport_ItemCardPicByName
**Snippet:**
```lua
require("Passport_ItemCardPicByName")

function GetPassport_CardFrame_MUis(ui)
  local uis = {}
  uis.ItemCardPic = GetPassport_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## MP/Passport_CardQBByName.lua.lua
**Functions:**
- GetPassport_CardQBUis
**Snippet:**
```lua
function GetPassport_CardQBUis(ui)
  local uis = {}
  
  uis.QBHolder = ui:GetChild("QBHolder")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_ClothesBuyBtnByName.lua.lua
**Functions:**
- GetPassport_ClothesBuyBtnUis
**Snippet:**
```lua
function GetPassport_ClothesBuyBtnUis(ui)
  local uis = {}
  
  uis.PriceTxt = ui:GetChild("PriceTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_ClothesGetTipsByName.lua.lua
**Functions:**
- GetPassport_ClothesGetTipsUis
**Snippet:**
```lua
function GetPassport_ClothesGetTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_ClothesNameTipsByName.lua.lua
**Functions:**
- GetPassport_ClothesNameTipsUis
**Snippet:**
```lua
function GetPassport_ClothesNameTipsUis(ui)
  local uis = {}
  
  uis.Name1Txt = ui:GetChild("Name1Txt")
  uis.Name2Txt = ui:GetChild("Name2Txt")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_ClothesTipsByName.lua.lua
**Functions:**
- GetPassport_ClothesTipsUis
**Snippet:**
```lua
function GetPassport_ClothesTipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_Clothes_Grade1ByName.lua.lua
**Functions:**
- GetPassport_Clothes_Grade1Uis
**Requires:**
- Passport_ClothesGetTipsByName
**Snippet:**
```lua
require("Passport_ClothesGetTipsByName")

function GetPassport_Clothes_Grade1Uis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.BuyBtn = ui:GetChild("BuyBtn")
  uis.GetTips = GetPassport_ClothesGetTipsUis(ui:GetChild("GetTips"))
  uis.ItemList = ui:GetChild("ItemList")
```

---

## MP/Passport_Clothes_Grade2ByName.lua.lua
**Functions:**
- GetPassport_Clothes_Grade2Uis
**Requires:**
- Passport_ClothesGetTipsByName
**Snippet:**
```lua
require("Passport_ClothesGetTipsByName")

function GetPassport_Clothes_Grade2Uis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.BuyBtn = ui:GetChild("BuyBtn")
  uis.GetTips = GetPassport_ClothesGetTipsUis(ui:GetChild("GetTips"))
  uis.ItemList = ui:GetChild("ItemList")
```

---

## MP/Passport_Clothes_ItemAddByName.lua.lua
**Functions:**
- GetPassport_Clothes_ItemAddUis
**Snippet:**
```lua
function GetPassport_Clothes_ItemAddUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## MP/Passport_Clothes_ItemCardPicByName.lua.lua
**Functions:**
- GetPassport_Clothes_ItemCardPicUis
**Snippet:**
```lua
function GetPassport_Clothes_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.buyCtr = ui:GetController("buy")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_Clothes_ItemFrameByName.lua.lua
**Functions:**
- GetPassport_Clothes_ItemFrameUis
**Requires:**
- Passport_Clothes_ItemCardPicByName
**Snippet:**
```lua
require("Passport_Clothes_ItemCardPicByName")

function GetPassport_Clothes_ItemFrameUis(ui)
  local uis = {}
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.ItemCardPic = GetPassport_Clothes_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.typeCtr = ui:GetController("type")
```

---

## MP/Passport_EndTwoByName.lua.lua
**Functions:**
- GetPassport_EndTwoUis
**Requires:**
- Passport_AllFrame_EByName
**Snippet:**
```lua
require("Passport_AllFrame_EByName")

function GetPassport_EndTwoUis(ui)
  local uis = {}
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.LevelWordTxt = ui:GetChild("LevelWordTxt")
  uis.Item1 = GetPassport_AllFrame_EUis(ui:GetChild("Item1"))
  uis.Item2 = GetPassport_AllFrame_EUis(ui:GetChild("Item2"))
```

---

## MP/Passport_ExpProgressBarByName.lua.lua
**Functions:**
- GetPassport_ExpProgressBarUis
**Requires:**
- Passport_ExpProgressFillByName
**Snippet:**
```lua
require("Passport_ExpProgressFillByName")

function GetPassport_ExpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetPassport_ExpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## MP/Passport_ExpProgressFillByName.lua.lua
**Functions:**
- GetPassport_ExpProgressFillUis
**Snippet:**
```lua
function GetPassport_ExpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## MP/Passport_FullLevelByName.lua.lua
**Functions:**
- GetPassport_FullLevelUis
**Snippet:**
```lua
function GetPassport_FullLevelUis(ui)
  local uis = {}
  
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_ItemCardPicByName.lua.lua
**Functions:**
- GetPassport_ItemCardPicUis
**Snippet:**
```lua
function GetPassport_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_ItemFrame_EByName.lua.lua
**Functions:**
- GetPassport_ItemFrame_EUis
**Snippet:**
```lua
function GetPassport_ItemFrame_EUis(ui)
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

## MP/Passport_ItemFrame_MByName.lua.lua
**Functions:**
- GetPassport_ItemFrame_MUis
**Snippet:**
```lua
function GetPassport_ItemFrame_MUis(ui)
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

## MP/Passport_LevelBuyBtnByName.lua.lua
**Functions:**
- GetPassport_LevelBuyBtnUis
**Snippet:**
```lua
function GetPassport_LevelBuyBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_LevelByName.lua.lua
**Functions:**
- GetPassport_LevelUis
**Requires:**
- Passport_WeekNumberByName
- Passport_FullLevelByName
**Snippet:**
```lua
require("Passport_WeekNumberByName")
require("Passport_FullLevelByName")

function GetPassport_LevelUis(ui)
  local uis = {}
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.ExpNumberTxt = ui:GetChild("ExpNumberTxt")
  uis.WeekNumber = GetPassport_WeekNumberUis(ui:GetChild("WeekNumber"))
  uis.ExpProgressBar = ui:GetChild("ExpProgressBar")
  uis.LevelBuyBtn = ui:GetChild("LevelBuyBtn")
```

---

## MP/Passport_LevelRegionByName.lua.lua
**Functions:**
- GetPassport_LevelRegionUis
**Requires:**
- Passport_LevelByName
**Snippet:**
```lua
require("Passport_LevelByName")

function GetPassport_LevelRegionUis(ui)
  local uis = {}
  uis.LevelBtn = GetPassport_LevelUis(ui:GetChild("LevelBtn"))
  uis.root = ui
  return uis
end
```

---

## MP/Passport_LevelTitleByName.lua.lua
**Functions:**
- GetPassport_LevelTitleUis
**Snippet:**
```lua
function GetPassport_LevelTitleUis(ui)
  local uis = {}
  
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.LevelWordTxt = ui:GetChild("LevelWordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_LevelUpBgByName.lua.lua
**Functions:**
- GetPassport_LevelUpBgUis
**Snippet:**
```lua
function GetPassport_LevelUpBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## MP/Passport_LevelUpTipsByName.lua.lua
**Functions:**
- GetPassport_LevelUpTipsUis
**Requires:**
- CommonResource_PopupBgByName
- Passport_LevelUpBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("Passport_LevelUpBgByName")

function GetPassport_LevelUpTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.LevelUpBg = GetPassport_LevelUpBgUis(ui:GetChild("LevelUpBg"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
```

---

## MP/Passport_LevelUpTipsWindowByName.lua.lua
**Functions:**
- GetPassport_LevelUpTipsWindowUis
**Requires:**
- Passport_LevelUpTipsByName
**Snippet:**
```lua
require("Passport_LevelUpTipsByName")

function GetPassport_LevelUpTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetPassport_LevelUpTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Passport_MaxBtnByName.lua.lua
**Functions:**
- GetPassport_MaxBtnUis
**Snippet:**
```lua
function GetPassport_MaxBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_MiddleRegionByName.lua.lua
**Functions:**
- GetPassport_MiddleRegionUis
**Snippet:**
```lua
function GetPassport_MiddleRegionUis(ui)
  local uis = {}
  
  uis.MiddleList = ui:GetChild("MiddleList")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_MinBtnByName.lua.lua
**Functions:**
- GetPassport_MinBtnUis
**Snippet:**
```lua
function GetPassport_MinBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_NumberStripByName.lua.lua
**Functions:**
- GetPassport_NumberStripUis
**Snippet:**
```lua
function GetPassport_NumberStripUis(ui)
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

## MP/Passport_PassportByName.lua.lua
**Functions:**
- GetPassport_PassportUis
**Requires:**
- CommonResource_BackGroundByName
- Passport_RewardRegionByName
- Passport_LevelRegionByName
- Passport_TaskRegionByName
- Passport_TimeByName
- Passport_CardClothesRegionByName
- Passport_TabRegionByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("Passport_RewardRegionByName")
require("Passport_LevelRegionByName")
require("Passport_TaskRegionByName")
require("Passport_TimeByName")
require("Passport_CardClothesRegionByName")
require("Passport_TabRegionByName")
require("CommonResource_CurrencyReturnByName")

function GetPassport_PassportUis(ui)
```

---

## MP/Passport_PassportPic1ByName.lua.lua
**Functions:**
- GetPassport_PassportPic1Uis
**Snippet:**
```lua
function GetPassport_PassportPic1Uis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_PassportPicByName.lua.lua
**Functions:**
- GetPassport_PassportPicUis
**Snippet:**
```lua
function GetPassport_PassportPicUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.BuyTxt = ui:GetChild("BuyTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_PassportWindowByName.lua.lua
**Functions:**
- GetPassport_PassportWindowUis
**Requires:**
- Passport_PassportByName
**Snippet:**
```lua
require("Passport_PassportByName")

function GetPassport_PassportWindowUis(ui)
  local uis = {}
  uis.Main = GetPassport_PassportUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/Passport_ReduceBtnByName.lua.lua
**Functions:**
- GetPassport_ReduceBtnUis
**Snippet:**
```lua
function GetPassport_ReduceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_RewardRegionByName.lua.lua
**Functions:**
- GetPassport_RewardRegionUis
**Requires:**
- Passport_MiddleRegionByName
- Passport_StartTwoByName
- Passport_EndTwoByName
**Snippet:**
```lua
require("Passport_MiddleRegionByName")
require("Passport_StartTwoByName")
require("Passport_EndTwoByName")

function GetPassport_RewardRegionUis(ui)
  local uis = {}
  uis.MiddleList = GetPassport_MiddleRegionUis(ui:GetChild("MiddleList"))
  uis.StartTwo = GetPassport_StartTwoUis(ui:GetChild("StartTwo"))
  uis.EndTwo = GetPassport_EndTwoUis(ui:GetChild("EndTwo"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## MP/Passport_RewardTwoByName.lua.lua
**Functions:**
- GetPassport_RewardTwoUis
**Requires:**
- Passport_RewardTwoItemByName
- Passport_LevelTitleByName
**Snippet:**
```lua
require("Passport_RewardTwoItemByName")
require("Passport_LevelTitleByName")

function GetPassport_RewardTwoUis(ui)
  local uis = {}
  uis.Reward1 = GetPassport_RewardTwoItemUis(ui:GetChild("Reward1"))
  uis.Reward2 = GetPassport_RewardTwoItemUis(ui:GetChild("Reward2"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Title = GetPassport_LevelTitleUis(ui:GetChild("Title"))
```

---

## MP/Passport_RewardTwoItemByName.lua.lua
**Functions:**
- GetPassport_RewardTwoItemUis
**Requires:**
- Passport_AllFrame_MByName
**Snippet:**
```lua
require("Passport_AllFrame_MByName")

function GetPassport_RewardTwoItemUis(ui)
  local uis = {}
  uis.Item = GetPassport_AllFrame_MUis(ui:GetChild("Item"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_StartTwoByName.lua.lua
**Functions:**
- GetPassport_StartTwoUis
**Requires:**
- Passport_PassportPic1ByName
- Passport_PassportPicByName
**Snippet:**
```lua
require("Passport_PassportPic1ByName")
require("Passport_PassportPicByName")

function GetPassport_StartTwoUis(ui)
  local uis = {}
  uis.Pic1 = GetPassport_PassportPic1Uis(ui:GetChild("Pic1"))
  uis.Pic = GetPassport_PassportPicUis(ui:GetChild("Pic"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.root = ui
```

---

## MP/Passport_TabBtnByName.lua.lua
**Functions:**
- GetPassport_TabBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetPassport_TabBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## MP/Passport_TabRegionByName.lua.lua
**Functions:**
- GetPassport_TabRegionUis
**Snippet:**
```lua
function GetPassport_TabRegionUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_TaskAniByName.lua.lua
**Functions:**
- GetPassport_TaskAniUis
**Requires:**
- Passport_TaskByName
**Snippet:**
```lua
require("Passport_TaskByName")

function GetPassport_TaskAniUis(ui)
  local uis = {}
  uis.Task = GetPassport_TaskUis(ui:GetChild("Task"))
  uis.root = ui
  return uis
end
```

---

## MP/Passport_TaskByName.lua.lua
**Functions:**
- GetPassport_TaskUis
**Requires:**
- Passport_TaskExpByName
**Snippet:**
```lua
require("Passport_TaskExpByName")

function GetPassport_TaskUis(ui)
  local uis = {}
  uis.TaskfreshBtn = ui:GetChild("TaskfreshBtn")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.ProgressTxt = ui:GetChild("ProgressTxt")
  uis.TaskGuideBtn = ui:GetChild("TaskGuideBtn")
  uis.TaskExp = GetPassport_TaskExpUis(ui:GetChild("TaskExp"))
  uis.GetTxt = ui:GetChild("GetTxt")
```

---

## MP/Passport_TaskCycleBtnByName.lua.lua
**Functions:**
- GetPassport_TaskCycleBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetPassport_TaskCycleBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## MP/Passport_TaskExpByName.lua.lua
**Functions:**
- GetPassport_TaskExpUis
**Snippet:**
```lua
function GetPassport_TaskExpUis(ui)
  local uis = {}
  
  uis.ItemPicLoader = ui:GetChild("ItemPicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_TaskfreshBtnByName.lua.lua
**Functions:**
- GetPassport_TaskfreshBtnUis
**Snippet:**
```lua
function GetPassport_TaskfreshBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_TaskGuideBtnByName.lua.lua
**Functions:**
- GetPassport_TaskGuideBtnUis
**Snippet:**
```lua
function GetPassport_TaskGuideBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_TaskMaxByName.lua.lua
**Functions:**
- GetPassport_TaskMaxUis
**Snippet:**
```lua
function GetPassport_TaskMaxUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_TaskRegionByName.lua.lua
**Functions:**
- GetPassport_TaskRegionUis
**Requires:**
- Passport_TaskMaxByName
**Snippet:**
```lua
require("Passport_TaskMaxByName")

function GetPassport_TaskRegionUis(ui)
  local uis = {}
  uis.TaskCycleList = ui:GetChild("TaskCycleList")
  uis.TaskList = ui:GetChild("TaskList")
  uis.TaskMax = GetPassport_TaskMaxUis(ui:GetChild("TaskMax"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## MP/Passport_TimeByName.lua.lua
**Functions:**
- GetPassport_TimeUis
**Snippet:**
```lua
function GetPassport_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## MP/Passport_WeekNumberByName.lua.lua
**Functions:**
- GetPassport_WeekNumberUis
**Snippet:**
```lua
function GetPassport_WeekNumberUis(ui)
  local uis = {}
  
  uis.LimitTxt = ui:GetChild("LimitTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## MP/pathfinder.lua.lua
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
- Node:new
- Node:totalCost
- PathFinder:new
- PathFinder:search
**Snippet:**
```lua
local NODE_CATEGORY = {
  UNVISITED = "UNVISITED",
  OPENED = "OPENED",
  CLOSED = "CLOSED"
}
local new_BinaryHeap = function(compareFunc)
  local BinaryHeap = {}
  BinaryHeap.__index = BinaryHeap
  
  function BinaryHeap:new()
```

---

## MP/PhysicsConst.lua.lua
**Snippet:**
```lua
PI = 3.1415926
MathConst = {
  ZERO = 2.0E-4,
  DEG_TO_RAD = PI / 180,
  RAD_TO_DEG = 180 / PI,
  HALF_PI = PI / 2,
  DOUBLE_PI = PI * 2,
  Infinity = math.huge
}
Utils = {
```

---

## MP/PhysicsScriptList.lua.lua
**Requires:**
- PhysicsConst
- Create
- Body
- World
- Arbiter
- CollideManager
- Shape
- Circle
- Polygon
- Segment
- Rectangle
**Snippet:**
```lua
require("PhysicsConst")
require("Create")
Body = require("Body")
World = require("World")
Arbiter = require("Arbiter")
CollideManager = require("CollideManager")
Shape = require("Shape")
Circle = require("Circle")
Polygon = require("Polygon")
Segment = require("Segment")
```

---

## MP/PlayerInfo_AllBtnByName.lua.lua
**Functions:**
- GetPlayerInfo_AllBtnUis
**Snippet:**
```lua
function GetPlayerInfo_AllBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_AnBtnByName.lua.lua
**Functions:**
- GetPlayerInfo_AnBtnUis
**Requires:**
- PlayerInfo_BgAniByName
**Snippet:**
```lua
require("PlayerInfo_BgAniByName")

function GetPlayerInfo_AnBtnUis(ui)
  local uis = {}
  uis.BgAni = GetPlayerInfo_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_ArrayBtnByName.lua.lua
**Functions:**
- GetPlayerInfo_ArrayBtnUis
**Snippet:**
```lua
function GetPlayerInfo_ArrayBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_BattleBtnByName.lua.lua
**Functions:**
- GetPlayerInfo_BattleBtnUis
**Snippet:**
```lua
function GetPlayerInfo_BattleBtnUis(ui)
  local uis = {}
  
  uis.Name1Txt = ui:GetChild("Name1Txt")
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Name2Txt = ui:GetChild("Name2Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## MP/PlayerInfo_BgAniByName.lua.lua
**Functions:**
- GetPlayerInfo_BgAniUis
**Snippet:**
```lua
function GetPlayerInfo_BgAniUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_BirthdayByName.lua.lua
**Functions:**
- GetPlayerInfo_BirthdayUis
**Snippet:**
```lua
function GetPlayerInfo_BirthdayUis(ui)
  local uis = {}
  
  uis.BirthdayTxt = ui:GetChild("BirthdayTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.SetBtn = ui:GetChild("SetBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_BirthdaySetBtnByName.lua.lua
**Functions:**
- GetPlayerInfo_BirthdaySetBtnUis
**Snippet:**
```lua
function GetPlayerInfo_BirthdaySetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_BirthdayTipsByName.lua.lua
**Functions:**
- GetPlayerInfo_BirthdayTipsUis
**Requires:**
- CommonResource_PopupBgByName
- CommonResource_Popup_BByName
- PlayerInfo_BirthdayTips_TimeRegionByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("CommonResource_Popup_BByName")
require("PlayerInfo_BirthdayTips_TimeRegionByName")

function GetPlayerInfo_BirthdayTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Popup_B = GetCommonResource_Popup_BUis(ui:GetChild("Popup_B"))
  uis.Rename1 = GetPlayerInfo_BirthdayTips_TimeRegionUis(ui:GetChild("Rename1"))
```

---

## MP/PlayerInfo_BirthdayTipsWindowByName.lua.lua
**Functions:**
- GetPlayerInfo_BirthdayTipsWindowUis
**Requires:**
- PlayerInfo_BirthdayTipsByName
**Snippet:**
```lua
require("PlayerInfo_BirthdayTipsByName")

function GetPlayerInfo_BirthdayTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetPlayerInfo_BirthdayTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_BirthdayTips_TimeAniByName.lua.lua
**Functions:**
- GetPlayerInfo_BirthdayTips_TimeAniUis
**Snippet:**
```lua
function GetPlayerInfo_BirthdayTips_TimeAniUis(ui)
  local uis = {}
  
  uis.TimeList = ui:GetChild("TimeList")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_BirthdayTips_TimeByName.lua.lua
**Functions:**
- GetPlayerInfo_BirthdayTips_TimeUis
**Requires:**
- PlayerInfo_BirthdayTips_TimeAniByName
**Snippet:**
```lua
require("PlayerInfo_BirthdayTips_TimeAniByName")

function GetPlayerInfo_BirthdayTips_TimeUis(ui)
  local uis = {}
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.Time = GetPlayerInfo_BirthdayTips_TimeAniUis(ui:GetChild("Time"))
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_BirthdayTips_TimeNumberByName.lua.lua
**Functions:**
- GetPlayerInfo_BirthdayTips_TimeNumberUis
**Snippet:**
```lua
function GetPlayerInfo_BirthdayTips_TimeNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_BirthdayTips_TimeRegionByName.lua.lua
**Functions:**
- GetPlayerInfo_BirthdayTips_TimeRegionUis
**Requires:**
- PlayerInfo_BirthdayTips_TimeByName
**Snippet:**
```lua
require("PlayerInfo_BirthdayTips_TimeByName")

function GetPlayerInfo_BirthdayTips_TimeRegionUis(ui)
  local uis = {}
  uis.Month = GetPlayerInfo_BirthdayTips_TimeUis(ui:GetChild("Month"))
  uis.Day = GetPlayerInfo_BirthdayTips_TimeUis(ui:GetChild("Day"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_CardHeadByName.lua.lua
**Functions:**
- GetPlayerInfo_CardHeadUis
**Requires:**
- PlayerInfo_CardHeadPicByName
**Snippet:**
```lua
require("PlayerInfo_CardHeadPicByName")

function GetPlayerInfo_CardHeadUis(ui)
  local uis = {}
  uis.CardHeadPic = GetPlayerInfo_CardHeadPicUis(ui:GetChild("CardHeadPic"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_CardHeadPicByName.lua.lua
**Functions:**
- GetPlayerInfo_CardHeadPicUis
**Snippet:**
```lua
function GetPlayerInfo_CardHeadPicUis(ui)
  local uis = {}
  
  uis.HeadLoader = ui:GetChild("HeadLoader")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_CardNumberByName.lua.lua
**Functions:**
- GetPlayerInfo_CardNumberUis
**Snippet:**
```lua
function GetPlayerInfo_CardNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.CardNumberTxt = ui:GetChild("CardNumberTxt")
  uis.HeadList = ui:GetChild("HeadList")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_CardPicByName.lua.lua
**Functions:**
- GetPlayerInfo_CardPicUis
**Snippet:**
```lua
function GetPlayerInfo_CardPicUis(ui)
  local uis = {}
  
  uis.CardPicLoader = ui:GetChild("CardPicLoader")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_CardScreenByName.lua.lua
**Functions:**
- GetPlayerInfo_CardScreenUis
**Requires:**
- PlayerInfo_GatherChoiceByName
**Snippet:**
```lua
require("PlayerInfo_GatherChoiceByName")

function GetPlayerInfo_CardScreenUis(ui)
  local uis = {}
  uis.PopupCloseBtn = ui:GetChild("PopupCloseBtn")
  uis.GatherChoice = GetPlayerInfo_GatherChoiceUis(ui:GetChild("GatherChoice"))
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_CardShowByName.lua.lua
**Functions:**
- GetPlayerInfo_CardShowUis
**Snippet:**
```lua
function GetPlayerInfo_CardShowUis(ui)
  local uis = {}
  
  uis.CardShowLoader = ui:GetChild("CardShowLoader")
  uis.CardShowHolder = ui:GetChild("CardShowHolder")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_CardTipsByName.lua.lua
**Functions:**
- GetPlayerInfo_CardTipsUis
**Requires:**
- PlayerInfo_Quality1_1ByName
- PlayerInfo_CardPicByName
- PlayerInfo_Quality1_2ByName
- CommonResource_OccupationByName
- CommonResource_CardBreachByName
**Snippet:**
```lua
require("PlayerInfo_Quality1_1ByName")
require("PlayerInfo_CardPicByName")
require("PlayerInfo_Quality1_2ByName")
require("CommonResource_OccupationByName")
require("CommonResource_CardBreachByName")

function GetPlayerInfo_CardTipsUis(ui)
  local uis = {}
  uis.Quality1_1 = GetPlayerInfo_Quality1_1Uis(ui:GetChild("Quality1_1"))
  uis.CardPic = GetPlayerInfo_CardPicUis(ui:GetChild("CardPic"))
```

---

## MP/PlayerInfo_CardTypeChoiceByName.lua.lua
**Functions:**
- GetPlayerInfo_CardTypeChoiceUis
**Snippet:**
```lua
function GetPlayerInfo_CardTypeChoiceUis(ui)
  local uis = {}
  
  uis.ArrayBtn = ui:GetChild("ArrayBtn")
  uis.AllBtn = ui:GetChild("AllBtn")
  uis.ScreenBtn = ui:GetChild("ScreenBtn")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_ChoiceByName.lua.lua
**Functions:**
- GetPlayerInfo_ChoiceUis
**Requires:**
- CommonResource_BackGroundByName
- PlayerInfo_CardTypeChoiceByName
- PlayerInfo_CardScreenByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("PlayerInfo_CardTypeChoiceByName")
require("PlayerInfo_CardScreenByName")
require("CommonResource_CurrencyReturnByName")

function GetPlayerInfo_ChoiceUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.ChoiceList = ui:GetChild("ChoiceList")
  uis.CardTypeChoice = GetPlayerInfo_CardTypeChoiceUis(ui:GetChild("CardTypeChoice"))
```

---

## MP/PlayerInfo_ChoiceHeadByName.lua.lua
**Functions:**
- GetPlayerInfo_ChoiceHeadUis
**Requires:**
- CommonResource_PopupBgByName
- PlayerInfo_ChoiceHeadTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("PlayerInfo_ChoiceHeadTipsByName")

function GetPlayerInfo_ChoiceHeadUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.ChoiceHeadTips = GetPlayerInfo_ChoiceHeadTipsUis(ui:GetChild("ChoiceHeadTips"))
  uis.root = ui
  return uis
```

---

## MP/PlayerInfo_ChoiceHeadDetailsByName.lua.lua
**Functions:**
- GetPlayerInfo_ChoiceHeadDetailsUis
**Requires:**
- CommonResource_HeadByName
- PlayerInfo_ChoiceHeadDetailsLockByName
- PlayerInfo_ChoiceHeadDetailsInUseByName
**Snippet:**
```lua
require("CommonResource_HeadByName")
require("PlayerInfo_ChoiceHeadDetailsLockByName")
require("PlayerInfo_ChoiceHeadDetailsInUseByName")

function GetPlayerInfo_ChoiceHeadDetailsUis(ui)
  local uis = {}
  uis.Head = GetCommonResource_HeadUis(ui:GetChild("Head"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.UseBtn = ui:GetChild("UseBtn")
  uis.Lock = GetPlayerInfo_ChoiceHeadDetailsLockUis(ui:GetChild("Lock"))
```

---

## MP/PlayerInfo_ChoiceHeadDetailsInUseByName.lua.lua
**Functions:**
- GetPlayerInfo_ChoiceHeadDetailsInUseUis
**Snippet:**
```lua
function GetPlayerInfo_ChoiceHeadDetailsInUseUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_ChoiceHeadDetailsLockByName.lua.lua
**Functions:**
- GetPlayerInfo_ChoiceHeadDetailsLockUis
**Snippet:**
```lua
function GetPlayerInfo_ChoiceHeadDetailsLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_ChoiceHeadDetailsUseBtnByName.lua.lua
**Functions:**
- GetPlayerInfo_ChoiceHeadDetailsUseBtnUis
**Snippet:**
```lua
function GetPlayerInfo_ChoiceHeadDetailsUseBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_ChoiceHeadDetailsWordByName.lua.lua
**Functions:**
- GetPlayerInfo_ChoiceHeadDetailsWordUis
**Snippet:**
```lua
function GetPlayerInfo_ChoiceHeadDetailsWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_ChoiceHeadFramePicBgByName.lua.lua
**Functions:**
- GetPlayerInfo_ChoiceHeadFramePicBgUis
**Snippet:**
```lua
function GetPlayerInfo_ChoiceHeadFramePicBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_ChoiceHeadPicAniBtnByName.lua.lua
**Functions:**
- GetPlayerInfo_ChoiceHeadPicAniBtnUis
**Requires:**
- PlayerInfo_ChoiceHeadPicByName
**Snippet:**
```lua
require("PlayerInfo_ChoiceHeadPicByName")

function GetPlayerInfo_ChoiceHeadPicAniBtnUis(ui)
  local uis = {}
  uis.ChoiceHeadPic = GetPlayerInfo_ChoiceHeadPicUis(ui:GetChild("ChoiceHeadPic"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_ChoiceHeadPicBgByName.lua.lua
**Functions:**
- GetPlayerInfo_ChoiceHeadPicBgUis
**Snippet:**
```lua
function GetPlayerInfo_ChoiceHeadPicBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_ChoiceHeadPicByName.lua.lua
**Functions:**
- GetPlayerInfo_ChoiceHeadPicUis
**Requires:**
- PlayerInfo_ChoiceHeadPicBgByName
- PlayerInfo_ChoiceHeadFramePicBgByName
- PlayerInfo_ChoiceHeadPicUseByName
**Snippet:**
```lua
require("PlayerInfo_ChoiceHeadPicBgByName")
require("PlayerInfo_ChoiceHeadFramePicBgByName")
require("PlayerInfo_ChoiceHeadPicUseByName")

function GetPlayerInfo_ChoiceHeadPicUis(ui)
  local uis = {}
  uis.HeadBg = GetPlayerInfo_ChoiceHeadPicBgUis(ui:GetChild("HeadBg"))
  uis.FramePic = GetPlayerInfo_ChoiceHeadFramePicBgUis(ui:GetChild("FramePic"))
  uis.Use = GetPlayerInfo_ChoiceHeadPicUseUis(ui:GetChild("Use"))
  uis.c2Ctr = ui:GetController("c2")
```

---

## MP/PlayerInfo_ChoiceHeadPicUseByName.lua.lua
**Functions:**
- GetPlayerInfo_ChoiceHeadPicUseUis
**Snippet:**
```lua
function GetPlayerInfo_ChoiceHeadPicUseUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_ChoiceHeadTipsByName.lua.lua
**Functions:**
- GetPlayerInfo_ChoiceHeadTipsUis
**Requires:**
- PlayerInfo_ChoiceHeadDetailsByName
**Snippet:**
```lua
require("PlayerInfo_ChoiceHeadDetailsByName")

function GetPlayerInfo_ChoiceHeadTipsUis(ui)
  local uis = {}
  uis.Tab1Btn = ui:GetChild("Tab1Btn")
  uis.Tab2Btn = ui:GetChild("Tab2Btn")
  uis.Tab3Btn = ui:GetChild("Tab3Btn")
  uis.HeadList = ui:GetChild("HeadList")
  uis.Details = GetPlayerInfo_ChoiceHeadDetailsUis(ui:GetChild("Details"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## MP/PlayerInfo_ChoiceHeadWindowByName.lua.lua
**Functions:**
- GetPlayerInfo_ChoiceHeadWindowUis
**Requires:**
- PlayerInfo_ChoiceHeadByName
**Snippet:**
```lua
require("PlayerInfo_ChoiceHeadByName")

function GetPlayerInfo_ChoiceHeadWindowUis(ui)
  local uis = {}
  uis.Main = GetPlayerInfo_ChoiceHeadUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_ChoiceTab1BtnByName.lua.lua
**Functions:**
- GetPlayerInfo_ChoiceTab1BtnUis
**Snippet:**
```lua
function GetPlayerInfo_ChoiceTab1BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_ChoiceTab2BtnByName.lua.lua
**Functions:**
- GetPlayerInfo_ChoiceTab2BtnUis
**Snippet:**
```lua
function GetPlayerInfo_ChoiceTab2BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_ChoiceTab3BtnByName.lua.lua
**Functions:**
- GetPlayerInfo_ChoiceTab3BtnUis
**Snippet:**
```lua
function GetPlayerInfo_ChoiceTab3BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_ChoiceTipsBtnByName.lua.lua
**Functions:**
- GetPlayerInfo_ChoiceTipsBtnUis
**Requires:**
- PlayerInfo_CardTipsByName
**Snippet:**
```lua
require("PlayerInfo_CardTipsByName")

function GetPlayerInfo_ChoiceTipsBtnUis(ui)
  local uis = {}
  uis.CardTips = GetPlayerInfo_CardTipsUis(ui:GetChild("CardTips"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_ChoiceWindowByName.lua.lua
**Functions:**
- GetPlayerInfo_ChoiceWindowUis
**Requires:**
- PlayerInfo_ChoiceByName
**Snippet:**
```lua
require("PlayerInfo_ChoiceByName")

function GetPlayerInfo_ChoiceWindowUis(ui)
  local uis = {}
  uis.Main = GetPlayerInfo_ChoiceUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_CloseBtnByName.lua.lua
**Functions:**
- GetPlayerInfo_CloseBtnUis
**Snippet:**
```lua
function GetPlayerInfo_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_CodeBtnByName.lua.lua
**Functions:**
- GetPlayerInfo_CodeBtnUis
**Snippet:**
```lua
function GetPlayerInfo_CodeBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_CopyBtnByName.lua.lua
**Functions:**
- GetPlayerInfo_CopyBtnUis
**Snippet:**
```lua
function GetPlayerInfo_CopyBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_ElementChoiceByName.lua.lua
**Functions:**
- GetPlayerInfo_ElementChoiceUis
**Snippet:**
```lua
function GetPlayerInfo_ElementChoiceUis(ui)
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

## MP/PlayerInfo_FangYuBtnByName.lua.lua
**Functions:**
- GetPlayerInfo_FangYuBtnUis
**Requires:**
- PlayerInfo_BgAniByName
**Snippet:**
```lua
require("PlayerInfo_BgAniByName")

function GetPlayerInfo_FangYuBtnUis(ui)
  local uis = {}
  uis.BgAni = GetPlayerInfo_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_FaShiBtnByName.lua.lua
**Functions:**
- GetPlayerInfo_FaShiBtnUis
**Requires:**
- PlayerInfo_BgAniByName
**Snippet:**
```lua
require("PlayerInfo_BgAniByName")

function GetPlayerInfo_FaShiBtnUis(ui)
  local uis = {}
  uis.BgAni = GetPlayerInfo_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_GatherChoiceByName.lua.lua
**Functions:**
- GetPlayerInfo_GatherChoiceUis
**Requires:**
- PlayerInfo_OccupationChoiceByName
- PlayerInfo_ElementChoiceByName
**Snippet:**
```lua
require("PlayerInfo_OccupationChoiceByName")
require("PlayerInfo_ElementChoiceByName")

function GetPlayerInfo_GatherChoiceUis(ui)
  local uis = {}
  uis.OccupationChoice = GetPlayerInfo_OccupationChoiceUis(ui:GetChild("OccupationChoice"))
  uis.ElementChoice = GetPlayerInfo_ElementChoiceUis(ui:GetChild("ElementChoice"))
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_GongJianBtnByName.lua.lua
**Functions:**
- GetPlayerInfo_GongJianBtnUis
**Requires:**
- PlayerInfo_BgAniByName
**Snippet:**
```lua
require("PlayerInfo_BgAniByName")

function GetPlayerInfo_GongJianBtnUis(ui)
  local uis = {}
  uis.BgAni = GetPlayerInfo_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_GuangBtnByName.lua.lua
**Functions:**
- GetPlayerInfo_GuangBtnUis
**Requires:**
- PlayerInfo_BgAniByName
**Snippet:**
```lua
require("PlayerInfo_BgAniByName")

function GetPlayerInfo_GuangBtnUis(ui)
  local uis = {}
  uis.BgAni = GetPlayerInfo_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_GuildByName.lua.lua
**Functions:**
- GetPlayerInfo_GuildUis
**Snippet:**
```lua
function GetPlayerInfo_GuildUis(ui)
  local uis = {}
  
  uis.GuildTxt = ui:GetChild("GuildTxt")
  uis.AddressTxt = ui:GetChild("AddressTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_HideBtnByName.lua.lua
**Functions:**
- GetPlayerInfo_HideBtnUis
**Snippet:**
```lua
function GetPlayerInfo_HideBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_HuoBtnByName.lua.lua
**Functions:**
- GetPlayerInfo_HuoBtnUis
**Requires:**
- PlayerInfo_BgAniByName
**Snippet:**
```lua
require("PlayerInfo_BgAniByName")

function GetPlayerInfo_HuoBtnUis(ui)
  local uis = {}
  uis.BgAni = GetPlayerInfo_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_JinZhanBtnByName.lua.lua
**Functions:**
- GetPlayerInfo_JinZhanBtnUis
**Requires:**
- PlayerInfo_BgAniByName
**Snippet:**
```lua
require("PlayerInfo_BgAniByName")

function GetPlayerInfo_JinZhanBtnUis(ui)
  local uis = {}
  uis.BgAni = GetPlayerInfo_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_LeftByName.lua.lua
**Functions:**
- GetPlayerInfo_LeftUis
**Requires:**
- CommonResource_HeadByName
- PlayerInfo_TimeByName
- PlayerInfo_LevelByName
- PlayerInfo_GuildByName
- PlayerInfo_BirthdayByName
- PlayerInfo_CardNumberByName
**Snippet:**
```lua
require("CommonResource_HeadByName")
require("PlayerInfo_TimeByName")
require("PlayerInfo_LevelByName")
require("PlayerInfo_GuildByName")
require("PlayerInfo_BirthdayByName")
require("PlayerInfo_CardNumberByName")

function GetPlayerInfo_LeftUis(ui)
  local uis = {}
  uis.Head = GetCommonResource_HeadUis(ui:GetChild("Head"))
```

---

## MP/PlayerInfo_LevelByName.lua.lua
**Functions:**
- GetPlayerInfo_LevelUis
**Snippet:**
```lua
function GetPlayerInfo_LevelUis(ui)
  local uis = {}
  
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.IDTxt = ui:GetChild("IDTxt")
  uis.CopyBtn = ui:GetChild("CopyBtn")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_MaterialByName.lua.lua
**Functions:**
- GetPlayerInfo_MaterialUis
**Snippet:**
```lua
function GetPlayerInfo_MaterialUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_MuBtnByName.lua.lua
**Functions:**
- GetPlayerInfo_MuBtnUis
**Requires:**
- PlayerInfo_BgAniByName
**Snippet:**
```lua
require("PlayerInfo_BgAniByName")

function GetPlayerInfo_MuBtnUis(ui)
  local uis = {}
  uis.BgAni = GetPlayerInfo_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_NameBtnByName.lua.lua
**Functions:**
- GetPlayerInfo_NameBtnUis
**Snippet:**
```lua
function GetPlayerInfo_NameBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_OccupationChoiceByName.lua.lua
**Functions:**
- GetPlayerInfo_OccupationChoiceUis
**Snippet:**
```lua
function GetPlayerInfo_OccupationChoiceUis(ui)
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

## MP/PlayerInfo_OtherMaterialByName.lua.lua
**Functions:**
- GetPlayerInfo_OtherMaterialUis
**Snippet:**
```lua
function GetPlayerInfo_OtherMaterialUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_PlayerByName.lua.lua
**Functions:**
- GetPlayerInfo_PlayerUis
**Requires:**
- CommonResource_BackGroundByName
- PlayerInfo_CardShowByName
- PlayerInfo_LeftByName
- PlayerInfo_RightByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("PlayerInfo_CardShowByName")
require("PlayerInfo_LeftByName")
require("PlayerInfo_RightByName")

function GetPlayerInfo_PlayerUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.CardShow = GetPlayerInfo_CardShowUis(ui:GetChild("CardShow"))
  uis.CloseBtn = ui:GetChild("CloseBtn")
```

---

## MP/PlayerInfo_PlayerWindowByName.lua.lua
**Functions:**
- GetPlayerInfo_PlayerWindowUis
**Requires:**
- PlayerInfo_PlayerByName
**Snippet:**
```lua
require("PlayerInfo_PlayerByName")

function GetPlayerInfo_PlayerWindowUis(ui)
  local uis = {}
  uis.Main = GetPlayerInfo_PlayerUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_PlotByName.lua.lua
**Functions:**
- GetPlayerInfo_PlotUis
**Snippet:**
```lua
function GetPlayerInfo_PlotUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_Quality1_1ByName.lua.lua
**Functions:**
- GetPlayerInfo_Quality1_1Uis
**Snippet:**
```lua
function GetPlayerInfo_Quality1_1Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_Quality1_2ByName.lua.lua
**Functions:**
- GetPlayerInfo_Quality1_2Uis
**Snippet:**
```lua
function GetPlayerInfo_Quality1_2Uis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_RightByName.lua.lua
**Functions:**
- GetPlayerInfo_RightUis
**Requires:**
- PlayerInfo_TitleByName
- PlayerInfo_PlotByName
- PlayerInfo_OtherMaterialByName
**Snippet:**
```lua
require("PlayerInfo_TitleByName")
require("PlayerInfo_PlotByName")
require("PlayerInfo_OtherMaterialByName")

function GetPlayerInfo_RightUis(ui)
  local uis = {}
  uis.Title1 = GetPlayerInfo_TitleUis(ui:GetChild("Title1"))
  uis.Plot = GetPlayerInfo_PlotUis(ui:GetChild("Plot"))
  uis.BattleBtn = ui:GetChild("BattleBtn")
  uis.Title2 = GetPlayerInfo_TitleUis(ui:GetChild("Title2"))
```

---

## MP/PlayerInfo_ScreenBtnByName.lua.lua
**Functions:**
- GetPlayerInfo_ScreenBtnUis
**Snippet:**
```lua
function GetPlayerInfo_ScreenBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_ShuiBtnByName.lua.lua
**Functions:**
- GetPlayerInfo_ShuiBtnUis
**Requires:**
- PlayerInfo_BgAniByName
**Snippet:**
```lua
require("PlayerInfo_BgAniByName")

function GetPlayerInfo_ShuiBtnUis(ui)
  local uis = {}
  uis.BgAni = GetPlayerInfo_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_TimeByName.lua.lua
**Functions:**
- GetPlayerInfo_TimeUis
**Snippet:**
```lua
function GetPlayerInfo_TimeUis(ui)
  local uis = {}
  
  uis.DayTxt = ui:GetChild("DayTxt")
  uis.RegisterTxt = ui:GetChild("RegisterTxt")
  uis.RegisterTimeTxt = ui:GetChild("RegisterTimeTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_TitleByName.lua.lua
**Functions:**
- GetPlayerInfo_TitleUis
**Snippet:**
```lua
function GetPlayerInfo_TitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.HideBtn = ui:GetChild("HideBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerInfo_TuXiBtnByName.lua.lua
**Functions:**
- GetPlayerInfo_TuXiBtnUis
**Requires:**
- PlayerInfo_BgAniByName
**Snippet:**
```lua
require("PlayerInfo_BgAniByName")

function GetPlayerInfo_TuXiBtnUis(ui)
  local uis = {}
  uis.BgAni = GetPlayerInfo_BgAniUis(ui:GetChild("BgAni"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerLevelUp_EffectByName.lua.lua
**Functions:**
- GetPlayerLevelUp_EffectUis
**Snippet:**
```lua
function GetPlayerLevelUp_EffectUis(ui)
  local uis = {}
  
  uis.EffectLoader = ui:GetChild("EffectLoader")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerLevelUp_LevelUpByName.lua.lua
**Functions:**
- GetPlayerLevelUp_LevelUpUis
**Requires:**
- PlayerLevelUp_EffectByName
**Snippet:**
```lua
require("PlayerLevelUp_EffectByName")

function GetPlayerLevelUp_LevelUpUis(ui)
  local uis = {}
  uis.Effect = GetPlayerLevelUp_EffectUis(ui:GetChild("Effect"))
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.ContentList = ui:GetChild("ContentList")
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.root = ui
  return uis
```

---

## MP/PlayerLevelUp_LevelUpWindowByName.lua.lua
**Functions:**
- GetPlayerLevelUp_LevelUpWindowUis
**Requires:**
- PlayerLevelUp_LevelUpByName
**Snippet:**
```lua
require("PlayerLevelUp_LevelUpByName")

function GetPlayerLevelUp_LevelUpWindowUis(ui)
  local uis = {}
  uis.Main = GetPlayerLevelUp_LevelUpUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/PlayerLevelUp_OpenWordAniByName.lua.lua
**Functions:**
- GetPlayerLevelUp_OpenWordAniUis
**Requires:**
- PlayerLevelUp_OpenWordByName
**Snippet:**
```lua
require("PlayerLevelUp_OpenWordByName")

function GetPlayerLevelUp_OpenWordAniUis(ui)
  local uis = {}
  uis.OpenWord = GetPlayerLevelUp_OpenWordUis(ui:GetChild("OpenWord"))
  uis.root = ui
  return uis
end
```

---

## MP/PlayerLevelUp_OpenWordByName.lua.lua
**Functions:**
- GetPlayerLevelUp_OpenWordUis
**Snippet:**
```lua
function GetPlayerLevelUp_OpenWordUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerPrefsUtil.lua.lua
**Functions:**
- PlayerPrefsUtil.SetInt
- PlayerPrefsUtil.GetInt
- PlayerPrefsUtil.SetString
- PlayerPrefsUtil.GetString
- PlayerPrefsUtil.SetFloat
- PlayerPrefsUtil.GetFloat
**Snippet:**
```lua
local PlayerPrefsUtil = {}
local PlayerPrefs = CS.UnityEngine.PlayerPrefs
PLAYER_PREF_ENUM = {
  CARD_TYPE = "CARD_TYPE",
  GUILD_LEVEL = "GUILD_LEVEL",
  GUILD_LIMIT_LEVEL = "GUILD_LIMIT_LEVEL",
  TEMP_ACCOUNT = "TEMP_ACCOUNT",
  TEMP_PASSWORD = "TEMP_PASSWORD",
  NEW_SEASON = "NEW_SEASON",
  ARENA_DAY = "ARENA_DAY",
```

---

## MP/PlayerReturnsPopupWindow.lua.lua
**Functions:**
- PlayerReturnsPopupWindow.ReInitData
- PlayerReturnsPopupWindow.OnInit
- PlayerReturnsPopupWindow.UpdateInfo
- uis.Main.Tips.WordList.itemRenderer
- PlayerReturnsPopupWindow.InitBtn
- PlayerReturnsPopupWindow.OnClose
**Requires:**
- PlayerReturns_PopupWindowByName
**Snippet:**
```lua
require("PlayerReturns_PopupWindowByName")
local PlayerReturnsPopupWindow = {}
local uis, contentPane

function PlayerReturnsPopupWindow.ReInitData()
end

function PlayerReturnsPopupWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.PlayerReturnsPopupWindow.package, WinResConfig.PlayerReturnsPopupWindow.comName, function(com)
    contentPane = com
```

---

## MP/PlayerReturnsWindow.lua.lua
**Functions:**
- RefreshLoginRewardPanel
- panel.WordList.itemRenderer
- itemlist.itemRenderer
- RefreshSignRewardPanel
- itemlist.itemRenderer
- list.itemRenderer
- list.itemRenderer
- RefreshShopPanel
- rootlist.itemRenderer
- PlayerReturnsWindow.ReInitData
- PlayerReturnsWindow.OnInit
- PlayerReturnsWindow.UpdateInfo
- tablist.itemRenderer
- PlayerReturnsWindow.InitBtn
- PlayerReturnsWindow.OnClose
- PlayerReturnsWindow.HandleMessage
**Requires:**
- PlayerReturns_PlayerReturnsWindowByName
**Snippet:**
```lua
require("PlayerReturns_PlayerReturnsWindowByName")
local PlayerReturnsWindow = {}
local uis, contentPane, TAB_LOOKUP, RefreshLoginRewardPanel, RefreshSignRewardPanel, RefreshShopPanel

function RefreshLoginRewardPanel()
  RedDotMgr.UpdateNodeByWindowName(WinResConfig.PlayerReturnsWindow.name)
  local activInfo = ActivityReturnData.GetActivityInfo()
  local got = activInfo and activInfo.freeReward > 0
  local panel = uis.Main.LandReward
  local getBtn = panel.root:GetChild("Get")
```

---

## MP/PlayerReturns_LandRewardByName.lua.lua
**Functions:**
- GetPlayerReturns_LandRewardUis
**Snippet:**
```lua
function GetPlayerReturns_LandRewardUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerReturns_LandReward_GetBtnByName.lua.lua
**Functions:**
- GetPlayerReturns_LandReward_GetBtnUis
**Snippet:**
```lua
function GetPlayerReturns_LandReward_GetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerReturns_LandReward_WordByName.lua.lua
**Functions:**
- GetPlayerReturns_LandReward_WordUis
**Snippet:**
```lua
function GetPlayerReturns_LandReward_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerReturns_MultipleByName.lua.lua
**Functions:**
- GetPlayerReturns_MultipleUis
**Requires:**
- PlayerReturns_Multiple_NumberByName
**Snippet:**
```lua
require("PlayerReturns_Multiple_NumberByName")

function GetPlayerReturns_MultipleUis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.Number = GetPlayerReturns_Multiple_NumberUis(ui:GetChild("Number"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.GoBtn = ui:GetChild("GoBtn")
  uis.root = ui
  return uis
```

---

## MP/PlayerReturns_Multiple_GoBtnByName.lua.lua
**Functions:**
- GetPlayerReturns_Multiple_GoBtnUis
**Snippet:**
```lua
function GetPlayerReturns_Multiple_GoBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerReturns_Multiple_NumberByName.lua.lua
**Functions:**
- GetPlayerReturns_Multiple_NumberUis
**Snippet:**
```lua
function GetPlayerReturns_Multiple_NumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerReturns_PlayerReturnsByName.lua.lua
**Functions:**
- GetPlayerReturns_PlayerReturnsUis
**Requires:**
- CommonResource_BackGroundByName
- PlayerReturns_LandRewardByName
- PlayerReturns_SignRewardByName
- PlayerReturns_MultipleByName
- PlayerReturns_ShopByName
- PlayerReturns_TabRegionByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("PlayerReturns_LandRewardByName")
require("PlayerReturns_SignRewardByName")
require("PlayerReturns_MultipleByName")
require("PlayerReturns_ShopByName")
require("PlayerReturns_TabRegionByName")
require("CommonResource_CurrencyReturnByName")

function GetPlayerReturns_PlayerReturnsUis(ui)
  local uis = {}
```

---

## MP/PlayerReturns_PlayerReturnsWindowByName.lua.lua
**Functions:**
- GetPlayerReturns_PlayerReturnsWindowUis
**Requires:**
- PlayerReturns_PlayerReturnsByName
**Snippet:**
```lua
require("PlayerReturns_PlayerReturnsByName")

function GetPlayerReturns_PlayerReturnsWindowUis(ui)
  local uis = {}
  uis.Main = GetPlayerReturns_PlayerReturnsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/PlayerReturns_PopupByName.lua.lua
**Functions:**
- GetPlayerReturns_PopupUis
**Requires:**
- CommonResource_PopupBgByName
- PlayerReturns_Popup_TipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("PlayerReturns_Popup_TipsByName")

function GetPlayerReturns_PopupUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Tips = GetPlayerReturns_Popup_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
```

---

## MP/PlayerReturns_PopupWindowByName.lua.lua
**Functions:**
- GetPlayerReturns_PopupWindowUis
**Requires:**
- PlayerReturns_PopupByName
**Snippet:**
```lua
require("PlayerReturns_PopupByName")

function GetPlayerReturns_PopupWindowUis(ui)
  local uis = {}
  uis.Main = GetPlayerReturns_PopupUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/PlayerReturns_Popup_GoBtnByName.lua.lua
**Functions:**
- GetPlayerReturns_Popup_GoBtnUis
**Snippet:**
```lua
function GetPlayerReturns_Popup_GoBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerReturns_Popup_TipsByName.lua.lua
**Functions:**
- GetPlayerReturns_Popup_TipsUis
**Snippet:**
```lua
function GetPlayerReturns_Popup_TipsUis(ui)
  local uis = {}
  
  uis.GoBtn = ui:GetChild("GoBtn")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerReturns_Popup_WordByName.lua.lua
**Functions:**
- GetPlayerReturns_Popup_WordUis
**Snippet:**
```lua
function GetPlayerReturns_Popup_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerReturns_ShopByName.lua.lua
**Functions:**
- GetPlayerReturns_ShopUis
**Requires:**
- PlayerReturns_Shop_TokenRegionByName
**Snippet:**
```lua
require("PlayerReturns_Shop_TokenRegionByName")

function GetPlayerReturns_ShopUis(ui)
  local uis = {}
  uis.TokenRegion = GetPlayerReturns_Shop_TokenRegionUis(ui:GetChild("TokenRegion"))
  uis.ItemRegionList = ui:GetChild("ItemRegionList")
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerReturns_Shop_BuyBtnByName.lua.lua
**Functions:**
- GetPlayerReturns_Shop_BuyBtnUis
**Snippet:**
```lua
function GetPlayerReturns_Shop_BuyBtnUis(ui)
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

## MP/PlayerReturns_Shop_ItemByName.lua.lua
**Functions:**
- GetPlayerReturns_Shop_ItemUis
**Requires:**
- CommonResource_ItemFrameByName
- PlayerReturns_Shop_MoveWordByName
- PlayerReturns_Shop_SellOutByName
**Snippet:**
```lua
require("CommonResource_ItemFrameByName")
require("PlayerReturns_Shop_MoveWordByName")
require("PlayerReturns_Shop_SellOutByName")

function GetPlayerReturns_Shop_ItemUis(ui)
  local uis = {}
  uis.Item = GetCommonResource_ItemFrameUis(ui:GetChild("Item"))
  uis.MoveWord = GetPlayerReturns_Shop_MoveWordUis(ui:GetChild("MoveWord"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.BuyBtn = ui:GetChild("BuyBtn")
```

---

## MP/PlayerReturns_Shop_ItemLockByName.lua.lua
**Functions:**
- GetPlayerReturns_Shop_ItemLockUis
**Requires:**
- PlayerReturns_Shop_ItemLockWordByName
**Snippet:**
```lua
require("PlayerReturns_Shop_ItemLockWordByName")

function GetPlayerReturns_Shop_ItemLockUis(ui)
  local uis = {}
  uis.LockWord = GetPlayerReturns_Shop_ItemLockWordUis(ui:GetChild("LockWord"))
  uis.root = ui
  return uis
end
```

---

## MP/PlayerReturns_Shop_ItemLockWordByName.lua.lua
**Functions:**
- GetPlayerReturns_Shop_ItemLockWordUis
**Snippet:**
```lua
function GetPlayerReturns_Shop_ItemLockWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerReturns_Shop_ItemRegionByName.lua.lua
**Functions:**
- GetPlayerReturns_Shop_ItemRegionUis
**Requires:**
- PlayerReturns_Shop_ItemLockByName
**Snippet:**
```lua
require("PlayerReturns_Shop_ItemLockByName")

function GetPlayerReturns_Shop_ItemRegionUis(ui)
  local uis = {}
  uis.ItemList = ui:GetChild("ItemList")
  uis.ItemLock = GetPlayerReturns_Shop_ItemLockUis(ui:GetChild("ItemLock"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerReturns_Shop_MoveWordByName.lua.lua
**Functions:**
- GetPlayerReturns_Shop_MoveWordUis
**Snippet:**
```lua
function GetPlayerReturns_Shop_MoveWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerReturns_Shop_SellOutByName.lua.lua
**Functions:**
- GetPlayerReturns_Shop_SellOutUis
**Snippet:**
```lua
function GetPlayerReturns_Shop_SellOutUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerReturns_Shop_TokenGetBtnByName.lua.lua
**Functions:**
- GetPlayerReturns_Shop_TokenGetBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetPlayerReturns_Shop_TokenGetBtnUis(ui)
  local uis = {}
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerReturns_Shop_TokenProgressBarByName.lua.lua
**Functions:**
- GetPlayerReturns_Shop_TokenProgressBarUis
**Requires:**
- PlayerReturns_Shop_TokenProgressFillByName
**Snippet:**
```lua
require("PlayerReturns_Shop_TokenProgressFillByName")

function GetPlayerReturns_Shop_TokenProgressBarUis(ui)
  local uis = {}
  uis.bar = GetPlayerReturns_Shop_TokenProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## MP/PlayerReturns_Shop_TokenProgressFillByName.lua.lua
**Functions:**
- GetPlayerReturns_Shop_TokenProgressFillUis
**Snippet:**
```lua
function GetPlayerReturns_Shop_TokenProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## MP/PlayerReturns_Shop_TokenRegionByName.lua.lua
**Functions:**
- GetPlayerReturns_Shop_TokenRegionUis
**Snippet:**
```lua
function GetPlayerReturns_Shop_TokenRegionUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.TokenProgressBar = ui:GetChild("TokenProgressBar")
  uis.ProgressTxt = ui:GetChild("ProgressTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## MP/PlayerReturns_SignRewardByName.lua.lua
**Functions:**
- GetPlayerReturns_SignRewardUis
**Snippet:**
```lua
function GetPlayerReturns_SignRewardUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerReturns_SignReward_ItemByName.lua.lua
**Functions:**
- GetPlayerReturns_SignReward_ItemUis
**Requires:**
- CommonResource_ItemFrameByName
**Snippet:**
```lua
require("CommonResource_ItemFrameByName")

function GetPlayerReturns_SignReward_ItemUis(ui)
  local uis = {}
  uis.Item = GetCommonResource_ItemFrameUis(ui:GetChild("Item"))
  uis.DayTxt = ui:GetChild("DayTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## MP/PlayerReturns_TabBtnByName.lua.lua
**Functions:**
- GetPlayerReturns_TabBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetPlayerReturns_TabBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerReturns_TabRegionByName.lua.lua
**Functions:**
- GetPlayerReturns_TabRegionUis
**Requires:**
- PlayerReturns_TabTimeByName
**Snippet:**
```lua
require("PlayerReturns_TabTimeByName")

function GetPlayerReturns_TabRegionUis(ui)
  local uis = {}
  uis.TabTime = GetPlayerReturns_TabTimeUis(ui:GetChild("TabTime"))
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerReturns_TabTimeByName.lua.lua
**Functions:**
- GetPlayerReturns_TabTimeUis
**Snippet:**
```lua
function GetPlayerReturns_TabTimeUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlayerWindow.lua.lua
**Functions:**
- PlayerWindow.ReInitData
- PlayerWindow.OnInit
- PlayerWindow.UpdatePlayerInformation
- PlayerWindow.UpdateAccount
- PlayerWindow.UpdateResources
- right.MaterialList.itemRenderer
- right.MaterialList.itemRenderer
- PlayerWindow.UpdateResourceState
- PlayerWindow.UpdateCardList
- uis.Main.Left.CardNumber.HeadList.itemRenderer
- PlayerWindow.UpdateGuildInfo
- PlayerWindow.InitBtn
- PlayerWindow.OpenCodeWindow
- PlayerWindow.GetRenameCost
- PlayerWindow.TouchRenameBtn
- PlayerWindow.OnShown
- PlayerWindow.OnHide
- PlayerWindow.OnClose
- PlayerWindow.HandleMessage
**Requires:**
- PlayerInfo_PlayerWindowByName
**Snippet:**
```lua
require("PlayerInfo_PlayerWindowByName")
local PlayerWindow = {}
local uis, contentPane, playerInfo

function PlayerWindow.ReInitData()
end

function PlayerWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.PlayerWindow.package, WinResConfig.PlayerWindow.comName, function(com)
    contentPane = com
```

---

## MP/PlotDungeonWindow.lua.lua
**Functions:**
- PlotDungeonWindow.OnInit
- PlotDungeonWindow.LoadSpine
- PlotDungeonWindow.InitInfo
- PlotDungeonWindow.ShowChapterInfo
- PlotDungeonWindow.LoadChapterInfo
- PlotDungeonWindow.ShowStageInfo
- scrollPane.onScrollUpdateLua
- PlotDungeonWindow.StageItemClick
- PlotDungeonWindow.ItemOnClick
- PlotDungeonWindow.UpdateChapterPage
- PlotDungeonWindow.InitBtn
- PlotDungeonWindow.InitChapterReward
- PlotDungeonWindow.ChapterEndTips
- PlotDungeonWindow.OnShown
- PlotDungeonWindow.ChapterOpenTips
- PlotDungeonWindow.OnClose
- PlotDungeonWindow.HandleMessage
**Requires:**
- PlotDungeon_PlotDungeonWindowByName
**Snippet:**
```lua
require("PlotDungeon_PlotDungeonWindowByName")
local PlotDungeonWindow = {}
local uis, contentPane, currentSelectChapter, curChapterData, currentChapterIndex, jumpTb, playAnim
local pointPath = {
  "Assets/Art/Models/UI_spine/prefab/ui_adventure_point1.prefab",
  "Assets/Art/Models/UI_spine/prefab/ui_adventure_point2.prefab",
  "Assets/Art/Models/UI_spine/prefab/ui_adventure_point3.prefab"
}
local spinePoint

```

---

## MP/PlotDungeon_ChapterMap_01ByName.lua.lua
**Functions:**
- GetPlotDungeon_ChapterMap_01Uis
**Requires:**
- PlotDungeon_PlotInfoBtnAniByName
**Snippet:**
```lua
require("PlotDungeon_PlotInfoBtnAniByName")

function GetPlotDungeon_ChapterMap_01Uis(ui)
  local uis = {}
  uis.Q1 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q1"))
  uis.Q2 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q2"))
  uis.Q3 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q3"))
  uis.Q4 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q4"))
  uis.Q5 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q5"))
  uis.Q6 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q6"))
```

---

## MP/PlotDungeon_ChapterMap_02ByName.lua.lua
**Functions:**
- GetPlotDungeon_ChapterMap_02Uis
**Requires:**
- PlotDungeon_PlotInfoBtnAniByName
**Snippet:**
```lua
require("PlotDungeon_PlotInfoBtnAniByName")

function GetPlotDungeon_ChapterMap_02Uis(ui)
  local uis = {}
  uis.Q1 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q1"))
  uis.Q2 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q2"))
  uis.Q3 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q3"))
  uis.Q4 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q4"))
  uis.Q5 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q5"))
  uis.Q6 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q6"))
```

---

## MP/PlotDungeon_ChapterMap_03ByName.lua.lua
**Functions:**
- GetPlotDungeon_ChapterMap_03Uis
**Requires:**
- PlotDungeon_PlotInfoBtnAniByName
**Snippet:**
```lua
require("PlotDungeon_PlotInfoBtnAniByName")

function GetPlotDungeon_ChapterMap_03Uis(ui)
  local uis = {}
  uis.Q1 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q1"))
  uis.Q2 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q2"))
  uis.Q3 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q3"))
  uis.Q4 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q4"))
  uis.Q5 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q5"))
  uis.Q6 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q6"))
```

---

## MP/PlotDungeon_ChapterMap_04ByName.lua.lua
**Functions:**
- GetPlotDungeon_ChapterMap_04Uis
**Requires:**
- PlotDungeon_PlotInfoBtnAniByName
**Snippet:**
```lua
require("PlotDungeon_PlotInfoBtnAniByName")

function GetPlotDungeon_ChapterMap_04Uis(ui)
  local uis = {}
  uis.Q1 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q1"))
  uis.Q2 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q2"))
  uis.Q3 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q3"))
  uis.Q4 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q4"))
  uis.Q5 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q5"))
  uis.Q6 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q6"))
```

---

## MP/PlotDungeon_ChapterMap_05ByName.lua.lua
**Functions:**
- GetPlotDungeon_ChapterMap_05Uis
**Requires:**
- PlotDungeon_PlotInfoBtnAniByName
**Snippet:**
```lua
require("PlotDungeon_PlotInfoBtnAniByName")

function GetPlotDungeon_ChapterMap_05Uis(ui)
  local uis = {}
  uis.Q1 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q1"))
  uis.Q2 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q2"))
  uis.Q3 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q3"))
  uis.Q4 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q4"))
  uis.Q5 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q5"))
  uis.Q6 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q6"))
```

---

## MP/PlotDungeon_ChapterMap_06ByName.lua.lua
**Functions:**
- GetPlotDungeon_ChapterMap_06Uis
**Requires:**
- PlotDungeon_PlotInfoBtnAniByName
**Snippet:**
```lua
require("PlotDungeon_PlotInfoBtnAniByName")

function GetPlotDungeon_ChapterMap_06Uis(ui)
  local uis = {}
  uis.Q1 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q1"))
  uis.Q2 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q2"))
  uis.Q3 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q3"))
  uis.Q4 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q4"))
  uis.Q5 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q5"))
  uis.Q6 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q6"))
```

---

## MP/PlotDungeon_ChapterMap_07ByName.lua.lua
**Functions:**
- GetPlotDungeon_ChapterMap_07Uis
**Requires:**
- PlotDungeon_PlotInfoBtnAniByName
**Snippet:**
```lua
require("PlotDungeon_PlotInfoBtnAniByName")

function GetPlotDungeon_ChapterMap_07Uis(ui)
  local uis = {}
  uis.Q1 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q1"))
  uis.Q2 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q2"))
  uis.Q3 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q3"))
  uis.Q4 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q4"))
  uis.Q5 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q5"))
  uis.Q6 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q6"))
```

---

## MP/PlotDungeon_ChapterMap_08ByName.lua.lua
**Functions:**
- GetPlotDungeon_ChapterMap_08Uis
**Requires:**
- PlotDungeon_PlotInfoBtnAniByName
**Snippet:**
```lua
require("PlotDungeon_PlotInfoBtnAniByName")

function GetPlotDungeon_ChapterMap_08Uis(ui)
  local uis = {}
  uis.Q1 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q1"))
  uis.Q2 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q2"))
  uis.Q3 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q3"))
  uis.Q4 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q4"))
  uis.Q5 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q5"))
  uis.Q6 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q6"))
```

---

## MP/PlotDungeon_ChapterMap_09ByName.lua.lua
**Functions:**
- GetPlotDungeon_ChapterMap_09Uis
**Requires:**
- PlotDungeon_PlotInfoBtnAniByName
**Snippet:**
```lua
require("PlotDungeon_PlotInfoBtnAniByName")

function GetPlotDungeon_ChapterMap_09Uis(ui)
  local uis = {}
  uis.Q1 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q1"))
  uis.Q2 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q2"))
  uis.Q3 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q3"))
  uis.Q4 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q4"))
  uis.Q5 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q5"))
  uis.Q6 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q6"))
```

---

## MP/PlotDungeon_ChapterMap_10ByName.lua.lua
**Functions:**
- GetPlotDungeon_ChapterMap_10Uis
**Requires:**
- PlotDungeon_PlotInfoBtnAniByName
**Snippet:**
```lua
require("PlotDungeon_PlotInfoBtnAniByName")

function GetPlotDungeon_ChapterMap_10Uis(ui)
  local uis = {}
  uis.Q1 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q1"))
  uis.Q2 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q2"))
  uis.Q3 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q3"))
  uis.Q4 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q4"))
  uis.Q5 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q5"))
  uis.Q6 = GetPlotDungeon_PlotInfoBtnAniUis(ui:GetChild("Q6"))
```

---

## MP/PlotDungeon_ChapterRewardBtnByName.lua.lua
**Functions:**
- GetPlotDungeon_ChapterRewardBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetPlotDungeon_ChapterRewardBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlotDungeon_DungeonMapByName.lua.lua
**Functions:**
- GetPlotDungeon_DungeonMapUis
**Snippet:**
```lua
function GetPlotDungeon_DungeonMapUis(ui)
  local uis = {}
  
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.MapList = ui:GetChild("MapList")
  uis.root = ui
  return uis
end
```

---

## MP/PlotDungeon_EffectHolderByName.lua.lua
**Functions:**
- GetPlotDungeon_EffectHolderUis
**Snippet:**
```lua
function GetPlotDungeon_EffectHolderUis(ui)
  local uis = {}
  
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## MP/PlotDungeon_LeftBtnByName.lua.lua
**Functions:**
- GetPlotDungeon_LeftBtnUis
**Snippet:**
```lua
function GetPlotDungeon_LeftBtnUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlotDungeon_OpenSceneByName.lua.lua
**Functions:**
- GetPlotDungeon_OpenSceneUis
**Requires:**
- CommonResource_BackGroundByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")

function GetPlotDungeon_OpenSceneUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
```

---

## MP/PlotDungeon_OpenSceneWindowByName.lua.lua
**Functions:**
- GetPlotDungeon_OpenSceneWindowUis
**Requires:**
- PlotDungeon_OpenSceneByName
**Snippet:**
```lua
require("PlotDungeon_OpenSceneByName")

function GetPlotDungeon_OpenSceneWindowUis(ui)
  local uis = {}
  uis.Main = GetPlotDungeon_OpenSceneUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/PlotDungeon_OpenTitleByName.lua.lua
**Functions:**
- GetPlotDungeon_OpenTitleUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetPlotDungeon_OpenTitleUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.EffectBgHolder = ui:GetChild("EffectBgHolder")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
```

---

## MP/PlotDungeon_OpenTitleWindowByName.lua.lua
**Functions:**
- GetPlotDungeon_OpenTitleWindowUis
**Requires:**
- PlotDungeon_OpenTitleByName
**Snippet:**
```lua
require("PlotDungeon_OpenTitleByName")

function GetPlotDungeon_OpenTitleWindowUis(ui)
  local uis = {}
  uis.Main = GetPlotDungeon_OpenTitleUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/PlotDungeon_PlotBtnByName.lua.lua
**Functions:**
- GetPlotDungeon_PlotBtnUis
**Snippet:**
```lua
function GetPlotDungeon_PlotBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlotDungeon_PlotDungeonByName.lua.lua
**Functions:**
- GetPlotDungeon_PlotDungeonUis
**Requires:**
- CommonResource_BackGroundByName
- PlotDungeon_DungeonMapByName
- PlotDungeon_TitleByName
- PlotDungeon_RightRegionByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("PlotDungeon_DungeonMapByName")
require("PlotDungeon_TitleByName")
require("PlotDungeon_RightRegionByName")
require("CommonResource_CurrencyReturnByName")

function GetPlotDungeon_PlotDungeonUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.DungeonMap = GetPlotDungeon_DungeonMapUis(ui:GetChild("DungeonMap"))
```

---

## MP/PlotDungeon_PlotDungeonWindowByName.lua.lua
**Functions:**
- GetPlotDungeon_PlotDungeonWindowUis
**Requires:**
- PlotDungeon_PlotDungeonByName
**Snippet:**
```lua
require("PlotDungeon_PlotDungeonByName")

function GetPlotDungeon_PlotDungeonWindowUis(ui)
  local uis = {}
  uis.Main = GetPlotDungeon_PlotDungeonUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/PlotDungeon_PlotInfoBtnAniByName.lua.lua
**Functions:**
- GetPlotDungeon_PlotInfoBtnAniUis
**Requires:**
- PlotDungeon_EffectHolderByName
**Snippet:**
```lua
require("PlotDungeon_EffectHolderByName")

function GetPlotDungeon_PlotInfoBtnAniUis(ui)
  local uis = {}
  uis.EffectHolder = GetPlotDungeon_EffectHolderUis(ui:GetChild("EffectHolder"))
  uis.PlotInfoBtn = ui:GetChild("PlotInfoBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## MP/PlotDungeon_PlotInfoBtnByName.lua.lua
**Functions:**
- GetPlotDungeon_PlotInfoBtnUis
**Snippet:**
```lua
function GetPlotDungeon_PlotInfoBtnUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
```

---

## MP/PlotDungeon_PlotRewardByName.lua.lua
**Functions:**
- GetPlotDungeon_PlotRewardUis
**Requires:**
- CommonResource_PopupBgByName
- PlotDungeon_PlotRewardTipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("PlotDungeon_PlotRewardTipsByName")

function GetPlotDungeon_PlotRewardUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.PlotRewardTips = GetPlotDungeon_PlotRewardTipsUis(ui:GetChild("PlotRewardTips"))
  uis.root = ui
  return uis
```

---

## MP/PlotDungeon_PlotRewardCompleteByName.lua.lua
**Functions:**
- GetPlotDungeon_PlotRewardCompleteUis
**Snippet:**
```lua
function GetPlotDungeon_PlotRewardCompleteUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlotDungeon_PlotRewardLockByName.lua.lua
**Functions:**
- GetPlotDungeon_PlotRewardLockUis
**Snippet:**
```lua
function GetPlotDungeon_PlotRewardLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlotDungeon_PlotRewardTipsByName.lua.lua
**Functions:**
- GetPlotDungeon_PlotRewardTipsUis
**Requires:**
- PlotDungeon_PlotRewardLockByName
- PlotDungeon_PlotRewardCompleteByName
**Snippet:**
```lua
require("PlotDungeon_PlotRewardLockByName")
require("PlotDungeon_PlotRewardCompleteByName")

function GetPlotDungeon_PlotRewardTipsUis(ui)
  local uis = {}
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.RewardTxt = ui:GetChild("RewardTxt")
  uis.ItemList = ui:GetChild("ItemList")
```

---

## MP/PlotDungeon_PlotRewardWindowByName.lua.lua
**Functions:**
- GetPlotDungeon_PlotRewardWindowUis
**Requires:**
- PlotDungeon_PlotRewardByName
**Snippet:**
```lua
require("PlotDungeon_PlotRewardByName")

function GetPlotDungeon_PlotRewardWindowUis(ui)
  local uis = {}
  uis.Main = GetPlotDungeon_PlotRewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/PlotDungeon_RewardBtnByName.lua.lua
**Functions:**
- GetPlotDungeon_RewardBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetPlotDungeon_RewardBtnUis(ui)
  local uis = {}
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlotDungeon_RightBtnByName.lua.lua
**Functions:**
- GetPlotDungeon_RightBtnUis
**Snippet:**
```lua
function GetPlotDungeon_RightBtnUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## MP/PlotDungeon_RightRegionByName.lua.lua
**Functions:**
- GetPlotDungeon_RightRegionUis
**Snippet:**
```lua
function GetPlotDungeon_RightRegionUis(ui)
  local uis = {}
  
  uis.RightBtn = ui:GetChild("RightBtn")
  uis.RightUnknownBtn = ui:GetChild("RightUnknownBtn")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/PlotDungeon_RightUnknownBtnByName.lua.lua
**Functions:**
- GetPlotDungeon_RightUnknownBtnUis
**Snippet:**
```lua
function GetPlotDungeon_RightUnknownBtnUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlotDungeon_TitleByName.lua.lua
**Functions:**
- GetPlotDungeon_TitleUis
**Snippet:**
```lua
function GetPlotDungeon_TitleUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlotItemGetWindow.lua.lua
**Functions:**
- PlotItemGetWindow.ReInitData
- PlotItemGetWindow.OnInit
- PlotItemGetWindow.OnShowAnimationEnd
- PlotItemGetWindow.UpdateInfo
- PlotItemGetWindow.PlayNextItem
- PlotItemGetWindow.InitBtn
- PlotItemGetWindow.OnShown
- PlotItemGetWindow.OnHide
- PlotItemGetWindow.OnClose
- PlotItemGetWindow.HandleMessage
**Requires:**
- PlotPlay_PlotItemGetByName
**Snippet:**
```lua
require("PlotPlay_PlotItemGetByName")
local PlotItemGetWindow = {}
local uis, contentPane, items, curIndex, canTouch

function PlotItemGetWindow.ReInitData()
end

function PlotItemGetWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.PlotItemGetWindow.package, WinResConfig.PlotItemGetWindow.comName, function(com)
    contentPane = com
```

---

## MP/PlotPlayBattleScriptList.lua.lua
**Requires:**
- PlotPlayBattle_1
- PlotPlayBattle_2
**Snippet:**
```lua
local require = require
require("PlotPlayBattle_1")
require("PlotPlayBattle_2")
```

---

## MP/PlotPlayBattle_1.lua.lua
**Functions:**
- PlotBattle.SpeakFunc
- PlotBattle.Start
- PlotBattle.Close
- PlotBattle.PlotBattleUpdate
**Snippet:**
```lua
BattleData.InitBattleData = {
  id = 1,
  uid = 1,
  mapId = 10001,
  randomSeeds = {10000},
  actorLeft = {
    uid = 1,
    badge = {},
    unitList = {
      {
```

---

## MP/PlotPlayBattle_2.lua.lua
**Functions:**
- PlotBattle.SpeakFunc
- PlotBattle.Start
- PlotBattle.Close
- PlotBattle.PlotBattleUpdate
**Snippet:**
```lua
BattleData.InitBattleData = {
  id = 2,
  uid = 2,
  mapId = 10001,
  randomSeeds = {10000},
  actorLeft = {
    uid = 1,
    badge = {
      id = 21110100,
      level = 4,
```

---

## MP/PlotPlayData.lua.lua
**Functions:**
- PlotPlayData.InitData
- PlotPlayData.SetCurPartId
- PlotPlayData.GetCurPartId
- PlotPlayData.SetCurSectionId
- PlotPlayData.GetCurSectionId
- PlotPlayData.SetCurDialogId
- PlotPlayData.GetCurDialogId
- PlotPlayData.SetIsAuto
- PlotPlayData.GetIsAuto
- PlotPlayData.SetPartEndCallback
- PlotPlayData.GetPartEndCallback
- PlotPlayData.SetCurPartState
- PlotPlayData.GetCurPartState
- PlotPlayData.SetFixedPartIds
- PlotPlayData.GetFixedPartIds
- PlotPlayData.GetNextDialogId
- PlotPlayData.GetNextSectionId
- PlotPlayData.GetDialogs
- PlotPlayData.GetDialogsInSection
- PlotPlayData.GetFirstDialogInPart
- PlotPlayData.GetFirstDialogInSection
- PlotPlayData.GetStartPosition
- PlotPlayData.GetEndPosition
- PlotPlayData.ClearData
- PlotPlayData.IsPlotFinished
- PlotPlayData.UpdateFinishedPlot
- PlotPlayData.InsertFinishedPlot
- PlotPlayData.GetCurPartRewardDialogs
- PlotPlayData.GetSoundPath
**Snippet:**
```lua
PlotPlayData = {
  finishedPlotList = {},
  isAutoPlay = false,
  autoPlayWaitTime = 0.5
}
local curPartId, curSectionId, curDialogId
local isAuto = false
local partEndCallback = false
local curPartState, fixedPartIds
PLOT_PLAY_STATE = {
```

---

## MP/PlotPlayEditorData.lua.lua
**Functions:**
- PlotPlayEditorData.LoadCSV
- PlotPlayEditorData.TableToCsv
- PlotPlayEditorData.SaveCSV
- PlotPlayEditorData.GetPlotInit
- PlotPlayEditorData.GetCurPartDataList
- PlotPlayEditorData.GetPartData
- PlotPlayEditorData.GetCurSectionIds
- PlotPlayEditorData.GetSectionDataList
- PlotPlayEditorData.GetSectionData
- PlotPlayEditorData.GetCurDialogIds
- PlotPlayEditorData.GetDialogDataList
- PlotPlayEditorData.GetDialogData
- PlotPlayEditorData.GetWord
- PlotPlayEditorData.GetPartSkipTipsId
- PlotPlayEditorData.GetPartStartTitleId
- PlotPlayEditorData.GetPartStartSubtitleId
- PlotPlayEditorData.GetPartStartNameTitleId
- PlotPlayEditorData.GetPartStartNameSubtitleId
- PlotPlayEditorData.GetPartEndTitleId
- PlotPlayEditorData.GetPartEndSubtitleId
- PlotPlayEditorData.GetPartEndNameTitleId
- PlotPlayEditorData.GetPartEndNameSubtitleId
- PlotPlayEditorData.GetTalkWordId
- PlotPlayEditorData.GetExplainWordId
- PlotPlayEditorData.GetNarratorWordId
- PlotPlayEditorData.GetMiddleWordId
- PlotPlayEditorData.GetOptionWordId
- PlotPlayEditorData.GetSpeakNameWordId
- PlotPlayEditorData.GetExplainNameWordId
- PlotPlayEditorData.GetCGWordId
- PlotPlayEditorData.GetOpenTitle1WordId
- PlotPlayEditorData.GetOpenTitle2WordId
- PlotPlayEditorData.AddOrUpdatePart
- PlotPlayEditorData.DeletePart
- PlotPlayEditorData.AddOrUpdateSection
- PlotPlayEditorData.DeleteSection
- PlotPlayEditorData.GetAvailableSectionId
- PlotPlayEditorData.AddOrUpdateDialog
- PlotPlayEditorData.DeleteDialog
- PlotPlayEditorData.GetAvailableDialogId
- PlotPlayEditorData.AddOrUpdateWord
- PlotPlayEditorData.DeleteWord
- PlotPlayEditorData.GetLocalBg
- PlotPlayEditorData.GetLocalCard
**Snippet:**
```lua
PlotPlayEditorData = {}
local partKeyList = {}
local partTypeList = {}
local partDesList = {}
local sectionKeyList = {}
local sectionTypeList = {}
local sectionDesList = {}
local dialogKeyList = {}
local dialogTypeList = {}
local dialogDesList = {}
```

---

## MP/PlotPlayEditorMgr.lua.lua
**Functions:**
- PlotPlayEditorMgr.SaveFile
- PlotPlayEditorMgr.ShowError
**Snippet:**
```lua
PlotPlayEditorMgr = {}

function PlotPlayEditorMgr.SaveFile()
  PlotPlayEditorData.SaveCSV()
end

function PlotPlayEditorMgr.ShowError(title, content)
  CS.UnityEditor.EditorUtility.DisplayDialog(title, content, "确认")
end
```

---

## MP/PlotPlayEditorScriptList.lua.lua
**Requires:**
- PlotPlayEditorMgr
- PlotPlayEditorData
- PlotPlayEditorStruct
**Snippet:**
```lua
local require = require
require("PlotPlayEditorMgr")
require("PlotPlayEditorData")
require("PlotPlayEditorStruct")
```

---

## MP/PlotPlayEditorStruct.lua.lua
**Functions:**
- GetPartStruct
- GetSectionStruct
- GetDialogStruct
**Snippet:**
```lua
function GetPartStruct(param)
  return {
    id = param.id or "",
    
    next_part = param.next_part or "",
    section_ids = param.section_ids or "",
    title = param.title or "",
    skip_tips = param.skip_tips or "",
    use_static = param.use_static or ""
  }
```

---

## MP/PlotPlayEditorWindow.lua.lua
**Functions:**
- PlotPlayEditorWindow.ReInitData
- PlotPlayEditorWindow.OnInit
- PlotPlayEditorWindow.UpdateInfo
- PlotPlayEditorWindow.UpdatePartList
- PlotPlayEditorWindow.UpdateSectionList
- PlotPlayEditorWindow.UpdateDialogList
- PlotPlayEditorWindow.RenderPart
- PlotPlayEditorWindow.RenderSection
- PlotPlayEditorWindow.RenderDialog
- PlotPlayEditorWindow.PopPartEdit
- PlotPlayEditorWindow.ClosePartEdit
- PlotPlayEditorWindow.PopSectionEdit
- PlotPlayEditorWindow.CloseSectionEdit
- PlotPlayEditorWindow.UpdateSelectList
- PlotPlayEditorWindow.ShowBgList
- PlotPlayEditorWindow.CreateBgInList
- PlotPlayEditorWindow.CreateCardInList
- PlotPlayEditorWindow.CreateHeadInList
- PlotPlayEditorWindow.ClearSelectBtn
- PlotPlayEditorWindow.InitBtn
- PlotPlayEditorWindow.InitDialogEdit
- PlotPlayEditorWindow.UpdateDialogEdit
- PlotPlayEditorWindow.UpdateDialogHead
- PlotPlayEditorWindow.UpdateDialogCard
- PlotPlayEditorWindow.ShowPopAction
- PlotPlayEditorWindow.UpdateDialogText
- PlotPlayEditorWindow.UpdateDialogEffect
- PlotPlayEditorWindow.UpdateDialogAnimation
- PlotPlayEditorWindow.UpdateDialogCG
- PlotPlayEditorWindow.UpdateDialogOpen
- PlotPlayEditorWindow.UpdateEditComp
- PlotPlayEditorWindow.UpdatePlotPlay
- PlotPlayEditorWindow.DisplayDialog
- PlotPlayEditorWindow.OnShown
- PlotPlayEditorWindow.OnHide
- PlotPlayEditorWindow.OnClose
- PlotPlayEditorWindow.HandleMessage
**Requires:**
- PlotPlayEditor_PlotPlayEditorWindowByName
- PlotPlayEditor_ChapterEditByName
- PlotPlayEditor_CardByName
- PlotPlay_PlotPlayWindowByName
**Snippet:**
```lua
require("PlotPlayEditor_PlotPlayEditorWindowByName")
local SELECT_RES_TYPE = {
  BACKGROUND = 1,
  CARD = 2,
  HEAD = 3
}
local PlotPlayEditorWindow = {}
local uis, contentPane, selectPartId, selectSectionId, selectDialogId
local tempParts = {}
local tempSections = {}
```

---

## MP/PlotPlayEditor_CardBlinkByName.lua.lua
**Functions:**
- GetPlotPlayEditor_CardBlinkUis
**Snippet:**
```lua
function GetPlotPlayEditor_CardBlinkUis(ui)
  local uis = {}
  
  uis.BlinkEditBtn = ui:GetChild("BlinkEditBtn")
  uis.BlinkTemplateList = ui:GetChild("BlinkTemplateList")
  uis.BlinkAddBtn = ui:GetChild("BlinkAddBtn")
  uis.BlinkDelBtn = ui:GetChild("BlinkDelBtn")
  uis.BlinkSaveBtn = ui:GetChild("BlinkSaveBtn")
  uis.BlinkJumpBtn = ui:GetChild("BlinkJumpBtn")
  uis.root = ui
```

---

## MP/PlotPlayEditor_CardByName.lua.lua
**Functions:**
- GetPlotPlayEditor_CardUis
**Requires:**
- PlotPlayEditor_CardSkinByName
- PlotPlayEditor_CardTimelineByName
- PlotPlayEditor_CardBlinkByName
- PlotPlayEditor_CardScaleAndPositionByName
- PlotPlayEditor_CardEffectByName
- PlotPlayEditor_CardSpeakByName
- PlotPlayEditor_ShakeByName
**Snippet:**
```lua
require("PlotPlayEditor_CardSkinByName")
require("PlotPlayEditor_CardTimelineByName")
require("PlotPlayEditor_CardBlinkByName")
require("PlotPlayEditor_CardScaleAndPositionByName")
require("PlotPlayEditor_CardEffectByName")
require("PlotPlayEditor_CardSpeakByName")
require("PlotPlayEditor_ShakeByName")

function GetPlotPlayEditor_CardUis(ui)
  local uis = {}
```

---

## MP/PlotPlayEditor_CardEffectByName.lua.lua
**Functions:**
- GetPlotPlayEditor_CardEffectUis
**Snippet:**
```lua
function GetPlotPlayEditor_CardEffectUis(ui)
  local uis = {}
  
  uis.EffectInCBox = ui:GetChild("EffectInCBox")
  uis.EffectOutCBox = ui:GetChild("EffectOutCBox")
  uis.CardEffectCBox = ui:GetChild("CardEffectCBox")
  uis.InParamTxt = ui:GetChild("InParamTxt")
  uis.OutParamTxt = ui:GetChild("OutParamTxt")
  uis.root = ui
  return uis
```

---

## MP/PlotPlayEditor_CardScaleAndPositionByName.lua.lua
**Functions:**
- GetPlotPlayEditor_CardScaleAndPositionUis
**Snippet:**
```lua
function GetPlotPlayEditor_CardScaleAndPositionUis(ui)
  local uis = {}
  
  uis.PosXTxt = ui:GetChild("PosXTxt")
  uis.PosYTxt = ui:GetChild("PosYTxt")
  uis.ScaleTxt = ui:GetChild("ScaleTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlayEditor_CardSkinByName.lua.lua
**Functions:**
- GetPlotPlayEditor_CardSkinUis
**Snippet:**
```lua
function GetPlotPlayEditor_CardSkinUis(ui)
  local uis = {}
  
  uis.SkinList = ui:GetChild("SkinList")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlayEditor_CardSpeakByName.lua.lua
**Functions:**
- GetPlotPlayEditor_CardSpeakUis
**Snippet:**
```lua
function GetPlotPlayEditor_CardSpeakUis(ui)
  local uis = {}
  
  uis.IsSpeakerBtn = ui:GetChild("IsSpeakerBtn")
  uis.IsLightBtn = ui:GetChild("IsLightBtn")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlayEditor_CardTimelineByName.lua.lua
**Functions:**
- GetPlotPlayEditor_CardTimelineUis
**Snippet:**
```lua
function GetPlotPlayEditor_CardTimelineUis(ui)
  local uis = {}
  
  uis.CreateBtn = ui:GetChild("CreateBtn")
  uis.LookBtn = ui:GetChild("LookBtn")
  uis.PathTxt = ui:GetChild("PathTxt")
  uis.DelBtn = ui:GetChild("DelBtn")
  uis.AddBtn = ui:GetChild("AddBtn")
  uis.SaveBtn = ui:GetChild("SaveBtn")
  uis.EditTemplateBtn = ui:GetChild("EditTemplateBtn")
```

---

## MP/PlotPlayEditor_ChapterEditByName.lua.lua
**Functions:**
- GetPlotPlayEditor_ChapterEditUis
**Snippet:**
```lua
function GetPlotPlayEditor_ChapterEditUis(ui)
  local uis = {}
  
  uis.IdInputTxt = ui:GetChild("IdInputTxt")
  uis.RefreshBtn = ui:GetChild("RefreshBtn")
  uis.DelBtn = ui:GetChild("DelBtn")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.LeftBtn = ui:GetChild("LeftBtn")
  uis.RightBtn = ui:GetChild("RightBtn")
```

---

## MP/PlotPlayEditor_ClickButtonByName.lua.lua
**Functions:**
- GetPlotPlayEditor_ClickButtonUis
**Snippet:**
```lua
function GetPlotPlayEditor_ClickButtonUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlayEditor_ComboBoxFileByName.lua.lua
**Functions:**
- GetPlotPlayEditor_ComboBoxFileUis
**Snippet:**
```lua
function GetPlotPlayEditor_ComboBoxFileUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlayEditor_ComboBoxFile_itemByName.lua.lua
**Functions:**
- GetPlotPlayEditor_ComboBoxFile_itemUis
**Snippet:**
```lua
function GetPlotPlayEditor_ComboBoxFile_itemUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlayEditor_ComboBoxFile_popupByName.lua.lua
**Functions:**
- GetPlotPlayEditor_ComboBoxFile_popupUis
**Snippet:**
```lua
function GetPlotPlayEditor_ComboBoxFile_popupUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlayEditor_DialogAnimationByName.lua.lua
**Functions:**
- GetPlotPlayEditor_DialogAnimationUis
**Snippet:**
```lua
function GetPlotPlayEditor_DialogAnimationUis(ui)
  local uis = {}
  
  uis.AnimationUrlTxt = ui:GetChild("AnimationUrlTxt")
  uis.BattleScriptTxt = ui:GetChild("BattleScriptTxt")
  uis.TextSoundTxt = ui:GetChild("TextSoundTxt")
  uis.EnvSoundTxt = ui:GetChild("EnvSoundTxt")
  uis.SpecialSoundTxt = ui:GetChild("SpecialSoundTxt")
  uis.DelayTimeTxt = ui:GetChild("DelayTimeTxt")
  uis.root = ui
```

---

## MP/PlotPlayEditor_DialogBtnByName.lua.lua
**Functions:**
- GetPlotPlayEditor_DialogBtnUis
**Snippet:**
```lua
function GetPlotPlayEditor_DialogBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.AddBtn = ui:GetChild("AddBtn")
  uis.IdTxt = ui:GetChild("IdTxt")
  uis.IndexCBox = ui:GetChild("IndexCBox")
  uis.NextCBox = ui:GetChild("NextCBox")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
```

---

## MP/PlotPlayEditor_DialogCardByName.lua.lua
**Functions:**
- GetPlotPlayEditor_DialogCardUis
**Snippet:**
```lua
function GetPlotPlayEditor_DialogCardUis(ui)
  local uis = {}
  
  uis.CardList = ui:GetChild("CardList")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlayEditor_DialogCGByName.lua.lua
**Functions:**
- GetPlotPlayEditor_DialogCGUis
**Snippet:**
```lua
function GetPlotPlayEditor_DialogCGUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.XTxt = ui:GetChild("XTxt")
  uis.YTxt = ui:GetChild("YTxt")
  uis.ScaleTxt = ui:GetChild("ScaleTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlayEditor_DialogCompByName.lua.lua
**Functions:**
- GetPlotPlayEditor_DialogCompUis
**Snippet:**
```lua
function GetPlotPlayEditor_DialogCompUis(ui)
  local uis = {}
  
  uis.DialogList = ui:GetChild("DialogList")
  uis.AddDialogBtn = ui:GetChild("AddDialogBtn")
  uis.DelDialogBtn = ui:GetChild("DelDialogBtn")
  uis.CopyDialogBtn = ui:GetChild("CopyDialogBtn")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlayEditor_DialogEditByName.lua.lua
**Functions:**
- GetPlotPlayEditor_DialogEditUis
**Requires:**
- PlotPlayEditor_DialogCardByName
- PlotPlayEditor_DialogEffectByName
- PlotPlayEditor_DialogTextByName
- PlotPlayEditor_HeadByName
- PlotPlayEditor_DialogAnimationByName
- PlotPlayEditor_DialogCGByName
- PlotPlayEditor_DialogOpenByName
**Snippet:**
```lua
require("PlotPlayEditor_DialogCardByName")
require("PlotPlayEditor_DialogEffectByName")
require("PlotPlayEditor_DialogTextByName")
require("PlotPlayEditor_HeadByName")
require("PlotPlayEditor_DialogAnimationByName")
require("PlotPlayEditor_DialogCGByName")
require("PlotPlayEditor_DialogOpenByName")

function GetPlotPlayEditor_DialogEditUis(ui)
  local uis = {}
```

---

## MP/PlotPlayEditor_DialogEffectByName.lua.lua
**Functions:**
- GetPlotPlayEditor_DialogEffectUis
**Snippet:**
```lua
function GetPlotPlayEditor_DialogEffectUis(ui)
  local uis = {}
  
  uis.CameraMoveCBox = ui:GetChild("CameraMoveCBox")
  uis.CameraScaleCBox = ui:GetChild("CameraScaleCBox")
  uis.CameraMoveDelayTxt = ui:GetChild("CameraMoveDelayTxt")
  uis.CameraScaleDelayTxt = ui:GetChild("CameraScaleDelayTxt")
  uis.CameraShakeCBox = ui:GetChild("CameraShakeCBox")
  uis.CameraShakeDelayTxt = ui:GetChild("CameraShakeDelayTxt")
  uis.CameraMoveStartTxt = ui:GetChild("CameraMoveStartTxt")
```

---

## MP/PlotPlayEditor_DialogOpenByName.lua.lua
**Functions:**
- GetPlotPlayEditor_DialogOpenUis
**Snippet:**
```lua
function GetPlotPlayEditor_DialogOpenUis(ui)
  local uis = {}
  
  uis.Title1Txt = ui:GetChild("Title1Txt")
  uis.Title2Txt = ui:GetChild("Title2Txt")
  uis.ChooseBtn = ui:GetChild("ChooseBtn")
  uis.ClearBtn = ui:GetChild("ClearBtn")
  uis.BgHolder = ui:GetChild("BgHolder")
  uis.BgLoader = ui:GetChild("BgLoader")
  uis.BgMoveCBox = ui:GetChild("BgMoveCBox")
```

---

## MP/PlotPlayEditor_DialogTextByName.lua.lua
**Functions:**
- GetPlotPlayEditor_DialogTextUis
**Requires:**
- PlotPlayEditor_OptionByName
**Snippet:**
```lua
require("PlotPlayEditor_OptionByName")

function GetPlotPlayEditor_DialogTextUis(ui)
  local uis = {}
  uis.TalkWordTxt = ui:GetChild("TalkWordTxt")
  uis.ExplainWordNameTxt = ui:GetChild("ExplainWordNameTxt")
  uis.ExplainWordTxt = ui:GetChild("ExplainWordTxt")
  uis.NarratorWordTxt = ui:GetChild("NarratorWordTxt")
  uis.MiddleWordTxt = ui:GetChild("MiddleWordTxt")
  uis.Option1 = GetPlotPlayEditor_OptionUis(ui:GetChild("Option1"))
```

---

## MP/PlotPlayEditor_EditCompByName.lua.lua
**Functions:**
- GetPlotPlayEditor_EditCompUis
**Snippet:**
```lua
function GetPlotPlayEditor_EditCompUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlayEditor_HeadByName.lua.lua
**Functions:**
- GetPlotPlayEditor_HeadUis
**Snippet:**
```lua
function GetPlotPlayEditor_HeadUis(ui)
  local uis = {}
  
  uis.HeadHolder = ui:GetChild("HeadHolder")
  uis.ChooseHeadBtn = ui:GetChild("ChooseHeadBtn")
  uis.ActionList = ui:GetChild("ActionList")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.ReviewHeadTxt = ui:GetChild("ReviewHeadTxt")
  uis.ClearBtn = ui:GetChild("ClearBtn")
  uis.SaveBtn = ui:GetChild("SaveBtn")
```

---

## MP/PlotPlayEditor_OptionByName.lua.lua
**Functions:**
- GetPlotPlayEditor_OptionUis
**Snippet:**
```lua
function GetPlotPlayEditor_OptionUis(ui)
  local uis = {}
  
  uis.OptionTxt = ui:GetChild("OptionTxt")
  uis.JumpCBox = ui:GetChild("JumpCBox")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlayEditor_PartCompByName.lua.lua
**Functions:**
- GetPlotPlayEditor_PartCompUis
**Snippet:**
```lua
function GetPlotPlayEditor_PartCompUis(ui)
  local uis = {}
  
  uis.ChapterList = ui:GetChild("ChapterList")
  uis.AddChapterBtn = ui:GetChild("AddChapterBtn")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlayEditor_PlotPlayEditorByName.lua.lua
**Functions:**
- GetPlotPlayEditor_PlotPlayEditorUis
**Requires:**
- PlotPlayEditor_EditCompByName
- PlotPlayEditor_PartCompByName
- PlotPlayEditor_DialogEditByName
- PlotPlayEditor_SectionCompByName
- PlotPlayEditor_DialogCompByName
- PlotPlayEditor_ResourceChooseByName
**Snippet:**
```lua
require("PlotPlayEditor_EditCompByName")
require("PlotPlayEditor_PartCompByName")
require("PlotPlayEditor_DialogEditByName")
require("PlotPlayEditor_SectionCompByName")
require("PlotPlayEditor_DialogCompByName")
require("PlotPlayEditor_ResourceChooseByName")

function GetPlotPlayEditor_PlotPlayEditorUis(ui)
  local uis = {}
  uis.EditComp = GetPlotPlayEditor_EditCompUis(ui:GetChild("EditComp"))
```

---

## MP/PlotPlayEditor_PlotPlayEditorWindowByName.lua.lua
**Functions:**
- GetPlotPlayEditor_PlotPlayEditorWindowUis
**Requires:**
- PlotPlayEditor_PlotPlayEditorByName
**Snippet:**
```lua
require("PlotPlayEditor_PlotPlayEditorByName")

function GetPlotPlayEditor_PlotPlayEditorWindowUis(ui)
  local uis = {}
  uis.Main = GetPlotPlayEditor_PlotPlayEditorUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlayEditor_PopAddActionByName.lua.lua
**Functions:**
- GetPlotPlayEditor_PopAddActionUis
**Snippet:**
```lua
function GetPlotPlayEditor_PopAddActionUis(ui)
  local uis = {}
  
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Action0List = ui:GetChild("Action0List")
  uis.Action1List = ui:GetChild("Action1List")
  uis.Action1ChangeList = ui:GetChild("Action1ChangeList")
  uis.Action2List = ui:GetChild("Action2List")
  uis.Action6List = ui:GetChild("Action6List")
  uis.Action5List = ui:GetChild("Action5List")
```

---

## MP/PlotPlayEditor_ResourceChooseByName.lua.lua
**Functions:**
- GetPlotPlayEditor_ResourceChooseUis
**Requires:**
- PlotPlayEditor_SelectAreaByName
**Snippet:**
```lua
require("PlotPlayEditor_SelectAreaByName")

function GetPlotPlayEditor_ResourceChooseUis(ui)
  local uis = {}
  uis.SelectArea = GetPlotPlayEditor_SelectAreaUis(ui:GetChild("SelectArea"))
  uis.Ratio1Btn = ui:GetChild("Ratio1Btn")
  uis.Ratio2Btn = ui:GetChild("Ratio2Btn")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## MP/PlotPlayEditor_SectionBtnByName.lua.lua
**Functions:**
- GetPlotPlayEditor_SectionBtnUis
**Snippet:**
```lua
function GetPlotPlayEditor_SectionBtnUis(ui)
  local uis = {}
  
  uis.IdTxt = ui:GetChild("IdTxt")
  uis.IndexCBox = ui:GetChild("IndexCBox")
  uis.BgHolder = ui:GetChild("BgHolder")
  uis.BgLoader = ui:GetChild("BgLoader")
  uis.EffectInCBox = ui:GetChild("EffectInCBox")
  uis.EffectOutCBox = ui:GetChild("EffectOutCBox")
  uis.SkipBtn = ui:GetChild("SkipBtn")
```

---

## MP/PlotPlayEditor_SectionCompByName.lua.lua
**Functions:**
- GetPlotPlayEditor_SectionCompUis
**Snippet:**
```lua
function GetPlotPlayEditor_SectionCompUis(ui)
  local uis = {}
  
  uis.SectionList = ui:GetChild("SectionList")
  uis.AddSectionBtn = ui:GetChild("AddSectionBtn")
  uis.DelSectionBtn = ui:GetChild("DelSectionBtn")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlayEditor_SectionEditByName.lua.lua
**Functions:**
- GetPlotPlayEditor_SectionEditUis
**Snippet:**
```lua
function GetPlotPlayEditor_SectionEditUis(ui)
  local uis = {}
  
  uis.IdInputTxt = ui:GetChild("IdInputTxt")
  uis.AddBtn = ui:GetChild("AddBtn")
  uis.DelBtn = ui:GetChild("DelBtn")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.LeftBtn = ui:GetChild("LeftBtn")
  uis.RightBtn = ui:GetChild("RightBtn")
```

---

## MP/PlotPlayEditor_SelectAreaByName.lua.lua
**Functions:**
- GetPlotPlayEditor_SelectAreaUis
**Snippet:**
```lua
function GetPlotPlayEditor_SelectAreaUis(ui)
  local uis = {}
  
  uis.SelectList = ui:GetChild("SelectList")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlayEditor_SelectBtnInListByName.lua.lua
**Functions:**
- GetPlotPlayEditor_SelectBtnInListUis
**Snippet:**
```lua
function GetPlotPlayEditor_SelectBtnInListUis(ui)
  local uis = {}
  
  uis.BgHolder = ui:GetChild("BgHolder")
  uis.BgLoader = ui:GetChild("BgLoader")
  uis.CardHolder = ui:GetChild("CardHolder")
  uis.HeadHolder = ui:GetChild("HeadHolder")
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
```

---

## MP/PlotPlayEditor_SelectButtonByName.lua.lua
**Functions:**
- GetPlotPlayEditor_SelectButtonUis
**Snippet:**
```lua
function GetPlotPlayEditor_SelectButtonUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlayEditor_ShakeByName.lua.lua
**Functions:**
- GetPlotPlayEditor_ShakeUis
**Snippet:**
```lua
function GetPlotPlayEditor_ShakeUis(ui)
  local uis = {}
  
  uis.ShakeCBox = ui:GetChild("ShakeCBox")
  uis.ShakeDelayTxt = ui:GetChild("ShakeDelayTxt")
  uis.ShakeTimeTxt = ui:GetChild("ShakeTimeTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlayEditor_SwitchButtonByName.lua.lua
**Functions:**
- GetPlotPlayEditor_SwitchButtonUis
**Snippet:**
```lua
function GetPlotPlayEditor_SwitchButtonUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlayEndWindow.lua.lua
**Functions:**
- PlotPlayEndWindow.ReInitData
- PlotPlayEndWindow.OnInit
- PlotPlayEndWindow.UpdateInfo
- PlotPlayEndWindow.ShowEffect
- PlotPlayEndWindow.InitBtn
- PlotPlayEndWindow.OnShown
- PlotPlayEndWindow.OnHide
- PlotPlayEndWindow.OnClose
- PlotPlayEndWindow.HandleMessage
**Requires:**
- PlotPlay_EndByName
**Snippet:**
```lua
require("PlotPlay_EndByName")
local PlotPlayEndWindow = {}
local uis, contentPane, effectObject, closeCallback

function PlotPlayEndWindow.ReInitData()
end

function PlotPlayEndWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.PlotPlayEndWindow.package, WinResConfig.PlotPlayEndWindow.comName, function(com)
    contentPane = com
```

---

## MP/PlotPlayMgr.lua.lua
**Functions:**
- PlotPlayMgr.PlayFixedPlots
- PlotPlayMgr.PlayPlot
- PlotPlayMgr.PlayPrologue
- PlotPlayMgr.GetSectionIdSkipTo
- PlotPlayMgr.SkipPart
- PlotPlayMgr.DealSkipProcess
- PlotPlayMgr.PlayPlotEnd
- PlotPlayMgr.ChangeToNextPlot
- PlotPlayMgr.GetLive2DInfo
- PlotPlayMgr.GetSpineInfo
- PlotPlayMgr.RenderToHolder
- PlotPlayMgr.RenderToLoaderRT
- PlotPlayMgr.ReleaseFromRT
- PlotPlayMgr.ShowPlotReview
- list.itemProvider
- list.itemRenderer
- wordList.itemRenderer
- PlotPlayMgr.PlayVoice
**Snippet:**
```lua
PlotPlayMgr = {
  forcePlay = false,
  needStopWhenQuitReview = false,
  curPlotType = 0
}

function PlotPlayMgr.PlayFixedPlots(partIds)
  if partIds and #partIds > 0 then
    PlotPlayData.SetFixedPartIds(partIds)
    PlotPlayMgr.PlayPlot(partIds[1], nil, nil, nil, true)
```

---

## MP/PlotPlayScriptList.lua.lua
**Requires:**
- PlotPlayMgr
- PlotPlayData
- PlotPlayService
**Snippet:**
```lua
local require = require
require("PlotPlayMgr")
require("PlotPlayData")
require("PlotPlayService")
```

---

## MP/PlotPlayService.lua.lua
**Functions:**
- PlotPlayService.Init
- PlotPlayService.GetAllFinishedPlotsReq
- PlotPlayService.GetAllFinishedPlotsRsp
- PlotPlayService.FinishPlotReq
- PlotPlayService.FinishPlotRsp
- PlotPlayService.StoryOperateReportReq
- PlotPlayService.StoryOperateReportRsp
**Snippet:**
```lua
PlotPlayService = {}

function PlotPlayService.Init()
  Net.AddListener(Proto.MsgName.FinishPlotRsp, PlotPlayService.FinishPlotRsp)
  Net.AddListener(Proto.MsgName.GetAllFinishedPlotsRsp, PlotPlayService.GetAllFinishedPlotsRsp)
  Net.AddListener(Proto.MsgName.StoryOperateReportRsp, PlotPlayService.StoryOperateReportRsp)
end

function PlotPlayService.GetAllFinishedPlotsReq()
  local m = {}
```

---

## MP/PlotPlayStartWindow.lua.lua
**Functions:**
- PlotPlayStartWindow.ReInitData
- PlotPlayStartWindow.OnInit
- PlotPlayStartWindow.UpdateInfo
- PlotPlayStartWindow.ShowEffect
- PlotPlayStartWindow.InitBtn
- PlotPlayStartWindow.OnShown
- PlotPlayStartWindow.OnHide
- PlotPlayStartWindow.OnClose
- PlotPlayStartWindow.HandleMessage
**Requires:**
- PlotPlay_StartByName
**Snippet:**
```lua
require("PlotPlay_StartByName")
local PlotPlayStartWindow = {}
local uis, contentPane, effectObject, closeCallback

function PlotPlayStartWindow.ReInitData()
end

function PlotPlayStartWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.PlotPlayStartWindow.package, WinResConfig.PlotPlayStartWindow.comName, function(com)
    contentPane = com
```

---

## MP/PlotPlayWindow.lua.lua
**Functions:**
- PlotPlayWindow.ReInitData
- PlotPlayWindow.OnInit
- PlotPlayWindow.Start
- PlotPlayWindow.InitCtrl
- PlotPlayWindow.PlayPart
- PlotPlayWindow.PlaySection
- PlotPlayWindow.PlayDialog
- PlotPlayWindow.Play
- PlotPlayWindow.PlayOpen
- PlotPlayWindow.RealPlay
- PlotPlayWindow.DestroyAnimation
- PlotPlayWindow.Update
- PlotPlayWindow.Pause
- PlotPlayWindow.Resume
- PlotPlayWindow.Skip
- PlotPlayWindow.ShowSkipTips
- PlotPlayWindow.CloseSkipTips
- PlotPlayWindow.SureToSkip
- PlotPlayWindow.LookBack
- PlotPlayWindow.ClickAuto
- PlotPlayWindow.UpdateAutoDisplay
- PlotPlayWindow.UpdateBtnVisible
- PlotPlayWindow.ShowBackground
- PlotPlayWindow.ShowBackgroundById
- PlotPlayWindow.UpdateWord
- PlotPlayWindow.ShowTypingEffect
- curTypingEffect.effectEndAction
- PlotPlayWindow.SpeedUpTypingEffect
- PlotPlayWindow.StopTypingEffect
- PlotPlayWindow.PlayVoice
- PlotPlayWindow.PlayEnvSound
- PlotPlayWindow.PlaySpecialSound
- PlotPlayWindow.StopSpecialSound
- PlotPlayWindow.StopBgEffectSound
- PlotPlayWindow.PlayPlotEffect
- PlotPlayWindow.ShowRole
- PlotPlayWindow.AddSimulateVoiceModel
- PlotPlayWindow.SimulateVoiceMouth
- PlotPlayWindow.RandomMouth
- PlotPlayWindow.StopSimulateVoiceMouth
- PlotPlayWindow.InitCamera
- PlotPlayWindow.UpdateCamera
- PlotPlayWindow.ShowRoleEnd
- PlotPlayWindow.PlayTalkAnimIn
- PlotPlayWindow.PlayTalkAnimOut
- PlotPlayWindow.ShowCardEnterEffect
- PlotPlayWindow.ShowDialogEndEffect
- PlotPlayWindow.ShowCardOutEffect
- PlotPlayWindow.InitBtn
- PlotPlayWindow.ClickTouchBtn
- PlotPlayWindow.ClickHideBtn
- PlotPlayWindow.ClickTouchScreenBtn
- PlotPlayWindow.UpdateForceAutoDialog
- PlotPlayWindow.IsCurDialogForceAuto
- PlotPlayWindow.PlayEnd
- PlotPlayWindow.PlayPlotAllEnd
- PlotPlayWindow.OpenReview
- PlotPlayWindow.StopPlayingVoice
- PlotPlayWindow.CloseReview
- PlotPlayWindow.OnShown
- PlotPlayWindow.OnHide
- PlotPlayWindow.OnPreClose
- PlotPlayWindow.OnClose
- PlotPlayWindow.HandleMessage
**Requires:**
- PlotPlay_PlotPlayWindowByName
**Snippet:**
```lua
require("PlotPlay_PlotPlayWindowByName")
local PlotPlayWindow = {}
local uis, contentPane, typingEffectTalk, typingEffectMiddle, typingEffectNarrator, curTypingEffect
local typingInterval = 0.05
local typingSpeedUpInterval = 0.001
local speakChangeInterval = 0.2
local changeDialogTouchableDelayTime = 0.5
local colorSpeak = Color(1, 1, 1, 1)
local colorNoSpeak = Color(0.7, 0.7, 0.7, 1)
local curBackgroundId, curRoleHeadId, curRoleHeadObject
```

---

## MP/PlotPlay_AutoBtnByName.lua.lua
**Functions:**
- GetPlotPlay_AutoBtnUis
**Snippet:**
```lua
function GetPlotPlay_AutoBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_AutoGroupByName.lua.lua
**Functions:**
- GetPlotPlay_AutoGroupUis
**Requires:**
- PlotPlay_NextStepByName
**Snippet:**
```lua
require("PlotPlay_NextStepByName")

function GetPlotPlay_AutoGroupUis(ui)
  local uis = {}
  uis.NextStep = GetPlotPlay_NextStepUis(ui:GetChild("NextStep"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_CardByName.lua.lua
**Functions:**
- GetPlotPlay_CardUis
**Requires:**
- PlotPlay_OsMaskByName
**Snippet:**
```lua
require("PlotPlay_OsMaskByName")

function GetPlotPlay_CardUis(ui)
  local uis = {}
  uis.OsMask = GetPlotPlay_OsMaskUis(ui:GetChild("OsMask"))
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_CardShowByName.lua.lua
**Functions:**
- GetPlotPlay_CardShowUis
**Snippet:**
```lua
function GetPlotPlay_CardShowUis(ui)
  local uis = {}
  
  uis.CardLoader = ui:GetChild("CardLoader")
  uis.CardHolder = ui:GetChild("CardHolder")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_CGWordByName.lua.lua
**Functions:**
- GetPlotPlay_CGWordUis
**Snippet:**
```lua
function GetPlotPlay_CGWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_CloseBtnByName.lua.lua
**Functions:**
- GetPlotPlay_CloseBtnUis
**Snippet:**
```lua
function GetPlotPlay_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_EndByName.lua.lua
**Functions:**
- GetPlotPlay_EndUis
**Snippet:**
```lua
function GetPlotPlay_EndUis(ui)
  local uis = {}
  
  uis.EffectLoader = ui:GetChild("EffectLoader")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.TitleElpisTxt = ui:GetChild("TitleElpisTxt")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_ErectedHeadBgByName.lua.lua
**Functions:**
- GetPlotPlay_ErectedHeadBgUis
**Requires:**
- PlotPlay_CardShowByName
**Snippet:**
```lua
require("PlotPlay_CardShowByName")

function GetPlotPlay_ErectedHeadBgUis(ui)
  local uis = {}
  uis.CardShow = GetPlotPlay_CardShowUis(ui:GetChild("CardShow"))
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_ErectedHeadByName.lua.lua
**Functions:**
- GetPlotPlay_ErectedHeadUis
**Requires:**
- PlotPlay_ErectedHeadBgByName
**Snippet:**
```lua
require("PlotPlay_ErectedHeadBgByName")

function GetPlotPlay_ErectedHeadUis(ui)
  local uis = {}
  uis.ErectedHeadBg = GetPlotPlay_ErectedHeadBgUis(ui:GetChild("ErectedHeadBg"))
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_ExplainWordByName.lua.lua
**Functions:**
- GetPlotPlay_ExplainWordUis
**Snippet:**
```lua
function GetPlotPlay_ExplainWordUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_HideBtnByName.lua.lua
**Functions:**
- GetPlotPlay_HideBtnUis
**Snippet:**
```lua
function GetPlotPlay_HideBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_LineByName.lua.lua
**Functions:**
- GetPlotPlay_LineUis
**Snippet:**
```lua
function GetPlotPlay_LineUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_LookBackBtnByName.lua.lua
**Functions:**
- GetPlotPlay_LookBackBtnUis
**Snippet:**
```lua
function GetPlotPlay_LookBackBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_MiddleWordByName.lua.lua
**Functions:**
- GetPlotPlay_MiddleWordUis
**Snippet:**
```lua
function GetPlotPlay_MiddleWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.WordEffectTxt = ui:GetChild("WordEffectTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_NarratorWord1ByName.lua.lua
**Functions:**
- GetPlotPlay_NarratorWord1Uis
**Snippet:**
```lua
function GetPlotPlay_NarratorWord1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_NarratorWordByName.lua.lua
**Functions:**
- GetPlotPlay_NarratorWordUis
**Snippet:**
```lua
function GetPlotPlay_NarratorWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_NarratorWordTalkByName.lua.lua
**Functions:**
- GetPlotPlay_NarratorWordTalkUis
**Snippet:**
```lua
function GetPlotPlay_NarratorWordTalkUis(ui)
  local uis = {}
  
  uis.WordList = ui:GetChild("WordList")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_NextStepByName.lua.lua
**Functions:**
- GetPlotPlay_NextStepUis
**Snippet:**
```lua
function GetPlotPlay_NextStepUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_NpcHeadByName.lua.lua
**Functions:**
- GetPlotPlay_NpcHeadUis
**Requires:**
- PlotPlay_NpcHeadPicByName
**Snippet:**
```lua
require("PlotPlay_NpcHeadPicByName")

function GetPlotPlay_NpcHeadUis(ui)
  local uis = {}
  uis.NpcHeadLoader = GetPlotPlay_NpcHeadPicUis(ui:GetChild("NpcHeadLoader"))
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_NpcHeadPicByName.lua.lua
**Functions:**
- GetPlotPlay_NpcHeadPicUis
**Snippet:**
```lua
function GetPlotPlay_NpcHeadPicUis(ui)
  local uis = {}
  
  uis.NpcHeadLoader = ui:GetChild("NpcHeadLoader")
  uis.NpcHeadHolder = ui:GetChild("NpcHeadHolder")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_OptionByName.lua.lua
**Functions:**
- GetPlotPlay_OptionUis
**Snippet:**
```lua
function GetPlotPlay_OptionUis(ui)
  local uis = {}
  
  uis.TimeProgressBar = ui:GetChild("TimeProgressBar")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_OptionGroupByName.lua.lua
**Functions:**
- GetPlotPlay_OptionGroupUis
**Snippet:**
```lua
function GetPlotPlay_OptionGroupUis(ui)
  local uis = {}
  
  uis.OptionList = ui:GetChild("OptionList")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_OptionStripByName.lua.lua
**Functions:**
- GetPlotPlay_OptionStripUis
**Requires:**
- PlotPlay_OptionByName
**Snippet:**
```lua
require("PlotPlay_OptionByName")

function GetPlotPlay_OptionStripUis(ui)
  local uis = {}
  uis.Option = GetPlotPlay_OptionUis(ui:GetChild("Option"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_OsMaskByName.lua.lua
**Functions:**
- GetPlotPlay_OsMaskUis
**Snippet:**
```lua
function GetPlotPlay_OsMaskUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_OwnReviewWordByName.lua.lua
**Functions:**
- GetPlotPlay_OwnReviewWordUis
**Snippet:**
```lua
function GetPlotPlay_OwnReviewWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.VoicePlayBtn = ui:GetChild("VoicePlayBtn")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_OwnReviewWordTalkByName.lua.lua
**Functions:**
- GetPlotPlay_OwnReviewWordTalkUis
**Snippet:**
```lua
function GetPlotPlay_OwnReviewWordTalkUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_OwnVoicePlayBtnByName.lua.lua
**Functions:**
- GetPlotPlay_OwnVoicePlayBtnUis
**Snippet:**
```lua
function GetPlotPlay_OwnVoicePlayBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_PartStartBgByName.lua.lua
**Functions:**
- GetPlotPlay_PartStartBgUis
**Snippet:**
```lua
function GetPlotPlay_PartStartBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_PartStartByName.lua.lua
**Functions:**
- GetPlotPlay_PartStartUis
**Requires:**
- PlotPlay_CardByName
- PlotPlay_PartStartBgByName
**Snippet:**
```lua
require("PlotPlay_CardByName")
require("PlotPlay_PartStartBgByName")

function GetPlotPlay_PartStartUis(ui)
  local uis = {}
  uis.BackGround = GetPlotPlay_CardUis(ui:GetChild("BackGround"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.PartStartBg = GetPlotPlay_PartStartBgUis(ui:GetChild("PartStartBg"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
```

---

## MP/PlotPlay_PlotEffectByName.lua.lua
**Functions:**
- GetPlotPlay_PlotEffectUis
**Snippet:**
```lua
function GetPlotPlay_PlotEffectUis(ui)
  local uis = {}
  
  uis.EffectLoader = ui:GetChild("EffectLoader")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_PlotItemByName.lua.lua
**Functions:**
- GetPlotPlay_PlotItemUis
**Snippet:**
```lua
function GetPlotPlay_PlotItemUis(ui)
  local uis = {}
  
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_PlotItemGetByName.lua.lua
**Functions:**
- GetPlotPlay_PlotItemGetUis
**Requires:**
- PlotPlay_PlotItemByName
**Snippet:**
```lua
require("PlotPlay_PlotItemByName")

function GetPlotPlay_PlotItemGetUis(ui)
  local uis = {}
  uis.PlotItem = GetPlotPlay_PlotItemUis(ui:GetChild("PlotItem"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.SureBtn = ui:GetChild("SureBtn")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_PlotPlayByName.lua.lua
**Functions:**
- GetPlotPlay_PlotPlayUis
**Requires:**
- PlotPlay_CardByName
- PlotPlay_TalkByName
- PlotPlay_PartStartByName
- PlotPlay_PlotEffectByName
**Snippet:**
```lua
require("PlotPlay_CardByName")
require("PlotPlay_TalkByName")
require("PlotPlay_PartStartByName")
require("PlotPlay_PlotEffectByName")

function GetPlotPlay_PlotPlayUis(ui)
  local uis = {}
  uis.BackGround = GetPlotPlay_CardUis(ui:GetChild("BackGround"))
  uis.Card = GetPlotPlay_CardUis(ui:GetChild("Card"))
  uis.Talk = GetPlotPlay_TalkUis(ui:GetChild("Talk"))
```

---

## MP/PlotPlay_PlotPlayWindowByName.lua.lua
**Functions:**
- GetPlotPlay_PlotPlayWindowUis
**Requires:**
- PlotPlay_PlotPlayByName
**Snippet:**
```lua
require("PlotPlay_PlotPlayByName")

function GetPlotPlay_PlotPlayWindowUis(ui)
  local uis = {}
  uis.Main = GetPlotPlay_PlotPlayUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_PopupBgByName.lua.lua
**Functions:**
- GetPlotPlay_PopupBgUis
**Snippet:**
```lua
function GetPlotPlay_PopupBgUis(ui)
  local uis = {}
  
  uis.BlurLoader = ui:GetChild("BlurLoader")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_ReviewByName.lua.lua
**Functions:**
- GetPlotPlay_ReviewUis
**Snippet:**
```lua
function GetPlotPlay_ReviewUis(ui)
  local uis = {}
  
  uis.ReviewTalkList = ui:GetChild("ReviewTalkList")
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_ReviewTalkByName.lua.lua
**Functions:**
- GetPlotPlay_ReviewTalkUis
**Snippet:**
```lua
function GetPlotPlay_ReviewTalkUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_ReviewVoicePlayBtnByName.lua.lua
**Functions:**
- GetPlotPlay_ReviewVoicePlayBtnUis
**Snippet:**
```lua
function GetPlotPlay_ReviewVoicePlayBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_ReviewWordByName.lua.lua
**Functions:**
- GetPlotPlay_ReviewWordUis
**Snippet:**
```lua
function GetPlotPlay_ReviewWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.VoicePlayBtn = ui:GetChild("VoicePlayBtn")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_SkipBtnByName.lua.lua
**Functions:**
- GetPlotPlay_SkipBtnUis
**Snippet:**
```lua
function GetPlotPlay_SkipBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_SkipCloseBtnByName.lua.lua
**Functions:**
- GetPlotPlay_SkipCloseBtnUis
**Snippet:**
```lua
function GetPlotPlay_SkipCloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_SkipTipsByName.lua.lua
**Functions:**
- GetPlotPlay_SkipTipsUis
**Requires:**
- PlotPlay_PopupBgByName
**Snippet:**
```lua
require("PlotPlay_PopupBgByName")

function GetPlotPlay_SkipTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetPlotPlay_PopupBgUis(ui:GetChild("PopupBg"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.SureBtn = ui:GetChild("SureBtn")
  uis.SkipCloseBtn = ui:GetChild("SkipCloseBtn")
  uis.root = ui
```

---

## MP/PlotPlay_StartByName.lua.lua
**Functions:**
- GetPlotPlay_StartUis
**Snippet:**
```lua
function GetPlotPlay_StartUis(ui)
  local uis = {}
  
  uis.EffectLoader = ui:GetChild("EffectLoader")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.TitleElpisTxt = ui:GetChild("TitleElpisTxt")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
```

---

## MP/PlotPlay_TalkByName.lua.lua
**Functions:**
- GetPlotPlay_TalkUis
**Requires:**
- PlotPlay_TalkWordByName
- PlotPlay_ExplainWordByName
- PlotPlay_NarratorWordByName
- PlotPlay_MiddleWordByName
- PlotPlay_OptionGroupByName
- PlotPlay_AutoGroupByName
**Snippet:**
```lua
require("PlotPlay_TalkWordByName")
require("PlotPlay_ExplainWordByName")
require("PlotPlay_NarratorWordByName")
require("PlotPlay_MiddleWordByName")
require("PlotPlay_OptionGroupByName")
require("PlotPlay_AutoGroupByName")

function GetPlotPlay_TalkUis(ui)
  local uis = {}
  uis.TalkWord = GetPlotPlay_TalkWordUis(ui:GetChild("TalkWord"))
```

---

## MP/PlotPlay_TalkWordByName.lua.lua
**Functions:**
- GetPlotPlay_TalkWordUis
**Requires:**
- PlotPlay_NpcHeadByName
- PlotPlay_LineByName
**Snippet:**
```lua
require("PlotPlay_NpcHeadByName")
require("PlotPlay_LineByName")

function GetPlotPlay_TalkWordUis(ui)
  local uis = {}
  uis.NpcHead = GetPlotPlay_NpcHeadUis(ui:GetChild("NpcHead"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Line = GetPlotPlay_LineUis(ui:GetChild("Line"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## MP/PlotPlay_TimeProgressBarByName.lua.lua
**Functions:**
- GetPlotPlay_TimeProgressBarUis
**Snippet:**
```lua
function GetPlotPlay_TimeProgressBarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## MP/PlotPlay_TouchBtnByName.lua.lua
**Functions:**
- GetPlotPlay_TouchBtnUis
**Snippet:**
```lua
function GetPlotPlay_TouchBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## MP/PlotRewardWindow.lua.lua
**Functions:**
- PlotRewardWindow.ReInitData
- PlotRewardWindow.OnInit
- PlotRewardWindow.Init
- PlotRewardWindow.UpdateInfo
- tips.ItemList.itemRenderer
- PlotRewardWindow.InitBtn
- PlotRewardWindow.OnClose
**Requires:**
- PlotDungeon_PlotRewardWindowByName
**Snippet:**
```lua
require("PlotDungeon_PlotRewardWindowByName")
local PlotRewardWindow = {}
local uis, contentPane

function PlotRewardWindow.ReInitData()
end

function PlotRewardWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.PlotRewardWindow.package, WinResConfig.PlotRewardWindow.comName, function(com)
    contentPane = com
```

---

## MP/Polygon.lua.lua
**Functions:**
- Polygon:__ctor
- Polygon:init
- Polygon:initLocalData
- Polygon:initMassData
- Polygon:translateCentroid
- Polygon:updateVertices
- Polygon:updateNormals
- Polygon:update
- Polygon:setAngle
- Polygon:setPos
- Polygon:updateAABB
- Polygon:containPoint
- Polygon:pointRayCasting
- Polygon.projectPointToEdge
- Polygon.computeNormal
- Polygon.computeNormals
**Snippet:**
```lua
local base = Shape
local Polygon = Create("Polygon", base)

function Polygon:__ctor()
  self.shapeType = ShapeType.Poly
  self.vertices = nil
  self.normals = nil
  self.localVertices = nil
  self.localNormals = nil
  self.vertexCount = 0
```

---

## MP/profiler.lua.lua
**Functions:**
- Profiler:start
- Profiler:stop
- profiler_hook_wrapper_by_call
- Profiler:analysis_call_info
- Profiler:get_func_info_by_cache
- Profiler:format_header
- Profiler:report
- Profiler:dump_report_to_file
- Profiler:pretty_name
**Snippet:**
```lua
local EMPTY_TIME = "0.0000"
local emptyToThis = "~"
local timeWidth = 7
local relaWidth = 6
local callWidth = 10
local divider = ""
local formatOutput = ""
local formatTotalTime = "Total time spent in profiled functions: %s\n"
local formatFunTime = "%04.4f"
local formatFunRelative = "%03.1f"
```

---

## MP/Proto.lua.lua
**Snippet:**
```lua
local Proto = {
  Schema = "syntax = \"proto3\"\n\n\n\n\n//玩家排行信息\nmessage GameRankActorInfo {\n    int64 uin                   = 1;\n    int32 level                 = 2;    //等级\n    int32 faceId                = 3;    //头像ID\n    string name                 = 4;    //名字\n    int64 guildUid              = 5;    //所在公会 uid\n    string guildName            = 6;    //所在公会名字\n    int32   rank                = 7;    //排行\n    int64 score                 = 8;    //积分\n    int64 stamp                 = 9;    //上榜时间\n    ActorHead actorHead         = 10;   //头像信息\n}\n\n\nmessage ActivityBaseInfo {\n    int32 activityId    = 1;    //活动ID\n    int64 startStamp    = 2;    //开始时间\n    int64 endStamp      = 3;    //结束时间\n}\n\n//签到活动\nmessage ActivitySignIn {\n    ActivityBaseInfo baseInfo   = 1;\n    int32 curDay                = 2;\n    bool    isTodaySignIn       = 3;\n}\n//关卡活动\nmessage ActivityStage {\n    ActivityBaseInfo baseInfo       = 1;\n    map<int32,int64> normalChapter  = 2;    //解锁的普通章节\n    map<int32,int64> creamChapter   = 3;    //解锁的素材章节\n    map<int32,int64> bossChapter    = 4;    //解锁的boss章节\n    repeated int32  finishStages    = 5;    //完成的关卡\n    map<int32,int32>    boughtItem  = 6;    //已经购买的商品 格子ID->购买数量\n    repeated TaskInfo taskList      = 7;    //当前任务列表\n    int32 curDay                    = 8;    //签到数据\n    repeated   int32 signDay        = 9;    //签到数据\n    int32 creamCount                = 10;   //素材本挑战次数\n\n}\n\n//搜索活动\nmessage ActivitySearch {\n    ActivityBaseInfo baseInfo   = 1;\n    bool isTodaySearch          = 2;\n    repeated ItemTuple dropRewards      = 3;    //掉落奖励\n    repeated ItemTuple showRewards      = 4;    //显示奖励\n    repeated ItemTuple specialRewards   = 5;    //额外奖励\n    repeated int32  choosePos           = 6;    //选择位置\n    int32 totalCount                    = 7;\n    int32 curCount                      = 8;\n}\n\n//回归活动\nmessage ActivityReturn {\n    ActivityBaseInfo baseInfo = 1;\n    int32 returnDay           = 2;  //已回归天数\n    int32 signDay             = 3;  //已签到的天数\n    int32 activityCheckInType = 4;  //使用的签到奖励类型\n    string picUrl             = 5;  //活动图片 url\n}\n//转盘（多轮）活动\nmessage TurnPoolRoundData {\n    int32 round                 = 1;\n    int32 turnNum               = 2;    //抽取次数\n    repeated TurnPoolData pools = 3;\n    int64 unlockStamp           = 4;    //解锁时间\n}\n//转盘活动\nmessage TurnPoolData {\n    int32 poolId = 1;\n    int32 count = 2;\n    int32 prob  = 3;\n}\n\n//回归活动\nmessage ActivityReturnPro {\n    ActivityBaseInfo baseInfo       = 1;\n    int32 freeReward                = 2;\n    int32 returnDay                 = 3;  //已回归天数\n    int32 signDay                   = 4;  //已签到的天数\n    repeated DropMulti dailyDrop    = 5;  //每日掉落增益次数\n    map<int32,int32>    boughtItem  = 6;  //已经购买的商品 格子ID->购买数量\n    repeated TaskInfo taskList      = 7;  //当前任务列表\n    int32 costItemCount             = 8;  \n\n}\n//掉落活动\nmessage ActivityDropMulti {\n    ActivityBaseInfo baseInfo       = 1;\n    repeated DropMulti dailyDrop    = 2;  //每日掉落增益次数\n}\nmessage ActivityTurnTable {\n    ActivityBaseInfo baseInfo = 1;\n    int32 turnNum               = 2;    //抽取次数\n    repeated TurnPoolData pools = 3;\n    int32 freeGet               = 4;    //免费次数是否领取\n}\n\n\nmessage ActivityTurnTableRound {\n    ActivityBaseInfo baseInfo                = 1;\n    repeated TurnPoolRoundData rounds        = 2;\n    int32 curRound                           = 3;\n    int32 freeGet                            = 4;    //免费次数是否领取\n    int32 totalRechargeAmount                = 5;    //总充值金额\n    int32 fetchedRechargeLevel               = 6;    //已领取的充值奖励档位\n    bool dailyRechargeReward                 = 7;    //是否可以领取每日奖励\n    int32  resetCount                        = 8;    //重置次数\n}\n\nmessage GetActivityAllReq {\n    \n}\n\nmessage GetActivityAllRsp {\n    repeated ActivitySignIn signInAct   = 1;    //签到活动\n    repeated ActivityStage  stageAct    = 2;    //关卡活动\n    repeated ActivitySearch searchAct   = 3;    //搜索活动\n    ActivityReturn returnAct            = 4;    //回归活动\n    repeated ActivityTurnTable turnAct  = 5;    //转盘活动\n    ActivityTurnTableRound roundAct     = 6;    //转盘（多轮）活动(累充抽奖)\n    ActivityReturnPro returnProAct      = 7;    //回归活动(pro)\n    repeated ActivityDropMulti dropAct  = 8;    //掉落活动\n}\n\n//领取累充抽奖的累充奖励\nmessage FetchAccumRechargeRewardReq {\n    int32 activityId    = 1;    //活动 id\n    int32 rechargeLevel = 2;    //0: 表示领取每日奖励 奖励档位发最高可领取的档位(base_activity_recharge.csv 表的 recharge_level 字段)\n}\n\nmessage FetchAccumRechargeRewardRsp {\n    repeated ItemTuple rewards = 1;\n    int32 fetchedRechargeLevel = 2;    //已领取的充值奖励档位\n    bool dailyRechargeReward   = 3;    //是否可以领取每日奖励\n}\n\n//活动签到\nmessage ActivitySignInReq {\n    int32 activityId = 1;\n}\n\nmessage ActivitySignInRsp {\n    repeated ItemTuple rewards      = 1;\n    ActivitySignIn signInAct        = 2;\n}\n\n//关卡签到\nmessage ActivityStageSignInReq {\n    int32 activityId = 1;\n    int32 signDay    = 2;\n}\n\nmessage ActivityStageSignInRsp {\n    int32 activityId                = 1;\n    repeated DropTuple rewards      = 2;\n    int32 curDay                    = 3;    //签到数据\n    repeated   int32 signDay        = 4;    //签到数据\n}\n//活动商店购买\nmessage ActivityStageShopBuyReq {\n    int32 gridId        = 1;\n    int32 buyCount      = 2;\n}\n\n//小游戏\nmessage ActivityGetMiniGameReq {\n    int32 activityId    = 1;\n    int32 gameId        = 2;\n    \n}\n\nmessage ActivityGetMiniGameRsp {\n    repeated TaskInfo taskList              = 1;    //当前任务列表\n    repeated MiniGameRecord records         = 2;    //小游戏记录\n    int32 miniScore                         = 3;    //小游戏累积积分\n    int32 miniDailyStat                     = 4;    //小游戏每日奖励 enum TASK_STATE\n    int32 miniDailyScore                    = 5;    //小游戏每日累积积分\n    int32 miniHighScore                     = 6;    //小游戏最高积分\n    int32  miniDailyNum                     = 7;    //小游戏每日游戏次数\n    map<int32,int32> extraCount             = 8;    //小游戏额外数据\n    int32 gameId                            = 9;\n}\n\nmessage ActivityPlayMiniGameReq {\n    int32 activityId                = 1;\n    int32 gameId                    = 2;\n    MiniGameRecord records          = 3;    //小游戏记录\n    int32 playSec                   = 4;    //游戏时间\n    int32 extStat                   = 5;    //1:时间校验\n}\n\nmessage ActivityPlayMiniGameRsp { \n    \n}\n\nmessage ActivityRewardMiniGameReq {\n    int32 activityId                = 1;   \n    int32 gameId                    = 2;\n    int32 subId                     = 3;\n}\n\nmessage ActivityRewardMiniGameRsp { \n    int32 gameId                    = 1;\n    repeated DropTuple rewards      = 2;\n    int32 miniDailyStat             = 3;    //小游戏每日奖励 enum TASK_STATE\n    map<int32,int32> extraCount     = 4;    //小游戏额外数据\n}\n\nmessage ActivityStageShopBuyRsp {\n    repeated DropTuple rewards      = 1;\n    map<int32,int32>    boughtItem  = 2;    //已经购买的商品 格子ID->购买数量\n}\n\n//活动任务领奖\nmessage ActivityStageTaskRewardReq {\n    int32 activityId            = 1;\n    int64 taskUid               = 2;\n}\n\nmessage ActivityStageTaskRewardRsp {\n    repeated DropTuple rewards      = 1;\n    repeated TaskInfo changeTask    = 2;    //改变的任务\n}\n\n//搜索活动领奖\nmessage ActivitySearchReq {\n    int32 activityId                    = 1;\n    repeated int32  choosePos           = 2;    //选择位置\n}\n\nmessage ActivitySearchRsp {\n    repeated ItemTuple dropRewards      = 1;    //掉落奖励\n    repeated ItemTuple showRewards      = 2;    //显示奖励\n    repeated ItemTuple specialRewards   = 3;    //额外奖励\n    int32 totalCount                    = 4;\n    int32 curCount                      = 5;\n}\n//获取所有banner\nmessage GetAllBannerReq {\n}\n\nmessage GetAllBannerRsp {\n    repeated int32 idList = 1;\n}\n\n//通过活动 id 获取活动信息\nmessage GetOpActivityByIdReq {\n    repeated int32 activityIds = 1;\n}\n\nmessage GetOpActivityByIdRsp {\n    repeated OpActivity infos = 1;\n}\n\n//回归活动签到\nmessage ActivityReturnSignInReq {\n    int32 signDay = 1;\n}\n\nmessage ActivityReturnSignInRsp {\n    repeated ItemTuple rewards = 1;\n    ActivityReturn returnAct   = 2;\n}\n\n//活动回顾\nmessage ActivityReviewInfo {\n    int64 uin = 1;\n    repeated int32 unlockList       = 2;\n    map<int32,int32>    boughtItem  = 3;    //已经购买的商品 格子ID->购买数量\n}\n\n//获取所有回归活动\nmessage GetActivityReviewInfoReq {\n\n}\n\nmessage GetActivityReviewInfoRsp {\n    repeated int32 unlockList       = 1;\n    map<int32,int32>    boughtItem  = 2;    //已经购买的商品 格子ID->购买数量\n}\n//回归活动解锁\nmessage ActivityReviewUnlockReq {\n    int32 actId = 1;\n}\n\nmessage ActivityReviewUnlockRsp {\n    repeated int32 unlockList    = 1;\n}\n//回归活动商店购买\nmessage ActivityReviewShopBuyReq {\n    int32 gridId        = 1;\n    int32 buyCount      = 2;\n}\n\nmessage ActivityReviewShopBuyRsp {\n    repeated DropTuple rewards      = 1;\n    map<int32,int32>    boughtItem  = 2;    //已经购买的商品 格子ID->购买数量\n}\n\n//转盘抽奖\nmessage ActivityDoTurnTableReq {\n    int32 activityId                    = 1;    \n}\nmessage ActivityDoTurnTableRsp {\n    int32 poolId                            = 1;    //掉落Id\n    repeated DropTuple rewards              = 2;    //\n    int32 turnNum                           = 3;    //抽取次数\n    repeated TurnPoolData pools             = 4;\n}\n//转盘（多轮）抽奖\nmessage ActivityDoTurnTableRoundReq {\n    int32 activityId                    = 1;    \n    int32 roundId                       = 2;\n}\nmessage ActivityDoTurnTableRoundRsp {\n    int32 poolId                            = 1;    //掉落Id\n    repeated DropTuple rewards              = 2;    //\n    TurnPoolRoundData   roundData           = 3;\n}\n\n//领取免费资源\nmessage ActivityTurnTableGetFreeReq {\n    int32 activityId                    = 1;    \n}\n\nmessage ActivityTurnTableGetFreeRsp {\n    repeated DropTuple rewards         = 1;    // \n}\n\n//获取活动游戏排行榜\nmessage ActivityGetGameTopRankReq {\n    int32 activityId        = 1;    \n    int32 gameId            = 2;\n}\n\nmessage ActivityGetGameTopRankRsp {\n    int32       rank                        = 1;    //自己排名\n    int32 score                             = 2;    //自己分数\n    repeated    GameRankActorInfo rankList  = 3;\n}\n//回归活动pro 签到\nmessage ActivityReturnProSigninReq {\n    int32 activityId = 1;\n    int32 signType = 2; //0 免费签到 1 7日签到\n}\n\nmessage ActivityReturnProSigninRsp {\n    repeated DropTuple rewards      = 1;\n    int32 activityId                = 2;  //\n    int32 freeReward                = 3;\n    int32 signDay                   = 4;  //已签到的天数\n}\n\n\n//回归活动pro 购买\nmessage ActivityReturnProShopBuyReq {\n    int32 activityId            = 1;\n    int32 gridId                = 2;\n    int32 buyCount              = 3;\n}\n\nmessage ActivityReturnProShopBuyRsp {\n    int32 activityId                = 1;  //\n    repeated DropTuple rewards      = 2;\n    map<int32,int32>    boughtItem  = 3;    //已经购买的商品 格子ID->购买数量\n    int32 costItemCount             = 4; \n}\n\n//活动任务领奖\nmessage ActivityReturnProTaskRewardReq {\n    int32 activityId            = 1;\n    int64 taskUid               = 2;\n}\n\nmessage ActivityReturnProTaskRewardRsp {\n    int32 activityId                = 1;  //\n    repeated DropTuple rewards      = 2;\n    repeated TaskInfo changeTask    = 3;    //改变的任务\n}\n\n//获取关卡掉落增益\nmessage ActivityGetStageDropMultiReq {\n    int32 stageId = 1;\n}\n\nmessage ActivityGetStageDropMultiRsp {\n    int32 stageId = 1;\n    repeated DropMulti dropMultis    = 2;  //掉落增益次数\n}\n\n\n\n\nmessage CreateActorReq {\n    string name         = 1;\n    string deviceId     = 2;    //设备 id\n    string channel      = 3;    //渠道\n    int32 platform      = 4;    //sp_common.proto   enum PLATFORM_TYPE\n    string loginIP       = 5;    //用户 ip 地址\n}\n\nmessage CreateActorRsp {\n    ActorInfo actor = 1;\n}\n\n\nmessage GetActorInfoReq {\n\n}\n\nmessage GetActorInfoRsp {\n    ActorInfo actor = 1;\n}\n\nmessage GetActorMirrorInfoReq {\n\n}\n\nmessage GetActorMirrorInfoRsp {\n    ActorMirrorInfo info = 1;\n}\n\nmessage ActorInfoUpdateNotify {\n    ActorInfo actor = 1;\n}\n\n//玩家修改名字\nmessage ChangeNameReq {\n    string name = 1;\n}\n\nmessage ChangeNameRsp {\n    ActorInfo actor = 1;\n}\n\nmessage OfflineReq {\n}\n\nmessage OfflineRsp {\n}\n\nmessage HeartBeatReq {\n    string plat = 1;\n}\n\nmessage HeartBeatRsp {\n    int64 maxResId  = 1;    //当前最大客户端资源id,用于控制客户端在游戏内弹出去更新资源\n    int64 sysStamp  = 2;    //系统时间\n    int32 resVersion= 3;    //客户端资源版本号\n    bool debug      = 4;    //是否开启 debug 日志开关\n    int32 loginDays = 5;    //登录天数\n    int64 nextRreshDaySec = 6;  //下次天更新的绝对秒数\n}\n\nmessage HeartBeatNotify {\n    string gtwId    = 1;\n}\n\nmessage GetActorSignInReq {\n}\n\nmessage GetActorSignInRsp {\n    int32 signStat      = 1;\n    bool isTodaySignIn  = 2;\n    int32 allDay        = 3;    //总签到天\n}\n\nmessage ActorSignInReq  {\n}\n\nmessage ActorSignInRsp  {\n    int32 signStat      = 1;\n    bool isTodaySignIn  = 2;\n    ItemTuple reward    = 3;\n    int32 allDay        = 4;    //总签到天\n}\n\nmessage ActorGmReq {\n    string command          = 1;    //gm指令\n    repeated string params  = 2;    //参数\n}\n\nmessage ActorGmRsp {\n    string ret          = 1;\n    string failCmd      = 2;    //执行失败的命令\n}\n\nmessage GetUnlockedFeaturesReq {\n}\n\nmessage GetUnlockedFeaturesRsp {\n    repeated int32 featureIds = 1;\n}\n\n//获取已获得的 emoji\nmessage GetEmojiReq {\n\n}\n\nmessage GetEmojiRsp {\n    repeated string latestEmojiLst = 1;\n}\n\n//客户端上报最近使用的表情\nmessage ReportLatestEmojiReq {\n    repeated string latestEmojiLst  = 1;\n}\n\nmessage ReportLatestEmojiRsp {\n\n}\n\n//获取玩家信息面板详细信息\nmessage GetSelfDetailInfoReq {\n}\n\nmessage GetSelfDetailInfoRsp {\n    int32 currentStage          = 1;    //剧情副本进度: 当前关卡\n    int32 winCount              = 2;    //战斗胜利次数\n    int32 killMobCount          = 3;    //击退魔物数量\n    bool hideResource           = 4;    //是否对别人隐藏物资显示\n    int32 totalCardCount        = 5;    //卡牌总量\n    repeated int32 displayCards = 6;    //展示的卡牌\n    bool inGuild                = 7;    //是否已加入公会\n    string guildName            = 8;    //所在公会名字\n    string city                 = 9;    //所在城市\n}\n\n//查看别人的详细信息\nmessage GetOtherDetailInfoReq {\n    int64 targetUin = 1;\n}\n\nmessage GetOtherDetailInfoRsp {\n    ActorMirrorInfo info        = 1;\n    int32 relationState         = 2;   //sp_datamodel.proto    enum RELATION_STATE\n    string remark               = 3;   //给对方设置的备注\n\n    int32 currentStage          = 4;    //剧情副本进度: 当前关卡\n    int32 winCount              = 5;    //战斗胜利次数\n    int32 killMobCount          = 6;    //击退魔物数量\n    bool hideResource           = 7;    //是否对别人隐藏物资显示\n    repeated CardInfo displayCards = 8;    //展示的卡牌\n    bool inGuild                = 9;    //是否已加入公会\n    string guildName            = 10;    //所在公会名字\n    string city                 = 11;   //所在城市\n\n    repeated ItemInfo resources = 12;   //物资信息\n    int32 loginDays             = 13;   //登录天数\n    bool blockMe                = 14;   //对方是否屏蔽了自己\n}\n\n//设置个人信息面板展示的卡牌\nmessage SetProfileDisplayCardsReq {\n    repeated int32 cardIds      = 1;\n}\n\nmessage SetProfileDisplayCardsRsp {\n}\n\n//设置个人信息面板物资展示开关\nmessage SetProfileShowResourceReq {\n    bool hideResource  = 1; //是否隐藏物资显示\n}\n\nmessage SetProfileShowResourceRsp {\n}\n\n\n\n//故事\nmessage GetStoryListReq {\n    int32 newStory = 1;\n}\n\nmessage GetStoryListRsp {\n    repeated int32 storyList       = 1;\n    repeated int32 staredSoundLst  = 2;    //收藏的音乐\n    repeated int32 soundPlaylist   = 3;    //播放列表\n}\n\n//收藏音乐\nmessage OperateStarSoundReq {\n    int32 soundId = 1;\n    int32 opType  = 2;  //1: 收藏  2: 取消收藏\n}\n\nmessage OperateStarSoundRsp {\n    repeated int32 staredSoundLst = 1;\n}\n\n//操作音乐播放列表\nmessage OperateSoundPlayListReq {\n    int32 soundId = 1;\n    int32 opType  = 2;  //1: 加入播放列表  2: 移除播放列表   3: 上移   4: 下移\n}\n\nmessage OperateSoundPlayListRsp {\n    repeated int32 soundPlaylist = 1;\n}\n\nmessage SaveSettingsReq {\n    string settings = 1;\n\n    //type: 3战斗帧率设置、4界面帧率设置、5公告开启设置、7音效开启设置、8音乐开启设置、9配音开启设置、10战斗状态开启设置、11血条开启设置、12普通伤害开启设置\n    //value: type-3: 高帧为1, 低帧为0. type-4: 高帧为1, 低帧为0. type5-12: 关闭为0, 开启为1\n    int32 opType    = 2;\n    string value    = 3;\n}\n\nmessage SaveSettingsRsp {\n}\n\nmessage ChangeFaceReq {\n    int32 faceId = 1;\n}\n\nmessage ChangeFaceRsp {\n    int32 faceId = 1;\n}\n\nmessage ChangeHeadReq {\n    ActorHead head = 1;\n}\n\nmessage ChangeHeadRsp {\n    ActorHead head = 1;\n}\n\n//上报完成新手引导\nmessage FinishGuideReq {\n    int32 guideId   = 1;\n    int32 step      = 2;\n}\n\nmessage FinishGuideRsp {\n    int32 guideId   = 1;\n    int32 step      = 2;\n}\n\n//获取新手引导进度\nmessage GetGuideProgressReq {\n}\n\nmessage GetGuideProgressRsp {\n    repeated GuideInfo finishedGuides = 1;  //已完成的新手引导\n}\n\n//检查功能是否开启\nmessage CheckFeatureOpenReq {\n    repeated int32 featureIds = 1;\n}\n\nmessage CheckFeatureOpenRsp {\n    repeated int32 featureIds       = 1;    //请求检查的 featureId\n    repeated int32 openFeatureIds   = 2;    //已开启的 featureId\n}\n\n//请求完成剧情\nmessage FinishPlotReq {\n    int32 plotId            = 1;\n    repeated int32 stepIds  = 2;\n    bool skip               = 3;\n}\n\nmessage FinishPlotRsp {\n    int32 plotId                = 1;\n    repeated int32 stepIds      = 2;\n    bool skip                   = 3;\n    repeated ItemTuple rewards  = 4;    //奖励\n}\n\n//获取所有已完成的剧情 id\nmessage GetAllFinishedPlotsReq {\n}\n\nmessage GetAllFinishedPlotsRsp {\n    repeated int32 plotIdLst    = 1;\n}\n\n//体力恢复信息\nmessage EnergyRecoverInfo {\n    int32 curEnergy             = 1;    //当前体力\n    int32 energyRecoverLimit    = 2;    //体力恢复上限\n    int32 curBuyTimes           = 3;    //当前已购买次数\n    int32 maxBuyTimes           = 4;    //购买次数上限\n    int64 nextRecoverStamp      = 5;    //下次恢复时间\n    int64 recoverDoneStamp      = 6;    //全部恢复时间\n}\n\n//获取体力恢复信息\nmessage GetEnergyRecoverInfoReq {\n}\n\nmessage GetEnergyRecoverInfoRsp {\n    EnergyRecoverInfo info  = 1;\n}\n\n//修改密码\nmessage ChangePasswordReq {\n    string accountId    = 1;    //游戏内改密码可以不传该值\n    string oldPassword  = 2;    //旧密码\n    string newPassword  = 3;    //新密码\n}\n\nmessage ChangePasswordRsp {\n}\n\n//更新公会操作状态\nmessage UpdateGuildOperateStateReq {\n    string operate = 1;\n}\n\nmessage UpdateGuildOperateStateRsp {\n}\n\n//获取公会操作状态\nmessage GetGuildOperateStateReq {\n}\n\nmessage GetGuildOperateStateRsp {\n    bool createdGuild = 1;    //是否创建过公会\n    bool appliedGuild = 2;   //是否申请加入过公会\n}\n\nmessage StoryOperateReportReq {\n    int32 storyType = 1;    //1主线剧情/2新手引导剧情/3活动本剧情\n    int32 storyId   = 2;    //关联剧情大类ID\n    int32 dialogId  = 3;    //关联剧情每句ID\n    int32 jump      = 4;    //1跳过，空为非跳过\n}\n\nmessage StoryOperateReportRsp{\n}\n\n//领取补给\nmessage RewardSupplyReq {\n    int32 rewardId  = 1;\n    bool isRedeem   = 2;    //是否为补领\n}\nmessage RewardSupplyRsp {\n    repeated DropTuple reward       = 1;    //奖励\n    repeated int32 rewarded         = 2;\n}\n//获取补给信息\nmessage GetSupplyInfoReq {\n}\nmessage GetSupplyInfoRsp {\n    repeated int32 rewarded = 1;    //已经领取的\n}\n\n//客户端操作记录上报\nmessage ReportOperateRecordReq {\n    int32 opType            = 1;\n    repeated int32 values   = 2;\n}\n\nmessage ReportOperateRecordRsp{\n}\n\n//获取操作记录\nmessage GetOperateRecordReq {\n    repeated int32 opTypes  = 1;    //获取多个 opType 的记录,如果传空就获取所有类型的记录\n}\n\nmessage GetOperateRecordRsp {\n    repeated OperateRecord records = 1;\n}\n\n//设置生日\nmessage SetBirthdayReq {\n    int32 birthday = 1;     // month * 100 + day\n}\n\nmessage SetBirthdayRsp {\n    ActorInfo actor = 1;\n}\n\n//客户端请求同步资源(物品、角色、徽章)\nmessage BatchSyncResReq {\n    int64 itemSyncKey   = 1;    //客户端物品的 syncKey\n    int64 cardSyncKey   = 2;    //客户端角色的 syncKey\n    int64 badgeSyncKey  = 3;    //客户端徽章的 syncKey\n}\n\nmessage BatchSyncResRsp {\n}\n\n//使用兑换码\nmessage UseExchangeCodeReq {\n    string code = 1;\n}\n\nmessage UseExchangeCodeRsp {\n    string code                 = 1;\n    repeated DropTuple rewards  = 2;\n}\n\n//客户端异常上报\nmessage ClientAbnormalReportReq {\n    string reason = 1;\n}\n\nmessage ClientAbnormalReportRsp {\n}\n\n\nmessage GetAgreementInfoReq {\n}\n\nmessage AgreementShow {\n    int32 season            = 2;\n    repeated int32 rewards  = 3;\n    repeated int32 openList = 4;\n}\nmessage GetAgreementInfoRsp {\n    int32 curDay                    = 1;\n    repeated AgreementShow datas  = 2;\n}\n\nmessage RewardAgreementReq {\n    int32 season        = 1;\n    int32 rewardId      = 2;\n}\n\nmessage RewardAgreementRsp {\n    repeated DropTuple reward       = 1;    //奖励\n    repeated int32 rewards          = 2;\n    AgreementShow agreement         = 3;\n}\n\nmessage CliTriggerEventNotify {\n    string eventId = 1; //stdspend4000  dupspend100\n}\n\n\n\n\n\nenum ARENA_SEASON_STAT {\n    CLOSE           = 0;    //赛季关闭\n    CREATING        = 1;    //赛季开启中\n    OPEN            = 2;    //开启\n    SETTLE          = 3;    //结算\n    DAILY_SETTLE    = 4;    //每日结算\n}\n\nmessage ArenaMirrorInfo {\n    int64 uin                       = 1;\n    int64 createTime                = 2;    //账号创建时间\n    int64 fightScore                = 3;    //战斗积分\n    int32 level                     = 4;    //等级\n    int32 faceId                    = 5;    //头像ID\n    string name                     = 6;    //名字\n    int64 guildUid                  = 7;    //所在公会 uid\n    string guildName                = 8;    //所在公会名字\n    int32 arenaMedal                = 9;    //竞技场的勋章\n    int64 lastLoginStamp            = 10;   //上次登录时间\n    bool isOnline                   = 11;   //是否在线\n    int32 randNameId                = 12;   //随机nameID\n    ActorHead actorHead             = 13;   //头像信息\n}\n//竞技场对手数据\nmessage ArenaOpponentInfo {\n    ArenaMirrorInfo info    = 1;    //对手人物信息\n    int32 rank              = 2;    //排行\n}\n//匹配信息\nmessage ArenaMatchData {\n    int32   rank                            = 1;    //自己排名\n    int32   level                           = 2;    //自己段位\n    repeated int32 opponentRanks            = 3;    //匹配到的 3 个名次\n    repeated ArenaOpponentInfo opponents    = 4;    //对手信息\n    int32 seasonId                          = 5;    //赛季 id\n}\n//请求竞技场数据\nmessage ArenaGetAllReq {\n\n}\n\nmessage ArenaGetAllRsp {\n    int32   curSeason                   = 1;    //当前赛季ID\n    int64   nextFightTime               = 2;    //下次挑战时间\n    int64   seasonStartTime             = 3;    //赛季开始时间\n    int64   seasonEndTime               = 4;    //赛季结束时间\n    int64   seasonEndStartTime          = 5;    //赛季结算完成时间\n    int32   fightNum                    = 6;    //挑战次数\n    int32   buyNum                      = 7;    //挑战购买次数\n    int32   highRank                    = 8;    //赛季最高排名\n    repeated int32   rewardList         = 9;    //赛季领奖id\n    ArenaMatchData  matchInfo           = 10;   //匹配信息\n    int64   nextSettleTime              = 11;   //下次结算时间\n    int32   seasonStat                  = 12;   //赛季状态\n    int32   rewardPhase                 = 13;   //领奖季度\n    bool    isDailySettle               = 14;   //是否每日结算\n    int32 historyHighRank               = 15;   //历史最高排名\n}\n//请求战斗记录\nmessage ArenaGetRecordReq {\n}\nmessage ArenaGetRecordRsp {\n    repeated ArenaBattleRecord records = 1;  //战斗记录\n}\n\n//存储战斗记录\nmessage ArenaSaveBattleRecordReq {\n    int64 fightUin  = 1;    //挑战者Uin\n    int64 defendUin = 2;    //防守者Uin\n    bool isWin      = 3;    //战斗结果\n    int64 fightStamp = 4;    //战斗时间\n    int64 battleUid = 5;    //战斗记录Uin\n}\n\nmessage ArenaSaveBattleRecordRsp {\n}\n//请求刷新匹配\nmessage ArenaGetMatchReq {\n    bool isRefresh  = 1;    //是否刷新\n}\n\nmessage ArenaGetMatchRsp {\n    ArenaMatchData  matchInfo      = 1;   //匹配信息\n    int64   nextSettleTime         = 2;   //下次结算时间\n    int32   seasonStat             = 3;   //赛季状态\n    int32   seasonZone             = 4;   //赛季分区\n    bool    isDailySettle          = 5;   //是否每日结算\n}\n\n\n//请求竞技场对手阵容\nmessage ArenaGetOpponentFormationReq {\n    int32 opponentRank = 1; //对手排名\n    int64 opponentUin  = 2; //对手 uin\n    bool isSvr         = 3; //服务器专用字段 标识 是否是 gamesvr 的请求\n}\n\nmessage ArenaGetOpponentFormationRsp {\n    bool    isChange                    = 1;    //对手是否变化\n    BattleFormation formation           = 2;    //玩家战斗信息，包含防守信息\n    ArenaMatchData  matchInfo           = 3;    //最新匹配信息\n    int32  opponentRank                 = 4;    //匹配的rank\n    int64   fightUin                    = 5;    //对手的Uin\n}\n\n//竞技场挑战\nmessage ArenaFightReq {\n    int32           fightRank   = 1;    //对手排名\n    BattleFormation formation   = 2;    //布阵信息\n}\n\nmessage ArenaFightRsp {\n    bool    isChange            = 1;    //对手是否变化\n    int64   nextFightTime       = 2;    //下次挑战时间\n    int32   fightNum            = 3;    //挑战次数\n    string battleRecord         = 4;    //战斗信息 TOD\n    int32   highRank            = 5;    //赛季最高排名\n}\n//竞技场更新排名\nmessage ArenaSwitchRankReq {\n    int32   switchRank          = 1;    //更换的排名\n}\nmessage ArenaSwitchRankRsp {\n    ArenaMatchData matchInfo    = 1;    //最新匹配信息\n}\n\n\n//竞技场设置防守阵容\nmessage ArenaSetDefenseReq {\n    ArenaDefenseFormation defenseFormation = 1;    //设置阵容\n}\n\nmessage ArenaSetDefenseRsp {\n\n}\n//获取竞技场防守阵容\nmessage ArenaGetAllDefenseReq {\n    int32 formationType = 1;  //阵容类型 enum FORMATION_TYPE\n}\nmessage ArenaGetAllDefenseRsp {\n    ArenaDefenseFormation defenseFormation = 1;   //竞技场保存的阵容数据\n    int32 formationType = 2;  //阵容类型 enum FORMATION_TYPE\n}\n\n//更新玩家镜像信息\nmessage ArenaUpdateActorMirrorReq {\n    ActorMirrorInfo info    = 1;\n}\nmessage ArenaUpdateActorMirrorRsp {\n}\n//查看竞技场排名\nmessage ArenaGetTopRankReq {\n    \n}\n\nmessage ArenaGetTopRankRsp {\n    int32   rank                            = 1;    //自己排名\n    int32 arenaMedal                        = 2;    //竞技场的勋章\n    repeated    ArenaOpponentInfo rankList  = 3;\n}\n\n\n\n\n\n\n//请求竞技场角色阵容\n//message ArenaGetRoleFormationReq {\n//    int64 uin = 1; //角色uin\n//}\n\n//message ArenaGetRoleFormationRsp {\n//    BattleActorData battleActorData   = 1;    //玩家战斗信息\n//}\n\n//刷新挑战CD\nmessage ArenaRefreshFightCDReq {\n}\n\nmessage ArenaRefreshFightCDRsp {\n    int64   nextFightTime               = 1;    //下次挑战时间\n}\n//重置挑战次数\nmessage ArenaResetFightNumReq {\n    \n}\n\nmessage ArenaResetFightNumRsp {\n    int32   fightNum                    = 1;    //挑战次数\n    int32   buyNum                      = 2;    //挑战购买次数\n}\n\n//领取赛季排名奖励\nmessage ArenaGetRankRewardReq {\n    int32   rewardId        = 1;\n    int32 rewardType        = 2;    //领奖类型 ARENA_REWARD_TYPE\n}\n\nmessage ArenaGetRankRewardRsp {\n    repeated ItemTuple goods            = 1;    //奖励列表\n    repeated int32   rewardList         = 2;    //赛季已领奖id\n}\n\n\n\n\n\n//获取所有徽章\nmessage GetAllBadgesReq {\n}\n\nmessage GetAllBadgesRsp {\n    repeated BadgeInfo badges = 1;\n    int64 syncKey             = 2;\n}\n\n//给角色穿戴徽章\nmessage WearBadgeReq {\n    repeated int64 badgeUidLst = 1;\n    int32 cardId               = 2;\n}\n\nmessage WearBadgeRsp {\n    repeated BadgeInfo badgeInfos = 1;  //穿戴徽章后,更新徽章信息\n    repeated CardInfo cardInfos   = 2;  //穿戴徽章后,更新角色信息\n}\n\n//取下徽章\nmessage TakeoffBadgeReq {\n    int32 cardId               = 1;\n    repeated int64 badgeUidLst = 2;\n}\n\nmessage TakeoffBadgeRsp {\n    repeated BadgeInfo badgeInfo = 1;    //取下徽章后,更新徽章和角色信息\n    CardInfo cardInfo            = 2;\n}\n\n//徽章升级\nmessage LevelupBadgeReq {\n    int64 badgeUid                  = 1;\n    map<int64, int32> itemUid2Count = 2;    //消耗的物品 itemUid -> count\n}\n\nmessage LevelupBadgeRsp {\n    BadgeInfo badgeInfo = 1;    //取消徽章后,更新徽章和角色信息\n    CardInfo cardInfo   = 2;\n}\n\n//分解徽章\nmessage DecomposeBadgeReq {\n    bool all                   = 1;\n    repeated int64 badgeUidLst = 2;\n}\n\nmessage DecomposeBadgeRsp {\n    repeated int64 delBadgeUidLst  = 1;    //删除这些徽章\n    repeated ItemTuple gainItems   = 2;    //分解后获得的物品\n}\n\nmessage SetBadgeLockStateReq {\n    int64 badgeUid = 1;\n    bool locked    = 2; //是否锁定\n}\n\nmessage SetBadgeLockStateRsp {\n    int64 badgeUid = 1;\n    bool locked    = 2; //是否锁定\n}\n\n//新获得徽章通知\nmessage NewBadgeNotify {\n    repeated BadgeInfo badges = 1;    //新增的徽章\n    int64 syncKey             = 2;\n}\n\n//清除徽章的 new 标识\nmessage ClearBadgeNewTagReq {\n    repeated int64 badgeUidLst = 1; //徽章 uid 列表\n    bool clearAll              = 2; //清除所有\n}\n\nmessage ClearBadgeNewTagRsp {\n    repeated int64 badgeUidLst = 1; //徽章 uid 列表\n    bool clearAll              = 2; //清除所有\n}\n\n//请求交换 2 个角色的徽章\nmessage SwitchBadgeReq {\n    int32 cardId1   = 1;\n    int32 cardId2   = 2;\n    repeated int32 badgeTypes = 3;   //交换的部位\n}\n\nmessage SwitchBadgeRsp {\n    repeated BadgeInfo badgeInfos = 1;  //交换徽章后,更新徽章信息\n    repeated CardInfo cardInfos   = 2;  //交换徽章后,更新角色信息\n}\n\n\n\nmessage SkillLevel {\n    int32 skillId   = 1;\n    int32 level     = 2;\n}\n\n//战斗单位，可能是卡片或建筑\nmessage BattleUnitInit {\n    int64 uid                       = 1;    //唯一标识\n    int64 uin                       = 2;    //所属角色唯一标识\n    int32 id                        = 3;    //配置id\n    int32 pos                       = 4;    //位置\n    int32 level                     = 5;    //等级\n    int32 quality                   = 6;    //突破\n    int32 grade                     = 7;    //觉醒等级\n    int32 fashionId                 = 9;    //正在使用的时装 id\n    int64 hp                        = 10;   //当前血量\n    int64 maxHp                     = 11;   //最大血量\n    repeated SkillLevel skillLevels = 12;   //技能等级信息\n    repeated int32 badgeSuitIds     = 13;   //当前生效的套装 id\n    repeated string badgeAttributes = 14;   //徽章加成的属性 attrId:initValue:extraRatio\n    repeated string rogueAttributes = 15;   //肉鸽系统: 角色属性强化加成 attrId:initValue:extraRatio\n    repeated int32 allSealIds       = 16;   //所有生效的印章 仅在使用别人的卡时,才会有这个数据\n    repeated string sealBigAttrs    = 17;   //大印章属性 job:level:quality:addUpLevel\n    int32 handBookGrowId            = 18;   //角色图鉴养成 base_card_hand_book_grow.id\n}\n\n//战斗统计用\nmessage BattleRecordUnit {\n    int32 id                        = 1;    //配置id\n    int32 fashionId                 = 2;    //正在使用的时装 id\n    int32 quality                   = 3;    //突破\n}\n\nmessage BattleActorData {\n    int64 uin                         = 1;    //账号唯一标识，非玩家时为0\n    repeated BattleUnitInit unitList  = 2;    //队伍里的单位信息，包括卡片和建筑\n    int32   monsterGroupId            = 3;    //怪物组id\n    int32 burstId                     = 4;\n    int32 leaderCardId                = 5;    //队长角色 id\n    repeated BurstOrderSetting burstOrderSetting = 9;    //总攻技能释放顺序设置\n    repeated int32 allSealIds         = 10;   //所有穿戴的印章\n    repeated string sealBigAttrs      = 11;   //大印章属性 job:level:quality:addUpLevel\n    int32 handBookGrowId              = 12;   //角色图鉴养成 base_card_hand_book_grow.id\n}\n\n//阵容数据\nmessage BattleFormation {\n    repeated BattleUnitInit cardList         = 1;    //卡牌站位 pos -> cardInfo\n    repeated BattleUnitInit buildingList     = 2;    //建筑站位 pos -> building\n    int32 burstId                            = 3;\n    int32      mapId                         = 4;    //地图ID\n    int32 leaderCardId                = 5;    //队长角色 id\n    repeated BurstOrderSetting burstOrderSetting = 6;    //总攻技能释放顺序设置\n    repeated int32 allSealIds         = 7;   //所有穿戴的印章\n    repeated string sealBigAttrs      = 8;   //大印章属性 job:level:quality:addUpLevel\n    int32 handBookGrowId              = 9;   //角色图鉴养成 base_card_hand_book_grow.id\n}\n\n//战斗过程中释放技能数据\nmessage BattleSkillInfo {\n    int32 camp      = 1;    //技能所对应阵营\n    int32 skillId   = 2;    //技能id\n    int32 frame     = 3;    //技能释放的时间点\n    int32 burstId   = 4;    //爆裂对象id\n    repeated BurstChooseCardInfo burstChooseCardInfos = 5;  //爆裂期间选取的释放角色信息\n    int32 cardSkillStartFrame = 6;  //爆裂选取角色后开始释放技能的时间\n}\n\n//战斗过程中手动技能数据\nmessage BattleManuallySkillInfo {\n    int32 camp      = 1;    //技能所对应阵营\n    int32 skillId   = 2;    //技能id\n    float x         = 3;    //坐标x\n    float y         = 4;    //坐标y\n    float z         = 5;    //坐标z\n    int32 frame     = 6;    //技能释放的时间点\n    int32 skillLevel     = 7;    //技能等级\n    BattleManuallySkillPosition position = 8;   //技能释放位置\n}\n\n//手动释放技能的位置\nmessage BattleManuallySkillPosition {\n    int32 x         = 1;    //坐标x\n    int32 y         = 2;    //坐标y\n    int32 z         = 3;    //坐标z\n}\n\n//爆裂释放信息\nmessage BurstChooseCardInfo {\n    int64 unitUid   = 1;   //选中的卡片uid\n    int32 skillId   = 2;   //角色的爆裂技能id\n    bool alreadyDeal = 3;  //是否已处理\n    int32 chooseCostFrame = 4;  //选择耗时\n}\n\n\n//战斗过程中单位的信息记录\nmessage BattleUnitRecord {\n    int64 uid                               = 1;    //单位uid\n    int32 camp                              = 2;    //阵营\n    int32 deadTime                          = 3;    //死亡时间\n    BattleRecordUnit unitInfo               = 4;    //单位的基本信息\n    repeated BattleUnitSkillInfo skillInfos = 5;    //单位释放技能记录\n}\n\n//单位释放的技能记录\nmessage BattleUnitSkillInfo {\n    int32 id          = 1;    //技能id\n    int32 type        = 2;    //技能类型\n    int32 level       = 3;    //技能等级\n    int32 frame       = 4;    //技能释放的时间点\n}\n\n//战斗队伍状态\nmessage BattleTeamState {\n    int64 uin                           = 1;\n    repeated ObjectState cardStates     = 2;\n}\n\n//初始化数据\n//重要: 初始化数据里的所有字段禁止使用 map, 包括结构体字段的内部字段\nmessage BattleInitData {    \n    int64 seqId                     = 1;\n    int32 sceneType                 = 2;    //sp_scene.proto    enum SCENE_TYPE\n    int32 stageId                   = 3;    //关卡id\n    repeated int32 randomSeeds      = 4;    //随机数\n    BattleActorData actorLeft       = 5;    //左侧角色\n    BattleActorData actorRight      = 6;    //右侧角色\n    BattleActorData neutral         = 7;    //中立\n    int64   enemyUin                = 8;    //对手Uin\n    int32   mapId                   = 9;    //地图ID\n    int32 powerDifference           = 10;   //战力差值\n    map<int32,int32> buffList       = 11;   //废弃改字段了 战斗外传入的buff列表 IntPair.key 为buff id IntPair.value 为层数\n    string extData                  = 12;   //透传参数\n    int32 specialBattleIndex        = 13;   //特殊战斗index\n    int32 limitFrame                = 14;   //战斗限时（帧数）\n    bool quickBattle                = 15;   //是否是快速战斗\n    RogueBattleData rogueData       = 16;   //肉鸽战斗数据\n    repeated IntPair buffs          = 17;   //战斗外传入的buff列表 IntPair.key 为buff id IntPair.value 为层数\n    GuildWarBattleData guildWarData = 18;  //公会战战斗数据\n    bool simulate                   = 19;   //是否是模拟战斗\n}\n\n//肉鸽战斗相关数据 里面的字段数据必须避免使用 map 结构\nmessage RogueBattleData {\n    int32 difficultyId                = 1;    //肉鸽难度id, 取 base_rogue_difficulty 表 buff_list\n    repeated int32 rogueTreasureIds   = 2;    //肉鸽宝物\n    repeated int32 rogueHolyIds       = 3;    //肉鸽圣物\n    repeated int32 rogueTalentIds     = 4;    //肉鸽天赋\n    repeated IntPair aliveCardCounts  = 5;    //存活角色各职业数量 IntPair.key 为职业类型 IntPair.value 为角色数量\n    int32 tokenCount                  = 6;    //当前代币数量\n    int32 consumeAttribPoint          = 7;    //当前消耗的属性点\n    repeated int32 buffIds            = 8;    //额外生效的 buff\n    int32 chapterId                   = 9;    //当前层的章节 id\n}\n\n//公会战战斗相关数据\nmessage GuildWarBattleData {\n    repeated SkillLevel guildWarSkills  = 1; //携带的战术技能\n    int32 compensateUid                 = 2; //补偿阵容uid  0:表示不使用补偿战斗\n    int32 compensateTime                = 3; //补偿战斗时长\n    repeated CardSimple assistCardInfos = 4; //使用的助战角色  非补偿战斗需要上传\n    int32 round                         = 5; //当前轮次\n}\n\n//客户端请求准备战斗, 获取战斗初始化数据\nmessage PrepareBattleReq { \n    int32 sceneType                 = 1;    //sp_scene.proto    enum SCENE_TYPE\n    int32 stageId                   = 2;    //关卡id\n    map<int64, int32> cardUid2Pos   = 3;    //卡牌站位 cardUid -> pos\n    map<int64, int32> buildUid2Pos  = 4;    //建筑站位 buildUid -> pos\n    string extData                  = 5;    //透传参数 (探险队领地战斗事件 eventId|nodeId|storyId|nextNodeId|nextNodeCoordinate)\n    repeated BattleArrayData specialArray= 8;    //特殊布阵信息（当前远征使用）\n    int32 leaderCardId              = 9;    //队长角色 id\n    int64 arenaOpponentUin          = 10;   //竞技场: 挑战的对手uin\n    bool arenaForceRank             = 11;   //竞技场: 如果挑战的名次对手uin变了,是否强制挑战改排名\n    int32 prepareStoreSceneType     = 12;   //战斗阵容保存类型 enum SCENE_TYPE\n    repeated BurstOrderSetting burstOrderSetting = 13;    //总攻技能释放顺序设置\n    bool quickBattle                = 14;   //是否是快速战斗\n    GuildWarBattleData guildWarData = 15;  //公会战战斗数据\n    bool simulate                   = 16;   //是否是模拟战斗\n}\n\nmessage PrepareBattleRsp {\n    BattleInitData  initData        = 1;    //战斗初始化数据\n    string initMd5                  = 2;    //初始化数据 md5 值\n}\n\n//战斗结算消息\nmessage BattleCompleteData {\n    BattleInitData initData                  = 1;    //战斗初始化服务器下发数据\n    repeated UnitDamageInfo unitDamage       = 2;    //战斗单位的伤害信息统计\n    BattleTeamState teamState1               = 3;    //战斗结束后左边队伍卡牌状态\n    BattleTeamState teamState2               = 4;    //战斗结束后右边队伍卡牌状态\n    repeated BattleSkillInfo skillInfos      = 5;    //战斗中徽章技能的释放\n    repeated BattleUnitRecord unitRecords    = 6;    //战斗中单位信息记录\n    int32 totalFrame                         = 7;    //战斗耗时 帧\n    int32 killMobCount                       = 8;    //击杀魔物数量\n    ChallengeResultData challengeResultData  = 9;    //记录战斗的挑战数据(特殊战斗使用)\n    bool damageDiff                          = 10;   //客户端和战斗服务器计算的伤害值是否有差异\n    int32 totalTime                          = 11;   //战斗总时长(秒)\n    int32 leftTime                           = 12;   //战斗剩余时长(秒)\n    repeated BattleManuallySkillInfo manuallySkillInfos      = 13;    //战斗中手动技能的释放\n    repeated ManuallySkillDamageInfo manuallySkillDamage     = 14;    //手动技能的伤害记录\n}\n\n//战斗伤害统计，手动技能\nmessage ManuallySkillDamageInfo {\n    int32 skillId                   = 1;    //技能id\n    int32 camp                      = 2;    //阵营\n    int64 damage                    = 3;    //伤害\n    int64 treat                     = 4;    //治疗\n    int32 activeCount               = 5;    //技能释放次数\n    int32 skillEffectType           = 6;    //技能效果类型（用来却分增减益）\n    int32 skillLevel                = 7;    //技能等级\n    int64 shield                    = 8;    //护盾\n}\n\n//战斗伤害统计，单位\nmessage UnitDamageInfo {\n    int64 uid                       = 1;    //单位uid\n    int32 camp                      = 2;    //阵营\n    int64 damage                    = 3;    //伤害\n    int64 damaged                   = 4;    //承受伤害\n    int64 treat                     = 5;    //治疗\n    int64 treated                   = 6;    //承受治疗\n    int32 deadTime                  = 7;    //死亡时间\n    BattleRecordUnit unitInfo       = 8;   //单位的基本信息\n    int64 killedByUid               = 9;   //记录击杀自己的单位\n}\n\n//手动挑战关卡\nmessage ChallengeStageReq {\n    int64 seqId                         = 1;\n    int32 stageId                       = 2;    //关卡id\n    int32 sceneType                     = 3;    //sp_scene.proto    enum SCENE_TYPE\n    bool win                            = 4;    //是否通关\n    BattleCompleteData battleData       = 5;    //战斗产生的数据（客户端传来的）\n    bool abort                          = 6;    //是否中途退出\n    int32 costTime                      = 7;    //战斗耗时 秒\n    string clientVersion                = 8;    //客户端版本号\n    string initMd5                      = 9;    //初始化数据 md5 值\n}\n\nmessage ChallengeStageRsp {\n    int32 stageId                       = 1;    //关卡id\n    int32 sceneType                     = 2;    //sp_scene.proto    enum SCENE_TYPE\n    bool win                            = 3;    //是否通关\n    StageInfo info                      = 4;    //通关后,更新关卡信息\n    int32 currentChapter                = 5;    //当前开启的章节\n    repeated ItemTuple FirstItemDrops   = 6;    //首次通关，关卡掉落\n    repeated ItemTuple itemDrops        = 7;    //关卡掉落\n    BattleCompleteData battleData       = 8;    //战斗产生的数据（战斗服传来的）\n\n    int32 level                         = 9;    //团队等级\n    int32 exp                           = 10;   //团队经验\n    bool firstPass                      = 11;   //是否为首次通关\n    BattleInitData  nextInitData        = 12;   //特殊战斗下一场战斗初始化数据\n\n    //额外数据 远征战斗(sproto_datamodel.ExpeditionStateRecord)\n    //肉鸽战斗 RogueNodeBattleResult\n    //公会战战斗 GuildWarBattleResult\n    bytes extData                       = 13;\n    repeated ItemTuple activityDrops    = 14;   //活动掉落\n}\n\n//保存关卡阵容\nmessage SaveStagePrepareInfoReq {\n    int32 prepareStoreSceneType         = 1;    //sp_scene.proto    enum SCENE_TYPE\n    map<int64, int32> cardUid2Pos       = 3;    //卡牌站位 cardUid -> pos\n    map<int64, int32> buildUid2Pos      = 4;    //建筑站位 buildUid -> pos\n    int32 leaderCardId                  = 5;    //队长角色 id\n    repeated BurstOrderSetting burstOrderSetting = 6;    //总攻技能释放顺序设置\n}\n\nmessage SaveStagePrepareInfoRsp {\n}\n\n//获取上次挑战的阵容信息\nmessage GetStagePrepareInfoReq {\n    int32 sceneType = 1;    //sp_scene.proto    enum SCENE_TYPE\n    int32 stageId   = 2;    //关卡 id (竞技场传 0)\n    string extData  = 3;    //透传信息\n    int32 prepareStoreSceneType = 4;    //战斗阵容存储类型\n    bool quickBattle = 5;   //是否是快速战斗\n    int32 guildWarCompensateUid = 6;    //公会战 使用的补偿阵容uid\n    bool simulate               = 7;   //是否是模拟战斗\n}\n\nmessage GetStagePrepareInfoRsp {\n    StagePrepareInfo info       = 1;\n    BattleTeamState teamState1  = 2;    //战斗结束后左边队伍卡牌状态\n    BattleTeamState teamState2  = 3;    //战斗结束后右边队伍卡牌状态\n    string extData              = 4;    //透传信息\n    bool quickBattle = 5;   //是否是快速战斗\n    int32 guildWarCompensateUid = 6;    //公会战 使用的补偿阵容uid\n    int32 guildWarCompensateTime= 7;    //公会战 使用的补偿阵容的补偿时长\n    repeated CardSimple guildWarAssistCardInfos = 8;  //公会战 可助战角色信息\n}\n\n//退出布阵界面\nmessage ExitStagePrepareReq {\n    int32 sceneType = 1;\n    int32 guildWarBossIndex = 2;    //公会战 boss 位置索引\n}\n\nmessage ExitStagePrepareRsp {\n}\n\n//好友切磋,获取对方的防守阵容\nmessage GetFriendDefenceFormationReq {\n    int32 opponentUin = 1;\n}\n\nmessage GetFriendDefenceFormationRsp {\n    int32 opponentUin           = 1;\n    BattleFormation formation   = 2;\n}\n\n//获取战斗回放数据\nmessage GetBattleRecordReq {\n    int64 battleUid     = 1;\n}\n\nmessage GetBattleRecordRsp {\n    BattleRecord record = 1;\n}\n\nenum BATTLE_CHALLENGE_CONDITION {\n    BCC_NONE                = 0;\n    REMAIN_TIME             = 1;    //剩余时间\n    DEAD_COUNT              = 2;    //阵亡角色人数\n    DEAD_JOB_COUNT          = 3;    //阵亡角色中指定职业人数\n    EMBATTLE_COUNT          = 4;    //上阵角色人数\n    EMBATTLE_JOB_COUNT      = 5;    //上阵角色中指定职业人数\n    MIN_HP_JOB              = 6;    //指定职业的最低血量（万分比）\n    HP_PERCENT              = 7;    //总血量比例（万分比）\n}\n\nmessage ChallengeResultData {\n    int32 remainTime                             = 1;    //剩余时间\n    repeated ChallengeResultCard deadInfos       = 2;    //角色死亡情况（分职业统计）\n    repeated ChallengeResultCard embattleInfos   = 3;    //角色上阵情况（分职业统计）\n    repeated ChallengeResultCard minHpInfos      = 4;    //角色最低血量情况（万分比）（分职业统计）\n    int32 remainHpPercent                        = 5;    //剩余总血量（万分比）\n    int32 remainFrames                           = 6;    //剩余时间（帧数）\n    map<int32,int32>    buffList                 = 7;    //buff列表 ID->增加的层数\n    int32               score                    = 8;    //积分\n}\n\nmessage ChallengeResultCard {\n    int32 job              = 1;    //职业\n    int32 value            = 2;    //对应数据\n}\n\n\n\nmessage RewardLvShow {\n    int32       passId                  = 1;\n    repeated int32 rewardLvs            = 2;\n}\n\nmessage BattlePassShowInfo {\n    int32 passPortId                    = 1;    //通行证ID\n    bool isUnLock                       = 2;    //是否解锁\n    int32 lv                            = 3;    //当前等级\n    int32 exp                           = 4;    //当前经验\n    int32   expLimit                    = 5;    //经验限制进度\n    repeated    int32       openList    = 6;    //开启的子通行证\n    repeated TaskInfo dailyTask         = 7;    //每日任务\n    repeated TaskInfo weeklyTask        = 8;    //每周任务\n    repeated TaskInfo totalTask         = 9;    //当前任务\n    repeated RewardLvShow      rewards  = 10;    //领奖信息 passId->领奖状态\n    int64                     endStamp  = 11;   //到期时间\n}\n//请求通行证信息\nmessage GetBattlePassInfoReq {\n    \n}\nmessage GetBattlePassInfoRsp {\n    repeated BattlePassShowInfo info  = 1;\n}\n\n//通行证任务刷新\nmessage BattlePassTaskRefreshReq {\n    int32 phaseId               = 1;    //通行证期数  \n    int64 taskUid               = 2;    //任务uID\n}\nmessage BattlePassTaskRefreshRsp {\n    repeated TaskInfo taskList              = 1;    //当前的任务列表\n    map<int32,int32>      taskLimits        = 2;    //剩余的任务次数\n}\n//通行证任务领奖\nmessage BattlePassTaskRewardReq {\n    int32 phaseId               = 1;    //通行证期数  \n    int64 taskUid               = 2;    //任务uID\n}\nmessage BattlePassTaskRewardRsp {\n    int32 exp               = 1;    //奖励的经验\n    BattlePassShowInfo info = 2;         \n}\n\n\n//通行证等级购买\nmessage BattlePassBuyLevelReq {\n    int32 phaseId               = 1;    //通行证期数  \n    int32 buyLevel              = 2;    //购买等级\n}\nmessage BattlePassBuyLevelRsp {\n    int32 phaseId               = 1;    //通行证期数  \n    int32 level                 = 2;    //当前等级\n}\n//通行证奖励领取\nmessage BattlePassGetRewardReq {\n    int32 phaseId               = 1;    //通行证期数\n    int32 passId                = 2;    //子通行证ID\n    int32 rewardLv              = 3;    //领奖等级\n    bool  rewardAll             = 4;    //是否全部领取\n}\nmessage BattlePassGetRewardRsp {\n    repeated ItemTuple goods    = 1;    //领取的奖励\n    BattlePassShowInfo info     = 2;\n}\n\nmessage BattlePassBuySuccessNotify {\n    repeated BattlePassShowInfo allBattlePass = 1;\n}\n//boss挑战\n\n\n\n\n\n\n\nmessage BossRankInfo {\n    int64 uin       = 1;\n    int32 rank      = 2;\n    int32 rankRatio = 3;\n}\n//获取boss挑战信息\nmessage GetBossInfoReq {\n    \n}\n\nmessage GetBossInfoRsp {\n    int32   season          = 1;    //当前赛季\n    int64 endStamp          = 2;    //结束时间\n    int64 nextStartStamp    = 3;    //下期开始时间\n    int32 fighterCount      = 4;    //普通挑战次数\n    int32 challengeCount    = 5;    //高难挑战次数\n    int64 highScore         = 6;    //最高积分 \n    int32   curChapter      = 7;    //当前章节\n    int32   curStage        = 8;    //当前关卡\n    int64   bossHpMax       = 9;   //boss上限血量\n    int64   bossHpCur       = 10;   //boss当前血量\n    int32 rank              = 11;   //排名 绝对排名\n    int32 rankRatio         = 12;   //排名 万分比\n    repeated BossChallengeRecord challenge   = 13;    //当前挑战数据\n    bool isStart            = 14;\n    repeated int32  rewardStages             = 15;  //已领取奖励\n    int32 highScoreDiff     = 16;\n    int32 phase             = 17;   //发奖周期\n}\n\n//玩家排行信息\nmessage BossRankActorInfo {\n    int64 uin                   = 1;\n    int32 level                 = 2;    //等级\n    int32 faceId                = 3;    //头像ID\n    string name                 = 4;    //名字\n    int64 guildUid              = 5;    //所在公会 uid\n    string guildName            = 6;    //所在公会名字\n    int32   rank                = 7;    //排行\n    int64 score                 = 8;    //积分\n    int32 scoreDiff             = 9;\n    ActorHead actorHead         = 10;   //头像信息\n}\n\n//获取boss排行榜信息\nmessage GetBossTopRankReq {\n    int32 index = 1;    //\n}\n\nmessage GetBossTopRankRsp {\n    int32       rank                        = 1;    //自己排名\n    int32 rankRatio                         = 2;\n    repeated    BossRankActorInfo rankList  = 3;\n    int32 index                             = 4;\n    int32 rankCount                         = 5;    //榜单人数\n}\n//开始挑战\nmessage StartBossChallengeReq {\n}\nmessage StartBossChallengeRsp {\n}\n//放弃挑战\nmessage GiveupBossChallengeReq {\n    int32 stage = 1;\n}\n\nmessage GiveupBossChallengeRsp {\n\n}\n//积分变化通知\nmessage BossChallengeHighScoreNotify {\n    int32 curRank       = 1;\n    int32 curRankRatio  = 2;\n    int32 upRank        = 3;\n    int64 highScore     = 4;\n    int32 highScoreDiff = 5;\n}\n\n//领取奖励\nmessage RewardBossChallengeReq {\n    int32 stage = 1;  \n}\n\nmessage RewardBossChallengeRsp {\n    repeated DropTuple rewards    = 1;    //奖励列表\n    repeated int32  rewardStages  = 2;  //已领取奖励\n}\n\n//获取boss排行榜玩家挑战信息\nmessage GetBossRankActorRecordReq {\n    int64 uin       = 1;    //uin\n}\n\nmessage GetBossRankActorRecordRsp {\n    int64 uin   = 1;\n    repeated BossChallengeRecord challenges = 2;\n}\n\nmessage CacheChallengeRecord {\n    repeated BossChallengeRecord challenges   = 1;    //当前挑战数据\n}\n\nmessage BossChallengeInfo {\n    int32 season        = 1;\n    int64 startTime     = 2;\n    int64 endTime       = 3;\n    int64 endStartTime  = 4;\n    int32 chapter       = 5;\n    int32 settle        = 6;\n    int32 rewardCount   = 7;\n    int32 rewardCycle   = 8;\n    \n}\n\n\n\n\n//获取所有卡牌\nmessage GetAllCardsReq {\n    int64 syncKey = 1;  //重新登录后发 0\n}\n\n\nmessage GetAllCardsRsp {\n    repeated CardInfo cardList  = 1;\n    int64 syncKey               = 2;    //客户端更新本地的 syncKey\n}\n\n\n//卡牌状态更新通知\nmessage CardUpdateNotify {\n    repeated CardInfo addCardList   = 1;    //新增的卡牌\n    repeated int64 delCardUidList   = 2;    //需要删除的卡牌列表\n    int64 syncKey                   = 3;    //客户端更新本地的 syncKey\n}\n\n//卡牌升级\nmessage LevelupCardReq {\n    int32 cardId                    = 1;\n    map<int64, int32> itemUid2Count = 2;    //消耗的物品 itemUid -> count\n}\n\nmessage LevelupCardRsp {\n    CardUpdate updateInfo = 1;\n}\n\n//卡牌突破\nmessage QualityUpCardReq {\n    int32 cardId = 1;\n}\n\nmessage QualityUpCardRsp {\n    CardUpdate updateInfo = 1;\n}\n\n\n//卡牌技能升级\nmessage LevelupCardSkillReq {\n    int32 cardId  = 1;\n    int32 skillId = 2;\n}\n\nmessage LevelupCardSkillRsp {\n    CardUpdate updateInfo = 1;\n}\n\n//卡牌觉醒\nmessage GradeUpCardReq {\n    int32 cardId = 1;\n}\n\nmessage GradeUpCardRsp {\n    CardUpdate updateInfo = 1;\n}\n\n//卡牌多次觉醒\nmessage MultiGradeUpCardReq {\n    int32 cardId = 1;\n}\n\nmessage MultiGradeUpCardRsp {\n    CardUpdate updateInfo = 1;\n}\n\nmessage GetCardAllTeamReq {\n\n}\n\nmessage GetCardAllTeamRsp {\n    repeated CardTeamInfo teams = 1;\n}\n\nmessage SetCardTeamReq {\n    int32 teamId            = 1;\n    repeated int32 cardIds  = 2;\n    string name             = 3;\n}\n\nmessage SetCardTeamRsp {\n    CardTeamInfo teamInfo   = 1;\n}\n\nmessage ChangeCardTeamNameReq {\n    int32 teamId = 1;\n    string name  = 2;\n}\n\nmessage ChangeCardTeamNameRsp {\n    CardTeamInfo teamInfo   = 1;\n}\n\nmessage ChangeCardFashionReq {\n    int32 cardId    = 1;\n    int32 fashionId = 2;\n}\n\nmessage ChangeCardFashionRsp {\n    CardUpdate updateInfo = 1;\n}\n\nmessage GetAllShowFashionReq {\n}\n\nmessage GetAllShowFashionRsp {\n    repeated int64 fashionIds = 1;\n}\n\n//给角色投递卡牌刷新事件\nmessage EventRefreshCardSkill {\n    int32 cardId    = 1;\n    int32 skillId   = 2;\n}\n\nmessage GetAllCardFashionReq {\n}\n\nmessage GetAllCardFashionRsp {\n     map<int32, int64>  ownFashions = 1;\n}\n\n//领取图鉴奖励: 领取成功后客户端修改本地所有角色数据: CardInfo.handBookReward 设置为 true\nmessage FetchHandBookRewardReq {\n}\n\nmessage FetchHandBookRewardRsp {\n    repeated ItemTuple rewards = 1;\n}\n\n//激活图鉴成长\nmessage ActivateHandBookGrowReq {\n    int32 handBookGrowId = 1;\n}\n\nmessage ActivateHandBookGrowRsp {\n    ActorInfo info = 1;\n}\n\n//角色点击事迹上报\nmessage ClickCardStoryEventReportReq {\n    repeated CardClickedStoryEventInfo infos = 1;\n}\n\nmessage ClickCardStoryEventReportRsp {\n}\n\n//获取所有角色已点击事迹\nmessage GetCardClickedStoryEventsReq {\n}\n\nmessage GetCardClickedStoryEventsRsp {\n    repeated CardClickedStoryEventInfo infos = 1;\n}\n\n//查看别人的角色信息\nmessage GetOtherCardInfoReq {\n    int64 targetUin  = 1;\n    int64 cardUid    = 2;\n}\n\nmessage GetOtherCardInfoRsp {\n    CardInfo cardInfo               = 1;\n    repeated BadgeInfo badgeInfos   = 2;    //角色穿戴的徽章\n    repeated int32 allSealIds       = 3;    //所有生效的印章\n    repeated string sealBigAttrs    = 4;   //大印章属性 job:level:quality:addUpLevel\n    int32 handBookGrowId            = 5;    //角色图鉴养成 base_card_hand_book_grow.id\n}\n\nmessage CardRobotTestInitialReq {\n    repeated int32 cardIds = 1;\n    int32 mainLineStageId  = 2;\n}\n\nmessage CardRobotTestInitialRsp {\n    repeated CardInfo cardInfos = 1;\n}\n\n//设置角色关注\nmessage SetCardFocusReq {\n    int32 cardId = 1;   //清除所有角色的关注\n    bool focus   = 2;   //是否关注, 如果要清楚所有角色的关注: cardId = 0, focused = false\n}\n\nmessage SetCardFocusRsp {\n    int32 cardId = 1;\n    bool focus   = 2;\n}\n\n//设置看板娘角色展示\nmessage SetCardFashionShowReq {\n    repeated int32 showFashionIds = 1;  //最多 5 个值\n}\n\nmessage SetCardFashionShowRsp {\n    ActorInfo actor = 1;\n}\n\n\n\n\nmessage CarnivelStageShow {\n    int32 stageId                   = 1;\n    repeated TaskInfo taskList      = 2;    //当前任务列表\n}\n//请求通行证信息\nmessage GetCarnivalInfoReq {\n    int64 refreshStamp                          = 1;  \n}\nmessage GetCarnivalInfoRsp {\n    repeated CarnivelStageShow stageList        = 1;    //阶段信息\n    repeated int32 rewardTragets                = 2;    //已经领奖的目标\n    int64        closedStamp                    = 3;   //关闭时间\n    int64 refreshStamp                          = 4;  \n}\n\n\n\n//通行证奖励领取\nmessage CarnivalGetRewardReq {\n    int64 taskUid   = 1;    //领奖任务\n    int32  rewardId = 2;    //领奖目标\n}\nmessage CarnivalGetRewardRsp {\n    repeated DropTuple goods                    = 1;    //领取的奖励\n    repeated CarnivelStageShow stageList        = 2;    //阶段信息\n    repeated int32 rewardTragets                = 3;    //已经领奖的目标\n    int64        closedStamp                    = 4;   //关闭时间\n}\n\n\n\nmessage Head {\n    uint32 cmd          = 1;\n    int64 uin           = 2;\n    uint32 sequence     = 3;\n    int32 retCode       = 4;\n    string openId       = 5;\n    string gtwId        = 6;\n    string gameId       = 7;\n    string dbId         = 8;\n    string reply        = 9;\n    string serviceId    = 10;\n    bytes trace         = 11;\n    int32 platform      = 12;   //enum PLATFORM_TYPE\n    string errMsg       = 13;   //错误信息\n    bool resend         = 14;   //重发的请求\n}\n\nmessage Msg {\n    Head head  = 1;\n    bytes body = 2;\n}\n\nmessage KvPair {\n    string key      = 1;\n    string strValue = 2;\n    int64 intValue  = 3;\n}\n\nmessage IntPair {\n    uint32 key      = 1;\n    int64 value     = 2;\n}\n\nmessage Position {\n    int32 x = 1;\n    int32 y = 2;\n}\nenum SpecialItemId {\n    SID_NONE             = 0;\n    SID_BIND_DIAMOND     = 21000001; //绑定钻石\n    SID_DIAMOND          = 21000002; //钻石\n    SID_GOLD             = 21000003; //金币\n    SID_ENERGY           = 21000004; //体力\n    SID_ROLE_EXP         = 21000005; //主角经验\n    SID_BATTLEPASS_EXP   = 21000007; //主角经验\n    SID_GACHA1           = 21100001; //单抽券\n    SID_GACHA10          = 21100002; //十连券\n    SID_UP_GACHA1        = 21100004; //up 单抽券\n    SID_UP_GACHA10       = 21100003; //up 十连券\n    SID_MANOR_ACTION_VALUE  = 21000009;   //探险地图行动值\n    SID_MANOR_PLOT_VALUE    = 21000013;   //探险地图支线剧情点\n    SID_BOSS_CHALLENGE      = 21000014;   //BOSS挑战次数\n    SID_GUILD_EXP        = 21000016; //公会经验\n    SID_MONTH_CARD_ITEM  = 21000017; //月卡功能道具\n    SID_BATTLE_PASS_101  = 21000018; //秘银凭证道具\n    SID_BATTLE_PASS_102  = 21000019; //黑耀凭证道具\n    SID_SHOP_TOKEN_A     = 21000201; //商店代币A\n    SID_SHOP_TOKEN_B     = 21000202; //商店代币B\n    SID_DISPATCH_EXP     = 21000022; //派遣经验\n    SID_GUILD_WAR_SKILL_POINT = 21000021;   //公会战技能点\n    SID_SEAL_HOOK_EXP    = 21000030; //大刻印挂机经验\n}\nenum CMD {\n    NONE                                = 0;\n    REQ_RSP_INTERVAL                    = 100000;\n\n    DB_START                            = 100;\n    DB_QUERY_UNIQUE_DATA_REQ            = 101;      //DbQueryUniqueDataReq\n    DB_QUERY_UNIQUE_DATA_RSP            = 100101;   //DbQueryUniqueDataRsp\n    DB_QUERY_BATCH_DATA_REQ             = 102;      //DbQueryBatchDataReq\n    DB_QUERY_BATCH_DATA_RSP             = 100102;   //DbQueryBatchDataRsp\n    DB_DELETE_DATA_REQ                  = 103;      //DbDeleteDataReq\n    DB_DELETE_DATA_RSP                  = 100103;   //DbDeleteDataRsp\n    DB_INSERT_DATA_REQ                  = 104;      //DbInsertDataReq\n    DB_INSERT_DATA_RSP                  = 100104;   //DbInsertDataRsp\n    DB_UPDATE_DATA_REQ                  = 105;      //DbUpdateDataReq\n    DB_UPDATE_DATA_RSP                  = 100105;   //DbUpdateDataRsp\n    DB_UPDATE_BATCH_DATA_REQ            = 106;      //DbUpdateBatchDataReq\n    DB_UPDATE_BATCH_DATA_RSP            = 100106;   //DbUpdateBatchDataRsp\n    DB_CREATE_INDEX_REQ                 = 107;      //DbCreateIndexReq\n    DB_CREATE_INDEX_RSP                 = 100107;   //DbCreateIndexRsp\n    DB_ALLOC_GAME_REQ                   = 108;      //AllocGameReq\n    DB_ALLOC_GAME_RSP                   = 100108;   //AllocGameRsp\n    DB_QUERY_COUNT_REQ                  = 109;      //DbQueryCountReq\n    DB_QUERY_COUNT_RSP                  = 100109;   //DbQueryCountReq\n    DB_TRANSACTION_OP_REQ               = 110;      //DbTransactionOpReq\n    DB_TRANSACTION_OP_RSP               = 100110;   //DbTransactionOpRsp\n    DB_UPSERT_DATA_REQ                  = 111;      //DbUpsertDataReq\n    DB_UPSERT_DATA_RSP                  = 100111;   //DbUpsertDataRsp\n\tDB_TABLE_DROP_REQ                  \t= 112;      //DbTableDropReq\n    DB_TABLE_DROP_RSP                  \t= 100112;   //DbTableDropRsp\n    DB_QUERY_UNIQUE_AND_UPDATE_REQ      = 113;      //DbQueryOneAndUpdateReq\n    DB_QUERY_UNIQUE_AND_UPDATE_RSP      = 100113;   //DbQueryOneAndUpdateRsp\n    DB_END                              = 199;\n\n    SYS_START                           = 200;\n    SYS_GET_RES_VERSION_REQ             = 202;      //GetResVersionReq\n    SYS_GET_RES_VERSION_RSP             = 100202;   //GetResVersionRsp\n    SYS_ACTOR_INFO_UPDATED_REQ          = 204;      //SysActorInfoUpdatedReq\n    SYS_ACTOR_INFO_UPDATED_RSP          = 100204;   //SysActorInfoUpdatedRsp\n    SYS_EXIT_LUA_VM_REQ                 = 205;\n    SYS_EXIT_LUA_VM_RSP                 = 100205;\n    SYS_HOT_LOAD_REQ                    = 206;\n    SYS_HOT_LOAD_RSP                    = 100206;\n    SYS_RECHARGE_ORDER_DELIVERY_REQ     = 207;      //SysRechargeOrderDeliveryReq\n    SYS_RECHARGE_ORDER_DELIVERY_RSP     = 100207;   //SysRechargeOrderDeliveryRsp\n    SYS_INCR_GUILD_EXP_REQ              = 208;      //IncrGuildExpReq\n    SYS_KICK_OFF_USER_FROM_GAME_REQ     = 209;      //KickOffUserFromGameReq\n    SYS_KICK_OFF_USER_FROM_GAME_RSP     = 10209;    //KickOffUserFromGameRsp\n    SYS_UPDATE_GUILD_MEMBER_NAME_REQ    = 210;      //SysUpdateGuildMemberNameReq\n    SYS_RECHARGE_ORDER_REFUND_REQ       = 211;      //SysRechargeOrderRefundReq\n    SYS_RECHARGE_ORDER_REFUND_RSP       = 100211;   //SysRechargeOrderRefundRsp\n    SYS_GUILD_WAR_SETTLE_REQ            = 212;      //SysGuildWarBattleSettleReq\n    SYS_GUILD_WAR_SETTLE_RSP            = 100212;   //SysGuildWarBattleSettleRsp\n    SYS_GUILD_WAR_GET_PROGRESS_REQ      = 213;      //SysGetGuildWarProgressReq\n    SYS_GUILD_WAR_GET_PROGRESS_RSP      = 100213;   //SysGetGuildWarProgressRsp\n    SYS_ADD_GUILD_HEAD_REQ              = 214;      //SysAddGuildHeadReq\n    SYS_ADD_GUILD_HEAD_RSP              = 100214;   //SysAddGuildHeadRsp\n    SYS_CHECK_OWN_EMOJI_REQ             = 215;      //SysCheckOwnEmojiReq\n    SYS_CHECK_OWN_EMOJI_RSP             = 100215;   //SysCheckOwnEmojiRsp\n    SYS_END                             = 299;\n\n    GM_START                            = 300;\n    GM_SEND_GLOBAL_MAIL_REQ             = 301;      //SendGlobalMailReq\n    GM_SEND_GLOBAL_MAIL_RSP             = 100301;   //SendGlobalMailRsp\n    GM_SEND_PRIVATE_MAIL_REQ            = 302;      //SendPrivateMailReq\n    GM_SEND_PRIVATE_MAIL_RSP            = 100302;   //SendPrivateMailRsp\n    GM_FETCH_GLOBAL_MAIL_REQ            = 303;      //FetchGlobalMailReq\n    GM_FETCH_GLOBAL_MAIL_RSP            = 100303;   //FetchGlobalMailRsp\n    GM_GET_ALL_FASHIONS_REQ             = 304;      //GetAllOpFashionsReq\n    GM_GET_ALL_FASHIONS_RSP             = 100304;   //GetAllOpFashionsRsp\n    GM_GET_ALL_GIFTPACKAGE_REQ          = 305;      //GetAllGiftPackageReq\n    GM_GET_ALL_GIFTPACKAGE_RSP          = 100305;   //GetAllGiftPackageRsp\n    GM_GET_ALL_ACTICITY_REQ             = 306;      //GetAllOpActivityReq\n    GM_GET_ALL_ACTICITY_RSP             = 100306;   //GetAllOpActivityRsp\n    GM_GET_ALL_SHOP_LABEL_REQ           = 307;      //GetAllShopLabelReq\n    GM_GET_ALL_SHOP_LABEL_RSP           = 100307;   //GetAllShopLabelRsp\n    GM_END                              = 399;\n\n    NOTIFY_CLIENT_START                 = 400;\n    CARD_UPDATE_NOTIFY                  = 401;      //CardUpdateNotify\n    NEW_MESSAGE_NOTIFY                  = 402;      //NewMessageNotify\n    RELATION_CHANGED_NOTIFY             = 403;      //RelationChangedNotify\n    NEW_MAIL_NOTIFY                     = 404;      //NewMailNotify\n    KICK_OFF_NOTIFY                     = 405;      //KickOffNotify\n    MUTED_BY_SYSTEM_NOTIFY              = 406;      //MutedBySystemNotify\n    ACTOR_INFO_UPDATE_NOTIFY            = 407;      //ActorInfoUpdateNotify\n    NEW_BADGE_NOTIFY                    = 408;      //NewBadgeNotify\n    RELATION_DEL_APPLICANT_NOTIFY       = 409;      //RelationDelApplicantNotify\n    MANOR_EVENT_NOTIFY                  = 411;      //ManorEventUpdateNotify\n    GUILD_EVENT_NOTIFY                  = 412;      //GuildEventNotify\n    MANOR_CONVEY_NOTIFY                 = 413;      //ManorConveyNotify\n    MANOR_INFO_UPDATE_NOTIFY            = 414;      //ManorInfoUpdateNotify\n    BATTLEPASS_BUY_SUCCESS_NOTIFY       = 415;      //BattlePassBuySuccessNotify\n    BOSS_CHALLENGE_HIGH_SCORE           = 416;      //BossChallengeHighScoreNotify\n    ROGUE_CARD_UPDATE_NOTIFY            = 417;      //RogueCardUpdateNotify\n    FASHION_ADD_NOTIFY                  = 418;      //FashionAddNotify\n    NOTIFY_CLIENT_END                   = 499;\n\n\n    LOGIN_START                         = 1000;\n    LOGIN_AUTH_TOKEN_REQ                = 1001;     //AuthTokenReq\n    LOGIN_AUTH_TOKEN_RSP                = 101001;   //AuthTokenRsp\n    LOGIN_ENTER_GAME_REQ                = 1002;     //EnterGameReq\n    LOGIN_ENTER_GAME_RSP                = 101002;   //EnterGameRsp\n    LOGIN_KICK_OFF_REQ                  = 1003;     //KickOffReq\n    LOGIN_KICK_OFF_RSP                  = 101003;   //KickOffRsp\n    LOGIN_END                           = 1099;\n\n    ACTOR_START                         = 1100;\n    ACTOR_CREATE_ACTOR_REQ              = 1101;     //CreateActorReq\n    ACTOR_CREATE_ACTOR_RSP              = 101101;   //CreateActorRsp\n    ACTOR_GET_ACTOR_INFO_REQ            = 1102;     //GetActorInfoReq\n    ACTOR_GET_ACTOR_INFO_RSP            = 101102;   //GetActorInfoRsp\n    ACTOR_OFFLINE_REQ                   = 1104;     //OfflineReq\n    ACTOR_OFFLINE_RSP                   = 101104;   //OfflineRsp\n    ACTOR_HEART_BEAT_REQ                = 1105;     //HeartBeatReq\n    ACTOR_HEART_BEAT_RSP                = 101105;   //HeartBeatRsp\n    ACTOR_EVENT_NOTIFY_REQ              = 1106;     //EventNotifyReq\n    ACTOR_EVENT_NOTIFY_RSP              = 101106;   //EventNotifyRsp\n    ACTOR_GET_SIGN_IN_REQ               = 1107;     //GetActorSignInReq\n    ACTOR_GET_SIGN_IN_RSP               = 101107;   //GetActorSignInRsp\n    ACTOR_SIGN_IN_REQ                   = 1108;     //ActorSignInReq   \n    ACTOR_SIGN_IN_RSP                   = 101108;   //ActorSignInRsp\n    ACTOR_GM_REQ                        = 1109;     //ActorGmReq\n    ACTOR_GM_RSP                        = 101109;   //ActorGmRsp\n    ACTOR_GET_UNLOCKED_FEATURES_REQ     = 1110;     //GetUnlockedFeaturesReq\n    ACTOR_GET_UNLOCKED_FEATURES_RSP     = 101110;   //GetUnlockedFeaturesRsp\n    ACTOR_GET_EMOJI_REQ                 = 1111;     //GetEmojiReq\n    ACTOR_GET_EMOJI_RSP                 = 101111;   //GetEmojiRsp\n    ACTOR_REPORT_LATEST_EMOJI_REQ       = 1112;     //ReportLatestEmojiReq\n    ACTOR_REPORT_LATEST_EMOJI_RSP       = 101112;   //ReportLatestEmojiRsp\n    ACTOR_GET_OTHER_DETAIL_INFO_REQ     = 1113;     //GetOtherDetailInfoReq\n    ACTOR_GET_OTHER_DETAIL_INFO_RSP     = 101113;   //GetOtherDetailInfoRsp\n    ACTOR_GET_STORY_REQ                 = 1114;     //GetStoryListReq\n    ACTOR_GET_STORY_RSP                 = 101114;   //GetStoryListRsp\n    ACTOR_CHANGE_NAME_REQ               = 1115;     //ChangeNameReq\n    ACTOR_CHANGE_NAME_RSP               = 101115;   //ChangeNameRsp\n    ACTOR_SAVE_SETTINGS_REQ             = 1116;     //SaveSettingsReq\n    ACTOR_SAVE_SETTINGS_RSP             = 101116;   //SaveSettingsRsp\n    ACTOR_CHANGE_FACE_REQ               = 1117;     //ChangeFaceReq\n    ACTOR_CHANGE_FACE_RSP               = 101117;   //ChangeFaceRsp\n    ACTOR_FINISH_GUIDE_REQ              = 1118;     //FinishGuideReq\n    ACTOR_FINISH_GUIDE_RSP              = 101118;   //FinishGuideRsp\n    ACTOR_GET_GUIDE_PROGRESS_REQ        = 1119;     //GetGuideProgressReq\n    ACTOR_GET_GUIDE_PROGRESS_RSP        = 101119;   //GetGuideProgressRsp\n    ACTOR_CHECK_FEATURE_OPEN_REQ        = 1120;     //CheckFeatureOpenReq\n    ACTOR_CHECK_FEATURE_OPEN_RSP        = 101120;   //CheckFeatureOpenRsp\n    ACTOR_GET_ACTOR_MIRROR_INFO_REQ     = 1121;     //GetActorMirrorInfoReq\n    ACTOR_GET_ACTOR_MIRROR_INFO_RSP     = 101121;   //GetActorMirrorInfoRsp\n    ACTOR_FINISH_PLOT_REQ               = 1122;     //FinishPlotReq\n    ACTOR_FINISH_PLOT_RSP               = 101122;   //FinishPlotRsp\n    ACTOR_GET_ALL_FINISHED_PLOTS_REQ    = 1123;     //GetAllFinishedPlotsReq\n    ACTOR_GET_ALL_FINISHED_PLOTS_RSP    = 101123;   //GetAllFinishedPlotsRsp\n    ACTOR_GET_SELF_DETAIL_INFO_REQ      = 1124;     //GetSelfDetailInfoReq\n    ACTOR_GET_SELF_DETAIL_INFO_RSP      = 101124;   //GetSelfDetailInfoRsp\n    ACTOR_SET_PROFILE_DISPLAY_CARDS_REQ = 1125;     //SetProfileDisplayCardsReq\n    ACTOR_SET_PROFILE_DISPLAY_CARDS_RSP = 101125;   //SetProfileDisplayCardsRsp\n    ACTOR_SET_PROFILE_SHOW_RESOURCE_REQ = 1126;     //SetProfileShowResourceReq\n    ACTOR_SET_PROFILE_SHOW_RESOURCE_RSP = 101126;   //SetProfileShowResourceRsp\n    ACTOR_GET_ENERGY_RECOVER_INFO_REQ   = 1127;     //GetEnergyRecoverInfoReq\n    ACTOR_GET_ENERGY_RECOVER_INFO_RSP   = 101127;   //GetEnergyRecoverInfoRsp\n    ACTOR_CHANGE_PASSWORD_REQ           = 1128;     //ChangePasswordReq\n    ACTOR_CHANGE_PASSWORD_RSP           = 101128;   //ChangePasswordRsp\n    ACTOR_UPDATE_GUILD_OPERATE_STATE_REQ= 1129;     //UpdateGuildOperateStateReq\n    ACTOR_UPDATE_GUILD_OPERATE_STATE_RSP= 101129;   //UpdateGuildOperateStateRsp\n    ACTOR_GET_GUILD_OPERATE_STATE_REQ   = 1130;     //GetGuildOperateStateReq\n    ACTOR_GET_GUILD_OPERATE_STATE_RSP   = 101130;   //GetGuildOperateStateRsp\n    ACTOR_STORY_OPERATE_REPORT_REQ      = 1131;     //StoryOperateReportReq\n    ACTOR_STORY_OPERATE_REPORT_RSP      = 101131;   //StoryOperateReportRsp\n    ACTOR_REPORT_OPERATE_RECORD_REQ     = 1132;     //ReportOperateRecordReq\n    ACTOR_REPORT_OPERATE_RECORD_RSP     = 101132;   //ReportOperateRecordRsp\n    ACTOR_GET_OPERATE_RECORD_REQ        = 1133;     //GetOperateRecordReq\n    ACTOR_GET_OPERATE_RECORD_RSP        = 101133;   //GetOperateRecordRsp\n    ACTOR_BATCH_SYNC_RES_REQ            = 1134;     //BatchSyncResReq\n    ACTOR_BATCH_SYNC_RES_RSP            = 101134;   //BatchSyncResRsp\n    ACTOR_CHANGE_HEAD_REQ               = 1135;     //ChangeHeadReq\n    ACTOR_CHANGE_HEAD_RSP               = 101135;   //ChangeHeadRsp\n    ACTOR_USE_EXCHANGE_CODE_REQ         = 1136;     //UseExchangeCodeReq\n    ACTOR_USE_EXCHANGE_CODE_RSP         = 101136;   //UseExchangeCodeRsp\n    ACTOR_CLIENT_ABNORMAL_REPORT_REQ    = 1137;     //ClientAbnormalReportReq\n    ACTOR_CLIENT_ABNORMAL_REPORT_RSP    = 101137;   //ClientAbnormalReportRsp\n    ACTOR_OPERATE_STAR_SOUND_REQ        = 1138;     //OperateStarSoundReq\n    ACTOR_OPERATE_STAR_SOUND_RSP        = 101138;   //OperateStarSoundRsp\n    ACTOR_OPERATE_SOUND_PLAYLIST_REQ    = 1139;     //OperateSoundPlayListReq\n    ACTOR_OPERATE_SOUND_PLAYLIST_RSP    = 101139;   //OperateSoundPlayListRsp\n    ACTOR_SET_BIRTHDAY_REQ              = 1140;     //SetBirthdayReq\n    ACTOR_SET_BIRTHDAY_RSP              = 101140;   //SetBirthdayRsp\n    ACTOR_ACTIVATE_HAND_BOOK_GROW_REQ   = 1145;     //ActivateHandBookGrowReq\n    ACTOR_ACTIVATE_HAND_BOOK_GROW_RSP   = 101145;   //ActivateHandBookGrowRsp\n    ACTOR_END                           = 1199;\n\n    IM_START                            = 1200;\n    IM_SEND_MESSAGE_REQ                 = 1201;     //SendMessageReq\n    IM_SEND_MESSAGE_RSP                 = 101201;   //SendMessageRsp\n    IM_SYNC_MESSAGE_REQ                 = 1202;     //SyncMessageReq\n    IM_SYNC_MESSAGE_RSP                 = 101202;   //SyncMessageRsp\n    IM_SWITCH_WORLD_GROUP_REQ           = 1203;     //SwitchWorldGroupReq\n    IM_SWITCH_WORLD_GROUP_RSP           = 101203;   //SwitchWorldGroupRsp\n    IM_REPORT_USER_REQ                  = 1204;     //ReportUserReq\n    IM_REPORT_USER_RSP                  = 101204;   //ReportUserRsp\n    IM_SYNC_PRIVATE_HISTORY_MESSAGE_REQ = 1205;     //SyncPrivateHistoryMessageReq\n    IM_SYNC_PRIVATE_HISTORY_MESSAGE_RSP = 101205;   //SyncPrivateHistoryMessageRsp\n    IM_GET_WORLD_LINE_INFO_REQ          = 1206;     //GetWorldLineInfoReq\n    IM_GET_WORLD_LINE_INFO_RSP          = 101206;   //GetWorldLineInfoRsp\n    IM_GET_CHANNEL_NEWEST_MESSAGE_REQ   = 1207;     //GetChannelNewestMessageReq\n    IM_GET_CHANNEL_NEWEST_MESSAGE_RSP   = 101207;   //GetChannelNewestMessageRsp\n    IM_GET_PRIVATE_CHATTING_TARGET_REQ  = 1208;     //GetPrivateChattingTargetReq\n    IM_GET_PRIVATE_CHATTING_TARGET_RSP  = 101208;   //GetPrivateChattingTargetRsp\n    IM_CHANGE_PRIVATE_CHATTING_TARGET_REQ = 1209;   //ChangePrivateChattingTargetReq\n    IM_CHANGE_PRIVATE_CHATTING_TARGET_RSP = 101209; //ChangePrivateChattingTargetRsp\n    IM_GET_CHAT_STATE_REQ               = 1210;     //GetChatStateReq\n    IM_GET_CHAT_STATE_RSP               = 101210;   //GetChatStateRsp\n    IM_MARK_MESSAGE_READ_REQ            = 1211;     //MarkMessageReadReq\n    IM_MARK_MESSAGE_READ_RSP            = 101211;   //MarkMessageReadRsp\n    IM_END                              = 1299;\n\n    ITEM_START                          = 1300;\n    ITEM_GET_ITEMS_REQ                  = 1301;     //GetItemsReq\n    ITEM_GET_ITEMS_RSP                  = 101301;   //GetItemsRsp\n    ITEM_SYNC_ITEMS_REQ                 = 1302;     //SyncItemsReq\n    ITEM_SYNC_ITEMS_RSP                 = 101302;   //SyncItemsRsp\n    ITEM_BUY_COUNT_RESOURCE_REQ         = 1303;     //BuyCountResourceReq\n    ITEM_BUY_COUNT_RESOURCE_RSP         = 101303;   //BuyCountResourceRsp\n    ITEM_USE_ITEM_REQ                   = 1304;     //UseItemReq\n    ITEM_USE_ITEM_RSP                   = 101304;   //UseItemRsp\n    ITEM_SALE_ITEM_REQ                  = 1305;     //SaleItemReq\n    ITEM_SALE_ITEM_RSP                  = 101305;   //SaleItemRsp\n    ITEM_CONSUME_ITEM_REQ               = 1306;     //ConsumeItemReq\n    ITEM_CONSUME_ITEM_RSP               = 101306;   //ConsumeItemRsp\n    ITEM_CHECK_ENOUGH_REQ               = 1307;     //CheckItemEnoughReq\n    ITEM_CHECK_ENOUGH_RSP               = 101307;   //CheckItemEnoughReq\n    ITEM_EXCHANGE_CARD_FRAGMENT_REQ     = 1308;     //ExchangeCardFragmentReq\n    ITEM_EXCHANGE_CARD_FRAGMENT_RSP     = 101308;   //ExchangeCardFragmentRsp\n    ITEM_EXCHANGE_ENERGY_REQ            = 1309;     //ExchangeEnergyReq\n    ITEM_EXCHANGE_ENERGY_RSP            = 101309;   //ExchangeEnergyRsp\n    ITEM_GET_STORY_MONSTER_LIST_REQ     = 1310;     //GetStoryMonsterListReq\n    ITEM_GET_STORY_MONSTER_LIST_RSP     = 101310;   //GetStoryMonsterListRsp\n    ITEM_BATCH_USE_ITEMS_REQ            = 1311;     //BatchUseItemsReq\n    ITEM_BATCH_USE_ITEMS_RSP            = 101311;   //BatchUseItemsRsp\n    ITEM_CLICK_STORY_EVENT_REPORT_REQ   = 1312;     //ClickStoryEventReportReq\n    ITEM_CLICK_STORY_EVENT_REPORT_RSP   = 101312;   //ClickStoryEventReportRsp\n    ITEM_END                            = 1399;\n\n    CARD_START                          = 1400;\n    CARD_GET_ALL_CARDS_REQ              = 1401;     //GetAllCardsReq\n    CARD_GET_ALL_CARDS_RSP              = 101401;   //GetAllCardsRsp\n    CARD_LEVELUP_REQ                    = 1402;     //LevelupCardReq\n    CARD_LEVELUP_RSP                    = 101402;   //LevelupCardRsp\n    CARD_QUALITY_UP_REQ                 = 1403;     //QualityUpCardReq\n    CARD_QUALITY_UP_RSP                 = 101403;   //QualityUpCardRsp\n    CARD_LEVELUP_SKILL_REQ              = 1404;     //LevelupCardSkillReq\n    CARD_LEVELUP_SKILL_RSP              = 101404;   //LevelupCardSkillRsp\n    CARD_GRADE_UP_REQ                   = 1405;     //GradeUpCardReq\n    CARD_GRADE_UP_RSP                   = 101405;   //GradeUpCardRsp\n    CARD_GET_ALL_TEAM_REQ               = 1406;     //GetCardAllTeamReq\n    CARD_GET_ALL_TEAM_RSP               = 101406;   //GetCardAllTeamRsp\n    CARD_SET_TEAM_REQ                   = 1407;     //SetCardTeamReq\n    CARD_SET_TEAM_RSP                   = 101407;   //SetCardTeamRsp\n    CARD_CHANGE_TEAM_NAME_REQ           = 1408;     //ChangeCardTeamNameReq\n    CARD_CHANGE_TEAM_NAME_RSP           = 101408;   //ChangeCardTeamNameRsp\n    CARD_CHANGE_FASHION_ID_REQ          = 1409;     //ChangeCardFashionReq\n    CARD_CHANGE_FASHION_ID_RSP          = 101409;   //ChangeCardFashionRsp\n    CARD_GET_ALL_SHOW_FASHION_REQ       = 1410;     //GetAllShowFashionReq\n    CARD_GET_ALL_SHOW_FASHION_RSP       = 101410;   //GetAllShowFashionRsp\n    CARD_GET_FASHION_REQ                = 1411;     //GetAllCardFashionReq\n    CARD_GET_FASHION_RSP                = 101411;   //GetAllCardFashionRsp\n    CARD_CLICK_STORY_EVENT_REPORT_REQ   = 1412;     //ClickCardStoryEventReportReq\n    CARD_CLICK_STORY_EVENT_REPORT_RSP   = 101412;   //ClickCardStoryEventReportRsp\n    CARD_GET_CLICKED_STORY_EVENTS_REQ   = 1413;     //GetCardClickedStoryEventsReq\n    CARD_GET_CLICKED_STORY_EVENTS_RSP   = 101413;   //GetCardClickedStoryEventsRsp\n    CARD_GET_OTHER_CARD_INFO_REQ        = 1414;     //GetOtherCardInfoReq\n    CARD_GET_OTHER_CARD_INFO_RSP        = 101414;   //GetOtherCardInfoRsp\n    CARD_ROBOT_TEST_INITIAL_REQ         = 1415;     //CardRobotTestInitialReq\n    CARD_ROBOT_TEST_INITIAL_RSP         = 101415;   //CardRobotTestInitialRsp\n    CARD_MULTI_GRADE_UP_REQ             = 1416;     //MultiGradeUpCardReq\n    CARD_MULTI_GRADE_UP_RSP             = 101416;   //MultiGradeUpCardRsp\n    CARD_SET_FOCUS_REQ                  = 1417;     //SetCardFocusReq\n    CARD_SET_FOCUS_RSP                  = 101417;   //SetCardFocusRsp\n    CARD_SET_FASHION_SHOW_REQ           = 1418;     //SetCardFashionShowReq\n    CARD_SET_FASHION_SHOW_RSP           = 101418;   //SetCardFashionShowRsp\n    CARD_FETCH_HAND_BOOK_REWARD_REQ     = 1419;     //FetchHandBookRewardReq\n    CARD_FETCH_HAND_BOOK_REWARD_RSP     = 101419;   //FetchHandBookRewardRsp\n    CARD_ACTIVATE_HAND_BOOK_GROW_REQ    = 1420;     //ActivateHandBookGrowReq\n    CARD_ACTIVATE_HAND_BOOK_GROW_RSP    = 101420;   //ActivateHandBookGrowRsp\n    CARD_END                            = 1499;\n\n    SCENE_START                         = 1500;\n    SCENE_GET_SCENE_INFO_REQ            = 1501;     //GetSceneInfoReq\n    SCENE_GET_SCENE_INFO_RSP            = 101501;   //GetSceneInfoRsp\n    SCENE_GET_CHAPTER_STAGE_REQ         = 1502;     //GetChapterStageReq\n    SCENE_GET_CHAPTER_STAGE_RSP         = 101502;   //GetChapterStageRsp\n    SCENE_CHALLENGE_STAGE_REQ           = 1503;     //ChallengeStageReq\n    SCENE_CHALLENGE_STAGE_RSP           = 101503;   //ChallengeStageRsp\n    SCENE_GET_CHALLENGE_RECORD_REQ      = 1505;     //GetChallengeRecordReq\n    SCENE_GET_CHALLENGE_RECORD_RSP      = 101505;   //GetChallengeRecordRsp\n    SCENE_FETCH_CHAPTER_REWARD_REQ      = 1506;     //FetchSceneChapterRewardReq\n    SCENE_FETCH_CHAPTER_REWARD_RSP      = 101506;   //FetchSceneChapterRewardRsp\n    SCENE_GET_OPEN_STAGES_REQ           = 1507;     //GetOpenStagesReq\n    SCENE_GET_OPEN_STAGES_RSP           = 101507;   //GetOpenStagesRsp\n    SCENE_FETCH_STAGE_REWARD_REQ        = 1508;     //FetchSceneStageRewardReq\n    SCENE_FETCH_STAGE_REWARD_RSP        = 101508;   //FetchSceneStageRewardRsp\n    SCENE_SWEEP_STAGE_REQ               = 1509;     //SweepStageReq\n    SCENE_SWEEP_STAGE_RSP               = 101509;   //SweepStageRsp\n    SCENE_GET_FEATURE_SCHEDULE_REQ      = 1510;     //GetFeatureScheduleReq\n    SCENE_GET_FEATURE_SCHEDULE_RSP      = 101510;   //GetFeatureScheduleRsp\n    SCENE_GET_MULTI_DROP_ACTIVITY_REQ   = 1511;     //GetMultiDropActivityReq\n    SCENE_GET_MULTI_DROP_ACTIVITY_RSP   = 101511;   //GetMultiDropActivityRsp\n    SCENE_GET_RANK_REQ                  = 1515;     //GetSceneRankReq\n    SCENE_GET_RANK_RSP                  = 101515;   //GetSceneRankRsp\n    SCENE_END                           = 1599;\n\n    RELATION_START                      = 1600;\n    RELATION_GET_FRIENDS_REQ            = 1601;     //GetFriendsReq\n    RELATION_GET_FRIENDS_RSP            = 101601;   //GetFriendsRsp\n    RELATION_APPLY_ADD_FRIEND_REQ       = 1602;     //ApplyAddFriendReq\n    RELATION_APPLY_ADD_FRIEND_RSP       = 101602;   //ApplyAddFriendRsp\n    RELATION_AGREE_FRIEND_APPLY_REQ     = 1603;     //AgreeFriendApplyReq\n    RELATION_AGREE_FRIEND_APPLY_RSP     = 101603;   //AgreeFriendApplyRsp\n    RELATION_DISAGREE_FRIEND_APPLY_REQ  = 1604;     //DisagreeFriendReq\n    RELATION_DISAGREE_FRIEND_APPLY_RSP  = 101604;   //DisagreeFriendRsp\n    RELATION_BLOCK_TARGET_REQ           = 1605;     //BlockTargetReq\n    RELATION_BLOCK_TARGET_RSP           = 101605;   //BlockTargetRsp\n    RELATION_DELETE_RELATION_REQ        = 1606;     //DeleteRelationReq\n    RELATION_DELETE_RELATION_RSP        = 101606;   //DeleteRelationRsp\n    RELATION_SEARCH_TARGET_REQ          = 1607;     //SearchTargetReq\n    RELATION_SEARCH_TARGET_RSP          = 101607;   //SearchTargetRsp\n    RELATION_SET_REMARK_RELATION_REQ    = 1608;     //SetRelationRemarkReq\n    RELATION_SET_REMARK_RELATION_RSP    = 101608;   //SetRelationRemarkRsp\n    RELATION_GET_ALL_BLOCK_TARGET_REQ   = 1609;     //GetAllBlockTargetReq\n    RELATION_GET_ALL_BLOCK_TARGET_RSP   = 101609;   //GetAllBlockTargetRsp\n    RELATION_GET_FIGHT_RECORD_REQ       = 1610;     //GetFriendFightRecordReq\n    RELATION_GET_FIGHT_RECORD_RSP       = 101610;   //GetFriendFightRecordRsp\n    RELATION_END                        = 1699;\n\n    BADGE_START                         = 1700;\n    BADGE_GET_ALL_REQ                   = 1701;     //GetAllBadgesReq\n    BADGE_GET_ALL_RSP                   = 101701;   //GetAllBadgesRsp\n    BADGE_WEAR_REQ                      = 1702;     //WearBadgeReq\n    BADGE_WEAR_RSP                      = 101702;   //WearBadgeRsp\n    BADGE_TAKEOFF_REQ                   = 1703;     //TakeoffBadgeReq\n    BADGE_TAKEOFF_RSP                   = 101703;   //TakeoffBadgeRsp\n    BADGE_LEVELUP_REQ                   = 1704;     //LevelupBadgeReq\n    BADGE_LEVELUP_RSP                   = 101704;   //LevelupBadgeRsp\n    BADGE_DECOMPOSE_REQ                 = 1705;     //DecomposeBadgeReq\n    BADGE_DECOMPOSE_RSP                 = 101705;   //DecomposeBadgeRsp\n    BADGE_SET_LOCK_STATE_REQ            = 1706;     //SetBadgeLockStateReq\n    BADGE_SET_LOCK_STATE_RSP            = 101706;   //SetBadgeLockStateRsp\n    BADGE_CLEAR_NEW_TAG_REQ             = 1707;     //ClearBadgeNewTagReq\n    BADGE_CLEAR_NEW_TAG_RSP             = 101707;   //ClearBadgeNewTagRsp\n    BADGE_SWITCH_REQ                    = 1708;     //SwitchBadgeReq\n    BADGE_SWITCH_RSP                    = 101708;   //SwitchBadgeRsp\n    BADGE_END                           = 1799;\n\n    MAIL_START                          = 1800;\n    MAIL_GET_ALL_MAILS_REQ              = 1801;     //GetAllMailsReq\n    MAIL_GET_ALL_MAILS_RSP              = 101801;   //GetAllMailsRsp\n    MAIL_FETCH_MAIL_ATTACHMENT_REQ      = 1802;     //FetchMailAttachmentReq\n    MAIL_FETCH_MAIL_ATTACHMENT_RSP      = 101802;   //FetchMailAttachmentRsp\n    MAIL_DELETE_MAIL_REQ                = 1803;     //DeleteMailReq\n    MAIL_DELETE_MAIL_RSP                = 101803;   //DeleteMailRsp\n    MAIL_MARK_READ_REQ                  = 1804;     //MarkMailReadReq\n    MAIL_MARK_READ_RSP                  = 101804;   //MarkMailReadRsp\n    MAIL_END                            = 1899;\n\n    BATTLE_START                        = 1900;\n    BATTLE_PREPARE_REQ                  = 1901;     //PrepareBattleReq\n    BATTLE_PREPARE_RSP                  = 101901;   //PrepareBattleRsp\n    BATTLE_GET_STAGE_PREPARE_INFO_REQ   = 1902;     //GetStagePrepareInfoReq\n    BATTLE_GET_STAGE_PREPARE_INFO_RSP   = 101902;   //GetStagePrepareInfoRsp\n    BATTLE_GET_BATTLE_RECORD_REQ        = 1905;     //GetBattleRecordReq\n    BATTLE_GET_BATTLE_RECORD_RSP        = 101905;   //GetBattleRecordRsp\n    BATTLE_SAVE_STAGE_PREPARE_INFO_REQ  = 1906;     //SaveStagePrepareInfoReq\n    BATTLE_SAVE_STAGE_PREPARE_INFO_RSP  = 101906;   //SaveStagePrepareInfoRsp\n    BATTLE_EXIT_STAGE_PREPARE_REQ       = 1907;     //ExitStagePrepareReq\n    BATTLE_EXIT_STAGE_PREPARE_RSP       = 101907;   //ExitStagePrepareRsp\n    BATTLE_GET_FRIEND_DEFENCE_FORMATION_REQ = 1908;   //GetFriendDefenceFormationReq\n    BATTLE_GET_FRIEND_DEFENCE_FORMATION_RSP = 101908; //GetFriendDefenceFormationRsp\n    BATTLE_END                          = 1999;\n\n    BOSS_START                          = 2000;\n    BOSS_GET_BOSS_INFO_REQ              = 2001;     //GetBossInfoReq\n    BOSS_GET_BOSS_INFO_RSP              = 102001;   //GetBossInfoRsp\n    BOSS_GET_BOSS_TOP_RANK_REQ          = 2002;     //GetBossTopRankReq\n    BOSS_GET_BOSS_TOP_RANK_RSP          = 102002;   //GetBossTopRankRsp\n    BOSS_GET_BOSS_RANK_ACTOR_RECORD_REQ = 2003;     //GetBossRankActorRecordReq\n    BOSS_GET_BOSS_RANK_ACTOR_RECORD_RSP = 102003;   //GetBossRankActorRecordRsp\n    BOSS_GIVE_UP_BOSS_CHALLENGE_REQ     = 2004;     //GiveupBossChallengeReq\n    BOSS_GIVE_UP_BOSS_CHALLENGE_RSP     = 102004;   //GiveupBossChallengeRsp \n    BOSS_QUICK_BOSS_CHALLENGE_REQ       = 2005;     //QuickBossChallengeReq\n    BOSS_QUICK_BOSS_CHALLENGE_RSP       = 102005;   //QuickBossChallengeRsp \n    BOSS_START_BOSS_CHALLENGE_REQ       = 2006;     //StartBossChallengeReq\n    BOSS_START_BOSS_CHALLENGE_RSP       = 102006;   //StartBossChallengeRsp \n    BOSS_REWARD_BOSS_CHALLENGE_REQ      = 2007;     //RewardBossChallengeReq\n    BOSS_REWARD_BOSS_CHALLENGE_RSP      = 102007;   //RewardBossChallengeRsp \n    BOSS_END                            = 2099;\n\n    MANOR_START                         = 2100;\n    MANOR_GET_MANOR_INFO_REQ            = 2101;     //GetManorInfoReq\n    MANOR_GET_MANOR_INFO_RSP            = 102101;   //GetManorInfoRsp\n    MANOR_TRIGGER_EVENT_REQ             = 2102;     //ManorTriggerEventReq\n    MANOR_TRIGGER_EVENT_RSP             = 102102;   //ManorTriggerEventRsp\n    MANOR_REPORT_POSITION_REQ           = 2103;     //ManorReportPositionReq\n    MANOR_REPORT_POSITION_RSP           = 102103;   //ManorReportPositionRsp\n    MANOR_PROCESS_EVENT_REQ             = 2104;     //ManorProcessEventReq\n    MANOR_PROCESS_EVENT_RSP             = 102104;   //ManorProcessEventRsp\n    MANOR_FINISH_STORY_REQ              = 2105;     //ManorFinishStoryReq\n    MANOR_FINISH_STORY_RSP              = 102105;   //ManorFinishStoryRsp\n    MANOR_GET_MANOR_INFO_SIMPLE_REQ     = 2106;     //GetManorInfoSimpleReq\n    MANOR_GET_MANOR_INFO_SIMPLE_RSP     = 102106;   //GetManorInfoSimpleRsp\n    MANOR_REPORT_EVENT_POSITION_REQ     = 2107;     //ManorReportEventPositionReq\n    MANOR_REPORT_EVENT_POSITION_RSP     = 102107;   //ManorReportEventPositionRsp\n    MANOR_JUMP_STORY_EVENT_REQ          = 2108;     //ManorJumpStoryEventReq\n    MANOR_JUMP_STORY_EVENT_RSP          = 102108;   //ManorJumpStoryEventRsp\n    MANOR_GET_FEATURE_SCHEDULE_REQ      = 2109;     //GetManorFeatureScheduleReq\n    MANOR_GET_FEATURE_SCHEDULE_RSP      = 102109;   //GetManorFeatureScheduleRsp\n    MANOR_FETCH_ROOKIE_REWARD_REQ       = 2110;     //ManorFetchRookieRewardReq\n    MANOR_FETCH_ROOKIE_REWARD_RSP       = 102110;   //ManorFetchRookieRewardRsp\n    MANOR_GET_ACTIVITY_ROLE_PLOT_EVENT_REQ = 2111;  //ManorGetActivityRolePlotEventReq\n    MANOR_GET_ACTIVITY_ROLE_PLOT_EVENT_RSP = 102111;//ManorGetActivityRolePlotEventRsp\n    MANOR_BATCH_PROCESS_EVENT_REQ       = 2112;     //ManorBatchProcessEventReq\n    MANOR_BATCH_PROCESS_EVENT_RSP       = 102112;   //ManorBatchProcessEventRsp\n    MANOR_END                           = 2199;\n\n    //肉鸽\n    ROGUE_START                         = 2200;\n    ROGUE_GET_ROGUE_INFO_REQ            = 2201;     //GetRogueInfoReq\n    ROGUE_GET_ROGUE_INFO_RSP            = 102201;   //GetRogueInfoRsp\n    ROGUE_START_ROGUE_GAME_REQ          = 2202;     //StartRogueGameReq\n    ROGUE_START_ROGUE_GAME_RSP          = 102202;   //StartRogueGameRsp\n    ROGUE_GET_ROGUE_STATE_REQ           = 2203;     //GetRogueStateInfoReq\n    ROGUE_GET_ROGUE_STATE_RSP           = 102203;   //GetRogueStateInfoRsp\n    ROGUE_ENTER_ROGUE_NODE_REQ          = 2204;     //EnterRogueNodeReq\n    ROGUE_ENTER_ROGUE_NODE_RSP          = 102204;   //EnterRogueNodeRsp\n    ROGUE_EXIT_ROGUE_NODE_REQ           = 2205;     //ExitRogueNodeReq\n    ROGUE_EXIT_ROGUE_NODE_RSP           = 102205;   //ExitRogueNodeRsp\n    ROGUE_ENHANCE_CARD_ATTRIB_REQ       = 2206;     //EnhanceRogueCardAttribReq\n    ROGUE_ENHANCE_CARD_ATTRIB_RSP       = 102206;   //EnhanceRogueCardAttribRsp\n    ROGUE_ACTIVATE_TALENT_REQ           = 2207;     //ActivateRogueTalentReq\n    ROGUE_ACTIVATE_TALENT_RSP           = 102207;   //ActivateRogueTalentRsp\n    ROGUE_BUY_SHOP_TREASURE_REQ         = 2208;     //BuyRogueNodeShopTreasureReq\n    ROGUE_BUY_SHOP_TREASURE_RSP         = 102208;   //BuyRogueNodeShopTreasureRsp\n    ROGUE_REFRESH_SHOP_REQ              = 2209;     //RefreshRogueNodeShopReq\n    ROGUE_REFRESH_SHOP_RSP              = 102209;   //RefreshRogueNodeShopRsp\n    ROGUE_FETCH_NODE_REWARD_REQ         = 2210;     //FetchRogueNodeRewardReq\n    ROGUE_FETCH_NODE_REWARD_RSP         = 102210;   //FetchRogueNodeRewardRsp\n    ROGUE_QUIT_GAME_REQ                 = 2211;     //QuitRogueGameReq\n    ROGUE_QUIT_GAME_RSP                 = 102211;   //QuitRogueGameRsp\n    ROGUE_GET_PIC_NEW_STATE_REQ         = 2212;     //GetRoguePicNewStateReq\n    ROGUE_GET_PIC_NEW_STATE_RSP         = 102212;   //GetRoguePicNewStateRsp\n    ROGUE_CLEAR_PIC_NEW_STATE_REQ       = 2213;     //ClearRoguePicNewStateReq\n    ROGUE_CLEAR_PIC_NEW_STATE_RSP       = 102213;   //ClearRoguePicNewStateRsp\n    ROGUE_GET_ALL_PIC_REQ               = 2214;     //GetRogueAllPicReq\n    ROGUE_GET_ALL_PIC_RSP               = 102214;   //GetRogueAllPicRsp\n    ROGUE_GET_TRENDS_REQ                = 2215;     //GetRogueTrendsReq\n    ROGUE_GET_TRENDS_RSP                = 102215;   //GetRogueTrendsRsp\n    ROGUE_FETCH_THEME_LEVEL_REWARD_REQ  = 2216;     //FetchRogueThemeLevelRewardReq\n    ROGUE_FETCH_THEME_LEVEL_REWARD_RSP  = 102216;   //FetchRogueThemeLevelRewardRsp\n    ROGUE_GET_TOP_SCORE_RECORD_REQ      = 2217;     //GetRogueTopScoreRecordReq\n    ROGUE_GET_TOP_SCORE_RECORD_RSP      = 102217;   //GetRogueTopScoreRecordRsp\n    ROGUE_FETCH_TREND_TASK_REWARD_REQ   = 2218;     //FetchRogueTrendTaskRewardReq\n    ROGUE_FETCH_TREND_TASK_REWARD_RSP   = 102218;   //FetchRogueTrendTaskRewardRsp\n    ROGUE_FINISH_EVENT_STORY_REQ        = 2219;     //FinishRogueEventStoryReq\n    ROGUE_FINISH_EVENT_STORY_RSP        = 102219;   //FinishRogueEventStoryRsp\n    ROGUE_RECRUIT_INITIAL_CARD_REQ      = 2220;     //RecruitRogueInitialCardReq\n    ROGUE_RECRUIT_INITIAL_CARD_RSP      = 102220;   //RecruitRogueInitialCardRsp\n    ROGUE_CHOOSE_INITIAL_TREASURE_REQ   = 2221;     //ChooseRogueInitialTreasureReq\n    ROGUE_CHOOSE_INITIAL_TREASURE_RSP   = 102221;   //ChooseRogueInitialTreasureRsp\n    ROGUE_FINISH_EVENT_KEY_STORY_REQ    = 2222;     //FinishRogueEventKeyStoryReq\n    ROGUE_FINISH_EVENT_KEY_STORY_RSP    = 102222;   //FinishRogueEventKeyStoryRsp\n    ROGUE_CHOOSE_EVENT_BATTLE_STORY_REQ = 2223;     //ChooseRogueEventBattleStoryReq\n    ROGUE_CHOOSE_EVENT_BATTLE_STORY_RSP = 102223;   //ChooseRogueEventBattleStoryRsp\n    ROGUE_SWEEP_REQ                     = 2224;     //SweepRogueReq\n    ROGUE_SWEEP_RSP                     = 102224;   //SweepRogueRsp\n    ROGUE_END                           = 2299;\n\n    GUILD_WAR_START                     = 2300;\n    GUILD_WAR_GET_SCHEDULE_REQ          = 2301;     //GetGuildWarScheduleReq\n    GUILD_WAR_GET_SCHEDULE_RSP          = 102301;   //GetGuildWarScheduleRsp\n    GUILD_WAR_GET_ALL_INFO_REQ          = 2302;     //GetGuildWarAllInfoReq\n    GUILD_WAR_GET_ALL_INFO_RSP          = 102302;   //GetGuildWarAllInfoRsp\n    GUILD_WAR_GET_COMPENSATION_FORMATION_REQ = 2303;    //GetGuildWarCompensateFormationReq\n    GUILD_WAR_GET_COMPENSATION_FORMATION_RSP = 102303;  //GetGuildWarCompensateFormationRsp\n    GUILD_WAR_LEVEL_UP_SKILL_REQ        = 2304;     //LevelupGuildWarSkillReq\n    GUILD_WAR_LEVEL_UP_SKILL_RSP        = 102304;   //LevelupGuildWarSkillRsp\n    GUILD_WAR_SET_ASSIST_CARD_REQ       = 2305;     //SetGuildWarAssistCardReq\n    GUILD_WAR_SET_ASSIST_CARD_RSP       = 102305;   //SetGuildWarAssistCardRsp\n    GUILD_WAR_GET_RECOMMEND_FORMATION_REQ = 2306;   //GetGuildWarRecommendFormationReq\n    GUILD_WAR_GET_RECOMMEND_FORMATION_RSP = 102306; //GetGuildWarRecommendFormationRsp\n    GUILD_WAR_GET_RANK_INFO_REQ           = 2307;   //GetGuildWarRankReq\n    GUILD_WAR_GET_RANK_INFO_RSP           = 102307; //GetGuildWarRankRsp\n    GUILD_WAR_REWARD_TASK_REQ             = 2308;   //RewardGuildWarTaskReq\n    GUILD_WAR_REWARD_TASK_RSP             = 102308; //RewardGuildWarTaskRsp\n    GUILD_WAR_SET_SKILL_TEAM_REQ          = 2309;   //SetGuildWarSkillTeamReq\n    GUILD_WAR_SET_SKILL_TEAM_RSP          = 102309; //SetGuildWarSkillTeamRsp\n    GUILD_WAR_GET_BATTLE_RECORD_REQ       = 2310;   //GetGuildWarBattleRecordReq\n    GUILD_WAR_GET_BATTLE_RECORD_RSP       = 102310; //GetGuildWarBattleRecordRsp\n    GUILD_WAR_GET_IN_BATTLE_COUNT_REQ     = 2311;   //GetGuildWarInBattleCountReq\n    GUILD_WAR_GET_IN_BATTLE_COUNT_RSP     = 102311; //GetGuildWarInBattleCountRsp\n    GUILD_WAR_END                       = 2399;\n\n    SEAL_START                          = 2400;\n    GET_SEAL_WEAR_INFO_REQ              = 2401;     //GetSealWearInfoReq\n    GET_SEAL_WEAR_INFO_RSP              = 102401;   //GetSealWearInfoRsp\n    SEAL_WEAR_REQ                       = 2402;     //WearSealReq\n    SEAL_WEAR_RSP                       = 102402;   //WearSealRsp\n    SEAL_TAKE_OFF_REQ                   = 2403;     //TakeoffSealReq\n    SEAL_TAKE_OFF_RSP                   = 102403;   //TakeoffSealRsp\n    SEAL_COMPOSITE_REQ                  = 2404;     //CompositeSealReq\n    SEAL_COMPOSITE_RSP                  = 102404;   //CompositeSealRsp\n    SEAL_BIG_LEVELUP_REQ                = 2405;     //SealBigLevelupReq\n    SEAL_BIG_LEVELUP_RSP                = 102405;   //SealBigLevelupRsp\n    SEAL_BIG_QUALITY_UP_REQ             = 2406;     //SealBigQualityUpReq\n    SEAL_BIG_QUALITY_UP_RSP             = 102406;   //SealBigQualityUpRsp\n    SEAL_BIG_ADD_UP_REQ                 = 2407;     //SealBigAddUpReq\n    SEAL_BIG_ADD_UP_RSP                 = 102407;   //SealBigAddUpRsp\n    SEAL_BIG_GET_HOOK_INFO_REQ          = 2408;     //GetSealBigHookInfoReq\n    SEAL_BIG_GET_HOOK_INFO_RSP          = 102408;   //GetSealBigHookInfoRsp\n    SEAL_BIG_FETCH_HOOK_REWARD_REQ      = 2409;     //FetchSealBigHookRewardReq\n    SEAL_BIG_FETCH_HOOK_REWARD_RSP      = 102409;   //FetchSealBigHookRewardRsp\n    SEAL_BIG_QUIT_HOOK_CHALLENGE_REQ    = 2410;     //QuitSealBigHookChallengeReq\n    SEAL_BIG_QUIT_HOOK_CHALLENGE_RSP    = 102410;   //QuitSealBigHookChallengeRsp\n    SEAL_END                            = 2499;\n\n    GUILD_START                         = 10000;\n    GUILD_GET_MY_GUILD_INFO_REQ         = 10001;    //GetMyGuildInfoReq\n    GUILD_GET_MY_GUILD_INFO_RSP         = 110001;   //GetMyGuildInfoRsp\n    GUILD_CREATE_GUILD_REQ              = 10002;    //CreateGuildReq\n    GUILD_CREATE_GUILD_RSP              = 110002;   //CreateGuildRsp\n    GUILD_SEARCH_BY_NAME_REQ            = 10003;    //SearchGuildByNameReq\n    GUILD_SEARCH_BY_NAME_RSP            = 110003;   //SearchGuildByNameRsp\n    GUILD_GET_GUILD_MEMBERS_REQ         = 10004;    //GetGuildMembersReq\n    GUILD_GET_GUILD_MEMBERS_RSP         = 110004;   //GetGuildMembersRsp\n    GUILD_CHANGE_ICON_REQ               = 10005;    //ChangeGuildIconReq\n    GUILD_CHANGE_ICON_RSP               = 110005;   //ChangeGuildIconRsp\n    GUILD_CHANGE_NAME_REQ               = 10006;    //ChangeGuildNameReq\n    GUILD_CHANGE_NAME_RSP               = 110006;   //ChangeGuildNameRsp\n    GUILD_CHANGE_NOTICE_REQ             = 10007;    //ChangeGuildNoticeReq\n    GUILD_CHANGE_NOTICE_RSP             = 110007;   //ChangeGuildNoticeRsp\n    GUILD_SET_LEVEL_LIMIT_REQ           = 10008;    //SetGuildLevelLimitReq\n    GUILD_SET_LEVEL_LIMIT_RSP           = 110008;   //SetGuildLevelLimitRsp\n    GUILD_APPLY_TO_JOIN_REQ             = 10009;    //ApplyJoinGuildReq\n    GUILD_APPLY_TO_JOIN_RSP             = 110009;   //ApplyJoinGuildRsp\n    GUILD_CANCEL_JOIN_REQ               = 10010;    //CancelJoinGuildReq\n    GUILD_CANCEL_JOIN_RSP               = 110010;   //CancelJoinGuildRsp\n    GUILD_PROCESS_JOIN_APPLY_REQ        = 10011;    //ProcessGuildJoinApplyReq\n    GUILD_PROCESS_JOIN_APPLY_RSP        = 110011;   //ProcessGuildJoinApplyRsp\n    GUILD_OPERATE_VICE_LEADER_REQ       = 10012;    //OperateGuildViceLeaderReq\n    GUILD_OPERATE_VICE_LEADER_RSP       = 110012;   //OperateGuildViceLeaderRsp\n    GUILD_KICK_OUT_MEMBER_REQ           = 10013;    //KickOutGuildMemberReq\n    GUILD_KICK_OUT_MEMBER_RSP           = 110013;   //KickOutGuildMemberRsp\n    GUILD_TRANSFER_LEADER_REQ           = 10014;    //TransferGuildLeaderReq\n    GUILD_TRANSFER_LEADER_RSP           = 110014;   //TransferGuildLeaderRsp\n    GUILD_DISMISS_REQ                   = 10015;    //DismissGuildReq\n    GUILD_DISMISS_RSP                   = 110015;   //DismissGuildRsp\n    GUILD_EXIT_REQ                      = 10016;    //ExitGuildReq\n    GUILD_EXIT_RSP                      = 110016;   //ExitGuildRsp\n    GUILD_GET_RECOMMEND_REQ             = 10017;    //GetRecommendGuildReq\n    GUILD_GET_RECOMMEND_RSP             = 110017;   //GetRecommendGuildRsp\n    GUILD_START_IMPEACH_LEADER_REQ      = 10018;    //StartImpeachGuildLeaderReq\n    GUILD_START_IMPEACH_LEADER_RSP      = 110018;   //StartImpeachGuildLeaderRsp\n    GUILD_VOTE_IMPEACH_LEADER_REQ       = 10019;    //VoteImpeachGuildLeaderReq\n    GUILD_VOTE_IMPEACH_LEADER_RSP       = 110019;   //VoteImpeachGuildLeaderRsp\n    GUILD_NOTIFY_CONSUME_ENERGY_REQ     = 10020;    //NotifyGuildConsumeEnergyReq\n    GUILD_NOTIFY_CONSUME_ENERGY_RSP     = 110020;   //NotifyGuildConsumeEnergyRsp\n    GUILD_QUICK_JOIN_REQ                = 10021;    //QuickJoinGuildReq\n    GUILD_QUICK_JOIN_RSP                = 110021;   //QuickJoinGuildRsp\n    GUILD_AUTO_JOIN_REQ                 = 10022;    //AutoJoinGuildReq\n    GUILD_AUTO_JOIN_RSP                 = 110022;   //AutoJoinGuildRsp\n    GUILD_GET_USER_GUILD_UID_REQ        = 10023;    //GetUserGuildUidReq\n    GUILD_GET_USER_GUILD_UID_RSP        = 110023;   //GetUserGuildUidRsp\n    GUILD_GET_APPLIED_GUILDS_REQ        = 10024;    //GetAppliedGuildsReq\n    GUILD_GET_APPLIED_GUILDS_RSP        = 110024;   //GetAppliedGuildsRsp\n    GUILD_SET_TARGET_REQ                = 10025;    //SetGuildTargetReq\n    GUILD_SET_TARGET_RSP                = 110025;   //SetGuildTargetRsp\n    GUILD_GET_IMPEACH_INFO_REQ          = 10026;    //GetImpeachInfoReq\n    GUILD_GET_IMPEACH_INFO_RSP          = 110026;   //GetImpeachInfoRsp\n    GUILD_GET_MY_GUILD_SIMPLE_INFO_REQ  = 10027;    //GetMyGuildSimpleInfoReq\n    GUILD_GET_MY_GUILD_SIMPLE_INFO_RSP  = 110027;   //GetMyGuildSimpleInfoRsp\n    GUILD_GET_PRACTICE_RANK_REQ         = 10028;    //GetGuildPracticeRankReq\n    GUILD_GET_PRACTICE_RANK_RSP         = 110028;   //GetGuildPracticeRankRsp\n    GUILD_GET_PRACTICE_RECORD_REQ       = 10029;    //GetGuildPracticeRecordReq\n    GUILD_GET_PRACTICE_RECORD_RSP       = 110029;   //GetGuildPracticeRecordRsp\n    GUILD_SAVE_PRACTICE_RECORD_REQ      = 10030;    //SaveGuildPracticeRecordReq\n    GUILD_SAVE_PRACTICE_RECORD_RSP      = 110030;   //SaveGuildPracticeRecordRsp\n    GUILD_SET_POLICY_REQ                = 10031;    //SetGuildPolicyReq\n    GUILD_SET_POLICY_RSP                = 110031;   //SetGuildPolicyRsp\n    GUILD_SEARCH_BY_CONDITIONS_REQ      = 10032;    //SearchGuildByConditionsReq\n    GUILD_SEARCH_BY_CONDITIONS_RSP      = 110032;   //SearchGuildByConditionsRsp\n    GUILD_WAR_GET_RANK_INFO_EXT_REQ     = 10033;   //GetGuildWarRankExtReq\n    GUILD_WAR_GET_RANK_INFO_EXT_RSP     = 110033;  //GetGuildWarRankExtRsp\n    GUILD_END                           = 10099;\n\n    ARENA_START                         = 10100;\n    ARENA_GET_ALL_REQ                   = 10101;    //ArenaGetAllReq\n    ARENA_GET_ALL_RSP                   = 110101;   //ArenaGetAllRsp\n    ARENA_GET_MATCH_REQ                 = 10102;    //ArenaGetMatchReq\n    ARENA_GET_MATCH_RSP                 = 110102;   //ArenaGetMatchRsp\n    ARENA_GET_RECORD_REQ                = 10103;    //ArenaGetRecordReq\n    ARENA_GET_RECORD_RSP                = 110103;   //ArenaGetRecordRsp\n    ARENA_FIGHT_REQ                     = 10104;    //ArenaFightReq\n    ARENA_FIGHT_RSP                     = 110104;   //ArenaFightRsp\n    ARENA_SWITCH_RANK_REQ               = 10105;    //ArenaSwitchRankReq\n    ARENA_SWITCH_RANK_RSP               = 110105;   //ArenaSwitchRankRsp\n    ARENA_SET_DEFENSE_REQ               = 10106;    //ArenaSetDefenseReq\n    ARENA_SET_DEFENSE_RSP               = 110106;   //ArenaSetDefenseRsp\n    ARENA_UPDATE_ACTOR_MIRROR_REQ       = 10107;    //ArenaUpdateActorMirrorReq\n    ARENA_UPDATE_ACTOR_MIRROR_RSP       = 110107;   //ArenaUpdateActorMirrorRsp\n    ARENA_GET_TOP_RANK_REQ              = 10108;    //ArenaGetTopRankReq\n    ARENA_GET_TOP_RANK_RSP              = 110108;   //ArenaGetTopRankRsp\n    ARENA_GET_OPPONENT_FORMATION_REQ    = 10112;    //ArenaGetOpponentFormationReq\n    ARENA_GET_OPPONENT_FORMATION_RSP    = 110112;   //ArenaGetOpponentFormationRsp\n    ARENA_GET_ROLE_FORMATION_REQ        = 10113;    //ArenaGetRoleFormationReq \n    ARENA_GET_ROLE_FORMATION_RSP        = 110113;   //ArenaGetRoleFormationRsp\n    ARENA_REFRESH_ARENA_CD_REQ          = 10114;    //ArenaRefreshFightCDReq \n    ARENA_REFRESH_ARENA_CD_RSP          = 110114;   //ArenaRefreshFightCDRsp\n    ARENA_RESET_ARENA_FIGHT_NUM_REQ     = 10115;    //ArenaResetFightNumReq \n    ARENA_RESET_ARENA_FIGHT_NUM_RSP     = 110115;   //ArenaResetFightNumRsp\n    ARENA_GET_RANK_REWARD_REQ           = 10116;    //ArenaGetRankRewardReq \n    ARENA_GET_RANK_REWARD_RSP           = 110116;   //ArenaGetRankRewardRsp\n    ARENA_GET_ALL_DEFENSE_REQ           = 10117;    //ArenaGetAllDefenseReq\n    ARENA_GET_ALL_DEFENSE_RSP           = 110117;   //ArenaGetAllDefenseRsp\n    ARENA_SAVE_BATTLE_RECORD_REQ        = 10118;    //ArenaSaveBattleRecordReq\n    ARENA_SAVE_BATTLE_RECORD_RSP        = 110118;   //ArenaSaveBattleRecordRsp\n    ARENA_END                           = 10199;\n    \n    SHOP_START                          = 10200;\n    SHOP_GET_LIST_REQ                   = 10201;    //GetShopInfoReq\n    SHOP_GET_LIST_RSP                   = 110201;   //GetShopInfoRsp\n    SHOP_BUY_GOODS_REQ                  = 10202;    //BuyShopGoodsReq\n    SHOP_BUY_GOODS_RSP                  = 110202;   //BuyShopGoodsRsp\n    SHOP_REFRESH_GOODS_REQ              = 10203;    //RefreshShopGoodsReq\n    SHOP_REFRESH_GOODS_RSP              = 110203;   //RefreshShopGoodsRsp\n    SHOP_BUY_SEAL_GOODS_REQ             = 10204;    //BuySealShopGoodsReq\n    SHOP_BUY_SEAL_GOODS_RSP             = 110204;   //BuySealShopGoodsRsp\n    SHOP_END                            = 10299;\n\n    BATTLE_PASS_START                   = 10300;\n    BATTLE_PASS_GET_INFO_REQ            = 10301;    //GetBattlePassInfoReq\n    BATTLE_PASS_GET_INFO_RSP            = 110301;   //GetBattlePassInfoRsp\n    BATTLE_PASS_TASK_REFRESH_REQ        = 10302;    //BattlePassTaskRefreshReq\n    BATTLE_PASS_TASK_REFRESH_RSP        = 110302;   //BattlePassTaskRefreshRsp\n    BATTLE_PASS_TASK_RWEARD_REQ         = 10303;    //BattlePassTaskRewardReq\n    BATTLE_PASS_TASK_RWEARD_RSP         = 110303;   //BattlePassTaskRewardRsp\n    BATTLE_PASS_BUYLEVEL_REQ            = 10304;    //BattlePassBuyLevelReq\n    BATTLE_PASS_BUYLEVEL_RSP            = 110304;   //BattlePassBuyLevelRsp\n    BATTLE_PASS_GET_REWARD_REQ          = 10305;    //BattlePassGetRewardReq\n    BATTLE_PASS_GET_REWARD_RSP          = 110305;   //BattlePassGetRewardRsp\n    BATTLE_PASS_END                     = 10399;\n    \n    CARNIVAL_START                      = 10400;\n    CARNIVAL_GET_INFO_REQ               = 10401;    //GetCarnivalInfoReq\n    CARNIVAL_GET_INFO_RSP               = 110401;   //GetCarnivalInfoRsp\n    CARNIVAL_GET_REWARD_REQ             = 10402;    //CarnivalGetRewardReq\n    CARNIVAL_GET_REWARD_RSP             = 110402;   //CarnivalGetRewardRsp\n    CARNIVAL_END                        = 10499;\n    \n    GACHA_START                         = 10500;\n    GACHA_GET_INFO_REQ                  = 10501;    //GetGachaInfoReq\n    GACHA_GET_INFO_RSP                  = 110501;   //GetGachaInfoRsp\n    GACHA_DO_REQ                        = 10502;    //DoGachaReq   \n    GACHA_DO_RSP                        = 110502;   //DoGachaRsp\n    GACHA_EXCHANGE_REQ                  = 10503;    //ExchangeGachaReq\n    GACHA_EXCHANGE_RSP                  = 110503;   //ExchangeGachaRsp\n    GACHA_GET_RECORDS_REQ               = 10504;    //GetGachaRecordsReq\n    GACHA_GET_RECORDS_RSP               = 110504;   //GetGachaRecordsRsp\n    GACHA_SET_TARGET_REQ                = 10505;    //SetGachaTargetReq\n    GACHA_SET_TARGET_RSP                = 110505;   //SetGachaTargetRsp\n    GACHA_GET_EXTRA_REQ                 = 10506;    //GetGachaExtraReq\n    GACHA_GET_EXTRA_RSP                 = 110506;  //GetGachaExtraRsp\n    GACHA_END                           = 10599;\n    \n    PURCHASE_START                      = 10600;\n    PURCHASE_BUY_REQ                    = 10601;    //PurchaseBuyReq\n    PURCHASE_BUY_RSP                    = 110601;   //PurchaseBuyRsp\n    PURCHASE_GET_REQ                    = 10602;    //PurchaseGetReq\n    PURCHASE_GET_RSP                    = 110602;   //PurchaseGetRsp\n    PURCHASE_GET_PRODUCTS_REQ           = 10603;    //GetPurchaseProductsReq\n    PURCHASE_GET_PRODUCTS_RSP           = 110603;   //GetPurchaseProductsRsp\n    PURCHASE_BUY_FASHION_REQ            = 10604;    //FashionBuyReq\n    PURCHASE_BUY_FASHION_RSP            = 110604;   //FashionBuyRsp\n    PURCHASE_MONTHCARD_REWARD_REQ       = 10605;    //MonthCardDailyRewardReq\n    PURCHASE_MONTHCARD_REWARD_RSP       = 110605;   //MonthCardDailyRewardRsp\n    PURCHASE_BUY_BATTLEPASS_REQ         = 10606;    //BattlePassBuyReq\n    PURCHASE_BUY_BATTLEPASS_RSP         = 110606;   //BattlePassBuyRsp\n    PURCHASE_CREATE_PAY_ORDER_REQ       = 10607;    //CreatePayOrderReq\n    PURCHASE_CREATE_PAY_ORDER_RSP       = 110607;   //CreatePayOrderRsp\n    PURCHASE_CANCEL_PAY_ORDER_REQ       = 10608;    //CancelPayOrderReq\n    PURCHASE_CANCEL_PAY_ORDER_RSP       = 110608;   //CancelPayOrderRsp\n    PURCHASE_FINISH_PAY_ORDER_REQ       = 10609;    //FinishPayOrderReq\n    PURCHASE_FINISH_PAY_ORDER_RSP       = 110609;   //FinishPayOrderRsp\n    PURCHASE_FETCH_WEEK_PAY_REWARD_REQ  = 10610;    //FetchWeekPayRewardReq\n    PURCHASE_FETCH_WEEK_PAY_REWARD_RSP  = 110610;   //FetchWeekPayRewardRsp\n    PURCHASE_END                        = 10699;\n    \n    EXPEDITION_START                    = 10700;    \n    EXPEDITION_GET_INFO_REQ             = 10701;    //GetExpeditionInfoReq\n    EXPEDITION_GET_INFO_RSP             = 110701;   //GetExpeditionInfoRsp\n    EXPEDITION_GET_REWARD_REQ           = 10703;    //GetExpeditionRewardReq\n    EXPEDITION_GET_REWARD_RSP           = 110703;   //GetExpeditionRewardRsp\n    EXPEDITION_END                      = 10799;\n    \n    ACTIVITY_START                      = 10800;\n    ACTIVITY_GET_ALL_REQ                = 10801;    //GetActivityAllReq\n    ACTIVITY_GET_ALL_RSP                = 110801;   //GetActivityAllRsp\n    ACTIVITY_SIGNIN_REQ                 = 10802;    //ActivitySignInReq\n    ACTIVITY_SIGNIN_RSP                 = 110802;   //ActivitySignInRsp\n    ACTIVITY_STAGE_SHOP_BUY_REQ         = 10803;    //ActivityStageShopBuyReq\n    ACTIVITY_STAGE_SHOP_BUY_RSP         = 110803;   //ActivityStageShopBuyRsp\n    ACTIVITY_STAGE_TASK_REWARD_REQ      = 10804;    //ActivityStageTaskRewardReq\n    ACTIVITY_STAGE_TASK_REWARD_RSP      = 110804;   //ActivityStageTaskRewardRsp\n    ACTIVITY_SEARCH_REQ                 = 10805;    //ActivitySearchReq\n    ACTIVITY_SEARCH_RSP                 = 110805;   //ActivitySearchRsp\n    ACTIVITY_GET_BANNER_REQ             = 10806;    //GetAllBannerReq\n    ACTIVITY_GET_BANNER_RSP             = 110806;   //GetAllBannerRsp\n    ACTIVITY_GET_OP_ACTIVITY_BY_ID_REQ  = 10807;    //GetOpActivityByIdReq\n    ACTIVITY_GET_OP_ACTIVITY_BY_ID_RSP  = 110807;   //GetOpActivityByIdRsp\n    ACTIVITY_GET_RECOMMEND_IMG_REQ      = 10808;    //GetAllRecommendImgReq\n    ACTIVITY_GET_RECOMMEND_IMG_RSP      = 110808;   //GetAllRecommendImgRsp\n    ACTIVITY_STAGE_SIGNIN_REQ           = 10809;    //ActivityStageSignInReq\n    ACTIVITY_STAGE_SIGNIN_RSP           = 110809;   //ActivityStageSignInRsp\n    ACTIVITY_STAGE_GET_MINIGAME_REQ     = 10810;    //ActivityGetMiniGameReq\n    ACTIVITY_STAGE_GET_MINIGAME_RSP     = 110810;   //ActivityGetMiniGameRsp\n    ACTIVITY_STAGE_PLAY_MINIGAME_REQ    = 10811;    //ActivityPlayMiniGameReq\n    ACTIVITY_STAGE_PLAY_MINIGAME_RSP    = 110811;   //ActivityPlayMiniGameRsp\n    ACTIVITY_STAGE_RWRAD_MINIGAME_REQ   = 10812;    //ActivityRewardMiniGameReq\n    ACTIVITY_STAGE_RWRAD_MINIGAME_RSP   = 110812;   //ActivityRewardMiniGameRsp\n    ACTIVITY_RETURN_SIGN_IN_REQ         = 10813;    //ActivityReturnSignInReq\n    ACTIVITY_RETURN_SIGN_IN_RSP         = 110813;   //ActivityReturnSignInRsp\n    ACTIVITY_GET_REVIEW_REQ             = 10814;    //GetActivityReviewInfoReq\n    ACTIVITY_GET_REVIEW_RSP             = 110814;   //GetActivityReviewInfoRsp\n    ACTIVITY_REVIEW_SHOP_BUY_REQ        = 10815;    //ActivityReviewShopBuyReq\n    ACTIVITY_REVIEW_SHOP_BUY_RSP        = 110815;   //ActivityReviewShopBuyRsp\n    ACTIVITY_REVIEW_UNLOCK_REQ          = 10816;    //ActivityReviewUnlockReq\n    ACTIVITY_REVIEW_UNLOCK_RSP          = 110816;   //ActivityReviewUnlockRsp\n    ACTIVITY_DO_TURNTABLE_REQ           = 10817;    //ActivityDoTurnTableReq\n    ACTIVITY_DO_TURNTABLE_RSP           = 110817;   //ActivityDoTurnTableRsp\n    ACTIVITY_TURNTABLE_GET_FREE_REQ     = 10818;   //ActivityTurnTableGetFreeReq\n    ACTIVITY_TURNTABLE_GET_FREE_RSP     = 110818;   //ActivityTurnTableGetFreeRsp\n    ACTIVITY_GET_GAME_TOP_RANK_REQ      = 10819;   //ActivityGetGameTopRankReq\n    ACTIVITY_GET_GAME_TOP_RANK_RSP      = 110819;   //ActivityGetGameTopRankRsp\n    ACTIVITY_DO_TURNTABLE_ROUND_REQ     = 10820;    //ActivityDoTurnTableRoundReq\n    ACTIVITY_DO_TURNTABLE_ROUND_RSP     = 110820;   //ActivityDoTurnTableRoundRsp\n    ACTIVITY_FETCH_ACCUM_RECHARGE_REWARD_REQ = 10821; //FetchAccumRechargeRewardReq\n    ACTIVITY_FETCH_ACCUM_RECHARGE_REWARD_RSP = 110821;//FetchAccumRechargeRewardRsp\n    ACTIVITY_RETURNPRO_SIGNIN_REQ       = 10822;    //ActivityReturnProSigninReq\n    ACTIVITY_RETURNPRO_SIGNIN_RSP       = 110822;   //ActivityReturnProSigninRsp\n    ACTIVITY_RETURNPRO_SHOP_BUY_REQ     = 10823;    //ActivityReturnProShopBuyReq\n    ACTIVITY_RETURNPRO_SHOP_BUY_RSP     = 110823;   //ActivityReturnProShopBuyRsp\n    ACTIVITY_RETURNPRO_TASK_REWARD_REQ  = 10824;    //ActivityReturnProTaskRewardReq\n    ACTIVITY_RETURNPRO_TASK_REWARD_RSP  = 110824;   //ActivityReturnProTaskRewardRsp\n    ACTIVITY_GET_STAGE_DROP_MULTI_REQ   = 10825;    //ActivityGetStageDropMultiReq\n    ACTIVITY_GET_STAGE_DROP_MULTI_RSP   = 110825;   //ActivityGetStageDropMultiRsp\n    ACTIVITY_END                        = 10899;\n    \n    PLANT_START                         = 10900;\n    PLANT_GET_INFO_REQ                  = 10901;    //GetPlantInfoReq\n    PLANT_GET_INFO_RSP                  = 110901;   //GetPlantInfoRsp\n    PLANT_FLOWER_REWARD_REQ             = 10902;    //RewardFlowerReq\n    PLANT_FLOWER_REWARD_RSP             = 110902;   //RewardFlowerRsp\n    PLANT_TASK_REWARD_REQ               = 10903;    //RewardPlantTaskReq\n    PLANT_TASK_REWARD_RSP               = 110903;   //RewardPlantTaskRsp\n    PLANT_END                           = 10999;\n    \n    COMMON_TASK_START                   = 11000;\n    COMMON_TASK_GET_INFO_REQ            = 11001;    //GetCommonTaskInfoReq\n    COMMON_TASK_GET_INFO_RSP            = 111001;   //GetCommonTaskInfoRsp\n    COMMON_TASK_REPLACE_REQ             = 11002;    //CommonTaskReplaceReq\n    COMMON_TASK_REPLACE_RSP             = 111002;   //CommonTaskReplaceRsp\n    COMMON_TASK_REWARD_REQ              = 11003;    //CommonTaskRewardReq\n    COMMON_TASK_REWARD_RSP              = 111003;   //CommonTaskRewardRsp\n    COMMON_TASK_REFRESH_REQ             = 11004;    //GetTaskRefreshStampReq\n    COMMON_TASK_REFRESH_RSP             = 111004;   //GetTaskRefreshStampRsp\n    COMMON_TASK_END                     = 11999;\n    \n    COMMON_GIFT_START                   = 12000;\n    COMMON_GIFT_GET_INFO_REQ            = 12001;    //GetGiftInfoReq\n    COMMON_GIFT_GET_INFO_RSP            = 112001;   //GetGiftInfoRsp\n    COMMON_GIFT_BUY_REQ                 = 12002;    //BuyGiftReq\n    COMMON_GIFT_BUY_RSP                 = 112002;   //BuyGiftRsp\n    COMMON_GIFT_REWARD_REQ              = 12003;    //GetGiftRewardReq\n    COMMON_GIFT_REWARD_RSP              = 112003;   //GetGiftRewardRsp\n    COMMON_GIFT_END                     = 12999;\n    \n    SUPPLY_START                        = 13000;\n    SUPPLY_GET_INFO_REQ                 = 13001;    //GetSupplyInfoReq\n    SUPPLY_GET_INFO_RSP                 = 113001;   //GetSupplyInfoRsp\n    SUPPLY_REWARDED_REQ                 = 13002;    //RewardSupplyReq\n    SUPPLY_REWARDED_RSP                 = 113002;   //RewardSupplyRsp\n    SUPPLY_END                          = 13999;\n    \n    BUFF_STAGE_START                    = 14000;\n    BUFF_STAGE_GET_INFO_REQ             = 14001;    //BuffStageGetInfoReq\n    BUFF_STAGE_GET_INFO_RSP             = 114001;   //BuffStageGetInfoRsp\n    BUFF_STAGE_REWARD_REQ               = 14002;    //BuffStageRewardReq\n    BUFF_STAGE_REWARD_RSP               = 114002;   //BuffStageRewardRsp\n    BUFF_STAGE_END                      = 14999;\n    \n    CYCLE_TASK_START                    = 15000;\n    CYCLE_TASK_GET_INFO_REQ             = 15001;    //GetCycleTaskInfoReq\n    CYCLE_TASK_GET_INFO_RSP             = 115001;   //GetCycleTaskInfoRsp\n    CYCLE_TASK_REWARD_REQ               = 15002;    //CycleTaskRewardReq\n    CYCLE_TASK_REWARD_RSP               = 115002;   //CycleTaskRewardRsp\n    CYCLE_TASK_END                      = 15999;\n    \n    AGREEMENT_START                     = 16000;\n    AGREEMENT_GET_INFO_REQ              = 16001;    //GetAgreementInfoReq\n    AGREEMENT_GET_INFO_RSP              = 116001;   //GetAgreementInfoRsp\n    AGREEMENT_REWARD_REQ                = 16002;    //RewardAgreementReq\n    AGREEMENT_REWARD_RSP                = 116002;   //RewardAgreementRsp\n    AGREEMENT_END                       = 16999;\n    \n    DISPATCH_START                      = 17000;\n    DISPATCH_GET_INFO_REQ               = 17001;    //GetDispatchInfoReq\n    DISPATCH_GET_INFO_RSP               = 117001;   //GetDispatchInfoRsp\n    DISPATCH_START_REQ                  = 17002;    //StartDispatchInfoReq\n    DISPATCH_START_RSP                  = 117002;   //StartDispatchInfoRsp\n    DISPATCH_REWARD_REQ                 = 17003;    //RewardDispatchInfoReq\n    DISPATCH_REWARD_RSP                 = 117003;   //RewardDispatchInfoRsp\n    CANCEL_REWARD_REQ                   = 17004;    //CancelDispatchInfoReq\n    CANCEL_REWARD_RSP                   = 117004;   //CancelDispatchInfoRsp\n    DISPATCH_END                        = 17999;\n    \n    LIMIT_CHALLENGE_START               = 18000;\n    LIMIT_CHALLENGE_GET_INFO_REQ        = 18001;    //GetLimitChallengeInfoReq\n    LIMIT_CHALLENGE_GET_INFO_RSP        = 118001;   //GetLimitChallengeInfoRsp\n    LIMIT_CHALLENGE_RESET_REQ           = 18002;    //ResetLimitChallengeReq\n    LIMIT_CHALLENGE_RESET_RSP           = 118002;   //ResetLimitChallengeRsp\n    LIMIT_CHALLENGE_REWARD_TASK_REQ     = 18003;    //RewardLimitChallengeTaskReq\n    LIMIT_CHALLENGE_REWARD_TASK_RSP     = 118003;   //RewardLimitChallengeTaskRsp\n    LIMIT_CHALLENGE_END                 = 18999;\n}\n\nenum RET_CODE {\n    RC_OK                               = 0;                //正常\n    RC_INTERNAL_SERVER_ERROR            = 500;              //内部服务错误\n    RC_PARAM_ERROR                      = 1000;             //参数错误\n    RC_PB_ERROR                         = 1001;             //proto buffer序列化反序列化错误\n    RC_NO_MSG_HANDLER                   = 1002;             //没有找到消息处理器\n    RC_DB_NOT_EXIST                     = 1003;             //数据库不存在\n    RC_DB_OP_ERROR                      = 1004;             //DB操作失败\n    RC_DATA_NOT_FOUND                   = 1005;             //未查询到数据\n    RC_RPC_ERROR                        = 1006;             //RPC调用失败\n    RC_ID_EXHAUSTED                     = 1007;             //ID耗尽\n    RC_DELAY_RESPONSE                   = 1008;             //延时回复\n    RC_SERVICE_ABNORMAL                 = 1009;             //服务异常\n    RC_SERVICE_TIMEOUT                  = 1010;             //服务超时\n    RC_REDIS_ABNORMAL                   = 1011;             //redis服务异常\n    RC_INTERNAL_DATA_ERROR              = 1012;             //内部数据错误\n    RC_TRANSACTION_OP_NOT_SUPPORTED     = 1013;             //不支持的事务操作\n    RC_DB_DUPLICATE_KEY_ERROR           = 1014;             //DB键值重复\n    RC_RSP_PKG_CACHE_EXPIRE             = 1015;             //缓存的回复包过期\n    RC_SERVICE_CLOSED                   = 1016;             //服务器未开启\n    RC_SERVICE_BUSY                     = 1017;             //服务器忙，排队等待\n    RC_GAIN_DISTRIBUTE_LOCK_FAIL        = 1018;             //获取分布式锁失败\n    RC_ALL_GAME_SERVER_FULL             = 1019;             //服务器人数已满, 暂时无法登录\n    RC_RPC_NATS_ABNORMAL                = 1020;             //RPC nats 异常\n    RC_ALLOC_WORKER_ID_FAIL             = 1021;             //workerId 分配失败\n    RC_NO_AVAILABLE_GAME_NODE           = 1022;             //没有可用的 gamesvr 节点\n    RC_RESEND_CACHE_MISS                = 1023;             //重发请求缓存 miss\n\n    \n    RC_ACCOUNT_EXIST                    = 1100;             //账号已存在\n    RC_WRONG_ACCOUNT_OR_PASSWORD        = 1101;             //账号不存在或密码错误\n    RC_TOKEN_INVALID                    = 1102;             //token失效\n    RC_TOKEN_EXPIRE                     = 1103;             //token已过期\n    RC_TOKEN_NOT_AUTHED                 = 1104;             //未验证token\n    RC_TOKEN_ILLEGAL                    = 1105;             //token不合法\n    RC_ENTER_GAME_FAIL                  = 1106;             //进入gameSvr失败\n    RC_ACTOR_NOT_EXIST                  = 1107;             //角色不存在\n    RC_ACTOR_OFFLINE                    = 1108;             //角色离线\n    RC_CONFIG_DATA_NOT_EXIST            = 1109;             //配置数据不存在\n    RC_CONFIG_DATA_ERROR                = 1110;             //配置数据错误\n    RC_ACTOR_LEVEL_LOW                  = 1111;             //团队等级不达标\n    RC_ACCOUNT_NOT_EXIST                = 1112;             //账号不存在\n    RC_FUNCTION_NOT_UNLOCK              = 1113;             //功能未开启\n    RC_SERVER_IN_MAINTAIN               = 1114;             //服务器维护中\n    RC_NO_PRIVILEGE                     = 1115;             //无权限\n    RC_REACH_USER_CREATE_LIMIT          = 1116;             //已达到服务器创建角色数量限制\n\n    RC_INHERIT_CODE_OR_PASSWORD_WRONG   = 1150;             //引继码或密码错误\n    RC_INHERIT_CODE_INVALID             = 1151;             //引继码已失效\n    RC_INHERIT_ACCOUNT_EXIST            = 1152;             //引继账号已存在\n\n    RC_ITEM_NOT_ENOUGH                  = 1200;             //物品不足\n    RC_ITEM_NOT_EXIST                   = 1201;             //物品不存在\n    RC_ITEM_BUY_TIMES_MAX               = 1202;             //购买次数达到上限\n    RC_ITEM_COUNT_NOT_ENOUGH            = 1203;             //物品数量不足\n    RC_ITEM_CANNOT_SALE                 = 1204;             //物品不能卖出\n    RC_ITEM_NOT_CONFORM_EXCHANGE_RULE   = 1205;             //不符合兑换规则\n    RC_ITEM_COUNT_MAX                   = 1206;             //资源数量上限\n    RC_ITEM_EMOJI_NOT_OWN               = 1207;             //暂未获得该表情\n\n    RC_MAIL_NOT_EXIST                   = 1250;             //邮件不存在\n    RC_MAIL_ATTACHMENT_FETCHED          = 1251;             //已领取附件\n    RC_MAIL_EXPIRED                     = 1252;             //邮件已过期\n    RC_MAIL_CANNOT_DELETE               = 1253;             //该邮件不能删除\n\n    RC_CARD_LEVEL_LIMIT                 = 1300;             //卡牌等级达到上限\n    RC_CARD_QUALITY_LIMIT               = 1301;             //卡牌突破达到上限\n    RC_CARD_NOT_EXIST                   = 1302;             //卡牌不存在\n    RC_CARD_SKILL_NOT_UNLOCKED          = 1303;             //卡牌技能未解锁\n    RC_CARD_SKILL_LEVEL_LIMIT           = 1304;             //卡牌技能等级达到上限\n    RC_CARD_GRADE_LIMIT                 = 1305;             //卡牌觉醒达到上限\n    RC_CARD_LEVEL_NOT_MAX               = 1306;             //卡牌等级未达到上限\n    RC_CARD_QUALITY_NOT_SATISFIED       = 1307;             //卡牌突破等级不足\n    RC_CARD_NOT_OWN_FASHION             = 1308;             //卡牌没有该时装\n    RC_CARD_GRADE_UP_MATERIAL_ENOUGH    = 1311;             //已拥有足够的觉醒材料\n\n    RC_SCENE_CHAPTER_NOT_OPEN           = 1400;             //章节未开启\n    RC_SCENE_PRE_NOT_PASS               = 1401;             //前置关卡未通过\n    RC_SCENE_CHALLENGE_COUNT_MAX        = 1403;             //关卡挑战次数已达上限\n    RC_SCENE_NOT_UNLOCKED               = 1404;             //副本未解锁\n    RC_SCENE_NOT_OPEN                   = 1405;             //副本暂未开放\n    RC_SCENE_SVR_BATTLE_CALC_UN_MATCH   = 1406;             //服务器计算的战斗结果和客户端的不一致\n    RC_SCENE_BATTLE_INIT_DATA_ERROR     = 1407;             //战斗初始化数据错误\n    RC_SCENE_CHAPTER_REWARD_FETCHED     = 1408;             //章节奖励已领取\n    RC_SCENE_NOT_PASS_CHAPTER           = 1409;             //未通关章节\n    RC_SCENE_CUR_STAGE_NOT_OPEN         = 1410;             //当前关卡未开启\n    RC_SCENE_STAGE_REWARD_FETCHED       = 1411;             //关卡奖励已领取\n    RC_SCENE_NOT_PASS_STAGE             = 1412;             //未通过该关卡\n\n    RC_RELATION_BEEN_FRIEND             = 1500;             //已建立好友关系\n    RC_RELATION_APPLYING                = 1502;             //已申请添加对方为好友\n    RC_RELATION_BLOCK_TARGET            = 1503;             //已屏蔽对方, 不能添加好友\n    RC_RELATION_BLOCKED_BY_TARGET       = 1504;             //已被对方屏蔽\n    RC_RELATION_FRIEND_MAX              = 1506;             //当前好友数量达到上限\n    RC_RELATION_TARGET_FRIEND_MAX       = 1507;             //对方好友数量达到上限\n    RC_RELATION_FRIEND_AND_APPLYING_MAX = 1508;             //当前好友和已申请数量达到上限\n    RC_RELATION_APPLY_CANCELED          = 1510;             //好友申请已被取消\n    RC_RELATION_BLOCK_MAX               = 1511;             //屏蔽列表达到上限\n    RC_RELATION_REMARK_NON_FRIEND       = 1512;             //不是好友, 无法设置备注名\n    RC_RELATION_CANNOT_BLOCK_FRIEND     = 1513;             //无法屏蔽好友\n    RC_RELATION_TARGET_FUNC_NOT_OPEN    = 1514;             //对方的好友功能未开启\n    RC_RELATION_NEED_REM_BLOCK          = 1515;             //该玩家在屏蔽列表中，请先移除屏蔽\n\n\n    RC_TASK_NOT_FINISHED                = 1600;             //任务未完成\n    RC_TASK_HAS_FETCH_REWARD            = 1601;             //已领取奖励\n    RC_TASK_NOT_EXIST                   = 1602;             //任务不存在\n\n    RC_BADGE_LEVEL_MAX                  = 1702;             //徽章等级达到上限\n    RC_BADGE_NOT_ACTIVATED              = 1703;             //徽章未激活\n    RC_BADGE_HAS_WEAR                   = 1704;             //角色已穿戴该徽章\n    RC_BADGE_NOT_WEAR                   = 1705;             //未穿戴该徽章\n    RC_BADGE_NO_DECOMPOSE               = 1706;             //没有可分解的徽章\n\n    RC_GM_REPEATED_MAIL                 = 1800;             //重复发送邮件\n    RC_GM_SYSTEM_MAIL_HAS_SEND          = 1801;             //系统邮件已发送\n\n    RC_BOSS_NOT_EXIST                   = 1903;             //boss不存在\n    RC_ACTIVITY_BOSS_CLOSED             = 1905;             //活动 boss 已关闭\n\n    RC_OP_ACTIVITY_ITEM_NOT_OFF_SHELF   = 2000;             //活动条目未处于下架状态\n    RC_OP_ACTIVITY_ITEM_NOT_REMOVED     = 2001;             //活动条目未处于移除状态\n    RC_OP_ACTIVITY_ITEM_WAIT_VERIFY     = 2002;             //活动条目审核中\n    RC_OP_ACTIVITY_ITEM_CANNOT_SELL     = 2003;             //无法出售\n    RC_OP_LOGIN_NOTICE_EXIST            = 2004;             //登录公告已存在\n    RC_OP_MAIL_ITEM_EXCEED_LIMIT        = 2005;             //邮件附件物品数量超出限制\n    RC_OP_GM_OPERATE_USER_FAIL          = 2006;             //GM 操作玩家失败\n    RC_OP_NO_TARGET_CHANNEL             = 2007;             //没有目标渠道\n\n    RC_MANOR_NOT_FOUND_EVENT            = 2100;             //未找到事件\n    RC_MANOR_EVENT_HAS_FINISHED         = 2101;             //事件已完成\n    RC_MANOR_PRE_NODE_NOT_FINISHED      = 2102;             //前置节点未完成\n    RC_MANOR_EVENT_CANNOT_TRIGGER       = 2103;             //事件不能触发\n    RC_MANOR_NOT_IN_EVENT_GRID          = 2104;             //不在事件格子中\n    RC_MANOR_PRE_EVENT_NOT_FINISHED     = 2106;             //前置事件未完成\n    RC_MANOR_PLOT_EVENT_EXIST_IN_GROUP  = 2107;             //同组支线事件已存在\n    RC_MANOR_PLOT_EVENT_NODE_CONFIG_ERR = 2108;             //支线事件节点配置错误\n    RC_MANOR_FIX_BUILDING_TIMES_OVER    = 2109;             //固定建筑次数已用完\n    RC_MANOR_NO_PLOT_EVENT_CARD         = 2110;             //没有支线事件的角色\n    RC_MANOR_MAP_SUB_NOT_OPEN           = 2111;             //当前不在目标的地图区域中\n    RC_MANOR_PLOT_BATTLE_HAS_FINISHED   = 2112;             //剧情战斗已完成\n    RC_MANOR_ACTIVITY_ROLE_PLOT_SUSPEND = 2113;             //活动支线暂停中\n    RC_MANOR_EVENT_EXPIRE               = 2114;             //该事件已过期\n\n    RC_ROGUE_GAME_RUNNING               = 2200;             //肉鸽: 当前主题局内正在进行中\n    RC_ROGUE_DIFFICULTY_LEVEL_LOCKED    = 2201;             //肉鸽: 该难度等级未解锁\n    RC_ROGUE_CARD_ATTRIB_LEVEL_MAX      = 2202;             //肉鸽: 角色属性升级已达上限\n    RC_ROGUE_TALENT_HAS_LEVELUP         = 2203;             //肉鸽: 天赋已升级\n    RC_ROGUE_PRE_TALENT_NOT_LEVELUP     = 2204;             //肉鸽: 前置天赋未升级\n    RC_ROGUE_PRE_NODE_NOT_FINISHED      = 2205;             //肉鸽: 前置节点未完成\n    RC_ROGUE_CUR_NODE_NOT_FINISHED      = 2206;             //肉鸽: 当前节点未完成\n    RC_ROGUE_RANDOM_POOL_ERR            = 2207;             //肉鸽: 随机池错误\n    RC_ROGUE_NODE_REWARD_NOT_FETCHED    = 2208;             //肉鸽: 还有节点奖励未领取\n    RC_ROGUE_NODE_REWARD_FETCHED        = 2209;             //肉鸽: 该奖励已领取\n    RC_ROGUE_CARD_RECRUITED             = 2210;             //肉鸽: 该角色已招募\n    RC_ROGUE_HAS_OWN_TREASURE           = 2211;             //肉鸽: 已拥有该宝物\n    RC_ROGUE_SHOP_TREASURE_NOT_EXIST    = 2212;             //肉鸽: 商店没有该宝物\n    RC_ROGUE_SHOP_RESET_MAX             = 2213;             //肉鸽: 商店重置次数达到上限\n    RC_ROGUE_GAME_NOT_RUNNING           = 2214;             //肉鸽: 本局未开始\n    RC_ROGUE_THEME_LEVEL_LOW            = 2215;             //肉鸽: 主题等级不足\n    RC_ROGUE_INITIAL_RECRUIT_DONE       = 2216;             //肉鸽: 已完成初始招募\n    RC_ROGUE_NODE_FINISHED_CANNOT_REWARD= 2217;             //肉鸽: 该节点已完成,无法领取奖励\n    RC_ROGUE_OWN_ALL_TREASURE           = 2218;             //肉鸽: 已拥有该节点全部宝物，无法再获得\n    RC_ROGUE_NO_SWEEP_COUNT             = 2219;             //肉鸽: 没有快速探索次数\n    RC_ROGUE_CUR_NODE_FINISHED          = 2220;             //肉鸽: 当前节点已完成\n\n    RC_EXCHANGE_CODE_NOT_EXIST          = 2300;             //兑换码不存在\n    RC_EXCHANGE_CODE_USED               = 2301;             //该兑换码已使用\n    RC_EXCHANGE_CODE_USE_TIMES_MAX      = 2302;             //该兑换码的兑换次数已达上限\n    RC_EXCHANGE_CODE_EXPIRE             = 2303;             //兑换码已过期\n    RC_EXCHANGE_CODE_NO_PERMISSION      = 2304;             //没有该兑换码使用权限\n    RC_EXCHANGE_CODE_LEVEL_LOW          = 2306;             //无法使用该兑换码, 等级需要达到%s级\n    RC_EXCHANGE_CODE_LEVEL_HIGH         = 2307;             //无法使用该兑换码, 等级不能超过%s级\n\n    //公会战\n    RC_GUILD_WAR_NOT_START              = 2400;             //公会战未开启\n    RC_GUILD_WAR_SKILL_NOT_EXIST        = 2401;             //不存在该战术技能\n    RC_GUILD_WAR_SKILL_LEVEL_MAX        = 2402;             //该战术技能已达最高等级\n    RC_GUILD_WAR_NOT_PARTICIPATE        = 2403;             //暂未参与公会战\n    RC_GUILD_WAR_BOSS_DEAD              = 2404;             //该 boss 已阵亡\n    RC_GUILD_WAR_NO_FIGHT_COUNT         = 2405;             //今日挑战次数已用完\n    RC_GUILD_WAR_COMPENSATE_NOT_EXIST   = 2406;             //不存在该延长阵容\n    RC_GUILD_WAR_CANNOT_REPEAT_USE_CARD = 2407;             //不能重复使用角色\n    RC_GUILD_WAR_FIGHT_STATE_FINISHED   = 2408;             //公会战挑战期已结束\n    RC_GUILD_WAR_BOSS_DEAD_BEFORE       = 2409;             //该 boss 已先阵亡,结算失败\n    RC_GUILD_WAR_FIGHT_CANNOT_EXIT      = 2410;             //公会战挑战期间不能退出公会\n    RC_GUILD_WAR_FIGHT_CANNOT_DISMISS   = 2411;             //公会战挑战期间不能解散\n    RC_GUILD_WAR_FIGHT_CANNOT_KICK      = 2412;             //公会战挑战期间不能踢出成员\n\n    //印章\n    RC_SEAL_LEVEL_MAX                   = 2413;             //印章已达最高级\n    RC_SEAL_BIG_LEVEL_LIMIT             = 2414;             //大印章等级已达到上限\n    RC_SEAL_BIG_QUALITY_MAX             = 2415;             //大印章突破已达到上限\n    RC_SEAL_BIG_ADD_UP_MAX              = 2416;             //大印章增幅已达到上限\n    RC_SEAL_BIG_LEVEL_LOW               = 2417;             //大印章等级不足\n\n    // 第三方 sdk 返回的错误码转换\n    //bilbili 错误码\n    RC_BILIBILI_ACCOUNT_NOT_LOGIN       = 3000;             //帐号未登陆\n    RC_BILIBILI_ACCOUNT_BANNED          = 3001;             //账号被封停\n    RC_BILIBILI_PARAM_ERROR             = 3002;             //请求参数错误\n    RC_BILIBILI_SERVER_INTERNAL_ERROR   = 3004;             //服务器内部错误\n    RC_BILIBILI_CALL_TOO_RAPID          = 3005;             //调用速度过快\n    RC_BILIBILI_USER_NOT_ACTIVE         = 3006;             //游戏封测，用户未激活\n    //bilbili 错误码---end\n\n    RC_IM_GROUP_MAX_MEMBERS             = 5202;             //群聊成员数量达上限\n    RC_IM_WORLD_GROUP_NOT_EXIST         = 5204;             //世界频道不存在\n    RC_IM_CHANNEL_IN_CD                 = 5205;             //频道 cd 中\n    RC_IM_MUTED_BY_SYSTEM               = 5206;             //被系统禁言中\n    RC_IM_MUTED_REASON_SENSITIVE        = 5207;             //禁言原因: 多次发送敏感词\n    RC_IM_MUTED_REASON_REPORT_SENSITIVE = 5208;             //禁言原因: 被多人举报且含有敏感词\n    RC_IM_MUTED_REASON_REPORT           = 5209;             //禁言原因: 被多人举报\n    RC_IM_MUTED_REASON_REPEAT_MSG       = 5210;             //禁言原因: 连续发送重复消息\n    RC_IM_MUTED_REASON_GM               = 5211;             //禁言原因: 被 GM 禁言\n\n    RC_GUILD_NOT_EXIST                  = 5300;             //公会不存在\n    RC_GUILD_NOT_IN                     = 5301;             //未在公会中\n    RC_GUILD_HAS_IN                     = 5302;             //已在公会中\n    RC_GUILD_IN_JOIN_CD                 = 5303;             //申请加入公会CD中\n    RC_GUILD_MEMBER_MAX                 = 5304;             //公会成员达到上限\n    RC_GUILD_APPLICANT_MAX              = 5305;             //公会申请人达到上限\n    RC_GUILD_USER_APPLIED_MAX           = 5306;             //玩家申请的公会数量达到上限\n    RC_GUILD_APPLICANT_NOT_EXIST        = 5307;             //该申请人不存在\n    RC_GUILD_VICE_LEADER_MAX            = 5308;             //副队长数量达到上限\n    RC_GUILD_NOT_MEMBER                 = 5309;             //对方不是公会成员\n    RC_GUILD_NO_PERMISSION              = 5310;             //没有操作权限\n    RC_GUILD_NAME_OCCUPIED              = 5311;             //公会名字已被占用\n    RC_GUILD_IN_RECOMMEND_CD            = 5312;             //公会推荐 CD 中\n    RC_GUILD_IMPEACHING                 = 5313;             //正在弹劾中\n    RC_GUILD_NOT_MEET_IMPEACH_COND      = 5314;             //不满足弹劾条件\n    RC_GUILD_NO_IMPEACH_VOTE_PERMISSION = 5315;             //目前没有投票权限\n    RC_GUILD_NOT_IMPEACHING             = 5316;             //目前不在弹劾期\n    RC_GUILD_IMPEACH_VOTED              = 5317;             //弹劾队长已投票\n    RC_GUILD_IMPEACH_INITIATOR_NO_EXIT  = 5318;             //弹劾期间发起人不能退出公会\n    RC_GUILD_IMPEACH_INITIATOR_NO_KICK  = 5319;             //不能踢出弹劾发起人\n    RC_GUILD_NOT_FOUND_PROPER_GUILD     = 5320;             //未找到合适的公会\n    RC_GUILD_NO_QUICK_JOIN_LEVEL_LIMIT  = 5321;             //不能快速加入设置了等级条件的公会\n    RC_GUILD_REJECT_JOIN                = 5322;             //探险队拒绝加入\n    RC_GUILD_CHAT_BLOCKED_BY_GM         = 5323;             //探险队聊天被 GM 屏蔽\n    RC_GUILD_NOT_OWN_HEAD_ID            = 5324;             //暂未获得该头像\n\n    RC_ARENA_NOT_FOUND                  = 5400;             //未找到赛区\n    RC_ARENA_ACTOR_CLOSED\t            = 5402;             //竞技场关闭中\n    RC_ARENA_FIGHT_NUM_EXIST\t        = 5403;             //还有挑战次数不能重置\n    RC_ARENA_FIGHT_CD\t                = 5404;             //竞技场挑战CD中\n    RC_ARENA_FIGHT_NO_NUM   \t        = 5405;             //竞技场挑战次数不足\n    RC_ARENA_OPPONENT_CHANGE       \t    = 5407;             //竞技场对手已经变化\n    RC_ARENA_TARGET_CANT_FIGHT          = 5408;             //竞技场对上无法挑战\n    \n    RC_SHOP_GOODS_NOT_EXIST             = 5501;             //商品不存在\n    RC_SHOP_GOODS_SOLD_OUT              = 5502;             //商品已售完\n    RC_SHOP_GRID_NOT_UNLOCKED           = 5504;             //商品未解锁\n    \n    RC_GACHA_POOL_LOCKED                = 5601;             //卡池未解锁\n    RC_GACHA_COUNT_MAX                  = 5602;             //已经达到抽取次数上限\n    RC_GACHA_POINT_NOT_ENOUGH           = 5603;             //积分不足\n    RC_GACHA_EXCHANGE_LIMIT_MAX         = 5604;             //兑换达到上限\n    RC_GACHA_EXTRA_REWARDED             = 5605;             //额外奖励已经领取\n    RC_GACHA_EXTRA_CARD_NOT_FOUND       = 5606;             //额外奖励卡片不存在\n\n    RC_SIGN_HAS_SIGNED                  = 5701;             //已经签过到\n    \n    RC_ACTOR_BANNED                     = 5801;             //角色被ban\n    \n    RC_BATTLEPASS_OUT_TIME              = 5901;             //通行证未在有效期\n    RC_BATTLEPASS_EXP_MAX               = 5902;             //通行证经验上限\n    RC_BATTLEPASS_NO_TASK               = 5903;             //通行证没有可以刷新的任务\n    \n    RC_CARNIVAL_REWARDED                = 6001;             //嘉年华奖励已经领取\n    RC_CARNIVAL_CLOSED                  = 6002;             //嘉年华活动已关闭\n\n    RC_PURCHASE_MONTHCARD_REWARDED      = 6100;             //月卡已经领取过\n    RC_PURCHASE_MONTHCARD_EXPIRED       = 6101;             //月卡已经到期\n    RC_PURCHASE_MONTHCARD_MAX           = 6102;             //月卡天数已满\n    \n    RC_ACTIVITY_NOT_EXIST               = 6201;             //活动不存在\n    RC_ACTIVITY_CAN_NOT_SIGNIN          = 6202;             //无法签到\n    RC_ACTIVITY_ON_SHELF_EXIST          = 6203;             //该活动已上架过\n    \n    RC_BOSS_CHALLENGE_NOT_EXIST         = 6301;             //当前没有挑战活动\n    RC_BOSS_CHALLENGE_FIGHT_NOT_ENOUGH  = 6302;             //挑战次数不足\n    RC_BUFF_STAGE_CHALLENGE_NOT_REACH   = 6303;             //buff stage目标未达成\n    \n    RC_AGREEMENT_REWARDED               = 6401;             //密约已经领取了\n    RC_AGREEMENT_NOT_OPEN               = 6402;             //密约未开放\n}\n\n//日志类型\nenum LOG_ID {\n    LI_NONE                          = 0;\n    //消耗\n    CONSUME_LEVELUP                  = 10001;             //卡牌升级\n    CONSUME_QUALITY_UP               = 10002;             //卡牌突破\n    CONSUME_SKILL_LEVELUP            = 10003;             //卡牌技能升级\n    CONSUME_GRADE_UP                 = 10004;             //卡牌觉醒\n    CONSUME_CHALLENGE_STAGE          = 10005;             //挑战关卡消耗\n    CONSUME_BADGE_ACTIVATE           = 10006;             //徽章激活\n    CONSUME_BADGE_GRADE_UP           = 10007;             //徽章觉醒\n    CONSUME_BADGE_LEVELUP            = 10008;             //徽章升级\n    CONSUME_BUY_ENERGY               = 10009;             //购买体力\n    CONSUME_USE_PACKAGE              = 10011;             //使用礼包时消耗\n    CONSUME_ITEM_EXPIRED             = 10012;             //物品过期后自动删除\n    CONSUME_CREATE_GUILD             = 10013;             //创建公会消耗\n    CONSUME_EXCHANGE_ITEM            = 10014;             //兑换物品消耗\n    CONSUME_CHANGE_GUILD_NAME        = 10015;             //修改公会名字消耗\n    CONSUME_CHANGE_NAME              = 10016;             //修改名字消耗\n    CONSUME_EXCHANGE_ENERGY          = 10018;             //体力药水兑换体力\n    CONSUME_PROCESS_MANOR_EVENT      = 10019;             //处理探索地图事件消耗\n    CONSUME_CLI_GM                   = 10020;             //通过 gm 指令消耗\n    CONSUME_BATCH_USE_ITEMS          = 10021;             //批量使用物品\n    CONSUME_GACHA_COST               = 10022;             //抽卡消耗\n    CONSUME_BUY_BATTLEPASS_LEVEL     = 10023;             //购买通行证等级消耗\n    CONSUME_BUY_GIFT                 = 10024;             //礼包购买消耗\n    CONSUME_SALE_ITEM                = 10025;             //卖出物品消耗\n    CONSUME_TASK_ITEM_EXPIRE         = 10026;             //任务物品过期删除\n    CONSUME_RESET_ARENA_FIGHT_NUM    = 10027;             //重置竞技场次数消耗\n    CONSUME_REFRESH_ARENA_FIGHT_CD   = 10028;             //刷新竞技场挑战CD消耗\n    CONSUME_BUY_FASHION              = 10029;             //购买时装消耗\n    CONSUME_FORCE_REFRESH_SHOP_GOODS = 10030;             //强制刷新商店消耗\n    CONSUME_ACTIVITY_SLOT            = 10031;             //活动 slot 消耗\n    CONSUME_BUY_SHOP_GOODS           = 10032;             //购买商店物品消耗\n    CONSUME_DAILY_SUPPLY             = 10033;             //每日补给补领消耗\n    CONSUME_GM_DEDUCT                = 10034;             //GM 扣除\n    CONSUME_ROGUE_ENHANCE_CARD       = 10035;             //肉鸽: 强化角色消耗\n    CONSUME_ROGUE_ACTIVATE_TALENT    = 10036;             //肉鸽: 激活天赋消耗\n    CONSUME_ROGUE_REVIVE_CARD        = 10037;             //肉鸽: 复活角色消耗\n    CONSUME_ROGUE_AUTO_CLEAN         = 10038;             //肉鸽: 单局结束后自动清理资源\n    CONSUME_ROGUE_BUY_TREASURE       = 10039;             //肉鸽: 购买宝物消耗\n    CONSUME_ROGUE_RESET_SHOP         = 10040;             //肉鸽: 重置商店节点消耗\n    CONSUME_ROGUE_RECRUIT            = 10041;             //肉鸽: 招募角色消耗\n    CONSUME_ROGUE_EVENT_STORY        = 10042;             //肉鸽: 事件节点剧情消耗\n    CONSUME_RECHARGE_REFUND_DEDUCT   = 10050;             //充值退款扣除\n    CONSUME_GUILD_WAR_SKILL_LEVELUP  = 10051;             //公会战: 战术技能升级消耗\n    CONSUME_DISPATCH_EXTRA           = 10052;             //额外派遣\n    CONSUME_GUILD_WAR_SEASON_RESET   = 10053;             //公会战: 赛季重置自动扣除\n    CONSUME_WEAR_SEAL                = 10054;             //穿戴印章消耗\n    CONSUME_SEAL_COMPOSITE           = 10055;             //合成印章消耗\n    CONSUME_ACTIVITY_TURNTABLE       = 10056;             //活动转盘\n    CONSUME_ACTIVITY_REVIEW          = 10057;             //回归活动消耗\n    CONSUME_SEAL_BIG_LEVELUP         = 10058;             //大印章升级消耗\n    CONSUME_SEAL_BIG_QUALITY_UP      = 10059;             //大印章突破消耗\n    CONSUME_SEAL_BIG_ADD_UP          = 10060;             //大印章增幅消耗\n    CONSUME_SEAL_HOOK_FAST_COLLECT   = 10061;             //刻印挂机快速采集消耗\n\n    //获得\n    GAIN_ROLE_INITIAL                = 20001;             //获得初始资源\n    GAIN_AUTO_RECOVER                = 20002;             //物品自动回复\n    GAIN_MAIN_LINE_STAGE             = 20003;             //主线剧情副本\n    GAIN_MAIL_ATTACHMENT             = 20004;             //邮件附件\n    GAIN_BUY_ENERGY                  = 20005;             //购买体力\n    GAIN_BUY_SHOP_GOODS              = 20007;             //购买商店商品\n    GAIN_USE_PACKAGE                 = 20009;             //使用礼包时获得\n    GAIN_BATTLEPASS_REWARD           = 20010;             //通行证领奖\n    GAIN_TASK_REWARD                 = 20011;             //任务领奖\n    GAIN_GACHA_REWARD                = 20013;             //招募奖励\n    GAIN_EXCHANGE_ITEM               = 20014;             //兑换物品获得\n    GAIN_BUY_BATTLEPASS_LV           = 20015;             //购买通行证等级\n    GAIN_REWARD_ARENA_TASK           = 20019;             //领取竞技场任务奖励\n    GAIN_REWARD_CARNIVAL             = 20020;             //领取通行证\n    GAIN_PURCHASE_BUY                = 20022;             //内购\n    GAIN_MONTHCARD_REWARD            = 20023;             //月卡领奖\n    GAIN_CHAPTER_REWARD              = 20024;             //章节奖励\n    GAIN_FETCH_STAGE_REWARD          = 20025;             //领取的关卡奖励\n    GAIN_ACTIVITY_SIGNIN             = 20026;             //活动签到\n    GAIN_ACTIVITY_SHOP               = 20027;             //活动商店\n    GAIN_ACTIVITY_TASK               = 20028;             //活动任务\n    GAIN_ACTIVITY_MINIGAME           = 20029;             //活动小游戏\n    GAIN_PLANT_FLOWER_REWARD         = 20032;             //植物花朵奖励\n    GAIN_FINISH_PLOT                 = 20033;             //完成剧情的奖励\n    GAIN_ACTIVITY_SEARCH             = 20034;             //搜索活动\n    GAIN_EXCHANGE_ENERGY             = 20035;             //体力药水兑换体力\n    GAIN_PROCESS_MANOR_EVENT         = 20036;             //处理探索地图事件\n    GAIN_CLI_GM                      = 20037;             //通过 gm 指令获得\n    GAIN_GACHA_EXCHANGE              = 20038;             //招募兑换\n    GAIN_GACHA_EXTRA                 = 20039;             //招募额外奖励\n    GAIN_BATCH_USE_ITEMS             = 20040;             //批量使用物品获得\n    GAIN_NORMAL_SIGNIN               = 20041;             //普通签到\n    GAIN_SALE_ITEM                   = 20042;             //卖出物品获得\n    GAIN_PLAYER_LEVELUP_REWARD       = 20043;             //玩家升级奖励\n    GAIN_BUY_GIFT_PACKAGE            = 20044;             //购买礼包时获得奖励\n    GAIN_DECOMPOSE_BADGE             = 20045;             //分解徽章获得\n    GAIN_BADGE_LEVELUP_RETURN        = 20046;             //徽章升满级时的材料返还\n    GAIN_EXPEDITION_REWARD           = 20047;             //远征奖励\n    GAIN_GIFT_REWARD                 = 20048;             //礼包奖励\n    GAIN_ACTIVITY_TRANS              = 20049;             //活动转化\n    GAIN_ACTIVITY_STAGE              = 20050;             //活动关卡\n    GAIN_DAILY_SUPPLY                = 20051;             //每日补给\n    GAIN_BOSS_CHAllENGE_FIGHT        = 20052;             //boss挑战战斗奖励\n    GAIN_BUFF_STAGE_REWARD           = 20053;             //buff stage奖励\n    GAIN_ROGUE_NODE_REWARD_OPTION    = 20054;             //肉鸽: 节点奖励选项\n    GAIN_ROGUE_THEME_LEVEL_REWARD    = 20055;             //肉鸽: 主题等级奖励\n    GAIN_ROGUE_NEW_GAME              = 20056;             //肉鸽: 开局获得的奖励\n    GAIN_ROGUE_ENTER_NODE_REWARD     = 20057;             //肉鸽: 进入节点的奖励(宝物效果)\n    GAIN_ROGUE_ENTER_NEW_LAYER_REWARD= 20058;             //肉鸽: 进入下一层获得奖励(宝物效果)\n    GAIN_ROGUE_TREASURE_EFFECT_REWARD= 20059;             //肉鸽: 获得宝物触发的一次性奖励\n    GAIN_ROGUE_SETTLE_REWARD         = 20060;             //肉鸽: 结算奖励\n    GAIN_USE_EXCHANGE_CODE           = 20061;             //使用兑换码获得奖励\n    GAIN_AGREEMENT_REWARD            = 20062;             //密约领奖\n    GAIN_DISPATCH_REWARD             = 20063;             //派遣领奖\n    GAIN_DISPATCH_CANCEL_RETURN      = 20064;             //派遣取消返还\n    GAIN_RETURN_SIGN_IN              = 20070;             //回归签到\n    GAIN_SEAL_TAKE_OFF               = 20071;             //取下印章获得\n    GAIN_SEAL_COMPOSITE              = 20072;             //合成印章获得\n    GAIN_WEEK_ACCUM_PAY              = 20073;             //每周累充奖励\n    GAIN_ACTIVITY_TURNTABLE          = 20074;             //活动转盘获得\n    GAIN_SEAL_BIG_HOOK               = 20075;             //大刻印挂机奖励\n    GAIN_ACCUM_RECHARGE_REWARD       = 20076;             //累充奖励\n    GAIN_CARD_HAND_BOOK_REWARD       = 21001;             //角色图鉴奖励\n}\n\n//通知类型\nenum EVENT_TYPE {\n    ET_NONE                 = 0;\n    //推送给客户端的事件, 需要定义一个消息 cmd, 用于客户端导出\n    ET_CARD_UPDATE          = 1;        //CardUpdateNotify      卡牌更新通知\n    ET_IM_NEW_MESSAGE       = 2;        //NewMessageNotify      新消息通知\n    ET_ITEM_CHANGED         = 3;        //SyncItemsRsp          物品变更通知\n    ET_RELATION_CHANGED     = 4;        //RelationChangedNotify 好友请求\n    ET_NEW_MAIL             = 5;        //NewMailNotify         新邮件通知\n    ET_KICK_OFF             = 6;        //KickOffNotify         踢下线\n    ET_MUTED_BY_SYSTEM      = 7;        //MutedBySystemNotify   被系统禁言通知\n    ET_ACTOR_UPDATE         = 8;        //ActorInfoUpdateNotify 玩家信息更新通知\n    ET_NEW_BADGE            = 9;        //NewBadgeNotify        新增徽章通知\n    ET_RELATION_DEL_APPLICANT = 10;     //RelationDelApplicantNotify    删除好友请求通知\n    ET_MANOR_EVENT          = 12;       //ManorEventUpdateNotify    探险地图事件更新\n    ET_GUILD_EVENT          = 13;       //GuildEventNotify      公会事件通知\n    ET_MANOR_CONVEY         = 14;       //ManorConveyNotify     探险地图传送通知\n    ET_MANOR_INFO_UPDATE    = 15;       //ManorInfoUpdateNotify 探险地图信息更新通知\n    ET_BUY_BATTLEPASS_SUCCESS    = 16;     //BattlePassBuySuccessNotify      通行证购买成功通知\n    ET_BOSS_CHALLENGE_HIGH_SCORE = 17;     //BossChallengeHighScoreNotify      boss挑战最高积分通知\n    ET_ROGUE_CARD_UPDATE         = 18;     //RogueCardUpdateNotify  肉鸽角色信息更新通知\n    ET_FASHION_ADD          = 19;     //FashionAddNotify  肉鸽角色信息更新通知\n\n    //服务内部事件\n\n    //玩家进入游戏        在枚举上面写注释,规避客户端导出工具可能出现问题\n    ET_SYS_USER_ENTER_GAME  = 1000;\n    //玩家心跳  HeartBeatNotify\n    ET_SYS_USER_HEARTBEAT   = 1001;\n    //玩家离线\n    ET_SYS_USER_OFFLINE     = 1002;\n    //举报其他玩家\n    ET_SYS_REPORT_USER      = 1003;\n    //通知其他 GuildSvr 节点更新公会的推荐信息  GuildRecommendInfo\n    ET_SYS_GUILD_RECOMMEND  = 1004;\n    //公会解散\n    ET_SYS_GUILD_DISMISSED  = 1005;\n    //玩家进入公会\n    ET_SYS_GUILD_MEMBER_IN  = 1006;\n    //玩家退出公会\n    ET_SYS_GUILD_MEMBER_OUT = 1007;\n    //玩家信息更新    ActorInfo\n    ET_SYS_ACTOR_INFO_UPDATED = 1008;\n    //重新加载系统时间\n    ET_RELOAD_SYS_TIME      = 1009;\n}\n\n//事件通知\nmessage EventNotifyReq {\n    int32 eventType     = 1;    //enum EVENT_TYPE\n    bytes notifyBody    = 2;    //根据eventType对应的结构体解析\n}\n\n//事件通知\nmessage EventNotifyRsp {\n    int32 eventType     = 1;    //enum EVENT_TYPE\n    bytes notifyBody    = 2;    //根据eventType对应的结构体解析\n}\n\n//属性组\nenum ATTRIB_GROUP {\n    AG_NONE     = 0;\n    AG_CARD     = 1;    //卡牌基础属性\n    AG_LEVEL    = 2;    //等级加成\n    AG_QUALITY  = 3;    //突破加成\n    AG_BADGE    = 4;    //徽章加成\n    AG_SKILL    = 5;    //技能加成\n    AG_ROGUE_ENHANCE    = 6;    //肉鸽属性强化加成\n}\n\n//会话信息\nmessage UserSession {\n    string gtwId    = 1;\n    string gameId   = 2;\n    string dbId     = 3;\n}\n\n//邮件信息\nmessage MailInfo {\n    int64 mailUid       = 1;\n    string identify     = 2;    //标识,防止全服邮件重复发送\n    string title        = 3;    //邮件标题\n    string senderName   = 4;    //寄件人姓名\n    string content      = 5;    //邮件内容\n    string attachment   = 6;    //邮件附件 ItemTuple 三元组格式\n    int64 sendStamp     = 7;    //发送时间\n    int64 expireStamp   = 8;    //过期时间  只在发送邮件时设置为过期天数,其他时候都是真正的过期时间戳\n    int64 globalSeq     = 9;    //全服邮件 seq\n    bool canDelete      = 10;   //邮件是否能手动删除\n    bool fetched        = 11;   //是否已领取\n    bool read           = 12;   //是否已读\n\n    bool cliParse       = 13;   //如果为 true, title, senderName, content 字段发送的是文字表 id, 由客户端读取, 用下面几个字段进行参数替换\n    repeated string senderParams  = 14;     //寄件人姓名参数\n    repeated string titleParams   = 15;     //邮件标题中的参数\n    repeated string contentParams = 16;     //邮件内容中的参数\n    bool canPrior       = 17;   //邮件数量超出上限后能否被顶掉\n    string extra        = 18;    //扩充信息\n}\n\n//残血残怒状态\nmessage ObjectState {\n    int64 uid           = 1;\n    int32 id            = 2;    //cardId or monsterId\n    int32 position      = 3;    //位置\n    int64 maxHp         = 4;    //最大血量\n    int64 hp            = 5;    //当前血量\n}\n\n//游戏功能id\nenum FUNCTION_ID {\n    FD_NONE             = 0;\n    FD_BANNER           = 101;      //banner\n    FD_ACTIVITY_DROP    = 104;      //奖励翻倍活动\n    FD_GACHA            = 10103;    //扭蛋 \n    FD_BATTLE_PASS      = 10111;    //通行证\n    FD_ARENA            = 10303;    //竞技场\n    FD_BOSS_CHALLENGE   = 10304;    //BOSS挑战\n    FD_FRIEND           = 10115;    //好友\n    FD_ACTIVITY_SIGNIN  = 10118;    //签到活动\n    FD_ACTIVITY_STAGE   = 10119;    //关卡活动\n    FD_ACTIVITY_SEARCH  = 10123;    //搜索活动\n    FD_ACTIVITY_RETURN  = 10132;    //回归签到\n    FD_ACTIVITY_TURNTABLE  = 10134;    //转盘活动\n    FD_ACTIVITY_TURNTABLE_ROUND  = 10137;    //转盘（多轮）活动\n    FD_ACTIVITY_RETURN_PRO = 10138;    //玩家回归活动\n    FD_BUFF_STAGE       = 11315;    //buff关卡活动\n    FD_LIMIT_CHALLENGE  = 12601;    //限时挑战活动\n\n}\n\nenum ACTIVITY_GACHA_TYPE {\n    AGT_NONE            = 0;\n    AGT_OPNE            = 1;    //扭蛋活动开启\n    AGT_FREE            = 2;    //扭蛋活动免费次数\n}\nmessage DateTime {\n    int32 year      = 1;\n    int32 month     = 2;\n    int32 day       = 3;\n    int32 hour      = 4;\n    int32 minute    = 5;\n    int32 second    = 6;\n}\n\n\nenum CONDITION_TYPE {\n    CT_NONE         = 0;\n    CT_LEVEL        = 100;\n    CT_PASS_STAGE   = 200;\n    CT_CARD_EXP_ADD = 300;\n}\n//阵容类型\nenum BATTLE_FORMATION_TYPE {\n    BFT_NONE    = 0;\n    BFT_1       = 1;\n    BFT_2       = 2;\n    BFT_3       = 3;\n}\n\nenum PLATFORM_TYPE {\n    PFT_NONE         = 0;\n    PFT_ANDROID      = 1;\n    PFT_IOS          = 2;\n}\n\nenum TASK_BELONG_TYPE {\n    TBT_NONE            = 0;\n    TBT_BATTLEPASS      = 1;\n    TBT_CARNIVAL        = 2;\n    TBT_PLANT           = 3;\n    TBT_COMMON          = 4;\n}\nenum CHALLENGE_STAT_TYPE {\n    CST_NONE        = 0;\n    CST_FINISH      = 1;\n    CST_REWARDED    = 2;\n}\nenum TASK_CONDITION_TYPE {\n    TCT_NONE    = 0;\n    TCT_LEVEL                   = 100;  //玩家等级\n    TCT_PASS_STAGE              = 200;  //通关指定关卡\n    TCT_KILL_MONSTER_COUNT      = 201;  //击杀怪物数量\n    TCT_PASS_EXPERIMENT_COUNT   = 202;  //通过试炼次数\n    TCT_PASS_EXPERIMENT_DIFF    = 203;  //通关指定难度试炼\n    TCT_ARENA_FIGHT_COUNT       = 204;  //竞技场挑战次数\n    TCT_ARENA_REACH_RANK        = 205;  //竞技场到达排名 \n    TCT_PASS_EXPERIMENT_HIGH    = 206;  //远征历史最高关卡 \n    TCT_CLIMB_TOWER_COUNT       = 207;  //参与爬塔\n    TCT_BOSS_CHALLENGE          = 208;  //参与个人挑战战斗\n    TCT_GUILD_PRATICE           = 209;  //参与探险队演练\n    TCT_BOSS_CHALLENGE_DIFF     = 210;  //通过指定难度boss挑战\n    TCT_PASS_SPECIAL_STAGE_COUNT= 211;  //通过指定关卡数量\n    TCT_EXPEDITION_FIGHT_COUNT  = 251;  //远征挑战次数\n    TCT_BOSS_FIGHT_COUNT        = 252;  //BOSS挑战次数\n    TCT_BUILDING_FIGHT_COUNT    = 254;  //建筑关卡挑战次数\n    TCT_EXPLORE_ROUGE           = 255;  //成功探索肉鸽\n    TCT_PASS_STAGE_BY_CTYPE     = 256;  //通关指定章节type关卡\n    TCT_MINIGAME_TOTALSCORE     = 257;  //小游戏总计分数\n    TCT_MINIGAME_ONCESCORE      = 258;  //小游戏最高分数\n    TCT_MINIGAME_PLAY_COUNT     = 259;  //小游戏游玩次数\n    TCT_GUILD_WAR_FIGHT_COUNT   = 262;  //公会战挑战次数\n    TCT_GUILD_WAR_SCORE         = 263;  //工会战积分\n    TCT_ACTIVITY_PASS_STAGE_BY_CTYPE    = 264;  //通关活动指定章节类型关卡\n    TCT_ACTIVITY_MINIGAME_TOTALSCORE    = 265;  //活动小游戏总计分数\n    TCT_ACTIVITY_MINIGAME_ONCESCORE     = 266;  //活动小游戏最高分数\n    TCT_ACTIVITY_PLAY_COUNT     = 267;  //活动小游戏游玩次数\n    TCT_CARD_EXP_ADD_COUNT      = 300;  //卡片强化次数\n    TCT_CARD_LEVEL_UP_COUNT     = 301;  //卡片升级次数\n    TCT_CARD_BREAK_COUNT        = 302;  //卡片突破次数\n    TCT_CARD_LEVEL_NUM          = 351;  //卡牌指定等级数量\n    TCT_CARD_SKILL_NUM          = 352;  //卡牌指定技能数量\n    TCT_CARD_BREAK_NUM          = 353;  //卡牌指定突破数量\n    TCT_CARD_GRADE_NUM          = 354;  //卡牌指定觉醒数量\n    TCT_BADGE_LEVEL_NUM         = 355;  //徽章指定等级数量\n    TCT_BADGE_LEVEL_UP_COUNT    = 356;  //徽章指定突破数量\n    TCT_COST_RESOURCE_NUM       = 400;  //资源消耗数量\n    TCT_RESOURCE_NUM            = 401;  //持有资源数量\n    TCT_GET_COIN_NUM            = 451;  //累积获取金币\n    TCT_LOGIN_DAY               = 500;  //连续登陆天数\n    TCT_ONLINE_MIN              = 501;  //累积在线分钟\n    TCT_SHOP_BUY_COUNT          = 502;  //商店购买次数\n    TCT_ENERGY_BUY_COUNT        = 503;  //体力购买次数\n    TCT_GACHA_COUNT             = 504;  //招募次数\n    TCT_GUILD_REWARD_COUNT      = 505;  //工会补给领取次数\n    TCT_MANOR_EVENT_COUNT       = 600;  //大地图事件\n    TCT_MANOR_RESOURCE_NUM      = 601;  //大地图资源\n    TCT_MANOR_SPECIAL_EVENT_COUNT       = 602;  //大地图指定事件\n    TCT_ROGUE_DIFFICULTY_LEVEL_COUNT    = 701;  //指定主题下，通关指定难度N次\n    TCT_ROGUE_COST_TOKEN                = 702;  //指定主题下，单局中累计消耗N货券\n    TCT_ROGUE_EVENT_COUNT               = 703;  //指定主题下，单局中累计完成事件区域N次\n    TCT_ROGUE_TREASURE_PIC              = 704;  //指定主题下，图鉴中解锁N个宝物\n    TCT_ROGUE_COST_ATTRIB_POINT         = 705;  //指定主题下，单局中累计消耗N点荣誉\n    TCT_ROGUE_BATTLE_COUNT              = 706;  //指定主题下，累计通过战斗区域N次\n    TCT_ROGUE_TRIGGER_ENDING_COUNT      = 707;  //指定主题下，完成指定结局ID N次\n    TCT_ROGUE_GAIN_TOKEN                = 708;  //指定主题下，单局中累计获得N货券\n    TCT_ROGUE_SCORE                     = 709;  //指定主题下，指定难度下，单局最高评分达到XXX\n}\n\n\n//所有需要写入db的数据模型在这里定义,避免使用嵌套结构\n\n\n\nmessage UserLoginLog {\n    int64 uin       = 1;\n    string dbId     = 2;\n    string openId   = 3;\n}\n\n//用于分配自增 id 的表  route.incr_id_alloc\nmessage IncrIdAlloc {\n    string name     = 1;\n    int64 incrId    = 2;\n}\n\n//每个服务节点分配的 workerId    route.service_node\nmessage ServiceNodeInfo {\n    string serviceId  = 1;\n    int32 workerId    = 2;\n    int64 stamp       = 3;\n}\n\n//用户账户信息 account.account\nmessage AccountInfo {\n    string accountId    = 1;\n    string password     = 2;\n    string accountType  = 3;    //ssoul wx\n    string openId       = 4;\n    string imei         = 5;\n    string osVersion    = 6;\n    int32 platform      = 7;\n    string channel      = 8;\n    int64 createStamp   = 9;\n}\n\n//引继码 account.inherit_account\nmessage InheritAccountInfo {\n    string inheritCode      = 1;\n    string openId           = 2;\n    string password         = 3;\n    int64 createStamp       = 4;\n    string bindAccountId    = 5;    //该引继码绑定的 accountId\n    int32 used              = 6;\n}\n\n//数据库实例表 route.db_instance_info\nmessage DbInstanceInfo {\n    int32 instanceId    = 1;\n    string uri          = 2;\n    string username     = 3;\n    string password     = 4;\n    int32 mode          = 5;\n}\n\n//数据库路由表 route.db_route\nmessage DbRoute {\n    string dbId         = 1;    //全局唯一\n    string groupName    = 2;    //数据库组名,例如db.go文件中定义的GameDB,一个组下面可以有多个database\n    string database     = 3;    //数据库名字\n    int32 instanceId    = 4;    //DbInstanceInfo.instanceId\n}\n\n\n//用户game分配信息 route.user_game_alloc\nmessage UserGameAlloc {\n    string openId           = 1;    //本地游戏服使用的 openId\n    int64 uin               = 2;\n    string dbId             = 3;    //用户数据所在dbId,对应DbRoute.dbId\n    string deviceId         = 4;    //创建角色时的设备 id\n    string channel          = 5;    //创建角色时的渠道\n    int32 platform          = 6;    //创建角色时的平台 sp_common.proto   enum PLATFORM_TYPE\n    string sdkOpenId        = 7;    //第三方 sdk 的 openId\n}\n\n//用户\n//用户限制信息\nmessage ActorControl {\n    int64 uin           = 1;    //用户Uin\n    int64 banStamp      = 2;    //封号时间\n    int64 terminalStamp = 3;    //封号终止时间    0: 永久封号\n    string operator     = 4;    //操作人\n}\n\n//用户的角色信息 game.actor\nmessage ActorInfo {\n    string openId       = 1;\n    int64 uin           = 2;\n    int32 exp           = 3;\n    int32 level         = 4;\n    int32 power         = 5;\n    string name         = 6;\n    int32 faceId        = 8;\n    int64 createStamp   = 9;\n    int32 loginDays     = 10;   //登录天数\n    int32 platform      = 11;   //创建角色时的平台\n    string channel      = 12;   //渠道\n    string deviceId     = 13;   //创建角色时的设备 id\n    int32 curPlatform   = 16;   //当前平台\n    int32 changeNameCount = 17;  //改名次数\n    ActorHead actorHead = 18;  //头像数据\n    repeated int32 showFashionIds = 19;  //最多 5 个展示角色的 fashionId\n    int32 showFashionIndex = 20;    //当前展示第几个 fashion\n    int32 birthday      = 21;   // 月: birthday / 100   日: birthday % 100\n    int32 activeHandBookGrowId = 22;    //激活的图鉴成长进度 (base_card_hand_book_grow.id)\n}\n\nmessage ActorHead {\n    int32 fashionId   = 1; //头像，对应card fashion表\n    int32 headId      = 2; //头像，对应 base_item 表\n    int32 headRectId  = 3; //头像框，对应 base_item 表\n    int64 headRectStamp = 4;    //头像框到期时间\n    int32 headRectExtra = 5;    //头像框额外字段\n    int64 headRectItemUid = 6;\n}\n\n//需要重置的系统类型\nenum MODULE_RESET_TYPE {\n    MRT_NONE                = 0;\n    MRT_BOSS_DAILY          = 1;\n    MRT_SHOP_DAILY          = 2;\n    MRT_TASK_DAILY          = 3;\n    MRT_TASK_WEEKLY         = 4;\n    MRT_GACHA_DAILY         = 5;\n    MRT_ARENA_DAILY         = 6;\n    MRT_PURCHASE_DAILY      = 7;\n    MRT_PURCHASE_WEEKLY     = 8;\n    MRT_PURCHASE_MONTHLY    = 9;\n    MRT_CARNIVAL_DAILY      = 10;\n    MRT_BATTLE_PASS_WEEKLY  = 11;\n    MRT_EXPEDITION_WEEKLY   = 12;\n    MRT_PLANT_DAILY         = 13;\n    MRT_ARENA_WEEKLY        = 14;\n    MRT_MANOR               = 15;\n    MRT_BATTLE_PASS_DAILY   = 16;\n    MRT_GIFT_DAILY          = 17;\n    MRT_GIFT_WEEKLY         = 18;\n    MRT_GIFT_MONTHLY        = 19;\n    MRT_SUPPLY_DAILY        = 20;\n    MRT_BUFF_STAGE_WEEKLY   = 21;\n    MRT_ROGUE_WEEKLY        = 22;\n    MRT_AGREEMENT_WEEKLY    = 23;\n    MRT_ACTIVITY_DAILY      = 24;\n}\n\n//重置周期\nenum RESET_PERIOD {\n    RP_NONE     = 0;\n    RP_DAILY    = 1;    //每日重置\n    RP_WEEKLY   = 2;    //每周重置\n    RP_MONTHLY  = 3;    //每月重置\n}\n\n//用户状态信息,存储一些不需要下发给客户端的状态数据 game.actor_state\nmessage ActorState {\n    int64 uin                       = 1;\n    int64 globalMailSeq             = 2;    //收取全局邮件的seq\n    int64 lastResetStamp            = 3;    //上次数据重置时间\n    map<int32, int32> cntResources  = 4;    //次数资源\n    int32 signInState               = 5;    //签到状态\n    int64 lastSignInStamp           = 6;    //上次签到时间\n    map<int32, int64> item2RecoverStamp = 7;//物品上次自动恢复时间  itemId -> lastRecoverStamp\n    int64 lastArenaFightStamp       = 8;    //上次竞技场挑战时间\n    repeated string latestEmoji     = 9;    //最近使用的表情\n    bool resInitialed               = 10;   //初始资源是否已发放\n    int64 lastLoginStamp            = 11;   //上次登录时间\n    int32 loginDays                 = 12;   //登录天数\n    uint32 logLoginStamp            = 13;   //用于日志记录的登录时间\n    int32 totalPay                  = 14;   //累积充值额度\n    int32 onlineDuration            = 15;   //在线时长(分)\n    int64 levelupStamp              = 16;   //玩家上次升级时间\n    int32  allSignInDay             = 17;   //玩家总签到天数\n    map<int32, int64> resetStamps   = 18;   //各个系统的重置时间 MODULE_RESET_TYPE -> stamp\n    repeated int32 profileShowCards = 19;   //个人信息面板展示的卡牌\n    int32 winCount                  = 20;   //战斗胜利次数\n    int32 killMobCount              = 21;   //击退魔物数量\n    bool hideResource               = 22;   //是否对别人隐藏物资显示\n    int64 manorUnlockStamp          = 24;   //探险地图功能解锁时间\n    int32 guildOperateState         = 25;   //高 16 位: 是否创建过公会   低 16 位: 是否申请过公会\n    int32 mainLineStage             = 26;   //主线完成的最新关卡\n    int64 itemSyncKey               = 27;\n    int64 cardSyncKey               = 28;\n    int64 badgeSyncKey              = 29;\n    int32 rogueSweepCount           = 30;   //肉鸽扫荡次数\n    int32 badgeLevelCount           = 31;   //徽章累积升级等级\n    int32 rebateTag                 = 32;   //充值返利标识\n    int64 offlineStamp              = 33;   //离线时间\n    map<int32, int32> dropMulti     = 34;   //倍率掉落次数 enum MULTI_DROP_SCENE_GROUP -> cnt\n    int32 birthdayRewardYear        = 35;   //生日发奖年份\n}\n\n//用户客户端设置 game.actor_setting\nmessage ActorSetting {\n    int64 uin       = 1;\n    string settings = 2;\n}\n\n//全服玩家名字\nmessage GlobalActorName {\n    string name = 1;\n    int64 uin   = 2;\n    string dbId = 3;    //玩家所在的 DB\n    int64 stamp = 4;\n}\n\n//用户物品 game.actor_item\nmessage ItemInfo {\n    int64 itemUid       = 1;\n    int64 uin           = 2;\n    int64 count         = 3;\n    int32 itemId        = 4;\n    uint32 expireStamp  = 5;    //物品过期时间戳\n}\n\n//发给离线用户的物品 game.actor_item_offline\nmessage OfflineItem {\n    int64 uid           = 1;\n    int64 uin           = 2;\n    int64 stamp         = 3;\n    int32 logId         = 4;\n    string itemTupleRaw = 5;\n}\n\n//队伍 game.actor_card_team\nmessage CardTeamInfo {\n    int64 uin               = 1;\n    int32 teamId            = 2;\n    string name             = 3;\n    repeated int32 cardIds  = 4;\n}\n\n//用户卡牌 game.actor_card\nmessage CardInfo {\n    int64 cardUid                       = 1;    //卡片唯一标识\n    int64 uin                           = 2;    //所属角色唯一标识\n    int32 cardId                        = 3;    //卡片配置id\n    int32 level                         = 4;    //等级\n    int32 quality                       = 5;    //突破\n    int32 grade                         = 6;    //觉醒等级\n    int32 power                         = 7;    //战力\n    int32 exp                           = 8;    //经验\n    map<int32, int32> skill2Level       = 9;    //技能等级 skillId -> level\n    map<int32, int32> gradeUpSkills     = 10;   //觉醒影响的技能等级 skillId -> level\n    map<int32, int32> attributes        = 11;   //全量属性数据,给客户端下发的数据不包含徽章的加成\n    int32 fashionId                     = 12;   //正在使用的时装 id\n    map<int32, int64>  ownFashionIds    = 13;   //已拥有的时装 id 列表->获得时间\n    repeated int64 wearBadgeUids        = 14;   //当前穿戴的徽章物品 uid\n    repeated int32 badgeSuitIds         = 15;   //当前生效的套装 id\n    repeated string badgeAttributes     = 16;   //徽章加成的属性(单独存储) attrId:initValue:extraRatio\n    map<int32, int32> badgeId2Levels    = 17;   //当前穿戴徽章 badgeId -> level\n    bool focus                          = 18;   //是否关注\n    bool handBookReward                 = 19;   //是否已领取图鉴奖励\n}\n\n//卡牌精简信息\nmessage CardSimple {\n    int64 cardUid          = 1;    //卡片唯一标识\n    int64 uin              = 2;    //所属角色唯一标识\n    int32 cardId           = 3;    //卡片配置id\n    int32 level            = 4;    //等级\n    int32 quality          = 5;    //突破\n    int32 grade            = 6;    //觉醒等级\n    int32 fashionId        = 7;    //正在使用的时装 id\n    int32 position         = 8;    //布阵位置\n}\n\n//卡牌时装\nmessage CardFashions {\n    int64 uin                          = 1;     //所属角色唯一标识\n    map<int32, int64> ownFashionIds    = 2;     //已拥有的时装 id 列表->获得时间\n}\n//玩家卡牌数据更新\nmessage CardUpdate {\n    int32 cardId                            = 1;    //卡片配置id\n    map<int32, int32> basic                 = 2;    //卡牌基本属性变化  enum CARD_BASE_ATTR -> value\n    map<int32, int32> skill2Level           = 3;    //技能等级变化, skillId -> level, 如果要删除技能 level 填 -1\n    map<int32, int32> gradeUpSkills         = 4;    //觉醒影响的技能等级 skillId -> level\n    map<int32, int32> attributes            = 5;    //全量属性数据变化  enum ATTR_ID -> value\n    int64 syncKey                           = 6;\n    map<int32, int64> ownFashionIds         = 7;    //全部已有的时装id 列表->获得时间 直接覆盖之前的数据\n    map<int32, int32> skillUpFinishStamp    = 8;    //卡牌技能升级时间, 覆盖之前的数据\n}\n\nenum CARD_BASE_ATTR {\n    CBA_NONE          = 0;\n    LEVEL             = 1;    //等级\n    QUALITY           = 2;    //突破\n    WEAPON_LEVEL      = 3;    //专属武器等级\n    WEAPON_QUALITY    = 4;    //专属武器突破\n    GRADE             = 5;    //星级\n    POWER             = 6;    //战力\n    EXP               = 7;    //经验\n    FASHION           = 8;    //当前使用的时装\n}\n\nenum ATTR_ID {\n    AID_NONE    = 0;\n\tHP \t\t\t= 40000101;     //当前生命值\n\tMAX_HP \t\t= 40000102;     //生命值上限\n\tATK \t\t= 40000103;     //攻击力\n\tDEF \t\t= 40000104;     //防御力\n\tCRT \t\t= 40000201;     //暴击\n\tBLK \t\t= 40000202;     //格挡\n\tEVA \t\t= 40000203;     //闪避\n\tCRT_INT \t= 40000204;     //暴击伤害\n\tBLK_INT \t= 40000205;     //格挡强度\n\tSPD_MOVE \t= 40000301;     //移动速度\n\tSPD_ATK \t= 40000302;     //攻击速度\n\tRANGE_ATK \t= 40000303;     //攻击距离\n\tBLOCK_MAX \t= 40000304;     //阻挡数\n\tSTOIC \t\t= 40000305;     //易损值\n\tSHIELD \t\t= 40000306;     //护盾值\n\tMAX_RAGE \t= 40000307;     //最大怒气值\n\tRAGE \t\t= 40000308;     //当前怒气值\n\tRAGE_TIME   = 40000309;     //怒气时间回复\n\tRAGE_ATK    = 40000310;     //怒气攻击回复量\n\tRAGE_HIT    = 40000311;     //怒气受击回复量\n\tRAGE_KILL   = 40000313;     //怒气击杀回复\n\tBLOCK_COUNT = 40000314;     //自身阻挡计数\n    SPD_MOVE_ENHANCE = 40000315;     //移速增强\n    SPD_ATK_ENHANCE  = 40000316;     //攻速增强\n\tRESTRAINT_ADD1 = 40000401;  //对\"水\"属性英雄伤害加成\n\tRESTRAINT_ADD2 = 40000402;  //对\"火\"属性英雄伤害加成\n\tRESTRAINT_ADD3 = 40000403;  //对\"木\"属性英雄伤害加成\n\tRESTRAINT_ADD4 = 40000404;  //对\"暗\"属性英雄伤害加成\n\tRESTRAINT_ADD5 = 40000405;  //对\"光\"属性英雄伤害加成\n\tRESTRAINT_SUB1 = 40000406;  //受到\"水\"属性英雄伤害减免\n\tRESTRAINT_SUB2 = 40000407;  //受到\"火\"属性英雄伤害减免\n\tRESTRAINT_SUB3 = 40000408;  //受到\"木\"属性英雄伤害减免\n\tRESTRAINT_SUB4 = 40000409;  //受到\"暗\"属性英雄伤害减免\n\tRESTRAINT_SUB5 = 40000410;  //受到\"光\"属性英雄伤害减免\n\tDAMAGE_ADD  = 40000411;     //伤害加成\n\tDAMAGE_SUB  = 40000412;     //伤害减免\n\tTREAT_ADD   = 40000501;     //治疗加成%（技能用）\n\tBE_TREAT_ADD   = 40000502;  //受到治疗加成%（技能用）\n\tTENACITY       = 40000601;  //韧性\n    SHIELD_SPECIAL = 40000602;  //特殊护盾\n}\n\nmessage ItemTuple {\n    int32 tupleType  = 1;   //enum TUPLE_TYPE\n    int32 itemId     = 2;\n    int32 count      = 3;\n    int64 uid        = 4;\n}\n\nmessage DropTuple {\n    ItemTuple item                  = 1;\n    repeated ItemTuple changeItem   = 2;\n    bool        isNew               = 3;\n}\n//关卡信息 game.actor_stage\nmessage StageInfo {\n    int64 uin               = 1;\n    int32 stageId           = 2;    //关卡id\n    int32 sceneType         = 3;    //副本类型  enum SCENE_TYPE\n    int32 chapterId         = 4;    //章节id\n    int32 challengeCount    = 5;    //挑战次数\n    int64 challengeStamp    = 6;    //上次挑战时间,如果跨天就把 challengeCount 置0\n    int32 hpPercent         = 7;    //挑战后 关卡剩余血量百分比\n    int32 bottomMissCount   = 8;    //保底掉落 miss 次数\n}\n\n//副本进度信息\nmessage SceneProgressInfo {\n    int64 uin               = 1;\n    int32 sceneType         = 2;\n    int32 chapterId         = 3;    //章节进度\n    int32 passedStageId     = 4;    //当前已通关的最新关卡,适用于章节有前后置的副本,例如主线、爬塔\n    int32 rewardedChapter   = 5;    //已领取的章节奖励进度\n    map<int32, int32> chapter2PassedStageId = 6;  //各个章节已通关的最新关卡,适用于章节没有前后置关系的副本,例如 boss本、日常本\n    map<int32, int32> stage2BottomMissCount = 7;  //关卡掉落保底 miss 次数\n    repeated int32 rewardedStages           = 8;  //已手动领取奖励的关卡\n    int64 resetStamp        = 9;    //上次重置时间\n    repeated int32 allPassedStages = 10;   //所有已通关的关卡 id,仅日常本需要保存该字段,用于判断是否首通,因为日常本可以解锁后续多个关卡,不按照顺序打就会导致前面的关卡拿不到首通奖励\n    int32 maxStageId               = 11;   //历史通过最大关卡, 目前副本类型 61-63 记录该值\n}\n\n//战斗回放记录 battle.battle_record\nmessage BattleRecord {\n    int64 battleUid         = 1;    //战斗记录uid\n    int64 uin               = 2;    //发起方uin\n    int64 targetId          = 3;    //对方id  pvp: 对方uin, pve: 关卡id\n    int32 sceneType         = 4;    //副本类型  sp_scene.proto  enum BATTLE_TYPE\n    bool win                = 5;    //发起方是否胜利\n    int64 stamp             = 6;    //发生时间\n    bytes data              = 7;    //sp_battle.proto BattleCompleteData 序列化后的数据\n    int64 battleSeqId       = 8;    //战斗 seqId\n}\n\nmessage ArenaBattleRecord {\n    ActorMirrorInfo opponent    = 1;\n    bool   isWin                = 2;\n    int64   battleUid           = 3;\n    int64   stamp               = 4;\n    bool isDefend               = 5;\n}\n\nenum RELATION_STATE {\n    RS_NONE     = 0;\n    APPLYING    = 1;    //主动方 自己正请求加别人为好友\n    APPLIED     = 2;    //被动方 收到的别人的好友请求\n    FRIEND      = 3;    //好友状态\n    BLOCK       = 4;    //屏蔽状态\n    DELETE      = 5;    //删除 (仅用于客户端删除本地数据)\n}\n\n//好友关系数据 game.actor_relation\nmessage RelationInfo {\n    int64 uin       = 1;\n    int64 targetUin = 2;\n    int64 stamp     = 3;\n    int32 state     = 4;    //enum RELATION_STATE\n    string remark   = 5;    //备注\n}\n\n//徽章 game.actor_badge\nmessage BadgeInfo {\n    int64 uin               = 1;\n    int64 badgeUid          = 2;    //唯一标识\n    int32 badgeId           = 3;    //徽章id\n    int32 level             = 4;    //等级\n    int32 exp               = 5;    //经验\n    int32 mainAttribute     = 6;    //主属性 baseBadgeAttributeId\n    repeated int32 viceAttributes = 7;   //副属性 baseBadgeAttributeId\n    map<int32, int32> attributeLevels = 8;  //属性等级,包含主属性和副属性    baseBadgeAttributeId -> level\n    int32 wearCardId        = 9;    //当前穿戴该徽章的角色 id (只在内存中,变更时不写数据库)\n    bool locked             = 10;   //是否上锁\n    bool isNew              = 11;\n    int32 costGold          = 12;   //消耗的金币总量\n}\n\nenum TASK_STATE {\n    NORMAL      = 0; \n    FINISHED    = 1;    //已完成\n    REWARD      = 2;    //已领奖\n    OVERDUE     = 3;    //已过期\n}\n//用户任务 game.actor_task\nmessage TaskInfo {\n    int64 uin           = 1;\n    int64 uid           = 2;\n    int32 taskId        = 3;\n    int32 value         = 4;\n    int64 startStamp    = 5;\n    int32 state         = 6;    //enum TASK_STATE\n}\n\n//IM 小队群聊信息 message.group\nmessage IMGroupInfo {\n    string sessionId        = 1;\n    int32 memberCount       = 2;    //成员数量\n}\n\nenum MAIL_SCOPE {\n    MS_NONE     = 0;\n    MS_ALL      = 1;    //所有玩家\n    MS_SPECIFIC = 2;    //指定玩家\n    MS_LEVEL    = 3;    //等级区间\n}\n\n//全服邮件 game.global_mail\nmessage GlobalMail {\n    int64 mailUid       = 1;    //邮件唯一标识\n    string title        = 2;    //邮件标题\n    string senderName   = 3;    //寄件人姓名\n    string content      = 4;    //邮件内容\n    string attachment   = 5;    //邮件附件 ItemTuple 三元组格式\n    int64 sendStamp     = 6;    //发送时间\n    int64 expireStamp   = 7;    //过期时间\n    int32 userScope     = 8;    //玩家范围  enum MAIL_SCOPE\n    int64 createRoleFromStamp = 9;  //创角开始时间\n    int64 createRoleToStamp   = 10; //创角结束时间\n    int32 minLevel      = 11;   //等级范围\n    int32 maxLevel      = 12;\n    bool canDelete      = 13;    //是否能手动删除\n    repeated string targetChannels = 14;    //目标渠道\n}\n\n//玩家邮件 game.actor_mail\nmessage ActorMail {\n    int64 mailUid       = 1;    //邮件唯一标识\n    int64 uin           = 2;    //接受方 uin, 为0表示全服邮件\n    string title        = 3;    //邮件标题\n    string senderName   = 4;    //寄件人姓名\n    string content      = 5;    //邮件内容\n    string attachment   = 6;    //邮件附件 ItemTuple 三元组格式\n    int64 sendStamp     = 7;    //发送时间\n    int64 expireStamp   = 8;    //过期时间\n    int64 relateUid     = 9;    //如果是全服邮件,该值为全服邮件的 mailUid\n    bool canDelete      = 10;   //是否能手动删除\n    bool fetched        = 11;   //是否已领取附件\n    bool read           = 12;   //是否已读\n    bool cliParse       = 13;\n    repeated string senderParams  = 14;     //寄件人姓名参数\n    repeated string titleParams   = 15;     //邮件标题中的参数\n    repeated string contentParams = 16;     //邮件内容中的参数\n    bool canPrior       = 17;   //邮件数量超出上限后能否被顶掉\n    string extra        = 18;    //扩充信息\n}\n\n//公会信息 guild.guild\nmessage GuildInfo {\n    int64 guildUid              = 1;\n    string name                 = 2;\n    int64 ownerUin              = 3;\n    int64 createStamp           = 4;\n    int32 level                 = 5;    //公会等级\n    int32 exp                   = 6;    //公会经验\n    int32 activePoint           = 7;    //公会每日累积的活跃值\n    int32 activeLevel           = 8;    //活跃等级\n    int32 iconId                = 9;    //公会图标\n    int32 levelLimit            = 10;   //加入等级限制    -1:任何人可加入直接加入,无需审核  -2:拒绝申请\n    int32 memberCount           = 11;   //成员数量\n    string notice               = 12;   //公告\n//    repeated string allTargets  = 14;   //所有的公会目标\n//    repeated int32 targetIdxes  = 15;   //当前勾选的公会目标索引\n\n    int64 resetStamp            = 16;   //上次重置时间\n    int32 dayAverActivePointSum = 17;   //日人均活跃度之和\n    bool impeaching             = 18;   //是否在弹劾中\n    int64 impeachStamp          = 19;   //弹劾开始时间\n\n    bool applying               = 20;   //在搜索其他公会时,用来展示自己是否在申请该公会中,以及申请过期时间\n    int64 applyTimeout          = 21;   //申请还剩多久过期 秒\n    string leaderName           = 22;   //队长名字  不更新,下发给客户端时临时获取\n    int32 dayExp                = 23;   //当日已获得的经验值\n    int32 DayBeginLevel         = 24;   //当日开始等级\n    repeated int32 unlockedHeadIds = 25; //已解锁的头像\n    int32 lastGuildWarRank      = 26;   //上期公会战排名\n    int32 lastGuildWarActCnt    = 27;   //上期公会战参与公会数量\n    int32 policy                = 28;   //活动方针\n}\n\n//公会路由信息: 公会所在的guildSvr服务节点信息 route.guild_route\nmessage GuildRoute {\n    int64 guildUid          = 1;\n    string serviceId        = 2;\n}\n\n//玩家所在公会 route.user_guild\nmessage UserGuild {\n    int64 uin               = 1;\n    int64 guildUid          = 2;    //玩家所在公会 guildUid\n    int64 stamp             = 3;    //进入公会时间\n    string serviceId        = 4;\n}\n\n//公会成员信息 guild.guild_member\nmessage GuildMember {\n    int64 uin               = 1;\n    int64 guildUid          = 2;    //所在公会 uid\n    int64 joinStamp         = 3;    //加入公会时间\n    int32 roleType          = 4;    //角色类型 队长、副队长、普通成员  enum GUILD_ROLE_TYPE\n    int32 activePoint       = 5;    //公会成员每日累积的活跃值\n    int64 resetStamp        = 6;    //重置时间(活跃值)\n    int64 activeStamp       = 7;    //活跃时间\n    string name             = 8;    //姓名\n    int32 level             = 9;    //等级\n    int32 faceId            = 10;   //头像\n    bool isOnline           = 11;   //是否在线\n    bool autoJoin           = 12;   //是否自动加入\n}\n\nmessage GuildApplicant {\n    int64 uin               = 1;\n    string name             = 2;    //姓名\n    int32 level             = 3;    //等级\n    int32 faceId            = 4;    //头像\n    int64 expireStamp       = 5;    //过期时间\n    int64 activeStamp       = 6;    //活跃时间\n    bool isOnline           = 7;    //是否在线\n}\n\n//公会用于推荐的信息\nmessage GuildRecommendInfo {\n    int64 guildUid          = 1;\n    string name             = 2;\n    int32 level             = 3;    //等级\n    int32 activeLevel       = 4;    //活跃度\n    int32 memberCount       = 5;    //成员数量\n    int32 applicantCount    = 6;    //申请者人数\n    int32 levelLimit        = 7;    //加入等级限制\n    int32 iconId            = 8;\n//    repeated string allTargets = 9;   //所有的公会目标\n//    repeated int32 targetIdxes = 10;   //当前勾选的公会目标索引\n    string leaderName       = 11;   //队长名字\n    int32 lastGuildWarRank  = 12;   //上期公会战排名\n    int32 lastGuildWarActCnt= 13;   //上期公会战参与公会数量\n    int32 policy            = 14;   //活动方针\n}\n\n//竞技场人物信息\nmessage ActorMirrorInfo {\n    int64 uin                   = 1;\n    int64 createTime            = 2;    //账号创建时间\n    int64 fightScore            = 3;    //战斗积分\n    int32 level                 = 4;    //等级\n    int32 faceId                = 5;    //头像ID\n    string name                 = 6;    //名字\n    int64 guildUid              = 7;    //所在公会 uid\n    string guildName            = 8;    //所在公会名字\n    int32 arenaMedal            = 9;    //竞技场的勋章\n    int64 lastLoginStamp        = 10;   //上次登录时间\n    bytes   arenaFormation      = 11;   //竞技场阵容 (机器人专有)BattleFormation的二进制bytes数据\n    bool isOnline               = 12;   //是否在线\n    int32 cardCount             = 13;   //玩家卡牌数量\n    int32 randNameId            = 14;   //随机nameID\n    ActorHead actorHead         = 15;   //头像信息\n}\n//竞技场玩家信息\nmessage ActorArenaInfo {\n    int64 uin                   = 1;\n    int64 createTime            = 2;    //账号创建时间\n    int64 fightScore            = 3;    //战斗积分\n    int64 lastLoginStamp        = 4;    //上次登录时间\n}\n\n//阵容类型\nenum FORMATION_TYPE {\n    FORMATION_TYPE_ARENA          = 0;    //竞技场防守阵容\n    FORMATION_TYPE_FRIEND_FIGHT   = 1;    //好友切磋防守阵容\n}\n\n//竞技场防守阵容数据\nmessage ArenaDefenseFormation {\n    int32 level                     = 1;    //阵容等级(用以匹配防守方阵容)\n    map<int64, int32> cardUid2Pos   = 2;    //卡牌站位 cardUid -> pos\n    map<int64, int32> buildUid2Pos  = 3;    //建筑站位 buildUid -> pos\n    int32 arenaMapId                = 4;    //设置的防守地图 BaseArenaMap\n    int32 leaderCardId              = 5;    //队长角色 id\n    repeated BurstOrderSetting burstOrderSetting = 6;    //总攻技能释放顺序设置\n    int32 formationType             = 7;    //阵容类型  enum FORMATION_TYPE\n} \n\n//记录总攻技能释放顺序设置\nmessage BurstOrderSetting {\n    int32 job              = 1;    //职业\n    repeated int64 cardList = 2;    //角色优先级排序表\n}\n\nmessage ActorArenaZone {\n    int64 uin   = 1;\n    int32 zone  = 2;    //赛季赛区\n}\n//竞技场荣誉信息\nmessage ActorArenaHonor {\n    int64 uin           = 1;\n    int32 arenaMedal    = 2;\n}\n\n//boss挑战信息 game.actor_boss_consume\nmessage ActorBossConsume {\n    int64 uin                   = 1;\n    repeated int32 usedCardIds  = 2;    //阶段1已使用的卡牌\n    int32 challengeCount        = 3;    //阶段2的挑战次数\n}\n\n\n//boss挑战关卡信息 game.actor_boss\nmessage ActorBossInfo {\n    int64 uid                   = 1;\n    int64 uin                   = 2;\n    int64 activityUid           = 3;    //boss活动uid 常规boss为0\n    int32 chapterId             = 4;    //boss 章节id\n    int32 stageId               = 5;    //当前boss关卡id    如果是 boss 章节的第一个关卡,就在第一阶段\n    int32 stageIdx              = 6;    //章节中的第几个关卡\n    int32 position              = 7;    //手动添加的活动boss的位置 从1开始\n    int32 challengeCount        = 8;    //挑战次数\n    int32 winCount              = 9;   //胜利次数\n}\n\n//记录各种副本的残血残怒情况 game.actor_fight_state\nmessage ActorFightState {\n    int64 uid                   = 1;\n    int64 uin                   = 2;\n    int32 sceneType             = 3;    //副本类型\n    int32 extId                 = 4;    //扩展id\n    repeated ObjectState ownStates = 5;\n    repeated ObjectState targetStates = 6;\n}\n\n//玩家新手引导 game.actor_guide\nmessage GuideInfo {\n    int64 uin               = 1;\n    int32 guideId           = 2;\n    repeated int32 steps    = 3;\n    int64 stamp             = 4;\n}\n\n//玩家完成的剧情信息 game.actor_plot\nmessage PlotInfo {\n    int64 uin       = 1;\n    int64 stamp     = 2;\n    int32 plotId    = 3;\n}\n\n//玩家完成剧情已领取的奖励标识 game.actor_plot_reward\nmessage PlotReward {\n    int64 uin       = 1;\n    int32 stepId    = 2;\n    int32 plotId    = 3;\n    int64 stamp     = 4;\n}\n\n//商品信息\nmessage ShopGoodsInfo {\n    int32 gridId            = 1;    //格子ID\n    int32 goodsId           = 2;    //商品ID(通过配置表对应商品内容，购买消耗等)\n    int32 boughtNum         = 3;    //商品购买次数\n    int64 nextRefreshTime   = 4;    //下次刷新时间\n    bool unlocked           = 5;    //是否已解锁\n    int64 unlockTime        = 6;    //解锁时间\n}\n\n//商店信息\nmessage ShopInfo {\n    int64 uin                       = 1;\n    int32 typeId                    = 2;    //类型ID\n    int32 refreshNum                = 3;    //刷新次数\n    int64 nextRefreshTime           = 4;    //下次刷新时间\n    bool isOpen                     = 5;    //是否开启\n    map<int32,ShopGoodsInfo> goods  = 6;    //格子ID -> 商店商品\n}\n\n\n//通行证信息\nmessage BattlePassInfo {\n    int64 uin                           = 1;\n    int32 passPortId                    = 2;    //通行证ID\n    bool isUnLock                       = 3;    //是否解锁\n    int32 lv                            = 4;    //当前等级\n    int32 exp                           = 5;    //当前经验\n    int32   expLimit                    = 6;    //经验限制进度\n    repeated    int32       openList    = 7;    //开启的奖励类型\n    map<int32,bytes> rewards            = 8;   //领奖信息 typeid->领奖状态\n    repeated    int64 dailyTask         = 9;\n    repeated    int64 weeklyTask        = 10;\n    repeated    int64 totalTask         = 11;\n}\nmessage CarnivalStage {\n    repeated int64 taskUid              = 1;    //任务Uid\n}\n\n//嘉年华信息\nmessage CarnivalInfo {\n    int64 uin                           = 1;\n    int64 nextStamp                     = 2;    //开启时间\n    map<int32,CarnivalStage> stages     = 3;    //阶段数据\n    repeated int32 rewardList           = 4;    //领奖列表\n    int64   closeStamp                  = 5;    //记录id\n}\n\n//招募记录\nmessage GachaRecord {\n    int32 poolId                    = 1;\n    repeated ItemTuple gachaDrop    = 2;\n    int64   timestamp               = 3;\n    int64   uin                     = 4;\n    int32   index                   = 5;\n    int32   recordId                = 6;\n}\n\n//卡池信息\nmessage GachaPool {\n    int32 point                     = 1;    //兑换点数\n    map<int32,int32>   exchangeList = 2;    //卡片ID->兑换次数\n    repeated  GachaRecord records   = 3;    //timestamp->抽卡记录\n    int64 actUin                    = 4;    //活动Uid\n    int32 gachaCount                = 5;    //抽卡次数\n    int32   target                  = 6;    //目标卡\n    int32 targetCount               = 7;    //目标卡计数\n    int32 extraRewarded             = 8;    //领取的额外奖励卡片\n}\nmessage GachaFloor {\n    int32 reachNum      = 1;    //达成次数\n    int32 count         = 2;    //当前累计次数\n}\nmessage PoolGachaRecord {\n    repeated  GachaRecord records       = 1; //timestamp->抽卡记录\n}\n//招募信息\nmessage GachaInfo {\n    int64 uin                           = 1;\n    map<int32,GachaPool>    poolList    = 2; //卡池ID->卡池信息\n    map<int32,GachaFloor>    floor      = 3; //保底ID->累计次数\n    map<int32,int32>    dailyGachaCount = 4; //modid->每日抽卡次数\n    map<int32,int32>    totalGachaCount = 5; //modid->总计抽卡次数\n    map<int32,int32>    targetCount     = 6; //bottom_main_type->目标保底次数\n    map<int32,int32>    recordCount     = 7; //卡池记录count\n}\n\nmessage ExpeditionStateRecord {\n    int32 stageId               = 1;\n    repeated int32 challenged   = 2;    //完成的挑战\n    repeated int64 battleUid    = 3;\n}\n\nmessage ChapterInfo {\n    int32 chapterId             = 1;\n    int64 unlockStamp           = 2;\n    int32 buffID                = 3;\n}\n//远征信息\nmessage ExpeditionInfo {\n    int64 uin                               = 1;\n    int32 cycle                             = 2;    //当前周期\n    bool jumpRefresh                        = 3;    //是否垮周期更新\n    repeated ChapterInfo chapters           = 4;    //当前章节\n    int32 curStage                          = 5;    //当前进度\n    repeated ExpeditionStateRecord records  = 6;    //挑战记录  \n    repeated int32 rewardIndex              = 7;    //已经领取奖励index\n    int32   highPassStar                    = 8;    //最高通关关卡星数\n}\n\n//竞技场个人信息\nmessage ActorArenaPersonal {\n    int64 uin                                           = 1;\n    int32 highRank                                      = 2;    //赛季最高排名\n    repeated int32 rewardList                           = 3;    //领奖列表\n    int64 nextArenaFightStamp                           = 4;    //下次竞技场挑战时间\n    int32 buyFightNum                                   = 5;    //购买挑战次数\n    int32 fightNum                                      = 6;    //挑战次数\n    int32 arenaMedal                                    = 7;    //赛季勋章\n    ArenaDefenseFormation defenseFormation              = 8;   //防守阵容\n    int32 season                                        = 9;    //当前赛季\n    repeated int32 weeklyRewardList                     = 10;   //每周领奖列表\n    int32 historyHighRank                                 = 11;   //历史最高排名\n    ArenaDefenseFormation friendFightFormation          = 12;   //好友切磋的阵容\n}\n\nmessage BattleArrayData {\n    map<int64, int32> cardUid2Pos   = 1;    //卡牌站位 cardUid -> pos\n    map<int64, int32> buildUid2Pos  = 2;    //建筑站位 buildUid -> pos\n    int32 index                     = 3;    //\n    int32 leaderCardId              = 4;    //队长角色 id\n    repeated BurstOrderSetting burstOrderSetting = 5;    //总攻技能释放顺序设置\n}\n\n//game.actor_stage_prepare\nmessage StagePrepareInfo {\n    int64 uin                           = 1;\n    int64 uid                           = 2;\n    int32 sceneType                     = 3;    //sp_scene.proto    enum SCENE_TYPE\n    int32 stageId                       = 4;\n    map<int64, int32> cardUid2Pos       = 5;    //卡牌站位 cardUid -> pos\n    map<int64, int32> buildUid2Pos      = 6;    //建筑站位 buildUid -> pos\n    repeated BattleArrayData  specialArray    = 7;    //特殊布阵信息（当前远征使用）\n    int32 leaderCardId                  = 8;    //队长角色 id\n    repeated BurstOrderSetting burstOrderSetting = 9;    //总攻技能释放顺序设置\n}\n\n//内购订单信息\nmessage PurchaseOrder {\n    int64 uin                       = 1;\n    int64 purchaseUid               = 2;    //订单ID\n    int32 productId                 = 3;    //商品ID\n    int64 timestamp                 = 4;    \n}\n//内购信息\nmessage PurchaseInfo {\n    int64 uin                           = 1;\n    map<int32,int64> monthCard          = 2;    //MonthCardType -> 月卡截止时间\n    map<int32,bool>  monthDaily         = 3;    //\n    map<int32,int32>    boughtRecord    = 4;    //购买记录 basePayProduct.id -> 购买次数\n    repeated int32    firstBought       = 5;    //已经首冲的商品（额外存储，用于重置功能）\n    int64 firstRechargeResetStamp       = 6;    //首充重置时间\n}\n\nenum TIME_STATE {\n    TS_NONE         = 0;\n    TS_WAITING      = 1;    //未开启\n    TS_RUNNING      = 2;    //进行中\n    TS_FINISH       = 3;    //已结束\n    TS_SUSPEND      = 4;    //暂停状态\n}\n\nenum VERIFY_STATE {\n    VS_NONE         = 0;\n    VS_APPROVE      = 1;    //审核通过\n    VS_ON_SHELF     = 2;    //审核上架\n    VS_OFF_SHELF    = 3;    //审核下架\n    VS_MODIFY       = 4;    //审核修改\n    VS_REJECT       = 5;    //拒绝\n    VS_DRAFT        = 6;    //草稿\n}\n\nenum HARD_STATE {\n    HS_NONE         = 0;\n    HS_NORMAL       = 1;    //正常\n    HS_OFF_SHELF    = 2;    //下架\n    HS_REMOVED      = 3;    //移除\n}\n\n//运营 web 用户信息 gm.op_user\nmessage OpUser {\n    string username         = 1;    //用户名\n    string password         = 2;\n    repeated string roles   = 3;\n    string name             = 4;    //昵称\n    string avatar           = 5;    //头像\n    int64 createStamp       = 6;\n    string title            = 7;\n}\n\n//推荐图 gm.op_recommend_img gm.op_recommend_img_verify\nmessage OpRecommendImg {\n    int64 uid                   = 1;\n    int64 startStamp            = 2;    //开始时间\n    int64 endStamp              = 3;    //结束时间\n    int32 sortValue             = 4;    //排序值\n    int32 imgLayout             = 5;    //图片布局模板\n    int32 timeState             = 6;    //时间状态  enum TIME_STATE\n    int32 verifyState           = 7;    //审核状态  enum VERIFY_STATE\n    int32 hardState             = 8;    //enum HARD_STATE\n    string remark               = 9;    //备注\n    repeated string images      = 10;   //图片 url 列表\n    repeated string jumpTargets = 11;   //图片跳转列表\n    repeated int32 jumpTypes    = 12;   //跳转类型 enum RECOMMEND_IMG_JUMP_TYPE  0: 无跳转   1: 跳转商店   2: 商店购买面板   3: 直接购买\n    string cnName               = 13;   //中文名字\n    string enName               = 14;   //英文名字\n    bool permanent              = 15;   //是否永久显示\n    bool boughtHide             = 16;   //是否购买后就不显示 下面 2 个字段用于判断是否已购买\n    int32 productType           = 17;   //推荐的商品类型  enum RECOMMEND_IMG_PRODUCT_TYPE  1: base_pay_product 2: base_fashion 3: base_gift\n    string productItemIds       = 18;   //推荐的商品 id\n    repeated string targetChannels = 19;//目标渠道\n    int32 levelLimit            = 20;   //玩家等级限制\n}\n\n//礼包 gm.op_gift_package gm.op_gift_package_verify\nmessage OpGiftPackage {\n    int64 uid                   = 1;\n    int64 startStamp            = 2;    //开始时间\n    int64 endStamp              = 3;    //结束时间\n    int32 sortValue             = 4;    //排序值\n    int32 timeState             = 5;    //时间状态  enum TIME_STATE\n    int32 verifyState           = 6;    //审核状态  enum VERIFY_STATE\n    int32 hardState             = 7;    //enum HARD_STATE\n    string remark               = 8;    //备注\n    int32 shelfArea             = 9;    //上架区域      1: 精选组合     2: 超值优惠  大于10000000,则为上架的商店标签uid\n    int64 iosPackageId          = 10;   //ios 礼包 id\n    int64 androidPackageId      = 11;   //android 礼包 id\n}\n\n//时装 gm.op_fashion gm.op_fashion_verify\nmessage OpFashion {\n    int64 uid                   = 1;\n    int64 startStamp            = 2;    //开始时间\n    int64 endStamp              = 3;    //结束时间\n    int32 sortValue             = 4;    //排序值\n    int32 timeState             = 5;    //时间状态  enum TIME_STATE\n    int32 verifyState           = 6;    //审核状态  enum VERIFY_STATE\n    int32 hardState             = 7;    //enum HARD_STATE\n    int64 fashionId             = 8;    //时装 id\n    bool newTag                 = 9;    //是否是新品标记\n}\n\n//通过活动上架的时装 上架过就一直展示 gm.op_fashion_show\nmessage OpFashionShow {\n    int64 uid                   = 1;    //OpFashion.uid\n    int64 fashionId             = 2;\n    int64 startStamp            = 3;\n}\n\n//礼包 gm.op_notice gm.op_notice_verify gm.op_notice_draft\nmessage OpNotice {\n    int64 uid                   = 1;\n    int64 startStamp            = 2;    //开始时间\n    int64 endStamp              = 3;    //结束时间\n    int32 sortValue             = 4;    //排序值\n    int32 timeState             = 5;    //时间状态  enum TIME_STATE\n    int32 verifyState           = 6;    //审核状态  enum VERIFY_STATE\n    int32 hardState             = 7;    //enum HARD_STATE\n    string remark               = 8;    //备注\n    int32 shelfArea             = 9;    //上架区域      1: 精选组合     2: 超值优惠\n    int32 modelType             = 10;   //模板类型 1: 图文  2: 整图\n    string title                = 11;   //标题\n    string subTitle             = 12;   //副标题\n    string content              = 13;   //正文内容  用于图文\n    string picUrl               = 14;   //图片路径  用于整图\n    string jumpTarget           = 15;   //跳转目标\n    string cliTag               = 16;\n    repeated string targetChannels = 17;//目标渠道\n}\n\n//活动时间类型\nenum ACTIVITY_TIME_TYPE {\n    ATT_NONE        = 0;\n    ATT_FIXED       = 1;    //固定时间\n    ATT_WEEK_LOOP   = 2;    //每周循环\n    ATT_MONTH_LOOP  = 3;    //每月循环\n}\n\n//活动 gm.op_activity gm.op_activity_verify\nmessage OpActivity {\n    int64 uid                   = 1;\n    int32 timeState             = 2;    //时间状态  enum TIME_STATE\n    int32 verifyState           = 3;    //审核状态  enum VERIFY_STATE\n    int32 hardState             = 4;    //enum HARD_STATE\n\n    int32 activityId            = 5;    //活动 ID\n\n    int32 timeType              = 6;    //时间类型 enum ACTIVITY_TIME_TYPE\n    int64 startStamp            = 7;    //开始时间 (固定时间使用)\n    int64 endStamp              = 8;    //结束时间 (固定时间使用)\n    int64 offShelfStamp         = 9;    //下架时间戳 (固定时间使用)\n\n    int32 startWeekDay          = 10;    //周几开始 (每周循环使用)\n    int32 endWeekDay            = 11;   //周几结束 (每周循环使用)\n    int32 offShelfWeekDay       = 12;   //周几下架 (每周循环使用)\n\n    int32 startMonthDay         = 13;   //每月几号开始 (每月循环使用)\n    int32 endMonthDay           = 14;   //每月几号结束 (每月循环使用)\n    int32 offShelfMonthDay      = 15;   //每月几号下架 (每月循环使用)\n\n    string startTime            = 16;   //开始时间点 例如: 12:00  每周循环和每月循环使用\n    string endTime              = 17;   //结束时间点\n    string offShelfTime         = 18;   //下架时间点\n\n    string remark               = 19;   //备注\n    bool suspend                = 20;   //是否暂停状态\n    string picUrl               = 21;   //活动图片地址\n}\n\n//系统邮件 gm.op_system_mail\nmessage OpSystemMail {\n    int64 uid                   = 1;\n    int32 timeState             = 2;    //时间状态  enum TIME_STATE\n    int32 verifyState           = 3;    //审核状态  enum VERIFY_STATE\n    int32 hardState             = 4;    //enum HARD_STATE\n\n    repeated string targetChannels  = 5;    //渠道\n    int32 userScope             = 6;    //enum MAIL_SCOPE 玩家范围 1:所有玩家   2:指定玩家 uin  3:等级区间\n    string remark               = 7;    //备注\n    int64 createRoleFromStamp   = 8;    //创角开始时间\n    int64 createRoleToStamp     = 9;    //创角结束时间\n    bool scheduleSend           = 10;   //是否定时发送\n    int64 sendStamp             = 11;   //定时发送时间\n    int32 minLevel              = 12;   //userScope == 3 时, 等级区间\n    int32 maxLevel              = 13;\n    string receiverUins         = 14;   //userScope == 2 时, 玩家 uin 列表, |分割\n    string senderName           = 15;   //寄件人名字\n    string mailTitle            = 16;   //邮件标题\n    string mailContent          = 17;   //邮件内容\n    repeated ItemTuple attachments = 18;    //附件\n    int32 expireDays            = 19;   //过期天数\n    int32 totalCount            = 20;   //需要发送总数\n    int32 successCount          = 21;   //发送成功数量\n    bool saveAsDraft            = 22;   //是否存为草稿\n    bool sendDone               = 23;   //是否完成发送\n}\n\n//兑换码 gm.op_exchange_code\nmessage OpExchangeCode {\n    int64 uid                   = 1;\n    int32 timeState             = 2;    //时间状态  enum TIME_STATE\n    int32 verifyState           = 3;    //审核状态  enum VERIFY_STATE\n    int32 hardState             = 4;    //enum HARD_STATE\n\n    repeated string targetChannels  = 5;    //渠道\n    string remark               = 6;    //备注\n    int64 startStamp            = 7;    //开始时间\n    int64 endStamp              = 8;    //结束时间\n    int32 generateType          = 9;   //生成方式 1:指定兑换码 2:批量生成 3:导入兑换码\n    int32 generateCount         = 10;   //生成数量\n    int32 maxExchangeCount      = 11;   //兑换次数上限\n    string exchangeCodePrefix   = 12;   //兑换码前缀\n    int32 exchangeCodeLength    = 13;   //兑换码长度\n    int32 userScope             = 14;    //enum MAIL_SCOPE 玩家范围 1:所有玩家   2:指定玩家 uin  3:等级区间\n    int32 minLevel              = 15;   //userScope == 3 时, 等级区间\n    int32 maxLevel              = 16;\n    string targetUins           = 17;   //userScope == 2 时, 玩家 uin 列表, |分割\n    repeated ItemTuple attachments = 18;    //附件\n    int32 successCount          = 19;   //已成功兑换人数\n}\n\n//gm 生成的兑换码 gm.exchange_code\nmessage ExchangeCode {\n    string code         = 1;\n    int64 uid           = 2;    //关联 OpExchangeCode.uid\n    int32 exchangeTimes = 3;    //已兑换次数\n}\n\n//玩家已使用的兑换码 game.actor_exchange_code\nmessage ActorExchangeCode {\n    int64 uin           = 1;\n    string code         = 2;\n    int64 stamp         = 3;    //兑换时间\n}\n\n//派遣信息 game.actor_battle_dispatch\nmessage BattleDispatchInfo {\n    int64 uin           = 1;\n    int32 activityId    = 2;    //活动本的活动 id, 非活动本传 0\n    int32 sceneType     = 3;    //副本类型\n    int32 stageId       = 4;    //关卡 id\n    bytes data          = 5;    //DispatchData 序列化后的数据\n}\n\n\n//ip 白名单 gm.whitelist_ip\nmessage WhitelistIP {\n    string ip           = 1;    //ip 地址\n    string remark       = 2;    //备注\n    string operator     = 3;\n    int64 createStamp   = 4;    //创建时间\n}\n\n//白名单类型\nenum WHITELIST_TYPE {\n    WLT_NONE            = 0;\n    IP                  = 1;    //ip 地址\n    ACCOUNT_ID          = 2;    //账号 id\n    UIN                 = 3;    //玩家 uin\n}\n\nmessage WhitelistInfo {\n    string whiteTag     = 1;\n    int32 whiteType     = 2;    //enum WHITELIST_TYPE\n    string remark       = 3;    //备注\n    string operator     = 4;\n    int64 createStamp   = 5;    //创建时间\n}\n\n//图片上传记录 gm.uploadPicRecord\nmessage UploadPicRecord {\n    string picName  = 1;\n    string picUrl   = 2;\n    int64 stamp     = 3;\n}\n\n\n//获得的 cg 和 bgm  game.actor_story_cgbgm_group\nmessage StoryCgBgmGroup {\n    int64 uin               = 1;\n    int32 groupId           = 2;\n    repeated int32 cgBgmIds = 3;\n}\n\n//音乐收藏 game.actor_sound\nmessage ActorSound {\n    int64 uin = 1;\n    repeated int32 staredSoundLst  = 2;    //收藏的音乐\n    repeated int32 soundPlaylist   = 3;    //播放列表\n}\n\nmessage ActivityItem {\n    int64 uid   = 1;\n    int32 id    = 2;\n    int32 count = 3;\n}\n//活动存储数据\nmessage ActivityStoreInfo {\n    int64 uin                       = 1;    //\n    int32 activityId                = 2;\n    int64 uid                       = 3;    //所属活动的uid   \n    bytes storeData                 = 4;    //根据活动类型存储\n    map <int32,ActivityItem> items  = 5;    //活动物品 id->物品\n    int64 lastItemResetStamp        = 6;    //上次物品重置时间\n}\n// 签到活动数据\nmessage SignInActInfo {\n    int32   curDay              = 1;    \n    int64 lastSignInStamp       = 2;\n}\n//搜索活动\nmessage SearchActInfo {\n    int64 lastSearchStamp = 1;\n    repeated ItemTuple dropRewards      = 2;    //掉落奖励\n    repeated ItemTuple showRewards      = 3;    //显示奖励\n    repeated ItemTuple specialRewards   = 4;    //额外奖励\n    repeated int32  choosePos           = 5;    //选择位置\n    int32 curCount                      = 6;\n}\n\n//回归签到活动\nmessage ReturnActInfo {\n    int32 returnDay = 1;  //已回归天数\n    int32 signDay   = 2;  //已签到的天数\n    int64 triggerStamp = 3; //回归触发时间\n}\n\n//转盘活动\nmessage TurnTableInfo {\n    map<int32,int32>  turnList = 1;\n    int32 freeGet              = 2;    //免费次数是否领取\n}\n//转盘活动多轮次(累充抽奖)\nmessage TurnTableRoundInfo {\n    map<int32,TurnTableInfo>  rounds = 1;\n    int64 freeStamp                  = 2;    //免费领取时间\n    int32 totalRechargeAmount        = 3;    //总充值金额\n    int32 fetchedRechargeLevel       = 4;    //已领取的充值奖励档位\n    int64 dailyRechargeRewardTime    = 5;    //累充每日领取时间\n    int32 resetCount                 = 6;    //重置次数\n}\nmessage MiniGameData {\n   repeated MiniGameRecord records          = 1;    //小游戏记录\n   int32 miniScore                          = 2;    //小游戏累积积分\n   int32 miniDailyStat                      = 3;    //小游戏每日奖励 TASK_STATE\n   int32 miniDailyScore                     = 4;    //小游戏每日累积积分\n   int32 miniHighScore                      = 5;    //小游戏最高积分\n   int32 miniDailyNum                       = 6;   //小游戏每日次数\n   map<int32,int32> extraCount              = 7;    //小游戏额外数据\n}\nmessage MiniGameRecord {\n    map<int32,int32> counts = 1;\n    int32           point   = 2;\n    int64           stamp   = 3;\n}\n//关卡活动数据\nmessage StageActInfo {\n   repeated int32 challengeStages           = 1;    //挑战通关关卡\n   map<int32,int32>    boughtItem           = 2;    //已经购买的商品 格子ID->购买数量\n   repeated   int32 signDay                 = 3;    //已经签到的天\n   int32 creamCount                         = 4;    //素材本挑战次数\n   repeated MiniGameRecord records          = 5;    //小游戏记录\n   int32 miniScore                          = 6;    //小游戏累积积分\n   int32 miniDailyStat                      = 7;    //小游戏每日奖励 TASK_STATE\n   int32 miniDailyScore                     = 8;    //小游戏每日累积积分\n   int32 miniHighScore                      = 9;    //小游戏最高积分\n   int32 miniDailyNum                       = 10;   //小游戏每日次数\n   map<int32,MiniGameData> miniGames        = 11;   //小游戏数据\n}\n\n//多倍掉落\nmessage DropMulti {\n    int32 type  = 1;\n    int32 multi = 2;\n    int32 count = 3;\n    int32 maxCount = 4;\n}\n\n//回归活动\nmessage ReturnProActInfo {\n    int32 triggerCount              = 1; //触发次数\n    int64 startStamp                = 2;\n    int64 endStamp                  = 3;\n    int32 freeReward                = 4;\n    int32 signReward                = 5;\n    repeated DropMulti dailyDrop    = 6;\n    map<int32,int32>    boughtItem  = 7;    //已经购买的商品 格子ID->购买数量\n    int64 dailyTaskUin              = 8;\n    int32 costItemCount             = 9;         \n}\n\n//掉落活动\nmessage DropMultiActInfo {\n    repeated DropMulti dailyDrops    = 1;\n}\n\n//探险领地信息\nmessage ActorManor {\n    int64 uin           = 1;\n    int32 mapId         = 2;    //当前所在地图\n    string coordinate   = 4;    //当前坐标\n    int32 mapLevel      = 6;    //地图等级\n    int32 tokenConsumeCount = 8;    //代币消耗数量\n    int32 shopFreeCount     = 9;    //深渊商店免费领取次数\n    bool rookieFinished     = 10;   //是否已通关新手区域\n    bool rookieReward       = 11;   //是否已领取新手区域奖励\n    string guildWarCoordinate = 12; //所在公会战地图坐标\n    map<int32,string> actCoordinates    = 13;   //活动地图坐标    mapId -> coordinate\n}\n\nmessage ManorStoryOption {\n    int32 storyId                   = 1;\n    repeated int32 optionIndexes    = 2;    //随机出来的选项索引,从 0 开始\n}\n\n//探险队领地事件 game.actor_manor_event\nmessage ManorEvent {\n    int64 uin           = 1;\n    int32 eventId       = 2;    //事件 id\n    int32 mapId         = 3;    //地图 id\n    int32 gridId        = 4;    //事件所在格子组 id\n    int32 plotNodeId    = 5;    //支线事件节点进度 当前完成的节点 id, 为 0 表示当前正在处理第一个节点\n    int64 plotNodeStamp = 6;    //支线事件节点处理事件    有的后置节点会间隔一段时间触发, 客户端以此来做定时\n    int32 nextPlotNodeId= 7;    //支线事件下一个待处理的节点\n    string coordinate   = 8;    //事件坐标位置\n    int64 resetStamp    = 9;    //事件重置时间   (如果是支线事件: 为 0 表示,这个事件还没有被创建出来,只是标识这个格子组会有这个事件,需要客户端来触发)\n    int64 finishStamp   = 10;   //事件结束时间   不为 0 表示事件已结束\n    int32 processTimes  = 11;   //处理次数\n    repeated ManorNodeProgress progress = 12; //若是支线事件并且已完成这里记录所有的进度信息\n    int32 parentId      = 13;   //所属 id\n    string parameter    = 14;\n    repeated int32 finishedStoryId    = 15; //当前完成的 storyId\n    repeated ManorStoryOption options = 16; //剧情中随机出来的选项\n    int32 coordinateVersion = 17;   //事件当前坐标版本  如果和当前配置不一致,就重新生成坐标\n    int64 nextResetStamp = 18;  //下次重置时间\n    bool suspend         = 19;  //事件是否暂停 用于活动支线事件, 暂停后不能继续处理\n    ManorStoryProgress storyProgress  = 20; //剧情进度\n    int32 eventType      = 21;  //事件类型\n}\n\n//探险队领地事件的位置\nmessage ManorEventPosition {\n    int64 uin                    = 1;\n    map<int32, string> positions = 2;   //eventId -> gridId|coordinate\n}\n\n//剧情进度\nmessage ManorStoryProgress {\n    repeated int32 stories = 1;     //记录剧情走向,仅记录分叉选择\n    int32 lastStory        = 2;     //最后触发的 story\n}\n\n//探险队领地事件结点处理记录\nmessage ManorNodeProgress {\n    int32 nodeId           = 1;     //当前结点Id\n    repeated int32 stories = 2;     //如果是剧情类型的话 记录剧情走向  优化: 仅记录分叉选择\n    int32 lastStory        = 3;     //最后触发的 story\n}\n\n//植物系统\nmessage PlantInfo {\n    int64 uin                           = 1;\n    map<int32,int32>  unlockFlower      = 2;//解锁的花朵 \n    int64   plantTaskUid                = 3;\n    int32   taskDailyRewarded           = 4;//每日任务奖励领取次数\n}\n//常规任务系统\nmessage ComTaskInfo {\n    int64 uin                       = 1;\n    map<int32,int64>    taskList    = 2;\n    repeated int32 dailyRewards     = 3;    //天目标已领奖阶段\n    repeated int32 totalRewards     = 4;    //总目标已领奖阶段\n}\n//任务系统\nmessage CycleTaskInfo {\n    int64 uin                       = 1;\n    repeated int64    taskList      = 2;\n    repeated int32 weeklyRewards    = 3;    //周目标已领奖阶段\n}\n//竞技场奖励类型\nenum ARENA_REWARD_TYPE {\n    ATR_NONE        = 0;\n    ATR_SEASON      = 2;    //赛季奖励\n    ATR_WEEKLY      = 3;    //周奖励\n}\n\n//怪物图鉴组 game.actor_story_monster_group\nmessage StoryMonsterGroup {\n    int64 uin                 = 1;\n    int32 groupId             = 2;   //组 id, 一个组保存 32 个 monsterId\n    repeated int32 monsterIds = 3;\n}\n\n//已点击事迹组 game.actor_clicked_story_group\nmessage ClickedStoryEventGroup {\n    int64 uin               = 1;\n    int32 groupId           = 2;    //组 id, 一个组保存 32 个 monsterId\n    repeated int32 eventIds = 3;\n}\n\n//角色的事迹信息\nmessage CardClickedStoryEventInfo {\n    int64 uin               = 1;\n    int32 cardId            = 2;\n    repeated int32 eventIds = 3;\n}\n\n//内部订单  game.actor_pay_transaction\nmessage PayTransaction {\n    int64 uin               = 1;\n    int64 uniqueId          = 2;\n    int32 productBaseId     = 3;    //base_pay_product.id\n    string productId        = 4;\n    int64 stamp             = 5;\n    int32 state             = 6;    //订单状态\n    string nonce            = 7;    //透传参数  uniqueId:transactionId\n}\n\n//通用充值订单 gm.common_recharge_order\nmessage CommonRechargeOrder {\n    string orderId          = 1;    //本次充值在平台上的订单号\n    string transactionId    = 2;    //商店订单号(由Apple, Google, Alipay, 微信等平台提供)\n    string productId        = 3;    //产品标识,作为充值依据\n    string sdkUid           = 4;    //sdk 玩家的唯一标识\n    int64 payStamp          = 5;   //支付时间\n    string srvId            = 6;    //游戏服务器ID\n    string nonce            = 7;    //充值透传参数(可选)\n    string payType          = 8;    //支付方式  (apple,googleplay,alipay,wechat,web,benefits)\n    int64 expireStamp       = 9;    //订阅过期时间戳(秒) 仅续订充值项有效\n    bool isFreeTrial        = 10;    //是否免费试用 仅续订充值项有效\n    string channel          = 11;   //充值 sdk 渠道\n    int32 money             = 12;   //支付金额(单位：分)\n    int32 pay_money         = 13;   //实际支付金额\n    int32 game_money        = 14;   //应用内货币\n    string currency         = 15;   //货币类型\n    string userIP           = 16;   //ip地址\n}\n\n//haoplay 充值平台的充值订单通知\nmessage HaoPlayRechargeOrder {\n    string productid        = 1;    //产品标识,作为充值依据\n    int64 uid               = 2;    //玩家的唯一标识\n    string order            = 3;    //本次充值在平台上的订单号\n    string transactionid    = 4;    //商店订单号(由Apple, Google, Alipay, 微信等平台提供)\n    string srvid            = 5;    //游戏服务器ID\n    string nonce            = 6;    //充值透传参数(可选)\n    string paytype          = 7;    //支付方式  (apple,googleplay,alipay,wechat,web,benefits)\n    int64 expires_date_ms   = 8;    //订阅过期时间戳(毫秒) 仅续订充值项有效\n    bool is_free_trial      = 9;    //是否免费试用 仅续订充值项有效\n    int32 price             = 10;\n    string currency         = 11;   //货币类型 例如: RMB, USD\n    string user_ip          = 12;\n}\n\n//充值平台的订阅订单通知\nmessage HaoPlaySubscribeOrder {\n    string productid        = 1;    //产品标识\n    int32 uid               = 2;    //玩家的唯一标识\n    string srvid            = 3;    //游戏服务器ID\n    string order            = 4;    //首次订阅原始平台订单号\n    string nonce            = 5;    //首次订阅原始订单透传参数\n    string expires_date_ms  = 6;    //订阅过期时间戳(毫秒)\n}\n\n//bilibili 充值平台回调通知\nmessage BiliRechargeOrder {\n    string id               = 1;    //订单ID\n    string order_no         = 2;    //bilibili游戏SDK服务器方订单号\n    string out_trade_no     = 3;    //游戏CP厂商支付订单号\n    string uid              = 4;    //B站用户ID\n    string username         = 5;    //用户名\n    string role             = 6;    //角色名\n    string money            = 7;    //支付金额(单位：分)\n    string pay_money        = 8;    //实际支付金额，单位：分\n    string game_money       = 9;    //应用内货币\n    string merchant_id      = 10;   //商户ID\n    string game_id          = 11;   //游戏ID\n    string zone_id          = 12;   //区服ID\n    string product_name     = 13;   //商品名称\n    string product_desc     = 14;   //商品描述\n    string pay_time         = 15;   //订单支付时间\n    string client_ip        = 16;   //客户端IP\n    string extension_info   = 17;   //额外信息，原样通知回来\n    int32 order_status      = 18;   //订单状态：1为已完成\n    string sign             = 19;   //md5加密后的签名\n}\n\n//退款等待封禁用户 gm.actor_refund_wait_block\nmessage ActorRefundWaitBlock {\n    int64 uin           = 1;\n    int32 diamondCount  = 2;    //退款扣为负数,进入名单时的钻石数量\n    int64 stamp         = 3;\n}\n\n//礼包系统\nmessage GiftItem {\n    int32 giftId                = 1;\n    int64 getStamp              = 2;    //获取时间\n    repeated int32 rewards      = 3;    //已经领奖的阶段\n    int32 boughtNum             = 4;    //购买次数\n}\nmessage GiftInfo {\n    int64 uin                     = 1;\n    repeated GiftItem gifts       = 2;    //已经购买的礼包\n    \n}\n\n//补给系统\nmessage SupplyInfo {\n    int64 uin               = 1;\n    repeated int32 rewards  = 2;\n}\n\n\n//探险队演练伤害记录 guild.guild_practice_record\nmessage GuildPracticeRecord {\n    int64 uin           = 1;\n    int32 stageId       = 2;    //关卡 id\n    int64 totalDamage   = 3;    //总伤害\n    int64 guildUid      = 4;\n    int64 stamp         = 5;\n    map<int32, CardInfo> pos2CardInfos = 6; //角色布阵位置     position -> CardInfo\n    map<int64, int64> cardUid2Damages  = 7; //每个角色的伤害   cardUid -> damage\n    int32 leaderCardId  = 8;    //队长角色 id\n}\nmessage CardFaceInfo {\n    int32 cardId = 1;\n    int32 fashionId = 2;\n}\nmessage BossChallengeRecord {\n    int64 score                     = 1;\n    map<int32,int32>  cardList      = 2;    //参战角色     id -> showid\n}\n//Boss挑战数据\nmessage BossInfo {\n    int64 uin               = 1;\n    int32 season            = 2;    //周期\n    int32 fighterCount      = 3;    //普通挑战次数\n    int32 challengeCount    = 4;    //高难挑战次数\n    int64 highScore         = 5;    //最高积分 \n    int32   curStage        = 6;    //当前关卡\n    repeated int32 finishStage                = 7;    //已经通关的关卡\n    repeated BossChallengeRecord challenges   = 8;    //当前挑战数据\n    bool isStart            = 9;\n    repeated int32  rewardStages              = 10;  //已领取奖励\n    int32 oldRank           = 11;   //老排名\n    int32 highRank          = 12;   //最高排名\n}\n\n//竞技场匹配的对手信息 game.actor_arena_match\nmessage ArenaMatchInfo {\n    int64 uin           = 1;\n    int32 seasonId      = 2;\n    bytes matchInfo     = 3;    //sproto.ArenaMatchData\n}\n\n//玩家操作记录 game.actor_operate_record\nmessage OperateRecord {\n    int64 uin               = 1;\n    int32 opType            = 2;    //操作类型值\n    repeated int32 values   = 3;\n}\nmessage BuffStage  {\n    int32 stageId               = 1;\n    int32 buffLayer             = 2;\n    map<int32,int32> targets    = 3; //KEY:cfg VALUE:CHALLENGE_STAT_TYPE\n    int64 openStamp             = 4;    //开启时间\n    int32 score                 = 5;    //积分\n    bool isUnLock               = 6;    //是否解锁\n}\n\nmessage BuffStageInfo {\n    int64 uin                   = 1;\n    int64 endStamp              = 2;\n    int32 chapterId             = 3;\n    map<int32,BuffStage> stages = 4;\n    int32 chapterTarget         = 5;    //CHALLENGE_STAT_TYPE\n    map<int32,int32>    highScore = 6;\n    map<int32,int32>    highBuffLayer = 7;\n}\n//密约信息\nmessage AgreementInfo {\n    int64 uin               = 1;\n    int32   season          = 2;\n    repeated int32 rewards  = 3;\n    repeated int32 openList = 4;\n}\nmessage AgreementData {\n    repeated int32 rewards  = 1;\n    repeated int32 openList = 2;\n    int64 refreshStamp      = 3;\n}\nmessage AgreementsInfo {\n    int64 uin                       = 1;\n    map<int32,AgreementData> infos  = 2;\n}\n\n\n\n\n\n//匹配条件,如果bsonRaw有数据,使用bsonRaw进行匹配,否则使用kvs按顺序进行匹配\nmessage DbFilter {\n    bytes bsonRaw          = 1;     //bson.D raw数据,用来支持复杂的查询条件,例如: { $or: [ {platform: {$gt:0}}, {password: \"123456\"} ] }, bson编码\n    repeated KvPair kvs    = 2;\n    DbSortKey sortKey      = 3;\n    bool secondaryPref     = 4;     //读策略是否为 SecondaryPreferred\n    uint32 modKey          = 5;\n}\n\nmessage DbSortKey {\n    string field           = 1;\n    bool ascend            = 2;    //true: 升序  false: 降序\n}\n\n//请求查询按条件匹配大批的数量\nmessage DbQueryCountReq {\n    string tableName       = 1;\n    DbFilter filter        = 2;\n}\n\nmessage DbQueryCountRsp {\n    int64 count = 1;\n}\n\n//按条件查询一行数据\nmessage DbQueryUniqueDataReq {\n    string tableName       = 1;\n    DbFilter filter        = 2;\n}\n\nmessage DbQueryUniqueDataRsp {\n    bytes raw             = 1;\n}\n\n//findOneAndUpdate\nmessage DbQueryOneAndUpdateReq {\n    string tableName       = 1;\n    DbFilter filter        = 2;\n    bytes raw              = 3;\n}\n\nmessage DbQueryOneAndUpdateRsp {\n    bytes raw             = 1;\n}\n\n//按条件查询多行数据\nmessage DbQueryBatchDataReq {\n    string tableName    = 1;\n    DbFilter filter     = 2;\n    int32 skip          = 3;\n    int32 limit         = 4;\n    repeated DbSortKey sortKeys = 5;\n}\n\nmessage DbQueryBatchDataRsp {\n    repeated bytes raws = 1;\n}\n\nmessage DbIndex {\n    repeated string fields  = 1;\n    bool unique             = 2;\n    bool useKv              = 3;    //是否使用 kvFields 字段创建索引\n    repeated KvPair kvFields= 4;\n}\n\n//创建索引\nmessage DbCreateIndexReq {\n    string database     = 1;\n    string tableName    = 2;\n    repeated DbIndex indexes = 3;\n}\n\nmessage DbCreateIndexRsp {\n\n}\n\n//按条件删除数据\nmessage DbDeleteDataReq {\n    string tableName       = 1;\n    DbFilter filter        = 2;\n}\n\nmessage DbDeleteDataRsp {\n    int64 deleteCount      = 1;\n}\n\n//插入数据\nmessage DbInsertDataReq {\n    string tableName    = 1;\n    repeated bytes raws = 2;\n}\n\nmessage DbInsertDataRsp {\n    int64 insertCount   = 1;\n}\n\n//按条件更新一行数据\nmessage DbUpdateDataReq {\n    string tableName    = 1;\n    DbFilter filter     = 2;\n    bytes raw           = 3;\n}\n\nmessage DbUpdateDataRsp {\n\n}\n\n//更新一条记录,不存在则插入\nmessage DbUpsertDataReq {\n    string tableName    = 1;\n    DbFilter filter     = 2;\n    bytes raw           = 3;\n}\n\nmessage DbUpsertDataRsp {\n\n}\n\n\n//按条件更新多行数据\nmessage DbUpdateBatchDataReq {\n    string tableName    = 1;\n    DbFilter filter     = 2;\n    bytes raw           = 3;\n}\n\nmessage DbUpdateBatchDataRsp {\n    int64 modifyCount   = 1;\n}\n\nmessage DbOp {\n    uint32 cmd      = 1;\n    bytes opRaw     = 2;\n}\n\n//在事务里执行多个操作\nmessage DbTransactionOpReq {\n    repeated DbOp ops = 1;\n    bool forceTx      = 2;  //强制事务执行\n}\n\nmessage DbTransactionOpRsp {\n\n}\n\nmessage AllocGameReq {\n    string openId   = 1;\n    string deviceId = 2;\n    string channel  = 3;\n    int32 platform  = 4;\n    string sdkOpenId = 5;    //第三方 sdk 的 openId\n}\n\nmessage AllocGameRsp {\n    string dbId     = 1;\n    string gameId   = 2;\n    int64 uin       = 3;\n}\n\nmessage DbTableDropReq {\n\tstring tableName    = 1;\n}\nmessage DbTableDropRsp {\n}\n\n\n\n//派遣信息\nmessage DispatchGroup {\n    repeated int32 cardId       = 1;\n    int64       overStamp       = 2;\n    ItemTuple extraCost         = 3;\n    bool    isExtra             = 4;\n    int32 rewardId              = 5;\n}\nmessage DispatchInfo {\n    int64 uin                           = 1;\n    int32 level                         = 2;\n    int32 exp                           = 3;\n    map <int32,DispatchGroup> groups    = 4;    //groupid->DispatchGroup\n    int64 levelUpStamp                  = 5;    //升级时间\n}\n\n\n//获取信息\nmessage GetDispatchInfoReq {\n}\n\nmessage DispatchGroupShow {\n    int32 groupId               = 1;\n    int32 rewardId              = 2;\n    repeated int32 cards        = 3;\n    int64       overStamp       = 4;\n    bool    isExtra             = 5;\n\n}\nmessage GetDispatchInfoRsp {\n    repeated DispatchGroupShow groups   = 1;\n    int32 level                         = 2;\n    int32 exp                           = 3;\n}\n//开始派遣\nmessage StartDispatchInfoReq {\n    int32 groupId           = 1;\n    int32 rewardId          = 2;\n    repeated int32 cards    = 3;\n    int32 extraPos          = 4;\n}\n\nmessage StartDispatchInfoRsp {\n    repeated DispatchGroupShow groups = 1;\n}\n\n//派遣领奖\nmessage RewardDispatchInfoReq {\n        int32 groupId  = 1;\n}\n\nmessage RewardDispatchInfoRsp {\n    repeated DropTuple drops = 1;\n    repeated DispatchGroupShow groups = 2;\n    int32 level                       = 3;\n    int32 exp                         = 4;\n}\n//取消派遣\nmessage CancelDispatchInfoReq {\n    int32 groupId  = 1;\n}\n\nmessage CancelDispatchInfoRsp {\n    repeated DispatchGroupShow groups = 1;\n    ItemTuple returnItem              = 2;\n}\n\n\n\n\n//获取远征信息\nmessage GetExpeditionInfoReq {\n\n}\n\nmessage GetExpeditionInfoRsp {\n    int32 curStage                          = 1;    //当前进度\n    repeated ChapterInfo chapters           = 2;    //当前章节\n    int64 nextRefreshStamp                  = 3;    //下次更新时间\n    repeated ExpeditionStateRecord records  = 4;    //挑战记录  \n    repeated int32 rewards                  = 5;    //已经领取奖励的index\n    int32 highPassStar                      = 6;    //最高通关关卡\n    int32 cycle                             = 7;    //周期(百位为周期类型,个位十位为周期)\n}\n\n\n//领取远征奖励\nmessage GetExpeditionRewardReq {\n    int32 rewardId          = 1;\n}\n\nmessage GetExpeditionRewardRsp {\n    repeated DropTuple goods            = 1;    //领取的奖励\n    repeated int32 rewards              = 2;    //已经领取的奖励\n}\n\n\n\n\n\n\n//请求招募信息\nmessage GetGachaInfoReq {\n\n    \n}\nmessage GachaPoolShow {\n    int32   poolId                  = 1;\n    int32 point                     = 2;    //兑换点数\n    map<int32,int32>   exchangeList = 3;    //卡片ID->兑换次数\n    int32   target                  = 4;    //目标卡\n    int32 extraRewarded             = 5;    //领取的额外奖励卡片\n    int32 gachaCount                = 6;    //抽卡次数\n    int32 floorMax                  = 7;    //保底上限\n    int32 floorCount                = 8;    //保底计数\n    bool isReach                    = 9;    //是否硬保底\n}\nmessage GetGachaInfoRsp {\n    map<int32,int64>           openList = 1;  //卡池ID->结束时间(-1为无限期)\n    repeated GachaPoolShow    poolList  = 2; //卡池ID->卡池信息\n    map<int32,int32>    dailyGachaCount = 3; //modid->每日已经抽卡次数\n    map<int32,int32>    totalGachaCount = 4; //modid->总计抽卡次数\n    map<int32,int32>    dailyFreeCount  = 5;//modid->每日免费抽卡次数\n}\n\n\n//招募\nmessage DoGachaReq {\n    int32 gachaMode = 1;\n}\n\nmessage DoGachaRsp {\n    repeated DropTuple drops            = 1;  \n    repeated GachaPoolShow poolInfo     = 2;\n    map<int32,int32>    dailyGachaCount = 3; //modid->每日抽卡次数\n    map<int32,int32>    totalGachaCount = 4; //modid->总计抽卡次数\n    map<int32,int64>           openList = 5;  //卡池ID->结束时间(-1为无限期)\n    map<int32,int32>    dailyFreeCount  = 6;//modid->每日免费抽卡次数\n    int32   poolId                      = 7;\n}\n\n\n//兑换招募物品\nmessage ExchangeGachaReq {\n    int32 poolId = 1;\n    int32 itemId = 2;   \n}\n\nmessage ExchangeGachaRsp {\n    DropTuple reward                = 1;\n    GachaPoolShow poolInfo          = 2;\n}\n\n//抽卡记录\nmessage GetGachaRecordsReq {\n    int32 poolId = 1;\n}\nmessage GetGachaRecordsRsp {\n    repeated  GachaRecord records       = 1; //timestamp->抽卡记录\n}\n\n//设置抽卡目标\nmessage SetGachaTargetReq {\n    int32 gachaId   = 1;\n    int32 cardId    = 2;\n}\n\nmessage SetGachaTargetRsp {\n    GachaPoolShow poolInfo          = 2;\n}\n\n//获取额外奖励\nmessage GetGachaExtraReq {\n    int32 gachaId   = 1;\n    int32 cardId    = 2;\n}\n\nmessage GetGachaExtraRsp {\n    DropTuple reward                = 1;  \n    GachaPoolShow poolInfo          = 2;\n}\n\n\n\n//发送全服邮件\nmessage SendGlobalMailReq {\n    GlobalMail mailInfo = 1;\n}\n\nmessage SendGlobalMailRsp {\n\n}\n\n//发送私人邮件\nmessage SendPrivateMailReq {\n    int64 toUin         = 1;    //接收方uin\n    MailInfo mailInfo   = 2;\n}\n\nmessage SendPrivateMailRsp {\n\n}\n\n//拉取全服邮件\nmessage FetchGlobalMailReq {\n    int64 seqId = 1;\n}\n\nmessage FetchGlobalMailRsp {\n    repeated GlobalMail mails = 1;\n    int64 globalMailSeq     = 2;\n}\n\n//封禁角色\nmessage BanActorReq {\n    int64 uin       = 1;\n    int32 banSecs   = 2;    //封禁秒数\n    DateTime banDate  = 3;    //封禁到某个时间点\n    \n}\n\nmessage BanActorRsp {\n}\n\n//踢掉角色\nmessage KickActorReq {\n    int64 uin       = 1;\n    int32 reason    = 2;\n}\nmessage KickActorRsp {\n}\n\n\n\n//公会成员角色类型\nenum GUILD_ROLE_TYPE {\n    GRT_NONE        = 0;\n    GRT_LEADER      = 1;    //队长\n    GRT_VICE_LEADER = 2;    //副队长\n    GRT_NORMAL      = 3;    //普通成员\n}\n\n//获取公会列表\nmessage GetGuildListReq {\n    int32 skip      = 1;\n    int32 count     = 2;\n}\n\nmessage GetGuildListRsp {\n    repeated GuildInfo infos = 1;\n}\n\n//创建公会\nmessage CreateGuildReq {\n    string name         = 1;\n    string targetSvcId  = 2;\n}\n\nmessage CreateGuildRsp {\n    GuildInfo info      = 1;\n    string serviceId    = 2;    //公会所在服务节点  公会内部的其他请求在消息头中设置 Head.serviceId\n\n    repeated GuildMember members = 3;   //公会成员\n}\n\n//获取自己所在公会信息\nmessage GetMyGuildInfoReq {\n    bool withMember     = 1;    //是否需要获取公会成员信息\n    string extData      = 2;\n}\n\n//弹劾信息\nmessage ImpeachInfo {\n    int64 initiatorUin  = 1;    //弹劾发起人 uin\n    int32 approveCount  = 2;    //支持数量\n    int32 opposeCount   = 3;    //反对数量\n    int32 myVote        = 4;    //自己的投票 0: 未投票  1: 支持   2: 反对   4: 没有投票权限\n    int64 endTimeout    = 5;    //还剩下多长时间弹劾结束 秒\n}\n\nmessage GetMyGuildInfoRsp {\n    GuildInfo info      = 1;\n    string serviceId    = 2;    //公会所在服务节点  公会内部的其他请求在消息头中设置 Head.serviceId\n\n    repeated GuildMember members        = 3;    //公会成员\n    ImpeachInfo impeachInfo             = 4;    //弹劾信息 如果 GuildInfo.impeaching == true, 才有数据\n\n    repeated GuildApplicant applicants  = 5;    //申请者列表\n    int64 joinCdStamp                   = 6;    //退出公会后重新加入新的公会 cd 截止时间戳\n    string extData                      = 7;\n    int32 roleType                      = 8;\n\n    bool createdGuild                   = 9;    //是否创建过公会\n    bool appliedGuild                   = 10;   //是否申请加入过公会\n}\n\n//获取别人的公会信息\nmessage GetOtherGuildInfoReq {\n    int64 guildUid = 1;\n}\n\nmessage GetOtherGuildInfoRsp {\n    GuildInfo info = 1;\n}\n\n//获取公会成员 uin 列表     服务端使用\nmessage GetGuildMembersReq {\n    bool simplify = 1;\n}\n\nmessage GetGuildMembersRsp {\n    int64 guildUid              = 1;\n    repeated int64 memberUinLst = 2;\n\n    repeated GuildMember members        = 3;    //公会成员\n    repeated GuildApplicant applicants  = 4;    //申请者列表\n}\n\n//通过名字搜索公会\nmessage SearchGuildByNameReq {\n    string name     = 1;\n    int32 offset    = 2;    //分页获取\n}\n\nmessage SearchGuildByNameRsp {\n    repeated GuildInfo infos = 1;\n    bool hasMore             = 2;   //是否需要还有需要分页\n}\n\n//修改公会图标\nmessage ChangeGuildIconReq {\n    int32 iconId = 1;\n}\n\nmessage ChangeGuildIconRsp {\n}\n\n//修改公会名字\nmessage ChangeGuildNameReq {\n    string name = 1;\n}\n\nmessage ChangeGuildNameRsp {\n}\n\n//修改公会公告\nmessage ChangeGuildNoticeReq {\n    string notice = 1;\n}\n\nmessage ChangeGuildNoticeRsp {\n    string notice = 1;\n}\n\n//设置公会加入等级限制\nmessage SetGuildLevelLimitReq {\n    int32 levelLimit = 1;\n}\n\nmessage SetGuildLevelLimitRsp {\n}\n\n//请求加入公会\nmessage ApplyJoinGuildReq {\n    int64 guildUid = 1;\n}\n\nmessage ApplyJoinGuildRsp {\n    GuildInfo info = 1;     //点击了申请加入公会,客户端刷新该公会的信息\n    bool hasIn     = 2;     //是否已经直接加入了公会\n}\n\n//撤销加入公会的申请\nmessage CancelJoinGuildReq {\n    int64 guildUid = 1;\n}\n\nmessage CancelJoinGuildRsp {\n}\n\n//处理公会的加入申请\nmessage ProcessGuildJoinApplyReq {\n    int64 applicantUin  = 1;    //申请者 uin, 为0则表示全部处理\n    bool agree          = 2;    //是否同意加入\n}\n\nmessage ProcessGuildJoinApplyRsp {\n}\n\n//操作公会副队长\nmessage OperateGuildViceLeaderReq {\n    int64 targetUin = 1;    //对方 uin\n    bool promote    = 2;    //true: 晋升为副队长  false: 降职副队长\n}\n\nmessage OperateGuildViceLeaderRsp {\n}\n\n//踢出公会成员\nmessage KickOutGuildMemberReq {\n    int64 targetUin = 1;\n}\n\nmessage KickOutGuildMemberRsp {\n}\n\n//移交公会队长给其他人\nmessage TransferGuildLeaderReq {\n    int64 targetUin = 1;\n}\n\nmessage TransferGuildLeaderRsp {\n}\n\n//解散公会\nmessage DismissGuildReq {\n}\n\nmessage DismissGuildRsp {\n}\n\n//退出公会\nmessage ExitGuildReq {\n}\n\nmessage ExitGuildRsp {\n}\n\n//获取推荐的公会\nmessage GetRecommendGuildReq {\n    bool firstRecommend = 1;    //第一次进界面发这个请求时设置为 true, 在界面内点击 \"刷新列表\" 就发 false\n}\n\nmessage GetRecommendGuildRsp {\n    repeated GuildInfo infos = 1;\n}\n\n//弹劾队长\nmessage StartImpeachGuildLeaderReq {\n}\n\nmessage StartImpeachGuildLeaderRsp {\n    ImpeachInfo impeachInfo = 1;\n}\n\n//弹劾投票\nmessage VoteImpeachGuildLeaderReq {\n    bool approve = 1;   //是否赞成弹劾\n}\n\nmessage VoteImpeachGuildLeaderRsp {\n    ImpeachInfo impeachInfo = 1;\n}\n\n//通知公会玩家消耗了体力\nmessage NotifyGuildConsumeEnergyReq {\n    int32 energyCount   = 1;\n}\n\n//快速加入公会\nmessage QuickJoinGuildReq {\n}\n\nmessage QuickJoinGuildRsp {\n}\n\n//自动加入公会    服务端内部使用\nmessage AutoJoinGuildReq {\n    int64 guildUid  = 1;\n}\n\nmessage AutoJoinGuildRsp {\n}\n\n//获取玩家公会的 guildUid\nmessage GetUserGuildUidReq {\n}\n\nmessage GetUserGuildUidRsp {\n    int64 guildUid  = 1;\n    string svcId    = 2;    //公会所在的服务节点 id\n}\n\n//获取已发送申请的公会列表\nmessage GetAppliedGuildsReq {\n}\n\nmessage GetAppliedGuildsRsp {\n    repeated GuildInfo guildInfos = 1;\n}\n\n//设置公会目标\nmessage SetGuildTargetReq {\n    repeated int32 targetIdxes = 1;   //当前勾选的公会目标索引\n}\n\nmessage SetGuildTargetRsp {\n}\n\n//获取弹劾信息\nmessage GetImpeachInfoReq {\n\n}\n\nmessage GetImpeachInfoRsp {\n    bool impeaching  = 1;   //是否在弹劾中\n    ImpeachInfo info = 2;   //弹劾信息\n}\n\n//获取自己公会的简要信息\nmessage GetMyGuildSimpleInfoReq {\n\n}\n\nmessage GetMyGuildSimpleInfoRsp {\n    int64 guildUid      = 1;    //公会 uid, 大于 0 表示在公会中\n    string guildName    = 2;    //公会名字\n    int32 roleType      = 3;    //玩家在公会中的职位     enum GUILD_ROLE_TYPE\n    string notice       = 4;    //当前公告内容\n}\n\nenum GUILD_EVENT_TYPE {\n    GE_NONE             = 0;\n    GE_APPROVE_JOIN     = 1;    //被同意加入公会\n    GE_KICK_OUT         = 2;    //被踢出公会\n}\n\n//公会状态变更通知\nmessage GuildEventNotify {\n    GUILD_EVENT_TYPE eventType  = 1;\n    string guildName            = 2;    //公会名字\n}\n\n//设置探险队的活动方针\nmessage SetGuildPolicyReq {\n    int32 policy = 1;\n}\n\nmessage SetGuildPolicyRsp {\n}\n\n//搜索探险队\nmessage SearchGuildByConditionsReq {\n    int32 offset        = 1;    //分页获取\n\n    string name         = 2;    //探险队名字\n    int32 MinMemberCnt  = 3;    //min 成员人数\n    int32 MaxMemberCnt  = 4;    //max 成员人数\n    int32 policy        = 5;    //活动方针\n    int32 guildWarRankOpt  = 7;    //上期公会战排名选项 0: 不限, 1: 1-5名, 2: 6-60名, 3: 前10%, 4: 前30%, 5: 前50%\n    int32 joinCondition = 8;    //加入条件 0: 不限  1: 自由加入  2: 需要审核\n}\n\nmessage SearchGuildByConditionsRsp {\n    repeated GuildInfo infos = 1;\n    bool hasMore             = 2;   //是否还有更多结果\n}\n\n\n\n\nmessage GuildPracticeRankData {\n    int64 uin           = 1;\n    string name         = 2;\n    int32 totalDamage   = 3;    //总伤害\n    int32 rank          = 4;    //排名 从 1 开始\n    int64  stamp        = 5;\n    int32 faceId        = 6;\n    ActorHead actorHead = 7;\n}\n\n//获取某个演练关卡的排名\nmessage GetGuildPracticeRankReq {\n    int32 stageId = 1;  //关卡 id\n}\n\nmessage GetGuildPracticeRankRsp {\n    int32 stageId = 1;\n    repeated GuildPracticeRankData rankDataLst = 2;\n}\n\n//获取某个演练关卡详细记录数据\nmessage GetGuildPracticeRecordReq {\n    int32 stageId   = 1;\n    int64 targetUin = 2;\n}\n\nmessage GetGuildPracticeRecordRsp {\n    GuildPracticeRecord record = 1;\n}\n\nmessage SaveGuildPracticeRecordReq {\n    GuildPracticeRecord record = 1;\n}\n\nmessage SaveGuildPracticeRecordRsp {\n    int64 historyDamageMax = 1;\n    int32 curRank          = 2; //当前排名\n}\n\n\n//公会战\n\n\n\n//公会战状态\nenum GuildWarState {\n    GWS_NONE            = 0;\n    GWS_NOTICE          = 1;    //公告期\n    GWS_FIGHT           = 2;    //挑战期\n    GWS_SETTLE_WAIT     = 3;    //结算等待期\n    GWS_SETTLE          = 4;    //结算期\n    GWS_CLOSE           = 5;    //关闭期\n}\n\n//公会战阶段信息\nmessage GuildWarSchedule {\n    int32 seasonId      = 1;    //赛季 id\n    int32 phase         = 2;    //BaseGuildWar 使用的 phase\n    int32 state         = 3;    //enum GuildWarState\n    int64 startStamp    = 4;\n    int64 endStamp      = 5;\n}\n\n//公会的公会战进度数据\nmessage GuildWarProgress {\n    int64 guildUid      = 1;\n    int32 seasonId      = 2;\n    int32 round         = 3;    //当前关卡最低轮次\n    int32 score         = 7;    //积分\n    repeated GuildWarBoss allBoss = 9;  //当前所有 boss 状态\n}\n\n//各个位置 boss 信息\nmessage GuildWarBoss {\n    int32 index         = 1;    //boss 位置索引 (1-5)\n    int32 round         = 2;    //boss 轮次\n    int32 stageId       = 3;    //当前关卡  0: 表示打通了所有 boss\n    int32 leftHpPercent = 4;    //剩余血量百分比, 临时计算\n    bool locked         = 5;    //是否锁定中\n    repeated ObjectState bossStates = 6;    //boss 状态\n}\n\nmessage GuildWarRankInfo {\n    int64 uin       = 1;\n    int32 rank      = 2;\n    int32 rankRatio = 3;\n}\n\n//战术技能编队\nmessage GuildWarSkillTeam {\n    int32 teamId            = 1;    //1 - 4\n    repeated int32 skillIds = 2;\n    bool used               = 3;    //是否当前使用中\n}\n\n//公会战玩家自己的数据\n//存储在 game 库  game.actor_guild_war\nmessage ActorGuildWar {\n    int64 uin                           = 1;\n    int32 seasonId                      = 2;    //当前数据所属的赛季,如果和当前系统赛季不一致,就需要重置数据\n    map<int32,int32> assistCardId2Count = 3;    //当前设置的助战角色的助战次数 cardId -> 助战次数\n    map<int32,int32> skill2Level        = 4;    //战术技能等级\n    int32 fightCount                    = 6;    //已挑战次数\n    int64 dailyResetStamp               = 7;    //每日重置时间\n    repeated int64  taskUid             = 8;    //任务列表\n    repeated int32 usedSelfCardIds      = 9;    //已使用的自己角色 cardId\n    repeated int32 usedAssistCardIds    = 10;   //已使用的助战角色 cardId\n    repeated GuildWarSkillTeam skillTeams = 11; //战术技能编队列表\n    int64 lastFightStamp                = 12;   //上次战斗时间\n}\n\n//补偿战斗阵容    game.actor_guildwar_compensate_formation\nmessage GuildWarCompensateFormation {\n    int64 uin               = 1;\n    int32 compensateUid     = 2; //补偿阵容uid(生成补偿阵容的关卡id)\n    int32 compensateTime    = 3; //补偿战斗时长\n    repeated CardSimple cardInfos                = 4;    //上阵角色数据, 包含自己的和助战的\n    int32 leaderCardId                           = 5;    //队长角色 id\n    repeated BurstOrderSetting burstOrderSetting = 6;    //总攻技能释放顺序设置\n}\n\n//公会战战斗结果数据\nmessage GuildWarBattleResult {\n    int32 compensateTime    = 1;    //获得的补偿时长(秒)\n    bool bossDeadBefore     = 2;    //true: 结算时 boss 已阵亡\n}\n\n//推荐阵容(一个关卡在 redis 保存伤害前 100 的阵容)\nmessage GuildWarRecommendFormation {\n    int32 stageId           = 1;    //关卡 id\n    int64 fighterUin        = 2;    //挑战者 uin\n    string fighterName      = 3;    //挑战者名字\n    repeated CardSimple cardInfos = 4;   //上阵角色列表\n    int64 damageHp          = 6;    //伤害值\n    int64 battleUid         = 7;    //战斗回放uid\n    repeated SkillLevel skillLevels = 8;    //使用的战术技能\n    int32 battleTime        = 9;    //战斗时长\n    int32 version           = 10;\n}\n\n//公会战战斗记录\nmessage GuildWarBattleRecord {\n    int32 stageId       = 1;    //关卡 id\n    int32 round         = 2;    //轮次\n    int64 damageHp      = 3;    //伤害值\n    int64 battleUid     = 4;    //战斗回放uid\n    int64 stamp         = 5;    //挑战时间\n    int32 version       = 6;\n}\n\n//获取公会战阶段信息\nmessage GetGuildWarScheduleReq {\n}\n\nmessage GetGuildWarScheduleRsp {\n    GuildWarSchedule schedule = 1;\n    bool inGuild              = 2;  //是否已加入公会\n}\n\n//获取公会战所有相关信息\nmessage GetGuildWarAllInfoReq {\n}\n\nmessage GetGuildWarAllInfoRsp {\n    GuildWarSchedule schedule       = 1;    //公会战赛程状态\n    GuildWarProgress progress       = 2;    //公会战进度\n    ActorGuildWar actorGuildWar     = 3;    //自己的信息\n    bool inGuild                    = 4;    //当前是否在公会中\n    repeated TaskInfo tasks         = 5;    //任务列表\n}\n\n//获取补偿阵容\nmessage GetGuildWarCompensateFormationReq {\n}\n\nmessage GetGuildWarCompensateFormationRsp {\n    repeated GuildWarCompensateFormation formations = 1;\n}\n\n//升级战术技能\nmessage LevelupGuildWarSkillReq {\n    int32 skillId = 1;\n}\n\nmessage LevelupGuildWarSkillRsp {\n    int32 skillId = 1;\n    int32 level   = 2;\n}\n\n//设置助战角色\nmessage SetGuildWarAssistCardReq {\n    repeated int32 cardIds = 1;\n}\n\nmessage SetGuildWarAssistCardRsp {\n    map<int32,int32> assistCardId2Count = 1;    //当前设置的助战角色的助战次数 cardId -> 助战次数\n}\n\n//获取推荐阵容\nmessage GetGuildWarRecommendFormationReq {\n    int32 stageId = 1;  //关卡 id\n}\n\nmessage GetGuildWarRecommendFormationRsp {\n    repeated GuildWarRecommendFormation formations = 1;\n}\n\n//设置战术技能方案\nmessage SetGuildWarSkillTeamReq {\n    GuildWarSkillTeam team = 1;\n}\n\nmessage SetGuildWarSkillTeamRsp {\n    repeated GuildWarSkillTeam skillTeams = 1;\n}\n\n//获取公会战战斗记录\nmessage GetGuildWarBattleRecordReq {\n}\n\nmessage GetGuildWarBattleRecordRsp {\n    repeated GuildWarBattleRecord records = 1;\n}\n\n//获取积分排行榜信息\nmessage GuildRankInfo {\n    int64 guildUid              = 1;\n    int32 level                 = 2;    //等级\n    int32 iconId                = 3;    //头像ID\n    string name                 = 4;    //名字\n    int32 rank                  = 5;    //排行\n    int64 score                 = 6;    //积分\n    int32 memberCount           = 7;    //成员数量\n    int32 actCount              = 8;    //参与数量\n    int32 round                 = 9;    //轮次\n}\n\nmessage GuildWarMemberRankInfo {\n    int64 uin                   = 1;\n    int32 level                 = 2;    //等级\n    string name                 = 3;    //名字\n    ActorHead actorHead         = 4;   //头像信息\n    int32   rank                = 5;    //排行\n    int64 score                 = 6;    //积分\n\n}\n\nmessage GetGuildWarRankReq {\n}\n\nmessage GetGuildWarRankRsp {\n    repeated    GuildRankInfo guildList          = 1;    //公会排名\n    repeated GuildWarMemberRankInfo memberList   = 2;    //成员排名\n    int32       rank                             = 3;    //自己公会排名\n    int32 rankRatio                              = 4;    //自己公会排名比例\n    GuildRankInfo mineGuild                      = 5;    //自己公会 \n    \n}\n\nmessage GetGuildWarRankExtReq {\n}\n\nmessage GetGuildWarRankExtRsp {\n    repeated    GuildRankInfo guildList          = 1;    //公会排名\n    repeated GuildWarMemberRankInfo memberList   = 2;    //成员排名\n    int32       rank                             = 3;    //自己公会排名\n    int32 rankRatio                              = 4;    //自己公会排名比例\n    GuildRankInfo mineGuild                      = 5;    //自己公会\n}\n\n//公会战任务\nmessage RewardGuildWarTaskReq {\n    int64 taskUid               = 1;    //领奖任务\n}\n\nmessage RewardGuildWarTaskRsp {\n    repeated DropTuple goods    = 1;    //领取的奖励\n    TaskInfo task               = 2;\n}\n\n//获取当前正在挑战的人数\nmessage GetGuildWarInBattleCountReq {\n\n}\n\nmessage GetGuildWarInBattleCountRsp {\n    map<int32, int32> index2BattleCnt = 2;    //每个关卡正在挑战人数 bossIndex -> cnt\n}\n\n\n\n//消息类型\nenum MSG_TYPE {\n    MSG_NONE        = 0;\n    MSG_TEXT        = 1;\n    MSG_EMOJI       = 2;\n    MSG_JOIN_GUILD  = 3;    //加入公会的提示信息 ChannelMsg.fromUin 字段标识加入公会玩家 uin\n}\n\n//会话类型\nenum IM_SESSION_TYPE {\n    IST_NONE    = 0;\n    PRIVATE     = 1;        //私聊\n    UNION       = 2;        //公会聊天\n    WORLD       = 3;        //世界聊天\n}\n\nmessage MutedBySystemNotify {\n    int32 muteReason            = 1;    //enum RET_CODE\n    int32 durationInSec         = 2;    //禁言时长 秒\n    repeated int32 muteChannels = 3;    //被禁言的频道 enum IM_SESSION_TYPE\n    bool mute                   = 4;    //是否已禁言\n}\n\nmessage ChannelMsg {\n    int32 msgType       = 1;    //enum MSG_TYPE\n    int32 cliSeq        = 2;    //客户端上传一个消息序列号\n    int64 msgId         = 3;    //消息id 服务器生成\n    int32 sessionType   = 4;    //enum IM_SESSION_TYPE\n    string sessionId    = 5;    //会话ID  只有世界频道聊天需要传频道的 sessionId\n    int64 fromUin       = 6;    //发送者uin\n    int64 toUin         = 7;    //接受者uin,群聊填0\n    int64 stamp         = 8;    //发送时间\n\tstring content      = 9;    //消息内容\n    int32 emojiId       = 10;   //消息类型为 MSG_EMOJI 时, 设置为该表情的 id\n}\n\n//消息读取进度\nmessage MsgProgress {\n    int64 uin           = 1;\n    int64 targetUin     = 2;    //聊天对象 id\n    int32 sessionType   = 3;    //enum IM_SESSION_TYPE\n    int64 newestMsgId   = 4;    //最新消息 id\n    int64 readMsgId     = 5;    //当前已读消息进度\n}\n\n//请求发送IM消息\nmessage SendMessageReq {\n    ChannelMsg  channelMsg = 1;\n}\n\n//发送IM消息回包\nmessage SendMessageRsp {\n    ChannelMsg  channelMsg = 1;\n}\n\n//请求拉取IM消息\nmessage SyncMessageReq {\n    int32 sessionType   = 1;    //enum IM_SESSION_TYPE    客户端维护这3个syncKey\n    string sessionId    = 2;\n    int64 syncKey       = 3;\n}\n\n//拉取IM消息回包\nmessage SyncMessageRsp {\n    int32 sessionType           = 1;    //enum IM_SESSION_TYPE\n    int64 syncKey               = 2;\n    bool hasMore                = 3;    //是否还有新消息需要继续拉取\n    repeated ChannelMsg msgList = 4;\n\n    repeated ActorMirrorInfo senderInfos = 5;    //消息发送方的信息 uin -> ActorMirrorInfo\n    map<int64,int64> uin2FlushMsgTime    = 6;    //uin -> stamp 世界频道中该玩家的消息时间小于这个值就过滤掉\n}\n\n//拉取私聊对象的历史消息\nmessage SyncPrivateHistoryMessageReq {\n    int64 targetUin     = 1;    //私聊对象的 uin\n    int64 msgId         = 2;    //第一次拉历史消息传 0, 后续分页拉取就传上次回复的第一条消息的 msgId    (目前不用)\n}\n\n//拉取历史消息回包\nmessage SyncPrivateHistoryMessageRsp {\n    int64 targetUin             = 1;\n    repeated ChannelMsg msgList = 2;\n    ActorMirrorInfo targetInfo  = 3;    //对方的信息\n    bool hasMore                = 4;    //是否还有历史消息可以继续拉取\n}\n\n//IM新消息通知\nmessage NewMessageNotify {\n    int32 sessionType           = 1;    //enum IM_SESSION_TYPE\n    ActorMirrorInfo senderInfo  = 2;    //发送方的信息\n\n    int64 syncKey               = 3;    //世界频道的聊天消息通知才会发 syncKey 和 channelMsg\n    ChannelMsg channelMsg       = 4;\n}\n\n//给玩家分配世界聊天线路\nmessage AllocUserWorldGroupReq {\n\n}\n\nmessage AllocUserWorldGroupRsp {\n    string sessionId = 1;\n}\n\nmessage WorldLineInfo {\n    int32 lineId        = 1;\n    string sessionId    = 2;    //线路的 sessionId\n    int32 loadPercent   = 3;    //负载万分比\n}\n\n//获取世界频道线路信息\nmessage GetWorldLineInfoReq {\n}\n\nmessage GetWorldLineInfoRsp {\n    repeated WorldLineInfo lineInfoLst = 1;\n}\n\n//切换世界聊天线路\nmessage SwitchWorldGroupReq {\n    string dstSessionId = 1;\n}\n\nmessage SwitchWorldGroupRsp {\n    WorldLineInfo lineInfo = 1;\n}\n\n//举报理由\nenum E_REPORT_REASON {\n    ERR_NONE        = 0;\n    ERR_PORN        = 1;    //色情\n    ERR_POLITICS    = 2;    //反动政治\n    ERR_ADS_FRAUD   = 3;    //广告欺诈\n    ERR_ABUSE       = 4;    //谩骂骚扰\n    ERR_OTHER       = 5;    //其他\n}\n\n//举报其他玩家\nmessage ReportUserReq {\n    int64 targetUin         = 1;    //被举报玩家 uin\n    repeated int32 reasons  = 2;    //enum E_REPORT_REASON\n    int64 msgId             = 3;    //被举报消息的 msgId\n    string sessionId        = 4;    //被举报消息所在的 sessionId\n    string content          = 5;    //被举报的消息内容\n}\n\nmessage ReportUserRsp {\n\n}\n\n//获取多个聊天频道(世界, 社团, 私聊)的最新的一条消息在主界面展示\nmessage GetChannelNewestMessageReq {\n\n}\n\nmessage GetChannelNewestMessageRsp {\n    repeated ChannelMsg msgList             = 1;\n    repeated ActorMirrorInfo senderInfos    = 2;\n    WorldLineInfo myLineInfo                = 3;    //自己所在线路信息\n    repeated int32 mutedChannels            = 4;    //被禁言的频道    enum IM_SESSION_TYPE\n    repeated int64 unReadTargetUinLst       = 5;    //有未读消息的聊天对象 uin\n    bool unionUnRead                        = 6;    //是否有未读的公会消息\n}\n\n//获取正在聊天的私聊对象\nmessage GetPrivateChattingTargetReq {\n\n}\n\nmessage GetPrivateChattingTargetRsp {\n    repeated ActorMirrorInfo infos = 1;\n}\n\n//修改私聊对象\nmessage ChangePrivateChattingTargetReq {\n    int64 addTargetUin  = 1;    //添加某个聊天对象的 uin\n    int64 delTargetUin  = 2;    //移除某个聊天对象的 uin\n}\n\nmessage ChangePrivateChattingTargetRsp {\n\n}\n\n//获取聊天相关状态\nmessage GetChatStateReq {\n\n}\n\nmessage GetChatStateRsp {\n    int32 muteReason            = 1;    //enum RET_CODE\n    int32 durationInSec         = 2;    //禁言时长 秒   mute = true 且 durationInSec = 0 表示永久禁言\n    repeated int32 muteChannels = 3;    //被禁言的频道 enum IM_SESSION_TYPE\n    bool mute                   = 4;    //是否被禁言\n}\n\n//设置聊天消息已读\nmessage MarkMessageReadReq {\n    int32 sessionType   = 1;    //enum IM_SESSION_TYPE\n    int64 targetUin     = 2;    //聊天对象 uin, 社团聊天就发 0\n    int64 msgId         = 3;    //最后一条消息的 msgId\n}\n\nmessage MarkMessageReadRsp {\n}\n\n\n\n\n\n//资源大种类\nenum TUPLE_TYPE {\n    TT_NONE     = 0;\n    ITEM        = 1;    //物品\n    CARD        = 2;    //卡牌\n    BADGE       = 3;    //徽章\n    T_FASHION   = 4;    //时装\n    CG          = 5;    //CG\n    BGM         = 6;    //bgm\n    STORY_MONSTER = 7;    //怪物图鉴\n    GIFT        = 8;    //礼包\n}\n\n//通用物品类型\nenum ITEM_TYPE {\n    IT_NONE             = 0;\n    BIND_DIAMOND        = 1;    //绑钻\n    RECHARGE_DIAMOND    = 2;    //充值钻\n    GAME_COIN           = 3;    //金币\n    ENERGY              = 4;    //体力\n    ROLE_EXP            = 5;    //玩家经验\n    CARD_EXP            = 6;    //卡牌经验\n    MONTH_CARD          = 11;  //月卡\n    BATTLE_PASS         = 12;  //通行证\n    BATTLE_PASS_SINIOR  = 13;  //通行证-高级\n    BATTLE_PASS_ACTIVITY= 14;  //通行证-活动\n    SEAL                = 16;   //印章\n    EXP_ITEM            = 101;  //经验药水\n    CONSUME_MATERIAL    = 102;  //消耗材料\n    UNIVERSAL_CARD      = 103;  //万能角色卡\n    SAME_NAME_CARD      = 104;  //同名角色卡\n    BADGE_EXP_ITEM      = 105;  //徽章经验药水\n    MANOR_SALEABLE_ITEM = 107;  //大地图可兑换道具\n    HEAD_ITEM           = 108;  //头像\n    HEAD_RECT_ITEM      = 109;  //头像框\n    EMOJI               = 110;  //表情\n    RANDOM_PACKAGE      = 201;  //随机礼包\n    CHOSEN_PACKAGE      = 202;  //选择礼包\n    REGULAR_PACKAGE     = 203;  //固定礼包\n    FIX_COUNT_PACKAGE   = 204;  //固定数量兑换礼包  N个物品兑换一次奖励\n    PROFESSION_PACKAGE  = 205;  //职业选择礼包\n    ARENA_MAP           = 301;  //竞技场地图\n    ARENA_BUILDING      = 302;  //竞技场建筑\n    ROGUE_ITEM          = 401;  //肉鸽相关物品\n}\n\nenum TIMES_TYPE {\n    TIMES_TYPE_NONE     = 0;\n    TT_ENERGY           = 1;    //体力\n    TT_ARENA_FIGHT      = 2;    //竞技场挑战\n}\n\n//次数资源\nenum CNT_RESOURCE_TYPE {\n    CRT_NONE                    = 0;\n    CRT_ENERGY_BUY_TIMES        = 1;    //体力已购买次数\n    CRT_ARENA_BUY_FIGHT_TIMES   = 2;    //竞技场已购买次数\n    CRT_ARENA_TOTAL_FIGHT_COUNT = 3;    //竞技场总共可挑战次数\n}\n\nmessage ItemDrop {\n    ItemTuple item  = 1;\n    int32 prob      = 2;    //概率\n}\n\n//获取所有物品\nmessage GetItemsReq {\n\n}\n\n//获取所有物品\nmessage GetItemsRsp {\n    repeated ItemInfo items = 1;\n    int64 syncKey           = 2;    //用于增量同步的syncKey\n}\n\n//同步变化的物品\nmessage SyncItemsReq {\n    int64 syncKey = 1;\n}\n\nmessage SyncItemsRsp {\n    repeated ItemInfo items         = 1;    //新增或有变化的物品\n    repeated int64 delItemUidLst    = 2;    //需要删除的物品 itemUid\n    int64 syncKey                   = 3;    //新的syncKey\n    bool cliReq                     = 4;    //是否是客户端主动来请求的\n    int64 lastSyncKey               = 5;    //服务器上次主动通知时的 key, 如果客户端本地值相同, 说明客户端全部收到了之前的通知, 否则客户端主动发送 syncItemsReq 来更新\n}\n\n//购买次数资源\nmessage BuyCountResourceReq {\n    int32 timesType     = 1;    //enum CNT_RESOURCE_TYPE\n    int32 count         = 2;    //购买次数\n}\n\nmessage BuyCountResourceRsp {\n    int32 timesType                 = 1;    //enum TIMES_TYPE\n    map<int32, int32> cntResources  = 2;    //次数资源\n}\n\n//使用物品(开礼包)\nmessage UseItemReq {\n    int64 itemUid   = 1;    //物品id\n    int32 count     = 2;    //使用数量\n    string params   = 3;    //参数    选择礼包: 选择第几个物品, 从 1 开始\n}\n\nmessage UseItemRsp {\n    repeated DropTuple items = 1;   //使用礼包后获得的物品\n}\n\n//批量使用物品\nmessage BatchUseItemsReq {\n    map<int64, int32> itemUid2Count = 1;    //itemUid -> count\n}\n\nmessage BatchUseItemsRsp {\n    repeated DropTuple items = 1;   //使用礼包后获得的物品\n}\n\n//卖出物品\nmessage SaleItemReq {\n    int64 itemUid   = 1;    //物品id\n    int32 count     = 2;\n}\n\nmessage SaleItemRsp {\n    ItemTuple item  = 1;    //卖出后得到的东西\n}\n\n//消耗物品  服务端内部使用\nmessage ConsumeItemReq {\n    repeated ItemTuple items    = 1;\n    LOG_ID logId                = 2;\n}\n\nmessage ConsumeItemRsp {\n}\n\n//检查物品是否足够  服务端内部使用\nmessage CheckItemEnoughReq {\n    repeated ItemTuple items    = 1;\n}\n\nmessage CheckItemEnoughRsp {\n    bool enough = 1;\n}\n\n//兑换卡牌碎片\nmessage ExchangeCardFragmentReq {\n    int32 itemId        = 1;\n    int32 count         = 2;\n    int32 targetItemId  = 3;    //兑换的目标物品 id\n}\n\nmessage ExchangeCardFragmentRsp {\n    ItemTuple item      = 1;    //兑换后得到的物品\n}\n\n//使用物品兑换体力\nmessage ExchangeEnergyReq {\n    map<int64, int32> items = 1;    //itemUid -> count\n}\n\nmessage ExchangeEnergyRsp {\n}\n\n//请求已获得的怪物图鉴\nmessage GetStoryMonsterListReq {\n}\n\nmessage GetStoryMonsterListRsp {\n    repeated int32 storyMonsterIds      = 1;   //已获得的怪物图鉴列表\n    repeated int32 clickedStoryEventId  = 2;   //已点击过的事迹 id\n}\n\n//点击事迹上报\nmessage ClickStoryEventReportReq {\n    repeated int32 eventIds = 1;\n}\n\nmessage ClickStoryEventReportRsp {\n}\n\n\n\n\n\n\n//限时挑战信息\nmessage LimitChallengeInfo {\n    int64 uin                   = 1;\n    repeated int64 taskUid      = 2;\n    repeated int32 passStages   = 3;\n    int32 activityId            = 4;\n\n}\n//获取信息\nmessage GetLimitChallengeInfoReq {\n}\nmessage GetLimitChallengeInfoRsp {\n    int32 activityId            = 1;\n    repeated int32 passStages   = 2;\n    repeated TaskInfo  tasks    = 3;\n    int64 startStamp            = 4;\n    int64 endStamp              = 5;\n}\n\n//重置\nmessage ResetLimitChallengeReq {\n}\n\nmessage ResetLimitChallengeRsp {\n    int32 activityId            = 1;\n    repeated int32 passStages   = 2;\n}\n\n//领取任务\nmessage RewardLimitChallengeTaskReq {\n    int64 taskUin = 1;\n}\n\nmessage RewardLimitChallengeTaskRsp {\n    repeated DropTuple rewards  = 1;\n    TaskInfo  task              = 2;\n    \n}\n\n\n\nmessage LogBase {\n\tint64 uin           = 1;\n\tstring channel      = 2;    //渠道\n\tstring deviceId     = 3;    //设备 id\n\tuint32 createdTime  = 4;    //创建角色时间\n\tuint32 dataTime     = 5;    //日志时间\n\tint32 platform      = 6;    //平台\n\tint32 level         = 7;    //团队等级\n\tint32 day           = 8;    //登录天数\n\tint32 power         = 9;    //战斗力\n\tint32 pay           = 10;   //充值总额度\n}\n\n//登录类型\nenum LOGIN_TYPE {\n    LT_NONE         = 0;\n    LT_DEFAULT      = 1;    //默认登录\n    LT_RECONNECT    = 2;    //重连登录\n    LT_REGISTER     = 3;    //创建角色登录\n}\n\n//登出类型\nenum LOGOUT_TYPE {\n    LOT_NONE            = 0;\n    LOT_DEFAULT         = 1;    //默认登出\n    LOT_SERVER_CLOSE    = 2;    //服务器关闭\n    LOT_GM_KICK         = 3;    //GM 踢下线\n}\n\n//团队操作类型\nenum PLAYER_OPERATE_TYPE {\n    POT_NONE        = 0;\n    POT_GAIN_EXP    = 1;    //获得经验\n    POT_LEVELUP     = 2;    //升级\n}\n\n//卡牌操作类型\nenum CARD_OPERATE_TYPE {\n    COT_NONE            = 0;\n    COT_GAIN_EXP        = 1;    //获得经验\n    COT_LEVELUP         = 2;    //升级\n    COT_QUALITY_UP      = 3;    //突破\n    COT_GRADE_UP        = 4;    //觉醒\n    COT_NORMAL_SKILL_LEVELUP    = 5;    //普攻击技能升级\n    COT_SPECIAL_SKILL_LEVELUP   = 6;    //小技能升级\n    COT_BURST_SKILL_LEVELUP     = 7;    //必杀技能升级\n    COT_GROW_SKILL_1_LEVELUP    = 8;    //被动技能1升级\n    COT_GROW_SKILL_2_LEVELUP    = 9;    //被动技能2升级\n    COT_GROW_SKILL_3_LEVELUP    = 10;    //被动技能3升级\n}\n\n//徽章操作类型\nenum BADGE_OPERATE_TYPE {\n    BOT_NONE            = 0;\n    BOT_GAIN_EXP        = 1;    //获得经验\n    BOT_LEVELUP         = 2;    //升级\n}\n\n//物品操作类型\nenum ITEM_OPERATE_TYPE {\n    IOT_NONE    = 0;\n    IOT_GAIN    = 1;    //获得\n    IOT_CONSUME = 2;    //消耗\n}\n\n//公会操作类型\nenum GUILD_OPERATE_TYPE {\n    GOT_NONE            = 0;\n    GOT_CREATE          = 1;    //创建公会\n    GOT_JOIN            = 2;    //加入公会\n    GOT_EXIT            = 3;    //退出公会\n    GOT_KICK_OUT_MEMBER = 4;    //提出公会\n    GOT_DISMISS         = 5;    //解散公会\n    GOT_CHANGE_BADGE    = 6;    //更改公会徽章\n    GOT_CHANGE_NAME     = 7;    //更改公会名字\n    GOT_CHANGE_NOTICE   = 8;    //更改公会公告\n    GOT_CHANGE_CONDITION= 9;    //修改入会条件\n    GOT_APPROVE         = 10;   //同意入会申请\n    GOT_REJECT          = 11;   //拒绝入会申请\n    GOT_PROMOTE_MEMBER  = 12;   //晋升目标成员\n    GOT_DEMOTE_MEMBER   = 13;   //降级目标成员\n    GOT_SEND_MESSAGE    = 14;   //公会成功发言\n    GOT_GM_SET_LEVEL    = 15;   //GM 修改等级\n    GOT_GM_BLOCK        = 16;   //GM block 聊天和 公告\n    GOT_GM_UNBLOCK      = 17;   //GM unblock 聊天和公告\n}\n\n//邮件操作类型\nenum MAIL_OPERATE_TYPE {\n    MOT_NONE            = 0;\n    MOT_RECEIVE         = 1;    //收到邮件\n    MOT_MARK_READ       = 2;    //标记已读\n    MOT_FETCH_ATTACHMENT= 3;    //领取附件\n    MOT_DELETE          = 4;    //手动删除邮件\n    MOT_EXPIRE          = 5;    //邮件过期删除\n}\n\n//商店操作类型\nenum SHOP_OPERATE_TYPE  {\n    SPOT_NONE           = 0;\n    SPOT_BUY            = 1;    //购买\n    SPOT_REFRESH        = 2;    //刷新\n}\n\n//商店操作类型\nenum TASK_TYPE  {\n    TKT_NONE           = 0;\n    TKT_BATTLAPASS     = 1;    //通行证任务\n    TKT_CAINIVAL       = 2;    //嘉年华任务\n}\n\n\n\n//http 用户验证\nmessage AuthReq {\n    string accountId    = 1;    //邮箱或其他唯一标识\n    string accountType  = 2;\n    string password     = 3;    //游客登录,不用填密码\n    string imei         = 4;\n    string osVersion    = 5;    //os 版本\n    string channel      = 6;    //渠道\n    int32 platform      = 7;    //enum PLATFORM_TYPE\n    bool autoCreate     = 8;    //是否自动创建账号\n}\n\nmessage AuthRsp {\n    string openId   = 1;\n    string token    = 2;\n}\n\n//http 账号密码模式 创建账号\nmessage CreateAccountReq {\n    string accountId    = 1;    //邮箱或其他唯一标识\n    string accountType  = 2;\n    string password     = 3;\n    string imei         = 4;\n    string osVersion    = 5;    //os 版本\n    string channel      = 6;    //渠道\n    int32 platform      = 7;    //enum PLATFORM_TYPE\n}\n\nmessage CreateAccountRsp {\n    string openId   = 1;\n    string token    = 2;\n}\n\n//http 生成引继码\nmessage GenerateInheritCodeReq {\n    string token    = 1;\n    string password = 2;\n}\n\nmessage GenerateInheritCodeRsp {\n    string inheritCode = 1;\n}\n\nmessage AuthByInheritReq {\n    string accountId    = 1;    //传设备 id\n    string imei         = 2;\n    string osVersion    = 3;    //os 版本\n    string channel      = 4;    //渠道\n    int32 platform      = 5;    //enum PLATFORM_TYPE\n\n    string inheritCode  = 6;    //引继码\n    string inheritPwd   = 7;    //印记密码\n}\n\nmessage AuthByInheritRsp {\n    string openId   = 1;\n    string token    = 2;\n}\n\n//http 获取网关地址\nmessage LoginReq {\n    string openId   = 1;\n    string token    = 2;\n    int32 platform  = 3;\n    string channel  = 4;    //PnSDK_CN  Bilibili\n    string buildVersion = 5;\n    bool authRemote = 6;    //是否 sdk 远端验证\n}\n\nmessage LoginRsp {\n    repeated string addresses   = 1;    //网关地址\n    int32 maintainState         = 2;    //维护状态 1:维护中\n    string maintainNotice       = 3;    //维护公告\n    int32 timezoneOffset        = 4;    //时区偏移 秒    例如东8区: 28800\n    string publicKey            = 5;\n}\n\n//http req  第三方平台登录\nmessage LoginByOAuthReq {\n    string openPlat     = 1;    //第三方平台\n    string appId        = 2;\n    string code         = 3;\n    string state        = 4;\n    string imei         = 5;\n    string osVersion    = 6;    //os 版本\n    string channel      = 7;    //渠道\n    int32 platform      = 8;    //enum PLATFORM_TYPE\n}\n\n//http rsp\nmessage LoginByOAuthRsp {\n    repeated string addresses   = 1;    //网关地址\n    int32 maintainState         = 2;    //维护状态 1:维护中\n    int32 timezoneOffset        = 3;    //时区偏移 秒    例如东8区: 28800\n    string token                = 4;\n    string openId               = 5;\n}\n\n\n//客户端连接上gatewaySvr后,首先验证token\nmessage AuthTokenReq {\n    string token    = 1;\n    bool authRemote = 2;    //是否 sdk 远端验证\n    string openId   = 3;    //第三方账号系统的 id\n    string channel  = 4;\n}\n\nmessage AuthTokenRsp {\n    string openId       = 1;\n    string sdkOpenId    = 2;    //第三方 sdk 的 openId\n}\n\nmessage AuthTokenV2Rsp {\n    int32 code      = 1;\n    string error    = 2;\n    int32 uid       = 3;\n}\n\nmessage EnterGameReq {\n    string token        = 1;\n    string secret       = 2;\n    string deviceId     = 3;    //设备 id\n    string channel      = 4;    //渠道\n    int32 platform      = 5;    //sp_common.proto   enum PLATFORM_TYPE\n    bool authRemote     = 6;    //是否 sdk 远端验证\n    string openId       = 7;    //第三方账号系统的 id\n    int32 graphicsDeviceID = 8;\n    int32 graphicsDeviceVendorID = 9;\n    string loginIP       = 10;   //用户 ip 地址\n}\n\nmessage EnterGameRsp {\n    bool actorExist     = 1;    //是否已存在角色\n    ActorInfo actor     = 2;\n    int64 sysStamp      = 3;    //系统时间\n    string svrVersion   = 4;    //服务器版本信息\n    string settings     = 5;    //设置信息\n    int64 openSvrTime   = 6;    //开服时间\n}\n\nenum E_KICKOFF_REASON {\n    E_KR_NONE           = 0;\n    E_KR_SYSTEM         = 1;    //系统踢下线\n    E_KR_OTHER_DEVICE   = 2;    //被其他设备\n    E_KR_CLOSE_SERVER   = 3;    //关服踢下线\n}\n\nmessage KickOffReq {\n    int64 uin       = 1;        //0: 踢所有人下线\n    int32 reason    = 2;        //enum E_KICKOFF_REASON\n}\n\nmessage KickOffRsp {\n\n}\n\nmessage KickOffNotify {\n    int64 uin       = 1;\n    int32 reason    = 2;        //enum E_KICKOFF_REASON\n}\n\n\n\nmessage GetAllMailsReq {\n    int64 mailSeq = 1;              //客户端可以传一个 mailSeq 值,增量拉取新邮件.传 0 即全量拉取\n}\n\nmessage GetAllMailsRsp {\n    int64 mailSeq           = 1;    //更新客户端本地 mailSeq 值\n    repeated MailInfo mails = 2;\n}\n\nmessage FetchMailAttachmentReq {\n    int64 mailUid = 1;  //0: 领取所有附件\n}\n\nmessage FetchMailAttachmentRsp {\n    repeated int64 fetchedUidLst    = 1;    //已领取的邮件 mailUid\n    repeated DropTuple items        = 2;    //领取到的物品\n}\n\nmessage DeleteMailReq {\n    int64 mailUid = 1;\n}\n\nmessage DeleteMailRsp {\n}\n\nmessage MarkMailReadReq {\n    int64 mailUid = 1;\n}\n\nmessage MarkMailReadRsp {\n\n}\n\nmessage NewMailNotify {\n\n}\n\n\n//探险地图\n\n\n\n\n//事件类型\nenum MANOR_EVENT_TYPE {\n    MET_NONE                = 0;\n    MET_INITIATIVE          = 1;    //主动事件\n    MET_ROLE_PLOT           = 2;    //角色剧情\n    MET_DAILY_RANDOM        = 3;    //每日随机事件\n    MET_FIX_BUILDING        = 4;    //固定建筑\n    MET_BARRIER             = 6;    //阻挡物事件\n    MET_BGM_PIC             = 7;    //bgm 图鉴事件\n    MET_MONSTER_PIC         = 8;    //魔物图鉴事件\n    MET_ACTIVITY_ROLE_PLOT  = 10;   //活动支线剧情事件\n    MET_EXPEDITION          = 11;   //远征建筑\n    MET_BOSS                = 12;   //boss 建筑\n    MET_ROGUE               = 13;   //肉鸽建筑\n    MET_CONVEY              = 14;   //传送门\n    MET_BUFF_STAGE          = 15;   //buff累积关卡建筑\n    MET_GROUP_REFRESH       = 21;   //同组刷新事件\n}\n\n//主动事件子类型\nenum MANOR_SUB_EVENT {\n    MSE_NONE            = 0;\n    MSE_BATTLE          = 1;    //战斗\n    MST_PLOT            = 2;    //剧情\n    MST_PACKAGE         = 3;    //宝箱\n    MST_ROAD            = 4;    //路牌\n    MST_SHOP_NPC        = 5;    //商店NPC\n    MST_DOOR            = 6;    //门\n}\n\n//深渊功能开启状态\nmessage ManorFeatureSchedule {\n    int32 eventType = 1;    //enum MANOR_EVENT_TYPE 事件类型, 目前类型 4, 15 会用到\n    bool open       = 2;    //是否开启\n    int64 startTime = 3;    //开启时间\n    int64 endTime   = 4;    //结束时间\n}\n\n//获取探险地图所有所有信息\nmessage GetManorInfoReq {\n    int32 mapId = 1;    //地图 id\n}\n\nmessage GetManorInfoRsp {\n    ActorManor manorInfo            = 1;\n    repeated ManorEvent allEvents   = 2;    //已有的事件\n    int64 actionValueRecoverStamp   = 3;    //行动值完全恢复时间\n    int64 plotValueRecoverStamp     = 4;    //剧情点完全恢复时间\n    repeated ManorFeatureSchedule featureSchedules = 5; //玩法开启状态\n}\n\nmessage GetManorFeatureScheduleReq {\n}\n\nmessage GetManorFeatureScheduleRsp {\n    repeated ManorFeatureSchedule featureSchedules = 1; //玩法开启状态\n}\n\n//获取探险地图简要信息\nmessage GetManorInfoSimpleReq {\n}\n\nmessage GetManorInfoSimpleRsp {\n    ActorManor manorInfo            = 1;\n}\n\n//事件更新通知\nmessage ManorEventUpdateNotify {\n    repeated ManorEvent events    = 1;    //需要更新的事件\n    repeated int32 deleteEventIds = 2;    //删除事件id列表\n}\n\n//探险地图信息更新通知\nmessage ManorInfoUpdateNotify {\n    ActorManor manorInfo = 1;\n}\n\n//传送通知\nmessage ManorConveyNotify {\n    string coordinate   = 1;\n}\n\n//客户端在移动过程中触发一个事件, 仅支线事件第一个节点的触发, 同一组的支线事件只能由一个\nmessage ManorTriggerEventReq {\n    int32 gridId        = 1;    //客户端当前所在格子组\n    string coordinate   = 2;    //客户端当前坐标\n    int32 eventId       = 3;\n    int32 mapSubId      = 4;    //当前所处的地图区域 id\n    string nodeCoordinate = 5;  //支线事件节点坐标\n}\n\nmessage ManorTriggerEventRsp {\n    ManorEvent event    = 1;    //触发的事件信息\n    int64 actionValueRecoverStamp   = 3;    //行动值完全恢复时间\n    int64 plotValueRecoverStamp     = 4;    //剧情点完全恢复时间\n}\n\n//客户端上报自己的位置\nmessage ManorReportPositionReq {\n    string coordinate   = 2;\n    int32 mapId         = 3;\n}\n\nmessage ManorReportPositionRsp {\n}\n\n\n//处理事件 (除战斗外的事件都用这个接口)\nmessage ManorProcessEventReq {\n    int32 eventId   = 1;    //事件 id\n    int32 nodeId    = 2;    //当前处理的支线事件节点 id\n    int32 nextNodeId = 3;   //下一个要处理的节点 id\n    ManorNodeProgress progress = 4; //如果是剧情结点发送该剧情所有的走向包括选项id\n    int32 mapSubId   = 5;   //当前所处的地图区域 id\n    string nodeCoordinate = 6;  //支线事件节点坐标\n}\n\nmessage ManorProcessEventRsp {\n    repeated DropTuple rewards  = 1;    //奖励\n    ManorEvent event            = 2;    //更新事件状态\n    int64 actionValueRecoverStamp   = 4;    //行动值完全恢复时间\n    int64 plotValueRecoverStamp     = 5;    //剧情点完全恢复时间\n}\n\nmessage ManorBatchProcessEventReq {\n    repeated int32 eventIds = 1;\n}\n\nmessage ManorEventReward {\n    ManorEvent event = 1;\n    repeated ItemTuple rewards = 2;\n}\n\nmessage ManorBatchProcessEventRsp {\n    repeated ManorEventReward eventRewards = 1;\n}\n\n//完成一句剧情对话\nmessage ManorFinishStoryReq {\n    int32 eventId   = 1;    //事件 id\n    int32 storyId   = 2;    //当前完成的 storyId\n    ManorStoryProgress storyProgress = 3;\n}\n\nmessage ManorFinishStoryRsp {\n    int32 eventId   = 1;    //事件 id\n    int32 storyId   = 2;    //当前完成的 storyId\n    repeated int32 optionIndexes = 3;   //选项索引\n}\n\n//跳过随机剧情事件\nmessage ManorJumpStoryEventReq {\n    int32 eventId   = 1;    //事件 id\n}\n\nmessage ManorJumpStoryEventRsp {\n    ManorEvent event            = 1;    //更新事件状态\n    int64 actionValueRecoverStamp   = 3;    //行动值完全恢复时间\n    int64 plotValueRecoverStamp     = 4;    //剧情点完全恢复时间\n    repeated DropTuple rewards      = 5;    //奖励\n}\n\n//上报随机事件位置\nmessage ManorReportEventPositionReq {\n    int32 eventId       = 1;    //事件 id\n    string coordinate   = 2;    //位置\n}\n\nmessage ManorReportEventPositionRsp {\n\n}\n\n//领取新手区域奖励\nmessage ManorFetchRookieRewardReq {\n}\n\nmessage ManorFetchRookieRewardRsp {\n    ActorManor manorInfo = 1;\n    repeated ItemTuple rewards = 2;\n}\n\nmessage ManorGetActivityRolePlotEventReq {\n}\n\nmessage ManorGetActivityRolePlotEventRsp {\n    repeated ManorEvent events = 1;\n}\n\n\n\n\n\nenum FLOWER_STATE {\n    FS_NONE     = 0;\n    FS_UNLOCK   = 1;\n    FS_OPEN     = 2;\n    FS_REWARED  = 3;\n}\n//请求植物信息\nmessage GetPlantInfoReq {\n    int64 refreshStamp                          = 1;  \n}\n\nmessage PlantData {\n    int32 plantId               = 1;\n    map<int32,int32> flowers    = 2;  //flowerId->状态\n}\n//回复植物信息\nmessage GetPlantInfoRsp {\n    repeated PlantData plantList    = 1;\n    TaskInfo dailyTask              = 2;\n    int64 refreshStamp              = 3;  \n}\n\n//请求领取开花奖励\nmessage RewardFlowerReq {\n    int32 plantId   = 1;\n    int32 flowerId  = 2;\n}\n\n//回复领取开花奖励\nmessage RewardFlowerRsp {\n    repeated ItemTuple rewards          = 1;\n    repeated PlantData plantList        = 2;\n}\n\n//领取植物任务奖励请求\nmessage RewardPlantTaskReq {\n    int64 taskUid = 1;\n}\n//领取植物任务奖励回复\nmessage RewardPlantTaskRsp {\n    repeated DropTuple rewards  = 1;\n}\n\n\n\nenum PRODUCT_TYPE {\n    PT_NONE             = 0;\n    PT_RECHARGE         = 1;    //充值档位\n    PT_MONTH_CARD       = 2;    //月卡\n    PT_GIFT             = 3;    //礼包\n    PT_BATTLE_PASS      = 4;    //通行证\n    PT_BATTLE_PASS_HIGH = 6;    //特级通行证\n    PT_BATTLE_PASS_DIS  = 7;    //差值通行证\n    PT_AGREEMENT        = 8;    //密约\n\n    PT_FASHION          = 11;   //时装\n}\n\n//支付订单状态\nenum PAY_ORDER_STATE {\n    POS_NONE        = 0;\n    POS_CREATED     = 1;    //创建订单\n    POS_PAYED       = 2;    //支付完成\n    POS_DELIVERY    = 3;    //发货完成\n    POS_CANCELED    = 4;    //取消订单\n    POS_FAIL        = 5;    //失败(订单错误)\n    POS_REFUNDING   = 6;    //退款中, 收到平台退款通知后将订单状态修改为该值\n    POS_REFUND_DONE = 7;    //退款完成\n}\n\nmessage GetPurchaseProductsReq {\n    repeated int32 productTypes = 1;  //PRODUCT_TYPE\n    int32 platformType          = 2;  //PLATFORM_TYPE\n}\nmessage ProductInfo {\n    int32 id            = 1;\n    int32 productType   = 2;    //PRODUCT_TYPE\n    int64 endStamp      = 3;\n    int32 shelfArea     = 4;    //上架区域 大于10000000, 则为 ShopLabel 页签\n    bool newTag         = 5;    //是否是新品标记\n    bool owned          = 6;    //是否拥有（时装）\n    int32 sort          = 7;    //排序ID\n}\n\n//商店页签\nmessage ShopLabel {\n    int64 uid        = 1;\n    int32 sortValue  = 2;    //排序值\n    string labelName = 3;    //页签名字\n    int64 startStamp = 4;    //开始时间\n    int64 endStamp   = 5;    //结束时间\n}\n\nmessage GetPurchaseProductsRsp {\n    repeated ProductInfo list     = 1;\n    repeated ShopLabel shopLabels = 2;\n}\n\n\nmessage PurchaseGetReq {\n    \n}\n\nmessage PurchaseGetRsp {\n    map<int32,int64>   monthCardDay     = 1;\n    map<int32,bool>    monthCardReward  = 2;\n    map<int32, int32>  limitRecord      = 3;    //购买记录\n    bool               isBought         = 4;    //是否首冲\n    WeekPayInfo    weekPayInfo          = 5;    //每周累充信息\n}\n\nmessage PurchaseBuyReq {\n    int32 id            = 1;\n}\n\nmessage PurchaseBuyRsp {\n    repeated ItemTuple reward                = 1;\n    map<int32,int64>   monthCardDay          = 2;\n    map<int32, int32>  limitRecord           = 3;    //购买记录\n    bool                isBought             = 4;    //是否首冲\n}\n\nmessage FashionBuyReq {\n    int32 buyFashionId        = 1;\n}\n\nmessage FashionBuyRsp {\n    int32 buyFashionId        = 1;\n}\n\nmessage MonthCardDailyRewardReq {\n    int32 cardType              = 1;\n}\n\nmessage MonthCardDailyRewardRsp {\n    repeated ItemTuple reward                   = 1;\n    map<int32,bool>   monthCardReward           = 2;\n}\n//购买通行证请求\nmessage BattlePassBuyReq {\n    int32 productId = 1;\n}\n//购买通行证回复\nmessage BattlePassBuyRsp {\n    repeated BattlePassShowInfo allBattlePass = 1;\n}\n\n//创建充值订单\nmessage CreatePayOrderReq {\n    int32 productBaseId = 1;   //base_pay_product.id\n}\n\nmessage CreatePayOrderRsp {\n    int32 productBaseId = 1;   //base_pay_product.id\n    string nonce        = 2;   //传递给 sdk 平台的透传参数\n    string orderSign    = 3;   //for bilibili order_sign\n    string productId    = 4;   //商品名字 base_pay_product.product_id\n}\n\n//取消订单\nmessage CancelPayOrderReq {\n    string nonce    = 1;    //传递给 sdk 平台的透传参数\n}\n\nmessage CancelPayOrderRsp {\n    string nonce        = 1;   //传递给 sdk 平台的透传参数\n    int32 productBaseId = 2;   //base_pay_product.id\n}\n\n//完成订单\nmessage FinishPayOrderReq {\n    string nonce    = 1;    //传递给 sdk 平台的透传参数\n}\n\nmessage FinishPayOrderRsp {\n    string nonce        = 1;    //传递给 sdk 平台的透传参数\n    int32 productBaseId = 2;    //base_pay_product.id\n}\n\n//每周累充 game.actor_week_pay\nmessage WeekPayInfo {\n    int64 uin   = 1;\n    int32 index              = 2;   //当前周期\n    int32 consumeBindDiamond = 3;   //本周消耗的欧泊   大于等于配置里要求的值即可领取改档奖励\n    int32 rechargeAmount     = 4;   //本周充值金额\n    int32 bindDiamondReward  = 5;   //已领取的欧泊消耗奖励值   比如 30 档位的奖励已领取,就记为 30\n    int32 rechargeReward     = 6;   //已领取的充值奖励值\n    int64 resetStamp         = 7;   //周重置时间\n}\n\nenum WEEK_PAY_REWARD_TYPE {\n    WPRT_NONE = 0;\n    WPRT_CONSUME_BIND_DIAMOND   = 1; //累积消耗欧泊奖励\n    WPRT_RECHARGE               = 2; //累积充值奖励\n}\n\nmessage FetchWeekPayRewardReq {\n    int32 rewardType  = 1;  //enum WEEK_PAY_REWARD_TYPE  0:全部领取\n}\n\nmessage FetchWeekPayRewardRsp {\n    int32 rewardType        = 1;  //enum WEEK_PAY_REWARD_TYPE\n    WeekPayInfo weekPayInfo = 2;\n    repeated DropTuple rewards = 3;\n}\n\n\n\n\n\n//关系变更通知\nmessage RelationChangedNotify {\n    RelationInfo info           = 1;\n    ActorMirrorInfo targetInfo  = 2;    //对方信息\n}\n\n//删除收到的好友请求\nmessage RelationDelApplicantNotify {\n    int64 targetUin = 1;\n}\n\n//请求获取好友列表\nmessage GetFriendsReq {\n\n}\n\nmessage GetFriendsRsp {\n    repeated RelationInfo relations         = 1;    //关系列表(好友、收到的申请)\n    repeated ActorMirrorInfo targetInfos    = 2;    //对方的信息\n}\n\n//请求向对方发出添加好友申请\nmessage ApplyAddFriendReq {\n    int64 targetUin = 1;\n}\n\nmessage ApplyAddFriendRsp {\n    RelationInfo info = 1;\n}\n\n//同意对方的好友请求\nmessage AgreeFriendApplyReq {\n    int64 targetUin = 1;        //0 表示同意所有\n}\n\nmessage AgreeFriendApplyRsp {\n    int64 targetUin             = 1;\n    repeated RelationInfo infos = 2;    //更新关系数据 (成为好友或者删除好友请求)\n}\n\n//拒绝对方的好友请求\nmessage DisagreeFriendReq {\n    int64 targetUin = 1;        //0 表示拒绝所有\n}\n\nmessage DisagreeFriendRsp {\n    int64 targetUin = 1;        //客户端直接删除本地数据\n}\n\n//屏蔽其他玩家\nmessage BlockTargetReq {\n    int64 targetUin = 1;\n}\n\nmessage BlockTargetRsp {\n    RelationInfo info           = 1;\n    ActorMirrorInfo targetInfo  = 2;    //对方信息\n}\n\n//请求删除关系: 删除好友、解除屏蔽\nmessage DeleteRelationReq {\n    int64 targetUin = 1;\n}\n\nmessage DeleteRelationRsp {\n    int64 targetUin = 1;\n}\n\n//搜索玩家\nmessage SearchTargetReq {\n    string searchKey = 1;\n}\n\nmessage SearchTargetRsp {\n    repeated RelationInfo infos             = 1;\n    repeated ActorMirrorInfo targetInfos    = 2;    //对方信息\n}\n\n//设置备注名\nmessage SetRelationRemarkReq {\n    int64 targetUin = 1;\n    string remark   = 2;\n}\n\nmessage SetRelationRemarkRsp {\n    RelationInfo info = 1;\n}\n\n//获取所有已屏蔽玩家\nmessage GetAllBlockTargetReq {\n}\n\nmessage GetAllBlockTargetRsp {\n    repeated int64 blockTargets = 1;\n}\n\n\nmessage FriendFightRecord {\n    int64 uin                 = 1;\n    int32 index               = 2;\n    int64 opponentUin         = 3; //对手 uin\n    int64 battleUid           = 4;\n    int64 stamp               = 5;\n    bool isWin                = 6; //是否胜利\n    bool isDefend             = 7; //是否是防守方\n    ActorMirrorInfo opponent  = 8; //对手信息\n}\n\n//获取好友切磋战斗记录\nmessage GetFriendFightRecordReq {\n}\n\nmessage GetFriendFightRecordRsp {\n    repeated FriendFightRecord records = 1;\n}\n\n\n\n\n\n//game.actor_rogue_theme 肉鸽主题数据\nmessage RogueTheme {\n    int64 uin           = 1;\n    int32 themeId       = 2;    //主题 id\n    int32 topScore      = 3;    //最高综合评分\n    int32 level         = 4;    //主题等级\n    int32 rewardedLevel = 5;    //主题等级奖励领取进度\n    int32 exp           = 6;    //主题经验\n    repeated int32 talentIds        = 7;   //已激活的天赋\n    int32 unlockedDifficultyLevel   = 8;   //当前已通关的难度等级\n    int32 curDifficultyLevel        = 9;   //本局选择的难度等级, 0 标识还没有选择过\n    repeated int32 treasureIds      = 10;   //本局已获得的宝物\n    repeated int32 holyIds          = 11;   //本局已解锁的圣物\n    repeated int32 cardIds          = 12;   //本局已招募的角色\n    repeated int32 initTreasureIds  = 13;   //开局供选择的初始宝物\n    bool running                    = 14;   //是否已开局 true: 继续探索流程  false: 开始探索开局流程\n    repeated int32 onceEffTreasures = 15;   //暂未使用的一次性效果宝物\n    int32 freeEnhanceCardTimes      = 16;   //免费角色强化次数\n    int32 chapterId                 = 17;   //当前章节进度\n    repeated int32 starAttribPointAddCosts = 19;    //各星级角色属性强化消耗的属性点增加值(5个值, 分别对应角色5个星级角色的增加值)\n    map<int32, int32> onceTreasureEffBattles = 20;  //宝物效果: 和战斗场次相关的一次性效果, treasureId -> 生效剩余战斗场次 (为 0 了就触发奖励)\n    int64 startTime                 = 21;   //开局时间\n    repeated int32 keyStoryIds      = 22;   //事件节点完成的关键剧情(用于检测是否触发结局)\n    int32 totalTalent               = 23;   //累计获得的天赋点\n    int64 levelupStamp              = 24;   //升级时间\n    int32 sweepCount                = 25;   //已使用的扫荡次数\n    repeated int32 allSealIds       = 26;   //锁定的印章\n    repeated string sealBigAttrs    = 27;   //大印章属性 job:level:quality:addUpLevel\n    int32 handBookGrowId            = 28;   //角色图鉴养成 base_card_hand_book_grow.id\n}\n\n//肉鸽节点类型\nenum ROGUE_NODE_TYPE {\n    ROGUE_NODE_TYPE_NONE    = 0;\n    RNT_NORMAL_BATTLE       = 1;    //常规战斗\n    RNT_ENCOUNTER_BATTLE    = 2;    //遭遇战斗\n    RNT_BOSS_BATTLE         = 3;    //boss 战斗\n    RNT_SHOP                = 11;   //商店\n    RNT_EVENT               = 12;   //事件\n    RNT_SUPPLY              = 13;   //补给\n}\n\n//肉鸽节点奖励类型\nenum ROGUE_REWARD_TYPE {\n    ROGUE_REWARD_TYPE_NONE  = 0;\n    RRT_RECRUIT             = 1;    //招募券\n    RRT_TOKEN               = 2;    //随机代币\n    RRT_ATTRIB_POINT        = 3;    //随机属性点\n    RRT_TREASURE            = 4;    //随机宝物\n    RRT_RECOVER_HP          = 5;    //恢复血量\n    RRT_REVIVE              = 6;    //复活\n    RRT_SPECIFIC_TREASURE   = 7;    //指定宝物\n    RRT_SHOP_BUY_TREASURE   = 11;   //商店购买宝物(仅用于日志打点)\n    RRT_SHOP_REFRESH        = 12;   //商店重置(仅用于日志打点)\n}\n\n//肉鸽节点\nmessage RogueNode {\n    int32 nodeId            = 1;    //节点 id\n    int32 stageId           = 2;    //关卡 id, 仅用于节点类型为: 1常规战斗、2遭遇战斗、3BOSS战斗\n    map<int32, int32> shopTreasure2Prices = 3; //商店宝物id -> 价格  仅用于节点类型为: 11 商店\n    int32 shopResetCount    = 4;    //商店重置次数\n    int32 eventId           = 5;    //事件 id, 仅用于节点类型为: 12事件    base_story 表的 id\n    bool jobDone            = 6;    //该节点任务是否已完成(战斗胜利、完成剧情事件), true 状态才能领取奖励\n    bool extraReward        = 7;    //是否触发额外奖励\n    repeated int32 rewardOptions = 8;     //奖励选项(base_rogue_node_reward 表)\n    repeated int32 doneRewardOptions = 9; //已领取的奖励选项\n    repeated int32 extraBuffIds = 10;     //临时生效的 buff\n    bool finished           = 11;    //该节点是否已处理完成(包括奖励选项)\n    int32 tokenAddPercent = 12;       //战斗节点的代币奖励加成万分比\n    int32 attribPointAddPercent = 13; //属性点奖励加成万分比\n    int32 eventStoryId          = 14; //事件类型节点的 story 进度\n    int32 supplyRewardCount     = 15; //补给节点奖励领取次数上限\n    int32 eventRandTreasure     = 16; //事件节点的剧情里概率获得的宝物\n    int32 keyStoryId            = 17; //事件节点当前关键剧情 id\n}\n\n//动态信息\nmessage RogueTrend {\n    int32 trendId       = 1;\n    bool finished       = 2;  //是否已完成\n    bool unlocked       = 3;  //是否已解锁\n    int64 unlockStamp   = 4;  //解锁时间\n    TaskInfo taskInfo   = 5;    //任务列表\n    int32 taskId        = 6;\n}\n\nenum ROGUE_STAT {\n    ROGUE_STAT_NONE     = 0;\n    LAYER_COUNT         = 1;    //通过层数\n    TOTAL_NODES         = 2;    //通过总节点数\n    TRIGGER_EVENT_COUNT = 3;    //触发事件数\n    NORMAL_BATTLE       = 4;    //常规战斗次数\n    ENCOUNTER_BATTLE    = 5;    //遭遇战次数\n    BOSS_BATTLE         = 6;    //boss战次数\n    NORMAL_BATTLE_LEFT_TIME    = 7;    //常规战斗关卡通关剩余时长\n    LEFT_HP_PERCENT     = 8;    //角色剩余血量万分比\n    TREASURE_COUNT      = 9;    //获取的宝物数\n    TOTAL_TOKEN         = 10;   //获得的累计代币数\n    TOTAL_ATTRIB_POINT  = 11;   //获得的累计属性点\n    RECRUIT_COUNT       = 12;   //招募成员数\n    ATTRIB_POINT_COST   = 13;   //属性点消耗数量\n    REVIVE_COUNT        = 14;   //复活次数\n    ENCOUNTER_BATTLE_LEFT_TIME = 15;    //常规战斗关卡通关剩余时长\n    BOSS_BATTLE_LEFT_TIME      = 16;    //boss战斗关卡通关剩余时长\n}\n\n//game.actor_rogue_chapter 肉鸽章节\nmessage RogueChapter {\n    int64 uin               = 1;\n    int32 themeId           = 2;    //主题 id\n    int32 layerIndex        = 3;    //当前层级\n    int32 chapterId         = 4;    //当前层的章节id\n    repeated int32 finishedNodeIds = 5; //当前层已处理完成的节点\n    RogueNode curNode       = 6; //当前节点信息\n    repeated int32 usedPoolIds = 7; //已使用的 poolId\n    //统计信息\n    map<int32, int32> stats = 8;    //enum ROGUE_STAT -> value\n    map<int32, int32> nextNode2StageIds = 9;    //后置战斗关卡节点的 stageId\n    map<int32, int32> nextNode2PoolId   = 10;   //后置战斗关卡使用的 poolId\n    int32 lastNodeEndingId = 11;    //第 5,6 层最后一个节点触发的 ending\n    bool triggerHideLayer  = 12;    //是否触发了隐藏层\n    int32 finishLayer      = 13;    //已完成的层\n}\n\n//肉鸽图鉴类型\nenum ROGUE_PIC_TYPE {\n    RPT_NONE    = 0;\n    TREASURE    = 1;    //宝物图鉴\n    EVENT       = 2;    //事件图鉴\n    ENDING      = 3;    //结局图鉴\n    HOLY        = 4;    //圣物图鉴\n}\n\n//game.actor_rogue_pic 肉鸽图鉴\nmessage RoguePicInfo {\n    int64 uin                   = 1;\n    int32 themeId               = 2;  //主题 id\n    int32 picType               = 3;  //图鉴列席    enum ROGUE_PIC_TYPE\n    map<int32, bool> picId2States = 4;  //picId -> state  true: 显示 new 标记\n}\n\nmessage RogueRecruitCard {\n    repeated CardInfo allCards = 1;\n    repeated RogueCardBadge cardBadges = 2;\n}\n\nmessage RogueRecruitPool {\n    int64 uin       = 1;\n    bytes poolRaw   = 2;    //RogueRecruitCard\n}\n\n//game.actor_rogue_card 角色信息\nmessage RogueCardInfo {\n    int64 uin           = 1;\n    int32 themeId       = 2;\n    int32 cardId        = 3;\n    CardInfo info       = 4;\n    map<int32, int32> attribLevels = 5;    //属性等级 attributeId -> level\n    repeated string rogueAttributes = 7;   //肉鸽系统: 角色属性强化加成 attrId:initValue:extraRatio\n}\n\nmessage RogueRecord {\n    int64 uin                   = 1;\n    int32 themeId               = 2;    //主题 id\n    int32 level                 = 3;    //主题等级\n    int32 difficultyLevel       = 4;    //难度等级\n    int32 layerIndex            = 5;    //到达层数\n    int32 chapterId             = 6;    //最后章节 id\n    int32 lastNodeId            = 7;    //最后到达的节点 id\n    int32 score                 = 8;    //综合评分\n    repeated RogueCardInfo cardInfos = 9;   //招募的角色\n    repeated int32 treasureIds  = 10;    //获得的宝物\n    repeated int32 holyIds      = 11;    //获得的圣物\n    int64 startTime             = 12;   //开局时间\n    int64 endTime               = 13;   //结束时间\n    map<int32, int32> stats     = 14;   //统计信息 enum ROGUE_STAT -> value\n    bool allPass                = 15;   //是否全部通关\n    int32 endingId              = 16;   //触发的结局\n    int32 totalTreasurePic      = 17;   //累计解锁的宝物图鉴数量\n}\n\n//game.actor_rogue_record 挑战记录\nmessage RogueTopScoreRecord {\n    int64 uin       = 1;\n    int32 themeId   = 2;    //主题 id\n    int32 score     = 3;\n    bytes recordRaw = 4;    //RogueRecord\n}\n\n//角色穿戴的徽章\nmessage RogueCardBadge {\n    int32 cardId = 1;\n    repeated BadgeInfo badges = 2;\n}\n\n//请求获取肉鸽信息\nmessage GetRogueInfoReq {\n}\n\nmessage GetRogueInfoRsp {\n    RogueTheme themeInfo           = 1; //主题信息\n    repeated RogueTrend trendInfos = 2; //任务动态\n    int32 themeUnlockLevel         = 3; //主题等级解锁进度\n    int32 initialRecruitCount      = 4; //开局招募角色数量\n    int32 initialTreasureCount     = 5; //开局选择宝物的数量\n    repeated CardInfo allCards     = 6; //可供招募的所有角色\n    repeated RogueCardBadge cardBadges = 7; //可供招募的所有角色的徽章信息\n}\n\n//请求开局\nmessage StartRogueGameReq {\n    int32 difficultyLevel   = 1;    //选择的难度等级\n}\n\nmessage StartRogueGameRsp {\n    RogueTheme themeInfo                = 1;    //主题信息\n    RogueChapter chapterInfo            = 2;    //章节信息\n    repeated ItemTuple rewards          = 4;    //开局奖励\n}\n\n//开局选择宝物\nmessage ChooseRogueInitialTreasureReq {\n    repeated int32 treasureIds = 1;\n}\n\nmessage ChooseRogueInitialTreasureRsp {\n    RogueTheme themeInfo        = 1;    //主题信息\n    repeated ItemTuple rewards  = 2;    //开局宝物触发的奖励\n}\n\n//开局招募角色\nmessage RecruitRogueInitialCardReq {\n    repeated int32 cardIds  = 1;    //开局招募的角色\n}\n\nmessage RecruitRogueInitialCardRsp {\n    RogueTheme themeInfo                = 1;    //主题信息\n    RogueChapter chapterInfo            = 2;    //章节信息\n    repeated RogueCardInfo cardInfos    = 3;    //角色信息\n}\n\n//请求获取肉鸽状态: 章节信息、招募的角色数据, 点击继续探索、或者完成一个节点后请求一下\nmessage GetRogueStateInfoReq {\n}\n\nmessage GetRogueStateInfoRsp {\n    RogueTheme themeInfo                = 1;    //主题信息\n    RogueChapter chapterInfo            = 2;    //章节信息\n    repeated RogueCardInfo cardInfos    = 3;    //角色信息\n}\n\n//请求进入节点\nmessage EnterRogueNodeReq {\n    int32 nodeId = 1;\n}\n\nmessage EnterRogueNodeRsp {\n    RogueChapter chapterInfo   = 1;    //章节信息\n    repeated ItemTuple rewards = 2;    //进入节点的奖励\n}\n\n//请求升级角色属性\nmessage EnhanceRogueCardAttribReq {\n    int32 cardId     = 1;\n    int32 attribId   = 2; //enum ATTR_ID\n}\n\nmessage EnhanceRogueCardAttribRsp {\n    RogueCardInfo cardInfo = 1;\n    RogueTheme themeInfo   = 2;\n}\n\n//请求激活天赋\nmessage ActivateRogueTalentReq {\n    int32 talendId = 1;\n}\n\nmessage ActivateRogueTalentRsp {\n    RogueTheme themeInfo = 1;   //更新主题数据\n}\n\n//请求购买商店节点的宝物\nmessage BuyRogueNodeShopTreasureReq {\n    int32 itemId = 1;\n}\n\nmessage BuyRogueNodeShopTreasureRsp {\n    RogueTheme themeInfo     = 1;\n    RogueChapter chapterInfo = 2;    //购买后更新数据\n    repeated ItemTuple rewards = 3;  //奖励: 用于展示\n    int32 gainTreasureId       = 4;         //获得的宝物\n    repeated int32 unlockHolyIds = 5;       //解锁的圣物\n}\n\n//请求刷新商店节点的物品\nmessage RefreshRogueNodeShopReq {\n}\n\nmessage RefreshRogueNodeShopRsp {\n    RogueChapter chapterInfo = 1;\n}\n\n//请求领取节点奖励\nmessage FetchRogueNodeRewardReq {\n    int32 rewardId = 1;\n    string param   = 2;     //招募奖励: 传招募的角色 cardId, 复活奖励: 传复活角色的 cardId 列表, cardId1|cardId2\n}\n\nmessage FetchRogueNodeRewardRsp {\n    RogueTheme themeInfo     = 1;\n    RogueChapter chapterInfo = 2;           //更新章节数据\n    repeated RogueCardInfo cardInfos = 3;   //更新角色\n    repeated ItemTuple rewards = 4;         //奖励: 用于展示\n    int32 gainTreasureId       = 5;         //获得的宝物\n    repeated int32 unlockHolyIds = 6;       //解锁的圣物\n    int32 rewardId               = 7;       //奖励选项 id\n}\n\n//请求离开节点\nmessage ExitRogueNodeReq {\n    int32 nodeId = 1;\n}\n\nmessage ExitRogueNodeRsp {\n    RogueChapter chapterInfo   = 1;    //章节信息\n    repeated ItemTuple rewards = 2;    //退出当前层最后节点后,进入下一层的奖励\n    RogueSettleInfo settleInfo = 3;    //结算信息\n    int32 extraGainTreasureId  = 4;    //退出节点时额外获得的宝物(宝物效果的额外奖励)\n}\n\n//结算信息\nmessage RogueSettleInfo {\n    RogueTheme themeInfo = 1;\n    RogueRecord record   = 2;\n    repeated ItemTuple rewards = 3;     //结算奖励: 天赋点\n    int32 gainThemeExp   = 4;           //获得的主题经验\n    int32 endingId       = 5;           //触发的结局\n}\n\n//请求放弃本局挑战\nmessage QuitRogueGameReq {\n}\n\nmessage QuitRogueGameRsp {\n    RogueSettleInfo settleInfo = 1;\n}\n\n//请求获取新图鉴状态\nmessage GetRoguePicNewStateReq {\n}\n\nmessage GetRoguePicNewStateRsp {\n    repeated int32 newTreasureIds = 1;  //显示 new 标记的宝物\n    repeated int32 newEventIds    = 2;  //显示 new 标记的事件\n    repeated int32 newEndingIds   = 3;  //显示 new 标记的结局\n    repeated int32 newHolyIds     = 4;  //显示 new 标记的圣物\n}\n\n//清除图鉴的 new 状态\nmessage ClearRoguePicNewStateReq {\n    int32 roguePicType = 1; //enum ROGUE_PIC_TYPE\n}\n\nmessage ClearRoguePicNewStateRsp {\n}\n\n//请求获取所有图鉴数据\nmessage GetRogueAllPicReq {\n    int32 roguePicType = 1; //enum ROGUE_PIC_TYPE\n}\n\nmessage GetRogueAllPicRsp {\n    RoguePicInfo picInfo = 1;\n}\n\n//请求获取任务\nmessage GetRogueTrendsReq {\n}\n\nmessage GetRogueTrendsRsp {\n    repeated RogueTrend trendInfos = 1;\n    int32 groupId = 2;\n}\n\n//战斗节点结果数据\nmessage RogueNodeBattleResult {\n    bool gameSettle             = 1;    //本局是否结算\n    RogueSettleInfo settleInfo  = 2;    //本局结算信息  如果 gameSettle = true, 该值有效\n    RogueChapter chapterInfo    = 3;    //章节信息\n    repeated RogueCardInfo cardInfos = 4;   //更新角色数据\n    repeated ItemTuple rewards  = 5;    //宝物效果触发的奖励\n}\n\n//请求领取主题等级奖励\nmessage FetchRogueThemeLevelRewardReq {\n    int32 rewardLevel = 1;\n}\n\nmessage FetchRogueThemeLevelRewardRsp {\n    RogueTheme themeInfo        = 1;\n    repeated ItemTuple rewards  = 2;  //奖励: 用于展示\n}\n\n//获取最高评分的记录\nmessage GetRogueTopScoreRecordReq {\n}\n\nmessage GetRogueTopScoreRecordRsp {\n    RogueRecord record   = 1;\n}\n\n//领取动态的任务奖励\nmessage FetchRogueTrendTaskRewardReq {\n    int32 trendId = 1;\n    int32 taskId  = 2;\n}\n\nmessage FetchRogueTrendTaskRewardRsp {\n    RogueTrend trendInfo        = 1;  //更新动态\n    repeated DropTuple rewards  = 2;  //奖励: 用于展示\n}\n\n//完成事件节点的剧情\nmessage FinishRogueEventStoryReq {\n    int32 eventId = 1;\n}\n\nmessage FinishRogueEventStoryRsp {\n}\n\n//完成事件节点的关键剧情点\nmessage FinishRogueEventKeyStoryReq {\n    int32 eventId = 1;\n    int32 storyId = 2;\n}\n\nmessage FinishRogueEventKeyStoryRsp {\n    RogueTheme themeInfo     = 1;\n    RogueChapter chapterInfo = 2;           //更新章节数据\n    repeated RogueCardInfo cardInfos = 3;   //更新角色\n    repeated ItemTuple rewards = 4;         //奖励: 用于展示\n    int32 gainTreasureId       = 5;         //获得的宝物\n    repeated int32 unlockHolyIds = 6;       //解锁的圣物\n}\n\n//事件节点选择某个战斗选项\nmessage ChooseRogueEventBattleStoryReq {\n    int32 eventId = 1;\n    int32 storyId = 2;\n    int32 preStoryId = 3;   //前一个 storyId\n}\n\nmessage ChooseRogueEventBattleStoryRsp {\n    RogueChapter chapterInfo = 1;           //更新章节数据\n}\n\n//肉鸽角色信息更新\nmessage RogueCardUpdateNotify {\n    repeated RogueCardInfo cardInfos = 1;\n}\n\n//扫荡 快速探索\nmessage SweepRogueReq {\n    int32 themeId = 1;\n}\n\nmessage SweepRogueRsp {\n    RogueTheme themeInfo    = 1;    //主题信息\n    int32 gainTalent        = 2;    //获得的天赋点\n    int32 gainExp           = 3;    //获得经验\n}\n\n\n\n//副本类型\nenum SCENE_TYPE {\n    SST_NONE            = 0;\n    MAIN_LINE           = 1;    //主线剧情副本\n    CLIMB_TOWER         = 2;    //爬塔\n    ARENA               = 5;    //竞技场\n    EXPEDITION          = 6;    //远征\n    BOSS_CHALLENGE      = 7;    //BOSS挑战\n    BUFF_STAGE          = 8;    //buff stage\n    ROGUE               = 9;    //肉鸽\n    LIMIT_CHALLENGE     = 10;   //限时挑战\n    DAILY_COIN          = 11;   //日常本-金币\n    DAILY_ROLE_EXP      = 12;   //日常本-角色经验\n    DAILY_SKILL_BOOK    = 13;   //日常本-技能书\n    DAILY_QUALITY_UP    = 14;   //日常本-突破\n    DAILY_MATERIAL      = 15;   //日常本-通用材料\n    DAILY_BADGE_EXP     = 16;   //日常本-徽章经验\n    ACTIVITY_NORAML     = 21;   //活动本普通\n    ACTIVITY_CREAM      = 22;   //活动本材料\n    ACTIVITY_BOSS       = 23;   //活动本boss\n    MANOR               = 31;   //探险地图\n    GUILD_WAR           = 32;   //公会战\n    BOSS_WATER          = 41;   //boss挑战-水\n    BOSS_FIRE           = 42;   //boss挑战-火\n    BOSS_WOOD           = 43;   //boss挑战-木\n    BOSS_LIGHT          = 44;   //boss挑战-光\n    BOSS_DARK           = 45;   //boss挑战-暗\n    GUILD_PRACTICE_NONE = 51;   //探险队演练-无属性\n    GUILD_PRACTICE_WATER= 52;   //探险队演练-水\n    GUILD_PRACTICE_FIRE = 53;   //探险队演练-火\n    GUILD_PRACTICE_WOOD = 54;   //探险队演练-木\n    GUILD_PRACTICE_LIGHT= 55;   //探险队演练-光\n    GUILD_PRACTICE_DARK = 56;   //探险队演练-暗\n    MANOR_WATER         = 61;   //深渊-水\n    MANOR_FIR           = 62;   //深渊-火\n    MANOR_WOOD          = 63;   //深渊-木\n    SEAL_HOOK           = 71;   //印章挂机\n    SEAL_QUALITY_UP     = 72;   //印章突破\n    FRIEND_FIGHT        = 81;   //好友切磋\n    PREPARE_STORE_COMMON        = 10000;    //战斗阵容通用存储类型\n}\n\n\n//关卡类型\nenum STAGE_TYPE {\n    ST_NONE             = 0;\n    DISPOSABLE          = 1;    //一次性\n    REPEAT              = 2;    //重复\n    PLOT                = 3;    //剧情\n    BOX                 = 4;    //宝箱\n    EXPEDITION_MONSTER  = 5;    //远征怪物\n    EXPEDITION_MIRROR   = 6;    //远征镜像\n}\n//章节开启条件类型\nenum CHAPTER_CONDITION_TYPE {\n    CCT_NONE    = 0;\n    ROLE_LEVEL  = 100;\n    PASS_STAGE  = 200;\n    SEAL_HOOK_LEVEL = 400;    //大刻印挂机玩法等级\n}\n\n//获取副本信息,当前开启到哪个章节\nmessage GetSceneInfoReq {\n    repeated int32 sceneTypes = 1;         //enum SCENE_TYPE\n}\n\n//副本信息\nmessage SceneInfo {\n    int32 sceneType                 = 1;   //enum SCENE_TYPE\n    int32 currentChapter            = 2;   //当前解锁到的章节 该章节之前的章节同样是解锁状态\n    bool unlocked                   = 3;   //是否已达到副本解锁条件\n    bool inOpenTime                 = 4;   //是否在副本开放期间\n    int32 totalPassed               = 5;   //总共通过的关卡数量\n    int32 currentStage              = 6;   //当前关卡   为 0 表示 currentChapter 当前章节全部通关, 但是可能由于没有后续章节,或者未达到下一个章节的解锁条件,就没有切换到下一个章节第一关\n    int32 rewardedChapter           = 7;   //已领取章节奖励的进度 该章节及之前的章节奖励已领取\n    bool currentStageOpen           = 8;   //当前关卡是否已开启\n    SceneChapter curChapterInfo     = 9;   //currentChapter 的章节信息\n    int64 sceneOpenStamp            = 10;  //副本开启时间戳\n    int64 sceneCloseStamp           = 11;  //副本关闭时间戳\n    repeated int32 rewardedStages   = 12;  //已手动领取奖励的关卡\n    int32 maxStageId                = 13;   //历史通过最大关卡, 目前副本类型 61-63 记录该值\n}\n\nmessage GetSceneInfoRsp {\n    repeated SceneInfo sceneInfos   = 1;\n}\n\n//获取当前章节已通关的关卡信息\nmessage GetChapterStageReq {\n    repeated int32 chapterIds = 1;\n}\n\n//副本的一个章节信息\nmessage SceneChapter {\n    int32 chapterId             = 1;\n    repeated StageInfo stages   = 2;\n    int32 stageOpenProgress     = 3;    //当前章节已解锁关卡进度\n}\n\nmessage GetChapterStageRsp {\n    repeated SceneChapter sceneChapters = 1;\n}\n\n//请求已开启的关卡\nmessage GetOpenStagesReq {\n    repeated int32 stageIds = 1;\n}\n\nmessage GetOpenStagesRsp {\n    repeated int32 openStageIds = 1;    //返回已开启的关卡id\n}\n\nenum SWEEP_TYPE {\n    SWEEP_TYPE_NONE     = 0;\n    BY_COUNT            = 1;    //按次数扫荡\n    BY_DEMAND           = 2;    //按需求扫荡\n}\n\n//获取战斗数据\nmessage GetChallengeRecordReq {\n    int32 stageId = 1;\n}\n\nmessage GetChallengeRecordRsp {\n    int32 stageId           = 1;\n    repeated int32 cardIds  = 2;    //阵容\n    bytes opRecord          = 3;    //操作记录\n}\n\n//领取副本章节奖励\nmessage FetchSceneChapterRewardReq {\n    int32 sceneType         = 1;    //副本类型\n    int32 chapterId         = 2;    //章节 id\n}\n\nmessage FetchSceneChapterRewardRsp {\n    int32 sceneType             = 1;    //副本类型\n    int32 rewardedChapter       = 2;    //已领取章节奖励的进度\n    repeated ItemTuple rewards  = 3;    //奖励\n}\n\n//手动领取关卡奖励\nmessage FetchSceneStageRewardReq {\n    int32 stageId   = 1;    //关卡 id\n    repeated int32 stageIdLst   = 2;\n}\n\nmessage FetchSceneStageRewardRsp {\n    int32 stageId                 = 1;    //关卡 id\n    repeated ItemTuple rewards    = 2;    //奖励\n    repeated int32 rewardedStages = 3;    //已领取奖励的关卡\n}\n\n//扫荡关卡\nmessage SweepStageReq {\n    int32 stageId   = 1;    //关卡 id\n}\n\nmessage SweepStageRsp {\n    int32 stageId   = 1;\n    repeated ItemTuple rewards  = 2;    //奖励\n    int32 level     = 3;   //团队等级\n    int32 exp       = 4;   //团队经验\n    repeated ItemTuple activityDrops = 5;   //活动掉落\n}\n\n//\nmessage BuffStageGetInfoReq {\n\n}\n\nmessage BuffStageGetInfoRsp {\n    int32 chapterId             = 1;\n    int64 endStamp              = 2;\n    repeated BuffStage stages   = 3;\n    int32 chapterTarget         = 4;\n    map<int32,int32>    buffList= 5;\n    repeated int32 openStages   = 6;\n    map<int32,int32>    highScore = 7;\n}\n\nmessage BuffStageRewardReq {\n    int32 rewardStage = 1;\n    int32 rewardId    = 2;\n}\n\nmessage BuffStageRewardRsp {\n    repeated DropTuple rewards  = 1;\n    BuffStage stage             = 2;\n    int32 chapterTarget         = 3;\n}\n\n\n//获取倍率掉落活动信息\nmessage GetMultiDropActivityReq {\n}\n\n//倍率掉落副本组类型\nenum MULTI_DROP_SCENE_GROUP {\n    MDSG_NONE   = 0;\n    MDSG_DAILY  = 1;    //日常本(物资补给): 11-16\n    MDSG_BOSS   = 2;    //徽章本(领主巢穴): 41-45\n}\n\nmessage MultiDropActivityInfo {\n    int32 activityId     = 1;   //当前生效的活动 id, 0:活动未生效\n    int32 sceneGroupType = 2;   //enum MULTI_DROP_SCENE_GROUP\n    int64 startStamp     = 3;   //活动开始时间\n    int64 endStamp       = 4;   //活动结束时间\n    int32 leftCnt        = 5;   //剩余次数\n    int32 showMulti      = 6;   //展示的倍率\n}\n\nmessage GetMultiDropActivityRsp {\n    repeated MultiDropActivityInfo infos = 1;\n}\n\nmessage SceneRankMember {\n    int64 uin       = 1;\n    int32 level     = 2;    //等级\n    int32 faceId    = 3;\n    ActorHead actorHead = 4;   //头像信息\n    string name         = 5;    //名字\n    string guildName    = 6;    //所在公会名字\n    int32 stageId       = 7;    //关卡进度\n    int32 rank          = 8;    //排名\n}\n\nmessage GetSceneRankReq {\n    int32 sceneType  = 1;    //MAIN_LINE CLIMB_TOWER\n    int32 startIndex = 2;    //用于分批请求 传当前已拉取到本地的数量 第一页传 0\n}\n\nmessage GetSceneRankRsp {\n    int32 sceneType  = 1;\n    int32 startIndex = 2;\n\n    int32 myRank     = 3;    //自己的排名    startIndex = 0 才有该值，超过 300 显示 rankRatio， 0: 未上榜\n    int32 rankRatio  = 4;    //自己排名比例   startIndex = 0 才有该值\n\n    repeated SceneRankMember members = 5;   //startIndex = 0 时候才有前三名\n    int32 totalRank  = 6;    //排行榜显示的总数量\n}\n\n\n\n\nmessage GetFeatureScheduleReq {\n}\n\nmessage GetFeatureScheduleRsp {\n    FeatureGuildWarInfo guildWar            = 1;    //强敌来袭 公会战\n    GetLimitChallengeInfoRsp limitChallenge = 2;    //灾兆断层 限时爬塔\n    BuffStageGetInfoRsp buffStage           = 3;    //旧日遗迹\n    GetCycleTaskInfoRsp rogueWeekTask       = 4;    //寻幽探秘 肉鸽周任务\n    GetManorInfoRsp manor                   = 5;    //地图物资\n    GetDispatchInfoRsp dispatch             = 6;    //深渊先遣队\n    FeatureManorSceneInfo manorScene        = 7;    //魔物猎场 深渊水火木\n    GetCommonTaskInfoRsp dailyTask          = 8;    //每日任务\n    ArenaGetAllRsp arena                    = 9;    //荣耀之地 竞技场\n    FeatureStageActivityInfo stageActInfo   = 10;   //角色活动\n    GetBossInfoRsp bossInfo                 = 11;   //幻象境地\n    GetSupplyInfoRsp supplyInfo             = 12;   //补给\n    SealBigHookInfo sealBigHookInfo         = 13;   //大刻印挂机\n\n}\n\n//公会战\nmessage FeatureGuildWarInfo {\n    GuildWarSchedule schedule = 1;    //公会战赛程状态\n    int32 fightCount          = 2;    //已挑战次数\n    int32 rank                = 3;    //自己公会排名\n    int32 rankRatio           = 4;    //自己公会排名比例\n}\n\nmessage FeatureManorSceneInfo {\n    repeated SceneInfo sceneInfos = 1;\n}\n\nmessage FeatureStageActivityInfo {\n    repeated ActivityStage stageAct = 1;\n}\n\n\n\n//印章孔位\nenum SEAL_POS {\n    SP_NONE = 0;\n    SP_ATK  = 1;    //攻击孔位\n    SP_DEF  = 2;    //防御孔位\n    SP_HP   = 3;    //生命孔位\n}\n\n\n//印章佩戴信息    game.actor_seal_wear\nmessage SealWearInfo {\n    int64 uin = 1;\n    int32 job = 2;  //职业类型\n    repeated int32 sealIds = 3; //已佩戴的印章 Id\n    int32 bigSealLevel     = 4; //大印章等级\n    int32 bigSealQuality   = 5; //大印章突破等级\n    int32 bigSealAddUpLevel= 6; //大印章增幅等级\n}\n\n//刻印挂机\nmessage SealBigHookInfo {\n    int64 uin       = 1;\n    int32 hookLevel = 2;    //挂机等级\n    int32 hookExp   = 3;    //挂机经验\n    int64 produceStartTime = 4;  //开始产出时间\n    int32 fastCollectCnt   = 5;  //快速采集剩余次数\n    repeated ItemTuple hookRewards = 6; //挂机产出的奖励\n    int64 resetStamp     = 7;   //重置时间\n\n    int32 passedStage    = 8;   //已通过关卡\n    int32 currentChapter = 9;  //当前章节\n    int32 currentStage   = 10;  //为 0 表示当前章节已全部通关\n    int32 round          = 11;  //当前正在挑战关卡轮次 (1: 表示已挑战过一轮)\n    repeated int32 usedCards = 12;  //已使用的角色\n    int64 hookLevelupTime = 13; //挂机升级时间\n    int64 lastProduceTime = 14; //上次产出时间\n}\n\n//获取所有印章穿戴信息\nmessage GetSealWearInfoReq {\n}\n\nmessage GetSealWearInfoRsp {\n    repeated SealWearInfo wearInfos = 1;\n}\n\n//穿戴印章\nmessage WearSealReq {\n    int32 job = 1;  //职业类型\n    repeated int32 sealIds = 2;\n}\n\nmessage WearSealRsp {\n    SealWearInfo wearInfo = 1;\n}\n\n//取下印章\nmessage TakeoffSealReq {\n    int32 job    = 1;  //职业类型\n    int32 sealId = 2;  //0: 全部取下\n}\n\nmessage TakeoffSealRsp {\n    SealWearInfo wearInfo = 1;\n}\n\n//合成徽章\nmessage CompositeSealReq {\n    int32 sealId  = 1;\n    int32 count   = 2;\n    bool useLucky = 3;  //是否使用幸运符\n}\n\nmessage CompositeSealRsp {\n    repeated ItemTuple gainItems = 1;\n}\n\n//大印章升级\nmessage SealBigLevelupReq {\n    int32 job     = 1;  //职业类型\n    int32 toLevel = 2;  //升级到该等级\n}\n\nmessage SealBigLevelupRsp {\n    SealWearInfo info = 1;\n}\n\n//大印章突破\nmessage SealBigQualityUpReq {\n    int32 job = 1;  //职业类型\n}\n\nmessage SealBigQualityUpRsp {\n    SealWearInfo info = 1;\n}\n\n//大印章增幅升级\nmessage SealBigAddUpReq {\n    int32 job = 1;  //职业类型\n}\n\nmessage SealBigAddUpRsp {\n    SealWearInfo info = 1;\n}\n\n//获取大印章挂机信息\nmessage GetSealBigHookInfoReq {\n\n}\n\nmessage GetSealBigHookInfoRsp {\n    SealBigHookInfo info = 1;\n}\n\n//采集挂机奖励\nmessage FetchSealBigHookRewardReq {\n    bool fastCollect   = 1;   //是否快速采集\n    int32 consumeType = 2;    //快速采集消耗品类型 1: 代币   2: 欧泊\n}\n\nmessage FetchSealBigHookRewardRsp {\n    SealBigHookInfo info       = 1;\n    repeated ItemTuple rewards = 2;\n}\n\n//放弃印章挂机本轮挑战\nmessage QuitSealBigHookChallengeReq {\n}\n\nmessage QuitSealBigHookChallengeRsp {\n    SealBigHookInfo info = 1;\n}\n\n\n\nenum SHOP_TYPE {\n    SHOP_TYPE_NONE = 0;\n    ST_BLUE = 1;    //蓝票商店\n    ST_RED  = 2;    //红票商店\n    ST_MANOR_PERIOD = 3;    //大地图周期商店\n    ST_MANOR_NORMAL = 4;    //大地图常规商店\n    ST_MANOR_SEAL   = 5;    //大地图刻印商店\n}\nmessage ShopGridInfo {\n    int32 gridId            = 1;    //格子ID\n    int32 goodsId           = 2;    //商品ID(通过配置表对应商品内容，购买消耗等)\n    int32 boughtNum         = 3;    //商品购买次数\n    int64 nextRefreshTime   = 4;    //下次刷新时间\n    bool unlocked           = 5;    //是否已解锁\n    int64 startTime         = 6;    //格子开始时间\n    int64 endTime           = 7;    //格子结束时间\n    int64 unlockTime        = 8;    //解锁时间戳\n}\nmessage ShopShowInfo {\n    int64 uin                       = 1;\n    int32 typeId                    = 2;    //类型ID\n    int32 refreshNum                = 3;    //刷新次数\n    int64 nextRefreshTime           = 4;    //下次刷新时间\n    bool isOpen                     = 5;    //是否开启\n    repeated ShopGridInfo  goods    = 6;    //商店商品\n    int32 manorFreeCount            = 7;    //深渊商店领取次数\n}\nmessage FashionAddNotify {\n    repeated int32 fashions = 2;\n}\n//请求商店信息\nmessage GetShopInfoReq {\n    repeated int32 types        = 1;\n}\nmessage GetShopInfoRsp {\n    repeated ShopShowInfo shopList  = 1;\n}\n\n//购买商品\nmessage BuyShopGoodsReq {\n    int32 gridId    = 1;\n    int32   num     = 2;\n}\n\nmessage BuyShopGoodsRsp {\n    repeated ItemTuple goods    = 1;    //购买的商品\n    ShopShowInfo shop           = 2;\n}\n\n//刷新商品\nmessage RefreshShopGoodsReq {\n    int32 shopType    = 1;\n}\n\nmessage RefreshShopGoodsRsp {\n    ShopShowInfo shop   = 1;\n}\n//获取礼包信息\nmessage GetGiftInfoReq {\n    \n}\n\nmessage GetGiftInfoRsp {\n    repeated GiftItem gifts       = 1;    //已经购买的礼包\n    repeated int32 canRewards     = 2;      //能够领奖的阶段\n}\n//购买礼包\nmessage BuyGiftReq {\n    int32 giftId = 1;\n}\n\nmessage BuyGiftRsp {\n    repeated GiftItem gifts       = 1;    //已经购买的礼包\n    repeated DropTuple goods      = 2;    //购买获得的物品\n    repeated ItemTuple rewards    = 3;      //配置的奖励\n    repeated int32 canRewards     = 4;      //能够领奖的阶段\n}\n//领取礼包\nmessage GetGiftRewardReq {\n    int32 gitfId    = 1;\n    int32 stepId    = 2;\n}\n\nmessage GetGiftRewardRsp {\n    repeated DropTuple goods        = 1;        //领取的物品\n    repeated GiftItem gifts         = 2;        //已经购买的礼包\n    repeated int32 canRewards       = 3;      //能够领奖的阶段\n}\nmessage BuyInfo {\n    int32 gridId    = 1;\n    int32   num     = 2;\n}\n//购买刻印\nmessage BuySealShopGoodsReq {\n    repeated BuyInfo bought = 1;\n}\n\nmessage BuySealShopGoodsRsp {\n    repeated ItemTuple goods    = 1;    //购买的商品\n    ShopShowInfo shop           = 2;\n}\n\n\n\nmessage SysAddItemReq {\n    int64 uin   = 1;\n    int32 logId = 2;\n    repeated ItemTuple items = 3;\n}\n\nmessage SysAddItemRsp {\n\n}\n\nmessage GetResVersionReq {\n\n}\n\nmessage GetResVersionRsp {\n    int64 iosMaxResId               = 1;    //ios资源库中最大resId\n    int64 iosMaxVisibleResId        = 2;    //ios对外可见最大resId\n    int64 androidMaxResId           = 3;    //android资源库中最大resId\n    int64 androidMaxVisibleResId    = 4;    //android对外可见最大resId\n}\n\nmessage ResMeta {\n    int64 resId = 1;\n    string path = 2;\n    string md5  = 3;\n    int32 size  = 4;\n}\n\nmessage ResUpdateList {\n    string newestCliVersion     = 1;    //当前客户端最新版本号\n    string minCliVersion        = 2;    //客户端最低版本号\n    string downloadUrl          = 3;    //ios客户端下载地址\n    repeated ResMeta updateList = 4;    //资源列表\n}\n\nmessage SysActorInfoUpdatedReq {\n    ActorInfo actorInfo = 1;\n}\n\nmessage SysActorInfoUpdatedRsp {\n}\n\n//充值订单发货\nmessage SysRechargeOrderDeliveryReq {\n    string order = 1;\n}\n\nmessage SysPayOrderDeliveryRsp {\n}\n\n//充值订单退款\nmessage SysRechargeOrderRefundReq {\n    string orderId = 1;\n}\n\nmessage SysRechargeOrderRefundRsp {\n}\n\n//增加公会经验\nmessage IncrGuildExpReq {\n    int32 exp = 1;\n}\n\n//将玩家从 gamesvr 踢下线(从内存移除)\nmessage KickOffUserFromGameReq {\n    int64 uin = 1;\n}\n\nmessage KickOffUserFromGameRsp {\n}\n\n//更新公会成员名字\nmessage SysUpdateGuildMemberNameReq {\n    int64 uin   = 1;\n    string name = 2;\n}\n\n//获取公会战进度\nmessage SysGetGuildWarProgressReq {\n}\n\nmessage SysGetGuildWarProgressRsp {\n    GuildWarProgress progress = 1;\n}\n\n//公会战战斗结算\nmessage SysGuildWarBattleSettleReq {\n    int32 stageId        = 1;\n    bool win             = 2;  //是否胜利\n    int32 battleTotalTime= 3;  //战斗完整时间\n    int32 battleLeftTime = 4;  //战斗剩余时间\n    int64 damageHp       = 5;  //伤害值\n    repeated BattleUnitInit bossInitialUnits  = 6;  //进战斗时 boss 初始状态\n    repeated ObjectState bossStates           = 7;  //战斗结束后 boss 最终状态\n    repeated int64 assistCardUidLst           = 8;  //使用的助战角色 cardUid\n    int32 round          = 9;   //当前轮次\n}\n\nmessage SysGuildWarBattleSettleRsp {\n    bool bossDeadBefore = 1;    //结算之前 boss 是否已阵亡\n    int64 finalDamageHp = 2;    //最终结算伤害\n    int32 score         = 3;    //获得积分\n    int32 compensateTime= 4;    //补偿时间 0:不补偿\n    bool bossDead       = 5;    //本次结算后 boss 是否阵亡\n    int64 totalScore    = 6;    //个人当前积分\n    int64 guildScore    = 7;    //公会积分\n    int64 BossLeftHp    = 8;    //boss当前剩余总血量\n}\n\n//给公会添加头像 id\nmessage SysAddGuildHeadReq {\n    repeated int32 headIds = 1;\n}\n\nmessage SysAddGuildHeadRsp {\n}\n\n//检查是否拥有 emoji\nmessage SysCheckOwnEmojiReq {\n    int32 emojiId = 1;\n}\n\nmessage SysCheckOwnEmojiRsp {\n    bool own = 1;\n}\n\n\n\n\n//任务事件类型\nenum TASK_EVENT {\n    TASK_EVENT_NONE         = 0;\n}\n\n//任务数据记录方式\nenum TASK_RECORD {\n    TASK_RECORD_NONE        = 0;\n    TR_SET_GE               = 1;    //设置值 >=\n    TR_SET_LE               = 2;    //设置值 <=\n    TR_ADD                  = 3;    //累加值\n}\n\nmessage CommonTask {\n    int32 index     = 1;\n    TaskInfo task   = 2;\n}\n//获取常规任务信息\nmessage GetCommonTaskInfoReq {\n    int64 refreshStamp  = 1;\n}\nmessage GetCommonTaskInfoRsp {\n    repeated CommonTask taskList    = 1;    //任务列表 \n    repeated int32 dailyRewards     = 2;    //天目标已领奖阶段    \n    repeated int32 totalRewards     = 3;    //总目标已领奖阶段\n    int64 refreshStamp              = 4;\n}\n//领取常规任务奖励\nmessage CommonTaskRewardReq {\n    int32 rewardType    = 1;        //0：任务奖励 3：天目标 2：总目标 \n    int32 rewardId      = 2;\n}\n\nmessage CommonTaskRewardRsp {\n    repeated DropTuple goods        = 1;    //领取的奖励\n    repeated int32 dailyRewards     = 2;    //天目标已领奖阶段\n    repeated int32 totalRewards     = 3;    //总目标已领奖阶段\n    repeated CommonTask taskList    = 4;    //任务列表 \n    int64 refreshStamp              = 5;    \n}\n\n//替换常规任务\nmessage CommonTaskReplaceReq {\n    int32 index         = 1;\n    int64 refreshStamp  = 2;\n}\nmessage CommonTaskReplaceRsp {\n    repeated CommonTask taskList    = 1;    //任务列表  \n    int64 refreshStamp              = 2;\n}\n\n//获取任务更新时间\nmessage GetTaskRefreshStampReq {\n    \n}\n\nmessage GetTaskRefreshStampRsp {\n    map<int32,int64>    refreshStamp  = 1; \n}\n//获取周期任务\nmessage GetCycleTaskInfoReq {\n}\nmessage GetCycleTaskInfoRsp {\n    repeated TaskInfo taskList      = 1;    //任务列表 \n    repeated int32 weeklyRewards    = 2;    //周目标已领奖阶段   \n    int64 refreshStamp              = 3;    //刷新时间点\n}\n\n//周期任务领奖\nmessage CycleTaskRewardReq {\n    int32 rewardType    = 1;    //0:领取任务 4:领取阶段奖励\n    int32 rewardId      = 2;    //0:任务ID 4：阶段Id\n}\n\nmessage CycleTaskRewardRsp {\n    repeated DropTuple goods        = 1;    //领取的奖励\n    repeated int32 weeklyRewards    = 2;    //已领奖阶段   \n}\n\n\n\n\n//gm 操作模块\nenum GM_OP_MODULE {\n    GOM_NONE            = 0;\n    GOM_IMAGE           = 1;    //图片操作\n    GOM_NOTICE          = 2;    //公告操作\n    GOM_MAIL            = 3;    //邮件操作\n    GOM_RECOMMEND_IMG   = 4;    //推荐图操作\n    GOM_GIFT_PACKAGE    = 5;    //礼包操作\n    GOM_FASHION         = 6;    //时装操作\n    GOM_ACTIVITY        = 7;    //活动操作\n    GOM_PLAYER          = 8;    //玩家操作\n    GOM_WHITE_LIST      = 9;    //白名单操作\n    GOM_CLI_RES_RELEASE = 10;   //客户端资源发布\n    GOM_SVR_STATE       = 11;   //服务器状态操作\n    GOM_CREATE_USER_LIMIT = 12; //创建上限操作\n    GOM_GUILD           = 13;   //探险队操作\n    GOM_EXCHANGE_CODE   = 14;   //兑换码\n    GOM_SHOP_LABEL      = 15;   //商店页签\n    GOM_SYNC_CONFIG     = 16;   //同步配置\n}\n\nenum ACTIVITY_OP {\n    AO_NONE        = 0;\n    AO_MODIFY      = 1;    //修改\n    AO_OFF_SHELF   = 2;    //下架\n    AO_REMOVE      = 3;    //移除\n    AO_DELETE      = 4;    //删除\n}\n\nenum NOTICE_TYPE {\n    NT_NONE         = 0;\n    NT_SYS          = 1;    //系统公告\n    NT_ACTIVITY     = 2;    //活动公告\n    NT_LOGIN        = 3;    //登录公告\n}\n\n//推荐图商品类型\nenum RECOMMEND_IMG_PRODUCT_TYPE {\n    RIP_NONE        = 0;\n    RIP_PAY_PRODUCT = 1;    //base_pay_product\n    PIP_FASHION     = 2;    //base_fashion\n    RIP_GIFT        = 3;    //base_gift\n}\n\n//推荐图跳转类型\nenum RECOMMEND_IMG_JUMP_TYPE {\n    RJT_NONE        = 0;    //无跳转\n    RJT_SHOP        = 1;    //跳转商店\n    RJT_SHOP_BUY    = 2;    //商店购买面板\n    RJT_BUY         = 3;    //直接购买\n}\n\n//获取所有的推荐图信息\nmessage GetAllRecommendImgReq {\n    bool onlyOnShelf = 1;   //只需要拉取已上架的\n    string channel   = 2;\n}\n\nmessage GetAllRecommendImgRsp {\n    repeated OpRecommendImg infos = 1;\n}\n\n//创建推荐图\nmessage CreateRecommendImgReq {\n    OpRecommendImg info = 1;\n}\n\nmessage CreateRecommendImgRsp {\n}\n\n//操作推荐图\nmessage OperateRecommendImgReq {\n    int64 uid           = 1;\n    int32 operation     = 2;    //enum ACTIVITY_OP\n    OpRecommendImg info = 3;    //只有修改才需要传这个\n}\n\nmessage OperateRecommendImgRsp {\n}\n\n//审核推荐图\nmessage VerifyRecommendImgReq {\n    int64 uid           = 1;    //推荐图的 id\n    int32 verifyState   = 2;    //1: 通过     2: 拒绝\n}\n\nmessage VerifyRecommendImgRsp {\n}\n\n\n//获取所有礼包\nmessage GetAllGiftPackageReq {\n    bool onlyOnShelf = 1;   //只需要拉取已上架的\n}\n\nmessage GetAllGiftPackageRsp {\n    repeated OpGiftPackage infos = 1;\n}\n\n//创建礼包\nmessage CreateGiftPackageReq {\n    OpGiftPackage info = 1;\n}\n\nmessage CreateGiftPackageRsp {\n}\n\n//操作礼包\nmessage OperateGiftPackageReq {\n    int64 uid           = 1;\n    int32 operation     = 2;    //enum ACTIVITY_OP\n    OpGiftPackage info  = 3;    //只有修改才需要传这个\n}\n\nmessage OperateGiftPackageRsp {\n}\n\n//审核礼包\nmessage VerifyGiftPackageReq {\n    int64 uid           = 1;    //推荐图的 id\n    int32 verifyState   = 2;    //1: 通过     2: 拒绝\n}\n\nmessage VerifyGiftPackageRsp {\n}\n\n///////////////////////////////////////////////////////////////\n//获取所有时装\nmessage GetAllOpFashionsReq {\n    bool onlyOnShelf = 1;   //只需要拉取已上架的\n}\n\nmessage GetAllOpFashionsRsp {\n    repeated OpFashion infos = 1;\n}\n\n//创建时装\nmessage CreateFashionReq {\n    OpFashion info = 1;\n}\n\nmessage CreateFashionRsp {\n}\n\n//操作时装\nmessage OperateFashionReq {\n    int64 uid           = 1;\n    int32 operation     = 2;    //enum ACTIVITY_OP\n    OpFashion info      = 3;    //只有修改才需要传这个\n}\n\nmessage OperateFashionRsp {\n}\n\n//审核时装\nmessage VerifyFashionReq {\n    int64 uid           = 1;\n    int32 verifyState   = 2;    //1: 通过     2: 拒绝\n}\n\nmessage VerifyFashionRsp {\n}\n\n///////////////////////////////////////////////////////////////\n//获取所有活动\nmessage GetAllOpActivityReq {\n    bool onlyOnShelf = 1;   //只需要拉取已上架的\n    int32 activityType = 2; //活动类型\n}\n\nmessage GetAllOpActivityRsp {\n    repeated OpActivity infos = 1;\n}\n\n//创建活动\nmessage CreateActivityReq {\n    OpActivity info = 1;\n}\n\nmessage CreateActivityRsp {\n}\n\n//操作活动\nmessage OperateActivityReq {\n    int64 uid           = 1;\n    int32 operation     = 2;    //enum ACTIVITY_OP\n    OpActivity info     = 3;    //只有修改才需要传这个\n}\n\nmessage OperateActivityRsp {\n}\n\n//审核活动\nmessage VerifyActivityReq {\n    int64 uid           = 1;\n    int32 verifyState   = 2;    //1: 通过     2: 拒绝\n}\n\nmessage VerifyActivityRsp {\n}\n\n///////////////////////////////////////////////////////////////\n//获取所有公告\nmessage GetAllNoticesReq {\n    bool onlyOnShelf = 1;   //只需要拉取已上架的\n    string channel   = 2;\n}\n\nmessage GetAllNoticesRsp {\n    repeated OpNotice normals   = 1;\n    repeated OpNotice drafts    = 2;    //草稿箱\n}\n\n//获取某个公告的信息\nmessage GetNoticeInfoReq {\n    int64 uid           = 1;\n    string noticeSource = 2;    //normal    draft\n}\n\nmessage GetNoticeInfoRsp {\n    OpNotice info       = 1;\n}\n\n//创建公告\nmessage CreateNoticeReq {\n    OpNotice info       = 1;\n    string noticeSource = 2;    //normal    draft\n}\n\nmessage CreateNoticeRsp {\n}\n\n//公告保存草稿箱\nmessage SaveNoticeDraftReq {\n    OpNotice info       = 1;\n}\n\nmessage SaveNoticeDraftRsp {\n}\n\n//操作活动\nmessage OperateNoticeReq {\n    int64 uid           = 1;\n    int32 operation     = 2;    //enum ACTIVITY_OP\n    OpNotice info       = 3;    //只有修改才需要传这个\n    string noticeSource = 4;    //normal    draft\n}\n\nmessage OperateNoticeRsp {\n}\n\n//审核活动\nmessage VerifyNoticeReq {\n    int64 uid           = 1;\n    int32 verifyState   = 2;    //1: 通过     2: 拒绝\n}\n\nmessage VerifyNoticeRsp {\n}\n///////////////////////////////////////////////////////////////\n//获取所有邮件\nmessage GetAllSystemMailReq {\n}\n\nmessage GetAllSystemMailRsp {\n    repeated OpSystemMail normals   = 1;\n    repeated OpSystemMail drafts    = 2;    //草稿箱\n}\n\n//创建公告\nmessage CreateSystemMailReq {\n    OpSystemMail info       = 1;\n}\n\nmessage CreateSystemMailRsp {\n}\n\n//操作活动\nmessage OperateSystemMailReq {\n    int64 uid           = 1;\n    int32 operation     = 2;    //enum ACTIVITY_OP\n    OpSystemMail info       = 3;    //只有修改才需要传这个\n}\n\nmessage OperateSystemMailRsp {\n}\n\n//审核活动\nmessage VerifySystemMailReq {\n    int64 uid           = 1;\n    int32 verifyState   = 2;    //1: 通过     2: 拒绝\n}\n\nmessage VerifySystemMailRsp {\n}\n///////////////////////////////////////////////////////////////\n\n//兑换码玩家范围\nenum EXCHANGE_CODE_USER_SCORE {\n    ECUS_NONE           = 0;\n    ECUS_ALL            = 1;    //所有玩家\n    ECUS_TARGET_UIN     = 2;    //指定玩家\n    ECUS_LEVEL_RANGE    = 3;    //等级区间\n}\n\n//兑换码生成类型\nenum EXCHANGE_CODE_GEN {\n    ECG_NONE            = 0;\n    ECG_SPECIFY         = 1;    //指定兑换码\n    ECS_BATCH_GEN       = 2;    //批量生成\n    ECS_IMPORT          = 3;    //导入兑换码\n}\n\n//获取所有兑换码\nmessage GetAllExchangeCodeReq {\n}\n\nmessage GetAllExchangeCodeRsp {\n    repeated OpExchangeCode normals   = 1;\n}\n\n//创建公告\nmessage CreateExchangeCodeReq {\n    OpExchangeCode info       = 1;\n}\n\nmessage CreateExchangeCodeRsp {\n}\n\n//操作活动\nmessage OperateExchangeCodeReq {\n    int64 uid           = 1;\n    int32 operation     = 2;    //enum ACTIVITY_OP\n    OpExchangeCode info       = 3;    //只有修改才需要传这个\n}\n\nmessage OperateExchangeCodeRsp {\n}\n\n//审核活动\nmessage VerifyExchangeCodeReq {\n    int64 uid           = 1;\n    int32 verifyState   = 2;    //1: 通过     2: 拒绝\n}\n\nmessage VerifyExchangeCodeRsp {\n}\n\n//批量获取兑换码\nmessage GetBatchExchangeCodeReq {\n    int64 uid           = 1;\n    int32 startIndex    = 2;\n    int32 endIndex      = 3;\n}\n\nmessage GetBatchExchangeCodeRsp {\n    repeated ExchangeCode codes = 1;\n}\n///////////////////////////////////////////////////////////////\n\n\nmessage ModifyOpItemRemarkReq {\n    string opItemType   = 1;\n    int64 uid           = 2;\n    string remark       = 3;\n}\n\nmessage UploadPicRsp {\n    string picUrl       = 1;\n}\n\nmessage GetUploadPicRecordRsp {\n    repeated UploadPicRecord infos = 1;\n}\n\nmessage SaveUploadPicRecordReq {\n    repeated UploadPicRecord infos = 1;\n}\n\nmessage OpUserInfo {\n    int64 uin           = 1;\n    string name         = 2;\n    string channel      = 3;    //渠道\n    int32 platform      = 4;    //平台\n    int32 level         = 5;\n    int32 diamond       = 6;    //钻石\n    int32 bindDiamond   = 7;    //绑定钻石\n    int32 gold          = 8;    //金币\n    int64 createStamp   = 9;    //注册时间\n    int32 privilegeTag  = 10;   //权限标识\n    bool isOnline       = 11;   //是否在线\n    bool blocked        = 12;   //是否封号\n    int64 offlineStamp  = 13;   //离线时间\n    string accountId    = 14;   //账号 id\n    bool debug          = 15;   //客户端是否开启 debug 日志\n    bool mute           = 16;   //是否禁言中\n    string guildInfo    = 17;   //所属探险队 guildUid|guildName\n}\n\nenum USER_INFO_TYPE {\n    UIT_NONE    = 0;\n    UIT_UIN     = 1;    //角色 uin\n    UIT_ACCOUNT = 2;    //账号\n    UIT_NAME    = 3;    //昵称\n}\n\n//封停状态\nenum BLOCK_STATE {\n    BS_NONE     = 0;\n    BS_NORMAL   = 1;\n    BS_BLOCKED  = 2;\n}\n\n//查询玩家信息\nmessage GetUserInfosReq {\n    string channel      = 1;\n    int32 platform      = 2;\n    int32 userInfoType  = 3;\n    int32 blockState    = 4;    //enum BLOCK_STATE\n    string queryValue   = 5;\n}\n\nmessage GetUserInfosRsp {\n    repeated OpUserInfo userInfos = 1;\n}\n\n//操作玩家\nmessage OperateUserReq {\n    int64 uin       = 1;\n    string opType   = 2;    //操作类型\n    string param    = 3;    //操作参数\n}\n\n//公会信息\nmessage OpGuildInfo {\n    string guildUid = 1;\n    GuildInfo info  = 2;\n    repeated GuildMember members = 3;\n    bool blockChat  = 4;    //是否封禁聊天和公告\n}\n\n//操作公会\nmessage OperateGuildReq {\n    string guildUid = 1;\n    string opType   = 2;    //操作类型\n    string param    = 3;    //操作参数\n}\n\n//获取玩家详细信息\nmessage GetUserDetailReq {\n    int64 uin = 1;\n}\n\nmessage GetUserDetailRsp {\n    OpUserInfo info             = 1;\n    repeated ItemInfo itemLst   = 2;    //物品列表\n    repeated CardInfo cardLst   = 3;    //卡牌列表\n    repeated BadgeInfo badgeLst = 4;    //徽章列表\n    repeated ActorMail mailLst  = 5;    //邮件列表\n    map<int32, int64> fashions  = 6;    //已获得的皮肤\n    repeated KvPair sceneProgress = 7; //副本关卡进度\n}\n\n//获取白名单列表\nmessage GetWhitelistReq {\n}\n\nmessage GetWhitelistRsp {\n    repeated WhitelistInfo infos  = 1;\n}\n\n//添加白名单\nmessage AddWhitelistReq {\n    WhitelistInfo info = 1;\n}\n\nmessage ModifyWhitelistRemarkReq {\n    string whiteTag = 1;\n    string remark   = 2;\n}\n\n//删除白名单\nmessage DeleteWhitelistReq {\n    string whiteTag = 1;\n}\n\n//设置服务器维护状态\nmessage SetServerStateReq {\n    string svrState  = 1;\n    string maintainNotice = 2;  //维护提示\n}\n\n//设置创建角色数量限制\nmessage SetUserCreateLimitReq {\n    int32 limitCount = 1;\n}\n\n//启动游戏上报\nmessage LaunchGameReq {\n    int32 platform  = 1;    //enum PLATFORM_TYPE\n    string deviceId = 2;    //设备 id\n}\n\nmessage LaunchGameRsp {\n}\n\n//查询充值记录\nmessage GetUserRechargeRecordReq {\n    int64 uin      = 1;\n    int64 fromTime = 2;    //查询时间范围\n    int64 toTime   = 3;\n}\n\nmessage OpOrderInfo {\n    CommonRechargeOrder orderInfo = 1;\n    int32 state = 2;    //sproto.PAY_ORDER_STATE\n    int32 gainDiamond = 3;\n}\n\nmessage GetUserRechargeRecordRsp {\n    repeated OpOrderInfo infos = 1;\n}\n\n///////////////////////////////////////////////////////////////////////////////////////////////////\n\n//商店标签 gm.op_shop_label gm.op_shop_label_verify\nmessage OpShopLabel {\n    int64 uid                   = 1;\n    int64 startStamp            = 2;    //开始时间\n    int64 endStamp              = 3;    //结束时间\n    int32 sortValue             = 4;    //排序值\n    int32 timeState             = 5;    //时间状态  enum TIME_STATE\n    int32 verifyState           = 6;    //审核状态  enum VERIFY_STATE\n    int32 hardState             = 7;    //enum HARD_STATE\n    string remark               = 8;    //备注\n    string labelName            = 9;    //页签名字\n}\n\n//获取所有礼包\nmessage GetAllShopLabelReq {\n    bool onlyOnShelf = 1;   //只需要拉取已上架的\n}\n\nmessage GetAllShopLabelRsp {\n    repeated OpShopLabel infos = 1;\n}\n\n//创建礼包\nmessage CreateShopLabelReq {\n    OpShopLabel info = 1;\n}\n\nmessage CreateShopLabelRsp {\n}\n\n//操作礼包\nmessage OperateShopLabelReq {\n    int64 uid           = 1;\n    int32 operation     = 2;    //enum ACTIVITY_OP\n    OpShopLabel info    = 3;    //只有修改才需要传这个\n}\n\nmessage OperateShopLabelRsp {\n}\n\n//通用审核接口\nmessage CommonVerifyOpItemReq {\n    string opItemType   = 1;\n    int64 uid           = 2;\n    int32 verifyState   = 3;    //1: 通过     2: 拒绝\n}\n\nmessage CommonVerifyOpItemRsp {\n}\n\n///////////////////////////////////////////////////////////////////////////////////////////////////\n\n\n",
  EventMsgNameByID = {
    [1] = "CardUpdateNotify",
    [2] = "NewMessageNotify",
    [3] = "SyncItemsRsp",
    [4] = "RelationChangedNotify",
    [5] = "NewMailNotify",
    [6] = "KickOffNotify",
    [7] = "MutedBySystemNotify",
```

---

## MP/Protoc.lua.lua
**Functions:**
- Lexer.new
- Lexer:__call
- Lexer:test
- Lexer:expected
- Lexer:pos2loc
- Lexer:error
- Lexer:opterror
- Lexer:whitespace
- Lexer:comment
- Lexer:line_end
- Lexer:eof
- Lexer:keyword
- Lexer:ident
- Lexer:full_ident
- Lexer:integer
- Lexer:number
- Lexer:quote
- Lexer:structure
- Lexer:array
- Lexer:constant
- Lexer:option_name
- Lexer:type_name
- Parser.new
- Parser:error
- Parser:addpath
- Parser:parsefile
- toplevel:package
- toplevel:import
- msg_body:message
- msg_body:enum
- msg_body:extend
- msg_body:extensions
- msg_body:reserved
- msg_body:oneof
- msg_body:option
- toplevel:message
- toplevel:enum
- toplevel:option
- toplevel:extend
- svr_body:rpc
- svr_body:option
- svr_body.stream
- toplevel:service
- ctx.import_fallback
- ctx.type_fallback
- ctx.on_import
- Parser:parse
- check_message
- Parser:resolve
- Parser.reload
- self.on_import
- Parser:compile
- Parser:compilefile
- Parser:load
- Parser:loadfile
**Snippet:**
```lua
local string = string
local tonumber = tonumber
local setmetatable = setmetatable
local error = error
local ipairs = ipairs
local io = io
local table = table
local math = math
local assert = assert
local tostring = tostring
```

---
