# SwiftUI Components Library

A personal collection of reusable **SwiftUI UI experiments and interface components**. It explores small, isolated views and interaction patterns in a single Xcode project.

> **Status:** Learning / reference project. The repository is a SwiftUI example app, not a published Swift Package or a drop-in production design system.

## What's inside

Browse `SwiftUIComponents/Components/` for examples organized by type:

- Buttons, text fields, pickers and tab bar elements
- Cards, decorative components, backgrounds and animations
- Activity indicator and ring-style UI
- Additional examples in `Shapes/`, `Extensions/`, `Test/` and `LoadingTest/`

Explore the actual implementation and previews before copying a component into another project; there is no compatibility or API stability guarantee.

## Getting started

1. Open `SwiftUIComponents.xcodeproj` in Xcode on macOS.
2. Choose a suitable simulator or device supported by the Xcode project settings.
3. Build and run the example app, or inspect individual views with Xcode previews.
4. Adapt the chosen component to your app and review any assets, custom fonts or dependencies it needs.

SwiftUI/iOS builds and simulator debugging require a compatible macOS/Xcode environment; a Windows machine alone cannot run the native Xcode toolchain.

## Structure

```text
SwiftUIComponents/
  Components/
    Animations/
    Backgrounds/
    Buttons/
    Cards/
    Decors/
    Pickers/
    Tabbar/
    TextFields/
  Extensions/
  Fonts/
  Shapes/
  Assets.xcassets/
  ContentView.swift
  SwiftUIComponentsApp.swift
```

## Notes

This repository does not currently declare a reuse license. Unless a license is later added, do not assume the source can be redistributed as an open-source component package.

Components may be learning exercises or adaptations; credit and rights for any external material should be verified before reuse.
