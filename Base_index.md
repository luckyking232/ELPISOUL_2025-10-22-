# Base

## Base/BaseActivity.lua.lua
**Snippet:**
```lua
BaseActivity = {
  [70060001] = {
    id = 70060001,
    name = function()
      return T(80619001)
    end,
    type = 10111,
    initial_condition = 0,
    time_type = 0,
    relative_begin_time = 0,
```

---

## Base/BaseActivityAgreement.lua.lua
**Snippet:**
```lua
BaseActivityAgreement = {
  [70820001] = {
    id = 70820001,
    index = 1,
    free_group_id = 101,
    pay_group_id = 102,
    type = 1,
    mail_id = 70090017,
    name = function()
      return T(80670016)
```

---

## Base/BaseActivityAgreementReward.lua.lua
**Snippet:**
```lua
BaseActivityAgreementReward = {
  [70821011] = {
    id = 70821011,
    group_id = 101,
    level = 1,
    need_day = 1,
    reward = {
      "1:21000003:4000"
    }
  },
```

---

## Base/BaseActivityBanner.lua.lua
**Snippet:**
```lua
BaseActivityBanner = {
  [10001] = {
    id = 10001,
    type = 1,
    open_condition = "70020100:1",
    banner_pic = "HomeAd:HomeAd_001",
    banner_sort = 1
  },
  [10301] = {
    id = 10301,
```

---

## Base/BaseActivityCarnival.lua.lua
**Snippet:**
```lua
BaseActivityCarnival = {
  [70070701] = {
    id = 70070701,
    name = function()
      return T(80607001)
    end,
    pre_id = 0,
    next_id = 70070702,
    task_list = {
      70051001,
```

---

## Base/BaseActivityCarnivalTarget.lua.lua
**Snippet:**
```lua
BaseActivityCarnivalTarget = {
  [70070801] = {
    id = 70070801,
    index = 1,
    reward = {
      "1:21010001:30000"
    },
    unlock_points = {
      "1:21000008:30"
    }
```

---

## Base/BaseActivityCheckIn.lua.lua
**Snippet:**
```lua
BaseActivityCheckIn = {
  [70801001] = {
    id = 70801001,
    type = 10,
    day = 1,
    reward = {
      "1:21000001:500",
      "1:21000003:20000"
    }
  },
```

---

## Base/BaseActivityExplore.lua.lua
**Snippet:**
```lua
BaseActivityExplore = {
  [70810101] = {
    id = 70810101,
    type = 1,
    reward = {
      "1:21000001:100"
    },
    reward_prob = 2000,
    index = 1
  },
```

---

## Base/BaseActivityGame.lua.lua
**Snippet:**
```lua
BaseActivityGame = {
  [70076121] = {
    id = 70076121,
    game_id = 70441005,
    game_day = 1,
    item = {
      70076502,
      70076503,
      70076504,
      70076505,
```

---

## Base/BaseActivityGameDifficulty.lua.lua
**Snippet:**
```lua
BaseActivityGameDifficulty = {
  [70076001] = {
    id = 70076001,
    game_grid = 4,
    game_day = 1,
    game_end = 1,
    game_initial = {
      6,
      7,
      8,
```

---

## Base/BaseActivityGameItem.lua.lua
**Snippet:**
```lua
BaseActivityGameItem = {
  [70076501] = {
    id = 70076501,
    game_id = 70441005,
    type = 1,
    icon = "ActivityDungeon1004:MiniStart_Item01"
  },
  [70076502] = {
    id = 70076502,
    game_id = 70441005,
```

---

## Base/BaseActivityGameMap.lua.lua
**Snippet:**
```lua
BaseActivityGameMap = {
  [70910001] = {
    id = 70910001,
    game_id = 70441008,
    item_site = "|4:7|3:4:5:6:7:8|3:4:5:6:7:8|4:5:6:7|5:6|"
  },
  [70910002] = {
    id = 70910002,
    game_id = 70441008,
    item_site = "|3:5:6:8:9|3:5:6:8:9|2:3:5:6:8|2:3:5:6:8||"
```

---

## Base/BaseActivityGameMatchThree.lua.lua
**Snippet:**
```lua
BaseActivityGameMatchThree = {
  [70076101] = {
    id = 70076101,
    game_day = 1,
    item1 = {
      70076202,
      70076203,
      70076204,
      70076205
    },
```

---

## Base/BaseActivityGameMatchThreeItem.lua.lua
**Snippet:**
```lua
BaseActivityGameMatchThreeItem = {
  [70076201] = {
    id = 70076201,
    icon = "ActivityDungeon1004:MiniStart_Item01",
    type = 1
  },
  [70076202] = {
    id = 70076202,
    icon = "ActivityDungeon1004:MiniStart_Item02",
    type = 2
```

---

## Base/BaseActivityGameMining.lua.lua
**Snippet:**
```lua
BaseActivityGameMining = {
  [70076101] = {
    id = 70076101,
    game_day = 1,
    item = {
      70076201,
      70076201,
      70076202,
      70076202,
      70076203,
```

---

## Base/BaseActivityGameMiningItem.lua.lua
**Snippet:**
```lua
BaseActivityGameMiningItem = {
  [70076201] = {
    id = 70076201,
    icon = "ActivityDungeon1003:MiniStart_Item1_1",
    type = 1,
    num = {
      1,
      0,
      0
    },
```

---

## Base/BaseActivityGameMonster.lua.lua
**Snippet:**
```lua
BaseActivityGameMonster = {
  [78000000] = {
    id = 78000000,
    game_id = 70441010,
    type = 1,
    time = 0,
    speed = 80,
    speedUp = "150:100|100:110|50:120",
    skinName = "yellow",
    mode = "0:7|27:7|54:5|79:5",
```

---

## Base/BaseActivityPayWeek.lua.lua
**Snippet:**
```lua
BaseActivityPayWeek = {
  [70830201] = {
    id = 70830201,
    index = 1,
    type = 2,
    parameter = 6,
    reward = {
      "1:21000023:1"
    }
  },
```

---

## Base/BaseActivityRecharge.lua.lua
**Snippet:**
```lua
BaseActivityRecharge = {
  [70930101] = {
    id = 70930101,
    group_id = 101,
    recharge_level = 6,
    reward = {
      "1:21000037:4"
    }
  },
  [70930102] = {
```

---

## Base/BaseActivityReturn.lua.lua
**Snippet:**
```lua
BaseActivityReturn = {
  [70060702] = {
    id = 70060702,
    trigger_time = 21,
    trigger_level = 12,
    trigger_interval = 42,
    continue_time = 7,
    trigger_max = -1,
    reward = {
      "1:21000001:600",
```

---

## Base/BaseActivitySchedule.lua.lua
**Snippet:**
```lua
BaseActivitySchedule = {
  [70900101] = {
    id = 70900101,
    type = 1,
    sub_type = 101,
    name = function()
      return T(80635101)
    end,
    icon = "SchedulePic:SchedulePic_1001",
    sort = 1
```

---

## Base/BaseActivityShop.lua.lua
**Snippet:**
```lua
BaseActivityShop = {
  [70420001] = {id = 70420001, token_id = 21001001},
  [70420002] = {id = 70420002, token_id = 21001002},
  [70420003] = {id = 70420003, token_id = 21001003},
  [70420004] = {id = 70420004, token_id = 21001004},
  [70420005] = {id = 70420005, token_id = 21001005},
  [70420006] = {id = 70420006, token_id = 21001006},
  [70420007] = {id = 70420007, token_id = 21001007},
  [70420008] = {id = 70420008, token_id = 21001008},
  [70420009] = {id = 70420009, token_id = 21001009},
```

---

## Base/BaseActivityShopGrid.lua.lua
**Snippet:**
```lua
BaseActivityShopGrid = {
  [70480111] = {
    id = 70480111,
    activity_shop_id = 70421001,
    item = {
      "1:21181201:1"
    },
    sell_price = {
      "1:21000027:3"
    },
```

---

## Base/BaseActivitySignIn.lua.lua
**Snippet:**
```lua
BaseActivitySignIn = {
  [70060101] = {
    id = 70060101,
    index = 1,
    reward = {
      "1:21000003:2000",
      "1:21010001:2500",
      "1:21000003:3000",
      "1:21000201:40",
      "1:21000003:4000",
```

---

## Base/BaseActivityStageConfig.lua.lua
**Snippet:**
```lua
BaseActivityStageConfig = {
  [70440001] = {
    id = 70440001,
    task_group_id = {
      70410101,
      70410102,
      70410103,
      70410104,
      70410105,
      70410106,
```

---

## Base/BaseActivityStageGame.lua.lua
**Snippet:**
```lua
BaseActivityStageGame = {
  [70441001] = {
    id = 70441001,
    game_task_id = {
      70460101,
      70460102,
      70460103,
      70460104,
      70460105,
      70460106,
```

---

## Base/BaseActivityStageReview.lua.lua
**Snippet:**
```lua
BaseActivityStageReview = {
  [70442001] = {
    id = 70442001,
    name = function()
      return T(80636001)
    end,
    icon = "AbyssActivityPlot:ActivityCover_1000",
    des_date = function()
      return T(80637001)
    end,
```

---

## Base/BaseActivityTurntable.lua.lua
**Snippet:**
```lua
BaseActivityTurntable = {
  [70920100] = {
    id = 70920100,
    cost_type = 21,
    cost_change = 21000028,
    group_id = 1,
    pay_free_reward = {
      "1:21000029:6"
    },
    pay_id = {
```

---

## Base/BaseActivityTurntablePool.lua.lua
**Snippet:**
```lua
BaseActivityTurntablePool = {
  [70920101] = {
    id = 70920101,
    group_id = 1,
    reward = {
      "4:12001983:1"
    },
    max_num = 1,
    prob = 50,
    unlock_num = 4,
```

---

## Base/BaseActivityTurntableRecharge.lua.lua
**Snippet:**
```lua
BaseActivityTurntableRecharge = {
  [70930100] = {
    id = 70930100,
    unlock_time = {
      0,
      86400,
      172800
    },
    cost_type = {
      24,
```

---

## Base/BaseActivityVitGet.lua.lua
**Snippet:**
```lua
BaseActivityVitGet = {
  [70073101] = {
    id = 70073101,
    name = function()
      return T(80662101)
    end,
    remark = function()
      return T(80662201)
    end,
    des = function()
```

---

## Base/BaseAdventure.lua.lua
**Snippet:**
```lua
BaseAdventure = {
  [70070301] = {
    id = 70070301,
    name = function()
      return T(80240101)
    end,
    name_detail = function()
      return T(80240101)
    end,
    des = function()
```

---

## Base/BaseArenaLevel.lua.lua
**Snippet:**
```lua
BaseArenaLevel = {
  [50300101] = {
    id = 50300101,
    level = 1,
    rank_high = 1,
    rank_low = 3000,
    card_list = {
      10000101,
      10000134,
      10000104,
```

---

## Base/BaseArenaMap.lua.lua
**Snippet:**
```lua
BaseArenaMap = {
  [50301101] = {
    id = 50301101,
    name = function()
      return T(80620101)
    end,
    des = function()
      return T(80620201)
    end,
    icon = "MapPic:MapPic_1000_1",
```

---

## Base/BaseArenaRankReward.lua.lua
**Snippet:**
```lua
BaseArenaRankReward = {
  [50302101] = {
    id = 50302101,
    type = 3,
    rank_high = 1,
    rank_low = 1,
    reward = {
      "1:21000001:800",
      "1:21000402:40",
      "1:21010001:10000",
```

---

## Base/BaseArenaRobot.lua.lua
**Snippet:**
```lua
BaseArenaRobot = {
  [50305001] = {
    id = 50305001,
    region_low = 1901,
    region_high = 2001,
    robot_group_ids = {
      50411010,
      50411020,
      50411030,
      50411040,
```

---

## Base/BaseArenaTargetRule.lua.lua
**Snippet:**
```lua
BaseArenaTargetRule = {
  [50300201] = {
    id = 50300201,
    region_low = 1501,
    region_high = 2001,
    player1_high = 9441,
    player1_low = 9626,
    player2_high = 9627,
    player2_low = 9813,
    player3_high = 9814,
```

---

## Base/BaseAttribute.lua.lua
**Snippet:**
```lua
BaseAttribute = {
  [40000101] = {
    id = 40000101,
    name = "hp",
    display_name = function()
      return T(80000101)
    end,
    power = 0
  },
  [40000102] = {
```

---

## Base/BaseBadge.lua.lua
**Snippet:**
```lua
BaseBadge = {
  [21080011] = {
    id = 21080011,
    name = function()
      return T(80701001)
    end,
    des = function()
      return T(80702001)
    end,
    icon = "ItemIcon:21080011",
```

---

## Base/BaseBadgeAttribute.lua.lua
**Snippet:**
```lua
BaseBadgeAttribute = {
  [40005001] = {
    id = 40005001,
    type = 1,
    value = "1:40000103:22",
    value_add = 7,
    show_type = 1
  },
  [40005002] = {
    id = 40005002,
```

---

## Base/BaseBadgeLevelUp.lua.lua
**Snippet:**
```lua
BaseBadgeLevelUp = {
  [40004001000] = {
    id = 40004001000,
    next_exp = 150,
    cost_money = 1,
    vice_type = 0
  },
  [40004001001] = {
    id = 40004001001,
    next_exp = 210,
```

---

## Base/BaseBadgeSuit.lua.lua
**Snippet:**
```lua
BaseBadgeSuit = {
  [40007001] = {
    id = 40007001,
    des = function()
      return T(80703001, 15)
    end,
    badge_ids = {
      21080011,
      21080012,
      21080013,
```

---

## Base/BaseBadgeSuitGroup.lua.lua
**Snippet:**
```lua
BaseBadgeSuitGroup = {
  [40008001] = {
    id = 40008001,
    name = function()
      return T(80704001)
    end,
    icon = "ItemIcon:40008001",
    suit_id = {40007001, 40007002},
    sort = 1,
    des = function()
```

---

## Base/BaseBattlePass.lua.lua
**Snippet:**
```lua
BaseBattlePass = {
  [70040011] = {id = 70040011, open = true},
  [70040012] = {id = 70040012, open = false},
  [70040021] = {id = 70040021, open = true},
  [70040022] = {id = 70040022, open = false},
  [70040031] = {id = 70040031, open = true},
  [70040032] = {id = 70040032, open = false},
  [70040041] = {id = 70040041, open = true},
  [70040042] = {id = 70040042, open = false},
  [70040051] = {id = 70040051, open = true},
```

---

## Base/BaseBattlePassLevel.lua.lua
**Snippet:**
```lua
BaseBattlePassLevel = {
  [70041000] = {
    id = 70041000,
    type = 1,
    level = 0,
    next_exp = 30,
    next_cost = {
      "1:21000001:300"
    }
  },
```

---

## Base/BaseBattlePassport.lua.lua
**Snippet:**
```lua
BaseBattlePassport = {
  [70040010] = {
    id = 70040010,
    group_id = 1,
    pass_ids = {70040011, 70040012},
    grow_model_id = 1,
    level_max = 50,
    exp_max = 500,
    fashion_pic = "PassportPic:PassportBanner_1000",
    bg_pic = "PassportPic:Passport_1000",
```

---

## Base/BaseBattlePassReward.lua.lua
**Snippet:**
```lua
BaseBattlePassReward = {
  [28000100] = {
    id = 28000100,
    pass_id = 70040011,
    level = 0,
    reward = {
      "1:21010001:1000"
    }
  },
  [28000101] = {
```

---

## Base/BaseBattleTarget.lua.lua
**Snippet:**
```lua
BaseBattleTarget = {
  [2033] = {
    id = 2033,
    target_type = 2030,
    target_param = 3
  },
  [2035] = {
    id = 2035,
    target_type = 2030,
    target_param = 5
```

---

## Base/BaseBiography.lua.lua
**Snippet:**
```lua
BaseBiography = {
  [70610001] = {
    id = 70610001,
    name = function()
      return T(80626001)
    end,
    name_english = function()
      return T(80626101)
    end,
    pre = 0,
```

---

## Base/BaseBiographyFlower.lua.lua
**Snippet:**
```lua
BaseBiographyFlower = {
  [70620101] = {
    id = 70620101,
    pre = 0,
    next = {70620102},
    open_condition = {
      "70020200:50110108"
    }
  },
  [70620102] = {
```

---

## Base/BaseBuffPath.lua.lua
**Snippet:**
```lua
BaseBuffPath = {
  [120] = {
    id = 120,
    settle_path = "battle/FX_battle_normal_counterattack.prefab",
    loop = 1
  },
  [403] = {
    id = 403,
    settle_path = "battle/FX_battle_normal_immunity.prefab",
    loop = 1
```

---

## Base/BaseBuilding.lua.lua
**Snippet:**
```lua
BaseBuilding = {
  [13000001] = {
    id = 13000001,
    cost = 0,
    range = {80, 80},
    type = 2,
    monster_id = 36000001,
    passive_skill = {41034615},
    star = 1
  },
```

---

## Base/BaseBurst.lua.lua
**Snippet:**
```lua
BaseBurst = {
  [1001] = {
    id = 1001,
    energy_max = 30000,
    energy = 9000,
    energy_time = 100,
    energy_skill = 41011000,
    energy_cycle = 15,
    energy_need_jobs = {
      1,
```

---

## Base/BaseBuyTime.lua.lua
**Snippet:**
```lua
BaseBuyTime = {
  [70030001] = {
    id = 70030001,
    type = 1,
    start = 1,
    finish = 1,
    cost = {
      "1:21000001:60"
    },
    reward = {
```

---

## Base/BaseCard.lua.lua
**Snippet:**
```lua
BaseCard = {
  [10000101] = {
    id = 10000101,
    name = function()
      return T(80101101)
    end,
    name_english = function()
      return T(80102101)
    end,
    des = function()
```

---

## Base/BaseCardGradeUp.lua.lua
**Snippet:**
```lua
BaseCardGradeUp = {
  [10000101000] = {
    id = 10000101000,
    cost = {
      "1:21070101:1"
    },
    unlock_skill_id = 0
  },
  [10000101001] = {
    id = 10000101001,
```

---

## Base/BaseCardHandBook.lua.lua
**Snippet:**
```lua
BaseCardHandBook = {
  [10000101] = {
    id = 10000101,
    show_type = 1,
    first_reward = {
      "1:21000001:20"
    }
  },
  [10000102] = {
    id = 10000102,
```

---

## Base/BaseCardHandBookGrow.lua.lua
**Snippet:**
```lua
BaseCardHandBookGrow = {
  [24040101] = {
    id = 24040101,
    group = 1,
    next = 24040102,
    show_type = 0,
    star_cost = 1,
    add_attr = {
      "1:40000103:2"
    }
```

---

## Base/BaseCardLevelUp.lua.lua
**Snippet:**
```lua
BaseCardLevelUp = {
  [40002101001] = {
    id = 40002101001,
    add_attr = {
      "1:40000103:0",
      "1:40000104:0",
      "1:40000102:0"
    },
    level_show = 1,
    task_parameter = 10001
```

---

## Base/BaseCardLevelUpCost.lua.lua
**Snippet:**
```lua
BaseCardLevelUpCost = {
  [40003001001] = {
    id = 40003001001,
    next_exp = 100,
    cost_money = 1
  },
  [40003001002] = {
    id = 40003001002,
    next_exp = 110,
    cost_money = 1
```

---

## Base/BaseCardQualityUp.lua.lua
**Snippet:**
```lua
BaseCardQualityUp = {
  [10000101000] = {
    id = 10000101000,
    add_attr = {
      "1:40000103:0",
      "1:40000104:0",
      "1:40000102:0"
    },
    cost = {
      "1:21000003:3000",
```

---

## Base/BaseCardSound.lua.lua
**Snippet:**
```lua
BaseCardSound = {
  [85010001] = {id = 85010001},
  [85010002] = {id = 85010002},
  [85010003] = {id = 85010003},
  [85010004] = {id = 85010004},
  [85011010] = {
    id = 85011010,
    name = function()
      return T(80120001)
    end,
```

---

## Base/BaseChapter.lua.lua
**Snippet:**
```lua
BaseChapter = {
  [50000101] = {
    id = 50000101,
    name = function()
      return T(80200000, 1)
    end,
    chapter_english = function()
      return T(80200001)
    end,
    name_detail = function()
```

---

## Base/BaseClientGoTo.lua.lua
**Snippet:**
```lua
BaseClientGoTo = {
  [2100000301] = {
    id = 2100000301,
    name = function()
      return T(84105010, T(80202101))
    end,
    go_to_feature = 10501,
    go_to_stage = 50130101,
    sort = 15,
    type = 0
```

---

## Base/BaseCondition.lua.lua
**Snippet:**
```lua
BaseCondition = {
  [70020100] = {
    id = 70020100,
    type = 100,
    judge = 5,
    save = 0,
    accu = 0
  },
  [70020101] = {
    id = 70020101,
```

---

## Base/BaseCvNameCn.lua.lua
**Snippet:**
```lua
BaseCvNameCn = {
  [80108101] = {
    id = 80108101,
    name_cn = "徐翔",
    name_jp = "田丸笃志"
  },
  [80108102] = {
    id = 80108102,
    name_cn = "宴宁",
    name_jp = "花咲心优"
```

---

## Base/BaseCvNameJp.lua.lua
**Snippet:**
```lua
BaseCvNameJp = {
  [80108101] = {
    id = 80108101,
    name_cn = "徐翔",
    name_jp = "田丸篤志"
  },
  [80108102] = {
    id = 80108102,
    name_cn = "宴宁",
    name_jp = "花咲心優"
```

---

## Base/BaseDailyDungeon.lua.lua
**Snippet:**
```lua
BaseDailyDungeon = {
  [50000300] = {
    id = 50000300,
    name = function()
      return T(80202100)
    end,
    name_detail = function()
      return T(80202001)
    end,
    des = function()
```

---

## Base/BaseDispatchLevel.lua.lua
**Snippet:**
```lua
BaseDispatchLevel = {
  [70074001] = {
    id = 70074001,
    level = 1,
    next_exp = 500
  },
  [70074002] = {
    id = 70074002,
    level = 2,
    next_exp = 550
```

---

## Base/BaseDispatchReward.lua.lua
**Snippet:**
```lua
BaseDispatchReward = {
  [70075001] = {
    id = 70075001,
    group_id = 101,
    level_range = {1, 2},
    time = 240,
    reward = {
      "1:21000022:50",
      "1:21000025:31"
    },
```

---

## Base/BaseDispatchTeam.lua.lua
**Snippet:**
```lua
BaseDispatchTeam = {
  [70073301] = {
    id = 70073301,
    name_team = function()
      return T(80634001)
    end,
    dispatch_level = 1,
    job_num = {
      5,
      4,
```

---

## Base/BaseEmoji.lua.lua
**Snippet:**
```lua
BaseEmoji = {
  [70080101] = {
    id = 70080101,
    group_id = 70080100,
    path = "ChatEmoji:Emoji_1000",
    sort = 1
  },
  [70080102] = {
    id = 70080102,
    group_id = 70080100,
```

---

## Base/BaseEmojiGroup.lua.lua
**Snippet:**
```lua
BaseEmojiGroup = {
  [70080100] = {
    id = 70080100,
    icon = "ChatEmoji:Title_01",
    sort = 1
  },
  [70080200] = {
    id = 70080200,
    icon = "ChatEmoji:Title_02",
    sort = 2
```

---

## Base/BaseErrorCode.lua.lua
**Snippet:**
```lua
BaseErrorCode = {
  [-1] = {
    id = -1,
    text = function(...)
      return T(7000001, ...)
    end
  },
  [-2] = {
    id = -2,
    text = function(...)
```

---

## Base/BaseExpedition.lua.lua
**Snippet:**
```lua
BaseExpedition = {
  [50700001] = {
    id = 50700001,
    type = 0,
    index = 1,
    chapter_ids = {
      "50002001:46201101",
      "50002002:46201101",
      "50002003:46201101",
      "50002004:46201101"
```

---

## Base/BaseExpeditionMap.lua.lua
**Snippet:**
```lua
BaseExpeditionMap = {
  [101] = {
    id = 101,
    map_id = 10408,
    role_num = 4
  },
  [102] = {
    id = 102,
    map_id = 10603,
    role_num = 6
```

---

## Base/BaseExpeditionReward.lua.lua
**Snippet:**
```lua
BaseExpeditionReward = {
  [24010001] = {
    id = 24010001,
    name = function()
      return T(80610001)
    end,
    index = 1,
    unlock_points = 3
  },
  [24010002] = {
```

---

## Base/BaseExpeditionRobot.lua.lua
**Snippet:**
```lua
BaseExpeditionRobot = {
  [77070501] = {
    id = 77070501,
    power_range = 99999,
    robot_group_ids = {
      50412900,
      50412910,
      50412920
    }
  }
```

---

## Base/BaseFashion.lua.lua
**Snippet:**
```lua
BaseFashion = {
  [12010000] = {
    id = 12010000,
    start_interval = 1,
    interval = 30,
    spd = "battlespine_empty.prefab",
    spd_scale = 10000,
    range = 40,
    effect_scale = 10000,
    manor_scale = 13265
```

---

## Base/BaseFashionBubble.lua.lua
**Snippet:**
```lua
BaseFashionBubble = {
  [100011] = {
    id = 100011,
    unlock_bubble_ids = {85011011},
    login_bubble_ids = {85021011},
    standby_bubble_ids = {85031011, 85031012},
    quality_bubble_ids = {
      85041011,
      85041012,
      85041013
```

---

## Base/BaseFeature.lua.lua
**Snippet:**
```lua
BaseFeature = {
  [10100] = {
    id = 10100,
    name = function()
      return T(80625100)
    end,
    window_name = "HomeWindow"
  },
  [10101] = {id = 10101, level = 1},
  [10102] = {
```

---

## Base/BaseFixed.lua.lua
**Snippet:**
```lua
BaseFixed = {
  [70010000] = {id = 70010000, int_value = 1},
  [70010001] = {
    id = 70010001,
    array_value = "1:21000001:1500|1:21000003:5000|1:21010001:5000|1:21000004:80|1:21000009:80|1:21000013:5|2:10000101:1|2:10000104:1|2:10000118:1|2:10000134:1|1:21120101:1|1:21120102:1|1:21120103:1|1:21120104:1|1:21140001:1|1:21140002:1|1:21140003:1|1:21140004:1|1:21140005:1|1:21140006:1|1:21140007:1|1:21140008:1|1:21030401:2|1:21020004:2"
  },
  [70010002] = {id = 70010002, int_value = 360},
  [70010003] = {id = 70010003, int_value = 1650},
  [70010004] = {id = 70010004, array_value = "1:0500:MX0"},
  [70010005] = {
```

---

## Base/BaseGacha.lua.lua
**Snippet:**
```lua
BaseGacha = {
  [24000001] = {
    id = 24000001,
    name = function()
      return T(80613001)
    end,
    type = 1,
    banner = "LotteryAd:LotteryBanner_002",
    back_ground = "Assets/Art/TextureSingle/LotteryBg/LotteryBg_002.png",
    bottom_type = 0,
```

---

## Base/BaseGachaBottomPool.lua.lua
**Snippet:**
```lua
BaseGachaBottomPool = {
  [24002012] = {
    id = 24002012,
    type = 2,
    bottom_num = 10,
    drop_pool = 22500012,
    priority = 2,
    bottom_type = 2,
    bottom_time = -1
  },
```

---

## Base/BaseGachaBottomUp.lua.lua
**Snippet:**
```lua
BaseGachaBottomUp = {
  [24003021] = {
    id = 24003021,
    up_pool = 22500021,
    up_add = {
      "61:61:500",
      "62:62:1000",
      "63:63:1500",
      "64:64:2000",
      "65:65:2500",
```

---

## Base/BaseGachaMode.lua.lua
**Snippet:**
```lua
BaseGachaMode = {
  [24001012] = {
    id = 24001012,
    type = 4,
    mode = 2,
    gacha_time = 10,
    cost = {
      "1:21100001:8"
    },
    day_limit_num = -1,
```

---

## Base/BaseGift.lua.lua
**Snippet:**
```lua
BaseGift = {
  [27000000] = {
    id = 27000000,
    type = 4,
    gift_reward_ids = {27100001, 27100002},
    condition = {"70020100:1"},
    sell_limit_type = 4,
    sell_limit_max = 1,
    sort = 999
  },
```

---

## Base/BaseGiftPage.lua.lua
**Snippet:**
```lua
BaseGiftPage = {
  [70073201] = {
    id = 70073201,
    type = 1,
    name = function()
      return T(80670001)
    end,
    icon = "Shop:ShopTab_1",
    sort = 10
  },
```

---

## Base/BaseGiftReward.lua.lua
**Snippet:**
```lua
BaseGiftReward = {
  [27100001] = {
    id = 27100001,
    condition = {"70020100:1"},
    days_limit = 0,
    rewards = {
      "1:21100001:10",
      "1:21100004:10",
      "4:12001183:1"
    }
```

---

## Base/BaseGuideCaption.lua.lua
**Snippet:**
```lua
BaseGuideCaption = {
  [70730010] = {
    id = 70730010,
    picture = {
      "Guide_%s:Guide_100",
      "Guide_%s:Guide_101"
    },
    aperture = 2
  },
  [70730020] = {
```

---

## Base/BaseGuideProcess.lua.lua
**Snippet:**
```lua
BaseGuideProcess = {
  [70720000] = {
    id = 70720000,
    window_name = "PlotPlayWindow",
    plot_stage = 50110101,
    next_process = 70720001,
    step1 = {70710000},
    key1 = 70710000
  },
  [70720001] = {
```

---

## Base/BaseGuideRemind.lua.lua
**Snippet:**
```lua
BaseGuideRemind = {
  [70700000] = {
    id = 70700000,
    window_name = "HomeWindow",
    ctrl_id = "MiddleZone/AdventureBtn",
    level_range = {5, 40},
    wait_time = 3,
    bubble_state = 1,
    bubble_pos = {0, 0},
    bubble_text = function()
```

---

## Base/BaseGuideStep.lua.lua
**Snippet:**
```lua
BaseGuideStep = {
  [70710000] = {
    id = 70710000,
    type = 7,
    plot_stage = 50110101,
    listen_complete_func = function()
      return GuideMgr.IsStageComplete(50110101)
    end,
    direct_play = 1,
    manual_play = 1
```

---

## Base/BaseGuildHeadIcon.lua.lua
**Snippet:**
```lua
BaseGuildHeadIcon = {
  [70070201] = {
    id = 70070201,
    icon = "GuildHead:Guild_1000",
    sort = 1000
  },
  [70070202] = {
    id = 70070202,
    icon = "GuildHead:Guild_1001",
    sort = 999
```

---

## Base/BaseGuildLevelUp.lua.lua
**Snippet:**
```lua
BaseGuildLevelUp = {
  [70070101] = {
    id = 70070101,
    name = function()
      return T(80602001)
    end,
    level = 1,
    next_exp = 1000,
    max_member = 20,
    max_exp = 2000
```

---

## Base/BaseGuildPolicy.lua.lua
**Snippet:**
```lua
BaseGuildPolicy = {
  [70070001] = {
    id = 70070001,
    name = function()
      return T(80670101)
    end,
    sort = 1
  },
  [70070002] = {
    id = 70070002,
```

---

## Base/BaseGuildWar.lua.lua
**Snippet:**
```lua
BaseGuildWar = {
  [51400001] = {
    id = 51400001,
    phase = 1,
    next = 51400002,
    chapter_id = {
      50020101,
      50020102,
      50020103,
      50020104,
```

---

## Base/BaseGuildWarReward.lua.lua
**Snippet:**
```lua
BaseGuildWarReward = {
  [24030101] = {
    id = 24030101,
    phase = 1,
    rank_type = 1,
    rank_high = 1,
    rank_low = 5,
    reward = {
      "1:21000001:3000",
      "1:21010001:200000",
```

---

## Base/BaseItem.lua.lua
**Snippet:**
```lua
BaseItem = {
  [21000001] = {
    id = 21000001,
    name = function()
      return T(81000001)
    end,
    remark = function()
      return T(82000001)
    end,
    des = function()
```

---

## Base/BaseJob.lua.lua
**Snippet:**
```lua
BaseJob = {
  [1] = {
    id = 1,
    range_find = 240,
    beat_back_frames = 30,
    damage_add_1 = 0,
    damage_add_2 = 0,
    damage_add_3 = 0,
    damage_add_4 = 0,
    damage_add_5 = 0
```

---

## Base/BaseMail.lua.lua
**Snippet:**
```lua
BaseMail = {
  [70090001] = {
    id = 70090001,
    title = 80640011,
    sender = 80640012,
    content = 80640013,
    date = 7,
    prior = 0,
    delete = 0
  },
```

---

## Base/BaseManorEvent.lua.lua
**Snippet:**
```lua
BaseManorEvent = {
  [76201001] = {
    id = 76201001,
    map_id = 75000001,
    spd = "Assets/Art/Map/Prefab/Items/board_01.prefab",
    resist = 1,
    site = 75101001,
    type = 1,
    sub_type = 4,
    reset_type = 0,
```

---

## Base/BaseManorGoTo.lua.lua
**Snippet:**
```lua
BaseManorGoTo = {
  [75600101] = {
    id = 75600101,
    group_id = 1,
    name = function()
      return T(87200101)
    end,
    name_english = function()
      return T(87210101)
    end,
```

---

## Base/BaseManorGrid.lua.lua
**Snippet:**
```lua
BaseManorGrid = {
  [75101000] = {
    id = 75101000,
    map_id = 75000001,
    coordinate = {"-3:-31"}
  },
  [75101001] = {
    id = 75101001,
    map_id = 75000001,
    coordinate = {"-2:-29"}
```

---

## Base/BaseManorLevelUp.lua.lua
**Snippet:**
```lua
BaseManorLevelUp = {
  [75001001] = {
    id = 75001001,
    level = 1,
    next_exp = 0,
    bgm_num = 3,
    monster_num = 3,
    name = function()
      return T(86000101)
    end,
```

---

## Base/BaseManorMap.lua.lua
**Snippet:**
```lua
BaseManorMap = {
  [75000001] = {
    id = 75000001,
    map_path = "PATH",
    first_site = {75101000}
  },
  [75000101] = {
    id = 75000101,
    map_path = "PATH",
    first_site = {75200100}
```

---

## Base/BaseManorMapSub.lua.lua
**Snippet:**
```lua
BaseManorMapSub = {
  [1] = {
    id = 1,
    name = function()
      return T(86000001)
    end,
    name_english = function()
      return T(86000009)
    end,
    type = 0,
```

---

## Base/BaseManorNode.lua.lua
**Snippet:**
```lua
BaseManorNode = {
  [76500101] = {
    id = 76500101,
    map_id = 75000001,
    spd = "Assets/Art/Map/Prefab/Items/build_05.prefab",
    resist = 1,
    site_range = {
      3,
      4,
      5
```

---

## Base/BaseManorReward.lua.lua
**Snippet:**
```lua
BaseManorReward = {
  [75501011] = {
    id = 75501011,
    group_id = 101,
    level = {1, 1},
    reward = {
      "1:21000311:2"
    },
    level_range = {1, 30}
  },
```

---

## Base/BaseMap.lua.lua
**Snippet:**
```lua
BaseMap = {
  [1] = {
    id = 1,
    size = {15, 5},
    size_own = {5, 5},
    size_enemy = {5, 5},
    background_path = "battlescene_90220003.prefab",
    role_site = {
      101,
      102,
```

---

## Base/BaseMonster.lua.lua
**Snippet:**
```lua
BaseMonster = {
  minId = 30000101,
  maxId = 52022002,
  step = 2000
}
```

---

## Base/BaseMonsterAttrPower.lua.lua
**Snippet:**
```lua
BaseMonsterAttrPower = {
  [77070401] = {
    id = 77070401,
    min = 1,
    max = 5000,
    attr_ratio = {
      "40000102:760",
      "40000103:40",
      "40000104:90"
    }
```

---

## Base/BaseMonsterGroup.lua.lua
**Snippet:**
```lua
BaseMonsterGroup = {
  [50200001] = {
    id = 50200001,
    monster_list = {
      30100001,
      30100002,
      30100003,
      30100004,
      30100005,
      30100006,
```

---

## Base/BaseMonsterPart0.lua.lua
**Snippet:**
```lua
BaseMonsterPart0 = {
  [30000101] = {
    id = 30000101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 210,
```

---

## Base/BaseMonsterPart10.lua.lua
**Snippet:**
```lua
BaseMonsterPart10 = {
  [30020101] = {
    id = 30020101,
    name = function()
      return T(80301201)
    end,
    type = 4,
    element_type = {2},
    star = 0,
    level = 210,
```

---

## Base/BaseMonsterPart1005.lua.lua
**Snippet:**
```lua
BaseMonsterPart1005 = {
  [32010101] = {
    id = 32010101,
    name = function()
      return T(80301002)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 1,
```

---

## Base/BaseMonsterPart1010.lua.lua
**Snippet:**
```lua
BaseMonsterPart1010 = {
  [32020101] = {
    id = 32020101,
    name = function()
      return T(80301002)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 6,
```

---

## Base/BaseMonsterPart1015.lua.lua
**Snippet:**
```lua
BaseMonsterPart1015 = {
  [32030101] = {
    id = 32030101,
    name = function()
      return T(80301002)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 18,
```

---

## Base/BaseMonsterPart1020.lua.lua
**Snippet:**
```lua
BaseMonsterPart1020 = {
  [32040101] = {
    id = 32040101,
    name = function()
      return T(80301002)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 33,
```

---

## Base/BaseMonsterPart1025.lua.lua
**Snippet:**
```lua
BaseMonsterPart1025 = {
  [32050101] = {
    id = 32050101,
    name = function()
      return T(80301002)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 45,
```

---

## Base/BaseMonsterPart1030.lua.lua
**Snippet:**
```lua
BaseMonsterPart1030 = {
  [32060101] = {
    id = 32060101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 57,
```

---

## Base/BaseMonsterPart1035.lua.lua
**Snippet:**
```lua
BaseMonsterPart1035 = {
  [32070101] = {
    id = 32070101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 72,
```

---

## Base/BaseMonsterPart1040.lua.lua
**Snippet:**
```lua
BaseMonsterPart1040 = {
  [32080101] = {
    id = 32080101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 84,
```

---

## Base/BaseMonsterPart1045.lua.lua
**Snippet:**
```lua
BaseMonsterPart1045 = {
  [32090101] = {
    id = 32090101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 96,
```

---

## Base/BaseMonsterPart1050.lua.lua
**Snippet:**
```lua
BaseMonsterPart1050 = {
  [32100101] = {
    id = 32100101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 108,
```

---

## Base/BaseMonsterPart1055.lua.lua
**Snippet:**
```lua
BaseMonsterPart1055 = {
  [32110101] = {
    id = 32110101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 120,
```

---

## Base/BaseMonsterPart1060.lua.lua
**Snippet:**
```lua
BaseMonsterPart1060 = {
  [32120101] = {
    id = 32120101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 132,
```

---

## Base/BaseMonsterPart1065.lua.lua
**Snippet:**
```lua
BaseMonsterPart1065 = {
  [32130101] = {
    id = 32130101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 141,
```

---

## Base/BaseMonsterPart1070.lua.lua
**Snippet:**
```lua
BaseMonsterPart1070 = {
  [32140101] = {
    id = 32140101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 150,
```

---

## Base/BaseMonsterPart1075.lua.lua
**Snippet:**
```lua
BaseMonsterPart1075 = {
  [32150101] = {
    id = 32150101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 159,
```

---

## Base/BaseMonsterPart1080.lua.lua
**Snippet:**
```lua
BaseMonsterPart1080 = {
  [32160101] = {
    id = 32160101,
    name = function()
      return T(80301002)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 168,
```

---

## Base/BaseMonsterPart1085.lua.lua
**Snippet:**
```lua
BaseMonsterPart1085 = {
  [32170101] = {
    id = 32170101,
    name = function()
      return T(80301002)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 177,
```

---

## Base/BaseMonsterPart1090.lua.lua
**Snippet:**
```lua
BaseMonsterPart1090 = {
  [32180101] = {
    id = 32180101,
    name = function()
      return T(80301002)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 186,
```

---

## Base/BaseMonsterPart1095.lua.lua
**Snippet:**
```lua
BaseMonsterPart1095 = {
  [32190101] = {
    id = 32190101,
    name = function()
      return T(80301002)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 195,
```

---

## Base/BaseMonsterPart1100.lua.lua
**Snippet:**
```lua
BaseMonsterPart1100 = {
  [32200101] = {
    id = 32200101,
    name = function()
      return T(80301002)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 204,
```

---

## Base/BaseMonsterPart11005.lua.lua
**Snippet:**
```lua
BaseMonsterPart11005 = {
  [52010101] = {
    id = 52010101,
    name = function()
      return T(80301904)
    end,
    type = 2,
    element_type = {3},
    star = 0,
    level = 130,
```

---

## Base/BaseMonsterPart11006.lua.lua
**Snippet:**
```lua
BaseMonsterPart11006 = {
  [52012101] = {
    id = 52012101,
    name = function()
      return T(80301904)
    end,
    type = 2,
    element_type = {3},
    star = 0,
    level = 170,
```

---

## Base/BaseMonsterPart11007.lua.lua
**Snippet:**
```lua
BaseMonsterPart11007 = {
  [52014101] = {
    id = 52014101,
    name = function()
      return T(80301903)
    end,
    type = 5,
    element_type = {2},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart11008.lua.lua
**Snippet:**
```lua
BaseMonsterPart11008 = {
  [52016101] = {
    id = 52016101,
    name = function()
      return T(80301904)
    end,
    type = 2,
    element_type = {3},
    star = 0,
    level = 80,
```

---

## Base/BaseMonsterPart11009.lua.lua
**Snippet:**
```lua
BaseMonsterPart11009 = {
  [52018101] = {
    id = 52018101,
    name = function()
      return T(80301903)
    end,
    type = 5,
    element_type = {2},
    star = 0,
    level = 120,
```

---

## Base/BaseMonsterPart11010.lua.lua
**Snippet:**
```lua
BaseMonsterPart11010 = {
  [52020101] = {
    id = 52020101,
    name = function()
      return T(80301904)
    end,
    type = 2,
    element_type = {3},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart1105.lua.lua
**Snippet:**
```lua
BaseMonsterPart1105 = {
  [32210101] = {
    id = 32210101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart1110.lua.lua
**Snippet:**
```lua
BaseMonsterPart1110 = {
  [32220101] = {
    id = 32220101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart1115.lua.lua
**Snippet:**
```lua
BaseMonsterPart1115 = {
  [32230101] = {
    id = 32230101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart1120.lua.lua
**Snippet:**
```lua
BaseMonsterPart1120 = {
  [32240101] = {
    id = 32240101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart1125.lua.lua
**Snippet:**
```lua
BaseMonsterPart1125 = {
  [32250101] = {
    id = 32250101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart1130.lua.lua
**Snippet:**
```lua
BaseMonsterPart1130 = {
  [32260101] = {
    id = 32260101,
    name = function()
      return T(80301401)
    end,
    type = 1,
    element_type = {5},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart1135.lua.lua
**Snippet:**
```lua
BaseMonsterPart1135 = {
  [32270101] = {
    id = 32270101,
    name = function()
      return T(80301501)
    end,
    type = 1,
    element_type = {4},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart1140.lua.lua
**Snippet:**
```lua
BaseMonsterPart1140 = {
  [32280101] = {
    id = 32280101,
    name = function()
      return T(80301203)
    end,
    type = 1,
    element_type = {2},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart1145.lua.lua
**Snippet:**
```lua
BaseMonsterPart1145 = {
  [32290101] = {
    id = 32290101,
    name = function()
      return T(80301303)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart1150.lua.lua
**Snippet:**
```lua
BaseMonsterPart1150 = {
  [32300101] = {
    id = 32300101,
    name = function()
      return T(80301103)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart1155.lua.lua
**Snippet:**
```lua
BaseMonsterPart1155 = {
  [32310101] = {
    id = 32310101,
    name = function()
      return T(80301401)
    end,
    type = 1,
    element_type = {5},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart1160.lua.lua
**Snippet:**
```lua
BaseMonsterPart1160 = {
  [32320101] = {
    id = 32320101,
    name = function()
      return T(80301501)
    end,
    type = 1,
    element_type = {4},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart1165.lua.lua
**Snippet:**
```lua
BaseMonsterPart1165 = {
  [32330101] = {
    id = 32330101,
    name = function()
      return T(80301203)
    end,
    type = 1,
    element_type = {2},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart1170.lua.lua
**Snippet:**
```lua
BaseMonsterPart1170 = {
  [32340101] = {
    id = 32340101,
    name = function()
      return T(80301303)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart1175.lua.lua
**Snippet:**
```lua
BaseMonsterPart1175 = {
  [32350101] = {
    id = 32350101,
    name = function()
      return T(80301103)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart1180.lua.lua
**Snippet:**
```lua
BaseMonsterPart1180 = {
  [32360101] = {
    id = 32360101,
    name = function()
      return T(80301401)
    end,
    type = 1,
    element_type = {5},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart1185.lua.lua
**Snippet:**
```lua
BaseMonsterPart1185 = {
  [32370101] = {
    id = 32370101,
    name = function()
      return T(80301501)
    end,
    type = 1,
    element_type = {4},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart1190.lua.lua
**Snippet:**
```lua
BaseMonsterPart1190 = {
  [32380101] = {
    id = 32380101,
    name = function()
      return T(80301207)
    end,
    type = 1,
    element_type = {2},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart1195.lua.lua
**Snippet:**
```lua
BaseMonsterPart1195 = {
  [32390101] = {
    id = 32390101,
    name = function()
      return T(80301303)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart1200.lua.lua
**Snippet:**
```lua
BaseMonsterPart1200 = {
  [32400101] = {
    id = 32400101,
    name = function()
      return T(80301103)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart15.lua.lua
**Snippet:**
```lua
BaseMonsterPart15 = {
  [30030101] = {
    id = 30030101,
    name = function()
      return T(80301301)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 210,
```

---

## Base/BaseMonsterPart15000.lua.lua
**Snippet:**
```lua
BaseMonsterPart15000 = {
  [30000101] = {
    id = 30000101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 210,
```

---

## Base/BaseMonsterPart15005.lua.lua
**Snippet:**
```lua
BaseMonsterPart15005 = {
  [30010101] = {
    id = 30010101,
    name = function()
      return T(80301101)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 210,
```

---

## Base/BaseMonsterPart15010.lua.lua
**Snippet:**
```lua
BaseMonsterPart15010 = {
  [30020101] = {
    id = 30020101,
    name = function()
      return T(80301201)
    end,
    type = 4,
    element_type = {2},
    star = 0,
    level = 210,
```

---

## Base/BaseMonsterPart15015.lua.lua
**Snippet:**
```lua
BaseMonsterPart15015 = {
  [30030101] = {
    id = 30030101,
    name = function()
      return T(80301301)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 210,
```

---

## Base/BaseMonsterPart15020.lua.lua
**Snippet:**
```lua
BaseMonsterPart15020 = {
  [30040101] = {
    id = 30040101,
    name = function()
      return T(80301401)
    end,
    type = 1,
    element_type = {5},
    star = 0,
    level = 210,
```

---

## Base/BaseMonsterPart15025.lua.lua
**Snippet:**
```lua
BaseMonsterPart15025 = {
  [30050101] = {
    id = 30050101,
    name = function()
      return T(80301501)
    end,
    type = 1,
    element_type = {4},
    star = 0,
    level = 210,
```

---

## Base/BaseMonsterPart15035.lua.lua
**Snippet:**
```lua
BaseMonsterPart15035 = {
  [30070101] = {
    id = 30070101,
    name = function()
      return T(80301701)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 210,
```

---

## Base/BaseMonsterPart1505.lua.lua
**Snippet:**
```lua
BaseMonsterPart1505 = {
  [33010211] = {
    id = 33010211,
    name = function()
      return T(80301409)
    end,
    type = 4,
    element_type = {5},
    star = 0,
    level = 20,
```

---

## Base/BaseMonsterPart15050.lua.lua
**Snippet:**
```lua
BaseMonsterPart15050 = {
  [30100001] = {
    id = 30100001,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 210,
```

---

## Base/BaseMonsterPart20.lua.lua
**Snippet:**
```lua
BaseMonsterPart20 = {
  [30040101] = {
    id = 30040101,
    name = function()
      return T(80301401)
    end,
    type = 1,
    element_type = {5},
    star = 0,
    level = 210,
```

---

## Base/BaseMonsterPart2000.lua.lua
**Snippet:**
```lua
BaseMonsterPart2000 = {
  [34001101] = {
    id = 34001101,
    name = function()
      return T(80301115)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 60,
```

---

## Base/BaseMonsterPart2001.lua.lua
**Snippet:**
```lua
BaseMonsterPart2001 = {
  [34002101] = {
    id = 34002101,
    name = function()
      return T(80301117)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 60,
```

---

## Base/BaseMonsterPart2005.lua.lua
**Snippet:**
```lua
BaseMonsterPart2005 = {
  [34011101] = {
    id = 34011101,
    name = function()
      return T(80301214)
    end,
    type = 4,
    element_type = {2},
    star = 0,
    level = 60,
```

---

## Base/BaseMonsterPart2006.lua.lua
**Snippet:**
```lua
BaseMonsterPart2006 = {
  [34012101] = {
    id = 34012101,
    name = function()
      return T(80301216)
    end,
    type = 4,
    element_type = {2},
    star = 0,
    level = 60,
```

---

## Base/BaseMonsterPart2010.lua.lua
**Snippet:**
```lua
BaseMonsterPart2010 = {
  [34021101] = {
    id = 34021101,
    name = function()
      return T(80301315)
    end,
    type = 2,
    element_type = {3},
    star = 0,
    level = 60,
```

---

## Base/BaseMonsterPart2011.lua.lua
**Snippet:**
```lua
BaseMonsterPart2011 = {
  [34022101] = {
    id = 34022101,
    name = function()
      return T(80301317)
    end,
    type = 2,
    element_type = {3},
    star = 0,
    level = 60,
```

---

## Base/BaseMonsterPart25.lua.lua
**Snippet:**
```lua
BaseMonsterPart25 = {
  [30050101] = {
    id = 30050101,
    name = function()
      return T(80301501)
    end,
    type = 1,
    element_type = {4},
    star = 0,
    level = 210,
```

---

## Base/BaseMonsterPart2500.lua.lua
**Snippet:**
```lua
BaseMonsterPart2500 = {
  [35001101] = {
    id = 35001101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 1,
```

---

## Base/BaseMonsterPart2501.lua.lua
**Snippet:**
```lua
BaseMonsterPart2501 = {
  [35002101] = {
    id = 35002101,
    name = function()
      return T(80301002)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 1,
```

---

## Base/BaseMonsterPart2502.lua.lua
**Snippet:**
```lua
BaseMonsterPart2502 = {
  [35004101] = {
    id = 35004101,
    name = function()
      return T(80301103)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 1,
```

---

## Base/BaseMonsterPart2505.lua.lua
**Snippet:**
```lua
BaseMonsterPart2505 = {
  [35010101] = {
    id = 35010101,
    name = function()
      return T(80301002)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 94,
```

---

## Base/BaseMonsterPart2506.lua.lua
**Snippet:**
```lua
BaseMonsterPart2506 = {
  [35012101] = {
    id = 35012101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 1,
```

---

## Base/BaseMonsterPart2507.lua.lua
**Snippet:**
```lua
BaseMonsterPart2507 = {
  [35014101] = {
    id = 35014101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 1,
```

---

## Base/BaseMonsterPart2510.lua.lua
**Snippet:**
```lua
BaseMonsterPart2510 = {
  [35020101] = {
    id = 35020101,
    name = function()
      return T(80301002)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 112,
```

---

## Base/BaseMonsterPart2511.lua.lua
**Snippet:**
```lua
BaseMonsterPart2511 = {
  [35022101] = {
    id = 35022101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 1,
```

---

## Base/BaseMonsterPart2512.lua.lua
**Snippet:**
```lua
BaseMonsterPart2512 = {
  [35024101] = {
    id = 35024101,
    name = function()
      return T(80301207)
    end,
    type = 1,
    element_type = {2},
    star = 0,
    level = 1,
```

---

## Base/BaseMonsterPart2515.lua.lua
**Snippet:**
```lua
BaseMonsterPart2515 = {
  [35030101] = {
    id = 35030101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 132,
```

---

## Base/BaseMonsterPart2520.lua.lua
**Snippet:**
```lua
BaseMonsterPart2520 = {
  [35040101] = {
    id = 35040101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 152,
```

---

## Base/BaseMonsterPart2525.lua.lua
**Snippet:**
```lua
BaseMonsterPart2525 = {
  [35050101] = {
    id = 35050101,
    name = function()
      return T(80301203)
    end,
    type = 1,
    element_type = {2},
    star = 0,
    level = 188,
```

---

## Base/BaseMonsterPart2530.lua.lua
**Snippet:**
```lua
BaseMonsterPart2530 = {
  [35060101] = {
    id = 35060101,
    name = function()
      return T(80301304)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 208,
```

---

## Base/BaseMonsterPart2535.lua.lua
**Snippet:**
```lua
BaseMonsterPart2535 = {
  [35070101] = {
    id = 35070101,
    name = function()
      return T(80301104)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart2540.lua.lua
**Snippet:**
```lua
BaseMonsterPart2540 = {
  [35080101] = {
    id = 35080101,
    name = function()
      return T(80301203)
    end,
    type = 1,
    element_type = {2},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart2545.lua.lua
**Snippet:**
```lua
BaseMonsterPart2545 = {
  [35090101] = {
    id = 35090101,
    name = function()
      return T(80301104)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart2546.lua.lua
**Snippet:**
```lua
BaseMonsterPart2546 = {
  [35092101] = {
    id = 35092101,
    name = function()
      return T(80301308)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart2550.lua.lua
**Snippet:**
```lua
BaseMonsterPart2550 = {
  [35100101] = {
    id = 35100101,
    name = function()
      return T(80301203)
    end,
    type = 1,
    element_type = {2},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart2555.lua.lua
**Snippet:**
```lua
BaseMonsterPart2555 = {
  [35110101] = {
    id = 35110101,
    name = function()
      return T(80301104)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart2560.lua.lua
**Snippet:**
```lua
BaseMonsterPart2560 = {
  [35120101] = {
    id = 35120101,
    name = function()
      return T(80301304)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart2565.lua.lua
**Snippet:**
```lua
BaseMonsterPart2565 = {
  [35130101] = {
    id = 35130101,
    name = function()
      return T(80301203)
    end,
    type = 1,
    element_type = {2},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart2570.lua.lua
**Snippet:**
```lua
BaseMonsterPart2570 = {
  [35140101] = {
    id = 35140101,
    name = function()
      return T(80301104)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart2575.lua.lua
**Snippet:**
```lua
BaseMonsterPart2575 = {
  [35150101] = {
    id = 35150101,
    name = function()
      return T(80301304)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart2580.lua.lua
**Snippet:**
```lua
BaseMonsterPart2580 = {
  [35160101] = {
    id = 35160101,
    name = function()
      return T(80301203)
    end,
    type = 1,
    element_type = {2},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart2585.lua.lua
**Snippet:**
```lua
BaseMonsterPart2585 = {
  [35170101] = {
    id = 35170101,
    name = function()
      return T(80301104)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart2590.lua.lua
**Snippet:**
```lua
BaseMonsterPart2590 = {
  [35180101] = {
    id = 35180101,
    name = function()
      return T(80301303)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart2999.lua.lua
**Snippet:**
```lua
BaseMonsterPart2999 = {
  [36000001] = {
    id = 36000001,
    type = 5,
    element_type = {0},
    star = 0,
    level = 0,
    quality = 0,
    grade = 0,
    rank = 1,
```

---

## Base/BaseMonsterPart3000.lua.lua
**Snippet:**
```lua
BaseMonsterPart3000 = {
  [36000101] = {
    id = 36000101,
    type = 5,
    element_type = {0},
    star = 0,
    level = 0,
    quality = 0,
    grade = 0,
    rank = 1,
```

---

## Base/BaseMonsterPart35.lua.lua
**Snippet:**
```lua
BaseMonsterPart35 = {
  [30070101] = {
    id = 30070101,
    name = function()
      return T(80301701)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 210,
```

---

## Base/BaseMonsterPart3500.lua.lua
**Snippet:**
```lua
BaseMonsterPart3500 = {
  [37000101] = {
    id = 37000101,
    name = function()
      return T(80301006)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 5,
```

---

## Base/BaseMonsterPart3505.lua.lua
**Snippet:**
```lua
BaseMonsterPart3505 = {
  [37010101] = {
    id = 37010101,
    name = function()
      return T(80301104)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 50,
```

---

## Base/BaseMonsterPart3510.lua.lua
**Snippet:**
```lua
BaseMonsterPart3510 = {
  [37020101] = {
    id = 37020101,
    name = function()
      return T(80301304)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 50,
```

---

## Base/BaseMonsterPart3515.lua.lua
**Snippet:**
```lua
BaseMonsterPart3515 = {
  [37030101] = {
    id = 37030101,
    name = function()
      return T(80301207)
    end,
    type = 1,
    element_type = {2},
    star = 0,
    level = 50,
```

---

## Base/BaseMonsterPart36.lua.lua
**Snippet:**
```lua
BaseMonsterPart36 = {
  [30072101] = {
    id = 30072101,
    name = function()
      return T(80301721)
    end,
    type = 2,
    element_type = {2},
    star = 0,
    level = 1,
```

---

## Base/BaseMonsterPart40.lua.lua
**Snippet:**
```lua
BaseMonsterPart40 = {
  [30080101] = {
    id = 30080101,
    name = function()
      return T(80301801)
    end,
    type = 2,
    element_type = {0},
    star = 0,
    level = 210,
```

---

## Base/BaseMonsterPart4000.lua.lua
**Snippet:**
```lua
BaseMonsterPart4000 = {
  [38000101] = {
    id = 38000101,
    name = function()
      return T(80301706)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 1,
```

---

## Base/BaseMonsterPart4010.lua.lua
**Snippet:**
```lua
BaseMonsterPart4010 = {
  [38020101] = {
    id = 38020101,
    name = function()
      return T(80301101)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 20,
```

---

## Base/BaseMonsterPart4011.lua.lua
**Snippet:**
```lua
BaseMonsterPart4011 = {
  [38022101] = {
    id = 38022101,
    name = function()
      return T(80301301)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 70,
```

---

## Base/BaseMonsterPart4015.lua.lua
**Snippet:**
```lua
BaseMonsterPart4015 = {
  [38030101] = {
    id = 38030101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 100,
```

---

## Base/BaseMonsterPart4020.lua.lua
**Snippet:**
```lua
BaseMonsterPart4020 = {
  [38040101] = {
    id = 38040101,
    name = function()
      return T(80301302)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 70,
```

---

## Base/BaseMonsterPart4021.lua.lua
**Snippet:**
```lua
BaseMonsterPart4021 = {
  [38042101] = {
    id = 38042101,
    name = function()
      return T(80301402)
    end,
    type = 1,
    element_type = {5},
    star = 0,
    level = 70,
```

---

## Base/BaseMonsterPart4025.lua.lua
**Snippet:**
```lua
BaseMonsterPart4025 = {
  [38051101] = {
    id = 38051101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 70,
```

---

## Base/BaseMonsterPart4026.lua.lua
**Snippet:**
```lua
BaseMonsterPart4026 = {
  [38052101] = {
    id = 38052101,
    name = function()
      return T(80301401)
    end,
    type = 1,
    element_type = {5},
    star = 0,
    level = 70,
```

---

## Base/BaseMonsterPart4027.lua.lua
**Snippet:**
```lua
BaseMonsterPart4027 = {
  [38054101] = {
    id = 38054101,
    name = function()
      return T(80301207)
    end,
    type = 1,
    element_type = {2},
    star = 0,
    level = 70,
```

---

## Base/BaseMonsterPart4030.lua.lua
**Snippet:**
```lua
BaseMonsterPart4030 = {
  [38061101] = {
    id = 38061101,
    name = function()
      return T(80301012)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 70,
```

---

## Base/BaseMonsterPart4031.lua.lua
**Snippet:**
```lua
BaseMonsterPart4031 = {
  [38062101] = {
    id = 38062101,
    name = function()
      return T(80301408)
    end,
    type = 2,
    element_type = {5},
    star = 0,
    level = 70,
```

---

## Base/BaseMonsterPart4032.lua.lua
**Snippet:**
```lua
BaseMonsterPart4032 = {
  [38064101] = {
    id = 38064101,
    name = function()
      return T(80301510)
    end,
    type = 5,
    element_type = {4},
    star = 0,
    level = 70,
```

---

## Base/BaseMonsterPart4035.lua.lua
**Snippet:**
```lua
BaseMonsterPart4035 = {
  [38071101] = {
    id = 38071101,
    name = function()
      return T(80301801)
    end,
    type = 2,
    element_type = {0},
    star = 0,
    level = 70,
```

---

## Base/BaseMonsterPart4036.lua.lua
**Snippet:**
```lua
BaseMonsterPart4036 = {
  [38072101] = {
    id = 38072101,
    name = function()
      return T(80301803)
    end,
    type = 5,
    element_type = {0},
    star = 0,
    level = 70,
```

---

## Base/BaseMonsterPart4040.lua.lua
**Snippet:**
```lua
BaseMonsterPart4040 = {
  [38080101] = {
    id = 38080101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 200,
```

---

## Base/BaseMonsterPart4041.lua.lua
**Snippet:**
```lua
BaseMonsterPart4041 = {
  [38082101] = {
    id = 38082101,
    name = function()
      return T(80301108)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart4050.lua.lua
**Snippet:**
```lua
BaseMonsterPart4050 = {
  [38100101] = {
    id = 38100101,
    name = function()
      return T(80301006)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 140,
```

---

## Base/BaseMonsterPart4060.lua.lua
**Snippet:**
```lua
BaseMonsterPart4060 = {
  [38120101] = {
    id = 38120101,
    name = function()
      return T(80301411)
    end,
    type = 5,
    element_type = {5},
    star = 0,
    level = 20,
```

---

## Base/BaseMonsterPart4061.lua.lua
**Snippet:**
```lua
BaseMonsterPart4061 = {
  [38122101] = {
    id = 38122101,
    name = function()
      return T(80301016)
    end,
    type = 2,
    element_type = {1},
    star = 0,
    level = 20,
```

---

## Base/BaseMonsterPart4062.lua.lua
**Snippet:**
```lua
BaseMonsterPart4062 = {
  [38124101] = {
    id = 38124101,
    name = function()
      return T(80301411)
    end,
    type = 5,
    element_type = {5},
    star = 0,
    level = 20,
```

---

## Base/BaseMonsterPart4063.lua.lua
**Snippet:**
```lua
BaseMonsterPart4063 = {
  [38126101] = {
    id = 38126101,
    name = function()
      return T(80301016)
    end,
    type = 2,
    element_type = {1},
    star = 0,
    level = 20,
```

---

## Base/BaseMonsterPart4064.lua.lua
**Snippet:**
```lua
BaseMonsterPart4064 = {
  [38128101] = {
    id = 38128101,
    name = function()
      return T(80301113)
    end,
    type = 5,
    element_type = {3},
    star = 0,
    level = 20,
```

---

## Base/BaseMonsterPart45.lua.lua
**Snippet:**
```lua
BaseMonsterPart45 = {
  [30090301] = {
    id = 30090301,
    name = function()
      return T(80301903)
    end,
    type = 5,
    element_type = {2},
    star = 0,
    level = 210,
```

---

## Base/BaseMonsterPart4500.lua.lua
**Snippet:**
```lua
BaseMonsterPart4500 = {
  [39000101] = {
    id = 39000101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 20,
```

---

## Base/BaseMonsterPart4501.lua.lua
**Snippet:**
```lua
BaseMonsterPart4501 = {
  [39002101] = {
    id = 39002101,
    name = function()
      return T(80301007)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 100,
```

---

## Base/BaseMonsterPart4502.lua.lua
**Snippet:**
```lua
BaseMonsterPart4502 = {
  [39004101] = {
    id = 39004101,
    name = function()
      return T(80301011)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 130,
```

---

## Base/BaseMonsterPart4503.lua.lua
**Snippet:**
```lua
BaseMonsterPart4503 = {
  [39006101] = {
    id = 39006101,
    name = function()
      return T(80301103)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 90,
```

---

## Base/BaseMonsterPart4504.lua.lua
**Snippet:**
```lua
BaseMonsterPart4504 = {
  [39008101] = {
    id = 39008101,
    name = function()
      return T(80301203)
    end,
    type = 1,
    element_type = {2},
    star = 0,
    level = 45,
```

---

## Base/BaseMonsterPart4505.lua.lua
**Snippet:**
```lua
BaseMonsterPart4505 = {
  [39010101] = {
    id = 39010101,
    name = function()
      return T(80301012)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart4506.lua.lua
**Snippet:**
```lua
BaseMonsterPart4506 = {
  [39012101] = {
    id = 39012101,
    name = function()
      return T(80301501)
    end,
    type = 1,
    element_type = {4},
    star = 0,
    level = 110,
```

---

## Base/BaseMonsterPart4507.lua.lua
**Snippet:**
```lua
BaseMonsterPart4507 = {
  [39014101] = {
    id = 39014101,
    name = function()
      return T(80301012)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 40,
```

---

## Base/BaseMonsterPart4508.lua.lua
**Snippet:**
```lua
BaseMonsterPart4508 = {
  [39016101] = {
    id = 39016101,
    name = function()
      return T(80301209)
    end,
    type = 2,
    element_type = {2},
    star = 0,
    level = 80,
```

---

## Base/BaseMonsterPart4509.lua.lua
**Snippet:**
```lua
BaseMonsterPart4509 = {
  [39018101] = {
    id = 39018101,
    name = function()
      return T(80301304)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 85,
```

---

## Base/BaseMonsterPart4510.lua.lua
**Snippet:**
```lua
BaseMonsterPart4510 = {
  [39020101] = {
    id = 39020101,
    name = function()
      return T(80301002)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 25,
```

---

## Base/BaseMonsterPart4511.lua.lua
**Snippet:**
```lua
BaseMonsterPart4511 = {
  [39022101] = {
    id = 39022101,
    name = function()
      return T(80301406)
    end,
    type = 1,
    element_type = {5},
    star = 0,
    level = 130,
```

---

## Base/BaseMonsterPart4512.lua.lua
**Snippet:**
```lua
BaseMonsterPart4512 = {
  [39024101] = {
    id = 39024101,
    name = function()
      return T(80301203)
    end,
    type = 1,
    element_type = {2},
    star = 0,
    level = 60,
```

---

## Base/BaseMonsterPart4513.lua.lua
**Snippet:**
```lua
BaseMonsterPart4513 = {
  [39026101] = {
    id = 39026101,
    name = function()
      return T(80301209)
    end,
    type = 2,
    element_type = {2},
    star = 0,
    level = 140,
```

---

## Base/BaseMonsterPart4514.lua.lua
**Snippet:**
```lua
BaseMonsterPart4514 = {
  [39028101] = {
    id = 39028101,
    name = function()
      return T(80301103)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 95,
```

---

## Base/BaseMonsterPart4515.lua.lua
**Snippet:**
```lua
BaseMonsterPart4515 = {
  [39030101] = {
    id = 39030101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 30,
```

---

## Base/BaseMonsterPart4516.lua.lua
**Snippet:**
```lua
BaseMonsterPart4516 = {
  [39032101] = {
    id = 39032101,
    name = function()
      return T(80301304)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 65,
```

---

## Base/BaseMonsterPart4517.lua.lua
**Snippet:**
```lua
BaseMonsterPart4517 = {
  [39034101] = {
    id = 39034101,
    name = function()
      return T(80301104)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 55,
```

---

## Base/BaseMonsterPart4518.lua.lua
**Snippet:**
```lua
BaseMonsterPart4518 = {
  [39036101] = {
    id = 39036101,
    name = function()
      return T(80301507)
    end,
    type = 1,
    element_type = {4},
    star = 0,
    level = 150,
```

---

## Base/BaseMonsterPart4519.lua.lua
**Snippet:**
```lua
BaseMonsterPart4519 = {
  [39038101] = {
    id = 39038101,
    name = function()
      return T(80301402)
    end,
    type = 1,
    element_type = {5},
    star = 0,
    level = 115,
```

---

## Base/BaseMonsterPart4520.lua.lua
**Snippet:**
```lua
BaseMonsterPart4520 = {
  [39040101] = {
    id = 39040101,
    name = function()
      return T(80301304)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 45,
```

---

## Base/BaseMonsterPart4521.lua.lua
**Snippet:**
```lua
BaseMonsterPart4521 = {
  [39042101] = {
    id = 39042101,
    name = function()
      return T(80301307)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 90,
```

---

## Base/BaseMonsterPart4522.lua.lua
**Snippet:**
```lua
BaseMonsterPart4522 = {
  [39044101] = {
    id = 39044101,
    name = function()
      return T(80301104)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 85,
```

---

## Base/BaseMonsterPart4523.lua.lua
**Snippet:**
```lua
BaseMonsterPart4523 = {
  [39046101] = {
    id = 39046101,
    name = function()
      return T(80301002)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 25,
```

---

## Base/BaseMonsterPart4524.lua.lua
**Snippet:**
```lua
BaseMonsterPart4524 = {
  [39048101] = {
    id = 39048101,
    name = function()
      return T(80301507)
    end,
    type = 1,
    element_type = {4},
    star = 0,
    level = 130,
```

---

## Base/BaseMonsterPart4525.lua.lua
**Snippet:**
```lua
BaseMonsterPart4525 = {
  [39050101] = {
    id = 39050101,
    name = function()
      return T(80301304)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 60,
```

---

## Base/BaseMonsterPart4526.lua.lua
**Snippet:**
```lua
BaseMonsterPart4526 = {
  [39052101] = {
    id = 39052101,
    name = function()
      return T(80301207)
    end,
    type = 1,
    element_type = {2},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart4527.lua.lua
**Snippet:**
```lua
BaseMonsterPart4527 = {
  [39054101] = {
    id = 39054101,
    name = function()
      return T(80301308)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 100,
```

---

## Base/BaseMonsterPart4528.lua.lua
**Snippet:**
```lua
BaseMonsterPart4528 = {
  [39056101] = {
    id = 39056101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 30,
```

---

## Base/BaseMonsterPart4529.lua.lua
**Snippet:**
```lua
BaseMonsterPart4529 = {
  [39058101] = {
    id = 39058101,
    name = function()
      return T(80301507)
    end,
    type = 1,
    element_type = {4},
    star = 0,
    level = 65,
```

---

## Base/BaseMonsterPart4530.lua.lua
**Snippet:**
```lua
BaseMonsterPart4530 = {
  [39060101] = {
    id = 39060101,
    name = function()
      return T(80301203)
    end,
    type = 1,
    element_type = {2},
    star = 0,
    level = 75,
```

---

## Base/BaseMonsterPart4531.lua.lua
**Snippet:**
```lua
BaseMonsterPart4531 = {
  [39062101] = {
    id = 39062101,
    name = function()
      return T(80301108)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart4532.lua.lua
**Snippet:**
```lua
BaseMonsterPart4532 = {
  [39064101] = {
    id = 39064101,
    name = function()
      return T(80301402)
    end,
    type = 1,
    element_type = {5},
    star = 0,
    level = 115,
```

---

## Base/BaseMonsterPart4533.lua.lua
**Snippet:**
```lua
BaseMonsterPart4533 = {
  [39066101] = {
    id = 39066101,
    name = function()
      return T(80301203)
    end,
    type = 1,
    element_type = {2},
    star = 0,
    level = 45,
```

---

## Base/BaseMonsterPart4534.lua.lua
**Snippet:**
```lua
BaseMonsterPart4534 = {
  [39068101] = {
    id = 39068101,
    name = function()
      return T(80301308)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 140,
```

---

## Base/BaseMonsterPart4535.lua.lua
**Snippet:**
```lua
BaseMonsterPart4535 = {
  [39070101] = {
    id = 39070101,
    name = function()
      return T(80301103)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 95,
```

---

## Base/BaseMonsterPart47.lua.lua
**Snippet:**
```lua
BaseMonsterPart47 = {
  [30095001] = {
    id = 30095001,
    name = function()
      return T(80301950)
    end,
    type = 5,
    element_type = {4},
    star = 0,
    level = 210,
```

---

## Base/BaseMonsterPart49.lua.lua
**Snippet:**
```lua
BaseMonsterPart49 = {
  [30100001] = {
    id = 30100001,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 210,
```

---

## Base/BaseMonsterPart499.lua.lua
**Snippet:**
```lua
BaseMonsterPart499 = {
  [31000001] = {
    id = 31000001,
    name = function()
      return T(80301702)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 1,
```

---

## Base/BaseMonsterPart5.lua.lua
**Snippet:**
```lua
BaseMonsterPart5 = {
  [30010101] = {
    id = 30010101,
    name = function()
      return T(80301101)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 210,
```

---

## Base/BaseMonsterPart500.lua.lua
**Snippet:**
```lua
BaseMonsterPart500 = {
  [31001001] = {
    id = 31001001,
    name = function()
      return T(80301713)
    end,
    type = 2,
    element_type = {4},
    star = 0,
    level = 1,
```

---

## Base/BaseMonsterPart505.lua.lua
**Snippet:**
```lua
BaseMonsterPart505 = {
  [31010101] = {
    id = 31010101,
    name = function()
      return T(80301002)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 1,
```

---

## Base/BaseMonsterPart510.lua.lua
**Snippet:**
```lua
BaseMonsterPart510 = {
  [31020101] = {
    id = 31020101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 1,
```

---

## Base/BaseMonsterPart515.lua.lua
**Snippet:**
```lua
BaseMonsterPart515 = {
  [31030101] = {
    id = 31030101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 25,
```

---

## Base/BaseMonsterPart520.lua.lua
**Snippet:**
```lua
BaseMonsterPart520 = {
  [31040101] = {
    id = 31040101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 52,
```

---

## Base/BaseMonsterPart525.lua.lua
**Snippet:**
```lua
BaseMonsterPart525 = {
  [31050101] = {
    id = 31050101,
    name = function()
      return T(80301002)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 72,
```

---

## Base/BaseMonsterPart530.lua.lua
**Snippet:**
```lua
BaseMonsterPart530 = {
  [31060101] = {
    id = 31060101,
    name = function()
      return T(80301304)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 93,
```

---

## Base/BaseMonsterPart535.lua.lua
**Snippet:**
```lua
BaseMonsterPart535 = {
  [31070101] = {
    id = 31070101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 117,
```

---

## Base/BaseMonsterPart540.lua.lua
**Snippet:**
```lua
BaseMonsterPart540 = {
  [31080101] = {
    id = 31080101,
    name = function()
      return T(80301002)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 131,
```

---

## Base/BaseMonsterPart545.lua.lua
**Snippet:**
```lua
BaseMonsterPart545 = {
  [31090101] = {
    id = 31090101,
    name = function()
      return T(80301002)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 152,
```

---

## Base/BaseMonsterPart550.lua.lua
**Snippet:**
```lua
BaseMonsterPart550 = {
  [31100101] = {
    id = 31100101,
    name = function()
      return T(80301203)
    end,
    type = 1,
    element_type = {2},
    star = 0,
    level = 185,
```

---

## Base/BaseMonsterPart555.lua.lua
**Snippet:**
```lua
BaseMonsterPart555 = {
  [31110101] = {
    id = 31110101,
    name = function()
      return T(80301104)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 205,
```

---

## Base/BaseMonsterPart560.lua.lua
**Snippet:**
```lua
BaseMonsterPart560 = {
  [31120101] = {
    id = 31120101,
    name = function()
      return T(80301303)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart565.lua.lua
**Snippet:**
```lua
BaseMonsterPart565 = {
  [31130101] = {
    id = 31130101,
    name = function()
      return T(80301203)
    end,
    type = 1,
    element_type = {2},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart570.lua.lua
**Snippet:**
```lua
BaseMonsterPart570 = {
  [31140101] = {
    id = 31140101,
    name = function()
      return T(80301104)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart575.lua.lua
**Snippet:**
```lua
BaseMonsterPart575 = {
  [31150101] = {
    id = 31150101,
    name = function()
      return T(80301304)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart580.lua.lua
**Snippet:**
```lua
BaseMonsterPart580 = {
  [31160101] = {
    id = 31160101,
    name = function()
      return T(80301203)
    end,
    type = 1,
    element_type = {2},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart585.lua.lua
**Snippet:**
```lua
BaseMonsterPart585 = {
  [31170101] = {
    id = 31170101,
    name = function()
      return T(80301103)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart590.lua.lua
**Snippet:**
```lua
BaseMonsterPart590 = {
  [31180101] = {
    id = 31180101,
    name = function()
      return T(80301303)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart595.lua.lua
**Snippet:**
```lua
BaseMonsterPart595 = {
  [31190101] = {
    id = 31190101,
    name = function()
      return T(80301203)
    end,
    type = 1,
    element_type = {2},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart755.lua.lua
**Snippet:**
```lua
BaseMonsterPart755 = {
  [31510101] = {
    id = 31510101,
    name = function()
      return T(80301002)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 50,
```

---

## Base/BaseMonsterPart760.lua.lua
**Snippet:**
```lua
BaseMonsterPart760 = {
  [31520101] = {
    id = 31520101,
    name = function()
      return T(80301002)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 68,
```

---

## Base/BaseMonsterPart765.lua.lua
**Snippet:**
```lua
BaseMonsterPart765 = {
  [31530101] = {
    id = 31530101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 88,
```

---

## Base/BaseMonsterPart770.lua.lua
**Snippet:**
```lua
BaseMonsterPart770 = {
  [31540101] = {
    id = 31540101,
    name = function()
      return T(80301001)
    end,
    type = 1,
    element_type = {0},
    star = 0,
    level = 108,
```

---

## Base/BaseMonsterPart775.lua.lua
**Snippet:**
```lua
BaseMonsterPart775 = {
  [31550101] = {
    id = 31550101,
    name = function()
      return T(80301203)
    end,
    type = 1,
    element_type = {2},
    star = 0,
    level = 144,
```

---

## Base/BaseMonsterPart780.lua.lua
**Snippet:**
```lua
BaseMonsterPart780 = {
  [31560101] = {
    id = 31560101,
    name = function()
      return T(80301304)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 168,
```

---

## Base/BaseMonsterPart785.lua.lua
**Snippet:**
```lua
BaseMonsterPart785 = {
  [31570101] = {
    id = 31570101,
    name = function()
      return T(80301104)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 194,
```

---

## Base/BaseMonsterPart790.lua.lua
**Snippet:**
```lua
BaseMonsterPart790 = {
  [31580101] = {
    id = 31580101,
    name = function()
      return T(80301203)
    end,
    type = 1,
    element_type = {2},
    star = 0,
    level = 214,
```

---

## Base/BaseMonsterPart795.lua.lua
**Snippet:**
```lua
BaseMonsterPart795 = {
  [31590101] = {
    id = 31590101,
    name = function()
      return T(80301104)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart796.lua.lua
**Snippet:**
```lua
BaseMonsterPart796 = {
  [31592101] = {
    id = 31592101,
    name = function()
      return T(80301308)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart800.lua.lua
**Snippet:**
```lua
BaseMonsterPart800 = {
  [31600101] = {
    id = 31600101,
    name = function()
      return T(80301203)
    end,
    type = 1,
    element_type = {2},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart805.lua.lua
**Snippet:**
```lua
BaseMonsterPart805 = {
  [31610101] = {
    id = 31610101,
    name = function()
      return T(80301104)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart810.lua.lua
**Snippet:**
```lua
BaseMonsterPart810 = {
  [31620101] = {
    id = 31620101,
    name = function()
      return T(80301304)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart815.lua.lua
**Snippet:**
```lua
BaseMonsterPart815 = {
  [31630101] = {
    id = 31630101,
    name = function()
      return T(80301203)
    end,
    type = 1,
    element_type = {2},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart820.lua.lua
**Snippet:**
```lua
BaseMonsterPart820 = {
  [31640101] = {
    id = 31640101,
    name = function()
      return T(80301104)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart825.lua.lua
**Snippet:**
```lua
BaseMonsterPart825 = {
  [31650101] = {
    id = 31650101,
    name = function()
      return T(80301304)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart830.lua.lua
**Snippet:**
```lua
BaseMonsterPart830 = {
  [31660101] = {
    id = 31660101,
    name = function()
      return T(80301203)
    end,
    type = 1,
    element_type = {2},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart835.lua.lua
**Snippet:**
```lua
BaseMonsterPart835 = {
  [31670101] = {
    id = 31670101,
    name = function()
      return T(80301104)
    end,
    type = 1,
    element_type = {1},
    star = 0,
    level = 220,
```

---

## Base/BaseMonsterPart840.lua.lua
**Snippet:**
```lua
BaseMonsterPart840 = {
  [31680101] = {
    id = 31680101,
    name = function()
      return T(80301303)
    end,
    type = 1,
    element_type = {3},
    star = 0,
    level = 220,
```

---

## Base/BaseName.lua.lua
**Snippet:**
```lua
BaseName = {
  [1] = {
    id = 1,
    name = function()
      return T(87100001)
    end
  },
  [2] = {
    id = 2,
    name = function()
```

---

## Base/BaseNamePlayer.lua.lua
**Snippet:**
```lua
BaseNamePlayer = {
  [1] = {
    id = 1,
    name = function()
      return T(87110001)
    end
  },
  [2] = {
    id = 2,
    name = function()
```

---

## Base/BasePayProduct.lua.lua
**Snippet:**
```lua
BasePayProduct = {
  [25000001] = {
    id = 25000001,
    product_id = "cn.haoplay.elpis.diamond1",
    name = function()
      return T(80615001)
    end,
    icon = "Shop:Recharge_1",
    type = 1,
    price = 6,
```

---

## Base/BasePlayerLevelUp.lua.lua
**Snippet:**
```lua
BasePlayerLevelUp = {
  [1] = {
    id = 1,
    next_exp = 15,
    max_energy = 80,
    reward = {
      "1:21000004:30"
    },
    arrange_num = 4,
    arrange_next_id = 3,
```

---

## Base/BasePlotDialog.lua.lua
**Snippet:**
```lua
BasePlotDialog = {
  [1010101001] = {
    id = 1010101001,
    talk_text = function()
      return T_S(10101010010)
    end,
    scale = {10000},
    skin = {"broken"},
    blink_timeline = {
      "Assets/Art/PlotPlay/Timeline/BlinkTemplate/90110001/90110001_0.playable"
```

---

## Base/BasePlotDialogPart0.lua.lua
**Snippet:**
```lua
BasePlotDialogPart0 = {
  [1000101001] = {
    id = 1000101001,
    talk_text = function()
      return T_S(10001010010)
    end,
    next_dialog = 1000101002,
    env_sound = 20002
  },
  [1000101002] = {
```

---

## Base/BasePlotDialogPart100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart100 = {
  [1000301001] = {
    id = 1000301001,
    talk_text = function()
      return T_S(10003010010)
    end,
    next_dialog = 1000301002,
    env_sound = 20007
  },
  [1000301002] = {
```

---

## Base/BasePlotDialogPart10000.lua.lua
**Snippet:**
```lua
BasePlotDialogPart10000 = {
  [1020101001] = {
    id = 1020101001,
    talk_text = function()
      return T_S(10201010010)
    end,
    is_master = 1,
    next_dialog = 1020101002,
    text_sound_path = "event:/voice_cn/story/M0000/M0000_story_00028",
    text_sound_bank = "bank:/voice_cn/sty/M0000_1",
```

---

## Base/BasePlotDialogPart10050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart10050 = {
  [1020201001] = {
    id = 1020201001,
    talk_text = function()
      return T_S(10202010010)
    end,
    next_dialog = 1020201002,
    env_sound = 20007
  },
  [1020201002] = {
```

---

## Base/BasePlotDialogPart10051.lua.lua
**Snippet:**
```lua
BasePlotDialogPart10051 = {
  [1020203001] = {
    id = 1020203001,
    talk_text = function()
      return T_S(10202030010)
    end,
    role_ids = {90110001},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart10100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart10100 = {
  [1020301001] = {
    id = 1020301001,
    talk_text = function()
      return T_S(10203010010)
    end,
    role_ids = {90110001},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart10101.lua.lua
**Snippet:**
```lua
BasePlotDialogPart10101 = {
  [1020303001] = {
    id = 1020303001,
    talk_text = function()
      return T_S(10203030010)
    end,
    role_ids = {90110015, 90110016},
    scale = {10000, 10000},
    action = {"", ""},
    action_timeline = {
```

---

## Base/BasePlotDialogPart10150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart10150 = {
  [1020401001] = {
    id = 1020401001,
    talk_text = function()
      return T_S(10204010010)
    end,
    role_ids = {90110001, 90110002},
    scale = {10000, 10000},
    skin = {"common", "common"},
    action = {"", ""},
```

---

## Base/BasePlotDialogPart10151.lua.lua
**Snippet:**
```lua
BasePlotDialogPart10151 = {
  [1020403001] = {
    id = 1020403001,
    talk_text = function()
      return T_S(10204030010)
    end,
    next_dialog = 1020403002,
    speak_head = 90120012,
    speak_head_actions = {
      "idle",
```

---

## Base/BasePlotDialogPart150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart150 = {
  [1000401001] = {
    id = 1000401001,
    talk_text = function()
      return T_S(10004010010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart15000.lua.lua
**Snippet:**
```lua
BasePlotDialogPart15000 = {
  [1030101001] = {
    id = 1030101001,
    talk_text = function()
      return T_S(10301010010)
    end,
    role_ids = {90110002},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart15001.lua.lua
**Snippet:**
```lua
BasePlotDialogPart15001 = {
  [1030103001] = {
    id = 1030103001,
    talk_text = function()
      return T_S(10301030010)
    end,
    next_dialog = 1030103002,
    speak_head = 90120028,
    speak_head_actions = {
      "talk",
```

---

## Base/BasePlotDialogPart15050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart15050 = {
  [1030201001] = {
    id = 1030201001,
    talk_text = function()
      return T_S(10302010010)
    end,
    next_dialog = 1030201002,
    env_sound = 20005,
    open_title_1 = function()
      return T_S(10302010018)
```

---

## Base/BasePlotDialogPart15053.lua.lua
**Snippet:**
```lua
BasePlotDialogPart15053 = {
  [1030207001] = {
    id = 1030207001,
    talk_text = function()
      return T_S(10302070010)
    end,
    role_ids = {90110001},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart15054.lua.lua
**Snippet:**
```lua
BasePlotDialogPart15054 = {
  [1030210001] = {
    id = 1030210001,
    talk_text = function()
      return T_S(10302100010)
    end,
    next_dialog = 1030210002,
    env_sound = 20007
  },
  [1030210002] = {
```

---

## Base/BasePlotDialogPart15055.lua.lua
**Snippet:**
```lua
BasePlotDialogPart15055 = {
  [1030211001] = {
    id = 1030211001,
    middle_text = function()
      return T_S(10302110013)
    end,
    speak_name = function()
      return T_S(10302110015)
    end,
    text_sound_path = "event:/voice_cn/story/M0001/M0001_story_00055",
```

---

## Base/BasePlotDialogPart15100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart15100 = {
  [1030301001] = {
    id = 1030301001,
    talk_text = function()
      return T_S(10303010010)
    end,
    next_dialog = 1030301002,
    speak_name = function()
      return T_S(10303010015)
    end,
```

---

## Base/BasePlotDialogPart15101.lua.lua
**Snippet:**
```lua
BasePlotDialogPart15101 = {
  [1030303001] = {
    id = 1030303001,
    cg_text = function()
      return T_S(10303030017)
    end,
    cg_position_scale = "-312:-85:8200",
    next_dialog = 1030303002,
    speak_name = function()
      return T_S(10303030015)
```

---

## Base/BasePlotDialogPart15150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart15150 = {
  [1030401001] = {
    id = 1030401001,
    middle_text = function()
      return T_S(10304010013)
    end,
    next_dialog = 1030401002,
    env_sound = 20008,
    open_title_1 = function()
      return T_S(10304010018)
```

---

## Base/BasePlotDialogPart200.lua.lua
**Snippet:**
```lua
BasePlotDialogPart200 = {
  [1000501001] = {
    id = 1000501001,
    talk_text = function()
      return T_S(10005010010)
    end,
    role_ids = {90110001},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart20000.lua.lua
**Snippet:**
```lua
BasePlotDialogPart20000 = {
  [1040101001] = {
    id = 1040101001,
    next_dialog = 1040101002,
    camera_shake = {
      "2",
      "0",
      "1800"
    },
    env_sound = 20001,
```

---

## Base/BasePlotDialogPart20001.lua.lua
**Snippet:**
```lua
BasePlotDialogPart20001 = {
  [1040103001] = {
    id = 1040103001,
    talk_text = function()
      return T_S(10401030010)
    end,
    next_dialog = 1040103002,
    speak_head = 90120026,
    speak_head_actions = {
      "talk",
```

---

## Base/BasePlotDialogPart20050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart20050 = {
  [1040201001] = {
    id = 1040201001,
    talk_text = function()
      return T_S(10402010010)
    end,
    next_dialog = 1040201002,
    speak_head = 90120026,
    speak_head_actions = {
      "idle",
```

---

## Base/BasePlotDialogPart20051.lua.lua
**Snippet:**
```lua
BasePlotDialogPart20051 = {
  [1040203001] = {
    id = 1040203001,
    talk_text = function()
      return T_S(10402030010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart20052.lua.lua
**Snippet:**
```lua
BasePlotDialogPart20052 = {
  [1040205001] = {
    id = 1040205001,
    talk_text = function()
      return T_S(10402050010)
    end,
    role_ids = {90110006},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/DialogAction/1040205001/1040205001_90110006.playable"
```

---

## Base/BasePlotDialogPart20100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart20100 = {
  [1040301001] = {
    id = 1040301001,
    talk_text = function()
      return T_S(10403010010)
    end,
    next_dialog = 1040301002,
    speak_name = function()
      return T_S(10403010015)
    end,
```

---

## Base/BasePlotDialogPart20101.lua.lua
**Snippet:**
```lua
BasePlotDialogPart20101 = {
  [1040303001] = {
    id = 1040303001,
    talk_text = function()
      return T_S(10403030010)
    end,
    role_ids = {90110004},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart20102.lua.lua
**Snippet:**
```lua
BasePlotDialogPart20102 = {
  [1040305001] = {
    id = 1040305001,
    talk_text = function()
      return T_S(10403050010)
    end,
    role_ids = {90110004},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart20103.lua.lua
**Snippet:**
```lua
BasePlotDialogPart20103 = {
  [1040307001] = {
    id = 1040307001,
    talk_text = function()
      return T_S(10403070010)
    end,
    next_dialog = 1040307002,
    env_sound = 20005
  },
  [1040307002] = {
```

---

## Base/BasePlotDialogPart20150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart20150 = {
  [1040401001] = {
    id = 1040401001,
    talk_text = function()
      return T_S(10404010010)
    end,
    next_dialog = 1040401002,
    speak_name = function()
      return T_S(10404010015)
    end,
```

---

## Base/BasePlotDialogPart20151.lua.lua
**Snippet:**
```lua
BasePlotDialogPart20151 = {
  [1040403001] = {
    id = 1040403001,
    talk_text = function()
      return T_S(10404030010)
    end,
    next_dialog = 1040403002,
    speak_head = 90120035,
    speak_head_actions = {
      "talk",
```

---

## Base/BasePlotDialogPart20200.lua.lua
**Snippet:**
```lua
BasePlotDialogPart20200 = {
  [1040501001] = {
    id = 1040501001,
    talk_text = function()
      return T_S(10405010010)
    end,
    role_ids = {90110004},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart20250.lua.lua
**Snippet:**
```lua
BasePlotDialogPart20250 = {
  [1040601001] = {
    id = 1040601001,
    talk_text = function()
      return T_S(10406010010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart20251.lua.lua
**Snippet:**
```lua
BasePlotDialogPart20251 = {
  [1040603001] = {
    id = 1040603001,
    talk_text = function()
      return T_S(10406030010)
    end,
    role_ids = {90110008},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/DialogAction/1040603001/1040603001_90110008.playable"
```

---

## Base/BasePlotDialogPart20252.lua.lua
**Snippet:**
```lua
BasePlotDialogPart20252 = {
  [1040605001] = {
    id = 1040605001,
    talk_text = function()
      return T_S(10406050010)
    end,
    role_ids = {90110002},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart20300.lua.lua
**Snippet:**
```lua
BasePlotDialogPart20300 = {
  [1040701001] = {
    id = 1040701001,
    talk_text = function()
      return T_S(10407010010)
    end,
    role_ids = {90110001},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart20400.lua.lua
**Snippet:**
```lua
BasePlotDialogPart20400 = {
  [1040901001] = {
    id = 1040901001,
    talk_text = function()
      return T_S(10409010010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart20401.lua.lua
**Snippet:**
```lua
BasePlotDialogPart20401 = {
  [1040903001] = {
    id = 1040903001,
    talk_text = function()
      return T_S(10409030010)
    end,
    role_ids = {90110003, 90110002},
    scale = {10000, 10000},
    skin = {"common", "common"},
    action = {"", ""},
```

---

## Base/BasePlotDialogPart250.lua.lua
**Snippet:**
```lua
BasePlotDialogPart250 = {
  [1000601001] = {
    id = 1000601001,
    talk_text = function()
      return T_S(10006010010)
    end,
    is_master = 1,
    role_ids = {90110006},
    scale = {10000},
    action_timeline = {
```

---

## Base/BasePlotDialogPart25000.lua.lua
**Snippet:**
```lua
BasePlotDialogPart25000 = {
  [1050101001] = {
    id = 1050101001,
    talk_text = function()
      return T_S(10501010010)
    end,
    role_ids = {90110004},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart25001.lua.lua
**Snippet:**
```lua
BasePlotDialogPart25001 = {
  [1050103001] = {
    id = 1050103001,
    talk_text = function()
      return T_S(10501030010)
    end,
    role_ids = {90110004},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart25002.lua.lua
**Snippet:**
```lua
BasePlotDialogPart25002 = {
  [1050105001] = {
    id = 1050105001,
    next_dialog = 1050105002,
    camera_shake = {
      "2",
      "0",
      "1200"
    },
    env_sound = 20004,
```

---

## Base/BasePlotDialogPart25050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart25050 = {
  [1050201001] = {
    id = 1050201001,
    talk_text = function()
      return T_S(10502010010)
    end,
    scale = {10000},
    next_dialog = 1050201002,
    env_sound = 20002
  },
```

---

## Base/BasePlotDialogPart25051.lua.lua
**Snippet:**
```lua
BasePlotDialogPart25051 = {
  [1050203001] = {
    id = 1050203001,
    talk_text = function()
      return T_S(10502030010)
    end,
    role_ids = {90110015, 90110016},
    scale = {10000, 10000},
    action = {"", ""},
    action_timeline = {
```

---

## Base/BasePlotDialogPart25052.lua.lua
**Snippet:**
```lua
BasePlotDialogPart25052 = {
  [1050205001] = {
    id = 1050205001,
    talk_text = function()
      return T_S(10502050010)
    end,
    role_ids = {90110015, 90110016},
    scale = {10000, 10000},
    action = {"", ""},
    action_timeline = {
```

---

## Base/BasePlotDialogPart25053.lua.lua
**Snippet:**
```lua
BasePlotDialogPart25053 = {
  [1050207001] = {
    id = 1050207001,
    talk_text = function()
      return T_S(10502070010)
    end,
    next_dialog = 1050207002,
    speak_head = 90120006,
    speak_head_actions = {
      "talk",
```

---

## Base/BasePlotDialogPart25100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart25100 = {
  [1050301001] = {
    id = 1050301001,
    talk_text = function()
      return T_S(10503010010)
    end,
    role_ids = {90110001},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart25101.lua.lua
**Snippet:**
```lua
BasePlotDialogPart25101 = {
  [1050303001] = {
    id = 1050303001,
    talk_text = function()
      return T_S(10503030010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart25150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart25150 = {
  [1050401001] = {
    id = 1050401001,
    talk_text = function()
      return T_S(10504010010)
    end,
    role_ids = {90110004},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart25200.lua.lua
**Snippet:**
```lua
BasePlotDialogPart25200 = {
  [1050501001] = {
    id = 1050501001,
    talk_text = function()
      return T_S(10505010010)
    end,
    role_ids = {90110001},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart25201.lua.lua
**Snippet:**
```lua
BasePlotDialogPart25201 = {
  [1050503001] = {
    id = 1050503001,
    talk_text = function()
      return T_S(10505030010)
    end,
    next_dialog = 1050503002,
    speak_head = 90120023,
    speak_head_actions = {
      "talk",
```

---

## Base/BasePlotDialogPart25202.lua.lua
**Snippet:**
```lua
BasePlotDialogPart25202 = {
  [1050505001] = {
    id = 1050505001,
    talk_text = function()
      return T_S(10505050010)
    end,
    role_ids = {90110001},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart25250.lua.lua
**Snippet:**
```lua
BasePlotDialogPart25250 = {
  [1050601001] = {
    id = 1050601001,
    talk_text = function()
      return T_S(10506010010)
    end,
    next_dialog = 1050601002,
    camera_shake = {
      "3",
      "0",
```

---

## Base/BasePlotDialogPart25251.lua.lua
**Snippet:**
```lua
BasePlotDialogPart25251 = {
  [1050603001] = {
    id = 1050603001,
    talk_text = function()
      return T_S(10506030010)
    end,
    next_dialog = 1050603002,
    env_sound = 20004,
    special_sound = 23026
  },
```

---

## Base/BasePlotDialogPart25252.lua.lua
**Snippet:**
```lua
BasePlotDialogPart25252 = {
  [1050606001] = {
    id = 1050606001,
    talk_text = function()
      return T_S(10506060010)
    end,
    role_ids = {90110004},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart25253.lua.lua
**Snippet:**
```lua
BasePlotDialogPart25253 = {
  [1050607001] = {
    id = 1050607001,
    talk_text = function()
      return T_S(10506070010)
    end,
    role_ids = {90110004},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart300.lua.lua
**Snippet:**
```lua
BasePlotDialogPart300 = {
  [1000701001] = {
    id = 1000701001,
    talk_text = function()
      return T_S(10007010010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart30000.lua.lua
**Snippet:**
```lua
BasePlotDialogPart30000 = {
  [1060101001] = {
    id = 1060101001,
    talk_text = function()
      return T_S(10601010010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart30050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart30050 = {
  [1060201001] = {
    id = 1060201001,
    talk_text = function()
      return T_S(10602010010)
    end,
    next_dialog = 1060201002,
    env_sound = 20009,
    open_title_1 = function()
      return T_S(10602010018)
```

---

## Base/BasePlotDialogPart30051.lua.lua
**Snippet:**
```lua
BasePlotDialogPart30051 = {
  [1060203001] = {
    id = 1060203001,
    talk_text = function()
      return T_S(10602030010)
    end,
    role_ids = {90110007},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/DialogAction/1060203001/1060203001_90110007.playable"
```

---

## Base/BasePlotDialogPart30100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart30100 = {
  [1060301001] = {
    id = 1060301001,
    talk_text = function()
      return T_S(10603010010)
    end,
    next_dialog = 1060301024,
    env_sound = 20002,
    open_title_1 = function()
      return T_S(10603010018)
```

---

## Base/BasePlotDialogPart30101.lua.lua
**Snippet:**
```lua
BasePlotDialogPart30101 = {
  [1060303001] = {
    id = 1060303001,
    talk_text = function()
      return T_S(10603030010)
    end,
    role_ids = {90110009, 90110010},
    scale = {10000, 10000},
    action = {"", ""},
    action_timeline = {
```

---

## Base/BasePlotDialogPart30150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart30150 = {
  [1060401001] = {
    id = 1060401001,
    talk_text = function()
      return T_S(10604010010)
    end,
    role_ids = {90110009, 90110010},
    scale = {10000, 10000},
    action = {"", ""},
    action_timeline = {
```

---

## Base/BasePlotDialogPart30151.lua.lua
**Snippet:**
```lua
BasePlotDialogPart30151 = {
  [1060403001] = {
    id = 1060403001,
    talk_text = function()
      return T_S(10604030010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart30200.lua.lua
**Snippet:**
```lua
BasePlotDialogPart30200 = {
  [1060501001] = {
    id = 1060501001,
    talk_text = function()
      return T_S(10605010010)
    end,
    next_dialog = 1060501002,
    env_sound = 20002,
    open_title_1 = function()
      return T_S(10605010018)
```

---

## Base/BasePlotDialogPart30201.lua.lua
**Snippet:**
```lua
BasePlotDialogPart30201 = {
  [1060503001] = {
    id = 1060503001,
    middle_text = function()
      return T_S(10605030013)
    end,
    next_dialog = 1060503002
  },
  [1060503002] = {
    id = 1060503002,
```

---

## Base/BasePlotDialogPart30202.lua.lua
**Snippet:**
```lua
BasePlotDialogPart30202 = {
  [1060505001] = {
    id = 1060505001,
    talk_text = function()
      return T_S(10605050010)
    end,
    role_ids = {90110012},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/DialogAction/1060505001/1060505001_90110012.playable"
```

---

## Base/BasePlotDialogPart350.lua.lua
**Snippet:**
```lua
BasePlotDialogPart350 = {
  [1000801001] = {
    id = 1000801001,
    talk_text = function()
      return T_S(10008010010)
    end,
    next_dialog = 1000801002,
    speak_head = 90120052,
    env_sound = 20002
  },
```

---

## Base/BasePlotDialogPart35000.lua.lua
**Snippet:**
```lua
BasePlotDialogPart35000 = {
  [1070101001] = {
    id = 1070101001,
    talk_text = function()
      return T_S(10701010010)
    end,
    next_dialog = 1070101002,
    speak_head = 90120023,
    speak_head_actions = {
      "talk",
```

---

## Base/BasePlotDialogPart35001.lua.lua
**Snippet:**
```lua
BasePlotDialogPart35001 = {
  [1070103001] = {
    id = 1070103001,
    talk_text = function()
      return T_S(10701030010)
    end,
    role_ids = {90110011},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart35050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart35050 = {
  [1070201001] = {
    id = 1070201001,
    next_dialog = 1070201002,
    camera_shake = {
      "3",
      "0",
      "1800"
    },
    env_sound = 20004,
```

---

## Base/BasePlotDialogPart35100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart35100 = {
  [1070301001] = {
    id = 1070301001,
    talk_text = function()
      return T_S(10703010010)
    end,
    next_dialog = 1070301002,
    speak_name = function()
      return T_S(10703010015)
    end,
```

---

## Base/BasePlotDialogPart35101.lua.lua
**Snippet:**
```lua
BasePlotDialogPart35101 = {
  [1070303001] = {
    id = 1070303001,
    talk_text = function()
      return T_S(10703030010)
    end,
    next_dialog = 1070303002,
    speak_name = function()
      return T_S(10703030015)
    end,
```

---

## Base/BasePlotDialogPart35102.lua.lua
**Snippet:**
```lua
BasePlotDialogPart35102 = {
  [1070305001] = {
    id = 1070305001,
    talk_text = function()
      return T_S(10703050010)
    end,
    role_ids = {90110003},
    scale = {10000, 10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart35103.lua.lua
**Snippet:**
```lua
BasePlotDialogPart35103 = {
  [1070307001] = {
    id = 1070307001,
    talk_text = function()
      return T_S(10703070010)
    end,
    is_master = 1,
    role_ids = {90110004},
    scale = {10000},
    skin = {"common"},
```

---

## Base/BasePlotDialogPart35150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart35150 = {
  [1070401001] = {
    id = 1070401001,
    talk_text = function()
      return T_S(10704010010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart35151.lua.lua
**Snippet:**
```lua
BasePlotDialogPart35151 = {
  [1070403001] = {
    id = 1070403001,
    talk_text = function()
      return T_S(10704030010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart35152.lua.lua
**Snippet:**
```lua
BasePlotDialogPart35152 = {
  [1070405001] = {
    id = 1070405001,
    talk_text = function()
      return T_S(10704050010)
    end,
    is_master = 1,
    next_dialog = 1070405002,
    text_sound_path = "event:/voice_cn/story/M0000/M0000_story_00230",
    text_sound_bank = "bank:/voice_cn/sty/M0000_3",
```

---

## Base/BasePlotDialogPart40000.lua.lua
**Snippet:**
```lua
BasePlotDialogPart40000 = {
  [1080101001] = {
    id = 1080101001,
    talk_text = function()
      return T_S(10801010010)
    end,
    role_ids = {90110004},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart40001.lua.lua
**Snippet:**
```lua
BasePlotDialogPart40001 = {
  [1080103001] = {
    id = 1080103001,
    talk_text = function()
      return T_S(10801030010)
    end,
    next_dialog = 1080103002,
    speak_head = 90120014,
    speak_head_actions = {
      "idle",
```

---

## Base/BasePlotDialogPart40002.lua.lua
**Snippet:**
```lua
BasePlotDialogPart40002 = {
  [1080105001] = {
    id = 1080105001,
    talk_text = function()
      return T_S(10801050010)
    end,
    role_ids = {90110009},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/DialogAction/1080105001/1080105001_90110009.playable"
```

---

## Base/BasePlotDialogPart40003.lua.lua
**Snippet:**
```lua
BasePlotDialogPart40003 = {
  [1080107001] = {
    id = 1080107001,
    talk_text = function()
      return T_S(10801070010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart40050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart40050 = {
  [1080201001] = {
    id = 1080201001,
    talk_text = function()
      return T_S(10802010010)
    end,
    role_ids = {90110001},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart40051.lua.lua
**Snippet:**
```lua
BasePlotDialogPart40051 = {
  [1080203001] = {
    id = 1080203001,
    talk_text = function()
      return T_S(10802030010)
    end,
    is_master = 1,
    next_dialog = 1080203002,
    text_sound_path = "event:/voice_cn/story/M0000/M0000_story_00248_01",
    text_sound_bank = "bank:/voice_cn/sty/M0000_3",
```

---

## Base/BasePlotDialogPart40052.lua.lua
**Snippet:**
```lua
BasePlotDialogPart40052 = {
  [1080205001] = {
    id = 1080205001,
    talk_text = function()
      return T_S(10802050010)
    end,
    is_master = 1,
    next_dialog = 1080205002,
    text_sound_path = "event:/voice_cn/story/M0000/M0000_story_00267",
    text_sound_bank = "bank:/voice_cn/sty/M0000_3",
```

---

## Base/BasePlotDialogPart40100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart40100 = {
  [1080301001] = {
    id = 1080301001,
    talk_text = function()
      return T_S(10803010010)
    end,
    role_ids = {90110001},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart40101.lua.lua
**Snippet:**
```lua
BasePlotDialogPart40101 = {
  [1080303001] = {
    id = 1080303001,
    talk_text = function()
      return T_S(10803030010)
    end,
    next_dialog = 1080303002,
    speak_head = 90120014,
    speak_head_actions = {
      "idle",
```

---

## Base/BasePlotDialogPart40102.lua.lua
**Snippet:**
```lua
BasePlotDialogPart40102 = {
  [1080305001] = {
    id = 1080305001,
    talk_text = function()
      return T_S(10803050010)
    end,
    role_ids = {90110001},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart40150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart40150 = {
  [1080401001] = {
    id = 1080401001,
    talk_text = function()
      return T_S(10804010010)
    end,
    next_dialog = 1080401002,
    env_sound = 20004,
    open_title_1 = function()
      return T_S(10804010018)
```

---

## Base/BasePlotDialogPart40151.lua.lua
**Snippet:**
```lua
BasePlotDialogPart40151 = {
  [1080403001] = {
    id = 1080403001,
    talk_text = function()
      return T_S(10804030010)
    end,
    next_dialog = 1080403002,
    speak_head = 90120033,
    speak_head_actions = {
      "talk",
```

---

## Base/BasePlotDialogPart40152.lua.lua
**Snippet:**
```lua
BasePlotDialogPart40152 = {
  [1080405001] = {
    id = 1080405001,
    talk_text = function()
      return T_S(10804050010)
    end,
    role_ids = {90110011},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart40153.lua.lua
**Snippet:**
```lua
BasePlotDialogPart40153 = {
  [1080407001] = {
    id = 1080407001,
    talk_text = function()
      return T_S(10804070010)
    end,
    next_dialog = 1080407002,
    speak_head = 90120013,
    speak_head_actions = {
      "idle",
```

---

## Base/BasePlotDialogPart40200.lua.lua
**Snippet:**
```lua
BasePlotDialogPart40200 = {
  [1080501001] = {
    id = 1080501001,
    talk_text = function()
      return T_S(10805010010)
    end,
    next_dialog = 1080501002,
    env_sound = 20007,
    open_title_1 = function()
      return T_S(10805010018)
```

---

## Base/BasePlotDialogPart40201.lua.lua
**Snippet:**
```lua
BasePlotDialogPart40201 = {
  [1080503001] = {
    id = 1080503001,
    talk_text = function()
      return T_S(10805030010)
    end,
    role_ids = {90110011},
    scale = {10000},
    skin = {"crazy"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart40202.lua.lua
**Snippet:**
```lua
BasePlotDialogPart40202 = {
  [1080505001] = {
    id = 1080505001,
    talk_text = function()
      return T_S(10805050010)
    end,
    role_ids = {90110002},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart45000.lua.lua
**Snippet:**
```lua
BasePlotDialogPart45000 = {
  [1090101001] = {
    id = 1090101001,
    talk_text = function()
      return T_S(10901010010)
    end,
    is_os = 1,
    role_ids = {90110004},
    scale = {10000},
    skin = {"common"},
```

---

## Base/BasePlotDialogPart45050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart45050 = {
  [1090201001] = {
    id = 1090201001,
    talk_text = function()
      return T_S(10902010010)
    end,
    next_dialog = 1090201002,
    speak_head = 90120023,
    speak_head_actions = {
      "talk",
```

---

## Base/BasePlotDialogPart45100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart45100 = {
  [1090301001] = {
    id = 1090301001,
    talk_text = function()
      return T_S(10903010010)
    end,
    next_dialog = 1090301002,
    speak_head = 90120036,
    speak_head_actions = {
      "idle",
```

---

## Base/BasePlotDialogPart45101.lua.lua
**Snippet:**
```lua
BasePlotDialogPart45101 = {
  [1090303001] = {
    id = 1090303001,
    talk_text = function()
      return T_S(10903030010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart45150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart45150 = {
  [1090401001] = {
    id = 1090401001,
    talk_text = function()
      return T_S(10904010010)
    end,
    is_os = 1,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
```

---

## Base/BasePlotDialogPart45151.lua.lua
**Snippet:**
```lua
BasePlotDialogPart45151 = {
  [1090403001] = {
    id = 1090403001,
    talk_text = function()
      return T_S(10904030010)
    end,
    next_dialog = 1090403002,
    speak_head = 90120036,
    speak_head_actions = {
      "idle",
```

---

## Base/BasePlotDialogPart45200.lua.lua
**Snippet:**
```lua
BasePlotDialogPart45200 = {
  [1090501001] = {
    id = 1090501001,
    talk_text = function()
      return T_S(10905010010)
    end,
    next_dialog = 1090501002,
    speak_head = 90120037,
    speak_head_actions = {
      "idle",
```

---

## Base/BasePlotDialogPart45250.lua.lua
**Snippet:**
```lua
BasePlotDialogPart45250 = {
  [1090601001] = {
    id = 1090601001,
    talk_text = function()
      return T_S(10906010010)
    end,
    next_dialog = 1090601002,
    env_sound = 20003,
    open_title_1 = function()
      return T_S(10906010018)
```

---

## Base/BasePlotDialogPart45300.lua.lua
**Snippet:**
```lua
BasePlotDialogPart45300 = {
  [1090701001] = {
    id = 1090701001,
    talk_text = function()
      return T_S(10907010010)
    end,
    next_dialog = 1090701002,
    speak_head = 90120024,
    speak_head_actions = {
      "idle",
```

---

## Base/BasePlotDialogPart45301.lua.lua
**Snippet:**
```lua
BasePlotDialogPart45301 = {
  [1090703001] = {
    id = 1090703001,
    talk_text = function()
      return T_S(10907030010)
    end,
    is_master = 1,
    is_os = 1,
    next_dialog = 1090703002,
    text_sound_path = "event:/voice_cn/story/M0000/M0000_story_00307",
```

---

## Base/BasePlotDialogPart45350.lua.lua
**Snippet:**
```lua
BasePlotDialogPart45350 = {
  [1090801001] = {
    id = 1090801001,
    talk_text = function()
      return T_S(10908010010)
    end,
    next_dialog = 1090801002,
    env_sound = 20003,
    open_title_1 = function()
      return T_S(10908010018)
```

---

## Base/BasePlotDialogPart45351.lua.lua
**Snippet:**
```lua
BasePlotDialogPart45351 = {
  [1090803001] = {
    id = 1090803001,
    talk_text = function()
      return T_S(10908030010)
    end,
    next_dialog = 1090803002,
    camera_shake = {
      "3",
      "0",
```

---

## Base/BasePlotDialogPart45400.lua.lua
**Snippet:**
```lua
BasePlotDialogPart45400 = {
  [1090901001] = {
    id = 1090901001,
    talk_text = function()
      return T_S(10909010010)
    end,
    role_ids = {90110003, 90110015},
    scale = {10000, 10000},
    skin = {"common"},
    action = {"", ""},
```

---

## Base/BasePlotDialogPart45401.lua.lua
**Snippet:**
```lua
BasePlotDialogPart45401 = {
  [1090903001] = {
    id = 1090903001,
    talk_text = function()
      return T_S(10909030010)
    end,
    role_ids = {90110016, 90110015},
    scale = {10000, 10000},
    action = {"", ""},
    action_timeline = {
```

---

## Base/BasePlotDialogPart45402.lua.lua
**Snippet:**
```lua
BasePlotDialogPart45402 = {
  [1090905001] = {
    id = 1090905001,
    talk_text = function()
      return T_S(10909050010)
    end,
    role_ids = {90110013},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/DialogAction/1090905001/1090905001_90110013.playable"
```

---

## Base/BasePlotDialogPart50.lua.lua
**Snippet:**
```lua
BasePlotDialogPart50 = {
  [1000201001] = {
    id = 1000201001,
    talk_text = function()
      return T_S(10002010010)
    end,
    next_dialog = 1000201002,
    env_sound = 20008
  },
  [1000201002] = {
```

---

## Base/BasePlotDialogPart5000.lua.lua
**Snippet:**
```lua
BasePlotDialogPart5000 = {
  [1010101001] = {
    id = 1010101001,
    talk_text = function()
      return T_S(10101010010)
    end,
    scale = {10000},
    skin = {"broken"},
    blink_timeline = {
      "Assets/Art/PlotPlay/Timeline/BlinkTemplate/90110001/90110001_0.playable"
```

---

## Base/BasePlotDialogPart50000.lua.lua
**Snippet:**
```lua
BasePlotDialogPart50000 = {
  [1100101001] = {
    id = 1100101001,
    talk_text = function()
      return T_S(11001010010)
    end,
    next_dialog = 1100101002,
    env_sound = 20008
  },
  [1100101002] = {
```

---

## Base/BasePlotDialogPart50001.lua.lua
**Snippet:**
```lua
BasePlotDialogPart50001 = {
  [1100103001] = {
    id = 1100103001,
    talk_text = function()
      return T_S(11001030010)
    end,
    next_dialog = 1100103002,
    env_sound = 20008
  },
  [1100103002] = {
```

---

## Base/BasePlotDialogPart50002.lua.lua
**Snippet:**
```lua
BasePlotDialogPart50002 = {
  [1100105001] = {
    id = 1100105001,
    talk_text = function()
      return T_S(11001050010)
    end,
    scale = {10000},
    next_dialog = 1100105002,
    speak_head = 90120043,
    speak_head_actions = {
```

---

## Base/BasePlotDialogPart5001.lua.lua
**Snippet:**
```lua
BasePlotDialogPart5001 = {
  [1010103001] = {
    id = 1010103001,
    talk_text = function()
      return T_S(10101030010)
    end,
    next_dialog = 1010103002,
    env_sound = 20008
  },
  [1010103002] = {
```

---

## Base/BasePlotDialogPart50050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart50050 = {
  [1100201001] = {
    id = 1100201001,
    talk_text = function()
      return T_S(11002010010)
    end,
    next_dialog = 1100201002,
    env_sound = 20005,
    open_title_1 = function()
      return T_S(11002010018)
```

---

## Base/BasePlotDialogPart50051.lua.lua
**Snippet:**
```lua
BasePlotDialogPart50051 = {
  [1100203001] = {
    id = 1100203001,
    talk_text = function()
      return T_S(11002030010)
    end,
    scale = {10000},
    next_dialog = 1100203002,
    env_sound = 20003
  },
```

---

## Base/BasePlotDialogPart50100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart50100 = {
  [1100301001] = {
    id = 1100301001,
    talk_text = function()
      return T_S(11003010010)
    end,
    next_dialog = 1100301002,
    env_sound = 20007,
    open_title_1 = function()
      return T_S(11003010018)
```

---

## Base/BasePlotDialogPart50101.lua.lua
**Snippet:**
```lua
BasePlotDialogPart50101 = {
  [1100303001] = {
    id = 1100303001,
    talk_text = function()
      return T_S(11003030010)
    end,
    next_dialog = 1100303002,
    env_sound = 20004
  },
  [1100303002] = {
```

---

## Base/BasePlotDialogPart50102.lua.lua
**Snippet:**
```lua
BasePlotDialogPart50102 = {
  [1100305001] = {
    id = 1100305001,
    talk_text = function()
      return T_S(11003050010)
    end,
    next_dialog = 1100305002,
    env_sound = 20005
  },
  [1100305002] = {
```

---

## Base/BasePlotDialogPart50150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart50150 = {
  [1100401001] = {
    id = 1100401001,
    talk_text = function()
      return T_S(11004010010)
    end,
    role_ids = {90110001},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart50151.lua.lua
**Snippet:**
```lua
BasePlotDialogPart50151 = {
  [1100403001] = {
    id = 1100403001,
    talk_text = function()
      return T_S(11004030010)
    end,
    next_dialog = 1100403002,
    env_sound = 20008
  },
  [1100403002] = {
```

---

## Base/BasePlotDialogPart50200.lua.lua
**Snippet:**
```lua
BasePlotDialogPart50200 = {
  [1100501001] = {
    id = 1100501001,
    talk_text = function()
      return T_S(11005010010)
    end,
    role_ids = {90110004},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart50201.lua.lua
**Snippet:**
```lua
BasePlotDialogPart50201 = {
  [1100503001] = {
    id = 1100503001,
    talk_text = function()
      return T_S(11005030010)
    end,
    next_dialog = 1100503002,
    camera_shake = {
      "3",
      "0",
```

---

## Base/BasePlotDialogPart50202.lua.lua
**Snippet:**
```lua
BasePlotDialogPart50202 = {
  [1100505001] = {
    id = 1100505001,
    talk_text = function()
      return T_S(11005050010)
    end,
    is_master = 1,
    next_dialog = 1100505002,
    text_sound_path = "event:/voice_cn/story/M0000/M0000_story_00353",
    text_sound_bank = "bank:/voice_cn/sty/M0000_4",
```

---

## Base/BasePlotDialogPart50250.lua.lua
**Snippet:**
```lua
BasePlotDialogPart50250 = {
  [1100601001] = {
    id = 1100601001,
    talk_text = function()
      return T_S(11006010010)
    end,
    is_master = 0,
    next_dialog = 1100601009,
    speak_name = function()
      return T_S(11006010015)
```

---

## Base/BasePlotDialogPart50251.lua.lua
**Snippet:**
```lua
BasePlotDialogPart50251 = {
  [1100603001] = {
    id = 1100603001,
    talk_text = function()
      return T_S(11006030010)
    end,
    role_ids = {90110004},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart50252.lua.lua
**Snippet:**
```lua
BasePlotDialogPart50252 = {
  [1100605001] = {
    id = 1100605001,
    middle_text = function()
      return T_S(11006050013)
    end,
    env_sound = 20002
  },
  [1100606001] = {
    id = 1100606001,
```

---

## Base/BasePlotDialogPart504950.lua.lua
**Snippet:**
```lua
BasePlotDialogPart504950 = {
  [2010001001] = {
    id = 2010001001,
    talk_text = function()
      return T_S(20100010010)
    end,
    next_dialog = 2010001003,
    env_sound = 20002
  },
  [2010001003] = {
```

---

## Base/BasePlotDialogPart5050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart5050 = {
  [1010201001] = {
    id = 1010201001,
    talk_text = function()
      return T_S(10102010010)
    end,
    next_dialog = 1010201002,
    env_sound = 20005
  },
  [1010201002] = {
```

---

## Base/BasePlotDialogPart505000.lua.lua
**Snippet:**
```lua
BasePlotDialogPart505000 = {
  [2010101001] = {
    id = 2010101001,
    talk_text = function()
      return T_S(20101010010)
    end,
    is_master = 1,
    next_dialog = 2010101002,
    env_sound = 20005,
    open_title_1 = function()
```

---

## Base/BasePlotDialogPart505001.lua.lua
**Snippet:**
```lua
BasePlotDialogPart505001 = {
  [2010103001] = {
    id = 2010103001,
    talk_text = function()
      return T_S(20101030010)
    end,
    is_master = 0,
    next_dialog = 2010103002,
    env_sound = 20005
  },
```

---

## Base/BasePlotDialogPart505002.lua.lua
**Snippet:**
```lua
BasePlotDialogPart505002 = {
  [2010105001] = {
    id = 2010105001,
    talk_text = function()
      return T_S(20101050010)
    end,
    next_dialog = 2010105002,
    env_sound = 20003
  },
  [2010105002] = {
```

---

## Base/BasePlotDialogPart505050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart505050 = {
  [2010201001] = {
    id = 2010201001,
    talk_text = function()
      return T_S(20102010010)
    end,
    next_dialog = 2010201002,
    speak_name = function()
      return T_S(20102010015)
    end,
```

---

## Base/BasePlotDialogPart5051.lua.lua
**Snippet:**
```lua
BasePlotDialogPart5051 = {
  [1010203001] = {
    id = 1010203001,
    talk_text = function()
      return T_S(10102030010)
    end,
    role_ids = {90110004},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart505100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart505100 = {
  [2010301001] = {
    id = 2010301001,
    talk_text = function()
      return T_S(20103010010)
    end,
    role_ids = {90110019},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/DialogAction/2010301001/2010301001_90110019.playable"
```

---

## Base/BasePlotDialogPart505150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart505150 = {
  [2010401001] = {
    id = 2010401001,
    talk_text = function()
      return T_S(20104010010)
    end,
    role_ids = {90110020},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/DialogAction/2010401001/2010401001_90110020.playable"
```

---

## Base/BasePlotDialogPart5052.lua.lua
**Snippet:**
```lua
BasePlotDialogPart5052 = {
  [1010205001] = {
    id = 1010205001,
    talk_text = function()
      return T_S(10102050010)
    end,
    scale = {10000},
    skin = {"common"},
    blink_timeline = {
      "Assets/Art/PlotPlay/Timeline/BlinkTemplate/90110001/90110001_0.playable"
```

---

## Base/BasePlotDialogPart505200.lua.lua
**Snippet:**
```lua
BasePlotDialogPart505200 = {
  [2010501001] = {
    id = 2010501001,
    talk_text = function()
      return T_S(20105010010)
    end,
    role_ids = {90110020},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/DialogAction/2010501001/2010501001_90110020.playable"
```

---

## Base/BasePlotDialogPart505250.lua.lua
**Snippet:**
```lua
BasePlotDialogPart505250 = {
  [2010601001] = {
    id = 2010601001,
    talk_text = function()
      return T_S(20106010010)
    end,
    role_ids = {90110020},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110020/90110020_0.playable"
```

---

## Base/BasePlotDialogPart505251.lua.lua
**Snippet:**
```lua
BasePlotDialogPart505251 = {
  [2010603001] = {
    id = 2010603001,
    talk_text = function()
      return T_S(20106030010)
    end,
    role_ids = {90110019, 90110020},
    scale = {10000, 10000},
    action = {"", ""},
    action_timeline = {
```

---

## Base/BasePlotDialogPart505300.lua.lua
**Snippet:**
```lua
BasePlotDialogPart505300 = {
  [2010701001] = {
    id = 2010701001,
    talk_text = function()
      return T_S(20107010010)
    end,
    role_ids = {90110020},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110020/90110020_0.playable"
```

---

## Base/BasePlotDialogPart505301.lua.lua
**Snippet:**
```lua
BasePlotDialogPart505301 = {
  [2010703001] = {
    id = 2010703001,
    talk_text = function()
      return T_S(20107030010)
    end,
    role_ids = {90110020},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110020/90110020_0.playable"
```

---

## Base/BasePlotDialogPart505350.lua.lua
**Snippet:**
```lua
BasePlotDialogPart505350 = {
  [2010801001] = {
    id = 2010801001,
    talk_text = function()
      return T_S(20108010010)
    end,
    is_master = 1,
    next_dialog = 2010801002,
    env_sound = 20002,
    open_title_1 = function()
```

---

## Base/BasePlotDialogPart505400.lua.lua
**Snippet:**
```lua
BasePlotDialogPart505400 = {
  [2010901001] = {
    id = 2010901001,
    talk_text = function()
      return T_S(20109010010)
    end,
    next_dialog = 2010901002,
    env_sound = 20004
  },
  [2010901002] = {
```

---

## Base/BasePlotDialogPart505450.lua.lua
**Snippet:**
```lua
BasePlotDialogPart505450 = {
  [2011001001] = {
    id = 2011001001,
    talk_text = function()
      return T_S(20110010010)
    end,
    next_dialog = 2011001002,
    env_sound = 20004,
    open_title_1 = function()
      return T_S(20110010018)
```

---

## Base/BasePlotDialogPart505500.lua.lua
**Snippet:**
```lua
BasePlotDialogPart505500 = {
  [2011101001] = {
    id = 2011101001,
    talk_text = function()
      return T_S(20111010010)
    end,
    next_dialog = 2011101002,
    env_sound = 20004
  },
  [2011101002] = {
```

---

## Base/BasePlotDialogPart505501.lua.lua
**Snippet:**
```lua
BasePlotDialogPart505501 = {
  [2011103001] = {
    id = 2011103001,
    cg_text = function()
      return T_S(20111030017)
    end,
    cg_position_scale = "-213:-171:8400",
    next_dialog = 2011103002,
    speak_name = function()
      return T_S(20111030015)
```

---

## Base/BasePlotDialogPart505502.lua.lua
**Snippet:**
```lua
BasePlotDialogPart505502 = {
  [2011105001] = {
    id = 2011105001,
    talk_text = function()
      return T_S(20111050010)
    end,
    next_dialog = 2011105002,
    camera_shake = {
      "1",
      "0",
```

---

## Base/BasePlotDialogPart505550.lua.lua
**Snippet:**
```lua
BasePlotDialogPart505550 = {
  [2011201001] = {
    id = 2011201001,
    talk_text = function()
      return T_S(20112010010)
    end,
    is_master = 1,
    next_dialog = 2011201002,
    env_sound = 20009,
    open_title_1 = function()
```

---

## Base/BasePlotDialogPart505600.lua.lua
**Snippet:**
```lua
BasePlotDialogPart505600 = {
  [2011301001] = {
    id = 2011301001,
    talk_text = function()
      return T_S(20113010010)
    end,
    role_ids = {90110020},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110020/90110020_0.playable"
```

---

## Base/BasePlotDialogPart505650.lua.lua
**Snippet:**
```lua
BasePlotDialogPart505650 = {
  [2011401001] = {
    id = 2011401001,
    talk_text = function()
      return T_S(20114010010)
    end,
    next_dialog = 2011401002,
    speak_name = function()
      return T_S(20114010015)
    end,
```

---

## Base/BasePlotDialogPart505651.lua.lua
**Snippet:**
```lua
BasePlotDialogPart505651 = {
  [2011403001] = {
    id = 2011403001,
    talk_text = function()
      return T_S(20114030010)
    end,
    next_dialog = 2011403002,
    env_sound = 20002
  },
  [2011403002] = {
```

---

## Base/BasePlotDialogPart5100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart5100 = {
  [1010301001] = {
    id = 1010301001,
    talk_text = function()
      return T_S(10103010010)
    end,
    role_ids = {90110015},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/DialogAction/1010301001/1010301001_90110015.playable"
```

---

## Base/BasePlotDialogPart510000.lua.lua
**Snippet:**
```lua
BasePlotDialogPart510000 = {
  [2020101001] = {
    id = 2020101001,
    talk_text = function()
      return T_S(20201010010)
    end,
    scale = {10000},
    next_dialog = 2020101002,
    speak_head = 90120022,
    speak_head_actions = {"talk", "idle"},
```

---

## Base/BasePlotDialogPart510001.lua.lua
**Snippet:**
```lua
BasePlotDialogPart510001 = {
  [2020103001] = {
    id = 2020103001,
    talk_text = function()
      return T_S(20201030010)
    end,
    role_ids = {90110001},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart510050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart510050 = {
  [2020201001] = {
    id = 2020201001,
    talk_text = function()
      return T_S(20202010010)
    end,
    next_dialog = 2020201002,
    env_sound = 20001,
    open_title_1 = function()
      return T_S(20202010018)
```

---

## Base/BasePlotDialogPart510051.lua.lua
**Snippet:**
```lua
BasePlotDialogPart510051 = {
  [2020203001] = {
    id = 2020203001,
    talk_text = function()
      return T_S(20202030010)
    end,
    role_ids = {90110002},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart5101.lua.lua
**Snippet:**
```lua
BasePlotDialogPart5101 = {
  [1010303001] = {
    id = 1010303001,
    talk_text = function()
      return T_S(10103030010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart510100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart510100 = {
  [2020301001] = {
    id = 2020301001,
    talk_text = function()
      return T_S(20203010010)
    end,
    next_dialog = 2020301002,
    speak_head = 90120058,
    speak_head_actions = {"talk", "idle"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart510101.lua.lua
**Snippet:**
```lua
BasePlotDialogPart510101 = {
  [2020303001] = {
    id = 2020303001,
    talk_text = function()
      return T_S(20203030010)
    end,
    is_master = 1,
    next_dialog = 2020303002,
    env_sound = 20003
  },
```

---

## Base/BasePlotDialogPart510102.lua.lua
**Snippet:**
```lua
BasePlotDialogPart510102 = {
  [2020305001] = {
    id = 2020305001,
    talk_text = function()
      return T_S(20203050010)
    end,
    role_ids = {90110002},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart510150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart510150 = {
  [2020401001] = {
    id = 2020401001,
    talk_text = function()
      return T_S(20204010010)
    end,
    next_dialog = 2020401002,
    speak_head = 90120058,
    speak_head_actions = {"idle", "talk"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart510151.lua.lua
**Snippet:**
```lua
BasePlotDialogPart510151 = {
  [2020403001] = {
    id = 2020403001,
    talk_text = function()
      return T_S(20204030010)
    end,
    next_dialog = 2020403002,
    env_sound = 20001
  },
  [2020403002] = {
```

---

## Base/BasePlotDialogPart5102.lua.lua
**Snippet:**
```lua
BasePlotDialogPart5102 = {
  [1010305001] = {
    id = 1010305001,
    talk_text = function()
      return T_S(10103050010)
    end,
    role_ids = {90110015},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/DialogAction/1010305001/1010305001_90110015.playable"
```

---

## Base/BasePlotDialogPart510200.lua.lua
**Snippet:**
```lua
BasePlotDialogPart510200 = {
  [2020501001] = {
    id = 2020501001,
    talk_text = function()
      return T_S(20205010010)
    end,
    next_dialog = 2020501002,
    env_sound = 20008,
    open_title_1 = function()
      return T_S(20205010018)
```

---

## Base/BasePlotDialogPart510201.lua.lua
**Snippet:**
```lua
BasePlotDialogPart510201 = {
  [2020503001] = {
    id = 2020503001,
    talk_text = function()
      return T_S(20205030010)
    end,
    role_ids = {90110001},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart510202.lua.lua
**Snippet:**
```lua
BasePlotDialogPart510202 = {
  [2020505001] = {
    id = 2020505001,
    talk_text = function()
      return T_S(20205050010)
    end,
    is_master = 1,
    next_dialog = 2020505002,
    env_sound = 20002
  },
```

---

## Base/BasePlotDialogPart510250.lua.lua
**Snippet:**
```lua
BasePlotDialogPart510250 = {
  [2020601001] = {
    id = 2020601001,
    talk_text = function()
      return T_S(20206010010)
    end,
    role_ids = {90110024},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110024/90110024_0.playable"
```

---

## Base/BasePlotDialogPart510251.lua.lua
**Snippet:**
```lua
BasePlotDialogPart510251 = {
  [2020603001] = {
    id = 2020603001,
    talk_text = function()
      return T_S(20206030010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart510300.lua.lua
**Snippet:**
```lua
BasePlotDialogPart510300 = {
  [2020701001] = {
    id = 2020701001,
    talk_text = function()
      return T_S(20207010010)
    end,
    role_ids = {90110024},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110024/90110024_0.playable"
```

---

## Base/BasePlotDialogPart510301.lua.lua
**Snippet:**
```lua
BasePlotDialogPart510301 = {
  [2020703001] = {
    id = 2020703001,
    talk_text = function()
      return T_S(20207030010)
    end,
    cg_position_scale = "-108:-191:10000",
    next_dialog = 2020703002,
    env_sound = 20006
  },
```

---

## Base/BasePlotDialogPart510302.lua.lua
**Snippet:**
```lua
BasePlotDialogPart510302 = {
  [2020705001] = {
    id = 2020705001,
    talk_text = function()
      return T_S(20207050010)
    end,
    next_dialog = 2020705002,
    speak_head = 90120058,
    speak_head_actions = {"idle", "talk"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart510350.lua.lua
**Snippet:**
```lua
BasePlotDialogPart510350 = {
  [2020801001] = {
    id = 2020801001,
    talk_text = function()
      return T_S(20208010010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart510400.lua.lua
**Snippet:**
```lua
BasePlotDialogPart510400 = {
  [2020901001] = {
    id = 2020901001,
    talk_text = function()
      return T_S(20209010010)
    end,
    next_dialog = 2020901002,
    env_sound = 20005,
    open_title_1 = function()
      return T_S(20209010018)
```

---

## Base/BasePlotDialogPart510401.lua.lua
**Snippet:**
```lua
BasePlotDialogPart510401 = {
  [2020903001] = {
    id = 2020903001,
    talk_text = function()
      return T_S(20209030010)
    end,
    next_dialog = 2020903002,
    speak_head = 90120056,
    speak_head_actions = {"talk", "idle"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart510450.lua.lua
**Snippet:**
```lua
BasePlotDialogPart510450 = {
  [2021001001] = {
    id = 2021001001,
    talk_text = function()
      return T_S(20210010010)
    end,
    role_ids = {90110023},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110023/90110023_0.playable"
```

---

## Base/BasePlotDialogPart510500.lua.lua
**Snippet:**
```lua
BasePlotDialogPart510500 = {
  [2021101001] = {
    id = 2021101001,
    talk_text = function()
      return T_S(20211010010)
    end,
    next_dialog = 2021101002,
    speak_name = function()
      return T_S(20211010015)
    end,
```

---

## Base/BasePlotDialogPart510501.lua.lua
**Snippet:**
```lua
BasePlotDialogPart510501 = {
  [2021103001] = {
    id = 2021103001,
    talk_text = function()
      return T_S(20211030010)
    end,
    next_dialog = 2021103002,
    speak_head = 90120058,
    speak_head_actions = {"talk", "idle"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart5150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart5150 = {
  [1010401001] = {
    id = 1010401001,
    talk_text = function()
      return T_S(10104010010)
    end,
    role_ids = {90110001},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart515000.lua.lua
**Snippet:**
```lua
BasePlotDialogPart515000 = {
  [2030101001] = {
    id = 2030101001,
    talk_text = function()
      return T_S(20301010010)
    end,
    next_dialog = 2030101002,
    env_sound = 20009
  },
  [2030101002] = {
```

---

## Base/BasePlotDialogPart515050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart515050 = {
  [2030201001] = {
    id = 2030201001,
    talk_text = function()
      return T_S(20302010010)
    end,
    next_dialog = 2030201002,
    env_sound = 20001,
    open_title_1 = function()
      return T_S(20302010018)
```

---

## Base/BasePlotDialogPart515051.lua.lua
**Snippet:**
```lua
BasePlotDialogPart515051 = {
  [2030203001] = {
    id = 2030203001,
    talk_text = function()
      return T_S(20302030010)
    end,
    role_ids = {90110029},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110029/90110029_0.playable"
```

---

## Base/BasePlotDialogPart515100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart515100 = {
  [2030301001] = {
    id = 2030301001,
    talk_text = function()
      return T_S(20303010010)
    end,
    role_ids = {90110029},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110029/90110029_0.playable"
```

---

## Base/BasePlotDialogPart515150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart515150 = {
  [2030401001] = {
    id = 2030401001,
    talk_text = function()
      return T_S(20304010010)
    end,
    next_dialog = 2030401002,
    env_sound = 20002,
    open_title_1 = function()
      return T_S(20304010018)
```

---

## Base/BasePlotDialogPart515151.lua.lua
**Snippet:**
```lua
BasePlotDialogPart515151 = {
  [2030403001] = {
    id = 2030403001,
    talk_text = function()
      return T_S(20304030010)
    end,
    is_os = 1,
    role_ids = {90110028},
    scale = {10000},
    action_timeline = {
```

---

## Base/BasePlotDialogPart515200.lua.lua
**Snippet:**
```lua
BasePlotDialogPart515200 = {
  [2030501001] = {
    id = 2030501001,
    talk_text = function()
      return T_S(20305010010)
    end,
    next_dialog = 2030501002,
    camera_shake = {
      "2",
      "0",
```

---

## Base/BasePlotDialogPart515250.lua.lua
**Snippet:**
```lua
BasePlotDialogPart515250 = {
  [2030601001] = {
    id = 2030601001,
    talk_text = function()
      return T_S(20306010010)
    end,
    role_ids = {90110029},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110029/90110029_0.playable"
```

---

## Base/BasePlotDialogPart515300.lua.lua
**Snippet:**
```lua
BasePlotDialogPart515300 = {
  [2030701001] = {
    id = 2030701001,
    talk_text = function()
      return T_S(20307010010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart515301.lua.lua
**Snippet:**
```lua
BasePlotDialogPart515301 = {
  [2030703001] = {
    id = 2030703001,
    talk_text = function()
      return T_S(20307030010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart515350.lua.lua
**Snippet:**
```lua
BasePlotDialogPart515350 = {
  [2030801001] = {
    id = 2030801001,
    talk_text = function()
      return T_S(20308010010)
    end,
    next_dialog = 2030801002,
    env_sound = 20008,
    open_title_1 = function()
      return T_S(20308010018)
```

---

## Base/BasePlotDialogPart515400.lua.lua
**Snippet:**
```lua
BasePlotDialogPart515400 = {
  [2030901001] = {
    id = 2030901001,
    talk_text = function()
      return T_S(20309010010)
    end,
    scale = {10000},
    next_dialog = 2030901002,
    speak_name = function()
      return T_S(20309010015)
```

---

## Base/BasePlotDialogPart515401.lua.lua
**Snippet:**
```lua
BasePlotDialogPart515401 = {
  [2030903001] = {
    id = 2030903001,
    talk_text = function()
      return T_S(20309030010)
    end,
    role_ids = {90110029},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110029/90110029_0.playable"
```

---

## Base/BasePlotDialogPart515450.lua.lua
**Snippet:**
```lua
BasePlotDialogPart515450 = {
  [2031001001] = {
    id = 2031001001,
    talk_text = function()
      return T_S(20310010010)
    end,
    role_ids = {90110004},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart515451.lua.lua
**Snippet:**
```lua
BasePlotDialogPart515451 = {
  [2031003001] = {
    id = 2031003001,
    talk_text = function()
      return T_S(20310030010)
    end,
    next_dialog = 2031003002,
    env_sound = 20003
  },
  [2031003002] = {
```

---

## Base/BasePlotDialogPart515500.lua.lua
**Snippet:**
```lua
BasePlotDialogPart515500 = {
  [2031101001] = {
    id = 2031101001,
    talk_text = function()
      return T_S(20311010010)
    end,
    next_dialog = 2031101002,
    env_sound = 20007,
    open_title_1 = function()
      return T_S(20311010018)
```

---

## Base/BasePlotDialogPart515501.lua.lua
**Snippet:**
```lua
BasePlotDialogPart515501 = {
  [2031103001] = {
    id = 2031103001,
    cg_text = function()
      return T_S(20311030017)
    end,
    cg_position_scale = "-50:-88:8800",
    next_dialog = 2031103002,
    speak_name = function()
      return T_S(20311030015)
```

---

## Base/BasePlotDialogPart515550.lua.lua
**Snippet:**
```lua
BasePlotDialogPart515550 = {
  [2031201001] = {
    id = 2031201001,
    talk_text = function()
      return T_S(20312010010)
    end,
    next_dialog = 2031201002,
    env_sound = 20002,
    open_title_1 = function()
      return T_S(20312010018)
```

---

## Base/BasePlotDialogPart515551.lua.lua
**Snippet:**
```lua
BasePlotDialogPart515551 = {
  [2031203001] = {
    id = 2031203001,
    talk_text = function()
      return T_S(20312030010)
    end,
    role_ids = {90110029, 90110028},
    scale = {10000, 10000},
    action = {"", ""},
    action_timeline = {
```

---

## Base/BasePlotDialogPart5200.lua.lua
**Snippet:**
```lua
BasePlotDialogPart5200 = {
  [1010501001] = {
    id = 1010501001,
    talk_text = function()
      return T_S(10105010010)
    end,
    next_dialog = 1010501002,
    speak_head = 90120017,
    speak_head_actions = {
      "angry",
```

---

## Base/BasePlotDialogPart520000.lua.lua
**Snippet:**
```lua
BasePlotDialogPart520000 = {
  [2040101001] = {
    id = 2040101001,
    talk_text = function()
      return T_S(20401010010)
    end,
    role_ids = {90110001},
    scale = {10000, 10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart520001.lua.lua
**Snippet:**
```lua
BasePlotDialogPart520001 = {
  [2040103001] = {
    id = 2040103001,
    talk_text = function()
      return T_S(20401030010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart520050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart520050 = {
  [2040201001] = {
    id = 2040201001,
    talk_text = function()
      return T_S(20402010010)
    end,
    next_dialog = 2040201002,
    env_sound = 20002,
    open_title_1 = function()
      return T_S(20402010018)
```

---

## Base/BasePlotDialogPart520051.lua.lua
**Snippet:**
```lua
BasePlotDialogPart520051 = {
  [2040203001] = {
    id = 2040203001,
    talk_text = function()
      return T_S(20402030010)
    end,
    next_dialog = 2040203002,
    env_sound = 20002
  },
  [2040203002] = {
```

---

## Base/BasePlotDialogPart5201.lua.lua
**Snippet:**
```lua
BasePlotDialogPart5201 = {
  [1010503001] = {
    id = 1010503001,
    talk_text = function()
      return T_S(10105030010)
    end,
    role_ids = {90110004, 90110003},
    scale = {10000, 10000},
    skin = {"common", "common"},
    action = {"", ""},
```

---

## Base/BasePlotDialogPart520100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart520100 = {
  [2040301001] = {
    id = 2040301001,
    talk_text = function()
      return T_S(20403010010)
    end,
    next_dialog = 2040301002,
    env_sound = 20008,
    open_title_1 = function()
      return T_S(20403010018)
```

---

## Base/BasePlotDialogPart520101.lua.lua
**Snippet:**
```lua
BasePlotDialogPart520101 = {
  [2040303001] = {
    id = 2040303001,
    talk_text = function()
      return T_S(20403030010)
    end,
    next_dialog = 2040303002,
    speak_head = 90120041,
    speak_head_actions = {"idle", "talk"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart520150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart520150 = {
  [2040401001] = {
    id = 2040401001,
    talk_text = function()
      return T_S(20404010010)
    end,
    next_dialog = 2040401002,
    env_sound = 20009,
    open_title_1 = function()
      return T_S(20404010018)
```

---

## Base/BasePlotDialogPart5202.lua.lua
**Snippet:**
```lua
BasePlotDialogPart5202 = {
  [1010505001] = {
    id = 1010505001,
    talk_text = function()
      return T_S(10105050010)
    end,
    role_ids = {90110001, 90110002},
    scale = {10000, 10000},
    skin = {"common", "common"},
    action = {"", ""},
```

---

## Base/BasePlotDialogPart520200.lua.lua
**Snippet:**
```lua
BasePlotDialogPart520200 = {
  [2040501001] = {
    id = 2040501001,
    talk_text = function()
      return T_S(20405010010)
    end,
    next_dialog = 2040501002,
    env_sound = 20004,
    open_title_1 = function()
      return T_S(20405010018)
```

---

## Base/BasePlotDialogPart520250.lua.lua
**Snippet:**
```lua
BasePlotDialogPart520250 = {
  [2040601001] = {
    id = 2040601001,
    talk_text = function()
      return T_S(20406010010)
    end,
    next_dialog = 2040601002,
    env_sound = 20004,
    open_title_1 = function()
      return T_S(20406010018)
```

---

## Base/BasePlotDialogPart520300.lua.lua
**Snippet:**
```lua
BasePlotDialogPart520300 = {
  [2040701001] = {
    id = 2040701001,
    talk_text = function()
      return T_S(20407010010)
    end,
    next_dialog = 2040701002,
    env_sound = 20007,
    open_title_1 = function()
      return T_S(20407010018)
```

---

## Base/BasePlotDialogPart520350.lua.lua
**Snippet:**
```lua
BasePlotDialogPart520350 = {
  [2040801001] = {
    id = 2040801001,
    talk_text = function()
      return T_S(20408010010)
    end,
    next_dialog = 2040801002,
    env_sound = 20003,
    open_title_1 = function()
      return T_S(20408010018)
```

---

## Base/BasePlotDialogPart520351.lua.lua
**Snippet:**
```lua
BasePlotDialogPart520351 = {
  [2040803001] = {
    id = 2040803001,
    talk_text = function()
      return T_S(20408030010)
    end,
    next_dialog = 2040803002,
    speak_name = function()
      return T_S(20408030015)
    end,
```

---

## Base/BasePlotDialogPart520352.lua.lua
**Snippet:**
```lua
BasePlotDialogPart520352 = {
  [2040805001] = {
    id = 2040805001,
    talk_text = function()
      return T_S(20408050010)
    end,
    is_master = 1,
    next_dialog = 2040805002,
    env_sound = 20003
  },
```

---

## Base/BasePlotDialogPart520400.lua.lua
**Snippet:**
```lua
BasePlotDialogPart520400 = {
  [2040901001] = {
    id = 2040901001,
    talk_text = function()
      return T_S(20409010010)
    end,
    role_ids = {90110031},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110031/90110031_0.playable"
```

---

## Base/BasePlotDialogPart520401.lua.lua
**Snippet:**
```lua
BasePlotDialogPart520401 = {
  [2040903001] = {
    id = 2040903001,
    talk_text = function()
      return T_S(20409030010)
    end,
    next_dialog = 2040903002,
    env_sound = 20007
  },
  [2040903002] = {
```

---

## Base/BasePlotDialogPart520450.lua.lua
**Snippet:**
```lua
BasePlotDialogPart520450 = {
  [2041001001] = {
    id = 2041001001,
    talk_text = function()
      return T_S(20410010010)
    end,
    next_dialog = 2041001002,
    env_sound = 20004,
    open_title_1 = function()
      return T_S(20410010018)
```

---

## Base/BasePlotDialogPart520500.lua.lua
**Snippet:**
```lua
BasePlotDialogPart520500 = {
  [2041101001] = {
    id = 2041101001,
    talk_text = function()
      return T_S(20411010010)
    end,
    next_dialog = 2041101002,
    speak_head = 90120066,
    speak_head_actions = {"idle", "talk"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart520550.lua.lua
**Snippet:**
```lua
BasePlotDialogPart520550 = {
  [2041201001] = {
    id = 2041201001,
    talk_text = function()
      return T_S(20412010010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart5250.lua.lua
**Snippet:**
```lua
BasePlotDialogPart5250 = {
  [1010601001] = {
    id = 1010601001,
    talk_text = function()
      return T_S(10106010010)
    end,
    role_ids = {90110001},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart525000.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525000 = {
  [2050101001] = {
    id = 2050101001,
    talk_text = function()
      return T_S(20501010010)
    end,
    next_dialog = 2050101002,
    env_sound = 20003
  },
  [2050101002] = {
```

---

## Base/BasePlotDialogPart525001.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525001 = {
  [2050103001] = {
    id = 2050103001,
    talk_text = function()
      return T_S(20501030010)
    end,
    next_dialog = 2050103002,
    speak_head = 90120062,
    speak_head_actions = {"talk", "idle"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart525050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525050 = {
  [2050201001] = {
    id = 2050201001,
    talk_text = function()
      return T_S(20502010010)
    end,
    next_dialog = 2050201002,
    speak_head = 90120002,
    speak_head_actions = {"talk", "idle"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart525051.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525051 = {
  [2050203001] = {
    id = 2050203001,
    talk_text = function()
      return T_S(20502030010)
    end,
    next_dialog = 2050203002,
    env_sound = 20002
  },
  [2050203002] = {
```

---

## Base/BasePlotDialogPart5251.lua.lua
**Snippet:**
```lua
BasePlotDialogPart5251 = {
  [1010603001] = {
    id = 1010603001,
    talk_text = function()
      return T_S(10106030010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart525100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525100 = {
  [2050301001] = {
    id = 2050301001,
    talk_text = function()
      return T_S(20503010010)
    end,
    next_dialog = 2050301002,
    env_sound = 20002,
    open_title_1 = function()
      return T_S(20503010018)
```

---

## Base/BasePlotDialogPart525101.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525101 = {
  [2050303001] = {
    id = 2050303001,
    talk_text = function()
      return T_S(20503030010)
    end,
    next_dialog = 2050303002,
    env_sound = 20002
  },
  [2050303002] = {
```

---

## Base/BasePlotDialogPart525150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525150 = {
  [2050401001] = {
    id = 2050401001,
    talk_text = function()
      return T_S(20504010010)
    end,
    next_dialog = 2050401002,
    env_sound = 20009,
    open_title_1 = function()
      return T_S(20504010018)
```

---

## Base/BasePlotDialogPart525151.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525151 = {
  [2050403001] = {
    id = 2050403001,
    talk_text = function()
      return T_S(20504030010)
    end,
    next_dialog = 2050403002,
    speak_head = 90120077,
    speak_head_actions = {"idle", "talk"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart5252.lua.lua
**Snippet:**
```lua
BasePlotDialogPart5252 = {
  [1010605001] = {
    id = 1010605001,
    talk_text = function()
      return T_S(10106050010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart525200.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525200 = {
  [2050501001] = {
    id = 2050501001,
    talk_text = function()
      return T_S(20505010010)
    end,
    next_dialog = 2050501002,
    speak_head = 90120078,
    speak_head_actions = {"talk", "idle"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart525201.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525201 = {
  [2050503001] = {
    id = 2050503001,
    talk_text = function()
      return T_S(20505030010)
    end,
    next_dialog = 2050503002,
    env_sound = 20002
  },
  [2050503002] = {
```

---

## Base/BasePlotDialogPart525250.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525250 = {
  [2050601001] = {
    id = 2050601001,
    talk_text = function()
      return T_S(20506010010)
    end,
    next_dialog = 2050601002,
    env_sound = 20002,
    open_title_1 = function()
      return T_S(20506010018)
```

---

## Base/BasePlotDialogPart525251.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525251 = {
  [2050603001] = {
    id = 2050603001,
    talk_text = function()
      return T_S(20506030010)
    end,
    is_master = 1,
    next_dialog = 2050603002,
    env_sound = 20006
  },
```

---

## Base/BasePlotDialogPart5253.lua.lua
**Snippet:**
```lua
BasePlotDialogPart5253 = {
  [1010607001] = {
    id = 1010607001,
    talk_text = function()
      return T_S(10106070010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart525300.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525300 = {
  [2050701001] = {
    id = 2050701001,
    talk_text = function()
      return T_S(20507010010)
    end,
    next_dialog = 2050701002,
    env_sound = 20002,
    open_title_1 = function()
      return T_S(20507010018)
```

---

## Base/BasePlotDialogPart525301.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525301 = {
  [2050703001] = {
    id = 2050703001,
    talk_text = function()
      return T_S(20507030010)
    end,
    next_dialog = 2050703002,
    env_sound = 20002
  },
  [2050703002] = {
```

---

## Base/BasePlotDialogPart525350.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525350 = {
  [2050801001] = {
    id = 2050801001,
    talk_text = function()
      return T_S(20508010010)
    end,
    next_dialog = 2050801002,
    env_sound = 20002,
    open_title_1 = function()
      return T_S(20508010018)
```

---

## Base/BasePlotDialogPart525351.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525351 = {
  [2050803001] = {
    id = 2050803001,
    talk_text = function()
      return T_S(20508030010)
    end,
    next_dialog = 2050803002,
    env_sound = 20001
  },
  [2050803002] = {
```

---

## Base/BasePlotDialogPart5254.lua.lua
**Snippet:**
```lua
BasePlotDialogPart5254 = {
  [1010609001] = {
    id = 1010609001,
    talk_text = function()
      return T_S(10106090010)
    end,
    next_dialog = 1010609002,
    speak_head = 90120029,
    speak_head_actions = {
      "angry",
```

---

## Base/BasePlotDialogPart525400.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525400 = {
  [2050901001] = {
    id = 2050901001,
    talk_text = function()
      return T_S(20509010010)
    end,
    next_dialog = 2050901002,
    speak_head = 90120079,
    speak_head_actions = {"idle", "talk"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart525401.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525401 = {
  [2050903001] = {
    id = 2050903001,
    talk_text = function()
      return T_S(20509030010)
    end,
    next_dialog = 2050903002,
    env_sound = 20001
  },
  [2050903002] = {
```

---

## Base/BasePlotDialogPart525402.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525402 = {
  [2050905001] = {
    id = 2050905001,
    talk_text = function()
      return T_S(20509050010)
    end,
    next_dialog = 2050905002,
    speak_head = 90120079,
    speak_head_actions = {"idle", "talk"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart525450.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525450 = {
  [2051001001] = {
    id = 2051001001,
    talk_text = function()
      return T_S(20510010010)
    end,
    next_dialog = 2051001002,
    speak_head = 90120079,
    speak_head_actions = {"talk", "idle"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart525500.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525500 = {
  [2051101001] = {
    id = 2051101001,
    talk_text = function()
      return T_S(20511010010)
    end,
    next_dialog = 2051101002,
    env_sound = 20001,
    open_title_1 = function()
      return T_S(20511010018)
```

---

## Base/BasePlotDialogPart525501.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525501 = {
  [2051103001] = {
    id = 2051103001,
    talk_text = function()
      return T_S(20511030010)
    end,
    next_dialog = 2051103002,
    speak_head = 90120080,
    speak_head_actions = {"talk", "idle"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart525502.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525502 = {
  [2051105001] = {
    id = 2051105001,
    talk_text = function()
      return T_S(20511050010)
    end,
    next_dialog = 2051105002,
    speak_head = 90120079,
    speak_head_actions = {"idle", "talk"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart525550.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525550 = {
  [2051201001] = {
    id = 2051201001,
    talk_text = function()
      return T_S(20512010010)
    end,
    next_dialog = 2051201002,
    speak_head = 90120079,
    speak_head_actions = {"talk", "idle"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart525600.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525600 = {
  [2051301001] = {
    id = 2051301001,
    talk_text = function()
      return T_S(20513010010)
    end,
    next_dialog = 2051301002,
    env_sound = 20004,
    open_title_1 = function()
      return T_S(20513010018)
```

---

## Base/BasePlotDialogPart525601.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525601 = {
  [2051303001] = {
    id = 2051303001,
    talk_text = function()
      return T_S(20513030010)
    end,
    next_dialog = 2051303002,
    env_sound = 20008
  },
  [2051303002] = {
```

---

## Base/BasePlotDialogPart525650.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525650 = {
  [2051401001] = {
    id = 2051401001,
    talk_text = function()
      return T_S(20514010010)
    end,
    next_dialog = 2051401002,
    env_sound = 20003,
    open_title_1 = function()
      return T_S(20514010018)
```

---

## Base/BasePlotDialogPart525700.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525700 = {
  [2051501001] = {
    id = 2051501001,
    talk_text = function()
      return T_S(20515010010)
    end,
    next_dialog = 2051501002,
    env_sound = 20007,
    open_title_1 = function()
      return T_S(20515010018)
```

---

## Base/BasePlotDialogPart525750.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525750 = {
  [2051601001] = {
    id = 2051601001,
    talk_text = function()
      return T_S(20516010010)
    end,
    next_dialog = 2051601002,
    env_sound = 20002,
    open_title_1 = function()
      return T_S(20516010018)
```

---

## Base/BasePlotDialogPart525751.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525751 = {
  [2051603001] = {
    id = 2051603001,
    talk_text = function()
      return T_S(20516030010)
    end,
    role_ids = {90110005},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110005/90110005_0.playable"
```

---

## Base/BasePlotDialogPart525752.lua.lua
**Snippet:**
```lua
BasePlotDialogPart525752 = {
  [2051605001] = {
    id = 2051605001,
    talk_text = function()
      return T_S(20516050010)
    end,
    next_dialog = 2051605002,
    env_sound = 20009
  },
  [2051605002] = {
```

---

## Base/BasePlotDialogPart530000.lua.lua
**Snippet:**
```lua
BasePlotDialogPart530000 = {
  [2060101001] = {
    id = 2060101001,
    talk_text = function()
      return T_S(20601010010)
    end,
    scale = {10000},
    next_dialog = 2060101002,
    env_sound = 20001
  },
```

---

## Base/BasePlotDialogPart530001.lua.lua
**Snippet:**
```lua
BasePlotDialogPart530001 = {
  [2060103001] = {
    id = 2060103001,
    talk_text = function()
      return T_S(20601030010)
    end,
    role_ids = {90110032},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110032/90110032_0.playable"
```

---

## Base/BasePlotDialogPart530050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart530050 = {
  [2060201001] = {
    id = 2060201001,
    talk_text = function()
      return T_S(20602010010)
    end,
    next_dialog = 2060201002,
    env_sound = 20007,
    open_title_1 = function()
      return T_S(20602010018)
```

---

## Base/BasePlotDialogPart530100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart530100 = {
  [2060301001] = {
    id = 2060301001,
    talk_text = function()
      return T_S(20603010010)
    end,
    next_dialog = 2060301002,
    env_sound = 20005,
    open_title_1 = function()
      return T_S(20603010018)
```

---

## Base/BasePlotDialogPart530150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart530150 = {
  [2060401001] = {
    id = 2060401001,
    talk_text = function()
      return T_S(20604010010)
    end,
    next_dialog = 2060401002,
    env_sound = 20007,
    open_title_1 = function()
      return T_S(20604010018)
```

---

## Base/BasePlotDialogPart530200.lua.lua
**Snippet:**
```lua
BasePlotDialogPart530200 = {
  [2060501001] = {
    id = 2060501001,
    talk_text = function()
      return T_S(20605010010)
    end,
    role_ids = {90110032},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110032/90110032_0.playable"
```

---

## Base/BasePlotDialogPart530201.lua.lua
**Snippet:**
```lua
BasePlotDialogPart530201 = {
  [2060503001] = {
    id = 2060503001,
    talk_text = function()
      return T_S(20605030010)
    end,
    next_dialog = 2060503002,
    env_sound = 20003
  },
  [2060503002] = {
```

---

## Base/BasePlotDialogPart530250.lua.lua
**Snippet:**
```lua
BasePlotDialogPart530250 = {
  [2060601001] = {
    id = 2060601001,
    talk_text = function()
      return T_S(20606010010)
    end,
    role_ids = {90110032},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110032/90110032_0.playable"
```

---

## Base/BasePlotDialogPart530251.lua.lua
**Snippet:**
```lua
BasePlotDialogPart530251 = {
  [2060603001] = {
    id = 2060603001,
    talk_text = function()
      return T_S(20606030010)
    end,
    next_dialog = 2060603002,
    env_sound = 20003
  },
  [2060603002] = {
```

---

## Base/BasePlotDialogPart530300.lua.lua
**Snippet:**
```lua
BasePlotDialogPart530300 = {
  [2060701001] = {
    id = 2060701001,
    talk_text = function()
      return T_S(20607010010)
    end,
    next_dialog = 2060701002,
    env_sound = 20007,
    open_title_1 = function()
      return T_S(20607010018)
```

---

## Base/BasePlotDialogPart530350.lua.lua
**Snippet:**
```lua
BasePlotDialogPart530350 = {
  [2060801001] = {
    id = 2060801001,
    talk_text = function()
      return T_S(20608010010)
    end,
    is_master = 1,
    next_dialog = 2060801002,
    env_sound = 20008,
    open_title_1 = function()
```

---

## Base/BasePlotDialogPart530351.lua.lua
**Snippet:**
```lua
BasePlotDialogPart530351 = {
  [2060803001] = {
    id = 2060803001,
    talk_text = function()
      return T_S(20608030010)
    end,
    role_ids = {90110032},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110032/90110032_0.playable"
```

---

## Base/BasePlotDialogPart5350.lua.lua
**Snippet:**
```lua
BasePlotDialogPart5350 = {
  [1010801001] = {
    id = 1010801001,
    talk_text = function()
      return T_S(10108010010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart535000.lua.lua
**Snippet:**
```lua
BasePlotDialogPart535000 = {
  [2070101001] = {
    id = 2070101001,
    talk_text = function()
      return T_S(20701010010)
    end,
    role_ids = {90110023},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110023/90110023_0.playable"
```

---

## Base/BasePlotDialogPart535001.lua.lua
**Snippet:**
```lua
BasePlotDialogPart535001 = {
  [2070103001] = {
    id = 2070103001,
    talk_text = function()
      return T_S(20701030010)
    end,
    role_ids = {90110023},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110023/90110023_0.playable"
```

---

## Base/BasePlotDialogPart535050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart535050 = {
  [2070201001] = {
    id = 2070201001,
    talk_text = function()
      return T_S(20702010010)
    end,
    role_ids = {90110023},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110023/90110023_0.playable"
```

---

## Base/BasePlotDialogPart5351.lua.lua
**Snippet:**
```lua
BasePlotDialogPart5351 = {
  [1010803001] = {
    id = 1010803001,
    talk_text = function()
      return T_S(10108030010)
    end,
    next_dialog = 1010803002,
    speak_head = 90120003,
    speak_head_actions = {
      "talk",
```

---

## Base/BasePlotDialogPart535100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart535100 = {
  [2070301001] = {
    id = 2070301001,
    talk_text = function()
      return T_S(20703010010)
    end,
    role_ids = {90110023},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110023/90110023_0.playable"
```

---

## Base/BasePlotDialogPart535101.lua.lua
**Snippet:**
```lua
BasePlotDialogPart535101 = {
  [2070303001] = {
    id = 2070303001,
    middle_text = function()
      return T_S(20703030013)
    end,
    next_dialog = 2070303002,
    env_sound = 20005
  },
  [2070303002] = {
```

---

## Base/BasePlotDialogPart535150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart535150 = {
  [2070401001] = {
    id = 2070401001,
    talk_text = function()
      return T_S(20704010010)
    end,
    role_ids = {90110023},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110023/90110023_0.playable"
```

---

## Base/BasePlotDialogPart5352.lua.lua
**Snippet:**
```lua
BasePlotDialogPart5352 = {
  [1010805001] = {
    id = 1010805001,
    talk_text = function()
      return T_S(10108050010)
    end,
    role_ids = {90110004},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart535200.lua.lua
**Snippet:**
```lua
BasePlotDialogPart535200 = {
  [2070501001] = {
    id = 2070501001,
    middle_text = function()
      return T_S(20705010013)
    end,
    next_dialog = 2070501002,
    speak_name = function()
      return T_S(20705010015)
    end,
```

---

## Base/BasePlotDialogPart535201.lua.lua
**Snippet:**
```lua
BasePlotDialogPart535201 = {
  [2070503001] = {
    id = 2070503001,
    talk_text = function()
      return T_S(20705030010)
    end,
    next_dialog = 2070503002,
    env_sound = 20002
  },
  [2070503002] = {
```

---

## Base/BasePlotDialogPart535202.lua.lua
**Snippet:**
```lua
BasePlotDialogPart535202 = {
  [2070505001] = {
    id = 2070505001,
    talk_text = function()
      return T_S(20705050010)
    end,
    next_dialog = 2070505002,
    env_sound = 20002
  },
  [2070505002] = {
```

---

## Base/BasePlotDialogPart535250.lua.lua
**Snippet:**
```lua
BasePlotDialogPart535250 = {
  [2070601001] = {
    id = 2070601001,
    middle_text = function()
      return T_S(20706010013)
    end,
    next_dialog = 2070601002,
    env_sound = 20006,
    open_title_1 = function()
      return T_S(20706010018)
```

---

## Base/BasePlotDialogPart535251.lua.lua
**Snippet:**
```lua
BasePlotDialogPart535251 = {
  [2070603001] = {
    id = 2070603001,
    talk_text = function()
      return T_S(20706030010)
    end,
    next_dialog = 2070603002,
    env_sound = 20006
  },
  [2070603002] = {
```

---

## Base/BasePlotDialogPart535252.lua.lua
**Snippet:**
```lua
BasePlotDialogPart535252 = {
  [2070605001] = {
    id = 2070605001,
    talk_text = function()
      return T_S(20706050010)
    end,
    role_ids = {90110023, 90110033},
    scale = {10000, 10000},
    action = {"", ""},
    action_timeline = {
```

---

## Base/BasePlotDialogPart535300.lua.lua
**Snippet:**
```lua
BasePlotDialogPart535300 = {
  [2070701001] = {
    id = 2070701001,
    talk_text = function()
      return T_S(20707010010)
    end,
    role_ids = {90110033},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110033/90110033_0.playable"
```

---

## Base/BasePlotDialogPart535301.lua.lua
**Snippet:**
```lua
BasePlotDialogPart535301 = {
  [2070703001] = {
    id = 2070703001,
    talk_text = function()
      return T_S(20707030010)
    end,
    next_dialog = 2070703002,
    env_sound = 20004
  },
  [2070703002] = {
```

---

## Base/BasePlotDialogPart535350.lua.lua
**Snippet:**
```lua
BasePlotDialogPart535350 = {
  [2070801001] = {
    id = 2070801001,
    talk_text = function()
      return T_S(20708010010)
    end,
    role_ids = {90110033},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110033/90110033_0.playable"
```

---

## Base/BasePlotDialogPart540000.lua.lua
**Snippet:**
```lua
BasePlotDialogPart540000 = {
  [2080101001] = {
    id = 2080101001,
    talk_text = function()
      return T_S(20801010010)
    end,
    next_dialog = 2080101002,
    env_sound = 20001
  },
  [2080101002] = {
```

---

## Base/BasePlotDialogPart540001.lua.lua
**Snippet:**
```lua
BasePlotDialogPart540001 = {
  [2080103001] = {
    id = 2080103001,
    talk_text = function()
      return T_S(20801030010)
    end,
    next_dialog = 2080103002,
    speak_head = 90120082,
    speak_head_actions = {"talk", "idle"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart540050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart540050 = {
  [2080201001] = {
    id = 2080201001,
    talk_text = function()
      return T_S(20802010010)
    end,
    next_dialog = 2080201002,
    speak_head = 90120082,
    speak_head_actions = {"talk", "idle"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart540100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart540100 = {
  [2080301001] = {
    id = 2080301001,
    talk_text = function()
      return T_S(20803010010)
    end,
    next_dialog = 2080301002,
    speak_head = 90120082,
    speak_head_actions = {"talk", "idle"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart540150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart540150 = {
  [2080401001] = {
    id = 2080401001,
    talk_text = function()
      return T_S(20804010010)
    end,
    next_dialog = 2080401002,
    speak_head = 90120083,
    speak_head_actions = {"idle", "talk"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart540151.lua.lua
**Snippet:**
```lua
BasePlotDialogPart540151 = {
  [2080403001] = {
    id = 2080403001,
    talk_text = function()
      return T_S(20804030010)
    end,
    next_dialog = 2080403002,
    env_sound = 20008
  },
  [2080403002] = {
```

---

## Base/BasePlotDialogPart540200.lua.lua
**Snippet:**
```lua
BasePlotDialogPart540200 = {
  [2080501001] = {
    id = 2080501001,
    talk_text = function()
      return T_S(20805010010)
    end,
    next_dialog = 2080501002,
    env_sound = 20002,
    open_title_1 = function()
      return T_S(20805010018)
```

---

## Base/BasePlotDialogPart540201.lua.lua
**Snippet:**
```lua
BasePlotDialogPart540201 = {
  [2080503001] = {
    id = 2080503001,
    talk_text = function()
      return T_S(20805030010)
    end,
    role_ids = {90110034},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110034/90110034_0.playable"
```

---

## Base/BasePlotDialogPart540250.lua.lua
**Snippet:**
```lua
BasePlotDialogPart540250 = {
  [2080601001] = {
    id = 2080601001,
    talk_text = function()
      return T_S(20806010010)
    end,
    next_dialog = 2080601002,
    speak_head = 90120083,
    speak_head_actions = {"talk", "idle"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart540251.lua.lua
**Snippet:**
```lua
BasePlotDialogPart540251 = {
  [2080603001] = {
    id = 2080603001,
    talk_text = function()
      return T_S(20806030010)
    end,
    next_dialog = 2080603002,
    speak_head = 90120082,
    speak_head_actions = {"talk", "idle"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart540300.lua.lua
**Snippet:**
```lua
BasePlotDialogPart540300 = {
  [2080701001] = {
    id = 2080701001,
    talk_text = function()
      return T_S(20807010010)
    end,
    next_dialog = 2080701002,
    env_sound = 20007,
    open_title_1 = function()
      return T_S(20807010018)
```

---

## Base/BasePlotDialogPart540301.lua.lua
**Snippet:**
```lua
BasePlotDialogPart540301 = {
  [2080703001] = {
    id = 2080703001,
    talk_text = function()
      return T_S(20807030010)
    end,
    next_dialog = 2080703002,
    env_sound = 20007
  },
  [2080703002] = {
```

---

## Base/BasePlotDialogPart540350.lua.lua
**Snippet:**
```lua
BasePlotDialogPart540350 = {
  [2080801001] = {
    id = 2080801001,
    talk_text = function()
      return T_S(20808010010)
    end,
    next_dialog = 2080801002,
    speak_head = 90120083,
    speak_head_actions = {"idle", "talk"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart540351.lua.lua
**Snippet:**
```lua
BasePlotDialogPart540351 = {
  [2080803001] = {
    id = 2080803001,
    talk_text = function()
      return T_S(20808030010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart540352.lua.lua
**Snippet:**
```lua
BasePlotDialogPart540352 = {
  [2080805001] = {
    id = 2080805001,
    talk_text = function()
      return T_S(20808050010)
    end,
    next_dialog = 2080805002,
    env_sound = 20001
  },
  [2080805002] = {
```

---

## Base/BasePlotDialogPart545000.lua.lua
**Snippet:**
```lua
BasePlotDialogPart545000 = {
  [2090101001] = {
    id = 2090101001,
    talk_text = function()
      return T_S(20901010010)
    end,
    scale = {10000, 10000},
    next_dialog = 2090101002,
    speak_head = 90120025,
    speak_head_actions = {"talk", "idle"},
```

---

## Base/BasePlotDialogPart545001.lua.lua
**Snippet:**
```lua
BasePlotDialogPart545001 = {
  [2090103001] = {
    id = 2090103001,
    talk_text = function()
      return T_S(20901030010)
    end,
    role_ids = {90110009},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110009/90110009_0.playable"
```

---

## Base/BasePlotDialogPart545050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart545050 = {
  [2090201001] = {
    id = 2090201001,
    talk_text = function()
      return T_S(20902010010)
    end,
    next_dialog = 2090201002,
    env_sound = 20002,
    open_title_1 = function()
      return T_S(20902010018)
```

---

## Base/BasePlotDialogPart545051.lua.lua
**Snippet:**
```lua
BasePlotDialogPart545051 = {
  [2090203001] = {
    id = 2090203001,
    talk_text = function()
      return T_S(20902030010)
    end,
    next_dialog = 2090203002,
    env_sound = 20002
  },
  [2090203002] = {
```

---

## Base/BasePlotDialogPart545100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart545100 = {
  [2090301001] = {
    id = 2090301001,
    talk_text = function()
      return T_S(20903010010)
    end,
    role_ids = {90110009},
    scale = {10000, 10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110009/90110009_0.playable"
```

---

## Base/BasePlotDialogPart545150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart545150 = {
  [2090401001] = {
    id = 2090401001,
    talk_text = function()
      return T_S(20904010010)
    end,
    next_dialog = 2090401002,
    speak_head = 90120034,
    speak_head_actions = {"idle", "talk"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart545151.lua.lua
**Snippet:**
```lua
BasePlotDialogPart545151 = {
  [2090403001] = {
    id = 2090403001,
    talk_text = function()
      return T_S(20904030010)
    end,
    next_dialog = 2090403002,
    env_sound = 20008
  },
  [2090403002] = {
```

---

## Base/BasePlotDialogPart545200.lua.lua
**Snippet:**
```lua
BasePlotDialogPart545200 = {
  [2090501001] = {
    id = 2090501001,
    talk_text = function()
      return T_S(20905010010)
    end,
    is_master = 1,
    next_dialog = 2090501002,
    env_sound = 20001,
    open_title_1 = function()
```

---

## Base/BasePlotDialogPart545250.lua.lua
**Snippet:**
```lua
BasePlotDialogPart545250 = {
  [2090601001] = {
    id = 2090601001,
    talk_text = function()
      return T_S(20906010010)
    end,
    next_dialog = 2090601002,
    env_sound = 20002,
    open_title_1 = function()
      return T_S(20906010018)
```

---

## Base/BasePlotDialogPart545300.lua.lua
**Snippet:**
```lua
BasePlotDialogPart545300 = {
  [2090701001] = {
    id = 2090701001,
    talk_text = function()
      return T_S(20907010010)
    end,
    scale = {10000},
    next_dialog = 2090701002,
    speak_head = 90120086,
    speak_head_actions = {"idle", "talk"},
```

---

## Base/BasePlotDialogPart545301.lua.lua
**Snippet:**
```lua
BasePlotDialogPart545301 = {
  [2090703001] = {
    id = 2090703001,
    talk_text = function()
      return T_S(20907030010)
    end,
    next_dialog = 2090703002,
    env_sound = 20008
  },
  [2090703002] = {
```

---

## Base/BasePlotDialogPart545302.lua.lua
**Snippet:**
```lua
BasePlotDialogPart545302 = {
  [2090705001] = {
    id = 2090705001,
    talk_text = function()
      return T_S(20907050010)
    end,
    role_ids = {90110004},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart545303.lua.lua
**Snippet:**
```lua
BasePlotDialogPart545303 = {
  [2090707001] = {
    id = 2090707001,
    talk_text = function()
      return T_S(20907070010)
    end,
    role_ids = {90110009},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/DialogAction/2090707001/2090707001_90110009.playable"
```

---

## Base/BasePlotDialogPart545350.lua.lua
**Snippet:**
```lua
BasePlotDialogPart545350 = {
  [2090801001] = {
    id = 2090801001,
    talk_text = function()
      return T_S(20908010010)
    end,
    next_dialog = 2090801002,
    env_sound = 20006,
    open_title_1 = function()
      return T_S(20908010018)
```

---

## Base/BasePlotDialogPart545400.lua.lua
**Snippet:**
```lua
BasePlotDialogPart545400 = {
  [2090901001] = {
    id = 2090901001,
    talk_text = function()
      return T_S(20909010010)
    end,
    next_dialog = 2090901002,
    env_sound = 20002,
    open_title_1 = function()
      return T_S(20909010018)
```

---

## Base/BasePlotDialogPart545450.lua.lua
**Snippet:**
```lua
BasePlotDialogPart545450 = {
  [2091001001] = {
    id = 2091001001,
    talk_text = function()
      return T_S(20910010010)
    end,
    role_ids = {90110037},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/DialogAction/2091001001/2091001001_90110037.playable"
```

---

## Base/BasePlotDialogPart545500.lua.lua
**Snippet:**
```lua
BasePlotDialogPart545500 = {
  [2091101001] = {
    id = 2091101001,
    talk_text = function()
      return T_S(20911010010)
    end,
    role_ids = {90110039},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart545550.lua.lua
**Snippet:**
```lua
BasePlotDialogPart545550 = {
  [2091201001] = {
    id = 2091201001,
    talk_text = function()
      return T_S(20912010010)
    end,
    next_dialog = 2091201002,
    speak_head = 90120086,
    speak_head_actions = {"talk", "idle"},
    env_sound = 20002,
```

---

## Base/BasePlotDialogPart545600.lua.lua
**Snippet:**
```lua
BasePlotDialogPart545600 = {
  [2091301001] = {
    id = 2091301001,
    talk_text = function()
      return T_S(20913010010)
    end,
    next_dialog = 2091301002,
    speak_head = 90120086,
    speak_head_actions = {"talk", "idle"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart545650.lua.lua
**Snippet:**
```lua
BasePlotDialogPart545650 = {
  [2091401001] = {
    id = 2091401001,
    talk_text = function()
      return T_S(20914010010)
    end,
    next_dialog = 2091401002,
    env_sound = 20003,
    open_title_1 = function()
      return T_S(20914010018)
```

---

## Base/BasePlotDialogPart545700.lua.lua
**Snippet:**
```lua
BasePlotDialogPart545700 = {
  [2091501001] = {
    id = 2091501001,
    talk_text = function()
      return T_S(20915010010)
    end,
    next_dialog = 2091501002,
    env_sound = 20002,
    open_title_1 = function()
      return T_S(20915010018)
```

---

## Base/BasePlotDialogPart545750.lua.lua
**Snippet:**
```lua
BasePlotDialogPart545750 = {
  [2091601001] = {
    id = 2091601001,
    talk_text = function()
      return T_S(20916010010)
    end,
    next_dialog = 2091601002,
    env_sound = 20008,
    open_title_1 = function()
      return T_S(20916010018)
```

---

## Base/BasePlotDialogPart55000.lua.lua
**Snippet:**
```lua
BasePlotDialogPart55000 = {
  [1110101001] = {
    id = 1110101001,
    talk_text = function()
      return T_S(11101010010)
    end,
    next_dialog = 1110101002,
    camera_scale = {
      "2",
      "0",
```

---

## Base/BasePlotDialogPart550000.lua.lua
**Snippet:**
```lua
BasePlotDialogPart550000 = {
  [2100101001] = {
    id = 2100101001,
    talk_text = function()
      return T_S(21001010010)
    end,
    role_ids = {90110035},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110035/90110035_1.playable"
```

---

## Base/BasePlotDialogPart550001.lua.lua
**Snippet:**
```lua
BasePlotDialogPart550001 = {
  [2100103001] = {
    id = 2100103001,
    talk_text = function()
      return T_S(21001030010)
    end,
    next_dialog = 2100103002,
    env_sound = 20002
  },
  [2100103002] = {
```

---

## Base/BasePlotDialogPart55001.lua.lua
**Snippet:**
```lua
BasePlotDialogPart55001 = {
  [1110103001] = {
    id = 1110103001,
    talk_text = function()
      return T_S(11101030010)
    end,
    role_ids = {90110001},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart55002.lua.lua
**Snippet:**
```lua
BasePlotDialogPart55002 = {
  [1110105001] = {
    id = 1110105001,
    talk_text = function()
      return T_S(11101050010)
    end,
    role_ids = {90110005},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110005/90110005_0.playable"
```

---

## Base/BasePlotDialogPart550050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart550050 = {
  [2100201001] = {
    id = 2100201001,
    talk_text = function()
      return T_S(21002010010)
    end,
    role_ids = {90110005},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110005/90110005_0.playable"
```

---

## Base/BasePlotDialogPart550100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart550100 = {
  [2100301001] = {
    id = 2100301001,
    talk_text = function()
      return T_S(21003010010)
    end,
    next_dialog = 2100301002,
    env_sound = 20006,
    open_title_1 = function()
      return T_S(21003010018)
```

---

## Base/BasePlotDialogPart550150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart550150 = {
  [2100401001] = {
    id = 2100401001,
    talk_text = function()
      return T_S(21004010010)
    end,
    next_dialog = 2100401002,
    env_sound = 20001,
    open_title_1 = function()
      return T_S(21004010018)
```

---

## Base/BasePlotDialogPart550200.lua.lua
**Snippet:**
```lua
BasePlotDialogPart550200 = {
  [2100501001] = {
    id = 2100501001,
    talk_text = function()
      return T_S(21005010010)
    end,
    next_dialog = 2100501002,
    env_sound = 20001,
    open_title_1 = function()
      return T_S(21005010018)
```

---

## Base/BasePlotDialogPart550250.lua.lua
**Snippet:**
```lua
BasePlotDialogPart550250 = {
  [2100601001] = {
    id = 2100601001,
    talk_text = function()
      return T_S(21006010010)
    end,
    next_dialog = 2100601002,
    speak_head = 90120047,
    speak_head_actions = {"talk", "idle"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart550300.lua.lua
**Snippet:**
```lua
BasePlotDialogPart550300 = {
  [2100701001] = {
    id = 2100701001,
    talk_text = function()
      return T_S(21007010010)
    end,
    next_dialog = 2100701002,
    env_sound = 20003,
    open_title_1 = function()
      return T_S(21007010018)
```

---

## Base/BasePlotDialogPart550350.lua.lua
**Snippet:**
```lua
BasePlotDialogPart550350 = {
  [2100801001] = {
    id = 2100801001,
    talk_text = function()
      return T_S(21008010010)
    end,
    next_dialog = 2100801002,
    env_sound = 20006,
    open_title_1 = function()
      return T_S(21008010018)
```

---

## Base/BasePlotDialogPart550351.lua.lua
**Snippet:**
```lua
BasePlotDialogPart550351 = {
  [2100803001] = {
    id = 2100803001,
    talk_text = function()
      return T_S(21008030010)
    end,
    is_master = 0,
    next_dialog = 2100803002,
    speak_head = 90120080,
    speak_head_actions = {"idle", "talk"},
```

---

## Base/BasePlotDialogPart55050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart55050 = {
  [1110201001] = {
    id = 1110201001,
    talk_text = function()
      return T_S(11102010010)
    end,
    role_ids = {90110004},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart55051.lua.lua
**Snippet:**
```lua
BasePlotDialogPart55051 = {
  [1110203001] = {
    id = 1110203001,
    talk_text = function()
      return T_S(11102030010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart55100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart55100 = {
  [1110301001] = {
    id = 1110301001,
    talk_text = function()
      return T_S(11103010010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart55101.lua.lua
**Snippet:**
```lua
BasePlotDialogPart55101 = {
  [1110303001] = {
    id = 1110303001,
    talk_text = function()
      return T_S(11103030010)
    end,
    next_dialog = 1110303002,
    speak_head = 90120024,
    speak_head_actions = {"talk", "idle"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart55102.lua.lua
**Snippet:**
```lua
BasePlotDialogPart55102 = {
  [1110305001] = {
    id = 1110305001,
    talk_text = function()
      return T_S(11103050010)
    end,
    next_dialog = 1110305002,
    env_sound = 20002
  },
  [1110305002] = {
```

---

## Base/BasePlotDialogPart55150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart55150 = {
  [1110401001] = {
    id = 1110401001,
    talk_text = function()
      return T_S(11104010010)
    end,
    next_dialog = 1110401002,
    env_sound = 20001,
    open_title_1 = function()
      return T_S(11104010018)
```

---

## Base/BasePlotDialogPart55151.lua.lua
**Snippet:**
```lua
BasePlotDialogPart55151 = {
  [1110403001] = {
    id = 1110403001,
    talk_text = function()
      return T_S(11104030010)
    end,
    next_dialog = 1110403002,
    speak_head = 90120033,
    speak_head_actions = {"idle", "talk"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart55200.lua.lua
**Snippet:**
```lua
BasePlotDialogPart55200 = {
  [1110501001] = {
    id = 1110501001,
    talk_text = function()
      return T_S(11105010010)
    end,
    next_dialog = 1110501002,
    env_sound = 20006,
    open_title_1 = function()
      return T_S(11105010018)
```

---

## Base/BasePlotDialogPart55201.lua.lua
**Snippet:**
```lua
BasePlotDialogPart55201 = {
  [1110503001] = {
    id = 1110503001,
    talk_text = function()
      return T_S(11105030010)
    end,
    role_ids = {90110012},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110012/90110012_0.playable"
```

---

## Base/BasePlotDialogPart55250.lua.lua
**Snippet:**
```lua
BasePlotDialogPart55250 = {
  [1110601001] = {
    id = 1110601001,
    talk_text = function()
      return T_S(11106010010)
    end,
    next_dialog = 1110601002,
    env_sound = 20003,
    open_title_1 = function()
      return T_S(11106010018)
```

---

## Base/BasePlotDialogPart55300.lua.lua
**Snippet:**
```lua
BasePlotDialogPart55300 = {
  [1110701001] = {
    id = 1110701001,
    talk_text = function()
      return T_S(11107010010)
    end,
    next_dialog = 1110701002,
    camera_shake = {
      "3",
      "0",
```

---

## Base/BasePlotDialogPart55350.lua.lua
**Snippet:**
```lua
BasePlotDialogPart55350 = {
  [1110801001] = {
    id = 1110801001,
    talk_text = function()
      return T_S(11108010010)
    end,
    next_dialog = 1110801002,
    env_sound = 20001,
    open_title_1 = function()
      return T_S(11108010018)
```

---

## Base/BasePlotDialogPart55351.lua.lua
**Snippet:**
```lua
BasePlotDialogPart55351 = {
  [1110803001] = {
    id = 1110803001,
    talk_text = function()
      return T_S(11108030010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart555000.lua.lua
**Snippet:**
```lua
BasePlotDialogPart555000 = {
  [2110101001] = {
    id = 2110101001,
    talk_text = function()
      return T_S(21101010010)
    end,
    next_dialog = 2110101002,
    speak_name = function()
      return T_S(21101010015)
    end,
```

---

## Base/BasePlotDialogPart555001.lua.lua
**Snippet:**
```lua
BasePlotDialogPart555001 = {
  [2110103001] = {
    id = 2110103001,
    talk_text = function()
      return T_S(21101030010)
    end,
    role_ids = {90110041},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110041/90110041_1.playable"
```

---

## Base/BasePlotDialogPart555050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart555050 = {
  [2110201001] = {
    id = 2110201001,
    talk_text = function()
      return T_S(21102010010)
    end,
    next_dialog = 2110201002,
    env_sound = 20007,
    open_title_1 = function()
      return T_S(21102010018)
```

---

## Base/BasePlotDialogPart555100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart555100 = {
  [2110301001] = {
    id = 2110301001,
    talk_text = function()
      return T_S(21103010010)
    end,
    next_dialog = 2110301002,
    env_sound = 20007,
    open_title_1 = function()
      return T_S(21103010018)
```

---

## Base/BasePlotDialogPart555150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart555150 = {
  [2110401001] = {
    id = 2110401001,
    talk_text = function()
      return T_S(21104010010)
    end,
    role_ids = {90110040},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110040/90110040_0.playable"
```

---

## Base/BasePlotDialogPart555200.lua.lua
**Snippet:**
```lua
BasePlotDialogPart555200 = {
  [2110501001] = {
    id = 2110501001,
    talk_text = function()
      return T_S(21105010010)
    end,
    role_ids = {90110040},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110040/90110040_1.playable"
```

---

## Base/BasePlotDialogPart555201.lua.lua
**Snippet:**
```lua
BasePlotDialogPart555201 = {
  [2110503001] = {
    id = 2110503001,
    talk_text = function()
      return T_S(21105030010)
    end,
    role_ids = {90110041},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110041/90110041_0.playable"
```

---

## Base/BasePlotDialogPart555250.lua.lua
**Snippet:**
```lua
BasePlotDialogPart555250 = {
  [2110601001] = {
    id = 2110601001,
    talk_text = function()
      return T_S(21106010010)
    end,
    role_ids = {90110041},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110041/90110041_1.playable"
```

---

## Base/BasePlotDialogPart555300.lua.lua
**Snippet:**
```lua
BasePlotDialogPart555300 = {
  [2110701001] = {
    id = 2110701001,
    talk_text = function()
      return T_S(21107010010)
    end,
    next_dialog = 2110701002,
    camera_shake = {
      "2",
      "0",
```

---

## Base/BasePlotDialogPart555301.lua.lua
**Snippet:**
```lua
BasePlotDialogPart555301 = {
  [2110703001] = {
    id = 2110703001,
    talk_text = function()
      return T_S(21107030010)
    end,
    role_ids = {90110040},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110040/90110040_0.playable"
```

---

## Base/BasePlotDialogPart555302.lua.lua
**Snippet:**
```lua
BasePlotDialogPart555302 = {
  [2110705001] = {
    id = 2110705001,
    talk_text = function()
      return T_S(21107050010)
    end,
    next_dialog = 2110705002,
    env_sound = 20007
  },
  [2110705002] = {
```

---

## Base/BasePlotDialogPart555350.lua.lua
**Snippet:**
```lua
BasePlotDialogPart555350 = {
  [2110801001] = {
    id = 2110801001,
    talk_text = function()
      return T_S(21108010010)
    end,
    next_dialog = 2110801002,
    speak_head = 90120013,
    speak_head_actions = {"idle", "talk"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart5950.lua.lua
**Snippet:**
```lua
BasePlotDialogPart5950 = {
  [1012001001] = {
    id = 1012001001,
    animation_path = "Assets/Art/OpenCG/Prefab/InGameCg_001.prefab"
  }
}
```

---

## Base/BasePlotDialogPart60000.lua.lua
**Snippet:**
```lua
BasePlotDialogPart60000 = {
  [1120101001] = {
    id = 1120101001,
    talk_text = function()
      return T_S(11201010010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart60001.lua.lua
**Snippet:**
```lua
BasePlotDialogPart60001 = {
  [1120103001] = {
    id = 1120103001,
    talk_text = function()
      return T_S(11201030010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart60050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart60050 = {
  [1120201001] = {
    id = 1120201001,
    talk_text = function()
      return T_S(11202010010)
    end,
    next_dialog = 1120201002,
    env_sound = 20007
  },
  [1120201002] = {
```

---

## Base/BasePlotDialogPart60051.lua.lua
**Snippet:**
```lua
BasePlotDialogPart60051 = {
  [1120203001] = {
    id = 1120203001,
    talk_text = function()
      return T_S(11202030010)
    end,
    next_dialog = 1120203002,
    speak_head = 90120023,
    speak_head_actions = {"idle", "talk"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart60100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart60100 = {
  [1120301001] = {
    id = 1120301001,
    talk_text = function()
      return T_S(11203010010)
    end,
    role_ids = {90110004},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart60101.lua.lua
**Snippet:**
```lua
BasePlotDialogPart60101 = {
  [1120303001] = {
    id = 1120303001,
    talk_text = function()
      return T_S(11203030010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart60102.lua.lua
**Snippet:**
```lua
BasePlotDialogPart60102 = {
  [1120305001] = {
    id = 1120305001,
    talk_text = function()
      return T_S(11203050010)
    end,
    next_dialog = 1120305002,
    env_sound = 20004
  },
  [1120305002] = {
```

---

## Base/BasePlotDialogPart60150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart60150 = {
  [1120401001] = {
    id = 1120401001,
    talk_text = function()
      return T_S(11204010010)
    end,
    next_dialog = 1120401002,
    env_sound = 20006
  },
  [1120401002] = {
```

---

## Base/BasePlotDialogPart60151.lua.lua
**Snippet:**
```lua
BasePlotDialogPart60151 = {
  [1120403001] = {
    id = 1120403001,
    talk_text = function()
      return T_S(11204030010)
    end,
    role_ids = {90110005},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110005/90110005_0.playable"
```

---

## Base/BasePlotDialogPart60152.lua.lua
**Snippet:**
```lua
BasePlotDialogPart60152 = {
  [1120405001] = {
    id = 1120405001,
    talk_text = function()
      return T_S(11204050010)
    end,
    is_master = 1,
    next_dialog = 1120405002,
    text_sound_path = "event:/voice_cn/story/M0000/M0000_story_00567",
    text_sound_bank = "bank:/voice_cn/sty/M0000_6",
```

---

## Base/BasePlotDialogPart60200.lua.lua
**Snippet:**
```lua
BasePlotDialogPart60200 = {
  [1120501001] = {
    id = 1120501001,
    talk_text = function()
      return T_S(11205010010)
    end,
    role_ids = {90110009},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/ActionTemplate/90110009/90110009_0.playable"
```

---

## Base/BasePlotDialogPart60201.lua.lua
**Snippet:**
```lua
BasePlotDialogPart60201 = {
  [1120503001] = {
    id = 1120503001,
    talk_text = function()
      return T_S(11205030010)
    end,
    next_dialog = 1120503002,
    speak_head = 90120021,
    speak_head_actions = {"idle", "talk"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart60250.lua.lua
**Snippet:**
```lua
BasePlotDialogPart60250 = {
  [1120601001] = {
    id = 1120601001,
    talk_text = function()
      return T_S(11206010010)
    end,
    next_dialog = 1120601002,
    env_sound = 20001
  },
  [1120601002] = {
```

---

## Base/BasePlotDialogPart60251.lua.lua
**Snippet:**
```lua
BasePlotDialogPart60251 = {
  [1120603001] = {
    id = 1120603001,
    talk_text = function()
      return T_S(11206030010)
    end,
    next_dialog = 1120603002,
    speak_head = 90120048,
    speak_head_actions = {"idle", "talk"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart60300.lua.lua
**Snippet:**
```lua
BasePlotDialogPart60300 = {
  [1120701001] = {
    id = 1120701001,
    talk_text = function()
      return T_S(11207010010)
    end,
    next_dialog = 1120701002,
    env_sound = 20002,
    open_title_1 = function()
      return T_S(11207010018)
```

---

## Base/BasePlotDialogPart60301.lua.lua
**Snippet:**
```lua
BasePlotDialogPart60301 = {
  [1120703001] = {
    id = 1120703001,
    talk_text = function()
      return T_S(11207030010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart6050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart6050 = {
  [1012201001] = {
    id = 1012201001,
    battle_script = "PlotPlayBattle_2"
  }
}
```

---

## Base/BasePlotDialogPart65000.lua.lua
**Snippet:**
```lua
BasePlotDialogPart65000 = {
  [1130101001] = {
    id = 1130101001,
    talk_text = function()
      return T_S(11301010010)
    end,
    next_dialog = 1130101002,
    camera_shake = {
      "1",
      "0",
```

---

## Base/BasePlotDialogPart65001.lua.lua
**Snippet:**
```lua
BasePlotDialogPart65001 = {
  [1130103001] = {
    id = 1130103001,
    talk_text = function()
      return T_S(11301030010)
    end,
    role_ids = {90110005},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/DialogAction/1130103001/1130103001_90110005.playable"
```

---

## Base/BasePlotDialogPart65050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart65050 = {
  [1130201001] = {
    id = 1130201001,
    talk_text = function()
      return T_S(11302010010)
    end,
    next_dialog = 1130201002,
    env_sound = 20005,
    open_title_1 = function()
      return T_S(11302010018)
```

---

## Base/BasePlotDialogPart65051.lua.lua
**Snippet:**
```lua
BasePlotDialogPart65051 = {
  [1130203001] = {
    id = 1130203001,
    env_sound = 20007,
    force_auto = 1
  },
  [1130204001] = {
    id = 1130204001,
    talk_text = function()
      return T_S(11302040010)
```

---

## Base/BasePlotDialogPart65052.lua.lua
**Snippet:**
```lua
BasePlotDialogPart65052 = {
  [1130205001] = {
    id = 1130205001,
    talk_text = function()
      return T_S(11302050010)
    end,
    next_dialog = 1130205002,
    speak_name = function()
      return T_S(11302050015)
    end,
```

---

## Base/BasePlotDialogPart65100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart65100 = {
  [1130301001] = {
    id = 1130301001,
    talk_text = function()
      return T_S(11303010010)
    end,
    next_dialog = 1130301002,
    env_sound = 20004
  },
  [1130301002] = {
```

---

## Base/BasePlotDialogPart65150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart65150 = {
  [1130401001] = {
    id = 1130401001,
    talk_text = function()
      return T_S(11304010010)
    end,
    next_dialog = 1130401002,
    env_sound = 20007,
    open_title_1 = function()
      return T_S(11304010018)
```

---

## Base/BasePlotDialogPart65151.lua.lua
**Snippet:**
```lua
BasePlotDialogPart65151 = {
  [1130403001] = {
    id = 1130403001,
    talk_text = function()
      return T_S(11304030010)
    end,
    next_dialog = 1130403002,
    env_sound = 20005
  },
  [1130403002] = {
```

---

## Base/BasePlotDialogPart65200.lua.lua
**Snippet:**
```lua
BasePlotDialogPart65200 = {
  [1130501001] = {
    id = 1130501001,
    talk_text = function()
      return T_S(11305010010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart65201.lua.lua
**Snippet:**
```lua
BasePlotDialogPart65201 = {
  [1130503001] = {
    id = 1130503001,
    talk_text = function()
      return T_S(11305030010)
    end,
    next_dialog = 1130503002,
    speak_head = 90120024,
    speak_head_actions = {"talk", "idle"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart65250.lua.lua
**Snippet:**
```lua
BasePlotDialogPart65250 = {
  [1130601001] = {
    id = 1130601001,
    talk_text = function()
      return T_S(11306010010)
    end,
    next_dialog = 1130601002,
    env_sound = 20006,
    open_title_1 = function()
      return T_S(11306010018)
```

---

## Base/BasePlotDialogPart70000.lua.lua
**Snippet:**
```lua
BasePlotDialogPart70000 = {
  [1140101001] = {
    id = 1140101001,
    talk_text = function()
      return T_S(11401010010)
    end,
    next_dialog = 1140101002,
    env_sound = 20009
  },
  [1140101002] = {
```

---

## Base/BasePlotDialogPart70050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart70050 = {
  [1140201001] = {
    id = 1140201001,
    talk_text = function()
      return T_S(11402010010)
    end,
    next_dialog = 1140201002,
    env_sound = 20003
  },
  [1140201002] = {
```

---

## Base/BasePlotDialogPart70051.lua.lua
**Snippet:**
```lua
BasePlotDialogPart70051 = {
  [1140203001] = {
    id = 1140203001,
    talk_text = function()
      return T_S(11402030010)
    end,
    next_dialog = 1140203002,
    speak_head = 90120072,
    speak_head_actions = {"talk", "idle"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart70052.lua.lua
**Snippet:**
```lua
BasePlotDialogPart70052 = {
  [1140205001] = {
    id = 1140205001,
    talk_text = function()
      return T_S(11402050010)
    end,
    env_sound = 20005
  },
  [1140206001] = {
    id = 1140206001,
```

---

## Base/BasePlotDialogPart70053.lua.lua
**Snippet:**
```lua
BasePlotDialogPart70053 = {
  [1140207001] = {
    id = 1140207001,
    talk_text = function()
      return T_S(11402070010)
    end,
    is_master = 1,
    next_dialog = 1140207002,
    text_sound_path = "event:/voice_cn/story/M0000/M0000_story_00711",
    text_sound_bank = "bank:/voice_cn/sty/M0000_8_14th",
```

---

## Base/BasePlotDialogPart70054.lua.lua
**Snippet:**
```lua
BasePlotDialogPart70054 = {
  [1140209001] = {
    id = 1140209001,
    talk_text = function()
      return T_S(11402090010)
    end,
    next_dialog = 1140209002,
    speak_name = function()
      return T_S(11402090015)
    end,
```

---

## Base/BasePlotDialogPart70100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart70100 = {
  [1140301001] = {
    id = 1140301001,
    talk_text = function()
      return T_S(11403010010)
    end,
    next_dialog = 1140301002,
    env_sound = 20003,
    open_title_1 = function()
      return T_S(11403010018)
```

---

## Base/BasePlotDialogPart70101.lua.lua
**Snippet:**
```lua
BasePlotDialogPart70101 = {
  [1140303001] = {
    id = 1140303001,
    talk_text = function()
      return T_S(11403030010)
    end,
    next_dialog = 1140303002,
    env_sound = 20006
  },
  [1140303002] = {
```

---

## Base/BasePlotDialogPart70102.lua.lua
**Snippet:**
```lua
BasePlotDialogPart70102 = {
  [1140305001] = {
    id = 1140305001,
    talk_text = function()
      return T_S(11403050010)
    end,
    next_dialog = 1140305002,
    speak_name = function()
      return T_S(11403050015)
    end,
```

---

## Base/BasePlotDialogPart70103.lua.lua
**Snippet:**
```lua
BasePlotDialogPart70103 = {
  [1140307001] = {
    id = 1140307001,
    talk_text = function()
      return T_S(11403070010)
    end,
    role_ids = {90110010},
    scale = {10000},
    action_timeline = {
      "Assets/Art/PlotPlay/Timeline/DialogAction/1140307001/1140307001_90110010.playable"
```

---

## Base/BasePlotDialogPart70150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart70150 = {
  [1140401001] = {
    id = 1140401001,
    talk_text = function()
      return T_S(11404010010)
    end,
    role_ids = {90110003},
    scale = {10000},
    skin = {"common"},
    action_timeline = {
```

---

## Base/BasePlotDialogPart70200.lua.lua
**Snippet:**
```lua
BasePlotDialogPart70200 = {
  [1140501001] = {
    id = 1140501001,
    talk_text = function()
      return T_S(11405010010)
    end,
    next_dialog = 1140501002,
    speak_head = 90120064,
    speak_head_actions = {"talk", "idle"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart70201.lua.lua
**Snippet:**
```lua
BasePlotDialogPart70201 = {
  [1140503001] = {
    id = 1140503001,
    talk_text = function()
      return T_S(11405030010)
    end,
    next_dialog = 1140503002,
    env_sound = 20004
  },
  [1140503002] = {
```

---

## Base/BasePlotDialogPart70202.lua.lua
**Snippet:**
```lua
BasePlotDialogPart70202 = {
  [1140505001] = {
    id = 1140505001,
    talk_text = function()
      return T_S(11405050010)
    end,
    role_ids = {90110009, 90110010},
    scale = {10000, 10000},
    action = {"", ""},
    action_timeline = {
```

---

## Base/BasePlotDialogPart70250.lua.lua
**Snippet:**
```lua
BasePlotDialogPart70250 = {
  [1140601001] = {
    id = 1140601001,
    talk_text = function()
      return T_S(11406010010)
    end,
    next_dialog = 1140601002,
    speak_head = 90120064,
    speak_head_actions = {"talk", "idle"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart70251.lua.lua
**Snippet:**
```lua
BasePlotDialogPart70251 = {
  [1140603001] = {
    id = 1140603001,
    talk_text = function()
      return T_S(11406030010)
    end,
    next_dialog = 1140603002,
    env_sound = 20005
  },
  [1140603002] = {
```

---

## Base/BasePlotDialogPart70252.lua.lua
**Snippet:**
```lua
BasePlotDialogPart70252 = {
  [1140605001] = {
    id = 1140605001,
    talk_text = function()
      return T_S(11406050010)
    end,
    next_dialog = 1140605002,
    env_sound = 20009
  },
  [1140605002] = {
```

---

## Base/BasePlotDialogPart75000.lua.lua
**Snippet:**
```lua
BasePlotDialogPart75000 = {
  [1150101001] = {
    id = 1150101001,
    talk_text = function()
      return T_S(11501010010)
    end,
    next_dialog = 1150101002,
    camera_scale = {
      "1",
      "0",
```

---

## Base/BasePlotDialogPart75001.lua.lua
**Snippet:**
```lua
BasePlotDialogPart75001 = {
  [1150103001] = {
    id = 1150103001,
    talk_text = function()
      return T_S(11501030010)
    end,
    next_dialog = 1150103002,
    env_sound = 20002
  },
  [1150103002] = {
```

---

## Base/BasePlotDialogPart75002.lua.lua
**Snippet:**
```lua
BasePlotDialogPart75002 = {
  [1150105001] = {
    id = 1150105001,
    talk_text = function()
      return T_S(11501050010)
    end,
    next_dialog = 1150105002,
    env_sound = 20008
  },
  [1150105002] = {
```

---

## Base/BasePlotDialogPart75050.lua.lua
**Snippet:**
```lua
BasePlotDialogPart75050 = {
  [1150201001] = {
    id = 1150201001,
    talk_text = function()
      return T_S(11502010010)
    end,
    next_dialog = 1150201002,
    env_sound = 20005,
    open_title_1 = function()
      return T_S(11502010018)
```

---

## Base/BasePlotDialogPart75051.lua.lua
**Snippet:**
```lua
BasePlotDialogPart75051 = {
  [1150203001] = {
    id = 1150203001,
    talk_text = function()
      return T_S(11502030010)
    end,
    next_dialog = 1150203002,
    camera_shake = {
      "2",
      "0",
```

---

## Base/BasePlotDialogPart75052.lua.lua
**Snippet:**
```lua
BasePlotDialogPart75052 = {
  [1150205001] = {
    id = 1150205001,
    talk_text = function()
      return T_S(11502050010)
    end,
    next_dialog = 1150205002,
    speak_head = 90120031,
    speak_head_actions = {"talk", "idle"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart75100.lua.lua
**Snippet:**
```lua
BasePlotDialogPart75100 = {
  [1150301001] = {
    id = 1150301001,
    talk_text = function()
      return T_S(11503010010)
    end,
    next_dialog = 1150301002,
    env_sound = 20007,
    open_title_1 = function()
      return T_S(11503010018)
```

---

## Base/BasePlotDialogPart75101.lua.lua
**Snippet:**
```lua
BasePlotDialogPart75101 = {
  [1150303001] = {
    id = 1150303001,
    talk_text = function()
      return T_S(11503030010)
    end,
    next_dialog = 1150303002,
    env_sound = 20005
  },
  [1150303002] = {
```

---

## Base/BasePlotDialogPart75102.lua.lua
**Snippet:**
```lua
BasePlotDialogPart75102 = {
  [1150305001] = {
    id = 1150305001,
    talk_text = function()
      return T_S(11503050010)
    end,
    next_dialog = 1150305002,
    speak_head = 90120031,
    speak_head_actions = {"talk", "idle"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart75150.lua.lua
**Snippet:**
```lua
BasePlotDialogPart75150 = {
  [1150401001] = {
    id = 1150401001,
    talk_text = function()
      return T_S(11504010010)
    end,
    next_dialog = 1150401002,
    speak_head = 90120031,
    speak_head_actions = {"talk", "idle"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart75151.lua.lua
**Snippet:**
```lua
BasePlotDialogPart75151 = {
  [1150403001] = {
    id = 1150403001,
    talk_text = function()
      return T_S(11504030010)
    end,
    next_dialog = 1150403002,
    speak_head = 90120031,
    speak_head_actions = {"talk", "idle"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart75152.lua.lua
**Snippet:**
```lua
BasePlotDialogPart75152 = {
  [1150405001] = {
    id = 1150405001,
    middle_text = function()
      return T_S(11504050013)
    end,
    next_dialog = 1150405002,
    speak_name = function()
      return T_S(11504050015)
    end,
```

---

## Base/BasePlotDialogPart75153.lua.lua
**Snippet:**
```lua
BasePlotDialogPart75153 = {
  [1150407001] = {
    id = 1150407001,
    talk_text = function()
      return T_S(11504070010)
    end,
    next_dialog = 1150407002,
    env_sound = 20003
  },
  [1150407002] = {
```

---

## Base/BasePlotDialogPart75154.lua.lua
**Snippet:**
```lua
BasePlotDialogPart75154 = {
  [1150409001] = {
    id = 1150409001,
    talk_text = function()
      return T_S(11504090010)
    end,
    next_dialog = 1150409002,
    env_sound = 20003
  },
  [1150409002] = {
```

---

## Base/BasePlotDialogPart75200.lua.lua
**Snippet:**
```lua
BasePlotDialogPart75200 = {
  [1150501001] = {
    id = 1150501001,
    talk_text = function()
      return T_S(11505010010)
    end,
    next_dialog = 1150501002,
    speak_head = 90120031,
    speak_head_actions = {"talk", "idle"},
    speak_name = function()
```

---

## Base/BasePlotDialogPart75201.lua.lua
**Snippet:**
```lua
BasePlotDialogPart75201 = {
  [1150503001] = {
    id = 1150503001,
    talk_text = function()
      return T_S(11505030010)
    end,
    next_dialog = 1150503002,
    env_sound = 20007
  },
  [1150503002] = {
```

---

## Base/BasePlotHead.lua.lua
**Snippet:**
```lua
BasePlotHead = {
  [90120001] = {
    id = 90120001,
    name = function()
      return T(80100019)
    end,
    spine_path = "Assets/Art/Models/DialogHead/prefab/dialoghead_12033001.prefab",
    head_icon = "CardHeadRect:HeadRect_10003_1"
  },
  [90120002] = {
```

---

## Base/BasePlotPart.lua.lua
**Snippet:**
```lua
BasePlotPart = {
  [10001] = {
    id = 10001,
    section_ids = {1000101},
    skip_tips = function()
      return T_S(100011)
    end,
    use_static = 0
  },
  [10002] = {
```

---

## Base/BasePlotPlayBG.lua.lua
**Snippet:**
```lua
BasePlotPlayBG = {
  [70141001] = {
    id = 70141001,
    cg_path = "FX_CG_001.prefab",
    effect_sound = 21001,
    snapshot_path = "snapshot:/Story_Reverb/revb_70141001"
  },
  [70141002] = {
    id = 70141002,
    cg_path = "FX_CG_002.prefab",
```

---

## Base/BasePlotReward.lua.lua
**Snippet:**
```lua
BasePlotReward = {
  [1040603007] = {
    id = 1040603007,
    reward = {
      "1:21150001:1"
    }
  },
  [1060201033] = {
    id = 1060201033,
    reward = {
```

---

## Base/BasePlotRole.lua.lua
**Snippet:**
```lua
BasePlotRole = {
  [90110001] = {
    id = 90110001,
    name = function()
      return T(80100001)
    end,
    spine_path = "npcspine_90110001.prefab",
    head_icon = "CardHeadRect:HeadRect_10018_1",
    texture_path = "npc_texture_90110001.prefab"
  },
```

---

## Base/BasePlotSection.lua.lua
**Snippet:**
```lua
BasePlotSection = {
  [1010101] = {
    id = 1010101,
    bg_id = 90210064,
    dialog_ids = {
      1010101001,
      1010101002,
      1010101003,
      1010101004,
      1010101005,
```

---

## Base/BasePlotWord_cn.lua.lua
**Snippet:**
```lua
BasePlotWord_cn = {
  [10101] = {
    id = 10101,
    name = "学员遇险"
  },
  [101011] = {
    id = 101011,
    name = "在安妮斯的请求下，阔别深渊多年的你决定再次前往深渊，营救被困的学员......"
  },
  [10101010010] = {
```

---

## Base/BasePlotWord_jp.lua.lua
**Snippet:**
```lua
BasePlotWord_jp = {
  [10101] = {id = 10101},
  [101011] = {id = 101011},
  [10101010010] = {id = 10101010010},
  [10101020010] = {id = 10101020010},
  [10101020020] = {id = 10101020020},
  [10101020025] = {id = 10101020025},
  [10101020030] = {id = 10101020030},
  [10101020035] = {id = 10101020035},
  [10101020040] = {id = 10101020040},
```

---

## Base/BaseRaidBossReward.lua.lua
**Snippet:**
```lua
BaseRaidBossReward = {
  [24020101] = {
    id = 24020101,
    phase = 1,
    rank_type = 1,
    rank_high = 1,
    rank_low = 5,
    reward = {
      "1:21181001:1",
      "1:21000001:1500",
```

---

## Base/BaseRogueCardAttribEnhance.lua.lua
**Snippet:**
```lua
BaseRogueCardAttribEnhance = {
  [50851101] = {
    id = 50851101,
    group_id = 101,
    attrib_id = 40000103,
    star = 1,
    level = 0,
    cost = {
      "1:21160004:3"
    }
```

---

## Base/BaseRogueChapter.lua.lua
**Snippet:**
```lua
BaseRogueChapter = {
  [50831111] = {
    id = 50831111,
    group_id = 101,
    layer_index = 1,
    name = function()
      return T(80272111)
    end,
    map_path = "RogueBuild01:Map_101",
    back_ground = "RogueBuild01:Map_1"
```

---

## Base/BaseRogueDifficulty.lua.lua
**Snippet:**
```lua
BaseRogueDifficulty = {
  [50803100] = {
    id = 50803100,
    group_id = 101,
    name = function()
      return T(80264101)
    end,
    des = function()
      return T(80265101)
    end,
```

---

## Base/BaseRogueEnding.lua.lua
**Snippet:**
```lua
BaseRogueEnding = {
  [50806101] = {
    id = 50806101,
    group_id = 101,
    name = function()
      return T(80271103)
    end,
    des_title = function()
      return T(80271103)
    end,
```

---

## Base/BaseRogueEndingPool.lua.lua
**Snippet:**
```lua
BaseRogueEndingPool = {
  [5130101] = {
    id = 5130101,
    group_id = 101,
    stage_id = 51100321,
    priority = 1,
    ending_id = 50806101
  },
  [5130102] = {
    id = 5130102,
```

---

## Base/BaseRogueEvent.lua.lua
**Snippet:**
```lua
BaseRogueEvent = {
  [50805101] = {
    id = 50805101,
    group_id = 101,
    name = function()
      return T(80268101)
    end,
    des_title = function()
      return T(80269101)
    end,
```

---

## Base/BaseRogueHoly.lua.lua
**Snippet:**
```lua
BaseRogueHoly = {
  [50821001] = {
    id = 50821001,
    group_id = 101,
    name = function()
      return T(86761001)
    end,
    des = function()
      return T(86771001)
    end,
```

---

## Base/BaseRogueLevel.lua.lua
**Snippet:**
```lua
BaseRogueLevel = {
  [50800001001] = {
    id = 50800001001,
    level = 1,
    next_exp = 100,
    reward = {
      "1:21000003:10000"
    },
    unlock_phase = 0,
    phase_show_id = "1:21000001",
```

---

## Base/BaseRogueNode.lua.lua
**Snippet:**
```lua
BaseRogueNode = {
  [50911101] = {
    id = 50911101,
    name = function()
      return T(80273001)
    end,
    name_detail = function()
      return T(80273001)
    end,
    chapter_id = 50831111,
```

---

## Base/BaseRogueNodeReward.lua.lua
**Snippet:**
```lua
BaseRogueNodeReward = {
  [50841001] = {
    id = 50841001,
    name = function()
      return T(80274001)
    end,
    des = function()
      return T(80275001)
    end,
    type = 1
```

---

## Base/BaseRoguePool.lua.lua
**Snippet:**
```lua
BaseRoguePool = {
  [51010101] = {
    id = 51010101,
    group_id = 101,
    type = 1,
    difficulty_range = {0, 99},
    layerIndex_range = {1, 1},
    parameter = "51100111"
  },
  [51010102] = {
```

---

## Base/BaseRogueScore.lua.lua
**Snippet:**
```lua
BaseRogueScore = {
  [50861001] = {
    id = 50861001,
    group_id = 101,
    name = function()
      return T(80276001)
    end,
    icon = "ItemIcon:gold1",
    type = 1,
    score_unit = "200|400|600|800|1000|1200",
```

---

## Base/BaseRogueTalent.lua.lua
**Snippet:**
```lua
BaseRogueTalent = {
  [50804101] = {
    id = 50804101,
    group_id = 101,
    name = function()
      return T(80266101)
    end,
    des = function()
      return T(80267101, 10)
    end,
```

---

## Base/BaseRogueTalentAtt.lua.lua
**Snippet:**
```lua
BaseRogueTalentAtt = {
  [10101] = {
    id = 10101,
    name = function()
      return T(80267001)
    end,
    type = "1:40000103"
  },
  [10102] = {
    id = 10102,
```

---

## Base/BaseRogueTheme.lua.lua
**Snippet:**
```lua
BaseRogueTheme = {
  [50800001] = {
    id = 50800001,
    name = function()
      return T(80260001)
    end,
    name_level = function()
      return T(80260002)
    end,
    level_exp_item = 21160001,
```

---

## Base/BaseRogueTreasure.lua.lua
**Snippet:**
```lua
BaseRogueTreasure = {
  [50811001] = {
    id = 50811001,
    group_id = 101,
    name = function()
      return T(86731001)
    end,
    des = function()
      return T(86741001)
    end,
```

---

## Base/BaseRogueTreasureDrop.lua.lua
**Snippet:**
```lua
BaseRogueTreasureDrop = {
  [50806100] = {
    id = 50806100,
    drop = {
      "50811002:1:0",
      "50811013:1:0",
      "50811021:1:0",
      "50811028:1:0",
      "50811034:1:0",
      "50811045:1:0",
```

---

## Base/BaseRogueTreasureType.lua.lua
**Snippet:**
```lua
BaseRogueTreasureType = {
  [50810001] = {
    id = 50810001,
    level = 1,
    type = 4,
    icon = "RogueBuild01:50810001"
  },
  [50810002] = {
    id = 50810002,
    level = 2,
```

---

## Base/BaseRogueTrends.lua.lua
**Snippet:**
```lua
BaseRogueTrends = {
  [50802011] = {
    id = 50802011,
    group_id = 101,
    chapter_id = 50802010,
    name = function()
      return T(80261011)
    end,
    des = function()
      return T(80262011)
```

---

## Base/BaseRogueTrendsChapter.lua.lua
**Snippet:**
```lua
BaseRogueTrendsChapter = {
  [50802010] = {
    id = 50802010,
    group_id = 101,
    name = function()
      return T(80261010)
    end,
    des = function()
      return T(80262010)
    end,
```

---

## Base/BaseSeal.lua.lua
**Snippet:**
```lua
BaseSeal = {
  [21171101] = {
    id = 21171101,
    job = 1,
    attr_type = 1,
    level = 1,
    value = {
      "1:40000103:25"
    },
    cost = {
```

---

## Base/BaseSealBigAddUp.lua.lua
**Snippet:**
```lua
BaseSealBigAddUp = {
  [21180001000] = {id = 21180001000},
  [21180001001] = {
    id = 21180001001,
    add_attr = 1000,
    cost = {
      "1:21000003:12000",
      "1:21030501:2",
      "1:21020005:3"
    },
```

---

## Base/BaseSealBigLevelUp.lua.lua
**Snippet:**
```lua
BaseSealBigLevelUp = {
  [21180001000] = {id = 21180001000},
  [21180001001] = {
    id = 21180001001,
    add_attr = {
      "1:40000103:4",
      "1:40000104:0",
      "1:40000102:0"
    },
    cost = {
```

---

## Base/BaseSealBigQualityUp.lua.lua
**Snippet:**
```lua
BaseSealBigQualityUp = {
  [21180001000] = {
    id = 21180001000,
    add_attr = {
      "1:40000103:8",
      "1:40000104:10",
      "1:40000102:160"
    },
    cost = {
      "1:21000003:50000",
```

---

## Base/BaseSealJob.lua.lua
**Snippet:**
```lua
BaseSealJob = {
  [21170001] = {
    id = 21170001,
    job = 1,
    holes = {
      1,
      2,
      3
    },
    seal_big_id = 21180001
```

---

## Base/BaseSealOnHookLevel.lua.lua
**Snippet:**
```lua
BaseSealOnHookLevel = {
  [21000030001] = {id = 21000030001, next_exp = 500},
  [21000030002] = {id = 21000030002, next_exp = 525},
  [21000030003] = {id = 21000030003, next_exp = 551},
  [21000030004] = {id = 21000030004, next_exp = 578},
  [21000030005] = {id = 21000030005, next_exp = 606},
  [21000030006] = {id = 21000030006, next_exp = 636},
  [21000030007] = {id = 21000030007, next_exp = 699},
  [21000030008] = {id = 21000030008, next_exp = 768},
  [21000030009] = {id = 21000030009, next_exp = 844},
```

---

## Base/BaseShootCard.lua.lua
**Snippet:**
```lua
BaseShootCard = {
  [78000100] = {
    id = 78000100,
    type = 5,
    max_hp = 5000,
    atk = 0,
    crt = 0,
    spd_atk = 0,
    range_atk = {0},
    spd = "Assets/Art/Models/MiniGame022/prefab/minigamespine_zhalan_pixel.prefab",
```

---

## Base/BaseShootMonsterGroup.lua.lua
**Snippet:**
```lua
BaseShootMonsterGroup = {
  [78029901] = {
    id = 78029901,
    group_id = 99,
    wave_num = 0,
    interval_time = 0,
    monsters = {"78000201:1"},
    add_hp_per = 0,
    add_exp_per = 0
  },
```

---

## Base/BaseShootSkill.lua.lua
**Snippet:**
```lua
BaseShootSkill = {
  [78010110] = {
    id = 78010110,
    name = function()
      return T(80440110)
    end,
    des = function()
      return T(80450110)
    end,
    icon = "ActivityDungeon1017Battle:Skill_10018_1",
```

---

## Base/BaseShootSkillBuff.lua.lua
**Snippet:**
```lua
BaseShootSkillBuff = {
  [78040101] = {
    id = 78040101,
    value = {
      "2002:2:2:40000103:3000:0"
    },
    settle_type = 0,
    deduce_type = 999
  },
  [78040102] = {
```

---

## Base/BaseShootStage.lua.lua
**Snippet:**
```lua
BaseShootStage = {
  [78000001] = {
    id = 78000001,
    name = function()
      return T(80220001, "01")
    end,
    pre = 0,
    next = {78000002},
    unlock_day = 0,
    card_id = {
```

---

## Base/BaseShop.lua.lua
**Snippet:**
```lua
BaseShop = {
  [23000001] = {
    id = 23000001,
    name = function()
      return T(80612001)
    end,
    name_english = function()
      return T(80612101)
    end,
    type = 1,
```

---

## Base/BaseShopGrid.lua.lua
**Snippet:**
```lua
BaseShopGrid = {
  [23010101] = {
    id = 23010101,
    shop_type = 1,
    reset_type = 1,
    reset_time = {
      "3:010500:MX0"
    },
    sell_limit_time = 5,
    open_condition = {"70020100:1"},
```

---

## Base/BaseShopPool.lua.lua
**Snippet:**
```lua
BaseShopPool = {
  [23110101] = {
    id = 23110101,
    grid_id = 23010101,
    item = "1:21100004:1",
    sell_price = "1:21000201:60",
    prob = 10000,
    open_condition = {"70020100:1"}
  },
  [23110102] = {
```

---

## Base/BaseSkill.lua.lua
**Snippet:**
```lua
BaseSkill = {
  [41011000] = {
    id = 41011000,
    type = 8,
    max_level = 0
  },
  [41011101] = {
    id = 41011101,
    name = function()
      return T(80418002)
```

---

## Base/BaseSkillBuff.lua.lua
**Snippet:**
```lua
BaseSkillBuff = {
  [43100001] = {
    id = 43100001,
    type = 1,
    value = {
      "519:0:0:0:0:0"
    },
    trigger_condition = 0,
    trigger_type = 0,
    trigger_value = 0,
```

---

## Base/BaseSkillBuffEffect.lua.lua
**Snippet:**
```lua
BaseSkillBuffEffect = {
  [1] = {id = 1},
  [101] = {id = 101, attribute_id = 40000101},
  [102] = {id = 102, attribute_id = 40000101},
  [103] = {
    id = 103,
    attribute_id = 40000101,
    def = 1,
    element_type = {2},
    restraint_add3 = 3000,
```

---

## Base/BaseSkillBuffPre.lua.lua
**Snippet:**
```lua
BaseSkillBuffPre = {
  [46101101] = {
    id = 46101101,
    name = function()
      return T(80900001)
    end,
    des = function()
      return T(80910010, 10)
    end,
    icon = "BuffIcon:tower_0101",
```

---

## Base/BaseSkillLevelUp.lua.lua
**Snippet:**
```lua
BaseSkillLevelUp = {
  [41011000001] = {
    id = 41011000001,
    trigger_limit = {1001},
    trigger_limit_type = {5},
    trigger_limit_value = {100},
    buff_list = {
      "43100001:3002:10000",
      "43100002:3002:10000"
    }
```

---

## Base/BaseSkillParameter.lua.lua
**Snippet:**
```lua
BaseSkillParameter = {
  [40001001] = {id = 40001001, data = 10000},
  [40001002] = {id = 40001002, data = 0},
  [40001003] = {id = 40001003, data = 10000},
  [40001004] = {id = 40001004, data = 0},
  [40001005] = {id = 40001005, data = 100000},
  [40001006] = {id = 40001006, data = 0},
  [40001007] = {id = 40001007, data = 10000},
  [40001008] = {id = 40001008, data = 0},
  [40001009] = {id = 40001009, data = 10000},
```

---

## Base/BaseSkillShow.lua.lua
**Snippet:**
```lua
BaseSkillShow = {
  [42110100] = {
    id = 42110100,
    total_f = 31,
    display_ids = {42110151, 42110152}
  },
  [42310100] = {
    id = 42310100,
    total_f = 66,
    display_ids = {42310151}
```

---

## Base/BaseSkillShowDisplay.lua.lua
**Snippet:**
```lua
BaseSkillShowDisplay = {
  [42810001] = {
    id = 42810001,
    bullet_effect = "10003/FX_10003_skill1_bullet.prefab",
    bullet_hit_effect = "10003/FX_10003_skill1_hit.prefab",
    bullet_scale = 5000,
    bend_scale = {1},
    bullet_speed = 300,
    max_distance = 200
  },
```

---

## Base/BaseSkillShowGroup.lua.lua
**Snippet:**
```lua
BaseSkillShowGroup = {
  [1004301] = {
    id = 1004301,
    fashion_show_ids = {
      "12001431:42114356",
      "12001432:42114356",
      "12001433:42114362"
    }
  },
  [1004302] = {
```

---

## Base/BaseSkillSummon.lua.lua
**Snippet:**
```lua
BaseSkillSummon = {
  [1001] = {
    id = 1001,
    building_id = 13100000,
    pos = {
      1,
      0,
      0
    },
    destroy_time = 999,
```

---

## Base/BaseSkillSummonGroup.lua.lua
**Snippet:**
```lua
BaseSkillSummonGroup = {
  [101] = {
    id = 101,
    summon_id = {
      20101,
      20101,
      20102,
      20102
    },
    summon_site = {
```

---

## Base/BaseSkillTag.lua.lua
**Snippet:**
```lua
BaseSkillTag = {
  [101] = {
    id = 101,
    name = function()
      return T(80661101)
    end,
    icon = "Battle:Bust_1004"
  },
  [102] = {
    id = 102,
```

---

## Base/BaseSound.lua.lua
**Snippet:**
```lua
BaseSound = {
  [70160001] = {
    id = 70160001,
    name = function()
      return T(80881001)
    end,
    path = "event:/bgm/bgm_system/bgm_system_login96bpm",
    bank = "bank:/bgm/bgm_system/bgm_system_login96bpm",
    bg_path = "FX_ui_StoryMusicPic_1000.prefab",
    composer = function()
```

---

## Base/BaseSoundChapter.lua.lua
**Snippet:**
```lua
BaseSoundChapter = {
  [70150001] = {
    id = 70150001,
    name = function()
      return T(80880001)
    end,
    icon = "StoryMusicPic:StoryMusicPic_1000",
    child_ids = {
      70160001,
      70160002,
```

---

## Base/BaseSoundPath.lua.lua
**Snippet:**
```lua
BaseSoundPath = {
  [1001] = {
    id = 1001,
    path = "event:/bgm/bgm_system/bgm_system_main77bpm",
    bank = "bank:/bgm/bgm_system/bgm_system_main77bpm",
    trigger_sound = 100104
  },
  [1010] = {
    id = 1010,
    path = "event:/bgm/bgm_system/bgm_system_login96bpm",
```

---

## Base/BaseStage.lua.lua
**Snippet:**
```lua
BaseStage = {
  [50110101] = {
    id = 50110101,
    name = function()
      return T(80220001, "01")
    end,
    name_detail = function()
      return T(80221001)
    end,
    name_english = function()
```

---

## Base/BaseStageChallenge.lua.lua
**Snippet:**
```lua
BaseStageChallenge = {
  [101] = {
    id = 101,
    name = function()
      return T(80680101, 30)
    end,
    condition = {"1:5:30", ""}
  },
  [201] = {
    id = 201,
```

---

## Base/BaseStageScore.lua.lua
**Snippet:**
```lua
BaseStageScore = {
  [1001] = {
    id = 1001,
    time_range = {0, 2700},
    monster_score = {
      50,
      50,
      500,
      500,
      500
```

---

## Base/BaseStory.lua.lua
**Snippet:**
```lua
BaseStory = {
  [70200101] = {
    id = 70200101,
    name = function()
      return T(80830001)
    end,
    name_detail = function()
      return T(80831011)
    end,
    open_condition = "70020200:50110101",
```

---

## Base/BaseStoryCg.lua.lua
**Snippet:**
```lua
BaseStoryCg = {
  [70140001] = {
    id = 70140001,
    name = function()
      return T(80850001)
    end,
    name_english = function()
      return T(80852001)
    end,
    des = function()
```

---

## Base/BaseStoryCgChapter.lua.lua
**Snippet:**
```lua
BaseStoryCgChapter = {
  [70130001] = {
    id = 70130001,
    name = function()
      return T(80850001)
    end,
    type = 1,
    child_ids = {
      70140001,
      70140002,
```

---

## Base/BaseStoryChapter.lua.lua
**Snippet:**
```lua
BaseStoryChapter = {
  [70110001] = {
    id = 70110001,
    name = function()
      return T(80810001)
    end,
    name_english = function()
      return T(80812001)
    end,
    des = function()
```

---

## Base/BaseStoryMonster.lua.lua
**Snippet:**
```lua
BaseStoryMonster = {
  [70181001] = {
    id = 70181001,
    name = function()
      return T(80301001)
    end,
    des = {80311001, 80321001},
    type = 4,
    level = function()
      return T(80300001)
```

---

## Base/BaseStoryMonsterCamp.lua.lua
**Snippet:**
```lua
BaseStoryMonsterCamp = {
  [70170001] = {
    id = 70170001,
    name = function()
      return T(80840001)
    end,
    name_english = function()
      return T(80841001)
    end,
    icon = "StoryMonsterPic:StoryMonsterPic_1000",
```

---

## Base/BaseStoryRelation.lua.lua
**Snippet:**
```lua
BaseStoryRelation = {
  [70120001] = {
    id = 70120001,
    name = function()
      return T(80841001)
    end,
    name_english = function()
      return T(80842001)
    end,
    des = function()
```

---

## Base/BaseStorySimple.lua.lua
**Snippet:**
```lua
BaseStorySimple = {
  [77000101] = {
    id = 77000101,
    type = 4,
    remark = function()
      return T(86100101)
    end,
    next = 77000102
  },
  [77000102] = {
```

---

## Base/BaseSubSkill.lua.lua
**Snippet:**
```lua
BaseSubSkill = {
  [42110101] = {
    id = 42110101,
    damage_rate = {5000}
  },
  [42110102] = {
    id = 42110102,
    damage_rate = {5000}
  },
  [42310101] = {
```

---

## Base/BaseTask.lua.lua
**Snippet:**
```lua
BaseTask = {
  [70050001] = {
    id = 70050001,
    name = function()
      return T(80630500, 1)
    end,
    belong = 1,
    task_condition = 500,
    task_parameter = {1},
    is_inherit = 0,
```

---

## Base/BaseTaskCommon.lua.lua
**Snippet:**
```lua
BaseTaskCommon = {
  [70053201] = {
    id = 70053201,
    index = 1,
    reward = {
      "1:21000015:20",
      "1:21000005:80",
      "1:21000012:20",
      "1:21000016:20"
    },
```

---

## Base/BaseTaskPool.lua.lua
**Snippet:**
```lua
BaseTaskPool = {
  [70053301] = {
    id = 70053301,
    drop = "3:70053001:1:10|3:70053002:1:10|3:70053003:1:10|3:70053004:1:10|3:70053005:1:10|3:70053006:1:10|3:70053007:1:10|3:70053008:1:10|3:70053009:1:10|3:70053010:1:10|3:70053101:1:10|3:70053102:1:10|3:70053103:1:10|3:70053104:1:10|3:70053106:1:10|3:70053107:1:10"
  },
  [70070901] = {
    id = 70070901,
    drop = "3:70052001:1:10|3:70052002:1:10|3:70052003:1:10|3:70052004:1:10|3:70052005:1:10|3:70052006:1:10|3:70052007:1:10|3:70052008:1:10"
  }
}
```

---

## Base/BaseTaskTarget.lua.lua
**Snippet:**
```lua
BaseTaskTarget = {
  [70071001] = {
    id = 70071001,
    type = 3,
    index = 1,
    reward = {
      "1:21000005:20",
      "1:21000001:20",
      "1:21000003:1000"
    },
```

---

## Base/BaseTowerMap.lua.lua
**Snippet:**
```lua
BaseTowerMap = {
  [70072001] = {
    id = 70072001,
    name = function()
      return T(80256001)
    end,
    name_english = function()
      return T(80257001)
    end,
    des = function()
```

---

## Base/BaseWord_cn.lua.lua
**Snippet:**
```lua
BaseWord_cn = {
  [1] = {id = 1, name = "UID:%s"},
  [2] = {id = 2, name = "%s  %s"},
  [3] = {id = 3, name = "招募"},
  [4] = {
    id = 4,
    name = "[size=30]深[/size]渊探索"
  },
  [5] = {id = 5, name = "探险队"},
  [6] = {id = 6, name = "事 迹"},
```

---

## Base/BaseWord_jp.lua.lua
**Snippet:**
```lua
BaseWord_jp = {
  [1] = {id = 1},
  [2] = {id = 2},
  [3] = {id = 3},
  [4] = {id = 4},
  [5] = {id = 5},
  [6] = {id = 6},
  [7] = {id = 7},
  [8] = {id = 8},
  [9] = {id = 9},
```

---

## Base/Base_AniByName.lua.lua
**Functions:**
- GetBase_AniUis
**Snippet:**
```lua
function GetBase_AniUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Base/Base_NoneComponentByName.lua.lua
**Functions:**
- GetBase_NoneComponentUis
**Snippet:**
```lua
function GetBase_NoneComponentUis(ui)
  local uis = {}
  
  uis.root = ui
  return uis
end
```

---

## Base/Base_UILayerByName.lua.lua
**Functions:**
- GetBase_UILayerUis
**Requires:**
- Base_NoneComponentByName
**Snippet:**
```lua
require("Base_NoneComponentByName")

function GetBase_UILayerUis(ui)
  local uis = {}
  uis.Bottom = GetBase_NoneComponentUis(ui:GetChild("Bottom"))
  uis.MainUI = GetBase_NoneComponentUis(ui:GetChild("MainUI"))
  uis.HUD = GetBase_NoneComponentUis(ui:GetChild("HUD"))
  uis.HUD1 = GetBase_NoneComponentUis(ui:GetChild("HUD1"))
  uis.Popup = GetBase_NoneComponentUis(ui:GetChild("Popup"))
  uis.Notice = GetBase_NoneComponentUis(ui:GetChild("Notice"))
```

---
