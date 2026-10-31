<div align="center">

<img src="assets/banner.svg" alt="Animated 3D wireframe globe with orbiting rings and spinning solids above a neon perspective grid" width="100%" />

<h1>Mahir Hasan Sifat</h1>

**I solve hard problems for fun, then build backends that keep them solved.**

Dhaka, Bangladesh &nbsp;·&nbsp; open to relocation and remote

[![LinkedIn](https://img.shields.io/badge/LinkedIn-mah1r-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mah1r)
[![Codeforces](https://img.shields.io/badge/Codeforces-Mah1r-1F8ACB?style=flat-square&logo=codeforces&logoColor=white)](https://codeforces.com/profile/Mah1r)
[![Email](https://img.shields.io/badge/Email-say%20hi-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:mahirhasan333@gmail.com)

</div>

<br/>

## The arena

I've been competing since 2020. This is what that looks like when you plot it, straight from the Codeforces API: 3,070 submissions and 120 rated contests, including the stretch where my rating collapsed and the climb back.

<div align="center">

<img src="assets/cp_journey.svg" alt="Codeforces rating over 120 contests: fell to 517, climbed to a personal best of 1412. 1,389 problems solved, 629 active days, 20 day streak, hardest solved 2300." width="100%" />

<br/><br/>

<img src="assets/cp_heat.svg" alt="Heatmap of 3,070 Codeforces submissions from 2020 to 2024, with breakdowns by difficulty and topic" width="100%" />

</div>

- **ICPC Asia Dhaka Regional 2023: [61st](https://bapsoj.org/contests/icpc-dhaka-regional-site-2023/standings).** Also 7th at the IUBAT Collaborative Contest 2023 and a BUET IUPC 2023 team.
- **42 problems rated 1700 or higher**, the hardest at 2300, from a rating that once sat at 517.
- **96% C++.** Peak hours are 8 to 10 PM Dhaka time, and the busiest month was April 2020 with 168 submissions.
- **2,500+ problems and 300+ contests** across eight judges: Codeforces, CodeChef, AtCoder, LeetCode, LightOJ, Toph, UVa and VJudge. Codeforces alone accounts for 1,389 of them.
- I also set and tested 15+ contest problems as Judging Director of the DIU Take-Off Programming Contest.

<div align="center">

[![Codeforces](https://img.shields.io/badge/Codeforces-Mah1r-1F8ACB?style=for-the-badge&logo=codeforces&logoColor=white)](https://codeforces.com/profile/Mah1r)
[![CodeChef](https://img.shields.io/badge/CodeChef-foxxin-5B4638?style=for-the-badge&logo=codechef&logoColor=white)](https://www.codechef.com/users/foxxin)
[![AtCoder](https://img.shields.io/badge/AtCoder-renzaluar-222222?style=for-the-badge&logo=atcoder&logoColor=white)](https://atcoder.jp/users/renzaluar)
[![LeetCode](https://img.shields.io/badge/LeetCode-renzaluar-FFA116?style=for-the-badge&logo=leetcode&logoColor=white)](https://leetcode.com/renzaluar/)
[![Toph](https://img.shields.io/badge/Toph-Mah1r__-2c3e50?style=for-the-badge)](https://toph.co/u/Mah1r_)
[![LightOJ](https://img.shields.io/badge/LightOJ-renzaluar-F5A623?style=for-the-badge)](https://lightoj.com/user/renzaluar)

</div>

<br/>

## Things I build when nobody's asking

### [Notif Guardian](https://github.com/mahir-hs/notif-guardian) &nbsp;<sub>Kotlin · Jetpack Compose</sub>
My Xiaomi phone kept delivering WhatsApp messages hours late. The usual advice is "enable autostart", and that wasn't the problem. So I went digging on the device and found the real culprit: HyperOS's *Millet* freezer was cgroup-freezing Google Play services, the process that carries every push notification, the moment the screen turned off. It was missing from a system no-restrict list, and the OS rewrote that list whenever it liked. Notif Guardian repairs it, and a tiny helper app puts it back within about 20 ms each time the system wipes it.
**[How it works &rarr;](https://mahir-hs.github.io/notif-guardian/)**

### [ParcelTrack](https://github.com/mahir-hs/ParcelTrack) &nbsp;<sub>.NET 10 · Kafka · Postgres · Redis · YARP</sub>
Six microservices that follow parcels across Pathao, Steadfast and RedX: a gateway, a shipment service on Clean Architecture and CQRS with a transactional outbox, circuit-breaker polling, and HMAC-signed webhooks. A playground for the part of distributed systems nobody draws on the whiteboard: what happens on the retry.

### [GPS-Tracking](https://github.com/mahir-hs/GPS-Tracking) &nbsp;<sub>Go · MQTT · TimescaleDB · WebSocket</sub>
Devices publish over MQTT, positions land in TimescaleDB, and clients watch them move live over WebSocket. All of it runs from one `docker compose up`.

### Brain MRI &times; graph neural networks &nbsp;<sub>Python · PyTorch Geometric</sub>
Each scan becomes a 256-node graph and a GATv2 classifies four tumour types at 98.78%. Then I found my first train/test split had leaked near-duplicate images, threw out the flattering number and rebuilt the evaluation properly. I trust the honest one more.

<br/>

## By day: making retries harmless

I work on payments, wallets and a large SQL Server to PostgreSQL migration for a travel platform. The recurring theme is making sure that doing something twice is the same as doing it once. Below is that idea in one loop: the first request goes through, the retry with the same key is stopped at Redis.

<div align="center">

<img src="assets/pipeline.svg" alt="Animation: a request passes the Redis idempotency check, is committed to PostgreSQL with an outbox row, published to Kafka and delivered by FCM, while a duplicate retry is rejected at Redis" width="100%" />

</div>

<br/>

<div align="center">

![C#](https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=csharp&logoColor=white)
![.NET](https://img.shields.io/badge/.NET-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=kotlin&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Angular](https://img.shields.io/badge/Angular-DD0031?style=flat-square&logo=angular&logoColor=white)

<sub>Competitive stats are pulled from the Codeforces API and regenerated from the raw submission data.</sub>

</div>
