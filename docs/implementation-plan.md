# Plan de implementare

## Justificarea tehnologiilor

| Alegere | Motiv |
|---|---|
| Java 21 + Spring Boot | Cunoscut de cel puțin un membru; structură clară (controller, service, repository); Spring Security gata făcut pentru JWT. |
| PostgreSQL | Date relaționale clare (utilizator, obiectiv, task, sesiune); agregări SQL bune pentru statistici. |
| React + Vite | Interfață dinamică (cronometru, grafice); ecosistem mare. |
| Chart.js | Grafice simple, suficiente pentru statistici lunare și anuale. |
| Docker Compose | Pornirea bazei de date și a aplicației identic pe toate calculatoarele echipei. |



## Strategia de versionare

- Branch-ul `main` conține doar cod funcțional.
- Fiecare funcționalitate se face pe un branch propriu: `feature/<nume-scurt>` (ex. `feature/timer`).
- Modificările intră în `main` prin Pull Request, aprobat de cel puțin un alt membru.
- Mesaje de commit scurte, la imperativ: `Adaugă endpoint pentru statistici lunare`.
- Task-urile echipei se urmăresc în GitHub Issues sau într-un board GitHub Projects.

## Planul de implementare

| Etapa | Conținut | Cerințe | Prioritate |
|---|---|---|---|
| 1. Fundație | Repo, structura proiectului, baza de date, Docker Compose | NFR-06, NFR-08 | Mare |
| 2. Autentificare | Register, login, JWT, izolarea datelor | FR-01, FR-02, NFR-01, NFR-02 | Mare |
| 3. Obiective și task-uri | CRUD, status, progres | FR-03, FR-04, FR-05, FR-08 | Mare |
| 4. Timp | Cronometru, sesiuni, timp manual | FR-06, FR-07 | Mare |
| 5. Dashboard | Obiective active, task-uri de azi, întârzieri | FR-09, FR-15 | Medie |
| 6. Statistici | Endpoint-uri lunare și anuale, grafice, teste | FR-10, FR-11, NFR-07 | Mare |
| 7. Finisare | Filtre, design responsiv, remedieri | FR-12, NFR-04 | Medie |
| 8. Opțional | Categorii, export CSV | FR-13, FR-14 | Mică |

## Repartizarea responsabilităților (de completat)

| Zonă | Responsabil |
|---|---|
| Backend: autentificare și securitate | _Flavius/Raul_ |
| Backend: obiective, task-uri, timp | _Flavius_ |
| Backend: statistici și teste | _Flavius_ |
| Frontend: autentificare, dashboard | _Raul_ |
| Frontend: obiective, task-uri, cronometru | _Raul_ |
| Frontend: statistici și grafice | _Raul_ |
| Documentație, wireframe-uri, prezentare | _Flavius_ |

## Riscuri

| Risc | Măsură |
|---|---|
| Timp insuficient | Se implementează întâi cerințele M; cele C se lasă la final. |
| Membri cu nivel tehnic diferit | Lucru în perechi și revizuire reciprocă prin Pull Request. |
| Calcule greșite la statistici | Teste automate pe serviciul de statistici. |
