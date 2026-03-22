# Android MVVM Clean Architecture

![Android](https://img.shields.io/badge/Android-3DDC84?style=flat&logo=android&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat&logo=kotlin&logoColor=white)
![MVVM](https://img.shields.io/badge/Architecture-MVVM-blue)
![Clean Architecture](https://img.shields.io/badge/Clean-Architecture-orange)
![Min SDK](https://img.shields.io/badge/minSdk-24-green)

A production-ready Android sample application demonstrating **MVVM + Clean Architecture** principles using modern Android development tools and best practices.

---

## Architecture Overview

This project follows **Clean Architecture** with three distinct layers:

```
app/
├── data/                    # Data Layer
│   ├── local/               # Room Database (DAOs, Entities)
│   ├── remote/              # Retrofit API (Services, DTOs)
│   ├── repository/          # Repository Implementations
│   └── mapper/              # Data <-> Domain mappers
│
├── domain/                  # Domain Layer (pure Kotlin, no Android deps)
│   ├── model/               # Domain Models
│   ├── repository/          # Repository Interfaces
│   └── usecase/             # Business Logic Use Cases
│
├── presentation/            # Presentation Layer
│   ├── ui/                  # Activities, Fragments
│   ├── viewmodel/           # ViewModels (StateFlow/LiveData)
│   └── adapter/             # RecyclerView Adapters
│
└── di/                      # Dependency Injection (Hilt Modules)
```

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Language | Kotlin |
| Architecture | MVVM + Clean Architecture |
| DI | Hilt |
| Async | Coroutines + Flow |
| Networking | Retrofit + OkHttp |
| Local DB | Room |
| Image Loading | Coil |
| Navigation | Jetpack Navigation Component |
| Testing | JUnit4, MockK, Turbine |
| CI | GitHub Actions |
| Code Quality | SonarQube, Detekt |

---

## Key Features

- Unidirectional Data Flow (UDF) with StateFlow
- Offline-first strategy using Room + Remote data sync
- Dependency injection with Hilt across all layers
- Error handling with sealed Result/UiState classes
- 80%+ unit test coverage across domain and presentation layers
- GitHub Actions CI pipeline with automated tests and lint checks

---

## Testing Strategy

```
test/
├── domain/usecase/          # Use case unit tests (MockK)
├── data/repository/         # Repository unit tests
├── presentation/viewmodel/  # ViewModel tests with Turbine (Flow testing)
└── utils/                   # Test utilities and fakes
```

Run tests:
```bash
./gradlew test                  # Unit tests
./gradlew connectedAndroidTest  # Instrumented tests
./gradlew jacocoTestReport      # Coverage report
```

---

## CI/CD Pipeline

```yaml
# .github/workflows/android-ci.yml
- Lint check (ktlint + detekt)
- Unit tests
- Code coverage (JaCoCo)
- SonarQube analysis
- Build APK/AAB
```

---

## Getting Started

1. Clone the repository
```bash
git clone https://github.com/radha-panda/android-mvvm-clean-architecture.git
```

2. Open in Android Studio (Hedgehog or later)
3. Sync Gradle
4. Run on emulator or physical device (API 24+)

---

## Author

**Radha Rani Panda** — Mobile Team Lead | 8+ Years Android/iOS/Flutter  
[LinkedIn](https://www.linkedin.com/in/radha-rani-panda-6754a2124/) · [GitHub](https://github.com/radha-panda)
