# Waterloo Rocketry 2025 Software Design Cycle - Status Report

*As of Feb 17, 2026*

---

## 1. Who's Working on What Right Now

### ChrisYx511 (Chris Yang) — Tech Lead / Multi-project

- Actively working on **DAQms data module** ([omnibus-DAQms PR #10](https://github.com/waterloo-rocketry/omnibus-DAQms/pull/10), WIP, updated 2026-02-12)
- Working on **Docker Compose orchestration** for omnibus stack ([omnibus PR #457](https://github.com/waterloo-rocketry/omnibus/pull/457), updated 2026-02-17)
- Assigned to [#85](https://github.com/waterloo-rocketry/2025-software-issues/issues/85) — Build the large standard data module per PDR design
- Assigned to [#70](https://github.com/waterloo-rocketry/2025-software-issues/issues/70) — Scaffold GH repos for new projects
- Assigned to [#20](https://github.com/waterloo-rocketry/2025-software-issues/issues/20) — Documentation for omnibus-bridge and omnibus-ts

### john-jpet — Avionics Testing App / Omnibus Bridge

- Working on **board status display** for avionics testing app ([avionics-testing-app PR #6](https://github.com/waterloo-rocketry/omnibus-avionics-testing-app/pull/6), open, updated 2026-01-25)
- Working on **Omnibus-TS connection management** ([avionics-testing-app PR #8](https://github.com/waterloo-rocketry/omnibus-avionics-testing-app/pull/8), open, updated 2026-01-27)
- Completed omnibus-bridge tasks: [#103](https://github.com/waterloo-rocketry/2025-software-issues/issues/103), [#104](https://github.com/waterloo-rocketry/2025-software-issues/issues/104), [#105](https://github.com/waterloo-rocketry/2025-software-issues/issues/105) (all closed ~Jan 2026)
- Assigned to [#93](https://github.com/waterloo-rocketry/2025-software-issues/issues/93) — Add Omnibus-TS data context to avionics testing app
- Leads [Epic #11](https://github.com/waterloo-rocketry/2025-software-issues/issues/11) — Avionics Testing App

### danielcwq (Daniel Ching) — DAQms FED

- Has open PR to **integrate omnibus-ts library** into DAQms ([omnibus-DAQms PR #8](https://github.com/waterloo-rocketry/omnibus-DAQms/pull/8), updated 2026-02-12)
- Assigned to [#87](https://github.com/waterloo-rocketry/2025-software-issues/issues/87) — Refactor useOmnibus context/hook to use Omnibus library
- Lead of [Epic #4](https://github.com/waterloo-rocketry/2025-software-issues/issues/4) — DAQms FED

### Qubik65536 & eteo-l — LabJack / Docker

- Recently completed the **LJM source prototype** ([#75](https://github.com/waterloo-rocketry/2025-software-issues/issues/75) closed 2026-02-02, [omnibus PR #448](https://github.com/waterloo-rocketry/omnibus/pull/448) merged)
- Now assigned to [#109](https://github.com/waterloo-rocketry/2025-software-issues/issues/109) — Create tests for LabJack data source (updated 2026-02-02)
- Qubik65536 also on [Epic #6](https://github.com/waterloo-rocketry/2025-software-issues/issues/6) — Package Omnibus Infra Better

### k72jiang (Kenny Jiang) — Parsley Instance ID

- Working on [#99](https://github.com/waterloo-rocketry/2025-software-issues/issues/99) — Add Parsley instance ID to CAN Messages
- Has open PR: [omnibus PR #444](https://github.com/waterloo-rocketry/omnibus/pull/444) (updated 2026-02-11)

### ShreyShingala — SocketIO Server / Parsley

- Working on **SocketIO server** ([omnibus PR #447](https://github.com/waterloo-rocketry/omnibus/pull/447), updated 2026-02-13) for [#84](https://github.com/waterloo-rocketry/2025-software-issues/issues/84)
- Completed multiple Parsley tasks: [#76](https://github.com/waterloo-rocketry/2025-software-issues/issues/76), [#92](https://github.com/waterloo-rocketry/2025-software-issues/issues/92), [#95](https://github.com/waterloo-rocketry/2025-software-issues/issues/95) (all closed ~Jan 2026)
- Also assigned to [#33](https://github.com/waterloo-rocketry/2025-software-issues/issues/33) — Parsley code quality audit

### Jack-Brown12 (Jack Brown) — Log Parsing / Timestamps

- Working on [#98](https://github.com/waterloo-rocketry/2025-software-issues/issues/98) — Add client timestamp option to globallog source
- Has open PR: [omnibus PR #454](https://github.com/waterloo-rocketry/omnibus/pull/454) (updated 2026-02-12)
- Part of [Epic #49](https://github.com/waterloo-rocketry/2025-software-issues/issues/49) — Log Parsing Improvements

### james-t-smith — Omnibus Message Types

- Working on [#79](https://github.com/waterloo-rocketry/2025-software-issues/issues/79) — Implement DAQMessage class
- Has two open PRs: [omnibus PR #434](https://github.com/waterloo-rocketry/omnibus/pull/434) (DAQMessage, stale since Nov 2025) and [omnibus PR #440](https://github.com/waterloo-rocketry/omnibus/pull/440) (ParsleyMessage, updated 2026-02-12)

### AtikshV — Omnibus Bridge Testing

- Working on [#19](https://github.com/waterloo-rocketry/2025-software-issues/issues/19) — Testing strategy for omnibus-bridge / omnibus-ts
- Has open PR: [omnibus PR #431](https://github.com/waterloo-rocketry/omnibus/pull/431) — omnibus_bridge test (updated 2026-02-12)
- Also assigned to [#67](https://github.com/waterloo-rocketry/2025-software-issues/issues/67) — Create omnibus-bridge

### Vaishali-Anapayan — DAQms FED / Plot Config

- Recently merged [omnibus-DAQms PR #13](https://github.com/waterloo-rocketry/omnibus-DAQms/pull/13) (d3.js dependencies, 2026-02-12)
- Has open PR [omnibus-DAQms PR #12](https://github.com/waterloo-rocketry/omnibus-DAQms/pull/12) (updated 2026-02-12)
- Assigned to [#86](https://github.com/waterloo-rocketry/2025-software-issues/issues/86) — Build plot configuration component

### yashjain128 (Yash Jain) — RLCSv3 Messages / Omnibus Bridge

- Has open PR: [omnibus PR #437](https://github.com/waterloo-rocketry/omnibus/pull/437) — RLCSv3 message type (stale since 2026-01-09)
- Assigned to [#83](https://github.com/waterloo-rocketry/2025-software-issues/issues/83) and [#96](https://github.com/waterloo-rocketry/2025-software-issues/issues/96)

### str4wb3rrytea & jennnniferkuang — Website / DAQms

- str4wb3rrytea assigned to [#97](https://github.com/waterloo-rocketry/2025-software-issues/issues/97) — Add/remove arbitrary data modules to dashboard (updated 2026-02-08)
- str4wb3rrytea assigned to [#89](https://github.com/waterloo-rocketry/2025-software-issues/issues/89) — Update sponsor package (merged [website-react PR #113](https://github.com/waterloo-rocketry/website-react/pull/113))
- jennnniferkuang leads [Project #5](https://github.com/waterloo-rocketry/2025-software-issues/issues/5) — Website Refresh
- Both assigned to [#43](https://github.com/waterloo-rocketry/2025-software-issues/issues/43), [#44](https://github.com/waterloo-rocketry/2025-software-issues/issues/44) — Website mockups and media coordination

### sphealmeon — DAQms Main Menu

- Assigned to [#108](https://github.com/waterloo-rocketry/2025-software-issues/issues/108) — Build the main menu for DAQms (updated 2026-01-27)

### Zarar3 (Zarar Khan) — CAN Sender

- Working on [#71](https://github.com/waterloo-rocketry/2025-software-issues/issues/71) — Make CAN Sender
- Has open PR: [avionics-testing-app PR #7](https://github.com/waterloo-rocketry/omnibus-avionics-testing-app/pull/7) (updated 2026-02-10)

### vincentjguo — OpenRocket / Log Parsing

- Leads [Project #14](https://github.com/waterloo-rocketry/2025-software-issues/issues/14) — OpenRocket Plugin Development
- Leads [Epic #49](https://github.com/waterloo-rocketry/2025-software-issues/issues/49) — Log Parsing Improvements
- Completed [#15](https://github.com/waterloo-rocketry/2025-software-issues/issues/15) — Logger board parsing support

### Theni1 — Parsley

- Assigned to [#91](https://github.com/waterloo-rocketry/2025-software-issues/issues/91) — Zod-based types for parsely-ts (stale)
- Also on [#33](https://github.com/waterloo-rocketry/2025-software-issues/issues/33) — Parsley code quality audit

### k5lowe — SocketIO Server

- Assigned to [#84](https://github.com/waterloo-rocketry/2025-software-issues/issues/84) — Build SocketIO Server (updated 2026-01-16)

---

## 2. Stale Tasks (Assigned but Little Recent Activity)

| Issue | Title | Assignee(s) | Last Updated | Notes |
|-------|-------|-------------|--------------|-------|
| [#91](https://github.com/waterloo-rocketry/2025-software-issues/issues/91) | Add Zod based types to parsely-ts | Theni1 | **2025-11-12** | No comments, no linked PR. ~3 months stale. |
| [#96](https://github.com/waterloo-rocketry/2025-software-issues/issues/96) | Expose omnibus connection/disconnection status | yashjain128 | **2025-11-26** | No comments, no linked PR. ~3 months stale. |
| [#83](https://github.com/waterloo-rocketry/2025-software-issues/issues/83) | Add dataclass for RLCSv3 Messages | yashjain128 | **2025-11-05** | PR [omnibus #437](https://github.com/waterloo-rocketry/omnibus/pull/437) open but stale since 2026-01-09. |
| [#87](https://github.com/waterloo-rocketry/2025-software-issues/issues/87) | Refactor useOmnibus context/hook | danielcwq | **2025-11-12** | No comments, no specific PR. ~3 months stale. |
| [#86](https://github.com/waterloo-rocketry/2025-software-issues/issues/86) | Build plot configuration component | Vaishali-Anapayan | **2025-11-09** | No comments. ~3 months stale. |
| [#71](https://github.com/waterloo-rocketry/2025-software-issues/issues/71) | Make CAN Sender | Zarar3 | **2025-11-26** | Issue stale, but [avionics-testing-app PR #7](https://github.com/waterloo-rocketry/omnibus-avionics-testing-app/pull/7) is active (2026-02-10). |
| [#79](https://github.com/waterloo-rocketry/2025-software-issues/issues/79) | Implement DAQMessage class | james-t-smith | **2025-10-31** | [omnibus PR #434](https://github.com/waterloo-rocketry/omnibus/pull/434) stale since 2025-11-20, but newer PR [#440](https://github.com/waterloo-rocketry/omnibus/pull/440) active. |
| [#33](https://github.com/waterloo-rocketry/2025-software-issues/issues/33) | Parsley code quality audit | yashjain128, ShreyShingala, Theni1 | **2025-11-04** | Has 2 comments but no recent movement. ~3 months stale. |
| [#70](https://github.com/waterloo-rocketry/2025-software-issues/issues/70) | Scaffold GH repos for new projects | ChrisYx511 | **2025-10-05** | ~4 months stale. Repos likely already created manually. |
| [#67](https://github.com/waterloo-rocketry/2025-software-issues/issues/67) | Create Omnibus-bridge | AtikshV | **2026-01-15** | ~1 month stale. Omnibus-bridge work seems handled by john-jpet's PRs instead. |

---

## 3. Overall Project Progress

### Project #1: New Frontend for DAQ Ops (DAQms) — [Issue #1](https://github.com/waterloo-rocketry/2025-software-issues/issues/1)

**Status: In Progress, ~40-50% complete**

**Goal:** Replace Omnibus Dashboard for DAQ ops with a React/Vite dashboard featuring a customizable grid of plots. PDR passed, CDR not yet done.

**What's done:**

- Story [#24](https://github.com/waterloo-rocketry/2025-software-issues/issues/24) (UI components with shadcn/ui) — **Closed**
- d3.js line chart component ([#92](https://github.com/waterloo-rocketry/2025-software-issues/issues/92)) — **Closed**, merged via [DAQms PR #7](https://github.com/waterloo-rocketry/omnibus-DAQms/pull/7)
- WebSocket mock data integration ([#65](https://github.com/waterloo-rocketry/2025-software-issues/issues/65), [#66](https://github.com/waterloo-rocketry/2025-software-issues/issues/66)) — **Closed**
- Fix rendering bugs ([#88](https://github.com/waterloo-rocketry/2025-software-issues/issues/88)) — **Closed**
- Dockerfile for globallog ([omnibus PR #456](https://github.com/waterloo-rocketry/omnibus/pull/456)) — **Merged**

**What's in progress:**

- Data module component ([#85](https://github.com/waterloo-rocketry/2025-software-issues/issues/85)) — WIP PR [DAQms #10](https://github.com/waterloo-rocketry/omnibus-DAQms/pull/10)
- Omnibus-ts integration ([DAQms PR #8](https://github.com/waterloo-rocketry/omnibus-DAQms/pull/8)) — Open
- Main menu ([#108](https://github.com/waterloo-rocketry/2025-software-issues/issues/108)) — Assigned to sphealmeon
- Add/remove data modules ([#97](https://github.com/waterloo-rocketry/2025-software-issues/issues/97)) — Assigned to str4wb3rrytea
- Plot configuration ([#86](https://github.com/waterloo-rocketry/2025-software-issues/issues/86)) — Stale

**What's not started:**

- Stories [#21](https://github.com/waterloo-rocketry/2025-software-issues/issues/21) (plot grid system), [#22](https://github.com/waterloo-rocketry/2025-software-issues/issues/22) (WebSocket real-time data integration), [#23](https://github.com/waterloo-rocketry/2025-software-issues/issues/23) (data series registry) — All unassigned
- Non-root Dockerfile directive ([#111](https://github.com/waterloo-rocketry/2025-software-issues/issues/111)) — Unassigned

**Assessment:** Core UI scaffolding is done and charting works. The major remaining work is real-time WebSocket data integration, plot grid customization, and the data series registry — all critical for MVP. CDR still pending. Behind the original "2 month" timeline for Epic #4.

---

### Project #2: 2025 Omnibus Systems Architecture Refresh — [Issue #2](https://github.com/waterloo-rocketry/2025-software-issues/issues/2)

**Status: In Progress, ~50-60% complete**

**Goal:** Modernize Omnibus infrastructure with uv packaging, Docker containers, WebSocket bridge (omnibus-bridge), TypeScript library (omnibus-ts), and better deployment.

**What's done:**

- uv workspace migration ([#25](https://github.com/waterloo-rocketry/2025-software-issues/issues/25)) — **Closed**
- omnibus-ts library ([#18](https://github.com/waterloo-rocketry/2025-software-issues/issues/18)) — **Closed**, [omnibus-ts PR #1](https://github.com/waterloo-rocketry/omnibus-ts/pull/1) merged
- Ansible playbook story ([#28](https://github.com/waterloo-rocketry/2025-software-issues/issues/28)) — **Closed**
- omnibus-bridge project structure, message translation, ZeroMQ receiver ([#103](https://github.com/waterloo-rocketry/2025-software-issues/issues/103), [#104](https://github.com/waterloo-rocketry/2025-software-issues/issues/104), [#105](https://github.com/waterloo-rocketry/2025-software-issues/issues/105)) — **Closed** by john-jpet
- Omnibus server Dockerfile ([omnibus PR #433](https://github.com/waterloo-rocketry/omnibus/pull/433)) — **Merged**
- LJM source prototype ([#75](https://github.com/waterloo-rocketry/2025-software-issues/issues/75)) — **Closed**, PR merged
- LJM Dockerfile ([omnibus PR #452](https://github.com/waterloo-rocketry/omnibus/pull/452)) — **Merged**
- Globallog Dockerfile ([omnibus PR #456](https://github.com/waterloo-rocketry/omnibus/pull/456)) — **Merged**

**What's in progress:**

- Docker Compose orchestration ([omnibus PR #457](https://github.com/waterloo-rocketry/omnibus/pull/457)) — Active today
- SocketIO server ([#84](https://github.com/waterloo-rocketry/2025-software-issues/issues/84)) — PR [omnibus #447](https://github.com/waterloo-rocketry/omnibus/pull/447) open
- Parsley instance ID ([#99](https://github.com/waterloo-rocketry/2025-software-issues/issues/99)) — PR [omnibus #444](https://github.com/waterloo-rocketry/omnibus/pull/444) open
- Client timestamp for globallog ([#98](https://github.com/waterloo-rocketry/2025-software-issues/issues/98)) — PR [omnibus #454](https://github.com/waterloo-rocketry/omnibus/pull/454) open
- LJM tests ([#109](https://github.com/waterloo-rocketry/2025-software-issues/issues/109)) — Assigned
- omnibus-bridge prototype ([#102](https://github.com/waterloo-rocketry/2025-software-issues/issues/102)) — Open
- omnibus-bridge testing ([#19](https://github.com/waterloo-rocketry/2025-software-issues/issues/19)) — PR [omnibus #431](https://github.com/waterloo-rocketry/omnibus/pull/431) open

**What's not started:**

- Docker Compose orchestration story ([#27](https://github.com/waterloo-rocketry/2025-software-issues/issues/27)) — Unassigned (though PR #457 addresses it)
- Typed Parsley parsing ([#100](https://github.com/waterloo-rocketry/2025-software-issues/issues/100), [#101](https://github.com/waterloo-rocketry/2025-software-issues/issues/101)) — Unassigned
- Documentation ([#20](https://github.com/waterloo-rocketry/2025-software-issues/issues/20)) — Assigned but no activity
- Message types story ([#78](https://github.com/waterloo-rocketry/2025-software-issues/issues/78)) — Open, PRs in progress

**Assessment:** Good momentum. The core bridge/infrastructure work is largely done. Docker packaging is actively being wrapped up. The remaining work is testing, documentation, and some Parsley improvements. This is the most active project. Tracking reasonably well against the architecture described in the project description.

---

### Project #5: Website Design Refresh & Infrastructure Refresh — [Issue #5](https://github.com/waterloo-rocketry/2025-software-issues/issues/5)

**Status: Early Stage, ~10-15% complete**

**Goal:** Refresh the Waterloo Rocketry website design + add InvenTree inventory management + infrastructure improvements.

**What's done:**

- Sponsor package update ([#89](https://github.com/waterloo-rocketry/2025-software-issues/issues/89)) — [website-react PR #113](https://github.com/waterloo-rocketry/website-react/pull/113) merged

**What's in progress:**

- Design mockups ([#43](https://github.com/waterloo-rocketry/2025-software-issues/issues/43)) — Assigned to jennnniferkuang & str4wb3rrytea but last updated 2025-11-13
- Media coordination ([#44](https://github.com/waterloo-rocketry/2025-software-issues/issues/44)) — Same status
- TypeScript migration ([#47](https://github.com/waterloo-rocketry/2025-software-issues/issues/47)) — Assigned to jennnniferkuang, stale since 2025-11-13

**What's not started:**

- All InvenTree stories ([#29](https://github.com/waterloo-rocketry/2025-software-issues/issues/29), [#30](https://github.com/waterloo-rocketry/2025-software-issues/issues/30), [#31](https://github.com/waterloo-rocketry/2025-software-issues/issues/31), [#32](https://github.com/waterloo-rocketry/2025-software-issues/issues/32)) — All unassigned
- Team feedback collection ([#45](https://github.com/waterloo-rocketry/2025-software-issues/issues/45)) — Unassigned
- Website build epic ([#16](https://github.com/waterloo-rocketry/2025-software-issues/issues/16)) — Unassigned

**Assessment:** This project appears to have stalled. Design work was assigned months ago but there's been no visible issue activity since November 2025. The InvenTree infrastructure stories are entirely unstarted and unassigned. Significantly behind the "4 month" estimated timeline.

---

### Project #8: Telemetry Monitoring System — [Issue #8](https://github.com/waterloo-rocketry/2025-software-issues/issues/8)

**Status: In Progress, ~25-30% complete. PDR and CDR not passed.**

**Goal:** Standalone Electron+React app for telemetry monitoring, reflecting rocket architecture, with integrated Parsley source and Omnibus server.

**What's done:**

- Parsley code quality audit started ([#34](https://github.com/waterloo-rocketry/2025-software-issues/issues/34) closed, [#33](https://github.com/waterloo-rocketry/2025-software-issues/issues/33) open with some work)
- Multiple Parsley test tasks completed ([#64](https://github.com/waterloo-rocketry/2025-software-issues/issues/64), [#68](https://github.com/waterloo-rocketry/2025-software-issues/issues/68), [#73](https://github.com/waterloo-rocketry/2025-software-issues/issues/73), [#74](https://github.com/waterloo-rocketry/2025-software-issues/issues/74), [#76](https://github.com/waterloo-rocketry/2025-software-issues/issues/76), [#77](https://github.com/waterloo-rocketry/2025-software-issues/issues/77))
- Parsley DataClass refactors ([#76](https://github.com/waterloo-rocketry/2025-software-issues/issues/76), [#77](https://github.com/waterloo-rocketry/2025-software-issues/issues/77)) — Closed
- Board data React component ([#72](https://github.com/waterloo-rocketry/2025-software-issues/issues/72)) — Closed by john-jpet
- Logger board parsing ([#15](https://github.com/waterloo-rocketry/2025-software-issues/issues/15)) — Closed by vincentjguo

**What's in progress:**

- Board status display ([#40](https://github.com/waterloo-rocketry/2025-software-issues/issues/40)) — [avionics-testing-app PR #6](https://github.com/waterloo-rocketry/omnibus-avionics-testing-app/pull/6) open
- Omnibus-TS connection in avionics app ([#93](https://github.com/waterloo-rocketry/2025-software-issues/issues/93)) — [avionics-testing-app PR #8](https://github.com/waterloo-rocketry/omnibus-avionics-testing-app/pull/8) open
- CAN sender ([#71](https://github.com/waterloo-rocketry/2025-software-issues/issues/71)) — [avionics-testing-app PR #7](https://github.com/waterloo-rocketry/omnibus-avionics-testing-app/pull/7) active

**What's not started:**

- All Telemetry FED stories ([#36](https://github.com/waterloo-rocketry/2025-software-issues/issues/36)-[#39](https://github.com/waterloo-rocketry/2025-software-issues/issues/39), [#42](https://github.com/waterloo-rocketry/2025-software-issues/issues/42)) — All unassigned
- Enhanced Parsley bindings ([#35](https://github.com/waterloo-rocketry/2025-software-issues/issues/35)) — Unassigned
- Telemetry BED ([#13](https://github.com/waterloo-rocketry/2025-software-issues/issues/13)) — Unassigned
- Parsely-ts Zod types ([#91](https://github.com/waterloo-rocketry/2025-software-issues/issues/91)) — Stale

**Assessment:** The avionics testing app (a precursor/proof-of-concept) is actively being built, with board display and CAN sender PRs in progress. However, the actual Telemetry Monitoring System (the Electron app described in the project) hasn't started — all its core stories are unassigned. The project timeline originally expected a prototype by early December and Rms development by mid-January. This is significantly behind schedule. Neither PDR nor CDR have been passed.

---

### Project #14: OpenRocket Plugin Development — [Issue #14](https://github.com/waterloo-rocketry/2025-software-issues/issues/14)

**Status: Early Stage, description still TBD**

**Goal:** TBD (project description says "TBD" for both description and success criteria).

**What's done:**

- Logger board parsing ([#15](https://github.com/waterloo-rocketry/2025-software-issues/issues/15)) — Closed
- Some simulation-related stories closed ([#61](https://github.com/waterloo-rocketry/2025-software-issues/issues/61), [#62](https://github.com/waterloo-rocketry/2025-software-issues/issues/62))

**What's in progress:**

- Log Parsing Improvements ([Epic #49](https://github.com/waterloo-rocketry/2025-software-issues/issues/49)) — Assigned to vincentjguo, Sameek-Sharma, Jack-Brown12, RoshanD15

**Assessment:** Hard to evaluate against the original description since it's TBD. There is related activity in the log parsing epic, but the core project scope is undefined. Led by vincentjguo.

---

### Epic #49: Log Parsing Improvements (sub-project of #2)

**Status: In Progress, ~20% complete**

Assigned to vincentjguo, Sameek-Sharma, Jack-Brown12, RoshanD15. Jack-Brown12 has an active PR for client timestamps. The CAN message parsing and Parsley improvements stories ([#51](https://github.com/waterloo-rocketry/2025-software-issues/issues/51), [#100](https://github.com/waterloo-rocketry/2025-software-issues/issues/100), [#101](https://github.com/waterloo-rocketry/2025-software-issues/issues/101)) remain unassigned/unstarted.
