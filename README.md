# Unit Converter with Navigation — InternCircle Project 04

A Flutter multi-screen unit converter with a home menu and one reusable converter screen for length, weight, and temperature.

## Features

- Home screen with Length, Weight, and Temperature category cards.
- Navigation with `Navigator.push()` and the standard AppBar back button.
- One shared `ConverterPage` receives category configuration as data.
- Dropdown menus to select source and destination units.
- Swap button to exchange the selected units.
- Pure conversion functions outside the widget classes.
- Safe numeric input parsing with `double.tryParse`.
- A visible validation message for invalid input.
- Results rounded to four decimal places for display.
- Assertions run at startup and Flutter unit tests in `test/conversion_test.dart`.

## Conversion data

- Length base unit: metre. 1 km = 1000 m; 1 mile = 1609.344 m; 1 cm = 0.01 m.
- Weight base unit: kilogram. 1 kg = 1000 g; 1 lb = 0.45359237 kg.
- Temperature is converted through Celsius. Fahrenheit = Celsius × 9/5 + 32. Kelvin is also supported.

## Run locally

1. Install Flutter and check `flutter doctor`.
2. Open this project folder in VS Code or Android Studio.
3. Run `flutter pub get`.
4. Run `flutter test`.
5. Run `flutter run`.

## Run in DartPad

1. Open https://dartpad.dev/ and select Flutter mode.
2. Copy all code from `lib/main.dart` into the editor.
3. Press Run.
4. Test all three category cards, dropdowns, swap button, and invalid input.

DartPad's single-file mode runs `main.dart`; the separate `test/conversion_test.dart` file is intended for the full local Flutter project.

## Test cases

| Category | Input | From | To | Expected |
|---|---:|---|---|---:|
| Length | 1 | Kilometre | Metre | 1000 |
| Length | 1 | Mile | Metre | 1609.344 |
| Weight | 1 | Kilogram | Gram | 1000 |
| Weight | 1 | Pound | Kilogram | 0.45359237 |
| Temperature | 100 | Celsius | Fahrenheit | 212 |
| Temperature | 32 | Fahrenheit | Celsius | 0 |
| Temperature | 0 | Celsius | Kelvin | 273.15 |

## Before submitting

- [ ] Home screen shows all three converter categories.
- [ ] Each category opens its converter screen.
- [ ] Back navigation returns to the home screen.
- [ ] Both unit dropdowns work.
- [ ] Swap button exchanges the units.
- [ ] Length, weight, and temperature conversions are correct.
- [ ] Invalid input displays a message rather than crashing.
- [ ] Results display four decimal places.
- [ ] Startup assertions and `flutter test` pass.
- [ ] Capture a screenshot of the home screen and one converter screen.

## Submission items from the learner guide

The guide asks for:
1. Your DartPad link.
2. Screenshots of the home screen and one converter.
3. The assertions you used.

Upload this project to a public GitHub repository and include its link in your InternCircle task submission. Make sure anyone with the link can view it.
