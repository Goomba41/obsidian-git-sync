---
status: draft
layer: architecture
related: [[DDD-Clean-Arch-Flow]], [[Atomic-BEM-Integration]]
tags: [#architecture, #nuxt, #vue3, #ddd, #clean-arch, #hidden-hippo]
---
# 🗂️ Структура проекта Hidden Hippo

## 🎯 Назначение
Структура проекта объединяет **DDD + Clean Architecture** на уровне бизнес-логики и **Atomic Design + BEM** на уровне UI. Nuxt 3 используется как фреймворк-оркестратор с SSR/ISR, подготовкой к кэшированию и оффлайн-режиму.

## 📐 Маппинг папок → Архитектурные слои

| Папка в проекте | Архитектурный слой | Ответственность | Примеры |
|----------------|-------------------|----------------|---------|
| `core/domain/` | Domain Layer | Сущности, value objects, интерфейсы репозиториев, domain events | `entities/`, `types/password.ts`, `repositories/` |
| `core/application/` | Application Layer | Use-cases, DTOs, оркестрация сценариев, валидация на уровне бизнес-правил | `use-cases/validatePassword.ts`, `dtos/` |
| `entities/` | Feature-Entities + Basic UI | Доменные сущности с примитивным UI (карточки, списки) | `patient-card/`, `license-info/` |
| `features/` | Use-Case Implementation | Бизнес-фичи, связка UI + composable + use-case | `login-form/`, `license-activation/`, `report-export/` |
| `widgets/` | Composition Layer | Композиция фич и сущностей в бизнес-блоки | `dashboard-header/`, `analytics-filter-bar/` |
| `shared/` | Cross-cutting | Переиспользуемые утилиты, UI-атомы/молекулы, хелперы | `ui/atoms/Button.vue`, `useLocale.ts` |
| `app/` | App Layer | Роутинг, лейауты, глобальные провайдеры, инициализация | `layout/default.vue`, `providers/` |
| `components/app/layout` | Presentation Shell | Верхнеуровневые оболочки приложения | `Header.vue`, `Sidebar.vue`, `Footer.vue` |
| `stores/` | State Management | Глобальное состояние (Pinia), кэш-менеджер, offline queue | `auth.store.ts`, `cache.store.ts` |
| `composables/` | Vue Logic Layer | Reactivity-логика, хуки жизненного цикла, адаптеры | `useNetwork.ts`, `useTheme.ts` |

## 🔄 Направление зависимостей