Here's your complete PayCore project zip. Here's what's inside:
Backend (Java / Spring Boot)

PayCoreApplication.java — main entry point
Employee.java + Payroll.java — Hibernate @Entity models
EmployeeRepository.java + PayrollRepository.java — Spring Data JPA repositories with custom @Query methods
DeductionEngine.java — core tax engine with progressive slab calculation (New Regime FY 2025-26), PF, ESI, and Professional Tax
EmployeeService.java + PayrollService.java — full business logic with @Transactional
EmployeeController.java + PayrollController.java — REST API endpoints with @CrossOrigin
application.properties — MySQL + Hibernate + Swagger config
pom.xml — Spring Boot 3.2, Hibernate 6, JWT, Swagger, Lombok, MySQL

DevOps

.github/workflows/ci-cd.yml — 4-stage GitHub Actions pipeline: test → build → docker push → Netlify deploy
Dockerfile — multi-stage (Maven builder + JRE alpine runtime, non-root user)
netlify.toml — SPA routing, API proxy, security headers

Tests

DeductionEngineTest.java — JUnit 5 tests covering all deduction rules

Docs

