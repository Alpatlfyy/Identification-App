# Application structure

Feature-specific code lives under `features/`. Shared application foundations
live under `app/`, `core/`, and `shared/`.

```text
lib/
├── app/                         # App bootstrap and global composition
├── core/
│   ├── constants/               # Application-wide constants
│   ├── routing/                 # Route names and navigation setup
│   ├── theme/                   # Global theme and design tokens
│   └── widgets/                 # Core widgets used across features
├── features/
│   ├── gate/                    # Kiosk home screen and gate status
│   ├── identification/          # Who: face, badge, QR, NIP, fingerprint
│   ├── attribute_check/         # What: PPE and cleanroom checks
│   ├── guest/                   # Guest registration and invitations
│   ├── exit/                    # Exit flow and visit completion
│   ├── supervisor/              # Protected supervisor operations
│   └── error_handling/          # Recovery and user-facing error states
└── shared/                      # Reusable widgets, models, services
```

As each feature grows, use this internal structure:

```text
feature_name/
├── data/                        # API, device, and repository implementations
├── domain/                      # Entities and use cases
└── presentation/
    ├── screens/                 # Full-page flows
    ├── widgets/                 # Feature-specific UI
    └── controllers/             # State and flow coordination
```
