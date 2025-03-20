# Gaming Library

## Opdrachten

### Opdracht 1 - Database ontwerp

- Maak op basis van onderstaande userstories en het SQL-bestand een database ontwerp. 

### Opdracht 2 - Repository

- Maak gebruik van de repository: https://github.com/NOVA-college-Haarlem/gaming-project-blok-3
- Fork de repository
- Clone de repository

### Opdracht 3 - Website

- Maak een website voor een gaming library.

### Opdracht 4 - Controleren

- Controleer je website door gebruik te maken van de rubric.

## User Stories Gaming Library

### Overzichtspagina

**Als een** bezoeker  
**Wil ik** een overzicht zien van alle beschikbare games  
**Zodat ik** snel kan bladeren door verschillende games

**Als een** bezoeker  
**Wil ik** basisinformatie zien van elke game (titel, uitgever, releasedate, thumbnail afbeelding)  
**Zodat ik** een eerste indruk krijg zonder naar de detailpagina te hoeven gaan

**Als een** bezoeker  
**Wil ik** op een game kunnen klikken  
**Zodat ik** naar de detailpagina kan gaan voor meer informatie

### Filtering

**Als een** bezoeker  
**Wil ik** kunnen filteren op platform (PC, PlayStation, Xbox, Nintendo, etc.)  
**Zodat ik** alleen games zie voor platforms die ik bezit

**Als een** bezoeker  
**Wil ik** kunnen filteren op genre (Action, RPG, Adventure, etc.)  
**Zodat ik** games vind die passen bij mijn voorkeur

### Overige Functionaliteiten

**Als een** bezoeker  
**Wil ik** kunnen sorteren op prijs (van laag naar hoog of hoog naar laag)  
**Zodat ik** games kan vinden binnen mijn budget

**Als een** bezoeker  
**Wil ik** zien hoeveel resultaten er beschikbaar zijn binnen mijn gekozen filters  
**Zodat ik** weet hoeveel opties ik heb

**Als een** bezoeker  
**Wil ik** de tekstgrootte van de website kunnen aanpassen (klein, normaal, groot)  
**Zodat ik** de tekst leesbaar hou

## SQL-bestand

```sql
- Database schema voor Gaming Library met één tabel

-- Games tabel
CREATE TABLE games (
    id INT PRIMARY KEY AUTO_INCREMENT,
    titel VARCHAR(100) NOT NULL,
    uitgever VARCHAR(100) NOT NULL,
    platform VARCHAR(50) NOT NULL,
    genre VARCHAR(50) NOT NULL,
    beschrijving TEXT,
    releasedate DATE,
    prijs DECIMAL(10, 2),
    thumbnail_url VARCHAR(255)
);

-- Voorbeelddata invoegen
INSERT INTO games (titel, uitgever, platform, genre, beschrijving, releasedate, prijs, thumbnail_url) VALUES 
('The Legend of Zelda: Breath of the Wild', 'Nintendo', 'Nintendo Switch', 'Adventure', 'Een episch avontuur in een open wereld met Link.', '2017-03-03', 59.99, 'zelda.jpg'),
('God of War Ragnarök', 'Sony', 'PlayStation 5', 'Action', 'Kratos en Atreus gaan op reis door de negen rijken om Ragnarök te voorkomen.', '2022-11-09', 69.99, 'gow.jpg'),
('Halo Infinite', 'Microsoft', 'Xbox Series X', 'FPS', 'Master Chief keert terug in een nieuw avontuur tegen de Banished.', '2021-12-08', 59.99, 'halo.jpg'),
('Elden Ring', 'FromSoftware', 'PC', 'RPG', 'Een episch fantasy-actie RPG in een wereld gecreëerd door Hidetaka Miyazaki en George R.R. Martin.', '2022-02-25', 59.99, 'eldenring.jpg'),
('FIFA 23', 'EA Sports', 'PlayStation 5', 'Sports', 'De nieuwste editie van de populaire voetbalsimulatie.', '2022-09-30', 69.99, 'fifa23.jpg'),
('Minecraft', 'Mojang', 'PC', 'Sandbox', 'Een spel over het plaatsen van blokken en avonturen beleven.', '2011-11-18', 29.99, 'minecraft.jpg'),
('Fortnite', 'Epic Games', 'Xbox Series X', 'Battle Royale', 'Een gratis te spelen Battle Royale-game waarbij 100 spelers tegen elkaar strijden.', '2017-07-25', 0.00, 'fortnite.jpg'),
('Red Dead Redemption 2', 'Rockstar Games', 'PlayStation 4', 'Action Adventure', 'Een episch verhaal over het leven in het genadeloze hart van Amerika in 1899.', '2018-10-26', 39.99, 'rdr2.jpg'),
('Animal Crossing: New Horizons', 'Nintendo', 'Nintendo Switch', 'Simulation', 'Ontsnap naar een verlaten eiland en creëer je eigen paradijs.', '2020-03-20', 49.99, 'animalcrossing.jpg'),
('Cyberpunk 2077', 'CD Projekt Red', 'PC', 'RPG', 'Een open-wereld actie-avontuur in de donkere toekomst van Night City.', '2020-12-10', 49.99, 'cyberpunk.jpg'),
('Call of Duty: Modern Warfare II', 'Activision', 'Xbox Series X', 'FPS', 'De terugkeer van Task Force 141 in een wereldwijde strijd.', '2022-10-28', 69.99, 'codmw2.jpg'),
('Assassins Creed Valhalla', 'Ubisoft', 'PlayStation 5', 'Action RPG', 'Word een Vikingkrijger en leid je clan van de barre kusten van Noorwegen naar een nieuw thuis.', '2020-11-10', 59.99, 'acvalhalla.jpg'),
('Super Mario Odyssey', 'Nintendo', 'Nintendo Switch', 'Platformer', 'Ga op avontuur met Mario in vreemde en nieuwe koninkrijken.', '2017-10-27', 49.99, 'marioodyssey.jpg'),
('The Witcher 3: Wild Hunt', 'CD Projekt Red', 'PC', 'RPG', 'Jaag als monster-jager Geralt van Rivia terwijl hij zoekt naar zijn adoptiefdochter.', '2015-05-19', 39.99, 'witcher3.jpg'),
('Overwatch 2', 'Blizzard', 'PlayStation 5', 'FPS', 'Een team-gebaseerde actieshooter met diverse helden.', '2022-10-04', 0.00, 'overwatch2.jpg');
```

## Rubric

# Beoordelingsrubric Gaming Library Project

## Overzichtspagina

| Criterium                         | Onvoldoende                                 | Voldoende                                       | Goed                                                                     |
| --------------------------------- | ------------------------------------------- | ----------------------------------------------- | ------------------------------------------------------------------------ |
| **Basisweergave van games**       | Games worden niet of nauwelijks getoond     | Games worden correct weergegeven                | Games worden aantrekkelijk weergegeven met duidelijke visuele hiërarchie |
| **Filter op platform**            | Filter werkt niet of met ernstige fouten    | Filter werkt, maar heeft kleine gebreken        | Filter werkt perfect en is gebruiksvriendelijk                           |
| **Filter op genre**               | Filter werkt niet of met ernstige fouten    | Filter werkt, maar heeft kleine gebreken        | Filter werkt perfect en is gebruiksvriendelijk                           |
| **Sortering op prijs**            | Sortering werkt niet of met ernstige fouten | Sortering werkt, maar heeft kleine gebreken     | Sortering werkt perfect en is gebruiksvriendelijk                        |
| **Doorklikken naar detailpagina** | Links werken niet of met ernstige fouten    | Links werken, maar zijn niet optimaal geplaatst | Links werken perfect en zijn intuïtief                                   |

## Detailpagina

| Criterium                           | Onvoldoende                               | Voldoende                          | Goed                                                   |
| ----------------------------------- | ----------------------------------------- | ---------------------------------- | ------------------------------------------------------ |
| **Weergave van game details**       | Details worden niet of nauwelijks getoond | Details worden correct weergegeven | Details worden uitgebreid en aantrekkelijk weergegeven |
| **Teruglink naar overzichtspagina** | Link werkt niet of is niet aanwezig       | Link is aanwezig en werkt          | Link is duidelijk zichtbaar en gebruiksvriendelijk     |

## Algemene aspecten

| Criterium              | Onvoldoende                                        | Voldoende                                                                  | Goed                                                                      |
| ---------------------- | -------------------------------------------------- | -------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| **Database connectie** | Query's werken niet of met ernstige fouten         | Query's werken, maar zijn niet geoptimaliseerd                             | Query's werken goed en zijn geoptimaliseerd                               
| **Code kwaliteit**     | Rommelige code met veel fouten                     | Redelijk nette code met enkele fouten                                      | Nette, goed gestructureerde code zonder fouten                            |
