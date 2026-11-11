# Goal Tracker

Aplicație web pentru urmărirea obiectivelor și a task-urilor: utilizatorul își definește obiective, le descompune în task-uri cu timp estimat, își măsoară timpul real, vede progresul și primește statistici lunare și anuale.

## Problema abordată

Obiectivele personale și academice se pierd ușor între liste de task-uri, calendare și notițe. Lipsesc două lucruri: o legătură clară între un obiectiv și task-urile lui și o imagine despre cât timp s-a lucrat efectiv și cât s-a finalizat. Goal Tracker rezolvă asta într-un singur loc.

## Obiective

- Permite crearea de obiective și de task-uri asociate lor.
- Măsoară timpul estimat și timpul real pentru fiecare task.
- Afișează progresul fiecărui obiectiv (procent de task-uri finalizate).
- Generează statistici lunare și anuale despre task-urile efectuate.

## Utilizatori vizați

- Studenți care își urmăresc proiectele, examenele și deprinderile.
- Persoane care lucrează independent și vor să-și monitorizeze productivitatea.

## Echipa și responsabilități

| Membru | Rol principal | Responsabilități |
|---|---|---|
| Flavius A. | _de completat_ | _de completat_ |
| _Membru 2_ | _de completat_ | _de completat_ |
| _Membru 3_ | _de completat_ | _de completat_ |

> Completați tabelul. Fiecare membru trebuie să-și poată prezenta și justifica contribuția la prezentarea orală.

## Funcționalități propuse

- Înregistrare și autentificare.
- CRUD pentru obiective (titlu, descriere, termen, categorie).
- CRUD pentru task-uri (titlu, obiectiv, prioritate, durată estimată, termen, status).
- Cronometru pe task și introducere manuală de timp.
- Marcarea task-urilor ca finalizate și calculul automat al progresului.
- Dashboard cu progresul obiectivelor și task-urile de azi.
- Statistici lunare și anuale: task-uri finalizate, timp total lucrat, timp estimat vs. real.
- Filtrare și căutare după status, obiectiv, perioadă.

## Tehnologii alese (propunere)

| Strat | Tehnologie |
|---|---|
| Frontend | React + Vite, Chart.js pentru grafice |
| Backend | Java 21, Spring Boot (REST API, Spring Security cu JWT) |
| Bază de date | PostgreSQL |
| Versionare | Git + GitHub (flux pe branch-uri și Pull Request-uri) |

Justificarea completă este în [docs/implementation-plan.md](docs/implementation-plan.md).

## Documentație

- [Cerințe funcționale și nefuncționale](docs/requirements.md)
- [Scenarii de utilizare](docs/use-cases.md)
- [Wireframe-uri și fluxuri de navigare](docs/wireframes/README.md)
- [Arhitectura aplicației](docs/architecture.md)
- [Model de date și endpoint-uri](docs/data-model.md)
- [Plan de implementare](docs/implementation-plan.md)
