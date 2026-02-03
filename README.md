# Kotlin Multiplatform Skills

Claude Code plugin providing stack-specific skills and agents for Kotlin Multiplatform (KMP) development.

## Installation

### Add the Marketplace

```bash
/plugin marketplace add pddhkt/kotlin-kmp-skills
```

### Install the Plugin

```bash
# Project scope (recommended)
/plugin install kotlin-kmp@kotlin-kmp-skills --scope project

# User scope
/plugin install kotlin-kmp@kotlin-kmp-skills
```

## Available Skills

| Skill | Usage | Description |
|-------|-------|-------------|
| kmp | `/kotlin-kmp:kmp` | KMP project structure, expect/actual, Gradle |
| sqldelight | `/kotlin-kmp:sqldelight` | SQLDelight schema and migrations |
| ktor | `/kotlin-kmp:ktor` | Ktor networking patterns |
| koin | `/kotlin-kmp:koin` | Koin dependency injection |
| android | `/kotlin-kmp:android` | Android-specific implementation |
| ios | `/kotlin-kmp:ios` | iOS-specific implementation |
| reflect | `/kotlin-kmp:reflect` | Push skill improvements back to source repo |

## Included Agents

| Agent | Description |
|-------|-------------|
| shared-impl | Shared/common code implementation specialist |
| android-impl | Android platform implementation specialist |
| ios-impl | iOS platform implementation specialist |
| database-impl | SQLDelight database specialist |
| network-impl | Ktor networking specialist |

## Stack Detection

This stack is auto-detected when a project contains:
- `shared/` directory
- `composeApp/` directory
- `iosApp/` directory

## Updating

```bash
/plugin marketplace update kotlin-kmp-skills
```

## Repository Structure

```
kotlin-kmp-skills/
├── .claude-plugin/
│   └── marketplace.json
├── stack.json
│
└── plugins/
    └── kotlin-kmp/
        ├── .claude-plugin/
        │   └── plugin.json
        ├── agents/
        │   ├── shared-impl.md
        │   ├── android-impl.md
        │   ├── ios-impl.md
        │   ├── database-impl.md
        │   └── network-impl.md
        └── skills/
            ├── kmp/
            ├── sqldelight/
            ├── ktor/
            ├── koin/
            ├── android/
            ├── ios/
            └── reflect/
```

## License

MIT
