# ERP-System – Technisches Gesamtkonzept

Umfassende Beschreibung einer modularen, skalierbaren ERP-Plattform auf Basis moderner .NET-Technologien.

---

## 1. Systemarchitektur

### 1.1 Technologie-Stack

**Frontend**
- ASP.NET Core 10 Razor Pages  
- Bootstrap 5 / Tailwind CSS  
- JavaScript / TypeScript  

**Backend**
- C# .NET 10  
- Clean Architecture  

**Weitere Komponenten**
- Datenbank: Microsoft SQL Server (Entity Framework Core)  
- Authentifizierung: ASP.NET Core Identity  
- API: RESTful APIs  
- Caching: Redis / Memory Cache  
- Message Queue: RabbitMQ / Azure Service Bus  
- Reporting: Crystal Reports / DevExpress / SSRS  
- Dokumente: Azure Blob Storage oder lokales Dateisystem  

---

### 1.2 Architektur-Muster (Clean Architecture)

┌─────────────────────────────────────────┐
│ Presentation Layer │
│ (Razor Pages, Controllers, APIs) │
└─────────────────────────────────────────┘
↓
┌─────────────────────────────────────────┐
│ Application Layer │
│ (Services, DTOs, Validators, Mapper) │
└─────────────────────────────────────────┘
↓
┌─────────────────────────────────────────┐
│ Domain Layer │
│ (Entities, Aggregates, Events) │
└─────────────────────────────────────────┘
↓
┌─────────────────────────────────────────┐
│ Infrastructure Layer │
│ (EF Core, Repositories, External APIs) │
└─────────────────────────────────────────┘
