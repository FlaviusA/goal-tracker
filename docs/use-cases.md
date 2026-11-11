# Scenarii de utilizare

Fiecare scenariu are precondiții, pași și rezultat verificabil.

## UC-01: Crearea unui obiectiv cu task-uri

- **Actor:** utilizator autentificat
- **Precondiții:** utilizatorul este logat.
- **Flux principal:**
  1. Utilizatorul apasă „Obiectiv nou”.
  2. Completează titlul („Licență”), descrierea și termenul (30 iunie 2027) și salvează.
  3. Sistemul afișează pagina obiectivului, cu progres 0%.
  4. Utilizatorul apasă „Adaugă task”, introduce „Scrie capitolul 1”, durată estimată 4 ore, prioritate înaltă, și salvează.
  5. Sistemul afișează task-ul în lista obiectivului, cu statusul „De făcut”.
- **Flux alternativ:** dacă titlul lipsește, sistemul afișează eroare și nu salvează.
- **Rezultat verificabil:** obiectivul și task-ul apar în listă și rămân după reîncărcarea paginii.

## UC-02: Lucrul pe un task cu cronometru și finalizarea lui

- **Actor:** utilizator autentificat
- **Precondiții:** există un obiectiv cu cel puțin un task cu statusul „De făcut”.
- **Flux principal:**
  1. Utilizatorul deschide task-ul și apasă „Start”.
  2. Sistemul trece task-ul în „În lucru” și pornește cronometrul.
  3. După un timp, utilizatorul apasă „Stop”.
  4. Sistemul salvează sesiunea (început, sfârșit, durată) și actualizează timpul total al task-ului.
  5. Utilizatorul apasă „Finalizează”.
  6. Sistemul marchează task-ul „Finalizat”, salvează data finalizării și recalculează progresul obiectivului.
- **Flux alternativ:** utilizatorul adaugă manual 45 de minute dacă a uitat să pornească cronometrul; sistemul creează o sesiune cu durata respectivă.
- **Rezultat verificabil:** progresul obiectivului crește (ex. de la 0% la 25% pentru 1 din 4 task-uri), iar timpul real al task-ului este suma sesiunilor.

## UC-03: Consultarea statisticilor lunare și anuale

- **Actor:** utilizator autentificat
- **Precondiții:** există task-uri finalizate în cel puțin o lună.
- **Flux principal:**
  1. Utilizatorul deschide pagina „Statistici”.
  2. Alege vizualizarea „Lunar” și luna dorită (noiembrie 2026).
  3. Sistemul afișează numărul de task-uri finalizate, timpul total lucrat și raportul estimat vs. real.
  4. Utilizatorul trece pe „Anual” și alege 2026.
  5. Sistemul afișează un grafic cu task-urile finalizate pe fiecare lună și totalul anual.
- **Flux alternativ:** pentru o perioadă fără activitate, sistemul afișează „Nu există date” și valori 0.
- **Rezultat verificabil:** valorile afișate coincid cu datele din baza de date (verificabil prin teste pe serviciul de statistici).

## UC-04: Înregistrare și autentificare

- **Actor:** vizitator
- **Flux principal:**
  1. Vizitatorul deschide pagina „Înregistrare” și introduce email și parolă.
  2. Sistemul creează contul cu parola hash-uită.
  3. Utilizatorul se autentifică, iar sistemul returnează un token și îl redirecționează la dashboard.
- **Flux alternativ:** dacă emailul există deja, sistemul afișează eroare; dacă parola este greșită la login, sistemul afișează „Date incorecte” fără să spună care câmp e greșit.
- **Rezultat verificabil:** fără token valid, API-ul răspunde cu 401 la orice endpoint protejat.
