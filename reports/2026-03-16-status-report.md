# Software Design Cycle Status Report — 2026-03-16

## Section 1: Who's Working on What Right Now

### ChrisYx511

**Epic/Project Leadership:**
- Project Lead: [#1 DAQms](https://github.com/waterloo-rocketry/2025-software-issues/issues/1), [#2 Omnibus Architecture Refresh](https://github.com/waterloo-rocketry/2025-software-issues/issues/2)
- Epic Co-Lead: [#6 Package Omnibus Infra Better](https://github.com/waterloo-rocketry/2025-software-issues/issues/6), [#7 InvenTree](https://github.com/waterloo-rocketry/2025-software-issues/issues/7)

**Active PRs:**
- [omnibus-DAQms#10](https://github.com/waterloo-rocketry/omnibus-DAQms/pull/10) — Created Data Module (updated 2026-03-15)
- [parsley-ts#1](https://github.com/waterloo-rocketry/parsley-ts/pull/1) — feat: add Zod-based CAN message type definitions (updated 2026-02-24)
- [parsley#63](https://github.com/waterloo-rocketry/parsley/pull/63) — Add pyright strict type checking annotations (updated 2026-03-15)
- [parsley#62](https://github.com/waterloo-rocketry/parsley/pull/62) — refactor: use uv for lint workflow (updated 2026-03-16)
- [parsley#56](https://github.com/waterloo-rocketry/parsley/pull/56) — refactor: make types.py the sole source of truth for CAN message definitions (updated 2026-03-15)
- [omnibus#460](https://github.com/waterloo-rocketry/omnibus/pull/460) — [WIP] Initial CONOPS for Docker Compose deployment (updated 2026-02-25)

**Recently Merged PRs:**
- [omnibus#466](https://github.com/waterloo-rocketry/omnibus/pull/466) — test: rewrite websocket server tests (merged 2026-03-15)
- [omnibus#465](https://github.com/waterloo-rocketry/omnibus/pull/465) — refactor: replace per-message ZMQ Sender with persistent queue-based relay (merged 2026-03-15)
- [omnibus-DAQms#17](https://github.com/waterloo-rocketry/omnibus-DAQms/pull/17) — feat: refactor OmnibusProvider to use omnibus-ts library (merged 2026-03-10)
- [omnibus#459](https://github.com/waterloo-rocketry/omnibus/pull/459) — refactor(ljm): multi-stage Docker build for smaller image (merged 2026-03-12)
- [daq-raspi-deploy#1](https://github.com/waterloo-rocketry/daq-raspi-deploy/pull/1) — feat: add NetworkManager configuration tasks (merged 2026-03-16)
- [omnibus-ts#6](https://github.com/waterloo-rocketry/omnibus-ts/pull/6) — feat: add connection lifecycle API (merged 2026-03-01)
- [omnibus-ts#7](https://github.com/waterloo-rocketry/omnibus-ts/pull/7) — Bump version to 0.3.0 (merged 2026-03-01)

**Assigned Open Issues:**
- [#96](https://github.com/waterloo-rocketry/2025-software-issues/issues/96) — Expose the omnibus connection and disconnection status
- [#87](https://github.com/waterloo-rocketry/2025-software-issues/issues/87) — Refactor the useOmnibus context and hook to use the Omnibus library
- [#85](https://github.com/waterloo-rocketry/2025-software-issues/issues/85) — Build the large standard data module in accordance with PDR design
- [#70](https://github.com/waterloo-rocketry/2025-software-issues/issues/70) — Scaffold GH repos for new projects
- [#20](https://github.com/waterloo-rocketry/2025-software-issues/issues/20) — Create comprehensive documentation for omnibus-bridge and omnibus-ts
- [#48](https://github.com/waterloo-rocketry/2025-software-issues/issues/48) — Parsley USB crash bug

---

### eteo-l (Xinyu Liu)

**Active PRs:**
- [omnibus#470](https://github.com/waterloo-rocketry/omnibus/pull/470) — tests(sources/ljm): Add Unit Tests (updated 2026-03-16)

**Assigned Open Issues:**
- [#123](https://github.com/waterloo-rocketry/2025-software-issues/issues/123) — Add LabJack Input Range Check (co-assigned with Qubik65536)
- [#109](https://github.com/waterloo-rocketry/2025-software-issues/issues/109) — Create Tests for LabJack Data Source (co-assigned with Qubik65536)

---

### Qubik65536

**Recently Merged PRs:**
- [omnibus#462](https://github.com/waterloo-rocketry/omnibus/pull/462) — refactor(sources/ljm): Update Negative Address Dict for Differential Mode (merged 2026-03-10)

**Assigned Open Issues:**
- [#123](https://github.com/waterloo-rocketry/2025-software-issues/issues/123) — Add LabJack Input Range Check (co-assigned with eteo-l)
- [#109](https://github.com/waterloo-rocketry/2025-software-issues/issues/109) — Create Tests for LabJack Data Source (co-assigned with eteo-l)
- [#56](https://github.com/waterloo-rocketry/2025-software-issues/issues/56) — Create Data Source for LabJack LJM (story lead, co-assigned with eteo-l)

**Epic Co-Lead:** [#6 Package Omnibus Infra Better](https://github.com/waterloo-rocketry/2025-software-issues/issues/6)

---

### ShreyShingala

**Active PRs:**
- [omnibus#469](https://github.com/waterloo-rocketry/omnibus/pull/469) — Bitfield Checkboxes (updated 2026-03-15)
- [omnibus#468](https://github.com/waterloo-rocketry/omnibus/pull/468) — Fixing bug and memory (updated 2026-03-15)
- [omnibus#467](https://github.com/waterloo-rocketry/omnibus/pull/467) — Updating to 2026.3 CAN messages (updated 2026-03-15)
- [omnibus#447](https://github.com/waterloo-rocketry/omnibus/pull/447) — Feature/issue 84 socketio server (updated 2026-03-15)

**Assigned Open Issues:**
- [#33](https://github.com/waterloo-rocketry/2025-software-issues/issues/33) — Conduct comprehensive code quality audit for Parsley (co-assigned with yashjain128, Theni1)

**Recently Closed PRs:**
- [omnibus#464](https://github.com/waterloo-rocketry/omnibus/pull/464) — Parsley-Omnibus-2026-Update (closed 2026-03-15)

---

### Jack-Brown12

**Active PRs:**
- [parsley#61](https://github.com/waterloo-rocketry/parsley/pull/61) — Add to_flat_dict method for ParsleyError and ParsleyObject (updated 2026-03-15)
- [omnibus#454](https://github.com/waterloo-rocketry/omnibus/pull/454) — J84brown/add client timestamp (updated 2026-03-12)

**Assigned Open Issues:**
- [#98](https://github.com/waterloo-rocketry/2025-software-issues/issues/98) — Add client timestamp option to globallog source
- [#51](https://github.com/waterloo-rocketry/2025-software-issues/issues/51) — Parse CAN messages from data_processing_v2

---

### k72jiang (Kenny Jiang)

**Recently Merged PRs:**
- [omnibus#444](https://github.com/waterloo-rocketry/omnibus/pull/444) — K72jiang/add parsley instance (merged 2026-03-12)

**Recently Closed Issues:**
- [#99](https://github.com/waterloo-rocketry/2025-software-issues/issues/99) — Add Parsley instance ID to CAN Messages (closed 2026-03-12)

**Epic Co-Lead:** [#6 Package Omnibus Infra Better](https://github.com/waterloo-rocketry/2025-software-issues/issues/6)

---

### john-jpet (John Petruzziello)

**Active PRs:**
- [omnibus-avionics-testing-app#8](https://github.com/waterloo-rocketry/omnibus-avionics-testing-app/pull/8) — feat(renderer): add Omnibus-TS connection management (updated 2026-01-27)
- [omnibus-avionics-testing-app#6](https://github.com/waterloo-rocketry/omnibus-avionics-testing-app/pull/6) — Issue 40 implement board status display (updated 2026-01-25)

**Assigned Open Issues:**
- [#93](https://github.com/waterloo-rocketry/2025-software-issues/issues/93) — Add Omnibus-TS data context to Avionics Testing App
- [#40](https://github.com/waterloo-rocketry/2025-software-issues/issues/40) — Implement board status display from Parsley

**Recently Closed Issues:**
- [#105](https://github.com/waterloo-rocketry/2025-software-issues/issues/105) — Implement ZeroMQ message receiver
- [#104](https://github.com/waterloo-rocketry/2025-software-issues/issues/104) — Implement message translation logic for omnibus-bridge
- [#103](https://github.com/waterloo-rocketry/2025-software-issues/issues/103) — Create project structure for omnibus-bridge

**Epic Lead:** [#11 Avionics Testing App](https://github.com/waterloo-rocketry/2025-software-issues/issues/11)

---

### str4wb3rrytea (Sophia Xu)

**Active PRs:**
- [website-react#123](https://github.com/waterloo-rocketry/website-react/pull/123) — Replaced sponsorship package with a smaller one (updated 2026-02-08)
- [website-react#119](https://github.com/waterloo-rocketry/website-react/pull/119) — added ts dependencies and changed banner photo to tsx (updated 2025-11-27)
- [website-react#117](https://github.com/waterloo-rocketry/website-react/pull/117) — new home page (updated 2025-11-27)

**Recently Merged PRs:**
- [omnibus-DAQms#16](https://github.com/waterloo-rocketry/omnibus-DAQms/pull/16) — Implement dynamic plot management to Sensor Monitoring Dashboard (merged 2026-03-02)

**Assigned Open Issues:**
- [#108](https://github.com/waterloo-rocketry/2025-software-issues/issues/108) — Build the Main Menu for DAQms
- [#97](https://github.com/waterloo-rocketry/2025-software-issues/issues/97) — Add ability to add and remove arbitrary data modules to the dashboard
- [#89](https://github.com/waterloo-rocketry/2025-software-issues/issues/89) — Update to new sponsor package

**Epic Co-Lead:** [#12 Website Design Process](https://github.com/waterloo-rocketry/2025-software-issues/issues/12), [#7 InvenTree](https://github.com/waterloo-rocketry/2025-software-issues/issues/7)

---

### danielcwq (Daniel Ching)

**Active PRs:**
- [omnibus-DAQms#8](https://github.com/waterloo-rocketry/omnibus-DAQms/pull/8) — feat: integrate omnibus-ts library for DAQ communication (updated 2026-02-21)

**Epic Co-Lead:** [#4 DAQms FED](https://github.com/waterloo-rocketry/2025-software-issues/issues/4)

---

### Vaishali-Anapayan

**Active PRs:**
- [omnibus-DAQms#12](https://github.com/waterloo-rocketry/omnibus-DAQms/pull/12) — Add edit graph drop-down and edit graph pop-up (updated 2026-03-15)
- [omnibus-avionics-testing-app#9](https://github.com/waterloo-rocketry/omnibus-avionics-testing-app/pull/9) — Create mock backend (updated 2026-03-02)

**Assigned Open Issues:**
- [#86](https://github.com/waterloo-rocketry/2025-software-issues/issues/86) — Build the plot configuration component

---

### yashjain128 (Yash Jain)

**Assigned Open Issues:**
- [#102](https://github.com/waterloo-rocketry/2025-software-issues/issues/102) — Create a omnibus-bridge prototype (co-assigned with john-jpet)
- [#83](https://github.com/waterloo-rocketry/2025-software-issues/issues/83) — Add dataclass for RLCSv3 Messages
- [#33](https://github.com/waterloo-rocketry/2025-software-issues/issues/33) — Conduct comprehensive code quality audit for Parsley (co-assigned)

**Closed PRs:**
- [omnibus#437](https://github.com/waterloo-rocketry/omnibus/pull/437) — Create pydantic rlcsv3message type (closed, not merged)

---

### jennnniferkuang (Jennifer Kuang)

**Active PRs:**
- [website-react#118](https://github.com/waterloo-rocketry/website-react/pull/118) — added home-new hidden page (updated 2025-11-27)
- [website-react#116](https://github.com/waterloo-rocketry/website-react/pull/116) — Test (updated 2025-11-25)

**Project Lead:** [#5 Website Design Refresh](https://github.com/waterloo-rocketry/2025-software-issues/issues/5)
**Epic Co-Lead:** [#12 Website Design Process](https://github.com/waterloo-rocketry/2025-software-issues/issues/12), [#7 InvenTree](https://github.com/waterloo-rocketry/2025-software-issues/issues/7)

---

### AtikshV

**Assigned Open Issues:**
- [#19](https://github.com/waterloo-rocketry/2025-software-issues/issues/19) — Implement comprehensive testing strategy for omnibus-bridge and omnibus-ts
- [#67](https://github.com/waterloo-rocketry/2025-software-issues/issues/67) — Create Omnibus-bridge

**Closed PRs:**
- [omnibus#431](https://github.com/waterloo-rocketry/omnibus/pull/431) — simple omnibus_bridge test (closed, not merged)

**Epic Lead:** [#9 Parsley Source Reliability Audit](https://github.com/waterloo-rocketry/2025-software-issues/issues/9)

---

### arulinimuthu

**Assigned Open Issues:**
- [#122](https://github.com/waterloo-rocketry/2025-software-issues/issues/122) — Export Wind Level Format (updated 2026-03-15)

---

### vincentjguo

**Project Lead:** [#14 OpenRocket Plugin Development](https://github.com/waterloo-rocketry/2025-software-issues/issues/14)
**Epic Co-Lead:** [#49 Log Parsing Improvements](https://github.com/waterloo-rocketry/2025-software-issues/issues/49)

---

### james-t-smith

**Assigned Open Issues:**
- [#79](https://github.com/waterloo-rocketry/2025-software-issues/issues/79) — Implement DAQMessage class
- [#78](https://github.com/waterloo-rocketry/2025-software-issues/issues/78) — Omnibus Message Types (story)

**Closed PRs:**
- [omnibus#440](https://github.com/waterloo-rocketry/omnibus/pull/440) — Jt3smith/build parsleymessage class (closed, not merged)
- [omnibus#434](https://github.com/waterloo-rocketry/omnibus/pull/434) — Create DAQMessage Pydantic Model (closed, not merged)

---

### Zarar3 (Zarar Khan)

**Active PRs:**
- [omnibus-avionics-testing-app#7](https://github.com/waterloo-rocketry/omnibus-avionics-testing-app/pull/7) — Added the can sender prototype (updated 2026-02-10)

**Assigned Open Issues:**
- [#71](https://github.com/waterloo-rocketry/2025-software-issues/issues/71) — Make CAN Sender

---

### k5lowe

**Assigned Open Issues:**
- [#84](https://github.com/waterloo-rocketry/2025-software-issues/issues/84) — Build SocketIO Server

---

### Theni1

**Assigned Open Issues:**
- [#33](https://github.com/waterloo-rocketry/2025-software-issues/issues/33) — Conduct comprehensive code quality audit for Parsley (co-assigned)

---

## Section 2: Stale Tasks

| Issue | Title | Assignee(s) | Last Updated | Notes |
|-------|-------|-------------|--------------|-------|
| [#70](https://github.com/waterloo-rocketry/2025-software-issues/issues/70) | Scaffold GH repos for new projects | ChrisYx511 | 2025-10-05 | No comments, no linked PR. ~5 months stale. Repos appear to have been scaffolded already (omnibus-DAQms, omnibus-ts, etc. exist). Likely can be closed. |
| [#86](https://github.com/waterloo-rocketry/2025-software-issues/issues/86) | Build the plot configuration component | Vaishali-Anapayan | 2025-11-09 | No comments. ~4 months stale. Related PR [omnibus-DAQms#12](https://github.com/waterloo-rocketry/omnibus-DAQms/pull/12) is active (updated 2026-03-15), so work may be in progress. |
| [#89](https://github.com/waterloo-rocketry/2025-software-issues/issues/89) | Update to new sponsor package | str4wb3rrytea | 2025-11-11 | ~4 months stale on the issue, but [website-react#123](https://github.com/waterloo-rocketry/website-react/pull/123) was opened for this (updated 2026-02-08). PR itself is ~5 weeks stale. |
| [#71](https://github.com/waterloo-rocketry/2025-software-issues/issues/71) | Make CAN Sender | Zarar3 | 2025-11-26 | 1 comment. ~4 months stale. Linked PR [avionics-testing-app#7](https://github.com/waterloo-rocketry/omnibus-avionics-testing-app/pull/7) last updated 2026-02-10 (~5 weeks stale). |
| [#78](https://github.com/waterloo-rocketry/2025-software-issues/issues/78) | Omnibus Message Types | james-t-smith | 2025-11-04 | No comments. ~4.5 months stale. Both linked PRs ([omnibus#440](https://github.com/waterloo-rocketry/omnibus/pull/440), [omnibus#434](https://github.com/waterloo-rocketry/omnibus/pull/434)) were closed without merging. |
| [#79](https://github.com/waterloo-rocketry/2025-software-issues/issues/79) | Implement DAQMessage class | james-t-smith | 2025-10-31 | No comments. ~4.5 months stale. PRs closed without merge (same as #78). |
| [#93](https://github.com/waterloo-rocketry/2025-software-issues/issues/93) | Add Omnibus-TS data context to Avionics Testing App | john-jpet | 2026-01-25 | No comments. ~7 weeks stale. Linked PR [avionics-testing-app#8](https://github.com/waterloo-rocketry/omnibus-avionics-testing-app/pull/8) also stale (last updated 2026-01-27). |
| [#40](https://github.com/waterloo-rocketry/2025-software-issues/issues/40) | Implement board status display from Parsley | john-jpet | 2025-10-07 | No comments. ~5 months stale. Linked PR [avionics-testing-app#6](https://github.com/waterloo-rocketry/omnibus-avionics-testing-app/pull/6) last updated 2026-01-25 (~7 weeks stale). |
| [#67](https://github.com/waterloo-rocketry/2025-software-issues/issues/67) | Create Omnibus-bridge | AtikshV | 2026-01-15 | 1 comment. ~2 months stale. Linked PR [omnibus#431](https://github.com/waterloo-rocketry/omnibus/pull/431) was closed without merge. |
| [#19](https://github.com/waterloo-rocketry/2025-software-issues/issues/19) | Implement comprehensive testing strategy for omnibus-bridge and omnibus-ts | AtikshV | 2025-09-24 | No comments. ~6 months stale. No linked PR. |
| [#84](https://github.com/waterloo-rocketry/2025-software-issues/issues/84) | Build SocketIO Server | k5lowe | 2026-01-16 | 1 comment. ~2 months stale. Related PR [omnibus#447](https://github.com/waterloo-rocketry/omnibus/pull/447) by ShreyShingala is active (updated 2026-03-15) — may overlap or supersede this task. |
| [#98](https://github.com/waterloo-rocketry/2025-software-issues/issues/98) | Add client timestamp option to globallog source | Jack-Brown12 | 2026-01-14 | No comments. ~2 months stale. Linked PR [omnibus#454](https://github.com/waterloo-rocketry/omnibus/pull/454) last updated 2026-03-12 — PR is active. |
| [#47](https://github.com/waterloo-rocketry/2025-software-issues/issues/47) | Use TypeScript on all website surfaces | jennnniferkuang | 2025-11-13 | No comments. ~4 months stale. Related PR [website-react#115](https://github.com/waterloo-rocketry/website-react/pull/115) was merged, but PRs [#119](https://github.com/waterloo-rocketry/website-react/pull/119), [#118](https://github.com/waterloo-rocketry/website-react/pull/118), [#117](https://github.com/waterloo-rocketry/website-react/pull/117) are ~4 months stale. |
| [#44](https://github.com/waterloo-rocketry/2025-software-issues/issues/44) | Coordinate with media team for branding requirements | jennnniferkuang, str4wb3rrytea | 2025-11-13 | No comments. ~4 months stale. No linked PR. Design coordination task. |
| [#43](https://github.com/waterloo-rocketry/2025-software-issues/issues/43) | Create multiple website design mockups | jennnniferkuang, str4wb3rrytea | 2025-11-13 | No comments. ~4 months stale. No linked PR. Design task. |
| [#33](https://github.com/waterloo-rocketry/2025-software-issues/issues/33) | Conduct comprehensive code quality audit for Parsley | yashjain128, ShreyShingala, Theni1 | 2025-11-04 | 2 comments. ~4.5 months stale. Several related Parsley PRs have been merged, but the story itself hasn't been updated. |
| [#48](https://github.com/waterloo-rocketry/2025-software-issues/issues/48) | Parsley USB crash bug | ChrisYx511, celery6 | 2025-09-24 | 2 comments. ~6 months stale. Bug report with no linked fix PR. |
| [#102](https://github.com/waterloo-rocketry/2025-software-issues/issues/102) | Create an omnibus-bridge prototype | yashjain128, john-jpet | 2026-01-28 | No comments. ~7 weeks stale. Prototype may already exist via merged bridge PRs. |

---

## Section 3: Overall Project Progress

### Project [#1](https://github.com/waterloo-rocketry/2025-software-issues/issues/1): New Frontend for DAQ Ops — DAQms
**Status: Active development, ~40% complete**

**Goal:** Build a React dashboard for DAQ sensors to replace Omnibus Dashboard, deployed to the DAQ computer.

**What's done:**
- [#24](https://github.com/waterloo-rocketry/2025-software-issues/issues/24) — Responsive UI components using shadcn/ui and Tailwind (CLOSED)
- [#92](https://github.com/waterloo-rocketry/2025-software-issues/issues/92) — d3.js line chart visualization component (CLOSED)
- [#88](https://github.com/waterloo-rocketry/2025-software-issues/issues/88) — Fix double and forced rendering in data graphs (CLOSED)
- [#119](https://github.com/waterloo-rocketry/2025-software-issues/issues/119) — DAQms default route bug fix (CLOSED)
- [omnibus-DAQms#16](https://github.com/waterloo-rocketry/omnibus-DAQms/pull/16) — Dynamic plot management merged
- [omnibus-DAQms#17](https://github.com/waterloo-rocketry/omnibus-DAQms/pull/17) — OmnibusProvider refactored to use omnibus-ts merged

**What's in progress:**
- [omnibus-DAQms#10](https://github.com/waterloo-rocketry/omnibus-DAQms/pull/10) — Data Module (ChrisYx511)
- [omnibus-DAQms#12](https://github.com/waterloo-rocketry/omnibus-DAQms/pull/12) — Edit graph UI (Vaishali-Anapayan)
- [omnibus-DAQms#8](https://github.com/waterloo-rocketry/omnibus-DAQms/pull/8) — omnibus-ts integration (danielcwq)
- [#108](https://github.com/waterloo-rocketry/2025-software-issues/issues/108) — Build the Main Menu for DAQms (str4wb3rrytea)
- [#97](https://github.com/waterloo-rocketry/2025-software-issues/issues/97) — Add/remove arbitrary data modules (str4wb3rrytea)
- [#96](https://github.com/waterloo-rocketry/2025-software-issues/issues/96) — Expose omnibus connection status (ChrisYx511)
- [#87](https://github.com/waterloo-rocketry/2025-software-issues/issues/87) — Refactor useOmnibus hook (ChrisYx511)
- [#85](https://github.com/waterloo-rocketry/2025-software-issues/issues/85) — Build the large standard data module (ChrisYx511)

**What's not started:**
- [#23](https://github.com/waterloo-rocketry/2025-software-issues/issues/23) — Data series registry and plot configuration system
- [#22](https://github.com/waterloo-rocketry/2025-software-issues/issues/22) — Real-time WebSocket data integration for plot updates
- [#21](https://github.com/waterloo-rocketry/2025-software-issues/issues/21) — Customizable plot grid system
- [#111](https://github.com/waterloo-rocketry/2025-software-issues/issues/111) — Add non-root USER directive to globallog Dockerfile

**Assessment:** DAQms is the most active project. The frontend has foundational components in place (d3.js charts, dynamic plot management, omnibus-ts integration). The team is now building out the data module UI and main menu. Key risks: several unassigned stories (#21, #22, #23) for core data plumbing remain untouched. CDR has not been completed yet. The project needs to accelerate on the data series registry and WebSocket integration to connect the UI to live data.

---

### Project [#2](https://github.com/waterloo-rocketry/2025-software-issues/issues/2): 2025 Omnibus Systems Architecture Refresh
**Status: Good progress, ~50% complete**

**Goal:** Refactor Omnibus architecture with Docker packaging, WebSocket bridge, TypeScript bindings, and improved deployment.

**What's done:**
- [#25](https://github.com/waterloo-rocketry/2025-software-issues/issues/25) — Migrate Omnibus to uv workspace (CLOSED)
- [#18](https://github.com/waterloo-rocketry/2025-software-issues/issues/18) — Create TypeScript omnibus-ts library (CLOSED)
- [#28](https://github.com/waterloo-rocketry/2025-software-issues/issues/28) — Create Ansible playbook for DAQ PC deployment (CLOSED)
- [#99](https://github.com/waterloo-rocketry/2025-software-issues/issues/99) — Add Parsley instance ID to CAN Messages (CLOSED)
- [#103](https://github.com/waterloo-rocketry/2025-software-issues/issues/103), [#104](https://github.com/waterloo-rocketry/2025-software-issues/issues/104), [#105](https://github.com/waterloo-rocketry/2025-software-issues/issues/105) — omnibus-bridge project structure, translation logic, ZMQ receiver (all CLOSED)
- [#75](https://github.com/waterloo-rocketry/2025-software-issues/issues/75) — Prototype LJM Source (CLOSED)
- [#94](https://github.com/waterloo-rocketry/2025-software-issues/issues/94) — CLI flag for Omnibus Server quiet mode (CLOSED)
- Docker containers for omnibus-server, LJM source, globallog all created and published
- omnibus-ts published to NPM (v0.3.0), connection lifecycle API added
- Docker Compose initial deployment created ([omnibus#457](https://github.com/waterloo-rocketry/omnibus/pull/457) merged)
- Multi-stage Docker build for LJM source ([omnibus#459](https://github.com/waterloo-rocketry/omnibus/pull/459) merged)
- NetworkManager Ansible tasks for daq-raspi-deploy ([daq-raspi-deploy#1](https://github.com/waterloo-rocketry/daq-raspi-deploy/pull/1) merged)

**What's in progress:**
- [omnibus#470](https://github.com/waterloo-rocketry/omnibus/pull/470) — LJM unit tests (eteo-l)
- [omnibus#460](https://github.com/waterloo-rocketry/omnibus/pull/460) — Docker Compose CONOPS (ChrisYx511, WIP)
- [#56](https://github.com/waterloo-rocketry/2025-software-issues/issues/56) — LabJack LJM Data Source story (Qubik65536, eteo-l)
- [#123](https://github.com/waterloo-rocketry/2025-software-issues/issues/123) — LabJack Input Range Check
- [#109](https://github.com/waterloo-rocketry/2025-software-issues/issues/109) — LJM Source Tests
- [#51](https://github.com/waterloo-rocketry/2025-software-issues/issues/51) — Parse CAN messages from data_processing_v2 (Jack-Brown12)
- [parsley#61](https://github.com/waterloo-rocketry/parsley/pull/61) — Add to_flat_dict (Jack-Brown12)
- [omnibus#454](https://github.com/waterloo-rocketry/omnibus/pull/454) — Add client timestamp (Jack-Brown12)
- [parsley-ts#1](https://github.com/waterloo-rocketry/parsley-ts/pull/1) — Zod-based CAN message type definitions (ChrisYx511)

**What's not started:**
- [#27](https://github.com/waterloo-rocketry/2025-software-issues/issues/27) — Docker Compose orchestration for Omnibus deployment
- [#101](https://github.com/waterloo-rocketry/2025-software-issues/issues/101) — Update Parsley source to use new parsers
- [#100](https://github.com/waterloo-rocketry/2025-software-issues/issues/100) — Use typed parses in Parsley to build parsing payloads
- [#115](https://github.com/waterloo-rocketry/2025-software-issues/issues/115) — Implement the parsing of received CAN/Message schema
- [#114](https://github.com/waterloo-rocketry/2025-software-issues/issues/114) — Implement the sending of CAN/Command type Omnibus Messages
- [#113](https://github.com/waterloo-rocketry/2025-software-issues/issues/113) — Send CAN/Message messages from a Mock Backend
- [#120](https://github.com/waterloo-rocketry/2025-software-issues/issues/120) — Integrate parsley-ts payload schemas with omnibus-ts CAN message types
- [#110](https://github.com/waterloo-rocketry/2025-software-issues/issues/110) — Improve LJM Source Docker Image size

**Assessment:** This is the most mature project. The core infrastructure (uv workspace, Docker containers, omnibus-ts library, bridge) is largely in place. The LJM data source has been prototyped and is now being tested and refined. The deployment story is advancing with Docker Compose and Ansible. Key remaining work: Docker Compose orchestration (#27), CAN message schema parsing (#115, #114), and several unassigned tasks for mock backends and Parsley integration. The Log Parsing Improvements epic (#49) is active with Jack-Brown12 contributing client timestamp and flat dict features.

---

### Project [#5](https://github.com/waterloo-rocketry/2025-software-issues/issues/5): Website Design Refresh & Infrastructure Refresh
**Status: Early/stalled, ~15% complete**

**Goal:** Redesign the Waterloo Rocketry website and add infrastructure improvements (InvenTree, IaC).

**What's done:**
- [website-react#115](https://github.com/waterloo-rocketry/website-react/pull/115) — TypeScript migration merged
- [website-react#113](https://github.com/waterloo-rocketry/website-react/pull/113) — Sponsor package updated
- [website-react#122](https://github.com/waterloo-rocketry/website-react/pull/122) — Outreach page updated

**What's in progress:**
- [website-react#123](https://github.com/waterloo-rocketry/website-react/pull/123) — Smaller sponsorship package (str4wb3rrytea, ~5 weeks stale)
- [website-react#119](https://github.com/waterloo-rocketry/website-react/pull/119) — TS dependencies (str4wb3rrytea, ~4 months stale)
- [website-react#118](https://github.com/waterloo-rocketry/website-react/pull/118) — Home-new hidden page (jennnniferkuang, ~4 months stale)
- [website-react#117](https://github.com/waterloo-rocketry/website-react/pull/117) — New home page (str4wb3rrytea, ~4 months stale)
- [#47](https://github.com/waterloo-rocketry/2025-software-issues/issues/47) — TypeScript on all surfaces (jennnniferkuang)
- [#44](https://github.com/waterloo-rocketry/2025-software-issues/issues/44) — Coordinate branding with media team
- [#43](https://github.com/waterloo-rocketry/2025-software-issues/issues/43) — Create design mockups

**What's not started:**
- [#32](https://github.com/waterloo-rocketry/2025-software-issues/issues/32) — Set up monitoring, alerting for InvenTree
- [#31](https://github.com/waterloo-rocketry/2025-software-issues/issues/31) — Implement IaC with Terraform and Ansible
- [#30](https://github.com/waterloo-rocketry/2025-software-issues/issues/30) — Deploy InvenTree with Caddy
- [#29](https://github.com/waterloo-rocketry/2025-software-issues/issues/29) — Docker infrastructure for Oracle Cloud VM
- [#45](https://github.com/waterloo-rocketry/2025-software-issues/issues/45) — Collect team feedback on design options

**Assessment:** This project has stalled significantly. The website redesign PRs (#117, #118, #119) haven't been updated in ~4 months. The TypeScript migration was completed, but the design mockup and branding coordination stories (#43, #44) show no recent activity. The entire InvenTree infrastructure epic (#7) has not started. This project needs re-engagement from jennnniferkuang and str4wb3rrytea, or a scope adjustment.

---

### Project [#8](https://github.com/waterloo-rocketry/2025-software-issues/issues/8): Telemetry Monitoring System
**Status: Early stage, ~15% complete**

**Goal:** Build a standalone Electron-based telemetry monitoring app that reflects rocket architecture, capable of operating independently with a Parsley source.

**What's done:**
- [#34](https://github.com/waterloo-rocketry/2025-software-issues/issues/34) — Parsley code quality audit story (CLOSED)
- [#72](https://github.com/waterloo-rocketry/2025-software-issues/issues/72) — React Component for Board Data (CLOSED)
- [#15](https://github.com/waterloo-rocketry/2025-software-issues/issues/15) — Onboard log parsing support (CLOSED)
- Various Parsley tests and quality improvements (CLOSED: #73, #74, #64, #68, #63, #77, #76, #95)

**What's in progress:**
- [avionics-testing-app#6](https://github.com/waterloo-rocketry/omnibus-avionics-testing-app/pull/6) — Board status display (john-jpet, ~7 weeks stale)
- [avionics-testing-app#8](https://github.com/waterloo-rocketry/omnibus-avionics-testing-app/pull/8) — Omnibus-TS connection management (john-jpet, ~7 weeks stale)
- [avionics-testing-app#7](https://github.com/waterloo-rocketry/omnibus-avionics-testing-app/pull/7) — CAN sender prototype (Zarar3, ~5 weeks stale)
- [avionics-testing-app#9](https://github.com/waterloo-rocketry/omnibus-avionics-testing-app/pull/9) — Mock backend (Vaishali-Anapayan)
- [#33](https://github.com/waterloo-rocketry/2025-software-issues/issues/33) — Parsley code quality audit (yashjain128, ShreyShingala, Theni1)
- ShreyShingala has active Parsley-related omnibus PRs (#467, #468, #469)

**What's not started:**
- [#36](https://github.com/waterloo-rocketry/2025-software-issues/issues/36) — Standalone Electron application
- [#37](https://github.com/waterloo-rocketry/2025-software-issues/issues/37) — Internal Omnibus server orchestration
- [#38](https://github.com/waterloo-rocketry/2025-software-issues/issues/38) — External Omnibus server connectivity
- [#39](https://github.com/waterloo-rocketry/2025-software-issues/issues/39) — Telemetry operator interface design
- [#41](https://github.com/waterloo-rocketry/2025-software-issues/issues/41) — CAN command sender interface
- [#42](https://github.com/waterloo-rocketry/2025-software-issues/issues/42) — Package as Electron application
- [#35](https://github.com/waterloo-rocketry/2025-software-issues/issues/35) — Enhance Parsley message parsing

**Assessment:** The Avionics Testing App (Epic #11) was the initial proving ground for this project, and it has made some progress with board status display and CAN sender prototypes. However, the avionics testing app PRs have gone stale (~7 weeks without updates). The broader Telemetry Monitoring System stories (Electron packaging, server orchestration, operator interface) are entirely unstarted. Parsley quality improvements continue through ShreyShingala's active work. This project needs significant acceleration to meet its goals — the Electron app stories need to be assigned and started.

---

### Project [#14](https://github.com/waterloo-rocketry/2025-software-issues/issues/14): OpenRocket Plugin Development
**Status: Early stage, ~5% complete**

**Goal:** TBD — OpenRocket plugin development led by vincentjguo.

**What's done:**
- No closed issues directly under this project.

**What's in progress:**
- [#49](https://github.com/waterloo-rocketry/2025-software-issues/issues/49) — Log Parsing Improvements epic (vincentjguo, Sameek-Sharma, Jack-Brown12, RoshanD15)

**Assessment:** This project has minimal description and unclear success criteria. The Log Parsing Improvements epic (#49) is the primary active workstream under vincentjguo's leadership, with Jack-Brown12 contributing CAN message parsing and client timestamp features. The project needs its goals and success criteria defined.
