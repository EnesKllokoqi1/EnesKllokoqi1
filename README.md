<div align="center">

# Enes Kllokoqi

### Backend Developer · C# · ASP.NET Core · Prishtina, Kosovo 🇽🇰

*First-year Computer and Software Engineering student with 2+ years of self-directed C# development, including a 3-month C# internship at Star Labs. I build clean, tested, production-minded APIs.*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Enes_Kllokoqi-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/enes-kllokoqi-461bb5451/)
[![GitHub](https://img.shields.io/badge/GitHub-EnesKllokoqi1-181717?logo=github)](https://github.com/EnesKllokoqi1)
![C#](https://img.shields.io/badge/C%23-512BD4?logo=csharp&logoColor=white)
![.NET](https://img.shields.io/badge/.NET_9-512BD4?logo=dotnet&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?logo=jsonwebtokens&logoColor=white)

</div>

---

## 👋 About me

I'm Enes, a **backend developer from Prishtina** with **over two years of experience** in **C# and .NET**. I've completed a **3-month internship at Star Labs**, and I'm currently a **first-year student at the Faculty of Electrical and Computer Engineering (FIEK), University of Prishtina, majoring in Computer and Software Engineering**.

I build REST APIs end to end: designing the data model, securing it with **JWT and refresh tokens stored in HttpOnly cookies to protect against XSS token theft**, adding role-based permissions, structuring the code in clean layers, and making it testable. Right now I'm **working on ShopSphere while studying full-time**. ShopSphere is an e-commerce backend where I'm adding the things that make an API production-ready: **caching, testing, rate limiting and custom exception handling**.

**What I care about**

- Readable code first, clever code second
- Clear separation between controllers, business logic and data access
- Secure authentication: tokens kept out of reach of client-side JavaScript, and least-privilege roles
- APIs that fail gracefully, with consistent and meaningful errors
- Performance basics like caching, and protection like rate limiting
- Tests that let me refactor without fear
- Optimization

---

## ⏱️ Right now

- 🛠️ Building **ShopSphere**, my main backend project
- 🎓 Studying **Computer and Software Engineering** (year 1) at **FIEK, University of Prishtina**
- 🎯 Balancing both deliberately: university builds the fundamentals and discipline; ShopSphere is where I put them into practice.

---

## 🎓 Education

**University of Prishtina, Faculty of Electrical and Computer Engineering (FIEK)**
B.Sc. in **Computer and Software Engineering**, first year (in progress)


---

## 💼 Experience

### C# Intern, Star Labs
*September 2025 – November 2025*

- Worked on a collaborative full-stack healthcare application (**SmartMedicationHealthApp**) built by our team
- The team implemented robust C# RESTful APIs and a microservices architecture, alongside efficient database management and Clean Code architecture. I also contributed to several core REST APIs while actively preparing for college
- [Project repo →](https://github.com/EnesKllokoqi1/sl-team-5)
### Independent projects, 2+ years
Hands-on general and backend development in C# through personal projects, including **ShopSphere** and **WebAuthAPI**, covering authentication, authorization, data modeling, layered architecture and API design.

---

## 🧰 Tech stack

| Area | Technologies |
| --- | --- |
| **Language** | C# |
| **Framework** | .NET 9, ASP.NET Core Web API, xUnit.net |
| **ORM and data** | Entity Framework Core (migrations, seeding, indexing) |
| **Database** | PostgreSQL, SQLite|
| **Authentication** | JWT access tokens and refresh tokens stored in HttpOnly cookies (protection against XSS token theft), role-based authorization |
| **API documentation** | Scalar (interactive API reference) |
| **Architecture** | Clean Architecture, Dependency Injection, Service–Interface pattern, Repository pattern, DTOs, Separation of Concerns |
| **Tooling** | Git, GitHub, Visual Studio, Jira |
| **Config** | `.env` files and `appsettings.json` |
| **Others** | Web Caching, Rate Limiting, Secure Authentication, Unit Testing|

**Currently adding:** caching · automated testing · rate limiting · custom exceptions


---

## 📌 Featured projects

## 🛒 ShopSphere: E-commerce Backend
[Project repo →](https://github.com/EnesKllokoqi1/ShopSphere) (not yet finished)
  
**My main project, under active development (30+ commits)**

A Clean Architecture ASP.NET Core backend for an online shop. I'm building it alongside my first year of university, and I'm using it to practice the engineering that separates a working API from a *production-ready* one.


**Project structure**


```text
ShopSphere.API/
├── src/ShopService/
│   ├── ShopService.API/            # controllers, middleware, DI wiring
│   ├── ShopService.Application/    # use cases,  DTOs, service interfaces
│   ├── ShopService.Domain/         # entities, value objects, domain interfaces (no dependencies)
│   └── ShopService.Infrastructure/ # EF Core, external services, repository implementations
├── tests/ShopService.Tests/        # dedicated test project
├── .env.example                    # configuration template (no secrets committed)
└── ShopSphere.sln
```

**Production-readiness roadmap**

| Feature | Goal | Status |
| --- | --- | --- |
| 🧱 **Clean Architecture** | Controller → Service → Repository with DI | ✅ In place |
| 🗄️ **Caching** | Cut database load on frequently read data | 🚧 In progress |
| 🧪 **Testing** | Unit tests for services, integration tests for endpoints | 🚧 In progress |
| 🚦 **Rate limiting** | Protect the API from abuse and traffic spikes | 🚧 In progress |
| ⚠️ **Custom exceptions** | Domain-specific errors with consistent API responses | 🚧 In progress |

**Why these four?**

- **Caching** reduces repeated database reads, such as product listings and catalog data, and makes responses faster.
- **Testing** lets me refactor safely, because services depend on interfaces and are easy to mock.
- **Rate limiting** keeps a single client from overwhelming the API and protects sensitive endpoints.
- **Custom exceptions** replace generic errors with meaningful ones (not found, validation failed, conflict) and map them to the right HTTP status codes in one central place.

---

## 🏗️ WebAuthAPI: Construction & Assignment Management

[Project repo →](https://github.com/EnesKllokoqi1/WebAuthAPI)

A detailed ASP.NET Core Web API that models how a construction business works: acquiring properties, managing a workforce, and tracking work through a central assignment system.

**The idea:** three entities (users, buildings and workers) are connected through one **Assignment Engine**.

| Entity | Role |
| --- | --- |
| **Users** | Acquire buildings and initiate assignments |
| **Buildings** | The properties where work happens |
| **Workers** | Staff created and managed by an admin, who perform the tasks |

**How assignments work**

An assignment starts out unlinked. After creation, the API links it to a user, a building and a worker through authenticated endpoints. Only then can it move through its lifecycle (start, complete, confirm, reject, cancel). The result is a clear audit trail of who is working where, which property is being serviced, and who is responsible.

**Highlights**

- ✅ **36 functional endpoints**
- ✅ **JWT authentication with refresh tokens stored in HttpOnly cookies**, keeping tokens out of reach of client-side JavaScript for secure long-term sessions
- ✅ **Role-based permissions:** admins manage the workforce, users manage properties and assignments
- ✅ **15+ specialized DTOs** so entities are never exposed directly
- ✅ **Service–Interface pattern** and **dependency injection** for decoupled, testable logic
- ✅ **EF Core** with automated migrations, database seeding and an index on emails
- ✅ **Flexible enums:** endpoints accept strings or integers (`"High"` = `3`)
- ✅ **Interactive docs** with Scalar


**Project structure**

```text
WebAuthAPI/
└── src/ConstructionWebAPI/
    ├── Controllers/   # the 36 endpoints and routes
    ├── Services/      # business logic: buildings, workers, assignments, auth
    ├── DTOs/          # Assignment, Building, User and Worker models
    └── Enums/         # Status, Priority, Role, Gender
```

**Run it locally**

```bash
git clone https://github.com/EnesKllokoqi1/WebAuthAPI.git
cd WebAuthAPI

# point appsettings.json (or a .env file) at your PostgreSQL instance
dotnet ef database update
dotnet run
# then open https://localhost:{PORT}/scalar
```

---

## 🧱 How I structure my APIs

1. **Controllers** handle only HTTP: routing, status codes, input validation.
2. **Services** hold the business rules and depend on interfaces, not implementations.
3. **Repositories** talk to the database through EF Core.
4. **DTOs** define exactly what goes in and out of the API, so entities are never exposed.
5. **Dependency Injection** wires it together, so every layer can be tested in isolation.
6. **Central error handling** (in progress) turns custom exceptions into consistent responses.

---

## 🎯 What I'm looking for

- A **junior backend developer role or internship** Preferably in C# / .NET (ASP.NET Core Web API)
- A team that values testing, clean architecture and code review
- Real production systems where I can learn how things scale and fail

---

## 🌱 Roadmap

- [x] C# and ASP.NET Core Web API
- [x] Entity Framework Core and PostgreSQL
- [x] JWT authentication, refresh tokens in cookies, and role-based authorization
- [x] Clean Architecture with DI, repositories and DTOs
- [x] Real-world team experience (Star Labs internship)
- [ ] Caching in ShopSphere
- [ ] Automated testing in ShopSphere
- [ ] Rate limiting in ShopSphere
- [ ] Custom exceptions and global error handling in ShopSphere
- [ ] Logging and observability
- [ ] Docker and CI/CD with GitHub Actions
- [ ] Data structures and algorithms (alongside my degree)
- [ ] Stripe payment integration

---

## 🏆 GitHub achievements

- 🦈 **Pull Shark** (x2)
- 🔫 **Quickdraw**

---

## 💬 Quick Q&A

**Why backend?**
I like building the part nobody sees but everything depends on: data, rules and security.

**How do you handle authentication?**
JWT access tokens and refresh tokens, stored in HttpOnly cookies instead of being exposed to client-side JavaScript, so an XSS attack can't simply read them.

**What are you working on right now?**
ShopSphere, taking it from "it works" to "it's production-ready" with caching, tests, rate limiting and proper error handling, while completing my first year at FIEK.

**What are you studying?**
Computer and Software Engineering at the Faculty of Electrical and Computer Engineering, University of Prishtina.

**What did you take from your internship?**
I learned how a production app is built from scratch — from architecture and code review to shipping incrementally.

---

## 📫 Let's connect

- ✉️ Email: [eneskllokoqi@gmail.com](mailto:eneskllokoqi@gmail.com)
- 💼 LinkedIn: [Enes Kllokoqi](https://www.linkedin.com/in/enes-kllokoqi-461bb5451/)

<div align="center">

*Thanks for stopping by. Feel free to open an issue or a PR on any of my repos.* ⭐

</div>
