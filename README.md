# 天机推演 · 六十四卦数据与 AI 解读引擎

> 用 AI 让三千年前的《周易》智慧重新被看见。官网：**[claw-book.cn](https://claw-book.cn/)** · 微信小程序「天机推演」

天机推演是一个结合**传统易学**与**现代大模型**的开放内容项目。本仓库开源完整的**六十四卦结构化数据**（卦辞、六爻爻辞原文 + 白话解读 + 现代应用），以及把数据渲染为黑金极简风格网页的**静态页面生成器**。

---

## ✨ 在线体验

| 入口 | 链接 |
|---|---|
| **官网首页** | https://claw-book.cn/ |
| 六十四卦详解（在线版） | https://claw-book.cn/liu-shi-si-gua.html |
| 卦例：乾卦详解 | https://claw-book.cn/gua-01.html |
| 卦例：未济卦详解 | https://claw-book.cn/gua-64.html |
| 微信小程序 | 微信搜索「天机推演」 |

---

## 📦 内容

- **`data/gua64.py`** —— 六十四卦完整数据（上经 1-30 + 下经 31-64），每卦包含：
  - `name` 卦名 / `full` 卦象全称（如「乾为天」）
  - `sym` Unicode 标准卦符（䷀～䷿）
  - `judge` 卦辞原文（《周易》通行本）
  - `yao` 六爻爻辞原文（初六/九二/…/上九）
  - `mean` 白话卦义解读
  - `app` 现代应用场景参考

- **`tools/gen_pages.py`** —— 黑金极简风格页面生成器：
  - 每卦生成一个独立 HTML（`gua-01.html` ~ `gua-64.html`）
  - 完整 SEO 标签：title / description / canonical / Open Graph / Twitter Card / JSON-LD（Article）
  - 响应式布局，移动端 2 列、桌面 4 列
  - 内置上下卦、总览、知识库站内互链

```bash
# 生成 64 个卦页面到 output/
python tools/gen_pages.py
```

## 🛠 技术栈

- Python 3（标准库，无第三方依赖）
- 数据驱动：一条卦数据 → 一个独立静态页
- 纯静态 HTML + CSS，可直接部署到任意静态托管

## ⚖️ 说明

- 卦辞/爻辞依据公开《周易》通行本整理。
- 内容为文化科普与传统文化研究用途，**仅供参考**，不构成任何预测或决策依据。

## 📄 License

[MIT](./LICENSE)

---

**天机推演** —— 以 AI 为桥，让易经走进当代生活。了解更多请访问 [claw-book.cn](https://claw-book.cn/)。
