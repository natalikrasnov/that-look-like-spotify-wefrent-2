# deployRocket Project Dossier

This branch is managed by deployRocket. It intentionally stores only this dossier README as machine-readable and human-readable project memory.

Generated application files are committed to the repository default branch after Codex returns a valid file set. If the default branch only has an initial README, code generation has not succeeded yet.

## Agent State

~~~deployrocket-state-json
{
  "id": "bmF0YWxpa3Jhc25vdi90aGF0LWxvb2stbGlrZS1zcG90aWZ5LXdlZnJlbnQtMg",
  "name": "NoirTune AI",
  "summary": "A mobile-first, dark-mode, Spotify-inspired web app that lets users generate AI-style music from prompts, manage a personal library of created tracks, and play, delete, download, or share them—all running fully client-side as a static site.",
  "status": "GENERATING_PROMPT",
  "currentStep": "Generating Codex prompt",
  "githubRepoUrl": "https://github.com/natalikrasnov/that-look-like-spotify-wefrent-2",
  "githubOwner": "natalikrasnov",
  "githubRepo": "that-look-like-spotify-wefrent-2",
  "githubUserLogin": "natalikrasnov",
  "githubDefaultBranch": "main",
  "error": null,
  "createdAt": "2026-05-27T11:03:13.038Z",
  "updatedAt": "2026-05-27T11:04:49.499Z",
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
        "title": "NoirTune AI — Static Vite React + TypeScript (Clean Architecture) Spotify-like Dark UI Music Generator",
        "summary": "Build a production-ready, mobile-first, dark-mode, Spotify-inspired (but not identical) static web app that simulates AI music generation client-side, includes a library and custom playback, and runs fully in the browser (GitHub Pages compatible). Use Uncle Bob / Clean Architecture layering with domain/use-cases/adapters/UI separation. No real OAuth or Gemini calls—simulate sign-in and generation, store all data locally (localStorage + IndexedDB).",
        "architectureInstructions": [
          "Enforce Clean Architecture (Uncle Bob): separate `domain` (entities/value objects), `application` (use cases), `adapters` (interfaces + implementations), `ui` (React components/pages). Domain must not import React or browser APIs.",
          "Use dependency inversion: UI depends on use-case interfaces; concrete implementations live in `infrastructure` and are wired in a single composition root (e.g., `src/app/di/container.ts`).",
          "Define domain entities: `Track`, `TrackId`, `GenerationSettings`, `UserProfile`, `AppPreferences` with strong TypeScript types.",
          "Define repository/service interfaces in `application/ports`: `TrackRepository`, `AuthRepository`, `PreferencesRepository`, `AudioGenerator`, `ShareService`, `ClipboardService`.",
          "Implement adapters/infrastructure: localStorage for auth + preferences + metadata, IndexedDB for audio blobs, Web Audio API for generation, Web Share API + clipboard fallback for sharing.",
          "No backend, no secrets, no external private APIs, no serverless functions. Any 'Gemini' functionality must be clearly labeled as simulated in UI and implemented locally.",
          "Make the app resilient: handle missing Web Share API, handle Safari/iOS audio quirks, show friendly errors, provide empty states and first-run onboarding.",
          "Use HashRouter (or equivalent) to ensure GitHub Pages routing works under repository subpaths. Also set Vite base to relative (`base: './'`)."
        ],
        "frontendInstructions": [
          "Tech: Vite + React + TypeScript, static build only. Use React Router with hash routing for GH Pages compatibility.",
          "Design: dark-mode only with unique palette (not Spotify green). Use deep charcoal background with neon accents (e.g., purple/teal). Use CSS variables for theme + accent selection. Implement smooth transitions and micro-interactions (hover/press states, subtle skeleton loaders).",
          "Layout: mobile-first with bottom tab navigation (Home, Generate, Library, Settings). Persistent mini-player dock at bottom when a track exists; tapping opens Now Playing.",
          "Screens: Splash/Init, Home (quick actions + recent), Generate (prompt + advanced settings + generate), Library (search/sort/filter), Now Playing (full player), Track Details (metadata + actions), Settings (defaults + accent + playback), About/Help (explain simulation + privacy).",
          "Player: custom UI with play/pause, seek bar with current time/duration, next/prev through library queue, shuffle/repeat toggles (client-side logic), volume slider, and keyboard shortcuts (Space play/pause, arrows seek).",
          "Track actions: rename, delete (confirm), download (WAV blob), share (Web Share or copy link/text), view details (prompt/settings/createdAt).",
          "Accessibility: ARIA labels for controls, focus rings, sufficient contrast, large touch targets, semantic headings, keyboard navigation for main actions.",
          "Performance: keep dependencies light; prefer handcrafted CSS. Use code splitting for routes if appropriate. Avoid heavy UI kits."
        ],
        "backendInstructions": [
          "None. The app must be serverless and browser-only.",
          "Simulate 'Sign in with Google': store a mock user profile in localStorage; include a clear note that this is a demo/simulation and not real OAuth.",
          "Simulate 'Gemini music generation': generate audio locally using Web Audio API (OfflineAudioContext), producing a WAV Blob. The prompt and settings influence generation deterministically (e.g., hash prompt to pick scale/melody). Show a progress indicator to mimic AI generation latency."
        ],
        "modificationInstructions": [
          "Create a complete, buildable repository with all required files. Do not leave TODOs or stubs.",
          "Ensure the build output works when deployed to GitHub Pages under a repository subpath (use `base: './'` and hash routing).",
          "Persist library and preferences across reloads using localStorage + IndexedDB (audio blobs). Provide migration-safe storage keys.",
          "Include sample seed tracks on first run (generated locally once) OR provide a one-tap 'Create sample tracks' button in onboarding.",
          "Implement export/import of library metadata as JSON (and optionally include audio as downloadable per-track WAV). Import should merge safely and avoid ID collisions.",
          "Provide clear in-app messaging: 'Gemini/Google auth are simulated in this static demo; no network requests are made by default.'"
        ],
        "acceptanceCriteria": [
          "Runs fully offline after initial load; no backend required; no external API calls needed for core functionality.",
          "Builds with `npm install` + `npm run build` and previews with `npm run dev` without errors.",
          "GH Pages compatible: routes work on refresh thanks to hash routing; assets resolve correctly due to relative base path.",
          "Generate flow produces an actual playable audio track (WAV) stored locally and playable in the custom player.",
          "Library supports list/search, track details, rename, delete, download, and share with fallback behavior.",
          "Clean Architecture structure is present and respected (domain independent; use cases orchestrate; adapters isolate browser APIs).",
          "UI is dark-mode, polished, mobile-first, and accessible with ARIA labels and keyboard support."
        ],
        "codexPrompt": "You are Codex. Generate a complete replacement file set for a brand-new repository implementing the app described below. Output a full project with all files (include file paths and contents). Do NOT output patches; output the entire repository contents.\n\nProject: NoirTune AI\nType: Static Vite + React + TypeScript app (browser-only, serverless) deployable to GitHub Pages.\nRouting: Must work on GitHub Pages under repo subpath; use HashRouter and set Vite `base: './'`.\n\nCore concept:\n- Spotify-inspired dark UI (NOT identical), unique color palette (deep charcoal + neon purple/teal accents), mobile-first.\n- Purpose: generate music from a prompt via AI — but since this must be static/serverless, implement AI generation as a LOCAL SIMULATION using Web Audio API. Clearly disclose in UI that Google/Gemini and OAuth are simulated in this demo.\n- User library of generated tracks with custom playback: play/pause/seek/next/prev/shuffle/repeat/volume.\n- Track management: rename, delete, download WAV, share (Web Share API fallback to clipboard).\n- Data persistence: metadata in localStorage; audio blobs in IndexedDB (implement a small wrapper yourself; do not add heavy deps). Preferences in localStorage.\n\nArchitecture requirement (Uncle Bob / Clean Architecture):\n- Must have layers:\n  1) `src/domain/*` — Entities/value objects/types (no React, no browser APIs)\n  2) `src/application/*` — Use cases + ports (interfaces) + DTOs\n  3) `src/infrastructure/*` — Implementations using browser APIs (localStorage, IndexedDB, Web Audio, Web Share)\n  4) `src/app/*` — Composition root/DI container wiring implementations to use cases\n  5) `src/ui/*` — React components, pages, routes, styling\n- Domain must not import from application/ui/infrastructure.\n- UI must call use cases; do not call localStorage/IndexedDB/WebAudio directly from UI.\n\nFeatures/screens:\n1) Splash/Init: brief loader while repositories initialize, then route to Home.\n2) Home: quick actions (Generate), Recent tracks carousel/list, and visible mini-player if a track exists.\n3) Generate:\n   - Prompt textarea\n   - Advanced settings: duration seconds (slider), genre, mood, tempo, instruments, intensity (selects/sliders)\n   - Generate button triggers simulated AI generation with progress state.\n   - Generated track is saved to library and starts playing.\n4) Library:\n   - List of tracks (title, duration, createdAt, small artwork)\n   - Search by title/prompt\n   - Sort options (Newest/Oldest/Title)\n   - Tap opens Track Details; play button starts playback.\n5) Now Playing:\n   - Full player: artwork placeholder gradient, title, time, seek bar, play/pause, next/prev, shuffle, repeat, volume.\n   - Queue is the current sorted library list.\n6) Track Details:\n   - Show prompt + settings + createdAt\n   - Actions: Rename title, Download WAV, Share, Delete (confirm)\n7) Settings:\n   - Default duration\n   - Accent color selection (within dark mode)\n   - Playback defaults (e.g., autoplay on generate, default volume)\n   - Simulated Google sign-in section (Sign in/out)\n8) About/Help:\n   - Explain: this is a static demo; Google OAuth and Gemini are simulated; no network calls by default.\n   - Explain local storage, privacy, and limitations.\n\nSimulated Google auth:\n- Provide a \"Sign in with Google\" button that creates a mock profile (name, email, avatar color) saved in localStorage.\n- Provide sign out.\n- UI should clearly label this as \"Simulated\".\n- DO NOT implement real OAuth, do not request credentials.\n\nSimulated AI music generation:\n- Implement an `AudioGenerator` using OfflineAudioContext.\n- Generate a short musical clip based on prompt hash and settings:\n  - Map genre/mood to scale + wave type + filter\n  - Use tempo to place notes\n  - Use intensity to control gain/distortion-ish soft clipping\n  - Duration is the requested seconds (cap e.g. 5–60 sec)\n- Render to AudioBuffer then encode to WAV Blob (implement WAV encoding in TS).\n- Return a Blob and derived metadata (duration, waveform seed).\n\nStorage:\n- Track metadata stored in localStorage under a versioned key.\n- Audio blobs stored in IndexedDB keyed by trackId.\n- Provide use case to delete track which removes both metadata and blob.\n- Provide export/import metadata JSON (export downloads a json file; import via file input).\n\nPlayer:\n- Implement playback using HTMLAudioElement created from Blob URL (URL.createObjectURL).\n- Maintain player state in a React context/store (but keep core logic in application services if possible).\n- Seeking updates currentTime.\n- Handle end-of-track and repeat/shuffle.\n\nUI/Styling:\n- Use plain CSS (or CSS modules) with CSS variables for theme.\n- Mobile-first: bottom tab bar, sticky mini-player.\n- Smooth transitions and skeleton loaders.\n- Accessibility: proper aria-labels, focus states, keyboard shortcuts.\n\nBuild/deploy constraints:\n- Must be static and GitHub Pages compatible.\n- Use `HashRouter` and Vite `base: './'`.\n- No backend, no server calls, no secrets.\n\nImplementation details:\n- Provide `package.json` with scripts: dev/build/preview/lint (optional) and proper dependencies.\n- Provide `vite.config.ts`, `tsconfig.json`, `index.html`.\n- Use strict TypeScript.\n- Ensure all routes and components compile.\n\nDeliverables:\n- Output the complete file tree with contents.\n- No TODOs, no placeholders that break behavior.\n- Include a small set of seed tracks created on first run (generated locally) OR an onboarding action to generate them.\n\nRecommended file structure (you may refine but keep Clean Architecture):\n- src/domain/entities/Track.ts\n- src/domain/valueObjects/TrackId.ts\n- src/domain/types.ts\n- src/application/ports/*.ts\n- src/application/usecases/*.ts\n- src/infrastructure/storage/LocalStorage*.ts\n- src/infrastructure/storage/IndexedDb*.ts\n- src/infrastructure/audio/WebAudioGenerator.ts\n- src/infrastructure/share/WebShareService.ts\n- src/app/di/container.ts\n- src/ui/App.tsx\n- src/ui/routes.tsx\n- src/ui/components/*\n- src/ui/pages/*\n- src/ui/styles/*\n\nNow generate the entire repository."
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

Current stage: **Generating Codex prompt**

Complete: **no**

| Stage | State |
| --- | --- |
| Received user prompt | done |
| Generated product requirements | done |
| Created architecture plan | current |
| Generated project code | pending |
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
  "title": "NoirTune AI — Static Vite React + TypeScript (Clean Architecture) Spotify-like Dark UI Music Generator",
  "summary": "Build a production-ready, mobile-first, dark-mode, Spotify-inspired (but not identical) static web app that simulates AI music generation client-side, includes a library and custom playback, and runs fully in the browser (GitHub Pages compatible). Use Uncle Bob / Clean Architecture layering with domain/use-cases/adapters/UI separation. No real OAuth or Gemini calls—simulate sign-in and generation, store all data locally (localStorage + IndexedDB).",
  "architectureInstructions": [
    "Enforce Clean Architecture (Uncle Bob): separate `domain` (entities/value objects), `application` (use cases), `adapters` (interfaces + implementations), `ui` (React components/pages). Domain must not import React or browser APIs.",
    "Use dependency inversion: UI depends on use-case interfaces; concrete implementations live in `infrastructure` and are wired in a single composition root (e.g., `src/app/di/container.ts`).",
    "Define domain entities: `Track`, `TrackId`, `GenerationSettings`, `UserProfile`, `AppPreferences` with strong TypeScript types.",
    "Define repository/service interfaces in `application/ports`: `TrackRepository`, `AuthRepository`, `PreferencesRepository`, `AudioGenerator`, `ShareService`, `ClipboardService`.",
    "Implement adapters/infrastructure: localStorage for auth + preferences + metadata, IndexedDB for audio blobs, Web Audio API for generation, Web Share API + clipboard fallback for sharing.",
    "No backend, no secrets, no external private APIs, no serverless functions. Any 'Gemini' functionality must be clearly labeled as simulated in UI and implemented locally.",
    "Make the app resilient: handle missing Web Share API, handle Safari/iOS audio quirks, show friendly errors, provide empty states and first-run onboarding.",
    "Use HashRouter (or equivalent) to ensure GitHub Pages routing works under repository subpaths. Also set Vite base to relative (`base: './'`)."
  ],
  "frontendInstructions": [
    "Tech: Vite + React + TypeScript, static build only. Use React Router with hash routing for GH Pages compatibility.",
    "Design: dark-mode only with unique palette (not Spotify green). Use deep charcoal background with neon accents (e.g., purple/teal). Use CSS variables for theme + accent selection. Implement smooth transitions and micro-interactions (hover/press states, subtle skeleton loaders).",
    "Layout: mobile-first with bottom tab navigation (Home, Generate, Library, Settings). Persistent mini-player dock at bottom when a track exists; tapping opens Now Playing.",
    "Screens: Splash/Init, Home (quick actions + recent), Generate (prompt + advanced settings + generate), Library (search/sort/filter), Now Playing (full player), Track Details (metadata + actions), Settings (defaults + accent + playback), About/Help (explain simulation + privacy).",
    "Player: custom UI with play/pause, seek bar with current time/duration, next/prev through library queue, shuffle/repeat toggles (client-side logic), volume slider, and keyboard shortcuts (Space play/pause, arrows seek).",
    "Track actions: rename, delete (confirm), download (WAV blob), share (Web Share or copy link/text), view details (prompt/settings/createdAt).",
    "Accessibility: ARIA labels for controls, focus rings, sufficient contrast, large touch targets, semantic headings, keyboard navigation for main actions.",
    "Performance: keep dependencies light; prefer handcrafted CSS. Use code splitting for routes if appropriate. Avoid heavy UI kits."
  ],
  "backendInstructions": [
    "None. The app must be serverless and browser-only.",
    "Simulate 'Sign in with Google': store a mock user profile in localStorage; include a clear note that this is a demo/simulation and not real OAuth.",
    "Simulate 'Gemini music generation': generate audio locally using Web Audio API (OfflineAudioContext), producing a WAV Blob. The prompt and settings influence generation deterministically (e.g., hash prompt to pick scale/melody). Show a progress indicator to mimic AI generation latency."
  ],
  "modificationInstructions": [
    "Create a complete, buildable repository with all required files. Do not leave TODOs or stubs.",
    "Ensure the build output works when deployed to GitHub Pages under a repository subpath (use `base: './'` and hash routing).",
    "Persist library and preferences across reloads using localStorage + IndexedDB (audio blobs). Provide migration-safe storage keys.",
    "Include sample seed tracks on first run (generated locally once) OR provide a one-tap 'Create sample tracks' button in onboarding.",
    "Implement export/import of library metadata as JSON (and optionally include audio as downloadable per-track WAV). Import should merge safely and avoid ID collisions.",
    "Provide clear in-app messaging: 'Gemini/Google auth are simulated in this static demo; no network requests are made by default.'"
  ],
  "acceptanceCriteria": [
    "Runs fully offline after initial load; no backend required; no external API calls needed for core functionality.",
    "Builds with `npm install` + `npm run build` and previews with `npm run dev` without errors.",
    "GH Pages compatible: routes work on refresh thanks to hash routing; assets resolve correctly due to relative base path.",
    "Generate flow produces an actual playable audio track (WAV) stored locally and playable in the custom player.",
    "Library supports list/search, track details, rename, delete, download, and share with fallback behavior.",
    "Clean Architecture structure is present and respected (domain independent; use cases orchestrate; adapters isolate browser APIs).",
    "UI is dark-mode, polished, mobile-first, and accessible with ARIA labels and keyboard support."
  ],
  "codexPrompt": "You are Codex. Generate a complete replacement file set for a brand-new repository implementing the app described below. Output a full project with all files (include file paths and contents). Do NOT output patches; output the entire repository contents.\n\nProject: NoirTune AI\nType: Static Vite + React + TypeScript app (browser-only, serverless) deployable to GitHub Pages.\nRouting: Must work on GitHub Pages under repo subpath; use HashRouter and set Vite `base: './'`.\n\nCore concept:\n- Spotify-inspired dark UI (NOT identical), unique color palette (deep charcoal + neon purple/teal accents), mobile-first.\n- Purpose: generate music from a prompt via AI — but since this must be static/serverless, implement AI generation as a LOCAL SIMULATION using Web Audio API. Clearly disclose in UI that Google/Gemini and OAuth are simulated in this demo.\n- User library of generated tracks with custom playback: play/pause/seek/next/prev/shuffle/repeat/volume.\n- Track management: rename, delete, download WAV, share (Web Share API fallback to clipboard).\n- Data persistence: metadata in localStorage; audio blobs in IndexedDB (implement a small wrapper yourself; do not add heavy deps). Preferences in localStorage.\n\nArchitecture requirement (Uncle Bob / Clean Architecture):\n- Must have layers:\n  1) `src/domain/*` — Entities/value objects/types (no React, no browser APIs)\n  2) `src/application/*` — Use cases + ports (interfaces) + DTOs\n  3) `src/infrastructure/*` — Implementations using browser APIs (localStorage, IndexedDB, Web Audio, Web Share)\n  4) `src/app/*` — Composition root/DI container wiring implementations to use cases\n  5) `src/ui/*` — React components, pages, routes, styling\n- Domain must not import from application/ui/infrastructure.\n- UI must call use cases; do not call localStorage/IndexedDB/WebAudio directly from UI.\n\nFeatures/screens:\n1) Splash/Init: brief loader while repositories initialize, then route to Home.\n2) Home: quick actions (Generate), Recent tracks carousel/list, and visible mini-player if a track exists.\n3) Generate:\n   - Prompt textarea\n   - Advanced settings: duration seconds (slider), genre, mood, tempo, instruments, intensity (selects/sliders)\n   - Generate button triggers simulated AI generation with progress state.\n   - Generated track is saved to library and starts playing.\n4) Library:\n   - List of tracks (title, duration, createdAt, small artwork)\n   - Search by title/prompt\n   - Sort options (Newest/Oldest/Title)\n   - Tap opens Track Details; play button starts playback.\n5) Now Playing:\n   - Full player: artwork placeholder gradient, title, time, seek bar, play/pause, next/prev, shuffle, repeat, volume.\n   - Queue is the current sorted library list.\n6) Track Details:\n   - Show prompt + settings + createdAt\n   - Actions: Rename title, Download WAV, Share, Delete (confirm)\n7) Settings:\n   - Default duration\n   - Accent color selection (within dark mode)\n   - Playback defaults (e.g., autoplay on generate, default volume)\n   - Simulated Google sign-in section (Sign in/out)\n8) About/Help:\n   - Explain: this is a static demo; Google OAuth and Gemini are simulated; no network calls by default.\n   - Explain local storage, privacy, and limitations.\n\nSimulated Google auth:\n- Provide a \"Sign in with Google\" button that creates a mock profile (name, email, avatar color) saved in localStorage.\n- Provide sign out.\n- UI should clearly label this as \"Simulated\".\n- DO NOT implement real OAuth, do not request credentials.\n\nSimulated AI music generation:\n- Implement an `AudioGenerator` using OfflineAudioContext.\n- Generate a short musical clip based on prompt hash and settings:\n  - Map genre/mood to scale + wave type + filter\n  - Use tempo to place notes\n  - Use intensity to control gain/distortion-ish soft clipping\n  - Duration is the requested seconds (cap e.g. 5–60 sec)\n- Render to AudioBuffer then encode to WAV Blob (implement WAV encoding in TS).\n- Return a Blob and derived metadata (duration, waveform seed).\n\nStorage:\n- Track metadata stored in localStorage under a versioned key.\n- Audio blobs stored in IndexedDB keyed by trackId.\n- Provide use case to delete track which removes both metadata and blob.\n- Provide export/import metadata JSON (export downloads a json file; import via file input).\n\nPlayer:\n- Implement playback using HTMLAudioElement created from Blob URL (URL.createObjectURL).\n- Maintain player state in a React context/store (but keep core logic in application services if possible).\n- Seeking updates currentTime.\n- Handle end-of-track and repeat/shuffle.\n\nUI/Styling:\n- Use plain CSS (or CSS modules) with CSS variables for theme.\n- Mobile-first: bottom tab bar, sticky mini-player.\n- Smooth transitions and skeleton loaders.\n- Accessibility: proper aria-labels, focus states, keyboard shortcuts.\n\nBuild/deploy constraints:\n- Must be static and GitHub Pages compatible.\n- Use `HashRouter` and Vite `base: './'`.\n- No backend, no server calls, no secrets.\n\nImplementation details:\n- Provide `package.json` with scripts: dev/build/preview/lint (optional) and proper dependencies.\n- Provide `vite.config.ts`, `tsconfig.json`, `index.html`.\n- Use strict TypeScript.\n- Ensure all routes and components compile.\n\nDeliverables:\n- Output the complete file tree with contents.\n- No TODOs, no placeholders that break behavior.\n- Include a small set of seed tracks created on first run (generated locally) OR an onboarding action to generate them.\n\nRecommended file structure (you may refine but keep Clean Architecture):\n- src/domain/entities/Track.ts\n- src/domain/valueObjects/TrackId.ts\n- src/domain/types.ts\n- src/application/ports/*.ts\n- src/application/usecases/*.ts\n- src/infrastructure/storage/LocalStorage*.ts\n- src/infrastructure/storage/IndexedDb*.ts\n- src/infrastructure/audio/WebAudioGenerator.ts\n- src/infrastructure/share/WebShareService.ts\n- src/app/di/container.ts\n- src/ui/App.tsx\n- src/ui/routes.tsx\n- src/ui/components/*\n- src/ui/pages/*\n- src/ui/styles/*\n\nNow generate the entire repository."
}
~~~

## Action History

- 2026-05-27T11:03:13.038Z - Received user input (info)
- 2026-05-27T11:03:16.972Z - Processing user input (info)
- 2026-05-27T11:03:45.060Z - Generated structured product requirements (success)
- 2026-05-27T11:03:48.039Z - Creating architecture and implementation prompt (info)

## Latest Error

None.
