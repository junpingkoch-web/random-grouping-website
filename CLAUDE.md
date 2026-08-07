# Project: random-grouping-website（随机分组工具）

零构建静态站，单文件结构（全部内联在 `index.html`，没有 `style.css`/`script.js`）。三语（zh/en/de）。
按目标组数或目标每组人数，把一份名单随机拆分成若干组。

## 文件结构
- `index.html` — 唯一核心文件
- `ads.txt` / `robots.txt` / `sitemap.xml` / `README.md` — 之前审查发现全部缺失，已补齐

## 已知的异常（跟其他 sibling 仓库不一致，尚未处理）
- **`.github/workflows/` 里有 Jekyll 构建工作流**（`jekyll-docker.yml`、`jekyll-gh-pages.yml`），
  这是 GitHub 创建仓库时的默认模板遗留，不是这个工具家族的标准做法——其他零构建仓库都是
  直接从分支根目录发布，不需要任何 Actions 工作流。这两个文件目前处于"没人主动配置但会在
  每次 push 时真实触发"的状态。是否要移除以匹配其他仓库的模式，需要你确认——改动 CI/CD
  配置不是我会擅自做的事。
- **根目录有一个被 git 追踪的 108KB 中文命名 zip 文件**（`随机分组工具...zip`），
  你之前明确表示"无所谓"，我没有动它，保持原样。

## Commands
- 无构建/测试命令
- 本地预览：共享配置 `C:\Users\junpi\.claude\.claude\launch.json`，端口 5508

## 明确禁止的事
- 不要把单文件拆成 `index.html`/`style.css`/`script.js` 三件套，除非被明确要求
- 不要擅自删除/修改 `.github/workflows/` 里的 Jekyll 工作流文件——先跟用户确认

## 部署流程
- 改完直接 commit + push 到 `main`
- Commit 作者身份：`Junping Koch <junping.koch@gmail.com>`，仓库单独设置

## 持续维护
每次你需要重复纠正 Claude 同一件事三次以上，就把结论补进这个文件对应章节。
