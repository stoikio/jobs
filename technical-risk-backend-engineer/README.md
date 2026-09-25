# Python Backend & AI Engineer — Technical risk

## Introduction

Stoik's CERT handles cyber incidents for our policyholders: mailbox compromise, ransomware, wire fraud. On each incident an analyst goes through a series of tasks. They pull logs from the client's environment, analyse evidence, email the client and write the final report. The engineering team wants to build an LLM-based system to handle most of that work.
⠀
⠀
## Requirements

### Functional

- An investigation lasts anywhere from a few hours to several weeks, and some of that time is spent waiting for a client reply or logs availability. Your system must be able to wait on those event and trigger the following steps.
- Tasks come in different kinds. Some need an LLM agent with tools, others are plain deterministic code. Some tasks depends on each other while other are fully independent. Your system should optimize execution time while respecting those constraints.
- The plan to handle an incident isn't fully fixed. New information, like a client email or a finding, can add, retry or cancel tasks.
- The model never acts on the outside world by itself to avoid rogue agents. External actions should be approved by a human analyst. Your system must include a validation system for those actions.
⠀

### Non Functional 

- The service can restart at any time, in the middle of a task or a wait, and must not lose or duplicate work.
- Each investigation has a cost budget it can't exceed.
- Many investigations run at the same time, under the LLM provider's rate limits.
- An analyst should be able to understand afterwards why the system did what it did.



## Task
The main building blocks of the architecture, what each one is responsible for and how they interact.
