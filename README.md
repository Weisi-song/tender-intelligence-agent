# 招标情报智能体

> 这是一个脱敏案例，不公开真实标讯、内部筛选标准、账号凭证或生产自动化流程。

我将原本依赖人工检索和转发的每日招标监测工作，设计成了一套自动化流程。

## 问题

关键词检索会产生大量噪音结果，仍需人工逐条判断业务相关性、区分正式招标与招标预告，并识别具有战略价值的潜在线索。

## 我的解决方案

- 使用多组关键词批量检索标讯
- 通过 Agent 进行第二轮相关性筛选
- 按业务规则划分第一、第二梯队
- 区分招标信息与招标预告
- 对战略相关的发布主体设置特殊保留规则
- 通过人工校准持续优化规则和 Prompt

## 工作流

```text
标讯来源 → 关键词检索 → Agent + 业务规则筛选 → 优先级分类 → 人工复核 → 每日简报
```

## 系统如何改进

我持续将 Agent 输出与经理的人工标注进行比对，定位误判与遗漏，再迭代筛选规则和 Prompt，直到每日结果可以稳定用于常规工作。

## 公开范围

本仓库呈现工作流和产品决策，后续将增加模拟输入输出及脱敏简报预览。


---

## English

# Tender Intelligence Agent

> A sanitized portfolio case study. Real tender records, internal criteria, credentials, and production automation are not published.

I automated a daily tender-monitoring workflow that had previously required manual searching and forwarding.

## The problem

Keyword searches produced a large, noisy set of notices. A person still had to inspect each result, judge business relevance, distinguish active tenders from advance notices, and identify strategically useful leads.

## What I built

- Batch retrieval using multiple keyword groups
- Agent-assisted second-pass relevance screening
- Business-rule classification into first- and second-priority leads
- Separation of tender notices and advance notices
- Special retention rules for strategically relevant issuers
- A human-in-the-loop calibration process for improving rules and prompts

## Workflow

```text
Tender sources → Keyword retrieval → Agent + business-rule filtering
               → Priority classification → Human review → Daily brief
```

## How the system improved

I repeatedly compared agent output with a manager's manual labels, identified false positives and missed cases, then refined the rules and prompts until the daily results became stable enough for routine use.

## Public portfolio scope

This repository documents the workflow and product decisions. A mock input/output example and sanitized report preview are planned.
