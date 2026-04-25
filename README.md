# VIDEO FORGE

VIDEO FORGE is a browser-based AI video storyboard generator. It helps you turn a simple concept into a structured video project with generated scenes, narration, and audio previews.

## What It Does

- Generates a shot list from a video idea.
- Creates one image per scene with gpt-image-2.
- Accepts up to 5 reference images to keep style consistency.
- Generates narration automatically or uses a manual script.
- Creates real TTS audio tracks with /v1/audio/speech.
- Shows a live 5-step workflow with progress and logs.
- Displays generated scenes in an interactive filmstrip preview.
- Lets you download generated images and audio files.

## Main Features

- Scenario tab: concept, duration, format, manual shots or auto shots.
- Reference Images tab: upload visual references, choose image style, size, and quality.
- Narration tab: auto narration, manual narration, or no narration.
- Rendering tab: pacing, transitions, music mood, subtitles mode, extra instructions.
- Result area: storyboard preview, script preview, audio tracks, downloads.

## API Flow

VIDEO FORGE uses these Lewisnote-compatible endpoints:

- https://build.lewisnote.com/v1/chat/completions`n+- https://build.lewisnote.com/v1/images/generations`n+- https://build.lewisnote.com/v1/audio/speech`n+
Models currently used:

- gpt-5.4-nano for scenario generation, narration, and reference analysis.
- gpt-image-2 for image generation.
- 	ts-1 for voice synthesis.

## Project Structure

- index.html: page structure.
- style.css: all styles.
- pp.js: application logic and API calls.

## How To Use

1. Open index.html in a browser.
2. Enter your API key in the top-right field.
3. Write your video concept.
4. Choose duration and format.
5. Add manual shots or enable automatic shot generation.
6. Optionally upload reference images.
7. Choose narration mode and voice.
8. Click GENERER LE PROJET IA.
9. Wait for the 5-step pipeline to finish.
10. Preview scenes, audio, and downloads in the result area.

## 5-Step Pipeline

1. Scenario generation.
2. Reference analysis and image generation.
3. Narration script creation.
4. TTS audio generation.
5. Storyboard assembly.

## Notes

- The app currently builds a complete interactive storyboard, not a final MP4 render.
- A real exported video would require an additional backend video assembly step.
- The API key is stored in browser local storage for convenience.
- No default secret key is hardcoded in the app.

## Recommended Usage

- Use strong, specific prompts for better visual results.
- Upload consistent character or environment references when you want continuity.
- Use manual narration when timing and wording need tighter control.
- Use auto narration for fast concept prototyping.

## Status

The frontend is ready as a local prototype and the configured API routes are valid and reachable.
