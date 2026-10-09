# Economic Intelligence System

## Pipeline Architecture Diagram

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
