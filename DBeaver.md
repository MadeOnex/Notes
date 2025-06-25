## Projekt Starten

~ Create
```sql
CREATE DATABASE "name";
```

~ Use
```sql
USE "name";
```

~Delete
```sql
DROP DATABASE IF EXISTS "name";
```

## Befehle

~ Entität erstellen
```sql
CREATE TABLE Tabellenname (
Attributsname1 | Datentyp | Zusätzliche Parameter,
Attributsname2 | Datentyp | Zusätzliche Parameter
);
```

~ Foreign Keys in Entität
```sql
FOREIGN KEY (Attributsname) REFERENCES Referenztabelle (Referenzattribut);
```
~ Foreign key am Ende 
```sql
ALTER TABLE Tabellenname ADD FOREIGN KEY (TabellenAttribut) REFERENCES Referenztabelle (Referenzattribut);
```

~ Attribut Hinzufügen
```sql
ALTER TABLE Tabellenname ADD COLUMN Attriubutsname Datentyp;
```

~Eigenschaften Ändern 
```sql
ALTER TABLE Tabellenname MODFIY COLUMN Attributsname NeuerDatentyp;
```

~ Name Attribut Ändern
```sql
ALTER TABLE Tabellenname CHANGE COLUMN alterAttributname neuerAttributname Datentyp;
```

~ Attribut löschen
```sql
ALTER TABLE Tabellenname DROP COLUMN Attributname;
```

~ Attribut Name Ändern
```sql
ALTER TABLE AlterTabellenname RENAME TO NeuerTabellenname;
```

~ Constraint hinzufügen
```sql
ALTER TABLE Tabellenname ADD CONSTRAINT Constraintname CONSTRAINT (Attributname);
```

~ Beispiele CHECK / UNIQUE
```sql
ALTER TABLE freund ADD CONSTRAINT check_freunschaftslevel CHECK (freunschaftslevel >= 0 AND freunschaftslevel <= 100);

ALTER TABLE kunde ADD CONSTRAINT unique_eMail UNIQUE (eMail);
```
