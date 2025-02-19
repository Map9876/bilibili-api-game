# bilibili-api-game




### 《哔哩哔哩游戏信息 API 文档》 

由ai生成： https://www.n.cn/search/e390884302134e3cb34869d5a5d49863?fr=none

https://www.n.cn/search/681c0fcababf4d95a293008678e218ef?fr=none

一、API 概述 
本 API 用于获取指定游戏（仙剑世界）的详细信息，包括游戏基本信息、下载链接、运营信息等。 通过游戏页面：
https://www.biligame.com/detail/?id=109365
电脑版获取
 
二、API 地址 
```plaintext 
https://line1-h5-pc-api.biligame.com/game/detail/gameinfo 
``` 
 
三、请求信息 
1. 请求方式 
GET 
 
2. 请求参数 
| 参数名         | 类型     | 是否必选 | 描述                                                 | 
|--------------|--------|------|----------------------------------------------------| 
| game_base_id | number | 是    | 游戏的基础 ID，此处仙剑世界的 ID 为 109365                           | 
| ts           | number | 否    | 时间戳，请求示例中的值为 1739974867216                      | 
| request_id   | string | 否    | 请求 ID，用于追踪请求，示例值为 yTWqCM6o4PBQYl4d4NJ3kGkfOPh63zxB | 
| appkey       | string | 否    | 应用密钥，示例值为 h9Ejat5tFh81cq8V                         | 
| sign         | string | 否    | 签名字符串，用于验证请求的合法性，示例值为 b12a35c74713b280b31f61c73873576b | 
 
3. 请求示例 
```plaintext 
https://line1-h5-pc-api.biligame.com/game/detail/gameinfo?game_base_id=109365
``` 
 
四、响应信息 
1. 响应格式 
JSON 
 
2. 响应参数 
| 参数名         | 类型       | 描述                                                         | 
|--------------|----------|------------------------------------------------------------| 
| code         | number   | 响应状态码，0 表示成功                                               | 
| message      | string   | 响应消息，成功时返回“成功”                                           | 
| request_id   | string   | 请求 ID，与请求时的 request_id 一致                             | 
| ts           | number   | 响应的时间戳                                                     | 
| data         | object   | 游戏详细信息的对象，包含以下子参数：                                       | 
| ├ game_base_id   | number   | 游戏的基础 ID，此处为 109365                                        | 
| ├ title          | string   | 游戏标题，此处为“仙剑世界”                                       | 
| ├ icon           | string   | 游戏图标链接，示例值为`//i0.hdslb.com/bfs/game/ee3add277f0d63debdc6679f363d763dc8907f24.jpg` | 
| ├ video_url      | number   | 游戏视频的 ID，示例值为 1455298725                             | 
| ├ is_android_online | boolean | 安卓版本是否在线，示例值为 true                               | 
| ├ is_ios_online  | boolean  | iOS 版本是否在线，示例值为 true                                 | 
| ├ is_pc_online   | boolean  | PC 版本是否在线，示例值为 true                                 | 
| ├ download_count | number   | 下载次数，示例值为 411288                                     | 
| ├ operator_name  | string   | 运营商名称，此处为“中手游”                                       | 
| ├ developer_name | string   | 开发者名称，此处为“深圳市中手游网络科技有限公司”                         | 
| ├ notice_title   | string   | 公告标题，如“B 服与官服（包括 ios 与 pc）可同服游玩，好友互通！”        | 
| ├ notice_content | string   | 公告内容，包含领取福利的链接，示例值为“B站下载领取独家定制小电视头像框及定制称号：https://xjsj.biligame.com/cfxj/h5” | 
| ├ summary        | string   | 游戏简介，此处为“仙剑 IP 首款开放世界 RPG”                          | 
| ├ android_download_link | string | 安卓版下载链接，示例值为 `https://pkg.biligame.com/games/xjsj_1.0.491.1191731_20250212_114909_277a7.apk` | 
| ├ pc_download_link | string    | PC 版下载链接（若有）                                               | 
| ├ privacy_policy_link | string | 隐私政策链接，如`https://cdnserver.cmge.com/service/xjsj/privacy_ZSY.html` |  
| ├ related_game_base_id | number | 相关游戏的基础 ID，示例值为 111696                                   | 
| ├ related_pc_game | object | 相关 PC 游戏的详细信息，结构与上述游戏信息类似                         | 
 
3. 响应示例 
```json 
{
  "code": 0,
  "message": "成功",
  "request_id": "yTWqCM6o4PBQYl4d4NJ3kGkfOPh63zxB",
  "ts": 1739975386042,
  "data": {
    "game_base_id": 109365,
    "title": "仙剑世界",
    "expended_name": "",
    "game_name_v2": "仙剑世界",
    "expanded_name": "",
    "postfix_list": [],
    "icon": "//i0.hdslb.com/bfs/game/ee3add277f0d63debdc6679f363d763dc8907f24.jpg",
    "video_image": "//i0.hdslb.com/bfs/game/3cf975aea6c84bef1654e833f7697a4cd55e2b91.jpg",
    "video_url": 1455298725,
    "source": 0,
    "is_android_online": true,
    "is_ios_online": true,
    "is_pc_online": true,
    "download_count": 411288,
    "forum_link": "",
    "operator_name": "中手游",
    "operator_id": "181521457112957814",
    "developer_name": "深圳市中手游网络科技有限公司",
    "establisher_name": "满天星工作室",
    "pc_background": "//i0.hdslb.com/bfs/game/28c09d02e3dc5a0f185b90c2d8aae2d083a4f716.jpg",
    "pc_logo": "//i0.hdslb.com/bfs/game/ed3e44c8e1f35ef22fa7fd1c143d7ad45ce90586.png",
    "notice_title": "B服与官服（包括ios与pc）可同服游玩，好友互通！",
    "notice_content": "B站下载领取独家定制小电视头像框及定制称号：https://xjsj.biligame.com/cfxj/h5",
    "summary": "仙剑IP首款开放世界RPG",
    "android_game_status": 0,
    "android_book_link": "",
    "android_download_link": "https://pkg.biligame.com/games/xjsj_1.0.491.1191731_20250212_114909_277a7.apk",
    "android_download_link2": "https://pkgdl.biligame.net/games/xjsj_1.0.491.1191731_20250212_114909_277a7.apk",
    "android_sign": "f0cff1dab3300c3026cb4a17bd9447d4",
    "android_pkg_name": "com.cmge.xianjianshijie.bilibili",
    "android_pkg_size": 284695935,
    "android_pkg_ver": 1191732,
    "ios_game_status": 7,
    "ios_book_link": "",
    "ios_download_link": "",
    "pc_game_status": 3,
    "pc_download_link": "",
    "pc_download_link2": "",
    "pc_book_link": "",
    "download_status": 1,
    "purchase_type": 0,
    "privacy_policy_link": "https://cdnserver.cmge.com/service/xjsj/privacy_ZSY.html",
    "use_new_ui": true,
    "online_platform": "Android",
    "recommend_reason": "1万人搜索",
    "rank_type": 1,
    "game_rank": 1,
    "presale_status": 0,
    "show_presale": 0,
    "related_game_base_id": 111696,
    "related_pc_game": {
      "game_base_id": 111696,
      "title": "仙剑世界（PC版）",
      "expended_name": "",
      "game_name_v2": "仙剑世界（PC版）",
      "expanded_name": "",
      "postfix_list": [],
      "icon": "//i0.hdslb.com/bfs/game/678606ea3a764f0643db4847a4d89f7b2dea5cb5.jpg",
      "video_image": "//i0.hdslb.com/bfs/game/2ed7aa5ecda7e3e1310b76b36652d2f42fa3eb6c.jpg",
      "video_url": 1455298725,
      "source": 3,
      "is_android_online": true,
      "is_ios_online": false,
      "is_pc_online": true,
      "download_count": 0,
      "forum_link": "",
      "operator_name": "中手游",
      "operator_id": "181521457112957814",
      "developer_name": "深圳市中手游网络科技有限公司",
      "establisher_name": "满天星工作室",
      "pc_background": "//i0.hdslb.com/bfs/game/c378437d50204fecaea319fd09f09024343d4e99.jpg",
      "pc_logo": "//i0.hdslb.com/bfs/game/ba041014adc34230b81e677c1b1018e43bf49ed6.png",
      "notice_title": "B服与官服（包括ios与pc）可同服游玩，好友互通！",
      "notice_content": "B站下载领取独家定制小电视头像框及定制称号：https://xjsj.biligame.com/cfxj",
      "summary": "仙剑IP首款开放世界RPG",
      "android_game_status": 6,
      "android_book_link": "",
      "android_download_link": "",
      "android_download_link2": "",
      "android_sign": "",
      "android_pkg_name": "",
      "pc_game_status": 0,
      "pc_download_link": "https://pkg.biligame.com/games/setup_xjsjBiliBili_3.2.5_02111822/564863/setup_xjsjBiliBili_3.2.5_02111822.exe",
      "pc_download_link2": "https://pkgdl.biligame.net/games/setup_xjsjBiliBili_3.2.5_02111822/564863/setup_xjsjBiliBili_3.2.5_02111822.exe",
      "pc_book_link": "",
      "download_status": 1,
      "purchase_type": 0,
      "privacy_policy_link": "https://app.biligame.com/privacy_agreement",
      "use_new_ui": true,
      "online_platform": "PC",
      "presale_status": 0,
      "show_presale": 0,
      "related_game_base_id": 109365,
      "is_show_ios": 0,
      "is_show_android": 1,
      "is_show_pc": 1 
    },
    "is_show_ios": 1,
    "is_show_android": 1,
    "is_show_pc": 1 
  }
}
```



### 哔哩哔哩小游戏信息查询 API 文档 
 https://www.n.cn/search/cb5d5bcd48ad4d0795d7aff3a919ebcc?fr=none
 
 https://app.biligame.com/mini-games/home/index.html?_bilifrom=sk小游戏中心，
浏览器打开之后，会跳转到app，通过alook浏览器能复制URL Scheme为
bilibili://game_center/game_jump?url=https%3A%2F%2Fapp.biligame.com%2Fmini-games%2Fhome%2Findex.html%3F_bilifrom%3Dsk
URL Scheme直接看html也能看到不过。


https://miniapp.bilibili.com/game/biligamed7ad58094563d08b?miniGameFrom=20004&sourcefrom=2499999981
小游戏页面，

一、API 概述 
此 API 用于获取哔哩哔哩小游戏的详细信息，如游戏名称、图标、介绍等。
二、API 地址 
``` 
https://miniapp.bilibili.com/api/miniapp/info/main 
``` 
 
三、请求信息 
 
1. 请求方式 
`GET` 或 `POST`（根据实际请求使用的 `curl` 脚本建议使用 `POST`） 

 https://miniapp.bilibili.com/api/miniapp/info/main?appId=biligamed7ad58094563d08b&miniappkey=46f711c1974a468c99c5e79af5509685
2. 请求参数 
| 参数名 | 类型 | 是否必传 | 描述 | 
| ---- | ---- | ---- | ---- | 
| appId | string | 是 | 小游戏的唯一标识符，例如 `biligamed7ad58094563d08b` | 
| miniappkey | string | 否 | 与小游戏关联的密钥，例如 `46f711c1974a468c99c5e79af5509685` | 

```json 
{ 
    "code": 0, 
    "message": "success", 
    "data": { 
        "appId": "biligamed7ad58094563d08b", 
        "name": "合成金铲子", 
        "logo": "https://i0.hdslb.com/bfs/game/43782775bef9fcb6f4086a3539372ff54662f042.png", 
        "introduction": "快来合成金铲子，欢乐不停歇。", 
        "companyName": "深圳澎云科技有限公司", 
        "cats": ["休闲"], 
        "catTrees": ["游戏>休闲"], 
        "type": 1, 
        "origin": 1, 
        "loadingImagePortrait": "https://i0.hdslb.com/bfs/game/a3697b521dd5074daaaef2718b1552094ae3af46.jpg", 
        "loadingImageLandscape": null, 
        "recordNumber": "粤ICP备2023123804号 - 2X", 
        "mtime": 1732877427000, 
        "modCreateTime": 1732877427000, 
        "statement": "本服务由开发者向哔哩哔哩用户提供，开发者对本服务信息内容、数据资料及其运营行为等的真实性、合法性及有效性承担全部责任。\n哔哩哔哩向开发者提供技术支持服务。", 
        "request": [ 
            "https://cdwaterbear.cn", 
            "https://logstorage.cocos.com", 
            "https://smby - config.oss - cn - shenzhen.aliyuncs.com", 
            "https://analytics.oceanengine.com", 
            "https://smcy - subconfig.oss - cn - shenzhen.aliyuncs.com", 
            "https://www.deniulor.com", 
            "https://umini.shujupie.com", 
            "https://api.cygame666.cn", 
            "https://service.cygame666.cn", 
            "https://cdn - corp - backup.cygame666.cn", 
            "https://backend.gravity - engine.com", 
            "https://api.sm0.fun", 
            "https://service.api.xiaoyouxi.co" 
        ], 
        "socket": null, 
        "uploadFile": null, 
        "downloadFile": [ 
            "https://game.sp.dubyc.com", 
            "https://api.cygame666.cn", 
            "https://service.cygame666.cn", 
            "https://cdn - corp - backup.cygame666.cn", 
            "https://cdn1.sm0.fun" 
        ], 
        "business": null 
    }, 
    "errtag": 0 
} 
```
