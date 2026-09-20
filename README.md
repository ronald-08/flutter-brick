# Flutter Brick

A Mason brick for bootstrapping a Flutter application with a feature-oriented
folder structure and clear boundaries between shared code, data access, and UI.

## Generated Structure

Running the brick creates the following layout:

```sh
lib/
├── main.dart                           # Application entry point
├── core/                               # Common shared code 
│   ├── constants/                      
│   ├── models/
│   ├── theme/
│   ├── utils/
│   └── widgets/
├── data/
│   ├── repository/                     # Data (Model)
│   └── service/                        # External services
└── ui/
    ├── feature_1/                      # Some feature of the app
    │   ├── feature_1_view.dart         # UI (View)
    │   └── feature_1_viewmodel.dart    # Logic (View Model)
    └── feature_2/
        ├── feature_2_view.dart
        └── feature_2_viewmodel.dart
```

The `core` directories are intended for code shared across the application.
The `data` directories provide locations for repositories and external-data
services. Each UI feature keeps its view and view model together so features
can grow independently.

## Getting Started

Install the [Mason CLI](https://docs.brickhub.dev/) if it is not already
available:

```bash
dart pub global activate mason_cli
```

From the root of an existing Flutter project, add this brick from GitHub:

```bash
mason add flutter-brick --git-url https://github.com/ronald-08/flutter-brick
```

Generate the scaffold:

```bash
mason make flutter-brick
```

By default, Mason writes the generated files relative to the current project
directory. Run the command from your Flutter project root so the template is
created under `lib/`.


## Reference

- [Flutter Guide to App Architecture](https://docs.flutter.dev/app-architecture/guide)