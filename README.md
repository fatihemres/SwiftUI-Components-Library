# SwiftUI Components Library

A collection of **SwiftUI component studies, animation experiments and UI patterns** built in a single iOS example app. The focus is on learning how individual views are constructed, styled and composed rather than distributing a ready-to-use component package.

> **Project status:** Personal learning/portfolio project. This is an **Xcode iOS app**, not a Swift Package, an API-stable component library or a production design system. Individual demos may use fixed dimensions, bundled assets and illustrative text.

## Explore the components

| Area | Examples in the repository | What they demonstrate |
| --- | --- | --- |
| **Buttons and menus** | [GradientButton](SwiftUIComponents/Components/Buttons/GradientButtonStyle+Preview.swift), [MenuButton](SwiftUIComponents/Components/Buttons/MenuButton.swift), [NamedButton](SwiftUIComponents/Components/Buttons/NamedButton.swift), [LongRectangleMenuButton](SwiftUIComponents/Components/Buttons/LongRectangleMenuButton.swift) | Custom button styling, gradients and image/text menu tiles |
| **Cards** | [CustomCard](SwiftUIComponents/Components/Cards/CustomCard.swift) | Layered background shapes, typography and card composition |
| **Text input** | [CustomTextField1](SwiftUIComponents/Components/TextFields/CustomTextField1.swift), [PlaceholderModifier](SwiftUIComponents/Components/TextFields/PlaceholderModifier.swift) | TextField styling and a custom placeholder modifier |
| **Pickers** | [PricePicker](SwiftUIComponents/Components/Pickers/PricePicker.swift) | A two-handle price-range interaction prototype |
| **Navigation UI** | [Tabbar1](SwiftUIComponents/Components/Tabbar/Tabbar1.swift), [AppCoordinator example](SwiftUIComponents/Test/AppCoordinator.swift) | Custom tab-bar appearance and NavigationStack routing |
| **Loading / animation** | [ActivityIndicator](SwiftUIComponents/Components/ActivityIndicator.swift), [Ring](SwiftUIComponents/Components/Ring.swift), [Spiral](SwiftUIComponents/Components/Backgrounds/Spiral.swift) | Animating shapes, Canvas and TimelineView rendering |
| **Decorative geometry** | [CustomCircle](SwiftUIComponents/Components/Decors/CustomCircle.swift), [Triangle](SwiftUIComponents/Shapes/Triangle.swift) | Small reusable decorative elements |

See [`SwiftUIComponents/Components/`](SwiftUIComponents/Components) for additional experiments. Some files are works in progress; the presence of a file or preview does not imply a polished reusable API.

## What launches when you run the app?

The entry point is [`SwiftUIComponentsApp.swift`](SwiftUIComponents/SwiftUIComponentsApp.swift). It currently launches **`LoadingTestView`**, which links to **`DataFetchView`**. The latter uses a **two-second local simulated delay** before displaying four sample strings; it does **not** fetch data from a network service.

The older combined interface experiment is in [`ContentView.swift`](SwiftUIComponents/ContentView.swift), and many components have their own `#Preview` blocks or `PreviewProvider` examples. To inspect them, open the appropriate Swift file in Xcode and use its preview. The app's launch screen is not a navigable catalog of every component.

## Tools and implementation

- **Swift 5 / SwiftUI**, with `IPHONEOS_DEPLOYMENT_TARGET = 17.4` in the checked-in Xcode project.
- Custom views, `ButtonStyle`, `Shape`, `Canvas`, `TimelineView`, `NavigationStack`, state and bindings.
- Local SVG/color assets and bundled **Poppins** fonts (see the third-party font license in [`Fonts/OFL.txt`](SwiftUIComponents/Fonts/OFL.txt)).
- Programmatic screens; no third-party dependency manager or package manifest is present in the current repository.

Many controls are demonstration-specific: colors, Turkish UI labels, image names, font names and frame sizes may require adaptation before reuse in another app.

## Open the project

1. Use a compatible **Mac with Xcode** (or inspect the source code on any operating system). This repository targets **iOS 17.4+** according to its checked-in project setting; support on other deployment targets has not been verified.
2. Clone the repository:
   ```bash
   git clone https://github.com/fatihemres/SwiftUI-Components-Library.git
   cd SwiftUI-Components-Library
   ```
3. Open [`SwiftUIComponents.xcodeproj`](SwiftUIComponents.xcodeproj), choose the `SwiftUIComponents` scheme and a supported iOS simulator, then build or run.
4. For a particular UI study, open its source file and use Xcode previews. Inspect required color assets, icons, fonts and extensions before moving code.

### Continuous integration

[GitHub Actions](.github/workflows/ios-build.yml) checks that the **example app builds for the iOS Simulator** using a hosted macOS machine and Xcode 16.4. This is a **build check**, not a unit-test, visual regression test or real-device quality claim. Check the workflow run for actual status.

## Repository map

```text
SwiftUIComponents/
  SwiftUIComponentsApp.swift     # App entry: LoadingTestView
  ContentView.swift             # Composite UI experiment
  Components/                  # Buttons, cards, pickers, text fields, effects
  LoadingTest/                 # Local loading / sample-data demonstration
  Test/                        # NavigationStack coordinator example
  Shapes/                      # Custom SwiftUI shapes
  Extensions/                  # Color and view helpers
  Assets.xcassets/             # Named icons, colors and artwork
  Fonts/                       # Poppins font files and OFL license
SwiftUIComponents.xcodeproj/   # Xcode app project
```

## License and attribution

The author's original material is **proprietary / all rights reserved**; see [LICENSE](LICENSE). Public availability does not grant permission to reuse proprietary components. Fonts, external samples and other third-party assets remain subject to their respective rights and licenses. Verify attribution and third-party permissions before reusing an individual element.
