# deployRocket Project Dossier

This branch is managed by deployRocket. It intentionally stores only this dossier README as machine-readable and human-readable project memory.

Generated application files are committed to the repository default branch after Codex returns a valid file set. If the default branch only has an initial README, code generation has not succeeded yet.

## Agent State

~~~deployrocket-state-json
{
  "id": "bmF0YWxpa3Jhc25vdi90aGF0LWxvb2stbGlrZS1zcG90aWZ5LXdlZnJlbnQtMg",
  "name": "NoirTune AI",
  "summary": "A mobile-first, dark-mode, Spotify-inspired web app that lets users generate AI-style music from prompts, manage a personal library of created tracks, and play, delete, download, or share them—all running fully client-side as a static site.",
  "status": "SENDING_TO_CODEX",
  "currentStep": "Submitting prompt to Codex",
  "githubRepoUrl": "https://github.com/natalikrasnov/that-look-like-spotify-wefrent-2",
  "githubOwner": "natalikrasnov",
  "githubRepo": "that-look-like-spotify-wefrent-2",
  "githubUserLogin": "natalikrasnov",
  "githubDefaultBranch": "main",
  "error": null,
  "createdAt": "2026-05-27T11:03:13.038Z",
  "updatedAt": "2026-05-27T11:04:55.481Z",
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
        "title": "NoirTune AI — Static Spotify-like Dark Music Generator (Client-only) with Clean Architecture",
        "summary": "Build a production-oriented, mobile-first, dark-mode, Spotify-inspired (but visually distinct) static web app that simulates AI music generation in the browser, stores generated tracks locally, and provides a custom playback experience with library management, download, and share. Must be Vite + React + TypeScript, GitHub Pages compatible, and organized using Uncle Bob / Clean Architecture (domain/use-cases/adapters/UI).",
        "architectureInstructions": [
          "Use Vite + React + TypeScript only (static build). No backend, no server functions, no databases, no external private APIs.",
          "Enforce Clean Architecture (Uncle Bob): domain entities/value objects in a framework-agnostic layer; use cases orchestrate; adapters implement storage/audio/share/auth; UI only depends on use cases via interfaces.",
          "Organize folders similar to: src/domain, src/application (use-cases), src/adapters (storage/audio/share/auth), src/ui (components/pages/router), src/shared (utils).",
          "All persistence must be client-side: localStorage for small config + metadata; IndexedDB for audio blobs (WAV). Provide robust fallback if IndexedDB unavailable (store only metadata and regenerate audio on-demand).",
          "Implement simulated Google sign-in (mock) stored in localStorage. App must clearly state in UI (About/Help + Auth screen) that it is simulated because this is a static-only app and cannot securely handle real OAuth or Gemini credentials.",
          "Implement 'AI music generation' as deterministic procedural generation via Web Audio API (OfflineAudioContext) based on prompt + settings (seeded RNG). Produce a WAV Blob for download/playback and store it locally.",
          "No TODOs/placeholders. Everything must build and run."
        ],
        "frontendInstructions": [
          "Mobile-first UI, dark mode only, Spotify-like layout patterns (bottom tab navigation, cards, prominent player) but with a unique color palette (e.g., charcoal + neon purple/teal).",
          "Use HashRouter for GitHub Pages compatibility (no server rewrite). Ensure asset base works for subpath deploy by setting Vite base to './'.",
          "Screens: Splash/Loading (brief init), Home, Generate, Library (search/sort), Now Playing, Track Details, Settings, About/Help, and a simple Auth/Account panel.",
          "Interactive UI: skeleton loaders for generation/list loading, smooth transitions (CSS), micro-interactions (button press states), accessible controls (ARIA labels, keyboard support).",
          "Playback: custom player with play/pause, seek, time display, next/previous in queue (library order), volume, repeat, shuffle.",
          "Track management: delete, rename title, view details (prompt + settings + createdAt), download (WAV + JSON metadata), share (Web Share API when available, else copy-to-clipboard).",
          "On first run: show onboarding hints and optionally seed a couple of sample tracks (generated locally) OR offer a one-tap 'Generate sample tracks' action."
        ],
        "backendInstructions": [
          "None. Must remain fully browser-only. Do not include server code, API calls to Gemini, Google OAuth flows, or any secrets.",
          "Simulate auth and AI generation locally; disclose limitations clearly in the app."
        ],
        "modificationInstructions": [
          "Create mode: Codex must output a COMPLETE REPLACEMENT FILE SET for a new repository.",
          "Include all necessary config files: package.json, vite.config.ts, tsconfig.json, index.html, src entry, CSS, and any minimal utilities.",
          "Avoid heavy dependencies. Prefer small/zero deps. If using a tiny helper for IndexedDB, implement it yourself rather than adding a library."
        ],
        "acceptanceCriteria": [
          "Runs with: npm install && npm run dev; builds with: npm run build; output works as static files on GitHub Pages.",
          "Uses HashRouter and Vite base './' (or otherwise demonstrably supports repo subpath deployments).",
          "All features implemented: generate track from prompt+settings (procedural), local library persistence, full player, delete/rename/details, download/share, settings, about/help, simulated google auth.",
          "Clean Architecture separation: domain has no React imports; use cases depend on interfaces; adapters implement browser APIs; UI layer uses use cases.",
          "No external API keys, no secret prompts, no network calls required.",
          "Accessible: ARIA labels for player buttons, keyboard interaction for key controls, good contrast in dark UI."
        ],
        "codexPrompt": "You are Codex. Generate a complete replacement file set for a new repo implementing the following app.\n\nAPP: NoirTune AI\nA mobile-first, dark-mode-only, Spotify-inspired (but visually distinct) music generation + playback web app. It must be a static Vite React TypeScript SPA that works on GitHub Pages with repository subpath deployments.\n\nCRITICAL CONSTRAINTS\n- Static-only, browser-only: no backend, no serverless functions, no DB, no private APIs.\n- Do NOT implement real Google OAuth or real Gemini API calls. This cannot be secured in a static app.\n- Instead, implement:\n  1) Simulated “Sign in with Google” UI that stores a mock profile in localStorage.\n  2) Simulated “Gemini AI music generation” done locally using Web Audio API (OfflineAudioContext) to procedurally generate music from prompt + settings.\n- The UI must clearly disclose this simulation (About/Help + Auth screen text).\n\nTECH STACK\n- Vite + React + TypeScript.\n- HashRouter for routing.\n- Vite base set to './' to support GitHub Pages subpath deployments.\n- Minimal dependencies.\n\nCLEAN ARCHITECTURE (UNCLE BOB)\nEnforce separation:\n1) Domain layer (no React):\n   - Entities: Track, UserProfile, GenerationSettings.\n   - Value objects: TrackId, DurationSeconds, etc (keep practical).\n   - Domain types/guards.\n2) Application layer (use cases):\n   - GenerateTrackUseCase\n   - ListTracksUseCase\n   - GetTrackUseCase\n   - DeleteTrackUseCase\n   - RenameTrackUseCase\n   - ExportLibraryUseCase\n   - ImportLibraryUseCase\n   - UpdateSettingsUseCase / GetSettingsUseCase\n   - Auth: SignInMockUseCase / SignOutUseCase / GetCurrentUserUseCase\n3) Adapters:\n   - TrackRepository: metadata in localStorage + audio blobs in IndexedDB (WAV). Provide fallback if IDB unavailable.\n   - AudioGenerator: procedural audio generation producing AudioBuffer and WAV Blob; seeded RNG from prompt+settings for reproducibility.\n   - PlayerController: wraps HTMLAudioElement for playback of Blob URLs; exposes play/pause/seek/volume, repeat/shuffle, queue navigation.\n   - ShareService: Web Share API when available; fallback to copy-to-clipboard.\n   - DownloadService: triggers downloads for WAV + JSON.\n4) UI layer:\n   - Pages + components. UI calls use cases via thin hooks/controllers.\n\nFEATURES / SCREENS\n- Splash/Loading: quick init while loading library/settings.\n- Home: quick actions (Generate), recent tracks list, continue playing.\n- Generate:\n  - Prompt textarea.\n  - Advanced settings controls: duration (seconds), genre, mood, tempo, instruments, intensity (sliders/selects).\n  - Generate button with progress simulation and skeleton.\n  - After generation: auto-add to library, navigate to Now Playing.\n- Library:\n  - List all tracks stored locally.\n  - Search by title/prompt, sort (newest/oldest/name/duration).\n  - Tap track to open Now Playing.\n- Now Playing:\n  - Artwork placeholder (generated gradient based on seed).\n  - Play/pause, next/prev, seek bar, current time/remaining, volume.\n  - Repeat toggle and shuffle toggle.\n  - Queue preview.\n- Track Details:\n  - Title (editable), createdAt, duration.\n  - Show prompt + settings.\n  - Actions: download WAV, download JSON metadata, share, delete.\n- Settings:\n  - Default duration.\n  - Playback defaults (e.g., auto-play on open, default volume).\n  - Theme accent selection within dark palette.\n  - Export library JSON + Import library JSON (file input). Import should merge tracks and store audio blobs when present (if exported with audio) or regenerate if only metadata.\n- About/Help:\n  - Explain limitations: simulated Google sign-in and simulated Gemini generation because app is static.\n  - Short privacy note: everything stored locally.\n- Auth/Account:\n  - “Sign in with Google” button that just creates a mock user (name, email, avatar color) and stores it.\n  - Show signed-in state + sign out.\n\nAUDIO GENERATION\n- Procedurally generate a short musical loop/track using OfflineAudioContext.\n- Use prompt+settings to derive:\n  - Seeded RNG.\n  - Scale selection, tempo, instrument (oscillator type), filter, envelope.\n- Render to AudioBuffer for the full duration.\n- Encode to WAV (PCM 16-bit) in-browser.\n- Store WAV Blob in IndexedDB with a key referenced by Track metadata.\n\nPERSISTENCE\n- localStorage:\n  - user profile mock\n  - app settings\n  - track metadata list (id, title, prompt, settings, createdAt, duration, audioBlobKey)\n- IndexedDB:\n  - audio blobs keyed by audioBlobKey\n- Provide migration/versioning for stored schema.\n\nUX / DESIGN\n- Dark mode only; unique palette (not Spotify green). Use CSS variables for theme accents.\n- Mobile-first: bottom tab bar for Home / Generate / Library / Settings.\n- Persistent mini-player bar at bottom when something is loaded; tap opens Now Playing.\n- Smooth transitions and subtle skeleton loading.\n- Large touch targets.\n\nACCESSIBILITY\n- ARIA labels for all player controls.\n- Keyboard support: space toggles play/pause on Now Playing when focused; sliders accessible.\n- Contrast-safe typography.\n\nGITHUB PAGES\n- Use HashRouter.\n- Vite base './'.\n- Ensure all links and asset paths work when deployed under /<repo>/.\n\nDELIVERABLE\nOutput the complete repository file tree with file contents. No placeholders, no TODOs.\nInclude at minimum:\n- package.json with scripts dev/build/preview\n- vite.config.ts\n- tsconfig.json\n- index.html\n- src/main.tsx, src/App.tsx\n- Full src/ structure implementing Clean Architecture\n- CSS/theme files\n- README.md explaining:\n  - how to run\n  - GitHub Pages notes\n  - that Google auth and Gemini are simulated locally\n\nWhen implementing, prioritize correctness, buildability, and polish. Keep dependencies minimal and code well-typed with TypeScript.\n"
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

Current stage: **Submitting prompt to Codex**

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
  "title": "NoirTune AI — Static Spotify-like Dark Music Generator (Client-only) with Clean Architecture",
  "summary": "Build a production-oriented, mobile-first, dark-mode, Spotify-inspired (but visually distinct) static web app that simulates AI music generation in the browser, stores generated tracks locally, and provides a custom playback experience with library management, download, and share. Must be Vite + React + TypeScript, GitHub Pages compatible, and organized using Uncle Bob / Clean Architecture (domain/use-cases/adapters/UI).",
  "architectureInstructions": [
    "Use Vite + React + TypeScript only (static build). No backend, no server functions, no databases, no external private APIs.",
    "Enforce Clean Architecture (Uncle Bob): domain entities/value objects in a framework-agnostic layer; use cases orchestrate; adapters implement storage/audio/share/auth; UI only depends on use cases via interfaces.",
    "Organize folders similar to: src/domain, src/application (use-cases), src/adapters (storage/audio/share/auth), src/ui (components/pages/router), src/shared (utils).",
    "All persistence must be client-side: localStorage for small config + metadata; IndexedDB for audio blobs (WAV). Provide robust fallback if IndexedDB unavailable (store only metadata and regenerate audio on-demand).",
    "Implement simulated Google sign-in (mock) stored in localStorage. App must clearly state in UI (About/Help + Auth screen) that it is simulated because this is a static-only app and cannot securely handle real OAuth or Gemini credentials.",
    "Implement 'AI music generation' as deterministic procedural generation via Web Audio API (OfflineAudioContext) based on prompt + settings (seeded RNG). Produce a WAV Blob for download/playback and store it locally.",
    "No TODOs/placeholders. Everything must build and run."
  ],
  "frontendInstructions": [
    "Mobile-first UI, dark mode only, Spotify-like layout patterns (bottom tab navigation, cards, prominent player) but with a unique color palette (e.g., charcoal + neon purple/teal).",
    "Use HashRouter for GitHub Pages compatibility (no server rewrite). Ensure asset base works for subpath deploy by setting Vite base to './'.",
    "Screens: Splash/Loading (brief init), Home, Generate, Library (search/sort), Now Playing, Track Details, Settings, About/Help, and a simple Auth/Account panel.",
    "Interactive UI: skeleton loaders for generation/list loading, smooth transitions (CSS), micro-interactions (button press states), accessible controls (ARIA labels, keyboard support).",
    "Playback: custom player with play/pause, seek, time display, next/previous in queue (library order), volume, repeat, shuffle.",
    "Track management: delete, rename title, view details (prompt + settings + createdAt), download (WAV + JSON metadata), share (Web Share API when available, else copy-to-clipboard).",
    "On first run: show onboarding hints and optionally seed a couple of sample tracks (generated locally) OR offer a one-tap 'Generate sample tracks' action."
  ],
  "backendInstructions": [
    "None. Must remain fully browser-only. Do not include server code, API calls to Gemini, Google OAuth flows, or any secrets.",
    "Simulate auth and AI generation locally; disclose limitations clearly in the app."
  ],
  "modificationInstructions": [
    "Create mode: Codex must output a COMPLETE REPLACEMENT FILE SET for a new repository.",
    "Include all necessary config files: package.json, vite.config.ts, tsconfig.json, index.html, src entry, CSS, and any minimal utilities.",
    "Avoid heavy dependencies. Prefer small/zero deps. If using a tiny helper for IndexedDB, implement it yourself rather than adding a library."
  ],
  "acceptanceCriteria": [
    "Runs with: npm install && npm run dev; builds with: npm run build; output works as static files on GitHub Pages.",
    "Uses HashRouter and Vite base './' (or otherwise demonstrably supports repo subpath deployments).",
    "All features implemented: generate track from prompt+settings (procedural), local library persistence, full player, delete/rename/details, download/share, settings, about/help, simulated google auth.",
    "Clean Architecture separation: domain has no React imports; use cases depend on interfaces; adapters implement browser APIs; UI layer uses use cases.",
    "No external API keys, no secret prompts, no network calls required.",
    "Accessible: ARIA labels for player buttons, keyboard interaction for key controls, good contrast in dark UI."
  ],
  "codexPrompt": "You are Codex. Generate a complete replacement file set for a new repo implementing the following app.\n\nAPP: NoirTune AI\nA mobile-first, dark-mode-only, Spotify-inspired (but visually distinct) music generation + playback web app. It must be a static Vite React TypeScript SPA that works on GitHub Pages with repository subpath deployments.\n\nCRITICAL CONSTRAINTS\n- Static-only, browser-only: no backend, no serverless functions, no DB, no private APIs.\n- Do NOT implement real Google OAuth or real Gemini API calls. This cannot be secured in a static app.\n- Instead, implement:\n  1) Simulated “Sign in with Google” UI that stores a mock profile in localStorage.\n  2) Simulated “Gemini AI music generation” done locally using Web Audio API (OfflineAudioContext) to procedurally generate music from prompt + settings.\n- The UI must clearly disclose this simulation (About/Help + Auth screen text).\n\nTECH STACK\n- Vite + React + TypeScript.\n- HashRouter for routing.\n- Vite base set to './' to support GitHub Pages subpath deployments.\n- Minimal dependencies.\n\nCLEAN ARCHITECTURE (UNCLE BOB)\nEnforce separation:\n1) Domain layer (no React):\n   - Entities: Track, UserProfile, GenerationSettings.\n   - Value objects: TrackId, DurationSeconds, etc (keep practical).\n   - Domain types/guards.\n2) Application layer (use cases):\n   - GenerateTrackUseCase\n   - ListTracksUseCase\n   - GetTrackUseCase\n   - DeleteTrackUseCase\n   - RenameTrackUseCase\n   - ExportLibraryUseCase\n   - ImportLibraryUseCase\n   - UpdateSettingsUseCase / GetSettingsUseCase\n   - Auth: SignInMockUseCase / SignOutUseCase / GetCurrentUserUseCase\n3) Adapters:\n   - TrackRepository: metadata in localStorage + audio blobs in IndexedDB (WAV). Provide fallback if IDB unavailable.\n   - AudioGenerator: procedural audio generation producing AudioBuffer and WAV Blob; seeded RNG from prompt+settings for reproducibility.\n   - PlayerController: wraps HTMLAudioElement for playback of Blob URLs; exposes play/pause/seek/volume, repeat/shuffle, queue navigation.\n   - ShareService: Web Share API when available; fallback to copy-to-clipboard.\n   - DownloadService: triggers downloads for WAV + JSON.\n4) UI layer:\n   - Pages + components. UI calls use cases via thin hooks/controllers.\n\nFEATURES / SCREENS\n- Splash/Loading: quick init while loading library/settings.\n- Home: quick actions (Generate), recent tracks list, continue playing.\n- Generate:\n  - Prompt textarea.\n  - Advanced settings controls: duration (seconds), genre, mood, tempo, instruments, intensity (sliders/selects).\n  - Generate button with progress simulation and skeleton.\n  - After generation: auto-add to library, navigate to Now Playing.\n- Library:\n  - List all tracks stored locally.\n  - Search by title/prompt, sort (newest/oldest/name/duration).\n  - Tap track to open Now Playing.\n- Now Playing:\n  - Artwork placeholder (generated gradient based on seed).\n  - Play/pause, next/prev, seek bar, current time/remaining, volume.\n  - Repeat toggle and shuffle toggle.\n  - Queue preview.\n- Track Details:\n  - Title (editable), createdAt, duration.\n  - Show prompt + settings.\n  - Actions: download WAV, download JSON metadata, share, delete.\n- Settings:\n  - Default duration.\n  - Playback defaults (e.g., auto-play on open, default volume).\n  - Theme accent selection within dark palette.\n  - Export library JSON + Import library JSON (file input). Import should merge tracks and store audio blobs when present (if exported with audio) or regenerate if only metadata.\n- About/Help:\n  - Explain limitations: simulated Google sign-in and simulated Gemini generation because app is static.\n  - Short privacy note: everything stored locally.\n- Auth/Account:\n  - “Sign in with Google” button that just creates a mock user (name, email, avatar color) and stores it.\n  - Show signed-in state + sign out.\n\nAUDIO GENERATION\n- Procedurally generate a short musical loop/track using OfflineAudioContext.\n- Use prompt+settings to derive:\n  - Seeded RNG.\n  - Scale selection, tempo, instrument (oscillator type), filter, envelope.\n- Render to AudioBuffer for the full duration.\n- Encode to WAV (PCM 16-bit) in-browser.\n- Store WAV Blob in IndexedDB with a key referenced by Track metadata.\n\nPERSISTENCE\n- localStorage:\n  - user profile mock\n  - app settings\n  - track metadata list (id, title, prompt, settings, createdAt, duration, audioBlobKey)\n- IndexedDB:\n  - audio blobs keyed by audioBlobKey\n- Provide migration/versioning for stored schema.\n\nUX / DESIGN\n- Dark mode only; unique palette (not Spotify green). Use CSS variables for theme accents.\n- Mobile-first: bottom tab bar for Home / Generate / Library / Settings.\n- Persistent mini-player bar at bottom when something is loaded; tap opens Now Playing.\n- Smooth transitions and subtle skeleton loading.\n- Large touch targets.\n\nACCESSIBILITY\n- ARIA labels for all player controls.\n- Keyboard support: space toggles play/pause on Now Playing when focused; sliders accessible.\n- Contrast-safe typography.\n\nGITHUB PAGES\n- Use HashRouter.\n- Vite base './'.\n- Ensure all links and asset paths work when deployed under /<repo>/.\n\nDELIVERABLE\nOutput the complete repository file tree with file contents. No placeholders, no TODOs.\nInclude at minimum:\n- package.json with scripts dev/build/preview\n- vite.config.ts\n- tsconfig.json\n- index.html\n- src/main.tsx, src/App.tsx\n- Full src/ structure implementing Clean Architecture\n- CSS/theme files\n- README.md explaining:\n  - how to run\n  - GitHub Pages notes\n  - that Google auth and Gemini are simulated locally\n\nWhen implementing, prioritize correctness, buildability, and polish. Keep dependencies minimal and code well-typed with TypeScript.\n"
}
~~~

## Action History

- 2026-05-27T11:03:13.038Z - Received user input (info)
- 2026-05-27T11:03:16.972Z - Processing user input (info)
- 2026-05-27T11:03:45.060Z - Generated structured product requirements (success)
- 2026-05-27T11:03:48.039Z - Creating architecture and implementation prompt (info)
- 2026-05-27T11:04:53.779Z - Generated structured Codex prompt (success)
- 2026-05-27T11:04:55.481Z - Sent prompt to Codex (info)

## Latest Error

None.
