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

### Govee for Home Assistant

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

**[→ lasswellt/govee-homeassistant](https://github.com/lasswellt/govee-homeassistant)**

### Everything else

| Project | What it is | Built with |
|---|---|---|
| **[blitz-cc](https://github.com/lasswellt/blitz-cc)** | A language-agnostic agentic development loop for Claude Code — sprint workflow, agents, quality gates | Shell, Markdown |
| **[cc-metrics](https://github.com/lasswellt/cc-metrics)** | Self-hosted OpenTelemetry dashboard for Claude Code token use and cost | JavaScript, OTel |
| **[claudeHQ](https://github.com/lasswellt/claudeHQ)** | Workforce management for Claude Code: monitor and control sessions across machines from one dashboard | Nuxt 3, Vuetify, TypeScript |
| **[signalslate](https://github.com/lasswellt/signalslate)** | One morning page — mail, calendar, tasks and chat across every account, rendered to PDF and pushed to a reMarkable | Python, Docker |
| **[navien-homeassistant](https://github.com/lasswellt/navien-homeassistant)** | HACS integration for Navien NaviLink water heaters | Python |
| **[remodel-planner](https://github.com/lasswellt/remodel-planner)** | Room-by-room remodel planner: SVG floorplan with snapping, phase-gated tasks, budgets, permits | TypeScript, Firebase |
| **[omarchy-copilot](https://github.com/lasswellt/omarchy-copilot)** · **[omarchy-antigravity](https://github.com/lasswellt/omarchy-antigravity)** | Status bar widgets for the GitHub Copilot CLI and Google Antigravity | Python, Shell |

Two platforms are in private development: **CubeSP**, a multi-portal ITSM/PSA platform
for MSPs, and **MEMBRIX**, a membership and event operating system. Both are
TypeScript monorepos on Vue 3 and Firebase.

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
