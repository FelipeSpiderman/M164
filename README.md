# Datenbank Modul Lernportfolio

Dokumentation des Lernportfolios und der bearbeiteten Themen im Datenbank Modul.

---

## Lektion vom 13.05.2025

**Wichtigste Themen:**

- Einführung in relationale Datenbanken
- Grundlagen der Datenmodellierung (Entitäten, Attribute, Beziehungen)
- Einführung in ER-Diagramme (logisch)
- Überblick über SQL und seine Hauptkategorien (DDL, DML, DQL, DCL, TCL)
- Installation und Einrichtung von MySQL/MariaDB
- Erste Schritte mit MySQL Workbench

**Kurze Zusammenfassung / Kernkonzepte:**

Die erste Lektion führte in die Grundlagen relationaler Datenbanken ein, mit Fokus auf die Datenmodellierung. Entitäten (z. B. Tabellen), Attribute (Spalten) und Beziehungen (1:1, 1:n, m:n) wurden definiert, und die Erstellung logischer ER-Diagramme wurde geübt. Ein Überblick über SQL wurde gegeben, einschließlich seiner Hauptkategorien: DDL (Strukturdefinition), DML (Datenmanipulation), DQL (Datenabfrage), DCL (Zugriffskontrolle) und TCL (Transaktionskontrolle). Praktisch wurde MySQL/MariaDB installiert, und die ersten Schritte mit MySQL Workbench (z. B. Verbindung zur Datenbank, einfache Schemata) wurden durchgeführt. Ziel war es, ein grundlegendes Verständnis für die Struktur und Verwaltung relationaler Datenbanken zu schaffen.

**Wichtige Befehle/Konzepte:**

- Grundkonzepte: Entitäten, Attribute, Primär- und Fremdschlüssel.
- Beziehungen: 1:1, 1:n, m:n.
- SQL-Kategorien: DDL (`CREATE`, `ALTER`, `DROP`), DML (`INSERT`, `UPDATE`, `DELETE`), DQL (`SELECT`), DCL (`GRANT`, `REVOKE`), TCL (`COMMIT`, `ROLLBACK`).
- MySQL Workbench: Verbindung herstellen, einfache Schemata erstellen.

**Checkpoint-Fragen (Reflexion):**

- Was ist der Unterschied zwischen einer Entität und einem Attribut?
- Welche Arten von Beziehungen gibt es in einem ER-Diagramm?
- Welche SQL-Kategorien gibt es, und wofür werden sie verwendet?
- Warum ist MySQL Workbench nützlich für die Datenmodellierung?

**Auftrag:**

- Einfache ER-Diagramme skizzieren (z. B. für eine Bibliotheksdatenbank).
- MySQL/MariaDB installieren und eine Testdatenbank anlegen.
- Ergebnisse und Skripte im Lernportfolio ablegen.

---

## Lektion vom 20.05.2025

**Wichtigste Themen:**

- Recap Tag 1 und Lösungen
- Datenmodellierung: Generalisierung/Spezialisierung
- Beziehungsarten: Identifying vs. Non-Identifying Relationships
- Datenbank Management Systeme (DBMS): Merkmale, Vor-/Nachteile, Produkte
- DDL (Data Definition Language): `CREATE SCHEMA/DATABASE`, `CREATE TABLE`, `DROP TABLE`, `ALTER TABLE`
- Zeichensätze (Character Sets)
- Nutzung von MySQL Workbench (Forward Engineering, Synchronize Model)
- Recherche zu fortgeschrittenen Themen (Partition, Storage Engine, Tablespace)

**Kurze Zusammenfassung / Kernkonzepte:**

Diese Lektion vertiefte die Datenmodellierung mit Generalisierung/Spezialisierung zur Reduzierung von Redundanz ("is_a"-Beziehung). Wir lernten den Unterschied zwischen Identifying (Child-PK enthält Parent-FK) und Non-Identifying Relationships (Child-PK unabhängig vom Parent-FK). Ein zentrales Thema war das DBMS, dessen Funktionen (Datenhaltung, DQL, DDL, DML, DCL, TCL, Konsistenzkontrolle, Transaktionen), Vor- und Nachteile sowie Produkte (z. B. MySQL, MariaDB, PostgreSQL). Praktisch wurde mit DDL-Befehlen gearbeitet (`CREATE SCHEMA`, `CREATE TABLE`, `DROP TABLE`, `ALTER TABLE ADD/DROP/CHANGE/MODIFY`), und die Bedeutung von Zeichensätzen (`utf8mb4`) für Datenkodierung wurde hervorgehoben. MySQL Workbench wurde für Forward Engineering (DDL-Skripte aus Modellen) und Synchronize Model (Abgleich Modell-Datenbank) eingesetzt.

**Wichtige DDL-Befehle:**

- `CREATE SCHEMA db_name;` (oder `DATABASE`)
- `CREATE TABLE table_name (...);`
- `DROP TABLE table_name;`
- `ALTER TABLE table_name ADD column_name datatype;`
- `ALTER TABLE table_name DROP column_name;`
- `ALTER TABLE table_name CHANGE old_col_name new_col_name datatype;`
- `ALTER TABLE table_name MODIFY column_name new_datatype;`

**Checkpoint-Fragen (Reflexion):**

- Warum Generalisierung/Spezialisierung?
- Wie wird eine Identifying Beziehung in SQL erstellt?
- Welche Befehle gehören zur DDL-Gruppe?

**Auftrag:**

- ER-Diagramm mit Generalisierung/Spezialisierung erstellen.
- DDL-Skripte für ein einfaches Schema schreiben und in MySQL Workbench testen.
- Ergebnisse und Skripte im Lernportfolio ablegen.

---

## Lektion vom 27.05.2025

**Wichtigste Themen:**

- Vertiefung Datentypen in MariaDB/MySQL
- Komplexere Beziehungsmodelle: Mehrfachbeziehungen, Rekursion (strenge Hierarchie), einfache Hierarchie (Zwischentabelle), Stücklistenproblem
- Repetition und Anwendung von DML-Befehlen (`INSERT`, `UPDATE`, `DELETE`)
- Repetition und Anwendung von DQL-Befehlen (`SELECT`)
- Erweiterung und Befüllung des "Tourenplaner"-Schemas
- Nutzung von MySQL Workbench für Forward Engineering

**Kurze Zusammenfassung / Kernkonzepte:**

Die Lektion behandelte fortgeschrittene Beziehungstypen wie Mehrfachbeziehungen, rekursive Beziehungen (Hierarchien) und das Stücklistenproblem, inklusive deren Umsetzung (z. B. Zwischentabellen). DML-Befehle (`INSERT`, `UPDATE`, `DELETE`) und DQL-Befehle (`SELECT` mit `WHERE`, `ORDER BY`) wurden wiederholt und angewendet. Das "Tourenplaner"-Schema wurde erweitert, mittels Forward Engineering in der Datenbank umgesetzt und mit Beispieldaten gefüllt, mit Fokus auf hierarchische Daten. Die Datenkorrektheit wurde mit `SELECT`-Abfragen überprüft.

**Wichtige Befehle/Konzepte:**

- SQL-Datentypen (z. B. `INT`, `VARCHAR`, `DATE`).
- Modellierung von 1:mc und m:n Beziehungen (Rekursion/Hierarchie).
- DML: `INSERT INTO ... VALUES ...;`, `UPDATE ... SET ... WHERE ...;`, `DELETE FROM ... WHERE ...;`
- DQL: `SELECT ... FROM ... WHERE ... ORDER BY ...;`, Nutzung von JOINs.
- Forward Engineering in MySQL Workbench.

**Checkpoint-Fragen (Reflexion):**

- Welche Schwierigkeiten treten bei FK-Constraints auf?
- Warum sind NULL-Werte in Hierarchie-Tabellen unzulässig?
- Wann verwendet man Zwischentabellen statt rekursiver Beziehungen?
- Welche SQL-Datentypen sind für bestimmte Daten geeignet?

**Auftrag:**

- Erweiterung des "Tourenplaner"-Schemas mit rekursiven Beziehungen.
- DML- und DQL-Befehle anwenden, Daten einfügen und abfragen.
- Ergebnisse und Skripte im Lernportfolio ablegen.

---

## Lektion vom 03.06.2025

**Wichtigste Themen:**

- Datenbankbeziehungen mit Constraints
- Anwendung von Constraints mit Forward Engineering und `ALTER TABLE`
- Grundlagen der Mengenlehre und Bezug zu Datenbanken
- Vertiefung von `SELECT`-JOINs (`INNER`, `LEFT`, `RIGHT`, `FULL OUTER`)
- Abfragen über mehrere Tabellen

**Kurze Zusammenfassung / Kernkonzepte:**

Die Lektion fokussierte auf die Umsetzung von Beziehungen im physischen Modell mit Constraints (`NOT NULL`, `UNIQUE`, Fremdschlüssel) zur Sicherstellung der referentiellen Integrität. MySQL Workbench generierte diese Constraints via Forward Engineering, und manuelle Anpassungen wurden mit `ALTER TABLE ADD CONSTRAINT FOREIGN KEY` geübt. Die Verbindung zwischen Mengenlehre (Schnittmenge, Vereinigungsmenge) und SQL-JOINs (`INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN`) wurde hergestellt. Praktische Übungen umfassten komplexe Abfragen über mehrere Tabellen.

**Wichtige Befehle/Konzepte:**

- Referentielle Integrität.
- Constraints: `NOT NULL`, `UNIQUE`, `FOREIGN KEY`.
- `ALTER TABLE ADD CONSTRAINT FOREIGN KEY (...) REFERENCES ... (...);`
- Mengenlehre: ∩ (`INNER JOIN`), ∪ (`FULL OUTER JOIN`), \ (Differenz).
- JOIN-Typen: `INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN`.
- `GROUP BY`, `GROUP_CONCAT`.

**Checkpoint-Fragen (Reflexion):**

- Was ist referentielle Integrität?
- Welche Constraints gibt es für Beziehungen?
- Unterschied zwischen `LEFT JOIN` und `RIGHT JOIN`?
- Wie werden 1:1- und m:n-Beziehungen umgesetzt?
- Was passiert bei ungültigen FK-Einträgen ohne Constraints?

**Auftrag:**

- ER-Diagramm mit Constraints erstellen und via Forward Engineering umsetzen.
- JOIN-Abfragen über mehrere Tabellen durchführen.
- Ergebnisse und Skripte im Lernportfolio ablegen.

---

## Lektion vom 10.06.2025

**Wichtigste Themen:**

- Datenlöschung und Datenintegrität
- Fremdschlüssel-Regeln (`ON DELETE`)
- `SELECT` mit ALIAS
- Aggregatsfunktionen (`COUNT`, `SUM`, `AVG`, `MIN`, `MAX`)
- `GROUP BY` und `HAVING`
- Reihenfolge der `SELECT`-Klauseln

**Kurze Zusammenfassung / Kernkonzepte:**

Die Lektion behandelte, warum Daten in professionellen Datenbanken selten physisch gelöscht werden, um Integrität und Nachvollziehbarkeit zu gewährleisten. Fremdschlüssel-Constraints (`ON DELETE NO ACTION/RESTRICT`, `CASCADE`, `SET NULL`) wurden konfiguriert. Fortgeschrittene `SELECT`-Operationen umfassten ALIAS, Aggregatsfunktionen, `GROUP BY` und `HAVING`. Die Reihenfolge der `SELECT`-Klauseln (MERKSATZ: Sag Fritz...) wurde betont.

**Wichtige Befehle/Konzepte:**

- Datenintegrität: Genauigkeit, Konsistenz, Vollständigkeit.
- `ON DELETE` Optionen: `NO ACTION`, `RESTRICT`, `CASCADE`, `SET NULL`.
- `SELECT column AS alias`, `SELECT * FROM table AS alias JOIN ...`.
- Aggregatsfunktionen: `COUNT()`, `SUM()`, `AVG()`, `MIN()`, `MAX()`.
- `GROUP BY column1, column2, ...`, `HAVING condition`.
- `SELECT ... FROM ... JOIN ... WHERE ... GROUP BY ... HAVING ... ORDER BY ... LIMIT ...`.

**Checkpoint-Fragen (Reflexion):**

- Was sind die fünf Aspekte der Datenintegrität?
- Unterschied zwischen Datenintegrität und -konsistenz?
- Gefahr bei `ON DELETE CASCADE`?
- Unterschied zwischen `COUNT(*)` und `COUNT(attr)`?
- Wann wird `HAVING` verwendet?

**Auftrag:**

- Fremdschlüssel-Regeln in einem Schema implementieren.
- Abfragen mit Aggregatsfunktionen und `GROUP BY`/`HAVING` erstellen.
- Ergebnisse und Skripte im Lernportfolio ablegen.

---

## Lektion vom 17.06.2025

**Wichtige Themen:**

- Subqueries (skalare/nicht-skalare)
- Bulkimport mit `LOAD DATA INFILE`
- CSV-Datenanpassung (Datumsformate, Spaltenreihenfolge)
- Normalisierung in 3. Normalform (3NF)
- Redundanzprüfung und -bereinigung
- Datenübertragung mit `INSERT INTO ... SELECT ...`
- Arbeiten mit `db_adressen`

**Kurze Zusammenfassung / Kernkonzepte:**

Die Lektion behandelte Subqueries (skalare: ein Wert; nicht-skalare: Listen mit `IN`) und den effizienten CSV-Import mit `LOAD DATA INFILE`, inklusive Anpassungen (z. B. `STR_TO_DATE`, `CASE`). Die Datenbank `db_adressen` wurde in 3NF normalisiert (`tbl_Person`, `tbl_Str`, `tbl_Ort`). Redundanzen wurden mit `GROUP BY`/`HAVING` geprüft und bereinigt, Daten mit `INSERT INTO ... SELECT ...` übertragen und mit `SELECT ... JOIN ...` validiert.

**Wichtige Befehle:**

- Skalare Subquery: `SELECT ... WHERE col < (SELECT MIN(col) FROM ...);`
- Nicht-skalare Subquery: `SELECT ... WHERE col IN (SELECT col FROM ...);`
- `LOAD DATA [LOCAL] INFILE 'path/file.csv' INTO TABLE ... FIELDS TERMINATED BY ',' LINES TERMINATED BY '\r\n' IGNORE 1 ROWS;`
- `SET col = STR_TO_DATE(@var, '%d.%m.%Y');`, `SET col = CASE WHEN @var = 'val' THEN x ELSE y END;`
- Redundanzprüfung: `SELECT col, COUNT(*) FROM table GROUP BY col HAVING COUNT(*) > 1;`

**Checkpoint-Fragen:**

- Zweck von Subqueries?
- Unterschied skalare vs. nicht-skalare Subqueries?
- Bedeutung von `IGNORE 1 ROWS` in `LOAD DATA INFILE`?
- Folgen falscher `LINES TERMINATED BY`-Einstellung?
- Einstellungen für `LOAD DATA LOCAL INFILE`?

**Auftrag:**

- Subselect-Aufgabe (35 Min, Einzelarbeit).
- CSV-Import mit `LOAD DATA LOCAL INFILE` (30 Min, Partnerarbeit): `db_adressen` erstellen, Daten in 3NF normalisieren, Redundanzen bereinigen, Ergebnisse prüfen.
- Ergebnisse und Skripte im Lernportfolio ablegen.

---

## Lektion vom 24.06.2025

**Wichtige Themen:**

- Datenbanksicherung: Konzepte und Methoden
- Backup-Typen: Voll-, differentielles, inkrementelles Backup
- Backup-Tools: `mysqldump`, phpMyAdmin, Mariabackup, Workbench
- Normalisierung der `db_freifaecher`-Datenbank
- Datenimport mit `LOAD DATA LOCAL INFILE`
- Redundanzbereinigung und Datenvalidierung
- Abfragen mit `SELECT` und Export mit `SELECT INTO OUTFILE`

**Kurze Zusammenfassung / Kernkonzepte:**

Die Lektion fokussierte auf Datensicherung (Voll-, differentielles, inkrementelles Backup) mit Tools wie `mysqldump` und Mariabackup. Ein logisches Backup der `tourenplaner`-Datenbank wurde erstellt und wiederhergestellt. Die `db_freifaecher`-Datenbank wurde aus Excel in 1NF und 2NF normalisiert (Tabellen: Schüler, Lehrer, Freifächer, Klassen, Anmeldungen), mit `LOAD DATA LOCAL INFILE` befüllt, Redundanzen bereinigt und mit `SELECT ... JOIN ...` validiert. Abfragen (z. B. Teilnehmerzahl, Klassenliste) wurden mit `SELECT INTO OUTFILE` exportiert. 290 Testdatensätze wurden generiert.

**Wichtige Befehle:**

- Backup: `mysqldump -u root -p tourenplaner > C:/BACKUP/tp_dump.sql`
- Restore: `mysql> SOURCE C:/BACKUP/dump.sql`
- Import: `LOAD DATA LOCAL INFILE 'C:/path/file.csv' INTO TABLE ... FIELDS TERMINATED BY ',' LINES TERMINATED BY '\r\n' IGNORE 1 ROWS;`
- Export: `SELECT ... INTO OUTFILE 'C:/M164/outfile.csv' FIELDS TERMINATED BY ',' LINES TERMINATED BY '\r\n';`
- Redundanzprüfung: `SELECT col, COUNT(*) FROM table GROUP BY col HAVING COUNT(*) > 1;`

**Checkpoint-Fragen:**

- Ablauf der Normalisierung?
- Unterschied logisches vs. physisches Backup?
- Restore-Prozess für verschiedene Backup-Typen?
- Schritte zur 3. Normalform?
- Funktion von `SELECT INTO OUTFILE`?

**Auftrag:**

- Datensicherung (50 Min, Team): Logisches Backup mit `mysqldump`, physisches Backup mit Mariabackup.
- Freifächer (4-6 Lektionen, Einzelarbeit): Excel in 1NF/2NF, ERD, DDL-Script, Datenimport, Redundanzbereinigung, Testdaten (290 DS), Abfragen, Export, Backup.
- Ergebnisse und Skripte im Lernportfolio ablegen.

---

## Lektion vom 01.07.2025

**Wichtige Themen:**

- Recap und Q&A zu Tag 7
- Daten normalisiert einbinden (1. und 2. Normalform)
- Erstellung logischer und physischer ER-Diagramme
- Datenimport mit `LOAD DATA LOCAL INFILE`
- Redundanzbereinigung und Datenvalidierung
- Testdatengenerierung (290 Schüler-Datensätze)
- Opendata-Analyse: Steuerdaten Stadt Zürich, Bildungsdaten BFS
- Backup-Erstellung
- Vorbereitung auf LB2

**Kurze Zusammenfassung / Kernkonzepte:**

Die Lektion vertiefte die Normalisierung (1NF, 2NF) mit der `db_freifaecher`-Datenbank. Eine Excel-Tabelle wurde in 1NF überführt, ein logisches ERD (2NF, fünf Tabellen, Kardinalitäten) und ein physisches ERD mit Constraints (`NOT NULL`, `UNIQUE`, Fremdschlüssel) erstellt. Ein DDL-Script wurde via Forward Engineering generiert. Daten wurden mit `LOAD DATA LOCAL INFILE` importiert, Fremdschlüssel überprüft, Redundanzen bereinigt und Daten validiert. 290 Testdatensätze wurden generiert (Excel, Zufallszahlen) und verarbeitet. Abfragen (z. B. Teilnehmerzahl von Inge Sommer, Klassenliste, Freifächer "Chor"/"Elektronik") wurden mit `SELECT INTO OUTFILE` exportiert. Opendata-Quellen (Steuerdaten Stadt Zürich, Bildungsdaten BFS) wurden analysiert, normalisiert, importiert und abgefragt (z. B. `_p25`, `_p50`, `_p75`, Schulbesuchsquote). Ein Backup wurde erstellt.

**Wichtige Befehle/Konzepte:**

- 1NF: Atomare Felder, Redundanz.
- 2NF: Beseitigung von Teilschlüsselabhängigkeiten.
- Logisches ERD: Kardinalitäten (1:1, 1:n, m:n).
- Physisches ERD: `NOT NULL`, `UNIQUE`, Fremdschlüssel.
- `LOAD DATA LOCAL INFILE 'file.csv' INTO TABLE ... FIELDS TERMINATED BY ',' LINES TERMINATED BY '\r\n' IGNORE 1 ROWS;`
- Redundanzprüfung: `SELECT col, COUNT(*) FROM table GROUP BY col HAVING COUNT(*) > 1;`
- Export: `SELECT ... INTO OUTFILE 'file.csv' FIELDS TERMINATED BY ',' LINES TERMINATED BY '\r\n';`
- Backup: `mysqldump -u root -p db_freifaecher > backup.sql`

**Checkpoint-Fragen (Reflexion):**

- Unterschied zwischen 1NF und 2NF?
- Wie definiert man Kardinalitäten?
- Schritte beim Datenimport mit `LOAD DATA LOCAL INFILE`?
- Wie überprüft man Fremdschlüssel-Beziehungen?
- Bedeutung von `_p25`, `_p50`, `_p75`?
- Warum Backup vor LB2?

**Auftrag:**

- Freifächer (3-4 Lektionen, Einzelarbeit): Excel in 1NF/2NF, ERD, DDL-Script, Datenimport, Redundanzbereinigung, Testdaten (290 DS), Abfragen, Export, Backup.
- Opendata (2 Lektionen, Einzelarbeit): Analyse/Normalisierung von Steuerdaten oder Bildungsdaten, ERD, DDL/DML-Skripte, Bulkimport, Abfragen, Backup.
- Ergebnisse und Skripte im Lernportfolio ablegen.

---

## Lektion vom 08.07.2025

**Wichtige Themen:**

- Weiterarbeit an der Praxisarbeit zur Vorbereitung auf LB2
- Repetition der Kernkonzepte (Normalisierung, ERD, Constraints, Datenimport, Abfragen)
- Leistungsbewertung LB2 (40%, 100 Minuten)
- Backup und Dokumentation

**Kurze Zusammenfassung / Kernkonzepte:**

Die abschließende Lektion fokussierte auf die Praxisarbeit und Repetition für die LB2: Normalisierung (1NF bis 3NF), ERDs, Constraints (`NOT NULL`, `UNIQUE`, Fremdschlüssel), Datenimport mit `LOAD DATA LOCAL INFILE`, Redundanzbereinigung und Abfragen. Die Praxisarbeit umfasste die `db_freifaecher`- oder eine Opendata-Datenbank (z. B. Steuerdaten, Bildungsdaten). Die LB2 (40%, 100 Minuten) testete Datenmodellierung, SQL-Skripte und Datenanalyse. Ergebnisse wurden dokumentiert, und ein Backup wurde erstellt.

**Wichtige Befehle/Konzepte:**

- Normalisierung: 1NF, 2NF, 3NF.
- ERD: Logisch (Kardinalitäten), physisch (Constraints).
- Constraints: `NOT NULL`, `UNIQUE`, `FOREIGN KEY ... ON DELETE ...`.
- `LOAD DATA LOCAL INFILE 'file.csv' INTO TABLE ... FIELDS TERMINATED BY ',' LINES TERMINATED BY '\r\n' IGNORE 1 ROWS;`
- Abfragen: `SELECT ... FROM ... JOIN ... WHERE ... GROUP BY ... HAVING ... ORDER BY ...;`
- Export: `SELECT ... INTO OUTFILE 'file.csv' FIELDS TERMINATED BY ',' LINES TERMINATED BY '\r\n';`
- Backup: `mysqldump -u root -p db_name > backup.sql`

**Checkpoint-Fragen (Reflexion):**

- Schritte zur 3NF-Normalisierung?
- Wie stellt man referenzielle Integrität sicher?
- Rolle von `LOAD DATA LOCAL INFILE`?
- Wie validiert man importierte Daten?
- Warum ist Dokumentation wichtig?
- Welche Backup-Methode wurde verwendet?

**Auftrag:**

- Praxisarbeit (Einzelarbeit): Weiterarbeit an `db_freifaecher` oder Opendata-Datenbank, Normalisierung, ERD, DDL/DML-Skripte, Datenimport, Abfragen, Backup.
- LB2 (100 Minuten): Praktische Umsetzung von Datenmodellierung, SQL-Skripten, Datenanalyse.
- Dokumentation: Ergebnisse und Skripte im Lernportfolio ablegen, Backup erstellen.