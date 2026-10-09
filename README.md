# Economic Intelligence System

## Introduction

Accurate projections of macroeconomic indicators will enable planners and advisors to make informed decisions, allowing the government to anticipate economic shifts, implement timely interventions, and enhance national economic stability.

## Objective

Develop an AI-driven machine learning (ML) model trained on a wide range of historical and real-time economic data to enhance the accuracy and timeliness of macroeconomic forecasts, thereby providing a more robust analytical foundation for the Treasury’s work.

## Approach

In economics, statistical time-series models provide strong baselines because they are specifically designed to model temporal dependencies using limited historical observations. Given the current dataset — monthly frequency, approximately 260 observations, a single variable, and no external drivers — it is preferable to start with statistical forecasting models rather than more complex machine learning models such as XGBoost. With limited data, complex ML models may capture historical patterns very well but fail to generalize to unseen periods.

## Architecture

```mermaid
flowchart LR
    A[("📦 Dataset")]
    B["Validation<br/>& Cleaning"]
    C["Time-Series<br/>Preparation"]
    D["Exploratory<br/>Analysis"]
    E["Model<br/>Training"]
    F["Backtesting<br/>& Evaluation"]
    G["Forecast"]
    H["🤖 DeepSeek<br/>Explanation"]
    I["📄 Report"]

    A --> B --> C --> D --> E --> F --> G --> H --> I
    F -. "retrain" .-> E

    classDef data fill:#E6F1FB,stroke:#185FA5,color:#0C447C
    classDef proc fill:#E1F5EE,stroke:#0F6E56,color:#085041
    classDef ml fill:#EEEDFE,stroke:#534AB7,color:#3C3489
    classDef out fill:#FAEEDA,stroke:#854F0B,color:#633806

    class A data
    class B,C,D proc
    class E,F,G ml
    class H,I out
```
