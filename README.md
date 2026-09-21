# Tom Lasswell

**Director of IT** &nbsp;·&nbsp; Atlanta, GA &nbsp;·&nbsp; [lasswell.me](https://lasswell.me)

I lead IT infrastructure and service delivery — data center, cloud, security, and the
operating model that holds them together. Twenty years in, most of the work is
organizational: deciding what to standardize, what to retire, and who owns the thing
at 3 a.m.

I also never stopped writing code. The Home Assistant integration further down this
page runs in roughly 5,400 homes. Keeping something in production that strangers
depend on is the cheapest way I know to stay honest about what I ask engineers to do.

---

## How I think about the work

**Infrastructure is a product.** Core systems earn the same rigor as software —
roadmaps, service levels, versioning, a named owner. The moment the network has a
backlog instead of a ticket queue, the business starts talking about it differently.

**Governance should accelerate decisions, not queue them.** Most change advisory
boards are a tax on velocity that buys no safety. Guiding principles used as decision
filters push judgment down to the people holding the context.

**The service desk is the product surface.** It is where the entire IT organization is
actually evaluated. Staffing it like a cost center and then wondering why IT has no
credibility is a self-inflicted wound.

**Ship it.** Perfect is the enemy of shipped, and a platform nobody uses is a rounding
error no matter how elegant the architecture.

---

## Writing

A ten-part series on modernizing ITSM for cloud-native, multi-framework organizations:

- [Why ITSM Still Matters in a Cloud-Native, Agile, Multi-Framework World](https://lasswell.me/why-itsm-still-matters-in-a-cloud-native-agile-multi-framework-world/)
- [The Service Value System: Connecting Strategy to Execution](https://lasswell.me/the-service-value-system-how-to-connect-strategy-to-execution-through-value-streams/)
- [Governance Without Gridlock: Agility and Accountability in Service Delivery](https://lasswell.me/governance-without-gridlock-balancing-agility-and-accountability-in-service-delivery/)
- [Infrastructure as a Product: Treating Core Systems With the Rigor of Software](https://lasswell.me/infrastructure-as-a-product-treating-core-systems-with-the-same-rigor-as-software/)
- [Change Enablement in a DevOps World: Replacing Fear With Velocity and Trust](https://lasswell.me/change-enablement-in-a-devops-world-replacing-fear-of-change-with-velocity-and-trust/)
- [Service Portfolios & Productization: Defining and Managing IT Services](https://lasswell.me/service-portfolios-productization-defining-marketing-and-managing-it-services/)

Earlier series cover technology leadership, tech roadmaps, and the outsourcing versus
in-housing decision. Full archive at **[lasswell.me](https://lasswell.me)**.

---

## Code

Leadership is the day job. This is the part that keeps me fluent.

### Home Assistant

Two HACS integrations, both written against cloud APIs that were never documented
for this purpose. Between them they cover most of what is plugged in at my house.

#### Govee

[![Active installs](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/lasswellt/govee-homeassistant/badges/installs.json)](https://analytics.home-assistant.io/)
[![Stars](https://img.shields.io/github/stars/lasswellt/govee-homeassistant?style=flat-square&color=e3b341&label=stars)](https://github.com/lasswellt/govee-homeassistant)
[![Forks](https://img.shields.io/github/forks/lasswellt/govee-homeassistant?style=flat-square&color=8b949e&label=forks)](https://github.com/lasswellt/govee-homeassistant/network/members)
[![Release](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/lasswellt/govee-homeassistant/badges/release.json)](https://github.com/lasswellt/govee-homeassistant/releases)

A HACS custom component covering Govee lights, plugs, fans, humidifiers, heaters,
sensors, and leak hubs. Capability-based rather than SKU-based — entities are built
from what each device advertises, so new models in a known class generally work
without a release. Real-time push over Govee's AWS IoT MQTT, with automatic local LAN
control and cloud fallback. Python, MIT, released most weeks, and by a wide margin
the most-used thing I have shipped.

Accepted into the **[HACS default registry](https://github.com/hacs/default)** in
January 2026, so it installs from inside HACS without adding a custom repository.

**[→ lasswellt/govee-homeassistant](https://github.com/lasswellt/govee-homeassistant)**

#### Navien NaviLink

[![Quality scale](https://img.shields.io/badge/quality%20scale-gold-FFD700?style=flat-square)](https://developers.home-assistant.io/docs/core/integration-quality-scale/)
[![Release](https://img.shields.io/github/v/release/lasswellt/navien-homeassistant?style=flat-square&color=41BDF5&label=release)](https://github.com/lasswellt/navien-homeassistant/releases)
[![License](https://img.shields.io/github/license/lasswellt/navien-homeassistant?style=flat-square&color=41BDF5)](https://github.com/lasswellt/navien-homeassistant/blob/main/LICENSE)

Tankless water heaters and combi-boilers over the NaviLink cloud. The interesting
part is the client: REST authentication, AWS SigV4 WebSocket signing and an MQTT
transport, written from scratch and asyncio-native, with no `boto3` and no
`AWSIoTPythonSDK` — `paho-mqtt` driven on the event loop with no background network
thread. Telemetry is capability-gated, so a unit only grows the entities it actually
has.

**[→ lasswellt/navien-homeassistant](https://github.com/lasswellt/navien-homeassistant)**

### Omarchy

I run [Omarchy](https://omarchy.org) as my daily driver and write bar plugins for it.
Both of these answer the same question — *how much of my AI quota is left* — for
tools that do not otherwise say.

Each is a `service` plus a `bar-widget`: a collector emits one JSON usage record in
the same contract Omarchy's first-party collectors use, a QML service publishes it on
a timer, and both the built-in Agents panel and the plugin's own panel read that one
file. One data path, two views, so they cannot disagree.

| Plugin | What it surfaces |
|---|---|
| **[omarchy-copilot](https://github.com/lasswellt/omarchy-copilot)** | GitHub Copilot premium-request quota with a reset countdown, AI credits, tokens by day and model, and which repositories the work happened in. Quota is read live from the CLI's JSON-RPC runtime rather than its cache, and costs no premium requests to collect. |
| **[omarchy-antigravity](https://github.com/lasswellt/omarchy-antigravity)** | Google Antigravity limits across all four quota buckets, merged across the `agy` CLI and the IDE because the quota is account-wide. Ships a smoke suite that fails loudly if Antigravity's JSON envelope changes shape. |

Both MIT, both QML with shell and Python collectors.

### Everything else

| Project | What it is | Built with |
|---|---|---|
| **[blitz-cc](https://github.com/lasswellt/blitz-cc)** | A language-agnostic agentic development loop for Claude Code — sprint workflow, agents, quality gates | Shell, Markdown |
| **[cc-metrics](https://github.com/lasswellt/cc-metrics)** | Self-hosted OpenTelemetry dashboard for Claude Code token use and cost | JavaScript, OTel |
| **[claudeHQ](https://github.com/lasswellt/claudeHQ)** | Workforce management for Claude Code: monitor and control sessions across machines from one dashboard | Nuxt 3, Vuetify, TypeScript |
| **[signalslate](https://github.com/lasswellt/signalslate)** | One morning page — mail, calendar, tasks and chat across every account, rendered to PDF and pushed to a reMarkable | Python, Docker |
| **[flight-search](https://github.com/lasswellt/flight-search)** | Flight search on the Amadeus API — Vue frontend, Express backend, and an MCP server so assistants can query it directly | Vue 3, Express, MCP |
| **[remodel-planner](https://github.com/lasswellt/remodel-planner)** | Room-by-room remodel planner: SVG floorplan with snapping, phase-gated tasks, budgets, permits | TypeScript, Firebase |

Two platforms are in private development: **CubeSP**, a multi-portal ITSM/PSA platform
for MSPs, and **MEMBRIX**, a membership and event operating system. Both are
TypeScript monorepos on Vue 3 and Firebase.

Architecture notes live in
**[playbook-library](https://github.com/lasswellt/playbook-library/wiki)**, a wiki-only
repository. Its centerpiece is a multi-project Quasar and Firebase playbook — several
independently deployed apps sharing one Firebase backend, composed through module
federation — with three runnable companion repos as its worked example:
[host](https://github.com/lasswellt/pb-example-host),
[knowledge](https://github.com/lasswellt/pb-example-knowledge) and
[administration](https://github.com/lasswellt/pb-example-administration).

---

## Stack

Azure and AWS, Kubernetes and Docker, Firebase and Firestore. Python for integrations
and automation, TypeScript and Vue 3 for products, PowerShell where the fleet lives.
Datadog and Microsoft Sentinel for observability, Azure DevOps for pipelines, SQL
throughout — plus a working knowledge of every ITIL practice I have opinions about.

---

## Connect

[LinkedIn](https://www.linkedin.com/in/lasswellt/) &nbsp;·&nbsp;
[lasswell.me](https://lasswell.me) &nbsp;·&nbsp;
[Medium](https://lasswellt.medium.com) &nbsp;·&nbsp;
[X](https://x.com/TomLasswell)
