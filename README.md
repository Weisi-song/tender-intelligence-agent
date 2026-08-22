# 招标信息智能筛选工具

> 这是一个脱敏案例，不公开真实标讯、内部筛选标准、账号凭证或生产自动化流程。

公司原本需要每天安排人员在招标网站上搜索新标讯，再把可能相关的信息发给销售。我把这项重复工作做成了一套自动化流程：先批量抓取，再用 AI 和业务规则进行筛选、分类，最后输出值得销售查看和跟进的结果。

## 问题

单靠关键词会搜出大量看似相关、实际无关的结果，仍然需要人工逐条阅读。除了判断是否与公司业务有关，还要区分正式招标和招标预告，并保留一些虽然不直接相关、但适合后续建联的重要信息。

## 我的解决方案

- 用多组关键词批量抓取当天可能相关的标讯
- 让 AI 根据业务规则完成第二轮筛选
- 按价值和相关程度划分第一、第二梯队
- 分开整理正式招标信息和招标预告
- 对教育局等重要发布主体设置额外保留规则
- 持续用人工标注结果校准筛选规则和 Prompt

## 工作流

```text
标讯来源 → 关键词检索 → Agent + 业务规则筛选 → 优先级分类 → 人工复核 → 每日简报
```

## 系统如何改进

在早期，我多次请经理对原始标讯进行人工分类，再把他的判断与 AI 输出逐条比对，找出误判和遗漏。经过多轮调整后，筛选结果已经能够稳定用于每天的常规跟进。

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
