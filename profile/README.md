# Yakoon

**An open-source operating environment for executable capabilities.**

A pack brings capabilities into a Yakoon environment. A capability is an
executable, describable and controllable action — a command. Yakoon
provides the shared operational framework in which these capabilities
run: runtime, identity, permissions, stores, resources, audit, hosts,
scheduling, resolution and lifecycle.

`yak` makes capabilities travel: from source to pack, into a
distribution, through discovery and installation, into an assembled
environment — as a running capability.

```text
         AUTHOR
           │
       builds Pack
           │
           ▼
     Distribution
           │
           ▼
          yak
           │
      Installation
           │
       Assembly
           │
           ▼
       YAKOON OS
           │
           ▼
     new Capability
           │
           ▼
         ACTOR
   Human · AI · Software
```

Capabilities are used by humans, by software and by AI agents. All of
them are actors within the same identity and permission boundaries.
Because commands are describable and reachable through one command
world, AI becomes a natural actor — not a special one:

> **What a human can do in Yakoon, an AI agent can do as well — but no
> more.**

## Repositories

Each repository describes itself. From top to bottom:

| Repository | What it is |
|---|---|
| `developer` | The entry point — a ready-to-run Yakoon workspace |
| `runtime` | The runtime and the platform model |
| `sdk` | Build packs against Yakoon |
| `apps` | Platform tools, including `yak` |
| `pack-system` | Foundational OS capabilities |
| `pack-ident` | Identity and authorization |
| `pack-crm` | A real domain pack on Yakoon |
| `pack-luma` | Spatial memory |
| `pack-labs` | Experiments |
| `launcher` | The bootstrap — `pip install yakoon` |
| `dists` | Where built packs are distributed from |

## Status

Yakoon is under active development. The platform runs, packs install and
assemble into an environment, and capabilities are usable by humans and
AI agents today.

> Yakoon provides infrastructure. Packs bring executable capabilities.
> Humans, software and AI use them.
