# career-data

我获得了大家梦寐以求的大厂身份，却过的不开心，到底哪里出了问题？

悬着的心落下，终于死掉了，进了公司。

这是一个人公开记录自己职业和收入变化的仓库。起点是 2026 年 10 月，一份工资，记为 1.0x。目标是 10x。过程公开：日志、决策、每个月的收入倍数和结构。做到了，这里就是证据；没做到，这里就是复盘材料。

它不是励志文，是一套可以照抄的方法。你 fork 一份，把我的数字换成你的，就能开始。

## 方法

一个月一个循环，五步：

1. **记录**：发生了什么就写进 `career-log.md`，一条一个日期一件事，只追加不改写。
2. **账本**：`income/` 按月记收入相对基线的倍数和各来源占比。10 倍是用这个数衡量的，不是用感觉。绝对数字、公司名、没宣布的计划放你自己的私有仓库。
3. **决策**：要跟踪几个月以上的事，在 `decisions/` 立一个文件，写清前提、备选、理由和检查日期。
4. **执行**：当前工作在 `employment/`，职责、成果、薪资、感受分开写。
5. **复盘**：月底按 `modes/review.md` 问四个问题，答案追加到账本和决策文件里。

## 目录

| 路径 | 内容 |
|------|------|
| `career-log.md` | 职业日志，只追加 |
| `income/<year>.md` | 收入账本，按月按来源 |
| `employment/<company>.md` | 每段工作一个文件 |
| `decisions/<yyyy-mm>-<slug>.md` | 每个长期决策一个文件 |
| `modes/review.md` | 月度复盘的固定问题 |
| `modes/interview-prep.md` | 面试前准备：从 JD 生成准备手册的方法，手册本身放私有仓库 |
| `modes/interview-review.md` | 面试后复盘与结果追踪：表现复盘和雇主结果分开，结果只认已发生的下一步动作 |
| `scripts/`、`templates/`、`tests/` | 复盘打分和结果追踪脚本、输入模板与测试，`npm test` 运行 |
| `AGENTS.md` | 给 AI Agent 的写入规则，Claude Code / Codex 进目录就会读 |

## 怎么用

```
git clone https://github.com/luochen211/career-data my-career
cd my-career
# 删掉我的记录，保留结构和规则
rm career-log.md income/*.md
```

然后在这个目录里打开你的 AI Agent，说"记一条日志"或"做本月复盘"，它会按 `AGENTS.md` 的规则写到对应文件。拿到面试时，把 JD 贴给它，说"按 interview-prep 做面试前准备"；面试结束后，把文字记录给它，说"按 interview-review 复盘"。

## 配套

找工作那一段用 [career-ops](https://github.com/luochen211/career-ops)。它负责扫岗、评估、定制简历、投递跟踪；这个仓库负责拿到工作之后的事。两者的数据可以分开放，投递记录含联系人信息，应保持私有。
