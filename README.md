{
  "id": 0,
  "name": "默认订阅",
  "version": 71,
  "author": "lisonge",
  "supportUri": "https://github.com/gkd-kit/subscription",
  "apps": [
    {
      "id": "air.tv.douyu.android",
      "name": "斗鱼",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": [
            "com.douyu.module.home.pages.main.MainActivity",
            "com.douyu.module.ad.launch.HotStartSplashActivity"
          ],
          "rules": [
            {
              "matches": "@TextView[text^='跳过'] + LinearLayout TextView[text*=\"跳转\"]",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/38517192/50c858ee-d331-4d5a-b5db-5eb17323c5ff"
            },
            "[text^='跳过'] + * >2 TextView[text*='跳转']"
          ]
        },
        {
          "key": 1,
          "name": "青少年模式",
          "desc": "关闭青少年模式提醒弹窗",
          "activityIds": [
            "com.douyu.module.young.view.YoungModeGuideDialog",
            "com.douyu.module.home.pages.main.MainActivity"
          ],
          "snapshotUrls": "https://gkd-kit.gitee.io/import/38517192/1c081a65-688a-406b-b67b-9bfb9aba0fad",
          "rules": [
            "[text='开启青少年模式'] + [text='我知道了']"
          ]
        },
        {
          "key": 2,
          "name": "新版本弹窗",
          "activityIds": [
            "com.douyu.module.update.view.UpdateDialog",
            "com.douyu.module.home.pages.main.MainActivity"
          ],
          "rules": "[text=\"立即升级\"] - [text=\"忽略\"][clickable=true]"
        }
      ]
    },
    {
      "id": "cmb.pb",
      "name": "招商银行",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "cmb.pb.app.mainframe.container.PBMainActivity",
          "rules": "[id=`cmb.pb:id/ll_launch_ad_skip_hot_area`]"
        }
      ]
    },
    {
      "id": "cn.damai",
      "name": "大麦",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "cn.damai.launcher.splash.SplashMainActivity",
          "rules": "[id=\"cn.damai:id/homepage_advert_pb\"]",
          "snapshotUrls": "https://gkd-kit.gitee.io/import/38517192/38859663-6f0c-48b1-9392-20ae937a8c9e"
        }
      ]
    },
    {
      "id": "cn.wps.moffice_eng",
      "name": "WPS",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "cn.wps.moffice.documentmanager.PreStartActivity",
          "rules": "[id=`cn.wps.moffice_eng:id/splash_skip`]"
        },
        {
          "key": 1,
          "name": "首页-文档列表广告",
          "exampleUrls": [
            "https://github.com/gkd-kit/subscription/assets/38517192/57787554-0443-4bc0-9f29-1759aae07b9b"
          ],
          "activityIds": [
            "cn.wps.moffice.main.StartPublicActivity",
            "cn.wps.moffice.main.local.HomeRootActivity"
          ],
          "rules": [
            {
              "matches": "[text=\"关闭当前广告\"]",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/12505365"
            },
            {
              "matches": "[id$=\"/nativeclose\"]",
              "snapshotUrls": [
                "https://gkd-kit.gitee.io/import/12505350",
                "https://gkd-kit.gitee.io/import/12505286"
              ]
            }
          ]
        }
      ]
    },
    {
      "id": "com.MobileTicket",
      "name": "铁路12306",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.MobileTicket.ui.dialog.SplashAdDialog",
          "rules": "[id=`com.MobileTicket:id/tv_skip`]"
        }
      ]
    },
    {
      "id": "com.UCMobile",
      "name": "UC浏览器",
      "groups": [
        {
          "key": -1,
          "name": "开屏广告",
          "desc": "空规则组-待实现",
          "activityIds": "com.uc.browser.InnerUCMobile"
        },
        {
          "key": 0,
          "name": "推荐页广告",
          "activityIds": "com.uc.browser.InnerUCMobile",
          "rules": [
            "TextView[text=`屏蔽此条广告`]",
            "TextView[text=`广告`] +n ImageView[desc=`不感兴趣`]"
          ]
        }
      ]
    },
    {
      "id": "com.achievo.vipshop",
      "name": "唯品会",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.achievo.vipshop.activity.LodingActivity",
          "rules": "[id=`com.achievo.vipshop:id/adv_countdown`]"
        }
      ]
    },
    {
      "id": "com.alibaba.android.rimet",
      "name": "钉钉",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.alibaba.android.rimet.biz.SplashActivity",
          "rules": "[id=\"com.alibaba.android.rimet:id/btn_check_detail\"||text^=\"跳过\"]",
          "snapshotUrls": "https://gkd-kit.songe.li/import/12506211"
        }
      ]
    },
    {
      "id": "com.alibaba.wireless",
      "name": "阿里巴巴",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.alibaba.wireless.launch.home.V5HomeActivity",
          "rules": "[id=`com.alibaba.wireless:id/v5_splash_over`]"
        }
      ]
    },
    {
      "id": "com.android.bankabc",
      "name": "中国农业银行",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.alipay.mobile.quinox.LauncherActivity",
          "rules": [
            "ImageView[id=\"com.android.bankabc:id/close\"]"
          ],
          "snapshotUrls": "https://gkd-kit.gitee.io/import/38517192/3653218a-e0e0-4a60-8308-dea5fd4179b3"
        }
      ]
    },
    {
      "id": "com.android.thememanager",
      "name": "miui主题壁纸",
      "groups": [
        {
          "key": 1,
          "name": "推荐下广告",
          "desc": "注意如果使用ADB禁用了MIUI广告组件,点击此按钮会无反应,可关闭此规则,避免过多相同点击记录",
          "rules": "[id=`com.android.thememanager:id/ad_close_btn`]"
        }
      ]
    },
    {
      "id": "com.anjuke.android.app",
      "name": "安居客",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.anjuke.android.app.mainmodule.WelcomeActivity",
          "rules": "[id=`com.anjuke.android.app:id/skip_btn`]"
        }
      ]
    },
    {
      "id": "com.baidu.BaiduMap",
      "name": "百度地图",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.baidu.baidumaps.MapsActivity",
          "rules": [
            "@TextView[text^=`跳过`] + TextView[text=`广告`]",
            "ImageView[clickable=false] + TextView[text^='跳过'][clickable=true]"
          ]
        }
      ]
    },
    {
      "id": "com.baidu.duer.superapp",
      "name": "小度",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.baidu.duer.superapp.splash.SplashActivity",
          "rules": "[id=\"com.byted.pangle:id/tt_splash_skip_btn\"]",
          "snapshotUrls": "https://gkd-kit.gitee.io/import/12506571"
        }
      ]
    },
    {
      "id": "com.baidu.homework",
      "name": "作业帮",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.baidu.homework.activity.init.InitActivity",
          "rules": "[id=`com.baidu.homework:id/adx_splash_skip_text`]"
        }
      ]
    },
    {
      "id": "com.baidu.netdisk",
      "name": "百度网盘",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.baidu.netdisk.ui.Navigate",
          "rules": [
            {
              "matches": "TextView[text=\"跳过\"][clickable=true]",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/38517192/edc1d0a6-ebdd-48b0-9e11-f0b2c277c40a"
            },
            "@TextView[text^=`跳过`] + TextView[text=`广告`]",
            "[id='com.byted.pangle:id/tt_splash_skip_btn']"
          ]
        }
      ]
    },
    {
      "id": "com.baidu.tieba",
      "name": "百度贴吧",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "desc": "数字倒计时广告,圆形倒计时广告",
          "activityIds": [
            "com.baidu.tieba.tblauncher.MainTabActivity",
            "com.baidu.tieba.pb.pb.main.PbActivity"
          ],
          "rules": [
            "TextView[text*=`广告`] - TextView[text^=`跳过`]",
            "[id=`com.kwad.dy.sdk:id/ksad_splash_circle_skip_view`] TextView[text=`跳过`]",
            "[id=`com.byted.pangle:id/tt_splash_skip_btn`]"
          ]
        },
        {
          "key": 1,
          "name": "任意界面-选择不喜欢理由-不感兴趣",
          "rules": "@View[text=null] - TextView[text=`选择不喜欢理由`][index=0]"
        },
        {
          "key": 2,
          "name": "首页/贴吧帖子列表-推荐列表-长得像帖子的广告卡片",
          "activityIds": [
            "com.baidu.tieba.tblauncher.MainTabActivity",
            "com.baidu.tieba.frs.FrsActivity"
          ],
          "rules": [
            "ImageView < @FrameLayout < LinearLayout < RelativeLayout <n LinearLayout < RelativeLayout + LinearLayout > RelativeLayout > TextView[text$=`广告`]"
          ]
        },
        {
          "key": 3,
          "name": "某个广告卡片",
          "desc": "忘记是哪个卡片了",
          "activityIds": [
            "com.baidu.tieba.tblauncher.MainTabActivity",
            "com.baidu.tieba.pb.pb.main.PbActivity"
          ],
          "rules": "TextView[text=`广告`] <n FrameLayout <n LinearLayout - RelativeLayout @FrameLayout > ImageView"
        },
        {
          "key": 4,
          "name": "帖子评论区内部广告卡片",
          "activityIds": "com.baidu.tieba.frs.FrsActivity",
          "rules": "ImageView < @FrameLayout < LinearLayout < RelativeLayout <n LinearLayout < RelativeLayout + LinearLayout[id=`com.baidu.tieba:id/obfuscated`] TextView[text=`广告`]"
        },
        {
          "key": 5,
          "name": "帖子评论区广告卡片",
          "activityIds": "com.baidu.tieba.pb.pb.main.PbActivity",
          "rules": [
            "TextView[text=`广告`] <n FrameLayout +n RelativeLayout[id=`com.baidu.tieba:id/obfuscated`] ImageView",
            "TextView[text$=`广告`] +n FrameLayout[id=`com.baidu.tieba:id/obfuscated`] ImageView[id=null]",
            "TextView[text$=`广告`] < RelativeLayout <n LinearLayout - RelativeLayout ImageView[id=null][desc=null]"
          ]
        },
        {
          "key": 6,
          "name": "首页左侧游戏广告小图标",
          "activityIds": "com.baidu.tieba.tblauncher.MainTabActivity",
          "rules": [
            "ImageView[clickable=true] - RelativeLayout[clickable=false][childCount=1] > ImageView[clickable=true]"
          ]
        },
        {
          "key": 7,
          "name": "升级弹窗",
          "activityIds": "com.baidu.tieba.UpdateDialog",
          "rules": "[text=\"稍后再说\"]",
          "snapshotUrls": "https://gkd-kit.gitee.io/import/12496934"
        }
      ]
    },
    {
      "id": "com.baidu.wenku",
      "name": "百度文库",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": [
            "com.baidu.wenku.splash.view.activity.WelcomeActivity",
            "com.miui.home.launcher.Launcher"
          ],
          "rules": "[id=\"com.baidu.wenku:id/jump_second\"]",
          "snapshotUrls": [
            "https://gkd-kit.gitee.io/import/12520200",
            "https://gkd-kit.gitee.io/import/12520204"
          ]
        }
      ]
    },
    {
      "id": "com.baidutieba.davy",
      "name": "贴吧一键签到大师",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": [
            "com.baidutieba.SplashActivity",
            "com.miui.home.launcher.Launcher"
          ],
          "rules": "[id=\"com.baidutieba.davy:id/skipBt\"]",
          "snapshotUrls": "https://gkd-kit.gitee.io/import/12504282"
        },
        {
          "key": 1,
          "name": "内部弹窗广告",
          "activityIds": "com.davy.commonlibrary.utils.DialogUtil",
          "rules": [
            {
              "matches": "[id=\"com.baidutieba.davy:id/exit\"]",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/12504289"
            },
            {
              "matches": "[id=\"com.baidutieba.davy:id/mimo_interstitial_close_img\"]",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/12504291"
            }
          ]
        }
      ]
    },
    {
      "id": "com.bjsk.intelligent",
      "name": "WiFi智能钥匙",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.cssq.wifi.ui.splash.SplashActivity",
          "rules": [
            "[text^=`跳过`]",
            "[id=`com.byted.pangle:id/tt_splash_skip_btn`]"
          ]
        },
        {
          "key": 1,
          "name": "内部启动广告",
          "activityIds": "com.bytedance.sdk.openadsdk.stub.activity.Stub_Standard_Portrait_Activity",
          "rules": [
            "Image < @View +4 TextView[text=`反馈`] + View TextView[text=`广告`]"
          ]
        }
      ]
    },
    {
      "id": "com.cmcc.cmvideo",
      "name": "咪咕视频",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.cmcc.cmvideo.main.application.CompatibleMainActivity",
          "rules": "[id=`com.cmcc.cmvideo:id/skip_button`]"
        },
        {
          "key": 1,
          "name": "青少年模式弹窗",
          "activityIds": "com.cmcc.cmvideo.main.application.CompatibleMainActivity",
          "rules": "[id=\"com.cmcc.cmvideo:id/btn_cancle\"]",
          "snapshotUrls": "https://gkd-kit.gitee.io/import/12498307"
        },
        {
          "key": 2,
          "name": "右下角小广告",
          "activityIds": "com.cmcc.cmvideo.main.application.CompatibleMainActivity",
          "rules": "[id=\"com.cmcc.cmvideo:id/iv_right_bottom_close\"]",
          "snapshotUrls": "https://gkd-kit.gitee.io/import/12498315"
        }
      ]
    },
    {
      "id": "com.coolapk.market",
      "name": "酷安",
      "groups": [
        {
          "key": -1,
          "name": "开屏广告",
          "activityIds": [
            "com.coolapk.market.view.splash.SplashActivity",
            "com.coolapk.market.view.main.MainActivity"
          ],
          "rules": "[id$=\":id/tt_splash_skip_btn\"]",
          "snapshotUrls": [
            "https://gkd-kit.gitee.io/import/38517192/4ba30986-55d4-4a94-b7e2-6cf7d9c6d66d",
            "https://gkd-kit.gitee.io/import/12503773"
          ]
        },
        {
          "key": 0,
          "name": "关闭卡片广告",
          "desc": "点击卡片右上角按钮,然后点击关闭弹窗",
          "activityIds": [
            "com.coolapk.market.view.main.MainActivity",
            "com.coolapk.market.view.base.SimpleAlphaActivity"
          ],
          "rules": [
            {
              "activityIds": [
                "com.bytedance.sdk.openadsdk.core.dislike.ui",
                "com.coolapk.market.view.main.MainActivity",
                "com.coolapk.market.view.base.SimpleAlphaActivity"
              ],
              "snapshotUrls": "https://gkd-kit.gitee.io/import/38517192/9badc07c-4da2-4066-8af5-d96a86a28315",
              "matches": "@LinearLayout > TextView[id!=null][text=`不感兴趣`]"
            },
            "Button[text$=\"免广告\"] + Button[text=\"不感兴趣\"]",
            "Button[text$=`去广告`] - Button[text=`不感兴趣`]",
            "[id=`com.coolapk.market:id/close_view`]"
          ]
        },
        {
          "key": 1,
          "name": "关闭升级弹窗",
          "activityIds": "com.coolapk.market.view.main.MainActivity",
          "snapshotUrls": "https://gkd-kit.gitee.io/import/12503762",
          "rules": "[text=`立即更新`] - [text=`取消`]"
        }
      ]
    },
    {
      "id": "com.copymanga.app",
      "name": "拷貝漫畫",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": [
            "com.copymanga.app.MainActivity",
            "com.miui.home.launcher.Launcher",
            "com.reaper.flutter.reaper_flutter_plugin.activity.ReaperSplashActivity"
          ],
          "rules": [
            {
              "matches": "TextView[text!=null] - TextView[text^=\"跳过\"]",
              "snapshotUrls": [
                "https://gkd-kit.gitee.io/import/12504489",
                "https://gkd-kit.gitee.io/import/12504507"
              ]
            },
            {
              "matches": "ImageView + ViewGroup > TextView[text=\"跳过\"]",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/12504492"
            }
          ]
        },
        {
          "key": 1,
          "name": "内部弹窗广告",
          "activityIds": "com.copymanga.app.MainActivity",
          "rules": [
            {
              "activityIds": "com.kwad.components.ad.interstitial",
              "matches": "TextView[text=\"跳过\"]",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/12504486"
            },
            {
              "activityIds": "com.kwad.components.ad.interstitial",
              "matches": "ViewGroup[clickable=true] > ImageView",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/12504488"
            },
            {
              "matches": "ImageView < FrameLayout < FrameLayout +2 FrameLayout > ImageView",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/12504501"
            },
            {
              "matches": "ImageView + FrameLayout + FrameLayout > ImageView",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/12504520"
            }
          ]
        },
        {
          "key": 2,
          "name": "加入书架按钮下面的广告",
          "activityIds": "com.copymanga.app.MainActivity",
          "rules": {
            "matches": "ImageView[id=\"com.copymanga.app:id/close\"]",
            "snapshotUrls": "https://gkd-kit.gitee.io/import/12504525"
          }
        }
      ]
    },
    {
      "id": "com.cs_credit_bank",
      "name": "发现精彩",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.mapass.example.activity.MainActivity_",
          "rules": "[id=\"com.cs_credit_bank:id/start_skip\"]",
          "snapshotUrls": "https://gkd-kit.songe.li/import/12536487"
        }
      ]
    },
    {
      "id": "com.ct.client",
      "name": "中国电信",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": [
            "com.ct.client.activity.MainActivity",
            "com.ct.client.activity.SplashActivity"
          ],
          "rules": "[id=\"com.ct.client:id/tvSkip\"||id=\"com.ct.client:id/btSkip\"]",
          "snapshotUrls": [
            "https://gkd-kit.songe.li/import/12508958"
          ]
        },
        {
          "key": 1,
          "name": "用户引导",
          "enable": false,
          "activityIds": "com.ct.client.activity.UserGuideActivity",
          "rules": "[id=\"com.ct.client:id/tvSkip\"]",
          "snapshotUrls": [
            "https://gkd-kit.songe.li/import/12508971"
          ]
        }
      ]
    },
    {
      "id": "com.daimajia.gold",
      "name": "稀土掘金",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "im.juejin.android.ui.SplashActivity",
          "rules": "[id=`com.daimajia.gold:id/fl_skip`]"
        }
      ]
    },
    {
      "id": "com.dianping.v1",
      "name": "大众点评",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.dianping.v1.NovaMainActivity",
          "rules": "[id=`com.dianping.v1:id/new_skip`]"
        }
      ]
    },
    {
      "id": "com.douban.frodo",
      "name": "豆瓣",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": [
            "com.douban.frodo.activity.SplashActivity",
            "com.douban.frodo.splash.SplashActivityHot"
          ],
          "rules": "[id=\"com.douban.frodo:id/skip\"||text^=\"跳过\"]",
          "snapshotUrls": [
            "https://gkd-kit.gitee.io/import/12505151",
            "https://gkd-kit.gitee.io/import/12505152",
            "https://gkd-kit.gitee.io/import/12506164"
          ]
        },
        {
          "key": 1,
          "name": "不同步到我的动态",
          "desc": "标记看过时，不同步到我的动态",
          "enable": false,
          "activityIds": "com.douban.frodo.subject.activity.RatingActivity",
          "rules": "[id=\"com.douban.frodo:id/check_status\"][checked=true]",
          "snapshotUrls": [
            "https://gkd-kit.gitee.io/import/12508777"
          ]
        },
        {
          "key": 2,
          "name": "剧照广告",
          "activityIds": "com.douban.frodo.baseproject.image.SociableImageActivity",
          "rules": [
            {
              "matches": "TextView[id=\"com.douban.frodo:id/ad_not_interest\"][text=\"广告\"][visibleToUser=true]",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/12509475"
            },
            {
              "matches": "TextView[id=\"com.douban.frodo:id/mainText\"][text=\"不感兴趣\"]",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/12509476"
            }
          ]
        }
      ]
    },
    {
      "id": "com.dragon.read",
      "name": "番茄免费小说",
      "groups": [
        {
          "key": 0,
          "name": "阅读页面底部广告",
          "rules": [
            {
              "activityIds": "com.dragon.read.ad.banner.ui",
              "matches": "@[clickable=true] TextView[text=`关闭此条广告`]"
            },
            {
              "activityIds": "com.dragon.read.reader.ReaderActivity",
              "matches": "@ImageView - LinearLayout TextView[text=`广告`]"
            }
          ]
        }
      ]
    },
    {
      "id": "com.duokan.phone.remotecontroller",
      "name": "万能遥控",
      "groups": [
        {
          "key": 0,
          "name": "底部横幅广告",
          "activityIds": "com.xiaomi.mitv.phone.remotecontroller.HoriWidgetMainActivityV2",
          "rules": "ImageView[id=`com.duokan.phone.remotecontroller:id/image_close_banner`]"
        }
      ]
    },
    {
      "id": "com.duowan.kiwi",
      "name": "虎牙直播",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": [
            "com.duowan.kiwi.homepage.Homepage",
            "com.duowan.kiwi.adsplash.view.AdSplashActivity"
          ],
          "rules": [
            "[id=`com.duowan.kiwi:id/skip_time`]"
          ]
        },
        {
          "key": 1,
          "name": "青少年弹窗",
          "activityIds": [
            "com.duowan.kiwi.homepage.Homepage",
            "com.miui.home.launcher.Launcher"
          ],
          "rules": "[id=`com.duowan.kiwi:id/hyui_dialog_button_positive`][text=`我知道了`]"
        }
      ]
    },
    {
      "id": "com.estrongs.android.pop",
      "name": "ES文件浏览器",
      "groups": [
        {
          "key": 0,
          "name": "内部弹窗广告",
          "rules": [
            {
              "activityIds": "com.fighter.loader.view.InteractTemplateAdDialog",
              "matches": "[id=\"com.estrongs.android.pop:id/iv_close\"]",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/12509667"
            },
            {
              "activityIds": "com.estrongs.android.pop.view.FileExplorerActivity",
              "matches": "TextView[text!=null] < FrameLayout - ImageView - FrameLayout > ImageView",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/12509669"
            }
          ]
        }
      ]
    },
    {
      "id": "com.google.android.youtube",
      "name": "youtube",
      "groups": [
        {
          "key": 0,
          "name": "视频播放-跳过广告",
          "activityIds": "com.google.android.apps.youtube.app.watchwhile.WatchWhileActivity",
          "rules": "[id=`com.google.android.youtube:id/skip_ad_button`]"
        }
      ]
    },
    {
      "id": "com.gotokeep.keep",
      "name": "Keep",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.gotokeep.keep.splash.SplashActivity",
          "rules": "[id=`com.gotokeep.keep:id/textSkip`]"
        }
      ]
    },
    {
      "id": "com.greenpoint.android.mc10086.activity",
      "name": "中国移动",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.mc10086.cmcc.view.tabs.AppTabFragment",
          "rules": "[id=`com.greenpoint.android.mc10086.activity:id/video_time_skip`]"
        },
        {
          "key": 1,
          "name": "关闭更新弹窗",
          "activityIds": "com.mc10086.cmcc.view.tabs.AppTabFragment",
          "snapshotUrls": "https://gkd-kit.gitee.io/import/12534264",
          "rules": "Button[text=\"以后再说\"][id^=\"com.greenpoint.android.mc10086.activity:id/dialog_btn\"]"
        }
      ]
    },
    {
      "id": "com.handsgo.jiakao.android",
      "name": "驾考宝典",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.handsgo.jiakao.android.splash.Login",
          "rules": "[id=`com.handsgo.jiakao.android:id/closeLayout`]"
        }
      ]
    },
    {
      "id": "com.heytap.market",
      "name": "软件商店",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.heytap.cdo.client.cards.page.main.maintab.MainTabActivity",
          "rules": "[id=\"android:id/content\"] > RelativeLayout > LinearLayout > [text=\"跳过\"]",
          "snapshotUrls": "https://gkd-kit.gitee.io/import/12506561"
        }
      ]
    },
    {
      "id": "com.hunantv.imgo.activity",
      "name": "芒果TV",
      "groups": [
        {
          "key": -1,
          "name": "开屏广告",
          "activityIds": "com.hunantv.imgo.activity.MainActivity",
          "rules": [
            {
              "matches": "[id=\"com.hunantv.imgo.activity:id/layout_boot_skip\"]",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/38517192/7202bd0a-a5c6-4ec4-9547-bf4ca6d372d0"
            },
            {
              "matches": "TextView[text!=null] - [text^=\"跳过\"]",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/38517192/7202bd0a-a5c6-4ec4-9547-bf4ca6d372d0"
            }
          ]
        },
        {
          "key": 0,
          "name": "关闭青少年模式提示",
          "activityIds": [
            "com.hunantv.imgo.activity.MainActivity",
            "miuix.appcompat.app.m"
          ],
          "rules": "[id=`com.hunantv.imgo.activity:id/btnIknow`]"
        },
        {
          "key": 1,
          "name": "首页推荐流-卡片广告",
          "activityIds": "com.hunantv.imgo.activity.MainActivity",
          "rules": [
            {
              "matches": "[id=\"com.hunantv.imgo.activity:id/close_ad\"]",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/38517192/40fb71ad-01a5-4420-9150-88172ff8a3bf"
            },
            {
              "matches": "@[id=\"com.hunantv.imgo.activity:id/layout_logo\"] > [id=\"com.hunantv.imgo.activity:id/tv_ad_logo\"]",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/38517192/b74150b5-8e9f-4cbb-86a7-722fc739a1b8"
            }
          ]
        }
      ]
    },
    {
      "id": "com.hupu.games",
      "name": "虎扑",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "desc": "开屏广告,任意界面切回APP广告",
          "rules": "[id=\"com.byted.pangle:id/tt_splash_skip_btn\"]",
          "snapshotUrls": [
            "https://gkd-kit.gitee.io/import/12509060",
            "https://gkd-kit.gitee.io/import/12510962"
          ]
        },
        {
          "key": 1,
          "activityIds": "com.hupu.games.main.MainActivity",
          "name": "推荐流广告",
          "desc": "点击卡片右上角广告文字,出现广告反馈,点击屏蔽该广告",
          "rules": [
            {
              "activityIds": [
                "com.google.android.material.bottomsheet.BottomSheetDialog",
                "com.hupu.games.main.MainActivity"
              ],
              "matches": "[id=\"com.hupu.games:id/tv_title\"][text=\"屏蔽该广告\"]",
              "snapshotUrls": [
                "https://gkd-kit.gitee.io/import/12511010",
                "https://gkd-kit.gitee.io/import/12534848"
              ]
            },
            {
              "matches": "[id=\"com.hupu.games:id/tv_tag\"][text=\"广告\"]",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/12511005"
            }
          ]
        }
      ]
    },
    {
      "id": "com.hupu.shihuo",
      "name": "识货",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.shizhi.shihuoapp.module.main.ui.welcome.WelcomeActivity",
          "rules": "[id=`com.hupu.shihuo:id/fl_countdown`]"
        }
      ]
    },
    {
      "id": "com.hxak.liangongbao",
      "name": "链工宝",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.hxak.liangongbao.login.ui.HomeActivity",
          "rules": "[id=`com.hxak.liangongbao:id/time_down`]"
        }
      ]
    },
    {
      "id": "com.icbc",
      "name": "中国工商银行",
      "groups": [
        {
          "key": 0,
          "name": "第一次启动提示",
          "activityIds": "com.icbc.activity.init.SplashActivity",
          "rules": "[id=`com.icbc:id/close_btn`]"
        }
      ]
    },
    {
      "id": "com.intsig.camscanner",
      "name": "扫描全能王",
      "groups": [
        {
          "key": 0,
          "name": "开屏vip提示",
          "activityIds": "com.intsig.camscanner.guide.guidevideo.GuideVideoActivity",
          "rules": "[id=`com.intsig.camscanner:id/tv_drop_cnl_close_new`]"
        }
      ]
    },
    {
      "id": "com.iqiyi.hotchat",
      "name": "爱奇艺热聊",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.iqiyi.hotchat.ui.activity.AdvertisementActivity",
          "rules": "[id=`com.iqiyi.hotchat:id/tv_advertisement_lunch_skip`]"
        }
      ]
    },
    {
      "id": "com.jdcloud.mt.smartrouter",
      "name": "京东云无线宝",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.jdcloud.mt.smartrouter.nwelcome.WelcomeActivity",
          "rules": "LinearLayout > TextView[text^=\"跳过\"]",
          "snapshotUrls": "https://gkd-kit.songe.li/import/12535237"
        }
      ]
    },
    {
      "id": "com.jingdong.app.mall",
      "name": "京东",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.jingdong.app.mall.MainFrameActivity",
          "rules": "[desc$=\"广告\"] +2 [desc=\"跳过\"] > [text=\"跳过\"]",
          "snapshotUrls": "https://gkd-kit.gitee.io/import/12519430"
        }
      ]
    },
    {
      "id": "com.jym.mall",
      "name": "交易猫",
      "groups": [
        {
          "key": 0,
          "name": "升级弹窗",
          "rules": "[id=\"com.jym.mall:id/tv_cancel\"][text=\"下次再说\"]",
          "snapshotUrls": "https://gkd-kit.gitee.io/import/12496974"
        }
      ]
    },
    {
      "id": "com.kmxs.reader",
      "name": "七猫免费小说",
      "groups": [
        {
          "key": 0,
          "name": "关闭青少年模式",
          "activityIds": "com.kmxs.reader.home.ui.HomeActivity",
          "rules": "[id=`com.kmxs.reader:id/young_dialog_close`]"
        }
      ]
    },
    {
      "id": "com.koudai.weidian.buyer",
      "name": "微店",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.koudai.weidian.buyer.activity.SplashActivity",
          "rules": "[id=\"com.koudai.weidian.buyer:id/skip_view\"||text=\"跳过\"]",
          "snapshotUrls": "https://gkd-kit.songe.li/import/12506297"
        }
      ]
    },
    {
      "id": "com.kuaikan.comic",
      "name": "快看",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.kuaikan.comic.ui.AdvertisementActivity",
          "rules": "[id=`com.kuaikan.comic:id/skip_button`]"
        }
      ]
    },
    {
      "id": "com.kuaishou.nebula",
      "name": "快手极速版",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.yxcorp.gifshow.HomeActivity",
          "rules": "[id=\"com.kuaishou.nebula:id/splash_skip_text\"]",
          "snapshotUrls": "https://gkd-kit.gitee.io/import/12519389"
        }
      ]
    },
    {
      "id": "com.kugou.android",
      "name": "酷狗音乐",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.kugou.android.app.splash.SplashActivity",
          "rules": "[desc=`跳过`]"
        }
      ]
    },
    {
      "id": "com.kwai.videoeditor",
      "name": "快影",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.kwai.videoeditor.activity.splash.InnerVideoSplashActivity",
          "rules": [
            "Button[text=\"跳过\"]"
          ],
          "snapshotUrls": "https://gkd-kit.gitee.io/import/38517192/d12c3b08-8233-4584-b2b9-595ebb4ce665"
        }
      ]
    },
    {
      "id": "com.lucky.luckyclient",
      "name": "瑞幸咖啡",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.luckin.client.main.FirstActivity",
          "rules": "[id=\"com.lucky.luckyclient:id/tv_skip\"]",
          "snapshotUrls": "https://gkd-kit.songe.li/import/12508764"
        }
      ]
    },
    {
      "id": "com.luna.music",
      "name": "汽水音乐",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.luna.biz.ad.AdActivity",
          "rules": "[id$=\"/tt_splash_skip_btn\"]",
          "snapshotUrls": "https://gkd-kit.gitee.io/import/12514049"
        }
      ]
    },
    {
      "id": "com.miaoying.appmy.cs",
      "name": "新小财神影视",
      "groups": [
        {
          "key": -1,
          "name": "关闭公告栏",
          "desc": "APP启动时出现的公告栏",
          "activityIds": [
            "com.miaoying.appmy.cs.MainActivity",
            "com.miui.home.launcher.Launcher"
          ],
          "rules": "@[desc=\"我知道了\"] + [desc=\"了解更多\"]",
          "snapshotUrls": "https://gkd-kit.gitee.io/import/12522872"
        }
      ]
    },
    {
      "id": "com.mihoyo.hyperion",
      "name": "米游社",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": [
            "com.mihoyo.hyperion.ui.SplashActivity",
            "com.mihoyo.hyperion.splash.SplashActivity"
          ],
          "rules": "[id=`com.mihoyo.hyperion:id/mSplashBtJump`]",
          "snapshotUrls": "https://gkd-kit.gitee.io/import/12482738"
        },
        {
          "key": 1,
          "name": "青少年模式",
          "desc": "关闭青少年模式提醒弹窗",
          "rules": "TextView[id=`com.mihoyo.hyperion:id/tv_dialog_i_know`]"
        }
      ]
    },
    {
      "id": "com.miui.player",
      "name": "小米音乐",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.tencent.qqmusiclite.activity.MainActivity",
          "rules": "@TextView[text$=`跳过`] + TextView[id=`com.miui.player:id/ad_view`]"
        }
      ]
    },
    {
      "id": "com.miui.systemAdSolution",
      "name": "miui系统广告",
      "groups": [
        {
          "key": 0,
          "name": "任意app开屏广告",
          "desc": "此广告组件可以使用ADB卸载",
          "rules": "[id=`com.miui.systemAdSolution:id/view_skip_button`]"
        },
        {
          "key": 1,
          "name": "miui-为什么不希望看到这条推广",
          "desc": "关闭这个提示",
          "activityIds": "com.xiaomi.ad.feedback",
          "rules": "[id=`com.miui.systemAdSolution:id/no_interest`]"
        }
      ]
    },
    {
      "id": "com.mt.mtxx.mtxx",
      "name": "美图秀秀",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.meitu.business.ads.core.activity.AdActivity",
          "rules": "[text=`跳过广告`]",
          "snapshotUrls": "https://gkd-kit.gitee.io/import/38517192/1f56aa17-c290-4e56-b6fb-a94bc778448b"
        }
      ]
    },
    {
      "id": "com.netease.cloudmusic",
      "name": "网易云音乐",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.netease.cloudmusic.activity.MainActivity",
          "rules": "TextView[text^=`跳过`][id=`com.netease.cloudmusic:id/skipBtn`]"
        },
        {
          "key": 1,
          "name": "广告卡片",
          "rules": [
            {
              "activityIds": "com.netease.cloudmusic.module.ad.feedback.AdFeedbackBottomSheet",
              "matches": "[text=\"直接关闭\"]",
              "snapshotUrls": [
                "https://gkd-kit.songe.li/import/38517192/fea3449b-d642-4d75-929f-490421cc9080"
              ]
            },
            {
              "activityIds": "com.netease.cloudmusic.activity.MainActivity",
              "matches": "[id=\"com.netease.cloudmusic:id/adTagClose\"]",
              "snapshotUrls": "https://gkd-kit.songe.li/import/38517192/a977b19d-2b3c-43df-ba01-63e7cbbb3908"
            }
          ]
        }
      ]
    },
    {
      "id": "com.njh.biubiu",
      "name": "biubiu加速器",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.njh.ping.business.base.activity.BusinessActivity",
          "rules": [
            {
              "matches": "[text=\"跳过\"]",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/12512845"
            }
          ]
        }
      ]
    },
    {
      "id": "com.qidian.QDReader",
      "name": "起点读书",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": [
            "com.qidian.QDReader.ui.activity.SplashADActivity",
            "com.qidian.QDReader.ui.activity.SplashImageActivity"
          ],
          "rules": "Button[text^=`跳过`]",
          "snapshotUrls": [
            "https://gkd-kit.gitee.io/import/12508836"
          ]
        }
      ]
    },
    {
      "id": "com.qiyi.video",
      "name": "爱奇艺",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "org.qiyi.android.video.MainActivity",
          "rules": "@FrameLayout[id=`com.qiyi.video:id/unused_res_a`] > LinearLayout[id=null] > TextView[text=`关闭`][id=`com.qiyi.video:id/unused_res_a`]"
        },
        {
          "key": 1,
          "name": "青少年弹窗",
          "activityIds": "org.qiyi.basecore.widget.dialog.AlertDialogBottom1",
          "rules": "Button[id=`com.qiyi.video:id/confirm_btn`][text=`我知道了`]"
        },
        {
          "key": 2,
          "name": "我的-顶部广告",
          "activityIds": "org.qiyi.android.video.MainActivity",
          "snapshotUrls": "https://gkd-kit.gitee.io/import/12495050",
          "rules": [
            "[id=\"com.qiyi.video:id/unused_res_a\"] > [id=\"com.qiyi.video:id/close\"]"
          ]
        }
      ]
    },
    {
      "id": "com.quark.browser",
      "name": "夸克浏览器",
      "groups": [
        {
          "key": 0,
          "name": "小说阅读页面底部广告",
          "activityIds": "com.ucpro.BrowserActivity",
          "rules": [
            "[id=`com.quark.browser:id/tv_close_ad`][text=`关闭广告`]",
            "[id=`com.quark.browser:id/ad_close_layout_container`]"
          ]
        }
      ]
    },
    {
      "id": "com.sankuai.meituan",
      "name": "美团",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.meituan.android.pt.homepage.activity.MainActivity",
          "rules": "TextView[id=`com.sankuai.meituan:id/close_btn`][text^=`跳过`]"
        }
      ]
    },
    {
      "id": "com.sankuai.meituan.takeoutnew",
      "name": "美团外卖",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.sankuai.meituan.takeoutnew.ui.page.boot.SplashAdActivity",
          "rules": "TextView[text*=`跳过`]"
        },
        {
          "key": 1,
          "name": "关闭更新弹窗",
          "activityIds": "com.sankuai.waimai.business.page.homepage.widget.dialog.UpdateForceInstallDialog",
          "rules": [
            "[id='com.sankuai.meituan.takeoutnew:id/wm_upgrade_force_cancel']"
          ]
        },
        {
          "key": 2,
          "name": "关闭美食广告弹窗",
          "activityIds": "com.sankuai.waimai.platform.mach.dialog.DynamicDialog",
          "rules": [
            "@[desc='关闭'][clickable=true] > ImageView"
          ]
        }
      ]
    },
    {
      "id": "com.sdu.didi.psnger",
      "name": "滴滴",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.didi.sdk.app.launch.splash.SplashActivity",
          "rules": "[id=`com.sdu.didi.psnger:id/skip_ad_ll`]"
        }
      ]
    },
    {
      "id": "com.shark.jizhang",
      "name": "鲨鱼记账",
      "groups": [
        {
          "key": 0,
          "name": "新用户特惠广告",
          "desc": "弹窗广告,右下角浮动广告",
          "activityIds": "com.shark.jizhang.module.main.MainActivity",
          "rules": [
            {
              "matches": "[id=\"com.shark.jizhang:id/buy_later_view\"||id=\"com.shark.jizhang:id/tv_count_down\"] - [id=\"com.shark.jizhang:id/close_view\"]",
              "snapshotUrls": [
                "https://gkd-kit.gitee.io/import/12518500",
                "https://gkd-kit.gitee.io/import/12518517"
              ]
            }
          ]
        }
      ]
    },
    {
      "id": "com.shuqi.controller",
      "name": "书旗小说",
      "groups": [
        {
          "key": 0,
          "name": "内部右侧浮动广告",
          "activityIds": "com.shuqi.home.MainActivity",
          "rules": "[id=\"com.shuqi.controller:id/promotion_close\"]",
          "snapshotUrls": "https://gkd-kit.gitee.io/import/12513811"
        },
        {
          "key": 1,
          "name": "关闭打卡红包弹窗",
          "activityIds": "com.shuqi.common",
          "rules": "[id=\"com.shuqi.controller:id/bottomCloseImg\"]",
          "snapshotUrls": "https://gkd-kit.gitee.io/import/12513822"
        },
        {
          "key": 2,
          "name": "阅读页面底部广告",
          "desc": "点击关闭x图标-关闭优惠券弹窗-关闭当前广告",
          "rules": [
            {
              "activityIds": "com.shuqi.android.ui.dialog",
              "matches": "[id=\"com.shuqi.controller:id/right_close_ad_text\"]",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/12513893"
            },
            {
              "activityIds": "com.shuqi.monthlypay.view",
              "matches": [
                "[text*=\"优惠券\"]",
                "[id=\"com.shuqi.controller:id/close_btn\"]"
              ],
              "snapshotUrls": "https://gkd-kit.gitee.io/import/12513908"
            },
            {
              "activityIds": "com.shuqi.reader.ShuqiReaderActivity",
              "matches": "@ImageView[clickable=true] - RelativeLayout [id=\"com.shuqi.controller:id/noah_tv_stencil_native_source\"]",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/12513860"
            }
          ]
        },
        {
          "key": 3,
          "name": "听书页面底部广告",
          "desc": "点击卡片右上角关闭按钮-点击底部中间<关闭当前广告>",
          "activityIds": "com.shuqi.audio.online.view.AudioBookActivity",
          "rules": [
            {
              "matches": "[id=\"com.shuqi.controller:id/remove_current_ad\"]",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/12513959"
            },
            {
              "matches": "[id=\"com.shuqi.controller:id/ad_close_but\"]",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/12513944"
            }
          ]
        }
      ]
    },
    {
      "id": "com.sina.weibo",
      "name": "微博",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.sina.weibo.mobileads.view.",
          "rules": [
            "@RelativeLayout > TextView[text=`跳过`]"
          ]
        },
        {
          "key": 1,
          "name": "评论区顶部-相关推荐",
          "activityIds": "com.sina.weibo.feed.DetailWeiboActivity",
          "rules": "ImageView[id=`com.sina.weibo:id/iv_ad_x`]"
        },
        {
          "key": 2,
          "name": "关闭不感兴趣广告弹窗",
          "activityIds": "com.sina.weibo.view.bottomsheet.dialog.",
          "rules": {
            "matches": [
              "[text=\"为何会看到此广告\"]",
              "[text=\"不感兴趣\"]"
            ]
          }
        },
        {
          "key": 3,
          "name": "兴趣领域推荐",
          "desc": "出现在长久未登录的账户再次登录时",
          "activityIds": "com.sina.weibo.account.interest.InterestActivity",
          "rules": "[id=\"com.sina.weibo:id/rl_account_title_bar\"] > [id=\"com.sina.weibo:id/tv_title_bar_skip\"&&text=\"跳过\"]",
          "snapshotUrls": "https://gkd-kit.songe.li/import/12531405"
        },
        {
          "key": 4,
          "name": "精选博主推荐",
          "desc": "出现在长久未登录的账户再次登录时",
          "activityIds": "com.sina.weibo.account.recommend.RecommendActivity",
          "rules": [
            "[id=\"com.sina.weibo:id/tv_option\"&&text=\"取消勾选\"]",
            "[id=\"com.sina.weibo:id/new_next_btn\"&&text=\"进入微博（已选0个）\"]"
          ],
          "snapshotUrls": [
            "https://gkd-kit.songe.li/import/12531433",
            "https://gkd-kit.songe.li/import/12531434"
          ]
        }
      ]
    },
    {
      "id": "com.sinovatech.unicom.ui",
      "name": "中国联通",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.sinovatech.unicom.basic.ui.activity.WelcomeClient",
          "rules": "[id=\"com.sinovatech.unicom.ui:id/welcome_advertise_close\"]",
          "snapshotUrls": "https://gkd-kit.songe.li/import/12535185"
        }
      ]
    },
    {
      "id": "com.smile.gifmaker",
      "name": "快手",
      "groups": [
        {
          "key": 0,
          "name": "关闭青少年弹窗",
          "activityIds": "com.yxcorp.gifshow.HomeActivity",
          "rules": "@[id=`com.smile.gifmaker:id/positive`] + [id=`com.smile.gifmaker:id/set_teenage_mode`]"
        }
      ]
    },
    {
      "id": "com.smzdm.client.android",
      "name": "什么值得买",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.smzdm.client.android.app.WelComeActivity",
          "rules": "[id=\"com.smzdm.client.android:id/tv_skip\"]",
          "snapshotUrls": "https://gkd-kit.songe.li/import/12535072"
        }
      ]
    },
    {
      "id": "com.snda.wifilocating",
      "name": "WiFi万能钥匙",
      "groups": [
        {
          "key": -1,
          "name": "开屏广告",
          "activityIds": "com.lantern.launcher.ui.MainActivity",
          "snapshotUrls": "https://gkd-kit.gitee.io/import/38517192/4d6fdd1e-28ec-4b61-86e2-641b7b5b8899",
          "rules": [
            "TextView[text=\"广告\"] -3 RelativeLayout > TextView[text*=\"跳过\"]"
          ]
        },
        {
          "key": 0,
          "name": "内部广告",
          "activityIds": "com.lantern.launcher.ui.MainActivityICS",
          "rules": [
            {
              "matches": [
                "[id=`com.snda.wifilocating:id/outer_ad_dislike_item_title`][text=`为什么看到此广告`]",
                "@[id=`com.snda.wifilocating:id/outer_ad_dislike_item_one`] [id=`com.snda.wifilocating:id/outer_ad_dislike_item_title`][text=`不感兴趣`]"
              ]
            },
            "ImageView[id=`com.snda.wifilocating:id/feed_item_sdk_logo`] < LinearLayout + [id=`com.snda.wifilocating:id/feed_item_dislike`]"
          ]
        }
      ]
    },
    {
      "id": "com.ss.android.article.video",
      "name": "西瓜视频",
      "groups": [
        {
          "key": 0,
          "name": "西瓜视频-关闭青少年模式弹窗",
          "activityIds": "com.ixigua.commonui.uikit.dialog.XGAlertDialog",
          "snapshotUrls": [
            "https://gkd-kit.gitee.io/import/38517192/78f0c1f6-e8da-4bc4-acd3-5e6dc056b044"
          ],
          "rules": [
            "TextView[text=\"我知道了\"][clickable=true]"
          ]
        }
      ]
    },
    {
      "id": "com.ss.android.ugc.aweme",
      "name": "抖音",
      "groups": [
        {
          "key": 0,
          "name": "关闭青少年弹窗",
          "rules": "Button[text=`开启青少年模式`] + * > Button[text!=null]"
        },
        {
          "key": 1,
          "name": "关闭用户推荐",
          "rules": [
            {
              "activityIds": "com.google.android.material.bottomsheet.BottomSheetDialog",
              "matches": "[id=\"com.ss.android.ugc.aweme:id/desc\"][text=\"减少此类推荐\"]",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/12520962"
            },
            {
              "activityIds": "com.ss.android.ugc.aweme.main.MainActivity",
              "matches": "[text=\"换一个\"] - FrameLayout[clickable=true] > ImageView[clickable=true]",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/12520943"
            }
          ]
        },
        {
          "key": 2,
          "activityIds": [
            "com.ss.android.ugc.aweme.main.MainActivity",
            "com.miui.home.launcher.Launcher"
          ],
          "name": "关闭朋友推荐弹窗",
          "rules": "[text=\"朋友推荐\"] +2 [id=\"com.ss.android.ugc.aweme:id/close\"]",
          "snapshotUrls": [
            "https://gkd-kit.gitee.io/import/12525387",
            "https://gkd-kit.gitee.io/import/12525389"
          ]
        },
        {
          "key": 3,
          "name": "关闭更新弹窗",
          "activityIds": "com.ss.android.ugc.aweme.main.MainActivity",
          "rules": "@[text=\"以后再说\"] +2 [text=\"立即升级\"]",
          "snapshotUrls": "https://gkd-kit.gitee.io/import/12534016"
        }
      ]
    },
    {
      "id": "com.taobao.taobao",
      "name": "淘宝",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.taobao.bootimage.activity.BootImageActivity",
          "rules": "[id='com.taobao.taobao:id/close']"
        }
      ]
    },
    {
      "id": "com.tencent.androidqqmail",
      "name": "qq邮箱",
      "groups": [
        {
          "key": 0,
          "name": "广告邮件-列表卡片广告",
          "activityIds": "com.tencent.qqmail.fragment.base.MailFragmentActivity",
          "rules": [
            "TextView[text=`赞助商提供的广告`] <n FrameLayout <n ListView[id=`com.tencent.androidqqmail:id/pop_up_list`] TextView[text=`不感兴趣`]",
            "[id=`com.tencent.androidqqmail:id/advertise_view_ad`]"
          ]
        }
      ]
    },
    {
      "id": "com.tencent.djcity",
      "name": "掌上道聚城",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.tencent.djcity.activities.homepage.PortalActivity",
          "rules": "[id=`com.tencent.djcity:id/ad_view_ll_skip`]"
        }
      ]
    },
    {
      "id": "com.tencent.karaoke",
      "name": "全民K歌",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.tencent.karaoke.module.splash.ui.SplashAdDialog",
          "rules": "[text*=`跳过`][id!=null]"
        }
      ]
    },
    {
      "id": "com.tencent.mm",
      "name": "微信",
      "groups": [
        {
          "key": 0,
          "name": "关闭朋友圈广告",
          "desc": "朋友圈信息流广告,点击关闭按钮,确认关闭",
          "activityIds": "com.tencent.mm.plugin.sns.ui.SnsTimeLineUI",
          "exampleUrls": [
            "https://github.com/gkd-kit/subscription/assets/38517192/c9ae4bba-a748-4755-b5e4-c7ad3d489a79"
          ],
          "rules": [
            "TextView[text*=\"广告\"] + TextView[text=\"关闭该广告\"]",
            "ImageView - TextView[text=\"广告\"][id!=null][index=0]"
          ]
        },
        {
          "key": 1,
          "name": "电脑微信快捷自动登录",
          "activityIds": ".plugin.webwx.ui.ExtDeviceWXLoginUI",
          "rules": "TextView[text=\"取消登录\"] - Button[text=\"登录\"]"
        },
        {
          "key": 2,
          "name": "浏览器扫码微信登录自动授权",
          "activityIds": [
            "com.tencent.mm.plugin.webview.ui.tools.SDKOAuthUI"
          ],
          "rules": "Button[text=\"拒绝\"] - Button[text=\"允许\"]"
        },
        {
          "key": 3,
          "name": "微信手机第三方APP申请使用",
          "desc": "自动点击同意",
          "rules": [
            "TextView + TextView[text=\"申请使用\"]",
            "Button[text=\"拒绝\"] - Button[text=\"允许\"]"
          ]
        },
        {
          "key": 4,
          "name": "微信读书网页版扫码登录自动授权",
          "activityIds": [
            "com.tencent.mm.plugin.webview.ui.tools.MMWebViewUI"
          ],
          "rules": [
            {
              "matches": "Button[text=\"登 录\"]",
              "snapshotUrls": "https://gkd-kit.songe.li/import/12506197"
            },
            {
              "matches": [
                "[text=\"登录成功\"]",
                "[id=\"com.tencent.mm:id/g1\"][desc=\"返回\"]"
              ],
              "snapshotUrls": "https://gkd-kit.songe.li/import/12506201"
            }
          ]
        }
      ]
    },
    {
      "id": "com.tencent.mobileqq",
      "name": "QQ",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.tencent.mobileqq.activity.SplashActivity",
          "rules": "[text*=`跳过`]"
        },
        {
          "key": 1,
          "name": "消息页面-顶部广告",
          "activityIds": "com.tencent.mobileqq.activity.SplashActivity",
          "rules": [
            "ImageView[id!=null][desc='关闭'][clickable=true]"
          ]
        },
        {
          "key": 2,
          "name": "好友动态-广告卡片",
          "rules": [
            {
              "activityIds": "com.tencent.qqlive.module.videoreport.inject.dialog.ReportDialog",
              "matches": "[clickable=true] > ImageView + TextView[text=\"关闭此条广告\"]"
            },
            {
              "activityIds": "com.qzone.reborn.feedx.activity.QZoneFriendFeedXActivity",
              "matches": "View[desc=\"广告\"] + ImageView[clickable=true]"
            }
          ]
        }
      ]
    },
    {
      "id": "com.tencent.mtt",
      "name": "QQ浏览器",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.tencent.mtt.MainActivity",
          "rules": [
            "@View[id=null] + ImageView + FrameLayout TextView[text=`向上滑动或点击查看`]",
            {
              "matches": "@LinearLayout[clickable=true] > TextView[text=\"跳过\"]",
              "snapshotUrls": [
                "https://gkd-kit.gitee.io/import/38517192/7d8e9661-c29a-4448-94c2-d7b0a1756107"
              ]
            }
          ]
        }
      ]
    },
    {
      "id": "com.tencent.qqlive",
      "name": "腾讯视频",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.tencent.qqlive.ona.activity.SplashHomeActivity",
          "rules": [
            "TextView[text*=`互动广告`] < LinearLayout < FrameLayout + FrameLayout > TextView[text=`跳过`]",
            "TextView[text=`广告`] LinearLayout + TextView[text=`跳过`]"
          ]
        },
        {
          "key": 1,
          "name": "关闭青少年弹窗",
          "activityIds": "com.tencent.qqlive.ona.update.trunk.client.TrunkUpdateActivity",
          "rules": "TextView[text*=`青少年模式`] +n TextView[id=`com.tencent.qqlive:id/arg`][text=`我知道了`]"
        }
      ]
    },
    {
      "id": "com.tencent.qqmusic",
      "name": "QQ音乐",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": [
            "com.tencent.qqmusic.activity.AppStarterActivity",
            "com.tencent.qqmusic.business.splash.thirdpartsplash.tme.union.SplashDialog"
          ],
          "rules": "TextView[text=`跳过`][clickable=true]"
        },
        {
          "key": 1,
          "name": "推荐页-广告卡片",
          "activityIds": "com.tencent.qqmusic.activity.AppStarterActivity",
          "rules": [
            "@LinearLayout[clickable=true] > TextView[text='广告'] + ImageView",
            "TextView[text=\"广告 | 关闭\"][clickable=true]"
          ]
        }
      ]
    },
    {
      "id": "com.tencent.qt.sns",
      "name": "掌上穿越火线",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.tencent.gamehelper.ui.main.WelcomeActivity",
          "rules": "[id=`com.tencent.qt.sns:id/tv_timer`][text$=`跳过`]"
        }
      ]
    },
    {
      "id": "com.weico.international",
      "name": "微博轻享版",
      "groups": [
        {
          "key": -1,
          "name": "开屏广告",
          "activityIds": "com.weico.international.ui.ad.AdActivity",
          "rules": "TextView[text*=\"跳过\"]",
          "snapshotUrls": [
            "https://gkd-kit.gitee.io/import/12509123",
            "https://gkd-kit.gitee.io/import/12510132"
          ]
        },
        {
          "key": 0,
          "name": "主页-推荐流广告",
          "activityIds": "com.weico.international.activity.MainFragmentActivity",
          "exampleUrls": "https://github.com/gkd-kit/subscription/assets/38517192/e713a2ca-5048-486a-874f-dd876d53c49b",
          "rules": [
            {
              "activityIds": "com.google.android.material.bottomsheet.BottomSheetDialog",
              "matches": "@View > [text=\"不感兴趣\"]",
              "snapshotUrls": [
                "https://gkd-kit.gitee.io/import/12505755",
                "https://gkd-kit.gitee.io/import/12505764"
              ]
            },
            {
              "matches": "[id=\"com.weico.international:id/item_timeline_ad_action\"]",
              "snapshotUrls": [
                "https://gkd-kit.gitee.io/import/12505753",
                "https://gkd-kit.gitee.io/import/12505763"
              ]
            }
          ]
        }
      ]
    },
    {
      "id": "com.xiachufang",
      "name": "下厨房",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": [
            "com.xiachufang.startpage.ui.StartPageActivity"
          ],
          "rules": "[id$=\"/tt_splash_skip_btn\"||id$=\"/start_page_count_down_tv\"||text$=\"跳过\"]",
          "snapshotUrls": [
            "https://gkd-kit.songe.li/import/12505985",
            "https://gkd-kit.songe.li/import/12506014",
            "https://gkd-kit.songe.li/import/12506041"
          ]
        }
      ]
    },
    {
      "id": "com.xiaomi.market",
      "name": "小米应用商店",
      "groups": [
        {
          "key": 0,
          "name": "首页悬浮窗广告",
          "activityIds": "com.xiaomi.market.ui.FloatWebActivity",
          "rules": "Button[text='关闭']"
        }
      ]
    },
    {
      "id": "com.xiaomi.shop",
      "name": "小米商城",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.xiaomi.shop.activity.MainTabActivity",
          "rules": "[id=\"com.xiaomi.shop:id/skip\"]",
          "snapshotUrls": [
            "https://gkd-kit.gitee.io/import/38517192/9083b291-43f8-4d92-a506-a9dc6ed0156f"
          ]
        }
      ]
    },
    {
      "id": "com.ximalaya.ting.android",
      "name": "喜马拉雅",
      "groups": [
        {
          "key": -1,
          "name": "开屏广告",
          "activityIds": [
            "com.ximalaya.ting.android.host.activity.MainActivity",
            "com.ximalaya.ting.android.host.activity.SplashAdActivity"
          ],
          "rules": [
            {
              "matches": "[id=\"com.ximalaya.ting.android:id/xm_ad_host_count_down_click_lay\"]",
              "snapshotUrls": [
                "https://gkd-kit.gitee.io/import/12506207",
                "https://gkd-kit.gitee.io/import/12506273"
              ]
            }
          ]
        },
        {
          "key": 0,
          "name": "首页右侧浮动广告",
          "activityIds": "com.ximalaya.ting.android.host.activity.MainActivity",
          "rules": "[id=\"com.ximalaya.ting.android:id/main_ad_broadside_close_real\"]",
          "snapshotUrls": [
            "https://gkd-kit.gitee.io/import/38517192/45664dfb-b8e6-4bdb-b5bb-9852c7a86a2f"
          ]
        },
        {
          "key": 1,
          "name": "播放页面-暂停按钮下面的广告",
          "activityIds": "com.ximalaya.ting.android.host.activity.MainActivity",
          "rules": "[id=\"com.ximalaya.ting.android:id/x_play_ad_banner_close_real\"]",
          "snapshotUrls": "https://gkd-kit.gitee.io/import/12506218"
        },
        {
          "key": 2,
          "name": "播放页面-底部推荐列表-夹杂广告",
          "desc": "点击关闭-点击屏蔽",
          "rules": [
            {
              "activityIds": "com.ximalaya.ting.android.main.dialog",
              "matches": "@[clickable=true] > [text=\"屏蔽\"] + [text=\"关闭当前广告\"]",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/12506269"
            },
            {
              "activityIds": "com.ximalaya.ting.android.host.activity.MainActivity",
              "matches": "[id=\"com.ximalaya.ting.android:id/main_close\"]",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/12506225"
            }
          ]
        },
        {
          "key": 3,
          "name": "播放页面-播放前广告",
          "activityIds": [
            "com.ximalaya.ting.android.host.activity.MainActivity",
            "com.ximalaya.ting.android.framework.view.dialog"
          ],
          "rules": "[id=\"com.ximalaya.ting.android:id/main_play_ad_close_real\"]",
          "snapshotUrls": [
            "https://gkd-kit.gitee.io/import/12506250",
            "https://gkd-kit.gitee.io/import/12520626"
          ]
        },
        {
          "key": 4,
          "name": "首页-推荐列表广告",
          "desc": "点击关闭-点击屏蔽",
          "rules": [
            {
              "activityIds": "com.ximalaya.ting.android.adsdk.view.DislikeDialog.DislikeBottomDialog",
              "matches": "[id=\"com.ximalaya.ting.android:id/xm_ad_main_ad_dislike_shield\"]",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/12506258"
            },
            {
              "activityIds": "com.ximalaya.ting.android.host.activity.MainActivity",
              "matches": "[id=\"com.ximalaya.ting.android:id/xm_ad_close_real\"]",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/12506253"
            }
          ]
        },
        {
          "key": 5,
          "name": "关闭热播推荐广告",
          "activityIds": "com.ximalaya.ting.android.host.activity.MainActivity",
          "rules": [
            {
              "matches": "[text=\"热播推荐\"] + ImageView + ImageView",
              "snapshotUrls": "https://gkd-kit.gitee.io/import/12506270"
            }
          ]
        },
        {
          "key": 6,
          "name": "关闭更新弹窗",
          "rules": "[id=\"com.ximalaya.ting.android:id/host_tv_update_later\"]",
          "snapshotUrls": "https://gkd-kit.gitee.io/import/12506287"
        },
        {
          "key": 7,
          "name": "关闭青少年模式弹窗",
          "activityIds": "com.ximalaya.ting.android.host.activity.MainActivity",
          "snapshotUrls": "https://gkd-kit.gitee.io/import/12506209",
          "rules": {
            "matches": [
              "[text*=\"青少年模式\"][id=\"com.ximalaya.ting.android:id/host_btn_set\"]",
              "[id=\"com.ximalaya.ting.android:id/host_dialog_close\"]"
            ]
          }
        }
      ]
    },
    {
      "id": "com.ximalaya.ting.lite",
      "name": "喜马拉雅极速版",
      "groups": [
        {
          "key": 1,
          "name": "开屏广告",
          "activityIds": "com.ximalaya.ting.android.host.activity.WelComeActivity",
          "rules": [
            "[id=\"com.ximalaya.ting.lite:id/host_common_time_countdown_text_view\"]"
          ]
        },
        {
          "key": 0,
          "name": "首页-推荐-卡片广告",
          "activityIds": "com.ximalaya.ting.android.host.activity.MainActivity",
          "rules": "[id='com.ximalaya.ting.lite:id/main_ad_top_home_iv_close']"
        }
      ]
    },
    {
      "id": "com.xunlei.downloadprovider",
      "name": "迅雷",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.xunlei.downloadprovider.launch.LaunchActivity",
          "rules": "TextView[text^=`跳过`]"
        }
      ]
    },
    {
      "id": "com.yek.android.kfc.activitys",
      "name": "肯德基",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.yum.android.superkfc.ui.v5.HomeV5Activity",
          "rules": "[id=`com.yek.android.kfc.activitys:id/splash_tv_3`]"
        }
      ]
    },
    {
      "id": "com.yipiao",
      "name": "智行火车票12306抢票",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.app.main.entrance.MainActivity",
          "rules": "LinearLayout > TextView + TextView[text=`跳过`]"
        }
      ]
    },
    {
      "id": "com.zhihu.android",
      "name": "知乎",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": [
            "com.zhihu.android.app.ui.activity.LauncherActivity",
            "com.zhihu.android.app.ui.activity.LaunchAdActivity",
            "com.zhihu.android.app.feed.AdTransparentHostActivity",
            "com.miui.home.launcher.Launcher"
          ],
          "rules": "TextView[id=`com.zhihu.android:id/btn_skip`]"
        },
        {
          "key": 1,
          "name": "关闭广告弹窗",
          "desc": "点击 关闭广告按钮 之后出现的广告弹窗",
          "activityIds": [
            "com.zhihu.android.ContentActivity",
            "com.zhihu.android.app.ui.activity.MainActivity"
          ],
          "rules": "@FrameLayout ImageView + TextView[text*=`虚假广告`][id=`com.zhihu.android:id/tv_content`]"
        },
        {
          "key": 2,
          "name": "关闭广告原因",
          "desc": "点击 关闭广告按钮 之后出现的选择原因",
          "activityIds": "com.zhihu.android.ContentActivity",
          "rules": [
            "[id=`com.zhihu.android:id/confirm_uninterest`]",
            "[id=`com.zhihu.android:id/revert_uninterest`] <n * + [id=`com.zhihu.android:id/reason_container`] > [id=`com.zhihu.android:id/uninterest_reason`]"
          ]
        },
        {
          "key": 3,
          "name": "关闭推荐",
          "desc": "关闭回答底部其他回答",
          "activityIds": "com.zhihu.android.mix.activity.ContentMixProfileActivity",
          "rules": [
            "TextView + View + TextView + TextView[text$=`评论`][text*=`赞同`] + View"
          ]
        },
        {
          "key": 5,
          "name": "推荐页广告卡片",
          "desc": "赚稿费广告卡片,盐选推荐广告,知乎学课堂,汽车广告",
          "activityIds": "com.zhihu.android.app.ui.activity.MainActivity",
          "rules": [
            "[id='com.zhihu.android:id/content'] >2 TextView[text='不感兴趣'][id='com.zhihu.android:id/title']",
            "TextView[text=`内容质量差`][id=`com.zhihu.android:id/tv_content`]",
            "@ImageView[id=`com.zhihu.android:id/menu`] < FrameLayout - * > TextView[text^=`广告`]",
            "@ImageView[id=null][clickable=true] -n TextView[text*=`广告`][index=0]"
          ]
        },
        {
          "key": 6,
          "name": "问题-回答列表-卡片广告",
          "activityIds": "com.zhihu.android.ContentActivity",
          "rules": [
            "@ImageView -n TextView[text=`广告`][index=0]",
            "ImageView[id=null] + TextView[text!=null][id=null] + ViewGroup > ImageView[clickable=true]"
          ]
        },
        {
          "key": 7,
          "name": "回答底部评论顶部的任意广告推荐",
          "activityIds": [
            "com.zhihu.android.mixshortcontainer.MixShortContainerActivity",
            "com.zhihu.android.app.ui.activity.HostActivity"
          ],
          "rules": [
            "@Image + TextView[text$=`的广告`]",
            "TextView[text$=`的广告`] +n TextView[text=`×`]",
            "TextView[text=`查看详情`] + TextView[text=`×`]",
            "TextView[text*=`赞同`][text*=`评论`] + TextView[text=`×`]",
            "TextView[text*=`回答`][text*=`关注`] + TextView[text=`×`]",
            "TextView[text!=null] + TextView[text*=`赞同`] + View > Image",
            "TextView[text$=`的广告`] - Image[id=null]",
            "TextView[text*=`广告`] +2 Image[id=null]",
            "TextView[text*=`点赞`][text*=`的回答`] +2 Image[id=null]",
            "TextView[text=''] + Image[text=''] + TextView[text='​'] + Image[id=null][clickable=true]"
          ]
        },
        {
          "key": 8,
          "name": "关闭首页广告",
          "activityIds": "com.zhihu.android.app.ui.activity.AdAlphaVideoActivity",
          "rules": "[id=`com.zhihu.android:id/tv_ad_close`]"
        },
        {
          "key": 9,
          "name": "推荐页-顶部广告",
          "activityIds": "com.zhihu.android.app.ui.activity.MainActivity",
          "rules": [
            "[id='com.zhihu.android:id/tv_ad_tag'] + [id='com.zhihu.android:id/img_close_focus']"
          ]
        }
      ]
    },
    {
      "id": "com.zidongdianji",
      "name": "自动点击器",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "com.autoclicker.clicker.ads.SplashActivity",
          "rules": [
            "[id=`com.byted.pangle:id/tt_splash_skip_btn`]",
            "TextView[text^=`跳过`]"
          ]
        },
        {
          "key": 1,
          "name": "首页顶部广告卡片",
          "activityIds": "com.autoclicker.clicker.MainActivity",
          "rules": [
            {
              "activityIds": "com.bytedance.sdk.openadsdk.core.dislike.ui",
              "matches": "@LinearLayout > TextView[id=`com.byted.pangle:id/tt_item_tv`][text=`不感兴趣`]"
            },
            "Image < @View + View >2 [text*=`广告`]"
          ]
        }
      ]
    },
    {
      "id": "ctrip.android.view",
      "name": "携程旅行",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "ctrip.android.publicproduct.home.view.CtripHomeActivity",
          "rules": [
            "LinearLayout[childCount=2] > TextView + TextView[text=\"跳过\"||text=\"跳过广告\"]"
          ],
          "snapshotUrls": [
            "https://gkd-kit.gitee.io/import/38517192/104f3807-7613-46ff-9eb2-3c8bcb6ee3b1",
            "https://gkd-kit.songe.li/import/12511071"
          ]
        }
      ]
    },
    {
      "id": "gov.pianzong.androidnga",
      "name": "NGA玩家社区",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "gov.pianzong.androidnga.activity.LoadingActivity",
          "rules": [
            "[id=\"gov.pianzong.androidnga:id/iv_tg_ad\"]"
          ],
          "snapshotUrls": "https://gkd-kit.gitee.io/import/12476484"
        },
        {
          "key": 1,
          "name": "首页-推荐-广告卡片",
          "activityIds": "com.donews.nga.activitys.MainActivity",
          "rules": [
            "[id=\"gov.pianzong.androidnga:id/iv_close_ad\"]"
          ],
          "snapshotUrls": "https://gkd-kit.gitee.io/import/12482727"
        }
      ]
    },
    {
      "id": "li.songe.gkd",
      "name": "GKD",
      "groups": [
        {
          "key": 0,
          "name": "GKD-空规则组"
        }
      ]
    },
    {
      "id": "me.ele",
      "name": "饿了么",
      "groups": [
        {
          "key": 0,
          "name": "开屏广告",
          "activityIds": "me.ele.application.ui.splash.SplashActivity",
          "rules": "[id=\"me.ele:id/skip_button\"]",
          "snapshotUrls": "https://gkd-kit.songe.li/import/12534930"
        }
      ]
    },
    {
      "id": "tv.danmaku.bili",
      "name": "B站",
      "groups": [
        {
          "key": -1,
          "name": "开屏广告",
          "desc": "开屏广告,切回APP开屏广告",
          "rules": "TextView[id=`tv.danmaku.bili:id/count_down`]"
        },
        {
          "key": 0,
          "name": "评论区顶部公告横幅",
          "rules": "LinearLayout[id=`tv.danmaku.bili:id/ad_tint_frame`] > ImageView[desc=`关闭`]",
          "excludeActivityIds": [
            "com.bilibili.bililive.room.ui.roomv3.LiveRoomActivityV3"
          ]
        },
        {
          "key": 1,
          "name": "青少年模式弹窗",
          "rules": "TextView[text*=`青少年模式`] + TextView[text=`我知道了`]"
        },
        {
          "key": 2,
          "name": "动态推荐卡片",
          "rules": [
            {
              "activityIds": "tv.danmaku.bili.MainActivityV2",
              "matches": "[id=`tv.danmaku.bili:id/ad_goods_mark_big`]"
            }
          ]
        },
        {
          "key": 3,
          "name": "点击关闭广告后出现的弹窗",
          "rules": [
            {
              "activityIds": "com.bilibili.lib.ui.menu",
              "matches": "TextView[text='广告质量差'||text='推广质量差'][id^='tv.danmaku.bili:id/reason']"
            }
          ]
        },
        {
          "key": 4,
          "name": "视频底部广告",
          "activityIds": "com.bilibili.video.videodetail.VideoDetailsActivity",
          "rules": [
            "[id=`tv.danmaku.bili:id/reason1_layout`] > [id=`tv.danmaku.bili:id/reason1`][text*=`广告`]",
            "[id=`tv.danmaku.bili:id/ad_tint_frame`][desc^=`UP主推荐广告`] @[id=`tv.danmaku.bili:id/more`] > ImageView"
          ]
        },
        {
          "key": 5,
          "name": "推荐页-可跳过广告",
          "activityIds": "tv.danmaku.bili.MainActivityV2",
          "rules": [
            "[id=`tv.danmaku.bili:id/click_skip`]"
          ]
        }
      ]
    }
  ]
}
