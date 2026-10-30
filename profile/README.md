# magnify

**Construction documentation, virtual site tours and project portals for developers and real-estate stakeholders.**
Amman, Jordan · Cairo, Egypt · [magnify-vt.com](https://magnify-vt.com)

---

## What we build

magnify turns site visits into structured, searchable project records: scheduled 360° capture, automated processing, progress and as-built virtual tours, technical data, and a secure portal for every client.

## Platform map

| Repository | System | Status |
|---|---|---|
| `magnify-works` | Internal operations: photo-editing tracking, QC, photographer scheduling | Running (internal) |
| `magnify-data` | Technical data collection: submittals, data sheets, nameplates by discipline / system / room | In development |
| `magnify-studio` | Tour production workspace: all tour tools behind one interface | In development |
| `magnify-capture` | Android field app for photographers (Insta360 capture → upload) | In development |
| `magnify-cleaner` | Batch AI cleaning of 360° panoramas (tripod, people, clutter), runs locally | In development |
| `magnify-autotour` | Automatic tour generation from walkthrough video + floor plans | Research |
| `magnify-player` | magnify web tour player (progress and layered as-built tours) | Planned |
| `magnify-portal` | Client portal: each client sees only their own projects, tours and documents | Planned |
| `magnify-infra` | Server, database and deployment configuration | Planned |
| `magnify-docs` | Architecture, database design, roles, roadmap, security | Active |

## Architecture at a glance

```
Sales order (ERPNext) ─► Projects & scheduling ─► Field capture app ─► Storage
                                                                         │
     Client portal ◄── Tour player ◄── Studio / automated processing ◄──┘
```

One database, one set of users and permissions, separate modules.
Full details live in `magnify-docs`.

## Principles

- **Client data stays protected.** Client imagery is processed on our own machines, never sent to third-party AI services.
- **Automation first.** Every project moves from sales order to delivered tour with as few manual steps as possible.
- **One system.** Shared users, roles and projects across every module.

---

© magnify. All repositories are private and proprietary.
