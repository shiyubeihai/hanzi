# Demos · 免费试玩

各个小作品的试用版与免费完整版集合，用于 GitHub Pages 托管。试玩免费，付费作品的完整版需购买。

## 当前内容

| 目录 | 作品 | 说明 |
|---|---|---|
| `hanzi_match/` | 汉字拼音配对 | 2264 条 · 1504 个汉字，全部 / 词语 / 单字 / 地名四模式，带朗读与练习日历 |
| `italiano2000-demo/` | Italiano2000 消消乐 | 200 词打字试玩版，意大利语 A1–B1 |
| `italiano2000-matching-demo/` | Italiano2000 连连看 | 200 词试玩版，三模式 + 背景音乐，手机可玩 |
| `english-matching-demo/` | 初中英语连线消消乐 | 免费完整版，1924 词 + 171 短语，词性标注 + TTS + 错词本 |
| `highschool-matching-demo/` | 高中英语连线消消乐 | 免费版，1002 词 + 305 搭配，例句 + TTS + 错词本 |
| `index.html` | 目录页 | 卡片列表（手动维护） |

> `english-matching-demo/` 和 `highschool-matching-demo/` 是免费完整版，词库有意公开；其余试玩目录只放付费产品的子集。

## 发布到 GitHub Pages

1. 把本目录推到仓库 `demos` 的 `main` 分支。
2. 打开仓库 **Settings → Pages**。
3. Source 选 **Deploy from a branch**，Branch 选 `main` / `(root)`，保存。
4. 等 1–2 分钟，访问：
   `https://<你的用户名>.github.io/demos/`
5. 试玩版地址：
   - 打字：`https://<你的用户名>.github.io/demos/italiano2000-demo/`
   - 连连看：`https://<你的用户名>.github.io/demos/italiano2000-matching-demo/`
   - 英语连连看（初中）：`https://<你的用户名>.github.io/demos/english-matching-demo/`
   - 英语连连看（高中）：`https://<你的用户名>.github.io/demos/highschool-matching-demo/`

> 免费账户的 GitHub Pages 需要仓库为 **Public**。付费产品只放试玩子集，不要放完整词库和付费音频；`english-matching-demo/` 和 `highschool-matching-demo/` 是明确公开的免费完整版，不受此限。

## 新增一个试玩版

1. 新建目录，例如 `deutsch1000-demo/`。
2. 放入单文件 `index.html`（相对路径引用资源，避免绝对路径）。
3. 在根目录 `index.html` 的卡片列表里加一张卡片，链接到该目录。
4. 推送后自动生效。

## 购买链接

试玩版侧栏有「完整版」卡片，默认隐藏购买按钮。上架面包多后，在试玩 HTML 里找到：

```js
const BUY_URL = ""; // TODO: 上架后填入面包多作品链接
```

填成你的作品链接即可，例如 `https://mbd.pub/o/xxxx`。

## 不要提交到公开仓库

- Italiano2000 的完整词库（2085 词）与完整版 HTML
- 预生成的音频精灵（`*.mp3` / `*.m4a`）
- Anki 词库、付费 PDF、授权文件
- 任何包含买家信息或订单号的版本

`.gitignore` 已经拦截常见的大文件类型，但提交前仍建议 `git status` 检查一遍。

## 授权

试玩版采用「免费试玩」授权：可自由访问和分享链接，但禁止转售、拆分词库或用于商业再发布。详见 `LICENSE.md`。

完整版为付费产品，购买后获得个人使用授权，具体条款以商品页为准。

## 合规提醒

- 不要在产品名或文案中使用「多邻国」等第三方商标，也不要声称官方关联。
- 词表请以原创整理的方式呈现，不要复制课程原句或音频。
