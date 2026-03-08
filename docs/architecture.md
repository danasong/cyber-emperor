# Cyber Emperor Architecture / 赛博皇帝架构图

## High-Level Architecture

```mermaid
flowchart TD
    U[User Goal / 用户目标] --> ZS[Zhongshu Sheng / 中书省\nTask Design & Planning]
    ZS --> MX[Menxia Sheng / 门下省\nReview & Risk Control]
    MX --> SS[Shangshu Sheng / 尚书省\nDispatch & Aggregation]

    SS --> LB1[吏部 / Role Routing]
    SS --> LB2[户部 / Scope & Resource Control]
    SS --> LB3[礼部 / Standards & Delivery Voice]
    SS --> LB4[兵部 / Parallel Dispatch]
    SS --> LB5[刑部 / Validation & QA]
    SS --> LB6[工部 / Build & Implementation]

    LB4 --> SC[shadow-clone\nParallel Subagents]
    LB6 --> CCH[claude-code-hook\nComplex Coding Engine]
    SC --> R[Subagent Results / 分身结果]
    CCH --> R
    R --> LB5
    LB5 --> D[Unified Delivery / 统一交付]
```

## Execution Flow

```mermaid
sequenceDiagram
    participant User as User / 用户
    participant Main as Main Session / 本体
    participant ZS as 中书省
    participant MX as 门下省
    participant SS as 尚书省
    participant SA as Subagents / 分身
    participant Hook as Claude Code Hook
    participant QA as 刑部验收

    User->>Main: Submit complex task
    Main->>ZS: Define objective and split work
    ZS->>MX: Send plan for review
    MX->>SS: Approve / revise plan
    SS->>SA: Dispatch parallel tasks via sessions_spawn
    SA->>Hook: Use hook for complex coding tasks
    Hook-->>SA: Completion callback
    SA-->>QA: Return results for validation
    QA-->>Main: Pass / fail with findings
    Main-->>User: Final unified delivery
```

## Design Summary

- `cyber-emperor` is the governance layer
- `shadow-clone` is the parallel execution layer
- `claude-code-hook` is the complex coding execution layer
- Final delivery is always unified, reviewed, and structured

## 中文说明

- `cyber-emperor` 负责治理、编排、控风险、收口
- `shadow-clone` 负责并行派发分身
- `claude-code-hook` 负责复杂编码零轮询执行
- 最终结果必须经过验收并统一交付，而不是拼盘式输出
