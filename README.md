# 招聘最后交接（recruitment-handover）

本仓库是一次性完整交接包，包含**两部分**：

| 部分 | 位置 | 是什么 |
|---|---|---|
| ① 招聘系统真实代码 | `zhipin-mvp/` | **智聘·招聘管理系统**（Python Flask 后端 + 前端 + Agent 能力），可二次开发 |
| ② AI 视频方法论笔记 | 根目录 3 份 md | 原作者转行 AI 视频/短剧的方法论（与代码无关，独立阅读） |

---

## ① zhipin-mvp —— 招聘系统代码

| 项 | 内容 |
|---|---|
| 技术栈 | 后端 Python Flask + SQLAlchemy；前端 React + Vite（`frontend/`、`readdy-frontend/`）；Agent 框架 `base_agent/` |
| 入口文档 | `zhipin-mvp/README.md` → `QUICKSTART.md`（跑起来）→ `AGENTS.md`（给 AI 的开发约定）→ `docs/` |
| 配置 | 复制 `backend/.env.example` 为 `backend/.env` 填自己的 key（**仓库不含任何真实密钥**，LLM key、JWT secret 都需自配） |
| 代码快照日期 | 2026-07-24（此后公司仓库可能有更新，以本快照为准做二次开发） |
| 数据 | 默认 SQLite，开箱即用；可配 MySQL |

### 给 AI 的接管提示词（整段复制）

```
克隆 https://github.com/hl13544175837-coder/recruitment-handover 到本地。
这是一个招聘系统的交接仓库：真实代码在 zhipin-mvp/ 目录（Python Flask 后端 + React 前端）。
按顺序读：zhipin-mvp/README.md → QUICKSTART.md → AGENTS.md → backend/.env.example，
然后帮我在本地把后端和前端跑起来。仓库不含真实密钥，需要我提供 LLM API key。
根目录的 3 份 md 是另一个方向的笔记（AI 视频方法论），与代码无关，先不用管。
跟我说话用大白话 + 表格 + 短句。
```

---

## ② AI 视频方法论笔记（与代码无关）

| 文件 | 是什么 |
|---|---|
| `招聘系统最后交接-本地备份.md` | ⭐ 交接主文档（Agent 自包含上下文，12 章） |
| `AI视频-Agent协作手册.md` | 5 核心词 / 万能公式 / 资源地图 / 6 个 Prompt 模板 / 爆款拆解库 16 字段表 |
| `会话交接-上下文整理.md` | 方法论推导过程、环境故障记录、未完成事项 |

如果你是为**招聘系统代码**而来，这部分可以忽略。它是原作者转行 AI 视频/短剧的方法论沉淀，主线任务是「拆解 AI 短剧 → 建爆款拆解库」，详见交接主文档。

---

## 安全说明

- 本仓库**不含任何账号、密码、API 密钥、token**（已全量扫描，密钥均为占位符）
- 代码内含原公司内网环境地址（Apollo/测试库 IP，公网不可达），仅作历史参考
- 真实配置（`backend/.env`）从未入库，接手者需自行创建

## License

[MIT](LICENSE) —— 任何人可自由使用、修改、分发。
