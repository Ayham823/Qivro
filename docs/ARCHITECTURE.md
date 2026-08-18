# Qivro Architecture Notes

## Request Path

```mermaid
sequenceDiagram
    participant U as User
    participant W as Next.js Web
    participant N as Nginx
    participant B as NestJS API
    participant P as PostgreSQL
    participant R as Redis
    participant A as FastAPI AI

    U->>W: Search or property action
    W->>N: HTTPS request
    N->>B: Route /api request
    B->>R: Cache, limits, or queue state
    B->>P: Authorized domain query
    opt Language understanding is useful
        B->>A: Structured AI request
        A-->>B: Validated structured response
    end
    B-->>W: Stable JSON contract
    W-->>U: Localized product state
```

## Design Principles

1. The Backend owns business rules, authorization, and persistence.
2. Frontend applications consume stable HTTP contracts.
3. The AI service is an adapter boundary, not a source of authority.
4. Redis supports caching, rate limiting, queues, and realtime coordination.
5. Long-running or retryable work belongs in background workers.
6. Public traffic enters through Nginx; internal services use Docker DNS.
7. External providers are optional adapters with deterministic fallbacks where appropriate.

## Data and AI Safety

- Original owner-entered property content is preserved.
- Generated translations are versioned and reviewed before publication.
- Model responses are validated before affecting product behavior.
- Property facts are sourced from Qivro data, not invented by a model.
- Secrets and provider keys stay outside browser applications and Git history.

## Environment Progression

The current architecture targets a Docker Compose environment on a single
Linux host. The service boundaries are designed to permit later movement to
managed PostgreSQL, managed Redis, container registries, load balancing, and
orchestrated compute without rewriting the product domains.
