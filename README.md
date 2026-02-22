# Archivium Web

Frontend del sistema Archivium.
Interfaz para gestión centralizada de contenido cultural.

---

## 📌 Visión del Proyecto

Aplicación web que permita:

- Gestionar listas de contenido por tipo
- Marcar como visto / leído / jugado
- Calificar contenido
- Sincronizar anime/manga con MyAnimeList
- Configurar cuenta MAL

---

## 🏗 Stack Tecnológico

- React (Vite)
- TailwindCSS
- Axios
- TanStack Query
- TanStack Table
- ChartJS (futuro)
- Storybook

---

## 📂 Funcionalidades MVP

- Login básico
- Listas por tipo:
    - Juegos
    - Anime
    - Manga
    - Películas
    - Libros
    - Series
- Botón:
    - Marcar como completado
    - Editar calificación
- Sincronización con MyAnimeList (anime/manga)
- CRUD completo para contenido propio

---

## 🧠 Arquitectura

- Separación por features
- Hooks personalizados
- Gestión de estado con TanStack Query
- API centralizada vía Axios instance

### 📁 Estructura de Carpetas

```
src/
├── modules/                    # Módulos de la aplicación (por feature)
│   ├── anime/
│   ├── manga/
│   ├── games/
│   ├── movies/
│   ├── books/
│   ├── series/
│   └── [module-name]/
│       ├── components/         # Componentes cuyo estado/lógica es del módulo
│       ├── hooks/              # Hooks específicos del módulo
│       ├── types/              # Tipos/interfaces del módulo
│       ├── utils/              # Utilidades del módulo
│       ├── schemas/            # Schemas Zod del módulo
│       └── index.ts            # Exportaciones del módulo
│
├── shared/                     # Código compartido entre módulos
│   ├── components/             # Componentes UI puros (sin lógica)
│   ├── contexts/               # Contextos globales (auth, user, config)
│   ├── hooks/                  # Hooks compartidos reutilizables
│   ├── types/                  # Tipos/interfaces compartidas
│   ├── utils/                  # Utilidades compartidas
│   ├── schemas/                # Schemas Zod compartidos
│   └── index.ts                # Exportaciones compartidas
│
├── styles/                     # Estilos globales y configuración
│   ├── globals.css
│   ├── variables.css
│   └── tailwind.config.ts
│
├── routes/                     # Configuración de rutas
│   └── router.tsx              # Definición de rutas
│
├── services/                   # Servicios (API calls, integraciones externas)
│   ├── api.ts                  # Instancia de Axios
│   ├── authService.ts
│   ├── myAnimeListService.ts
│   └── [service-name].ts
│
├── App.tsx
├── main.tsx
└── index.css
```

**Notas sobre la organización:**

- **Módulos**: Cada tipo de contenido (anime, manga, etc.) es un módulo independiente
- **Componentes compartidos (ui)**: Botones, inputs, cards, etc. siempre van en `shared/components`
- **Componentes con lógica**: Formularios, modales, etc. van en:
    - Su módulo respectivo si solo se usan en ese módulo
    - `shared/components` si se reutilizan en múltiples módulos
- **Contextos**: Siempre en `shared/contexts` (auth, user, theme, etc.)
- **Hooks**: Pueden estar en el módulo o en `shared/hooks` según su alcance
- **Tipos, Utils, Schemas**: Duplicar en módulos si son específicos, centralizar en `shared` si se usan en varios

---

## 🧪 Testing

- Jest
- React Testing Library
- Playwright (E2E)

Cobertura objetivo:

- 70% mínimo

Se prioriza:

- Test de comportamiento
- Test de integración de componentes
- Flujos completos E2E

---

## 📊 Futuro (No MVP)

- Dashboard analítico
- Gráficas de consumo
- Estadísticas por tipo
- Historial detallado

---

## 🧱 Convenciones de Trabajo

- Feature branches
- Rama exclusiva de testing
- No push directo a main
- Revisión obligatoria antes de merge
- Storybook para componentes reutilizables

---

## 🎯 Objetivo

Centralizar la gestión de consumo cultural en un solo sistema,
con trazabilidad, organización y control total.
