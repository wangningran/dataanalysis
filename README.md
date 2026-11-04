# Python 数据分析实战：用 A 股数据走一遍完整流程

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/wangningran/dataanalysis/blob/main/python_data_analysis_a_share.ipynb)

一节 60 分钟的 Python 数据分析技能课。用宁德时代（300750）、阳光电源（300274）的日线行情，从取数、清洗、处理、可视化一直讲到自动化流程。

## 内容

| 时间 | 部分 | 主要内容 |
|---|---|---|
| 0–5 分钟 | 摸底 | 目标与问题 |
| 5–30 分钟 | pandas / numpy | **基本概念：** ndarray 与向量化、广播、Series / DataFrame / Index、`loc` / `iloc`、清洗 / 处理 / 聚合与 split-apply-combine<br>**进阶：** 数据体检、组内填充与未来函数、收益率、SQL 窗口函数对照、`resample` 等 |
| 30–42 分钟 | 可视化 | **基本概念：** matplotlib 的 Figure / Axes、plotly express 与 graph_objects<br>**实战：** 净值与回撤、交互 K 线 |
| 42–55 分钟 | 自动化取数与处理 | **基本概念：** API 与 JSON 解析、ETL、函数化与参数化<br>**实战：** 日志、重试、增量更新、幂等写入、Excel 日报、cron / GitHub Actions 定时运行 |
| 55–60 分钟 | 练习与总结 | 课后练习、项目写法示例 |

附录是 pandas 常用操作速查表和面试常问问题。

## 怎么运行

**推荐：** 点上面的 "Open in Colab" 按钮，不用安装任何软件。打开后先运行第一个代码单元格安装依赖（去掉开头的 `#`），再选"代码执行程序 → 全部运行"。

**本地运行：**

```bash
pip install -r requirements.txt
jupyter lab
```

## 数据来源

notebook 按下面的顺序取数，任何一步失败都会自动换下一种：

1. [akshare](https://github.com/akfamily/akshare) 实时获取前复权日线，成功后保存为 `a_share_daily.csv`
2. 读取本地的 `a_share_daily.csv`
3. 生成结构相同的模拟数据（只用于演示，不是真实行情）

运行时会打印实际用的是哪一种数据。

> plotly 交互图在 GitHub 页面预览里不显示，在 Colab 或 Jupyter 中运行即可看到。
