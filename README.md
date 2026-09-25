# Prove Statistics, Machine Learning, and Probability Theorems

面向统计学、机器学习理论与概率论的 Codex 定理证明 skill。支持证明、反证、补全引理、修复证明、推导界与审查论证，强调精确假设、多路线探索和对抗性审查。

A reusable Codex skill for rigorous theorem development in statistics, machine learning theory, and probability, with explicit assumptions, diverse proof routes, counterexample search, and adversarial auditing.

## 来源与改造

这个 skill 于 2026 年 7 月 15 日根据作者提供的 `cdc_prompt.pdf` 改造而成。它将原 prompt 中的多路线探索、动态分工、持续研究与独立审查思路，整理成可以反复调用的统计学、机器学习和概率论证明工作流。

改造后的核心要求包括：

- 固定原命题的量词、假设、概率模式和常数依赖，逐项记录证明义务。
- 探索机制不同的证明路线，并主动寻找反例。
- 在运行环境允许时分派有明确边界的子任务；否则按顺序完成独立检查。
- 在合并引理前核对假设、零测集、滤过、常数和极限顺序。
- 明确区分完整证明、反证、条件证明和部分结果，不把数值验证或未解决的归约当成证明。

仓库包含改写后的 skill；`cdc_prompt.pdf` 原文件不在其中。该 skill 不预设目标命题必然为真，也不承诺固定研究时长。模型和推理强度由运行环境选择，skill 本身不锁定某个模型。

## 安装

使用默认 Codex 技能目录时，可直接克隆本仓库。仓库根目录就是 skill 目录。

Windows PowerShell：

```powershell
git clone https://github.com/zdacongming-glitch/prove-stat-ml-probability-theorems.git "$env:USERPROFILE\.codex\skills\prove-stat-ml-probability-theorems"
```

macOS / Linux：

```bash
git clone https://github.com/zdacongming-glitch/prove-stat-ml-probability-theorems.git ~/.codex/skills/prove-stat-ml-probability-theorems
```

已有同名 skill 时，先将仓库克隆到其他目录，再比较或合并需要更新的文件。安装后在 Codex 新任务中调用此 skill；如技能列表尚未刷新，可重启客户端。

## 使用示例

提供完整命题、已知假设、允许引用的结果，以及希望得到的结论。

```text
请使用 $prove-stat-ml-probability-theorems 证明下面的定理。
先明确所有假设和量词，检查命题是否成立，再给出证明并做对抗审查。
定理：……
```

```text
请使用 $prove-stat-ml-probability-theorems 检查下面的学习理论证明。
定位第一个未被证明的步骤，核查数据依赖与概率界；能修复则给出完整修复，
不能修复则说明精确缺口或构造反例。
证明：……
```

```text
请使用 $prove-stat-ml-probability-theorems 判断下面的概率论命题是否正确。
尝试不同证明路线，优先检验边界情形和最弱允许分布。
命题：……
```

## 文件说明

| 文件 | 作用 |
| --- | --- |
| [SKILL.md](SKILL.md) | 触发描述、执行约束、八步工作流及结果分类 |
| [agents/openai.yaml](agents/openai.yaml) | Codex 显示名称、简短描述和默认调用提示 |
| [references/proof-protocol.md](references/proof-protocol.md) | 假设台账、证明义务、路线登记、综合与退出条件 |
| [references/domain-routes.md](references/domain-routes.md) | 概率论、统计学与机器学习理论的证明方法目录 |
| [references/adversarial-audit.md](references/adversarial-audit.md) | 逻辑、可测性、依赖、常数、渐近和边界情形的检查清单 |

## 结果分类

| 状态 | 含义 |
| --- | --- |
| Complete proof | 所有证明义务已关闭，并通过审查 |
| Disproof | 找到满足全部假设且违反结论的反例 |
| Conditional proof | 结论依赖明确标出的额外假设或外部猜想 |
| Partial result | 给出已严格证明的部分和精确的未解决步骤 |

这些标签用于约束论证和报告方式。最终证明仍需逐步核验；工作流检查本身不构成数学正确性的证书。
