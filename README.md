# research-workspace

面向新科研项目、论文返修、分析重建与接续的Codex skill。核心目标：**为论文写作建立容易理解、容易审查、容易追溯的轻量工作区。**

它指导agent按科学问题建立模块，明确环境与成果复用，并让论文结论、图表和具体数值能够反查实际方法、分析样本与源数据。默认不生成哈希清单、多层audit/cache、重复总结或无用途的空目录。

## 安装

将本仓库`skills/research-workspace`目录复制到：

- Codex全局技能目录：`~/.codex/skills/research-workspace`（如自定义CODEX_HOME，则使用其skills目录）；
- 或项目技能目录：`.agents/skills/research-workspace`。

不要复制整个仓库作为技能目录。重新开启会话后调用：

```text
请使用 $research-workspace，读取我提供的架构、论文与审稿意见，
在指定路径下建立论文返修工作区。先建立模块和运行说明，不执行分析。
```

## 行为边界

- 新项目Python模块默认独立venv，R模块独立R依赖环境；接续时尊重既有环境约束，支持明确的Windows/WSL分工。
- 论文证据导航、实际Methods记录、样本流转与子图/数值来源融入现有README，不另建多套“证据包”。
- 正式分析明确干净会话运行入口；重要人工判断可追溯，关键数据表明确标识、关联关系与缺失值语义。按授权做轻量样例验证，不把目录检查当成分析复现。
- 顶层README提供总入口，每个模块一份README；目录深度按必要性控制。
- 不把计划当成果，不把旧结果复制成新分析结果。
- 初始方案允许试错、优化或停止：保留重要尝试及决策依据，区分临时探索与正式结果；不以事后选择评价标准制造成功，也不要求每次试错复制工作区。
- 不自动迁移数据、训练模型、上传论文/患者资料或发布GitHub。
- 标准README/requirements文件按完整路径唯一，科研文件使用模块编号和用途命名。

技能入口：[SKILL.md](skills/research-workspace/SKILL.md)。只有一份必要的[README模板参考](skills/research-workspace/references/workspace-template.md)，没有依赖安装器或自动执行分析的脚本。

本仓库仅包含通用技能说明，不包含任何具体项目数据、论文、审稿意见、本机路径或账户凭据。
