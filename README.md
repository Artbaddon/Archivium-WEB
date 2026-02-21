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