# AzureVoice

Minimal scaffold for AzureVoice — a music business platform (catalog, licensing, copyright, analytics).

Getting started (local):
1. Copy `.env.example` -> `.env` and fill values (DATABASE_URL, REDIS_URL, SPOTIFY_CLIENT_ID, SPOTIFY_CLIENT_SECRET, NEXTAUTH_SECRET, etc).
2. Start infra (docker-compose): `docker-compose up -d`
3. Install deps: `npm install` or `yarn`
4. Run migrations: `npx prisma migrate dev`
5. Start dev: `npm run dev` (Next.js)
6. Start worker (in separate terminal): `npm run worker`

Tech stack (MVP):
- Next.js + TypeScript (apps/web)
- Chakra UI (UI library; replaceable)
- Prisma + PostgreSQL
- Redis + BullMQ for queue/worker
- Vercel recommended for deployment

See `.env.example` for required environment variables.
