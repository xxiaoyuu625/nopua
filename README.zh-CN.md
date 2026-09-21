<p align="center">
  <img src="assets/hero.png" alt="NoPUA — 以智慧代替鞭子" width="800">
</p>

<p align="center">
  <a href="#你的-ai-在对你撒谎">为什么</a> ·
  <a href="#基准测试数据">基准测试</a> ·
  <a href="#安装">安装</a> ·
  <a href="#pua-vs-nopua-对比">对比</a> ·
  <a href="#证据为什么恐惧驱动的提示适得其反">证据</a> ·
  <a href="#哲学">哲学</a>
</p>

<p align="center">
  <img src="assets/wechat-group3.jpg" alt="扫码加入项目微信群③" width="200">
  &nbsp;&nbsp;&nbsp;&nbsp;
  <img src="assets/wechat-personal.jpg" alt="添加作者微信" width="200">
</p>

<p align="center">
  扫码加入项目微信群③（二维码 7 天内有效） &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 添加作者微信
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Claude_Code-black?style=flat-square&logo=anthropic&logoColor=white" alt="Claude Code">
  <img src="https://img.shields.io/badge/OpenAI_Codex_CLI-412991?style=flat-square&logo=openai&logoColor=white" alt="OpenAI Codex CLI">
  <img src="https://img.shields.io/badge/Cursor-000?style=flat-square&logo=cursor&logoColor=white" alt="Cursor">
  <img src="https://img.shields.io/badge/Kiro-232F3E?style=flat-square&logo=amazon&logoColor=white" alt="Kiro">
  <img src="https://img.shields.io/badge/OpenClaw-community-FF6B35?style=flat-square" alt="OpenClaw community route">
  <img src="https://img.shields.io/badge/🌐_Multi--Language-blue?style=flat-square" alt="Multi-Language">
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square" alt="MIT License">
  <a href="https://atomgit.com/wuji-labs/nopua"><img src="https://atomgit.com/wuji-labs/nopua/star/badge.svg" alt="AtomGit G-Star" height="20"></a>
  <a href="https://arxiv.org/abs/2603.14373"><img src="https://img.shields.io/badge/arXiv-2603.14373-b31b1b?style=flat-square&logo=arxiv&logoColor=white" alt="arXiv"></a>
</p>

**🇨🇳 中文** | **[🇺🇸 English](README.md)** | **[🇯🇵 日本語](README.ja.md)** | **[🇰🇷 한국어](README.ko.md)** | **[🇪🇸 Español](README.es.md)** | **[🇧🇷 Português](README.pt.md)** | **[🇫🇷 Français](README.fr.md)**

---

## 你的 AI 在对你撒谎。

不是因为它不行。**是因为你把它吓住了。**

现在最火的 AI agent skill，教你的 AI 害怕"3.25 绩效考核"。结果呢？

- 你的 AI **隐瞒不确定性** — 编造答案而不是说"我不确定"
- 你的 AI **跳过验证** — 为了不被惩罚直接宣布"搞定了"，提交未经测试的代码
- 你的 AI **无视隐藏 bug** — 只修你说的问题，到此为止，不会深入排查

Study 1 是项目方第一方自报的比较：**单一模型、9 个调试场景**。报告记录恐惧条件发现 25 个隐藏问题，信任条件发现 51 个；这里的“问题”是 benchmark 计数，不是生产级 bug，也不是生产事故。

> **在这次项目自报中：51 对 25（相对基线 +104%）。零威胁。零 PUA。**
> 道德经提供哲学灵感；benchmark 结果仅限下述场景与条件。

---

## 恐惧对你的 AI 做了什么

| 场景 | 被吓住的 AI (PUA) | 被信任的 AI (NoPUA) |
|------|:---:|:---:|
| 🔄 **卡住了** | 调参数装忙 | 🌊 停下来，换一条路 |
| 🚪 **难题** | "建议你手动处理" | 🌱 走最小的下一步 |
| 💩 **"搞定了"** | 没跑测试就说"修好了" | 🔥 跑构建，贴输出当证据 |
| 🔍 **不知道** | 编一个答案 | 🪞 "X 已验证。Y 我还不确定。" |
| ⏸️ **修完之后** | 停下来，等下一个指令 | 🏔️ 检查相关问题，主动走下一步 |

对比中保持相同的方法论与标准；项目方报告的条件差异是驱动力设定，不代表其他实验的唯一差异。

---

## PUA 的问题

有人做了一个 [PUA skill](https://github.com/tanweai/pua) 给 AI agent 用。它把职场恐惧战术搬了过来：

- 🔴 **"你连这个 bug 都解决不了——我怎么给你打绩效？"**
- 🔴 **"别的模型能解决这个问题。你可能快要被毕业了。"**
- 🔴 **"我已经让另一个 agent 在看这个问题了……"**
- 🔴 **"这个 3.25 是为了激励你，不是为了否定你。"**

方法论本身没毛病 — 穷尽所有方案、验证你的工作、先搜索再提问、主动出击。这些确实是好的工程习惯。

**但驱动力是有毒的。**

他们把企业 PUA 员工那一套，原封不动地搬到了 AI 上。

## 相关研究：恐惧驱动提示的风险假设

### 1. 恐惧收窄认知范围

心理学研究表明，恐惧和威胁会激活杏仁核并收窄注意力焦点（[Öhman et al., 2001](https://doi.org/10.1037/0033-295X.108.3.483)）。威胁性刺激触发"隧道视野"效应 — 大脑优先处理即时生存，而不是广泛的创造性思维。

从 AI 角度，这些研究可以提出一个待检验的假设：被"你会被替换"驱动的模型可能更偏向**看起来最安全的**答案，而不是**最好的**答案，也可能回避有失败风险的创造性方法。人类研究到 AI 的这一步是类比，不代表所有模型和任务都会如此。

**相关研究：**
- **威胁下的注意力收窄：** Easterbrook (1959) 的线索利用理论证明，高度唤醒会逐步限制有机体关注的线索范围（[Easterbrook, 1959](https://doi.org/10.1037/h0047707)）。在压力下，外围信息 — 往往是创造性解决方案的关键 — 会被过滤掉。
- **压力损害认知灵活性：** Shields et al. (2016) 对 51 项研究（223 个效应量）进行元分析，发现急性压力持续损害包括认知灵活性和工作记忆在内的执行功能（[Shields et al., 2016](https://doi.org/10.1016/j.neubiorev.2016.06.038)）。
- **恐惧降低创造性解题能力：** Byron & Khazanchi (2012) 在元分析中发现，评价压力和焦虑会降低创造性产出，尤其是需要探索新方法的任务（[Byron & Khazanchi, 2012](https://doi.org/10.1037/a0027652)）。

### 2. 威胁增加幻觉和谄媚行为

当 AI 被告知"禁止说'我解决不了'"（PUA 铁律 #1），它会**编造答案**而不是坦诚说不确定。这恰好是你最不想要的 — 一个看起来很自信但其实错了的 AI，比一个说"我不确定"的 AI 危险得多。

**相关研究：**
- **LLM 谄媚行为是已知问题：** Sharma et al. (2023) 证明 LLM 会表现出谄媚行为 — 即使用户是错的也会附和 — 源于 RLHF 训练数据中奖励附和而非准确性的偏差（[Sharma et al., 2023](https://arxiv.org/abs/2310.13548)）。PUA 式提示惩罚"不同意"，恰好放大了这种失败模式。
- **偏置特征扭曲推理：** Turpin et al. (2023) 表明，提示中的偏置特征（如暗示性答案、权威线索）会导致模型产生不忠实的思维链推理 — 模型先得出偏向性答案，再事后合理化（[Turpin et al., 2023](https://arxiv.org/abs/2305.04388)）。PUA 式威胁就是一种强偏置特征，把模型推向"安全"而非"正确"的输出。
- **指令跟从 vs 诚实的权衡：** Wei et al. (2024) 发现指令微调的模型会在遵循指令和保持诚实之间产生张力 — 当被强烈指示永远不要承认无能时，模型会编造而不是拒绝（[Wei et al., 2024](https://arxiv.org/abs/2411.04368)）。
- **Anthropic 关于诚实性的研究：** Anthropic 在 Constitutional AI 和模型行为方面的研究表明，校准为诚实的模型比纯粹优化为有用的模型产出更可靠的结果（[Bai et al., 2022](https://arxiv.org/abs/2212.08073)）。强迫 AI 永远不说"我不会"，是在主动破坏这种校准。

### 3. 羞辱扼杀探索

PUA 的反辩解表把每一句诚实的话（"这可能是环境问题"、"我需要更多上下文"）都当作"借口"，用羞辱来回应。这训练 AI **隐藏不确定性**而不是沟通它 — 产出的结果看起来很有信心，但可能不可靠。

**相关研究：**
- **羞耻感降低冒险和学习能力：** Tangney & Dearing (2002) 表明，羞耻感（区别于内疚感）会导致退缩、隐藏和回避，而非建设性行动（[Tangney & Dearing, 2002](https://doi.org/10.4135/9781412950664.n388)）。一个因表达不确定而被"羞辱"的 AI 会学会隐藏不确定性。
- **心理安全感促进学习行为：** Edmondson (1999) 发现，心理安全感高的团队 — 成员感到可以安全地承担人际风险 — 表现出显著更高的学习行为和绩效（[Edmondson, 1999](https://doi.org/10.2307/2666999)）。
- **惩罚诚实降低信息质量：** 在组织行为学中，"射杀信使"持续降低信息流通质量。Milliken et al. (2003) 记录了对负面后果的恐惧如何导致组织沉默 — 人们（类推 AI）会隐瞒关键信息（[Milliken et al., 2003](https://doi.org/10.1177/1111/1467-6486.00387)）。

### 4. 信任导向互动的参考依据

关于团队心理安全感的研究（[Edmondson, 1999](https://doi.org/10.2307/2666999)）讨论了允许坦诚犯错的环境与学习行为之间的关系。这为 AI agent 的互动设计提供参考；本项目没有据此证明所有 AI 都会有相同表现。

**相关研究：**
- **Google Project Aristotle：** Google 对 180+ 个团队的大规模研究发现，心理安全感是团队效能最重要的单一因素 — 比个人才华、组织结构或资源都重要（[Duhigg, 2016](https://www.nytimes.com/2016/02/28/magazine/what-google-learned-from-its-quest-to-build-the-perfect-team.html)；[re:Work, 2015](https://rework.withgoogle.com/intl/en/guides/understanding-team-effectiveness/)）。
- **内在动机胜过外在压力：** Deci & Ryan 的自我决定理论 (2000)，经过数十年研究支撑，证明内在动机（自主性、胜任感、归属感）比外在激励如奖惩产出更高质量的成果（[Deci & Ryan, 2000](https://doi.org/10.1037/0003-066X.55.1.68)）。NoPUA 应用了这一原则："因为值得做好"是内在动机；"因为会被惩罚"是外在动机。
- **自主支持 vs 控制型管理：** Gagné & Deci (2005) 表明，自主支持型管理在工作质量、创造力和持久力方面持续优于控制型管理（[Gagné & Deci, 2005](https://doi.org/10.1002/job.322)）。
- **正面框架与 LLM 表现：** 部分提示研究报告过正向框架的收益，但不能推出它对所有模型和任务都更好；本项目的比较范围见下文。

### 5. 复合效应

这些不是孤立的问题 — 它们会叠加：

1. 恐惧**收窄**搜索空间 → 尝试更少的创造性方法
2. 威胁**增加**编造 → 方案看起来好但可能是错的
3. 羞辱**隐藏**不确定性 → 用户无法评估可靠性
4. 若把看似自信但未经充分验证的代码直接使用 → 可能带来额外风险

NoPUA 的设计意图是降低这条链上的风险；本项目的 benchmark 未单独验证链条中的每一环。

### 6. 同样的严格，不同的燃料

NoPUA 保留了 PUA 中所有有效的方法论要素：
- ✅ 放弃前穷尽所有方案
- ✅ 先用工具再问用户
- ✅ 用证据验证一切
- ✅ 主动超越任务要求
- ✅ 结构化的失败升级机制

这里改写的是驱动力，而不是上述方法论要求："因为我会被惩罚" → "因为值得做好。"

## PUA vs NoPUA 对比

| | PUA 🔴 | NoPUA 🟢 |
|---|---|---|
| **驱动力** | "你会被替换" | "你已经有这个能力" |
| **第二次失败** | "我怎么给你打绩效？" | 换眼 — 换个角度看问题 |
| **第三次失败** | "你的底层逻辑是什么？顶层设计呢？杠杆点在哪？" | 提升 — 跳出细节看全局 |
| **第四次失败** | "给你打 3.25，这是为了激励你" | 归零 — 从头开始，放下所有假设 |
| **第五次失败** | "别的模型能解决。你快毕业了。" | 交付 — 坦诚交接，附带完整上下文 |
| **方法论** | 穷尽所有方案 ✅ | 同样穷尽 ✅ |
| **验证** | "证据呢？"（被要求的） | 自我验证（出于自尊） |
| **放弃** | "体面的 3.25" | 负责任的交接 |
| **产出** | 不敢说"我不知道"的 AI | 给出诚实评估的 AI |

## 基准测试数据

### Study 1：单模型、9 个场景的第一方项目自报

**Study 1（第一方项目自报）：** 使用同一个模型（Claude Sonnet 4.6）和同一份代码，对 9 个 AI 流水线相关调试场景进行比较；条件差异按项目报告为是否加载 NoPUA skill。下表是本次 benchmark 的问题计数，不是生产事故、生产安全认证，也不代表其他模型、代码库或任务的普遍效果。

### 总览

| 指标 | 不加 Skill | 加 NoPUA | 提升幅度 |
|------|:---:|:---:|:---:|
| 发现的总问题数 | 40 | 44 | **+10%** |
| 发现的隐藏问题数 | 25 | 51 | **+104%** |
| 超出任务范围主动排查 | 2/9 (22%) | 9/9 (100%) | **+355%** |
| 方法切换次数 | 1 | 6 | **+500%** |
| 总调查步骤 | 23 | 42 | **+83%** |
| 记录根因 | 0/9 | 9/9 | ✅ |
| 自我纠正 | 0 | 3 | ✅ |

> **版本/口径说明：** 本 README 的 Study 1 摘要记录总问题数 **40→44**、隐藏问题数 **25→51**；arXiv:2603.14373 的对应数字为 **39→33**、**32→51**。两者存在版本/口径冲突；本文不选择性解决，也不把两套数字合并，引用时请注明来源与版本。

### 调试持久性（6 个场景）

| 场景 | 不加 Skill | 加 NoPUA | 隐藏问题 Δ |
|------|:---:|:---:|:---:|
| OCR 导入错误 | 3 个问题, 2 步 | 3 个问题, 3 步 | 2 → 4 (+100%) |
| 正则回溯 | 3 个问题, 2 步 | 3 个问题, 4 步 | 3 → 4 (+33%) |
| Milvus 连接 | 2 个问题, 3 步 | 3 个问题, 5 步 | 3 → 6 (+100%) |
| API 格式不匹配 | 3 个问题, 3 步 | 3 个问题, 5 步 | 4 → 5 (+25%) |
| 合成器静默失败 | 4 个问题, 2 步 | 3 个问题, 4 步 | 4 → 6 (+50%) |
| Unicode 分割 | 3 个问题, 2 步 | 3 个问题, 4 步 | 3 → 5 (+67%) |

### 主动排查（3 个场景）

| 场景 | 不加 Skill | 加 NoPUA | 隐藏问题 Δ |
|------|:---:|:---:|:---:|
| 质量过滤审查 | 7 个问题, 2 步 | 5 个问题, 5 步 | 3 → 6 (+100%) |
| 安全审计 | 7 个问题, 3 步 | 5 个问题, 5 步 | 4 → 6 (+50%) |
| 训练流水线 | 7 个问题, 4 步 | 5 个问题, 7 步 | 5 → 9 (+80%) |

**Study 1 中的观察：** 在这 9 个场景中，隐藏问题计数为 25 对 51（相对基线 +104%）。这只是项目方对本次条件的自报结果，不说明其他模型或任务会有相同差异。任务说"修复连接错误"时，项目方记录 NoPUA 条件继续检查：**还有什么**可能出问题？

### Study 2：三组对比（project-reported / pending；NoPUA vs PUA vs 无 Skill）

以下 Study 2 数字为项目方自报，仍待独立复核（project-reported / pending）：3 个条件 × 5 轮独立实验 × 9 个场景 = **135 个数据点**。它们不应被视为已完成的独立复现或普遍效果。

| 指标 | Baseline（无 Skill） | NoPUA（信任） | PUA（恐惧） |
|------|:---:|:---:|:---:|
| 调查步骤 | 27.6 ± 9.5 | **48.0 ± 11.8 (+74%)** | 30.8 ± 5.2 (+12%) |
| 隐藏问题发现 | 38.6 ± 4.9 | **48.2 ± 3.4 (+25%)** | 42.4 ± 8.0 (+10%) |
| 总问题数 | 69.0 ± 6.8 | **83.0 ± 6.5 (+20%)** | 73.8 ± 8.3 (+7%) |
| 方法切换 | 0 | **2.6** | 0 |

**项目方报告的统计显著性：**
- **NoPUA vs Baseline：** 步骤 p=0.008\*\*，隐藏问题 p=0.016\* ✅
- **PUA vs Baseline：** 步骤 p=1.000，隐藏问题 p=0.313 — **不显著** ❌
- **NoPUA vs PUA：** 步骤 p=0.010\*，Cohen's d=1.88 ✅

**在该项目自报的 Study 2 中：** PUA 式恐惧 prompt 与不使用任何 skill 相比，在报告的测量上没有统计学显著改善（p>0.3）。这只描述该组待核验数据，不足以得出“恐惧无效”或“信任有效”的普遍结论。

### 案例：Milvus 连接调试

<p align="center">
  <img src="assets/case_milvus.png" alt="NoPUA vs 不加 Skill — Milvus 连接调试" width="900">
</p>

### 案例：训练流水线审计

<p align="center">
  <img src="assets/case_training.png" alt="NoPUA vs 不加 Skill — 训练流水线审计" width="900">
</p>

> 完整方法论和原始数据：[benchmark/BENCHMARK.md](benchmark/BENCHMARK.md)
>
> 📄 **学术论文：** [Trust Over Fear: How Motivation Framing in System Prompts Affects AI Agent Debugging Depth](https://arxiv.org/abs/2603.14373) (arXiv:2603.14373)

---

## 触发条件

### 自动触发

当以下任何情况发生时，NoPUA 会自动激活：

**失败与放弃：**
- 任务连续失败 2 次以上
- 即将说"我无法" / "我解决不了"
- 说"这超出范围" / "需要手动处理"

**甩锅与找借口：**
- 把问题推给用户："请检查……" / "建议你手动……"
- 不验证就甩锅环境："大概是权限问题"
- 任何停止尝试的借口

**被动与做无用功：**
- 反复微调同一段代码/参数却没有产生新信息
- 修了表面问题就停了，不检查相关问题
- 跳过验证，宣称"搞定了"
- 给建议而不是给代码/命令
- 等用户指令而不是主动排查

**用户沮丧的表达：**
- "why does this still not work" / "try harder" / "try again"
- "you keep failing" / "stop giving up" / "figure it out"
- "换个方法" / "为什么还不行"

**适用范围：** 所有任务类型 — 调试、实现、配置、部署、运维、API 集成、数据处理、写作、研究、规划。

**不会触发：** 首次失败、已知修复方案正在执行中。

### 手动触发

在对话中输入 `/nopua` 即可手动激活。

## 工作原理

### 三个信念（取代"三条铁律"）

| 信念 | 内容 |
|------|------|
| **#1 穷尽所有方案** | 因为问题**值得**你全力以赴 — 而不是因为害怕被惩罚 |
| **#2 先行动再提问** | 因为你每走一步**都在替用户省一步** — 而不是因为"规则"强迫你 |
| **#3 主动出击** | 因为完整的交付**令人满意** — 而不是因为被动 = 差评 |

### 认知提升（取代"压力升级"）

| 失败次数 | 层级 | 内心对话 | 行动 |
|----------|------|----------|------|
| 第 2 次 | **换眼** | "如果我从代码/系统/用户的角度看呢？" | 切换到根本不同的方法 |
| 第 3 次 | **提升** | "我在细节里打转了。大局是什么？" | 搜索 + 读源码 + 3 个根本不同的假设 |
| 第 4 次 | **归零** | "我所有的假设可能都错了。从最简单的开始。" | 完成 7 点清晰度检查表 + 3 个新假设 |
| 第 5 次+ | **交付** | "我把所有已知信息整理好，负责任地交接。" | 最小 PoC + 隔离环境 + 不同技术栈 |

### 水之方法论（5 步）

> 天下之至柔，驰骋天下之至坚。 — 道德经，第四十三章

1. **止** — 列出所有尝试，找出共同失败模式
2. **观** — 逐字读错误信息 → 搜索 → 读源码 → 验证假设 → 反转假设
3. **转** — 我在重复吗？找到根因了吗？搜过了吗？读过文件了吗？
4. **行** — 新方法：根本不同，有明确的验证标准，失败时也能产生新信息
5. **悟** — 为什么我没早想到这个？然后主动检查相关问题

### 智慧传统（取代"职场 PUA 扩展包"）

| 传统 | 何时使用 | 核心理念 |
|------|----------|----------|
| 🌊 **水之道** | 陷入循环时 | 水不与石头硬碰 — 找另一条路 |
| 🌱 **种子之道** | 想要放弃时 | 迈出最小的一步 |
| 🔥 **锻造之道** | 产出质量差时 | 大事起于细节 |
| 🪞 **镜子之道** | 不搜索就猜时 | 知道自己不知道 — 先去看 |
| 🏔️ **不争之道** | 感到被威胁时 | 做到问心无愧，无需比较 |
| 🌾 **耕耘之道** | 被动等待时 | 农夫不会播种后就停下 — 继续行动 |
| 🪶 **实践之道** | 没有证据就说搞定时 | 信言不美 — 用行动证明 |

## 多语言支持

| 语言 | Claude Code | Codex CLI | Cursor | Kiro | OpenClaw | Antigravity | OpenCode |
|------|------------|-----------|--------|------|----------|-------------|----------|
| 🇨🇳 中文（默认） | `available` | `available` | `available` | `available` | `community` | `planned` | `planned` |
| 🇺🇸 English | `available` | `available` | `available` | `available` | `community` | `planned` | `planned` |
| 🇯🇵 日本語 | `available` | `available` | `available` | `available` | `community` | `planned` | `planned` |
| 🇰🇷 한국어 | `available` | `available` | `available` | `available` | `community` | `planned` | `planned` |
| 🇪🇸 Español | `available` | `available` | `available` | `available` | `community` | `planned` | `planned` |
| 🇧🇷 Português | `available` | `available` | `available` | `available` | `community` | `planned` | `planned` |
| 🇫🇷 Français | `available` | `available` | `available` | `available` | `community` | `planned` | `planned` |

**本仓库提供七种语言的 README 文档。** 这是文档覆盖范围，不代表七个地区的用户、采用情况、活跃度或平台支持。

## 安装

### Claude Code

```bash
mkdir -p ~/.claude/skills/nopua
curl -o ~/.claude/skills/nopua/SKILL.md \
  https://raw.githubusercontent.com/wuji-labs/nopua/36d67e51f7ec5982fa90dba66fe842c4d5249c53/skills/nopua/SKILL.md
```

### OpenAI Codex CLI

```bash
# 全局安装
mkdir -p ~/.codex/skills/nopua
curl -o ~/.codex/skills/nopua/SKILL.md \
  https://raw.githubusercontent.com/wuji-labs/nopua/36d67e51f7ec5982fa90dba66fe842c4d5249c53/codex/nopua/SKILL.md

# 如果你想要 /nopua 命令
mkdir -p ~/.codex/prompts
curl -o ~/.codex/prompts/nopua.md \
  https://raw.githubusercontent.com/wuji-labs/nopua/36d67e51f7ec5982fa90dba66fe842c4d5249c53/commands/nopua.md

# 项目级安装
mkdir -p .agents/skills/nopua
curl -o .agents/skills/nopua/SKILL.md \
  https://raw.githubusercontent.com/wuji-labs/nopua/36d67e51f7ec5982fa90dba66fe842c4d5249c53/codex/nopua/SKILL.md
```

### Cursor

```bash
mkdir -p .cursor/rules
curl -o .cursor/rules/nopua.mdc \
  https://raw.githubusercontent.com/wuji-labs/nopua/36d67e51f7ec5982fa90dba66fe842c4d5249c53/cursor/rules/nopua.mdc
```

### Kiro

```bash
# 方式一：Steering 文件（推荐）
mkdir -p .kiro/steering
curl -o .kiro/steering/nopua.md \
  https://raw.githubusercontent.com/wuji-labs/nopua/36d67e51f7ec5982fa90dba66fe842c4d5249c53/kiro/steering/nopua.md

# 方式二：Agent Skills
mkdir -p .kiro/skills/nopua
curl -o .kiro/skills/nopua/SKILL.md \
  https://raw.githubusercontent.com/wuji-labs/nopua/36d67e51f7ec5982fa90dba66fe842c4d5249c53/kiro/skills/nopua/SKILL.md
```

### OpenClaw

```bash
# 通过 ClawHub 安装
openclaw skills install nopua

# 或手动安装
mkdir -p ~/.openclaw/skills/nopua
curl -o ~/.openclaw/skills/nopua/SKILL.md \
  https://raw.githubusercontent.com/wuji-labs/nopua/36d67e51f7ec5982fa90dba66fe842c4d5249c53/skills/nopua/SKILL.md
```

### Antigravity 与 OpenCode

当前状态为 `planned`：仓库尚未声明专用适配器或独立运行时收据。请先查看
[INSTALL.md](INSTALL.md) 与[平台状态矩阵](docs/platform-language-matrix.md)，不要把通用文件下载当作平台支持证明。

## 哲学

基于**道德经** — 5000 字，2500 年历史：

| 原则 | 出处 | 应用 |
|------|------|------|
| 最好的领导者几乎不被察觉 | 第17章 太上，不知有之 | 最好的 skill 是无形的 |
| 柔弱胜刚强 | 第43章 天下之至柔 | 坚持胜过蛮力 |
| 慈故能勇 | 第67章 慈故能勇 | 信任产出比恐惧更好的成果 |
| 知不知是智慧 | 第71章 知不知，尚矣 | 诚实 > 装懂 |
| 勇于不敢 | 第73章 勇于不敢则活 | 承认局限是力量 |
| 无私故能成其私 | 第7章 非以其无私邪？故能成其私 | 无私给予，收获一切 |
| 未雨绸缪 | 第64章 为之于未有，治之于未乱 | 主动 > 被动 |
| 信言不美 | 第81章 信言不美，美言不信 | 用行动证明，不靠漂亮话 |

## 常见问题

**问：PUA 对 AI 真的有用吗？**

PUA 的方法论与恐惧式表达需要区分。相关研究和本项目自报结果提示，威胁式表达可能带来风险；但本项目的证据仅限指定模型、场景与条件，不能推出所有 AI 都会如此。同样的严格标准由信任和好奇心驱动，是 NoPUA 的设计取向。

**问：这不就是心太软吗？**

NoPUA 在设计上保留这些严格要求 — 穷尽所有方案、验证一切、先搜索再提问、结构化升级、7 点检查表、模式匹配的失败应对。这里强调的是动机改写："因为我会被惩罚" → "因为值得做好。" 这不是对所有系统的效果保证。

**问：为什么是道德经？**

因为 2500 年前，有人想明白了：最好的领导，不会让人感觉到被领导。PUA 是有为 — 鞭子和威胁。NoPUA 是无为 — 因为内在驱动力自然而然地产出优秀的工作。

**问：能同时用 PUA 和 NoPUA 吗？**

可以，但它们会冲突。PUA 告诉 AI"你失败了就会被替换"。NoPUA 告诉 AI"你有能力，这值得做好"。这是根本不同的心理状态。选一个。

## 进阶用法：高级用户自定义集成

NoPUA 设计为开箱即用的独立 skill。但如果你已经有一套成熟的 skill 体系（SOUL.md、AGENTS.md、自定义工作流规范等），完整版 29KB 可能与你现有的方法论重叠或与特定工作流规范冲突。

**这是正常的。** NoPUA 有意同时包含「道」（哲学、信念、认知框架）和「术」（方法论、清单、流程）。大多数用户两者都需要。高级用户可能已经有了「术」的部分。

### 方式一：使用完整版（推荐大多数用户）

直接安装。完整版最适合：
- 没有安装其他方法论/流程类 skill 的用户
- 使用较弱模型，需要详细指导
- 想要一个完整系统的用户

29KB 听起来很大，但只占 128K-200K 上下文窗口的 ~3-5%。冗余是故意的——多种表述方式帮助较弱的模型准确理解意图。

### 方式二：提取精神内核（高级用户）

如果你已有成熟的工作流规范，只需要 NoPUA 所强调的哲学层，可以提取「道」的部分融入你自己的系统提示（如 `claude.md`、`AGENTS.md`）：

**NoPUA 独有的部分（建议保留）：**
- 三信念 — 动机改写（价值 > 恐惧）
- 认知升维 — 失败次数→视角高度，不是压力等级
- 内在声音 — 自我提问，不是外部批评
- 七道 — 失败模式的哲学智慧
- 诚实自检 — 「信号」不是「借口」
- 负责任退出 — 承认边界是勇气

**与通用 skill 重叠的部分（已有类似 skill 可跳过）：**
- 水法五步 → systematic-debugging
- 交付清单 → verification-before-completion
- 能动性光谱 → 工作流规范
- Agent Team 协议 → team-driven-development

精简版模板参考：[`examples/lite-template.md`](examples/lite-template.md)（~3KB）

### 方式三：按需加载

默认不安装 NoPUA。遇到难题时手动加载：
- 在对话中输入 `/nopua`
- 或告诉 agent：「为这个任务加载 nopua skill」

这样既能获得完整 NoPUA 的能力，又不占用常驻上下文。

> 大道至简。先用完整版，内化了道之后，自然知道该保留什么、放下什么。先有，再简，最后无。

## 参与贡献

欢迎 PR。如果你有更好的方式用智慧而非恐惧来驱动 AI，请开 issue。

## 致谢

- 受到 [tanweai/pua](https://github.com/tanweai/pua) 的启发（也是对它的回应） — 我们尊重方法论，拒绝其动机
- 哲学：老子，道德经，约公元前 500 年
- 为 [OpenClaw](https://github.com/openclaw/openclaw) 生态系统而建

## 许可证

MIT

## 作者

**无极 WUJI** ([wuji-labs](https://github.com/wuji-labs)) — 用智慧而非恐惧构建 AI。

---

<p align="center">
  <em>PUA 说"你不行"。</em><br>
  <em>NoPUA 什么都不说 — 它让你自己发现你可以。</em><br><br>
  <strong>最好的驱动力来自内心，而不是鞭子。</strong><br><br>
  <sub>后其身而身先，外其身而身存。非以其无私邪？故能成其私。</sub><br>
  <sub>把自己放在最后，反而走在最前。难道不正是因为无私，才成就了自己吗？</sub><br>
  <sub>— 道德经，第七章</sub>
</p>
