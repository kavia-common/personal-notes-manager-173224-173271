# Ocean Notes (Astro)

A simple, modern notes app UI built with Astro using the Ocean Professional theme. Notes are stored locally in your browser (localStorage). No backend required.

## Features
- Single-page layout with sidebar and main editor
- Create, select, edit, and delete notes
- Auto-save on blur and manual Save button
- Notes persist in localStorage
- Accessible labels, focus styles, and keyboard selection
- Ocean Professional style: blue primary, amber secondary, rounded corners, subtle shadows, soft gradients

## Getting started

From this container root:

1. Install dependencies
   npm install

2. Start dev server on port 3000 (already configured in astro.config.mjs)
   npm run dev

3. Open the app
   http://localhost:3000

To build and preview:
   npm run build
   npm run preview

## Project structure
- src/styles/theme.css: Global theme variables and shared styles
- src/lib/store.ts: Tiny client-side store with localStorage persistence
- src/pages/index.astro: Main page and layout structure
- src/components/Sidebar.astro: Notes list and New button
- src/components/NoteEditor.astro: Title/content editor with save/delete
- src/components/EmptyState.astro: Placeholder when nothing selected
- src/layouts/Layout.astro: Base HTML document and theme toggle

## Notes on data
All notes are kept in localStorage under keys:
- notes_app__notes
- notes_app__selected

Clearing browser storage will remove notes.

## Accessibility
- Inputs have labels (screen-reader-only for clean UI)
- Keyboard support for selecting notes (Enter/Space)
- Focus-visible ring uses theme color

## Styling
The Ocean Professional style is implemented via CSS variables and utility classes:
- Primary: #2563EB
- Secondary: #F59E0B
- Error: #EF4444
- Background: #f9fafb
- Surface: #ffffff
- Text: #111827

Smooth transitions, rounded corners, and shadows are applied for a modern, professional look.
