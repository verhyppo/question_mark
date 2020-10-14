# Database

```sql
CREATE TABLE "users" (
  "id" SERIAL PRIMARY KEY,
  "email" varchar,
  "created_at" timestamp
);

CREATE TABLE "passions" (
  "id" SERIAL PRIMARY KEY,
  "name" varchar NOT NULL
);

CREATE TABLE "behaviors" (
  "id" SERIAL PRIMARY KEY,
  "name" varchar NOT NULL
);

CREATE TABLE "user_passion" (
  "id" SERIAL PRIMARY KEY,
  "user_id" int,
  "passion_id" int,
  "value" int
);

CREATE TABLE "user_behavior" (
  "id" SERIAL PRIMARY KEY,
  "user_id" int,
  "behavior_id" int,
  "value" int
);

ALTER TABLE "users" ADD FOREIGN KEY ("id") REFERENCES "user_passion" ("user_id");

ALTER TABLE "users" ADD FOREIGN KEY ("id") REFERENCES "user_behavior" ("user_id");

ALTER TABLE "passions" ADD FOREIGN KEY ("id") REFERENCES "user_passion" ("passion_id");

ALTER TABLE "behaviors" ADD FOREIGN KEY ("id") REFERENCES "user_behavior" ("behavior_id");

```