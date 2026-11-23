# The Welders Guild (companion page)

This repository is a lightweight public shell for **The Welders Guild**.

The working application — founding roll, member portal, certification review,
coins/tiers, job board, and admin console — lives in
[`guild-server`](https://github.com/glenngerbrick-ship-it/guild-server).

## How the two repos fit together

| Repo | Role |
|---|---|
| **welders-guild** (this one) | Static companion / marketing face |
| **guild-server** | Express + SQLite app that serves the real site and APIs |

## Run the real app

```bash
cd ../guild-server   # or clone that repo
npm install
cp .env.example .env # set ADMIN_USER, ADMIN_PASS, SESSION_SECRET
npm start
```

- Public site — http://localhost:3000
- Guild Hall — http://localhost:3000/portal
- Admin — http://localhost:3000/admin

Optional demo data (fresh DB only):

```bash
npm run demo
```

Every demo account password is printed when seeding finishes.

## Preview this companion page

```bash
python3 -m http.server 8080
# open http://localhost:8080
```
