# Minglu Sun · 个人网站

## 文件夹里有什么

```
index.html        整个网站（所有页面、交互和文字都在这里）
images/           About 页照片、论文 Figure 1
papers/           论文 PDF
cv.pdf            CV
og-image.png      链接预览图（发链接时显示的卡片）
.nojekyll         让 GitHub Pages 原样发布文件，不要删
```

## 第一次部署（GitHub Pages）

1. 登录 GitHub，右上角 **+ → New repository**。
2. Repository name 填 **`ooodddee.github.io`**（必须和你的用户名完全一致），选 **Public**，点 **Create repository**。
3. 在新仓库页面点 **uploading an existing file**，把这个文件夹里的**所有内容**拖进去（是文件夹里面的东西，不是文件夹本身；`images/`、`papers/` 两个文件夹也要一起拖）。点 **Commit changes**。
4. 进入仓库的 **Settings → Pages**：Source 选 **Deploy from a branch**，Branch 选 **main**、文件夹选 **/ (root)**，点 Save。
5. 等一两分钟，打开 **https://ooodddee.github.io** 就能看到网站。

> 如果上传时 `.nojekyll` 没有显示出来也没关系，可以在仓库里点 **Add file → Create new file**，文件名写 `.nojekyll`，内容留空，直接提交。

## 以后怎么改

**改文字**：在 GitHub 上打开 `index.html` → 右上角铅笔 ✏️ → 用 Ctrl/Cmd + F 搜索要改的那句话 → 改引号或标签里的文字 → **Commit changes**。约一分钟后网站更新。

**换 CV / 论文 PDF**：仓库里 **Add file → Upload files**，上传同名文件（`cv.pdf` 或 `papers/knowing-is-not-telling.pdf`）覆盖即可，不需要改代码。

**常见修改在 index.html 里搜这些词：**

| 想改什么 | 搜索 |
|---|---|
| 首页 News | `class="news"` |
| 项目的问题、状态、Key finding | 项目名，例如 `Ranked Last` |
| Research Agenda 页 | `id="agendaView"` |
| About 布告栏的便签 | `const LOG=[` |
| 布告栏照片对应哪张图 | `const PH=` |
| 三个一分钟故事的每页文字 | `const STEPS=[` |

**加一张布告栏便签**：在 `const LOG=[` 下面复制一行，改 `when`（日期）、`where`（地点）、`what`（一到两句话）。如果有照片，把照片上传到 `images/`，在 `const PH=` 里加一行名字和路径，再在便签里写 `photos:['名字']`。

**加照片注意**：照片先压缩到宽边 1000 像素左右再上传，网页会快很多。

## 绑定自己的域名（可选）

买好域名后，在 **Settings → Pages → Custom domain** 填入域名，再按 GitHub 提示在域名商那里加 DNS 记录。之后把 `index.html` 里两处 `https://ooodddee.github.io/og-image.png` 改成新域名，链接预览图才会正确显示。

## 别忘了

CV 顶部还写着占位的 `yourwebsite.com`，部署后改成 `https://ooodddee.github.io`。
