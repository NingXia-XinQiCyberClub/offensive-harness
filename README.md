# offensive-harness

面向**授权渗透测试、攻防演练与 CTF 竞赛**的统一编排与自动化 harness。

本仓库由宁夏大学鑫启网安俱乐部（[NingXia-XinQiCyberClub](https://github.com/NingXia-XinQiCyberClub)）发起，目标是给零散的探测脚本、利用工具与结果整理流程提供一个共用的外壳：一处定义目标与任务，按统一接口调度各环节，并输出结构化的过程记录与报告。

> 本项目仅用于合法授权的安全测试与教学研究。使用前请确认你已获得目标所有者的明确书面授权，并遵守所在地法律法规。

---

## 一、当前状态

**规划中。** 仓库尚未进入实现阶段，技术栈亦未确定。

| 项目 | 状态 |
| :-- | :-- |
| 项目定位与范围 | 讨论中 |
| 技术栈选型 | 待定 |
| 代码实现 | 无 |
| 可用版本 | 无 |

现阶段仓库仅包含本文件、[LICENSE](LICENSE) 与 `.gitignore`。关于架构与选型的讨论将在 [Discussions](https://github.com/NingXia-XinQiCyberClub/.github/discussions) 中进行，结论会回写到本文件。

---

## 二、计划中的能力

以下为设想中的能力边界，**均未实现**，仅用于说明项目方向。

| 能力 | 说明 |
| :-- | :-- |
| 模块化插件 | 探测、利用、后渗透、信息整理等环节以插件形式接入，通过统一接口注册与发现，便于单独开发与替换 |
| 任务编排 | 以声明式配置描述任务与依赖关系，支持串行、并行与条件分支，失败可重试、可中断 |
| 多目标 / 多任务管理 | 统一维护目标清单与任务队列，支持分组、并发限流与进度追踪 |
| 报告生成 | 将执行记录、中间产出与发现项汇总为结构化报告，支持导出为 Markdown / JSON 等格式 |
| 可扩展接口 | 对外提供稳定的调用接口，便于与自有平台、CI 流程或其他工具链集成 |
| 过程可追溯 | 完整记录每一步的输入、输出与时间戳，便于复盘与审计 |

选型需要权衡的方向包括：实现语言（Python 生态成熟、Go 分发方便）、插件隔离方式（进程内调用还是独立进程）、配置格式与报告模板。这些会在确定技术栈时一并讨论。

---

## 三、目录结构

当前仓库内容如下：

```
offensive-harness/
├── README.md      # 本文件
├── LICENSE        # MIT 协议
└── .gitignore     # 通用忽略规则
```

代码、文档与测试目录将在确定技术栈后补充。

---

## 四、贡献方式

目前处于规划阶段，最有价值的参与方式是参与方案讨论：技术栈选择、插件接口设计、报告格式等都可以在 Discussions 中提出。

进入实现阶段后，请遵循组织统一的协作规范：

| 文件 | 用途 |
| :-- | :-- |
| [CONTRIBUTING.md](https://github.com/NingXia-XinQiCyberClub/.github/blob/main/CONTRIBUTING.md) | 分支模型、提交信息规范、变更请求流程 |
| [CODE_OF_CONDUCT.md](https://github.com/NingXia-XinQiCyberClub/.github/blob/main/CODE_OF_CONDUCT.md) | 成员行为准则 |
| [SECURITY.md](https://github.com/NingXia-XinQiCyberClub/.github/blob/main/SECURITY.md) | 安全缺陷上报流程，**不得通过公开工单披露** |
| [SUPPORT.md](https://github.com/NingXia-XinQiCyberClub/.github/blob/main/SUPPORT.md) | 提问规范与响应时限 |

上述文件由组织级 [.github](https://github.com/NingXia-XinQiCyberClub/.github) 仓库统一维护，适用于包含本仓库在内的全部组织仓库。

---

## 五、License

本项目采用 [MIT](LICENSE) 协议，Copyright (c) 2026 VioLina。
