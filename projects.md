## 🚀 My team- and pet-projects

### Corporate Q&A Platform "Muza" 🏢

[Team](https://github.com/Team5-Muza) project: Commercial project, full-stack enterprise solution, ready to production (as MVP)

- **My Role:** Sole Backend Developer (in team of 6 specialists) 👨‍💻
- **Tech Stack:**
  - **Backend Stack:** Java, Spring Boot 3, Maven, PostgreSQL, Apache Kafka, Docker, GitLab CI/CD, Swagger/OpenAPI
  - **Frontend Stack:** React + TypeScript, Redux Toolkit, Ant Design, Responsive Design
  - **DevOps & Infrastructure:** Docker Swarm, Traefik, GitLab CI/CD, Portainer, Grafana, Prometheus, Mail Service
- **Key Achievements:**
  - **Production-ready REST API** with complete Swagger documentation
  - **Asynchronous notification system** via Apache Kafka with email service
  - **Full-text search** across questions and answers
  - **Python script for data migration** - imported Stack Overflow dump
  - **Pagination and performance optimization**
  - **100% release readiness** - all critical bugs resolved
- **Project Scale:** 🚀 Developed end-to-end in just 1 month by 6-person team
- **Quality Assurance:** 180+ test cases, 💯 100% functional coverage, enterprise-grade testing

### [Digital Factory Backend](https://gitlab.deevlab.space/digital-factory/backend) 🏭

Team project: Commercial project, microservice backend ecosystem for 3D printing calculation service (MVP ready)

- **My Role:** Lead Backend Developer (in team of 3 backend specialists + algorithmic engineer) 👨‍💻
- **Tech Stack:**
  - **Core Stack:** Kotlin, Spring Boot 4 Spring Cloud Gateway (WebFlux), PostgreSQL, Liquibase, Gradle (Kotlin DSL)
  - **Async Processing:** PostgreSQL-based task queue (SKIP LOCKED), Heartbeat mechanism, batch processing
  - **File Storage:** AWS S3 SDK, MinIO, presigned URLs (direct upload for ≤5MB, multipart for >5MB)
  - **Resilience:** Resilience4j (Circuit Breaker, Retry with exponential backoff), AOP aspects
  - **Python Worker:** Python 3.13, NumPy, Numba (JIT), psycopg2, requests
  - **Testing:** Python, pytest, Pydantic (auto-generated from OpenAPI), parallel execution
  - **DevOps:** Docker, Docker Compose, GitLab CI/CD, Actuator metrics
- **Project Scale:** 🚀 4 microservices, 2 PostgreSQL instances, full async pipeline
- **Key Achievements:**
  - **Full microservice architecture** - API Gateway (Spring Cloud Gateway), Root Backend (main API), Slicer API (task orchestrator), Slicer Worker (Python computation)
  - **Implicit authentication** - anonymous users created automatically, `user_id` stored in HttpOnly cookie, no login required
  - **Async STL processing** - files are sliced asynchronously (volume, filament length, print time, cost), user doesn't wait
  - **PostgreSQL as message queue** - atomic task acquisition with `FOR UPDATE SKIP LOCKED`, heartbeat mechanism prevents stuck workers
  - **Resilience patterns** - Circuit Breaker for external API failures, Retry with exponential backoff, graceful shutdown
  - **OpenAPI filtering** - Gateway hides internal `user_id` parameter from public documentation
  - **Batch processing schedulers** - status updates and result processing with configurable batch sizes
  - **Python worker with JIT** - NumPy + Numba for fast geometry calculations, ~60% faster than pure Python
  - **120+ integration tests** - Python + pytest with auto-generated models from OpenAPI, parallel execution
- **Quality Assurance:** Full async pipeline testing (PENDING → PROCESSING → COMPLETED), Gateway proxy tests, automatic resource cleanup

### [Locus No Pilotus: Trajectory Calculator](https://github.com/BPLA-Team/locus_no_pilotus) 📐

[Team](https://github.com/BPLA-Team) project: Project of four first-year MIPT AES DAFE students to create a mathematical trajectory calculator for delivery drones in Qt C++

- **Tech Stack:**
  - **Core Stack:** C++17, Qt Framework (5/6, Widgets, Core), CMake 3.20+, Ninja, MSYS2/MinGW-w64
  - **Visualization:** QCustomPlot (git submodule), custom `PlotItemArc` renderer for circular arcs
  - **Math Engine:** Self-implemented computational geometry - common tangent enumeration, visibility graphs, Dijkstra's algorithm; Little's branch-and-bound TSP solver with matrix reduction and zero-power heuristics; multi-agent support via depot-cloning
  - **Persistence:** JSON via Qt JSON API; four-section format with ID-range validation and bidirectional change detection
  - **Testing:** Boost.Test, 100+ test cases, property-based randomized testing (1000 iterations)
  - **DevOps:** GitHub Actions CI/CD for Doxygen docs auto-deploy to GitHub Pages
- **Project Scale:** 🚀 ~60 source files across 4 layered namespaces (`lib/`, `math/`, `gui/`, `data_tools/`), 3 git submodules
- **Key Achievements:**
  - **Clean four-layer architecture** - domain model → computational geometry + TSP → drawable Qt wrappers → MVC glue (DataManager + PlotArea + TablesConnection)
  - **Multi-agent trajectory planning** - computes optimal paths for 1–9 drones visiting all control points while avoiding polygonal hills, circular no-fly zones, and forbidden flight corridors
  - **Little's Algorithm from scratch** - branch-and-bound with matrix reduction, zero-power branching, priority-stack frontier; handles random, symmetric, and obstacle-laden matrices up to 10×10
  - **Obstacle-aware pairwise pathfinding** - visibility graph over common tangents between obstacles; Dijkstra finds shortest collision-free path; arcs along obstacle perimeters when hugging circles
  - **Triple input mode** - modeless dialogs, interactive plot-based creation (click-drag-preview), and bidirectional table editing synchronized with live plot
  - **Pre-calculation validation pipeline** - circle-circle intersection, target-inside-obstacle, hill convexity, max 30 targets, TrappyLine combinatorial constraints
  - **Animated trajectory playback** - flying robot traverses computed path with configurable speed and smooth line/arc interpolation
  - **JSON persistence with change detection** - auto-prompts on unsaved changes; ID-range enforcement per object type (10000–19999 for Targets, etc.)
- **Quality Assurance:** 100+ Boost.Test cases - Point arithmetic, Segment construction, intersection detection (all 3 result types), distance functions, Dijkstra (6 graphs), Little's TSP (single & multi-salesman, 2×2 to 10×10), optimal way end-to-end (12 scenarios), tangent geometry (all obstacle pairings + edge cases)

### [Graphic Calculator: FIDocalcus](https://github.com/BPLA-Team/graphic_calculator) 🧮

[Team](https://github.com/BPLA-Team) project: Project of three first-year MIPT AES DAFE students to create a graphic calculator in FLTK C++

- **Tech Stack:** C++, FLTK, CMake, OpenGL, Git, Doxygen
- **Key Features:** Advanced expression parser with reverse Polish notation, real-time graphing with domain segmentation, numerical analysis (roots, extremes, derivatives), function intersection detection, cross-platform GUI, clean frontend-backend architecture, automatic discontinuity handling, interactive function management

### [DrugDesign Data Analysis](https://github.com/UmbrellaLeaf5/DrugDesign_data_analysis) 🧪

Pet-project: Module of the DrugDesign project responsible for loading and pre-processing data from ChEMBL and PubChem, necessary for further modeling and analysis in drug development

- **Tech Stack:** Python, ChEMBL WebResource Client, PubChemPy, Requests, Pandas, NumPy, Loguru, JSON configuration, Google Drive API, Doxygen
- **Key Features:** Automated data pipeline from chemical databases, compound and activity downloading from ChEMBL, toxicity data extraction from PubChem, configurable filtering system, SDF file handling, retry mechanisms with exponential backoff, comprehensive logging, data validation and cleaning, batch processing with pagination

### [File Spec Contractor](https://github.com/UmbrellaLeaf5/file_spec_contractor) 📋

Pet-project: CLI tool for generating compact `.fsc.md` file specifications via LLM API - saves tokens when AI agents work with codebases

- **Tech Stack:** Python 3.12+, Typer, Rich, httpx, Pydantic v2, charset-normalizer, pytest, uv
- **Key Features:**
  - **Three generation modes** - per-file sequential, per-file parallel (ThreadPoolExecutor with configurable concurrency), and bulk (all files in a single LLM call with regex-based response parsing and automatic fallback to per-file on parse failure)
  - **Smart caching with freshness tracking** - skips files when spec.mtime >= source.mtime; auto-migrates cached specs when output mode changes to avoid unnecessary API calls; `--force` to regenerate everything
  - **Pluggable LLM providers** - OpenRouter (OpenAI-compatible, free tier) and DeepSeek via abstract registry; 3-tier API key resolution (CLI flag → env var → `.env` file via python-dotenv)
  - **Three-tier configuration** - CLI arguments → `.fsc/config.toml` → `~/.config/fsc/config.toml` with deep-merge of sections; Pydantic v2 validation with helpful error messages
  - **Three output layouts** - mirror (preserves directory structure), adjacent (spec next to source file), batch (numbered folders of N files each)
  - **Versioned prompt system** - 8+ built-in prompt versions (en/ru), auto-selects latest for configured language, custom `.fsc/PROMPT.md` override with language mismatch detection
  - **Strict specification format** - 6-section structure (Purpose, Dependencies, Public API, Implementation Notes, Handle with Care, Code Style); inherited methods grouped by source, private/protected excluded, re-export modules annotated separately
  - **Resilience and graceful degradation** - Ctrl+C preserves already-completed specs; individual file errors don't block remaining files; bulk mode falls back to per-file on parse failure with missed-file retry; atomic writes via temp-file + `os.replace()`
  - **Rich terminal experience** - colored output, per-file progress bars, API spinner; `--no-progress` for CI/scripts; full lifecycle commands (init, generate, clean, deinit, reinit) all with `--dry-run`, `--force`, `--yes` flags

### [Notes Maker](https://github.com/UmbrellaLeaf5/notes_maker) 📝

Pet-project: Simple realization of a working notes (.txt files) maker and editor in PyQt6

- **Tech Stack:** Python, PyQt6, file I/O operations, virtual environments (uv/venv)
- **Key Features:** Dark theme GUI, complete CRUD operations for text files, automatic encoding detection (UTF-8/CP1251), smart file naming system, real-time auto-saving, dual-window interface (main window + note editor), hover effects and interactive UI elements, folder-based note organization

### [Notes organizer](https://github.com/UmbrellaLeaf5/notes_organizer) 📱

Pet-project: Simple application for easy notes organization on Flutter (Dart)

- **Tech Stack:** Dart, Flutter, Material Design 3, Cross-platform development
- **Key Features:** Cross-platform compatibility (Web/Desktop), Material Design 3 with dark theme, complete CRUD operations for notes, smart file import system (.txt files), gesture support (long press, right-click), keyboard shortcuts (Ctrl/Cmd+Enter), contextual menus, custom icons and Comfortaa font, responsive widget-based architecture

### [CMake Evaluation Calculator](https://github.com/UmbrellaLeaf5/cmake_eval_calculator) ⚡

Pet-project: _!UNFINISHED!_ Evaluation calculator with grammar using (idea from Bjarne Stroustrup: "Programming. Principles and Practice Using C++") fully in CMake

- **Tech Stack:** CMake, Turing-complete build system, grammar-based parsing
- **Key Features:** Expression evaluation entirely in CMake, grammar implementation from Stroustrup's book, Turing-complete build system utilization, mathematical expression parsing without traditional programming languages, educational exploration of CMake's computational capabilities

### [Simple Calculator](https://github.com/UmbrellaLeaf5/simple_calculator) 🧮

Pet-project: Simple realization of a working calculator (similar to the Windows version) in PyQt6

- **Tech Stack:** Python, PyQt6, virtual environments (uv/venv)
- **Key Features:** Windows-style dark theme interface, basic arithmetic operations (+, -, \*, /), advanced math functions (square root, power, reciprocal, modulo), dual-display system (expression + result), decimal number support, button hover animations, clear/clear-entry functionality, sign change operation, professional UI with color-coded buttons

### [Cesar Len Key](https://github.com/UmbrellaLeaf5/cesar_len_key) 🔐

Pet-project: Modification of the Caesar cipher, created by me at school and rewritten in my first year at MIPT

- **Tech Stack:** Python, math library, modular arithmetic, trigonometric functions
- **Key Features:** Enhanced Caesar cipher with dynamic key-based shifts, piecewise alphabet shuffling algorithm, trigonometric functions for non-linear transformations, support for 172 characters (Latin, Cyrillic, special symbols), symmetric block encryption, mathematical optimization using divisors and modular arithmetic

### [CesarLen PassVault](https://github.com/UmbrellaLeaf5/cesar_len_pass_vault) 🔐

Pet-project: Kivy-based GUI password vault with dual encryption and Yandex.Disk cloud sync - no local files, everything lives as encrypted blobs in the cloud

- **Tech Stack:** Python 3.12, Kivy 2.3, Yandex.Disk REST API, python-dotenv, Cesar Len Key cipher, PyInstaller (Windows .exe), Buildozer (Android .apk), pytest, GitHub Actions CI/CD
- **Key Features:**
  - **Dual encryption** - two independent ciphers (primary: `CryptedLines`, backup: multi‑round Caesar with SHA‑256 key stretching, HMAC subkeys, integer‑only shifts)
  - **Split editor** - view and compare primary/backup vaults side‑by‑side, sync‑on‑upload popup
  - **Pre‑start setup screen** - prompts for Yandex.Disk token and remote path on first launch, saves to `.env`
  - **Android support** - settings stored as `settings.json` in `user_data_dir` (no `.env` files on mobile)
  - **Cross‑platform** - Windows `.exe` via PyInstaller (ANGLE backend) and Android `.apk` via Buildozer, both built in GitHub Actions on tag push
  - **46 unit tests** - covering both ciphers, models, storage, and sync

### [State Machine Executor](https://github.com/UmbrellaLeaf5/state_machines_executor) 🤖

Pet-project: _!UNFINISHED!_ Creating an executor to simplify the creation of Moore and Mealy finite state machines that receive a binary number as input

- **Tech Stack:** Python, DearPyGui, IceCream, Pytest, Finite State Machine theory
- **Key Features:** Visual FSM editor with DearPyGui GUI, support for both Moore and Mealy machines, binary number input processing, automated state transition execution, debugging with IceCream, comprehensive testing with Pytest, educational tool for automata theory

### [Tasks Organizer](https://github.com/UmbrellaLeaf5/tasks_organizer) ✅

Pet-project: Simple realization of (todo) tasks organizer and editor in Kotlin Spring Boot (with PostgreSQL)

- **Tech Stack:** Kotlin, Spring Boot 3.5.6, Spring Data JPA, PostgreSQL, Docker, Docker Compose, Maven, REST API
- **Key Features:** Full CRUD operations for users and notes, basic search functionality (in titles/content), user authentication and authorization, containerized database deployment, RESTful API with proper HTTP methods, relational database design with foreign keys and cascading operations, comprehensive error handling and validation

(with [database in docker-compose](https://github.com/UmbrellaLeaf5/tasks_organizer_postgresql_docker_compose))
