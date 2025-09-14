
---

## Prerequisites

- Java 17+ installed
- Gradle 8.x installed (or use the Gradle wrapper `gradlew`)
- MySQL database (optional, if using JPA)

---

## Modules

| Module  | Description |
|---------|------------|
| `Web`   | Main Spring Boot module. Produces **runnable fat jar**. Depends on all other modules. |
| `service` | Library module containing business logic. Can produce its own jar. |
| `data`    | Library module containing repositories and entities. Can produce its own jar. |
| `util`    | Library module containing utilities and helpers. Can produce its own jar. |

---

## Gradle Tasks

### 1. Build a module independently

```bash
# Build Web module (fat jar)
./gradlew :Web:bootJar

# Build Service module jar
./gradlew :service:bootJar

# Build Data module jar
./gradlew :data:bootJar
