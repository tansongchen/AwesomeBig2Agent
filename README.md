# 「神算子」：基于极小极大化算法的 Big2 纸牌游戏智能体

「神算子」是 2020 年春季学期环境科学与工程学院《数据结构与算法》课程大作业中本组（成员为：程国洋、戚博闻、谭淞宸、周泽堃）提交的 Big2 纸牌游戏智能体。

## 特性

- 使用动态规划实现出牌算法；
- 使用极小极大化算法和 α-β 剪枝进行精确解的求算；
- 使用效用估计函数和迭代深入搜索进行近似解的求算。

详细介绍参见 `doc/` 目录下的报告和演示文稿。

## 结构

- `src/dealer.py` 和 `src/big2.py` 是游戏框架文件，由老师和助教提供；
- `src/Team1.py` 和 `src/Team2.py` 是由老师和助教提供的智能体示例，其中 `Team1` 只会出单牌，`Team2` 为人工。
- `src/awesome.py` 是「神算子」智能体；
- `src/smart.py` 是「智多星」智能体。
- `test/` 中包含各种测试文件。

## 使用

「神算子」使用 Python 3 编写，包含一个源代码文件（`awesome.py`），其中使用了 Python 3 的内建模块 `time` 和 `itertools`。「神算子」在 macOS 10.15.4 (Python 3.8.2, 64 位) 和 Red Hat Enterprise Linux Server 6.5 (Python 3.8.3, 64 位) 上实测均能成功运行，理论上在任何 64 位、Python >= 3.5 的环境中均可运行。在总计三千余局的测试中，「神算子」最大内存占用为 100 MB，但由于对手对内存的使用情况不同，实际内存占用可能高于此值。

首先下载或克隆本仓库，进入 `AwesomeBig2Agent` 目录，输入

```bash
python3 src/big2.py -a awesome -d smart -g 120
```

即可体验。其中，`-a awesome` 表示由「神算子」作先手，`-d smart` 表示由「智多星」作后手，`-g 120` 表示选择内置的第 120 个牌局（牌局数据文件在 `test/benchmark.in` 文件中）。
