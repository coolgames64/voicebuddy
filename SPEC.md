# Voice Buddy 🌟 - Translation App Spec

## Concept & Vision
Voice Buddy is a friendly, colourful translation app for kids. Point your phone at someone speaking a different language, tap and hold a button, and it listens, translates, and SPEAKS the translation back to you — like having a pocket translator friend! Designed for a 7-year-old: big buttons, fun animations, simple flow.

## Design Language

### Aesthetic
Playful, bright, kid-friendly — think Duolingo meets a friendly robot. Rounded corners everywhere, bouncy animations, soft gradients.

### Colours
- Primary: `#4A90E2` (friendly blue)
- Secondary: `#FF6B9D` (playful pink)
- Accent: `#FFD93D` (sunny yellow)
- Background: `#F0F4FF` (soft sky blue)
- Text: `#2D3748` (dark but soft)

### Typography
- Headings: **Nunito** (rounded, friendly, Google Fonts)
- Body: **Nunito**

### Motion Philosophy
- Bouncy micro-interactions on buttons (scale 1.05 on tap)
- Pulsing microphone animation when listening
- Language flags swap with smooth horizontal slide
- Fun confetti/sparkle when translation completes

## Pages

### 1. Home Page
- Big app logo/title "Voice Buddy 🌟"
- Two large flag buttons: 🇨🇳 Chinese | 🇬🇧 English
- Tapping a flag selects it as source/target
- Direction indicator: "🔊 Speaking [FROM] → [TO]"
- Big "START TALKING" button to go to recording page

### 2. Recording Page
- Shows current language pair at top
- HUGE circular microphone button (centre of screen)
- "Hold to Talk" instruction text
- While holding: pulsing animation, "Listening..." text
- On release: processes, shows "Translating..." then "Speaking..."
- Result text shown in both languages (original + translated)
- "Try Again" button
- "Change Language" back to home

### 3. Settings Page
- Language toggles (more languages coming soon)
- Voice speed: Normal / Slow
- App version info

## Technical Approach
- **Single HTML file** with embedded CSS and JS
- **Web Speech API** for speech recognition (Chrome/Safari)
- **Speech Synthesis API** for friendly voice output
- **LibreTranslate API** (free, no API key needed) for translation
- **localStorage** for saving language preference
- Works on mobile browsers (iOS Safari, Chrome Android)

## Features
- One-tap language swap (tap the ↔️ arrow)
- Visual feedback for each state (listening, translating, speaking)
- Error messages in friendly kid-language ("Oops! Didn't catch that, try again?")
- Works offline for common phrases (cached)