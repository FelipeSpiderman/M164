# Datenbank Modul Lernportfolio

Dokumentation des Lernportfolios und der bearbeiteten Themen im Datenbank Modul.

---

## Lektion vom 13.05.2025

**Wichtigste Themen:**

- [Stichpunkt 1 zum Hauptthema]
- [Stichpunkt 2 zum Hauptthema]
- [etc.]

**Kurze Zusammenfassung / Kernkonzepte:**

- [Prägnante Beschreibung der wichtigsten Aktivitäten oder Konzepte, z.B. "Einführung in XY, Fokus auf Z.", "Wichtige Diagrammtypen besprochen.", "Aufgabe X bearbeitet, Anwendung von Y."]
- [Wichtigstes gelerntes Konzept kurz erklärt.]
- [Ggf. Verweis auf Ergebnisse/Skripte, wenn relevant und kurz zu halten.]

---

## Lektion vom 20.05.2025

**Wichtigste Themen:**

- Recap Tag 1 und Lösungen
- Datenmodellierung: Generalisierung / Spezialisierung
- Beziehungsarten: Identifying vs. Non-Identifying Relationships
- Datenbank Management Systeme (DBMS): Merkmale, Vor-/Nachteile, Produkte
- DDL (Data Definition Language): CREATE SCHEMA/DATABASE, CREATE TABLE, DROP TABLE, ALTER TABLE
- Zeichensätze (Character Sets)
- Nutzung von MySQL Workbench (Forward Engineering, Synchronize Model)
- Recherche zu fortgeschrittenen Themen (Partition, Storage Engine, Tablespace)

**Kurze Zusammenfassung / Kernkonzepte:**
Diese Lektion vertiefte die Datenmodellierung mit Generalisierung/Spezialisierung zur Reduzierung von Redundanz ("is_a"-Beziehung). Wir lernten die Unterscheidung zwischen Identifying (Child-PK enthält Parent-FK) und Non-Identifying Relationships (Child-PK ist unabhängig vom Parent-FK) kennen. Ein zentrales Thema war das DBMS, dessen Funktionen (Integrierte Datenhaltung, DQL, DDL, DML, DCL, TCL, Konsistenzkontrolle, Transaktionen etc.), Vor- und Nachteile sowie verschiedene Produkte besprochen wurden. Praktisch wurde mit DDL-Befehlen gearbeitet (`CREATE SCHEMA`, `CREATE TABLE`, `DROP TABLE`, `ALTER TABLE ADD/DROP/CHANGE/MODIFY`) und die Bedeutung von Character Sets (`utf8mb4`) für die Datenkodierung hervorgehoben. Die Nutzung von MySQL Workbench für das automatische Generieren von DDL-Skripten aus Modellen (Forward Engineering) und den Abgleich von Modell und Datenbank (Synchronize Model) wurde eingeführt.

**Wichtige DDL-Befehle:**

- `CREATE SCHEMA db_name;` (oder `DATABASE`)
- `CREATE TABLE table_name (...);`
- `DROP TABLE table_name;`
- `ALTER TABLE table_name ADD column_name datatype;`
- `ALTER TABLE table_name DROP column_name;`
- `ALTER TABLE table_name CHANGE old_col_name new_col_name datatype;`
- `ALTER TABLE table_name MODIFY column_name new_datatype;`

**Checkpoint Fragen (Reflexion):**

- Warum Generalisierung/Spezialisierung?
- Warum Identifying Beziehung? Wie wird sie mit SQL erstellt?
- Welche Befehle gehören zur DDL-Gruppe?

---

## Lektion vom 27.05.2025

**Wichtigste Themen:**

- Vertiefung Datentypen in MariaDB/MySQL
- Komplexere Beziehungsmodelle: Mehrfachbeziehungen, Rekursion (strenge Hierarchie), Einfache Hierarchie (mit Zwischentabelle), Stücklistenproblem
- Repetition und Anwendung von DML-Befehlen (INSERT, UPDATE, DELETE)
- Repetition und Anwendung von DQL-Befehlen (SELECT)
- Erweiterung und Befüllung des "Tourenplaner"-Schemas mit Daten
- Nutzung von MySQL Workbench für Forward Engineering

**Kurze Zusammenfassung / Kernkonzepte:**
Diese Lektion behandelte fortgeschrittene Beziehungstypen in der Datenmodellierung wie Mehrfachbeziehungen, rekursive Beziehungen (Hierarchien) und das Stücklistenproblem, inklusive deren Abbildung im relationalen Modell (teilweise über Zwischentabellen). Wir wiederholten und übten die Kernbefehle der Datenmanipulationssprache (DML: INSERT, UPDATE, DELETE) und der Datenabfragesprache (DQL: SELECT mit WHERE und ORDER BY). Das erweiterte "Tourenplaner"-Schema wurde mit diesen komplexeren Beziehungen ergänzt, mittels Forward Engineering in der Datenbank umgesetzt und anschliessend mit Beispieldaten gefüllt, wobei besonderes Augenmerk auf die hierarchischen Daten gelegt wurde. Die Korrektheit der eingefügten Daten wurde mit SELECT-Abfragen überprüft.

**Wichtige Befehle/Konzepte:**

- Definition und Anwendung verschiedener SQL-Datentypen.
- Modellierung von 1:mc und mc:mc Beziehungen auf Entitäten des gleichen Typs (Rekursion/Hierarchie).
- DML: `INSERT INTO ... VALUES ...;`, `UPDATE ... SET ... WHERE ...;`, `DELETE FROM ... WHERE ...;`.
- DQL: `SELECT ... FROM ... WHERE ... ORDER BY ...;`, Nutzung von JOINs für Abfragen über mehrere Tabellen.
- Forward Engineering in Workbench zum Erstellen der Datenbankstruktur aus dem Modell.

**Checkpoint Fragen (Reflexion):**

- Schwierigkeiten beim Einfügen von Daten mit FK-Constraints?
- Warum NULL in tbl_Hierarchie nicht zulässig?
- Wann Hierarchie-Tabelle statt rekursiver Beziehung nutzen?
- Überprüfung der SQL-Datentypen-Tabelle.

---

## Lektion vom 03.06.2025

**Wichtigste Themen:**

- Datenbankbeziehungen mit Einschränkungen (Constraints)
- Anwendung von Constraints mit Forward Engineering und ALTER TABLE
- Grundlagen der Mengenlehre und deren Bezug zu Datenbanken
- Vertiefung und Anwendung von SELECT JOINs (INNER, LEFT, RIGHT, FULL OUTER)
- Abfragen über mehrere Tabellen

**Kurze Zusammenfassung / Kernkonzepte:**
Die Lektion konzentrierte sich auf die Umsetzung von Datenbankbeziehungen im physischen Modell, insbesondere unter Verwendung von Constraints wie `NOT NULL` und `UNIQUE` für Fremdschlüssel, um die referentielle Integrität sicherzustellen. Wir untersuchten, wie Workbench diese Einschränkungen beim Forward Engineering generiert und lernten, wie man sie manuell mit `ALTER TABLE ADD CONSTRAINT FOREIGN KEY` hinzufügt. Die Verbindung zwischen Mengenlehre (Schnittmenge, Vereinigungsmenge etc.) und SQL JOIN-Operationen wurde hergestellt, um das Verständnis von Datenabfragen über mehrere Tabellen (`INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN`) zu vertiefen und praktisch anzuwenden. Umfangreiche Übungen zur Datenabfrage mit JOINs, einschliesslich komplexerer Szenarien über mehrere Tabellen, standen im Fokus.

**Wichtige Befehle/Konzepte:**

- Konzept der Referential Integrity (referentielle Integrität).
- Implementierung von Constraints (NN, UQ, FOREIGN KEY) im physischen Modell.
- Syntax für `ALTER TABLE ADD CONSTRAINT FOREIGN KEY (...) REFERENCES ... (...);`
- Grundlegende Mengenlehre-Operationen (∩, ∪, \) und ihre Entsprechungen in SQL JOINs.
- Unterschiedliche JOIN-Typen: `INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN`.
- Konzept des Kartesischen Produkts.
- Anwendung von `GROUP BY` und `GROUP_CONCAT` für komplexere Abfragen.

**Checkpoint Fragen (Reflexion):**

- Definition und Beispiel für referentielle Integrität.
- Welche Constraints kann eine Beziehung haben?
- Unterschied zwischen LEFT JOIN und RIGHT JOIN.
- Umsetzung von 1:1 und c:m Beziehungen.
- Nachteil der Definition von Beziehungen nur über PK/FK ohne Constraints.
- Folgen eines ungültigen FS-Eintrags mit/ohne Constraint.

---

## Lektion vom 10.06.2025

**Wichtigste Themen:**

- Datenlöschung und Datenintegrität in professionellen Datenbanken
- Fremdschlüssel-Regeln (`ON DELETE`)
- SELECT mit ALIAS
- Aggregatsfunktionen (`COUNT`, `SUM`, `AVG`, `MIN`, `MAX`)
- GROUP BY
- HAVING Condition
- Reihenfolge der SELECT-Klauseln

**Kurze Zusammenfassung / Kernkonzepte:**
Diese Lektion behandelte, warum in professionellen Datenbanken Daten selten physisch gelöscht werden, um Datenintegrität und Nachvollziehbarkeit zu gewährleisten. Wir lernten, wie Fremdschlüssel-Constraints das Löschverhalten (`ON DELETE` mit `NO ACTION`/`RESTRICT`, `CASCADE`, `SET NULL`) beeinflussen und wie man diese in Workbench oder via `ALTER TABLE` konfiguriert. Ein Hauptfokus lag auf fortgeschrittenen SELECT-Operationen: Nutzung von ALIAS für Spalten/Tabellen, Anwendung von Aggregatsfunktionen zur Datenzusammenfassung, Gruppierung von Ergebnissen mit GROUP BY und Filtern gruppierter Ergebnisse mit HAVING. Die korrekte Reihenfolge der SELECT-Klauseln (MERKSATZ: Sag Fritz...) wurde hervorgehoben.

**Wichtige Befehle/Konzepte:**

- Datenintegrität (Genauigkeit, Konsistenz, Vollständigkeit).
- `ON DELETE` Optionen (`NO ACTION`, `RESTRICT`, `CASCADE`, `SET NULL`).
- `SELECT column AS alias`, `SELECT * FROM table AS alias JOIN ...`.
- Aggregatsfunktionen: `COUNT()`, `SUM()`, `AVG()`, `MIN()`, `MAX()`.
- `GROUP BY column1, column2, ...`
- `HAVING condition` (Filter auf aggregierte Ergebnisse).
- Reihenfolge der SELECT-Klauseln: `SELECT ... FROM ... JOIN ... WHERE ... GROUP BY ... HAVING ... ORDER BY ... LIMIT ...`.

**Checkpoint Fragen (Reflexion):**

- Nennen Sie die fünf Aspekte der Datenintegrität.
- Unterschied zwischen Datenintegrität und Datenkonsistenz.
- Gefahr bei `ON DELETE CASCADE`.
- Unterschied zwischen `COUNT(*)` und `COUNT(attr)`.
- SELECT mit `WHERE BETWEEN`.
- Wichtiges bei der HAVING Klausel.

---

## Lektion vom 17.06.2025

**Wichtige Themen:**

- Subqueries (skalare/nicht-skalare Unterabfragen)
- Bulkimport mit `LOAD DATA INFILE` (Server/Client)
- CSV-Datenanpassung (Datumsformate, Spaltenreihenfolge, überspringen/hinzufügen von Attributen)
- Normalisierung in 3. Normalform (3NF) mit SQL
- Redundanzprüfung und -bereinigung
- Datenübertragung mit `INSERT INTO ... SELECT ...`
- Arbeiten mit `db_adressen`

**Zusammenfassung:**

Diese Lektion behandelt Subqueries zur dynamischen Datenfilterung (skalare: ein Wert, nicht-skalare: Listen mit `IN`). `LOAD DATA INFILE` wurde für effizienten CSV-Import (Server/Client) geübt, inklusive Anpassungen wie `STR_TO_DATE` für Datumsformate, Spaltenüberspringen und Wertezuweisung via `CASE`. Die Datenbank `db_adressen` wurde in 3NF normalisiert (`tbl_Person`, `tbl_Str`, `tbl_Ort`) mit SQL-Befehlen. Redundanzen wurden mit `GROUP BY`/`HAVING` geprüft und bereinigt. Daten wurden mit `INSERT INTO ... SELECT ...` übertragen und mit `SELECT ... JOIN ...` validiert.

**Wichtige Befehle:**

- Skalare Subquery: `SELECT ... WHERE col < (SELECT MIN(col) FROM ...);`
- Nicht-skalare Subquery: `SELECT ... WHERE col IN (SELECT col FROM ...);`
- `LOAD DATA [LOCAL] INFILE 'path/file.csv' INTO TABLE ... FIELDS TERMINATED BY ',' LINES TERMINATED BY '\r\n' IGNORE 1 ROWS;`
- Datumsanpassung: `SET col = STR_TO_DATE(@var, '%d.%m.%Y');`
- Attribut hinzufügen: `SET col = value;`
- Werte ändern: `SET col = CASE WHEN @var = 'val' THEN x ELSE y END;`
- Redundanzprüfung: `SELECT col, COUNT(*) FROM table GROUP BY col HAVING COUNT(*) > 1;`

**Checkpoint-Fragen:**

- Zweck von Subqueries und warum in Klammern?
- Unterschied skalare vs. nicht-skalare Subqueries?
- Gefahren bei Subqueries (z. B. falsche Datensätze)?
- Bedeutung von `IGNORE 1 ROWS` in `LOAD DATA INFILE`?
- Folgen falscher `LINES TERMINATED BY`-Einstellung?
- Einstellungen für `LOAD DATA LOCAL INFILE` (`local_infile`, `secure_file_priv`)?
- Anpassung der Spaltenreihenfolge beim Import?

**Auftrag:**

- Subselect-Aufgabe umsetzen (35 Min, Einzelarbeit).
- CSV-Import mit `LOAD DATA LOCAL INFILE` (30 Min, Partnerarbeit): `db_adressen` erstellen, Daten in `tbl_Adr` importieren, in 3NF normalisieren (`tbl_Person`, `tbl_Str`, `tbl_Ort`), Daten übertragen, Redundanzen bereinigen, Ergebnisse mit `SELECT ... JOIN ...` prüfen.
- Ergebnisse und Skripte im Lernportfolio ablegen.

---

## Lektion vom 24.06.2025

**Wichtige Themen:**

- Datenbanksicherung: Konzepte und Methoden
- Backup-Typen: Voll-, differentielles, inkrementelles Backup
- Backup-Tools: `mysqldump`, phpMyAdmin, Mariabackup, Workbench, Docker
- Normalisierung der `db_freifaecher`-Datenbank
- Datenimport mit `LOAD DATA LOCAL INFILE`
- Redundanzbereinigung und Datenvalidierung
- Abfragen mit `SELECT` und Export mit `SELECT INTO OUTFILE`

**Zusammenfassung:**

Die Lektion fokussierte auf Datensicherungskonzepte (Online-/Offline-Backups, Voll-/differentielles/inkrementelles Backup) und deren Umsetzung mit Tools wie `mysqldump`, phpMyAdmin, Mariabackup und Workbench. Praktisch wurde ein logisches Backup der `tourenplaner`-Datenbank erstellt, analysiert und wiederhergestellt. Die `db_freifaecher`-Datenbank wurde aus einer Excel-Tabelle in die 1. Normalform (1NF) überführt, in die 2. Normalform (2NF) normalisiert (Tabellen: Schüler, Lehrer, Freifächer, Klassen, Anmeldungen) und mit `LOAD DATA LOCAL INFILE` befüllt. Redundanzen wurden bereinigt, Daten mit `SELECT ... JOIN ...` validiert und spezifische Abfragen (z. B. Teilnehmerzahl, Klassenliste) durchgeführt. Ergebnisse wurden mit `SELECT INTO OUTFILE` exportiert. Zusätzlich wurden 290 Testdatensätze generiert und verarbeitet.

**Wichtige Befehle:**

- Backup: `mysqldump -u root -p tourenplaner > C:/BACKUP/tp_dump.sql`
- Restore: `mysql> SOURCE C:/BACKUP/dump.sql`
- Import: `LOAD DATA LOCAL INFILE 'C:/path/file.csv' INTO TABLE ... FIELDS TERMINATED BY ',' LINES TERMINATED BY '\r\n' IGNORE 1 ROWS;`
- Export: `SELECT ... INTO OUTFILE 'C:/M164/outfile.csv' FIELDS TERMINATED BY ',' LINES TERMINATED BY '\r\n';`
- Redundanzprüfung: `SELECT col, COUNT(*) FROM table GROUP BY col HAVING COUNT(*) > 1;`
- Normalisierung: `INSERT INTO table1 (col1, col2) SELECT col1, col2 FROM table2;`

**Checkpoint-Fragen:**

- Ablauf der Normalisierung in eine DB?
- Unterschied logisches vs. physisches Backup?
- Restore-Prozess für Voll-, inkrementelles, differentielles Backup?
- Drei Backup-Methoden und deren Befehle/Vorgehen?
- Fünf Schritte zur 3. Normalform?
- Funktion von `SELECT INTO OUTFILE`?

**Auftrag:**

- Datensicherung (50 Min, Team): Logisches Backup mit `mysqldump`, Analyse, Restore, physisches Backup mit Mariabackup.
- Freifächer (4-6 Lektionen, Einzelarbeit): Excel in 1NF, log./phys. ERD (2NF), DDL-Script, Datenimport, Redundanzbereinigung, Validierung, Testdaten (290 DS), Abfragen, Export mit `SELECT INTO OUTFILE`, Backup der DB.
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
- Opendata-Analyse: Steuerdaten Stadt Zürich und Bildungsdaten BFS
- Backup-Erstellung
- Vorbereitung auf LB2

**Kurze Zusammenfassung / Kernkonzepte:**

Die Lektion begann mit einem Recap und Q&A zu Tag 7, gefolgt von der Vertiefung der Normalisierung am Beispiel der `db_freifaecher`-Datenbank. Eine Excel-Tabelle wurde in die 1. Normalform (1NF) überführt (atomare Felder, bewusste Redundanz), und ein logisches ERD mit mindestens fünf Tabellen in der 2. Normalform (2NF) inklusive Kardinalitäten wurde erstellt. Das physische ERD wurde mit Constraints (`NOT NULL`, `UNIQUE`, Fremdschlüssel) umgesetzt, und ein DDL-Script wurde via Forward Engineering generiert. Daten wurden aus CSV-Dateien mittels `LOAD DATA LOCAL INFILE` importiert, Fremdschlüssel-Beziehungen überprüft, Redundanzen bereinigt und Daten mit SELECT-Abfragen validiert. 290 Testdatensätze für Schüler wurden mit einem Testdatengenerator (Excel, Zufallszahlen durch vertikale Verschiebung) erstellt, importiert und validiert. Spezifische Abfragen (z. B. Teilnehmerzahl von Inge Sommer, Klassenliste, Freifächer "Chor" oder "Elektronik") wurden durchgeführt und mit `SELECT INTO OUTFILE` exportiert. Opendata-Quellen (Steuerdaten Stadt Zürich, Bildungsdaten BFS) wurden analysiert, normalisiert, importiert und abgefragt (z. B. Median-Einkommen, Schulbesuchsquote). Abschließend wurde ein Backup erstellt.

**Wichtige Befehle/Konzepte:**

- 1. Normalform: Atomare Felder, Redundanz erzeugt.
- 2. Normalform: Teilschlüsselabhängigkeiten beseitigt.
- Logisches ERD: Kardinalitäten (1:1, 1:n, m:n).
- Physisches ERD: `NOT NULL`, `UNIQUE`, Fremdschlüssel-Constraints.
- `LOAD DATA LOCAL INFILE 'file.csv' INTO TABLE ... FIELDS TERMINATED BY ',' LINES TERMINATED BY '\r\n' IGNORE 1 ROWS;`
- Redundanzprüfung: `SELECT col, COUNT(*) FROM table GROUP BY col HAVING COUNT(*) > 1;`
- Export: `SELECT ... INTO OUTFILE 'file.csv' FIELDS TERMINATED BY ',' LINES TERMINATED BY '\r\n';`
- Testdatengenerierung: Zufallsdaten in Excel (z. B. vertikale Verschiebung, Suchen-Ersetzen).
- Opendata: Normalisierung, Bulkimport, DML-Skripte, Abfragen (z. B. `_p25`, `_p50`, `_p75` für Steuerdaten).
- Backup: `mysqldump -u root -p db_freifaecher > backup.sql`

**Checkpoint-Fragen (Reflexion):**

- Was ist der Unterschied zwischen 1NF und 2NF?
- Wie definiert man Kardinalitäten im logischen ERD?
- Welche Schritte sind beim Datenimport mit `LOAD DATA LOCAL INFILE` zu beachten?
- Wie überprüft man die Korrektheit von Fremdschlüssel-Beziehungen?
- Was bedeuten `_p25`, `_p50`, `_p75` in den Steuerdaten?
- Warum ist ein Backup vor LB2 wichtig?

**Auftrag:**

- Freifächer (3-4 Lektionen, Einzelarbeit): Excel in 1NF, log./phys. ERD (2NF), DDL-Script, Datenimport, Redundanzbereinigung, 290 Testdatensätze, SELECT-Abfragen, Export mit `SELECT INTO OUTFILE`, Backup.
- Opendata (2 Lektionen, Einzelarbeit): Analyse und Normalisierung von Steuerdaten oder Bildungsdaten, phys. ERD, DDL- und DML-Skripte, Bulkimport, Abfragen (z. B. maximales/niedrigstes Steuereinkommen, Schulbesuchsquote), Backup.
- Ergebnisse und Skripte im Lernportfolio ablegen.

---

## Lektion vom 08.07.2025

**Wichtige Themen:**

- Weiterarbeit an der Praxisarbeit zur Vorbereitung auf LB2
- Repetition der Kernkonzepte (Normalisierung, ERD, Constraints, Datenimport, Abfragen)
- Durchführung der Leistungsbewertung LB2 (40%, 100 Minuten)
- Backup und Dokumentation

**Kurze Zusammenfassung / Kernkonzepte:**

Die Lektion war der abschließende Tag vor der LB2 und konzentrierte sich auf die Praxisarbeit sowie die Repetition der Kernkonzepte: Normalisierung (1NF bis 3NF), Erstellung von logischen und physischen ERDs, Implementierung von Constraints (`NOT NULL`, `UNIQUE`, Fremdschlüssel), Datenimport mit `LOAD DATA LOCAL INFILE`, Redundanzbereinigung, Datenvalidierung und komplexe SELECT-Abfragen. Die Praxisarbeit umfasste die Weiterarbeit an der `db_freifaecher`-Datenbank oder einer Opendata-Datenbank (z. B. Steuerdaten, Bildungsdaten), inklusive Normalisierung, Import, Abfragen und Backup. Die LB2 (40%, ca. 100 Minuten) testete diese Konzepte praktisch, mit Fokus auf Datenmodellierung, SQL-Skripte und Datenanalyse. Ergebnisse und Skripte wurden dokumentiert, und ein abschließendes Backup der Datenbank wurde erstellt.

**Wichtige Befehle/Konzepte:**

- Normalisierung: 1NF (atomare Felder), 2NF (Teilschlüsselabhängigkeiten), 3NF (transitive Abhängigkeiten).
- ERD: Logisches (Kardinalitäten) und physisches (Constraints) Model.
- Constraints: `NOT NULL`, `UNIQUE`, `FOREIGN KEY ... ON DELETE ...`.
- `LOAD DATA LOCAL INFILE 'file.csv' INTO TABLE ... FIELDS TERMINATED BY ',' LINES TERMINATED BY '\r\n' IGNORE 1 ROWS;`
- Abfragen: `SELECT ... FROM ... JOIN ... WHERE ... GROUP BY ... HAVING ... ORDER BY ...;`
- Export: `SELECT ... INTO OUTFILE 'file.csv' FIELDS TERMINATED BY ',' LINES TERMINATED BY '\r\n';`
- Backup: `mysqldump -u root -p db_name > backup.sql`

**Checkpoint-Fragen (Reflexion):**

- Welche Schritte umfasst die Normalisierung bis 3NF?
- Wie stellt man referenzielle Integrität mit Fremdschlüsseln sicher?
- Welche Rolle spielt `LOAD DATA LOCAL INFILE` bei der Datenmigration?
- Wie validiert man importierte Daten mit SELECT-Abfragen?
- Warum ist die Dokumentation von Skripten im Lernportfolio wichtig?
- Welche Backup-Methode wurde für die Praxisarbeit verwendet?

**Referenzen:**

- Subquery Manual
- Subquery Beispiele
- LOAD DATA INFILE
- [MySQL Dump](https://linuxize.com/post/how-to-back-up-and-restore-mysql-databases-with-mysqldump/)
- [MariaDB Backup Tool](https://mariadb.com/docs/server/server-usage/backup-and-restore/mariadb-backup)
- [Opendata Stadt Zürich](https://data.stadt-zuerich.ch/)
- [Bildungsdaten BFS](https://data.bfs.admin.ch/)

**Auftrag:**

- Praxisarbeit (Einzelarbeit): Weiterarbeit an `db_freifaecher` oder Opendata-Datenbank, Normalisierung, ERD, DDL/DML-Skripte, Datenimport, Abfragen, Backup.
- LB2 (100 Minuten): Praktische Umsetzung von Datenmodellierung, SQL-Skripten und Datenanalyse.
- Dokumentation: Ergebnisse und Skripte im Lernportfolio ablegen, Backup der Datenbank erstellen.
