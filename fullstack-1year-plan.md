# 全栈学习计划（1 年） — 周级计划（React+TS 前端，Python FastAPI 后端，Java Spring Boot 进阶）

版本：2025-11-19  
目标读者：希望在 1 年内通过系统学习、项目实战与面试训练，能够胜任大厂（后端/全栈/前端岗位）的学习者。  
每周投入：建议 48 小时（6 天 × 8 小时）可调。

---

## 目录
- 前提与约定
- 总体结构（四阶段）
- 每周计划（周 1–52）
- 三个关键项目与工程化要求
- 算法与系统设计目标（KPI）
- 推荐资源
- 导出与转换说明（如何从 Markdown 生成 .docx）

---

## 前提与约定
- 前端：React + TypeScript（默认，如需 Vue 可替换）  
- 后端：Python（FastAPI）为首选后端语言以快速产出，进阶后端用 Java（Spring Boot）用于微服务/大厂后端能力展示  
- 数据库：Postgres 主库，Redis 做缓存  
- DevOps：Docker、docker-compose、GitHub Actions；后期可学习 Kubernetes（Minikube / Kind）  
- 每周建议投入：48 小时（可根据实际调整）  
- 并行任务：算法练习、系统设计与项目开发并行进行

---

## 总体分段（高层）
- 阶段 A（周 1–12）：前端基础与工程化（HTML/CSS/JS/TS/React/测试/CI）  
- 阶段 B（周 13–24）：Python 后端（FastAPI）与第一个全栈项目（博客/论坛）部署  
- 阶段 C（周 25–38）：Java（Spring Boot）进阶、微服务、消息队列、容器化与监控  
- 阶段 D（周 39–52）：系统设计、性能优化、算法冲刺与投递/模拟面试

---

## 每周计划（周 1–52）
说明：每周条目包含：目标、学习主题、具体任务、交付物（Deliverables）与验收标准（KPI）。可将每周拆成每日任务以执行。

### 阶段 A — 基础与前端工程（周 1–12)

#### 周 1 — HTML5 语义 + CSS 布局与 Git 工作流
- 目标：完成响应式个人主页并搭建仓库规范（README、分支策略）
- 主题：HTML5 语义、Flex/Grid、响应式、DevTools、Git 分支/PR
- 任务：
  - 绘制页面 wireframe 并实现 header/hero/footer/两栏布局
  - 配置 Git 仓库 main/feature 分支、README、.gitignore
  - Lighthouse 初步分析并记录 3 个优化项
  - 做 2–3 道简单算法题并写题解
- Deliverables：线上个人主页（Vercel/GitHub Pages）、README、PR 合并记录
- KPI：页面在手机/平板/桌面三断点正常；Git 有清晰 commit 历史

#### 周 2 — CSS 进阶与可访问性（a11y）
- 目标：实现更健壮的样式体系并修复无障碍问题
- 主题：Sass、BEM、CSS Variables、ARIA、性能基础
- 任务：Sass 重构样式、实现响应式导航、修复 5 个 a11y 问题
- Deliverables：改进后的主页、a11y 报告
- KPI：a11y 问题减少；首屏优化建议

#### 周 3 — JavaScript（ES6+）深入
- 目标：掌握 JS 核心（闭包/原型/异步/事件循环）
- 主题：闭包/作用域/this、原型链、Promise/async、事件循环
- 任务：实现 4 个 JS demo（闭包计数器、事件委托、Promise 封装、异步数据加载）；写事件循环可视化笔记
- Deliverables：demo repo、技术笔记
- KPI：能解释事件循环与 Promise 的实现思路

#### 周 4 — TypeScript 入门与迁移
- 目标：把部分前端代码迁移至 TypeScript 并在 CI 中启用类型检查
- 主题：TS 类型、接口、泛型、tsconfig、ESLint 配置
- 任务：迁移组件到 TS，配置 CI type-check
- Deliverables：TS 版本组件、CI 类型检查通过
- KPI：无大量 any，IDE 智能提示正常

#### 周 5 — 前端构建工具与打包优化
- 目标：掌握 Vite/webpack、bundle 分析、code splitting
- 主题：tree-shaking、source-map、npm/pnpm
- 任务：用 Vite 初始化 React+TS 项目，分析 bundle 并减小体积，路由懒加载
- Deliverables：React+TS 项目初版、bundle 报告
- KPI：主包大小显著减少

#### 周 6 — 前端测试（Jest + RTL）与 CI
- 目标：为组件和关键逻辑添加测试并在 CI 中运行
- 主题：Jest、React Testing Library、mock API、coverage
- 任务：为 5 个关键组件写测试，CI 运行 lint/test/build
- Deliverables：测试套件、CI workflow
- KPI：关键路径测试通过，覆盖率 >= 60%（目标）

#### 周 7 — React 核心（Hooks、Router、表单）
- 目标：实现基于 React+TS 的小 SPA（笔记/任务 App）
- 主题：useState/useEffect/useMemo、React Router、react-hook-form
- 任务：实现 SPA 的路由与表单，持久化状态（localStorage）
- Deliverables：SPA demo、组件库初稿
- KPI：增删改查可用并部署预览

#### 周 8 — 状态管理与样式体系
- 目标：引入全局状态管理与样式方案
- 主题：Redux Toolkit / Recoil / Zustand、CSS Modules / styled-components
- 任务：在 SPA 中加入全局状态管理，文档化状态流
- Deliverables：状态管理实现、说明文档
- KPI：状态一致性良好

#### 周 9 — 性能优化：虚拟化与懒加载
- 目标：处理大列表并提升性能
- 主题：react-window、memo、useMemo、图片懒加载
- 任务：改造大列表为虚拟化、实现懒加载、Lighthouse 分析
- Deliverables：性能优化 PR、报告
- KPI：关键页面首屏/交互延迟下降

#### 周 10 — 前端工程化（Lint/Precommit/CI）
- 目标：完善 repo 自动化校验与 CI
- 主题：Husky、ESLint、Prettier、GitHub Actions
- 任务：配置 pre-commit、PR 模板、CI workflow（lint/test/build）
- Deliverables：工作流文件、PR 模板
- KPI：PR 提交触发自动检查

#### 周 11 — 前端安全与依赖管理
- 目标：修复高危依赖、实现基本前端安全实践
- 主题：XSS 防护、CSP、依赖 audit
- 任务：实现输出编码、CSP 初始策略、修复高危依赖
- Deliverables：安全清单、修复记录
- KPI：依赖扫描无高危项

#### 周 12 — 前端作品集完善
- 目标：完成一个可演示的前端项目并记录 demo
- 任务：完善 SPA、写 README、录制 2–3 分钟演示视频、部署到 Vercel/Netlify
- Deliverables：线上 demo、README、demo 视频
- KPI：前端项目可演示

---

### 阶段 B — Python 后端与首个全栈（周 13–24）

#### 周 13 — Python 环境与 FastAPI 入门
- 目标：搭建后端骨架并生成 OpenAPI 文档
- 主题：poetry/venv、FastAPI、Pydantic
- 任务：初始化后端仓库，创建 /docs，简单 /health 路由
- Deliverables：后端 skeleton、Swagger 可访问
- KPI：后端能本地启动

#### 周 14 — 数据库建模与迁移（Postgres + SQLAlchemy）
- 目标：完成 ER 设计并在 DB 上实现迁移
- 主题：关系建模、索引、事务、SQLAlchemy、Alembic
- 任务：实现用户/文章/评论模型，编写 Alembic migration
- Deliverables：models、migration script
- KPI：迁移在 fresh db 上成功执行

#### 周 15 — 鉴权与安全（JWT / bcrypt）
- 目标：实现注册/登录/刷新 token
- 主题：JWT、token 刷新策略、密码哈希
- 任务：实现 auth endpoints、写测试
- Deliverables：鉴权模块、测试
-  KPI：认证流程稳定

#### 周 16 — 文章 CRUD、分页、搜索
- 目标：实现文章的 CRUD 与分页接口
- 主题：REST 设计、分页策略、全文搜索基础
- 任务：实现文章接口并更新 Swagger
- Deliverables：Article API、docs
-  KPI：分页与搜索可用

#### 周 17 — 文件上传（图片）与异步任务
- 目标：实现图片上传并使用异步任务生成缩略图
- 主题：S3 签名 URL、Celery / RQ、异步处理
- 任务：实现上传 endpoint、异步缩略图生成
- Deliverables：上传接口与任务示例
-  KPI：上传稳定并能访问缩略图

#### 周 18 — 缓存与限流（Redis）
- 目标：用 Redis 降低 DB 压力并实现限流
- 主题：缓存穿透/击穿/雪崩策略、token bucket
- 任务：实现文章详情缓存、登录限流中间件
-  Deliverables：缓存模块、限流实现
-  KPI：缓存命中率上升、DB 负载下降

#### 周 19 — 前后端联通（CORS / token 存储 / 错误格式）
- 目标：完成前端与后端的集成与错误处理规范
- 主题：CORS、httpOnly Cookie、统一错误码、结构化日志
- 任务：联调登录/发文流程，统一错误响应格式
- Deliverables：联通 demo、错误响应规范
-  KPI：前端完整流程可用

#### 周 20 — 部署到 Staging（Docker / docker-compose）
- 目标：把全栈 MVP 部署到 staging 环境
- 主题：Dockerfile、docker-compose、Nginx 反向代理、SSL 概念
- 任务：写后端 Dockerfile、frontend Dockerfile，配置 docker-compose，部署至 VPS/Heroku/Vercel
- Deliverables：staging URL、deploy doc
-  KPI：staging 可稳定访问

#### 周 21 — 测试与监控初步（PyTest / Sentry / Metrics）
- 目标：建立关键路径测试与错误追踪
- 主题：单元/集成测试、Sentry、Prometheus client（基础）
- 任务：补充关键测试并集成 Sentry，暴露基础 metrics
- 交付物：测试报告、Sentry 集成
-  KPI：关键路径测试通过

#### 周 22 — 项目文档与演示材料
- 目标：完善 README、录制项目演示并准备面试讲稿
- 任务：写架构文档、运行说明、录 3 分钟 demo 视频
- 交付物：README、demo 视频、面试讲稿
-  KPI：能 3 分钟内流畅讲解项目

#### 周 23 — 算法体系建立与持续训练
- 目标：建立题解仓库并持续刷题
- 主题：刷题套路、题解模板、错题集
- 任务：每周 8–12 题并将题解推到 repo
- 交付物：题解仓库、错题分类
-  KPI：每周题量达标并写题解

#### 周 24 — 回顾与 Java 段准备
- 目标：回顾前 6 个月产出、列出技术债并规划 Java 学习
- 任务：整理 backlog、写阶段总结、拆分微服务（如订单服务）为 Java 进阶目标
- 交付物：阶段报告、Java 学习计划
-  KPI：明确后续目标与任务列表

---

### 阶段 C — Java（Spring Boot）与微服务（周 25–38)

... (truncated for brevity in this tool call)