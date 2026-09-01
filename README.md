# Quant Research Portfolio

> 一个统一的研究工作流框架，分为两个部分：QS 项目集，以及 ML / AI 知识库集。

[进入 QS 项目集](#1-qs-project-portfolio) · [进入 ML / AI 知识库](#2-ml-ai-knowledge-base)

## 总体结构

```mermaid
flowchart LR
  ROOT["统一研究工作流"]
  PROJECTS["QS 项目集"]
  KNOWLEDGE["ML AI 知识库集"]
  ROOT --> PROJECTS
  ROOT --> KNOWLEDGE
```

## 1. QS Project Portfolio

基于 QS 工作流时序图，项目集只聚焦两个项目：

- **04 Alpha Signal**
- **05 Portfolio Risk**

### 项目框架图

```mermaid
flowchart TB
  QS["QS Project Portfolio"]
  ALPHA["04 Alpha Signal"]
  RISK["05 Portfolio Risk"]
  QS --> ALPHA
  QS --> RISK
```

### QS 工作流时序图

```mermaid
sequenceDiagram
  autonumber
  participant PM
  participant QS
  participant DATA
  participant RISK
  PM->>QS: Define question and mandate
  QS->>DATA: Request audited data
  DATA-->>QS: Return data and quality checks
  Note over QS: 04 Alpha Signal
  QS->>QS: Build and test alpha signal
  QS-->>PM: Deliver alpha research memo
  Note over QS: 05 Portfolio Risk
  QS->>RISK: Construct portfolio and assess risk
  RISK-->>QS: Return risk and cost results
  QS-->>PM: Deliver portfolio risk brief
  PM-->>QS: Review and approve next experiment
```

[查看 QS 项目框架与时序图](./QS_QA_%E5%B7%A5%E4%BD%9C%E6%B5%81%E6%97%B6%E5%BA%8F%E5%9B%BE_%E5%BA%94%E6%9C%89%E9%A1%B9%E7%9B%AE%E6%B8%85%E5%8D%95.md)

## 2. ML / AI Knowledge Base

知识库集只保留学习框架和知识产出流程，不在这里展开具体 Notebook 或课程内容。

### 知识库框架图

```mermaid
flowchart TB
  KB["ML AI Knowledge Base"]
  ML["ML"]
  DL["DL"]
  TS["Time Series"]
  AI["AI LLM"]
  KB --> ML
  KB --> DL
  KB --> TS
  KB --> AI
```

### 知识库产出时序图

```mermaid
sequenceDiagram
  autonumber
  participant AUTHOR
  participant SOURCE
  participant WORKBENCH
  participant REVIEW
  participant PUBLISH
  AUTHOR->>SOURCE: Select topic and learning goal
  SOURCE-->>AUTHOR: Provide outline and references
  AUTHOR->>WORKBENCH: Build framework and examples
  WORKBENCH->>REVIEW: Run checks and review
  REVIEW-->>WORKBENCH: Return corrections
  WORKBENCH->>PUBLISH: Prepare public knowledge artifact
  PUBLISH-->>AUTHOR: Return feedback for iteration
```

[查看原 ML / AI workflow](https://github.com/Aayloo/ml-ai-learning-workflow)

---

这个仓库的入口只负责展示两部分的关系、框架图和时序图；具体项目代码与知识库内容保持在各自目录或仓库中。
