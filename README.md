
````markdown
# 🗄️ OneArmy-Compatible PostgreSQL Schema

This repository contains a `schema.sql` script that defines a PostgreSQL schema mirroring the Firebase structure of the [OneArmy Community Platform](https://github.com/OneArmyWorld/Community-Platform).

It provides a clean, relational schema to serve as the backend for a self-hosted admin interface (e.g., built with [Refine.dev](https://refine.dev)) and replaces Firebase with PostgreSQL or a Supabase-compatible database.

---

## 📦 Features

✅ Clean, blank-slate schema (no seed data)  
✅ Tables for all major OneArmy Community Platform entities  
✅ Compatible with PostgreSQL or Supabase  
✅ Ready for use with Refine-based admin tools

---

## 📁 Schema Overview

| Table Name        | Description                                          |
|-------------------|------------------------------------------------------|
| `users`           | Core user profiles                                   |
| `roles`           | Role definitions (admin, moderator, user, etc.)      |
| `user_roles`      | Many-to-many mapping of users to roles               |
| `howtos`          | Step-by-step user-generated guides                   |
| `howto_steps`     | Individual steps within a how-to                     |
| `researches`      | Research-style posts with updates                    |
| `research_updates`| Update logs tied to research posts                   |
| `events`          | Community events or meetups                          |
| `comments`        | Comments on any type of post                         |
| `tags`            | Content tags                                         |
| `howto_tags`      | Tags linked to how-to posts                          |
| `research_tags`   | Tags linked to research posts                        |
| `event_tags`      | Tags linked to events                                |

---

## ⚙️ Usage

1. **Create a new PostgreSQL database**  
   You can use any PostgreSQL instance (local, Supabase, or cloud).

2. **Run the schema script:**

   ```bash
   psql -U your_user -d your_database -f schema.sql
````

Or if using Supabase CLI:

```bash
supabase db reset
supabase db push --file schema.sql
```

3. **Connect your frontend**
   Point your Refine or admin app to the newly created schema and start building.

---

## ✅ Requirements

* PostgreSQL 13 or higher
* Refine frontend or other CMS layer (not included)
* No preexisting tables with conflicting names
* Optional: Supabase for hosted Postgres and auth

---

## 🚫 No Data Migrations

This script assumes a **fresh install**.
There is **no support for migrating Firebase data** at this stage. Future migration tooling may be added later.

---

## 🔗 Resources

* [OneArmy Community Platform](https://github.com/OneArmyWorld/Community-Platform)
* [Refine.dev](https://refine.dev/)
* [Supabase](https://supabase.com/)

---

> *Maintained by SkairCrow for use in the AdminDash project, supporting decentralized and self-hosted community infrastructure.*

```
