# Long Chansamanakreaksa (Reaksa)

**Backend Developer · Phnom Penh, Cambodia**

I build backend systems that handle real complexity domain-driven Python services, typed Node.js APIs, CI/CD pipelines, and AI-integrated applications. Currently targeting backend and full-stack roles across Cambodia and Southeast Asia.

---

## Featured Projects

### REMA — Rapid Emergency Medical Access

Humanitarian logistics system for the **Viet Nam Red Cross**. Delivers emergency medical kits to flood-affected households in Ho Chi Minh City within 24–48 hours.

Built solo as a university challenge entry (4-person team scope). The system handles:

- **3-layer warehouse model** — central warehouse → 3 district sub-warehouses → last-mile delivery
- **20-point household prioritization scoring** — medical urgency, vulnerability, flood exposure, self-sufficiency, isolation
- **Water-depth-adaptive routing** — motorbike (0–30 cm) → bicycle/foot (30–60 cm) → boat (60–80 cm) → suspended (>80 cm)
- **Role-based access control** — 5 roles: SUPER_ADMIN, EMERGENCY_COORDINATOR, HUB_MANAGER, VOLUNTEER, VIEWER
- **AI-powered operational brief** — Emergency Coordinators generate a live situation summary via Anthropic Claude (advisory only, no PII)
- **113 automated unit tests** gating every deployment via GitHub Actions CI/CD

**Stack:** Node.js · TypeScript · Express · Prisma · PostgreSQL · React · Tailwind CSS · Recharts · Leaflet.js · Anthropic API · Docker · GitHub Actions · Render · Supabase · Vercel

| | |
|---|---|
| Frontend | https://rema-system.vercel.app  |
| Backend API | https://rema-medical-logistics.onrender.com |
| Swagger docs | https://rema-medical-logistics.onrender.com/api/docs |
| Repository | [longreaksa404/rema-medical-logistics](https://github.com/longreaksa404/rema-medical-logistics) |

**Test accounts** (password: `rema1234`):

| Role | Email |
|---|---|
| Emergency Coordinator | coordinator@rema.vn |
| Hub Manager | hub1@rema.vn |
| Volunteer | volunteer1@rema.vn |
| Viewer | viewer@rema.vn |

---

## Tech Stack

| Category | Tools |
|---|---|
| **Node.js ecosystem** | TypeScript · Express · Prisma · Jest + ts-jest · JWT · Swagger |
| **Python ecosystem** | Django · DRF · Celery · Redis · Pytest · Gunicorn · Nginx |
| **Frontend** | React (Vite) · TypeScript · Tailwind CSS · Recharts · Leaflet.js |
| **Databases** | PostgreSQL · MySQL · Redis |
| **Infrastructure** | Docker · Docker Compose · GitHub Actions · Render · Supabase · Vercel |
| **AI** | Anthropic Claude API (`@anthropic-ai/sdk`) — server-side integration |
| **Practices** | Domain-Driven Design · RBAC · Audit trails · REST APIs · CI/CD |

---

## Engineering Practices

**Testing discipline:** Every project has automated tests. REMA has 113 unit tests covering the scoring engine, activation trigger, stock scarcity logic, and route selection all pure functions, all CI-gated. IMS has 35+ tests covering domain logic and API behavior.

**CI/CD:** GitHub Actions runs tests on every pull request. PRs are blocked if tests fail. Merging to `main` triggers an automatic Render redeploy. This is enforced via branch protection not just configured.

**Security:** JWT authentication with bcrypt (cost factor 12), role-based access control on every endpoint, secrets managed via environment variables only (never committed). API keys are server-side only never in the frontend bundle.

**Audit trails:** Every stock movement in both projects creates an immutable log record. Nothing is deleted only deactivated.

---

## Connect

- **LinkedIn:** [Long Chansamanakreaksa](https://www.linkedin.com/in/long-chansamanakreaksa-64930b34b)
- **Email:** helloworldreaksa@gmail.com
- **GitHub:** [@longreaksa404](https://github.com/longreaksa404)
