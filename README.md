# 一吸一呼

一吸一呼，妙不可言。

按住，等光环满一圈，再松开。每天三十口，偷偷攒点底气。一个故意不说明白、但可以拿去挑衅朋友的小游戏。

[**在线试玩 →**](https://humanv.github.io/kegel-exercise/)

![一吸一呼页面预览](preview.png)

## 玩法

- **按住**圆盘或全局长按 **空格键** 蓄气：四层共 68 片短圆花瓣像一朵暖黄色菊花，会交错拧紧，光粒被吸进中心，镜头同步推近，四周慢慢变暗，直到满环。
- 满环时画面轻轻一震，伴随清越磬音；继续按住超过目标时长 1.5 秒进入「深蓄」态，花心透出流金微光，实时显示蓄气秒数。
- **松开**后花瓣按本次收紧的时长慢慢摊开，光粒向外散开，荡出涟漪，再缓缓恢复呼吸感。
- 收和放使用同一套时间：默认入门 **3 秒**，也可在左侧切换 **进阶 5 秒** 或 **资深 8 秒**；按得更久，舒展也更久（上限 10 秒）。
- 光没满就松手，这一口不算；松开后要等它散完，再开始下一口。
- 每完成一口，外圈就点亮一颗小小的星。三十口，连成今天的一整圈。
- 第 10、20、30 口会出现印章和一句话；页面氛围光晕、星环和今日状态会分四个阶段演进，并配有动态轮换文案。
- 左侧微录会保留**近七日轨迹**、**连续打卡天数**、**历史累计气数**与**今日最深一口**。
- 支持鼠标、触屏和全局空格键；右上角可手动切换**浅色 / 深色外观**，手机与深色模式均已适配。
- 如果系统开启了“减少动态效果”，页面会显示一条提示；点「仍然播放」可以在本次访问里恢复动效。

## 拿去炫耀

右上角的箭头或底部的「拿去炫耀」会生成一张今日战绩卡，包含暖金菊花、气数、随机称号、评语和连练记录。

- **复制挑衅文案**：生成一个带 `?c=你的气数` 的链接，朋友打开后会看到“收到挑衅：有人偷偷练了 N 口”。
- **保存战绩卡**：纯前端离线生成高清 PNG 密报图，支持一键下载或直接随系统分享发出。
- **换一句评语**：不满意当前称号或评语时可随时换一套再炫耀。
- **反杀闭环**：朋友的挑战进度会实时显示；超过对方后会触发反超印章，按钮自动切换为「反杀炫耀」并生成专属回怼文案。
- 挑战链接最多把对方的目标带到 30 口，不会鼓励无限加练。

![战绩卡预览](share-preview.png)

## 声音

右上角有两个独立开关：

- **音乐开 / 关**：连续背景音乐。
- **音效开 / 关**：起手声、随蓄力进度上扬的连续聚气共鸣音、满环磬音、散气呼息、未达标和成就提示音。

浏览器禁止页面在没有交互时自动出声，所以打开页面后需要先点击或按一次键。开启“音效”时会播放一小段试听。所有声音都由浏览器 Web Audio 实时合成，不加载外部音轨。

## 运行

无需构建，也没有运行依赖。直接双击 `index.html` 即可打开。

如需通过本地服务器访问：

```powershell
python -m http.server 8000
# 浏览器打开 http://localhost:8000
```

页面使用 Google Fonts；字体加载失败时会回退到系统中文字体，不影响功能。

## 文件

- `index.html`：完整页面，样式、交互脚本和音乐合成逻辑均内联。
- `preview.png`：页面预览图。
- `share-preview.png`：战绩卡预览。

## 技术

原生 HTML、CSS 和 JavaScript。每日气数保存在浏览器 `localStorage`；Web Audio 负责实时背景音乐和独立音效。

<details>
<summary>开发者说明：底层节奏与健康边界</summary>

游戏不展示训练说明，但交互节奏参考了常见的盆底肌训练入门方案：收紧约 3 秒、完全放松约 3 秒，每天约 30 次。游戏只把节奏藏在光圈和散气动画里。

这不是医疗建议。孕期、产后、近期盆腔手术、盆底疼痛或练习后症状加重时，请先咨询医生或盆底康复师；疑似盆底高张力时不应默认加练收缩。页面底部只保留“身体不舒服，就停”的简短提示。

参考资料：

- [NICE NG123：女性尿失禁与盆腔器官脱垂管理](https://www.nice.org.uk/guidance/ng123)
- [NHS Leeds：男性盆底肌练习](https://leedscommunityhealthcare.nhs.uk/our-services-a-z/continence-urology-and-colorectal-cucs/bladder-problems-cucs/pelvic-floor-exercises-for-men-cucs/)
- [NHS LSCFT：女性盆底肌练习说明](https://www.lscft.nhs.uk/our-services/service-finder-z/continence-service/pelvic-floor-physiotherapy/pelvic-floor-muscle-exercise-information-sheet-women)
- [NHS MKUH：孕期与产后盆底护理](https://www.mkuh.nhs.uk/maternity-services/your-pregnancy-journey/postnatal-care/care-of-the-pelvic-floor-and-perineum)
- [Torosis et al., A Treatment Algorithm for High-Tone Pelvic Floor Dysfunction](https://pmc.ncbi.nlm.nih.gov/articles/PMC10953682/)

</details>
