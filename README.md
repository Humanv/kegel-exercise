# 提气 · 一口气小游戏

按住，等光环满一圈，再松开。每天三十口，偷偷攒点底气。

[**在线试玩 →**](https://humanv.github.io/kegel-exercise/)

![提气页面预览](preview.png)

## 玩法

- **按住**圆盘蓄气：四层共 70 片细长花瓣会交错拧紧，光粒被吸进中心，镜头同步推近，四周慢慢变暗，直到满环。
- 满环时画面轻轻一震；**松开**后慢半拍展开：花瓣层层摊开，光粒向外散开，荡出两三圈涟漪，再缓缓恢复呼吸感。
- 光没满就松手，这一口不算；松开后要等它散完，再开始下一口。
- 每完成一口，外圈就点亮一颗小小的星。三十口，连成今天的一整圈。
- 第 10、20、30 口会出现印章和一句话；底色、光圈和今日状态也会跟着变化。
- 今日状态会经历：气还没聚 → 有点儿意思了 → 气顺了 → 气势来了 → 圆满了。
- 支持鼠标、触屏和空格键；手机、深色模式和减少动态效果都做了适配。

## 声音

右上角有两个独立开关：

- **音乐开 / 关**：连续背景音乐。
- **音效开 / 关**：聚气、满环、散气、未达标和成就提示音。

浏览器禁止页面在没有交互时自动出声，所以打开页面后需要先点击或按一次键。开启“音效”时会播放一小段试听。所有声音都由浏览器实时合成，不加载外部音轨。

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
