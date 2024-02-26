
# Animated Onboarding Screen Package

This package provides a set of widgets to create beautiful and responsive animated onboarding screens for your Flutter applications. It utilizes the powerful lottie library to display engaging animations and allows you to customize various aspects of the onboarding experience.

## Features

- Easy to use: Define title, subtitle, and animation paths to create onboarding screens.
- Responsive: adapts to different screen sizes and text scales seamlessly.
- Customizable: Change fonts, colors, and animation sizes to match your app's design.
- Two Page Styles: Choose from the standard ```PageBuider``` for single animation or ```UniquePageBuider``` for displaying two animations side-by-side.
- Crossplatfrom support (ios / android)

## Installation

To use this package, add ```animated_onboarding_screen``` as a dependency in your pubspec.yaml file.

```YAML
dependencies:
  flutter:
    sdk: flutter
  animated_onboarding_screen: ^1.0.0
```

Then run ```flutter pub get``` to install package

## Usage

- Import package

```dart
import 'package:animated_onboarding_screen/animated_onboarding_screen.dart';
```

- Create ```PageBuider``` for standard onboarding:

```dart
PageBuider(
  animationPath: 'assets/animations/animation_1.json',
  title: 'Welcome to our app!',
  subtitle: 'Get started with a few simple steps.',
),
```

- Create ```UniquePageBuider``` for dual animation:

```dart
UniquePageBuider(
  uniqueAnimationPath: 'assets/animations/animation_1.json',
  uniqueAnimationPath2: 'assets/animations/animation_2.json',
  uniqueTitle: 'Explore different features',
  uniqueSubTitle: 'Discover the power of our app.',
),
```

- Customize:

```dart
Text(
  title,
  style: GoogleFonts.montserrat(
    fontSize: 20.0,
    fontWeight: FontWeight.bold,
  ),
),
```

- Change the animation size by modifying the ```height``` and ```width``` properties of ```Lottie.asset```.

## Example

```dart
import 'package:flutter/material.dart';
import 'package:animated_onboarding_screen/animated_onboarding_screen.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text('Animated Onboarding Screen Demo'),
        ),
        body: OnboardingScreen(),
      ),
    );
  }
}

class OnboardingScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return PageView(
      children: [
        PageBuilder(
          animationPath: 'assets/animations/animation1.json',
          title: 'Welcome to MyApp',
          subtitle: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.',
        ),
        UniquePageBuilder(
          uniqueAnimationPath: 'assets/animations/animation2.json',
          uniqueAnimationPath2: 'assets/animations/animation3.json',
          uniqueTitle: 'Discover Amazing Features',
          uniqueSubTitle: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.',
        ),
      ],
    );
  }
}

```

## Contributing

We welcome contributions to this package! Please feel free to fork the repository and submit your pull requests..



## Acknowledgements

- [Lottie animation](https://help.lottiefiles.com/hc/en-us/articles/4439877810841-Getting-Started)

## 🚀 About Me

Hi I am [Soumyajit Mukherjee](https://github.com/Sm69mu) & I'm a Flutter developer.
