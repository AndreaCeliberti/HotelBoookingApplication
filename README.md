# HotelBoookingApplication

Applicazione web sviluppata in ASP.NET Core per la gestione di una struttura alberghiera, con funzionalità dedicate a clienti, camere e prenotazioni.

## Descrizione

Il progetto implementa una classica architettura MVC e include una separazione tra controller, modelli, servizi, view model e livello dati.  
L'applicazione gestisce le principali entità di dominio di un sistema di booking alberghiero e comprende anche una parte dedicata all'autenticazione degli utenti.

## Funzionalità principali

- Gestione clienti
- Gestione camere
- Gestione prenotazioni
- Autenticazione e gestione utenti
- Accesso ai dati tramite Entity Framework Core
- Utilizzo di migration per l'evoluzione del database
- Interfaccia server-rendered tramite Razor Views

## Struttura del progetto

- `Controllers/`  
  Contiene i controller principali dell'applicazione:
  - `CameraController`
  - `ClienteController`
  - `HomeController`
  - `IdentityController`
  - `PrenotazioneController`

- `Data/`  
  Contiene il contesto del database:
  - `HotelDbContext`

- `Models/`  
  Contiene le entità di dominio e i modelli applicativi:
  - `ApplicationUser`
  - `Camera`
  - `Cliente`
  - `Prenotazione`

- `Services/`  
  Contiene il livello servizi per la logica applicativa:
  - `CameraService`
  - `ClienteService`
  - `PrenotazioneService`

- `ViewModels/`  
  Contiene i modelli usati per lo scambio dati tra controller e viste

- `Views/`  
  Contiene le viste Razor dell'applicazione

- `Migrations/`  
  Contiene le migration Entity Framework Core per la gestione dello schema del database

## Tecnologie utilizzate

- C#
- ASP.NET Core MVC
- Entity Framework Core
- SQL Server
- Razor Views
- HTML
- CSS
- JavaScript

## Obiettivo del progetto

Questo progetto è stato realizzato per mettere in pratica lo sviluppo di un'applicazione backend strutturata in .NET, con particolare attenzione a:

- modellazione delle entità
- organizzazione del codice in livelli
- gestione del database
- implementazione di operazioni CRUD
- autenticazione utenti
- sviluppo di una web application completa in ambito gestionale

## Avvio del progetto

### Requisiti

- .NET SDK installato
- SQL Server disponibile in locale o configurato tramite connection string
- IDE consigliato: Visual Studio

### Avvio

1. Clonare il repository

git clone https://github.com/AndreaCeliberti/HotelBoookingApplication.git

2. Entrare nella cartella del progetto

cd HotelBoookingApplication

3. Configurare la connection string nel file appsettings.json
4. Applicare le migration al database
dotnet ef database update

5. Avviare l'applicazione
dotnet run
