# 月度仪表盘 - CHANGELOG

> 变更记录（append-only）：只新增条目，不重写历史。
> 原 `project_memory/` 的通用变更信息将逐步按粒度迁移到各自目录。

## 2026-06-02
- 初始化按粒度拆分后的 `project_memory/monthly/`，并从原 `PROJECT_STATE.md`、`TODO.md` 迁移月度相关内容（原文件保留）。

## 2026-06-04
- 更新当前月份（2026-05）月度仪表盘输出结构：按 `dashboard/monthly/YYYY-MM/` 生成 `index.html + data.csv + dashboard.png`，并更新 `dashboard/monthly/index.html` 指向当月目录。
- 「汇总（所有国家）」柱状图数值规则增强：上涨显示绿色并追加 `↑`，下跌显示红色并追加 `↓`（与字体颜色一致）。

