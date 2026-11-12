# celestial-bodies-database
Relational PostgreSQL database modeling galaxies, stars, planets, moons, and space missions for the freeCodeCamp Relational Database Certification.

# Celestial Bodies Database

A relational PostgreSQL database built for the **freeCodeCamp Relational Database Certification** (`Celestial Bodies Database` project).

## Database Schema

The `universe` database consists of five normalized tables with primary keys, foreign key relationships, `UNIQUE` constraints, and `NOT NULL` data integrity rules:

* **`galaxy`** — Stores galaxy classifications, distances from Earth (in million light-years), ages, and active galactic nucleus status.
* **`star`** — References `galaxy(galaxy_id)` and records spectral types, surface temperatures (Kelvin), solar masses, and main-sequence status.
* **`planet`** — References `star(star_id)` and details planet types, orbital periods, habitability, and sphericity.
* **`moon`** — References `planet(planet_id)` and tracks moon diameters, orbital periods, and sphericity.
* **`space_mission`** — Tracks notable space exploration missions, launch years, agencies, and crew status.

## Recreating the Database

To restore the database locally using PostgreSQL:

```bash
psql -U postgres < universe.sql
