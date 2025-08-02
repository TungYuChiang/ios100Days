# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

WeSplit is an iOS application built with SwiftUI that helps users calculate bill splitting and tip calculations. It's part of a 100 Days of iOS development learning journey. The app allows users to enter a bill amount, select the number of people to split between, choose a tip percentage, and calculates both the total amount and amount per person.

## Architecture

- **SwiftUI App**: Modern declarative UI framework with iOS 18.5+ target
- **Single View Architecture**: Main functionality contained in `ContentView.swift`
- **App Entry Point**: `WeSplitApp.swift` serves as the main app entry point with @main
- **Bundle Identifier**: com.tungyu.WeSplit
- **State Management**: Uses `@State` and `@FocusState` property wrappers

## Key Components

- `ContentView.swift`: Main calculator view with Form-based UI containing:
  - TextField for bill amount input with currency formatting
  - Picker for number of people (2-99)
  - Picker for tip percentage (0-100%)
  - Computed properties for `totalPerPerson` and `totalAmount`
  - Conditional styling (red text for 0% tip)
- `WeSplitApp.swift`: App delegate and scene configuration

## Development Commands

**Build and Run:**
- Open in Xcode: `open WeSplit.xcodeproj`
- Build from Xcode: Cmd+B
- Run on simulator: Cmd+R

**Testing:**
- Run tests: Cmd+U in Xcode
- Test target uses Swift Testing framework (not XCTest)
- Unit tests: `WeSplitTests/WeSplitTests.swift`
- UI tests: `WeSplitUITests/WeSplitUITests.swift`

## Code Patterns

- **Form-based UI**: Uses SwiftUI Form with Sections for organized layout
- **NavigationStack**: Modern navigation container
- **Picker Styles**: Uses `.navigationLink` picker style for selections
- **Currency Formatting**: Uses `Locale.current.currency?.identifier ?? "USD"`
- **Keyboard Management**: `@FocusState` for decimal pad keyboard with Done button
- **Conditional Modifiers**: `.foregroundColor(tipPercentage == 0 ? .red : .primary)`

## Development Configuration

- **iOS Deployment Target**: 18.5
- **Swift Version**: 5.0
- **Device Support**: iPhone and iPad (Universal)
- **SwiftUI Previews**: Enabled for rapid UI development
- **Asset Generation**: Swift Asset Symbol Extensions enabled