# Gold Price Prediction

基于宏观经济因素的每日黄金价格预测项目，使用 Claude Code 的 Prompt-Driven 模式运行。

## 项目简介

本项目通过分析实际利率、央行购金行为、ETF 资金流向、交易时段特征等宏观因素，生成 7 日黄金价格预测报告。

## 项目结构

```
predict/                              — 每日预测报告 (markdown)
.claude/
  ├── commands/predict.md             — /predict 命令定义
  └── skills/gold-price-analysis/     — 黄金分析框架 (4步决策模型)
CLAUDE.md                             — Claude Code 项目说明
```

## 使用方式

### 前置要求

- 安装 [Claude Code](https://github.com/anthropics/claude-code)

### 生成预测报告

1. 在项目目录下启动 Claude Code：
   ```bash
   cd Gold-Price-Prediction
   claude
   ```

2. 输入 `/predict` 命令，Claude 会自动：
   - 搜索最新市场数据（国际金价、上海金、美元指数、GLD 持仓等）
   - 基于 4 步分析框架生成预测
   - 保存报告到 `predict/` 目录

## 预测报告内容

每份报告包含：
- 当前市场数据汇总
- 4 步框架分析（实际利率、央行购金、ETF 流向、交易时段）
- 7 日价格预测区间
- 本周关键事件
- 风险提示
- 操作建议

## 分析框架

`.claude/skills/gold-price-analysis/SKILL.md` 定义了核心分析方法：

**黄金 4 步决策模型**：
1. **实际利率趋势** - 联邦基金利率 - 核心 PCE，下降看多
2. **央行购金行为** - 世界黄金协会数据，净买入看多
3. **ETF 资金流向** - GLD 持仓变化，增持看多
4. **交易时段特征** - 美盘主导=机构认可，亚盘主导=散户 FOMO

详细框架还包含铜价分析、金铜比阈值、风险管理等内容。

## 免责声明

本项目生成的预测报告仅供参考，不构成投资建议。投资有风险，决策需谨慎。

## License

[MIT](LICENSE)
