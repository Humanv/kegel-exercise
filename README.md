# 提气 · 凯格尔练习

一个轻量的凯格尔练习网页小游戏。按住收紧、松开放松，一次完整的收放记作一次。

[**在线试玩 →**](https://humanv.github.io/kegel-exercise/)

![提气练习页面预览](preview.png)

## 玩法

- **按住**中央圆盘（鼠标、触屏或空格键）：花瓣收拢，表示收紧盆底肌。
- **松开**：花瓣展开，并记录一次完成。
- 右上角显示今日完成次数，按天保存在浏览器的 `localStorage` 中；清零需要二次确认。
- 建议每下收紧 3 秒、放松 3 秒，全程自然呼吸。

## 运行

无需构建，也没有运行依赖。直接双击 `index.html` 即可打开。

如需通过本地服务器访问：

```powershell
python -m http.server 8000
# 浏览器打开 http://localhost:8000
```

页面使用 Google Fonts；字体加载失败时会回退到系统中文字体，不影响功能。

## 文件

- `index.html`：完整页面，样式与交互脚本均内联。
- `preview.png`：页面预览图。

## 技术

原生 HTML、CSS 和 JavaScript，响应式布局，支持深色模式与 prefers-reduced-motion。
