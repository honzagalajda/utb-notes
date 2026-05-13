## Vytvoření tabulky

```sql
CREATE TABLE users (
  id INT NOT NULL IDENTITY(1,1) UNIQUE,
  firstname VARCHAR(50) NOT NULL,
  lastname VARCHAR(50) NOT NULL,
  email VARCHAR(255) NOT NULL,
  role_id INT NOT NULL,
  PRIMARY KEY (id)
);
```

## Příkaz GO

Označuje konec jedné dávky (batch) příkazů a pošle je serveru k vykonání.

## Auto increment (IDENTITY)

`IDENTITY(seed, increment)` seed = počíteční hodnota; increment = o kolik se má navýšít.

## Cizí klíč / Úprava tabulky

```sql
ALTER TABLE users
ADD CONSTRAINT FK_users_roles
FOREIGN KEY (role_id)
REFERENCES roles (id)
ON UPDATE NO ACTION
ON DELETE NO ACTION;
```

`ADD phone VARCHAR(20) NULL` - přidá sloupec

`ALTER COLUMN email VARCHAR(255) NOT NULL` - změní sloupec

`DROP COLUMN phone` - vymaže sloupec `phone`

`ADD CONSTRAINT FK_<parent>_<child>` přidává novou podmínku do tabulky.

`ON UPDATE NO ACTION` nebude možné změnit `id` v tabulce `roles`, na kterou nějaký `users.role_id` odkazuje.

`ON DELETE NO ACTION` nepůjde smazat řádek `roles`, na který odkazuje nějaký řádek v `users`.

## Plnění hodnot

```sql
INSERT INTO roles (name)
VALUES
('trenér'),
('žák');
```

## Výběr hodnot

`DISTINCT` vypíše pouze unikátní hodnoty a záznamy seřadí abecedně (odstraní redundanci)

`LIKE / NOT LIKE` % (nahrazuje znak nebo kolekci znaků), \_ (nahradí jeden konkrétní znak) \[] (nahradí interval znaků \[a - z]) 

`ORDER BY` seřadí (DESC / ASC)

```sql
-- 1) Všichni žáci (role = 'žák'):
SELECT u.*
FROM users u
JOIN roles r ON u.role_id = r.id
WHERE r.name = 'žák';
```

```sql
-- 5) Počet rezervací v jednotlivých lekcích:
SELECT c.id AS class_id,
       c.name,
       COUNT(r.id) AS reservations_count
FROM classes c
LEFT JOIN reservations r ON c.id = r.class_id
GROUP BY c.id, c.name;
```

```sql
-- 6) Součet všech plateb:
SELECT SUM(amount) AS total_revenue
FROM payments;
```

```sql
-- 7) Počet rezervací na jednoho uživatele:
SELECT u.id,
       u.firstname,
       u.lastname,
       COUNT(r.id) AS reservations_count
FROM users u
LEFT JOIN reservations r ON u.id = r.user_id
GROUP BY u.id, u.firstname, u.lastname;
```

```sql
-- 8) Lekce s datem a časem ve formátu pouze datum (CONVERT):
SELECT id,
       name,
       CONVERT(date, start_time) AS start_date,
       CONVERT(time, start_time) AS start_time_only
FROM classes;
```

```sql
-- 9) E‑maily uživatelů malými písmeny (LOWER):
SELECT id,
       firstname,
       lastname,
       LOWER(email) AS email_lower
FROM users;
```

```sql
-- Časový rozdíl
SELECT id,
       name,
       DATEDIFF(minute, start_time, end_time) AS duration
FROM classes;
```

## Aktualizace tabulky

```sql
UPDATE u
SET u.role_id = r.id
FROM users u
JOIN roles r ON r.name = 'žák'
WHERE u.id = 10;
```

## Mazání z tabulky

```sql
DELETE u
FROM users u
JOIN roles r ON u.role_id = r.id
WHERE r.name = 'žák';
```

## Proměnné

`DECLARE @PredmetID char(5)='testt'

`SET @PredmetID='testt'`

## Pohled

Pohled – VIEW, není nic jiného než SQL dotaz, který je uložený v databázi pod 
konkrétním jménem