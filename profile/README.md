# Yakoon

<img src="../brand/png/yakoon-dark.png" width="210" alt="Yakoon">

**An open-source operating environment for executable capabilities.**

A pack brings capabilities into a Yakoon environment. A capability is an
executable, describable and controllable action — a command. Yakoon
provides the shared operational framework in which these capabilities
run: runtime, identity, permissions, stores, resources, audit, hosts,
scheduling, resolution and lifecycle.

`yak` makes capabilities travel: from source to pack, into a
distribution, through discovery and installation, into an assembled
environment — as a running capability.

## The model

```text
                  PACKS
                    │
           bring capabilities
                    │
                    ▼
              ┌──────────┐
              │  YAKOON  │
              └────┬─────┘
                   │
          shared command world
                   │
        ┌──────────┼──────────┐
        ▲          ▲          ▲
      Human     Software    AI Agent
```

Packs bring capabilities. Yakoon provides the infrastructure they
shouldn't have to build themselves. Capabilities are exposed as commands
in one shared command world.

## Packs

What "a pack brings capabilities" means in practice — capabilities are
grouped by domain, not by technology:

```text
 CRM            Billing          Project       Infrastructure
  │               │                 │                │
  ▼               ▼                 ▼                ▼
customer.*      invoice.*        project.*        backup.*
contact.*       payment.*        task.*           database.*
...             sepa.*           ...              tunnel.*
```

*`Billing`, `Project` and `Infrastructure` are illustrative examples.
`CRM` is a real pack in this organization.*

## Actors

All of them are actors within the same identity and permission
boundaries. Because commands are describable and reachable through one
command world, AI becomes a natural actor — not a special one:

```text
                 Identity / Session
                        │
                        ▼
                      Actor
                        │
             ┌──────────┼──────────┐
             ▼          ▼          ▼
           Human     Software   AI Agent
             │          │          │
             └──────────┼──────────┘
                        ▼
                     Commands
                        │
                Permissions / Scope
                        │
                        ▼
             Resources / Capabilities
```

> **What a human can do in Yakoon, an AI agent can do as well — but no
> more.**

## Repositories

Each repository describes itself. From top to bottom:

| Repository | What it is |
|---|---|
| `developer` | The entry point — a ready-to-run Yakoon workspace |
| `runtime` | The runtime and the platform model |
| `sdk` | Build components against Yakoon |
| `apps` | Platform tools, including `yak` |
| `caps-system` | Foundational system capabilities |
| `caps-ident` | Identity and authorization capabilities |
| `caps-contacts` | CRM capabilities |
| `caps-worlds` | Spatial memory capabilities |
| `caps-labs` | Experiments |
| `launcher` | The bootstrap — `pip install yakoon` |

## Status

Yakoon is under active development. The platform runs, components install
and assemble into environments, and their capabilities are available
through a shared command model.

> Yakoon provides infrastructure. Caps bring executable capabilities.
> Humans, software and AI can use them.
