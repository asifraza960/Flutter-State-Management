# ⚡ Flutter State Management Masterclass (BLoC & Riverpod)

[![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev/)
[![BLoC](https://img.shields.io/badge/BLoC-42A5F5?style=for-the-badge&logo=flutter&logoColor=white)](https://bloclibrary.dev/)
[![Riverpod](https://img.shields.io/badge/Riverpod-000000?style=for-the-badge&logo=flutter&logoColor=white)](https://riverpod.dev/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

A production-ready reference repository demonstrating practical, clean, and scalable **State Management Solutions** in Flutter—focusing on **BLoC / Cubit** and **Riverpod (2.0+)**.

This project provides real-world comparative implementations of enterprise architectural patterns, reactive streams, state immutability, dependency injection, and UI decoupling.

---

## 🛠️ State Management Comparison

| Feature / Criteria | BLoC / Cubit 🧱 | Riverpod 🌊 |
| :--- | :--- | :--- |
| **Core Concept** | Event-Driven / Stream-based architecture | Compile-safe, reactive Provider network |
| **Boilerplate Level** | Moderate to High (Events, States, Handlers) | Low (Simplified syntax with Codegen/Notifiers) |
| **Context Dependency** | Requires `BuildContext` to read states | Completely independent of `BuildContext` |
| **Best Used For** | Enterprise apps, strict Event-State audit trails | Large scalable apps, reactive caching, asynchronous flows |
| **Testing** | Highly testable via `bloc_test` | Highly testable with global override support |

---

## 🚀 Key Features Covered

* 🧱 **BLoC & Cubit Solutions:**
  * Strict Event-to-State transformations.
  * Stream-based state emissions using `flutter_bloc`.
  * State immutability powered by `freezed` and `equatable`.
  * Optimizing UI rebuilds using `BlocBuilder`, `BlocListener`, and `BlocSelector`.

* 🌊 **Riverpod 2.0+ Architecture:**
  * Compile-time safe dependencies without `BuildContext`.
  * Auto-disposing states, family modifiers, and async caching.
  * State handling using `Notifier` and `AsyncNotifier`.
  * UI integration using `ConsumerWidget` and `ref.watch` / `ref.read`.

---

## 📂 Repository Structure

```text
lib/
 ├── core/                      # Shared models, constants, and network drivers
 ├── features/
 │   ├── bloc_implementation/    # BLoC & Cubit state management workflow
 │   │   ├── bloc/              # Events, States, & BLoC logic
 │   │   ├── cubit/             # Light-weight Cubit controllers
 │   │   └── view/              # UI screens listening to BLoC
 │   │
 │   └── riverpod_implementation/ # Riverpod 2.0+ workflow
 │       ├── providers/         # Notifiers & AsyncNotifiers
 │       └── view/              # UI screens utilizing ConsumerWidget
 │
 └── main.dart                  # Feature switcher entry point
