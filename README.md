<div align="center">

<img src="assets/hero.svg" alt="Mahir Hasan Sifat, backend engineer in Dhaka, Bangladesh" width="100%" />

</div>

## About

I build the backend parts that have to be right: payments, wallets, concurrency, migrations and event pipelines. Day to day that's **.NET and PostgreSQL** on a B2B/B2C online travel platform. On the side I chase problems until I find the actual root cause, and I like writing it up so the next person doesn't have to.

I came up through competitive programming (ICPC, Codeforces, CodeChef), so I still think in complexity and edge cases first. I'm **open to relocation and remote work**.

<div align="center">

<img src="assets/stats.svg" alt="200+ stored procedures migrated, 100+ blocking defects fixed, ICPC Dhaka Regional 2023 61st place, 2500+ problems solved" width="100%" />

</div>

## What I've shipped

<div align="center">

<img src="assets/pipeline.svg" alt="Animation: a payment request passes the Redis idempotency check, is committed to PostgreSQL with an outbox row, published to Kafka and delivered by FCM, while a duplicate retry is rejected at Redis" width="100%" />

<sub>The reliability work in one loop: the first request goes through, the retry with the same key is stopped at Redis.</sub>

</div>

- **PostgreSQL migration** &mdash; moved 200+ SQL Server stored procedures to PostgreSQL functions across booking, ticketing, refunds and accounting, with behaviour parity against the legacy system. Then stabilised the rollout by fixing 100+ release-blocking defects across payments, invoicing and financial reports.
- **Money-safe concurrency** &mdash; Redis-backed idempotency service and a fault-tolerant distributed lock manager. Fixed race conditions in agent wallet top-up approval by redesigning the database locking.
- **Event-driven notifications** &mdash; Kafka pipeline with FCM push delivery supporting single-user, group and exclusion-based targeting.
- **Shared data-access layer** &mdash; one abstraction over EF Core and Dapper across SQL Server and PostgreSQL, used by the team's services.
- **Security** &mdash; TOTP two-factor authentication, and browser-fingerprint validation on login and token refresh against session hijacking.
- **Performance** &mdash; used APM traces to find slow endpoints, then fixed them through execution-plan analysis.

## Things I'm building

### [Notif Guardian](https://github.com/mahir-hs/notif-guardian) &nbsp;<sub>Kotlin · Jetpack Compose · Android</sub>
Notifications from WhatsApp, Telegram and Gmail arriving late on Xiaomi, Redmi and POCO phones is a known, annoying problem, and "turn on autostart" doesn't fix it. I traced it on a real device to HyperOS's *Millet* freezer cgroup-freezing Google Play services (the FCM host) on screen-off, because it was missing from the system's no-restrict list. Notif Guardian detects and repairs that. A small helper app re-adds protected apps within about 20 ms whenever the system rewrites the list.
**[Read the write-up and docs &rarr;](https://mahir-hs.github.io/notif-guardian/)**

### [ParcelTrack](https://github.com/mahir-hs/ParcelTrack) &nbsp;<sub>.NET 10 · PostgreSQL · Kafka · Redis · Keycloak · YARP</sub>
Multi-carrier parcel tracking for Bangladeshi couriers (Pathao, Steadfast, RedX). Six services: a YARP and Keycloak gateway, shipment (Clean Architecture and CQRS with a transactional outbox), tracking with Polly circuit breakers, notifications, and HMAC-signed webhook dispatch. A learning project where I worked through failure semantics properly instead of just drawing boxes.

### [GPS-Tracking](https://github.com/mahir-hs/GPS-Tracking) &nbsp;<sub>Go · MQTT · TimescaleDB · Redis · WebSocket</sub>
Device location ingestion over MQTT into TimescaleDB, streamed live to clients over WebSocket, all in Docker Compose.

### Research &mdash; brain MRI tumour classification with graph neural networks
Four-class classification by modelling each MRI as a 256-node patch graph (GATv2). Reached 98.78% mean accuracy over three seeds, then found that the first image-level split leaked near-duplicates and rebuilt the evaluation with duplicate-group-aware splits, shuffled-edge controls and leave-one-source-out testing. I trust the lower, honest number more than the first flattering one.

## Toolbox

<div align="center">

![C#](https://img.shields.io/badge/C%23-512BD4?style=for-the-badge&logo=csharp&logoColor=white)
![.NET](https://img.shields.io/badge/.NET_10-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=microsoftsqlserver&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Angular](https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white)

</div>

**Patterns I reach for:** Clean Architecture · CQRS · transactional outbox · idempotency keys · distributed locking · event-driven design · Testcontainers-backed integration tests

## Competitive programming

| Where | Result |
|---|---|
| ICPC Asia Dhaka Regional 2023 | **61st place** |
| IUBAT Collaborative Contest 2023 | 7th place |
| Codeforces | Specialist, max rating **1412** |
| CodeChef | 3&#9733;, max rating **1606** (best rank 85th, top 0.3%) |
| Overall | 300+ contests, 2,500+ problems solved across Codeforces, CodeChef, AtCoder, LightOJ, UVa, Toph and LeetCode |

I also served as Judging Director of the DIU Take-Off Programming Contest (set and tested 15+ problems) and teach DSA classes.

## Education and languages

**BSc in Computer Science and Engineering**, Daffodil International University, 2020&ndash;2024, CGPA 3.66/4.00.
Bangla (native) · English (IELTS Academic 7.0) · German (learning)

## Say hello

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-mah1r-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mah1r)
[![Email](https://img.shields.io/badge/Email-mahirhasan333@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:mahirhasan333@gmail.com)
[![LeetCode](https://img.shields.io/badge/LeetCode-renzaluar-FFA116?style=for-the-badge&logo=leetcode&logoColor=white)](https://leetcode.com/renzaluar/)

<img src="https://capsule-render.vercel.app/api?type=waving&height=100&color=0:06b6d4,50:1d4ed8,100:0f172a&section=footer" alt="" />

</div>
