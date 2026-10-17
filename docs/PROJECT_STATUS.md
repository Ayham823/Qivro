# Qivro Project Status

This document prevents planned ideas from being confused with implemented or
connected capabilities.

| Area | Status | Notes |
| --- | --- | --- |
| Customer web application | Implemented locally | Responsive Next.js application with localized routes |
| Property discovery and details | Implemented locally | Search, filters, details, favorites, and saved searches |
| Owner property management | Implemented locally | Draft, validation, media, preview, publish, and edit flows |
| Authentication and authorization | Implemented locally | Backend-controlled identity, roles, and ownership checks |
| Messaging and notifications | Implemented locally | Human conversations and localized system notifications |
| Admin operations console | Foundation implemented | Moderation, analytics, audit, review, and system views |
| PostgreSQL and Prisma | Implemented locally | Schema, migrations, seeds, and backup/restore contracts |
| Redis and BullMQ | Implemented locally | Cache, limits, queues, and worker contracts |
| Multilingual product | Implemented locally | English, Arabic, Hebrew, RTL, formatting, and SEO foundations |
| AI provider boundary | Implemented locally | Mock plus configurable external text-provider adapters |
| Production AI providers | Provider-dependent | Requires approved accounts, keys, budgets, and monitoring |
| Payments | In development | Production provider and full webhook lifecycle not claimed |
| AI media and 3D | In development | Contracts and foundations exist; production processing is not claimed |
| Public live deployment | Not available | Screenshots come from deterministic local seed data |
| Managed AWS services | Planned progression | No live inventory is claimed from repository documentation |
| Native iOS product | Early foundation | Not presented as a finished application |

## October 2026 source update\n\nNew local source areas include map clustering and building links, owner insights, shared-living and household workflows, privacy/consent contracts, and native marketplace-read adapters. These remain development work pending coordinated review and release acceptance. See the [development update](DEVELOPMENT_UPDATE_2026_10.md); the existing status rows above do not imply full production coverage.\n\n## Terminology

- **Implemented locally** means the behavior exists and has been exercised in
  the local Qivro environment.
- **Foundation implemented** means meaningful structure exists, but the area is
  not presented as complete.
- **Provider-dependent** means code integration alone is not evidence of a live
  account or production operation.
- **Planned progression** describes an architectural direction, not a delivered feature.
