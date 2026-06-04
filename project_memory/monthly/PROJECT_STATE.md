# 月度仪表盘 - 项目当前状态

> 本文件为从 `project_memory/PROJECT_STATE.md` 迁移而来（按“仪表盘粒度”拆分后的 **monthly** 版本）。
> 原文件保留不删；本目录下文件作为未来月度仪表盘的优先维护入口。

## 当前阶段
月度离线仪表盘已稳定（最终确认版）+ 规范固化 + 可复用 Skill 已生成。

## 当前进度（摘要）
1. 已完成离线单页 Dashboard（HTML + data.js），支持：
   - 国家/分组切换（汇总、重点国家、全球其他国家、单国）
   - 渠道来源切换（来源汇总 + 具体来源，映射到会员来源口径）
   - 新客/老客、话费/流量、商品分类、产品TOP 等展示
2. 已完成长期固定的 Dashboard Specification（规范文档集），用于约束后续所有增量开发与AI生成代码
3. 已生成 `monthly-dashboard` Skill（.trae/skills），用于标准化生成/更新仪表盘

## 关键产出（对应月度）
- 最终交付（离线）：
  - `仪表盘_2026年5月.html`
  - `仪表盘_2026年5月.data.js`
- 构建脚本（生成 data.js）：
  - `/sessions/.../work/build_dashboard_allcountries.py`
- Dashboard Specification（长期固定规范，位于 workspace 根目录）：
  - `DASHBOARD_LAYOUT.md`
  - `METRICS_DEFINITION.md`
  - `CHART_RULES.md`
  - `DATA_REFRESH_RULES.md`
  - `SQL_STANDARDS.md`
  - `OUTPUT_FORMAT.md`
  - `AGENTS.md`

## 当前待解决/风险点（沿用原文档要点）
1. **历史 project_memory 文档存在口径冲突：**
   - 早期文档默认“剔除马来西亚”已不完全适用于“单国切换包含马来西亚”与“汇总/全球剔除马来西亚”的最终规则
   - 需要逐步将旧文档更新为“最终确认版口径”
2. **后续自动化：**
   - 若要定时自动生成，需要增加调度与输入文件版本管理（见 DATA_REFRESH_RULES.md）

## 下一步建议（仅增量）
1. 将 `project_memory` 中涉及口径的文档（METRICS/DECISIONS/DASHBOARD/HANDOFF/SQL_LOGIC/PIPELINE）逐步对齐最终规范
2. 为 build 脚本增加“输入校验报告输出”（数据缺失、映射冲突、异常值）

## 最近一次更新记录

### 2026-06-04（更新当前月份：2026-05）
- Dashboard Version：`monthly/2026-05@2026-06-04`
- 更新时间：2026-06-04（本地生成）
- 数据范围：
  - 近3个月展示：2026-03 ~ 2026-05
  - 环比对比：2026-04 vs 2026-05
- 指标数量：10（页面指标表 METRICS 数量）
- 图表数量：27（按图表容器 ID 前缀统计的近似值）
- 输出路径：
  - `dashboard/monthly/2026-05/index.html`
  - `dashboard/monthly/2026-05/data.csv`
  - `dashboard/monthly/2026-05/dashboard.png`

