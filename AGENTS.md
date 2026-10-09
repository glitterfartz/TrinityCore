# Repository Guidelines

## Project Structure & Module Organization

TrinityCore is a C++ MMORPG server built with CMake. Shared utilities live in `src/common`; server gameplay, database access, and executables live in `src/server`. Zone, encounter, and spell scripts belong in `src/server/scripts/<module>`. Client-data extraction tools live in `src/tools`.

Use `tests/common` and `tests/game` for automated tests, `sql/base` and `sql/updates` for database definitions and migrations, and `doc` for documentation. Zone guides belong in `doc/zones`; database references belong in `doc/world-database`. Vendored dependencies are in `dep`; avoid unrelated vendor changes. Extracted client assets are configured through `DataDir`, not committed as source.

## Build, Test, and Development Commands

Install the branch-compatible compiler, MySQL, Boost, and OpenSSL dependencies before configuring. Use an out-of-source build:

```powershell
cmake -S . -B build -DBUILD_TESTING=ON -DSCRIPTS=static
cmake --build build --config RelWithDebInfo --parallel
ctest --test-dir build -C RelWithDebInfo --output-on-failure
```

These commands configure scripts and tests, compile, and run discovered tests. Preserve existing build-cache dependency settings. Launch the built `bnetserver` and `worldserver` executables with their configured `.conf` files, databases, and matching extracted client data. Use Debug builds when investigating crashes.

## Coding Style & Naming Conventions

Follow `.editorconfig`: four spaces, no tabs, final newlines, trimmed trailing whitespace, and a 160-character line limit. C/C++ files specify Latin-1; other files default to UTF-8. Match nearby brace layout and naming. Preserve exact script registration names and database `ScriptName`/`StringId` bindings. Keep changes focused; editor configuration is the checked-in formatting baseline.

## Testing Guidelines

Tests use Catch2 and CTest discovery. Follow existing descriptive test cases and filenames such as `tests/common/EventMap.cpp`. Add regression coverage for changed behavior; no numeric coverage threshold is specified. For gameplay changes, report in-game reproduction and verification alongside automated results. Documentation changes should check links and distinguish inspected implementation from untested runtime behavior.

## Commit & Pull Request Guidelines

Use the history's subsystem prefix: `Core/Players: ...`, `Scripts/Spells: ...`, or `DB/Quest: ...`. Keep each fix on a focused branch. Follow `pull_request_template.md`: describe changes, link issues, list build/gameplay tests, and disclose known issues. Use pending SQL names such as `9999_99_99_99_world.sql`; update base schemas for auth/characters changes. Upstream SQL-only contributions follow the issue workflow in `CONTRIBUTING.md`.

## Configuration & Database Safety

Keep credentials and local configuration out of commits. Prefer read-only database inspection during research. Record core revision, database version, and client build when diagnosing content compatibility.
