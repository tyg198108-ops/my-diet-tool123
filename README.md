# 中医九种体质自测

一个可发布到 GitHub Pages 的静态网页版中医九种体质自测工具。

## 项目说明

本工具依据中华中医药学会标准《中医体质分类与判定》（ZYYXH/T157-2009）设计，包含 67 道题目，覆盖九种体质：

平和质 · 气虚质 · 阳虚质 · 阴虚质 · 痰湿质 · 湿热质 · 血瘀质 · 气郁质 · 特禀质

测试完成后，系统会根据转化分给出体质判定结果，并提供针对性的饮食建议与起居调养提示。

> **注意**：本测试结果仅供日常养生参考，不能替代医学诊断。如有明显不适，请及时就医。

## 本地预览

直接双击 `index.html` 即可在浏览器中打开使用，无需服务器。

或者使用任意静态服务器：

```bash
cd tcm-constitution-test
# Python 3
python -m http.server 8000
# 然后访问 http://localhost:8000
```

## 发布到 GitHub Pages

1. 在 GitHub 新建一个仓库，例如 `tcm-constitution-test`。
2. 将本文件夹内的全部文件上传到仓库根目录：
   - `index.html`
   - `css/style.css`
   - `js/app.js`
   - `.nojekyll`
   - `README.md`
3. 进入仓库 **Settings → Pages**。
4. 在 **Build and deployment** 中选择 **Deploy from a branch**，分支选择 `main`（或 `master`），文件夹选择 `/ (root)`。
5. 保存后稍等片刻，GitHub 会给出访问链接，例如：
   `https://你的用户名.github.io/tcm-constitution-test/`

## 技术栈

- 纯 HTML / CSS / JavaScript，无外部依赖
- 响应式布局，适配手机与桌面
- 支持键盘操作（1–5 选择选项，左右箭头切换题目）

## 自定义

如需调整题目、评分阈值或建议内容，请编辑 `js/app.js` 中的 `questions`、`constitutions` 及 `determine` 函数。

## 许可

本项目采用 MIT 协议开源，可自由用于学习、教学及非商业场景。
