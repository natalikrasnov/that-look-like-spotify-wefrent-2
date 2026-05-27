# deployRocket Project Dossier

This branch is managed by deployRocket. It intentionally stores only this dossier README as machine-readable and human-readable project memory.

Generated application files are committed to the repository default branch after Codex returns a valid file set. If the default branch only has an initial README, code generation has not succeeded yet.

## Agent State

~~~deployrocket-state-json
{
  "id": "bmF0YWxpa3Jhc25vdi90aGF0LWxvb2stbGlrZS1zcG90aWZ5LXdlZnJlbnQtMg",
  "name": "NoirTune AI",
  "summary": "A mobile-first, dark-mode, Spotify-inspired web app that lets users generate AI-style music from prompts, manage a personal library of created tracks, and play, delete, download, or share them—all running fully client-side as a static site.",
  "status": "CODEX_WORKING",
  "currentStep": "Codex is generating project files",
  "githubRepoUrl": "https://github.com/natalikrasnov/that-look-like-spotify-wefrent-2",
  "githubOwner": "natalikrasnov",
  "githubRepo": "that-look-like-spotify-wefrent-2",
  "githubUserLogin": "natalikrasnov",
  "githubDefaultBranch": "main",
  "error": null,
  "createdAt": "2026-05-27T11:03:13.038Z",
  "updatedAt": "2026-05-27T11:05:12.823Z",
  "actions": [
    {
      "id": "action_31cdc0b94c6c17bb318b",
      "at": "2026-05-27T11:03:13.038Z",
      "message": "Received user input",
      "level": "info",
      "status": "IDLE"
    },
    {
      "id": "action_66c79e42a47e7a7970a5",
      "at": "2026-05-27T11:03:16.972Z",
      "message": "Processing user input",
      "level": "info",
      "status": "PROCESSING_INPUT"
    },
    {
      "id": "action_d8223dffb745d77e8264",
      "at": "2026-05-27T11:03:45.060Z",
      "message": "Generated structured product requirements",
      "level": "success",
      "status": "PROCESSING_INPUT"
    },
    {
      "id": "action_7fc6a1609461b8c656b9",
      "at": "2026-05-27T11:03:48.039Z",
      "message": "Creating architecture and implementation prompt",
      "level": "info",
      "status": "GENERATING_PROMPT"
    },
    {
      "id": "action_dc0d3decc46e3491f961",
      "at": "2026-05-27T11:04:53.779Z",
      "message": "Generated structured Codex prompt",
      "level": "success",
      "status": "GENERATING_PROMPT"
    },
    {
      "id": "action_a986ce0afbdb9740a598",
      "at": "2026-05-27T11:04:55.481Z",
      "message": "Sent prompt to Codex",
      "level": "info",
      "status": "SENDING_TO_CODEX"
    },
    {
      "id": "action_263eb85b1b0dbfc8c3a8",
      "at": "2026-05-27T11:05:03.985Z",
      "message": "Generated structured Codex prompt",
      "level": "success",
      "status": "SENDING_TO_CODEX"
    },
    {
      "id": "action_4d85d1433db9cf96b89a",
      "at": "2026-05-27T11:05:05.819Z",
      "message": "Sent prompt to Codex",
      "level": "info",
      "status": "SENDING_TO_CODEX"
    },
    {
      "id": "action_a873a7729a1fbc5c151d",
      "at": "2026-05-27T11:05:12.823Z",
      "message": "Codex started generation",
      "level": "info",
      "status": "CODEX_WORKING"
    }
  ],
  "inputs": [
    {
      "id": "input_8434078b95afeec429d4",
      "kind": "create",
      "text": "create app that look like spotify with wefrent colors(must be dark mode). the purpose of the app is generate music via ai. and have a custom user playback with all the songs the user create (he can delete song and downlod and share). the ai is gemini of google- so add an auth to google and use the ai creadentials  (auto by default (do tell this to the user) for creating music from prompt. there will be setting for how long the song should be and every thing else from user prompt. the ui shold be interactive and easy to use for the user, smooth use. also for the code, use ancle bob method archetecture.",
      "images": [],
      "createdAt": "2026-05-27T11:03:09.660Z",
      "structuredRequirements": {
        "projectName": "NoirTune AI",
        "summary": "A mobile-first, dark-mode, Spotify-inspired web app that lets users generate AI-style music from prompts, manage a personal library of created tracks, and play, delete, download, or share them—all running fully client-side as a static site.",
        "intent": "Provide a smooth, interactive, Spotify-like music experience focused on generating and managing user-created tracks, while remaining a serverless, browser-only app compatible with GitHub Pages.",
        "targetUsers": [
          "Mobile users who want to quickly generate short music ideas from text prompts",
          "Creators who want a simple library + playback experience for generated tracks",
          "Users who prefer a dark, Spotify-like UI/UX"
        ],
        "coreFeatures": [
          "Spotify-inspired dark UI (not identical), with a distinct color palette (non-Spotify colors) and mobile-first navigation",
          "Prompt-to-music generation flow (client-side simulated AI generation)",
          "Generation settings: song duration (seconds), plus additional prompt options (e.g., genre, mood, tempo, instruments, intensity) captured as structured inputs",
          "Track library: list of all generated tracks stored locally (localStorage) with metadata (title, prompt, settings, createdAt, duration)",
          "Custom playback screen: play/pause, seek, time display, next/previous in library queue, volume, repeat/shuffle (client-side)",
          "Track management: delete track, rename title, view details (prompt + settings)",
          "Download track (client-generated audio export when feasible; otherwise export metadata as JSON and/or a placeholder audio file generated via Web Audio API)",
          "Share track via Web Share API when available (share link and/or exported file); fallback to copy-to-clipboard share text",
          "Onboarding/empty states: first-run hints and sample tracks (static seed data) if library is empty",
          "Accessibility basics: readable contrast in dark mode, keyboard support for primary controls, ARIA labels for player buttons",
          "Architecture requirement: Uncle Bob / Clean Architecture style separation (domain entities + use cases + adapters + UI)"
        ],
        "screens": [
          "Splash/Loading (brief app init, optional)",
          "Home (featured/quick actions: Generate, Recent tracks)",
          "Generate (prompt input + advanced settings + generate button + progress simulation)",
          "Library (all user-created tracks with search/filter/sort)",
          "Now Playing (full player UI: artwork placeholder, controls, queue)",
          "Track Details (prompt/settings/createdAt, actions: rename, download, share, delete)",
          "Settings (app-level preferences: default duration, playback defaults, theme accent selection within dark mode)",
          "About/Help (explains client-side simulated AI behavior and limitations)"
        ],
        "designDirection": "Mobile-first, Spotify-like layout patterns (bottom tab navigation, card-based lists, prominent player), but with a unique dark palette (e.g., deep charcoal background with a neon accent like purple/teal). Smooth transitions, subtle gradients, glass/blur accents used sparingly, responsive typography, and large touch targets. UI should feel fast with skeleton loaders and micro-interactions for generation and playback.",
        "constraints": [
          "Must be a serverless, browser-only web app runnable from static files on GitHub Pages (no backend/server).",
          "No real Google OAuth sign-in flow and no real Gemini API credential handling can be performed securely in a static-only app; implement as a simulated 'Sign in with Google' UI state stored in localStorage (mock user profile) and clearly label it as simulated in the UI.",
          "No real AI music generation via Gemini (or any external AI) unless the user manually provides their own key and accepts client-side exposure; by default implement client-side simulated generation (e.g., procedural audio using Web Audio API) and store resulting audio/metadata locally.",
          "All data persistence must use localStorage/IndexedDB (preferred for blobs) and/or in-memory state; include export/import library as JSON for backup.",
          "Downloads and sharing must work without a server: generate a Blob URL for audio/JSON and use Web Share API where supported; provide fallbacks.",
          "Performance: optimized for mobile; minimize bundle size; avoid heavy dependencies where possible.",
          "Clean Architecture (Uncle Bob) enforced in code organization: domain layer independent of UI frameworks, use cases orchestrate behavior, interface adapters for storage/audio/share, UI layer for views."
        ],
        "imageContext": [],
        "repositoryNameSuggestion": "noirtune-ai"
      },
      "codexPrompt": {
        "title": "NoirTune AI — Static Vite React TS (Spotify-like dark UI) with Clean Architecture, client-only AI music simulation",
        "summary": "Create a production-oriented, mobile-first, dark-mode, Spotify-inspired (but unique palette) static web app that simulates AI music generation from prompts, stores a personal track library locally, and provides a custom playback experience with delete/download/share. Must be 100% browser-only (GitHub Pages compatible) and follow Uncle Bob / Clean Architecture separation.",
        "architectureInstructions": [
          "Use Clean Architecture (Uncle Bob) with strict layer separation and dependency direction: UI (React) -> application (use cases) -> domain (entities/interfaces). Infrastructure/adapters implement interfaces and are injected.",
          "Organize code into: src/domain (entities, value objects, repository ports), src/application (use cases, DTOs), src/infrastructure (implementations: storage, audio generation, sharing, download, clock/uuid), src/presentation (React routes/pages/components, hooks, state).",
          "Domain must be framework-agnostic: no React, no browser globals inside domain/application layers (wrap browser APIs behind interfaces in infrastructure).",
          "Use small dependency surface; prefer custom utilities over heavy UI/state libs. If using any external lib, justify and keep minimal (e.g., none or a tiny idb helper).",
          "No TODOs/placeholders that break flows; all core features must be implemented end-to-end, even if AI generation is simulated.",
          "Provide a clear disclaimer in the UI: Google sign-in and Gemini AI generation are simulated in this static demo; no real OAuth or API keys are used by default.",
          "All persistence must be localStorage and/or IndexedDB. Prefer IndexedDB for audio blobs and localStorage for small preferences/auth state. Include export/import JSON for backup.",
          "Ensure GitHub Pages compatibility including repository subpath deployment: configure Vite base to './' and use HashRouter to avoid 404 routing issues."
        ],
        "frontendInstructions": [
          "Tech: Vite + React + TypeScript. Use React Router with HashRouter. Mobile-first layout with bottom tab navigation (Home, Generate, Library, Settings). Add Now Playing route and Track Details route.",
          "Design: Dark mode only with a unique palette (NOT Spotify green). Use deep charcoal background + neon accent (e.g., purple/teal). Implement CSS variables for theme + accent selection in Settings. Provide smooth transitions, subtle gradients, skeleton loaders for generation.",
          "Accessibility: large touch targets, keyboard support for main controls, visible focus rings, aria-labels for icon buttons, sufficient contrast. Player controls must be reachable via keyboard.",
          "UI elements: top header with app name/avatar; cards for tracks; search bar; sort/filter chips; empty states with helpful hints; toasts/snackbars for actions (saved, deleted, copied).",
          "Playback: custom player using HTMLAudioElement with Blob URLs from stored audio. Provide play/pause, seek bar, current time/duration, next/prev, volume, mute, shuffle, repeat (off/one/all). Show mini-player persistent at bottom above tabs when a track is selected.",
          "Track actions: delete, rename, download, share. Download should save WAV audio when available; also allow metadata JSON download. Share should use Web Share API when supported; fallback to copy-to-clipboard share text (track title + prompt/settings summary).",
          "Generation screen: prompt textarea + advanced settings (duration seconds, genre, mood, tempo BPM, instruments tags, intensity). Generate button triggers simulated progress (staged: “Analyzing”, “Composing”, “Rendering”). On completion, saves track and navigates to Now Playing.",
          "Auth: Provide a simulated “Sign in with Google” UI (no real OAuth). Store mock user profile in localStorage. Show user avatar initials. Allow sign out.",
          "Seed data: On first run, if no tracks exist, offer to create a couple of sample tracks (procedurally generated) or display example cards with a one-tap “Generate sample” action."
        ],
        "backendInstructions": [
          "None. Absolutely no server, no serverless functions, no external APIs, no secret handling. All behavior must be client-side using simulated generation + local persistence.",
          "Do NOT implement real Google OAuth or Gemini API calls. Implement mock auth state and simulated AI generation only, and label it clearly in About/Help and near auth/generation UI."
        ],
        "modificationInstructions": [
          "Return a COMPLETE replacement file set for a new repository (create mode). Include all config files and source files needed to build and run.",
          "Include: package.json, index.html, vite.config.ts, tsconfig.json, tsconfig.node.json, public assets (favicon optional), and all src/* files.",
          "Ensure `npm install`, `npm run dev`, and `npm run build` succeed with no missing imports.",
          "No placeholder TODOs; all routes must render and core flows must work offline."
        ],
        "acceptanceCriteria": [
          "Builds as a static site via Vite and runs fully in-browser with no backend.",
          "GitHub Pages compatible: Vite base set to './' and routing works under a subpath using HashRouter.",
          "Dark-mode-only Spotify-like experience with distinct non-Spotify color palette; mobile-first bottom tabs; smooth interactions.",
          "Simulated Google sign-in (localStorage) with clear disclaimer; no real OAuth.",
          "Simulated AI music generation from prompt/settings producing an actual playable audio file (procedural via Web Audio), saved locally.",
          "Track library persisted locally; list/search/sort; track details view; rename/delete work.",
          "Custom playback (mini + full now playing) supports play/pause/seek/next/prev/volume/shuffle/repeat.",
          "Download (WAV + metadata JSON) works; Share via Web Share API with clipboard fallback works.",
          "Export/import library JSON works (and rehydrates metadata + any stored audio where possible).",
          "Clean Architecture structure present: domain/application independent of React; infrastructure implements ports; UI depends on use cases via adapters."
        ],
        "codexPrompt": "You are Codex. Generate a complete, production-ready static Vite + React + TypeScript application named “NoirTune AI”. Return the FULL FILE SET as a complete replacement (every file with its full contents). The app must be 100% browser-only and deployable to GitHub Pages (no backend, no secrets, no external APIs).\n\nHIGH-LEVEL PRODUCT\n- Spotify-inspired (layout patterns only), dark-mode-only music app with a unique palette (deep charcoal + neon purple/teal accents; NOT Spotify green).\n- Purpose: generate music “via AI” from a text prompt and settings. Since this is a static app, implement AI generation as a client-side simulation that procedurally generates audio using the Web Audio API.\n- Users can manage their generated tracks in a personal library: play, queue, delete, rename, download, share.\n- Must feel smooth and interactive: micro-interactions, skeleton/progress states, responsive, mobile-first.\n\nCRITICAL CONSTRAINTS\n- Static-only: NO server, NO serverless functions, NO databases, NO private APIs.\n- Do NOT implement real Google OAuth or Gemini API calls. Implement a simulated “Sign in with Google” UI and store a mock user profile in localStorage. Clearly disclose in UI (About/Help and near relevant UI) that auth + Gemini generation are simulated in this demo.\n- Persist data locally using IndexedDB (audio blobs) + localStorage (metadata/preferences/auth). Must work offline.\n- GitHub Pages compatibility: use `HashRouter` and set Vite `base: './'`.\n\nARCHITECTURE (UNCLE BOB / CLEAN ARCHITECTURE)\nEnforce separation and dependency rule:\n1) domain (no React, no browser globals):\n   - Entities/types: Track, TrackId, GenerationSettings, UserProfile, PlaybackState.\n   - Repository ports (interfaces): TrackRepository, PreferencesRepository, AuthRepository.\n   - Domain utilities: validation, formatting helpers (pure).\n2) application (use cases, no React):\n   - Use cases: generateTrack, listTracks, getTrack, renameTrack, deleteTrack, exportLibrary, importLibrary, signInMock, signOut, updatePreferences.\n   - Each use case takes dependencies via constructor or parameters (ports).\n3) infrastructure (adapters/implementations):\n   - Storage:\n     - Track metadata in localStorage OR IndexedDB, but audio blobs MUST be in IndexedDB.\n     - Implement IndexedDB wrapper without heavy libs (write a small helper) or use a tiny dependency only if necessary.\n   - Audio generation:\n     - Implement procedural audio generation based on settings using Web Audio API.\n     - Use OfflineAudioContext to render audio buffer for the chosen duration.\n     - Encode buffer to WAV (implement a WAV encoder utility) and store Blob in IndexedDB.\n   - Share/download adapters:\n     - Download: create Blob URLs and trigger download for WAV and JSON.\n     - Share: Web Share API if supported, otherwise copy-to-clipboard.\n   - Utilities: uuid generator (crypto.randomUUID when available with fallback), clock.\n4) presentation (React UI):\n   - Routes/pages/components. UI calls application use cases via a dependency container.\n   - Global state with React context + reducer (or minimal custom store). Avoid heavy state libs.\n\nFEATURES TO IMPLEMENT\nROUTES / SCREENS\n- Splash/Loading: brief init while loading repositories and preferences.\n- Home: quick actions (Generate), recent tracks, and a CTA if empty.\n- Generate: prompt textarea + advanced settings:\n  - duration (seconds)\n  - genre (select)\n  - mood (select)\n  - tempo BPM (slider)\n  - instruments (tag input)\n  - intensity (slider)\n  - optional seed (number) for reproducibility\n  Generate button shows a staged progress simulation and then saves a new track.\n- Library: list of all tracks with search, sort (recent, title, duration), and filter chips (genre/mood). Each track card has quick actions.\n- Now Playing: full player view with artwork placeholder, title, controls, seek, queue list.\n- Track Details: shows prompt + settings + createdAt, actions: rename, download WAV, download JSON, share, delete.\n- Settings:\n  - default duration\n  - default volume\n  - accent color picker (within dark theme)\n  - toggles: reduce motion (optional)\n  - export/import library JSON\n  - mock Google sign-in/out\n- About/Help: clearly explain limitations: client-side simulated auth + AI generation; no real Gemini.\n\nPLAYBACK\n- Implement a PlayerController in infrastructure or application that manages:\n  - current track id, queue order, shuffle, repeat mode (off/one/all), volume, isPlaying.\n- Use an HTMLAudioElement for playback of WAV Blob URLs.\n- Mini-player persists above bottom tabs when a track is selected.\n- Next/previous navigates within library queue; shuffle randomizes but preserves ability to go back.\n\nDATA MODEL\n- Track metadata includes: id, title, prompt, settings, createdAt ISO, durationSec, audioBlobId/reference, waveform optional.\n- Store audio blob in IndexedDB keyed by track id.\n\nEXPORT/IMPORT\n- Export library JSON: metadata + (optionally) omit audio blobs to keep it simple; BUT provide a clear message.\n- Import library JSON: merge/replace behavior with user choice; if audio missing, imported tracks appear but are not playable until regenerated (make UI graceful).\n\nUI/UX\n- Mobile-first, bottom tab bar with icons (use inline SVG).\n- Smooth transitions, subtle gradients, skeletons during generation.\n- Toast notifications for: saved, deleted, copied, downloaded, import success/failure.\n- Strong accessibility: aria-labels on controls, focus outlines, keyboard shortcuts for space play/pause on Now Playing.\n\nIMPLEMENTATION DETAILS\n- Tooling:\n  - Vite React TS template.\n  - React Router.\n  - No Tailwind required; implement polished CSS with variables and reusable components.\n- GitHub Pages:\n  - vite.config.ts sets base: './'\n  - use HashRouter\n\nDELIVERABLE\nReturn the complete repository file tree with full contents. Include at minimum:\n- package.json with scripts: dev, build, preview\n- vite.config.ts\n- tsconfig.json, tsconfig.node.json\n- index.html\n- src/main.tsx, src/App.tsx\n- src/presentation/* (routes/pages/components/styles)\n- src/domain/*\n- src/application/*\n- src/infrastructure/*\n- src/shared/* (if needed)\n\nQUALITY BAR\n- Must run without external services.\n- No broken routes, no TODO stubs.\n- Procedural audio generation must create a real playable WAV.\n- Local persistence must work.\n- Clean Architecture must be evident from folder structure and dependency direction.\n\nNow generate the full codebase."
      }
    }
  ],
  "lastCommittedPaths": [],
  "autoRepairAttempts": [],
  "activeInputId": "input_8434078b95afeec429d4",
  "activeRunKind": "create"
}
~~~

## Status

Current stage: **Codex is generating project files**

Complete: **no**

| Stage | State |
| --- | --- |
| Received user prompt | done |
| Generated product requirements | done |
| Created architecture plan | done |
| Generated project code | current |
| Committed files to GitHub | pending |
| Published project | pending |

## Project

Name: NoirTune AI

Summary: A mobile-first, dark-mode, Spotify-inspired web app that lets users generate AI-style music from prompts, manage a personal library of created tracks, and play, delete, download, or share them—all running fully client-side as a static site.

Repository: https://github.com/natalikrasnov/that-look-like-spotify-wefrent-2

Live site: pending GitHub Pages publish

GitHub Pages status: pending

Code branch: main

State branch: deployrocket-state

## Original Prompt

create app that look like spotify with wefrent colors(must be dark mode). the purpose of the app is generate music via ai. and have a custom user playback with all the songs the user create (he can delete song and downlod and share). the ai is gemini of google- so add an auth to google and use the ai creadentials  (auto by default (do tell this to the user) for creating music from prompt. there will be setting for how long the song should be and every thing else from user prompt. the ui shold be interactive and easy to use for the user, smooth use. also for the code, use ancle bob method archetecture.

## Architecture And Prompt

### Structured Requirements

~~~json
{
  "projectName": "NoirTune AI",
  "summary": "A mobile-first, dark-mode, Spotify-inspired web app that lets users generate AI-style music from prompts, manage a personal library of created tracks, and play, delete, download, or share them—all running fully client-side as a static site.",
  "intent": "Provide a smooth, interactive, Spotify-like music experience focused on generating and managing user-created tracks, while remaining a serverless, browser-only app compatible with GitHub Pages.",
  "targetUsers": [
    "Mobile users who want to quickly generate short music ideas from text prompts",
    "Creators who want a simple library + playback experience for generated tracks",
    "Users who prefer a dark, Spotify-like UI/UX"
  ],
  "coreFeatures": [
    "Spotify-inspired dark UI (not identical), with a distinct color palette (non-Spotify colors) and mobile-first navigation",
    "Prompt-to-music generation flow (client-side simulated AI generation)",
    "Generation settings: song duration (seconds), plus additional prompt options (e.g., genre, mood, tempo, instruments, intensity) captured as structured inputs",
    "Track library: list of all generated tracks stored locally (localStorage) with metadata (title, prompt, settings, createdAt, duration)",
    "Custom playback screen: play/pause, seek, time display, next/previous in library queue, volume, repeat/shuffle (client-side)",
    "Track management: delete track, rename title, view details (prompt + settings)",
    "Download track (client-generated audio export when feasible; otherwise export metadata as JSON and/or a placeholder audio file generated via Web Audio API)",
    "Share track via Web Share API when available (share link and/or exported file); fallback to copy-to-clipboard share text",
    "Onboarding/empty states: first-run hints and sample tracks (static seed data) if library is empty",
    "Accessibility basics: readable contrast in dark mode, keyboard support for primary controls, ARIA labels for player buttons",
    "Architecture requirement: Uncle Bob / Clean Architecture style separation (domain entities + use cases + adapters + UI)"
  ],
  "screens": [
    "Splash/Loading (brief app init, optional)",
    "Home (featured/quick actions: Generate, Recent tracks)",
    "Generate (prompt input + advanced settings + generate button + progress simulation)",
    "Library (all user-created tracks with search/filter/sort)",
    "Now Playing (full player UI: artwork placeholder, controls, queue)",
    "Track Details (prompt/settings/createdAt, actions: rename, download, share, delete)",
    "Settings (app-level preferences: default duration, playback defaults, theme accent selection within dark mode)",
    "About/Help (explains client-side simulated AI behavior and limitations)"
  ],
  "designDirection": "Mobile-first, Spotify-like layout patterns (bottom tab navigation, card-based lists, prominent player), but with a unique dark palette (e.g., deep charcoal background with a neon accent like purple/teal). Smooth transitions, subtle gradients, glass/blur accents used sparingly, responsive typography, and large touch targets. UI should feel fast with skeleton loaders and micro-interactions for generation and playback.",
  "constraints": [
    "Must be a serverless, browser-only web app runnable from static files on GitHub Pages (no backend/server).",
    "No real Google OAuth sign-in flow and no real Gemini API credential handling can be performed securely in a static-only app; implement as a simulated 'Sign in with Google' UI state stored in localStorage (mock user profile) and clearly label it as simulated in the UI.",
    "No real AI music generation via Gemini (or any external AI) unless the user manually provides their own key and accepts client-side exposure; by default implement client-side simulated generation (e.g., procedural audio using Web Audio API) and store resulting audio/metadata locally.",
    "All data persistence must use localStorage/IndexedDB (preferred for blobs) and/or in-memory state; include export/import library as JSON for backup.",
    "Downloads and sharing must work without a server: generate a Blob URL for audio/JSON and use Web Share API where supported; provide fallbacks.",
    "Performance: optimized for mobile; minimize bundle size; avoid heavy dependencies where possible.",
    "Clean Architecture (Uncle Bob) enforced in code organization: domain layer independent of UI frameworks, use cases orchestrate behavior, interface adapters for storage/audio/share, UI layer for views."
  ],
  "imageContext": [],
  "repositoryNameSuggestion": "noirtune-ai"
}
~~~

### Codex Prompt Plan

~~~json
{
  "title": "NoirTune AI — Static Vite React TS (Spotify-like dark UI) with Clean Architecture, client-only AI music simulation",
  "summary": "Create a production-oriented, mobile-first, dark-mode, Spotify-inspired (but unique palette) static web app that simulates AI music generation from prompts, stores a personal track library locally, and provides a custom playback experience with delete/download/share. Must be 100% browser-only (GitHub Pages compatible) and follow Uncle Bob / Clean Architecture separation.",
  "architectureInstructions": [
    "Use Clean Architecture (Uncle Bob) with strict layer separation and dependency direction: UI (React) -> application (use cases) -> domain (entities/interfaces). Infrastructure/adapters implement interfaces and are injected.",
    "Organize code into: src/domain (entities, value objects, repository ports), src/application (use cases, DTOs), src/infrastructure (implementations: storage, audio generation, sharing, download, clock/uuid), src/presentation (React routes/pages/components, hooks, state).",
    "Domain must be framework-agnostic: no React, no browser globals inside domain/application layers (wrap browser APIs behind interfaces in infrastructure).",
    "Use small dependency surface; prefer custom utilities over heavy UI/state libs. If using any external lib, justify and keep minimal (e.g., none or a tiny idb helper).",
    "No TODOs/placeholders that break flows; all core features must be implemented end-to-end, even if AI generation is simulated.",
    "Provide a clear disclaimer in the UI: Google sign-in and Gemini AI generation are simulated in this static demo; no real OAuth or API keys are used by default.",
    "All persistence must be localStorage and/or IndexedDB. Prefer IndexedDB for audio blobs and localStorage for small preferences/auth state. Include export/import JSON for backup.",
    "Ensure GitHub Pages compatibility including repository subpath deployment: configure Vite base to './' and use HashRouter to avoid 404 routing issues."
  ],
  "frontendInstructions": [
    "Tech: Vite + React + TypeScript. Use React Router with HashRouter. Mobile-first layout with bottom tab navigation (Home, Generate, Library, Settings). Add Now Playing route and Track Details route.",
    "Design: Dark mode only with a unique palette (NOT Spotify green). Use deep charcoal background + neon accent (e.g., purple/teal). Implement CSS variables for theme + accent selection in Settings. Provide smooth transitions, subtle gradients, skeleton loaders for generation.",
    "Accessibility: large touch targets, keyboard support for main controls, visible focus rings, aria-labels for icon buttons, sufficient contrast. Player controls must be reachable via keyboard.",
    "UI elements: top header with app name/avatar; cards for tracks; search bar; sort/filter chips; empty states with helpful hints; toasts/snackbars for actions (saved, deleted, copied).",
    "Playback: custom player using HTMLAudioElement with Blob URLs from stored audio. Provide play/pause, seek bar, current time/duration, next/prev, volume, mute, shuffle, repeat (off/one/all). Show mini-player persistent at bottom above tabs when a track is selected.",
    "Track actions: delete, rename, download, share. Download should save WAV audio when available; also allow metadata JSON download. Share should use Web Share API when supported; fallback to copy-to-clipboard share text (track title + prompt/settings summary).",
    "Generation screen: prompt textarea + advanced settings (duration seconds, genre, mood, tempo BPM, instruments tags, intensity). Generate button triggers simulated progress (staged: “Analyzing”, “Composing”, “Rendering”). On completion, saves track and navigates to Now Playing.",
    "Auth: Provide a simulated “Sign in with Google” UI (no real OAuth). Store mock user profile in localStorage. Show user avatar initials. Allow sign out.",
    "Seed data: On first run, if no tracks exist, offer to create a couple of sample tracks (procedurally generated) or display example cards with a one-tap “Generate sample” action."
  ],
  "backendInstructions": [
    "None. Absolutely no server, no serverless functions, no external APIs, no secret handling. All behavior must be client-side using simulated generation + local persistence.",
    "Do NOT implement real Google OAuth or Gemini API calls. Implement mock auth state and simulated AI generation only, and label it clearly in About/Help and near auth/generation UI."
  ],
  "modificationInstructions": [
    "Return a COMPLETE replacement file set for a new repository (create mode). Include all config files and source files needed to build and run.",
    "Include: package.json, index.html, vite.config.ts, tsconfig.json, tsconfig.node.json, public assets (favicon optional), and all src/* files.",
    "Ensure `npm install`, `npm run dev`, and `npm run build` succeed with no missing imports.",
    "No placeholder TODOs; all routes must render and core flows must work offline."
  ],
  "acceptanceCriteria": [
    "Builds as a static site via Vite and runs fully in-browser with no backend.",
    "GitHub Pages compatible: Vite base set to './' and routing works under a subpath using HashRouter.",
    "Dark-mode-only Spotify-like experience with distinct non-Spotify color palette; mobile-first bottom tabs; smooth interactions.",
    "Simulated Google sign-in (localStorage) with clear disclaimer; no real OAuth.",
    "Simulated AI music generation from prompt/settings producing an actual playable audio file (procedural via Web Audio), saved locally.",
    "Track library persisted locally; list/search/sort; track details view; rename/delete work.",
    "Custom playback (mini + full now playing) supports play/pause/seek/next/prev/volume/shuffle/repeat.",
    "Download (WAV + metadata JSON) works; Share via Web Share API with clipboard fallback works.",
    "Export/import library JSON works (and rehydrates metadata + any stored audio where possible).",
    "Clean Architecture structure present: domain/application independent of React; infrastructure implements ports; UI depends on use cases via adapters."
  ],
  "codexPrompt": "You are Codex. Generate a complete, production-ready static Vite + React + TypeScript application named “NoirTune AI”. Return the FULL FILE SET as a complete replacement (every file with its full contents). The app must be 100% browser-only and deployable to GitHub Pages (no backend, no secrets, no external APIs).\n\nHIGH-LEVEL PRODUCT\n- Spotify-inspired (layout patterns only), dark-mode-only music app with a unique palette (deep charcoal + neon purple/teal accents; NOT Spotify green).\n- Purpose: generate music “via AI” from a text prompt and settings. Since this is a static app, implement AI generation as a client-side simulation that procedurally generates audio using the Web Audio API.\n- Users can manage their generated tracks in a personal library: play, queue, delete, rename, download, share.\n- Must feel smooth and interactive: micro-interactions, skeleton/progress states, responsive, mobile-first.\n\nCRITICAL CONSTRAINTS\n- Static-only: NO server, NO serverless functions, NO databases, NO private APIs.\n- Do NOT implement real Google OAuth or Gemini API calls. Implement a simulated “Sign in with Google” UI and store a mock user profile in localStorage. Clearly disclose in UI (About/Help and near relevant UI) that auth + Gemini generation are simulated in this demo.\n- Persist data locally using IndexedDB (audio blobs) + localStorage (metadata/preferences/auth). Must work offline.\n- GitHub Pages compatibility: use `HashRouter` and set Vite `base: './'`.\n\nARCHITECTURE (UNCLE BOB / CLEAN ARCHITECTURE)\nEnforce separation and dependency rule:\n1) domain (no React, no browser globals):\n   - Entities/types: Track, TrackId, GenerationSettings, UserProfile, PlaybackState.\n   - Repository ports (interfaces): TrackRepository, PreferencesRepository, AuthRepository.\n   - Domain utilities: validation, formatting helpers (pure).\n2) application (use cases, no React):\n   - Use cases: generateTrack, listTracks, getTrack, renameTrack, deleteTrack, exportLibrary, importLibrary, signInMock, signOut, updatePreferences.\n   - Each use case takes dependencies via constructor or parameters (ports).\n3) infrastructure (adapters/implementations):\n   - Storage:\n     - Track metadata in localStorage OR IndexedDB, but audio blobs MUST be in IndexedDB.\n     - Implement IndexedDB wrapper without heavy libs (write a small helper) or use a tiny dependency only if necessary.\n   - Audio generation:\n     - Implement procedural audio generation based on settings using Web Audio API.\n     - Use OfflineAudioContext to render audio buffer for the chosen duration.\n     - Encode buffer to WAV (implement a WAV encoder utility) and store Blob in IndexedDB.\n   - Share/download adapters:\n     - Download: create Blob URLs and trigger download for WAV and JSON.\n     - Share: Web Share API if supported, otherwise copy-to-clipboard.\n   - Utilities: uuid generator (crypto.randomUUID when available with fallback), clock.\n4) presentation (React UI):\n   - Routes/pages/components. UI calls application use cases via a dependency container.\n   - Global state with React context + reducer (or minimal custom store). Avoid heavy state libs.\n\nFEATURES TO IMPLEMENT\nROUTES / SCREENS\n- Splash/Loading: brief init while loading repositories and preferences.\n- Home: quick actions (Generate), recent tracks, and a CTA if empty.\n- Generate: prompt textarea + advanced settings:\n  - duration (seconds)\n  - genre (select)\n  - mood (select)\n  - tempo BPM (slider)\n  - instruments (tag input)\n  - intensity (slider)\n  - optional seed (number) for reproducibility\n  Generate button shows a staged progress simulation and then saves a new track.\n- Library: list of all tracks with search, sort (recent, title, duration), and filter chips (genre/mood). Each track card has quick actions.\n- Now Playing: full player view with artwork placeholder, title, controls, seek, queue list.\n- Track Details: shows prompt + settings + createdAt, actions: rename, download WAV, download JSON, share, delete.\n- Settings:\n  - default duration\n  - default volume\n  - accent color picker (within dark theme)\n  - toggles: reduce motion (optional)\n  - export/import library JSON\n  - mock Google sign-in/out\n- About/Help: clearly explain limitations: client-side simulated auth + AI generation; no real Gemini.\n\nPLAYBACK\n- Implement a PlayerController in infrastructure or application that manages:\n  - current track id, queue order, shuffle, repeat mode (off/one/all), volume, isPlaying.\n- Use an HTMLAudioElement for playback of WAV Blob URLs.\n- Mini-player persists above bottom tabs when a track is selected.\n- Next/previous navigates within library queue; shuffle randomizes but preserves ability to go back.\n\nDATA MODEL\n- Track metadata includes: id, title, prompt, settings, createdAt ISO, durationSec, audioBlobId/reference, waveform optional.\n- Store audio blob in IndexedDB keyed by track id.\n\nEXPORT/IMPORT\n- Export library JSON: metadata + (optionally) omit audio blobs to keep it simple; BUT provide a clear message.\n- Import library JSON: merge/replace behavior with user choice; if audio missing, imported tracks appear but are not playable until regenerated (make UI graceful).\n\nUI/UX\n- Mobile-first, bottom tab bar with icons (use inline SVG).\n- Smooth transitions, subtle gradients, skeletons during generation.\n- Toast notifications for: saved, deleted, copied, downloaded, import success/failure.\n- Strong accessibility: aria-labels on controls, focus outlines, keyboard shortcuts for space play/pause on Now Playing.\n\nIMPLEMENTATION DETAILS\n- Tooling:\n  - Vite React TS template.\n  - React Router.\n  - No Tailwind required; implement polished CSS with variables and reusable components.\n- GitHub Pages:\n  - vite.config.ts sets base: './'\n  - use HashRouter\n\nDELIVERABLE\nReturn the complete repository file tree with full contents. Include at minimum:\n- package.json with scripts: dev, build, preview\n- vite.config.ts\n- tsconfig.json, tsconfig.node.json\n- index.html\n- src/main.tsx, src/App.tsx\n- src/presentation/* (routes/pages/components/styles)\n- src/domain/*\n- src/application/*\n- src/infrastructure/*\n- src/shared/* (if needed)\n\nQUALITY BAR\n- Must run without external services.\n- No broken routes, no TODO stubs.\n- Procedural audio generation must create a real playable WAV.\n- Local persistence must work.\n- Clean Architecture must be evident from folder structure and dependency direction.\n\nNow generate the full codebase."
}
~~~

## Action History

- 2026-05-27T11:03:13.038Z - Received user input (info)
- 2026-05-27T11:03:16.972Z - Processing user input (info)
- 2026-05-27T11:03:45.060Z - Generated structured product requirements (success)
- 2026-05-27T11:03:48.039Z - Creating architecture and implementation prompt (info)
- 2026-05-27T11:04:53.779Z - Generated structured Codex prompt (success)
- 2026-05-27T11:04:55.481Z - Sent prompt to Codex (info)
- 2026-05-27T11:05:03.985Z - Generated structured Codex prompt (success)
- 2026-05-27T11:05:05.819Z - Sent prompt to Codex (info)
- 2026-05-27T11:05:12.823Z - Codex started generation (info)

## Latest Error

None.
