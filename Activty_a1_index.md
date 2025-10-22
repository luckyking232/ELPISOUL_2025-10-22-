# Activty/a1

## Activty/a1/ActivityCasket01_AssetsTipsByName.lua.lua
**Functions:**
- GetActivityCasket01_AssetsTipsUis
**Snippet:**
```lua
function GetActivityCasket01_AssetsTipsUis(ui)
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

## Activty/a1/ActivityCasket01_CasketByName.lua.lua
**Functions:**
- GetActivityCasket01_CasketUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityCasket01_MapRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityCasket01_MapRegionByName")

function GetActivityCasket01_CasketUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TopImage = ui:GetChild("TopImage")
  uis.BottomImage = ui:GetChild("BottomImage")
  uis.LeftImage = ui:GetChild("LeftImage")
  uis.RightImage = ui:GetChild("RightImage")
```

---

## Activty/a1/ActivityCasket01_CasketWindowByName.lua.lua
**Functions:**
- GetActivityCasket01_CasketWindowUis
**Requires:**
- ActivityCasket01_CasketByName
**Snippet:**
```lua
require("ActivityCasket01_CasketByName")

function GetActivityCasket01_CasketWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityCasket01_CasketUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket01_ExplainContentByName.lua.lua
**Functions:**
- GetActivityCasket01_ExplainContentUis
**Snippet:**
```lua
function GetActivityCasket01_ExplainContentUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket01_ExplainRewardItemByName.lua.lua
**Functions:**
- GetActivityCasket01_ExplainRewardItemUis
**Requires:**
- CommonResource_ItemFrameByName
**Snippet:**
```lua
require("CommonResource_ItemFrameByName")

function GetActivityCasket01_ExplainRewardItemUis(ui)
  local uis = {}
  uis.RewardTxt = ui:GetChild("RewardTxt")
  uis.Item = GetCommonResource_ItemFrameUis(ui:GetChild("Item"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket01_ExplainShopItemByName.lua.lua
**Functions:**
- GetActivityCasket01_ExplainShopItemUis
**Snippet:**
```lua
function GetActivityCasket01_ExplainShopItemUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.BuyNumberTxt = ui:GetChild("BuyNumberTxt")
  uis.PriceTxt = ui:GetChild("PriceTxt")
  uis.GroupNumberTxt = ui:GetChild("GroupNumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket01_ExplainTab1BtnByName.lua.lua
**Functions:**
- GetActivityCasket01_ExplainTab1BtnUis
**Snippet:**
```lua
function GetActivityCasket01_ExplainTab1BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket01_ExplainTab2BtnByName.lua.lua
**Functions:**
- GetActivityCasket01_ExplainTab2BtnUis
**Snippet:**
```lua
function GetActivityCasket01_ExplainTab2BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket01_ExplainTab3BtnByName.lua.lua
**Functions:**
- GetActivityCasket01_ExplainTab3BtnUis
**Snippet:**
```lua
function GetActivityCasket01_ExplainTab3BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket01_ExplainTips1ByName.lua.lua
**Functions:**
- GetActivityCasket01_ExplainTips1Uis
**Snippet:**
```lua
function GetActivityCasket01_ExplainTips1Uis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.ContentList = ui:GetChild("ContentList")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket01_ExplainTips2ByName.lua.lua
**Functions:**
- GetActivityCasket01_ExplainTips2Uis
**Snippet:**
```lua
function GetActivityCasket01_ExplainTips2Uis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.ContentList = ui:GetChild("ContentList")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket01_ExplainTips3ByName.lua.lua
**Functions:**
- GetActivityCasket01_ExplainTips3Uis
**Snippet:**
```lua
function GetActivityCasket01_ExplainTips3Uis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.ContentList = ui:GetChild("ContentList")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket01_ExplainTipsByName.lua.lua
**Functions:**
- GetActivityCasket01_ExplainTipsUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityCasket01_ExplainTipsRegionByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityCasket01_ExplainTipsRegionByName")

function GetActivityCasket01_ExplainTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.ExplainTips = GetActivityCasket01_ExplainTipsRegionUis(ui:GetChild("ExplainTips"))
  uis.root = ui
  return uis
```

---

## Activty/a1/ActivityCasket01_ExplainTipsRegionByName.lua.lua
**Functions:**
- GetActivityCasket01_ExplainTipsRegionUis
**Requires:**
- ActivityCasket01_ExplainTips1ByName
- ActivityCasket01_ExplainTips2ByName
- ActivityCasket01_ExplainTips3ByName
**Snippet:**
```lua
require("ActivityCasket01_ExplainTips1ByName")
require("ActivityCasket01_ExplainTips2ByName")
require("ActivityCasket01_ExplainTips3ByName")

function GetActivityCasket01_ExplainTipsRegionUis(ui)
  local uis = {}
  uis.ExplainTips1 = GetActivityCasket01_ExplainTips1Uis(ui:GetChild("ExplainTips1"))
  uis.ExplainTips2 = GetActivityCasket01_ExplainTips2Uis(ui:GetChild("ExplainTips2"))
  uis.ExplainTips3 = GetActivityCasket01_ExplainTips3Uis(ui:GetChild("ExplainTips3"))
  uis.BurstTab1Btn = ui:GetChild("BurstTab1Btn")
```

---

## Activty/a1/ActivityCasket01_ExplainTipsWindowByName.lua.lua
**Functions:**
- GetActivityCasket01_ExplainTipsWindowUis
**Requires:**
- ActivityCasket01_ExplainTipsByName
**Snippet:**
```lua
require("ActivityCasket01_ExplainTipsByName")

function GetActivityCasket01_ExplainTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityCasket01_ExplainTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket01_ExplainWordByName.lua.lua
**Functions:**
- GetActivityCasket01_ExplainWordUis
**Snippet:**
```lua
function GetActivityCasket01_ExplainWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket01_GaChaBtnByName.lua.lua
**Functions:**
- GetActivityCasket01_GaChaBtnUis
**Requires:**
- ActivityCasket01_GaChaSpendByName
**Snippet:**
```lua
require("ActivityCasket01_GaChaSpendByName")

function GetActivityCasket01_GaChaBtnUis(ui)
  local uis = {}
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.Word3Txt = ui:GetChild("Word3Txt")
  uis.Spend1 = GetActivityCasket01_GaChaSpendUis(ui:GetChild("Spend1"))
  uis.Spend2 = GetActivityCasket01_GaChaSpendUis(ui:GetChild("Spend2"))
  uis.ProgressTxt = ui:GetChild("ProgressTxt")
```

---

## Activty/a1/ActivityCasket01_GaChaSpendByName.lua.lua
**Functions:**
- GetActivityCasket01_GaChaSpendUis
**Snippet:**
```lua
function GetActivityCasket01_GaChaSpendUis(ui)
  local uis = {}
  
  uis.SpendTxt = ui:GetChild("SpendTxt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket01_MapRegionByName.lua.lua
**Functions:**
- GetActivityCasket01_MapRegionUis
**Snippet:**
```lua
function GetActivityCasket01_MapRegionUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket01_OrdinaryRewardTag_1001ByName.lua.lua
**Functions:**
- GetActivityCasket01_OrdinaryRewardTag_1001Uis
**Requires:**
- ActivityCasket01_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket01_RewardMoveWord_01ByName")

function GetActivityCasket01_OrdinaryRewardTag_1001Uis(ui)
  local uis = {}
  uis.MoveWord = GetActivityCasket01_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket01_OrdinaryRewardTag_1002ByName.lua.lua
**Functions:**
- GetActivityCasket01_OrdinaryRewardTag_1002Uis
**Requires:**
- ActivityCasket01_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket01_RewardMoveWord_01ByName")

function GetActivityCasket01_OrdinaryRewardTag_1002Uis(ui)
  local uis = {}
  uis.MoveWord = GetActivityCasket01_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket01_OrdinaryRewardTag_1003ByName.lua.lua
**Functions:**
- GetActivityCasket01_OrdinaryRewardTag_1003Uis
**Requires:**
- ActivityCasket01_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket01_RewardMoveWord_01ByName")

function GetActivityCasket01_OrdinaryRewardTag_1003Uis(ui)
  local uis = {}
  uis.MoveWord = GetActivityCasket01_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket01_OrdinaryRewardTag_1004ByName.lua.lua
**Functions:**
- GetActivityCasket01_OrdinaryRewardTag_1004Uis
**Requires:**
- ActivityCasket01_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket01_RewardMoveWord_01ByName")

function GetActivityCasket01_OrdinaryRewardTag_1004Uis(ui)
  local uis = {}
  uis.MoveWord = GetActivityCasket01_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket01_OrdinaryRewardTag_1005ByName.lua.lua
**Functions:**
- GetActivityCasket01_OrdinaryRewardTag_1005Uis
**Requires:**
- ActivityCasket01_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket01_RewardMoveWord_01ByName")

function GetActivityCasket01_OrdinaryRewardTag_1005Uis(ui)
  local uis = {}
  uis.MoveWord = GetActivityCasket01_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket01_OrdinaryRewardTag_1006ByName.lua.lua
**Functions:**
- GetActivityCasket01_OrdinaryRewardTag_1006Uis
**Requires:**
- ActivityCasket01_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket01_RewardMoveWord_01ByName")

function GetActivityCasket01_OrdinaryRewardTag_1006Uis(ui)
  local uis = {}
  uis.MoveWord = GetActivityCasket01_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket01_OrdinaryRewardTag_1007ByName.lua.lua
**Functions:**
- GetActivityCasket01_OrdinaryRewardTag_1007Uis
**Requires:**
- ActivityCasket01_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket01_RewardMoveWord_01ByName")

function GetActivityCasket01_OrdinaryRewardTag_1007Uis(ui)
  local uis = {}
  uis.MoveWord = GetActivityCasket01_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket01_OrdinaryRewardTag_1008ByName.lua.lua
**Functions:**
- GetActivityCasket01_OrdinaryRewardTag_1008Uis
**Requires:**
- ActivityCasket01_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket01_RewardMoveWord_01ByName")

function GetActivityCasket01_OrdinaryRewardTag_1008Uis(ui)
  local uis = {}
  uis.MoveWord = GetActivityCasket01_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket01_OrdinaryRewardTag_1009ByName.lua.lua
**Functions:**
- GetActivityCasket01_OrdinaryRewardTag_1009Uis
**Requires:**
- ActivityCasket01_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket01_RewardMoveWord_01ByName")

function GetActivityCasket01_OrdinaryRewardTag_1009Uis(ui)
  local uis = {}
  uis.MoveWord = GetActivityCasket01_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket01_OrdinaryRewardTag_1010ByName.lua.lua
**Functions:**
- GetActivityCasket01_OrdinaryRewardTag_1010Uis
**Requires:**
- ActivityCasket01_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket01_RewardMoveWord_01ByName")

function GetActivityCasket01_OrdinaryRewardTag_1010Uis(ui)
  local uis = {}
  uis.BoxHolder = ui:GetChild("BoxHolder")
  uis.MoveWord = GetActivityCasket01_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## Activty/a1/ActivityCasket01_RecordBtnByName.lua.lua
**Functions:**
- GetActivityCasket01_RecordBtnUis
**Snippet:**
```lua
function GetActivityCasket01_RecordBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket01_RewardMoveWord_01ByName.lua.lua
**Functions:**
- GetActivityCasket01_RewardMoveWord_01Uis
**Snippet:**
```lua
function GetActivityCasket01_RewardMoveWord_01Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket01_RuleBtnByName.lua.lua
**Functions:**
- GetActivityCasket01_RuleBtnUis
**Snippet:**
```lua
function GetActivityCasket01_RuleBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket01_ShopBtnByName.lua.lua
**Functions:**
- GetActivityCasket01_ShopBtnUis
**Snippet:**
```lua
function GetActivityCasket01_ShopBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TagTxt = ui:GetChild("TagTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket01_TagRegion_01ByName.lua.lua
**Functions:**
- GetActivityCasket01_TagRegion_01Uis
**Requires:**
- ActivityCasket01_OrdinaryRewardTag_1010ByName
- ActivityCasket01_OrdinaryRewardTag_1001ByName
- ActivityCasket01_OrdinaryRewardTag_1002ByName
- ActivityCasket01_OrdinaryRewardTag_1003ByName
- ActivityCasket01_OrdinaryRewardTag_1004ByName
- ActivityCasket01_OrdinaryRewardTag_1009ByName
- ActivityCasket01_OrdinaryRewardTag_1008ByName
- ActivityCasket01_OrdinaryRewardTag_1007ByName
- ActivityCasket01_OrdinaryRewardTag_1006ByName
- ActivityCasket01_OrdinaryRewardTag_1005ByName
**Snippet:**
```lua
require("ActivityCasket01_OrdinaryRewardTag_1010ByName")
require("ActivityCasket01_OrdinaryRewardTag_1001ByName")
require("ActivityCasket01_OrdinaryRewardTag_1002ByName")
require("ActivityCasket01_OrdinaryRewardTag_1003ByName")
require("ActivityCasket01_OrdinaryRewardTag_1004ByName")
require("ActivityCasket01_OrdinaryRewardTag_1009ByName")
require("ActivityCasket01_OrdinaryRewardTag_1008ByName")
require("ActivityCasket01_OrdinaryRewardTag_1007ByName")
require("ActivityCasket01_OrdinaryRewardTag_1006ByName")
require("ActivityCasket01_OrdinaryRewardTag_1005ByName")
```

---

## Activty/a1/ActivityCasket02_AssetsTipsByName.lua.lua
**Functions:**
- GetActivityCasket02_AssetsTipsUis
**Snippet:**
```lua
function GetActivityCasket02_AssetsTipsUis(ui)
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

## Activty/a1/ActivityCasket02_CasketByName.lua.lua
**Functions:**
- GetActivityCasket02_CasketUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityCasket02_MapRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityCasket02_MapRegionByName")

function GetActivityCasket02_CasketUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TopImage = ui:GetChild("TopImage")
  uis.BottomImage = ui:GetChild("BottomImage")
  uis.LeftImage = ui:GetChild("LeftImage")
  uis.RightImage = ui:GetChild("RightImage")
```

---

## Activty/a1/ActivityCasket02_CasketWindowByName.lua.lua
**Functions:**
- GetActivityCasket02_CasketWindowUis
**Requires:**
- ActivityCasket02_CasketByName
**Snippet:**
```lua
require("ActivityCasket02_CasketByName")

function GetActivityCasket02_CasketWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityCasket02_CasketUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket02_ExplainContentByName.lua.lua
**Functions:**
- GetActivityCasket02_ExplainContentUis
**Snippet:**
```lua
function GetActivityCasket02_ExplainContentUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket02_ExplainRewardItemByName.lua.lua
**Functions:**
- GetActivityCasket02_ExplainRewardItemUis
**Requires:**
- CommonResource_ItemFrameByName
**Snippet:**
```lua
require("CommonResource_ItemFrameByName")

function GetActivityCasket02_ExplainRewardItemUis(ui)
  local uis = {}
  uis.RewardTxt = ui:GetChild("RewardTxt")
  uis.Item = GetCommonResource_ItemFrameUis(ui:GetChild("Item"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket02_ExplainShopItemByName.lua.lua
**Functions:**
- GetActivityCasket02_ExplainShopItemUis
**Snippet:**
```lua
function GetActivityCasket02_ExplainShopItemUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.BuyNumberTxt = ui:GetChild("BuyNumberTxt")
  uis.PriceTxt = ui:GetChild("PriceTxt")
  uis.GroupNumberTxt = ui:GetChild("GroupNumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket02_ExplainTab1BtnByName.lua.lua
**Functions:**
- GetActivityCasket02_ExplainTab1BtnUis
**Snippet:**
```lua
function GetActivityCasket02_ExplainTab1BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket02_ExplainTab2BtnByName.lua.lua
**Functions:**
- GetActivityCasket02_ExplainTab2BtnUis
**Snippet:**
```lua
function GetActivityCasket02_ExplainTab2BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket02_ExplainTab3BtnByName.lua.lua
**Functions:**
- GetActivityCasket02_ExplainTab3BtnUis
**Snippet:**
```lua
function GetActivityCasket02_ExplainTab3BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket02_ExplainTips1ByName.lua.lua
**Functions:**
- GetActivityCasket02_ExplainTips1Uis
**Snippet:**
```lua
function GetActivityCasket02_ExplainTips1Uis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.ContentList = ui:GetChild("ContentList")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket02_ExplainTips2ByName.lua.lua
**Functions:**
- GetActivityCasket02_ExplainTips2Uis
**Snippet:**
```lua
function GetActivityCasket02_ExplainTips2Uis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.ContentList = ui:GetChild("ContentList")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket02_ExplainTips3ByName.lua.lua
**Functions:**
- GetActivityCasket02_ExplainTips3Uis
**Snippet:**
```lua
function GetActivityCasket02_ExplainTips3Uis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.ContentList = ui:GetChild("ContentList")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket02_ExplainTipsByName.lua.lua
**Functions:**
- GetActivityCasket02_ExplainTipsUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityCasket02_ExplainTipsRegionByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityCasket02_ExplainTipsRegionByName")

function GetActivityCasket02_ExplainTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.ExplainTips = GetActivityCasket02_ExplainTipsRegionUis(ui:GetChild("ExplainTips"))
  uis.root = ui
  return uis
```

---

## Activty/a1/ActivityCasket02_ExplainTipsRegionByName.lua.lua
**Functions:**
- GetActivityCasket02_ExplainTipsRegionUis
**Requires:**
- ActivityCasket02_ExplainTips1ByName
- ActivityCasket02_ExplainTips2ByName
- ActivityCasket02_ExplainTips3ByName
**Snippet:**
```lua
require("ActivityCasket02_ExplainTips1ByName")
require("ActivityCasket02_ExplainTips2ByName")
require("ActivityCasket02_ExplainTips3ByName")

function GetActivityCasket02_ExplainTipsRegionUis(ui)
  local uis = {}
  uis.ExplainTips1 = GetActivityCasket02_ExplainTips1Uis(ui:GetChild("ExplainTips1"))
  uis.ExplainTips2 = GetActivityCasket02_ExplainTips2Uis(ui:GetChild("ExplainTips2"))
  uis.ExplainTips3 = GetActivityCasket02_ExplainTips3Uis(ui:GetChild("ExplainTips3"))
  uis.BurstTab1Btn = ui:GetChild("BurstTab1Btn")
```

---

## Activty/a1/ActivityCasket02_ExplainTipsWindowByName.lua.lua
**Functions:**
- GetActivityCasket02_ExplainTipsWindowUis
**Requires:**
- ActivityCasket02_ExplainTipsByName
**Snippet:**
```lua
require("ActivityCasket02_ExplainTipsByName")

function GetActivityCasket02_ExplainTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityCasket02_ExplainTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket02_ExplainWordByName.lua.lua
**Functions:**
- GetActivityCasket02_ExplainWordUis
**Snippet:**
```lua
function GetActivityCasket02_ExplainWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket02_GaChaBtnByName.lua.lua
**Functions:**
- GetActivityCasket02_GaChaBtnUis
**Requires:**
- ActivityCasket02_GaChaSpendByName
**Snippet:**
```lua
require("ActivityCasket02_GaChaSpendByName")

function GetActivityCasket02_GaChaBtnUis(ui)
  local uis = {}
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.Word3Txt = ui:GetChild("Word3Txt")
  uis.Spend1 = GetActivityCasket02_GaChaSpendUis(ui:GetChild("Spend1"))
  uis.Spend2 = GetActivityCasket02_GaChaSpendUis(ui:GetChild("Spend2"))
  uis.ProgressTxt = ui:GetChild("ProgressTxt")
```

---

## Activty/a1/ActivityCasket02_GaChaSpendByName.lua.lua
**Functions:**
- GetActivityCasket02_GaChaSpendUis
**Snippet:**
```lua
function GetActivityCasket02_GaChaSpendUis(ui)
  local uis = {}
  
  uis.SpendTxt = ui:GetChild("SpendTxt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket02_MapRegionByName.lua.lua
**Functions:**
- GetActivityCasket02_MapRegionUis
**Snippet:**
```lua
function GetActivityCasket02_MapRegionUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket02_OrdinaryRewardTag_1001ByName.lua.lua
**Functions:**
- GetActivityCasket02_OrdinaryRewardTag_1001Uis
**Requires:**
- ActivityCasket02_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket02_RewardMoveWord_01ByName")

function GetActivityCasket02_OrdinaryRewardTag_1001Uis(ui)
  local uis = {}
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.MoveWord = GetActivityCasket02_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket02_OrdinaryRewardTag_1002ByName.lua.lua
**Functions:**
- GetActivityCasket02_OrdinaryRewardTag_1002Uis
**Requires:**
- ActivityCasket02_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket02_RewardMoveWord_01ByName")

function GetActivityCasket02_OrdinaryRewardTag_1002Uis(ui)
  local uis = {}
  uis.MoveWord = GetActivityCasket02_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket02_OrdinaryRewardTag_1003ByName.lua.lua
**Functions:**
- GetActivityCasket02_OrdinaryRewardTag_1003Uis
**Requires:**
- ActivityCasket02_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket02_RewardMoveWord_01ByName")

function GetActivityCasket02_OrdinaryRewardTag_1003Uis(ui)
  local uis = {}
  uis.MoveWord = GetActivityCasket02_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket02_OrdinaryRewardTag_1004ByName.lua.lua
**Functions:**
- GetActivityCasket02_OrdinaryRewardTag_1004Uis
**Requires:**
- ActivityCasket02_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket02_RewardMoveWord_01ByName")

function GetActivityCasket02_OrdinaryRewardTag_1004Uis(ui)
  local uis = {}
  uis.MoveWord = GetActivityCasket02_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket02_OrdinaryRewardTag_1005ByName.lua.lua
**Functions:**
- GetActivityCasket02_OrdinaryRewardTag_1005Uis
**Requires:**
- ActivityCasket02_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket02_RewardMoveWord_01ByName")

function GetActivityCasket02_OrdinaryRewardTag_1005Uis(ui)
  local uis = {}
  uis.MoveWord = GetActivityCasket02_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket02_OrdinaryRewardTag_1006ByName.lua.lua
**Functions:**
- GetActivityCasket02_OrdinaryRewardTag_1006Uis
**Requires:**
- ActivityCasket02_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket02_RewardMoveWord_01ByName")

function GetActivityCasket02_OrdinaryRewardTag_1006Uis(ui)
  local uis = {}
  uis.MoveWord = GetActivityCasket02_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket02_OrdinaryRewardTag_1007ByName.lua.lua
**Functions:**
- GetActivityCasket02_OrdinaryRewardTag_1007Uis
**Requires:**
- ActivityCasket02_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket02_RewardMoveWord_01ByName")

function GetActivityCasket02_OrdinaryRewardTag_1007Uis(ui)
  local uis = {}
  uis.MoveWord = GetActivityCasket02_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket02_OrdinaryRewardTag_1008ByName.lua.lua
**Functions:**
- GetActivityCasket02_OrdinaryRewardTag_1008Uis
**Requires:**
- ActivityCasket02_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket02_RewardMoveWord_01ByName")

function GetActivityCasket02_OrdinaryRewardTag_1008Uis(ui)
  local uis = {}
  uis.MoveWord = GetActivityCasket02_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket02_OrdinaryRewardTag_1009ByName.lua.lua
**Functions:**
- GetActivityCasket02_OrdinaryRewardTag_1009Uis
**Requires:**
- ActivityCasket02_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket02_RewardMoveWord_01ByName")

function GetActivityCasket02_OrdinaryRewardTag_1009Uis(ui)
  local uis = {}
  uis.MoveWord = GetActivityCasket02_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket02_OrdinaryRewardTag_1010ByName.lua.lua
**Functions:**
- GetActivityCasket02_OrdinaryRewardTag_1010Uis
**Requires:**
- ActivityCasket02_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket02_RewardMoveWord_01ByName")

function GetActivityCasket02_OrdinaryRewardTag_1010Uis(ui)
  local uis = {}
  uis.BoxHolder = ui:GetChild("BoxHolder")
  uis.MoveWord = GetActivityCasket02_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## Activty/a1/ActivityCasket02_RecordBtnByName.lua.lua
**Functions:**
- GetActivityCasket02_RecordBtnUis
**Snippet:**
```lua
function GetActivityCasket02_RecordBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket02_RewardMoveWord_01ByName.lua.lua
**Functions:**
- GetActivityCasket02_RewardMoveWord_01Uis
**Snippet:**
```lua
function GetActivityCasket02_RewardMoveWord_01Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket02_RuleBtnByName.lua.lua
**Functions:**
- GetActivityCasket02_RuleBtnUis
**Snippet:**
```lua
function GetActivityCasket02_RuleBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket02_ShopBtnByName.lua.lua
**Functions:**
- GetActivityCasket02_ShopBtnUis
**Snippet:**
```lua
function GetActivityCasket02_ShopBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TagTxt = ui:GetChild("TagTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket02_TagRegion_01ByName.lua.lua
**Functions:**
- GetActivityCasket02_TagRegion_01Uis
**Requires:**
- ActivityCasket02_OrdinaryRewardTag_1010ByName
- ActivityCasket02_OrdinaryRewardTag_1001ByName
- ActivityCasket02_OrdinaryRewardTag_1002ByName
- ActivityCasket02_OrdinaryRewardTag_1003ByName
- ActivityCasket02_OrdinaryRewardTag_1004ByName
- ActivityCasket02_OrdinaryRewardTag_1009ByName
- ActivityCasket02_OrdinaryRewardTag_1008ByName
- ActivityCasket02_OrdinaryRewardTag_1007ByName
- ActivityCasket02_OrdinaryRewardTag_1006ByName
- ActivityCasket02_OrdinaryRewardTag_1005ByName
**Snippet:**
```lua
require("ActivityCasket02_OrdinaryRewardTag_1010ByName")
require("ActivityCasket02_OrdinaryRewardTag_1001ByName")
require("ActivityCasket02_OrdinaryRewardTag_1002ByName")
require("ActivityCasket02_OrdinaryRewardTag_1003ByName")
require("ActivityCasket02_OrdinaryRewardTag_1004ByName")
require("ActivityCasket02_OrdinaryRewardTag_1009ByName")
require("ActivityCasket02_OrdinaryRewardTag_1008ByName")
require("ActivityCasket02_OrdinaryRewardTag_1007ByName")
require("ActivityCasket02_OrdinaryRewardTag_1006ByName")
require("ActivityCasket02_OrdinaryRewardTag_1005ByName")
```

---

## Activty/a1/ActivityCasket2ExplainTipsWindow.lua.lua
**Functions:**
- ActivityCasket2ExplainTipsWindow.ReInitData
- ActivityCasket2ExplainTipsWindow.OnInit
- ActivityCasket2ExplainTipsWindow.UpdateInfo
- ActivityCasket2ExplainTipsWindow.ShowShop
- tips.ContentList.itemRenderer
- ActivityCasket2ExplainTipsWindow.ShowRule
- tips.ContentList.itemRenderer
- wordList.itemRenderer
- ActivityCasket2ExplainTipsWindow.ShowRecord
- tips.ContentList.itemRenderer
- ActivityCasket2ExplainTipsWindow.GetPoolInfo
- ActivityCasket2ExplainTipsWindow.GetCost
- ActivityCasket2ExplainTipsWindow.InitBtn
- ActivityCasket2ExplainTipsWindow.OnClose
- ActivityCasket2ExplainTipsWindow.HandleMessage
**Requires:**
- ActivityCasket01_ExplainTipsWindowByName
**Snippet:**
```lua
require("ActivityCasket01_ExplainTipsWindowByName")
local ActivityCasket2ExplainTipsWindow = {}
local uis, contentPane, turnTableConfig, turnTableInfo

function ActivityCasket2ExplainTipsWindow.ReInitData()
end

function ActivityCasket2ExplainTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ActivityCasket2ExplainTipsWindow.package, WinResConfig.ActivityCasket2ExplainTipsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/a1/ActivityCasket2Window.lua.lua
**Functions:**
- ActivityCasket2Window.ReInitData
- ActivityCasket2Window.OnInit
- ActivityCasket2Window.GetPoolInfo
- ActivityCasket2Window.UpdateInfo
- ActivityCasket2Window.PlanAnim
- ActivityCasket2Window.GetData
- ActivityCasket2Window.GetCost
- ActivityCasket2Window.InitAssetsTips
- uis.Main.AssetsTipsList.itemRenderer
- ActivityCasket2Window.InitBtn
- ActivityCasket2Window.OnShown
- ActivityCasket2Window.OnClose
- ActivityCasket2Window.CheckActivityEnd
- ActivityCasket2Window.HandleMessage
**Requires:**
- ActivityCasket01_CasketWindowByName
**Snippet:**
```lua
require("ActivityCasket01_CasketWindowByName")
local ActivityCasket2Window = {}
local uis, contentPane, turnTableInfo, turnTableConfig, boxObj, tempHolder, boxUnlockNum, showBoxOpen, maxNum, curIndex, lastIndex, isActivityEnd, animPlay, mapCom
local tatalNum = 1
local speedUpNum = 0
local time = 0.015
local speedUp = 0.005
local waitTime = 0.8

function ActivityCasket2Window.ReInitData()
```

---

## Activty/a1/ActivityCasket3ExplainTipsWindow.lua.lua
**Functions:**
- ActivityCasket3ExplainTipsWindow.ReInitData
- ActivityCasket3ExplainTipsWindow.OnInit
- ActivityCasket3ExplainTipsWindow.UpdateInfo
- ActivityCasket3ExplainTipsWindow.ShowShop
- tips.ContentList.itemRenderer
- ActivityCasket3ExplainTipsWindow.ShowRule
- tips.ContentList.itemRenderer
- wordList.itemRenderer
- ActivityCasket3ExplainTipsWindow.ShowRecord
- tips.ContentList.itemRenderer
- ActivityCasket3ExplainTipsWindow.GetPoolInfo
- ActivityCasket3ExplainTipsWindow.GetCost
- ActivityCasket3ExplainTipsWindow.InitBtn
- ActivityCasket3ExplainTipsWindow.OnClose
- ActivityCasket3ExplainTipsWindow.HandleMessage
**Requires:**
- ActivityCasket02_ExplainTipsWindowByName
**Snippet:**
```lua
require("ActivityCasket02_ExplainTipsWindowByName")
local ActivityCasket3ExplainTipsWindow = {}
local uis, contentPane, turnTableConfig, turnTableInfo

function ActivityCasket3ExplainTipsWindow.ReInitData()
end

function ActivityCasket3ExplainTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ActivityCasket3ExplainTipsWindow.package, WinResConfig.ActivityCasket3ExplainTipsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/a1/ActivityCasket3Window.lua.lua
**Functions:**
- ActivityCasket3Window.ReInitData
- ActivityCasket3Window.OnInit
- ActivityCasket3Window.GetPoolInfo
- ActivityCasket3Window.UpdateInfo
- ActivityCasket3Window.PlanAnim
- ActivityCasket3Window.GetData
- ActivityCasket3Window.GetCost
- ActivityCasket3Window.InitAssetsTips
- uis.Main.AssetsTipsList.itemRenderer
- ActivityCasket3Window.InitBtn
- ActivityCasket3Window.OnShown
- ActivityCasket3Window.OnClose
- ActivityCasket3Window.CheckActivityEnd
- ActivityCasket3Window.HandleMessage
**Requires:**
- ActivityCasket02_CasketWindowByName
**Snippet:**
```lua
require("ActivityCasket02_CasketWindowByName")
local ActivityCasket3Window = {}
local uis, contentPane, turnTableInfo, turnTableConfig, maxNum, curIndex, lastIndex, isActivityEnd, animPlay, boxObj, tempHolder, boxUnlockNum, showBoxOpen, mapCom
local tatalNum = 1
local speedUpNum = 0
local time = 0.015
local speedUp = 0.005
local waitTime = 0.8

function ActivityCasket3Window.ReInitData()
```

---

## Activty/a1/ActivityCasketExplainTipsWindow.lua.lua
**Functions:**
- ActivityCasketExplainTipsWindow.ReInitData
- ActivityCasketExplainTipsWindow.OnInit
- ActivityCasketExplainTipsWindow.UpdateInfo
- ActivityCasketExplainTipsWindow.ShowShop
- tips.ContentList.itemRenderer
- ActivityCasketExplainTipsWindow.ShowRule
- tips.ContentList.itemRenderer
- wordList.itemRenderer
- ActivityCasketExplainTipsWindow.ShowRecord
- tips.ContentList.itemRenderer
- ActivityCasketExplainTipsWindow.GetPoolInfo
- ActivityCasketExplainTipsWindow.GetCost
- ActivityCasketExplainTipsWindow.InitBtn
- ActivityCasketExplainTipsWindow.OnClose
- ActivityCasketExplainTipsWindow.HandleMessage
**Requires:**
- ActivityCasket_ExplainTipsWindowByName
**Snippet:**
```lua
require("ActivityCasket_ExplainTipsWindowByName")
local ActivityCasketExplainTipsWindow = {}
local uis, contentPane, turnTableConfig, turnTableInfo

function ActivityCasketExplainTipsWindow.ReInitData()
end

function ActivityCasketExplainTipsWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ActivityCasketExplainTipsWindow.package, WinResConfig.ActivityCasketExplainTipsWindow.comName, function(com)
    contentPane = com
```

---

## Activty/a1/ActivityCasketHome_CardByName.lua.lua
**Functions:**
- GetActivityCasketHome_CardUis
**Requires:**
- ActivityCasketHome_CardPicByName
- ActivityCasketHome_StateByName
- ActivityCasketHome_TimeByName
**Snippet:**
```lua
require("ActivityCasketHome_CardPicByName")
require("ActivityCasketHome_StateByName")
require("ActivityCasketHome_TimeByName")

function GetActivityCasketHome_CardUis(ui)
  local uis = {}
  uis.Pic = GetActivityCasketHome_CardPicUis(ui:GetChild("Pic"))
  uis.SignList = ui:GetChild("SignList")
  uis.State = GetActivityCasketHome_StateUis(ui:GetChild("State"))
  uis.Time = GetActivityCasketHome_TimeUis(ui:GetChild("Time"))
```

---

## Activty/a1/ActivityCasketHome_CardPicByName.lua.lua
**Functions:**
- GetActivityCasketHome_CardPicUis
**Snippet:**
```lua
function GetActivityCasketHome_CardPicUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasketHome_CasketHomeByName.lua.lua
**Functions:**
- GetActivityCasketHome_CasketHomeUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityCasketHome_TipsByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityCasketHome_TipsByName")

function GetActivityCasketHome_CasketHomeUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Tips = GetActivityCasketHome_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
```

---

## Activty/a1/ActivityCasketHome_CasketHomeWindowByName.lua.lua
**Functions:**
- GetActivityCasketHome_CasketHomeWindowUis
**Requires:**
- ActivityCasketHome_CasketHomeByName
**Snippet:**
```lua
require("ActivityCasketHome_CasketHomeByName")

function GetActivityCasketHome_CasketHomeWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityCasketHome_CasketHomeUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasketHome_CloseBtnByName.lua.lua
**Functions:**
- GetActivityCasketHome_CloseBtnUis
**Snippet:**
```lua
function GetActivityCasketHome_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasketHome_Sign1ByName.lua.lua
**Functions:**
- GetActivityCasketHome_Sign1Uis
**Snippet:**
```lua
function GetActivityCasketHome_Sign1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasketHome_Sign2ByName.lua.lua
**Functions:**
- GetActivityCasketHome_Sign2Uis
**Snippet:**
```lua
function GetActivityCasketHome_Sign2Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasketHome_StateByName.lua.lua
**Functions:**
- GetActivityCasketHome_StateUis
**Snippet:**
```lua
function GetActivityCasketHome_StateUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasketHome_TimeByName.lua.lua
**Functions:**
- GetActivityCasketHome_TimeUis
**Snippet:**
```lua
function GetActivityCasketHome_TimeUis(ui)
  local uis = {}
  
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasketHome_TipsByName.lua.lua
**Functions:**
- GetActivityCasketHome_TipsUis
**Snippet:**
```lua
function GetActivityCasketHome_TipsUis(ui)
  local uis = {}
  
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.CardList = ui:GetChild("CardList")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasketWindow.lua.lua
**Functions:**
- ActivityCasketWindow.ReInitData
- ActivityCasketWindow.OnInit
- ActivityCasketWindow.GetPoolInfo
- ActivityCasketWindow.UpdateInfo
- ActivityCasketWindow.PlanAnim
- ActivityCasketWindow.GetData
- ActivityCasketWindow.GetCost
- ActivityCasketWindow.InitAssetsTips
- uis.Main.AssetsTipsList.itemRenderer
- ActivityCasketWindow.InitBtn
- ActivityCasketWindow.OnShown
- ActivityCasketWindow.OnClose
- ActivityCasketWindow.CheckActivityEnd
- ActivityCasketWindow.HandleMessage
**Requires:**
- ActivityCasket_CasketWindowByName
**Snippet:**
```lua
require("ActivityCasket_CasketWindowByName")
local ActivityCasketWindow = {}
local uis, contentPane, turnTableInfo, turnTableConfig, maxNum, curIndex, lastIndex, isActivityEnd, animPlay, boxObj, tempHolder, boxUnlockNum, showBoxOpen, mapCom
local tatalNum = 1
local speedUpNum = 0
local time = 0.015
local speedUp = 0.005
local waitTime = 0.8

function ActivityCasketWindow.ReInitData()
```

---

## Activty/a1/ActivityCasket_AssetsTipsByName.lua.lua
**Functions:**
- GetActivityCasket_AssetsTipsUis
**Snippet:**
```lua
function GetActivityCasket_AssetsTipsUis(ui)
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

## Activty/a1/ActivityCasket_CasketByName.lua.lua
**Functions:**
- GetActivityCasket_CasketUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityCasket_MapRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityCasket_MapRegionByName")

function GetActivityCasket_CasketUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TopImage = ui:GetChild("TopImage")
  uis.BottomImage = ui:GetChild("BottomImage")
  uis.LeftImage = ui:GetChild("LeftImage")
  uis.RightImage = ui:GetChild("RightImage")
```

---

## Activty/a1/ActivityCasket_CasketWindowByName.lua.lua
**Functions:**
- GetActivityCasket_CasketWindowUis
**Requires:**
- ActivityCasket_CasketByName
**Snippet:**
```lua
require("ActivityCasket_CasketByName")

function GetActivityCasket_CasketWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityCasket_CasketUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket_ExplainContentByName.lua.lua
**Functions:**
- GetActivityCasket_ExplainContentUis
**Snippet:**
```lua
function GetActivityCasket_ExplainContentUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.WordList = ui:GetChild("WordList")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket_ExplainRecordByName.lua.lua
**Functions:**
- GetActivityCasket_ExplainRecordUis
**Snippet:**
```lua
function GetActivityCasket_ExplainRecordUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.OrderTxt = ui:GetChild("OrderTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## Activty/a1/ActivityCasket_ExplainRewardItemByName.lua.lua
**Functions:**
- GetActivityCasket_ExplainRewardItemUis
**Requires:**
- CommonResource_ItemFrameByName
**Snippet:**
```lua
require("CommonResource_ItemFrameByName")

function GetActivityCasket_ExplainRewardItemUis(ui)
  local uis = {}
  uis.RewardTxt = ui:GetChild("RewardTxt")
  uis.Item = GetCommonResource_ItemFrameUis(ui:GetChild("Item"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket_ExplainShopItemByName.lua.lua
**Functions:**
- GetActivityCasket_ExplainShopItemUis
**Snippet:**
```lua
function GetActivityCasket_ExplainShopItemUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.BuyNumberTxt = ui:GetChild("BuyNumberTxt")
  uis.PriceTxt = ui:GetChild("PriceTxt")
  uis.GroupNumberTxt = ui:GetChild("GroupNumberTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket_ExplainTab1BtnByName.lua.lua
**Functions:**
- GetActivityCasket_ExplainTab1BtnUis
**Snippet:**
```lua
function GetActivityCasket_ExplainTab1BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket_ExplainTab2BtnByName.lua.lua
**Functions:**
- GetActivityCasket_ExplainTab2BtnUis
**Snippet:**
```lua
function GetActivityCasket_ExplainTab2BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket_ExplainTab3BtnByName.lua.lua
**Functions:**
- GetActivityCasket_ExplainTab3BtnUis
**Snippet:**
```lua
function GetActivityCasket_ExplainTab3BtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket_ExplainTips1ByName.lua.lua
**Functions:**
- GetActivityCasket_ExplainTips1Uis
**Snippet:**
```lua
function GetActivityCasket_ExplainTips1Uis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.ContentList = ui:GetChild("ContentList")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket_ExplainTips2ByName.lua.lua
**Functions:**
- GetActivityCasket_ExplainTips2Uis
**Snippet:**
```lua
function GetActivityCasket_ExplainTips2Uis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.ContentList = ui:GetChild("ContentList")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket_ExplainTips3ByName.lua.lua
**Functions:**
- GetActivityCasket_ExplainTips3Uis
**Snippet:**
```lua
function GetActivityCasket_ExplainTips3Uis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.ContentList = ui:GetChild("ContentList")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket_ExplainTips4ByName.lua.lua
**Functions:**
- GetActivityCasket_ExplainTips4Uis
**Snippet:**
```lua
function GetActivityCasket_ExplainTips4Uis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.ContentList = ui:GetChild("ContentList")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket_ExplainTipsByName.lua.lua
**Functions:**
- GetActivityCasket_ExplainTipsUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityCasket_ExplainTipsRegionByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityCasket_ExplainTipsRegionByName")

function GetActivityCasket_ExplainTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.ExplainTips = GetActivityCasket_ExplainTipsRegionUis(ui:GetChild("ExplainTips"))
  uis.root = ui
  return uis
```

---

## Activty/a1/ActivityCasket_ExplainTipsRegionByName.lua.lua
**Functions:**
- GetActivityCasket_ExplainTipsRegionUis
**Requires:**
- ActivityCasket_ExplainTips1ByName
- ActivityCasket_ExplainTips2ByName
- ActivityCasket_ExplainTips4ByName
**Snippet:**
```lua
require("ActivityCasket_ExplainTips1ByName")
require("ActivityCasket_ExplainTips2ByName")
require("ActivityCasket_ExplainTips4ByName")

function GetActivityCasket_ExplainTipsRegionUis(ui)
  local uis = {}
  uis.ExplainTips1 = GetActivityCasket_ExplainTips1Uis(ui:GetChild("ExplainTips1"))
  uis.ExplainTips2 = GetActivityCasket_ExplainTips2Uis(ui:GetChild("ExplainTips2"))
  uis.ExplainTips3 = GetActivityCasket_ExplainTips4Uis(ui:GetChild("ExplainTips3"))
  uis.BurstTab1Btn = ui:GetChild("BurstTab1Btn")
```

---

## Activty/a1/ActivityCasket_ExplainTipsWindowByName.lua.lua
**Functions:**
- GetActivityCasket_ExplainTipsWindowUis
**Requires:**
- ActivityCasket_ExplainTipsByName
**Snippet:**
```lua
require("ActivityCasket_ExplainTipsByName")

function GetActivityCasket_ExplainTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityCasket_ExplainTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket_ExplainWordByName.lua.lua
**Functions:**
- GetActivityCasket_ExplainWordUis
**Snippet:**
```lua
function GetActivityCasket_ExplainWordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket_GaChaBtnByName.lua.lua
**Functions:**
- GetActivityCasket_GaChaBtnUis
**Requires:**
- ActivityCasket_GaChaSpendByName
**Snippet:**
```lua
require("ActivityCasket_GaChaSpendByName")

function GetActivityCasket_GaChaBtnUis(ui)
  local uis = {}
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.Word2Txt = ui:GetChild("Word2Txt")
  uis.Word3Txt = ui:GetChild("Word3Txt")
  uis.Spend1 = GetActivityCasket_GaChaSpendUis(ui:GetChild("Spend1"))
  uis.Spend2 = GetActivityCasket_GaChaSpendUis(ui:GetChild("Spend2"))
  uis.ProgressTxt = ui:GetChild("ProgressTxt")
```

---

## Activty/a1/ActivityCasket_GaChaSpendByName.lua.lua
**Functions:**
- GetActivityCasket_GaChaSpendUis
**Snippet:**
```lua
function GetActivityCasket_GaChaSpendUis(ui)
  local uis = {}
  
  uis.SpendTxt = ui:GetChild("SpendTxt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket_MapRegionByName.lua.lua
**Functions:**
- GetActivityCasket_MapRegionUis
**Snippet:**
```lua
function GetActivityCasket_MapRegionUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket_OrdinaryRewardTag_1001ByName.lua.lua
**Functions:**
- GetActivityCasket_OrdinaryRewardTag_1001Uis
**Requires:**
- ActivityCasket_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket_RewardMoveWord_01ByName")

function GetActivityCasket_OrdinaryRewardTag_1001Uis(ui)
  local uis = {}
  uis.MoveWord = GetActivityCasket_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket_OrdinaryRewardTag_1002ByName.lua.lua
**Functions:**
- GetActivityCasket_OrdinaryRewardTag_1002Uis
**Requires:**
- ActivityCasket_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket_RewardMoveWord_01ByName")

function GetActivityCasket_OrdinaryRewardTag_1002Uis(ui)
  local uis = {}
  uis.MoveWord = GetActivityCasket_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket_OrdinaryRewardTag_1003ByName.lua.lua
**Functions:**
- GetActivityCasket_OrdinaryRewardTag_1003Uis
**Requires:**
- ActivityCasket_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket_RewardMoveWord_01ByName")

function GetActivityCasket_OrdinaryRewardTag_1003Uis(ui)
  local uis = {}
  uis.MoveWord = GetActivityCasket_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket_OrdinaryRewardTag_1004ByName.lua.lua
**Functions:**
- GetActivityCasket_OrdinaryRewardTag_1004Uis
**Requires:**
- ActivityCasket_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket_RewardMoveWord_01ByName")

function GetActivityCasket_OrdinaryRewardTag_1004Uis(ui)
  local uis = {}
  uis.MoveWord = GetActivityCasket_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket_OrdinaryRewardTag_1005ByName.lua.lua
**Functions:**
- GetActivityCasket_OrdinaryRewardTag_1005Uis
**Requires:**
- ActivityCasket_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket_RewardMoveWord_01ByName")

function GetActivityCasket_OrdinaryRewardTag_1005Uis(ui)
  local uis = {}
  uis.MoveWord = GetActivityCasket_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket_OrdinaryRewardTag_1006ByName.lua.lua
**Functions:**
- GetActivityCasket_OrdinaryRewardTag_1006Uis
**Requires:**
- ActivityCasket_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket_RewardMoveWord_01ByName")

function GetActivityCasket_OrdinaryRewardTag_1006Uis(ui)
  local uis = {}
  uis.MoveWord = GetActivityCasket_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket_OrdinaryRewardTag_1007ByName.lua.lua
**Functions:**
- GetActivityCasket_OrdinaryRewardTag_1007Uis
**Requires:**
- ActivityCasket_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket_RewardMoveWord_01ByName")

function GetActivityCasket_OrdinaryRewardTag_1007Uis(ui)
  local uis = {}
  uis.MoveWord = GetActivityCasket_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket_OrdinaryRewardTag_1008ByName.lua.lua
**Functions:**
- GetActivityCasket_OrdinaryRewardTag_1008Uis
**Requires:**
- ActivityCasket_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket_RewardMoveWord_01ByName")

function GetActivityCasket_OrdinaryRewardTag_1008Uis(ui)
  local uis = {}
  uis.MoveWord = GetActivityCasket_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket_OrdinaryRewardTag_1009ByName.lua.lua
**Functions:**
- GetActivityCasket_OrdinaryRewardTag_1009Uis
**Requires:**
- ActivityCasket_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket_RewardMoveWord_01ByName")

function GetActivityCasket_OrdinaryRewardTag_1009Uis(ui)
  local uis = {}
  uis.MoveWord = GetActivityCasket_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityCasket_OrdinaryRewardTag_1010ByName.lua.lua
**Functions:**
- GetActivityCasket_OrdinaryRewardTag_1010Uis
**Requires:**
- ActivityCasket_RewardMoveWord_01ByName
**Snippet:**
```lua
require("ActivityCasket_RewardMoveWord_01ByName")

function GetActivityCasket_OrdinaryRewardTag_1010Uis(ui)
  local uis = {}
  uis.BoxHolder = ui:GetChild("BoxHolder")
  uis.MoveWord = GetActivityCasket_RewardMoveWord_01Uis(ui:GetChild("MoveWord"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## Activty/a1/ActivityCasket_RecordBtnByName.lua.lua
**Functions:**
- GetActivityCasket_RecordBtnUis
**Snippet:**
```lua
function GetActivityCasket_RecordBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket_RewardMoveWord_01ByName.lua.lua
**Functions:**
- GetActivityCasket_RewardMoveWord_01Uis
**Snippet:**
```lua
function GetActivityCasket_RewardMoveWord_01Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket_RuleBtnByName.lua.lua
**Functions:**
- GetActivityCasket_RuleBtnUis
**Snippet:**
```lua
function GetActivityCasket_RuleBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket_ShopBtnByName.lua.lua
**Functions:**
- GetActivityCasket_ShopBtnUis
**Snippet:**
```lua
function GetActivityCasket_ShopBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TagTxt = ui:GetChild("TagTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityCasket_TagRegion_01ByName.lua.lua
**Functions:**
- GetActivityCasket_TagRegion_01Uis
**Requires:**
- ActivityCasket_OrdinaryRewardTag_1010ByName
- ActivityCasket_OrdinaryRewardTag_1001ByName
- ActivityCasket_OrdinaryRewardTag_1002ByName
- ActivityCasket_OrdinaryRewardTag_1003ByName
- ActivityCasket_OrdinaryRewardTag_1004ByName
- ActivityCasket_OrdinaryRewardTag_1009ByName
- ActivityCasket_OrdinaryRewardTag_1008ByName
- ActivityCasket_OrdinaryRewardTag_1007ByName
- ActivityCasket_OrdinaryRewardTag_1006ByName
- ActivityCasket_OrdinaryRewardTag_1005ByName
**Snippet:**
```lua
require("ActivityCasket_OrdinaryRewardTag_1010ByName")
require("ActivityCasket_OrdinaryRewardTag_1001ByName")
require("ActivityCasket_OrdinaryRewardTag_1002ByName")
require("ActivityCasket_OrdinaryRewardTag_1003ByName")
require("ActivityCasket_OrdinaryRewardTag_1004ByName")
require("ActivityCasket_OrdinaryRewardTag_1009ByName")
require("ActivityCasket_OrdinaryRewardTag_1008ByName")
require("ActivityCasket_OrdinaryRewardTag_1007ByName")
require("ActivityCasket_OrdinaryRewardTag_1006ByName")
require("ActivityCasket_OrdinaryRewardTag_1005ByName")
```

---

## Activty/a1/ActivityChallengeWindow.lua.lua
**Functions:**
- ActivityChallengeWindow.ReInitData
- ActivityChallengeWindow.OnInit
- ActivityChallengeWindow.UpdateInfo
- uis.Main.ChapterList.itemRenderer
- ActivityChallengeWindow.ShoweStage
- ActivityChallengeWindow.StageItemClick
- ActivityChallengeWindow.ShopInfo
- ActivityChallengeWindow.GetChapterPassById
- ActivityChallengeWindow.GetCurStage
- ActivityChallengeWindow.GetFirstChapter
- ActivityChallengeWindow.GetAllChapterId
- ActivityChallengeWindow.InitBtn
- ActivityChallengeWindow.CloseWindow
- ActivityChallengeWindow.OnShown
- ActivityChallengeWindow.OnClose
**Requires:**
- ActivityDungeon1_ChallengeWindowByName
**Snippet:**
```lua
require("ActivityDungeon1_ChallengeWindowByName")
local ActivityChallengeWindow = {}
local uis, contentPane, activityInfo, scrollingTween

function ActivityChallengeWindow.ReInitData()
end

function ActivityChallengeWindow.OnInit(bridgeObj)
  bridgeObj:SetViewAsync(WinResConfig.ActivityChallengeWindow.package, WinResConfig.ActivityChallengeWindow.comName, function(com)
    contentPane = com
```

---

## Activty/a1/ActivityDungeon1001_ActivityDungeonByName.lua.lua
**Functions:**
- GetActivityDungeon1001_ActivityDungeonUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1001_MainTitleByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1001_MainTitleByName")
require("CommonResource_CurrencyReturnByName")

function GetActivityDungeon1001_ActivityDungeonUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.MainTitle = GetActivityDungeon1001_MainTitleUis(ui:GetChild("MainTitle"))
  uis.PlotBtn = ui:GetChild("PlotBtn")
  uis.TaskBtn = ui:GetChild("TaskBtn")
```

---

## Activty/a1/ActivityDungeon1001_ActivityDungeonWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1001_ActivityDungeonWindowUis
**Requires:**
- ActivityDungeon1001_ActivityDungeonByName
**Snippet:**
```lua
require("ActivityDungeon1001_ActivityDungeonByName")

function GetActivityDungeon1001_ActivityDungeonWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1001_ActivityDungeonUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_AddBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_AddBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_AddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_BossBattleByName.lua.lua
**Functions:**
- GetActivityDungeon1001_BossBattleUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1001_BossBattle_InfoByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1001_BossBattle_InfoByName")

function GetActivityDungeon1001_BossBattleUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.Info = GetActivityDungeon1001_BossBattle_InfoUis(ui:GetChild("Info"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a1/ActivityDungeon1001_BossBattleWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1001_BossBattleWindowUis
**Requires:**
- ActivityDungeon1001_BossBattleByName
**Snippet:**
```lua
require("ActivityDungeon1001_BossBattleByName")

function GetActivityDungeon1001_BossBattleWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1001_BossBattleUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_BossBattle_Info1ByName.lua.lua
**Functions:**
- GetActivityDungeon1001_BossBattle_Info1Uis
**Snippet:**
```lua
function GetActivityDungeon1001_BossBattle_Info1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_BossBattle_InfoByName.lua.lua
**Functions:**
- GetActivityDungeon1001_BossBattle_InfoUis
**Requires:**
- ActivityDungeon1001_BossBattle_Info1ByName
**Snippet:**
```lua
require("ActivityDungeon1001_BossBattle_Info1ByName")

function GetActivityDungeon1001_BossBattle_InfoUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = GetActivityDungeon1001_BossBattle_Info1Uis(ui:GetChild("WordTxt"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_BossBattle_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1001_BossBattle_TipsAniUis
**Requires:**
- ActivityDungeon1001_BossBattle_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1001_BossBattle_TipsByName")

function GetActivityDungeon1001_BossBattle_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1001_BossBattle_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_BossBattle_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1001_BossBattle_TipsUis
**Requires:**
- ActivityDungeon1001_BossBattle_TipsRewardByName
**Snippet:**
```lua
require("ActivityDungeon1001_BossBattle_TipsRewardByName")

function GetActivityDungeon1001_BossBattle_TipsUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1001_BossBattle_TipsRewardUis(ui:GetChild("Reward"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.NumberWordTxt = ui:GetChild("NumberWordTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a1/ActivityDungeon1001_BossBattle_TipsRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1001_BossBattle_TipsRewardUis
**Snippet:**
```lua
function GetActivityDungeon1001_BossBattle_TipsRewardUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_BossBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_BossBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_BossBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
```

---

## Activty/a1/ActivityDungeon1001_BuyLevelBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_BuyLevelBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_BuyLevelBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_BuyLevelDes1ByName.lua.lua
**Functions:**
- GetActivityDungeon1001_BuyLevelDes1Uis
**Requires:**
- ActivityDungeon1001_NumberStripByName
- ActivityDungeon1001_BuyPriceNumberByName
**Snippet:**
```lua
require("ActivityDungeon1001_NumberStripByName")
require("ActivityDungeon1001_BuyPriceNumberByName")

function GetActivityDungeon1001_BuyLevelDes1Uis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.NumberStrip = GetActivityDungeon1001_NumberStripUis(ui:GetChild("NumberStrip"))
  uis.BuyPriceNumber = GetActivityDungeon1001_BuyPriceNumberUis(ui:GetChild("BuyPriceNumber"))
```

---

## Activty/a1/ActivityDungeon1001_BuyLevelDes2ByName.lua.lua
**Functions:**
- GetActivityDungeon1001_BuyLevelDes2Uis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1001_BuyLevelDes1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1001_BuyLevelDes1ByName")

function GetActivityDungeon1001_BuyLevelDes2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.BuyLevelDes1 = GetActivityDungeon1001_BuyLevelDes1Uis(ui:GetChild("BuyLevelDes1"))
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.root = ui
```

---

## Activty/a1/ActivityDungeon1001_BuyLevelDesWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1001_BuyLevelDesWindowUis
**Requires:**
- ActivityDungeon1001_BuyLevelDes2ByName
**Snippet:**
```lua
require("ActivityDungeon1001_BuyLevelDes2ByName")

function GetActivityDungeon1001_BuyLevelDesWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1001_BuyLevelDes2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_BuyLevelItemByName.lua.lua
**Functions:**
- GetActivityDungeon1001_BuyLevelItemUis
**Requires:**
- ActivityDungeon1001_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1001_PassReward_AllFrame_EByName")

function GetActivityDungeon1001_BuyLevelItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1001_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_BuyPriceNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1001_BuyPriceNumberUis
**Snippet:**
```lua
function GetActivityDungeon1001_BuyPriceNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_ChallengeByName.lua.lua
**Functions:**
- GetActivityDungeon1001_ChallengeUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1001_MapListByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1001_MapListByName")

function GetActivityDungeon1001_ChallengeUis(ui)
  local uis = {}
  uis.BgList = ui:GetChild("BgList")
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Map = GetActivityDungeon1001_MapListUis(ui:GetChild("Map"))
  uis.ShopBtn = ui:GetChild("ShopBtn")
  uis.ChapterList = ui:GetChild("ChapterList")
```

---

## Activty/a1/ActivityDungeon1001_ChallengeChapterBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_ChallengeChapterBtnUis
**Requires:**
- ActivityDungeon1001_NormalPointLockByName
**Snippet:**
```lua
require("ActivityDungeon1001_NormalPointLockByName")

function GetActivityDungeon1001_ChallengeChapterBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Lock = GetActivityDungeon1001_NormalPointLockUis(ui:GetChild("Lock"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Activty/a1/ActivityDungeon1001_ChallengeShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_ChallengeShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_ChallengeShopBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_ChallengeWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1001_ChallengeWindowUis
**Requires:**
- ActivityDungeon1001_ChallengeByName
**Snippet:**
```lua
require("ActivityDungeon1001_ChallengeByName")

function GetActivityDungeon1001_ChallengeWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1001_ChallengeUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MainTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MainTitleUis
**Snippet:**
```lua
function GetActivityDungeon1001_MainTitleUis(ui)
  local uis = {}
  
  uis.Time1Txt = ui:GetChild("Time1Txt")
  uis.Time2Txt = ui:GetChild("Time2Txt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MapBottom_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MapBottom_1Uis
**Snippet:**
```lua
function GetActivityDungeon1001_MapBottom_1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MapBottom_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MapBottom_2Uis
**Snippet:**
```lua
function GetActivityDungeon1001_MapBottom_2Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MapBottom_3ByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MapBottom_3Uis
**Snippet:**
```lua
function GetActivityDungeon1001_MapBottom_3Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MapListByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MapListUis
**Snippet:**
```lua
function GetActivityDungeon1001_MapListUis(ui)
  local uis = {}
  
  uis.MapList = ui:GetChild("MapList")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Map_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Map_1Uis
**Snippet:**
```lua
function GetActivityDungeon1001_Map_1Uis(ui)
  local uis = {}
  
  uis.Point1Btn = ui:GetChild("Point1Btn")
  uis.Point2Btn = ui:GetChild("Point2Btn")
  uis.Point3Btn = ui:GetChild("Point3Btn")
  uis.Point4Btn = ui:GetChild("Point4Btn")
  uis.Point5Btn = ui:GetChild("Point5Btn")
  uis.Point6Btn = ui:GetChild("Point6Btn")
  uis.Point7Btn = ui:GetChild("Point7Btn")
```

---

## Activty/a1/ActivityDungeon1001_Map_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Map_2Uis
**Snippet:**
```lua
function GetActivityDungeon1001_Map_2Uis(ui)
  local uis = {}
  
  uis.Point1Btn = ui:GetChild("Point1Btn")
  uis.Point2Btn = ui:GetChild("Point2Btn")
  uis.Point3Btn = ui:GetChild("Point3Btn")
  uis.Point4Btn = ui:GetChild("Point4Btn")
  uis.Point5Btn = ui:GetChild("Point5Btn")
  uis.Point6Btn = ui:GetChild("Point6Btn")
  uis.Point7Btn = ui:GetChild("Point7Btn")
```

---

## Activty/a1/ActivityDungeon1001_Map_3ByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Map_3Uis
**Snippet:**
```lua
function GetActivityDungeon1001_Map_3Uis(ui)
  local uis = {}
  
  uis.Point1Btn = ui:GetChild("Point1Btn")
  uis.Point2Btn = ui:GetChild("Point2Btn")
  uis.Point3Btn = ui:GetChild("Point3Btn")
  uis.Point4Btn = ui:GetChild("Point4Btn")
  uis.Point5Btn = ui:GetChild("Point5Btn")
  uis.Point6Btn = ui:GetChild("Point6Btn")
  uis.Point7Btn = ui:GetChild("Point7Btn")
```

---

## Activty/a1/ActivityDungeon1001_MaterialBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MaterialBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1001_MaterialBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
```

---

## Activty/a1/ActivityDungeon1001_MaterialByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MaterialUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1001_Material_BattleNumberByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1001_Material_BattleNumberByName")

function GetActivityDungeon1001_MaterialUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.BattleNumber = GetActivityDungeon1001_Material_BattleNumberUis(ui:GetChild("BattleNumber"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a1/ActivityDungeon1001_MaterialWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MaterialWindowUis
**Requires:**
- ActivityDungeon1001_MaterialByName
**Snippet:**
```lua
require("ActivityDungeon1001_MaterialByName")

function GetActivityDungeon1001_MaterialWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1001_MaterialUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Material_BattleAniByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Material_BattleAniUis
**Requires:**
- ActivityDungeon1001_Material_BattleByName
**Snippet:**
```lua
require("ActivityDungeon1001_Material_BattleByName")

function GetActivityDungeon1001_Material_BattleAniUis(ui)
  local uis = {}
  uis.Battle = GetActivityDungeon1001_Material_BattleUis(ui:GetChild("Battle"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Material_BattleByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Material_BattleUis
**Snippet:**
```lua
function GetActivityDungeon1001_Material_BattleUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Material_BattleNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Material_BattleNumberUis
**Snippet:**
```lua
function GetActivityDungeon1001_Material_BattleNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MaxBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MaxBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_MaxBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MinBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MinBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_MinBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniGameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniGameBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1001_MiniGameBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniGameByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniGameUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1001_MiniMain_TopByName
- ActivityDungeon1001_MiniMain_BottonByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1001_MiniMain_TopByName")
require("ActivityDungeon1001_MiniMain_BottonByName")

function GetActivityDungeon1001_MiniGameUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Top = GetActivityDungeon1001_MiniMain_TopUis(ui:GetChild("Top"))
  uis.Botton = GetActivityDungeon1001_MiniMain_BottonUis(ui:GetChild("Botton"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a1/ActivityDungeon1001_MiniGameStartByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniGameStartUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1001_MiniStart_MidRegionByName
- ActivityDungeon1001_MiniStart_LeftRegionByName
- ActivityDungeon1001_MiniStart_RightRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1001_MiniStart_MidRegionByName")
require("ActivityDungeon1001_MiniStart_LeftRegionByName")
require("ActivityDungeon1001_MiniStart_RightRegionByName")

function GetActivityDungeon1001_MiniGameStartUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.MidRegion = GetActivityDungeon1001_MiniStart_MidRegionUis(ui:GetChild("MidRegion"))
  uis.LeftRegion = GetActivityDungeon1001_MiniStart_LeftRegionUis(ui:GetChild("LeftRegion"))
```

---

## Activty/a1/ActivityDungeon1001_MiniGameStartWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniGameStartWindowUis
**Requires:**
- ActivityDungeon1001_MiniGameStartByName
**Snippet:**
```lua
require("ActivityDungeon1001_MiniGameStartByName")

function GetActivityDungeon1001_MiniGameStartWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1001_MiniGameStartUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniGameWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniGameWindowUis
**Requires:**
- ActivityDungeon1001_MiniGameByName
**Snippet:**
```lua
require("ActivityDungeon1001_MiniGameByName")

function GetActivityDungeon1001_MiniGameWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1001_MiniGameUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniIntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniIntegralUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetActivityDungeon1001_MiniIntegralUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
  return uis
```

---

## Activty/a1/ActivityDungeon1001_MiniIntegralWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniIntegralWindowUis
**Requires:**
- ActivityDungeon1001_MiniIntegralByName
**Snippet:**
```lua
require("ActivityDungeon1001_MiniIntegralByName")

function GetActivityDungeon1001_MiniIntegralWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1001_MiniIntegralUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniIntegral_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniIntegral_TipsAniUis
**Requires:**
- ActivityDungeon1001_MiniIntegral_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1001_MiniIntegral_TipsByName")

function GetActivityDungeon1001_MiniIntegral_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1001_MiniIntegral_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniIntegral_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniIntegral_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1001_MiniIntegral_TipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniMain_BottonByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniMain_BottonUis
**Requires:**
- ActivityDungeon1001_MiniMain_TodayTaskByName
**Snippet:**
```lua
require("ActivityDungeon1001_MiniMain_TodayTaskByName")

function GetActivityDungeon1001_MiniMain_BottonUis(ui)
  local uis = {}
  uis.TaskBtn = ui:GetChild("TaskBtn")
  uis.RecordBtn = ui:GetChild("RecordBtn")
  uis.TodayTask = GetActivityDungeon1001_MiniMain_TodayTaskUis(ui:GetChild("TodayTask"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniMain_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniMain_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1001_MiniMain_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniMain_RecordBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniMain_RecordBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_MiniMain_RecordBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniMain_StartBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniMain_StartBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_MiniMain_StartBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniMain_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniMain_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1001_MiniMain_TaskBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniMain_TodayTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniMain_TodayTaskUis
**Requires:**
- ActivityDungeon1001_PassReward_AllFrame_EByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("ActivityDungeon1001_PassReward_AllFrame_EByName")
require("CommonResource_RedDotByName")

function GetActivityDungeon1001_MiniMain_TodayTaskUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1001_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a1/ActivityDungeon1001_MiniMain_TopByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniMain_TopUis
**Requires:**
- ActivityDungeon1001_MiniMain_IntegralByName
**Snippet:**
```lua
require("ActivityDungeon1001_MiniMain_IntegralByName")

function GetActivityDungeon1001_MiniMain_TopUis(ui)
  local uis = {}
  uis.Integral = GetActivityDungeon1001_MiniMain_IntegralUis(ui:GetChild("Integral"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniStart_CloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniStart_CloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_MiniStart_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniStart_EndAgainBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniStart_EndAgainBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_MiniStart_EndAgainBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniStart_EndCloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniStart_EndCloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_MiniStart_EndCloseBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniStart_EndRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniStart_EndRewardUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetActivityDungeon1001_MiniStart_EndRewardUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.NumberWordTxt = ui:GetChild("NumberWordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.AgainBtn = ui:GetChild("AgainBtn")
  uis.CloseBtn = ui:GetChild("CloseBtn")
```

---

## Activty/a1/ActivityDungeon1001_MiniStart_EndRewardWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniStart_EndRewardWindowUis
**Requires:**
- ActivityDungeon1001_MiniStart_EndRewardByName
**Snippet:**
```lua
require("ActivityDungeon1001_MiniStart_EndRewardByName")

function GetActivityDungeon1001_MiniStart_EndRewardWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1001_MiniStart_EndRewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniStart_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniStart_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1001_MiniStart_IntegralUis(ui)
  local uis = {}
  
  uis.NumberWordTxt = ui:GetChild("NumberWordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.NumberWord1Txt = ui:GetChild("NumberWord1Txt")
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniStart_LeftMoveBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniStart_LeftMoveBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_MiniStart_LeftMoveBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniStart_LeftRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniStart_LeftRegionUis
**Requires:**
- ActivityDungeon1001_MiniStart_IntegralByName
**Snippet:**
```lua
require("ActivityDungeon1001_MiniStart_IntegralByName")

function GetActivityDungeon1001_MiniStart_LeftRegionUis(ui)
  local uis = {}
  uis.Integral = GetActivityDungeon1001_MiniStart_IntegralUis(ui:GetChild("Integral"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.LeftMoveBtn = ui:GetChild("LeftMoveBtn")
  uis.RightMoveBtn = ui:GetChild("RightMoveBtn")
  uis.root = ui
  return uis
```

---

## Activty/a1/ActivityDungeon1001_MiniStart_MidArticleByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniStart_MidArticleUis
**Snippet:**
```lua
function GetActivityDungeon1001_MiniStart_MidArticleUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniStart_MidRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniStart_MidRegionUis
**Snippet:**
```lua
function GetActivityDungeon1001_MiniStart_MidRegionUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniStart_RightMoveBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniStart_RightMoveBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_MiniStart_RightMoveBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniStart_RightNextByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniStart_RightNextUis
**Snippet:**
```lua
function GetActivityDungeon1001_MiniStart_RightNextUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniStart_RightPutBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniStart_RightPutBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_MiniStart_RightPutBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniStart_RightRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniStart_RightRegionUis
**Requires:**
- ActivityDungeon1001_MiniStart_RightNextByName
**Snippet:**
```lua
require("ActivityDungeon1001_MiniStart_RightNextByName")

function GetActivityDungeon1001_MiniStart_RightRegionUis(ui)
  local uis = {}
  uis.Next = GetActivityDungeon1001_MiniStart_RightNextUis(ui:GetChild("Next"))
  uis.PutBtn = ui:GetChild("PutBtn")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniTaskUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1001_MiniTask_IntegralByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1001_MiniTask_IntegralByName")

function GetActivityDungeon1001_MiniTaskUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Integral = GetActivityDungeon1001_MiniTask_IntegralUis(ui:GetChild("Integral"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a1/ActivityDungeon1001_MiniTaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniTaskWindowUis
**Requires:**
- ActivityDungeon1001_MiniTaskByName
**Snippet:**
```lua
require("ActivityDungeon1001_MiniTaskByName")

function GetActivityDungeon1001_MiniTaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1001_MiniTaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniTask_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniTask_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1001_MiniTask_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniTask_RewardItemByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniTask_RewardItemUis
**Snippet:**
```lua
function GetActivityDungeon1001_MiniTask_RewardItemUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniTask_RewardItemGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniTask_RewardItemGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_MiniTask_RewardItemGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniTask_TipsAniUis
**Requires:**
- ActivityDungeon1001_MiniTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1001_MiniTask_TipsByName")

function GetActivityDungeon1001_MiniTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1001_MiniTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_MiniTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1001_MiniTask_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1001_MiniTask_TipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.ItemList = ui:GetChild("ItemList")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a1/ActivityDungeon1001_NormalBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_NormalBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_NormalBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_NormalPoint1BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_NormalPoint1BtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_NormalPoint1BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_NormalPoint2BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_NormalPoint2BtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_NormalPoint2BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_NormalPointBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_NormalPointBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_NormalPointBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_NormalPointLockByName.lua.lua
**Functions:**
- GetActivityDungeon1001_NormalPointLockUis
**Snippet:**
```lua
function GetActivityDungeon1001_NormalPointLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_NumberStripByName.lua.lua
**Functions:**
- GetActivityDungeon1001_NumberStripUis
**Snippet:**
```lua
function GetActivityDungeon1001_NumberStripUis(ui)
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

## Activty/a1/ActivityDungeon1001_PassBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1001_PassBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_PassClothes_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassClothes_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_PassClothes_BuyBtnUis(ui)
  local uis = {}
  
  uis.PriceTxt = ui:GetChild("PriceTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_PassClothes_BuyRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassClothes_BuyRewardUis
**Snippet:**
```lua
function GetActivityDungeon1001_PassClothes_BuyRewardUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_PassClothes_CardQBByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassClothes_CardQBUis
**Snippet:**
```lua
function GetActivityDungeon1001_PassClothes_CardQBUis(ui)
  local uis = {}
  
  uis.QBHolder = ui:GetChild("QBHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_PassClothes_ClothseRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassClothes_ClothseRegionUis
**Requires:**
- ActivityDungeon1001_PassClothes_WordByName
- ActivityDungeon1001_PassClothes_CardQBByName
- ActivityDungeon1001_PassClothes_BuyRewardByName
**Snippet:**
```lua
require("ActivityDungeon1001_PassClothes_WordByName")
require("ActivityDungeon1001_PassClothes_CardQBByName")
require("ActivityDungeon1001_PassClothes_BuyRewardByName")

function GetActivityDungeon1001_PassClothes_ClothseRegionUis(ui)
  local uis = {}
  uis.Word = GetActivityDungeon1001_PassClothes_WordUis(ui:GetChild("Word"))
  uis.CardQB = GetActivityDungeon1001_PassClothes_CardQBUis(ui:GetChild("CardQB"))
  uis.BuyReward = GetActivityDungeon1001_PassClothes_BuyRewardUis(ui:GetChild("BuyReward"))
  uis.BuyBtn = ui:GetChild("BuyBtn")
```

---

## Activty/a1/ActivityDungeon1001_PassClothes_NameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassClothes_NameBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_PassClothes_NameBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_PassClothes_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassClothes_WordUis
**Snippet:**
```lua
function GetActivityDungeon1001_PassClothes_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_PassportByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassportUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1001_PassReward_RewardRegionByName
- ActivityDungeon1001_PassTask_TaskRegionByName
- ActivityDungeon1001_PassClothes_ClothseRegionByName
- ActivityDungeon1001_Passport_LevelByName
- ActivityDungeon1001_Sign_TimeByName
- ActivityDungeon1001_Passport_TabRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1001_PassReward_RewardRegionByName")
require("ActivityDungeon1001_PassTask_TaskRegionByName")
require("ActivityDungeon1001_PassClothes_ClothseRegionByName")
require("ActivityDungeon1001_Passport_LevelByName")
require("ActivityDungeon1001_Sign_TimeByName")
require("ActivityDungeon1001_Passport_TabRegionByName")

function GetActivityDungeon1001_PassportUis(ui)
  local uis = {}
```

---

## Activty/a1/ActivityDungeon1001_PassportUp_LevelUpBgByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassportUp_LevelUpBgUis
**Snippet:**
```lua
function GetActivityDungeon1001_PassportUp_LevelUpBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_PassportUp_LevelUpTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassportUp_LevelUpTipsUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1001_PassportUp_LevelUpBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1001_PassportUp_LevelUpBgByName")

function GetActivityDungeon1001_PassportUp_LevelUpTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.LevelUpBg = GetActivityDungeon1001_PassportUp_LevelUpBgUis(ui:GetChild("LevelUpBg"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
```

---

## Activty/a1/ActivityDungeon1001_PassportUp_LevelUpTipsWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassportUp_LevelUpTipsWindowUis
**Requires:**
- ActivityDungeon1001_PassportUp_LevelUpTipsByName
**Snippet:**
```lua
require("ActivityDungeon1001_PassportUp_LevelUpTipsByName")

function GetActivityDungeon1001_PassportUp_LevelUpTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1001_PassportUp_LevelUpTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_PassportWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassportWindowUis
**Requires:**
- ActivityDungeon1001_PassportByName
**Snippet:**
```lua
require("ActivityDungeon1001_PassportByName")

function GetActivityDungeon1001_PassportWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1001_PassportUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Passport_AllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Passport_AllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_Passport_AllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Passport_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Passport_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_Passport_BuyBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Passport_ExpProgressBarByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Passport_ExpProgressBarUis
**Requires:**
- ActivityDungeon1001_Passport_ExpProgressFillByName
**Snippet:**
```lua
require("ActivityDungeon1001_Passport_ExpProgressFillByName")

function GetActivityDungeon1001_Passport_ExpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetActivityDungeon1001_Passport_ExpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Passport_ExpProgressFillByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Passport_ExpProgressFillUis
**Snippet:**
```lua
function GetActivityDungeon1001_Passport_ExpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Passport_LevelByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Passport_LevelUis
**Snippet:**
```lua
function GetActivityDungeon1001_Passport_LevelUis(ui)
  local uis = {}
  
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.ExpNumberTxt = ui:GetChild("ExpNumberTxt")
  uis.ExpProgressBar = ui:GetChild("ExpProgressBar")
  uis.LevelBuyBtn = ui:GetChild("LevelBuyBtn")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Passport_TabBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Passport_TabBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1001_Passport_TabBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## Activty/a1/ActivityDungeon1001_Passport_TabRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Passport_TabRegionUis
**Snippet:**
```lua
function GetActivityDungeon1001_Passport_TabRegionUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_PassReward_AllFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassReward_AllFrame_EUis
**Requires:**
- ActivityDungeon1001_PassReward_ItemFrame_EByName
- ActivityDungeon1001_PassReward_CardFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1001_PassReward_ItemFrame_EByName")
require("ActivityDungeon1001_PassReward_CardFrame_EByName")

function GetActivityDungeon1001_PassReward_AllFrame_EUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1001_PassReward_ItemFrame_EUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1001_PassReward_CardFrame_EUis(ui:GetChild("CardFrame"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## Activty/a1/ActivityDungeon1001_PassReward_AllFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassReward_AllFrame_MUis
**Requires:**
- ActivityDungeon1001_PassReward_ItemFrame_MByName
- ActivityDungeon1001_PassReward_CardFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1001_PassReward_ItemFrame_MByName")
require("ActivityDungeon1001_PassReward_CardFrame_MByName")

function GetActivityDungeon1001_PassReward_AllFrame_MUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1001_PassReward_ItemFrame_MUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1001_PassReward_CardFrame_MUis(ui:GetChild("CardFrame"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityDungeon1001_PassReward_CardFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassReward_CardFrame_EUis
**Requires:**
- ActivityDungeon1001_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1001_PassReward_ItemCardPicByName")

function GetActivityDungeon1001_PassReward_CardFrame_EUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1001_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a1/ActivityDungeon1001_PassReward_CardFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassReward_CardFrame_MUis
**Requires:**
- ActivityDungeon1001_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1001_PassReward_ItemCardPicByName")

function GetActivityDungeon1001_PassReward_CardFrame_MUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1001_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a1/ActivityDungeon1001_PassReward_EndTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassReward_EndTwoUis
**Requires:**
- ActivityDungeon1001_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1001_PassReward_AllFrame_EByName")

function GetActivityDungeon1001_PassReward_EndTwoUis(ui)
  local uis = {}
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.Item1 = GetActivityDungeon1001_PassReward_AllFrame_EUis(ui:GetChild("Item1"))
  uis.Item2 = GetActivityDungeon1001_PassReward_AllFrame_EUis(ui:GetChild("Item2"))
  uis.root = ui
```

---

## Activty/a1/ActivityDungeon1001_PassReward_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassReward_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1001_PassReward_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_PassReward_ItemFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassReward_ItemFrame_EUis
**Snippet:**
```lua
function GetActivityDungeon1001_PassReward_ItemFrame_EUis(ui)
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

## Activty/a1/ActivityDungeon1001_PassReward_ItemFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassReward_ItemFrame_MUis
**Snippet:**
```lua
function GetActivityDungeon1001_PassReward_ItemFrame_MUis(ui)
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

## Activty/a1/ActivityDungeon1001_PassReward_LevelTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassReward_LevelTitleUis
**Snippet:**
```lua
function GetActivityDungeon1001_PassReward_LevelTitleUis(ui)
  local uis = {}
  
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_PassReward_MiddleRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassReward_MiddleRegionUis
**Snippet:**
```lua
function GetActivityDungeon1001_PassReward_MiddleRegionUis(ui)
  local uis = {}
  
  uis.MiddleList = ui:GetChild("MiddleList")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_PassReward_MidTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassReward_MidTwoUis
**Requires:**
- ActivityDungeon1001_PassReward_MidTwoItemByName
- ActivityDungeon1001_PassReward_LevelTitleByName
**Snippet:**
```lua
require("ActivityDungeon1001_PassReward_MidTwoItemByName")
require("ActivityDungeon1001_PassReward_LevelTitleByName")

function GetActivityDungeon1001_PassReward_MidTwoUis(ui)
  local uis = {}
  uis.Reward1 = GetActivityDungeon1001_PassReward_MidTwoItemUis(ui:GetChild("Reward1"))
  uis.Reward2 = GetActivityDungeon1001_PassReward_MidTwoItemUis(ui:GetChild("Reward2"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Title = GetActivityDungeon1001_PassReward_LevelTitleUis(ui:GetChild("Title"))
```

---

## Activty/a1/ActivityDungeon1001_PassReward_MidTwoItemByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassReward_MidTwoItemUis
**Requires:**
- ActivityDungeon1001_PassReward_AllFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1001_PassReward_AllFrame_MByName")

function GetActivityDungeon1001_PassReward_MidTwoItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1001_PassReward_AllFrame_MUis(ui:GetChild("Item"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_PassReward_PicByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassReward_PicUis
**Snippet:**
```lua
function GetActivityDungeon1001_PassReward_PicUis(ui)
  local uis = {}
  
  uis.BuyTxt = ui:GetChild("BuyTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_PassReward_RewardRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassReward_RewardRegionUis
**Requires:**
- ActivityDungeon1001_PassReward_MiddleRegionByName
- ActivityDungeon1001_PassReward_StartTwoByName
- ActivityDungeon1001_PassReward_EndTwoByName
**Snippet:**
```lua
require("ActivityDungeon1001_PassReward_MiddleRegionByName")
require("ActivityDungeon1001_PassReward_StartTwoByName")
require("ActivityDungeon1001_PassReward_EndTwoByName")

function GetActivityDungeon1001_PassReward_RewardRegionUis(ui)
  local uis = {}
  uis.MiddleList = GetActivityDungeon1001_PassReward_MiddleRegionUis(ui:GetChild("MiddleList"))
  uis.StartTwo = GetActivityDungeon1001_PassReward_StartTwoUis(ui:GetChild("StartTwo"))
  uis.EndTwo = GetActivityDungeon1001_PassReward_EndTwoUis(ui:GetChild("EndTwo"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a1/ActivityDungeon1001_PassReward_StartTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassReward_StartTwoUis
**Requires:**
- ActivityDungeon1001_PassReward_PicByName
**Snippet:**
```lua
require("ActivityDungeon1001_PassReward_PicByName")

function GetActivityDungeon1001_PassReward_StartTwoUis(ui)
  local uis = {}
  uis.Pic = GetActivityDungeon1001_PassReward_PicUis(ui:GetChild("Pic"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_PassTask_TaskRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassTask_TaskRegionUis
**Requires:**
- ActivityDungeon1001_TaskMaxByName
**Snippet:**
```lua
require("ActivityDungeon1001_TaskMaxByName")

function GetActivityDungeon1001_PassTask_TaskRegionUis(ui)
  local uis = {}
  uis.TipsList = ui:GetChild("TipsList")
  uis.Max = GetActivityDungeon1001_TaskMaxUis(ui:GetChild("Max"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_PassTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassTask_TipsAniUis
**Requires:**
- ActivityDungeon1001_PassTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1001_PassTask_TipsByName")

function GetActivityDungeon1001_PassTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1001_PassTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_PassTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassTask_TipsUis
**Requires:**
- ActivityDungeon1001_PassTask_TipsIntegralByName
**Snippet:**
```lua
require("ActivityDungeon1001_PassTask_TipsIntegralByName")

function GetActivityDungeon1001_PassTask_TipsUis(ui)
  local uis = {}
  uis.ProgressTxt = ui:GetChild("ProgressTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Integral = GetActivityDungeon1001_PassTask_TipsIntegralUis(ui:GetChild("Integral"))
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a1/ActivityDungeon1001_PassTask_TipsIntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PassTask_TipsIntegralUis
**Snippet:**
```lua
function GetActivityDungeon1001_PassTask_TipsIntegralUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_PlotBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PlotBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_PlotBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_PlotByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PlotUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1001_Plot_WordByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1001_Plot_WordByName")

function GetActivityDungeon1001_PlotUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Word = GetActivityDungeon1001_Plot_WordUis(ui:GetChild("Word"))
  uis.PlotList = ui:GetChild("PlotList")
  uis.ProspectBtn = ui:GetChild("ProspectBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a1/ActivityDungeon1001_PlotWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1001_PlotWindowUis
**Requires:**
- ActivityDungeon1001_PlotByName
**Snippet:**
```lua
require("ActivityDungeon1001_PlotByName")

function GetActivityDungeon1001_PlotWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1001_PlotUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Plot_ProspectBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Plot_ProspectBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_Plot_ProspectBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Plot_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Plot_TipsAniUis
**Requires:**
- ActivityDungeon1001_Plot_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1001_Plot_TipsByName")

function GetActivityDungeon1001_Plot_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1001_Plot_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Plot_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Plot_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1001_Plot_TipsUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Plot_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Plot_WordUis
**Snippet:**
```lua
function GetActivityDungeon1001_Plot_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_ReduceBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_ReduceBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_ReduceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_ShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_ShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_ShopBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_ShopByName.lua.lua
**Functions:**
- GetActivityDungeon1001_ShopUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1001_Shop_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1001_Shop_TimeByName")

function GetActivityDungeon1001_ShopUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Time = GetActivityDungeon1001_Shop_TimeUis(ui:GetChild("Time"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a1/ActivityDungeon1001_ShopWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1001_ShopWindowUis
**Requires:**
- ActivityDungeon1001_ShopByName
**Snippet:**
```lua
require("ActivityDungeon1001_ShopByName")

function GetActivityDungeon1001_ShopWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1001_ShopUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Shop_CardHeadBgByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Shop_CardHeadBgUis
**Snippet:**
```lua
function GetActivityDungeon1001_Shop_CardHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Shop_ItemAniByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Shop_ItemAniUis
**Requires:**
- ActivityDungeon1001_Shop_ItemByName
**Snippet:**
```lua
require("ActivityDungeon1001_Shop_ItemByName")

function GetActivityDungeon1001_Shop_ItemAniUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1001_Shop_ItemUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Shop_ItemBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Shop_ItemBtnUis
**Requires:**
- ActivityDungeon1001_Shop_CardHeadBgByName
- ActivityDungeon1001_Shop_ItemNumberByName
- ActivityDungeon1001_Shop_UseMarkByName
**Snippet:**
```lua
require("ActivityDungeon1001_Shop_CardHeadBgByName")
require("ActivityDungeon1001_Shop_ItemNumberByName")
require("ActivityDungeon1001_Shop_UseMarkByName")

function GetActivityDungeon1001_Shop_ItemBtnUis(ui)
  local uis = {}
  uis.CardHeadBg = GetActivityDungeon1001_Shop_CardHeadBgUis(ui:GetChild("CardHeadBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.ItemNumber = GetActivityDungeon1001_Shop_ItemNumberUis(ui:GetChild("ItemNumber"))
```

---

## Activty/a1/ActivityDungeon1001_Shop_ItemByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Shop_ItemUis
**Requires:**
- ActivityDungeon1001_Shop_SellOutByName
**Snippet:**
```lua
require("ActivityDungeon1001_Shop_SellOutByName")

function GetActivityDungeon1001_Shop_ItemUis(ui)
  local uis = {}
  uis.ItemBtn = ui:GetChild("ItemBtn")
  uis.SellOut = GetActivityDungeon1001_Shop_SellOutUis(ui:GetChild("SellOut"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Shop_ItemNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Shop_ItemNumberUis
**Snippet:**
```lua
function GetActivityDungeon1001_Shop_ItemNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Shop_ItemRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Shop_ItemRegionUis
**Requires:**
- ActivityDungeon1001_Shop_TitleByName
**Snippet:**
```lua
require("ActivityDungeon1001_Shop_TitleByName")

function GetActivityDungeon1001_Shop_ItemRegionUis(ui)
  local uis = {}
  uis.ShopTitle = GetActivityDungeon1001_Shop_TitleUis(ui:GetChild("ShopTitle"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Shop_SellOutByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Shop_SellOutUis
**Snippet:**
```lua
function GetActivityDungeon1001_Shop_SellOutUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Shop_StarByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Shop_StarUis
**Snippet:**
```lua
function GetActivityDungeon1001_Shop_StarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Shop_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Shop_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1001_Shop_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Shop_TitleByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Shop_TitleUis
**Snippet:**
```lua
function GetActivityDungeon1001_Shop_TitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Shop_UseMarkByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Shop_UseMarkUis
**Snippet:**
```lua
function GetActivityDungeon1001_Shop_UseMarkUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_SignBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_SignBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1001_SignBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_SignByName.lua.lua
**Functions:**
- GetActivityDungeon1001_SignUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1001_Sign_RewardListByName
- ActivityDungeon1001_Sign_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1001_Sign_RewardListByName")
require("ActivityDungeon1001_Sign_TimeByName")

function GetActivityDungeon1001_SignUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.RewardList = GetActivityDungeon1001_Sign_RewardListUis(ui:GetChild("RewardList"))
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.Time = GetActivityDungeon1001_Sign_TimeUis(ui:GetChild("Time"))
```

---

## Activty/a1/ActivityDungeon1001_SignWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1001_SignWindowUis
**Requires:**
- ActivityDungeon1001_SignByName
**Snippet:**
```lua
require("ActivityDungeon1001_SignByName")

function GetActivityDungeon1001_SignWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1001_SignUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Sign_AllFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Sign_AllFrameUis
**Requires:**
- ActivityDungeon1001_Sign_ItemFrameByName
- ActivityDungeon1001_Sign_CardFrameByName
**Snippet:**
```lua
require("ActivityDungeon1001_Sign_ItemFrameByName")
require("ActivityDungeon1001_Sign_CardFrameByName")

function GetActivityDungeon1001_Sign_AllFrameUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1001_Sign_ItemFrameUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1001_Sign_CardFrameUis(ui:GetChild("CardFrame"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityDungeon1001_Sign_CardFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Sign_CardFrameUis
**Requires:**
- ActivityDungeon1001_Sign_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1001_Sign_ItemCardPicByName")

function GetActivityDungeon1001_Sign_CardFrameUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1001_Sign_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a1/ActivityDungeon1001_Sign_GetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Sign_GetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_Sign_GetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Sign_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Sign_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1001_Sign_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Sign_ItemFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Sign_ItemFrameUis
**Snippet:**
```lua
function GetActivityDungeon1001_Sign_ItemFrameUis(ui)
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

## Activty/a1/ActivityDungeon1001_Sign_RewardAniByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Sign_RewardAniUis
**Requires:**
- ActivityDungeon1001_Sign_RewardByName
**Snippet:**
```lua
require("ActivityDungeon1001_Sign_RewardByName")

function GetActivityDungeon1001_Sign_RewardAniUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1001_Sign_RewardUis(ui:GetChild("Reward"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Sign_RewardByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Sign_RewardUis
**Requires:**
- ActivityDungeon1001_Sign_AllFrameByName
**Snippet:**
```lua
require("ActivityDungeon1001_Sign_AllFrameByName")

function GetActivityDungeon1001_Sign_RewardUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1001_Sign_AllFrameUis(ui:GetChild("Item"))
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Sign_RewardListByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Sign_RewardListUis
**Snippet:**
```lua
function GetActivityDungeon1001_Sign_RewardListUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_Sign_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1001_Sign_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1001_Sign_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_TaskAllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_TaskAllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_TaskAllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1001_TaskBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_TaskByName.lua.lua
**Functions:**
- GetActivityDungeon1001_TaskUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1001_TaskTitleByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1001_TaskTitleByName")

function GetActivityDungeon1001_TaskUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TaskTitle = GetActivityDungeon1001_TaskTitleUis(ui:GetChild("TaskTitle"))
  uis.TaskTipsList = ui:GetChild("TaskTipsList")
  uis.AllGetBtn = ui:GetChild("AllGetBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a1/ActivityDungeon1001_TaskGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1001_TaskGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1001_TaskGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_TaskMaxByName.lua.lua
**Functions:**
- GetActivityDungeon1001_TaskMaxUis
**Snippet:**
```lua
function GetActivityDungeon1001_TaskMaxUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_TaskProgressByName.lua.lua
**Functions:**
- GetActivityDungeon1001_TaskProgressUis
**Snippet:**
```lua
function GetActivityDungeon1001_TaskProgressUis(ui)
  local uis = {}
  
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_TaskTipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1001_TaskTipsAniUis
**Requires:**
- ActivityDungeon1001_TaskTipsByName
**Snippet:**
```lua
require("ActivityDungeon1001_TaskTipsByName")

function GetActivityDungeon1001_TaskTipsAniUis(ui)
  local uis = {}
  uis.TaskTips = GetActivityDungeon1001_TaskTipsUis(ui:GetChild("TaskTips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_TaskTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1001_TaskTipsUis
**Requires:**
- ActivityDungeon1001_TaskProgressByName
**Snippet:**
```lua
require("ActivityDungeon1001_TaskProgressByName")

function GetActivityDungeon1001_TaskTipsUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.RewardList = ui:GetChild("RewardList")
  uis.TaskProgress = GetActivityDungeon1001_TaskProgressUis(ui:GetChild("TaskProgress"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a1/ActivityDungeon1001_TaskTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1001_TaskTitleUis
**Snippet:**
```lua
function GetActivityDungeon1001_TaskTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1001_TaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1001_TaskWindowUis
**Requires:**
- ActivityDungeon1001_TaskByName
**Snippet:**
```lua
require("ActivityDungeon1001_TaskByName")

function GetActivityDungeon1001_TaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1001_TaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_ActivityDungeonByName.lua.lua
**Functions:**
- GetActivityDungeon1_ActivityDungeonUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1_MainTitleByName
- CommonResource_CurrencyReturnByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1_MainTitleByName")
require("CommonResource_CurrencyReturnByName")

function GetActivityDungeon1_ActivityDungeonUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.PlotBtn = ui:GetChild("PlotBtn")
  uis.TaskBtn = ui:GetChild("TaskBtn")
  uis.ShopBtn = ui:GetChild("ShopBtn")
```

---

## Activty/a1/ActivityDungeon1_ActivityDungeonWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1_ActivityDungeonWindowUis
**Requires:**
- ActivityDungeon1_ActivityDungeonByName
**Snippet:**
```lua
require("ActivityDungeon1_ActivityDungeonByName")

function GetActivityDungeon1_ActivityDungeonWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1_ActivityDungeonUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_AddBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_AddBtnUis
**Snippet:**
```lua
function GetActivityDungeon1_AddBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_BossBattleByName.lua.lua
**Functions:**
- GetActivityDungeon1_BossBattleUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1_BossBattle_InfoByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1_BossBattle_InfoByName")

function GetActivityDungeon1_BossBattleUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.Info = GetActivityDungeon1_BossBattle_InfoUis(ui:GetChild("Info"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a1/ActivityDungeon1_BossBattleWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1_BossBattleWindowUis
**Requires:**
- ActivityDungeon1_BossBattleByName
**Snippet:**
```lua
require("ActivityDungeon1_BossBattleByName")

function GetActivityDungeon1_BossBattleWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1_BossBattleUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_BossBattle_Info1ByName.lua.lua
**Functions:**
- GetActivityDungeon1_BossBattle_Info1Uis
**Snippet:**
```lua
function GetActivityDungeon1_BossBattle_Info1Uis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_BossBattle_InfoByName.lua.lua
**Functions:**
- GetActivityDungeon1_BossBattle_InfoUis
**Requires:**
- ActivityDungeon1_BossBattle_Info1ByName
**Snippet:**
```lua
require("ActivityDungeon1_BossBattle_Info1ByName")

function GetActivityDungeon1_BossBattle_InfoUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.WordTxt = GetActivityDungeon1_BossBattle_Info1Uis(ui:GetChild("WordTxt"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_BossBattle_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1_BossBattle_TipsAniUis
**Requires:**
- ActivityDungeon1_BossBattle_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1_BossBattle_TipsByName")

function GetActivityDungeon1_BossBattle_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1_BossBattle_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_BossBattle_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1_BossBattle_TipsUis
**Requires:**
- ActivityDungeon1_BossBattle_TipsRewardByName
**Snippet:**
```lua
require("ActivityDungeon1_BossBattle_TipsRewardByName")

function GetActivityDungeon1_BossBattle_TipsUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1_BossBattle_TipsRewardUis(ui:GetChild("Reward"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.NumberWordTxt = ui:GetChild("NumberWordTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a1/ActivityDungeon1_BossBattle_TipsRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1_BossBattle_TipsRewardUis
**Snippet:**
```lua
function GetActivityDungeon1_BossBattle_TipsRewardUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_BossBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_BossBtnUis
**Snippet:**
```lua
function GetActivityDungeon1_BossBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
```

---

## Activty/a1/ActivityDungeon1_BuyLevelBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_BuyLevelBtnUis
**Snippet:**
```lua
function GetActivityDungeon1_BuyLevelBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_BuyLevelDes1ByName.lua.lua
**Functions:**
- GetActivityDungeon1_BuyLevelDes1Uis
**Requires:**
- ActivityDungeon1_NumberStripByName
- ActivityDungeon1_BuyPriceNumberByName
**Snippet:**
```lua
require("ActivityDungeon1_NumberStripByName")
require("ActivityDungeon1_BuyPriceNumberByName")

function GetActivityDungeon1_BuyLevelDes1Uis(ui)
  local uis = {}
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.NumberStrip = GetActivityDungeon1_NumberStripUis(ui:GetChild("NumberStrip"))
  uis.BuyPriceNumber = GetActivityDungeon1_BuyPriceNumberUis(ui:GetChild("BuyPriceNumber"))
```

---

## Activty/a1/ActivityDungeon1_BuyLevelDes2ByName.lua.lua
**Functions:**
- GetActivityDungeon1_BuyLevelDes2Uis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1_BuyLevelDes1ByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1_BuyLevelDes1ByName")

function GetActivityDungeon1_BuyLevelDes2Uis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.BuyLevelDes1 = GetActivityDungeon1_BuyLevelDes1Uis(ui:GetChild("BuyLevelDes1"))
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.root = ui
```

---

## Activty/a1/ActivityDungeon1_BuyLevelDesWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1_BuyLevelDesWindowUis
**Requires:**
- ActivityDungeon1_BuyLevelDes2ByName
**Snippet:**
```lua
require("ActivityDungeon1_BuyLevelDes2ByName")

function GetActivityDungeon1_BuyLevelDesWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1_BuyLevelDes2Uis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_BuyLevelItemByName.lua.lua
**Functions:**
- GetActivityDungeon1_BuyLevelItemUis
**Requires:**
- ActivityDungeon1_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1_PassReward_AllFrame_EByName")

function GetActivityDungeon1_BuyLevelItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_BuyPriceNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1_BuyPriceNumberUis
**Snippet:**
```lua
function GetActivityDungeon1_BuyPriceNumberUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_ChallengeByName.lua.lua
**Functions:**
- GetActivityDungeon1_ChallengeUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1_MapListByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1_MapListByName")

function GetActivityDungeon1_ChallengeUis(ui)
  local uis = {}
  uis.BgList = ui:GetChild("BgList")
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Map = GetActivityDungeon1_MapListUis(ui:GetChild("Map"))
  uis.ShopBtn = ui:GetChild("ShopBtn")
  uis.ChapterList = ui:GetChild("ChapterList")
```

---

## Activty/a1/ActivityDungeon1_ChallengeChapterBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_ChallengeChapterBtnUis
**Requires:**
- ActivityDungeon1_NormalPointLockByName
**Snippet:**
```lua
require("ActivityDungeon1_NormalPointLockByName")

function GetActivityDungeon1_ChallengeChapterBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Lock = GetActivityDungeon1_NormalPointLockUis(ui:GetChild("Lock"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Activty/a1/ActivityDungeon1_ChallengeShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_ChallengeShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1_ChallengeShopBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_ChallengeWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1_ChallengeWindowUis
**Requires:**
- ActivityDungeon1_ChallengeByName
**Snippet:**
```lua
require("ActivityDungeon1_ChallengeByName")

function GetActivityDungeon1_ChallengeWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1_ChallengeUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MainTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1_MainTitleUis
**Snippet:**
```lua
function GetActivityDungeon1_MainTitleUis(ui)
  local uis = {}
  
  uis.Time1Txt = ui:GetChild("Time1Txt")
  uis.Time2Txt = ui:GetChild("Time2Txt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MapBottom_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1_MapBottom_1Uis
**Snippet:**
```lua
function GetActivityDungeon1_MapBottom_1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MapBottom_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1_MapBottom_2Uis
**Snippet:**
```lua
function GetActivityDungeon1_MapBottom_2Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MapListByName.lua.lua
**Functions:**
- GetActivityDungeon1_MapListUis
**Snippet:**
```lua
function GetActivityDungeon1_MapListUis(ui)
  local uis = {}
  
  uis.MapList = ui:GetChild("MapList")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Map_1ByName.lua.lua
**Functions:**
- GetActivityDungeon1_Map_1Uis
**Snippet:**
```lua
function GetActivityDungeon1_Map_1Uis(ui)
  local uis = {}
  
  uis.Point1Btn = ui:GetChild("Point1Btn")
  uis.Point2Btn = ui:GetChild("Point2Btn")
  uis.Point3Btn = ui:GetChild("Point3Btn")
  uis.Point4Btn = ui:GetChild("Point4Btn")
  uis.Point5Btn = ui:GetChild("Point5Btn")
  uis.Point6Btn = ui:GetChild("Point6Btn")
  uis.Point7Btn = ui:GetChild("Point7Btn")
```

---

## Activty/a1/ActivityDungeon1_Map_2ByName.lua.lua
**Functions:**
- GetActivityDungeon1_Map_2Uis
**Snippet:**
```lua
function GetActivityDungeon1_Map_2Uis(ui)
  local uis = {}
  
  uis.Point1Btn = ui:GetChild("Point1Btn")
  uis.Point2Btn = ui:GetChild("Point2Btn")
  uis.Point3Btn = ui:GetChild("Point3Btn")
  uis.Point4Btn = ui:GetChild("Point4Btn")
  uis.Point5Btn = ui:GetChild("Point5Btn")
  uis.Point6Btn = ui:GetChild("Point6Btn")
  uis.Point7Btn = ui:GetChild("Point7Btn")
```

---

## Activty/a1/ActivityDungeon1_MaterialBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_MaterialBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1_MaterialBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
```

---

## Activty/a1/ActivityDungeon1_MaterialByName.lua.lua
**Functions:**
- GetActivityDungeon1_MaterialUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1_Material_BattleNumberByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1_Material_BattleNumberByName")

function GetActivityDungeon1_MaterialUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.BattleList = ui:GetChild("BattleList")
  uis.BattleNumber = GetActivityDungeon1_Material_BattleNumberUis(ui:GetChild("BattleNumber"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
```

---

## Activty/a1/ActivityDungeon1_MaterialWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1_MaterialWindowUis
**Requires:**
- ActivityDungeon1_MaterialByName
**Snippet:**
```lua
require("ActivityDungeon1_MaterialByName")

function GetActivityDungeon1_MaterialWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1_MaterialUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Material_BattleAniByName.lua.lua
**Functions:**
- GetActivityDungeon1_Material_BattleAniUis
**Requires:**
- ActivityDungeon1_Material_BattleByName
**Snippet:**
```lua
require("ActivityDungeon1_Material_BattleByName")

function GetActivityDungeon1_Material_BattleAniUis(ui)
  local uis = {}
  uis.Battle = GetActivityDungeon1_Material_BattleUis(ui:GetChild("Battle"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Material_BattleByName.lua.lua
**Functions:**
- GetActivityDungeon1_Material_BattleUis
**Snippet:**
```lua
function GetActivityDungeon1_Material_BattleUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Material_BattleNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1_Material_BattleNumberUis
**Snippet:**
```lua
function GetActivityDungeon1_Material_BattleNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MaxBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_MaxBtnUis
**Snippet:**
```lua
function GetActivityDungeon1_MaxBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MinBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_MinBtnUis
**Snippet:**
```lua
function GetActivityDungeon1_MinBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniGameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniGameBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1_MiniGameBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniGameByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniGameUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1_MiniMain_TopByName
- ActivityDungeon1_MiniMain_BottonByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1_MiniMain_TopByName")
require("ActivityDungeon1_MiniMain_BottonByName")

function GetActivityDungeon1_MiniGameUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Top = GetActivityDungeon1_MiniMain_TopUis(ui:GetChild("Top"))
  uis.Botton = GetActivityDungeon1_MiniMain_BottonUis(ui:GetChild("Botton"))
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a1/ActivityDungeon1_MiniGameStartByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniGameStartUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1_MiniStart_IntegralByName
- ActivityDungeon1_MiniStart_FlowerMapByName
- ActivityDungeon1_MiniStart_PauseTipsByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1_MiniStart_IntegralByName")
require("ActivityDungeon1_MiniStart_FlowerMapByName")
require("ActivityDungeon1_MiniStart_PauseTipsByName")

function GetActivityDungeon1_MiniGameStartUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.CloseBtn = ui:GetChild("CloseBtn")
  uis.PauseBtn = ui:GetChild("PauseBtn")
```

---

## Activty/a1/ActivityDungeon1_MiniGameStartWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniGameStartWindowUis
**Requires:**
- ActivityDungeon1_MiniGameStartByName
**Snippet:**
```lua
require("ActivityDungeon1_MiniGameStartByName")

function GetActivityDungeon1_MiniGameStartWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1_MiniGameStartUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniGameWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniGameWindowUis
**Requires:**
- ActivityDungeon1_MiniGameByName
**Snippet:**
```lua
require("ActivityDungeon1_MiniGameByName")

function GetActivityDungeon1_MiniGameWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1_MiniGameUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniIntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniIntegralUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetActivityDungeon1_MiniIntegralUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
  uis.root = ui
  return uis
```

---

## Activty/a1/ActivityDungeon1_MiniIntegralWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniIntegralWindowUis
**Requires:**
- ActivityDungeon1_MiniIntegralByName
**Snippet:**
```lua
require("ActivityDungeon1_MiniIntegralByName")

function GetActivityDungeon1_MiniIntegralWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1_MiniIntegralUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniIntegral_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniIntegral_TipsAniUis
**Requires:**
- ActivityDungeon1_MiniIntegral_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1_MiniIntegral_TipsByName")

function GetActivityDungeon1_MiniIntegral_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1_MiniIntegral_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniIntegral_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniIntegral_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1_MiniIntegral_TipsUis(ui)
  local uis = {}
  
  uis.ItemList = ui:GetChild("ItemList")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniMain_BottonByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniMain_BottonUis
**Requires:**
- ActivityDungeon1_MiniMain_TodayTaskByName
**Snippet:**
```lua
require("ActivityDungeon1_MiniMain_TodayTaskByName")

function GetActivityDungeon1_MiniMain_BottonUis(ui)
  local uis = {}
  uis.TaskBtn = ui:GetChild("TaskBtn")
  uis.RecordBtn = ui:GetChild("RecordBtn")
  uis.TodayTask = GetActivityDungeon1_MiniMain_TodayTaskUis(ui:GetChild("TodayTask"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniMain_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniMain_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1_MiniMain_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniMain_RecordBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniMain_RecordBtnUis
**Snippet:**
```lua
function GetActivityDungeon1_MiniMain_RecordBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniMain_StartBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniMain_StartBtnUis
**Snippet:**
```lua
function GetActivityDungeon1_MiniMain_StartBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniMain_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniMain_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1_MiniMain_TaskBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniMain_TodayIntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniMain_TodayIntegralUis
**Snippet:**
```lua
function GetActivityDungeon1_MiniMain_TodayIntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniMain_TodayTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniMain_TodayTaskUis
**Requires:**
- ActivityDungeon1_PassReward_AllFrame_EByName
- CommonResource_RedDotByName
**Snippet:**
```lua
require("ActivityDungeon1_PassReward_AllFrame_EByName")
require("CommonResource_RedDotByName")

function GetActivityDungeon1_MiniMain_TodayTaskUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1_PassReward_AllFrame_EUis(ui:GetChild("Item"))
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a1/ActivityDungeon1_MiniMain_TopByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniMain_TopUis
**Requires:**
- ActivityDungeon1_MiniMain_IntegralByName
- ActivityDungeon1_MiniMain_TodayIntegralByName
**Snippet:**
```lua
require("ActivityDungeon1_MiniMain_IntegralByName")
require("ActivityDungeon1_MiniMain_TodayIntegralByName")

function GetActivityDungeon1_MiniMain_TopUis(ui)
  local uis = {}
  uis.Integral = GetActivityDungeon1_MiniMain_IntegralUis(ui:GetChild("Integral"))
  uis.TodayIntegral = GetActivityDungeon1_MiniMain_TodayIntegralUis(ui:GetChild("TodayIntegral"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniStart_CloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniStart_CloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1_MiniStart_CloseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniStart_CountdownByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniStart_CountdownUis
**Snippet:**
```lua
function GetActivityDungeon1_MiniStart_CountdownUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniStart_CountdownWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniStart_CountdownWindowUis
**Requires:**
- ActivityDungeon1_MiniStart_CountdownByName
**Snippet:**
```lua
require("ActivityDungeon1_MiniStart_CountdownByName")

function GetActivityDungeon1_MiniStart_CountdownWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1_MiniStart_CountdownUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniStart_EndAgainBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniStart_EndAgainBtnUis
**Snippet:**
```lua
function GetActivityDungeon1_MiniStart_EndAgainBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniStart_EndCloseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniStart_EndCloseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1_MiniStart_EndCloseBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniStart_EndRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniStart_EndRewardUis
**Requires:**
- CommonResource_PopupBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")

function GetActivityDungeon1_MiniStart_EndRewardUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.ItemList = ui:GetChild("ItemList")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.AgainBtn = ui:GetChild("AgainBtn")
  uis.CloseBtn = ui:GetChild("CloseBtn")
```

---

## Activty/a1/ActivityDungeon1_MiniStart_EndRewardItemByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniStart_EndRewardItemUis
**Snippet:**
```lua
function GetActivityDungeon1_MiniStart_EndRewardItemUis(ui)
  local uis = {}
  
  uis.FlowerLoader = ui:GetChild("FlowerLoader")
  uis.FlowerHolder = ui:GetChild("FlowerHolder")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniStart_EndRewardWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniStart_EndRewardWindowUis
**Requires:**
- ActivityDungeon1_MiniStart_EndRewardByName
**Snippet:**
```lua
require("ActivityDungeon1_MiniStart_EndRewardByName")

function GetActivityDungeon1_MiniStart_EndRewardWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1_MiniStart_EndRewardUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniStart_EndTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniStart_EndTipsUis
**Snippet:**
```lua
function GetActivityDungeon1_MiniStart_EndTipsUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniStart_EndTipsWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniStart_EndTipsWindowUis
**Requires:**
- ActivityDungeon1_MiniStart_EndTipsByName
**Snippet:**
```lua
require("ActivityDungeon1_MiniStart_EndTipsByName")

function GetActivityDungeon1_MiniStart_EndTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1_MiniStart_EndTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniStart_FlowerByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniStart_FlowerUis
**Snippet:**
```lua
function GetActivityDungeon1_MiniStart_FlowerUis(ui)
  local uis = {}
  
  uis.FlowerLoader = ui:GetChild("FlowerLoader")
  uis.FlowerHolder = ui:GetChild("FlowerHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniStart_FlowerDotBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniStart_FlowerDotBtnUis
**Requires:**
- ActivityDungeon1_MiniStart_GetIntegralByName
**Snippet:**
```lua
require("ActivityDungeon1_MiniStart_GetIntegralByName")

function GetActivityDungeon1_MiniStart_FlowerDotBtnUis(ui)
  local uis = {}
  uis.FlowerLoader = ui:GetChild("FlowerLoader")
  uis.FlowerHolder = ui:GetChild("FlowerHolder")
  uis.GetIntegral = GetActivityDungeon1_MiniStart_GetIntegralUis(ui:GetChild("GetIntegral"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
```

---

## Activty/a1/ActivityDungeon1_MiniStart_FlowerMapByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniStart_FlowerMapUis
**Snippet:**
```lua
function GetActivityDungeon1_MiniStart_FlowerMapUis(ui)
  local uis = {}
  
  uis.Dot1Btn = ui:GetChild("Dot1Btn")
  uis.Dot2Btn = ui:GetChild("Dot2Btn")
  uis.Dot3Btn = ui:GetChild("Dot3Btn")
  uis.Dot4Btn = ui:GetChild("Dot4Btn")
  uis.Dot5Btn = ui:GetChild("Dot5Btn")
  uis.Dot6Btn = ui:GetChild("Dot6Btn")
  uis.Dot7Btn = ui:GetChild("Dot7Btn")
```

---

## Activty/a1/ActivityDungeon1_MiniStart_GetIntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniStart_GetIntegralUis
**Snippet:**
```lua
function GetActivityDungeon1_MiniStart_GetIntegralUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniStart_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniStart_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1_MiniStart_IntegralUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniStart_PauseBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniStart_PauseBtnUis
**Snippet:**
```lua
function GetActivityDungeon1_MiniStart_PauseBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniStart_PauseTips1ByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniStart_PauseTips1Uis
**Snippet:**
```lua
function GetActivityDungeon1_MiniStart_PauseTips1Uis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniStart_PauseTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniStart_PauseTipsUis
**Requires:**
- ActivityDungeon1_MiniStart_PauseTips1ByName
**Snippet:**
```lua
require("ActivityDungeon1_MiniStart_PauseTips1ByName")

function GetActivityDungeon1_MiniStart_PauseTipsUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1_MiniStart_PauseTips1Uis(ui:GetChild("Tips"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniTaskByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniTaskUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1_MiniTask_IntegralByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1_MiniTask_IntegralByName")

function GetActivityDungeon1_MiniTaskUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.TouchScreenBtn = ui:GetChild("TouchScreenBtn")
  uis.Integral = GetActivityDungeon1_MiniTask_IntegralUis(ui:GetChild("Integral"))
  uis.TipsList = ui:GetChild("TipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a1/ActivityDungeon1_MiniTaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniTaskWindowUis
**Requires:**
- ActivityDungeon1_MiniTaskByName
**Snippet:**
```lua
require("ActivityDungeon1_MiniTaskByName")

function GetActivityDungeon1_MiniTaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1_MiniTaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniTask_IntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniTask_IntegralUis
**Snippet:**
```lua
function GetActivityDungeon1_MiniTask_IntegralUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniTask_RewardItemByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniTask_RewardItemUis
**Snippet:**
```lua
function GetActivityDungeon1_MiniTask_RewardItemUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniTask_RewardItemGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniTask_RewardItemGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1_MiniTask_RewardItemGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniTask_TipsAniUis
**Requires:**
- ActivityDungeon1_MiniTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1_MiniTask_TipsByName")

function GetActivityDungeon1_MiniTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1_MiniTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_MiniTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1_MiniTask_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1_MiniTask_TipsUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.Word1Txt = ui:GetChild("Word1Txt")
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.ItemList = ui:GetChild("ItemList")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a1/ActivityDungeon1_NormalBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_NormalBtnUis
**Snippet:**
```lua
function GetActivityDungeon1_NormalBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.newCtr = ui:GetController("new")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_NormalPoint1BtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_NormalPoint1BtnUis
**Snippet:**
```lua
function GetActivityDungeon1_NormalPoint1BtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_NormalPointBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_NormalPointBtnUis
**Snippet:**
```lua
function GetActivityDungeon1_NormalPointBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_NormalPointLockByName.lua.lua
**Functions:**
- GetActivityDungeon1_NormalPointLockUis
**Snippet:**
```lua
function GetActivityDungeon1_NormalPointLockUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_NumberStripByName.lua.lua
**Functions:**
- GetActivityDungeon1_NumberStripUis
**Snippet:**
```lua
function GetActivityDungeon1_NumberStripUis(ui)
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

## Activty/a1/ActivityDungeon1_PassBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1_PassBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_PassClothes_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassClothes_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1_PassClothes_BuyBtnUis(ui)
  local uis = {}
  
  uis.PriceTxt = ui:GetChild("PriceTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_PassClothes_BuyRewardByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassClothes_BuyRewardUis
**Snippet:**
```lua
function GetActivityDungeon1_PassClothes_BuyRewardUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_PassClothes_CardQBByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassClothes_CardQBUis
**Snippet:**
```lua
function GetActivityDungeon1_PassClothes_CardQBUis(ui)
  local uis = {}
  
  uis.QBHolder = ui:GetChild("QBHolder")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_PassClothes_ClothseRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassClothes_ClothseRegionUis
**Requires:**
- ActivityDungeon1_PassClothes_WordByName
- ActivityDungeon1_PassClothes_CardQBByName
- ActivityDungeon1_PassClothes_BuyRewardByName
**Snippet:**
```lua
require("ActivityDungeon1_PassClothes_WordByName")
require("ActivityDungeon1_PassClothes_CardQBByName")
require("ActivityDungeon1_PassClothes_BuyRewardByName")

function GetActivityDungeon1_PassClothes_ClothseRegionUis(ui)
  local uis = {}
  uis.Word = GetActivityDungeon1_PassClothes_WordUis(ui:GetChild("Word"))
  uis.CardQB = GetActivityDungeon1_PassClothes_CardQBUis(ui:GetChild("CardQB"))
  uis.BuyReward = GetActivityDungeon1_PassClothes_BuyRewardUis(ui:GetChild("BuyReward"))
  uis.BuyBtn = ui:GetChild("BuyBtn")
```

---

## Activty/a1/ActivityDungeon1_PassClothes_NameBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassClothes_NameBtnUis
**Snippet:**
```lua
function GetActivityDungeon1_PassClothes_NameBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_PassClothes_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassClothes_WordUis
**Snippet:**
```lua
function GetActivityDungeon1_PassClothes_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_PassportByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassportUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1_PassReward_RewardRegionByName
- ActivityDungeon1_PassTask_TaskRegionByName
- ActivityDungeon1_PassClothes_ClothseRegionByName
- ActivityDungeon1_Passport_LevelByName
- ActivityDungeon1_Sign_TimeByName
- ActivityDungeon1_Passport_TabRegionByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1_PassReward_RewardRegionByName")
require("ActivityDungeon1_PassTask_TaskRegionByName")
require("ActivityDungeon1_PassClothes_ClothseRegionByName")
require("ActivityDungeon1_Passport_LevelByName")
require("ActivityDungeon1_Sign_TimeByName")
require("ActivityDungeon1_Passport_TabRegionByName")

function GetActivityDungeon1_PassportUis(ui)
  local uis = {}
```

---

## Activty/a1/ActivityDungeon1_PassportUp_LevelUpBgByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassportUp_LevelUpBgUis
**Snippet:**
```lua
function GetActivityDungeon1_PassportUp_LevelUpBgUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_PassportUp_LevelUpTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassportUp_LevelUpTipsUis
**Requires:**
- CommonResource_PopupBgByName
- ActivityDungeon1_PassportUp_LevelUpBgByName
**Snippet:**
```lua
require("CommonResource_PopupBgByName")
require("ActivityDungeon1_PassportUp_LevelUpBgByName")

function GetActivityDungeon1_PassportUp_LevelUpTipsUis(ui)
  local uis = {}
  uis.PopupBg = GetCommonResource_PopupBgUis(ui:GetChild("PopupBg"))
  uis.LevelUpBg = GetActivityDungeon1_PassportUp_LevelUpBgUis(ui:GetChild("LevelUpBg"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.SubtitleTxt = ui:GetChild("SubtitleTxt")
  uis.LevelTxt = ui:GetChild("LevelTxt")
```

---

## Activty/a1/ActivityDungeon1_PassportUp_LevelUpTipsWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassportUp_LevelUpTipsWindowUis
**Requires:**
- ActivityDungeon1_PassportUp_LevelUpTipsByName
**Snippet:**
```lua
require("ActivityDungeon1_PassportUp_LevelUpTipsByName")

function GetActivityDungeon1_PassportUp_LevelUpTipsWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1_PassportUp_LevelUpTipsUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_PassportWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassportWindowUis
**Requires:**
- ActivityDungeon1_PassportByName
**Snippet:**
```lua
require("ActivityDungeon1_PassportByName")

function GetActivityDungeon1_PassportWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1_PassportUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Passport_AllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_Passport_AllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1_Passport_AllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Passport_BuyBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_Passport_BuyBtnUis
**Snippet:**
```lua
function GetActivityDungeon1_Passport_BuyBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Passport_ExpProgressBarByName.lua.lua
**Functions:**
- GetActivityDungeon1_Passport_ExpProgressBarUis
**Requires:**
- ActivityDungeon1_Passport_ExpProgressFillByName
**Snippet:**
```lua
require("ActivityDungeon1_Passport_ExpProgressFillByName")

function GetActivityDungeon1_Passport_ExpProgressBarUis(ui)
  local uis = {}
  uis.bar = GetActivityDungeon1_Passport_ExpProgressFillUis(ui:GetChild("bar"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Passport_ExpProgressFillByName.lua.lua
**Functions:**
- GetActivityDungeon1_Passport_ExpProgressFillUis
**Snippet:**
```lua
function GetActivityDungeon1_Passport_ExpProgressFillUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Passport_LevelByName.lua.lua
**Functions:**
- GetActivityDungeon1_Passport_LevelUis
**Snippet:**
```lua
function GetActivityDungeon1_Passport_LevelUis(ui)
  local uis = {}
  
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.ExpNumberTxt = ui:GetChild("ExpNumberTxt")
  uis.ExpProgressBar = ui:GetChild("ExpProgressBar")
  uis.LevelBuyBtn = ui:GetChild("LevelBuyBtn")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Passport_TabBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_Passport_TabBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1_Passport_TabBtnUis(ui)
  local uis = {}
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
```

---

## Activty/a1/ActivityDungeon1_Passport_TabRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1_Passport_TabRegionUis
**Snippet:**
```lua
function GetActivityDungeon1_Passport_TabRegionUis(ui)
  local uis = {}
  
  uis.TabList = ui:GetChild("TabList")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_PassReward_AllFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassReward_AllFrame_EUis
**Requires:**
- ActivityDungeon1_PassReward_ItemFrame_EByName
- ActivityDungeon1_PassReward_CardFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1_PassReward_ItemFrame_EByName")
require("ActivityDungeon1_PassReward_CardFrame_EByName")

function GetActivityDungeon1_PassReward_AllFrame_EUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1_PassReward_ItemFrame_EUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1_PassReward_CardFrame_EUis(ui:GetChild("CardFrame"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
```

---

## Activty/a1/ActivityDungeon1_PassReward_AllFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassReward_AllFrame_MUis
**Requires:**
- ActivityDungeon1_PassReward_ItemFrame_MByName
- ActivityDungeon1_PassReward_CardFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1_PassReward_ItemFrame_MByName")
require("ActivityDungeon1_PassReward_CardFrame_MByName")

function GetActivityDungeon1_PassReward_AllFrame_MUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1_PassReward_ItemFrame_MUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1_PassReward_CardFrame_MUis(ui:GetChild("CardFrame"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityDungeon1_PassReward_CardFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassReward_CardFrame_EUis
**Requires:**
- ActivityDungeon1_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1_PassReward_ItemCardPicByName")

function GetActivityDungeon1_PassReward_CardFrame_EUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a1/ActivityDungeon1_PassReward_CardFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassReward_CardFrame_MUis
**Requires:**
- ActivityDungeon1_PassReward_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1_PassReward_ItemCardPicByName")

function GetActivityDungeon1_PassReward_CardFrame_MUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1_PassReward_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a1/ActivityDungeon1_PassReward_EndTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassReward_EndTwoUis
**Requires:**
- ActivityDungeon1_PassReward_AllFrame_EByName
**Snippet:**
```lua
require("ActivityDungeon1_PassReward_AllFrame_EByName")

function GetActivityDungeon1_PassReward_EndTwoUis(ui)
  local uis = {}
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.Item1 = GetActivityDungeon1_PassReward_AllFrame_EUis(ui:GetChild("Item1"))
  uis.Item2 = GetActivityDungeon1_PassReward_AllFrame_EUis(ui:GetChild("Item2"))
  uis.root = ui
```

---

## Activty/a1/ActivityDungeon1_PassReward_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassReward_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1_PassReward_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_PassReward_ItemFrame_EByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassReward_ItemFrame_EUis
**Snippet:**
```lua
function GetActivityDungeon1_PassReward_ItemFrame_EUis(ui)
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

## Activty/a1/ActivityDungeon1_PassReward_ItemFrame_MByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassReward_ItemFrame_MUis
**Snippet:**
```lua
function GetActivityDungeon1_PassReward_ItemFrame_MUis(ui)
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

## Activty/a1/ActivityDungeon1_PassReward_LevelTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassReward_LevelTitleUis
**Snippet:**
```lua
function GetActivityDungeon1_PassReward_LevelTitleUis(ui)
  local uis = {}
  
  uis.LevelTxt = ui:GetChild("LevelTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_PassReward_MiddleRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassReward_MiddleRegionUis
**Snippet:**
```lua
function GetActivityDungeon1_PassReward_MiddleRegionUis(ui)
  local uis = {}
  
  uis.MiddleList = ui:GetChild("MiddleList")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_PassReward_MidTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassReward_MidTwoUis
**Requires:**
- ActivityDungeon1_PassReward_MidTwoItemByName
- ActivityDungeon1_PassReward_LevelTitleByName
**Snippet:**
```lua
require("ActivityDungeon1_PassReward_MidTwoItemByName")
require("ActivityDungeon1_PassReward_LevelTitleByName")

function GetActivityDungeon1_PassReward_MidTwoUis(ui)
  local uis = {}
  uis.Reward1 = GetActivityDungeon1_PassReward_MidTwoItemUis(ui:GetChild("Reward1"))
  uis.Reward2 = GetActivityDungeon1_PassReward_MidTwoItemUis(ui:GetChild("Reward2"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.Title = GetActivityDungeon1_PassReward_LevelTitleUis(ui:GetChild("Title"))
```

---

## Activty/a1/ActivityDungeon1_PassReward_MidTwoItemByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassReward_MidTwoItemUis
**Requires:**
- ActivityDungeon1_PassReward_AllFrame_MByName
**Snippet:**
```lua
require("ActivityDungeon1_PassReward_AllFrame_MByName")

function GetActivityDungeon1_PassReward_MidTwoItemUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1_PassReward_AllFrame_MUis(ui:GetChild("Item"))
  uis.EffectHolder = ui:GetChild("EffectHolder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_PassReward_PicByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassReward_PicUis
**Snippet:**
```lua
function GetActivityDungeon1_PassReward_PicUis(ui)
  local uis = {}
  
  uis.BuyTxt = ui:GetChild("BuyTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_PassReward_RewardRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassReward_RewardRegionUis
**Requires:**
- ActivityDungeon1_PassReward_MiddleRegionByName
- ActivityDungeon1_PassReward_StartTwoByName
- ActivityDungeon1_PassReward_EndTwoByName
**Snippet:**
```lua
require("ActivityDungeon1_PassReward_MiddleRegionByName")
require("ActivityDungeon1_PassReward_StartTwoByName")
require("ActivityDungeon1_PassReward_EndTwoByName")

function GetActivityDungeon1_PassReward_RewardRegionUis(ui)
  local uis = {}
  uis.MiddleList = GetActivityDungeon1_PassReward_MiddleRegionUis(ui:GetChild("MiddleList"))
  uis.StartTwo = GetActivityDungeon1_PassReward_StartTwoUis(ui:GetChild("StartTwo"))
  uis.EndTwo = GetActivityDungeon1_PassReward_EndTwoUis(ui:GetChild("EndTwo"))
  uis.c1Ctr = ui:GetController("c1")
```

---

## Activty/a1/ActivityDungeon1_PassReward_StartTwoByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassReward_StartTwoUis
**Requires:**
- ActivityDungeon1_PassReward_PicByName
**Snippet:**
```lua
require("ActivityDungeon1_PassReward_PicByName")

function GetActivityDungeon1_PassReward_StartTwoUis(ui)
  local uis = {}
  uis.Pic = GetActivityDungeon1_PassReward_PicUis(ui:GetChild("Pic"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.Effect2Holder = ui:GetChild("Effect2Holder")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_PassTask_TaskRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassTask_TaskRegionUis
**Requires:**
- ActivityDungeon1_TaskMaxByName
**Snippet:**
```lua
require("ActivityDungeon1_TaskMaxByName")

function GetActivityDungeon1_PassTask_TaskRegionUis(ui)
  local uis = {}
  uis.TipsList = ui:GetChild("TipsList")
  uis.Max = GetActivityDungeon1_TaskMaxUis(ui:GetChild("Max"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_PassTask_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassTask_TipsAniUis
**Requires:**
- ActivityDungeon1_PassTask_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1_PassTask_TipsByName")

function GetActivityDungeon1_PassTask_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1_PassTask_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_PassTask_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassTask_TipsUis
**Requires:**
- ActivityDungeon1_PassTask_TipsIntegralByName
**Snippet:**
```lua
require("ActivityDungeon1_PassTask_TipsIntegralByName")

function GetActivityDungeon1_PassTask_TipsUis(ui)
  local uis = {}
  uis.ProgressTxt = ui:GetChild("ProgressTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.Integral = GetActivityDungeon1_PassTask_TipsIntegralUis(ui:GetChild("Integral"))
  uis.TipsTxt = ui:GetChild("TipsTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a1/ActivityDungeon1_PassTask_TipsIntegralByName.lua.lua
**Functions:**
- GetActivityDungeon1_PassTask_TipsIntegralUis
**Snippet:**
```lua
function GetActivityDungeon1_PassTask_TipsIntegralUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_PlotBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_PlotBtnUis
**Snippet:**
```lua
function GetActivityDungeon1_PlotBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_PlotByName.lua.lua
**Functions:**
- GetActivityDungeon1_PlotUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1_Plot_WordByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1_Plot_WordByName")

function GetActivityDungeon1_PlotUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Word = GetActivityDungeon1_Plot_WordUis(ui:GetChild("Word"))
  uis.PlotList = ui:GetChild("PlotList")
  uis.ProspectBtn = ui:GetChild("ProspectBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a1/ActivityDungeon1_PlotWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1_PlotWindowUis
**Requires:**
- ActivityDungeon1_PlotByName
**Snippet:**
```lua
require("ActivityDungeon1_PlotByName")

function GetActivityDungeon1_PlotWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1_PlotUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Plot_ProspectBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_Plot_ProspectBtnUis
**Snippet:**
```lua
function GetActivityDungeon1_Plot_ProspectBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.LockTxt = ui:GetChild("LockTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.lockCtr = ui:GetController("lock")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Plot_TipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1_Plot_TipsAniUis
**Requires:**
- ActivityDungeon1_Plot_TipsByName
**Snippet:**
```lua
require("ActivityDungeon1_Plot_TipsByName")

function GetActivityDungeon1_Plot_TipsAniUis(ui)
  local uis = {}
  uis.Tips = GetActivityDungeon1_Plot_TipsUis(ui:GetChild("Tips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Plot_TipsByName.lua.lua
**Functions:**
- GetActivityDungeon1_Plot_TipsUis
**Snippet:**
```lua
function GetActivityDungeon1_Plot_TipsUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Plot_WordByName.lua.lua
**Functions:**
- GetActivityDungeon1_Plot_WordUis
**Snippet:**
```lua
function GetActivityDungeon1_Plot_WordUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_ReduceBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_ReduceBtnUis
**Snippet:**
```lua
function GetActivityDungeon1_ReduceBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_ShopBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_ShopBtnUis
**Snippet:**
```lua
function GetActivityDungeon1_ShopBtnUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_ShopByName.lua.lua
**Functions:**
- GetActivityDungeon1_ShopUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1_Shop_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1_Shop_TimeByName")

function GetActivityDungeon1_ShopUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.Time = GetActivityDungeon1_Shop_TimeUis(ui:GetChild("Time"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.AssetsTipsList = ui:GetChild("AssetsTipsList")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a1/ActivityDungeon1_ShopWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1_ShopWindowUis
**Requires:**
- ActivityDungeon1_ShopByName
**Snippet:**
```lua
require("ActivityDungeon1_ShopByName")

function GetActivityDungeon1_ShopWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1_ShopUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Shop_CardHeadBgByName.lua.lua
**Functions:**
- GetActivityDungeon1_Shop_CardHeadBgUis
**Snippet:**
```lua
function GetActivityDungeon1_Shop_CardHeadBgUis(ui)
  local uis = {}
  
  uis.PicLoader = ui:GetChild("PicLoader")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Shop_ItemAniByName.lua.lua
**Functions:**
- GetActivityDungeon1_Shop_ItemAniUis
**Requires:**
- ActivityDungeon1_Shop_ItemByName
**Snippet:**
```lua
require("ActivityDungeon1_Shop_ItemByName")

function GetActivityDungeon1_Shop_ItemAniUis(ui)
  local uis = {}
  uis.Item = GetActivityDungeon1_Shop_ItemUis(ui:GetChild("Item"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Shop_ItemBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_Shop_ItemBtnUis
**Requires:**
- ActivityDungeon1_Shop_CardHeadBgByName
- ActivityDungeon1_Shop_ItemNumberByName
- ActivityDungeon1_Shop_UseMarkByName
**Snippet:**
```lua
require("ActivityDungeon1_Shop_CardHeadBgByName")
require("ActivityDungeon1_Shop_ItemNumberByName")
require("ActivityDungeon1_Shop_UseMarkByName")

function GetActivityDungeon1_Shop_ItemBtnUis(ui)
  local uis = {}
  uis.CardHeadBg = GetActivityDungeon1_Shop_CardHeadBgUis(ui:GetChild("CardHeadBg"))
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.ItemNumber = GetActivityDungeon1_Shop_ItemNumberUis(ui:GetChild("ItemNumber"))
```

---

## Activty/a1/ActivityDungeon1_Shop_ItemByName.lua.lua
**Functions:**
- GetActivityDungeon1_Shop_ItemUis
**Requires:**
- ActivityDungeon1_Shop_SellOutByName
**Snippet:**
```lua
require("ActivityDungeon1_Shop_SellOutByName")

function GetActivityDungeon1_Shop_ItemUis(ui)
  local uis = {}
  uis.ItemBtn = ui:GetChild("ItemBtn")
  uis.SellOut = GetActivityDungeon1_Shop_SellOutUis(ui:GetChild("SellOut"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Shop_ItemNumberByName.lua.lua
**Functions:**
- GetActivityDungeon1_Shop_ItemNumberUis
**Snippet:**
```lua
function GetActivityDungeon1_Shop_ItemNumberUis(ui)
  local uis = {}
  
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Shop_ItemRegionByName.lua.lua
**Functions:**
- GetActivityDungeon1_Shop_ItemRegionUis
**Requires:**
- ActivityDungeon1_Shop_TitleByName
**Snippet:**
```lua
require("ActivityDungeon1_Shop_TitleByName")

function GetActivityDungeon1_Shop_ItemRegionUis(ui)
  local uis = {}
  uis.ShopTitle = GetActivityDungeon1_Shop_TitleUis(ui:GetChild("ShopTitle"))
  uis.ItemList = ui:GetChild("ItemList")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Shop_SellOutByName.lua.lua
**Functions:**
- GetActivityDungeon1_Shop_SellOutUis
**Snippet:**
```lua
function GetActivityDungeon1_Shop_SellOutUis(ui)
  local uis = {}
  
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Shop_StarByName.lua.lua
**Functions:**
- GetActivityDungeon1_Shop_StarUis
**Snippet:**
```lua
function GetActivityDungeon1_Shop_StarUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Shop_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1_Shop_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1_Shop_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Shop_TitleByName.lua.lua
**Functions:**
- GetActivityDungeon1_Shop_TitleUis
**Snippet:**
```lua
function GetActivityDungeon1_Shop_TitleUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Shop_UseMarkByName.lua.lua
**Functions:**
- GetActivityDungeon1_Shop_UseMarkUis
**Snippet:**
```lua
function GetActivityDungeon1_Shop_UseMarkUis(ui)
  local uis = {}
  
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_SignBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_SignBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1_SignBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_SignByName.lua.lua
**Functions:**
- GetActivityDungeon1_SignUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1_Sign_RewardListByName
- ActivityDungeon1_Sign_TimeByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1_Sign_RewardListByName")
require("ActivityDungeon1_Sign_TimeByName")

function GetActivityDungeon1_SignUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.RewardList = GetActivityDungeon1_Sign_RewardListUis(ui:GetChild("RewardList"))
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.Time = GetActivityDungeon1_Sign_TimeUis(ui:GetChild("Time"))
```

---

## Activty/a1/ActivityDungeon1_SignWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1_SignWindowUis
**Requires:**
- ActivityDungeon1_SignByName
**Snippet:**
```lua
require("ActivityDungeon1_SignByName")

function GetActivityDungeon1_SignWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1_SignUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Sign_AllFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1_Sign_AllFrameUis
**Requires:**
- ActivityDungeon1_Sign_ItemFrameByName
- ActivityDungeon1_Sign_CardFrameByName
**Snippet:**
```lua
require("ActivityDungeon1_Sign_ItemFrameByName")
require("ActivityDungeon1_Sign_CardFrameByName")

function GetActivityDungeon1_Sign_AllFrameUis(ui)
  local uis = {}
  uis.ItemFrame = GetActivityDungeon1_Sign_ItemFrameUis(ui:GetChild("ItemFrame"))
  uis.CardFrame = GetActivityDungeon1_Sign_CardFrameUis(ui:GetChild("CardFrame"))
  uis.Effect1Holder = ui:GetChild("Effect1Holder")
  uis.c2Ctr = ui:GetController("c2")
  uis.root = ui
```

---

## Activty/a1/ActivityDungeon1_Sign_CardFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1_Sign_CardFrameUis
**Requires:**
- ActivityDungeon1_Sign_ItemCardPicByName
**Snippet:**
```lua
require("ActivityDungeon1_Sign_ItemCardPicByName")

function GetActivityDungeon1_Sign_CardFrameUis(ui)
  local uis = {}
  uis.ItemCardPic = GetActivityDungeon1_Sign_ItemCardPicUis(ui:GetChild("ItemCardPic"))
  uis.c1Ctr = ui:GetController("c1")
  uis.c2Ctr = ui:GetController("c2")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
```

---

## Activty/a1/ActivityDungeon1_Sign_GetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_Sign_GetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1_Sign_GetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Sign_ItemCardPicByName.lua.lua
**Functions:**
- GetActivityDungeon1_Sign_ItemCardPicUis
**Snippet:**
```lua
function GetActivityDungeon1_Sign_ItemCardPicUis(ui)
  local uis = {}
  
  uis.ItemLoader = ui:GetChild("ItemLoader")
  uis.c3Ctr = ui:GetController("c3")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Sign_ItemFrameByName.lua.lua
**Functions:**
- GetActivityDungeon1_Sign_ItemFrameUis
**Snippet:**
```lua
function GetActivityDungeon1_Sign_ItemFrameUis(ui)
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

## Activty/a1/ActivityDungeon1_Sign_RewardAniByName.lua.lua
**Functions:**
- GetActivityDungeon1_Sign_RewardAniUis
**Requires:**
- ActivityDungeon1_Sign_RewardByName
**Snippet:**
```lua
require("ActivityDungeon1_Sign_RewardByName")

function GetActivityDungeon1_Sign_RewardAniUis(ui)
  local uis = {}
  uis.Reward = GetActivityDungeon1_Sign_RewardUis(ui:GetChild("Reward"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Sign_RewardByName.lua.lua
**Functions:**
- GetActivityDungeon1_Sign_RewardUis
**Requires:**
- ActivityDungeon1_Sign_AllFrameByName
**Snippet:**
```lua
require("ActivityDungeon1_Sign_AllFrameByName")

function GetActivityDungeon1_Sign_RewardUis(ui)
  local uis = {}
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Item = GetActivityDungeon1_Sign_AllFrameUis(ui:GetChild("Item"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
```

---

## Activty/a1/ActivityDungeon1_Sign_RewardListByName.lua.lua
**Functions:**
- GetActivityDungeon1_Sign_RewardListUis
**Snippet:**
```lua
function GetActivityDungeon1_Sign_RewardListUis(ui)
  local uis = {}
  
  uis.RewardList = ui:GetChild("RewardList")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_Sign_TimeByName.lua.lua
**Functions:**
- GetActivityDungeon1_Sign_TimeUis
**Snippet:**
```lua
function GetActivityDungeon1_Sign_TimeUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.TimeTxt = ui:GetChild("TimeTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_TaskAllGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_TaskAllGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1_TaskAllGetBtnUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_TaskBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_TaskBtnUis
**Requires:**
- CommonResource_RedDotByName
**Snippet:**
```lua
require("CommonResource_RedDotByName")

function GetActivityDungeon1_TaskBtnUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.Red = GetCommonResource_RedDotUis(ui:GetChild("Red"))
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_TaskByName.lua.lua
**Functions:**
- GetActivityDungeon1_TaskUis
**Requires:**
- CommonResource_BackGroundByName
- ActivityDungeon1_TaskTitleByName
**Snippet:**
```lua
require("CommonResource_BackGroundByName")
require("ActivityDungeon1_TaskTitleByName")

function GetActivityDungeon1_TaskUis(ui)
  local uis = {}
  uis.BackGround = GetCommonResource_BackGroundUis(ui:GetChild("BackGround"))
  uis.TaskTitle = GetActivityDungeon1_TaskTitleUis(ui:GetChild("TaskTitle"))
  uis.TaskTipsList = ui:GetChild("TaskTipsList")
  uis.AllGetBtn = ui:GetChild("AllGetBtn")
  uis.ReturnBtn = ui:GetChild("ReturnBtn")
```

---

## Activty/a1/ActivityDungeon1_TaskGetBtnByName.lua.lua
**Functions:**
- GetActivityDungeon1_TaskGetBtnUis
**Snippet:**
```lua
function GetActivityDungeon1_TaskGetBtnUis(ui)
  local uis = {}
  
  uis.buttonCtr = ui:GetController("button")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_TaskMaxByName.lua.lua
**Functions:**
- GetActivityDungeon1_TaskMaxUis
**Snippet:**
```lua
function GetActivityDungeon1_TaskMaxUis(ui)
  local uis = {}
  
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_TaskProgressByName.lua.lua
**Functions:**
- GetActivityDungeon1_TaskProgressUis
**Snippet:**
```lua
function GetActivityDungeon1_TaskProgressUis(ui)
  local uis = {}
  
  uis.Number1Txt = ui:GetChild("Number1Txt")
  uis.Number2Txt = ui:GetChild("Number2Txt")
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_TaskTipsAniByName.lua.lua
**Functions:**
- GetActivityDungeon1_TaskTipsAniUis
**Requires:**
- ActivityDungeon1_TaskTipsByName
**Snippet:**
```lua
require("ActivityDungeon1_TaskTipsByName")

function GetActivityDungeon1_TaskTipsAniUis(ui)
  local uis = {}
  uis.TaskTips = GetActivityDungeon1_TaskTipsUis(ui:GetChild("TaskTips"))
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_TaskTipsByName.lua.lua
**Functions:**
- GetActivityDungeon1_TaskTipsUis
**Requires:**
- ActivityDungeon1_TaskProgressByName
**Snippet:**
```lua
require("ActivityDungeon1_TaskProgressByName")

function GetActivityDungeon1_TaskTipsUis(ui)
  local uis = {}
  uis.NameTxt = ui:GetChild("NameTxt")
  uis.GetBtn = ui:GetChild("GetBtn")
  uis.RewardList = ui:GetChild("RewardList")
  uis.TaskProgress = GetActivityDungeon1_TaskProgressUis(ui:GetChild("TaskProgress"))
  uis.c1Ctr = ui:GetController("c1")
  uis.root = ui
```

---

## Activty/a1/ActivityDungeon1_TaskTitleByName.lua.lua
**Functions:**
- GetActivityDungeon1_TaskTitleUis
**Snippet:**
```lua
function GetActivityDungeon1_TaskTitleUis(ui)
  local uis = {}
  
  uis.TitleTxt = ui:GetChild("TitleTxt")
  uis.WordTxt = ui:GetChild("WordTxt")
  uis.NumberTxt = ui:GetChild("NumberTxt")
  uis.root = ui
  return uis
end
```

---

## Activty/a1/ActivityDungeon1_TaskWindowByName.lua.lua
**Functions:**
- GetActivityDungeon1_TaskWindowUis
**Requires:**
- ActivityDungeon1_TaskByName
**Snippet:**
```lua
require("ActivityDungeon1_TaskByName")

function GetActivityDungeon1_TaskWindowUis(ui)
  local uis = {}
  uis.Main = GetActivityDungeon1_TaskUis(ui:GetChild("Main"))
  uis.root = ui
  return uis
end
```

---
