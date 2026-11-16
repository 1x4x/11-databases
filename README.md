# Övning 2 – Databas med studenter

## Beskrivning
I denna övning skapar vi en databas med en tabell som heter `student`. Tabellen innehåller information om studenter, såsom ID, förnamn, efternamn och kommentarer.

## 1. Skapa databasen

```sql
CREATE DATABASE studenter;
USE studenter;
```

## 2. Skapa tabellen student

```sql
CREATE TABLE student (
    sid INT NOT NULL PRIMARY KEY,
    fname VARCHAR(20) NOT NULL,
    lname VARCHAR(20) NOT NULL,
    comment TEXT NULL
);
```

### Tabellstruktur

| Kolumn | Datatyp | NULL | Nyckel |
|--------|---------|------|--------|
| sid | INT | Nej | PRIMARY KEY |
| fname | VARCHAR(20) | Nej | Nej |
| lname | VARCHAR(20) | Nej | Nej |
| comment | TEXT | Ja | Nej |

## 3. Lägg till minst 3 studenter

```sql
INSERT INTO student (sid, fname, lname, comment)
VALUES
(1, 'Ali', 'Ahmed', 'Bra student'),
(2, 'Sara', 'Karlsson', 'Gillar programmering'),
(3, 'Erik', 'Svensson', NULL);
```

## 4. Visa alla studenter

```sql
SELECT * FROM student;
```

## 5. Förväntat resultat

| sid | fname | lname | comment |
|-----|-------|-------|---------|
| 1 | Ali | Ahmed | Bra student |
| 2 | Sara | Karlsson | Gillar programmering |
| 3 | Erik | Svensson | NULL |

## 6. Förklaring

- **sid:** Studentens unika ID och tabellens primärnyckel.
- **fname:** Studentens förnamn, max 20 tecken.
- **lname:** Studentens efternamn, max 20 tecken.
- **comment:** En valfri kommentar om studenten.
- **PRIMARY KEY:** Säkerställer att varje student har ett unikt ID.
- **NOT NULL:** Betyder att kolumnen måste innehålla ett värde.
- **NULL:** Betyder att ett värde kan saknas.

## Slutsats

I denna övning har vi:
- Skapat en databas som heter `studenter`.
- Skapat en tabell som heter `student`.
- Definierat en primärnyckel och obligatoriska fält.
- Lagt till tre studenter.
- Hämtat alla studenter med `SELECT`.
