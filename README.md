# AI 产品开发工程师简历

> 覃涛 / Qin Tao — AI 产品开发工程师 | 现居武汉市
>
> 从数据采集到智能预测到内容营销的全链路工具栈构建
>
>【线上预览简历】https://quenteenfixed.github.io/ai-resume/resume.html
>
> 调研：
> 【长周期任务的自运转智能体，以营收利润为核心评估指标】 https://quenteenfixed.github.io/ai-resume/long-horizon/deploy.html
> 【技术方案1】：https://quenteenfixed.github.io/ai-resume/long-horizon/github-tech-plan.html
> 【技术方案2】：https://quenteenfixed.github.io/ai-resume/long-horizon/inspect-ai-tech-plan.html

## 个人信息

| | |
|---|---|
| **姓名** | 覃涛 (Qin Tao) |
| **现居** | 武汉市 |
| **学历** | 硕士研究生 |
| **GitHub** | [@quenteenfixed](https://github.com/quenteenfixed) |
| **爱好** | 足球、篮球 |

## 教育背景

- **2009.09 ~ 2012.06** — 中南大学，硕士研究生
- **2005.09 ~ 2009.06** — 中南大学，本科

## 工作经历

- **2019 ~ 至今** — 自主创业 / AI 产品开发工程师
  - 聚焦 AI 驱动的产品开发，独立设计并实现从赛事数据采集、多维度预测建模、视频自动生成到多平台内容分发的全链路自动化工具栈
- **2012.08 ~ 2019.01** — 百度上海研发中心，研发工程师
  - 参与百度核心产品研发，积累大规模系统设计、高性能工程实践和团队协作经验

## AI 开发理念

> AI 时代的开发，优先定好和想清楚需求、文档，再派发任务给 AI。

遵循 **需求先行 → 文档驱动 → AI 派发 → 验证闭环** 的开发方法论。以下是部分 AI 开发过程对话记录：

1. [足球预测系统需求与开发方案](https://share.traecontent.cn/share/HMG2OYWEE23L.T?enter_from=pc)
2. [XGBoost 足球预测系统深度设计调研](https://share.traecontent.cn/share/NOB6IMM4XI5LBX?enter_from=pc)
3. [AI 足球预测系统开发](https://share.traecontent.cn/share/6ZEUYKXO6KG7ZD?enter_from=pc)
4. [足球预测系统开发与测试](https://share.traecontent.cn/share/LI_V4YAG-_K6_D?enter_from=pc)
5. [分析系统置信度与风险因子逻辑](https://share.traecontent.cn/share/ECHF22HD5-2J5U?enter_from=pc)
6. [XGBoost 足球预测系统开发](https://share.traecontent.cn/share/HJIMIX4N4D2RQJ?enter_from=pc)

## 项目总览

独立设计、开发并部署了一套完整的"产品-推广"AI自动化流程工具栈，覆盖 **数据采集 → 智能分析 → 内容生产 → 多端分发** 全链路闭环。

| # | 项目 | 技术栈 | 仓库 |
|---|------|--------|------|
| 01 | **AIBall Solo** — 足球赛事数据分析与智能预测平台 | FastAPI + Vue 3 + PostgreSQL + Docker | [GitHub](https://github.com/quenteenfixed/aiball-solo) |
| 02 | **AIBall Auto Collect** — 多维赛事数据自动采集系统 | Node.js + Puppeteer + ES Modules | [GitHub](https://github.com/quenteenfixed/aiball-auto-collect) |
| 03 | **AIBall XGBoost** — 多维度赛事预测机器学习系统 | Python + XGBoost + scikit-learn + SciPy | [GitHub](https://github.com/quenteenfixed/aiball-xgboost) |
| 04 | **AIMap** — 基于地图的客户数据智能采集系统 | Python + Playwright + MutationObserver | [GitHub](https://github.com/quenteenfixed/aimap-ball) |
| 05 | **AIAutoVideo** — 分镜脚本自动生成视频系统 | TypeScript + React + Remotion + edge-TTS | [GitHub](https://github.com/quenteenfixed/aiautovideo) |
| 06 | **AIVideo Publish** — 多平台短视频自动发布系统 | Vue 3 + Flask + CloakBrowser + SQLite |  |

## 系统架构

```
┌─────────────────────────────────────────────────────────┐
│                    数据采集层                              │
│  ┌─────────────────────┐  ┌──────────────────────────┐   │
│  │ AIBall Auto Collect  │  │ AIMap                    │   │
│  │ Puppeteer 赛事采集   │  │ 高德地图商户线索采集      │   │
│  │ 交锋/赔率/大小球     │  │ Playwright+反检测        │   │
│  └──────────┬──────────┘  └──────────────────────────┘   │
└─────────────┼────────────────────────────────────────────┘
              ↓
┌─────────────────────────────────────────────────────────┐
│                    智能分析层                              │
│  ┌─────────────────────┐  ┌──────────────────────────┐   │
│  │ AIBall Solo          │  │ AIBall XGBoost           │   │
│  │ 六路融合预测引擎      │  │ ML预测管线               │   │
│  │ FastAPI+Vue3全栈     │  │ 分类+Poisson+比分矩阵    │   │
│  └──────────┬──────────┘  └──────────┬───────────────┘   │
└─────────────┼────────────────────────┼──────────────────┘
              ↓                        ↓
┌─────────────────────────────────────────────────────────┐
│                    内容生产层                              │
│  ┌──────────────────────────────────────────────────┐    │
│  │ AIAutoVideo                                       │    │
│  │ 分镜脚本 → 视频自动渲染                            │    │
│  │ Remotion + TTS + 逐词字幕 + ECharts图表           │    │
│  └──────────────────────┬───────────────────────────┘    │
└─────────────────────────┼────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────┐
│                    多端分发层                              │
│  ┌──────────────────────────────────────────────────┐    │
│  │ AIVideo Publish                                   │    │
│  │ 19平台一键自动发布                                 │    │
│  │ Vue3+Flask+CloakBrowser+MCP                      │    │
│  └──────────────────────────────────────────────────┘    │
└─────────────────────────────────────────────────────────┘
```

## 核心数据

- **6** 个完整产品级系统
- **19** 个平台自动分发（抖音/快手/B站/小红书/TikTok/YouTube等）
- **581** 维特征工程（XGBoost预测系统）
- **59.66%** 预测准确率，RPS 0.2106 优于所有基线模型
- **440+** 条商户线索采集（高德地图）
- **5** 套视频视觉模板 + **6** 类场景类型 + **9** 种转场效果

## 技术栈总览

### 后端开发
Python 3.11 · FastAPI · Flask · Uvicorn · SQLAlchemy · Pydantic · JWT · MCP Protocol · A2A Protocol

### 前端开发
Vue 3 · TypeScript · React 18 · Vite · Pinia · Element Plus · Tailwind CSS · ECharts · Remotion

### 机器学习 / AI
XGBoost · scikit-learn · Poisson Regression · Dixon-Coles · Isotonic Regression · ELO Rating · Optuna · Walk-Forward CV · Gemini API

### 浏览器自动化
Puppeteer · Playwright · CloakBrowser · MutationObserver · 反检测指纹隐藏 · Cookie持久化 · 拟人化操作

### 视频 / 多媒体
Remotion 4.0 · FFmpeg · edge-TTS · Lottie · ECharts · Pexels API · 逐词字幕同步

### 数据库 / 存储
PostgreSQL 15 · SQLite · JSON文件存储 · S3对象存储 · Docker Volume

### DevOps / 部署
Docker Compose · Nginx · systemd · CI/CD脚本 · 健康检查 · 镜像回滚 · Shell自动化

## 线上成品展示
1. [展示 1](https://quenteenfixed.github.io/ai-resume/showcase/aiball-index-01.png)
2. [展示 2](https://quenteenfixed.github.io/ai-resume/showcase/aiball-index-02.png)
3. [展示 3](https://quenteenfixed.github.io/ai-resume/showcase/aiball-index-03.png)
4. [展示 4](https://quenteenfixed.github.io/ai-resume/showcase/aiball-index-04.png)
5. [展示 5](https://quenteenfixed.github.io/ai-resume/showcase/aiball-match-01.png)
6. [展示 6](https://quenteenfixed.github.io/ai-resume/showcase/aiball-match-02.png)
7. [展示 7](https://quenteenfixed.github.io/ai-resume/showcase/aiball-match-03.png)

## 在线预览

https://quenteenfixed.github.io/ai-resume/resume.html

## License

MIT
