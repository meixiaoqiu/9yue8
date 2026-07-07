# 9月8

这是一个基于 Hugo 的静态个人网站，用于写作、发布文章和展示个人内容。

## 本地预览

如果 Hugo 已加入系统 `PATH`，使用：

```powershell
hugo server -D
```

发布前建议执行一次生产构建检查：

```powershell
hugo --gc --minify
```

当前配置使用 `PaperMod` 主题，并通过 Git submodule 固定来源。首次克隆仓库时建议使用：

```powershell
git clone --recurse-submodules https://github.com/meixiaoqiu/9yue8.git
```

如果已经普通克隆仓库，再执行：

```powershell
git submodule update --init --recursive
```

## 开源边界

- 网站代码、Hugo 配置、模板和样式可以作为公开仓库维护。
- `content/` 下的文章内容保留作者版权。
- `static/`、文章配图和原创素材保留作者版权。
- 未经许可，不得转载文章、复用图片或复用原创素材。
- 如果后续要给代码单独采用 MIT、Apache-2.0 等许可证，请同时保留上述内容和素材版权边界。

## 日常写作与安全检查

日常写文章时，把私有草稿、私人笔记、原图、备份和部署资料放在 `.gitignore` 已排除的目录中，例如 `_private/`、`drafts/`、`private-notes/`、`raw-images/`、`backup/`。

以下情况建议重新做一次安全检查：

- 第一次开源前
- 修改主题或升级主题前后
- 加入第三方 JavaScript、统计、评论、广告、字体或 CDN 时
- 新增或修改 GitHub Actions 时
- 修改依赖、构建流程或部署流程时
- 重大发布前
