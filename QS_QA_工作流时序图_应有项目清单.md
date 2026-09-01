# QS Project Portfolio：框架图与时序图

> 项目集只聚焦两个项目：**04 Alpha Signal** 与 **05 Portfolio Risk**。

## QS 工作流时序图

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

本页只保留原始 QS 工作流，并以两个项目框标识 Project 04 与 Project 05。
