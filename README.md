# Flutter Feature-First Mason Brick 🧱

Mason brick that scaffolds a **Feature-First / Clean-Light Architecture** for Flutter applications

---

## 🏗️ Architectural Blueprint

The generated folder framework strictly separates your **UI presentation**, **business logic state controllers**, and **network data streams** into independent modular layers:

```text
lib/
│
├── core/                        # Global shared codebase components
│   ├── constants/               # System styling keys, asset maps, asset icon helpers
│   ├── theme/                   # Visual design token structures & variants
│   └── utils/                   # Shared pure utility extensions (e.g., currency formatters)
│
├── data/                        # THE NETWORK & PERSISTENCE LAYER (Firestore)
│   ├── models/                  # Type-safe Dart serialization maps (fromJson / toJson)
│   └── services/                # Pure Firestore stream managers, write transactions & queries
│
├── domain/                      # BUSINESS LOGIC & COMPONENT STATE LAYER
│   ├── ledger_manager/          # Global workspace context controllers
│   └── transaction_feed_manager/# Combined multi-ledger stream distributors
│
└── presentation/                # ISOLATED USER INTERFACE LAYER (Feature-Driven)
    ├── dashboard/               # Metric evaluation grids, pie charts, and balance feeds
    ├── records/                 # Interactive histories, list tiles, and transaction capture forms
    └── settings/                # Management panels for members, workspaces, and categories
```

---

## 🚀 Getting Started

### 📋 Prerequisites
Ensure you have the [Mason CLI](https://brickhub.dev) installed globally on your machine:

```bash
dart pub global activate mason_cli
```

### 📦 Installation & Usage
You can add this brick to your project directly from GitHub and run it to scaffold your architecture instantly. 

Run these commands in the root directory of your Flutter project:

```bash
# 1. Add the brick straight from your GitHub repository URL
mason add flutter-brick --git-url https://github.com

# 2. Run the brick to scaffold the architecture layout inside your lib/ folder
mason make flutter-brick
```
