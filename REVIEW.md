# 博客项目审查报告（2026-03-28）

## 已落地优化

1. **修复资源链接的可移植性**
   - 将 `main.css`、`favicon` 与 `about` 页面链接统一改为 `relative_url`。
   - 好处：部署到子路径（如 `https://example.com/blog`）时，静态资源与页面链接不会 404。

2. **修复布局中的无效 HTML 结构**
   - 移除了 `_layouts/home.html` 与 `_layouts/post.html` 中嵌套在页面内容区域里的 `<head>` 标签。
   - 好处：减少 HTML 语义错误，提升浏览器兼容性与可维护性。

3. **修复首页列表语义结构**
   - 调整了首页文章列表容器，避免无意义的 `<ul>` 嵌套。
   - 好处：DOM 结构更清晰，后续样式维护成本更低。

## 建议后续改进（未在本次直接改动）

1. **依赖锁定与可复现构建**
   - 当前缺少 `Gemfile.lock`，建议在可访问 RubyGems 的环境中执行 `bundle install` 后提交锁文件。

2. **前端第三方脚本的安全与性能**
   - `highlight.js`、MathJax、Google Analytics 均走外链，可考虑：
     - 增加 SRI（Subresource Integrity）；
     - 将关键资源本地化或延迟加载策略细化。

3. **配置项环境化**
   - `G-E9RDYFK5CS` 这类统计 ID 建议通过 `_config.yml` 配置项注入，避免主题代码硬编码。

4. **内容质量自动检查**
   - 增加 CI（如 GitHub Actions）执行：
     - `bundle exec jekyll build`（构建检查）
     - Markdown lint（写作规范）
     - HTMLProofer（死链检查）

5. **SEO 与内容分发**
   - 已启用 `jekyll-feed`、`jekyll-seo-tag`、`jekyll-sitemap`，建议补充：
     - `robots.txt`；
     - 社交分享图（Open Graph image）的统一策略。

