# Cerințe

Prioritizare MoSCoW: **M** = obligatoriu, **S** = important, **C** = dorit dacă rămâne timp.

## Cerințe funcționale

| ID | Cerință | Prioritate |
|---|---|---|
| FR-01 | Utilizatorul își poate crea cont cu email și parolă. | M |
| FR-02 | Utilizatorul se poate autentifica și deconecta. | M |
| FR-03 | Utilizatorul poate crea, edita, vedea și șterge obiective (titlu, descriere, termen). | M |
| FR-04 | Utilizatorul poate crea, edita, vedea și șterge task-uri asociate unui obiectiv. | M |
| FR-05 | Un task are durată estimată, prioritate, termen și status (de făcut, în lucru, finalizat). | M |
| FR-06 | Utilizatorul poate porni și opri un cronometru pe un task; timpul se salvează ca sesiune de lucru. | M |
| FR-07 | Utilizatorul poate adăuga manual timp lucrat pe un task. | S |
| FR-08 | Progresul unui obiectiv se calculează automat din task-urile finalizate. | M |
| FR-09 | Dashboard-ul afișează obiectivele active cu progres și task-urile cu termen azi. | M |
| FR-10 | Aplicația afișează statistici lunare: task-uri finalizate, timp total, estimat vs. real. | M |
| FR-11 | Aplicația afișează statistici anuale, defalcate pe luni. | M |
| FR-12 | Task-urile se pot filtra după status, obiectiv și perioadă. | S |
| FR-13 | Obiectivele se pot grupa pe categorii. | C |
| FR-14 | Utilizatorul poate exporta statisticile în CSV. | C |
| FR-15 | Utilizatorul primește un indicator vizual pentru task-urile întârziate. | S |

## Cerințe nefuncționale

| ID | Cerință | Prioritate |
|---|---|---|
| NFR-01 | Parolele se stochează hash-uite (BCrypt), niciodată în plaintext. | M |
| NFR-02 | Fiecare utilizator vede doar datele proprii. | M |
| NFR-03 | Paginile principale se încarcă în sub 2 secunde pe o conexiune normală. | S |
| NFR-04 | Interfața este utilizabilă pe desktop și pe telefon (design responsiv). | S |
| NFR-05 | API-ul respectă convențiile REST și returnează coduri HTTP corecte. | M |
| NFR-06 | Codul este versionat în Git, iar modificările intră prin Pull Request. | M |
| NFR-07 | Logica de calcul a statisticilor are teste automate. | S |
| NFR-08 | Aplicația rulează local cu o singură comandă (Docker Compose). | C |
