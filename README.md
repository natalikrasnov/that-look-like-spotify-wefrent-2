# deployRocket Project Dossier

This branch is managed by deployRocket. It intentionally stores only this dossier README as machine-readable and human-readable project memory.

Generated application files are committed to the repository default branch after Codex returns a valid file set. If the default branch only has an initial README, code generation has not succeeded yet.

## Agent State

~~~deployrocket-state-json
{
  "id": "bmF0YWxpa3Jhc25vdi90aGF0LWxvb2stbGlrZS1zcG90aWZ5LXdlZnJlbnQtMg",
  "name": "NoirTune AI",
  "summary": "A mobile-first, dark-mode, Spotify-inspired web app that lets users generate AI-style music from prompts, manage a personal library of created tracks, and play, delete, download, or share them—all running fully client-side as a static site.",
  "status": "PROCESSING_INPUT",
  "currentStep": "Processing input",
  "githubRepoUrl": "https://github.com/natalikrasnov/that-look-like-spotify-wefrent-2",
  "githubOwner": "natalikrasnov",
  "githubRepo": "that-look-like-spotify-wefrent-2",
  "githubUserLogin": "natalikrasnov",
  "githubDefaultBranch": "main",
  "error": null,
  "createdAt": "2026-05-27T11:03:13.038Z",
  "updatedAt": "2026-05-27T11:03:43.469Z",
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

Current stage: **Processing input**

Complete: **no**

| Stage | State |
| --- | --- |
| Received user prompt | done |
| Generated product requirements | current |
| Created architecture plan | pending |
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

Codex prompt plan is pending.

## Action History

- 2026-05-27T11:03:13.038Z - Received user input (info)
- 2026-05-27T11:03:16.972Z - Processing user input (info)

## Latest Error

None.
