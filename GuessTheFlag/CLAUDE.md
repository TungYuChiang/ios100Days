# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a SwiftUI iOS app called "GuessTheFlag" - a flag guessing game where users identify country flags. It's part of a 100 Days of iOS development learning journey.

## Architecture

- **SwiftUI App**: Modern declarative UI framework
- **Single View Architecture**: Main game logic contained in `ContentView.swift`
- **App Entry Point**: `GuessTheFlagApp.swift` serves as the main app entry point
- **Asset Management**: Country flag images stored in `Assets.xcassets` with @1x, @2x, @3x variants

## Key Components

- `ContentView.swift`: Main game view containing flag selection logic, scoring, and UI
- `GuessTheFlagApp.swift`: App delegate and scene configuration
- Flag assets for 11 countries in various resolutions

## Development Commands

**Build and Run:**
- Open in Xcode: `open GuessTheFlag.xcodeproj`
- Build from Xcode: Cmd+B
- Run on simulator: Cmd+R

**Testing:**
- Run tests: Cmd+U in Xcode
- Test target uses Swift Testing framework (not XCTest)
- Unit tests: `GuessTheFlagTests.swift`
- UI tests: `GuessTheFlagUITests.swift`

## Code Style

- SwiftUI declarative syntax
- State management using `@State` property wrappers
- Functional approach for game logic (`askQuestion()`, `flagTapped()`)
- Modern Swift features (trailing closures, implicit returns)