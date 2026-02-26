# من يقودنا؟ - لعبة اجتماعية مصرية

## Overview
A fully offline Egyptian Arabic social deduction game "من يقودنا؟" (Who Leads Us?). Built with Expo React Native with stunning dark neon aesthetics.

## Architecture

### Frontend (Expo React Native)
- **Framework**: Expo SDK 54, Expo Router v6 (file-based routing)
- **Language**: TypeScript
- **Fonts**: Cairo (Arabic Google Font) - Regular, SemiBold, Bold, Black
- **State**: React Context (GameContext) + AsyncStorage for persistence
- **Animations**: react-native-reanimated
- **UI**: Custom components with LinearGradient and Ionicons

### Backend (Express)
- Minimal Express server (port 5000) serving static landing page
- No backend needed - game is 100% offline

## Game Features
- **6 Game Modes**: Classic, Horror, Sci-Fi, Social, Adventure, Political
- **12 Scenarios**: 2 per mode with unique storylines
- **4 Roles**: Guide (مرشد), Deceiver (مخادع), Member (عضو), Chaotic (فوضوي)
- **No-Guide Mode**: 15% chance per round (adds mystery)
- **Score System**: Points tracked per player
- **Badges**: 6 achievement badges
- **Statistics**: Persistent stats via AsyncStorage

## Screens
- `app/index.tsx` - Home screen with animated neon background
- `app/setup.tsx` - 3-step game setup (players → mode → scenario)
- `app/role-reveal.tsx` - Secret role reveal with card flip animation
- `app/discussion.tsx` - 2-minute countdown timer with tips
- `app/voting.tsx` - Per-player voting system
- `app/results.tsx` - Cinematic results reveal
- `app/how-to-play.tsx` - Egyptian Arabic instructions
- `app/settings.tsx` - Sound, tension level, theme color
- `app/stats.tsx` - Player rankings and badges

## Key Components
- `components/AnimatedBackground.tsx` - Animated neon orbs background
- `context/GameContext.tsx` - Full game state management
- `constants/gameData.ts` - All game modes, scenarios, roles, badges
- `constants/colors.ts` - Dark neon color palette

## Color Palette
- Background: #050510 (deep dark navy)
- Neon Blue: #00D4FF
- Neon Purple: #8B5CF6
- Neon Red: #FF2D55
- Neon Green: #39FF14
- Gold: #FFD700

## Routing
All navigation is via expo-router Stack with no tab bar.
The (tabs) directory exists but is gutted to avoid conflicts.

## Design
- RTL Arabic text (Cairo font)
- Dark neon aesthetic (purple/blue/red/green glow effects)
- Animated backgrounds with floating orbs
- Card flip animations for role reveal
- Haptic feedback on all interactions
- Cinematic results screen
