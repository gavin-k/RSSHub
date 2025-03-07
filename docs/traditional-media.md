---
pageClass: routes
---

# 传统媒体

## 21 财经

### 频道

<Route author="brilon" example="/21caijing/channel/readnumber" path="/21caijing/channel/:name" :paramsDesc="['频道名称，可在[https://m.21jingji.com/](https://m.21jingji.com/)页面URL中找到']"/>

## AP News

### 话题

<Route author="zoenglinghou" example="/apnews/topics/apf-topnews" path="/apnews/topics/:topic" :paramsDesc="['话题名称，可在 URL 中找到，例如 AP Top News [https://apnews.com/apf-topnews](https://apnews.com/apf-topnews) 的话题为 `apf-topnews`']" radar="1"/>

## BBC

### BBC

<Route author="HenryQW" example="/bbc/chinese" path="/bbc/:channel?" :paramsDesc="['频道, 缺省为热门']">

通过提取文章全文，以提供比官方源更佳的阅读体验.

支持大部分频道，频道名称见[官方频道 RSS](https://www.bbc.co.uk/news/10628494).

-   频道为单一路径，如 `https://feeds.bbci.co.uk/news/business/rss.xml` 则为 `/bbc/business`.
-   频道包含多重路径，如 `https://feeds.bbci.co.uk/news/world/asia/rss.xml` 则替换 `/` 为 `-` `/bbc/world-asia`.
-   例外: BBC 中文网为 `/bbc/chinese`, 繁体中文为 `/bbc/traditionalchinese`.

</Route>

## e 公司

### 快讯

<Route author="hillerliao" example="/egsea/flash" path="/egsea/flash" />

## FT 中文网

### FT 中文网

<Route author="HenryQW xyqfer" example="/ft/chinese/hotstoryby7day" path="/ft/:language/:channel?" :paramsDesc="['语言，简体`chinese`，繁体`traditional`', '频道, 缺省为每日更新']">

::: tip 提示

-   不支持付费文章.
-   由于未知原因 FT 中文网的 SSL 证书不被信任 (参见[SSL Labs 报告](https://www.ssllabs.com/ssltest/analyze.html?d=www.ftchinese.com&latest)), 所有文章通过 http 协议获取.

:::

通过提取文章全文，以提供比官方源更佳的阅读体验.

支持所有频道，频道名称见[官方频道 RSS](http://www.ftchinese.com/channel/rss.html).

-   频道为单一路径，如 `http://www.ftchinese.com/rss/news` 则为 `/ft/chinese/news`.
-   频道包含多重路径，如 `http://www.ftchinese.com/rss/column/007000002` 则替换 `/` 为 `-` `/ft/chinese/column-007000002`.

</Route>

## NHK

### News Web Easy

<Route author="Andiedie" example="/nhk/news_web_easy" path="/nhk/news_web_easy"/>

## Solidot

### 最新消息

<Route author="sgqy" example="/solidot/linux" path="/solidot/:type?" :paramsDesc="['消息类型. 默认为 www. 在网站上方选择后复制子域名即可']">

::: tip 提示

Solidot 提供的 feed:

-   <https://www.solidot.org/index.rss>

:::

| 全部 | 创业    | Linux | 科学    | 科技       | 移动   | 苹果  | 硬件     | 软件     | 安全     | 游戏  | 书籍  | ask | idle | 博客 | 云计算 |
| ---- | ------- | ----- | ------- | ---------- | ------ | ----- | -------- | -------- | -------- | ----- | ----- | --- | ---- | ---- | ------ |
| www  | startup | linux | science | technology | mobile | apple | hardware | software | security | games | books | ask | idle | blog | cloud  |

</Route>

## The Economist

### 分类

<Route author="ImSingee" example="/the-economist/latest" path="/the-economist/:endpoint" :paramsDesc="['分类名称，可在 [官方 RSS 页面 ](https://www.economist.com/rss) 找到，例如 https://www.economist.com/china/rss.xml 即为 china']"/>

### GRE Vocabulary

<Route author="xyqfer" example="/the-economist/gre-vocabulary" path="/the-economist/gre-vocabulary" />

## Yahoo

### 新聞

<Route author="KeiLongW" example="/yahoo-news/hk/world" path="/yahoo-news/:region/:category?" :paramsDesc="['地区','类别']">

`地区`

| 香港 | 台灣 | 美國 |
| ---- | ---- | ---- |
| hk   | tw   | en   |

`类別`

| 新聞總集 | 兩岸國際 | 財經     | 娛樂          | 體育   | 健康   |
| -------- | -------- | -------- | ------------- | ------ | ------ |
| (空)     | world    | business | entertainment | sports | health |

</Route>

## 半月谈

### 板块

<Route author="LogicJake" example="/banyuetan/jicengzhili" path="/banyuetan/:name" :paramsDesc="['板块名称，可在 URL 中找到']"/>

## 北极星电力网

### 北极星环保

<Route author="zsimple"  example="/bjx/huanbao" path="/bjx/huanbao" />

## 财新网

> 网站部分内容需要付费订阅，RSS 仅做更新提醒，不含付费内容.

### 新闻分类

<Route author="idealclover" example="/caixin/finance/regulation" path="/caixin/:column/:category" :paramsDesc="['栏目名', '栏目下的子分类名']">

Column 列表:

| 经济    | 金融    | 政经  | 环科    | 世界          | 观点网  | 文化    | 周刊   |
| ------- | ------- | ----- | ------- | ------------- | ------- | ------- | ------ |
| economy | finance | china | science | international | opinion | culture | weekly |

以金融板块为例的 category 列表: （其余 column 以类似方式寻找）

| 监管       | 银行 | 证券基金 | 信托保险        | 投资       | 创新       | 市场   |
| ---------- | ---- | -------- | --------------- | ---------- | ---------- | ------ |
| regulation | bank | stock    | insurance_trust | investment | innovation | market |

Category 列表:

| 封面报道   | 开卷  | 社论      | 时事            | 编辑寄语    | 经济    | 金融    | 商业     | 环境与科技             | 民生    | 副刊   |
| ---------- | ----- | --------- | --------------- | ----------- | ------- | ------- | -------- | ---------------------- | ------- | ------ |
| coverstory | first | editorial | current_affairs | editor_desk | economy | finance | business | environment_technology | cwcivil | column |

</Route>

### 首页新闻

<Route author="EsuRt"  example="/caixin/article" path="/caixin/article"/>

## 第一财经

### 直播区

<Route author="sanmmm" example="/yicai/brief" path="/yicai/brief" />

## 东方网

### 上海新闻

<Route author="saury" example="/eastday/sh" path="/eastday/sh" />

</Route>

## 端传媒

### 端传媒

<Route author="prnake" example="/initium/feature/zh-hans" path="/initium/:type?/:language?" :paramsDesc="['栏目，缺省为深度', '语言，简体`zh-hans`，繁体`zh-hant`，缺省为简体']"/>

::: warning 注意

付费内容全文需要登陆获取，详情见部署页面的配置模块。

:::

Type 栏目:

| 深度    | What’s New | 广场              | Pick-Up |
| ------- | ---------- | ----------------- | ------- |
| feature | news-brief | notes-and-letters | pick_up |

通过提取文章全文，以提供比官方源更佳的阅读体验.

</Route>
## 多维新闻网

### 要闻

<Route author="HenryQW" example="/dwnews/yaowen/global" path="/dwnews/yaowen/:region?" :paramsDesc="['要闻地区，默认`全部`，可选地区如下']">

| 全部   | 国际   | 中国  | 香港     | 台湾   | 经济   | 视觉   |
| ------ | ------ | ----- | -------- | ------ | ------ | ------ |
| yaowen | global | china | hongkong | taiwan | jingji | shijue |

</Route>

### 24 小时新闻排行榜

<Route author="HenryQW" example="/dwnews/rank" path="/dwnews/rank"/>

## 华尔街见闻

### 华尔街见闻

<Route author="conanjunn" example="/wallstreetcn/news/global" path="/wallstreetcn/news/global" />

## 极客公园

### 全球快讯

<Route author="xyqfer" example="/geekpark/breakingnews" path="/geekpark/breakingnews" />

## 界面新闻

### 栏目

<Route author="WenhuWee" example="/jiemian/list/79" path="/jiemian/list/:category" :paramsDesc="['对应栏目后在地址栏找到']"/>

## 经济观察网

### 分类资讯

<Route author="epirus" example="/eeo/15" path="/eeo/:category" :paramsDesc="['分类']">

category 对应的关键词有

| 时事 | 政策 | 证券 | 资本 | 理财 | 新科技 | 大健康 | 房产 | 汽车 | 消费 | 影视 | 娱乐 | 体育 | 教育 | 观察家 | 专栏 | 书评 | 个人历史 | 宏观 |
| ---- | ---- | ---- | ---- | ---- | ------ | ------ | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ------ | ---- | ---- | -------- | ---- |
| 01   | 02   | 03   | 04   | 05   | 06     | 07     | 08   | 09   | 10   | 11   | 12   | 13   | 14   | 15     | 16   | 17   | 18       | 19   |

</Route>

## 联合早报

### 即时新闻

<Route author="lengthmin" example="/zaobao/realtime/china" path="/zaobao/realtime/:type?" :paramsDesc="['分类, 缺省为 china']">

| 中国  | 新加坡    | 国际  | 财经     |
| ----- | --------- | ----- | -------- |
| china | singapore | world | zfinance |

</Route>

### 新闻

<Route author="lengthmin" example="/zaobao/znews/china" path="/zaobao/znews/:type?" :paramsDesc="['分类, 缺省为 china']">

| 中国  | 新加坡    | 东南亚 | 国际  | 体育   | 早报现在 |
| ----- | --------- | ------ | ----- | ------ | -------- |
| china | singapore | sea    | world | sports | fukan    |

</Route>

### 其他栏目

除了上面两个兼容规则之外，联合早报网站里所有页面形如 <https://www.zaobao.com/wencui/politic> 这样的栏目都能被这个规则解析到，早报的大部分栏目都是这个样式的。你可以测试之后再订阅。

<Route author="lengthmin" example="/zaobao/wencui/politic" path="/zaobao/:type/:section" :paramsDesc="['https://www.zaobao.com/**wencui**/politic 中的 **wencui**', 'https://www.zaobao.com/wencui/**politic** 中的 **politic**']" />

## 连线 Wired

非订阅用户每月有阅读全文次数限制。

### 标签

<Route author="Naiqus" example="/wired/tag/bitcoin" path="/wired/tag/:tag" :paramsDesc="['标签']">

</Route>

## 每经网

### 重磅原创

<Route author="MeXunco" example="/nbd/daily" path="/nbd/daily" />

## 南方周末

### 新闻分类

<Route author="ranpox xyqfer" example="/infzm/2" path="/infzm/:id" :paramsDesc="['南方周末内容分区 id, 可在该内容分区的 URL 中找到(即 https://www.infzm.com/contents?term_id=:id)']">

下面给出部分参考:

| 推荐 | 新闻 | 观点 | 文化 | 人物 | 影像 | 专题 | 生活 | 视频 |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| 1    | 2    | 3    | 4    | 7    | 8    | 6    | 5    | 131  |

</Route>

## 纽约时报

### 新闻

<Route author="HenryQW" example="/nytimes/dual" path="/nytimes/:lang?" :paramsDesc="['语言, 缺省中文']">

通过提取文章全文，以提供比官方源更佳的阅读体验。

| 默认中文 | 中英对照 | 英文 | 中英对照 (繁体中文)     | 繁体中文           |
| -------- | -------- | ---- | ----------------------- | ------------------ |
| (空)     | dual     | en   | dual-traditionalchinese | traditionalchinese |

</Route>

### 每日简报

<Route author="xyqfer" example="/nytimes/morning_post" path="/nytimes/morning_post"/>

## 澎湃新闻

### 首页头条

<Route author="HenryQW" example="/thepaper/featured" path="/thepaper/featured"/>

### 频道

<Route author="xyqfer" example="/thepaper/channel/27224" path="/thepaper/channel/:id" :paramsDesc="['频道 id']"/>

### 澎湃美数组作品集

<Route author="umm233" example="/thepaper/839studio/2" path="/thepaper/839studio/:id?" :paramsDesc="['分类 id 可选，默认订阅全部分类']">

| 视频 | 交互 | 信息图 | 数据故事 |
| ---- | ---- | ------ | -------- |
| 2    | 4    | 3      | 453      |

</Route>

## 齐鲁晚报

### 新闻

<Route author="nczitzk" example="/qlwb/news" path="/qlwb/news"/>

### 今日城市

<Route author="nczitzk" example="/qlwb/city/:city" path="/qlwb/city" :paramsDesc="['城市代码']">

| 今日临沂 | 今日德州 | 今日威海 | 今日枣庄  | 今日淄博 | 今日烟台 | 今日潍坊 | 今日菏泽 | 今日日照 | 今日泰山 | 今日聊城  | 今日济宁 |
| -------- | -------- | -------- | --------- | -------- | -------- | -------- | -------- | -------- | -------- | --------- | -------- |
| linyi    | dezhou   | weihai   | zaozhuang | zibo     | yantai   | weifang  | heze     | rizhao   | taishan  | liaocheng | jining   |

</Route>

## 人民日报

### 观点

<Route author="LogicJake"  example="/people/opinion/223228" path="/people/opinion/:id" :paramsDesc="['板块id，可在 URL 中找到']"/>

### 环保频道

<Route author="zsimple"  example="/people/env/74877" path="/people/env/:id" :paramsDesc="['板块id，可在 URL 中找到']"/>

### 习近平系列重要讲话

<Route author="LogicJake"  example="/people/xjpjh" path="/people/xjpjh/:keyword?/:year?" :paramsDesc="['关键词，默认不填','年份，默认all']"/>

## 人民日报社 国际金融报

### 栏目

<Route author="Origami404" example="/ifnews/48" path="/ifnews/:cid" :paramsDesc="['栏目ID']">

`cid`可在对应栏目的 url 后的参数中获取，如`热点快报`的栏目 url 为`http://www.ifnews.com/column.html?cid=48`, `cid`即为`48`.

</Route>

## 日本経済新聞

### ホームページ

<Route author="zjysdhr" example="/nikkei/index" path="/nikkei/index" radar="1">

日文版首页

</Route>

## 网易新闻专栏

### 栏目

<Route author="Solist-X" example="/netease/news/special/1" path="/netease/news/special/:type?" :paramsDesc="['栏目']">

| 轻松一刻 | 槽值 | 人间 | 大国小民 | 三三有梗 | 数读 | 看客 | 下划线 | 谈心社 | 哒哒 | 胖编怪聊 | 曲一刀 | 今日之声 | 浪潮 | 沸点 |
| -------- | ---- | ---- | -------- | -------- | ---- | ---- | ------ | ------ | ---- | -------- | ------ | -------- | ---- | ---- |
| 1        | 2    | 3    | 4        | 5        | 6    | 7    | 8      | 9      | 10   | 11       | 12     | 13       | 14   | 15   |

</Route>

## 卫报 The Guardian

通过提取文章全文，以提供比官方源更佳的阅读体验。

### Editorial

<Route author="HenryQW" example="/guardian/editorial" path="/guardian/editorial"/>

### China

<Route author="Polynomia" example="/guardian/china" path="/guardian/china"/>

## 文汇报

### 分类

<Route author="hoilc" example="/whb/bihui" path="/whb/:category" :paramsDesc="['文汇报分类名, 可在该分类的 URL 中找到(即 http://www.whb.cn/zhuzhan/:category/index.html)']" />

## 香港 01

### 热门

<Route author="hoilc" example="/hk01/hot" path="/hk01/hot" />

### 栏目

<Route author="hoilc" example="/hk01/zone/11" path="/hk01/zone/:id" :paramsDesc="['栏目id, 可在URL中找到']"/>

### 子栏目

<Route author="hoilc" example="/hk01/channel/391" path="/hk01/channel/:id" :paramsDesc="['子栏目id, 可在URL中找到']"/>

### 专题

<Route author="hoilc" example="/hk01/issue/649" path="/hk01/issue/:id" :paramsDesc="['专题id, 可在URL中找到']"/>

### 标签

<Route author="hoilc" example="/hk01/tag/2787" path="/hk01/tag/:id" :paramsDesc="['标签id, 可在URL中找到']"/>

## 香港電台

### 新聞

香港電台官方已有提供全文 RSS，詳細可前往官方網站： <https://news.rthk.hk/rthk/ch/rss.htm>

此路由主要補回官方 RSS 缺少的圖片以及 Link 元素。（官方 RSS 沒有 Link 元素可能導致某些 RSS 客戶端出現問題）

<Route author="KeiLongW" example="/rthk-news/hk/international" path="/rthk-news/:lang/:category" :paramsDesc="['语言，繁体`hk`，英文`en`','类别']">

| local    | greaterchina | international | finance  | sport    |
| -------- | ------------ | ------------- | -------- | -------- |
| 本地新聞 | 大中華新聞   | 國際新聞      | 財經新聞 | 體育新聞 |

</Route>

## 新京报

### 栏目

<Route author="DIYgod" example="/bjnews/realtime" path="/bjnews/:category" :paramsDesc="['新京报的栏目名, 点击对应栏目后在地址栏找到']"/>

### 电子报

<Route author="MisteryMonster" example="/bjnews/epaper/A" path="/bjnews/epaper/:cat" :paramsDesc="['新京报叠名：`A`,`B`,`C`,`D`,特刊为`special`']"/>

## 新浪科技

### 科学探索

<Route author="LogicJake" example="/sina/discovery/zx" path="/sina/discovery/:type" :paramsDesc="['订阅分区类型']">

分类：

| zx   | twhk     | dwzw     | zrdl     | lskg     | smyx     | shbk     | kjqy     |
| ---- | -------- | -------- | -------- | -------- | -------- | -------- | -------- |
| 最新 | 天文航空 | 动物植物 | 自然地理 | 历史考古 | 生命医学 | 生活百科 | 科技前沿 |

</Route>

### 滚动新闻

<Route author="xyqfer" example="/sina/rollnews" path="/sina/rollnews" />

## 央视新闻

### 新闻联播

<Route author="zengxs" example="/cctv/xwlb" path="/cctv/xwlb">

新闻联播内容摘要。

</Route>

### 专题

<Route author="idealclover xyqfer" example="/cctv/world" path="/cctv/:category" :paramsDesc="['分类名']">

| 新闻 | 国内  | 国际  | 社会    | 法治 | 文娱 | 科技 | 生活 | 教育 | 每周质量报告 |
| ---- | ----- | ----- | ------- | ---- | ---- | ---- | ---- | ---- | ------------ |
| news | china | world | society | law  | ent  | tech | life | edu  | mzzlbg       |

</Route>

### 新闻联播文字版

<Route author="luyuhuang" example="/xinwenlianbo/index" path="/xinwenlianbo/index" radar="1"/>

## 朝日新聞中文網（繁體中文版）

### 新聞分類

<Route author="qiwihui" example="/asahichinese-f/society" path="/asahichinese-f/:category/:subCate?" :paramsDesc="['版块', '子版块']">

版块：

| society  | politics_economy | cool_japan | travel     | sports     | business   | technology | world      | opinion    | whatsnew |
| -------- | ---------------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | -------- |
| 國內綜合 | 政治・經濟       | 文化・生活 | 旅遊・活動 | 體育・奧運 | 商業・商品 | IT ・科技  | 國際・東亞 | 評論・專欄 | 最新消息 |

版块 `cool_japan` 和 `travel` 包含子版块：

`cool_japan`：

| entertainment | anime | life       | style_culture |
| ------------- | ----- | ---------- | ------------- |
| 藝能          | 動漫  | 生活・美食 | 時尚・藝文    |

`travel`:

| news | scenery | topic | move |
| ---- | ------- | ----- | ---- |
| 資訊 | 風景    | 體驗  | 交通 |

</Route>

## 朝日新聞中文网（简体中文版）

### 新闻分类

<Route author="zhouchang29" example="/asahichinese-j/society" path="/asahichinese-j/:category/:subCate?" :paramsDesc="['版块', '子版块']">

版块：

| society  | politics_economy | cool_japan | travel     | sports     | business   | technology | world      | opinion    | whatsnew |
| -------- | ---------------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | -------- |
| 日本社会 | 政治・经济       | 文娱・生活 | 旅游・活动 | 体育・奥运 | 商务・商品 | IT ・科技  | 国际・东亚 | 观点・专栏 | 最新     |

版块 `cool_japan` 和 `travel` 包含子版块：

`cool_japan`：

| entertainment | anime | life       | style_culture |
| ------------- | ----- | ---------- | ------------- |
| 艺能          | 动漫  | 生活・美食 | 时尚・文化    |

`travel`:

| news | scenery | topic | move |
| ---- | ------- | ----- | ---- |
| 资讯 | 风景    | 体验  | 交通 |

</Route>

## 中国日报

### 英语点津

<Route author="sanmmm" example="/chinadaily/english/thelatest" path="/chinadaily/english/:category" :paramsDesc="['目录分类']">

目录分类

| 最新      | 双语           | 热词          | 口语            | 译词          | 视频        | 听力     | 专栏      | 文件                     | 考试         |
| --------- | -------------- | ------------- | --------------- | ------------- | ----------- | -------- | --------- | ------------------------ | ------------ |
| thelatest | news_bilingual | news_hotwords | practice_tongue | trans_collect | video_links | audio_cd | columnist | 5af95d44a3103f6866ee845c | englishexams |

</Route>

## 中時電子報

### 新聞

<Route author="luyuhuang" example="/chinatimes/realtimenews" path="/chinatimes/:caty" :paramsDesc="['类别']" radar="1">

| realtimenews | politic | opinion | life | star | money | society | hottopic | tube    | world | armament | chinese | fashion | sports | technologynews | travel | album |
| ------------ | ------- | ------- | ---- | ---- | ----- | ------- | -------- | ------- | ----- | -------- | ------- | ------- | ------ | -------------- | ------ | ----- |
| 即時         | 政治    | 言論    | 生活 | 娛樂 | 財經  | 社會    | 話題     | 快點 TV | 國際  | 軍事     | 兩岸    | 時尚    | 體育   | 科技           | 玩食   | 專輯  |

</Route>

## 中外对话

### 主题

<Route author="zoenglinghou" example="/chinadialogue/topics/cities" path="/chinadialogue/topics/:topic" :paramsDesc="['主题分类']">

| 商业     | 城市化 | 气候变化与能源            | 自然保护     | 管制与法律         | 健康与食品      | 自然灾害          | 污染      | 科学与技术       | 安全     | 水    |
| -------- | ------ | ------------------------- | ------------ | ------------------ | --------------- | ----------------- | --------- | ---------------- | -------- | ----- |
| business | cities | climate-change-and-energy | conservation | governance-and-law | health-and-food | natural-disasters | pollution | science-and-tech | security | water |

</Route>

### 栏目

<Route author="zoenglinghou" example="/chinadialogue/article" path="/chinadialogue/:column" :paramsDesc="['栏目分类']">

| 文章    | 博客 | 文化    | 报告    |
| ------- | ---- | ------- | ------- |
| article | blog | culture | reports |

</Route>
