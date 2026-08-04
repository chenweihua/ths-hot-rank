# 沪深热榜 - 股票热度排名追踪

实时追踪同花顺、东方财富、雪球等平台的股票热度排名，提供趋势分析和可视化展示。

## 功能特点

- **多平台数据整合**: 同花顺热榜、东方财富浏览排名、雪球热股
- **实时热度追踪**: 每30分钟自动更新数据
- **趋势可视化**: 股票排名变化趋势图
- **板块分析**: 热门概念板块及龙头股
- **涨停分析**: 连板天数、涨停原因

## 数据来源

- 同花顺热榜: https://eq.10jqka.com.cn/frontend/thsTopRank/index.html#/
- 东方财富: https://guba.eastmoney.com/rank/
- 雪球热股: https://xueqiu.com/hq

## 技术栈

- 前端: HTML5 + CSS3 + JavaScript + Chart.js
- 后端: Python 3.11
- 部署: GitHub Pages + GitHub Actions

## 数据更新

GitHub Actions 每30分钟自动运行数据抓取脚本，更新以下文件:

- `data/current.json` - 当前热榜数据
- `data/snapshots.json` - 历史快照数据
- `data/sectors.json` - 板块数据
- `data/sector_leaders.json` - 板块龙头股
- `data/xueqiu_hot.json` - 雪球热股数据

## 本地开发

```bash
# 安装依赖
pip install requests

# 运行数据抓取
python scripts/fetch_data.py

# 本地预览
python -m http.server 8000
```

## 访问地址

https://chenweihua.github.io/ths-hot-rank/
