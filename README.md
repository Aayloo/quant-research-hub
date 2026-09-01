# Quant Research Portfolio

> 一个统一的研究工作流框架，分为两个部分：QS 项目集，以及 ML / AI 知识库集。

[进入 QS 项目集](#1-qs-project-portfolio) · [进入 ML / AI 知识库](#2-ml--ai-knowledge-base)

## 总体结构

![统一研究工作流](./docs/qs-project-framework.svg)

## 1. QS Project Portfolio

基于本地 QS 工作流 README，项目集只聚焦两个项目：

- **04 Alpha Signal**
- **05 Portfolio Risk**

### 项目框架图

![QS 项目框架图](./docs/qs-project-framework.svg)

### QS 工作流时序图

~~~mermaid
sequenceDiagram
    autonumber
    actor PM as Portfolio Manager
    participant QS as Quantitative Strategist
    participant DATA as Data and Research Stack
    participant RISK as Portfolio and Risk Stack

    PM->>QS: Define investment question, mandate, horizon and constraints
    QS->>DATA: Specify point-in-time data and universe
    DATA-->>QS: Return audited data and data-quality report
    rect rgb(235,245,255)
        Note over QS,DATA: Project 04 — Alpha Signal Research
        QS->>QS: Form economic hypothesis and factor/model specification
        QS->>DATA: Build features, labels and time-ordered datasets
        QS->>QS: Train baseline and candidate models
        QS->>QS: Generate out-of-sample forecasts and alpha signals
        QS-->>PM: Deliver alpha evidence and signal research memo
    end
    rect rgb(235,255,240)
        Note over QS,RISK: Project 05 — Portfolio Construction & Risk
        QS->>RISK: Analyze holdings or optionally convert alpha views into target portfolio
        RISK-->>QS: Return weights, turnover, exposures, costs and stress results
        QS->>QS: Backtest, attribute performance and test robustness
        QS-->>PM: Deliver portfolio recommendation and risk brief
    end
    PM-->>QS: Challenge assumptions or approve the next experiment
    QS->>QS: Monitor drift and iterate the research loop
~~~

[查看 QS 项目框架与时序图](./QS_QA_%E5%B7%A5%E4%BD%9C%E6%B5%81%E6%97%B6%E5%BA%8F%E5%9B%BE_%E5%BA%94%E6%9C%89%E9%A1%B9%E7%9B%AE%E6%B8%85%E5%8D%95.md)

## 2. ML / AI Knowledge Base

知识库集只保留学习框架和知识产出流程，不展开具体 Notebook 或课程内容。

### 知识库框架图

![ML AI 知识库框架图](./docs/ml-ai-framework.svg)

### 知识库产出时序图

![ML AI 知识库产出时序图](./docs/ml-ai-sequence.svg)

这个仓库的入口只负责展示 QS 项目集与 ML / AI 知识库集的关系、框架图和时序图。
